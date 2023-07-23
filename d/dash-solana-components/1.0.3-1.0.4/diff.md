# Comparing `tmp/dash_solana_components-1.0.3-py3-none-any.whl.zip` & `tmp/dash_solana_components-1.0.4-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,13 +1,13 @@
-Zip file size: 753984 bytes, number of entries: 11
--rw-r--r--  2.0 unx     1261 b- defN 23-Jul-23 07:10 dash_solana_components/SolanaWalletMultiButton.py
+Zip file size: 753964 bytes, number of entries: 11
+-rw-r--r--  2.0 unx     1233 b- defN 23-Jul-23 07:48 dash_solana_components/SolanaWalletMultiButton.py
 -rw-r--r--  2.0 unx     1582 b- defN 23-Jun-22 23:55 dash_solana_components/__init__.py
--rw-r--r--  2.0 unx      105 b- defN 23-Jul-23 07:10 dash_solana_components/_imports_.py
--rw-r--r--  2.0 unx  2482033 b- defN 23-Jul-23 07:07 dash_solana_components/dash_solana_components.js
--rw-r--r--  2.0 unx     1497 b- defN 23-Jul-23 07:10 dash_solana_components/metadata.json
--rw-r--r--  2.0 unx     1790 b- defN 23-Jul-23 07:10 dash_solana_components/package-info.json
--rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/LICENSE
--rw-r--r--  2.0 unx      209 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/WHEEL
--rw-r--r--  2.0 unx       23 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/top_level.txt
--rw-rw-r--  2.0 unx     1043 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/RECORD
-11 files, 2489635 bytes uncompressed, 752174 bytes compressed:  69.8%
+-rw-r--r--  2.0 unx      105 b- defN 23-Jul-23 07:48 dash_solana_components/_imports_.py
+-rw-r--r--  2.0 unx  2481957 b- defN 23-Jul-23 07:45 dash_solana_components/dash_solana_components.js
+-rw-r--r--  2.0 unx     1450 b- defN 23-Jul-23 07:48 dash_solana_components/metadata.json
+-rw-r--r--  2.0 unx     1790 b- defN 23-Jul-23 07:48 dash_solana_components/package-info.json
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 07:48 dash_solana_components-1.0.4.dist-info/LICENSE
+-rw-r--r--  2.0 unx      209 b- defN 23-Jul-23 07:48 dash_solana_components-1.0.4.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 07:48 dash_solana_components-1.0.4.dist-info/WHEEL
+-rw-r--r--  2.0 unx       23 b- defN 23-Jul-23 07:48 dash_solana_components-1.0.4.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     1043 b- defN 23-Jul-23 07:48 dash_solana_components-1.0.4.dist-info/RECORD
+11 files, 2489484 bytes uncompressed, 752154 bytes compressed:  69.8%
```

## zipnote {}

```diff
@@ -12,23 +12,23 @@
 
 Filename: dash_solana_components/metadata.json
 Comment: 
 
 Filename: dash_solana_components/package-info.json
 Comment: 
 
-Filename: dash_solana_components-1.0.3.dist-info/LICENSE
+Filename: dash_solana_components-1.0.4.dist-info/LICENSE
 Comment: 
 
-Filename: dash_solana_components-1.0.3.dist-info/METADATA
+Filename: dash_solana_components-1.0.4.dist-info/METADATA
 Comment: 
 
-Filename: dash_solana_components-1.0.3.dist-info/WHEEL
+Filename: dash_solana_components-1.0.4.dist-info/WHEEL
 Comment: 
 
-Filename: dash_solana_components-1.0.3.dist-info/top_level.txt
+Filename: dash_solana_components-1.0.4.dist-info/top_level.txt
 Comment: 
 
-Filename: dash_solana_components-1.0.3.dist-info/RECORD
+Filename: dash_solana_components-1.0.4.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## dash_solana_components/SolanaWalletMultiButton.py

