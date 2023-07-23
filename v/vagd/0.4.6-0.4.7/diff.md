# Comparing `tmp/vagd-0.4.6.tar.gz` & `tmp/vagd-0.4.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vagd-0.4.6.tar", last modified: Tue Jul 18 13:01:54 2023, max compression
+gzip compressed data, was "vagd-0.4.7.tar", last modified: Sun Jul 23 18:26:16 2023, max compression
```

## Comparing `vagd-0.4.6.tar` & `vagd-0.4.7.tar`

### file list

```diff
@@ -1,39 +1,41 @@
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-18 13:01:54.072378 vagd-0.4.6/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)    35149 2023-03-05 14:43:59.000000 vagd-0.4.6/LICENSE
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4389 2023-07-18 13:01:54.072378 vagd-0.4.6/PKG-INFO
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     3805 2023-06-17 16:19:04.000000 vagd-0.4.6/README.md
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      880 2023-07-18 13:01:09.000000 vagd-0.4.6/pyproject.toml
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       38 2023-07-18 13:01:54.072378 vagd-0.4.6/setup.cfg
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-18 13:01:54.065711 vagd-0.4.6/src/
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-18 13:01:54.065711 vagd-0.4.6/src/vagd/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       53 2023-03-20 14:52:11.000000 vagd-0.4.6/src/vagd/__init__.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      220 2023-03-14 11:41:30.000000 vagd-0.4.6/src/vagd/__main__.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      939 2023-06-17 11:38:21.000000 vagd-0.4.6/src/vagd/box.py
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-18 13:01:54.069044 vagd-0.4.6/src/vagd/gdb/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)    20349 2023-03-04 14:19:11.000000 vagd-0.4.6/src/vagd/gdb/__init__.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4178 2023-03-04 12:55:58.000000 vagd-0.4.6/src/vagd/gdb/events.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      983 2023-03-04 12:55:58.000000 vagd-0.4.6/src/vagd/gdb/printing.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       47 2023-03-04 12:55:58.000000 vagd-0.4.6/src/vagd/gdb/prompt.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      865 2023-03-04 12:55:58.000000 vagd-0.4.6/src/vagd/gdb/types.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      135 2023-03-04 12:55:58.000000 vagd-0.4.6/src/vagd/gdb/unwinder.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      844 2023-03-04 12:55:58.000000 vagd-0.4.6/src/vagd/gdb/xmethod.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       44 2023-03-14 14:03:57.000000 vagd-0.4.6/src/vagd/gdb.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1195 2023-04-08 07:51:28.000000 vagd-0.4.6/src/vagd/helper.py
--rwxr-xr-x   0 gfelber   (1000) gfelber   (1000)     1299 2023-07-18 13:00:12.000000 vagd-0.4.6/src/vagd/template.txt
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1307 2023-07-15 07:29:51.000000 vagd-0.4.6/src/vagd/templates.py
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-18 13:01:54.072378 vagd-0.4.6/src/vagd/virts/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      132 2023-03-20 14:52:11.000000 vagd-0.4.6/src/vagd/virts/__init__.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     5773 2023-07-15 07:37:43.000000 vagd-0.4.6/src/vagd/virts/dogd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)    10666 2023-06-17 15:51:31.000000 vagd-0.4.6/src/vagd/virts/pwngd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)    10849 2023-06-17 15:49:55.000000 vagd-0.4.6/src/vagd/virts/qegd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1345 2023-03-20 14:52:11.000000 vagd-0.4.6/src/vagd/virts/shgd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     3592 2023-03-20 14:52:11.000000 vagd-0.4.6/src/vagd/virts/vagd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      843 2023-03-14 14:21:12.000000 vagd-0.4.6/src/vagd/wrapper.py
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-18 13:01:54.069044 vagd-0.4.6/src/vagd.egg-info/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4389 2023-07-18 13:01:54.000000 vagd-0.4.6/src/vagd.egg-info/PKG-INFO
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      678 2023-07-18 13:01:54.000000 vagd-0.4.6/src/vagd.egg-info/SOURCES.txt
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)        1 2023-07-18 13:01:54.000000 vagd-0.4.6/src/vagd.egg-info/dependency_links.txt
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       31 2023-07-18 13:01:54.000000 vagd-0.4.6/src/vagd.egg-info/requires.txt
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)        5 2023-07-18 13:01:54.000000 vagd-0.4.6/src/vagd.egg-info/top_level.txt
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-18 13:01:54.072378 vagd-0.4.6/test/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1206 2023-06-17 15:43:05.000000 vagd-0.4.6/test/test.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    35149 2023-03-05 14:43:59.000000 vagd-0.4.7/LICENSE
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4389 2023-07-23 18:26:16.364571 vagd-0.4.7/PKG-INFO
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     3805 2023-06-17 16:19:04.000000 vagd-0.4.7/README.md
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      900 2023-07-23 18:22:49.000000 vagd-0.4.7/pyproject.toml
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       38 2023-07-23 18:26:16.364571 vagd-0.4.7/setup.cfg
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.357904 vagd-0.4.7/src/
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.361237 vagd-0.4.7/src/vagd/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       53 2023-03-20 14:52:11.000000 vagd-0.4.7/src/vagd/__init__.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      224 2023-07-23 17:47:27.000000 vagd-0.4.7/src/vagd/__main__.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      939 2023-06-17 11:38:21.000000 vagd-0.4.7/src/vagd/box.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/src/vagd/gdb/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    20349 2023-03-04 14:19:11.000000 vagd-0.4.7/src/vagd/gdb/__init__.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4178 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/events.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      983 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/printing.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       47 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/prompt.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      865 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/types.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      135 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/unwinder.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      844 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/xmethod.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       44 2023-03-14 14:03:57.000000 vagd-0.4.7/src/vagd/gdb.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1195 2023-04-08 07:51:28.000000 vagd-0.4.7/src/vagd/helper.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/src/vagd/res/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    12925 2023-07-23 18:20:22.000000 vagd-0.4.7/src/vagd/res/seccomp.json
+-rwxr-xr-x   0 gfelber   (1000) gfelber   (1000)     1371 2023-07-23 17:55:01.000000 vagd-0.4.7/src/vagd/res/template.txt
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1307 2023-07-15 07:29:51.000000 vagd-0.4.7/src/vagd/templates.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/src/vagd/virts/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      132 2023-03-20 14:52:11.000000 vagd-0.4.7/src/vagd/virts/__init__.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     6028 2023-07-23 18:17:58.000000 vagd-0.4.7/src/vagd/virts/dogd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    10666 2023-06-17 15:51:31.000000 vagd-0.4.7/src/vagd/virts/pwngd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    10849 2023-06-17 15:49:55.000000 vagd-0.4.7/src/vagd/virts/qegd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1345 2023-03-20 14:52:11.000000 vagd-0.4.7/src/vagd/virts/shgd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     3592 2023-03-20 14:52:11.000000 vagd-0.4.7/src/vagd/virts/vagd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      843 2023-03-14 14:21:12.000000 vagd-0.4.7/src/vagd/wrapper.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.361237 vagd-0.4.7/src/vagd.egg-info/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4389 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/PKG-INFO
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      708 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/SOURCES.txt
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)        1 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/dependency_links.txt
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       31 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/requires.txt
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)        5 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/top_level.txt
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/test/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1207 2023-07-23 17:36:24.000000 vagd-0.4.7/test/test.py
```

### Comparing `vagd-0.4.6/LICENSE` & `vagd-0.4.7/LICENSE`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/PKG-INFO` & `vagd-0.4.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: vagd
-Version: 0.4.6
+Version: 0.4.7
 Summary: VirtuAlization GDb integrations in pwntools
 Author-email: 0x6fe1be2 <author@example.com>
 Project-URL: Homepage, https://github.com/gfelber/vagd
 Project-URL: Documentation, https://gfelber.github.io/vagd/
 Project-URL: Bug Tracker, https://github.com/gfelber/vagd/issues
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Programming Language :: Python :: 3
```

