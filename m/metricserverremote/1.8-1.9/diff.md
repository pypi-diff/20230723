# Comparing `tmp/metricserverremote-1.8.tar.gz` & `tmp/metricserverremote-1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\metricserverremote-1.8.tar", last modified: Tue Aug 23 10:26:47 2022, max compression
+gzip compressed data, was "metricserverremote-1.9.tar", last modified: Sun Jul 23 11:46:46 2023, max compression
```

## Comparing `metricserverremote-1.8.tar` & `metricserverremote-1.9.tar`

### file list

```diff
@@ -1,64 +1,64 @@
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/
--rw-rw-rw-   0        0        0     1014 2018-12-28 13:35:24.000000 metricserverremote-1.8/LICENSE
--rw-rw-rw-   0        0        0       77 2018-12-28 14:47:06.000000 metricserverremote-1.8/MANIFEST.in
--rw-rw-rw-   0        0        0      469 2022-08-23 10:26:47.000000 metricserverremote-1.8/PKG-INFO
--rw-rw-rw-   0        0        0      919 2019-01-15 12:58:28.000000 metricserverremote-1.8/README.md
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote/
--rw-rw-rw-   0        0        0        0 2018-12-28 13:03:31.000000 metricserverremote-1.8/metricserverremote/__init__.py
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote/mswsdls/
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote/mswsdls/license/
--rw-rw-rw-   0        0        0      575 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/license/Arrays.xsd
--rw-rw-rw-   0        0        0     3796 2018-12-28 08:53:09.000000 metricserverremote-1.8/metricserverremote/mswsdls/license/service.wsdl
--rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/license/service.xsd
--rw-rw-rw-   0        0        0     5940 2018-12-28 09:38:46.000000 metricserverremote-1.8/metricserverremote/mswsdls/license/soap.malden.co.uk.wsdl
--rw-rw-rw-   0        0        0     3095 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/license/soap.malden.co.uk.xsd
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote/mswsdls/metrics/
--rw-rw-rw-   0        0        0      575 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/metrics/Arrays.xsd
--rw-rw-rw-   0        0        0     3871 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/metrics/Malden.MetricsServer.Service.Metric.Data.xsd
--rw-rw-rw-   0        0        0     4478 2019-05-10 07:22:10.000000 metricserverremote-1.8/metricserverremote/mswsdls/metrics/service.wsdl
--rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/metrics/service.xsd
--rw-rw-rw-   0        0        0     7721 2019-01-11 13:59:59.000000 metricserverremote-1.8/metricserverremote/mswsdls/metrics/soap.malden.co.uk.wsdl
--rw-rw-rw-   0        0        0     5426 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/metrics/soap.malden.co.uk.xsd
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/
--rw-rw-rw-   0        0        0     1814 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/Malden.MetricsServer.Service.Output.Data.xsd
--rw-rw-rw-   0        0        0     5856 2019-01-11 14:23:30.000000 metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/service.wsdl
--rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/service.xsd
--rw-rw-rw-   0        0        0    10569 2019-01-11 14:09:48.000000 metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/soap.malden.co.uk.wsdl
--rw-rw-rw-   0        0        0     6694 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/soap.malden.co.uk.xsd
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote/mswsdls/processing/
--rw-rw-rw-   0        0        0      830 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/processing/Arrays.xsd
--rw-rw-rw-   0        0        0     1235 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/processing/Malden.MetricsServer.Service.Process.Data.xsd
--rw-rw-rw-   0        0        0      351 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/processing/Message.xsd
--rw-rw-rw-   0        0        0     5301 2019-07-03 15:13:02.000000 metricserverremote-1.8/metricserverremote/mswsdls/processing/service.wsdl
--rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/processing/service.xsd
--rw-rw-rw-   0        0        0     8460 2019-07-03 14:54:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/processing/soap.malden.co.uk.wsdl
--rw-rw-rw-   0        0        0     4478 2019-07-03 14:57:10.000000 metricserverremote-1.8/metricserverremote/mswsdls/processing/soap.malden.co.uk.xsd
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote/mswsdls/result/
--rw-rw-rw-   0        0        0     1075 2018-11-21 17:09:40.000000 metricserverremote-1.8/metricserverremote/mswsdls/result/Malden.MetricsServer.Service.Process.Data.xsd
--rw-rw-rw-   0        0        0      351 2018-11-21 17:09:40.000000 metricserverremote-1.8/metricserverremote/mswsdls/result/Message.xsd
--rw-rw-rw-   0        0        0     3231 2019-11-25 13:19:38.000000 metricserverremote-1.8/metricserverremote/mswsdls/result/service.wsdl
--rw-rw-rw-   0        0        0     2491 2018-11-21 17:09:40.000000 metricserverremote-1.8/metricserverremote/mswsdls/result/service.xsd
--rw-rw-rw-   0        0        0     5243 2019-11-25 13:21:28.000000 metricserverremote-1.8/metricserverremote/mswsdls/result/soap.malden.co.uk.wsdl
--rw-rw-rw-   0        0        0     3323 2019-11-25 13:22:18.000000 metricserverremote-1.8/metricserverremote/mswsdls/result/soap.malden.co.uk.xsd
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote/mswsdls/tags/
--rw-rw-rw-   0        0        0      575 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/tags/Arrays.xsd
--rw-rw-rw-   0        0        0      930 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/tags/Malden.MetricsServer.Service.Tags.Data.xsd
--rw-rw-rw-   0        0        0     2362 2018-12-28 08:55:39.000000 metricserverremote-1.8/metricserverremote/mswsdls/tags/service.wsdl
--rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/tags/service.xsd
--rw-rw-rw-   0        0        0     3318 2018-12-28 09:40:07.000000 metricserverremote-1.8/metricserverremote/mswsdls/tags/soap.malden.co.uk.wsdl
--rw-rw-rw-   0        0        0     2139 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/tags/soap.malden.co.uk.xsd
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote/mswsdls/users/
--rw-rw-rw-   0        0        0      575 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/users/Arrays.xsd
--rw-rw-rw-   0        0        0     3570 2018-12-28 09:44:20.000000 metricserverremote-1.8/metricserverremote/mswsdls/users/service.wsdl
--rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/users/service.xsd
--rw-rw-rw-   0        0        0     5727 2018-12-28 09:37:02.000000 metricserverremote-1.8/metricserverremote/mswsdls/users/soap.malden.co.uk.wsdl
--rw-rw-rw-   0        0        0     3901 2018-07-12 13:11:42.000000 metricserverremote-1.8/metricserverremote/mswsdls/users/soap.malden.co.uk.xsd
--rw-rw-rw-   0        0        0    23290 2022-08-23 10:23:21.000000 metricserverremote-1.8/metricserverremote/server.py
-drwxrwxrwx   0        0        0        0 2022-08-23 10:26:47.000000 metricserverremote-1.8/metricserverremote.egg-info/
--rw-rw-rw-   0        0        0      469 2022-08-23 10:26:46.000000 metricserverremote-1.8/metricserverremote.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     2548 2022-08-23 10:26:46.000000 metricserverremote-1.8/metricserverremote.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-08-23 10:26:46.000000 metricserverremote-1.8/metricserverremote.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        5 2022-08-23 10:26:46.000000 metricserverremote-1.8/metricserverremote.egg-info/requires.txt
--rw-rw-rw-   0        0        0       19 2022-08-23 10:26:46.000000 metricserverremote-1.8/metricserverremote.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2022-08-23 10:26:47.000000 metricserverremote-1.8/setup.cfg
--rw-rw-rw-   0        0        0      633 2022-08-23 10:24:08.000000 metricserverremote-1.8/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.640945 metricserverremote-1.9/
+-rw-rw-rw-   0        0        0     1014 2018-12-28 13:35:24.000000 metricserverremote-1.9/LICENSE
+-rw-rw-rw-   0        0        0       77 2018-12-28 14:47:06.000000 metricserverremote-1.9/MANIFEST.in
+-rw-rw-rw-   0        0        0      451 2023-07-23 11:46:46.640945 metricserverremote-1.9/PKG-INFO
+-rw-rw-rw-   0        0        0      919 2019-01-15 12:58:28.000000 metricserverremote-1.9/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.588780 metricserverremote-1.9/metricserverremote/
+-rw-rw-rw-   0        0        0        0 2018-12-28 13:03:31.000000 metricserverremote-1.9/metricserverremote/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.582954 metricserverremote-1.9/metricserverremote/mswsdls/
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.599790 metricserverremote-1.9/metricserverremote/mswsdls/license/
+-rw-rw-rw-   0        0        0      575 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/license/Arrays.xsd
+-rw-rw-rw-   0        0        0     3796 2018-12-28 08:53:09.000000 metricserverremote-1.9/metricserverremote/mswsdls/license/service.wsdl
+-rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/license/service.xsd
+-rw-rw-rw-   0        0        0     5940 2018-12-28 09:38:46.000000 metricserverremote-1.9/metricserverremote/mswsdls/license/soap.malden.co.uk.wsdl
+-rw-rw-rw-   0        0        0     3095 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/license/soap.malden.co.uk.xsd
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.606819 metricserverremote-1.9/metricserverremote/mswsdls/metrics/
+-rw-rw-rw-   0        0        0      575 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/metrics/Arrays.xsd
+-rw-rw-rw-   0        0        0     3871 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/metrics/Malden.MetricsServer.Service.Metric.Data.xsd
+-rw-rw-rw-   0        0        0     4478 2019-05-10 07:22:10.000000 metricserverremote-1.9/metricserverremote/mswsdls/metrics/service.wsdl
+-rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/metrics/service.xsd
+-rw-rw-rw-   0        0        0     7721 2019-01-11 13:59:59.000000 metricserverremote-1.9/metricserverremote/mswsdls/metrics/soap.malden.co.uk.wsdl
+-rw-rw-rw-   0        0        0     5426 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/metrics/soap.malden.co.uk.xsd
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.611791 metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/
+-rw-rw-rw-   0        0        0     1814 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/Malden.MetricsServer.Service.Output.Data.xsd
+-rw-rw-rw-   0        0        0     5856 2019-01-11 14:23:30.000000 metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/service.wsdl
+-rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/service.xsd
+-rw-rw-rw-   0        0        0    10569 2019-01-11 14:09:48.000000 metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/soap.malden.co.uk.wsdl
+-rw-rw-rw-   0        0        0     6694 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/soap.malden.co.uk.xsd
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.619941 metricserverremote-1.9/metricserverremote/mswsdls/processing/
+-rw-rw-rw-   0        0        0      830 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/processing/Arrays.xsd
+-rw-rw-rw-   0        0        0     1235 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/processing/Malden.MetricsServer.Service.Process.Data.xsd
+-rw-rw-rw-   0        0        0      351 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/processing/Message.xsd
+-rw-rw-rw-   0        0        0     5301 2019-07-03 15:13:02.000000 metricserverremote-1.9/metricserverremote/mswsdls/processing/service.wsdl
+-rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/processing/service.xsd
+-rw-rw-rw-   0        0        0     8460 2019-07-03 14:54:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/processing/soap.malden.co.uk.wsdl
+-rw-rw-rw-   0        0        0     4478 2019-07-03 14:57:10.000000 metricserverremote-1.9/metricserverremote/mswsdls/processing/soap.malden.co.uk.xsd
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.627945 metricserverremote-1.9/metricserverremote/mswsdls/result/
+-rw-rw-rw-   0        0        0     1075 2018-11-21 17:09:40.000000 metricserverremote-1.9/metricserverremote/mswsdls/result/Malden.MetricsServer.Service.Process.Data.xsd
+-rw-rw-rw-   0        0        0      351 2018-11-21 17:09:40.000000 metricserverremote-1.9/metricserverremote/mswsdls/result/Message.xsd
+-rw-rw-rw-   0        0        0     3231 2019-11-25 13:19:38.000000 metricserverremote-1.9/metricserverremote/mswsdls/result/service.wsdl
+-rw-rw-rw-   0        0        0     2491 2018-11-21 17:09:40.000000 metricserverremote-1.9/metricserverremote/mswsdls/result/service.xsd
+-rw-rw-rw-   0        0        0     5243 2019-11-25 13:21:28.000000 metricserverremote-1.9/metricserverremote/mswsdls/result/soap.malden.co.uk.wsdl
+-rw-rw-rw-   0        0        0     3323 2019-11-25 13:22:18.000000 metricserverremote-1.9/metricserverremote/mswsdls/result/soap.malden.co.uk.xsd
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.633940 metricserverremote-1.9/metricserverremote/mswsdls/tags/
+-rw-rw-rw-   0        0        0      575 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/tags/Arrays.xsd
+-rw-rw-rw-   0        0        0      930 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/tags/Malden.MetricsServer.Service.Tags.Data.xsd
+-rw-rw-rw-   0        0        0     2362 2018-12-28 08:55:39.000000 metricserverremote-1.9/metricserverremote/mswsdls/tags/service.wsdl
+-rw-rw-rw-   0        0        0     2491 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/tags/service.xsd
+-rw-rw-rw-   0        0        0     3318 2018-12-28 09:40:07.000000 metricserverremote-1.9/metricserverremote/mswsdls/tags/soap.malden.co.uk.wsdl
+-rw-rw-rw-   0        0        0     2139 2018-07-12 13:11:42.000000 metricserverremote-1.9/metricserverremote/mswsdls/tags/soap.malden.co.uk.xsd
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.638940 metricserverremote-1.9/metricserverremote/mswsdls/users/
+-rw-rw-rw-   0        0        0      575 2023-07-21 10:04:18.000000 metricserverremote-1.9/metricserverremote/mswsdls/users/Arrays.xsd
+-rw-rw-rw-   0        0        0     3888 2023-07-21 12:11:47.000000 metricserverremote-1.9/metricserverremote/mswsdls/users/service.wsdl
+-rw-rw-rw-   0        0        0     2491 2023-07-21 10:04:18.000000 metricserverremote-1.9/metricserverremote/mswsdls/users/service.xsd
+-rw-rw-rw-   0        0        0     6331 2023-07-21 12:07:49.000000 metricserverremote-1.9/metricserverremote/mswsdls/users/soap.malden.co.uk.wsdl
+-rw-rw-rw-   0        0        0     4358 2023-07-21 10:04:18.000000 metricserverremote-1.9/metricserverremote/mswsdls/users/soap.malden.co.uk.xsd
+-rw-rw-rw-   0        0        0    23505 2023-07-21 11:46:16.000000 metricserverremote-1.9/metricserverremote/server.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:46.594796 metricserverremote-1.9/metricserverremote.egg-info/
+-rw-rw-rw-   0        0        0      451 2023-07-23 11:46:46.000000 metricserverremote-1.9/metricserverremote.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     2548 2023-07-23 11:46:46.000000 metricserverremote-1.9/metricserverremote.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:46:46.000000 metricserverremote-1.9/metricserverremote.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        5 2023-07-23 11:46:46.000000 metricserverremote-1.9/metricserverremote.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       19 2023-07-23 11:46:46.000000 metricserverremote-1.9/metricserverremote.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 11:46:46.641944 metricserverremote-1.9/setup.cfg
+-rw-rw-rw-   0        0        0      633 2023-07-23 11:38:01.000000 metricserverremote-1.9/setup.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `metricserverremote-1.8/LICENSE` & `metricserverremote-1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/README.md` & `metricserverremote-1.9/README.md`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/license/Arrays.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/license/Arrays.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/license/service.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/license/service.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/license/service.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/license/service.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/license/soap.malden.co.uk.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/license/soap.malden.co.uk.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/license/soap.malden.co.uk.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/license/soap.malden.co.uk.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/metrics/Arrays.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/metrics/Arrays.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/metrics/Malden.MetricsServer.Service.Metric.Data.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/metrics/Malden.MetricsServer.Service.Metric.Data.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/metrics/service.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/metrics/service.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/metrics/service.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/metrics/service.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/metrics/soap.malden.co.uk.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/metrics/soap.malden.co.uk.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/metrics/soap.malden.co.uk.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/metrics/soap.malden.co.uk.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/Malden.MetricsServer.Service.Output.Data.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/Malden.MetricsServer.Service.Output.Data.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/service.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/service.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/service.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/service.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/soap.malden.co.uk.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/soap.malden.co.uk.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/outputconfiguration/soap.malden.co.uk.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/outputconfiguration/soap.malden.co.uk.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/processing/Arrays.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/processing/Arrays.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/processing/Malden.MetricsServer.Service.Process.Data.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/processing/Malden.MetricsServer.Service.Process.Data.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/processing/service.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/processing/service.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/processing/service.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/processing/service.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/processing/soap.malden.co.uk.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/processing/soap.malden.co.uk.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/processing/soap.malden.co.uk.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/processing/soap.malden.co.uk.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/result/Malden.MetricsServer.Service.Process.Data.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/result/Malden.MetricsServer.Service.Process.Data.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/result/service.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/result/service.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/result/service.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/result/service.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/result/soap.malden.co.uk.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/result/soap.malden.co.uk.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/result/soap.malden.co.uk.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/result/soap.malden.co.uk.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/tags/Arrays.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/tags/Arrays.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/tags/Malden.MetricsServer.Service.Tags.Data.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/tags/Malden.MetricsServer.Service.Tags.Data.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/tags/service.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/tags/service.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/tags/service.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/tags/service.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/tags/soap.malden.co.uk.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/tags/soap.malden.co.uk.wsdl`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/tags/soap.malden.co.uk.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/tags/soap.malden.co.uk.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/users/Arrays.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/users/Arrays.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/users/service.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/users/service.wsdl`

 * *Files 2% similar despite different names*

#### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/users/service.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/users/service.wsdl`

```diff
@@ -1,9 +1,9 @@
 <?xml version="1.0" encoding="utf-8"?>
-<wsdl:definitions xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:wsa10="http://www.w3.org/2005/08/addressing" xmlns:tns="http://tempuri.org/" xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" xmlns:i0="http://soap.malden.co.uk" xmlns:wsam="http://www.w3.org/2007/05/addressing/metadata" xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/" name="UserServices" targetNamespace="http://tempuri.org/">
+<wsdl:definitions xmlns:wsam="http://www.w3.org/2007/05/addressing/metadata" xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:i0="http://soap.malden.co.uk" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://tempuri.org/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/" name="UserServices" targetNamespace="http://tempuri.org/">
   <wsdl:import namespace="http://soap.malden.co.uk" location="soap.malden.co.uk.wsdl"/>
   <wsdl:types/>
   <wsdl:binding name="user" type="i0:IUserService">
     <soap:binding transport="http://schemas.xmlsoap.org/soap/http"/>
     <wsdl:operation name="InitiateLogon">
       <soap:operation soapAction="http://soap.malden.co.uk/IUserService/InitiateLogon" style="document"/>
       <wsdl:input>
@@ -21,14 +21,23 @@
       <wsdl:input>
         <soap:body use="literal"/>
       </wsdl:input>
       <wsdl:output>
         <soap:body use="literal"/>
       </wsdl:output>
     </wsdl:operation>
+    <wsdl:operation name="Logoff">
+      <soap:operation soapAction="http://soap.malden.co.uk/IUserService/Logoff" style="document"/>
+      <wsdl:input>
+        <soap:body use="literal"/>
+      </wsdl:input>
+      <wsdl:output>
+        <soap:body use="literal"/>
+      </wsdl:output>
+    </wsdl:operation>
     <wsdl:operation name="LdapAuthenticate">
       <soap:operation soapAction="http://soap.malden.co.uk/IUserService/LdapAuthenticate" style="document"/>
       <wsdl:input>
         <soap:body use="literal"/>
       </wsdl:input>
       <wsdl:output>
         <soap:body use="literal"/>
```

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/users/service.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/users/service.xsd`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/users/soap.malden.co.uk.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/users/soap.malden.co.uk.wsdl`

 * *Files 6% similar despite different names*

#### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/users/soap.malden.co.uk.wsdl` & `metricserverremote-1.9/metricserverremote/mswsdls/users/soap.malden.co.uk.wsdl`

```diff
@@ -1,9 +1,9 @@
 <?xml version="1.0" encoding="utf-8"?>
-<wsdl:definitions xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:wsa10="http://www.w3.org/2005/08/addressing" xmlns:tns="http://soap.malden.co.uk" xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" xmlns:wsam="http://www.w3.org/2007/05/addressing/metadata" xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/" targetNamespace="http://soap.malden.co.uk">
+<wsdl:definitions xmlns:wsam="http://www.w3.org/2007/05/addressing/metadata" xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://soap.malden.co.uk" xmlns:wsa10="http://www.w3.org/2005/08/addressing" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/" targetNamespace="http://soap.malden.co.uk">
   <wsdl:types>
     <xsd:schema targetNamespace="http://soap.malden.co.uk/Imports">
       <xsd:import namespace="http://soap.malden.co.uk" schemaLocation="soap.malden.co.uk.xsd"/>
       <xsd:import namespace="http://schemas.microsoft.com/2003/10/Serialization/" schemaLocation="service.xsd"/>
       <xsd:import namespace="http://schemas.microsoft.com/2003/10/Serialization/Arrays" schemaLocation="Arrays.xsd"/>
     </xsd:schema>
   </wsdl:types>
@@ -18,14 +18,20 @@
   </wsdl:message>
   <wsdl:message name="IUserService_CompleteLogon_InputMessage">
     <wsdl:part name="parameters" element="tns:CompleteLogon"/>
   </wsdl:message>
   <wsdl:message name="IUserService_CompleteLogon_OutputMessage">
     <wsdl:part name="parameters" element="tns:CompleteLogonResponse"/>
   </wsdl:message>
+  <wsdl:message name="IUserService_Logoff_InputMessage">
+    <wsdl:part name="parameters" element="tns:Logoff"/>
+  </wsdl:message>
+  <wsdl:message name="IUserService_Logoff_OutputMessage">
+    <wsdl:part name="parameters" element="tns:LogoffResponse"/>
+  </wsdl:message>
   <wsdl:message name="IUserService_LdapAuthenticate_InputMessage">
     <wsdl:part name="parameters" element="tns:LdapAuthenticate"/>
   </wsdl:message>
   <wsdl:message name="IUserService_LdapAuthenticate_OutputMessage">
     <wsdl:part name="parameters" element="tns:LdapAuthenticateResponse"/>
   </wsdl:message>
   <wsdl:message name="IUserService_Setting_InputMessage">
@@ -52,14 +58,18 @@
       <wsdl:output wsaw:Action="http://soap.malden.co.uk/IUserService/InitiateLogonResponse" message="tns:IUserService_InitiateLogon_OutputMessage"/>
       <wsdl:fault wsaw:Action="http://soap.malden.co.uk/IUserService/InitiateLogonAccountUnknownFaultFault" name="AccountUnknownFaultFault" message="tns:IUserService_InitiateLogon_AccountUnknownFaultFault_FaultMessage"/>
     </wsdl:operation>
     <wsdl:operation name="CompleteLogon">
       <wsdl:input wsaw:Action="http://soap.malden.co.uk/IUserService/CompleteLogon" message="tns:IUserService_CompleteLogon_InputMessage"/>
       <wsdl:output wsaw:Action="http://soap.malden.co.uk/IUserService/CompleteLogonResponse" message="tns:IUserService_CompleteLogon_OutputMessage"/>
     </wsdl:operation>
+    <wsdl:operation name="Logoff">
+      <wsdl:input wsaw:Action="http://soap.malden.co.uk/IUserService/Logoff" message="tns:IUserService_Logoff_InputMessage"/>
+      <wsdl:output wsaw:Action="http://soap.malden.co.uk/IUserService/LogoffResponse" message="tns:IUserService_Logoff_OutputMessage"/>
+    </wsdl:operation>
     <wsdl:operation name="LdapAuthenticate">
       <wsdl:input wsaw:Action="http://soap.malden.co.uk/IUserService/LdapAuthenticate" message="tns:IUserService_LdapAuthenticate_InputMessage"/>
       <wsdl:output wsaw:Action="http://soap.malden.co.uk/IUserService/LdapAuthenticateResponse" message="tns:IUserService_LdapAuthenticate_OutputMessage"/>
     </wsdl:operation>
     <wsdl:operation name="Setting">
       <wsdl:input wsaw:Action="http://soap.malden.co.uk/IUserService/Setting" message="tns:IUserService_Setting_InputMessage"/>
       <wsdl:output wsaw:Action="http://soap.malden.co.uk/IUserService/SettingResponse" message="tns:IUserService_Setting_OutputMessage"/>
```

### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/users/soap.malden.co.uk.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/users/soap.malden.co.uk.xsd`

 * *Files 2% similar despite different names*

#### Comparing `metricserverremote-1.8/metricserverremote/mswsdls/users/soap.malden.co.uk.xsd` & `metricserverremote-1.9/metricserverremote/mswsdls/users/soap.malden.co.uk.xsd`

```diff
@@ -39,14 +39,28 @@
   <xs:element name="CompleteLogonResponse">
     <xs:complexType>
       <xs:sequence>
         <xs:element minOccurs="0" name="CompleteLogonResult" nillable="true" type="xs:string"/>
       </xs:sequence>
     </xs:complexType>
   </xs:element>
+  <xs:element name="Logoff">
+    <xs:complexType>
+      <xs:sequence>
+        <xs:element minOccurs="0" name="sessionId" nillable="true" type="xs:string"/>
+      </xs:sequence>
+    </xs:complexType>
+  </xs:element>
+  <xs:element name="LogoffResponse">
+    <xs:complexType>
+      <xs:sequence>
+        <xs:element minOccurs="0" name="LogoffResult" nillable="true" type="xs:string"/>
+      </xs:sequence>
+    </xs:complexType>
+  </xs:element>
   <xs:element name="LdapAuthenticate">
     <xs:complexType>
       <xs:sequence>
         <xs:element minOccurs="0" name="authToken" nillable="true" type="xs:base64Binary"/>
       </xs:sequence>
     </xs:complexType>
   </xs:element>
```

