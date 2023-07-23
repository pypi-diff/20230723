# Comparing `tmp/torchhandy-0.0.5.tar.gz` & `tmp/torchhandy-0.0.6.tar.gz`

## Comparing `torchhandy-0.0.5.tar` & `torchhandy-0.0.6.tar`

### file list

```diff
@@ -1,14 +1,14 @@
--rw-r--r--   0        0        0      175 2020-02-02 00:00:00.000000 torchhandy-0.0.5/.pypirc
--rw-r--r--   0        0        0     5713 2020-02-02 00:00:00.000000 torchhandy-0.0.5/torchhandy/Block.py
--rw-r--r--   0        0        0     3528 2020-02-02 00:00:00.000000 torchhandy-0.0.5/torchhandy/Conv.py
--rw-r--r--   0        0        0     1619 2020-02-02 00:00:00.000000 torchhandy-0.0.5/torchhandy/Diffusion.py
--rw-r--r--   0        0        0     2256 2020-02-02 00:00:00.000000 torchhandy-0.0.5/torchhandy/FC.py
--rw-r--r--   0        0        0     2959 2020-02-02 00:00:00.000000 torchhandy-0.0.5/torchhandy/Parallel.py
--rw-r--r--   0        0        0     6027 2020-02-02 00:00:00.000000 torchhandy-0.0.5/torchhandy/Train.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 torchhandy-0.0.5/torchhandy/__init__.py
--rw-r--r--   0        0        0     2539 2020-02-02 00:00:00.000000 torchhandy-0.0.5/torchhandy/utils.py
--rw-r--r--   0        0        0       15 2020-02-02 00:00:00.000000 torchhandy-0.0.5/.gitignore
--rw-r--r--   0        0        0     1093 2020-02-02 00:00:00.000000 torchhandy-0.0.5/LICENSE
--rw-r--r--   0        0        0      152 2020-02-02 00:00:00.000000 torchhandy-0.0.5/README.md
--rw-r--r--   0        0        0      660 2020-02-02 00:00:00.000000 torchhandy-0.0.5/pyproject.toml
--rw-r--r--   0        0        0     1906 2020-02-02 00:00:00.000000 torchhandy-0.0.5/PKG-INFO
+-rw-r--r--   0        0        0      175 2020-02-02 00:00:00.000000 torchhandy-0.0.6/.pypirc
+-rw-r--r--   0        0        0     5713 2020-02-02 00:00:00.000000 torchhandy-0.0.6/torchhandy/Block.py
+-rw-r--r--   0        0        0     3528 2020-02-02 00:00:00.000000 torchhandy-0.0.6/torchhandy/Conv.py
+-rw-r--r--   0        0        0     1619 2020-02-02 00:00:00.000000 torchhandy-0.0.6/torchhandy/Diffusion.py
+-rw-r--r--   0        0        0     2256 2020-02-02 00:00:00.000000 torchhandy-0.0.6/torchhandy/FC.py
+-rw-r--r--   0        0        0     2959 2020-02-02 00:00:00.000000 torchhandy-0.0.6/torchhandy/Parallel.py
+-rw-r--r--   0        0        0     6051 2020-02-02 00:00:00.000000 torchhandy-0.0.6/torchhandy/Train.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 torchhandy-0.0.6/torchhandy/__init__.py
+-rw-r--r--   0        0        0     2539 2020-02-02 00:00:00.000000 torchhandy-0.0.6/torchhandy/utils.py
+-rw-r--r--   0        0        0       15 2020-02-02 00:00:00.000000 torchhandy-0.0.6/.gitignore
+-rw-r--r--   0        0        0     1093 2020-02-02 00:00:00.000000 torchhandy-0.0.6/LICENSE
+-rw-r--r--   0        0        0      152 2020-02-02 00:00:00.000000 torchhandy-0.0.6/README.md
+-rw-r--r--   0        0        0      660 2020-02-02 00:00:00.000000 torchhandy-0.0.6/pyproject.toml
+-rw-r--r--   0        0        0     1906 2020-02-02 00:00:00.000000 torchhandy-0.0.6/PKG-INFO
```

### Comparing `torchhandy-0.0.5/torchhandy/Block.py` & `torchhandy-0.0.6/torchhandy/Block.py`

 * *Files identical despite different names*

