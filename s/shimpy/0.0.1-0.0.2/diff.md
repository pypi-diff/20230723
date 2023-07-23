# Comparing `tmp/shimpy-0.0.1.tar.gz` & `tmp/shimpy-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "shimpy-0.0.1.tar", max compression
+gzip compressed data, was "shimpy-0.0.2.tar", max compression
```

## Comparing `shimpy-0.0.1.tar` & `shimpy-0.0.2.tar`

### file list

```diff
@@ -1,15 +1,17 @@
--rw-r--r--   0        0        0     1060 2023-07-20 13:07:56.973570 shimpy-0.0.1/LICENSE
--rw-r--r--   0        0        0      590 2023-07-20 16:52:57.302076 shimpy-0.0.1/README.md
--rw-r--r--   0        0        0      519 2023-07-21 12:32:29.521991 shimpy-0.0.1/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-20 13:41:17.460780 shimpy-0.0.1/shimpy/__init__.py
--rw-r--r--   0        0        0        0 2023-07-20 14:08:03.269569 shimpy-0.0.1/shimpy/account/__init__.py
--rw-r--r--   0        0        0     1381 2023-07-21 20:40:52.669451 shimpy-0.0.1/shimpy/account/commands.py
--rw-r--r--   0        0        0        0 2023-07-20 14:08:23.814076 shimpy-0.0.1/shimpy/address/__init__.py
--rw-r--r--   0        0        0     1182 2023-07-21 20:45:33.778576 shimpy-0.0.1/shimpy/address/commands.py
--rw-r--r--   0        0        0      373 2023-07-20 16:53:18.915292 shimpy-0.0.1/shimpy/cli.py
--rw-r--r--   0        0        0        0 2023-07-20 16:53:25.716211 shimpy-0.0.1/shimpy/nft/__init__.py
--rw-r--r--   0        0        0     1596 2023-07-21 20:57:12.805001 shimpy-0.0.1/shimpy/nft/commands.py
--rw-r--r--   0        0        0        0 2023-07-20 14:26:14.288929 shimpy-0.0.1/shimpy/node/__init__.py
--rw-r--r--   0        0        0      281 2023-07-20 14:38:35.363075 shimpy-0.0.1/shimpy/node/commands.py
--rw-r--r--   0        0        0     1473 1970-01-01 00:00:00.000000 shimpy-0.0.1/setup.py
--rw-r--r--   0        0        0     1101 1970-01-01 00:00:00.000000 shimpy-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0     1060 2023-07-20 13:07:56.973570 shimpy-0.0.2/LICENSE
+-rw-r--r--   0        0        0      621 2023-07-23 20:43:37.263875 shimpy-0.0.2/README.md
+-rw-r--r--   0        0        0      519 2023-07-23 20:43:42.113092 shimpy-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-20 13:41:17.460780 shimpy-0.0.2/shimpy/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-20 14:08:03.269569 shimpy-0.0.2/shimpy/account/__init__.py
+-rw-r--r--   0        0        0     1381 2023-07-21 20:40:52.669451 shimpy-0.0.2/shimpy/account/commands.py
+-rw-r--r--   0        0        0        0 2023-07-20 14:08:23.814076 shimpy-0.0.2/shimpy/address/__init__.py
+-rw-r--r--   0        0        0     1182 2023-07-21 20:45:33.778576 shimpy-0.0.2/shimpy/address/commands.py
+-rw-r--r--   0        0        0      462 2023-07-23 20:41:26.224432 shimpy-0.0.2/shimpy/cli.py
+-rw-r--r--   0        0        0        0 2023-07-20 16:53:25.716211 shimpy-0.0.2/shimpy/nft/__init__.py
+-rw-r--r--   0        0        0     1596 2023-07-21 20:57:12.805001 shimpy-0.0.2/shimpy/nft/commands.py
+-rw-r--r--   0        0        0        0 2023-07-20 14:26:14.288929 shimpy-0.0.2/shimpy/node/__init__.py
+-rw-r--r--   0        0        0      281 2023-07-20 14:38:35.363075 shimpy-0.0.2/shimpy/node/commands.py
+-rw-r--r--   0        0        0        0 2023-07-23 20:39:50.400318 shimpy-0.0.2/shimpy/transactions/__init__.py
+-rw-r--r--   0        0        0     1046 2023-07-23 20:42:24.490598 shimpy-0.0.2/shimpy/transactions/commands.py
+-rw-r--r--   0        0        0     1533 1970-01-01 00:00:00.000000 shimpy-0.0.2/setup.py
+-rw-r--r--   0        0        0     1132 1970-01-01 00:00:00.000000 shimpy-0.0.2/PKG-INFO
```

### Comparing `shimpy-0.0.1/LICENSE` & `shimpy-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `shimpy-0.0.1/README.md` & `shimpy-0.0.2/README.md`

 * *Files 18% similar despite different names*

