# Comparing `tmp/foliolib-0.3.9a1.tar.gz` & `tmp/foliolib-0.3.9a2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "foliolib-0.3.9a1.tar", last modified: Sat Jul 15 07:29:52 2023, max compression
+gzip compressed data, was "foliolib-0.3.9a2.tar", last modified: Sat Jul 15 08:03:26 2023, max compression
```

## Comparing `foliolib-0.3.9a1.tar` & `foliolib-0.3.9a2.tar`

### file list

```diff
@@ -1,136 +1,153 @@
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.410090 foliolib-0.3.9a1/
--rw-r--r--   0 tobi      (1000) tobi      (1000)    35146 2020-10-11 07:41:52.000000 foliolib-0.3.9a1/COPYING
--rw-r--r--   0 tobi      (1000) tobi      (1000)       43 2020-11-07 12:13:21.000000 foliolib-0.3.9a1/MANIFEST.in
--rw-r--r--   0 tobi      (1000) tobi      (1000)     2753 2023-07-15 07:29:52.410090 foliolib-0.3.9a1/PKG-INFO
--rw-r--r--   0 tobi      (1000) tobi      (1000)     2013 2023-07-14 07:29:20.000000 foliolib-0.3.9a1/README.rst
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.402090 foliolib-0.3.9a1/foliolib/
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1031 2023-03-24 13:25:47.000000 foliolib-0.3.9a1/foliolib/__init__.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      396 2023-07-15 07:29:49.000000 foliolib-0.3.9a1/foliolib/__version__.py
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.402090 foliolib-0.3.9a1/foliolib/apiBuilder/
--rw-r--r--   0 tobi      (1000) tobi      (1000)      351 2022-10-11 12:37:16.000000 foliolib-0.3.9a1/foliolib/apiBuilder/__init__.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1288 2022-03-13 04:11:25.000000 foliolib-0.3.9a1/foliolib/apiBuilder/build_api.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1586 2022-05-04 20:18:39.000000 foliolib-0.3.9a1/foliolib/apiBuilder/cli.py
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.402090 foliolib-0.3.9a1/foliolib/cli/
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3820 2023-06-16 04:28:16.000000 foliolib-0.3.9a1/foliolib/cli/__init__.py
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.402090 foliolib-0.3.9a1/foliolib/cli/folio/
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1541 2023-07-11 10:00:13.000000 foliolib-0.3.9a1/foliolib/cli/folio/__init__.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3433 2023-07-12 05:56:16.000000 foliolib-0.3.9a1/foliolib/cli/folio/inventory.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      634 2022-02-21 04:57:32.000000 foliolib-0.3.9a1/foliolib/cli/main.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      374 2022-02-21 04:57:41.000000 foliolib-0.3.9a1/foliolib/cli/main_err.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      895 2022-02-21 04:57:36.000000 foliolib-0.3.9a1/foliolib/cli/main_noauth.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     4591 2023-04-15 04:58:38.000000 foliolib-0.3.9a1/foliolib/cli/module.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3495 2023-04-01 07:43:09.000000 foliolib-0.3.9a1/foliolib/cli/okapi.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      446 2022-02-21 04:57:17.000000 foliolib-0.3.9a1/foliolib/cli/orderedGroup.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3892 2023-07-14 03:48:00.000000 foliolib-0.3.9a1/foliolib/cli/platform.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     2759 2023-04-21 05:25:46.000000 foliolib-0.3.9a1/foliolib/cli/server.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    12868 2022-10-06 05:29:03.000000 foliolib-0.3.9a1/foliolib/cli/tenant.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    13254 2023-07-15 06:44:14.000000 foliolib-0.3.9a1/foliolib/config.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      801 2022-05-09 17:52:49.000000 foliolib-0.3.9a1/foliolib/exceptions.py
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.402090 foliolib-0.3.9a1/foliolib/folio/
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1870 2022-10-06 05:35:01.000000 foliolib-0.3.9a1/foliolib/folio/__init__.py
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.410090 foliolib-0.3.9a1/foliolib/folio/api/
--rw-r--r--   0 tobi      (1000) tobi      (1000)        0 2021-11-15 08:23:39.000000 foliolib-0.3.9a1/foliolib/folio/api/__init__.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     9675 2023-07-10 17:25:41.000000 foliolib-0.3.9a1/foliolib/folio/api/audit.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     2643 2023-07-10 17:25:41.000000 foliolib-0.3.9a1/foliolib/folio/api/authtoken.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     7100 2023-07-10 17:25:41.000000 foliolib-0.3.9a1/foliolib/folio/api/bulkOperations.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     8152 2023-07-10 17:25:41.000000 foliolib-0.3.9a1/foliolib/folio/api/calendar.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    40915 2023-07-10 17:25:41.000000 foliolib-0.3.9a1/foliolib/folio/api/circulation.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    73691 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/circulationStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     6506 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/configuration.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    16302 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/consortia.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     4913 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/copycat.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    54009 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/courses.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    19883 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/dataExport.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     6349 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/dataExportSpring.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    10066 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/dataExportWorker.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    13485 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/dataImport.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    37645 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/dataImportConverterStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    41060 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/diConverterStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     2213 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/ebsconet.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     7884 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/email.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     5628 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/entitiesLinks.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    25152 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/ermUsage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     5745 2023-07-10 17:25:42.000000 foliolib-0.3.9a1/foliolib/folio/api/ermUsageHarvester.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     8498 2023-07-10 17:25:43.000000 foliolib-0.3.9a1/foliolib/folio/api/eusageReports.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     4273 2023-07-10 17:25:43.000000 foliolib-0.3.9a1/foliolib/folio/api/eventConfig.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    80620 2023-07-10 17:25:43.000000 foliolib-0.3.9a1/foliolib/folio/api/feesfines.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    76479 2023-07-10 17:25:43.000000 foliolib-0.3.9a1/foliolib/folio/api/finance.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    79172 2023-07-10 17:25:43.000000 foliolib-0.3.9a1/foliolib/folio/api/financeStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    51717 2023-07-10 17:25:44.000000 foliolib-0.3.9a1/foliolib/folio/api/fincConfig.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     6999 2023-07-10 17:25:41.000000 foliolib-0.3.9a1/foliolib/folio/api/folioCustomFields.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1342 2023-07-10 17:25:41.000000 foliolib-0.3.9a1/foliolib/folio/api/folioSpringBase.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1787 2023-07-10 17:25:41.000000 foliolib-0.3.9a1/foliolib/folio/api/folioVertxLib.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     8283 2023-07-10 17:25:44.000000 foliolib-0.3.9a1/foliolib/folio/api/gobi.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     7801 2023-07-10 17:25:44.000000 foliolib-0.3.9a1/foliolib/folio/api/idmConnect.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    74110 2023-07-10 17:26:02.000000 foliolib-0.3.9a1/foliolib/folio/api/innReach.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    22929 2023-07-10 17:26:02.000000 foliolib-0.3.9a1/foliolib/folio/api/inventory.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)   220610 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/inventoryStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     6001 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/inventoryUpdate.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    45051 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/invoice.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    47143 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/invoiceStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    54294 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/kbEbscoJava.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3051 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/ldp.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1332 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/licenses.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     8538 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/login.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     4260 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/loginSaml.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    17932 2023-07-10 17:26:03.000000 foliolib-0.3.9a1/foliolib/folio/api/marccat.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    20533 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/metaStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     8754 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/notes.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     8870 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/notify.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    12602 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/oaiPmh.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    63105 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/orders.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    78262 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/ordersStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     4978 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/organizations.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    45825 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/organizationsStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3632 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/passwordValidator.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     5893 2023-07-10 17:26:04.000000 foliolib-0.3.9a1/foliolib/folio/api/patron.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    15601 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/patronBlocks.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    14392 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/permissions.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     9093 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/pubsub.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     4777 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/quickMarc.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    17165 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/remoteStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    21731 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/reservoir.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1928 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/rtac.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    18371 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/search.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      732 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/sender.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     5419 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/settings.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    11215 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/sharedIndex.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    23625 2023-07-10 17:26:05.000000 foliolib-0.3.9a1/foliolib/folio/api/sourceRecordManager.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    29289 2023-07-10 17:26:06.000000 foliolib-0.3.9a1/foliolib/folio/api/sourceRecordStorage.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3187 2023-07-10 17:26:06.000000 foliolib-0.3.9a1/foliolib/folio/api/tags.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     4091 2023-07-10 17:26:06.000000 foliolib-0.3.9a1/foliolib/folio/api/templateEngine.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      870 2023-07-10 17:26:06.000000 foliolib-0.3.9a1/foliolib/folio/api/userImport.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    24695 2023-07-10 17:26:06.000000 foliolib-0.3.9a1/foliolib/folio/api/users.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    11127 2023-07-10 17:26:06.000000 foliolib-0.3.9a1/foliolib/folio/api/usersBl.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     5803 2022-05-31 09:32:11.000000 foliolib-0.3.9a1/foliolib/folio/config.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     8495 2021-02-25 09:49:29.000000 foliolib-0.3.9a1/foliolib/folio/dataImport.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      436 2022-03-17 02:39:17.000000 foliolib-0.3.9a1/foliolib/folio/exceptions.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      945 2022-04-08 08:56:47.000000 foliolib-0.3.9a1/foliolib/folio/inventory.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    24355 2023-05-09 16:17:52.000000 foliolib-0.3.9a1/foliolib/folio/inventoryReferenceData.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     9397 2023-05-20 07:12:08.000000 foliolib-0.3.9a1/foliolib/folio/users.py
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.410090 foliolib-0.3.9a1/foliolib/helper/
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1436 2023-07-13 08:08:57.000000 foliolib-0.3.9a1/foliolib/helper/__init__.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     9225 2023-07-14 07:35:11.000000 foliolib-0.3.9a1/foliolib/helper/database.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3572 2023-07-14 08:44:58.000000 foliolib-0.3.9a1/foliolib/helper/folio.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     5212 2023-07-14 06:23:10.000000 foliolib-0.3.9a1/foliolib/helper/modules.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3827 2023-07-13 16:48:50.000000 foliolib-0.3.9a1/foliolib/helper/okapi.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     9347 2023-07-14 06:23:10.000000 foliolib-0.3.9a1/foliolib/helper/platform.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1918 2023-07-14 06:27:21.000000 foliolib-0.3.9a1/foliolib/helper/tenant.py
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.410090 foliolib-0.3.9a1/foliolib/okapi/
--rw-r--r--   0 tobi      (1000) tobi      (1000)    14520 2022-10-13 08:48:51.000000 foliolib-0.3.9a1/foliolib/okapi/__init__.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)     2399 2022-07-24 04:45:10.000000 foliolib-0.3.9a1/foliolib/okapi/exceptions.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    16413 2023-07-15 06:48:17.000000 foliolib-0.3.9a1/foliolib/okapi/kubeClient.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)      542 2022-03-22 15:04:58.000000 foliolib-0.3.9a1/foliolib/okapi/misc.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    39244 2023-07-14 06:23:10.000000 foliolib-0.3.9a1/foliolib/okapi/okapiClient.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    10030 2023-07-13 16:49:11.000000 foliolib-0.3.9a1/foliolib/okapi/okapiModule.py
--rw-r--r--   0 tobi      (1000) tobi      (1000)    18331 2023-07-15 07:26:25.000000 foliolib-0.3.9a1/foliolib/okapi/okapiModuleKubernetes.py
-drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 07:29:52.402090 foliolib-0.3.9a1/foliolib.egg-info/
--rw-r--r--   0 tobi      (1000) tobi      (1000)     2753 2023-07-15 07:29:52.000000 foliolib-0.3.9a1/foliolib.egg-info/PKG-INFO
--rw-r--r--   0 tobi      (1000) tobi      (1000)     3790 2023-07-15 07:29:52.000000 foliolib-0.3.9a1/foliolib.egg-info/SOURCES.txt
--rw-r--r--   0 tobi      (1000) tobi      (1000)        1 2023-07-15 07:29:52.000000 foliolib-0.3.9a1/foliolib.egg-info/dependency_links.txt
--rw-r--r--   0 tobi      (1000) tobi      (1000)       46 2023-07-15 07:29:52.000000 foliolib-0.3.9a1/foliolib.egg-info/entry_points.txt
--rw-r--r--   0 tobi      (1000) tobi      (1000)      130 2023-07-15 07:29:52.000000 foliolib-0.3.9a1/foliolib.egg-info/requires.txt
--rw-r--r--   0 tobi      (1000) tobi      (1000)      126 2023-07-15 07:29:52.000000 foliolib-0.3.9a1/foliolib.egg-info/top_level.txt
--rw-r--r--   0 tobi      (1000) tobi      (1000)      305 2023-02-21 08:41:56.000000 foliolib-0.3.9a1/requirements.txt
--rw-r--r--   0 tobi      (1000) tobi      (1000)     1182 2023-07-15 07:29:52.410090 foliolib-0.3.9a1/setup.cfg
--rw-r--r--   0 tobi      (1000) tobi      (1000)      117 2023-05-29 06:44:32.000000 foliolib-0.3.9a1/setup.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.514171 foliolib-0.3.9a2/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    35146 2020-10-11 07:41:52.000000 foliolib-0.3.9a2/COPYING
+-rw-r--r--   0 tobi      (1000) tobi      (1000)       43 2020-11-07 12:13:21.000000 foliolib-0.3.9a2/MANIFEST.in
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     2753 2023-07-15 08:03:26.514171 foliolib-0.3.9a2/PKG-INFO
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     2013 2023-07-14 07:29:20.000000 foliolib-0.3.9a2/README.rst
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.502171 foliolib-0.3.9a2/foliolib/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1031 2023-03-24 13:25:47.000000 foliolib-0.3.9a2/foliolib/__init__.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      396 2023-07-15 08:03:24.000000 foliolib-0.3.9a2/foliolib/__version__.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.502171 foliolib-0.3.9a2/foliolib/apiBuilder/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      351 2022-10-11 12:37:16.000000 foliolib-0.3.9a2/foliolib/apiBuilder/__init__.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1288 2022-03-13 04:11:25.000000 foliolib-0.3.9a2/foliolib/apiBuilder/build_api.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1586 2022-05-04 20:18:39.000000 foliolib-0.3.9a2/foliolib/apiBuilder/cli.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.502171 foliolib-0.3.9a2/foliolib/apiBuilder/oas/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1336 2023-05-17 08:34:02.000000 foliolib-0.3.9a2/foliolib/apiBuilder/oas/__init__.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     2724 2023-05-17 07:58:59.000000 foliolib-0.3.9a2/foliolib/apiBuilder/oas/baseoas.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1299 2022-10-11 12:36:09.000000 foliolib-0.3.9a2/foliolib/apiBuilder/oas/helper.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     4575 2023-05-16 13:07:57.000000 foliolib-0.3.9a2/foliolib/apiBuilder/oas/oaSchema.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    15324 2023-05-17 07:19:21.000000 foliolib-0.3.9a2/foliolib/apiBuilder/oas/oaSchemaMethod.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1623 2023-05-11 09:59:26.000000 foliolib-0.3.9a2/foliolib/apiBuilder/oas/oaSchemaPath.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      260 2022-05-05 06:38:40.000000 foliolib-0.3.9a2/foliolib/apiBuilder/oas/operationIds.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.502171 foliolib-0.3.9a2/foliolib/apiBuilder/raml/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     2985 2022-04-08 09:41:36.000000 foliolib-0.3.9a2/foliolib/apiBuilder/raml/__init__.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    10711 2022-04-13 08:26:00.000000 foliolib-0.3.9a2/foliolib/apiBuilder/raml/codeBuilder.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      543 2022-03-17 02:28:58.000000 foliolib-0.3.9a2/foliolib/apiBuilder/raml/exceptions.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1642 2022-04-08 10:40:47.000000 foliolib-0.3.9a2/foliolib/apiBuilder/raml/helper.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      176 2022-10-11 12:36:55.000000 foliolib-0.3.9a2/foliolib/apiBuilder/raml/names.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     9330 2023-02-10 08:52:51.000000 foliolib-0.3.9a2/foliolib/apiBuilder/raml/ramlMethod.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     5632 2021-11-17 13:32:20.000000 foliolib-0.3.9a2/foliolib/apiBuilder/raml/ramlUrl.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     9934 2023-02-10 08:52:10.000000 foliolib-0.3.9a2/foliolib/apiBuilder/raml/tpl.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.506171 foliolib-0.3.9a2/foliolib/cli/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     3820 2023-06-16 04:28:16.000000 foliolib-0.3.9a2/foliolib/cli/__init__.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.506171 foliolib-0.3.9a2/foliolib/cli/folio/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1541 2023-07-11 10:00:13.000000 foliolib-0.3.9a2/foliolib/cli/folio/__init__.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     3433 2023-07-12 05:56:16.000000 foliolib-0.3.9a2/foliolib/cli/folio/inventory.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      634 2022-02-21 04:57:32.000000 foliolib-0.3.9a2/foliolib/cli/main.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      374 2022-02-21 04:57:41.000000 foliolib-0.3.9a2/foliolib/cli/main_err.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      895 2022-02-21 04:57:36.000000 foliolib-0.3.9a2/foliolib/cli/main_noauth.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     4591 2023-04-15 04:58:38.000000 foliolib-0.3.9a2/foliolib/cli/module.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     3495 2023-04-01 07:43:09.000000 foliolib-0.3.9a2/foliolib/cli/okapi.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      446 2022-02-21 04:57:17.000000 foliolib-0.3.9a2/foliolib/cli/orderedGroup.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     3892 2023-07-14 03:48:00.000000 foliolib-0.3.9a2/foliolib/cli/platform.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     2759 2023-04-21 05:25:46.000000 foliolib-0.3.9a2/foliolib/cli/server.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    12868 2022-10-06 05:29:03.000000 foliolib-0.3.9a2/foliolib/cli/tenant.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    13264 2023-07-15 07:59:37.000000 foliolib-0.3.9a2/foliolib/config.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      801 2022-05-09 17:52:49.000000 foliolib-0.3.9a2/foliolib/exceptions.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.506171 foliolib-0.3.9a2/foliolib/folio/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1870 2022-10-06 05:35:01.000000 foliolib-0.3.9a2/foliolib/folio/__init__.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.514171 foliolib-0.3.9a2/foliolib/folio/api/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)        0 2021-11-15 08:23:39.000000 foliolib-0.3.9a2/foliolib/folio/api/__init__.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     9675 2023-07-10 17:25:41.000000 foliolib-0.3.9a2/foliolib/folio/api/audit.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     2643 2023-07-10 17:25:41.000000 foliolib-0.3.9a2/foliolib/folio/api/authtoken.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     7100 2023-07-10 17:25:41.000000 foliolib-0.3.9a2/foliolib/folio/api/bulkOperations.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     8152 2023-07-10 17:25:41.000000 foliolib-0.3.9a2/foliolib/folio/api/calendar.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    40915 2023-07-10 17:25:41.000000 foliolib-0.3.9a2/foliolib/folio/api/circulation.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    73691 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/circulationStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     6506 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/configuration.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    16302 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/consortia.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     4913 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/copycat.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    54009 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/courses.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    19883 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/dataExport.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     6349 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/dataExportSpring.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    10066 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/dataExportWorker.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    13485 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/dataImport.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    37645 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/dataImportConverterStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    41060 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/diConverterStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     2213 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/ebsconet.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     7884 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/email.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     5628 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/entitiesLinks.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    25152 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/ermUsage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     5745 2023-07-10 17:25:42.000000 foliolib-0.3.9a2/foliolib/folio/api/ermUsageHarvester.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     8498 2023-07-10 17:25:43.000000 foliolib-0.3.9a2/foliolib/folio/api/eusageReports.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     4273 2023-07-10 17:25:43.000000 foliolib-0.3.9a2/foliolib/folio/api/eventConfig.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    80620 2023-07-10 17:25:43.000000 foliolib-0.3.9a2/foliolib/folio/api/feesfines.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    76479 2023-07-10 17:25:43.000000 foliolib-0.3.9a2/foliolib/folio/api/finance.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    79172 2023-07-10 17:25:43.000000 foliolib-0.3.9a2/foliolib/folio/api/financeStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    51717 2023-07-10 17:25:44.000000 foliolib-0.3.9a2/foliolib/folio/api/fincConfig.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     6999 2023-07-10 17:25:41.000000 foliolib-0.3.9a2/foliolib/folio/api/folioCustomFields.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1342 2023-07-10 17:25:41.000000 foliolib-0.3.9a2/foliolib/folio/api/folioSpringBase.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1787 2023-07-10 17:25:41.000000 foliolib-0.3.9a2/foliolib/folio/api/folioVertxLib.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     8283 2023-07-10 17:25:44.000000 foliolib-0.3.9a2/foliolib/folio/api/gobi.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     7801 2023-07-10 17:25:44.000000 foliolib-0.3.9a2/foliolib/folio/api/idmConnect.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    74110 2023-07-10 17:26:02.000000 foliolib-0.3.9a2/foliolib/folio/api/innReach.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    22929 2023-07-10 17:26:02.000000 foliolib-0.3.9a2/foliolib/folio/api/inventory.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)   220610 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/inventoryStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     6001 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/inventoryUpdate.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    45051 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/invoice.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    47143 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/invoiceStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    54294 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/kbEbscoJava.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     3051 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/ldp.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1332 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/licenses.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     8538 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/login.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     4260 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/loginSaml.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    17932 2023-07-10 17:26:03.000000 foliolib-0.3.9a2/foliolib/folio/api/marccat.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    20533 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/metaStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     8754 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/notes.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     8870 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/notify.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    12602 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/oaiPmh.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    63105 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/orders.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    78262 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/ordersStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     4978 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/organizations.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    45825 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/organizationsStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     3632 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/passwordValidator.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     5893 2023-07-10 17:26:04.000000 foliolib-0.3.9a2/foliolib/folio/api/patron.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    15601 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/patronBlocks.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    14392 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/permissions.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     9093 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/pubsub.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     4777 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/quickMarc.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    17165 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/remoteStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    21731 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/reservoir.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1928 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/rtac.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    18371 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/search.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      732 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/sender.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     5419 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/settings.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    11215 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/sharedIndex.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    23625 2023-07-10 17:26:05.000000 foliolib-0.3.9a2/foliolib/folio/api/sourceRecordManager.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    29289 2023-07-10 17:26:06.000000 foliolib-0.3.9a2/foliolib/folio/api/sourceRecordStorage.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     3187 2023-07-10 17:26:06.000000 foliolib-0.3.9a2/foliolib/folio/api/tags.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     4091 2023-07-10 17:26:06.000000 foliolib-0.3.9a2/foliolib/folio/api/templateEngine.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      870 2023-07-10 17:26:06.000000 foliolib-0.3.9a2/foliolib/folio/api/userImport.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    24695 2023-07-10 17:26:06.000000 foliolib-0.3.9a2/foliolib/folio/api/users.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    11127 2023-07-10 17:26:06.000000 foliolib-0.3.9a2/foliolib/folio/api/usersBl.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     5803 2022-05-31 09:32:11.000000 foliolib-0.3.9a2/foliolib/folio/config.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     8495 2021-02-25 09:49:29.000000 foliolib-0.3.9a2/foliolib/folio/dataImport.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      436 2022-03-17 02:39:17.000000 foliolib-0.3.9a2/foliolib/folio/exceptions.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      945 2022-04-08 08:56:47.000000 foliolib-0.3.9a2/foliolib/folio/inventory.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    24355 2023-05-09 16:17:52.000000 foliolib-0.3.9a2/foliolib/folio/inventoryReferenceData.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     9397 2023-05-20 07:12:08.000000 foliolib-0.3.9a2/foliolib/folio/users.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.514171 foliolib-0.3.9a2/foliolib/helper/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1436 2023-07-13 08:08:57.000000 foliolib-0.3.9a2/foliolib/helper/__init__.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     9225 2023-07-14 07:35:11.000000 foliolib-0.3.9a2/foliolib/helper/database.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     3572 2023-07-14 08:44:58.000000 foliolib-0.3.9a2/foliolib/helper/folio.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     5212 2023-07-14 06:23:10.000000 foliolib-0.3.9a2/foliolib/helper/modules.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     3827 2023-07-13 16:48:50.000000 foliolib-0.3.9a2/foliolib/helper/okapi.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     9347 2023-07-14 06:23:10.000000 foliolib-0.3.9a2/foliolib/helper/platform.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1918 2023-07-14 06:27:21.000000 foliolib-0.3.9a2/foliolib/helper/tenant.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.514171 foliolib-0.3.9a2/foliolib/okapi/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    14520 2022-10-13 08:48:51.000000 foliolib-0.3.9a2/foliolib/okapi/__init__.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     2399 2022-07-24 04:45:10.000000 foliolib-0.3.9a2/foliolib/okapi/exceptions.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    16413 2023-07-15 06:48:17.000000 foliolib-0.3.9a2/foliolib/okapi/kubeClient.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      542 2022-03-22 15:04:58.000000 foliolib-0.3.9a2/foliolib/okapi/misc.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    39244 2023-07-14 06:23:10.000000 foliolib-0.3.9a2/foliolib/okapi/okapiClient.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    10030 2023-07-13 16:49:11.000000 foliolib-0.3.9a2/foliolib/okapi/okapiModule.py
+-rw-r--r--   0 tobi      (1000) tobi      (1000)    18331 2023-07-15 07:26:25.000000 foliolib-0.3.9a2/foliolib/okapi/okapiModuleKubernetes.py
+drwxr-xr-x   0 tobi      (1000) tobi      (1000)        0 2023-07-15 08:03:26.502171 foliolib-0.3.9a2/foliolib.egg-info/
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     2753 2023-07-15 08:03:26.000000 foliolib-0.3.9a2/foliolib.egg-info/PKG-INFO
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     4345 2023-07-15 08:03:26.000000 foliolib-0.3.9a2/foliolib.egg-info/SOURCES.txt
+-rw-r--r--   0 tobi      (1000) tobi      (1000)        1 2023-07-15 08:03:26.000000 foliolib-0.3.9a2/foliolib.egg-info/dependency_links.txt
+-rw-r--r--   0 tobi      (1000) tobi      (1000)       46 2023-07-15 08:03:26.000000 foliolib-0.3.9a2/foliolib.egg-info/entry_points.txt
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      130 2023-07-15 08:03:26.000000 foliolib-0.3.9a2/foliolib.egg-info/requires.txt
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      175 2023-07-15 08:03:26.000000 foliolib-0.3.9a2/foliolib.egg-info/top_level.txt
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      305 2023-02-21 08:41:56.000000 foliolib-0.3.9a2/requirements.txt
+-rw-r--r--   0 tobi      (1000) tobi      (1000)     1233 2023-07-15 08:03:26.514171 foliolib-0.3.9a2/setup.cfg
+-rw-r--r--   0 tobi      (1000) tobi      (1000)      117 2023-05-29 06:44:32.000000 foliolib-0.3.9a2/setup.py
```

### Comparing `foliolib-0.3.9a1/COPYING` & `foliolib-0.3.9a2/COPYING`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/PKG-INFO` & `foliolib-0.3.9a2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: foliolib
-Version: 0.3.9a1
+Version: 0.3.9a2
 Summary: Okapi/Folio Manager and Library
 Home-page: https://github.com/tobi-weber/foliolib
 Author: Tobias Weber
 Author-email: tobi-weber@gmx.de
 License: GPL-3.0 License
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `foliolib-0.3.9a1/README.rst` & `foliolib-0.3.9a2/README.rst`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/__init__.py` & `foliolib-0.3.9a2/foliolib/__init__.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/apiBuilder/build_api.py` & `foliolib-0.3.9a2/foliolib/apiBuilder/build_api.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/apiBuilder/cli.py` & `foliolib-0.3.9a2/foliolib/apiBuilder/cli.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/__init__.py` & `foliolib-0.3.9a2/foliolib/cli/__init__.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/folio/__init__.py` & `foliolib-0.3.9a2/foliolib/cli/folio/__init__.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/folio/inventory.py` & `foliolib-0.3.9a2/foliolib/cli/folio/inventory.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/main.py` & `foliolib-0.3.9a2/foliolib/cli/main.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/main_noauth.py` & `foliolib-0.3.9a2/foliolib/cli/main_noauth.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/module.py` & `foliolib-0.3.9a2/foliolib/cli/module.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/okapi.py` & `foliolib-0.3.9a2/foliolib/cli/okapi.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/platform.py` & `foliolib-0.3.9a2/foliolib/cli/platform.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/server.py` & `foliolib-0.3.9a2/foliolib/cli/server.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/cli/tenant.py` & `foliolib-0.3.9a2/foliolib/cli/tenant.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/config.py` & `foliolib-0.3.9a2/foliolib/config.py`

 * *Files 1% similar despite different names*

