# Comparing `tmp/jssp_tool-1.0.5-py3-none-any.whl.zip` & `tmp/jssp_tool-1.0.6-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,8 +1,8 @@
-Zip file size: 34849 bytes, number of entries: 48
+Zip file size: 34728 bytes, number of entries: 48
 -rw-r--r--  2.0 unx     3917 b- defN 23-Jul-23 00:17 examples/gnn_dispatch/Params.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 00:17 examples/gnn_dispatch/__init__.py
 -rw-r--r--  2.0 unx      187 b- defN 23-Jul-23 00:17 examples/gnn_dispatch/global_util.py
 -rw-r--r--  2.0 unx      927 b- defN 23-Jul-23 00:17 examples/gnn_dispatch/my_memory.py
 -rw-r--r--  2.0 unx     4674 b- defN 23-Jul-23 00:17 examples/gnn_dispatch/runner.py
 -rw-r--r--  2.0 unx     1908 b- defN 23-Jul-23 00:17 examples/gnn_dispatch/train_ppo.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 00:17 examples/gnn_dispatch/env/__init__.py
@@ -18,19 +18,19 @@
 -rw-r--r--  2.0 unx      488 b- defN 23-Jul-23 00:17 jssp_tool/env/util/config_util.py
 -rw-r--r--  2.0 unx      771 b- defN 23-Jul-23 00:17 jssp_tool/env/util/random_util.py
 -rw-r--r--  2.0 unx      245 b- defN 23-Jul-23 00:17 jssp_tool/env/util/time_util.py
 -rw-r--r--  2.0 unx      285 b- defN 23-Jul-23 00:17 jssp_tool/env/util/torch_util.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 00:17 jssp_tool/plotter/__init__.py
 -rw-r--r--  2.0 unx     1472 b- defN 23-Jul-23 00:17 jssp_tool/plotter/gantt_plot.py
 -rw-r--r--  2.0 unx     3406 b- defN 23-Jul-23 00:17 jssp_tool/plotter/network_plot.py
--rw-r--r--  2.0 unx       19 b- defN 23-Jul-23 00:17 jssp_tool/rl/__init__.py
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 00:22 jssp_tool/rl/__init__.py
 -rw-r--r--  2.0 unx       38 b- defN 23-Jul-23 00:17 jssp_tool/rl/agent/__init__.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 00:17 jssp_tool/rl/agent/dqn/__init__.py
 -rw-r--r--  2.0 unx     5000 b- defN 23-Jul-23 00:17 jssp_tool/rl/agent/dqn/ddqn.py
--rw-r--r--  2.0 unx       52 b- defN 23-Jul-23 00:17 jssp_tool/rl/agent/ppo/__init__.py
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 00:22 jssp_tool/rl/agent/ppo/__init__.py
 -rw-r--r--  2.0 unx     2576 b- defN 23-Jul-23 00:18 jssp_tool/rl/agent/ppo/memory.py
 -rw-r--r--  2.0 unx     4641 b- defN 23-Jul-23 00:17 jssp_tool/rl/agent/ppo/ppo_base.py
 -rw-r--r--  2.0 unx      702 b- defN 23-Jul-23 00:17 jssp_tool/rl/agent/ppo/ppo_discrete.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 00:17 jssp_tool/rl/epsilon_strategy/__init__.py
 -rw-r--r--  2.0 unx      518 b- defN 23-Jul-23 00:17 jssp_tool/rl/epsilon_strategy/linear_decay.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 00:17 jssp_tool/rl/replay_buffer/__init__.py
 -rw-r--r--  2.0 unx     1993 b- defN 23-Jul-23 00:17 jssp_tool/rl/replay_buffer/replay_buffer.py
@@ -39,12 +39,12 @@
 -rw-r--r--  2.0 unx      843 b- defN 23-Jul-23 00:17 jssp_tool/rl/replay_buffer/a/random.py
 -rw-r--r--  2.0 unx     9304 b- defN 23-Jul-23 00:17 jssp_tool/rl/replay_buffer/a/sum_tree.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 00:17 jssp_tool/rl/replay_buffer/priority/__init__.py
 -rw-r--r--  2.0 unx     3461 b- defN 23-Jul-23 00:17 jssp_tool/rl/replay_buffer/priority/priority_replay_buffer.py
 -rw-r--r--  2.0 unx     2091 b- defN 23-Jul-23 00:17 jssp_tool/rl/replay_buffer/priority/sum_tree.py
 -rw-r--r--  2.0 unx       22 b- defN 23-Jul-23 00:17 jssp_tool/util/__init__.py
 -rw-r--r--  2.0 unx     7906 b- defN 23-Jul-23 00:17 jssp_tool/util/logger.py
