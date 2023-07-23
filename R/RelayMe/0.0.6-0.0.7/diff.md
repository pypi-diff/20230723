# Comparing `tmp/RelayMe-0.0.6.tar.gz` & `tmp/RelayMe-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "RelayMe-0.0.6.tar", last modified: Fri Jul 14 23:24:53 2023, max compression
+gzip compressed data, was "RelayMe-0.0.7.tar", last modified: Sun Jul 23 15:10:44 2023, max compression
```

## Comparing `RelayMe-0.0.6.tar` & `RelayMe-0.0.7.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-07-14 23:24:53.504353 RelayMe-0.0.6/
--rw-rw-rw-   0        0        0      518 2023-07-14 23:22:37.000000 RelayMe-0.0.6/CHANGELOG.txt
--rw-rw-rw-   0        0        0     1066 2023-07-13 14:27:01.000000 RelayMe-0.0.6/LICENCE.txt
--rw-rw-rw-   0        0        0       25 2023-07-13 14:09:08.000000 RelayMe-0.0.6/MANIFEST.in
--rw-rw-rw-   0        0        0     2806 2023-07-14 23:24:53.503355 RelayMe-0.0.6/PKG-INFO
--rw-rw-rw-   0        0        0     1744 2023-07-14 23:20:53.000000 RelayMe-0.0.6/README.txt
-drwxrwxrwx   0        0        0        0 2023-07-14 23:24:53.473919 RelayMe-0.0.6/RelayMe/
--rw-rw-rw-   0        0        0     1603 2023-07-14 23:21:04.000000 RelayMe-0.0.6/RelayMe/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-14 23:24:53.501358 RelayMe-0.0.6/RelayMe.egg-info/
--rw-rw-rw-   0        0        0     2806 2023-07-14 23:24:53.000000 RelayMe-0.0.6/RelayMe.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      201 2023-07-14 23:24:53.000000 RelayMe-0.0.6/RelayMe.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-14 23:24:53.000000 RelayMe-0.0.6/RelayMe.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-07-14 23:24:53.000000 RelayMe-0.0.6/RelayMe.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-14 23:24:53.504353 RelayMe-0.0.6/setup.cfg
--rw-rw-rw-   0        0        0      779 2023-07-14 23:21:16.000000 RelayMe-0.0.6/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:10:44.177452 RelayMe-0.0.7/
+-rw-rw-rw-   0        0        0      643 2023-07-23 15:04:29.000000 RelayMe-0.0.7/CHANGELOG.txt
+-rw-rw-rw-   0        0        0     1066 2023-07-13 14:27:01.000000 RelayMe-0.0.7/LICENCE.txt
+-rw-rw-rw-   0        0        0       25 2023-07-13 14:09:08.000000 RelayMe-0.0.7/MANIFEST.in
+-rw-rw-rw-   0        0        0     3412 2023-07-23 15:10:44.176451 RelayMe-0.0.7/PKG-INFO
+-rw-rw-rw-   0        0        0     2225 2023-07-23 15:08:30.000000 RelayMe-0.0.7/README.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 15:10:44.106340 RelayMe-0.0.7/RelayMe/
+-rw-rw-rw-   0        0        0     3215 2023-07-23 15:00:19.000000 RelayMe-0.0.7/RelayMe/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:10:44.173499 RelayMe-0.0.7/RelayMe.egg-info/
+-rw-rw-rw-   0        0        0     3412 2023-07-23 15:10:43.000000 RelayMe-0.0.7/RelayMe.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      201 2023-07-23 15:10:43.000000 RelayMe-0.0.7/RelayMe.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:10:43.000000 RelayMe-0.0.7/RelayMe.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 15:10:43.000000 RelayMe-0.0.7/RelayMe.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:10:44.177452 RelayMe-0.0.7/setup.cfg
+-rw-rw-rw-   0        0        0      779 2023-07-23 15:09:21.000000 RelayMe-0.0.7/setup.py
```

### Comparing `RelayMe-0.0.6/LICENCE.txt` & `RelayMe-0.0.7/LICENCE.txt`

 * *Files identical despite different names*

### Comparing `RelayMe-0.0.6/PKG-INFO` & `RelayMe-0.0.7/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: RelayMe
-Version: 0.0.6
+Version: 0.0.7
 Summary: Sends emails with chosen email relay service
 Home-page: 
 Author: Elijah Phifer
 Author-email: elijahphifer9@gmail.com
 License: MIT
 Keywords: mail,email,relay,relayservice
 Classifier: Development Status :: 5 - Production/Stable
@@ -13,15 +13,15 @@
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 License-File: LICENCE.txt
 
 RelayMe
 =======
 
