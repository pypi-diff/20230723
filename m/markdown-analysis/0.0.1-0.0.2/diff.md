# Comparing `tmp/markdown_analysis-0.0.1.tar.gz` & `tmp/markdown_analysis-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "markdown_analysis-0.0.1.tar", last modified: Sun Jul 23 10:27:47 2023, max compression
+gzip compressed data, was "markdown_analysis-0.0.2.tar", last modified: Sun Jul 23 10:42:02 2023, max compression
```

## Comparing `markdown_analysis-0.0.1.tar` & `markdown_analysis-0.0.2.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 10:27:47.315466 markdown_analysis-0.0.1/
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1066 2023-07-23 10:09:40.000000 markdown_analysis-0.0.1/LICENSE
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      475 2023-07-23 10:27:47.313953 markdown_analysis-0.0.1/PKG-INFO
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1538 2023-07-23 10:10:57.000000 markdown_analysis-0.0.1/README.md
-drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 10:27:47.276834 markdown_analysis-0.0.1/markdown_analysis.egg-info/
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      475 2023-07-23 10:27:47.000000 markdown_analysis-0.0.1/markdown_analysis.egg-info/PKG-INFO
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      272 2023-07-23 10:27:47.000000 markdown_analysis-0.0.1/markdown_analysis.egg-info/SOURCES.txt
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        1 2023-07-23 10:27:47.000000 markdown_analysis-0.0.1/markdown_analysis.egg-info/dependency_links.txt
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       21 2023-07-23 10:27:47.000000 markdown_analysis-0.0.1/markdown_analysis.egg-info/top_level.txt
-drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 10:27:47.295894 markdown_analysis-0.0.1/mrkdwn_analysis/
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 09:51:56.000000 markdown_analysis-0.0.1/mrkdwn_analysis/__init__.py
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1321 2023-07-23 10:11:58.000000 markdown_analysis-0.0.1/mrkdwn_analysis/markdown_analyzer.py
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       38 2023-07-23 10:27:47.316464 markdown_analysis-0.0.1/setup.cfg
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      611 2023-07-23 10:27:18.000000 markdown_analysis-0.0.1/setup.py
-drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 10:27:47.304422 markdown_analysis-0.0.1/test/
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 09:52:05.000000 markdown_analysis-0.0.1/test/__init__.py
+drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 10:42:02.817616 markdown_analysis-0.0.2/
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1066 2023-07-23 10:09:40.000000 markdown_analysis-0.0.2/LICENSE
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     2046 2023-07-23 10:42:02.815615 markdown_analysis-0.0.2/PKG-INFO
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1538 2023-07-23 10:10:57.000000 markdown_analysis-0.0.2/README.md
+drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 10:42:02.771615 markdown_analysis-0.0.2/markdown_analysis.egg-info/
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     2046 2023-07-23 10:42:02.000000 markdown_analysis-0.0.2/markdown_analysis.egg-info/PKG-INFO
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      272 2023-07-23 10:42:02.000000 markdown_analysis-0.0.2/markdown_analysis.egg-info/SOURCES.txt
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        1 2023-07-23 10:42:02.000000 markdown_analysis-0.0.2/markdown_analysis.egg-info/dependency_links.txt
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       21 2023-07-23 10:42:02.000000 markdown_analysis-0.0.2/markdown_analysis.egg-info/top_level.txt
+drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 10:42:02.792617 markdown_analysis-0.0.2/mrkdwn_analysis/
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 09:51:56.000000 markdown_analysis-0.0.2/mrkdwn_analysis/__init__.py
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1321 2023-07-23 10:11:58.000000 markdown_analysis-0.0.2/mrkdwn_analysis/markdown_analyzer.py
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       38 2023-07-23 10:42:02.817616 markdown_analysis-0.0.2/setup.cfg
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      830 2023-07-23 10:41:57.000000 markdown_analysis-0.0.2/setup.py
+drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 10:42:02.803615 markdown_analysis-0.0.2/test/
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 09:52:05.000000 markdown_analysis-0.0.2/test/__init__.py
```

### Comparing `markdown_analysis-0.0.1/LICENSE` & `markdown_analysis-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `markdown_analysis-0.0.1/README.md` & `markdown_analysis-0.0.2/README.md`

 * *Files identical despite different names*

### Comparing `markdown_analysis-0.0.1/mrkdwn_analysis/markdown_analyzer.py` & `markdown_analysis-0.0.2/mrkdwn_analysis/markdown_analyzer.py`

 * *Files identical despite different names*

### Comparing `markdown_analysis-0.0.1/setup.py` & `markdown_analysis-0.0.2/setup.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,12 +1,18 @@
 from setuptools import setup, find_packages
 
+# Lire le contenu du fichier README
+with open("README.md", "r", encoding="utf-8") as fh:
+    long_description = fh.read()
+
 setup(
     name='markdown_analysis',
-    version='0.0.1',
+    version='0.0.2',
+    long_description=long_description,
+    long_description_content_type="text/markdown",
     description='A library to analyze markdown files',
     author='yannbanas',
     author_email='yannbanas@gmail.com',
     url='https://github.com/yannbanas/mrkdwn_analysis',
     packages=find_packages(),
     install_requires=[
         # list your dependencies here
```

