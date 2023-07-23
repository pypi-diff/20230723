# Comparing `tmp/stability_matrix_tools-0.1.9.tar.gz` & `tmp/stability_matrix_tools-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "stability_matrix_tools-0.1.9.tar", max compression
+gzip compressed data, was "stability_matrix_tools-0.2.0.tar", max compression
```

## Comparing `stability_matrix_tools-0.1.9.tar` & `stability_matrix_tools-0.2.0.tar`

### file list

```diff
@@ -1,21 +1,21 @@
--rw-r--r--   0        0        0    35163 2023-06-30 22:15:25.032480 stability_matrix_tools-0.1.9/LICENSE
--rw-r--r--   0        0        0      632 2023-07-02 05:05:03.292780 stability_matrix_tools-0.1.9/pyproject.toml
--rw-r--r--   0        0        0       47 2023-06-30 22:15:24.995957 stability_matrix_tools-0.1.9/README.md
--rw-r--r--   0        0        0        0 2023-06-30 19:14:24.481835 stability_matrix_tools-0.1.9/src/stability_matrix_tools/__init__.py
--rw-r--r--   0        0        0     2329 2023-07-01 03:50:14.086249 stability_matrix_tools-0.1.9/src/stability_matrix_tools/b2.py
--rw-r--r--   0        0        0      380 2023-07-01 04:29:55.594056 stability_matrix_tools-0.1.9/src/stability_matrix_tools/cf.py
--rw-r--r--   0        0        0     3068 2023-07-01 07:09:28.831003 stability_matrix_tools-0.1.9/src/stability_matrix_tools/keys.py
--rw-r--r--   0        0        0      245 2023-07-01 06:42:59.756522 stability_matrix_tools-0.1.9/src/stability_matrix_tools/main.py
--rw-r--r--   0        0        0        0 2023-06-30 19:29:16.679181 stability_matrix_tools-0.1.9/src/stability_matrix_tools/models/__init__.py
--rw-r--r--   0        0        0      518 2023-07-01 03:35:42.001028 stability_matrix_tools-0.1.9/src/stability_matrix_tools/models/settings.py
--rw-r--r--   0        0        0     1529 2023-07-02 05:02:18.271653 stability_matrix_tools-0.1.9/src/stability_matrix_tools/models/update_info.py
--rw-r--r--   0        0        0      325 2023-06-30 21:06:10.076637 stability_matrix_tools-0.1.9/src/stability_matrix_tools/models/version.py
--rw-r--r--   0        0        0     5386 2023-07-02 05:05:03.290781 stability_matrix_tools-0.1.9/src/stability_matrix_tools/updates.py
--rw-r--r--   0        0        0        0 2023-07-01 02:42:39.117279 stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/__init__.py
--rw-r--r--   0        0        0      588 2023-07-01 04:29:34.632450 stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/cf_cache.py
--rw-r--r--   0        0        0     1634 2023-06-30 21:18:44.596055 stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/progress.py
--rw-r--r--   0        0        0     1948 2023-07-01 06:57:32.338302 stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/signing.py
--rw-r--r--   0        0        0      709 2023-07-01 08:56:22.308456 stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/stream_hash.py
--rw-r--r--   0        0        0     2051 2023-07-01 08:34:51.103754 stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/uploader.py
--rw-r--r--   0        0        0     1162 1970-01-01 00:00:00.000000 stability_matrix_tools-0.1.9/setup.py
--rw-r--r--   0        0        0      811 1970-01-01 00:00:00.000000 stability_matrix_tools-0.1.9/PKG-INFO
+-rw-r--r--   0        0        0    35163 2023-06-30 22:15:25.032480 stability_matrix_tools-0.2.0/LICENSE
+-rw-r--r--   0        0        0      634 2023-07-23 18:48:14.440974 stability_matrix_tools-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0       47 2023-06-30 22:15:24.995957 stability_matrix_tools-0.2.0/README.md
+-rw-r--r--   0        0        0        0 2023-06-30 19:14:24.481835 stability_matrix_tools-0.2.0/src/stability_matrix_tools/__init__.py
+-rw-r--r--   0        0        0     2329 2023-07-01 03:50:14.086249 stability_matrix_tools-0.2.0/src/stability_matrix_tools/b2.py
+-rw-r--r--   0        0        0      380 2023-07-01 04:29:55.594056 stability_matrix_tools-0.2.0/src/stability_matrix_tools/cf.py
+-rw-r--r--   0        0        0     3394 2023-07-02 06:18:20.084545 stability_matrix_tools-0.2.0/src/stability_matrix_tools/keys.py
+-rw-r--r--   0        0        0      245 2023-07-01 06:42:59.756522 stability_matrix_tools-0.2.0/src/stability_matrix_tools/main.py
+-rw-r--r--   0        0        0        0 2023-06-30 19:29:16.679181 stability_matrix_tools-0.2.0/src/stability_matrix_tools/models/__init__.py
+-rw-r--r--   0        0        0      518 2023-07-01 03:35:42.001028 stability_matrix_tools-0.2.0/src/stability_matrix_tools/models/settings.py
+-rw-r--r--   0        0        0     1717 2023-07-23 07:50:17.828531 stability_matrix_tools-0.2.0/src/stability_matrix_tools/models/update_info.py
+-rw-r--r--   0        0        0      325 2023-06-30 21:06:10.076637 stability_matrix_tools-0.2.0/src/stability_matrix_tools/models/version.py
+-rw-r--r--   0        0        0     7706 2023-07-23 18:47:42.841536 stability_matrix_tools-0.2.0/src/stability_matrix_tools/updates.py
+-rw-r--r--   0        0        0        0 2023-07-01 02:42:39.117279 stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/__init__.py
+-rw-r--r--   0        0        0      588 2023-07-01 04:29:34.632450 stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/cf_cache.py
+-rw-r--r--   0        0        0     1634 2023-06-30 21:18:44.596055 stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/progress.py
+-rw-r--r--   0        0        0     2182 2023-07-02 06:18:20.086547 stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/signing.py
+-rw-r--r--   0        0        0      709 2023-07-01 08:56:22.308456 stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/stream_hash.py
+-rw-r--r--   0        0        0     2051 2023-07-01 08:34:51.103754 stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/uploader.py
+-rw-r--r--   0        0        0     1166 1970-01-01 00:00:00.000000 stability_matrix_tools-0.2.0/setup.py
+-rw-r--r--   0        0        0      815 1970-01-01 00:00:00.000000 stability_matrix_tools-0.2.0/PKG-INFO
```

### Comparing `stability_matrix_tools-0.1.9/LICENSE` & `stability_matrix_tools-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `stability_matrix_tools-0.1.9/pyproject.toml` & `stability_matrix_tools-0.2.0/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 [tool.poetry]
 name = "stability-matrix-tools"
-version = "0.1.9"
+version = "0.2.0"
 description = ""
 authors = ["Ionite <dev@ionite.io>"]
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = ">=3.10, <3.12"
 typer = {extras = ["all"], version = "^0.9.0"}
-pydantic = {extras = ["dotenv"], version = "^2.0"}
+pydantic = {extras = ["dotenv"], version = "^2.0.1"}
 semver = "^3.0.1"
 httpx = "^0.24.1"
 b2sdk = "^1.21.0"
 python-dotenv = "^1.0.0"
 cryptography = "^41.0.1"
 keyring = "^24.2.0"
 pyperclip = "^1.8.2"
```

