# Comparing `tmp/ubox-0.0.1.4.tar.gz` & `tmp/ubox-0.0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ubox-0.0.1.4.tar", last modified: Sat Jul 22 13:53:16 2023, max compression
+gzip compressed data, was "ubox-0.0.1.5.tar", last modified: Sun Jul 23 00:32:22 2023, max compression
```

## Comparing `ubox-0.0.1.4.tar` & `ubox-0.0.1.5.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 tek        (501) staff       (20)        0 2023-07-22 13:53:16.010302 ubox-0.0.1.4/
--rw-r--r--   0 tek        (501) staff       (20)     1060 2023-07-22 12:39:24.000000 ubox-0.0.1.4/LICENSE
--rw-r--r--   0 tek        (501) staff       (20)      536 2023-07-22 13:53:16.010052 ubox-0.0.1.4/PKG-INFO
--rw-r--r--   0 tek        (501) staff       (20)       25 2023-07-22 12:44:39.000000 ubox-0.0.1.4/README.md
--rw-r--r--   0 tek        (501) staff       (20)       38 2023-07-22 13:53:16.010378 ubox-0.0.1.4/setup.cfg
--rw-r--r--   0 tek        (501) staff       (20)     1218 2023-07-22 13:53:12.000000 ubox-0.0.1.4/setup.py
-drwxr-xr-x   0 tek        (501) staff       (20)        0 2023-07-22 13:53:16.007906 ubox-0.0.1.4/ubox/
--rw-r--r--   0 tek        (501) staff       (20)      201 2023-07-22 13:52:38.000000 ubox-0.0.1.4/ubox/__init__.py
--rw-r--r--   0 tek        (501) staff       (20)     1643 2023-07-22 12:50:59.000000 ubox-0.0.1.4/ubox/crypto.py
--rw-r--r--   0 tek        (501) staff       (20)      793 2023-07-22 13:03:05.000000 ubox-0.0.1.4/ubox/identifiers.py
--rw-r--r--   0 tek        (501) staff       (20)      721 2023-07-22 13:53:01.000000 ubox-0.0.1.4/ubox/random.py
-drwxr-xr-x   0 tek        (501) staff       (20)        0 2023-07-22 13:53:16.009659 ubox-0.0.1.4/ubox.egg-info/
--rw-r--r--   0 tek        (501) staff       (20)      536 2023-07-22 13:53:15.000000 ubox-0.0.1.4/ubox.egg-info/PKG-INFO
--rw-r--r--   0 tek        (501) staff       (20)      205 2023-07-22 13:53:15.000000 ubox-0.0.1.4/ubox.egg-info/SOURCES.txt
--rw-r--r--   0 tek        (501) staff       (20)        1 2023-07-22 13:53:15.000000 ubox-0.0.1.4/ubox.egg-info/dependency_links.txt
--rw-r--r--   0 tek        (501) staff       (20)        5 2023-07-22 13:53:15.000000 ubox-0.0.1.4/ubox.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 00:32:22.926906 ubox-0.0.1.5/
+-rw-rw-rw-   0        0        0     1081 2023-07-23 00:28:21.000000 ubox-0.0.1.5/LICENSE
+-rw-rw-rw-   0        0        0      556 2023-07-23 00:32:22.925930 ubox-0.0.1.5/PKG-INFO
+-rw-rw-rw-   0        0        0       27 2023-07-23 00:28:21.000000 ubox-0.0.1.5/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 00:32:22.927881 ubox-0.0.1.5/setup.cfg
+-rw-rw-rw-   0        0        0     1250 2023-07-23 00:30:27.000000 ubox-0.0.1.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:32:22.895673 ubox-0.0.1.5/ubox/
+-rw-rw-rw-   0        0        0      261 2023-07-23 00:30:16.000000 ubox-0.0.1.5/ubox/__init__.py
+-rw-rw-rw-   0        0        0     1713 2023-07-23 00:28:21.000000 ubox-0.0.1.5/ubox/crypto.py
+-rw-rw-rw-   0        0        0      822 2023-07-23 00:28:21.000000 ubox-0.0.1.5/ubox/identifiers.py
+-rw-rw-rw-   0        0        0      747 2023-07-23 00:28:21.000000 ubox-0.0.1.5/ubox/random.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:32:22.923977 ubox-0.0.1.5/ubox.egg-info/
+-rw-rw-rw-   0        0        0      556 2023-07-23 00:32:22.000000 ubox-0.0.1.5/ubox.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      205 2023-07-23 00:32:22.000000 ubox-0.0.1.5/ubox.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 00:32:22.000000 ubox-0.0.1.5/ubox.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        5 2023-07-23 00:32:22.000000 ubox-0.0.1.5/ubox.egg-info/top_level.txt
```

### Comparing `ubox-0.0.1.4/LICENSE` & `ubox-0.0.1.5/LICENSE`

 * *Ordering differences only*

 * *Files 20% similar despite different names*

```diff
@@ -1,21 +1,21 @@
-MIT License
-
-Copyright (c) 2023 abc
-
-Permission is hereby granted, free of charge, to any person obtaining a copy
-of this software and associated documentation files (the "Software"), to deal
-in the Software without restriction, including without limitation the rights
-to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
-copies of the Software, and to permit persons to whom the Software is
-furnished to do so, subject to the following conditions:
-
-The above copyright notice and this permission notice shall be included in all
-copies or substantial portions of the Software.
-
-THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
-IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
-FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
-AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
-LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
-OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
-SOFTWARE.
+MIT License
+
+Copyright (c) 2023 abc
+
+Permission is hereby granted, free of charge, to any person obtaining a copy
+of this software and associated documentation files (the "Software"), to deal
+in the Software without restriction, including without limitation the rights
+to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+copies of the Software, and to permit persons to whom the Software is
+furnished to do so, subject to the following conditions:
+
+The above copyright notice and this permission notice shall be included in all
+copies or substantial portions of the Software.
+
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+SOFTWARE.
```

### Comparing `ubox-0.0.1.4/PKG-INFO` & `ubox-0.0.1.5/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,18 +1,18 @@
-Metadata-Version: 2.1
-Name: ubox
-Version: 0.0.1.4
-Summary: Python Utils Box for Botting/Spoofing (encryption, random, etc)
-Author: Tekky
-Author-email: <support@g4f.ai>
-Classifier: Development Status :: 2 - Pre-Alpha
-Classifier: Intended Audience :: Developers
-Classifier: Programming Language :: Python :: 3
-Classifier: Operating System :: Unix
-Classifier: Operating System :: MacOS :: MacOS X
-Classifier: Operating System :: Microsoft :: Windows
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
-
-# ubox
- Python Utils Box
+Metadata-Version: 2.1
+Name: ubox
+Version: 0.0.1.5
+Summary: Python Utils Box for Botting/Spoofing (encryption, random, etc)
+Author: Tekky
+Author-email: <support@g4f.ai>
+Classifier: Development Status :: 2 - Pre-Alpha
+Classifier: Intended Audience :: Developers
+Classifier: Programming Language :: Python :: 3
+Classifier: Operating System :: Unix
+Classifier: Operating System :: MacOS :: MacOS X
+Classifier: Operating System :: Microsoft :: Windows
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
+
+# ubox
+ Python Utils Box
```

### Comparing `ubox-0.0.1.4/ubox/crypto.py` & `ubox-0.0.1.5/ubox/crypto.py`

 * *Ordering differences only*

 * *Files 20% similar despite different names*

```diff
@@ -1,71 +1,71 @@
-import base64
-import hashlib
-
-# base64
-def b64enc(data: bytes) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-
-    return base64.b64encode(data).decode('utf-8')
-
-def b64dec(data: str) -> bytes:
-    return base64.b64decode(data).decode('utf-8')
-
-def b64encb(data: bytes) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-
-    return base64.b64encode(data)
-
-def b64decb(data: str) -> bytes:
-    return base64.b64decode(data)
-
-#sha
-
-def sha256(data: bytes) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-    
-    return hashlib.sha256(data).hexdigest()
-
-def sha256b(data: str) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-        
-    return hashlib.sha256(data).digest()
-
-def sha512(data: bytes) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-    
-    return hashlib.sha512(data).hexdigest()
-
-def sha512b(data: str) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-        
-    return hashlib.sha512(data).digest()
-
-def sha1(data: bytes) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-    
-    return hashlib.sha1(data).hexdigest()
-
-def sha1b(data: str) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-        
-    return hashlib.sha1(data).digest()
-
-def md5(data: bytes) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-    
-    return hashlib.md5(data).hexdigest()
-
-def md5b(data: str) -> str:
-    if isinstance(data, str):
-        data = data.encode('utf-8')
-        
+import base64
+import hashlib
+
+# base64
+def b64enc(data: bytes) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+
+    return base64.b64encode(data).decode('utf-8')
+
+def b64dec(data: str) -> bytes:
+    return base64.b64decode(data).decode('utf-8')
+
+def b64encb(data: bytes) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+
+    return base64.b64encode(data)
+
+def b64decb(data: str) -> bytes:
+    return base64.b64decode(data)
+
+#sha
+
+def sha256(data: bytes) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+    
+    return hashlib.sha256(data).hexdigest()
+
+def sha256b(data: str) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+        
+    return hashlib.sha256(data).digest()
+
+def sha512(data: bytes) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+    
+    return hashlib.sha512(data).hexdigest()
+
+def sha512b(data: str) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+        
+    return hashlib.sha512(data).digest()
+
+def sha1(data: bytes) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+    
+    return hashlib.sha1(data).hexdigest()
+
+def sha1b(data: str) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+        
+    return hashlib.sha1(data).digest()
+
+def md5(data: bytes) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+    
+    return hashlib.md5(data).hexdigest()
+
+def md5b(data: str) -> str:
+    if isinstance(data, str):
+        data = data.encode('utf-8')
+        
     return hashlib.md5(data).digest()