```diff
@@ -25,11 +25,12 @@
   - list: List all accounts
 - address
   - new: Generate new address for account
   - list: List all addresses in the account
 - nft
   - mint: Mint new NFT
   - send: Send NFT to an address
+- send: Send SMR to an address
 
 ### Contributions Welcome
 
 #### Under Development
```

### Comparing `shimpy-0.0.1/pyproject.toml` & `shimpy-0.0.2/pyproject.toml`

 * *Files 24% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "shimpy"
-version = "0.0.1"
+version = "0.0.2"
 description = "Sample CLI Tool to interact with Shimmer Network."
 authors = ["Kumar Anirudha <mail@anirudha.dev>"]
 license = "MIT"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.11"
```

### Comparing `shimpy-0.0.1/shimpy/account/commands.py` & `shimpy-0.0.2/shimpy/account/commands.py`

 * *Files identical despite different names*

### Comparing `shimpy-0.0.1/shimpy/address/commands.py` & `shimpy-0.0.2/shimpy/address/commands.py`

 * *Files identical despite different names*

### Comparing `shimpy-0.0.1/shimpy/nft/commands.py` & `shimpy-0.0.2/shimpy/nft/commands.py`

 * *Files identical despite different names*

### Comparing `shimpy-0.0.1/setup.py` & `shimpy-0.0.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,27 +1,32 @@
 # -*- coding: utf-8 -*-
 from setuptools import setup
 
 packages = \
-['shimpy', 'shimpy.account', 'shimpy.address', 'shimpy.nft', 'shimpy.node']
+['shimpy',
+ 'shimpy.account',
+ 'shimpy.address',
+ 'shimpy.nft',
+ 'shimpy.node',
+ 'shimpy.transactions']
 
 package_data = \
 {'': ['*']}
 
 install_requires = \
 ['arrow>=1.2.3,<2.0.0', 'click>=8.1.6,<9.0.0', 'iota-sdk==1.0.0rc1']
 
 entry_points = \
 {'console_scripts': ['shimpy = shimpy.cli:shimpy']}
 
 setup_kwargs = {
     'name': 'shimpy',
-    'version': '0.0.1',
+    'version': '0.0.2',
     'description': 'Sample CLI Tool to interact with Shimmer Network.',
-    'long_description': '# Shimpy\n\nSample CLI Tool to interact with Shimmer Network using [iota-sdk](https://pypi.org/project/iota-sdk/).\n\n## Install\n\n### Using pip\n\n`pip install shimpy`\n\n### Using poetry\n\n`poetry add shimpy`\n\n## Usage\n\n`shimpy --help`\n\n## Commands\n\n- info : Get Info about Node\n- account\n  - new: Generate new account\n  - balance: Get balance by account alias\n  - list: List all accounts\n- address\n  - new: Generate new address for account\n  - list: List all addresses in the account\n- nft\n  - mint: Mint new NFT\n  - send: Send NFT to an address\n\n### Contributions Welcome\n\n#### Under Development\n',
+    'long_description': '# Shimpy\n\nSample CLI Tool to interact with Shimmer Network using [iota-sdk](https://pypi.org/project/iota-sdk/).\n\n## Install\n\n### Using pip\n\n`pip install shimpy`\n\n### Using poetry\n\n`poetry add shimpy`\n\n## Usage\n\n`shimpy --help`\n\n## Commands\n\n- info : Get Info about Node\n- account\n  - new: Generate new account\n  - balance: Get balance by account alias\n  - list: List all accounts\n- address\n  - new: Generate new address for account\n  - list: List all addresses in the account\n- nft\n  - mint: Mint new NFT\n  - send: Send NFT to an address\n- send: Send SMR to an address\n\n### Contributions Welcome\n\n#### Under Development\n',
     'author': 'Kumar Anirudha',
     'author_email': 'mail@anirudha.dev',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
     'packages': packages,
     'package_data': package_data,
```

### Comparing `shimpy-0.0.1/PKG-INFO` & `shimpy-0.0.2/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: shimpy
-Version: 0.0.1
+Version: 0.0.2
 Summary: Sample CLI Tool to interact with Shimmer Network.
 License: MIT
 Author: Kumar Anirudha
 Author-email: mail@anirudha.dev
 Requires-Python: >=3.11,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -41,12 +41,13 @@
   - list: List all accounts
 - address
   - new: Generate new address for account
   - list: List all addresses in the account
 - nft
   - mint: Mint new NFT
   - send: Send NFT to an address
+- send: Send SMR to an address
 
 ### Contributions Welcome
 
 #### Under Development
```

