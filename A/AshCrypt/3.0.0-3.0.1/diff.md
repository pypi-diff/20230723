# Comparing `tmp/AshCrypt-3.0.0.tar.gz` & `tmp/AshCrypt-3.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/AshCrypt-3.0.0.tar", last modified: Fri Jul 21 20:36:38 2023, max compression
+gzip compressed data, was "dist/AshCrypt-3.0.1.tar", last modified: Sun Jul 23 12:59:24 2023, max compression
```

## Comparing `AshCrypt-3.0.0.tar` & `AshCrypt-3.0.1.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/AshCrypt/
--rw-r--r--   0 runner    (1001) docker     (123)    38210 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/AshCryptGUI.py
--rw-r--r--   0 runner    (1001) docker     (123)      281 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      105 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6583 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/clicrypt.py
--rw-r--r--   0 runner    (1001) docker     (123)     7145 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/crypt.py
--rw-r--r--   0 runner    (1001) docker     (123)     8681 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/database.py
--rw-r--r--   0 runner    (1001) docker     (123)     3875 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/filecrypt.py
--rw-r--r--   0 runner    (1001) docker     (123)      479 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/qr.py
--rw-r--r--   0 runner    (1001) docker     (123)     1737 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/textcrypt.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/AshCrypt/unittests/
--rw-r--r--   0 runner    (1001) docker     (123)       31 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/unittests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3263 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/AshCrypt/unittests/unittest_crypt.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/AshCrypt.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1359 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/AshCrypt.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      428 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/AshCrypt.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/AshCrypt.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       70 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/AshCrypt.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/AshCrypt.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1359 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    21244 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-21 20:36:38.000000 AshCrypt-3.0.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1613 2023-07-21 20:36:28.000000 AshCrypt-3.0.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/AshCrypt/
+-rw-r--r--   0 runner    (1001) docker     (123)    38088 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/AshCryptGUI.py
+-rw-r--r--   0 runner    (1001) docker     (123)      281 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      105 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6583 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/clicrypt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7145 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/crypt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8681 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/database.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3875 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/filecrypt.py
+-rw-r--r--   0 runner    (1001) docker     (123)      479 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/qr.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1737 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/textcrypt.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/AshCrypt/unittests/
+-rw-r--r--   0 runner    (1001) docker     (123)       31 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/unittests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3263 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/AshCrypt/unittests/unittest_crypt.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/AshCrypt.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1359 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/AshCrypt.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      428 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/AshCrypt.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/AshCrypt.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/AshCrypt.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/AshCrypt.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1359 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    21477 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 12:59:24.000000 AshCrypt-3.0.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1619 2023-07-23 12:59:14.000000 AshCrypt-3.0.1/setup.py
```

### Comparing `AshCrypt-3.0.0/AshCrypt/AshCryptGUI.py` & `AshCrypt-3.0.1/AshCrypt/AshCryptGUI.py`

 * *Files 1% similar despite different names*

```diff
@@ -1093,22 +1093,13 @@
 def rm_json():
     global usable_real_path
     file = os.path.join(usable_real_path, 'output.json')
     if os.path.exists(file):
         os.remove(file)
 
 
-def rm_qr():
-    if os.path.exists('qrv10.png'):
-        os.remove('qrv10.png')
 
-
-def rm_all():
-    rm_qr()
-    rm_json()
-
-
-atexit.register(rm_all)
+atexit.register(rm_json)
 
 
 if __name__ == '__main__':
     main_object.mainloop()