```diff
@@ -303,16 +303,16 @@
             self.__foliolibcfg["Cache"] = {}
             self.__foliolibcfg["Cache"]["descriptors"] = os.path.join(self.get_confdir(),
                                                                       "cache",
                                                                       "descriptors")
             self.__foliolibcfg["Cache"]["platforms"] = os.path.join(self.get_confdir(),
                                                                     "cache",
                                                                     "platforms")
-            self.__foliolibcfg["GitHub"] = {}
-            self.__foliolibcfg["GitHub"]["access-token"] = ""
+            # self.__foliolibcfg["GitHub"] = {}
+            # self.__foliolibcfg["GitHub"]["access-token"] = ""
             with open(fpath, "w") as f:
                 self.__foliolibcfg.write(f)
         else:
             log.debug("%s already exists.", fpath)
 
     def create_server_conf(self, name: str, okapi_host: str = "localhost",
                            okapi_port: str = "9130", ssl=False):
@@ -338,17 +338,17 @@
             self.__servercfg["Okapi"]["foliolibenv"] = str(True)
             self.__servercfg["Cli"] = {}
             self.__servercfg["Cli"]["confirm"] = str(True)
             self.__servercfg["Cli"]["loglevel"] = "INFO"
             self.__servercfg["Env"] = {}
             self.__servercfg["Env"]["db_host"] = okapi_host
             self.__servercfg["Env"]["db_port"] = "default"
-            self.__servercfg["Env"]["db_username"] = "okapi"
-            self.__servercfg["Env"]["db_password"] = "okapi25"
-            self.__servercfg["Env"]["db_database"] = "okapi"
+            self.__servercfg["Env"]["db_username"] = "folio"
+            self.__servercfg["Env"]["db_password"] = "folio"
+            self.__servercfg["Env"]["db_database"] = "okapi_modules"
             self.__servercfg["Env"]["db_querytimeout"] = "120000"
             self.__servercfg["Env"]["db_charset"] = "UTF-8"
             self.__servercfg["Env"]["kafka_host"] = okapi_host
             self.__servercfg["Env"]["kafka_port"] = "9092"
             self.__servercfg["Env"]["okapi_url"] = f"http://{okapi_host}:{okapi_port}"
             self.__servercfg["Env"]["replication_factor"] = "1"
             with open(fpath, "w") as f:
```

