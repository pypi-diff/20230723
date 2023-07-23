# Comparing `tmp/django-passkeys-1.2.4.tar.gz` & `tmp/django-passkeys-1.2.5b1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-passkeys-1.2.4.tar", last modified: Mon Jun 19 14:09:30 2023, max compression
+gzip compressed data, was "django-passkeys-1.2.5b1.tar", last modified: Sun Jul 23 15:45:59 2023, max compression
```

## Comparing `django-passkeys-1.2.4.tar` & `django-passkeys-1.2.5b1.tar`

### file list

```diff
@@ -1,40 +1,40 @@
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     1075 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/LICENSE
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)      192 2023-06-19 06:42:21.000000 django-passkeys-1.2.4/MANIFEST.in
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     7691 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/PKG-INFO
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     6314 2023-06-19 13:56:23.000000 django-passkeys-1.2.4/README.md
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/django_passkeys.egg-info/
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     7691 2023-06-19 14:09:30.000000 django-passkeys-1.2.4/django_passkeys.egg-info/PKG-INFO
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)      864 2023-06-19 14:09:30.000000 django-passkeys-1.2.4/django_passkeys.egg-info/SOURCES.txt
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)        1 2023-06-19 14:09:30.000000 django-passkeys-1.2.4/django_passkeys.egg-info/dependency_links.txt
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)        1 2023-04-09 09:42:26.000000 django-passkeys-1.2.4/django_passkeys.egg-info/not-zip-safe
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)       47 2023-06-19 14:09:30.000000 django-passkeys-1.2.4/django_passkeys.egg-info/requires.txt
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)       17 2023-06-19 14:09:30.000000 django-passkeys-1.2.4/django_passkeys.egg-info/top_level.txt
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/passkeys/
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     5823 2023-06-19 06:42:21.000000 django-passkeys-1.2.4/passkeys/FIDO2.py
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)       65 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/__init__.py
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)      790 2023-06-19 06:42:21.000000 django-passkeys-1.2.4/passkeys/backend.py
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/passkeys/migrations/
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     1176 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/migrations/0001_initial.py
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)        0 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/migrations/__init__.py
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)      599 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/models.py
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/passkeys/static/
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/passkeys/static/passkeys/
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/passkeys/static/passkeys/css/
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     1590 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/static/passkeys/css/bootstrap-toggle.min.css
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/passkeys/static/passkeys/imgs/
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     8981 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/static/passkeys/imgs/FIDO-Passkey_Icon-White.png
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/passkeys/static/passkeys/js/
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     2684 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/static/passkeys/js/base64url.js
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     4129 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/static/passkeys/js/bootstrap-toggle.min.js
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)      687 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/static/passkeys/js/helpers.js
-drwxrwxr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/passkeys/templates/
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     5795 2023-05-23 13:57:16.000000 django-passkeys-1.2.4/passkeys/templates/PassKeys.html
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)      128 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/templates/PassKeys_base.html
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)      724 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/templates/check_passkeys.js
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)      807 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/templates/modal.html
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     2249 2023-06-08 06:46:46.000000 django-passkeys-1.2.4/passkeys/templates/passkeys.js
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)      563 2023-04-09 08:41:37.000000 django-passkeys-1.2.4/passkeys/urls.py
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     1023 2023-06-19 13:24:31.000000 django-passkeys-1.2.4/passkeys/views.py
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)       38 2023-06-19 14:09:30.716174 django-passkeys-1.2.4/setup.cfg
--rw-rw-r--   0 mohamed   (1000) mohamed   (1000)     1811 2023-06-19 14:09:28.000000 django-passkeys-1.2.4/setup.py
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.363121 django-passkeys-1.2.5b1/
+-rw-r--r--   0 mohamed    (501) admin       (80)     1075 2022-10-28 09:47:43.000000 django-passkeys-1.2.5b1/LICENSE
+-rw-r--r--   0 mohamed    (501) admin       (80)      192 2023-07-23 15:26:08.000000 django-passkeys-1.2.5b1/MANIFEST.in
+-rw-r--r--   0 mohamed    (501) admin       (80)     7693 2023-07-23 15:45:59.362784 django-passkeys-1.2.5b1/PKG-INFO
+-rw-r--r--   0 mohamed    (501) admin       (80)     6314 2023-07-23 15:26:08.000000 django-passkeys-1.2.5b1/README.md
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.350595 django-passkeys-1.2.5b1/django_passkeys.egg-info/
+-rw-r--r--   0 mohamed    (501) admin       (80)     7693 2023-07-23 15:45:59.000000 django-passkeys-1.2.5b1/django_passkeys.egg-info/PKG-INFO
+-rw-r--r--   0 mohamed    (501) admin       (80)      864 2023-07-23 15:45:59.000000 django-passkeys-1.2.5b1/django_passkeys.egg-info/SOURCES.txt
+-rw-r--r--   0 mohamed    (501) admin       (80)        1 2023-07-23 15:45:59.000000 django-passkeys-1.2.5b1/django_passkeys.egg-info/dependency_links.txt
+-rw-r--r--   0 mohamed    (501) admin       (80)        1 2022-10-28 09:57:05.000000 django-passkeys-1.2.5b1/django_passkeys.egg-info/not-zip-safe
+-rw-r--r--   0 mohamed    (501) admin       (80)       47 2023-07-23 15:45:59.000000 django-passkeys-1.2.5b1/django_passkeys.egg-info/requires.txt
+-rw-r--r--   0 mohamed    (501) admin       (80)       17 2023-07-23 15:45:59.000000 django-passkeys-1.2.5b1/django_passkeys.egg-info/top_level.txt
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.354161 django-passkeys-1.2.5b1/passkeys/
+-rw-r--r--   0 mohamed    (501) admin       (80)     5823 2023-07-23 15:26:08.000000 django-passkeys-1.2.5b1/passkeys/FIDO2.py
+-rw-r--r--   0 mohamed    (501) admin       (80)       65 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/__init__.py
+-rw-r--r--   0 mohamed    (501) admin       (80)      790 2023-07-23 15:26:08.000000 django-passkeys-1.2.5b1/passkeys/backend.py
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.356831 django-passkeys-1.2.5b1/passkeys/migrations/
+-rw-r--r--   0 mohamed    (501) admin       (80)     1176 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/migrations/0001_initial.py
+-rw-r--r--   0 mohamed    (501) admin       (80)        0 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/migrations/__init__.py
+-rw-r--r--   0 mohamed    (501) admin       (80)      599 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/models.py
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.343089 django-passkeys-1.2.5b1/passkeys/static/
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.344336 django-passkeys-1.2.5b1/passkeys/static/passkeys/
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.357245 django-passkeys-1.2.5b1/passkeys/static/passkeys/css/
+-rw-r--r--   0 mohamed    (501) admin       (80)     1590 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/static/passkeys/css/bootstrap-toggle.min.css
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.357836 django-passkeys-1.2.5b1/passkeys/static/passkeys/imgs/
+-rw-r--r--   0 mohamed    (501) admin       (80)     8981 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/static/passkeys/imgs/FIDO-Passkey_Icon-White.png
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.359416 django-passkeys-1.2.5b1/passkeys/static/passkeys/js/
+-rw-r--r--   0 mohamed    (501) admin       (80)     2684 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/static/passkeys/js/base64url.js
+-rw-r--r--   0 mohamed    (501) admin       (80)     4129 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/static/passkeys/js/bootstrap-toggle.min.js
+-rw-r--r--   0 mohamed    (501) admin       (80)      687 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/static/passkeys/js/helpers.js
+drwxr-xr-x   0 mohamed    (501) admin       (80)        0 2023-07-23 15:45:59.361998 django-passkeys-1.2.5b1/passkeys/templates/
+-rw-r--r--   0 mohamed    (501) admin       (80)     5795 2023-06-07 15:50:35.000000 django-passkeys-1.2.5b1/passkeys/templates/PassKeys.html
+-rw-r--r--   0 mohamed    (501) admin       (80)      128 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/templates/PassKeys_base.html
+-rw-r--r--   0 mohamed    (501) admin       (80)      724 2022-10-29 13:23:58.000000 django-passkeys-1.2.5b1/passkeys/templates/check_passkeys.js
+-rw-r--r--   0 mohamed    (501) admin       (80)      807 2022-10-29 09:43:43.000000 django-passkeys-1.2.5b1/passkeys/templates/modal.html
+-rw-r--r--   0 mohamed    (501) admin       (80)     2612 2023-07-23 15:34:36.000000 django-passkeys-1.2.5b1/passkeys/templates/passkeys.js
+-rw-r--r--   0 mohamed    (501) admin       (80)      563 2022-10-29 13:32:38.000000 django-passkeys-1.2.5b1/passkeys/urls.py
+-rw-r--r--   0 mohamed    (501) admin       (80)     1023 2023-07-23 15:26:08.000000 django-passkeys-1.2.5b1/passkeys/views.py
+-rw-r--r--   0 mohamed    (501) admin       (80)       38 2023-07-23 15:45:59.363261 django-passkeys-1.2.5b1/setup.cfg
+-rw-r--r--   0 mohamed    (501) admin       (80)     1813 2023-07-23 15:45:27.000000 django-passkeys-1.2.5b1/setup.py
```

### Comparing `django-passkeys-1.2.4/LICENSE` & `django-passkeys-1.2.5b1/LICENSE`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/PKG-INFO` & `django-passkeys-1.2.5b1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-passkeys
-Version: 1.2.4
+Version: 1.2.5b1
 Summary: A Django Authentication Backend for Passkeys
 Home-page: https://github.com/mkalioby/django-passkeys
 Download-URL: https://github.com/mkalioby/django-passkeys
 Author: Mohamed El-Kalioby
 Author-email: mkalioby@mkalioby.com
 License: MIT
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `django-passkeys-1.2.4/README.md` & `django-passkeys-1.2.5b1/README.md`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/django_passkeys.egg-info/PKG-INFO` & `django-passkeys-1.2.5b1/django_passkeys.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-passkeys
-Version: 1.2.4
+Version: 1.2.5b1
 Summary: A Django Authentication Backend for Passkeys
 Home-page: https://github.com/mkalioby/django-passkeys
 Download-URL: https://github.com/mkalioby/django-passkeys
 Author: Mohamed El-Kalioby
 Author-email: mkalioby@mkalioby.com
 License: MIT
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `django-passkeys-1.2.4/django_passkeys.egg-info/SOURCES.txt` & `django-passkeys-1.2.5b1/django_passkeys.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/FIDO2.py` & `django-passkeys-1.2.5b1/passkeys/FIDO2.py`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/backend.py` & `django-passkeys-1.2.5b1/passkeys/backend.py`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/migrations/0001_initial.py` & `django-passkeys-1.2.5b1/passkeys/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/models.py` & `django-passkeys-1.2.5b1/passkeys/models.py`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/static/passkeys/css/bootstrap-toggle.min.css` & `django-passkeys-1.2.5b1/passkeys/static/passkeys/css/bootstrap-toggle.min.css`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/static/passkeys/imgs/FIDO-Passkey_Icon-White.png` & `django-passkeys-1.2.5b1/passkeys/static/passkeys/imgs/FIDO-Passkey_Icon-White.png`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/static/passkeys/js/base64url.js` & `django-passkeys-1.2.5b1/passkeys/static/passkeys/js/base64url.js`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/static/passkeys/js/bootstrap-toggle.min.js` & `django-passkeys-1.2.5b1/passkeys/static/passkeys/js/bootstrap-toggle.min.js`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/static/passkeys/js/helpers.js` & `django-passkeys-1.2.5b1/passkeys/static/passkeys/js/helpers.js`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/templates/PassKeys.html` & `django-passkeys-1.2.5b1/passkeys/templates/PassKeys.html`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/templates/check_passkeys.js` & `django-passkeys-1.2.5b1/passkeys/templates/check_passkeys.js`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/templates/modal.html` & `django-passkeys-1.2.5b1/passkeys/templates/modal.html`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/templates/passkeys.js` & `django-passkeys-1.2.5b1/passkeys/templates/passkeys.js`

 * *Files 14% similar despite different names*

