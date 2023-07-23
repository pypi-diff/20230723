# Comparing `tmp/xyz_common-0.1.5-py3-none-any.whl.zip` & `tmp/xyz_common-0.1.6-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,23 +1,23 @@
-Zip file size: 12126 bytes, number of entries: 21
+Zip file size: 12606 bytes, number of entries: 21
 -rw-r--r--  2.0 unx       45 b- defN 20-Jan-21 08:52 xyz_common/__init__.py
 -rw-r--r--  2.0 unx     1763 b- defN 20-Aug-07 03:03 xyz_common/admin.py
--rw-r--r--  2.0 unx     1749 b- defN 22-Jul-13 09:40 xyz_common/apis.py
+-rw-r--r--  2.0 unx     1809 b- defN 23-Jul-23 13:56 xyz_common/apis.py
 -rw-r--r--  2.0 unx      337 b- defN 20-Jan-21 08:55 xyz_common/apps.py
 -rw-r--r--  2.0 unx     1389 b- defN 21-Nov-08 00:26 xyz_common/consumers.py
 -rw-r--r--  2.0 unx      893 b- defN 20-Dec-05 08:29 xyz_common/helper.py
 -rw-r--r--  2.0 unx     4436 b- defN 22-May-29 14:07 xyz_common/models.py
 -rw-r--r--  2.0 unx     3188 b- defN 22-May-29 16:54 xyz_common/receivers.py
 -rw-r--r--  2.0 unx      629 b- defN 21-Dec-12 10:33 xyz_common/serializers.py
 -rw-r--r--  2.0 unx      407 b- defN 22-Jun-22 16:08 xyz_common/signals.py
--rw-r--r--  2.0 unx      208 b- defN 20-Sep-14 14:50 xyz_common/urls.py
--rw-r--r--  2.0 unx     1582 b- defN 21-Jun-24 09:19 xyz_common/views.py
+-rw-r--r--  2.0 unx      244 b- defN 23-Jun-01 18:23 xyz_common/urls.py
+-rw-r--r--  2.0 unx     3508 b- defN 23-Jun-01 18:30 xyz_common/views.py
 -rw-r--r--  2.0 unx     4701 b- defN 20-Feb-04 10:21 xyz_common/migrations/0001_initial.py
 -rw-r--r--  2.0 unx     1146 b- defN 20-Aug-07 11:12 xyz_common/migrations/0002_auto_20200807_1912.py
 -rw-r--r--  2.0 unx      526 b- defN 21-Dec-16 13:40 xyz_common/migrations/0003_auto_20211216_2140.py
 -rw-r--r--  2.0 unx      503 b- defN 22-May-29 14:10 xyz_common/migrations/0004_auto_20220529_2210.py
 -rw-r--r--  2.0 unx        0 b- defN 20-Feb-04 10:21 xyz_common/migrations/__init__.py
--rw-r--r--  2.0 unx      955 b- defN 22-Jul-14 01:58 xyz_common-0.1.5.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 22-Jul-14 01:58 xyz_common-0.1.5.dist-info/WHEEL
--rw-r--r--  2.0 unx       11 b- defN 22-Jul-14 01:58 xyz_common-0.1.5.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     1726 b- defN 22-Jul-14 01:58 xyz_common-0.1.5.dist-info/RECORD
-21 files, 26286 bytes uncompressed, 9308 bytes compressed:  64.6%
+-rw-r--r--  2.0 unx      927 b- defN 23-Jul-23 17:56 xyz_common-0.1.6.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 17:56 xyz_common-0.1.6.dist-info/WHEEL
+-rw-r--r--  2.0 unx       11 b- defN 23-Jul-23 17:56 xyz_common-0.1.6.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     1726 b- defN 23-Jul-23 17:56 xyz_common-0.1.6.dist-info/RECORD
+21 files, 28280 bytes uncompressed, 9788 bytes compressed:  65.4%
```

## zipnote {}

```diff
@@ -45,20 +45,20 @@
 
 Filename: xyz_common/migrations/0004_auto_20220529_2210.py
 Comment: 
 
 Filename: xyz_common/migrations/__init__.py
 Comment: 
 
-Filename: xyz_common-0.1.5.dist-info/METADATA
+Filename: xyz_common-0.1.6.dist-info/METADATA
 Comment: 
 
-Filename: xyz_common-0.1.5.dist-info/WHEEL
+Filename: xyz_common-0.1.6.dist-info/WHEEL
 Comment: 
 
