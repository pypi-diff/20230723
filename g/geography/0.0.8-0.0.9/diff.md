# Comparing `tmp/geography-0.0.8.tar.gz` & `tmp/geography-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "geography-0.0.8.tar", last modified: Sun Oct 31 23:28:46 2021, max compression
+gzip compressed data, was "geography-0.0.9.tar", last modified: Sun Oct 31 23:37:19 2021, max compression
```

## Comparing `geography-0.0.8.tar` & `geography-0.0.9.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2021-10-31 23:28:46.492221 geography-0.0.8/
--rw-rw-rw-   0        0        0     1060 2021-10-30 22:11:52.000000 geography-0.0.8/LICENSE.txt
--rw-rw-rw-   0        0        0        0 2021-10-30 22:11:07.000000 geography-0.0.8/MANIFEST.in
--rw-rw-rw-   0        0        0      567 2021-10-31 23:28:46.491721 geography-0.0.8/PKG-INFO
--rw-rw-rw-   0        0        0       49 2021-10-30 22:10:28.000000 geography-0.0.8/README.txt
-drwxrwxrwx   0        0        0        0 2021-10-31 23:28:46.476719 geography-0.0.8/geography/
--rw-rw-rw-   0        0        0   126680 2021-10-31 23:27:42.000000 geography-0.0.8/geography/__init__.py
-drwxrwxrwx   0        0        0        0 2021-10-31 23:28:46.490721 geography-0.0.8/geography.egg-info/
--rw-rw-rw-   0        0        0      567 2021-10-31 23:28:46.000000 geography-0.0.8/geography.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      197 2021-10-31 23:28:46.000000 geography-0.0.8/geography.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2021-10-31 23:28:46.000000 geography-0.0.8/geography.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       10 2021-10-31 23:28:46.000000 geography-0.0.8/geography.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2021-10-31 23:28:46.492221 geography-0.0.8/setup.cfg
--rw-rw-rw-   0        0        0      699 2021-10-31 23:28:37.000000 geography-0.0.8/setup.py
+drwxrwxrwx   0        0        0        0 2021-10-31 23:37:19.046060 geography-0.0.9/
+-rw-rw-rw-   0        0        0     1060 2021-10-30 22:11:52.000000 geography-0.0.9/LICENSE.txt
+-rw-rw-rw-   0        0        0        0 2021-10-30 22:11:07.000000 geography-0.0.9/MANIFEST.in
+-rw-rw-rw-   0        0        0      567 2021-10-31 23:37:19.045560 geography-0.0.9/PKG-INFO
+-rw-rw-rw-   0        0        0       49 2021-10-30 22:10:28.000000 geography-0.0.9/README.txt
+drwxrwxrwx   0        0        0        0 2021-10-31 23:37:19.030557 geography-0.0.9/geography/
+-rw-rw-rw-   0        0        0   128097 2021-10-31 23:36:10.000000 geography-0.0.9/geography/__init__.py
+drwxrwxrwx   0        0        0        0 2021-10-31 23:37:19.044560 geography-0.0.9/geography.egg-info/
+-rw-rw-rw-   0        0        0      567 2021-10-31 23:37:18.000000 geography-0.0.9/geography.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      197 2021-10-31 23:37:18.000000 geography-0.0.9/geography.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2021-10-31 23:37:18.000000 geography-0.0.9/geography.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       10 2021-10-31 23:37:18.000000 geography-0.0.9/geography.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2021-10-31 23:37:19.046060 geography-0.0.9/setup.cfg
+-rw-rw-rw-   0        0        0      699 2021-10-31 23:37:07.000000 geography-0.0.9/setup.py
```

### Comparing `geography-0.0.8/LICENSE.txt` & `geography-0.0.9/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `geography-0.0.8/PKG-INFO` & `geography-0.0.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: geography
-Version: 0.0.8
+Version: 0.0.9
 Summary: Get info about countries and states
 Home-page: UNKNOWN
 Author: FrenchFries8854
 Author-email: frenchfries8854@gmail.com
 License: MIT
 Keywords: geography
 Platform: UNKNOWN
```

### Comparing `geography-0.0.8/geography/__init__.py` & `geography-0.0.9/geography/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -3193,14 +3193,32 @@
     def getAreaInMiles(cls, alpha3: str):
         if Countries.doesCountryExist(alpha3) is False:
             return None
         else:
             return math.ceil(int(Data.alpha3ToAreaKMm[alpha3.upper()]) / 2.59)
 
     @classmethod
+    def getAreaRanking(cls, alpha3: str):
+        if Countries.doesCountryExist(alpha3) is False:
+            return None
+        else:
+            areaDict = {}
+            for count, item in enumerate(Data.alpha3List):
+                if Countries.getAreaInKM(item) is None:
+                    pass
+                else:
+                    areaDict[item] = Countries.getAreaInKM(item)
+            newSorted = dict(sorted(areaDict.items(), key=lambda kv: kv[1], reverse=True))
+            rank = 0
+            for count, item in enumerate(newSorted):
+                if str(item) == alpha3.upper():
+                    rank = count + 1
+            return rank
+
+    @classmethod
     def getCapital(cls, alpha3: str):
         if Countries.doesCountryExist(alpha3) is False:
             return None
         else:
             return Data.alpha3ToCapital[Countries.getRedirectedNameToAlpha3(alpha3)]
 
     @classmethod
@@ -3355,14 +3373,32 @@
     def getAreaMiles(cls, usStateAlpha: str):
         if UsaStates.doesStateExist(usStateAlpha) is False:
             return None
         else:
             return math.ceil(int(Data.alpha3ToAreaKMm[UsaStates.getRedirectedNameToAlpha(usStateAlpha)]) / 2.59)
 
     @classmethod
+    def getAreaRanking(cls, usStateAlpha: str):
+        if UsaStates.doesStateExist(usStateAlpha) is False:
+            return None
+        else:
+            areaDict = {}
+            for count, item in enumerate(Data.usaStateAlphaList):
+                if UsaStates.getAreaKM(item) is None:
+                    pass
+                else:
+                    areaDict[item] = UsaStates.getAreaKM(item)
+            newSorted = dict(sorted(areaDict.items(), key=lambda kv: kv[1], reverse=True))
+            rank = 0
+            for count, item in enumerate(newSorted):
+                if str(item) == usStateAlpha.upper():
+                    rank = count + 1
+            return rank
+
+    @classmethod
     def getCapital(cls, usStateAlpha: str):
         if UsaStates.doesStateExist(usStateAlpha) is False:
             return None
         else:
             return Data.usaStateAlphaToCapital[UsaStates.getRedirectedNameToAlpha(usStateAlpha)]
 
     @classmethod
```

### Comparing `geography-0.0.8/geography.egg-info/PKG-INFO` & `geography-0.0.9/geography.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: geography
-Version: 0.0.8
+Version: 0.0.9
 Summary: Get info about countries and states
 Home-page: UNKNOWN
 Author: FrenchFries8854
 Author-email: frenchfries8854@gmail.com
 License: MIT
 Keywords: geography
 Platform: UNKNOWN
```

### Comparing `geography-0.0.8/setup.py` & `geography-0.0.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     "Operating System :: Microsoft :: Windows :: Windows 10",
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python :: 3"
 ]
 
 setup(
     name="geography",
-    version="0.0.8",
+    version="0.0.9",
     description="Get info about countries and states",
     long_description="Get info about countries and states",
     url="",
     author="FrenchFries8854",
     author_email="frenchfries8854@gmail.com",
     license="MIT",
     classifiers=classifiers,
```

