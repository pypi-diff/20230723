# Comparing `tmp/kitman-0.1.5.tar.gz` & `tmp/kitman-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "kitman-0.1.5.tar", last modified: Thu Mar 30 19:08:16 2023, max compression
+gzip compressed data, was "kitman-0.2.0.tar", last modified: Sun Jul 23 10:40:07 2023, max compression
```

## Comparing `kitman-0.1.5.tar` & `kitman-0.2.0.tar`

### file list

```diff
@@ -1,103 +1,103 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.666679 kitman-0.1.5/
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-03-30 19:08:01.000000 kitman-0.1.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1376 2023-03-30 19:08:16.666679 kitman-0.1.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      860 2023-03-30 19:08:01.000000 kitman-0.1.5/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      162 2023-03-30 19:08:01.000000 kitman-0.1.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)     1170 2023-03-30 19:08:16.666679 kitman-0.1.5/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.646679 kitman-0.1.5/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.650680 kitman-0.1.5/src/kitman/
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.650680 kitman-0.1.5/src/kitman/cli/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      370 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/conf.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.654680 kitman-0.1.5/src/kitman/core/
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      592 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/commands.py
--rw-r--r--   0 runner    (1001) docker     (123)     1270 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/configs.py
--rw-r--r--   0 runner    (1001) docker     (123)      281 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/converters.py
--rw-r--r--   0 runner    (1001) docker     (123)     6039 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/domain.py
--rw-r--r--   0 runner    (1001) docker     (123)     8010 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/dynamic.py
--rw-r--r--   0 runner    (1001) docker     (123)     1056 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/events.py
--rw-r--r--   0 runner    (1001) docker     (123)      143 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/geo.py
--rw-r--r--   0 runner    (1001) docker     (123)     2008 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/handlers.py
--rw-r--r--   0 runner    (1001) docker     (123)      502 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/queries.py
--rw-r--r--   0 runner    (1001) docker     (123)      502 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/schemas.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.654680 kitman-0.1.5/src/kitman/core/sdk/
--rw-r--r--   0 runner    (1001) docker     (123)      199 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/sdk/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2576 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/sdk/client.py
--rw-r--r--   0 runner    (1001) docker     (123)     3671 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/sdk/decorators.py
--rw-r--r--   0 runner    (1001) docker     (123)      136 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/sdk/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)      111 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/sdk/request.py
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/sdk/response.py
--rw-r--r--   0 runner    (1001) docker     (123)      229 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/core/services.py
--rw-r--r--   0 runner    (1001) docker     (123)      764 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     7623 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kitman.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.658680 kitman-0.1.5/src/kitman/kits/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.658680 kitman-0.1.5/src/kitman/kits/iam/
--rw-r--r--   0 runner    (1001) docker     (123)      158 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.658680 kitman-0.1.5/src/kitman/kits/iam/auth/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/auth/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2609 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/auth/base.py
--rw-r--r--   0 runner    (1001) docker     (123)      750 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/auth/proxy.py
--rw-r--r--   0 runner    (1001) docker     (123)      343 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/auth/token.py
--rw-r--r--   0 runner    (1001) docker     (123)      701 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      319 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/deps.py
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/domain.py
--rw-r--r--   0 runner    (1001) docker     (123)      282 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     2887 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/models.py
--rw-r--r--   0 runner    (1001) docker     (123)     2006 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/iam/services.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.662680 kitman-0.1.5/src/kitman/kits/templating/
--rw-r--r--   0 runner    (1001) docker     (123)      189 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/templating/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      793 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/templating/apps.py
--rw-r--r--   0 runner    (1001) docker     (123)     7656 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/templating/dependency_resolvers.py
--rw-r--r--   0 runner    (1001) docker     (123)     5414 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/templating/domain.py
--rw-r--r--   0 runner    (1001) docker     (123)       95 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/templating/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     7436 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/templating/generics.py
--rw-r--r--   0 runner    (1001) docker     (123)     4512 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/templating/models.py
--rw-r--r--   0 runner    (1001) docker     (123)      121 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/templating/services.py
--rw-r--r--   0 runner    (1001) docker     (123)      940 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/kits/templating/templating.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.662680 kitman-0.1.5/src/kitman/plugins/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.662680 kitman-0.1.5/src/kitman/plugins/beanie/
--rw-r--r--   0 runner    (1001) docker     (123)       90 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/beanie/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2515 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/beanie/deps.py
--rw-r--r--   0 runner    (1001) docker     (123)      151 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/beanie/domain.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.662680 kitman-0.1.5/src/kitman/plugins/cors/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/cors/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/cors/plugin.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.662680 kitman-0.1.5/src/kitman/plugins/loguru/
--rw-r--r--   0 runner    (1001) docker     (123)       33 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/loguru/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      693 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/loguru/plugin.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.662680 kitman-0.1.5/src/kitman/plugins/ormar/
--rw-r--r--   0 runner    (1001) docker     (123)       80 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/ormar/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1729 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/ormar/mixins.py
--rw-r--r--   0 runner    (1001) docker     (123)     1375 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/ormar/models.py
--rw-r--r--   0 runner    (1001) docker     (123)     3253 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/ormar/plugin.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.662680 kitman-0.1.5/src/kitman/plugins/ory/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/ory/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2238 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/ory/iam.py
--rw-r--r--   0 runner    (1001) docker     (123)      210 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/ory/schemas.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.666679 kitman-0.1.5/src/kitman/plugins/redis/
--rw-r--r--   0 runner    (1001) docker     (123)       70 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/redis/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      143 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/redis/client.py
--rw-r--r--   0 runner    (1001) docker     (123)     1926 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/redis/plugin.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.666679 kitman-0.1.5/src/kitman/plugins/stripe/
--rw-r--r--   0 runner    (1001) docker     (123)       55 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/stripe/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.666679 kitman-0.1.5/src/kitman/plugins/stripe/api/
--rw-r--r--   0 runner    (1001) docker     (123)       34 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/stripe/api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/stripe/api/commands.py
--rw-r--r--   0 runner    (1001) docker     (123)      975 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/stripe/api/queries.py
--rw-r--r--   0 runner    (1001) docker     (123)     1280 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/stripe/api/router.py
--rw-r--r--   0 runner    (1001) docker     (123)      110 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/stripe/api/schemas.py
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/stripe/domain.py
--rw-r--r--   0 runner    (1001) docker     (123)      693 2023-03-30 19:08:01.000000 kitman-0.1.5/src/kitman/plugins/stripe/plugin.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.650680 kitman-0.1.5/src/kitman.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1376 2023-03-30 19:08:16.000000 kitman-0.1.5/src/kitman.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2572 2023-03-30 19:08:16.000000 kitman-0.1.5/src/kitman.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-30 19:08:16.000000 kitman-0.1.5/src/kitman.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-03-30 19:08:16.000000 kitman-0.1.5/src/kitman.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-03-30 19:08:16.000000 kitman-0.1.5/src/kitman.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-30 19:08:16.666679 kitman-0.1.5/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1279 2023-03-30 19:08:01.000000 kitman-0.1.5/tests/test_config.py
--rw-r--r--   0 runner    (1001) docker     (123)      568 2023-03-30 19:08:01.000000 kitman-0.1.5/tests/test_errors.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.981662 kitman-0.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-07-23 10:39:52.000000 kitman-0.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1376 2023-07-23 10:40:07.981662 kitman-0.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      860 2023-07-23 10:39:52.000000 kitman-0.2.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      162 2023-07-23 10:39:52.000000 kitman-0.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-07-23 10:40:07.981662 kitman-0.2.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.945662 kitman-0.2.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.953662 kitman-0.2.0/src/kitman/
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.953662 kitman-0.2.0/src/kitman/cli/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      377 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/conf.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.961662 kitman-0.2.0/src/kitman/core/
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      592 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/commands.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2269 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/configs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      281 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/converters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6224 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/domain.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8010 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/dynamic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1056 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/events.py
+-rw-r--r--   0 runner    (1001) docker     (123)      143 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/geo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2008 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/handlers.py
+-rw-r--r--   0 runner    (1001) docker     (123)      502 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/queries.py
+-rw-r--r--   0 runner    (1001) docker     (123)      502 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/schemas.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.961662 kitman-0.2.0/src/kitman/core/sdk/
+-rw-r--r--   0 runner    (1001) docker     (123)      199 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/sdk/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2576 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/sdk/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3671 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/sdk/decorators.py
+-rw-r--r--   0 runner    (1001) docker     (123)      136 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/sdk/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      111 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/sdk/request.py
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/sdk/response.py
+-rw-r--r--   0 runner    (1001) docker     (123)      229 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/core/services.py
+-rw-r--r--   0 runner    (1001) docker     (123)      764 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7606 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kitman.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.961662 kitman-0.2.0/src/kitman/kits/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.965662 kitman-0.2.0/src/kitman/kits/iam/
+-rw-r--r--   0 runner    (1001) docker     (123)      158 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.969662 kitman-0.2.0/src/kitman/kits/iam/auth/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/auth/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2563 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/auth/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)      750 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/auth/proxy.py
+-rw-r--r--   0 runner    (1001) docker     (123)      343 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/auth/token.py
+-rw-r--r--   0 runner    (1001) docker     (123)      701 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      319 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/deps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/domain.py
+-rw-r--r--   0 runner    (1001) docker     (123)      282 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2887 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2006 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/iam/services.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.973662 kitman-0.2.0/src/kitman/kits/templating/
+-rw-r--r--   0 runner    (1001) docker     (123)      189 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/templating/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      756 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/templating/apps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7656 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/templating/dependency_resolvers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6195 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/templating/domain.py
+-rw-r--r--   0 runner    (1001) docker     (123)       95 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/templating/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7338 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/templating/generics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4512 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/templating/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)      121 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/templating/services.py
+-rw-r--r--   0 runner    (1001) docker     (123)      966 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/kits/templating/templating.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.973662 kitman-0.2.0/src/kitman/plugins/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.973662 kitman-0.2.0/src/kitman/plugins/beanie/
+-rw-r--r--   0 runner    (1001) docker     (123)       90 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/beanie/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2515 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/beanie/deps.py
+-rw-r--r--   0 runner    (1001) docker     (123)      151 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/beanie/domain.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.973662 kitman-0.2.0/src/kitman/plugins/cors/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/cors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/cors/plugin.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.973662 kitman-0.2.0/src/kitman/plugins/loguru/
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/loguru/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      693 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/loguru/plugin.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.977662 kitman-0.2.0/src/kitman/plugins/ormar/
+-rw-r--r--   0 runner    (1001) docker     (123)       80 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/ormar/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1729 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/ormar/mixins.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1375 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/ormar/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3469 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/ormar/plugin.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.977662 kitman-0.2.0/src/kitman/plugins/ory/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/ory/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2238 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/ory/iam.py
+-rw-r--r--   0 runner    (1001) docker     (123)      210 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/ory/schemas.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.977662 kitman-0.2.0/src/kitman/plugins/redis/
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/redis/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      143 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/redis/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1926 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/redis/plugin.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.977662 kitman-0.2.0/src/kitman/plugins/stripe/
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/stripe/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.981662 kitman-0.2.0/src/kitman/plugins/stripe/api/
+-rw-r--r--   0 runner    (1001) docker     (123)       34 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/stripe/api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/stripe/api/commands.py
+-rw-r--r--   0 runner    (1001) docker     (123)      975 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/stripe/api/queries.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1280 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/stripe/api/router.py
+-rw-r--r--   0 runner    (1001) docker     (123)      110 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/stripe/api/schemas.py
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/stripe/domain.py
+-rw-r--r--   0 runner    (1001) docker     (123)      693 2023-07-23 10:39:52.000000 kitman-0.2.0/src/kitman/plugins/stripe/plugin.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.953662 kitman-0.2.0/src/kitman.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1376 2023-07-23 10:40:07.000000 kitman-0.2.0/src/kitman.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2572 2023-07-23 10:40:07.000000 kitman-0.2.0/src/kitman.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 10:40:07.000000 kitman-0.2.0/src/kitman.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-07-23 10:40:07.000000 kitman-0.2.0/src/kitman.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 10:40:07.000000 kitman-0.2.0/src/kitman.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:07.981662 kitman-0.2.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1279 2023-07-23 10:39:52.000000 kitman-0.2.0/tests/test_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      568 2023-07-23 10:39:52.000000 kitman-0.2.0/tests/test_errors.py
```

### Comparing `kitman-0.1.5/LICENSE` & `kitman-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/PKG-INFO` & `kitman-0.2.0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kitman
-Version: 0.1.5
+Version: 0.2.0
 Summary: A handy toolkit for building saas applications
 Home-page: https://github.com/madskronborg/kitman
 Author: Mads Kronborg
 Author-email: me@madskronborg.dk
 Project-URL: Bug Tracker, https://github.com/madskronborg/kitman/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `kitman-0.1.5/README.md` & `kitman-0.2.0/README.md`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/setup.cfg` & `kitman-0.2.0/setup.cfg`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = kitman
