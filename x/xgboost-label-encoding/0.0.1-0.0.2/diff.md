# Comparing `tmp/xgboost_label_encoding-0.0.1.tar.gz` & `tmp/xgboost_label_encoding-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "xgboost_label_encoding-0.0.1.tar", last modified: Wed Apr 12 03:06:23 2023, max compression
+gzip compressed data, was "xgboost_label_encoding-0.0.2.tar", last modified: Sun Jul 23 00:19:35 2023, max compression
```

## Comparing `xgboost_label_encoding-0.0.1.tar` & `xgboost_label_encoding-0.0.2.tar`

### file list

```diff
@@ -1,30 +1,30 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-12 03:06:23.829406 xgboost_label_encoding-0.0.1/
--rw-r--r--   0 runner    (1001) docker     (123)       48 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/CHANGELOG.md
--rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     2369 2023-04-12 03:06:23.829406 xgboost_label_encoding-0.0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1668 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-12 03:06:23.825405 xgboost_label_encoding-0.0.1/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      623 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/docs/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)       48 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/docs/changelog.md
--rwxr-xr-x   0 runner    (1001) docker     (123)     7300 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      213 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/docs/contents.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1668 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/docs/index.md
--rw-r--r--   0 runner    (1001) docker     (123)      784 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)       90 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/docs/modules.rst
--rw-r--r--   0 runner    (1001) docker     (123)      202 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/docs/xgboost_label_encoding.rst
--rw-r--r--   0 runner    (1001) docker     (123)      207 2023-04-12 03:06:23.829406 xgboost_label_encoding-0.0.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1436 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-12 03:06:23.829406 xgboost_label_encoding-0.0.1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      954 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/tests/test_package.py
--rw-r--r--   0 runner    (1001) docker     (123)     3192 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/tests/test_xgboost_with_label_encoding.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-12 03:06:23.829406 xgboost_label_encoding-0.0.1/xgboost_label_encoding/
--rw-r--r--   0 runner    (1001) docker     (123)     2926 2023-04-12 03:05:30.000000 xgboost_label_encoding-0.0.1/xgboost_label_encoding/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-12 03:06:23.829406 xgboost_label_encoding-0.0.1/xgboost_label_encoding.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2369 2023-04-12 03:06:23.000000 xgboost_label_encoding-0.0.1/xgboost_label_encoding.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      592 2023-04-12 03:06:23.000000 xgboost_label_encoding-0.0.1/xgboost_label_encoding.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-12 03:06:23.000000 xgboost_label_encoding-0.0.1/xgboost_label_encoding.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-12 03:06:23.000000 xgboost_label_encoding-0.0.1/xgboost_label_encoding.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       45 2023-04-12 03:06:23.000000 xgboost_label_encoding-0.0.1/xgboost_label_encoding.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-04-12 03:06:23.000000 xgboost_label_encoding-0.0.1/xgboost_label_encoding.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 00:19:35.641719 xgboost_label_encoding-0.0.2/
+-rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/CHANGELOG.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     2369 2023-07-23 00:19:35.641719 xgboost_label_encoding-0.0.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1668 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 00:19:35.641719 xgboost_label_encoding-0.0.2/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      623 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/docs/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/docs/changelog.md
+-rwxr-xr-x   0 runner    (1001) docker     (123)     7300 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      213 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/docs/contents.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1668 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/docs/index.md
+-rw-r--r--   0 runner    (1001) docker     (123)      784 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)       90 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/docs/modules.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      202 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/docs/xgboost_label_encoding.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      207 2023-07-23 00:19:35.645719 xgboost_label_encoding-0.0.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1436 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 00:19:35.641719 xgboost_label_encoding-0.0.2/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      954 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/tests/test_package.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3192 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/tests/test_xgboost_with_label_encoding.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 00:19:35.641719 xgboost_label_encoding-0.0.2/xgboost_label_encoding/
+-rw-r--r--   0 runner    (1001) docker     (123)     3161 2023-07-23 00:18:47.000000 xgboost_label_encoding-0.0.2/xgboost_label_encoding/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 00:19:35.641719 xgboost_label_encoding-0.0.2/xgboost_label_encoding.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2369 2023-07-23 00:19:35.000000 xgboost_label_encoding-0.0.2/xgboost_label_encoding.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      592 2023-07-23 00:19:35.000000 xgboost_label_encoding-0.0.2/xgboost_label_encoding.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 00:19:35.000000 xgboost_label_encoding-0.0.2/xgboost_label_encoding.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 00:19:35.000000 xgboost_label_encoding-0.0.2/xgboost_label_encoding.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       45 2023-07-23 00:19:35.000000 xgboost_label_encoding-0.0.2/xgboost_label_encoding.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-07-23 00:19:35.000000 xgboost_label_encoding-0.0.2/xgboost_label_encoding.egg-info/top_level.txt
```

### Comparing `xgboost_label_encoding-0.0.1/LICENSE` & `xgboost_label_encoding-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `xgboost_label_encoding-0.0.1/PKG-INFO` & `xgboost_label_encoding-0.0.2/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xgboost_label_encoding
-Version: 0.0.1
+Version: 0.0.2
 Summary: Xgboost Label Encoding
 Home-page: https://github.com/maximz/xgboost-label-encoding
 Author: Maxim Zaslavsky
 Author-email: maxim@maximz.com
 License: MIT license
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `xgboost_label_encoding-0.0.1/README.md` & `xgboost_label_encoding-0.0.2/README.md`

 * *Files identical despite different names*

### Comparing `xgboost_label_encoding-0.0.1/docs/Makefile` & `xgboost_label_encoding-0.0.2/docs/Makefile`

 * *Files identical despite different names*

### Comparing `xgboost_label_encoding-0.0.1/docs/conf.py` & `xgboost_label_encoding-0.0.2/docs/conf.py`

 * *Files identical despite different names*

### Comparing `xgboost_label_encoding-0.0.1/docs/index.md` & `xgboost_label_encoding-0.0.2/docs/index.md`

 * *Files identical despite different names*

### Comparing `xgboost_label_encoding-0.0.1/docs/make.bat` & `xgboost_label_encoding-0.0.2/docs/make.bat`

 * *Files identical despite different names*

### Comparing `xgboost_label_encoding-0.0.1/setup.py` & `xgboost_label_encoding-0.0.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -25,15 +25,15 @@
     author_email="maxim@maximz.com",
     name="xgboost_label_encoding",
     description="Xgboost Label Encoding",
     packages=find_packages(
         include=["xgboost_label_encoding", "xgboost_label_encoding.*"]
     ),
     python_requires=">=3.8",
