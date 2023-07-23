# Comparing `tmp/xyz_auth-0.1.8-py3-none-any.whl.zip` & `tmp/xyz_auth-0.1.9-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,23 +1,23 @@
-Zip file size: 15544 bytes, number of entries: 21
+Zip file size: 15548 bytes, number of entries: 21
 -rw-r--r--  2.0 unx      994 b- defN 20-Jun-25 21:49 xyz_auth/__init__.py
 -rw-r--r--  2.0 unx     1036 b- defN 22-May-08 09:56 xyz_auth/admins.py
 -rw-r--r--  2.0 unx     3180 b- defN 22-May-10 03:58 xyz_auth/apis.py
 -rw-r--r--  2.0 unx      327 b- defN 21-Jan-17 16:14 xyz_auth/apps.py
 -rw-r--r--  2.0 unx      870 b- defN 21-Jun-21 00:10 xyz_auth/auth_backends.py
 -rw-r--r--  2.0 unx      767 b- defN 22-May-08 09:56 xyz_auth/authentications.py
 -rw-r--r--  2.0 unx     1947 b- defN 21-Dec-29 18:10 xyz_auth/filters.py
--rw-r--r--  2.0 unx    15230 b- defN 22-Oct-21 03:21 xyz_auth/helper.py
+-rw-r--r--  2.0 unx    14580 b- defN 22-Oct-22 18:36 xyz_auth/helper.py
 -rw-r--r--  2.0 unx     1032 b- defN 22-May-08 09:57 xyz_auth/mixins.py
 -rw-r--r--  2.0 unx     1539 b- defN 22-May-08 09:53 xyz_auth/models.py
 -rw-r--r--  2.0 unx      828 b- defN 22-May-08 09:53 xyz_auth/permissions.py
 -rw-r--r--  2.0 unx      522 b- defN 22-Aug-02 23:53 xyz_auth/receivers.py
 -rw-r--r--  2.0 unx     2951 b- defN 20-Aug-07 03:40 xyz_auth/serializers.py
 -rw-r--r--  2.0 unx      396 b- defN 22-Aug-02 23:53 xyz_auth/signals.py
--rw-r--r--  2.0 unx     1292 b- defN 20-Aug-09 23:03 xyz_auth/stats.py
+-rw-r--r--  2.0 unx     1287 b- defN 22-Oct-22 07:43 xyz_auth/stats.py
 -rw-r--r--  2.0 unx     1391 b- defN 21-Jan-18 00:20 xyz_auth/migrations/0001_initial.py
 -rw-r--r--  2.0 unx        0 b- defN 21-Jan-18 00:20 xyz_auth/migrations/__init__.py
--rw-r--r--  2.0 unx      960 b- defN 22-Oct-21 04:23 xyz_auth-0.1.8.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 22-Oct-21 04:23 xyz_auth-0.1.8.dist-info/WHEEL
--rw-r--r--  2.0 unx        9 b- defN 22-Oct-21 04:23 xyz_auth-0.1.8.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     1624 b- defN 22-Oct-21 04:23 xyz_auth-0.1.8.dist-info/RECORD
-21 files, 36987 bytes uncompressed, 12934 bytes compressed:  65.0%
+-rw-r--r--  2.0 unx      960 b- defN 22-Oct-22 18:57 xyz_auth-0.1.9.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 22-Oct-22 18:57 xyz_auth-0.1.9.dist-info/WHEEL
+-rw-r--r--  2.0 unx        9 b- defN 22-Oct-22 18:57 xyz_auth-0.1.9.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx     1624 b- defN 22-Oct-22 18:57 xyz_auth-0.1.9.dist-info/RECORD
+21 files, 36332 bytes uncompressed, 12938 bytes compressed:  64.4%
```

## zipnote {}

```diff
@@ -45,20 +45,20 @@
 
 Filename: xyz_auth/migrations/0001_initial.py
 Comment: 
 
 Filename: xyz_auth/migrations/__init__.py
 Comment: 
 
