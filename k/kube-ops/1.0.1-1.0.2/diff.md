# Comparing `tmp/kube_ops-1.0.1-py3-none-any.whl.zip` & `tmp/kube_ops-1.0.2-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,14 +1,14 @@
-Zip file size: 18926 bytes, number of entries: 12
--rw-r--r--  2.0 unx     1311 b- defN 23-Jul-23 07:32 kube/__init__.py
+Zip file size: 18964 bytes, number of entries: 12
+-rw-r--r--  2.0 unx     1310 b- defN 23-Jul-23 11:51 kube/__init__.py
+-rw-r--r--  2.0 unx    32538 b- defN 23-Jul-23 05:31 kube/api.py
 -rw-r--r--  2.0 unx     2611 b- defN 23-Jul-23 07:44 kube/common.py
--rw-r--r--  2.0 unx     5081 b- defN 23-Jul-23 03:58 kube/config.py
+-rw-r--r--  2.0 unx     5080 b- defN 23-Jul-23 11:51 kube/config.py
 -rw-r--r--  2.0 unx     1197 b- defN 23-Jul-23 06:20 kube/enums.py
--rw-r--r--  2.0 unx    32538 b- defN 23-Jul-23 05:31 kube/kube.py
 -rw-r--r--  2.0 unx    19115 b- defN 23-Jul-23 10:00 kube/manifests.py
 -rw-r--r--  2.0 unx    10932 b- defN 23-Jul-23 10:00 kube/templates.py
--rw-r--r--  2.0 unx     1069 b- defN 23-Jul-23 10:22 kube_ops-1.0.1.dist-info/LICENSE
--rw-r--r--  2.0 unx     3356 b- defN 23-Jul-23 10:22 kube_ops-1.0.1.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 10:22 kube_ops-1.0.1.dist-info/WHEEL
--rw-r--r--  2.0 unx        5 b- defN 23-Jul-23 10:22 kube_ops-1.0.1.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      895 b- defN 23-Jul-23 10:22 kube_ops-1.0.1.dist-info/RECORD
-12 files, 78202 bytes uncompressed, 17458 bytes compressed:  77.7%
+-rw-r--r--  2.0 unx     1069 b- defN 23-Jul-23 11:53 kube_ops-1.0.2.dist-info/LICENSE
+-rw-r--r--  2.0 unx     3425 b- defN 23-Jul-23 11:53 kube_ops-1.0.2.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 11:53 kube_ops-1.0.2.dist-info/WHEEL
+-rw-r--r--  2.0 unx        5 b- defN 23-Jul-23 11:53 kube_ops-1.0.2.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      894 b- defN 23-Jul-23 11:53 kube_ops-1.0.2.dist-info/RECORD
+12 files, 78268 bytes uncompressed, 17498 bytes compressed:  77.6%
```

## zipnote {}

```diff
@@ -1,37 +1,37 @@
 Filename: kube/__init__.py
 Comment: 
 
+Filename: kube/api.py
+Comment: 
+
 Filename: kube/common.py
 Comment: 
 
 Filename: kube/config.py
 Comment: 
 
 Filename: kube/enums.py
 Comment: 
 
-Filename: kube/kube.py
-Comment: 
-
 Filename: kube/manifests.py
 Comment: 
 
 Filename: kube/templates.py
 Comment: 
 
-Filename: kube_ops-1.0.1.dist-info/LICENSE
+Filename: kube_ops-1.0.2.dist-info/LICENSE
 Comment: 
 
-Filename: kube_ops-1.0.1.dist-info/METADATA
+Filename: kube_ops-1.0.2.dist-info/METADATA
 Comment: 
 
-Filename: kube_ops-1.0.1.dist-info/WHEEL
+Filename: kube_ops-1.0.2.dist-info/WHEEL
 Comment: 
 
-Filename: kube_ops-1.0.1.dist-info/top_level.txt
+Filename: kube_ops-1.0.2.dist-info/top_level.txt
 Comment: 
 
-Filename: kube_ops-1.0.1.dist-info/RECORD
+Filename: kube_ops-1.0.2.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## kube/__init__.py

```diff
@@ -1,13 +1,13 @@
+from .api import KubeApi, CustomObjectDef, dict_to_labels
 from .common import env_from_configmap, env_from_configmap_key_ref, env_from_secret, env_from_secret_key_ref, \
     env_from_field_ref, empty_dir, volume_from_configmap, volume_from_secret
 from .config import Kubeconfig
 from .enums import ImagePullPolicy, ServiceType, SecretType, PVCAccessMode, IngressRulePathType, MatchExprOperator, \
     VolumeModes
-from .kube import KubeApi, CustomObjectDef, dict_to_labels
 from .manifests import ConfigMap, CronJob, Job, Deployment, Ingress, Namespace, Pod, PersistentVolumeClaim, \
     StatefulSet, Secret, SecretImagePull, SecretTLS, Service
 from .templates import Container
 
 __all__ = [
     'ConfigMap',
     'Container',
```

