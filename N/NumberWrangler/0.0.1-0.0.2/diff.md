# Comparing `tmp/NumberWrangler-0.0.1.tar.gz` & `tmp/NumberWrangler-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "NumberWrangler-0.0.1.tar", last modified: Sat Dec 24 06:08:07 2022, max compression
+gzip compressed data, was "NumberWrangler-0.0.2.tar", last modified: Sun Jul 23 17:08:53 2023, max compression
```

## Comparing `NumberWrangler-0.0.1.tar` & `NumberWrangler-0.0.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 abhayshukla   (501) staff       (20)        0 2022-12-24 06:08:07.515207 NumberWrangler-0.0.1/
--rw-r--r--   0 abhayshukla   (501) staff       (20)        0 2022-12-23 22:08:10.000000 NumberWrangler-0.0.1/MANIFEST.in
-drwxr-xr-x   0 abhayshukla   (501) staff       (20)        0 2022-12-24 06:08:07.514395 NumberWrangler-0.0.1/NumberWrangler/
--rw-r--r--   0 abhayshukla   (501) staff       (20)     2485 2022-12-24 05:33:17.000000 NumberWrangler-0.0.1/NumberWrangler/Wrangler.py
--rw-r--r--   0 abhayshukla   (501) staff       (20)        0 2022-12-23 22:11:05.000000 NumberWrangler-0.0.1/NumberWrangler/__init__.py
-drwxr-xr-x   0 abhayshukla   (501) staff       (20)        0 2022-12-24 06:08:07.515070 NumberWrangler-0.0.1/NumberWrangler.egg-info/
--rw-r--r--   0 abhayshukla   (501) staff       (20)     1371 2022-12-24 06:08:07.000000 NumberWrangler-0.0.1/NumberWrangler.egg-info/PKG-INFO
--rw-r--r--   0 abhayshukla   (501) staff       (20)      252 2022-12-24 06:08:07.000000 NumberWrangler-0.0.1/NumberWrangler.egg-info/SOURCES.txt
--rw-r--r--   0 abhayshukla   (501) staff       (20)        1 2022-12-24 06:08:07.000000 NumberWrangler-0.0.1/NumberWrangler.egg-info/dependency_links.txt
--rw-r--r--   0 abhayshukla   (501) staff       (20)       15 2022-12-24 06:08:07.000000 NumberWrangler-0.0.1/NumberWrangler.egg-info/top_level.txt
--rw-r--r--   0 abhayshukla   (501) staff       (20)     1371 2022-12-24 06:08:07.515283 NumberWrangler-0.0.1/PKG-INFO
--rw-r--r--   0 abhayshukla   (501) staff       (20)      899 2022-12-24 05:53:22.000000 NumberWrangler-0.0.1/README.md
--rw-r--r--   0 abhayshukla   (501) staff       (20)      103 2022-12-24 05:54:12.000000 NumberWrangler-0.0.1/pyproject.toml
--rw-r--r--   0 abhayshukla   (501) staff       (20)      554 2022-12-24 06:08:07.515637 NumberWrangler-0.0.1/setup.cfg
+drwxr-xr-x   0 abhayshukla   (501) staff       (20)        0 2023-07-23 17:08:53.026409 NumberWrangler-0.0.2/
+-rw-r--r--   0 abhayshukla   (501) staff       (20)        0 2022-12-23 22:08:10.000000 NumberWrangler-0.0.2/MANIFEST.in
+drwxr-xr-x   0 abhayshukla   (501) staff       (20)        0 2023-07-23 17:08:53.025449 NumberWrangler-0.0.2/NumberWrangler/
+-rw-r--r--   0 abhayshukla   (501) staff       (20)     3182 2023-07-23 17:01:31.000000 NumberWrangler-0.0.2/NumberWrangler/Wrangler.py
+-rw-r--r--   0 abhayshukla   (501) staff       (20)        0 2022-12-23 22:11:05.000000 NumberWrangler-0.0.2/NumberWrangler/__init__.py
+drwxr-xr-x   0 abhayshukla   (501) staff       (20)        0 2023-07-23 17:08:53.026221 NumberWrangler-0.0.2/NumberWrangler.egg-info/
+-rw-r--r--   0 abhayshukla   (501) staff       (20)     1371 2023-07-23 17:08:53.000000 NumberWrangler-0.0.2/NumberWrangler.egg-info/PKG-INFO
+-rw-r--r--   0 abhayshukla   (501) staff       (20)      252 2023-07-23 17:08:53.000000 NumberWrangler-0.0.2/NumberWrangler.egg-info/SOURCES.txt
+-rw-r--r--   0 abhayshukla   (501) staff       (20)        1 2023-07-23 17:08:53.000000 NumberWrangler-0.0.2/NumberWrangler.egg-info/dependency_links.txt
+-rw-r--r--   0 abhayshukla   (501) staff       (20)       15 2023-07-23 17:08:53.000000 NumberWrangler-0.0.2/NumberWrangler.egg-info/top_level.txt
+-rw-r--r--   0 abhayshukla   (501) staff       (20)     1371 2023-07-23 17:08:53.026518 NumberWrangler-0.0.2/PKG-INFO
+-rw-r--r--   0 abhayshukla   (501) staff       (20)      899 2022-12-24 05:53:22.000000 NumberWrangler-0.0.2/README.md
+-rw-r--r--   0 abhayshukla   (501) staff       (20)      103 2022-12-24 05:54:12.000000 NumberWrangler-0.0.2/pyproject.toml
+-rw-r--r--   0 abhayshukla   (501) staff       (20)      554 2023-07-23 17:08:53.026914 NumberWrangler-0.0.2/setup.cfg
```

### Comparing `NumberWrangler-0.0.1/NumberWrangler/Wrangler.py` & `NumberWrangler-0.0.2/NumberWrangler/Wrangler.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,48 +1,88 @@
 from random import SystemRandom, choice
 
 # Wrangler function
