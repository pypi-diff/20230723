# Comparing `tmp/chromedriver_auto-0.0.4.tar.gz` & `tmp/chromedriver_auto-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chromedriver_auto-0.0.4.tar", last modified: Sun Jul 23 17:46:32 2023, max compression
+gzip compressed data, was "chromedriver_auto-1.0.1.tar", last modified: Sun Jul 23 17:50:25 2023, max compression
```

## Comparing `chromedriver_auto-0.0.4.tar` & `chromedriver_auto-1.0.1.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:46:32.056561 chromedriver_auto-0.0.4/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)     1074 2023-07-23 17:17:05.000000 chromedriver_auto-0.0.4/LICENSE
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 17:46:32.056621 chromedriver_auto-0.0.4/PKG-INFO
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      155 2023-07-23 17:34:22.000000 chromedriver_auto-0.0.4/README.md
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      103 2023-07-23 17:08:21.000000 chromedriver_auto-0.0.4/pyproject.toml
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      761 2023-07-23 17:46:32.056902 chromedriver_auto-0.0.4/setup.cfg
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:46:32.054766 chromedriver_auto-0.0.4/src/
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:46:32.055649 chromedriver_auto-0.0.4/src/chromedriver_auto/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:06:12.000000 chromedriver_auto-0.0.4/src/chromedriver_auto/__init__.py
--rw-r--r--   0 sorowerhossan   (501) staff       (20)     4489 2023-07-23 17:44:47.000000 chromedriver_auto-0.0.4/src/chromedriver_auto/driver_ready.py
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:46:32.056433 chromedriver_auto-0.0.4/src/chromedriver_auto.egg-info/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 17:46:32.000000 chromedriver_auto-0.0.4/src/chromedriver_auto.egg-info/PKG-INFO
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      294 2023-07-23 17:46:32.000000 chromedriver_auto-0.0.4/src/chromedriver_auto.egg-info/SOURCES.txt
--rw-r--r--   0 sorowerhossan   (501) staff       (20)        1 2023-07-23 17:46:32.000000 chromedriver_auto-0.0.4/src/chromedriver_auto.egg-info/dependency_links.txt
--rw-r--r--   0 sorowerhossan   (501) staff       (20)       18 2023-07-23 17:46:32.000000 chromedriver_auto-0.0.4/src/chromedriver_auto.egg-info/top_level.txt
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:50:25.492159 chromedriver_auto-1.0.1/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     1074 2023-07-23 17:17:05.000000 chromedriver_auto-1.0.1/LICENSE
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 17:50:25.492223 chromedriver_auto-1.0.1/PKG-INFO
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      155 2023-07-23 17:34:22.000000 chromedriver_auto-1.0.1/README.md
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      103 2023-07-23 17:08:21.000000 chromedriver_auto-1.0.1/pyproject.toml
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      761 2023-07-23 17:50:25.492443 chromedriver_auto-1.0.1/setup.cfg
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:50:25.490504 chromedriver_auto-1.0.1/src/
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:50:25.491416 chromedriver_auto-1.0.1/src/chromedriver_auto/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:06:12.000000 chromedriver_auto-1.0.1/src/chromedriver_auto/__init__.py
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     4669 2023-07-23 17:49:54.000000 chromedriver_auto-1.0.1/src/chromedriver_auto/driver_ready.py
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:50:25.492051 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 17:50:25.000000 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/PKG-INFO
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      294 2023-07-23 17:50:25.000000 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/SOURCES.txt
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)        1 2023-07-23 17:50:25.000000 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/dependency_links.txt
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)       18 2023-07-23 17:50:25.000000 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/top_level.txt
```

### Comparing `chromedriver_auto-0.0.4/LICENSE` & `chromedriver_auto-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `chromedriver_auto-0.0.4/PKG-INFO` & `chromedriver_auto-1.0.1/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chromedriver_auto
-Version: 0.0.4
+Version: 1.0.1
 Summary: This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 Home-page: https://github.com/pypa/sampleproject
 Author: Sorower Hossan
 Author-email: sorower37@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `chromedriver_auto-0.0.4/setup.cfg` & `chromedriver_auto-1.0.1/setup.cfg`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = chromedriver_auto
-version = 0.0.4
+version = 1.0.1
 author = Sorower Hossan
 author_email = sorower37@gmail.com
 description = This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/pypa/sampleproject
 project_urls =
```

