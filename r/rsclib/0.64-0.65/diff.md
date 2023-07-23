# Comparing `tmp/rsclib-0.64.tar.gz` & `tmp/rsclib-0.65.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rsclib-0.64.tar", last modified: Tue Mar 28 15:59:14 2023, max compression
+gzip compressed data, was "rsclib-0.65.tar", last modified: Sun Jul 23 13:53:12 2023, max compression
```

## Comparing `rsclib-0.64.tar` & `rsclib-0.65.tar`

### file list

```diff
@@ -1,47 +1,51 @@
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-03-28 15:59:14.281975 rsclib-0.64/
--rw-r--r--   0 ralf      (1000) priv      (1011)    31338 2023-03-28 15:59:14.285975 rsclib-0.64/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)    35805 2023-03-28 15:58:57.053979 rsclib-0.64/README.html
--rw-r--r--   0 ralf      (1000) priv      (1011)    25150 2023-03-28 15:56:54.866004 rsclib-0.64/README.rst
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-03-28 15:59:14.233975 rsclib-0.64/bin/
--rwxr-xr-x   0 ralf      (1000) priv      (1011)      546 2022-03-15 09:28:59.516873 rsclib-0.64/bin/ast_sip_check
--rwxr-xr-x   0 ralf      (1000) priv      (1011)      479 2022-03-15 09:28:59.516873 rsclib-0.64/bin/rsclib-hexdump
--rw-r--r--   0 ralf      (1000) priv      (1011)      821 2022-03-15 09:28:59.520873 rsclib-0.64/bin/rsclib-unhexdump
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-03-28 15:59:14.281975 rsclib-0.64/rsclib/
--rw-r--r--   0 ralf      (1000) priv      (1011)     2729 2022-03-15 09:28:59.524873 rsclib-0.64/rsclib/Config_File.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    35410 2022-03-15 09:28:59.532873 rsclib-0.64/rsclib/IP_Address.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     2983 2021-07-20 11:13:43.380502 rsclib-0.64/rsclib/Math.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    13272 2021-07-20 11:13:52.056499 rsclib-0.64/rsclib/PDF_Signature.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     4232 2022-03-15 09:28:59.536873 rsclib-0.64/rsclib/PM_Value.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     5976 2020-01-14 20:33:59.546694 rsclib-0.64/rsclib/Phone.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     6545 2017-08-06 17:21:57.553518 rsclib-0.64/rsclib/Rational.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     4470 2017-07-24 22:10:03.732670 rsclib-0.64/rsclib/TeX_CSV_Writer.py
--rw-r--r--   0 ralf      (1000) priv      (1011)       15 2023-03-28 15:58:57.057978 rsclib-0.64/rsclib/Version.py
--rw-r--r--   0 ralf      (1000) priv      (1011)       37 2014-04-12 19:15:07.000000 rsclib-0.64/rsclib/__init__.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    42872 2020-03-03 14:08:03.970874 rsclib-0.64/rsclib/ast_call.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     6509 2022-03-15 09:28:59.540873 rsclib-0.64/rsclib/ast_cdr.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     4266 2020-01-14 20:33:59.550695 rsclib-0.64/rsclib/ast_probe.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     1281 2019-12-01 20:44:56.608060 rsclib-0.64/rsclib/autosuper.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     1523 2020-01-14 20:33:59.550695 rsclib-0.64/rsclib/base_pickler.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    11164 2020-01-14 20:33:59.562694 rsclib-0.64/rsclib/bero.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     1731 2021-07-20 12:27:41.302946 rsclib-0.64/rsclib/capacitance.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     9080 2020-01-14 20:33:59.570695 rsclib-0.64/rsclib/crm.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    22717 2023-03-28 14:44:39.051152 rsclib-0.64/rsclib/execute.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2291 2017-07-24 21:21:50.828835 rsclib-0.64/rsclib/grepmime.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     3634 2022-03-15 09:28:59.544873 rsclib-0.64/rsclib/hexdump.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    18943 2018-08-16 20:18:30.407214 rsclib-0.64/rsclib/inductance.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    30587 2022-03-15 09:28:59.548873 rsclib-0.64/rsclib/isdn.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     6244 2017-07-24 21:22:14.300673 rsclib-0.64/rsclib/iter_recipes.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     1778 2017-07-24 22:50:36.687654 rsclib-0.64/rsclib/lc_resonator.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    20872 2022-03-15 09:28:59.552873 rsclib-0.64/rsclib/nmap.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    17926 2020-01-14 20:33:59.586694 rsclib-0.64/rsclib/ocf.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     3050 2022-03-30 12:40:10.298578 rsclib-0.64/rsclib/pycompat.py
--rw-r--r--   0 ralf      (1000) zoo-staff  (1014)    50686 2021-10-04 16:00:23.603166 rsclib-0.64/rsclib/sqlparser.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     7208 2022-03-15 09:28:59.560873 rsclib-0.64/rsclib/stateparser.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     2086 2017-07-24 22:10:49.980349 rsclib-0.64/rsclib/timeout.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    31827 2022-03-15 09:28:59.568873 rsclib-0.64/rsclib/trafficshape.py
--rw-r--r--   0 ralf      (1000) priv      (1011)      345 2021-04-24 14:24:52.322329 rsclib-0.64/rsclib/velocityfactor.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     3014 2022-03-15 09:28:59.572873 rsclib-0.64/setup.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)      573 2022-03-15 09:28:59.576873 rsclib-0.64/test2_exec.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)      700 2022-03-15 09:28:59.584873 rsclib-0.64/test_exec.py
--rw-r--r--   0 ralf      (1000) priv      (1011)      261 2022-03-15 09:28:59.588873 rsclib-0.64/test_ipt.py
--rw-r--r--   0 ralf      (1000) priv      (1011)      302 2022-03-15 09:28:59.592873 rsclib-0.64/test_ipt2.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 13:53:12.856679 rsclib-0.65/
+-rw-r--r--   0 ralf      (1000) priv      (1011)      123 2014-04-17 17:42:41.000000 rsclib-0.65/MANIFEST.in
+-rw-r--r--   0 ralf      (1000) priv      (1011)    26783 2023-07-23 13:53:12.856679 rsclib-0.65/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)    36068 2023-07-23 13:52:01.000000 rsclib-0.65/README.html
+-rw-r--r--   0 ralf      (1000) priv      (1011)    25374 2023-07-23 13:43:00.000000 rsclib-0.65/README.rst
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2711 2023-07-23 13:30:20.000000 rsclib-0.65/pyproject.toml
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 13:53:12.828678 rsclib-0.65/rsclib/
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2729 2022-03-15 09:28:59.000000 rsclib-0.65/rsclib/Config_File.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    35410 2022-03-15 09:28:59.000000 rsclib-0.65/rsclib/IP_Address.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2983 2021-07-20 11:13:43.000000 rsclib-0.65/rsclib/Math.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    13272 2021-07-20 11:13:52.000000 rsclib-0.65/rsclib/PDF_Signature.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     4232 2022-03-15 09:28:59.000000 rsclib-0.65/rsclib/PM_Value.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     5976 2020-01-14 20:33:59.000000 rsclib-0.65/rsclib/Phone.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     6545 2017-08-06 17:21:57.000000 rsclib-0.65/rsclib/Rational.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     4470 2017-07-24 22:10:03.000000 rsclib-0.65/rsclib/TeX_CSV_Writer.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)       15 2023-07-23 13:52:01.000000 rsclib-0.65/rsclib/Version.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)       37 2014-04-12 19:15:07.000000 rsclib-0.65/rsclib/__init__.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    42872 2020-03-03 14:08:03.000000 rsclib-0.65/rsclib/ast_call.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     6509 2022-03-15 09:28:59.000000 rsclib-0.65/rsclib/ast_cdr.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     4787 2023-07-23 13:51:04.000000 rsclib-0.65/rsclib/ast_probe.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1281 2019-12-01 20:44:56.000000 rsclib-0.65/rsclib/autosuper.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1523 2020-01-14 20:33:59.000000 rsclib-0.65/rsclib/base_pickler.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    11164 2020-01-14 20:33:59.000000 rsclib-0.65/rsclib/bero.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1731 2021-07-20 12:27:41.000000 rsclib-0.65/rsclib/capacitance.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     9080 2020-01-14 20:33:59.000000 rsclib-0.65/rsclib/crm.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    22717 2023-03-28 14:44:39.000000 rsclib-0.65/rsclib/execute.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2291 2017-07-24 21:21:50.000000 rsclib-0.65/rsclib/grepmime.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     4998 2023-07-23 13:50:59.000000 rsclib-0.65/rsclib/hexdump.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    18943 2018-08-16 20:18:30.000000 rsclib-0.65/rsclib/inductance.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    30587 2022-03-15 09:28:59.000000 rsclib-0.65/rsclib/isdn.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     6244 2017-07-24 21:22:14.000000 rsclib-0.65/rsclib/iter_recipes.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1778 2017-07-24 22:50:36.000000 rsclib-0.65/rsclib/lc_resonator.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    20872 2022-03-15 09:28:59.000000 rsclib-0.65/rsclib/nmap.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    17926 2020-01-14 20:33:59.000000 rsclib-0.65/rsclib/ocf.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     3050 2022-03-30 12:40:10.000000 rsclib-0.65/rsclib/pycompat.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    50686 2021-10-04 16:00:23.000000 rsclib-0.65/rsclib/sqlparser.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     7208 2022-03-15 09:28:59.000000 rsclib-0.65/rsclib/stateparser.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2086 2017-07-24 22:10:49.000000 rsclib-0.65/rsclib/timeout.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    31827 2022-03-15 09:28:59.000000 rsclib-0.65/rsclib/trafficshape.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 13:53:12.848678 rsclib-0.65/rsclib.egg-info/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    26783 2023-07-23 13:53:12.000000 rsclib-0.65/rsclib.egg-info/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)      880 2023-07-23 13:53:12.000000 rsclib-0.65/rsclib.egg-info/SOURCES.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-07-23 13:53:12.000000 rsclib-0.65/rsclib.egg-info/dependency_links.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)      153 2023-07-23 13:53:12.000000 rsclib-0.65/rsclib.egg-info/entry_points.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        7 2023-07-23 13:53:12.000000 rsclib-0.65/rsclib.egg-info/top_level.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-07-23 13:53:12.856679 rsclib-0.65/setup.cfg
+-rw-r--r--   0 ralf      (1000) priv      (1011)     3101 2023-07-23 13:44:29.000000 rsclib-0.65/setup.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)      573 2022-03-15 09:28:59.000000 rsclib-0.65/test2_exec.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)      700 2022-03-15 09:28:59.000000 rsclib-0.65/test_exec.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)      261 2022-03-15 09:28:59.000000 rsclib-0.65/test_ipt.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)      302 2022-03-15 09:28:59.000000 rsclib-0.65/test_ipt2.py
```

### Comparing `rsclib-0.64/README.html` & `rsclib-0.65/README.html`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 <?xml version="1.0" encoding="utf-8" ?>
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
 <head>
 <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
-<meta name="generator" content="Docutils 0.16: http://docutils.sourceforge.net/" />
+<meta name="generator" content="Docutils 0.19: https://docutils.sourceforge.io/" />
 <title>rsclib: Utility Routines</title>
 <meta name="author" content="Ralf Schlatterbeck &lt;rsc&#64;runtux.com&gt;" />
 <style type="text/css">
 
 /*
 :Author: David Goodger
 :Contact: goodger@users.sourceforge.net
@@ -390,45 +390,57 @@
 <pre class="literal-block">
 python setup.py install --prefix=/usr/local
 </pre>
 <p>Alternatively get it from pypi and/or install via pip.</p>
 </div>
 <div class="section" id="changes">
 <h1>Changes</h1>
-<dl class="docutils">
-<dt>Version 0.64: Small execute.Log updates</dt>
-<dd><ul class="first last simple">
+<p>Version 0.65: Use pyproject.toml</p>
+<blockquote>
+<ul class="simple">
+<li>Use new-style packaging with pyproject.toml, old-style setup.py is
+still available</li>
+<li>Use console script entry points instead of explicit scripts in
+directory bin</li>
+</ul>
+</blockquote>
+<p>Version 0.64: Small execute.Log updates</p>
+<blockquote>
+<ul class="simple">
 <li>Add add_stderr_handler method to also log to stderr</li>
 </ul>
-</dd>
-<dt>Version 0.63: Python3 fixes</dt>
-<dd><ul class="first last simple">
+</blockquote>
+<p>Version 0.63: Python3 fixes</p>
+<blockquote>
+<ul class="simple">
 <li>Fix bytes_ord to also deal with a bytes object in python3</li>
 </ul>
-</dd>
-<dt>Version 0.62: Python3 fixes</dt>
-<dd><ul class="first last simple">
+</blockquote>
+<p>Version 0.62: Python3 fixes</p>
+<blockquote>
+<ul class="simple">
 <li>More Python3 fixes</li>
 <li>Update of stateparser</li>
 <li>hexdump/unhexdump</li>
 </ul>
-</dd>
-<dt>Version 0.61: sqlparser</dt>
-<dd><ul class="first last simple">
+</blockquote>
+<p>Version 0.61: sqlparser</p>
+<blockquote>
+<ul class="simple">
 <li>Allow filtering during reading of sql dump</li>
 </ul>
-</dd>
-<dt>Version 0.60: Python3 fixes</dt>
-<dd><ul class="first last simple">
+</blockquote>
+<p>Version 0.60: Python3 fixes</p>
+<blockquote>
+<ul class="simple">
 <li>hexdump</li>
 <li>xrange</li>
 <li>compatibility for bytes iterator</li>
 </ul>
-</dd>
-</dl>
+</blockquote>
 <p>Version 0.59: sqlparser</p>
 <blockquote>
 <ul class="simple">
 <li>Support older postgresql versions, tested 9.6</li>
 </ul>
 </blockquote>
 <p>Version 0.58: sqlparser</p>
```

