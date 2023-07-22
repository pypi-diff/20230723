# Comparing `tmp/threemystic_cloud_data_client-0.1.33.tar.gz` & `tmp/threemystic_cloud_data_client-0.1.34.tar.gz`

## Comparing `threemystic_cloud_data_client-0.1.33.tar` & `threemystic_cloud_data_client-0.1.34.tar`

### file list

```diff
@@ -1,45 +1,45 @@
--rw-r--r--   0        0        0      212 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/__main__.py
--rw-r--r--   0        0        0       23 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/__version__.py
--rw-r--r--   0        0        0     3895 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_data_client.py
--rw-r--r--   0        0        0     4150 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cli/__init__.py
--rw-r--r--   0        0        0     2950 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cli/actions/base_class/base.py
--rw-r--r--   0        0        0      702 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cli/actions/config/__init__.py
--rw-r--r--   0        0        0      568 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/__init__.py
--rw-r--r--   0        0        0      260 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/base_class/base.py
--rw-r--r--   0        0        0      325 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/client/__init__.py
--rw-r--r--   0        0        0    17529 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/client/actions/vm.py
--rw-r--r--   0        0        0     1481 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/client/actions/vmimage.py
--rw-r--r--   0        0        0     5122 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/client/actions/base_class/base.py
--rw-r--r--   0        0        0     3032 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/config/step_1.py
--rw-r--r--   0        0        0      443 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/config/base_class/base.py
--rw-r--r--   0        0        0      583 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/__init__.py
--rw-r--r--   0        0        0      264 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/base_class/base.py
--rw-r--r--   0        0        0      331 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/__init__.py
--rw-r--r--   0        0        0    23320 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/budget.py
--rw-r--r--   0        0        0     4629 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/certificates.py
--rw-r--r--   0        0        0     5358 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/cloudstorage.py
--rw-r--r--   0        0        0    11867 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/database.py
--rw-r--r--   0        0        0     2315 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/datawarehouse.py
--rw-r--r--   0        0        0    10075 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/dns.py
--rw-r--r--   0        0        0     1691 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/memorydb.py
--rw-r--r--   0        0        0     5647 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/secrets.py
--rw-r--r--   0        0        0    13040 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/storage.py
--rw-r--r--   0        0        0    13572 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vm.py
--rw-r--r--   0        0        0     3094 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vmimage.py
--rw-r--r--   0        0        0     3092 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vmss.py
--rw-r--r--   0        0        0      986 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/base_class/base.py
--rw-r--r--   0        0        0     2917 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/config/step_1.py
--rw-r--r--   0        0        0      445 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/config/base_class/base.py
--rw-r--r--   0        0        0     8657 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/base_class/base.py
--rw-r--r--   0        0        0    11700 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/base_class/base_client.py
--rw-r--r--   0        0        0    22664 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/base_class/base_data.py
--rw-r--r--   0        0        0      593 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/general/__init__.py
--rw-r--r--   0        0        0     4709 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/general/config/step_1.py
--rw-r--r--   0        0        0    14025 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/general/config/step_2.py
--rw-r--r--   0        0        0      396 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/general/config/base_class/base.py
--rw-r--r--   0        0        0     1799 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/.gitignore
--rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/LICENSE
--rw-r--r--   0        0        0     2715 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/README.md
--rw-r--r--   0        0        0      692 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/hatch.toml
--rw-r--r--   0        0        0     3783 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/pyproject.toml
--rw-r--r--   0        0        0     4677 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.33/PKG-INFO
+-rw-r--r--   0        0        0      212 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/__main__.py
+-rw-r--r--   0        0        0       23 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/__version__.py
+-rw-r--r--   0        0        0     3895 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_data_client.py
+-rw-r--r--   0        0        0     4150 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cli/__init__.py
+-rw-r--r--   0        0        0     2950 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cli/actions/base_class/base.py
+-rw-r--r--   0        0        0      702 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cli/actions/config/__init__.py
+-rw-r--r--   0        0        0      568 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/__init__.py
+-rw-r--r--   0        0        0      260 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/base_class/base.py
+-rw-r--r--   0        0        0      325 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/client/__init__.py
+-rw-r--r--   0        0        0    17992 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/client/actions/vm.py
+-rw-r--r--   0        0        0     1481 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/client/actions/vmimage.py
+-rw-r--r--   0        0        0     5122 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/client/actions/base_class/base.py
+-rw-r--r--   0        0        0     3032 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/config/step_1.py
+-rw-r--r--   0        0        0      443 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/config/base_class/base.py
+-rw-r--r--   0        0        0      583 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/__init__.py
+-rw-r--r--   0        0        0      264 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/base_class/base.py
+-rw-r--r--   0        0        0      331 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/__init__.py
+-rw-r--r--   0        0        0    23320 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/budget.py
+-rw-r--r--   0        0        0     4629 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/certificates.py
+-rw-r--r--   0        0        0     5358 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/cloudstorage.py
+-rw-r--r--   0        0        0    11867 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/database.py
+-rw-r--r--   0        0        0     2315 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/datawarehouse.py
+-rw-r--r--   0        0        0    10075 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/dns.py
+-rw-r--r--   0        0        0     1691 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/memorydb.py
+-rw-r--r--   0        0        0     5647 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/secrets.py
+-rw-r--r--   0        0        0    13040 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/storage.py
+-rw-r--r--   0        0        0    13572 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vm.py
+-rw-r--r--   0        0        0     3094 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vmimage.py
+-rw-r--r--   0        0        0     3092 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vmss.py
+-rw-r--r--   0        0        0      986 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/base_class/base.py
+-rw-r--r--   0        0        0     2917 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/config/step_1.py
+-rw-r--r--   0        0        0      445 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/config/base_class/base.py
+-rw-r--r--   0        0        0     8657 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/base_class/base.py
+-rw-r--r--   0        0        0    11700 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/base_class/base_client.py
+-rw-r--r--   0        0        0    22664 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/base_class/base_data.py
+-rw-r--r--   0        0        0      593 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/general/__init__.py
+-rw-r--r--   0        0        0     4709 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/general/config/step_1.py
+-rw-r--r--   0        0        0    14025 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/general/config/step_2.py
+-rw-r--r--   0        0        0      396 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/general/config/base_class/base.py
+-rw-r--r--   0        0        0     1799 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/.gitignore
+-rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/LICENSE
+-rw-r--r--   0        0        0     2715 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/README.md
+-rw-r--r--   0        0        0      692 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/hatch.toml
+-rw-r--r--   0        0        0     3783 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/pyproject.toml
+-rw-r--r--   0        0        0     4677 2020-02-02 00:00:00.000000 threemystic_cloud_data_client-0.1.34/PKG-INFO
```

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_data_client.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_data_client.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cli/__init__.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cli/__init__.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cli/actions/base_class/base.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cli/actions/base_class/base.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cli/actions/config/__init__.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cli/actions/config/__init__.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/__init__.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/__init__.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/client/actions/vm.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/client/actions/vm.py`

 * *Files 4% similar despite different names*

```diff
@@ -80,23 +80,35 @@
 
     for asg in groups:
       for instance in asg["Instances"]:
         return_data[instance["InstanceId"]] = self.__get_asg_extra_data(asg_data= asg)
     
     return return_data
   
