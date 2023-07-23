# Comparing `tmp/MarsGT-0.1.8.tar.gz` & `tmp/MarsGT-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/MarsGT-0.1.8.tar", last modified: Wed Jul 19 02:08:32 2023, max compression
+gzip compressed data, was "dist/MarsGT-0.1.9.tar", last modified: Sun Jul 23 14:08:21 2023, max compression
```

## Comparing `MarsGT-0.1.8.tar` & `MarsGT-0.1.9.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 duanmaoteng (40439) PCON0022  (6618)        0 2023-07-19 02:08:32.237646 MarsGT-0.1.8/
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)       34 2023-06-03 06:21:54.000000 MarsGT-0.1.8/MANIFEST.in
-drwxr-xr-x   0 duanmaoteng (40439) PCON0022  (6618)        0 2023-07-19 02:08:32.201649 MarsGT-0.1.8/MarsGT/
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)        2 2023-06-03 06:21:57.000000 MarsGT-0.1.8/MarsGT/__init__.py
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)     6719 2023-06-03 08:36:23.000000 MarsGT-0.1.8/MarsGT/conv.py
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)     8824 2023-07-18 10:28:20.000000 MarsGT-0.1.8/MarsGT/egrn.py
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)    21360 2023-06-03 08:36:23.000000 MarsGT-0.1.8/MarsGT/marsgt_model.py
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)     7805 2023-07-18 10:28:36.000000 MarsGT-0.1.8/MarsGT/utils.py
-drwxr-xr-x   0 duanmaoteng (40439) PCON0022  (6618)        0 2023-07-19 02:08:32.219650 MarsGT-0.1.8/MarsGT.egg-info/
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      963 2023-07-19 02:08:32.000000 MarsGT-0.1.8/MarsGT.egg-info/PKG-INFO
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      267 2023-07-19 02:08:32.000000 MarsGT-0.1.8/MarsGT.egg-info/SOURCES.txt
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)        1 2023-07-19 02:08:32.000000 MarsGT-0.1.8/MarsGT.egg-info/dependency_links.txt
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      260 2023-07-19 02:08:32.000000 MarsGT-0.1.8/MarsGT.egg-info/requires.txt
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)        7 2023-07-19 02:08:32.000000 MarsGT-0.1.8/MarsGT.egg-info/top_level.txt
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      963 2023-07-19 02:08:32.235647 MarsGT-0.1.8/PKG-INFO
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      709 2023-07-19 01:31:01.000000 MarsGT-0.1.8/README.md
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)       38 2023-07-19 02:08:32.237652 MarsGT-0.1.8/setup.cfg
--rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)     1336 2023-07-19 02:06:32.000000 MarsGT-0.1.8/setup.py
+drwxr-xr-x   0 duanmaoteng (40439) PCON0022  (6618)        0 2023-07-23 14:08:21.179870 MarsGT-0.1.9/
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)       34 2023-06-03 06:21:54.000000 MarsGT-0.1.9/MANIFEST.in
+drwxr-xr-x   0 duanmaoteng (40439) PCON0022  (6618)        0 2023-07-23 14:08:21.137859 MarsGT-0.1.9/MarsGT/
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)        2 2023-06-03 06:21:57.000000 MarsGT-0.1.9/MarsGT/__init__.py
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)     6719 2023-06-03 08:36:23.000000 MarsGT-0.1.9/MarsGT/conv.py
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)     8824 2023-07-18 10:28:20.000000 MarsGT-0.1.9/MarsGT/egrn.py
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)    21360 2023-06-03 08:36:23.000000 MarsGT-0.1.9/MarsGT/marsgt_model.py
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)     8280 2023-07-23 14:06:25.000000 MarsGT-0.1.9/MarsGT/utils.py
+drwxr-xr-x   0 duanmaoteng (40439) PCON0022  (6618)        0 2023-07-23 14:08:21.173852 MarsGT-0.1.9/MarsGT.egg-info/
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      963 2023-07-23 14:08:20.000000 MarsGT-0.1.9/MarsGT.egg-info/PKG-INFO
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      267 2023-07-23 14:08:20.000000 MarsGT-0.1.9/MarsGT.egg-info/SOURCES.txt
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)        1 2023-07-23 14:08:20.000000 MarsGT-0.1.9/MarsGT.egg-info/dependency_links.txt
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      260 2023-07-23 14:08:20.000000 MarsGT-0.1.9/MarsGT.egg-info/requires.txt
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)        7 2023-07-23 14:08:20.000000 MarsGT-0.1.9/MarsGT.egg-info/top_level.txt
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      963 2023-07-23 14:08:21.177889 MarsGT-0.1.9/PKG-INFO
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)      709 2023-07-19 01:31:01.000000 MarsGT-0.1.9/README.md
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)       38 2023-07-23 14:08:21.180857 MarsGT-0.1.9/setup.cfg
+-rw-r--r--   0 duanmaoteng (40439) PCON0022  (6618)     1336 2023-07-23 14:07:48.000000 MarsGT-0.1.9/setup.py
```

### Comparing `MarsGT-0.1.8/MarsGT/conv.py` & `MarsGT-0.1.9/MarsGT/conv.py`

 * *Files identical despite different names*

### Comparing `MarsGT-0.1.8/MarsGT/egrn.py` & `MarsGT-0.1.9/MarsGT/egrn.py`

 * *Files identical despite different names*

### Comparing `MarsGT-0.1.8/MarsGT/marsgt_model.py` & `MarsGT-0.1.9/MarsGT/marsgt_model.py`

 * *Files identical despite different names*

### Comparing `MarsGT-0.1.8/MarsGT/utils.py` & `MarsGT-0.1.9/MarsGT/utils.py`

 * *Files 10% similar despite different names*

```diff
@@ -48,27 +48,27 @@
         gene_indices_all = []
         peak_indices_all = []
         if i < n_batch:
             for index, node in enumerate(node_ids[i * cell_size:(i + 1) * cell_size]):
                 rna_ = RNA_matrix1[:, node].todense()
                 rna_[rna_ < 5] = 0
                 gene_indices = subgraph(RNA_matrix.transpose(), node, neighbor, np.squeeze(np.array(np.log(rna_ + 1))))
