# Comparing `tmp/id2xml-1.5.1.tar.gz` & `tmp/id2xml-1.5.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "id2xml-1.5.1.tar", last modified: Wed Jul 12 19:43:14 2023, max compression
+gzip compressed data, was "id2xml-1.5.2.tar", last modified: Sun Jul 23 07:54:10 2023, max compression
```

## Comparing `id2xml-1.5.1.tar` & `id2xml-1.5.2.tar`

### file list

```diff
@@ -1,29 +1,29 @@
-drwxr-xr-x   0 kesara     (501) staff       (20)        0 2023-07-12 19:43:14.729301 id2xml-1.5.1/
--rw-r--r--   0 kesara     (501) staff       (20)     1507 2023-07-12 19:39:27.000000 id2xml-1.5.1/LICENSE
--rw-r--r--   0 kesara     (501) staff       (20)      325 2023-07-12 19:39:27.000000 id2xml-1.5.1/MANIFEST.in
--rw-r--r--   0 kesara     (501) staff       (20)     4137 2023-07-12 19:39:27.000000 id2xml-1.5.1/Makefile
--rw-r--r--   0 kesara     (501) staff       (20)     3176 2023-07-12 19:43:14.729179 id2xml-1.5.1/PKG-INFO
--rw-r--r--   0 kesara     (501) staff       (20)     1167 2023-07-12 19:39:27.000000 id2xml-1.5.1/README.rst
--rw-r--r--   0 kesara     (501) staff       (20)    20835 2023-07-12 19:39:27.000000 id2xml-1.5.1/changelog
-drwxr-xr-x   0 kesara     (501) staff       (20)        0 2023-07-12 19:43:14.727595 id2xml-1.5.1/id2xml/
--rw-r--r--   0 kesara     (501) staff       (20)      202 2023-07-12 19:39:27.000000 id2xml-1.5.1/id2xml/__init__.py
-drwxr-xr-x   0 kesara     (501) staff       (20)        0 2023-07-12 19:43:14.728911 id2xml-1.5.1/id2xml/data/
--rw-r--r--   0 kesara     (501) staff       (20)     7330 2023-07-12 19:39:27.000000 id2xml-1.5.1/id2xml/data/v2.rnc
--rw-r--r--   0 kesara     (501) staff       (20)    17351 2023-07-12 19:39:27.000000 id2xml-1.5.1/id2xml/data/v2.rng
--rw-r--r--   0 kesara     (501) staff       (20)    22756 2023-07-12 19:39:27.000000 id2xml-1.5.1/id2xml/data/v3.rnc
--rw-r--r--   0 kesara     (501) staff       (20)    51940 2023-07-12 19:39:27.000000 id2xml-1.5.1/id2xml/data/v3.rng
--rw-r--r--   0 kesara     (501) staff       (20)     6167 2023-07-12 19:39:27.000000 id2xml-1.5.1/id2xml/debug.py
--rw-r--r--   0 kesara     (501) staff       (20)   130702 2023-07-12 19:39:27.000000 id2xml-1.5.1/id2xml/parser.py
--rw-r--r--   0 kesara     (501) staff       (20)    10748 2023-07-12 19:39:27.000000 id2xml-1.5.1/id2xml/run.py
--rw-r--r--   0 kesara     (501) staff       (20)     6459 2023-07-12 19:39:27.000000 id2xml-1.5.1/id2xml/utils.py
-drwxr-xr-x   0 kesara     (501) staff       (20)        0 2023-07-12 19:43:14.728325 id2xml-1.5.1/id2xml.egg-info/
--rw-r--r--   0 kesara     (501) staff       (20)     3176 2023-07-12 19:43:14.000000 id2xml-1.5.1/id2xml.egg-info/PKG-INFO
--rw-r--r--   0 kesara     (501) staff       (20)      444 2023-07-12 19:43:14.000000 id2xml-1.5.1/id2xml.egg-info/SOURCES.txt
--rw-r--r--   0 kesara     (501) staff       (20)        1 2023-07-12 19:43:14.000000 id2xml-1.5.1/id2xml.egg-info/dependency_links.txt
--rw-r--r--   0 kesara     (501) staff       (20)       42 2023-07-12 19:43:14.000000 id2xml-1.5.1/id2xml.egg-info/entry_points.txt
--rw-r--r--   0 kesara     (501) staff       (20)        1 2023-07-12 19:43:14.000000 id2xml-1.5.1/id2xml.egg-info/not-zip-safe
--rw-r--r--   0 kesara     (501) staff       (20)       56 2023-07-12 19:43:14.000000 id2xml-1.5.1/id2xml.egg-info/requires.txt
--rw-r--r--   0 kesara     (501) staff       (20)        7 2023-07-12 19:43:14.000000 id2xml-1.5.1/id2xml.egg-info/top_level.txt
--rw-r--r--   0 kesara     (501) staff       (20)       43 2023-07-12 19:39:27.000000 id2xml-1.5.1/requirements.txt
--rw-r--r--   0 kesara     (501) staff       (20)       38 2023-07-12 19:43:14.729334 id2xml-1.5.1/setup.cfg
--rw-r--r--   0 kesara     (501) staff       (20)     5923 2023-07-12 19:39:27.000000 id2xml-1.5.1/setup.py
+drwxr-xr-x   0 kesara     (501) staff       (20)        0 2023-07-23 07:54:10.739709 id2xml-1.5.2/
+-rw-r--r--   0 kesara     (501) staff       (20)     1507 2023-07-12 19:39:27.000000 id2xml-1.5.2/LICENSE
+-rw-r--r--   0 kesara     (501) staff       (20)      325 2023-07-12 19:39:27.000000 id2xml-1.5.2/MANIFEST.in
+-rw-r--r--   0 kesara     (501) staff       (20)     4137 2023-07-12 19:39:27.000000 id2xml-1.5.2/Makefile
+-rw-r--r--   0 kesara     (501) staff       (20)     2292 2023-07-23 07:54:10.739599 id2xml-1.5.2/PKG-INFO
+-rw-r--r--   0 kesara     (501) staff       (20)     1167 2023-07-12 19:39:27.000000 id2xml-1.5.2/README.rst
+-rw-r--r--   0 kesara     (501) staff       (20)    20984 2023-07-23 07:53:48.000000 id2xml-1.5.2/changelog
+drwxr-xr-x   0 kesara     (501) staff       (20)        0 2023-07-23 07:54:10.737820 id2xml-1.5.2/id2xml/
+-rw-r--r--   0 kesara     (501) staff       (20)      202 2023-07-23 07:53:48.000000 id2xml-1.5.2/id2xml/__init__.py
+drwxr-xr-x   0 kesara     (501) staff       (20)        0 2023-07-23 07:54:10.739349 id2xml-1.5.2/id2xml/data/
+-rw-r--r--   0 kesara     (501) staff       (20)     7330 2023-07-12 19:39:27.000000 id2xml-1.5.2/id2xml/data/v2.rnc
+-rw-r--r--   0 kesara     (501) staff       (20)    17351 2023-07-12 19:39:27.000000 id2xml-1.5.2/id2xml/data/v2.rng
+-rw-r--r--   0 kesara     (501) staff       (20)    22756 2023-07-12 19:39:27.000000 id2xml-1.5.2/id2xml/data/v3.rnc
+-rw-r--r--   0 kesara     (501) staff       (20)    51940 2023-07-12 19:39:27.000000 id2xml-1.5.2/id2xml/data/v3.rng
+-rw-r--r--   0 kesara     (501) staff       (20)     6167 2023-07-12 19:39:27.000000 id2xml-1.5.2/id2xml/debug.py
+-rw-r--r--   0 kesara     (501) staff       (20)   130504 2023-07-23 07:53:48.000000 id2xml-1.5.2/id2xml/parser.py
+-rw-r--r--   0 kesara     (501) staff       (20)    10748 2023-07-12 19:39:27.000000 id2xml-1.5.2/id2xml/run.py
+-rw-r--r--   0 kesara     (501) staff       (20)     6459 2023-07-12 19:39:27.000000 id2xml-1.5.2/id2xml/utils.py
+drwxr-xr-x   0 kesara     (501) staff       (20)        0 2023-07-23 07:54:10.738747 id2xml-1.5.2/id2xml.egg-info/
+-rw-r--r--   0 kesara     (501) staff       (20)     2292 2023-07-23 07:54:10.000000 id2xml-1.5.2/id2xml.egg-info/PKG-INFO
+-rw-r--r--   0 kesara     (501) staff       (20)      444 2023-07-23 07:54:10.000000 id2xml-1.5.2/id2xml.egg-info/SOURCES.txt
+-rw-r--r--   0 kesara     (501) staff       (20)        1 2023-07-23 07:54:10.000000 id2xml-1.5.2/id2xml.egg-info/dependency_links.txt
+-rw-r--r--   0 kesara     (501) staff       (20)       42 2023-07-23 07:54:10.000000 id2xml-1.5.2/id2xml.egg-info/entry_points.txt
+-rw-r--r--   0 kesara     (501) staff       (20)        1 2023-07-12 19:43:14.000000 id2xml-1.5.2/id2xml.egg-info/not-zip-safe
+-rw-r--r--   0 kesara     (501) staff       (20)       56 2023-07-23 07:54:10.000000 id2xml-1.5.2/id2xml.egg-info/requires.txt
+-rw-r--r--   0 kesara     (501) staff       (20)        7 2023-07-23 07:54:10.000000 id2xml-1.5.2/id2xml.egg-info/top_level.txt
+-rw-r--r--   0 kesara     (501) staff       (20)       43 2023-07-12 19:39:27.000000 id2xml-1.5.2/requirements.txt
+-rw-r--r--   0 kesara     (501) staff       (20)       38 2023-07-23 07:54:10.739740 id2xml-1.5.2/setup.cfg
+-rw-r--r--   0 kesara     (501) staff       (20)     5923 2023-07-12 19:39:27.000000 id2xml-1.5.2/setup.py
```

### Comparing `id2xml-1.5.1/LICENSE` & `id2xml-1.5.2/LICENSE`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/Makefile` & `id2xml-1.5.2/Makefile`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/PKG-INFO` & `id2xml-1.5.2/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: id2xml
-Version: 1.5.1
+Version: 1.5.2
 Summary: Convert text-format RFCs and Internet-Drafts to .xml format
 Home-page: https://tools.ietf.org/tools/ietfdb/browser/branch/elft/id2xml/
 Author: Henrik Levkowetz
 Author-email: henrik@levkowetz.com
 License: Simplified BSD
 Keywords: Internet-Draft text to xml conversion
 Classifier: Development Status :: 5 - Production/Stable