-  async def __process_account_region_lbinstances_targethealth(self, alb_client, targetgroup_arn, *args, **kwargs):
-    return alb_client.describe_target_health(TargetGroupArn=targetgroup_arn)
+  async def __process_account_region_lb_instances_targethealth(self, alb_client, targetgroup_arn, *args, **kwargs):
+    return self.get_cloud_client().general_boto_call_array(
+      boto_call=lambda: alb_client.describe_target_health(TargetGroupArn=targetgroup_arn),
+      boto_params= None,
+      boto_nextkey = None,
+      boto_key="LoadBalancerDescriptions",
+      logger = self.get_common().get_logger()
+    )
 
-  async def __process_account_region_lbinstances_targetgroups(self, alb_client, lb_arn, *args, **kwargs):
-    return alb_client.describe_target_groups(LoadBalancerArn=lb_arn)
+  async def __process_account_region_lb_instances_targetgroups(self, alb_client, lb_arn, *args, **kwargs):
+    return self.get_cloud_client().general_boto_call_array(
+      boto_call=lambda: alb_client.describe_target_groups(LoadBalancerArn=lb_arn),
+      boto_params= None,
+      boto_nextkey = None,
+      boto_key="LoadBalancerDescriptions",
+      logger = self.get_common().get_logger()
+    )
   
