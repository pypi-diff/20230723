# Comparing `tmp/pykeadhcp-0.6.0a1.tar.gz` & `tmp/pykeadhcp-0.7.0a2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pykeadhcp-0.6.0a1.tar", max compression
+gzip compressed data, was "pykeadhcp-0.7.0a2.tar", max compression
```

## Comparing `pykeadhcp-0.6.0a1.tar` & `pykeadhcp-0.7.0a2.tar`

### file list

```diff
@@ -1,67 +1,68 @@
--rw-r--r--   0        0        0    11356 2023-07-08 15:09:04.227639 pykeadhcp-0.6.0a1/LICENSE
--rw-r--r--   0        0        0     8001 2023-07-08 15:09:04.227639 pykeadhcp-0.6.0a1/README.md
--rw-r--r--   0        0        0       30 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/__init__.py
--rw-r--r--   0        0        0      174 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/daemons/__init__.py
--rw-r--r--   0        0        0     4508 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/daemons/ctrlagent.py
--rw-r--r--   0        0        0     4526 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/daemons/ddns.py
--rw-r--r--   0        0        0    70245 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/daemons/dhcp4.py
--rw-r--r--   0        0        0    69516 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/daemons/dhcp6.py
--rw-r--r--   0        0        0     4068 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/exceptions.py
--rw-r--r--   0        0        0    10415 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/kea.py
--rw-r--r--   0        0        0        0 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/__init__.py
--rw-r--r--   0        0        0        0 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/ctrlagent/__init__.py
--rw-r--r--   0        0        0      457 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/ctrlagent/config.py
--rw-r--r--   0        0        0        0 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp4/__init__.py
--rw-r--r--   0        0        0      331 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp4/client_class.py
--rw-r--r--   0        0        0      798 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp4/config.py
--rw-r--r--   0        0        0      212 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp4/lease.py
--rw-r--r--   0        0        0      303 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp4/reservation.py
--rw-r--r--   0        0        0      453 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp4/shared_network.py
--rw-r--r--   0        0        0      684 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp4/subnet.py
--rw-r--r--   0        0        0        0 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/__init__.py
--rw-r--r--   0        0        0      253 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/client_class.py
--rw-r--r--   0        0        0      922 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/config.py
--rw-r--r--   0        0        0      346 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/lease.py
--rw-r--r--   0        0        0      438 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/pd_pool.py
--rw-r--r--   0        0        0      212 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/reservation.py
--rw-r--r--   0        0        0      296 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/server_id.py
--rw-r--r--   0        0        0      380 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/shared_network.py
--rw-r--r--   0        0        0      501 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/subnet.py
--rw-r--r--   0        0        0     1638 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/enums.py
--rw-r--r--   0        0        0      169 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/__init__.py
--rw-r--r--   0        0        0      181 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/api_response.py
--rw-r--r--   0        0        0      477 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/authentication.py
--rw-r--r--   0        0        0      435 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/base.py
--rw-r--r--   0        0        0      415 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/client_class.py
--rw-r--r--   0        0        0     1394 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/config.py
--rw-r--r--   0        0        0      396 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/control_socket.py
--rw-r--r--   0        0        0     2458 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/daemon.py
--rw-r--r--   0        0        0      734 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/database.py
--rw-r--r--   0        0        0      399 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/dhcp_common.py
--rw-r--r--   0        0        0      873 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/dhcp_ddns.py
--rw-r--r--   0        0        0      158 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/dhcp_queue_control.py
--rw-r--r--   0        0        0      183 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/hook.py
--rw-r--r--   0        0        0      403 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/lease.py
--rw-r--r--   0        0        0      558 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/logger.py
--rw-r--r--   0        0        0      181 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/multi_threading.py
--rw-r--r--   0        0        0      259 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/option_data.py
--rw-r--r--   0        0        0      294 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/option_def.py
--rw-r--r--   0        0        0      306 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/pool.py
--rw-r--r--   0        0        0      141 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/relay.py
--rw-r--r--   0        0        0      302 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/remote_map.py
--rw-r--r--   0        0        0      217 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/remote_server.py
--rw-r--r--   0        0        0      436 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/reservation.py
--rw-r--r--   0        0        0      112 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/sanity_check.py
--rw-r--r--   0        0        0      175 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/shared_network.py
--rw-r--r--   0        0        0      249 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/sockets.py
--rw-r--r--   0        0        0      477 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/status.py
--rw-r--r--   0        0        0      390 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/models/generic/subnet.py
--rw-r--r--   0        0        0      152 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/parsers/__init__.py
--rw-r--r--   0        0        0      508 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/parsers/ctrlagent.py
--rw-r--r--   0        0        0        0 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/parsers/ddns.py
--rw-r--r--   0        0        0    17838 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/parsers/dhcp4.py
--rw-r--r--   0        0        0    20361 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/parsers/dhcp6.py
--rw-r--r--   0        0        0     3436 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/parsers/exceptions.py
--rw-r--r--   0        0        0      825 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pykeadhcp/parsers/generic.py
--rw-r--r--   0        0        0      449 2023-07-08 15:09:04.231640 pykeadhcp-0.6.0a1/pyproject.toml
--rw-r--r--   0        0        0     8608 1970-01-01 00:00:00.000000 pykeadhcp-0.6.0a1/PKG-INFO
+-rw-r--r--   0        0        0    11356 2023-07-23 15:42:50.250528 pykeadhcp-0.7.0a2/LICENSE
+-rw-r--r--   0        0        0     8001 2023-07-23 15:42:50.250528 pykeadhcp-0.7.0a2/README.md
+-rw-r--r--   0        0        0       30 2023-07-23 15:42:50.250528 pykeadhcp-0.7.0a2/pykeadhcp/__init__.py
+-rw-r--r--   0        0        0      174 2023-07-23 15:42:50.250528 pykeadhcp-0.7.0a2/pykeadhcp/daemons/__init__.py
+-rw-r--r--   0        0        0     4508 2023-07-23 15:42:50.250528 pykeadhcp-0.7.0a2/pykeadhcp/daemons/ctrlagent.py
+-rw-r--r--   0        0        0     4526 2023-07-23 15:42:50.250528 pykeadhcp-0.7.0a2/pykeadhcp/daemons/ddns.py
+-rw-r--r--   0        0        0    78658 2023-07-23 15:42:50.250528 pykeadhcp-0.7.0a2/pykeadhcp/daemons/dhcp4.py
+-rw-r--r--   0        0        0    78637 2023-07-23 15:42:50.250528 pykeadhcp-0.7.0a2/pykeadhcp/daemons/dhcp6.py
+-rw-r--r--   0        0        0     4068 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/exceptions.py
+-rw-r--r--   0        0        0    10415 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/kea.py
+-rw-r--r--   0        0        0        0 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/ctrlagent/__init__.py
+-rw-r--r--   0        0        0      457 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/ctrlagent/config.py
+-rw-r--r--   0        0        0        0 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp4/__init__.py
+-rw-r--r--   0        0        0      331 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp4/client_class.py
+-rw-r--r--   0        0        0      798 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp4/config.py
+-rw-r--r--   0        0        0      212 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp4/lease.py
+-rw-r--r--   0        0        0      303 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp4/reservation.py
+-rw-r--r--   0        0        0      453 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp4/shared_network.py
+-rw-r--r--   0        0        0      684 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp4/subnet.py
+-rw-r--r--   0        0        0        0 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/__init__.py
+-rw-r--r--   0        0        0      253 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/client_class.py
+-rw-r--r--   0        0        0      954 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/config.py
+-rw-r--r--   0        0        0      346 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/lease.py
+-rw-r--r--   0        0        0      438 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/pd_pool.py
+-rw-r--r--   0        0        0      212 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/reservation.py
+-rw-r--r--   0        0        0      296 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/server_id.py
+-rw-r--r--   0        0        0      380 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/shared_network.py
+-rw-r--r--   0        0        0      501 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/subnet.py
+-rw-r--r--   0        0        0     2345 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/enums.py
+-rw-r--r--   0        0        0      169 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/__init__.py
+-rw-r--r--   0        0        0      181 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/api_response.py
+-rw-r--r--   0        0        0      477 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/authentication.py
+-rw-r--r--   0        0        0      435 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/base.py
+-rw-r--r--   0        0        0      415 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/client_class.py
+-rw-r--r--   0        0        0     1394 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/config.py
+-rw-r--r--   0        0        0      396 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/control_socket.py
+-rw-r--r--   0        0        0     2487 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/daemon.py
+-rw-r--r--   0        0        0      734 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/database.py
+-rw-r--r--   0        0        0      399 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/dhcp_common.py
+-rw-r--r--   0        0        0      873 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/dhcp_ddns.py
+-rw-r--r--   0        0        0      158 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/dhcp_queue_control.py
+-rw-r--r--   0        0        0      636 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/high_availability.py
+-rw-r--r--   0        0        0      183 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/hook.py
+-rw-r--r--   0        0        0      403 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/lease.py
+-rw-r--r--   0        0        0      558 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/logger.py
+-rw-r--r--   0        0        0      181 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/multi_threading.py
+-rw-r--r--   0        0        0      259 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/option_data.py
+-rw-r--r--   0        0        0      294 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/option_def.py
+-rw-r--r--   0        0        0      306 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/pool.py
+-rw-r--r--   0        0        0      141 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/relay.py
+-rw-r--r--   0        0        0      302 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/remote_map.py
+-rw-r--r--   0        0        0      217 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/remote_server.py
+-rw-r--r--   0        0        0      436 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/reservation.py
+-rw-r--r--   0        0        0      180 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/sanity_check.py
+-rw-r--r--   0        0        0      175 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/shared_network.py
+-rw-r--r--   0        0        0      249 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/sockets.py
+-rw-r--r--   0        0        0      420 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/status.py
+-rw-r--r--   0        0        0      390 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/models/generic/subnet.py
+-rw-r--r--   0        0        0      152 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/parsers/__init__.py
+-rw-r--r--   0        0        0      508 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/parsers/ctrlagent.py
+-rw-r--r--   0        0        0        0 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/parsers/ddns.py
+-rw-r--r--   0        0        0    17838 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/parsers/dhcp4.py
+-rw-r--r--   0        0        0    20361 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/parsers/dhcp6.py
+-rw-r--r--   0        0        0     3436 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/parsers/exceptions.py
+-rw-r--r--   0        0        0      825 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pykeadhcp/parsers/generic.py
+-rw-r--r--   0        0        0      547 2023-07-23 15:42:50.254528 pykeadhcp-0.7.0a2/pyproject.toml
+-rw-r--r--   0        0        0     8608 1970-01-01 00:00:00.000000 pykeadhcp-0.7.0a2/PKG-INFO
```

### Comparing `pykeadhcp-0.6.0a1/LICENSE` & `pykeadhcp-0.7.0a2/LICENSE`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/README.md` & `pykeadhcp-0.7.0a2/README.md`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/daemons/ctrlagent.py` & `pykeadhcp-0.7.0a2/pykeadhcp/daemons/ctrlagent.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/daemons/ddns.py` & `pykeadhcp-0.7.0a2/pykeadhcp/daemons/ddns.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/daemons/dhcp4.py` & `pykeadhcp-0.7.0a2/pykeadhcp/daemons/dhcp4.py`

 * *Files 4% similar despite different names*

```diff
@@ -62,14 +62,165 @@
         """Returns list of compilation options that this particular binary was built with
 
         Kea API Reference:
             https://kea.readthedocs.io/en/kea-2.2.0/api.html#ref-build-report
         """
         return self.api.send_command(command="build-report", service=self.service)
 
