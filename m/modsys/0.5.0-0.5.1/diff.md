# Comparing `tmp/modsys-0.5.0.tar.gz` & `tmp/modsys-0.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "modsys-0.5.0.tar", last modified: Sun Jul 23 18:21:49 2023, max compression
+gzip compressed data, was "modsys-0.5.1.tar", last modified: Sun Jul 23 18:33:51 2023, max compression
```

## Comparing `modsys-0.5.0.tar` & `modsys-0.5.1.tar`

### file list

```diff
@@ -1,80 +1,80 @@
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.600432 modsys-0.5.0/
--rw-r--r--   0 abpyguru   (501) staff       (20)    10964 2023-07-23 18:01:37.000000 modsys-0.5.0/LICENSE
--rw-r--r--   0 abpyguru   (501) staff       (20)    12511 2023-07-23 18:21:49.600172 modsys-0.5.0/PKG-INFO
--rw-r--r--   0 abpyguru   (501) staff       (20)    12090 2023-07-23 18:01:37.000000 modsys-0.5.0/README.md
--rwxr-xr-x   0 abpyguru   (501) staff       (20)      876 2023-07-23 18:01:37.000000 modsys-0.5.0/cli.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.589487 modsys-0.5.0/modsys/
--rw-r--r--   0 abpyguru   (501) staff       (20)     5471 2023-07-23 18:20:46.000000 modsys-0.5.0/modsys/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     8435 2023-07-23 18:20:46.000000 modsys-0.5.0/modsys/client.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.590669 modsys-0.5.0/modsys/connectors/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.590884 modsys-0.5.0/modsys/connectors/aws/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/aws/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.592250 modsys-0.5.0/modsys/connectors/google/
--rw-r--r--   0 abpyguru   (501) staff       (20)      864 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/google/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1077 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/google/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     4419 2023-07-23 18:20:46.000000 modsys-0.5.0/modsys/connectors/google/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1024 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/google/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.592614 modsys-0.5.0/modsys/connectors/microsoft/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/microsoft/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.593954 modsys-0.5.0/modsys/connectors/openai/
--rw-r--r--   0 abpyguru   (501) staff       (20)      851 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/openai/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1073 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/openai/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2569 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/openai/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1006 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/openai/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.594721 modsys-0.5.0/modsys/connectors/sightengine/
--rw-r--r--   0 abpyguru   (501) staff       (20)      840 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/sightengine/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1071 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/sightengine/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2879 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/sightengine/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      982 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/sightengine/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.594899 modsys-0.5.0/modsys/connectors/spot/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/connectors/spot/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2044 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/const.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.595101 modsys-0.5.0/modsys/database/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.595860 modsys-0.5.0/modsys/database/firebase/
--rw-r--r--   0 abpyguru   (501) staff       (20)      820 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/firebase/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1538 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/firebase/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     3544 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/firebase/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1488 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/firebase/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.596039 modsys-0.5.0/modsys/database/mongo/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/mongo/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.596230 modsys-0.5.0/modsys/database/mysql/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/mysql/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.596437 modsys-0.5.0/modsys/database/postgres/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/postgres/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.597153 modsys-0.5.0/modsys/database/supabase/
--rw-r--r--   0 abpyguru   (501) staff       (20)      820 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/supabase/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      789 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/supabase/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1603 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/supabase/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      860 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/database/supabase/local.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     4247 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/exceptions.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2492 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/manager.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.598255 modsys-0.5.0/modsys/plugins/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     5546 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/evaluations.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     3217 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/grading.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2217 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/prompts.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     4072 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/utils.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     6503 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/plugins/validation.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     2114 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/resource.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.598466 modsys-0.5.0/modsys/service/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.598623 modsys-0.5.0/modsys/service/graphql/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/graphql/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.599731 modsys-0.5.0/modsys/service/json/
--rw-r--r--   0 abpyguru   (501) staff       (20)      804 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/json/__init__.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      942 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/json/base.py
--rw-r--r--   0 abpyguru   (501) staff       (20)     1397 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/json/cloud.py
--rw-r--r--   0 abpyguru   (501) staff       (20)      905 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/service/json/local.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.599910 modsys-0.5.0/modsys/tests/
--rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.0/modsys/tests/__init__.py
-drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:21:49.590528 modsys-0.5.0/modsys.egg-info/
--rw-r--r--   0 abpyguru   (501) staff       (20)    12511 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/PKG-INFO
--rw-r--r--   0 abpyguru   (501) staff       (20)     1674 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/SOURCES.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)        1 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/dependency_links.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)       43 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/entry_points.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)      520 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/requires.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)       11 2023-07-23 18:21:49.000000 modsys-0.5.0/modsys.egg-info/top_level.txt
--rw-r--r--   0 abpyguru   (501) staff       (20)       38 2023-07-23 18:21:49.600484 modsys-0.5.0/setup.cfg
--rw-r--r--   0 abpyguru   (501) staff       (20)     2407 2023-07-23 18:21:16.000000 modsys-0.5.0/setup.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.790198 modsys-0.5.1/
+-rw-r--r--   0 abpyguru   (501) staff       (20)    10964 2023-07-23 18:01:37.000000 modsys-0.5.1/LICENSE
+-rw-r--r--   0 abpyguru   (501) staff       (20)    12511 2023-07-23 18:33:51.789915 modsys-0.5.1/PKG-INFO
+-rw-r--r--   0 abpyguru   (501) staff       (20)    12090 2023-07-23 18:01:37.000000 modsys-0.5.1/README.md
+-rwxr-xr-x   0 abpyguru   (501) staff       (20)      876 2023-07-23 18:01:37.000000 modsys-0.5.1/cli.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.776111 modsys-0.5.1/modsys/
+-rw-r--r--   0 abpyguru   (501) staff       (20)     5471 2023-07-23 18:20:46.000000 modsys-0.5.1/modsys/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     8435 2023-07-23 18:20:46.000000 modsys-0.5.1/modsys/client.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.778013 modsys-0.5.1/modsys/connectors/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.778524 modsys-0.5.1/modsys/connectors/aws/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/aws/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.779763 modsys-0.5.1/modsys/connectors/google/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      864 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/google/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1077 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/google/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     4417 2023-07-23 18:32:09.000000 modsys-0.5.1/modsys/connectors/google/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1024 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/google/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.780142 modsys-0.5.1/modsys/connectors/microsoft/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/microsoft/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.782100 modsys-0.5.1/modsys/connectors/openai/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      851 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/openai/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1073 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/openai/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2569 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/openai/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1006 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/openai/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.783168 modsys-0.5.1/modsys/connectors/sightengine/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      840 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/sightengine/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1071 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/sightengine/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2879 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/sightengine/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      982 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/sightengine/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.783427 modsys-0.5.1/modsys/connectors/spot/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/connectors/spot/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2044 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/const.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.783666 modsys-0.5.1/modsys/database/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.784711 modsys-0.5.1/modsys/database/firebase/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      820 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/firebase/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1538 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/firebase/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     3544 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/firebase/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1488 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/firebase/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.784982 modsys-0.5.1/modsys/database/mongo/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/mongo/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.785209 modsys-0.5.1/modsys/database/mysql/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/mysql/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.785412 modsys-0.5.1/modsys/database/postgres/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/postgres/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.786183 modsys-0.5.1/modsys/database/supabase/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      820 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/supabase/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      789 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/supabase/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1603 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/supabase/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      860 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/database/supabase/local.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     4247 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/exceptions.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2492 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/manager.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.787353 modsys-0.5.1/modsys/plugins/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/plugins/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     5546 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/plugins/evaluations.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     3217 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/plugins/grading.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2217 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/plugins/prompts.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     4072 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/plugins/utils.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     6503 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/plugins/validation.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2114 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/resource.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.787545 modsys-0.5.1/modsys/service/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/service/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.787726 modsys-0.5.1/modsys/service/graphql/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/service/graphql/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.789460 modsys-0.5.1/modsys/service/json/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      804 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/service/json/__init__.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      942 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/service/json/base.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1397 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/service/json/cloud.py
+-rw-r--r--   0 abpyguru   (501) staff       (20)      905 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/service/json/local.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.789640 modsys-0.5.1/modsys/tests/
+-rw-r--r--   0 abpyguru   (501) staff       (20)      695 2023-07-23 18:01:37.000000 modsys-0.5.1/modsys/tests/__init__.py
+drwxr-xr-x   0 abpyguru   (501) staff       (20)        0 2023-07-23 18:33:51.777868 modsys-0.5.1/modsys.egg-info/
+-rw-r--r--   0 abpyguru   (501) staff       (20)    12511 2023-07-23 18:33:51.000000 modsys-0.5.1/modsys.egg-info/PKG-INFO
+-rw-r--r--   0 abpyguru   (501) staff       (20)     1674 2023-07-23 18:33:51.000000 modsys-0.5.1/modsys.egg-info/SOURCES.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)        1 2023-07-23 18:33:51.000000 modsys-0.5.1/modsys.egg-info/dependency_links.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)       43 2023-07-23 18:33:51.000000 modsys-0.5.1/modsys.egg-info/entry_points.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)      520 2023-07-23 18:33:51.000000 modsys-0.5.1/modsys.egg-info/requires.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)       11 2023-07-23 18:33:51.000000 modsys-0.5.1/modsys.egg-info/top_level.txt
+-rw-r--r--   0 abpyguru   (501) staff       (20)       38 2023-07-23 18:33:51.790247 modsys-0.5.1/setup.cfg
+-rw-r--r--   0 abpyguru   (501) staff       (20)     2407 2023-07-23 18:33:14.000000 modsys-0.5.1/setup.py
```

### Comparing `modsys-0.5.0/LICENSE` & `modsys-0.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/PKG-INFO` & `modsys-0.5.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: modsys
-Version: 0.5.0
+Version: 0.5.1
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
-Metadata-Version: 2.1 Name: modsys Version: 0.5.0 Summary: A radically simple
+Metadata-Version: 2.1 Name: modsys Version: 0.5.1 Summary: A radically simple
 framework for ML/AI model management Home-page: https://github.com/modsysML/
 modsys Author: ModsysML Author-email: adrbrownx@gmail.com License: Apache
 License, Version 2.0 Platform: Any Classifier: Operating System :: OS
 Independent Classifier: Programming Language :: Python :: 3 Description-
 Content-Type: text/markdown License-File: LICENSE # modsys: model management
 tool [![python](https://img.shields.io/pypi/pyversions/3)](https://
 www.python.org/downloads/) ![GitHub Workflow Status](https://img.shields.io/
```

### Comparing `modsys-0.5.0/README.md` & `modsys-0.5.1/README.md`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/cli.py` & `modsys-0.5.1/cli.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/__init__.py` & `modsys-0.5.1/modsys/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/client.py` & `modsys-0.5.1/modsys/client.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/__init__.py` & `modsys-0.5.1/modsys/connectors/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/aws/__init__.py` & `modsys-0.5.1/modsys/connectors/aws/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/google/__init__.py` & `modsys-0.5.1/modsys/connectors/google/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/google/base.py` & `modsys-0.5.1/modsys/connectors/google/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/google/cloud.py` & `modsys-0.5.1/modsys/connectors/google/cloud.py`

 * *Files 2% similar despite different names*

```diff
@@ -99,16 +99,16 @@
             )
 
     def call_api(
         self,
         prompt: str,
         content_id: str,
         community_id: str,
-        score: float,
-        category: str,
+        score=None,
+        category=None,
     ):
         transformed_data = self.transform(
             prompt, content_id, community_id, score, category
         )
         url = transformed_data["url"]
         body = transformed_data["body"]
```

### Comparing `modsys-0.5.0/modsys/connectors/google/local.py` & `modsys-0.5.1/modsys/connectors/google/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/microsoft/__init__.py` & `modsys-0.5.1/modsys/connectors/microsoft/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/openai/__init__.py` & `modsys-0.5.1/modsys/connectors/openai/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/openai/base.py` & `modsys-0.5.1/modsys/connectors/openai/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/openai/cloud.py` & `modsys-0.5.1/modsys/connectors/openai/cloud.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/openai/local.py` & `modsys-0.5.1/modsys/connectors/openai/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/sightengine/__init__.py` & `modsys-0.5.1/modsys/connectors/sightengine/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/sightengine/base.py` & `modsys-0.5.1/modsys/connectors/sightengine/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/sightengine/cloud.py` & `modsys-0.5.1/modsys/connectors/sightengine/cloud.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/sightengine/local.py` & `modsys-0.5.1/modsys/connectors/sightengine/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/connectors/spot/__init__.py` & `modsys-0.5.1/modsys/connectors/spot/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/const.py` & `modsys-0.5.1/modsys/const.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/__init__.py` & `modsys-0.5.1/modsys/database/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/firebase/__init__.py` & `modsys-0.5.1/modsys/database/firebase/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/firebase/base.py` & `modsys-0.5.1/modsys/database/firebase/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/firebase/cloud.py` & `modsys-0.5.1/modsys/database/firebase/cloud.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/firebase/local.py` & `modsys-0.5.1/modsys/database/firebase/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/mongo/__init__.py` & `modsys-0.5.1/modsys/database/mongo/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/mysql/__init__.py` & `modsys-0.5.1/modsys/database/mysql/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/postgres/__init__.py` & `modsys-0.5.1/modsys/database/postgres/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/supabase/__init__.py` & `modsys-0.5.1/modsys/database/supabase/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/supabase/base.py` & `modsys-0.5.1/modsys/database/supabase/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/supabase/cloud.py` & `modsys-0.5.1/modsys/database/supabase/cloud.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/database/supabase/local.py` & `modsys-0.5.1/modsys/database/supabase/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/exceptions.py` & `modsys-0.5.1/modsys/exceptions.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/manager.py` & `modsys-0.5.1/modsys/manager.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/plugins/__init__.py` & `modsys-0.5.1/modsys/plugins/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/plugins/evaluations.py` & `modsys-0.5.1/modsys/plugins/evaluations.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/plugins/grading.py` & `modsys-0.5.1/modsys/plugins/grading.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/plugins/prompts.py` & `modsys-0.5.1/modsys/plugins/prompts.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/plugins/utils.py` & `modsys-0.5.1/modsys/plugins/utils.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/plugins/validation.py` & `modsys-0.5.1/modsys/plugins/validation.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/resource.py` & `modsys-0.5.1/modsys/resource.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/service/__init__.py` & `modsys-0.5.1/modsys/service/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/service/graphql/__init__.py` & `modsys-0.5.1/modsys/service/graphql/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/service/json/__init__.py` & `modsys-0.5.1/modsys/service/json/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/service/json/base.py` & `modsys-0.5.1/modsys/service/json/base.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/service/json/cloud.py` & `modsys-0.5.1/modsys/service/json/cloud.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/service/json/local.py` & `modsys-0.5.1/modsys/service/json/local.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys/tests/__init__.py` & `modsys-0.5.1/modsys/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys.egg-info/PKG-INFO` & `modsys-0.5.1/modsys.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: modsys
-Version: 0.5.0
+Version: 0.5.1
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
-Metadata-Version: 2.1 Name: modsys Version: 0.5.0 Summary: A radically simple
+Metadata-Version: 2.1 Name: modsys Version: 0.5.1 Summary: A radically simple
 framework for ML/AI model management Home-page: https://github.com/modsysML/
 modsys Author: ModsysML Author-email: adrbrownx@gmail.com License: Apache
 License, Version 2.0 Platform: Any Classifier: Operating System :: OS
 Independent Classifier: Programming Language :: Python :: 3 Description-
 Content-Type: text/markdown License-File: LICENSE # modsys: model management
 tool [![python](https://img.shields.io/pypi/pyversions/3)](https://
 www.python.org/downloads/) ![GitHub Workflow Status](https://img.shields.io/
```

### Comparing `modsys-0.5.0/modsys.egg-info/SOURCES.txt` & `modsys-0.5.1/modsys.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/modsys.egg-info/requires.txt` & `modsys-0.5.1/modsys.egg-info/requires.txt`

 * *Files identical despite different names*

### Comparing `modsys-0.5.0/setup.py` & `modsys-0.5.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -23,15 +23,15 @@
     long_description = f.read()
 
 with open("requirements.txt") as f:
     requirements = f.read().splitlines()
 
 setup(
     name="modsys",
-    version="0.5.0",
+    version="0.5.1",
     description="A radically simple framework for ML/AI model management",
     author="ModsysML",
     author_email="adrbrownx@gmail.com",
     packages=find_packages(),
     py_modules=["cli", "modsys"],
     url="https://github.com/modsysML/modsys",
     license="Apache License, Version 2.0",
```

