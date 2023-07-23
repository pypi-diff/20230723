# Comparing `tmp/brishgarden-0.2.3.tar.gz` & `tmp/brishgarden-0.2.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "brishgarden-0.2.3.tar", max compression
+gzip compressed data, was "brishgarden-0.2.3.1.tar", max compression
```

## Comparing `brishgarden-0.2.3.tar` & `brishgarden-0.2.3.1.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0      993 2021-04-08 09:23:10.867216 brishgarden-0.2.3/brishgarden/__init__.py
--rw-r--r--   0        0        0     9629 2021-04-09 13:23:05.704554 brishgarden-0.2.3/brishgarden/garden.py
--rw-r--r--   0        0        0     1037 2021-04-09 13:23:15.501898 brishgarden-0.2.3/pyproject.toml
--rw-r--r--   0        0        0      990 2021-04-09 13:23:37.818642 brishgarden-0.2.3/setup.py
--rw-r--r--   0        0        0      793 2021-04-09 13:23:37.818956 brishgarden-0.2.3/PKG-INFO
+-rw-r--r--   0        0        0      583 2021-09-30 22:13:41.001363 brishgarden-0.2.3.1/brishgarden/__init__.py
+-rw-r--r--   0        0        0     8519 2022-06-12 11:26:47.199547 brishgarden-0.2.3.1/brishgarden/garden.py
+-rw-r--r--   0        0        0      861 2023-07-23 15:50:58.965821 brishgarden-0.2.3.1/pyproject.toml
+-rw-r--r--   0        0        0     1053 1970-01-01 00:00:00.000000 brishgarden-0.2.3.1/setup.py
+-rw-r--r--   0        0        0      975 1970-01-01 00:00:00.000000 brishgarden-0.2.3.1/PKG-INFO
```

### Comparing `brishgarden-0.2.3/brishgarden/garden.py` & `brishgarden-0.2.3.1/brishgarden/garden.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,139 +1,53 @@
-import logging, os, time
-import functools
-from concurrent.futures import ThreadPoolExecutor
-import asyncio
+import logging
+import os
+import time
 import brish
-from brish import CmdResult, z, zp, UninitializedBrishException
-
-
-def zn(*a, getframe=3, **kw):
-    # runs my personal commands
-    if os.environ.get("NIGHTDIR"):
-        return z(*a, **kw, getframe=getframe)
-    else:
-        return None
-
+from brish import CmdResult, z, zp, UninitializedBrishException, zn
+from pynight.common_async import force_async, async_max_workers_set
+from pynight.common_fastapi import FastAPISettings, EndpointLoggingFilter1, request_path_get, check_ip
+from pynight.common_telegram import log_tlg
 
 import traceback
 import re
 from typing import Optional
 from collections.abc import Iterable
 
 from fastapi import FastAPI, Response, Request
-from pydantic import BaseSettings
-
-##
-# ix_flag = False
-
-
-# def ix():
-#     global ix_flag
-#     if not ix_flag:
-#         import nest_asyncio
-
-#         nest_asyncio.apply()
-#         ix_flag = True
-
-
-def embed2():
-    # from IPython import embed
-    # ix()
-    # embed(using='asyncio')
-    # from ipydex import IPS, ip_syshook, ST, activate_ips_on_exception, dirsearch
-    # IPS()
-    print("None of these work at all with uvicorn's loop.")
-
-
-##
-def force_async(f):
-    @functools.wraps(f)
-    def inner(*args, **kwargs):
-        loop = asyncio.get_running_loop()
-        return loop.run_in_executor(None, lambda: f(*args, **kwargs))
-
-    return inner
-
-
-##
-
-
-class Settings(BaseSettings):
-    # disabling the docs
-    openapi_url: str = ""  # "/openapi.json"
-
-
-settings = Settings()
 
+settings = FastAPISettings()
 app = FastAPI(openapi_url=settings.openapi_url)
+
 logger = logging.getLogger("uvicorn")  # alt: from uvicorn.config import logger
+
 isDbg = os.environ.get(
     "BRISHGARDEN_DEBUGME", False
 )  # we can't reuse 'DEBUGME' or it will pollute all the brishes
 if isDbg:
     logger.info("Debug mode enabled")
 
