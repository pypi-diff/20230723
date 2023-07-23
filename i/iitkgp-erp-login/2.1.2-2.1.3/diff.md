# Comparing `tmp/iitkgp_erp_login-2.1.2.tar.gz` & `tmp/iitkgp_erp_login-2.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "iitkgp_erp_login-2.1.2.tar", last modified: Sat Jul 22 20:44:13 2023, max compression
+gzip compressed data, was "iitkgp_erp_login-2.1.3.tar", last modified: Sun Jul 23 10:28:40 2023, max compression
```

## Comparing `iitkgp_erp_login-2.1.2.tar` & `iitkgp_erp_login-2.1.3.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:44:13.388147 iitkgp_erp_login-2.1.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-07-22 20:43:34.000000 iitkgp_erp_login-2.1.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    16718 2023-07-22 20:44:13.388147 iitkgp_erp_login-2.1.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    16160 2023-07-22 20:43:34.000000 iitkgp_erp_login-2.1.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      773 2023-07-22 20:43:57.000000 iitkgp_erp_login-2.1.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 20:44:13.388147 iitkgp_erp_login-2.1.2/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:44:13.388147 iitkgp_erp_login-2.1.2/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:44:13.388147 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 20:43:34.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      403 2023-07-22 20:43:34.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login/endpoints.py
--rw-r--r--   0 runner    (1001) docker     (123)     5496 2023-07-22 20:43:34.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login/erp.py
--rw-r--r--   0 runner    (1001) docker     (123)     1184 2023-07-22 20:43:34.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login/read_mail.py
--rw-r--r--   0 runner    (1001) docker     (123)     1669 2023-07-22 20:43:34.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:44:13.388147 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    16718 2023-07-22 20:44:13.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      410 2023-07-22 20:44:13.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 20:44:13.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       92 2023-07-22 20:44:13.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       17 2023-07-22 20:44:13.000000 iitkgp_erp_login-2.1.2/src/iitkgp_erp_login.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:28:40.508271 iitkgp_erp_login-2.1.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-07-23 10:27:54.000000 iitkgp_erp_login-2.1.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    17662 2023-07-23 10:28:40.508271 iitkgp_erp_login-2.1.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    17104 2023-07-23 10:27:54.000000 iitkgp_erp_login-2.1.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      773 2023-07-23 10:28:21.000000 iitkgp_erp_login-2.1.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 10:28:40.508271 iitkgp_erp_login-2.1.3/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:28:40.504271 iitkgp_erp_login-2.1.3/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:28:40.508271 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 10:27:54.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      403 2023-07-23 10:27:54.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login/endpoints.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5695 2023-07-23 10:27:54.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login/erp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1184 2023-07-23 10:27:54.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login/read_mail.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1669 2023-07-23 10:27:54.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:28:40.508271 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    17662 2023-07-23 10:28:40.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      410 2023-07-23 10:28:40.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 10:28:40.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       92 2023-07-23 10:28:40.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       17 2023-07-23 10:28:40.000000 iitkgp_erp_login-2.1.3/src/iitkgp_erp_login.egg-info/top_level.txt
```

### Comparing `iitkgp_erp_login-2.1.2/LICENSE` & `iitkgp_erp_login-2.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `iitkgp_erp_login-2.1.2/PKG-INFO` & `iitkgp_erp_login-2.1.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: iitkgp_erp_login
-Version: 2.1.2
+Version: 2.1.3
 Summary: A package to automate login process in ERP for IIT-KGP
 Author-email: Arpit Bhardwaj <proffapt@pm.me>
 Project-URL: Homepage, https://github.com/proffapt/iitkgp-erp-login-pypi
 Project-URL: Bug Tracker, https://github.com/proffapt/iitkgp-erp-login-pypi/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -39,14 +39,15 @@
 	- <a href="#session-alive-input">Input</a>
 	- <a href="#session-alive-output">Output</a>
 	- <a href="#session-alive-usage">Usage</a>
 - <a href="#ssotoken-alive">SSOToken status check</a>
 	- <a href="#ssotoken-alive-input">Input</a>
 	- <a href="#ssotoken-alive-output">Output</a>
 	- <a href="#ssotoken-alive-usage">Usage</a>
+- <a href="#tokens-from-file">Get tokens from file</a>
 - <a href="#example">Example</a>
 
 </details>
 
 <div id="endpoints"></div>
 
 ## Endpoints
@@ -405,14 +406,53 @@
 
 logged_in_url = f"{HOMEPAGE_URL}?ssoToken={ssoToken}"
 webbrowser.open(logged_in_url)
 ```
 
 > **Note** This is merely a Proof of Concept example; this exact functionality has been integrated into the login function itself from version **2.1.0** onwards.
 
