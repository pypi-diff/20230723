# Comparing `tmp/hamradio-0.4.tar.gz` & `tmp/hamradio-0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hamradio-0.4.tar", last modified: Sat May 14 10:22:22 2022, max compression
+gzip compressed data, was "hamradio-0.5.tar", last modified: Sun Jul 23 13:00:47 2023, max compression
```

## Comparing `hamradio-0.4.tar` & `hamradio-0.5.tar`

### file list

```diff
@@ -1,26 +1,33 @@
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2022-05-14 10:22:22.648599 hamradio-0.4/
--rw-r--r--   0 ralf      (1000) priv      (1011)     5306 2022-05-14 10:22:22.652598 hamradio-0.4/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)    10380 2022-05-14 10:20:46.860621 hamradio-0.4/README.html
--rw-r--r--   0 ralf      (1000) priv      (1011)     3740 2022-05-14 10:20:06.996631 hamradio-0.4/README.rst
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2022-05-14 10:22:22.636598 hamradio-0.4/bin/
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       60 2021-10-07 14:35:44.989302 hamradio-0.4/bin/callsign_lookup
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       65 2021-10-07 14:35:48.345301 hamradio-0.4/bin/qsl-export
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       67 2021-10-07 14:35:51.181300 hamradio-0.4/bin/qso-import
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2022-05-14 10:22:22.648599 hamradio-0.4/hamradio/
--rw-r--r--   0 ralf      (1000) priv      (1011)       14 2022-05-14 10:20:46.864621 hamradio-0.4/hamradio/Version.py
--rw-r--r--   0 ralf      (1000) priv      (1011)        0 2019-08-25 09:17:17.331729 hamradio-0.4/hamradio/__init__.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    16639 2021-09-13 11:46:12.078611 hamradio-0.4/hamradio/adif.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     5039 2021-09-13 11:46:12.078611 hamradio-0.4/hamradio/bandplan.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    11647 2021-10-07 20:25:54.675919 hamradio-0.4/hamradio/cty.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2022-05-14 10:22:22.648599 hamradio-0.4/hamradio/data/
--rw-r--r--   0 ralf      (1000) priv      (1011)    46469 2019-06-10 12:33:36.000000 hamradio-0.4/hamradio/data/2019_Current_Deleted(3).txt
--rw-r--r--   0 ralf      (1000) priv      (1011)   285503 2021-09-13 19:00:21.330684 hamradio-0.4/hamradio/data/cty.dat
--rw-r--r--   0 ralf      (1000) priv      (1011)    91744 2021-09-13 18:58:38.610741 hamradio-0.4/hamradio/data/wae-country-list.html
--rw-r--r--   0 ralf      (1000) priv      (1011)    41629 2021-10-15 10:23:34.296818 hamradio-0.4/hamradio/dbimport.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    12566 2021-09-13 19:42:09.121728 hamradio-0.4/hamradio/dxcc.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     9031 2021-10-07 14:35:00.825314 hamradio-0.4/hamradio/eqsl.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     4498 2021-10-07 14:35:13.901311 hamradio-0.4/hamradio/lotw.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     8782 2021-10-07 14:35:25.129307 hamradio-0.4/hamradio/qslcard.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     5887 2021-09-13 11:46:12.142612 hamradio-0.4/hamradio/qth.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     4935 2021-09-17 10:30:48.975572 hamradio-0.4/hamradio/requester.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     3343 2022-05-14 10:15:59.756689 hamradio-0.4/setup.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 13:00:47.968678 hamradio-0.5/
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1555 2023-07-23 09:55:31.000000 hamradio-0.5/LICENSE
+-rw-r--r--   0 ralf      (1000) priv      (1011)      164 2021-10-07 14:37:54.000000 hamradio-0.5/MANIFEST.in
+-rw-r--r--   0 ralf      (1000) priv      (1011)     4704 2023-07-23 13:00:47.968678 hamradio-0.5/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)    10380 2023-07-23 12:58:27.000000 hamradio-0.5/README.html
+-rw-r--r--   0 ralf      (1000) priv      (1011)     3740 2022-05-14 10:20:06.000000 hamradio-0.5/README.rst
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 13:00:47.900678 hamradio-0.5/hamradio/
+-rw-r--r--   0 ralf      (1000) priv      (1011)       14 2023-07-23 12:58:27.000000 hamradio-0.5/hamradio/Version.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)        0 2019-08-25 09:17:17.000000 hamradio-0.5/hamradio/__init__.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    16639 2021-09-13 11:46:12.000000 hamradio-0.5/hamradio/adif.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     5039 2021-09-13 11:46:12.000000 hamradio-0.5/hamradio/bandplan.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    11647 2021-10-07 20:25:54.000000 hamradio-0.5/hamradio/cty.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 13:00:47.956678 hamradio-0.5/hamradio/data/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    46469 2019-06-10 12:33:36.000000 hamradio-0.5/hamradio/data/2019_Current_Deleted(3).txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)   285503 2021-09-13 19:00:21.000000 hamradio-0.5/hamradio/data/cty.dat
+-rw-r--r--   0 ralf      (1000) priv      (1011)    91744 2021-09-13 18:58:38.000000 hamradio-0.5/hamradio/data/wae-country-list.html
+-rw-r--r--   0 ralf      (1000) priv      (1011)    42049 2023-06-24 07:18:31.000000 hamradio-0.5/hamradio/dbimport.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    12566 2021-09-13 19:42:09.000000 hamradio-0.5/hamradio/dxcc.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     9031 2021-10-07 14:35:00.000000 hamradio-0.5/hamradio/eqsl.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     4498 2021-10-07 14:35:13.000000 hamradio-0.5/hamradio/lotw.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     8782 2021-10-07 14:35:25.000000 hamradio-0.5/hamradio/qslcard.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     5887 2021-09-13 11:46:12.000000 hamradio-0.5/hamradio/qth.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     5038 2022-06-07 07:35:26.000000 hamradio-0.5/hamradio/requester.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 13:00:47.920678 hamradio-0.5/hamradio.egg-info/
+-rw-r--r--   0 ralf      (1000) priv      (1011)     4704 2023-07-23 13:00:47.000000 hamradio-0.5/hamradio.egg-info/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)      585 2023-07-23 13:00:47.000000 hamradio-0.5/hamradio.egg-info/SOURCES.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-07-23 13:00:47.000000 hamradio-0.5/hamradio.egg-info/dependency_links.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)      126 2023-07-23 13:00:47.000000 hamradio-0.5/hamradio.egg-info/entry_points.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       20 2023-07-23 13:00:47.000000 hamradio-0.5/hamradio.egg-info/requires.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       14 2023-07-23 13:00:47.000000 hamradio-0.5/hamradio.egg-info/top_level.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)     3002 2023-07-23 12:56:36.000000 hamradio-0.5/pyproject.toml
+-rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-07-23 13:00:47.968678 hamradio-0.5/setup.cfg
+-rw-r--r--   0 ralf      (1000) priv      (1011)     3404 2023-07-23 10:32:53.000000 hamradio-0.5/setup.py
```

### Comparing `hamradio-0.4/PKG-INFO` & `hamradio-0.5/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,109 +1,111 @@
-Metadata-Version: 1.1
+Metadata-Version: 2.1
 Name: hamradio