## kube/config.py

```diff
@@ -9,15 +9,15 @@
 
 import yaml
 from kubernetes import client
 from kubernetes.config.incluster_config import SERVICE_HOST_ENV_NAME, SERVICE_PORT_ENV_NAME, SERVICE_CERT_FILENAME
 from urllib3.exceptions import InsecureRequestWarning
 from urllib3.exceptions import MaxRetryError
 
-from .kube import KubeApi
+from .api import KubeApi
 
 
 class Kubeconfig:
     def __init__(self):
         self.__current_context = None
         self.__clusters = {}
         self.__contexts = {}
```

## Comparing `kube/kube.py` & `kube/api.py`

 * *Files identical despite different names*

## Comparing `kube_ops-1.0.1.dist-info/LICENSE` & `kube_ops-1.0.2.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `kube_ops-1.0.1.dist-info/METADATA` & `kube_ops-1.0.2.dist-info/METADATA`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kube-ops
-Version: 1.0.1
+Version: 1.0.2
 Summary: Kubernetes OOP
 Author-email: myback <54638513+myback@users.noreply.github.com>
 License: MIT License
         
         Copyright (c) 2023 myback.space
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -29,14 +29,16 @@
 Project-URL: Bug Tracker, https://github.com/myback/kube-ops/issues
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
+Requires-Dist: pyyaml (~=6.0.1)
+Requires-Dist: kubernetes (~=27.2.0)
 
 # kube-py
 Use OOP to manage Kubernetes objects 
 
 ### Usages
 ```python
 import kube
```

## Comparing `kube_ops-1.0.1.dist-info/RECORD` & `kube_ops-1.0.2.dist-info/RECORD`

 * *Files 17% similar despite different names*

```diff
@@ -1,12 +1,12 @@
-kube/__init__.py,sha256=32JoiD_mHLjRPJu3PGBeHAWWbLHd795b6KYGpmAfOGk,1311
+kube/__init__.py,sha256=C7bskcMvkVYH2EoqnLUWBnv3GvTab-fEP_aFolr3uNY,1310
+kube/api.py,sha256=EBURovq7vq7BAbQBVu2Ux5GlXQc6cWqCt912Ty8Ri1g,32538
 kube/common.py,sha256=XRpVZJz700HSeErD7gFc1dWzT5GQlrhB1jEuxQ48N0Q,2611
-kube/config.py,sha256=mcvFXDVK95AWvMyl8otrOQW6M4R_pv16Qrirv9PHmCA,5081
+kube/config.py,sha256=iVa7oi0Rn3HerTlfq0OLbd_GJYhzzubkbki9AL1Q8_U,5080
 kube/enums.py,sha256=egCkn8c3AJKzuYjKkbiX5re4J1z1rIiJc6WQcVvL9ug,1197
-kube/kube.py,sha256=EBURovq7vq7BAbQBVu2Ux5GlXQc6cWqCt912Ty8Ri1g,32538
 kube/manifests.py,sha256=Xuftc2TeJ-F0HBSg8bQSr8RaKMntHC2Hv_rKTS6KMZI,19115
 kube/templates.py,sha256=9KcL3RUK9bexg6USf3Jp752bDND0pqzsZQSpd7A8ZtA,10932
-kube_ops-1.0.1.dist-info/LICENSE,sha256=4UMudA3MzI411FVQKHbbLdnwm2GjFrbv5LBNk5ZTT8Y,1069
-kube_ops-1.0.1.dist-info/METADATA,sha256=1EF7O_YqVoZkECCpEpjwZslXlqtUW3msfc5kcRtQX6s,3356
-kube_ops-1.0.1.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-kube_ops-1.0.1.dist-info/top_level.txt,sha256=VviGlBjAU4SlS_NC5yQCpy0uOZb8yzwuA9KQU4Tvrgc,5
-kube_ops-1.0.1.dist-info/RECORD,,
+kube_ops-1.0.2.dist-info/LICENSE,sha256=4UMudA3MzI411FVQKHbbLdnwm2GjFrbv5LBNk5ZTT8Y,1069
+kube_ops-1.0.2.dist-info/METADATA,sha256=aTYSBVCPtEPCfjphUhYQUuL1kTg7M3rZ0gWwDWjeAMY,3425
+kube_ops-1.0.2.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+kube_ops-1.0.2.dist-info/top_level.txt,sha256=VviGlBjAU4SlS_NC5yQCpy0uOZb8yzwuA9KQU4Tvrgc,5
+kube_ops-1.0.2.dist-info/RECORD,,
```