-def Variate(number, multiplier=1, add=False, subtr=False, Round=0): ##maybe specify add or remove wrangle or have 2 funct
-    # Verifying inputs
-    if isinstance(number, (int, float)) and isinstance(multiplier, (int, float)) and isinstance(Round, int) and isinstance(add, bool) and isinstance(subtr, bool):
-
-        # Math 🤓
-        def addWrangle(number, multiplier, Round):
-            if Round == 0:
-                return(int(round((number + round((SystemRandom().uniform(0, 10)), Round) * multiplier), Round)))
+def Variate(number, multiplier=1, add=False, subtr=False, round=0):
+
+    if (
+        isinstance(number, (int, float))
+        and isinstance(multiplier, (int, float))
+        and isinstance(round, int)
+        and isinstance(add, bool)
+        and isinstance(subtr, bool)
+    ):
+
+        def addWrangle(number, multiplier, round):
+            if round == 0:
+                return int(
+                    round(
+                        (
+                            number
+                            + round((SystemRandom().uniform(0, 10)), round) * multiplier
+                        ),
+                        round,
+                    )
+                )
             else:
-                return(round((number + round((SystemRandom().uniform(0, 10)), Round) * multiplier), Round))
-   
-        def subtrWrangle(number, multiplier, Round):
-            if Round == 0:
-                return(int(round((number - round((SystemRandom().uniform(0, 10)), Round) * multiplier), Round)))
+                return round(
+                    (
+                        number
+                        + round((SystemRandom().uniform(0, 10)), round) * multiplier
+                    ),
+                    round,
+                )
+
+        def subtrWrangle(number, multiplier, round):
+            if round == 0:
+                return int(
+                    round(
+                        (
+                            number
+                            - round((SystemRandom().uniform(0, 10)), round) * multiplier
+                        ),
+                        round,
+                    )
+                )
             else:
