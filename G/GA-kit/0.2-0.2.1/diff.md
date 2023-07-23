# Comparing `tmp/GA_kit-0.2.tar.gz` & `tmp/GA_kit-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "GA_kit-0.2.tar", last modified: Sun Jul 23 15:24:54 2023, max compression
+gzip compressed data, was "GA_kit-0.2.1.tar", last modified: Sun Jul 23 18:02:36 2023, max compression
```

## Comparing `GA_kit-0.2.tar` & `GA_kit-0.2.1.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 15:24:54.844644 GA_kit-0.2/
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 15:24:54.820644 GA_kit-0.2/GA_kit/
--rw-r--r--   0 ralf      (1000) priv      (1011)       14 2023-07-23 15:22:04.000000 GA_kit-0.2/GA_kit/Version.py
--rw-r--r--   0 ralf      (1000) priv      (1011)        0 2021-11-20 15:21:14.000000 GA_kit-0.2/GA_kit/__init__.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     8495 2023-07-23 15:10:10.000000 GA_kit-0.2/GA_kit/deceptive.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     5711 2020-06-04 16:08:11.000000 GA_kit-0.2/GA_kit/ecga.py
--rw-r--r--   0 ralf      (1000) priv      (1011)    14233 2020-06-04 16:08:07.000000 GA_kit-0.2/GA_kit/hboa.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     6265 2020-06-04 16:08:01.000000 GA_kit-0.2/GA_kit/sga.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 15:24:54.840644 GA_kit-0.2/GA_kit.egg-info/
--rw-r--r--   0 ralf      (1000) priv      (1011)    10650 2023-07-23 15:24:54.000000 GA_kit-0.2/GA_kit.egg-info/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)      337 2023-07-23 15:24:54.000000 GA_kit-0.2/GA_kit.egg-info/SOURCES.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-07-23 15:24:54.000000 GA_kit-0.2/GA_kit.egg-info/dependency_links.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)       64 2023-07-23 15:24:54.000000 GA_kit-0.2/GA_kit.egg-info/entry_points.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)       13 2023-07-23 15:24:54.000000 GA_kit-0.2/GA_kit.egg-info/requires.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)        7 2023-07-23 15:24:54.000000 GA_kit-0.2/GA_kit.egg-info/top_level.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)     1552 2020-06-04 16:07:23.000000 GA_kit-0.2/LICENSE
--rw-r--r--   0 ralf      (1000) priv      (1011)        0 2020-06-04 16:10:46.000000 GA_kit-0.2/MANIFEST.in
--rw-r--r--   0 ralf      (1000) priv      (1011)    10650 2023-07-23 15:24:54.844644 GA_kit-0.2/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)     9535 2023-07-23 15:08:45.000000 GA_kit-0.2/README.rst
--rw-r--r--   0 ralf      (1000) priv      (1011)     2979 2023-07-23 15:16:08.000000 GA_kit-0.2/pyproject.toml
--rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-07-23 15:24:54.844644 GA_kit-0.2/setup.cfg
--rw-r--r--   0 ralf      (1000) priv      (1011)     3257 2023-07-23 15:16:18.000000 GA_kit-0.2/setup.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 18:02:36.916611 GA_kit-0.2.1/
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 18:02:36.892611 GA_kit-0.2.1/GA_kit/
+-rw-r--r--   0 ralf      (1000) priv      (1011)       16 2023-07-23 18:02:19.000000 GA_kit-0.2.1/GA_kit/Version.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)        0 2021-11-20 15:21:14.000000 GA_kit-0.2.1/GA_kit/__init__.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     8356 2023-07-23 16:43:34.000000 GA_kit-0.2.1/GA_kit/deceptive.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     5715 2023-07-23 16:37:40.000000 GA_kit-0.2.1/GA_kit/ecga.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)    14236 2023-07-23 16:37:58.000000 GA_kit-0.2.1/GA_kit/hboa.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     6265 2020-06-04 16:08:01.000000 GA_kit-0.2.1/GA_kit/sga.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 18:02:36.912611 GA_kit-0.2.1/GA_kit.egg-info/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    10652 2023-07-23 18:02:36.000000 GA_kit-0.2.1/GA_kit.egg-info/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)      337 2023-07-23 18:02:36.000000 GA_kit-0.2.1/GA_kit.egg-info/SOURCES.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-07-23 18:02:36.000000 GA_kit-0.2.1/GA_kit.egg-info/dependency_links.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       64 2023-07-23 18:02:36.000000 GA_kit-0.2.1/GA_kit.egg-info/entry_points.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       13 2023-07-23 18:02:36.000000 GA_kit-0.2.1/GA_kit.egg-info/requires.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        7 2023-07-23 18:02:36.000000 GA_kit-0.2.1/GA_kit.egg-info/top_level.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1552 2020-06-04 16:07:23.000000 GA_kit-0.2.1/LICENSE
+-rw-r--r--   0 ralf      (1000) priv      (1011)        0 2020-06-04 16:10:46.000000 GA_kit-0.2.1/MANIFEST.in
+-rw-r--r--   0 ralf      (1000) priv      (1011)    10652 2023-07-23 18:02:36.916611 GA_kit-0.2.1/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)     9535 2023-07-23 15:08:45.000000 GA_kit-0.2.1/README.rst
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2979 2023-07-23 15:16:08.000000 GA_kit-0.2.1/pyproject.toml
+-rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-07-23 18:02:36.916611 GA_kit-0.2.1/setup.cfg
+-rw-r--r--   0 ralf      (1000) priv      (1011)     3257 2023-07-23 15:16:18.000000 GA_kit-0.2.1/setup.py
```

### Comparing `GA_kit-0.2/GA_kit/deceptive.py` & `GA_kit-0.2.1/GA_kit/deceptive.py`

 * *Files 2% similar despite different names*

```diff
@@ -29,17 +29,17 @@
 # ****************************************************************************
 
 from __future__ import print_function
 from pga import PGA, PGA_STOP_MAXITER, PGA_REPORT_STRING, PGA_POPREPL_RTR
 from pga import PGA_OLDPOP
 from rsclib.autosuper import autosuper
 from argparse import ArgumentParser