-  async def __process_account_region_lbinstances(self, account, region, loop, *args, **kwargs):
+  async def __process_account_region_lb_instances(self, account, region, loop, *args, **kwargs):
 
-      lbInstances = {}
+      lb_instances = {}
       
       elbClassic = self.get_cloud_client().get_boto_client(
         client= "elb",
         account= account,
         region= region
       )
 
@@ -105,23 +117,23 @@
         boto_params={},
         boto_nextkey = None,
         boto_key="LoadBalancerDescriptions",
         logger = self.get_common().get_logger()
       )
       
       for elb in elbs:
-        numInstances = len(elb['Instances'])
-        if numInstances < 1:
+        num_instances = len(elb['Instances'])
+        if num_instances < 1:
           continue
         for i in elb['Instances']:
-          if not i['InstanceId'] in lbInstances:
-            lbInstances[i['InstanceId']] = {}
-          if elb['LoadBalancerName'] in lbInstances[i['InstanceId']]:
+          if not i['InstanceId'] in lb_instances:
+            lb_instances[i['InstanceId']] = {}
+          if elb['LoadBalancerName'] in lb_instances[i['InstanceId']]:
             continue
-          lbInstances[i['InstanceId']][elb['LoadBalancerName']] = ({"instance": i['InstanceId'], "lbType": "ELB", "lbName": elb['LoadBalancerName'], "lbDNSName": elb['DNSName']})
+          lb_instances[i['InstanceId']][elb['LoadBalancerName']] = ({"instance": i['InstanceId'], "lbType": "ELB", "lbName": elb['LoadBalancerName'], "lbDNSName": elb['DNSName']})
       
       alb = self.get_cloud_client().get_boto_client(
         client= "elbv2",
         account= account,
         region= region
       )
 
@@ -129,44 +141,44 @@
         boto_call=lambda item: alb.describe_load_balancers(),
         boto_params={},
         boto_nextkey = None,
         boto_key="LoadBalancers",
         logger = self.get_common().get_logger()
       )
       if len(albs) < 1:
-        return lbInstances
+        return lb_instances
 
       targetGroups = { 
-        lb['LoadBalancerArn']: loop.create_task(self.__process_account_region_lbinstances_targetgroups(alb_client= alb, lb_arn= lb['LoadBalancerArn'])) for lb in albs
+        lb['LoadBalancerArn']: loop.create_task(self.__process_account_region_lb_instances_targetgroups(alb_client= alb, lb_arn= lb['LoadBalancerArn'])) for lb in albs
       }
       
       if len(targetGroups) < 1:
-        return lbInstances
+        return lb_instances
       await asyncio.wait(targetGroups.values())
     
-      for lb in albs:   
+      for lb in albs:
         targets_health = {
-          group['TargetGroupArn']: loop.create_task(self.__process_account_region_lbinstances_targethealth(alb_client= alb, targetgroup_arn= group['TargetGroupArn'])) for group in targetGroups[lb['LoadBalancerArn']].result()['TargetGroups']
+          group['TargetGroupArn']: loop.create_task(self.__process_account_region_lb_instances_targethealth(alb_client= alb, targetgroup_arn= group['TargetGroupArn'])) for group in targetGroups[lb['LoadBalancerArn']].result()['TargetGroups']
         }  
         if len(targets_health) < 1:
          continue
         await asyncio.wait(targets_health.values())     
 
         for _, targets in targets_health.items():
           for target in targets.result()['TargetHealthDescriptions']:
             if len(target['Target']) < 1:
               continue
 
-            if not target['Target']['Id'] in lbInstances:
-              lbInstances[target['Target']['Id']] = {}
-            if lb['LoadBalancerName'] in lbInstances[target['Target']['Id']]:
+            if not target['Target']['Id'] in lb_instances:
+              lb_instances[target['Target']['Id']] = {}
+            if lb['LoadBalancerName'] in lb_instances[target['Target']['Id']]:
               continue
