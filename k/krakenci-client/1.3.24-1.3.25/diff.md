# Comparing `tmp/krakenci_client-1.3.24.tar.gz` & `tmp/krakenci_client-1.3.25.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "krakenci_client-1.3.24.tar", max compression
+gzip compressed data, was "krakenci_client-1.3.25.tar", max compression
```

## Comparing `krakenci_client-1.3.24.tar` & `krakenci_client-1.3.25.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0     1401 2023-07-13 05:30:44.000000 krakenci_client-1.3.24/README.md
--rw-r--r--   0        0        0    12722 2023-07-13 05:30:44.000000 krakenci_client-1.3.24/kraken/client/main.py
--rw-r--r--   0        0        0     2222 2023-07-13 05:32:39.533655 krakenci_client-1.3.24/kraken/client/toolops.py
--rw-r--r--   0        0        0       19 2023-07-13 05:32:39.533655 krakenci_client-1.3.24/kraken/client/version.py
--rw-r--r--   0        0        0     1069 2023-07-13 05:32:40.137655 krakenci_client-1.3.24/pyproject.tml
--rw-r--r--   0        0        0     2312 1970-01-01 00:00:00.000000 krakenci_client-1.3.24/setup.py
--rw-r--r--   0        0        0     2595 1970-01-01 00:00:00.000000 krakenci_client-1.3.24/PKG-INFO
+-rw-r--r--   0        0        0     1401 2023-07-22 13:18:10.000000 krakenci_client-1.3.25/README.md
+-rw-r--r--   0        0        0    12722 2023-07-22 13:18:10.000000 krakenci_client-1.3.25/kraken/client/main.py
+-rw-r--r--   0        0        0     2222 2023-07-22 13:20:02.772360 krakenci_client-1.3.25/kraken/client/toolops.py
+-rw-r--r--   0        0        0       19 2023-07-22 13:20:02.772360 krakenci_client-1.3.25/kraken/client/version.py
+-rw-r--r--   0        0        0     1069 2023-07-22 13:20:03.324474 krakenci_client-1.3.25/pyproject.tml
+-rw-r--r--   0        0        0     2312 1970-01-01 00:00:00.000000 krakenci_client-1.3.25/setup.py
+-rw-r--r--   0        0        0     2595 1970-01-01 00:00:00.000000 krakenci_client-1.3.25/PKG-INFO
```

### Comparing `krakenci_client-1.3.24/README.md` & `krakenci_client-1.3.25/README.md`

 * *Files identical despite different names*

### Comparing `krakenci_client-1.3.24/kraken/client/main.py` & `krakenci_client-1.3.25/kraken/client/main.py`

 * *Files identical despite different names*

### Comparing `krakenci_client-1.3.24/kraken/client/toolops.py` & `krakenci_client-1.3.25/kraken/client/toolops.py`

 * *Files identical despite different names*

### Comparing `krakenci_client-1.3.24/pyproject.tml` & `krakenci_client-1.3.25/pyproject.tml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "krakenci-client"
-version="1.3.24"
+version="1.3.25"
 description = "A client tool for Kraken CI server."
 authors = ["Michal Nowikowski <godfryd@gmail.com>"]
 readme = "README.md"
 homepage = "https://kraken.ci/"
 repository = "https://github.com/kraken-ci/kraken"
 documentation = "https://kraken.ci/docs"
 keywords = ["building", "testing", "continuous-integration", "ci", "cd", "cicd"]
```

### Comparing `krakenci_client-1.3.24/setup.py` & `krakenci_client-1.3.25/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -14,15 +14,15 @@
  'tabulate>=0.8.9,<0.9.0']
 
 entry_points = \
 {'console_scripts': ['kkci = kraken.client.main:main']}
 
 setup_kwargs = {
     'name': 'krakenci-client',
-    'version': '1.3.24',
+    'version': '1.3.25',
     'description': 'A client tool for Kraken CI server.',
     'long_description': '# Kraken CI Client\n\nThis is a client tool for accessing Kraken CI server, https://kraken.ci.\n\n\n<!-- ABOUT THE PROJECT -->\n## About Kraken CI\n\n![Kraken CI Results Page](https://kraken.ci/img/slide-branch-results.png)\n\nKraken CI is a modern, open-source, on-premise CI/CD system\nthat is highly scalable and focused on testing.\n\nMore information can be found on https://kraken.ci\n\n\n<!-- GETTING STARTED -->\n## Getting Started\n\nQuick start guide is here: https://kraken.ci/docs/quick-start\n\nFull installation manual: https://kraken.ci/docs/installation\n\nAnd here is developers guide: https://kraken.ci/docs/dev-guide\n\n\n<!-- USAGE EXAMPLES -->\n## Usage\n\nGuides can be found here: https://kraken.ci/docs/guide-intro\n\nDemo site is available here: https://lab.kraken.ci/\n\n\n<!-- ROADMAP -->\n## Roadmap\n\nSee the [open issues](https://github.com/kraken-ci/kraken/issues) for a list of proposed features (and known issues).\n\n\n<!-- CONTRIBUTING -->\n## Contributing\n\nContributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.\n\nDetails on https://kraken.ci/docs/contrib-kraken\n\n\n<!-- LICENSE -->\n## License\n\nDistributed under the Apache 2.0 License. See `LICENSE` for more information.\n\n\n<!-- CONTACT -->\n## Contact\n\nMichal Nowikowski - godfryd@gmail.com\n\nProject Link: [https://kraken.ci](https://kraken.ci)\n',
     'author': 'Michal Nowikowski',
     'author_email': 'godfryd@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://kraken.ci/',
```

### Comparing `krakenci_client-1.3.24/PKG-INFO` & `krakenci_client-1.3.25/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: krakenci-client
-Version: 1.3.24
+Version: 1.3.25
 Summary: A client tool for Kraken CI server.
 Home-page: https://kraken.ci/
 License: Apache-2.0
 Keywords: building,testing,continuous-integration,ci,cd,cicd
 Author: Michal Nowikowski
 Author-email: godfryd@gmail.com
 Requires-Python: >=3.7,<4.0
```