-version = 0.1.5
+version = 0.2.0
 author = Mads Kronborg
 author_email = me@madskronborg.dk
 description = A handy toolkit for building saas applications
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/madskronborg/kitman
 project_urls = 
@@ -17,14 +17,16 @@
 [options]
 package_dir = 
 	= src
 packages = find:
 python_requires = >=3.10
 install_requires = 
 	pydantic[orjson,email]
+	pydantic-settings
+	pydantic-extra-types
 	ormar
 	fastapi
 	deepmerge
 	httpx[http2]
 	makefun
 	redis
 	hiredis
```

### Comparing `kitman-0.1.5/src/kitman/core/commands.py` & `kitman-0.2.0/src/kitman/core/commands.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/core/domain.py` & `kitman-0.2.0/src/kitman/core/domain.py`

 * *Files 6% similar despite different names*

```diff
@@ -20,17 +20,16 @@
     PhoneNumberFormat,
     PhoneNumberType,
     format_number,
     is_valid_number,
     number_type,
 )
 from phonenumbers import parse as parse_phone_number
-from pydantic import BaseModel, Field, constr, create_model, root_validator, validator
+from pydantic import ConfigDict, BaseModel, Field, constr, create_model, root_validator, validator
 from pydantic.fields import FieldInfo, ModelField