#### js-beautify {}

```diff
@@ -3,22 +3,24 @@
 } <
 script type = "application/javascript"
 src = "{% static 'passkeys/js/base64url.js' %}" > < /script> <
     script type = "application/javascript"
 src = "{% static 'passkeys/js/helpers.js' %}" > < /script> <
     script type = "text/javascript" >
     window.conditionalUI = false;
+window.conditionUIAbortController = new AbortController();
+window.conditionUIAbortSignal = conditionUIAbortController.signal;
 
 function checkConditionalUI(form) {
     if (window.PublicKeyCredential && PublicKeyCredential.isConditionalMediationAvailable) {
         // Check if conditional mediation is available.
         PublicKeyCredential.isConditionalMediationAvailable().then((result) => {
             window.conditionalUI = result;
             if (window.conditionalUI) {
-                authn(form)
+                start_authn(form, true)
             }
         });
     }
 }
 
 var GetAssertReq = (getAssert) => {
     getAssert.publicKey.challenge = base64url.decode(getAssert.publicKey.challenge);
@@ -26,30 +28,32 @@
     for (let allowCred of getAssert.publicKey.allowCredentials) {
         allowCred.id = base64url.decode(allowCred.id);
     }
 
     return getAssert
 }
 
-function authn(form) {
+function start_authn(form, conditionalUI = false) {
     window.loginForm = form;
     fetch('{% url '
         passkeys: auth_begin ' %}', {
             method: 'GET',
         }).then(function(response) {
         if (response.ok) {
             return response.json().then(function(req) {
                 return GetAssertReq(req)
             });
         }
         throw new Error('No credential available to authenticate!');
     }).then(function(options) {
-        if (window.conditionalUI) {
+        if (conditionalUI) {
             options.mediation = 'conditional';
-        }
+            options.signal = window.conditionUIAbortSignal;
+        } else
+            window.conditionUIAbortController.abort()
         console.log(options)
         return navigator.credentials.get(options);
     }).then(function(assertion) {
         pk = $("#passkeys")
         if (pk.length == 0) {
             console.error("Did you add the 'passkeys' hidden input field")
             return
@@ -66,10 +70,13 @@
     $(document).ready(function() {
         if (location.protocol != 'https:') {
             console.error("Passkeys must work under secure context")
         }
     });
 }
 
+function authn(form) {
+    start_authn(form, false)
+}
 
 <
 /script>
```

### Comparing `django-passkeys-1.2.4/passkeys/urls.py` & `django-passkeys-1.2.5b1/passkeys/urls.py`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/passkeys/views.py` & `django-passkeys-1.2.5b1/passkeys/views.py`

 * *Files identical despite different names*

### Comparing `django-passkeys-1.2.4/setup.py` & `django-passkeys-1.2.5b1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 
 from setuptools import find_packages, setup
 
 setup(
     name='django-passkeys',
-    version='1.2.4',
+    version='1.2.5b1',
     description='A Django Authentication Backend for Passkeys',
     long_description=open("README.md").read(),
     long_description_content_type="text/markdown",
     author='Mohamed El-Kalioby',
     author_email = 'mkalioby@mkalioby.com',
     url = 'https://github.com/mkalioby/django-passkeys',
     download_url='https://github.com/mkalioby/django-passkeys',
```

