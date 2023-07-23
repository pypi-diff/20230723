# Comparing `tmp/anchovy-0.7.1.tar.gz` & `tmp/anchovy-0.8.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "anchovy-0.7.1.tar", last modified: Sat Jul 22 03:42:14 2023, max compression
+gzip compressed data, was "anchovy-0.8.0.tar", last modified: Sun Jul 23 07:22:55 2023, max compression
```

## Comparing `anchovy-0.7.1.tar` & `anchovy-0.8.0.tar`

### file list

```diff
@@ -1,56 +1,56 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.118933 anchovy-0.7.1/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.110933 anchovy-0.7.1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.110933 anchovy-0.7.1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      923 2023-07-22 03:42:02.000000 anchovy-0.7.1/.github/workflows/python-cq.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1583 2023-07-22 03:42:02.000000 anchovy-0.7.1/.github/workflows/python-publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)       95 2023-07-22 03:42:02.000000 anchovy-0.7.1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-07-22 03:42:02.000000 anchovy-0.7.1/.tokeignore
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-22 03:42:02.000000 anchovy-0.7.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     6038 2023-07-22 03:42:14.118933 anchovy-0.7.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4903 2023-07-22 03:42:06.000000 anchovy-0.7.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.110933 anchovy-0.7.1/examples/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.114933 anchovy-0.7.1/examples/_images/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/_images/.credits.md
--rw-r--r--   0 runner    (1001) docker     (123)   890709 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/_images/anchovy-nypl.jpg
--rw-r--r--   0 runner    (1001) docker     (123)   706821 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/_images/home-sweet-home-cdk.jpg
--rw-r--r--   0 runner    (1001) docker     (123)   679302 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/_images/nice-wheels-cdk.jpg
--rw-r--r--   0 runner    (1001) docker     (123)   482152 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/_images/quayside-newcastle.jpg
--rw-r--r--   0 runner    (1001) docker     (123)   447542 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/_images/stormy-cdk.jpg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.114933 anchovy-0.7.1/examples/basic_site/
--rw-r--r--   0 runner    (1001) docker     (123)      294 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/basic_site/base.jinja.html
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/basic_site/index.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.114933 anchovy-0.7.1/examples/basic_site/static/
--rw-r--r--   0 runner    (1001) docker     (123)      276 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/basic_site/static/core.css
--rw-r--r--   0 runner    (1001) docker     (123)      977 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/basic_site.py
--rw-r--r--   0 runner    (1001) docker     (123)     1488 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/css_transformer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.114933 anchovy-0.7.1/examples/gallery/
--rw-r--r--   0 runner    (1001) docker     (123)      294 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/gallery/base.jinja.html
--rw-r--r--   0 runner    (1001) docker     (123)      673 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/gallery/index.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.114933 anchovy-0.7.1/examples/gallery/static/
--rw-r--r--   0 runner    (1001) docker     (123)      526 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/gallery/static/core.css
--rw-r--r--   0 runner    (1001) docker     (123)     1528 2023-07-22 03:42:02.000000 anchovy-0.7.1/examples/gallery.py
--rw-r--r--   0 runner    (1001) docker     (123)    11159 2023-07-22 03:42:02.000000 anchovy-0.7.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 03:42:14.118933 anchovy-0.7.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 03:42:02.000000 anchovy-0.7.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.110933 anchovy-0.7.1/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.118933 anchovy-0.7.1/src/anchovy/
--rw-r--r--   0 runner    (1001) docker     (123)      510 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       30 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7601 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     8692 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/core.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.118933 anchovy-0.7.1/src/anchovy/css/
--rw-r--r--   0 runner    (1001) docker     (123)      812 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/css/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9395 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/css/parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     4926 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/dependencies.py
--rw-r--r--   0 runner    (1001) docker     (123)     5169 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/images.py
--rw-r--r--   0 runner    (1001) docker     (123)     5560 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/jinja.py
--rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/paths.py
--rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/pretty_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1863 2023-07-22 03:42:02.000000 anchovy-0.7.1/src/anchovy/simple.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 03:42:14.118933 anchovy-0.7.1/src/anchovy.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6038 2023-07-22 03:42:14.000000 anchovy-0.7.1/src/anchovy.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1170 2023-07-22 03:42:14.000000 anchovy-0.7.1/src/anchovy.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 03:42:14.000000 anchovy-0.7.1/src/anchovy.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       45 2023-07-22 03:42:14.000000 anchovy-0.7.1/src/anchovy.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      337 2023-07-22 03:42:14.000000 anchovy-0.7.1/src/anchovy.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-22 03:42:14.000000 anchovy-0.7.1/src/anchovy.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.199470 anchovy-0.8.0/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.187470 anchovy-0.8.0/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.191470 anchovy-0.8.0/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      923 2023-07-23 07:22:39.000000 anchovy-0.8.0/.github/workflows/python-cq.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1583 2023-07-23 07:22:39.000000 anchovy-0.8.0/.github/workflows/python-publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)       95 2023-07-23 07:22:39.000000 anchovy-0.8.0/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-07-23 07:22:39.000000 anchovy-0.8.0/.tokeignore
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 07:22:39.000000 anchovy-0.8.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     6038 2023-07-23 07:22:55.199470 anchovy-0.8.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4903 2023-07-23 07:22:47.000000 anchovy-0.8.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.191470 anchovy-0.8.0/examples/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.195470 anchovy-0.8.0/examples/_images/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/_images/.credits.md
+-rw-r--r--   0 runner    (1001) docker     (123)   890709 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/_images/anchovy-nypl.jpg
+-rw-r--r--   0 runner    (1001) docker     (123)   706821 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/_images/home-sweet-home-cdk.jpg
+-rw-r--r--   0 runner    (1001) docker     (123)   679302 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/_images/nice-wheels-cdk.jpg
+-rw-r--r--   0 runner    (1001) docker     (123)   482152 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/_images/quayside-newcastle.jpg
+-rw-r--r--   0 runner    (1001) docker     (123)   447542 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/_images/stormy-cdk.jpg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.195470 anchovy-0.8.0/examples/basic_site/
+-rw-r--r--   0 runner    (1001) docker     (123)      294 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/basic_site/base.jinja.html
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/basic_site/index.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.195470 anchovy-0.8.0/examples/basic_site/static/
+-rw-r--r--   0 runner    (1001) docker     (123)      276 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/basic_site/static/core.css
+-rw-r--r--   0 runner    (1001) docker     (123)      977 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/basic_site.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1540 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/css_transformer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.195470 anchovy-0.8.0/examples/gallery/
+-rw-r--r--   0 runner    (1001) docker     (123)      294 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/gallery/base.jinja.html
+-rw-r--r--   0 runner    (1001) docker     (123)      673 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/gallery/index.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.195470 anchovy-0.8.0/examples/gallery/static/
+-rw-r--r--   0 runner    (1001) docker     (123)      526 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/gallery/static/core.css
+-rw-r--r--   0 runner    (1001) docker     (123)     1528 2023-07-23 07:22:39.000000 anchovy-0.8.0/examples/gallery.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11159 2023-07-23 07:22:39.000000 anchovy-0.8.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 07:22:55.199470 anchovy-0.8.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 07:22:39.000000 anchovy-0.8.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.187470 anchovy-0.8.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.195470 anchovy-0.8.0/src/anchovy/
+-rw-r--r--   0 runner    (1001) docker     (123)      510 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7601 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8692 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/core.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.199470 anchovy-0.8.0/src/anchovy/css/
+-rw-r--r--   0 runner    (1001) docker     (123)      812 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/css/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9395 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/css/parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4926 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/dependencies.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5169 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/images.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5500 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/jinja.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4357 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/paths.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/pretty_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1863 2023-07-23 07:22:39.000000 anchovy-0.8.0/src/anchovy/simple.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:22:55.199470 anchovy-0.8.0/src/anchovy.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6038 2023-07-23 07:22:55.000000 anchovy-0.8.0/src/anchovy.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1170 2023-07-23 07:22:55.000000 anchovy-0.8.0/src/anchovy.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 07:22:55.000000 anchovy-0.8.0/src/anchovy.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       45 2023-07-23 07:22:55.000000 anchovy-0.8.0/src/anchovy.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      337 2023-07-23 07:22:55.000000 anchovy-0.8.0/src/anchovy.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 07:22:55.000000 anchovy-0.8.0/src/anchovy.egg-info/top_level.txt
```

### Comparing `anchovy-0.7.1/.github/workflows/python-cq.yml` & `anchovy-0.8.0/.github/workflows/python-cq.yml`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/.github/workflows/python-publish.yml` & `anchovy-0.8.0/.github/workflows/python-publish.yml`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/LICENSE` & `anchovy-0.8.0/LICENSE`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/PKG-INFO` & `anchovy-0.8.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: anchovy
-Version: 0.7.1
+Version: 0.8.0
 Summary: A minimal, unopinionated file processing engine intended for static website generation.
 Author-email: Daniel Foerster <pydsigner@gmail.com>
 License: Apache-2.0
 Keywords: static,website,generation,html,css,template
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `anchovy-0.7.1/README.md` & `anchovy-0.8.0/README.md`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/_images/.credits.md` & `anchovy-0.8.0/examples/_images/.credits.md`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/_images/anchovy-nypl.jpg` & `anchovy-0.8.0/examples/_images/anchovy-nypl.jpg`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/_images/home-sweet-home-cdk.jpg` & `anchovy-0.8.0/examples/_images/home-sweet-home-cdk.jpg`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/_images/nice-wheels-cdk.jpg` & `anchovy-0.8.0/examples/_images/nice-wheels-cdk.jpg`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/_images/quayside-newcastle.jpg` & `anchovy-0.8.0/examples/_images/quayside-newcastle.jpg`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/_images/stormy-cdk.jpg` & `anchovy-0.8.0/examples/_images/stormy-cdk.jpg`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/basic_site.py` & `anchovy-0.8.0/examples/basic_site.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/css_transformer.py` & `anchovy-0.8.0/examples/css_transformer.py`

 * *Files 13% similar despite different names*