### Comparing `chromedriver_auto-0.0.4/src/chromedriver_auto/driver_ready.py` & `chromedriver_auto-1.0.1/src/chromedriver_auto/driver_ready.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,113 +1,111 @@
-
-import os
-import platform
-import subprocess
-import zipfile
-from selenium import webdriver
-import requests
-from selenium.webdriver.chrome.service import Service
-
-def test():
-    print('hiiiiiiiiii')
-    return 'done'
-# def get_operating_system():
-#     return platform.system()
-
-# # Example usage:
-# os_name = get_operating_system()
-# if os_name == "Windows":
-#     file_path= str(os.getcwd()) + '/chrome/chromedriver-win'
-# elif os_name == "Darwin":
-#     file_path= str(os.getcwd()) + '/chrome/chromedriver-mac-arm64'
-# try:
-#     service = Service(executable_path=file_path)
-#     driver = webdriver.Chrome(service=service)
-# except:
-#     file_path= os.getcwd()
-#     print(file_path)
-    
-#     def get_chrome_version():
-#         if platform.system() == 'Windows':
-#             try:
-#                 process = subprocess.Popen(['wmic', 'datafile', 'where', 'name="C:\\\\Program Files (x86)\\\\Google\\\\Chrome\\\\Application\\\\chrome.exe"', 'get', 'Version'], stdout=subprocess.PIPE, stderr=subprocess.PIPE, shell=True)
-#                 output, error = process.communicate()
-#                 if not error:
-#                     version = output.decode().strip().split('\n')[1].strip()
-#                     return version
-#             except Exception as e:
-#                 print("Error occurred:", e)
-#         elif platform.system() == 'Darwin':  # macOS
-#             try:
-#                 process = subprocess.Popen(['/Applications/Google Chrome.app/Contents/MacOS/Google Chrome', '--version'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)
-#                 output, error = process.communicate()
-#                 if not error:
-#                     version = output.decode().strip().split(' ')[2]
-#                     return version
-#             except Exception as e:
-#                 print("Error occurred:", e)
-#         elif platform.system() == 'Linux':
-#             try:
-#                 process = subprocess.Popen(['google-chrome', '--version'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)
-#                 output, error = process.communicate()
-#                 if not error:
-#                     version = output.decode().strip().split(' ')[2]
-#                     return version
-#             except Exception as e:
-#                 print("Error occurred:", e)
-
-#         return None
-
-#     chrome_version = get_chrome_version()
-#     print(chrome_version)
-#     def get_operating_system():
-#         return platform.system()
-
-#     # Example usage:
-#     os_name = get_operating_system()
-#     if os_name == "Windows":
-#         def get_windows_architecture():
-#             return platform.architecture()[0]
-#         windows_arch = get_windows_architecture()
-
-#         if windows_arch == '32bit':
-#             download_url = f'https://edgedl.me.gvt1.com/edgedl/chrome/chrome-for-testing/{chrome_version}/win32/chromedriver-win32.zip'
-#         elif windows_arch == '64bit':
-#             download_url = f'https://edgedl.me.gvt1.com/edgedl/chrome/chrome-for-testing/{chrome_version}/win64/chromedriver-win64.zip'
-#             print("Windows OS is 64-bit.")
-        
-#         r = requests.get(download_url, allow_redirects=True)
-#         open('chromedriver-win.zip', 'wb').write(r.content)
+def chrome_driver():
+    import os
+    import platform
+    import subprocess
+    import zipfile
+    from selenium import webdriver
+    import requests
+    from selenium.webdriver.chrome.service import Service
+
+
+    def get_operating_system():
+        return platform.system()
+
+    # Example usage:
+    os_name = get_operating_system()
+    if os_name == "Windows":
+        file_path= str(os.getcwd()) + '/chrome/chromedriver-win'
+    elif os_name == "Darwin":
+        file_path= str(os.getcwd()) + '/chrome/chromedriver-mac-arm64'
+    try:
+        service = Service(executable_path=file_path)
+        driver = webdriver.Chrome(service=service)
+    except:
+        file_path= os.getcwd()
+        print(file_path)
         