### Comparing `rsclib-0.64/README.rst` & `rsclib-0.65/README.rst`

 * *Files 1% similar despite different names*

```diff
@@ -110,29 +110,41 @@
 
 Alternatively get it from pypi and/or install via pip.
 
 
 Changes
 -------
 
+Version 0.65: Use pyproject.toml
+
+    - Use new-style packaging with pyproject.toml, old-style setup.py is
+      still available
+    - Use console script entry points instead of explicit scripts in
+      directory bin
+
 Version 0.64: Small execute.Log updates
+
     - Add add_stderr_handler method to also log to stderr
 
 Version 0.63: Python3 fixes
+
     - Fix bytes_ord to also deal with a bytes object in python3
 
 Version 0.62: Python3 fixes
+
     - More Python3 fixes
     - Update of stateparser
     - hexdump/unhexdump
 
 Version 0.61: sqlparser
+
     - Allow filtering during reading of sql dump
 
 Version 0.60: Python3 fixes
+
     - hexdump
     - xrange
     - compatibility for bytes iterator
 
 Version 0.59: sqlparser
 
     - Support older postgresql versions, tested 9.6
```

### Comparing `rsclib-0.64/rsclib/Config_File.py` & `rsclib-0.65/rsclib/Config_File.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/IP_Address.py` & `rsclib-0.65/rsclib/IP_Address.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/Math.py` & `rsclib-0.65/rsclib/Math.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/PDF_Signature.py` & `rsclib-0.65/rsclib/PDF_Signature.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/PM_Value.py` & `rsclib-0.65/rsclib/PM_Value.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/Phone.py` & `rsclib-0.65/rsclib/Phone.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/Rational.py` & `rsclib-0.65/rsclib/Rational.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/TeX_CSV_Writer.py` & `rsclib-0.65/rsclib/TeX_CSV_Writer.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/ast_call.py` & `rsclib-0.65/rsclib/ast_call.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/ast_cdr.py` & `rsclib-0.65/rsclib/ast_cdr.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/ast_probe.py` & `rsclib-0.65/rsclib/ast_probe.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,9 @@
 #!/usr/bin/python
