# Comparing `tmp/ciscopykit-2.1.2.tar.gz` & `tmp/ciscopykit-2.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ciscopykit-2.1.2.tar", last modified: Fri Jul 21 23:05:47 2023, max compression
+gzip compressed data, was "ciscopykit-2.1.3.tar", last modified: Sun Jul 23 09:03:55 2023, max compression
```

## Comparing `ciscopykit-2.1.2.tar` & `ciscopykit-2.1.3.tar`

### file list

```diff
@@ -1,52 +1,52 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.643316 ciscopykit-2.1.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1079 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/LICENSE.md
--rw-r--r--   0 runner    (1001) docker     (123)       98 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)      846 2023-07-21 23:05:47.643316 ciscopykit-2.1.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4186 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.639316 ciscopykit-2.1.2/ciscopykit/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1014 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/app.py
--rw-r--r--   0 runner    (1001) docker     (123)     8396 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/device.py
--rw-r--r--   0 runner    (1001) docker     (123)     1769 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/entry_point.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.639316 ciscopykit-2.1.2/ciscopykit/help/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/help/demo.py
--rw-r--r--   0 runner    (1001) docker     (123)     2268 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/interface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.639316 ciscopykit-2.1.2/ciscopykit/lan_security/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/lan_security/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7025 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/lan_security/app.py
--rw-r--r--   0 runner    (1001) docker     (123)     2096 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/lan_security/dhcp_snooping.py
--rw-r--r--   0 runner    (1001) docker     (123)     3440 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/lan_security/dynamic_arp_inspection.py
--rw-r--r--   0 runner    (1001) docker     (123)     2532 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/lan_security/stp_security.py
--rw-r--r--   0 runner    (1001) docker     (123)     2489 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/lan_security/switchport_security.py
--rw-r--r--   0 runner    (1001) docker     (123)     2503 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/lan_security/vlan_security.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.643316 ciscopykit-2.1.2/ciscopykit/routing/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/routing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4430 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/routing/dynamic_routing.py
--rw-r--r--   0 runner    (1001) docker     (123)     4553 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/routing/static_routing.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.643316 ciscopykit-2.1.2/ciscopykit/services/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/services/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2128 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/services/app.py
--rw-r--r--   0 runner    (1001) docker     (123)     1705 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/services/dhcp_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     1092 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/services/pat_service.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.643316 ciscopykit-2.1.2/ciscopykit/switch/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/switch/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2611 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/switch/app.py
--rw-r--r--   0 runner    (1001) docker     (123)      376 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/switch/l2_switch.py
--rw-r--r--   0 runner    (1001) docker     (123)     2246 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/switch/l3_switch.py
--rw-r--r--   0 runner    (1001) docker     (123)     5952 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/switch/switch.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.643316 ciscopykit-2.1.2/ciscopykit/templates/
--rw-r--r--   0 runner    (1001) docker     (123)     1963 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/templates/generate_router_config.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/templates/placeholder.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.643316 ciscopykit-2.1.2/ciscopykit/vlan/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/vlan/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/vlan/app.py
--rw-r--r--   0 runner    (1001) docker     (123)      996 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/ciscopykit/vlan/vlan.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 23:05:47.639316 ciscopykit-2.1.2/ciscopykit.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      846 2023-07-21 23:05:47.000000 ciscopykit-2.1.2/ciscopykit.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1209 2023-07-21 23:05:47.000000 ciscopykit-2.1.2/ciscopykit.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-21 23:05:47.000000 ciscopykit-2.1.2/ciscopykit.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      215 2023-07-21 23:05:47.000000 ciscopykit-2.1.2/ciscopykit.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       45 2023-07-21 23:05:47.000000 ciscopykit-2.1.2/ciscopykit.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-07-21 23:05:47.000000 ciscopykit-2.1.2/ciscopykit.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-21 23:05:47.643316 ciscopykit-2.1.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1425 2023-07-21 23:05:32.000000 ciscopykit-2.1.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.255138 ciscopykit-2.1.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1079 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/LICENSE.md
+-rw-r--r--   0 runner    (1001) docker     (123)       98 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)      846 2023-07-23 09:03:55.251138 ciscopykit-2.1.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4192 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.247138 ciscopykit-2.1.3/ciscopykit/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1014 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/app.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8396 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/device.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1769 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/entry_point.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.251138 ciscopykit-2.1.3/ciscopykit/help/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/help/demo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2268 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/interface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.251138 ciscopykit-2.1.3/ciscopykit/lan_security/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/lan_security/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7025 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/lan_security/app.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2096 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/lan_security/dhcp_snooping.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3440 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/lan_security/dynamic_arp_inspection.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2532 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/lan_security/stp_security.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2489 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/lan_security/switchport_security.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2503 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/lan_security/vlan_security.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.251138 ciscopykit-2.1.3/ciscopykit/routing/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/routing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14787 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/routing/dynamic_routing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4553 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/routing/static_routing.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.251138 ciscopykit-2.1.3/ciscopykit/services/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/services/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2128 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/services/app.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1705 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/services/dhcp_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1092 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/services/pat_service.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.251138 ciscopykit-2.1.3/ciscopykit/switch/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/switch/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2611 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/switch/app.py
+-rw-r--r--   0 runner    (1001) docker     (123)      376 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/switch/l2_switch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2246 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/switch/l3_switch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5952 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/switch/switch.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.251138 ciscopykit-2.1.3/ciscopykit/templates/
+-rw-r--r--   0 runner    (1001) docker     (123)     1963 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/templates/generate_router_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/templates/placeholder.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.251138 ciscopykit-2.1.3/ciscopykit/vlan/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/vlan/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/vlan/app.py
+-rw-r--r--   0 runner    (1001) docker     (123)      996 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/ciscopykit/vlan/vlan.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:03:55.251138 ciscopykit-2.1.3/ciscopykit.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      846 2023-07-23 09:03:55.000000 ciscopykit-2.1.3/ciscopykit.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1209 2023-07-23 09:03:55.000000 ciscopykit-2.1.3/ciscopykit.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 09:03:55.000000 ciscopykit-2.1.3/ciscopykit.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      215 2023-07-23 09:03:55.000000 ciscopykit-2.1.3/ciscopykit.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       45 2023-07-23 09:03:55.000000 ciscopykit-2.1.3/ciscopykit.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-07-23 09:03:55.000000 ciscopykit-2.1.3/ciscopykit.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 09:03:55.255138 ciscopykit-2.1.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1425 2023-07-23 09:03:37.000000 ciscopykit-2.1.3/setup.py
```

### Comparing `ciscopykit-2.1.2/LICENSE.md` & `ciscopykit-2.1.3/LICENSE.md`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/PKG-INFO` & `ciscopykit-2.1.3/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ciscopykit
-Version: 2.1.2
+Version: 2.1.3
 Summary: A network management toolkit for Cisco devices keeping track of devices when using GNS3 / Cisco Packet Tracer
 Home-page: https://github.com/Vincent-de-Torres-Portfolio/ciscopykit
 Author: devinci-it
 Author-email: vince.dev@icloud.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `ciscopykit-2.1.2/README.md` & `ciscopykit-2.1.3/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -6,17 +6,17 @@
 
 ## Features
 
 - Device Management: Add, remove, and modify Cisco devices effortlessly. *
 - Interface Management: Assign and remove IP addresses for network interfaces with ease. *
 - Configuration Management: Retrieve and update device configurations seamlessly. *
 -  IP Services Features :