-from pydantic.generics import GenericModel
 
 # Value objects
 OpenAPIResponseType = dict[int | str, dict[str, Any]]
 
 RETURN_TYPE = TypeVar("RETURN_TYPE")
 
 DependencyCallable = Callable[
@@ -54,16 +53,15 @@
     header = "header"
     query = "query"
     cookie = "cookie"
 
 
 # Schemas
 class Schema(BaseModel):
-    class Config:
-        orm_mode = True
+    model_config = ConfigDict(from_attributes=True)
 
 
 class SchemaOut(Schema):
     id: UUID
 
 
 # Entities
@@ -120,25 +118,27 @@
         return model
 
 
 class TimestampedEntity(Entity):
     created: datetime.datetime = Field(default_factory=datetime.datetime.utcnow)
     updated: datetime.datetime = Field(default_factory=datetime.datetime.utcnow)
 
+    # TODO[pydantic]: We couldn't refactor the `validator`, please replace it by `field_validator` manually.
+    # Check https://docs.pydantic.dev/dev-v2/migration/#changes-to-validators for more information.
     @validator("updated", always=True)
     def set_updated(cls, value: datetime.datetime | None, **kwargs):
 
         return datetime.datetime.utcnow()
 
 
 # Pages
 TPageItem = TypeVar("TPageItem", bound=Schema)
 
 
-class Page(GenericModel, Generic[TPageItem]):
+class Page(BaseModel, Generic[TPageItem]):
 
     page: int = 1
     size: int = 100
     total: int
     items: list[TPageItem]
     prev_page: int | None = None
     next_page: int | None = None
```

### Comparing `kitman-0.1.5/src/kitman/core/dynamic.py` & `kitman-0.2.0/src/kitman/core/dynamic.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/core/events.py` & `kitman-0.2.0/src/kitman/core/events.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/core/handlers.py` & `kitman-0.2.0/src/kitman/core/handlers.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/core/sdk/client.py` & `kitman-0.2.0/src/kitman/core/sdk/client.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/core/sdk/decorators.py` & `kitman-0.2.0/src/kitman/core/sdk/decorators.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/exceptions.py` & `kitman-0.2.0/src/kitman/exceptions.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/kitman.py` & `kitman-0.2.0/src/kitman/kitman.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,35 +1,35 @@
 from __future__ import annotations
 
 from typing import Generic, Protocol, TypeVar, overload
 
 from fastapi import FastAPI, Request
 from fastapi.responses import JSONResponse
-from pydantic import BaseModel, BaseSettings
-from pydantic.generics import GenericModel
+from pydantic import BaseModel
 
 from kitman import exceptions
 from kitman.core.commands import Command, CommandHandler, TCommandHandler
 from kitman.core.events import BaseEmitter, DomainEvent, EventHandler
 from kitman.core.queries import Query, QueryHandler, TQueryHandler
 
 from .conf import Settings
+from pydantic_settings import BaseSettings
 
 TKitmanSettings = TypeVar("TKitmanSettings", bound=Settings)
 TInstallableSettings = TypeVar(
     "TInstallableConf", bound=BaseSettings | BaseModel | None
 )
 TInstallable = TypeVar("TInstallable", bound="Installable")
 
 
 class InstallableError(Exception):
     pass
 
 
-class InstallableManager(GenericModel, Generic[TInstallable, TInstallableSettings]):
+class InstallableManager(BaseModel, Generic[TInstallable, TInstallableSettings]):
 
     default_settings: TInstallableSettings | None = None
     require_settings: bool = False
 
     parent: TInstallable | Installable | None = None
 
     plugins: dict[type[Plugin], Plugin] = []
```

### Comparing `kitman-0.1.5/src/kitman/kits/iam/auth/base.py` & `kitman-0.2.0/src/kitman/kits/iam/auth/base.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 import enum
 from collections.abc import Coroutine
 from typing import Generic, Literal, TypeVar
 
 from fastapi import Depends, Header, Query, Request, status
 from pydantic import BaseModel
-from pydantic.generics import GenericModel
 
 from kitman import (
     InstallableManager,
     Kitman,
     Plugin,
     TInstallable,
     TInstallableSettings,
@@ -57,15 +56,15 @@
     def get_value(self, request: Request) -> str | int:
         return request.cookies.get(self.key)
 
 
 # End location strategies
 
 
-class BaseAuthenticationConf(GenericModel, Generic[domain.TUser]):
+class BaseAuthenticationConf(BaseModel, Generic[domain.TUser]):
 
     get_user: Coroutine[list[str | int, bool, bool], None, domain.TUser | None]
     location: BaseLocationStrategy = HeaderLocationStrategy(key="Authentication")
 
 
 TAuthenticationConf = TypeVar("TAuthenticationConf", bound=BaseAuthenticationConf)
```

### Comparing `kitman-0.1.5/src/kitman/kits/iam/auth/proxy.py` & `kitman-0.2.0/src/kitman/kits/iam/auth/proxy.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/kits/iam/conf.py` & `kitman-0.2.0/src/kitman/kits/iam/conf.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/kits/iam/domain.py` & `kitman-0.2.0/src/kitman/kits/iam/domain.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/kits/iam/models.py` & `kitman-0.2.0/src/kitman/kits/iam/models.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/kits/iam/services.py` & `kitman-0.2.0/src/kitman/kits/iam/services.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/kits/templating/apps.py` & `kitman-0.2.0/src/kitman/kits/templating/apps.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,13 +1,11 @@
 from typing import TYPE_CHECKING
-from kitman.core import configs
-from kitman.conf import settings
 
-if TYPE_CHECKING:
-    from .models import 
+from kitman.conf import settings
+from kitman.core import configs
 
 
 class TemplatingModelsConfig(configs.SimpleConfig):
 
     template_variable: configs.ModelConfig
     template_item: configs.ModelConfig
     template: configs.ModelConfig
@@ -22,10 +20,10 @@
 
 class TemplatingServicesConfig(configs.SimpleConfig):
 
     pass
 
 
 class TemplatingConfig(
-    configs.AppConfig[TemplatingModelsConfig, TemplatingServicesConfig]
+    configs.AppConfig[TemplatingModelsConfig, TemplatingServicesConfig, None]
 ):
     pass
```

### Comparing `kitman-0.1.5/src/kitman/kits/templating/dependency_resolvers.py` & `kitman-0.2.0/src/kitman/kits/templating/dependency_resolvers.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/kits/templating/generics.py` & `kitman-0.2.0/src/kitman/kits/templating/generics.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from itertools import chain
 from typing import Generic, Type, overload
 from typing_extensions import Self
-from pydantic import parse_obj_as
+from pydantic import ConfigDict, parse_obj_as
 
 from collections import OrderedDict
 
 from .dependency_resolvers import TemplateDependencyResolver
 
 from . import domain
 
@@ -16,17 +16,15 @@
         domain.TTemplate,
         domain.TTemplateItem,
         domain.TTemplateVariable,
         domain.TTemplateStructure,
         domain.TTemplateBuild,
     ]
 ):
