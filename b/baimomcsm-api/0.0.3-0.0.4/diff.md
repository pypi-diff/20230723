# Comparing `tmp/baimomcsm_api-0.0.3.tar.gz` & `tmp/baimomcsm_api-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\baimomcsm_api-0.0.3.tar", last modified: Fri Jul 21 05:49:08 2023, max compression
+gzip compressed data, was "dist\baimomcsm_api-0.0.4.tar", last modified: Sat Jul 22 23:39:08 2023, max compression
```

## Comparing `baimomcsm_api-0.0.3.tar` & `baimomcsm_api-0.0.4.tar`

### file list

```diff
@@ -1,21 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-07-21 05:49:08.629371 baimomcsm_api-0.0.3/
--rw-rw-rw-   0        0        0    11558 2023-07-20 13:08:31.000000 baimomcsm_api-0.0.3/LICENSE
--rw-rw-rw-   0        0        0       37 2023-07-21 05:42:37.000000 baimomcsm_api-0.0.3/MANIFEST.in
--rw-rw-rw-   0        0        0     2203 2023-07-21 05:49:08.629371 baimomcsm_api-0.0.3/PKG-INFO
--rw-rw-rw-   0        0        0     1105 2023-07-21 05:41:37.000000 baimomcsm_api-0.0.3/README.html
--rw-rw-rw-   0        0        0      873 2023-07-21 05:00:19.000000 baimomcsm_api-0.0.3/README.md
-drwxrwxrwx   0        0        0        0 2023-07-21 05:49:08.619376 baimomcsm_api-0.0.3/baimomcsm_api/
--rw-rw-rw-   0        0        0       45 2023-07-21 05:33:57.000000 baimomcsm_api-0.0.3/baimomcsm_api/__init__.py
--rw-rw-rw-   0        0        0     3278 2023-07-21 04:56:37.000000 baimomcsm_api-0.0.3/baimomcsm_api/applications.py
--rw-rw-rw-   0        0        0      196 2023-07-20 11:37:00.000000 baimomcsm_api-0.0.3/baimomcsm_api/baimomcsm_error.py
--rw-rw-rw-   0        0        0     2549 2023-07-20 12:36:12.000000 baimomcsm_api-0.0.3/baimomcsm_api/common.py
--rw-rw-rw-   0        0        0      183 2023-07-20 08:13:27.000000 baimomcsm_api-0.0.3/baimomcsm_api/log_writer.py
--rw-rw-rw-   0        0        0     1328 2023-07-20 12:07:25.000000 baimomcsm_api-0.0.3/baimomcsm_api/request_sender.py
-drwxrwxrwx   0        0        0        0 2023-07-21 05:49:08.629371 baimomcsm_api-0.0.3/baimomcsm_api.egg-info/
--rw-rw-rw-   0        0        0     2203 2023-07-21 05:49:08.000000 baimomcsm_api-0.0.3/baimomcsm_api.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      407 2023-07-21 05:49:08.000000 baimomcsm_api-0.0.3/baimomcsm_api.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-21 05:49:08.000000 baimomcsm_api-0.0.3/baimomcsm_api.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-07-21 05:49:08.000000 baimomcsm_api-0.0.3/baimomcsm_api.egg-info/requires.txt
--rw-rw-rw-   0        0        0       14 2023-07-21 05:49:08.000000 baimomcsm_api-0.0.3/baimomcsm_api.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-21 05:49:08.629371 baimomcsm_api-0.0.3/setup.cfg
--rw-rw-rw-   0        0        0     1568 2023-07-21 05:48:27.000000 baimomcsm_api-0.0.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-22 23:39:08.921743 baimomcsm_api-0.0.4/
+-rw-rw-rw-   0        0        0       37 2023-07-21 05:42:37.000000 baimomcsm_api-0.0.4/MANIFEST.in
+-rw-rw-rw-   0        0        0     2203 2023-07-22 23:39:08.920722 baimomcsm_api-0.0.4/PKG-INFO
+-rw-rw-rw-   0        0        0      873 2023-07-22 23:32:50.000000 baimomcsm_api-0.0.4/README.md
+drwxrwxrwx   0        0        0        0 2023-07-22 23:39:08.908517 baimomcsm_api-0.0.4/baimomcsm_api/
+-rw-rw-rw-   0        0        0       45 2023-07-21 05:33:57.000000 baimomcsm_api-0.0.4/baimomcsm_api/__init__.py
+-rw-rw-rw-   0        0        0     3278 2023-07-22 13:03:27.000000 baimomcsm_api-0.0.4/baimomcsm_api/applications.py
+-rw-rw-rw-   0        0        0      196 2023-07-20 11:37:00.000000 baimomcsm_api-0.0.4/baimomcsm_api/baimomcsm_error.py
+-rw-rw-rw-   0        0        0     2555 2023-07-22 13:08:53.000000 baimomcsm_api-0.0.4/baimomcsm_api/common.py
+-rw-rw-rw-   0        0        0      183 2023-07-20 08:13:27.000000 baimomcsm_api-0.0.4/baimomcsm_api/log_writer.py
+-rw-rw-rw-   0        0        0     1740 2023-07-22 13:15:51.000000 baimomcsm_api-0.0.4/baimomcsm_api/request_sender.py
+-rw-rw-rw-   0        0        0     3414 2023-07-22 23:32:21.000000 baimomcsm_api-0.0.4/baimomcsm_api/users.py
+drwxrwxrwx   0        0        0        0 2023-07-22 23:39:08.918398 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/
+-rw-rw-rw-   0        0        0     2203 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      410 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       14 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-22 23:39:08.921743 baimomcsm_api-0.0.4/setup.cfg
+-rw-rw-rw-   0        0        0     1568 2023-07-22 23:38:36.000000 baimomcsm_api-0.0.4/setup.py
```

### Comparing `baimomcsm_api-0.0.3/PKG-INFO` & `baimomcsm_api-0.0.4/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: baimomcsm_api
-Version: 0.0.3
+Version: 0.0.4
 Summary: MCSManager API for Python (开发中)
 Home-page: https://github.com/Zhou-Shilin/BaimoMCSManager-API
 Author: BaimoQilin
 Author-email: admin@baimoqilin.top
 License: Apache 2.0
 Description: # BaimoMCSManager API for `Python`
         [![PRs welcome](https://img.shields.io/badge/PRs-welcome-20BF20)](https://github.com/Zhou-Shilin/BaimoMCSManager-API/pulls)
@@ -15,18 +15,18 @@
         
         ## ⚠️注意
         这个项目仍在开发中，仅支持部分功能。  
           
         当前进展：
          - [x] 面板通用设置 ( `common.py`)
          - [x] 应用实例管理 (`applications.py`)
+         - [x] 多用户管理 (`auth.py`)
          - [ ] 实例文件管理 (`files.py`)
          - [ ] 计划任务管理 (`plans.py`)
          - [ ] 守护进程管理 ( `remote_service.py`)
-         - [ ] 多用户管理 (`auth.py`)
         
         ## 📖使用方法
         施工中……
 Platform: all
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Natural Language :: Chinese (Simplified)
```

### Comparing `baimomcsm_api-0.0.3/README.md` & `baimomcsm_api-0.0.4/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -7,14 +7,14 @@
 
 ## ⚠️注意
 这个项目仍在开发中，仅支持部分功能。  
   
 当前进展：
  - [x] 面板通用设置 ( `common.py`)
  - [x] 应用实例管理 (`applications.py`)
+ - [x] 多用户管理 (`auth.py`)
  - [ ] 实例文件管理 (`files.py`)
  - [ ] 计划任务管理 (`plans.py`)
  - [ ] 守护进程管理 ( `remote_service.py`)
- - [ ] 多用户管理 (`auth.py`)
 
 ## 📖使用方法
 施工中……
```

### Comparing `baimomcsm_api-0.0.3/baimomcsm_api/applications.py` & `baimomcsm_api-0.0.4/baimomcsm_api/applications.py`

 * *Files identical despite different names*

### Comparing `baimomcsm_api-0.0.3/baimomcsm_api/common.py` & `baimomcsm_api-0.0.4/baimomcsm_api/common.py`

 * *Files 3% similar despite different names*

```diff
@@ -38,15 +38,15 @@
 
     api_url = url + "/api/overview/setting"
 
     response = sendRequest(api_url, apikey)
 
     return response
 
-def edit_settings(url, apikey, httpPort="25566", httpIP=None, dataPort=23334, forwardType=1, crossDomain=False, gzip=False, maxCompress=1, maxDonwload=10, zipType=1, loginCheckIp=True, loginInfo="", canFileManager=true, language="en_us", quickInstallAddr="https://mcsmanager.oss-cn-guangzhou.aliyuncs.com/quick_install.json", redisUrl=""):
+def edit_settings(url, apikey, httpPort="25566", httpIP=None, dataPort=23334, forwardType=1, crossDomain=False, gzip=False, maxCompress=1, maxDonwload=10, zipType=1, loginCheckIp=True, loginInfo="", canFileManager=True, language="en_us", quickInstallAddr="https://mcsmanager.oss-cn-guangzhou.aliyuncs.com/quick_install.json", redisUrl=""):
     # 修改面板设置
     # 返回类型：bool
     # 返回内容解释：True（成功）
 
     api_url = url + "/api/overview/setting"
 
     _body = {
@@ -63,10 +63,10 @@
         'loginInfo': loginInfo, 
         'canFileManager': canFileManager, 
         'language': language, 
         'quickInstallAddr': quickInstallAddr, 
         'redisUrl': redisUrl
     }
 
-    response = sendRequest(api_url, uuid, remote_uuid, apikey, body=_body)
+    response = sendRequest(api_url, None, None, apikey, method="put",body=_body)
 
     return True
```

### Comparing `baimomcsm_api-0.0.3/baimomcsm_api/request_sender.py` & `baimomcsm_api-0.0.4/baimomcsm_api/request_sender.py`

 * *Files 14% similar despite different names*

```diff
@@ -23,20 +23,29 @@
 
     if method == "get":
         response = requests.get(api_url, params=_params, headers=_headers)
     elif method == "post":
         response = requests.post(api_url, params=_params, headers=_headers, json=body)
     elif method == "put":
         response = requests.put(api_url, params=_params, headers=_headers, json=body)
+    elif method == "delete":
+        response = requests.delete(api_url, params=_params, headers=_headers, json=body)
     else:
-        raise NoThatMethod("没有这种请求方式（目前仅支持get, post, push）")
+        raise NoThatMethod("内部程序错误：没有这种请求方式（目前仅支持get, post, push, delete）")
 
     if response.status_code == 200:
         log("(sendRequest) Successful 200")
 
         return response.json()
     else:
         log("(sendRequest) Failed " + str(response.status_code))
 
-        raise RequestException("请求返回状态码为" + str(response.status_code))
+        if response.status_code == 400:
+            reason = "参数错误"
+        elif response.status_code == 403:
+            reason = "无权限"
+        elif response.status_code == 500:
+            reason = "服务器异常"
+        
+        raise RequestException("请求返回状态码为" + str(response.status_code) + " " + reason)
 
         return False
```

### Comparing `baimomcsm_api-0.0.3/baimomcsm_api.egg-info/PKG-INFO` & `baimomcsm_api-0.0.4/baimomcsm_api.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: baimomcsm-api
-Version: 0.0.3
+Version: 0.0.4
 Summary: MCSManager API for Python (开发中)
 Home-page: https://github.com/Zhou-Shilin/BaimoMCSManager-API
 Author: BaimoQilin
 Author-email: admin@baimoqilin.top
 License: Apache 2.0
 Description: # BaimoMCSManager API for `Python`
         [![PRs welcome](https://img.shields.io/badge/PRs-welcome-20BF20)](https://github.com/Zhou-Shilin/BaimoMCSManager-API/pulls)
@@ -15,18 +15,18 @@
         
         ## ⚠️注意
         这个项目仍在开发中，仅支持部分功能。  
           
         当前进展：
          - [x] 面板通用设置 ( `common.py`)
          - [x] 应用实例管理 (`applications.py`)
+         - [x] 多用户管理 (`auth.py`)
          - [ ] 实例文件管理 (`files.py`)
          - [ ] 计划任务管理 (`plans.py`)
          - [ ] 守护进程管理 ( `remote_service.py`)
-         - [ ] 多用户管理 (`auth.py`)
         
         ## 📖使用方法
         施工中……
 Platform: all
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Natural Language :: Chinese (Simplified)
```

### Comparing `baimomcsm_api-0.0.3/setup.py` & `baimomcsm_api-0.0.4/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from distutils.core import setup
 from setuptools import find_packages
 
 with open("README.md", "r", encoding="utf-8") as f:
   long_description = f.read()
 
 setup(name='baimomcsm_api',  # 包名
-      version='0.0.3',  # 版本号
+      version='0.0.4',  # 版本号
       description='MCSManager API for Python (开发中)',
       long_description=long_description,
       long_description_content_type="text/markdown",
       author='BaimoQilin',
       author_email='admin@baimoqilin.top',
       url='https://github.com/Zhou-Shilin/BaimoMCSManager-API',
       install_requires=["requests"],
```