```

### Comparing `ubox-0.0.1.4/ubox/identifiers.py` & `ubox-0.0.1.5/ubox/identifiers.py`

 * *Ordering differences only*

 * *Files 24% similar despite different names*

```diff
@@ -1,30 +1,30 @@
-import uuid, random
-
-def uuid1():
-    return str(uuid.uuid1())
-
-def uuid3():
-    return str(uuid.uuid3())
-
-def uuid5():
-    return str(uuid.uuid5())
-
-def uuid4():
-    return str(uuid.uuid4())
-
-def imei():
-    def checksum(number, alphabet='0123456789'):
-        n = len(alphabet)
-        number = tuple(alphabet.index(i)
-                    for i in reversed(str(number)))
-        return (sum(number[::2]) +
-                sum(sum(divmod(i * 2, n))
-                    for i in number[1::2])) % n
-
-    def calc_check_digit(number, alphabet='0123456789'):
-        """Calculate the extra digit."""
-        check_digit = checksum(number + alphabet[0])
-        return alphabet[-check_digit]
-    
-    imei = '99001201' + str(random.randint(000000, 999999))
+import uuid, random
+
+def uuid1():
+    return str(uuid.uuid1())
+
+def uuid3():
+    return str(uuid.uuid3())
+
+def uuid5():
+    return str(uuid.uuid5())
+
+def uuid4():
+    return str(uuid.uuid4())
+
+def imei():
+    def checksum(number, alphabet='0123456789'):
+        n = len(alphabet)
+        number = tuple(alphabet.index(i)
+                    for i in reversed(str(number)))
+        return (sum(number[::2]) +
+                sum(sum(divmod(i * 2, n))
+                    for i in number[1::2])) % n
+
+    def calc_check_digit(number, alphabet='0123456789'):
+        """Calculate the extra digit."""
+        check_digit = checksum(number + alphabet[0])
+        return alphabet[-check_digit]
+    
+    imei = '99001201' + str(random.randint(000000, 999999))
     return imei + calc_check_digit(imei)