### Comparing `vagd-0.4.6/README.md` & `vagd-0.4.7/README.md`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/pyproject.toml` & `vagd-0.4.7/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "vagd"
-version = "0.4.6"
+version = "0.4.7"
 authors = [
   { name="0x6fe1be2", email="author@example.com" },
 ]
 description = "VirtuAlization GDb integrations in pwntools"
 readme = "README.md"
 requires-python = ">=3.7"
 dependencies = ['pwntools', 'python-vagrant', 'docker']
@@ -18,15 +18,15 @@
 requires = ["setuptools", "wheel", "pwntools", "python-vagrant", "docker"]
 build-backend = "setuptools.build_meta"
 
 [tool.setuptools.packages.find]
 where = ["src"]
 
 [tool.setuptools.package-data]
-"vagd" = ["template.txt"]
+"vagd.res" = ["template.txt", "seccomp.json"]
 "vagd.gdb" = ["*.pyi"]
 
 
 [project.urls]
 "Homepage" = "https://github.com/gfelber/vagd"
 "Documentation" = "https://gfelber.github.io/vagd/"
 "Bug Tracker" = "https://github.com/gfelber/vagd/issues"
```

### Comparing `vagd-0.4.6/src/vagd/box.py` & `vagd-0.4.7/src/vagd/box.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/gdb/__init__.pyi` & `vagd-0.4.7/src/vagd/gdb/__init__.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/gdb/events.pyi` & `vagd-0.4.7/src/vagd/gdb/events.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/gdb/printing.pyi` & `vagd-0.4.7/src/vagd/gdb/printing.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/gdb/types.pyi` & `vagd-0.4.7/src/vagd/gdb/types.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/gdb/xmethod.pyi` & `vagd-0.4.7/src/vagd/gdb/xmethod.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/helper.py` & `vagd-0.4.7/src/vagd/helper.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/template.txt` & `vagd-0.4.7/src/vagd/res/template.txt`

 * *Files 8% similar despite different names*

```diff
@@ -36,16 +36,17 @@
 def get_target(**kw):
     global vm
     if args.REMOTE:
         context.log_level = 'debug'
         return remote(IP, PORT)
 
     if not vm:
-        vm = Vagd(exe.path, vbox=Box.UBUNTU_FOCAL64, ex=True, fast=True)
+        vm = Dogd(exe.path, image=Box.DOCKER_FOCAL, ex=True, fast=True)
+        # vm = Vagd(exe.path, vbox=Box.UBUNTU_FOCAL64, ex=True, fast=True)
         # vm = Qegd(exe.path, img=Box.CLOUDIMAGE_FOCAL, user='ubuntu', ex=True, fast=True)
-        # vm = Dogd(exe.path, image=Box.DOCKER_FOCAL, ex=True, fast=True)
+        # vm = Shgd(exe.path, user='user', port=22, ex=True, fast=True)
     return vm.start(argv=ARGS, env=ENV, gdbscript=GDB, **kw)
 
 
 t = get_target()
 
 t.interactive()
```

### Comparing `vagd-0.4.6/src/vagd/templates.py` & `vagd-0.4.7/src/vagd/templates.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/virts/dogd.py` & `vagd-0.4.7/src/vagd/virts/dogd.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import os
 import pwn
+import json
 import docker
 
 from vagd import templates, helper
 from vagd.box import Box
 from vagd.virts.shgd import Shgd
 from vagd.virts.pwngd import Pwngd
 from typing import Dict
@@ -74,15 +75,20 @@
 
     def _create_docker_instance(self):
         pwn.log.info('starting docker instance')
         self._port = helper.first_free_port(Dogd.DEFAULT_PORT)
         self._forward.update({'22/tcp': self._port})
         if self._isalpine:
             self._forward.update({f'{Pwngd.STATIC_GDBSRV_PORT}/tcp': Pwngd.STATIC_GDBSRV_PORT})
