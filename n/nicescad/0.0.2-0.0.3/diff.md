# Comparing `tmp/nicescad-0.0.2.tar.gz` & `tmp/nicescad-0.0.3.tar.gz`

## Comparing `nicescad-0.0.2.tar` & `nicescad-0.0.3.tar`

### file list

```diff
@@ -1,24 +1,71 @@
--rw-r--r--   0        0        0      362 2020-02-02 00:00:00.000000 nicescad-0.0.2/.project
--rw-r--r--   0        0        0      455 2020-02-02 00:00:00.000000 nicescad-0.0.2/.pydevproject
--rw-r--r--   0        0        0     1180 2020-02-02 00:00:00.000000 nicescad-0.0.2/.github/workflows/build.yml
--rw-r--r--   0        0        0      629 2020-02-02 00:00:00.000000 nicescad-0.0.2/.github/workflows/upload-to-pypi.yml
--rw-r--r--   0        0        0      506 2020-02-02 00:00:00.000000 nicescad-0.0.2/examples/openjscad_logo.scad
--rw-r--r--   0        0        0   495635 2020-02-02 00:00:00.000000 nicescad-0.0.2/examples/openjscad_logo.stl
--rw-r--r--   0        0        0       19 2020-02-02 00:00:00.000000 nicescad-0.0.2/nicescad/__init__.py
--rw-r--r--   0        0        0     3447 2020-02-02 00:00:00.000000 nicescad-0.0.2/nicescad/local_filepicker.py
--rw-r--r--   0        0        0     2898 2020-02-02 00:00:00.000000 nicescad-0.0.2/nicescad/nicescad_cmd.py
--rw-r--r--   0        0        0     4510 2020-02-02 00:00:00.000000 nicescad-0.0.2/nicescad/openscad.py
--rw-r--r--   0        0        0      804 2020-02-02 00:00:00.000000 nicescad-0.0.2/nicescad/profiler.py
--rw-r--r--   0        0        0      880 2020-02-02 00:00:00.000000 nicescad-0.0.2/nicescad/version.py
--rw-r--r--   0        0        0     7065 2020-02-02 00:00:00.000000 nicescad-0.0.2/nicescad/webserver.py
--rwxr-xr-x   0        0        0     2023 2020-02-02 00:00:00.000000 nicescad-0.0.2/scripts/doc
--rwxr-xr-x   0        0        0       78 2020-02-02 00:00:00.000000 nicescad-0.0.2/scripts/install
--rwxr-xr-x   0        0        0      135 2020-02-02 00:00:00.000000 nicescad-0.0.2/scripts/test
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 nicescad-0.0.2/tests/__init__.py
--rw-r--r--   0        0        0     1022 2020-02-02 00:00:00.000000 nicescad-0.0.2/tests/basetest.py
--rw-r--r--   0        0        0      681 2020-02-02 00:00:00.000000 nicescad-0.0.2/tests/test_openscad.py
--rw-r--r--   0        0        0     3078 2020-02-02 00:00:00.000000 nicescad-0.0.2/.gitignore
--rw-r--r--   0        0        0    11357 2020-02-02 00:00:00.000000 nicescad-0.0.2/LICENSE
--rw-r--r--   0        0        0     1160 2020-02-02 00:00:00.000000 nicescad-0.0.2/README.md
--rw-r--r--   0        0        0     1558 2020-02-02 00:00:00.000000 nicescad-0.0.2/pyproject.toml
--rw-r--r--   0        0        0     2458 2020-02-02 00:00:00.000000 nicescad-0.0.2/PKG-INFO
+-rw-r--r--   0        0        0      362 2020-02-02 00:00:00.000000 nicescad-0.0.3/.project
+-rw-r--r--   0        0        0      455 2020-02-02 00:00:00.000000 nicescad-0.0.3/.pydevproject
+-rw-r--r--   0        0        0     1180 2020-02-02 00:00:00.000000 nicescad-0.0.3/.github/workflows/build.yml
+-rw-r--r--   0        0        0      629 2020-02-02 00:00:00.000000 nicescad-0.0.3/.github/workflows/upload-to-pypi.yml
+-rw-r--r--   0        0        0       19 2020-02-02 00:00:00.000000 nicescad-0.0.3/nicescad/__init__.py
+-rw-r--r--   0        0        0     3447 2020-02-02 00:00:00.000000 nicescad-0.0.3/nicescad/local_filepicker.py
+-rw-r--r--   0        0        0     3168 2020-02-02 00:00:00.000000 nicescad-0.0.3/nicescad/nicescad_cmd.py
+-rw-r--r--   0        0        0     8540 2020-02-02 00:00:00.000000 nicescad-0.0.3/nicescad/openscad.py
+-rw-r--r--   0        0        0     1939 2020-02-02 00:00:00.000000 nicescad-0.0.3/nicescad/process.py
+-rw-r--r--   0        0        0      804 2020-02-02 00:00:00.000000 nicescad-0.0.3/nicescad/profiler.py
+-rw-r--r--   0        0        0      883 2020-02-02 00:00:00.000000 nicescad-0.0.3/nicescad/version.py
+-rw-r--r--   0        0        0    16337 2020-02-02 00:00:00.000000 nicescad-0.0.3/nicescad/webserver.py
+-rw-r--r--   0        0        0     4454 2020-02-02 00:00:00.000000 nicescad-0.0.3/nicescad/web/static/css/pygments.css
+-rw-r--r--   0        0        0     1093 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/intersection.scad
+-rw-r--r--   0        0        0      506 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openjscad_logo.scad
+-rw-r--r--   0        0        0   495635 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openjscad_logo.stl
+-rw-r--r--   0        0        0     1043 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/GEB.scad
+-rw-r--r--   0        0        0      895 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/advance_intersection.scad
+-rw-r--r--   0        0        0     3034 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/animation.scad
+-rw-r--r--   0        0        0     1258 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/demo_cut.scad
+-rw-r--r--   0        0        0     2501 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/difference.scad
+-rw-r--r--   0        0        0     1159 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/fractal.scad
+-rw-r--r--   0        0        0      665 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/intersecting.scad
+-rw-r--r--   0        0        0     1648 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/iteration.scad
+-rw-r--r--   0        0        0     1746 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/module_recursion.scad
+-rw-r--r--   0        0        0     1087 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/offset.scad
+-rw-r--r--   0        0        0     1305 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/search.scad
+-rw-r--r--   0        0        0      954 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Advanced/translation.scad
+-rw-r--r--   0        0        0     2503 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/CSG-modules.scad
+-rw-r--r--   0        0        0      779 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/CSG.scad
+-rw-r--r--   0        0        0     1194 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/LetterBlock.scad
+-rw-r--r--   0        0        0     1546 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/children.scad
+-rw-r--r--   0        0        0     1788 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/children_indexed.scad
+-rw-r--r--   0        0        0      705 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/difference_cube.scad
+-rw-r--r--   0        0        0     1007 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/difference_sphere.scad
+-rw-r--r--   0        0        0     1031 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/intersection.scad
+-rw-r--r--   0        0        0     1279 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/linear_extrude.scad
+-rw-r--r--   0        0        0     1250 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/logo.scad
+-rw-r--r--   0        0        0     1403 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/logo_and_text.scad
+-rw-r--r--   0        0        0     2017 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/projection.scad
+-rw-r--r--   0        0        0     1237 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/rotate_extrude.scad
+-rw-r--r--   0        0        0      878 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/surface.scad
+-rw-r--r--   0        0        0      949 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/surface_image.scad
+-rw-r--r--   0        0        0     1591 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/text_on_cube.scad
+-rw-r--r--   0        0        0     1048 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/translate.scad
+-rw-r--r--   0        0        0      943 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Basics/union.scad
+-rw-r--r--   0        0        0     1729 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Extrusion/cut_view.scad
+-rw-r--r--   0        0        0     1624 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Extrusion/fan_view.scad
+-rw-r--r--   0        0        0     1260 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Extrusion/text.scad
+-rw-r--r--   0        0        0     1218 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Functions/functions.scad
+-rw-r--r--   0        0        0     1799 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Functions/recursion.scad
+-rw-r--r--   0        0        0     1107 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Shapes/chopped_blocks.scad
+-rw-r--r--   0        0        0      782 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Shapes/fence.scad
+-rw-r--r--   0        0        0      992 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Shapes/flat_body.scad
+-rw-r--r--   0        0        0      707 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Shapes/polyhedron.scad
+-rw-r--r--   0        0        0     1692 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Shapes/rounded_box.scad
+-rw-r--r--   0        0        0      693 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Shapes/sphere.scad
+-rw-r--r--   0        0        0     4444 2020-02-02 00:00:00.000000 nicescad-0.0.3/scad_examples/openscad_examples/Shapes/tripod.scad
+-rwxr-xr-x   0        0        0     2023 2020-02-02 00:00:00.000000 nicescad-0.0.3/scripts/doc
+-rwxr-xr-x   0        0        0       78 2020-02-02 00:00:00.000000 nicescad-0.0.3/scripts/install
+-rw-r--r--   0        0        0     7380 2020-02-02 00:00:00.000000 nicescad-0.0.3/scripts/openscad_example_scraper.py
+-rwxr-xr-x   0        0        0      135 2020-02-02 00:00:00.000000 nicescad-0.0.3/scripts/test
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 nicescad-0.0.3/tests/__init__.py
+-rw-r--r--   0        0        0     1022 2020-02-02 00:00:00.000000 nicescad-0.0.3/tests/basetest.py
+-rw-r--r--   0        0        0     1543 2020-02-02 00:00:00.000000 nicescad-0.0.3/tests/test_openscad.py
+-rw-r--r--   0        0        0      649 2020-02-02 00:00:00.000000 nicescad-0.0.3/tests/test_webserver.py
+-rw-r--r--   0        0        0     3094 2020-02-02 00:00:00.000000 nicescad-0.0.3/.gitignore
+-rw-r--r--   0        0        0    11357 2020-02-02 00:00:00.000000 nicescad-0.0.3/LICENSE
+-rw-r--r--   0        0        0     1508 2020-02-02 00:00:00.000000 nicescad-0.0.3/README.md
+-rw-r--r--   0        0        0     1787 2020-02-02 00:00:00.000000 nicescad-0.0.3/pyproject.toml
+-rw-r--r--   0        0        0     2854 2020-02-02 00:00:00.000000 nicescad-0.0.3/PKG-INFO
```