```diff
@@ -8,26 +8,26 @@
 
 
 Keyword arguments:
 
 - id (string; optional):
     Unique ID to identify this component in Dash callbacks.
 
-- initialPublicKeyState (string; optional)
+- network (a value equal to: 'devnet', 'mainnet', 'testnet'; default 'mainnet')
 
-- network (a value equal to: 'devnet', 'mainnet', 'testnet'; default 'mainnet')"""
+- publicKeyState (string; optional)"""
     _children_props = []
     _base_nodes = ['children']
     _namespace = 'dash_solana_components'
     _type = 'SolanaWalletMultiButton'
     @_explicitize_args
-    def __init__(self, network=Component.UNDEFINED, initialPublicKeyState=Component.UNDEFINED, id=Component.UNDEFINED, **kwargs):
-        self._prop_names = ['id', 'initialPublicKeyState', 'network']
+    def __init__(self, network=Component.UNDEFINED, publicKeyState=Component.UNDEFINED, id=Component.UNDEFINED, **kwargs):
+        self._prop_names = ['id', 'network', 'publicKeyState']
         self._valid_wildcard_attributes =            []
-        self.available_properties = ['id', 'initialPublicKeyState', 'network']
+        self.available_properties = ['id', 'network', 'publicKeyState']
         self.available_wildcard_properties =            []
         _explicit_args = kwargs.pop('_explicit_args')
         _locals = locals()
         _locals.update(kwargs)  # For wildcard attrs and excess named props
         args = {k: _locals[k] for k in _explicit_args}
 
         super(SolanaWalletMultiButton, self).__init__(**args)
```

## dash_solana_components/dash_solana_components.js

### js-beautify {}

```diff
@@ -41850,15 +41850,15 @@
                 r.d(e, {
                     Z: () => a
                 });
                 var n = r(8081),
                     i = r.n(n),
                     o = r(23645),
                     s = r.n(o)()(i());
-                s.push([t.id, ".SolanaWalletMultiButton {\n  min-height: 100vh;\n  display: flex;\n  justify-content: center;\n  align-items: center;\n}", ""]);
+                s.push([t.id, ".SampleCSS {\n  display: flex;\n  justify-content: center;\n  align-items: center;\n}", ""]);
                 const a = s
             },
             23645: t => {
                 "use strict";
                 t.exports = function(t) {
                     var e = [];
                     return e.toString = function() {
@@ -64055,33 +64055,33 @@
                         devnet: s.WalletAdapterNetwork.Devnet,
                         mainnet: s.WalletAdapterNetwork.Mainnet,
                         testnet: s.WalletAdapterNetwork.Testnet
                     },
                     p = function(t) {
                         var e = t.id,
                             r = t.network,
-                            n = t.initialPublicKeyState,
+                            n = t.setProps,
                             i = f[r],
-                            o = (0, d.useState)(n),
-                            s = (o[0], o[1]),
-                            a = function(t) {
-                                s(t)
+                            o = function(t) {
+                                n && n({
+                                    publicKeyState: t
+                                })
                             };
                         return d.default.createElement("div", {
                             id: e
                         }, d.default.createElement(g, {
                             network: i,
-                            onPublicKeyUpdate: a
+                            onPublicKeyUpdate: o
                         }, d.default.createElement(y, {
-                            onPublicKeyUpdate: a
+                            onPublicKeyUpdate: o
                         })))
                     };
                 p.defaultProps = {
                     network: "mainnet",
-                    initialPublicKeyState: null
+                    PublicKeyState: null
                 }, e.default = p;
                 var g = function(t) {
                         t.children;
                         var e = t.network,
                             r = t.onPublicKeyUpdate,
                             n = (0, d.useMemo)((function() {
                                 return (0, l.clusterApiUrl)(e)
@@ -64101,18 +64101,18 @@
                     y = function(t) {
                         var e = t.onPublicKeyUpdate,
                             r = (0, h.useWallet)(),
                             n = r.publicKey,
                             i = r.connected;
                         return (0, d.useEffect)((function() {
                             if (i) {
-                                var t = (null == n ? void 0 : n.toString()) || null;
+                                var t = null == n ? void 0 : n.toString();
                                 console.log(t), e(t)
                             }
-                        }), [i, n]), d.default.createElement("div", {
+                        }), [i, n, e]), d.default.createElement("div", {
                             className: "SolanaWalletMultiButton"
                         }, d.default.createElement(c.WalletMultiButton, null))
                     }
             },
             39294: function(t, e, r) {
                 "use strict";
                 var n = this && this.__importDefault || function(t) {
```

## dash_solana_components/metadata.json

