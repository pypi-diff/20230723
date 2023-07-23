# Comparing `tmp/pyqtclass-0.1.0.tar.gz` & `tmp/pyqtclass-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyqtclass-0.1.0.tar", last modified: Sun Mar 26 08:37:23 2023, max compression
+gzip compressed data, was "pyqtclass-0.2.0.tar", last modified: Sun Jul 23 04:56:30 2023, max compression
```

## Comparing `pyqtclass-0.1.0.tar` & `pyqtclass-0.2.0.tar`

### file list

```diff
@@ -1,13 +1,18 @@
-drwxrwxrwx   0        0        0        0 2023-03-26 08:37:23.544027 pyqtclass-0.1.0/
--rw-rw-rw-   0        0        0     1086 2023-03-24 01:33:53.000000 pyqtclass-0.1.0/LICENSE
--rw-rw-rw-   0        0        0      586 2023-03-26 08:37:23.543027 pyqtclass-0.1.0/PKG-INFO
--rw-rw-rw-   0        0        0       96 2023-03-24 01:33:53.000000 pyqtclass-0.1.0/README.md
--rw-rw-rw-   0        0        0       42 2023-03-26 08:37:23.544027 pyqtclass-0.1.0/setup.cfg
--rw-rw-rw-   0        0        0      839 2023-03-26 08:36:31.000000 pyqtclass-0.1.0/setup.py
-drwxrwxrwx   0        0        0        0 2023-03-26 08:37:23.520021 pyqtclass-0.1.0/src/
-drwxrwxrwx   0        0        0        0 2023-03-26 08:37:23.541026 pyqtclass-0.1.0/src/pyqtclass.egg-info/
--rw-rw-rw-   0        0        0      586 2023-03-26 08:37:23.000000 pyqtclass-0.1.0/src/pyqtclass.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      210 2023-03-26 08:37:23.000000 pyqtclass-0.1.0/src/pyqtclass.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-03-26 08:37:23.000000 pyqtclass-0.1.0/src/pyqtclass.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       19 2023-03-26 08:37:23.000000 pyqtclass-0.1.0/src/pyqtclass.egg-info/requires.txt
--rw-rw-rw-   0        0        0        1 2023-03-26 08:37:23.000000 pyqtclass-0.1.0/src/pyqtclass.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 04:56:30.987832 pyqtclass-0.2.0/
+-rw-rw-rw-   0        0        0     1086 2023-03-24 01:33:53.000000 pyqtclass-0.2.0/LICENSE
+-rw-rw-rw-   0        0        0      586 2023-07-23 04:56:30.986834 pyqtclass-0.2.0/PKG-INFO
+-rw-rw-rw-   0        0        0       96 2023-07-23 04:52:26.000000 pyqtclass-0.2.0/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 04:56:30.987832 pyqtclass-0.2.0/setup.cfg
+-rw-rw-rw-   0        0        0      844 2023-07-23 04:49:09.000000 pyqtclass-0.2.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:56:30.942552 pyqtclass-0.2.0/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 04:56:30.957827 pyqtclass-0.2.0/src/pyqtclass/
+-rw-rw-rw-   0        0        0     6146 2023-03-26 08:08:02.000000 pyqtclass-0.2.0/src/pyqtclass/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:56:30.980831 pyqtclass-0.2.0/src/pyqtclass.egg-info/
+-rw-rw-rw-   0        0        0      586 2023-07-23 04:56:30.000000 pyqtclass-0.2.0/src/pyqtclass.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      275 2023-07-23 04:56:30.000000 pyqtclass-0.2.0/src/pyqtclass.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 04:56:30.000000 pyqtclass-0.2.0/src/pyqtclass.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       19 2023-07-23 04:56:30.000000 pyqtclass-0.2.0/src/pyqtclass.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       15 2023-07-23 04:56:30.000000 pyqtclass-0.2.0/src/pyqtclass.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 04:56:30.984832 pyqtclass-0.2.0/src/test/
+-rw-rw-rw-   0        0        0        0 2023-03-26 08:20:21.000000 pyqtclass-0.2.0/src/test/__init__.py
+-rw-rw-rw-   0        0        0      791 2023-03-24 04:26:33.000000 pyqtclass-0.2.0/src/test/utest.py
```

### Comparing `pyqtclass-0.1.0/LICENSE` & `pyqtclass-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pyqtclass-0.1.0/PKG-INFO` & `pyqtclass-0.2.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyqtclass
-Version: 0.1.0
+Version: 0.2.0
 Summary: PyQt 기반으로 동작하는 객체들의 베이스클래스 모음 패키지
 Home-page: https://github.com/innovata/PyQtClasses
 Author: innovata
 Author-email: iinnovata@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `pyqtclass-0.1.0/setup.py` & `pyqtclass-0.2.0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,24 +2,24 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="pyqtclass",
-    version="0.1.0",
+    version="0.2.0",
     author="innovata",
     author_email="iinnovata@gmail.com",
     description='PyQt 기반으로 동작하는 객체들의 베이스클래스 모음 패키지',
     long_description=long_description,
     long_description_content_type="text/markdown",
     url=f"https://github.com/innovata/PyQtClasses",
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
     ],
     package_dir={"":"src"},
-    packages=setuptools.find_packages(),
+    packages=setuptools.find_packages('src'),
     python_requires=">=3.8",
     install_requires=['ipylib', 'PyQt5', 'trddt'],
 )
```

### Comparing `pyqtclass-0.1.0/src/pyqtclass.egg-info/PKG-INFO` & `pyqtclass-0.2.0/src/pyqtclass.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyqtclass
-Version: 0.1.0
+Version: 0.2.0
 Summary: PyQt 기반으로 동작하는 객체들의 베이스클래스 모음 패키지
 Home-page: https://github.com/innovata/PyQtClasses
 Author: innovata
 Author-email: iinnovata@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