-Filename: xyz_auth-0.1.8.dist-info/METADATA
+Filename: xyz_auth-0.1.9.dist-info/METADATA
 Comment: 
 
-Filename: xyz_auth-0.1.8.dist-info/WHEEL
+Filename: xyz_auth-0.1.9.dist-info/WHEEL
 Comment: 
 
-Filename: xyz_auth-0.1.8.dist-info/top_level.txt
+Filename: xyz_auth-0.1.9.dist-info/top_level.txt
 Comment: 
 
-Filename: xyz_auth-0.1.8.dist-info/RECORD
+Filename: xyz_auth-0.1.9.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## xyz_auth/helper.py

```diff
@@ -151,43 +151,23 @@
             return qset
         scope = d2.get('scope', {})
         if scope == '@all':
             return qset
 
         conds = []
         for fn, mnl in scope.items():
-            # print mn, mnl, fn, r
             field = m._meta.get_field(fn)
             if isinstance(mnl, string_types):
                 mnl = [mnl]
             if relation_limit and relation_limit in mnl:
                 mnl = [relation_limit]
             for mn2 in mnl:
-                # lookup = "%s__in" % fn
-                # if mn2 == 'auth.user':
-                #     lkd = {lookup: [user.id]}
-                # elif mn2 == r:
-                #     lkd = {lookup: [role.id]}
-                # else:
-                #     m2 = apps.get_model(mn2)
-                #     # print field
-                #     pqset = filter_query_set_for_user(mn2, user, scope_map=scope_map, relation_lookups=relation_lookups)
-                #     if isinstance(field, GenericForeignKey):
-                #         lookup = "%s__in" % field.fk_field
-                #         ids = list(pqset.values_list('id', flat=True))
-                #         lkd = {field.ct_field: ContentType.objects.get_for_model(m2), lookup: ids}
-                #     else:
-                #         mrfn = 'id'
-                #         if field.related_model != m2:
-                #             f = modelutils.get_model_related_field(m2, field.related_model)
-                #             mrfn = f.name
-                #         ids = list(pqset.values_list(mrfn, flat=True))
-                #         lkd = {lookup: ids}
-                cond = get_filter_cond_for_user_role(user, r, field, mn2, scope_map=scope_map,
-                                                     relation_lookups=relation_lookups)
+                cond = get_filter_cond_for_user_role(
+                    user, r, field, mn2, scope_map=scope_map, relation_lookups=relation_lookups
+                )
                 if cond:
                     conds.append(cond)
         conds = reduce_conds(conds) if conds else None
         if "filter" in d2:
             cond = Q(**d2['filter'])
             conds = cond if conds is None else conds & cond
         if conds:
@@ -202,38 +182,50 @@
             import traceback
             log.error('filter_query_set_for_user %s:%s error. %s', mn, role_conds, traceback.format_exc())
         return qset.distinct()
     return qset.none()
 
 
 def get_filter_cond_for_user_role(user, role_name, field, model_name, **kwargs):
-    lookup = "%s__in" % field.name
+    # lookup = "%s__in" % field.name
     if model_name == 'auth.user':
-        lkd = {lookup: [user.id]}
-    elif model_name == role_name:
-        lkd = {lookup: [getattr(user, role_name).id]}
+        return Q(**{field.name: user.id})
+    if model_name == role_name:
+        role = getattr(user, role_name)
+        return Q(**{field.name: role.id})
+        # rmname = role._meta.label_lower
+        # if rmname == field.model._meta.label_lower:
+        #     return Q(**{'id': role.id})
+        # model_name =
+    model = apps.get_model(model_name)
+    pqset = filter_query_set_for_user(model_name, user, **kwargs)
+    if isinstance(field, GenericForeignKey):
+        lookup = "%s__in" % field.fk_field
+        ids = list(pqset.values_list('id', flat=True))
+        if not ids:
+            return
+        return Q(**{field.ct_field: ContentType.objects.get_for_model(model), lookup: ids})
+
+    mrfn = 'id'
+    f = field
+    if f.related_model != model:
+        f = modelutils.get_model_related_field(model, field.related_model)
+        mrfn = f.name
+    ids = list(pqset.values_list(mrfn, flat=True))
+    if not ids:
+        return
+    # lkd = {lookup: ids}
+    if field.one_to_many:
+        return Q(**{'%s__in' % (f.related_query_name or f.related_name): ids})
     else:
-        model = apps.get_model(model_name)
-        pqset = filter_query_set_for_user(model_name, user, **kwargs)
-        if isinstance(field, GenericForeignKey):
-            lookup = "%s__in" % field.fk_field
-            ids = list(pqset.values_list('id', flat=True))
-            if not ids:
-                return
-            lkd = {field.ct_field: ContentType.objects.get_for_model(model), lookup: ids}
-        else:
-            mrfn = 'id'
-            if field.related_model != model:
-                f = modelutils.get_model_related_field(model, field.related_model)
-                mrfn = f.name
-            ids = list(pqset.values_list(mrfn, flat=True))
-            if not ids:
-                return
-            lkd = {lookup: ids}
-    return Q(**lkd)
+        # print(field.model, field.related_model)
+        f = modelutils.get_model_related_field(f.through, f.related_model)
+        lookup = {"%s__in" % f.name: ids}
+        mids = field.through.objects.filter(**lookup).values_list('%s_id' % field.model._meta.model_name, flat=True)
+        return Q(**{'id__in': list(mids)})
 
 
 def user_has_model_permission(model, user, action):
     from django.db.models import QuerySet
     if isinstance(model, QuerySet):
         model = model.model
     meta = model._meta
```

