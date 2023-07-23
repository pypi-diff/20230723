# Comparing `tmp/pyassist-0.2.3.tar.gz` & `tmp/pyassist-0.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyassist-0.2.3.tar", last modified: Sat Jul 22 09:30:47 2023, max compression
+gzip compressed data, was "pyassist-0.2.4.tar", last modified: Sun Jul 23 21:07:15 2023, max compression
```

## Comparing `pyassist-0.2.3.tar` & `pyassist-0.2.4.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 09:30:47.419053 pyassist-0.2.3/
--rw-rw-rw-   0        0        0     1063 2023-06-28 16:14:31.000000 pyassist-0.2.3/LICENSE
--rw-rw-rw-   0        0        0      871 2023-07-22 09:30:47.419053 pyassist-0.2.3/PKG-INFO
--rw-rw-rw-   0        0        0       52 2023-06-28 16:30:47.000000 pyassist-0.2.3/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 09:30:47.405051 pyassist-0.2.3/pyassist/
--rw-rw-rw-   0        0        0      272 2023-05-18 18:11:12.000000 pyassist-0.2.3/pyassist/CustomError.py
-drwxrwxrwx   0        0        0        0 2023-07-22 09:30:47.416053 pyassist-0.2.3/pyassist/Network/
--rw-rw-rw-   0        0        0       54 2023-06-29 10:38:20.000000 pyassist-0.2.3/pyassist/Network/__init__.py
--rw-rw-rw-   0        0        0     7013 2023-07-22 09:16:27.000000 pyassist-0.2.3/pyassist/Network/network.py
--rw-rw-rw-   0        0        0     8704 2023-06-29 10:57:47.000000 pyassist-0.2.3/pyassist/Network/proxy.py
-drwxrwxrwx   0        0        0        0 2023-07-22 09:30:47.418054 pyassist-0.2.3/pyassist/Scraper/
--rw-rw-rw-   0        0        0       52 2023-06-29 11:24:12.000000 pyassist-0.2.3/pyassist/Scraper/__init__.py
--rw-rw-rw-   0        0        0     1821 2023-06-29 11:22:50.000000 pyassist-0.2.3/pyassist/Scraper/bs4.py
--rw-rw-rw-   0        0        0     3960 2023-06-30 17:19:32.000000 pyassist-0.2.3/pyassist/Scraper/selenium.py
--rw-rw-rw-   0        0        0      102 2023-07-01 21:15:26.000000 pyassist-0.2.3/pyassist/__init__.py
--rw-rw-rw-   0        0        0     1834 2023-06-29 10:33:09.000000 pyassist-0.2.3/pyassist/process.py
--rw-rw-rw-   0        0        0     1961 2023-06-29 10:33:04.000000 pyassist-0.2.3/pyassist/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-22 09:30:47.414051 pyassist-0.2.3/pyassist.egg-info/
--rw-rw-rw-   0        0        0      871 2023-07-22 09:30:47.000000 pyassist-0.2.3/pyassist.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      443 2023-07-22 09:30:47.000000 pyassist-0.2.3/pyassist.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 09:30:47.000000 pyassist-0.2.3/pyassist.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       78 2023-07-22 09:30:47.000000 pyassist-0.2.3/pyassist.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-07-22 09:30:47.000000 pyassist-0.2.3/pyassist.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       86 2023-07-22 09:30:47.420051 pyassist-0.2.3/setup.cfg
--rw-rw-rw-   0        0        0     2050 2023-07-22 09:30:40.000000 pyassist-0.2.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:07:15.228216 pyassist-0.2.4/
+-rw-rw-rw-   0        0        0     1063 2023-06-28 16:14:31.000000 pyassist-0.2.4/LICENSE
+-rw-rw-rw-   0        0        0      871 2023-07-23 21:07:15.228216 pyassist-0.2.4/PKG-INFO
+-rw-rw-rw-   0        0        0       52 2023-06-28 16:30:47.000000 pyassist-0.2.4/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 21:07:15.206208 pyassist-0.2.4/pyassist/
+-rw-rw-rw-   0        0        0      272 2023-05-18 18:11:12.000000 pyassist-0.2.4/pyassist/CustomError.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:07:15.225208 pyassist-0.2.4/pyassist/Network/
+-rw-rw-rw-   0        0        0       54 2023-06-29 10:38:20.000000 pyassist-0.2.4/pyassist/Network/__init__.py
+-rw-rw-rw-   0        0        0     7013 2023-07-22 09:16:27.000000 pyassist-0.2.4/pyassist/Network/network.py
+-rw-rw-rw-   0        0        0     8704 2023-06-29 10:57:47.000000 pyassist-0.2.4/pyassist/Network/proxy.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:07:15.227215 pyassist-0.2.4/pyassist/Scraper/
+-rw-rw-rw-   0        0        0       52 2023-06-29 11:24:12.000000 pyassist-0.2.4/pyassist/Scraper/__init__.py
+-rw-rw-rw-   0        0        0     1821 2023-06-29 11:22:50.000000 pyassist-0.2.4/pyassist/Scraper/bs4.py
+-rw-rw-rw-   0        0        0     3960 2023-06-30 17:19:32.000000 pyassist-0.2.4/pyassist/Scraper/selenium.py
+-rw-rw-rw-   0        0        0      102 2023-07-01 21:15:26.000000 pyassist-0.2.4/pyassist/__init__.py
+-rw-rw-rw-   0        0        0     1834 2023-06-29 10:33:09.000000 pyassist-0.2.4/pyassist/process.py
+-rw-rw-rw-   0        0        0     2209 2023-07-23 20:38:17.000000 pyassist-0.2.4/pyassist/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:07:15.222205 pyassist-0.2.4/pyassist.egg-info/
+-rw-rw-rw-   0        0        0      871 2023-07-23 21:07:15.000000 pyassist-0.2.4/pyassist.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      443 2023-07-23 21:07:15.000000 pyassist-0.2.4/pyassist.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 21:07:15.000000 pyassist-0.2.4/pyassist.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       78 2023-07-23 21:07:15.000000 pyassist-0.2.4/pyassist.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 21:07:15.000000 pyassist-0.2.4/pyassist.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       86 2023-07-23 21:07:15.229217 pyassist-0.2.4/setup.cfg
+-rw-rw-rw-   0        0        0     2050 2023-07-23 21:06:41.000000 pyassist-0.2.4/setup.py
```

### Comparing `pyassist-0.2.3/LICENSE` & `pyassist-0.2.4/LICENSE`

 * *Files identical despite different names*

### Comparing `pyassist-0.2.3/PKG-INFO` & `pyassist-0.2.4/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pyassist
-Version: 0.2.3
+Version: 0.2.4
 Summary: This is Python Utility
 Home-page: https://github.com/ISabariRajan