-
-class EndpointFilter(logging.Filter):
-    def filter(self, record: logging.LogRecord) -> bool:
-        try:
-            if isDbg:
-                # logger.info(f"LogRecord:\n{record.__dict__}")
-                return True
-            ##
-            # msg: str = record.getMessage()
-            # return msg.find("/zsh/nolog/") == -1
-            ##
-            if hasattr(record, "scope"):
-                return record.scope.get("path", "") != "/zsh/nolog/"
-            else:
-                return not (record.args[2] in ("/zsh/nolog/", "/api/v1/zsh/nolog/"))
-        except:
-            res = traceback.format_exc()
-            try:
-                res += f"\n\nLogRecord:\n{record.__dict__}"
-                ##
-                msg: str = record.getMessage()
-                res += f"\n\nmsg:\n{msg}"
-                res += f"\n{msg.__dict__}"
-            except:
-                pass
-
-            logger.warning(res)
-            return True
-
-
-logging.getLogger("uvicorn.access").addFilter(EndpointFilter())
-# Our usage of internal zsh APIs will fail gracefully on foreign systems.
-myip = zn("myip")
-seenIPs = {"127.0.0.1", myip.out.strip() if myip else ""}
-
-
-def newBrish(**kwargs):
-    return brish.Brish(
-        # FORCE_INTERACTIVE is set by tmuxnewsh2
-        boot_cmd="export GARDEN_ZSH=y ; unset FORCE_INTERACTIVE ; mkdir -p ~/tmp/garden/ ; cd ~/tmp/garden/ ",
-        **kwargs,
-    )
-
-
+skip_paths=("/zsh/nolog/", "/api/v1/zsh/nolog/")
+logging.getLogger("uvicorn.access").addFilter(EndpointLoggingFilter1(isDbg=isDbg, logger=logger, skip_paths=skip_paths))
+###
 brishes_n_default = 16
 try:
     brishes_n = int(os.environ.get("BRISHGARDEN_N", brishes_n_default))
 except:
     brishes_n = brishes_n_default
 
-loop = asyncio.get_running_loop()
-executor = ThreadPoolExecutor(max_workers=(brishes_n + 16))
-loop.set_default_executor(executor)
+executor = async_max_workers_set(brishes_n + 16)
+###
+def newBrish(session="", **kwargs):
+    return brish.Brish(
+        #: FORCE_INTERACTIVE is set by tmuxnewsh2
+        boot_cmd="export GARDEN_ZSH=y ; export GARDEN_SESSION={session} ; unset FORCE_INTERACTIVE ; garden_root=~/tmp/garden/ ; mkdir -p $garden_root ; cd $garden_root ",
+        **kwargs,
+    )
 
-logger.info(f"Initializing {brishes_n} brishes ...")
 brish_server = None
-
-
 def brish_server_cleanup(brish_server):
     try:
         if brish_server:
             if isinstance(brish_server, Iterable):
                 for b, _ in brish_server:
                     try:
                         b.cleanup()
@@ -146,15 +60,15 @@
 
 
 def init_brishes(erase_sessions=True):
     global brish_server, brishes, allBrishes
 
     brishes = []  # helps avoid UninitializedBrishException
     if erase_sessions:
-        if allBrishes:
+        if allBrishes:  # @noflycheck
             executor.submit(lambda: brish_server_cleanup(allBrishes.values()))
             # https://docs.python.org/3/library/concurrent.futures.html
     else:
         executor.submit(lambda: brish_server_cleanup(brish_server))
 
     brish_server = newBrish(server_count=brishes_n)
     brishes = [i for i in range(brishes_n)]
@@ -163,18 +77,19 @@
         allBrishes = new_brishes
     else:
         allBrishes.update(new_brishes)
 
 
 allBrishes = None
 brish_server = None
+logger.info(f"Initializing {brishes_n} brishes ...")
 init_brishes()
-zn("bell-sc2-nav_online")
-
+zn("bell_awaysh=no bell-sc2-nav_online || true")
 
+###
 @app.get("/")
 def read_root():
     return {"Hello": "World"}
 
 
 @app.post("/test/")
 def test(body: dict):
@@ -187,129 +102,139 @@
     return Response(content=ans, media_type="text/plain")
 
 
 @app.get("/request/ip/")
 async def get_ip(request: Request):
     ans = request.client.host
     return Response(content=ans, media_type="text/plain")
