# Comparing `tmp/dash_solana_components-1.0.2-py3-none-any.whl.zip` & `tmp/dash_solana_components-1.0.3-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,13 +1,13 @@
-Zip file size: 753851 bytes, number of entries: 11
--rw-r--r--  2.0 unx     1124 b- defN 23-Jul-23 06:06 dash_solana_components/SolanaWalletMultiButton.py
+Zip file size: 753984 bytes, number of entries: 11
+-rw-r--r--  2.0 unx     1261 b- defN 23-Jul-23 07:10 dash_solana_components/SolanaWalletMultiButton.py
 -rw-r--r--  2.0 unx     1582 b- defN 23-Jun-22 23:55 dash_solana_components/__init__.py
--rw-r--r--  2.0 unx      105 b- defN 23-Jul-23 06:06 dash_solana_components/_imports_.py
--rw-r--r--  2.0 unx  2481774 b- defN 23-Jul-23 06:03 dash_solana_components/dash_solana_components.js
--rw-r--r--  2.0 unx     1227 b- defN 23-Jul-23 06:06 dash_solana_components/metadata.json
--rw-r--r--  2.0 unx     1790 b- defN 23-Jul-23 06:06 dash_solana_components/package-info.json
--rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/LICENSE
--rw-r--r--  2.0 unx      209 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/WHEEL
--rw-r--r--  2.0 unx       23 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/top_level.txt
--rw-rw-r--  2.0 unx     1043 b- defN 23-Jul-23 06:06 dash_solana_components-1.0.2.dist-info/RECORD
-11 files, 2488969 bytes uncompressed, 752041 bytes compressed:  69.8%
+-rw-r--r--  2.0 unx      105 b- defN 23-Jul-23 07:10 dash_solana_components/_imports_.py
+-rw-r--r--  2.0 unx  2482033 b- defN 23-Jul-23 07:07 dash_solana_components/dash_solana_components.js
+-rw-r--r--  2.0 unx     1497 b- defN 23-Jul-23 07:10 dash_solana_components/metadata.json
+-rw-r--r--  2.0 unx     1790 b- defN 23-Jul-23 07:10 dash_solana_components/package-info.json
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/LICENSE
+-rw-r--r--  2.0 unx      209 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/WHEEL
+-rw-r--r--  2.0 unx       23 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     1043 b- defN 23-Jul-23 07:10 dash_solana_components-1.0.3.dist-info/RECORD
+11 files, 2489635 bytes uncompressed, 752174 bytes compressed:  69.8%
```

## zipnote {}

```diff
@@ -12,23 +12,23 @@
 
 Filename: dash_solana_components/metadata.json
 Comment: 
 
 Filename: dash_solana_components/package-info.json
 Comment: 
 
-Filename: dash_solana_components-1.0.2.dist-info/LICENSE
+Filename: dash_solana_components-1.0.3.dist-info/LICENSE
 Comment: 
 
-Filename: dash_solana_components-1.0.2.dist-info/METADATA
+Filename: dash_solana_components-1.0.3.dist-info/METADATA
 Comment: 
 
-Filename: dash_solana_components-1.0.2.dist-info/WHEEL
+Filename: dash_solana_components-1.0.3.dist-info/WHEEL
 Comment: 
 
-Filename: dash_solana_components-1.0.2.dist-info/top_level.txt
+Filename: dash_solana_components-1.0.3.dist-info/top_level.txt
 Comment: 
 
-Filename: dash_solana_components-1.0.2.dist-info/RECORD
+Filename: dash_solana_components-1.0.3.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## dash_solana_components/SolanaWalletMultiButton.py