-Version: 0.4
+Version: 0.5
 Summary: Utilities for Ham radio
 Home-page: https://github.com/schlatterbeck/hamradio
 Author: Ralf Schlatterbeck
-Author-email: rsc@runtux.com
+Author-email: Ralf Schlatterbeck <rsc@runtux.com>
 License: BSD License
-Description: Ham-Radio scripts
-        =================
-        
-        :Author: Ralf Schlatterbeck <rsc@runtux.com>
-        
-        .. |--| unicode:: U+2013   .. en dash
-        
-        Note that the binaries currently installed with the package work only in
-        conjunction with my logging database based on Roundup_.
-        
-        The software in the modules of this python package centers around
-        handling of QSO logging data, retrieval of electronic QSLs from various
-        electronic QSL services (currently Logbook of the World LOTW_ and eQSL_)
-        and interfacing to my logging database written with the bugtracking
-        framework Roundup_. The logging database is part of my `time-track-tool`_
-        several packages that build on Roundup_, among them a time tracking tool
-        and a QSO logger.
-        
-        .. _Roundup: https://sourceforge.net/projects/roundup/
-        .. _eQSL: https://www.eqsl.cc/
-        .. _LOTW: https://lotw.arrl.org/
-        .. _`time-track-tool`: https://github.com/time-track-tool/time-track-tool
-        
-        The adif module is used to parse ADIF files.
-        Basic usage is at the end of the file, it can be called to do a
-        round-trip of an ADIF file (reading it in and writing it out).
-        
-        The bandplan module implements a definition of the ham radio bands and
-        corresponding frequencies for a country. Currently only Austria is
-        implemented, it should be easy to add other countries. I'm mainly using
-        it for looking up the corresponding band for a given frequency (e.g.
-        when receiving data from WSJTX_ which includes only a frequency not the
-        band).
-        
-        .. _WSJTX: https://physics.princeton.edu/pulsar/k1jt/wsjtx.html
-        
-        The dbimport module is used for communicating with my time-track-tool_
-        logging database via its `REST API`_. It makes use of the requester
-        module which factors out some of the common `REST API`_ calls.
-        
-        .. _`REST API`: https://roundup.sourceforge.io/docs/rest.html
-        
-        The dxcc module is used to parse the `official DXCC list`_ from the ARRL
-        homepage and do basic callsign lookups via the prefix list given in that
-        document. Note that the prefix list often does not identify the DXCC
-        entity unambiguously or even gets the DXCC entity wrong in some cases.
-        
-        .. _`official DXCC list`:
-            http://www.arrl.org/files/file/DXCC/2019_Current_Deleted(3).txt
-        
-        The cty module is used to extract information from the well known
-        ``CTY.DAT`` `country database`_ by Jim Reisert, AD1C. This database is
-        much better at matching callsign prefixes to DXCC country, CQ-Zone and
-        ITU-Zone information than the information in the ARRL list used by the
-        dxcc module above. The module can be called with a set of callsigns to
-        look up, the code at the end of the module should give you an idea on
-        how to use it. Currently only DXCC lookup is implemented, CQ-Zone and
-        ITU-Zone info may follow at some point.
-        
-        .. _`country database`: https://www.country-files.com
-        
-        The eqsl and lotw modules are used for retrieving QSO and QSL log
-        information from Logbook of the World LOTW_ and eQSL_. Note that the
-        eqsl package also supports retrieving the QSL "cards". You should have a
-        `silver membership with eQSL`_ for using that feature. You should get a
-        quick idea how to use these modules from looking into the dbimport
-        module. Note that both, eqsl and lotw use the requester module.
-        
-        .. _`silver membership with eQSL`: http://www.eqsl.cc/qslcard/GeteQSL.txt
-        
-        The qth module implements conversion from GPS coordinates to Maidenhead
-        locator. It has a doctest in the Maidenhead_Locator class that should
-        give you an idea on how to use it. It does support extended locators
-        beyond length 6 used by some VHF groups.
-        
-        Changes
-        -------
-        
-        Version 0.4: Fix setup.py install_requires
-        
-        Version 0.2-0.3: Updates to documentation and setup
-        
-        Version 0.1: Initial release
-        
-        Note that this project is quite old |--| I'm using it for myself so far
-        and the first release just now should not scare you too much.
-        
+Project-URL: Homepage, https://github.com/schlatterbeck/hamradio
+Project-URL: Bug Tracker, https://github.com/schlatterbeck/hamradio/issues
 Platform: Any
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Intended Audience :: Developers
-Classifier: Programming Language :: Python :: 2
-Classifier: Programming Language :: Python :: 2.7
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.5
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Python: >=3.6
+Description-Content-Type: text/x-rst
+License-File: LICENSE
+
+Ham-Radio scripts
+=================
+
+:Author: Ralf Schlatterbeck <rsc@runtux.com>
+
+.. |--| unicode:: U+2013   .. en dash
+
+Note that the binaries currently installed with the package work only in
+conjunction with my logging database based on Roundup_.
+
+The software in the modules of this python package centers around
+handling of QSO logging data, retrieval of electronic QSLs from various
+electronic QSL services (currently Logbook of the World LOTW_ and eQSL_)
+and interfacing to my logging database written with the bugtracking
+framework Roundup_. The logging database is part of my `time-track-tool`_
+several packages that build on Roundup_, among them a time tracking tool
+and a QSO logger.
+
+.. _Roundup: https://sourceforge.net/projects/roundup/
+.. _eQSL: https://www.eqsl.cc/
+.. _LOTW: https://lotw.arrl.org/
+.. _`time-track-tool`: https://github.com/time-track-tool/time-track-tool
+
+The adif module is used to parse ADIF files.
+Basic usage is at the end of the file, it can be called to do a
+round-trip of an ADIF file (reading it in and writing it out).
+
+The bandplan module implements a definition of the ham radio bands and
+corresponding frequencies for a country. Currently only Austria is
+implemented, it should be easy to add other countries. I'm mainly using
+it for looking up the corresponding band for a given frequency (e.g.
+when receiving data from WSJTX_ which includes only a frequency not the
+band).
+
+.. _WSJTX: https://physics.princeton.edu/pulsar/k1jt/wsjtx.html
+
+The dbimport module is used for communicating with my time-track-tool_
+logging database via its `REST API`_. It makes use of the requester
+module which factors out some of the common `REST API`_ calls.
+
+.. _`REST API`: https://roundup.sourceforge.io/docs/rest.html
+
+The dxcc module is used to parse the `official DXCC list`_ from the ARRL
+homepage and do basic callsign lookups via the prefix list given in that
+document. Note that the prefix list often does not identify the DXCC
+entity unambiguously or even gets the DXCC entity wrong in some cases.
+
+.. _`official DXCC list`:
+    http://www.arrl.org/files/file/DXCC/2019_Current_Deleted(3).txt
+
+The cty module is used to extract information from the well known
+``CTY.DAT`` `country database`_ by Jim Reisert, AD1C. This database is
+much better at matching callsign prefixes to DXCC country, CQ-Zone and
+ITU-Zone information than the information in the ARRL list used by the
+dxcc module above. The module can be called with a set of callsigns to
+look up, the code at the end of the module should give you an idea on
+how to use it. Currently only DXCC lookup is implemented, CQ-Zone and
+ITU-Zone info may follow at some point.
+
+.. _`country database`: https://www.country-files.com
+
+The eqsl and lotw modules are used for retrieving QSO and QSL log
+information from Logbook of the World LOTW_ and eQSL_. Note that the
+eqsl package also supports retrieving the QSL "cards". You should have a
+`silver membership with eQSL`_ for using that feature. You should get a
+quick idea how to use these modules from looking into the dbimport
+module. Note that both, eqsl and lotw use the requester module.
+
+.. _`silver membership with eQSL`: http://www.eqsl.cc/qslcard/GeteQSL.txt
+
+The qth module implements conversion from GPS coordinates to Maidenhead
+locator. It has a doctest in the Maidenhead_Locator class that should
+give you an idea on how to use it. It does support extended locators
+beyond length 6 used by some VHF groups.
+
+Changes
+-------
+
+Version 0.4: Fix setup.py install_requires
+
+Version 0.2-0.3: Updates to documentation and setup
+
+Version 0.1: Initial release
+
+Note that this project is quite old |--| I'm using it for myself so far
+and the first release just now should not scare you too much.
```

### Comparing `hamradio-0.4/README.html` & `hamradio-0.5/README.html`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 <?xml version="1.0" encoding="utf-8" ?>
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
 <head>
 <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
-<meta name="generator" content="Docutils 0.16: http://docutils.sourceforge.net/" />
+<meta name="generator" content="Docutils 0.19: https://docutils.sourceforge.io/" />
 <title>Ham-Radio scripts</title>
 <meta name="author" content="Ralf Schlatterbeck &lt;rsc&#64;runtux.com&gt;" />
 <style type="text/css">
 
 /*
 :Author: David Goodger
 :Contact: goodger@users.sourceforge.net
```

