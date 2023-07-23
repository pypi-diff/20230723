# Comparing `tmp/dash_solana_components-1.0.1-py3-none-any.whl.zip` & `tmp/dash_solana_components-1.0.2-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,15 +1,13 @@
-Zip file size: 755461 bytes, number of entries: 13
--rw-r--r--  2.0 unx     1201 b- defN 23-Jul-23 04:39 dash_solana_components/App.py
--rw-r--r--  2.0 unx     1268 b- defN 23-Jul-23 04:39 dash_solana_components/DashSolanaComponents.py
--rw-r--r--  2.0 unx     1280 b- defN 23-Jul-23 05:44 dash_solana_components/SolanaWalletMultiButton.py
+Zip file size: 753851 bytes, number of entries: 11
+-rw-r--r--  2.0 unx     1124 b- defN 23-Jul-23 06:06 dash_solana_components/SolanaWalletMultiButton.py
 -rw-r--r--  2.0 unx     1582 b- defN 23-Jun-22 23:55 dash_solana_components/__init__.py
--rw-r--r--  2.0 unx      105 b- defN 23-Jul-23 05:44 dash_solana_components/_imports_.py
--rw-r--r--  2.0 unx  2481757 b- defN 23-Jul-23 05:31 dash_solana_components/dash_solana_components.js
--rw-r--r--  2.0 unx     1129 b- defN 23-Jul-23 05:44 dash_solana_components/metadata.json
--rw-r--r--  2.0 unx     1790 b- defN 23-Jul-23 05:44 dash_solana_components/package-info.json
--rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 05:44 dash_solana_components-1.0.1.dist-info/LICENSE
--rw-r--r--  2.0 unx      209 b- defN 23-Jul-23 05:44 dash_solana_components-1.0.1.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 05:44 dash_solana_components-1.0.1.dist-info/WHEEL
--rw-r--r--  2.0 unx       23 b- defN 23-Jul-23 05:44 dash_solana_components-1.0.1.dist-info/top_level.txt
--rw-rw-r--  2.0 unx     1232 b- defN 23-Jul-23 05:44 dash_solana_components-1.0.1.dist-info/RECORD
-13 files, 2491668 bytes uncompressed, 753349 bytes compressed:  69.8%
+-rw-r--r--  2.0 unx      105 b- defN 23-Jul-23 06:06 dash_solana_components/_imports_.py
+-rw-r--r--  2.0 unx  2481774 b- defN 23-Jul-23 06:03 dash_solana_components/dash_solana_components.js
+-rw-r--r--  2.0 unx     1227 b- defN 23-Jul-23 06:06 dash_solana_components/metadata.json
+-rw-r--r--  2.0 unx     1790 b- defN 23-Jul-23 06:06 dash_solana_components/package-info.json
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/LICENSE
+-rw-r--r--  2.0 unx      209 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/WHEEL
+-rw-r--r--  2.0 unx       23 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     1043 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/RECORD
+11 files, 2488969 bytes uncompressed, 752041 bytes compressed:  69.8%
```

## zipnote {}

```diff
@@ -1,13 +1,7 @@
-Filename: dash_solana_components/App.py
-Comment: 
-
-Filename: dash_solana_components/DashSolanaComponents.py
-Comment: 
-
 Filename: dash_solana_components/SolanaWalletMultiButton.py
 Comment: 
 
 Filename: dash_solana_components/__init__.py
 Comment: 
 
 Filename: dash_solana_components/_imports_.py
@@ -18,23 +12,23 @@
 
 Filename: dash_solana_components/metadata.json
 Comment: 
 
 Filename: dash_solana_components/package-info.json
 Comment: 
 
-Filename: dash_solana_components-1.0.1.dist-info/LICENSE
+Filename: dash_solana_components-1.0.2.dist-info/LICENSE
 Comment: 
 
-Filename: dash_solana_components-1.0.1.dist-info/METADATA
+Filename: dash_solana_components-1.0.2.dist-info/METADATA
 Comment: 
 
-Filename: dash_solana_components-1.0.1.dist-info/WHEEL
+Filename: dash_solana_components-1.0.2.dist-info/WHEEL
 Comment: 
 
-Filename: dash_solana_components-1.0.1.dist-info/top_level.txt
+Filename: dash_solana_components-1.0.2.dist-info/top_level.txt
 Comment: 
 
-Filename: dash_solana_components-1.0.1.dist-info/RECORD
+Filename: dash_solana_components-1.0.2.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## dash_solana_components/SolanaWalletMultiButton.py

```diff
@@ -8,29 +8,24 @@
 
 
 Keyword arguments:
 
 - id (string; optional):
     Unique ID to identify this component in Dash callbacks.
 
-- network (a value equal to: 'devnet', 'mainnet', 'testnet'; required)"""
+- network (a value equal to: 'devnet', 'mainnet', 'testnet'; default 'mainnet')"""
     _children_props = []
     _base_nodes = ['children']
     _namespace = 'dash_solana_components'
     _type = 'SolanaWalletMultiButton'
     @_explicitize_args
-    def __init__(self, network=Component.REQUIRED, id=Component.UNDEFINED, **kwargs):
+    def __init__(self, network=Component.UNDEFINED, id=Component.UNDEFINED, **kwargs):
         self._prop_names = ['id', 'network']
         self._valid_wildcard_attributes =            []
         self.available_properties = ['id', 'network']
         self.available_wildcard_properties =            []
         _explicit_args = kwargs.pop('_explicit_args')
         _locals = locals()
         _locals.update(kwargs)  # For wildcard attrs and excess named props
         args = {k: _locals[k] for k in _explicit_args}
 
-        for k in ['network']:
-            if k not in args:
-                raise TypeError(
-                    'Required argument `' + k + '` was not specified.')
-
         super(SolanaWalletMultiButton, self).__init__(**args)
```