```diff
@@ -8,24 +8,26 @@
 
 
 Keyword arguments:
 
 - id (string; optional):
     Unique ID to identify this component in Dash callbacks.
 
+- initialPublicKeyState (string; optional)
+
 - network (a value equal to: 'devnet', 'mainnet', 'testnet'; default 'mainnet')"""
     _children_props = []
     _base_nodes = ['children']
     _namespace = 'dash_solana_components'
     _type = 'SolanaWalletMultiButton'
     @_explicitize_args
-    def __init__(self, network=Component.UNDEFINED, id=Component.UNDEFINED, **kwargs):
-        self._prop_names = ['id', 'network']
+    def __init__(self, network=Component.UNDEFINED, initialPublicKeyState=Component.UNDEFINED, id=Component.UNDEFINED, **kwargs):
+        self._prop_names = ['id', 'initialPublicKeyState', 'network']
         self._valid_wildcard_attributes =            []
-        self.available_properties = ['id', 'network']
+        self.available_properties = ['id', 'initialPublicKeyState', 'network']
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
@@ -64055,47 +64055,64 @@
                         devnet: s.WalletAdapterNetwork.Devnet,
                         mainnet: s.WalletAdapterNetwork.Mainnet,
                         testnet: s.WalletAdapterNetwork.Testnet
                     },
                     p = function(t) {
                         var e = t.id,
                             r = t.network,
-                            n = f[r];
+                            n = t.initialPublicKeyState,
+                            i = f[r],
+                            o = (0, d.useState)(n),
+                            s = (o[0], o[1]),
+                            a = function(t) {
+                                s(t)
+                            };
                         return d.default.createElement("div", {
                             id: e
                         }, d.default.createElement(g, {
-                            network: n
-                        }, d.default.createElement(y, null)))
+                            network: i,
+                            onPublicKeyUpdate: a
+                        }, d.default.createElement(y, {
+                            onPublicKeyUpdate: a
+                        })))
                     };
                 p.defaultProps = {
-                    network: "mainnet"
+                    network: "mainnet",
+                    initialPublicKeyState: null
                 }, e.default = p;
                 var g = function(t) {
-                        var e = t.children,
-                            r = t.network,
+                        t.children;
+                        var e = t.network,
+                            r = t.onPublicKeyUpdate,
                             n = (0, d.useMemo)((function() {
-                                return (0, l.clusterApiUrl)(r)
-                            }), [r]),
+                                return (0, l.clusterApiUrl)(e)
+                            }), [e]),
                             i = (0, d.useMemo)((function() {
                                 return [new u.PhantomWalletAdapter, new u.SolflareWalletAdapter, new u.BackpackWalletAdapter, new u.LedgerWalletAdapter]
-                            }), [r]);
+                            }), [e]);
                         return d.default.createElement(a.ConnectionProvider, {
                             endpoint: n
                         }, d.default.createElement(a.WalletProvider, {
                             wallets: i,
                             autoConnect: !0
-                        }, d.default.createElement(c.WalletModalProvider, null, e)))
+                        }, d.default.createElement(c.WalletModalProvider, null, d.default.createElement(y, {
+                            onPublicKeyUpdate: r
+                        }))))
                     },
-                    y = function() {
-                        var t = (0, h.useWallet)(),
-                            e = t.publicKey,
-                            r = t.connected;
+                    y = function(t) {
+                        var e = t.onPublicKeyUpdate,
+                            r = (0, h.useWallet)(),
+                            n = r.publicKey,
+                            i = r.connected;
                         return (0, d.useEffect)((function() {
-                            r && console.log(null == e ? void 0 : e.toString())
-                        }), [r, e]), d.default.createElement("div", {
+                            if (i) {
+                                var t = (null == n ? void 0 : n.toString()) || null;
+                                console.log(t), e(t)
+                            }
+                        }), [i, n]), d.default.createElement("div", {
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

 * *Similarity: 0.984375%*

 * *Differences: {"'src/ts/components/SolanaWalletMultiButton.tsx'": "{'props': {'initialPublicKeyState': "*

 * *                                                    "OrderedDict([('description', ''), "*

 * *                                                    "('required', False), ('defaultValue', "*

 * *                                                    "OrderedDict([('value', 'null'), ('computed', "*

 * *                                                    "False)])), ('type', OrderedDict([('name', "*

 * *                                           […]*

```diff
@@ -8,14 +8,26 @@
                 "description": "Unique ID to identify this component in Dash callbacks.",
                 "required": false,
                 "type": {
                     "name": "string",
                     "raw": "string"
                 }
             },