### Comparing `hamradio-0.4/README.rst` & `hamradio-0.5/README.rst`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/adif.py` & `hamradio-0.5/hamradio/adif.py`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/bandplan.py` & `hamradio-0.5/hamradio/bandplan.py`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/cty.py` & `hamradio-0.5/hamradio/cty.py`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/data/2019_Current_Deleted(3).txt` & `hamradio-0.5/hamradio/data/2019_Current_Deleted(3).txt`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/data/cty.dat` & `hamradio-0.5/hamradio/data/cty.dat`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/data/wae-country-list.html` & `hamradio-0.5/hamradio/data/wae-country-list.html`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/dbimport.py` & `hamradio-0.5/hamradio/dbimport.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 #!/usr/bin/python
-# Copyright (C) 2019-21 Dr. Ralf Schlatterbeck Open Source Consulting.
+# Copyright (C) 2019-22 Dr. Ralf Schlatterbeck Open Source Consulting.
 # Reichergasse 131, A-3411 Weidling.
 # Web: http://www.runtux.com Email: office@runtux.com
 # ****************************************************************************
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are
 # met:
 #
@@ -748,15 +748,15 @@
                 if not self.args.dry_run :
                     d = dict (date_recv = rdate)
                     self.au.put \
                         ('qsl/%s' % qsl ['id'], json = d, etag = q ['@etag'])
             elif cmpd and qsl ['date_recv'][:10] != rdate [:10] :
                 # We only compare the date, not the time
                 # (time is always empty in LOTW)
