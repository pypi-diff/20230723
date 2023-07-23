# Comparing `tmp/nonebot2-2.0.0rc4.tar.gz` & `tmp/nonebot2-2.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot2-2.0.0rc4.tar", max compression
+gzip compressed data, was "nonebot2-2.0.1.tar", max compression
```

## Comparing `nonebot2-2.0.0rc4.tar` & `nonebot2-2.0.1.tar`

### file list

```diff
@@ -1,54 +1,53 @@
--rw-r--r--   0        0        0     1078 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/LICENSE
--rw-r--r--   0        0        0    15189 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/README.md
--rw-r--r--   0        0        0    12147 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/__init__.py
--rw-r--r--   0        0        0      742 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/adapters/__init__.py
--rw-r--r--   0        0        0     8480 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/config.py
--rw-r--r--   0        0        0     2148 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/consts.py
--rw-r--r--   0        0        0     6877 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/dependencies/__init__.py
--rw-r--r--   0        0        0     1623 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/dependencies/utils.py
--rw-r--r--   0        0        0     1312 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/drivers/__init__.py
--rw-r--r--   0        0        0     1439 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/drivers/_lifespan.py
--rw-r--r--   0        0        0     5573 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/drivers/aiohttp.py
--rw-r--r--   0        0        0    10258 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/drivers/fastapi.py
--rw-r--r--   0        0        0     2115 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/drivers/httpx.py
--rw-r--r--   0        0        0     4417 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/drivers/none.py
--rw-r--r--   0        0        0     8985 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/drivers/quart.py
--rw-r--r--   0        0        0     3950 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/drivers/websockets.py
--rw-r--r--   0        0        0     6394 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/exception.py
--rw-r--r--   0        0        0        0 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/__init__.py
--rw-r--r--   0        0        0      253 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/adapter/__init__.py
--rw-r--r--   0        0        0     3747 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/adapter/adapter.py
--rw-r--r--   0        0        0     5076 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/adapter/bot.py
--rw-r--r--   0        0        0     2567 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/adapter/event.py
--rw-r--r--   0        0        0     9500 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/adapter/message.py
--rw-r--r--   0        0        0     6322 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/adapter/template.py
--rw-r--r--   0        0        0     1123 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/driver/__init__.py
--rw-r--r--   0        0        0     8526 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/driver/driver.py
--rw-r--r--   0        0        0    11086 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/driver/model.py
--rw-r--r--   0        0        0      464 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/matcher/__init__.py
--rw-r--r--   0        0        0     2760 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/matcher/manager.py
--rw-r--r--   0        0        0    26149 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/matcher/matcher.py
--rw-r--r--   0        0        0      731 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/matcher/provider.py
--rw-r--r--   0        0        0    12389 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/params.py
--rw-r--r--   0        0        0     5623 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/permission.py
--rw-r--r--   0        0        0     3130 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/internal/rule.py
--rw-r--r--   0        0        0     2479 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/log.py
--rw-r--r--   0        0        0      989 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/matcher.py
--rw-r--r--   0        0        0    10148 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/message.py
--rw-r--r--   0        0        0     6083 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/params.py
--rw-r--r--   0        0        0     3047 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/permission.py
--rw-r--r--   0        0        0     5544 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/plugin/__init__.py
--rw-r--r--   0        0        0     5417 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/plugin/load.py
--rw-r--r--   0        0        0     8694 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/plugin/manager.py
--rw-r--r--   0        0        0    29283 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/plugin/on.py
--rw-r--r--   0        0        0    15563 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/plugin/on.pyi
--rw-r--r--   0        0        0     1481 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/plugin/plugin.py
--rw-r--r--   0        0        0      290 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/plugins/echo.py
--rw-r--r--   0        0        0      878 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/plugins/single_session.py
--rw-r--r--   0        0        0        0 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/py.typed
--rw-r--r--   0        0        0    21917 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/rule.py
--rw-r--r--   0        0        0     4822 2023-04-01 03:59:23.818395 nonebot2-2.0.0rc4/nonebot/typing.py
--rw-r--r--   0        0        0     6179 2023-04-01 03:59:23.822395 nonebot2-2.0.0rc4/nonebot/utils.py
--rw-r--r--   0        0        0     2724 2023-04-01 03:59:23.822395 nonebot2-2.0.0rc4/pyproject.toml
--rw-r--r--   0        0        0    17006 1970-01-01 00:00:00.000000 nonebot2-2.0.0rc4/setup.py
--rw-r--r--   0        0        0    17090 1970-01-01 00:00:00.000000 nonebot2-2.0.0rc4/PKG-INFO
+-rw-r--r--   0        0        0     1078 2023-07-23 08:24:31.167328 nonebot2-2.0.1/LICENSE
+-rw-r--r--   0        0        0    17510 2023-07-23 08:24:31.167328 nonebot2-2.0.1/README.md
+-rw-r--r--   0        0        0    12430 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/__init__.py
+-rw-r--r--   0        0        0      913 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/adapters/__init__.py
+-rw-r--r--   0        0        0     9151 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/config.py
+-rw-r--r--   0        0        0     1863 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/consts.py
+-rw-r--r--   0        0        0     6910 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/dependencies/__init__.py
+-rw-r--r--   0        0        0     1668 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/dependencies/utils.py
+-rw-r--r--   0        0        0     1312 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/drivers/__init__.py
+-rw-r--r--   0        0        0     1512 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/drivers/_lifespan.py
+-rw-r--r--   0        0        0     5430 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/drivers/aiohttp.py
+-rw-r--r--   0        0        0    10006 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/drivers/fastapi.py
+-rw-r--r--   0        0        0     2119 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/drivers/httpx.py
+-rw-r--r--   0        0        0     4509 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/drivers/none.py
+-rw-r--r--   0        0        0     9000 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/drivers/quart.py
+-rw-r--r--   0        0        0     3967 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/drivers/websockets.py
+-rw-r--r--   0        0        0     6463 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/exception.py
+-rw-r--r--   0        0        0        0 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/__init__.py
+-rw-r--r--   0        0        0      253 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/adapter/__init__.py
+-rw-r--r--   0        0        0     3747 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/adapter/adapter.py
+-rw-r--r--   0        0        0     5076 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/adapter/bot.py
+-rw-r--r--   0        0        0     2631 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/adapter/event.py
+-rw-r--r--   0        0        0    12281 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/adapter/message.py
+-rw-r--r--   0        0        0     6373 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/adapter/template.py
+-rw-r--r--   0        0        0     1123 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/driver/__init__.py
+-rw-r--r--   0        0        0     8632 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/driver/driver.py
+-rw-r--r--   0        0        0    11228 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/driver/model.py
+-rw-r--r--   0        0        0      464 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/matcher/__init__.py
+-rw-r--r--   0        0        0     2760 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/matcher/manager.py
+-rw-r--r--   0        0        0    26241 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/matcher/matcher.py
+-rw-r--r--   0        0        0      731 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/matcher/provider.py
+-rw-r--r--   0        0        0    15313 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/params.py
+-rw-r--r--   0        0        0     5623 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/permission.py
+-rw-r--r--   0        0        0     3130 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/internal/rule.py
+-rw-r--r--   0        0        0     2501 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/log.py
+-rw-r--r--   0        0        0      989 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/matcher.py
+-rw-r--r--   0        0        0    15088 2023-07-23 08:24:31.167328 nonebot2-2.0.1/nonebot/message.py
+-rw-r--r--   0        0        0     5862 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/params.py
+-rw-r--r--   0        0        0     3063 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/permission.py
+-rw-r--r--   0        0        0     5618 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/plugin/__init__.py
+-rw-r--r--   0        0        0     6904 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/plugin/load.py
+-rw-r--r--   0        0        0     8764 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/plugin/manager.py
+-rw-r--r--   0        0        0    30011 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/plugin/on.py
+-rw-r--r--   0        0        0    14499 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/plugin/on.pyi
+-rw-r--r--   0        0        0     2449 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/plugin/plugin.py
+-rw-r--r--   0        0        0      601 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/plugins/echo.py
+-rw-r--r--   0        0        0     1259 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/plugins/single_session.py
+-rw-r--r--   0        0        0        0 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/py.typed
+-rw-r--r--   0        0        0    22824 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/rule.py
+-rw-r--r--   0        0        0     4980 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/typing.py
+-rw-r--r--   0        0        0     7159 2023-07-23 08:24:31.171328 nonebot2-2.0.1/nonebot/utils.py
+-rw-r--r--   0        0        0     3141 2023-07-23 08:24:31.171328 nonebot2-2.0.1/pyproject.toml
+-rw-r--r--   0        0        0    19521 1970-01-01 00:00:00.000000 nonebot2-2.0.1/PKG-INFO
```

### Comparing `nonebot2-2.0.0rc4/LICENSE` & `nonebot2-2.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/README.md` & `nonebot2-2.0.1/README.md`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 <!-- markdownlint-disable MD033 MD041 -->
 <p align="center">
-  <a href="https://v2.nonebot.dev/"><img src="https://v2.nonebot.dev/logo.png" width="200" height="200" alt="nonebot"></a>
+  <a href="https://nonebot.dev/"><img src="https://nonebot.dev/logo.png" width="200" height="200" alt="nonebot"></a>
 </p>
 
 <div align="center">
 
 # NoneBot
 
 <!-- prettier-ignore-start -->
@@ -15,26 +15,42 @@
 </div>
 
 <p align="center">
   <a href="https://raw.githubusercontent.com/nonebot/nonebot2/master/LICENSE">
     <img src="https://img.shields.io/github/license/nonebot/nonebot2" alt="license">
   </a>
   <a href="https://pypi.python.org/pypi/nonebot2">
-    <img src="https://img.shields.io/pypi/v/nonebot2" alt="pypi">
+    <img src="https://img.shields.io/pypi/v/nonebot2?logo=python&logoColor=edb641" alt="pypi">
   </a>
-  <img src="https://img.shields.io/badge/python-3.8+-blue" alt="python">
+  <img src="https://img.shields.io/badge/python-3.8+-blue?logo=python&logoColor=edb641" alt="python">
+  <a href="https://github.com/psf/black">
+    <img src="https://img.shields.io/badge/code%20style-black-000000.svg?logo=python&logoColor=edb641" alt="black">
+  </a>
+  <a href="https://github.com/Microsoft/pyright">
+    <img src="https://img.shields.io/badge/types-pyright-797952.svg?logo=python&logoColor=edb641" alt="pyright">
+  </a>
+  <a href="https://github.com/astral-sh/ruff">
+    <img src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/charliermarsh/ruff/main/assets/badge/v2.json" alt="ruff">
+  </a>
+  <br />
   <a href="https://codecov.io/gh/nonebot/nonebot2">
     <img src="https://codecov.io/gh/nonebot/nonebot2/branch/master/graph/badge.svg?token=2P0G0VS7N4" alt="codecov"/>
   </a>
   <a href="https://github.com/nonebot/nonebot2/actions/workflows/website-deploy.yml">
     <img src="https://github.com/nonebot/nonebot2/actions/workflows/website-deploy.yml/badge.svg?branch=master&event=push" alt="site"/>
   </a>
   <a href="https://results.pre-commit.ci/latest/github/nonebot/nonebot2/master">
     <img src="https://results.pre-commit.ci/badge/github/nonebot/nonebot2/master.svg" alt="pre-commit" />
   </a>
+  <a href="https://github.com/nonebot/nonebot2/actions/workflows/pyright.yml">
+    <img src="https://github.com/nonebot/nonebot2/actions/workflows/pyright.yml/badge.svg?branch=master&event=push" alt="pyright">
+  </a>
+  <a href="https://github.com/nonebot/nonebot2/actions/workflows/ruff.yml">
+    <img src="https://github.com/nonebot/nonebot2/actions/workflows/ruff.yml/badge.svg?branch=master&event=push" alt="ruff">
+  </a>
   <br />
   <a href="https://onebot.dev/">
     <img src="https://img.shields.io/badge/OneBot-v11-black?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABABAMAAABYR2ztAAAAIVBMVEUAAAAAAAADAwMHBwceHh4UFBQNDQ0ZGRkoKCgvLy8iIiLWSdWYAAAAAXRSTlMAQObYZgAAAQVJREFUSMftlM0RgjAQhV+0ATYK6i1Xb+iMd0qgBEqgBEuwBOxU2QDKsjvojQPvkJ/ZL5sXkgWrFirK4MibYUdE3OR2nEpuKz1/q8CdNxNQgthZCXYVLjyoDQftaKuniHHWRnPh2GCUetR2/9HsMAXyUT4/3UHwtQT2AggSCGKeSAsFnxBIOuAggdh3AKTL7pDuCyABcMb0aQP7aM4AnAbc/wHwA5D2wDHTTe56gIIOUA/4YYV2e1sg713PXdZJAuncdZMAGkAukU9OAn40O849+0ornPwT93rphWF0mgAbauUrEOthlX8Zu7P5A6kZyKCJy75hhw1Mgr9RAUvX7A3csGqZegEdniCx30c3agAAAABJRU5ErkJggg==" alt="onebot">
   </a>
   <a href="https://onebot.dev/">
     <img src="https://img.shields.io/badge/OneBot-v12-black?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABABAMAAABYR2ztAAAAIVBMVEUAAAAAAAADAwMHBwceHh4UFBQNDQ0ZGRkoKCgvLy8iIiLWSdWYAAAAAXRSTlMAQObYZgAAAQVJREFUSMftlM0RgjAQhV+0ATYK6i1Xb+iMd0qgBEqgBEuwBOxU2QDKsjvojQPvkJ/ZL5sXkgWrFirK4MibYUdE3OR2nEpuKz1/q8CdNxNQgthZCXYVLjyoDQftaKuniHHWRnPh2GCUetR2/9HsMAXyUT4/3UHwtQT2AggSCGKeSAsFnxBIOuAggdh3AKTL7pDuCyABcMb0aQP7aM4AnAbc/wHwA5D2wDHTTe56gIIOUA/4YYV2e1sg713PXdZJAuncdZMAGkAukU9OAn40O849+0ornPwT93rphWF0mgAbauUrEOthlX8Zu7P5A6kZyKCJy75hhw1Mgr9RAUvX7A3csGqZegEdniCx30c3agAAAABJRU5ErkJggg==" alt="onebot">
   </a>
@@ -45,17 +61,17 @@
     <img src="https://img.shields.io/badge/%E9%A3%9E%E4%B9%A6-Bot-lightgrey?style=social&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz48c3ZnIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDQ4IDQ4IiBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xNyAyOUMyMSAyOSAyNSAyNi45MzM5IDI4IDIzLjQwNjVDMzYgMTQgNDEuNDI0MiAxNi44MTY2IDQ0IDE3Ljk5OThDMzguNSAyMC45OTk4IDQwLjUgMjkuNjIzMyAzMyAzNS45OTk4QzI4LjM4MiAzOS45MjU5IDIzLjQ5NDUgNDEuMDE0IDE5IDQxQzEyLjUyMzEgNDAuOTc5OSA2Ljg2MjI2IDM3Ljc2MzcgNCAzNS40MDYzVjE2Ljk5OTgiIHN0cm9rZT0iIzMzMyIgc3Ryb2tlLXdpZHRoPSI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz48cGF0aCBkPSJNNS42NDgwOCAxNS44NjY5QzUuMDIyMzEgMTQuOTU2NyAzLjc3NzE1IDE0LjcyNjEgMi44NjY5NCAxNS4zNTE5QzEuOTU2NzMgMTUuOTc3NyAxLjcyNjE1IDE3LjIyMjggMi4zNTE5MiAxOC4xMzMxTDUuNjQ4MDggMTUuODY2OVpNMzYuMDAyMSAzNS43MzA5QzM2Ljk1OCAzNS4xNzc0IDM3LjI4NDMgMzMuOTUzOSAzNi43MzA5IDMyLjk5NzlDMzYuMTc3NCAzMi4wNDIgMzQuOTUzOSAzMS43MTU3IDMzLjk5NzkgMzIuMjY5MUwzNi4wMDIxIDM1LjczMDlaTTIuMzUxOTIgMTguMTMzMUM1LjI0MzUgMjIuMzM5IDEwLjc5OTIgMjguMTQ0IDE2Ljg4NjUgMzIuMjIzOUMxOS45MzQ1IDM0LjI2NjcgMjMuMjE3IDM1Ljk0NiAyNi40NDkgMzYuNzMyNEMyOS42OTQ2IDM3LjUyMiAzMy4wNDUxIDM3LjQ0MjggMzYuMDAyMSAzNS43MzA5TDMzLjk5NzkgMzIuMjY5MUMzMi4yMDQ5IDMzLjMwNzIgMjkuOTkyOSAzMy40NzggMjcuMzk0NyAzMi44NDU4QzI0Ljc4MyAzMi4yMTAzIDIxLjk0MDUgMzAuNzk1OCAxOS4xMTM1IDI4LjkwMTFDMTMuNDUwOCAyNS4xMDYgOC4yNTY1IDE5LjY2MSA1LjY0ODA4IDE1Ljg2NjlMMi4zNTE5MiAxOC4xMzMxWiIgZmlsbD0iIzMzMyIvPjxwYXRoIGQ9Ik0zMy41OTQ1IDE3QzMyLjgzOTggMTQuNzAyNyAzMC44NTQ5IDkuOTQwNTQgMjcuNTk0NSA3SDExLjU5NDVDMTUuMjE3MSAxMC42NzU3IDIzIDE2IDI3IDI0IiBzdHJva2U9IiMzMzMiIHN0cm9rZS13aWR0aD0iNCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+PC9zdmc+" alt="feishu">
   </a>
   <a href="https://docs.github.com/en/developers/apps">
     <img src="https://img.shields.io/badge/GitHub-Bot-181717?style=social&logo=github" alt="github"/>
   </a>
   <a href="https://bot.q.qq.com/wiki/">
     <img src="https://img.shields.io/badge/QQ%E9%A2%91%E9%81%93-Bot-lightgrey?style=social&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMTIuODIgMTMwLjg5Ij48ZyBkYXRhLW5hbWU9IuWbvuWxgiAyIj48ZyBkYXRhLW5hbWU9IuWbvuWxgiAxIj48cGF0aCBkPSJNNTUuNjMgMTMwLjhjLTcgMC0xMy45LjA4LTIwLjg2IDAtMTkuMTUtLjI1LTMxLjcxLTExLjQtMzQuMjItMzAuMy00LjA3LTMwLjY2IDE0LjkzLTU5LjIgNDQuODMtNjYuNjQgMi0uNTEgNS4yMS0uMzEgNS4yMS0xLjYzIDAtMi4xMy4xNC0yLjEzLjE0LTUuNTcgMC0uODktMS4zLTEuNDYtMi4yMi0yLjMxLTYuNzMtNi4yMy03LjY3LTEzLjQxLTEtMjAuMTggNS40LTUuNTIgMTEuODctNS40IDE3LjgtLjU5IDYuNDkgNS4yNiA2LjMxIDEzLjA4LS44NiAyMS0uNjguNzQtMS43OCAxLjYtMS43OCAyLjY3djQuMjFjMCAxLjM1IDIuMiAxLjYyIDQuNzkgMi4zNSAzMS4wOSA4LjY1IDQ4LjE3IDM0LjEzIDQ1IDY2LjM3LTEuNzYgMTguMTUtMTQuNTYgMzAuMjMtMzIuNyAzMC42My04LjAyLjE5LTE2LjA3LS4wMS0yNC4xMy0uMDF6IiBmaWxsPSIjMDI5OWZlIi8+PHBhdGggZD0iTTMxLjQ2IDExOC4zOGMtMTAuNS0uNjktMTYuOC02Ljg2LTE4LjM4LTE3LjI3LTMtMTkuNDIgMi43OC0zNS44NiAxOC40Ni00Ny44MyAxNC4xNi0xMC44IDI5Ljg3LTEyIDQ1LjM4LTMuMTkgMTcuMjUgOS44NCAyNC41OSAyNS44MSAyNCA0NS4yOS0uNDkgMTUuOS04LjQyIDIzLjE0LTI0LjM4IDIzLjUtNi41OS4xNC0xMy4xOSAwLTE5Ljc5IDAiIGZpbGw9IiNmZWZlZmUiLz48cGF0aCBkPSJNNDYuMDUgNzkuNThjLjA5IDUgLjIzIDkuODItNyA5Ljc3LTcuODItLjA2LTYuMS01LjY5LTYuMjQtMTAuMTktLjE1LTQuODItLjczLTEwIDYuNzMtOS44NHM2LjM3IDUuNTUgNi41MSAxMC4yNnoiIGZpbGw9IiMxMDlmZmUiLz48cGF0aCBkPSJNODAuMjcgNzkuMjdjLS41MyAzLjkxIDEuNzUgOS42NC01Ljg4IDEwLTcuNDcuMzctNi44MS00LjgyLTYuNjEtOS41LjItNC4zMi0xLjgzLTEwIDUuNzgtMTAuNDJzNi41OSA0Ljg5IDYuNzEgOS45MnoiIGZpbGw9IiMwODljZmUiLz48L2c+PC9nPjwvc3ZnPg==" alt="QQ频道">
-  <a href="https://ding-doc.dingtalk.com/document#/org-dev-guide/elzz1p">
-    <img src="https://img.shields.io/badge/%E9%92%89%E9%92%89-Bot-lightgrey?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAMAAACdt4HsAAAAnFBMVEUAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD4jUzeAAAAM3RSTlMAQKSRaA+/f0YyFevh29R3cyklIfrlyrGsn41tVUs48c/HqJm9uZdhX1otGwkF9IN8V1CX0Q+IAAABY0lEQVRYw+3V2W7CMBAF0JuNQAhhX9OEfYdu9///rUVWpagE27Ef2gfO+0zGozsKnv6bMGzAhkNytIe5gDdzrwtTCwrbI8x4/NF668NAxgI3Q3UtFi3TyPwNQtPLUUmDd8YfqGLNe4v22XwEYb5zoOuF5baHq2UHtsKe5ivWfGAwrWu2mC34QM0PoCAuqZdOmiwV+5BLyMRtZ7dTSEcs48rzWfzwptMLyzpApka1SJ5FtR4kfCqNIBPEVDmqoqgwUYY5plQOlf6UEjNoOPnuKB6wzDyCrks///TDza8+PnR109WQdxLo8RKWq0PPnuXG0OXKQ6wWLFnCg75uYYbhmMIVVdQ709q33aHbGIj6Duz+2k1HQFX9VwqmY8xYsEJll2ahvhWgsjYLHFRXvIi2Qb0jzMQCzC3FAoydxCma88UCzE3JCWwkjCNYyMUCzHX4DiuTMawEwwhW6hnshPhjZzzJfAH0YacpbmRd7QAAAABJRU5ErkJggg==" alt="dingtalk">
   </a>
+  <!-- <a href="https://ding-doc.dingtalk.com/document#/org-dev-guide/elzz1p">
+    <img src="https://img.shields.io/badge/%E9%92%89%E9%92%89-Bot-lightgrey?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAMAAACdt4HsAAAAnFBMVEUAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD4jUzeAAAAM3RSTlMAQKSRaA+/f0YyFevh29R3cyklIfrlyrGsn41tVUs48c/HqJm9uZdhX1otGwkF9IN8V1CX0Q+IAAABY0lEQVRYw+3V2W7CMBAF0JuNQAhhX9OEfYdu9///rUVWpagE27Ef2gfO+0zGozsKnv6bMGzAhkNytIe5gDdzrwtTCwrbI8x4/NF668NAxgI3Q3UtFi3TyPwNQtPLUUmDd8YfqGLNe4v22XwEYb5zoOuF5baHq2UHtsKe5ivWfGAwrWu2mC34QM0PoCAuqZdOmiwV+5BLyMRtZ7dTSEcs48rzWfzwptMLyzpApka1SJ5FtR4kfCqNIBPEVDmqoqgwUYY5plQOlf6UEjNoOPnuKB6wzDyCrks///TDza8+PnR109WQdxLo8RKWq0PPnuXG0OXKQ6wWLFnCg75uYYbhmMIVVdQ709q33aHbGIj6Duz+2k1HQFX9VwqmY8xYsEJll2ahvhWgsjYLHFRXvIi2Qb0jzMQCzC3FAoydxCma88UCzE3JCWwkjCNYyMUCzHX4DiuTMawEwwhW6hnshPhjZzzJfAH0YacpbmRd7QAAAABJRU5ErkJggg==" alt="dingtalk"> -->
   </a>
   <br />
   <a href="https://jq.qq.com/?_wv=1027&k=5OFifDh">
     <img src="https://img.shields.io/badge/QQ%E7%BE%A4-768887710-orange?style=flat-square" alt="QQ Chat Group">
   </a>
   <a href="https://qun.qq.com/qqweb/qunpro/share?_wv=3&_wwv=128&appChannel=share&inviteCode=7b4a3&appChannel=share&businessType=9&from=246610&biz=ka">
     <img src="https://img.shields.io/badge/QQ%E9%A2%91%E9%81%93-NoneBot-5492ff?style=flat-square" alt="QQ Channel">
@@ -65,77 +81,79 @@
   </a>
   <a href="https://discord.gg/VKtE6Gdc4h">
     <img src="https://discordapp.com/api/guilds/847819937858584596/widget.png?style=shield" alt="Discord Server">
   </a>
 </p>
 
 <p align="center">
-  <a href="https://v2.nonebot.dev/">文档</a>
+  <a href="https://nonebot.dev/">文档</a>
   ·
-  <a href="https://v2.nonebot.dev/docs/quick-start">快速上手</a>
+  <a href="https://nonebot.dev/docs/quick-start">快速上手</a>
   ·
   <a href="#插件">文档打不开？</a>
 </p>
 
 <p align="center">
   <a href="https://asciinema.org/a/569440">
-    <img src="https://v2.nonebot.dev/img/setup.svg">
+    <img src="https://nonebot.dev/img/setup.svg">
   </a>
 </p>
 
 ## 简介
 
 NoneBot2 是一个现代、跨平台、可扩展的 Python 聊天机器人框架，它基于 Python 的类型注解和异步特性，能够为你的需求实现提供便捷灵活的支持。
 
 ## 特色
 
 - 异步优先：基于 Python 的异步特性，即使是~~非常~~大量的消息，也能吞吐自如
 - 易于开发：配合 NB-CLI 脚手架，代码编写上手简单，没有过多的冗余代码，可以让开发者专注于业务逻辑
-- 生而可靠：100% 类型注解覆盖，配合编辑器的类型推导功能，能将绝大多数的 Bug 杜绝在编辑器中 ([编辑器支持](https://v2.nonebot.dev/docs/editor-support))
+- 生而可靠：100% 类型注解覆盖，配合编辑器的类型推导功能，能将绝大多数的 Bug 杜绝在编辑器中 ([编辑器支持](https://nonebot.dev/docs/editor-support))
 - 社区丰富：社区用户众多，直接和间接用户超过十万人，每天都有大量的活跃用户 ([社区资源](#社区资源))
 - 海纳百川：一个框架，支持多个聊天软件平台，可自定义通信协议
 
-  |                                 协议名称                                  | 状态 |                                注释                                |
-  | :-----------------------------------------------------------------------: | :--: | :----------------------------------------------------------------: |
-  |                    [OneBot 协议](https://onebot.dev/)                     |  ✅  | 支持 QQ、TG、微信公众号等[平台](https://onebot.dev/ecosystem.html) |
-  |              [Telegram](https://core.telegram.org/bots/api)               |  ✅  |                                                                    |
-  |            [飞书](https://open.feishu.cn/document/home/index)             |  ✅  |                                                                    |
-  |           [GitHub](https://docs.github.com/en/developers/apps)            |  ✅  |                       GitHub APP & OAuth APP                       |
-  |                   [QQ 频道](https://bot.q.qq.com/wiki/)                   |  ✅  |                          官方接口调整较多                          |
-  |                [钉钉](https://open.dingtalk.com/document/)                |  🤗  |                          寻找 Maintainer                           |
-  |                                  Console                                  |  ✅  |                             控制台交互                             |
-  |                  [开黑啦](https://developer.kookapp.cn/)                  |  ↗️  |                             由社区贡献                             |
-  |           [Mirai](https://docs.mirai.mamoe.net/mirai-api-http/)           |  ↗️  |                             由社区贡献                             |
-  |        [Ntchat](https://github.com/JustUndertaker/adapter-ntchat)         |  ↗️  |                             由社区贡献                             |
-  | [MineCraft (Spigot)](https://github.com/17TheWord/nonebot-adapter-spigot) |  ↗️  |                             由社区贡献                             |
-  |        [BiliBili Live](https://github.com/wwweww/adapter-bilibili)        |  ↗️  |                             由社区贡献                             |
+  |                                                       协议名称                                                        | 状态 |                                   注释                                    |
+  | :-------------------------------------------------------------------------------------------------------------------: | :--: | :-----------------------------------------------------------------------: |
+  |               OneBot（[仓库](https://github.com/nonebot/adapter-onebot)，[协议](https://onebot.dev/)）                |  ✅  | 支持 QQ、TG、微信公众号、KOOK 等[平台](https://onebot.dev/ecosystem.html) |
+  |      Telegram（[仓库](https://github.com/nonebot/adapter-telegram)，[协议](https://core.telegram.org/bots/api)）      |  ✅  |                                                                           |
+  |     飞书（[仓库](https://github.com/nonebot/adapter-feishu)，[协议](https://open.feishu.cn/document/home/index)）     |  ✅  |                                                                           |
+  |         GitHub（[仓库](https://github.com/nonebot/adapter-github)，[协议](https://docs.github.com/en/apps)）          |  ✅  |                          GitHub APP & OAuth APP                           |
+  |           QQ 频道（[仓库](https://github.com/nonebot/adapter-qqguild)，[协议](https://bot.q.qq.com/wiki/)）           |  ✅  |                             官方接口调整较多                              |
+  |         钉钉（[仓库](https://github.com/nonebot/adapter-ding)，[协议](https://open.dingtalk.com/document/)）          |  🤗  |                        寻找 Maintainer（暂不可用）                        |
+  |                             Console（[仓库](https://github.com/nonebot/adapter-console)）                             |  ✅  |                                控制台交互                                 |
+  |     开黑啦（[仓库](https://github.com/Tian-que/nonebot-adapter-kaiheila)，[协议](https://developer.kookapp.cn/)）     |  ↗️  |                                由社区贡献                                 |
+  | Mirai（[仓库](https://github.com/ieew/nonebot_adapter_mirai2)，[协议](https://docs.mirai.mamoe.net/mirai-api-http/)） |  ↗️  |                            QQ 协议，由社区贡献                            |
+  |                          Ntchat（[仓库](https://github.com/JustUndertaker/adapter-ntchat)）                           |  ↗️  |                           微信协议，由社区贡献                            |
+  |                      MineCraft（[仓库](https://github.com/17TheWord/nonebot-adapter-minecraft)）                      |  ↗️  |                                由社区贡献                                 |
+  |                          BiliBili Live（[仓库](https://github.com/wwweww/adapter-bilibili)）                          |  ↗️  |                                由社区贡献                                 |
+  |                       Walle-Q（[仓库](https://github.com/onebot-walle/nonebot_adapter_walleq)）                       |  ↗️  |                            QQ 协议，由社区贡献                            |
+  |                       Villa（[仓库](https://github.com/CMHopeSunshine/nonebot-adapter-villa)）                        |  ↗️  |                     米游社大别野 Bot 协议，由社区贡献                     |
 
 - 坚实后盾：支持多种 web 框架，可自定义替换、组合
 
-  |                          驱动框架                          |  类型  |
-  | :--------------------------------------------------------: | :----: |
-  |          [FastAPI](https://fastapi.tiangolo.com/)          | 服务端 |
-  |   [Quart](https://pgjones.gitlab.io/quart/) (异步 Flask)   | 服务端 |
-  |       [aiohttp](https://docs.aiohttp.org/en/stable/)       | 客户端 |
-  |           [httpx](https://www.python-httpx.org/)           | 客户端 |
-  | [websockets](https://websockets.readthedocs.io/en/stable/) | 客户端 |
+  |                              驱动框架                               |  类型  |
+  | :-----------------------------------------------------------------: | :----: |
+  |              [FastAPI](https://fastapi.tiangolo.com/)               | 服务端 |
+  | [Quart](https://quart.palletsprojects.com/en/latest/)（异步 Flask） | 服务端 |
+  |           [aiohttp](https://docs.aiohttp.org/en/stable/)            | 客户端 |
+  |               [httpx](https://www.python-httpx.org/)                | 客户端 |
+  |     [websockets](https://websockets.readthedocs.io/en/stable/)      | 客户端 |
 
-更多：[概览](https://v2.nonebot.dev/docs/)
+更多：[概览](https://nonebot.dev/docs/)
 
 ## 什么不是 NoneBot2
 
 NoneBot2 不是某个平台或者协议的具体实现，它只负责和已有协议适配器通信，并处理接收到的事件。所以，“NoneBot 有 blabla 平台的 blabla 功能吗？”这种问题是与 NoneBot2 无关的。请在相应平台的功能文档中确认，或与相应平台的协议适配开发者联系。
 
 NoneBot2 不是 NoneBot1 的替代品。事实上，它们都在被积极的维护着。但是，如果你想尝试一些新功能，或者想要支持更多的平台，可以考虑使用 NoneBot2。
 
 > ~~NoneBot2 和 NoneBot1 的区别，就像是 VisualStudio Code 和 VisualStudio 一样~~
 
 ## 即刻开始
 
-~~完整~~文档可以在 [这里](https://v2.nonebot.dev/) 查看。
+~~完整~~文档可以在 [这里](https://nonebot.dev/) 查看。
 
 懒得看文档？下面是快速安装指南：
 
 1. 安装 [pipx](https://pypa.github.io/pipx/)
 
    ```bash
    python -m pip install --user pipx
