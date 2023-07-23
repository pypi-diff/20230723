# Comparing `tmp/fogLedger-3.0.1b0.tar.gz` & `tmp/fogLedger-3.0.2b0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fogLedger-3.0.1b0.tar", last modified: Wed Jul 12 03:10:07 2023, max compression
+gzip compressed data, was "fogLedger-3.0.2b0.tar", last modified: Sun Jul 23 04:57:20 2023, max compression
```

## Comparing `fogLedger-3.0.1b0.tar` & `fogLedger-3.0.2b0.tar`

### file list

```diff
@@ -1,30 +1,33 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 03:10:07.703019 fogLedger-3.0.1b0/
--rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1588 2023-07-12 03:10:07.703019 fogLedger-3.0.1b0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2171 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 03:10:07.699019 fogLedger-3.0.1b0/fogLedger.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1588 2023-07-12 03:10:07.000000 fogLedger-3.0.1b0/fogLedger.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      608 2023-07-12 03:10:07.000000 fogLedger-3.0.1b0/fogLedger.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-12 03:10:07.000000 fogLedger-3.0.1b0/fogLedger.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-12 03:10:07.000000 fogLedger-3.0.1b0/fogLedger.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-12 03:10:07.000000 fogLedger-3.0.1b0/fogLedger.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-12 03:10:07.000000 fogLedger-3.0.1b0/fogLedger.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 03:10:07.699019 fogLedger-3.0.1b0/fogledger/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 03:10:07.699019 fogLedger-3.0.1b0/fogledger/data/
--rw-r--r--   0 runner    (1001) docker     (123)     4389 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/data/config-coo.json
--rw-r--r--   0 runner    (1001) docker     (123)     4304 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/data/config-node.json
--rw-r--r--   0 runner    (1001) docker     (123)     4471 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/data/config-spammer.json
--rwxr-xr-x   0 runner    (1001) docker     (123)     3544 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/data/private-tangle.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     1704 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/data/utils.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 03:10:07.699019 fogLedger-3.0.1b0/fogledger/indy/
--rw-r--r--   0 runner    (1001) docker     (123)     5235 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/indy/IndyBasic.py
--rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/indy/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 03:10:07.703019 fogLedger-3.0.1b0/fogledger/iota/
--rw-r--r--   0 runner    (1001) docker     (123)     8362 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/iota/IotaBasic.py
--rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/iota/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1326 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/test-iota-distributed-network.py
--rw-r--r--   0 runner    (1001) docker     (123)      877 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/fogledger/test-iota-local-network.py
--rw-r--r--   0 runner    (1001) docker     (123)       84 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-12 03:10:07.703019 fogLedger-3.0.1b0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1913 2023-07-12 03:09:56.000000 fogLedger-3.0.1b0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:57:20.778889 fogLedger-3.0.2b0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1588 2023-07-23 04:57:20.774888 fogLedger-3.0.2b0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2171 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:57:20.774888 fogLedger-3.0.2b0/fogLedger.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1588 2023-07-23 04:57:20.000000 fogLedger-3.0.2b0/fogLedger.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      699 2023-07-23 04:57:20.000000 fogLedger-3.0.2b0/fogLedger.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 04:57:20.000000 fogLedger-3.0.2b0/fogLedger.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 04:57:20.000000 fogLedger-3.0.2b0/fogLedger.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-23 04:57:20.000000 fogLedger-3.0.2b0/fogLedger.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-23 04:57:20.000000 fogLedger-3.0.2b0/fogLedger.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:57:20.774888 fogLedger-3.0.2b0/fogledger/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:57:20.774888 fogLedger-3.0.2b0/fogledger/data/
+-rw-r--r--   0 runner    (1001) docker     (123)     4389 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/data/config-coo.json
+-rw-r--r--   0 runner    (1001) docker     (123)     4304 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/data/config-node.json
+-rw-r--r--   0 runner    (1001) docker     (123)     4471 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/data/config-spammer.json
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2934 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/data/private-tangle.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1704 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/data/utils.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:57:20.774888 fogLedger-3.0.2b0/fogledger/indy/
+-rw-r--r--   0 runner    (1001) docker     (123)     5235 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/indy/IndyBasic.py
+-rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/indy/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:57:20.774888 fogLedger-3.0.2b0/fogledger/iota/
+-rw-r--r--   0 runner    (1001) docker     (123)      278 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/iota/CoordConfig.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9647 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/iota/IotaBasic.py
+-rw-r--r--   0 runner    (1001) docker     (123)      219 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/iota/NodeConfig.py
+-rw-r--r--   0 runner    (1001) docker     (123)      288 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/iota/SpammerConfig.py
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/iota/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1326 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/test-iota-distributed-network.py
+-rw-r--r--   0 runner    (1001) docker     (123)      877 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/fogledger/test-iota-local-network.py
+-rw-r--r--   0 runner    (1001) docker     (123)       84 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 04:57:20.778889 fogLedger-3.0.2b0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1913 2023-07-23 04:57:08.000000 fogLedger-3.0.2b0/setup.py
```

### Comparing `fogLedger-3.0.1b0/LICENSE.txt` & `fogLedger-3.0.2b0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `fogLedger-3.0.1b0/PKG-INFO` & `fogLedger-3.0.2b0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fogLedger
-Version: 3.0.1b0
+Version: 3.0.2b0
 Summary: Plugin to build DLTs in Fogbed.
 Home-page: https://github.com/larsid/FogLedger/tree/v2.0.0
 Author: Matheus Nascimento
 Author-email: matheusnascimentoti99@gmail.com
 Keywords: networking,emulator,protocol,Internet,dlt,indy,fog
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `fogLedger-3.0.1b0/README.md` & `fogLedger-3.0.2b0/README.md`

 * *Files identical despite different names*

### Comparing `fogLedger-3.0.1b0/fogLedger.egg-info/PKG-INFO` & `fogLedger-3.0.2b0/fogLedger.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fogLedger
-Version: 3.0.1b0
+Version: 3.0.2b0
 Summary: Plugin to build DLTs in Fogbed.
 Home-page: https://github.com/larsid/FogLedger/tree/v2.0.0
 Author: Matheus Nascimento
 Author-email: matheusnascimentoti99@gmail.com
 Keywords: networking,emulator,protocol,Internet,dlt,indy,fog
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `fogLedger-3.0.1b0/fogLedger.egg-info/SOURCES.txt` & `fogLedger-3.0.2b0/fogLedger.egg-info/SOURCES.txt`

 * *Files 9% similar despite different names*