### Comparing `stability_matrix_tools-0.1.9/src/stability_matrix_tools/b2.py` & `stability_matrix_tools-0.2.0/src/stability_matrix_tools/b2.py`

 * *Files identical despite different names*

### Comparing `stability_matrix_tools-0.1.9/src/stability_matrix_tools/keys.py` & `stability_matrix_tools-0.2.0/src/stability_matrix_tools/keys.py`

 * *Files 3% similar despite different names*

```diff
@@ -46,24 +46,31 @@
 
     ssh_key = signing.private_key_to_ssh(private_key)
     pyperclip.copy(ssh_key)
     cp("✅  Private key copied to clipboard.")
 
 
 @app.command()
-def get_public():
+def get_public(key_format: Annotated[str, Option("--format")] = "openssh"):
     """Loads current public key to clipboard."""
     public_key = signing.get_public_key_keyring()
     if not public_key:
         cp("❌  Private key not found.")
         raise SystemExit(1)
 
-    ssh_pub_key = signing.public_key_to_ssh(public_key)
-    pyperclip.copy(ssh_pub_key)
-    cp(ssh_pub_key)
+    if key_format == "openssh":
+        pub_key = signing.public_key_to_ssh(public_key)
+    elif key_format == "b64":
+        pub_key_bytes = signing.public_key_to_bytes(public_key)
+        pub_key = base64.b64encode(pub_key_bytes).decode("utf-8")
+    else:
+        cp("❌  Invalid key format.")
+        raise SystemExit(1)
+    pyperclip.copy(pub_key)
+    cp(pub_key)
     cp("✅  Public key copied to clipboard.")
 
 
 @app.command()
 def sign(message: str):
     """Sign a message with the current private key. Produces base64 signature."""
     private_key = signing.get_private_key_keyring()
```

### Comparing `stability_matrix_tools-0.1.9/src/stability_matrix_tools/models/settings.py` & `stability_matrix_tools-0.2.0/src/stability_matrix_tools/models/settings.py`

 * *Files identical despite different names*