@@ -184,15 +202,15 @@
   ```
 
   或者尝试以下镜像：
 
   - [文档镜像(中国境内)](https://nb2.baka.icu)
   - [文档镜像(Vercel)](https://nonebot2-vercel-mirror.vercel.app)
 
-- 其他插件请查看 [商店](https://v2.nonebot.dev/store)
+- 其他插件请查看 [商店](https://nonebot.dev/store)
 
 ## 许可证
 
 `NoneBot` 采用 `MIT` 许可证进行开源
 
 ```text
 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
```

#### html2text {}

```diff
@@ -1,60 +1,75 @@
                                    [nonebot]
          # NoneBot   _â¨ è·¨å¹³å° Python å¼æ­¥æºå¨äººæ¡æ¶ â¨_
-           [license] [pypi] [python] [codecov] [site] [pre-commit]
-     [onebot] [onebot] [telegram] [feishu] [github] [QQé¢é]_[dingtalk]
-       [QQ_Chat_Group] [QQ_Channel] [Telegram_Channel] [Discord_Server]
+              [license] [pypi] [python] [black] [pyright] [ruff]
+                [codecov] [site] [pre-commit] [pyright] [ruff]
+          [onebot] [onebot] [telegram] [feishu] [github] [QQé¢é]
+
+[QQ_Chat_Group] [QQ_Channel] [Telegram_Channel] [Discord_Server]
                  ææ¡£ Â· å¿«éä¸æ Â· ææ¡£æä¸å¼ï¼