-  - DHCP Service Configuration: Configure DHCP on network devices to efficiently manage IP address assignment.
-  - Port Address Translation (PAT) Configuration: Configure Port Address Translation (PAT) for simplified network address translation.
-  - L3 Switch Configuration: Generate and configure Layer 3 switch settings effortlessly.
+    - DHCP Service Configuration: Configure DHCP on network devices to efficiently manage IP address assignment.
+    - Port Address Translation (PAT) Configuration: Configure Port Address Translation (PAT) for simplified network address translation.
+    - L3 Switch Configuration: Generate and configure Layer 3 switch settings effortlessly.
 - LAN Security Features:
   - [Switchport Security](lan_security/README.md#switchport-security-module): Configure security settings for switchports to prevent unauthorized access.
   - [VLAN Security](lan_security/README.md#vlan-security-module): Manage VLANs and configure VLAN-based security policies to control traffic flow.
   - [DHCP Snooping](lan_security/README.md#dhcp-snooping-module): Enable and configure DHCP snooping to protect against rogue DHCP servers.
   - [Dynamic ARP Inspection](lan_security/README.md#dynamic-arp-inspection-module): Validate ARP packets to prevent ARP spoofing attacks.
   - [STP Security](lan_security/README.md#stp-security-module): Enhance Spanning Tree Protocol (STP) security to safeguard against STP-based attacks.
```

### Comparing `ciscopykit-2.1.2/ciscopykit/app.py` & `ciscopykit-2.1.3/ciscopykit/app.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/device.py` & `ciscopykit-2.1.3/ciscopykit/device.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/entry_point.py` & `ciscopykit-2.1.3/ciscopykit/entry_point.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/interface.py` & `ciscopykit-2.1.3/ciscopykit/interface.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/lan_security/app.py` & `ciscopykit-2.1.3/ciscopykit/lan_security/app.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/lan_security/dhcp_snooping.py` & `ciscopykit-2.1.3/ciscopykit/lan_security/dhcp_snooping.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/lan_security/dynamic_arp_inspection.py` & `ciscopykit-2.1.3/ciscopykit/lan_security/dynamic_arp_inspection.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/lan_security/stp_security.py` & `ciscopykit-2.1.3/ciscopykit/lan_security/stp_security.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/lan_security/switchport_security.py` & `ciscopykit-2.1.3/ciscopykit/lan_security/switchport_security.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/lan_security/vlan_security.py` & `ciscopykit-2.1.3/ciscopykit/lan_security/vlan_security.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/routing/static_routing.py` & `ciscopykit-2.1.3/ciscopykit/routing/static_routing.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/services/app.py` & `ciscopykit-2.1.3/ciscopykit/services/app.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/services/dhcp_service.py` & `ciscopykit-2.1.3/ciscopykit/services/dhcp_service.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/services/pat_service.py` & `ciscopykit-2.1.3/ciscopykit/services/pat_service.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/switch/app.py` & `ciscopykit-2.1.3/ciscopykit/switch/app.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/switch/l3_switch.py` & `ciscopykit-2.1.3/ciscopykit/switch/l3_switch.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/switch/switch.py` & `ciscopykit-2.1.3/ciscopykit/switch/switch.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/templates/generate_router_config.py` & `ciscopykit-2.1.3/ciscopykit/templates/generate_router_config.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/vlan/app.py` & `ciscopykit-2.1.3/ciscopykit/vlan/app.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit/vlan/vlan.py` & `ciscopykit-2.1.3/ciscopykit/vlan/vlan.py`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/ciscopykit.egg-info/PKG-INFO` & `ciscopykit-2.1.3/ciscopykit.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ciscopykit
-Version: 2.1.2
+Version: 2.1.3
 Summary: A network management toolkit for Cisco devices keeping track of devices when using GNS3 / Cisco Packet Tracer
 Home-page: https://github.com/Vincent-de-Torres-Portfolio/ciscopykit
 Author: devinci-it
 Author-email: vince.dev@icloud.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `ciscopykit-2.1.2/ciscopykit.egg-info/SOURCES.txt` & `ciscopykit-2.1.3/ciscopykit.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `ciscopykit-2.1.2/setup.py` & `ciscopykit-2.1.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='ciscopykit',
-    version='2.1.2',
+    version='2.1.3',
     author='devinci-it',
     author_email='vince.dev@icloud.com',
     description='A network management toolkit for Cisco devices keeping track of devices when using GNS3 / Cisco Packet Tracer',
     long_description='''A network management toolkit for Cisco devices. It provides classes and methods to manage network devices, interfaces, and configurations.''',
     url='https://github.com/Vincent-de-Torres-Portfolio/ciscopykit',
     packages=find_packages(),
     classifiers=[
```

