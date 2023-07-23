# Comparing `tmp/inpost-0.1.5a1.tar.gz` & `tmp/inpost-0.1.5a2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "inpost-0.1.5a1.tar", max compression
+gzip compressed data, was "inpost-0.1.5a2.tar", max compression
```

## Comparing `inpost-0.1.5a1.tar` & `inpost-0.1.5a2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
--rw-r--r--   0        0        0     1307 2023-06-24 19:18:25.396890 inpost-0.1.5a1/README.md
--rw-r--r--   0        0        0       24 2023-01-11 14:04:51.297207 inpost-0.1.5a1/inpost/__init__.py
--rw-r--r--   0        0        0    59055 2023-06-24 21:34:19.057880 inpost-0.1.5a1/inpost/api.py
--rw-r--r--   0        0        0     3541 2023-06-24 17:20:24.712098 inpost-0.1.5a1/inpost/static/__init__.py
--rw-r--r--   0        0        0     2951 2023-06-24 16:59:22.179852 inpost-0.1.5a1/inpost/static/endpoints.py
--rw-r--r--   0        0        0     2715 2023-06-24 17:48:43.048073 inpost-0.1.5a1/inpost/static/exceptions.py
--rw-r--r--   0        0        0     2677 2023-06-24 21:04:10.186415 inpost-0.1.5a1/inpost/static/friends.py
--rw-r--r--   0        0        0       47 2023-01-08 12:39:56.709189 inpost-0.1.5a1/inpost/static/headers.py
--rw-r--r--   0        0        0     1559 2023-06-24 20:38:42.495391 inpost-0.1.5a1/inpost/static/notifications.py
--rw-r--r--   0        0        0    46977 2023-07-02 08:49:07.499846 inpost-0.1.5a1/inpost/static/parcels.py
--rw-r--r--   0        0        0     8116 2023-06-24 19:22:24.781835 inpost-0.1.5a1/inpost/static/statuses.py
--rw-r--r--   0        0        0     1517 2023-07-02 08:49:07.499846 inpost-0.1.5a1/pyproject.toml
--rw-r--r--   0        0        0     2225 1970-01-01 00:00:00.000000 inpost-0.1.5a1/setup.py
--rw-r--r--   0        0        0     2522 1970-01-01 00:00:00.000000 inpost-0.1.5a1/PKG-INFO
+-rw-r--r--   0        0        0     1307 2023-06-24 19:18:25.396890 inpost-0.1.5a2/README.md
+-rw-r--r--   0        0        0       24 2023-01-11 14:04:51.297207 inpost-0.1.5a2/inpost/__init__.py
+-rw-r--r--   0        0        0    59170 2023-07-23 09:01:08.211300 inpost-0.1.5a2/inpost/api.py
+-rw-r--r--   0        0        0     3541 2023-06-24 17:20:24.712098 inpost-0.1.5a2/inpost/static/__init__.py
+-rw-r--r--   0        0        0     2951 2023-06-24 16:59:22.179852 inpost-0.1.5a2/inpost/static/endpoints.py
+-rw-r--r--   0        0        0     2715 2023-06-24 17:48:43.048073 inpost-0.1.5a2/inpost/static/exceptions.py
+-rw-r--r--   0        0        0     2677 2023-06-24 21:04:10.186415 inpost-0.1.5a2/inpost/static/friends.py
+-rw-r--r--   0        0        0       47 2023-01-08 12:39:56.709189 inpost-0.1.5a2/inpost/static/headers.py
+-rw-r--r--   0        0        0     1559 2023-06-24 20:38:42.495391 inpost-0.1.5a2/inpost/static/notifications.py
+-rw-r--r--   0        0        0    46977 2023-07-02 08:49:07.499846 inpost-0.1.5a2/inpost/static/parcels.py
+-rw-r--r--   0        0        0     8116 2023-06-24 19:22:24.781835 inpost-0.1.5a2/inpost/static/statuses.py
+-rw-r--r--   0        0        0     1517 2023-07-23 09:00:39.784483 inpost-0.1.5a2/pyproject.toml
+-rw-r--r--   0        0        0     2225 1970-01-01 00:00:00.000000 inpost-0.1.5a2/setup.py
+-rw-r--r--   0        0        0     2522 1970-01-01 00:00:00.000000 inpost-0.1.5a2/PKG-INFO
```

### Comparing `inpost-0.1.5a1/README.md` & `inpost-0.1.5a2/README.md`

 * *Files identical despite different names*

### Comparing `inpost-0.1.5a1/inpost/api.py` & `inpost-0.1.5a2/inpost/api.py`

 * *Files 1% similar despite different names*

```diff
@@ -585,21 +585,21 @@
         if resp.status == 200:
             self._log.debug(f"collected compartment properties for {parcel_obj_.shipment_number}")
             parcel_obj_.compartment_properties = await resp.json()
             return parcel_obj_
 
         raise UnidentifiedAPIError(reason=resp)
 