### Comparing `stability_matrix_tools-0.1.9/src/stability_matrix_tools/models/update_info.py` & `stability_matrix_tools-0.2.0/src/stability_matrix_tools/models/update_info.py`

 * *Files 12% similar despite different names*

```diff
@@ -50,7 +50,13 @@
 
     @field_serializer("release_date")
     def serialize_dt(self, dt: datetime, _info):
         return dt.replace(tzinfo=timezone.utc).isoformat()
 
     class Config:
         arbitrary_types_allowed = True
+
+
+class UpdateCollection(BaseModel):
+    win_x64: UpdateInfo | None = Field(alias="win-x64", default=None)
+    linux_x64: UpdateInfo | None = Field(alias="linux-x64", default=None)
+
```

### Comparing `stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/cf_cache.py` & `stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/cf_cache.py`

 * *Files identical despite different names*

### Comparing `stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/progress.py` & `stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/progress.py`

 * *Files identical despite different names*

### Comparing `stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/signing.py` & `stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/signing.py`

 * *Files 13% similar despite different names*

```diff
@@ -21,14 +21,22 @@
     key_bytes = public_key.public_bytes(
         encoding=serialization.Encoding.OpenSSH,
         format=serialization.PublicFormat.OpenSSH,
     )
     return key_bytes.decode("utf-8")
 
 
+def public_key_to_bytes(public_key: Ed25519PublicKey) -> bytes:
+    key_bytes = public_key.public_bytes(
+        encoding=serialization.Encoding.Raw,
+        format=serialization.PublicFormat.Raw,
+    )
+    return key_bytes
+
+
 def ssh_to_key(key: str) -> Ed25519PrivateKey:
     key_bytes = key.encode("utf-8")
     return serialization.load_ssh_private_key(key_bytes, None)
 
 
 def get_private_key_keyring() -> Ed25519PrivateKey | None:
     """Get the private key from the keyring."""
```

### Comparing `stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/stream_hash.py` & `stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/stream_hash.py`

 * *Files identical despite different names*

### Comparing `stability_matrix_tools-0.1.9/src/stability_matrix_tools/utils/uploader.py` & `stability_matrix_tools-0.2.0/src/stability_matrix_tools/utils/uploader.py`

 * *Files identical despite different names*

### Comparing `stability_matrix_tools-0.1.9/setup.py` & `stability_matrix_tools-0.2.0/setup.py`

 * *Files 16% similar despite different names*

```diff
@@ -14,26 +14,26 @@
 
 install_requires = \
 ['b2sdk>=1.21.0,<2.0.0',
  'blake3>=0.3.3,<0.4.0',
  'cryptography>=41.0.1,<42.0.0',
  'httpx>=0.24.1,<0.25.0',
  'keyring>=24.2.0,<25.0.0',
- 'pydantic[dotenv]>=2.0,<3.0',
+ 'pydantic[dotenv]>=2.0.1,<3.0.0',
  'pyperclip>=1.8.2,<2.0.0',
  'python-dotenv>=1.0.0,<2.0.0',
  'semver>=3.0.1,<4.0.0',
  'typer[all]>=0.9.0,<0.10.0']
 
 entry_points = \
 {'console_scripts': ['sm-tools = stability_matrix_tools.main:app']}
 
 setup_kwargs = {
     'name': 'stability-matrix-tools',
-    'version': '0.1.9',
+    'version': '0.2.0',
     'description': '',
     'long_description': '# sm-tools\n Stability Matrix development tools\n',
     'author': 'Ionite',
     'author_email': 'dev@ionite.io',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
```

### Comparing `stability_matrix_tools-0.1.9/PKG-INFO` & `stability_matrix_tools-0.2.0/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 Metadata-Version: 2.1
 Name: stability-matrix-tools
-Version: 0.1.9
+Version: 0.2.0
 Summary: 
 Author: Ionite
 Author-email: dev@ionite.io
 Requires-Python: >=3.10,<3.12
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: b2sdk (>=1.21.0,<2.0.0)
 Requires-Dist: blake3 (>=0.3.3,<0.4.0)
 Requires-Dist: cryptography (>=41.0.1,<42.0.0)
 Requires-Dist: httpx (>=0.24.1,<0.25.0)
 Requires-Dist: keyring (>=24.2.0,<25.0.0)
-Requires-Dist: pydantic[dotenv] (>=2.0,<3.0)
+Requires-Dist: pydantic[dotenv] (>=2.0.1,<3.0.0)
 Requires-Dist: pyperclip (>=1.8.2,<2.0.0)
 Requires-Dist: python-dotenv (>=1.0.0,<2.0.0)
 Requires-Dist: semver (>=3.0.1,<4.0.0)
 Requires-Dist: typer[all] (>=0.9.0,<0.10.0)
 Description-Content-Type: text/markdown
 
 # sm-tools
```