-Filename: xyz_common-0.1.5.dist-info/top_level.txt
+Filename: xyz_common-0.1.6.dist-info/top_level.txt
 Comment: 
 
-Filename: xyz_common-0.1.5.dist-info/RECORD
+Filename: xyz_common-0.1.6.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## xyz_common/apis.py

```diff
@@ -14,15 +14,17 @@
 @register()
 class ContenttypeViewSet(viewsets.ReadOnlyModelViewSet):
     queryset = ctmodels.ContentType.objects.all().order_by('app_label')
     serializer_class = serializers.ContenttypeSerializer
     permission_classes = []
     search_fields = ('app_label', 'model')
     filter_fields = {
-        'id': ['exact', 'in']
+        'id': ['exact', 'in'],
+        'app_label': ['exact'],
+        'model': ['exact']
     }
 
     def filter_queryset(self, queryset):
         if self.action == 'all':
             return self.queryset
         from xyz_auth.helper import get_user_model_permissions
         from django.db.models import Q
```

## xyz_common/urls.py

```diff
@@ -1,8 +1,9 @@
 # -*- coding:utf-8 -*- 
 __author__ = 'denishuang'
 from django.conf.urls import url
 from . import views
 app_name = 'common'
 urlpatterns = [
     url(r'^async_result/(?P<task_id>[\w-]+)/', views.async_result),
+    url(r'^stream/', views.stream),
 ]
```

## xyz_common/views.py

```diff
@@ -1,11 +1,23 @@
-
 import json
+import time
+import datetime
 import six
 from six import text_type
+from django.http.response import StreamingHttpResponse
+
+def stream(request):
+    def event_stream():
+        while True:
+            time.sleep(3)
+            t = datetime.datetime.now()
+            print(t)
+            yield 'data: The server time is: %s\n\n' % t
+    return StreamingHttpResponse(event_stream(), content_type='text/event-stream')
+
 if six.PY2:
     from dwebsocket.decorators import accept_websocket
     from django.http import HttpResponse
     from celery.result import AsyncResult
     import logging
 
     log = logging.getLogger("django")
@@ -39,9 +51,52 @@
             pm(d)
             try:
                 r = rs.get(on_message=pm, propagate=False)
             except Exception as e:
                 body = {'status': 'FAILURE', 'result': text_type(e)}
                 request.websocket.send(('%s\r' % json.dumps(body)).encode('utf8'))
 else:
+    # import asyncio
+    # import websockets
+
+    # async def recv_msg(websocket):
+    #     while True:
+    #         recv_text = await websocket.recv()
+    #         response_text = f"your submit context: {recv_text}"
+    #         await websocket.send(response_text)
+    #
+    #
+    # async def main_logic(websocket, path):
+    #     #await check_permit(websocket)
+    #     await recv_msg(websocket)
+
+    #
+    # start_server = websockets.serve(main_logic, '127.0.0.1', 5678)
+    # asyncio.get_event_loop().run_until_complete(start_server)
+    # asyncio.get_event_loop().run_forever()
+    from celery.result import AsyncResult
+
     def async_result(request, task_id):
-        pass
+        # rs = AsyncResult(task_id)
+        # events= []
+        # def pm(body):
+        #     try:
+        #         if body['status'] in ['FAILURE', 'REVOKED']:
+        #             body['result'] = text_type(body['result'])
+        #         events.insert(0, json.dumps(body))
+        #     except Exception:
+        #         import traceback
+        #         log.error("async_result dump json error, body: %s; error: %s", body, traceback.format_exc())
+
+        # r = rs.get(on_message=pm, propagate=False)
+
+        def event_stream():
+            while True:
+                time.sleep(3)
+                print('event_stream')
+                yield 'data: interval\n\n'
+                # while events:
+                #     text = events.pop()
+                #     yield 'data: %s\n\n' % text
+                # yield 'data: interval'
+
+        return StreamingHttpResponse(event_stream(), content_type='text/event-stream')
```

## Comparing `xyz_common-0.1.5.dist-info/METADATA` & `xyz_common-0.1.6.dist-info/METADATA`

 * *Files 16% similar despite different names*

```diff
@@ -1,16 +1,15 @@
 Metadata-Version: 2.1
 Name: xyz-common
-Version: 0.1.5
+Version: 0.1.6
 Summary: common
 Home-page: https://github.com/szuprefix/py-xyz-common
 Author: szuprefix
 Author-email: szuprefix@126.com
 License: MIT
-Platform: UNKNOWN
 Classifier: Environment :: Web Environment
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Topic :: Text Processing :: Indexing
 Classifier: Topic :: Utilities
 Classifier: Topic :: Internet
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
@@ -20,10 +19,7 @@
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.5
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Requires-Dist: django (>=1.11.2)
 
-UNKNOWN
-
-
```