-    version="0.0.1",
+    version="0.0.2",
     classifiers=[
         "Development Status :: 2 - Pre-Alpha",
         "Intended Audience :: Developers",
         "License :: OSI Approved :: MIT License",
         "Natural Language :: English",
         "Programming Language :: Python :: 3",
         "Programming Language :: Python :: 3.8",
```

### Comparing `xgboost_label_encoding-0.0.1/tests/test_package.py` & `xgboost_label_encoding-0.0.2/tests/test_package.py`

 * *Files identical despite different names*

### Comparing `xgboost_label_encoding-0.0.1/tests/test_xgboost_with_label_encoding.py` & `xgboost_label_encoding-0.0.2/tests/test_xgboost_with_label_encoding.py`

 * *Files identical despite different names*

### Comparing `xgboost_label_encoding-0.0.1/xgboost_label_encoding/__init__.py` & `xgboost_label_encoding-0.0.2/xgboost_label_encoding/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 """Xgboost Label Encoding."""
 
 __author__ = """Maxim Zaslavsky"""
 __email__ = "maxim@maximz.com"
-__version__ = "0.0.1"
+__version__ = "0.0.2"
 
 # Set default logging handler to avoid "No handler found" warnings.
 import logging
 from logging import NullHandler
 
 logging.getLogger(__name__).addHandler(NullHandler())
 
@@ -39,15 +39,15 @@
         self.class_weight = class_weight
 
     def fit(
         self,
         X: np.ndarray,
         y: np.ndarray,
         sample_weight: Optional[np.ndarray] = None,
-        **kwargs
+        **kwargs,
     ) -> Self:
         if self.class_weight is not None:
             # Use sklearn to compute class weights, then map to individual sample weights
             sample_weight_computed = sklearn.utils.class_weight.compute_sample_weight(
                 class_weight=self.class_weight, y=y
             )
             if sample_weight is None:
@@ -63,14 +63,19 @@
                 # Then, multiply the two
                 sample_weight = sample_weight * sample_weight_computed
 
         # Encode y labels
         self.label_encoder_ = LabelEncoder()
         transformed_y = self.label_encoder_.fit_transform(y)
 
+        if len(self.label_encoder_.classes_) < 2:
+            raise ValueError(
+                f"Training data needs to have at least 2 classes, but the data contains only one class: {self.label_encoder_.classes_[0]}"
+            )
+
         # fit as usual
         super().fit(X, transformed_y, sample_weight=sample_weight, **kwargs)
 
         # set classes_
         self.classes_: np.ndarray = self.label_encoder_.classes_
         return self
```

### Comparing `xgboost_label_encoding-0.0.1/xgboost_label_encoding.egg-info/PKG-INFO` & `xgboost_label_encoding-0.0.2/xgboost_label_encoding.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xgboost-label-encoding
-Version: 0.0.1
+Version: 0.0.2
 Summary: Xgboost Label Encoding
 Home-page: https://github.com/maximz/xgboost-label-encoding
 Author: Maxim Zaslavsky
 Author-email: maxim@maximz.com
 License: MIT license
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `xgboost_label_encoding-0.0.1/xgboost_label_encoding.egg-info/SOURCES.txt` & `xgboost_label_encoding-0.0.2/xgboost_label_encoding.egg-info/SOURCES.txt`

 * *Files identical despite different names*