-# -*- coding: iso-8859-1 -*-
-# Copyright (C) 2015-17 Dr. Ralf Schlatterbeck Open Source Consulting.
+# Copyright (C) 2015-23 Dr. Ralf Schlatterbeck Open Source Consulting.
 # Reichergasse 131, A-3411 Weidling.
 # Web: http://www.runtux.com Email: office@runtux.com
 # All rights reserved
 # ****************************************************************************
 # This library is free software; you can redistribute it and/or modify
 # it under the terms of the GNU Library General Public License as
 # published by the Free Software Foundation; either version 2 of the
@@ -17,110 +16,130 @@
 #
 # You should have received a copy of the GNU Library General Public
 # License along with this program; if not, write to the Free Software
 # Foundation, Inc., 675 Mass Ave, Cambridge, MA 02139, USA.
 # ****************************************************************************
 
 from __future__         import print_function
+import sys
 from time               import sleep
 from asterisk.manager   import Manager, ManagerSocketException
 from rsclib.execute     import Log
 from rsclib.Config_File import Config_File
 
-class Config (Config_File) :
+class Config (Config_File):
 
-    def __init__ (self, config = 'ast_probe', path = '/etc/ast_probe') :
+    def __init__ (self, config = 'ast_probe', path = '/etc/ast_probe'):
         self.__super.__init__ \
             ( path, config
             , ASTERISK_HOST         = 'localhost'
             , ASTERISK_MGR_ACCOUNT  = 'user'
             , ASTERISK_MGR_PASSWORD = 'secret'
             )
     # end def __init__
 
 # end class Config
 