-        container = self._client.containers.run(self._bimage, ports=self._forward, detach=True, remove=True)
+
+        dir = os.path.dirname(os.path.realpath(__file__))
+        with open(dir[:dir.rfind('/')] + '/res/seccomp.json', 'r') as seccomp_file:
+            seccomp_rules = seccomp_file.read().strip()
+
+        container = self._client.containers.run(self._bimage, ports=self._forward, detach=True, remove=True, security_opt=[f'seccomp:{seccomp_rules}'])
         self._id = container.id
         pwn.log.info(f'started docker instance {container.short_id}')
         with open(Dogd.LOCKFILE, 'w') as lockfile:
             lockfile.write(container.id + ':' + str(self._port))
 
     def _build_image(self):
         pwn.log.info('building docker image')
```

### Comparing `vagd-0.4.6/src/vagd/virts/pwngd.py` & `vagd-0.4.7/src/vagd/virts/pwngd.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/virts/qegd.py` & `vagd-0.4.7/src/vagd/virts/qegd.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/virts/shgd.py` & `vagd-0.4.7/src/vagd/virts/shgd.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/virts/vagd.py` & `vagd-0.4.7/src/vagd/virts/vagd.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd/wrapper.py` & `vagd-0.4.7/src/vagd/wrapper.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.6/src/vagd.egg-info/PKG-INFO` & `vagd-0.4.7/src/vagd.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: vagd
-Version: 0.4.6
+Version: 0.4.7
 Summary: VirtuAlization GDb integrations in pwntools
 Author-email: 0x6fe1be2 <author@example.com>
 Project-URL: Homepage, https://github.com/gfelber/vagd
 Project-URL: Documentation, https://gfelber.github.io/vagd/
 Project-URL: Bug Tracker, https://github.com/gfelber/vagd/issues
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Programming Language :: Python :: 3
```

### Comparing `vagd-0.4.6/src/vagd.egg-info/SOURCES.txt` & `vagd-0.4.7/src/vagd.egg-info/SOURCES.txt`

 * *Files 14% similar despite different names*

```diff
@@ -2,29 +2,30 @@
 README.md
 pyproject.toml
 src/vagd/__init__.py
 src/vagd/__main__.py
 src/vagd/box.py
 src/vagd/gdb.py
 src/vagd/helper.py
-src/vagd/template.txt
 src/vagd/templates.py
 src/vagd/wrapper.py
 src/vagd.egg-info/PKG-INFO
 src/vagd.egg-info/SOURCES.txt
 src/vagd.egg-info/dependency_links.txt
 src/vagd.egg-info/requires.txt
 src/vagd.egg-info/top_level.txt
 src/vagd/gdb/__init__.pyi
 src/vagd/gdb/events.pyi
 src/vagd/gdb/printing.pyi
 src/vagd/gdb/prompt.pyi
 src/vagd/gdb/types.pyi
 src/vagd/gdb/unwinder.pyi
 src/vagd/gdb/xmethod.pyi
+src/vagd/res/seccomp.json
+src/vagd/res/template.txt
 src/vagd/virts/__init__.py
 src/vagd/virts/dogd.py
 src/vagd/virts/pwngd.py
 src/vagd/virts/qegd.py
 src/vagd/virts/shgd.py
 src/vagd/virts/vagd.py
 test/test.py
```

### Comparing `vagd-0.4.6/test/test.py` & `vagd-0.4.7/test/test.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 ENV = {}
 API = True
 GDB = f"""
 b main
 c"""
 
 context.binary = exe = ELF(BINARY, checksec=False)
-context.aslr = True
+context.aslr = False
 
 byt = lambda x: str(x).encode()
 
 
 def vms():
     log.info("Testing Vagrant")
     vm = Vagd(exe.path, vbox=Box.UBUNTU_FOCAL64, tmp=True, fast=True, ex=True)
```