-    async def open_compartment(self, parcel_obj: Parcel) -> bool:
+    async def open_compartment(self, parcel_obj: Parcel) -> Parcel:
         """Opens compartment for `Inpost.parcel` object
 
         :param parcel_obj: Parcel object
         :type parcel_obj: Parcel
-        :return: True if compartment gets opened
-        :rtype: bool
+        :return: Parcel with compartment location set if it gets opened
+        :rtype: Parcel
         :raises NotAuthenticatedError: User not authenticated in inpost service
         :raises UnauthorizedError: Unauthorized access to inpost services,
         :raises NotFoundError: Phone number not found
         :raises UnidentifiedAPIError: Unexpected thing happened
         """
 
         self._log.info(f"opening compartment for {parcel_obj.shipment_number}")
@@ -616,15 +616,16 @@
             headers=None,
             data={"sessionUuid": parcel_obj.compartment_properties.session_uuid},
             autorefresh=True,
         )
 
         if resp.status == 200:
             self._log.debug(f"opened compartment for {parcel_obj.shipment_number}")
-            return True
+            parcel_obj.compartment_location = await resp.json()
+            return parcel_obj
 
         raise UnidentifiedAPIError(reason=resp)
 
     async def check_compartment_status(
         self, parcel_obj: Parcel, expected_status: CompartmentExpectedStatus = CompartmentExpectedStatus.OPENED
     ) -> bool:
         """Checks and compare compartment status (e.g. opened, closed) with expected status
@@ -737,17 +738,17 @@
 
         if parcel_obj is None:
             raise NoParcelError(reason="Could not obtain desired parcel!")
 
         self._log.info(f"collecting parcel with shipment number {parcel_obj.shipment_number}")
 
         if parcel_obj_ := await self.collect_compartment_properties(parcel_obj=parcel_obj, location=location):
-            if await self.open_compartment(parcel_obj=parcel_obj_):
-                if await self.check_compartment_status(parcel_obj=parcel_obj_):
-                    return parcel_obj_
+            if parcel_obj__ := await self.open_compartment(parcel_obj=parcel_obj_):
+                if await self.check_compartment_status(parcel_obj=parcel_obj__):
+                    return parcel_obj__
 
         return None
 
     async def close_compartment(self, parcel_obj: Parcel) -> bool:
         """Checks whether actual compartment status and expected one matches then notifies inpost api that
         compartment is closed. Should be invoked after collecting parcel
