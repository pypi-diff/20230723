# Comparing `tmp/devpm-1.1.1.tar.gz` & `tmp/devpm-1.2.0.tar.gz`

## Comparing `devpm-1.1.1.tar` & `devpm-1.2.0.tar`

### file list

```diff
@@ -1,32 +1,33 @@
--rw-r--r--   0        0        0     9260 2020-02-02 00:00:00.000000 devpm-1.1.1/devpackage.schema.json
--rw-r--r--   0        0        0      162 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/__init__.py
--rw-r--r--   0        0        0     1379 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/__main__.py
--rw-r--r--   0        0        0      162 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/__init__.py
--rw-r--r--   0        0        0     1046 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/cli/base_command.py
--rw-r--r--   0        0        0     2044 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/cli/main.py
--rw-r--r--   0        0        0     2385 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/__init__.py
--rw-r--r--   0        0        0     1395 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/base_run.py
--rw-r--r--   0        0        0      321 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/cr.py
--rw-r--r--   0        0        0     1796 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/githook.py
--rw-r--r--   0        0        0     3157 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/install.py
--rw-r--r--   0        0        0      274 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/lint.py
--rw-r--r--   0        0        0      445 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/pr.py
--rw-r--r--   0        0        0      277 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/restart.py
--rw-r--r--   0        0        0      602 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/run.py
--rw-r--r--   0        0        0      275 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/start.py
--rw-r--r--   0        0        0      274 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/stop.py
--rw-r--r--   0        0        0      274 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/test.py
--rw-r--r--   0        0        0      719 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/commands/version.py
--rw-r--r--   0        0        0      162 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/utils/__init__.py
--rw-r--r--   0        0        0     1326 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/utils/bash.py
--rw-r--r--   0        0        0     2231 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/utils/bin.py
--rw-r--r--   0        0        0     2694 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/utils/code.py
--rw-r--r--   0        0        0     2399 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/utils/context.py
--rw-r--r--   0        0        0     9179 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/utils/git.py
--rw-r--r--   0        0        0      597 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/utils/log.py
--rw-r--r--   0        0        0     1989 2020-02-02 00:00:00.000000 devpm-1.1.1/devpm/_internal/utils/pip.py
--rw-r--r--   0        0        0     3143 2020-02-02 00:00:00.000000 devpm-1.1.1/.gitignore
--rw-r--r--   0        0        0     1064 2020-02-02 00:00:00.000000 devpm-1.1.1/LICENSE
--rw-r--r--   0        0        0     5403 2020-02-02 00:00:00.000000 devpm-1.1.1/README.md
--rw-r--r--   0        0        0      714 2020-02-02 00:00:00.000000 devpm-1.1.1/pyproject.toml
--rw-r--r--   0        0        0     5892 2020-02-02 00:00:00.000000 devpm-1.1.1/PKG-INFO
+-rw-r--r--   0        0        0     9479 2020-02-02 00:00:00.000000 devpm-1.2.0/devpackage.schema.json
+-rw-r--r--   0        0        0     2432 2020-02-02 00:00:00.000000 devpm-1.2.0/example/version.py
+-rw-r--r--   0        0        0      162 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/__init__.py
+-rw-r--r--   0        0        0     1379 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/__main__.py
+-rw-r--r--   0        0        0      162 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/__init__.py
+-rw-r--r--   0        0        0     1046 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/cli/base_command.py
+-rw-r--r--   0        0        0     2044 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/cli/main.py
+-rw-r--r--   0        0        0     2385 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/__init__.py
+-rw-r--r--   0        0        0     1642 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/base_run.py
+-rw-r--r--   0        0        0      321 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/cr.py
+-rw-r--r--   0        0        0     1796 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/githook.py
+-rw-r--r--   0        0        0     3157 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/install.py
+-rw-r--r--   0        0        0      274 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/lint.py
+-rw-r--r--   0        0        0      445 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/pr.py
+-rw-r--r--   0        0        0      277 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/restart.py
+-rw-r--r--   0        0        0      602 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/run.py
+-rw-r--r--   0        0        0      275 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/start.py
+-rw-r--r--   0        0        0      274 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/stop.py
+-rw-r--r--   0        0        0      274 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/test.py
+-rw-r--r--   0        0        0     3054 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/commands/version.py
+-rw-r--r--   0        0        0      162 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/utils/__init__.py
+-rw-r--r--   0        0        0     1326 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/utils/bash.py
+-rw-r--r--   0        0        0     2231 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/utils/bin.py
+-rw-r--r--   0        0        0     2694 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/utils/code.py
+-rw-r--r--   0        0        0     3684 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/utils/context.py
+-rw-r--r--   0        0        0     9179 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/utils/git.py
+-rw-r--r--   0        0        0      597 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/utils/log.py
+-rw-r--r--   0        0        0     1989 2020-02-02 00:00:00.000000 devpm-1.2.0/devpm/_internal/utils/pip.py
+-rw-r--r--   0        0        0     3143 2020-02-02 00:00:00.000000 devpm-1.2.0/.gitignore
+-rw-r--r--   0        0        0     1064 2020-02-02 00:00:00.000000 devpm-1.2.0/LICENSE
+-rw-r--r--   0        0        0     5403 2020-02-02 00:00:00.000000 devpm-1.2.0/README.md
+-rw-r--r--   0        0        0      708 2020-02-02 00:00:00.000000 devpm-1.2.0/pyproject.toml
+-rw-r--r--   0        0        0     5892 2020-02-02 00:00:00.000000 devpm-1.2.0/PKG-INFO
```