### Comparing `foliolib-0.3.9a1/foliolib/exceptions.py` & `foliolib-0.3.9a2/foliolib/exceptions.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/__init__.py` & `foliolib-0.3.9a2/foliolib/folio/__init__.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/audit.py` & `foliolib-0.3.9a2/foliolib/folio/api/audit.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/authtoken.py` & `foliolib-0.3.9a2/foliolib/folio/api/authtoken.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/bulkOperations.py` & `foliolib-0.3.9a2/foliolib/folio/api/bulkOperations.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/calendar.py` & `foliolib-0.3.9a2/foliolib/folio/api/calendar.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/circulation.py` & `foliolib-0.3.9a2/foliolib/folio/api/circulation.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/circulationStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/circulationStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/configuration.py` & `foliolib-0.3.9a2/foliolib/folio/api/configuration.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/consortia.py` & `foliolib-0.3.9a2/foliolib/folio/api/consortia.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/copycat.py` & `foliolib-0.3.9a2/foliolib/folio/api/copycat.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/courses.py` & `foliolib-0.3.9a2/foliolib/folio/api/courses.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/dataExport.py` & `foliolib-0.3.9a2/foliolib/folio/api/dataExport.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/dataExportSpring.py` & `foliolib-0.3.9a2/foliolib/folio/api/dataExportSpring.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/dataExportWorker.py` & `foliolib-0.3.9a2/foliolib/folio/api/dataExportWorker.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/dataImport.py` & `foliolib-0.3.9a2/foliolib/folio/api/dataImport.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/dataImportConverterStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/dataImportConverterStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/diConverterStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/diConverterStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/ebsconet.py` & `foliolib-0.3.9a2/foliolib/folio/api/ebsconet.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/email.py` & `foliolib-0.3.9a2/foliolib/folio/api/email.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/entitiesLinks.py` & `foliolib-0.3.9a2/foliolib/folio/api/entitiesLinks.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/ermUsage.py` & `foliolib-0.3.9a2/foliolib/folio/api/ermUsage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/ermUsageHarvester.py` & `foliolib-0.3.9a2/foliolib/folio/api/ermUsageHarvester.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/eusageReports.py` & `foliolib-0.3.9a2/foliolib/folio/api/eusageReports.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/eventConfig.py` & `foliolib-0.3.9a2/foliolib/folio/api/eventConfig.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/feesfines.py` & `foliolib-0.3.9a2/foliolib/folio/api/feesfines.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/finance.py` & `foliolib-0.3.9a2/foliolib/folio/api/finance.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/financeStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/financeStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/fincConfig.py` & `foliolib-0.3.9a2/foliolib/folio/api/fincConfig.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/folioCustomFields.py` & `foliolib-0.3.9a2/foliolib/folio/api/folioCustomFields.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/folioSpringBase.py` & `foliolib-0.3.9a2/foliolib/folio/api/folioSpringBase.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/folioVertxLib.py` & `foliolib-0.3.9a2/foliolib/folio/api/folioVertxLib.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/gobi.py` & `foliolib-0.3.9a2/foliolib/folio/api/gobi.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/idmConnect.py` & `foliolib-0.3.9a2/foliolib/folio/api/idmConnect.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/innReach.py` & `foliolib-0.3.9a2/foliolib/folio/api/innReach.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/inventory.py` & `foliolib-0.3.9a2/foliolib/folio/api/inventory.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/inventoryStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/inventoryStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/inventoryUpdate.py` & `foliolib-0.3.9a2/foliolib/folio/api/inventoryUpdate.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/invoice.py` & `foliolib-0.3.9a2/foliolib/folio/api/invoice.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/invoiceStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/invoiceStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/kbEbscoJava.py` & `foliolib-0.3.9a2/foliolib/folio/api/kbEbscoJava.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/ldp.py` & `foliolib-0.3.9a2/foliolib/folio/api/ldp.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/licenses.py` & `foliolib-0.3.9a2/foliolib/folio/api/licenses.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/login.py` & `foliolib-0.3.9a2/foliolib/folio/api/login.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/loginSaml.py` & `foliolib-0.3.9a2/foliolib/folio/api/loginSaml.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/marccat.py` & `foliolib-0.3.9a2/foliolib/folio/api/marccat.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/metaStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/metaStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/notes.py` & `foliolib-0.3.9a2/foliolib/folio/api/notes.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/notify.py` & `foliolib-0.3.9a2/foliolib/folio/api/notify.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/oaiPmh.py` & `foliolib-0.3.9a2/foliolib/folio/api/oaiPmh.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/orders.py` & `foliolib-0.3.9a2/foliolib/folio/api/orders.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/ordersStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/ordersStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/organizations.py` & `foliolib-0.3.9a2/foliolib/folio/api/organizations.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/organizationsStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/organizationsStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/passwordValidator.py` & `foliolib-0.3.9a2/foliolib/folio/api/passwordValidator.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/patron.py` & `foliolib-0.3.9a2/foliolib/folio/api/patron.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/patronBlocks.py` & `foliolib-0.3.9a2/foliolib/folio/api/patronBlocks.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/permissions.py` & `foliolib-0.3.9a2/foliolib/folio/api/permissions.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/pubsub.py` & `foliolib-0.3.9a2/foliolib/folio/api/pubsub.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/quickMarc.py` & `foliolib-0.3.9a2/foliolib/folio/api/quickMarc.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/remoteStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/remoteStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/reservoir.py` & `foliolib-0.3.9a2/foliolib/folio/api/reservoir.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/rtac.py` & `foliolib-0.3.9a2/foliolib/folio/api/rtac.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/search.py` & `foliolib-0.3.9a2/foliolib/folio/api/search.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/sender.py` & `foliolib-0.3.9a2/foliolib/folio/api/sender.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/settings.py` & `foliolib-0.3.9a2/foliolib/folio/api/settings.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/sharedIndex.py` & `foliolib-0.3.9a2/foliolib/folio/api/sharedIndex.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/sourceRecordManager.py` & `foliolib-0.3.9a2/foliolib/folio/api/sourceRecordManager.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/sourceRecordStorage.py` & `foliolib-0.3.9a2/foliolib/folio/api/sourceRecordStorage.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/tags.py` & `foliolib-0.3.9a2/foliolib/folio/api/tags.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/templateEngine.py` & `foliolib-0.3.9a2/foliolib/folio/api/templateEngine.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/userImport.py` & `foliolib-0.3.9a2/foliolib/folio/api/userImport.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/users.py` & `foliolib-0.3.9a2/foliolib/folio/api/users.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/api/usersBl.py` & `foliolib-0.3.9a2/foliolib/folio/api/usersBl.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/config.py` & `foliolib-0.3.9a2/foliolib/folio/config.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/dataImport.py` & `foliolib-0.3.9a2/foliolib/folio/dataImport.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/inventory.py` & `foliolib-0.3.9a2/foliolib/folio/inventory.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/inventoryReferenceData.py` & `foliolib-0.3.9a2/foliolib/folio/inventoryReferenceData.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/folio/users.py` & `foliolib-0.3.9a2/foliolib/folio/users.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/helper/__init__.py` & `foliolib-0.3.9a2/foliolib/helper/__init__.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/helper/database.py` & `foliolib-0.3.9a2/foliolib/helper/database.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/helper/folio.py` & `foliolib-0.3.9a2/foliolib/helper/folio.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/helper/modules.py` & `foliolib-0.3.9a2/foliolib/helper/modules.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/helper/okapi.py` & `foliolib-0.3.9a2/foliolib/helper/okapi.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/helper/platform.py` & `foliolib-0.3.9a2/foliolib/helper/platform.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/helper/tenant.py` & `foliolib-0.3.9a2/foliolib/helper/tenant.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/okapi/__init__.py` & `foliolib-0.3.9a2/foliolib/okapi/__init__.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/okapi/exceptions.py` & `foliolib-0.3.9a2/foliolib/okapi/exceptions.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/okapi/kubeClient.py` & `foliolib-0.3.9a2/foliolib/okapi/kubeClient.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/okapi/misc.py` & `foliolib-0.3.9a2/foliolib/okapi/misc.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/okapi/okapiClient.py` & `foliolib-0.3.9a2/foliolib/okapi/okapiClient.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/okapi/okapiModule.py` & `foliolib-0.3.9a2/foliolib/okapi/okapiModule.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib/okapi/okapiModuleKubernetes.py` & `foliolib-0.3.9a2/foliolib/okapi/okapiModuleKubernetes.py`

 * *Files identical despite different names*