-                self.notice \
+                self.info \
                     ( "QSL receive time not matching: %s %s %s vs %s"
                     % (date, a.call, qsl ['date_sent'], a.get_qsl_rdate ())
                     )
             qso  = self.au.get ('qso/%s' % qsl ['qso']['id'])
             qso  = qso ['data']
             etag = qso ['@etag']
             q_id = qso ['id']
@@ -935,30 +935,39 @@
 
 # end class DB_Importer
 
 def main () :
     methods = [x [3:] for x in DB_Importer.__dict__ if x.startswith ('do_')]
     qsl_types = ['LOTW', 'eQSL']
     default_url = os.environ.get ('WBF_DBURL', 'http://bee.priv.zoo:8080/qso/')
+    antenna_defaults = \
+        [ '20m:Magnetic Loop D=88cm'
+        , '17m:Magnetic Loop D=88cm'
+        , '40m:Magnetic Loop D=3.5m'
+        , '30m:Magnetic Loop D=1.9m'
+        , '15m:Magnetic Loop D=57cm'
+        , '12m:Magnetic Loop D=57cm'
+        , '10m:Magnetic Loop D=57cm'
+        ]
+    ant = os.environ.get ('WBF_ANTENNA', '')
+    if ant:
+        ant = [x.strip () for x in ant.split (',', 1)]
+        # Since we're appending to the end these will overwrite existing
+        # defaults
+        antenna_defaults.extend (ant)
     cmd = ArgumentParser ()
     cmd.add_argument \
         ( "command"
         , help    = "Command to execute, allowed: %s" % ', '.join (methods)
         )
     cmd.add_argument \
         ( "adiffile"
         , help    = "ADIF file to import"
         , nargs   = '?'
         )