-    class Config:
-        template_structure_model: Type[domain.TTemplateStructure]
-        template_build_model: Type[domain.TTemplateBuild]
+    model_config = ConfigDict()
 
     _group: domain.TTemplateGroup | None = None
     _user_templates: dict[str, domain.TTemplate] = {}
     _user_variables: dict[str, domain.TTemplateVariable] = {}
 
     # Private
     def _get_item_index(
```

### Comparing `kitman-0.1.5/src/kitman/kits/templating/models.py` & `kitman-0.2.0/src/kitman/kits/templating/models.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/kits/templating/templating.py` & `kitman-0.2.0/src/kitman/kits/templating/templating.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from __future__ import annotations
 from . import domain
 from . import generics
+from pydantic import ConfigDict
 
 
 class TemplateVariable(domain.BaseTemplateVariable):
     pass
 
 
 class TemplateItem(domain.BaseTemplateItem["Template"]):
@@ -37,10 +38,8 @@
         Template,
         TemplateItem,
         TemplateVariable,
         TemplateStructure,
         TemplateBuild,
     ]
 ):
-    class Config:
-        template_structure_model = TemplateStructure
-        template_build_model = TemplateBuild
+    model_config = ConfigDict(template_structure_model=TemplateStructure, template_build_model=TemplateBuild)
```

### Comparing `kitman-0.1.5/src/kitman/plugins/beanie/deps.py` & `kitman-0.2.0/src/kitman/plugins/beanie/deps.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/plugins/cors/plugin.py` & `kitman-0.2.0/src/kitman/plugins/cors/plugin.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/plugins/loguru/plugin.py` & `kitman-0.2.0/src/kitman/plugins/loguru/plugin.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/plugins/ormar/mixins.py` & `kitman-0.2.0/src/kitman/plugins/ormar/mixins.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/plugins/ormar/models.py` & `kitman-0.2.0/src/kitman/plugins/ormar/models.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/plugins/ormar/plugin.py` & `kitman-0.2.0/src/kitman/plugins/ormar/plugin.py`

 * *Files 6% similar despite different names*

```diff
@@ -11,19 +11,21 @@
 
 from .models import BaseQueryset
 
 
 class PostgresConf(BaseModel):
 
     SERVER: str | None = None