+<div id="tokens-from-file"></div>
+
+## Get tokens from file
+
+The logic for retrieving tokens (`sessionToken` & `ssoToken`) from a file, created earlier by the module itself, is implemented in the `get_tokens_from_file(token_file)` function in [erp.py](https://github.com/proffapt/iitkgp-erp-login-pypi/blob/main/src/iitkgp_erp_login/erp.py). The input and output specifications for the function are mentioned below.
+
+<table>
+<tr>
+<td> Input </td> 
+<td> 
+
+`token_file` - The file containing tokens. 
+
+</td>
+</tr>
+<tr>
+<td> Output </td>
+<td>
+
+`sessionToken, ssoToken`
+
+</td>
+</tr>
+<tr>
+<td> Usage </td>
+<td>
+
+```python
+import iitkgp_erp_login.erp as erp
+
+sessionToken, ssoToken = erp.get_tokens_from_file('.session_token')
+# Here, '.session_token' is the name of file contianing session tokens.
+# It must be as same as the value of 'SESSION_STORAGE_FILE', if used.
+```
+
+</td>
+</tr>
+</table>
+
 <div id="example"></div>
 
 ## Example
 
 Now, we will create a script that opens the ERP Homepage on your default browser with a logged-in session.
 
 1. Install the package.
```

#### html2text {}

```diff
@@ -1,23 +1,23 @@
-Metadata-Version: 2.1 Name: iitkgp_erp_login Version: 2.1.2 Summary: A package
+Metadata-Version: 2.1 Name: iitkgp_erp_login Version: 2.1.3 Summary: A package
 to automate login process in ERP for IIT-KGP Author-email: Arpit Bhardwaj
 pm.me> Project-URL: Homepage, https://github.com/proffapt/iitkgp-erp-login-pypi
 Project-URL: Bug Tracker, https://github.com/proffapt/iitkgp-erp-login-pypi/
 issues Classifier: Programming Language :: Python :: 3 Classifier: License ::
 OSI Approved :: MIT License Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6 Description-Content-Type: text/markdown License-File:
 LICENSE # ERP Login Module Tired of the tedious ERP login process? Wanted to
 automate some ERP workflow but stuck at login?
 ð Introducing **iitkgp-erp-login**: Your Ultimate ERP Login Automation
 Module for _IIT-KGP_ ! ð Key Features: - Seamless Credentials & OTP Handling
 - Effortless Session & ssoToken Management - Smart Token Storage for Efficiency
 > **Note** This package is not officially affiliated with IIT Kharagpur.  Table
 of Contents - Endpoints - About - Usage - Login - Input - Output - Usage -
 Session_status_check - Input - Output - Usage - SSOToken_status_check - Input -
-Output - Usage - Example
+Output - Usage - Get_tokens_from_file - Example
 ## Endpoints The [endpoints.py](https://github.com/proffapt/iitkgp-erp-login-
 pypi/blob/main/src/iitkgp_erp_login/endpoints.py) file includes all the
 necessary endpoints for the ERP login workflow.
 ### About - `HOMEPAGE_URL`: The URL of the ERP homepage/loginpage. -
 `SECRET_QUESTION_URL`: The URL for retrieving the secret question for
 authentication. - `OTP_URL`: The URL for requesting the OTP (One-Time Password)
 for authentication. - `LOGIN_URL`: The URL for ERP login. - `WELCOMEPAGE_URL`:
@@ -183,14 +183,26 @@
 open(".session", "w") as file: file.write(ssoToken) else: _, ssoToken =
 erp.login(headers, session, ERPCREDS=creds, OTP_CHECK_INTERVAL=2, LOGGING=True)
 with open(".session", "w") as file: file.write(ssoToken) logged_in_url = f"
 {HOMEPAGE_URL}?ssoToken={ssoToken}" webbrowser.open(logged_in_url) ``` >
 **Note** This is merely a Proof of Concept example; this exact functionality
 has been integrated into the login function itself from version **2.1.0**
 onwards.