+            "initialPublicKeyState": {
+                "defaultValue": {
+                    "computed": false,
+                    "value": "null"
+                },
+                "description": "",
+                "required": false,
+                "type": {
+                    "name": "string",
+                    "raw": "string"
+                }
+            },
             "network": {
                 "defaultValue": {
                     "computed": false,
                     "value": "'mainnet'"
                 },
                 "description": "",
                 "required": false,
```

## dash_solana_components/package-info.json

### Pretty-printed

 * *Similarity: 0.9615384615384616%*

 * *Differences: {"'version'": "'1.0.3'"}*

```diff
@@ -48,9 +48,9 @@
     "scripts": {
         "build": "npm run build:js && npm run build:backends",
         "build:backends": "dash-generate-components ./src/ts/components dash_solana_components -p package-info.json --r-prefix 'dsc' --jl-prefix 'dsc' --ignore \\.test\\.",
         "build:js": "webpack",
         "build:js::dev": "webpack --mode development",
         "watch": "npm run build:js::dev -- --watch"
     },
-    "version": "1.0.2"
+    "version": "1.0.3"
 }
```

## Comparing `dash_solana_components-1.0.2.dist-info/RECORD` & `dash_solana_components-1.0.3.dist-info/RECORD`

 * *Files 18% similar despite different names*

```diff
@@ -1,11 +1,11 @@
-dash_solana_components/SolanaWalletMultiButton.py,sha256=sQ5CR1ymsFswkDPoZJcPUtF_iZPeZKAydqP4ibXEEeY,1124
+dash_solana_components/SolanaWalletMultiButton.py,sha256=IfIxADHAV8ySHpA-gt07YwKvBFDS5kO0N_HiP7GqDU0,1261
 dash_solana_components/__init__.py,sha256=fmorU2H8dmwKKhifxQbrk74q5muWjedxZne_AmHBFrs,1582
 dash_solana_components/_imports_.py,sha256=tjgZ6BqflN9PQ1mS0j4tnlQkXzwT7jd2RPXGSB0V1I8,105
-dash_solana_components/dash_solana_components.js,sha256=2uquLz_PVFqgWyuV__VmVkC9ZUCIshoPiFl-MM3fOJs,2481774
-dash_solana_components/metadata.json,sha256=9KF8W9koh7Ys30oq7JLt0-YylnrrND9uCthepF5gsy0,1227
-dash_solana_components/package-info.json,sha256=GE8Ta2yVlcuGiFCSPPLtEsGjp1JcSHhp2He5XxNevC8,1790
-dash_solana_components-1.0.2.dist-info/LICENSE,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
-dash_solana_components-1.0.2.dist-info/METADATA,sha256=OUpH_J4q6onBYD4URuAbXimI5sg0GhwAkWQ6U2ShLa0,209
-dash_solana_components-1.0.2.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-dash_solana_components-1.0.2.dist-info/top_level.txt,sha256=9h2taIa9zNl2nHlWXExuUFRlEoBzfLs8p9-M8t5g9hk,23
-dash_solana_components-1.0.2.dist-info/RECORD,,
+dash_solana_components/dash_solana_components.js,sha256=To5djhOlNqTPXjh2rqp23Jjn5xIwyQ2oZfZNxLZIEhE,2482033
+dash_solana_components/metadata.json,sha256=_cdDoJcCfeICQnxkGU0omeFnEnJXY8Y1YsTYlHwCtV8,1497
+dash_solana_components/package-info.json,sha256=giAlonof-Hk3MNqRcNH_mhCvnIqhK9XvjqdqyNsrtWs,1790
+dash_solana_components-1.0.3.dist-info/LICENSE,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
+dash_solana_components-1.0.3.dist-info/METADATA,sha256=_NxlXZxjAll5prtb4TQFCh6FHfWBQGk2bkyy_e9GlRA,209
+dash_solana_components-1.0.3.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+dash_solana_components-1.0.3.dist-info/top_level.txt,sha256=9h2taIa9zNl2nHlWXExuUFRlEoBzfLs8p9-M8t5g9hk,23
+dash_solana_components-1.0.3.dist-info/RECORD,,
```