## xyz_auth/stats.py

```diff
@@ -5,16 +5,16 @@
 
 
 def stats_login(qset=None, measures=None, period=None):
     from xyz_common.models import Event
     qset = qset if qset is not None else Event.objects.filter(name__startswith='login')
     qset = statutils.using_stats_db(qset)
     dstat = statutils.DateStat(qset, 'create_time')
-    gm = {'login.wechat.mp.qrcode': u'电脑扫码', 'login.wechat.mp': u'微信公号', 'login.mobile': u'手机号', 'login': u'帐号密码',
-          'login.temptoken': u'临时密码'}
+    gm = {'login.wechat.mp.qrcode': '电脑扫码', 'login.wechat.mp': '微信公号', 'login.mobile': '手机号', 'login': '帐号密码',
+          'login.temptoken': '临时密码'}
     funcs = {
         'today': lambda: dstat.stat("今天", count_field="owner_id", distinct=True, only_first=True),
         'yesterday': lambda: dstat.stat("昨天", count_field="owner_id", distinct=True, only_first=True),
         'all': lambda: qset.values("owner_id").distinct().count(),
         'count': lambda: dstat.get_period_query_set(period).count(),
         'daily': lambda: dstat.stat(period, count_field='owner_id', distinct=True),
         'type': lambda: statutils.count_by(
```

## Comparing `xyz_auth-0.1.8.dist-info/METADATA` & `xyz_auth-0.1.9.dist-info/METADATA`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xyz-auth
-Version: 0.1.8
+Version: 0.1.9
 Summary: auth common api
 Home-page: https://github.com/szuprefix/py-xyz-auth
 Author: szuprefix
 Author-email: szuprefix@126.com
 License: MIT
 Platform: UNKNOWN
 Classifier: Environment :: Web Environment