-
-
-pattern_magic = re.compile(r"(?im)^%GARDEN_(\S+)\s+((?:.|\n)*)$")
-
+###
+pattern_magic = re.compile(r"(?im)^%GARDEN_(\S+)\s+((?:.|\n)*)$") # @duplicateCode/86da52eced14bf6baa394f50a9601812
 
 @app.post("/zsh/")
 @app.post("/zsh/nolog/")
 def cmd_zsh(body: dict, request: Request):
-    # GET Method: cmd: str, verbose: Optional[int] = 0
-    # body: cmd [verbose: int=0,1] [stdin: str]
-    first_seen = False
-    ip = request.client.host
-    if not (ip in seenIPs):
-        first_seen = True
-        logger.warning(f"New IP seen: {ip}")
-        # We log the IP separately, to be sure that an injection attack can't stop the message.
-        zn("tsend -- {os.environ.get('tlogs')} 'New IP seen by the Garden: '{ip}")
-        seenIPs.add(ip)
-
-    session = body.get("session", "")
-    cmd = body.get("cmd", "")
-    stdin = body.get("stdin", "")
-    json_output = int(
-        body.get("json_output", body.get("verbose", 0))
-    )  # old API had this named 'verbose'
-    ##
-    nolog = (
-        not isDbg and ip == "127.0.0.1" and bool(body.get("nolog", ""))
-    )  # Use /zsh/nolog/ to hide the access logs.
-    log_level = int(body.get("log_level", 1))
-    if isDbg:
-        log_level = max(log_level, 100)
-    ##
-
-    log = f"{ip} - cmd: {cmd}, session: {session}, stdin: {stdin[0:100]}, brishes: {len(brishes)}, allBrishes: {len(allBrishes)}"
-    nolog or logger.info(log)
-    first_seen and zn("tsend -- {os.environ.get('tlogs')} {log}")
-
-    if cmd == "":
-        return Response(content="Empty command received.", media_type="text/plain")
-    magic_matches = pattern_magic.match(cmd)
-    if magic_matches is not None:
-        magic_head = magic_matches.group(1)
-        magic_exp = magic_matches.group(2)
-        log = f"Magic received: {magic_head}"
-        logger.info(log)
-        if magic_head == "ALL":
-            init_brishes()
-        else:
-            log += "\nUnknown magic!"
-            logger.warning("Unknown magic!")
+    try:
+        # GET Method: cmd: str, verbose: Optional[int] = 0
+        # body: cmd [verbose: int=0,1] [stdin: str]
+        ##
+        # print(body)
+        # print(request.__dict__)
+        ##
+        ip, first_seen = check_ip(request, logger=logger)
+        req_path = request_path_get(request)
+
+        session = body.get("session", "")
+        cmd = body.get("cmd", "")
+        stdin = body.get("stdin", "")
+        json_output = int(
+            body.get("json_output", body.get("verbose", 0))
+        )  # old API had this named 'verbose'
+        ##
+        nolog = (
+            not isDbg and ip == "127.0.0.1" and
+            (bool(body.get("nolog", "")) or (req_path in skip_paths))
+        )  # Use /zsh/nolog/ to hide the access logs.
+
+        log_level = int(body.get("log_level", 1))
+        if isDbg:
+            log_level = max(log_level, 100)
+
+        failure_expected = bool(body.get("failure_expected", False))
+        ##
+
+        log = f"{ip} - cmd: {cmd}, session: {session}, stdin: {stdin[0:100]}, brishes: {len(brishes)}, allBrishes: {len(allBrishes)}"
+        if failure_expected:
+            log+=", failure_expected"
+
+        nolog or logger.info(log)
+        first_seen and log_tlg(log)
+
+        if cmd == "":
+            return Response(content="Empty command received.", media_type="text/plain")
+        magic_matches = pattern_magic.match(cmd)
+        if magic_matches is not None:
+            magic_head = magic_matches.group(1)
+            magic_exp = magic_matches.group(2)
+            log = f"Magic received: {magic_head}"
+            logger.info(log)
+            if magic_head == "ALL":
+                init_brishes()
+            else:
+                log += "\nUnknown magic!"
+                logger.warning("Unknown magic!")
 