-class Asterisk_Probe (Log) :
+class Asterisk_Probe (Log):
 
     def __init__ \
         ( self
         , config  = 'ast_probe'
         , cfgpath = '/etc/ast_probe'
         , cfg     = None
         , retries = 0
         , ** kw
-        ) :
-        if cfg :
+        ):
+        if cfg:
             self.cfg = cfg
-        else :
+        else:
             self.cfg = cfg = Config (config = config, path = cfgpath)
         self.__super.__init__ (** kw)
-        if 'manager' in kw :
+        if 'manager' in kw:
             self.mgr = mgr = kw ['manager']
-        else :
+        else:
             self.mgr = mgr = Manager ()
-            for r in range (retries + 1) :
-                try :
+            for r in range (retries + 1):
+                try:
                     mgr.connect (cfg.ASTERISK_HOST)
                     break
-                except ManagerSocketException :
-                    if r >= retries :
+                except ManagerSocketException:
+                    if r >= retries:
                         raise
                     sleep (1)
             mgr.login (cfg.ASTERISK_MGR_ACCOUNT, cfg.ASTERISK_MGR_PASSWORD)
     # end def __init__
 
-    def close (self) :
+    def close (self):
         self.mgr.close ()
         self.mgr = None
     # end def close
 
-    def probe_apps (self) :
+    def probe_apps (self):
         mgr = self.mgr
         r = mgr.command ('core show applications')
         d = {}