## dash_solana_components/dash_solana_components.js

### js-beautify {}

```diff
@@ -64062,15 +64062,17 @@
                             n = f[r];
                         return d.default.createElement("div", {
                             id: e
                         }, d.default.createElement(g, {
                             network: n
                         }, d.default.createElement(y, null)))
                     };
-                p.defaultProps = {}, e.default = p;
+                p.defaultProps = {
+                    network: "mainnet"
+                }, e.default = p;
                 var g = function(t) {
                         var e = t.children,
                             r = t.network,
                             n = (0, d.useMemo)((function() {
                                 return (0, l.clusterApiUrl)(r)
                             }), [r]),
                             i = (0, d.useMemo)((function() {
```

## dash_solana_components/metadata.json

### Pretty-printed

 * *Similarity: 0.99609375%*

 * *Differences: {"'src/ts/components/SolanaWalletMultiButton.tsx'": "{'props': {'network': {'required': False, "*

 * *                                                    "'defaultValue': OrderedDict([('value', "*

 * *                                                    '"\'mainnet\'"), (\'computed\', False)])}}}'}*

```diff
@@ -9,16 +9,20 @@
                 "required": false,
                 "type": {
                     "name": "string",
                     "raw": "string"
                 }
             },
             "network": {
+                "defaultValue": {
+                    "computed": false,
+                    "value": "'mainnet'"
+                },
                 "description": "",
-                "required": true,
+                "required": false,
                 "type": {
                     "name": "enum",
                     "raw": "\"devnet\" | \"mainnet\" | \"testnet\"",
                     "value": [
                         {
                             "computed": false,
                             "value": "'devnet'"
```

## dash_solana_components/package-info.json

### Pretty-printed

 * *Similarity: 0.9615384615384616%*

 * *Differences: {"'version'": "'1.0.2'"}*

```diff
@@ -48,9 +48,9 @@
     "scripts": {
         "build": "npm run build:js && npm run build:backends",
         "build:backends": "dash-generate-components ./src/ts/components dash_solana_components -p package-info.json --r-prefix 'dsc' --jl-prefix 'dsc' --ignore \\.test\\.",
         "build:js": "webpack",
         "build:js::dev": "webpack --mode development",
         "watch": "npm run build:js::dev -- --watch"
     },
-    "version": "1.0.1"
+    "version": "1.0.2"
 }
```

## Comparing `dash_solana_components-1.0.1.dist-info/RECORD` & `dash_solana_components-1.0.2.dist-info/RECORD`

 * *Files 26% similar despite different names*

```diff
@@ -1,13 +1,11 @@
-dash_solana_components/App.py,sha256=cqB6WxcsZseIq6yLIF7WQSZI2uqFn-hNRAKOFWztq6Q,1201
-dash_solana_components/DashSolanaComponents.py,sha256=0S4m9cCSndt-rqjEiBUBNh8TXpRmaNjfUxv3ghiNw5o,1268
-dash_solana_components/SolanaWalletMultiButton.py,sha256=dsav-iKa40UdEmB1b0EIQFbtFe-ctU7JA88Yp8wUHI0,1280
+dash_solana_components/SolanaWalletMultiButton.py,sha256=sQ5CR1ymsFswkDPoZJcPUtF_iZPeZKAydqP4ibXEEeY,1124
 dash_solana_components/__init__.py,sha256=fmorU2H8dmwKKhifxQbrk74q5muWjedxZne_AmHBFrs,1582
 dash_solana_components/_imports_.py,sha256=tjgZ6BqflN9PQ1mS0j4tnlQkXzwT7jd2RPXGSB0V1I8,105
-dash_solana_components/dash_solana_components.js,sha256=8TrBBunNlL7c-XdnsrVyiwUTI_8IHEXQkeieqP8RZh8,2481757
-dash_solana_components/metadata.json,sha256=dP8q0eE8m-TzfTLjtVYPhOWK2zQmret6G6WtawmaMXo,1129
-dash_solana_components/package-info.json,sha256=uNT79L755K802F08fqQEVz-194aDmKE3Ehnoft2Ppk4,1790
-dash_solana_components-1.0.1.dist-info/LICENSE,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
-dash_solana_components-1.0.1.dist-info/METADATA,sha256=Y6mja1M4L3JfYTVeJWAj803dtLEUTusxJPu49so2ZFE,209
-dash_solana_components-1.0.1.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-dash_solana_components-1.0.1.dist-info/top_level.txt,sha256=9h2taIa9zNl2nHlWXExuUFRlEoBzfLs8p9-M8t5g9hk,23
-dash_solana_components-1.0.1.dist-info/RECORD,,
+dash_solana_components/dash_solana_components.js,sha256=2uquLz_PVFqgWyuV__VmVkC9ZUCIshoPiFl-MM3fOJs,2481774
+dash_solana_components/metadata.json,sha256=9KF8W9koh7Ys30oq7JLt0-YylnrrND9uCthepF5gsy0,1227
+dash_solana_components/package-info.json,sha256=GE8Ta2yVlcuGiFCSPPLtEsGjp1JcSHhp2He5XxNevC8,1790
+dash_solana_components-1.0.2.dist-info/LICENSE,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
+dash_solana_components-1.0.2.dist-info/METADATA,sha256=OUpH_J4q6onBYD4URuAbXimI5sg0GhwAkWQ6U2ShLa0,209
+dash_solana_components-1.0.2.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+dash_solana_components-1.0.2.dist-info/top_level.txt,sha256=9h2taIa9zNl2nHlWXExuUFRlEoBzfLs8p9-M8t5g9hk,23
+dash_solana_components-1.0.2.dist-info/RECORD,,
```