-    USER: str | None
+    USER: str | None = None
     PASSWORD: str
     DB: str
     URI: PostgresDsn | None = None
 
+    # TODO[pydantic]: We couldn't refactor the `validator`, please replace it by `field_validator` manually.
+    # Check https://docs.pydantic.dev/dev-v2/migration/#changes-to-validators for more information.
     @validator("URI", pre=True)
     def assemble_db_connection(cls, v: str | None, values: dict[str, Any]) -> Any:
         if isinstance(v, str):
             return v
         return PostgresDsn.build(
             scheme="postgres",
             user=values.get("USER"),
```

### Comparing `kitman-0.1.5/src/kitman/plugins/ory/iam.py` & `kitman-0.2.0/src/kitman/plugins/ory/iam.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/plugins/redis/plugin.py` & `kitman-0.2.0/src/kitman/plugins/redis/plugin.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/plugins/stripe/api/queries.py` & `kitman-0.2.0/src/kitman/plugins/stripe/api/queries.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/plugins/stripe/api/router.py` & `kitman-0.2.0/src/kitman/plugins/stripe/api/router.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman/plugins/stripe/plugin.py` & `kitman-0.2.0/src/kitman/plugins/stripe/plugin.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/src/kitman.egg-info/PKG-INFO` & `kitman-0.2.0/src/kitman.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kitman
-Version: 0.1.5
+Version: 0.2.0
 Summary: A handy toolkit for building saas applications
 Home-page: https://github.com/madskronborg/kitman
 Author: Mads Kronborg
 Author-email: me@madskronborg.dk
 Project-URL: Bug Tracker, https://github.com/madskronborg/kitman/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `kitman-0.1.5/src/kitman.egg-info/SOURCES.txt` & `kitman-0.2.0/src/kitman.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/tests/test_config.py` & `kitman-0.2.0/tests/test_config.py`

 * *Files identical despite different names*

### Comparing `kitman-0.1.5/tests/test_errors.py` & `kitman-0.2.0/tests/test_errors.py`

 * *Files identical despite different names*