+## Get tokens from file The logic for retrieving tokens (`sessionToken` &
+`ssoToken`) from a file, created earlier by the module itself, is implemented
+in the `get_tokens_from_file(token_file)` function in [erp.py](https://
+github.com/proffapt/iitkgp-erp-login-pypi/blob/main/src/iitkgp_erp_login/
+erp.py). The input and output specifications for the function are mentioned
+below.
+Input  `token_file` - The file containing tokens.
+Output `sessionToken, ssoToken`
+       ```python import iitkgp_erp_login.erp as erp sessionToken, ssoToken =
+Usage  erp.get_tokens_from_file('.session_token') # Here, '.session_token' is
+       the name of file contianing session tokens. # It must be as same as the
+       value of 'SESSION_STORAGE_FILE', if used. ```
 ## Example Now, we will create a script that opens the ERP Homepage on your
 default browser with a logged-in session. 1. Install the package. ```bash pip
 install iitkgp-erp-login ``` 2. Make sure that erpcreds.py & token.json files
 exist in the same directory as the script we are about to create. 3. Create a
 file named `open_erp.py` and include the following code: ```python import
 requests import webbrowser import erpcreds import iitkgp_erp_login.erp as erp
 from iitkgp_erp_login.endpoints import HOMEPAGE_URL headers = { 'timeout':
```

### Comparing `iitkgp_erp_login-2.1.2/README.md` & `iitkgp_erp_login-2.1.3/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -25,14 +25,15 @@
 	- <a href="#session-alive-input">Input</a>
 	- <a href="#session-alive-output">Output</a>
 	- <a href="#session-alive-usage">Usage</a>
 - <a href="#ssotoken-alive">SSOToken status check</a>
 	- <a href="#ssotoken-alive-input">Input</a>
 	- <a href="#ssotoken-alive-output">Output</a>
 	- <a href="#ssotoken-alive-usage">Usage</a>
+- <a href="#tokens-from-file">Get tokens from file</a>
 - <a href="#example">Example</a>
 
 </details>
 
 <div id="endpoints"></div>
 
 ## Endpoints
@@ -391,14 +392,53 @@
 
 logged_in_url = f"{HOMEPAGE_URL}?ssoToken={ssoToken}"
 webbrowser.open(logged_in_url)
 ```
 
 > **Note** This is merely a Proof of Concept example; this exact functionality has been integrated into the login function itself from version **2.1.0** onwards.
 
+<div id="tokens-from-file"></div>
+
+## Get tokens from file
+
+The logic for retrieving tokens (`sessionToken` & `ssoToken`) from a file, created earlier by the module itself, is implemented in the `get_tokens_from_file(token_file)` function in [erp.py](https://github.com/proffapt/iitkgp-erp-login-pypi/blob/main/src/iitkgp_erp_login/erp.py). The input and output specifications for the function are mentioned below.
+
+<table>
+<tr>
+<td> Input </td> 
+<td> 
+
+`token_file` - The file containing tokens. 
+
+</td>
+</tr>
+<tr>
+<td> Output </td>
+<td>
+
+`sessionToken, ssoToken`
+
+</td>
+</tr>
+<tr>
+<td> Usage </td>
+<td>
+
+```python
+import iitkgp_erp_login.erp as erp
+
+sessionToken, ssoToken = erp.get_tokens_from_file('.session_token')
+# Here, '.session_token' is the name of file contianing session tokens.
+# It must be as same as the value of 'SESSION_STORAGE_FILE', if used.
+```
+
+</td>
+</tr>
+</table>
+
 <div id="example"></div>
 
 ## Example
 
 Now, we will create a script that opens the ERP Homepage on your default browser with a logged-in session.
 
 1. Install the package.
```

#### html2text {}

