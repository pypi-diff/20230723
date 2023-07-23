# Comparing `tmp/phap-2.2.1rc1.tar.gz` & `tmp/phap-3.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "phap-2.2.1rc1.tar", last modified: Sat May 27 02:53:42 2023, max compression
+gzip compressed data, was "phap-3.0.0.tar", last modified: Sun Jul 23 04:50:57 2023, max compression
```

## Comparing `phap-2.2.1rc1.tar` & `phap-3.0.0.tar`

### file list

```diff
@@ -1,28 +1,29 @@
-drwxrwxrwx   0        0        0        0 2023-05-27 02:53:42.328446 phap-2.2.1rc1/
--rw-rw-rw-   0        0        0     1069 2023-05-25 04:31:47.000000 phap-2.2.1rc1/LICENSE
--rw-rw-rw-   0        0        0     2048 2023-05-27 02:53:42.326449 phap-2.2.1rc1/PKG-INFO
--rw-rw-rw-   0        0        0     1248 2023-05-27 02:53:14.000000 phap-2.2.1rc1/README.md
--rw-rw-rw-   0        0        0       86 2022-03-12 07:02:40.000000 phap-2.2.1rc1/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-27 02:53:42.328446 phap-2.2.1rc1/setup.cfg
--rw-rw-rw-   0        0        0     1686 2023-05-27 02:51:19.000000 phap-2.2.1rc1/setup.py
-drwxrwxrwx   0        0        0        0 2023-05-27 02:53:41.906673 phap-2.2.1rc1/src/
-drwxrwxrwx   0        0        0        0 2023-05-27 02:53:41.920305 phap-2.2.1rc1/src/numalgo/
--rw-rw-rw-   0        0        0       62 2023-05-26 11:43:30.000000 phap-2.2.1rc1/src/numalgo/__init__.py
--rw-rw-rw-   0        0        0      450 2023-05-27 02:24:29.000000 phap-2.2.1rc1/src/numalgo/deskcheck.py
-drwxrwxrwx   0        0        0        0 2023-05-27 02:53:41.921304 phap-2.2.1rc1/src/phap/
--rw-rw-rw-   0        0        0      881 2023-05-26 10:49:29.000000 phap-2.2.1rc1/src/phap/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-27 02:53:42.298383 phap-2.2.1rc1/src/phap.egg-info/
--rw-rw-rw-   0        0        0     2048 2023-05-27 02:53:41.000000 phap-2.2.1rc1/src/phap.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      419 2023-05-27 02:53:41.000000 phap-2.2.1rc1/src/phap.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-27 02:53:41.000000 phap-2.2.1rc1/src/phap.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       21 2023-05-27 02:53:41.000000 phap-2.2.1rc1/src/phap.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-05-27 02:53:42.304392 phap-2.2.1rc1/src/stralgo/
--rw-rw-rw-   0        0        0       55 2023-05-26 11:28:00.000000 phap-2.2.1rc1/src/stralgo/__init__.py
--rw-rw-rw-   0        0        0      972 2023-02-20 00:51:10.000000 phap-2.2.1rc1/src/stralgo/base.py
-drwxrwxrwx   0        0        0        0 2023-05-27 02:53:42.308389 phap-2.2.1rc1/src/stralgo/hash/
--rw-rw-rw-   0        0        0      251 2023-05-26 11:43:14.000000 phap-2.2.1rc1/src/stralgo/hash/__init__.py
--rw-rw-rw-   0        0        0      460 2023-02-20 00:51:14.000000 phap-2.2.1rc1/src/stralgo/hash/sha.py
-drwxrwxrwx   0        0        0        0 2023-05-27 02:53:42.312400 phap-2.2.1rc1/src/stralgo/hash/sm/
--rw-rw-rw-   0        0        0       26 2023-05-26 09:54:41.000000 phap-2.2.1rc1/src/stralgo/hash/sm/__init__.py
--rw-rw-rw-   0        0        0     6937 2023-05-26 09:54:41.000000 phap-2.2.1rc1/src/stralgo/hash/sm/sm3libs.py
--rw-rw-rw-   0        0        0      175 2023-05-25 04:35:10.000000 phap-2.2.1rc1/src/stralgo/json.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:50:57.772704 phap-3.0.0/
+-rw-rw-rw-   0        0        0     1069 2023-05-25 04:31:47.000000 phap-3.0.0/LICENSE
+-rw-rw-rw-   0        0        0     2495 2023-07-23 04:50:57.770704 phap-3.0.0/PKG-INFO
+-rw-rw-rw-   0        0        0     1698 2023-07-23 04:49:48.000000 phap-3.0.0/README.md
+-rw-rw-rw-   0        0        0       86 2022-03-12 07:02:40.000000 phap-3.0.0/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 04:50:57.772704 phap-3.0.0/setup.cfg
+-rw-rw-rw-   0        0        0     1683 2023-07-23 04:49:19.000000 phap-3.0.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:50:57.683406 phap-3.0.0/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 04:50:57.738000 phap-3.0.0/src/algo/
+-rw-rw-rw-   0        0        0      210 2023-07-23 04:14:03.000000 phap-3.0.0/src/algo/__init__.py
+-rw-rw-rw-   0        0        0      601 2023-07-23 04:13:41.000000 phap-3.0.0/src/algo/arraylib.py
+-rw-rw-rw-   0        0        0     2357 2023-07-23 04:09:49.000000 phap-3.0.0/src/algo/treelib.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:50:57.740980 phap-3.0.0/src/phap/
+-rw-rw-rw-   0        0        0      940 2023-07-23 04:16:00.000000 phap-3.0.0/src/phap/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:50:57.751110 phap-3.0.0/src/phap.egg-info/
+-rw-rw-rw-   0        0        0     2495 2023-07-23 04:50:57.000000 phap-3.0.0/src/phap.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      432 2023-07-23 04:50:57.000000 phap-3.0.0/src/phap.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 04:50:57.000000 phap-3.0.0/src/phap.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 04:50:57.000000 phap-3.0.0/src/phap.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 04:50:57.759109 phap-3.0.0/src/stralgo/
+-rw-rw-rw-   0        0        0      718 2023-07-23 04:26:02.000000 phap-3.0.0/src/stralgo/__init__.py
+-rw-rw-rw-   0        0        0     1021 2023-07-23 04:21:42.000000 phap-3.0.0/src/stralgo/base.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:50:57.764702 phap-3.0.0/src/stralgo/hash/
+-rw-rw-rw-   0        0        0      354 2023-07-23 04:20:12.000000 phap-3.0.0/src/stralgo/hash/__init__.py
+-rw-rw-rw-   0        0        0      508 2023-07-23 04:20:41.000000 phap-3.0.0/src/stralgo/hash/sha.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:50:57.767703 phap-3.0.0/src/stralgo/hash/sm/
+-rw-rw-rw-   0        0        0      148 2023-07-23 04:17:13.000000 phap-3.0.0/src/stralgo/hash/sm/__init__.py
+-rw-rw-rw-   0        0        0     7024 2023-07-23 04:18:55.000000 phap-3.0.0/src/stralgo/hash/sm/sm3libs.py
+-rw-rw-rw-   0        0        0      233 2023-07-23 04:22:18.000000 phap-3.0.0/src/stralgo/json.py
```

### Comparing `phap-2.2.1rc1/LICENSE` & `phap-3.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `phap-2.2.1rc1/PKG-INFO` & `phap-3.0.0/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: phap
-Version: 2.2.1rc1
+Version: 3.0.0
 Summary: Programing Helpful Algorithm Package
 Home-page: https://github.com/DashBing/phap/
 Author: DashBing
 Author-email: mcbbkf@outlook.com
 Project-URL: Github, https://github.com/DashBing/phap/
 Project-URL: Old Project Version(stralgo), https://pypi.org/project/stralgo/
 Classifier: Development Status :: 5 - Production/Stable
@@ -20,30 +20,38 @@
 
 # phap
 ### *Programing Helpful Algorithm Package*
 ### Powered by Python 3.11
 [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](http://choosealicense.com/licenses/mit/)
 
 ### English  | [简体中文](README-zh-CN.md)
+#### *如果你不是在Github上阅读本说明，你可能无法打开非英语版本的说明文档*
+#### *请前往[Github](https://github.com/DashBing/phap/ "Github")网站，确保你能够成功地切换语言*
 
 # Links
 [Github](https://github.com/DashBing/phap/ "Github") | [Pypi](https://pypi.org/project/phap/ "Pypi") | [Pypi (stralgo)](https://pypi.org/project/stralgo/ "Pypi (stralgo)")
 
 # Versions
 ## Stable Version
 + v0.1.0 (stralgo)
 + v1.1.1 (stralgo)
 + v2.1.2
++ v2.2.1
 
 ## Latest Available Version
-+ v2.2.0
++ v3.0.0
 
 ## Latest Version
 ### *(The data under the master branch is inaccurate. Please refer to the dev branch for details)*
-+ v2.2.1-rc1
++ v3.0.0
+
+# To Use
+## Read our development document
+### *(Click the [Github](https://github.com/DashBing/phap/ "Github") link to read this document，or you may can not to open the link)*
++ [Development Document](doc/README.md)
 
 # Build
 ## Precondition
 + Install git and make tools
 + Install Python(the version 3.9 or the version 3.11)
 + Clone source code from source repository
 ```