```diff
@@ -14,9 +14,12 @@
 fogledger/data/config-coo.json
 fogledger/data/config-node.json
 fogledger/data/config-spammer.json
 fogledger/data/private-tangle.sh
 fogledger/data/utils.sh
 fogledger/indy/IndyBasic.py
 fogledger/indy/__init__.py
+fogledger/iota/CoordConfig.py
 fogledger/iota/IotaBasic.py
+fogledger/iota/NodeConfig.py
+fogledger/iota/SpammerConfig.py
 fogledger/iota/__init__.py
```

### Comparing `fogLedger-3.0.1b0/fogledger/data/config-coo.json` & `fogLedger-3.0.2b0/fogledger/data/config-coo.json`

 * *Files identical despite different names*

### Comparing `fogLedger-3.0.1b0/fogledger/data/config-node.json` & `fogLedger-3.0.2b0/fogledger/data/config-node.json`

 * *Files identical despite different names*

### Comparing `fogLedger-3.0.1b0/fogledger/data/config-spammer.json` & `fogLedger-3.0.2b0/fogledger/data/config-spammer.json`

 * *Files identical despite different names*

### Comparing `fogLedger-3.0.1b0/fogledger/data/private-tangle.sh` & `fogLedger-3.0.2b0/fogledger/data/private-tangle.sh`

 * *Files 20% similar despite different names*