### Pretty-printed

 * *Similarity: 0.9747395833333333%*

 * *Differences: {"'src/ts/components/SolanaWalletMultiButton.tsx'": "{'props': {'setProps': {'type': {'raw': "*

 * *                                                    "'((props: { publicKeyState?: string; }) => "*

 * *                                                    'void) & ((props: Record<string, any>) => '*

 * *                                                    "void)'}}, 'publicKeyState': "*

 * *                                                    "OrderedDict([('description', ''), "*

 * *                                                    […]*

```diff
@@ -8,26 +8,14 @@
                 "description": "Unique ID to identify this component in Dash callbacks.",
                 "required": false,
                 "type": {
                     "name": "string",
                     "raw": "string"
                 }
             },
-            "initialPublicKeyState": {
-                "defaultValue": {
-                    "computed": false,
-                    "value": "null"
-                },
-                "description": "",
-                "required": false,
-                "type": {
-                    "name": "string",
-                    "raw": "string"
-                }
-            },
             "network": {
                 "defaultValue": {
                     "computed": false,
                     "value": "'mainnet'"
                 },
                 "description": "",
                 "required": false,
@@ -46,18 +34,26 @@
                         {
                             "computed": false,
                             "value": "'testnet'"
                         }
                     ]
                 }
             },
+            "publicKeyState": {
+                "description": "",
+                "required": false,
+                "type": {
+                    "name": "string",
+                    "raw": "string"
+                }
+            },
             "setProps": {
                 "description": "Update props to trigger callbacks.",
                 "required": true,
                 "type": {
                     "name": "func",
-                    "raw": "(props: Record<string, any>) => void"
+                    "raw": "((props: { publicKeyState?: string; }) => void) & ((props: Record<string, any>) => void)"
                 }
             }
         }
     }
 }
```

## dash_solana_components/package-info.json

### Pretty-printed

 * *Similarity: 0.9615384615384616%*

 * *Differences: {"'version'": "'1.0.4'"}*

```diff
@@ -48,9 +48,9 @@
     "scripts": {
         "build": "npm run build:js && npm run build:backends",
         "build:backends": "dash-generate-components ./src/ts/components dash_solana_components -p package-info.json --r-prefix 'dsc' --jl-prefix 'dsc' --ignore \\.test\\.",
         "build:js": "webpack",
         "build:js::dev": "webpack --mode development",
         "watch": "npm run build:js::dev -- --watch"
     },
-    "version": "1.0.3"
+    "version": "1.0.4"
 }
```

## Comparing `dash_solana_components-1.0.3.dist-info/RECORD` & `dash_solana_components-1.0.4.dist-info/RECORD`

 * *Files 14% similar despite different names*

```diff
@@ -1,11 +1,11 @@
-dash_solana_components/SolanaWalletMultiButton.py,sha256=IfIxADHAV8ySHpA-gt07YwKvBFDS5kO0N_HiP7GqDU0,1261
+dash_solana_components/SolanaWalletMultiButton.py,sha256=VSVRulJuO_kx1rEKUQLHwxmiNPyvyY4cR42iRJIBgXw,1233
 dash_solana_components/__init__.py,sha256=fmorU2H8dmwKKhifxQbrk74q5muWjedxZne_AmHBFrs,1582
 dash_solana_components/_imports_.py,sha256=tjgZ6BqflN9PQ1mS0j4tnlQkXzwT7jd2RPXGSB0V1I8,105
-dash_solana_components/dash_solana_components.js,sha256=To5djhOlNqTPXjh2rqp23Jjn5xIwyQ2oZfZNxLZIEhE,2482033
-dash_solana_components/metadata.json,sha256=_cdDoJcCfeICQnxkGU0omeFnEnJXY8Y1YsTYlHwCtV8,1497
-dash_solana_components/package-info.json,sha256=giAlonof-Hk3MNqRcNH_mhCvnIqhK9XvjqdqyNsrtWs,1790
-dash_solana_components-1.0.3.dist-info/LICENSE,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
-dash_solana_components-1.0.3.dist-info/METADATA,sha256=_NxlXZxjAll5prtb4TQFCh6FHfWBQGk2bkyy_e9GlRA,209
-dash_solana_components-1.0.3.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-dash_solana_components-1.0.3.dist-info/top_level.txt,sha256=9h2taIa9zNl2nHlWXExuUFRlEoBzfLs8p9-M8t5g9hk,23
-dash_solana_components-1.0.3.dist-info/RECORD,,
+dash_solana_components/dash_solana_components.js,sha256=fF0VceuPb0-neukzGcRU31oeQiASo8pg9iW1C7l1wYE,2481957
+dash_solana_components/metadata.json,sha256=ezAIwxKRFbczD3UfICrgzYcJ79uO56kmkWG1oBQ6zR8,1450
+dash_solana_components/package-info.json,sha256=ULERybgqnePFoQEesOCNIZr2fml4mBmHznriVCh69rg,1790
+dash_solana_components-1.0.4.dist-info/LICENSE,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
+dash_solana_components-1.0.4.dist-info/METADATA,sha256=mjkNUqXtDUdVNNAmESIH1ABUFJr8sMubl3BryZ33oYg,209
+dash_solana_components-1.0.4.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+dash_solana_components-1.0.4.dist-info/top_level.txt,sha256=9h2taIa9zNl2nHlWXExuUFRlEoBzfLs8p9-M8t5g9hk,23
+dash_solana_components-1.0.4.dist-info/RECORD,,
```