```

### Comparing `phap-2.2.1rc1/README.md` & `phap-3.0.0/README.md`

 * *Files 26% similar despite different names*

```diff
@@ -1,29 +1,37 @@
 # phap
 ### *Programing Helpful Algorithm Package*
 ### Powered by Python 3.11
 [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](http://choosealicense.com/licenses/mit/)
 
 ### English  | [简体中文](README-zh-CN.md)
+#### *如果你不是在Github上阅读本说明，你可能无法打开非英语版本的说明文档*
+#### *请前往[Github](https://github.com/DashBing/phap/ "Github")网站，确保你能够成功地切换语言*
 
 # Links
 [Github](https://github.com/DashBing/phap/ "Github") | [Pypi](https://pypi.org/project/phap/ "Pypi") | [Pypi (stralgo)](https://pypi.org/project/stralgo/ "Pypi (stralgo)")
 
 # Versions
 ## Stable Version
 + v0.1.0 (stralgo)
 + v1.1.1 (stralgo)
 + v2.1.2
++ v2.2.1
 
 ## Latest Available Version
-+ v2.2.0
++ v3.0.0
 
 ## Latest Version
 ### *(The data under the master branch is inaccurate. Please refer to the dev branch for details)*
-+ v2.2.1-rc1
++ v3.0.0
+
+# To Use
+## Read our development document
+### *(Click the [Github](https://github.com/DashBing/phap/ "Github") link to read this document，or you may can not to open the link)*
++ [Development Document](doc/README.md)
 
 # Build
 ## Precondition
 + Install git and make tools
 + Install Python(the version 3.9 or the version 3.11)
 + Clone source code from source repository
 ```
```

### Comparing `phap-2.2.1rc1/setup.py` & `phap-3.0.0/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="phap",
-    version="2.2.1rc1",  #版本
+    version="3.0.0",  #版本
     author="DashBing",
     author_email="mcbbkf@outlook.com",
     description="Programing Helpful Algorithm Package",
     long_description=long_description,
     long_description_content_type="text/markdown",
     #scripts=[],
     url="https://github.com/DashBing/phap/",
```

### Comparing `phap-2.2.1rc1/src/phap.egg-info/PKG-INFO` & `phap-3.0.0/src/phap.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: phap
-Version: 2.2.1rc1
+Version: 3.0.0
 Summary: Programing Helpful Algorithm Package
 Home-page: https://github.com/DashBing/phap/
 Author: DashBing
 Author-email: mcbbkf@outlook.com
 Project-URL: Github, https://github.com/DashBing/phap/
 Project-URL: Old Project Version(stralgo), https://pypi.org/project/stralgo/
 Classifier: Development Status :: 5 - Production/Stable
@@ -20,30 +20,38 @@
 
 # phap
 ### *Programing Helpful Algorithm Package*
 ### Powered by Python 3.11
 [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](http://choosealicense.com/licenses/mit/)
 
 ### English  | [简体中文](README-zh-CN.md)
+#### *如果你不是在Github上阅读本说明，你可能无法打开非英语版本的说明文档*
+#### *请前往[Github](https://github.com/DashBing/phap/ "Github")网站，确保你能够成功地切换语言*
 
 # Links
 [Github](https://github.com/DashBing/phap/ "Github") | [Pypi](https://pypi.org/project/phap/ "Pypi") | [Pypi (stralgo)](https://pypi.org/project/stralgo/ "Pypi (stralgo)")
 
 # Versions
 ## Stable Version
 + v0.1.0 (stralgo)
 + v1.1.1 (stralgo)
 + v2.1.2
++ v2.2.1
 
 ## Latest Available Version
-+ v2.2.0
++ v3.0.0
 
 ## Latest Version
 ### *(The data under the master branch is inaccurate. Please refer to the dev branch for details)*
-+ v2.2.1-rc1
++ v3.0.0
+
+# To Use
+## Read our development document
+### *(Click the [Github](https://github.com/DashBing/phap/ "Github") link to read this document，or you may can not to open the link)*
++ [Development Document](doc/README.md)
 
 # Build
 ## Precondition
 + Install git and make tools
 + Install Python(the version 3.9 or the version 3.11)
 + Clone source code from source repository
 ```
```

### Comparing `phap-2.2.1rc1/src/stralgo/base.py` & `phap-3.0.0/src/stralgo/base.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+# 本模块是关于base系列算法的集合
+
 from base64 import b16encode as _b16e
 from base64 import b16decode as _b16d
 from base64 import b32encode as _b32e
 from base64 import b32decode as _b32d
 from base64 import b64encode as _b64e
 from base64 import b64decode as _b64d
 from base64 import b85encode as _b85e
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `phap-2.2.1rc1/src/stralgo/hash/sm/sm3libs.py` & `phap-3.0.0/src/stralgo/hash/sm/sm3libs.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,7 +1,11 @@
+'''
+本模块中部分内容为互联网中搜集
+'''
+
 def sm3_int_hex(
         m='61626364616263646162636461626364616263646162636461626364616263646162636461626364616263646162636461626364616263646162636461626364',
         IV='7380166f4914b2b9172442d7da8a0600a96f30bc163138aae38dee4db0fb0e4e'
     ):
     #填充函数
     def filling(m):
         #消息m是一个16进制字符串
@@ -258,15 +262,15 @@
     s = ""
     text = list(text)
     for i in text:
         s = s + str(ord(i))
     #print(s)
     return(s)
 
-def sm3(text:str, IV:str='7380166f4914b2b9172442d7da8a0600a96f30bc163138aae38dee4db0fb0e4e') -> str:
+def sm3(text:str, IV:str='7380166f4914b2b9172442d7da8a0600a96f30bc163138aae38dee4db0fb0e4e') -> str:  # 商密算法的主函数
     s = str_to_int(text)
     s = sm3_int_hex(m=s, IV=IV)
     return(s)
 
 if __name__ == "__main__":
     while True:
         print(sm3(text=input()))
```

