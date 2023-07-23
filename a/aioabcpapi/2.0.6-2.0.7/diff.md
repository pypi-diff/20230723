# Comparing `tmp/aioabcpapi-2.0.6.tar.gz` & `tmp/aioabcpapi-2.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aioabcpapi-2.0.6.tar", last modified: Sun Jul 16 18:03:00 2023, max compression
+gzip compressed data, was "aioabcpapi-2.0.7.tar", last modified: Sun Jul 23 12:52:38 2023, max compression
```

## Comparing `aioabcpapi-2.0.6.tar` & `aioabcpapi-2.0.7.tar`

### file list

```diff
@@ -1,34 +1,32 @@
-drwxrwxrwx   0        0        0        0 2023-07-16 18:03:00.829148 aioabcpapi-2.0.6/
--rw-rw-rw-   0        0        0     1085 2022-05-10 19:34:18.000000 aioabcpapi-2.0.6/LICENSE
--rw-rw-rw-   0        0        0     5371 2023-07-16 18:03:00.829148 aioabcpapi-2.0.6/PKG-INFO
--rw-rw-rw-   0        0        0     4549 2023-05-08 23:26:33.000000 aioabcpapi-2.0.6/README.md
-drwxrwxrwx   0        0        0        0 2023-07-16 18:03:00.716123 aioabcpapi-2.0.6/aioabcpapi/
--rw-rw-rw-   0        0        0      530 2023-07-16 18:01:38.000000 aioabcpapi-2.0.6/aioabcpapi/__init__.py
--rw-rw-rw-   0        0        0      653 2023-06-23 21:18:29.000000 aioabcpapi-2.0.6/aioabcpapi/abcp.py
--rw-rw-rw-   0        0        0    20655 2023-07-15 19:33:16.000000 aioabcpapi-2.0.6/aioabcpapi/api.py
--rw-rw-rw-   0        0        0     4794 2023-06-24 13:28:13.000000 aioabcpapi-2.0.6/aioabcpapi/base.py
-drwxrwxrwx   0        0        0        0 2023-07-16 18:03:00.782138 aioabcpapi-2.0.6/aioabcpapi/cp/
--rw-rw-rw-   0        0        0        2 2022-07-27 23:21:17.000000 aioabcpapi-2.0.6/aioabcpapi/cp/__init__.py
--rw-rw-rw-   0        0        0   114141 2023-07-15 20:04:31.000000 aioabcpapi-2.0.6/aioabcpapi/cp/admin.py
--rw-rw-rw-   0        0        0      321 2023-06-23 21:51:21.000000 aioabcpapi-2.0.6/aioabcpapi/cp/base.py
--rw-rw-rw-   0        0        0    60771 2023-06-24 10:40:46.000000 aioabcpapi-2.0.6/aioabcpapi/cp/client.py
--rw-rw-rw-   0        0        0      535 2023-03-24 12:28:09.000000 aioabcpapi-2.0.6/aioabcpapi/exceptions.py
-drwxrwxrwx   0        0        0        0 2023-07-16 18:03:00.796143 aioabcpapi-2.0.6/aioabcpapi/ts/
--rw-rw-rw-   0        0        0        0 2022-05-22 19:06:06.000000 aioabcpapi-2.0.6/aioabcpapi/ts/__init__.py
--rw-rw-rw-   0        0        0   126500 2023-07-16 12:15:07.000000 aioabcpapi-2.0.6/aioabcpapi/ts/admin.py
--rw-rw-rw-   0        0        0      668 2023-06-24 10:35:56.000000 aioabcpapi-2.0.6/aioabcpapi/ts/base.py
--rw-rw-rw-   0        0        0    47189 2023-07-16 10:26:02.000000 aioabcpapi-2.0.6/aioabcpapi/ts/client.py
-drwxrwxrwx   0        0        0        0 2023-07-16 18:03:00.814143 aioabcpapi-2.0.6/aioabcpapi/utils/
--rw-rw-rw-   0        0        0        2 2022-12-13 06:33:44.000000 aioabcpapi-2.0.6/aioabcpapi/utils/__init__.py
--rw-rw-rw-   0        0        0      805 2022-12-13 07:00:57.000000 aioabcpapi-2.0.6/aioabcpapi/utils/fields_checker.py
--rw-rw-rw-   0        0        0     9063 2023-06-24 10:35:56.000000 aioabcpapi-2.0.6/aioabcpapi/utils/payload.py
-drwxrwxrwx   0        0        0        0 2023-07-16 18:03:00.745129 aioabcpapi-2.0.6/aioabcpapi.egg-info/
--rw-rw-rw-   0        0        0     5371 2023-07-16 18:03:00.000000 aioabcpapi-2.0.6/aioabcpapi.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      894 2023-07-16 18:03:00.000000 aioabcpapi-2.0.6/aioabcpapi.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-16 18:03:00.000000 aioabcpapi-2.0.6/aioabcpapi.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       72 2023-07-16 18:03:00.000000 aioabcpapi-2.0.6/aioabcpapi.egg-info/requires.txt
--rw-rw-rw-   0        0        0       56 2023-07-16 18:03:00.000000 aioabcpapi-2.0.6/aioabcpapi.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      206 2023-07-16 18:03:00.836149 aioabcpapi-2.0.6/setup.cfg
--rw-rw-rw-   0        0        0     1329 2023-07-16 18:01:38.000000 aioabcpapi-2.0.6/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-16 18:03:00.827147 aioabcpapi-2.0.6/test/
--rw-rw-rw-   0        0        0    15807 2022-08-10 22:50:42.000000 aioabcpapi-2.0.6/test/test_payload.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:52:38.041733 aioabcpapi-2.0.7/
+-rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5218 2023-07-23 12:52:38.041733 aioabcpapi-2.0.7/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4469 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:52:38.033733 aioabcpapi-2.0.7/aioabcpapi/
+-rw-r--r--   0 runner    (1001) docker     (123)      517 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      628 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/abcp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20165 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4828 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:52:38.037733 aioabcpapi-2.0.7/aioabcpapi/cp/
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/cp/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   112490 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/cp/admin.py
+-rw-r--r--   0 runner    (1001) docker     (123)      308 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/cp/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    59872 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/cp/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)      493 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/exceptions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:52:38.037733 aioabcpapi-2.0.7/aioabcpapi/ts/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/ts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   124897 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/ts/admin.py
+-rw-r--r--   0 runner    (1001) docker     (123)      645 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/ts/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)    46799 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/ts/client.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:52:38.041733 aioabcpapi-2.0.7/aioabcpapi/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      790 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/utils/fields_checker.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8839 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/aioabcpapi/utils/payload.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:52:38.037733 aioabcpapi-2.0.7/aioabcpapi.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5218 2023-07-23 12:52:38.000000 aioabcpapi-2.0.7/aioabcpapi.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      591 2023-07-23 12:52:38.000000 aioabcpapi-2.0.7/aioabcpapi.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 12:52:38.000000 aioabcpapi-2.0.7/aioabcpapi.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       76 2023-07-23 12:52:38.000000 aioabcpapi-2.0.7/aioabcpapi.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       56 2023-07-23 12:52:38.000000 aioabcpapi-2.0.7/aioabcpapi.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      197 2023-07-23 12:52:38.041733 aioabcpapi-2.0.7/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1254 2023-07-23 12:52:23.000000 aioabcpapi-2.0.7/setup.py
```

### Comparing `aioabcpapi-2.0.6/PKG-INFO` & `aioabcpapi-2.0.7/PKG-INFO`

 * *Files 13% similar despite different names*

```diff
@@ -1,103 +1,102 @@
-Metadata-Version: 2.1
-Name: aioabcpapi
-Version: 2.0.6
-Summary: Async library for ABCP API
-Home-page: https://github.com/bl4ckm45k/aioabcpapi
-Author: bl4ckm45k
-Author-email: nonpowa@gmail.com
-License: MIT
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
-Classifier: Framework :: AsyncIO
-Classifier: Intended Audience :: Developers
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Operating System :: OS Independent
-Classifier: Topic :: Software Development :: Libraries :: Application Frameworks
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
-## AioAbcpApi
-
-Асинхронная библиотека для [API ABCP](https://www.abcp.ru/wiki/ABCP.API "API ABCP")
-с [asyncio](https://docs.python.org/3/library/asyncio.html "asyncio")
-и [aiohttp](https://github.com/aio-libs/aiohttp "aiohttp")
-
-![](https://img.shields.io/github/stars/bl4ckm45k/aioabcpapi.svg)
-![](https://img.shields.io/github/forks/bl4ckm45k/aioabcpapi.svg)
-![](https://img.shields.io/github/issues/bl4ckm45k/aioabcpapi.svg)
-[![Supported python versions](https://img.shields.io/pypi/pyversions/aioabcpapi.svg)](https://pypi.python.org/pypi/aioabcpapi)
-[![Downloads](https://img.shields.io/pypi/dm/aioabcpapi.svg?)](https://pypi.python.org/pypi/aioabcpapi)
-[![PyPi Package Version](https://img.shields.io/pypi/v/aioabcpapi)](https://pypi.python.org/pypi/aioabcpapi)
-
-
-Присоединяйтесь к [телеграм чату](https://t.me/aioabcpapi "Телеграм чат")
-### Установка
-`pip install aioabcpapi`
-
-### Описание
-
-------------
-
-Все методы максимально приближены к древовидному оформлению [официальной документации](https://www.abcp.ru/wiki/ABCP.API).
-
-Разделяются на `cp` и `ts`, они в свою очередь разделяются на `client` и `admin`, далее для поиска нужного вам метода
-отталкивайтесь от документации [API ABCP](https://www.abcp.ru/wiki/ABCP.API).
-
-Для примера, из документации **TS.Client**, [Обновление позиции в корзине](https://www.abcp.ru/wiki/API.TS.Client#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D0.B5)
-описание операции следующее:
->  Операция: POST /ts/cart/update
-
-Для использования этого метода нам нужно будет обратиться к `await api.ts.client.cart.update()`
-
-### Доступ к API
-
-------------
-[Для API Администратора](https://cp.abcp.ru/?page=allsettings&systemsettings&apiInformation)
-
-Если вы являетесь клиентом магазина на платформе ABCP, обратитесь к вашему менеджеру. (Вам понадобится статический IP адрес)
-
-### Примечание 
-
-------------
-
-Все аргументы времени, такие как `create_time`, `update_time`, `date_start`, `date_end` и прочие, принимают `str` или `datetime`. При передаче `datetime` объект будет преобразован в зависимости от требований метода в `RFC3339` или `"%Y-%m-%d %H:%M:%S"`
-
-### Пример
-
-------------
-
-```python
-import asyncio
-from aioabcpapi import Abcp
-
-host, login, password = 'id33333', 'api@id33333', 'md5hash'
-api = Abcp(host, login, password)
-
-
-async def search_some_parts(article, brand):
-    search_result = await api.cp.client.search.articles(number=article, brand=brand,
-                                                        use_online_stocks=True,
-                                                        disable_online_filtering=True,
-                                                        with_out_analogs=True)
-    for x in search_result:
-        if float(x['price']) < 3000:
-            print('Похоже на чудо, но скорее ошибка прайса. Отключим пока поставщика')
-            await api.cp.admin.distributors.edit_status(x['distributorId'], False)
-        elif float(x['price']) < 37000:
-            await api.cp.client.basket.add(basket_positions={'number': x['article'],
-                                                             'brand': x['brand'],
-                                                             'supplierCode': x['supplierCode'],
-                                                             'itemKey': x['itemKey'],
-                                                             'quantity': 1,
-                                                             'comment': f"Да, РРЦ никто не любит"})
-
-
-if __name__ == '__main__':
-    asyncio.run(search_some_parts('602000600', 'LuK'))
-```
-
-[**Больше примеров**](https://github.com/bl4ckm45k/aioabcpapi/tree/master/examples "Примеры")
+Metadata-Version: 2.1
+Name: aioabcpapi
+Version: 2.0.7
+Summary: Async library for ABCP API
+Home-page: https://github.com/bl4ckm45k/aioabcpapi
+Author: bl4ckm45k
+Author-email: nonpowa@gmail.com
+License: MIT
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Classifier: Framework :: AsyncIO
+Classifier: Intended Audience :: Developers
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Operating System :: OS Independent
+Classifier: Topic :: Software Development :: Libraries :: Application Frameworks
+Requires-Python: >=3.8
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
+## AioAbcpApi
+
+Асинхронная библиотека для [API ABCP](https://www.abcp.ru/wiki/ABCP.API "API ABCP")
+с [asyncio](https://docs.python.org/3/library/asyncio.html "asyncio")
+и [aiohttp](https://github.com/aio-libs/aiohttp "aiohttp")
+
+![](https://img.shields.io/github/stars/bl4ckm45k/aioabcpapi.svg)
+![](https://img.shields.io/github/forks/bl4ckm45k/aioabcpapi.svg)
+![](https://img.shields.io/github/issues/bl4ckm45k/aioabcpapi.svg)
+[![Supported python versions](https://img.shields.io/pypi/pyversions/aioabcpapi.svg)](https://pypi.python.org/pypi/aioabcpapi)
+[![Downloads](https://img.shields.io/pypi/dm/aioabcpapi.svg?)](https://pypi.python.org/pypi/aioabcpapi)
+[![PyPi Package Version](https://img.shields.io/pypi/v/aioabcpapi)](https://pypi.python.org/pypi/aioabcpapi)
+
+
+Присоединяйтесь к [телеграм чату](https://t.me/aioabcpapi "Телеграм чат")
+### Установка
+`pip install aioabcpapi`
+
+### Описание
+
+------------
+
+Все методы максимально приближены к древовидному оформлению [официальной документации](https://www.abcp.ru/wiki/ABCP.API).
+
+Разделяются на `cp` и `ts`, они в свою очередь разделяются на `client` и `admin`, далее для поиска нужного вам метода
+отталкивайтесь от документации [API ABCP](https://www.abcp.ru/wiki/ABCP.API).
+
+Для примера, из документации **TS.Client**, [Обновление позиции в корзине](https://www.abcp.ru/wiki/API.TS.Client#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D0.B5)
+описание операции следующее:
+>  Операция: POST /ts/cart/update
+
+Для использования этого метода нам нужно будет обратиться к `await api.ts.client.cart.update()`
+
+### Доступ к API
+
+------------
+[Для API Администратора](https://cp.abcp.ru/?page=allsettings&systemsettings&apiInformation)
+
+Если вы являетесь клиентом магазина на платформе ABCP, обратитесь к вашему менеджеру. (Вам понадобится статический IP адрес)
+
+### Примечание 
+
+------------
+
+Все аргументы времени, такие как `create_time`, `update_time`, `date_start`, `date_end` и прочие, принимают `str` или `datetime`. При передаче `datetime` объект будет преобразован в зависимости от требований метода в `RFC3339` или `"%Y-%m-%d %H:%M:%S"`
+
+### Пример
+
+------------
+
+```python
+import asyncio
+from aioabcpapi import Abcp
+
+host, login, password = 'id33333', 'api@id33333', 'md5hash'
+api = Abcp(host, login, password)
+
+
+async def search_some_parts(article, brand):
+    search_result = await api.cp.client.search.articles(number=article, brand=brand,
+                                                        use_online_stocks=True,
+                                                        disable_online_filtering=True,
+                                                        with_out_analogs=True)
+    for x in search_result:
+        if float(x['price']) < 3000:
+            print('Похоже на чудо, но скорее ошибка прайса. Отключим пока поставщика')
+            await api.cp.admin.distributors.edit_status(x['distributorId'], False)
+        elif float(x['price']) < 37000:
+            await api.cp.client.basket.add(basket_positions={'number': x['article'],
+                                                             'brand': x['brand'],
+                                                             'supplierCode': x['supplierCode'],
+                                                             'itemKey': x['itemKey'],
+                                                             'quantity': 1,
+                                                             'comment': f"Да, РРЦ никто не любит"})
+
+
+if __name__ == '__main__':
+    asyncio.run(search_some_parts('602000600', 'LuK'))
+```
+
+[**Больше примеров**](https://github.com/bl4ckm45k/aioabcpapi/tree/master/examples "Примеры")
```

### Comparing `aioabcpapi-2.0.6/README.md` & `aioabcpapi-2.0.7/README.md`

 * *Ordering differences only*

 * *Files 6% similar despite different names*

```diff
@@ -1,81 +1,81 @@
-## AioAbcpApi
-
-Асинхронная библиотека для [API ABCP](https://www.abcp.ru/wiki/ABCP.API "API ABCP")
-с [asyncio](https://docs.python.org/3/library/asyncio.html "asyncio")
-и [aiohttp](https://github.com/aio-libs/aiohttp "aiohttp")
-
-![](https://img.shields.io/github/stars/bl4ckm45k/aioabcpapi.svg)
-![](https://img.shields.io/github/forks/bl4ckm45k/aioabcpapi.svg)
-![](https://img.shields.io/github/issues/bl4ckm45k/aioabcpapi.svg)
-[![Supported python versions](https://img.shields.io/pypi/pyversions/aioabcpapi.svg)](https://pypi.python.org/pypi/aioabcpapi)
-[![Downloads](https://img.shields.io/pypi/dm/aioabcpapi.svg?)](https://pypi.python.org/pypi/aioabcpapi)
-[![PyPi Package Version](https://img.shields.io/pypi/v/aioabcpapi)](https://pypi.python.org/pypi/aioabcpapi)
-
-
-Присоединяйтесь к [телеграм чату](https://t.me/aioabcpapi "Телеграм чат")
-### Установка
-`pip install aioabcpapi`
-
-### Описание
-
-------------
-
-Все методы максимально приближены к древовидному оформлению [официальной документации](https://www.abcp.ru/wiki/ABCP.API).
-
-Разделяются на `cp` и `ts`, они в свою очередь разделяются на `client` и `admin`, далее для поиска нужного вам метода
-отталкивайтесь от документации [API ABCP](https://www.abcp.ru/wiki/ABCP.API).
-
-Для примера, из документации **TS.Client**, [Обновление позиции в корзине](https://www.abcp.ru/wiki/API.TS.Client#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D0.B5)
-описание операции следующее:
->  Операция: POST /ts/cart/update
-
-Для использования этого метода нам нужно будет обратиться к `await api.ts.client.cart.update()`
-
-### Доступ к API
-
-------------
-[Для API Администратора](https://cp.abcp.ru/?page=allsettings&systemsettings&apiInformation)
-
-Если вы являетесь клиентом магазина на платформе ABCP, обратитесь к вашему менеджеру. (Вам понадобится статический IP адрес)
-
-### Примечание 
-
-------------
-
-Все аргументы времени, такие как `create_time`, `update_time`, `date_start`, `date_end` и прочие, принимают `str` или `datetime`. При передаче `datetime` объект будет преобразован в зависимости от требований метода в `RFC3339` или `"%Y-%m-%d %H:%M:%S"`
-
-### Пример
-
-------------
-
-```python
-import asyncio
-from aioabcpapi import Abcp
-
-host, login, password = 'id33333', 'api@id33333', 'md5hash'
-api = Abcp(host, login, password)
-
-
-async def search_some_parts(article, brand):
-    search_result = await api.cp.client.search.articles(number=article, brand=brand,
-                                                        use_online_stocks=True,
-                                                        disable_online_filtering=True,
-                                                        with_out_analogs=True)
-    for x in search_result:
-        if float(x['price']) < 3000:
-            print('Похоже на чудо, но скорее ошибка прайса. Отключим пока поставщика')
-            await api.cp.admin.distributors.edit_status(x['distributorId'], False)
-        elif float(x['price']) < 37000:
-            await api.cp.client.basket.add(basket_positions={'number': x['article'],
-                                                             'brand': x['brand'],
-                                                             'supplierCode': x['supplierCode'],
-                                                             'itemKey': x['itemKey'],
-                                                             'quantity': 1,
-                                                             'comment': f"Да, РРЦ никто не любит"})
-
-
-if __name__ == '__main__':
-    asyncio.run(search_some_parts('602000600', 'LuK'))
-```
-
+## AioAbcpApi
+
+Асинхронная библиотека для [API ABCP](https://www.abcp.ru/wiki/ABCP.API "API ABCP")
+с [asyncio](https://docs.python.org/3/library/asyncio.html "asyncio")
+и [aiohttp](https://github.com/aio-libs/aiohttp "aiohttp")
+
+![](https://img.shields.io/github/stars/bl4ckm45k/aioabcpapi.svg)
+![](https://img.shields.io/github/forks/bl4ckm45k/aioabcpapi.svg)
+![](https://img.shields.io/github/issues/bl4ckm45k/aioabcpapi.svg)
+[![Supported python versions](https://img.shields.io/pypi/pyversions/aioabcpapi.svg)](https://pypi.python.org/pypi/aioabcpapi)
+[![Downloads](https://img.shields.io/pypi/dm/aioabcpapi.svg?)](https://pypi.python.org/pypi/aioabcpapi)
+[![PyPi Package Version](https://img.shields.io/pypi/v/aioabcpapi)](https://pypi.python.org/pypi/aioabcpapi)
+
+
+Присоединяйтесь к [телеграм чату](https://t.me/aioabcpapi "Телеграм чат")
+### Установка
+`pip install aioabcpapi`
+
+### Описание
+
+------------
+
+Все методы максимально приближены к древовидному оформлению [официальной документации](https://www.abcp.ru/wiki/ABCP.API).
+
+Разделяются на `cp` и `ts`, они в свою очередь разделяются на `client` и `admin`, далее для поиска нужного вам метода
+отталкивайтесь от документации [API ABCP](https://www.abcp.ru/wiki/ABCP.API).
+
+Для примера, из документации **TS.Client**, [Обновление позиции в корзине](https://www.abcp.ru/wiki/API.TS.Client#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D0.B5)
+описание операции следующее:
+>  Операция: POST /ts/cart/update
+
+Для использования этого метода нам нужно будет обратиться к `await api.ts.client.cart.update()`
+
+### Доступ к API
+
+------------
+[Для API Администратора](https://cp.abcp.ru/?page=allsettings&systemsettings&apiInformation)
+
+Если вы являетесь клиентом магазина на платформе ABCP, обратитесь к вашему менеджеру. (Вам понадобится статический IP адрес)
+
+### Примечание 
+
+------------
+
+Все аргументы времени, такие как `create_time`, `update_time`, `date_start`, `date_end` и прочие, принимают `str` или `datetime`. При передаче `datetime` объект будет преобразован в зависимости от требований метода в `RFC3339` или `"%Y-%m-%d %H:%M:%S"`
+
+### Пример
+
+------------
+
+```python
+import asyncio
+from aioabcpapi import Abcp
+
+host, login, password = 'id33333', 'api@id33333', 'md5hash'
+api = Abcp(host, login, password)
+
+
+async def search_some_parts(article, brand):
+    search_result = await api.cp.client.search.articles(number=article, brand=brand,
+                                                        use_online_stocks=True,
+                                                        disable_online_filtering=True,
+                                                        with_out_analogs=True)
+    for x in search_result:
+        if float(x['price']) < 3000:
+            print('Похоже на чудо, но скорее ошибка прайса. Отключим пока поставщика')
+            await api.cp.admin.distributors.edit_status(x['distributorId'], False)
+        elif float(x['price']) < 37000:
+            await api.cp.client.basket.add(basket_positions={'number': x['article'],
+                                                             'brand': x['brand'],
+                                                             'supplierCode': x['supplierCode'],
+                                                             'itemKey': x['itemKey'],
+                                                             'quantity': 1,
+                                                             'comment': f"Да, РРЦ никто не любит"})
+
+
+if __name__ == '__main__':
+    asyncio.run(search_some_parts('602000600', 'LuK'))
+```
+
 [**Больше примеров**](https://github.com/bl4ckm45k/aioabcpapi/tree/master/examples "Примеры")
```

### Comparing `aioabcpapi-2.0.6/aioabcpapi/api.py` & `aioabcpapi-2.0.7/aioabcpapi/api.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,498 +1,498 @@
-import logging
-import re
-from dataclasses import dataclass
-from http import HTTPStatus
-from typing import Dict, Union
-
-import aiohttp
-
-from .exceptions import UnsupportedHost, PasswordType, UnsupportedLogin, NetworkError, \
-    AbcpAPIError, TeaPot, AbcpNotFoundError
-
-logging.basicConfig(level=logging.INFO)
-logger = logging.getLogger('api')
-
-
-def check_data(host: str, login: str, password: str):
-    regex_md = re.match(r"([a-f\d]{32})", password)
-    if not regex_md:
-        raise PasswordType('Допускаются пароли только в md5 hash')
-    host_id = host.split('.')[0]
-    if login[0:4] == 'api@':
-        return login.split('@')[1] == host_id
-    if host_id[2:].isdigit() and len(host_id) < 10 and host[0:2] == 'id':
-        if login.isdigit() and 4 < len(login) < 14:
-            return False
-        if '@' in login:
-            email = re.match('^[\w.]+@([\w-]+\.)+[\w-]{2,6}$', login, flags=re.IGNORECASE)
-            if not email:
-                raise UnsupportedLogin('Недопустимый логин')
-            return False
-        raise UnsupportedLogin('Недопустимый логин')
-    else:
-        raise UnsupportedHost(f'Имя хоста {host} не поддерживается\n'
-                              f'Допустимые имена:\n'
-                              f'id200.public.api.abcp.ru\n'
-                              f'abcp55333.public.api.abcp.ru')
-
-
-def check_result(method_name: str, content_type: str, status_code: int, body):
-    """
-    Checks whether `result` is a valid API response.
-    A result is considered invalid if:
-    - The server returned an HTTP response code other than 200
-    - The content of the result is invalid JSON.
-    - The method call was unsuccessful (The JSON 'ok' field equals False)
-
-    :param method_name: The name of the method called
-    :param status_code: status code
-    :param content_type: content type of result
-    :param body: result body
-    :return: The result parsed to a JSON dictionary
-    :raises ApiException: if one of the above listed cases is applicable
-    """
-    logger.debug('Response for %s: [%d] "%r"', method_name, status_code, body)
-
-    if content_type != 'application/json':
-        raise NetworkError(f"Invalid response with content type {content_type}: \"{body}\"")
-
-    if HTTPStatus.OK <= status_code <= HTTPStatus.IM_USED:
-        return body
-    elif status_code == HTTPStatus.BAD_REQUEST:
-        raise AbcpAPIError(f"{body['errorMessage']} {body['errorCode']} [{status_code}]")
-    elif status_code == HTTPStatus.NOT_FOUND:
-        if any(method_name == x for x in SEARCH_METHODS):
-            raise AbcpNotFoundError(f"{body['errorMessage']} {body['errorCode']} [{status_code}]")
-        raise AbcpAPIError(f"{body['errorMessage']} {body['errorCode']} [{status_code}]")
-    elif status_code == HTTPStatus.CONFLICT:
-        raise AbcpAPIError(f"{body} [{status_code}]")
-    elif status_code in (HTTPStatus.UNAUTHORIZED, HTTPStatus.FORBIDDEN):
-        raise AbcpAPIError(f"{body} [{status_code}]")
-    elif status_code >= HTTPStatus.INTERNAL_SERVER_ERROR:
-        raise AbcpAPIError(f"{body} [{status_code}]")
-    elif status_code == 418:
-        raise TeaPot("RFC 2324, секция 2.3.2: 418 I'm a teapot")
-
-    raise AbcpAPIError(f"{body} [{status_code}]")
-
-
-async def make_request_json(session, host, method,
-                            data: Dict, headers,
-                            **kwargs):
-    url = f'https://{host}/{method}'
-    try:
-        async with session.post(url, json=data, headers=headers, **kwargs) as response:
-            try:
-                body = await response.json()
-                return check_result(method, response.content_type, response.status, body)
-            except:
-                raise AbcpAPIError(response.text)
-    except aiohttp.ClientError as e:
-        raise NetworkError(f"aiohttp client throws an error: {e.__class__.__name__}: {e}")
-
-
-async def make_request(session, host, method,
-                       data: Union[Dict, aiohttp.FormData],
-                       headers, post,
-                       **kwargs):
-    logger.debug('Make _request: "%s" with data: "%r"', method, data)
-
-    url = f'https://{host}/{method}'
-    try:
-        if post:
-            async with session.post(url, data=data, headers=headers, **kwargs) as response:
-                try:
-                    body = await response.json()
-                except:
-                    body = response.text
-                return check_result(method, response.content_type, response.status, body)
-        else:
-            async with session.get(url, params=data, **kwargs) as response:
-                try:
-                    body = await response.json()
-                except:
-                    body = response.text
-                return check_result(method, response.content_type, response.status, body)
-    except aiohttp.ClientError as e:
-        raise NetworkError(f"aiohttp client throws an error: {e.__class__.__name__}: {e}")
-
-
-class Headers:
-    __json_header = {'Content-Type': 'application/json',
-                     'Accept': 'application/json'}
-    __url_encoded_header = {'Content-Type': 'application/x-www-form-urlencoded',
-                            'Accept': 'application/json'}
-    __multipart_header = None
-
-    def __init__(self):
-        pass
-
-    def json_header(self):
-        return self.__json_header
-
-    def url_encoded_header(self):
-        return self.__url_encoded_header
-
-    def multipart_header(self):
-        return self.__multipart_header
-
-
-class _Methods:
-    class Admin:
-        @dataclass(frozen=True)
-        class Orders:
-            GET_ORDERS_LIST: str = 'cp/orders'
-            GET_ORDER: str = 'cp/order'
-            STATUS_HISTORY: str = 'cp/order/statusHistory'
-            SAVE_ORDER: str = 'cp/order'
-            ONLINE_ORDER: str = 'cp/orders/online'
-
-        @dataclass(frozen=True)
-        class Finance:
-            UPDATE_BALANCE: str = 'cp/finance/userBalance'
-            UPDATE_CREDIT_LIMIT: str = 'cp/finance/creditLimit'
-            UPDATE_FINANCE_INFO: str = 'cp/finance/userInfo'
-            GET_PAYMENTS: str = 'cp/finance/payments'
-            GET_PAYMENTS_LINKS: str = 'cp/finance/paymentOrderLinks'
-            GET_PAYMENTS_ONLINE: str = 'cp/onlinePayments'
-            ADD_PAYMENTS: str = 'cp/finance/payments'
-            DELETE_PAYMENT_LINK: str = 'cp/finance/deleteLinkPayments'
-            LINK_EXISTING_PLAYMENT: str = 'cp/finance/paymentOrderLink'
-            REFUND_PAYMENT: str = 'cp/finance/paymentRefund'
-            GET_RECEIPTS: str = 'komtet/getChecks'
-            GET_PAYMENTS_SETTINGS: str = 'cp/payments/getPaymentMethodSettings'
-            DELETE_PAYMENT: str = 'cp/finance/deletePayments'
-
-        @dataclass(frozen=True)
-        class Users:
-            GET_USERS_LIST: str = 'cp/users'
-            CREATE_USER: str = 'cp/user/new'
-            GET_PROFILES: str = 'cp/users/profiles'
-            EDIT_PROFILE: str = 'cp/users/profile'
-
-            EDIT_USER: str = 'cp/user'
-
-            GET_USER_SHIPMENT_ADDRESS: str = 'cp/user/shipmentAddresses'
-            GET_USER_SHIPMENT_ADDRESS_ZONES: str = 'cp/user/shipmentAddressZones'
-            GET_USER_SHIPMENT_ADDRESS_ZONE: str = 'cp/user/shipmentAddressZones/{}'
-            UPDATE_SHIPMENT_ZONES: str = 'cp/user/shipmentAddressZones'
-            CREATE_SHIPMENT_ZONE: str = 'cp/user/shipmentAddressZones/new'
-            UPDATE_SHIPMENT_ZONE: str = 'cp/user/shipmentAddressZones/{}/update'
-            DELETE_SHIPMENT_ZONE: str = 'cp/user/shipmentAddress/{}/delete'
-            # Garage
-            GET_USERS_CARS: str = 'cp/garage'
-            SMS_SETTINGS: str = 'cp/user/smsSettings'
-
-        @dataclass(frozen=True)
-        class Staff:
-            GET_STAFF: str = 'cp/managers'
-            UPDATE_STAFF: str = 'cp/manager'
-
-        @dataclass(frozen=True)
-        class Statuses:
-            GET_STATUSES: str = 'cp/statuses'
-
-        @dataclass(frozen=True)
-        class Articles:
-            GET_BRANDS: str = 'cp/articles/brands'
-            GET_BRANDS_GROUP: str = 'cp/articles/brandsGroup'
-
-        @dataclass(frozen=True)
-        class Distributors:
-            GET_DISTRIBUTORS_LIST: str = 'cp/distributors'
-            EDIT_DISTRIBUTORS_STATUS: str = 'cp/distributor/status'
-            UPLOAD_PRICE: str = 'cp/distributor/pricelistUpdate'
-
-            GET_SUPPLIER_ROUTES: str = 'cp/routes'
-            UPDATE_ROUTE: str = 'cp/route'
-            UPDATE_ROUTE_STATUS: str = 'cp/routes/status'
-            DELETE_ROUTE: str = 'cp/route/delete'
-            EDIT_SUPPLIER_STATUS_FOR_OFFICE: str = 'cp/offices'
-            GET_OFFICE_SUPPLIERS: str = 'cp/offices'
-
-        @dataclass(frozen=True)
-        class Catalog:
-            INFO = f'cp/catalog/info'
-            SEARCH = f'cp/catalog/search'
-            INFO_BATCH = f'cp/catalog/info/batch'
-
-        @dataclass(frozen=True)
-        class UsersCatalog:
-            UPLOAD: str = 'cp/usercatalogs/{}/upload'
-
-        @dataclass(frozen=True)
-        class Payment:
-            TOKEN: str = 'cp/payment/token'
-            TOP_BALANCE: str = 'cp/payment/top-balance-link'
-
-    class Client:
-        # SEARCH METHODS
-        @dataclass(frozen=True)
-        class Search:
-            BRANDS: str = 'search/brands'
-            ARTICLES: str = 'search/articles'
-            BATCH: str = 'search/batch'
-            HISTORY: str = 'search/history'
-            TIPS: str = 'search/tips'
-            ADVICES: str = 'advices'
-            ADVICES_BATCH: str = 'advices/batch'
-
-        # BASKET METHODS
-        @dataclass(frozen=True)
-        class Basket:
-            BASKETS_LIST: str = 'basket/multibasket'
-            BASKET_ADD: str = 'basket/add'
-            BASKET_CLEAR: str = 'basket/clear'
-            BASKET_CONTENT: str = 'basket/content'
-            BASKET_OPTIONS: str = 'basket/options'
-            PAYMENT_METHODS: str = 'basket/paymentMethods'
-            SHIPMENT_METHOD: str = 'basket/shipmentMethods'
-            SHIPMENT_OFFICES: str = 'basket/shipmentOffices'
-            SHIPMENT_ADDRESS: str = 'basket/shipmentAddresses'
-            SHIPMENT_DATES: str = 'basket/shipmentDates'
-            BASKET_ORDER: str = 'basket/order'
-
-        @dataclass(frozen=True)
-        class Orders:
-            ORDERS_INSTANT: str = 'orders/instant'
-            GET_ORDERS_LIST: str = 'orders/list'
-            GET_ORDERS: str = 'orders'
-            CANCEL_POSITION: str = 'orders/cancelPosition'
-
-        @dataclass(frozen=True)
-        class User:
-            REGISTER: str = 'user/new'
-            ACTIVATION: str = 'user/activation'
-            USER_INFO: str = 'user/info'
-            USER_RESTORE: str = 'user/restore'
-
-        @dataclass(frozen=True)
-        class Garage:
-            USER_GARAGE: str = 'user/garage'
-            GARAGE_CAR: str = 'user/garage/car'
-            GARAGE_ADD: str = 'user/garage/add'
-            GARAGE_UPDATE: str = 'user/garage/update'
-            GARAGE_DELETE: str = 'user/garage/delete'
-
-        @dataclass(frozen=True)
-        class CarTree:
-            CAR_TREE_YEARS: str = 'cartree/years'
-            CAR_TREE_MANUFACTURERS: str = 'cartree/manufacturers'
-            CAR_TREE_MODELS: str = 'cartree/models'
-            CAR_TREE_MODIFICATIONS: str = 'cartree/modifications'
-
-        @dataclass(frozen=True)
-        class Form:
-            FIELDS: str = 'form/fields'
-
-        @dataclass(frozen=True)
-        class Articles:
-            BRANDS: str = 'articles/brands'
-            INFO: str = 'articles/info'
-
-    class TsClient:
-        @dataclass(frozen=True)
-        class GoodReceipts:
-            CREATE: str = 'ts/goodReceipts/create'
-            GET: str = 'ts/goodReceipts/get'
-            GET_POSITIONS: str = 'ts/goodReceipts/getPositions'
-
-        @dataclass(frozen=True)
-        class OrderPickings:
-            GET: str = 'ts/orderPickings/get'
-            GET_POSITIONS: str = 'ts/orderPickings/getGoods'
-
-        @dataclass(frozen=True)
-        class CustomerComplaints:
-            GET: str = 'ts/customerComplaints/get'
-            GET_POSITIONS: str = 'ts/customerComplaints/getPositions'
-            CREATE: str = 'ts/customerComplaints/create'
-            CREATE_POSITION_MULTIPLE: str = 'ts/customerComplaints/createPositionMultiple'
-            UPDATE: str = 'ts/customerComplaints/updatePosition'
-            CANCEL: str = 'ts/customerComplaints/cancelPosition'
-
-        @dataclass(frozen=True)
-        class Orders:
-            CREATE: str = 'ts/orders/createByCart'
-            GET_LIST: str = 'ts/orders/list'
-            GET: str = 'ts/orders/get'
-            REFUSE: str = 'ts/orders/refuse'
-
-        @dataclass(frozen=True)
-        class Cart:
-            CREATE: str = 'ts/cart/create'
-            UPDATE: str = 'ts/cart/update'
-            GET_LIST: str = 'ts/cart/list'
-            EXIST: str = 'ts/cart/exists'
-            SUMMARY: str = 'ts/cart/summary'
-            CLEAR: str = 'ts/cart/clear'
-            DELETE: str = 'ts/cart/deletePositions'
-
-        @dataclass(frozen=True)
-        class Positions:
-            GET: str = 'ts/positions/get'
-            GET_LIST: str = 'ts/positions/list'
-            CANCEL: str = 'ts/positions/cancel'
-            MASS_CANCEL: str = 'ts/positions/massCancel'
-
-        @dataclass(frozen=True)
-        class Agreements:
-            get_list: str = 'cp/ts/agreements/list'
-
-    @dataclass(frozen=True)
-    class TsAdmin:
-        @dataclass(frozen=True)
-        class OrderPickings:
-            FAST_GET_OUT: str = 'cp/ts/orderPickings/fastGetOut'
-            GET: str = 'cp/ts/orderPickings/get'
-            GET_GOODS: str = 'cp/ts/orderPickings/getGoods'
-            CREATE_BY_OLD_POS: str = 'cp/ts/orderPickings/createByOldPos'
-            CHANGE_STATUS: str = 'cp/ts/orderPickings/changeStatus'
-            UPDATE: str = 'cp/ts/orderPickings/update'
-            DELETE_POSITION: str = 'cp/ts/orderPickings/deletePosition'
-
-        @dataclass(frozen=True)
-        class CustomerComplaints:
-            GET: str = 'cp/ts/customerComplaints/get'
-            GET_POSITIONS: str = 'cp/ts/customerComplaints/getPositions'
-            CREATE: str = 'cp/ts/customerComplaints/create'
-            CREATE_POSITION: str = 'cp/ts/customerComplaints/createPosition'
-            CREATE_POSITION_MULTIPLE: str = 'cp/ts/customerComplaints/createPositionMultiple'
-            UPDATE_POSITION: str = 'cp/ts/customerComplaints/updatePosition'
-            CHANGE_STATUS_POSITION: str = 'cp/ts/customerComplaints/changeStatusPosition'
-            UPDATE: str = 'cp/ts/customerComplaints/update'
-            UPDATE_CUSTOM_FILE: str = 'cp/ts/customerComplaints/updateCustomFile'
-
-        class SupplierReturns:
-            @dataclass
-            class Operations:
-                __section: str = '/cp/ts/supplierReturns/operations'
-                LIST: str = f'{__section}/list'
-                SUM: str = f'{__section}/sum'
-                GET: str = f'{__section}/get'
-                CREATE: str = f'{__section}/create'
-                UPDATE: str = f'{__section}/update'
-                DELETE: str = f'{__section}/delete'
-
-            @dataclass
-            class Positions:
-                __section: str = '/cp/ts/supplierReturns/positions'
-                LIST: str = f'{__section}/list'
-                SUM: str = f'{__section}/sum'
-                STATUS: str = f'{__section}/status'
-                GET: str = f'{__section}/get'
-                CREATE_MULTIPLE: str = f'{__section}/createMultiple'
-                SPLIT = f'{__section}/split'
-                UPDATE = f'{__section}/update'
-                CHANGE_STATUS = f'{__section}/changeStatus'
-
-            @dataclass
-            class PositionsAttr:
-                __section: str = '/cp/ts/supplierReturns/positions/attr'
-                CREATE: str = f'{__section}/create'
-                UPDATE: str = f'{__section}/update'
-                DELETE: str = f'{__section}/delete'
-
-        @dataclass(frozen=True)
-        class DistributorOwners:
-            DISTRIBUTOR_OWNERS: str = 'cp/ts/distributorOwners'
-
-        @dataclass(frozen=True)
-        class Orders:
-            __section: str = 'cp/ts/orders'
-            CREATE: str = f'{__section}/create'
-            CREATE_BY_CART: str = f'{__section}/createByCart'
-            LIST: str = f'{__section}/list'
-            GET: str = f'{__section}/get'
-            REFUSE: str = f'{__section}/refuse'
-            UPDATE: str = f'{__section}/update'
-            MERGE: str = f'{__section}/merge'
-            SPLIT: str = f'{__section}/split'
-            REPRICE: str = f'{__section}/reprice'
-            MESSAGES_CREATE: str = f'{__section}/messages/create'
-            MESSAGES_GET_ONE: str = f'{__section}/messages/get'
-            MESSAGES_LIST: str = f'{__section}/messages/list'
-            MESSAGES_UPDATE: str = f'{__section}/messages/update'
-            MESSAGES_DELETE: str = f'{__section}/messages/delete'
-
-        @dataclass(frozen=True)
-        class Cart:
-            CREATE: str = 'cp/ts/cart/create'
-            UPDATE: str = 'cp/ts/cart/update'
-            GET_LIST: str = 'cp/ts/cart/list'
-            EXIST: str = 'cp/ts/cart/exists'
-            SUMMARY: str = 'cp/ts/cart/summary'
-            CLEAR: str = 'cp/ts/cart/clear'
-            DELETE: str = 'cp/ts/cart/delete'
-            TRANSFER: str = 'cp/ts/cart/transfer'
-
-        @dataclass(frozen=True)
-        class Positions:
-            GET: str = 'cp/ts/positions/get'
-            GET_LIST: str = 'cp/ts/positions/list'
-            CREATE: str = 'cp/ts/positions/create'
-            UPDATE: str = 'cp/ts/positions/update'
-            CANCEL: str = 'cp/ts/positions/cancel'
-            MASS_CANCEL: str = 'cp/ts/positions/massCancel'
-            CHANGE_STATUS: str = 'cp/ts/positions/changeStatus'
-            SPLIT: str = 'cp/ts/positions/split'
-            MERGE: str = 'cp/ts/positions/merge'
-            MESSAGES_LIST: str = 'cp/ts/positions/message/list'
-            MESSAGES_GET: str = 'cp/ts/positions/message/get'
-            MESSAGES_CREATE: str = 'cp/ts/positions/message/create'
-            MESSAGES_UPDATE: str = 'cp/ts/positions/message/update'
-            MESSAGES_DELETE: str = 'cp/ts/positions/message/delete'
-
-        @dataclass(frozen=True)
-        class GoodReceipts:
-            CREATE: str = 'cp/ts/goodReceipts/create'
-            GET: str = 'cp/ts/goodReceipts/get'
-            GET_POSITIONS: str = 'cp/ts/goodReceipts/getPositions'
-            UPDATE: str = 'cp/ts/goodReceipts/update'
-            CHANGE_STATUS: str = 'cp/ts/goodReceipts/changeStatus'
-            DELETE: str = 'cp/ts/goodReceipts/delete'
-
-            CREATE_POSITION: str = 'cp/ts/goodReceipts/createPosition'
-            DELETE_POSITION: str = 'cp/ts/goodReceipts/deletePosition'
-            GET_POSITION: str = 'cp/ts/goodReceipts/getPosition'
-            UPDATE_POSITION: str = 'cp/ts/goodReceipts/updatePosition'
-
-        @dataclass(frozen=True)
-        class Tags:
-            LIST: str = 'cp/ts/tags/list'
-            CREATE: str = 'cp/ts/tags/create'
-            DELETE: str = 'cp/ts/tags/delete'
-
-        @dataclass(frozen=True)
-        class TagsRelationships:
-            LIST: str = 'cp/ts/tagsRelationships/list'
-            CREATE: str = 'cp/ts/tagsRelationships/create'
-            DELETE: str = 'cp/ts/tagsRelationships/delete'
-
-        @dataclass(frozen=True)
-        class Payments:
-            GET_LIST: str = 'cp/ts/payments/list'
-            CREATE: str = 'cp/ts/payments/create'
-
-        @dataclass(frozen=True)
-        class PaymentMethods:
-            METHODS_LIST: str = 'cp/ts/paymentMethods/list'
-
-        @dataclass(frozen=True)
-        class Agreements:
-            get_list: str = 'cp/ts/agreements/list'
-
-        @dataclass(frozen=True)
-        class LegalPersons:
-            get_list: str = 'cp/ts/legalPersons/list'
-
-    class VinQu:
-        pass
-
-    class TecDoc:
-        pass
-
-
-SEARCH_METHODS = (_Methods.Client.Search.BRANDS, _Methods.Client.Search.ARTICLES, _Methods.Client.Search.BATCH,
-                  _Methods.Client.Search.HISTORY, _Methods.Client.Search.TIPS, _Methods.Client.Search.ADVICES,
-                  _Methods.Client.Search.ADVICES_BATCH)
+import logging
+import re
+from dataclasses import dataclass
+from http import HTTPStatus
+from typing import Dict, Union
+
+import aiohttp
+
+from .exceptions import UnsupportedHost, PasswordType, UnsupportedLogin, NetworkError, \
+    AbcpAPIError, TeaPot, AbcpNotFoundError
+
+logging.basicConfig(level=logging.INFO)
+logger = logging.getLogger('api')
+
+
+def check_data(host: str, login: str, password: str) -> bool:
+    regex_md = re.match(r"([a-f\d]{32})", password)
+    if not regex_md:
+        raise PasswordType('Допускаются пароли только в md5 hash')
+    host_id = host.split('.')[0]
+    if login[0:4] == 'api@':
+        return login.split('@')[1] == host_id
+    if host_id[2:].isdigit() and len(host_id) < 10 and host[0:2] == 'id':
+        if login.isdigit() and 4 < len(login) < 14:
+            return False
+        if '@' in login:
+            email = re.match('^[\w.]+@([\w-]+\.)+[\w-]{2,6}$', login, flags=re.IGNORECASE)
+            if not email:
+                raise UnsupportedLogin('Недопустимый логин')
+            return False
+        raise UnsupportedLogin('Недопустимый логин')
+    else:
+        raise UnsupportedHost(f'Имя хоста {host} не поддерживается\n'
+                              f'Допустимые имена:\n'
+                              f'id200.public.api.abcp.ru\n'
+                              f'abcp55333.public.api.abcp.ru')
+
+
+def check_result(method_name: str, content_type: str, status_code: int, body):
+    """
+    Checks whether `result` is a valid API response.
+    A result is considered invalid if:
+    - The server returned an HTTP response code other than 200
+    - The content of the result is invalid JSON.
+    - The method call was unsuccessful (The JSON 'ok' field equals False)
+
+    :param method_name: The name of the method called
+    :param status_code: status code
+    :param content_type: content type of result
+    :param body: result body
+    :return: The result parsed to a JSON dictionary
+    :raises ApiException: if one of the above listed cases is applicable
+    """
+    logger.debug('Response for %s: [%d] "%r"', method_name, status_code, body)
+
+    if content_type != 'application/json':
+        raise NetworkError(f"Invalid response with content type {content_type}: \"{body}\"")
+
+    if HTTPStatus.OK <= status_code <= HTTPStatus.IM_USED:
+        return body
+    elif status_code == HTTPStatus.BAD_REQUEST:
+        raise AbcpAPIError(f"{body['errorMessage']} {body['errorCode']} [{status_code}]")
+    elif status_code == HTTPStatus.NOT_FOUND:
+        if any(method_name == x for x in SEARCH_METHODS):
+            raise AbcpNotFoundError(f"{body['errorMessage']} {body['errorCode']} [{status_code}]")
+        raise AbcpAPIError(f"{body['errorMessage']} {body['errorCode']} [{status_code}]")
+    elif status_code == HTTPStatus.CONFLICT:
+        raise AbcpAPIError(f"{body} [{status_code}]")
+    elif status_code in (HTTPStatus.UNAUTHORIZED, HTTPStatus.FORBIDDEN):
+        raise AbcpAPIError(f"{body} [{status_code}]")
+    elif status_code >= HTTPStatus.INTERNAL_SERVER_ERROR:
+        raise AbcpAPIError(f"{body} [{status_code}]")
+    elif status_code == 418:
+        raise TeaPot("RFC 2324, секция 2.3.2: 418 I'm a teapot")
+
+    raise AbcpAPIError(f"{body} [{status_code}]")
+
+
+async def make_request_json(session, host, method,
+                            data: Dict, headers,
+                            **kwargs):
+    url = f'https://{host}/{method}'
+    try:
+        async with session.post(url, json=data, headers=headers, **kwargs) as response:
+            try:
+                body = await response.json()
+                return check_result(method, response.content_type, response.status, body)
+            except:
+                raise AbcpAPIError(response.text)
+    except aiohttp.ClientError as e:
+        raise NetworkError(f"aiohttp client throws an error: {e.__class__.__name__}: {e}")
+
+
+async def make_request(session, host, method,
+                       data: Union[Dict, aiohttp.FormData],
+                       headers, post,
+                       **kwargs):
+    logger.debug('Make _request: "%s" with data: "%r"', method, data)
+
+    url = f'https://{host}/{method}'
+    try:
+        if post:
+            async with session.post(url, data=data, headers=headers, **kwargs) as response:
+                try:
+                    body = await response.json()
+                except:
+                    body = response.text
+                return check_result(method, response.content_type, response.status, body)
+        else:
+            async with session.get(url, params=data, **kwargs) as response:
+                try:
+                    body = await response.json()
+                except:
+                    body = response.text
+                return check_result(method, response.content_type, response.status, body)
+    except aiohttp.ClientError as e:
+        raise NetworkError(f"aiohttp client throws an error: {e.__class__.__name__}: {e}")
+
+
+class Headers:
+    __json_header = {'Content-Type': 'application/json',
+                     'Accept': 'application/json'}
+    __url_encoded_header = {'Content-Type': 'application/x-www-form-urlencoded',
+                            'Accept': 'application/json'}
+    __multipart_header = None
+
+    def __init__(self):
+        pass
+
+    def json_header(self):
+        return self.__json_header
+
+    def url_encoded_header(self):
+        return self.__url_encoded_header
+
+    def multipart_header(self):
+        return self.__multipart_header
+
+
+class _Methods:
+    class Admin:
+        @dataclass(frozen=True)
+        class Orders:
+            GET_ORDERS_LIST: str = 'cp/orders'
+            GET_ORDER: str = 'cp/order'
+            STATUS_HISTORY: str = 'cp/order/statusHistory'
+            SAVE_ORDER: str = 'cp/order'
+            ONLINE_ORDER: str = 'cp/orders/online'
+
+        @dataclass(frozen=True)
+        class Finance:
+            UPDATE_BALANCE: str = 'cp/finance/userBalance'
+            UPDATE_CREDIT_LIMIT: str = 'cp/finance/creditLimit'
+            UPDATE_FINANCE_INFO: str = 'cp/finance/userInfo'
+            GET_PAYMENTS: str = 'cp/finance/payments'
+            GET_PAYMENTS_LINKS: str = 'cp/finance/paymentOrderLinks'
+            GET_PAYMENTS_ONLINE: str = 'cp/onlinePayments'
+            ADD_PAYMENTS: str = 'cp/finance/payments'
+            DELETE_PAYMENT_LINK: str = 'cp/finance/deleteLinkPayments'
+            LINK_EXISTING_PLAYMENT: str = 'cp/finance/paymentOrderLink'
+            REFUND_PAYMENT: str = 'cp/finance/paymentRefund'
+            GET_RECEIPTS: str = 'komtet/getChecks'
+            GET_PAYMENTS_SETTINGS: str = 'cp/payments/getPaymentMethodSettings'
+            DELETE_PAYMENT: str = 'cp/finance/deletePayments'
+
+        @dataclass(frozen=True)
+        class Users:
+            GET_USERS_LIST: str = 'cp/users'
+            CREATE_USER: str = 'cp/user/new'
+            GET_PROFILES: str = 'cp/users/profiles'
+            EDIT_PROFILE: str = 'cp/users/profile'
+
+            EDIT_USER: str = 'cp/user'
+
+            GET_USER_SHIPMENT_ADDRESS: str = 'cp/user/shipmentAddresses'
+            GET_USER_SHIPMENT_ADDRESS_ZONES: str = 'cp/user/shipmentAddressZones'
+            GET_USER_SHIPMENT_ADDRESS_ZONE: str = 'cp/user/shipmentAddressZones/{}'
+            UPDATE_SHIPMENT_ZONES: str = 'cp/user/shipmentAddressZones'
+            CREATE_SHIPMENT_ZONE: str = 'cp/user/shipmentAddressZones/new'
+            UPDATE_SHIPMENT_ZONE: str = 'cp/user/shipmentAddressZones/{}/update'
+            DELETE_SHIPMENT_ZONE: str = 'cp/user/shipmentAddress/{}/delete'
+            # Garage
+            GET_USERS_CARS: str = 'cp/garage'
+            SMS_SETTINGS: str = 'cp/user/smsSettings'
+
+        @dataclass(frozen=True)
+        class Staff:
+            GET_STAFF: str = 'cp/managers'
+            UPDATE_STAFF: str = 'cp/manager'
+
+        @dataclass(frozen=True)
+        class Statuses:
+            GET_STATUSES: str = 'cp/statuses'
+
+        @dataclass(frozen=True)
+        class Articles:
+            GET_BRANDS: str = 'cp/articles/brands'
+            GET_BRANDS_GROUP: str = 'cp/articles/brandsGroup'
+
+        @dataclass(frozen=True)
+        class Distributors:
+            GET_DISTRIBUTORS_LIST: str = 'cp/distributors'
+            EDIT_DISTRIBUTORS_STATUS: str = 'cp/distributor/status'
+            UPLOAD_PRICE: str = 'cp/distributor/pricelistUpdate'
+
+            GET_SUPPLIER_ROUTES: str = 'cp/routes'
+            UPDATE_ROUTE: str = 'cp/route'
+            UPDATE_ROUTE_STATUS: str = 'cp/routes/status'
+            DELETE_ROUTE: str = 'cp/route/delete'
+            EDIT_SUPPLIER_STATUS_FOR_OFFICE: str = 'cp/offices'
+            GET_OFFICE_SUPPLIERS: str = 'cp/offices'
+
+        @dataclass(frozen=True)
+        class Catalog:
+            INFO = f'cp/catalog/info'
+            SEARCH = f'cp/catalog/search'
+            INFO_BATCH = f'cp/catalog/info/batch'
+
+        @dataclass(frozen=True)
+        class UsersCatalog:
+            UPLOAD: str = 'cp/usercatalogs/{}/upload'
+
+        @dataclass(frozen=True)
+        class Payment:
+            TOKEN: str = 'cp/payment/token'
+            TOP_BALANCE: str = 'cp/payment/top-balance-link'
+
+    class Client:
+        # SEARCH METHODS
+        @dataclass(frozen=True)
+        class Search:
+            BRANDS: str = 'search/brands'
+            ARTICLES: str = 'search/articles'
+            BATCH: str = 'search/batch'
+            HISTORY: str = 'search/history'
+            TIPS: str = 'search/tips'
+            ADVICES: str = 'advices'
+            ADVICES_BATCH: str = 'advices/batch'
+
+        # BASKET METHODS
+        @dataclass(frozen=True)
+        class Basket:
+            BASKETS_LIST: str = 'basket/multibasket'
+            BASKET_ADD: str = 'basket/add'
+            BASKET_CLEAR: str = 'basket/clear'
+            BASKET_CONTENT: str = 'basket/content'
+            BASKET_OPTIONS: str = 'basket/options'
+            PAYMENT_METHODS: str = 'basket/paymentMethods'
+            SHIPMENT_METHOD: str = 'basket/shipmentMethods'
+            SHIPMENT_OFFICES: str = 'basket/shipmentOffices'
+            SHIPMENT_ADDRESS: str = 'basket/shipmentAddresses'
+            SHIPMENT_DATES: str = 'basket/shipmentDates'
+            BASKET_ORDER: str = 'basket/order'
+
+        @dataclass(frozen=True)
+        class Orders:
+            ORDERS_INSTANT: str = 'orders/instant'
+            GET_ORDERS_LIST: str = 'orders/list'
+            GET_ORDERS: str = 'orders'
+            CANCEL_POSITION: str = 'orders/cancelPosition'
+
+        @dataclass(frozen=True)
+        class User:
+            REGISTER: str = 'user/new'
+            ACTIVATION: str = 'user/activation'
+            USER_INFO: str = 'user/info'
+            USER_RESTORE: str = 'user/restore'
+
+        @dataclass(frozen=True)
+        class Garage:
+            USER_GARAGE: str = 'user/garage'
+            GARAGE_CAR: str = 'user/garage/car'
+            GARAGE_ADD: str = 'user/garage/add'
+            GARAGE_UPDATE: str = 'user/garage/update'
+            GARAGE_DELETE: str = 'user/garage/delete'
+
+        @dataclass(frozen=True)
+        class CarTree:
+            CAR_TREE_YEARS: str = 'cartree/years'
+            CAR_TREE_MANUFACTURERS: str = 'cartree/manufacturers'
+            CAR_TREE_MODELS: str = 'cartree/models'
+            CAR_TREE_MODIFICATIONS: str = 'cartree/modifications'
+
+        @dataclass(frozen=True)
+        class Form:
+            FIELDS: str = 'form/fields'
+
+        @dataclass(frozen=True)
+        class Articles:
+            BRANDS: str = 'articles/brands'
+            INFO: str = 'articles/info'
+
+    class TsClient:
+        @dataclass(frozen=True)
+        class GoodReceipts:
+            CREATE: str = 'ts/goodReceipts/create'
+            GET: str = 'ts/goodReceipts/get'
+            GET_POSITIONS: str = 'ts/goodReceipts/getPositions'
+
+        @dataclass(frozen=True)
+        class OrderPickings:
+            GET: str = 'ts/orderPickings/get'
+            GET_POSITIONS: str = 'ts/orderPickings/getGoods'
+
+        @dataclass(frozen=True)
+        class CustomerComplaints:
+            GET: str = 'ts/customerComplaints/get'
+            GET_POSITIONS: str = 'ts/customerComplaints/getPositions'
+            CREATE: str = 'ts/customerComplaints/create'
+            CREATE_POSITION_MULTIPLE: str = 'ts/customerComplaints/createPositionMultiple'
+            UPDATE: str = 'ts/customerComplaints/updatePosition'
+            CANCEL: str = 'ts/customerComplaints/cancelPosition'
+
+        @dataclass(frozen=True)
+        class Orders:
+            CREATE: str = 'ts/orders/createByCart'
+            GET_LIST: str = 'ts/orders/list'
+            GET: str = 'ts/orders/get'
+            REFUSE: str = 'ts/orders/refuse'
+
+        @dataclass(frozen=True)
+        class Cart:
+            CREATE: str = 'ts/cart/create'
+            UPDATE: str = 'ts/cart/update'
+            GET_LIST: str = 'ts/cart/list'
+            EXIST: str = 'ts/cart/exists'
+            SUMMARY: str = 'ts/cart/summary'
+            CLEAR: str = 'ts/cart/clear'
+            DELETE: str = 'ts/cart/deletePositions'
+
+        @dataclass(frozen=True)
+        class Positions:
+            GET: str = 'ts/positions/get'
+            GET_LIST: str = 'ts/positions/list'
+            CANCEL: str = 'ts/positions/cancel'
+            MASS_CANCEL: str = 'ts/positions/massCancel'
+
+        @dataclass(frozen=True)
+        class Agreements:
+            get_list: str = 'cp/ts/agreements/list'
+
+    @dataclass(frozen=True)
+    class TsAdmin:
+        @dataclass(frozen=True)
+        class OrderPickings:
+            FAST_GET_OUT: str = 'cp/ts/orderPickings/fastGetOut'
+            GET: str = 'cp/ts/orderPickings/get'
+            GET_GOODS: str = 'cp/ts/orderPickings/getGoods'
+            CREATE_BY_OLD_POS: str = 'cp/ts/orderPickings/createByOldPos'
+            CHANGE_STATUS: str = 'cp/ts/orderPickings/changeStatus'
+            UPDATE: str = 'cp/ts/orderPickings/update'
+            DELETE_POSITION: str = 'cp/ts/orderPickings/deletePosition'
+
+        @dataclass(frozen=True)
+        class CustomerComplaints:
+            GET: str = 'cp/ts/customerComplaints/get'
+            GET_POSITIONS: str = 'cp/ts/customerComplaints/getPositions'
+            CREATE: str = 'cp/ts/customerComplaints/create'
+            CREATE_POSITION: str = 'cp/ts/customerComplaints/createPosition'
+            CREATE_POSITION_MULTIPLE: str = 'cp/ts/customerComplaints/createPositionMultiple'
+            UPDATE_POSITION: str = 'cp/ts/customerComplaints/updatePosition'
+            CHANGE_STATUS_POSITION: str = 'cp/ts/customerComplaints/changeStatusPosition'
+            UPDATE: str = 'cp/ts/customerComplaints/update'
+            UPDATE_CUSTOM_FILE: str = 'cp/ts/customerComplaints/updateCustomFile'
+
+        class SupplierReturns:
+            @dataclass
+            class Operations:
+                __section: str = '/cp/ts/supplierReturns/operations'
+                LIST: str = f'{__section}/list'
+                SUM: str = f'{__section}/sum'
+                GET: str = f'{__section}/get'
+                CREATE: str = f'{__section}/create'
+                UPDATE: str = f'{__section}/update'
+                DELETE: str = f'{__section}/delete'
+
+            @dataclass
+            class Positions:
+                __section: str = '/cp/ts/supplierReturns/positions'
+                LIST: str = f'{__section}/list'
+                SUM: str = f'{__section}/sum'
+                STATUS: str = f'{__section}/status'
+                GET: str = f'{__section}/get'
+                CREATE_MULTIPLE: str = f'{__section}/createMultiple'
+                SPLIT = f'{__section}/split'
+                UPDATE = f'{__section}/update'
+                CHANGE_STATUS = f'{__section}/changeStatus'
+
+            @dataclass
+            class PositionsAttr:
+                __section: str = '/cp/ts/supplierReturns/positions/attr'
+                CREATE: str = f'{__section}/create'
+                UPDATE: str = f'{__section}/update'
+                DELETE: str = f'{__section}/delete'
+
+        @dataclass(frozen=True)
+        class DistributorOwners:
+            DISTRIBUTOR_OWNERS: str = 'cp/ts/distributorOwners'
+
+        @dataclass(frozen=True)
+        class Orders:
+            __section: str = 'cp/ts/orders'
+            CREATE: str = f'{__section}/create'
+            CREATE_BY_CART: str = f'{__section}/createByCart'
+            LIST: str = f'{__section}/list'
+            GET: str = f'{__section}/get'
+            REFUSE: str = f'{__section}/refuse'
+            UPDATE: str = f'{__section}/update'
+            MERGE: str = f'{__section}/merge'
+            SPLIT: str = f'{__section}/split'
+            REPRICE: str = f'{__section}/reprice'
+            MESSAGES_CREATE: str = f'{__section}/messages/create'
+            MESSAGES_GET_ONE: str = f'{__section}/messages/get'
+            MESSAGES_LIST: str = f'{__section}/messages/list'
+            MESSAGES_UPDATE: str = f'{__section}/messages/update'
+            MESSAGES_DELETE: str = f'{__section}/messages/delete'
+
+        @dataclass(frozen=True)
+        class Cart:
+            CREATE: str = 'cp/ts/cart/create'
+            UPDATE: str = 'cp/ts/cart/update'
+            GET_LIST: str = 'cp/ts/cart/list'
+            EXIST: str = 'cp/ts/cart/exists'
+            SUMMARY: str = 'cp/ts/cart/summary'
+            CLEAR: str = 'cp/ts/cart/clear'
+            DELETE: str = 'cp/ts/cart/delete'
+            TRANSFER: str = 'cp/ts/cart/transfer'
+
+        @dataclass(frozen=True)
+        class Positions:
+            GET: str = 'cp/ts/positions/get'
+            GET_LIST: str = 'cp/ts/positions/list'
+            CREATE: str = 'cp/ts/positions/create'
+            UPDATE: str = 'cp/ts/positions/update'
+            CANCEL: str = 'cp/ts/positions/cancel'
+            MASS_CANCEL: str = 'cp/ts/positions/massCancel'
+            CHANGE_STATUS: str = 'cp/ts/positions/changeStatus'
+            SPLIT: str = 'cp/ts/positions/split'
+            MERGE: str = 'cp/ts/positions/merge'
+            MESSAGES_LIST: str = 'cp/ts/positions/message/list'
+            MESSAGES_GET: str = 'cp/ts/positions/message/get'
+            MESSAGES_CREATE: str = 'cp/ts/positions/message/create'
+            MESSAGES_UPDATE: str = 'cp/ts/positions/message/update'
+            MESSAGES_DELETE: str = 'cp/ts/positions/message/delete'
+
+        @dataclass(frozen=True)
+        class GoodReceipts:
+            CREATE: str = 'cp/ts/goodReceipts/create'
+            GET: str = 'cp/ts/goodReceipts/get'
+            GET_POSITIONS: str = 'cp/ts/goodReceipts/getPositions'
+            UPDATE: str = 'cp/ts/goodReceipts/update'
+            CHANGE_STATUS: str = 'cp/ts/goodReceipts/changeStatus'
+            DELETE: str = 'cp/ts/goodReceipts/delete'
+
+            CREATE_POSITION: str = 'cp/ts/goodReceipts/createPosition'
+            DELETE_POSITION: str = 'cp/ts/goodReceipts/deletePosition'
+            GET_POSITION: str = 'cp/ts/goodReceipts/getPosition'
+            UPDATE_POSITION: str = 'cp/ts/goodReceipts/updatePosition'
+
+        @dataclass(frozen=True)
+        class Tags:
+            LIST: str = 'cp/ts/tags/list'
+            CREATE: str = 'cp/ts/tags/create'
+            DELETE: str = 'cp/ts/tags/delete'
+
+        @dataclass(frozen=True)
+        class TagsRelationships:
+            LIST: str = 'cp/ts/tagsRelationships/list'
+            CREATE: str = 'cp/ts/tagsRelationships/create'
+            DELETE: str = 'cp/ts/tagsRelationships/delete'
+
+        @dataclass(frozen=True)
+        class Payments:
+            GET_LIST: str = 'cp/ts/payments/list'
+            CREATE: str = 'cp/ts/payments/create'
+
+        @dataclass(frozen=True)
+        class PaymentMethods:
+            METHODS_LIST: str = 'cp/ts/paymentMethods/list'
+
+        @dataclass(frozen=True)
+        class Agreements:
+            get_list: str = 'cp/ts/agreements/list'
+
+        @dataclass(frozen=True)
+        class LegalPersons:
+            get_list: str = 'cp/ts/legalPersons/list'
+
+    class VinQu:
+        pass
+
+    class TecDoc:
+        pass
+
+
+SEARCH_METHODS = (_Methods.Client.Search.BRANDS, _Methods.Client.Search.ARTICLES, _Methods.Client.Search.BATCH,
+                  _Methods.Client.Search.HISTORY, _Methods.Client.Search.TIPS, _Methods.Client.Search.ADVICES,
+                  _Methods.Client.Search.ADVICES_BATCH)
```

### Comparing `aioabcpapi-2.0.6/aioabcpapi/base.py` & `aioabcpapi-2.0.7/aioabcpapi/base.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,129 +1,131 @@
-import asyncio
-import logging
-import ssl
-from typing import Dict, List, Optional, Union, Type
-
-import aiohttp
-import certifi
-import ujson as json
-from aiohttp import FormData
-
-from . import api
-from .api import Headers, _Methods
-from .exceptions import NotEnoughRights
-
-logging.basicConfig(level=logging.INFO)
-logger = logging.getLogger('base')
-
-
-class BaseAbcp:
-
-    def __init__(
-            self,
-            host: str,
-            login: str,
-            password: str,
-            loop: Optional[Union[asyncio.BaseEventLoop, asyncio.AbstractEventLoop]] = None,
-            connections_limit: int = None,
-            timeout: Optional[Union[int, float, aiohttp.ClientTimeout]] = None,
-    ):
-        """Для получения доступа к API если вы являетесь администратором, перейдите в ПУ.
-
-        https://cp.abcp.ru/?page=allsettings&systemsettings&apiInformation
-
-        Если вы являетесь клиентом, запросите доступ у вашего менеджера.
-
-        :param host: Хост
-        :param login: Логин
-        :param password: MD5-пароль
-        :raise: when host, login or password is invalid
-        :return: Объект класса
-        """
-
-        self._main_loop = loop
-        # Authentication
-
-        self._host = host
-        self._login = login
-        self._password = password
-        self.admin = api.check_data(host, login, password)
-
-        self.shipment_address = None
-        self.shipment_method = None
-        self.payment_method = None
-        self.shipment_office = None
-        self._ssl_context = ssl.create_default_context(cafile=certifi.where())
-
-        self._session: Optional[aiohttp.ClientSession] = None
-        self._connector_class: Type[aiohttp.TCPConnector] = aiohttp.TCPConnector
-        self._connector_init = dict(limit=connections_limit, ssl=self._ssl_context)
-        self._headers = Headers()
-
-        self.timeout = timeout
-
-    async def _get_new_session(self) -> aiohttp.ClientSession:
-        return aiohttp.ClientSession(
-            connector=self._connector_class(**self._connector_init),
-            json_serialize=json.dumps
-        )
-
-    @property
-    def _loop(self) -> Optional[asyncio.AbstractEventLoop]:
-        return self._main_loop
-
-    async def _get_session(self) -> Optional[aiohttp.ClientSession]:
-        if self._session is None or self._session.closed:
-            self._session = await self._get_new_session()
-
-        if not self._session._loop.is_running():
-            await self._session.close()
-            self._session = await self._get_new_session()
-
-        return self._session
-
-    async def close(self):
-        """
-        Close all client sessions
-        """
-        if self._session:
-            await self._session.close()
-
-    def __payload_check(self, payload):
-        if isinstance(payload, dict):
-            payload['userlogin'] = self._login
-            payload['userpsw'] = self._password
-        elif isinstance(payload, FormData):
-            payload.add_field('userlogin', self._login)
-            payload.add_field('userpsw', self._password)
-        elif payload is None:
-            payload = {'userlogin': self._login, 'userpsw': self._password}
-        return payload
-
-    async def request(self, method: str,
-                      payload: Union[Dict, FormData] = None, post: bool = False, **kwargs) -> Union[List, Dict, bool]:
-        """
-        Make an request to ABCP API
-
-        https://www.abcp.ru/wiki/API:Docs
-
-        :param method: API method
-        :type method: :obj:`str`
-        :param payload: _request parameters
-        :type payload: :obj:`dict`
-        :param post:
-        :return: result
-        :rtype: Union[List, Dict]
-        :raise: :obj:`utils.exceptions`
-        """
-        if not self.admin and isinstance(method, (_Methods.Admin, _Methods.TsAdmin)):
-            raise NotEnoughRights('Недостаточно прав для использования API администратора')
-        payload = self.__payload_check(payload)
-        if isinstance(payload, FormData):
-            headers = self._headers.multipart_header()
-        elif kwargs is not None and 'json' in kwargs.keys():
-            headers = self._headers.json_header()
-            return await api.make_request_json(await self._get_session(), self._host, method, payload, headers)
-        else:
-            headers = self._headers.url_encoded_header()
-        return await api.make_request(await self._get_session(), self._host,
-                                      method, payload, headers, post, timeout=self.timeout, **kwargs)
+import asyncio
+import logging
+import ssl
+from typing import Dict, List, Optional, Union, Type, Any
+
+import aiohttp
+import certifi
+import ujson
+from aiohttp import FormData
+
+from .api import Headers, _Methods, check_data, make_request_json, make_request
+from .exceptions import NotEnoughRights
+
+logging.basicConfig(level=logging.INFO)
+logger = logging.getLogger('base')
+
+
+class BaseAbcp:
+
+    def __init__(
+            self,
+            host: str,
+            login: str,
+            password: str,
+            loop: Optional[Union[asyncio.BaseEventLoop, asyncio.AbstractEventLoop]] = None,
+            connections_limit: int = None,
+            timeout: Optional[Union[int, float, aiohttp.ClientTimeout]] = None,
+    ):
+        """Для получения доступа к API если вы являетесь администратором, перейдите в ПУ.
+
+        https://cp.abcp.ru/?page=allsettings&systemsettings&apiInformation
+
+        Если вы являетесь клиентом, запросите доступ у вашего менеджера.
+
+        :param host: Хост
+        :param login: Логин
+        :param password: MD5-пароль
+        :raise: when host, login or password is invalid
+        :return: Объект класса
+        """
+
+        self._main_loop = loop
+        # Authentication
+
+        self._host = host
+        self._login = login
+        self._password = password
+        self.admin = check_data(host, login, password)
+
+        self.shipment_address = None
+        self.shipment_method = None
+        self.payment_method = None
+        self.shipment_office = None
+        self._ssl_context = ssl.create_default_context(cafile=certifi.where())
+
+        self._session: Optional[aiohttp.ClientSession] = None
+        self._connector_class: Type[aiohttp.TCPConnector] = aiohttp.TCPConnector
+        self._connector_init = dict(limit=connections_limit, ssl=self._ssl_context)
+        self._headers = Headers()
+
+        self.timeout = timeout
+
+    async def _get_new_session(self) -> aiohttp.ClientSession:
+        return aiohttp.ClientSession(
+            connector=self._connector_class(**self._connector_init),
+            json_serialize=ujson.dumps
+        )
+
+    @property
+    def _loop(self) -> Optional[asyncio.AbstractEventLoop]:
+        return self._main_loop
+
+    async def _get_session(self) -> Optional[aiohttp.ClientSession]:
+        if self._session is None or self._session.closed:
+            self._session = await self._get_new_session()
+
+        if not self._session._loop.is_running():
+            await self._session.close()
+            self._session = await self._get_new_session()
+
+        return self._session
+
+    async def close(self):
+        """
+        Close all client sessions
+        """
+        if self._session:
+            await self._session.close()
+
+    def __payload_check(self, payload: Union[Dict[str, Any], FormData]) -> Union[Dict[str, Any], FormData]:
+        if isinstance(payload, dict):
+            payload['userlogin'] = self._login
+            payload['userpsw'] = self._password
+            return payload
+        elif isinstance(payload, FormData):
+            payload.add_field('userlogin', self._login)
+            payload.add_field('userpsw', self._password)
+            return payload
+        elif payload is None:
+            payload = {'userlogin': self._login, 'userpsw': self._password}
+        return payload
+
+    async def request(self, method: str,
+                      payload: Union[Dict[str, Any], FormData] = None,
+                      post: bool = False, **kwargs) -> Union[List, Dict, bool]:
+        """
+        Make an request to ABCP API
+
+        https://www.abcp.ru/wiki/API:Docs
+
+        :param method: API method
+        :type method: :obj:`str`
+        :param payload: _request parameters
+        :type payload: :obj:`dict`
+        :param post:
+        :return: result
+        :rtype: Union[List, Dict]
+        :raise: :obj:`utils.exceptions`
+        """
+        if not self.admin and isinstance(method, (_Methods.Admin, _Methods.TsAdmin)):
+            raise NotEnoughRights('Недостаточно прав для использования API администратора')
+        payload = self.__payload_check(payload)
+        if isinstance(payload, FormData):
+            headers = self._headers.multipart_header()
+        elif kwargs is not None and 'json' in kwargs.keys():
+            headers = self._headers.json_header()
+            return await make_request_json(await self._get_session(), self._host, method, payload, headers)
+        else:
+            headers = self._headers.url_encoded_header()
+        return await make_request(await self._get_session(), self._host,
+                                  method, payload, headers, post, timeout=self.timeout, **kwargs)
```

### Comparing `aioabcpapi-2.0.6/aioabcpapi/cp/admin.py` & `aioabcpapi-2.0.7/aioabcpapi/cp/admin.py`

 * *Ordering differences only*

 * *Files 27% similar despite different names*

```diff
@@ -1,1651 +1,1651 @@
-#!/usr/bin/python
-# -*- coding: utf-8 -*-
-from datetime import datetime
-from io import BufferedReader
-from typing import Dict, List, Optional, Union
-
-from ..api import _Methods
-from ..base import BaseAbcp
-from ..exceptions import AbcpAPIError, AbcpParameterRequired, AbcpWrongParameterError
-from ..utils.payload import generate_payload, generate_payload_filter, generate_payload_payments, \
-    generate_payload_online_order, generate_file_payload
-
-
-class AdminApi:
-    def __init__(self, base: BaseAbcp):
-        """
-        Класс содержит методы административного интерфейса
-
-        https://www.abcp.ru/wiki/API.ABCP.Admin
-        """
-        self._base = base
-        self.orders = Orders(base)
-        self.finance = Finance(base)
-        self.users = Users(base)
-        self.staff = Staff(base)
-        self.statuses = Statuses(base)
-        self.distributors = Distributors(base)
-        self.catalog = Catalog(base)
-        self.articles = Articles(base)
-        self.users_catalog = UsersCatalog(base)
-        self.payment = Payment(base)
-
-
-class Orders:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get_orders_list(
-            self,
-            date_created_start: Union[str, datetime] = None,
-            date_created_end: Union[str, datetime] = None,
-            date_updated_start: Union[str, datetime] = None,
-            date_updated_end: Union[str, datetime] = None,
-            numbers: Union[str, int, List] = None,
-            internal_numbers: Optional[List] = None,
-            status_code: Union[str, int, List] = None,
-            office_id: Union[int, str] = None,
-            distributor_order_id: Union[int, str] = None,
-            is_canceled: Union[int, str] = None,
-            distributor_id: Union[str, int, List] = None,
-            user_id: Union[int, str] = None,
-            with_deleted: Union[str, bool] = None,
-            format: Optional[str] = None,
-            limit: Optional[int] = None,
-            skip: Optional[int] = None,
-            desc: Optional[bool] = None
-
-    ):
-        """Принимает в качестве параметров условия фильтрации заказов. Возвращает список заказов (в т.ч. список позиций заказа).
-
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.BE.D0.B2
-
-
-
-        :param user_id: Идентификатор клиента (покупателя). В результате вернутся все заказы, сделанные указанным клиентом.
-        :param date_created_start: Начальная дата размещения заказа `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_created_start: `str` or `datetime`
-        :param date_created_end: Конечная дата размещения заказа
-        :type date_created_end: `str` or `datetime`
-        :param date_updated_start: Начальная дата последнего обновления заказа в формате `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_updated_start: `str` or `datetime`
-        :param date_updated_end: Конечная дата последнего обновления заказа в формате `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_updated_end: `str` or `datetime`
-        :param numbers: Массив номеров заказов
-        :type numbers: list
-        :param internal_numbers: Массив номеров заказов в учетной системе (например, в 1С). Используется только, если в параметрах запроса не задан numbers.
-        :type internal_numbers: list
-        :param status_code: Код статус позиции заказа (один или массив кодов). Будут выбраны заказы содержащие хотя бы одну позицию в данном статусе.
-        :type status_code: Union[str, int, list]
-        :param office_id: Идентификатор офиса (в ответе по параметру могут быть отфильтрованы заказы где этот офис выбран как самовывоз или если это офис клиента или если менеджер клиента, сделавшего заказ, относится к данному офису)
-        :type office_id: int or str
-        :param distributor_order_id: Идентификатор заказа у поставщика. В результате вернутся все заказы которые были отправлены поставщику под этим номером.
-        :type distributor_order_id: int or str
-        :param is_canceled: Флаг "Запрос на удаление позиции". 0 - запрос не был отправлен, 1 - запрос отправлен, 2 - запрос отклонен менеджером.
-        :type is_canceled: int or str
-        :param distributor_id: Идентификатор (один или массив идентификаторов) поставщика. В результате вернутся все заказы, содержащие хотя бы одну позицию от указанного поставщика.
-        :type distributor_id: Union[str, int, list]
-        :param with_deleted: Признак, возвращать ли в ответе удаленные заказы и позиции
-        :type with_deleted: str or bool ('true', 'false', True, False)
-        :param format: Формат ответа. Доступные значения: <br>
-               additional - дописывает к заказу данные клиента при гостевом заказе; к позициям добавляет значение vinQueryIds
-               <br>short - сокращенный вариант отображения без содержимого позиций заказов
-               <br>count - возвращает только количество заказов по заданным условиям
-               <br>status_only - возвращает только номер заказа, а в узле позиций: id, statusCode, brand, number, numberFix, code
-               <br>p - заказы содержатся в поле items, данные о количестве содержатся в поле count
-        :type format: str
-        :param limit: Ограничение на возвращаемое кол-во
-        :type limit: int
-        :param skip: Сколько заказов пропустить
-        :type skip: int
-        :param desc: Обратный порядок
-        :type desc: : bool
-
-
-        """
-        if isinstance(date_created_start, datetime):
-            date_created_start = f'{date_created_start:%Y-%m-%d %H:%M:%S}'
-        if isinstance(date_created_end, datetime):
-            date_created_end = f'{date_created_end:%Y-%m-%d %H:%M:%S}'
-        if isinstance(date_updated_start, datetime):
-            date_updated_start = f'{date_updated_start:%Y-%m-%d %H:%M:%S}'
-        if isinstance(date_updated_end, datetime):
-            date_updated_end = f'{date_updated_end:%Y-%m-%d %H:%M:%S}'
-        if isinstance(format, str) and format not in ["additional", "short", "count", "status_only", "p"]:
-            raise AbcpWrongParameterError(
-                'Параметр "format" должен принимать одно из значений ["additional", "short", "count", "status_only", "p"]')
-        if limit is not None and not 1 <= int(limit) <= 1000:
-            raise AbcpAPIError(f'The limit must be more than {limit}')
-        if isinstance(status_code, (int, str)):
-            status_code = [status_code]
-        if not isinstance(numbers, list) and numbers is not None:
-            numbers = [numbers]
-        if isinstance(user_id, str) and not user_id.isdigit():
-            raise AbcpAPIError(f'Параметр user_id должен быть числом')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Orders.GET_ORDERS_LIST, payload)
-
-    async def get_order(
-            self,
-            number: Union[int, str] = None,
-            internal_number: Union[int, str] = None,
-            with_deleted: Union[str, bool] = None,
-            format: str = None
-
-    ):
-        """Принимает в качестве параметра онлайн-номер заказа. Возвращает информацию о заказе (в т.ч. список позиций заказа).
-
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BE_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B5
-
-
-        :param number: Номер заказа int или str
-        :type number: int or str
-        :param internal_number: Массив номеров заказов в учетной системе (например, в 1С).
-                Используется только, если в параметрах запроса не задан numbers.
-        :type internal_number: int or str
-        :param with_deleted: Признак, возвращать ли в ответе удаленные заказы и позиции
-        :type with_deleted: str or bool ('true', 'false', True, False)
-        :param format: Формат ответа. Доступные значения
-               additional - дописывает к заказу данные клиента при гостевом заказе; к позициям добавляет значение vinQueryIds
-               short - сокращенный вариант отображения без содержимого позиций заказов
-               count - возвращает только количество заказов по заданным условиям
-               status_only - возвращает только номер заказа, а в узле позиций: id, statusCode, brand, number, numberFix, code
-               p - заказы содержатся в поле items, данные о количестве содержатся в поле count
-        :type format: str
-
-        """
-        if number is None and internal_number is None:
-            raise AbcpParameterRequired(f'Один из параметров "number" или "internal_number" должен быть указан')
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Admin.Orders.GET_ORDER, payload)
-
-    async def status_history(
-            self,
-            position_id: Union[int, str]
-
-    ):
-        """Принимает в качестве параметра id позиции заказа. Возвращает информацию об истории изменений статуса позиции заказа.
-
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D1.81.D1.82.D0.BE.D1.80.D0.B8.D0.B8_.D0.B8.D0.B7.D0.BC.D0.B5.D0.BD.D0.B5.D0.BD.D0.B8.D0.B9_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.B0_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B0
-
-
-        :param position_id: Номер заказа int или str
-        :type position_id int or str
-
-
-        """
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Admin.Orders.STATUS_HISTORY, payload)
-
-    async def create_or_edit_order(
-            self,
-            number: Union[int, str] = None,
-            internal_number: Union[int, str] = None,
-            user_id: Union[int, str] = None,
-            date: Union[str, datetime] = None,
-            comment: str = None,
-            order_positions: Union[List[Dict], Dict] = None,
-            delivery_type_id: Union[int, str] = None,
-            delivery_office_id: Union[int, str] = None,
-            basket_id: Union[int, str] = None,
-            guest_order_name: str = None,
-            guest_order_mobile: str = None,
-            guest_order_email: str = None,
-            shipment_date: Union[str, datetime] = None,
-            delivery_cost: Union[str, int, float] = None,
-            delivery_address_id: Union[int, str] = None,
-            delivery_address: str = None,
-            manager_id: Union[int, str] = None,
-            client_order_number: str = None,
-            note: str = None,
-            del_note: Union[str, int] = None
-
-    ):
-        """Универсальный метод сохранения. Принимает в качестве параметра объект описывающий заказ. Для создания заказа
-         от имени Гостя, необходимо передавать корректно заполненные параметры: guestOrderName и guestOrderMobile или guestOrderEmail,
-          в зависимости от обязательности полей "Мобильный" или "Email" в форме создания гостевого заказа.
-
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.A1.D0.BE.D1.85.D1.80.D0.B0.D0.BD.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B0
-
-
-        :param manager_id: id менеджера по заказу
-        :param comment: Комментарий к заказу
-        :param date: Дата заказа `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param number: Онлайн-номер заказа
-        :type number: int or str
-        :param internal_number: Внутренний номер заказа, обязательный параметр для создания<br><br>
-        :type internal_number int or str
-        :param order_positions: Список словарей описывающих позиции, читайте документацию API.ABCP.Admin<br>В случае
-         редактирования заказа, могут быть указаны только позиции и поля, которые требуют изменения. В случае создания
-         заказа, должны быть указаны все позиции со всеми полями (кроме полей comment, supplierCode и itemKey).
-         При редактировании позиций обязательна передача параметра id. Если параметр id не передан, будет добавлена новая позиция.
-          При добавлении позиции все поля (кроме полей comment, supplierCode и itemKey) для нее являются обязательными. Для удаления позиции необходимо указать ей количество 0 или установить параметр delete в значение 1.<br><br>
-        :type order_positions: list of dictionaries
-        :param client_order_number: Номер заказа в системе учета клиента<br><br>
-        :type client_order_number: int or str
-        :param user_id: Идентификатор клиента на сайте, для которого создается заказ. Обязательный параметр, если создается заказ на клиента или сотрудника<br>
-        :type user_id: int or str
-        :param delivery_type_id: Тип доставки<br>
-        :type delivery_type_id: int or str
-        :param delivery_office_id: Идентификатор офиса самовывоза <br>
-        :type delivery_office_id: int or str
-        :param basket_id: 	Необязательный параметр - идентификатор корзины при использовании мультикорзины<br>
-        :type basket_id: int or str
-        :param guest_order_name: Необязательный параметр - имя клиента для оформления заказа от имени Гостя.
-         Для корректного оформления заказа под гостем должны быть указаны параметры guestOrderName и guestOrderMobile или
-          guestOrderEmail.
-        :type guest_order_name: str
-        :param guest_order_mobile: Необязательный параметр - контактный телефон клиента для оформления заказа от имени
-         Гостя. (в формате 70000000000). Для корректного оформления заказа под гостем должны быть указаны параметры
-          guestOrderName и guestOrderMobile или guestOrderEmail.
-        :type guest_order_mobile: str
-        :param guest_order_email: Необязательный параметр - e-mail для оформления заказа от имени Гостя.
-        (в формате user@domain.com). Для корректного оформления заказа под гостем должны быть указаны параметры guestOrderName и guestOrderMobile или guestOrderEmail.
-        :type guest_order_email: str
-        :param shipment_date: Дата доставки  `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type shipment_date: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param delivery_cost: Цена доставки
-        :type delivery_cost: int or float
-        :param delivery_address_id: Число. Идентификатор адреса доставки. Если нужно создать новый адрес, то нужно передать "-1" и в параметре deliveryAddress новый адрес доставки.
-        :type delivery_address_id: str or int
-        :param delivery_address: Текст. Адрес доставки, в случае, когда необходимо сразу создать новый адрес нужно в deliveryAddressId передавать "-1" + адрес доставки
-        :type delivery_address: str
-        :param note: Текст заметки администратора API
-        :type note: str
-        :param del_note: ID удаляемой заметки, value будет пустым
-        :type del_note: str, int
-
-
-        """
-        if isinstance(shipment_date, datetime):
-            shipment_date = f'{shipment_date:%Y-%m-%d %H:%M:%S}'
-        if isinstance(date, datetime):
-            date = f'{date:%Y-%m-%d %H:%M:%S}'
-        if isinstance(order_positions, dict):
-            order_positions = [order_positions]
-        if number is None and internal_number is None:
-            raise AbcpParameterRequired('number and internal_number is None')
-        if delivery_address_id is not None and int(delivery_address_id) == -1 and delivery_address is None:
-            raise AbcpAPIError('Не передан новый адрес доставки')
-        if delivery_cost is not None and delivery_address_id is None:
-            raise AbcpParameterRequired(
-                'Необходимо указать delivery_address_id если это существующий адрес '
-                'или delivery_address_id=-1 и новый delivery_address.')
-        if delivery_address_id is not None and delivery_type_id is None:
-            raise AbcpParameterRequired(
-                'Необходимо передать delivery_type_id чтобы установить адрес доставки')
-        if any(x is not None for x in [number, internal_number]) and all(
-                [order_positions, user_id, delivery_type_id, delivery_office_id, basket_id, guest_order_name,
-                 guest_order_mobile, guest_order_email, shipment_date, delivery_cost, delivery_address_id,
-                 delivery_address, client_order_number]) is None:
-            raise AbcpParameterRequired('Недостаточно параметров')
-        if note is not None and del_note is not None:
-            raise AbcpAPIError('Заметку можно либо удалить либо добавить')
-
-        payload = generate_payload(exclude=['client_order_number', 'order_positions', 'note', 'del_note'], order=True,
-                                   **locals())
-
-        return await self._base.request(_Methods.Admin.Orders.SAVE_ORDER, payload, True)
-
-    async def get_online_order_params(
-            self,
-            position_ids: Union[List, str, int]
-
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.B0.D1.80.D0.B0.D0.BC.D0.B5.D1.82.D1.80.D0.BE.D0.B2_.D0.B4.D0.BB.D1.8F_.D0.BE.D1.82.D0.BF.D1.80.D0.B0.D0.B2.D0.BA.D0.B8_online-.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D1.83
-        Это вспомогательная операция, которую необходимо выполнять перед отправкой online-заказа поставщику. Если
-        для поставщика есть дополнительные параметры заказа или позиций заказа, то в ответ вы получите набор данных.
-        На их основании нужно составить API запрос для отправки заказа. Если вы уже определились с какими параметрами
-        будете отправлять заказы поставщику, то эту операцию вызывать нет необходимости, можно сразу переходить к
-        методу отправки заказа.
-        Идентификаторы позиций, которые необходимо передавать в запросе,
-        должны принадлежать одному поставщику. Т.е. за один API запрос операции cp/orders/online можно отправить
-        позиции только одного поставщика. Если вам необходимо отправить позиции для двух поставщиков, то необходимо
-        предварительно сгруппировать идентификаторы позиций и выполнить два запроса к cp/orders/online по каждому из
-        поставщиков.
-        Кол-во идентификаторов позиций в одном запросе ограничено. За один API запрос отправить в заказ можно не
-        более 20 позиций для сторонних поставщиков. Для поставщиков работающих на платформе ABCP ограничение - 100
-        позиций.
-
-
-        :param position_ids: Массив идентификаторов позиций, которые нужно отправить поставщику (Позиции должны быть от одного поставщика)
-        :type position_ids: List of ids str or int no matter
-
-        """
-        if not isinstance(position_ids, list):
-            position_ids = [position_ids]
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Admin.Orders.ONLINE_ORDER, payload)
-
-    async def send_online_order(
-            self,
-            order_params: Union[List[Dict], Dict],
-            positions: Union[List[Dict], Dict],
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D1.82.D0.BF.D1.80.D0.B0.D0.B2.D0.BA.D0.B0_online-.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D1.83
-        Идентификаторы позиций, которые необходимо передавать в запросе, должны принадлежать одному поставщику.
-        Т.е. за один API запрос операции cp/orders/online можно отправить позиции только одного поставщика. Если вам
-        необходимо отправить позиции для двух поставщиков, то необходимо предварительно сгруппировать идентификаторы
-        позиций и выполнить два запроса к cp/orders/online по каждому из поставщиков. Кол-во идентификаторов позиций
-        в одном запросе ограничено. За один API запрос отправить в заказ можно не более 20 позиций для сторонних
-        поставщиков. Для поставщиков работающих на платформе ABCP ограничение - 100 позиций. В ответ вы можете
-        получить один или несколько созданных заказов. Отправка заказа аналогична отправке из панели управления. Если
-        заказ оформлен успешно, то результат фиксируется в панели управления, чекбокс заменятся на номер заказа
-        поставщика и его статус (если поставщик поддерживает передачу статуса). Если настроена синхронизация
-        статусов, она также активируется для отправленных позиций. Внимание! При работе с API поставщика,
-        в большинстве случаев используется общая корзина при работе с сайтом поставщика и при работе с API. При
-        отправке заказа поставщику последовательно выполняются запросы по предварительной очистке корзины,
-        добавлению товара в корзину, чтение и отправка её в заказ. Очень важно не допустить параллельной отправки
-        разных позиций одному поставщику. Так же в момент отправки заказа поставщику не должна производиться отправка
-        заказов из панели управления abcp и работа с корзиной на сайте поставщика. В противном случае вы можете
-        получить некорректные заказы, ошибки и задвоенные заказы с одинаковыми товарами.
-
-
-        :param order_params: Массив параметров заказа, который нужно сформировать на основе операции "Получение параметров для отправки online-заказа поставщику". Если у поставщика нет параметров заказа, то параметр orderParams необязательный.
-        :type order_params: List of dict example: [{'shipmentAddress': 77333, 'comment': 'Мой коментарий', 'deliveryType': 3, 'contactName': 'Иванов Иван'}]
-        :param positions: Массив данных с позициями заказов
-        d = await api.cp.admin.get_online_order_params(id=222)
-        order_params={d['orderParams'][0]['fieldName']: d['orderParams'][0]['enum'][2]['value']}, positions={'id': 263266039, 'comment': 'тест'}
-        :type positions: List of ids, str or int
-        """
-        if not isinstance(positions, list):
-            positions = [positions]
-
-        if isinstance(order_params, dict):
-            order_params = [order_params]
-        payload = generate_payload_online_order(**locals())
-
-        return await self._base.request(_Methods.Admin.Orders.ONLINE_ORDER, payload, True)
-
-
-class Finance:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def update_balance(
-            self,
-            user_id: Union[int, str],
-            balance: Union[float, int, str],
-            in_stop_list: Union[bool, str] = None
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B1.D0.B0.D0.BB.D0.B0.D0.BD.D1.81.D0.B0_.D0.BA.D0.BB.D0.B8.D0.B5.D0.BD.D1.82.D0.B0
-        Изменяет баланс клиента. Принимает в качестве параметра текущий баланс пользователя (float) в валюте сайта
-        и идентификатор пользователя на сайте. Идентификатор пользователя - это уникальное значение для всей системы,
-        которое может не совпадать со значением поля "Код клиента" в карточке клиента. Узнать его можно, либо из URL
-        карточки клиента, например, https://cp.abcp.ru/?page=customers&customerId=353169&action=editCustomer - в
-        данном случае идентификатор клиента это значение параметра customerId, а именно, 353169; либо,
-        при использовании синхронизации пользователей с помощью операции GET cp/users, идентификатор пользователя
-        возвращается в поле userId.
-        !!!Обновляет сальдо в карточке клиента(видно при редактировани), не влияет на модуль финансы, возможно я ошибаюсь!!!
-
-
-        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
-        :type user_id: int or str
-        :param balance: Значение баланса в валюте сайта
-        :type balance: float
-        :param in_stop_list: Признак нахождения клиента в стоп-листе (необязательный параметр)
-        :type in_stop_list: str or bool ('true', 'false', True, False)
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Finance.UPDATE_BALANCE, payload, True)
-
-    async def update_credit_limit(
-            self,
-            user_id: Union[int, str],
-            credit_limit: Union[float, int, str]
-
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BB.D0.B8.D0.BC.D0.B8.D1.82.D0.B0_.D0.BA.D1.80.D0.B5.D0.B4.D0.B8.D1.82.D0.B0_.D0.BA.D0.BB.D0.B8.D0.B5.D0.BD.D1.82.D0.B0
-        Изменяет лимит кредита клиента. Принимает в качестве параметра текущий лимит кредита пользователя (float) в валюте сайта и идентификатор пользователя на сайте.
-        !!!В случае успешного обновления баланса, метода возвращает:
-        userId, creditLimit и excludeCart. Параметр excludeCart не указан в документации метода!!!
-
-
-        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
-        :type user_id: int or str
-        :param credit_limit: Значение лимита кредита в валюте сайта
-        :type credit_limit: float
-        """
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Admin.Finance.UPDATE_CREDIT_LIMIT, payload, True)
-
-    async def update_finance_info(
-            self,
-            user_id: Union[int, str],
-            balance: Union[float, int, str] = None,
-            credit_limit: float = None,
-            in_stop_list: Union[bool, str] = None,
-            pay_delay: Union[int, str] = None,
-            overdue_saldo: Union[float, int, str] = None
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D1.84.D0.B8.D0.BD.D0.B0.D0.BD.D1.81.D0.BE.D0.B2.D0.BE.D0.B9_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BA.D0.BB.D0.B8.D0.B5.D0.BD.D1.82.D0.B0
-        Изменяет финансовую информацию клиента. Принимает в качестве параметров идентификатор пользователя на
-        сайте и финансовую информацию пользователя. Обязательно наличие как минимум одного из полей (balance,
-        creditLimit, inStopList, payDelay, overdueSaldo).
-
-
-        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
-        :type user_id: int or str
-        :param balance: Значение баланса в валюте сайта
-        :type balance: float
-        :param credit_limit: Значение лимита кредита в валюте сайта
-        :type credit_limit: float
-        :param in_stop_list: Признак нахождения клиента в стоп-листе
-        :type in_stop_list: str or bool ('true', 'false', True, False)
-        :param pay_delay: Отсрочка платежа(в днях)
-        :type pay_delay: int or str
-        :param overdue_saldo: Просроченный баланс
-        :type overdue_saldo: float
-        """
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Admin.Finance.UPDATE_FINANCE_INFO, payload, True)
-
-    async def get_payments_info(
-            self,
-            user_id: Union[int, str] = None,
-            payment_number: str = None,
-            create_date_time_start: Union[str, datetime] = None,
-            create_date_time_end: Union[str, datetime] = None
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BE.D0.B1_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82.D0.B0.D1.85_.D0.B8.D0.B7_.D1.84.D0.B8.D0.BD.D0.BC.D0.BE.D0.B4.D1.83.D0.BB.D1.8F
-        Возвращает список оплат из финмодуля.
-        Параметры paymentNumber, userId необязательные.
-        Если указан paymentNumber, то createDateTimeStart и createDateTimeEnd могут не указываться.
-        Если интервал дат выбран больше года, то в ответе получаем ошибку "Сократите диапазон дат и выполните запрос снова.
-        Диапазон не должен превышать 1 год."
-
-
-        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
-        :type user_id: int or str
-        :param payment_number: 	Номер платежа
-        :type payment_number: str
-        :param create_date_time_start: Начальная дата создания `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type create_date_time_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param create_date_time_end: Конечная дата создания `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type create_date_time_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-
-        """
-        if isinstance(create_date_time_start, datetime):
-            create_date_time_start = f'{create_date_time_start:%Y-%m-%d %H:%M:%S}'
-        if isinstance(create_date_time_end, datetime):
-            create_date_time_end = f'{create_date_time_end:%Y-%m-%d %H:%M:%S}'
-        if all(x is None for x in [user_id, payment_number, create_date_time_start, create_date_time_end]):
-            raise AbcpAPIError('Недостаточно параметров')
-        if payment_number is None and any(x is None for x in [create_date_time_start, create_date_time_end]):
-            raise AbcpAPIError('Недостаточно параметров')
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Admin.Finance.GET_PAYMENTS, payload)
-
-    async def get_payment_links(
-            self,
-            payment_numbers: Union[List, str, int] = None,
-            order_ids: Union[List, str, int] = None,
-            user_id: Union[int, str] = None,
-            date_time_start: Union[str, datetime] = None,
-            date_time_end: Union[str, datetime] = None,
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BE_.D0.BF.D1.80.D0.B8.D0.B2.D1.8F.D0.B7.D0.BA.D0.B0.D1.85_.D0.BF.D0.BB.D0.B0.D1.82.D0.B5.D0.B6.D0.B5.D0.B9_.D0.B8.D0.B7_.D0.BC.D0.BE.D0.B4.D1.83.D0.BB.D1.8F_.D0.A4.D0.B8.D0.BD.D0.B0.D0.BD.D1.81.D1.8B
-        Возвращает список привязок платежей из модуля Финансы.
-        При запросе указывать либо paymentNumbers либо orderIds либо userId с DateTimeStart и DateTimeEnd.
-
-        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
-        :type user_id: int or str
-        :param payment_numbers: массив с номерами платежей [str, str, str]
-        :type payment_numbers: List of str or str or int
-        :param order_ids: массив с номерами заказов,если передать 0 и диапазон дат, то можно получить список возвратов за период
-        :type order_ids: List of str or str or int
-        :param date_time_start: Начальная дата `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_time_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param date_time_end: Конечная дата  `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_time_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-
-        """
-
-        if isinstance(date_time_start, datetime):
-            date_time_start = f'{date_time_start:%Y-%m-%d %H:%M:%S}'
-        if isinstance(date_time_end, datetime):
-            date_time_end = f'{date_time_end:%Y-%m-%d %H:%M:%S}'
-        if all(x is None for x in [user_id, date_time_start, date_time_end]):
-            if any(y is not None for y in [payment_numbers, order_ids]):
-                pass
-            else:
-                raise AbcpParameterRequired(
-                    f'Недостаточно параметров, укажите user_id, date_time_start, date_time_end')
-        if not isinstance(order_ids, list) and order_ids is not None:
-            order_ids = [order_ids]
-        if not isinstance(payment_numbers, list) and payment_numbers is not None:
-            payment_numbers = [payment_numbers]
-        payload = generate_payload(exclude=['date_time_start', 'date_time_end'], **locals())
-
-        return await self._base.request(_Methods.Admin.Finance.GET_PAYMENTS_LINKS, payload)
-
-    async def get_online_payments(
-            self,
-            date_start: Union[str, datetime] = None,
-            date_end: Union[str, datetime] = None,
-            customer_ids: Union[List, int] = None,
-            payment_method_id: Union[int, str] = None,
-            status_ids: Union[List, str, int] = None,
-            order_ids: Union[List, str, int] = None
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_online_.D0.BF.D0.BB.D0.B0.D1.82.D0.B5.D0.B6.D0.B5.D0.B9
-        Возвращает список online платежей. Все параметры необязательные и принадлежат к параматерам filter
-
-
-        :param date_start: Дата начало периода для выбора платежей. `str` в формате %Y-%m-%d или %Y-%m-%d %H:%M:%S или datetime object(%Y-%m-%d)
-        :type date_start: `str` в формате %Y-%m-%d или datetime object. Для
-        :param date_end: Дата начало периода для выбора платежей. `str` в формате %Y-%m-%d или %Y-%m-%d %H:%M:%S или datetime object(%Y-%m-%d)
-        :type date_end: `str` в формате %Y-%m-%d или datetime object
-        :param customer_ids: Массив идентификаторов клиентов. Не более 100 штук в одном запросе.
-        :type customer_ids: List or str or int
-        :param payment_method_id: Идентификатор платежной системы. Получить можно из cp/users/profiles или в панели управления.
-        :type payment_method_id: str or int
-        :param status_ids: 	Массив идентификаторов статусов платежей:
-                            1 - Начата 2 - Завершена 3 - Неудача 4 - В обработке
-        :type status_ids: List or str or int
-        :param order_ids: Массив идентификаторов заказов. Не более 100 штук в одном запросе.
-        :type order_ids: List or str or int
-        """
-        if isinstance(date_start, datetime):
-            date_start = f'{date_start:%Y-%m-%d}'
-        if isinstance(date_end, datetime):
-            date_end = f'{date_end:%Y-%m-%d}'
-
-        if order_ids is not None and not isinstance(order_ids, list):
-            order_ids = [order_ids]
-        if status_ids is not None and not isinstance(status_ids, list):
-            status_ids = [status_ids]
-        if customer_ids is not None and not isinstance(customer_ids, list):
-            customer_ids = [customer_ids]
-
-        payload = generate_payload_filter(**locals())
-
-        return await self._base.request(_Methods.Admin.Finance.GET_PAYMENTS_ONLINE, payload)
-
-    async def add_multiple_payments(
-            self,
-            payments: Union[List[Dict], Dict] = None,
-            link_payments: Union[bool, int] = 0
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82
-        Добавляет платежи клиентам. Возвращает массив добавленных платежей.
-
-
-        :param payments: Массив с оплатами
-        :type payments: Union[List[Dict], Dict]
-        :param link_payments: Идентификатор платежной системы. Получить можно из cp/users/profiles или в панели управления.
-        :type link_payments: str or int
-        """
-        if isinstance(link_payments, bool):
-            link_payments = str(link_payments)
-        if type(payments) is dict:
-            payments = [payments]
-        payload = generate_payload_payments(single=False, **locals())
-
-        return await self._base.request(_Methods.Admin.Finance.ADD_PAYMENTS, payload, True)
-
-    async def add_single_payment(
-            self,
-            user_id: int,
-            payment_type_id: int,
-            amount: Union[float, int],
-            create_date_time: Union[str, datetime] = None,
-            payment_number: Union[str, int] = None,
-            comment: Optional[str] = None,
-            editor_id: Union[int, str] = None,
-            link_payments: Union[bool, int] = False
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82
-        Добавляет платежи клиентам. Возвращает массив добавленных платежей.
-
-
-        :param user_id: Идентификатор пользователя на сайте, которому добавляется оплата
-        :type user_id: int or str
-        :param create_date_time: Дата и время платежа, `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type create_date_time: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param payment_type_id: Id типа платежа
-        :type payment_type_id: str or int
-        :param amount: 	Сумма платежа
-        :type amount: float or int
-        :param payment_number: Номер платежа, максимум 64 символа. Необязательный параметр. Если передан пустой, то номер генерируется автоматически по маске переданного типа платежа
-        :type payment_number: str or int
-        :param comment: Комментарий к платежу (не обязательное)
-        :type comment: str
-        :param editor_id: Id сотрудника, которым был внесён платёж (не обязательное)
-        :type editor_id: str or int
-        :param link_payments: 	Параметр, отвечающий за автоматическую привязку платежей к заказам. 0 - не привязывать, 1 - привязывать
-        :type link_payments: int or str
-
-        """
-        if isinstance(link_payments, bool):
-            link_payments = int(link_payments)
-        if isinstance(create_date_time, datetime):
-            create_date_time = f'{create_date_time:%Y-%m-%d %H:%M:%S}'
-
-        payload = generate_payload_payments(**locals())
-
-        return await self._base.request(_Methods.Admin.Finance.ADD_PAYMENTS, payload, True)
-
-    async def delete_link_payment(
-            self,
-            payment_link_id: int
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.A3.D0.B4.D0.B0.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D1.80.D0.B8.D0.B2.D1.8F.D0.B7.D0.BA.D0.B8_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82.D1.8B
-        Удаляет привязку оплаты, увеличивает долг заказу, к которому была сделана привязка, на сумму удаляемой
-        привязки, увеличивает остаток оплаты на сумму удаляемой привязки, клиенту пересчитывает сальдо и долг по
-        заказам. Внимание!
-
-        С помощью одного запроса данная операция позволяет удалить только одну привязку. Массовое удаление недоступно
-
-
-        :param payment_link_id: Id привязки, которую нужно удалить.
-        :type payment_link_id: int or str
-        """
-
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Admin.Finance.DELETE_PAYMENT_LINK, payload, True)
-
-    async def link_existing_payment(
-            self,
-            payment_id: Union[str, int],
-            order_id: Union[str, int],
-            amount: Union[str, int, float]
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.BF.D0.B5.D1.80.D0.B0.D1.86.D0.B8.D1.8F_.D0.BF.D1.80.D0.B8.D0.B2.D1.8F.D0.B7.D0.BA.D0.B8_.D0.BF.D0.BE_.D1.80.D0.B0.D0.BD.D0.B5.D0.B5_.D0.B4.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.BD.D0.BE.D0.BC.D1.83_.D0.BF.D0.BB.D0.B0.D1.82.D0.B5.D0.B6.D1.83
-        Позволяет осуществлять привязку ранее созданного платежа
-
-
-        :param payment_id: id платежа.
-        :type payment_id: int or str
-        :param order_id: id заказа по которому делается привязка.
-        :type order_id: int or str
-        :param amount: 	Сумма привязки.
-        :type amount: str or int or float
-        """
-
-        if all(x.isdigit() for x in [payment_id, order_id, amount] if isinstance(x, str)):
-            pass
-        else:
-            raise AbcpAPIError('Все параметры должны являться цифрами')
-
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Admin.Finance.LINK_EXISTING_PLAYMENT, payload, True)
-
-    async def refund_payment(
-            self,
-            refund_payment_id: Union[str, int],
-            refund_amount: Union[str, int, float]
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.BF.D0.B5.D1.80.D0.B0.D1.86.D0.B8.D1.8F_.D0.B2.D0.BE.D0.B7.D0.B2.D1.80.D0.B0.D1.82.D0.B0_.D0.BF.D0.BB.D0.B0.D1.82.D0.B5.D0.B6.D0.B0
-        Позволяет осуществлять возврат ранее созданного платежа
-
-
-        :param refund_payment_id: id платежа.
-        :type refund_payment_id: int or str
-        :param refund_amount: Сумма возврата.
-        :type refund_amount: int or str or float
-        """
-        if not all(x.isdigit() for x in [refund_payment_id, refund_amount] if isinstance(x, str)):
-            raise AbcpAPIError('Все параметры должны являться цифрами')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Finance.REFUND_PAYMENT, payload, True)
-
-    async def delete_payment(self, payment_id: int, delete_link: Union[int, bool] = 0):
-        if isinstance(delete_link, bool):
-            delete_link = int(delete_link)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Finance.DELETE_PAYMENT, payload, True)
-
-    async def get_receipts(
-            self,
-            shop_id: Union[int, str] = None,
-            queue_id: Union[int, str] = None,
-            date_created_start: Union[str, datetime] = None,
-            date_created_end: Union[str, datetime] = None,
-            calculation_method: Union[str, int] = None,
-            print_paper_check: Union[str, int] = None,
-            vat: Union[str, int] = None,
-            calculation_subject: Union[str, int] = None,
-            payment_type: Union[str, int] = None,
-            type: Union[str, int] = None,
-            tax_system: Union[str, int] = None,
-            intent: Union[str, int] = None,
-            fiscalization: Union[str, int] = None,
-            employee_id: Union[int, str] = None,
-            client_id: Union[int, str] = None,
-            start: Union[str, int] = None,
-            rows_on_page: Union[str, int] = None,
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.87.D0.B5.D0.BA.D0.BE.D0.B2
-        Позволяет получить данные о чеках Комтет.
-
-
-        :param shop_id: ID магазина
-        :type shop_id: int or str
-        :param queue_id: ID очереди
-        :type queue_id: int or str
-        :param date_created_start: Начальная дата создания чека в формате `str` в формате %Y-%m-%d  или datetime object
-        :type date_created_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param date_created_end: Конечная дата создания чека `str` в формате %Y-%m-%d  или datetime object
-        :type date_created_end: `str` в формате %Y-%m-%d или datetime object
-        :param calculation_method: Способ расчета: 0 - Предоплата 100%, 1 - Предоплата, 2 - Полный расчет, 3 - Аванс, 4 - Частичный расчет и кредит, 5 - Оплата кредита, 6 - Передача в кредит.
-        :type calculation_method: int or str
-        :param print_paper_check: Был ли запрос печати бумажного чека: 0 - Нет, 1 - Да.
-        :type print_paper_check: int or str
-        :param vat: Налог: 5 - Без НДС, 0 - НДС по ставке 0%, 3 - НДС чека по расчетной ставке 10/110, 4 - НДС чека по расчетной ставке 20/120.
-        :type vat: int or str
-        :param calculation_subject: Предмет расчета: 0 -товар, 1 - работа, 2 - услуга, 3 - платеж.
-        :type calculation_subject: int or str
-        :param payment_type: 	Оплата: 0 - Безналичными, 1 - Наличными, 2 - Предоплата, 3 - Постоплата, 4 - Встречное предоставление.
-        :type payment_type: int or str
-        :param type: Тип чека: 0 - чек, 1- чек коррекции.
-        :param tax_system: Система налогообложения: 0 - ОСН, 1 - УСН доход, 2 - УСН доход - расход, 3 - ЕНВД, 4 - ЕСН, 5 - Патент.
-        :type tax_system: int or str
-        :param intent: Направление платежа: 0 - Приход, 1 - Расход, 2 - Возврат прихода, 3 - Возврат расхода.
-        :type intent: int or str
-        :param fiscalization: Фискализирован: 0 - Нет, 1 - Да.
-        :type fiscalization: int or str
-        :param employee_id: id сотрудника, отправившего чек.
-        :type employee_id: int or str
-        :param client_id: 	id клиента.
-        :type client_id: int or str
-        :param start: Отсчет чеков
-        :type start: int or str
-        :param rows_on_page: 	Количество "на странице"
-        :type rows_on_page: int or str
-
-
-        """
-        if isinstance(date_created_start, datetime):
-            date_created_start = f'{date_created_start:%Y-%m-%d}'
-        if isinstance(date_created_end, datetime):
-            date_created_end = f'{date_created_end:%Y-%m-%d}'
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Finance.GET_RECEIPTS, payload)
-
-    async def get_payments_methods(self, only_enabled: Union[bool, str] = None,
-                                   only_disabled: Union[bool, str] = None,
-                                   payment_method_id: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BD.D0.B0.D1.81.D1.82.D1.80.D0.BE.D0.B5.D0.BA_.D0.BF.D0.BB.D0.B0.D1.82.D1.91.D0.B6.D0.BD.D1.8B.D1.85_.D1.81.D0.B8.D1.81.D1.82.D0.B5.D0.BC
-        Возвращает настройки платёжных систем.
-        Если не указывать доп. параметры,
-        то будут возвращены все существующие настройки для всех платёжных систем (активных и отключенных).
-
-
-        :param only_enabled:если true, то будет возвращён список только включенных настроек ПС
-        :type only_enabled: bool or str
-        :param only_disabled: если true, то будет возвращён список только выключенных настроек ПС
-        :param payment_method_id: id конкретной платёжной системы для которой нужно получить настройки
-        :type payment_method_id: str or int
-        :return:dict
-        """
-        if all(x is not None for x in [only_enabled, only_disabled]):
-            raise AbcpAPIError('Укажите только один параметр должен быть указан only_enabled или only_disabled')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Finance.GET_PAYMENTS_SETTINGS, payload)
-
-
-class Users:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get_users(
-            self,
-            date_registred_start: Union[str, datetime] = None,
-            date_registred_end: Union[str, datetime] = None,
-            date_updated_start: Union[str, datetime] = None,
-            date_updated_end: Union[str, datetime] = None,
-            state: Union[str, int] = None,
-            customer_status: Union[str, int] = None,
-            customers_ids: Union[List, str, int] = None,
-            market_type: Union[str, int] = None,
-            phone: Union[str, int] = None,
-            enable_sms: Union[str, bool] = None,
-            email: str = None,
-            safe_mode: Union[str, int] = None,
-            format: str = None,
-            limit: Optional[int] = None,
-            skip: Optional[int] = None,
-            desc: Union[str, bool] = 'false'
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D0.B5.D0.B9
-        Принимает в качестве параметров условия фильтрации клиентов. Возвращает список клиентов.
-
-
-        :param date_registred_start: Начальная дата регистрации `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_registred_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param date_registred_end: Конечная дата регистрации `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_registred_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param date_updated_start: Начальная дата последнего обновления `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_updated_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param date_updated_end: Конечная дата последнего обновления `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_updated_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param state: Состояние клиента. Значения:-1 - отклоненный, 0 - ожидает регистрации, 1 - зарегистрированный,
-                       2 - удаленный.
-        :type state: int or str
-        :param customer_status: Идентификатор статуса покупателя, если указать 0 - будут выбраны пользователи без статуса
-        :type customer_status: int or str
-        :param customers_ids: Массив идентификаторов покупателей
-        :type customers_ids: List of str or int
-        :param market_type: Тип регистрации. Значения:  1 - Розница 2 - Опт
-        :type market_type: int or str
-        :param phone: Номер телефона клиента
-        :type phone: str 79998887766
-        :param enable_sms: Производится ли отпровка SMS клиенту
-        :param email: E-mail клиента
-        :type email: str
-        :param safe_mode: "Безопасный режим" для клиентов не имеющих поддержки формата JSON.
-                Может принимать значения 0 или 1. При включении (1), адреса доставки в ответе будут возвращаться в виде
-                массива объектов с полями "id" и "name", а не как "ключ - значение".
-        :type safe_mode: int or str
-        :param format: 	Формат ответа. Доступные значения: p - заказы содержатся в поле items,
-                        данные о количестве содержатся в поле count
-        :type format: str
-        :param limit: Количество возвращаемых записей заказов (число, по умолчанию - 1000).
-                      Чтобы получить информацию о количестве записей используйте параметр format со значением p
-        :type limit: int or str
-        :param skip: кол-во заказов, которые нужно пропустить. (число, по умолчанию - 0).
-        :type skip: int or str
-        :param desc: Обратное направление сортировки
-        :type desc: str or bool ('true', 'false', True, False)
-
-
-        """
-
-        if isinstance(date_registred_start, datetime):
-            date_registred_start = f'{date_registred_start:%Y-%m-%d %H:%M:%S}'
-        if isinstance(date_registred_end, datetime):
-            date_registred_end = f'{date_registred_end:%Y-%m-%d %H:%M:%S}'
-        if isinstance(date_updated_start, datetime):
-            date_updated_start = f'{date_updated_start:%Y-%m-%d %H:%M:%S}'
-        if isinstance(date_updated_end, datetime):
-            date_updated_end = f'{date_updated_end:%Y-%m-%d %H:%M:%S}'
-
-        if isinstance(format, str) and format != 'p':
-            raise AbcpWrongParameterError('The parameter "format" can only take the value "p" or None')
-        if not isinstance(customers_ids, list) and customers_ids is not None:
-            customers_ids = [customers_ids]
-        if isinstance(enable_sms, str) and (enable_sms != 'true' and enable_sms != 'false'):
-            raise AbcpAPIError('Параметр "enable_sms" должен быть булевым значением, либо строкой "true" или "false"')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Users.GET_USERS_LIST, payload)
-
-    async def create(
-            self,
-            market_type: Union[str, int],
-            name: str, password: str,
-            mobile: Union[str, int],
-            filial_id: Union[int, str] = None,
-            second_name: str = None, surname: str = None,
-            birth_date: Union[str, datetime] = None,
-            member_of_club: str = None, office: Union[str, int] = None,
-            email: str = None, icq: str = None, skype: str = None,
-            region_id: str = None, city: str = None,
-            organization_name: str = None, business: Union[str, int] = None,
-            organization_form: str = None, organization_official_name: str = None,
-            inn: Union[str, int] = None, kpp: Union[str, int] = None,
-            ogrn: Union[str, int] = None, organization_official_address: str = None,
-            bank_name: str = None, bik: Union[str, int] = None,
-            correspondent_account: Union[str, int] = None, organization_account: Union[str, int] = None,
-            delivery_address: str = None, comment: str = None, profile_id: str = None,
-            pickup_state: Union[int, bool] = None
-    ):
-        """Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.A1.D0.BE.D0.B7.D0.B4.D0.B0.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
-        Принимает параметры для регистрации пользователя. Осуществляет регистрацию нового пользователя в системе.
-        Возвращает статус выполнения операции регистрации, учетные данные нового пользователя, а так же сообщение об ошибке в случае возникновения таковой.
-
-        :param market_type: Тип регистрации: 1 - Розница, 2 - Опт
-        :type market_type: str or int
-        :param filial_id: Код филиала (если имеются)
-        :type filial_id: int or str
-        :param name: Имя :type name: str
-        :param password: Пароль :type password: str
-        :param second_name: Отчество :type second_name: str
-        :param surname: Фамилия :type surname: str
-        :param birth_date: Дата рождения :type birth_date: str datetime strftime("%Y-%m-%d")
-        :param mobile: Отчество :type mobile: str or int forman 79998887766
-        :param member_of_club: Название автоклуба :type member_of_club: str
-        :param office: Идентификатор офиса :type office: str or int
-        :param email: Отчество :type email: str
-        :param icq: icq :type icq: str
-        :param skype: Skype :type skype: str
-        :param region_id: Код региона :type region_id: str
-        :param city: Город :type city: str
-        :param name: Имя :type name: str
-        :param organization_name: Наименование организации :type organization_name: str
-        :param business: Тип организации. Значение от 1 до 3: 1 - Автосервис, 2 - Автомагазин, 3 - Собственный автопарк
-        :type business: str or int
-        :param organization_form: Правовая форма организации. Варианты: ООО, ОАО, ЗАО, ТОО, АО, ЧП, ПБОЮЛ
-        :type organization_form: str
-        :param organization_official_name: Наименование по регистрации (без правовой формы юр. лица)
-        :type organization_official_name: str
-        :param inn: ИНН :type inn: str
-        :param kpp: КПП :type kpp: str
-        :param ogrn: ОГРН :type ogrn: str
-        :param organization_official_address: Юридический адрес организации :type organization_official_address: str
-        :param bank_name: Наименование банка :type bank_name: str
-        :param bik: БИК банка :type bik: str or int
-        :param correspondent_account: Корреспондентский счет банка :type correspondent_account: str or int
-        :param organization_account: Расчетный счет организации :type organization_account: str or int
-        :param delivery_address: Адрес доставки :type delivery_address: str
-        :param comment: Комментарий :type comment: str
-        :param profile_id: Идентификатор профиля.
-        Если не указан, будет выставлен профиль по умолчанию для соответствующего типа регистрации (опт или розница).
-        :type profile_id: str
-        :param pickup_state: Запрет самовывоза для клиента. 0 - запретить самовывоз, 1- разрешить самовывоз. Параметр актуален только если у вас на сайте включена опция: "Корзина: запрет самовывоза определенным клиентам".
-        """
-
-        if isinstance(birth_date, datetime):
-            birth_date = f'{birth_date:%Y-%m-%d}'
-        if isinstance(pickup_state, bool):
-            pickup_state = int(pickup_state)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Users.CREATE_USER, payload, True)
-
-    async def get_profiles(
-            self,
-            profile_id: Union[int, str] = None,
-            skip: Optional[int] = None,
-            limit: Optional[int] = None,
-            format: str = None
-    ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D1.80.D0.BE.D1.84.D0.B8.D0.BB.D0.B5.D0.B9
-        Возвращает список всех профилей.
-
-
-        :param limit: Кол-во профилей в ответе. Необязательный параметр. Допустимые значения от 1 до 100. По умолчанию возвращаются все профили.
-        :param skip: Кол-во профилей, которые нужно пропустить. Необязательный параметр. По умолчанию: 0.
-        :param profile_id: Идентификатор профиля. Необязательный параметр. По умолчанию возвращаются все профили.
-        :param format: Формат ответа. Необязательное значение
-        Может принимать значения: "distributors" - выводить информацию по наценкам на поставщиков; "brands" - выводить информацию по наценкам на поставщиков и бренды
-        :type format: str 'distributors' or 'brands'
-        """
-        format_params_check = ('brands', 'distributors')
-        if isinstance(format, str) and format not in format_params_check:
-            raise AbcpWrongParameterError('format parameter can take values "brands" or "distributors"')
-        del format_params_check
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Users.GET_PROFILES, payload)
-
-    async def edit_profile(
-            self,
-            profile_id: Union[int, str],
-            code: Union[str, int] = None,
-            name: str = None,
-            comment: str = None,
-            price_up: Union[str, int] = None,
-            payment_methods: str = None,
-            matrix_price_ups: Union[List[Dict], Dict] = None,
-            distributors_price_ups: Union[List[Dict], Dict] = None,
-
-    ):
-
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D1.80.D0.BE.D1.84.D0.B8.D0.BB.D1.8F
-        Изменяет профиль. Принимает в качестве параметров идентификатор профиля на сайте и всю информацию о профиле,
-        возвращаемую операцией cp/users/profiles в формате brands.
-        Работает только при выключенной опции Профили: использовать групповое сохранение, иначе возвращает ошибку.
-        Если не указать идентификатор профиля, будет создан новый.
-        В данном случае, обязательными параметрами будут name и priceUp.
-        При создании профиля невозможно использовать имя и код существующих профилей.
-        Обязательно наличие как минимум одного из полей (code, name, comment, priceUp, paymentMethods, matrixPriceUps, distributorsPriceUps).
-
-
-        :param profile_id: Идентификатор профиля
-        :type profile_id: str or int
-        :param code: Код профиля
-        :type code: str or int
-        :param name: Наименование профиля
-        :type name: str
-        :param comment: Комментарий
-        :type comment: str
-        :param price_up: Наценка, %
-        :type price_up: str or int
-        :param payment_methods: 	Платежные системы
-        :type payment_methods: str or int
-        :param matrix_price_ups: Наценки от стоимости товара
-        :type matrix_price_ups: List of dicts
-        :param distributors_price_ups: Наценки по поставщикам
-        :type distributors_price_ups: str or int
-        """
-        if all(x is None for x in [code, name, comment,
-                                   price_up, payment_methods,
-                                   matrix_price_ups, distributors_price_ups]):
-            raise AbcpParameterRequired("Один из опциональных параметров должен быть передан")
-        if isinstance(matrix_price_ups, dict):
-            matrix_price_ups = [matrix_price_ups]
-        if isinstance(distributors_price_ups, dict):
-            distributors_price_ups = [distributors_price_ups]
-        payload = generate_payload(exclude=['matrix_price_ups', 'distributors_price_ups'], **locals())
-        return await self._base.request(_Methods.Admin.Users.EDIT_PROFILE, payload, True)
-
-    async def edit(
-            self,
-            user_id: Union[str, int], business: Union[str, int] = None,
-            email: str = None, name: str = None, second_name: str = None,
-            surname: str = None, password: str = None,
-            birth_date: Union[str, datetime] = None, city: str = None,
-            mobile: Union[str, int] = None, icq: str = None,
-            skype: str = None, enable_sms: Union[bool, str] = None, state: Union[str, int] = None,
-            profile_id: Union[int, str] = None, organization_name: str = None,
-            organization_form: str = None, organization_official_name: str = None,
-            inn: Union[str, int] = None, kpp: Union[str, int] = None, ogrn: Union[str, int] = None,
-            bank_name: str = None, bik: Union[str, int] = None,
-            correspondent_account: Union[str, int] = None, organization_account: Union[str, int] = None,
-            delivery_address: Union[List[Dict], Dict] = None, baskets: Union[List[Dict], Dict] = None,
-            baskets_delivery_address: Union[List[Dict], Dict] = None, comment: str = None,
-            manager_comment: str = None, manager_id: Union[int, str] = None,
-            user_code: Union[str, int] = None, client_service_employee_id: Union[int, str] = None,
-            client_service_employee2_id: Union[int, str] = None, client_service_employee3_id: Union[int, str] = None,
-            client_service_employee4_id: Union[int, str] = None, office: Union[List[Dict], Dict] = None,
-            info: str = None, safe_mode: Union[str, int] = None,
-            pickup_state: Union[int, bool] = None,
-
-    ):
-
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B4.D0.B0.D0.BD.D0.BD.D1.8B.D1.85_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
-        Осуществляет обновление данных пользователя, присланных в запросе.
-        При изменении данных пользователя необязательно передавать все параметры.
-        Используйте в запросе только те данные, которые вы собираетесь изменить.
-
-
-        :param ogrn: ОГРН
-        :param kpp: КПП
-        :param inn:ИНН
-        :param name: Имя
-        :param user_id: Идентификатор изменяемого клиента
-        :param business: Тип организации. Значение от 1 до 6:
-        :param email: Адрес электронной почты
-        :param second_name:	Отчество
-        :param surname: Фамилия
-        :param password: Необязательный параметр. Предназначен для изменения пароля пользователя
-        :param birth_date:Дата рождения `str` в формате %Y-%m-%d  или datetime object
-        :param city: Город
-        :param mobile: Номер мобильного телефона
-        :param icq:	ICQ UIN
-        :param skype: Skype
-        :param enable_sms: Производится ли отпровка SMS клиенту
-        :param state: Состояние аккаунта. Значения: от -1 до 2
-        :param profile_id: Идентификатор профиля
-        :param organization_name: Наименование организации
-        :param organization_form: Правовая форма организации.
-        :param organization_official_name: Наименование по регистрации (без правовой формы юр. лица)
-        :param bank_name: Наименование банка
-        :param bik: БИК банка
-        :param correspondent_account: Корреспондентский счет банка
-        :param organization_account: Расчетный счет организации
-        :param delivery_address: Адреса доставки (массив, где ключи - id адресов). Если передать пустой параметр deliveryAddress, то все адреса клиента будут удалены!
-        :param baskets: Корзины клиента (массив, где ключи - id корзин). Если передать пустой параметр baskets, то все корзины клиента будут удалены!
-        :param baskets_delivery_address: Связки корзины и адреса доставки(массив, где ключи - id корзин). Обновятся только переданные связки "корзина - Адрес доставки". Чтобы убрать привязку корзины и адреса нужно передать значение параметра = "0".
-        :param comment: Комментарий пользователя
-        :param manager_comment: Комментарий менеджера
-        :param manager_id: Идентификатор менеджера. Если передать managerId=0, то менеджер в карточке клиента удалится.
-        :param user_code: Внутренний код пользователя
-        :param client_service_employee_id: Идентификатор личного менеджера клиентской службы (дополнительная опция). Если передать clientServiceEmployeeId=0, то менеджер клиентской службы в карточке клиента удалится.
-        :param client_service_employee2_id: Идентификатор личного менеджера клиентской службы (дополнительная опция). Если передать clientServiceEmployeeId=0, то менеджер клиентской службы в карточке клиента удалится.
-        :param client_service_employee3_id: Идентификатор личного менеджера клиентской службы (дополнительная опция). Если передать clientServiceEmployeeId=0, то менеджер клиентской службы в карточке клиента удалится.
-        :param client_service_employee4_id: Идентификатор личного менеджера клиентской службы (дополнительная опция). Если передать clientServiceEmployeeId=0, то менеджер клиентской службы в карточке клиента удалится.
-        :param office: Массив идентификаторов офисов, к которым необходимо подключить клиента. Если идентификатор офиса, к одному из которых подключен клиент, не будет передан, то он будет отключен. Передать пустой параметр office нельзя, т.к. клиент должен быть подключен минимум к одному офису. Параметр актуален только если у вас на сайте включена опция: "Офисы: включить привязку к клиентам".
-        :param info: "Информация" в личном кабинете. В поле допустимо использование html-тегов. max 4000 символов. Закладка появляется только если есть данные в поле info для клиента.
-        :param safe_mode:
-        :param pickup_state: Запрет самовывоза для клиента. 0 - запретить самовывоз, 1- разрешить самовывоз. Параметр актуален только если у вас на сайте включена опция: "Корзина: запрет самовывоза определенным клиентам".
-        :return:
-        """
-        if isinstance(birth_date, datetime):
-            birth_date = f'{birth_date:%Y-%m-%d}'
-        if isinstance(pickup_state, bool):
-            pickup_state = int(pickup_state)
-        if isinstance(enable_sms, str) and (enable_sms != 'true' and enable_sms != 'false'):
-            raise AbcpAPIError('Параметр "enable_sms" должен быть булевым значением, либо строкой "true" или "false"')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Users.EDIT_USER, payload, True)
-
-    async def get_user_shipment_address(self, user_id: Union[int, str]):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B0.D0.B4.D1.80.D0.B5.D1.81.D0.BE.D0.B2_.D0.B4.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D0.BA.D0.B8
-
-        Возвращает список доступных адресов доставки. Идентификатор адреса доставки необходим при отправке заказа.
-
-        :param user_id: Идентификатор клиента
-        :type user_id: str or int
-        """
-
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Users.GET_USER_SHIPMENT_ADDRESS, payload)
-
-    async def get_shipment_address_zones(self):
-        """
-        Получение списка зон адресов доставки
-
-        :return: Возвращает список зон адресов доставки.
-        """
-        return await self._base.request(_Methods.Admin.Users.GET_USER_SHIPMENT_ADDRESS_ZONES)
-
-    async def get_shipment_address_zone(self, id: int):
-        """
-        Получение одной зоны адресов доставки
-
-        :param id: Уникальный идентификатор зоны адресов доставки
-        :return: Возвращает одну зону адресов доставки по указанному уникальному идентификатору.
-        """
-        return await self._base.request(_Methods.Admin.Users.GET_USER_SHIPMENT_ADDRESS_ZONE.format(id))
-
-    async def update_shipment_zones(self, zones: Union[List[Dict], Dict]):
-        """
-        Сохранение зон адресов доставки. Универсальный метод добавления и обновления зон адресов доставки.
-
-        :param zones: Массив объектов зон адресов доставки
-        :return:
-        """
-        if isinstance(zones, dict):
-            zones = [zones]
-
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Users.UPDATE_SHIPMENT_ZONES, payload, True)
-
-    async def create_shipment_zone(self, name: str, **kwargs):
-        """
-        Создание новой зоны адресов доставки. Метод создания одной зоны адресов доставки.
-
-        :param name: Название зоны
-        :param kwargs: Аргументы isOnDay{day}: int и stopTimeDay{day}: int
-        :return:
-        """
-        if kwargs is None:
-            raise AbcpParameterRequired('Необходимо передать аргументы "isOnDay{day:int}" и "stopTimeDay{day:int}"\n\n'
-                                        'Например: isOnDay1=1, stopTimeDay1="15:30"')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Users.CREATE_SHIPMENT_ZONE, payload, True, json=True)
-
-    async def update_shipment_zone(self, id: int, name: str, **kwargs):
-        """
-        Метод обновления данных одной зоны адресов доставки.
-
-        :param id: Идентификатор обновляемой зоны
-        :param name: Название зоны
-        :param kwargs: Аргументы isOnDay{day}: int и stopTimeDay{day}: int
-        :return:
-        """
-        if kwargs is None:
-            raise AbcpParameterRequired('Необходимо передать аргументы "isOnDay{day:int}" и "stopTimeDay{day:int}"\n\n'
-                                        'Например: isOnDay1=1, stopTimeDay1="15:30"')
-        _method = _Methods.Admin.Users.UPDATE_SHIPMENT_ZONE.format(id)
-        del id
-        payload = generate_payload(**locals())
-        return await self._base.request(_method, payload, True, json=True)
-
-    async def delete_shipment_zone(self, id: int):
-        return await self._base.request(_Methods.Admin.Users.DELETE_SHIPMENT_ZONE.format(id), None, True)
-
-    async def get_updated_cars(self, date_updated_start: str = None, date_updated_end: str = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.BE.D0.B2_.D0.BE.D1.84.D0.B8.D1.81.D0.B0
-        Возвращает информацию об автомобилях, в которые были внесены изменения за определённый период времени.
-        Если не переданы dateUpdatedStart и dateUpdatedEnd, то будет предоставлена информация за последний месяц.
-
-
-        :param date_updated_start: Начальная дата последнего обновления `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_updated_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :param date_updated_end: Конечная дата последнего обновления заказа `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :type date_updated_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
-        :return:dict
-        """
-        if isinstance(date_updated_start, datetime):
-            date_updated_start = f'{date_updated_start:%Y-%m-%d %H:%M:%S}'
-
-        if isinstance(date_updated_end, datetime):
-            date_updated_end = f'{date_updated_end:%Y-%m-%d %H:%M:%S}'
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Users.GET_USERS_CARS, payload)
-
-    async def get_sms_settings(self, user_ids: Union[List, int, str]):
-        if not isinstance(user_ids, list):
-            user_ids = [user_ids]
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Users.SMS_SETTINGS, payload)
-
-
-class Staff:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.81.D0.BE.D1.82.D1.80.D1.83.D0.B4.D0.BD.D0.B8.D0.BA.D0.BE.D0.B2
-        Возвращает список менеджеров.
-        """
-        return await self._base.request(_Methods.Admin.Staff.GET_STAFF)
-
-    async def update_manager(self, id: int, type_id: int = None,
-                             first_name: str = None, last_name: str = None,
-                             email: str = None, phone: str = None, mobile: str = None,
-                             sip: Union[str, int] = None, comment: str = None, boss_id: int = None, office_id: int = None):
-        """
-
-        Обновление данных сотрудника.
-
-        При изменении данных сотрудника необязательно передавать все параметры. Используйте в запросе только те данные, которые вы собираетесь изменить.
-
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B4.D0.B0.D0.BD.D0.BD.D1.8B.D1.85_.D1.81.D0.BE.D1.82.D1.80.D1.83.D0.B4.D0.BD.D0.B8.D0.BA.D0.B0
-
-        :param id: Идентификатор сотрудника (обязательное поле)
-        :param type_id: Идентификатор должности сотрудника
-        :param first_name: Имя сотрудника
-        :param last_name: Фамилия сотрудника
-        :param email: Адрес ящика электронной почты
-        :param phone: Номер телефона
-        :param mobile: Номер мобильного телефона
-        :param sip: SIP номер
-        :param comment: Комментарий
-        :param boss_id: Идентификатор руководителя
-        :param office_id: Идентификатор офиса
-        :return:
-        """
-        if isinstance(sip, str) and not sip.isdigit():
-            raise AbcpWrongParameterError('Параметр "SIP" должен быть числом')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Staff.UPDATE_STAFF, payload, True)
-
-
-class Statuses:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.BE.D0.B2
-        Возвращает список всех статусов позиций заказов.
-        """
-        return await self._base.request(_Methods.Admin.Statuses.GET_STATUSES)
-
-
-class Articles:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get_brands(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D1.80.D0.B0.D0.B2.D0.BE.D1.87.D0.BD.D0.B8.D0.BA.D0.B0_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D0.BE.D0.B2
-        Возвращает список всех брендов зарегистрированных в системе с их синонимами.
-        """
-        return await self._base.request(_Methods.Admin.Articles.GET_BRANDS)
-
-    async def get_brand_group(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D1.80.D0.B0.D0.B2.D0.BE.D1.87.D0.BD.D0.B8.D0.BA.D0.B0_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D0.BE.D0.B2
-
-        Возвращает список всех групп брендов зарегистрированных в системе.
-        """
-        return await self._base.request(_Methods.Admin.Articles.GET_BRANDS_GROUP)
-
-
-class Distributors:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get(self, distributors4mc: Union[str, int, bool] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.BE.D0.B2
-        Возвращает список всех поставщиков, подключенных в ПУ/Поставщики.
-
-
-        :param distributors4mc: При передаче "1" возвращает дополнительно поставщиков 4mycar"
-        :type distributors4mc: str or int
-        """
-        if isinstance(distributors4mc, bool):
-            distributors4mc = int(distributors4mc)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Distributors.GET_DISTRIBUTORS_LIST, payload)
-
-    async def edit_status(self, distributor_id: Union[int, str], status: Union[int, bool]):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.98.D0.B7.D0.BC.D0.B5.D0.BD.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
-        Изменение статуса поставщика
-
-
-        :param distributor_id: 	Id поставщика
-        :type distributor_id: str or int
-        :param status: 	1 - Вкл. / 0 - Выкл.
-        :type status: str or int
-        """
-        if isinstance(status, bool):
-            status = int(status)
-
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Distributors.EDIT_DISTRIBUTORS_STATUS, payload, True)
-
-    async def get_routes(self, distributor_id: Union[str, int]):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BC.D0.B0.D1.80.D1.88.D1.80.D1.83.D1.82.D0.BE.D0.B2_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
-        Возвращает список всех маршрутов поставщика.
-
-
-        :param distributor_id: 	Идентификатор поставщика
-        :type distributor_id: str or int
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Distributors.GET_SUPPLIER_ROUTES, payload)
-
-    async def edit_route(self,
-                         route_id: Union[str, int],
-                         deadline: Union[str, int] = None, deadline_replace: str = None,
-                         is_deadline_replace_franch_enabled: Union[str, bool] = None,
-                         deadline_max: Union[str, int] = None,
-                         normal_time_start: str = None, normal_time_end: str = None,
-                         normal_days_of_week: List = None,
-                         abnormal_deadline: Union[str, int] = None,
-                         abnormal_deadline_max: Union[str, int] = None,
-                         p1: Union[str, int] = None, p2: Union[str, int] = None,
-                         price_per_kg: Union[str, int] = None,
-                         price_up_added: Union[str, int] = None,
-                         c1: Union[str, int] = None,
-                         price_up_min: Union[str, int] = None, price_up_max: Union[str, int] = None,
-                         primary_price_up_to_contractor: Union[str, int] = None,
-                         delivery_probability: Union[str, int] = None,
-                         description: str = None,
-                         enable_color: Union[str, bool] = None, color: str = None,
-                         is_abnormal_color_enabled: Union[str, bool] = None, abnormal_color: str = None,
-                         no_return: Union[bool, str] = None,
-                         supplier_code_enabled_list: Union[List, List, str, int] = None,
-                         supplier_code_disabled_list: Union[List, List, str, int] = None,
-                         normal_time_display_only: Union[int, str] = None,
-                         disable_order_abnormal_time: Union[int, str] = None,
-                         not_use_online_supplier_deadline: Union[int, str] = None,
-                         ):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B4.D0.B0.D0.BD.D0.BD.D1.8B.D1.85_.D0.BC.D0.B0.D1.80.D1.88.D1.80.D1.83.D1.82.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
-        Осуществляет обновление данных маршрута поставщика, присланных в запросе.
-        При изменении данных маршрута необязательно передавать все параметры.
-        Используйте в запросе только те данные, которые вы собираетесь изменить.
-
-
-
-        :param route_id: Идентификатор маршрута поставщика
-        :type route_id: int or str
-        :param deadline: Срок поставки (часов)
-        :type deadline: int or str
-        :param deadline_replace: Текстовое значение для "Срока поставки"
-        :type deadline_replace: str
-        :param is_deadline_replace_franch_enabled: Передавать текстовое значение для "Срока поставки" франчайзи
-        :type is_deadline_replace_franch_enabled: bool or str
-        :param deadline_max: Максимальный срок поставки (часов)
-        :type deadline_max: int or str
-        :param normal_time_start:Начало рабочего времени (09:00)
-        :type normal_time_start: str
-        :param normal_time_end:Конец рабочего времени (09:00)
-        :type normal_time_end: str
-        :param normal_days_of_week:Стандартные дни недели ['Вт', 'Ср']
-        :type normal_days_of_week: list
-        :param abnormal_deadline:Срок поставки (вне стандартного времени)
-        :param abnormal_deadline_max:	Максимальный срок поставки (вне стандартного времени)
-        :param p1: Первичная наценка 10
-        :type p1: str or int
-        :param p2: Вторичная наценка
-        :type p2: str or int
-        :param price_per_kg: Стоимость 1КГ (в валюте поставщика) 200
-        :type price_per_kg: str or int
-        :param price_up_added:Добавочная наценка 3
-        :type price_up_added: str or int
-        :param c1: Коэффициент наценки 0 - 100
-        :type c1: str or int
-        :param price_up_min:Минимальная наценка
-        :type price_up_min:int or str
-        :param price_up_max:Максимальная наценка
-        :type price_up_max:int or str
-        :param primary_price_up_to_contractor:Приоритетная (если выше) наценка для клиента
-        :type primary_price_up_to_contractor: int or str
-        :param delivery_probability:Вероятность поставки (в процентах) %
-        :type delivery_probability: int or str
-        :param description:Краткое описание маршрута
-        :type description: str
-        :param enable_color:Выделять цветом 'false' or False
-        :type enable_color: bool or str
-        :param color: Цвет в HEX
-        :type color: str
-        :param is_abnormal_color_enabled: 	Выделять цветом в нерабочее время 'false' or False
-        :type is_abnormal_color_enabled: bool or str
-        :param abnormal_color:Цвет в HEX
-        :type abnormal_color: str
-        :param no_return:Без возврата 'false' or False
-        :type no_return: bool or str
-        :param supplier_code_enabled_list: Ограничить выдачу складами (массив)
-        :type supplier_code_enabled_list list or str
-        :param supplier_code_disabled_list: Исключить позиции по складам (массив)
-        :type supplier_code_disabled_list list or str
-        :param normal_time_display_only:Показывать только в стандартное время (0 - Нет, 1 - Да)
-        :type normal_time_display_only: int or str
-        :param disable_order_abnormal_time:Блокировать отправку заказа в нестандартное время (0 - Нет, 1 - Да). "1" сохраняется только при normalTimeDisplayOnly=1.
-        :type disable_order_abnormal_time: int or str
-        :param not_use_online_supplier_deadline: Не использовать срок поставки online-поставщика (0 - Нет, 1 - Да)
-        :type not_use_online_supplier_deadline: int or str
-        :return: dict
-        """
-        if supplier_code_enabled_list is not None and not isinstance(supplier_code_enabled_list, list):
-            supplier_code_enabled_list = [supplier_code_enabled_list]
-        if supplier_code_disabled_list is not None and isinstance(supplier_code_disabled_list, list):
-            supplier_code_disabled_list = [supplier_code_disabled_list]
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Admin.Distributors.UPDATE_ROUTE, payload, True)
-
-    async def edit_route_status(self, route_id: Union[str, int], status: Union[int, bool]):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.98.D0.B7.D0.BC.D0.B5.D0.BD.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.B0_.D0.BC.D0.B0.D1.80.D1.88.D1.80.D1.83.D1.82.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
-
-        Изменяет статус маршрута поставщика
-
-
-        :param route_id:	Идентификатор маршрута поставщика
-        :type route_id: int or str
-        :param status:  Значение нового статуса (1-вкл., 0-выкл.)
-        :type route_id: int or str
-        :return: dict
-        """
-        if isinstance(status, bool):
-            status = int(status)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Distributors.UPDATE_ROUTE_STATUS, payload, True)
-
-    async def delete_route(self, route_id: Union[int, str]):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.A3.D0.B4.D0.B0.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BC.D0.B0.D1.80.D1.88.D1.80.D1.83.D1.82.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
-        Удаляет маршрут поставщика.
-
-
-        :param route_id:Идентификатор маршрута поставщика
-        :type route_id: int or str
-        :return: dict
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Distributors.DELETE_ROUTE, payload, True)
-
-    async def connect_to_office(self, office_id: Union[str, int],
-                                distributors: Union[List[Dict], Dict] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.B4.D0.BA.D0.BB.D1.8E.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.BE.D0.B2_.D0.BA_.D0.BE.D1.84.D0.B8.D1.81.D1.83
-
-        Подключение/отключение поставщиков к офисам
-        Если параметр distributors не указан или содержит пустой список все поставщики офиса будут отключены
-
-
-        :param office_id: Идентификатор офиса.
-        :type office_id: int or str
-        :param distributors: Массив поставщиков, если параметр не передан или содержит пустое значение - отключаются все поставщики указанного офиса.
-        :type distributors List[Dict] or Dict
-        :return: dict
-        """
-        if isinstance(distributors, dict):
-            distributors = [distributors]
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Distributors.EDIT_SUPPLIER_STATUS_FOR_OFFICE, payload, True)
-
-    async def get_office_distributors(self, office_id: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.BE.D0.B2_.D0.BE.D1.84.D0.B8.D1.81.D0.B0
-        Возвращает информацию о подключенных к офису поставщиках
-
-
-        :param office_id: Идентификатор офиса. Если параметр не указан то в ответе возвращаются данные по всем офисам
-        :type office_id: str or int
-        :return:dict
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Distributors.GET_OFFICE_SUPPLIERS, payload)
-
-    async def pricelist_update(self, distributor_id: Union[str, int],
-                               upload_file: Union[str, BufferedReader],
-                               file_type_id: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.97.D0.B0.D0.B3.D1.80.D1.83.D0.B7.D0.BA.D0.B0_.D0.BF.D1.80.D0.B0.D0.B9.D1.81-.D0.BB.D0.B8.D1.81.D1.82.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
-        В ПУ, в разделе "Поставщики"/"Обн."/"Конфигурация прайс-листа" предварительно настраивается конфигурация
-        загружаемого прайс-листа. Специальных требований к прайс-листу нет, есть только обычные: наличие колонок
-        с ценой, брендом, каталожным номером, описанием, наличием. На вкладке "Загрузка прайс-листа" может быть
-        выбран любой способ загрузки
-
-
-        :param distributor_id: Id поставщика
-        :type distributor_id: :obj:`Union[str, int]`
-        :param upload_file: путь до файла прайс-листа
-        :type upload_file: :obj:`str` or :obj:`BufferedReader`
-        :param file_type_id: Смысла от параметра пока нет (15.05.2022)
-
-        :return: dict
-        """
-
-        payload = generate_file_payload(exclude=['upload_file'], **locals())
-        return await self._base.request(_Methods.Admin.Distributors.UPLOAD_PRICE, payload, True)
-
-
-class Catalog:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def info(self, goods_group: str, locale: str = 'ru_RU'):
-        """
-
-        :param goods_group:
-        :param locale:
-        :return:
-        """
-        payload = generate_payload(exclude=['goods_group'], **locals())
-        return await self._base.request(_Methods.Admin.Catalog.INFO, payload)
-
-    async def search(self, goods_group: str,
-                     properties: Union[List[Dict[str, str]], Dict[str, str]],
-                     skip: Optional[int] = None, limit: Optional[int] = None,
-                     locale: Optional[str] = None):
-        """
-
-        :param goods_group:
-        :param properties:
-        :param skip:
-        :param limit:
-        :param locale:
-        :return:
-        """
-        if isinstance(properties, dict):
-            properties = [properties]
-        payload = generate_payload(exclude=['goods_group', 'properties'], **locals())
-        return await self._base.request(_Methods.Admin.Catalog.SEARCH, payload, True)
-
-    async def info_batch(self, articles_catalog: Union[List[Dict[str, str]], Dict[str, str]], locale: str = 'ru_RU'):
-        if isinstance(articles_catalog, dict):
-            articles_catalog = [articles_catalog]
-        payload = generate_payload(exclude=['articles_catalog'], **locals())
-        return await self._base.request(_Methods.Admin.Catalog.INFO_BATCH, payload, True)
-
-
-class UsersCatalog:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def upload(self, catalog_id: Union[str, int],
-                     file: Union[str, BufferedReader],
-                     delete_old_mode: int = 0,
-                     default_attributes_hide: Union[str, bool] = 'false',
-                     article_only: Union[str, bool] = 'false',
-                     image_upload_mode: int = 0,
-                     image_archive: Union[str, BufferedReader] = None):
-        """
-
-        :param catalog_id:
-        :param file:
-        :param delete_old_mode:
-        :param default_attributes_hide:
-        :param article_only:
-        :param image_upload_mode:
-        :param image_archive:
-        :return:
-        """
-        if not 0 <= delete_old_mode <= 2:
-            raise AbcpWrongParameterError('Параметр "delete_old_mode" должен быть в диапазоне от 0 до 2')
-
-        if isinstance(default_attributes_hide, bool):
-            default_attributes_hide = str(default_attributes_hide).lower()
-
-        if isinstance(article_only, bool):
-            article_only = str(article_only).lower()
-
-        if image_upload_mode == 1 and image_archive is None:
-            raise AbcpWrongParameterError('Не передан архив с изображениями')
-
-        payload = generate_file_payload(exclude=['file', 'image_archive', 'catalog_id'], max_size=100, **locals())
-        return await self._base.request(_Methods.Admin.UsersCatalog.UPLOAD.format(catalog_id), payload, True)
-
-
-class Payment:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def token(self, number: Union[str, int]):
-        """
-        Получение ссылки на оплату заказа
-
-        :param number: Онлайн-номер заказа
-        :return:
-        """
-        if isinstance(number, str) and not number.isdigit():
-            raise AbcpWrongParameterError('Параметр "number" должен быть числом')
-
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Payment.TOKEN, payload)
-
-    async def top_balance_link(self, client_id: Union[str, int], amount: Union[float, int, str]):
-        """
-
-        :param client_id: Идентификатор клиента
-        :param amount: Сумма пополнения баланса
-        :return:
-        """
-        if isinstance(client_id, str) and not client_id.isdigit():
-            raise AbcpWrongParameterError('Параметр "client_id" должен быть числом')
-        if isinstance(amount, str) and not amount.isdigit():
-            raise AbcpWrongParameterError('Параметр "amount" должен быть числом')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Admin.Payment.TOP_BALANCE, payload)
+#!/usr/bin/python
+# -*- coding: utf-8 -*-
+from datetime import datetime
+from io import BufferedReader
+from typing import Dict, List, Optional, Union
+
+from ..api import _Methods
+from ..base import BaseAbcp
+from ..exceptions import AbcpAPIError, AbcpParameterRequired, AbcpWrongParameterError
+from ..utils.payload import generate_payload, generate_payload_filter, generate_payload_payments, \
+    generate_payload_online_order, generate_file_payload
+
+
+class AdminApi:
+    def __init__(self, base: BaseAbcp):
+        """
+        Класс содержит методы административного интерфейса
+
+        https://www.abcp.ru/wiki/API.ABCP.Admin
+        """
+        self._base = base
+        self.orders = Orders(base)
+        self.finance = Finance(base)
+        self.users = Users(base)
+        self.staff = Staff(base)
+        self.statuses = Statuses(base)
+        self.distributors = Distributors(base)
+        self.catalog = Catalog(base)
+        self.articles = Articles(base)
+        self.users_catalog = UsersCatalog(base)
+        self.payment = Payment(base)
+
+
+class Orders:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get_orders_list(
+            self,
+            date_created_start: Union[str, datetime] = None,
+            date_created_end: Union[str, datetime] = None,
+            date_updated_start: Union[str, datetime] = None,
+            date_updated_end: Union[str, datetime] = None,
+            numbers: Union[str, int, List] = None,
+            internal_numbers: Optional[List] = None,
+            status_code: Union[str, int, List] = None,
+            office_id: Union[int, str] = None,
+            distributor_order_id: Union[int, str] = None,
+            is_canceled: Union[int, str] = None,
+            distributor_id: Union[str, int, List] = None,
+            user_id: Union[int, str] = None,
+            with_deleted: Union[str, bool] = None,
+            format: Optional[str] = None,
+            limit: Optional[int] = None,
+            skip: Optional[int] = None,
+            desc: Optional[bool] = None
+
+    ):
+        """Принимает в качестве параметров условия фильтрации заказов. Возвращает список заказов (в т.ч. список позиций заказа).
+
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.BE.D0.B2
+
+
+
+        :param user_id: Идентификатор клиента (покупателя). В результате вернутся все заказы, сделанные указанным клиентом.
+        :param date_created_start: Начальная дата размещения заказа `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_created_start: `str` or `datetime`
+        :param date_created_end: Конечная дата размещения заказа
+        :type date_created_end: `str` or `datetime`
+        :param date_updated_start: Начальная дата последнего обновления заказа в формате `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_updated_start: `str` or `datetime`
+        :param date_updated_end: Конечная дата последнего обновления заказа в формате `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_updated_end: `str` or `datetime`
+        :param numbers: Массив номеров заказов
+        :type numbers: list
+        :param internal_numbers: Массив номеров заказов в учетной системе (например, в 1С). Используется только, если в параметрах запроса не задан numbers.
+        :type internal_numbers: list
+        :param status_code: Код статус позиции заказа (один или массив кодов). Будут выбраны заказы содержащие хотя бы одну позицию в данном статусе.
+        :type status_code: Union[str, int, list]
+        :param office_id: Идентификатор офиса (в ответе по параметру могут быть отфильтрованы заказы где этот офис выбран как самовывоз или если это офис клиента или если менеджер клиента, сделавшего заказ, относится к данному офису)
+        :type office_id: int or str
+        :param distributor_order_id: Идентификатор заказа у поставщика. В результате вернутся все заказы которые были отправлены поставщику под этим номером.
+        :type distributor_order_id: int or str
+        :param is_canceled: Флаг "Запрос на удаление позиции". 0 - запрос не был отправлен, 1 - запрос отправлен, 2 - запрос отклонен менеджером.
+        :type is_canceled: int or str
+        :param distributor_id: Идентификатор (один или массив идентификаторов) поставщика. В результате вернутся все заказы, содержащие хотя бы одну позицию от указанного поставщика.
+        :type distributor_id: Union[str, int, list]
+        :param with_deleted: Признак, возвращать ли в ответе удаленные заказы и позиции
+        :type with_deleted: str or bool ('true', 'false', True, False)
+        :param format: Формат ответа. Доступные значения: <br>
+               additional - дописывает к заказу данные клиента при гостевом заказе; к позициям добавляет значение vinQueryIds
+               <br>short - сокращенный вариант отображения без содержимого позиций заказов
+               <br>count - возвращает только количество заказов по заданным условиям
+               <br>status_only - возвращает только номер заказа, а в узле позиций: id, statusCode, brand, number, numberFix, code
+               <br>p - заказы содержатся в поле items, данные о количестве содержатся в поле count
+        :type format: str
+        :param limit: Ограничение на возвращаемое кол-во
+        :type limit: int
+        :param skip: Сколько заказов пропустить
+        :type skip: int
+        :param desc: Обратный порядок
+        :type desc: : bool
+
+
+        """
+        if isinstance(date_created_start, datetime):
+            date_created_start = f'{date_created_start:%Y-%m-%d %H:%M:%S}'
+        if isinstance(date_created_end, datetime):
+            date_created_end = f'{date_created_end:%Y-%m-%d %H:%M:%S}'
+        if isinstance(date_updated_start, datetime):
+            date_updated_start = f'{date_updated_start:%Y-%m-%d %H:%M:%S}'
+        if isinstance(date_updated_end, datetime):
+            date_updated_end = f'{date_updated_end:%Y-%m-%d %H:%M:%S}'
+        if isinstance(format, str) and format not in ["additional", "short", "count", "status_only", "p"]:
+            raise AbcpWrongParameterError(
+                'Параметр "format" должен принимать одно из значений ["additional", "short", "count", "status_only", "p"]')
+        if limit is not None and not 1 <= int(limit) <= 1000:
+            raise AbcpAPIError(f'The limit must be more than {limit}')
+        if isinstance(status_code, (int, str)):
+            status_code = [status_code]
+        if not isinstance(numbers, list) and numbers is not None:
+            numbers = [numbers]
+        if isinstance(user_id, str) and not user_id.isdigit():
+            raise AbcpAPIError(f'Параметр user_id должен быть числом')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Orders.GET_ORDERS_LIST, payload)
+
+    async def get_order(
+            self,
+            number: Union[int, str] = None,
+            internal_number: Union[int, str] = None,
+            with_deleted: Union[str, bool] = None,
+            format: str = None
+
+    ):
+        """Принимает в качестве параметра онлайн-номер заказа. Возвращает информацию о заказе (в т.ч. список позиций заказа).
+
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BE_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B5
+
+
+        :param number: Номер заказа int или str
+        :type number: int or str
+        :param internal_number: Массив номеров заказов в учетной системе (например, в 1С).
+                Используется только, если в параметрах запроса не задан numbers.
+        :type internal_number: int or str
+        :param with_deleted: Признак, возвращать ли в ответе удаленные заказы и позиции
+        :type with_deleted: str or bool ('true', 'false', True, False)
+        :param format: Формат ответа. Доступные значения
+               additional - дописывает к заказу данные клиента при гостевом заказе; к позициям добавляет значение vinQueryIds
+               short - сокращенный вариант отображения без содержимого позиций заказов
+               count - возвращает только количество заказов по заданным условиям
+               status_only - возвращает только номер заказа, а в узле позиций: id, statusCode, brand, number, numberFix, code
+               p - заказы содержатся в поле items, данные о количестве содержатся в поле count
+        :type format: str
+
+        """
+        if number is None and internal_number is None:
+            raise AbcpParameterRequired(f'Один из параметров "number" или "internal_number" должен быть указан')
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Admin.Orders.GET_ORDER, payload)
+
+    async def status_history(
+            self,
+            position_id: Union[int, str]
+
+    ):
+        """Принимает в качестве параметра id позиции заказа. Возвращает информацию об истории изменений статуса позиции заказа.
+
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D1.81.D1.82.D0.BE.D1.80.D0.B8.D0.B8_.D0.B8.D0.B7.D0.BC.D0.B5.D0.BD.D0.B5.D0.BD.D0.B8.D0.B9_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.B0_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B0
+
+
+        :param position_id: Номер заказа int или str
+        :type position_id int or str
+
+
+        """
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Admin.Orders.STATUS_HISTORY, payload)
+
+    async def create_or_edit_order(
+            self,
+            number: Union[int, str] = None,
+            internal_number: Union[int, str] = None,
+            user_id: Union[int, str] = None,
+            date: Union[str, datetime] = None,
+            comment: str = None,
+            order_positions: Union[List[Dict], Dict] = None,
+            delivery_type_id: Union[int, str] = None,
+            delivery_office_id: Union[int, str] = None,
+            basket_id: Union[int, str] = None,
+            guest_order_name: str = None,
+            guest_order_mobile: str = None,
+            guest_order_email: str = None,
+            shipment_date: Union[str, datetime] = None,
+            delivery_cost: Union[str, int, float] = None,
+            delivery_address_id: Union[int, str] = None,
+            delivery_address: str = None,
+            manager_id: Union[int, str] = None,
+            client_order_number: str = None,
+            note: str = None,
+            del_note: Union[str, int] = None
+
+    ):
+        """Универсальный метод сохранения. Принимает в качестве параметра объект описывающий заказ. Для создания заказа
+         от имени Гостя, необходимо передавать корректно заполненные параметры: guestOrderName и guestOrderMobile или guestOrderEmail,
+          в зависимости от обязательности полей "Мобильный" или "Email" в форме создания гостевого заказа.
+
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.A1.D0.BE.D1.85.D1.80.D0.B0.D0.BD.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B0
+
+
+        :param manager_id: id менеджера по заказу
+        :param comment: Комментарий к заказу
+        :param date: Дата заказа `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param number: Онлайн-номер заказа
+        :type number: int or str
+        :param internal_number: Внутренний номер заказа, обязательный параметр для создания<br><br>
+        :type internal_number int or str
+        :param order_positions: Список словарей описывающих позиции, читайте документацию API.ABCP.Admin<br>В случае
+         редактирования заказа, могут быть указаны только позиции и поля, которые требуют изменения. В случае создания
+         заказа, должны быть указаны все позиции со всеми полями (кроме полей comment, supplierCode и itemKey).
+         При редактировании позиций обязательна передача параметра id. Если параметр id не передан, будет добавлена новая позиция.
+          При добавлении позиции все поля (кроме полей comment, supplierCode и itemKey) для нее являются обязательными. Для удаления позиции необходимо указать ей количество 0 или установить параметр delete в значение 1.<br><br>
+        :type order_positions: list of dictionaries
+        :param client_order_number: Номер заказа в системе учета клиента<br><br>
+        :type client_order_number: int or str
+        :param user_id: Идентификатор клиента на сайте, для которого создается заказ. Обязательный параметр, если создается заказ на клиента или сотрудника<br>
+        :type user_id: int or str
+        :param delivery_type_id: Тип доставки<br>
+        :type delivery_type_id: int or str
+        :param delivery_office_id: Идентификатор офиса самовывоза <br>
+        :type delivery_office_id: int or str
+        :param basket_id: 	Необязательный параметр - идентификатор корзины при использовании мультикорзины<br>
+        :type basket_id: int or str
+        :param guest_order_name: Необязательный параметр - имя клиента для оформления заказа от имени Гостя.
+         Для корректного оформления заказа под гостем должны быть указаны параметры guestOrderName и guestOrderMobile или
+          guestOrderEmail.
+        :type guest_order_name: str
+        :param guest_order_mobile: Необязательный параметр - контактный телефон клиента для оформления заказа от имени
+         Гостя. (в формате 70000000000). Для корректного оформления заказа под гостем должны быть указаны параметры
+          guestOrderName и guestOrderMobile или guestOrderEmail.
+        :type guest_order_mobile: str
+        :param guest_order_email: Необязательный параметр - e-mail для оформления заказа от имени Гостя.
+        (в формате user@domain.com). Для корректного оформления заказа под гостем должны быть указаны параметры guestOrderName и guestOrderMobile или guestOrderEmail.
+        :type guest_order_email: str
+        :param shipment_date: Дата доставки  `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type shipment_date: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param delivery_cost: Цена доставки
+        :type delivery_cost: int or float
+        :param delivery_address_id: Число. Идентификатор адреса доставки. Если нужно создать новый адрес, то нужно передать "-1" и в параметре deliveryAddress новый адрес доставки.
+        :type delivery_address_id: str or int
+        :param delivery_address: Текст. Адрес доставки, в случае, когда необходимо сразу создать новый адрес нужно в deliveryAddressId передавать "-1" + адрес доставки
+        :type delivery_address: str
+        :param note: Текст заметки администратора API
+        :type note: str
+        :param del_note: ID удаляемой заметки, value будет пустым
+        :type del_note: str, int
+
+
+        """
+        if isinstance(shipment_date, datetime):
+            shipment_date = f'{shipment_date:%Y-%m-%d %H:%M:%S}'
+        if isinstance(date, datetime):
+            date = f'{date:%Y-%m-%d %H:%M:%S}'
+        if isinstance(order_positions, dict):
+            order_positions = [order_positions]
+        if number is None and internal_number is None:
+            raise AbcpParameterRequired('number and internal_number is None')
+        if delivery_address_id is not None and int(delivery_address_id) == -1 and delivery_address is None:
+            raise AbcpAPIError('Не передан новый адрес доставки')
+        if delivery_cost is not None and delivery_address_id is None:
+            raise AbcpParameterRequired(
+                'Необходимо указать delivery_address_id если это существующий адрес '
+                'или delivery_address_id=-1 и новый delivery_address.')
+        if delivery_address_id is not None and delivery_type_id is None:
+            raise AbcpParameterRequired(
+                'Необходимо передать delivery_type_id чтобы установить адрес доставки')
+        if any(x is not None for x in [number, internal_number]) and all(
+                [order_positions, user_id, delivery_type_id, delivery_office_id, basket_id, guest_order_name,
+                 guest_order_mobile, guest_order_email, shipment_date, delivery_cost, delivery_address_id,
+                 delivery_address, client_order_number]) is None:
+            raise AbcpParameterRequired('Недостаточно параметров')
+        if note is not None and del_note is not None:
+            raise AbcpAPIError('Заметку можно либо удалить либо добавить')
+
+        payload = generate_payload(exclude=['client_order_number', 'order_positions', 'note', 'del_note'], order=True,
+                                   **locals())
+
+        return await self._base.request(_Methods.Admin.Orders.SAVE_ORDER, payload, True)
+
+    async def get_online_order_params(
+            self,
+            position_ids: Union[List, str, int]
+
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.B0.D1.80.D0.B0.D0.BC.D0.B5.D1.82.D1.80.D0.BE.D0.B2_.D0.B4.D0.BB.D1.8F_.D0.BE.D1.82.D0.BF.D1.80.D0.B0.D0.B2.D0.BA.D0.B8_online-.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D1.83
+        Это вспомогательная операция, которую необходимо выполнять перед отправкой online-заказа поставщику. Если
+        для поставщика есть дополнительные параметры заказа или позиций заказа, то в ответ вы получите набор данных.
+        На их основании нужно составить API запрос для отправки заказа. Если вы уже определились с какими параметрами
+        будете отправлять заказы поставщику, то эту операцию вызывать нет необходимости, можно сразу переходить к
+        методу отправки заказа.
+        Идентификаторы позиций, которые необходимо передавать в запросе,
+        должны принадлежать одному поставщику. Т.е. за один API запрос операции cp/orders/online можно отправить
+        позиции только одного поставщика. Если вам необходимо отправить позиции для двух поставщиков, то необходимо
+        предварительно сгруппировать идентификаторы позиций и выполнить два запроса к cp/orders/online по каждому из
+        поставщиков.
+        Кол-во идентификаторов позиций в одном запросе ограничено. За один API запрос отправить в заказ можно не
+        более 20 позиций для сторонних поставщиков. Для поставщиков работающих на платформе ABCP ограничение - 100
+        позиций.
+
+
+        :param position_ids: Массив идентификаторов позиций, которые нужно отправить поставщику (Позиции должны быть от одного поставщика)
+        :type position_ids: List of ids str or int no matter
+
+        """
+        if not isinstance(position_ids, list):
+            position_ids = [position_ids]
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Admin.Orders.ONLINE_ORDER, payload)
+
+    async def send_online_order(
+            self,
+            order_params: Union[List[Dict], Dict],
+            positions: Union[List[Dict], Dict],
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D1.82.D0.BF.D1.80.D0.B0.D0.B2.D0.BA.D0.B0_online-.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D1.83
+        Идентификаторы позиций, которые необходимо передавать в запросе, должны принадлежать одному поставщику.
+        Т.е. за один API запрос операции cp/orders/online можно отправить позиции только одного поставщика. Если вам
+        необходимо отправить позиции для двух поставщиков, то необходимо предварительно сгруппировать идентификаторы
+        позиций и выполнить два запроса к cp/orders/online по каждому из поставщиков. Кол-во идентификаторов позиций
+        в одном запросе ограничено. За один API запрос отправить в заказ можно не более 20 позиций для сторонних
+        поставщиков. Для поставщиков работающих на платформе ABCP ограничение - 100 позиций. В ответ вы можете
+        получить один или несколько созданных заказов. Отправка заказа аналогична отправке из панели управления. Если
+        заказ оформлен успешно, то результат фиксируется в панели управления, чекбокс заменятся на номер заказа
+        поставщика и его статус (если поставщик поддерживает передачу статуса). Если настроена синхронизация
+        статусов, она также активируется для отправленных позиций. Внимание! При работе с API поставщика,
+        в большинстве случаев используется общая корзина при работе с сайтом поставщика и при работе с API. При
+        отправке заказа поставщику последовательно выполняются запросы по предварительной очистке корзины,
+        добавлению товара в корзину, чтение и отправка её в заказ. Очень важно не допустить параллельной отправки
+        разных позиций одному поставщику. Так же в момент отправки заказа поставщику не должна производиться отправка
+        заказов из панели управления abcp и работа с корзиной на сайте поставщика. В противном случае вы можете
+        получить некорректные заказы, ошибки и задвоенные заказы с одинаковыми товарами.
+
+
+        :param order_params: Массив параметров заказа, который нужно сформировать на основе операции "Получение параметров для отправки online-заказа поставщику". Если у поставщика нет параметров заказа, то параметр orderParams необязательный.
+        :type order_params: List of dict example: [{'shipmentAddress': 77333, 'comment': 'Мой коментарий', 'deliveryType': 3, 'contactName': 'Иванов Иван'}]
+        :param positions: Массив данных с позициями заказов
+        d = await api.cp.admin.get_online_order_params(id=222)
+        order_params={d['orderParams'][0]['fieldName']: d['orderParams'][0]['enum'][2]['value']}, positions={'id': 263266039, 'comment': 'тест'}
+        :type positions: List of ids, str or int
+        """
+        if not isinstance(positions, list):
+            positions = [positions]
+
+        if isinstance(order_params, dict):
+            order_params = [order_params]
+        payload = generate_payload_online_order(**locals())
+
+        return await self._base.request(_Methods.Admin.Orders.ONLINE_ORDER, payload, True)
+
+
+class Finance:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def update_balance(
+            self,
+            user_id: Union[int, str],
+            balance: Union[float, int, str],
+            in_stop_list: Union[bool, str] = None
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B1.D0.B0.D0.BB.D0.B0.D0.BD.D1.81.D0.B0_.D0.BA.D0.BB.D0.B8.D0.B5.D0.BD.D1.82.D0.B0
+        Изменяет баланс клиента. Принимает в качестве параметра текущий баланс пользователя (float) в валюте сайта
+        и идентификатор пользователя на сайте. Идентификатор пользователя - это уникальное значение для всей системы,
+        которое может не совпадать со значением поля "Код клиента" в карточке клиента. Узнать его можно, либо из URL
+        карточки клиента, например, https://cp.abcp.ru/?page=customers&customerId=353169&action=editCustomer - в
+        данном случае идентификатор клиента это значение параметра customerId, а именно, 353169; либо,
+        при использовании синхронизации пользователей с помощью операции GET cp/users, идентификатор пользователя
+        возвращается в поле userId.
+        !!!Обновляет сальдо в карточке клиента(видно при редактировани), не влияет на модуль финансы, возможно я ошибаюсь!!!
+
+
+        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
+        :type user_id: int or str
+        :param balance: Значение баланса в валюте сайта
+        :type balance: float
+        :param in_stop_list: Признак нахождения клиента в стоп-листе (необязательный параметр)
+        :type in_stop_list: str or bool ('true', 'false', True, False)
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Finance.UPDATE_BALANCE, payload, True)
+
+    async def update_credit_limit(
+            self,
+            user_id: Union[int, str],
+            credit_limit: Union[float, int, str]
+
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BB.D0.B8.D0.BC.D0.B8.D1.82.D0.B0_.D0.BA.D1.80.D0.B5.D0.B4.D0.B8.D1.82.D0.B0_.D0.BA.D0.BB.D0.B8.D0.B5.D0.BD.D1.82.D0.B0
+        Изменяет лимит кредита клиента. Принимает в качестве параметра текущий лимит кредита пользователя (float) в валюте сайта и идентификатор пользователя на сайте.
+        !!!В случае успешного обновления баланса, метода возвращает:
+        userId, creditLimit и excludeCart. Параметр excludeCart не указан в документации метода!!!
+
+
+        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
+        :type user_id: int or str
+        :param credit_limit: Значение лимита кредита в валюте сайта
+        :type credit_limit: float
+        """
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Admin.Finance.UPDATE_CREDIT_LIMIT, payload, True)
+
+    async def update_finance_info(
+            self,
+            user_id: Union[int, str],
+            balance: Union[float, int, str] = None,
+            credit_limit: float = None,
+            in_stop_list: Union[bool, str] = None,
+            pay_delay: Union[int, str] = None,
+            overdue_saldo: Union[float, int, str] = None
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D1.84.D0.B8.D0.BD.D0.B0.D0.BD.D1.81.D0.BE.D0.B2.D0.BE.D0.B9_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BA.D0.BB.D0.B8.D0.B5.D0.BD.D1.82.D0.B0
+        Изменяет финансовую информацию клиента. Принимает в качестве параметров идентификатор пользователя на
+        сайте и финансовую информацию пользователя. Обязательно наличие как минимум одного из полей (balance,
+        creditLimit, inStopList, payDelay, overdueSaldo).
+
+
+        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
+        :type user_id: int or str
+        :param balance: Значение баланса в валюте сайта
+        :type balance: float
+        :param credit_limit: Значение лимита кредита в валюте сайта
+        :type credit_limit: float
+        :param in_stop_list: Признак нахождения клиента в стоп-листе
+        :type in_stop_list: str or bool ('true', 'false', True, False)
+        :param pay_delay: Отсрочка платежа(в днях)
+        :type pay_delay: int or str
+        :param overdue_saldo: Просроченный баланс
+        :type overdue_saldo: float
+        """
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Admin.Finance.UPDATE_FINANCE_INFO, payload, True)
+
+    async def get_payments_info(
+            self,
+            user_id: Union[int, str] = None,
+            payment_number: str = None,
+            create_date_time_start: Union[str, datetime] = None,
+            create_date_time_end: Union[str, datetime] = None
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BE.D0.B1_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82.D0.B0.D1.85_.D0.B8.D0.B7_.D1.84.D0.B8.D0.BD.D0.BC.D0.BE.D0.B4.D1.83.D0.BB.D1.8F
+        Возвращает список оплат из финмодуля.
+        Параметры paymentNumber, userId необязательные.
+        Если указан paymentNumber, то createDateTimeStart и createDateTimeEnd могут не указываться.
+        Если интервал дат выбран больше года, то в ответе получаем ошибку "Сократите диапазон дат и выполните запрос снова.
+        Диапазон не должен превышать 1 год."
+
+
+        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
+        :type user_id: int or str
+        :param payment_number: 	Номер платежа
+        :type payment_number: str
+        :param create_date_time_start: Начальная дата создания `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type create_date_time_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param create_date_time_end: Конечная дата создания `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type create_date_time_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+
+        """
+        if isinstance(create_date_time_start, datetime):
+            create_date_time_start = f'{create_date_time_start:%Y-%m-%d %H:%M:%S}'
+        if isinstance(create_date_time_end, datetime):
+            create_date_time_end = f'{create_date_time_end:%Y-%m-%d %H:%M:%S}'
+        if all(x is None for x in [user_id, payment_number, create_date_time_start, create_date_time_end]):
+            raise AbcpAPIError('Недостаточно параметров')
+        if payment_number is None and any(x is None for x in [create_date_time_start, create_date_time_end]):
+            raise AbcpAPIError('Недостаточно параметров')
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Admin.Finance.GET_PAYMENTS, payload)
+
+    async def get_payment_links(
+            self,
+            payment_numbers: Union[List, str, int] = None,
+            order_ids: Union[List, str, int] = None,
+            user_id: Union[int, str] = None,
+            date_time_start: Union[str, datetime] = None,
+            date_time_end: Union[str, datetime] = None,
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BE_.D0.BF.D1.80.D0.B8.D0.B2.D1.8F.D0.B7.D0.BA.D0.B0.D1.85_.D0.BF.D0.BB.D0.B0.D1.82.D0.B5.D0.B6.D0.B5.D0.B9_.D0.B8.D0.B7_.D0.BC.D0.BE.D0.B4.D1.83.D0.BB.D1.8F_.D0.A4.D0.B8.D0.BD.D0.B0.D0.BD.D1.81.D1.8B
+        Возвращает список привязок платежей из модуля Финансы.
+        При запросе указывать либо paymentNumbers либо orderIds либо userId с DateTimeStart и DateTimeEnd.
+
+        :param user_id: Идентификатор пользователя на сайте, для которого обновляется баланс.
+        :type user_id: int or str
+        :param payment_numbers: массив с номерами платежей [str, str, str]
+        :type payment_numbers: List of str or str or int
+        :param order_ids: массив с номерами заказов,если передать 0 и диапазон дат, то можно получить список возвратов за период
+        :type order_ids: List of str or str or int
+        :param date_time_start: Начальная дата `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_time_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param date_time_end: Конечная дата  `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_time_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+
+        """
+
+        if isinstance(date_time_start, datetime):
+            date_time_start = f'{date_time_start:%Y-%m-%d %H:%M:%S}'
+        if isinstance(date_time_end, datetime):
+            date_time_end = f'{date_time_end:%Y-%m-%d %H:%M:%S}'
+        if all(x is None for x in [user_id, date_time_start, date_time_end]):
+            if any(y is not None for y in [payment_numbers, order_ids]):
+                pass
+            else:
+                raise AbcpParameterRequired(
+                    f'Недостаточно параметров, укажите user_id, date_time_start, date_time_end')
+        if not isinstance(order_ids, list) and order_ids is not None:
+            order_ids = [order_ids]
+        if not isinstance(payment_numbers, list) and payment_numbers is not None:
+            payment_numbers = [payment_numbers]
+        payload = generate_payload(exclude=['date_time_start', 'date_time_end'], **locals())
+
+        return await self._base.request(_Methods.Admin.Finance.GET_PAYMENTS_LINKS, payload)
+
+    async def get_online_payments(
+            self,
+            date_start: Union[str, datetime] = None,
+            date_end: Union[str, datetime] = None,
+            customer_ids: Union[List, int] = None,
+            payment_method_id: Union[int, str] = None,
+            status_ids: Union[List, str, int] = None,
+            order_ids: Union[List, str, int] = None
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_online_.D0.BF.D0.BB.D0.B0.D1.82.D0.B5.D0.B6.D0.B5.D0.B9
+        Возвращает список online платежей. Все параметры необязательные и принадлежат к параматерам filter
+
+
+        :param date_start: Дата начало периода для выбора платежей. `str` в формате %Y-%m-%d или %Y-%m-%d %H:%M:%S или datetime object(%Y-%m-%d)
+        :type date_start: `str` в формате %Y-%m-%d или datetime object. Для
+        :param date_end: Дата начало периода для выбора платежей. `str` в формате %Y-%m-%d или %Y-%m-%d %H:%M:%S или datetime object(%Y-%m-%d)
+        :type date_end: `str` в формате %Y-%m-%d или datetime object
+        :param customer_ids: Массив идентификаторов клиентов. Не более 100 штук в одном запросе.
+        :type customer_ids: List or str or int
+        :param payment_method_id: Идентификатор платежной системы. Получить можно из cp/users/profiles или в панели управления.
+        :type payment_method_id: str or int
+        :param status_ids: 	Массив идентификаторов статусов платежей:
+                            1 - Начата 2 - Завершена 3 - Неудача 4 - В обработке
+        :type status_ids: List or str or int
+        :param order_ids: Массив идентификаторов заказов. Не более 100 штук в одном запросе.
+        :type order_ids: List or str or int
+        """
+        if isinstance(date_start, datetime):
+            date_start = f'{date_start:%Y-%m-%d}'
+        if isinstance(date_end, datetime):
+            date_end = f'{date_end:%Y-%m-%d}'
+
+        if order_ids is not None and not isinstance(order_ids, list):
+            order_ids = [order_ids]
+        if status_ids is not None and not isinstance(status_ids, list):
+            status_ids = [status_ids]
+        if customer_ids is not None and not isinstance(customer_ids, list):
+            customer_ids = [customer_ids]
+
+        payload = generate_payload_filter(**locals())
+
+        return await self._base.request(_Methods.Admin.Finance.GET_PAYMENTS_ONLINE, payload)
+
+    async def add_multiple_payments(
+            self,
+            payments: Union[List[Dict], Dict] = None,
+            link_payments: Union[bool, int] = 0
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82
+        Добавляет платежи клиентам. Возвращает массив добавленных платежей.
+
+
+        :param payments: Массив с оплатами
+        :type payments: Union[List[Dict], Dict]
+        :param link_payments: Идентификатор платежной системы. Получить можно из cp/users/profiles или в панели управления.
+        :type link_payments: str or int
+        """
+        if isinstance(link_payments, bool):
+            link_payments = str(link_payments)
+        if type(payments) is dict:
+            payments = [payments]
+        payload = generate_payload_payments(single=False, **locals())
+
+        return await self._base.request(_Methods.Admin.Finance.ADD_PAYMENTS, payload, True)
+
+    async def add_single_payment(
+            self,
+            user_id: int,
+            payment_type_id: int,
+            amount: Union[float, int],
+            create_date_time: Union[str, datetime] = None,
+            payment_number: Union[str, int] = None,
+            comment: Optional[str] = None,
+            editor_id: Union[int, str] = None,
+            link_payments: Union[bool, int] = False
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82
+        Добавляет платежи клиентам. Возвращает массив добавленных платежей.
+
+
+        :param user_id: Идентификатор пользователя на сайте, которому добавляется оплата
+        :type user_id: int or str
+        :param create_date_time: Дата и время платежа, `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type create_date_time: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param payment_type_id: Id типа платежа
+        :type payment_type_id: str or int
+        :param amount: 	Сумма платежа
+        :type amount: float or int
+        :param payment_number: Номер платежа, максимум 64 символа. Необязательный параметр. Если передан пустой, то номер генерируется автоматически по маске переданного типа платежа
+        :type payment_number: str or int
+        :param comment: Комментарий к платежу (не обязательное)
+        :type comment: str
+        :param editor_id: Id сотрудника, которым был внесён платёж (не обязательное)
+        :type editor_id: str or int
+        :param link_payments: 	Параметр, отвечающий за автоматическую привязку платежей к заказам. 0 - не привязывать, 1 - привязывать
+        :type link_payments: int or str
+
+        """
+        if isinstance(link_payments, bool):
+            link_payments = int(link_payments)
+        if isinstance(create_date_time, datetime):
+            create_date_time = f'{create_date_time:%Y-%m-%d %H:%M:%S}'
+
+        payload = generate_payload_payments(**locals())
+
+        return await self._base.request(_Methods.Admin.Finance.ADD_PAYMENTS, payload, True)
+
+    async def delete_link_payment(
+            self,
+            payment_link_id: int
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.A3.D0.B4.D0.B0.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D1.80.D0.B8.D0.B2.D1.8F.D0.B7.D0.BA.D0.B8_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82.D1.8B
+        Удаляет привязку оплаты, увеличивает долг заказу, к которому была сделана привязка, на сумму удаляемой
+        привязки, увеличивает остаток оплаты на сумму удаляемой привязки, клиенту пересчитывает сальдо и долг по
+        заказам. Внимание!
+
+        С помощью одного запроса данная операция позволяет удалить только одну привязку. Массовое удаление недоступно
+
+
+        :param payment_link_id: Id привязки, которую нужно удалить.
+        :type payment_link_id: int or str
+        """
+
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Admin.Finance.DELETE_PAYMENT_LINK, payload, True)
+
+    async def link_existing_payment(
+            self,
+            payment_id: Union[str, int],
+            order_id: Union[str, int],
+            amount: Union[str, int, float]
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.BF.D0.B5.D1.80.D0.B0.D1.86.D0.B8.D1.8F_.D0.BF.D1.80.D0.B8.D0.B2.D1.8F.D0.B7.D0.BA.D0.B8_.D0.BF.D0.BE_.D1.80.D0.B0.D0.BD.D0.B5.D0.B5_.D0.B4.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.BD.D0.BE.D0.BC.D1.83_.D0.BF.D0.BB.D0.B0.D1.82.D0.B5.D0.B6.D1.83
+        Позволяет осуществлять привязку ранее созданного платежа
+
+
+        :param payment_id: id платежа.
+        :type payment_id: int or str
+        :param order_id: id заказа по которому делается привязка.
+        :type order_id: int or str
+        :param amount: 	Сумма привязки.
+        :type amount: str or int or float
+        """
+
+        if all(x.isdigit() for x in [payment_id, order_id, amount] if isinstance(x, str)):
+            pass
+        else:
+            raise AbcpAPIError('Все параметры должны являться цифрами')
+
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Admin.Finance.LINK_EXISTING_PLAYMENT, payload, True)
+
+    async def refund_payment(
+            self,
+            refund_payment_id: Union[str, int],
+            refund_amount: Union[str, int, float]
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.BF.D0.B5.D1.80.D0.B0.D1.86.D0.B8.D1.8F_.D0.B2.D0.BE.D0.B7.D0.B2.D1.80.D0.B0.D1.82.D0.B0_.D0.BF.D0.BB.D0.B0.D1.82.D0.B5.D0.B6.D0.B0
+        Позволяет осуществлять возврат ранее созданного платежа
+
+
+        :param refund_payment_id: id платежа.
+        :type refund_payment_id: int or str
+        :param refund_amount: Сумма возврата.
+        :type refund_amount: int or str or float
+        """
+        if not all(x.isdigit() for x in [refund_payment_id, refund_amount] if isinstance(x, str)):
+            raise AbcpAPIError('Все параметры должны являться цифрами')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Finance.REFUND_PAYMENT, payload, True)
+
+    async def delete_payment(self, payment_id: int, delete_link: Union[int, bool] = 0):
+        if isinstance(delete_link, bool):
+            delete_link = int(delete_link)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Finance.DELETE_PAYMENT, payload, True)
+
+    async def get_receipts(
+            self,
+            shop_id: Union[int, str] = None,
+            queue_id: Union[int, str] = None,
+            date_created_start: Union[str, datetime] = None,
+            date_created_end: Union[str, datetime] = None,
+            calculation_method: Union[str, int] = None,
+            print_paper_check: Union[str, int] = None,
+            vat: Union[str, int] = None,
+            calculation_subject: Union[str, int] = None,
+            payment_type: Union[str, int] = None,
+            type: Union[str, int] = None,
+            tax_system: Union[str, int] = None,
+            intent: Union[str, int] = None,
+            fiscalization: Union[str, int] = None,
+            employee_id: Union[int, str] = None,
+            client_id: Union[int, str] = None,
+            start: Union[str, int] = None,
+            rows_on_page: Union[str, int] = None,
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.87.D0.B5.D0.BA.D0.BE.D0.B2
+        Позволяет получить данные о чеках Комтет.
+
+
+        :param shop_id: ID магазина
+        :type shop_id: int or str
+        :param queue_id: ID очереди
+        :type queue_id: int or str
+        :param date_created_start: Начальная дата создания чека в формате `str` в формате %Y-%m-%d  или datetime object
+        :type date_created_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param date_created_end: Конечная дата создания чека `str` в формате %Y-%m-%d  или datetime object
+        :type date_created_end: `str` в формате %Y-%m-%d или datetime object
+        :param calculation_method: Способ расчета: 0 - Предоплата 100%, 1 - Предоплата, 2 - Полный расчет, 3 - Аванс, 4 - Частичный расчет и кредит, 5 - Оплата кредита, 6 - Передача в кредит.
+        :type calculation_method: int or str
+        :param print_paper_check: Был ли запрос печати бумажного чека: 0 - Нет, 1 - Да.
+        :type print_paper_check: int or str
+        :param vat: Налог: 5 - Без НДС, 0 - НДС по ставке 0%, 3 - НДС чека по расчетной ставке 10/110, 4 - НДС чека по расчетной ставке 20/120.
+        :type vat: int or str
+        :param calculation_subject: Предмет расчета: 0 -товар, 1 - работа, 2 - услуга, 3 - платеж.
+        :type calculation_subject: int or str
+        :param payment_type: 	Оплата: 0 - Безналичными, 1 - Наличными, 2 - Предоплата, 3 - Постоплата, 4 - Встречное предоставление.
+        :type payment_type: int or str
+        :param type: Тип чека: 0 - чек, 1- чек коррекции.
+        :param tax_system: Система налогообложения: 0 - ОСН, 1 - УСН доход, 2 - УСН доход - расход, 3 - ЕНВД, 4 - ЕСН, 5 - Патент.
+        :type tax_system: int or str
+        :param intent: Направление платежа: 0 - Приход, 1 - Расход, 2 - Возврат прихода, 3 - Возврат расхода.
+        :type intent: int or str
+        :param fiscalization: Фискализирован: 0 - Нет, 1 - Да.
+        :type fiscalization: int or str
+        :param employee_id: id сотрудника, отправившего чек.
+        :type employee_id: int or str
+        :param client_id: 	id клиента.
+        :type client_id: int or str
+        :param start: Отсчет чеков
+        :type start: int or str
+        :param rows_on_page: 	Количество "на странице"
+        :type rows_on_page: int or str
+
+
+        """
+        if isinstance(date_created_start, datetime):
+            date_created_start = f'{date_created_start:%Y-%m-%d}'
+        if isinstance(date_created_end, datetime):
+            date_created_end = f'{date_created_end:%Y-%m-%d}'
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Finance.GET_RECEIPTS, payload)
+
+    async def get_payments_methods(self, only_enabled: Union[bool, str] = None,
+                                   only_disabled: Union[bool, str] = None,
+                                   payment_method_id: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BD.D0.B0.D1.81.D1.82.D1.80.D0.BE.D0.B5.D0.BA_.D0.BF.D0.BB.D0.B0.D1.82.D1.91.D0.B6.D0.BD.D1.8B.D1.85_.D1.81.D0.B8.D1.81.D1.82.D0.B5.D0.BC
+        Возвращает настройки платёжных систем.
+        Если не указывать доп. параметры,
+        то будут возвращены все существующие настройки для всех платёжных систем (активных и отключенных).
+
+
+        :param only_enabled:если true, то будет возвращён список только включенных настроек ПС
+        :type only_enabled: bool or str
+        :param only_disabled: если true, то будет возвращён список только выключенных настроек ПС
+        :param payment_method_id: id конкретной платёжной системы для которой нужно получить настройки
+        :type payment_method_id: str or int
+        :return:dict
+        """
+        if all(x is not None for x in [only_enabled, only_disabled]):
+            raise AbcpAPIError('Укажите только один параметр должен быть указан only_enabled или only_disabled')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Finance.GET_PAYMENTS_SETTINGS, payload)
+
+
+class Users:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get_users(
+            self,
+            date_registred_start: Union[str, datetime] = None,
+            date_registred_end: Union[str, datetime] = None,
+            date_updated_start: Union[str, datetime] = None,
+            date_updated_end: Union[str, datetime] = None,
+            state: Union[str, int] = None,
+            customer_status: Union[str, int] = None,
+            customers_ids: Union[List, str, int] = None,
+            market_type: Union[str, int] = None,
+            phone: Union[str, int] = None,
+            enable_sms: Union[str, bool] = None,
+            email: str = None,
+            safe_mode: Union[str, int] = None,
+            format: str = None,
+            limit: Optional[int] = None,
+            skip: Optional[int] = None,
+            desc: Union[str, bool] = 'false'
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D0.B5.D0.B9
+        Принимает в качестве параметров условия фильтрации клиентов. Возвращает список клиентов.
+
+
+        :param date_registred_start: Начальная дата регистрации `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_registred_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param date_registred_end: Конечная дата регистрации `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_registred_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param date_updated_start: Начальная дата последнего обновления `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_updated_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param date_updated_end: Конечная дата последнего обновления `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_updated_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param state: Состояние клиента. Значения:-1 - отклоненный, 0 - ожидает регистрации, 1 - зарегистрированный,
+                       2 - удаленный.
+        :type state: int or str
+        :param customer_status: Идентификатор статуса покупателя, если указать 0 - будут выбраны пользователи без статуса
+        :type customer_status: int or str
+        :param customers_ids: Массив идентификаторов покупателей
+        :type customers_ids: List of str or int
+        :param market_type: Тип регистрации. Значения:  1 - Розница 2 - Опт
+        :type market_type: int or str
+        :param phone: Номер телефона клиента
+        :type phone: str 79998887766
+        :param enable_sms: Производится ли отпровка SMS клиенту
+        :param email: E-mail клиента
+        :type email: str
+        :param safe_mode: "Безопасный режим" для клиентов не имеющих поддержки формата JSON.
+                Может принимать значения 0 или 1. При включении (1), адреса доставки в ответе будут возвращаться в виде
+                массива объектов с полями "id" и "name", а не как "ключ - значение".
+        :type safe_mode: int or str
+        :param format: 	Формат ответа. Доступные значения: p - заказы содержатся в поле items,
+                        данные о количестве содержатся в поле count
+        :type format: str
+        :param limit: Количество возвращаемых записей заказов (число, по умолчанию - 1000).
+                      Чтобы получить информацию о количестве записей используйте параметр format со значением p
+        :type limit: int or str
+        :param skip: кол-во заказов, которые нужно пропустить. (число, по умолчанию - 0).
+        :type skip: int or str
+        :param desc: Обратное направление сортировки
+        :type desc: str or bool ('true', 'false', True, False)
+
+
+        """
+
+        if isinstance(date_registred_start, datetime):
+            date_registred_start = f'{date_registred_start:%Y-%m-%d %H:%M:%S}'
+        if isinstance(date_registred_end, datetime):
+            date_registred_end = f'{date_registred_end:%Y-%m-%d %H:%M:%S}'
+        if isinstance(date_updated_start, datetime):
+            date_updated_start = f'{date_updated_start:%Y-%m-%d %H:%M:%S}'
+        if isinstance(date_updated_end, datetime):
+            date_updated_end = f'{date_updated_end:%Y-%m-%d %H:%M:%S}'
+
+        if isinstance(format, str) and format != 'p':
+            raise AbcpWrongParameterError('The parameter "format" can only take the value "p" or None')
+        if not isinstance(customers_ids, list) and customers_ids is not None:
+            customers_ids = [customers_ids]
+        if isinstance(enable_sms, str) and (enable_sms != 'true' and enable_sms != 'false'):
+            raise AbcpAPIError('Параметр "enable_sms" должен быть булевым значением, либо строкой "true" или "false"')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Users.GET_USERS_LIST, payload)
+
+    async def create(
+            self,
+            market_type: Union[str, int],
+            name: str, password: str,
+            mobile: Union[str, int],
+            filial_id: Union[int, str] = None,
+            second_name: str = None, surname: str = None,
+            birth_date: Union[str, datetime] = None,
+            member_of_club: str = None, office: Union[str, int] = None,
+            email: str = None, icq: str = None, skype: str = None,
+            region_id: str = None, city: str = None,
+            organization_name: str = None, business: Union[str, int] = None,
+            organization_form: str = None, organization_official_name: str = None,
+            inn: Union[str, int] = None, kpp: Union[str, int] = None,
+            ogrn: Union[str, int] = None, organization_official_address: str = None,
+            bank_name: str = None, bik: Union[str, int] = None,
+            correspondent_account: Union[str, int] = None, organization_account: Union[str, int] = None,
+            delivery_address: str = None, comment: str = None, profile_id: str = None,
+            pickup_state: Union[int, bool] = None
+    ):
+        """Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.A1.D0.BE.D0.B7.D0.B4.D0.B0.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
+        Принимает параметры для регистрации пользователя. Осуществляет регистрацию нового пользователя в системе.
+        Возвращает статус выполнения операции регистрации, учетные данные нового пользователя, а так же сообщение об ошибке в случае возникновения таковой.
+
+        :param market_type: Тип регистрации: 1 - Розница, 2 - Опт
+        :type market_type: str or int
+        :param filial_id: Код филиала (если имеются)
+        :type filial_id: int or str
+        :param name: Имя :type name: str
+        :param password: Пароль :type password: str
+        :param second_name: Отчество :type second_name: str
+        :param surname: Фамилия :type surname: str
+        :param birth_date: Дата рождения :type birth_date: str datetime strftime("%Y-%m-%d")
+        :param mobile: Отчество :type mobile: str or int forman 79998887766
+        :param member_of_club: Название автоклуба :type member_of_club: str
+        :param office: Идентификатор офиса :type office: str or int
+        :param email: Отчество :type email: str
+        :param icq: icq :type icq: str
+        :param skype: Skype :type skype: str
+        :param region_id: Код региона :type region_id: str
+        :param city: Город :type city: str
+        :param name: Имя :type name: str
+        :param organization_name: Наименование организации :type organization_name: str
+        :param business: Тип организации. Значение от 1 до 3: 1 - Автосервис, 2 - Автомагазин, 3 - Собственный автопарк
+        :type business: str or int
+        :param organization_form: Правовая форма организации. Варианты: ООО, ОАО, ЗАО, ТОО, АО, ЧП, ПБОЮЛ
+        :type organization_form: str
+        :param organization_official_name: Наименование по регистрации (без правовой формы юр. лица)
+        :type organization_official_name: str
+        :param inn: ИНН :type inn: str
+        :param kpp: КПП :type kpp: str
+        :param ogrn: ОГРН :type ogrn: str
+        :param organization_official_address: Юридический адрес организации :type organization_official_address: str
+        :param bank_name: Наименование банка :type bank_name: str
+        :param bik: БИК банка :type bik: str or int
+        :param correspondent_account: Корреспондентский счет банка :type correspondent_account: str or int
+        :param organization_account: Расчетный счет организации :type organization_account: str or int
+        :param delivery_address: Адрес доставки :type delivery_address: str
+        :param comment: Комментарий :type comment: str
+        :param profile_id: Идентификатор профиля.
+        Если не указан, будет выставлен профиль по умолчанию для соответствующего типа регистрации (опт или розница).
+        :type profile_id: str
+        :param pickup_state: Запрет самовывоза для клиента. 0 - запретить самовывоз, 1- разрешить самовывоз. Параметр актуален только если у вас на сайте включена опция: "Корзина: запрет самовывоза определенным клиентам".
+        """
+
+        if isinstance(birth_date, datetime):
+            birth_date = f'{birth_date:%Y-%m-%d}'
+        if isinstance(pickup_state, bool):
+            pickup_state = int(pickup_state)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Users.CREATE_USER, payload, True)
+
+    async def get_profiles(
+            self,
+            profile_id: Union[int, str] = None,
+            skip: Optional[int] = None,
+            limit: Optional[int] = None,
+            format: str = None
+    ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D1.80.D0.BE.D1.84.D0.B8.D0.BB.D0.B5.D0.B9
+        Возвращает список всех профилей.
+
+
+        :param limit: Кол-во профилей в ответе. Необязательный параметр. Допустимые значения от 1 до 100. По умолчанию возвращаются все профили.
+        :param skip: Кол-во профилей, которые нужно пропустить. Необязательный параметр. По умолчанию: 0.
+        :param profile_id: Идентификатор профиля. Необязательный параметр. По умолчанию возвращаются все профили.
+        :param format: Формат ответа. Необязательное значение
+        Может принимать значения: "distributors" - выводить информацию по наценкам на поставщиков; "brands" - выводить информацию по наценкам на поставщиков и бренды
+        :type format: str 'distributors' or 'brands'
+        """
+        format_params_check = ('brands', 'distributors')
+        if isinstance(format, str) and format not in format_params_check:
+            raise AbcpWrongParameterError('format parameter can take values "brands" or "distributors"')
+        del format_params_check
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Users.GET_PROFILES, payload)
+
+    async def edit_profile(
+            self,
+            profile_id: Union[int, str],
+            code: Union[str, int] = None,
+            name: str = None,
+            comment: str = None,
+            price_up: Union[str, int] = None,
+            payment_methods: str = None,
+            matrix_price_ups: Union[List[Dict], Dict] = None,
+            distributors_price_ups: Union[List[Dict], Dict] = None,
+
+    ):
+
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D1.80.D0.BE.D1.84.D0.B8.D0.BB.D1.8F
+        Изменяет профиль. Принимает в качестве параметров идентификатор профиля на сайте и всю информацию о профиле,
+        возвращаемую операцией cp/users/profiles в формате brands.
+        Работает только при выключенной опции Профили: использовать групповое сохранение, иначе возвращает ошибку.
+        Если не указать идентификатор профиля, будет создан новый.
+        В данном случае, обязательными параметрами будут name и priceUp.
+        При создании профиля невозможно использовать имя и код существующих профилей.
+        Обязательно наличие как минимум одного из полей (code, name, comment, priceUp, paymentMethods, matrixPriceUps, distributorsPriceUps).
+
+
+        :param profile_id: Идентификатор профиля
+        :type profile_id: str or int
+        :param code: Код профиля
+        :type code: str or int
+        :param name: Наименование профиля
+        :type name: str
+        :param comment: Комментарий
+        :type comment: str
+        :param price_up: Наценка, %
+        :type price_up: str or int
+        :param payment_methods: 	Платежные системы
+        :type payment_methods: str or int
+        :param matrix_price_ups: Наценки от стоимости товара
+        :type matrix_price_ups: List of dicts
+        :param distributors_price_ups: Наценки по поставщикам
+        :type distributors_price_ups: str or int
+        """
+        if all(x is None for x in [code, name, comment,
+                                   price_up, payment_methods,
+                                   matrix_price_ups, distributors_price_ups]):
+            raise AbcpParameterRequired("Один из опциональных параметров должен быть передан")
+        if isinstance(matrix_price_ups, dict):
+            matrix_price_ups = [matrix_price_ups]
+        if isinstance(distributors_price_ups, dict):
+            distributors_price_ups = [distributors_price_ups]
+        payload = generate_payload(exclude=['matrix_price_ups', 'distributors_price_ups'], **locals())
+        return await self._base.request(_Methods.Admin.Users.EDIT_PROFILE, payload, True)
+
+    async def edit(
+            self,
+            user_id: Union[str, int], business: Union[str, int] = None,
+            email: str = None, name: str = None, second_name: str = None,
+            surname: str = None, password: str = None,
+            birth_date: Union[str, datetime] = None, city: str = None,
+            mobile: Union[str, int] = None, icq: str = None,
+            skype: str = None, enable_sms: Union[bool, str] = None, state: Union[str, int] = None,
+            profile_id: Union[int, str] = None, organization_name: str = None,
+            organization_form: str = None, organization_official_name: str = None,
+            inn: Union[str, int] = None, kpp: Union[str, int] = None, ogrn: Union[str, int] = None,
+            bank_name: str = None, bik: Union[str, int] = None,
+            correspondent_account: Union[str, int] = None, organization_account: Union[str, int] = None,
+            delivery_address: Union[List[Dict], Dict] = None, baskets: Union[List[Dict], Dict] = None,
+            baskets_delivery_address: Union[List[Dict], Dict] = None, comment: str = None,
+            manager_comment: str = None, manager_id: Union[int, str] = None,
+            user_code: Union[str, int] = None, client_service_employee_id: Union[int, str] = None,
+            client_service_employee2_id: Union[int, str] = None, client_service_employee3_id: Union[int, str] = None,
+            client_service_employee4_id: Union[int, str] = None, office: Union[List[Dict], Dict] = None,
+            info: str = None, safe_mode: Union[str, int] = None,
+            pickup_state: Union[int, bool] = None,
+
+    ):
+
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B4.D0.B0.D0.BD.D0.BD.D1.8B.D1.85_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
+        Осуществляет обновление данных пользователя, присланных в запросе.
+        При изменении данных пользователя необязательно передавать все параметры.
+        Используйте в запросе только те данные, которые вы собираетесь изменить.
+
+
+        :param ogrn: ОГРН
+        :param kpp: КПП
+        :param inn:ИНН
+        :param name: Имя
+        :param user_id: Идентификатор изменяемого клиента
+        :param business: Тип организации. Значение от 1 до 6:
+        :param email: Адрес электронной почты
+        :param second_name:	Отчество
+        :param surname: Фамилия
+        :param password: Необязательный параметр. Предназначен для изменения пароля пользователя
+        :param birth_date:Дата рождения `str` в формате %Y-%m-%d  или datetime object
+        :param city: Город
+        :param mobile: Номер мобильного телефона
+        :param icq:	ICQ UIN
+        :param skype: Skype
+        :param enable_sms: Производится ли отпровка SMS клиенту
+        :param state: Состояние аккаунта. Значения: от -1 до 2
+        :param profile_id: Идентификатор профиля
+        :param organization_name: Наименование организации
+        :param organization_form: Правовая форма организации.
+        :param organization_official_name: Наименование по регистрации (без правовой формы юр. лица)
+        :param bank_name: Наименование банка
+        :param bik: БИК банка
+        :param correspondent_account: Корреспондентский счет банка
+        :param organization_account: Расчетный счет организации
+        :param delivery_address: Адреса доставки (массив, где ключи - id адресов). Если передать пустой параметр deliveryAddress, то все адреса клиента будут удалены!
+        :param baskets: Корзины клиента (массив, где ключи - id корзин). Если передать пустой параметр baskets, то все корзины клиента будут удалены!
+        :param baskets_delivery_address: Связки корзины и адреса доставки(массив, где ключи - id корзин). Обновятся только переданные связки "корзина - Адрес доставки". Чтобы убрать привязку корзины и адреса нужно передать значение параметра = "0".
+        :param comment: Комментарий пользователя
+        :param manager_comment: Комментарий менеджера
+        :param manager_id: Идентификатор менеджера. Если передать managerId=0, то менеджер в карточке клиента удалится.
+        :param user_code: Внутренний код пользователя
+        :param client_service_employee_id: Идентификатор личного менеджера клиентской службы (дополнительная опция). Если передать clientServiceEmployeeId=0, то менеджер клиентской службы в карточке клиента удалится.
+        :param client_service_employee2_id: Идентификатор личного менеджера клиентской службы (дополнительная опция). Если передать clientServiceEmployeeId=0, то менеджер клиентской службы в карточке клиента удалится.
+        :param client_service_employee3_id: Идентификатор личного менеджера клиентской службы (дополнительная опция). Если передать clientServiceEmployeeId=0, то менеджер клиентской службы в карточке клиента удалится.
+        :param client_service_employee4_id: Идентификатор личного менеджера клиентской службы (дополнительная опция). Если передать clientServiceEmployeeId=0, то менеджер клиентской службы в карточке клиента удалится.
+        :param office: Массив идентификаторов офисов, к которым необходимо подключить клиента. Если идентификатор офиса, к одному из которых подключен клиент, не будет передан, то он будет отключен. Передать пустой параметр office нельзя, т.к. клиент должен быть подключен минимум к одному офису. Параметр актуален только если у вас на сайте включена опция: "Офисы: включить привязку к клиентам".
+        :param info: "Информация" в личном кабинете. В поле допустимо использование html-тегов. max 4000 символов. Закладка появляется только если есть данные в поле info для клиента.
+        :param safe_mode:
+        :param pickup_state: Запрет самовывоза для клиента. 0 - запретить самовывоз, 1- разрешить самовывоз. Параметр актуален только если у вас на сайте включена опция: "Корзина: запрет самовывоза определенным клиентам".
+        :return:
+        """
+        if isinstance(birth_date, datetime):
+            birth_date = f'{birth_date:%Y-%m-%d}'
+        if isinstance(pickup_state, bool):
+            pickup_state = int(pickup_state)
+        if isinstance(enable_sms, str) and (enable_sms != 'true' and enable_sms != 'false'):
+            raise AbcpAPIError('Параметр "enable_sms" должен быть булевым значением, либо строкой "true" или "false"')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Users.EDIT_USER, payload, True)
+
+    async def get_user_shipment_address(self, user_id: Union[int, str]):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B0.D0.B4.D1.80.D0.B5.D1.81.D0.BE.D0.B2_.D0.B4.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D0.BA.D0.B8
+
+        Возвращает список доступных адресов доставки. Идентификатор адреса доставки необходим при отправке заказа.
+
+        :param user_id: Идентификатор клиента
+        :type user_id: str or int
+        """
+
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Users.GET_USER_SHIPMENT_ADDRESS, payload)
+
+    async def get_shipment_address_zones(self):
+        """
+        Получение списка зон адресов доставки
+
+        :return: Возвращает список зон адресов доставки.
+        """
+        return await self._base.request(_Methods.Admin.Users.GET_USER_SHIPMENT_ADDRESS_ZONES)
+
+    async def get_shipment_address_zone(self, id: int):
+        """
+        Получение одной зоны адресов доставки
+
+        :param id: Уникальный идентификатор зоны адресов доставки
+        :return: Возвращает одну зону адресов доставки по указанному уникальному идентификатору.
+        """
+        return await self._base.request(_Methods.Admin.Users.GET_USER_SHIPMENT_ADDRESS_ZONE.format(id))
+
+    async def update_shipment_zones(self, zones: Union[List[Dict], Dict]):
+        """
+        Сохранение зон адресов доставки. Универсальный метод добавления и обновления зон адресов доставки.
+
+        :param zones: Массив объектов зон адресов доставки
+        :return:
+        """
+        if isinstance(zones, dict):
+            zones = [zones]
+
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Users.UPDATE_SHIPMENT_ZONES, payload, True)
+
+    async def create_shipment_zone(self, name: str, **kwargs):
+        """
+        Создание новой зоны адресов доставки. Метод создания одной зоны адресов доставки.
+
+        :param name: Название зоны
+        :param kwargs: Аргументы isOnDay{day}: int и stopTimeDay{day}: int
+        :return:
+        """
+        if kwargs is None:
+            raise AbcpParameterRequired('Необходимо передать аргументы "isOnDay{day:int}" и "stopTimeDay{day:int}"\n\n'
+                                        'Например: isOnDay1=1, stopTimeDay1="15:30"')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Users.CREATE_SHIPMENT_ZONE, payload, True, json=True)
+
+    async def update_shipment_zone(self, id: int, name: str, **kwargs):
+        """
+        Метод обновления данных одной зоны адресов доставки.
+
+        :param id: Идентификатор обновляемой зоны
+        :param name: Название зоны
+        :param kwargs: Аргументы isOnDay{day}: int и stopTimeDay{day}: int
+        :return:
+        """
+        if kwargs is None:
+            raise AbcpParameterRequired('Необходимо передать аргументы "isOnDay{day:int}" и "stopTimeDay{day:int}"\n\n'
+                                        'Например: isOnDay1=1, stopTimeDay1="15:30"')
+        _method = _Methods.Admin.Users.UPDATE_SHIPMENT_ZONE.format(id)
+        del id
+        payload = generate_payload(**locals())
+        return await self._base.request(_method, payload, True, json=True)
+
+    async def delete_shipment_zone(self, id: int):
+        return await self._base.request(_Methods.Admin.Users.DELETE_SHIPMENT_ZONE.format(id), None, True)
+
+    async def get_updated_cars(self, date_updated_start: str = None, date_updated_end: str = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.BE.D0.B2_.D0.BE.D1.84.D0.B8.D1.81.D0.B0
+        Возвращает информацию об автомобилях, в которые были внесены изменения за определённый период времени.
+        Если не переданы dateUpdatedStart и dateUpdatedEnd, то будет предоставлена информация за последний месяц.
+
+
+        :param date_updated_start: Начальная дата последнего обновления `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_updated_start: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :param date_updated_end: Конечная дата последнего обновления заказа `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :type date_updated_end: `str` в формате %Y-%m-%d %H:%M:%S  или datetime object
+        :return:dict
+        """
+        if isinstance(date_updated_start, datetime):
+            date_updated_start = f'{date_updated_start:%Y-%m-%d %H:%M:%S}'
+
+        if isinstance(date_updated_end, datetime):
+            date_updated_end = f'{date_updated_end:%Y-%m-%d %H:%M:%S}'
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Users.GET_USERS_CARS, payload)
+
+    async def get_sms_settings(self, user_ids: Union[List, int, str]):
+        if not isinstance(user_ids, list):
+            user_ids = [user_ids]
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Users.SMS_SETTINGS, payload)
+
+
+class Staff:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.81.D0.BE.D1.82.D1.80.D1.83.D0.B4.D0.BD.D0.B8.D0.BA.D0.BE.D0.B2
+        Возвращает список менеджеров.
+        """
+        return await self._base.request(_Methods.Admin.Staff.GET_STAFF)
+
+    async def update_manager(self, id: int, type_id: int = None,
+                             first_name: str = None, last_name: str = None,
+                             email: str = None, phone: str = None, mobile: str = None,
+                             sip: Union[str, int] = None, comment: str = None, boss_id: int = None, office_id: int = None):
+        """
+
+        Обновление данных сотрудника.
+
+        При изменении данных сотрудника необязательно передавать все параметры. Используйте в запросе только те данные, которые вы собираетесь изменить.
+
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B4.D0.B0.D0.BD.D0.BD.D1.8B.D1.85_.D1.81.D0.BE.D1.82.D1.80.D1.83.D0.B4.D0.BD.D0.B8.D0.BA.D0.B0
+
+        :param id: Идентификатор сотрудника (обязательное поле)
+        :param type_id: Идентификатор должности сотрудника
+        :param first_name: Имя сотрудника
+        :param last_name: Фамилия сотрудника
+        :param email: Адрес ящика электронной почты
+        :param phone: Номер телефона
+        :param mobile: Номер мобильного телефона
+        :param sip: SIP номер
+        :param comment: Комментарий
+        :param boss_id: Идентификатор руководителя
+        :param office_id: Идентификатор офиса
+        :return:
+        """
+        if isinstance(sip, str) and not sip.isdigit():
+            raise AbcpWrongParameterError('Параметр "SIP" должен быть числом')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Staff.UPDATE_STAFF, payload, True)
+
+
+class Statuses:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.BE.D0.B2
+        Возвращает список всех статусов позиций заказов.
+        """
+        return await self._base.request(_Methods.Admin.Statuses.GET_STATUSES)
+
+
+class Articles:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get_brands(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D1.80.D0.B0.D0.B2.D0.BE.D1.87.D0.BD.D0.B8.D0.BA.D0.B0_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D0.BE.D0.B2
+        Возвращает список всех брендов зарегистрированных в системе с их синонимами.
+        """
+        return await self._base.request(_Methods.Admin.Articles.GET_BRANDS)
+
+    async def get_brand_group(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D1.80.D0.B0.D0.B2.D0.BE.D1.87.D0.BD.D0.B8.D0.BA.D0.B0_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D0.BE.D0.B2
+
+        Возвращает список всех групп брендов зарегистрированных в системе.
+        """
+        return await self._base.request(_Methods.Admin.Articles.GET_BRANDS_GROUP)
+
+
+class Distributors:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get(self, distributors4mc: Union[str, int, bool] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.BE.D0.B2
+        Возвращает список всех поставщиков, подключенных в ПУ/Поставщики.
+
+
+        :param distributors4mc: При передаче "1" возвращает дополнительно поставщиков 4mycar"
+        :type distributors4mc: str or int
+        """
+        if isinstance(distributors4mc, bool):
+            distributors4mc = int(distributors4mc)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Distributors.GET_DISTRIBUTORS_LIST, payload)
+
+    async def edit_status(self, distributor_id: Union[int, str], status: Union[int, bool]):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.98.D0.B7.D0.BC.D0.B5.D0.BD.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
+        Изменение статуса поставщика
+
+
+        :param distributor_id: 	Id поставщика
+        :type distributor_id: str or int
+        :param status: 	1 - Вкл. / 0 - Выкл.
+        :type status: str or int
+        """
+        if isinstance(status, bool):
+            status = int(status)
+
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Distributors.EDIT_DISTRIBUTORS_STATUS, payload, True)
+
+    async def get_routes(self, distributor_id: Union[str, int]):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BC.D0.B0.D1.80.D1.88.D1.80.D1.83.D1.82.D0.BE.D0.B2_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
+        Возвращает список всех маршрутов поставщика.
+
+
+        :param distributor_id: 	Идентификатор поставщика
+        :type distributor_id: str or int
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Distributors.GET_SUPPLIER_ROUTES, payload)
+
+    async def edit_route(self,
+                         route_id: Union[str, int],
+                         deadline: Union[str, int] = None, deadline_replace: str = None,
+                         is_deadline_replace_franch_enabled: Union[str, bool] = None,
+                         deadline_max: Union[str, int] = None,
+                         normal_time_start: str = None, normal_time_end: str = None,
+                         normal_days_of_week: List = None,
+                         abnormal_deadline: Union[str, int] = None,
+                         abnormal_deadline_max: Union[str, int] = None,
+                         p1: Union[str, int] = None, p2: Union[str, int] = None,
+                         price_per_kg: Union[str, int] = None,
+                         price_up_added: Union[str, int] = None,
+                         c1: Union[str, int] = None,
+                         price_up_min: Union[str, int] = None, price_up_max: Union[str, int] = None,
+                         primary_price_up_to_contractor: Union[str, int] = None,
+                         delivery_probability: Union[str, int] = None,
+                         description: str = None,
+                         enable_color: Union[str, bool] = None, color: str = None,
+                         is_abnormal_color_enabled: Union[str, bool] = None, abnormal_color: str = None,
+                         no_return: Union[bool, str] = None,
+                         supplier_code_enabled_list: Union[List, List, str, int] = None,
+                         supplier_code_disabled_list: Union[List, List, str, int] = None,
+                         normal_time_display_only: Union[int, str] = None,
+                         disable_order_abnormal_time: Union[int, str] = None,
+                         not_use_online_supplier_deadline: Union[int, str] = None,
+                         ):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B4.D0.B0.D0.BD.D0.BD.D1.8B.D1.85_.D0.BC.D0.B0.D1.80.D1.88.D1.80.D1.83.D1.82.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
+        Осуществляет обновление данных маршрута поставщика, присланных в запросе.
+        При изменении данных маршрута необязательно передавать все параметры.
+        Используйте в запросе только те данные, которые вы собираетесь изменить.
+
+
+
+        :param route_id: Идентификатор маршрута поставщика
+        :type route_id: int or str
+        :param deadline: Срок поставки (часов)
+        :type deadline: int or str
+        :param deadline_replace: Текстовое значение для "Срока поставки"
+        :type deadline_replace: str
+        :param is_deadline_replace_franch_enabled: Передавать текстовое значение для "Срока поставки" франчайзи
+        :type is_deadline_replace_franch_enabled: bool or str
+        :param deadline_max: Максимальный срок поставки (часов)
+        :type deadline_max: int or str
+        :param normal_time_start:Начало рабочего времени (09:00)
+        :type normal_time_start: str
+        :param normal_time_end:Конец рабочего времени (09:00)
+        :type normal_time_end: str
+        :param normal_days_of_week:Стандартные дни недели ['Вт', 'Ср']
+        :type normal_days_of_week: list
+        :param abnormal_deadline:Срок поставки (вне стандартного времени)
+        :param abnormal_deadline_max:	Максимальный срок поставки (вне стандартного времени)
+        :param p1: Первичная наценка 10
+        :type p1: str or int
+        :param p2: Вторичная наценка
+        :type p2: str or int
+        :param price_per_kg: Стоимость 1КГ (в валюте поставщика) 200
+        :type price_per_kg: str or int
+        :param price_up_added:Добавочная наценка 3
+        :type price_up_added: str or int
+        :param c1: Коэффициент наценки 0 - 100
+        :type c1: str or int
+        :param price_up_min:Минимальная наценка
+        :type price_up_min:int or str
+        :param price_up_max:Максимальная наценка
+        :type price_up_max:int or str
+        :param primary_price_up_to_contractor:Приоритетная (если выше) наценка для клиента
+        :type primary_price_up_to_contractor: int or str
+        :param delivery_probability:Вероятность поставки (в процентах) %
+        :type delivery_probability: int or str
+        :param description:Краткое описание маршрута
+        :type description: str
+        :param enable_color:Выделять цветом 'false' or False
+        :type enable_color: bool or str
+        :param color: Цвет в HEX
+        :type color: str
+        :param is_abnormal_color_enabled: 	Выделять цветом в нерабочее время 'false' or False
+        :type is_abnormal_color_enabled: bool or str
+        :param abnormal_color:Цвет в HEX
+        :type abnormal_color: str
+        :param no_return:Без возврата 'false' or False
+        :type no_return: bool or str
+        :param supplier_code_enabled_list: Ограничить выдачу складами (массив)
+        :type supplier_code_enabled_list list or str
+        :param supplier_code_disabled_list: Исключить позиции по складам (массив)
+        :type supplier_code_disabled_list list or str
+        :param normal_time_display_only:Показывать только в стандартное время (0 - Нет, 1 - Да)
+        :type normal_time_display_only: int or str
+        :param disable_order_abnormal_time:Блокировать отправку заказа в нестандартное время (0 - Нет, 1 - Да). "1" сохраняется только при normalTimeDisplayOnly=1.
+        :type disable_order_abnormal_time: int or str
+        :param not_use_online_supplier_deadline: Не использовать срок поставки online-поставщика (0 - Нет, 1 - Да)
+        :type not_use_online_supplier_deadline: int or str
+        :return: dict
+        """
+        if supplier_code_enabled_list is not None and not isinstance(supplier_code_enabled_list, list):
+            supplier_code_enabled_list = [supplier_code_enabled_list]
+        if supplier_code_disabled_list is not None and isinstance(supplier_code_disabled_list, list):
+            supplier_code_disabled_list = [supplier_code_disabled_list]
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Admin.Distributors.UPDATE_ROUTE, payload, True)
+
+    async def edit_route_status(self, route_id: Union[str, int], status: Union[int, bool]):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.98.D0.B7.D0.BC.D0.B5.D0.BD.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.B0_.D0.BC.D0.B0.D1.80.D1.88.D1.80.D1.83.D1.82.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
+
+        Изменяет статус маршрута поставщика
+
+
+        :param route_id:	Идентификатор маршрута поставщика
+        :type route_id: int or str
+        :param status:  Значение нового статуса (1-вкл., 0-выкл.)
+        :type route_id: int or str
+        :return: dict
+        """
+        if isinstance(status, bool):
+            status = int(status)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Distributors.UPDATE_ROUTE_STATUS, payload, True)
+
+    async def delete_route(self, route_id: Union[int, str]):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.A3.D0.B4.D0.B0.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BC.D0.B0.D1.80.D1.88.D1.80.D1.83.D1.82.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
+        Удаляет маршрут поставщика.
+
+
+        :param route_id:Идентификатор маршрута поставщика
+        :type route_id: int or str
+        :return: dict
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Distributors.DELETE_ROUTE, payload, True)
+
+    async def connect_to_office(self, office_id: Union[str, int],
+                                distributors: Union[List[Dict], Dict] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.B4.D0.BA.D0.BB.D1.8E.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.BE.D0.B2_.D0.BA_.D0.BE.D1.84.D0.B8.D1.81.D1.83
+
+        Подключение/отключение поставщиков к офисам
+        Если параметр distributors не указан или содержит пустой список все поставщики офиса будут отключены
+
+
+        :param office_id: Идентификатор офиса.
+        :type office_id: int or str
+        :param distributors: Массив поставщиков, если параметр не передан или содержит пустое значение - отключаются все поставщики указанного офиса.
+        :type distributors List[Dict] or Dict
+        :return: dict
+        """
+        if isinstance(distributors, dict):
+            distributors = [distributors]
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Distributors.EDIT_SUPPLIER_STATUS_FOR_OFFICE, payload, True)
+
+    async def get_office_distributors(self, office_id: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.BE.D0.B2_.D0.BE.D1.84.D0.B8.D1.81.D0.B0
+        Возвращает информацию о подключенных к офису поставщиках
+
+
+        :param office_id: Идентификатор офиса. Если параметр не указан то в ответе возвращаются данные по всем офисам
+        :type office_id: str or int
+        :return:dict
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Distributors.GET_OFFICE_SUPPLIERS, payload)
+
+    async def pricelist_update(self, distributor_id: Union[str, int],
+                               upload_file: Union[str, BufferedReader],
+                               file_type_id: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Admin#.D0.97.D0.B0.D0.B3.D1.80.D1.83.D0.B7.D0.BA.D0.B0_.D0.BF.D1.80.D0.B0.D0.B9.D1.81-.D0.BB.D0.B8.D1.81.D1.82.D0.B0_.D0.BF.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D1.89.D0.B8.D0.BA.D0.B0
+        В ПУ, в разделе "Поставщики"/"Обн."/"Конфигурация прайс-листа" предварительно настраивается конфигурация
+        загружаемого прайс-листа. Специальных требований к прайс-листу нет, есть только обычные: наличие колонок
+        с ценой, брендом, каталожным номером, описанием, наличием. На вкладке "Загрузка прайс-листа" может быть
+        выбран любой способ загрузки
+
+
+        :param distributor_id: Id поставщика
+        :type distributor_id: :obj:`Union[str, int]`
+        :param upload_file: путь до файла прайс-листа
+        :type upload_file: :obj:`str` or :obj:`BufferedReader`
+        :param file_type_id: Смысла от параметра пока нет (15.05.2022)
+
+        :return: dict
+        """
+
+        payload = generate_file_payload(exclude=['upload_file'], **locals())
+        return await self._base.request(_Methods.Admin.Distributors.UPLOAD_PRICE, payload, True)
+
+
+class Catalog:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def info(self, goods_group: str, locale: str = 'ru_RU'):
+        """
+
+        :param goods_group:
+        :param locale:
+        :return:
+        """
+        payload = generate_payload(exclude=['goods_group'], **locals())
+        return await self._base.request(_Methods.Admin.Catalog.INFO, payload)
+
+    async def search(self, goods_group: str,
+                     properties: Union[List[Dict[str, str]], Dict[str, str]],
+                     skip: Optional[int] = None, limit: Optional[int] = None,
+                     locale: Optional[str] = None):
+        """
+
+        :param goods_group:
+        :param properties:
+        :param skip:
+        :param limit:
+        :param locale:
+        :return:
+        """
+        if isinstance(properties, dict):
+            properties = [properties]
+        payload = generate_payload(exclude=['goods_group', 'properties'], **locals())
+        return await self._base.request(_Methods.Admin.Catalog.SEARCH, payload, True)
+
+    async def info_batch(self, articles_catalog: Union[List[Dict[str, str]], Dict[str, str]], locale: str = 'ru_RU'):
+        if isinstance(articles_catalog, dict):
+            articles_catalog = [articles_catalog]
+        payload = generate_payload(exclude=['articles_catalog'], **locals())
+        return await self._base.request(_Methods.Admin.Catalog.INFO_BATCH, payload, True)
+
+
+class UsersCatalog:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def upload(self, catalog_id: Union[str, int],
+                     file: Union[str, BufferedReader],
+                     delete_old_mode: int = 0,
+                     default_attributes_hide: Union[str, bool] = 'false',
+                     article_only: Union[str, bool] = 'false',
+                     image_upload_mode: int = 0,
+                     image_archive: Union[str, BufferedReader] = None):
+        """
+
+        :param catalog_id:
+        :param file:
+        :param delete_old_mode:
+        :param default_attributes_hide:
+        :param article_only:
+        :param image_upload_mode:
+        :param image_archive:
+        :return:
+        """
+        if not 0 <= delete_old_mode <= 2:
+            raise AbcpWrongParameterError('Параметр "delete_old_mode" должен быть в диапазоне от 0 до 2')
+
+        if isinstance(default_attributes_hide, bool):
+            default_attributes_hide = str(default_attributes_hide).lower()
+
+        if isinstance(article_only, bool):
+            article_only = str(article_only).lower()
+
+        if image_upload_mode == 1 and image_archive is None:
+            raise AbcpWrongParameterError('Не передан архив с изображениями')
+
+        payload = generate_file_payload(exclude=['file', 'image_archive', 'catalog_id'], max_size=100, **locals())
+        return await self._base.request(_Methods.Admin.UsersCatalog.UPLOAD.format(catalog_id), payload, True)
+
+
+class Payment:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def token(self, number: Union[str, int]):
+        """
+        Получение ссылки на оплату заказа
+
+        :param number: Онлайн-номер заказа
+        :return:
+        """
+        if isinstance(number, str) and not number.isdigit():
+            raise AbcpWrongParameterError('Параметр "number" должен быть числом')
+
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Payment.TOKEN, payload)
+
+    async def top_balance_link(self, client_id: Union[str, int], amount: Union[float, int, str]):
+        """
+
+        :param client_id: Идентификатор клиента
+        :param amount: Сумма пополнения баланса
+        :return:
+        """
+        if isinstance(client_id, str) and not client_id.isdigit():
+            raise AbcpWrongParameterError('Параметр "client_id" должен быть числом')
+        if isinstance(amount, str) and not amount.isdigit():
+            raise AbcpWrongParameterError('Параметр "amount" должен быть числом')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Admin.Payment.TOP_BALANCE, payload)
```

### Comparing `aioabcpapi-2.0.6/aioabcpapi/cp/client.py` & `aioabcpapi-2.0.7/aioabcpapi/cp/client.py`

 * *Ordering differences only*

 * *Files 24% similar despite different names*

```diff
@@ -1,899 +1,899 @@
-import logging
-from typing import Dict, List, Union, Optional
-
-from ..api import _Methods
-from ..base import BaseAbcp
-from ..exceptions import NotEnoughRights, AbcpAPIError, AbcpParameterRequired, AbcpWrongParameterError
-from ..utils.payload import generate_payload
-
-logger = logging.getLogger('Cp.Client')
-
-
-class ClientApi:
-    def __init__(self, base: BaseAbcp):
-        """
-        Класс содержит методы клиентского интерфейса
-
-        https://www.abcp.ru/wiki/API.ABCP.Client
-        """
-        self._base = base
-        self.search = Search(base)
-        self.basket = Basket(base)
-        self.orders = Orders(base)
-        self.user = User(base)
-        self.garage = Garage(base)
-        self.car_tree = CarTree(base)
-        self.form = Form(base)
-        self.articles = Articles(base)
-
-
-class Search:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def brands(self, number: Union[str, int],
-                     use_online_stocks: Union[bool, int] = 0,
-                     locale: Optional[str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.B8.D1.81.D0.BA_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D0.BE.D0.B2_.D0.BF.D0.BE_.D0.BD.D0.BE.D0.BC.D0.B5.D1.80.D1.83
-        Осуществляет поиск по номеру детали и возвращает массив найденных брендов, имеющих деталь с искомым номером.
-        Аналог этапа выбора бренда на сайте.
-        :param number: Искомый номер детали
-        :type number: str or int
-        :param use_online_stocks: Флаг "использовать online-склады". Может принимать значения 0 или 1
-        :type use_online_stocks: str or int
-        :param locale: Локаль. Задается в формате language[_territory], например, ru_RU. По умолчанию используется локаль сайта.
-        :type locale: str
-        :return:
-        """
-        if isinstance(use_online_stocks, bool):
-            use_online_stocks = int(use_online_stocks)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Search.BRANDS, payload)
-
-    async def articles(self,
-                       number: Union[str, int],
-                       brand: Union[str, int],
-                       use_online_stocks: Union[bool, int] = 0,
-                       disable_online_filtering: Union[bool, int] = 0,
-                       with_out_analogs: Union[bool, int] = 1,
-                       profile_id: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.B8.D1.81.D0.BA_.D0.B4.D0.B5.D1.82.D0.B0.D0.BB.D0.B8_.D0.BF.D0.BE_.D0.BD.D0.BE.D0.BC.D0.B5.D1.80.D1.83_.D0.B8_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D1.83
-        Осуществляет поиск по номеру детали и бренду. Возвращает массив найденных деталей.
-        Так как один и тот же производитель может иметь несколько общепринятых наименований (например, GM и General Motors),
-        система постарается это учесть, используя собственную базу синонимов брендов.
-
-        :param number: Искомый номер детали
-        :type number: :obj:`str or int`
-        :param brand: Фильтр по имени производителя
-        :type brand: str or int
-        :param use_online_stocks: Флаг "использовать online-склады". Может принимать значения 0 или 1 (по умолчанию - 0)
-        :type use_online_stocks: str or int
-        :param disable_online_filtering: Флаг "отключить фильтры online поставщиков". Может принимать значения 0 или 1 (по умолчанию - 0)
-        :type disable_online_filtering: str or int
-        :param with_out_analogs: Флаг "исключить поиск по аналогам". По умолчанию - 0.
-        :type with_out_analogs: str or int
-        :param profile_id: При передаче этого параметра, поисковая выдача api-администратора формируется как для клиента с переданным профилем. Работает только под API-администратором.
-        :type profile_id: str or int
-        :return:
-        """
-        if not self._base.admin and profile_id is not None:
-            raise NotEnoughRights('Только API Администор может указывать Профиль пользователя')
-        if isinstance(use_online_stocks, bool):
-            use_online_stocks = int(use_online_stocks)
-        if isinstance(disable_online_filtering, bool):
-            disable_online_filtering = int(disable_online_filtering)
-        if isinstance(with_out_analogs, bool):
-            with_out_analogs = int(with_out_analogs)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Search.ARTICLES, payload)
-
-    async def batch(self, search: Union[List[Dict], Dict], profile_id: Union[int, str] = None):
-        """
-        Source https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.B0.D0.BA.D0.B5.D1.82.D0.BD.D1.8B.D0.B9_.D0.B7.D0.B0.D0.BF.D1.80.D0.BE.D1.81_.D0.B1.D0.B5.D0.B7_.D1.83.D1.87.D0.B5.D1.82.D0.B0_.D0.B0.D0.BD.D0.B0.D0.BB.D0.BE.D0.B3.D0.BE.D0.B2
-        Осуществляет поиск по номеру производителя и бренду детали. Возвращает массив найденных деталей.
-        Внимание! Данная операция не выполняет поиск по online-складам.
-
-
-        :param search: Набор искомых деталей в формате brand - number. Максимум 100 деталей.
-        :type search: dict or list of dicts ({'brand': 'LuK','number': '602000600'})
-        :param profile_id: При передаче этого параметра, поисковая выдача api-администратора формируется как для клиента с переданным профилем. Работает только под API-администратором.
-        :type profile_id: str or int
-        :return:
-        """
-        if not self._base.admin and profile_id is not None:
-            raise NotEnoughRights('Только API Администор может указывать Профиль пользователя')
-        if isinstance(search, dict):
-            search = [search]
-        payload = generate_payload(exclude=['search'], **locals())
-        # It can work with GET and POST, but the documentation specifies POST
-        return await self._base.request(_Methods.Client.Search.BATCH, payload, True)
-
-    async def history(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.98.D1.81.D1.82.D0.BE.D1.80.D0.B8.D1.8F_.D0.BF.D0.BE.D0.B8.D1.81.D0.BA.D0.B0
-        Возвращает массив последних (не более 50) поисковых запросов текущего пользователя.
-
-
-        :return: dict
-        """
-        return await self._base.request(_Methods.Client.Search.HISTORY)
-
-    async def tips(self, number: Union[str, int], locale: Optional[str]):
-        """Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.B4.D1.81.D0.BA.D0.B0.D0.B7.D0.BA.D0.B8_.D0.BF.D0.BE_.D0.BF.D0.BE.D0.B8.D1.81.D0.BA.D1.83
-        Возвращает по части номера массив подходящих пар бренд - номер
-
-
-        :param number:Номер (часть номера) детали
-        :type number: :obj:`str` or `int`
-        :param locale: Локаль. Задается в формате language[_territory], например, ru_RU. По умолчанию используется локаль сайта.
-        :type locale: :obj:`str
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Search.TIPS, payload)
-
-    async def advices(self, brand: Union[str, int], number: Union[str, int], limit: Optional[int] = 5):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.B8.D1.81.D0.BA_.D1.81.D0.BE.D0.BF.D1.83.D1.82.D1.81.D1.82.D0.B2.D1.83.D1.8E.D1.89.D0.B8.D1.85_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.BE.D0.B2
-        Функция реализует механизм "с этим товаром покупают" на основе статистики покупки комплектов товаров.
-        Типичный пример использования функции: покупатель выбрал масляный фильтр - система рекомендует остальные товары из набора для ТО.
-        Или, покупатель выбрал левый передний амортизатор, система покажет правый передний.
-        Осуществляет поиск сопутствующих товаров по запрашиваемой паре "Бренд-номер".
-        Дополнительно можно передать параметр limit (рекомендуется = 5), ограничивающий выдачу рекомендаций.
-
-
-        :param brand: Имя производителя
-        :type brand: :obj:`Union[str, int]`
-        :param number: Номер детали
-        :type number: :obj:`Union[str, int]`
-        :param limit: необязательный параметр, ограничивающий выдачу
-        :type limit :obj:`int`
-        :return:
-        """
-
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Search.ADVICES, payload)
-
-    async def advices_batch(self, articles: Union[List[Dict], Dict], limit: Optional[int] = 5):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9C.D0.B5.D1.85.D0.B0.D0.BD.D0.B8.D0.B7.D0.BC_.22.D0.A1_.D1.8D.D1.82.D0.B8.D0.BC_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.BE.D0.BC_.D0.BF.D0.BE.D0.BA.D1.83.D0.BF.D0.B0.D1.8E.D1.82.22
-        Функция реализует механизм "с этим товаром покупают" по нескольким товарам.
-        Дополнительно можно передать параметр limit (рекомендуется = 5), ограничивающий выдачу рекомендаций.
-        Параметры товаров передаются в виде JSON-массива articles из объектов с полями 'brand' и 'number'.
-
-
-        :param articles:
-        :param limit:
-        :return:
-        """
-        if isinstance(articles, dict):
-            articles = [articles]
-        payload = generate_payload(exclude=['articles'], **locals())
-        return await self._base.request(_Methods.Client.Search.ADVICES_BATCH, payload, True, json=True)
-
-
-class Basket:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get_baskets_list(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD
-        Получение списка корзин
-
-
-        :return: dict
-        """
-        return await self._base.request(_Methods.Client.Basket.BASKETS_LIST)
-
-    async def add(self, basket_positions: Union[List[Dict], Dict], basket_id: Union[int, str] = None):
-        """
-        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.BE.D0.B2_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.83._.D0.A3.D0.B4.D0.B0.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.B0_.D0.B8.D0.B7_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.8B
-
-        Осуществляет подготовку к отправке заказа на товары по номеру производителя, бренду и коду поставки или по коду детали.
-        Возвращает статус добавления товара в корзину по каждой позиции.
-        При добавлении brand - number - itemKey - supplierCode позиции,
-        которая уже была ранее добавлена в корзину, значение quantity будет прибавлено к существующему.
-        Удаление позиции - при добавлении brand - number - itemKey - supplierCode позиции,
-        которая уже была ранее добавлена в корзину, со значением quantity равным 0, позиция будет удалена из корзины.
-        Для изменения количества рекомендуется удалять позицию и ее добавлять заново с требуемым количеством.
-
-
-
-        :param basket_positions: Набор добавляемых деталей в формате brand - number - itemKey - supplierCode или code с указанием добавляемого количества в поле quantity и комментария к позиции в поле comment
-        :type basket_positions: :obj:`list` or :obj:`dict
-        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
-        :type basket_id: :obj:`str` or :obj:`int`
-        :return: dict
-        """
-        if isinstance(basket_positions, dict):
-            basket_positions = [basket_positions]
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Client.Basket.BASKET_ADD, payload, True)
-
-    async def clear(self, basket_id: Union[int, str] = None):
-        """
-        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9E.D1.87.D0.B8.D1.81.D1.82.D0.BA.D0.B0_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.8B
-
-        Удаляет все позиции из корзины.
-
-
-        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
-        :type basket_id: :obj:`Union[str, int]`
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Basket.BASKET_CLEAR, payload, True)
-
-    async def content(self, basket_id: Union[int, str] = None):
-
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.BE.D0.B2_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D0.B5
-
-        Получение списка товаров в корзине
-        Возвращает список позиций, находящихся в корзине.
-        Внимание! Если у вас подключена опция "Корзина: разрешать частичное оформление заказа".
-        То в ответ веб-сервиса будут попадать только отмеченные позиции.
-
-
-        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
-        :type basket_id: :obj:`Union[str, int]`
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Basket.BASKET_CONTENT, payload)
-
-    async def options(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BE.D0.BF.D1.86.D0.B8.D0.B9_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.8B
-
-        Получение опций корзины
-        Возвращает значение некоторых опций Корзины.
-
-        :return:
-        """
-        return await self._base.request(_Methods.Client.Basket.BASKET_OPTIONS)
-
-    async def payment_method(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.81.D0.BF.D0.BE.D1.81.D0.BE.D0.B1.D0.BE.D0.B2_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82.D1.8B
-
-        Получение списка способов оплаты
-        Возвращает список доступных способов оплаты.
-        Идентификатор способа оплаты необходим при отправке заказа (при включенной опции "Корзина: показывать тип оплаты").
-        :return:
-        """
-        return await self._base.request(_Methods.Client.Basket.PAYMENT_METHODS)
-
-    async def shipment_method(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.81.D0.BF.D0.BE.D1.81.D0.BE.D0.B1.D0.BE.D0.B2_.D0.B4.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D0.BA.D0.B8
-
-        Получение списка способов доставки
-
-        :return:
-        """
-        return await self._base.request(_Methods.Client.Basket.SHIPMENT_METHOD)
-
-    async def shipment_offices(self, offices_type: Optional[str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BE.D1.84.D0.B8.D1.81.D0.BE.D0.B2_.D1.81.D0.B0.D0.BC.D0.BE.D0.B2.D1.8B.D0.B2.D0.BE.D0.B7.D0.B0
-
-        Получение списка офисов самовывоза
-        Возвращает список доступных офисов для самовывоза.
-        Идентификатор офиса самовывоза при отправке заказа
-        (при включенной опции "Заказы: показывать офисы при выборе самовывоза").
-
-
-        :param offices_type: Не обязательный параметр:
-                            order - (используется по-умолчанию) возвращает офисы используемые для оформления заказа
-                            registration - возвращает офисы используемые для регистрации пользователя при включенной опции "Офисы: включить привязку к клиентам"
-        :return:
-        """
-        if isinstance(offices_type, str) and (offices_type != 'order' or offices_type != 'registration'):
-            raise AbcpParameterRequired("offices_type может принимать значения 'order' или 'registration'")
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Basket.SHIPMENT_OFFICES, payload)
-
-    async def shipment_address(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B0.D0.B4.D1.80.D0.B5.D1.81.D0.BE.D0.B2_.D0.B4.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D0.BA.D0.B8
-
-        Получение списка адресов доставки
-        Возвращает список доступных адресов доставки. Идентификатор адреса доставки необходим при отправке заказа.
-
-        :return:
-        """
-        return await self._base.request(_Methods.Client.Basket.SHIPMENT_ADDRESS)
-
-    async def shipment_dates(self, min_deadline_time: int, max_deadline_time: int,
-                             shipment_address: Union[str, int] = None):
-        """
-        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B4.D0.B0.D1.82_.D0.BE.D1.82.D0.B3.D1.80.D1.83.D0.B7.D0.BA.D0.B8
-
-        Получение списка дат отгрузки
-
-        Возвращает список доступных дат отгрузки.
-        Дата отгрузки необходима при отправке заказа при включенной опции "Корзина: показывать дату отгрузки".
-
-
-        :param min_deadline_time: Минимальный срок поставки, в часах, среди всех позиций, которые вы собрались отправлять в заказ.
-        :param max_deadline_time: Максимальный срок поставки, в часах, среди всех позиций, которые вы собрались отправлять в заказ.
-        :param shipment_address: id адреса доставки. Необязательный параметр.
-        Необходимо отправлять, если заказ будет оформлен с доставкой.
-        Для подготовки доставки офисам может требоваться дополнительное время на сборку.
-        При отправке параметра shipmentAddress получаем актуальные даты отгрузки с учетом времени комплектации в настройках офиса.
-
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Basket.SHIPMENT_DATES)
-
-    async def add_shipment_address(self, address: str):
-        """
-        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B0.D0.B4.D1.80.D0.B5.D1.81.D0.B0_.D0.B4.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D0.BA.D0.B8
-        Добавление адреса доставки
-        Для текущего покупателя добавляет "адрес доставки" и возвращает его идентификатор используемый в методе Отправка корзины в заказ
-
-
-        :param address: Обязательный, строка содержащая адрес.
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Basket.SHIPMENT_DATES, payload, True)
-
-    async def set_client_params(self,
-                                payment_method_index: int,
-                                shipment_address_index: int,
-                                shipment_method_index: int = None,
-                                shipment_office_index: int = None):
-        """
-        Устанавливает параметры для метода order.
-        Если все индексы переданы верно в методы api.cp.client.order.order_by_basket и api.cp.client.order.order_instant не требуется передавать аргументы:
-        'payment_method', 'shipment_address', 'shipment_method', 'shipment_office'.
-
-        :param payment_method_index: Обязательный параметр для любого типа отгрузки. Индекс типа оплаты полученный методом payment_method
-        :type payment_method_index: int
-        :param shipment_address_index: Обязательный параметр для любого типа отгрузки. Индекс адреса доставки полученный методом shipment_address
-        :type shipment_address_index: int
-        :param shipment_method_index: Не обязательный параметр, если используется самовывоз. Индекс типа доставки полученный методом payment_method
-        :type shipment_method_index: int
-        :param shipment_office_index: Не обязательный параметр, если используется доставка. Индекс офиса самовывоза полученый методом shipment_offices
-        :type shipment_office_index: int
-        :return:
-        """
-        try:
-            if shipment_address_index != 0 and shipment_office_index is not None:
-                raise AbcpParameterRequired('Для выбора самовывоза необходимо передать "shipment_address_index=0"')
-            payment_method = await self.payment_method()  # 0
-            self._base.payment_method = payment_method[payment_method_index]['id']
-            logger.info(
-                f'Выбран тип оплаты:\nID - {payment_method[payment_method_index]["id"]}\n'
-                f'Name - {payment_method[payment_method_index]["name"]}')
-            if shipment_method_index is not None and shipment_address_index is not None:
-                shipment_address = await self.shipment_address()  # 1
-                self._base.shipment_address = shipment_address[shipment_address_index]["id"]
-                logger.info(f'\n\n\n{shipment_address}\n\n\n\n')
-                logger.info(f'Выбран адрес доставки:\nID - {shipment_address[shipment_address_index]["id"]}\n'
-                            f'Name - {shipment_address[shipment_address_index]["name"]}')
-
-            if shipment_office_index is not None and shipment_method_index is None:
-                shipment_office = await self.shipment_offices()
-                self._base.shipment_office = shipment_office[shipment_office_index]["id"]
-                logger.info(f'Выбран офис самовывоза:\nID - {shipment_office[shipment_office_index]["id"]}\n'
-                            f'Name - {shipment_office[shipment_office_index]["name"]}\n')
-            elif shipment_method_index is not None and shipment_office_index is None:
-                shipment_method = await self.shipment_method()  # 0
-                self._base.shipment_method = shipment_method[shipment_method_index]['id']
-                logger.info(f'Выбран тип доставки:\nid - {shipment_method[shipment_method_index]["id"]}\n'
-                            f'Name - {shipment_method[shipment_method_index]["name"]}\n')
-        except KeyError:
-            raise AbcpAPIError('Неверно передан один из индексов')
-        except IndexError:
-            raise AbcpAPIError('Неверно передан один из индексов')
-
-
-class Orders:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def order_by_basket(self,
-                              payment_method: str = None,
-                              shipment_method: str = None,
-                              shipment_address: str = None,
-                              shipment_office: str = None,
-                              shipment_date: str = None,
-                              comment: str = None,
-                              basket_id: str = None,
-                              whole_order_only: int = None,
-                              position_ids: List = None,
-                              client_order_number: Union[str, int] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9E.D1.82.D0.BF.D1.80.D0.B0.D0.B2.D0.BA.D0.B0_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.8B_.D0.B2_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7
-        Отправка корзины в заказ
-        Осуществляет отправку позиций, содержащихся в корзине, в заказ.
-        Возвращает статус операции, а так же список созданных заказов со списками позиций в каждом из них.
-        Внимание!
-        При отправке заказа могут возникнуть ошибки, при этом, часть позиций могут отправиться.
-        Следовательно, независимо от статуса выполнения операции, необходимо проверять узел orders на наличие сформированных заказов.
-
-
-        :param payment_method: 	Идентификатор способа оплаты.
-        :param shipment_method: Идентификатор способа доставки.
-        :param shipment_address: Идентификатор адреса доставки.
-        :param shipment_office: Идентификатор офиса самовывоза
-        :param shipment_date: Дата отгрузки.
-        :param comment: Комментарий к заказу.
-        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
-        :param whole_order_only: Признак - оформить заказ целиком. Принимаемые значения - 0/1. По умолчанию - 0.
-        :param position_ids: Необязательный параметр - массив с номерами позиций заказа. Номера возвращает метод basket_content
-        :param client_order_number: Необязательный параметр - номер заказа в системе учета клиента
-        :return:
-        """
-        if payment_method is None:
-            payment_method = self._base.payment_method
-        if shipment_method is None:
-            shipment_method = self._base.shipment_method
-        if shipment_address is None:
-            shipment_address = self._base.shipment_address
-        if shipment_office is None:
-            shipment_office = self._base.shipment_office
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Basket.BASKET_ORDER, payload, True)
-
-    async def order_instant(self, positions: Union[List[Dict], Dict],
-                            payment_method: str = None, shipment_method: str = None,
-                            shipment_address: str = None, shipment_office: str = None, shipment_date: str = None,
-                            comment: str = None, basket_id: str = None, whole_order_only: int = 0,
-                            client_order_number: str = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9C.D0.BE.D0.BC.D0.B5.D0.BD.D1.82.D0.B0.D0.BB.D1.8C.D0.BD.D1.8B.D0.B9_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7
-        Объединяет в себе операции basket/add и basket/order то есть, добавляет переданный в параметрах список товаров в корзину и сразу же отправляет их в заказ.
-        У данной операции есть важная особенность - она не учитывает позиции, которые уже лежат в корзине,
-        в заказ они не попадут и останутся в корзине пользователя. Использование данной операции оптимально при автоматическом перезаказе у клиентов платформы ABCP.
-
-
-        :param positions: Набор добавляемых деталей в формате {'brand': luk, 'number': '602000600', 'itemKey': 'Xqgs...', 'supplierCode': '1234', 'quantity': 1, 'comment': 'Hello, part of world'}
-        :param payment_method: 	Идентификатор способа оплаты.
-        :type payment_method: str
-        :param shipment_method: Идентификатор способа доставки.
-        :type shipment_method: str
-        :param shipment_address: Идентификатор адреса доставки.
-        :type shipment_address: str
-        :param shipment_office: Идентификатор офиса самовывоза
-        :type shipment_office: str
-        :param shipment_date: Дата отгрузки.
-        :type shipment_date: str
-        :param comment: Комментарий к заказу.
-        :type comment: str
-        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
-        :type basket_id: str
-        :param whole_order_only: Признак - оформить заказ целиком. Принимаемые значения - 0/1. По умолчанию - 0.
-        :type whole_order_only: int
-        :param client_order_number: Необязательный параметр - номер заказа в системе учета клиента
-        :type client_order_number: str
-        :return:
-        """
-        if isinstance(positions, dict):
-            basket_positions = [positions]
-        else:
-            basket_positions = positions
-        del positions
-        if payment_method is None:
-            payment_method = self._base.payment_method
-        if shipment_method is None:
-            shipment_method = self._base.shipment_method
-        if shipment_address is None:
-            shipment_address = self._base.shipment_address
-        if shipment_office is None:
-            shipment_office = self._base.shipment_office
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Orders.ORDERS_INSTANT, payload, True)
-
-    async def orders_list(self, orders: Union[List, str, int]):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B9_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.BE.D0.B2_.D1.81.D0.BE_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.B0.D0.BC.D0.B8
-
-
-        :param orders: Список номеров заказа или один номер заказа
-        :type orders: :obj:`list` or :obj:`str`
-        :return:
-        """
-        if not isinstance(orders, list):
-            orders = [orders]
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Orders.GET_ORDERS_LIST, payload)
-
-    async def get_orders(self, format: str = None, skip: Optional[int] = None, limit: Optional[int] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.BE.D0.B2
-        Получение списка заказов
-        Осуществляет получение списка всех заказов клиента по страницам.
-        Сортировка по номеру заказа по убыванию, т.е. сначала передаются самые новые заказы.
-
-        :param format: (необязательный) - формат вывода результата. По умолчанию отображается информация только по заказам. При значении p - к заказам добавляется информация по всем позициям.
-        :param skip: (необязательный) - кол-во заказов, которые нужно пропустить. По умолчанию - 0.
-        :param limit: 	(необязательный) - кол-во заказов, которые нужно отобразить за один раз. Допускается любое значение от 1 до 1000. По умолчанию - 100.
-        :return:
-        """
-        if isinstance(format, str) and format != 'p':
-            raise AbcpWrongParameterError('Параметр format может принимать только значение "p"')
-        if isinstance(limit, int) and not 1 <= limit <= 1000:
-            raise AbcpWrongParameterError('Параметр limit может быть в диапазоне от 1 до 1000')
-
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Orders.GET_ORDERS, payload)
-
-    async def cancel_position(self, position_id: int):
-        """
-        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.97.D0.B0.D0.BF.D1.80.D0.BE.D1.81_.D0.BD.D0.B0_.D0.BE.D1.82.D0.BC.D0.B5.D0.BD.D1.83_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8
-        Запрос на отмену позиции
-        Выставляет позиции признак "Запрос на отмену"
-
-
-        :param position_id: Идентификатор позиции заказа
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Orders.CANCEL_POSITION, payload, True)
-
-
-class User:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def register(self,
-                       market_type: Union[str, int],
-                       name: str, second_name: str, surname: str,
-                       password: str, mobile: str,
-                       office: Union[str, int], email: str,
-                       icq: Union[str, int] = None, skype: str = None,
-                       region_id: Union[int, str] = None,
-                       business: Union[str, int] = None,
-                       organization_name: str = None,
-                       organization_form: str = None,
-                       organization_official_name: str = None,
-                       inn: Union[str, int] = None,
-                       kpp: Union[str, int] = None,
-                       ogrn: Union[str, int] = None,
-                       organization_official_address: Union[str, int] = None,
-                       bank_name: str = None,
-                       bik: Union[str, int] = None,
-                       correspondent_account: Union[str, int] = None,
-                       organization_account: Union[str, int] = None,
-                       delivery_address: str = None,
-                       comment: str = None,
-                       send_registration_email: Union[str, int] = None,
-                       member_of_club: str = None,
-                       birth_date: str = None,
-                       filial_id: Union[int, str] = None,
-                       profile_id: Union[int, str] = None,
-                       ):
-
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.A0.D0.B5.D0.B3.D0.B8.D1.81.D1.82.D1.80.D0.B0.D1.86.D0.B8.D1.8F_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
-        Принимает параметры для регистрации пользователя.
-        Осуществляет регистрацию нового пользователя в системе.
-        Возвращает статус выполнения операции регистрации, учетные данные нового пользователя, а так же сообщение об ошибке в случае возникновения таковой.
-        Регистрация через API запрещена при использовании модуля франчайзи, если выключен флаг "Головная компания (ГК) участвует в продажах".
-
-        :param market_type: Тип регистрации: 1. Розница 2. Опт
-        :param name: Имя
-        :param second_name: Отчество
-        :param surname: Фамилия
-        :param password: Пароль
-        :param mobile: Номер мобильного телефона
-        :param office: Идентификатор офиса
-        :param email: Почта
-        :param profile_id: Идентификатор профиля (Только для API администратора)
-        :param icq: ICQ UIN
-        :param skype: Skype
-        :param region_id: Код региона
-        :param business: Тип организации от 1 до 3. Автосервис, Автомагазин, Собственный автопарк
-        :param organization_name: Наименование организации
-        :param organization_form: Правовая форма организации. Варианты: ООО, ОАО, ЗАО, ТОО, АО, ЧП, ПБОЮЛ
-        :param organization_official_name: Наименование по регистрации (без правовой формы юр. лица)
-        :param inn: ИНН
-        :param kpp: КПП
-        :param ogrn: ОГРН
-        :param organization_official_address: Юридический адрес организации
-        :param bank_name: Наименование банка
-        :param bik: БИК
-        :param correspondent_account: Корреспондентский счет банка
-        :param organization_account: Расчетный счет организации
-        :param delivery_address: Адрес доставки
-        :param comment: Комментарий
-        :param send_registration_email: Необязательный, по-умолчанию - 0. 1 - отправлять клиенту, менеджеру письмо о регистрации 0 - не отправлять письмо
-        :param member_of_club: Название автоклуба
-        :param birth_date: Дата рождения, формат YYYY-MM-DD
-        :param filial_id: Код филиала (если имеются)
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.User.REGISTER, payload, True)
-
-    async def activate(self, user_code: int, activation_code: Union[str, int]):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.90.D0.BA.D1.82.D0.B8.D0.B2.D0.B0.D1.86.D0.B8.D1.8F_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
-
-
-        :param user_code: Внутренний код пользователя
-        :param activation_code: Код активации
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.User.ACTIVATION, payload, True)
-
-    async def user_info(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B4.D0.B0.D0.BD.D0.BD.D1.8B.D1.85_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F_.28.D0.B0.D0.B2.D1.82.D0.BE.D1.80.D0.B8.D0.B7.D0.B0.D1.86.D0.B8.D1.8F.29
-        Получение данных пользователя (авторизация)
-        Возвращает данные пользователя по логину и паролю.
-
-        :return:
-        """
-        return await self._base.request(_Methods.Client.User.USER_INFO)
-
-    async def restore(self, email_or_mobile: str = None, password_new: str = None, code: str = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.92.D0.BE.D1.81.D1.81.D1.82.D0.B0.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.B0.D1.80.D0.BE.D0.BB.D1.8F
-        Операция восстановление пароля пользователя.
-        Восстановление пароля состоит из двух этапов:
-
-        1. Запрос восстановления пароля с указанием номера телефона или email.
-        В результате успешного завершения будет отправлено стандартное письмо со ссылкой восстановления пароля на указанный email или код в SMS на указанный номер телефона.
-        2. Сохранение нового пароля с указанием кода подтверждения из SMS.
-        !!!Внимание!!!
-        Данный этап актуален только для восстановления по номеру телефона,
-        так как в случае с email, в письме придет ссылка на форму восстановления пароля на сайте, и второй этап будет выполнен в ней.
-        :param email_or_mobile:
-        :param password_new:
-        :param code:
-        :return:
-        """
-        if email_or_mobile is not None and any(x is not None for x in [password_new, code]):
-            raise AbcpAPIError('E-mail или мобильный используется только для первого этапа восстановления.'
-                               'А password_new и code для второго')
-        if email_or_mobile is None and any(x is None for x in [password_new, code]):
-            raise AbcpAPIError('Для второго этапа должны быть указаны password_new и code ')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.User.USER_RESTORE, payload, True)
-
-
-class Garage:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get_list(self, user_id: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9_.D0.B2_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6.D0.B5
-        Получение списка автомобилей в гараже
-
-
-        :param user_id: Указывается API администратором
-        :return:
-        """
-        if user_id is not None and not self._base.admin:
-            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
-        return await self._base.request(_Methods.Client.Garage.USER_GARAGE)
-
-    async def get_car(self, car_id: int, user_id: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BE.D0.B1_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5_.D0.B2_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6.D0.B5
-        Получение информации об автомобиле в гараже
-
-        Возвращает данные по одному автомобилю гаража текущего пользователя
-
-
-        :param user_id: Указывается API администратором
-        :param car_id: Идентификатор автомобиля в гараже
-        :return:
-        """
-        if user_id is not None and not self._base.admin:
-            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Garage.GARAGE_CAR, payload)
-
-    async def add(self, name: str,
-                  comment: str = None, year: str = None, vin: str = None,
-                  frame: str = None,
-                  mileage: str = None,
-                  manufacturer_id: Union[int, str] = None,
-                  model_id: Union[int, str] = None,
-                  modification_id: Union[int, str] = None,
-                  vehicle_reg_plate: str = None,
-                  user_id: Union[int, str] = None):
-
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D1.8F_.D0.B2_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6
-
-
-
-        :param name: Название автомобиля (пользовательское)
-        :param comment: Комментарий (пользовательский)
-        :param year: Год выпуска автомобиля
-        :param vin: VIN-код автомобиля
-        :param frame: Номер кузова автомобиля
-        :param mileage: Пробег автомобиля
-        :param manufacturer_id: Идентификатор марки автомобиля
-        :param model_id: Идентификатор модели автомобиля
-        :param modification_id: Идентификатор модификации автомобиля
-        :param vehicle_reg_plate: Государственный номер автомобиля
-        :param user_id: Указывается API администратором
-        :return:
-        """
-        if user_id is not None and not self._base.admin:
-            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
-        payload = generate_payload(**locals())
-
-        return await self._base.request(_Methods.Client.Garage.GARAGE_ADD, payload, True)
-
-    async def update(self, car_id: int, name: str = None,
-                     comment: str = None, year: str = None, vin: str = None,
-                     frame: str = None,
-                     mileage: str = None,
-                     manufacturer_id: Union[int, str] = None,
-                     model_id: Union[int, str] = None,
-                     modification_id: Union[int, str] = None,
-                     vehicle_reg_plate: str = None,
-                     user_id: Union[int, str] = None):
-
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D1.8F_.D0.B2_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6.D0.B5
-        Обновление машины в гараже.
-        Изменяет автомобиль в гараже.
-        Обязательным свойством автомобиля является только carId, то есть, можно передавать только те параметры, которые необходимо изменить.
-        Не переданные свойства изменены не будут.
-
-        :param car_id: Идентификатор автомобиля
-        :param name: Название автомобиля (пользовательское)
-        :param comment: Комментарий (пользовательский)
-        :param year: Год выпуска автомобиля
-        :param vin: VIN-код автомобиля
-        :param frame: Номер кузова автомобиля
-        :param mileage: Пробег автомобиля
-        :param manufacturer_id: Идентификатор марки автомобиля
-        :param model_id: Идентификатор модели автомобиля
-        :param modification_id: Идентификатор модификации автомобиля
-        :param vehicle_reg_plate: Государственный номер автомобиля
-        :param user_id: Указывается API администратором
-        :return:
-        """
-        if user_id is not None and not self._base.admin:
-            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Garage.GARAGE_UPDATE, payload, True)
-
-    async def delete(self, car_id: int, user_id: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.A3.D0.B4.D0.B0.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D1.8F_.D0.B8.D0.B7_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6.D0.B0
-        Удаление автомобиля из гаража
-
-
-        :param car_id:
-        :param user_id: Указывается API администратором
-        :return:
-        """
-        if user_id is not None and not self._base.admin:
-            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Garage.GARAGE_DELETE, payload, True)
-
-
-class CarTree:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def years(self, manufacturer_id: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.94.D0.B5.D1.80.D0.B5.D0.B2.D0.BE_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9
-        Получение списка годов дерева автомобилей
-        Возвращает список доступных годов для дерева автомобилей
-
-
-        :param manufacturer_id: Идентификатор марки для фильтрации. Необязательное.
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.CarTree.CAR_TREE_YEARS, payload)
-
-    async def manufacturers(self, year: int = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BC.D0.B0.D1.80.D0.BE.D0.BA_.D0.B4.D0.B5.D1.80.D0.B5.D0.B2.D0.B0_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9
-        Получение списка марок дерева автомобилей
-        Возвращает список доступных марок для дерева автомобилей
-
-
-        :param year: Год для фильтрации марок. Необязательное.
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.CarTree.CAR_TREE_MANUFACTURERS, payload)
-
-    async def models(self, manufacturer_id: Union[int, str] = None, year: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BC.D0.BE.D0.B4.D0.B5.D0.BB.D0.B5.D0.B9_.D0.B4.D0.B5.D1.80.D0.B5.D0.B2.D0.B0_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9
-
-
-        :param manufacturer_id: Идентификатор марки
-        :param year: Год для фильтрации моделей. Необязательное.
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.CarTree.CAR_TREE_MODELS, payload)
-
-    async def modifications(self, manufacturer_id: Union[int, str] = None, model_id: Union[int, str] = None,
-                            year: Union[int, str] = None):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BC.D0.BE.D0.B4.D0.B8.D1.84.D0.B8.D0.BA.D0.B0.D1.86.D0.B8.D0.B9_.D0.B4.D0.B5.D1.80.D0.B5.D0.B2.D0.B0_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9
-
-
-        :param manufacturer_id: Идентификатор марки
-        :param model_id: Идентификатор модели
-        :param year: Год для фильтрации моделей. Необязательное.
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.CarTree.CAR_TREE_MODIFICATIONS, payload)
-
-
-class Form:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def fields(self, name: str, locale: str = None):
-        """
-        Source:  https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D0.BE.D0.BB.D0.B5.D0.B9_.D1.84.D0.BE.D1.80.D0.BC.D1.8B
-        Получение списка полей формы
-
-        Возвращает список полей формы и все параметры в соответствии с установленными настройками в панели управления на странице Внешний вид и контент / Формы.
-        На текущий момент доступны только формы регистрации, реализованные в API-методе user/new.
-
-        :param name: Имя формы. Возможные значения: registration_wholesale - опт; registration_retail - розница
-        :param locale: 	Локаль формы (по умолчанию, ru_RU)
-        :return:
-        """
-        if name not in ['registration_wholesale', 'registration_retail']:
-            raise AbcpWrongParameterError(
-                "Name parameter must be one of: 'registration_wholesale', 'registration_retail'")
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.Client.Form.FIELDS, payload)
-
-
-class Articles:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def brands(self):
-        """
-        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D1.80.D0.B0.D0.B2.D0.BE.D1.87.D0.BD.D0.B8.D0.BA.D0.B0_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D0.BE.D0.B2
-        Получение справочника брендов
-        Возвращает список всех брендов зарегистрированных в системе с их синонимами.
-
-
-        :return:
-        """
-        return await self._base.request(_Methods.Client.Articles.BRANDS)
-
-    async def info(self, brand: Union[int, str], number: Union[str, int],
-                   format: str, source: Union[List, str],
-                   cross_image: int = None,
-                   with_original: str = None,
-                   locale: str = None):
-        if not self._base.admin:
-            raise AbcpAPIError('Операция доступна только администратору API')
-        if isinstance(format, str) and format not in 'bnpchmti':
-            raise AbcpWrongParameterError('Параметр "format" может содержать только символы: b, n, p, c, h, m, t, i')
-        if isinstance(source, str):
-            source = [source]
-        if isinstance(cross_image, int) and 'i' not in format:
-            raise AbcpWrongParameterError('')
-        if isinstance(source, list) and not all(x in ['standard', 'common', 'common_cat'] for x in source):
-            raise AbcpWrongParameterError(
-                'Параметр "source" может содержать следующие флаги: standard, common, common_cat')
-
-        payload = generate_payload(exclude=['cross_image', 'with_original'], **locals())
-        return await self._base.request(_Methods.Client.Articles.INFO, payload)
+import logging
+from typing import Dict, List, Union, Optional
+
+from ..api import _Methods
+from ..base import BaseAbcp
+from ..exceptions import NotEnoughRights, AbcpAPIError, AbcpParameterRequired, AbcpWrongParameterError
+from ..utils.payload import generate_payload
+
+logger = logging.getLogger('Cp.Client')
+
+
+class ClientApi:
+    def __init__(self, base: BaseAbcp):
+        """
+        Класс содержит методы клиентского интерфейса
+
+        https://www.abcp.ru/wiki/API.ABCP.Client
+        """
+        self._base = base
+        self.search = Search(base)
+        self.basket = Basket(base)
+        self.orders = Orders(base)
+        self.user = User(base)
+        self.garage = Garage(base)
+        self.car_tree = CarTree(base)
+        self.form = Form(base)
+        self.articles = Articles(base)
+
+
+class Search:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def brands(self, number: Union[str, int],
+                     use_online_stocks: Union[bool, int] = 0,
+                     locale: Optional[str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.B8.D1.81.D0.BA_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D0.BE.D0.B2_.D0.BF.D0.BE_.D0.BD.D0.BE.D0.BC.D0.B5.D1.80.D1.83
+        Осуществляет поиск по номеру детали и возвращает массив найденных брендов, имеющих деталь с искомым номером.
+        Аналог этапа выбора бренда на сайте.
+        :param number: Искомый номер детали
+        :type number: str or int
+        :param use_online_stocks: Флаг "использовать online-склады". Может принимать значения 0 или 1
+        :type use_online_stocks: str or int
+        :param locale: Локаль. Задается в формате language[_territory], например, ru_RU. По умолчанию используется локаль сайта.
+        :type locale: str
+        :return:
+        """
+        if isinstance(use_online_stocks, bool):
+            use_online_stocks = int(use_online_stocks)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Search.BRANDS, payload)
+
+    async def articles(self,
+                       number: Union[str, int],
+                       brand: Union[str, int],
+                       use_online_stocks: Union[bool, int] = 0,
+                       disable_online_filtering: Union[bool, int] = 0,
+                       with_out_analogs: Union[bool, int] = 1,
+                       profile_id: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.B8.D1.81.D0.BA_.D0.B4.D0.B5.D1.82.D0.B0.D0.BB.D0.B8_.D0.BF.D0.BE_.D0.BD.D0.BE.D0.BC.D0.B5.D1.80.D1.83_.D0.B8_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D1.83
+        Осуществляет поиск по номеру детали и бренду. Возвращает массив найденных деталей.
+        Так как один и тот же производитель может иметь несколько общепринятых наименований (например, GM и General Motors),
+        система постарается это учесть, используя собственную базу синонимов брендов.
+
+        :param number: Искомый номер детали
+        :type number: :obj:`str or int`
+        :param brand: Фильтр по имени производителя
+        :type brand: str or int
+        :param use_online_stocks: Флаг "использовать online-склады". Может принимать значения 0 или 1 (по умолчанию - 0)
+        :type use_online_stocks: str or int
+        :param disable_online_filtering: Флаг "отключить фильтры online поставщиков". Может принимать значения 0 или 1 (по умолчанию - 0)
+        :type disable_online_filtering: str or int
+        :param with_out_analogs: Флаг "исключить поиск по аналогам". По умолчанию - 0.
+        :type with_out_analogs: str or int
+        :param profile_id: При передаче этого параметра, поисковая выдача api-администратора формируется как для клиента с переданным профилем. Работает только под API-администратором.
+        :type profile_id: str or int
+        :return:
+        """
+        if not self._base.admin and profile_id is not None:
+            raise NotEnoughRights('Только API Администор может указывать Профиль пользователя')
+        if isinstance(use_online_stocks, bool):
+            use_online_stocks = int(use_online_stocks)
+        if isinstance(disable_online_filtering, bool):
+            disable_online_filtering = int(disable_online_filtering)
+        if isinstance(with_out_analogs, bool):
+            with_out_analogs = int(with_out_analogs)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Search.ARTICLES, payload)
+
+    async def batch(self, search: Union[List[Dict], Dict], profile_id: Union[int, str] = None):
+        """
+        Source https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.B0.D0.BA.D0.B5.D1.82.D0.BD.D1.8B.D0.B9_.D0.B7.D0.B0.D0.BF.D1.80.D0.BE.D1.81_.D0.B1.D0.B5.D0.B7_.D1.83.D1.87.D0.B5.D1.82.D0.B0_.D0.B0.D0.BD.D0.B0.D0.BB.D0.BE.D0.B3.D0.BE.D0.B2
+        Осуществляет поиск по номеру производителя и бренду детали. Возвращает массив найденных деталей.
+        Внимание! Данная операция не выполняет поиск по online-складам.
+
+
+        :param search: Набор искомых деталей в формате brand - number. Максимум 100 деталей.
+        :type search: dict or list of dicts ({'brand': 'LuK','number': '602000600'})
+        :param profile_id: При передаче этого параметра, поисковая выдача api-администратора формируется как для клиента с переданным профилем. Работает только под API-администратором.
+        :type profile_id: str or int
+        :return:
+        """
+        if not self._base.admin and profile_id is not None:
+            raise NotEnoughRights('Только API Администор может указывать Профиль пользователя')
+        if isinstance(search, dict):
+            search = [search]
+        payload = generate_payload(exclude=['search'], **locals())
+        # It can work with GET and POST, but the documentation specifies POST
+        return await self._base.request(_Methods.Client.Search.BATCH, payload, True)
+
+    async def history(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.98.D1.81.D1.82.D0.BE.D1.80.D0.B8.D1.8F_.D0.BF.D0.BE.D0.B8.D1.81.D0.BA.D0.B0
+        Возвращает массив последних (не более 50) поисковых запросов текущего пользователя.
+
+
+        :return: dict
+        """
+        return await self._base.request(_Methods.Client.Search.HISTORY)
+
+    async def tips(self, number: Union[str, int], locale: Optional[str]):
+        """Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.B4.D1.81.D0.BA.D0.B0.D0.B7.D0.BA.D0.B8_.D0.BF.D0.BE_.D0.BF.D0.BE.D0.B8.D1.81.D0.BA.D1.83
+        Возвращает по части номера массив подходящих пар бренд - номер
+
+
+        :param number:Номер (часть номера) детали
+        :type number: :obj:`str` or `int`
+        :param locale: Локаль. Задается в формате language[_territory], например, ru_RU. По умолчанию используется локаль сайта.
+        :type locale: :obj:`str
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Search.TIPS, payload)
+
+    async def advices(self, brand: Union[str, int], number: Union[str, int], limit: Optional[int] = 5):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.B8.D1.81.D0.BA_.D1.81.D0.BE.D0.BF.D1.83.D1.82.D1.81.D1.82.D0.B2.D1.83.D1.8E.D1.89.D0.B8.D1.85_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.BE.D0.B2
+        Функция реализует механизм "с этим товаром покупают" на основе статистики покупки комплектов товаров.
+        Типичный пример использования функции: покупатель выбрал масляный фильтр - система рекомендует остальные товары из набора для ТО.
+        Или, покупатель выбрал левый передний амортизатор, система покажет правый передний.
+        Осуществляет поиск сопутствующих товаров по запрашиваемой паре "Бренд-номер".
+        Дополнительно можно передать параметр limit (рекомендуется = 5), ограничивающий выдачу рекомендаций.
+
+
+        :param brand: Имя производителя
+        :type brand: :obj:`Union[str, int]`
+        :param number: Номер детали
+        :type number: :obj:`Union[str, int]`
+        :param limit: необязательный параметр, ограничивающий выдачу
+        :type limit :obj:`int`
+        :return:
+        """
+
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Search.ADVICES, payload)
+
+    async def advices_batch(self, articles: Union[List[Dict], Dict], limit: Optional[int] = 5):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9C.D0.B5.D1.85.D0.B0.D0.BD.D0.B8.D0.B7.D0.BC_.22.D0.A1_.D1.8D.D1.82.D0.B8.D0.BC_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.BE.D0.BC_.D0.BF.D0.BE.D0.BA.D1.83.D0.BF.D0.B0.D1.8E.D1.82.22
+        Функция реализует механизм "с этим товаром покупают" по нескольким товарам.
+        Дополнительно можно передать параметр limit (рекомендуется = 5), ограничивающий выдачу рекомендаций.
+        Параметры товаров передаются в виде JSON-массива articles из объектов с полями 'brand' и 'number'.
+
+
+        :param articles:
+        :param limit:
+        :return:
+        """
+        if isinstance(articles, dict):
+            articles = [articles]
+        payload = generate_payload(exclude=['articles'], **locals())
+        return await self._base.request(_Methods.Client.Search.ADVICES_BATCH, payload, True, json=True)
+
+
+class Basket:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get_baskets_list(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD
+        Получение списка корзин
+
+
+        :return: dict
+        """
+        return await self._base.request(_Methods.Client.Basket.BASKETS_LIST)
+
+    async def add(self, basket_positions: Union[List[Dict], Dict], basket_id: Union[int, str] = None):
+        """
+        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.BE.D0.B2_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.83._.D0.A3.D0.B4.D0.B0.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.B0_.D0.B8.D0.B7_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.8B
+
+        Осуществляет подготовку к отправке заказа на товары по номеру производителя, бренду и коду поставки или по коду детали.
+        Возвращает статус добавления товара в корзину по каждой позиции.
+        При добавлении brand - number - itemKey - supplierCode позиции,
+        которая уже была ранее добавлена в корзину, значение quantity будет прибавлено к существующему.
+        Удаление позиции - при добавлении brand - number - itemKey - supplierCode позиции,
+        которая уже была ранее добавлена в корзину, со значением quantity равным 0, позиция будет удалена из корзины.
+        Для изменения количества рекомендуется удалять позицию и ее добавлять заново с требуемым количеством.
+
+
+
+        :param basket_positions: Набор добавляемых деталей в формате brand - number - itemKey - supplierCode или code с указанием добавляемого количества в поле quantity и комментария к позиции в поле comment
+        :type basket_positions: :obj:`list` or :obj:`dict
+        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
+        :type basket_id: :obj:`str` or :obj:`int`
+        :return: dict
+        """
+        if isinstance(basket_positions, dict):
+            basket_positions = [basket_positions]
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Client.Basket.BASKET_ADD, payload, True)
+
+    async def clear(self, basket_id: Union[int, str] = None):
+        """
+        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9E.D1.87.D0.B8.D1.81.D1.82.D0.BA.D0.B0_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.8B
+
+        Удаляет все позиции из корзины.
+
+
+        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
+        :type basket_id: :obj:`Union[str, int]`
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Basket.BASKET_CLEAR, payload, True)
+
+    async def content(self, basket_id: Union[int, str] = None):
+
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.82.D0.BE.D0.B2.D0.B0.D1.80.D0.BE.D0.B2_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D0.B5
+
+        Получение списка товаров в корзине
+        Возвращает список позиций, находящихся в корзине.
+        Внимание! Если у вас подключена опция "Корзина: разрешать частичное оформление заказа".
+        То в ответ веб-сервиса будут попадать только отмеченные позиции.
+
+
+        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
+        :type basket_id: :obj:`Union[str, int]`
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Basket.BASKET_CONTENT, payload)
+
+    async def options(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BE.D0.BF.D1.86.D0.B8.D0.B9_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.8B
+
+        Получение опций корзины
+        Возвращает значение некоторых опций Корзины.
+
+        :return:
+        """
+        return await self._base.request(_Methods.Client.Basket.BASKET_OPTIONS)
+
+    async def payment_method(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.81.D0.BF.D0.BE.D1.81.D0.BE.D0.B1.D0.BE.D0.B2_.D0.BE.D0.BF.D0.BB.D0.B0.D1.82.D1.8B
+
+        Получение списка способов оплаты
+        Возвращает список доступных способов оплаты.
+        Идентификатор способа оплаты необходим при отправке заказа (при включенной опции "Корзина: показывать тип оплаты").
+        :return:
+        """
+        return await self._base.request(_Methods.Client.Basket.PAYMENT_METHODS)
+
+    async def shipment_method(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D1.81.D0.BF.D0.BE.D1.81.D0.BE.D0.B1.D0.BE.D0.B2_.D0.B4.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D0.BA.D0.B8
+
+        Получение списка способов доставки
+
+        :return:
+        """
+        return await self._base.request(_Methods.Client.Basket.SHIPMENT_METHOD)
+
+    async def shipment_offices(self, offices_type: Optional[str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BE.D1.84.D0.B8.D1.81.D0.BE.D0.B2_.D1.81.D0.B0.D0.BC.D0.BE.D0.B2.D1.8B.D0.B2.D0.BE.D0.B7.D0.B0
+
+        Получение списка офисов самовывоза
+        Возвращает список доступных офисов для самовывоза.
+        Идентификатор офиса самовывоза при отправке заказа
+        (при включенной опции "Заказы: показывать офисы при выборе самовывоза").
+
+
+        :param offices_type: Не обязательный параметр:
+                            order - (используется по-умолчанию) возвращает офисы используемые для оформления заказа
+                            registration - возвращает офисы используемые для регистрации пользователя при включенной опции "Офисы: включить привязку к клиентам"
+        :return:
+        """
+        if isinstance(offices_type, str) and (offices_type != 'order' or offices_type != 'registration'):
+            raise AbcpParameterRequired("offices_type может принимать значения 'order' или 'registration'")
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Basket.SHIPMENT_OFFICES, payload)
+
+    async def shipment_address(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B0.D0.B4.D1.80.D0.B5.D1.81.D0.BE.D0.B2_.D0.B4.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D0.BA.D0.B8
+
+        Получение списка адресов доставки
+        Возвращает список доступных адресов доставки. Идентификатор адреса доставки необходим при отправке заказа.
+
+        :return:
+        """
+        return await self._base.request(_Methods.Client.Basket.SHIPMENT_ADDRESS)
+
+    async def shipment_dates(self, min_deadline_time: int, max_deadline_time: int,
+                             shipment_address: Union[str, int] = None):
+        """
+        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B4.D0.B0.D1.82_.D0.BE.D1.82.D0.B3.D1.80.D1.83.D0.B7.D0.BA.D0.B8
+
+        Получение списка дат отгрузки
+
+        Возвращает список доступных дат отгрузки.
+        Дата отгрузки необходима при отправке заказа при включенной опции "Корзина: показывать дату отгрузки".
+
+
+        :param min_deadline_time: Минимальный срок поставки, в часах, среди всех позиций, которые вы собрались отправлять в заказ.
+        :param max_deadline_time: Максимальный срок поставки, в часах, среди всех позиций, которые вы собрались отправлять в заказ.
+        :param shipment_address: id адреса доставки. Необязательный параметр.
+        Необходимо отправлять, если заказ будет оформлен с доставкой.
+        Для подготовки доставки офисам может требоваться дополнительное время на сборку.
+        При отправке параметра shipmentAddress получаем актуальные даты отгрузки с учетом времени комплектации в настройках офиса.
+
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Basket.SHIPMENT_DATES)
+
+    async def add_shipment_address(self, address: str):
+        """
+        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B0.D0.B4.D1.80.D0.B5.D1.81.D0.B0_.D0.B4.D0.BE.D1.81.D1.82.D0.B0.D0.B2.D0.BA.D0.B8
+        Добавление адреса доставки
+        Для текущего покупателя добавляет "адрес доставки" и возвращает его идентификатор используемый в методе Отправка корзины в заказ
+
+
+        :param address: Обязательный, строка содержащая адрес.
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Basket.SHIPMENT_DATES, payload, True)
+
+    async def set_client_params(self,
+                                payment_method_index: int,
+                                shipment_address_index: int,
+                                shipment_method_index: int = None,
+                                shipment_office_index: int = None):
+        """
+        Устанавливает параметры для метода order.
+        Если все индексы переданы верно в методы api.cp.client.order.order_by_basket и api.cp.client.order.order_instant не требуется передавать аргументы:
+        'payment_method', 'shipment_address', 'shipment_method', 'shipment_office'.
+
+        :param payment_method_index: Обязательный параметр для любого типа отгрузки. Индекс типа оплаты полученный методом payment_method
+        :type payment_method_index: int
+        :param shipment_address_index: Обязательный параметр для любого типа отгрузки. Индекс адреса доставки полученный методом shipment_address
+        :type shipment_address_index: int
+        :param shipment_method_index: Не обязательный параметр, если используется самовывоз. Индекс типа доставки полученный методом payment_method
+        :type shipment_method_index: int
+        :param shipment_office_index: Не обязательный параметр, если используется доставка. Индекс офиса самовывоза полученый методом shipment_offices
+        :type shipment_office_index: int
+        :return:
+        """
+        try:
+            if shipment_address_index != 0 and shipment_office_index is not None:
+                raise AbcpParameterRequired('Для выбора самовывоза необходимо передать "shipment_address_index=0"')
+            payment_method = await self.payment_method()  # 0
+            self._base.payment_method = payment_method[payment_method_index]['id']
+            logger.info(
+                f'Выбран тип оплаты:\nID - {payment_method[payment_method_index]["id"]}\n'
+                f'Name - {payment_method[payment_method_index]["name"]}')
+            if shipment_method_index is not None and shipment_address_index is not None:
+                shipment_address = await self.shipment_address()  # 1
+                self._base.shipment_address = shipment_address[shipment_address_index]["id"]
+                logger.info(f'\n\n\n{shipment_address}\n\n\n\n')
+                logger.info(f'Выбран адрес доставки:\nID - {shipment_address[shipment_address_index]["id"]}\n'
+                            f'Name - {shipment_address[shipment_address_index]["name"]}')
+
+            if shipment_office_index is not None and shipment_method_index is None:
+                shipment_office = await self.shipment_offices()
+                self._base.shipment_office = shipment_office[shipment_office_index]["id"]
+                logger.info(f'Выбран офис самовывоза:\nID - {shipment_office[shipment_office_index]["id"]}\n'
+                            f'Name - {shipment_office[shipment_office_index]["name"]}\n')
+            elif shipment_method_index is not None and shipment_office_index is None:
+                shipment_method = await self.shipment_method()  # 0
+                self._base.shipment_method = shipment_method[shipment_method_index]['id']
+                logger.info(f'Выбран тип доставки:\nid - {shipment_method[shipment_method_index]["id"]}\n'
+                            f'Name - {shipment_method[shipment_method_index]["name"]}\n')
+        except KeyError:
+            raise AbcpAPIError('Неверно передан один из индексов')
+        except IndexError:
+            raise AbcpAPIError('Неверно передан один из индексов')
+
+
+class Orders:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def order_by_basket(self,
+                              payment_method: str = None,
+                              shipment_method: str = None,
+                              shipment_address: str = None,
+                              shipment_office: str = None,
+                              shipment_date: str = None,
+                              comment: str = None,
+                              basket_id: str = None,
+                              whole_order_only: int = None,
+                              position_ids: List = None,
+                              client_order_number: Union[str, int] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9E.D1.82.D0.BF.D1.80.D0.B0.D0.B2.D0.BA.D0.B0_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D1.8B_.D0.B2_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7
+        Отправка корзины в заказ
+        Осуществляет отправку позиций, содержащихся в корзине, в заказ.
+        Возвращает статус операции, а так же список созданных заказов со списками позиций в каждом из них.
+        Внимание!
+        При отправке заказа могут возникнуть ошибки, при этом, часть позиций могут отправиться.
+        Следовательно, независимо от статуса выполнения операции, необходимо проверять узел orders на наличие сформированных заказов.
+
+
+        :param payment_method: 	Идентификатор способа оплаты.
+        :param shipment_method: Идентификатор способа доставки.
+        :param shipment_address: Идентификатор адреса доставки.
+        :param shipment_office: Идентификатор офиса самовывоза
+        :param shipment_date: Дата отгрузки.
+        :param comment: Комментарий к заказу.
+        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
+        :param whole_order_only: Признак - оформить заказ целиком. Принимаемые значения - 0/1. По умолчанию - 0.
+        :param position_ids: Необязательный параметр - массив с номерами позиций заказа. Номера возвращает метод basket_content
+        :param client_order_number: Необязательный параметр - номер заказа в системе учета клиента
+        :return:
+        """
+        if payment_method is None:
+            payment_method = self._base.payment_method
+        if shipment_method is None:
+            shipment_method = self._base.shipment_method
+        if shipment_address is None:
+            shipment_address = self._base.shipment_address
+        if shipment_office is None:
+            shipment_office = self._base.shipment_office
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Basket.BASKET_ORDER, payload, True)
+
+    async def order_instant(self, positions: Union[List[Dict], Dict],
+                            payment_method: str = None, shipment_method: str = None,
+                            shipment_address: str = None, shipment_office: str = None, shipment_date: str = None,
+                            comment: str = None, basket_id: str = None, whole_order_only: int = 0,
+                            client_order_number: str = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9C.D0.BE.D0.BC.D0.B5.D0.BD.D1.82.D0.B0.D0.BB.D1.8C.D0.BD.D1.8B.D0.B9_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7
+        Объединяет в себе операции basket/add и basket/order то есть, добавляет переданный в параметрах список товаров в корзину и сразу же отправляет их в заказ.
+        У данной операции есть важная особенность - она не учитывает позиции, которые уже лежат в корзине,
+        в заказ они не попадут и останутся в корзине пользователя. Использование данной операции оптимально при автоматическом перезаказе у клиентов платформы ABCP.
+
+
+        :param positions: Набор добавляемых деталей в формате {'brand': luk, 'number': '602000600', 'itemKey': 'Xqgs...', 'supplierCode': '1234', 'quantity': 1, 'comment': 'Hello, part of world'}
+        :param payment_method: 	Идентификатор способа оплаты.
+        :type payment_method: str
+        :param shipment_method: Идентификатор способа доставки.
+        :type shipment_method: str
+        :param shipment_address: Идентификатор адреса доставки.
+        :type shipment_address: str
+        :param shipment_office: Идентификатор офиса самовывоза
+        :type shipment_office: str
+        :param shipment_date: Дата отгрузки.
+        :type shipment_date: str
+        :param comment: Комментарий к заказу.
+        :type comment: str
+        :param basket_id: Необязательный параметр - идентификатор корзины при использовании мультикорзины
+        :type basket_id: str
+        :param whole_order_only: Признак - оформить заказ целиком. Принимаемые значения - 0/1. По умолчанию - 0.
+        :type whole_order_only: int
+        :param client_order_number: Необязательный параметр - номер заказа в системе учета клиента
+        :type client_order_number: str
+        :return:
+        """
+        if isinstance(positions, dict):
+            basket_positions = [positions]
+        else:
+            basket_positions = positions
+        del positions
+        if payment_method is None:
+            payment_method = self._base.payment_method
+        if shipment_method is None:
+            shipment_method = self._base.shipment_method
+        if shipment_address is None:
+            shipment_address = self._base.shipment_address
+        if shipment_office is None:
+            shipment_office = self._base.shipment_office
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Orders.ORDERS_INSTANT, payload, True)
+
+    async def orders_list(self, orders: Union[List, str, int]):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B9_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.BE.D0.B2_.D1.81.D0.BE_.D1.81.D1.82.D0.B0.D1.82.D1.83.D1.81.D0.B0.D0.BC.D0.B8
+
+
+        :param orders: Список номеров заказа или один номер заказа
+        :type orders: :obj:`list` or :obj:`str`
+        :return:
+        """
+        if not isinstance(orders, list):
+            orders = [orders]
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Orders.GET_ORDERS_LIST, payload)
+
+    async def get_orders(self, format: str = None, skip: Optional[int] = None, limit: Optional[int] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B7.D0.B0.D0.BA.D0.B0.D0.B7.D0.BE.D0.B2
+        Получение списка заказов
+        Осуществляет получение списка всех заказов клиента по страницам.
+        Сортировка по номеру заказа по убыванию, т.е. сначала передаются самые новые заказы.
+
+        :param format: (необязательный) - формат вывода результата. По умолчанию отображается информация только по заказам. При значении p - к заказам добавляется информация по всем позициям.
+        :param skip: (необязательный) - кол-во заказов, которые нужно пропустить. По умолчанию - 0.
+        :param limit: 	(необязательный) - кол-во заказов, которые нужно отобразить за один раз. Допускается любое значение от 1 до 1000. По умолчанию - 100.
+        :return:
+        """
+        if isinstance(format, str) and format != 'p':
+            raise AbcpWrongParameterError('Параметр format может принимать только значение "p"')
+        if isinstance(limit, int) and not 1 <= limit <= 1000:
+            raise AbcpWrongParameterError('Параметр limit может быть в диапазоне от 1 до 1000')
+
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Orders.GET_ORDERS, payload)
+
+    async def cancel_position(self, position_id: int):
+        """
+        Source:https://www.abcp.ru/wiki/API.ABCP.Client#.D0.97.D0.B0.D0.BF.D1.80.D0.BE.D1.81_.D0.BD.D0.B0_.D0.BE.D1.82.D0.BC.D0.B5.D0.BD.D1.83_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8
+        Запрос на отмену позиции
+        Выставляет позиции признак "Запрос на отмену"
+
+
+        :param position_id: Идентификатор позиции заказа
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Orders.CANCEL_POSITION, payload, True)
+
+
+class User:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def register(self,
+                       market_type: Union[str, int],
+                       name: str, second_name: str, surname: str,
+                       password: str, mobile: str,
+                       office: Union[str, int], email: str,
+                       icq: Union[str, int] = None, skype: str = None,
+                       region_id: Union[int, str] = None,
+                       business: Union[str, int] = None,
+                       organization_name: str = None,
+                       organization_form: str = None,
+                       organization_official_name: str = None,
+                       inn: Union[str, int] = None,
+                       kpp: Union[str, int] = None,
+                       ogrn: Union[str, int] = None,
+                       organization_official_address: Union[str, int] = None,
+                       bank_name: str = None,
+                       bik: Union[str, int] = None,
+                       correspondent_account: Union[str, int] = None,
+                       organization_account: Union[str, int] = None,
+                       delivery_address: str = None,
+                       comment: str = None,
+                       send_registration_email: Union[str, int] = None,
+                       member_of_club: str = None,
+                       birth_date: str = None,
+                       filial_id: Union[int, str] = None,
+                       profile_id: Union[int, str] = None,
+                       ):
+
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.A0.D0.B5.D0.B3.D0.B8.D1.81.D1.82.D1.80.D0.B0.D1.86.D0.B8.D1.8F_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
+        Принимает параметры для регистрации пользователя.
+        Осуществляет регистрацию нового пользователя в системе.
+        Возвращает статус выполнения операции регистрации, учетные данные нового пользователя, а так же сообщение об ошибке в случае возникновения таковой.
+        Регистрация через API запрещена при использовании модуля франчайзи, если выключен флаг "Головная компания (ГК) участвует в продажах".
+
+        :param market_type: Тип регистрации: 1. Розница 2. Опт
+        :param name: Имя
+        :param second_name: Отчество
+        :param surname: Фамилия
+        :param password: Пароль
+        :param mobile: Номер мобильного телефона
+        :param office: Идентификатор офиса
+        :param email: Почта
+        :param profile_id: Идентификатор профиля (Только для API администратора)
+        :param icq: ICQ UIN
+        :param skype: Skype
+        :param region_id: Код региона
+        :param business: Тип организации от 1 до 3. Автосервис, Автомагазин, Собственный автопарк
+        :param organization_name: Наименование организации
+        :param organization_form: Правовая форма организации. Варианты: ООО, ОАО, ЗАО, ТОО, АО, ЧП, ПБОЮЛ
+        :param organization_official_name: Наименование по регистрации (без правовой формы юр. лица)
+        :param inn: ИНН
+        :param kpp: КПП
+        :param ogrn: ОГРН
+        :param organization_official_address: Юридический адрес организации
+        :param bank_name: Наименование банка
+        :param bik: БИК
+        :param correspondent_account: Корреспондентский счет банка
+        :param organization_account: Расчетный счет организации
+        :param delivery_address: Адрес доставки
+        :param comment: Комментарий
+        :param send_registration_email: Необязательный, по-умолчанию - 0. 1 - отправлять клиенту, менеджеру письмо о регистрации 0 - не отправлять письмо
+        :param member_of_club: Название автоклуба
+        :param birth_date: Дата рождения, формат YYYY-MM-DD
+        :param filial_id: Код филиала (если имеются)
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.User.REGISTER, payload, True)
+
+    async def activate(self, user_code: int, activation_code: Union[str, int]):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.90.D0.BA.D1.82.D0.B8.D0.B2.D0.B0.D1.86.D0.B8.D1.8F_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
+
+
+        :param user_code: Внутренний код пользователя
+        :param activation_code: Код активации
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.User.ACTIVATION, payload, True)
+
+    async def user_info(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B4.D0.B0.D0.BD.D0.BD.D1.8B.D1.85_.D0.BF.D0.BE.D0.BB.D1.8C.D0.B7.D0.BE.D0.B2.D0.B0.D1.82.D0.B5.D0.BB.D1.8F_.28.D0.B0.D0.B2.D1.82.D0.BE.D1.80.D0.B8.D0.B7.D0.B0.D1.86.D0.B8.D1.8F.29
+        Получение данных пользователя (авторизация)
+        Возвращает данные пользователя по логину и паролю.
+
+        :return:
+        """
+        return await self._base.request(_Methods.Client.User.USER_INFO)
+
+    async def restore(self, email_or_mobile: str = None, password_new: str = None, code: str = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.92.D0.BE.D1.81.D1.81.D1.82.D0.B0.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.B0.D1.80.D0.BE.D0.BB.D1.8F
+        Операция восстановление пароля пользователя.
+        Восстановление пароля состоит из двух этапов:
+
+        1. Запрос восстановления пароля с указанием номера телефона или email.
+        В результате успешного завершения будет отправлено стандартное письмо со ссылкой восстановления пароля на указанный email или код в SMS на указанный номер телефона.
+        2. Сохранение нового пароля с указанием кода подтверждения из SMS.
+        !!!Внимание!!!
+        Данный этап актуален только для восстановления по номеру телефона,
+        так как в случае с email, в письме придет ссылка на форму восстановления пароля на сайте, и второй этап будет выполнен в ней.
+        :param email_or_mobile:
+        :param password_new:
+        :param code:
+        :return:
+        """
+        if email_or_mobile is not None and any(x is not None for x in [password_new, code]):
+            raise AbcpAPIError('E-mail или мобильный используется только для первого этапа восстановления.'
+                               'А password_new и code для второго')
+        if email_or_mobile is None and any(x is None for x in [password_new, code]):
+            raise AbcpAPIError('Для второго этапа должны быть указаны password_new и code ')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.User.USER_RESTORE, payload, True)
+
+
+class Garage:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get_list(self, user_id: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9_.D0.B2_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6.D0.B5
+        Получение списка автомобилей в гараже
+
+
+        :param user_id: Указывается API администратором
+        :return:
+        """
+        if user_id is not None and not self._base.admin:
+            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
+        return await self._base.request(_Methods.Client.Garage.USER_GARAGE)
+
+    async def get_car(self, car_id: int, user_id: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B8.D0.BD.D1.84.D0.BE.D1.80.D0.BC.D0.B0.D1.86.D0.B8.D0.B8_.D0.BE.D0.B1_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5_.D0.B2_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6.D0.B5
+        Получение информации об автомобиле в гараже
+
+        Возвращает данные по одному автомобилю гаража текущего пользователя
+
+
+        :param user_id: Указывается API администратором
+        :param car_id: Идентификатор автомобиля в гараже
+        :return:
+        """
+        if user_id is not None and not self._base.admin:
+            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Garage.GARAGE_CAR, payload)
+
+    async def add(self, name: str,
+                  comment: str = None, year: str = None, vin: str = None,
+                  frame: str = None,
+                  mileage: str = None,
+                  manufacturer_id: Union[int, str] = None,
+                  model_id: Union[int, str] = None,
+                  modification_id: Union[int, str] = None,
+                  vehicle_reg_plate: str = None,
+                  user_id: Union[int, str] = None):
+
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.94.D0.BE.D0.B1.D0.B0.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D1.8F_.D0.B2_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6
+
+
+
+        :param name: Название автомобиля (пользовательское)
+        :param comment: Комментарий (пользовательский)
+        :param year: Год выпуска автомобиля
+        :param vin: VIN-код автомобиля
+        :param frame: Номер кузова автомобиля
+        :param mileage: Пробег автомобиля
+        :param manufacturer_id: Идентификатор марки автомобиля
+        :param model_id: Идентификатор модели автомобиля
+        :param modification_id: Идентификатор модификации автомобиля
+        :param vehicle_reg_plate: Государственный номер автомобиля
+        :param user_id: Указывается API администратором
+        :return:
+        """
+        if user_id is not None and not self._base.admin:
+            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
+        payload = generate_payload(**locals())
+
+        return await self._base.request(_Methods.Client.Garage.GARAGE_ADD, payload, True)
+
+    async def update(self, car_id: int, name: str = None,
+                     comment: str = None, year: str = None, vin: str = None,
+                     frame: str = None,
+                     mileage: str = None,
+                     manufacturer_id: Union[int, str] = None,
+                     model_id: Union[int, str] = None,
+                     modification_id: Union[int, str] = None,
+                     vehicle_reg_plate: str = None,
+                     user_id: Union[int, str] = None):
+
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D1.8F_.D0.B2_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6.D0.B5
+        Обновление машины в гараже.
+        Изменяет автомобиль в гараже.
+        Обязательным свойством автомобиля является только carId, то есть, можно передавать только те параметры, которые необходимо изменить.
+        Не переданные свойства изменены не будут.
+
+        :param car_id: Идентификатор автомобиля
+        :param name: Название автомобиля (пользовательское)
+        :param comment: Комментарий (пользовательский)
+        :param year: Год выпуска автомобиля
+        :param vin: VIN-код автомобиля
+        :param frame: Номер кузова автомобиля
+        :param mileage: Пробег автомобиля
+        :param manufacturer_id: Идентификатор марки автомобиля
+        :param model_id: Идентификатор модели автомобиля
+        :param modification_id: Идентификатор модификации автомобиля
+        :param vehicle_reg_plate: Государственный номер автомобиля
+        :param user_id: Указывается API администратором
+        :return:
+        """
+        if user_id is not None and not self._base.admin:
+            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Garage.GARAGE_UPDATE, payload, True)
+
+    async def delete(self, car_id: int, user_id: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.A3.D0.B4.D0.B0.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D1.8F_.D0.B8.D0.B7_.D0.B3.D0.B0.D1.80.D0.B0.D0.B6.D0.B0
+        Удаление автомобиля из гаража
+
+
+        :param car_id:
+        :param user_id: Указывается API администратором
+        :return:
+        """
+        if user_id is not None and not self._base.admin:
+            raise AbcpAPIError('Параметр "user_id" может быть передан только API администратором')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Garage.GARAGE_DELETE, payload, True)
+
+
+class CarTree:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def years(self, manufacturer_id: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.94.D0.B5.D1.80.D0.B5.D0.B2.D0.BE_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9
+        Получение списка годов дерева автомобилей
+        Возвращает список доступных годов для дерева автомобилей
+
+
+        :param manufacturer_id: Идентификатор марки для фильтрации. Необязательное.
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.CarTree.CAR_TREE_YEARS, payload)
+
+    async def manufacturers(self, year: int = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BC.D0.B0.D1.80.D0.BE.D0.BA_.D0.B4.D0.B5.D1.80.D0.B5.D0.B2.D0.B0_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9
+        Получение списка марок дерева автомобилей
+        Возвращает список доступных марок для дерева автомобилей
+
+
+        :param year: Год для фильтрации марок. Необязательное.
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.CarTree.CAR_TREE_MANUFACTURERS, payload)
+
+    async def models(self, manufacturer_id: Union[int, str] = None, year: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BC.D0.BE.D0.B4.D0.B5.D0.BB.D0.B5.D0.B9_.D0.B4.D0.B5.D1.80.D0.B5.D0.B2.D0.B0_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9
+
+
+        :param manufacturer_id: Идентификатор марки
+        :param year: Год для фильтрации моделей. Необязательное.
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.CarTree.CAR_TREE_MODELS, payload)
+
+    async def modifications(self, manufacturer_id: Union[int, str] = None, model_id: Union[int, str] = None,
+                            year: Union[int, str] = None):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BC.D0.BE.D0.B4.D0.B8.D1.84.D0.B8.D0.BA.D0.B0.D1.86.D0.B8.D0.B9_.D0.B4.D0.B5.D1.80.D0.B5.D0.B2.D0.B0_.D0.B0.D0.B2.D1.82.D0.BE.D0.BC.D0.BE.D0.B1.D0.B8.D0.BB.D0.B5.D0.B9
+
+
+        :param manufacturer_id: Идентификатор марки
+        :param model_id: Идентификатор модели
+        :param year: Год для фильтрации моделей. Необязательное.
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.CarTree.CAR_TREE_MODIFICATIONS, payload)
+
+
+class Form:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def fields(self, name: str, locale: str = None):
+        """
+        Source:  https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D0.BE.D0.BB.D0.B5.D0.B9_.D1.84.D0.BE.D1.80.D0.BC.D1.8B
+        Получение списка полей формы
+
+        Возвращает список полей формы и все параметры в соответствии с установленными настройками в панели управления на странице Внешний вид и контент / Формы.
+        На текущий момент доступны только формы регистрации, реализованные в API-методе user/new.
+
+        :param name: Имя формы. Возможные значения: registration_wholesale - опт; registration_retail - розница
+        :param locale: 	Локаль формы (по умолчанию, ru_RU)
+        :return:
+        """
+        if name not in ['registration_wholesale', 'registration_retail']:
+            raise AbcpWrongParameterError(
+                "Name parameter must be one of: 'registration_wholesale', 'registration_retail'")
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.Client.Form.FIELDS, payload)
+
+
+class Articles:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def brands(self):
+        """
+        Source: https://www.abcp.ru/wiki/API.ABCP.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D1.80.D0.B0.D0.B2.D0.BE.D1.87.D0.BD.D0.B8.D0.BA.D0.B0_.D0.B1.D1.80.D0.B5.D0.BD.D0.B4.D0.BE.D0.B2
+        Получение справочника брендов
+        Возвращает список всех брендов зарегистрированных в системе с их синонимами.
+
+
+        :return:
+        """
+        return await self._base.request(_Methods.Client.Articles.BRANDS)
+
+    async def info(self, brand: Union[int, str], number: Union[str, int],
+                   format: str, source: Union[List, str],
+                   cross_image: int = None,
+                   with_original: str = None,
+                   locale: str = None):
+        if not self._base.admin:
+            raise AbcpAPIError('Операция доступна только администратору API')
+        if isinstance(format, str) and format not in 'bnpchmti':
+            raise AbcpWrongParameterError('Параметр "format" может содержать только символы: b, n, p, c, h, m, t, i')
+        if isinstance(source, str):
+            source = [source]
+        if isinstance(cross_image, int) and 'i' not in format:
+            raise AbcpWrongParameterError('')
+        if isinstance(source, list) and not all(x in ['standard', 'common', 'common_cat'] for x in source):
+            raise AbcpWrongParameterError(
+                'Параметр "source" может содержать следующие флаги: standard, common, common_cat')
+
+        payload = generate_payload(exclude=['cross_image', 'with_original'], **locals())
+        return await self._base.request(_Methods.Client.Articles.INFO, payload)
```

### Comparing `aioabcpapi-2.0.6/aioabcpapi/ts/client.py` & `aioabcpapi-2.0.7/aioabcpapi/ts/client.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,739 +1,747 @@
-import base64
-from datetime import datetime
-from typing import Union, List, Dict
-
-import pytz
-from pyrfc3339 import generate
-
-from ..api import _Methods
-from ..base import BaseAbcp
-from ..exceptions import AbcpWrongParameterError
-from ..utils.fields_checker import check_fields
-from ..utils.payload import generate_payload
-
-
-class TsClientApi:
-    def __init__(self, base: BaseAbcp):
-        """
-        Класс содержит методы клиентского интерфейса
-
-        https://www.abcp.ru/wiki/API.TS.Client
-        """
-        self._base = base
-        self.good_receipts = GoodReceipts(base)
-        self.order_pickings = OrderPickings(base)
-        self.customer_complaints = CustomerComplaints(base)
-        self.orders = Orders(base)
-        self.cart = Cart(base)
-        self.positions = Positions(base)
-        self.agrements = Agreements(base)
-
-
-class GoodReceipts:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def create(self, code: Union[str, int],
-                     positions: Union[List[Dict[str, str]], Dict[str, str]],
-                     sup_number: str = None, sup_shipment_date: Union[str, datetime] = None):
-        """
-        Операция создания приёмки
-
-        Source:
-        :param code: Внутренний код контрагента-поставщика
-        :param positions: список словарей с позициями
-        :param sup_number: номер отгрузки поставщика
-        :param sup_shipment_date: дата и время отгрузки поставщика <br> `str` в формате %Y-%m-%d %H:%M:%S или datetime object<br>
-        :return: id `obj`
-        """
-        if isinstance(positions, dict):
-            positions = [positions]
-        payload = generate_payload(**locals())
-        if isinstance(sup_shipment_date, datetime):
-            sup_shipment_date = f'{sup_shipment_date:%Y-%m-%d %H:%M:%S}'
-        return await self._base.request(_Methods.TsClient.GoodReceipts.CREATE, payload, True)
-
-    async def get(self, limit: int = None, skip: int = None,
-                  output: str = None,
-                  auto: str = None,
-                  creator_id: Union[int, str] = None, worker_id: Union[int, str] = None,
-                  agreement_id: Union[int, str] = None, statuses: Union[List, str, int] = None,
-                  number: str = None,
-                  date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
-                  sup_number: str = None):
-        """
-        Получение списка операций приёмки
-
-        Source:
-
-        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
-        :param skip: количество операций в ответе, которое нужно пропустить
-        :param output: формат вывода, флаг 'd' - загрузка удалённых операций, 'e' - загрузка дополнительной информации (договора), 's' - суммы по позициям, кол-во позиций
-        :param auto: автоопределяемое поле (поиск по частичному номеру операции или идентификатору, если задано число)
-        :param creator_id: идентификатор сотрудника-создателя
-        :param worker_id: идентификатор сотрудника-исполнителя
-        :param agreement_id: идентификатор договора
-        :param statuses: стататус или статусы в List (Возможные значения: от 1 до 3)
-        :param number: номер операций
-        :param date_start: начальная дата диапазона поиска `str` в формате RFC3339 или datetime object
-        :param date_end: конечная дата диапазона поиска `str` в формате RFC3339 или datetime object
-        :param sup_number:
-        :return:
-        """
-        if isinstance(limit, int) and not 1 <= limit <= 1000:
-            raise AbcpWrongParameterError('Параметр "limit" может принимать значения от 1 до 1000')
-        if isinstance(date_start, datetime):
-            date_start = generate(date_start.replace(tzinfo=pytz.utc))
-        if isinstance(date_end, datetime):
-            date_end = generate(date_end.replace(tzinfo=pytz.utc))
-        if isinstance(output, str) and not all(x in 'des' for x in output):
-            raise AbcpWrongParameterError('Параметр "output" должен состоять из  ["d", "e", "s"]')
-        if isinstance(statuses, list):
-            if all(1 <= int(x) <= 3 for x in statuses):
-                statuses = ','.join(map(str, statuses))
-            else:
-                raise AbcpWrongParameterError('Параметр "statuses" принимет значения от 1 до 3')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.GoodReceipts.GET, payload)
-
-    async def get_positions(self, op_id: Union[str, int], limit: int = None, skip: int = None,
-                            output: str = None, product_id: Union[int, str] = None, auto: str = None):
-        """
-        Получение списка позиций приёмки
-
-        Source:
-
-        :param op_id: идентификатор операции
-        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
-        :param skip: количество операций в ответе, которое нужно пропустить
-        :param output: формат вывода, 'e' - загрузка дополнительной информации (справочные товары)
-        :param product_id: идентификатор товара справочника
-        :param auto:
-        :return:
-        """
-        if isinstance(limit, int) and not 1 <= limit <= 1000:
-            raise AbcpWrongParameterError('Параметр "limit" может принимать значения от 1 до 1000')
-        if isinstance(output, str) and output != 'e':
-            raise AbcpWrongParameterError('Параметр "output" принимает только значение "e"')
-        if isinstance(auto, str) and (len(auto) < 3):
-            raise AbcpWrongParameterError('Параметр "auto" должен состоять минимум из 3 символов')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.GoodReceipts.GET_POSITIONS, payload)
-
-
-class OrderPickings:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get(self, limit: int = None, skip: int = None,
-                  output: str = None, auto: Union[str, int] = None,
-                  creator_id: Union[int, str] = None, worker_id: Union[int, str] = None,
-                  agreement_id: Union[int, str] = None,
-                  status: Union[List, str, int] = None, number: str = None,
-                  date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
-                  co_old_pos_ids: Union[List, str, int] = None):
-        """
-        Получение списка операций отгрузки (расход)
-
-        Source:
-
-        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
-        :param skip: количество операций в ответе, которое нужно пропустить
-        :param output: формат вывода, флаг 'd' - загрузка удалённых операций, 'e' - загрузка дополнительной информации (договора), 's' - суммы по позициям, кол-во позиций
-        :param auto: автоопределяемое поле (поиск по частичному номеру операции или идентификатору, если задано число)
-        :param creator_id: идентификатор сотрудника-создателя
-        :param worker_id: идентификатор сотрудника-исполнителя
-        :param agreement_id: идентификатор договора
-        :param status: статус или список статусов (От 1 до 3)
-        :param number: номер операций
-        :param date_start: начальная дата диапазона поиска `str` в формате RFC3339 или datetime object
-        :param date_end: конечная дата диапазона поиска `str` в формате RFC3339 или datetime object
-        :param co_old_pos_ids: список идентификаторов позиций старых заказов
-        :return:
-        """
-        if isinstance(limit, int) and not 1 <= limit <= 1000:
-            raise AbcpWrongParameterError('Параметр "limit" может принимать значения от 1 до 1000')
-        if isinstance(date_start, datetime):
-            date_start = generate(date_start.replace(tzinfo=pytz.utc))
-        if isinstance(date_end, datetime):
-            date_end = generate(date_end.replace(tzinfo=pytz.utc))
-        if isinstance(status, int) and not 1 <= status <= 3:
-            raise AbcpWrongParameterError('Параметр "status" принимет значения от 1 до 3')
-        if isinstance(status, list):
-            if all(1 <= x <= 3 for x in status):
-                statuses = ','.join(map(str, status))
-            else:
-                raise AbcpWrongParameterError('Параметр "status" принимет значения от 1 до 3')
-        if isinstance(output, str) and (not all(x in 'des' for x in output) or len(output) > 3):
-            raise AbcpWrongParameterError('Параметр "output" должен состоять из  ["d", "e", "s"]')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.OrderPickings.GET, payload)
-
-    async def get_positions(self, op_id: Union[str, int], limit: int = None, skip: int = None, output: str = None,
-                            product_id: Union[int, str] = None,
-                            item_id: Union[int, str] = None, ignore_canceled: Union[int, bool] = None):
-        """
-        Получение списка позиций товаров отгрузки
-
-        Source:
-
-        :param op_id: идентификатор операции
-        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
-        :param skip: количество операций в ответе, которое нужно пропустить
-        :param output: формат вывода, 'e' - загрузка дополнительной информации (справочные товары), 'o' - дополнительно вернуть инфу об операции
-        :param product_id: идентификатор товара справочника
-        :param item_id: идентификатор партии товара
-        :param ignore_canceled: Признак не возвращать позиции аннулированных операций
-        :return:
-        """
-
-        if isinstance(ignore_canceled, int):
-            if ignore_canceled == 0:
-                ignore_canceled = None
-            elif ignore_canceled != 1:
-                raise AbcpWrongParameterError(
-                    'В параметр "ignore_canceled" передеаются значения 1 или True, 0 или False (В данном случае можно не указывать) ')
-
-        if isinstance(ignore_canceled, bool):
-            if ignore_canceled:
-                ignore_canceled = int(ignore_canceled)
-            else:
-                ignore_canceled = None
-
-        if isinstance(output, str) and (not all(x in 'oe' for x in output) or len(output) > 2):
-            raise AbcpWrongParameterError('Параметр "output" должен состоять из  ["o", "e"]')
-        if output is not None:
-            raise AbcpWrongParameterError('output must be a string')
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.OrderPickings.GET_POSITIONS, payload)
-
-
-class CustomerComplaints:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    class FieldsChecker:
-        get_fields = ["orderPicking", "agreement", "posInfo"]
-        get_positions_fields = ["product", "orderPickingInfo", "operationInfo", "supplierReturnPos"]
-
-    async def get(self, auto: Union[str, int] = None, creator_id: Union[int, str] = None,
-                  expert_id: Union[int, str] = None,
-                  order_picking_id: Union[int, str] = None, position_statuses: Union[List, str, int] = None,
-                  tag_ids: Union[List, str, int] = None, position_auto: str = None,
-                  number: str = None, date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
-                  skip: int = None, limit: int = None,
-                  output: str = None, fields: Union[List, str] = None):
-        # Who choose this namespacing with camelCase, snake_case, wtf case like tagIDs?
-
-        """
-        Получение списка операций возврата покупателя
-
-        Source:
-
-        :param auto: автоопределяемое поле (поиск по частичному номеру операции или идентификатору, если задано число)
-        :param creator_id: идентификатор сотрудника-создателя
-        :param expert_id: идентификатор сотрудника-эксперта
-        :param order_picking_id: идентификатор отгрузки
-        :param position_statuses: массив статусов позиций
-        :param tag_ids: массив идентификаторов тегов
-        :param position_auto: автоопределяемый параметр для поиска по позициям операции
-        :param number: номер операции
-        :param date_start: начальная дата диапазона поиска `str` в формате RFC3339 или datetime object
-        :param date_end:  конечная дата диапазона поиска `str` в формате RFC3339 или datetime object
-        :param skip: количество операций в ответе, которое нужно пропустить
-        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
-        :param output: формат вывода, 'e' - загрузка дополнительной информации(операция отгрузки и договор), 's' - будет возвращена дополнительная информация о количестве позиций во всех возможных статусах.
-        :param fields: загрузка дополнительной информации. Строка со следующими параметрами через запятую:<br><br>
-                    orderPicking - операция отгрузки, по которой создан возврат<br>
-                    agreement - договор, по которому выполнена отгрузка<br>
-                    posInfo - информация о количестве позиций во всех возможных статусах
-        :return:
-        """
-        if isinstance(date_start, datetime):
-            date_start = generate(date_start.replace(tzinfo=pytz.utc))
-        if isinstance(date_end, datetime):
-            date_end = generate(date_end.replace(tzinfo=pytz.utc))
-        if isinstance(tag_ids, (int, str)):
-            tag_ids = [tag_ids]
-        if isinstance(position_statuses, list):
-            position_statuses = ','.join(map(str, position_statuses))
-        if fields is not None:
-            fields = check_fields(fields, self.FieldsChecker.get_fields)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.CustomerComplaints.GET, payload)
-
-    async def get_positions(self, op_id: Union[str, int],
-                            order_picking_good_id: Union[int, str] = None,
-                            order_picking_good_ids: Union[List, str, int] = None,
-                            picking_ids: Union[List, str, int] = None,
-                            old_co_position_ids: Union[List, str, int] = None,
-                            old_item_id: Union[int, str] = None,
-                            item_id: Union[int, str] = None, loc_id: Union[int, str] = None,
-                            status: int = None, date_start: Union[str, datetime] = None,
-                            date_end: Union[str, datetime] = None,
-                            type: Union[str, int] = None, skip: int = None, limit: int = None,
-                            output: str = None, fields: Union[List, str] = None
-                            ):
-        """
-        Получение списка позиций возврата покупателя
-
-        Source: https://www.abcp.ru/wiki/API.TS.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B9_.D0.B2.D0.BE.D0.B7.D0.B2.D1.80.D0.B0.D1.82.D0.B0_.D0.BF.D0.BE.D0.BA.D1.83.D0.BF.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
-
-        :param op_id: идентификатор операции
-        :param order_picking_good_id: идентификатор позиции отгрузки
-        :param order_picking_good_ids: идентификаторы позиций расхода через запятую
-        :param picking_ids:  идентификаторы операции расхода через запятую
-        :param old_co_position_ids: Идентификаторы позиции заказа через запятую.
-        :param old_item_id: идентификатор партии из отгрузки
-        :param item_id: идентификатор созданной партии
-        :param loc_id: идентификатор места хранения
-        :param status:  статус позиции (1 - новый, 2 - в работе, 3 - отказ, 4 - подтверждён, 5 - выдано, 6 - аннулировано)
-        :param date_start: Начальная дата диапазона поиска `str` в формате RFC3339 или datetime object
-        :param date_end: Конечная дата диапазона поиска `str` в формате RFC3339 или datetime object
-        :param type:тип возврата (1 - возврат, 2 - отказ, 3 - брак.)
-        :param skip: количество операций в ответе, которое нужно пропустить
-        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
-        :param output:  формат вывода, 'e' - загрузка дополнительной информации (справочные товары)
-        :param fields: [необязательный] Загрузка дополнительной информации. Строка со следующими параметрами через запятую:
-                        product - товар из справочника
-                        orderPickingInfo - операция расхода; позиция расхода, связанная с возвратом; доступное для возврата количество
-                        operationInfo - информация об операции
-                        supplierReturnPos - связанный возврат поставщику (null, если такого нет)
-        :return:
-        """
-        if isinstance(order_picking_good_ids, list):
-            order_picking_good_ids = ','.join(map(str, order_picking_good_ids))
-
-        if isinstance(picking_ids, list):
-            picking_ids = ','.join(map(str, picking_ids))
-
-        if isinstance(old_co_position_ids, list):
-            old_co_position_ids = ','.join(map(str, old_co_position_ids))
-
-        if isinstance(date_start, datetime):
-            date_start = generate(date_start.replace(tzinfo=pytz.utc))
-        if isinstance(date_end, datetime):
-            date_end = generate(date_end.replace(tzinfo=pytz.utc))
-        if isinstance(status, int) and not 1 <= status <= 6:
-            raise AbcpWrongParameterError('Параметр "status" должен быть в диапазоне от 1 до 6')
-        if isinstance(type, int) and not 1 <= type <= 3:
-            raise AbcpWrongParameterError('Параметр "type" должен быть в диапазоне от 1 до 3')
-        if isinstance(output, str) and output != 'e':
-            raise AbcpWrongParameterError('Параметр "output" принимает только значение "e"')
-        if fields is not None:
-            fields = check_fields(fields, self.FieldsChecker.get_positions_fields)
-
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.CustomerComplaints.GET_POSITIONS, payload)
-
-    async def create(self, order_picking_id: Union[str, int], positions: Union[List[Dict], Dict]):
-        """
-        Создание возврата покупателя
-
-        Source:
-
-        :param order_picking_id: идентификатор отгрузки из которой возвращается товар
-        :param positions: список позиций
-        :return:
-        """
-
-        if isinstance(positions, dict):
-            positions = [positions]
-        payload = generate_payload(exclude=['positions'], **locals())
-        return await self._base.request(_Methods.TsClient.CustomerComplaints.CREATE, payload, True)
-
-    async def create_position_multiple(self, positions: Union[List[Dict], Dict],
-                                       customer_complaint_id: int,
-                                       customer_complaint: str,
-                                       custom_complaint_file: str = None):
-        with open(custom_complaint_file, "rb") as ccf:
-            encoded_string = base64.b64encode(ccf.read()).decode("utf-8")
-        custom_complaint_file = f"{encoded_string}"
-        del ccf
-        del encoded_string
-        if isinstance(positions, dict):
-            positions = [positions]
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.CustomerComplaints.CREATE_POSITION_MULTIPLE, payload, True)
-
-    async def update_position(self, id: int, quantity: Union[str, int]):
-        """
-        Изменение позиции возврата покупателя
-
-        Возможно изменение только количества товара позиции. Изменение возможно только в статусе "новый".
-
-        Source:
-
-        :param id: идентификатор позиции возврата покупателя
-        :param quantity: количество
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.CustomerComplaints.UPDATE, payload, True)
-
-    async def cancel_position(self, id: int):
-        """
-        Отмена позиции возврата покупателя
-
-        Отмена позиции возможна только в статусе "новый". Отмена позиции происходит путём изменения статуса позиции в статус 6 - аннулировано.
-
-        Source:
-
-        :param id: идентификатор позиции возврата покупателя
-
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.CustomerComplaints.CANCEL, payload, True)
-
-
-class Orders:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def create_by_cart(self, delivery_address: str, delivery_person: str, delivery_contact: str,
-                             delivery_comment: str = None, delivery_method_id: Union[int, str] = None,
-                             number: Union[str, int] = None, create_time: Union[str, datetime] = None,
-                             positions: Union[List, str, int] = None):
-        """
-
-        :param delivery_address: адрес доставки
-        :param delivery_person: контактное лицо
-        :param delivery_contact: контакт(телефон) получателя
-        :param delivery_comment: комментарий
-        :param delivery_method_id: ID способа доставки
-        :param number: номер заказа, если не указан, то сформируется согласно шаблону номеров заказов, если указан, то проверяется на уникальность
-        :param create_time: дата и время создания заказа, если не указан, заполняется автоматически, не может быть из будущего. `str` в формате RFC3339 или datetime object
-        :param positions: список ID позиций корзины
-        :return:
-        """
-        if isinstance(create_time, datetime):
-            create_time = generate(create_time.replace(tzinfo=pytz.utc))
-        if isinstance(positions, (int, str)):
-            positions = [positions]
-        payload = generate_payload(
-            exclude=['delivery_address', 'delivery_person',
-                     'delivery_contact', 'delivery_comment', 'delivery_method_id'],
-            **locals())
-        return await self._base.request(_Methods.TsClient.Orders.CREATE, payload, True)
-
-    async def get_list(self, number: Union[str, int] = None, agreement_id: Union[int, str] = None,
-                       manager_id: Union[int, str] = None,
-                       delivery_id: Union[int, str] = None, brand: str = None, message: str = None,
-                       date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
-                       update_date_start: Union[str, datetime] = None, update_date_end: Union[str, datetime] = None,
-                       deadline_date_start: Union[str, datetime] = None,
-                       deadline_date_end: Union[str, datetime] = None,
-                       order_ids: Union[List, str, int] = None,
-                       product_ids: Union[List, str, int] = None,
-                       position_statuses: Union[List, str, int] = None, limit: int = None,
-                       skip: int = None):
-        """
-
-        :param number: номер заказа
-        :param agreement_id: Идентификатор соглашения
-        :param manager_id: Идентификатор менеджера
-        :param delivery_id: Идентификатор доставки
-        :param brand: бренд товара, полное совпадение
-        :param message: комментарий к заказу или позиции заказа
-        :param date_start: начальная дата диапазона поиска по дате создания заказа(обязательное, если задан dateEnd) `str` в формате RFC3339 или datetime object
-        :param date_end: конечная дата диапазона поиска по дате создания заказа(обязательное, если задан dateStart) `str` в формате RFC3339 или datetime object
-        :param update_date_start: начальная дата диапазона поиска по дате обновления заказа `str` в формате RFC3339 или datetime object
-        :param update_date_end: конечная дата диапазона поиска по дате обновления заказа `str` в формате RFC3339 или datetime object
-        :param deadline_date_start: начальная дата диапазона поиска по дате ожидаемой поставки позиций заказа `str` в формате RFC3339 или datetime object
-        :param deadline_date_end: конечная дата диапазона поиска по дате ожидаемой поставки позиций заказа `str` в формате RFC3339 или datetime object
-        :param order_ids: Идентификаторы заказов через запятую
-        :param product_ids: Идентификаторы карточек товаров через запятую
-        :param position_statuses: статусы позиций заказов через запятую
-        :param skip: количество заказов в ответе, которое нужно пропустить
-        :param limit: максимальное количество заказов, которое должно быть возвращено в ответе
-        :return:
-        """
-        if isinstance(position_statuses, list):
-            position_statuses = ','.join(map(str, position_statuses))
-        if isinstance(product_ids, list):
-            product_ids = ','.join(map(str, product_ids))
-        if isinstance(order_ids, list):
-            order_ids = ','.join(map(str, order_ids))
-        if isinstance(date_start, datetime):
-            date_start = generate(date_start.replace(tzinfo=pytz.utc))
-        if isinstance(date_end, datetime):
-            date_end = generate(date_end.replace(tzinfo=pytz.utc))
-        if isinstance(update_date_start, datetime):
-            update_date_start = generate(update_date_start.replace(tzinfo=pytz.utc))
-        if isinstance(update_date_end, datetime):
-            update_date_end = generate(update_date_end.replace(tzinfo=pytz.utc))
-        if isinstance(deadline_date_start, datetime):
-            deadline_date_start = generate(deadline_date_start.replace(tzinfo=pytz.utc))
-        if isinstance(deadline_date_end, datetime):
-            deadline_date_end = generate(deadline_date_end.replace(tzinfo=pytz.utc))
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Orders.GET_LIST, payload)
-
-    async def get_order(self, order_id: Union[str, int]):
-        """
-        Получение одного заказа
-
-        Source:
-
-        :param order_id: Идентификатор заказа.
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Orders.GET, payload)
-
-    async def refuse(self, order_id: Union[str, int]):
-        """
-        Отказ от заказа
-
-        Source:
-
-        :param order_id:
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Orders.REFUSE, payload, True)
-
-
-class Cart:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def create(self, brand: str, number: str, quantity: int, supplier_code: Union[str, int], item_key: str,
-                     agreement_id: Union[int, str] = None):
-        """
-        Добавление позиции в корзину
-
-        Source:
-
-        :param brand: бренд
-        :param number: артикул по стандарту ABCP
-        :param quantity: количество товара
-        :param supplier_code: идентификатор маршрута прайс-листа
-        :param item_key: Код товара, полученный поиском search/articles | await api.cp.client.search.articles(602000600, 'Luk')
-        :param agreement_id: идентификатор договора, если не указан, то используется активный договор с клиентом по умолчанию
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Cart.CREATE, payload, True)
-
-    async def update(self, position_id: Union[str, int], quantity: int):
-        """
-        Обновление позиции в корзине
-
-        Source:
-
-        :param position_id: идентификатор позиции в корзине
-        :param quantity: новое количество
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Cart.UPDATE, payload, True)
-
-    async def get_list(self, position_ids: Union[List, str, int] = None, agreement_id: Union[int, str] = None,
-                       limit: int = None,
-                       skip: int = None):
-        """
-        Получение списка позиций в корзине
-
-        Source:
-        :param position_ids: Список идентификаторов позиций в корзине, через запятую
-        :param agreement_id: идентификатор договора, если не указан, то используется активный договор с клиентом по умолчанию
-        :param limit: максимальное количество позиций корзины, которое должно быть возвращено в ответе
-        :param skip: количество позиций корзины в ответе, которое нужно пропустить
-        :return:
-        """
-        if isinstance(position_ids, list):
-            position_ids = ','.join(map(str, position_ids))
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Cart.GET_LIST, payload, True)
-
-    async def exist(self, agreement_id: Union[str, int], brand: str, number_fix: str):
-        """
-        Проверка наличия позиции в корзине
-
-        Source:
-
-        :param agreement_id: идентификатор договора
-        :param brand: бренд
-        :param number_fix: артикул по стандарту ABCP
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Cart.EXIST, payload)
-
-    async def summary(self, agreement_id: Union[int, str] = None):
-        """
-        Получение суммарной информации по позициям корзины
-
-        Source:
-        :param agreement_id: идентификатор договора, если не указан, то используется активный договор с клиентом по умолчанию
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Cart.SUMMARY, payload)
-
-    async def clear(self, agreement_id: Union[str, int]):
-        """
-        Очистка корзины выбранного договора
-
-        Source:
-        :param agreement_id: идентификатор договора
-        :return:
-        """
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Cart.CLEAR, payload, True)
-
-    async def delete_positions(self, position_ids: Union[List, str, int]):
-        """
-        Удаление позиций корзины
-
-        Source:
-        :param position_ids:
-        :return:
-        """
-        if isinstance(position_ids, (int, str)):
-            position_ids = [position_ids]
-
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Cart.DELETE, payload, True)
-
-
-class Positions:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    class FieldsChecker:
-        additional_info = ["delivery", "unpaidAmount"]
-        statuses = ["prepayment", "canceled", "new",
-                    "supOrder", "supOrderCanceled", "reservation",
-                    "orderPicking", "delivery", "finished"]
-
-    async def get_position(self, position_id: Union[str, int], additional_info: Union[List, str] = None):
-        """
-
-        :param position_id: идентификатор позиции заказа
-        :param additional_info: доп. информация. Значения `str` или List ["delivery", "unpaidAmount"]
-        :return:
-        """
-        if additional_info is not None:
-            additional_info = check_fields(additional_info, self.FieldsChecker.additional_info)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Positions.GET, payload)
-
-    async def get_list(self, brand: str = None, message: str = None, agreement_id: Union[int, str] = None,
-                       manager_id: Union[int, str] = None,
-                       no_manager_assigned: bool = False,
-                       date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
-                       update_date_start: Union[str, datetime] = None, update_date_end: Union[str, datetime] = None,
-                       deadline_date_start: Union[str, datetime] = None, deadline_date_end: Union[str, datetime] = None,
-                       route_ids: Union[List, str, int] = None,
-                       distributor_ids: Union[List, str, int] = None, ids: Union[List, str, int] = None,
-                       order_ids: Union[List, str, int] = None, product_ids: Union[List, str, int] = None,
-                       statuses: Union[List, str] = None,
-                       tag_ids: Union[List, str, int] = None,
-                       limit: int = None, skip: int = None,
-                       additional_info: Union[List, str] = None):
-        """
-
-
-        :param brand:  бренд товара, полное совпадение
-        :param message: комментарий к позиции
-        :param agreement_id: идентификатор соглашения
-        :param manager_id: идентификатор менеджера
-        :param no_manager_assigned: добавляющий в выборку позиции без назначенного менеджера; используется с managerId
-        :param date_start: минимальная дата создания позиций заказов `str` в формате RFC3339 или datetime object
-        :param date_end: максимальная дата создания позиций заказов `str` в формате RFC3339 или datetime object
-        :param update_date_start: минимальная дата обновления заказов `str` в формате RFC3339 или datetime object
-        :param update_date_end: максимальная дата обновления заказов `str` в формате RFC3339 или datetime object
-        :param deadline_date_start: минимальная дата ожидаемая дата поставки на склад `str` в формате RFC3339 или datetime object
-        :param deadline_date_end: максимальная дата ожидаемая дата поставки на склад `str` в формате RFC3339 или datetime object
-        :param route_ids: идентификаторы маршрутов
-        :param distributor_ids: идентификаторы прайс-листов
-        :param ids: идентификаторы позиций заказов клиентов
-        :param order_ids: идентификаторы заказов клиентов
-        :param product_ids: идентификаторы карточек товаров через запятую
-        :param statuses: список статусов позиций заказов
-        :param tag_ids: id тегов
-        :param limit: ограничение по кол-ву заказов в выдаче
-        :param skip: смещение (по умолчанию 0)
-        :param additional_info: доп. информация. Значения `str` или List ["delivery", "unpaidAmount"]
-        :return:
-        """
-        if isinstance(date_start, datetime):
-            date_start = f'{date_start:%Y-%m-%d %H:%M:%S}'
-        if isinstance(date_end, datetime):
-            date_end = f'{date_end:%Y-%m-%d %H:%M:%S}'
-        if isinstance(update_date_start, datetime):
-            update_date_start = f'{update_date_start:%Y-%m-%d %H:%M:%S}'
-        if isinstance(update_date_end, datetime):
-            update_date_end = f'{update_date_end:%Y-%m-%d %H:%M:%S}'
-        if isinstance(deadline_date_start, datetime):
-            deadline_date_start = f'{deadline_date_start:%Y-%m-%d %H:%M:%S}'
-        if isinstance(deadline_date_end, datetime):
-            deadline_date_end = f'{deadline_date_end:%Y-%m-%d %H:%M:%S}'
-        if isinstance(product_ids, (int, str)):
-            product_ids = [product_ids]
-        if isinstance(route_ids, (int, str)):
-            route_ids = [route_ids]
-        if isinstance(distributor_ids, (int, str)):
-            distributor_ids = [distributor_ids]
-        if isinstance(ids, (int, str)):
-            ids = [ids]
-        if isinstance(order_ids, (int, str)):
-            order_ids = [order_ids]
-        if isinstance(statuses, str):
-            statuses = [statuses]
-        if isinstance(tag_ids, list):
-            tag_ids = ','.join(map(str, tag_ids))
-        if statuses is not None:
-            statuses = check_fields(statuses, self.FieldsChecker.statuses)
-        if additional_info is not None:
-            additional_info = check_fields(additional_info, self.FieldsChecker.additional_info)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Positions.GET_LIST, payload)
-
-    async def cancel(self, position_id: Union[str, int], additional_info: Union[List, str] = None):
-        """
-
-        :param position_id: идентификатор позиции заказа
-        :param additional_info: доп. информация. Значения `str` или List ["delivery", "unpaidAmount"]
-        :return:
-        """
-        if additional_info is not None:
-            additional_info = check_fields(additional_info, self.FieldsChecker.additional_info)
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Positions.CANCEL, payload, True)
-
-    async def mass_cancel(self, position_ids: Union[List, str, int], additional_info: Union[List, str] = None):
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Positions.MASS_CANCEL, payload, True)
-
-
-class Agreements:
-    def __init__(self, base: BaseAbcp):
-        self._base = base
-
-    async def get_list(self, contractor_ids: Union[int, str, List[int]] = None,
-                       contractor_requisite_ids: Union[int, str, List[int]] = None,
-                       shop_requisite_ids: Union[int, str, List[int]] = None,
-                       is_active: bool = None, is_delete: bool = None, is_default: bool = None,
-                       agreement_type: int = None, relation_type: int = None,
-                       number: str = None, currency: str = None,
-                       date_start: Union[datetime, str] = None, date_end: Union[datetime, str] = None,
-                       credit_limit: Union[float, int] = None,
-                       limit: int = None, skip: int = None):
-        if isinstance(date_start, datetime):
-            date_start = generate(date_start.replace(tzinfo=pytz.utc))
-        if isinstance(date_end, datetime):
-            date_end = generate(date_end.replace(tzinfo=pytz.utc))
-
-        if isinstance(contractor_ids, int) or isinstance(contractor_ids, str):
-            contractor_ids = [contractor_ids]
-        if isinstance(contractor_requisite_ids, int) or isinstance(contractor_requisite_ids, str):
-            contractor_requisite_ids = [contractor_requisite_ids]
-        if isinstance(shop_requisite_ids, int) or isinstance(shop_requisite_ids, str):
-            shop_requisite_ids = [shop_requisite_ids]
-
-        payload = generate_payload(**locals())
-        return await self._base.request(_Methods.TsClient.Agreements.get_list, payload)
+import base64
+from datetime import datetime
+from typing import Union, List, Dict
+
+import pytz
+from pyrfc3339 import generate
+
+from ..api import _Methods
+from ..base import BaseAbcp
+from ..exceptions import AbcpWrongParameterError
+from ..utils.fields_checker import check_fields
+from ..utils.payload import generate_payload
+
+
+class TsClientApi:
+    def __init__(self, base: BaseAbcp):
+        """
+        Класс содержит методы клиентского интерфейса
+
+        https://www.abcp.ru/wiki/API.TS.Client
+        """
+        self._base = base
+        self.good_receipts = GoodReceipts(base)
+        self.order_pickings = OrderPickings(base)
+        self.customer_complaints = CustomerComplaints(base)
+        self.orders = Orders(base)
+        self.cart = Cart(base)
+        self.positions = Positions(base)
+        self.agrements = Agreements(base)
+
+
+class GoodReceipts:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def create(self, code: Union[str, int],
+                     positions: Union[List[Dict[str, str]], Dict[str, str]],
+                     sup_number: str = None, sup_shipment_date: Union[str, datetime] = None):
+        """
+        Операция создания приёмки
+
+        Source:
+        :param code: Внутренний код контрагента-поставщика
+        :param positions: список словарей с позициями
+        :param sup_number: номер отгрузки поставщика
+        :param sup_shipment_date: дата и время отгрузки поставщика <br> `str` в формате %Y-%m-%d %H:%M:%S или datetime object<br>
+        :return: id `obj`
+        """
+        if isinstance(positions, dict):
+            positions = [positions]
+        payload = generate_payload(**locals())
+        if isinstance(sup_shipment_date, datetime):
+            sup_shipment_date = f'{sup_shipment_date:%Y-%m-%d %H:%M:%S}'
+        return await self._base.request(_Methods.TsClient.GoodReceipts.CREATE, payload, True)
+
+    async def get(self, limit: int = None, skip: int = None,
+                  output: str = None,
+                  auto: str = None,
+                  creator_id: Union[int, str] = None, worker_id: Union[int, str] = None,
+                  agreement_id: Union[int, str] = None, statuses: Union[List, str, int] = None,
+                  number: str = None,
+                  date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
+                  sup_number: str = None):
+        """
+        Получение списка операций приёмки
+
+        Source:
+
+        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
+        :param skip: количество операций в ответе, которое нужно пропустить
+        :param output: формат вывода, флаг 'd' - загрузка удалённых операций, 'e' - загрузка дополнительной информации (договора), 's' - суммы по позициям, кол-во позиций
+        :param auto: автоопределяемое поле (поиск по частичному номеру операции или идентификатору, если задано число)
+        :param creator_id: идентификатор сотрудника-создателя
+        :param worker_id: идентификатор сотрудника-исполнителя
+        :param agreement_id: идентификатор договора
+        :param statuses: стататус или статусы в List (Возможные значения: от 1 до 3)
+        :param number: номер операций
+        :param date_start: начальная дата диапазона поиска `str` в формате RFC3339 или datetime object
+        :param date_end: конечная дата диапазона поиска `str` в формате RFC3339 или datetime object
+        :param sup_number:
+        :return:
+        """
+        if isinstance(limit, int) and not 1 <= limit <= 1000:
+            raise AbcpWrongParameterError('Параметр "limit" может принимать значения от 1 до 1000')
+        if isinstance(date_start, datetime):
+            date_start = generate(date_start.replace(tzinfo=pytz.utc))
+        if isinstance(date_end, datetime):
+            date_end = generate(date_end.replace(tzinfo=pytz.utc))
+        if isinstance(output, str) and not all(x in 'des' for x in output):
+            raise AbcpWrongParameterError('Параметр "output" должен состоять из  ["d", "e", "s"]')
+        if isinstance(statuses, list):
+            if all(1 <= int(x) <= 3 for x in statuses):
+                statuses = ','.join(map(str, statuses))
+            else:
+                raise AbcpWrongParameterError('Параметр "statuses" принимет значения от 1 до 3')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.GoodReceipts.GET, payload)
+
+    async def get_positions(self, op_id: Union[str, int], limit: int = None, skip: int = None,
+                            output: str = None, product_id: Union[int, str] = None, auto: str = None):
+        """
+        Получение списка позиций приёмки
+
+        Source:
+
+        :param op_id: идентификатор операции
+        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
+        :param skip: количество операций в ответе, которое нужно пропустить
+        :param output: формат вывода, 'e' - загрузка дополнительной информации (справочные товары)
+        :param product_id: идентификатор товара справочника
+        :param auto:
+        :return:
+        """
+        if isinstance(limit, int) and not 1 <= limit <= 1000:
+            raise AbcpWrongParameterError('Параметр "limit" может принимать значения от 1 до 1000')
+        if isinstance(output, str) and output != 'e':
+            raise AbcpWrongParameterError('Параметр "output" принимает только значение "e"')
+        if isinstance(auto, str) and (len(auto) < 3):
+            raise AbcpWrongParameterError('Параметр "auto" должен состоять минимум из 3 символов')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.GoodReceipts.GET_POSITIONS, payload)
+
+
+class OrderPickings:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get(self, limit: int = None, skip: int = None,
+                  output: str = None, auto: Union[str, int] = None,
+                  creator_id: Union[int, str] = None, worker_id: Union[int, str] = None,
+                  agreement_id: Union[int, str] = None,
+                  status: Union[List, str, int] = None, number: str = None,
+                  date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
+                  co_old_pos_ids: Union[List, str, int] = None):
+        """
+        Получение списка операций отгрузки (расход)
+
+        Source:
+
+        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
+        :param skip: количество операций в ответе, которое нужно пропустить
+        :param output: формат вывода, флаг 'd' - загрузка удалённых операций, 'e' - загрузка дополнительной информации (договора), 's' - суммы по позициям, кол-во позиций
+        :param auto: автоопределяемое поле (поиск по частичному номеру операции или идентификатору, если задано число)
+        :param creator_id: идентификатор сотрудника-создателя
+        :param worker_id: идентификатор сотрудника-исполнителя
+        :param agreement_id: идентификатор договора
+        :param status: статус или список статусов (От 1 до 3)
+        :param number: номер операций
+        :param date_start: начальная дата диапазона поиска `str` в формате RFC3339 или datetime object
+        :param date_end: конечная дата диапазона поиска `str` в формате RFC3339 или datetime object
+        :param co_old_pos_ids: список идентификаторов позиций старых заказов
+        :return:
+        """
+        if isinstance(limit, int) and not 1 <= limit <= 1000:
+            raise AbcpWrongParameterError('Параметр "limit" может принимать значения от 1 до 1000')
+        if isinstance(date_start, datetime):
+            date_start = generate(date_start.replace(tzinfo=pytz.utc))
+        if isinstance(date_end, datetime):
+            date_end = generate(date_end.replace(tzinfo=pytz.utc))
+        if isinstance(status, int) and not 1 <= status <= 3:
+            raise AbcpWrongParameterError('Параметр "status" принимет значения от 1 до 3')
+        if isinstance(status, list):
+            if all(1 <= x <= 3 for x in status):
+                statuses = ','.join(map(str, status))
+            else:
+                raise AbcpWrongParameterError('Параметр "status" принимет значения от 1 до 3')
+        if isinstance(output, str) and (not all(x in 'des' for x in output) or len(output) > 3):
+            raise AbcpWrongParameterError('Параметр "output" должен состоять из  ["d", "e", "s"]')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.OrderPickings.GET, payload)
+
+    async def get_positions(self, op_id: Union[str, int], limit: int = None, skip: int = None, output: str = None,
+                            product_id: Union[int, str] = None,
+                            item_id: Union[int, str] = None, ignore_canceled: Union[int, bool] = None):
+        """
+        Получение списка позиций товаров отгрузки
+
+        Source:
+
+        :param op_id: идентификатор операции
+        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
+        :param skip: количество операций в ответе, которое нужно пропустить
+        :param output: формат вывода, 'e' - загрузка дополнительной информации (справочные товары), 'o' - дополнительно вернуть инфу об операции
+        :param product_id: идентификатор товара справочника
+        :param item_id: идентификатор партии товара
+        :param ignore_canceled: Признак не возвращать позиции аннулированных операций
+        :return:
+        """
+
+        if isinstance(ignore_canceled, int):
+            if ignore_canceled == 0:
+                ignore_canceled = None
+            elif ignore_canceled != 1:
+                raise AbcpWrongParameterError(
+                    'В параметр "ignore_canceled" передеаются значения 1 или True, 0 или False (В данном случае можно не указывать) ')
+
+        if isinstance(ignore_canceled, bool):
+            if ignore_canceled:
+                ignore_canceled = int(ignore_canceled)
+            else:
+                ignore_canceled = None
+
+        if isinstance(output, str) and (not all(x in 'oe' for x in output) or len(output) > 2):
+            raise AbcpWrongParameterError('Параметр "output" должен состоять из  ["o", "e"]')
+        if output is not None:
+            raise AbcpWrongParameterError('output must be a string')
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.OrderPickings.GET_POSITIONS, payload)
+
+
+class CustomerComplaints:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    class FieldsChecker:
+        get_fields = ["orderPicking", "agreement", "posInfo"]
+        get_positions_fields = ["product", "orderPickingInfo", "operationInfo", "supplierReturnPos"]
+
+    async def get(self, auto: Union[str, int] = None, creator_id: Union[int, str] = None,
+                  expert_id: Union[int, str] = None,
+                  order_picking_id: Union[int, str] = None, position_statuses: Union[List, str, int] = None,
+                  tag_ids: Union[List, str, int] = None, position_auto: str = None,
+                  number: str = None, date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
+                  skip: int = None, limit: int = None,
+                  output: str = None, fields: Union[List, str] = None):
+        # Who choose this namespacing with camelCase, snake_case, wtf case like tagIDs?
+
+        """
+        Получение списка операций возврата покупателя
+
+        Source:
+
+        :param auto: автоопределяемое поле (поиск по частичному номеру операции или идентификатору, если задано число)
+        :param creator_id: идентификатор сотрудника-создателя
+        :param expert_id: идентификатор сотрудника-эксперта
+        :param order_picking_id: идентификатор отгрузки
+        :param position_statuses: массив статусов позиций
+        :param tag_ids: массив идентификаторов тегов
+        :param position_auto: автоопределяемый параметр для поиска по позициям операции
+        :param number: номер операции
+        :param date_start: начальная дата диапазона поиска `str` в формате RFC3339 или datetime object
+        :param date_end:  конечная дата диапазона поиска `str` в формате RFC3339 или datetime object
+        :param skip: количество операций в ответе, которое нужно пропустить
+        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
+        :param output: формат вывода, 'e' - загрузка дополнительной информации(операция отгрузки и договор), 's' - будет возвращена дополнительная информация о количестве позиций во всех возможных статусах.
+        :param fields: загрузка дополнительной информации. Строка со следующими параметрами через запятую:<br><br>
+                    orderPicking - операция отгрузки, по которой создан возврат<br>
+                    agreement - договор, по которому выполнена отгрузка<br>
+                    posInfo - информация о количестве позиций во всех возможных статусах
+        :return:
+        """
+        if isinstance(date_start, datetime):
+            date_start = generate(date_start.replace(tzinfo=pytz.utc))
+        if isinstance(date_end, datetime):
+            date_end = generate(date_end.replace(tzinfo=pytz.utc))
+        if isinstance(tag_ids, (int, str)):
+            tag_ids = [tag_ids]
+        if isinstance(position_statuses, list):
+            position_statuses = ','.join(map(str, position_statuses))
+        if fields is not None:
+            fields = check_fields(fields, self.FieldsChecker.get_fields)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.CustomerComplaints.GET, payload)
+
+    async def get_positions(self, op_id: Union[str, int],
+                            order_picking_good_id: Union[int, str] = None,
+                            order_picking_good_ids: Union[List, str, int] = None,
+                            picking_ids: Union[List, str, int] = None,
+                            old_co_position_ids: Union[List, str, int] = None,
+                            old_item_id: Union[int, str] = None,
+                            item_id: Union[int, str] = None, loc_id: Union[int, str] = None,
+                            status: int = None, date_start: Union[str, datetime] = None,
+                            date_end: Union[str, datetime] = None,
+                            type: Union[str, int] = None, skip: int = None, limit: int = None,
+                            output: str = None, fields: Union[List, str] = None
+                            ):
+        """
+        Получение списка позиций возврата покупателя
+
+        Source: https://www.abcp.ru/wiki/API.TS.Client#.D0.9F.D0.BE.D0.BB.D1.83.D1.87.D0.B5.D0.BD.D0.B8.D0.B5_.D1.81.D0.BF.D0.B8.D1.81.D0.BA.D0.B0_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B9_.D0.B2.D0.BE.D0.B7.D0.B2.D1.80.D0.B0.D1.82.D0.B0_.D0.BF.D0.BE.D0.BA.D1.83.D0.BF.D0.B0.D1.82.D0.B5.D0.BB.D1.8F
+
+        :param op_id: идентификатор операции
+        :param order_picking_good_id: идентификатор позиции отгрузки
+        :param order_picking_good_ids: идентификаторы позиций расхода через запятую
+        :param picking_ids:  идентификаторы операции расхода через запятую
+        :param old_co_position_ids: Идентификаторы позиции заказа через запятую.
+        :param old_item_id: идентификатор партии из отгрузки
+        :param item_id: идентификатор созданной партии
+        :param loc_id: идентификатор места хранения
+        :param status:  статус позиции (1 - новый, 2 - в работе, 3 - отказ, 4 - подтверждён, 5 - выдано, 6 - аннулировано)
+        :param date_start: Начальная дата диапазона поиска `str` в формате RFC3339 или datetime object
+        :param date_end: Конечная дата диапазона поиска `str` в формате RFC3339 или datetime object
+        :param type:тип возврата (1 - возврат, 2 - отказ, 3 - брак.)
+        :param skip: количество операций в ответе, которое нужно пропустить
+        :param limit: максимальное количество операций, которое должно быть возвращено в ответе. Максимально возможное значение 1000. Если не указан будет установлено максимально возможное значение.
+        :param output:  формат вывода, 'e' - загрузка дополнительной информации (справочные товары)
+        :param fields: [необязательный] Загрузка дополнительной информации. Строка со следующими параметрами через запятую:
+                        product - товар из справочника
+                        orderPickingInfo - операция расхода; позиция расхода, связанная с возвратом; доступное для возврата количество
+                        operationInfo - информация об операции
+                        supplierReturnPos - связанный возврат поставщику (null, если такого нет)
+        :return:
+        """
+        if isinstance(order_picking_good_ids, list):
+            order_picking_good_ids = ','.join(map(str, order_picking_good_ids))
+
+        if isinstance(picking_ids, list):
+            picking_ids = ','.join(map(str, picking_ids))
+
+        if isinstance(old_co_position_ids, list):
+            old_co_position_ids = ','.join(map(str, old_co_position_ids))
+
+        if isinstance(date_start, datetime):
+            date_start = generate(date_start.replace(tzinfo=pytz.utc))
+        if isinstance(date_end, datetime):
+            date_end = generate(date_end.replace(tzinfo=pytz.utc))
+        if isinstance(status, int) and not 1 <= status <= 6:
+            raise AbcpWrongParameterError('Параметр "status" должен быть в диапазоне от 1 до 6')
+        if isinstance(type, int) and not 1 <= type <= 3:
+            raise AbcpWrongParameterError('Параметр "type" должен быть в диапазоне от 1 до 3')
+        if isinstance(output, str) and output != 'e':
+            raise AbcpWrongParameterError('Параметр "output" принимает только значение "e"')
+        if fields is not None:
+            fields = check_fields(fields, self.FieldsChecker.get_positions_fields)
+
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.CustomerComplaints.GET_POSITIONS, payload)
+
+    async def create(self, order_picking_id: Union[str, int], positions: Union[List[Dict], Dict]):
+        """
+        Создание возврата покупателя
+
+        Source:
+
+        :param order_picking_id: идентификатор отгрузки из которой возвращается товар
+        :param positions: список позиций
+        :return:
+        """
+
+        if isinstance(positions, dict):
+            positions = [positions]
+        payload = generate_payload(exclude=['positions'], **locals())
+        return await self._base.request(_Methods.TsClient.CustomerComplaints.CREATE, payload, True)
+
+    async def create_position_multiple(self, positions: Union[List[Dict], Dict],
+                                       customer_complaint_id: int,
+                                       customer_complaint: str,
+                                       custom_complaint_file: str = None):
+        with open(custom_complaint_file, "rb") as ccf:
+            encoded_string = base64.b64encode(ccf.read()).decode("utf-8")
+        custom_complaint_file = f"{encoded_string}"
+        del ccf
+        del encoded_string
+        if isinstance(positions, dict):
+            positions = [positions]
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.CustomerComplaints.CREATE_POSITION_MULTIPLE, payload, True)
+
+    async def update_position(self, id: int, quantity: Union[str, int]):
+        """
+        Изменение позиции возврата покупателя
+
+        Возможно изменение только количества товара позиции. Изменение возможно только в статусе "новый".
+
+        Source:
+
+        :param id: идентификатор позиции возврата покупателя
+        :param quantity: количество
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.CustomerComplaints.UPDATE, payload, True)
+
+    async def cancel_position(self, id: int):
+        """
+        Отмена позиции возврата покупателя
+
+        Отмена позиции возможна только в статусе "новый". Отмена позиции происходит путём изменения статуса позиции в статус 6 - аннулировано.
+
+        Source:
+
+        :param id: идентификатор позиции возврата покупателя
+
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.CustomerComplaints.CANCEL, payload, True)
+
+
+class Orders:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def create_by_cart(self, delivery_address: str, delivery_person: str, delivery_contact: str,
+                             delivery_comment: str = None, delivery_method_id: Union[int, str] = None,
+                             number: Union[str, int] = None, create_time: Union[str, datetime] = None,
+                             positions: Union[List, str, int] = None):
+        """
+
+        :param delivery_address: адрес доставки
+        :param delivery_person: контактное лицо
+        :param delivery_contact: контакт(телефон) получателя
+        :param delivery_comment: комментарий
+        :param delivery_method_id: ID способа доставки
+        :param number: номер заказа, если не указан, то сформируется согласно шаблону номеров заказов, если указан, то проверяется на уникальность
+        :param create_time: дата и время создания заказа, если не указан, заполняется автоматически, не может быть из будущего. `str` в формате RFC3339 или datetime object
+        :param positions: список ID позиций корзины
+        :return:
+        """
+        if isinstance(create_time, datetime):
+            create_time = generate(create_time.replace(tzinfo=pytz.utc))
+        if isinstance(positions, (int, str)):
+            positions = [positions]
+        payload = generate_payload(
+            exclude=['delivery_address', 'delivery_person',
+                     'delivery_contact', 'delivery_comment', 'delivery_method_id'],
+            **locals())
+        return await self._base.request(_Methods.TsClient.Orders.CREATE, payload, True)
+
+    async def get_list(self, number: Union[str, int] = None, agreement_id: Union[int, str] = None,
+                       manager_id: Union[int, str] = None,
+                       delivery_id: Union[int, str] = None, brand: str = None, message: str = None,
+                       date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
+                       update_date_start: Union[str, datetime] = None, update_date_end: Union[str, datetime] = None,
+                       deadline_date_start: Union[str, datetime] = None,
+                       deadline_date_end: Union[str, datetime] = None,
+                       order_ids: Union[List, str, int] = None,
+                       product_ids: Union[List, str, int] = None,
+                       position_statuses: Union[List, str, int] = None, limit: int = None,
+                       skip: int = None):
+        """
+
+        :param number: номер заказа
+        :param agreement_id: Идентификатор соглашения
+        :param manager_id: Идентификатор менеджера
+        :param delivery_id: Идентификатор доставки
+        :param brand: бренд товара, полное совпадение
+        :param message: комментарий к заказу или позиции заказа
+        :param date_start: начальная дата диапазона поиска по дате создания заказа(обязательное, если задан dateEnd) `str` в формате RFC3339 или datetime object
+        :param date_end: конечная дата диапазона поиска по дате создания заказа(обязательное, если задан dateStart) `str` в формате RFC3339 или datetime object
+        :param update_date_start: начальная дата диапазона поиска по дате обновления заказа `str` в формате RFC3339 или datetime object
+        :param update_date_end: конечная дата диапазона поиска по дате обновления заказа `str` в формате RFC3339 или datetime object
+        :param deadline_date_start: начальная дата диапазона поиска по дате ожидаемой поставки позиций заказа `str` в формате RFC3339 или datetime object
+        :param deadline_date_end: конечная дата диапазона поиска по дате ожидаемой поставки позиций заказа `str` в формате RFC3339 или datetime object
+        :param order_ids: Идентификаторы заказов через запятую
+        :param product_ids: Идентификаторы карточек товаров через запятую
+        :param position_statuses: статусы позиций заказов через запятую
+        :param skip: количество заказов в ответе, которое нужно пропустить
+        :param limit: максимальное количество заказов, которое должно быть возвращено в ответе
+        :return:
+        """
+        if isinstance(position_statuses, list):
+            position_statuses = ','.join(map(str, position_statuses))
+        if isinstance(product_ids, list):
+            product_ids = ','.join(map(str, product_ids))
+        if isinstance(order_ids, list):
+            order_ids = ','.join(map(str, order_ids))
+        if isinstance(date_start, datetime):
+            date_start = generate(date_start.replace(tzinfo=pytz.utc))
+        if isinstance(date_end, datetime):
+            date_end = generate(date_end.replace(tzinfo=pytz.utc))
+        if isinstance(update_date_start, datetime):
+            update_date_start = generate(update_date_start.replace(tzinfo=pytz.utc))
+        if isinstance(update_date_end, datetime):
+            update_date_end = generate(update_date_end.replace(tzinfo=pytz.utc))
+        if isinstance(deadline_date_start, datetime):
+            deadline_date_start = generate(deadline_date_start.replace(tzinfo=pytz.utc))
+        if isinstance(deadline_date_end, datetime):
+            deadline_date_end = generate(deadline_date_end.replace(tzinfo=pytz.utc))
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Orders.GET_LIST, payload)
+
+    async def get_order(self, order_id: Union[str, int]):
+        """
+        Получение одного заказа
+
+        Source:
+
+        :param order_id: Идентификатор заказа.
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Orders.GET, payload)
+
+    async def refuse(self, order_id: Union[str, int]):
+        """
+        Отказ от заказа
+
+        Source:
+
+        :param order_id:
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Orders.REFUSE, payload, True)
+
+
+class Cart:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def create(self, brand: str, number: str, quantity: int, supplier_code: Union[str, int], item_key: str,
+                     agreement_id: Union[int, str] = None):
+        """
+        Добавление позиции в корзину
+
+        Source:
+
+        :param brand: бренд
+        :param number: артикул по стандарту ABCP
+        :param quantity: количество товара
+        :param supplier_code: идентификатор маршрута прайс-листа
+        :param item_key: Код товара, полученный поиском search/articles | await api.cp.client.search.articles(602000600, 'Luk')
+        :param agreement_id: идентификатор договора, если не указан, то используется активный договор с клиентом по умолчанию
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Cart.CREATE, payload, True)
+
+    async def update(self, position_id: Union[str, int], quantity: int):
+        """
+        Обновление позиции в корзине
+
+        Source:
+
+        :param position_id: идентификатор позиции в корзине
+        :param quantity: новое количество
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Cart.UPDATE, payload, True)
+
+    async def get_list(self, position_ids: Union[List, str, int] = None, agreement_id: Union[int, str] = None,
+                       limit: int = None,
+                       skip: int = None):
+        """
+        Получение списка позиций в корзине
+
+        Source:
+        :param position_ids: Список идентификаторов позиций в корзине, через запятую
+        :param agreement_id: идентификатор договора, если не указан, то используется активный договор с клиентом по умолчанию
+        :param limit: максимальное количество позиций корзины, которое должно быть возвращено в ответе
+        :param skip: количество позиций корзины в ответе, которое нужно пропустить
+        :return:
+        """
+        if isinstance(position_ids, list):
+            position_ids = ','.join(map(str, position_ids))
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Cart.GET_LIST, payload, True)
+
+    async def exist(self, agreement_id: Union[str, int], brand: str, number_fix: str):
+        """
+        Проверка наличия позиции в корзине
+
+        Source:
+
+        :param agreement_id: идентификатор договора
+        :param brand: бренд
+        :param number_fix: артикул по стандарту ABCP
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Cart.EXIST, payload)
+
+    async def summary(self, agreement_id: Union[int, str] = None):
+        """
+        Получение суммарной информации по позициям корзины
+
+        Source:
+        :param agreement_id: идентификатор договора, если не указан, то используется активный договор с клиентом по умолчанию
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Cart.SUMMARY, payload)
+
+    async def clear(self, agreement_id: Union[str, int]):
+        """
+        Очистка корзины выбранного договора
+
+        Source:
+        :param agreement_id: идентификатор договора
+        :return:
+        """
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Cart.CLEAR, payload, True)
+
+    async def delete_positions(self, position_ids: Union[List, str, int]):
+        """
+        Удаление позиций корзины
+
+        Source:
+        :param position_ids:
+        :return:
+        """
+        if isinstance(position_ids, (int, str)):
+            position_ids = [position_ids]
+
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Cart.DELETE, payload, True)
+
+
+class Positions:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    class FieldsChecker:
+        additional_info = ["delivery", "unpaidAmount"]
+        statuses = ["prepayment", "canceled", "new",
+                    "supOrder", "supOrderCanceled", "reservation",
+                    "orderPicking", "delivery", "finished"]
+
+    async def get_position(self, position_id: Union[str, int], additional_info: Union[List, str] = None):
+        """
+
+        :param position_id: идентификатор позиции заказа
+        :param additional_info: доп. информация. Значения `str` или List ["delivery", "unpaidAmount"]
+        :return:
+        """
+        if additional_info is not None:
+            additional_info = check_fields(additional_info, self.FieldsChecker.additional_info)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Positions.GET, payload)
+
+    async def get_list(self, brand: str = None, message: str = None, agreement_id: Union[int, str] = None,
+                       manager_id: Union[int, str] = None,
+                       no_manager_assigned: bool = False,
+                       date_start: Union[str, datetime] = None, date_end: Union[str, datetime] = None,
+                       update_date_start: Union[str, datetime] = None, update_date_end: Union[str, datetime] = None,
+                       deadline_date_start: Union[str, datetime] = None, deadline_date_end: Union[str, datetime] = None,
+                       route_ids: Union[List, str, int] = None,
+                       distributor_ids: Union[List, str, int] = None, ids: Union[List, str, int] = None,
+                       order_ids: Union[List, str, int] = None, product_ids: Union[List, str, int] = None,
+                       statuses: Union[List, str] = None,
+                       tag_ids: Union[List, str, int] = None,
+                       limit: int = None, skip: int = None,
+                       additional_info: Union[List, str] = None):
+        """
+
+
+        :param brand:  бренд товара, полное совпадение
+        :param message: комментарий к позиции
+        :param agreement_id: идентификатор соглашения
+        :param manager_id: идентификатор менеджера
+        :param no_manager_assigned: добавляющий в выборку позиции без назначенного менеджера; используется с managerId
+        :param date_start: минимальная дата создания позиций заказов `str` в формате RFC3339 или datetime object
+        :param date_end: максимальная дата создания позиций заказов `str` в формате RFC3339 или datetime object
+        :param update_date_start: минимальная дата обновления заказов `str` в формате RFC3339 или datetime object
+        :param update_date_end: максимальная дата обновления заказов `str` в формате RFC3339 или datetime object
+        :param deadline_date_start: минимальная дата ожидаемая дата поставки на склад `str` в формате RFC3339 или datetime object
+        :param deadline_date_end: максимальная дата ожидаемая дата поставки на склад `str` в формате RFC3339 или datetime object
+        :param route_ids: идентификаторы маршрутов
+        :param distributor_ids: идентификаторы прайс-листов
+        :param ids: идентификаторы позиций заказов клиентов
+        :param order_ids: идентификаторы заказов клиентов
+        :param product_ids: идентификаторы карточек товаров через запятую
+        :param statuses: список статусов позиций заказов
+        :param tag_ids: id тегов
+        :param limit: ограничение по кол-ву заказов в выдаче
+        :param skip: смещение (по умолчанию 0)
+        :param additional_info: доп. информация. Значения `str` или List ["delivery", "unpaidAmount"]
+        :return:
+        """
+        if isinstance(date_start, datetime):
+            date_start = f'{date_start:%Y-%m-%d %H:%M:%S}'
+        if isinstance(date_end, datetime):
+            date_end = f'{date_end:%Y-%m-%d %H:%M:%S}'
+        if isinstance(update_date_start, datetime):
+            update_date_start = f'{update_date_start:%Y-%m-%d %H:%M:%S}'
+        if isinstance(update_date_end, datetime):
+            update_date_end = f'{update_date_end:%Y-%m-%d %H:%M:%S}'
+        if isinstance(deadline_date_start, datetime):
+            deadline_date_start = f'{deadline_date_start:%Y-%m-%d %H:%M:%S}'
+        if isinstance(deadline_date_end, datetime):
+            deadline_date_end = f'{deadline_date_end:%Y-%m-%d %H:%M:%S}'
+        if isinstance(product_ids, (int, str)):
+            product_ids = [product_ids]
+        if isinstance(route_ids, (int, str)):
+            route_ids = [route_ids]
+        if isinstance(distributor_ids, (int, str)):
+            distributor_ids = [distributor_ids]
+        if isinstance(ids, (int, str)):
+            ids = [ids]
+        if isinstance(order_ids, (int, str)):
+            order_ids = [order_ids]
+        if isinstance(statuses, str):
+            statuses = [statuses]
+        if isinstance(tag_ids, list):
+            tag_ids = ','.join(map(str, tag_ids))
+        if statuses is not None:
+            statuses = check_fields(statuses, self.FieldsChecker.statuses)
+        if additional_info is not None:
+            additional_info = check_fields(additional_info, self.FieldsChecker.additional_info)
+        if isinstance(no_manager_assigned, bool):
+            no_manager_assigned = str(no_manager_assigned)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Positions.GET_LIST, payload)
+
+    async def cancel(self, position_id: Union[str, int], additional_info: Union[List, str] = None):
+        """
+
+        :param position_id: идентификатор позиции заказа
+        :param additional_info: доп. информация. Значения `str` или List ["delivery", "unpaidAmount"]
+        :return:
+        """
+        if additional_info is not None:
+            additional_info = check_fields(additional_info, self.FieldsChecker.additional_info)
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Positions.CANCEL, payload, True)
+
+    async def mass_cancel(self, position_ids: Union[List, str, int], additional_info: Union[List, str] = None):
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Positions.MASS_CANCEL, payload, True)
+
+
+class Agreements:
+    def __init__(self, base: BaseAbcp):
+        self._base = base
+
+    async def get_list(self, contractor_ids: Union[int, str, List[int]] = None,
+                       contractor_requisite_ids: Union[int, str, List[int]] = None,
+                       shop_requisite_ids: Union[int, str, List[int]] = None,
+                       is_active: bool = None, is_delete: bool = None, is_default: bool = None,
+                       agreement_type: int = None, relation_type: int = None,
+                       number: str = None, currency: str = None,
+                       date_start: Union[datetime, str] = None, date_end: Union[datetime, str] = None,
+                       credit_limit: Union[float, int] = None,
+                       limit: int = None, skip: int = None):
+        if isinstance(date_start, datetime):
+            date_start = generate(date_start.replace(tzinfo=pytz.utc))
+        if isinstance(date_end, datetime):
+            date_end = generate(date_end.replace(tzinfo=pytz.utc))
+
+        if isinstance(contractor_ids, int) or isinstance(contractor_ids, str):
+            contractor_ids = [contractor_ids]
+        if isinstance(contractor_requisite_ids, int) or isinstance(contractor_requisite_ids, str):
+            contractor_requisite_ids = [contractor_requisite_ids]
+        if isinstance(shop_requisite_ids, int) or isinstance(shop_requisite_ids, str):
+            shop_requisite_ids = [shop_requisite_ids]
+        if isinstance(is_active, bool):
+            is_active = str(is_active)
+        if isinstance(is_delete, bool):
+            is_delete = str(is_delete)
+        if isinstance(is_default, bool):
+            is_default = str(is_default)
+
+        payload = generate_payload(**locals())
+        return await self._base.request(_Methods.TsClient.Agreements.get_list, payload)
```

### Comparing `aioabcpapi-2.0.6/aioabcpapi/utils/payload.py` & `aioabcpapi-2.0.7/aioabcpapi/utils/payload.py`

 * *Ordering differences only*

 * *Files 18% similar despite different names*

```diff
@@ -1,224 +1,224 @@
-import logging
-import os
-from io import BufferedReader
-
-from aiohttp import FormData
-
-from aioabcpapi.exceptions import FileSizeExceeded
-
-DEFAULT_FILTER = ['self', 'cls', 'kwargs']
-logger = logging.getLogger('utils/payload')
-
-
-def get_pascal_case_key(key: str):
-    return ''.join([*map(str.title, key.split('_'))])
-
-
-def get_camel_case_key(key: str):
-    return f"{''.join([key.split('_')[0].lower(), *map(str.title, key.split('_')[1:])])}"
-
-
-def get_excluded_keys(key: str):
-    excluded_keys = {
-        'order_positions': 'order[positions][_index_][_key_]',
-        'positions': 'positions[_index_][_key_]',
-        'articles_catalog': 'articles[_index_][_key_]',
-        'properties': 'properties[_key_][_index_]',
-        'order_params': 'orderParams[_key_]',
-        'distributors': 'distributors[_index_][_key_]',
-        'search': 'search[_index_][_key_]',
-        'basket_positions': 'positions[_index_][_key_]',
-        'goods_group': 'goods_group',
-        'note': 'order[notes][0][value]',
-        'del_note': 'order[notes][0][value]',
-        'delivery_address': 'delivery[meetData][address]',
-        'delivery_person': 'delivery[meetData][person]',
-        'delivery_contact': 'delivery[meetData][contact]',
-        'delivery_comment': 'delivery[meetData][comment]',
-        'delivery_employee_contact': 'delivery[meetData][employeeContact]',
-        'delivery_employee_person': 'delivery[meetData][employeePerson]',
-        'delivery_reseller_comment': 'delivery[meetData][resellerComment]',
-        'delivery_start_time': 'delivery[timeInterval][startTime]',
-        'delivery_end_time': 'delivery[timeInterval][endTime]',
-        'delivery_method_id': 'delivery[methodId]',
-        'client_order_number': 'clientOrderNumber',
-        'cross_image': 'cross_image',
-        'with_original': 'with_original',
-        'old_item_id': 'oldItemID',
-        'distributors_price_ups': 'distributorsPriceUps[_index_]',
-        'matrix_price_ups': 'matrixPriceUps[_index_]',
-    }
-    try:
-        return excluded_keys[key]
-    except KeyError:
-        return get_pascal_case_key(key)
-
-
-def generate_payload(exclude=None, order: bool = False, **kwargs):
-    """
-    Generate payload
-    :param exclude:
-    :param order: Generate dict for create or edit order
-    :param kwargs:
-    :return: dict
-    """
-    if exclude is None:
-        exclude = ['order_params', 'distributors', 'note', 'del_note',
-                   'basket_positions', 'sip']
-    data = {}
-
-    for key, value in kwargs.items():
-        if key not in exclude + DEFAULT_FILTER and value is not None and not key.startswith('_'):
-            if not order:
-                if isinstance(value, list):
-                    for i, x in enumerate(value):
-                        data[f"{get_camel_case_key(key)}[{i}]"] = x
-                else:
-                    data[get_camel_case_key(key)] = value
-            else:
-                data[f"order[{get_camel_case_key(key)}]"] = value
-        if key in exclude and key not in DEFAULT_FILTER and value is not None:
-            if isinstance(value, list):
-                if key == 'articles':
-                    data['articles'] = value
-                elif key == 'reseller_data':
-                    data['resellerData'] = value
-                elif key in ('distributors_price_ups', 'matrix_price_ups'):
-                    data = data | generate_price_ups(key, value)
-                else:
-                    data = {**data, **generate_from_list(key, value)}
-
-            else:
-                if key == 'sip':
-                    data[key.upper()] = value
-                if key == 'del_note':
-                    data['order[notes][0][value]'] = None
-                    data['order[notes][0][id]'] = value
-                else:
-                    data[get_excluded_keys(key)] = value
-        if key == 'kwargs':
-            for k, v, in value.items():
-                data[get_camel_case_key(k)] = v
-    logger.debug(f'{data}')
-    return data
-
-
-def generate_price_ups(key, value):
-    data = {}
-    for i in range(len(value)):
-        for key_z, value_z in value[i].items():
-            data_key = get_excluded_keys(key).replace('_index_', str(i)).replace('_key_', key_z)
-            if isinstance(value_z, dict):
-                list_keys = list(value_z.keys())
-                for key_j, value_j in value_z.items():
-                    index_key_j = list_keys.index(key_j)
-                    data[f'{data_key}[{key_z}][{index_key_j}][name]'] = key_j
-                    data[f'{data_key}[{key_z}][{index_key_j}][priceUp]'] = value_j
-            else:
-                data[f'{data_key}[{key_z}]'] = value_z
-    logger.debug(f'{data}')
-    return data
-
-
-def generate_from_list(key, value):
-    data = {}
-    for i in range(len(value)):
-        for key_z, value_z in value[i].items():
-            if not isinstance(value_z, list):
-                data_key = get_excluded_keys(key).replace('_index_', str(i)).replace('_key_', key_z)
-                data[data_key] = value_z
-            else:
-                data_key = get_excluded_keys(key).replace('_index_', str(i)).replace('_key_', key_z)
-                for index_j, value_j in enumerate(value_z):
-                    data[f'{data_key}[{index_j}]'] = value_j
-    logger.debug(f'{data}')
-    return data
-
-
-def generate_payload_filter(**kwargs):
-    data = {}
-    for key, value in kwargs.items():
-        if key not in DEFAULT_FILTER and value is not None and not key.startswith('_'):
-            if isinstance(value, list):
-                for i, x in enumerate(value):
-                    data[
-                        f"filter[{get_camel_case_key(key)}][{i}]"] = x
-            else:
-                data[f"filter[{get_camel_case_key(key)}]"] = value
-    logger.debug(f'{data}')
-    return data
-
-
-def generate_payload_payments(single: bool = True, **kwargs):
-    data = {}
-    for key, value in kwargs.items():
-        if key not in DEFAULT_FILTER and value is not None and not key.startswith('_'):
-            if single:
-                if key == 'link_payments':
-                    data['linkPayments'] = value
-                else:
-                    data[
-                        f"payments[0][{get_camel_case_key(key)}]"
-                    ] = value
-            else:
-                if isinstance(value, list):
-                    for z in range(len(value)):
-                        for key_z, value_z in value[z].items():
-                            data[f'payments[{z}][{key_z}]'] = value_z
-                else:
-                    data[get_camel_case_key(key)] = value
-    logger.debug(f'{data}')
-    return data
-
-
-def generate_payload_online_order(**kwargs):
-    """
-    Generate payload
-    :param kwargs:
-    :return: dict
-    """
-    data = {}
-    for key, value in kwargs.items():
-        if key not in DEFAULT_FILTER and value is not None and not key.startswith('_'):
-            if key == 'order_params':
-                for z in range(len(value)):
-                    for key_z, value_z in value[0].items():
-                        data[f'orderParams[{key_z}]'] = value_z
-            if key == 'positions':
-                for z in range(len(value)):
-                    for key_z, value_z in value[z].items():
-                        if key_z == 'id':
-                            data[f'positions[{z}][{key_z}]'] = value_z
-                        else:
-                            data[f'positions[{z}][positionParams][{key_z}]'] = value_z
-    logger.debug(f'{data}')
-    return data
-
-
-def generate_file_payload(exclude=None, max_size: int = None, **kwargs):
-    """
-    Generate payload
-    :param exclude:
-    :param max_size: Максимальный размер в Мб
-    :param kwargs:
-    :return: :obj:`aiohttp.FormData`
-    """
-    if exclude is None:
-        exclude = []
-    data = FormData()
-    for key, value in kwargs.items():
-        if key not in exclude + DEFAULT_FILTER and value is not None and not key.startswith('_'):
-            data.add_field(get_camel_case_key(key), str(value))
-        if key in exclude and key != '' and value is not None:
-            if isinstance(value, BufferedReader):
-                data.add_field(get_camel_case_key(key), value, filename=value.name, content_type='multipart/form-data')
-            if isinstance(value, str) and not value.isdigit():
-                with open(value, 'rb') as file:
-                    if max_size is not None:
-                        size = file.seek(0, os.SEEK_END)
-                        if (size / 1_048_576) > max_size: raise FileSizeExceeded(
-                            f'Файл не может быть больше {max_size} Мб')
-                    data.add_field(get_camel_case_key(key), file, filename=file.name,
-                                   content_type='multipart/form-data')
-    logger.debug(f'{data}')
-    return data
+import logging
+import os
+from io import BufferedReader
+
+from aiohttp import FormData
+
+from aioabcpapi.exceptions import FileSizeExceeded
+
+DEFAULT_FILTER = ['self', 'cls', 'kwargs']
+logger = logging.getLogger('utils/payload')
+
+
+def get_pascal_case_key(key: str):
+    return ''.join([*map(str.title, key.split('_'))])
+
+
+def get_camel_case_key(key: str):
+    return f"{''.join([key.split('_')[0].lower(), *map(str.title, key.split('_')[1:])])}"
+
+
+def get_excluded_keys(key: str):
+    excluded_keys = {
+        'order_positions': 'order[positions][_index_][_key_]',
+        'positions': 'positions[_index_][_key_]',
+        'articles_catalog': 'articles[_index_][_key_]',
+        'properties': 'properties[_key_][_index_]',
+        'order_params': 'orderParams[_key_]',
+        'distributors': 'distributors[_index_][_key_]',
+        'search': 'search[_index_][_key_]',
+        'basket_positions': 'positions[_index_][_key_]',
+        'goods_group': 'goods_group',
+        'note': 'order[notes][0][value]',
+        'del_note': 'order[notes][0][value]',
+        'delivery_address': 'delivery[meetData][address]',
+        'delivery_person': 'delivery[meetData][person]',
+        'delivery_contact': 'delivery[meetData][contact]',
+        'delivery_comment': 'delivery[meetData][comment]',
+        'delivery_employee_contact': 'delivery[meetData][employeeContact]',
+        'delivery_employee_person': 'delivery[meetData][employeePerson]',
+        'delivery_reseller_comment': 'delivery[meetData][resellerComment]',
+        'delivery_start_time': 'delivery[timeInterval][startTime]',
+        'delivery_end_time': 'delivery[timeInterval][endTime]',
+        'delivery_method_id': 'delivery[methodId]',
+        'client_order_number': 'clientOrderNumber',
+        'cross_image': 'cross_image',
+        'with_original': 'with_original',
+        'old_item_id': 'oldItemID',
+        'distributors_price_ups': 'distributorsPriceUps[_index_]',
+        'matrix_price_ups': 'matrixPriceUps[_index_]',
+    }
+    try:
+        return excluded_keys[key]
+    except KeyError:
+        return get_pascal_case_key(key)
+
+
+def generate_payload(exclude=None, order: bool = False, **kwargs):
+    """
+    Generate payload
+    :param exclude:
+    :param order: Generate dict for create or edit order
+    :param kwargs:
+    :return: dict
+    """
+    if exclude is None:
+        exclude = ['order_params', 'distributors', 'note', 'del_note',
+                   'basket_positions', 'sip']
+    data = {}
+
+    for key, value in kwargs.items():
+        if key not in exclude + DEFAULT_FILTER and value is not None and not key.startswith('_'):
+            if not order:
+                if isinstance(value, list):
+                    for i, x in enumerate(value):
+                        data[f"{get_camel_case_key(key)}[{i}]"] = x
+                else:
+                    data[get_camel_case_key(key)] = value
+            else:
+                data[f"order[{get_camel_case_key(key)}]"] = value
+        if key in exclude and key not in DEFAULT_FILTER and value is not None:
+            if isinstance(value, list):
+                if key == 'articles':
+                    data['articles'] = value
+                elif key == 'reseller_data':
+                    data['resellerData'] = value
+                elif key in ('distributors_price_ups', 'matrix_price_ups'):
+                    data = data | generate_price_ups(key, value)
+                else:
+                    data = {**data, **generate_from_list(key, value)}
+
+            else:
+                if key == 'sip':
+                    data[key.upper()] = value
+                if key == 'del_note':
+                    data['order[notes][0][value]'] = None
+                    data['order[notes][0][id]'] = value
+                else:
+                    data[get_excluded_keys(key)] = value
+        if key == 'kwargs':
+            for k, v, in value.items():
+                data[get_camel_case_key(k)] = v
+    logger.debug(f'{data}')
+    return data
+
+
+def generate_price_ups(key, value):
+    data = {}
+    for i in range(len(value)):
+        for key_z, value_z in value[i].items():
+            data_key = get_excluded_keys(key).replace('_index_', str(i)).replace('_key_', key_z)
+            if isinstance(value_z, dict):
+                list_keys = list(value_z.keys())
+                for key_j, value_j in value_z.items():
+                    index_key_j = list_keys.index(key_j)
+                    data[f'{data_key}[{key_z}][{index_key_j}][name]'] = key_j
+                    data[f'{data_key}[{key_z}][{index_key_j}][priceUp]'] = value_j
+            else:
+                data[f'{data_key}[{key_z}]'] = value_z
+    logger.debug(f'{data}')
+    return data
+
+
+def generate_from_list(key, value):
+    data = {}
+    for i in range(len(value)):
+        for key_z, value_z in value[i].items():
+            if not isinstance(value_z, list):
+                data_key = get_excluded_keys(key).replace('_index_', str(i)).replace('_key_', key_z)
+                data[data_key] = value_z
+            else:
+                data_key = get_excluded_keys(key).replace('_index_', str(i)).replace('_key_', key_z)
+                for index_j, value_j in enumerate(value_z):
+                    data[f'{data_key}[{index_j}]'] = value_j
+    logger.debug(f'{data}')
+    return data
+
+
+def generate_payload_filter(**kwargs):
+    data = {}
+    for key, value in kwargs.items():
+        if key not in DEFAULT_FILTER and value is not None and not key.startswith('_'):
+            if isinstance(value, list):
+                for i, x in enumerate(value):
+                    data[
+                        f"filter[{get_camel_case_key(key)}][{i}]"] = x
+            else:
+                data[f"filter[{get_camel_case_key(key)}]"] = value
+    logger.debug(f'{data}')
+    return data
+
+
+def generate_payload_payments(single: bool = True, **kwargs):
+    data = {}
+    for key, value in kwargs.items():
+        if key not in DEFAULT_FILTER and value is not None and not key.startswith('_'):
+            if single:
+                if key == 'link_payments':
+                    data['linkPayments'] = value
+                else:
+                    data[
+                        f"payments[0][{get_camel_case_key(key)}]"
+                    ] = value
+            else:
+                if isinstance(value, list):
+                    for z in range(len(value)):
+                        for key_z, value_z in value[z].items():
+                            data[f'payments[{z}][{key_z}]'] = value_z
+                else:
+                    data[get_camel_case_key(key)] = value
+    logger.debug(f'{data}')
+    return data
+
+
+def generate_payload_online_order(**kwargs):
+    """
+    Generate payload
+    :param kwargs:
+    :return: dict
+    """
+    data = {}
+    for key, value in kwargs.items():
+        if key not in DEFAULT_FILTER and value is not None and not key.startswith('_'):
+            if key == 'order_params':
+                for z in range(len(value)):
+                    for key_z, value_z in value[0].items():
+                        data[f'orderParams[{key_z}]'] = value_z
+            if key == 'positions':
+                for z in range(len(value)):
+                    for key_z, value_z in value[z].items():
+                        if key_z == 'id':
+                            data[f'positions[{z}][{key_z}]'] = value_z
+                        else:
+                            data[f'positions[{z}][positionParams][{key_z}]'] = value_z
+    logger.debug(f'{data}')
+    return data
+
+
+def generate_file_payload(exclude=None, max_size: int = None, **kwargs):
+    """
+    Generate payload
+    :param exclude:
+    :param max_size: Максимальный размер в Мб
+    :param kwargs:
+    :return: :obj:`aiohttp.FormData`
+    """
+    if exclude is None:
+        exclude = []
+    data = FormData()
+    for key, value in kwargs.items():
+        if key not in exclude + DEFAULT_FILTER and value is not None and not key.startswith('_'):
+            data.add_field(get_camel_case_key(key), str(value))
+        if key in exclude and key != '' and value is not None:
+            if isinstance(value, BufferedReader):
+                data.add_field(get_camel_case_key(key), value, filename=value.name, content_type='multipart/form-data')
+            if isinstance(value, str) and not value.isdigit():
+                with open(value, 'rb') as file:
+                    if max_size is not None:
+                        size = file.seek(0, os.SEEK_END)
+                        if (size / 1_048_576) > max_size: raise FileSizeExceeded(
+                            f'Файл не может быть больше {max_size} Мб')
+                    data.add_field(get_camel_case_key(key), file, filename=file.name,
+                                   content_type='multipart/form-data')
+    logger.debug(f'{data}')
+    return data
```

### Comparing `aioabcpapi-2.0.6/aioabcpapi.egg-info/PKG-INFO` & `aioabcpapi-2.0.7/aioabcpapi.egg-info/PKG-INFO`

 * *Files 13% similar despite different names*

```diff
@@ -1,103 +1,102 @@
-Metadata-Version: 2.1
-Name: aioabcpapi
-Version: 2.0.6
-Summary: Async library for ABCP API
-Home-page: https://github.com/bl4ckm45k/aioabcpapi
-Author: bl4ckm45k
-Author-email: nonpowa@gmail.com
-License: MIT
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
-Classifier: Framework :: AsyncIO
-Classifier: Intended Audience :: Developers
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Operating System :: OS Independent
-Classifier: Topic :: Software Development :: Libraries :: Application Frameworks
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
-## AioAbcpApi
-
-Асинхронная библиотека для [API ABCP](https://www.abcp.ru/wiki/ABCP.API "API ABCP")
-с [asyncio](https://docs.python.org/3/library/asyncio.html "asyncio")
-и [aiohttp](https://github.com/aio-libs/aiohttp "aiohttp")
-
-![](https://img.shields.io/github/stars/bl4ckm45k/aioabcpapi.svg)
-![](https://img.shields.io/github/forks/bl4ckm45k/aioabcpapi.svg)
-![](https://img.shields.io/github/issues/bl4ckm45k/aioabcpapi.svg)
-[![Supported python versions](https://img.shields.io/pypi/pyversions/aioabcpapi.svg)](https://pypi.python.org/pypi/aioabcpapi)
-[![Downloads](https://img.shields.io/pypi/dm/aioabcpapi.svg?)](https://pypi.python.org/pypi/aioabcpapi)
-[![PyPi Package Version](https://img.shields.io/pypi/v/aioabcpapi)](https://pypi.python.org/pypi/aioabcpapi)
-
-
-Присоединяйтесь к [телеграм чату](https://t.me/aioabcpapi "Телеграм чат")
-### Установка
-`pip install aioabcpapi`
-
-### Описание
-
-------------
-
-Все методы максимально приближены к древовидному оформлению [официальной документации](https://www.abcp.ru/wiki/ABCP.API).
-
-Разделяются на `cp` и `ts`, они в свою очередь разделяются на `client` и `admin`, далее для поиска нужного вам метода
-отталкивайтесь от документации [API ABCP](https://www.abcp.ru/wiki/ABCP.API).
-
-Для примера, из документации **TS.Client**, [Обновление позиции в корзине](https://www.abcp.ru/wiki/API.TS.Client#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D0.B5)
-описание операции следующее:
->  Операция: POST /ts/cart/update
-
-Для использования этого метода нам нужно будет обратиться к `await api.ts.client.cart.update()`
-
-### Доступ к API
-
-------------
-[Для API Администратора](https://cp.abcp.ru/?page=allsettings&systemsettings&apiInformation)
-
-Если вы являетесь клиентом магазина на платформе ABCP, обратитесь к вашему менеджеру. (Вам понадобится статический IP адрес)
-
-### Примечание 
-
-------------
-
-Все аргументы времени, такие как `create_time`, `update_time`, `date_start`, `date_end` и прочие, принимают `str` или `datetime`. При передаче `datetime` объект будет преобразован в зависимости от требований метода в `RFC3339` или `"%Y-%m-%d %H:%M:%S"`
-
-### Пример
-
-------------
-
-```python
-import asyncio
-from aioabcpapi import Abcp
-
-host, login, password = 'id33333', 'api@id33333', 'md5hash'
-api = Abcp(host, login, password)
-
-
-async def search_some_parts(article, brand):
-    search_result = await api.cp.client.search.articles(number=article, brand=brand,
-                                                        use_online_stocks=True,
-                                                        disable_online_filtering=True,
-                                                        with_out_analogs=True)
-    for x in search_result:
-        if float(x['price']) < 3000:
-            print('Похоже на чудо, но скорее ошибка прайса. Отключим пока поставщика')
-            await api.cp.admin.distributors.edit_status(x['distributorId'], False)
-        elif float(x['price']) < 37000:
-            await api.cp.client.basket.add(basket_positions={'number': x['article'],
-                                                             'brand': x['brand'],
-                                                             'supplierCode': x['supplierCode'],
-                                                             'itemKey': x['itemKey'],
-                                                             'quantity': 1,
-                                                             'comment': f"Да, РРЦ никто не любит"})
-
-
-if __name__ == '__main__':
-    asyncio.run(search_some_parts('602000600', 'LuK'))
-```
-
-[**Больше примеров**](https://github.com/bl4ckm45k/aioabcpapi/tree/master/examples "Примеры")
+Metadata-Version: 2.1
+Name: aioabcpapi
+Version: 2.0.7
+Summary: Async library for ABCP API
+Home-page: https://github.com/bl4ckm45k/aioabcpapi
+Author: bl4ckm45k
+Author-email: nonpowa@gmail.com
+License: MIT
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Classifier: Framework :: AsyncIO
+Classifier: Intended Audience :: Developers
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Operating System :: OS Independent
+Classifier: Topic :: Software Development :: Libraries :: Application Frameworks
+Requires-Python: >=3.8
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
+## AioAbcpApi
+
+Асинхронная библиотека для [API ABCP](https://www.abcp.ru/wiki/ABCP.API "API ABCP")
+с [asyncio](https://docs.python.org/3/library/asyncio.html "asyncio")
+и [aiohttp](https://github.com/aio-libs/aiohttp "aiohttp")
+
+![](https://img.shields.io/github/stars/bl4ckm45k/aioabcpapi.svg)
+![](https://img.shields.io/github/forks/bl4ckm45k/aioabcpapi.svg)
+![](https://img.shields.io/github/issues/bl4ckm45k/aioabcpapi.svg)
+[![Supported python versions](https://img.shields.io/pypi/pyversions/aioabcpapi.svg)](https://pypi.python.org/pypi/aioabcpapi)
+[![Downloads](https://img.shields.io/pypi/dm/aioabcpapi.svg?)](https://pypi.python.org/pypi/aioabcpapi)
+[![PyPi Package Version](https://img.shields.io/pypi/v/aioabcpapi)](https://pypi.python.org/pypi/aioabcpapi)
+
+
+Присоединяйтесь к [телеграм чату](https://t.me/aioabcpapi "Телеграм чат")
+### Установка
+`pip install aioabcpapi`
+
+### Описание
+
+------------
+
+Все методы максимально приближены к древовидному оформлению [официальной документации](https://www.abcp.ru/wiki/ABCP.API).
+
+Разделяются на `cp` и `ts`, они в свою очередь разделяются на `client` и `admin`, далее для поиска нужного вам метода
+отталкивайтесь от документации [API ABCP](https://www.abcp.ru/wiki/ABCP.API).
+
+Для примера, из документации **TS.Client**, [Обновление позиции в корзине](https://www.abcp.ru/wiki/API.TS.Client#.D0.9E.D0.B1.D0.BD.D0.BE.D0.B2.D0.BB.D0.B5.D0.BD.D0.B8.D0.B5_.D0.BF.D0.BE.D0.B7.D0.B8.D1.86.D0.B8.D0.B8_.D0.B2_.D0.BA.D0.BE.D1.80.D0.B7.D0.B8.D0.BD.D0.B5)
+описание операции следующее:
+>  Операция: POST /ts/cart/update
+
+Для использования этого метода нам нужно будет обратиться к `await api.ts.client.cart.update()`
+
+### Доступ к API
+
+------------
+[Для API Администратора](https://cp.abcp.ru/?page=allsettings&systemsettings&apiInformation)
+
+Если вы являетесь клиентом магазина на платформе ABCP, обратитесь к вашему менеджеру. (Вам понадобится статический IP адрес)
+
+### Примечание 
+
+------------
+
+Все аргументы времени, такие как `create_time`, `update_time`, `date_start`, `date_end` и прочие, принимают `str` или `datetime`. При передаче `datetime` объект будет преобразован в зависимости от требований метода в `RFC3339` или `"%Y-%m-%d %H:%M:%S"`
+
+### Пример
+
+------------
+
+```python
+import asyncio
+from aioabcpapi import Abcp
+
+host, login, password = 'id33333', 'api@id33333', 'md5hash'
+api = Abcp(host, login, password)
+
+
+async def search_some_parts(article, brand):
+    search_result = await api.cp.client.search.articles(number=article, brand=brand,
+                                                        use_online_stocks=True,
+                                                        disable_online_filtering=True,
+                                                        with_out_analogs=True)
+    for x in search_result:
+        if float(x['price']) < 3000:
+            print('Похоже на чудо, но скорее ошибка прайса. Отключим пока поставщика')
+            await api.cp.admin.distributors.edit_status(x['distributorId'], False)
+        elif float(x['price']) < 37000:
+            await api.cp.client.basket.add(basket_positions={'number': x['article'],
+                                                             'brand': x['brand'],
+                                                             'supplierCode': x['supplierCode'],
+                                                             'itemKey': x['itemKey'],
+                                                             'quantity': 1,
+                                                             'comment': f"Да, РРЦ никто не любит"})
+
+
+if __name__ == '__main__':
+    asyncio.run(search_some_parts('602000600', 'LuK'))
+```
+
+[**Больше примеров**](https://github.com/bl4ckm45k/aioabcpapi/tree/master/examples "Примеры")
```

### Comparing `aioabcpapi-2.0.6/setup.py` & `aioabcpapi-2.0.7/setup.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,33 +1,32 @@
-import sys
-from setuptools import setup
-
-if sys.version_info < (3, 7):
-    raise RuntimeError('Your Python version {0} is not supported, please install '
-                       'Python 3.7+'.format('.'.join(map(str, sys.version_info[:3]))))
-requirements = ["aiohttp>=3.8.3", "certifi>=2022.12.7", "ujson>=5.7.0", "pytz>=2022.7.1", "pyrfc3339"]
-setup(
-    name='aioabcpapi',
-    version='2.0.6',
-    author='bl4ckm45k',
-    author_email='nonpowa@gmail.com',
-    description='Async library for ABCP API',
-    long_description_content_type="text/markdown",
-    url="https://github.com/bl4ckm45k/aioabcpapi",
-    license="MIT",
-    packages=['aioabcpapi', 'aioabcpapi/cp', 'aioabcpapi/ts', 'aioabcpapi/utils'],
-    install_requires=requirements,
-    classifiers=[
-        'Programming Language :: Python :: 3.7',
-        'Programming Language :: Python :: 3.8',
-        'Programming Language :: Python :: 3.9',
-        'Programming Language :: Python :: 3.10',
-        'Programming Language :: Python :: 3.11',
-        'Framework :: AsyncIO',
-        'Intended Audience :: Developers',
-        'License :: OSI Approved :: MIT License',
-        'Operating System :: OS Independent',
-        'Topic :: Software Development :: Libraries :: Application Frameworks',
-
-    ],
-    python_requires='>=3.7'
-)
+import sys
+from setuptools import setup
+
+if sys.version_info < (3, 8):
+    raise RuntimeError('Your Python version {0} is not supported, please install '
+                       'Python 3.8+'.format('.'.join(map(str, sys.version_info[:3]))))
+requirements = ["wheel", "aiohttp>=3.8.5", "certifi>=2023.7.22", "ujson>=5.8.0", "pytz>=2023.3", "pyrfc3339"]
+setup(
+    name='aioabcpapi',
+    version='2.0.7',
+    author='bl4ckm45k',
+    author_email='nonpowa@gmail.com',
+    description='Async library for ABCP API',
+    long_description_content_type="text/markdown",
+    url="https://github.com/bl4ckm45k/aioabcpapi",
+    license="MIT",
+    packages=['aioabcpapi', 'aioabcpapi/cp', 'aioabcpapi/ts', 'aioabcpapi/utils'],
+    install_requires=requirements,
+    classifiers=[
+        'Programming Language :: Python :: 3.8',
+        'Programming Language :: Python :: 3.9',
+        'Programming Language :: Python :: 3.10',
+        'Programming Language :: Python :: 3.11',
+        'Framework :: AsyncIO',
+        'Intended Audience :: Developers',
+        'License :: OSI Approved :: MIT License',
+        'Operating System :: OS Independent',
+        'Topic :: Software Development :: Libraries :: Application Frameworks',
+
+    ],
+    python_requires='>=3.8'
+)
```