-            lbInstances[target['Target']['Id']][lb['LoadBalancerName']] = ({"instance": target['Target']['Id'], "lbType": "ALB", "lbName": lb['LoadBalancerName'], "lbDNSName": lb['DNSName']})        
+            lb_instances[target['Target']['Id']][lb['LoadBalancerName']] = ({"instance": target['Target']['Id'], "lbType": "ALB", "lbName": lb['LoadBalancerName'], "lbDNSName": lb['DNSName']})        
       
-      return lbInstances
+      return lb_instances
   
   async def __get_ec2_volume_details(self, ec2_client, *args, **kwargs):
         
       volumne_data = self.get_cloud_client().general_boto_call_array(
         boto_call=lambda item: ec2_client.describe_volumes(**item),
         boto_params={},
         boto_nextkey = "NextToken",
@@ -267,30 +279,30 @@
         "PlatformName": instance_information.get('PlatformName'),
         "PlatformVersion": instance_information.get('PlatformVersion'),
         "PingStatus": instance_information.get('PingStatus'),
         "PingTime": instance_information.get('LastPingDateTime'),
         "Version": instance_information.get('AgentVersion'),
     } 
   
-  async def __get_instance_withextra_data(self, ec2_client, ssm_client, task_asg_by_instance, account, region, lbInstances, instance, loop, *args, **kwargs):
+  async def __get_instance_withextra_data(self, ec2_client, ssm_client, task_asg_by_instance, account, region, lb_instances, instance, loop, *args, **kwargs):
       
       
       extra_data_tasks = {
         "extra_image": loop.create_task(self.__getImageInfo(imageId= instance["ImageId"])),
         "extra_instance_attributes": loop.create_task(self.__get_instance_attribute(account=account, client= ec2_client, instance=instance, loop= loop)),
         "extra_ssminfo": loop.create_task(self.__getSSMInfo(account=account, region=region, ssm_client=ssm_client, instance=instance)),
         "_ignore_extra_asg": task_asg_by_instance
         
       }      
 
       extra_data = {
         "extra_platform": instance["Platform"] if not self.get_common().helper_type().string().is_null_or_whitespace(string_value= instance.get("Platform")) else "Linux",
         "extra_subnet": instance["SubnetId"] if instance.get("SubnetId") is not None else "EC2Classic",
         "extra_vpc": instance["VpcId"] if instance.get("VpcId") is not None else "EC2Classic",
-        "extra_lb": lbInstances.get(instance["InstanceId"]) if lbInstances is not None else None,
+        "extra_lb": lb_instances.get(instance["InstanceId"]) if lb_instances is not None else None,
       }
 
       await asyncio.wait(extra_data_tasks.values())
 
       for key,item in extra_data_tasks.items():
         if key.lower().startswith("_ignore_"):
           continue
@@ -327,15 +339,15 @@
       logger = self.get_common().get_logger()
     )
 
     if len(instances_reservations) < 1:
       return []
 
     pre_process_tasks = {
-      "lb_instances": loop.create_task(self.__process_account_region_lbinstances(account, region, loop, *args, **kwargs)),
+      "lb_instances": loop.create_task(self.__process_account_region_lb_instances(account, region, loop, *args, **kwargs)),
       "volume_details": loop.create_task(self.__get_ec2_volume_details(ec2_client= ec2_client, *args, **kwargs))
 
     }
     await asyncio.wait(pre_process_tasks.values())
     
   
     instance_tasks = []
@@ -343,15 +355,15 @@
     instance_ebs_encrypted = {}
     for reservation in instances_reservations:
       for instance in reservation["Instances"]:
         if (instance["State"].get("Name")).lower() == "terminated":
           continue
         
         instance_ebs_encrypted[instance[self.data_id_name]] = None
-        instance_tasks.append(loop.create_task(self.__get_instance_withextra_data(ec2_client=ec2_client, ssm_client= ssm_client, task_asg_by_instance= task_asg_by_instance, account= account, region= region, lbInstances=pre_process_tasks["lb_instances"].result(), instance= instance, loop= loop)))
+        instance_tasks.append(loop.create_task(self.__get_instance_withextra_data(ec2_client=ec2_client, ssm_client= ssm_client, task_asg_by_instance= task_asg_by_instance, account= account, region= region, lb_instances=pre_process_tasks["lb_instances"].result(), instance= instance, loop= loop)))
         if instance.get("BlockDeviceMappings") is not None:
           for block_device in instance["BlockDeviceMappings"]:
             if block_device.get("Ebs") is None:
               instance_ebs_encrypted[instance[self.data_id_name]] = self.__is_ec2_ebs_encrypted_state(
                 running_state= instance_ebs_encrypted[instance[self.data_id_name]],
                 block_device_details= None
               )