--rw-r--r--  2.0 unx      318 b- defN 23-Jul-23 00:18 jssp_tool-1.0.5.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 00:18 jssp_tool-1.0.5.dist-info/WHEEL
--rw-r--r--  2.0 unx       19 b- defN 23-Jul-23 00:18 jssp_tool-1.0.5.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     4293 b- defN 23-Jul-23 00:18 jssp_tool-1.0.5.dist-info/RECORD
-48 files, 85115 bytes uncompressed, 27849 bytes compressed:  67.3%
+-rw-r--r--  2.0 unx      318 b- defN 23-Jul-23 00:22 jssp_tool-1.0.6.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 00:22 jssp_tool-1.0.6.dist-info/WHEEL
+-rw-r--r--  2.0 unx       19 b- defN 23-Jul-23 00:22 jssp_tool-1.0.6.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx     4291 b- defN 23-Jul-23 00:22 jssp_tool-1.0.6.dist-info/RECORD
+48 files, 85042 bytes uncompressed, 27728 bytes compressed:  67.4%
```

## zipnote {}

```diff
@@ -126,20 +126,20 @@
 
 Filename: jssp_tool/util/__init__.py
 Comment: 
 
 Filename: jssp_tool/util/logger.py
 Comment: 
 
-Filename: jssp_tool-1.0.5.dist-info/METADATA
+Filename: jssp_tool-1.0.6.dist-info/METADATA
 Comment: 
 
-Filename: jssp_tool-1.0.5.dist-info/WHEEL
+Filename: jssp_tool-1.0.6.dist-info/WHEEL
 Comment: 
 
-Filename: jssp_tool-1.0.5.dist-info/top_level.txt
+Filename: jssp_tool-1.0.6.dist-info/top_level.txt
 Comment: 
 
-Filename: jssp_tool-1.0.5.dist-info/RECORD
+Filename: jssp_tool-1.0.6.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## jssp_tool/rl/__init__.py

```diff
@@ -1,2 +0,0 @@
-00000000: 6672 6f6d 202e 7070 6f20 696d 706f 7274  from .ppo import
-00000010: 202a 0a                                   *.
```

## jssp_tool/rl/agent/ppo/__init__.py

```diff
@@ -1,4 +0,0 @@
-00000000: 6672 6f6d 202e 7070 6f5f 6261 7365 2069  from .ppo_base i
-00000010: 6d70 6f72 7420 2a0a 6672 6f6d 202e 7070  mport *.from .pp
-00000020: 6f5f 6469 7363 7265 7465 2069 6d70 6f72  o_discrete impor
-00000030: 7420 2a0a                                t *.
```

## Comparing `jssp_tool-1.0.5.dist-info/RECORD` & `jssp_tool-1.0.6.dist-info/RECORD`

 * *Files 6% similar despite different names*