-        for line in r.data.split ('\n') :
+        for line in r.data.split ('\n'):
             line = line.strip ()
-            try :
+            try:
                 k, v = (x.strip () for x in line.split (':', 1))
-            except ValueError :
+            except ValueError:
                 assert (  not line
                        or line == '--END COMMAND--'
                        or line.startswith ('-=') and line.endswith ('=-')
                        )
                 continue
             d [k] = v
         return d
     # end def probe_apps
 
-    def probe_sip_registry (self) :
+    def probe_sip_registry (self):
         r = self.mgr.command ('sip show registry')
         d = {}
-        for line in r.data.split ('\n') :
+        for line in r.data.split ('\n'):
             data = line.split (None, 5)
-            if len (data) != 6 :
+            if len (data) != 6:
                 assert data == [] or data [1] == 'SIP' or data [0] == '--END'
                 continue
-            if data [0] == 'Host' :
+            if data [0] == 'Host':
                 continue
-            if data [4] == 'Request' and data [5].startswith ('Sent') :
+            if data [4] == 'Request' and data [5].startswith ('Sent'):
                 data [4] = 'Request Sent'
                 data [5] = data [5].split (None, 1) [-1]
             host, port = data [0].split (':', 1)
             d [host] = data [4]
         return d
     # end def probe_sip_registry
 
-    def reload_sip (self) :
+    def reload_sip (self):
         r = self.mgr.command ('sip reload')
         self.log.info ('SIP reload')
     # end def reload_sip
 
 # end class Asterisk_Probe
 
-if __name__ == '__main__' :
+def sip_check ():
+    p = Asterisk_Probe ()
+    r = p.probe_sip_registry ()
+    reload = False
+    for name in sys.argv [1:]:
+        if name not in r:
+            p.log.error ("Host %s not found" % name)
+        elif r [name] == 'Request Sent':
+            p.log.warn ("Host %s: %s" % (name, r [name]))
+        elif r [name] != 'Registered':
+            p.log.error ("Host %s not registered: %s" % (name, r [name]))
+            reload = True
+        else:
+            p.log.debug ("Host %s OK" % name)
+
+    if reload:
+        p.reload_sip ()
+# end def sip_check
+
+if __name__ == '__main__':
     ap = Asterisk_Probe ()
     d = ap.probe_apps ()
-    for k in d :
+    for k in d:
         v = d [k]
         print ("%s: %s" % (k, v))
     ap.close ()