### Comparing `nicescad-0.0.2/.github/workflows/build.yml` & `nicescad-0.0.3/.github/workflows/build.yml`

 * *Files identical despite different names*

### Comparing `nicescad-0.0.2/.github/workflows/upload-to-pypi.yml` & `nicescad-0.0.3/.github/workflows/upload-to-pypi.yml`

 * *Files identical despite different names*

### Comparing `nicescad-0.0.2/examples/openjscad_logo.stl` & `nicescad-0.0.3/scad_examples/openjscad_logo.stl`

 * *Files identical despite different names*

### Comparing `nicescad-0.0.2/nicescad/local_filepicker.py` & `nicescad-0.0.3/nicescad/local_filepicker.py`

 * *Files identical despite different names*

### Comparing `nicescad-0.0.2/nicescad/nicescad_cmd.py` & `nicescad-0.0.3/nicescad/nicescad_cmd.py`

 * *Files 6% similar despite different names*

```diff
@@ -22,15 +22,17 @@
     Returns:
         ArgumentParser: the argument parser
     """
     parser = ArgumentParser(description=description, formatter_class=RawDescriptionHelpFormatter)
     parser.add_argument("-a","--about",help="show about info [default: %(default)s]",action="store_true")
     parser.add_argument("-c","--client", action="store_true", help="start client [default: %(default)s]")
     parser.add_argument("-d", "--debug", dest="debug", action="store_true", help="show debug info [default: %(default)s]")
+    parser.add_argument("-l", "--local", dest="local", action="store_true", help="run with local file system access [default: %(default)s]")
     parser.add_argument("-i", "--input", help="input file")
+    parser.add_argument("-rp", "--root_path",default=WebServer.examples_path(),help="path to scad files [default: %(default)s]")
 
     parser.add_argument("--host", default="localhost",
                             help="the host to serve / listen from [default: %(default)s]")
     parser.add_argument("--port",type=int,default=9858,help="the port to serve from [default: %(default)s]")
     parser.add_argument("-s","--serve", action="store_true", help="start webserver [default: %(default)s]")
     parser.add_argument("-V", "--version", action='version', version=version_msg)
     return parser
```