-        return Response(content=log, media_type="text/plain")
+            return Response(content=log, media_type="text/plain")
+
+        while True:
+            if session:
+                # @design garbage collect
+                myBrish, server_index = allBrishes.get(session, (None, None))
+                if not myBrish:
+                    myBrish, server_index = allBrishes.setdefault(
+                        session, (newBrish(session=session, server_count=1), 0)
+                    )  # is atomic https://bugs.python.org/issue13521#:~:text=setdefault()%20was%20intended%20to,()%20which%20can%20call%20arbitrary
+            else:
+                while len(brishes) <= 0:
+                    time.sleep(1)
+                myBrish = brish_server
+                server_index = brishes.pop()
+            ###
+            res: CmdResult
+            try:
+                if json_output == 0:
+                    # we need to output a single string, so we can't need to put stderr and stdout together
+                    res = myBrish.z(
+                        "{{ eval {cmd} }} 2>&1",
+                        fork=False,
+                        cmd_stdin=stdin,
+                        server_index=server_index,
+                    )
+                else:
+                    res = myBrish.send_cmd(
+                        cmd, fork=False, cmd_stdin=stdin, server_index=server_index
+                    )
+            except UninitializedBrishException:
+                if log_level >= 2:
+                    logger.info("Encountered UninitializedBrishException")
 
-    while True:
-        if session:
-            # @design garbage collect
-            myBrish, server_index = allBrishes.get(session, (None, None))
-            if not myBrish:
-                myBrish, server_index = allBrishes.setdefault(
-                    session, (newBrish(server_count=1), 0)
-                )  # is atomic https://bugs.python.org/issue13521#:~:text=setdefault()%20was%20intended%20to,()%20which%20can%20call%20arbitrary
-        else:
-            while len(brishes) <= 0:
                 time.sleep(1)
-            myBrish = brish_server
-            server_index = brishes.pop()
+                continue
+            except:
+                res = CmdResult(9000, "", traceback.format_exc(), cmd, stdin)
+                log_level = max(log_level, 101)
+
+            if not session and not (server_index in brishes):
+                # duplicate brishes might be added here because of race conditions, but as brishes have their own locking, this doesn't matter, as we garbage-collect the dups here
+                brishes.append(server_index)
+
+            break
         ###
-        res: CmdResult
-        try:
-            if json_output == 0:
-                # we need to output a single string, so we can't need to put stderr and stdout together
-                res = myBrish.z(
-                    "{{ eval {cmd} }} 2>&1",
-                    fork=False,
-                    cmd_stdin=stdin,
-                    server_index=server_index,
-                )
-            else:
-                res = myBrish.send_cmd(
-                    cmd, fork=False, cmd_stdin=stdin, server_index=server_index
-                )
-        except UninitializedBrishException:
-            if log_level >= 2:
-                logger.info("Encountered UninitializedBrishException")
-
-            time.sleep(1)
-            continue
-        except:
-            res = CmdResult(9000, "", traceback.format_exc(), cmd, stdin)
-            log_level = max(log_level, 101)
-
-        if not session and not (server_index in brishes):
-            # duplicate brishes might be added here because of race conditions, but as brishes have their own locking, this doesn't matter, as we garbage-collect the dups here
-            brishes.append(server_index)
-
-        break
-    ###
-    if res.retcode != 0:
-        if log_level >= 1:
-            nolog or logger.warning(f"Command failed:\n{res.longstr}")
+        if not failure_expected and res.retcode != 0:
             if log_level >= 1:
-                zn(
-                    """isLocal && {{ tts-glados1-cached "A command has failed." ; bello }} &>/dev/null </dev/null &"""
-                )
+                nolog or logger.warning(f"Command failed:\n{res.longstr}")
+                if log_level >= 1:
+                    zn(
+                        """
+                        if isMe && isLocal ; then
+                           {{ tts-glados1-cached "A command has failed." ; bello }} &>/dev/null </dev/null &
+                        fi
+                        """
+                    )
 