## Comparing `xyz_common-0.1.5.dist-info/RECORD` & `xyz_common-0.1.6.dist-info/RECORD`

 * *Files 13% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 xyz_common/__init__.py,sha256=8RHPSH4_WgexM0Ot0PUyxRDmCvCIHI4Iqhw_GljgP88,45
 xyz_common/admin.py,sha256=7s7DiBF_drxV-nRDR2NFeylMMV9EBbtM5QeL4JAT9cM,1763
-xyz_common/apis.py,sha256=7cIocwW7zApgpKorsLQiMgww90I9pkWJxztQhg1wzGk,1749
+xyz_common/apis.py,sha256=-BfOPaPFW4eu1uRaRYtsblc2SbM56BGXGxdq2ljdXEg,1809
 xyz_common/apps.py,sha256=HJJeq4M1D1Qz3rCfaCbhvJnasDLsE4Lq0uo4YhlC6zI,337
 xyz_common/consumers.py,sha256=7C0Nq2VPvE1aGgv24qoGJDubY3x-awIxf8b1d_tOsn8,1389
 xyz_common/helper.py,sha256=cA-y488jfHG24lubKNu-g8bvKxjFNcPAuGfwW8EkRxU,893
 xyz_common/models.py,sha256=lSHDi3VKzErCwbsmAYELqgj4_-0Yv9ByCzsShI3sk-s,4436
 xyz_common/receivers.py,sha256=EUGao1iXflCg0YFLPHu6Se5csfqbI_zK_ELunqG8wJQ,3188
 xyz_common/serializers.py,sha256=_stLaNkwnqga3hl-Ie_58IwlTXVXNPfS7gNJsCTUtxw,629
 xyz_common/signals.py,sha256=ItoFygOWSPf7ahIWXB5qxzbgkYWLyufMqZIEnyPQyRQ,407
-xyz_common/urls.py,sha256=gCv_Nkps4-2MhXx8we2cbqCJmpFhH06AHjAI2jAnWSc,208
-xyz_common/views.py,sha256=VisXE8dre4nOozbMWOMsLcr0qrg_ElovNHAnv4LSags,1582
+xyz_common/urls.py,sha256=iDp7o7bvHecDkxpx-ejN4q174hpwhOVFKpSJA_g5Nfk,244
+xyz_common/views.py,sha256=8Oe7Mph5E1neSelU_87eyKT4e2Mn3ECdHT129xvqDKg,3508
 xyz_common/migrations/0001_initial.py,sha256=uaYCe9DmcIwqIzaIPIWhrXQkP-XkrI52roePQdTZGO4,4701
 xyz_common/migrations/0002_auto_20200807_1912.py,sha256=uejzeqeVUEURegA6fKZt2gfvItLfXLKctLka3aKFcPk,1146
 xyz_common/migrations/0003_auto_20211216_2140.py,sha256=bQ7aIz_c05r3LGFJgxFa38GuF4DCvJcq2EG4-aiOeK4,526
 xyz_common/migrations/0004_auto_20220529_2210.py,sha256=3GuklPOUldK9WRRQEJB3U9ug2l9ufHv_b9Y_96j81YI,503
 xyz_common/migrations/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
-xyz_common-0.1.5.dist-info/METADATA,sha256=LBoPWr5DCe3cQ57HaZQC6-UCVBlfPKeyrmr3NBWKziw,955
-xyz_common-0.1.5.dist-info/WHEEL,sha256=g4nMs7d-Xl9-xC9XovUrsDHGXt-FT0E17Yqo92DEfvY,92
-xyz_common-0.1.5.dist-info/top_level.txt,sha256=eeCHjVTpP4CR6sbPgv6oLxH3cReF-qr4Tw-t4lRvUGM,11
-xyz_common-0.1.5.dist-info/RECORD,,
+xyz_common-0.1.6.dist-info/METADATA,sha256=GQ9QUDFQVPaOlznqnr3SmGmVb_viUId0Qo0JCRHZs2g,927
+xyz_common-0.1.6.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
+xyz_common-0.1.6.dist-info/top_level.txt,sha256=eeCHjVTpP4CR6sbPgv6oLxH3cReF-qr4Tw-t4lRvUGM,11
+xyz_common-0.1.6.dist-info/RECORD,,
```