-0.0.6
+0.0.7
 -----
 
 This module is geared towards emailing using email relay services.
 
 Prerequisites
 -------------
 
@@ -77,17 +77,33 @@
    sender = SenderConfig(config["EmailConfig"])
 
    body = "This is the body of the email."
    recipient = "John.Doe@mail.com"  # (or it can come from a config file where you could list multiple emails)
 
    sender.send_email(body, recipient)
 
+Here's an example of formatting with html:
+
+.. code-block:: python
+
+   sender = SenderConfig(config["EmailConfig"], format="html")
+
+   body = '''  <strong>Date-time</strong>:  2023-07-21 17:56:47.943528 <br>
+               <strong>id</strong>: 27 <br>
+               <strong>Message</strong>: This is a message
+   '''
+   recipient = "John.Doe@mail.com"  # (or it can come from a config file where you could list multiple emails)
+
+   sender.send_email(body, recipient)
 
 Change Log
 =============
+0.0.7 (07/23/2023)
+------------------
+-Added formating with html and the option to completely customize the entire email.
 
 0.0.6 (07/14/2023)
 -------------------
 -Added more variables to the config file.
 
 0.0.5 (07/14/2023)
 -------------------
```

### Comparing `RelayMe-0.0.6/README.txt` & `RelayMe-0.0.7/README.txt`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 RelayMe
 =======
 
-0.0.6
+0.0.7
 -----
 
 This module is geared towards emailing using email relay services.
 
 Prerequisites
 -------------
 
@@ -60,7 +60,21 @@
 
    sender = SenderConfig(config["EmailConfig"])
 
    body = "This is the body of the email."
    recipient = "John.Doe@mail.com"  # (or it can come from a config file where you could list multiple emails)
 
    sender.send_email(body, recipient)
+
+Here's an example of formatting with html:
+
+.. code-block:: python
+
+   sender = SenderConfig(config["EmailConfig"], format="html")
+
+   body = '''  <strong>Date-time</strong>:  2023-07-21 17:56:47.943528 <br>
+               <strong>id</strong>: 27 <br>
+               <strong>Message</strong>: This is a message
+   '''
+   recipient = "John.Doe@mail.com"  # (or it can come from a config file where you could list multiple emails)
+
+   sender.send_email(body, recipient)
```

### Comparing `RelayMe-0.0.6/RelayMe.egg-info/PKG-INFO` & `RelayMe-0.0.7/RelayMe.egg-info/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: RelayMe
-Version: 0.0.6
+Version: 0.0.7
 Summary: Sends emails with chosen email relay service
 Home-page: 
 Author: Elijah Phifer
 Author-email: elijahphifer9@gmail.com
 License: MIT
 Keywords: mail,email,relay,relayservice
 Classifier: Development Status :: 5 - Production/Stable
@@ -13,15 +13,15 @@
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 License-File: LICENCE.txt
 
 RelayMe
 =======
 
-0.0.6
+0.0.7
 -----
 
 This module is geared towards emailing using email relay services.
 
 Prerequisites
 -------------
 
@@ -77,17 +77,33 @@
    sender = SenderConfig(config["EmailConfig"])
 
    body = "This is the body of the email."
    recipient = "John.Doe@mail.com"  # (or it can come from a config file where you could list multiple emails)
 
    sender.send_email(body, recipient)
 
+Here's an example of formatting with html:
+
+.. code-block:: python
+
+   sender = SenderConfig(config["EmailConfig"], format="html")
+
+   body = '''  <strong>Date-time</strong>:  2023-07-21 17:56:47.943528 <br>
+               <strong>id</strong>: 27 <br>
+               <strong>Message</strong>: This is a message
+   '''
+   recipient = "John.Doe@mail.com"  # (or it can come from a config file where you could list multiple emails)
+
+   sender.send_email(body, recipient)
 
 Change Log
 =============
+0.0.7 (07/23/2023)
+------------------
+-Added formating with html and the option to completely customize the entire email.
 
 0.0.6 (07/14/2023)
 -------------------
 -Added more variables to the config file.
 
 0.0.5 (07/14/2023)
 -------------------
```

### Comparing `RelayMe-0.0.6/setup.py` & `RelayMe-0.0.7/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     'Operating System :: Microsoft :: Windows :: Windows 10',
     'License :: OSI Approved :: MIT License',
     'Programming Language :: Python :: 3'
 ]
 
 setup(
     name='RelayMe',
-    version='0.0.6',
+    version='0.0.7',
     description='Sends emails with chosen email relay service',
     long_description=open('README.txt').read() + '\n\n' +
     open('CHANGELOG.txt').read(),
     url='',
     author='Elijah Phifer',
     author_email='elijahphifer9@gmail.com',
     license='MIT',
```