```diff
@@ -2,15 +2,15 @@
 some ERP workflow but stuck at login?
 ð Introducing **iitkgp-erp-login**: Your Ultimate ERP Login Automation
 Module for _IIT-KGP_ ! ð Key Features: - Seamless Credentials & OTP Handling
 - Effortless Session & ssoToken Management - Smart Token Storage for Efficiency
 > **Note** This package is not officially affiliated with IIT Kharagpur.  Table
 of Contents - Endpoints - About - Usage - Login - Input - Output - Usage -
 Session_status_check - Input - Output - Usage - SSOToken_status_check - Input -
-Output - Usage - Example
+Output - Usage - Get_tokens_from_file - Example
 ## Endpoints The [endpoints.py](https://github.com/proffapt/iitkgp-erp-login-
 pypi/blob/main/src/iitkgp_erp_login/endpoints.py) file includes all the
 necessary endpoints for the ERP login workflow.
 ### About - `HOMEPAGE_URL`: The URL of the ERP homepage/loginpage. -
 `SECRET_QUESTION_URL`: The URL for retrieving the secret question for
 authentication. - `OTP_URL`: The URL for requesting the OTP (One-Time Password)
 for authentication. - `LOGIN_URL`: The URL for ERP login. - `WELCOMEPAGE_URL`:
@@ -176,14 +176,26 @@
 open(".session", "w") as file: file.write(ssoToken) else: _, ssoToken =
 erp.login(headers, session, ERPCREDS=creds, OTP_CHECK_INTERVAL=2, LOGGING=True)
 with open(".session", "w") as file: file.write(ssoToken) logged_in_url = f"
 {HOMEPAGE_URL}?ssoToken={ssoToken}" webbrowser.open(logged_in_url) ``` >
 **Note** This is merely a Proof of Concept example; this exact functionality
 has been integrated into the login function itself from version **2.1.0**
 onwards.
+## Get tokens from file The logic for retrieving tokens (`sessionToken` &
+`ssoToken`) from a file, created earlier by the module itself, is implemented
+in the `get_tokens_from_file(token_file)` function in [erp.py](https://
+github.com/proffapt/iitkgp-erp-login-pypi/blob/main/src/iitkgp_erp_login/
+erp.py). The input and output specifications for the function are mentioned
+below.
+Input  `token_file` - The file containing tokens.
+Output `sessionToken, ssoToken`
+       ```python import iitkgp_erp_login.erp as erp sessionToken, ssoToken =
+Usage  erp.get_tokens_from_file('.session_token') # Here, '.session_token' is
+       the name of file contianing session tokens. # It must be as same as the
+       value of 'SESSION_STORAGE_FILE', if used. ```
 ## Example Now, we will create a script that opens the ERP Homepage on your
 default browser with a logged-in session. 1. Install the package. ```bash pip
 install iitkgp-erp-login ``` 2. Make sure that erpcreds.py & token.json files
 exist in the same directory as the script we are about to create. 3. Create a
 file named `open_erp.py` and include the following code: ```python import
 requests import webbrowser import erpcreds import iitkgp_erp_login.erp as erp
 from iitkgp_erp_login.endpoints import HOMEPAGE_URL headers = { 'timeout':
```