```

### Comparing `ubox-0.0.1.4/ubox/random.py` & `ubox-0.0.1.5/ubox/random.py`

 * *Ordering differences only*

 * *Files 19% similar despite different names*

```diff
@@ -1,27 +1,27 @@
-import os
-import string
-import random
-
-def ranhex(length) -> str:
-    return os.urandom(length).hex()
-
-def ranstr(length, charset = (string.ascii_letters + string.digits)) -> str:
-    return ''.join(random.choices(charset, k=length))
-
-def ranint(minimum: int, maximum: int) -> int:
-    return random.randint(minimum, maximum)
-
-def rhex(length: int) -> str:
-    return ranhex(length)
-
-def rstr(length: int, charset: str = (string.ascii_letters + string.digits)) -> str:
-    return ranstr(length, charset)
-
-def rint(minimum: int, maximum: int) -> int:
-    return random.randint(minimum, maximum)
-
-def rbytes(length: int) -> bytes:
-    return os.urandom(length)
-
-def ranbytes(length: int) -> bytes:
+import os
+import string
+import random
+
+def ranhex(length) -> str:
+    return os.urandom(length).hex()
+
+def ranstr(length, charset = (string.ascii_letters + string.digits)) -> str:
+    return ''.join(random.choices(charset, k=length))
+
+def ranint(minimum: int, maximum: int) -> int:
+    return random.randint(minimum, maximum)
+
+def rhex(length: int) -> str:
+    return ranhex(length)
+
+def rstr(length: int, charset: str = (string.ascii_letters + string.digits)) -> str:
+    return ranstr(length, charset)
+
+def rint(minimum: int, maximum: int) -> int:
+    return random.randint(minimum, maximum)
+
+def rbytes(length: int) -> bytes:
+    return os.urandom(length)
+
+def ranbytes(length: int) -> bytes:
     return rbytes(length)
```

### Comparing `ubox-0.0.1.4/ubox.egg-info/PKG-INFO` & `ubox-0.0.1.5/ubox.egg-info/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,18 +1,18 @@
-Metadata-Version: 2.1
-Name: ubox
-Version: 0.0.1.4
-Summary: Python Utils Box for Botting/Spoofing (encryption, random, etc)
-Author: Tekky
-Author-email: <support@g4f.ai>
-Classifier: Development Status :: 2 - Pre-Alpha
-Classifier: Intended Audience :: Developers
-Classifier: Programming Language :: Python :: 3
-Classifier: Operating System :: Unix
-Classifier: Operating System :: MacOS :: MacOS X
-Classifier: Operating System :: Microsoft :: Windows
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
-
-# ubox
- Python Utils Box
+Metadata-Version: 2.1
+Name: ubox
+Version: 0.0.1.5
+Summary: Python Utils Box for Botting/Spoofing (encryption, random, etc)
+Author: Tekky
+Author-email: <support@g4f.ai>
+Classifier: Development Status :: 2 - Pre-Alpha
+Classifier: Intended Audience :: Developers
+Classifier: Programming Language :: Python :: 3
+Classifier: Operating System :: Unix
+Classifier: Operating System :: MacOS :: MacOS X
+Classifier: Operating System :: Microsoft :: Windows
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
+
+# ubox
+ Python Utils Box
```