### Comparing `nicescad-0.0.2/nicescad/profiler.py` & `nicescad-0.0.3/nicescad/profiler.py`

 * *Files identical despite different names*

### Comparing `nicescad-0.0.2/nicescad/version.py` & `nicescad-0.0.3/nicescad/version.py`

 * *Files 4% similar despite different names*

```diff
@@ -12,15 +12,15 @@
     version = nicescad.__version__
     date = '2023-07-19'
     updated = '2023-07-21'
     description = 'Nice Scad',
     
     authors = 'Wolfgang Fahl'
     
-    doc_url="https://github.com/WolfgangFahl/nicescad"
+    doc_url="https://wiki.bitplan.com/index.php/nicescad"
     chat_url="https://github.com/WolfgangFahl/nicescad/discussions"
     cm_url="https://github.com/WolfgangFahl/nicescad"
 
     license = f'''Copyright 2023 contributors. All rights reserved.
 
   Licensed under the Apache License 2.0
   http://www.apache.org/licenses/LICENSE-2.0
```

### Comparing `nicescad-0.0.2/scripts/doc` & `nicescad-0.0.3/scripts/doc`

 * *Files identical despite different names*

### Comparing `nicescad-0.0.2/tests/basetest.py` & `nicescad-0.0.3/tests/basetest.py`

 * *Files identical despite different names*

### Comparing `nicescad-0.0.2/.gitignore` & `nicescad-0.0.3/.gitignore`

 * *Files 4% similar despite different names*