### Comparing `foliolib-0.3.9a1/foliolib.egg-info/PKG-INFO` & `foliolib-0.3.9a2/foliolib.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: foliolib
-Version: 0.3.9a1
+Version: 0.3.9a2
 Summary: Okapi/Folio Manager and Library
 Home-page: https://github.com/tobi-weber/foliolib
 Author: Tobias Weber
 Author-email: tobi-weber@gmx.de
 License: GPL-3.0 License
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `foliolib-0.3.9a1/foliolib.egg-info/SOURCES.txt` & `foliolib-0.3.9a2/foliolib.egg-info/SOURCES.txt`

 * *Files 14% similar despite different names*

```diff
@@ -13,14 +13,29 @@
 foliolib.egg-info/dependency_links.txt
 foliolib.egg-info/entry_points.txt
 foliolib.egg-info/requires.txt
 foliolib.egg-info/top_level.txt
 foliolib/apiBuilder/__init__.py
 foliolib/apiBuilder/build_api.py
 foliolib/apiBuilder/cli.py
+foliolib/apiBuilder/oas/__init__.py
+foliolib/apiBuilder/oas/baseoas.py
+foliolib/apiBuilder/oas/helper.py
+foliolib/apiBuilder/oas/oaSchema.py
+foliolib/apiBuilder/oas/oaSchemaMethod.py
+foliolib/apiBuilder/oas/oaSchemaPath.py
+foliolib/apiBuilder/oas/operationIds.py
+foliolib/apiBuilder/raml/__init__.py
+foliolib/apiBuilder/raml/codeBuilder.py
+foliolib/apiBuilder/raml/exceptions.py
+foliolib/apiBuilder/raml/helper.py
+foliolib/apiBuilder/raml/names.py
+foliolib/apiBuilder/raml/ramlMethod.py
+foliolib/apiBuilder/raml/ramlUrl.py
+foliolib/apiBuilder/raml/tpl.py
 foliolib/cli/__init__.py
 foliolib/cli/main.py
 foliolib/cli/main_err.py
 foliolib/cli/main_noauth.py
 foliolib/cli/module.py
 foliolib/cli/okapi.py
 foliolib/cli/orderedGroup.py
```

### Comparing `foliolib-0.3.9a1/setup.cfg` & `foliolib-0.3.9a2/setup.cfg`

 * *Files 12% similar despite different names*

```diff
@@ -26,14 +26,16 @@
 	foliolib/cli
 	foliolib/cli/folio
 	foliolib/folio
 	foliolib/folio/api
 	foliolib/helper
 	foliolib/okapi
 	foliolib/apiBuilder
+	foliolib/apiBuilder/raml
+	foliolib/apiBuilder/oas
 install_requires = 
 	PyYAML>=5.3.1
 	inflection>=0.3.1
 	python_magic>=0.4.16
 	requests>=2.24.0
 	lxml>=4.6.1
 	click>=8.1.3
```

