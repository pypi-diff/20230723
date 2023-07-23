# Comparing `tmp/modsys-0.4.4.tar.gz` & `tmp/modsys-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "modsys-0.4.4.tar", last modified: Sat Jul 15 23:38:39 2023, max compression
+gzip compressed data, was "modsys-0.5.0.tar", last modified: Sun Jul 23 18:21:49 2023, max compression
```

## Comparing `modsys-0.4.4.tar` & `modsys-0.5.0.tar`

### file list

```diff
@@ -1,80 +1,80 @@
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.804917 modsys-0.4.4/
--rw-r--r--   0 abpyguru   (501) staff       (20)    10964 2023-07-11 22:52:05.000000 modsys-0.4.4/LICENSE
--rw-r--r--   0 abpyguru   (501) staff       (20)    12511 2023-07-15 23:38:39.804683 modsys-0.4.4/PKG-INFO
--rw-r--r--   0 abpyguru   (501) staff       (20)    12090 2023-07-11 22:52:05.000000 modsys-0.4.4/README.md
--rwxr-xr-x   0 abpyguru   (501) staff       (20)      876 2023-07-11 22:52:05.000000 modsys-0.4.4/cli.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.790390 modsys-0.4.4/modsys/
--rw-r--r--   0 abpyguru   (501) staff       (20)     5463 2023-07-14 02:29:55.000000 modsys-0.4.4/modsys/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     8057 2023-07-15 23:37:12.000000 modsys-0.4.4/modsys/client.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.792031 modsys-0.4.4/modsys/connectors/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.792235 modsys-0.4.4/modsys/connectors/aws/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-12 15:51:16.000000 modsys-0.4.4/modsys/connectors/aws/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.796095 modsys-0.4.4/modsys/connectors/google/
--rw-r--r--   0 abpyguru   (501) staff       (20)      864 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/google/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1077 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/google/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2887 2023-07-13 04:55:23.000000 modsys-0.4.4/modsys/connectors/google/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1024 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/google/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.796452 modsys-0.4.4/modsys/connectors/microsoft/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-12 15:51:16.000000 modsys-0.4.4/modsys/connectors/microsoft/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.797315 modsys-0.4.4/modsys/connectors/openai/
--rw-r--r--   0 abpyguru   (501) staff       (20)      851 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/openai/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1073 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/openai/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2569 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/openai/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1006 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/openai/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.798294 modsys-0.4.4/modsys/connectors/sightengine/
--rw-r--r--   0 abpyguru   (501) staff       (20)      840 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/sightengine/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1071 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/sightengine/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2879 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/sightengine/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      982 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/connectors/sightengine/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.798520 modsys-0.4.4/modsys/connectors/spot/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-12 15:51:16.000000 modsys-0.4.4/modsys/connectors/spot/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2044 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/const.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.798810 modsys-0.4.4/modsys/database/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.799997 modsys-0.4.4/modsys/database/firebase/
--rw-r--r--   0 abpyguru   (501) staff       (20)      820 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/firebase/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1538 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/firebase/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     3544 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/firebase/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1488 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/firebase/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.800198 modsys-0.4.4/modsys/database/mongo/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/mongo/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.800384 modsys-0.4.4/modsys/database/mysql/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/mysql/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.800571 modsys-0.4.4/modsys/database/postgres/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/postgres/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.801398 modsys-0.4.4/modsys/database/supabase/
--rw-r--r--   0 abpyguru   (501) staff       (20)      820 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/supabase/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      789 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/supabase/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1603 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/supabase/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      860 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/database/supabase/local.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     4247 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/exceptions.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2492 2023-07-14 02:29:55.000000 modsys-0.4.4/modsys/manager.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.802966 modsys-0.4.4/modsys/plugins/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/plugins/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     5296 2023-07-15 23:08:44.000000 modsys-0.4.4/modsys/plugins/evaluations.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     3217 2023-07-15 23:37:12.000000 modsys-0.4.4/modsys/plugins/grading.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2217 2023-07-15 22:44:53.000000 modsys-0.4.4/modsys/plugins/prompts.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     4072 2023-07-15 23:08:44.000000 modsys-0.4.4/modsys/plugins/utils.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     6503 2023-07-15 22:44:53.000000 modsys-0.4.4/modsys/plugins/validation.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2114 2023-07-14 02:29:55.000000 modsys-0.4.4/modsys/resource.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.803279 modsys-0.4.4/modsys/service/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/service/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.803458 modsys-0.4.4/modsys/service/graphql/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/service/graphql/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.804219 modsys-0.4.4/modsys/service/json/
--rw-r--r--   0 abpyguru   (501) staff       (20)      804 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/service/json/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      942 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/service/json/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1397 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/service/json/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      905 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/service/json/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.804414 modsys-0.4.4/modsys/tests/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-11 22:52:05.000000 modsys-0.4.4/modsys/tests/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-15 23:38:39.791847 modsys-0.4.4/modsys.egg-info/
--rw-r--r--   0 abpyguru   (501) staff       (20)    12511 2023-07-15 23:38:39.000000 modsys-0.4.4/modsys.egg-info/PKG-INFO
--rw-r--r--   0 abpyguru   (501) staff       (20)     1674 2023-07-15 23:38:39.000000 modsys-0.4.4/modsys.egg-info/SOURCES.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)        1 2023-07-15 23:38:39.000000 modsys-0.4.4/modsys.egg-info/dependency_links.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)       43 2023-07-15 23:38:39.000000 modsys-0.4.4/modsys.egg-info/entry_points.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)      520 2023-07-15 23:38:39.000000 modsys-0.4.4/modsys.egg-info/requires.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)       11 2023-07-15 23:38:39.000000 modsys-0.4.4/modsys.egg-info/top_level.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)       38 2023-07-15 23:38:39.804973 modsys-0.4.4/setup.cfg
--rw-r--r--   0 abpyguru   (501) staff       (20)     2407 2023-07-15 23:38:12.000000 modsys-0.4.4/setup.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.600432 modsys-0.5.0/
+-rw-r--r--   0 abpyguru   (501) staff       (20)    10964 2023-07-23 18:01:37.000000 modsys-0.5.0/LICENSE
+-rw-r--r--   0 abpyguru   (501) staff       (20)    12511 2023-07-23 18:21:49.600172 modsys-0.5.0/PKG-INFO
+-rw-r--r--   0 abpyguru   (501) staff       (20)    12090 2023-07-23 18:01:37.000000 modsys-0.5.0/README.md
+-rwxr-xr-x   0 abpyguru   (501) staff       (20)      876 2023-07-23 18:01:37.000000 modsys-0.5.0/cli.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.589487 modsys-0.5.0/modsys/
+-rw-r--r--   0 abpyguru   (501) staff       (20)     5471 2023-07-23 18:20:46.000000 modsys-0.5.0/modsys/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     8435 2023-07-23 18:20:46.000000 modsys-0.5.0/modsys/client.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.590669 modsys-0.5.0/modsys/connectors/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.590884 modsys-0.5.0/modsys/connectors/aws/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/aws/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.592250 modsys-0.5.0/modsys/connectors/google/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      864 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/google/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1077 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/google/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     4419 2023-07-23 18:20:46.000000 modsys-0.5.0/modsys/connectors/google/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1024 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/google/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.592614 modsys-0.5.0/modsys/connectors/microsoft/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/microsoft/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.593954 modsys-0.5.0/modsys/connectors/openai/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      851 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/openai/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1073 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/openai/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2569 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/openai/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1006 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/openai/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.594721 modsys-0.5.0/modsys/connectors/sightengine/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      840 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/sightengine/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1071 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/sightengine/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2879 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/sightengine/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      982 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/sightengine/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.594899 modsys-0.5.0/modsys/connectors/spot/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/spot/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2044 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/const.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.595101 modsys-0.5.0/modsys/database/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.595860 modsys-0.5.0/modsys/database/firebase/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      820 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/firebase/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1538 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/firebase/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     3544 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/firebase/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1488 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/firebase/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.596039 modsys-0.5.0/modsys/database/mongo/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/mongo/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.596230 modsys-0.5.0/modsys/database/mysql/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/mysql/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.596437 modsys-0.5.0/modsys/database/postgres/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/postgres/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.597153 modsys-0.5.0/modsys/database/supabase/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      820 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/supabase/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      789 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/supabase/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1603 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/supabase/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      860 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/supabase/local.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     4247 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/exceptions.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2492 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/manager.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.598255 modsys-0.5.0/modsys/plugins/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     5546 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/evaluations.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     3217 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/grading.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2217 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/prompts.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     4072 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/utils.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     6503 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/validation.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2114 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/resource.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.598466 modsys-0.5.0/modsys/service/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.598623 modsys-0.5.0/modsys/service/graphql/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/graphql/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.599731 modsys-0.5.0/modsys/service/json/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      804 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/json/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      942 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/json/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1397 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/json/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      905 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/json/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.599910 modsys-0.5.0/modsys/tests/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/tests/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.590528 modsys-0.5.0/modsys.egg-info/
+-rw-r--r--   0 abpyguru   (501) staff       (20)    12511 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/PKG-INFO
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1674 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/SOURCES.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)        1 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/dependency_links.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)       43 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/entry_points.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)      520 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/requires.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)       11 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/top_level.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)       38 2023-07-23 18:21:49.600484 modsys-0.5.0/setup.cfg
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2407 2023-07-23 18:21:16.000000 modsys-0.5.0/setup.py
```

### Comparing `modsys-0.4.4/LICENSE` & `modsys-0.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/PKG-INFO` & `modsys-0.5.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: modsys
-Version: 0.4.4
+Version: 0.5.0
 Summary: A radically simple framework for ML/AI model management
 Home-page: https://github.com/modsysML/modsys
 Author: ModsysML
 Author-email: adrbrownx@gmail.com
 License: Apache License, Version 2.0
 Platform: Any
 Classifier: Operating System :: OS Independent
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: modsys Version: 0.4.4 Summary: A radically simple
+Metadata-Version: 2.1 Name: modsys Version: 0.5.0 Summary: A radically simple
 framework for ML/AI model management Home-page: https://github.com/modsysML/
 modsys Author: ModsysML Author-email: adrbrownx@gmail.com License: Apache
 License, Version 2.0 Platform: Any Classifier: Operating System :: OS
 Independent Classifier: Programming Language :: Python :: 3 Description-
 Content-Type: text/markdown License-File: LICENSE # modsys: model management
 tool [![python](https://img.shields.io/pypi/pyversions/3)](https://
 www.python.org/downloads/) ![GitHub Workflow Status](https://img.shields.io/
```

### Comparing `modsys-0.4.4/README.md` & `modsys-0.5.0/README.md`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/cli.py` & `modsys-0.5.0/cli.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/__init__.py` & `modsys-0.5.0/modsys/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -75,15 +75,15 @@
     if provider_path.startswith("google_perspective:"):
         path_parts = provider_path.split(":")
         model_name = path_parts[0]
         model_type = path_parts[1]
         if model_type == "analyze":
             return client(model_type, secret)
         elif model_type == "suggest":
-            raise NotImplementedError
+            return client(model_type, secret)
         else:
             raise ValueError(f"Unknown OpenAI model type: {model_type}")
     else:
         return importlib.import_module(provider_path).default()
 
 
 def get_sightengine_client(
```

### Comparing `modsys-0.4.4/modsys/client.py` & `modsys-0.5.0/modsys/client.py`

 * *Files 3% similar despite different names*

```diff
@@ -150,22 +150,24 @@
             )
         else:
             return f"Provider {provider} not found"
 
     @classmethod
     def detectText(cls, *args, **kwargs):
         """
-        Detects text using the appropriate provider based on the `model` attribute of the class.
+        Detects text using the appropriate provider based on the `model` attribute of the class. If using google_perspective can also suggest scores as well.
 
         :param text: The text to be detected (optional).
         :type text: str
         :param operator: The operator to be used (optional).
         :type operator: str
         :param threshold: The threshold value to be used (optional).
         :type threshold: float
+        :param scores: A dict of attributes with their respective scores that you'd like to suggest (optional).
+        :type threshold: dict
 
         :return: The result of the text detection operation.
         :rtype: str
 
         """
         text = kwargs.get("text")
         operator = kwargs.get("operator")
@@ -179,14 +181,16 @@
                 cls._google_perspective_provider_path,
                 secret=cls._google_perspective_auth_token,
             )
             return conn.call_api(
                 kwargs["prompt"] if "prompt" in kwargs else None,
                 kwargs["content_id"] if "content_id" in kwargs else None,
                 kwargs["community_id"] if "community_id" in kwargs else None,
+                kwargs["score"] if "score" in kwargs else None,
+                kwargs["category"] if "category" in kwargs else None,
             )
         else:
             return "No provider connected"
 
     @classmethod
     def detectImage(cls, url, *args, **kwargs):
         if cls.model == "Sightengine":
@@ -196,15 +200,15 @@
                 cls._sightengine_api_user,
             )
             return conn.call_api(url)
         else:
             raise NotImplementedError
 
     @classmethod
-    def evaluate(cls, vars: list):
+    def evaluate(cls, vars: list, community_id):
         """
         After setting up the connection criteria for google_perspecitve
         run the evaluation.
 
         vars (json): [
             {
                 "item": "You suck at this game.",
@@ -226,13 +230,13 @@
             )
         else:
             raise NotImplementedError
 
         options = {"prompts": ["evaluate: {{item}}"], "vars": vars, "providers": [conn]}
 
         # Evaluation
-        summary = evaluate(options, conn)
+        summary = evaluate(options, conn, community_id=community_id)
         print_yellow = lambda x: cprint(x, "yellow")
         print_yellow(f"Evaluation complete: {json.dumps(summary['stats'], indent=4)}")
 
         # Output
         return summary["results"]
```

### Comparing `modsys-0.4.4/modsys/connectors/__init__.py` & `modsys-0.5.0/modsys/connectors/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/aws/__init__.py` & `modsys-0.5.0/modsys/connectors/aws/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/google/__init__.py` & `modsys-0.5.0/modsys/connectors/google/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/google/base.py` & `modsys-0.5.0/modsys/connectors/google/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/google/cloud.py` & `modsys-0.5.0/modsys/connectors/openai/cloud.py`

 * *Files 26% similar despite different names*

```diff
@@ -10,73 +10,65 @@
 #
 #    Unless required by applicable law or agreed to in writing, software
 #    distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
 #    WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
 #    License for the specific language governing permissions and limitations
 #    under the License.
 
-from modsys.connectors.google.base import AbstractGooglePerspectiveProvider
-from modsys.exceptions import AuthorizationFailure
-
-import os
 import requests
+import openai
+import os
 
+from modsys.connectors.openai.base import AbstractOpenAIProvider
 
-class GooglePerspectiveProvider(AbstractGooglePerspectiveProvider):
-    api_key_val = os.environ.get("PERSPECTIVE_API_KEY", None)
-    cache = os.environ.get("PERSPECTIVE_CACHE_OUTPUT", True)
-
-    def __init__(self, model_name: str, secret=None) -> None:
-        self.model_name = model_name  # analyze or suggest
-        self.secret = secret
-        if self.api_key_val is None and self.secret is None:
-            raise AuthorizationFailure
-        elif self.secret is None and self.api_key_val is not None:
-            self.api_key = self.api_key_val
-        else:
-            self.api_key = self.secret
 
-        self.cache = bool(self.cache)
+class OpenAiGenericProvider(AbstractOpenAIProvider):
+    temp_val = os.environ.get("OPENAI_TEMPERATURE", 0)
+    max_token_val = os.environ.get("OPENAI_MAX_TOKENS", 1024)
+    api_key_val = os.environ.get("OPENAI_API_KEY", None)
+
+    def __init__(self, model_name: str) -> None:
+        self.model_name = model_name
+        self.api_key = self.api_key_val
+        self.tokens = int(self.max_token_val)
+        self.temp = int(self.temp_val)
 
     def id(self) -> str:
-        return f"google_perspective:{self.model_name}"
+        return f"openai:{self.model_name}"
 
     def to_string(self) -> str:
-        return f"[Google Perspective Provider {self.model_name}]"
+        return f"[OpenAI Provider {self.model_name}]"
+
+    def token_settings(self) -> str:
+        return f"Using {self.tokens} tokens"
 
-    def cache_settings(self) -> str:
-        return f"Persist model output set to {self.cache}"
+    def temp_settings(self) -> str:
+        return f"Temp set to {self.temp}"
 
-    def call_api(self, prompt: str, content_id: str, community_id: str):
+    def call_api(self, prompt: str):
         body = {
-            "comment": {
-                "text": prompt,
-            },
-            "requestedAttributes": {
-                "TOXICITY": {},
-                "SEVERE_TOXICITY": {},
-                "INSULT": {},
-                "THREAT": {},
-                "SEXUALLY_EXPLICIT": {},
-                "SPAM": {},
-            },
-            "doNotStore": self.cache,
-            "clientToken": content_id,
-            "communityId": community_id,
+            "model": self.model_name,
+            "prompt": prompt,
+            "max_tokens": self.tokens,
+            "temperature": self.temp,
         }
-
         headers = {
             "Content-Type": "application/json",
+            "Authorization": f"Bearer {self.api_key}",
         }
         response = requests.post(
-            f"https://commentanalyzer.googleapis.com/v1alpha1/comments:{self.model_name}?key={self.api_key}",
-            headers=headers,
-            json=body,
+            "https://api.openai.com/v1/completions", headers=headers, json=body
         )
         if response.status_code == 200:
             data = response.json()
-            return data
+            return {
+                "output": data["choices"][0]["text"],
+                "tokenUsage": {
+                    "total": data["usage"]["total_tokens"],
+                    "prompt": data["usage"]["prompt_tokens"],
+                    "completion": data["usage"]["completion_tokens"],
+                },
+            }
         else:
-            print(response.json())
             raise Exception(
-                f"Google Perspective API call failed with status code {response.status_code}"
+                f"OpenAI API call failed with status code {response.json()}"
             )
```

### Comparing `modsys-0.4.4/modsys/connectors/google/local.py` & `modsys-0.5.0/modsys/connectors/google/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/microsoft/__init__.py` & `modsys-0.5.0/modsys/connectors/microsoft/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/openai/__init__.py` & `modsys-0.5.0/modsys/connectors/openai/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/openai/base.py` & `modsys-0.5.0/modsys/connectors/openai/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/openai/local.py` & `modsys-0.5.0/modsys/connectors/openai/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/sightengine/__init__.py` & `modsys-0.5.0/modsys/connectors/sightengine/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/sightengine/base.py` & `modsys-0.5.0/modsys/connectors/sightengine/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/sightengine/cloud.py` & `modsys-0.5.0/modsys/connectors/sightengine/cloud.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/sightengine/local.py` & `modsys-0.5.0/modsys/connectors/sightengine/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/connectors/spot/__init__.py` & `modsys-0.5.0/modsys/connectors/spot/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/const.py` & `modsys-0.5.0/modsys/const.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/__init__.py` & `modsys-0.5.0/modsys/database/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/firebase/__init__.py` & `modsys-0.5.0/modsys/database/firebase/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/firebase/base.py` & `modsys-0.5.0/modsys/database/firebase/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/firebase/cloud.py` & `modsys-0.5.0/modsys/database/firebase/cloud.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/firebase/local.py` & `modsys-0.5.0/modsys/database/firebase/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/mongo/__init__.py` & `modsys-0.5.0/modsys/database/mongo/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/mysql/__init__.py` & `modsys-0.5.0/modsys/database/mysql/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/postgres/__init__.py` & `modsys-0.5.0/modsys/database/postgres/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/supabase/__init__.py` & `modsys-0.5.0/modsys/database/supabase/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/supabase/base.py` & `modsys-0.5.0/modsys/database/supabase/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/supabase/cloud.py` & `modsys-0.5.0/modsys/database/supabase/cloud.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/database/supabase/local.py` & `modsys-0.5.0/modsys/database/supabase/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/exceptions.py` & `modsys-0.5.0/modsys/exceptions.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/manager.py` & `modsys-0.5.0/modsys/manager.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/plugins/__init__.py` & `modsys-0.5.0/modsys/plugins/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/plugins/evaluations.py` & `modsys-0.5.0/modsys/plugins/evaluations.py`

 * *Files 10% similar despite different names*

```diff
@@ -14,16 +14,17 @@
 #    License for the specific language governing permissions and limitations
 #    under the License.
 
 from jinja2 import Template, Environment, meta
 from .grading import matches_expected_val
 
 
-def evaluate(options, provider):
+def evaluate(options, provider, *args, **kwargs):
     results = []
+    community_id = kwargs["community_id"] if "community_id" in kwargs else None
     stats = {
         "successes": 0,
         "failures": 0,
         "error": [],
         "tokenUsage": {
             "total": 0,
             "prompt": 0,
@@ -74,17 +75,20 @@
                 stats["tokenUsage"]["completion"] += (
                     result["tokenUsage"].get("completion", 0) or 0
                 )
             elif provider_path.startswith("google_perspective:"):
                 # NOTE default community_id and content_id's to modsysML since we
                 # don't care about them for this use-case (testing). We only care
                 # when it involves analyzing items for moderation and suggestions
+                if community_id is None:
+                    print("Using modsys as the community ID since its None")
+
                 result = provider.call_api(
                     prompt=rendered_prompt,
-                    community_id="ModsysML",
+                    community_id=community_id if community_id else "ModsysML",
                     content_id="ModsysML",
                 )
 
                 # Find the score to compare against grade
                 result = {
                     key: score["summaryScore"]["value"]
                     for key, score in result["attributeScores"].items()
```

### Comparing `modsys-0.4.4/modsys/plugins/grading.py` & `modsys-0.5.0/modsys/plugins/grading.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/plugins/prompts.py` & `modsys-0.5.0/modsys/plugins/prompts.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/plugins/utils.py` & `modsys-0.5.0/modsys/plugins/utils.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/plugins/validation.py` & `modsys-0.5.0/modsys/plugins/validation.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/resource.py` & `modsys-0.5.0/modsys/resource.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/service/__init__.py` & `modsys-0.5.0/modsys/service/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/service/graphql/__init__.py` & `modsys-0.5.0/modsys/service/graphql/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/service/json/__init__.py` & `modsys-0.5.0/modsys/service/json/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/service/json/base.py` & `modsys-0.5.0/modsys/service/json/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/service/json/cloud.py` & `modsys-0.5.0/modsys/service/json/cloud.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/service/json/local.py` & `modsys-0.5.0/modsys/service/json/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys/tests/__init__.py` & `modsys-0.5.0/modsys/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys.egg-info/PKG-INFO` & `modsys-0.5.0/modsys.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: modsys
-Version: 0.4.4
+Version: 0.5.0
 Summary: A radically simple framework for ML/AI model management
 Home-page: https://github.com/modsysML/modsys
 Author: ModsysML
 Author-email: adrbrownx@gmail.com
 License: Apache License, Version 2.0
 Platform: Any
 Classifier: Operating System :: OS Independent
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: modsys Version: 0.4.4 Summary: A radically simple
+Metadata-Version: 2.1 Name: modsys Version: 0.5.0 Summary: A radically simple
 framework for ML/AI model management Home-page: https://github.com/modsysML/
 modsys Author: ModsysML Author-email: adrbrownx@gmail.com License: Apache
 License, Version 2.0 Platform: Any Classifier: Operating System :: OS
 Independent Classifier: Programming Language :: Python :: 3 Description-
 Content-Type: text/markdown License-File: LICENSE # modsys: model management
 tool [![python](https://img.shields.io/pypi/pyversions/3)](https://
 www.python.org/downloads/) ![GitHub Workflow Status](https://img.shields.io/
```

### Comparing `modsys-0.4.4/modsys.egg-info/SOURCES.txt` & `modsys-0.5.0/modsys.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/modsys.egg-info/requires.txt` & `modsys-0.5.0/modsys.egg-info/requires.txt`

 * *Files identical despite different names*

### Comparing `modsys-0.4.4/setup.py` & `modsys-0.5.0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -23,15 +23,15 @@
     long_description = f.read()
 
 with open("requirements.txt") as f:
     requirements = f.read().splitlines()
 
 setup(
     name="modsys",
-    version="0.4.4",
+    version="0.5.0",
     description="A radically simple framework for ML/AI model management",
     author="ModsysML",
     author_email="adrbrownx@gmail.com",
     packages=find_packages(),
     py_modules=["cli", "modsys"],
     url="https://github.com/modsysML/modsys",
     license="Apache License, Version 2.0",
```