```

### Comparing `rsclib-0.64/rsclib/autosuper.py` & `rsclib-0.65/rsclib/autosuper.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/base_pickler.py` & `rsclib-0.65/rsclib/base_pickler.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/bero.py` & `rsclib-0.65/rsclib/bero.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/capacitance.py` & `rsclib-0.65/rsclib/capacitance.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/crm.py` & `rsclib-0.65/rsclib/crm.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/execute.py` & `rsclib-0.65/rsclib/execute.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/grepmime.py` & `rsclib-0.65/rsclib/grepmime.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/hexdump.py` & `rsclib-0.65/rsclib/hexdump.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 #!/usr/bin/python
-# Copyright (C) 2011-21 Dr. Ralf Schlatterbeck Open Source Consulting.
+# Copyright (C) 2011-23 Dr. Ralf Schlatterbeck Open Source Consulting.
 # Reichergasse 131, A-3411 Weidling.
 # Web: http://www.runtux.com Email: office@runtux.com
 # All rights reserved
 # ****************************************************************************
 # This library is free software; you can redistribute it and/or modify
 # it under the terms of the GNU Library General Public License as
 # published by the Free Software Foundation; either version 2 of the
@@ -18,83 +18,132 @@
 # License along with this program; if not, write to the Free Software
 # Foundation, Inc., 675 Mass Ave, Cambridge, MA 02139, USA.
 # ****************************************************************************
 
 from __future__ import print_function
 import sys
 from rsclib.pycompat import bytes_ord, PY2
+from argparse        import ArgumentParser
 
-def ascii (s) :
-    if not PY2 :
-        if s > 128 :
+def ascii (s):
+    if not PY2:
+        if s > 128:
             return '.'
         s = chr (s)
-    if len (repr (s)) > 3 :
+    if len (repr (s)) > 3:
         return '.'
     return s
 # end def ascii
 
-def hexdump (s, start = 0, show_addr = True, last_addr = True) :
+def hexdump (s, start = 0, show_addr = True, last_addr = True):
     """
     >>> a = b'1234567890abcdefghijklmnopqrstuv'
     >>> print (hexdump (a + b'\\xce\\x02\\xb9\x49', show_addr = False))
     31 32 33 34 35 36 37 38 39 30 61 62 63 64 65 66   1234567890abcdef
     67 68 69 6a 6b 6c 6d 6e 6f 70 71 72 73 74 75 76   ghijklmnopqrstuv
     ce 02 b9 49                                       ...I            
     >>> print (hexdump (a + b'\\xce\\x02\\xb9\x49'))
     00000000  31 32 33 34 35 36 37 38 39 30 61 62 63 64 65 66   1234567890abcdef
     00000010  67 68 69 6a 6b 6c 6d 6e 6f 70 71 72 73 74 75 76   ghijklmnopqrstuv
     00000020  ce 02 b9 49                                       ...I            
     """
     assert isinstance (s, type (b''))
     r = []