-                    [https://v2.nonebot.dev/img/setup.svg]
+                      [https://nonebot.dev/img/setup.svg]
 ## ç®ä» NoneBot2 æ¯ä¸ä¸ªç°ä»£ãè·¨å¹³å°ãå¯æ©å±ç Python
 èå¤©æºå¨äººæ¡æ¶ï¼å®åºäº Python
 çç±»åæ³¨è§£åå¼æ­¥ç¹æ§ï¼è½å¤ä¸ºä½ çéæ±å®ç°æä¾ä¾¿æ·çµæ´»çæ¯æã
 ## ç¹è² - å¼æ­¥ä¼åï¼åºäº Python
 çå¼æ­¥ç¹æ§ï¼å³ä½¿æ¯~~éå¸¸~~å¤§éçæ¶æ¯ï¼ä¹è½ååèªå¦ -
 æäºå¼åï¼éå NB-CLI
 èææ¶ï¼ä»£ç ç¼åä¸æç®åï¼æ²¡æè¿å¤çåä½ä»£ç ï¼å¯ä»¥è®©å¼åèä¸æ³¨äºä¸å¡é»è¾
 - çèå¯é ï¼100%
 ç±»åæ³¨è§£è¦çï¼éåç¼è¾å¨çç±»åæ¨å¯¼åè½ï¼è½å°ç»å¤§å¤æ°ç
-Bug æç»å¨ç¼è¾å¨ä¸­ ([ç¼è¾å¨æ¯æ](https://v2.nonebot.dev/docs/
-editor-support)) -
+Bug æç»å¨ç¼è¾å¨ä¸­ ([ç¼è¾å¨æ¯æ](https://nonebot.dev/docs/editor-
+support)) -
 ç¤¾åºä¸°å¯ï¼ç¤¾åºç¨æ·ä¼å¤ï¼ç´æ¥åé´æ¥ç¨æ·è¶è¿åä¸äººï¼æ¯å¤©é½æå¤§éçæ´»è·ç¨æ·
 ([ç¤¾åºèµæº](#ç¤¾åºèµæº)) -
 æµ·çº³ç¾å·ï¼ä¸ä¸ªæ¡æ¶ï¼æ¯æå¤ä¸ªèå¤©è½¯ä»¶å¹³å°ï¼å¯èªå®ä¹éä¿¡åè®®
 | åè®®åç§° | ç¶æ | æ³¨é | | :-----------------------------------------
-------------------------------: | :--: | :-------------------------------------
----------------------------: | | [OneBot åè®®](https://onebot.dev/) | â |
-æ¯æ QQãTGãå¾®ä¿¡å¬ä¼å·ç­[å¹³å°](https://onebot.dev/ecosystem.html)
-| | [Telegram](https://core.telegram.org/bots/api) | â | | | [é£ä¹¦](https:/
-/open.feishu.cn/document/home/index) | â | | | [GitHub](https://
-docs.github.com/en/developers/apps) | â | GitHub APP & OAuth APP | | [QQ
-é¢é](https://bot.q.qq.com/wiki/) | â | å®æ¹æ¥å£è°æ´è¾å¤ | |
-[éé](https://open.dingtalk.com/document/) | ð¤ | å¯»æ¾ Maintainer | |
-Console | â | æ§å¶å°äº¤äº | | [å¼é»å¦](https://developer.kookapp.cn/
-) | âï¸ | ç±ç¤¾åºè´¡ç® | | [Mirai](https://docs.mirai.mamoe.net/mirai-
-api-http/) | âï¸ | ç±ç¤¾åºè´¡ç® | | [Ntchat](https://github.com/
-JustUndertaker/adapter-ntchat) | âï¸ | ç±ç¤¾åºè´¡ç® | | [MineCraft
-(Spigot)](https://github.com/17TheWord/nonebot-adapter-spigot) | âï¸ |
-ç±ç¤¾åºè´¡ç® | | [BiliBili Live](https://github.com/wwweww/adapter-bilibili)
-| âï¸ | ç±ç¤¾åºè´¡ç® | - åå®åç¾ï¼æ¯æå¤ç§ web
-æ¡æ¶ï¼å¯èªå®ä¹æ¿æ¢ãç»å | é©±å¨æ¡æ¶ | ç±»å | | :-------------
--------------------------------------------: | :----: | | [FastAPI](https://
-fastapi.tiangolo.com/) | æå¡ç«¯ | | [Quart](https://pgjones.gitlab.io/quart/
-) (å¼æ­¥ Flask) | æå¡ç«¯ | | [aiohttp](https://docs.aiohttp.org/en/stable/
-) | å®¢æ·ç«¯ | | [httpx](https://www.python-httpx.org/) | å®¢æ·ç«¯ | |
-[websockets](https://websockets.readthedocs.io/en/stable/) | å®¢æ·ç«¯ |
-æ´å¤ï¼[æ¦è§](https://v2.nonebot.dev/docs/) ## ä»ä¹ä¸æ¯ NoneBot2
-NoneBot2
+--------------------------------------------------------------------------: | :
+--: | :-----------------------------------------------------------------------:
+| | OneBotï¼[ä»åº](https://github.com/nonebot/adapter-onebot)ï¼[åè®®]
+(https://onebot.dev/)ï¼ | â | æ¯æ QQãTGãå¾®ä¿¡å¬ä¼å·ãKOOK ç­
+[å¹³å°](https://onebot.dev/ecosystem.html) | | Telegramï¼[ä»åº](https://
+github.com/nonebot/adapter-telegram)ï¼[åè®®](https://core.telegram.org/bots/
+api)ï¼ | â | | | é£ä¹¦ï¼[ä»åº](https://github.com/nonebot/adapter-
+feishu)ï¼[åè®®](https://open.feishu.cn/document/home/index)ï¼ | â | | |
+GitHubï¼[ä»åº](https://github.com/nonebot/adapter-github)ï¼[åè®®](https:/
+/docs.github.com/en/apps)ï¼ | â | GitHub APP & OAuth APP | | QQ é¢éï¼
+[ä»åº](https://github.com/nonebot/adapter-qqguild)ï¼[åè®®](https://
+bot.q.qq.com/wiki/)ï¼ | â | å®æ¹æ¥å£è°æ´è¾å¤ | | ééï¼[ä»åº]
+(https://github.com/nonebot/adapter-ding)ï¼[åè®®](https://open.dingtalk.com/
+document/)ï¼ | ð¤ | å¯»æ¾ Maintainerï¼æä¸å¯ç¨ï¼ | | Consoleï¼
+[ä»åº](https://github.com/nonebot/adapter-console)ï¼ | â | æ§å¶å°äº¤äº
+| | å¼é»å¦ï¼[ä»åº](https://github.com/Tian-que/nonebot-adapter-
+kaiheila)ï¼[åè®®](https://developer.kookapp.cn/)ï¼ | âï¸ |
+ç±ç¤¾åºè´¡ç® | | Miraiï¼[ä»åº](https://github.com/ieew/
+nonebot_adapter_mirai2)ï¼[åè®®](https://docs.mirai.mamoe.net/mirai-api-http/
+)ï¼ | âï¸ | QQ åè®®ï¼ç±ç¤¾åºè´¡ç® | | Ntchatï¼[ä»åº](https://
+github.com/JustUndertaker/adapter-ntchat)ï¼ | âï¸ |
+å¾®ä¿¡åè®®ï¼ç±ç¤¾åºè´¡ç® | | MineCraftï¼[ä»åº](https://github.com/
+17TheWord/nonebot-adapter-minecraft)ï¼ | âï¸ | ç±ç¤¾åºè´¡ç® | | BiliBili
+Liveï¼[ä»åº](https://github.com/wwweww/adapter-bilibili)ï¼ | âï¸ |
+ç±ç¤¾åºè´¡ç® | | Walle-Qï¼[ä»åº](https://github.com/onebot-walle/
+nonebot_adapter_walleq)ï¼ | âï¸ | QQ åè®®ï¼ç±ç¤¾åºè´¡ç® | | Villaï¼
+[ä»åº](https://github.com/CMHopeSunshine/nonebot-adapter-villa)ï¼ | âï¸ |
+ç±³æ¸¸ç¤¾å¤§å«é Bot åè®®ï¼ç±ç¤¾åºè´¡ç® | - åå®åç¾ï¼æ¯æå¤ç§
+web æ¡æ¶ï¼å¯èªå®ä¹æ¿æ¢ãç»å | é©±å¨æ¡æ¶ | ç±»å | | :---------
+--------------------------------------------------------: | :----: | |
+[FastAPI](https://fastapi.tiangolo.com/) | æå¡ç«¯ | | [Quart](https://
+quart.palletsprojects.com/en/latest/)ï¼å¼æ­¥ Flaskï¼ | æå¡ç«¯ | |
+[aiohttp](https://docs.aiohttp.org/en/stable/) | å®¢æ·ç«¯ | | [httpx](https://
+www.python-httpx.org/) | å®¢æ·ç«¯ | | [websockets](https://
+websockets.readthedocs.io/en/stable/) | å®¢æ·ç«¯ | æ´å¤ï¼[æ¦è§](https://
+nonebot.dev/docs/) ## ä»ä¹ä¸æ¯ NoneBot2 NoneBot2
 ä¸æ¯æä¸ªå¹³å°æèåè®®çå·ä½å®ç°ï¼å®åªè´è´£åå·²æåè®®ééå¨éä¿¡ï¼å¹¶å¤çæ¥æ¶å°çäºä»¶ãæä»¥ï¼âNoneBot
 æ blabla å¹³å°ç blabla åè½åï¼âè¿ç§é®é¢æ¯ä¸ NoneBot2
 æ å³çãè¯·å¨ç¸åºå¹³å°çåè½ææ¡£ä¸­ç¡®è®¤ï¼æä¸ç¸åºå¹³å°çåè®®ééå¼åèèç³»ã
 NoneBot2 ä¸æ¯ NoneBot1
 çæ¿ä»£åãäºå®ä¸ï¼å®ä»¬é½å¨è¢«ç§¯æçç»´æ¤çãä½æ¯ï¼å¦æä½ æ³å°è¯ä¸äºæ°åè½ï¼æèæ³è¦æ¯ææ´å¤çå¹³å°ï¼å¯ä»¥èèä½¿ç¨
 NoneBot2ã > ~~NoneBot2 å NoneBot1 çåºå«ï¼å°±åæ¯ VisualStudio Code
 å VisualStudio ä¸æ ·~~ ## å³å»å¼å§ ~~å®æ´~~ææ¡£å¯ä»¥å¨ [è¿é]
-(https://v2.nonebot.dev/) æ¥çã
+(https://nonebot.dev/) æ¥çã
 æå¾çææ¡£ï¼ä¸é¢æ¯å¿«éå®è£æåï¼ 1. å®è£ [pipx](https://
 pypa.github.io/pipx/) ```bash python -m pip install --user pipx python -m pipx
 ensurepath ``` 2. å®è£èææ¶ ```bash pipx install nb-cli ``` 3.
 ä½¿ç¨èææ¶åå»ºé¡¹ç® ```bash nb create ``` 4. è¿è¡é¡¹ç® ```bash nb
 run ``` ## ç¤¾åºèµæº ### å¸¸è§é®é¢ - [å¸¸è§é®é¢è§£ç­(FAQ)](https://
 faq.nonebot.dev/) - [è®ºå(Discussion)](https://discussions.nonebot.dev/) ###
 æç¨/å®éé¡¹ç®/ç»éªåäº« - [awesome-nonebot](https://github.com/
@@ -62,15 +77,15 @@
 è¿æä¸°å¯çå®æ¹ä»¥åç¬¬ä¸æ¹ç°æçæä»¶ä¾å¤§å®¶ä½¿ç¨ï¼ -
 [NoneBot-Plugin-Docs](https://github.com/nonebot/nonebot2/tree/master/packages/
 nonebot-plugin-docs)ï¼ç¦»çº¿ææ¡£è³æ¬å°é¡¹ç®ä½¿ç¨
 (å«åè¯´ææ¡£æä¸å¼äºï¼) å¨é¡¹ç®ç®å½ä¸æ§è¡ï¼ ```bash nb plugin
 install nonebot_plugin_docs ``` æèå°è¯ä»¥ä¸éåï¼ - [ææ¡£éå
 (ä¸­å½å¢å)](https://nb2.baka.icu) - [ææ¡£éå(Vercel)](https://
 nonebot2-vercel-mirror.vercel.app) - å¶ä»æä»¶è¯·æ¥ç [ååº](https://
-v2.nonebot.dev/store) ## è®¸å¯è¯ `NoneBot` éç¨ `MIT` è®¸å¯è¯è¿è¡å¼æº
+nonebot.dev/store) ## è®¸å¯è¯ `NoneBot` éç¨ `MIT` è®¸å¯è¯è¿è¡å¼æº
 ```text THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
 OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
 FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 SOFTWARE. ``` ## è´¡ç® è¯·åè [è´¡ç®æå](./CONTRIBUTING.md) ### é¸£è°¢
```

### Comparing `nonebot2-2.0.0rc4/nonebot/__init__.py` & `nonebot2-2.0.1/nonebot/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -20,20 +20,25 @@
 - `CommandGroup` => {ref}``CommandGroup` <nonebot.plugin.on.CommandGroup>`
 - `Matchergroup` => {ref}``MatcherGroup` <nonebot.plugin.on.MatcherGroup>`
 - `load_plugin` => {ref}``load_plugin` <nonebot.plugin.load.load_plugin>`
 - `load_plugins` => {ref}``load_plugins` <nonebot.plugin.load.load_plugins>`
 - `load_all_plugins` => {ref}``load_all_plugins` <nonebot.plugin.load.load_all_plugins>`
 - `load_from_json` => {ref}``load_from_json` <nonebot.plugin.load.load_from_json>`
 - `load_from_toml` => {ref}``load_from_toml` <nonebot.plugin.load.load_from_toml>`
-- `load_builtin_plugin` => {ref}``load_builtin_plugin` <nonebot.plugin.load.load_builtin_plugin>`
-- `load_builtin_plugins` => {ref}``load_builtin_plugins` <nonebot.plugin.load.load_builtin_plugins>`
+- `load_builtin_plugin` =>
+  {ref}``load_builtin_plugin` <nonebot.plugin.load.load_builtin_plugin>`
+- `load_builtin_plugins` =>
+  {ref}``load_builtin_plugins` <nonebot.plugin.load.load_builtin_plugins>`
 - `get_plugin` => {ref}``get_plugin` <nonebot.plugin.get_plugin>`
-- `get_plugin_by_module_name` => {ref}``get_plugin_by_module_name` <nonebot.plugin.get_plugin_by_module_name>`
-- `get_loaded_plugins` => {ref}``get_loaded_plugins` <nonebot.plugin.get_loaded_plugins>`
-- `get_available_plugin_names` => {ref}``get_available_plugin_names` <nonebot.plugin.get_available_plugin_names>`
+- `get_plugin_by_module_name` =>
+  {ref}``get_plugin_by_module_name` <nonebot.plugin.get_plugin_by_module_name>`
+- `get_loaded_plugins` =>
+  {ref}``get_loaded_plugins` <nonebot.plugin.get_loaded_plugins>`
+- `get_available_plugin_names` =>
+  {ref}``get_available_plugin_names` <nonebot.plugin.get_available_plugin_names>`
 - `require` => {ref}``require` <nonebot.plugin.load.require>`
 
 FrontMatter:
     sidebar_position: 0
     description: nonebot 模块
 """
 
@@ -65,45 +70,56 @@
 
     可用于在计划任务的回调等情形中获取当前 {ref}`nonebot.drivers.Driver` 实例。
 
     返回:
         全局 {ref}`nonebot.drivers.Driver` 对象
 
     异常:
-        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化 ({ref}`nonebot.init <nonebot.init>` 尚未调用)
+        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化
+            ({ref}`nonebot.init <nonebot.init>` 尚未调用)
 
     用法:
         ```python
         driver = nonebot.get_driver()
         ```
     """
     if _driver is None:
         raise ValueError("NoneBot has not been initialized.")
     return _driver
 
 
 @overload
 def get_adapter(name: str) -> Adapter:
-    ...
+    """
+    参数:
+        name: 适配器名称
+
+    返回:
+        指定名称的 {ref}`nonebot.adapters.Adapter` 对象
+    """
 
 
 @overload
 def get_adapter(name: Type[A]) -> A:
-    ...
+    """
+    参数:
+        name: 适配器类型
+
+    返回:
+        指定类型的 {ref}`nonebot.adapters.Adapter` 对象
+    """
 
 
 def get_adapter(name: Union[str, Type[Adapter]]) -> Adapter:
     """获取已注册的 {ref}`nonebot.adapters.Adapter` 实例。
 
-    返回:
-        指定名称或类型的 {ref}`nonebot.adapters.Adapter` 对象
-
     异常:
         ValueError: 指定的 {ref}`nonebot.adapters.Adapter` 未注册
-        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化 ({ref}`nonebot.init <nonebot.init>` 尚未调用)
+        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化
+            ({ref}`nonebot.init <nonebot.init>` 尚未调用)
 
     用法:
         ```python
         from nonebot.adapters.console import Adapter
         adapter = nonebot.get_adapter(Adapter)
         ```
     """
@@ -117,15 +133,16 @@
 def get_adapters() -> Dict[str, Adapter]:
     """获取所有已注册的 {ref}`nonebot.adapters.Adapter` 实例。
 
     返回:
         所有 {ref}`nonebot.adapters.Adapter` 实例字典
 
     异常:
-        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化 ({ref}`nonebot.init <nonebot.init>` 尚未调用)
+        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化
+            ({ref}`nonebot.init <nonebot.init>` 尚未调用)
 
     用法:
         ```python
         adapters = nonebot.get_adapters()
         ```
     """
     return get_driver()._adapters.copy()
@@ -135,37 +152,40 @@
     """获取全局 {ref}`nonebot.drivers.ReverseDriver` 对应的 Server App 对象。
 
     返回:
         Server App 对象
 
     异常:
         AssertionError: 全局 Driver 对象不是 {ref}`nonebot.drivers.ReverseDriver` 类型
-        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化 ({ref}`nonebot.init <nonebot.init>` 尚未调用)
+        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化
+            ({ref}`nonebot.init <nonebot.init>` 尚未调用)
 
     用法:
         ```python
         app = nonebot.get_app()
         ```
     """
     driver = get_driver()
     assert isinstance(
         driver, ReverseDriver
     ), "app object is only available for reverse driver"
     return driver.server_app
 
 
 def get_asgi() -> Any:
-    """获取全局 {ref}`nonebot.drivers.ReverseDriver` 对应 [ASGI](https://asgi.readthedocs.io/) 对象。
+    """获取全局 {ref}`nonebot.drivers.ReverseDriver` 对应
+    [ASGI](https://asgi.readthedocs.io/) 对象。
 
     返回:
         ASGI 对象
 
     异常:
         AssertionError: 全局 Driver 对象不是 {ref}`nonebot.drivers.ReverseDriver` 类型
-        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化 ({ref}`nonebot.init <nonebot.init>` 尚未调用)
+        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化
+            ({ref}`nonebot.init <nonebot.init>` 尚未调用)
 
     用法:
         ```python
         asgi = nonebot.get_asgi()
         ```
     """
     driver = get_driver()
@@ -178,23 +198,25 @@
 def get_bot(self_id: Optional[str] = None) -> Bot:
     """获取一个连接到 NoneBot 的 {ref}`nonebot.adapters.Bot` 对象。
 
     当提供 `self_id` 时，此函数是 `get_bots()[self_id]` 的简写；
     当不提供时，返回一个 {ref}`nonebot.adapters.Bot`。
 
     参数:
-        self_id: 用来识别 {ref}`nonebot.adapters.Bot` 的 {ref}`nonebot.adapters.Bot.self_id` 属性
+        self_id: 用来识别 {ref}`nonebot.adapters.Bot` 的
+            {ref}`nonebot.adapters.Bot.self_id` 属性
 
     返回:
         {ref}`nonebot.adapters.Bot` 对象
 
     异常:
         KeyError: 对应 self_id 的 Bot 不存在
         ValueError: 没有传入 self_id 且没有 Bot 可用
-        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化 ({ref}`nonebot.init <nonebot.init>` 尚未调用)
+        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化
+            ({ref}`nonebot.init <nonebot.init>` 尚未调用)
 
     用法:
         ```python
         assert nonebot.get_bot("12345") == nonebot.get_bots()["12345"]
 
         another_unspecified_bot = nonebot.get_bot()
         ```
@@ -209,18 +231,20 @@
     raise ValueError("There are no bots to get.")
 
 
 def get_bots() -> Dict[str, Bot]:
     """获取所有连接到 NoneBot 的 {ref}`nonebot.adapters.Bot` 对象。
 
     返回:
-        一个以 {ref}`nonebot.adapters.Bot.self_id` 为键，{ref}`nonebot.adapters.Bot` 对象为值的字典
+        一个以 {ref}`nonebot.adapters.Bot.self_id` 为键
+        {ref}`nonebot.adapters.Bot` 对象为值的字典
 
     异常:
-        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化 ({ref}`nonebot.init <nonebot.init>` 尚未调用)
+        ValueError: 全局 {ref}`nonebot.drivers.Driver` 对象尚未初始化
+            ({ref}`nonebot.init <nonebot.init>` 尚未调用)
 
     用法:
         ```python
         bots = nonebot.get_bots()
         ```
     """
     return get_driver().bots
```

### Comparing `nonebot2-2.0.0rc4/nonebot/adapters/__init__.py` & `nonebot2-2.0.1/nonebot/adapters/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -15,10 +15,15 @@
 from nonebot.internal.adapter import MessageTemplate as MessageTemplate
 
 __autodoc__ = {
     "Bot": True,
     "Event": True,
     "Adapter": True,
     "Message": True,
+    "Message.__getitem__": True,
+    "Message.__contains__": True,
+    "Message._construct": True,
     "MessageSegment": True,
+    "MessageSegment.__str__": True,
+    "MessageSegment.__add__": True,
     "MessageTemplate": True,
 }
```

### Comparing `nonebot2-2.0.0rc4/nonebot/config.py` & `nonebot2-2.0.1/nonebot/config.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,92 +1,100 @@
 """本模块定义了 NoneBot 本身运行所需的配置项。
 
-NoneBot 使用 [`pydantic`](https://pydantic-docs.helpmanual.io/) 以及 [`python-dotenv`](https://saurabh-kumar.com/python-dotenv/) 来读取配置。
+NoneBot 使用 [`pydantic`](https://pydantic-docs.helpmanual.io/) 以及
+[`python-dotenv`](https://saurabh-kumar.com/python-dotenv/) 来读取配置。
 
-配置项需符合特殊格式或 json 序列化格式。详情见 [`pydantic Field Type`](https://pydantic-docs.helpmanual.io/usage/types/) 文档。
+配置项需符合特殊格式或 json 序列化格式
+详情见 [`pydantic Field Type`](https://pydantic-docs.helpmanual.io/usage/types/) 文档。
 
 FrontMatter:
     sidebar_position: 1
     description: nonebot.config 模块
 """
+
 import os
 from datetime import timedelta
 from ipaddress import IPv4Address
 from typing import TYPE_CHECKING, Any, Set, Dict, Tuple, Union, Mapping, Optional
 
 from pydantic.utils import deep_update
+from pydantic.fields import Undefined, UndefinedType
 from pydantic import Extra, Field, BaseSettings, IPvAnyAddress
 from pydantic.env_settings import (
     DotenvType,
     SettingsError,
     EnvSettingsSource,
     InitSettingsSource,
     SettingsSourceCallable,
 )
 
 from nonebot.log import logger
 
 
 class CustomEnvSettings(EnvSettingsSource):
     def __call__(self, settings: BaseSettings) -> Dict[str, Any]:
-        """
-        Build environment variables suitable for passing to the Model.
-        """
+        """从环境变量和 dotenv 配置文件中读取配置项。"""
+
         d: Dict[str, Any] = {}
 
         if settings.__config__.case_sensitive:
             env_vars: Mapping[str, Optional[str]] = os.environ  # pragma: no cover
         else:
             env_vars = {k.lower(): v for k, v in os.environ.items()}
 
         env_file_vars = self._read_env_files(settings.__config__.case_sensitive)
         env_vars = {**env_file_vars, **env_vars}
 
         for field in settings.__fields__.values():
-            env_val: Optional[str] = None
+            env_val: Union[str, None, UndefinedType] = Undefined
             for env_name in field.field_info.extra["env_names"]:
-                env_val = env_vars.get(env_name)
+                env_val = env_vars.get(env_name, Undefined)
                 if env_name in env_file_vars:
                     del env_file_vars[env_name]
-                if env_val is not None:
+                if env_val is not Undefined:
                     break
 
             is_complex, allow_parse_failure = self.field_is_complex(field)
             if is_complex:
-                if env_val is None:
+                if isinstance(env_val, UndefinedType):
+                    # field is complex but no value found so far, try explode_env_vars
                     if env_val_built := self.explode_env_vars(field, env_vars):
                         d[field.alias] = env_val_built
+                elif env_val is None:
+                    d[field.alias] = env_val
                 else:
-                    # field is complex and there's a value, decode that as JSON, then add explode_env_vars
+                    # field is complex and there's a value
+                    # decode that as JSON, then add explode_env_vars
                     try:
                         env_val = settings.__config__.parse_env_var(field.name, env_val)
                     except ValueError as e:
                         if not allow_parse_failure:
                             raise SettingsError(
                                 f'error parsing env var "{env_name}"'  # type: ignore
                             ) from e
 
                     if isinstance(env_val, dict):
                         d[field.alias] = deep_update(
                             env_val, self.explode_env_vars(field, env_vars)
                         )
                     else:
                         d[field.alias] = env_val
-            elif env_val is not None:
-                # simplest case, field is not complex, we only need to add the value if it was found
+            elif not isinstance(env_val, UndefinedType):
+                # simplest case, field is not complex
+                # we only need to add the value if it was found
                 d[field.alias] = env_val
 
         # remain user custom config
         for env_name in env_file_vars:
             env_val = env_vars[env_name]
             if env_val and (val_striped := env_val.strip()):
                 # there's a value, decode that as JSON
                 try:
                     env_val = settings.__config__.parse_env_var(env_name, val_striped)
-                except ValueError as e:
+                except ValueError:
                     logger.trace(
                         "Error while parsing JSON for "
                         f"{env_name!r}={val_striped!r}. "
                         "Assumed as string."
                     )
 
             # explode value when it's a nested dict
@@ -135,15 +143,15 @@
                 file_secret_settings,
             )
 
 
 class Env(BaseConfig):
     """运行环境配置。大小写不敏感。
 
-    将会从 `环境变量` > `.env 环境配置文件` 的优先级读取环境信息。
+    将会从 **环境变量** > **dotenv 配置文件** 的优先级读取环境信息。
     """
 
     environment: str = "prod"
     """当前环境名。
 
     NoneBot 将从 `.env.{environment}` 文件中加载配置。
     """
@@ -154,35 +162,37 @@
 
 class Config(BaseConfig):
     """NoneBot 主要配置。大小写不敏感。
 
     除了 NoneBot 的配置项外，还可以自行添加配置项到 `.env.{environment}` 文件中。
     这些配置将会在 json 反序列化后一起带入 `Config` 类中。
 
-    配置方法参考: [配置](https://v2.nonebot.dev/docs/appendices/config)
+    配置方法参考: [配置](https://nonebot.dev/docs/appendices/config)
     """
 
     _env_file: DotenvType = ".env", ".env.prod"
 
     # nonebot configs
     driver: str = "~fastapi"
     """NoneBot 运行所使用的 `Driver` 。继承自 {ref}`nonebot.drivers.Driver` 。
 
     配置格式为 `<module>[:<Driver>][+<module>[:<Mixin>]]*`。
 
     `~` 为 `nonebot.drivers.` 的缩写。
+
+    配置方法参考: [配置驱动器](https://nonebot.dev/docs/advanced/driver#%E9%85%8D%E7%BD%AE%E9%A9%B1%E5%8A%A8%E5%99%A8)
     """
     host: IPvAnyAddress = IPv4Address("127.0.0.1")  # type: ignore
     """NoneBot {ref}`nonebot.drivers.ReverseDriver` 服务端监听的 IP/主机名。"""
     port: int = Field(default=8080, ge=1, le=65535)
     """NoneBot {ref}`nonebot.drivers.ReverseDriver` 服务端监听的端口。"""
     log_level: Union[int, str] = "INFO"
-    """NoneBot 日志输出等级，可以为 `int` 类型等级或等级名称
+    """NoneBot 日志输出等级，可以为 `int` 类型等级或等级名称。
 
-    参考 [`loguru 日志等级`](https://loguru.readthedocs.io/en/stable/api/logger.html#levels)。
+    参考 [记录日志](https://nonebot.dev/docs/appendices/log)，[loguru 日志等级](https://loguru.readthedocs.io/en/stable/api/logger.html#levels)。
 
     :::tip 提示
     日志等级名称应为大写，如 `INFO`。
     :::
 
     用法:
         ```conf
@@ -205,22 +215,26 @@
         ```
     """
     nickname: Set[str] = set()
     """机器人昵称。"""
     command_start: Set[str] = {"/"}
     """命令的起始标记，用于判断一条消息是不是命令。
 
+    参考[命令响应规则](https://nonebot.dev/docs/advanced/matcher#command)。
+
     用法:
         ```conf
         COMMAND_START=["/", ""]
         ```
     """
     command_sep: Set[str] = {"."}
     """命令的分隔标记，用于将文本形式的命令切分为元组（实际的命令名）。
 
+    参考[命令响应规则](https://nonebot.dev/docs/advanced/matcher#command)。
+
     用法:
         ```conf
         COMMAND_SEP=["."]
         ```
     """
     session_expire_timeout: timedelta = timedelta(minutes=2)
     """等待用户回复的超时时间。
```

### Comparing `nonebot2-2.0.0rc4/nonebot/consts.py` & `nonebot2-2.0.1/nonebot/consts.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 """本模块包含了 NoneBot 事件处理过程中使用到的常量。
 
 FrontMatter:
     sidebar_position: 9
     description: nonebot.consts 模块
 """
+
 import os
 import sys
 from typing import Literal
 
 # used by Matcher
 RECEIVE_KEY: Literal["_receive_{id}"] = "_receive_{id}"
 """`receive` 存储 key"""
@@ -38,20 +39,14 @@
 SHELL_ARGS: Literal["_args"] = "_args"
 """shell 命令 parse 后参数字典存储 key"""
 SHELL_ARGV: Literal["_argv"] = "_argv"
 """shell 命令原始参数列表存储 key"""
 
 REGEX_MATCHED: Literal["_matched"] = "_matched"
 """正则匹配结果存储 key"""
-REGEX_STR: Literal["_matched_str"] = "_matched_str"
-"""正则匹配文本存储 key"""
-REGEX_GROUP: Literal["_matched_groups"] = "_matched_groups"
-"""正则匹配 group 元组存储 key"""
-REGEX_DICT: Literal["_matched_dict"] = "_matched_dict"
-"""正则匹配 group 字典存储 key"""
 STARTSWITH_KEY: Literal["_startswith"] = "_startswith"
 """响应触发前缀 key"""
 ENDSWITH_KEY: Literal["_endswith"] = "_endswith"
 """响应触发后缀 key"""
 FULLMATCH_KEY: Literal["_fullmatch"] = "_fullmatch"
 """响应触发完整消息 key"""
 KEYWORD_KEY: Literal["_keyword"] = "_keyword"
```

### Comparing `nonebot2-2.0.0rc4/nonebot/dependencies/__init__.py` & `nonebot2-2.0.1/nonebot/dependencies/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -78,16 +78,16 @@
         pre_checkers: 依赖注入解析前的参数检查
         params: 具名参数列表
         parameterless: 匿名参数列表
         allow_types: 允许的参数类型
     """
 
     call: _DependentCallable[R]
-    params: Tuple[ModelField] = field(default_factory=tuple)
-    parameterless: Tuple[Param] = field(default_factory=tuple)
+    params: Tuple[ModelField, ...] = field(default_factory=tuple)
+    parameterless: Tuple[Param, ...] = field(default_factory=tuple)
 
     def __repr__(self) -> str:
         if inspect.isfunction(self.call) or inspect.isclass(self.call):
             call_str = self.call.__name__
         else:
             call_str = repr(self.call)
         return (
@@ -125,15 +125,16 @@
                 field_info = default_value
             else:
                 for allow_type in allow_types:
                     if field_info := allow_type._check_param(param, allow_types):
                         break
                 else:
                     raise ValueError(
-                        f"Unknown parameter {param.name} for function {call} with type {param.annotation}"
+                        f"Unknown parameter {param.name} "
+                        f"for function {call} with type {param.annotation}"
                     )
 
             default_value = field_info.default
 
             annotation: Any = Any
             required = default_value == Required
             if param.annotation != param.empty:
@@ -178,15 +179,15 @@
         parameterless: Optional[Iterable[Any]] = None,
         allow_types: Iterable[Type[Param]],
     ) -> "Dependent[R]":
         allow_types = tuple(allow_types)
 
         params = cls.parse_params(call, allow_types)
         parameterless_params = (
-            tuple()
+            ()
             if parameterless is None
             else cls.parse_parameterless(tuple(parameterless), allow_types)
         )
 
         return cls(call, params, parameterless_params)
 
     async def check(self, **params: Any) -> None:
```

### Comparing `nonebot2-2.0.0rc4/nonebot/dependencies/utils.py` & `nonebot2-2.0.1/nonebot/dependencies/utils.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,26 +1,28 @@
 """
 FrontMatter:
     sidebar_position: 1
     description: nonebot.dependencies.utils 模块
 """
+
 import inspect
 from typing import Any, Dict, TypeVar, Callable, ForwardRef
 
 from loguru import logger
 from pydantic.fields import ModelField
 from pydantic.typing import evaluate_forwardref
 
 from nonebot.exception import TypeMisMatch
 
 V = TypeVar("V")
 
 
 def get_typed_signature(call: Callable[..., Any]) -> inspect.Signature:
     """获取可调用对象签名"""
+
     signature = inspect.signature(call)
     globalns = getattr(call, "__globals__", {})
     typed_params = [
         inspect.Parameter(
             name=param.name,
             kind=param.kind,
             default=param.default,
@@ -29,25 +31,28 @@
         for param in signature.parameters.values()
     ]
     return inspect.Signature(typed_params)
 
 
 def get_typed_annotation(param: inspect.Parameter, globalns: Dict[str, Any]) -> Any:
     """获取参数的类型注解"""
+
     annotation = param.annotation
     if isinstance(annotation, str):
         annotation = ForwardRef(annotation)
         try:
             annotation = evaluate_forwardref(annotation, globalns, globalns)
         except Exception as e:
             logger.opt(colors=True, exception=e).warning(
                 f'Unknown ForwardRef["{param.annotation}"] for parameter {param.name}'
             )
             return inspect.Parameter.empty
     return annotation
 
 
 def check_field_type(field: ModelField, value: V) -> V:
+    """检查字段类型是否匹配"""
+
     _, errs_ = field.validate(value, {}, loc=())
     if errs_:
         raise TypeMisMatch(field, value)
     return value
```

### Comparing `nonebot2-2.0.0rc4/nonebot/drivers/__init__.py` & `nonebot2-2.0.1/nonebot/drivers/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/nonebot/drivers/_lifespan.py` & `nonebot2-2.0.1/nonebot/drivers/_lifespan.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,14 +1,15 @@
+from typing_extensions import TypeAlias
 from typing import Any, List, Union, Callable, Awaitable, cast
 
 from nonebot.utils import run_sync, is_coroutine_callable
 
-SYNC_LIFESPAN_FUNC = Callable[[], Any]
-ASYNC_LIFESPAN_FUNC = Callable[[], Awaitable[Any]]
-LIFESPAN_FUNC = Union[SYNC_LIFESPAN_FUNC, ASYNC_LIFESPAN_FUNC]
+SYNC_LIFESPAN_FUNC: TypeAlias = Callable[[], Any]
+ASYNC_LIFESPAN_FUNC: TypeAlias = Callable[[], Awaitable[Any]]
+LIFESPAN_FUNC: TypeAlias = Union[SYNC_LIFESPAN_FUNC, ASYNC_LIFESPAN_FUNC]
 
 
 class Lifespan:
     def __init__(self) -> None:
         self._startup_funcs: List[LIFESPAN_FUNC] = []
         self._shutdown_funcs: List[LIFESPAN_FUNC] = []
```

### Comparing `nonebot2-2.0.0rc4/nonebot/drivers/aiohttp.py` & `nonebot2-2.0.1/nonebot/drivers/aiohttp.py`

 * *Files 20% similar despite different names*

```diff
@@ -11,79 +11,81 @@
 :::
 
 FrontMatter:
     sidebar_position: 2
     description: nonebot.drivers.aiohttp 模块
 """
 
+from typing_extensions import override
 from typing import Type, AsyncGenerator
 from contextlib import asynccontextmanager
 
-from nonebot.typing import overrides
 from nonebot.drivers import Request, Response
 from nonebot.exception import WebSocketClosed
 from nonebot.drivers.none import Driver as NoneDriver
 from nonebot.drivers import WebSocket as BaseWebSocket
 from nonebot.drivers import HTTPVersion, ForwardMixin, ForwardDriver, combine_driver
 
 try:
     import aiohttp
 except ModuleNotFoundError as e:  # pragma: no cover
     raise ImportError(
-        "Please install aiohttp first to use this driver. `pip install nonebot2[aiohttp]`"
+        "Please install aiohttp first to use this driver. "
+        "Install with pip: `pip install nonebot2[aiohttp]`"
     ) from e
 
 
 class Mixin(ForwardMixin):
     """AIOHTTP Mixin"""
 
     @property
-    @overrides(ForwardMixin)
+    @override
     def type(self) -> str:
         return "aiohttp"
 
-    @overrides(ForwardMixin)
+    @override
     async def request(self, setup: Request) -> Response:
         if setup.version == HTTPVersion.H10:
             version = aiohttp.HttpVersion10
         elif setup.version == HTTPVersion.H11:
             version = aiohttp.HttpVersion11
         else:
             raise RuntimeError(f"Unsupported HTTP version: {setup.version}")
 
         timeout = aiohttp.ClientTimeout(setup.timeout)
-        files = None
+
+        data = setup.data
         if setup.files:
-            files = aiohttp.FormData()
+            data = aiohttp.FormData(data or {})
             for name, file in setup.files:
-                files.add_field(name, file[1], content_type=file[2], filename=file[0])
+                data.add_field(name, file[1], content_type=file[2], filename=file[0])
 
         cookies = {
             cookie.name: cookie.value for cookie in setup.cookies if cookie.value
         }
         async with aiohttp.ClientSession(
             cookies=cookies, version=version, trust_env=True
         ) as session:
             async with session.request(
                 setup.method,
                 setup.url,
-                data=setup.content or setup.data or files,
+                data=setup.content or data,
                 json=setup.json,
                 headers=setup.headers,
                 timeout=timeout,
                 proxy=setup.proxy,
             ) as response:
                 return Response(
                     response.status,
                     headers=response.headers.copy(),
                     content=await response.read(),
                     request=setup,
                 )
 
-    @overrides(ForwardMixin)
+    @override
     @asynccontextmanager
     async def websocket(self, setup: Request) -> AsyncGenerator["WebSocket", None]:
         if setup.version == HTTPVersion.H10:
             version = aiohttp.HttpVersion10
         elif setup.version == HTTPVersion.H11:
             version = aiohttp.HttpVersion11
         else:
@@ -111,64 +113,64 @@
         websocket: aiohttp.ClientWebSocketResponse,
     ):
         super().__init__(request=request)
         self.session = session
         self.websocket = websocket
 
     @property
-    @overrides(BaseWebSocket)
+    @override
     def closed(self):
         return self.websocket.closed
 
-    @overrides(BaseWebSocket)
+    @override
     async def accept(self):
         raise NotImplementedError
 
-    @overrides(BaseWebSocket)
+    @override
     async def close(self, code: int = 1000):
         await self.websocket.close(code=code)
         await self.session.close()
 
     async def _receive(self) -> aiohttp.WSMessage:
         msg = await self.websocket.receive()
         if msg.type in (aiohttp.WSMsgType.CLOSE, aiohttp.WSMsgType.CLOSING):
             raise WebSocketClosed(self.websocket.close_code or 1006)
         return msg
 
-    @overrides(BaseWebSocket)
+    @override
     async def receive(self) -> str:
         msg = await self._receive()
         if msg.type not in (aiohttp.WSMsgType.TEXT, aiohttp.WSMsgType.BINARY):
             raise TypeError(
                 f"WebSocket received unexpected frame type: {msg.type}, {msg.data!r}"
             )
         return msg.data
 
-    @overrides(BaseWebSocket)
+    @override
     async def receive_text(self) -> str:
         msg = await self._receive()
         if msg.type != aiohttp.WSMsgType.TEXT:
             raise TypeError(
                 f"WebSocket received unexpected frame type: {msg.type}, {msg.data!r}"
             )
         return msg.data
 
-    @overrides(BaseWebSocket)
+    @override
     async def receive_bytes(self) -> bytes:
         msg = await self._receive()
         if msg.type != aiohttp.WSMsgType.BINARY:
             raise TypeError(
                 f"WebSocket received unexpected frame type: {msg.type}, {msg.data!r}"
             )
         return msg.data
 
-    @overrides(BaseWebSocket)
+    @override
     async def send_text(self, data: str) -> None:
         await self.websocket.send_str(data)
 
-    @overrides(BaseWebSocket)
+    @override
     async def send_bytes(self, data: bytes) -> None:
         await self.websocket.send_bytes(data)
 
 
 Driver: Type[ForwardDriver] = combine_driver(NoneDriver, Mixin)  # type: ignore
 """AIOHTTP Driver"""
```

### Comparing `nonebot2-2.0.0rc4/nonebot/drivers/fastapi.py` & `nonebot2-2.0.1/nonebot/drivers/fastapi.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,20 +15,20 @@
     description: nonebot.drivers.fastapi 模块
 """
 
 
 import logging
 import contextlib
 from functools import wraps
+from typing_extensions import override
 from typing import Any, Dict, List, Tuple, Union, Optional
 
 from pydantic import BaseSettings
 
 from nonebot.config import Env
-from nonebot.typing import overrides
 from nonebot.exception import WebSocketClosed
 from nonebot.internal.driver import FileTypes
 from nonebot.config import Config as NoneBotConfig
 from nonebot.drivers import Request as BaseRequest
 from nonebot.drivers import WebSocket as BaseWebSocket
 from nonebot.drivers import ReverseDriver, HTTPServerSetup, WebSocketServerSetup
 
@@ -37,15 +37,16 @@
 try:
     import uvicorn
     from fastapi.responses import Response
     from fastapi import FastAPI, Request, UploadFile, status
     from starlette.websockets import WebSocket, WebSocketState, WebSocketDisconnect
 except ModuleNotFoundError as e:  # pragma: no cover
     raise ImportError(
-        "Please install FastAPI by using `pip install nonebot2[fastapi]`"
+        "Please install FastAPI first to use this driver. "
+        "Install with pip: `pip install nonebot2[fastapi]`"
     ) from e
 
 
 def catch_closed(func):
     @wraps(func)
     async def decorator(*args, **kwargs):
         try:
@@ -86,93 +87,93 @@
         extra = "ignore"
 
 
 class Driver(ReverseDriver):
     """FastAPI 驱动框架。"""
 
     def __init__(self, env: Env, config: NoneBotConfig):
-        super(Driver, self).__init__(env, config)
+        super().__init__(env, config)
 
         self.fastapi_config: Config = Config(**config.dict())
 
         self._lifespan = Lifespan()
 
         self._server_app = FastAPI(
             lifespan=self._lifespan_manager,
             openapi_url=self.fastapi_config.fastapi_openapi_url,
             docs_url=self.fastapi_config.fastapi_docs_url,
             redoc_url=self.fastapi_config.fastapi_redoc_url,
             **self.fastapi_config.fastapi_extra,
         )
 
     @property
-    @overrides(ReverseDriver)
+    @override
     def type(self) -> str:
         """驱动名称: `fastapi`"""
         return "fastapi"
 
     @property
-    @overrides(ReverseDriver)
+    @override
     def server_app(self) -> FastAPI:
         """`FastAPI APP` 对象"""
         return self._server_app
 
     @property
-    @overrides(ReverseDriver)
+    @override
     def asgi(self) -> FastAPI:
         """`FastAPI APP` 对象"""
         return self._server_app
 
     @property
-    @overrides(ReverseDriver)
+    @override
     def logger(self) -> logging.Logger:
         """fastapi 使用的 logger"""
         return logging.getLogger("fastapi")
 
-    @overrides(ReverseDriver)
+    @override
     def setup_http_server(self, setup: HTTPServerSetup):
         async def _handle(request: Request) -> Response:
             return await self._handle_http(request, setup)
 
         self._server_app.add_api_route(
             setup.path.path,
             _handle,
             name=setup.name,
             methods=[setup.method],
             include_in_schema=self.fastapi_config.fastapi_include_adapter_schema,
         )
 
-    @overrides(ReverseDriver)
+    @override
     def setup_websocket_server(self, setup: WebSocketServerSetup) -> None:
         async def _handle(websocket: WebSocket) -> None:
             await self._handle_ws(websocket, setup)
 
         self._server_app.add_api_websocket_route(
             setup.path.path,
             _handle,
             name=setup.name,
         )
 
-    @overrides(ReverseDriver)
+    @override
     def on_startup(self, func: LIFESPAN_FUNC) -> LIFESPAN_FUNC:
         return self._lifespan.on_startup(func)
 
-    @overrides(ReverseDriver)
+    @override
     def on_shutdown(self, func: LIFESPAN_FUNC) -> LIFESPAN_FUNC:
         return self._lifespan.on_shutdown(func)
 
     @contextlib.asynccontextmanager
     async def _lifespan_manager(self, app: FastAPI):
         await self._lifespan.startup()
         try:
             yield
         finally:
             await self._lifespan.shutdown()
 
-    @overrides(ReverseDriver)
+    @override
     def run(
         self,
         host: Optional[str] = None,
         port: Optional[int] = None,
         *,
         app: Optional[str] = None,
         **kwargs,
@@ -263,58 +264,58 @@
 
         await setup.handle_func(ws)
 
 
 class FastAPIWebSocket(BaseWebSocket):
     """FastAPI WebSocket Wrapper"""
 
-    @overrides(BaseWebSocket)
+    @override
     def __init__(self, *, request: BaseRequest, websocket: WebSocket):
         super().__init__(request=request)
         self.websocket = websocket
 
     @property
-    @overrides(BaseWebSocket)
+    @override
     def closed(self) -> bool:
         return (
             self.websocket.client_state == WebSocketState.DISCONNECTED
             or self.websocket.application_state == WebSocketState.DISCONNECTED
         )
 
-    @overrides(BaseWebSocket)
+    @override
     async def accept(self) -> None:
         await self.websocket.accept()
 
-    @overrides(BaseWebSocket)
+    @override
     async def close(
         self, code: int = status.WS_1000_NORMAL_CLOSURE, reason: str = ""
     ) -> None:
         await self.websocket.close(code, reason)
 
-    @overrides(BaseWebSocket)
+    @override
     async def receive(self) -> Union[str, bytes]:
         # assert self.websocket.application_state == WebSocketState.CONNECTED
         msg = await self.websocket.receive()
         if msg["type"] == "websocket.disconnect":
             raise WebSocketClosed(msg["code"])
         return msg["text"] if "text" in msg else msg["bytes"]
 
-    @overrides(BaseWebSocket)
+    @override
     @catch_closed
     async def receive_text(self) -> str:
         return await self.websocket.receive_text()
 
-    @overrides(BaseWebSocket)
+    @override
     @catch_closed
     async def receive_bytes(self) -> bytes:
         return await self.websocket.receive_bytes()
 
-    @overrides(BaseWebSocket)
+    @override
     async def send_text(self, data: str) -> None:
         await self.websocket.send({"type": "websocket.send", "text": data})
 
-    @overrides(BaseWebSocket)
+    @override
     async def send_bytes(self, data: bytes) -> None:
         await self.websocket.send({"type": "websocket.send", "bytes": data})
 
 
 __autodoc__ = {"catch_closed": False}
```

### Comparing `nonebot2-2.0.0rc4/nonebot/drivers/httpx.py` & `nonebot2-2.0.1/nonebot/drivers/httpx.py`

 * *Files 8% similar despite different names*

```diff
@@ -10,18 +10,19 @@
 本驱动仅支持客户端 HTTP 连接
 :::
 
 FrontMatter:
     sidebar_position: 3
     description: nonebot.drivers.httpx 模块
 """
+
+from typing_extensions import override
 from typing import Type, AsyncGenerator
 from contextlib import asynccontextmanager
 
-from nonebot.typing import overrides
 from nonebot.drivers.none import Driver as NoneDriver
 from nonebot.drivers import (
     Request,
     Response,
     WebSocket,
     HTTPVersion,
     ForwardMixin,
@@ -29,27 +30,28 @@
     combine_driver,
 )
 
 try:
     import httpx
 except ModuleNotFoundError as e:  # pragma: no cover
     raise ImportError(
-        "Please install httpx by using `pip install nonebot2[httpx]`"
+        "Please install httpx first to use this driver. "
+        "Install with pip: `pip install nonebot2[httpx]`"
     ) from e
 
 
 class Mixin(ForwardMixin):
     """HTTPX Mixin"""
 
     @property
-    @overrides(ForwardMixin)
+    @override
     def type(self) -> str:
         return "httpx"
 
-    @overrides(ForwardMixin)
+    @override
     async def request(self, setup: Request) -> Response:
         async with httpx.AsyncClient(
             cookies=setup.cookies.jar,
             http2=setup.version == HTTPVersion.H2,
             proxies=setup.proxy,
             follow_redirects=True,
         ) as client:
@@ -66,15 +68,15 @@
             return Response(
                 response.status_code,
                 headers=response.headers.multi_items(),
                 content=response.content,
                 request=setup,
             )
 
-    @overrides(ForwardMixin)
+    @override
     @asynccontextmanager
     async def websocket(self, setup: Request) -> AsyncGenerator[WebSocket, None]:
         async with super(Mixin, self).websocket(setup) as ws:
             yield ws
 
 
 Driver: Type[ForwardDriver] = combine_driver(NoneDriver, Mixin)  # type: ignore
```

### Comparing `nonebot2-2.0.0rc4/nonebot/drivers/none.py` & `nonebot2-2.0.1/nonebot/drivers/none.py`

 * *Files 5% similar despite different names*

```diff
@@ -5,22 +5,21 @@
 :::
 
 FrontMatter:
     sidebar_position: 6
     description: nonebot.drivers.none 模块
 """
 
-
 import signal
 import asyncio
 import threading
+from typing_extensions import override
 
 from nonebot.log import logger
 from nonebot.consts import WINDOWS
-from nonebot.typing import overrides
 from nonebot.config import Env, Config
 from nonebot.drivers import Driver as BaseDriver
 
 from ._lifespan import LIFESPAN_FUNC, Lifespan
 
 HANDLED_SIGNALS = (
     signal.SIGINT,  # Unix signal 2. Sent by Ctrl+C.
@@ -38,40 +37,36 @@
 
         self._lifespan = Lifespan()
 
         self.should_exit: asyncio.Event = asyncio.Event()
         self.force_exit: bool = False
 
     @property
-    @overrides(BaseDriver)
+    @override
     def type(self) -> str:
         """驱动名称: `none`"""
         return "none"
 
     @property
-    @overrides(BaseDriver)
+    @override
     def logger(self):
         """none driver 使用的 logger"""
         return logger
 
-    @overrides(BaseDriver)
+    @override
     def on_startup(self, func: LIFESPAN_FUNC) -> LIFESPAN_FUNC:
-        """
-        注册一个启动时执行的函数
-        """
+        """注册一个启动时执行的函数"""
         return self._lifespan.on_startup(func)
 
-    @overrides(BaseDriver)
+    @override
     def on_shutdown(self, func: LIFESPAN_FUNC) -> LIFESPAN_FUNC:
-        """
-        注册一个停止时执行的函数
-        """
+        """注册一个停止时执行的函数"""
         return self._lifespan.on_shutdown(func)
 
-    @overrides(BaseDriver)
+    @override
     def run(self, *args, **kwargs):
         """启动 none driver"""
         super().run(*args, **kwargs)
         loop = asyncio.get_event_loop()
         loop.run_until_complete(self._serve())
 
     async def _serve(self):
@@ -142,11 +137,19 @@
                 loop.add_signal_handler(sig, self._handle_exit, sig, None)
         except NotImplementedError:
             # Windows
             for sig in HANDLED_SIGNALS:
                 signal.signal(sig, self._handle_exit)
 
     def _handle_exit(self, sig, frame):
-        if self.should_exit.is_set():
-            self.force_exit = True
-        else:
+        self.exit(force=self.should_exit.is_set())
+
+    def exit(self, force: bool = False):
+        """退出 none driver
+
+        参数:
+            force: 强制退出
+        """
+        if not self.should_exit.is_set():
             self.should_exit.set()
+        if force:
+            self.force_exit = True
```

### Comparing `nonebot2-2.0.0rc4/nonebot/drivers/quart.py` & `nonebot2-2.0.1/nonebot/drivers/quart.py`

 * *Files 15% similar despite different names*

```diff
@@ -13,37 +13,50 @@
 FrontMatter:
     sidebar_position: 5
     description: nonebot.drivers.quart 模块
 """
 
 import asyncio
 from functools import wraps
-from typing import Any, Dict, List, Tuple, Union, TypeVar, Callable, Optional, Coroutine
+from typing_extensions import override
+from typing import (
+    Any,
+    Dict,
+    List,
+    Tuple,
+    Union,
+    TypeVar,
+    Callable,
+    Optional,
+    Coroutine,
+    cast,
+)
 
 from pydantic import BaseSettings
 
 from nonebot.config import Env
-from nonebot.typing import overrides
 from nonebot.exception import WebSocketClosed
 from nonebot.internal.driver import FileTypes
 from nonebot.config import Config as NoneBotConfig
 from nonebot.drivers import Request as BaseRequest
 from nonebot.drivers import WebSocket as BaseWebSocket
 from nonebot.drivers import ReverseDriver, HTTPServerSetup, WebSocketServerSetup
 
 try:
     import uvicorn
     from quart import request as _request
-    from quart import websocket as _websocket
+    from quart.ctx import WebsocketContext
+    from quart.globals import websocket_ctx
     from quart import Quart, Request, Response
     from quart.datastructures import FileStorage
     from quart import Websocket as QuartWebSocket
 except ModuleNotFoundError as e:  # pragma: no cover
     raise ImportError(
-        "Please install Quart by using `pip install nonebot2[quart]`"
+        "Please install Quart first to use this driver. "
+        "Install with pip: `pip install nonebot2[quart]`"
     ) from e
 
 _AsyncCallable = TypeVar("_AsyncCallable", bound=Callable[..., Coroutine])
 
 
 def catch_closed(func):
     @wraps(func)
@@ -85,71 +98,71 @@
         self.quart_config = Config(**config.dict())
 
         self._server_app = Quart(
             self.__class__.__qualname__, **self.quart_config.quart_extra
         )
 
     @property
-    @overrides(ReverseDriver)
+    @override
     def type(self) -> str:
         """驱动名称: `quart`"""
         return "quart"
 
     @property
-    @overrides(ReverseDriver)
+    @override
     def server_app(self) -> Quart:
         """`Quart` 对象"""
         return self._server_app
 
     @property
-    @overrides(ReverseDriver)
+    @override
     def asgi(self):
         """`Quart` 对象"""
         return self._server_app
 
     @property
-    @overrides(ReverseDriver)
+    @override
     def logger(self):
         """Quart 使用的 logger"""
         return self._server_app.logger
 
-    @overrides(ReverseDriver)
+    @override
     def setup_http_server(self, setup: HTTPServerSetup):
         async def _handle() -> Response:
             return await self._handle_http(setup)
 
         self._server_app.add_url_rule(
             setup.path.path,
             endpoint=setup.name,
             methods=[setup.method],
             view_func=_handle,
         )
 
-    @overrides(ReverseDriver)
+    @override
     def setup_websocket_server(self, setup: WebSocketServerSetup) -> None:
         async def _handle() -> None:
             return await self._handle_ws(setup)
 
         self._server_app.add_websocket(
             setup.path.path,
             endpoint=setup.name,
             view_func=_handle,
         )
 
-    @overrides(ReverseDriver)
+    @override
     def on_startup(self, func: _AsyncCallable) -> _AsyncCallable:
         """参考文档: [`Startup and Shutdown`](https://pgjones.gitlab.io/quart/how_to_guides/startup_shutdown.html)"""
         return self.server_app.before_serving(func)  # type: ignore
 
-    @overrides(ReverseDriver)
+    @override
     def on_shutdown(self, func: _AsyncCallable) -> _AsyncCallable:
         """参考文档: [`Startup and Shutdown`](https://pgjones.gitlab.io/quart/how_to_guides/startup_shutdown.html)"""
         return self.server_app.after_serving(func)  # type: ignore
 
-    @overrides(ReverseDriver)
+    @override
     def run(
         self,
         host: Optional[str] = None,
         port: Optional[int] = None,
         *,
         app: Optional[str] = None,
         **kwargs,
@@ -184,17 +197,15 @@
             log_config=LOGGING_CONFIG,
             **kwargs,
         )
 
     async def _handle_http(self, setup: HTTPServerSetup) -> Response:
         request: Request = _request
 
-        json = None
-        if request.is_json:
-            json = await request.get_json()
+        json = await request.get_json() if request.is_json else None
 
         data = await request.form
         files_dict = await request.files
         files: List[Tuple[str, FileTypes]] = []
         key: str
         value: FileStorage
         for key, value in files_dict.items():
@@ -219,74 +230,79 @@
         return Response(
             response.content or "",
             response.status_code or 200,
             headers=dict(response.headers),
         )
 
     async def _handle_ws(self, setup: WebSocketServerSetup) -> None:
-        websocket: QuartWebSocket = _websocket
+        ctx = cast(WebsocketContext, websocket_ctx.copy())
+        websocket = websocket_ctx.websocket
 
         http_request = BaseRequest(
             websocket.method,
             websocket.url,
             headers=list(websocket.headers.items()),
             cookies=list(websocket.cookies.items()),
             version=websocket.http_version,
         )
 
-        ws = WebSocket(request=http_request, websocket=websocket)
+        ws = WebSocket(request=http_request, websocket_ctx=ctx)
 
         await setup.handle_func(ws)
 
 
 class WebSocket(BaseWebSocket):
     """Quart WebSocket Wrapper"""
 
-    def __init__(self, *, request: BaseRequest, websocket: QuartWebSocket):
+    def __init__(self, *, request: BaseRequest, websocket_ctx: WebsocketContext):
         super().__init__(request=request)
-        self.websocket = websocket
+        self.websocket_ctx = websocket_ctx
 
     @property
-    @overrides(BaseWebSocket)
+    def websocket(self) -> QuartWebSocket:
+        return self.websocket_ctx.websocket
+
+    @property
+    @override
     def closed(self):
         # FIXME
         return True
 
-    @overrides(BaseWebSocket)
+    @override
     async def accept(self):
         await self.websocket.accept()
 
-    @overrides(BaseWebSocket)
+    @override
     async def close(self, code: int = 1000, reason: str = ""):
         await self.websocket.close(code, reason)
 
-    @overrides(BaseWebSocket)
+    @override
     @catch_closed
     async def receive(self) -> Union[str, bytes]:
         return await self.websocket.receive()
 
-    @overrides(BaseWebSocket)
+    @override
     @catch_closed
     async def receive_text(self) -> str:
         msg = await self.websocket.receive()
         if isinstance(msg, bytes):
             raise TypeError("WebSocket received unexpected frame type: bytes")
         return msg
 
-    @overrides(BaseWebSocket)
+    @override
     @catch_closed
     async def receive_bytes(self) -> bytes:
         msg = await self.websocket.receive()
         if isinstance(msg, str):
             raise TypeError("WebSocket received unexpected frame type: str")
         return msg
 
-    @overrides(BaseWebSocket)
+    @override
     async def send_text(self, data: str):
         await self.websocket.send(data)
 
-    @overrides(BaseWebSocket)
+    @override
     async def send_bytes(self, data: bytes):
         await self.websocket.send(data)
 
 
 __autodoc__ = {"catch_closed": False}
```

### Comparing `nonebot2-2.0.0rc4/nonebot/drivers/websockets.py` & `nonebot2-2.0.1/nonebot/drivers/websockets.py`

 * *Files 20% similar despite different names*

```diff
@@ -10,42 +10,47 @@
 本驱动仅支持客户端 WebSocket 连接
 :::
 
 FrontMatter:
     sidebar_position: 4
     description: nonebot.drivers.websockets 模块
 """
+
 import logging
 from functools import wraps
 from contextlib import asynccontextmanager
-from typing import Type, Union, AsyncGenerator
+from typing_extensions import ParamSpec, override
+from typing import Type, Union, TypeVar, Callable, Awaitable, AsyncGenerator
 
-from nonebot.typing import overrides
 from nonebot.log import LoguruHandler
 from nonebot.drivers import Request, Response
 from nonebot.exception import WebSocketClosed
 from nonebot.drivers.none import Driver as NoneDriver
 from nonebot.drivers import WebSocket as BaseWebSocket
 from nonebot.drivers import ForwardMixin, ForwardDriver, combine_driver
 
 try:
     from websockets.exceptions import ConnectionClosed
     from websockets.legacy.client import Connect, WebSocketClientProtocol
 except ModuleNotFoundError as e:  # pragma: no cover
     raise ImportError(
-        "Please install websockets by using `pip install nonebot2[websockets]`"
+        "Please install websockets first to use this driver. "
+        "Install with pip: `pip install nonebot2[websockets]`"
     ) from e
 
+T = TypeVar("T")
+P = ParamSpec("P")
+
 logger = logging.Logger("websockets.client", "INFO")
 logger.addHandler(LoguruHandler())
 
 
-def catch_closed(func):
+def catch_closed(func: Callable[P, Awaitable[T]]) -> Callable[P, Awaitable[T]]:
     @wraps(func)
-    async def decorator(*args, **kwargs):
+    async def decorator(*args: P.args, **kwargs: P.kwargs) -> T:
         try:
             return await func(*args, **kwargs)
         except ConnectionClosed as e:
             if e.rcvd_then_sent:
                 raise WebSocketClosed(e.rcvd.code, e.rcvd.reason)  # type: ignore
             else:
                 raise WebSocketClosed(e.sent.code, e.sent.reason)  # type: ignore
@@ -53,80 +58,80 @@
     return decorator
 
 
 class Mixin(ForwardMixin):
     """Websockets Mixin"""
 
     @property
-    @overrides(ForwardMixin)
+    @override
     def type(self) -> str:
         return "websockets"
 
-    @overrides(ForwardMixin)
+    @override
     async def request(self, setup: Request) -> Response:
         return await super(Mixin, self).request(setup)
 
-    @overrides(ForwardMixin)
+    @override
     @asynccontextmanager
     async def websocket(self, setup: Request) -> AsyncGenerator["WebSocket", None]:
         connection = Connect(
             str(setup.url),
             extra_headers={**setup.headers, **setup.cookies.as_header(setup)},
             open_timeout=setup.timeout,
         )
         async with connection as ws:
             yield WebSocket(request=setup, websocket=ws)
 
 
 class WebSocket(BaseWebSocket):
     """Websockets WebSocket Wrapper"""
 
-    @overrides(BaseWebSocket)
+    @override
     def __init__(self, *, request: Request, websocket: WebSocketClientProtocol):
         super().__init__(request=request)
         self.websocket = websocket
 
     @property
-    @overrides(BaseWebSocket)
+    @override
     def closed(self) -> bool:
         return self.websocket.closed
 
-    @overrides(BaseWebSocket)
+    @override
     async def accept(self):
         raise NotImplementedError
 
-    @overrides(BaseWebSocket)
+    @override
     async def close(self, code: int = 1000, reason: str = ""):
         await self.websocket.close(code, reason)
 
-    @overrides(BaseWebSocket)
+    @override
     @catch_closed
     async def receive(self) -> Union[str, bytes]:
         return await self.websocket.recv()
 
-    @overrides(BaseWebSocket)
+    @override
     @catch_closed
     async def receive_text(self) -> str:
         msg = await self.websocket.recv()
         if isinstance(msg, bytes):
             raise TypeError("WebSocket received unexpected frame type: bytes")
         return msg
 
-    @overrides(BaseWebSocket)
+    @override
     @catch_closed
     async def receive_bytes(self) -> bytes:
         msg = await self.websocket.recv()
         if isinstance(msg, str):
             raise TypeError("WebSocket received unexpected frame type: str")
         return msg
 
-    @overrides(BaseWebSocket)
+    @override
     async def send_text(self, data: str) -> None:
         await self.websocket.send(data)
 
-    @overrides(BaseWebSocket)
+    @override
     async def send_bytes(self, data: bytes) -> None:
         await self.websocket.send(data)
 
 
 Driver: Type[ForwardDriver] = combine_driver(NoneDriver, Mixin)  # type: ignore
 """Websockets Driver"""
```

### Comparing `nonebot2-2.0.0rc4/nonebot/exception.py` & `nonebot2-2.0.1/nonebot/exception.py`

 * *Files 6% similar despite different names*

```diff
@@ -39,17 +39,17 @@
 
     def __str__(self) -> str:
         return self.__repr__()
 
 
 # Rule Exception
 class ParserExit(NoneBotException):
-    """{ref}`nonebot.rule.shell_command` 处理消息失败时返回的异常"""
+    """{ref}`nonebot.rule.shell_command` 处理消息失败时返回的异常。"""
 
-    def __init__(self, status: int = 0, message: Optional[str] = None):
+    def __init__(self, status: int = 0, message: Optional[str] = None) -> None:
         self.status = status
         self.message = message
 
     def __repr__(self) -> str:
         return (
             f"ParserExit(status={self.status}"
             + (f", message={self.message!r}" if self.message else "")
@@ -65,15 +65,15 @@
 class IgnoredException(ProcessException):
     """指示 NoneBot 应该忽略该事件。可由 PreProcessor 抛出。
 
     参数:
         reason: 忽略事件的原因
     """
 
-    def __init__(self, reason: Any):
+    def __init__(self, reason: Any) -> None:
         self.reason: Any = reason
 
     def __repr__(self) -> str:
         return f"IgnoredException(reason={self.reason!r})"
 
 
 class SkippedException(ProcessException):
@@ -92,27 +92,28 @@
         ```
     """
 
 
 class TypeMisMatch(SkippedException):
     """当前 `Handler` 的参数类型不匹配。"""
 
-    def __init__(self, param: ModelField, value: Any):
+    def __init__(self, param: ModelField, value: Any) -> None:
         self.param: ModelField = param
         self.value: Any = value
 
     def __repr__(self) -> str:
         return (
             f"TypeMisMatch(param={self.param.name}, "
             f"type={self.param._type_display()}, value={self.value!r}>"
         )
 
 
 class MockApiException(ProcessException):
-    """指示 NoneBot 阻止本次 API 调用或修改本次调用返回值，并返回自定义内容。可由 api hook 抛出。
+    """指示 NoneBot 阻止本次 API 调用或修改本次调用返回值，并返回自定义内容。
+    可由 api hook 抛出。
 
     参数:
         result: 返回的内容
     """
 
     def __init__(self, result: Any):
         self.result = result
@@ -140,29 +141,31 @@
 
 # Matcher Exceptions
 class MatcherException(NoneBotException):
     """所有 Matcher 发生的异常基类。"""
 
 
 class PausedException(MatcherException):
-    """指示 NoneBot 结束当前 `Handler` 并等待下一条消息后继续下一个 `Handler`。可用于用户输入新信息。
+    """指示 NoneBot 结束当前 `Handler` 并等待下一条消息后继续下一个 `Handler`。
+    可用于用户输入新信息。
 
     可以在 `Handler` 中通过 {ref}`nonebot.matcher.Matcher.pause` 抛出。
 
     用法:
         ```python
         @matcher.handle()
         async def handler():
             await matcher.pause("some message")
         ```
     """
 
 
 class RejectedException(MatcherException):
-    """指示 NoneBot 结束当前 `Handler` 并等待下一条消息后重新运行当前 `Handler`。可用于用户重新输入。
+    """指示 NoneBot 结束当前 `Handler` 并等待下一条消息后重新运行当前 `Handler`。
+    可用于用户重新输入。
 
     可以在 `Handler` 中通过 {ref}`nonebot.matcher.Matcher.reject` 抛出。
 
     用法:
         ```python
         @matcher.handle()
         async def handler():
@@ -183,15 +186,15 @@
             await matcher.finish("some message")
         ```
     """
 
 
 # Adapter Exceptions
 class AdapterException(NoneBotException):
-    """代表 `Adapter` 抛出的异常，所有的 `Adapter` 都要在内部继承自这个 `Exception`
+    """代表 `Adapter` 抛出的异常，所有的 `Adapter` 都要在内部继承自这个 `Exception`。
 
     参数:
         adapter_name: 标识 adapter
     """
 
     def __init__(self, adapter_name: str, *args: object) -> None:
         super().__init__(*args)
@@ -206,30 +209,32 @@
 
 
 class ApiNotAvailable(AdapterException):
     """在 API 连接不可用时抛出。"""
 
 
 class NetworkError(AdapterException):
-    """在网络出现问题时抛出，如: API 请求地址不正确, API 请求无返回或返回状态非正常等。"""
+    """在网络出现问题时抛出，
+    如: API 请求地址不正确, API 请求无返回或返回状态非正常等。
+    """
 
 
 class ActionFailed(AdapterException):
     """API 请求成功返回数据，但 API 操作失败。"""
 
 
 # Driver Exceptions
 class DriverException(NoneBotException):
-    """`Driver` 抛出的异常基类"""
+    """`Driver` 抛出的异常基类。"""
 
 
 class WebSocketClosed(DriverException):
-    """WebSocket 连接已关闭"""
+    """WebSocket 连接已关闭。"""
 
-    def __init__(self, code: int, reason: Optional[str] = None):
+    def __init__(self, code: int, reason: Optional[str] = None) -> None:
         self.code = code
         self.reason = reason
 
     def __repr__(self) -> str:
         return (
             f"WebSocketClosed(code={self.code}"
             + (f", reason={self.reason!r}" if self.reason else "")
```

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/adapter/adapter.py` & `nonebot2-2.0.1/nonebot/internal/adapter/adapter.py`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/adapter/bot.py` & `nonebot2-2.0.1/nonebot/internal/adapter/bot.py`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/adapter/event.py` & `nonebot2-2.0.1/nonebot/internal/adapter/event.py`

 * *Files 2% similar despite different names*

```diff
@@ -40,29 +40,32 @@
 
     def __str__(self) -> str:
         return f"[{self.get_event_name()}]: {self.get_event_description()}"
 
     def get_log_string(self) -> str:
         """获取事件日志信息的方法。
 
-        通常你不需要修改这个方法，只有当希望 NoneBot 隐藏该事件日志时，可以抛出 `NoLogException` 异常。
+        通常你不需要修改这个方法，只有当希望 NoneBot 隐藏该事件日志时，
+        可以抛出 `NoLogException` 异常。
 
         异常:
-            NoLogException:
+            NoLogException: 希望 NoneBot 隐藏该事件日志
         """
         return f"[{self.get_event_name()}]: {self.get_event_description()}"
 
     @abc.abstractmethod
     def get_user_id(self) -> str:
         """获取事件主体 id 的方法，通常是用户 id 。"""
         raise NotImplementedError
 
     @abc.abstractmethod
     def get_session_id(self) -> str:
-        """获取会话 id 的方法，用于判断当前事件属于哪一个会话，通常是用户 id、群组 id 组合。"""
+        """获取会话 id 的方法，用于判断当前事件属于哪一个会话，
+        通常是用户 id、群组 id 组合。
+        """
         raise NotImplementedError
 
     @abc.abstractmethod
     def get_message(self) -> "Message":
         """获取事件消息内容的方法。"""
         raise NotImplementedError
```

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/adapter/message.py` & `nonebot2-2.0.1/nonebot/internal/adapter/message.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,29 +1,30 @@
 import abc
 from copy import deepcopy
+from typing_extensions import Self
 from dataclasses import field, asdict, dataclass
 from typing import (
     Any,
     Dict,
     List,
     Type,
     Tuple,
     Union,
     Generic,
     TypeVar,
     Iterable,
     Optional,
+    SupportsIndex,
     overload,
 )
 
 from pydantic import parse_obj_as
 
 from .template import MessageTemplate
 
-T = TypeVar("T")
 TMS = TypeVar("TMS", bound="MessageSegment")
 TM = TypeVar("TM", bound="Message")
 
 
 @dataclass
 class MessageSegment(abc.ABC, Generic[TM]):
     """消息段基类"""
@@ -43,29 +44,29 @@
     def __str__(self) -> str:
         """该消息段所代表的 str，在命令匹配部分使用"""
         raise NotImplementedError
 
     def __len__(self) -> int:
         return len(str(self))
 
-    def __ne__(self: T, other: T) -> bool:
+    def __ne__(self, other: Self) -> bool:
         return not self == other
 
     def __add__(self: TMS, other: Union[str, TMS, Iterable[TMS]]) -> TM:
         return self.get_message_class()(self) + other
 
     def __radd__(self: TMS, other: Union[str, TMS, Iterable[TMS]]) -> TM:
         return self.get_message_class()(other) + self
 
     @classmethod
     def __get_validators__(cls):
         yield cls._validate
 
     @classmethod
-    def _validate(cls, value):
+    def _validate(cls, value) -> Self:
         if isinstance(value, cls):
             return value
         if not isinstance(value, dict):
             raise ValueError(f"Expected dict for MessageSegment, got {type(value)}")
         if "type" not in value:
             raise ValueError(
                 f"Expected dict with 'type' for MessageSegment, got {value}"
@@ -80,25 +81,28 @@
 
     def values(self):
         return asdict(self).values()
 
     def items(self):
         return asdict(self).items()
 
-    def copy(self: T) -> T:
+    def join(self: TMS, iterable: Iterable[Union[TMS, TM]]) -> TM:
+        return self.get_message_class()(self).join(iterable)
+
+    def copy(self) -> Self:
         return deepcopy(self)
 
     @abc.abstractmethod
     def is_text(self) -> bool:
         """当前消息段是否为纯文本"""
         raise NotImplementedError
 
 
 class Message(List[TMS], abc.ABC):
-    """消息数组
+    """消息序列
 
     参数:
         message: 消息内容
     """
 
     def __init__(
         self,
@@ -113,20 +117,20 @@
             self.append(message)
         elif isinstance(message, Iterable):
             self.extend(message)
         else:
             self.extend(self._construct(message))  # pragma: no cover
 
     @classmethod
-    def template(cls: Type[TM], format_string: Union[str, TM]) -> MessageTemplate[TM]:
+    def template(cls, format_string: Union[str, TM]) -> MessageTemplate[Self]:
         """创建消息模板。
 
-        用法和 `str.format` 大致相同, 但是可以输出消息对象, 并且支持以 `Message` 对象作为消息模板
-
-        并且提供了拓展的格式化控制符, 可以用适用于该消息类型的 `MessageSegment` 的工厂方法创建消息
+        用法和 `str.format` 大致相同，支持以 `Message` 对象作为消息模板并输出消息对象。
+        并且提供了拓展的格式化控制符，
+        可以通过该消息类型的 `MessageSegment` 工厂方法创建消息。
 
         参数:
             format_string: 格式化模板
 
         返回:
             消息格式化器
         """
@@ -142,15 +146,15 @@
         return "".join(str(seg) for seg in self)
 
     @classmethod
     def __get_validators__(cls):
         yield cls._validate
 
     @classmethod
-    def _validate(cls, value):
+    def _validate(cls, value) -> Self:
         if isinstance(value, cls):
             return value
         elif isinstance(value, Message):
             raise ValueError(f"Type {type(value)} can not be converted to {cls}")
         elif isinstance(value, str):
             pass
         elif isinstance(value, dict):
@@ -165,165 +169,262 @@
 
     @staticmethod
     @abc.abstractmethod
     def _construct(msg: str) -> Iterable[TMS]:
         """构造消息数组"""
         raise NotImplementedError
 
-    def __add__(self: TM, other: Union[str, TMS, Iterable[TMS]]) -> TM:
+    def __add__(self, other: Union[str, TMS, Iterable[TMS]]) -> Self:
         result = self.copy()
         result += other
         return result
 
-    def __radd__(self: TM, other: Union[str, TMS, Iterable[TMS]]) -> TM:
+    def __radd__(self, other: Union[str, TMS, Iterable[TMS]]) -> Self:
         result = self.__class__(other)
         return result + self
 
-    def __iadd__(self: TM, other: Union[str, TMS, Iterable[TMS]]) -> TM:
+    def __iadd__(self, other: Union[str, TMS, Iterable[TMS]]) -> Self:
         if isinstance(other, str):
             self.extend(self._construct(other))
         elif isinstance(other, MessageSegment):
             self.append(other)
         elif isinstance(other, Iterable):
             self.extend(other)
         else:
             raise TypeError(f"Unsupported type {type(other)!r}")
         return self
 
     @overload
-    def __getitem__(self: TM, __args: str) -> TM:
-        """
+    def __getitem__(self, args: str) -> Self:
+        """获取仅包含指定消息段类型的消息
+
         参数:
-            __args: 消息段类型
+            args: 消息段类型
 
         返回:
-            所有类型为 `__args` 的消息段
+            所有类型为 `args` 的消息段
         """
 
     @overload
-    def __getitem__(self, __args: Tuple[str, int]) -> TMS:
-        """
+    def __getitem__(self, args: Tuple[str, int]) -> TMS:
+        """索引指定类型的消息段
+
         参数:
-            __args: 消息段类型和索引
+            args: 消息段类型和索引
 
         返回:
-            类型为 `__args[0]` 的消息段第 `__args[1]` 个
+            类型为 `args[0]` 的消息段第 `args[1]` 个
         """
 
     @overload
-    def __getitem__(self: TM, __args: Tuple[str, slice]) -> TM:
-        """
+    def __getitem__(self, args: Tuple[str, slice]) -> Self:
+        """切片指定类型的消息段
+
         参数:
-            __args: 消息段类型和切片
+            args: 消息段类型和切片
 
         返回:
-            类型为 `__args[0]` 的消息段切片 `__args[1]`
+            类型为 `args[0]` 的消息段切片 `args[1]`
         """
 
     @overload
-    def __getitem__(self, __args: int) -> TMS:
-        """
+    def __getitem__(self, args: int) -> TMS:
+        """索引消息段
+
         参数:
-            __args: 索引
+            args: 索引
 
         返回:
-            第 `__args` 个消息段
+            第 `args` 个消息段
         """
 
     @overload
-    def __getitem__(self: TM, __args: slice) -> TM:
-        """
+    def __getitem__(self, args: slice) -> Self:
+        """切片消息段
+
         参数:
-            __args: 切片
+            args: 切片
 
         返回:
-            消息切片 `__args`
+            消息切片 `args`
         """
 
     def __getitem__(
-        self: TM,
+        self,
         args: Union[
             str,
             Tuple[str, int],
             Tuple[str, slice],
             int,
             slice,
         ],
-    ) -> Union[TMS, TM]:
+    ) -> Union[TMS, Self]:
         arg1, arg2 = args if isinstance(args, tuple) else (args, None)
         if isinstance(arg1, int) and arg2 is None:
             return super().__getitem__(arg1)
         elif isinstance(arg1, slice) and arg2 is None:
             return self.__class__(super().__getitem__(arg1))
         elif isinstance(arg1, str) and arg2 is None:
             return self.__class__(seg for seg in self if seg.type == arg1)
         elif isinstance(arg1, str) and isinstance(arg2, int):
             return [seg for seg in self if seg.type == arg1][arg2]
         elif isinstance(arg1, str) and isinstance(arg2, slice):
             return self.__class__([seg for seg in self if seg.type == arg1][arg2])
         else:
             raise ValueError("Incorrect arguments to slice")  # pragma: no cover
 
-    def index(self, value: Union[TMS, str], *args) -> int:
+    def __contains__(self, value: Union[TMS, str]) -> bool:
+        """检查消息段是否存在
+
+        参数:
+            value: 消息段或消息段类型
+        返回:
+            消息内是否存在给定消息段或给定类型的消息段
+        """
+        if isinstance(value, str):
+            return bool(next((seg for seg in self if seg.type == value), None))
+        return super().__contains__(value)
+
+    def has(self, value: Union[TMS, str]) -> bool:
+        """与 {ref}``__contains__` <nonebot.adapters.Message.__contains__>` 相同"""
+        return value in self
+
+    def index(self, value: Union[TMS, str], *args: SupportsIndex) -> int:
+        """索引消息段
+
+        参数:
+            value: 消息段或者消息段类型
+            arg: start 与 end
+
+        返回:
+            索引 index
+
+        异常:
+            ValueError: 消息段不存在
+        """
         if isinstance(value, str):
             first_segment = next((seg for seg in self if seg.type == value), None)
             if first_segment is None:
-                raise ValueError(f"Segment with type {value} is not in message")
+                raise ValueError(f"Segment with type {value!r} is not in message")
             return super().index(first_segment, *args)
         return super().index(value, *args)
 
-    def get(self: TM, type_: str, count: Optional[int] = None) -> TM:
+    def get(self, type_: str, count: Optional[int] = None) -> Self:
+        """获取指定类型的消息段
+
+        参数:
+            type_: 消息段类型
+            count: 获取个数
+
+        返回:
+            构建的新消息
+        """
         if count is None:
             return self[type_]
 
         iterator, filtered = (
             seg for seg in self if seg.type == type_
         ), self.__class__()
         for _ in range(count):
             seg = next(iterator, None)
             if seg is None:
                 break
             filtered.append(seg)
         return filtered
 
     def count(self, value: Union[TMS, str]) -> int:
+        """计算指定消息段的个数
+
+        参数:
+            value: 消息段或消息段类型
+
+        返回:
+            个数
+        """
         return len(self[value]) if isinstance(value, str) else super().count(value)
 
-    def append(self: TM, obj: Union[str, TMS]) -> TM:
+    def only(self, value: Union[TMS, str]) -> bool:
+        """检查消息中是否仅包含指定消息段
+
+        参数:
+            value: 指定消息段或消息段类型
+
+        返回:
+            是否仅包含指定消息段
+        """
+        if isinstance(value, str):
+            return all(seg.type == value for seg in self)
+        return all(seg == value for seg in self)
+
+    def append(self, obj: Union[str, TMS]) -> Self:
         """添加一个消息段到消息数组末尾。
 
         参数:
             obj: 要添加的消息段
         """
         if isinstance(obj, MessageSegment):
             super().append(obj)
         elif isinstance(obj, str):
             self.extend(self._construct(obj))
         else:
             raise ValueError(f"Unexpected type: {type(obj)} {obj}")  # pragma: no cover
         return self
 
-    def extend(self: TM, obj: Union[TM, Iterable[TMS]]) -> TM:
+    def extend(self, obj: Union[Self, Iterable[TMS]]) -> Self:
         """拼接一个消息数组或多个消息段到消息数组末尾。
 
         参数:
             obj: 要添加的消息数组
         """
         for segment in obj:
             self.append(segment)
         return self
 
-    def copy(self: TM) -> TM:
+    def join(self, iterable: Iterable[Union[TMS, Self]]) -> Self:
+        """将多个消息连接并将自身作为分割
+
+        参数:
+            iterable: 要连接的消息
+
+        返回:
+            连接后的消息
+        """
+        ret = self.__class__()
+        for index, msg in enumerate(iterable):
+            if index != 0:
+                ret.extend(self)
+            if isinstance(msg, MessageSegment):
+                ret.append(msg.copy())
+            else:
+                ret.extend(msg.copy())
+        return ret
+
+    def copy(self) -> Self:
+        """深拷贝消息"""
         return deepcopy(self)
 
+    def include(self, *types: str) -> Self:
+        """过滤消息
+
+        参数:
+            types: 包含的消息段类型
+
+        返回:
+            新构造的消息
+        """
+        return self.__class__(seg for seg in self if seg.type in types)
+
+    def exclude(self, *types: str) -> Self:
+        """过滤消息
+
+        参数:
+            types: 不包含的消息段类型
+
+        返回:
+            新构造的消息
+        """
+        return self.__class__(seg for seg in self if seg.type not in types)
+
     def extract_plain_text(self) -> str:
         """提取消息内纯文本消息"""
 
         return "".join(str(seg) for seg in self if seg.is_text())
-
-
-__autodoc__ = {
-    "MessageSegment.__str__": True,
-    "MessageSegment.__add__": True,
-    "Message.__getitem__": True,
-    "Message._construct": True,
-}
```

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/adapter/template.py` & `nonebot2-2.0.1/nonebot/internal/adapter/template.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import functools
 from string import Formatter
+from typing_extensions import TypeAlias
 from typing import (
     TYPE_CHECKING,
     Any,
     Set,
     Dict,
     List,
     Type,
@@ -21,15 +22,15 @@
 
 if TYPE_CHECKING:
     from .message import Message, MessageSegment
 
 TM = TypeVar("TM", bound="Message")
 TF = TypeVar("TF", str, "Message")
 
-FormatSpecFunc = Callable[[Any], str]
+FormatSpecFunc: TypeAlias = Callable[[Any], str]
 FormatSpecFunc_T = TypeVar("FormatSpecFunc_T", bound=FormatSpecFunc)
 
 
 class MessageTemplate(Formatter, Generic[TF]):
     """消息模板格式化实现类。
 
     参数:
```

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/driver/__init__.py` & `nonebot2-2.0.1/nonebot/internal/driver/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/driver/driver.py` & `nonebot2-2.0.1/nonebot/internal/driver/driver.py`

 * *Files 2% similar despite different names*

```diff
@@ -85,17 +85,15 @@
     @abc.abstractmethod
     def logger(self):
         """驱动专属 logger 日志记录器"""
         raise NotImplementedError
 
     @abc.abstractmethod
     def run(self, *args, **kwargs):
-        """
-        启动驱动框架
-        """
+        """启动驱动框架"""
         logger.opt(colors=True).debug(
             f"<g>Loaded adapters: {escape_tag(', '.join(self._adapters))}</g>"
         )
 
     @abc.abstractmethod
     def on_startup(self, func: Callable) -> Callable:
         """注册一个在驱动器启动时执行的函数"""
@@ -148,16 +146,18 @@
                     )
                     for hook in self._bot_connection_hook
                 ]:
                     try:
                         await asyncio.gather(*coros)
                     except Exception as e:
                         logger.opt(colors=True, exception=e).error(
-                            "<r><bg #f8bbd0>Error when running WebSocketConnection hook. "
-                            "Running cancelled!</bg #f8bbd0></r>"
+                            "<r><bg #f8bbd0>"
+                            "Error when running WebSocketConnection hook. "
+                            "Running cancelled!"
+                            "</bg #f8bbd0></r>"
                         )
 
         asyncio.create_task(_run_hook(bot))
 
     def _bot_disconnect(self, bot: "Bot") -> None:
         """在连接断开后，调用该函数来注销 bot 对象"""
         if bot.self_id in self._bots:
@@ -173,16 +173,18 @@
                     )
                     for hook in self._bot_disconnection_hook
                 ]:
                     try:
                         await asyncio.gather(*coros)
                     except Exception as e:
                         logger.opt(colors=True, exception=e).error(
-                            "<r><bg #f8bbd0>Error when running WebSocketDisConnection hook. "
-                            "Running cancelled!</bg #f8bbd0></r>"
+                            "<r><bg #f8bbd0>"
+                            "Error when running WebSocketDisConnection hook. "
+                            "Running cancelled!"
+                            "</bg #f8bbd0></r>"
                         )
 
         asyncio.create_task(_run_hook(bot))
 
 
 class ForwardMixin(abc.ABC):
     """客户端混入基类。"""
@@ -237,21 +239,23 @@
 
 
 def combine_driver(driver: Type[Driver], *mixins: Type[ForwardMixin]) -> Type[Driver]:
     """将一个驱动器和多个混入类合并。"""
     # check first
     assert issubclass(driver, Driver), "`driver` must be subclass of Driver"
     assert all(
-        map(lambda m: issubclass(m, ForwardMixin), mixins)
+        issubclass(m, ForwardMixin) for m in mixins
     ), "`mixins` must be subclass of ForwardMixin"
 
     if not mixins:
         return driver
 
     def type_(self: ForwardDriver) -> str:
         return (
             driver.type.__get__(self)
             + "+"
-            + "+".join(map(lambda x: x.type.__get__(self), mixins))
+            + "+".join(x.type.__get__(self) for x in mixins)
         )
 
-    return type("CombinedDriver", (*mixins, driver, ForwardDriver), {"type": property(type_)})  # type: ignore
+    return type(
+        "CombinedDriver", (*mixins, driver, ForwardDriver), {"type": property(type_)}
+    )  # type: ignore
```

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/driver/model.py` & `nonebot2-2.0.1/nonebot/internal/driver/model.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import abc
 import urllib.request
 from enum import Enum
 from dataclasses import dataclass
+from typing_extensions import TypeAlias
 from http.cookiejar import Cookie, CookieJar
 from typing import (
     IO,
     Any,
     Dict,
     List,
     Tuple,
@@ -17,44 +18,46 @@
     Awaitable,
     MutableMapping,
 )
 
 from yarl import URL as URL
 from multidict import CIMultiDict
 
-RawURL = Tuple[bytes, bytes, Optional[int], bytes]
+RawURL: TypeAlias = Tuple[bytes, bytes, Optional[int], bytes]
 
-SimpleQuery = Union[str, int, float]
-QueryVariable = Union[SimpleQuery, List[SimpleQuery]]
-QueryTypes = Union[
+SimpleQuery: TypeAlias = Union[str, int, float]
+QueryVariable: TypeAlias = Union[SimpleQuery, List[SimpleQuery]]
+QueryTypes: TypeAlias = Union[
     None, str, Mapping[str, QueryVariable], List[Tuple[str, QueryVariable]]
 ]
 
-HeaderTypes = Union[
+HeaderTypes: TypeAlias = Union[
     None,
     CIMultiDict[str],
     Dict[str, str],
     List[Tuple[str, str]],
 ]
 
-CookieTypes = Union[None, "Cookies", CookieJar, Dict[str, str], List[Tuple[str, str]]]
+CookieTypes: TypeAlias = Union[
+    None, "Cookies", CookieJar, Dict[str, str], List[Tuple[str, str]]
+]
 
-ContentTypes = Union[str, bytes, None]
-DataTypes = Union[dict, None]
-FileContent = Union[IO[bytes], bytes]
-FileType = Tuple[Optional[str], FileContent, Optional[str]]
-FileTypes = Union[
+ContentTypes: TypeAlias = Union[str, bytes, None]
+DataTypes: TypeAlias = Union[dict, None]
+FileContent: TypeAlias = Union[IO[bytes], bytes]
+FileType: TypeAlias = Tuple[Optional[str], FileContent, Optional[str]]
+FileTypes: TypeAlias = Union[
     # file (or bytes)
     FileContent,
     # (filename, file (or bytes))
     Tuple[Optional[str], FileContent],
     # (filename, file (or bytes), content_type)
     FileType,
 ]
-FilesTypes = Union[Dict[str, FileTypes], List[Tuple[str, FileTypes]], None]
+FilesTypes: TypeAlias = Union[Dict[str, FileTypes], List[Tuple[str, FileTypes]], None]
 
 
 class HTTPVersion(Enum):
     H10 = "1.0"
     H11 = "1.1"
     H2 = "2"
 
@@ -156,26 +159,23 @@
 
     def __repr__(self) -> str:
         return f"{self.__class__.__name__}(status_code={self.status_code!r})"
 
 
 class WebSocket(abc.ABC):
     def __init__(self, *, request: Request):
-        # request
         self.request: Request = request
 
     def __repr__(self) -> str:
         return f"{self.__class__.__name__}('{self.request.url!s}')"
 
     @property
     @abc.abstractmethod
     def closed(self) -> bool:
-        """
-        连接是否已经关闭
-        """
+        """连接是否已经关闭"""
         raise NotImplementedError
 
     @abc.abstractmethod
     async def accept(self) -> None:
         """接受 WebSocket 连接请求"""
         raise NotImplementedError
```

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/matcher/manager.py` & `nonebot2-2.0.1/nonebot/internal/matcher/manager.py`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/matcher/matcher.py` & `nonebot2-2.0.1/nonebot/internal/matcher/matcher.py`

 * *Files 6% similar despite different names*

```diff
@@ -25,29 +25,28 @@
 from nonebot.internal.adapter import (
     Bot,
     Event,
     Message,
     MessageSegment,
     MessageTemplate,
 )
-from nonebot.consts import (
-    ARG_KEY,
-    RECEIVE_KEY,
-    REJECT_TARGET,
-    LAST_RECEIVE_KEY,
-    REJECT_CACHE_TARGET,
-)
 from nonebot.typing import (
-    Any,
     T_State,
     T_Handler,
     T_TypeUpdater,
     T_DependencyCache,
     T_PermissionUpdater,
 )
+from nonebot.consts import (
+    ARG_KEY,
+    RECEIVE_KEY,
+    REJECT_TARGET,
+    LAST_RECEIVE_KEY,
+    REJECT_CACHE_TARGET,
+)
 from nonebot.exception import (
     PausedException,
     StopPropagation,
     SkippedException,
     FinishedException,
     RejectedException,
 )
@@ -372,15 +371,15 @@
             if matcher.get_target() == RECEIVE_KEY.format(id=id):
                 matcher.set_receive(id, event)
                 return
             if matcher.get_receive(id, ...) is not ...:
                 return
             await matcher.reject()
 
-        _parameterless = (Depends(_receive), *(parameterless or tuple()))
+        _parameterless = (Depends(_receive), *(parameterless or ()))
 
         def _decorator(func: T_Handler) -> T_Handler:
             if cls.handlers and cls.handlers[-1].call is func:
                 func_handler = cls.handlers[-1]
                 new_handler = Dependent(
                     call=func_handler.call,
                     params=func_handler.params,
@@ -402,15 +401,16 @@
         cls,
         key: str,
         prompt: Optional[Union[str, Message, MessageSegment, MessageTemplate]] = None,
         parameterless: Optional[Iterable[Any]] = None,
     ) -> Callable[[T_Handler], T_Handler]:
         """装饰一个函数来指示 NoneBot 获取一个参数 `key`
 
-        当要获取的 `key` 不存在时接收用户新的一条消息再运行该函数，如果 `key` 已存在则直接继续运行
+        当要获取的 `key` 不存在时接收用户新的一条消息再运行该函数，
+        如果 `key` 已存在则直接继续运行
 
         参数:
             key: 参数名
             prompt: 在参数不存在时向用户发送的消息
             parameterless: 非参数类型依赖列表
         """
 
@@ -419,15 +419,15 @@
             if matcher.get_target() == ARG_KEY.format(key=key):
                 matcher.set_arg(key, event.get_message())
                 return
             if matcher.get_arg(key, ...) is not ...:
                 return
             await matcher.reject(prompt)
 
-        _parameterless = (Depends(_key_getter), *(parameterless or tuple()))
+        _parameterless = (Depends(_key_getter), *(parameterless or ()))
 
         def _decorator(func: T_Handler) -> T_Handler:
             if cls.handlers and cls.handlers[-1].call is func:
                 func_handler = cls.handlers[-1]
                 new_handler = Dependent(
                     call=func_handler.call,
                     params=func_handler.params,
@@ -450,15 +450,16 @@
         message: Union[str, Message, MessageSegment, MessageTemplate],
         **kwargs: Any,
     ) -> Any:
         """发送一条消息给当前交互用户
 
         参数:
             message: 消息内容
-            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，请参考对应 adapter 的 bot 对象 api
+            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，
+                请参考对应 adapter 的 bot 对象 api
         """
         bot = current_bot.get()
         event = current_event.get()
         state = current_matcher.get().state
         if isinstance(message, MessageTemplate):
             _message = message.format(**state)
         else:
@@ -471,15 +472,16 @@
         message: Optional[Union[str, Message, MessageSegment, MessageTemplate]] = None,
         **kwargs,
     ) -> NoReturn:
         """发送一条消息给当前交互用户并结束当前事件响应器
 
         参数:
             message: 消息内容
-            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，请参考对应 adapter 的 bot 对象 api
+            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，
+                请参考对应 adapter 的 bot 对象 api
         """
         if message is not None:
             await cls.send(message, **kwargs)
         raise FinishedException
 
     @classmethod
     async def pause(
@@ -487,15 +489,16 @@
         prompt: Optional[Union[str, Message, MessageSegment, MessageTemplate]] = None,
         **kwargs,
     ) -> NoReturn:
         """发送一条消息给当前交互用户并暂停事件响应器，在接收用户新的一条消息后继续下一个处理函数
 
         参数:
             prompt: 消息内容
-            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，请参考对应 adapter 的 bot 对象 api
+            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，
+                请参考对应 adapter 的 bot 对象 api
         """
         if prompt is not None:
             await cls.send(prompt, **kwargs)
         raise PausedException
 
     @classmethod
     async def reject(
@@ -504,15 +507,16 @@
         **kwargs,
     ) -> NoReturn:
         """最近使用 `got` / `receive` 接收的消息不符合预期，
         发送一条消息给当前交互用户并将当前事件处理流程中断在当前位置，在接收用户新的一个事件后从头开始执行当前处理函数
 
         参数:
             prompt: 消息内容
-            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，请参考对应 adapter 的 bot 对象 api
+            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，
+                请参考对应 adapter 的 bot 对象 api
         """
         if prompt is not None:
             await cls.send(prompt, **kwargs)
         raise RejectedException
 
     @classmethod
     async def reject_arg(
@@ -523,15 +527,16 @@
     ) -> NoReturn:
         """最近使用 `got` 接收的消息不符合预期，
         发送一条消息给当前交互用户并将当前事件处理流程中断在当前位置，在接收用户新的一条消息后从头开始执行当前处理函数
 
         参数:
             key: 参数名
             prompt: 消息内容
-            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，请参考对应 adapter 的 bot 对象 api
+            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，
+                请参考对应 adapter 的 bot 对象 api
         """
         matcher = current_matcher.get()
         matcher.set_target(ARG_KEY.format(key=key))
         if prompt is not None:
             await cls.send(prompt, **kwargs)
         raise RejectedException
 
@@ -544,15 +549,16 @@
     ) -> NoReturn:
         """最近使用 `receive` 接收的消息不符合预期，
         发送一条消息给当前交互用户并将当前事件处理流程中断在当前位置，在接收用户新的一个事件后从头开始执行当前处理函数
 
         参数:
             id: 消息 id
             prompt: 消息内容
-            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，请参考对应 adapter 的 bot 对象 api
+            kwargs: {ref}`nonebot.adapters.Bot.send` 的参数，
+                请参考对应 adapter 的 bot 对象 api
         """
         matcher = current_matcher.get()
         matcher.set_target(RECEIVE_KEY.format(id=id))
         if prompt is not None:
             await cls.send(prompt, **kwargs)
         raise RejectedException
```

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/matcher/provider.py` & `nonebot2-2.0.1/nonebot/internal/matcher/provider.py`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/params.py` & `nonebot2-2.0.1/nonebot/internal/params.py`

 * *Files 21% similar despite different names*

```diff
@@ -59,23 +59,31 @@
 
         def depend_gen_func():
             try:
                 yield ...
             finally:
                 ...
 
-        async def handler(param_name: Any = Depends(depend_func), gen: Any = Depends(depend_gen_func)):
+        async def handler(
+            param_name: Any = Depends(depend_func),
+            gen: Any = Depends(depend_gen_func),
+        ):
             ...
         ```
     """
     return DependsInner(dependency, use_cache=use_cache)
 
 
 class DependParam(Param):
-    """子依赖参数"""
+    """子依赖注入参数。
+
+    本注入解析所有子依赖注入，然后将它们的返回值作为参数值传递给父依赖。
+
+    本注入应该具有最高优先级，因此应该在其他参数之前检查。
+    """
 
     def __repr__(self) -> str:
         return f"Depends({self.extra['dependent']})"
 
     @classmethod
     def _check_param(
         cls, param: inspect.Parameter, allow_types: Tuple[Type[Param], ...]
@@ -164,15 +172,20 @@
     async def _check(self, **kwargs: Any) -> None:
         # run sub dependent pre-checkers
         sub_dependent: Dependent = self.extra["dependent"]
         await sub_dependent.check(**kwargs)
 
 
 class BotParam(Param):
-    """{ref}`nonebot.adapters.Bot` 参数"""
+    """{ref}`nonebot.adapters.Bot` 注入参数。
+
+    本注入解析所有类型为且仅为 {ref}`nonebot.adapters.Bot` 及其子类或 `None` 的参数。
+
+    为保证兼容性，本注入还会解析名为 `bot` 且没有类型注解的参数。
+    """
 
     def __repr__(self) -> str:
         return (
             "BotParam("
             + (
                 repr(cast(ModelField, checker).type_)
                 if (checker := self.extra.get("checker"))
@@ -183,40 +196,46 @@
 
     @classmethod
     def _check_param(
         cls, param: inspect.Parameter, allow_types: Tuple[Type[Param], ...]
     ) -> Optional["BotParam"]:
         from nonebot.adapters import Bot
 
-        if param.default == param.empty:
-            if generic_check_issubclass(param.annotation, Bot):
-                checker: Optional[ModelField] = None
-                if param.annotation is not Bot:
-                    checker = ModelField(
-                        name=param.name,
-                        type_=param.annotation,
-                        class_validators=None,
-                        model_config=CustomConfig,
-                        default=None,
-                        required=True,
-                    )
-                return cls(Required, checker=checker)
-            elif param.annotation == param.empty and param.name == "bot":
-                return cls(Required)
+        # param type is Bot(s) or subclass(es) of Bot or None
+        if generic_check_issubclass(param.annotation, Bot):
+            checker: Optional[ModelField] = None
+            if param.annotation is not Bot:
+                checker = ModelField(
+                    name=param.name,
+                    type_=param.annotation,
+                    class_validators=None,
+                    model_config=CustomConfig,
+                    default=None,
+                    required=True,
+                )
+            return cls(Required, checker=checker)
+        # legacy: param is named "bot" and has no type annotation
+        elif param.annotation == param.empty and param.name == "bot":
+            return cls(Required)
 
     async def _solve(self, bot: "Bot", **kwargs: Any) -> Any:
         return bot
 
     async def _check(self, bot: "Bot", **kwargs: Any) -> None:
         if checker := self.extra.get("checker"):
             check_field_type(checker, bot)
 
 
 class EventParam(Param):
-    """{ref}`nonebot.adapters.Event` 参数"""
+    """{ref}`nonebot.adapters.Event` 注入参数
+
+    本注入解析所有类型为且仅为 {ref}`nonebot.adapters.Event` 及其子类或 `None` 的参数。
+
+    为保证兼容性，本注入还会解析名为 `event` 且没有类型注解的参数。
+    """
 
     def __repr__(self) -> str:
         return (
             "EventParam("
             + (
                 repr(cast(ModelField, checker).type_)
                 if (checker := self.extra.get("checker"))
@@ -227,153 +246,204 @@
 
     @classmethod
     def _check_param(
         cls, param: inspect.Parameter, allow_types: Tuple[Type[Param], ...]
     ) -> Optional["EventParam"]:
         from nonebot.adapters import Event
 
-        if param.default == param.empty:
-            if generic_check_issubclass(param.annotation, Event):
-                checker: Optional[ModelField] = None
-                if param.annotation is not Event:
-                    checker = ModelField(
-                        name=param.name,
-                        type_=param.annotation,
-                        class_validators=None,
-                        model_config=CustomConfig,
-                        default=None,
-                        required=True,
-                    )
-                return cls(Required, checker=checker)
-            elif param.annotation == param.empty and param.name == "event":
-                return cls(Required)
+        # param type is Event(s) or subclass(es) of Event or None
+        if generic_check_issubclass(param.annotation, Event):
+            checker: Optional[ModelField] = None
+            if param.annotation is not Event:
+                checker = ModelField(
+                    name=param.name,
+                    type_=param.annotation,
+                    class_validators=None,
+                    model_config=CustomConfig,
+                    default=None,
+                    required=True,
+                )
+            return cls(Required, checker=checker)
+        # legacy: param is named "event" and has no type annotation
+        elif param.annotation == param.empty and param.name == "event":
+            return cls(Required)
 
     async def _solve(self, event: "Event", **kwargs: Any) -> Any:
         return event
 
     async def _check(self, event: "Event", **kwargs: Any) -> Any:
         if checker := self.extra.get("checker", None):
             check_field_type(checker, event)
 
 
 class StateParam(Param):
-    """事件处理状态参数"""
+    """事件处理状态注入参数
+
+    本注入解析所有类型为 `T_State` 的参数。
+
+    为保证兼容性，本注入还会解析名为 `state` 且没有类型注解的参数。
+    """
 
     def __repr__(self) -> str:
         return "StateParam()"
 
     @classmethod
     def _check_param(
         cls, param: inspect.Parameter, allow_types: Tuple[Type[Param], ...]
     ) -> Optional["StateParam"]:
-        if param.default == param.empty:
-            if param.annotation is T_State:
-                return cls(Required)
-            elif param.annotation == param.empty and param.name == "state":
-                return cls(Required)
+        # param type is T_State
+        if param.annotation is T_State:
+            return cls(Required)
+        # legacy: param is named "state" and has no type annotation
+        elif param.annotation == param.empty and param.name == "state":
+            return cls(Required)
 
     async def _solve(self, state: T_State, **kwargs: Any) -> Any:
         return state
 
 
 class MatcherParam(Param):
-    """事件响应器实例参数"""
+    """事件响应器实例注入参数
+
+    本注入解析所有类型为且仅为 {ref}`nonebot.matcher.Matcher` 及其子类或 `None` 的参数。
+
+    为保证兼容性，本注入还会解析名为 `matcher` 且没有类型注解的参数。
+    """
 
     def __repr__(self) -> str:
         return "MatcherParam()"
 
     @classmethod
     def _check_param(
         cls, param: inspect.Parameter, allow_types: Tuple[Type[Param], ...]
     ) -> Optional["MatcherParam"]:
         from nonebot.matcher import Matcher
 
-        if generic_check_issubclass(param.annotation, Matcher) or (
-            param.annotation == param.empty and param.name == "matcher"
-        ):
+        # param type is Matcher(s) or subclass(es) of Matcher or None
+        if generic_check_issubclass(param.annotation, Matcher):
+            checker: Optional[ModelField] = None
+            if param.annotation is not Matcher:
+                checker = ModelField(
+                    name=param.name,
+                    type_=param.annotation,
+                    class_validators=None,
+                    model_config=CustomConfig,
+                    default=None,
+                    required=True,
+                )
+            return cls(Required, checker=checker)
+        # legacy: param is named "matcher" and has no type annotation
+        elif param.annotation == param.empty and param.name == "matcher":
             return cls(Required)
 
     async def _solve(self, matcher: "Matcher", **kwargs: Any) -> Any:
         return matcher
 
+    async def _check(self, matcher: "Matcher", **kwargs: Any) -> Any:
+        if checker := self.extra.get("checker", None):
+            check_field_type(checker, matcher)
+
 
 class ArgInner:
     def __init__(
         self, key: Optional[str], type: Literal["message", "str", "plaintext"]
     ) -> None:
         self.key = key
         self.type = type
 
     def __repr__(self) -> str:
         return f"ArgInner(key={self.key!r}, type={self.type!r})"
 
 
 def Arg(key: Optional[str] = None) -> Any:
-    """`got` 的 Arg 参数消息"""
+    """Arg 参数消息"""
     return ArgInner(key, "message")
 
 
 def ArgStr(key: Optional[str] = None) -> str:
-    """`got` 的 Arg 参数消息文本"""
+    """Arg 参数消息文本"""
     return ArgInner(key, "str")  # type: ignore
 
 
 def ArgPlainText(key: Optional[str] = None) -> str:
-    """`got` 的 Arg 参数消息纯文本"""
+    """Arg 参数消息纯文本"""
     return ArgInner(key, "plaintext")  # type: ignore
 
 
 class ArgParam(Param):
-    """`got` 的 Arg 参数"""
+    """Arg 注入参数
+
+    本注入解析事件响应器操作 `got` 所获取的参数。
+
+    可以通过 `Arg`、`ArgStr`、`ArgPlainText` 等函数参数 `key` 指定获取的参数，
+    留空则会根据参数名称获取。
+    """
 
     def __repr__(self) -> str:
         return f"ArgParam(key={self.extra['key']!r}, type={self.extra['type']!r})"
 
     @classmethod
     def _check_param(
         cls, param: inspect.Parameter, allow_types: Tuple[Type[Param], ...]
     ) -> Optional["ArgParam"]:
         if isinstance(param.default, ArgInner):
             return cls(
                 Required, key=param.default.key or param.name, type=param.default.type
             )
+        elif get_origin(param.annotation) is Annotated:
+            for arg in get_args(param.annotation):
+                if isinstance(arg, ArgInner):
+                    return cls(Required, key=arg.key or param.name, type=arg.type)
 
     async def _solve(self, matcher: "Matcher", **kwargs: Any) -> Any:
-        message = matcher.get_arg(self.extra["key"])
+        key: str = self.extra["key"]
+        message = matcher.get_arg(key)
         if message is None:
             return message
         if self.extra["type"] == "message":
             return message
         elif self.extra["type"] == "str":
             return str(message)
         else:
             return message.extract_plain_text()
 
 
 class ExceptionParam(Param):
-    """`run_postprocessor` 的异常参数"""
+    """{ref}`nonebot.message.run_postprocessor` 的异常注入参数
+
+    本注入解析所有类型为 `Exception` 或 `None` 的参数。
+
+    为保证兼容性，本注入还会解析名为 `exception` 且没有类型注解的参数。
+    """
 
     def __repr__(self) -> str:
         return "ExceptionParam()"
 
     @classmethod
     def _check_param(
         cls, param: inspect.Parameter, allow_types: Tuple[Type[Param], ...]
     ) -> Optional["ExceptionParam"]:
-        if generic_check_issubclass(param.annotation, Exception) or (
-            param.annotation == param.empty and param.name == "exception"
-        ):
+        # param type is Exception(s) or subclass(es) of Exception or None
+        if generic_check_issubclass(param.annotation, Exception):
+            return cls(Required)
+        # legacy: param is named "exception" and has no type annotation
+        elif param.annotation == param.empty and param.name == "exception":
             return cls(Required)
 
     async def _solve(self, exception: Optional[Exception] = None, **kwargs: Any) -> Any:
         return exception
 
 
 class DefaultParam(Param):
-    """默认值参数"""
+    """默认值注入参数
+
+    本注入解析所有剩余未能解析且具有默认值的参数。
+
+    本注入参数应该具有最低优先级，因此应该在所有其他注入参数之后使用。
+    """
 
     def __repr__(self) -> str:
         return f"DefaultParam(default={self.default!r})"
 
     @classmethod
     def _check_param(
         cls, param: inspect.Parameter, allow_types: Tuple[Type[Param], ...]
```

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/permission.py` & `nonebot2-2.0.1/nonebot/internal/permission.py`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/nonebot/internal/rule.py` & `nonebot2-2.0.1/nonebot/internal/rule.py`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/nonebot/log.py` & `nonebot2-2.0.1/nonebot/log.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 """本模块定义了 NoneBot 的日志记录 Logger。
 
 NoneBot 使用 [`loguru`][loguru] 来记录日志信息。
 
-自定义 logger 请参考 [自定义日志](https://v2.nonebot.dev/docs/appendices/log)
+自定义 logger 请参考 [自定义日志](https://nonebot.dev/docs/appendices/log)
 以及 [`loguru`][loguru] 文档。
 
 [loguru]: https://github.com/Delgan/loguru
 
 FrontMatter:
     sidebar_position: 7
     description: nonebot.log 模块
@@ -50,15 +50,15 @@
 
     def emit(self, record: logging.LogRecord):
         try:
             level = logger.level(record.levelname).name
         except ValueError:
             level = record.levelno
 
-        frame, depth = logging.currentframe(), 2
+        frame, depth = sys._getframe(6), 6
         while frame and frame.f_code.co_filename == logging.__file__:
             frame = frame.f_back
             depth += 1
 
         logger.opt(depth=depth, exception=record.exc_info).log(
             level, record.getMessage()
         )
@@ -84,9 +84,10 @@
 logger_id = logger.add(
     sys.stdout,
     level=0,
     diagnose=False,
     filter=default_filter,
     format=default_format,
 )
+"""默认日志处理器 id"""
 
 __autodoc__ = {"logger_id": False}
```

### Comparing `nonebot2-2.0.0rc4/nonebot/matcher.py` & `nonebot2-2.0.1/nonebot/matcher.py`

 * *Files identical despite different names*

### Comparing `nonebot2-2.0.0rc4/nonebot/params.py` & `nonebot2-2.0.1/nonebot/params.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,15 @@
 """本模块定义了依赖注入的各类参数。
 
 FrontMatter:
     sidebar_position: 4
     description: nonebot.params 模块
 """
 
-import warnings
-from typing import Any, Dict, List, Tuple, Union, Optional
+from typing import Any, Dict, List, Match, Tuple, Union, Optional
 
 from nonebot.typing import T_State
 from nonebot.matcher import Matcher
 from nonebot.internal.params import Arg as Arg
 from nonebot.internal.params import ArgStr as ArgStr
 from nonebot.internal.params import Depends as Depends
 from nonebot.internal.params import ArgParam as ArgParam
@@ -21,23 +20,20 @@
 from nonebot.internal.params import DependParam as DependParam
 from nonebot.internal.params import ArgPlainText as ArgPlainText
 from nonebot.internal.params import DefaultParam as DefaultParam
 from nonebot.internal.params import MatcherParam as MatcherParam
 from nonebot.internal.params import ExceptionParam as ExceptionParam
 from nonebot.consts import (
     CMD_KEY,
-    REGEX_STR,
     PREFIX_KEY,
-    REGEX_DICT,
     SHELL_ARGS,
     SHELL_ARGV,
     CMD_ARG_KEY,
     KEYWORD_KEY,
     RAW_CMD_KEY,
-    REGEX_GROUP,
     ENDSWITH_KEY,
     CMD_START_KEY,
     FULLMATCH_KEY,
     REGEX_MATCHED,
     STARTSWITH_KEY,
     CMD_WHITESPACE_KEY,
 )
@@ -138,49 +134,43 @@
 
 
 def ShellCommandArgv() -> Any:
     """shell 命令原始参数列表"""
     return Depends(_shell_command_argv, use_cache=False)
 
 
-def _regex_matched(state: T_State) -> str:
+def _regex_matched(state: T_State) -> Match[str]:
     return state[REGEX_MATCHED]
 
 
-def RegexMatched() -> str:
+def RegexMatched() -> Match[str]:
     """正则匹配结果"""
-    warnings.warn(
-        '"RegexMatched()" will be changed to "re.Match" object, '
-        'use "RegexStr()" instead. '
-        "See https://github.com/nonebot/nonebot2/pull/1453 .",
-        DeprecationWarning,
-    )
     return Depends(_regex_matched, use_cache=False)
 
 
 def _regex_str(state: T_State) -> str:
-    return state[REGEX_STR]
+    return _regex_matched(state).group()
 
 
 def RegexStr() -> str:
     """正则匹配结果文本"""
     return Depends(_regex_str, use_cache=False)
 
 
 def _regex_group(state: T_State) -> Tuple[Any, ...]:
-    return state[REGEX_GROUP]
+    return _regex_matched(state).groups()
 
 
 def RegexGroup() -> Tuple[Any, ...]:
     """正则匹配结果 group 元组"""
     return Depends(_regex_group, use_cache=False)
 
 
 def _regex_dict(state: T_State) -> Dict[str, Any]:
-    return state[REGEX_DICT]
+    return _regex_matched(state).groupdict()
 
 
 def RegexDict() -> Dict[str, Any]:
     """正则匹配结果 group 字典"""
     return Depends(_regex_dict, use_cache=False)
```

### Comparing `nonebot2-2.0.0rc4/nonebot/permission.py` & `nonebot2-2.0.1/nonebot/permission.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 """本模块是 {ref}`nonebot.matcher.Matcher.permission` 的类型定义。
 
-每个 {ref}`nonebot.matcher.Matcher` 拥有一个 {ref}`nonebot.permission.Permission` ，
-其中是 `PermissionChecker` 的集合，只要有一个 `PermissionChecker` 检查结果为 `True` 时就会继续运行。
+每个{ref}`事件响应器 <nonebot.matcher.Matcher>`
+拥有一个 {ref}`nonebot.permission.Permission`，其中是 `PermissionChecker` 的集合。
+只要有一个 `PermissionChecker` 检查结果为 `True` 时就会继续运行。
 
 FrontMatter:
     sidebar_position: 6
     description: nonebot.permission 模块
 """
 
 from nonebot.params import EventType
```

### Comparing `nonebot2-2.0.0rc4/nonebot/plugin/__init__.py` & `nonebot2-2.0.1/nonebot/plugin/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -20,16 +20,18 @@
 - `CommandGroup` => {ref}``CommandGroup` <nonebot.plugin.on.CommandGroup>`
 - `Matchergroup` => {ref}``MatcherGroup` <nonebot.plugin.on.MatcherGroup>`
 - `load_plugin` => {ref}``load_plugin` <nonebot.plugin.load.load_plugin>`
 - `load_plugins` => {ref}``load_plugins` <nonebot.plugin.load.load_plugins>`
 - `load_all_plugins` => {ref}``load_all_plugins` <nonebot.plugin.load.load_all_plugins>`
 - `load_from_json` => {ref}``load_from_json` <nonebot.plugin.load.load_from_json>`
 - `load_from_toml` => {ref}``load_from_toml` <nonebot.plugin.load.load_from_toml>`
-- `load_builtin_plugin` => {ref}``load_builtin_plugin` <nonebot.plugin.load.load_builtin_plugin>`
-- `load_builtin_plugins` => {ref}``load_builtin_plugins` <nonebot.plugin.load.load_builtin_plugins>`
+- `load_builtin_plugin` =>
+  {ref}``load_builtin_plugin` <nonebot.plugin.load.load_builtin_plugin>`
+- `load_builtin_plugins` =>
+  {ref}``load_builtin_plugins` <nonebot.plugin.load.load_builtin_plugins>`
 - `require` => {ref}``require` <nonebot.plugin.load.require>`
 - `PluginMetadata` => {ref}``PluginMetadata` <nonebot.plugin.plugin.PluginMetadata>`
 
 FrontMatter:
     sidebar_position: 0
     description: nonebot.plugin 模块
 """
@@ -38,15 +40,15 @@
 from types import ModuleType
 from contextvars import ContextVar
 from typing import Set, Dict, List, Tuple, Optional
 
 _plugins: Dict[str, "Plugin"] = {}
 _managers: List["PluginManager"] = []
 _current_plugin_chain: ContextVar[Tuple["Plugin", ...]] = ContextVar(
-    "_current_plugin_chain", default=tuple()
+    "_current_plugin_chain", default=()
 )
 
 
 def _module_name_to_plugin_name(module_name: str) -> str:
     return module_name.rsplit(".", 1)[-1]
 
 
@@ -128,7 +130,8 @@
 from .load import load_from_json as load_from_json
 from .load import load_from_toml as load_from_toml
 from .on import on_shell_command as on_shell_command
 from .plugin import PluginMetadata as PluginMetadata
 from .load import load_all_plugins as load_all_plugins
 from .load import load_builtin_plugin as load_builtin_plugin
 from .load import load_builtin_plugins as load_builtin_plugins
+from .load import inherit_supported_adapters as inherit_supported_adapters
```

### Comparing `nonebot2-2.0.0rc4/nonebot/plugin/load.py` & `nonebot2-2.0.1/nonebot/plugin/load.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,35 +1,37 @@
 """本模块定义插件加载接口。
 
 FrontMatter:
     sidebar_position: 1
     description: nonebot.plugin.load 模块
 """
+
 import json
 from pathlib import Path
 from types import ModuleType
 from typing import Set, Union, Iterable, Optional
 
 from nonebot.utils import path_to_module_name
 
 from .plugin import Plugin
 from .manager import PluginManager
-from . import _managers, get_plugin, _module_name_to_plugin_name
+from . import _managers, get_plugin, _current_plugin_chain, _module_name_to_plugin_name
 
 try:  # pragma: py-gte-311
-    import tomllib  # pyright: reportMissingImports=false
+    import tomllib  # pyright: ignore[reportMissingImports]
 except ModuleNotFoundError:  # pragma: py-lt-311
     import tomli as tomllib
 
 
 def load_plugin(module_path: Union[str, Path]) -> Optional[Plugin]:
     """加载单个插件，可以是本地插件或是通过 `pip` 安装的插件。
 
     参数:
-        module_path: 插件名称 `path.to.your.plugin` 或插件路径 `pathlib.Path(path/to/your/plugin)`
+        module_path: 插件名称 `path.to.your.plugin`
+            或插件路径 `pathlib.Path(path/to/your/plugin)`
     """
     module_path = (
         path_to_module_name(module_path)
         if isinstance(module_path, Path)
         else module_path
     )
     manager = PluginManager([module_path])
@@ -59,15 +61,16 @@
     """
     manager = PluginManager(module_path, plugin_dir)
     _managers.append(manager)
     return manager.load_all_plugins()
 
 
 def load_from_json(file_path: str, encoding: str = "utf-8") -> Set[Plugin]:
-    """导入指定 json 文件中的 `plugins` 以及 `plugin_dirs` 下多个插件，以 `_` 开头的插件不会被导入!
+    """导入指定 json 文件中的 `plugins` 以及 `plugin_dirs` 下多个插件。
+    以 `_` 开头的插件不会被导入!
 
     参数:
         file_path: 指定 json 文件路径
         encoding: 指定 json 文件编码
 
     用法:
         ```json title=plugins.json
@@ -77,27 +80,29 @@
         }
         ```
 
         ```python
         nonebot.load_from_json("plugins.json")
         ```
     """
-    with open(file_path, "r", encoding=encoding) as f:
+    with open(file_path, encoding=encoding) as f:
         data = json.load(f)
     if not isinstance(data, dict):
         raise TypeError("json file must contains a dict!")
     plugins = data.get("plugins")
     plugin_dirs = data.get("plugin_dirs")
     assert isinstance(plugins, list), "plugins must be a list of plugin name"
     assert isinstance(plugin_dirs, list), "plugin_dirs must be a list of directories"
     return load_all_plugins(set(plugins), set(plugin_dirs))
 
 
 def load_from_toml(file_path: str, encoding: str = "utf-8") -> Set[Plugin]:
-    """导入指定 toml 文件 `[tool.nonebot]` 中的 `plugins` 以及 `plugin_dirs` 下多个插件，以 `_` 开头的插件不会被导入!
+    """导入指定 toml 文件 `[tool.nonebot]` 中的
+    `plugins` 以及 `plugin_dirs` 下多个插件。
+    以 `_` 开头的插件不会被导入!
 
     参数:
         file_path: 指定 toml 文件路径
         encoding: 指定 toml 文件编码
 
     用法:
         ```toml title=pyproject.toml
@@ -106,15 +111,15 @@
         plugin_dirs = ["some_dir"]
         ```
 
         ```python
         nonebot.load_from_toml("pyproject.toml")
         ```
     """
-    with open(file_path, "r", encoding=encoding) as f:
+    with open(file_path, encoding=encoding) as f:
         data = tomllib.loads(f.read())
 
     nonebot_data = data.get("tool", {}).get("nonebot")
     if nonebot_data is None:
         raise ValueError("Cannot find '[tool.nonebot]' in given toml file!")
     if not isinstance(nonebot_data, dict):
         raise TypeError("'[tool.nonebot]' must be a Table!")
@@ -157,15 +162,59 @@
     参数:
         name: 插件名，即 {ref}`nonebot.plugin.plugin.Plugin.name`。
 
     异常:
         RuntimeError: 插件无法加载
     """
     plugin = get_plugin(_module_name_to_plugin_name(name))
+    # if plugin not loaded
     if not plugin:
+        # plugin already declared
         if manager := _find_manager_by_name(name):
             plugin = manager.load_plugin(name)
+        # plugin not declared, try to declare and load it
         else:
-            plugin = load_plugin(name)
+            # clear current plugin chain, ensure plugin loaded in a new context
+            _t = _current_plugin_chain.set(())
+            try:
+                plugin = load_plugin(name)
+            finally:
+                _current_plugin_chain.reset(_t)
     if not plugin:
         raise RuntimeError(f'Cannot load plugin "{name}"!')
     return plugin.module
+
+
+def inherit_supported_adapters(*names: str) -> Optional[Set[str]]:
+    """获取已加载插件的适配器支持状态集合。
+
+    如果传入了多个插件名称，返回值会自动取交集。
+
+    参数:
+        names: 插件名称列表。
+
+    异常:
+        RuntimeError: 插件未加载
+        ValueError: 插件缺少元数据
+    """
+    final_supported: Optional[Set[str]] = None
+
+    for name in names:
+        plugin = get_plugin(_module_name_to_plugin_name(name))
+        if plugin is None:
+            raise RuntimeError(f'Plugin "{name}" is not loaded!')
+        meta = plugin.metadata
+        if meta is None:
+            raise ValueError(f'Plugin "{name}" has no metadata!')
+        support = meta.supported_adapters
+        if support is None:
+            continue
+        final_supported = (
+            support if final_supported is None else (final_supported & support)
+        )
+
+    return final_supported and {
+        f"nonebot.adapters.{adapter_name[1:]}"
+        if adapter_name.startswith("~")
+        else adapter_name
+        for adapter_name in final_supported
+    }
```

### Comparing `nonebot2-2.0.0rc4/nonebot/plugin/manager.py` & `nonebot2-2.0.1/nonebot/plugin/manager.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,14 +2,15 @@
 
 参考: [import hooks](https://docs.python.org/3/reference/import.html#import-hooks), [PEP302](https://www.python.org/dev/peps/pep-0302/)
 
 FrontMatter:
     sidebar_position: 5
     description: nonebot.plugin.manager 模块
 """
+
 import sys
 import pkgutil
 import importlib
 from pathlib import Path
 from itertools import chain
 from types import ModuleType
 from importlib.abc import MetaPathFinder
@@ -224,14 +225,15 @@
         # create plugin before executing
         plugin = _new_plugin(self.name, module, self.manager)
         setattr(module, "__plugin__", plugin)
 
         # detect parent plugin before entering current plugin context
         parent_plugins = _current_plugin_chain.get()
         for pre_plugin in reversed(parent_plugins):
+            # ensure parent plugin is declared before current plugin
             if _managers.index(pre_plugin.manager) < _managers.index(self.manager):
                 plugin.parent_plugin = pre_plugin
                 pre_plugin.sub_plugins.add(plugin)
                 break
 
         # enter plugin context
         _plugin_token = _current_plugin_chain.set(parent_plugins + (plugin,))
```

### Comparing `nonebot2-2.0.0rc4/nonebot/plugin/on.py` & `nonebot2-2.0.1/nonebot/plugin/on.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 """本模块定义事件响应器便携定义函数。
 
 FrontMatter:
     sidebar_position: 2
     description: nonebot.plugin.on 模块
 """
+
 import re
 import inspect
 from types import ModuleType
 from datetime import datetime, timedelta
 from typing import Any, Set, Dict, List, Type, Tuple, Union, Optional
 
 from nonebot.adapters import Event
@@ -318,15 +319,16 @@
     _depth: int = 0,
     **kwargs,
 ) -> Type[Matcher]:
     """注册一个支持 `shell_like` 解析参数的命令消息事件响应器。
 
     与普通的 `on_command` 不同的是，在添加 `parser` 参数时, 响应器会自动处理消息。
 
-    并将用户输入的原始参数列表保存在 `state["argv"]`, `parser` 处理的参数保存在 `state["args"]` 中
+    可以通过 {ref}`nonebot.params.ShellCommandArgv` 获取原始参数列表，
+    通过 {ref}`nonebot.params.ShellCommandArgs` 获取解析后的参数字典。
 
     参数:
         cmd: 指定命令内容
         rule: 事件响应规则
         aliases: 命令别名
         parser: `nonebot.rule.ArgumentParser` 对象
         permission: 事件响应权限
@@ -423,29 +425,33 @@
 
 
 class CommandGroup(_Group):
     """命令组，用于声明一组有相同名称前缀的命令。
 
     参数:
         cmd: 指定命令内容
+        prefix_aliases: 是否影响命令别名，给命令别名加前缀
         rule: 事件响应规则
         permission: 事件响应权限
         handlers: 事件处理函数列表
         temp: 是否为临时事件响应器（仅执行一次）
         expire_time: 事件响应器最终有效时间点，过时即被删除
         priority: 事件响应器优先级
         block: 是否阻止事件向更低优先级传递
         state: 默认 state
     """
 
-    def __init__(self, cmd: Union[str, Tuple[str, ...]], **kwargs):
+    def __init__(
+        self, cmd: Union[str, Tuple[str, ...]], prefix_aliases: bool = False, **kwargs
+    ):
         """命令前缀"""
         super().__init__(**kwargs)
         self.basecmd: Tuple[str, ...] = (cmd,) if isinstance(cmd, str) else cmd
         self.base_kwargs.pop("aliases", None)
+        self.prefix_aliases = prefix_aliases
 
     def __repr__(self) -> str:
         return f"CommandGroup(cmd={self.basecmd}, matchers={len(self.matchers)})"
 
     def command(self, cmd: Union[str, Tuple[str, ...]], **kwargs) -> Type[Matcher]:
         """注册一个新的命令。新参数将会覆盖命令组默认值
 
@@ -460,14 +466,19 @@
             expire_time: 事件响应器最终有效时间点，过时即被删除
             priority: 事件响应器优先级
             block: 是否阻止事件向更低优先级传递
             state: 默认 state
         """
         sub_cmd = (cmd,) if isinstance(cmd, str) else cmd
         cmd = self.basecmd + sub_cmd
+        if self.prefix_aliases and (aliases := kwargs.get("aliases")):
+            kwargs["aliases"] = {
+                self.basecmd + ((alias,) if isinstance(alias, str) else alias)
+                for alias in aliases
+            }
         matcher = on_command(cmd, **self._get_final_kwargs(kwargs))
         self.matchers.append(matcher)
         return matcher
 
     def shell_command(
         self, cmd: Union[str, Tuple[str, ...]], **kwargs
     ) -> Type[Matcher]:
@@ -484,14 +495,19 @@
             expire_time: 事件响应器最终有效时间点，过时即被删除
             priority: 事件响应器优先级
             block: 是否阻止事件向更低优先级传递
             state: 默认 state
         """
         sub_cmd = (cmd,) if isinstance(cmd, str) else cmd
         cmd = self.basecmd + sub_cmd
+        if self.prefix_aliases and (aliases := kwargs.get("aliases")):
+            kwargs["aliases"] = {
+                self.basecmd + ((alias,) if isinstance(alias, str) else alias)
+                for alias in aliases
+            }
         matcher = on_shell_command(cmd, **self._get_final_kwargs(kwargs))
         self.matchers.append(matcher)
         return matcher
 
 
 class MatcherGroup(_Group):
     """事件响应器组合，统一管理。为 `Matcher` 创建提供默认属性。"""
@@ -708,15 +724,16 @@
         parser: Optional[ArgumentParser] = None,
         **kwargs,
     ) -> Type[Matcher]:
         """注册一个支持 `shell_like` 解析参数的命令消息事件响应器。
 
         与普通的 `on_command` 不同的是，在添加 `parser` 参数时, 响应器会自动处理消息。
 
-        并将用户输入的原始参数列表保存在 `state["argv"]`, `parser` 处理的参数保存在 `state["args"]` 中
+        可以通过 {ref}`nonebot.params.ShellCommandArgv` 获取原始参数列表，
+        通过 {ref}`nonebot.params.ShellCommandArgs` 获取解析后的参数字典。
 
         参数:
             cmd: 指定命令内容
             aliases: 命令别名
             parser: `nonebot.rule.ArgumentParser` 对象
             rule: 事件响应规则
             permission: 事件响应权限
```

### Comparing `nonebot2-2.0.0rc4/nonebot/rule.py` & `nonebot2-2.0.1/nonebot/rule.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,20 +1,22 @@
 """本模块是 {ref}`nonebot.matcher.Matcher.rule` 的类型定义。
 
-每个事件响应器 {ref}`nonebot.matcher.Matcher` 拥有一个匹配规则 {ref}`nonebot.rule.Rule`
-其中是 `RuleChecker` 的集合，只有当所有 `RuleChecker` 检查结果为 `True` 时继续运行。
+每个{ref}`事件响应器 <nonebot.matcher.Matcher>`拥有一个
+{ref}`nonebot.rule.Rule`，其中是 `RuleChecker` 的集合。
+只有当所有 `RuleChecker` 检查结果为 `True` 时继续运行。
 
 FrontMatter:
     sidebar_position: 5
     description: nonebot.rule 模块
 """
 
 import re
 import shlex
 from argparse import Action
+from gettext import gettext
 from argparse import ArgumentError
 from contextvars import ContextVar
 from itertools import chain, product
 from argparse import Namespace as Namespace
 from argparse import ArgumentParser as ArgParser
 from typing import (
     IO,
@@ -39,47 +41,43 @@
 from nonebot.typing import T_State
 from nonebot.exception import ParserExit
 from nonebot.internal.rule import Rule as Rule
 from nonebot.adapters import Bot, Event, Message, MessageSegment
 from nonebot.params import Command, EventToMe, CommandArg, CommandWhitespace
 from nonebot.consts import (
     CMD_KEY,
-    REGEX_STR,
     PREFIX_KEY,
-    REGEX_DICT,
     SHELL_ARGS,
     SHELL_ARGV,
     CMD_ARG_KEY,
     KEYWORD_KEY,
     RAW_CMD_KEY,
-    REGEX_GROUP,
     ENDSWITH_KEY,
     CMD_START_KEY,
     FULLMATCH_KEY,
     REGEX_MATCHED,
     STARTSWITH_KEY,
     CMD_WHITESPACE_KEY,
 )
 
 T = TypeVar("T")
 
-CMD_RESULT = TypedDict(
-    "CMD_RESULT",
-    {
-        "command": Optional[Tuple[str, ...]],
-        "raw_command": Optional[str],
-        "command_arg": Optional[Message[MessageSegment]],
-        "command_start": Optional[str],
-        "command_whitespace": Optional[str],
-    },
-)
 
-TRIE_VALUE = NamedTuple(
-    "TRIE_VALUE", [("command_start", str), ("command", Tuple[str, ...])]
-)
+class CMD_RESULT(TypedDict):
+    command: Optional[Tuple[str, ...]]
+    raw_command: Optional[str]
+    command_arg: Optional[Message]
+    command_start: Optional[str]
+    command_whitespace: Optional[str]
+
+
+class TRIE_VALUE(NamedTuple):
+    command_start: str
+    command: Tuple[str, ...]
+
 
 parser_message: ContextVar[str] = ContextVar("parser_message")
 
 
 class TrieRule:
     prefix: CharTrie = CharTrie()
 
@@ -374,19 +372,20 @@
 
     def __hash__(self) -> int:
         return hash((frozenset(self.cmds),))
 
     async def __call__(
         self,
         cmd: Optional[Tuple[str, ...]] = Command(),
+        cmd_arg: Optional[Message] = CommandArg(),
         cmd_whitespace: Optional[str] = CommandWhitespace(),
     ) -> bool:
         if cmd not in self.cmds:
             return False
-        if self.force_whitespace is None:
+        if self.force_whitespace is None or not cmd_arg:
             return True
         if isinstance(self.force_whitespace, str):
             return self.force_whitespace == cmd_whitespace
         return self.force_whitespace == (cmd_whitespace is not None)
 
 
 def command(
@@ -403,15 +402,15 @@
     通过 {ref}`nonebot.params.CommandArg` 获取匹配成功的命令参数。
 
     参数:
         cmds: 命令文本或命令元组
         force_whitespace: 是否强制命令后必须有指定空白符
 
     用法:
-        使用默认 `command_start`, `command_sep` 配置
+        使用默认 `command_start`, `command_sep` 配置情况下：
 
         命令 `("test",)` 可以匹配: `/test` 开头的消息
         命令 `("test", "sub")` 可以匹配: `/test.sub` 开头的消息
 
     :::tip 提示
     命令内容与后续消息间无需空格!
     :::
@@ -438,46 +437,79 @@
 
     return Rule(CommandRule(commands, force_whitespace))
 
 
 class ArgumentParser(ArgParser):
     """`shell_like` 命令参数解析器，解析出错时不会退出程序。
 
+    支持 {ref}`nonebot.adapters.Message` 富文本解析。
+
     用法:
         用法与 `argparse.ArgumentParser` 相同，
         参考文档: [argparse](https://docs.python.org/3/library/argparse.html)
     """
 
     if TYPE_CHECKING:
 
         @overload
-        def parse_args(
-            self, args: Optional[Sequence[Union[str, MessageSegment]]] = ...
-        ) -> Namespace:
+        def parse_known_args(
+            self,
+            args: Optional[Sequence[Union[str, MessageSegment]]] = None,
+            namespace: None = None,
+        ) -> Tuple[Namespace, List[Union[str, MessageSegment]]]:
             ...
 
         @overload
-        def parse_args(
-            self, args: Optional[Sequence[Union[str, MessageSegment]]], namespace: None
-        ) -> Namespace:
-            ...  # type: ignore[misc]
+        def parse_known_args(
+            self, args: Optional[Sequence[Union[str, MessageSegment]]], namespace: T
+        ) -> Tuple[T, List[Union[str, MessageSegment]]]:
+            ...
 
         @overload
-        def parse_args(
-            self, args: Optional[Sequence[Union[str, MessageSegment]]], namespace: T
-        ) -> T:
+        def parse_known_args(
+            self, *, namespace: T
+        ) -> Tuple[T, List[Union[str, MessageSegment]]]:
             ...
 
-        def parse_args(
+        def parse_known_args(
             self,
             args: Optional[Sequence[Union[str, MessageSegment]]] = None,
             namespace: Optional[T] = None,
-        ) -> Union[Namespace, T]:
+        ) -> Tuple[Union[Namespace, T], List[Union[str, MessageSegment]]]:
             ...
 
+    @overload
+    def parse_args(
+        self,
+        args: Optional[Sequence[Union[str, MessageSegment]]] = None,
+        namespace: None = None,
+    ) -> Namespace:
+        ...
+
+    @overload
+    def parse_args(
+        self, args: Optional[Sequence[Union[str, MessageSegment]]], namespace: T
+    ) -> T:
+        ...
+
+    @overload
+    def parse_args(self, *, namespace: T) -> T:
+        ...
+
+    def parse_args(
+        self,
+        args: Optional[Sequence[Union[str, MessageSegment]]] = None,
+        namespace: Optional[T] = None,
+    ) -> Union[Namespace, T]:
+        result, argv = self.parse_known_args(args, namespace)
+        if argv:
+            msg = gettext("unrecognized arguments: %s")
+            self.error(msg % " ".join(map(str, argv)))
+        return cast(Union[Namespace, T], result)
+
     def _parse_optional(
         self, arg_string: Union[str, MessageSegment]
     ) -> Optional[Tuple[Optional[Action], str, Optional[str]]]:
         return (
             super()._parse_optional(arg_string) if isinstance(arg_string, str) else None
         )
 
@@ -554,30 +586,35 @@
     *cmds: Union[str, Tuple[str, ...]], parser: Optional[ArgumentParser] = None
 ) -> Rule:
     """匹配 `shell_like` 形式的消息命令。
 
     根据配置里提供的 {ref}``command_start` <nonebot.config.Config.command_start>`,
     {ref}``command_sep` <nonebot.config.Config.command_sep>` 判断消息是否为命令。
 
-    可以通过 {ref}`nonebot.params.Command` 获取匹配成功的命令（例: `("test",)`），
-    通过 {ref}`nonebot.params.RawCommand` 获取匹配成功的原始命令文本（例: `"/test"`），
-    通过 {ref}`nonebot.params.ShellCommandArgv` 获取解析前的参数列表（例: `["arg", "-h"]`），
-    通过 {ref}`nonebot.params.ShellCommandArgs` 获取解析后的参数字典（例: `{"arg": "arg", "h": True}`）。
+    可以通过 {ref}`nonebot.params.Command` 获取匹配成功的命令
+    （例: `("test",)`），
+    通过 {ref}`nonebot.params.RawCommand` 获取匹配成功的原始命令文本
+    （例: `"/test"`），
+    通过 {ref}`nonebot.params.ShellCommandArgv` 获取解析前的参数列表
+    （例: `["arg", "-h"]`），
+    通过 {ref}`nonebot.params.ShellCommandArgs` 获取解析后的参数字典
+    （例: `{"arg": "arg", "h": True}`）。
 
     :::warning 警告
     如果参数解析失败，则通过 {ref}`nonebot.params.ShellCommandArgs`
     获取的将是 {ref}`nonebot.exception.ParserExit` 异常。
     :::
 
     参数:
         cmds: 命令文本或命令元组
         parser: {ref}`nonebot.rule.ArgumentParser` 对象
 
     用法:
-        使用默认 `command_start`, `command_sep` 配置，更多示例参考 `argparse` 标准库文档。
+        使用默认 `command_start`, `command_sep` 配置，更多示例参考
+        [argparse](https://docs.python.org/3/library/argparse.html) 标准库文档。
 
         ```python
         from nonebot.rule import ArgumentParser
 
         parser = ArgumentParser()
         parser.add_argument("-a", action="store_true")
 
@@ -642,18 +679,15 @@
 
     async def __call__(self, event: Event, state: T_State) -> bool:
         try:
             msg = event.get_message()
         except Exception:
             return False
         if matched := re.search(self.regex, str(msg), self.flags):
-            state[REGEX_MATCHED] = matched.group()
-            state[REGEX_STR] = matched.group()
-            state[REGEX_GROUP] = matched.groups()
-            state[REGEX_DICT] = matched.groupdict()
+            state[REGEX_MATCHED] = matched
             return True
         else:
             return False
 
 
 def regex(regex: str, flags: Union[int, re.RegexFlag] = 0) -> Rule:
     """匹配符合正则表达式的消息字符串。
@@ -667,15 +701,16 @@
         flags: 正则表达式标记
 
     :::tip 提示
     正则表达式匹配使用 search 而非 match，如需从头匹配请使用 `r"^xxx"` 来确保匹配开头
     :::
 
     :::tip 提示
-    正则表达式匹配使用 `EventMessage` 的 `str` 字符串，而非 `EventMessage` 的 `PlainText` 纯文本字符串
+    正则表达式匹配使用 `EventMessage` 的 `str` 字符串，
+    而非 `EventMessage` 的 `PlainText` 纯文本字符串
     :::
     """
 
     return Rule(RegexRule(regex, flags))
 
 
 class ToMeRule:
```

### Comparing `nonebot2-2.0.0rc4/nonebot/typing.py` & `nonebot2-2.0.1/nonebot/typing.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 """本模块定义了 NoneBot 模块中共享的一些类型。
 
-下面的文档中，「类型」部分使用 Python 的 Type Hint 语法，
+使用 Python 的 Type Hint 语法，
 参考 [`PEP 484`](https://www.python.org/dev/peps/pep-0484/),
 [`PEP 526`](https://www.python.org/dev/peps/pep-0526/) 和
 [`typing`](https://docs.python.org/3/library/typing.html)。
 
-除了 Python 内置的类型，下面还出现了如下 NoneBot 自定类型，实际上它们是 Python 内置类型的别名。
-
 FrontMatter:
     sidebar_position: 11
     description: nonebot.typing 模块
 """
 
+import warnings
+from typing_extensions import ParamSpec, TypeAlias, override
 from typing import (
     TYPE_CHECKING,
     Any,
     Dict,
     Union,
     TypeVar,
     Callable,
@@ -26,157 +26,162 @@
 if TYPE_CHECKING:
     from asyncio import Task
 
     from nonebot.adapters import Bot
     from nonebot.permission import Permission
 
 T = TypeVar("T")
+P = ParamSpec("P")
 
-T_Wrapped = TypeVar("T_Wrapped", bound=Callable)
+T_Wrapped: TypeAlias = Callable[P, T]
 
 
-def overrides(InterfaceClass: object) -> Callable[[T_Wrapped], T_Wrapped]:
+def overrides(InterfaceClass: object):
     """标记一个方法为父类 interface 的 implement"""
 
-    def overrider(func: T_Wrapped) -> T_Wrapped:
-        assert func.__name__ in dir(InterfaceClass), f"Error method: {func.__name__}"
-        return func
-
-    return overrider
+    warnings.warn(
+        "overrides is deprecated and will be removed in a future version, "
+        "use @typing_extensions.override instead. "
+        "See [PEP 698](https://peps.python.org/pep-0698/) for more details.",
+        DeprecationWarning,
+    )
+    return override
 
 
 # state
-T_State = Dict[Any, Any]
+T_State: TypeAlias = Dict[Any, Any]
 """事件处理状态 State 类型"""
 
-_DependentCallable = Union[Callable[..., T], Callable[..., Awaitable[T]]]
+_DependentCallable: TypeAlias = Union[Callable[..., T], Callable[..., Awaitable[T]]]
 
 # driver hooks
-T_BotConnectionHook = _DependentCallable[Any]
+T_BotConnectionHook: TypeAlias = _DependentCallable[Any]
 """Bot 连接建立时钩子函数
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - DefaultParam: 带有默认值的参数
 """
-T_BotDisconnectionHook = _DependentCallable[Any]
+T_BotDisconnectionHook: TypeAlias = _DependentCallable[Any]
 """Bot 连接断开时钩子函数
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - DefaultParam: 带有默认值的参数
 """
 
 # api hooks
-T_CallingAPIHook = Callable[["Bot", str, Dict[str, Any]], Awaitable[Any]]
+T_CallingAPIHook: TypeAlias = Callable[["Bot", str, Dict[str, Any]], Awaitable[Any]]
 """`bot.call_api` 钩子函数"""
-T_CalledAPIHook = Callable[
+T_CalledAPIHook: TypeAlias = Callable[
     ["Bot", Optional[Exception], str, Dict[str, Any], Any], Awaitable[Any]
 ]
 """`bot.call_api` 后执行的函数，参数分别为 bot, exception, api, data, result"""
 
 # event hooks
-T_EventPreProcessor = _DependentCallable[Any]
+T_EventPreProcessor: TypeAlias = _DependentCallable[Any]
 """事件预处理函数 EventPreProcessor 类型
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - EventParam: Event 对象
 - StateParam: State 对象
 - DefaultParam: 带有默认值的参数
 """
-T_EventPostProcessor = _DependentCallable[Any]
+T_EventPostProcessor: TypeAlias = _DependentCallable[Any]
 """事件预处理函数 EventPostProcessor 类型
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - EventParam: Event 对象
 - StateParam: State 对象
 - DefaultParam: 带有默认值的参数
 """
 
 # matcher run hooks
-T_RunPreProcessor = _DependentCallable[Any]
+T_RunPreProcessor: TypeAlias = _DependentCallable[Any]
 """事件响应器运行前预处理函数 RunPreProcessor 类型
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - EventParam: Event 对象
 - StateParam: State 对象
 - MatcherParam: Matcher 对象
 - DefaultParam: 带有默认值的参数
 """
-T_RunPostProcessor = _DependentCallable[Any]
+T_RunPostProcessor: TypeAlias = _DependentCallable[Any]
 """事件响应器运行后后处理函数 RunPostProcessor 类型
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - EventParam: Event 对象
 - StateParam: State 对象
 - MatcherParam: Matcher 对象
 - ExceptionParam: 异常对象（可能为 None）
 - DefaultParam: 带有默认值的参数
 """
 
 # rule, permission
-T_RuleChecker = _DependentCallable[bool]
+T_RuleChecker: TypeAlias = _DependentCallable[bool]
 """RuleChecker 即判断是否响应事件的处理函数。
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - EventParam: Event 对象
 - StateParam: State 对象
 - DefaultParam: 带有默认值的参数
 """
-T_PermissionChecker = _DependentCallable[bool]
+T_PermissionChecker: TypeAlias = _DependentCallable[bool]
 """PermissionChecker 即判断事件是否满足权限的处理函数。
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - EventParam: Event 对象
 - DefaultParam: 带有默认值的参数
 """
 
-T_Handler = _DependentCallable[Any]
+T_Handler: TypeAlias = _DependentCallable[Any]
 """Handler 处理函数。"""
-T_TypeUpdater = _DependentCallable[str]
-"""TypeUpdater 在 Matcher.pause, Matcher.reject 时被运行，用于更新响应的事件类型。默认会更新为 `message`。
+T_TypeUpdater: TypeAlias = _DependentCallable[str]
+"""TypeUpdater 在 Matcher.pause, Matcher.reject 时被运行，用于更新响应的事件类型。
+默认会更新为 `message`。
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - EventParam: Event 对象
 - StateParam: State 对象
 - MatcherParam: Matcher 对象
 - DefaultParam: 带有默认值的参数
 """
-T_PermissionUpdater = _DependentCallable["Permission"]
-"""PermissionUpdater 在 Matcher.pause, Matcher.reject 时被运行，用于更新会话对象权限。默认会更新为当前事件的触发对象。
+T_PermissionUpdater: TypeAlias = _DependentCallable["Permission"]
+"""PermissionUpdater 在 Matcher.pause, Matcher.reject 时被运行，用于更新会话对象权限。
+默认会更新为当前事件的触发对象。
 
 依赖参数:
 
 - DependParam: 子依赖参数
 - BotParam: Bot 对象
 - EventParam: Event 对象
 - StateParam: State 对象
 - MatcherParam: Matcher 对象
 - DefaultParam: 带有默认值的参数
 """
-T_DependencyCache = Dict[_DependentCallable[Any], "Task[Any]"]
+T_DependencyCache: TypeAlias = Dict[_DependentCallable[Any], "Task[Any]"]
 """依赖缓存, 用于存储依赖函数的返回值"""
```

### Comparing `nonebot2-2.0.0rc4/nonebot/utils.py` & `nonebot2-2.0.1/nonebot/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -8,17 +8,18 @@
 import re
 import json
 import asyncio
 import inspect
 import importlib
 import dataclasses
 from pathlib import Path
+from contextvars import copy_context
 from functools import wraps, partial
 from contextlib import asynccontextmanager
-from typing_extensions import ParamSpec, get_args, get_origin
+from typing_extensions import ParamSpec, get_args, override, get_origin
 from typing import (
     Any,
     Type,
     Tuple,
     Union,
     TypeVar,
     Callable,
@@ -28,15 +29,14 @@
     ContextManager,
     overload,
 )
 
 from pydantic.typing import is_union, is_none_type
 
 from nonebot.log import logger
-from nonebot.typing import overrides
 
 P = ParamSpec("P")
 R = TypeVar("R")
 T = TypeVar("T")
 K = TypeVar("K")
 V = TypeVar("V")
 
@@ -53,28 +53,43 @@
 
 
 def generic_check_issubclass(
     cls: Any, class_or_tuple: Union[Type[Any], Tuple[Type[Any], ...]]
 ) -> bool:
     """检查 cls 是否是 class_or_tuple 中的一个类型子类。
 
-    特别的，如果 cls 是 `typing.Union` 或 `types.UnionType` 类型，
-    则会检查其中的类型是否是 class_or_tuple 中的一个类型子类。（None 会被忽略）
+    特别的：
+
+    - 如果 cls 是 `typing.Union` 或 `types.UnionType` 类型，
+      则会检查其中的所有类型是否是 class_or_tuple 中一个类型的子类或 None。
+    - 如果 cls 是 `typing.TypeVar` 类型，
+      则会检查其 `__bound__` 或 `__constraints__`
+      是否是 class_or_tuple 中一个类型的子类或 None。
     """
     try:
         return issubclass(cls, class_or_tuple)
     except TypeError:
         origin = get_origin(cls)
         if is_union(origin):
             return all(
                 is_none_type(type_) or generic_check_issubclass(type_, class_or_tuple)
                 for type_ in get_args(cls)
             )
+        # ensure generic List, Dict can be checked
         elif origin:
             return issubclass(origin, class_or_tuple)
+        elif isinstance(cls, TypeVar):
+            if cls.__constraints__:
+                return all(
+                    is_none_type(type_)
+                    or generic_check_issubclass(type_, class_or_tuple)
+                    for type_ in cls.__constraints__
+                )
+            elif cls.__bound__:
+                return generic_check_issubclass(cls.__bound__, class_or_tuple)
         return False
 
 
 def is_coroutine_callable(call: Callable[..., Any]) -> bool:
     """检查 call 是否是一个 callable 协程函数"""
     if inspect.isroutine(call):
         return inspect.iscoroutinefunction(call)
@@ -107,15 +122,16 @@
         call: 被装饰的同步函数
     """
 
     @wraps(call)
     async def _wrapper(*args: P.args, **kwargs: P.kwargs) -> R:
         loop = asyncio.get_running_loop()
         pfunc = partial(call, *args, **kwargs)
-        result = await loop.run_in_executor(None, pfunc)
+        context = copy_context()
+        result = await loop.run_in_executor(None, partial(context.run, pfunc))
         return result
 
     return _wrapper
 
 
 @asynccontextmanager
 async def run_sync_ctx_manager(
@@ -132,14 +148,15 @@
         await run_sync(cm.__exit__)(None, None, None)
 
 
 @overload
 async def run_coro_with_catch(
     coro: Coroutine[Any, Any, T],
     exc: Tuple[Type[Exception], ...],
+    return_on_err: None = None,
 ) -> Union[T, None]:
     ...
 
 
 @overload
 async def run_coro_with_catch(
     coro: Coroutine[Any, Any, T],
@@ -150,14 +167,25 @@
 
 
 async def run_coro_with_catch(
     coro: Coroutine[Any, Any, T],
     exc: Tuple[Type[Exception], ...],
     return_on_err: Optional[R] = None,
 ) -> Optional[Union[T, R]]:
+    """运行协程并当遇到指定异常时返回指定值。
+
+    参数:
+        coro: 要运行的协程
+        exc: 要捕获的异常
+        return_on_err: 当发生异常时返回的值
+
+    返回:
+        协程的返回值或发生异常时的指定值
+    """
+
     try:
         return await coro
     except exc:
         return return_on_err
 
 
 def get_name(obj: Any) -> str:
@@ -189,17 +217,17 @@
     instance = module
     for attr_str in cls.split("."):
         instance = getattr(instance, attr_str)
     return instance
 
 
 class DataclassEncoder(json.JSONEncoder):
-    """在JSON序列化 {re}`nonebot.adapters._message.Message` (List[Dataclass]) 时使用的 `JSONEncoder`"""
+    """可以序列化 {ref}`nonebot.adapters.Message`(List[Dataclass]) 的 `JSONEncoder`"""
 
-    @overrides(json.JSONEncoder)
+    @override
     def default(self, o):
         if dataclasses.is_dataclass(o):
             return {f.name: getattr(o, f.name) for f in dataclasses.fields(o)}
         return super().default(o)
 
 
 def logger_wrapper(logger_name: str):
@@ -207,17 +235,19 @@
 
     参数:
         logger_name: adapter 的名称
 
     返回:
         日志记录函数
 
-            - level: 日志等级
-            - message: 日志信息
-            - exception: 异常信息
+        日志记录函数的参数:
+
+        - level: 日志等级
+        - message: 日志信息
+        - exception: 异常信息
     """
 
     def log(level: str, message: str, exception: Optional[Exception] = None):
         logger.opt(colors=True, exception=exception).log(
             level, f"<m>{escape_tag(logger_name)}</m> | {message}"
         )
```

### Comparing `nonebot2-2.0.0rc4/pyproject.toml` & `nonebot2-2.0.1/pyproject.toml`

 * *Files 9% similar despite different names*

```diff
@@ -1,73 +1,79 @@
 [tool.poetry]
 name = "nonebot2"
-version = "2.0.0rc4"
+version = "2.0.1"
 description = "An asynchronous python bot framework."
 authors = ["yanyongyu <yyy@nonebot.dev>"]
 license = "MIT"
 readme = "README.md"
-homepage = "https://v2.nonebot.dev/"
+homepage = "https://nonebot.dev/"
 repository = "https://github.com/nonebot/nonebot2"
-documentation = "https://v2.nonebot.dev/"
+documentation = "https://nonebot.dev/"
 keywords = ["bot", "qq", "qqbot", "mirai", "coolq"]
 classifiers = [
   "Development Status :: 5 - Production/Stable",
   "Framework :: Robot Framework",
   "Framework :: Robot Framework :: Library",
   "Operating System :: OS Independent",
   "Programming Language :: Python :: 3"
 ]
 packages = [
   { include = "nonebot" },
 ]
 include = ["nonebot/py.typed"]
 
+[tool.poetry.urls]
+"Bug Tracker" = "https://github.com/nonebot/nonebot2/issues"
+"Changelog" = "https://nonebot.dev/changelog"
+"Funding" = "https://afdian.net/@nonebot"
+
 [tool.poetry.dependencies]
 python = "^3.8"
 yarl = "^1.7.2"
-loguru = "^0.6.0"
 pygtrie = "^2.4.1"
+loguru = ">=0.6.0,<1.0.0"
 typing-extensions = ">=4.0.0,<5.0.0"
 tomli = { version = "^2.0.1", python = "<3.11" }
 pydantic = { version = "^1.10.0", extras = ["dotenv"] }
 
-websockets = { version = "^10.0", optional = true }
+websockets = { version = ">=10.0", optional = true }
 Quart = { version = ">=0.18.0,<1.0.0", optional = true }
 fastapi = { version = ">=0.93.0,<1.0.0", optional = true }
 aiohttp = { version = "^3.7.4", extras = ["speedups"], optional = true }
 httpx = { version = ">=0.20.0,<1.0.0", extras = ["http2"], optional = true }
 uvicorn = { version = ">=0.20.0,<1.0.0", extras = ["standard"], optional = true }
 
 [tool.poetry.group.dev.dependencies]
-pycln = "^2.1.2"
 isort = "^5.10.1"
 black = "^23.1.0"
 nonemoji = "^0.1.2"
 pre-commit = "^3.0.0"
+ruff = ">=0.0.272,<1.0.0"
 
 [tool.poetry.group.test.dependencies]
 nonebug = "^0.3.0"
+werkzeug = "^2.3.6"
 pytest-cov = "^4.0.0"
 pytest-xdist = "^3.0.2"
 pytest-asyncio = "^0.21.0"
-coverage-conditional-plugin = "^0.8.0"
+coverage-conditional-plugin = "^0.9.0"
 
 [tool.poetry.group.docs.dependencies]
 nb-autodoc = "^1.0.0a5"
 
 [tool.poetry.extras]
 httpx = ["httpx"]
 aiohttp = ["aiohttp"]
 websockets = ["websockets"]
 quart = ["quart", "uvicorn"]
 fastapi = ["fastapi", "uvicorn"]
 all = ["fastapi", "quart", "aiohttp", "httpx", "websockets", "uvicorn"]
 
 [tool.pytest.ini_options]
-asyncio_mode = "auto"
+asyncio_mode = "strict"
 addopts = "--cov=nonebot --cov-append --cov-report=term-missing"
 filterwarnings = [
     "error",
     "ignore::DeprecationWarning",
 ]
 
 [tool.black]
@@ -82,24 +88,33 @@
 line_length = 88
 length_sort = true
 skip_gitignore = true
 force_sort_within_sections = true
 src_paths = ["nonebot", "tests"]
 extra_standard_library = ["typing_extensions"]
 
-[tool.pycln]
-path = "."
-all = false
+[tool.ruff]
+select = ["E", "W", "F", "UP", "C", "T", "PYI", "PT", "Q"]
+ignore = ["E402", "C901"]
+
+line-length = 88
+target-version = "py38"
+
+[tool.ruff.flake8-pytest-style]
+fixture-parentheses = false
+mark-parentheses = false
 
 [tool.pyright]
-reportShadowedImports = false
 pythonVersion = "3.8"
 pythonPlatform = "All"
 executionEnvironments = [
   { root = "./tests", extraPaths = ["./"] },
   { root = "./" },
 ]
 
+typeCheckingMode = "basic"
+reportShadowedImports = false
+
 
 [build-system]
 requires = ["poetry_core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `nonebot2-2.0.0rc4/setup.py` & `nonebot2-2.0.1/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,58 +1,280 @@
-# -*- coding: utf-8 -*-
-from setuptools import setup
+Metadata-Version: 2.1
+Name: nonebot2
+Version: 2.0.1
+Summary: An asynchronous python bot framework.
+Home-page: https://nonebot.dev/
+License: MIT
+Keywords: bot,qq,qqbot,mirai,coolq
+Author: yanyongyu
+Author-email: yyy@nonebot.dev
+Requires-Python: >=3.8,<4.0
+Classifier: Development Status :: 5 - Production/Stable
+Classifier: Framework :: Robot Framework
+Classifier: Framework :: Robot Framework :: Library
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Operating System :: OS Independent
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Provides-Extra: aiohttp
+Provides-Extra: all
+Provides-Extra: fastapi
+Provides-Extra: httpx
+Provides-Extra: quart
+Provides-Extra: websockets
+Requires-Dist: Quart (>=0.18.0,<1.0.0) ; extra == "quart" or extra == "all"
+Requires-Dist: aiohttp[speedups] (>=3.7.4,<4.0.0) ; extra == "aiohttp" or extra == "all"
+Requires-Dist: fastapi (>=0.93.0,<1.0.0) ; extra == "fastapi" or extra == "all"
+Requires-Dist: httpx[http2] (>=0.20.0,<1.0.0) ; extra == "httpx" or extra == "all"
+Requires-Dist: loguru (>=0.6.0,<1.0.0)
+Requires-Dist: pydantic[dotenv] (>=1.10.0,<2.0.0)
+Requires-Dist: pygtrie (>=2.4.1,<3.0.0)
+Requires-Dist: tomli (>=2.0.1,<3.0.0) ; python_version < "3.11"
+Requires-Dist: typing-extensions (>=4.0.0,<5.0.0)
+Requires-Dist: uvicorn[standard] (>=0.20.0,<1.0.0) ; extra == "quart" or extra == "fastapi" or extra == "all"
+Requires-Dist: websockets (>=10.0) ; extra == "websockets" or extra == "all"
+Requires-Dist: yarl (>=1.7.2,<2.0.0)
+Project-URL: Bug Tracker, https://github.com/nonebot/nonebot2/issues
+Project-URL: Changelog, https://nonebot.dev/changelog
+Project-URL: Documentation, https://nonebot.dev/
+Project-URL: Funding, https://afdian.net/@nonebot
+Project-URL: Repository, https://github.com/nonebot/nonebot2
+Description-Content-Type: text/markdown
 
-packages = \
-['nonebot',
- 'nonebot.adapters',
- 'nonebot.dependencies',
- 'nonebot.drivers',
- 'nonebot.internal',
- 'nonebot.internal.adapter',
- 'nonebot.internal.driver',
- 'nonebot.internal.matcher',
- 'nonebot.plugin',
- 'nonebot.plugins']
-
-package_data = \
-{'': ['*']}
-
-install_requires = \
-['loguru>=0.6.0,<0.7.0',
- 'pydantic[dotenv]>=1.10.0,<2.0.0',
- 'pygtrie>=2.4.1,<3.0.0',
- 'typing-extensions>=4.0.0,<5.0.0',
- 'yarl>=1.7.2,<2.0.0']
-
-extras_require = \
-{':python_version < "3.11"': ['tomli>=2.0.1,<3.0.0'],
- 'aiohttp': ['aiohttp[speedups]>=3.7.4,<4.0.0'],
- 'all': ['websockets>=10.0,<11.0',
-         'Quart>=0.18.0,<1.0.0',
-         'fastapi>=0.93.0,<1.0.0',
-         'aiohttp[speedups]>=3.7.4,<4.0.0',
-         'httpx[http2]>=0.20.0,<1.0.0',
-         'uvicorn[standard]>=0.20.0,<1.0.0'],
- 'fastapi': ['fastapi>=0.93.0,<1.0.0', 'uvicorn[standard]>=0.20.0,<1.0.0'],
- 'httpx': ['httpx[http2]>=0.20.0,<1.0.0'],
- 'quart': ['Quart>=0.18.0,<1.0.0', 'uvicorn[standard]>=0.20.0,<1.0.0'],
- 'websockets': ['websockets>=10.0,<11.0']}
-
-setup_kwargs = {
-    'name': 'nonebot2',
-    'version': '2.0.0rc4',
-    'description': 'An asynchronous python bot framework.',
-    'long_description': '<!-- markdownlint-disable MD033 MD041 -->\n<p align="center">\n  <a href="https://v2.nonebot.dev/"><img src="https://v2.nonebot.dev/logo.png" width="200" height="200" alt="nonebot"></a>\n</p>\n\n<div align="center">\n\n# NoneBot\n\n<!-- prettier-ignore-start -->\n<!-- markdownlint-disable-next-line MD036 -->\n_✨ 跨平台 Python 异步机器人框架 ✨_\n<!-- prettier-ignore-end -->\n\n</div>\n\n<p align="center">\n  <a href="https://raw.githubusercontent.com/nonebot/nonebot2/master/LICENSE">\n    <img src="https://img.shields.io/github/license/nonebot/nonebot2" alt="license">\n  </a>\n  <a href="https://pypi.python.org/pypi/nonebot2">\n    <img src="https://img.shields.io/pypi/v/nonebot2" alt="pypi">\n  </a>\n  <img src="https://img.shields.io/badge/python-3.8+-blue" alt="python">\n  <a href="https://codecov.io/gh/nonebot/nonebot2">\n    <img src="https://codecov.io/gh/nonebot/nonebot2/branch/master/graph/badge.svg?token=2P0G0VS7N4" alt="codecov"/>\n  </a>\n  <a href="https://github.com/nonebot/nonebot2/actions/workflows/website-deploy.yml">\n    <img src="https://github.com/nonebot/nonebot2/actions/workflows/website-deploy.yml/badge.svg?branch=master&event=push" alt="site"/>\n  </a>\n  <a href="https://results.pre-commit.ci/latest/github/nonebot/nonebot2/master">\n    <img src="https://results.pre-commit.ci/badge/github/nonebot/nonebot2/master.svg" alt="pre-commit" />\n  </a>\n  <br />\n  <a href="https://onebot.dev/">\n    <img src="https://img.shields.io/badge/OneBot-v11-black?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABABAMAAABYR2ztAAAAIVBMVEUAAAAAAAADAwMHBwceHh4UFBQNDQ0ZGRkoKCgvLy8iIiLWSdWYAAAAAXRSTlMAQObYZgAAAQVJREFUSMftlM0RgjAQhV+0ATYK6i1Xb+iMd0qgBEqgBEuwBOxU2QDKsjvojQPvkJ/ZL5sXkgWrFirK4MibYUdE3OR2nEpuKz1/q8CdNxNQgthZCXYVLjyoDQftaKuniHHWRnPh2GCUetR2/9HsMAXyUT4/3UHwtQT2AggSCGKeSAsFnxBIOuAggdh3AKTL7pDuCyABcMb0aQP7aM4AnAbc/wHwA5D2wDHTTe56gIIOUA/4YYV2e1sg713PXdZJAuncdZMAGkAukU9OAn40O849+0ornPwT93rphWF0mgAbauUrEOthlX8Zu7P5A6kZyKCJy75hhw1Mgr9RAUvX7A3csGqZegEdniCx30c3agAAAABJRU5ErkJggg==" alt="onebot">\n  </a>\n  <a href="https://onebot.dev/">\n    <img src="https://img.shields.io/badge/OneBot-v12-black?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABABAMAAABYR2ztAAAAIVBMVEUAAAAAAAADAwMHBwceHh4UFBQNDQ0ZGRkoKCgvLy8iIiLWSdWYAAAAAXRSTlMAQObYZgAAAQVJREFUSMftlM0RgjAQhV+0ATYK6i1Xb+iMd0qgBEqgBEuwBOxU2QDKsjvojQPvkJ/ZL5sXkgWrFirK4MibYUdE3OR2nEpuKz1/q8CdNxNQgthZCXYVLjyoDQftaKuniHHWRnPh2GCUetR2/9HsMAXyUT4/3UHwtQT2AggSCGKeSAsFnxBIOuAggdh3AKTL7pDuCyABcMb0aQP7aM4AnAbc/wHwA5D2wDHTTe56gIIOUA/4YYV2e1sg713PXdZJAuncdZMAGkAukU9OAn40O849+0ornPwT93rphWF0mgAbauUrEOthlX8Zu7P5A6kZyKCJy75hhw1Mgr9RAUvX7A3csGqZegEdniCx30c3agAAAABJRU5ErkJggg==" alt="onebot">\n  </a>\n  <a href="https://core.telegram.org/bots/api">\n    <img src="https://img.shields.io/badge/telegram-Bot-lightgrey?style=social&logo=telegram" alt="telegram">\n  </a>\n  <a href="https://open.feishu.cn/document/home/index">\n    <img src="https://img.shields.io/badge/%E9%A3%9E%E4%B9%A6-Bot-lightgrey?style=social&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz48c3ZnIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDQ4IDQ4IiBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xNyAyOUMyMSAyOSAyNSAyNi45MzM5IDI4IDIzLjQwNjVDMzYgMTQgNDEuNDI0MiAxNi44MTY2IDQ0IDE3Ljk5OThDMzguNSAyMC45OTk4IDQwLjUgMjkuNjIzMyAzMyAzNS45OTk4QzI4LjM4MiAzOS45MjU5IDIzLjQ5NDUgNDEuMDE0IDE5IDQxQzEyLjUyMzEgNDAuOTc5OSA2Ljg2MjI2IDM3Ljc2MzcgNCAzNS40MDYzVjE2Ljk5OTgiIHN0cm9rZT0iIzMzMyIgc3Ryb2tlLXdpZHRoPSI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz48cGF0aCBkPSJNNS42NDgwOCAxNS44NjY5QzUuMDIyMzEgMTQuOTU2NyAzLjc3NzE1IDE0LjcyNjEgMi44NjY5NCAxNS4zNTE5QzEuOTU2NzMgMTUuOTc3NyAxLjcyNjE1IDE3LjIyMjggMi4zNTE5MiAxOC4xMzMxTDUuNjQ4MDggMTUuODY2OVpNMzYuMDAyMSAzNS43MzA5QzM2Ljk1OCAzNS4xNzc0IDM3LjI4NDMgMzMuOTUzOSAzNi43MzA5IDMyLjk5NzlDMzYuMTc3NCAzMi4wNDIgMzQuOTUzOSAzMS43MTU3IDMzLjk5NzkgMzIuMjY5MUwzNi4wMDIxIDM1LjczMDlaTTIuMzUxOTIgMTguMTMzMUM1LjI0MzUgMjIuMzM5IDEwLjc5OTIgMjguMTQ0IDE2Ljg4NjUgMzIuMjIzOUMxOS45MzQ1IDM0LjI2NjcgMjMuMjE3IDM1Ljk0NiAyNi40NDkgMzYuNzMyNEMyOS42OTQ2IDM3LjUyMiAzMy4wNDUxIDM3LjQ0MjggMzYuMDAyMSAzNS43MzA5TDMzLjk5NzkgMzIuMjY5MUMzMi4yMDQ5IDMzLjMwNzIgMjkuOTkyOSAzMy40NzggMjcuMzk0NyAzMi44NDU4QzI0Ljc4MyAzMi4yMTAzIDIxLjk0MDUgMzAuNzk1OCAxOS4xMTM1IDI4LjkwMTFDMTMuNDUwOCAyNS4xMDYgOC4yNTY1IDE5LjY2MSA1LjY0ODA4IDE1Ljg2NjlMMi4zNTE5MiAxOC4xMzMxWiIgZmlsbD0iIzMzMyIvPjxwYXRoIGQ9Ik0zMy41OTQ1IDE3QzMyLjgzOTggMTQuNzAyNyAzMC44NTQ5IDkuOTQwNTQgMjcuNTk0NSA3SDExLjU5NDVDMTUuMjE3MSAxMC42NzU3IDIzIDE2IDI3IDI0IiBzdHJva2U9IiMzMzMiIHN0cm9rZS13aWR0aD0iNCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+PC9zdmc+" alt="feishu">\n  </a>\n  <a href="https://docs.github.com/en/developers/apps">\n    <img src="https://img.shields.io/badge/GitHub-Bot-181717?style=social&logo=github" alt="github"/>\n  </a>\n  <a href="https://bot.q.qq.com/wiki/">\n    <img src="https://img.shields.io/badge/QQ%E9%A2%91%E9%81%93-Bot-lightgrey?style=social&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMTIuODIgMTMwLjg5Ij48ZyBkYXRhLW5hbWU9IuWbvuWxgiAyIj48ZyBkYXRhLW5hbWU9IuWbvuWxgiAxIj48cGF0aCBkPSJNNTUuNjMgMTMwLjhjLTcgMC0xMy45LjA4LTIwLjg2IDAtMTkuMTUtLjI1LTMxLjcxLTExLjQtMzQuMjItMzAuMy00LjA3LTMwLjY2IDE0LjkzLTU5LjIgNDQuODMtNjYuNjQgMi0uNTEgNS4yMS0uMzEgNS4yMS0xLjYzIDAtMi4xMy4xNC0yLjEzLjE0LTUuNTcgMC0uODktMS4zLTEuNDYtMi4yMi0yLjMxLTYuNzMtNi4yMy03LjY3LTEzLjQxLTEtMjAuMTggNS40LTUuNTIgMTEuODctNS40IDE3LjgtLjU5IDYuNDkgNS4yNiA2LjMxIDEzLjA4LS44NiAyMS0uNjguNzQtMS43OCAxLjYtMS43OCAyLjY3djQuMjFjMCAxLjM1IDIuMiAxLjYyIDQuNzkgMi4zNSAzMS4wOSA4LjY1IDQ4LjE3IDM0LjEzIDQ1IDY2LjM3LTEuNzYgMTguMTUtMTQuNTYgMzAuMjMtMzIuNyAzMC42My04LjAyLjE5LTE2LjA3LS4wMS0yNC4xMy0uMDF6IiBmaWxsPSIjMDI5OWZlIi8+PHBhdGggZD0iTTMxLjQ2IDExOC4zOGMtMTAuNS0uNjktMTYuOC02Ljg2LTE4LjM4LTE3LjI3LTMtMTkuNDIgMi43OC0zNS44NiAxOC40Ni00Ny44MyAxNC4xNi0xMC44IDI5Ljg3LTEyIDQ1LjM4LTMuMTkgMTcuMjUgOS44NCAyNC41OSAyNS44MSAyNCA0NS4yOS0uNDkgMTUuOS04LjQyIDIzLjE0LTI0LjM4IDIzLjUtNi41OS4xNC0xMy4xOSAwLTE5Ljc5IDAiIGZpbGw9IiNmZWZlZmUiLz48cGF0aCBkPSJNNDYuMDUgNzkuNThjLjA5IDUgLjIzIDkuODItNyA5Ljc3LTcuODItLjA2LTYuMS01LjY5LTYuMjQtMTAuMTktLjE1LTQuODItLjczLTEwIDYuNzMtOS44NHM2LjM3IDUuNTUgNi41MSAxMC4yNnoiIGZpbGw9IiMxMDlmZmUiLz48cGF0aCBkPSJNODAuMjcgNzkuMjdjLS41MyAzLjkxIDEuNzUgOS42NC01Ljg4IDEwLTcuNDcuMzctNi44MS00LjgyLTYuNjEtOS41LjItNC4zMi0xLjgzLTEwIDUuNzgtMTAuNDJzNi41OSA0Ljg5IDYuNzEgOS45MnoiIGZpbGw9IiMwODljZmUiLz48L2c+PC9nPjwvc3ZnPg==" alt="QQ频道">\n  <a href="https://ding-doc.dingtalk.com/document#/org-dev-guide/elzz1p">\n    <img src="https://img.shields.io/badge/%E9%92%89%E9%92%89-Bot-lightgrey?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAMAAACdt4HsAAAAnFBMVEUAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD4jUzeAAAAM3RSTlMAQKSRaA+/f0YyFevh29R3cyklIfrlyrGsn41tVUs48c/HqJm9uZdhX1otGwkF9IN8V1CX0Q+IAAABY0lEQVRYw+3V2W7CMBAF0JuNQAhhX9OEfYdu9///rUVWpagE27Ef2gfO+0zGozsKnv6bMGzAhkNytIe5gDdzrwtTCwrbI8x4/NF668NAxgI3Q3UtFi3TyPwNQtPLUUmDd8YfqGLNe4v22XwEYb5zoOuF5baHq2UHtsKe5ivWfGAwrWu2mC34QM0PoCAuqZdOmiwV+5BLyMRtZ7dTSEcs48rzWfzwptMLyzpApka1SJ5FtR4kfCqNIBPEVDmqoqgwUYY5plQOlf6UEjNoOPnuKB6wzDyCrks///TDza8+PnR109WQdxLo8RKWq0PPnuXG0OXKQ6wWLFnCg75uYYbhmMIVVdQ709q33aHbGIj6Duz+2k1HQFX9VwqmY8xYsEJll2ahvhWgsjYLHFRXvIi2Qb0jzMQCzC3FAoydxCma88UCzE3JCWwkjCNYyMUCzHX4DiuTMawEwwhW6hnshPhjZzzJfAH0YacpbmRd7QAAAABJRU5ErkJggg==" alt="dingtalk">\n  </a>\n  </a>\n  <br />\n  <a href="https://jq.qq.com/?_wv=1027&k=5OFifDh">\n    <img src="https://img.shields.io/badge/QQ%E7%BE%A4-768887710-orange?style=flat-square" alt="QQ Chat Group">\n  </a>\n  <a href="https://qun.qq.com/qqweb/qunpro/share?_wv=3&_wwv=128&appChannel=share&inviteCode=7b4a3&appChannel=share&businessType=9&from=246610&biz=ka">\n    <img src="https://img.shields.io/badge/QQ%E9%A2%91%E9%81%93-NoneBot-5492ff?style=flat-square" alt="QQ Channel">\n  </a>\n  <a href="https://t.me/botuniverse">\n    <img src="https://img.shields.io/badge/telegram-botuniverse-blue?style=flat-square" alt="Telegram Channel">\n  </a>\n  <a href="https://discord.gg/VKtE6Gdc4h">\n    <img src="https://discordapp.com/api/guilds/847819937858584596/widget.png?style=shield" alt="Discord Server">\n  </a>\n</p>\n\n<p align="center">\n  <a href="https://v2.nonebot.dev/">文档</a>\n  ·\n  <a href="https://v2.nonebot.dev/docs/quick-start">快速上手</a>\n  ·\n  <a href="#插件">文档打不开？</a>\n</p>\n\n<p align="center">\n  <a href="https://asciinema.org/a/569440">\n    <img src="https://v2.nonebot.dev/img/setup.svg">\n  </a>\n</p>\n\n## 简介\n\nNoneBot2 是一个现代、跨平台、可扩展的 Python 聊天机器人框架，它基于 Python 的类型注解和异步特性，能够为你的需求实现提供便捷灵活的支持。\n\n## 特色\n\n- 异步优先：基于 Python 的异步特性，即使是~~非常~~大量的消息，也能吞吐自如\n- 易于开发：配合 NB-CLI 脚手架，代码编写上手简单，没有过多的冗余代码，可以让开发者专注于业务逻辑\n- 生而可靠：100% 类型注解覆盖，配合编辑器的类型推导功能，能将绝大多数的 Bug 杜绝在编辑器中 ([编辑器支持](https://v2.nonebot.dev/docs/editor-support))\n- 社区丰富：社区用户众多，直接和间接用户超过十万人，每天都有大量的活跃用户 ([社区资源](#社区资源))\n- 海纳百川：一个框架，支持多个聊天软件平台，可自定义通信协议\n\n  |                                 协议名称                                  | 状态 |                                注释                                |\n  | :-----------------------------------------------------------------------: | :--: | :----------------------------------------------------------------: |\n  |                    [OneBot 协议](https://onebot.dev/)                     |  ✅  | 支持 QQ、TG、微信公众号等[平台](https://onebot.dev/ecosystem.html) |\n  |              [Telegram](https://core.telegram.org/bots/api)               |  ✅  |                                                                    |\n  |            [飞书](https://open.feishu.cn/document/home/index)             |  ✅  |                                                                    |\n  |           [GitHub](https://docs.github.com/en/developers/apps)            |  ✅  |                       GitHub APP & OAuth APP                       |\n  |                   [QQ 频道](https://bot.q.qq.com/wiki/)                   |  ✅  |                          官方接口调整较多                          |\n  |                [钉钉](https://open.dingtalk.com/document/)                |  🤗  |                          寻找 Maintainer                           |\n  |                                  Console                                  |  ✅  |                             控制台交互                             |\n  |                  [开黑啦](https://developer.kookapp.cn/)                  |  ↗️  |                             由社区贡献                             |\n  |           [Mirai](https://docs.mirai.mamoe.net/mirai-api-http/)           |  ↗️  |                             由社区贡献                             |\n  |        [Ntchat](https://github.com/JustUndertaker/adapter-ntchat)         |  ↗️  |                             由社区贡献                             |\n  | [MineCraft (Spigot)](https://github.com/17TheWord/nonebot-adapter-spigot) |  ↗️  |                             由社区贡献                             |\n  |        [BiliBili Live](https://github.com/wwweww/adapter-bilibili)        |  ↗️  |                             由社区贡献                             |\n\n- 坚实后盾：支持多种 web 框架，可自定义替换、组合\n\n  |                          驱动框架                          |  类型  |\n  | :--------------------------------------------------------: | :----: |\n  |          [FastAPI](https://fastapi.tiangolo.com/)          | 服务端 |\n  |   [Quart](https://pgjones.gitlab.io/quart/) (异步 Flask)   | 服务端 |\n  |       [aiohttp](https://docs.aiohttp.org/en/stable/)       | 客户端 |\n  |           [httpx](https://www.python-httpx.org/)           | 客户端 |\n  | [websockets](https://websockets.readthedocs.io/en/stable/) | 客户端 |\n\n更多：[概览](https://v2.nonebot.dev/docs/)\n\n## 什么不是 NoneBot2\n\nNoneBot2 不是某个平台或者协议的具体实现，它只负责和已有协议适配器通信，并处理接收到的事件。所以，“NoneBot 有 blabla 平台的 blabla 功能吗？”这种问题是与 NoneBot2 无关的。请在相应平台的功能文档中确认，或与相应平台的协议适配开发者联系。\n\nNoneBot2 不是 NoneBot1 的替代品。事实上，它们都在被积极的维护着。但是，如果你想尝试一些新功能，或者想要支持更多的平台，可以考虑使用 NoneBot2。\n\n> ~~NoneBot2 和 NoneBot1 的区别，就像是 VisualStudio Code 和 VisualStudio 一样~~\n\n## 即刻开始\n\n~~完整~~文档可以在 [这里](https://v2.nonebot.dev/) 查看。\n\n懒得看文档？下面是快速安装指南：\n\n1. 安装 [pipx](https://pypa.github.io/pipx/)\n\n   ```bash\n   python -m pip install --user pipx\n   python -m pipx ensurepath\n   ```\n\n2. 安装脚手架\n\n   ```bash\n   pipx install nb-cli\n   ```\n\n3. 使用脚手架创建项目\n\n   ```bash\n   nb create\n   ```\n\n4. 运行项目\n\n   ```bash\n   nb run\n   ```\n\n## 社区资源\n\n### 常见问题\n\n- [常见问题解答(FAQ)](https://faq.nonebot.dev/)\n- [论坛(Discussion)](https://discussions.nonebot.dev/)\n\n### 教程/实际项目/经验分享\n\n- [awesome-nonebot](https://github.com/nonebot/awesome-nonebot)\n\n### 插件\n\n此外，NoneBot2 还有丰富的官方以及第三方现成的插件供大家使用：\n\n- [NoneBot-Plugin-Docs](https://github.com/nonebot/nonebot2/tree/master/packages/nonebot-plugin-docs)：离线文档至本地项目使用 (别再说文档打不开了！)\n\n  在项目目录下执行：\n\n  ```bash\n  nb plugin install nonebot_plugin_docs\n  ```\n\n  或者尝试以下镜像：\n\n  - [文档镜像(中国境内)](https://nb2.baka.icu)\n  - [文档镜像(Vercel)](https://nonebot2-vercel-mirror.vercel.app)\n\n- 其他插件请查看 [商店](https://v2.nonebot.dev/store)\n\n## 许可证\n\n`NoneBot` 采用 `MIT` 许可证进行开源\n\n```text\nTHE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR\nIMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS\nFOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR\nCOPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER\nIN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN\nCONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.\n```\n\n## 贡献\n\n请参考 [贡献指南](./CONTRIBUTING.md)\n\n### 鸣谢\n\n感谢以下开发者对 NoneBot2 作出的贡献：\n\n<a href="https://github.com/nonebot/nonebot2/graphs/contributors">\n  <img src="https://contrib.rocks/image?repo=nonebot/nonebot2&max=1000" />\n</a>\n',
-    'author': 'yanyongyu',
-    'author_email': 'yyy@nonebot.dev',
-    'maintainer': 'None',
-    'maintainer_email': 'None',
-    'url': 'https://v2.nonebot.dev/',
-    'packages': packages,
-    'package_data': package_data,
-    'install_requires': install_requires,
-    'extras_require': extras_require,
-    'python_requires': '>=3.8,<4.0',
-}
+<!-- markdownlint-disable MD033 MD041 -->
+<p align="center">
+  <a href="https://nonebot.dev/"><img src="https://nonebot.dev/logo.png" width="200" height="200" alt="nonebot"></a>
+</p>
 
+<div align="center">
+
+# NoneBot
+
+<!-- prettier-ignore-start -->
+<!-- markdownlint-disable-next-line MD036 -->
+_✨ 跨平台 Python 异步机器人框架 ✨_
+<!-- prettier-ignore-end -->
+
+</div>
+
+<p align="center">
+  <a href="https://raw.githubusercontent.com/nonebot/nonebot2/master/LICENSE">
+    <img src="https://img.shields.io/github/license/nonebot/nonebot2" alt="license">
+  </a>
+  <a href="https://pypi.python.org/pypi/nonebot2">
+    <img src="https://img.shields.io/pypi/v/nonebot2?logo=python&logoColor=edb641" alt="pypi">
+  </a>
+  <img src="https://img.shields.io/badge/python-3.8+-blue?logo=python&logoColor=edb641" alt="python">
+  <a href="https://github.com/psf/black">
+    <img src="https://img.shields.io/badge/code%20style-black-000000.svg?logo=python&logoColor=edb641" alt="black">
+  </a>
+  <a href="https://github.com/Microsoft/pyright">
+    <img src="https://img.shields.io/badge/types-pyright-797952.svg?logo=python&logoColor=edb641" alt="pyright">
+  </a>
+  <a href="https://github.com/astral-sh/ruff">
+    <img src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/charliermarsh/ruff/main/assets/badge/v2.json" alt="ruff">
+  </a>
+  <br />
+  <a href="https://codecov.io/gh/nonebot/nonebot2">
+    <img src="https://codecov.io/gh/nonebot/nonebot2/branch/master/graph/badge.svg?token=2P0G0VS7N4" alt="codecov"/>
+  </a>
+  <a href="https://github.com/nonebot/nonebot2/actions/workflows/website-deploy.yml">
+    <img src="https://github.com/nonebot/nonebot2/actions/workflows/website-deploy.yml/badge.svg?branch=master&event=push" alt="site"/>
+  </a>
+  <a href="https://results.pre-commit.ci/latest/github/nonebot/nonebot2/master">
+    <img src="https://results.pre-commit.ci/badge/github/nonebot/nonebot2/master.svg" alt="pre-commit" />
+  </a>
+  <a href="https://github.com/nonebot/nonebot2/actions/workflows/pyright.yml">
+    <img src="https://github.com/nonebot/nonebot2/actions/workflows/pyright.yml/badge.svg?branch=master&event=push" alt="pyright">
+  </a>
+  <a href="https://github.com/nonebot/nonebot2/actions/workflows/ruff.yml">
+    <img src="https://github.com/nonebot/nonebot2/actions/workflows/ruff.yml/badge.svg?branch=master&event=push" alt="ruff">
+  </a>
+  <br />
+  <a href="https://onebot.dev/">
+    <img src="https://img.shields.io/badge/OneBot-v11-black?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABABAMAAABYR2ztAAAAIVBMVEUAAAAAAAADAwMHBwceHh4UFBQNDQ0ZGRkoKCgvLy8iIiLWSdWYAAAAAXRSTlMAQObYZgAAAQVJREFUSMftlM0RgjAQhV+0ATYK6i1Xb+iMd0qgBEqgBEuwBOxU2QDKsjvojQPvkJ/ZL5sXkgWrFirK4MibYUdE3OR2nEpuKz1/q8CdNxNQgthZCXYVLjyoDQftaKuniHHWRnPh2GCUetR2/9HsMAXyUT4/3UHwtQT2AggSCGKeSAsFnxBIOuAggdh3AKTL7pDuCyABcMb0aQP7aM4AnAbc/wHwA5D2wDHTTe56gIIOUA/4YYV2e1sg713PXdZJAuncdZMAGkAukU9OAn40O849+0ornPwT93rphWF0mgAbauUrEOthlX8Zu7P5A6kZyKCJy75hhw1Mgr9RAUvX7A3csGqZegEdniCx30c3agAAAABJRU5ErkJggg==" alt="onebot">
+  </a>
+  <a href="https://onebot.dev/">
+    <img src="https://img.shields.io/badge/OneBot-v12-black?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABABAMAAABYR2ztAAAAIVBMVEUAAAAAAAADAwMHBwceHh4UFBQNDQ0ZGRkoKCgvLy8iIiLWSdWYAAAAAXRSTlMAQObYZgAAAQVJREFUSMftlM0RgjAQhV+0ATYK6i1Xb+iMd0qgBEqgBEuwBOxU2QDKsjvojQPvkJ/ZL5sXkgWrFirK4MibYUdE3OR2nEpuKz1/q8CdNxNQgthZCXYVLjyoDQftaKuniHHWRnPh2GCUetR2/9HsMAXyUT4/3UHwtQT2AggSCGKeSAsFnxBIOuAggdh3AKTL7pDuCyABcMb0aQP7aM4AnAbc/wHwA5D2wDHTTe56gIIOUA/4YYV2e1sg713PXdZJAuncdZMAGkAukU9OAn40O849+0ornPwT93rphWF0mgAbauUrEOthlX8Zu7P5A6kZyKCJy75hhw1Mgr9RAUvX7A3csGqZegEdniCx30c3agAAAABJRU5ErkJggg==" alt="onebot">
+  </a>
+  <a href="https://core.telegram.org/bots/api">
+    <img src="https://img.shields.io/badge/telegram-Bot-lightgrey?style=social&logo=telegram" alt="telegram">
+  </a>
+  <a href="https://open.feishu.cn/document/home/index">
+    <img src="https://img.shields.io/badge/%E9%A3%9E%E4%B9%A6-Bot-lightgrey?style=social&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz48c3ZnIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDQ4IDQ4IiBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xNyAyOUMyMSAyOSAyNSAyNi45MzM5IDI4IDIzLjQwNjVDMzYgMTQgNDEuNDI0MiAxNi44MTY2IDQ0IDE3Ljk5OThDMzguNSAyMC45OTk4IDQwLjUgMjkuNjIzMyAzMyAzNS45OTk4QzI4LjM4MiAzOS45MjU5IDIzLjQ5NDUgNDEuMDE0IDE5IDQxQzEyLjUyMzEgNDAuOTc5OSA2Ljg2MjI2IDM3Ljc2MzcgNCAzNS40MDYzVjE2Ljk5OTgiIHN0cm9rZT0iIzMzMyIgc3Ryb2tlLXdpZHRoPSI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz48cGF0aCBkPSJNNS42NDgwOCAxNS44NjY5QzUuMDIyMzEgMTQuOTU2NyAzLjc3NzE1IDE0LjcyNjEgMi44NjY5NCAxNS4zNTE5QzEuOTU2NzMgMTUuOTc3NyAxLjcyNjE1IDE3LjIyMjggMi4zNTE5MiAxOC4xMzMxTDUuNjQ4MDggMTUuODY2OVpNMzYuMDAyMSAzNS43MzA5QzM2Ljk1OCAzNS4xNzc0IDM3LjI4NDMgMzMuOTUzOSAzNi43MzA5IDMyLjk5NzlDMzYuMTc3NCAzMi4wNDIgMzQuOTUzOSAzMS43MTU3IDMzLjk5NzkgMzIuMjY5MUwzNi4wMDIxIDM1LjczMDlaTTIuMzUxOTIgMTguMTMzMUM1LjI0MzUgMjIuMzM5IDEwLjc5OTIgMjguMTQ0IDE2Ljg4NjUgMzIuMjIzOUMxOS45MzQ1IDM0LjI2NjcgMjMuMjE3IDM1Ljk0NiAyNi40NDkgMzYuNzMyNEMyOS42OTQ2IDM3LjUyMiAzMy4wNDUxIDM3LjQ0MjggMzYuMDAyMSAzNS43MzA5TDMzLjk5NzkgMzIuMjY5MUMzMi4yMDQ5IDMzLjMwNzIgMjkuOTkyOSAzMy40NzggMjcuMzk0NyAzMi44NDU4QzI0Ljc4MyAzMi4yMTAzIDIxLjk0MDUgMzAuNzk1OCAxOS4xMTM1IDI4LjkwMTFDMTMuNDUwOCAyNS4xMDYgOC4yNTY1IDE5LjY2MSA1LjY0ODA4IDE1Ljg2NjlMMi4zNTE5MiAxOC4xMzMxWiIgZmlsbD0iIzMzMyIvPjxwYXRoIGQ9Ik0zMy41OTQ1IDE3QzMyLjgzOTggMTQuNzAyNyAzMC44NTQ5IDkuOTQwNTQgMjcuNTk0NSA3SDExLjU5NDVDMTUuMjE3MSAxMC42NzU3IDIzIDE2IDI3IDI0IiBzdHJva2U9IiMzMzMiIHN0cm9rZS13aWR0aD0iNCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+PC9zdmc+" alt="feishu">
+  </a>
+  <a href="https://docs.github.com/en/developers/apps">
+    <img src="https://img.shields.io/badge/GitHub-Bot-181717?style=social&logo=github" alt="github"/>
+  </a>
+  <a href="https://bot.q.qq.com/wiki/">
+    <img src="https://img.shields.io/badge/QQ%E9%A2%91%E9%81%93-Bot-lightgrey?style=social&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMTIuODIgMTMwLjg5Ij48ZyBkYXRhLW5hbWU9IuWbvuWxgiAyIj48ZyBkYXRhLW5hbWU9IuWbvuWxgiAxIj48cGF0aCBkPSJNNTUuNjMgMTMwLjhjLTcgMC0xMy45LjA4LTIwLjg2IDAtMTkuMTUtLjI1LTMxLjcxLTExLjQtMzQuMjItMzAuMy00LjA3LTMwLjY2IDE0LjkzLTU5LjIgNDQuODMtNjYuNjQgMi0uNTEgNS4yMS0uMzEgNS4yMS0xLjYzIDAtMi4xMy4xNC0yLjEzLjE0LTUuNTcgMC0uODktMS4zLTEuNDYtMi4yMi0yLjMxLTYuNzMtNi4yMy03LjY3LTEzLjQxLTEtMjAuMTggNS40LTUuNTIgMTEuODctNS40IDE3LjgtLjU5IDYuNDkgNS4yNiA2LjMxIDEzLjA4LS44NiAyMS0uNjguNzQtMS43OCAxLjYtMS43OCAyLjY3djQuMjFjMCAxLjM1IDIuMiAxLjYyIDQuNzkgMi4zNSAzMS4wOSA4LjY1IDQ4LjE3IDM0LjEzIDQ1IDY2LjM3LTEuNzYgMTguMTUtMTQuNTYgMzAuMjMtMzIuNyAzMC42My04LjAyLjE5LTE2LjA3LS4wMS0yNC4xMy0uMDF6IiBmaWxsPSIjMDI5OWZlIi8+PHBhdGggZD0iTTMxLjQ2IDExOC4zOGMtMTAuNS0uNjktMTYuOC02Ljg2LTE4LjM4LTE3LjI3LTMtMTkuNDIgMi43OC0zNS44NiAxOC40Ni00Ny44MyAxNC4xNi0xMC44IDI5Ljg3LTEyIDQ1LjM4LTMuMTkgMTcuMjUgOS44NCAyNC41OSAyNS44MSAyNCA0NS4yOS0uNDkgMTUuOS04LjQyIDIzLjE0LTI0LjM4IDIzLjUtNi41OS4xNC0xMy4xOSAwLTE5Ljc5IDAiIGZpbGw9IiNmZWZlZmUiLz48cGF0aCBkPSJNNDYuMDUgNzkuNThjLjA5IDUgLjIzIDkuODItNyA5Ljc3LTcuODItLjA2LTYuMS01LjY5LTYuMjQtMTAuMTktLjE1LTQuODItLjczLTEwIDYuNzMtOS44NHM2LjM3IDUuNTUgNi41MSAxMC4yNnoiIGZpbGw9IiMxMDlmZmUiLz48cGF0aCBkPSJNODAuMjcgNzkuMjdjLS41MyAzLjkxIDEuNzUgOS42NC01Ljg4IDEwLTcuNDcuMzctNi44MS00LjgyLTYuNjEtOS41LjItNC4zMi0xLjgzLTEwIDUuNzgtMTAuNDJzNi41OSA0Ljg5IDYuNzEgOS45MnoiIGZpbGw9IiMwODljZmUiLz48L2c+PC9nPjwvc3ZnPg==" alt="QQ频道">
+  </a>
+  <!-- <a href="https://ding-doc.dingtalk.com/document#/org-dev-guide/elzz1p">
+    <img src="https://img.shields.io/badge/%E9%92%89%E9%92%89-Bot-lightgrey?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAMAAACdt4HsAAAAnFBMVEUAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD4jUzeAAAAM3RSTlMAQKSRaA+/f0YyFevh29R3cyklIfrlyrGsn41tVUs48c/HqJm9uZdhX1otGwkF9IN8V1CX0Q+IAAABY0lEQVRYw+3V2W7CMBAF0JuNQAhhX9OEfYdu9///rUVWpagE27Ef2gfO+0zGozsKnv6bMGzAhkNytIe5gDdzrwtTCwrbI8x4/NF668NAxgI3Q3UtFi3TyPwNQtPLUUmDd8YfqGLNe4v22XwEYb5zoOuF5baHq2UHtsKe5ivWfGAwrWu2mC34QM0PoCAuqZdOmiwV+5BLyMRtZ7dTSEcs48rzWfzwptMLyzpApka1SJ5FtR4kfCqNIBPEVDmqoqgwUYY5plQOlf6UEjNoOPnuKB6wzDyCrks///TDza8+PnR109WQdxLo8RKWq0PPnuXG0OXKQ6wWLFnCg75uYYbhmMIVVdQ709q33aHbGIj6Duz+2k1HQFX9VwqmY8xYsEJll2ahvhWgsjYLHFRXvIi2Qb0jzMQCzC3FAoydxCma88UCzE3JCWwkjCNYyMUCzHX4DiuTMawEwwhW6hnshPhjZzzJfAH0YacpbmRd7QAAAABJRU5ErkJggg==" alt="dingtalk"> -->
+  </a>
+  <br />
+  <a href="https://jq.qq.com/?_wv=1027&k=5OFifDh">
+    <img src="https://img.shields.io/badge/QQ%E7%BE%A4-768887710-orange?style=flat-square" alt="QQ Chat Group">
+  </a>
+  <a href="https://qun.qq.com/qqweb/qunpro/share?_wv=3&_wwv=128&appChannel=share&inviteCode=7b4a3&appChannel=share&businessType=9&from=246610&biz=ka">
+    <img src="https://img.shields.io/badge/QQ%E9%A2%91%E9%81%93-NoneBot-5492ff?style=flat-square" alt="QQ Channel">
+  </a>
+  <a href="https://t.me/botuniverse">
+    <img src="https://img.shields.io/badge/telegram-botuniverse-blue?style=flat-square" alt="Telegram Channel">
+  </a>
+  <a href="https://discord.gg/VKtE6Gdc4h">
+    <img src="https://discordapp.com/api/guilds/847819937858584596/widget.png?style=shield" alt="Discord Server">
+  </a>
+</p>
+
+<p align="center">
+  <a href="https://nonebot.dev/">文档</a>
+  ·
+  <a href="https://nonebot.dev/docs/quick-start">快速上手</a>
+  ·
+  <a href="#插件">文档打不开？</a>
+</p>
+
+<p align="center">
+  <a href="https://asciinema.org/a/569440">
+    <img src="https://nonebot.dev/img/setup.svg">
+  </a>
+</p>
+
+## 简介
+
+NoneBot2 是一个现代、跨平台、可扩展的 Python 聊天机器人框架，它基于 Python 的类型注解和异步特性，能够为你的需求实现提供便捷灵活的支持。
+
+## 特色
+
+- 异步优先：基于 Python 的异步特性，即使是~~非常~~大量的消息，也能吞吐自如
+- 易于开发：配合 NB-CLI 脚手架，代码编写上手简单，没有过多的冗余代码，可以让开发者专注于业务逻辑
+- 生而可靠：100% 类型注解覆盖，配合编辑器的类型推导功能，能将绝大多数的 Bug 杜绝在编辑器中 ([编辑器支持](https://nonebot.dev/docs/editor-support))
+- 社区丰富：社区用户众多，直接和间接用户超过十万人，每天都有大量的活跃用户 ([社区资源](#社区资源))
+- 海纳百川：一个框架，支持多个聊天软件平台，可自定义通信协议
+
+  |                                                       协议名称                                                        | 状态 |                                   注释                                    |
+  | :-------------------------------------------------------------------------------------------------------------------: | :--: | :-----------------------------------------------------------------------: |
+  |               OneBot（[仓库](https://github.com/nonebot/adapter-onebot)，[协议](https://onebot.dev/)）                |  ✅  | 支持 QQ、TG、微信公众号、KOOK 等[平台](https://onebot.dev/ecosystem.html) |
+  |      Telegram（[仓库](https://github.com/nonebot/adapter-telegram)，[协议](https://core.telegram.org/bots/api)）      |  ✅  |                                                                           |
+  |     飞书（[仓库](https://github.com/nonebot/adapter-feishu)，[协议](https://open.feishu.cn/document/home/index)）     |  ✅  |                                                                           |
+  |         GitHub（[仓库](https://github.com/nonebot/adapter-github)，[协议](https://docs.github.com/en/apps)）          |  ✅  |                          GitHub APP & OAuth APP                           |
+  |           QQ 频道（[仓库](https://github.com/nonebot/adapter-qqguild)，[协议](https://bot.q.qq.com/wiki/)）           |  ✅  |                             官方接口调整较多                              |
+  |         钉钉（[仓库](https://github.com/nonebot/adapter-ding)，[协议](https://open.dingtalk.com/document/)）          |  🤗  |                        寻找 Maintainer（暂不可用）                        |
+  |                             Console（[仓库](https://github.com/nonebot/adapter-console)）                             |  ✅  |                                控制台交互                                 |
+  |     开黑啦（[仓库](https://github.com/Tian-que/nonebot-adapter-kaiheila)，[协议](https://developer.kookapp.cn/)）     |  ↗️  |                                由社区贡献                                 |
+  | Mirai（[仓库](https://github.com/ieew/nonebot_adapter_mirai2)，[协议](https://docs.mirai.mamoe.net/mirai-api-http/)） |  ↗️  |                            QQ 协议，由社区贡献                            |
+  |                          Ntchat（[仓库](https://github.com/JustUndertaker/adapter-ntchat)）                           |  ↗️  |                           微信协议，由社区贡献                            |
+  |                      MineCraft（[仓库](https://github.com/17TheWord/nonebot-adapter-minecraft)）                      |  ↗️  |                                由社区贡献                                 |
+  |                          BiliBili Live（[仓库](https://github.com/wwweww/adapter-bilibili)）                          |  ↗️  |                                由社区贡献                                 |
+  |                       Walle-Q（[仓库](https://github.com/onebot-walle/nonebot_adapter_walleq)）                       |  ↗️  |                            QQ 协议，由社区贡献                            |
+  |                       Villa（[仓库](https://github.com/CMHopeSunshine/nonebot-adapter-villa)）                        |  ↗️  |                     米游社大别野 Bot 协议，由社区贡献                     |
+
+- 坚实后盾：支持多种 web 框架，可自定义替换、组合
+
+  |                              驱动框架                               |  类型  |
+  | :-----------------------------------------------------------------: | :----: |
+  |              [FastAPI](https://fastapi.tiangolo.com/)               | 服务端 |
+  | [Quart](https://quart.palletsprojects.com/en/latest/)（异步 Flask） | 服务端 |
+  |           [aiohttp](https://docs.aiohttp.org/en/stable/)            | 客户端 |
+  |               [httpx](https://www.python-httpx.org/)                | 客户端 |
+  |     [websockets](https://websockets.readthedocs.io/en/stable/)      | 客户端 |
+
+更多：[概览](https://nonebot.dev/docs/)
+
+## 什么不是 NoneBot2
+
+NoneBot2 不是某个平台或者协议的具体实现，它只负责和已有协议适配器通信，并处理接收到的事件。所以，“NoneBot 有 blabla 平台的 blabla 功能吗？”这种问题是与 NoneBot2 无关的。请在相应平台的功能文档中确认，或与相应平台的协议适配开发者联系。
+
+NoneBot2 不是 NoneBot1 的替代品。事实上，它们都在被积极的维护着。但是，如果你想尝试一些新功能，或者想要支持更多的平台，可以考虑使用 NoneBot2。
+
+> ~~NoneBot2 和 NoneBot1 的区别，就像是 VisualStudio Code 和 VisualStudio 一样~~
+
+## 即刻开始
+
+~~完整~~文档可以在 [这里](https://nonebot.dev/) 查看。
+
+懒得看文档？下面是快速安装指南：
+
+1. 安装 [pipx](https://pypa.github.io/pipx/)
+
+   ```bash
+   python -m pip install --user pipx
+   python -m pipx ensurepath
+   ```
+
+2. 安装脚手架
+
+   ```bash
+   pipx install nb-cli
+   ```
+
+3. 使用脚手架创建项目
+
+   ```bash
+   nb create
+   ```
+
+4. 运行项目
+
+   ```bash
+   nb run
+   ```
+
+## 社区资源
+
+### 常见问题
+
+- [常见问题解答(FAQ)](https://faq.nonebot.dev/)
+- [论坛(Discussion)](https://discussions.nonebot.dev/)
+
+### 教程/实际项目/经验分享
+
+- [awesome-nonebot](https://github.com/nonebot/awesome-nonebot)
+
+### 插件
+
+此外，NoneBot2 还有丰富的官方以及第三方现成的插件供大家使用：
+
+- [NoneBot-Plugin-Docs](https://github.com/nonebot/nonebot2/tree/master/packages/nonebot-plugin-docs)：离线文档至本地项目使用 (别再说文档打不开了！)
+
+  在项目目录下执行：
+
+  ```bash
+  nb plugin install nonebot_plugin_docs
+  ```
+
+  或者尝试以下镜像：
+
+  - [文档镜像(中国境内)](https://nb2.baka.icu)
+  - [文档镜像(Vercel)](https://nonebot2-vercel-mirror.vercel.app)
+
+- 其他插件请查看 [商店](https://nonebot.dev/store)
+
+## 许可证
+
+`NoneBot` 采用 `MIT` 许可证进行开源
+
+```text
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
+FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
+COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
+IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
+CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
+```
+
+## 贡献
+
+请参考 [贡献指南](./CONTRIBUTING.md)
+
+### 鸣谢
+
+感谢以下开发者对 NoneBot2 作出的贡献：
+
+<a href="https://github.com/nonebot/nonebot2/graphs/contributors">
+  <img src="https://contrib.rocks/image?repo=nonebot/nonebot2&max=1000" />
+</a>
 
-setup(**setup_kwargs)
```

#### html2text {}

```diff
@@ -1,109 +1,120 @@
-# -*- coding: utf-8 -*- from setuptools import setup packages = \ ['nonebot',
-'nonebot.adapters', 'nonebot.dependencies', 'nonebot.drivers',
-'nonebot.internal', 'nonebot.internal.adapter', 'nonebot.internal.driver',
-'nonebot.internal.matcher', 'nonebot.plugin', 'nonebot.plugins'] package_data =
-\ {'': ['*']} install_requires = \ ['loguru>=0.6.0,<0.7.0', 'pydantic
-[dotenv]>=1.10.0,<2.0.0', 'pygtrie>=2.4.1,<3.0.0', 'typing-
-extensions>=4.0.0,<5.0.0', 'yarl>=1.7.2,<2.0.0'] extras_require = \ {':
-python_version < "3.11"': ['tomli>=2.0.1,<3.0.0'], 'aiohttp': ['aiohttp
-[speedups]>=3.7.4,<4.0.0'], 'all': ['websockets>=10.0,<11.0',
-'Quart>=0.18.0,<1.0.0', 'fastapi>=0.93.0,<1.0.0', 'aiohttp
-[speedups]>=3.7.4,<4.0.0', 'httpx[http2]>=0.20.0,<1.0.0', 'uvicorn
-[standard]>=0.20.0,<1.0.0'], 'fastapi': ['fastapi>=0.93.0,<1.0.0', 'uvicorn
-[standard]>=0.20.0,<1.0.0'], 'httpx': ['httpx[http2]>=0.20.0,<1.0.0'], 'quart':
-['Quart>=0.18.0,<1.0.0', 'uvicorn[standard]>=0.20.0,<1.0.0'], 'websockets':
-['websockets>=10.0,<11.0']} setup_kwargs = { 'name': 'nonebot2', 'version':
-'2.0.0rc4', 'description': 'An asynchronous python bot framework.',
-'long_description': '\n
-                                \n [nonebot]\n
-\n\n
-  \n\n# NoneBot\n\n\n\n_â¨ è·¨å¹³å° Python å¼æ­¥æºå¨äººæ¡æ¶ â¨_\n\n\n
-\n\n
-\n \n_[license]\n\n \n_[pypi]\n\n [python]\n \n_[codecov]\n\n \n_[site]\n\n \n_
-                               [pre-commit]\n\n
-   \n \n_[onebot]\n\n \n_[onebot]\n\n \n_[telegram]\n\n \n_[feishu]\n\n \n_
-               [github]\n\n \n_[QQé¢é]\n_\n_[dingtalk]\n\n\n
-  \n \n_[QQ_Chat_Group]\n\n \n_[QQ_Channel]\n\n \n_[Telegram_Channel]\n\n \n_
-                             [Discord_Server]\n\n
-\n\n
-           \n ææ¡£\n Â·\n å¿«éä¸æ\n Â·\n ææ¡£æä¸å¼ï¼\n
-\n\n
-               \n \n_[https://v2.nonebot.dev/img/setup.svg]\n\n
-\n\n## ç®ä»\n\nNoneBot2 æ¯ä¸ä¸ªç°ä»£ãè·¨å¹³å°ãå¯æ©å±ç Python
+Metadata-Version: 2.1 Name: nonebot2 Version: 2.0.1 Summary: An asynchronous
+python bot framework. Home-page: https://nonebot.dev/ License: MIT Keywords:
+bot,qq,qqbot,mirai,coolq Author: yanyongyu Author-email: yyy@nonebot.dev
+Requires-Python: >=3.8,<4.0 Classifier: Development Status :: 5 - Production/
+Stable Classifier: Framework :: Robot Framework Classifier: Framework :: Robot
+Framework :: Library Classifier: License :: OSI Approved :: MIT License
+Classifier: Operating System :: OS Independent Classifier: Programming Language
+:: Python :: 3 Classifier: Programming Language :: Python :: 3.8 Classifier:
+Programming Language :: Python :: 3.9 Classifier: Programming Language ::
+Python :: 3.10 Classifier: Programming Language :: Python :: 3.11 Provides-
+Extra: aiohttp Provides-Extra: all Provides-Extra: fastapi Provides-Extra:
+httpx Provides-Extra: quart Provides-Extra: websockets Requires-Dist: Quart
+(>=0.18.0,<1.0.0) ; extra == "quart" or extra == "all" Requires-Dist: aiohttp
+[speedups] (>=3.7.4,<4.0.0) ; extra == "aiohttp" or extra == "all" Requires-
+Dist: fastapi (>=0.93.0,<1.0.0) ; extra == "fastapi" or extra == "all"
+Requires-Dist: httpx[http2] (>=0.20.0,<1.0.0) ; extra == "httpx" or extra ==
+"all" Requires-Dist: loguru (>=0.6.0,<1.0.0) Requires-Dist: pydantic[dotenv]
+(>=1.10.0,<2.0.0) Requires-Dist: pygtrie (>=2.4.1,<3.0.0) Requires-Dist: tomli
+(>=2.0.1,<3.0.0) ; python_version < "3.11" Requires-Dist: typing-extensions
+(>=4.0.0,<5.0.0) Requires-Dist: uvicorn[standard] (>=0.20.0,<1.0.0) ; extra ==
+"quart" or extra == "fastapi" or extra == "all" Requires-Dist: websockets
+(>=10.0) ; extra == "websockets" or extra == "all" Requires-Dist: yarl
+(>=1.7.2,<2.0.0) Project-URL: Bug Tracker, https://github.com/nonebot/nonebot2/
+issues Project-URL: Changelog, https://nonebot.dev/changelog Project-URL:
+Documentation, https://nonebot.dev/ Project-URL: Funding, https://afdian.net/
+@nonebot Project-URL: Repository, https://github.com/nonebot/nonebot2
+Description-Content-Type: text/markdown
+                                   [nonebot]
+         # NoneBot   _â¨ è·¨å¹³å° Python å¼æ­¥æºå¨äººæ¡æ¶ â¨_
+              [license] [pypi] [python] [black] [pyright] [ruff]
+                [codecov] [site] [pre-commit] [pyright] [ruff]
+          [onebot] [onebot] [telegram] [feishu] [github] [QQé¢é]
+
+[QQ_Chat_Group] [QQ_Channel] [Telegram_Channel] [Discord_Server]
+                 ææ¡£ Â· å¿«éä¸æ Â· ææ¡£æä¸å¼ï¼
+                      [https://nonebot.dev/img/setup.svg]
+## ç®ä» NoneBot2 æ¯ä¸ä¸ªç°ä»£ãè·¨å¹³å°ãå¯æ©å±ç Python
 èå¤©æºå¨äººæ¡æ¶ï¼å®åºäº Python
-çç±»åæ³¨è§£åå¼æ­¥ç¹æ§ï¼è½å¤ä¸ºä½ çéæ±å®ç°æä¾ä¾¿æ·çµæ´»çæ¯æã\n\n##
-ç¹è²\n\n- å¼æ­¥ä¼åï¼åºäº Python
-çå¼æ­¥ç¹æ§ï¼å³ä½¿æ¯~~éå¸¸~~å¤§éçæ¶æ¯ï¼ä¹è½ååèªå¦\n-
+çç±»åæ³¨è§£åå¼æ­¥ç¹æ§ï¼è½å¤ä¸ºä½ çéæ±å®ç°æä¾ä¾¿æ·çµæ´»çæ¯æã
+## ç¹è² - å¼æ­¥ä¼åï¼åºäº Python
+çå¼æ­¥ç¹æ§ï¼å³ä½¿æ¯~~éå¸¸~~å¤§éçæ¶æ¯ï¼ä¹è½ååèªå¦ -
 æäºå¼åï¼éå NB-CLI
-èææ¶ï¼ä»£ç ç¼åä¸æç®åï¼æ²¡æè¿å¤çåä½ä»£ç ï¼å¯ä»¥è®©å¼åèä¸æ³¨äºä¸å¡é»è¾\n-
-çèå¯é ï¼100%
+èææ¶ï¼ä»£ç ç¼åä¸æç®åï¼æ²¡æè¿å¤çåä½ä»£ç ï¼å¯ä»¥è®©å¼åèä¸æ³¨äºä¸å¡é»è¾
+- çèå¯é ï¼100%
 ç±»åæ³¨è§£è¦çï¼éåç¼è¾å¨çç±»åæ¨å¯¼åè½ï¼è½å°ç»å¤§å¤æ°ç
-Bug æç»å¨ç¼è¾å¨ä¸­ ([ç¼è¾å¨æ¯æ](https://v2.nonebot.dev/docs/
-editor-support))\n-
+Bug æç»å¨ç¼è¾å¨ä¸­ ([ç¼è¾å¨æ¯æ](https://nonebot.dev/docs/editor-
+support)) -
 ç¤¾åºä¸°å¯ï¼ç¤¾åºç¨æ·ä¼å¤ï¼ç´æ¥åé´æ¥ç¨æ·è¶è¿åä¸äººï¼æ¯å¤©é½æå¤§éçæ´»è·ç¨æ·
-([ç¤¾åºèµæº](#ç¤¾åºèµæº))\n-
-æµ·çº³ç¾å·ï¼ä¸ä¸ªæ¡æ¶ï¼æ¯æå¤ä¸ªèå¤©è½¯ä»¶å¹³å°ï¼å¯èªå®ä¹éä¿¡åè®®\n\n
-| åè®®åç§° | ç¶æ | æ³¨é |\n | :---------------------------------------
---------------------------------: | :--: | :-----------------------------------
------------------------------: |\n | [OneBot åè®®](https://onebot.dev/) | â
-| æ¯æ QQãTGãå¾®ä¿¡å¬ä¼å·ç­[å¹³å°](https://onebot.dev/
-ecosystem.html) |\n | [Telegram](https://core.telegram.org/bots/api) | â |
-|\n | [é£ä¹¦](https://open.feishu.cn/document/home/index) | â | |\n |
-[GitHub](https://docs.github.com/en/developers/apps) | â | GitHub APP & OAuth
-APP |\n | [QQ é¢é](https://bot.q.qq.com/wiki/) | â |
-å®æ¹æ¥å£è°æ´è¾å¤ |\n | [éé](https://open.dingtalk.com/document/) |
-ð¤ | å¯»æ¾ Maintainer |\n | Console | â | æ§å¶å°äº¤äº |\n |
-[å¼é»å¦](https://developer.kookapp.cn/) | âï¸ | ç±ç¤¾åºè´¡ç® |\n |
-[Mirai](https://docs.mirai.mamoe.net/mirai-api-http/) | âï¸ |
-ç±ç¤¾åºè´¡ç® |\n | [Ntchat](https://github.com/JustUndertaker/adapter-
-ntchat) | âï¸ | ç±ç¤¾åºè´¡ç® |\n | [MineCraft (Spigot)](https://
-github.com/17TheWord/nonebot-adapter-spigot) | âï¸ | ç±ç¤¾åºè´¡ç® |\n |
-[BiliBili Live](https://github.com/wwweww/adapter-bilibili) | âï¸ |
-ç±ç¤¾åºè´¡ç® |\n\n- åå®åç¾ï¼æ¯æå¤ç§ web
-æ¡æ¶ï¼å¯èªå®ä¹æ¿æ¢ãç»å\n\n | é©±å¨æ¡æ¶ | ç±»å |\n | :-------
--------------------------------------------------: | :----: |\n | [FastAPI]
-(https://fastapi.tiangolo.com/) | æå¡ç«¯ |\n | [Quart](https://
-pgjones.gitlab.io/quart/) (å¼æ­¥ Flask) | æå¡ç«¯ |\n | [aiohttp](https://
-docs.aiohttp.org/en/stable/) | å®¢æ·ç«¯ |\n | [httpx](https://www.python-
-httpx.org/) | å®¢æ·ç«¯ |\n | [websockets](https://websockets.readthedocs.io/
-en/stable/) | å®¢æ·ç«¯ |\n\næ´å¤ï¼[æ¦è§](https://v2.nonebot.dev/docs/
-)\n\n## ä»ä¹ä¸æ¯ NoneBot2\n\nNoneBot2
+([ç¤¾åºèµæº](#ç¤¾åºèµæº)) -
+æµ·çº³ç¾å·ï¼ä¸ä¸ªæ¡æ¶ï¼æ¯æå¤ä¸ªèå¤©è½¯ä»¶å¹³å°ï¼å¯èªå®ä¹éä¿¡åè®®
+| åè®®åç§° | ç¶æ | æ³¨é | | :-----------------------------------------
+--------------------------------------------------------------------------: | :
+--: | :-----------------------------------------------------------------------:
+| | OneBotï¼[ä»åº](https://github.com/nonebot/adapter-onebot)ï¼[åè®®]
+(https://onebot.dev/)ï¼ | â | æ¯æ QQãTGãå¾®ä¿¡å¬ä¼å·ãKOOK ç­
+[å¹³å°](https://onebot.dev/ecosystem.html) | | Telegramï¼[ä»åº](https://
+github.com/nonebot/adapter-telegram)ï¼[åè®®](https://core.telegram.org/bots/
+api)ï¼ | â | | | é£ä¹¦ï¼[ä»åº](https://github.com/nonebot/adapter-
+feishu)ï¼[åè®®](https://open.feishu.cn/document/home/index)ï¼ | â | | |
+GitHubï¼[ä»åº](https://github.com/nonebot/adapter-github)ï¼[åè®®](https:/
+/docs.github.com/en/apps)ï¼ | â | GitHub APP & OAuth APP | | QQ é¢éï¼
+[ä»åº](https://github.com/nonebot/adapter-qqguild)ï¼[åè®®](https://
+bot.q.qq.com/wiki/)ï¼ | â | å®æ¹æ¥å£è°æ´è¾å¤ | | ééï¼[ä»åº]
+(https://github.com/nonebot/adapter-ding)ï¼[åè®®](https://open.dingtalk.com/
+document/)ï¼ | ð¤ | å¯»æ¾ Maintainerï¼æä¸å¯ç¨ï¼ | | Consoleï¼
+[ä»åº](https://github.com/nonebot/adapter-console)ï¼ | â | æ§å¶å°äº¤äº
+| | å¼é»å¦ï¼[ä»åº](https://github.com/Tian-que/nonebot-adapter-
+kaiheila)ï¼[åè®®](https://developer.kookapp.cn/)ï¼ | âï¸ |
+ç±ç¤¾åºè´¡ç® | | Miraiï¼[ä»åº](https://github.com/ieew/
+nonebot_adapter_mirai2)ï¼[åè®®](https://docs.mirai.mamoe.net/mirai-api-http/
+)ï¼ | âï¸ | QQ åè®®ï¼ç±ç¤¾åºè´¡ç® | | Ntchatï¼[ä»åº](https://
+github.com/JustUndertaker/adapter-ntchat)ï¼ | âï¸ |
+å¾®ä¿¡åè®®ï¼ç±ç¤¾åºè´¡ç® | | MineCraftï¼[ä»åº](https://github.com/
+17TheWord/nonebot-adapter-minecraft)ï¼ | âï¸ | ç±ç¤¾åºè´¡ç® | | BiliBili
+Liveï¼[ä»åº](https://github.com/wwweww/adapter-bilibili)ï¼ | âï¸ |
+ç±ç¤¾åºè´¡ç® | | Walle-Qï¼[ä»åº](https://github.com/onebot-walle/
+nonebot_adapter_walleq)ï¼ | âï¸ | QQ åè®®ï¼ç±ç¤¾åºè´¡ç® | | Villaï¼
+[ä»åº](https://github.com/CMHopeSunshine/nonebot-adapter-villa)ï¼ | âï¸ |
+ç±³æ¸¸ç¤¾å¤§å«é Bot åè®®ï¼ç±ç¤¾åºè´¡ç® | - åå®åç¾ï¼æ¯æå¤ç§
+web æ¡æ¶ï¼å¯èªå®ä¹æ¿æ¢ãç»å | é©±å¨æ¡æ¶ | ç±»å | | :---------
+--------------------------------------------------------: | :----: | |
+[FastAPI](https://fastapi.tiangolo.com/) | æå¡ç«¯ | | [Quart](https://
+quart.palletsprojects.com/en/latest/)ï¼å¼æ­¥ Flaskï¼ | æå¡ç«¯ | |
+[aiohttp](https://docs.aiohttp.org/en/stable/) | å®¢æ·ç«¯ | | [httpx](https://
+www.python-httpx.org/) | å®¢æ·ç«¯ | | [websockets](https://
+websockets.readthedocs.io/en/stable/) | å®¢æ·ç«¯ | æ´å¤ï¼[æ¦è§](https://
+nonebot.dev/docs/) ## ä»ä¹ä¸æ¯ NoneBot2 NoneBot2
 ä¸æ¯æä¸ªå¹³å°æèåè®®çå·ä½å®ç°ï¼å®åªè´è´£åå·²æåè®®ééå¨éä¿¡ï¼å¹¶å¤çæ¥æ¶å°çäºä»¶ãæä»¥ï¼âNoneBot
 æ blabla å¹³å°ç blabla åè½åï¼âè¿ç§é®é¢æ¯ä¸ NoneBot2
-æ å³çãè¯·å¨ç¸åºå¹³å°çåè½ææ¡£ä¸­ç¡®è®¤ï¼æä¸ç¸åºå¹³å°çåè®®ééå¼åèèç³»ã\n\nNoneBot2
-ä¸æ¯ NoneBot1
+æ å³çãè¯·å¨ç¸åºå¹³å°çåè½ææ¡£ä¸­ç¡®è®¤ï¼æä¸ç¸åºå¹³å°çåè®®ééå¼åèèç³»ã
+NoneBot2 ä¸æ¯ NoneBot1
 çæ¿ä»£åãäºå®ä¸ï¼å®ä»¬é½å¨è¢«ç§¯æçç»´æ¤çãä½æ¯ï¼å¦æä½ æ³å°è¯ä¸äºæ°åè½ï¼æèæ³è¦æ¯ææ´å¤çå¹³å°ï¼å¯ä»¥èèä½¿ç¨
-NoneBot2ã\n\n> ~~NoneBot2 å NoneBot1 çåºå«ï¼å°±åæ¯ VisualStudio
-Code å VisualStudio ä¸æ ·~~\n\n## å³å»å¼å§\n\n~~å®æ´~~ææ¡£å¯ä»¥å¨
-[è¿é](https://v2.nonebot.dev/
-) æ¥çã\n\næå¾çææ¡£ï¼ä¸é¢æ¯å¿«éå®è£æåï¼\n\n1. å®è£
-[pipx](https://pypa.github.io/pipx/)\n\n ```bash\n python -m pip install --user
-pipx\n python -m pipx ensurepath\n ```\n\n2. å®è£èææ¶\n\n ```bash\n pipx
-install nb-cli\n ```\n\n3. ä½¿ç¨èææ¶åå»ºé¡¹ç®\n\n ```bash\n nb
-create\n ```\n\n4. è¿è¡é¡¹ç®\n\n ```bash\n nb run\n ```\n\n##
-ç¤¾åºèµæº\n\n### å¸¸è§é®é¢\n\n- [å¸¸è§é®é¢è§£ç­(FAQ)](https://
-faq.nonebot.dev/)\n- [è®ºå(Discussion)](https://discussions.nonebot.dev/
-)\n\n### æç¨/å®éé¡¹ç®/ç»éªåäº«\n\n- [awesome-nonebot](https://
-github.com/nonebot/awesome-nonebot)\n\n### æä»¶\n\næ­¤å¤ï¼NoneBot2
-è¿æä¸°å¯çå®æ¹ä»¥åç¬¬ä¸æ¹ç°æçæä»¶ä¾å¤§å®¶ä½¿ç¨ï¼\n\n-
+NoneBot2ã > ~~NoneBot2 å NoneBot1 çåºå«ï¼å°±åæ¯ VisualStudio Code
+å VisualStudio ä¸æ ·~~ ## å³å»å¼å§ ~~å®æ´~~ææ¡£å¯ä»¥å¨ [è¿é]
+(https://nonebot.dev/) æ¥çã
+æå¾çææ¡£ï¼ä¸é¢æ¯å¿«éå®è£æåï¼ 1. å®è£ [pipx](https://
+pypa.github.io/pipx/) ```bash python -m pip install --user pipx python -m pipx
+ensurepath ``` 2. å®è£èææ¶ ```bash pipx install nb-cli ``` 3.
+ä½¿ç¨èææ¶åå»ºé¡¹ç® ```bash nb create ``` 4. è¿è¡é¡¹ç® ```bash nb
+run ``` ## ç¤¾åºèµæº ### å¸¸è§é®é¢ - [å¸¸è§é®é¢è§£ç­(FAQ)](https://
+faq.nonebot.dev/) - [è®ºå(Discussion)](https://discussions.nonebot.dev/) ###
+æç¨/å®éé¡¹ç®/ç»éªåäº« - [awesome-nonebot](https://github.com/
+nonebot/awesome-nonebot) ### æä»¶ æ­¤å¤ï¼NoneBot2
+è¿æä¸°å¯çå®æ¹ä»¥åç¬¬ä¸æ¹ç°æçæä»¶ä¾å¤§å®¶ä½¿ç¨ï¼ -
 [NoneBot-Plugin-Docs](https://github.com/nonebot/nonebot2/tree/master/packages/
 nonebot-plugin-docs)ï¼ç¦»çº¿ææ¡£è³æ¬å°é¡¹ç®ä½¿ç¨
-(å«åè¯´ææ¡£æä¸å¼äºï¼)\n\n å¨é¡¹ç®ç®å½ä¸æ§è¡ï¼\n\n ```bash\n
-nb plugin install nonebot_plugin_docs\n ```\n\n æèå°è¯ä»¥ä¸éåï¼\n\n
-- [ææ¡£éå(ä¸­å½å¢å)](https://nb2.baka.icu)\n - [ææ¡£éå(Vercel)]
-(https://nonebot2-vercel-mirror.vercel.app)\n\n- å¶ä»æä»¶è¯·æ¥ç [ååº]
-(https://v2.nonebot.dev/store)\n\n## è®¸å¯è¯\n\n`NoneBot` éç¨ `MIT`
-è®¸å¯è¯è¿è¡å¼æº\n\n```text\nTHE SOFTWARE IS PROVIDED "AS IS", WITHOUT
-WARRANTY OF ANY KIND, EXPRESS OR\nIMPLIED, INCLUDING BUT NOT LIMITED TO THE
-WARRANTIES OF MERCHANTABILITY, FITNESS\nFOR A PARTICULAR PURPOSE AND
-NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR\nCOPYRIGHT HOLDERS BE LIABLE
-FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER\nIN AN ACTION OF CONTRACT,
-TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN\nCONNECTION WITH THE SOFTWARE OR
-THE USE OR OTHER DEALINGS IN THE SOFTWARE.\n```\n\n## è´¡ç®\n\nè¯·åè
-[è´¡ç®æå](./CONTRIBUTING.md)\n\n### é¸£è°¢\n\næè°¢ä»¥ä¸å¼åèå¯¹
-NoneBot2 ä½åºçè´¡ç®ï¼\n\n\n_[https://contrib.rocks/image?repo=nonebot/
-nonebot2&max=1000]\n\n', 'author': 'yanyongyu', 'author_email':
-'yyy@nonebot.dev', 'maintainer': 'None', 'maintainer_email': 'None', 'url':
-'https://v2.nonebot.dev/', 'packages': packages, 'package_data': package_data,
-'install_requires': install_requires, 'extras_require': extras_require,
-'python_requires': '>=3.8,<4.0', } setup(**setup_kwargs)
+(å«åè¯´ææ¡£æä¸å¼äºï¼) å¨é¡¹ç®ç®å½ä¸æ§è¡ï¼ ```bash nb plugin
+install nonebot_plugin_docs ``` æèå°è¯ä»¥ä¸éåï¼ - [ææ¡£éå
+(ä¸­å½å¢å)](https://nb2.baka.icu) - [ææ¡£éå(Vercel)](https://
+nonebot2-vercel-mirror.vercel.app) - å¶ä»æä»¶è¯·æ¥ç [ååº](https://
+nonebot.dev/store) ## è®¸å¯è¯ `NoneBot` éç¨ `MIT` è®¸å¯è¯è¿è¡å¼æº
+```text THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
+OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+SOFTWARE. ``` ## è´¡ç® è¯·åè [è´¡ç®æå](./CONTRIBUTING.md) ### é¸£è°¢
+æè°¢ä»¥ä¸å¼åèå¯¹ NoneBot2 ä½åºçè´¡ç®ï¼ [https://contrib.rocks/
+image?repo=nonebot/nonebot2&max=1000]
```