### Comparing `iitkgp_erp_login-2.1.2/pyproject.toml` & `iitkgp_erp_login-2.1.3/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "iitkgp_erp_login"
-version = "2.1.2"
+version = "2.1.3"
 authors = [
   { name="Arpit Bhardwaj", email="proffapt@pm.me" },
 ]
 description = "A package to automate login process in ERP for IIT-KGP"
 readme = "README.md"
 requires-python = ">=3.6"
 classifiers = [
```

### Comparing `iitkgp_erp_login-2.1.2/src/iitkgp_erp_login/erp.py` & `iitkgp_erp_login-2.1.3/src/iitkgp_erp_login/erp.py`

 * *Files 8% similar despite different names*

```diff
@@ -24,26 +24,24 @@
     if len(sys.argv) == 1 and sys.argv[0] == '-c':
         caller_file = None
     else:
         caller_file = inspect.getframeinfo(inspect.currentframe().f_back).filename
     token_file = f"{get_import_location(caller_file)}/{SESSION_STORAGE_FILE}" if SESSION_STORAGE_FILE else ""
     if SESSION_STORAGE_FILE:
         try:
-            with open(token_file, "r") as file:
-                lines = file.readlines()
-                sessionToken = lines[0].strip() if len(lines) > 0 else None
-                ssoToken = lines[1].strip() if len(lines) > 1 else None
+            sessionToken, ssoToken = get_tokens_from_file(token_file)
             logging.info(" Retrieved tokens from the file") if LOGGING else None
         except (FileNotFoundError, IOError):
             logging.error(f" Token file doesn't exist") if LOGGING else None
 
     if ssoToken and ssotoken_valid(ssoToken):
-        logging.info(" [SSOToken STATUS]: Valid!") if LOGGING else None
+        logging.info(" [SSOToken STATUS] >> Valid <<") if LOGGING else None
+        session.cookies.set('ssoToken', ssoToken, domain='erp.iitkgp.ac.in')
     else:
-        logging.info(" [SSOToken STATUS]: Not Valid!") if LOGGING and os.path.exists(token_file) else None
+        logging.info(" [SSOToken STATUS] >> Not Valid <<") if LOGGING and os.path.exists(token_file) else None
         
         if ERPCREDS != None:
             ROLL_NUMBER = ERPCREDS.ROLL_NUMBER
             PASSWORD = ERPCREDS.PASSWORD
         else:
             import getpass
             ROLL_NUMBER = input("Enter you Roll Number: ")
@@ -126,7 +124,17 @@
     return r.status_code == 404
 
 
 def ssotoken_valid(ssoToken):
     response = requests.get(f"{HOMEPAGE_URL}?ssoToken={ssoToken}")
     content_type = str(response.headers).split(',')[-1].split("'")[-2]
     return content_type == 'text/html;charset=UTF-8'
+
+
+def get_tokens_from_file(token_file):
+    with open(token_file, "r") as file:
+        lines = file.readlines()
+        sessionToken = lines[0].strip() if len(lines) > 0 else None
+        ssoToken = lines[1].strip() if len(lines) > 1 else None
+
+    return sessionToken, ssoToken
+
```

### Comparing `iitkgp_erp_login-2.1.2/src/iitkgp_erp_login/read_mail.py` & `iitkgp_erp_login-2.1.3/src/iitkgp_erp_login/read_mail.py`

 * *Files identical despite different names*

### Comparing `iitkgp_erp_login-2.1.2/src/iitkgp_erp_login/utils.py` & `iitkgp_erp_login-2.1.3/src/iitkgp_erp_login/utils.py`

 * *Files identical despite different names*

### Comparing `iitkgp_erp_login-2.1.2/src/iitkgp_erp_login.egg-info/PKG-INFO` & `iitkgp_erp_login-2.1.3/src/iitkgp_erp_login.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: iitkgp-erp-login
-Version: 2.1.2
+Version: 2.1.3
 Summary: A package to automate login process in ERP for IIT-KGP
 Author-email: Arpit Bhardwaj <proffapt@pm.me>
 Project-URL: Homepage, https://github.com/proffapt/iitkgp-erp-login-pypi
 Project-URL: Bug Tracker, https://github.com/proffapt/iitkgp-erp-login-pypi/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -39,14 +39,15 @@
 	- <a href="#session-alive-input">Input</a>
 	- <a href="#session-alive-output">Output</a>
 	- <a href="#session-alive-usage">Usage</a>
 - <a href="#ssotoken-alive">SSOToken status check</a>
 	- <a href="#ssotoken-alive-input">Input</a>
 	- <a href="#ssotoken-alive-output">Output</a>
 	- <a href="#ssotoken-alive-usage">Usage</a>
+- <a href="#tokens-from-file">Get tokens from file</a>
 - <a href="#example">Example</a>
 
 </details>
 
 <div id="endpoints"></div>
 
 ## Endpoints
@@ -405,14 +406,53 @@
 
 logged_in_url = f"{HOMEPAGE_URL}?ssoToken={ssoToken}"
 webbrowser.open(logged_in_url)
 ```
 
 > **Note** This is merely a Proof of Concept example; this exact functionality has been integrated into the login function itself from version **2.1.0** onwards.
 
+<div id="tokens-from-file"></div>
+
+## Get tokens from file
+
+The logic for retrieving tokens (`sessionToken` & `ssoToken`) from a file, created earlier by the module itself, is implemented in the `get_tokens_from_file(token_file)` function in [erp.py](https://github.com/proffapt/iitkgp-erp-login-pypi/blob/main/src/iitkgp_erp_login/erp.py). The input and output specifications for the function are mentioned below.
+
+<table>
+<tr>
+<td> Input </td> 
+<td> 
+
+`token_file` - The file containing tokens. 
+
+</td>
+</tr>
+<tr>
+<td> Output </td>
+<td>
+
+`sessionToken, ssoToken`
+
+</td>
+</tr>
+<tr>
+<td> Usage </td>
+<td>
+
+```python
+import iitkgp_erp_login.erp as erp
+
+sessionToken, ssoToken = erp.get_tokens_from_file('.session_token')
+# Here, '.session_token' is the name of file contianing session tokens.
+# It must be as same as the value of 'SESSION_STORAGE_FILE', if used.
+```
+
+</td>
+</tr>
+</table>
+
 <div id="example"></div>
 
 ## Example
 
 Now, we will create a script that opens the ERP Homepage on your default browser with a logged-in session.
 
 1. Install the package.
```

#### html2text {}

```diff
@@ -1,23 +1,23 @@
-Metadata-Version: 2.1 Name: iitkgp-erp-login Version: 2.1.2 Summary: A package
+Metadata-Version: 2.1 Name: iitkgp-erp-login Version: 2.1.3 Summary: A package
 to automate login process in ERP for IIT-KGP Author-email: Arpit Bhardwaj
 pm.me> Project-URL: Homepage, https://github.com/proffapt/iitkgp-erp-login-pypi
 Project-URL: Bug Tracker, https://github.com/proffapt/iitkgp-erp-login-pypi/
 issues Classifier: Programming Language :: Python :: 3 Classifier: License ::
 OSI Approved :: MIT License Classifier: Operating System :: OS Independent
 Requires-Python: >=3.6 Description-Content-Type: text/markdown License-File:
 LICENSE # ERP Login Module Tired of the tedious ERP login process? Wanted to
 automate some ERP workflow but stuck at login?
 ð Introducing **iitkgp-erp-login**: Your Ultimate ERP Login Automation
 Module for _IIT-KGP_ ! ð Key Features: - Seamless Credentials & OTP Handling
 - Effortless Session & ssoToken Management - Smart Token Storage for Efficiency
 > **Note** This package is not officially affiliated with IIT Kharagpur.  Table
 of Contents - Endpoints - About - Usage - Login - Input - Output - Usage -
 Session_status_check - Input - Output - Usage - SSOToken_status_check - Input -
-Output - Usage - Example
+Output - Usage - Get_tokens_from_file - Example
 ## Endpoints The [endpoints.py](https://github.com/proffapt/iitkgp-erp-login-
 pypi/blob/main/src/iitkgp_erp_login/endpoints.py) file includes all the
 necessary endpoints for the ERP login workflow.
 ### About - `HOMEPAGE_URL`: The URL of the ERP homepage/loginpage. -
 `SECRET_QUESTION_URL`: The URL for retrieving the secret question for
 authentication. - `OTP_URL`: The URL for requesting the OTP (One-Time Password)
 for authentication. - `LOGIN_URL`: The URL for ERP login. - `WELCOMEPAGE_URL`:
@@ -183,14 +183,26 @@
 open(".session", "w") as file: file.write(ssoToken) else: _, ssoToken =
 erp.login(headers, session, ERPCREDS=creds, OTP_CHECK_INTERVAL=2, LOGGING=True)
 with open(".session", "w") as file: file.write(ssoToken) logged_in_url = f"
 {HOMEPAGE_URL}?ssoToken={ssoToken}" webbrowser.open(logged_in_url) ``` >
 **Note** This is merely a Proof of Concept example; this exact functionality
 has been integrated into the login function itself from version **2.1.0**
 onwards.
+## Get tokens from file The logic for retrieving tokens (`sessionToken` &
+`ssoToken`) from a file, created earlier by the module itself, is implemented
+in the `get_tokens_from_file(token_file)` function in [erp.py](https://
+github.com/proffapt/iitkgp-erp-login-pypi/blob/main/src/iitkgp_erp_login/
+erp.py). The input and output specifications for the function are mentioned
+below.
+Input  `token_file` - The file containing tokens.
+Output `sessionToken, ssoToken`
+       ```python import iitkgp_erp_login.erp as erp sessionToken, ssoToken =
+Usage  erp.get_tokens_from_file('.session_token') # Here, '.session_token' is
+       the name of file contianing session tokens. # It must be as same as the
+       value of 'SESSION_STORAGE_FILE', if used. ```
 ## Example Now, we will create a script that opens the ERP Homepage on your
 default browser with a logged-in session. 1. Install the package. ```bash pip
 install iitkgp-erp-login ``` 2. Make sure that erpcreds.py & token.json files
 exist in the same directory as the script we are about to create. 3. Create a
 file named `open_erp.py` and include the following code: ```python import
 requests import webbrowser import erpcreds import iitkgp_erp_login.erp as erp
 from iitkgp_erp_login.endpoints import HOMEPAGE_URL headers = { 'timeout':
```