```

### Comparing `AshCrypt-3.0.0/AshCrypt/clicrypt.py` & `AshCrypt-3.0.1/AshCrypt/clicrypt.py`

 * *Files identical despite different names*

### Comparing `AshCrypt-3.0.0/AshCrypt/crypt.py` & `AshCrypt-3.0.1/AshCrypt/crypt.py`

 * *Files identical despite different names*

### Comparing `AshCrypt-3.0.0/AshCrypt/database.py` & `AshCrypt-3.0.1/AshCrypt/database.py`

 * *Files identical despite different names*

### Comparing `AshCrypt-3.0.0/AshCrypt/filecrypt.py` & `AshCrypt-3.0.1/AshCrypt/filecrypt.py`

 * *Files identical despite different names*

### Comparing `AshCrypt-3.0.0/AshCrypt/textcrypt.py` & `AshCrypt-3.0.1/AshCrypt/textcrypt.py`

 * *Files identical despite different names*

### Comparing `AshCrypt-3.0.0/AshCrypt/unittests/unittest_crypt.py` & `AshCrypt-3.0.1/AshCrypt/unittests/unittest_crypt.py`

 * *Files identical despite different names*

### Comparing `AshCrypt-3.0.0/AshCrypt.egg-info/PKG-INFO` & `AshCrypt-3.0.1/AshCrypt.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AshCrypt
-Version: 3.0.0
+Version: 3.0.1
 Summary: Comprehensive AES-256 Cryptography App & library equipped with files & text handling modules along with a database module to store encrypted content.
 Home-page: https://github.com/AshGw/AES-256.git
 Author: Ashref Gwader
 Author-email: AshrefGw@proton.me
 License: UNKNOWN
 Description: # Cryptography App &  Library : AES-256
         ##  Objective ##
```

### Comparing `AshCrypt-3.0.0/PKG-INFO` & `AshCrypt-3.0.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AshCrypt
-Version: 3.0.0
+Version: 3.0.1
 Summary: Comprehensive AES-256 Cryptography App & library equipped with files & text handling modules along with a database module to store encrypted content.
 Home-page: https://github.com/AshGw/AES-256.git
 Author: Ashref Gwader
 Author-email: AshrefGw@proton.me
 License: UNKNOWN
 Description: # Cryptography App &  Library : AES-256
         ##  Objective ##
```

### Comparing `AshCrypt-3.0.0/README.md` & `AshCrypt-3.0.1/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -2,37 +2,36 @@
 ##  Objective ## 
 #### Enhanced Security, Simplicity & Ease of use For Everyone And Anyone Willing To Use AES 256.
 ## Reason Behind It
 In a world where control, surveillance, and privacy violations are increasingly prevalent, the protection of individual freedom becomes crucial. 
 
 This led me to develop a set of tools in Python that leverages the AES-256 algorithm to make it easier for individuals to safeguard their data without blindly relying on third parties to do it for them. 
 
-My aim here is to make these tools accessible and user-friendly, even for individuals with limited programming knowledge. By providing these resources, I hope to contribute to the preservation of privacy and enable individuals to take control of their own data security, so feel free to explore these tools.
+My aim here is to make these tools accessible and user-friendly, even for individuals with a limited programming knowledge. By providing these resources, I hope to contribute to the preservation of privacy and enable individuals to take control of their own data security, so feel free to explore these tools.
 ## Overview ## 
 ![alt text](important/GUI.png)
 The project incorporates an App & a library called **AshCrypt** : 
 
 **App :** 