```diff
@@ -17,19 +17,19 @@
 jssp_tool/env/util/config_util.py,sha256=KEj0R1copDZl7U5xIMAbPJnc5jQZ0tOc76CK4tB5r9I,488
 jssp_tool/env/util/random_util.py,sha256=8ra62zF0yIdTmR92jBsmvKw2Try8On-4QtdJTJCDYbo,771
 jssp_tool/env/util/time_util.py,sha256=_uZztM7QsueAW0Z00mraZ_R4edZtjudLX1fovkobCMM,245
 jssp_tool/env/util/torch_util.py,sha256=BuUBPXFW3m0kAarGc_b8_u9EkRQq0K2Nmgp5UGWpMgE,285
 jssp_tool/plotter/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 jssp_tool/plotter/gantt_plot.py,sha256=favz25YIAQgnRPSvP9nmiPCjjYvmMaPPyVn9atwa1T4,1472
 jssp_tool/plotter/network_plot.py,sha256=-1hBAh6mjg0rtJQwjNkS5-Q_SXTcxMC3Krwoyjno2Uk,3406
-jssp_tool/rl/__init__.py,sha256=MvJ4IPBnyvmp4PIfVqYrkD2mBk0f3gWf4ANWzgHBVo8,19
+jssp_tool/rl/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 jssp_tool/rl/agent/__init__.py,sha256=N0GF3fveRLtaP7Jw_-QhUjzm26ME4DM388vcez-5u8A,38
 jssp_tool/rl/agent/dqn/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 jssp_tool/rl/agent/dqn/ddqn.py,sha256=w9sDEpylftkBeHqQPXmxK6EDhznnij-8IpkiyFvOD6Y,5000
-jssp_tool/rl/agent/ppo/__init__.py,sha256=KF-5f-SLPr6SEqv-QFpa__Ay2OY9tt5z8LK4qCAiDu4,52
+jssp_tool/rl/agent/ppo/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 jssp_tool/rl/agent/ppo/memory.py,sha256=vb5iaMckgIc25HOLR4UKVSbx3wS1X3OQTlST--3CjWg,2576
 jssp_tool/rl/agent/ppo/ppo_base.py,sha256=n0E_TenVZRavq3Efc-wHLwykViMKcBBRmuMlffAMzhg,4641
 jssp_tool/rl/agent/ppo/ppo_discrete.py,sha256=cCxau2iyMtMA2MoDydRXXPVUyrIQDsJ35ScOfIvbSYo,702
 jssp_tool/rl/epsilon_strategy/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 jssp_tool/rl/epsilon_strategy/linear_decay.py,sha256=Kwvj6A2KFgH4H2XD0Hcyq0S9bLiCc3CnVt61eP13u-o,518
 jssp_tool/rl/replay_buffer/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 jssp_tool/rl/replay_buffer/replay_buffer.py,sha256=50If2W_rM8F7bjYutFr9ynqJ1Nl0FZgxxyLhfwG0jQs,1993
@@ -38,11 +38,11 @@
 jssp_tool/rl/replay_buffer/a/random.py,sha256=gep0KQNl2-u6-HJij3YVG4Q82_f6pz3K4xriV-qf8FM,843
 jssp_tool/rl/replay_buffer/a/sum_tree.py,sha256=XcwKMWpthvvjznlyfHwbs7q9SkOA2QVNeVwRWZGq4u4,9304
 jssp_tool/rl/replay_buffer/priority/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 jssp_tool/rl/replay_buffer/priority/priority_replay_buffer.py,sha256=4Ch7WZaJbgzRWeRjXYAFhIwM_O7C6sGDPwNLXZI82hE,3461
 jssp_tool/rl/replay_buffer/priority/sum_tree.py,sha256=JdBiasQL9Jmmr8D8u9KJmCZXDYhRSnyWfxJ29ZF-thk,2091
 jssp_tool/util/__init__.py,sha256=4M4VPB5XDM-kSNpFiQUSoVKCSyy3DUIxym08ChTJ8K8,22
 jssp_tool/util/logger.py,sha256=ZngZzmlXkLJCUI7KG3ezc5MCfT_Ly1MQMJDVOqgF4KE,7906
-jssp_tool-1.0.5.dist-info/METADATA,sha256=TSezP4ms07OazEQwYuYlvd0dFxbAqHZsG0zASXPYPAE,318
-jssp_tool-1.0.5.dist-info/WHEEL,sha256=2wepM1nk4DS4eFpYrW1TTqPcoGNfHhhO_i5m4cOimbo,92
-jssp_tool-1.0.5.dist-info/top_level.txt,sha256=UYoYuY2dChwe9ixzTebOVCa9YM_1EXZCvq3gPbMvWic,19
-jssp_tool-1.0.5.dist-info/RECORD,,
+jssp_tool-1.0.6.dist-info/METADATA,sha256=yIPDX6J9XG48GKpXAsx7sVGjkH-7SOe4eVkxS3sXLZA,318
+jssp_tool-1.0.6.dist-info/WHEEL,sha256=2wepM1nk4DS4eFpYrW1TTqPcoGNfHhhO_i5m4cOimbo,92
+jssp_tool-1.0.6.dist-info/top_level.txt,sha256=UYoYuY2dChwe9ixzTebOVCa9YM_1EXZCvq3gPbMvWic,19
+jssp_tool-1.0.6.dist-info/RECORD,,
```