```diff
@@ -154,7 +154,9 @@
 
 # PyCharm
 #  JetBrains specific template is maintained in a separate JetBrains.gitignore that can
 #  be found at https://github.com/github/gitignore/blob/main/Global/JetBrains.gitignore
 #  and can be added to the global gitignore or merged into this file.  For a more nuclear
 #  option (not recommended) you can uncomment the following to ignore the entire idea folder.
 #.idea/
+# Mac
+.DS_Store
```

### Comparing `nicescad-0.0.2/LICENSE` & `nicescad-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `nicescad-0.0.2/pyproject.toml` & `nicescad-0.0.3/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -13,14 +13,19 @@
 readme = "README.md"
 license= "Apache-2.0"
 dependencies = [
 	# https://github.com/jeff-dh/SolidPython
 	'solidpython2>=2.0.2',
 	# https://pypi.org/project/pywin32/
 	'pywin32; platform_system=="Windows"',
+	# https://pypi.org/project/requests/
+	"requests",
+	# https://pypi.org/project/Pygments/
+	"pygments",
+	# nicegui
     'nicegui>=1.3.5',
 ]
 
 requires-python = ">=3.8"
 classifiers=[
     "Development Status :: 4 - Beta",
     "Environment :: Web Environment",
@@ -47,12 +52,15 @@
 
 [project.optional-dependencies]
 test = [
   "green",
 ]
 
 [tool.hatch.build.targets.wheel]
-packages = [
-  "nicescad",
-]
+only-include = ["nicescad","scad_examples"]
+
+[tool.hatch.build.targets.wheel.sources]
+"nicescad" = "nicescad"
+"scad_examples" = "scad_examples"
+
 [project.scripts]
 nicescad = "nicescad.nicescad_cmd:main"
```

### Comparing `nicescad-0.0.2/PKG-INFO` & `nicescad-0.0.3/PKG-INFO`

 * *Files 24% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nicescad
-Version: 0.0.2
+Version: 0.0.3
 Project-URL: Home, https://github.com/WolfgangFahl/nicescad
 Project-URL: Documentation, https://wiki.bitplan.com/index.php/nicescad
 Project-URL: Source, https://github.com/WolfgangFahl/nicescad
 Author-email: Wolfgang Fahl <wf@bitplan.com>
 Maintainer-email: Wolfgang Fahl <wf@bitplan.com>
 License-Expression: Apache-2.0
 License-File: LICENSE
@@ -19,30 +19,40 @@
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Python: >=3.8
 Requires-Dist: nicegui>=1.3.5
+Requires-Dist: pygments
 Requires-Dist: pywin32; platform_system == 'Windows'
+Requires-Dist: requests
 Requires-Dist: solidpython2>=2.0.2
 Provides-Extra: test
 Requires-Dist: green; extra == 'test'
 Description-Content-Type: text/markdown
 
 # nicescad
-
+nicescad brings OpenScad to the browser (again)
 
 [![Join the discussion at https://github.com/WolfgangFahl/nicescad/discussions](https://img.shields.io/github/discussions/WolfgangFahl/nicescad)](https://github.com/WolfgangFahl/nicescad/discussions) 
 [![pypi](https://img.shields.io/pypi/pyversions/nicescad)](https://pypi.org/project/nicescad/)
 [![Github Actions Build](https://github.com/WolfgangFahl/nicescad/workflows/Build/badge.svg?branch=main)](https://github.com/WolfgangFahl/nicescad/actions?query=workflow%3ABuild+branch%3Amain)
 [![PyPI Status](https://img.shields.io/pypi/v/nicescad.svg)](https://pypi.python.org/pypi/nicescad/)
 [![GitHub issues](https://img.shields.io/github/issues/WolfgangFahl/nicescad.svg)](https://github.com/WolfgangFahl/nicescad/issues)
 [![GitHub closed issues](https://img.shields.io/github/issues-closed/WolfgangFahl/nicescad.svg)](https://github.com/WolfgangFahl/nicescad/issues/?q=is%3Aissue+is%3Aclosed)
 [![License](https://img.shields.io/github/license/WolfgangFahl/nicescad.svg)](https://www.apache.org/licenses/LICENSE-2.0)
 
+## Demo 
+[Demo](http://nicescad.bitplan.com/)
+
 ## Docs and Tutorials
 [Wiki](https://wiki.bitplan.com/index.php/nicescad)
 
+## Examples
+* [Basics/logo](https://raw.githubusercontent.com/openscad/openscad/master/examples/Basics/logo.scad)
+* [Intersection](https://raw.githubusercontent.com/WolfgangFahl/nicescad/main/examples/intersection.scad)
+
 ## Links
 * https://openscad.org/
 * https://nicegui.io
+* https://ochafik.com/openscad2/
```