### Comparing `devpm-1.1.1/devpackage.schema.json` & `devpm-1.2.0/devpackage.schema.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.875%*

 * *Differences: {"'properties'": "{'version': OrderedDict([('description', 'Version used for `devpm version` auto "*

 * *                 "increasement.'), ('type', 'string')]), 'versionLoader': OrderedDict([('type', "*

 * *                 "'object'), ('properties', OrderedDict())])}",*

 * * "'title'": "'JSON schema for devpm devpackage.json files'"}*

```diff
@@ -263,17 +263,25 @@
                 },
                 "version": {
                     "$ref": "#/definitions/scriptsVersionBefore"
                 }
             },
             "type": "object"
         },
+        "version": {
+            "description": "Version used for `devpm version` auto increasement.",
+            "type": "string"
+        },
+        "versionLoader": {
+            "properties": {},
+            "type": "object"
+        },
         "vscodeDependencies": {
             "$ref": "#/definitions/vscodeDependency"
         },
         "vscodeUserSettings": {
             "$ref": "#/definitions/vscodeSettings"
         }
     },
-    "title": "JSON schema for devpm package.json files",
+    "title": "JSON schema for devpm devpackage.json files",
     "type": "object"
 }
```

### Comparing `devpm-1.1.1/devpm/__main__.py` & `devpm-1.2.0/devpm/__main__.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/cli/base_command.py` & `devpm-1.2.0/devpm/_internal/cli/base_command.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/cli/main.py` & `devpm-1.2.0/devpm/_internal/cli/main.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/commands/__init__.py` & `devpm-1.2.0/devpm/_internal/commands/__init__.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/commands/base_run.py` & `devpm-1.2.0/devpm/_internal/commands/base_run.py`

 * *Files 9% similar despite different names*

```diff
@@ -23,29 +23,35 @@
         print("Available scripts:")
         for name in scripts:
             print(f"  {name}")
             print(f"    {scripts[name]}")
         exit(1)
 
 
-    def run_script_group(self, name: str | None, args=None) -> None:
-        config = self.context.load_config()
+    def run_script_group(self, name: str | None, args=None, config: dict={}) -> None:
+        if not config:
+            config = self.context.load_config()
         scripts = {}
         if 'scripts' in config:
             scripts = config['scripts']
         if not name:
             # show scripts
             self.show_scripts(scripts)
         if not name in scripts:
             print(f"Missing script \"{name}\".\n")
             self.show_scripts(scripts)
-        self.run_script(f"pre{name}", scripts, args)
-        self.run_script(name, scripts, args)
-        self.run_script(f"post{name}", scripts, args)
+        self.run_script(f"pre{name}", scripts, config, args)
+        ret = self.run_script(name, scripts, config, args)
+        if ret != 0:
+            exit(ret)
+        self.run_script(f"post{name}", scripts, config, args)
 
 
-    def run_script(self, name: str, scripts: list[str], args=None) -> None:
+    def run_script(self, name: str, scripts: dict, config: dict={}, args=None) -> int:
         if name in scripts:
-            script = scripts[name]
+            script = self.context.evaluate(scripts[name], config)
             if args:
                 script += ' ' + ' '.join(args)
-            os.system(script)
+            print(f"> {name}")
+            print(f"> {script}")
+            return os.system(script)
+        return 0
```

### Comparing `devpm-1.1.1/devpm/_internal/commands/githook.py` & `devpm-1.2.0/devpm/_internal/commands/githook.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/commands/install.py` & `devpm-1.2.0/devpm/_internal/commands/install.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/commands/run.py` & `devpm-1.2.0/devpm/_internal/commands/run.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/utils/bash.py` & `devpm-1.2.0/devpm/_internal/utils/bash.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/utils/bin.py` & `devpm-1.2.0/devpm/_internal/utils/bin.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/utils/code.py` & `devpm-1.2.0/devpm/_internal/utils/code.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/utils/context.py` & `devpm-1.2.0/devpm/_internal/utils/context.py`

 * *Files 24% similar despite different names*

