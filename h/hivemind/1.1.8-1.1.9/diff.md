# Comparing `tmp/hivemind-1.1.8.tar.gz` & `tmp/hivemind-1.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hivemind-1.1.8.tar", last modified: Mon May  1 16:11:19 2023, max compression
+gzip compressed data, was "hivemind-1.1.9.tar", last modified: Sun Jul 23 13:00:42 2023, max compression
```

## Comparing `hivemind-1.1.8.tar` & `hivemind-1.1.9.tar`

### file list

```diff
@@ -1,126 +1,147 @@
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.793133 hivemind-1.1.8/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1096 2021-02-19 07:15:37.000000 hivemind-1.1.8/LICENSE
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1314 2023-05-01 16:11:19.792395 hivemind-1.1.8/PKG-INFO
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    10865 2023-03-31 13:55:15.000000 hivemind-1.1.8/README.md
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.498956 hivemind-1.1.8/hivemind/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      479 2023-05-01 16:10:38.000000 hivemind-1.1.8/hivemind/__init__.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.514307 hivemind-1.1.8/hivemind/averaging/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)       62 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/averaging/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    18412 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/averaging/allreduce.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    39698 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/averaging/averager.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6511 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/averaging/control.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      671 2021-08-11 06:04:46.000000 hivemind-1.1.8/hivemind/averaging/group_info.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5436 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/averaging/key_manager.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5450 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/averaging/load_balancing.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    28174 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/averaging/matchmaking.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    14877 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/averaging/partition.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.538033 hivemind-1.1.8/hivemind/compression/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      658 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/compression/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2823 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/compression/adaptive.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5178 2023-05-01 16:02:30.000000 hivemind-1.1.8/hivemind/compression/base.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4067 2022-06-08 15:22:00.000000 hivemind-1.1.8/hivemind/compression/floating.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     8300 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/compression/quantization.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2846 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/compression/serialization.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.550740 hivemind-1.1.8/hivemind/dht/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1057 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/dht/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3595 2021-08-11 06:04:46.000000 hivemind-1.1.8/hivemind/dht/crypto.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    14912 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/dht/dht.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    52055 2023-03-31 13:55:14.000000 hivemind-1.1.8/hivemind/dht/node.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    22566 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/dht/protocol.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    15550 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/dht/routing.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     7304 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/dht/schema.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3757 2021-08-11 06:04:46.000000 hivemind-1.1.8/hivemind/dht/storage.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    15234 2021-08-11 06:04:46.000000 hivemind-1.1.8/hivemind/dht/traverse.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4555 2021-07-12 19:08:17.000000 hivemind-1.1.8/hivemind/dht/validation.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.587394 hivemind-1.1.8/hivemind/hivemind_cli/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2021-04-02 18:12:53.000000 hivemind-1.1.8/hivemind/hivemind_cli/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      181 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/hivemind_cli/config.yml
--rwxrwxrwx   0 mryab    (1786541415) LD\Domain Users (593637566)  9172340 2023-01-03 13:33:41.000000 hivemind-1.1.8/hivemind/hivemind_cli/p2pd
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3325 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/hivemind_cli/run_dht.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6370 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/hivemind_cli/run_server.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.589454 hivemind-1.1.8/hivemind/moe/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      254 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/__init__.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.596790 hivemind-1.1.8/hivemind/moe/client/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      183 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/client/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    20911 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/client/beam_search.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     9758 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/client/expert.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    20442 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/client/moe.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1120 2023-03-31 13:55:15.000000 hivemind-1.1.8/hivemind/moe/client/remote_expert_worker.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    10484 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/client/switch_moe.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1644 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/expert_uid.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.605356 hivemind-1.1.8/hivemind/moe/server/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      260 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2731 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/checkpoints.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     7267 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/connection_handler.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4945 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/dht_handler.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.612025 hivemind-1.1.8/hivemind/moe/server/layers/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      398 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/layers/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3283 2021-07-12 19:08:17.000000 hivemind-1.1.8/hivemind/moe/server/layers/common.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1182 2021-08-11 06:04:46.000000 hivemind-1.1.8/hivemind/moe/server/layers/custom_experts.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1732 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/layers/dropout.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1209 2021-07-03 15:49:22.000000 hivemind-1.1.8/hivemind/moe/server/layers/lr_schedule.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1775 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/layers/optim.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     9743 2023-03-31 13:55:14.000000 hivemind-1.1.8/hivemind/moe/server/module_backend.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     8835 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/runtime.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    17792 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/server.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    10951 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/moe/server/task_pool.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.637466 hivemind-1.1.8/hivemind/optim/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      179 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/optim/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    12669 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/optim/grad_averager.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6239 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/optim/grad_scaler.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    45413 2023-03-31 13:55:14.000000 hivemind-1.1.8/hivemind/optim/optimizer.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    10944 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/optim/power_sgd_averager.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    17452 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/optim/progress_tracker.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    40626 2023-03-31 13:55:14.000000 hivemind-1.1.8/hivemind/optim/state_averager.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    12900 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/optim/training_averager.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.640612 hivemind-1.1.8/hivemind/p2p/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      204 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/p2p/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    30471 2023-05-01 16:02:30.000000 hivemind-1.1.8/hivemind/p2p/p2p_daemon.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.645624 hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      160 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    16666 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/control.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5992 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/datastructures.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4414 2023-05-01 16:02:30.000000 hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/p2pclient.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2271 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/utils.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6393 2023-03-31 13:55:15.000000 hivemind-1.1.8/hivemind/p2p/servicer.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.702378 hivemind-1.1.8/hivemind/proto/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      441 2022-06-16 10:08:09.000000 hivemind-1.1.8/hivemind/proto/auth.proto
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2572 2023-03-11 13:51:45.000000 hivemind-1.1.8/hivemind/proto/auth_pb2.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3672 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/proto/averaging.proto
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5102 2023-03-11 13:51:45.000000 hivemind-1.1.8/hivemind/proto/averaging_pb2.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      407 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/proto/crypto.proto
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2148 2023-03-11 13:51:45.000000 hivemind-1.1.8/hivemind/proto/crypto_pb2.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3364 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/proto/dht.proto
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5846 2023-03-11 13:51:45.000000 hivemind-1.1.8/hivemind/proto/dht_pb2.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4607 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/proto/p2pd.proto
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    19245 2023-03-11 13:51:45.000000 hivemind-1.1.8/hivemind/proto/p2pd_pb2.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      599 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/proto/runtime.proto
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3878 2023-03-11 13:51:45.000000 hivemind-1.1.8/hivemind/proto/runtime_pb2.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      114 2022-06-16 10:08:09.000000 hivemind-1.1.8/hivemind/proto/test.proto
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1609 2023-03-11 13:51:45.000000 hivemind-1.1.8/hivemind/proto/test_pb2.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.790797 hivemind-1.1.8/hivemind/utils/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      628 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/__init__.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     7162 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/asyncio.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     7781 2022-06-08 15:22:00.000000 hivemind-1.1.8/hivemind/utils/auth.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3293 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/crypto.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      740 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/limits.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6748 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/logging.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      849 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/math.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    15185 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/mpfuture.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2622 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/nested.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2712 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/networking.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3225 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/performance_ema.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2637 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/serializer.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1611 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/streaming.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4657 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/tensor_descr.py
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5533 2023-03-31 13:53:53.000000 hivemind-1.1.8/hivemind/utils/timed_storage.py
-drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-05-01 16:11:19.504021 hivemind-1.1.8/hivemind.egg-info/
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1314 2023-05-01 16:11:19.000000 hivemind-1.1.8/hivemind.egg-info/PKG-INFO
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3282 2023-05-01 16:11:19.000000 hivemind-1.1.8/hivemind.egg-info/SOURCES.txt
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)        1 2023-05-01 16:11:19.000000 hivemind-1.1.8/hivemind.egg-info/dependency_links.txt
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      125 2023-05-01 16:11:19.000000 hivemind-1.1.8/hivemind.egg-info/entry_points.txt
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      779 2023-05-01 16:11:19.000000 hivemind-1.1.8/hivemind.egg-info/requires.txt
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)        9 2023-05-01 16:11:19.000000 hivemind-1.1.8/hivemind.egg-info/top_level.txt
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      222 2023-03-31 13:53:53.000000 hivemind-1.1.8/pyproject.toml
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)       38 2023-05-01 16:11:19.793339 hivemind-1.1.8/setup.cfg
--rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6803 2023-03-31 13:53:53.000000 hivemind-1.1.8/setup.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.437372 hivemind-1.1.9/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1096 2021-02-19 07:15:37.000000 hivemind-1.1.9/LICENSE
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1295 2023-07-23 13:00:42.436664 hivemind-1.1.9/PKG-INFO
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    10865 2023-06-10 19:46:52.000000 hivemind-1.1.9/README.md
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.142758 hivemind-1.1.9/hivemind/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      479 2023-07-23 13:00:14.000000 hivemind-1.1.9/hivemind/__init__.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.164326 hivemind-1.1.9/hivemind/averaging/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)       62 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/averaging/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    18412 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/averaging/allreduce.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    39698 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/averaging/averager.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6511 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/averaging/control.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      671 2021-08-11 06:04:46.000000 hivemind-1.1.9/hivemind/averaging/group_info.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5436 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/averaging/key_manager.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5450 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/averaging/load_balancing.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    28371 2023-07-23 12:59:15.000000 hivemind-1.1.9/hivemind/averaging/matchmaking.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    14945 2023-07-23 12:59:15.000000 hivemind-1.1.9/hivemind/averaging/partition.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.178047 hivemind-1.1.9/hivemind/compression/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      658 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/compression/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2823 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/compression/adaptive.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5183 2023-07-23 12:59:16.000000 hivemind-1.1.9/hivemind/compression/base.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4067 2022-06-08 15:22:00.000000 hivemind-1.1.9/hivemind/compression/floating.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     8305 2023-07-23 12:59:16.000000 hivemind-1.1.9/hivemind/compression/quantization.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2846 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/compression/serialization.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.206466 hivemind-1.1.9/hivemind/dht/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1057 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/dht/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3595 2021-08-11 06:04:46.000000 hivemind-1.1.9/hivemind/dht/crypto.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    14912 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/dht/dht.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    52055 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/dht/node.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    22584 2023-07-23 12:59:15.000000 hivemind-1.1.9/hivemind/dht/protocol.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    15550 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/dht/routing.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     7304 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/dht/schema.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3757 2021-08-11 06:04:46.000000 hivemind-1.1.9/hivemind/dht/storage.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    15345 2023-07-23 12:59:15.000000 hivemind-1.1.9/hivemind/dht/traverse.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4555 2021-07-12 19:08:17.000000 hivemind-1.1.9/hivemind/dht/validation.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.265017 hivemind-1.1.9/hivemind/hivemind_cli/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2021-04-02 18:12:53.000000 hivemind-1.1.9/hivemind/hivemind_cli/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      181 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/hivemind_cli/config.yml
+-rwxrwxrwx   0 mryab    (1786541415) LD\Domain Users (593637566)  9172340 2023-01-03 13:33:41.000000 hivemind-1.1.9/hivemind/hivemind_cli/p2pd
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3475 2023-07-23 12:59:15.000000 hivemind-1.1.9/hivemind/hivemind_cli/run_dht.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6331 2023-07-23 12:59:15.000000 hivemind-1.1.9/hivemind/hivemind_cli/run_server.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.268507 hivemind-1.1.9/hivemind/moe/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      254 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/__init__.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.277810 hivemind-1.1.9/hivemind/moe/client/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      183 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/client/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    20911 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/client/beam_search.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     9758 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/client/expert.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    20442 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/client/moe.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1120 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/client/remote_expert_worker.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    10484 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/client/switch_moe.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1644 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/expert_uid.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.307067 hivemind-1.1.9/hivemind/moe/server/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      260 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/server/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2731 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/server/checkpoints.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     7267 2023-06-11 16:07:49.000000 hivemind-1.1.9/hivemind/moe/server/connection_handler.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4945 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/server/dht_handler.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.317703 hivemind-1.1.9/hivemind/moe/server/layers/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      398 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/server/layers/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3283 2023-06-11 15:31:16.000000 hivemind-1.1.9/hivemind/moe/server/layers/common.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1182 2021-08-11 06:04:46.000000 hivemind-1.1.9/hivemind/moe/server/layers/custom_experts.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1732 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/server/layers/dropout.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1209 2021-07-03 15:49:22.000000 hivemind-1.1.9/hivemind/moe/server/layers/lr_schedule.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1775 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/server/layers/optim.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     9743 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/server/module_backend.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     8835 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/server/runtime.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    17792 2023-06-11 16:08:17.000000 hivemind-1.1.9/hivemind/moe/server/server.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    10951 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/moe/server/task_pool.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.333605 hivemind-1.1.9/hivemind/optim/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      179 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/optim/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    12669 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/optim/grad_averager.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6239 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/optim/grad_scaler.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    45413 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/optim/optimizer.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    10944 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/optim/power_sgd_averager.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    17452 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/optim/progress_tracker.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    40626 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/optim/state_averager.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    12900 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/optim/training_averager.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.339375 hivemind-1.1.9/hivemind/p2p/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      204 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/p2p/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    30493 2023-07-23 12:59:16.000000 hivemind-1.1.9/hivemind/p2p/p2p_daemon.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.347496 hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      160 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    16666 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/control.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5992 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/datastructures.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4414 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/p2pclient.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2271 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/utils.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6393 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/p2p/servicer.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.370012 hivemind-1.1.9/hivemind/proto/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      441 2022-06-16 10:08:09.000000 hivemind-1.1.9/hivemind/proto/auth.proto
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3672 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/proto/averaging.proto
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      407 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/proto/crypto.proto
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3364 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/proto/dht.proto
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4607 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/proto/p2pd.proto
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      599 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/proto/runtime.proto
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      114 2022-06-16 10:08:09.000000 hivemind-1.1.9/hivemind/proto/test.proto
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.388460 hivemind-1.1.9/hivemind/utils/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      628 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/__init__.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     7162 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/asyncio.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     7781 2022-06-08 15:22:00.000000 hivemind-1.1.9/hivemind/utils/auth.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3293 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/crypto.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      740 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/limits.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6748 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/logging.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      849 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/math.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    15185 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/mpfuture.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2622 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/nested.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2712 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/networking.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3225 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/performance_ema.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2637 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/serializer.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1611 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/streaming.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4657 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/tensor_descr.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5533 2023-06-10 19:46:52.000000 hivemind-1.1.9/hivemind/utils/timed_storage.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.151380 hivemind-1.1.9/hivemind.egg-info/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1295 2023-07-23 13:00:42.000000 hivemind-1.1.9/hivemind.egg-info/PKG-INFO
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3781 2023-07-23 13:00:42.000000 hivemind-1.1.9/hivemind.egg-info/SOURCES.txt
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)        1 2023-07-23 13:00:42.000000 hivemind-1.1.9/hivemind.egg-info/dependency_links.txt
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      124 2023-07-23 13:00:42.000000 hivemind-1.1.9/hivemind.egg-info/entry_points.txt
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      777 2023-07-23 13:00:42.000000 hivemind-1.1.9/hivemind.egg-info/requires.txt
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)        9 2023-07-23 13:00:42.000000 hivemind-1.1.9/hivemind.egg-info/top_level.txt
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)      337 2023-07-23 12:59:15.000000 hivemind-1.1.9/pyproject.toml
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)       38 2023-07-23 13:00:42.437533 hivemind-1.1.9/setup.cfg
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6803 2023-06-10 19:46:52.000000 hivemind-1.1.9/setup.py
+drwxr-xr-x   0 mryab    (1786541415) LD\Domain Users (593637566)        0 2023-07-23 13:00:42.435196 hivemind-1.1.9/tests/
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     9981 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_allreduce.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     8978 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_allreduce_fault_tolerance.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6048 2022-06-08 15:22:00.000000 hivemind-1.1.9/tests/test_auth.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    18065 2023-07-23 12:59:15.000000 hivemind-1.1.9/tests/test_averaging.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2118 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_cli_scripts.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     9410 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_compression.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     7574 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_connection_handler.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2292 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_custom_experts.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3929 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_dht.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5419 2022-05-31 15:27:03.000000 hivemind-1.1.9/tests/test_dht_crypto.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     8918 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_dht_experts.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    12673 2023-07-23 12:59:15.000000 hivemind-1.1.9/tests/test_dht_node.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6855 2021-08-26 07:54:05.000000 hivemind-1.1.9/tests/test_dht_protocol.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     8151 2021-07-12 19:08:17.000000 hivemind-1.1.9/tests/test_dht_schema.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     5972 2021-08-11 06:04:46.000000 hivemind-1.1.9/tests/test_dht_storage.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3766 2021-08-11 06:04:46.000000 hivemind-1.1.9/tests/test_dht_validation.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     3531 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_expert_backend.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    13210 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_moe.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    17305 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_optimizer.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    15355 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_p2p_daemon.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    20371 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_p2p_daemon_bindings.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6953 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_p2p_servicer.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     1715 2023-07-23 12:55:49.000000 hivemind-1.1.9/tests/test_relays.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     6251 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_routing.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     2973 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_start_server.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)     4987 2023-06-10 19:46:52.000000 hivemind-1.1.9/tests/test_training.py
+-rw-r--r--   0 mryab    (1786541415) LD\Domain Users (593637566)    19238 2023-07-23 12:59:15.000000 hivemind-1.1.9/tests/test_util_modules.py
```

### Comparing `hivemind-1.1.8/LICENSE` & `hivemind-1.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/PKG-INFO` & `hivemind-1.1.9/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,17 +1,16 @@
 Metadata-Version: 2.1
 Name: hivemind