```

### Comparing `inpost-0.1.5a1/inpost/static/__init__.py` & `inpost-0.1.5a2/inpost/static/__init__.py`

 * *Files identical despite different names*

### Comparing `inpost-0.1.5a1/inpost/static/endpoints.py` & `inpost-0.1.5a2/inpost/static/endpoints.py`

 * *Files identical despite different names*

### Comparing `inpost-0.1.5a1/inpost/static/exceptions.py` & `inpost-0.1.5a2/inpost/static/exceptions.py`

 * *Files identical despite different names*

### Comparing `inpost-0.1.5a1/inpost/static/friends.py` & `inpost-0.1.5a2/inpost/static/friends.py`

 * *Files identical despite different names*

### Comparing `inpost-0.1.5a1/inpost/static/notifications.py` & `inpost-0.1.5a2/inpost/static/notifications.py`

 * *Files identical despite different names*

### Comparing `inpost-0.1.5a1/inpost/static/parcels.py` & `inpost-0.1.5a2/inpost/static/parcels.py`

 * *Files identical despite different names*

### Comparing `inpost-0.1.5a1/inpost/static/statuses.py` & `inpost-0.1.5a2/inpost/static/statuses.py`

 * *Files identical despite different names*

### Comparing `inpost-0.1.5a1/pyproject.toml` & `inpost-0.1.5a2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "inpost"
-version = "0.1.5a1"
+version = "0.1.5a2"
 description = "Asynchronous InPost package allowing you to manage existing incoming parcels without mobile app"
 authors = ["loboda4450 <loboda4450@gmail.com>", "MrKazik99 <mrkazik99@gmail.com>"]
 maintainers = ["loboda4450 <loboda4450@gmail.com>"]
 documentation = 'https://inpost-python.readthedocs.io/en/latest/index.html'
 repository = "https://github.com/IFOSSA/inpost-python"
 readme = "README.md"
 packages = [
```

### Comparing `inpost-0.1.5a1/setup.py` & `inpost-0.1.5a2/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -12,15 +12,15 @@
  'aiohttp>=3.8.1,<4.0.0',
  'arrow>=1.2.3,<2.0.0',
  'pytest>=7.4.0,<8.0.0',
  'qrcode>=7.3.1,<8.0.0']
 
 setup_kwargs = {
     'name': 'inpost',
-    'version': '0.1.5a1',
+    'version': '0.1.5a2',
     'description': 'Asynchronous InPost package allowing you to manage existing incoming parcels without mobile app',
     'long_description': "[![CodeFactor](https://www.codefactor.io/repository/github/ifossa/inpost-python/badge)](https://www.codefactor.io/repository/github/ifossa/inpost-python)\n![Code Quality](https://github.com/ifossa/inpost-python/actions/workflows/lint.yml/badge.svg?barnch=main)\n![Todos](https://github.com/ifossa/inpost-python/actions/workflows/todos.yml/badge.svg?barnch=main)\n\n# Inpost Python\n\nFully async Inpost library using Python 3.10.\n\n\n## Documentation\n\n[Readthedocs.io](https://inpost-python.readthedocs.io/en/latest/)\n\n\n## Usage/Examples\n\n\n```python\nfrom inpost.api import Inpost\n\ninp = Inpost('555333444')\nawait inp.send_sms_code():\n...\nif await inp.confirm_sms_code(123321):\n   print('Congratulations, you initialized successfully!')\n```\n\n## Before you contribute\n\n![Contributors](https://contrib.rocks/image?repo=ifossa/inpost-python)\n\nInstall linters and checkers, unlinted pull requests will not be approved\n```commandline\npoetry run pre-commit install\n```\n\n## Authors\n\n- [@loboda4450](https://www.github.com/loboda4450)\n- [@mrkazik99](https://www.github.com/mrkazik99)\n\n\n## Used By\n\nThis project is used by the following repos:\n\n[Inpost Telegram Bot](https://github.com/loboda4450/inpost-telegram-bot)\n\n\n\n## 😂 Here is a random joke that'll make you laugh!\n![Jokes Card](https://readme-jokes.vercel.app/api)",
     'author': 'loboda4450',
     'author_email': 'loboda4450@gmail.com',
     'maintainer': 'loboda4450',
     'maintainer_email': 'loboda4450@gmail.com',
     'url': 'https://github.com/IFOSSA/inpost-python',
```

### Comparing `inpost-0.1.5a1/PKG-INFO` & `inpost-0.1.5a2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: inpost
-Version: 0.1.5a1
+Version: 0.1.5a2
 Summary: Asynchronous InPost package allowing you to manage existing incoming parcels without mobile app
 Home-page: https://github.com/IFOSSA/inpost-python
 Author: loboda4450
 Author-email: loboda4450@gmail.com
 Maintainer: loboda4450
 Maintainer-email: loboda4450@gmail.com
 Requires-Python: >=3.10,<4.0
```