-<br>Fully-fledged application that integrates all the modules in the library merging them into a unified and powerful software solution for developers and for people with no programming knowledge whatsoever
+<br>Full-fledged application that integrates all the modules in the library merging them into a unified and powerful software solution for developers and for people with no programming knowledge whatsoever
 <br>check [GUI](https://github.com/AshGw/AES-256#AshCryptGUI) header for more info.
 
 **Library :** 
-<br>A simple, secure, and developer-oriented library for
-encryption and decryption with AES-256 (CBC) . 
+<br>A simple, secure, and developer-oriented library for performing encryption and decryption operations on data using the AES-256 (CBC) encryption algorithm.
 <br>The core of the library is the module `crypt`
 It offers cryptographic capabilities and top security measures to safeguard
 sensitive data,  providing a hassle-free experience when dealing with cryptographic libraries.
 <br>View [Features](https://github.com/AshGw/AES-256#features) Header for more details.
 
 
 
 
 
 ### For Developers ###
-The project uses `crypt` module to ensure secure data encryption and decryption for Files and Texts while keeping it very easy and simple to use .
+The project uses `crypt` module to ensure secure data encryption and decryption for files and texts while keeping it very easy and simple to use .
 view the headers for [filecrypt](https://github.com/AshGw/AES-256#filecrypt) and [textcrypt](https://github.com/AshGw/AES-256#textcrypt) to learn more.
 
 
 It also incorporates a database module that serve the same purpose which is allowing for the management and storage of classified content in a secure, 
 safe and simple manner.
 
 <br>The module has a simple straight forward approach for dealing with sqlite3 databases, even if you're not familiar with Python itself you can still use this module to run SQL queries and built in functions to perform various operations on a given database.<br>Check [database](https://github.com/AshGw/AES-256#database-1) header to learn more.
@@ -121,32 +120,32 @@
 
 ### Usage ##
 1) Generate a key if you don't have one already
 ```python
 mainkey = Enc.genkey()
 ```
 2) Before encrypting or decrypting anything, first set the arguments you want to pass, you can have an encrypted message or a  decrypted message , and a mainkey to use.
-<br>Set the correct mainkey ( 64 byte long key ) 
+<br>Set the correct mainkey ( 32 byte long key ) 
 ```python
 mainkey = '6ce113be19e898c2b98df82b7fa8efb166928925fc05574a54eb1114c3410900'
 ```
 The message can be of type string or bytes.
 <br>Normal string message :  
 ```python 
 message = 'Hello There'
 ```
 or a normal bytes message 
 ```python
 message = b'Hello There'
 ```
-or string URL safe encrypted message : 
+or string URL safe encrypted message ( to decrypt ): 
 ```python
 message = 'ZEfikRiNQ4EE1y5E-Qn4gQbo8goVpWLPstqTlgWtoRq1CK_oeMz4oelCYNpM-NZyzSIKk7DazkAUO9HcZJzWWMXR6zqRjNTN-c1Q6vRWSkj1g20oL6JbzUvEJL3xvY2-Fye1simoOAr7YP5YHAnSYAAAADIA0juak_JYQnzXQ-apJ8azahvngigFrHRg142g7OqvfA=='
 ```
-or bytes type encrypted message 
+or bytes type encrypted message ( to decrypt ):
 ```python
 message = b'dG\xe2\x91\x18\x8dC\x81\x04\xd7.D\xf9\t\xf8\x81\x06\xe8\xf2\n\x15\xa5b\xcf\xb2\xda\x93\x96\x05\xad\xa1\x1a\xb5\x08\xaf\xe8x\xcc\xf8\xa1\xe9B`\xdaL\xf8\xd6r\xcd"\n\x93\xb0\xda\xce@\x14;\xd1\xdcd\x9c\xd6X\xc5\xd1\xeb:\x91\x8c\xd4\xcd\xf9\xcdP\xea\xf4VJH\xf5\x83m(/\xa2[\xcdK\xc4$\xbd\xf1\xbd\x8d\xbe\x17\'\xb5\xb2)\xa88\n\xfb`\xfeX\x1c\t\xd2`\x00\x00\x002\x00\xd2;\x9a\x93\xf2XB|\xd7C\xe6\xa9\'\xc6\xb3j\x1b\xe7\x82(\x05\xact`\xd7\x8d\xa0\xec\xea\xaf|'
 ```
 3) Now pass the arguments accordingly. If you have a normal message and you try to decrypt it, an Exception will be raised so pass the arguments to the right classes. 
 <br><br>So first create an instance of either the `Enc` or `Dec` class. 
 <br>Here I chose to encrypt a message 
 ```python
@@ -158,22 +157,23 @@
 ```python
 output = instanceE.enc_to_bytes()
 ```
 you can also encrypt to a URL safe string
 ```python
 output = instanceE.enc_to_str()
 ```
+<br> The same logic applies to the decryption process simply switch `Enc` with `Dec` and `enc_to_bytes` to `dec_to_bytes`
 That simple, that's it.
 
 
 
 
 ## Features ## 
 - AES 256 CBC mode 
-- Generates a randomly secure 256 Bit main key 
+- Generates a randomly secure 256-bit main key 
 - Derives the HMAC and the AES key from the mainkey using bcrypt's KDFs with a configurable number of iterations with :
     - Salt : Random 128 bit value is generated  each time and passed to the KDF to generate the AES key
     - Pepper : Random 128 bit value is generated  each time and passed to the KDF to generate the HMAC
 - AES Key : 256 bit
 - HMAC : 256 bit hashed using SHA512
 - Generates a random 128 bit Initialization Vector (IV) each time for the Cipher
 - PKCS7 message padding
@@ -182,15 +182,15 @@
 - No need to manipulate the input to fit, it accepts strings or bytes you can pass them right away
 - You can get a string or a bytes representation of either the encryption or the decryption result
 - In `crypt` module the key is flexible it doesn't have to be 256 bit long, it can actually be of any length but that's up to you to ensure its security, or leave it as is and use the key generation function to get secure and random keys ( although in `textcrypt` and `filecrypt` you have to use a 256 bit long key )
 - Encrypting to a string has URL-safe string representation 
 ### Regarding KDFs
 Note that bcrypt is intentionally slow and computationally expensive, enhancing protection against brute-force attacks. The number of iterations, including salt and pepper, increases derivation time to strike a balance between security and performance. Use a suitable value based on your machine's capabilities and desired security level.
 <br>Im using 50 just to demonstrate the process and make it quick.
-<br>The bare minimum is 50, the max is 100 000, choose somewhere in between.
+<br>The bare minimum is 50 ( which is secure enough ), the max is 100 000, choose somewhere in between.
 <br>In my use case 50 takes around 0.5 secs while using the maximum number of iterations takes around 11 minutes to derive the keys and finish the cryptographic operations at hand.
 <br>You can check how it works by checking this [Jupyter Notebook](demo/performance-check.ipynb) demo file
 ## AshCryptGUI ##
 The GUI as mentioned above is a fully functional application , you can use it to encrypt files , texts , keep track of files by storing them on demand to a main database , also on demand it can keep track of the keys used for cryptographic operations.
 ### Usage ###
 1) Set the main key up. If you don't have one , press on the button `generate` to generate a secure safe key ready for use. Then insert it in the `MAINKEY` entry
 2) Now you're able to encrypt files or text (text is limited to 200 characters max)