-Version: 1.1.8
+Version: 1.1.9
 Summary: Decentralized deep learning in PyTorch
 Home-page: https://github.com/learning-at-home/hivemind
 Author: Learning@home & contributors
 Author-email: hivemind-team@hotmail.com
 License: MIT
 Keywords: pytorch,deep learning,machine learning,gpu,distributed computing,volunteer computing,dht
-Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
@@ -25,8 +24,7 @@
 Provides-Extra: dev
 Provides-Extra: docs
 Provides-Extra: bitsandbytes
 Provides-Extra: all
 License-File: LICENSE
 
 Decentralized deep learning in PyTorch. Built to train models on thousands of volunteers across the world.
-
```

### Comparing `hivemind-1.1.8/README.md` & `hivemind-1.1.9/README.md`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/averaging/allreduce.py` & `hivemind-1.1.9/hivemind/averaging/allreduce.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/averaging/averager.py` & `hivemind-1.1.9/hivemind/averaging/averager.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/averaging/control.py` & `hivemind-1.1.9/hivemind/averaging/control.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/averaging/group_info.py` & `hivemind-1.1.9/hivemind/averaging/group_info.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/averaging/key_manager.py` & `hivemind-1.1.9/hivemind/averaging/key_manager.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/averaging/load_balancing.py` & `hivemind-1.1.9/hivemind/averaging/load_balancing.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/averaging/matchmaking.py` & `hivemind-1.1.9/hivemind/averaging/matchmaking.py`

 * *Files 1% similar despite different names*