+    def cache_clear(self) -> KeaResponse:
+        """Removes all cached host reservations
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-clear
+        """
+        return self.api.send_command(
+            command="cache-clear", service=self.service, required_hook="host_cache"
+        )
+
+    def cache_flush(self, number: int) -> KeaResponse:
+        """Removes certain number of entries in the host cache
+
+        Args:
+            number:     Number of host caches to clear
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-flush
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-flush",
+            service=self.service,
+            arguments=number,  # Inconsistent API....
+            required_hook="host_cache",
+        )
+
+    def cache_get(self) -> List[Reservation4]:
+        """Gets full content of the host cache
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-get
+        """
+        data = self.api.send_command(
+            command="cache-get", service=self.service, required_hook="host_cache"
+        )
+
+        if data.result == 3:
+            return []
+
+        return [Reservation4.parse_obj(reservation) for reservation in data.arguments]
+
+    def cache_get_by_id(
+        self, identifier_type: HostReservationIdentifierEnum, identifier: str
+    ) -> List[Reservation4]:
+        """Returns entries matching the given identifier from the host cache
+
+        Args:
+            identifier_type:        Type of Identifier
+            identifier:             Identifier data
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-get-by-id
+        """
+        try:
+            HostReservationIdentifierEnum(identifier_type)
+        except ValueError:
+            raise KeaUnknownHostReservationTypeException(identifier_type)
+
+        data = self.api.send_command_with_arguments(
+            command="cache-get-by-id",
+            service=self.service,
+            arguments={identifier_type: identifier},
+            required_hook="host_cache",
+        )
+
+        if data.result == 3:
+            return []
+
+        return [Reservation4.parse_obj(reservation) for reservation in data.arguments]
+
+    def cache_insert(self, subnet_id: int, reservation: Reservation4) -> KeaResponse:
+        """Manually insert a host into the cache
+
+        Args:
+            reservation:    Reservation4 Object
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-insert
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-insert",
+            service=self.service,
+            arguments={
+                "subnet-id4": subnet_id,
+                "subnet-id6": 0,
+                **reservation.dict(
+                    exclude_none=True, exclude_unset=True, by_alias=True
+                ),
+            },
+            required_hook="host_cache",
+        )
+
+    def cache_load(self, filepath: str) -> KeaResponse:
+        """Instructs Kea to load from a previously dumped cache into its existing host cache
+
+        Args:
+            filepath:   File Path to load
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-load
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-load",
+            service=self.service,
+            arguments=filepath,  # Inconsistent API....
+            required_hook="host_cache",
+        )
+
+    def cache_remove(self, subnet_id: int, ip_address: str) -> KeaResponse:
+        """Remove an entry from the host cache
+
+        Args:
+            subnet_id:      Subnet ID
+            ip_address:     IP Address
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-remove
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-remove",
+            service=self.service,
+            arguments={"ip-address": ip_address, "subnet-id": subnet_id},
+            required_hook="host_cache",
+        )
+
+    def cache_size(self) -> KeaResponse:
+        """Returns the number of entries in the host cache
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-size
+        """
+        return self.api.send_command(
+            command="cache-size", service=self.service, required_hook="host_cache"
+        )
+
+    def cache_write(self, filepath: str) -> KeaResponse:
+        """Instructs Kea to write host cache content to disk
+
+        Args:
+            filepath:   File Path to save
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-write
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-write",
+            service=self.service,
+            arguments=filepath,  # Inconsistent API....
+            required_hook="host_cache",
+        )
+
     def class_add(self, client_class: ClientClass4) -> KeaResponse:
         """Adds a new class to the existing server configuration
 
         Args:
             client_class:       ClientClass4 Object
 
         Kea API Reference:
@@ -254,39 +405,124 @@
             https://kea.readthedocs.io/en/kea-2.2.0/arm/ctrl-channel.html#the-dhcp-enable-command
         """
         return self.api.send_command_with_arguments(
             command="dhcp-enable", service=self.service, arguments={"origin": "user"}
         )
 
     def ha_continue(self) -> KeaResponse:
-        raise NotImplementedError
+        """Resumes operation of a paused HA state machine.
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-continue
+        """
+        return self.api.send_command(
+            command="ha-continue", service=self.service, required_hook="ha"
+        )
 
     def ha_heartbeat(self) -> KeaResponse:
-        raise NotImplementedError
+        """Manually verify the HA state of local and remote servers.
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-heartbeat
+        """
+        return self.api.send_command(
+            command="ha-heartbeat",
+            service=self.service,
+            required_hook="ha",
+        )
+
+    def ha_maintenance_cancel(self) -> KeaResponse:
+        """Cancel maintenance via API
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-maintenance-cancel
+        """
+        return self.api.send_command(
+            command="ha-maintenance-cancel", service=self.service, required_hook="ha"
+        )
 
-    def ha_maintenance_canel(self) -> KeaResponse:
-        raise NotImplementedError
+    def ha_maintenance_notify(self, cancel: bool) -> KeaResponse:
+        """Typically used by servers and not an administrator, however this informs the partner HA
+        servers to transition to the in-maintenance state or revert from it
+
+        Args:
+            cancel:     Indicates server should transition to the in-maintenance state if False
 