```

### Comparing `AshCrypt-3.0.0/setup.py` & `AshCrypt-3.0.1/setup.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,29 +1,29 @@
-from setuptools import setup , find_packages
+from setuptools import setup, find_packages
 
-with open('AshCrypt/README.md','r') as f:
+with open('AshCrypt/README.md', 'r') as f:
     readme = f.read()
 
 setup(
     name='AshCrypt',
-    version='3.0.0',
+    version='3.0.1',
     author='Ashref Gwader',
     author_email='AshrefGw@proton.me',
     python_requires='>=3.7',
-    description="Comprehensive AES-256 Cryptography App & library equipped with files & text handling modules along with"
-                " a database module to store encrypted content.",
+    description="Comprehensive AES-256 Cryptography App & library equipped with files & text handling modules along"
+                " with a database module to store encrypted content.",
     long_description_content_type='text/markdown',
     long_description=readme,
     url='https://github.com/AshGw/AES-256.git',
-    packages=find_packages(exclude=['important', 'Docker-build','.github','Executables','demo']),
+    packages=find_packages(exclude=['important', 'Docker-build', '.github', 'Executables', 'demo']),
     package_data={
         'AshCrypt': ['**'],
     },
     exclude_package_data={
-        '': ['.gitignore','LICENSE','README'],
+        '': ['.gitignore', 'LICENSE', 'README'],
     },
     install_requires=[
         'bcrypt==4.0.1',
         'cryptography==40.0.2',
         'qrcode==7.4.2',
         'ttkbootstrap==1.10.1',
     ],
@@ -41,8 +41,8 @@
         'Programming Language :: Python :: 3.11',
     ],
     keywords=[
         'Cryptography application',
         'cryptography library'
         'AES-256',
     ],
-)
+)
```