-    antenna_defaults = \
-        [ '20m:Magnetic Loop D=88cm'
-        , '17m:Magnetic Loop D=88cm'
-        , '40m:Magnetic Loop D=3.5m'
-        , '15m:Magnetic Loop D=57cm'
-        ]
     cmd.add_argument \
         ( "-a", "--antenna"
         , help    = "Antenna to use for band, colon separated "
                     "band:antenna, later values override earlier values, "
                     "default=%(default)s"
         , action  = 'append'
         , default = antenna_defaults
@@ -992,15 +1001,15 @@
     cmd.add_argument \
         ( "-e", "--encoding"
         , help    = "Encoding of ADIF file, default=%(default)s"
         , default = 'utf-8'
         )
     cmd.add_argument \
         ( "-E", "--eqsl-username"
-        , help    = "eQSL Username"
+        , help    = 'eQSL Username, default="%(default)s"'
         , default = 'oe3rsu'
         )
     cmd.add_argument \
         ( "--eqsl-password"
         , help    = "eQSL Password, better use .netrc"
         )
     cmd.add_argument \
@@ -1011,15 +1020,15 @@
     cmd.add_argument \
         ( "--listfile"
         , help    = "File listing QSL records missing in DB"
                     " needed for export_adif_from_list command"
         )
     cmd.add_argument \
         ( "-L", "--lotw-username"
-        , help    = "LOTW Username"
+        , help    = 'LOTW Username, default="%(default)s"'
         , default = 'oe3rsu'
         )
     cmd.add_argument \
         ( "--lotw-password"
         , help    = "LOTW Password, better use .netrc"
         )
     cmd.add_argument \
@@ -1039,15 +1048,15 @@
     cmd.add_argument \
         ( "-U", "--url"
         , help    = "URL of tracker (without rest path) default: %(default)s"
         , default = default_url
         )
     cmd.add_argument \
         ( "-u", "--username"
-        , help    = "Username of hamlog database"
+        , help    = 'Username of hamlog database, default="%(default)s"'
         , default = 'ralf'
         )
     cmd.add_argument \
         ( "-v", "--verbose"
         , help    = "Verbose output"
         , action  = 'store_true'
         )
```

### Comparing `hamradio-0.4/hamradio/dxcc.py` & `hamradio-0.5/hamradio/dxcc.py`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/eqsl.py` & `hamradio-0.5/hamradio/eqsl.py`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/lotw.py` & `hamradio-0.5/hamradio/lotw.py`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/qslcard.py` & `hamradio-0.5/hamradio/qslcard.py`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/qth.py` & `hamradio-0.5/hamradio/qth.py`

 * *Files identical despite different names*

### Comparing `hamradio-0.4/hamradio/requester.py` & `hamradio-0.5/hamradio/requester.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 #!/usr/bin/python
-# Copyright (C) 2019-21 Dr. Ralf Schlatterbeck Open Source Consulting.
+# Copyright (C) 2019-22 Dr. Ralf Schlatterbeck Open Source Consulting.
 # Reichergasse 131, A-3411 Weidling.
 # Web: http://www.runtux.com Email: office@runtux.com
 # ****************************************************************************
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are
 # met:
 #
@@ -84,15 +84,18 @@
             pass
         if n :
             t = urlparse (self.url)
             a = n.authenticators (t.netloc)
         if a :
             un, d, pw = a
             if not self.relax_check and un != self.username :
-                raise ValueError ("Netrc username doesn't match")
+                raise ValueError \
+                    ( "Netrc username for %s doesn't match (expected: %s)"
+                    % (t.netloc, un)
+                    )
             self._pw = pw
             return pw
         pw = getpass ('Password: ')
         self._pw = pw
         return pw
     # end def get_pw
```

### Comparing `hamradio-0.4/setup.py` & `hamradio-0.5/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 #!/usr/bin/env python
-# Copyright (C) 2019-21 Dr. Ralf Schlatterbeck Open Source Consulting.
+# Copyright (C) 2019-23 Dr. Ralf Schlatterbeck Open Source Consulting.
 # Reichergasse 131, A-3411 Weidling.
 # Web: http://www.runtux.com Email: office@runtux.com
 # ****************************************************************************
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are
 # met:
 #
@@ -27,16 +27,22 @@
 # SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
 # ****************************************************************************
 
 try :
     from hamradio.Version import VERSION
 except :
     VERSION = None
+from warnings       import filterwarnings
 from distutils.core import setup, Extension
 
+filterwarnings \
+    ( "ignore"
+    , "Unknown distribution option: 'install_requires'"
+    )
+
 description = []
 with open ('README.rst') as f :
     for line in f :
             description.append (line)
 
 license     = 'BSD License'
 setup \
@@ -49,28 +55,28 @@
     , author_email     = "rsc@runtux.com"
     , install_requires = ['rsclib', 'requests', 'bs4']
     , packages         = ['hamradio']
     , package_data     = dict
         (hamradio = ['data/*.txt', 'data/*.dat', 'data/*.html'])
     , platforms        = 'Any'
     , python_requires  = '>=3.6'
-    , scripts          = [ 'bin/qso-import'
-                         , 'bin/callsign_lookup'
-                         , 'bin/qsl-export'
-                         ]
+    , entry_points     = dict
+        ( console_scripts =
+            [ 'callsign_lookup=hamradio.dxcc:main'
+            , 'qsl-export=hamradio.qslcard:main'
+            , 'qso-import=hamradio.dbimport:main'
+            ]
+        )
     , url              = 'https://github.com/schlatterbeck/hamradio'
     , classifiers      =
         [ 'Development Status :: 5 - Production/Stable'
         , 'License :: OSI Approved :: ' + license
         , 'Operating System :: OS Independent'
         , 'Programming Language :: Python'
         , 'Intended Audience :: Developers'
-        , 'Programming Language :: Python :: 2'
-        , 'Programming Language :: Python :: 2.7'
-        , 'Programming Language :: Python :: 3'
-        , 'Programming Language :: Python :: 3.5'
-        , 'Programming Language :: Python :: 3.6'
         , 'Programming Language :: Python :: 3.7'
         , 'Programming Language :: Python :: 3.8'
         , 'Programming Language :: Python :: 3.9'
+        , 'Programming Language :: Python :: 3.10'
+        , 'Programming Language :: Python :: 3.11'
         ]
     )
```