```diff
@@ -22,57 +22,34 @@
 fi
 
 command="$1"
 
 ip_address=$(echo $(dig +short myip.opendns.com @resolver1.opendns.com))
 COO_BOOTSTRAP_WAIT=10
 
-nodes="$2"
-# Split the node details string
-extra_nodes=($(echo "$nodes" | tr ':' ' '))
-
 
 
 clean () {
   if [ -d ./snapshots/private-tangle ]; then
     sudo rm -Rf ./snapshots/private-tangle/*
   fi
 
   # We need to do this so that initially the permissions are user's permissions
-  resetPeeringFile config/peering-spammer.json
-  resetPeeringFile config/peering-coo.json
-  if [ -n "${extra_nodes}" ]; then
-      for node in "${extra_nodes[@]}"; do
-        peering_path="config/peering-${node}.json"
-        echo "Resetting ${peering_path}"
-        resetPeeringFile "${peering_path}"
-      done
-  fi
+  #resetPeeringFile config/peering-spammer.json
+  #resetPeeringFile config/peering-coo.json
 }
 
 # Sets up the necessary directories if they do not exist yet
 volumeSetup () {
   mkdir -p "/tmp/iota/config"
   cp -r config-node.json "/tmp/iota/config/config-node.json"
   cp -r config-coo.json "/tmp/iota/config/config-coo.json"
   cp -r config-spammer.json "/tmp/iota/config/config-spammer.json"
   cd "/tmp/iota"
 
-  if ! [ -d ./config ]; then
-    mkdir ./config
-  else
-    cd ./config
-    for node in "${extra_nodes[@]}"; do
-      echo "Copying config-node.json to config-${node}.json"
-      cp config-node.json config-${node}.json
-      sed -i 's/node1/'$node'/g' config-${node}.json
-    done
-    cd ..
-  fi
-
   # Snapshots
   if ! [ -d ./snapshots ]; then
     mkdir ./snapshots
   fi
   
   if ! [ -d ./snapshots/private-tangle ]; then
     mkdir ./snapshots/private-tangle
```

### Comparing `fogLedger-3.0.1b0/fogledger/data/utils.sh` & `fogLedger-3.0.2b0/fogledger/data/utils.sh`

 * *Files identical despite different names*

### Comparing `fogLedger-3.0.1b0/fogledger/indy/IndyBasic.py` & `fogLedger-3.0.2b0/fogledger/indy/IndyBasic.py`

 * *Files identical despite different names*

### Comparing `fogLedger-3.0.1b0/fogledger/iota/IotaBasic.py` & `fogLedger-3.0.2b0/fogledger/iota/IotaBasic.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,32 +1,40 @@
 from fogbed import (
     Container, VirtualInstance, FogbedExperiment
 )
+from .NodeConfig import NodeConfig
+from .CoordConfig import CoordConfig
+from .SpammerConfig import SpammerConfig
 from typing import List
 from typing import Dict
 import os
 import json
 import time
 import subprocess
 import pkg_resources
 
 
 class IotaBasic:
     def __init__(
         self,
         exp: FogbedExperiment,
         prefix: str = 'cloud',
-        nodes: List[Dict[str, str]] = []
+        conf_nodes: List[NodeConfig] = [],
+        conf_coord: CoordConfig = None,
+        conf_spammer: SpammerConfig = None
     ) -> None:
         self.ledgers: List[VirtualInstance] = []
         self.nodes: Dict[str, Container] = {}
         self.exp = exp
         self.prefix = prefix
-        self.startScript(nodes)
-        self.createContainers(nodes)
+        self.conf_nodes = conf_nodes
+        self.conf_coord = conf_coord
+        self.conf_spammer = conf_spammer
+        self.startScript()
+        self.createContainers()
 
     def add_ledger(self, prefix: str, nodes: List[Container]):
         ledger = self.exp.add_virtual_instance(f'{prefix}')
         self._create_nodes(ledger, nodes)
         self.ledgers.append(ledger)
         return self.ledgers
 
@@ -39,65 +47,84 @@
         return nodes
 
     @staticmethod
     def read_file(file_path):
         with open(file_path, 'r') as file:
             return file.read()
 
-    def startScript(self, nodes: List[Dict[str, str]]):
+    def startScript(self):
         print("starting script...")
-        node_names = [node['name'] for node in nodes]
-        concatenated_string = ":".join(node_names)
         path_script = pkg_resources.resource_filename('fogledger', 'data')
         path_private_tangle = os.path.join(path_script, "private-tangle.sh")
         subprocess.run(["chmod", "+x", path_private_tangle])
-        subprocess.run(["/bin/bash", path_private_tangle, "install",
-                       concatenated_string], check=True, cwd=path_script)
+        subprocess.run(["/bin/bash", path_private_tangle, "install"], check=True, cwd=path_script)
         print("finished script...")
 
-    def createContainers(self, nodes: List[str]):
+    def createContainers(self):
         ### NODES ###