```diff
@@ -280,15 +280,15 @@
                 ):
                     # outcome 1: we have assembled a full group and are ready for allreduce
                     await self.leader_assemble_group()
 
             # wait for the group to be assembled or disbanded
             timeout = max(0.0, self.potential_leaders.declared_expiration_time - get_dht_time())
             await asyncio.wait(
-                {self.assembled_group, self.was_accepted_to_group.wait()},
+                {self.assembled_group, asyncio.create_task(self.was_accepted_to_group.wait())},
                 return_when=asyncio.FIRST_COMPLETED,
                 timeout=timeout,
             )
             if not self.assembled_group.done() and not self.was_accepted_to_group.is_set():
                 async with self.lock_request_join_group:
                     if self.assembled_group.done():
                         pass  # this covers a rare case when the group is assembled while the event loop was busy.
@@ -476,15 +476,19 @@
                 self.update_triggered.set()
 
             if maybe_next_leader is None or (entry.expiration_time, maybe_next_leader.to_bytes()) > (
                 self.declared_expiration_time,
                 self.peer_id.to_bytes(),
             ):
                 await asyncio.wait(
-                    {self.update_finished.wait(), self.declared_expiration.wait()}, return_when=asyncio.FIRST_COMPLETED
+                    {
+                        asyncio.create_task(self.update_finished.wait()),
+                        asyncio.create_task(self.declared_expiration.wait()),
+                    },
+                    return_when=asyncio.FIRST_COMPLETED,
                 )
                 self.declared_expiration.clear()
                 if self.update_finished.is_set():
                     self.update_finished.clear()
                     continue
                 else:
                     raise asyncio.TimeoutError("pop_next_leader was invalidated: re-declared averager in background")
@@ -507,15 +511,15 @@
                     continue
                 self.leader_queue.store(peer, peer_expiration_time, peer_expiration_time)
                 self.max_assured_time = max(self.max_assured_time, peer_expiration_time - DISCREPANCY)
 
             self.update_finished.set()
 
             await asyncio.wait(
-                {self.running.wait(), self.update_triggered.wait()},
+                {asyncio.create_task(self.running.wait()), asyncio.create_task(self.update_triggered.wait())},
                 return_when=asyncio.ALL_COMPLETED,
                 timeout=self.search_end_time - get_dht_time() if isfinite(self.search_end_time) else None,
             )
             self.update_triggered.clear()
 
     async def _declare_averager_periodically(self, step: StepControl, key_manager: GroupKeyManager) -> None:
         async with self.lock_declare:
```

