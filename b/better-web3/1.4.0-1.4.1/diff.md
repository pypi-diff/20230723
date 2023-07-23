# Comparing `tmp/better_web3-1.4.0.tar.gz` & `tmp/better_web3-1.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "better_web3-1.4.0.tar", max compression
+gzip compressed data, was "better_web3-1.4.1.tar", max compression
```

## Comparing `better_web3-1.4.0.tar` & `better_web3-1.4.1.tar`

### file list

```diff
@@ -1,38 +1,38 @@
--rw-r--r--   0        0        0      403 2023-07-17 08:30:00.413000 better_web3-1.4.0/better_web3/__init__.py
--rw-r--r--   0        0        0    10461 2023-07-17 08:28:26.368000 better_web3-1.4.0/better_web3/batch_call.py
--rw-r--r--   0        0        0    15896 2023-07-15 15:58:01.098000 better_web3-1.4.0/better_web3/chain.py
--rw-r--r--   0        0        0      251 2023-07-07 12:10:25.885000 better_web3-1.4.0/better_web3/contract/__init__.py
--rw-r--r--   0        0        0      525 2023-07-11 06:39:31.842000 better_web3-1.4.0/better_web3/contract/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0      687 2023-07-11 06:39:33.730000 better_web3-1.4.0/better_web3/contract/__pycache__/_abi.cpython-311.pyc
--rw-r--r--   0        0        0      351 2023-06-05 07:45:48.569000 better_web3-1.4.0/better_web3/contract/__pycache__/_paths.cpython-311.pyc
--rw-r--r--   0        0        0     2938 2023-07-11 06:39:31.913000 better_web3-1.4.0/better_web3/contract/__pycache__/contract.cpython-311.pyc
--rw-r--r--   0        0        0     1938 2023-07-11 06:39:34.027000 better_web3-1.4.0/better_web3/contract/__pycache__/disperse.cpython-311.pyc
--rw-r--r--   0        0        0     3687 2023-07-11 06:39:34.086000 better_web3-1.4.0/better_web3/contract/__pycache__/erc20.cpython-311.pyc
--rw-r--r--   0        0        0     5293 2023-07-11 06:39:34.163000 better_web3-1.4.0/better_web3/contract/__pycache__/erc721.cpython-311.pyc
--rw-r--r--   0        0        0     9601 2023-07-11 06:39:33.679000 better_web3-1.4.0/better_web3/contract/__pycache__/multicall.cpython-311.pyc
--rw-r--r--   0        0        0      352 2023-07-07 12:03:06.296000 better_web3-1.4.0/better_web3/contract/_abi.py
--rw-r--r--   0        0        0       99 2023-06-05 07:40:59.317000 better_web3-1.4.0/better_web3/contract/_paths.py
--rw-r--r--   0        0        0     1193 2023-06-23 09:34:50.869000 better_web3-1.4.0/better_web3/contract/abi/disperse.json
--rw-r--r--   0        0        0     6301 2023-06-05 07:31:12.380000 better_web3-1.4.0/better_web3/contract/abi/erc1155.json
--rw-r--r--   0        0        0     5904 2023-06-05 07:28:35.070000 better_web3-1.4.0/better_web3/contract/abi/erc20.json
--rw-r--r--   0        0        0     6755 2023-06-05 07:31:25.078000 better_web3-1.4.0/better_web3/contract/abi/erc721.json
--rw-r--r--   0        0        0     8859 2023-06-04 08:00:02.863000 better_web3-1.4.0/better_web3/contract/abi/multicall_v3.json
--rw-r--r--   0        0        0     1264 2023-07-10 08:18:27.356000 better_web3-1.4.0/better_web3/contract/contract.py
--rw-r--r--   0        0        0      974 2023-07-07 12:13:30.821000 better_web3-1.4.0/better_web3/contract/disperse.py
--rw-r--r--   0        0        0     1747 2023-07-07 20:11:33.426000 better_web3-1.4.0/better_web3/contract/erc20.py
--rw-r--r--   0        0        0     2876 2023-07-07 20:11:33.364000 better_web3-1.4.0/better_web3/contract/erc721.py
--rw-r--r--   0        0        0     6201 2023-07-07 12:07:18.259000 better_web3-1.4.0/better_web3/contract/multicall.py
--rw-r--r--   0        0        0      165 2023-06-06 11:25:51.067000 better_web3-1.4.0/better_web3/enums.py
--rw-r--r--   0        0        0     4037 2023-07-17 10:02:59.828000 better_web3-1.4.0/better_web3/proxy.py
--rw-r--r--   0        0        0      730 2023-07-17 08:28:26.473000 better_web3-1.4.0/better_web3/utils/__init__.py
--rw-r--r--   0        0        0      917 2023-07-17 08:28:28.447000 better_web3-1.4.0/better_web3/utils/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0     4132 2023-07-17 08:28:28.496000 better_web3-1.4.0/better_web3/utils/__pycache__/eth.cpython-311.pyc
--rw-r--r--   0        0        0     3469 2023-06-28 12:32:10.861000 better_web3-1.4.0/better_web3/utils/__pycache__/file.cpython-311.pyc
--rw-r--r--   0        0        0     1398 2023-07-11 06:39:33.869000 better_web3-1.4.0/better_web3/utils/__pycache__/other.cpython-311.pyc
--rw-r--r--   0        0        0     2131 2023-07-17 08:28:26.617000 better_web3-1.4.0/better_web3/utils/eth.py
--rw-r--r--   0        0        0     1020 2023-06-28 11:42:15.374000 better_web3-1.4.0/better_web3/utils/file.py
--rw-r--r--   0        0        0      663 2023-07-07 20:05:19.087000 better_web3-1.4.0/better_web3/utils/other.py
--rw-r--r--   0        0        0     3172 2023-07-17 10:00:37.875000 better_web3-1.4.0/better_web3/wallet.py
--rw-r--r--   0        0        0      412 2023-07-17 09:38:47.230000 better_web3-1.4.0/pyproject.toml
--rw-r--r--   0        0        0      479 2023-07-07 17:47:32.398000 better_web3-1.4.0/README.md
--rw-r--r--   0        0        0      863 1970-01-01 00:00:00.000000 better_web3-1.4.0/PKG-INFO
+-rw-r--r--   0        0        0      403 2023-07-17 08:30:00.413000 better_web3-1.4.1/better_web3/__init__.py
+-rw-r--r--   0        0        0    10461 2023-07-17 08:28:26.368000 better_web3-1.4.1/better_web3/batch_call.py
+-rw-r--r--   0        0        0    15939 2023-07-23 08:52:53.716000 better_web3-1.4.1/better_web3/chain.py
+-rw-r--r--   0        0        0      251 2023-07-07 12:10:25.885000 better_web3-1.4.1/better_web3/contract/__init__.py
+-rw-r--r--   0        0        0      525 2023-07-11 06:39:31.842000 better_web3-1.4.1/better_web3/contract/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0      687 2023-07-11 06:39:33.730000 better_web3-1.4.1/better_web3/contract/__pycache__/_abi.cpython-311.pyc
+-rw-r--r--   0        0        0      351 2023-06-05 07:45:48.569000 better_web3-1.4.1/better_web3/contract/__pycache__/_paths.cpython-311.pyc
+-rw-r--r--   0        0        0     2938 2023-07-11 06:39:31.913000 better_web3-1.4.1/better_web3/contract/__pycache__/contract.cpython-311.pyc
+-rw-r--r--   0        0        0     1938 2023-07-11 06:39:34.027000 better_web3-1.4.1/better_web3/contract/__pycache__/disperse.cpython-311.pyc
+-rw-r--r--   0        0        0     3687 2023-07-11 06:39:34.086000 better_web3-1.4.1/better_web3/contract/__pycache__/erc20.cpython-311.pyc
+-rw-r--r--   0        0        0     5293 2023-07-11 06:39:34.163000 better_web3-1.4.1/better_web3/contract/__pycache__/erc721.cpython-311.pyc
+-rw-r--r--   0        0        0     9601 2023-07-11 06:39:33.679000 better_web3-1.4.1/better_web3/contract/__pycache__/multicall.cpython-311.pyc
+-rw-r--r--   0        0        0      352 2023-07-07 12:03:06.296000 better_web3-1.4.1/better_web3/contract/_abi.py
+-rw-r--r--   0        0        0       99 2023-06-05 07:40:59.317000 better_web3-1.4.1/better_web3/contract/_paths.py
+-rw-r--r--   0        0        0     1193 2023-06-23 09:34:50.869000 better_web3-1.4.1/better_web3/contract/abi/disperse.json
+-rw-r--r--   0        0        0     6301 2023-06-05 07:31:12.380000 better_web3-1.4.1/better_web3/contract/abi/erc1155.json
+-rw-r--r--   0        0        0     5904 2023-06-05 07:28:35.070000 better_web3-1.4.1/better_web3/contract/abi/erc20.json
+-rw-r--r--   0        0        0     6755 2023-06-05 07:31:25.078000 better_web3-1.4.1/better_web3/contract/abi/erc721.json
+-rw-r--r--   0        0        0     8859 2023-06-04 08:00:02.863000 better_web3-1.4.1/better_web3/contract/abi/multicall_v3.json
+-rw-r--r--   0        0        0     1264 2023-07-10 08:18:27.356000 better_web3-1.4.1/better_web3/contract/contract.py
+-rw-r--r--   0        0        0      974 2023-07-07 12:13:30.821000 better_web3-1.4.1/better_web3/contract/disperse.py
+-rw-r--r--   0        0        0     1747 2023-07-07 20:11:33.426000 better_web3-1.4.1/better_web3/contract/erc20.py
+-rw-r--r--   0        0        0     2876 2023-07-07 20:11:33.364000 better_web3-1.4.1/better_web3/contract/erc721.py
+-rw-r--r--   0        0        0     6201 2023-07-07 12:07:18.259000 better_web3-1.4.1/better_web3/contract/multicall.py
+-rw-r--r--   0        0        0      165 2023-06-06 11:25:51.067000 better_web3-1.4.1/better_web3/enums.py
+-rw-r--r--   0        0        0     4037 2023-07-17 10:02:59.828000 better_web3-1.4.1/better_web3/proxy.py
+-rw-r--r--   0        0        0      730 2023-07-17 08:28:26.473000 better_web3-1.4.1/better_web3/utils/__init__.py
+-rw-r--r--   0        0        0      917 2023-07-17 08:28:28.447000 better_web3-1.4.1/better_web3/utils/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0     4132 2023-07-17 08:28:28.496000 better_web3-1.4.1/better_web3/utils/__pycache__/eth.cpython-311.pyc
+-rw-r--r--   0        0        0     3469 2023-06-28 12:32:10.861000 better_web3-1.4.1/better_web3/utils/__pycache__/file.cpython-311.pyc
+-rw-r--r--   0        0        0     1398 2023-07-11 06:39:33.869000 better_web3-1.4.1/better_web3/utils/__pycache__/other.cpython-311.pyc
+-rw-r--r--   0        0        0     2131 2023-07-17 08:28:26.617000 better_web3-1.4.1/better_web3/utils/eth.py
+-rw-r--r--   0        0        0     1020 2023-06-28 11:42:15.374000 better_web3-1.4.1/better_web3/utils/file.py
+-rw-r--r--   0        0        0      663 2023-07-07 20:05:19.087000 better_web3-1.4.1/better_web3/utils/other.py
+-rw-r--r--   0        0        0     3172 2023-07-17 10:00:37.875000 better_web3-1.4.1/better_web3/wallet.py
+-rw-r--r--   0        0        0      412 2023-07-23 08:52:53.613000 better_web3-1.4.1/pyproject.toml
+-rw-r--r--   0        0        0      479 2023-07-07 17:47:32.398000 better_web3-1.4.1/README.md
+-rw-r--r--   0        0        0      863 1970-01-01 00:00:00.000000 better_web3-1.4.1/PKG-INFO
```

### Comparing `better_web3-1.4.0/better_web3/batch_call.py` & `better_web3-1.4.1/better_web3/batch_call.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/chain.py` & `better_web3-1.4.1/better_web3/chain.py`

 * *Files 1% similar despite different names*

```diff
@@ -408,14 +408,15 @@
             # dynamic fee pricing
             max_fee_per_gas: Wei | int = None,
             max_priority_fee_per_gas: Wei | int = None,
             tx_speed: TxSpeed = TxSpeed.NORMAL,
     ) -> HexStr:
         tx = self.build_tx(
             fn,
+            address_from=account.address,
             gas=gas,
             nonce=nonce,
             value=value,
             gas_price=gas_price,
             max_fee_per_gas=max_fee_per_gas,
             max_priority_fee_per_gas=max_priority_fee_per_gas,
             tx_speed=tx_speed,
```

### Comparing `better_web3-1.4.0/better_web3/contract/__pycache__/__init__.cpython-311.pyc` & `better_web3-1.4.1/better_web3/contract/__pycache__/__init__.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/__pycache__/_abi.cpython-311.pyc` & `better_web3-1.4.1/better_web3/contract/__pycache__/_abi.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/__pycache__/contract.cpython-311.pyc` & `better_web3-1.4.1/better_web3/contract/__pycache__/contract.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/__pycache__/disperse.cpython-311.pyc` & `better_web3-1.4.1/better_web3/contract/__pycache__/disperse.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/__pycache__/erc20.cpython-311.pyc` & `better_web3-1.4.1/better_web3/contract/__pycache__/erc20.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/__pycache__/erc721.cpython-311.pyc` & `better_web3-1.4.1/better_web3/contract/__pycache__/erc721.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/__pycache__/multicall.cpython-311.pyc` & `better_web3-1.4.1/better_web3/contract/__pycache__/multicall.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/abi/disperse.json` & `better_web3-1.4.1/better_web3/contract/abi/disperse.json`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/abi/erc1155.json` & `better_web3-1.4.1/better_web3/contract/abi/erc1155.json`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/abi/erc20.json` & `better_web3-1.4.1/better_web3/contract/abi/erc20.json`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/abi/erc721.json` & `better_web3-1.4.1/better_web3/contract/abi/erc721.json`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/abi/multicall_v3.json` & `better_web3-1.4.1/better_web3/contract/abi/multicall_v3.json`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/contract.py` & `better_web3-1.4.1/better_web3/contract/contract.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/disperse.py` & `better_web3-1.4.1/better_web3/contract/disperse.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/erc20.py` & `better_web3-1.4.1/better_web3/contract/erc20.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/erc721.py` & `better_web3-1.4.1/better_web3/contract/erc721.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/contract/multicall.py` & `better_web3-1.4.1/better_web3/contract/multicall.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/proxy.py` & `better_web3-1.4.1/better_web3/proxy.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/utils/__init__.py` & `better_web3-1.4.1/better_web3/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/utils/__pycache__/__init__.cpython-311.pyc` & `better_web3-1.4.1/better_web3/utils/__pycache__/__init__.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/utils/__pycache__/eth.cpython-311.pyc` & `better_web3-1.4.1/better_web3/utils/__pycache__/eth.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/utils/__pycache__/file.cpython-311.pyc` & `better_web3-1.4.1/better_web3/utils/__pycache__/file.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/utils/__pycache__/other.cpython-311.pyc` & `better_web3-1.4.1/better_web3/utils/__pycache__/other.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/utils/eth.py` & `better_web3-1.4.1/better_web3/utils/eth.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/utils/file.py` & `better_web3-1.4.1/better_web3/utils/file.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/utils/other.py` & `better_web3-1.4.1/better_web3/utils/other.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/better_web3/wallet.py` & `better_web3-1.4.1/better_web3/wallet.py`

 * *Files identical despite different names*

### Comparing `better_web3-1.4.0/PKG-INFO` & `better_web3-1.4.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: better-web3
-Version: 1.4.0
+Version: 1.4.1
 Summary: Chains, Contracts(Multicall, Disperse, ERC20/ERC721), batch calls and other..
 Author: Alen
 Author-email: alen.kimov@gmail.com
 Requires-Python: >=3.11,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: web3 (>=6.6.1,<7.0.0)
```