-    for x in range (len (s) // 16 + 1) :
+    for x in range (len (s) // 16 + 1):
         slc  = s [x*16:(x+1)*16]
         adr  = '%08x'  % (start + x * 16)
         hex  = '%-48s' % ' '.join \
             ("%02x" % bytes_ord (k) for k in slc)
         char = '%-16s' % ''.join (ascii (k) for k in slc)
         vars = (adr, hex, char)
-        if not show_addr :
+        if not show_addr:
             vars = (hex, char)
-        if last_addr or slc :
+        if last_addr or slc:
             r.append ('  '.join (vars))
     return '\n'.join (r)
 # end def hexdump
 
-def unhexdump (iterable, file = None) :
+def unhexdump (iterable, file = None):
     """ Convert a hex-dump to binary
     """
     bin = []
     end = False
-    for line in iterable :
+    for line in iterable:
         line = line.strip ()
-        if not line :
+        if not line:
             continue
-        if end :
+        if end:
             raise ValueError ("Unknown hexdump format")
         x = line.split ('  ', 2)
-        if len (x) == 1 :
+        if len (x) == 1:
             h = x [0]
-        else :
+        else:
             h = x [1]
             assert len (x [0]) <= 8
         # Probably last line with only an address
-        if ' ' not in h and len (x) == 1 and len (h) > 2 :
+        if ' ' not in h and len (x) == 1 and len (h) > 2:
             end = True
             continue
         h = h.strip ().split (' ')
-        if len (h [0]) > 2 :
+        if len (h [0]) > 2:
             h = h [1:]
-        if sys.version_info [0] < 3 :
-            method = lambda x : b''.join (chr (c) for c in x)
-        else :
+        if sys.version_info [0] < 3:
+            method = lambda x: b''.join (chr (c) for c in x)
+        else:
             method = bytes
-        if file :
+        if file:
             file.write (method ((int (k, 16)) for k in h))
-        else :
+        else:
             bin.append (method ((int (k, 16)) for k in h))
-    if file :
+    if file:
         file.flush ()
         return None
     return b''.join (bin)
 # end def unhexdump
+
+def hexdump_f (f, bs = 512):
+    adr = 0
+    while 1:
+        b = f.read (bs)
+        if not b:
+            break
+        print (hexdump (b, adr, last_addr = False))
+        adr += bs
+# end def hexdump_f
+
+def hexdump_cmd ():
+    if len (sys.argv) > 1:
+        for fn in sys.argv [1:]:
+            if len (sys.argv) > 2:
+                print ("FILE: %s" % fn)
+            with open (fn, 'rb') as f:
+                hexdump_f (f)
+    else:
+        hexdump_f (sys.stdin.buffer)
+# end def hexdump_cmd
+
+def unhexdump_cmd ():
+    cmd = ArgumentParser ()
+    cmd.add_argument \
+        ( 'input_file'
+        , help  = "Input hexdump file to convert to binary"
+        , nargs = '?'
+        )
+    cmd.add_argument \
+        ( '-o', '--output-file'
+        , help  = "Output file for writing binary"
+        )
+    args = cmd.parse_args ()
+    if args.output_file:
+        with open (args.output_file, 'wb') as f_out:
+            if args.input_file:
+                with open (args.input_file, 'r') as f_in:
+                    unhexdump (f_in, f_out)
+            else:
+                unhexdump (sys.stdin, f_out)
+    else:
+        if args.input_file:
+            with open (args.input_file, 'r') as f_in:
+                unhexdump (f_in, sys.stdout.buffer)
+        else:
+            unhexdump (sys.stdin, sys.stdout.buffer)
+# end def unhexdump_cmd
```

### Comparing `rsclib-0.64/rsclib/inductance.py` & `rsclib-0.65/rsclib/inductance.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/isdn.py` & `rsclib-0.65/rsclib/isdn.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/iter_recipes.py` & `rsclib-0.65/rsclib/iter_recipes.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/lc_resonator.py` & `rsclib-0.65/rsclib/lc_resonator.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/nmap.py` & `rsclib-0.65/rsclib/nmap.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/ocf.py` & `rsclib-0.65/rsclib/ocf.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/pycompat.py` & `rsclib-0.65/rsclib/pycompat.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/sqlparser.py` & `rsclib-0.65/rsclib/sqlparser.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/stateparser.py` & `rsclib-0.65/rsclib/stateparser.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/timeout.py` & `rsclib-0.65/rsclib/timeout.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/rsclib/trafficshape.py` & `rsclib-0.65/rsclib/trafficshape.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/setup.py` & `rsclib-0.65/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -45,18 +45,21 @@
     , long_description = ''.join (description)
     , license          = license
     , author           = "Ralf Schlatterbeck"
     , author_email     = "rsc@runtux.com"
     , packages         = ['rsclib']
     , platforms        = 'Any'
     , url              = "http://rsclib.sourceforge.net/"
-    , scripts          = [ 'bin/ast_sip_check'
-                         , 'bin/rsclib-hexdump'
-                         , 'bin/rsclib-unhexdump'
-                         ]
+    , entry_points     = dict
+        ( console_scripts =
+            [ "ast_sip_check=rsclib.ast_probe:sip_check"
+            , "rsclib-hexdump=rsclib.hexdump:hexdump_cmd"
+            , "rsclib-unhexdump=rsclib.hexdump:unhexdump_cmd"
+            ]
+        )
     , python_requires  = rq
     , download_url     = \
         "%(download)s/%(VERSION)s/rsclib-%(VERSION)s.tar.gz" % locals ()
     , classifiers      = \
         [ 'Development Status :: 5 - Production/Stable'
         , 'License :: OSI Approved :: ' + license
         , 'Operating System :: OS Independent'
```

### Comparing `rsclib-0.64/test2_exec.py` & `rsclib-0.65/test2_exec.py`

 * *Files identical despite different names*

### Comparing `rsclib-0.64/test_exec.py` & `rsclib-0.65/test_exec.py`

 * *Files identical despite different names*