-        for index, nodeLabel in enumerate(nodes):
-            name = nodeLabel['name'] if (
-                "name" in nodeLabel) else str(index)
-            
-            ip = nodeLabel['ip'] if ("ip" in nodeLabel) else None
-            
-            port_bindings = nodeLabel['port_bindings'] if ("port_bindings" in nodeLabel) else {}
+        for index, node_conf in enumerate(self.conf_nodes):
+            name = node_conf.name
+            ip = node_conf.ip
+            port_bindings = node_conf.port_bindings
             
             node = Container(
                 name=name,
                 dimage='larsid/fogbed-iota-node:v3.0.0-beta',
                 ip=ip,
                 port_bindings=port_bindings,
                 ports=['14265', '8081', '1883', '15600', '14626/udp']
             )
-            self.add_ledger(f'ledger-{node.name}', [node])
+            self.add_ledger(f'ledger-{name}{index}', [node])
 
         ### COO ###
         coo = Container(
-            name='coo',
+            name=self.conf_coord.name,
+            ip = self.conf_coord.ip,
+            port_bindings = self.conf_coord.port_bindings,
             dimage='larsid/fogbed-iota-node:v3.0.0-beta',
             environment={'COO_PRV_KEYS': ''},
             ports=['15600']
         )
         self.add_ledger(f'ledger-{coo.name}', [coo])
 
         ### spammer ###
         spammer = Container(
-            name="spammer",
+            name= self.conf_spammer.name,
+            ip = self.conf_spammer.ip,
+            port_bindings = self.conf_spammer.port_bindings,
             dimage='larsid/fogbed-iota-node:v3.0.0-beta',
             ports=['15600', '14626/udp']
         )
         self.add_ledger(f'ledger-{spammer.name}', [spammer])
 
     def searchNode(self, node_name: str):
         for node in self.nodes.values():
             if node.name == node_name:
                 return node
+    
+    def configureNodes(self):
+        print("\nConfiguring nodes...")
+        file_path = os.path.join("/tmp", "iota")
+        config_file_coor = json.loads(IotaBasic.read_file(f"{file_path}/config/config-coo.json"))
+        config_file_spammer = json.loads(IotaBasic.read_file(f"{file_path}/config/config-spammer.json"))
+        config_file_node = json.loads(IotaBasic.read_file(f"{file_path}/config/config-node.json"))
+        for node in self.nodes.values():
+            json_data = {}
+            if(node.name == self.conf_coord.name):
+                json_data = config_file_coor
+                json_data["coordinator"]["interval"] = self.conf_coord.interval
+            elif(node.name == self.conf_spammer.name):
+                json_data = config_file_spammer
+                json_data["spammer"]["message"] = self.conf_spammer.message
+            else:
+                json_data = config_file_node
+            json_data["node"]["alias"] = node.name
+            updated_data = json.dumps(json_data)
+            node.cmd(f"echo \'{updated_data}\' | jq . > /app/config.json")
+        print("Nodes configured! ✅")
 
     # P2P identities are generated for each node
     def setupIdentities(self):
         print("\nGenerating P2P identities for each node")
         for node in self.nodes.values():
             node.cmd(f'./hornet tool p2pidentity-gen > {node.name}.identity.txt')
         print("P2P identities generated! ✅")
@@ -117,58 +144,55 @@
                     node_int.cmd(f"echo \'{updated_data}\' | jq . > /app/peering.json")
         print("peerID extracted! ✅")
 
     # Sets the Coordinator up by creating a key pair
     def setupCoordinator(self):
         print("\nSetting up the Coordinator")
         coo_key_pair_file = "coo-milestones-key-pair.txt"
-        coo = self.searchNode("coo")
+        coo = self.searchNode(self.conf_coord.name)
         if coo is not None:
             coo.cmd('mkdir -p /app/coo-state')
             coo.cmd(f'./hornet tool ed25519-key > {coo_key_pair_file}')
             COO_PRV_KEYS = coo.cmd(
                 f'cat {coo_key_pair_file} | awk -F : \'{{if ($1 ~ /private key/) print $2}}\' | sed "s/ \+//g" | tr -d "\n" | tr -d "\r"').strip("> >")
             coo.cmd(f'export COO_PRV_KEYS={COO_PRV_KEYS}')
             coo_public_key = coo.cmd(
                 f'cat {coo_key_pair_file} | awk -F : \'{{if ($1 ~ /public key/) print $2}}\' | sed "s/ \+//g" | tr -d "\n" | tr -d "\r"').strip("> >")