### Comparing `hivemind-1.1.8/hivemind/averaging/partition.py` & `hivemind-1.1.9/hivemind/averaging/partition.py`

 * *Files 1% similar despite different names*

```diff
@@ -220,15 +220,18 @@
         """Add vector part to accumulator, wait for all other vectors to be added, then return the average part"""
         assert 0 <= sender_index < self.num_senders, "invalid sender index"
         assert 0 <= part_index < self.num_parts, "invalid part index"
         self.num_parts_received[sender_index] += 1
 
         while part_index > self.current_part_index:
             # wait for previous parts to finish processing ...
-            await asyncio.wait({self.current_part_future, self.finished.wait()}, return_when=asyncio.FIRST_COMPLETED)
+            await asyncio.wait(
+                {self.current_part_future, asyncio.create_task(self.finished.wait())},
+                return_when=asyncio.FIRST_COMPLETED,
+            )
             if self.finished.is_set():
                 raise AllreduceException(f"attempted to aggregate part in a finalized {self.__class__.__name__}")
 
         if self.sender_failed_after[sender_index] != float("inf"):
             raise BannedException(f"sender {sender_index} was banned in background")
         assert part_index == self.current_part_index
```

### Comparing `hivemind-1.1.8/hivemind/compression/__init__.py` & `hivemind-1.1.9/hivemind/compression/__init__.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/compression/adaptive.py` & `hivemind-1.1.9/hivemind/compression/adaptive.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/compression/base.py` & `hivemind-1.1.9/hivemind/compression/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -80,15 +80,15 @@
     """A dummy compression strategy that preserves the original tensor as is."""
 
     compression_type = runtime_pb2.CompressionType.NONE
 
     def compress(self, tensor: torch.Tensor, info: CompressionInfo, allow_inplace: bool = False) -> runtime_pb2.Tensor:
         tensor = tensor.detach()
         shape = tensor.shape