@@ -45,44 +45,25 @@
 .. [2] Hoffman, P., "The "xml2rfc" Version 3 Vocabulary", RFC 7991, DOI
    10.17487/RFC7991, December 2016, http://www.rfc-editor.org/info/rfc7991>.
 
 
 Changelog
 =========
 
-Version 1.5.1 (12 Jul 2023)
+Version 1.5.2 (22 Jul 2023)
 ------------------------------------------------
 
 
-  * test: Improve tests (#14)
-
-  * fix: Parse boilerplate with revised BSD license (#13)
+  * fix: Avoid category loop (#18)
 
 
 
 
-Version 1.5.0 (03 Sep 2019)
+Version 1.5.1 (12 Jul 2023)
 ------------------------------------------------
 
 
-  * Fixed a few Python 3.x nits in the parser code.
-
-  * Changed generated anchor slugs so as to not collide with IDs used by 
-    xml2rfc, which in v3 mode reserves certain prefixes used for section, 
-    figure and table anchors and fragment identifiers.  Also fixed an xml2rfc 
-    v2v3 convertere compatibility issue.
-
-  * Added outdent to id2xml progress statements in order to more clearly 
-    differentiate them from warnings and errors.
-
-  * Added the possibility of setting document stream, IPR, and consensus 
-    values with switches instead of deriving them from the 'Status of this 
-    Memo' section, to make processing of documents with old status wording 
-    easier.
-
-  * Added a list of valid submission types and stream names to id2xml.utils.
-
-  * Tweaked several command-line options to better match those of xml2rfc.  
-    Added help for trace options when --help is given together with --debug.
+  * test: Improve tests (#14)
 
+  * fix: Parse boilerplate with revised BSD license (#13)
```

### Comparing `id2xml-1.5.1/README.rst` & `id2xml-1.5.2/README.rst`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/changelog` & `id2xml-1.5.2/changelog`

 * *Files 0% similar despite different names*

```diff
@@ -1,7 +1,13 @@
+id2xml (1.5.2) ietf; urgency=medium
+
+  * fix: Avoid category loop (#18)
+
+ -- Kesara Rathnayake  <kesara@staff.ietf.org>  22 Jul 2023 19:32:44 +1200
+
 id2xml (1.5.1) ietf; urgency=medium
 
   * test: Improve tests (#14)
 
   * fix: Parse boilerplate with revised BSD license (#13)
 
  -- Kesara Rathnayake  <kesara@staff.ietf.org>  12 Jul 2023 21:47:44 +1200
```

### Comparing `id2xml-1.5.1/id2xml/data/v2.rnc` & `id2xml-1.5.2/id2xml/data/v2.rnc`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/id2xml/data/v2.rng` & `id2xml-1.5.2/id2xml/data/v2.rng`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/id2xml/data/v3.rnc` & `id2xml-1.5.2/id2xml/data/v3.rnc`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/id2xml/data/v3.rng` & `id2xml-1.5.2/id2xml/data/v3.rng`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/id2xml/debug.py` & `id2xml-1.5.2/id2xml/debug.py`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/id2xml/parser.py` & `id2xml-1.5.2/id2xml/parser.py`

 * *Files 0% similar despite different names*

```diff
@@ -1489,27 +1489,23 @@
                     status_text = line.txt.split(None, 2)[-1].strip()
                     if not status_text in category_names:
                         self.warn(line.num, "Expected a recognized status name, found '%s'" % (line.txt, ))
                     else:
                         res.status = category_names[status_text]
                 else:
                     self.warn(line.num, "Expected 'Intended status: ', found '%s'" % (line.txt, ))
-                    lines.insert(0, line)
-                    self.dsay("pushing '%s'" % line.txt)
             else:
                 if line.txt.startswith('Category: '):
                     status_text = line.txt.split(None, 1)[-1].strip()
                     if not status_text in category_names:
                         self.warn(line.num, "Expected a recognized category, found '%s'" % (line.txt, ))
                     else:
                         res.status = category_names[status_text]
                 else:
                     self.warn(line.num, "Expected 'Category: ', found '%s'" % (line.txt, ))
-                    lines.insert(0, line)
-                    self.dsay("pushing '%s'" % line.txt)
 
         @dtrace
         def get_expiration(self, lines, res):
             # maybe expiration date
             if self.is_draft:
                 line = lines.pop(0) if lines else Line(None, '')
                 self.dshow('line')
```

### Comparing `id2xml-1.5.1/id2xml/run.py` & `id2xml-1.5.2/id2xml/run.py`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/id2xml/utils.py` & `id2xml-1.5.2/id2xml/utils.py`

 * *Files identical despite different names*

### Comparing `id2xml-1.5.1/id2xml.egg-info/PKG-INFO` & `id2xml-1.5.2/id2xml.egg-info/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: id2xml
-Version: 1.5.1
+Version: 1.5.2
 Summary: Convert text-format RFCs and Internet-Drafts to .xml format
 Home-page: https://tools.ietf.org/tools/ietfdb/browser/branch/elft/id2xml/
 Author: Henrik Levkowetz
 Author-email: henrik@levkowetz.com
 License: Simplified BSD
 Keywords: Internet-Draft text to xml conversion
 Classifier: Development Status :: 5 - Production/Stable
@@ -45,44 +45,25 @@
 .. [2] Hoffman, P., "The "xml2rfc" Version 3 Vocabulary", RFC 7991, DOI
    10.17487/RFC7991, December 2016, http://www.rfc-editor.org/info/rfc7991>.
 
 
 Changelog
 =========
 
-Version 1.5.1 (12 Jul 2023)
+Version 1.5.2 (22 Jul 2023)
 ------------------------------------------------
 
 
-  * test: Improve tests (#14)
-
-  * fix: Parse boilerplate with revised BSD license (#13)
+  * fix: Avoid category loop (#18)
 
 
 
 
-Version 1.5.0 (03 Sep 2019)
+Version 1.5.1 (12 Jul 2023)
 ------------------------------------------------
 
 
-  * Fixed a few Python 3.x nits in the parser code.
-
-  * Changed generated anchor slugs so as to not collide with IDs used by 
-    xml2rfc, which in v3 mode reserves certain prefixes used for section, 
-    figure and table anchors and fragment identifiers.  Also fixed an xml2rfc 
-    v2v3 convertere compatibility issue.
-
-  * Added outdent to id2xml progress statements in order to more clearly 
-    differentiate them from warnings and errors.
-
-  * Added the possibility of setting document stream, IPR, and consensus 
-    values with switches instead of deriving them from the 'Status of this 
-    Memo' section, to make processing of documents with old status wording 
-    easier.
-
-  * Added a list of valid submission types and stream names to id2xml.utils.
-
-  * Tweaked several command-line options to better match those of xml2rfc.  
-    Added help for trace options when --help is given together with --debug.
+  * test: Improve tests (#14)
 
+  * fix: Parse boilerplate with revised BSD license (#13)
```

### Comparing `id2xml-1.5.1/setup.py` & `id2xml-1.5.2/setup.py`

 * *Files identical despite different names*