```diff
@@ -5,52 +5,68 @@
 # Copyright (c) 2023 wequick
 # This software is distributed under the MIT license.
 
 # System context manager
 
 import json
 import os
+import re
 import subprocess
 import sys
 from devpm._internal.utils.git import Git
 from devpm._internal.utils.bash import Bash
 from devpm._internal.utils.log import Log
 from devpm._internal.utils.code import Code
 from devpm._internal.utils.pip import Pip
 
 
 class Context:
     def __init__(self):
         self.cwd = os.getcwd()
+        self.config_name = 'devpackage.json'
         self.log = Log()
         self.code = Code()
         self.pip = Pip()
         self.bash = Bash()
         self.git = Git()
 
+
+    def get_config_name(self) -> str:
+        return self.config_name
+
+
     def load_config(self) -> dict:
         config = {}
         if not sys.stdin.isatty():
             # Read from stdin
             s = ''
             for line in sys.stdin:
                 s += line.strip()
             try:
                 config = json.loads(s)
             except:
                 self.log.abort('Invalid config data')
         else:
             # Read from file
-            config_file = os.path.join(self.cwd, 'devpackage.json')
+            config_file = os.path.join(self.cwd, self.config_name)
             if not os.path.exists(config_file):
-                self.log.abort('devpackage.json no found.')
+                self.log.abort(f'Missing {self.config_name}.')
             with open(config_file, 'r', encoding='utf-8') as file:
                 config = json.load(file)
         return config
 
+
+    def write_config(self, config) -> bool:
+        config_file = os.path.join(self.cwd, self.config_name)
+        if not os.path.exists(config_file):
+            self.log.abort(f'Missing {self.config_name}.')
+        with open(config_file, 'w', encoding='utf-8') as file:
+            json.dump(config, file, indent=2)
+
+
     def check_install_exe(self, exe, url):
         installed_ver = None
         args = [exe, '-h']
         try:
             p = subprocess.Popen(args, stdout=subprocess.PIPE, stderr=subprocess.PIPE)
             output, error = p.communicate()
             if p.returncode != 1:
@@ -61,22 +77,46 @@
                 if len(output) > 0:
                     lines = output.splitlines()
                     installed_ver = lines[0]
         except:
             pass
         return installed_ver
 
-    def evaluate(self, exp, cwd):
-        if not exp or exp[0] != '$':
-            return exp
+
+    def evaluate_package_config(self, exp, config: dict={}) -> str:
+        def get_package_config(match_obj):
+            if match_obj.group() is not None:
+                s = match_obj.group(2)
+                arr = s[1:].split('.')
+                val = config
+                for key in arr:
+                    if not key in val:
+                        val = None
+                        break
+                    val = val[key]
+                return str(val) if val else match_obj.group()
+        return re.sub(r"(\$devpackage((\.[\d|\w|_]+){1,}))", get_package_config, exp)
+
+
+    def evaluate_func(self, exp) -> str:
         index = exp.find(':', 1)
         if index > 0:
             func = exp[1:index]
             args = exp[index+1:]
         else:
             func = exp[1:]
             args = None
         if func == 'pip.which':
             return self.pip.which(args)
         elif func == 'bash.which':
             return self.bash.which(args)
-        return None
+        return exp
+
+
+    def evaluate(self, exp, config: dict={}) -> str:
+        if not exp or not '$' in exp:
+            return exp
+        # evaluate devpackage.json
+        value = self.evaluate_package_config(exp, config)
+        # evaluate functions
+        value = self.evaluate_func(value)
+        return value
```

### Comparing `devpm-1.1.1/devpm/_internal/utils/git.py` & `devpm-1.2.0/devpm/_internal/utils/git.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/utils/log.py` & `devpm-1.2.0/devpm/_internal/utils/log.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/devpm/_internal/utils/pip.py` & `devpm-1.2.0/devpm/_internal/utils/pip.py`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/.gitignore` & `devpm-1.2.0/.gitignore`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/LICENSE` & `devpm-1.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/README.md` & `devpm-1.2.0/README.md`

 * *Files identical despite different names*

### Comparing `devpm-1.1.1/PKG-INFO` & `devpm-1.2.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: devpm
-Version: 1.1.1
+Version: 1.2.0
 Summary: Development package manager
 Project-URL: Homepage, https://github.com/wequick/devpm
 Project-URL: Bug Tracker, https://github.com/wequick/devpm/issues
 Author-email: Galen Lin <oolgloo.2012@gmail.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