-#         with zipfile.ZipFile(f'{file_path}/chromedriver-win.zip', 'r') as zip:
-#             try:
-#                 zip.extractall(f'{file_path}/chrome/')
-#             except:
-#                 pass
-#         try:
-#             os.remove(f'{file_path}/chromedriver-win.zip')
-#         except:
-#             pass
-
-#         file_path= str(os.getcwd()) + '/chrome/chromedriver-win'
-#     elif os_name == "Darwin":
-#         download_url = f'https://edgedl.me.gvt1.com/edgedl/chrome/chrome-for-testing/{chrome_version}/mac-arm64/chromedriver-mac-arm64.zip'
-#         r = requests.get(download_url, allow_redirects=True)
-
-#         open('chromedriver-mac-arm64.zip', 'wb').write(r.content)
-
-#         import zipfile
-#         with zipfile.ZipFile(f'{file_path}/chromedriver-mac-arm64.zip', 'r') as zip:
-#             try:
-#                 zip.extractall(f'{file_path}/chrome/')
-#             except:
-#                 pass
-#         try:
-#             os.remove(f'{file_path}/chromedriver-mac-arm64.zip')
-#         except:
-#             pass
-
-
-#         file_path= str(os.getcwd()) + '/chrome/chromedriver-mac-arm64'
-#     service = Service(executable_path=file_path)
-#     driver = webdriver.Chrome(service=service)
-#     # return driver
+        def get_chrome_version():
+            if platform.system() == 'Windows':
+                try:
+                    process = subprocess.Popen(['wmic', 'datafile', 'where', 'name="C:\\\\Program Files (x86)\\\\Google\\\\Chrome\\\\Application\\\\chrome.exe"', 'get', 'Version'], stdout=subprocess.PIPE, stderr=subprocess.PIPE, shell=True)
+                    output, error = process.communicate()
+                    if not error:
+                        version = output.decode().strip().split('\n')[1].strip()
+                        return version
+                except Exception as e:
+                    print("Error occurred:", e)
+            elif platform.system() == 'Darwin':  # macOS
+                try:
+                    process = subprocess.Popen(['/Applications/Google Chrome.app/Contents/MacOS/Google Chrome', '--version'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)
+                    output, error = process.communicate()
+                    if not error:
+                        version = output.decode().strip().split(' ')[2]
+                        return version
+                except Exception as e:
+                    print("Error occurred:", e)
+            elif platform.system() == 'Linux':
+                try:
+                    process = subprocess.Popen(['google-chrome', '--version'], stdout=subprocess.PIPE, stderr=subprocess.PIPE)
+                    output, error = process.communicate()
+                    if not error:
+                        version = output.decode().strip().split(' ')[2]
+                        return version
+                except Exception as e:
+                    print("Error occurred:", e)
+
+            return None
+
+        chrome_version = get_chrome_version()
+        print(chrome_version)
+        def get_operating_system():
+            return platform.system()
+
+        # Example usage:
+        os_name = get_operating_system()
+        if os_name == "Windows":
+            def get_windows_architecture():
+                return platform.architecture()[0]
+            windows_arch = get_windows_architecture()
+
+            if windows_arch == '32bit':
+                download_url = f'https://edgedl.me.gvt1.com/edgedl/chrome/chrome-for-testing/{chrome_version}/win32/chromedriver-win32.zip'
+            elif windows_arch == '64bit':
+                download_url = f'https://edgedl.me.gvt1.com/edgedl/chrome/chrome-for-testing/{chrome_version}/win64/chromedriver-win64.zip'
+                print("Windows OS is 64-bit.")
+            
+            r = requests.get(download_url, allow_redirects=True)
+            open('chromedriver-win.zip', 'wb').write(r.content)
+            
+            with zipfile.ZipFile(f'{file_path}/chromedriver-win.zip', 'r') as zip:
+                try:
+                    zip.extractall(f'{file_path}/chrome/')
+                except:
+                    pass
+            try:
+                os.remove(f'{file_path}/chromedriver-win.zip')
+            except:
+                pass
+
+            file_path= str(os.getcwd()) + '/chrome/chromedriver-win'
+        elif os_name == "Darwin":
+            download_url = f'https://edgedl.me.gvt1.com/edgedl/chrome/chrome-for-testing/{chrome_version}/mac-arm64/chromedriver-mac-arm64.zip'
+            r = requests.get(download_url, allow_redirects=True)
+
+            open('chromedriver-mac-arm64.zip', 'wb').write(r.content)
+
+            import zipfile
+            with zipfile.ZipFile(f'{file_path}/chromedriver-mac-arm64.zip', 'r') as zip:
+                try:
+                    zip.extractall(f'{file_path}/chrome/')
+                except:
+                    pass
+            try:
+                os.remove(f'{file_path}/chromedriver-mac-arm64.zip')
+            except:
+                pass
+
+
+            file_path= str(os.getcwd()) + '/chrome/chromedriver-mac-arm64'
+        service = Service(executable_path=file_path)
+        driver = webdriver.Chrome(service=service)
+        return driver
```

### Comparing `chromedriver_auto-0.0.4/src/chromedriver_auto.egg-info/PKG-INFO` & `chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chromedriver-auto
-Version: 0.0.4
+Version: 1.0.1
 Summary: This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 Home-page: https://github.com/pypa/sampleproject
 Author: Sorower Hossan
 Author-email: sorower37@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