-    if json_output == 0:
-        return Response(content=res.outerr, media_type="text/plain")
-    else:
-        return {
-            "cmd": cmd,
-            "session": session,
-            "brishes": len(brishes),
-            "allBrishes": len(allBrishes),
-            "out": res.out,
-            "err": res.err,
-            "retcode": res.retcode,
-        }
+        if json_output == 0:
+            return Response(content=res.outerr, media_type="text/plain")
+        else:
+            return {
+                "cmd": cmd,
+                "session": session,
+                "brishes": len(brishes),
+                "allBrishes": len(allBrishes),
+                "out": res.out,
+                "err": res.err,
+                "retcode": res.retcode,
+            }
+    except:
+        logger.warning(traceback.format_exc())
 
 
-# Old security scheme: (We now use Caddy's HTTP auth.)
+## Old security scheme: (We now use Caddy's HTTP auth.)
 # Use `pass: str`, hash it a lot along BRISHGARDEN_SALT, and compare to BRISHGARDEN_PASS. Abort if any of the two vars are empty. We probably need to answer the query right away for this security model to work, because hashing necessarily needs to be expensive.
```

### Comparing `brishgarden-0.2.3/pyproject.toml` & `brishgarden-0.2.3.1/pyproject.toml`

 * *Files 21% similar despite different names*

```diff
@@ -1,38 +1,24 @@
 [tool.poetry]
 name = "brishgarden"
-version = "0.2.3"
+version = "0.2.3.1"
 description = "BrishGarden uses Brish to serve an HTTP API that can execute interpreted code (that would otherwise need expensive startup costs) fast. It's also useful as a remote code executor."
 authors = ["NightMachinary <rudiwillalwaysloveyou@gmail.com>"]
 license = "MIT"
 
 [tool.poetry.dependencies]
-python = ">=3.7"
+python = ">=3.7,<4.0"
 python-multipart = ">=0.0.5"
 # brish = {git = "https://github.com/NightMachinary/brish.git"}
 fastapi = {extras = ["all"], version = ">=0.60"}
+pydantic-settings = "^2.0.2"
 passlib = {extras = ["bcrypt", "argon2"], version = ">=1.7"}
 python-jose = {extras = ["cryptography"], version = ">=3.1"}
 brish = "*"
-##
-# did not fix `ModuleNotFoundError: No module named 'setuptools'` after all
-# setuptools = "<50"
-# `pi 'setuptools<50'`
-##
+pynight = "*"
 
 [tool.poetry.scripts]
 brishgarden = 'brishgarden:main'
 
-
-
-
-
-
-
-
-[tool.dephell.main]
-from = {format = "poetry", path = "pyproject.toml"}
-to = {format = "setuppy", path = "setup.py"}
-
 [build-system]
-requires = ["poetry>=0.12"]
-build-backend = "poetry.masonry.api"
+requires = [  "setuptools", "poetry_core>=1.0"]
+build-backend = "poetry.core.masonry.api"
```

### Comparing `brishgarden-0.2.3/setup.py` & `brishgarden-0.2.3.1/setup.py`

 * *Files 13% similar despite different names*

```diff
@@ -7,32 +7,34 @@
 package_data = \
 {'': ['*']}
 
 install_requires = \
 ['brish',
  'fastapi[all]>=0.60',
  'passlib[argon2,bcrypt]>=1.7',
+ 'pydantic-settings>=2.0.2,<3.0.0',
+ 'pynight',
  'python-jose[cryptography]>=3.1',
  'python-multipart>=0.0.5']
 
 entry_points = \
 {'console_scripts': ['brishgarden = brishgarden:main']}
 
 setup_kwargs = {
     'name': 'brishgarden',
-    'version': '0.2.3',
+    'version': '0.2.3.1',
     'description': "BrishGarden uses Brish to serve an HTTP API that can execute interpreted code (that would otherwise need expensive startup costs) fast. It's also useful as a remote code executor.",
-    'long_description': None,
+    'long_description': 'None',
     'author': 'NightMachinary',
     'author_email': 'rudiwillalwaysloveyou@gmail.com',
-    'maintainer': None,
-    'maintainer_email': None,
-    'url': None,
+    'maintainer': 'None',
+    'maintainer_email': 'None',
+    'url': 'None',
     'packages': packages,
     'package_data': package_data,
     'install_requires': install_requires,
     'entry_points': entry_points,
-    'python_requires': '>=3.7',
+    'python_requires': '>=3.7,<4.0',
 }
 
 
 setup(**setup_kwargs)
```