-                peak_indices = subgraph(RNA_matrix.transpose(), node, neighbor,
+                peak_indices = subgraph(ATAC_matrix.transpose(), node, neighbor,
                                         np.squeeze(np.array(np.log(ATAC_matrix[:, node].todense() + 1))))
                 dic[node] = {'g': gene_indices, 'p': peak_indices}
                 gene_indices_all = gene_indices_all + gene_indices
                 peak_indices_all = peak_indices_all + peak_indices
             node_indices_all = node_ids[i * cell_size:(i + 1) * cell_size]
         else:
             for index, node in enumerate(node_ids[i * cell_size:]):
                 rna_ = RNA_matrix1[:, node].todense()
                 rna_[rna_ < 5] = 0
                 gene_indices = subgraph(RNA_matrix.transpose(), node, neighbor,
                                         np.squeeze(np.array(np.log(rna_[:, node].todense() + 1))))
-                peak_indices = subgraph(RNA_matrix.transpose(), node, neighbor,
+                peak_indices = subgraph(ATAC_matrix.transpose(), node, neighbor,
                                         np.squeeze(np.array(np.log(ATAC_matrix[:, node].todense() + 1))))
                 dic[node] = {'g': gene_indices, 'p': peak_indices}
                 gene_indices_all = gene_indices_all + gene_indices
                 peak_indices_all = peak_indices_all + peak_indices
             node_indices_all = node_ids[i * cell_size:]
 
         gene_indices_all = list(set(gene_indices_all))
@@ -102,35 +102,48 @@
         nll_loss = -logprobs.gather(dim=-1, index=target.unsqueeze(1))
         nll_loss = nll_loss.squeeze(1)
         smooth_loss = -logprobs.mean(dim=-1)
         loss = self.confidence * nll_loss + self.smoothing * smooth_loss
         return loss.mean()
 
 
-def initial_clustering(RNA_matrix, n_neighbors=15, n_pcs=40, resolution=0.5):
+def initial_clustering(RNA_matrix, custom_n_neighbors=None, n_pcs=40, custom_resolution=None, use_rep=None):
     print(
         '\tWhen the number of cells is less than or equal to 500, it is recommended to set the resolution value to 0.2.')
     print('\tWhen the number of cells is within the range of 500 to 5000, the resolution value should be set to 0.5.')
     print('\tWhen the number of cells is greater than 5000, the resolution value should be set to 0.8.')
 
     def segment_function(x):
         if x <= 500:
-            return 0.2,5
+            return 0.2, 5
         elif x <= 5000:
-            return 0.5,10
+            return 0.5, 10
         else:
-            return 0.8,15
+            return 0.8, 15
+
     adata = ad.AnnData(RNA_matrix.transpose(), dtype='int32')
-    resolution,n_neighbors = segment_function(adata.shape[0])
+
+    # If the user did not provide a custom resolution or n_neighbors value, use the values calculated by segment_function
+    if custom_resolution is None or custom_n_neighbors is None:
+        resolution, n_neighbors = segment_function(adata.shape[0])
+    else:
+        resolution = custom_resolution
+        n_neighbors = custom_n_neighbors
+
     sc.pp.normalize_total(adata, target_sum=1e4)
     sc.pp.log1p(adata)
-    sc.pp.neighbors(adata, n_neighbors=n_neighbors, n_pcs=n_pcs)
+
+    # Use the user-provided embedding if available, otherwise use n_pcs
+    if use_rep is not None:
+        adata.obsm['use_rep']=use_rep
+        sc.pp.neighbors(adata, use_rep='use_rep', n_neighbors=n_neighbors)
+    else:
+        sc.pp.neighbors(adata, n_neighbors=n_neighbors, n_pcs=n_pcs)
+
     sc.tl.leiden(adata, resolution)
-    #     sc.tl.umap(adata)
-    #     sc.pl.umap(adata, color=['leiden'])
     return adata.obs['leiden']
 
 
 def purity_score(y_true, y_pred):
     """Purity score
 
     Args:
```

### Comparing `MarsGT-0.1.8/MarsGT.egg-info/PKG-INFO` & `MarsGT-0.1.9/MarsGT.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MarsGT
-Version: 0.1.8
+Version: 0.1.9
 Summary: MarsGT: A Python library for rare cell identification (Internal testing only)
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: ==3.8.0
 Description-Content-Type: text/markdown
 
 ## Title：MarsGT:Multi-omics data analysis for rare population inference using single-cell graph transformer
 **Note: This project is for internal testing purposes only. Do not use it in a production environment.**
```

### Comparing `MarsGT-0.1.8/PKG-INFO` & `MarsGT-0.1.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MarsGT
-Version: 0.1.8
+Version: 0.1.9
 Summary: MarsGT: A Python library for rare cell identification (Internal testing only)
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: ==3.8.0
 Description-Content-Type: text/markdown
 
 ## Title：MarsGT:Multi-omics data analysis for rare population inference using single-cell graph transformer
 **Note: This project is for internal testing purposes only. Do not use it in a production environment.**
```

### Comparing `MarsGT-0.1.8/README.md` & `MarsGT-0.1.9/README.md`

 * *Files identical despite different names*

### Comparing `MarsGT-0.1.8/setup.py` & `MarsGT-0.1.9/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup, find_packages
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
     
 setup(
     name="MarsGT",
-    version='0.1.8',
+    version='0.1.9',
     packages=find_packages(),
     install_requires=[
         'anndata==0.8.0',
         'dill==0.3.4',
         'matplotlib==3.5.1',
         'numpy==1.22.3',
         'pandas==1.4.2',
```