```

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/client/actions/vmimage.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/client/actions/vmimage.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/client/actions/base_class/base.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/client/actions/base_class/base.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/aws/config/step_1.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/aws/config/step_1.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/__init__.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/__init__.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/budget.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/budget.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/certificates.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/certificates.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/cloudstorage.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/cloudstorage.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/database.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/database.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/datawarehouse.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/datawarehouse.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/dns.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/dns.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/memorydb.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/memorydb.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/secrets.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/secrets.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/storage.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/storage.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vm.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vm.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vmimage.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vmimage.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vmss.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/vmss.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/client/actions/base_class/base.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/client/actions/base_class/base.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/azure/config/step_1.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/azure/config/step_1.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/base_class/base.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/base_class/base.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/base_class/base_client.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/base_class/base_client.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/base_class/base_data.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/base_class/base_data.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/general/__init__.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/general/__init__.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/general/config/step_1.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/general/config/step_1.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/threemystic_cloud_data_client/cloud_providers/general/config/step_2.py` & `threemystic_cloud_data_client-0.1.34/threemystic_cloud_data_client/cloud_providers/general/config/step_2.py`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/.gitignore` & `threemystic_cloud_data_client-0.1.34/.gitignore`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/LICENSE` & `threemystic_cloud_data_client-0.1.34/LICENSE`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/README.md` & `threemystic_cloud_data_client-0.1.34/README.md`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/hatch.toml` & `threemystic_cloud_data_client-0.1.34/hatch.toml`

 * *Files identical despite different names*

### Comparing `threemystic_cloud_data_client-0.1.33/pyproject.toml` & `threemystic_cloud_data_client-0.1.34/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -24,15 +24,15 @@
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = [
   "colorama; platform_system == 'Windows'",
   "threemystic-common >= 0.1.17",
-  "threemystic-cloud-client >= 0.1.48",
+  "threemystic-cloud-client >= 0.1.49",
   "typing-extensions >= 4.4.0",
   "asyncio >= 3.4.3",
   "tqdm >= 4.65.0",
   "azure-mgmt-compute >= 29",
   "azure-mgmt-cosmosdb >= 9",
   "azure-mgmt-costmanagement >= 4",
   "azure-mgmt-dns >= 8",
```

### Comparing `threemystic_cloud_data_client-0.1.33/PKG-INFO` & `threemystic_cloud_data_client-0.1.34/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: threemystic-cloud-data-client
-Version: 0.1.33
+Version: 0.1.34
 Summary: A tool for collecting data from various cloud providers
 Project-URL: Homepage, https://github.com/3MysticApes/3mystic_cloud_data_client
 Project-URL: Bug Tracker, https://github.com/3MysticApes/3mystic_cloud_data_client/issues
 Author: Ron Truex
 License-Expression: MIT
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
@@ -35,15 +35,15 @@
 Requires-Dist: azure-mgmt-redis>=14
 Requires-Dist: azure-mgmt-resourcegraph>=8
 Requires-Dist: azure-mgmt-sql>=3
 Requires-Dist: azure-mgmt-sqlvirtualmachine>=0.6
 Requires-Dist: azure-mgmt-subscription>=3
 Requires-Dist: azure-mgmt-synapse>=2
 Requires-Dist: colorama; platform_system == 'Windows'
-Requires-Dist: threemystic-cloud-client>=0.1.48
+Requires-Dist: threemystic-cloud-client>=0.1.49
 Requires-Dist: threemystic-common>=0.1.17
 Requires-Dist: tqdm>=4.65.0
 Requires-Dist: typing-extensions>=4.4.0
 Description-Content-Type: text/markdown
 
 # 3mystic_cloud_data_client
 A set of scripts to help uniformly pull data from the cloud providers for various resources.
```