-    def ha_maintenance_notify(self) -> KeaResponse:
-        raise NotImplementedError
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-maintenance-notify
+        """
+        return self.api.send_command_with_arguments(
+            command="ha-maintenance-notify",
+            service=self.service,
+            arguments={"cancel": cancel},
+            required_hook="ha",
+        )
 
     def ha_maintenance_start(self) -> KeaResponse:
-        raise NotImplementedError
+        """Instruct the server to transition to the 'partner-in-maintenance' state
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-maintenance-start
+        """
+        return self.api.send_command(
+            command="ha-maintenance-start", service=self.service, required_hook="ha"
+        )
 
     def ha_reset(self) -> KeaResponse:
-        raise NotImplementedError
+        """Resets the HA state machine by forcing its state to 'waiting' state
 
-    def ha_scopes(self) -> KeaResponse:
-        raise NotImplementedError
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-reset
+        """
+        return self.api.send_command(
+            command="ha-reset", service=self.service, required_hook="ha"
+        )
+
+    def ha_scopes(self, ha_servers: List[str]) -> KeaResponse:
+        """Modifies the scope that the server is responsible for serving
 
-    def ha_sync(self) -> KeaResponse:
-        raise NotImplementedError
+        Args:
+            ha_servers:     List of servers (defined in the configuration file)
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-scopes
+        """
+        return self.api.send_command_with_arguments(
+            command="ha-scopes",
+            service=self.service,
+            arguments={"scopes": ha_servers},
+            required_hook="ha",
+        )
+
+    def ha_sync(self, partner_server: str, max_period: int) -> KeaResponse:
+        """Instructs the server to sync its local lease database with a selected partner server
+
+        Args:
+            partner_server:     Name of the partner server to sync with
+            max_period:         Max Period
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-sync
+        """
+        return self.api.send_command_with_arguments(
+            command="ha-sync",
+            service=self.service,
+            arguments={"server-name": partner_server, "max-period": max_period},
+            required_hook="ha",
+        )
 
     def ha_sync_complete_notify(self) -> KeaResponse:
-        raise NotImplementedError
+        """Typically used by the servers directly and not called via the API by an admin
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-sync-complete-notify
+        """
+        return self.api.send_command(
+            command="ha-sync-complete-notify", service=self.service, required_hook="ha"
+        )
 
     def lease4_add(
         self,
         *,
         ip_address: str,
         **kwargs,
     ) -> KeaResponse:
@@ -1613,15 +1849,15 @@
 
         Kea API Reference:
             https://kea.readthedocs.io/en/kea-2.2.0/api.html#reservation-del
         """
         try:
             HostReservationIdentifierEnum(identifier_type)
         except ValueError:
-            raise KeaUnknownHostReservationTypeException
+            raise KeaUnknownHostReservationTypeException(identifier_type)
 
         return self.api.send_command_with_arguments(
             command="reservation-del",
             service=self.service,
             arguments={
                 "subnet-id": subnet_id,
                 "identifier-type": identifier_type,
```

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/daemons/dhcp6.py` & `pykeadhcp-0.7.0a2/pykeadhcp/daemons/dhcp6.py`

 * *Files 4% similar despite different names*

```diff
@@ -63,14 +63,165 @@
         """Returns list of compilation options that this particular binary was built with
 
         Kea API Reference:
             https://kea.readthedocs.io/en/kea-2.2.0/api.html#ref-build-report
         """
         return self.api.send_command(command="build-report", service=self.service)
 
+    def cache_clear(self) -> KeaResponse:
+        """Removes all cached host reservations
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-clear
+        """
+        return self.api.send_command(
+            command="cache-clear", service=self.service, required_hook="host_cache"
+        )
+
+    def cache_flush(self, number: int) -> KeaResponse:
+        """Removes certain number of entries in the host cache
+
+        Args:
+            number:     Number of host caches to clear
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-flush
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-flush",
+            service=self.service,
+            arguments=number,  # Inconsistent API....
+            required_hook="host_cache",
+        )
+
+    def cache_get(self) -> List[Reservation6]:
+        """Gets full content of the host cache
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-get
+        """
+        data = self.api.send_command(
+            command="cache-get", service=self.service, required_hook="host_cache"
+        )
+
+        if data.result == 3:
+            return []
+
+        return [Reservation6.parse_obj(reservation) for reservation in data.arguments]
+
+    def cache_get_by_id(
+        self, identifier_type: HostReservationIdentifierEnum, identifier: str
+    ) -> List[Reservation6]:
+        """Returns entries matching the given identifier from the host cache
+
+        Args:
+            identifier_type:        Type of Identifier
+            identifier:             Identifier data
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-get-by-id
+        """
+        try:
+            HostReservationIdentifierEnum(identifier_type)
+        except ValueError:
+            raise KeaUnknownHostReservationTypeException(identifier_type)
+
+        data = self.api.send_command_with_arguments(
+            command="cache-get-by-id",
+            service=self.service,
+            arguments={identifier_type: identifier},
+            required_hook="host_cache",
+        )
+
+        if data.result == 3:
+            return []
+
+        return [Reservation6.parse_obj(reservation) for reservation in data.arguments]
+
+    def cache_insert(self, subnet_id: int, reservation: Reservation6) -> KeaResponse:
+        """Manually insert a host into the cache
+
+        Args:
+            reservation:    Reservation6 Object
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-insert
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-insert",
+            service=self.service,
+            arguments={
+                "subnet-id4": 0,
+                "subnet-id6": subnet_id,
+                **reservation.dict(
+                    exclude_none=True, exclude_unset=True, by_alias=True
+                ),
+            },
+            required_hook="host_cache",
+        )
+
+    def cache_load(self, filepath: str) -> KeaResponse:
+        """Instructs Kea to load from a previously dumped cache into its existing host cache
+
+        Args:
+            filepath:   File Path to load
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-load
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-load",
+            service=self.service,
+            arguments=filepath,  # Inconsistent API....
+            required_hook="host_cache",
+        )
+
+    def cache_remove(self, subnet_id: int, ip_address: str) -> KeaResponse:
+        """Remove an entry from the host cache
+
+        Args:
+            subnet_id:      Subnet ID
+            ip_address:     IP Address
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-remove
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-remove",
+            service=self.service,
+            arguments={"ip-address": ip_address, "subnet-id": subnet_id},
+            required_hook="host_cache",
+        )
+
+    def cache_size(self) -> KeaResponse:
+        """Returns the number of entries in the host cache
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-size
+        """
+        return self.api.send_command(
+            command="cache-size", service=self.service, required_hook="host_cache"
+        )
+
+    def cache_write(self, filepath: str) -> KeaResponse:
+        """Instructs Kea to write host cache content to disk
+
+        Args:
+            filepath:   File Path to save
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/kea-2.2.0/api.html#cache-write
+        """
+        return self.api.send_command_with_arguments(
+            command="cache-write",
+            service=self.service,
+            arguments=filepath,  # Inconsistent API....
+            required_hook="host_cache",
+        )
+
     def class_add(self, client_class: ClientClass6) -> KeaResponse:
         """Adds a new class to the existing server configuration
 
         Args:
             client_class:       ClientClass6 Object
 
         Kea API Reference:
@@ -254,14 +405,126 @@
         Kea API Reference:
             https://kea.readthedocs.io/en/kea-2.2.0/arm/ctrl-channel.html#the-dhcp-enable-command
         """
         return self.api.send_command_with_arguments(
             command="dhcp-enable", service=self.service, arguments={"origin": "user"}
         )
 
+    def ha_continue(self) -> KeaResponse:
+        """Resumes operation of a paused HA state machine.
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-continue
+        """
+        return self.api.send_command(
+            command="ha-continue", service=self.service, required_hook="ha"
+        )
+
+    def ha_heartbeat(self) -> KeaResponse:
+        """Manually verify the HA state of local and remote servers.
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-heartbeat
+        """
+        return self.api.send_command(
+            command="ha-heartbeat",
+            service=self.service,
+            required_hook="ha",
+        )
+
+    def ha_maintenance_cancel(self) -> KeaResponse:
+        """Cancel maintenance via API
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-maintenance-cancel
+        """
+        return self.api.send_command(
+            command="ha-maintenance-cancel", service=self.service, required_hook="ha"
+        )
+
+    def ha_maintenance_notify(self, cancel: bool) -> KeaResponse:
+        """Typically used by servers and not an administrator, however this informs the partner HA
+        servers to transition to the in-maintenance state or revert from it
+
+        Args:
+            cancel:     Indicates server should transition to the in-maintenance state if False
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-maintenance-notify
+        """
+        return self.api.send_command_with_arguments(
+            command="ha-maintenance-notify",
+            service=self.service,
+            arguments={"cancel": cancel},
+            required_hook="ha",
+        )
+
+    def ha_maintenance_start(self) -> KeaResponse:
+        """Instruct the server to transition to the 'partner-in-maintenance' state
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-maintenance-start
+        """
+        return self.api.send_command(
+            command="ha-maintenance-start", service=self.service, required_hook="ha"
+        )
+
+    def ha_reset(self) -> KeaResponse:
+        """Resets the HA state machine by forcing its state to 'waiting' state
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-reset
+        """
+        return self.api.send_command(
+            command="ha-reset", service=self.service, required_hook="ha"
+        )
+
+    def ha_scopes(self, ha_servers: List[str]) -> KeaResponse:
+        """Modifies the scope that the server is responsible for serving
+
+        Args:
+            ha_servers:     List of servers (defined in the configuration file)
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-scopes
+        """
+        return self.api.send_command_with_arguments(
+            command="ha-scopes",
+            service=self.service,
+            arguments={"scopes": ha_servers},
+            required_hook="ha",
+        )
+
+    def ha_sync(self, partner_server: str, max_period: int) -> KeaResponse:
+        """Instructs the server to sync its local lease database with a selected partner server
+
+        Args:
+            partner_server:     Name of the partner server to sync with
+            max_period:         Max Period
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-sync
+        """
+        return self.api.send_command_with_arguments(
+            command="ha-sync",
+            service=self.service,
+            arguments={"server-name": partner_server, "max-period": max_period},
+            required_hook="ha",
+        )
+
+    def ha_sync_complete_notify(self) -> KeaResponse:
+        """Typically used by the servers directly and not called via the API by an admin
+
+        Kea API Reference:
+            https://kea.readthedocs.io/en/latest/api.html#ha-sync-complete-notify
+        """
+        return self.api.send_command(
+            command="ha-sync-complete-notify", service=self.service, required_hook="ha"
+        )
+
     def lease6_add(
         self, *, ip_address: str, duid: str, iaid: int, **kwargs
     ) -> KeaResponse:
         """Administratively add a new IPv6 lease
 
         Args:
             ip_address:         IPv6 Address of lease
```

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/exceptions.py` & `pykeadhcp-0.7.0a2/pykeadhcp/exceptions.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/kea.py` & `pykeadhcp-0.7.0a2/pykeadhcp/kea.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp4/config.py` & `pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp4/config.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp4/subnet.py` & `pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp4/subnet.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/models/dhcp6/config.py` & `pykeadhcp-0.7.0a2/pykeadhcp/models/dhcp6/config.py`

 * *Files 12% similar despite different names*

```diff
@@ -15,7 +15,8 @@
     preferred_lifetime: Optional[int]
     min_preferred_lifetime: Optional[int]
     max_preferred_lifetime: Optional[int]
     subnet6: Optional[List[Subnet6]] = []
     mac_sources: Optional[List[str]] = []
     relay_supplied_options: Optional[List[str]] = []
     server_id: ServerId
+    pd_allocator: Optional[str]
```

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/models/enums.py` & `pykeadhcp-0.7.0a2/pykeadhcp/models/enums.py`

 * *Files 23% similar despite different names*

```diff
@@ -82,7 +82,35 @@
 class AuthenticationTypeEnum(str, Enum):
     basic = "basic"
 
 
 class RemoteMapTypeEnum(str, Enum):
     mysql = "mysql"
     postgresql = "postgresql"
+
+
+class HAModeTypeEnum(str, Enum):
+    load_balancing = "load-balancing"
+    hot_standby = "hot-standby"
+
+
+class HARoleTypeEnum(str, Enum):
+    primary = "primary"
+    secondary = "secondary"
+    standby = "standby"
+
+
+class HAStateTypeEnum(str, Enum):
+    backup = "backup"
+    communication_recovery = "communication-recovery"
+    hot_standby = "hot-standby"
+    load_balancing = "load-balancing"
+    in_maintenance = "in-maintenance"
+    partner_down = "partner-down"
+    partner_in_maintenance = "partner-in-maintenance"
+    passive_backup = "passive-backup"
+    ready = "ready"
+    synbcing = "syncing"
+    terminated = "terminated"
+    waiting = "waiting"
+    unavailable = "unavailable"
+    null = ""
```

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/models/generic/config.py` & `pykeadhcp-0.7.0a2/pykeadhcp/models/generic/config.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/models/generic/daemon.py` & `pykeadhcp-0.7.0a2/pykeadhcp/models/generic/daemon.py`

 * *Files 2% similar despite different names*

```diff
@@ -54,7 +54,8 @@
     multi_threading: Optional[MultiThreading]
     early_global_reservations_lookup: Optional[bool]
     ip_reservations_unique: Optional[bool]
     reservations_lookup_first: Optional[bool]
     compatibility: Optional[dict]
     parked_packet_limit: Optional[int]
     decline_probation_period: Optional[int]
+    allocator: Optional[str]
```

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/models/generic/database.py` & `pykeadhcp-0.7.0a2/pykeadhcp/models/generic/database.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/models/generic/dhcp_ddns.py` & `pykeadhcp-0.7.0a2/pykeadhcp/models/generic/dhcp_ddns.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/models/generic/logger.py` & `pykeadhcp-0.7.0a2/pykeadhcp/models/generic/logger.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/parsers/dhcp4.py` & `pykeadhcp-0.7.0a2/pykeadhcp/parsers/dhcp4.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/parsers/dhcp6.py` & `pykeadhcp-0.7.0a2/pykeadhcp/parsers/dhcp6.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/parsers/exceptions.py` & `pykeadhcp-0.7.0a2/pykeadhcp/parsers/exceptions.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/pykeadhcp/parsers/generic.py` & `pykeadhcp-0.7.0a2/pykeadhcp/parsers/generic.py`

 * *Files identical despite different names*

### Comparing `pykeadhcp-0.6.0a1/PKG-INFO` & `pykeadhcp-0.7.0a2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pykeadhcp
-Version: 0.6.0a1
+Version: 0.7.0a2
 Summary: Wrapper around requests module to query ISC Kea DHCP API Daemons (ctrlagent, dhcp4, dhcp6, ddns)
 License: Apache 2.0
 Author: Brandon Spendlove
 Author-email: brandon-spendlove@hotmail.co.uk
 Requires-Python: >=3.10,<4.0
 Classifier: License :: Other/Proprietary License
 Classifier: Programming Language :: Python :: 3
```

