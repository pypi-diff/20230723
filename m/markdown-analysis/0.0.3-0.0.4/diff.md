# Comparing `tmp/markdown_analysis-0.0.3.tar.gz` & `tmp/markdown_analysis-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "markdown_analysis-0.0.3.tar", last modified: Sun Jul 23 16:37:35 2023, max compression
+gzip compressed data, was "markdown_analysis-0.0.4.tar", last modified: Sun Jul 23 19:09:48 2023, max compression
```

## Comparing `markdown_analysis-0.0.3.tar` & `markdown_analysis-0.0.4.tar`

### file list

```diff
@@ -1,16 +1,17 @@
-drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 16:37:35.879602 markdown_analysis-0.0.3/
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1066 2023-07-23 10:09:40.000000 markdown_analysis-0.0.3/LICENSE
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     2046 2023-07-23 16:37:35.877601 markdown_analysis-0.0.3/PKG-INFO
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1538 2023-07-23 10:10:57.000000 markdown_analysis-0.0.3/README.md
-drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 16:37:35.831153 markdown_analysis-0.0.3/markdown_analysis.egg-info/
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     2046 2023-07-23 16:37:35.000000 markdown_analysis-0.0.3/markdown_analysis.egg-info/PKG-INFO
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      272 2023-07-23 16:37:35.000000 markdown_analysis-0.0.3/markdown_analysis.egg-info/SOURCES.txt
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        1 2023-07-23 16:37:35.000000 markdown_analysis-0.0.3/markdown_analysis.egg-info/dependency_links.txt
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       21 2023-07-23 16:37:35.000000 markdown_analysis-0.0.3/markdown_analysis.egg-info/top_level.txt
-drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 16:37:35.854154 markdown_analysis-0.0.3/mrkdwn_analysis/
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       47 2023-07-23 16:33:54.000000 markdown_analysis-0.0.3/mrkdwn_analysis/__init__.py
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1321 2023-07-23 10:11:58.000000 markdown_analysis-0.0.3/mrkdwn_analysis/markdown_analyzer.py
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       38 2023-07-23 16:37:35.880602 markdown_analysis-0.0.3/setup.cfg
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      830 2023-07-23 16:37:32.000000 markdown_analysis-0.0.3/setup.py
-drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 16:37:35.865601 markdown_analysis-0.0.3/test/
--rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 09:52:05.000000 markdown_analysis-0.0.3/test/__init__.py
+drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 19:09:48.452633 markdown_analysis-0.0.4/
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     1066 2023-07-23 10:09:40.000000 markdown_analysis-0.0.4/LICENSE
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     7582 2023-07-23 19:09:48.449631 markdown_analysis-0.0.4/PKG-INFO
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     7102 2023-07-23 19:06:35.000000 markdown_analysis-0.0.4/README.md
+drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 19:09:48.403425 markdown_analysis-0.0.4/markdown_analysis.egg-info/
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)     7582 2023-07-23 19:09:48.000000 markdown_analysis-0.0.4/markdown_analysis.egg-info/PKG-INFO
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      312 2023-07-23 19:09:48.000000 markdown_analysis-0.0.4/markdown_analysis.egg-info/SOURCES.txt
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        1 2023-07-23 19:09:48.000000 markdown_analysis-0.0.4/markdown_analysis.egg-info/dependency_links.txt
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       17 2023-07-23 19:09:48.000000 markdown_analysis-0.0.4/markdown_analysis.egg-info/requires.txt
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       21 2023-07-23 19:09:48.000000 markdown_analysis-0.0.4/markdown_analysis.egg-info/top_level.txt
+drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 19:09:48.424948 markdown_analysis-0.0.4/mrkdwn_analysis/
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       47 2023-07-23 16:33:54.000000 markdown_analysis-0.0.4/mrkdwn_analysis/__init__.py
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)    11721 2023-07-23 18:23:58.000000 markdown_analysis-0.0.4/mrkdwn_analysis/markdown_analyzer.py
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)       38 2023-07-23 19:09:48.453633 markdown_analysis-0.0.4/setup.cfg
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)      775 2023-07-23 19:09:27.000000 markdown_analysis-0.0.4/setup.py
+drwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 19:09:48.436949 markdown_analysis-0.0.4/test/
+-rwxrwxrwx   0 ybanas    (1000) ybanas    (1000)        0 2023-07-23 09:52:05.000000 markdown_analysis-0.0.4/test/__init__.py
```

### Comparing `markdown_analysis-0.0.3/LICENSE` & `markdown_analysis-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `markdown_analysis-0.0.3/setup.py` & `markdown_analysis-0.0.4/setup.py`

 * *Files 22% similar despite different names*

```diff
@@ -2,24 +2,24 @@
 
 # Lire le contenu du fichier README
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setup(
     name='markdown_analysis',
-    version='0.0.3',
+    version='0.0.4',
     long_description=long_description,
     long_description_content_type="text/markdown",
-    description='A library to analyze markdown files',
     author='yannbanas',
     author_email='yannbanas@gmail.com',
     url='https://github.com/yannbanas/mrkdwn_analysis',
     packages=find_packages(),
     install_requires=[
-        # list your dependencies here
+        'urllib3',
+        'requests'
     ],
     classifiers=[
         'Development Status :: 2 - Pre-Alpha',
         'Intended Audience :: Developers',
         'License :: OSI Approved :: MIT License',
         'Programming Language :: Python :: 3.11',
     ],
```