### Comparing `torchhandy-0.0.5/torchhandy/Conv.py` & `torchhandy-0.0.6/torchhandy/Conv.py`

 * *Files identical despite different names*

### Comparing `torchhandy-0.0.5/torchhandy/Diffusion.py` & `torchhandy-0.0.6/torchhandy/Diffusion.py`

 * *Files identical despite different names*

### Comparing `torchhandy-0.0.5/torchhandy/FC.py` & `torchhandy-0.0.6/torchhandy/FC.py`

 * *Files identical despite different names*

### Comparing `torchhandy-0.0.5/torchhandy/Parallel.py` & `torchhandy-0.0.6/torchhandy/Parallel.py`

 * *Files identical despite different names*

### Comparing `torchhandy-0.0.5/torchhandy/Train.py` & `torchhandy-0.0.6/torchhandy/Train.py`

 * *Files 1% similar despite different names*

```diff
@@ -128,15 +128,15 @@
         else:
             if ckpt['loss'] < self.best_val:
                 self.best_val = ckpt['loss']
                 self.trainer.save_model(ckpt, self.model, self.best_path)
         ed_time = time.time()
         dur = ed_time - st_time
         self.trainer.call_func(print, f'this epoch cost {dur} seconds, which is {dur / 60} minutes or {dur / 3600} hours')
-        self.trainer.call_func(self.model.generate_cases, dataset, 1, 
+        self.trainer.call_func(self.trainer.get_model(self.model).generate_cases, dataset, 1, 
                             self.trainer.get_device(), f'{self.model_name}_{type}_{epoch}')
         
     def train_model(self):
         for epoch in range(self.start_epoch, self.start_epoch + self.epochs):
             clear_cuda()
             self.forward_one_epoch(epoch, self.trainset, type = 'train')
             self.forward_one_epoch(epoch, self.valset, type = 'valid')
```

### Comparing `torchhandy-0.0.5/torchhandy/utils.py` & `torchhandy-0.0.6/torchhandy/utils.py`

 * *Files identical despite different names*

### Comparing `torchhandy-0.0.5/LICENSE` & `torchhandy-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `torchhandy-0.0.5/pyproject.toml` & `torchhandy-0.0.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 00000000: 5b62 7569 6c64 2d73 7973 7465 6d5d 0d0a  [build-system]..
 00000010: 7265 7175 6972 6573 203d 205b 2268 6174  requires = ["hat
 00000020: 6368 6c69 6e67 225d 0d0a 6275 696c 642d  chling"]..build-
 00000030: 6261 636b 656e 6420 3d20 2268 6174 6368  backend = "hatch
 00000040: 6c69 6e67 2e62 7569 6c64 220d 0a0d 0a5b  ling.build"....[
 00000050: 7072 6f6a 6563 745d 0d0a 6e61 6d65 203d  project]..name =
 00000060: 2022 746f 7263 6868 616e 6479 220d 0a76   "torchhandy"..v
-00000070: 6572 7369 6f6e 203d 2022 302e 302e 3522  ersion = "0.0.5"
+00000070: 6572 7369 6f6e 203d 2022 302e 302e 3622  ersion = "0.0.6"
 00000080: 0d0a 6175 7468 6f72 7320 3d20 5b0d 0a20  ..authors = [.. 
 00000090: 207b 206e 616d 653d 22e5 bca0 e88d 9fe8   { name=".......
 000000a0: 90b1 222c 2065 6d61 696c 3d22 706b 756c  ..", email="pkul
 000000b0: 656f 7a68 616e 6740 676d 6169 6c2e 636f  eozhang@gmail.co
 000000c0: 6d22 7d2c 0d0a 5d0d 0a0d 0a64 6573 6372  m"},..]....descr
 000000d0: 6970 7469 6f6e 203d 2022 746f 7263 6868  iption = "torchh
 000000e0: 616e 6479 2069 7320 6120 6861 6e64 7920  andy is a handy
```

### Comparing `torchhandy-0.0.5/PKG-INFO` & `torchhandy-0.0.6/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torchhandy
-Version: 0.0.5
+Version: 0.0.6
 Summary: torchhandy is a handy package that implements some commonly used modules and function.
 Project-URL: Homepage, https://github.com/NickYi1990/juans
 Author-email: 张荟萱 <pkuleozhang@gmail.com>
 License: MIT License
         
         Copyright (c) [2023] [Huixuan Zhang]
```