```

## Comparing `xyz_auth-0.1.8.dist-info/RECORD` & `xyz_auth-0.1.9.dist-info/RECORD`

 * *Files 15% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 xyz_auth/__init__.py,sha256=TFsCPMB7U92TowCV-FzGRMTM9Rj0o7f78xBK47Eqf5E,994
 xyz_auth/admins.py,sha256=Il2uIg7O7LLXvU49GEQm7ICfN5NkQRSA_BDVLhXx57U,1036
 xyz_auth/apis.py,sha256=DZVo7mqlSYRye2X7HKgAhRcu7FC9vOAJx40xJHsZsqg,3180
 xyz_auth/apps.py,sha256=PZ9h_Qsyd4XAoZ3URY2S0slDrR8C00I4_k5FjucyV1E,327
 xyz_auth/auth_backends.py,sha256=E2en15Ly5TnsuZdvPxpPaGHhGnf17RLgh1XINZ1hb_M,870
 xyz_auth/authentications.py,sha256=FlAjAgfi_-hzVdR0DaQZOM0Lb4bmETzShlGO23q4SX0,767
 xyz_auth/filters.py,sha256=yhhNzC1bsXYeTrYRDGxx5OcN93pIAe2jWARBBEQw73g,1947
-xyz_auth/helper.py,sha256=HU7IFlA30mKHXPGccl9fPP_77Oi8u-ijt3xPBq5XaxA,15230
+xyz_auth/helper.py,sha256=fLGGlyQFNFRwll0vTP6gHt2RCYLjbyvchQHJAjjH4_o,14580
 xyz_auth/mixins.py,sha256=h6MDpVdXASbCRLO0OEG92BHCOdlMh4mg-1aOFek-gpw,1032
 xyz_auth/models.py,sha256=0_Q8gfzP6vmGpctR098ITmPL97tKVlMC1RHkMRIY5JI,1539
 xyz_auth/permissions.py,sha256=kjEcbkYi78NQrtek11TBwKtPgrj4nSVG9Ga1zoqciaY,828
 xyz_auth/receivers.py,sha256=IPQTUr9_pKsbfsQRhHuaT1uRoxnbhve-jcZ6s709onw,522
 xyz_auth/serializers.py,sha256=BltaxUOGZupfwDdVQ2ODrP-Zuoi5LqcWeiZDAx-CorY,2951
 xyz_auth/signals.py,sha256=A10HtYJmaj2hAPvxx6-r7aaQAm1X9x5LQAt8H9HqWtk,396
-xyz_auth/stats.py,sha256=iOeUcbs8WkcPQeMBUtxnYwAcbLu-afBR41GzYonpcks,1292
+xyz_auth/stats.py,sha256=WOYsNoYZWiYBs_YVRkm8YDyUwqWYyRqdR1R1_8JrSxA,1287
 xyz_auth/migrations/0001_initial.py,sha256=MNdPQG6dRPDyPMTinVOZ5EyjnU_grNvrtpR3pCz71L0,1391
 xyz_auth/migrations/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
-xyz_auth-0.1.8.dist-info/METADATA,sha256=6a_UZl5rHZUpBvTQ6k-bhJRrnU8xTmRhi_cvKEbHQEE,960
-xyz_auth-0.1.8.dist-info/WHEEL,sha256=g4nMs7d-Xl9-xC9XovUrsDHGXt-FT0E17Yqo92DEfvY,92
-xyz_auth-0.1.8.dist-info/top_level.txt,sha256=X59UUi8NgqEXuMfyRQxVCxN1fPe-Kocrk3yCs_51rqk,9
-xyz_auth-0.1.8.dist-info/RECORD,,
+xyz_auth-0.1.9.dist-info/METADATA,sha256=be4QnGcrjGuQ5e0I2tDMtiiUMi3BuiWeklcdUVO9qp4,960
+xyz_auth-0.1.9.dist-info/WHEEL,sha256=g4nMs7d-Xl9-xC9XovUrsDHGXt-FT0E17Yqo92DEfvY,92
+xyz_auth-0.1.9.dist-info/top_level.txt,sha256=X59UUi8NgqEXuMfyRQxVCxN1fPe-Kocrk3yCs_51rqk,9
+xyz_auth-0.1.9.dist-info/RECORD,,
```

