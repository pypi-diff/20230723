# Comparing `tmp/local_lang-0.0.5.tar.gz` & `tmp/local_lang-0.0.6.tar.gz`

## Comparing `local_lang-0.0.5.tar` & `local_lang-0.0.6.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0      164 2020-02-02 00:00:00.000000 local_lang-0.0.5/locallang/__init__.py
--rw-r--r--   0        0        0     7308 2020-02-02 00:00:00.000000 local_lang-0.0.5/locallang/lang.py
--rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 local_lang-0.0.5/.gitignore
--rw-r--r--   0        0        0    35810 2020-02-02 00:00:00.000000 local_lang-0.0.5/LICENSE
--rw-r--r--   0        0        0       65 2020-02-02 00:00:00.000000 local_lang-0.0.5/README.md
--rw-r--r--   0        0        0      737 2020-02-02 00:00:00.000000 local_lang-0.0.5/pyproject.toml
--rw-r--r--   0        0        0      752 2020-02-02 00:00:00.000000 local_lang-0.0.5/PKG-INFO
+-rw-r--r--   0        0        0      164 2020-02-02 00:00:00.000000 local_lang-0.0.6/locallang/__init__.py
+-rw-r--r--   0        0        0     7344 2020-02-02 00:00:00.000000 local_lang-0.0.6/locallang/lang.py
+-rw-r--r--   0        0        0       16 2020-02-02 00:00:00.000000 local_lang-0.0.6/.gitignore
+-rw-r--r--   0        0        0    35810 2020-02-02 00:00:00.000000 local_lang-0.0.6/LICENSE
+-rw-r--r--   0        0        0     2728 2020-02-02 00:00:00.000000 local_lang-0.0.6/README.md
+-rw-r--r--   0        0        0      733 2020-02-02 00:00:00.000000 local_lang-0.0.6/pyproject.toml
+-rw-r--r--   0        0        0     3411 2020-02-02 00:00:00.000000 local_lang-0.0.6/PKG-INFO
```

### Comparing `local_lang-0.0.5/locallang/lang.py` & `local_lang-0.0.6/locallang/lang.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,21 +1,23 @@
 import json
 import os
 import re
+from typing import Any
 
 try:
     from local.localisation import Localisation
 except:
     print("\n\nPlease restart the app to finish the initialisation !\n\n")
 
 startPrefix = "{"
 endPrefix = "}"
 
 class LangInit:
-    __default_app_lang: str = None
+    __default_app_lang: str | None = None
+
     def __init__(self, default_app_lang: str = "en_us", reload_localisation: bool = True) -> None:
         file_path_exist = os.path.exists("./local/localisation.py")
         default_lang_path_exist = os.path.exists(f"./localisation/{default_app_lang}.json")
         self.__default_app_lang = default_app_lang
 
         if file_path_exist == False:
             os.makedirs("./local", exist_ok=True)
@@ -46,15 +48,15 @@
                 local_json_file.close()
 
                 new_local_json_file = open(f"./local/{l}.json", "w")
                 new_local_json_file.write(json.dumps(json_lang))
                 new_local_json_file.close()
                         
         default_local_json_file = open(f"./localisation/{self.__default_app_lang}.json", "rb")
-        default_json_lang: dict[str, str] = json.loads(default_local_json_file.read())
+        default_json_lang: dict[str, str | Any] = json.loads(default_local_json_file.read())
         default_local_json_file.close()
 
         local_py_file = open("./local/localisation.py", "w")
 
         python_lang = "import json\nfrom datetime import datetime, time\nclass Localisation:\n\t__lang: str\n\tdef __init__(self, lang: str) -> None:\n\t\tself.__lang = lang\n\tdef __get_local_str(self, key: str) -> str | None:\n\t\ttry:\n\t\t\tlang_file = open(f\"./local/{self.__lang}.json\", \"rb\")\n\t\t\tlang_js: dict[str, str] = json.loads(lang_file.read())\n\t\t\tlang_file.close()\n\t\t\treturn lang_js.get(key)\n\t\texcept:\n\t\t\tprint(f\"\\n\\nLocalisation {self.__lang} is not supported\\n\\n\")\n\t\t\treturn None"
 
         if len(default_json_lang.keys()) > 0:
@@ -94,15 +96,14 @@
                                         print(f"`format` key is required for `datetime` or `time` type")
                                         exit(0)
                                 else:
                                     print(f"`{type}` is not a supported type")
                                     exit(0)
                             else:
                                 parameters += f", {pk}: str | int | float | bool | datetime | time"
-
                                 condition += f"\n\t\tif type({pk}) == int or type({pk}) == float or type({pk}) == datetime or type({pk}) == time or type({pk}) == bool:\n\t\t\ttrad = trad.replace(\"{startPrefix}{pk}{endPrefix}\", {pk}.__str__())\n\t\telif type({pk}) == str:\n\t\t\ttrad = trad.replace(\"{startPrefix}{pk}{endPrefix}\", {pk})\n\t\telse:\n\t\t\tprint(f\"`{startPrefix}type({pk}){endPrefix}` is not a supported variable type\")\n\t\t\treturn None"
 
                     allKey: list[str] = re.findall("({[a-zA-Z]*})", value)
 
                     for a in allKey:
                         a = a.replace("{", "").replace("}", "")
                         if usedParam.__contains__(a) == False:
```

### Comparing `local_lang-0.0.5/LICENSE` & `local_lang-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `local_lang-0.0.5/pyproject.toml` & `local_lang-0.0.6/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "local_lang"
-version = "0.0.5"
+version = "0.0.6"
 authors = [
   { name="Maxlanf255", email="developer@pieteraerens.eu" },
 ]
 description = "A small package to localise your python application"
 readme = "README.md"
-requires-python = ">=3.7"
+requires-python = ">=3.8"
 classifiers = [
     "Programming Language :: Python :: 3.11",
     "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
     "Operating System :: OS Independent",
     "Topic :: Software Development :: Localization",
-    "Development Status :: 2 - Pre-Alpha",
+    "Development Status :: 3 - Alpha",
 ]
 
 [project.urls]
 "Homepage" = "https://github.com/maxland255/localisation_lang"
 "Bug Tracker" = "https://github.com/maxland255/localisation_lang/issues"
```