```diff
@@ -7,14 +7,20 @@
 TEST_STYLES = '''
 @import foo;
 
 .orange {
     color: #abc;
 }
 
+.a, .b {
+    .c, .d {
+        color: #def;
+    }
+}
+
 p {
     color: #fff;
     a {
         color: #55f;
     }
     .red {
         color: #f55;
```

### Comparing `anchovy-0.7.1/examples/gallery/index.md` & `anchovy-0.8.0/examples/gallery/index.md`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/gallery/static/core.css` & `anchovy-0.8.0/examples/gallery/static/core.css`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/examples/gallery.py` & `anchovy-0.8.0/examples/gallery.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/pyproject.toml` & `anchovy-0.8.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/src/anchovy/cli.py` & `anchovy-0.8.0/src/anchovy/cli.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/src/anchovy/core.py` & `anchovy-0.8.0/src/anchovy/core.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/src/anchovy/css/__init__.py` & `anchovy-0.8.0/src/anchovy/css/__init__.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/src/anchovy/css/parser.py` & `anchovy-0.8.0/src/anchovy/css/parser.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/src/anchovy/dependencies.py` & `anchovy-0.8.0/src/anchovy/dependencies.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/src/anchovy/images.py` & `anchovy-0.8.0/src/anchovy/images.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/src/anchovy/jinja.py` & `anchovy-0.8.0/src/anchovy/jinja.py`

 * *Files 3% similar despite different names*