-        dtype_name = str(tensor.dtype).lstrip("torch.")
+        dtype_name = str(tensor.dtype).replace("torch.", "")
         raw_data = tensor
         if tensor.dtype == torch.bfloat16:
             if USE_LEGACY_BFLOAT16:  # legacy mode: convert to fp32
                 raw_data = tensor.to(torch.float32)
             else:  # efficient mode: send bfloat16 data directly
                 # reinterpret_cast to an arbitrary 2-byte type supported by numpy
                 raw_data = tensor.view(torch.int16)
```

### Comparing `hivemind-1.1.8/hivemind/compression/floating.py` & `hivemind-1.1.9/hivemind/compression/floating.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/compression/quantization.py` & `hivemind-1.1.9/hivemind/compression/quantization.py`

 * *Files 0% similar despite different names*

```diff
@@ -136,15 +136,15 @@
             raise ImportError(BNB_MISSING_MESSAGE)
 
         quantized, (absmax, codebook) = quantize_blockwise(tensor)
         return quantized.numpy(), (absmax.numpy(), codebook.numpy())
 
     def compress(self, tensor: torch.Tensor, info: CompressionInfo, allow_inplace: bool = False) -> runtime_pb2.Tensor:
         tensor = tensor.detach()
-        dtype_name = str(tensor.dtype).lstrip("torch.")
+        dtype_name = str(tensor.dtype).replace("torch.", "")
         if tensor.dtype == torch.bfloat16:
             tensor = tensor.to(torch.float32)
 
         quantized, (absmax, codebook) = self.quantize(tensor, allow_inplace=allow_inplace)
 
         serialized_data = (
             np.int64(len(absmax)).tobytes(),
```

### Comparing `hivemind-1.1.8/hivemind/compression/serialization.py` & `hivemind-1.1.9/hivemind/compression/serialization.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/dht/__init__.py` & `hivemind-1.1.9/hivemind/dht/__init__.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/dht/crypto.py` & `hivemind-1.1.9/hivemind/dht/crypto.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/dht/dht.py` & `hivemind-1.1.9/hivemind/dht/dht.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/dht/node.py` & `hivemind-1.1.9/hivemind/dht/node.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/dht/protocol.py` & `hivemind-1.1.9/hivemind/dht/protocol.py`

 * *Files 0% similar despite different names*

```diff
@@ -117,15 +117,15 @@
         if responded and validate:
             try:
                 if not self.client_mode and not response.available:
                     raise ValidationError(
                         f"Peer {peer} can't access this node. " f"Probably, libp2p has failed to bypass the firewall"
                     )
 
-                if response.dht_time != dht_pb2.PingResponse.dht_time.DESCRIPTOR.default_value:
+                if response.dht_time != dht_pb2.PingResponse.DESCRIPTOR.fields_by_name["dht_time"].default_value:
                     if (
                         response.dht_time < time_requested - MAX_DHT_TIME_DISCREPANCY_SECONDS
                         or response.dht_time > time_responded + MAX_DHT_TIME_DISCREPANCY_SECONDS
                     ):
                         raise ValidationError(
                             f"local time must be within {MAX_DHT_TIME_DISCREPANCY_SECONDS} seconds "
                             f" of others(local: {time_requested:.5f}, peer: {response.dht_time:.5f})"
```

### Comparing `hivemind-1.1.8/hivemind/dht/routing.py` & `hivemind-1.1.9/hivemind/dht/routing.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/dht/schema.py` & `hivemind-1.1.9/hivemind/dht/schema.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/dht/storage.py` & `hivemind-1.1.9/hivemind/dht/storage.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/dht/traverse.py` & `hivemind-1.1.9/hivemind/dht/traverse.py`

 * *Files 1% similar despite different names*

```diff
@@ -205,15 +205,17 @@
             active_workers.update(queries_to_call)
             for query_to_call in queries_to_call:
                 visited_nodes[query_to_call].add(chosen_peer)
 
             # get nearest neighbors (over network) and update search heaps. Abort if search finishes early
             get_neighbors_task = asyncio.create_task(get_neighbors(chosen_peer, queries_to_call))
             pending_tasks.add(get_neighbors_task)
-            await asyncio.wait([get_neighbors_task, search_finished_event.wait()], return_when=asyncio.FIRST_COMPLETED)
+            await_finished_task = asyncio.create_task(search_finished_event.wait())
+            await asyncio.wait([get_neighbors_task, await_finished_task], return_when=asyncio.FIRST_COMPLETED)
+            del await_finished_task
             if search_finished_event.is_set():
                 break  # other worker triggered finish_search, we exit immediately
             pending_tasks.remove(get_neighbors_task)
 
             # add nearest neighbors to their respective heaps
             for query, (neighbors_for_query, should_stop) in get_neighbors_task.result().items():
                 if should_stop and (query in unfinished_queries):
```

### Comparing `hivemind-1.1.8/hivemind/dht/validation.py` & `hivemind-1.1.9/hivemind/dht/validation.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/hivemind_cli/p2pd` & `hivemind-1.1.9/hivemind/hivemind_cli/p2pd`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/hivemind_cli/run_dht.py` & `hivemind-1.1.9/hivemind/hivemind_cli/run_dht.py`

 * *Files 10% similar despite different names*

```diff
@@ -80,14 +80,19 @@
         use_ipfs=args.use_ipfs,
         identity_path=args.identity_path,
         use_relay=args.use_relay,
         use_auto_relay=args.use_auto_relay,
     )
     log_visible_maddrs(dht.get_visible_maddrs(), only_p2p=args.use_ipfs)
 
-    while True:
-        dht.run_coroutine(report_status, return_future=False)
-        time.sleep(args.refresh_period)
+    try:
+        while True:
+            dht.run_coroutine(report_status, return_future=False)
+            time.sleep(args.refresh_period)
+    except KeyboardInterrupt:
+        logger.info("Caught KeyboardInterrupt, shutting down")
+    finally:
+        dht.shutdown()
 
 
 if __name__ == "__main__":
     main()
```

### Comparing `hivemind-1.1.8/hivemind/hivemind_cli/run_server.py` & `hivemind-1.1.9/hivemind/hivemind_cli/run_server.py`

 * *Files 2% similar despite different names*

```diff
@@ -104,13 +104,11 @@
 
     server = Server.create(**args, optim_cls=optim_cls, start=True, compression=compression)
 
     try:
         server.join()
     except KeyboardInterrupt:
         logger.info("Caught KeyboardInterrupt, shutting down")
-    finally:
-        server.shutdown()
 
 
 if __name__ == "__main__":
     main()
```

### Comparing `hivemind-1.1.8/hivemind/moe/client/beam_search.py` & `hivemind-1.1.9/hivemind/moe/client/beam_search.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/client/expert.py` & `hivemind-1.1.9/hivemind/moe/client/expert.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/client/moe.py` & `hivemind-1.1.9/hivemind/moe/client/moe.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/client/remote_expert_worker.py` & `hivemind-1.1.9/hivemind/moe/client/remote_expert_worker.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/client/switch_moe.py` & `hivemind-1.1.9/hivemind/moe/client/switch_moe.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/expert_uid.py` & `hivemind-1.1.9/hivemind/moe/expert_uid.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/checkpoints.py` & `hivemind-1.1.9/hivemind/moe/server/checkpoints.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/connection_handler.py` & `hivemind-1.1.9/hivemind/moe/server/connection_handler.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/dht_handler.py` & `hivemind-1.1.9/hivemind/moe/server/dht_handler.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/layers/common.py` & `hivemind-1.1.9/hivemind/moe/server/layers/common.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/layers/custom_experts.py` & `hivemind-1.1.9/hivemind/moe/server/layers/custom_experts.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/layers/dropout.py` & `hivemind-1.1.9/hivemind/moe/server/layers/dropout.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/layers/lr_schedule.py` & `hivemind-1.1.9/hivemind/moe/server/layers/lr_schedule.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/layers/optim.py` & `hivemind-1.1.9/hivemind/moe/server/layers/optim.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/module_backend.py` & `hivemind-1.1.9/hivemind/moe/server/module_backend.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/runtime.py` & `hivemind-1.1.9/hivemind/moe/server/runtime.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/server.py` & `hivemind-1.1.9/hivemind/moe/server/server.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/moe/server/task_pool.py` & `hivemind-1.1.9/hivemind/moe/server/task_pool.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/optim/grad_averager.py` & `hivemind-1.1.9/hivemind/optim/grad_averager.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/optim/grad_scaler.py` & `hivemind-1.1.9/hivemind/optim/grad_scaler.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/optim/optimizer.py` & `hivemind-1.1.9/hivemind/optim/optimizer.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/optim/power_sgd_averager.py` & `hivemind-1.1.9/hivemind/optim/power_sgd_averager.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/optim/progress_tracker.py` & `hivemind-1.1.9/hivemind/optim/progress_tracker.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/optim/state_averager.py` & `hivemind-1.1.9/hivemind/optim/state_averager.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/optim/training_averager.py` & `hivemind-1.1.9/hivemind/optim/training_averager.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/p2p/p2p_daemon.py` & `hivemind-1.1.9/hivemind/p2p/p2p_daemon.py`

 * *Files 1% similar despite different names*

```diff
@@ -654,17 +654,17 @@
 
         self._alive = False
         if self._child is not None and self._child.returncode is None:
             with suppress(ProcessLookupError):
                 self._child.terminate()
                 logger.debug(f"Terminated p2pd with id = {self.peer_id}")
 
-            with suppress(FileNotFoundError):
+            with suppress(FileNotFoundError, TypeError):
                 os.remove(self._daemon_listen_maddr["unix"])
-        with suppress(FileNotFoundError):
+        with suppress(FileNotFoundError, TypeError):
             os.remove(self._client_listen_maddr["unix"])
 
     @staticmethod
     def _make_process_args(*args, **kwargs) -> List[str]:
         proc_args = []
         proc_args.extend(str(entry) for entry in args)
         proc_args.extend(
```

### Comparing `hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/control.py` & `hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/control.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/datastructures.py` & `hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/datastructures.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/p2pclient.py` & `hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/p2pclient.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/p2p/p2p_daemon_bindings/utils.py` & `hivemind-1.1.9/hivemind/p2p/p2p_daemon_bindings/utils.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/p2p/servicer.py` & `hivemind-1.1.9/hivemind/p2p/servicer.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/proto/averaging.proto` & `hivemind-1.1.9/hivemind/proto/averaging.proto`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/proto/dht.proto` & `hivemind-1.1.9/hivemind/proto/dht.proto`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/proto/p2pd.proto` & `hivemind-1.1.9/hivemind/proto/p2pd.proto`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/proto/runtime.proto` & `hivemind-1.1.9/hivemind/proto/runtime.proto`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/__init__.py` & `hivemind-1.1.9/hivemind/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/asyncio.py` & `hivemind-1.1.9/hivemind/utils/asyncio.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/auth.py` & `hivemind-1.1.9/hivemind/utils/auth.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/crypto.py` & `hivemind-1.1.9/hivemind/utils/crypto.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/limits.py` & `hivemind-1.1.9/hivemind/utils/limits.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/logging.py` & `hivemind-1.1.9/hivemind/utils/logging.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/math.py` & `hivemind-1.1.9/hivemind/utils/math.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/mpfuture.py` & `hivemind-1.1.9/hivemind/utils/mpfuture.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/nested.py` & `hivemind-1.1.9/hivemind/utils/nested.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/networking.py` & `hivemind-1.1.9/hivemind/utils/networking.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/performance_ema.py` & `hivemind-1.1.9/hivemind/utils/performance_ema.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/serializer.py` & `hivemind-1.1.9/hivemind/utils/serializer.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/streaming.py` & `hivemind-1.1.9/hivemind/utils/streaming.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/tensor_descr.py` & `hivemind-1.1.9/hivemind/utils/tensor_descr.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind/utils/timed_storage.py` & `hivemind-1.1.9/hivemind/utils/timed_storage.py`

 * *Files identical despite different names*

### Comparing `hivemind-1.1.8/hivemind.egg-info/PKG-INFO` & `hivemind-1.1.9/hivemind.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,17 +1,16 @@
 Metadata-Version: 2.1
 Name: hivemind
-Version: 1.1.8
+Version: 1.1.9
 Summary: Decentralized deep learning in PyTorch
 Home-page: https://github.com/learning-at-home/hivemind
 Author: Learning@home & contributors
 Author-email: hivemind-team@hotmail.com
 License: MIT
 Keywords: pytorch,deep learning,machine learning,gpu,distributed computing,volunteer computing,dht
-Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
@@ -25,8 +24,7 @@
 Provides-Extra: dev
 Provides-Extra: docs
 Provides-Extra: bitsandbytes
 Provides-Extra: all
 License-File: LICENSE
 
 Decentralized deep learning in PyTorch. Built to train models on thousands of volunteers across the world.
-
```

### Comparing `hivemind-1.1.8/hivemind.egg-info/SOURCES.txt` & `hivemind-1.1.9/hivemind.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -74,35 +74,55 @@
 hivemind/p2p/servicer.py
 hivemind/p2p/p2p_daemon_bindings/__init__.py
 hivemind/p2p/p2p_daemon_bindings/control.py
 hivemind/p2p/p2p_daemon_bindings/datastructures.py
 hivemind/p2p/p2p_daemon_bindings/p2pclient.py
 hivemind/p2p/p2p_daemon_bindings/utils.py
 hivemind/proto/auth.proto
-hivemind/proto/auth_pb2.py
 hivemind/proto/averaging.proto
-hivemind/proto/averaging_pb2.py
 hivemind/proto/crypto.proto
-hivemind/proto/crypto_pb2.py
 hivemind/proto/dht.proto
-hivemind/proto/dht_pb2.py
 hivemind/proto/p2pd.proto
-hivemind/proto/p2pd_pb2.py
 hivemind/proto/runtime.proto
-hivemind/proto/runtime_pb2.py
 hivemind/proto/test.proto
-hivemind/proto/test_pb2.py
 hivemind/utils/__init__.py
 hivemind/utils/asyncio.py
 hivemind/utils/auth.py
 hivemind/utils/crypto.py
 hivemind/utils/limits.py
 hivemind/utils/logging.py
 hivemind/utils/math.py
 hivemind/utils/mpfuture.py
 hivemind/utils/nested.py
 hivemind/utils/networking.py
 hivemind/utils/performance_ema.py
 hivemind/utils/serializer.py
 hivemind/utils/streaming.py
 hivemind/utils/tensor_descr.py
-hivemind/utils/timed_storage.py
+hivemind/utils/timed_storage.py
+tests/test_allreduce.py
+tests/test_allreduce_fault_tolerance.py
+tests/test_auth.py
+tests/test_averaging.py
+tests/test_cli_scripts.py
+tests/test_compression.py
+tests/test_connection_handler.py
+tests/test_custom_experts.py
+tests/test_dht.py
+tests/test_dht_crypto.py
+tests/test_dht_experts.py
+tests/test_dht_node.py
+tests/test_dht_protocol.py
+tests/test_dht_schema.py
+tests/test_dht_storage.py
+tests/test_dht_validation.py
+tests/test_expert_backend.py
+tests/test_moe.py
+tests/test_optimizer.py
+tests/test_p2p_daemon.py
+tests/test_p2p_daemon_bindings.py
+tests/test_p2p_servicer.py
+tests/test_relays.py
+tests/test_routing.py
+tests/test_start_server.py
+tests/test_training.py
+tests/test_util_modules.py
```

### Comparing `hivemind-1.1.8/hivemind.egg-info/requires.txt` & `hivemind-1.1.9/hivemind.egg-info/requires.txt`

 * *Files 2% similar despite different names*

```diff
@@ -3,20 +3,20 @@
 numpy>=1.17
 scipy>=1.2.1
 prefetch_generator>=1.0.1
 msgpack>=0.5.6
 sortedcontainers
 uvloop>=0.14.0
 grpcio-tools>=1.33.2
-protobuf<4.0.0,>=3.12.2
+protobuf>=3.12.2
 configargparse>=1.2.3
 multiaddr>=0.0.9
 pymultihash>=0.8.2
 cryptography>=3.4.6
-pydantic>=1.8.1
+pydantic<2.0,>=1.8.1
 
 [all]
 pytest==6.2.5
 pytest-forked
 pytest-asyncio==0.16.0
 pytest-cov
 coverage==6.0.2
```

### Comparing `hivemind-1.1.8/setup.py` & `hivemind-1.1.9/setup.py`

 * *Files identical despite different names*