-            
             file_path = os.path.join("/tmp", "iota")
             command = f'echo {coo_public_key} > {file_path}/coo-milestones-public-key.txt'
             os.system(command)
             for node in self.nodes.values():
-                json_data = IotaBasic.read_file(f"{file_path}/config/config-{node.name}.json")
+                json_data = node.cmd(f'cat /app/config.json').strip("> >")
                 json_data = json.loads(json_data)
                 json_data["protocol"]["publicKeyRanges"][0]["key"] = coo_public_key
                 updated_data = json.dumps(json_data)
                 node.cmd(f"echo \'{updated_data}\' | jq . > /app/config.json")
             print("Coordinator set up! ✅")
         else:
             print("Coordinator not found! ❌")
 
     def copySnapshotToNodes(self):
         print("\nCopying snapshot to each node")
         # Executar o comando base64 no arquivo full_snapshot.bin e capturar a saída
         file_path = os.path.join("/tmp", "iota", "snapshots", "private-tangle","full_snapshot.bin")
         command = f"base64 {file_path}"
         output = subprocess.run(command, capture_output=True, text=True, shell=True).stdout
-        print(output)
         # Salvar a saída em uma variável
         output_b64 = output.strip()
-        print("veio")
         for node in self.nodes.values():
             node.cmd("mkdir -p /app/snapshots/private-tangle")
             node.cmd(f"echo '{output_b64}' | base64 -d > /app/snapshots/private-tangle/full_snapshot.bin")
 
         print("Snapshot copied! ✅")
 
     # Bootstraps the coordinator
     def bootstrapCoordinator(self):
         print("Bootstrapping the Coordinator...")
         # Need to do it again otherwise the coo will not bootstrap
-        coo = self.searchNode("coo")
+        coo = self.searchNode(self.conf_coord.name)
         if coo is not None:
             coo.cmd(
                 f'./hornet --cooBootstrap --cooStartIndex 0 > coo.bootstrap.log &')
             print("Waiting for $bootstrap_tick seconds ... ⏳")
             time.sleep(30)
             bootstrapped = coo.cmd(
                 'grep "milestone issued (1)" coo.bootstrap.log | cat')
@@ -188,14 +212,15 @@
             node.cmd(f'./hornet > {node.name}.log &')
             print(f"\nStarting {node.name}... ⏳")
             time.sleep(3)
             print(f"{node.name} is up and running! ✅")
 
     def start_network(self):
         print("\nStarting the network...")
+        self.configureNodes()
         self.setupIdentities()
         self.extractPeerID()
         self.copySnapshotToNodes()
         self.setupCoordinator()
         self.bootstrapCoordinator()
         self.startContainers()
         print("Network is up and running! ✅")
```

### Comparing `fogLedger-3.0.1b0/fogledger/test-iota-distributed-network.py` & `fogLedger-3.0.2b0/fogledger/test-iota-distributed-network.py`

 * *Files identical despite different names*

### Comparing `fogLedger-3.0.1b0/fogledger/test-iota-local-network.py` & `fogLedger-3.0.2b0/fogledger/test-iota-local-network.py`

 * *Files identical despite different names*

### Comparing `fogLedger-3.0.1b0/setup.py` & `fogLedger-3.0.2b0/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from setuptools import setup, find_packages
 
 
 setup(
     name="fogLedger",
-    version="3.0.1-beta",
+    version="3.0.2-beta",
     description='Plugin to build DLTs in Fogbed.',
     long_description='Plugin to build DLT in Fogbed. Suport Hyperledger Indy. \
         The FogLedger is a plugin for [Fogbed](https://github.com/larsid/fogbed). It allows you to emulate a fog network with distributed ledgers. \
         Currently, FogLedger has suport for Hyperledger Indy. It is a distributed ledger, purpose-built for decentralized identity. \
         It provides tools, libraries, and reusable components for creating and using independent digital identities rooted on blockchains or other distributed ledgers so that they are interoperable across administrative domains, applications, and any other silo. \
         Indy is interoperable with other blockchains or can be used standalone powering the decentralization of identity. \
         With FogLedger you can create a network of nodes running Hyperledger Indy. A emulation can have multiple networks of nodes running different distributed ledgers. \
```