```diff
@@ -5,16 +5,14 @@
 from functools import reduce
 from pathlib import Path
 
 from .core import Context, Step
 from .dependencies import pip_dependency, Dependency
 
 if t.TYPE_CHECKING:
-    import commonmark
-    import commonmark.render.renderer
     from jinja2 import Environment
 
 
 MDProcessor = t.Callable[[str], str]
 
 
 class JinjaRenderStep(Step):
```

### Comparing `anchovy-0.7.1/src/anchovy/paths.py` & `anchovy-0.8.0/src/anchovy/paths.py`

 * *Files 10% similar despite different names*

```diff
@@ -13,22 +13,29 @@
     if 'stem' in _groups:
         return path.with_stem(_groups['stem'])
     if 'ext' in _groups and _groups['ext']:
         return path.with_name(path.name[:-len(_groups['ext'])])
     return path
 
 
-def _to_dir_inner(dest: Path, ext: str | None, context: Context, path: Path, match: t.Any):
+def _to_dir_inner(dest: Path,
+                  ext: str | None,
+                  context: Context,
+                  path: Path,
+                  match: t.Any,
+                  transform: t.Callable[[Path], Path] | None = None):
     path = _trim_ext_prefix(path, match) if ext and isinstance(match, re.Match) else path
 
     rel = path.relative_to(
         context['input_dir']
         if path.is_relative_to(context['input_dir'])
         else context['working_dir']
     )
+    if transform:
+        rel = transform(rel)
     new_path = dest / rel
 
     if ext:
         new_path = new_path.with_suffix(ext)
 
     return new_path
 
@@ -37,52 +44,55 @@
     """
     PathCalc which makes its input paths children of a specified directory.
     If @ext is specified, it will replace the extension of input paths. If the
     matcher produced an re.Match, it will be checked for explicitly defined
     extension information for the input paths, allowing for meaningful work
     with extensions that `pathlib.Path` does not reflect, like `.tar.gz`.
     """
-    def __init__(self, dest: Path, ext: str | None = None):
+    def __init__(self, dest: Path, ext: str | None = None, transform: t.Callable[[Path], Path] | None = None):
         self.dest = dest
         self.ext = ext
+        self.transform = transform
 
     def __call__(self, context: Context, path: Path, match: T) -> Path:
-        return _to_dir_inner(self.dest, self.ext, context, path, match)
+        return _to_dir_inner(self.dest, self.ext, context, path, match, self.transform)
 
 
 class OutputDirPathCalc(PathCalc[T]):
     """
     PathCalc which makes its input paths children of the Context's output
     directory. If @ext is specified, it will replace the extension of input
     paths. If the matcher produced an re.Match, it will be checked for
     explicitly defined extension information for the input paths, allowing for
     meaningful work with extensions that `pathlib.Path` does not reflect, like
     `.tar.gz`.
     """
-    def __init__(self, ext: str | None = None):
+    def __init__(self, ext: str | None = None, transform: t.Callable[[Path], Path] | None = None):
         self.ext = ext
+        self.transform = transform
 
     def __call__(self, context: Context, path: Path, match: T) -> Path:
-        return _to_dir_inner(context['output_dir'], self.ext, context, path, match)
+        return _to_dir_inner(context['output_dir'], self.ext, context, path, match, self.transform)
 
 
 class WorkingDirPathCalc(PathCalc[T]):
     """
     PathCalc which makes its input paths children of the Context's working
     directory. If @ext is specified, it will replace the extension of input
     paths. If the matcher produced an re.Match, it will be checked for
     explicitly defined extension information for the input paths, allowing for
     meaningful work with extensions that `pathlib.Path` does not reflect, like
     `.tar.gz`.
     """
-    def __init__(self, ext: str | None = None):
+    def __init__(self, ext: str | None = None, transform: t.Callable[[Path], Path] | None = None):
         self.ext = ext
+        self.transform = transform
 
     def __call__(self, context: Context, path: Path, match: T) -> Path:
-        return _to_dir_inner(context['working_dir'], self.ext, context, path, match)
+        return _to_dir_inner(context['working_dir'], self.ext, context, path, match, self.transform)
 
 
 class REMatcher(Matcher[re.Match | None]):
     """
     Path Matcher using regular expressions. @re_flags will be passed to
     `re.compile()`. @parent_dir, if specified, should be a key to a configured
     directory, not a Path, and will be used to handle matching the beginning of
```

### Comparing `anchovy-0.7.1/src/anchovy/pretty_utils.py` & `anchovy-0.8.0/src/anchovy/pretty_utils.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/src/anchovy/simple.py` & `anchovy-0.8.0/src/anchovy/simple.py`

 * *Files identical despite different names*

### Comparing `anchovy-0.7.1/src/anchovy.egg-info/PKG-INFO` & `anchovy-0.8.0/src/anchovy.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: anchovy
-Version: 0.7.1
+Version: 0.8.0
 Summary: A minimal, unopinionated file processing engine intended for static website generation.
 Author-email: Daniel Foerster <pydsigner@gmail.com>
 License: Apache-2.0
 Keywords: static,website,generation,html,css,template
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: Apache Software License
```

### Comparing `anchovy-0.7.1/src/anchovy.egg-info/SOURCES.txt` & `anchovy-0.8.0/src/anchovy.egg-info/SOURCES.txt`

 * *Files identical despite different names*