### Comparing `metricserverremote-1.8/metricserverremote/server.py` & `metricserverremote-1.9/metricserverremote/server.py`

 * *Files 1% similar despite different names*

```diff
@@ -26,14 +26,17 @@
 
     def md5hash(self, data):
         md5 = hashlib.md5()
         md5.update(data.encode('utf-8'))
         return md5.hexdigest()
 
     def logoff(self):
+        if self.sessionId is None:
+            return
+        self.userservice.Logoff(self.sessionId)
         self.sessionId = None
 
     def create_service(self, type, timeout):
         wsdlpath = '{}{}{}'.format(self.wsdldir, os.sep, '{}{}service.wsdl'.format(type,os.sep))
         if not os.path.exists(wsdlpath):
             return 'File {} needed by the python API not found'.format(wsdlpath)
         client = zeep.Client(wsdl=wsdlpath, transport=zeep.Transport(timeout=timeout))
@@ -47,26 +50,28 @@
         self.resultservice = self.create_service('result', timeout)
         self.processservice = self.create_service('processing', timeout)
         self.metricsservice = self.create_service('metrics', timeout)
         self.outputservice = self.create_service('outputconfiguration', timeout)
         self.userName = user
         self.password = password
         try:
-            salt = self.userservice.InitiateLogon(username=self.userName)
+            salt_id = self.userservice.InitiateLogon(username=self.userName)
+            items = salt_id.split(';')
             hashedpassword = self.md5hash(password)
-            ps = self.md5hash(hashedpassword + salt)
-            self.sessionId = self.userservice.CompleteLogon(username=self.userName, hash=ps, clientID=1)
+            ps = self.md5hash(hashedpassword + items[0])
+            self.sessionId = self.userservice.CompleteLogon(username=self.userName, hash=ps, clientID=items[1])
         except zeep.exceptions.Fault as fault:
             print('Login error : {}'.format(fault.message))
         except:
             print("Unexpected error:", sys.exc_info()[0])
             return 0
         if self.licenseservice.KeyInstalled():
             return 1
         else:
+            print("No MetricServer license installed")
             return 0
 
     def mask(self, output, tags):
         if len(tags) == 0:
             return 0
         header = zeep.xsd.ComplexType([
             zeep.xsd.Element('{http://soap.malden.co.uk}SessionId', zeep.xsd.String()),
```

### Comparing `metricserverremote-1.8/metricserverremote.egg-info/SOURCES.txt` & `metricserverremote-1.9/metricserverremote.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `metricserverremote-1.8/setup.py` & `metricserverremote-1.9/setup.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import setuptools
 
 setuptools.setup(
     name='metricserverremote',
-    version='1.8',
+    version='1.9',
     url='http://www.opalesystems.com',
     license='MIT',
     author='Adnane BERRADA',
     author_email='support@opalesystems.com',
     install_requires=[
         'zeep',
     ],
```