-from sga  import SGA
-from ecga import ECGA
-from hboa import HBOA
+from .sga  import SGA
+from .ecga import ECGA
+from .hboa import HBOA
 
 class Deceptive (autosuper) :
 
     fun = ((3, 1),)
     def __init__ \
         ( self
         , fun             = fun
@@ -49,32 +49,29 @@
         , maxiter         = 1000
         , tournament_size = 2
         , rtr_window_size = 0
         , s_penalty       = 2.0
         , min_split       = 0
         , max_parent      = 0
         ) :
-        self.random_seed     = random_seed
         self.fun             = fun
         self.shuffle         = shuffle
         self.s_penalty       = s_penalty
         self.min_split       = min_split
         self.max_parent      = max_parent
-        self.tournament_size = tournament_size
-        self.rtr_window_size = rtr_window_size
         stop_on = [PGA_STOP_MAXITER]
         length  = 0
         for k, n in self.fun :
             length += k * n
         self.__super.__init__ \
             ( length
             , maximize            = True
             , pop_size            = popsize
             , num_replace         = popsize
-            , random_seed         = self.random_seed
+            , random_seed         = random_seed
             , print_options       = [PGA_REPORT_STRING]
             , stopping_rule_types = stop_on
             , pop_replace_type    = PGA_POPREPL_RTR
             , print_frequency     = 10
             , max_GA_iter         = maxiter
             , tournament_size     = tournament_size
             , rtr_window_size     = rtr_window_size
```

### Comparing `GA_kit-0.2/GA_kit/ecga.py` & `GA_kit-0.2.1/GA_kit/ecga.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 #!/usr/bin/python3
-# Copyright (C) 2020 Dr. Ralf Schlatterbeck Open Source Consulting.
+# Copyright (C) 2020-23 Dr. Ralf Schlatterbeck Open Source Consulting.
 # Reichergasse 131, A-3411 Weidling.
 # Web: http://www.runtux.com Email: office@runtux.com
 # ****************************************************************************
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are
 # met:
 #
@@ -26,15 +26,15 @@
 # THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
 # (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
 # OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
 # ****************************************************************************
 
 from __future__ import print_function
 from math import log
-from sga import PMBGA, log2
+from .sga import PMBGA, log2
 
 def pkey (partition) :
     return (-len (partition), partition [0])
 
 class ECGA (PMBGA) :
     """ Extended Compacat Genetic Algorithm
     """
```

### Comparing `GA_kit-0.2/GA_kit/hboa.py` & `GA_kit-0.2.1/GA_kit/hboa.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 #!/usr/bin/python3
-# Copyright (C) 2020 Dr. Ralf Schlatterbeck Open Source Consulting.
+# Copyright (C) 2020-23 Dr. Ralf Schlatterbeck Open Source Consulting.
 # Reichergasse 131, A-3411 Weidling.
 # Web: http://www.runtux.com Email: office@runtux.com
 # ****************************************************************************
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are
 # met:
 #
@@ -26,15 +26,15 @@
 # THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
 # (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
 # OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
 # ****************************************************************************
 
 from sys  import stderr
 from math import log, lgamma
-from sga  import PMBGA, log2
+from .sga import PMBGA, log2
 
 class Bayesian_Network (object) :
 
     def __init__ \
         ( self, hboa, genes
         , lgamma     = lgamma
         , do_debug   = 0
```

### Comparing `GA_kit-0.2/GA_kit/sga.py` & `GA_kit-0.2.1/GA_kit/sga.py`

 * *Files identical despite different names*

### Comparing `GA_kit-0.2/GA_kit.egg-info/PKG-INFO` & `GA_kit-0.2.1/GA_kit.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: GA-kit
-Version: 0.2
+Version: 0.2.1
 Summary: Advanced Genetic Algorithm Toolkit
 Home-page: https://github.com/schlatterbeck/GA_kit
 Author: Ralf Schlatterbeck
 Author-email: Ralf Schlatterbeck <rsc@runtux.com>
 License: BSD License
 Project-URL: Homepage, https://github.com/schlatterbeck/GA_kit
 Project-URL: Bug Tracker, https://github.com/schlatterbeck/GA_kit/issues
```

### Comparing `GA_kit-0.2/LICENSE` & `GA_kit-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `GA_kit-0.2/PKG-INFO` & `GA_kit-0.2.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: GA_kit
-Version: 0.2
+Version: 0.2.1
 Summary: Advanced Genetic Algorithm Toolkit
 Home-page: https://github.com/schlatterbeck/GA_kit
 Author: Ralf Schlatterbeck
 Author-email: Ralf Schlatterbeck <rsc@runtux.com>
 License: BSD License
 Project-URL: Homepage, https://github.com/schlatterbeck/GA_kit
 Project-URL: Bug Tracker, https://github.com/schlatterbeck/GA_kit/issues
```

### Comparing `GA_kit-0.2/README.rst` & `GA_kit-0.2.1/README.rst`

 * *Files identical despite different names*

### Comparing `GA_kit-0.2/pyproject.toml` & `GA_kit-0.2.1/pyproject.toml`

 * *Files identical despite different names*

### Comparing `GA_kit-0.2/setup.py` & `GA_kit-0.2.1/setup.py`

 * *Files identical despite different names*