-                return(round((number - round((SystemRandom().uniform(0, 10)), Round) * multiplier), Round))
-
+                return round(
+                    (
+                        number
+                        - round((SystemRandom().uniform(0, 10)), round) * multiplier
+                    ),
+                    round,
+                )
 
-        # add vs subtract
         if add == True and subtr == True:
             raise TypeError("Wrangler can not add and subtract together")
         elif add == False and subtr == False:
-            if choice([0,1]) == 0:
-                return(addWrangle(number, multiplier, Round))
+            if choice([0, 1]) == 0:
+                return addWrangle(number, multiplier, round)
             else:
-                return(subtrWrangle(number, multiplier, Round))
+                return subtrWrangle(number, multiplier, round)
 
-        elif add == True and subtr == False: 
-            return(addWrangle(number, multiplier, Round))
+        elif add == True and subtr == False:
+            return addWrangle(number, multiplier, round)
         elif add == False and subtr == True:
-            return(subtrWrangle(number, multiplier, Round))
-       
+            return subtrWrangle(number, multiplier, round)
 
     # Verification fail
     else:
         if isinstance(number, (int, float)) == False:
-            raise TypeError(f"Number input '{number}' is not valid; must be a float or int (currently {type(number)}")
+            raise TypeError(
+                f"Number input '{number}' is not valid; must be a float or int (currently {type(number)}"
+            )
         elif isinstance(multiplier, (int, float)) == False:
-            raise TypeError(f"Multiplier input '{multiplier}' is not valid; must be a float or int (currently {type(multiplier)})")
-        elif isinstance(Round, int) == False:
-            raise TypeError(f"Rounding input '{Round}' is not valid; must be a int (currently {type(Round)})")
+            raise TypeError(
+                f"Multiplier input '{multiplier}' is not valid; must be a float or int (currently {type(multiplier)})"
+            )
+        elif isinstance(round, int) == False:
+            raise TypeError(
+                f"rounding input '{round}' is not valid; must be a int (currently {type(round)})"
+            )
         elif isinstance(add, bool) == False:
-            raise TypeError(f"Function input '{add}' is not valid; must be a bool (currently {type(add)})")
+            raise TypeError(
+                f"Function input '{add}' is not valid; must be a bool (currently {type(add)})"
+            )
         elif isinstance(subtr, bool) == False:
-            raise TypeError(f"Function input '{subtr}' is not valid; must be a bool (currently {type(subtr)})")
+            raise TypeError(
+                f"Function input '{subtr}' is not valid; must be a bool (currently {type(subtr)})"
+            )
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `NumberWrangler-0.0.1/NumberWrangler.egg-info/PKG-INFO` & `NumberWrangler-0.0.2/NumberWrangler.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: NumberWrangler
-Version: 0.0.1
+Version: 0.0.2
 Summary: Python package for slightly or massively variating numbers.
 Home-page: https://github.com/aboombadev/NumberWrangler
 Author: Abhay Shukla
 Author-email: notsure@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Classifier: Operating System :: OS Independent
```

### Comparing `NumberWrangler-0.0.1/PKG-INFO` & `NumberWrangler-0.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: NumberWrangler
-Version: 0.0.1
+Version: 0.0.2
 Summary: Python package for slightly or massively variating numbers.
 Home-page: https://github.com/aboombadev/NumberWrangler
 Author: Abhay Shukla
 Author-email: notsure@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Classifier: Operating System :: OS Independent
```

### Comparing `NumberWrangler-0.0.1/README.md` & `NumberWrangler-0.0.2/README.md`

 * *Files identical despite different names*

### Comparing `NumberWrangler-0.0.1/setup.cfg` & `NumberWrangler-0.0.2/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = NumberWrangler
-version = 0.0.1
+version = 0.0.2
 author = Abhay Shukla
 author_email = notsure@gmail.com
 description = Python package for slightly or massively variating numbers.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/aboombadev/NumberWrangler
 classifiers =
```