-Download-URL: https://github.com/ISabariRajan/Utilities/archive/refs/tags/v-0.2.3.tar.gz
+Download-URL: https://github.com/ISabariRajan/Utilities/archive/refs/tags/v-0.2.4.tar.gz
 Author: Sabari Rajan
 Author-email: mailme@isbarirajan.com
 License: MIT
 Keywords: Utility,utils,pyutils,assist,easy,service
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Build Tools
```

### Comparing `pyassist-0.2.3/pyassist/Network/network.py` & `pyassist-0.2.4/pyassist/Network/network.py`

 * *Files identical despite different names*

### Comparing `pyassist-0.2.3/pyassist/Network/proxy.py` & `pyassist-0.2.4/pyassist/Network/proxy.py`

 * *Files identical despite different names*

### Comparing `pyassist-0.2.3/pyassist/Scraper/bs4.py` & `pyassist-0.2.4/pyassist/Scraper/bs4.py`

 * *Files identical despite different names*

### Comparing `pyassist-0.2.3/pyassist/Scraper/selenium.py` & `pyassist-0.2.4/pyassist/Scraper/selenium.py`

 * *Files identical despite different names*

### Comparing `pyassist-0.2.3/pyassist/process.py` & `pyassist-0.2.4/pyassist/process.py`

 * *Files identical despite different names*

### Comparing `pyassist-0.2.3/pyassist/utils.py` & `pyassist-0.2.4/pyassist/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -27,14 +27,21 @@
 
     def parent_dir(self, filename):
         expanded_dir = os.path.expanduser(filename)
         realpath_dir = os.path.realpath(expanded_dir)
         directory = os.path.dirname(realpath_dir)
         return directory
 
+    def check_and_log_errors(self, error=None, header="Error: "):
+        if error:
+            if isinstance(error, list):
+                error = "\n".join(error)
+            message = f"{header}\n{error}"
+            self.error(message)
+
     # decode
     # * Decodes a byte to ("UTF-8") String
     # @param message    - Message to be decoded
     # @return String
     def decode(self, message):
         return message.decode("utf-8").strip()
```

### Comparing `pyassist-0.2.3/pyassist.egg-info/PKG-INFO` & `pyassist-0.2.4/pyassist.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: pyassist
-Version: 0.2.3
+Version: 0.2.4
 Summary: This is Python Utility
 Home-page: https://github.com/ISabariRajan
-Download-URL: https://github.com/ISabariRajan/Utilities/archive/refs/tags/v-0.2.3.tar.gz
+Download-URL: https://github.com/ISabariRajan/Utilities/archive/refs/tags/v-0.2.4.tar.gz
 Author: Sabari Rajan
 Author-email: mailme@isbarirajan.com
 License: MIT
 Keywords: Utility,utils,pyutils,assist,easy,service
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Build Tools
```

### Comparing `pyassist-0.2.3/setup.py` & `pyassist-0.2.4/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -6,21 +6,21 @@
 setup(
   name = 'pyassist',         # How you named your package folder (MyLib)
   packages = [
       'pyassist',
       'pyassist.Network',
       'pyassist.Scraper'
       ],   # Chose the same as "name"
-  version = '0.2.3',      # Start with a small number and increase it with every change you make
+  version = '0.2.4',      # Start with a small number and increase it with every change you make
   license='MIT',        # Chose a license from here: https://help.github.com/articles/licensing-a-repository
   description = """This is Python Utility""",   # Give a short description about your library
   author = 'Sabari Rajan',                   # Type in your name
   author_email = 'mailme@isbarirajan.com',      # Type in your E-Mail
   url = 'https://github.com/ISabariRajan',   # Provide either the link to your github or to your website
-  download_url = 'https://github.com/ISabariRajan/Utilities/archive/refs/tags/v-0.2.3.tar.gz',    # I explain this later on
+  download_url = 'https://github.com/ISabariRajan/Utilities/archive/refs/tags/v-0.2.4.tar.gz',    # I explain this later on
   keywords = ['Utility', 'utils', 'pyutils', 'assist', 'easy', 'service'],   # Keywords that define your package best
   install_requires=[
       "lxml", "pyloggerutils", "requests", "urllib3", "BeautifulSoup4", "webdriver_manager", "selenium"
   ],
   classifiers=[
     'Development Status :: 3 - Alpha',      # Chose either "3 - Alpha", "4 - Beta" or "5 - Production/Stable" as the current state of your package
     'Intended Audience :: Developers',      # Define that your audience are developers
```

