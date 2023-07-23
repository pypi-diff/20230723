# Comparing `tmp/weathon-0.0.0.17.tar.gz` & `tmp/weathon-0.0.0.18.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/weathon-0.0.0.17.tar", last modified: Wed Jul 12 06:21:16 2023, max compression
+gzip compressed data, was "dist/weathon-0.0.0.18.tar", last modified: Sun Jul 23 05:28:19 2023, max compression
```

## Comparing `weathon-0.0.0.17.tar` & `weathon-0.0.0.18.tar`

### file list

```diff
@@ -1,727 +1,784 @@
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/
--rw-r--r--   0 runner    (1001) docker     (122)       53 2023-07-12 06:21:16.000000 weathon-0.0.0.17/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (122)      859 2023-07-12 06:21:16.000000 weathon-0.0.0.17/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (122)       72 2023-07-12 06:21:16.000000 weathon-0.0.0.17/README.md
--rw-r--r--   0 runner    (1001) docker     (122)       38 2023-07-12 06:21:16.000000 weathon-0.0.0.17/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/
--rw-r--r--   0 runner    (1001) docker     (122)     3735 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/base/
--rw-r--r--   0 runner    (1001) docker     (122)      549 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      353 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/cli.py
--rw-r--r--   0 runner    (1001) docker     (122)     1399 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/dataset.py
--rw-r--r--   0 runner    (1001) docker     (122)     7221 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/hook.py
--rw-r--r--   0 runner    (1001) docker     (122)      339 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/loss.py
--rw-r--r--   0 runner    (1001) docker     (122)     2441 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/lr_scheduler.py
--rw-r--r--   0 runner    (1001) docker     (122)     2674 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/metric.py
--rw-r--r--   0 runner    (1001) docker     (122)    13442 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/model.py
--rw-r--r--   0 runner    (1001) docker     (122)    22187 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/pipeline.py
--rw-r--r--   0 runner    (1001) docker     (122)     9073 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/processor.py
--rw-r--r--   0 runner    (1001) docker     (122)    27009 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/base/trainer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/dataset/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/dataset/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/dataset/cv/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/dataset/cv/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/dataset/cv/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/dataset/cv/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4111 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/dataset/cv/ocr/datasets.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/dataset/nlp/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/dataset/nlp/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/dataset/nlp/text_classification/
--rw-r--r--   0 runner    (1001) docker     (122)       88 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/dataset/nlp/text_classification/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1637 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/dataset/nlp/text_classification/datasets.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/error/
--rw-r--r--   0 runner    (1001) docker     (122)       71 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/error/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     6288 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/error/error.py
--rw-r--r--   0 runner    (1001) docker     (122)     4018 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/error/hub_error.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/hooks/
--rw-r--r--   0 runner    (1001) docker     (122)     1773 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/hooks/checkpoint/
--rw-r--r--   0 runner    (1001) docker     (122)      116 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/checkpoint/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    16014 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/checkpoint/checkpoint_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)    10628 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/checkpoint/checkpoint_processor.py
--rw-r--r--   0 runner    (1001) docker     (122)     5442 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/checkpoint/load_checkpoint_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)      712 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/clip_clamp_logit_scale_hook.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/hooks/compression/
--rw-r--r--   0 runner    (1001) docker     (122)      557 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/compression/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     5013 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/compression/sparsity_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)     6999 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/compression/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/hooks/distributed/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/distributed/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1331 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/distributed/ddp_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)     8002 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/distributed/deepspeed_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)     6627 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/distributed/megatron_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)     4349 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/early_stop_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)     3715 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/evaluation_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)      673 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/iter_timer_hook.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/hooks/logger/
--rw-r--r--   0 runner    (1001) docker     (122)      606 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/logger/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4390 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/logger/base.py
--rw-r--r--   0 runner    (1001) docker     (122)     4403 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/logger/tensorboard_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)     7266 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/logger/text_logger_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)     6236 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/lr_scheduler_hook.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/hooks/optimizer/
--rw-r--r--   0 runner    (1001) docker     (122)      690 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/optimizer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     3065 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/optimizer/apex_optimizer_hook.py
--rw-r--r--   0 runner    (1001) docker     (122)     3584 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/optimizer/base.py
--rw-r--r--   0 runner    (1001) docker     (122)     3529 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/hooks/optimizer/torch_optimizer_hook.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/loss/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/loss/cv/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/cv/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/loss/cv/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/cv/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      930 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/cv/ocr/combined_loss.py
--rw-r--r--   0 runner    (1001) docker     (122)      653 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/cv/ocr/ctc_loss.py
--rw-r--r--   0 runner    (1001) docker     (122)     8596 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/cv/ocr/db_loss.py
--rw-r--r--   0 runner    (1001) docker     (122)    10118 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/cv/ocr/distillation_loss.py
--rw-r--r--   0 runner    (1001) docker     (122)     8245 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/cv/ocr/fce_loss.py
--rw-r--r--   0 runner    (1001) docker     (122)     4197 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/cv/ocr/pse_loss.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/loss/nlp/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/loss/nlp/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/metrics/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/metrics/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/metrics/common_metrics/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/metrics/common_metrics/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     2429 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/metrics/common_metrics/accuracy_metric.py
--rw-r--r--   0 runner    (1001) docker     (122)     1189 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/metrics/common_metrics/loss_metric.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/metrics/cv/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/metrics/cv/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/metrics/cv/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/metrics/cv/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    11464 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/metrics/cv/ocr/detection_metric.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/metrics/nlp/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/metrics/nlp/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     3214 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/metrics/nlp/sequence_classification_metric.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/
--rw-r--r--   0 runner    (1001) docker     (122)      135 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/cv/
--rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/cv/backbone/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     7084 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/det_conv_next.py
--rw-r--r--   0 runner    (1001) docker     (122)    10552 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/det_ghost_net.py
--rw-r--r--   0 runner    (1001) docker     (122)     7268 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/det_mobilenet_v3.py
--rw-r--r--   0 runner    (1001) docker     (122)     8440 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/det_resnet_vd.py
--rw-r--r--   0 runner    (1001) docker     (122)     7950 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/mobile_vit.py
--rw-r--r--   0 runner    (1001) docker     (122)     6021 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/rec_mobilenet_v3.py
--rw-r--r--   0 runner    (1001) docker     (122)     7126 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/rec_resnet_vd.py
--rw-r--r--   0 runner    (1001) docker     (122)    26071 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/backbone/ocr/transformer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/cv/heads/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/heads/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/cv/heads/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/heads/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     6172 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/heads/ocr/head.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/cv/necks/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/necks/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/cv/necks/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/necks/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    25098 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/necks/ocr/neck.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/cv/task_models/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/task_models/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/cv/task_models/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/task_models/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4487 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/task_models/ocr/ocr_detection.py
--rw-r--r--   0 runner    (1001) docker     (122)     1010 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/cv/task_models/ocr/ocr_recognition.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/
--rw-r--r--   0 runner    (1001) docker     (122)     5566 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/T5/
--rw-r--r--   0 runner    (1001) docker     (122)      545 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/T5/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    67175 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/T5/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     7488 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/T5/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    21421 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/T5/text2text_generation.py
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bart/
--rw-r--r--   0 runner    (1001) docker     (122)       62 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bart/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     2859 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bart/text_error_correction.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/
--rw-r--r--   0 runner    (1001) docker     (122)     1466 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    40425 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     7255 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)     4073 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/document_segmentation.py
--rw-r--r--   0 runner    (1001) docker     (122)      457 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/fill_mask.py
--rw-r--r--   0 runner    (1001) docker     (122)     6020 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/sentence_embedding.py
--rw-r--r--   0 runner    (1001) docker     (122)     7048 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/siamese_uie.py
--rw-r--r--   0 runner    (1001) docker     (122)     1413 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/text_classification.py
--rw-r--r--   0 runner    (1001) docker     (122)     1083 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/text_ranking.py
--rw-r--r--   0 runner    (1001) docker     (122)     2085 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/token_classification.py
--rw-r--r--   0 runner    (1001) docker     (122)     6867 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bert/word_alignment.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bloom/
--rw-r--r--   0 runner    (1001) docker     (122)      419 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bloom/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      457 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/bloom/backbone.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/canmt/
--rw-r--r--   0 runner    (1001) docker     (122)       51 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/canmt/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    52235 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/canmt/canmt_model.py
--rw-r--r--   0 runner    (1001) docker     (122)     2806 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/canmt/canmt_translation.py
--rw-r--r--   0 runner    (1001) docker     (122)    35688 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/canmt/sequence_generator.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/
--rwxr-xr-x   0 runner    (1001) docker     (122)      727 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    35473 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/codegeex.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     4000 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/codegeex_for_code_generation.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     3950 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/codegeex_for_code_translation.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     9997 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/inference.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     6111 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/tokenizer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/csanmt/
--rw-r--r--   0 runner    (1001) docker     (122)       46 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/csanmt/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    61912 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/csanmt/translation.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/
--rw-r--r--   0 runner    (1001) docker     (122)     1768 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    47942 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     6768 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    10330 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/fill_mask.py
--rw-r--r--   0 runner    (1001) docker     (122)    21421 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/tokenization.py
--rw-r--r--   0 runner    (1001) docker     (122)    10695 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/tokenization_fast.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/
--rw-r--r--   0 runner    (1001) docker     (122)      886 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     7089 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     1836 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/document_grounded_dialog_generate.py
--rw-r--r--   0 runner    (1001) docker     (122)     1216 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/document_grounded_dialog_rerank.py
--rw-r--r--   0 runner    (1001) docker     (122)     2203 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/document_grounded_dialog_retrieval.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/fid_T5/
--rw-r--r--   0 runner    (1001) docker     (122)     1079 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/fid_T5/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     8326 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/fid_T5/text_generation.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/fid_plug/
--rw-r--r--   0 runner    (1001) docker     (122)     1178 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/fid_plug/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    45082 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/fid_plug/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     5045 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/fid_plug/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)     6786 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/fid_plug/text_generation.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/
--rw-r--r--   0 runner    (1001) docker     (122)      537 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/generation/
--rw-r--r--   0 runner    (1001) docker     (122)       87 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/generation/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    10112 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/generation/strategies.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     5152 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/initialize.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/kernels/
--rw-r--r--   0 runner    (1001) docker     (122)     3263 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/kernels/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/quantization/
--rw-r--r--   0 runner    (1001) docker     (122)     2635 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/quantization/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1189 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/quantization/functional.py
--rw-r--r--   0 runner    (1001) docker     (122)     4510 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/quantization/layers.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    13746 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/text_generation.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt2/
--rw-r--r--   0 runner    (1001) docker     (122)      417 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt2/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      450 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt2/backbone.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/
--rw-r--r--   0 runner    (1001) docker     (122)      799 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    15741 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     8971 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    51463 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/distributed_gpt3.py
--rw-r--r--   0 runner    (1001) docker     (122)     2874 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/text_generation.py
--rw-r--r--   0 runner    (1001) docker     (122)     2586 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/tokenizer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/
--rw-r--r--   0 runner    (1001) docker     (122)      821 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    13127 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     5198 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/checkpointing.py
--rw-r--r--   0 runner    (1001) docker     (122)     4930 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    49319 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/distributed_gpt_moe.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1194 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/experts.py
--rw-r--r--   0 runner    (1001) docker     (122)     3504 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/layer.py
--rw-r--r--   0 runner    (1001) docker     (122)     2553 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/mappings.py
--rw-r--r--   0 runner    (1001) docker     (122)    23754 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/sharded_moe.py
--rw-r--r--   0 runner    (1001) docker     (122)     4110 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     2686 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/text_generation.py
--rw-r--r--   0 runner    (1001) docker     (122)     2277 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/tokenizer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_neo/
--rw-r--r--   0 runner    (1001) docker     (122)      421 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_neo/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      465 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_neo/backbone.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/hf_transformers/
--rw-r--r--   0 runner    (1001) docker     (122)      435 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/hf_transformers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4715 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/hf_transformers/backbone.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/llama/
--rw-r--r--   0 runner    (1001) docker     (122)      813 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/llama/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    29152 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/llama/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     4645 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/llama/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    11299 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/llama/convert_llama_weights_to_hf.py
--rw-r--r--   0 runner    (1001) docker     (122)     7164 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/llama/text_generation.py
--rw-r--r--   0 runner    (1001) docker     (122)    10280 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/llama/tokenization.py
--rw-r--r--   0 runner    (1001) docker     (122)     4667 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/llama/tokenization_fast.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/lstm/
--rw-r--r--   0 runner    (1001) docker     (122)      557 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/lstm/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1273 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/lstm/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     2133 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/lstm/token_classification.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/megatron_bert/
--rw-r--r--   0 runner    (1001) docker     (122)      635 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/megatron_bert/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    39816 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/megatron_bert/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     6546 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/megatron_bert/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    12392 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/megatron_bert/fill_mask.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/
--rw-r--r--   0 runner    (1001) docker     (122)      569 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    28113 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/arguments.py
--rw-r--r--   0 runner    (1001) docker     (122)    28162 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/blocklm_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    17992 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/configure_data.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/
--rw-r--r--   0 runner    (1001) docker     (122)    13653 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    20307 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/corpora.py
--rw-r--r--   0 runner    (1001) docker     (122)    45713 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/datasets.py
--rw-r--r--   0 runner    (1001) docker     (122)     3342 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/extraction.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     8459 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/file_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     9797 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/lazy_loader.py
--rw-r--r--   0 runner    (1001) docker     (122)     7221 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/samplers.py
--rw-r--r--   0 runner    (1001) docker     (122)     4661 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/sp_tokenizer.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    53304 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/tokenization.py
--rw-r--r--   0 runner    (1001) docker     (122)    14549 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/tokenization_gpt2.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    15772 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/wordpiece.py
--rw-r--r--   0 runner    (1001) docker     (122)    21669 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/generation_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    16146 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/mglm_for_text_summarization.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/
--rwxr-xr-x   0 runner    (1001) docker     (122)      984 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     5443 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/distributed.py
--rw-r--r--   0 runner    (1001) docker     (122)     9967 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/downstream.py
--rw-r--r--   0 runner    (1001) docker     (122)    70249 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/modeling_bert.py
--rw-r--r--   0 runner    (1001) docker     (122)     8740 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/modeling_glm.py
--rw-r--r--   0 runner    (1001) docker     (122)     2531 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/prompt.py
--rw-r--r--   0 runner    (1001) docker     (122)    48886 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/transformer.py
--rw-r--r--   0 runner    (1001) docker     (122)     1955 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/process_grid.py
--rw-r--r--   0 runner    (1001) docker     (122)      203 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/run_test.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    13467 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/data_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    10871 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/eval_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/language_model/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/language_model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    10032 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/language_model/dataset.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     1900 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/language_model/detokenizer.py
--rw-r--r--   0 runner    (1001) docker     (122)     9960 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/language_model/finetune.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/seq2seq/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/seq2seq/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    28186 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/seq2seq/dataset.py
--rw-r--r--   0 runner    (1001) docker     (122)    22654 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/seq2seq/evaluate.py
--rw-r--r--   0 runner    (1001) docker     (122)     5821 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/seq2seq/finetune.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    55015 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/dataset.py
--rw-r--r--   0 runner    (1001) docker     (122)     3279 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/evaluate.py
--rw-r--r--   0 runner    (1001) docker     (122)     5071 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/finetune.py
--rw-r--r--   0 runner    (1001) docker     (122)    56975 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/pvp.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/test/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/test/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      950 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/test/test_block.py
--rw-r--r--   0 runner    (1001) docker     (122)      704 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/test/test_rel_shift.py
--rw-r--r--   0 runner    (1001) docker     (122)    17815 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/train_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    19029 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/palm_v2/
--rw-r--r--   0 runner    (1001) docker     (122)     1265 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/palm_v2/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     5526 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/palm_v2/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    29453 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/palm_v2/dureader_eval.py
--rw-r--r--   0 runner    (1001) docker     (122)    55432 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/palm_v2/text_generation.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/peer/
--rw-r--r--   0 runner    (1001) docker     (122)     1191 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/peer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    55762 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/peer/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)    11713 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/peer/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)     6166 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/peer/sas_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     4936 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/peer/text_classification.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug/
--rwxr-xr-x   0 runner    (1001) docker     (122)     3321 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug/AnnealingLR.py
--rw-r--r--   0 runner    (1001) docker     (122)      607 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    41203 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)    11791 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    10917 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug/distributed_plug.py
--rw-r--r--   0 runner    (1001) docker     (122)     8377 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug/generator.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/
--rw-r--r--   0 runner    (1001) docker     (122)     1356 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     7668 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/adv_utils.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    47482 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     7953 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    10875 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/text_classification.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/
--rw-r--r--   0 runner    (1001) docker     (122)     1487 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    37917 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     6363 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)     4136 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/document_segmentation.py
--rw-r--r--   0 runner    (1001) docker     (122)    11015 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/fill_mask.py
--rw-r--r--   0 runner    (1001) docker     (122)     7142 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/tokenization.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/
--rw-r--r--   0 runner    (1001) docker     (122)      934 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1211 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)     3728 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/dialog_intent_prediction.py
--rw-r--r--   0 runner    (1001) docker     (122)     4274 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/dialog_modeling.py
--rw-r--r--   0 runner    (1001) docker     (122)    16545 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/dialog_state_tracking.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/
--rw-r--r--   0 runner    (1001) docker     (122)      371 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    10230 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/gen_unified_transformer.py
--rw-r--r--   0 runner    (1001) docker     (122)    10706 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/generator.py
--rw-r--r--   0 runner    (1001) docker     (122)     7451 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/intent_unified_transformer.py
--rw-r--r--   0 runner    (1001) docker     (122)     2934 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/model_base.py
--rw-r--r--   0 runner    (1001) docker     (122)     1186 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/tokenization_space.py
--rw-r--r--   0 runner    (1001) docker     (122)    11875 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/unified_transformer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     2347 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/embedder.py
--rw-r--r--   0 runner    (1001) docker     (122)      905 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/feedforward.py
--rw-r--r--   0 runner    (1001) docker     (122)     1670 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/functions.py
--rw-r--r--   0 runner    (1001) docker     (122)     3346 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/multihead_attention.py
--rw-r--r--   0 runner    (1001) docker     (122)     1871 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/transformer_block.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_cn/
--rw-r--r--   0 runner    (1001) docker     (122)      476 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_cn/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    44430 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_cn/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     5194 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_cn/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    30089 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_cn/table_question_answering.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_en/
--rw-r--r--   0 runner    (1001) docker     (122)      439 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_en/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     3648 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_en/text_to_sql.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/
--rw-r--r--   0 runner    (1001) docker     (122)     1671 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     7670 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/adv_utils.py
--rwxr-xr-x   0 runner    (1001) docker     (122)    40552 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     7571 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    26721 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/faq_question_answering.py
--rw-r--r--   0 runner    (1001) docker     (122)    12179 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/fill_mask.py
--rw-r--r--   0 runner    (1001) docker     (122)    11860 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/text_classification.py
--rw-r--r--   0 runner    (1001) docker     (122)    10990 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/token_classification.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/unite/
--rw-r--r--   0 runner    (1001) docker     (122)      572 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/unite/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      360 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/unite/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)    18097 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/unite/translation_evaluation.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/use/
--rw-r--r--   0 runner    (1001) docker     (122)      492 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/use/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     5082 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/use/transformer.py
--rw-r--r--   0 runner    (1001) docker     (122)     5753 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/use/user_satisfaction_estimation.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/veco/
--rw-r--r--   0 runner    (1001) docker     (122)     1476 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/veco/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4030 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/veco/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     1189 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/veco/configuration.py
--rw-r--r--   0 runner    (1001) docker     (122)     4296 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/veco/fill_mask.py
--rw-r--r--   0 runner    (1001) docker     (122)     6622 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/veco/text_classification.py
--rw-r--r--   0 runner    (1001) docker     (122)     4153 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/veco/token_classification.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/xlm_roberta/
--rw-r--r--   0 runner    (1001) docker     (122)     1153 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/xlm_roberta/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    42850 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/xlm_roberta/backbone.py
--rw-r--r--   0 runner    (1001) docker     (122)     7644 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/backbone/xlm_roberta/configuration.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/heads/
--rw-r--r--   0 runner    (1001) docker     (122)      608 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/heads/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    24860 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/heads/crf_head.py
--rw-r--r--   0 runner    (1001) docker     (122)     6652 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/heads/fill_mask_head.py
--rw-r--r--   0 runner    (1001) docker     (122)     4926 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/heads/infromation_extraction_head.py
--rw-r--r--   0 runner    (1001) docker     (122)     1702 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/heads/text_classification_head.py
--rw-r--r--   0 runner    (1001) docker     (122)      858 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/heads/text_generation_head.py
--rw-r--r--   0 runner    (1001) docker     (122)     1749 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/heads/text_ranking_head.py
--rw-r--r--   0 runner    (1001) docker     (122)     2267 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/heads/token_classification_head.py
--rw-r--r--   0 runner    (1001) docker     (122)      802 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/heads/torch_pretrain_head.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/
--rw-r--r--   0 runner    (1001) docker     (122)     1400 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     5163 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/feature_extraction.py
--rw-r--r--   0 runner    (1001) docker     (122)     2647 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/fill_mask.py
--rw-r--r--   0 runner    (1001) docker     (122)      715 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/information_extraction.py
--rw-r--r--   0 runner    (1001) docker     (122)    28842 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/task_model.py
--rw-r--r--   0 runner    (1001) docker     (122)     1830 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/text_classification.py
--rw-r--r--   0 runner    (1001) docker     (122)     8654 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/text_generation.py
--rw-r--r--   0 runner    (1001) docker     (122)     1916 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/text_ranking.py
--rw-r--r--   0 runner    (1001) docker     (122)     4764 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/models/nlp/task_models/token_classification.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/optimizer/
--rw-r--r--   0 runner    (1001) docker     (122)      579 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/optimizer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     7110 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/optimizer/child_tuning_adamw_optimizer.py
--rw-r--r--   0 runner    (1001) docker     (122)     2871 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/optimizer/warmup.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/pipelines/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/pipelines/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/
--rw-r--r--   0 runner    (1001) docker     (122)      637 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/cv/
--rw-r--r--   0 runner    (1001) docker     (122)     1843 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/cv/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/cv/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/cv/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     9062 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/cv/ocr/postprocessors.py
--rw-r--r--   0 runner    (1001) docker     (122)     2853 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/cv/ocr/preprocessor.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/nlp/
--rw-r--r--   0 runner    (1001) docker     (122)     5913 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/nlp/space/
--rw-r--r--   0 runner    (1001) docker     (122)     1166 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1858 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/args.py
--rw-r--r--   0 runner    (1001) docker     (122)     1504 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/batch.py
--rw-r--r--   0 runner    (1001) docker     (122)     3566 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/data_loader.py
--rw-r--r--   0 runner    (1001) docker     (122)     2634 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/dialog_intent_prediction_preprocessor.py
--rw-r--r--   0 runner    (1001) docker     (122)     2722 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/dialog_modeling_preprocessor.py
--rw-r--r--   0 runner    (1001) docker     (122)     5264 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/dialog_state_tracking_preprocessor.py
--rw-r--r--   0 runner    (1001) docker     (122)    56779 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/dst_processors.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/nlp/space/fields/
--rw-r--r--   0 runner    (1001) docker     (122)      539 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/fields/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    33816 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/fields/gen_field.py
--rw-r--r--   0 runner    (1001) docker     (122)    42399 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/fields/intent_field.py
--rw-r--r--   0 runner    (1001) docker     (122)     1097 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/lazy_dataset.py
--rw-r--r--   0 runner    (1001) docker     (122)     1881 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/preprocess.py
--rw-r--r--   0 runner    (1001) docker     (122)     1559 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/sampler.py
--rw-r--r--   0 runner    (1001) docker     (122)     2084 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/tensorlistdataset.py
--rw-r--r--   0 runner    (1001) docker     (122)    24749 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space/tokenizer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/
--rw-r--r--   0 runner    (1001) docker     (122)      601 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/fields/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/fields/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4886 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/fields/database.py
--rw-r--r--   0 runner    (1001) docker     (122)    15817 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/fields/schema_link.py
--rw-r--r--   0 runner    (1001) docker     (122)     4837 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/fields/struct.py
--rw-r--r--   0 runner    (1001) docker     (122)     4106 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/table_question_answering_preprocessor.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_en/
--rw-r--r--   0 runner    (1001) docker     (122)      793 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_en/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4830 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_en/conversational_text_to_sql_preprocessor.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/
--rw-r--r--   0 runner    (1001) docker     (122)      765 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    21518 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/common_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    12449 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/parse.py
--rw-r--r--   0 runner    (1001) docker     (122)     1329 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/preprocess_dataset.py
--rw-r--r--   0 runner    (1001) docker     (122)     2111 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/process_dataset.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/processors/nlp/text_classification/
--rw-r--r--   0 runner    (1001) docker     (122)      102 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/text_classification/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     8835 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/processors/nlp/text_classification/preprocessor.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/registry/
--rw-r--r--   0 runner    (1001) docker     (122)      840 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      687 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/dataset.py
--rw-r--r--   0 runner    (1001) docker     (122)      635 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/exporter.py
--rw-r--r--   0 runner    (1001) docker     (122)      260 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/hook.py
--rw-r--r--   0 runner    (1001) docker     (122)      262 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/loss.py
--rw-r--r--   0 runner    (1001) docker     (122)     1996 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/lr_scheduler.py
--rw-r--r--   0 runner    (1001) docker     (122)      918 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/metric.py
--rw-r--r--   0 runner    (1001) docker     (122)     3457 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/model.py
--rw-r--r--   0 runner    (1001) docker     (122)     1508 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/optimizer.py
--rw-r--r--   0 runner    (1001) docker     (122)      629 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/parallel.py
--rw-r--r--   0 runner    (1001) docker     (122)      630 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/pipeline.py
--rw-r--r--   0 runner    (1001) docker     (122)      889 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/processor.py
--rw-r--r--   0 runner    (1001) docker     (122)     6458 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/registry.py
--rw-r--r--   0 runner    (1001) docker     (122)      705 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/registry/trainer.py
--rw-r--r--   0 runner    (1001) docker     (122)      554 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/train.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/trainers/
--rw-r--r--   0 runner    (1001) docker     (122)      572 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/trainers/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/trainers/cv/
--rw-r--r--   0 runner    (1001) docker     (122)      430 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/trainers/cv/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/trainers/cv/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)      437 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/trainers/cv/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1824 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/trainers/cv/ocr/trainer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/trainers/nlp/
--rw-r--r--   0 runner    (1001) docker     (122)      495 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/trainers/nlp/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/trainers/nlp/text_classification/
--rw-r--r--   0 runner    (1001) docker     (122)       48 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/trainers/nlp/text_classification/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1704 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/trainers/nlp/text_classification/trainer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/tuner/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/tuner/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    38904 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/tuner/control_sd_lora.py
--rw-r--r--   0 runner    (1001) docker     (122)    24008 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/tuner/lora.py
--rw-r--r--   0 runner    (1001) docker     (122)     8840 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/tuner/sd_lora.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    29034 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ast_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/audio/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/audio/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    11685 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/audio/audio_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     2378 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/audio/tts_exceptions.py
--rw-r--r--   0 runner    (1001) docker     (122)    26336 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/checkpoint.py
--rw-r--r--   0 runner    (1001) docker     (122)     2522 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/chinese_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/cli/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cli/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      596 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cli/cli.py
--rw-r--r--   0 runner    (1001) docker     (122)     5553 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cli/cli_argument_parser.py
--rw-r--r--   0 runner    (1001) docker     (122)     4313 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cli/pipeline.py
--rw-r--r--   0 runner    (1001) docker     (122)     3247 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cli/plugins.py
--rw-r--r--   0 runner    (1001) docker     (122)    17525 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cli/training_args.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/config/
--rw-r--r--   0 runner    (1001) docker     (122)     6700 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    25420 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/config/config.py
--rw-r--r--   0 runner    (1001) docker     (122)     1002 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/config/config_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/constants/
--rw-r--r--   0 runner    (1001) docker     (122)      174 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/constants/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    55775 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/constants/constants.py
--rw-r--r--   0 runner    (1001) docker     (122)      518 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/constants/default_constant.py
--rw-r--r--   0 runner    (1001) docker     (122)     8091 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/constants/hub_constant.py
--rw-r--r--   0 runner    (1001) docker     (122)    24737 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/constants/map_constant.py
--rw-r--r--   0 runner    (1001) docker     (122)    49162 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/constants/output_constant.py
--rw-r--r--   0 runner    (1001) docker     (122)    10468 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/constants/pipeline_inputs.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/cv/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    23161 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/image_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/cv/motion_utils/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/motion_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     2307 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/motion_utils/motion_process.py
--rw-r--r--   0 runner    (1001) docker     (122)     3847 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/motion_utils/plot_script.py
--rw-r--r--   0 runner    (1001) docker     (122)     4290 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/motion_utils/rotation_conversions.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/cv/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)      138 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/ocr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    10826 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/ocr/common_modules.py
--rw-r--r--   0 runner    (1001) docker     (122)     3413 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/ocr/ocr_show_img.py
--rw-r--r--   0 runner    (1001) docker     (122)     7922 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/cv/ocr/utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     3103 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/data_collators.py
--rw-r--r--   0 runner    (1001) docker     (122)     1186 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/data_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/dataset/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/dataset/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/dataset/collate_fns/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/dataset/collate_fns/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/dataset/collate_fns/cv/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/dataset/collate_fns/cv/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      914 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/dataset/collate_fns/cv/ocr_collate_fn.py
--rw-r--r--   0 runner    (1001) docker     (122)     4112 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/dataset/dataset_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     5489 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/dataset/maxcompute_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     3689 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/device.py
--rw-r--r--   0 runner    (1001) docker     (122)      736 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/exporter_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/fileio/
--rw-r--r--   0 runner    (1001) docker     (122)       71 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     9861 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/caching.py
--rw-r--r--   0 runner    (1001) docker     (122)    10190 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/file.py
--rw-r--r--   0 runner    (1001) docker     (122)     1208 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/file_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/fileio/format/
--rw-r--r--   0 runner    (1001) docker     (122)       92 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/format/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      404 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/format/base.py
--rw-r--r--   0 runner    (1001) docker     (122)     1000 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/format/json.py
--rw-r--r--   0 runner    (1001) docker     (122)      996 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/format/json_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    13853 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/format/jsonplus.py
--rw-r--r--   0 runner    (1001) docker     (122)      619 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/format/yaml.py
--rw-r--r--   0 runner    (1001) docker     (122)     4203 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/fileio/io.py
--rw-r--r--   0 runner    (1001) docker     (122)     8117 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/git.py
--rw-r--r--   0 runner    (1001) docker     (122)    15723 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/import_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    10946 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/inference.py
--rw-r--r--   0 runner    (1001) docker     (122)    24911 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/input_output.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/logger/
--rw-r--r--   0 runner    (1001) docker     (122)       50 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/logger/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1196 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/logger/log_buffer.py
--rw-r--r--   0 runner    (1001) docker     (122)     2648 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/logger/logger.py
--rw-r--r--   0 runner    (1001) docker     (122)     7649 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/megatron_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     2335 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/metric.py
--rw-r--r--   0 runner    (1001) docker     (122)     5037 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/model_tag.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/nlp/
--rw-r--r--   0 runner    (1001) docker     (122)      446 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     4424 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/distributed.py
--rwxr-xr-x   0 runner    (1001) docker     (122)     4526 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/load_checkpoint.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/nlp/space/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     1858 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space/args.py
--rw-r--r--   0 runner    (1001) docker     (122)    11767 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space/clean_dataset.py
--rw-r--r--   0 runner    (1001) docker     (122)     1388 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space/criterions.py
--rw-r--r--   0 runner    (1001) docker     (122)    11201 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space/db_ops.py
--rw-r--r--   0 runner    (1001) docker     (122)     6123 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space/ontology.py
--rw-r--r--   0 runner    (1001) docker     (122)      146 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space/scores.py
--rw-r--r--   0 runner    (1001) docker     (122)     6302 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space/utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     1022 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space/utils_dst.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/nlp/space_T_en/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space_T_en/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      826 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/space_T_en/utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     2326 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/nlp/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/ops/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/ops/ailut/
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/ops/ailut/Ailut/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/ailut/Ailut/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/ops/ailut/Ailut/csrc/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/ailut/Ailut/csrc/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      105 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/ailut/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4314 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/ailut/pyinterfaces.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/
--rw-r--r--   0 runner    (1001) docker     (122)       55 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/functions/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/functions/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     2874 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/functions/quadtree_attention.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/modules/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/modules/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    13876 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/modules/quadtree_attention.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/src/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/src/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    20417 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/output.py
--rw-r--r--   0 runner    (1001) docker     (122)      988 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/parallel_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     3271 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/pipeline_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    39423 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/plugins.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/pretrained/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/pretrained/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/pretrained/converter/
--rw-r--r--   0 runner    (1001) docker     (122)       21 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/pretrained/converter/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/pretrained/converter/cv/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/pretrained/converter/cv/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/pretrained/converter/cv/ocr_detection/
--rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/pretrained/converter/cv/ocr_detection/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     3000 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/pretrained/converter/cv/ocr_detection/paddle_torch.py
--rw-r--r--   0 runner    (1001) docker     (122)      156 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/pretrained/converter/cv/ocr_detection/torch_torch.py
--rw-r--r--   0 runner    (1001) docker     (122)     1532 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/pretrained/utils.py
--rw-r--r--   0 runner    (1001) docker     (122)      564 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/print_info.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/processor/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/processor/postprocessors/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/postprocessors/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     6939 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/common.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    13028 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/augment.py
--rw-r--r--   0 runner    (1001) docker     (122)    27276 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/fce_aug.py
--rw-r--r--   0 runner    (1001) docker     (122)    26193 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/fce_target.py
--rw-r--r--   0 runner    (1001) docker     (122)     2264 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/iaa_augment.py
--rw-r--r--   0 runner    (1001) docker     (122)     5272 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/make_border_map.py
--rw-r--r--   0 runner    (1001) docker     (122)     4805 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/make_shrink_map.py
--rw-r--r--   0 runner    (1001) docker     (122)     7381 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/random_crop_data.py
--rw-r--r--   0 runner    (1001) docker     (122)     3263 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/preprocessor_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     4175 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/processor/preprocessors/transformers_tokenizer.py
--rw-r--r--   0 runner    (1001) docker     (122)     6158 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/service_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     2429 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/task_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     1543 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/tensor_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/test_utils/
--rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/test_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)    30141 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/test_utils/regress_test_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    12478 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/test_utils/test_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     1209 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/timer.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils/tools/
--rw-r--r--   0 runner    (1001) docker     (122)       49 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/tools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)      676 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/tools/eval.py
--rw-r--r--   0 runner    (1001) docker     (122)    11068 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/torch_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)      288 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/trainer_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)      546 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/trie.py
--rw-r--r--   0 runner    (1001) docker     (122)     1645 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/type_assert.py
--rw-r--r--   0 runner    (1001) docker     (122)      354 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/typing.py
--rw-r--r--   0 runner    (1001) docker     (122)      729 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils/url_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon/utils_/
--rw-r--r--   0 runner    (1001) docker     (122)     2702 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4790 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/attack.py
--rw-r--r--   0 runner    (1001) docker     (122)     2373 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/char_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    12460 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/conlleval.py
--rw-r--r--   0 runner    (1001) docker     (122)     2055 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/constants.py
--rw-r--r--   0 runner    (1001) docker     (122)     1249 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/data_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     5286 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/dictionary.py
--rw-r--r--   0 runner    (1001) docker     (122)     3814 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/ema.py
--rw-r--r--   0 runner    (1001) docker     (122)     2379 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/email_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)      668 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/encrypt_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)      674 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/environment_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    11031 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/file_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     4488 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/gpu_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     1283 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/ip_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)      627 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/json_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    21438 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/keyword_extract.py
--rw-r--r--   0 runner    (1001) docker     (122)     6569 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/label_studio_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     4481 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/loss_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    12341 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/midi_detector.py
--rw-r--r--   0 runner    (1001) docker     (122)     5159 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/minjoin.py
--rw-r--r--   0 runner    (1001) docker     (122)      661 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/model_ensemble.py
--rw-r--r--   0 runner    (1001) docker     (122)     4831 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/music.py
--rw-r--r--   0 runner    (1001) docker     (122)    21209 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/ner_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)      885 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/nextpow2.py
--rw-r--r--   0 runner    (1001) docker     (122)     5183 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/noise_reduction.py
--rw-r--r--   0 runner    (1001) docker     (122)     6305 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/note_plotter.py
--rw-r--r--   0 runner    (1001) docker     (122)    11716 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/number_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     2746 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/onset_frames_split.py
--rw-r--r--   0 runner    (1001) docker     (122)     6713 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/optimizer_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     1266 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/pdf_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     2366 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/prune.py
--rw-r--r--   0 runner    (1001) docker     (122)     2434 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/sampler.py
--rw-r--r--   0 runner    (1001) docker     (122)     9394 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/schedule_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)      584 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/semantic_scholar.py
--rw-r--r--   0 runner    (1001) docker     (122)     1663 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/sound_plot_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     3001 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/sound_recorder.py
--rw-r--r--   0 runner    (1001) docker     (122)     3194 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/states_machine.py
--rw-r--r--   0 runner    (1001) docker     (122)     3678 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/string_converter.py
--rw-r--r--   0 runner    (1001) docker     (122)    25723 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/string_similarity.py
--rw-r--r--   0 runner    (1001) docker     (122)    18063 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/string_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    10283 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/text_cluster.py
--rw-r--r--   0 runner    (1001) docker     (122)     1334 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/textrank.py
--rw-r--r--   0 runner    (1001) docker     (122)     8217 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/transformer_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)     6909 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/union_find.py
--rw-r--r--   0 runner    (1001) docker     (122)      532 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/wav_note.py
--rw-r--r--   0 runner    (1001) docker     (122)      653 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/wav_utils.py
--rw-r--r--   0 runner    (1001) docker     (122)    10737 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/word_discover.py
--rw-r--r--   0 runner    (1001) docker     (122)    41028 2023-07-12 06:20:33.000000 weathon-0.0.0.17/weathon/utils_/word_finder.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon.egg-info/
--rw-r--r--   0 runner    (1001) docker     (122)      859 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (122)    25488 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (122)       53 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (122)      504 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (122)        8 2023-07-12 06:21:16.000000 weathon-0.0.0.17/weathon.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/
+-rw-r--r--   0 runner    (1001) docker     (122)       53 2023-07-23 05:28:18.000000 weathon-0.0.0.18/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (122)      859 2023-07-23 05:28:19.000000 weathon-0.0.0.18/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (122)       72 2023-07-23 05:28:18.000000 weathon-0.0.0.18/README.md
+-rw-r--r--   0 runner    (1001) docker     (122)       38 2023-07-23 05:28:19.000000 weathon-0.0.0.18/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/
+-rw-r--r--   0 runner    (1001) docker     (122)      424 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/crawler/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/crawler/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/crawler/utils/
+-rw-r--r--   0 runner    (1001) docker     (122)      142 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/crawler/utils/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/crawler/utils/constants/
+-rw-r--r--   0 runner    (1001) docker     (122)       62 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/crawler/utils/constants/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1729 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/crawler/utils/header.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1552 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/crawler/utils/proxy.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/base/
+-rw-r--r--   0 runner    (1001) docker     (122)      418 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      353 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/cli.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1402 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/dataset.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7227 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)      339 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/loss.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2441 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/lr_scheduler.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2674 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/metric.py
+-rw-r--r--   0 runner    (1001) docker     (122)    13280 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/model.py
+-rw-r--r--   0 runner    (1001) docker     (122)    22217 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/pipeline.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8927 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/processor.py
+-rw-r--r--   0 runner    (1001) docker     (122)    26992 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/base/trainer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/dataset/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/dataset/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/dataset/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/dataset/cv/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/dataset/cv/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/dataset/cv/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4123 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/dataset/cv/ocr/datasets.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/dataset/nlp/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/dataset/nlp/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/dataset/nlp/text_classification/
+-rw-r--r--   0 runner    (1001) docker     (122)       91 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/dataset/nlp/text_classification/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1649 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/dataset/nlp/text_classification/datasets.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/error/
+-rw-r--r--   0 runner    (1001) docker     (122)       77 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/error/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6288 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/error/error.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4021 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/error/hub_error.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/hooks/
+-rw-r--r--   0 runner    (1001) docker     (122)     1776 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/hooks/checkpoint/
+-rw-r--r--   0 runner    (1001) docker     (122)      116 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/checkpoint/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    16044 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/checkpoint/checkpoint_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10643 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/checkpoint/checkpoint_processor.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5460 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/checkpoint/load_checkpoint_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)      724 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/clip_clamp_logit_scale_hook.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/hooks/compression/
+-rw-r--r--   0 runner    (1001) docker     (122)      560 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/compression/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5031 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/compression/sparsity_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7002 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/compression/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/hooks/distributed/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/distributed/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1349 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/distributed/ddp_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8027 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/distributed/deepspeed_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6663 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/distributed/megatron_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4361 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/early_stop_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3724 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/evaluation_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)      685 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/iter_timer_hook.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/hooks/logger/
+-rw-r--r--   0 runner    (1001) docker     (122)      609 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/logger/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4348 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/logger/base.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4412 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/logger/tensorboard_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7278 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/logger/text_logger_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6251 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/lr_scheduler_hook.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/hooks/optimizer/
+-rw-r--r--   0 runner    (1001) docker     (122)      693 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/optimizer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3084 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/optimizer/apex_optimizer_hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3596 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/optimizer/base.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3548 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/hooks/optimizer/torch_optimizer_hook.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/loss/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/loss/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/cv/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/loss/cv/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/cv/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      930 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/cv/ocr/combined_loss.py
+-rw-r--r--   0 runner    (1001) docker     (122)      653 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/cv/ocr/ctc_loss.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8602 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/cv/ocr/db_loss.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10118 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/cv/ocr/distillation_loss.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8245 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/cv/ocr/fce_loss.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4197 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/cv/ocr/pse_loss.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/loss/nlp/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/loss/nlp/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/metrics/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/metrics/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/metrics/common_metrics/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/metrics/common_metrics/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2447 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/metrics/common_metrics/accuracy_metric.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1204 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/metrics/common_metrics/loss_metric.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/metrics/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/metrics/cv/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/metrics/cv/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/metrics/cv/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11473 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/metrics/cv/ocr/detection_metric.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/metrics/nlp/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/metrics/nlp/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3235 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/metrics/nlp/sequence_classification_metric.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/
+-rw-r--r--   0 runner    (1001) docker     (122)      141 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7093 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/det_conv_next.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10558 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/det_ghost_net.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7280 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/det_mobilenet_v3.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8449 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/det_resnet_vd.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7950 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/mobile_vit.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6024 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/rec_mobilenet_v3.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7129 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/rec_resnet_vd.py
+-rw-r--r--   0 runner    (1001) docker     (122)    26077 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/transformer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/cv/heads/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/heads/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/cv/heads/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/heads/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6181 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/heads/ocr/head.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/cv/necks/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/necks/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/cv/necks/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/necks/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    25107 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/necks/ocr/neck.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/cv/task_models/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/task_models/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/cv/task_models/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/task_models/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4490 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/task_models/ocr/ocr_detection.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1019 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/cv/task_models/ocr/ocr_recognition.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/
+-rw-r--r--   0 runner    (1001) docker     (122)     5354 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/T5/
+-rw-r--r--   0 runner    (1001) docker     (122)      548 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/T5/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    67193 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/T5/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7491 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/T5/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    21436 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/T5/text2text_generation.py
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bart/
+-rw-r--r--   0 runner    (1001) docker     (122)       62 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bart/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2868 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bart/text_error_correction.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/
+-rw-r--r--   0 runner    (1001) docker     (122)     1469 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    40446 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7258 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4091 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/document_segmentation.py
+-rw-r--r--   0 runner    (1001) docker     (122)      472 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/fill_mask.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6038 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/sentence_embedding.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7057 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/siamese_uie.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1428 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/text_classification.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1098 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/text_ranking.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2100 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/token_classification.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6882 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/word_alignment.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bloom/
+-rw-r--r--   0 runner    (1001) docker     (122)      422 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bloom/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      466 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bloom/backbone.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/canmt/
+-rw-r--r--   0 runner    (1001) docker     (122)       51 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/canmt/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    52235 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/canmt/canmt_model.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2821 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/canmt/canmt_translation.py
+-rw-r--r--   0 runner    (1001) docker     (122)    35688 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/canmt/sequence_generator.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/
+-rwxr-xr-x   0 runner    (1001) docker     (122)      730 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    35473 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/codegeex.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     4018 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/codegeex_for_code_generation.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     3965 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/codegeex_for_code_translation.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     9997 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/inference.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     6111 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/tokenizer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/csanmt/
+-rw-r--r--   0 runner    (1001) docker     (122)       46 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/csanmt/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    61927 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/csanmt/translation.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/
+-rw-r--r--   0 runner    (1001) docker     (122)     1771 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    47963 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6771 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10348 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/fill_mask.py
+-rw-r--r--   0 runner    (1001) docker     (122)    21421 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/tokenization.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10698 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/tokenization_fast.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/
+-rw-r--r--   0 runner    (1001) docker     (122)      889 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7092 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1866 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/document_grounded_dialog_generate.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1243 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/document_grounded_dialog_rerank.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2221 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/document_grounded_dialog_retrieval.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_T5/
+-rw-r--r--   0 runner    (1001) docker     (122)     1082 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_T5/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8356 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_T5/text_generation.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_plug/
+-rw-r--r--   0 runner    (1001) docker     (122)     1181 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_plug/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    45082 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_plug/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5045 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_plug/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6810 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_plug/text_generation.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/
+-rw-r--r--   0 runner    (1001) docker     (122)      540 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/generation/
+-rw-r--r--   0 runner    (1001) docker     (122)       87 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/generation/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    10112 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/generation/strategies.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     5152 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/initialize.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/kernels/
+-rw-r--r--   0 runner    (1001) docker     (122)     3263 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/kernels/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/quantization/
+-rw-r--r--   0 runner    (1001) docker     (122)     2635 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/quantization/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1189 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/quantization/functional.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4510 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/quantization/layers.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    13779 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/text_generation.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt2/
+-rw-r--r--   0 runner    (1001) docker     (122)      420 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt2/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      459 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt2/backbone.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/
+-rw-r--r--   0 runner    (1001) docker     (122)      802 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    15744 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8971 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    51475 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/distributed_gpt3.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2892 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/text_generation.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2586 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/tokenizer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/
+-rw-r--r--   0 runner    (1001) docker     (122)      824 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    13130 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5198 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/checkpointing.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4930 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    49331 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/distributed_gpt_moe.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1194 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/experts.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3504 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/layer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2553 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/mappings.py
+-rw-r--r--   0 runner    (1001) docker     (122)    23754 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/sharded_moe.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4110 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2707 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/text_generation.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2277 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/tokenizer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_neo/
+-rw-r--r--   0 runner    (1001) docker     (122)      424 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_neo/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      474 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_neo/backbone.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/hf_transformers/
+-rw-r--r--   0 runner    (1001) docker     (122)      438 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/hf_transformers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4730 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/hf_transformers/backbone.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/
+-rw-r--r--   0 runner    (1001) docker     (122)      816 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    29170 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4645 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11299 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/convert_llama_weights_to_hf.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7179 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/text_generation.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10283 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/tokenization.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4670 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/tokenization_fast.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/lstm/
+-rw-r--r--   0 runner    (1001) docker     (122)      560 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/lstm/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1288 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/lstm/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2148 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/lstm/token_classification.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/megatron_bert/
+-rw-r--r--   0 runner    (1001) docker     (122)      638 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/megatron_bert/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    39837 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/megatron_bert/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6549 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/megatron_bert/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    12407 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/megatron_bert/fill_mask.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/
+-rw-r--r--   0 runner    (1001) docker     (122)      572 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    28113 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/arguments.py
+-rw-r--r--   0 runner    (1001) docker     (122)    28162 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/blocklm_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    17992 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/configure_data.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/
+-rw-r--r--   0 runner    (1001) docker     (122)    13653 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    20310 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/corpora.py
+-rw-r--r--   0 runner    (1001) docker     (122)    45716 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/datasets.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3342 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/extraction.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     8459 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/file_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     9797 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/lazy_loader.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7221 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/samplers.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4661 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/sp_tokenizer.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    53304 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/tokenization.py
+-rw-r--r--   0 runner    (1001) docker     (122)    14549 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/tokenization_gpt2.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    15772 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/wordpiece.py
+-rw-r--r--   0 runner    (1001) docker     (122)    21669 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/generation_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    16164 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/mglm_for_text_summarization.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/
+-rwxr-xr-x   0 runner    (1001) docker     (122)      984 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     5443 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/distributed.py
+-rw-r--r--   0 runner    (1001) docker     (122)     9967 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/downstream.py
+-rw-r--r--   0 runner    (1001) docker     (122)    70249 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/modeling_bert.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8743 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/modeling_glm.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2531 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/prompt.py
+-rw-r--r--   0 runner    (1001) docker     (122)    48886 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/transformer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1955 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/process_grid.py
+-rw-r--r--   0 runner    (1001) docker     (122)      203 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/run_test.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    13467 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/data_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10871 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/eval_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/language_model/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/language_model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10032 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/language_model/dataset.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     1900 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/language_model/detokenizer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     9960 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/language_model/finetune.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/seq2seq/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/seq2seq/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    28186 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/seq2seq/dataset.py
+-rw-r--r--   0 runner    (1001) docker     (122)    22654 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/seq2seq/evaluate.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5821 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/seq2seq/finetune.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    55021 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/dataset.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3279 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/evaluate.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5071 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/finetune.py
+-rw-r--r--   0 runner    (1001) docker     (122)    56975 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/pvp.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/test/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/test/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      950 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/test/test_block.py
+-rw-r--r--   0 runner    (1001) docker     (122)      704 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/test/test_rel_shift.py
+-rw-r--r--   0 runner    (1001) docker     (122)    17815 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/train_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    19029 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/palm_v2/
+-rw-r--r--   0 runner    (1001) docker     (122)     1268 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/palm_v2/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5532 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/palm_v2/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    29453 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/palm_v2/dureader_eval.py
+-rw-r--r--   0 runner    (1001) docker     (122)    55450 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/palm_v2/text_generation.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/
+-rw-r--r--   0 runner    (1001) docker     (122)     1194 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    55771 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11716 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6166 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/sas_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4951 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/text_classification.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/
+-rwxr-xr-x   0 runner    (1001) docker     (122)     3321 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/AnnealingLR.py
+-rw-r--r--   0 runner    (1001) docker     (122)      610 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    41209 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11797 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10932 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/distributed_plug.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8377 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/generator.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/
+-rw-r--r--   0 runner    (1001) docker     (122)     1359 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7671 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/adv_utils.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    47506 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7956 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10890 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/text_classification.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/
+-rw-r--r--   0 runner    (1001) docker     (122)     1490 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    37938 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6366 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4154 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/document_segmentation.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11033 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/fill_mask.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7148 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/tokenization.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/
+-rw-r--r--   0 runner    (1001) docker     (122)      937 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1217 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3729 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/dialog_intent_prediction.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4278 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/dialog_modeling.py
+-rw-r--r--   0 runner    (1001) docker     (122)    16569 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/dialog_state_tracking.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/
+-rw-r--r--   0 runner    (1001) docker     (122)      371 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10230 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/gen_unified_transformer.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10706 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/generator.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7454 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/intent_unified_transformer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2937 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/model_base.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1189 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/tokenization_space.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11884 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/unified_transformer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2347 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/embedder.py
+-rw-r--r--   0 runner    (1001) docker     (122)      905 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/feedforward.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1670 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/functions.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3346 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/multihead_attention.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1871 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/transformer_block.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_cn/
+-rw-r--r--   0 runner    (1001) docker     (122)      479 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_cn/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    44439 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_cn/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5194 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_cn/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    30107 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_cn/table_question_answering.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_en/
+-rw-r--r--   0 runner    (1001) docker     (122)      442 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_en/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3672 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_en/text_to_sql.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/
+-rw-r--r--   0 runner    (1001) docker     (122)     1674 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7673 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/adv_utils.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)    40573 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7574 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    26745 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/faq_question_answering.py
+-rw-r--r--   0 runner    (1001) docker     (122)    12191 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/fill_mask.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11875 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/text_classification.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11005 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/token_classification.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/unite/
+-rw-r--r--   0 runner    (1001) docker     (122)      575 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/unite/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      366 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/unite/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)    18118 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/unite/translation_evaluation.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/use/
+-rw-r--r--   0 runner    (1001) docker     (122)      495 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/use/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5082 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/use/transformer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5771 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/use/user_satisfaction_estimation.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/
+-rw-r--r--   0 runner    (1001) docker     (122)     1479 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4051 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1192 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4314 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/fill_mask.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6643 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/text_classification.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4171 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/token_classification.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/xlm_roberta/
+-rw-r--r--   0 runner    (1001) docker     (122)     1156 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/xlm_roberta/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    42871 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/xlm_roberta/backbone.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7647 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/backbone/xlm_roberta/configuration.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/
+-rw-r--r--   0 runner    (1001) docker     (122)      611 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    24869 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/crf_head.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6661 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/fill_mask_head.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4935 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/infromation_extraction_head.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1711 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/text_classification_head.py
+-rw-r--r--   0 runner    (1001) docker     (122)      867 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/text_generation_head.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1758 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/text_ranking_head.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2276 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/token_classification_head.py
+-rw-r--r--   0 runner    (1001) docker     (122)      811 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/heads/torch_pretrain_head.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/
+-rw-r--r--   0 runner    (1001) docker     (122)     1403 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5178 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/feature_extraction.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2659 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/fill_mask.py
+-rw-r--r--   0 runner    (1001) docker     (122)      727 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/information_extraction.py
+-rw-r--r--   0 runner    (1001) docker     (122)    28869 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/task_model.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1842 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/text_classification.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8672 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/text_generation.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1925 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/text_ranking.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4773 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/models/nlp/task_models/token_classification.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/optimizer/
+-rw-r--r--   0 runner    (1001) docker     (122)      582 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/optimizer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7119 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/optimizer/child_tuning_adamw_optimizer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2880 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/optimizer/warmup.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/pipelines/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/pipelines/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/
+-rw-r--r--   0 runner    (1001) docker     (122)      640 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)     1846 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/cv/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/cv/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/cv/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     9065 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/cv/ocr/postprocessors.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2736 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/cv/ocr/preprocessor.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/
+-rw-r--r--   0 runner    (1001) docker     (122)     5916 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/
+-rw-r--r--   0 runner    (1001) docker     (122)     1169 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1858 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/args.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1504 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/batch.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3566 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/data_loader.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2652 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/dialog_intent_prediction_preprocessor.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2740 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/dialog_modeling_preprocessor.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5282 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/dialog_state_tracking_preprocessor.py
+-rw-r--r--   0 runner    (1001) docker     (122)    56779 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/dst_processors.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/fields/
+-rw-r--r--   0 runner    (1001) docker     (122)      542 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/fields/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    33831 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/fields/gen_field.py
+-rw-r--r--   0 runner    (1001) docker     (122)    42411 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/fields/intent_field.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1097 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/lazy_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1881 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/preprocess.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1559 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/sampler.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2084 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/tensorlistdataset.py
+-rw-r--r--   0 runner    (1001) docker     (122)    24749 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space/tokenizer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/
+-rw-r--r--   0 runner    (1001) docker     (122)      604 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/fields/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/fields/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4886 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/fields/database.py
+-rw-r--r--   0 runner    (1001) docker     (122)    15817 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/fields/schema_link.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4837 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/fields/struct.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4124 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/table_question_answering_preprocessor.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/
+-rw-r--r--   0 runner    (1001) docker     (122)      796 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4848 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/conversational_text_to_sql_preprocessor.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/
+-rw-r--r--   0 runner    (1001) docker     (122)      768 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    21521 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/common_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    12449 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/parse.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1329 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/preprocess_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2111 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/process_dataset.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/text_classification/
+-rw-r--r--   0 runner    (1001) docker     (122)      102 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/text_classification/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8859 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/processors/nlp/text_classification/preprocessor.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/registry/
+-rw-r--r--   0 runner    (1001) docker     (122)      646 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      693 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/dataset.py
+-rw-r--r--   0 runner    (1001) docker     (122)      641 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/exporter.py
+-rw-r--r--   0 runner    (1001) docker     (122)      263 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/hook.py
+-rw-r--r--   0 runner    (1001) docker     (122)      265 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/loss.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2002 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/lr_scheduler.py
+-rw-r--r--   0 runner    (1001) docker     (122)      924 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/metric.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3478 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/model.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1514 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/optimizer.py
+-rw-r--r--   0 runner    (1001) docker     (122)      635 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/parallel.py
+-rw-r--r--   0 runner    (1001) docker     (122)      636 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/pipeline.py
+-rw-r--r--   0 runner    (1001) docker     (122)      895 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/processor.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6464 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/registry.py
+-rw-r--r--   0 runner    (1001) docker     (122)      714 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/registry/trainer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/trainers/
+-rw-r--r--   0 runner    (1001) docker     (122)      575 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/trainers/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/trainers/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)      433 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/trainers/cv/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/trainers/cv/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)      440 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/trainers/cv/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1845 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/trainers/cv/ocr/trainer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/trainers/nlp/
+-rw-r--r--   0 runner    (1001) docker     (122)      498 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/trainers/nlp/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/trainers/nlp/text_classification/
+-rw-r--r--   0 runner    (1001) docker     (122)       48 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/trainers/nlp/text_classification/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1719 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/trainers/nlp/text_classification/trainer.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon/dl/tuner/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/tuner/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    38904 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/tuner/control_sd_lora.py
+-rw-r--r--   0 runner    (1001) docker     (122)    24008 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/tuner/lora.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8840 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/tuner/sd_lora.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/aigc/
+-rw-r--r--   0 runner    (1001) docker     (122)       44 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/aigc/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2319 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/aigc/langchain_chatbot_example.py
+-rw-r--r--   0 runner    (1001) docker     (122)      249 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/aigc/milvus_example.py
+-rw-r--r--   0 runner    (1001) docker     (122)      572 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/aigc/tiktoken_encode.py
+-rw-r--r--   0 runner    (1001) docker     (122)    29083 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ast_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/audio/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/audio/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11691 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/audio/audio_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2378 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/audio/tts_exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (122)    26354 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/checkpoint.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2522 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/chinese_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/cli/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cli/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      562 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cli/cli.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5553 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cli/cli_argument_parser.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4319 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cli/pipeline.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3253 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cli/plugins.py
+-rw-r--r--   0 runner    (1001) docker     (122)    17531 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cli/training_args.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/config/
+-rw-r--r--   0 runner    (1001) docker     (122)     6632 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    25432 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/config/config.py
+-rw-r--r--   0 runner    (1001) docker     (122)      985 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/config/config_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/constants/
+-rw-r--r--   0 runner    (1001) docker     (122)      174 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/constants/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    55775 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/constants/constants.py
+-rw-r--r--   0 runner    (1001) docker     (122)      927 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/constants/default_constant.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8091 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/constants/hub_constant.py
+-rw-r--r--   0 runner    (1001) docker     (122)    24740 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/constants/map_constant.py
+-rw-r--r--   0 runner    (1001) docker     (122)    49165 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/constants/output_constant.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10471 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/constants/pipeline_inputs.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    23167 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/image_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/cv/motion_utils/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/motion_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2307 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/motion_utils/motion_process.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3847 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/motion_utils/plot_script.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4290 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/motion_utils/rotation_conversions.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/cv/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)      147 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/ocr/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10826 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/ocr/common_modules.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3413 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/ocr/ocr_show_img.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7922 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/cv/ocr/utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3103 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/data_collators.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1189 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/data_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/dataset/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/dataset/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/dataset/collate_fns/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/dataset/collate_fns/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/dataset/collate_fns/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/dataset/collate_fns/cv/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      914 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/dataset/collate_fns/cv/ocr_collate_fn.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4115 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/dataset/dataset_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5489 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/dataset/maxcompute_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3695 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/device.py
+-rw-r--r--   0 runner    (1001) docker     (122)      739 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/exporter_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/
+-rw-r--r--   0 runner    (1001) docker     (122)       72 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     9867 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/caching.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10241 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/file.py
+-rw-r--r--   0 runner    (1001) docker     (122)      913 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/file_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/format/
+-rw-r--r--   0 runner    (1001) docker     (122)       92 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/format/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      404 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/format/base.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1000 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/format/json.py
+-rw-r--r--   0 runner    (1001) docker     (122)      996 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/format/json_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    13853 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/format/jsonplus.py
+-rw-r--r--   0 runner    (1001) docker     (122)      619 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/format/yaml.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4203 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/fileio/io.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8126 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/git.py
+-rw-r--r--   0 runner    (1001) docker     (122)    15726 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/import_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10952 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/inference.py
+-rw-r--r--   0 runner    (1001) docker     (122)    24929 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/input_output.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/logger/
+-rw-r--r--   0 runner    (1001) docker     (122)       64 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/logger/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1196 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/logger/log_buffer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2654 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/logger/logger.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7661 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/megatron_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2335 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/metric.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5037 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/model_tag.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/
+-rw-r--r--   0 runner    (1001) docker     (122)      449 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     4424 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/distributed.py
+-rwxr-xr-x   0 runner    (1001) docker     (122)     4526 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/load_checkpoint.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1858 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/args.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11767 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/clean_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1388 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/criterions.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11201 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/db_ops.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6123 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/ontology.py
+-rw-r--r--   0 runner    (1001) docker     (122)      146 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/scores.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6305 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1024 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space/utils_dst.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space_T_en/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space_T_en/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      828 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/space_T_en/utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2326 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/nlp/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/ops/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/ops/ailut/
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/ops/ailut/Ailut/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/ailut/Ailut/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/ops/ailut/Ailut/csrc/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/ailut/Ailut/csrc/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      105 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/ailut/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4314 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/ailut/pyinterfaces.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/
+-rw-r--r--   0 runner    (1001) docker     (122)       55 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/functions/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/functions/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2874 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/functions/quadtree_attention.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/modules/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/modules/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    13879 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/modules/quadtree_attention.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/src/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/src/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    20420 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/output.py
+-rw-r--r--   0 runner    (1001) docker     (122)      991 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/parallel_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3286 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/pipeline_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    39436 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/plugins.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/converter/
+-rw-r--r--   0 runner    (1001) docker     (122)       21 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/converter/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/converter/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/converter/cv/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/converter/cv/ocr_detection/
+-rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/converter/cv/ocr_detection/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3000 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/converter/cv/ocr_detection/paddle_torch.py
+-rw-r--r--   0 runner    (1001) docker     (122)      156 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/converter/cv/ocr_detection/torch_torch.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1541 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/pretrained/utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)      570 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/print_info.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/processor/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/processor/postprocessors/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/postprocessors/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6945 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/common.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    13028 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/augment.py
+-rw-r--r--   0 runner    (1001) docker     (122)    27276 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/fce_aug.py
+-rw-r--r--   0 runner    (1001) docker     (122)    26193 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/fce_target.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2264 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/iaa_augment.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5272 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/make_border_map.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4805 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/make_shrink_map.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7384 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/random_crop_data.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3272 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/preprocessor_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4184 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/transformers_tokenizer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6167 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/service_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2432 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/task_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1543 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/tensor_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/dl/utils/test_utils/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/test_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    30141 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/test_utils/regress_test_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    12490 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/test_utils/test_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1209 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/timer.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11071 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/torch_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)      291 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/trainer_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)      546 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/trie.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1645 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/type_assert.py
+-rw-r--r--   0 runner    (1001) docker     (122)      357 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/typing.py
+-rw-r--r--   0 runner    (1001) docker     (122)      732 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/dl/utils/url_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/quantization/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/quantization/base/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/base/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     7275 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/base/tick_down.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/quantization/data/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/data/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      359 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/data/download.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/quantization/data/history_data/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/data/history_data/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/quantization/data/tick_data/
+-rw-r--r--   0 runner    (1001) docker     (122)      119 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/data/tick_data/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2531 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/data/tick_data/neteasy_tick.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2825 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/data/tick_data/sina_tick.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3100 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/data/tick_data/tencent_tick.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/quantization/test/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/test/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      360 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/test/test_stock_code.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/quantization/utils/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/utils/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/quantization/utils/constants/
+-rw-r--r--   0 runner    (1001) docker     (122)       77 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/utils/constants/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)    28687 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/utils/constants/js_decode.py
+-rw-r--r--   0 runner    (1001) docker     (122)    94376 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/utils/constants/stock_codes.py
+-rw-r--r--   0 runner    (1001) docker     (122)   129125 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/utils/constants/trade_date.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1348 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/utils/stock_codes.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1005 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/utils/stock_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1713 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/quantization/utils/trade_date.py
+-rw-r--r--   0 runner    (1001) docker     (122)      557 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/train.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/utils/
+-rw-r--r--   0 runner    (1001) docker     (122)      135 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/utils/constants/
+-rw-r--r--   0 runner    (1001) docker     (122)       63 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/constants/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)      544 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/constants/emoji.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1349 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/constants/melody.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/utils/db/
+-rw-r--r--   0 runner    (1001) docker     (122)       30 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/db/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4159 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/db/redis.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5286 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/dictionary.py
+-rw-r--r--   0 runner    (1001) docker     (122)      879 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/encrypt_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/utils/fileio/
+-rw-r--r--   0 runner    (1001) docker     (122)      223 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/fileio/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3182 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/fileio/file_decomposer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4497 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/fileio/file_reader.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1672 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/fileio/file_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)      650 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/fileio/file_writer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1174 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/fileio/pdf_reader.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2702 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/logger.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5159 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/minjoin.py
+-rw-r--r--   0 runner    (1001) docker     (122)      792 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/notify.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/utils/strings/
+-rw-r--r--   0 runner    (1001) docker     (122)        0 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/strings/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6909 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils/union_find.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:19.000000 weathon-0.0.0.18/weathon/utils_/
+-rw-r--r--   0 runner    (1001) docker     (122)     2780 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4790 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/attack.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2373 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/char_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    12460 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/conlleval.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1249 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/data_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3814 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/ema.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2379 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/email_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)      674 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/environment_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4488 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/gpu_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1283 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/ip_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)      627 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/json_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    21444 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/keyword_extract.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6569 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/label_studio_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4481 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/loss_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    12344 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/midi_detector.py
+-rw-r--r--   0 runner    (1001) docker     (122)      661 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/model_ensemble.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4831 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/music.py
+-rw-r--r--   0 runner    (1001) docker     (122)    21209 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/ner_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)      885 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/nextpow2.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5186 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/noise_reduction.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6308 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/note_plotter.py
+-rw-r--r--   0 runner    (1001) docker     (122)    11719 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/number_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2749 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/onset_frames_split.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6713 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/optimizer_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2366 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/prune.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2434 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/sampler.py
+-rw-r--r--   0 runner    (1001) docker     (122)     9394 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/schedule_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)      584 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/semantic_scholar.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1663 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/sound_plot_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3018 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/sound_recorder.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3194 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/states_machine.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3681 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/string_converter.py
+-rw-r--r--   0 runner    (1001) docker     (122)    25723 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/string_similarity.py
+-rw-r--r--   0 runner    (1001) docker     (122)    18072 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/string_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10283 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/text_cluster.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1334 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/textrank.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8280 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/transformer_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)      546 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/wav_note.py
+-rw-r--r--   0 runner    (1001) docker     (122)      653 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/wav_utils.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10737 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/word_discover.py
+-rw-r--r--   0 runner    (1001) docker     (122)    41028 2023-07-23 05:27:41.000000 weathon-0.0.0.18/weathon/utils_/word_finder.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (122)      859 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (122)    28625 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (122)       53 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (122)      607 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (122)        8 2023-07-23 05:28:18.000000 weathon-0.0.0.18/weathon.egg-info/top_level.txt
```

### Comparing `weathon-0.0.0.17/PKG-INFO` & `weathon-0.0.0.18/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: weathon
-Version: 0.0.0.17
+Version: 0.0.0.18
 Summary: weathon: a personal Weapon Depot for python, so called weathon.
 Home-page: https://github.com/LiZhen0628
 Author: LiZhen
 Author-email: 16621660628@163.com
 License: UNKNOWN
 Description: # weathon_package
         a personal Weapon Depot for python, so called weathon.
```

### Comparing `weathon-0.0.0.17/weathon/base/dataset.py` & `weathon-0.0.0.18/weathon/dl/base/dataset.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from typing import Any, List, Union
 import torch.utils.data
 from torch.utils.data import ConcatDataset as TorchConcatDataset
 
-from weathon.utils.constants import ModeKeys
+from weathon.dl.utils.constants import ModeKeys
 
 
 
 class TorchCustomDataset(torch.utils.data.Dataset):
     """The custom dataset base class for all the torch-based task processors.
     """
```

### Comparing `weathon-0.0.0.17/weathon/base/hook.py` & `weathon-0.0.0.18/weathon/dl/base/hook.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-from weathon.utils.constants import TrainerStages, Priority
-from weathon.utils.import_utils import is_method_overridden
+from weathon.dl.utils.constants import TrainerStages, Priority
+from weathon.dl.utils.import_utils import is_method_overridden
 
 
 class BaseHook:
     """
     The Hook base class of any modelscope trainers. You can build your own hook inherited from this class.
 
     回调函数支持列表：
```

### Comparing `weathon-0.0.0.17/weathon/base/lr_scheduler.py` & `weathon-0.0.0.18/weathon/dl/base/lr_scheduler.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/base/metric.py` & `weathon-0.0.0.18/weathon/dl/base/metric.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/base/model.py` & `weathon-0.0.0.18/weathon/dl/base/model.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,22 +8,22 @@
 from dataclasses import fields
 from packaging import version
 
 import torch
 from torch import nn
 from torch.nn import DataParallel
 
-from weathon.utils.checkpoint import save_checkpoint, save_configuration, save_pretrained
-from weathon.utils.config.config import ConfigDict, Config
-from weathon.utils.constants import ModelFile, Tasks
-from weathon.utils.device import verify_device
-from weathon.utils.fileio.file_utils import func_receive_dict_inputs
-from weathon.utils.logger import get_logger
-from weathon.utils.nlp.distributed import DistributedDataParallel
-from weathon.registry import build_backbone, build_model
+from weathon.dl.registry import build_backbone, build_model
+from weathon.dl.utils.checkpoint import save_checkpoint, save_configuration, save_pretrained
+from weathon.dl.utils.config.config import ConfigDict, Config
+from weathon.dl.utils.constants import ModelFile, Tasks
+from weathon.dl.utils.device import verify_device
+from weathon.dl.utils.fileio.file_utils import func_receive_dict_inputs
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.nlp.distributed import DistributedDataParallel
 
 logger = get_logger()
 
 
 class BaseHead(ABC):
     """The head base class is for the tasks head method definition
 
@@ -111,17 +111,14 @@
                 read out of config in the `model_name_or_path`. This is useful when the model to be loaded is not
                 equal to the model saved.
                 For example, load a `backbone` into a `text-classification` model.
                 Other kwargs will be directly fed into the `model` key, to replace the default configs.
         Returns:
             A model instance.
 
-        Examples:
-            >>> from weathon.base.model import BaseModel
-            >>> BaseModel.from_pretrained('damo/nlp_structbert_backbone_base_std', task='text-classification')
         """
 
         logger.info(f'initialize model from {local_model_dir}')
 
         cfg = cfg_dict if cfg_dict else Config.from_file(osp.join(local_model_dir, ModelFile.CONFIGURATION_YAML))
         task_name = cfg.task
         if 'task' in kwargs:
```

### Comparing `weathon-0.0.0.17/weathon/base/pipeline.py` & `weathon-0.0.0.18/weathon/dl/base/pipeline.py`

 * *Files 4% similar despite different names*

```diff
@@ -6,23 +6,23 @@
 from multiprocessing import Pool
 from threading import Lock
 from typing import Any, Dict, Generator, List, Mapping, Union
 
 import numpy as np
 
 from .model import BaseModel
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Frameworks, ModelFile
-from weathon.utils.constants.output_constant import TASK_OUTPUTS
-from weathon.utils.constants.pipeline_inputs import TASK_INPUTS
-from weathon.utils.device import verify_device, create_device, device_placement
-from weathon.utils.import_utils import is_torch_available, is_tf_available
-from weathon.utils.logger import get_logger
-from weathon.utils.pipeline_utils import check_input_type
-from weathon.utils.torch_utils import compile_model
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Frameworks, ModelFile
+from weathon.dl.utils.constants.output_constant import TASK_OUTPUTS
+from weathon.dl.utils.constants.pipeline_inputs import TASK_INPUTS
+from weathon.dl.utils.device import verify_device, create_device, device_placement
+from weathon.dl.utils.import_utils import is_torch_available, is_tf_available
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.pipeline_utils import check_input_type
+from weathon.dl.utils.torch_utils import compile_model
 from .processor import BaseProcessor
 
 if is_torch_available():
     import torch
 
 if is_tf_available():
     pass
@@ -433,15 +433,15 @@
         self.model_pool = Pool(self.world_size)
 
         if 'master_ip' not in kwargs:
             kwargs['master_ip'] = '127.0.0.1'
         master_port = int(kwargs['master_port']
                           ) if 'master_port' in kwargs else random.randint(
             29500, 39500)
-        from weathon.utils.torch_utils import _find_free_port, _is_free_port
+        from weathon.dl.utils.torch_utils import _find_free_port, _is_free_port
         if not _is_free_port(master_port):
             master_port = _find_free_port()
         kwargs['master_port'] = str(master_port)
         # TODO: Pass ip and port to megatron_util for initialization
         os.environ['MASTER_ADDR'] = kwargs['master_ip']
         os.environ['MASTER_PORT'] = kwargs['master_port']
```

### Comparing `weathon-0.0.0.17/weathon/base/processor.py` & `weathon-0.0.0.18/weathon/dl/base/processor.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 import os
 from abc import ABC, abstractmethod
 from typing import Dict, Any, Optional, Union, Callable, Sequence
 
-from weathon.registry import build_preprocessor
-from weathon.utils.config.config import Config, ConfigDict
-from weathon.utils.constants import ModeKeys, DEFAULT_MODEL_REVISION, Tasks, ModelFile
-from weathon.utils.constants import PREPROCESSOR_MAP
-from weathon.utils.logger import get_logger
+from weathon.dl.registry.processor import build_preprocessor
+from weathon.dl.utils.config.config import Config, ConfigDict
+from weathon.dl.utils.constants import ModeKeys, DEFAULT_MODEL_REVISION, Tasks, ModelFile
+from weathon.dl.utils.constants import PREPROCESSOR_MAP
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 class BaseProcessor(ABC):
 
     def __init__(self, mode=ModeKeys.INFERENCE, *args, **kwargs):
@@ -99,18 +99,14 @@
                 This is useful when the preprocessor does not have a `type` field and the task to be used is not
                 equal to the task of which the model is saved.
                 Other kwargs will be directly fed into the preprocessor, to replace the default configs.
 
         Returns:
             The preprocessor instance.
 
-        Examples:
-            >>> from weathon.base.processors import Preprocessor
-            >>> Preprocessor.from_pretrained('damo/nlp_debertav2_fill-mask_chinese-base')
-
         """
 
         model_dir = model_name_or_path
         if cfg_dict is None:
             cfg = Config.from_file(os.path.join(model_dir, ModelFile.CONFIGURATION_YAML))
         else:
             cfg = cfg_dict
@@ -207,10 +203,10 @@
             if 'preprocessor' in config and config['preprocessor'] is not None:
                 if 'mode' in config['preprocessor']:
                     config['preprocessor']['mode'] = 'inference'
                 elif 'val' in config['preprocessor'] and 'mode' in config['preprocessor']['val']:
                     config['preprocessor']['val']['mode'] = 'inference'
 
             if save_config_function is None:
-                from weathon.utils.checkpoint import save_configuration
+                from weathon.dl.utils.checkpoint import save_configuration
                 save_config_function = save_configuration
             save_config_function(target_folder, config)
```

### Comparing `weathon-0.0.0.17/weathon/base/trainer.py` & `weathon-0.0.0.18/weathon/dl/base/trainer.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,44 +10,43 @@
 import numpy as np
 import torch
 from torch import nn
 from torch.utils.data import DataLoader, Dataset
 from torch.utils.data.dataloader import default_collate
 from tqdm import tqdm
 
-from weathon.base import BaseMetric
-from weathon.base.loss import BaseLoss
-from weathon.base.model import TorchModel, BaseModel, BaseOutput
-from weathon.base.processor import BaseProcessor
-from weathon.base.hook import BaseHook
-from weathon.base.dataset import TorchCustomDataset
-
-from weathon.utils.logger.log_buffer import LogBuffer
-from weathon.utils.logger import get_logger
-from weathon.registry import (
+from weathon.dl.base import BaseMetric
+from weathon.dl.base.loss import BaseLoss
+from weathon.dl.base.model import TorchModel, BaseModel, BaseOutput
+from weathon.dl.base.processor import BaseProcessor
+from weathon.dl.base.hook import BaseHook
+from weathon.dl.base.dataset import TorchCustomDataset
+from weathon.dl.registry.registry import build_from_cfg, default_group
+
+from weathon.dl.utils.logger import LogBuffer
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.registry import (
                                 HOOKS,
                                 build_model,
                                 build_metric, 
                                 build_optimizer, 
                                 build_lr_scheduler, 
                                 build_custom_dataset, 
-                                build_preprocessor,
-                                build_postprocessor
-                            )
-from weathon.registry.registry import build_from_cfg, default_group
-from weathon.utils.data_utils import to_device
-from weathon.utils.device import create_device
-from weathon.utils.fileio.file_utils import func_receive_dict_inputs, ensure_dir
-from weathon.utils.fileio.format.json_utils import JSONIteratorEncoder
-from weathon.utils.config.config import Config, ConfigDict
-from weathon.utils.constants import ModeKeys, TrainerStages, Priority, get_priority, DEFAULT_HOOKS_CONFIG, \
+                                build_preprocessor
+)
+from weathon.dl.utils.data_utils import to_device
+from weathon.dl.utils.device import create_device
+from weathon.dl.utils.fileio.file_utils import func_receive_dict_inputs, ensure_directory
+from weathon.dl.utils.fileio.format.json_utils import JSONIteratorEncoder
+from weathon.dl.utils.config.config import Config, ConfigDict
+from weathon.dl.utils.constants import ModeKeys, TrainerStages, Priority, get_priority, DEFAULT_HOOKS_CONFIG, \
     HOOK_KEY_CHAIN_MAP
-from weathon.utils.torch_utils import set_random_seed, is_master
-from weathon.registry.loss import build_loss
-from weathon.utils.trainer_utils import worker_init_fn
+from weathon.dl.utils.torch_utils import set_random_seed, is_master
+from weathon.dl.registry.loss import build_loss
+from weathon.dl.utils.trainer_utils import worker_init_fn
 
 logger = get_logger()
 
 
 class BaseTrainer(ABC):
     """ 训练器基类, 不可被实例化
     训练器基类定义一些必要的接口, 提供默认的实现方法, 比如解析配置文件和命令行参数.
@@ -165,15 +164,15 @@
                                                 self.cfg.safe_get('evaluation.val_iters_per_epoch',
                                                                   np.iinfo(np.int32).max))
         self.use_fp16 = kwargs.get("use_fp16", self.cfg.get("use_fp16", False))
         self.device = create_device(kwargs.get("device", self.cfg.get("device", "gpu")))
 
         # 训练工作目录
         self.work_dir = kwargs.get("work_dir", self.cfg.safe_get("work_dir", "./work_dir"))
-        ensure_dir(self.work_dir)
+        ensure_directory(self.work_dir)
 
         # logger
         log_file = os.path.join(self.work_dir, '{}.log'.format(self.timestamp))
         self.logger = get_logger(log_file=log_file, log_level=self.cfg.get('log_level', 'INFO'))
 
         # 训练组件
         # data
@@ -473,15 +472,15 @@
                                 collate_fn=collate_fn, pin_memory=pin_memory, drop_last=drop_last,
                                 worker_init_fn=init_fn)
 
         return dataloader
 
     def set_checkpoint_file_to_hook(self, checkpoint_path, load_all_state, strict):
         if checkpoint_path is not None:
-            from weathon.hooks import LoadCheckpointHook
+            from weathon.dl.hooks import LoadCheckpointHook
             load_ckpt_hooks = list(filter(lambda hook: isinstance(hook, LoadCheckpointHook), self.hooks))
             if len(load_ckpt_hooks) == 0:
                 load_ckpt_hook = LoadCheckpointHook()
                 self.register_hook(load_ckpt_hook)
                 load_ckpt_hooks.append(load_ckpt_hook)
             load_ckpt_hooks[0].checkpoint_file = checkpoint_path
             load_ckpt_hooks[0].load_all_state = load_all_state
@@ -614,15 +613,15 @@
 
     def evaluate(self, *args, **kwargs) -> Dict[str, float]:
         self._mode = ModeKeys.EVAL
         self.print_hook_info()
         checkpoint_path = kwargs.get("checkpoint_path", None)
         strict = kwargs.get("strict", None)
         if checkpoint_path is not None:
-            from weathon.hooks import LoadCheckpointHook
+            from weathon.dl.hooks import LoadCheckpointHook
             LoadCheckpointHook.load_checkpoint(checkpoint_path, self, strict=strict)
         self.eval_dataloader = self.build_dataloader(self.eval_dataset, self.cfg.safe_get("evaluation.dataloader"),
                                                      ModeKeys.EVAL)
         self.data_loader = self.eval_dataloader
         for metric_cls in self.metric_classes:
             metric_cls.trainer = self
         metric_values = self.evaluation_loop(self.eval_dataloader)
```

### Comparing `weathon-0.0.0.17/weathon/dataset/cv/ocr/datasets.py` & `weathon-0.0.0.18/weathon/dl/dataset/cv/ocr/datasets.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import cv2
 import os.path as osp
 from typing import Optional, List
 
-from weathon.base.dataset import TorchCustomDataset
-from weathon.registry import CUSTOM_DATASETS
-from weathon.utils.config.config import ConfigDict
-from weathon.utils.constants import Tasks, Datasets
+from weathon.dl.base.dataset import TorchCustomDataset
+from weathon.dl.registry import CUSTOM_DATASETS
+from weathon.dl.utils.config.config import ConfigDict
+from weathon.dl.utils.constants import Tasks, Datasets
 
 
 @CUSTOM_DATASETS.register_module(group_key=Tasks.ocr_detection, module_name=Datasets.icdar2015_ocr_detection)
 class IcdarOcrDetectionDataset(TorchCustomDataset):
 
     def __init__(self, dataset_cfg: Optional[ConfigDict] = None, *args, **kwargs):
         dataset_cfg = dataset_cfg if dataset_cfg else dict()
```

### Comparing `weathon-0.0.0.17/weathon/dataset/nlp/text_classification/datasets.py` & `weathon-0.0.0.18/weathon/dl/dataset/nlp/text_classification/datasets.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from typing import Optional
 
 import pandas as pd
 import os.path as osp
 
-from weathon.base.dataset import TorchCustomDataset
-from weathon.registry import CUSTOM_DATASETS
-from weathon.utils.config.config import ConfigDict
-from weathon.utils.constants import Tasks, Datasets
+from weathon.dl.base.dataset import TorchCustomDataset
+from weathon.dl.registry import CUSTOM_DATASETS
+from weathon.dl.utils.config.config import ConfigDict
+from weathon.dl.utils.constants import Tasks, Datasets
 
 
 @CUSTOM_DATASETS.register_module(group_key=Tasks.text_classification, module_name=Datasets.jd_sentiment_text_classification)
 class JDTextClassificationDataset(TorchCustomDataset):
 
     def __init__(self, dataset_cfg: Optional[ConfigDict] = None,*args, **kwargs):
         dataset_cfg = dataset_cfg if dataset_cfg else dict()
```

### Comparing `weathon-0.0.0.17/weathon/error/error.py` & `weathon-0.0.0.18/weathon/dl/error/error.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/error/hub_error.py` & `weathon-0.0.0.18/weathon/dl/error/hub_error.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from http import HTTPStatus
 
 import requests
 from requests.exceptions import HTTPError
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 class NotSupportError(Exception):
     pass
```

### Comparing `weathon-0.0.0.17/weathon/hooks/__init__.py` & `weathon-0.0.0.18/weathon/dl/hooks/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .early_stop_hook import EarlyStopHook
     from .compression import SparsityHook
     from .evaluation_hook import EvaluationHook
     from .iter_timer_hook import IterTimerHook
     from .logger import TensorboardHook, TextLoggerHook
```

### Comparing `weathon-0.0.0.17/weathon/hooks/checkpoint/checkpoint_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/checkpoint/checkpoint_hook.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,21 +3,21 @@
 import random
 import time
 from typing import Optional
 
 import numpy as np
 import torch
 
-from weathon.base import BaseHook
-from weathon.hooks.checkpoint.checkpoint_processor import CheckpointProcessor
-from weathon.registry import HOOKS
-from weathon.utils.constants import Priority, ModelFile, LogKeys
-from weathon.utils.constants import Hooks
-from weathon.utils.logger import get_logger
-from weathon.utils.torch_utils import is_master
+from weathon.dl.base import BaseHook
+from weathon.dl.hooks.checkpoint.checkpoint_processor import CheckpointProcessor
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Priority, ModelFile, LogKeys
+from weathon.dl.utils.constants import Hooks
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.torch_utils import is_master
 
 
 class CheckpointStrategy:
     by_epoch = 'by_epoch'
     by_step = 'by_step'
     no = 'no'
 
@@ -263,27 +263,27 @@
         self._best_metric = None
         self._best_ckpt_file = None
         self.save_file_name = save_file_name
         self.restore_best = restore_best
         self.history_checkpoints = set()
 
     def after_train_epoch(self, trainer):
-        from weathon.hooks import EvaluationHook
+        from weathon.dl.hooks import EvaluationHook
         eval_hook = trainer.get_hook(EvaluationHook)
         if len(eval_hook) == 0:
             self.logger.error(
                 'Trying to save the best checkpoint, but there is no evaluation, skipping.'
             )
 
         if eval_hook[0].last_eval_tag == (
                 'epoch', trainer.epoch) and self._should_save(trainer):
             self._do_save(trainer, 'by_epoch')
 
     def after_train_iter(self, trainer):
-        from weathon.hooks import EvaluationHook
+        from weathon.dl.hooks import EvaluationHook
         eval_hook = trainer.get_hook(EvaluationHook)
         if len(eval_hook) == 0:
             self.logger.error(
                 'Trying to save the best checkpoint, but there is no evaluation, skipping.'
             )
 
         if eval_hook[0].last_eval_tag == (
@@ -370,9 +370,9 @@
                 'The state_dict is not available, the best metric value will be affected.'
             )
 
     def after_run(self, trainer):
         if self.restore_best:
             # If restore_best is True, will call the LoadCheckpointHook to load the best checkpoint
             # for later evaluation or prediction.
-            from weathon.hooks import LoadCheckpointHook
+            from weathon.dl.hooks import LoadCheckpointHook
             LoadCheckpointHook.load_checkpoint(self._best_ckpt_file, trainer)
```

### Comparing `weathon-0.0.0.17/weathon/hooks/checkpoint/checkpoint_processor.py` & `weathon-0.0.0.18/weathon/dl/hooks/checkpoint/checkpoint_processor.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 import os
 import re
 import shutil
 
-from weathon.utils.constants import ModelFile
-from weathon.utils.constants import Pipelines
-from weathon.utils.checkpoint import (load_checkpoint, save_checkpoint,
+from weathon.dl.utils.constants import ModelFile
+from weathon.dl.utils.constants import Pipelines
+from weathon.dl.utils.checkpoint import (load_checkpoint, save_checkpoint,
                                          save_configuration)
-from weathon.utils.logger import get_logger
-from weathon.utils.torch_utils import is_master
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.torch_utils import is_master
 
 
 class CheckpointProcessor:
 
     TRAINER_STATE_SUFFIX = '_trainer_state.pth'
 
     MODEL_STATE_SUFFIX = '.pth'
```

### Comparing `weathon-0.0.0.17/weathon/hooks/checkpoint/load_checkpoint_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/checkpoint/load_checkpoint_hook.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 import random
 from typing import Optional
 
 import numpy as np
 import torch
 from packaging import version
 
-from weathon.base import BaseHook
-from weathon.hooks.checkpoint.checkpoint_processor import CheckpointProcessor
-from weathon.registry import HOOKS
-from weathon.utils.constants import Priority
-from weathon.utils.constants import Hooks
-from weathon.utils.logger import get_logger
+from weathon.dl.base import BaseHook
+from weathon.dl.hooks.checkpoint.checkpoint_processor import CheckpointProcessor
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Priority
+from weathon.dl.utils.constants import Hooks
+from weathon.dl.utils.logger import get_logger
 
 
 @HOOKS.register_module(module_name=Hooks.LoadCheckpointHook)
 class LoadCheckpointHook(BaseHook):
     """Load a checkpoint file at the beginning of training or evaluating.
 
     This hook does not need to be configured or saved in the config file.
```

### Comparing `weathon-0.0.0.17/weathon/hooks/clip_clamp_logit_scale_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/clip_clamp_logit_scale_hook.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import torch
 
-from weathon.base import BaseHook
-from weathon.base.trainer import BaseTrainer
-from weathon.registry import HOOKS
-from weathon.utils.constants import Hooks
+from weathon.dl.base import BaseHook
+from weathon.dl.base.trainer import BaseTrainer
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Hooks
 
 
 @HOOKS.register_module(module_name=Hooks.ClipClampLogitScaleHook)
 class ClipClampLogitScaleHook(BaseHook):
     """ClipClampLogitScaleHook hook which performs clamp on CLIP logit scale parameter after update"""
 
     def after_train_iter(self, trainer: BaseTrainer):
```

### Comparing `weathon-0.0.0.17/weathon/hooks/compression/__init__.py` & `weathon-0.0.0.18/weathon/dl/hooks/compression/__init__.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .sparsity_hook import SparsityHook
     from .utils import SparseLinear, convert_sparse_network
 
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/hooks/compression/sparsity_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/compression/sparsity_hook.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 import os
 
-from weathon.base import BaseHook
-from weathon.registry import HOOKS
-from weathon.utils.constants import Priority
-from weathon.utils.constants import Hooks
+from weathon.dl.base import BaseHook
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Priority
+from weathon.dl.utils.constants import Hooks
 
-from weathon.utils.checkpoint import save_checkpoint
-from weathon.utils.torch_utils import is_master
+from weathon.dl.utils.checkpoint import save_checkpoint
+from weathon.dl.utils.torch_utils import is_master
 
 
 @HOOKS.register_module(module_name=Hooks.SparsityHook)
 class SparsityHook(BaseHook):
 
     PRIORITY = Priority.HIGHEST
```

### Comparing `weathon-0.0.0.17/weathon/hooks/compression/utils.py` & `weathon-0.0.0.18/weathon/dl/hooks/compression/utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import torch
 import torch.nn as nn
 
-from weathon.utils.torch_utils import is_master
+from weathon.dl.utils.torch_utils import is_master
 
 
 class SparseBinarizer(torch.autograd.Function):
 
     @staticmethod
     def forward(ctx, mask_scores, sparsity):
         num_prune = int(mask_scores.numel() * sparsity)
```

### Comparing `weathon-0.0.0.17/weathon/hooks/distributed/ddp_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/distributed/ddp_hook.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,13 +1,13 @@
-from weathon.base import BaseHook
-from weathon.registry import HOOKS
-from weathon.utils.constants import Priority, DistributedParallelType
-from weathon.utils.constants import Hooks
-from weathon.utils.device import create_device
-from weathon.utils.torch_utils import get_local_rank, init_dist
+from weathon.dl.base import BaseHook
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Priority, DistributedParallelType
+from weathon.dl.utils.constants import Hooks
+from weathon.dl.utils.device import create_device
+from weathon.dl.utils.torch_utils import get_local_rank, init_dist
 
 
 @HOOKS.register_module(module_name=Hooks.DDPHook)
 class DDPHook(BaseHook):
 
     PRIORITY = Priority.LOW
```

### Comparing `weathon-0.0.0.17/weathon/hooks/distributed/deepspeed_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/distributed/deepspeed_hook.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,24 +2,24 @@
 import shutil
 
 import deepspeed
 import torch
 from deepspeed import DeepSpeedEngine
 from megatron_util import mpu, print_rank_0
 
-from weathon.utils.constants import Hooks
-from weathon.utils.checkpoint import save_checkpoint
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants import Hooks
+from weathon.dl.utils.checkpoint import save_checkpoint
+from weathon.dl.utils.logger import get_logger
 from .. import CheckpointHook, BestCkptSaverHook, LoadCheckpointHook
 from ..checkpoint.checkpoint_processor import CheckpointProcessor
 from ..lr_scheduler_hook import LrSchedulerProcessor
 from ..optimizer.base import OptimizerHook, OptimizerProcessor
 from ...base import BaseHook
-from ...registry import HOOKS
-from ...utils.constants import Priority
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Priority
 
 
 class DeepspeedProcessor(CheckpointProcessor, LrSchedulerProcessor,
                          OptimizerProcessor):
 
     _BIN_FILE_DIR = 'model'
```

### Comparing `weathon-0.0.0.17/weathon/hooks/distributed/megatron_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/distributed/megatron_hook.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,26 +1,26 @@
 import os
 import shutil
 
 import torch
 from megatron_util import mpu
 
-from weathon.base import BaseHook
-from weathon.base.trainer import BaseTrainer
-from weathon.hooks import LoadCheckpointHook, CheckpointHook, BestCkptSaverHook
-from weathon.hooks.checkpoint.checkpoint_processor import CheckpointProcessor
-from weathon.registry import HOOKS
-from weathon.utils.constants import DistributedParallelType
-from weathon.utils.constants import Hooks
-
-from weathon.utils.checkpoint import load_checkpoint, save_checkpoint
-from weathon.utils.device import create_device
-from weathon.utils.logger import get_logger
-from weathon.utils.megatron_utils import is_megatron_initialized
-from weathon.utils.torch_utils import get_local_rank
+from weathon.dl.base import BaseHook
+from weathon.dl.base.trainer import BaseTrainer
+from weathon.dl.hooks import LoadCheckpointHook, CheckpointHook, BestCkptSaverHook
+from weathon.dl.hooks.checkpoint.checkpoint_processor import CheckpointProcessor
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import DistributedParallelType
+from weathon.dl.utils.constants import Hooks
+
+from weathon.dl.utils.checkpoint import load_checkpoint, save_checkpoint
+from weathon.dl.utils.device import create_device
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.megatron_utils import is_megatron_initialized
+from weathon.dl.utils.torch_utils import get_local_rank
 
 
 class MpuProcessor(CheckpointProcessor):
     _BIN_FILE_DIR = 'model'
 
     def rank_name(self):
         # TODO
```

### Comparing `weathon-0.0.0.17/weathon/hooks/early_stop_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/early_stop_hook.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import numpy as np
 
-from weathon.base import BaseHook
-from weathon.registry import HOOKS
-from weathon.utils.constants import Hooks,Priority
-from weathon.utils.logger import get_logger
+from weathon.dl.base import BaseHook
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Hooks,Priority
+from weathon.dl.utils.logger import get_logger
 
 
 class EarlyStopStrategy:
     by_epoch = 'by_epoch'
     by_step = 'by_step'
     no = 'no'
```

### Comparing `weathon-0.0.0.17/weathon/hooks/evaluation_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/evaluation_hook.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from collections import OrderedDict
 from typing import Optional
 
-from weathon.base import BaseHook
-from weathon.registry import HOOKS
-from weathon.utils.constants import Hooks
+from weathon.dl.base import BaseHook
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Hooks
 
 
 class EvaluationStrategy:
     by_epoch = 'by_epoch'
     by_step = 'by_step'
     no = 'no'
```

### Comparing `weathon-0.0.0.17/weathon/hooks/iter_timer_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/iter_timer_hook.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import time
 
-from weathon.base import BaseHook
-from weathon.registry import HOOKS
-from weathon.utils.constants import Priority, LogKeys
-from weathon.utils.constants import Hooks
+from weathon.dl.base import BaseHook
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Priority, LogKeys
+from weathon.dl.utils.constants import Hooks
 
 
 
 @HOOKS.register_module(module_name=Hooks.IterTimerHook)
 class IterTimerHook(BaseHook):
     PRIORITY = Priority.LOW
```

### Comparing `weathon-0.0.0.17/weathon/hooks/logger/__init__.py` & `weathon-0.0.0.18/weathon/dl/hooks/logger/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .base import LoggerHook
     from .tensorboard_hook import TensorboardHook
     from .text_logger_hook import TextLoggerHook
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/hooks/logger/base.py` & `weathon-0.0.0.18/weathon/dl/hooks/logger/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,16 +1,15 @@
-# Copyright (c) OpenMMLab. All rights reserved.
 import numbers
 from abc import ABCMeta, abstractmethod
 
 import numpy as np
 import torch
 
-from weathon.base import BaseHook
-from weathon.utils.constants import Priority, ModeKeys
+from weathon.dl.base import BaseHook
+from weathon.dl.utils.constants import Priority, ModeKeys
 
 
 class LoggerHook(BaseHook):
     """Base class for logger hooks.
 
     Args:
         interval (int): Logging interval (every k iterations). It is interval of iterations even by_epoch is true.
```

### Comparing `weathon-0.0.0.17/weathon/hooks/logger/tensorboard_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/logger/tensorboard_hook.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import os
 
 import numpy as np
 import torch
 
-from weathon.registry import HOOKS
-from weathon.utils.constants import Hooks,LogKeys
-from weathon.utils.torch_utils import master_only
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Hooks,LogKeys
+from weathon.dl.utils.torch_utils import master_only
 from .base import LoggerHook
 
 
 @HOOKS.register_module(module_name=Hooks.TensorboardHook)
 class TensorboardHook(LoggerHook):
     """
     TensorBoard hook for visualization.
```

### Comparing `weathon-0.0.0.17/weathon/hooks/logger/text_logger_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/logger/text_logger_hook.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,18 +3,18 @@
 import os.path as osp
 from collections import OrderedDict
 
 import json
 import torch
 from torch import distributed as dist
 
-from weathon.utils.constants import Hooks, LogKeys, ModeKeys
-from weathon.utils.fileio.format.json_utils import EnhancedEncoder
-from weathon.utils.torch_utils import is_master
-from weathon.registry import HOOKS
+from weathon.dl.utils.constants import Hooks, LogKeys, ModeKeys
+from weathon.dl.utils.fileio.format.json_utils import EnhancedEncoder
+from weathon.dl.utils.torch_utils import is_master
+from weathon.dl.registry import HOOKS
 from .base import LoggerHook
 
 
 @HOOKS.register_module(module_name=Hooks.TextLoggerHook)
 class TextLoggerHook(LoggerHook):
     """Logger hook in text, Output log to both console and local json file.
```

### Comparing `weathon-0.0.0.17/weathon/hooks/lr_scheduler_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/lr_scheduler_hook.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,12 @@
-from weathon.base import BaseHook
-from weathon.registry import HOOKS, build_lr_scheduler
-from weathon.utils.constants import Priority, LogKeys, Hooks
-from weathon.utils.logger import get_logger
-from weathon.utils.torch_utils import is_master
+from weathon.dl.base import BaseHook
+from weathon.dl.registry import HOOKS, build_lr_scheduler
+from weathon.dl.utils.constants import Priority, LogKeys, Hooks
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.torch_utils import is_master
 
 
 
 class LrSchedulerProcessor:
 
     def __init__(self):
         self.lr_strategy = None
```

### Comparing `weathon-0.0.0.17/weathon/hooks/optimizer/__init__.py` & `weathon-0.0.0.18/weathon/dl/hooks/optimizer/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .apex_optimizer_hook import ApexAMPOptimizerHook
     from .base import OptimizerHook, NoneOptimizerHook
     from .torch_optimizer_hook import TorchAMPOptimizerHook
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/hooks/optimizer/apex_optimizer_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/optimizer/apex_optimizer_hook.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 import logging
 
 import torch
 from packaging import version
 
-from weathon.utils.constants import Hooks
+from weathon.dl.utils.constants import Hooks
 from .base import OptimizerHook, OptimizerProcessor
-from ...base import BaseHook
-from ...registry import HOOKS
+from weathon.dl.base import BaseHook
+from weathon.dl.registry import HOOKS
 
 
 class ApexOptimizerProcessor(OptimizerProcessor):
 
     def __init__(self, opt_level):
         self.opt_level = opt_level
```

### Comparing `weathon-0.0.0.17/weathon/hooks/optimizer/base.py` & `weathon-0.0.0.18/weathon/dl/hooks/optimizer/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from torch.nn.utils import clip_grad
 
-from weathon.base import BaseHook
-from weathon.registry import HOOKS
-from weathon.utils.constants import Priority, Hooks
-from weathon.utils.constants.output_constant import OutputKeys
+from weathon.dl.base import BaseHook
+from weathon.dl.registry import HOOKS
+from weathon.dl.utils.constants import Priority, Hooks
+from weathon.dl.utils.constants.output_constant import OutputKeys
 
 
 class OptimizerProcessor:
 
     def initialize_optimizer(self, trainer):
         """Initialize the optimizer.
```

### Comparing `weathon-0.0.0.17/weathon/hooks/optimizer/torch_optimizer_hook.py` & `weathon-0.0.0.18/weathon/dl/hooks/optimizer/torch_optimizer_hook.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import logging
 
-from weathon.utils.constants import Hooks
+from weathon.dl.utils.constants import Hooks
 from .base import OptimizerHook, OptimizerProcessor
-from ...base import BaseHook
-from ...registry import HOOKS
+from weathon.dl.base import BaseHook
+from weathon.dl.registry import HOOKS
 
 
 class TorchAMPOptimizerProcessor(OptimizerProcessor):
 
     def __init__(self, scaler, scale_update_param):
         self.scaler = scaler
         self.scale_update_param = scale_update_param
```

### Comparing `weathon-0.0.0.17/weathon/loss/cv/ocr/combined_loss.py` & `weathon-0.0.0.18/weathon/dl/loss/cv/ocr/combined_loss.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/loss/cv/ocr/ctc_loss.py` & `weathon-0.0.0.18/weathon/dl/loss/cv/ocr/ctc_loss.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/loss/cv/ocr/db_loss.py` & `weathon-0.0.0.18/weathon/dl/loss/cv/ocr/db_loss.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from torch import nn
 
 import torch
 import torch.nn as nn
 
-from weathon.registry import LOSS
-from weathon.utils.constants import Tasks
+from weathon.dl.registry import LOSS
+from weathon.dl.utils.constants import Tasks
 
 
 class BalanceCrossEntropyLoss(nn.Module):
     '''
     Balanced cross entropy loss.
     Shape:
         - Input: :math:`(N, 1, H, W)`
```

### Comparing `weathon-0.0.0.17/weathon/loss/cv/ocr/distillation_loss.py` & `weathon-0.0.0.18/weathon/dl/loss/cv/ocr/distillation_loss.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/loss/cv/ocr/fce_loss.py` & `weathon-0.0.0.18/weathon/dl/loss/cv/ocr/fce_loss.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/loss/cv/ocr/pse_loss.py` & `weathon-0.0.0.18/weathon/dl/loss/cv/ocr/pse_loss.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/metrics/common_metrics/accuracy_metric.py` & `weathon-0.0.0.18/weathon/dl/metrics/common_metrics/accuracy_metric.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 from typing import Dict
 
 import numpy as np
 
-from weathon.base import BaseMetric
-from weathon.registry import METRICS
-from weathon.registry.registry import default_group
-from weathon.utils.chinese_utils import remove_space_between_chinese_chars
-from weathon.utils.constants import OutputKeys, Metrics, MetricKeys
-from weathon.utils.tensor_utils import torch_nested_numpify
+from weathon.dl.base import BaseMetric
+from weathon.dl.registry import METRICS
+from weathon.dl.registry.registry import default_group
+from weathon.dl.utils.chinese_utils import remove_space_between_chinese_chars
+from weathon.dl.utils.constants import OutputKeys, Metrics, MetricKeys
+from weathon.dl.utils.tensor_utils import torch_nested_numpify
 
 
 @METRICS.register_module(group_key=default_group, module_name=Metrics.accuracy)
 class AccuracyMetric(BaseMetric):
     """The metric computation class for classification classes.
 
     This metric class calculates accuracy for the whole input batches.
```

### Comparing `weathon-0.0.0.17/weathon/metrics/common_metrics/loss_metric.py` & `weathon-0.0.0.18/weathon/dl/metrics/common_metrics/loss_metric.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 from typing import Dict
 
 import numpy as np
 
-from weathon.base import BaseMetric
-from weathon.registry import METRICS
-from weathon.registry.registry import default_group
-from weathon.utils.constants import Metrics, OutputKeys
+from weathon.dl.base import BaseMetric
+from weathon.dl.registry import METRICS
+from weathon.dl.registry.registry import default_group
+from weathon.dl.utils.constants import Metrics, OutputKeys
 
-from weathon.utils.tensor_utils import (torch_nested_detach, torch_nested_numpify)
+from weathon.dl.utils.tensor_utils import (torch_nested_detach, torch_nested_numpify)
 
 
 @METRICS.register_module(group_key=default_group, module_name=Metrics.loss_metric)
 class LossMetric(BaseMetric):
     """The metric class to calculate average loss of batches.
 
     Args:
```

### Comparing `weathon-0.0.0.17/weathon/metrics/cv/ocr/detection_metric.py` & `weathon-0.0.0.18/weathon/dl/metrics/cv/ocr/detection_metric.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import numpy as np
 from typing import Dict
 from shapely.geometry import Polygon
 
-from weathon.base import BaseMetric
-from weathon.registry import METRICS
-from weathon.utils.constants import Tasks, Datasets
+from weathon.dl.base import BaseMetric
+from weathon.dl.registry import METRICS
+from weathon.dl.utils.constants import Tasks, Datasets
 
 
 class DetectionIoUEvaluator(object):
 
     def __init__(self, iou_constraint=0.5, area_precision_constraint=0.5):
         self.iou_constraint = iou_constraint
         self.area_precision_constraint = area_precision_constraint
```

### Comparing `weathon-0.0.0.17/weathon/metrics/nlp/sequence_classification_metric.py` & `weathon-0.0.0.18/weathon/dl/metrics/nlp/sequence_classification_metric.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 from typing import Dict
 import numpy as np
 from sklearn.metrics import accuracy_score, f1_score
 
-from weathon.base import BaseMetric
-from weathon.registry import METRICS
-from weathon.registry.registry import default_group
-from weathon.utils.constants import Tasks, Datasets
-from weathon.utils.constants import Metrics, MetricKeys
-from weathon.utils.constants.output_constant import OutputKeys
-from weathon.utils.tensor_utils import torch_nested_detach, torch_nested_numpify
+from weathon.dl.base import BaseMetric
+from weathon.dl.registry import METRICS
+from weathon.dl.registry.registry import default_group
+from weathon.dl.utils.constants import Tasks, Datasets
+from weathon.dl.utils.constants import Metrics, MetricKeys
+from weathon.dl.utils.constants.output_constant import OutputKeys
+from weathon.dl.utils.tensor_utils import torch_nested_detach, torch_nested_numpify
 
 
 @METRICS.register_module(group_key=default_group, module_name=Metrics.seq_cls_metric)
 @METRICS.register_module(group_key=Tasks.text_classification, module_name=Datasets.jd_sentiment_text_classification)
 class SequenceClassificationMetric(BaseMetric):
     """The metric computation class for sequence classification tasks.
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/backbone/ocr/det_conv_next.py` & `weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/det_conv_next.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 from functools import partial
 import logging
 import os
 
 import torch
 import torch.nn as nn
 import torch.nn.functional as F
-from weathon.models.cv.backbone.ocr.transformer import DropPath
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
+from weathon.dl.models.cv.backbone.ocr.transformer import DropPath
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
 
 
 class LayerNorm(nn.Module):
     r""" LayerNorm that supports two data formats: channels_last (default) or channels_first.
     The ordering of the dimensions in the inputs. channels_last corresponds to inputs with
     shape (batch_size, height, width, channels) while channels_first corresponds to inputs
     with shape (batch_size, channels, height, width).
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/backbone/ocr/det_ghost_net.py` & `weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/det_ghost_net.py`

 * *Files 0% similar despite different names*

```diff
@@ -10,16 +10,16 @@
 import torch
 import torch.nn as nn
 import torch.nn.functional as F
 import math
 import logging
 from collections import OrderedDict
 
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
 
 
 def _make_divisible(v, divisor, min_value=None):
     """
     This function is taken from the original tf repo.
     It ensures that all layers have a channel number that is divisible by 8
     It can be seen here:
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/backbone/ocr/det_mobilenet_v3.py` & `weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/det_mobilenet_v3.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,18 +3,18 @@
 from __future__ import print_function
 import logging
 import os
 import torch
 from torch import nn
 from collections import OrderedDict
 
-from weathon.models.cv.backbone.ocr.det_resnet_vd import ConvBNACT
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.cv.ocr.common_modules import SEBlock
+from weathon.dl.models.cv.backbone.ocr.det_resnet_vd import ConvBNACT
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.cv.ocr.common_modules import SEBlock
 
 
 class ResidualUnit(nn.Module):
     def __init__(self, num_in_filter, num_mid_filter, num_out_filter, stride, kernel_size, act=None, use_se=False):
         super().__init__()
         self.conv0 = ConvBNACT(in_channels=num_in_filter, out_channels=num_mid_filter, kernel_size=1, stride=1,
                                padding=0, act=act)
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/backbone/ocr/det_resnet_vd.py` & `weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/det_resnet_vd.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,17 +4,17 @@
 
 import logging
 import os
 
 import torch
 from torch import nn
 
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.cv.ocr.common_modules import ConvBNACT
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.cv.ocr.common_modules import ConvBNACT
 
 
 class ConvBNACTWithPool(nn.Module):
     def __init__(self, in_channels, out_channels, kernel_size, groups=1, act=None):
         super().__init__()
         # self.pool = nn.AvgPool2d(kernel_size=2, stride=2, padding=0, ceil_mode=True)
         self.pool = nn.AvgPool2d(kernel_size=2, stride=2, padding=0)
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/backbone/ocr/mobile_vit.py` & `weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/mobile_vit.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/cv/backbone/ocr/rec_mobilenet_v3.py` & `weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/rec_mobilenet_v3.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from __future__ import absolute_import
 from __future__ import division
 from __future__ import print_function
 
 from torch import nn
 
-from weathon.utils.cv.ocr.common_modules import ConvBNACT, SEBlock
+from weathon.dl.utils.cv.ocr.common_modules import ConvBNACT, SEBlock
 
 
 class ResidualUnit(nn.Module):
     def __init__(self, num_in_filter, num_mid_filter, num_out_filter, stride, kernel_size, act=None, use_se=False):
         super().__init__()
         self.expand_conv = ConvBNACT(in_channels=num_in_filter, out_channels=num_mid_filter, kernel_size=1, stride=1,
                                      padding=0, act=act)
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/backbone/ocr/rec_resnet_vd.py` & `weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/rec_resnet_vd.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from __future__ import absolute_import
 from __future__ import division
 from __future__ import print_function
 
 from torch import nn
 
-from weathon.utils.cv.ocr.common_modules import ConvBNACT
+from weathon.dl.utils.cv.ocr.common_modules import ConvBNACT
 
 
 class ConvBNACTWithPool(nn.Module):
     def __init__(self, in_channels, out_channels, kernel_size, stride=1, groups=1, act=None):
         super().__init__()
         self.pool = nn.AvgPool2d(kernel_size=stride, stride=stride, padding=0, ceil_mode=True)
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/backbone/ocr/transformer.py` & `weathon-0.0.0.18/weathon/dl/models/cv/backbone/ocr/transformer.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 import torch
 import torch.nn as nn
 import torch.nn.functional as F
 import torch.utils.checkpoint as checkpoint
 import numpy as np
 from collections import OrderedDict
 
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
 
 
 class Mlp(nn.Module):
     """ Multilayer perceptron."""
 
     def __init__(self, in_features, hidden_features=None, out_features=None, act_layer=nn.GELU, drop=0.):
         super().__init__()
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/heads/ocr/head.py` & `weathon-0.0.0.18/weathon/dl/models/cv/heads/ocr/head.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import torch
 from functools import partial
 from torch import nn
 import torch.nn.functional as F
 
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.cv.ocr.common_modules import ConvBNACT
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.cv.ocr.common_modules import ConvBNACT
 
 
 class Head(nn.Module):
     def __init__(self, in_channels):
         super().__init__()
         self.conv1 = nn.Conv2d(in_channels=in_channels, out_channels=in_channels // 4, kernel_size=3, padding=1,
                                bias=False)
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/necks/ocr/neck.py` & `weathon-0.0.0.18/weathon/dl/models/cv/necks/ocr/neck.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import torch.nn.init as init
 import torch
 from torch import nn
 import torch.nn.functional as F
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.cv.ocr.common_modules import ConvBNACT, SEBlock, ScaleFeatureSelection
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.cv.ocr.common_modules import ConvBNACT, SEBlock, ScaleFeatureSelection
 
 
 class Im2Seq(nn.Module):
     def __init__(self, in_channels, **kwargs):
         super().__init__()
         self.out_channels = in_channels
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/task_models/ocr/ocr_detection.py` & `weathon-0.0.0.18/weathon/dl/models/cv/task_models/ocr/ocr_detection.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,30 +2,28 @@
 import os
 
 import torch
 from torch import nn
 from addict import Dict
 from dataclasses import dataclass
 
-from weathon.base import TorchModel, BaseOuptut
-from weathon.registry import MODELS, build_model, build_loss, build_postprocessor
-from weathon.utils.constants import Tasks, Datasets
-from weathon.utils.typing import Tensor
+from weathon.dl.base import TorchModel, BaseOutput
+from weathon.dl.registry import MODELS, build_model, build_loss, build_postprocessor
+from weathon.dl.utils.constants import Tasks, Datasets
+from weathon.dl.utils.typing import Tensor
 
 
 @dataclass
 class DBModelOutput(BaseOutput):
-    logit:Tensor = None
+    logit: Tensor = None
     loss: Tensor = None
     loss_threshold_maps: Tensor = None
     loss_shrink_maps: Tensor = None
 
 
-
-
 @MODELS.register_module(Tasks.ocr_detection, module_name=Datasets.icdar2015_ocr_detection)
 class DetModel(TorchModel):
 
     def __init__(self, model_dir: str, **kwargs):
         """initialize the ocr recognition model from the `model_dir` path.
 
         Args:
@@ -47,15 +45,15 @@
         x = self.backbone(x)
         x = self.neck(x)
         x = self.head(x)
         output = dict(logit=x, loss=None)
         if self.training:
             loss_dict = self.criterion(x, inputs)
             output.update(**loss_dict)
-        
+
         return DBModelOutput(**output)
 
     def pose_process(self, **inputs) -> dict:
         if not self.training:
             boxes, scores = self.postprocess(self.forward(inputs).logit, inputs["shape"])
             inputs.update(dict(boxes=boxes, scores=scores))
         return inputs
```

### Comparing `weathon-0.0.0.17/weathon/models/cv/task_models/ocr/ocr_recognition.py` & `weathon-0.0.0.18/weathon/dl/models/cv/task_models/ocr/ocr_recognition.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-from weathon.base import TorchModel
-from weathon.registry import MODELS, build_model, build_loss
-from weathon.utils.constants import Tasks, Datasets
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS, build_model, build_loss
+from weathon.dl.utils.constants import Tasks, Datasets
 
 
 @MODELS.register_module(Tasks.ocr_recognition, module_name=Datasets.icdar2015_ocr_detection)
 class RecModel(TorchModel):
     def __init__(self, model_dir: str, **kwargs):
         super().__init__(model_dir, **kwargs)
         self.backbone = build_model(kwargs.get("backbone"), task_name=kwargs.get("task"))
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,53 +1,46 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .backbone.bart import BartForTextErrorCorrection
     from .backbone.bloom import BloomModel
     from .backbone.glm_130b import GLM130bForTextGeneration
     from .backbone.canmt import CanmtForTranslation
     from .backbone.deberta_v2 import DebertaV2ForMaskedLM, DebertaV2Model
     from .backbone.gpt_neo import GPTNeoModel
-    from weathon.models.nlp.backbone.gpt2 import GPT2Model
+    from weathon.dl.models.nlp.backbone.gpt2 import GPT2Model
     from .backbone.gpt3 import GPT3ForTextGeneration, DistributedGPT3
     from .backbone.gpt_moe import GPTMoEForTextGeneration, DistributedGPTMoE
     from .heads import TextClassificationHead
     from .backbone.hf_transformers import TransformersModel
     from .backbone.lstm import (
         LSTMModel,
         LSTMForTokenClassificationWithCRF,
     )
     from .backbone.mglm import MGLMForTextSummarization
-    from weathon.models.nlp.backbone.palm_v2 import PalmForTextGeneration
+    from weathon.dl.models.nlp.backbone.palm_v2 import PalmForTextGeneration
     from .backbone.plug_mental import (PlugMentalConfig, PlugMentalModel,
                                        PlugMentalForSequenceClassification)
     from .backbone.ponet import PoNetForMaskedLM, PoNetModel, PoNetConfig
     from .backbone.space_T_cn import TableQuestionAnswering
     from .backbone.space_T_en import StarForTextToSql
-    from weathon.models.nlp.backbone.structbert import (
-        SbertForFaqQuestionAnswering,
-        SbertForMaskedLM,
-        SbertForSequenceClassification,
-        SbertForTokenClassification,
-        SbertModel,
-    )
     from .backbone.T5 import T5ForConditionalGeneration
     from .task_models import (
         ModelForFeatureExtraction,
         ModelForInformationExtraction,
         ModelForTextClassification,
         SingleBackboneTaskModelBase,
         ModelForTextGeneration,
         ModelForTextRanking,
         ModelForTokenClassification,
         ModelForTokenClassificationWithCRF,
     )
-    from weathon.models.nlp.backbone.unite import UniTEForTranslationEvaluation
+    from weathon.dl.models.nlp.backbone.unite import UniTEForTranslationEvaluation
     from .backbone.use import UserSatisfactionEstimation
     from .backbone.llama import LlamaForTextGeneration, LlamaConfig, LlamaModel, LlamaTokenizer, LlamaTokenizerFast
 
 else:
     _import_structure = {
         'bart': ['BartForTextErrorCorrection'],
         'bert': [
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/T5/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/T5/__init__.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .backbone import T5Model
     from .text2text_generation import T5ForConditionalGeneration
 
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/T5/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/T5/backbone.py`

 * *Files 0% similar despite different names*

```diff
@@ -28,20 +28,20 @@
 from transformers.modeling_utils import (PreTrainedModel,
                                          find_pruneable_heads_and_indices,
                                          prune_linear_layer)
 from transformers.utils import (DUMMY_INPUTS, DUMMY_MASK, is_torch_fx_proxy)
 from transformers.utils.model_parallel_utils import (assert_device_map,
                                                      get_device_map)
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import BaseModel, TorchModel
-from weathon.registry import MODELS
-from weathon.utils.output.nlp_outputs import AttentionBackboneModelOutput, Seq2SeqModelOutput
-from weathon.utils.constants import Tasks
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import BaseModel, TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.output.nlp_outputs import AttentionBackboneModelOutput, Seq2SeqModelOutput
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.logger import get_logger
 from .configuration import T5Config
 
 logger = get_logger()
 
 
 ###################################################
 # This is a conversion method from TF 1.0 to PyTorch
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/T5/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/T5/configuration.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 # limitations under the License.
 """ T5 model configuration"""
 from typing import Mapping
 
 from transformers.configuration_utils import PretrainedConfig
 from transformers.onnx import OnnxSeq2SeqConfigWithPast
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 class T5Config(PretrainedConfig):
     r"""
     This is the configuration class to store the configuration of a [`T5Model`] or a [`TFT5Model`]. It is used to
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/T5/text2text_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/T5/text2text_generation.py`

 * *Files 0% similar despite different names*

```diff
@@ -17,19 +17,19 @@
 
 import torch
 from torch import nn
 from torch.nn import CrossEntropyLoss
 from transformers.utils.model_parallel_utils import (assert_device_map,
                                                      get_device_map)
 
-from weathon.utils.constants.metainfo import Models
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.logger import get_logger
-from weathon.utils.output.nlp_outputs import Seq2SeqLMOutput, AttentionBackboneModelOutput, TokenGeneratorOutput
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.output.nlp_outputs import Seq2SeqLMOutput, AttentionBackboneModelOutput, TokenGeneratorOutput
 from .backbone import T5PreTrainedModel, T5Stack, __HEAD_MASK_WARNING_MSG
 from .configuration import T5Config
 
 logger = get_logger()
 
 # Warning message for FutureWarning: head_mask was separated into two input args - head_mask, decoder_head_mask
 __HEAD_MASK_WARNING_MSG = """
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bart/text_error_correction.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bart/text_error_correction.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import os.path as osp
 from typing import Any, Dict
 
 import torch.cuda
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks, ModelFile, Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks, ModelFile, Models
 
 
 __all__ = ['BartForTextErrorCorrection']
 
 
 
 @MODELS.register_module(Tasks.text_error_correction, module_name=Models.bart)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .backbone import (
         BertLayer,
         BertModel,
         BertPreTrainedModel,
     )
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/backbone.py`

 * *Files 1% similar despite different names*

```diff
@@ -22,21 +22,21 @@
 from torch import nn
 from transformers.activations import ACT2FN
 from transformers.modeling_utils import (PreTrainedModel,
                                          apply_chunking_to_forward,
                                          find_pruneable_heads_and_indices,
                                          prune_linear_layer)
 
-from weathon.base import TorchModel, BaseModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.logger import get_logger
-from weathon.utils.nlp.utils import parse_labels_in_order
-from weathon.utils.output.nlp_outputs import AttentionBackboneModelOutput
+from weathon.dl.base import TorchModel, BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.nlp.utils import parse_labels_in_order
+from weathon.dl.utils.output.nlp_outputs import AttentionBackboneModelOutput
 from .configuration import BertConfig
 
 logger = get_logger()
 
 _CONFIG_FOR_DOC = 'BertConfig'
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/configuration.py`

 * *Files 0% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 """ BERT model configuration """
 from collections import OrderedDict
 from typing import Mapping
 
 from transformers.configuration_utils import PretrainedConfig
 from transformers.onnx import OnnxConfig
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 class BertConfig(PretrainedConfig):
     r"""
     This is the configuration class to store the configuration of a
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/document_segmentation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/document_segmentation.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 from typing import Any, Dict
 
 import torch
 from torch import nn
 from torch.nn import CrossEntropyLoss
 
-from weathon.base import BaseModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.models.nlp.ponet import PoNetConfig
-from weathon.utils.output.nlp_outputs import AttentionTokenClassificationModelOutput
+from weathon.dl.base import BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.models.nlp.ponet import PoNetConfig
+from weathon.dl.utils.output.nlp_outputs import AttentionTokenClassificationModelOutput
 from .backbone import BertModel, BertPreTrainedModel
 from .configuration import BertConfig
 
 __all__ = ['BertForDocumentSegmentation']
 
 
 @MODELS.register_module(Tasks.document_segmentation, module_name=Models.bert_for_ds)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/sentence_embedding.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/sentence_embedding.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import torch
 from torch import nn
 
-from weathon.base import BaseModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.output.nlp_outputs import SentencEmbeddingModelOutput
+from weathon.dl.base import BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.output.nlp_outputs import SentencEmbeddingModelOutput
 from .backbone import BertModel, BertPreTrainedModel
 
 
 class Pooler(nn.Module):
     """
     Parameter-free poolers to get the sentence embedding
     'cls': [CLS] representation with BERT/RoBERTa's MLP pooler.
@@ -72,15 +72,15 @@
                 for details.
             docs (:obj: `dict`): Dict of pretrained models's input for the query sequence. See
                 :meth:`transformers.PreTrainedTokenizer.encode` and :meth:`transformers.PreTrainedTokenizer.__call__`
                 for details.
         Returns:
             Returns `modelscope.outputs.SentencEmbeddingModelOutput
         Examples:
-            >>> from weathon.base import BaseModel, BasePreprocessor
+            >>> from weathon.dl.base import BaseModel, BasePreprocessor
             >>> model = BaseModel.from_pretrained('damo/nlp_corom_sentence-embedding_chinese-base')
             >>> preprocessor = BasePreprocessor.from_pretrained('damo/nlp_corom_sentence-embedding_chinese-base')
             >>> print(model(**preprocessor('source_sentence':['This is a test'])))
         """
         query_embeddings, doc_embeddings = None, None
         if query is not None:
             query_embeddings = self.encode(**query)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/siamese_uie.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/siamese_uie.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from copy import deepcopy
 
 import torch
 from torch import nn
 
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
 from .backbone import BertEncoder, BertModel, BertPreTrainedModel
 
 __all__ = ['SiameseUieModel']
 
 
 @MODELS.register_module(Tasks.siamese_uie, module_name=Models.bert)
 class SiameseUieModel(BertPreTrainedModel):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/text_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/text_classification.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,12 +1,12 @@
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.models.nlp import ModelForTextClassification
-from weathon.utils import logger as logging
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.models.nlp import ModelForTextClassification
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 @MODELS.register_module(Tasks.text_classification, module_name=Models.bert)
 @MODELS.register_module(Tasks.nli, module_name=Models.bert)
 @MODELS.register_module(Tasks.sentiment_classification, module_name=Models.bert)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/text_ranking.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/text_ranking.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,12 +1,12 @@
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.models.nlp import ModelForTextRanking
-from weathon.utils import logger as logging
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.models.nlp import ModelForTextRanking
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 @MODELS.register_module(Tasks.text_ranking, module_name=Models.bert)
 class BertForTextRanking(ModelForTextRanking):
     r"""Bert Model transformer with a sequence classification/regression head on top
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/token_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/token_classification.py`

 * *Files 2% similar despite different names*

```diff
@@ -9,20 +9,20 @@
 #     http://www.apache.org/licenses/LICENSE-2.0
 #
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Heads, Models
-from weathon.models.nlp.task_models.token_classification import (
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Heads, Models
+from weathon.dl.models.nlp.task_models.token_classification import (
     ModelForTokenClassification, ModelForTokenClassificationWithCRF)
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 @MODELS.register_module(Tasks.token_classification, module_name=Models.bert)
 @MODELS.register_module(Tasks.part_of_speech, module_name=Models.bert)
 @MODELS.register_module(Tasks.word_segmentation, module_name=Models.bert)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/bert/word_alignment.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/bert/word_alignment.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,19 +14,19 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 import torch
 import torch.nn as nn
 import torch.utils.checkpoint
 
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils import logger as logging
-from weathon.utils.output.nlp_outputs import WordAlignmentOutput
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.output.nlp_outputs import WordAlignmentOutput
 from .backbone import BertModel, BertPreTrainedModel
 
 logger = logging.get_logger()
 
 
 @MODELS.register_module(Tasks.word_alignment, module_name=Models.bert)
 class MBertForWordAlignment(BertPreTrainedModel):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/canmt/canmt_model.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/canmt/canmt_model.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/canmt/canmt_translation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/canmt/canmt_translation.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 import os.path as osp
 from typing import Dict
 
 import torch
 from torch import Tensor
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks, ModelFile
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.config.config import Config
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks, ModelFile
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.config.config import Config
 
 __all__ = ['CanmtForTranslation']
 
 
 @MODELS.register_module(Tasks.competency_aware_translation, module_name=Models.canmt)
 class CanmtForTranslation(TorchModel):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/canmt/sequence_generator.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/canmt/sequence_generator.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # Modified by Zhipu.AI
 # Original Copyright (c) Alibaba, Inc. and its affiliates.
 from typing import TYPE_CHECKING, Union
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .codegeex_for_code_translation import CodeGeeXForCodeTranslation
     from .codegeex_for_code_generation import CodeGeeXForCodeGeneration
 else:
     _import_structure = {
         'codegeex_for_code_translation': ['CodeGeeXForCodeTranslation'],
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/codegeex.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/codegeex.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/codegeex_for_code_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/codegeex_for_code_generation.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 # Copyright (c) 2022 Zhipu.AI
 import copy
 from typing import Dict
 
 import torch
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.constants.output_constant import OutputKeys
-from weathon.utils.logger import get_logger
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.constants.output_constant import OutputKeys
+from weathon.dl.utils.logger import get_logger
 from .codegeex import CodeGeeXModel
 from .inference import get_token_stream
 from .tokenizer import CodeGeeXTokenizer
 
 
 def model_provider():
     """Build the model."""
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/codegeex_for_code_translation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/codegeex_for_code_translation.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 # Copyright (c) 2022 Zhipu.AI
 import copy
 from typing import Dict
 
 import torch
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.logger import get_logger
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.logger import get_logger
 from .codegeex import CodeGeeXModel
 from .inference import get_token_stream
 from .tokenizer import CodeGeeXTokenizer
 
 
 def model_provider():
     """Build the model."""
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/inference.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/inference.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/codegeex/tokenizer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/codegeex/tokenizer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/csanmt/translation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/csanmt/translation.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,22 +4,22 @@
 import math
 import sys
 from collections import namedtuple
 from typing import Dict
 
 import tensorflow as tf
 
-from weathon.base import BaseModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
+from weathon.dl.base import BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
 
 __all__ = ['CsanmtForTranslation']
 
-from weathon.utils.typing import Tensor
+from weathon.dl.utils.typing import Tensor
 
 
 @MODELS.register_module(Tasks.translation, module_name=Models.translation)
 class CsanmtForTranslation(BaseModel):
 
     def __init__(self, model_dir, *args, **kwargs):
         """
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import DebertaV2Config
     from .tokenization import DebertaV2Tokenizer
     from .tokenization_fast import DebertaV2TokenizerFast
     from .backbone import (
         DebertaV2Model,
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/backbone.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,20 +21,20 @@
 import torch.utils.checkpoint
 from torch import nn
 from torch.nn import LayerNorm
 from transformers.activations import ACT2FN
 from transformers.modeling_utils import PreTrainedModel
 from transformers.pytorch_utils import softmax_backward_data
 
-from weathon.base import TorchModel, BaseModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils import logger as logging
-from weathon.utils.output.nlp_outputs import AttentionBackboneModelOutput
+from weathon.dl.base import TorchModel, BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.output.nlp_outputs import AttentionBackboneModelOutput
 from .configuration import DebertaV2Config
 
 logger = logging.get_logger()
 
 
 # Copied from transformers.models.deberta.modeling_deberta.ContextPooler
 class ContextPooler(nn.Module):
@@ -1134,15 +1134,15 @@
             return_dict (`bool`, *optional*):
                 Whether or not to return a dataclass instead of a plain tuple.
 
         Returns:
             Returns `modelscope.outputs.AttentionBackboneModelOutput`
 
         Examples:
-            >>> from weathon.base import BaseModel,BasePreprocessor
+            >>> from weathon.dl.base import BaseModel,BasePreprocessor
             >>> model = BaseModel.from_pretrained('damo/nlp_debertav2_fill-mask_chinese-lite', task='backbone')
             >>> preprocessor = BasePreprocessor.from_pretrained('damo/nlp_debertav2_fill-mask_chinese-lite')
             >>> print(model(**preprocessor('这是个测试')))
         """
 
         output_attentions = output_attentions if output_attentions is not None else self.config.output_attentions
         output_hidden_states = (
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/configuration.py`

 * *Files 0% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """ DeBERTa-v2 model configuration, mainly copied from :class:`~transformers.DeBERTaV2Config"""
 
 from transformers import PretrainedConfig
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 class DebertaV2Config(PretrainedConfig):
     r"""
     This is the configuration class to store the configuration of a [`DebertaV2Model`]. It is used to instantiate a
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/fill_mask.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/fill_mask.py`

 * *Files 0% similar despite different names*

```diff
@@ -17,18 +17,18 @@
 
 import torch
 import torch.utils.checkpoint
 from torch import nn
 from torch.nn import CrossEntropyLoss
 from transformers.activations import ACT2FN
 
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.output.nlp_outputs import AttentionFillMaskModelOutput
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.output.nlp_outputs import AttentionFillMaskModelOutput
 from .backbone import DebertaV2Model, DebertaV2PreTrainedModel
 
 
 # Copied from transformers.models.deberta.modeling_deberta.DebertaForMaskedLM with Deberta->DebertaV2
 @MODELS.register_module(Tasks.fill_mask, module_name=Models.deberta_v2)
 class DebertaV2ForMaskedLM(DebertaV2PreTrainedModel):
     r"""DeBERTa_v2 Model with a `language modeling` head on top.
@@ -123,21 +123,21 @@
                 config.vocab_size]` (see `input_ids` docstring) Tokens with indices set to `-100` are
                 ignored (masked), the loss is only computed for the tokens with labels in `[0, ..., config.vocab_size]`
 
         Returns:
             Returns `modelscope.outputs.AttentionFillMaskModelOutput`
 
         Examples:
-            >>> from weathon.base import BaseModel,BasePreprocessor
+            >>> from weathon.dl.base import BaseModel,BasePreprocessor
             >>> model = BaseModel.from_pretrained('damo/nlp_debertav2_fill-mask_chinese-lite')
             >>> preprocessor = BasePreprocessor.from_pretrained('damo/nlp_debertav2_fill-mask_chinese-lite')
             >>> # Call the model, return some tensors
             >>> print(model(**preprocessor('你师父差得动你，你师父可[MASK]不动我。')))
             >>> # Call the pipeline
-            >>> from weathon.base import pipeline
+            >>> from weathon.dl.base import pipeline
             >>> pipeline_ins = pipeline('fill-mask', model=model, preprocessor=preprocessor)
             >>> print(pipeline_ins('你师父差得动你，你师父可[MASK]不动我。'))
         """
 
         return_dict = return_dict if return_dict is not None else self.config.use_return_dict
 
         outputs = self.deberta(
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/tokenization.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/tokenization.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/deberta_v2/tokenization_fast.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/deberta_v2/tokenization_fast.py`

 * *Files 0% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 import os
 from shutil import copyfile
 from typing import Optional, Tuple
 
 from transformers.file_utils import is_sentencepiece_available
 from transformers.tokenization_utils_fast import PreTrainedTokenizerFast
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 if is_sentencepiece_available():
     from .tokenization import DebertaV2Tokenizer
 else:
     DebertaV2Tokenizer = None
 
 logger = logging.get_logger()
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/__init__.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .document_grounded_dialog_generate import DocumentGroundedDialogGenerateModel
     from .document_grounded_dialog_rerank import DocumentGroundedDialogRerankModel
     from .document_grounded_dialog_retrieval import DocumentGroundedDialogRetrievalModel
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/backbone.py`

 * *Files 0% similar despite different names*

```diff
@@ -22,15 +22,15 @@
 from torch import nn
 from torch.utils.checkpoint import checkpoint
 from transformers import (AutoConfig, DPRConfig, DPRQuestionEncoder,
                           MT5ForConditionalGeneration, RagTokenForGeneration,
                           XLMRobertaForSequenceClassification, XLMRobertaModel,
                           XLMRobertaTokenizer)
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 class Wrapper(nn.Module):
 
     def __init__(self, encoder):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/document_grounded_dialog_generate.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/document_grounded_dialog_generate.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 import os
 from typing import Dict
 
 import torch
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Tasks, ModelFile
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.typing import Tensor
-# from weathon.utils.typing import Tensor, TorchModel
-# from weathon.registry import MODELS
-# from weathon.utils.config.config import Config
-# from weathon.utils.constants import ModelFile, Tasks
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Tasks, ModelFile
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.typing import Tensor
+# from weathon.dl.utils.typing import Tensor, TorchModel
+# from weathon.dl.registry import MODELS
+# from weathon.dl.utils.config.config import Config
+# from weathon.dl.utils.constants import ModelFile, Tasks
 from .backbone import Re2GModel
 
 
 @MODELS.register_module(Tasks.document_grounded_dialog_generate, module_name=Models.doc2bot)
 class DocumentGroundedDialogGenerateModel(TorchModel):
     _backbone_prefix = ''
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/document_grounded_dialog_rerank.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/document_grounded_dialog_rerank.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 import os
 from typing import Dict
 
 import torch
 from torch import nn
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.typing import Tensor
-# from weathon.base import BaseModel, Tensor, TorchModel
-# from weathon.registry import MODELS
-# from weathon.utils.config.config import Config
-# from weathon.utils.constants import ModelFile, Tasks
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.typing import Tensor
+# from weathon.dl.base import BaseModel, Tensor, TorchModel
+# from weathon.dl.registry import MODELS
+# from weathon.dl.utils.config.config import Config
+# from weathon.dl.utils.constants import ModelFile, Tasks
 from .backbone import ClassifyRerank
 
 
 @MODELS.register_module(Tasks.document_grounded_dialog_rerank, module_name=Models.doc2bot)
 class DocumentGroundedDialogRerankModel(TorchModel):
     _backbone_prefix = ''
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/dgds/document_grounded_dialog_retrieval.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/dgds/document_grounded_dialog_retrieval.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 import os
 from typing import Dict
 
 import torch
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Tasks, ModelFile
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.typing import Tensor
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Tasks, ModelFile
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.typing import Tensor
 from .backbone import DPRModel
 
 
 @MODELS.register_module(Tasks.document_grounded_dialog_retrieval, module_name=Models.doc2bot)
 class DocumentGroundedDialogRetrievalModel(TorchModel):
     _backbone_prefix = ''
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/fid_T5/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_T5/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .text_generation import (T5Chat, FIDT5Chat)
 else:
     _import_structure = {
         'text_generation': ['T5Chat', 'FIDT5Chat'],
     }
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/fid_T5/text_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_T5/text_generation.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 import io
 import os
 
 import torch
 from transformers import AutoConfig
 
-from weathon.base import TorchModel
-from weathon.models.nlp import T5ForConditionalGeneration
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.output.nlp_outputs import TokenGeneratorOutput, TextGenerationModelOutput
-
-# from weathon.models.base import TorchModel
-# from weathon.registry import MODELS
-# from weathon.models.nlp.T5 import T5ForConditionalGeneration
+from weathon.dl.base import TorchModel
+from weathon.dl.models.nlp import T5ForConditionalGeneration
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.output.nlp_outputs import TokenGeneratorOutput, TextGenerationModelOutput
+
+# from weathon.dl.models.base import TorchModel
+# from weathon.dl.registry import MODELS
+# from weathon.dl.models.nlp.T5 import T5ForConditionalGeneration
 # from weathon.outputs import TextGenerationModelOutput, TokenGeneratorOutput
-# from weathon.utils.constants import Tasks
+# from weathon.dl.utils.constants import Tasks
 
 WEIGHTS_NAME = 'pytorch_model.bin'
 
 
 class T5Chat(TorchModel):
 
     def __init__(self, model_dir, *args, **kwargs):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/fid_plug/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_plug/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import PlugConfig
     from .text_generation import (PlugV2Chat, PlugV2FidChat)
 else:
     _import_structure = {
         'configuration': ['PlugConfig'],
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/fid_plug/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_plug/backbone.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/fid_plug/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_plug/configuration.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/fid_plug/text_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/fid_plug/text_generation.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 import io
 import os
 
 import torch
 from transformers.modeling_outputs import Seq2SeqLMOutput
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.output.nlp_outputs import TextGenerationModelOutput, TokenGeneratorOutput
-# from weathon.models.base import TorchModel
-# from weathon.registry import MODELS
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.output.nlp_outputs import TextGenerationModelOutput, TokenGeneratorOutput
+# from weathon.dl.models.base import TorchModel
+# from weathon.dl.registry import MODELS
 # from weathon.outputs import TextGenerationModelOutput, TokenGeneratorOutput
-# from weathon.utils.constants import Tasks
+# from weathon.dl.utils.constants import Tasks
 from .backbone import PlugForConditionalGeneration
 from .configuration import PlugConfig
 
 CONFIG_NAME = 'config.json'
 WEIGHTS_NAME = 'pytorch_model.bin'
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # Modified by Zhipu.AI
 # Original Copyright (c) Alibaba, Inc. and its affiliates.
 from typing import TYPE_CHECKING, Union
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .text_generation import GLM130bForTextGeneration
 else:
     _import_structure = {'text_generation': ['GLM130bForTextGeneration']}
 
     import sys
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/generation/strategies.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/generation/strategies.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/initialize.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/initialize.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/kernels/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/kernels/__init__.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/quantization/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/quantization/__init__.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/quantization/functional.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/quantization/functional.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/quantization/layers.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/quantization/layers.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/glm_130b/text_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/glm_130b/text_generation.py`

 * *Files 1% similar despite different names*

```diff
@@ -12,26 +12,26 @@
 import torch
 from SwissArmyTransformer import mpu
 from SwissArmyTransformer.generation.autoregressive_sampling import (
     get_masks_and_position_ids_default, update_mems)
 from SwissArmyTransformer.generation.utils import (generate_continually,
                                                    timed_name)
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Tasks, ModelFile
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.constants.output_constant import OutputKeys
-# from weathon.models.base import TorchModel
-# from weathon.registry import MODELS
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Tasks, ModelFile
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.constants.output_constant import OutputKeys
+# from weathon.dl.models.base import TorchModel
+# from weathon.dl.registry import MODELS
 # from weathon.outputs import OutputKeys
-# from weathon.utils.config.config import Config
-# from weathon.utils.constants import ModelFile, Tasks
-from weathon.utils.logger import get_logger
+# from weathon.dl.utils.config.config import Config
+# from weathon.dl.utils.constants import ModelFile, Tasks
+from weathon.dl.utils.logger import get_logger
 from .generation import BaseStrategy, BeamSearchStrategy
 from .initialize import initialize, initialize_model_and_tokenizer
 
 torch.set_num_threads(24)
 
 logger = get_logger()
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import GPT3Config
     from .backbone import GPT3Model
     from .text_generation import GPT3ForTextGeneration
     from .tokenizer import JiebaBPETokenizer
     from .distributed_gpt3 import DistributedGPT3
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/backbone.py`

 * *Files 0% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 
 import addict
 import torch
 from torch import nn
 from torch.nn import functional as F
 from transformers.modeling_utils import PreTrainedModel
 
-from weathon.utils.constants import ModelFile
+from weathon.dl.utils.constants import ModelFile
 from .configuration import GPT3Config
 from .distributed_gpt3 import sample
 
 
 class GPT3SelfAttention(nn.Module):
     """Parallel self-attention layer abstract class.
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/configuration.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/distributed_gpt3.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/distributed_gpt3.py`

 * *Files 1% similar despite different names*

```diff
@@ -24,18 +24,18 @@
 from megatron_util.model import (AttnMaskType, Float16Module, LayerNorm,
                                  bias_gelu_impl)
 from megatron_util.model.fused_softmax import FusedScaleMaskSoftmax
 from torch import nn
 from torch.nn import functional as F
 from transformers.modeling_utils import PreTrainedModel
 
-from weathon.base import TorchModel
-from weathon.models.nlp.backbone.gpt3 import GPT3Config
-from weathon.utils.megatron_utils import init_megatron_util
-from weathon.utils.nlp.load_checkpoint import pre_load
+from weathon.dl.base import TorchModel
+from weathon.dl.models.nlp.backbone.gpt3 import GPT3Config
+from weathon.dl.utils.megatron_utils import init_megatron_util
+from weathon.dl.utils.nlp.load_checkpoint import pre_load
 
 
 class GPT3ParallelMLP(nn.Module):
     """MLP.
 
     MLP will take the input with h hidden state, project it to 4*h
     hidden dimension, perform nonlinear transformation, and project the
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/text_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/text_generation.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 from collections import OrderedDict
 from typing import Dict
 
 import torch
 from transformers import BertTokenizer
 
-from weathon.base import TorchModel
-from weathon.models.nlp.backbone.gpt3 import GPT3Model
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks, Models
+from weathon.dl.base import TorchModel
+from weathon.dl.models.nlp.backbone.gpt3 import GPT3Model
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks, Models
 
 __all__ = ['GPT3ForTextGeneration']
 
-from weathon.utils.typing import Tensor
+from weathon.dl.utils.typing import Tensor
 
 
 @MODELS.register_module(Tasks.text_generation, module_name=Models.gpt3)
 class GPT3ForTextGeneration(TorchModel):
 
     def __init__(self, model_dir: str, *args, **kwargs):
         """initialize the text generation model from the `model_dir` path.
@@ -26,15 +26,15 @@
         super().__init__(model_dir, *args, **kwargs)
 
         # Temporarily compatible with DistributedGPT3 and GPT3Model,
         # the base/large model based on GPT3Model will be replaced in the future,
         # and GPT3Model will be deprecated
 
         # if 'megatron' in read_config(model_dir):
-        #     from weathon.models.nlp import DistributedGPT3
+        #     from weathon.dl.models.nlp import DistributedGPT3
         #     self.model = DistributedGPT3(model_dir, **kwargs)
         # else:
         #     self.model = GPT3Model.from_pretrained(model_dir)
         #     self.tokenizer = BertTokenizer.from_pretrained(model_dir)
 
         self.model = GPT3Model.from_pretrained(model_dir)
         self.tokenizer = BertTokenizer.from_pretrained(model_dir)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt3/tokenizer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt3/tokenizer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/__init__.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import GPTMoEConfig
     from .backbone import GPTMoEModel
     from .text_generation import GPTMoEForTextGeneration
     from .tokenizer import JiebaBPETokenizer
     from .distributed_gpt_moe import DistributedGPTMoE
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/backbone.py`

 * *Files 0% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 
 import addict
 import torch
 from torch import nn
 from torch.nn import functional as F
 from transformers.modeling_utils import PreTrainedModel
 
-from weathon.utils.constants import ModelFile
+from weathon.dl.utils.constants import ModelFile
 from .configuration import GPTMoEConfig
 
 
 class GPTMoESelfAttention(nn.Module):
     """Parallel self-attention layer abstract class.
 
     Self-attention layer takes input with size [s, b, h]
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/checkpointing.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/checkpointing.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/configuration.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/distributed_gpt_moe.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/distributed_gpt_moe.py`

 * *Files 0% similar despite different names*

```diff
@@ -21,18 +21,18 @@
 from megatron_util.model import (AttnMaskType, Float16Module, LayerNorm,
                                  bias_gelu_impl)
 from megatron_util.model.fused_softmax import FusedScaleMaskSoftmax
 from torch import nn
 from torch.nn import functional as F
 from transformers.modeling_utils import PreTrainedModel
 
-from weathon.base import TorchModel
-from weathon.models.nlp.gpt_moe import GPTMoEConfig
-from weathon.utils.megatron_utils import init_megatron_util
-from weathon.utils.output.nlp_outputs import TextGenerationModelOutput, TokenGeneratorOutput
+from weathon.dl.base import TorchModel
+from weathon.dl.models.nlp.gpt_moe import GPTMoEConfig
+from weathon.dl.utils.megatron_utils import init_megatron_util
+from weathon.dl.utils.output.nlp_outputs import TextGenerationModelOutput, TokenGeneratorOutput
 from .checkpointing import load_checkpoint
 from .moe.layer import MoE
 
 
 class GPTMoEParallelMLP(nn.Module):
 
     def __init__(self,
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/experts.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/experts.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/layer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/layer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/mappings.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/mappings.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/sharded_moe.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/sharded_moe.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/moe/utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/moe/utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/text_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/text_generation.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 from typing import Dict
 
 from transformers import BertTokenizer
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.models.nlp.gpt_moe import GPTMoEModel
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.models.nlp.gpt_moe import GPTMoEModel
 
 __all__ = ['GPTMoEForTextGeneration']
 
-from weathon.utils.typing import Tensor
+from weathon.dl.utils.typing import Tensor
 
 
 @MODELS.register_module(Tasks.text_generation, module_name=Models.gpt_moe)
 class GPTMoEForTextGeneration(TorchModel):
 
     def __init__(self, model_dir: str, *args, **kwargs):
         """initialize the text generation model from the `model_dir` path.
@@ -24,15 +24,15 @@
         """
         super().__init__(model_dir, *args, **kwargs)
 
         # Temporarily compatible with DistributedGPT3 and GPT3Model,
         # the base/large model based on GPT3Model will be replaced in the future,
         # and GPT3Model will be deprecated
         if 'model_parallel_size' in kwargs:
-            from weathon.models.nlp import DistributedGPTMoE
+            from weathon.dl.models.nlp import DistributedGPTMoE
             self.model = DistributedGPTMoE(model_dir, **kwargs)
         else:
             self.model = GPTMoEModel.from_pretrained(model_dir)
             self.tokenizer = BertTokenizer.from_pretrained(model_dir)
 
     def forward(self, input: Dict[str, Tensor]) -> Dict[str, Tensor]:
         """return the result by the model
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/gpt_moe/tokenizer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/gpt_moe/tokenizer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/hf_transformers/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/hf_transformers/backbone.py`

 * *Files 2% similar despite different names*

```diff
@@ -13,19 +13,19 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """PyTorch BERT model. """
 
 from transformers import AutoConfig, AutoModel
 from transformers.modeling_utils import PreTrainedModel
 
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.logger import get_logger
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 def _get_model_class(config, model_mapping):
     supported_models = model_mapping[type(config)]
     if not isinstance(supported_models, (list, tuple)):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/llama/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import LlamaConfig
     from .text_generation import LlamaForTextGeneration
     from .backbone import LlamaModel
     from .tokenization import LlamaTokenizer
     from .tokenization_fast import LlamaTokenizerFast
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/llama/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/backbone.py`

 * *Files 1% similar despite different names*

```diff
@@ -22,20 +22,20 @@
 
 import torch
 import torch.utils.checkpoint
 from torch import nn
 from transformers.activations import ACT2FN
 from transformers.modeling_utils import PreTrainedModel
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.output.nlp_outputs import AttentionBackboneModelOutput
-from weathon.utils.constants import Tasks
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.output.nlp_outputs import AttentionBackboneModelOutput
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.logger import get_logger
 from .configuration import LlamaConfig
 
 logger = get_logger(__name__)
 
 _CONFIG_FOR_DOC = 'LlamaConfig'
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/llama/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/configuration.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/llama/convert_llama_weights_to_hf.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/convert_llama_weights_to_hf.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/llama/text_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/text_generation.py`

 * *Files 1% similar despite different names*

```diff
@@ -18,19 +18,19 @@
 # limitations under the License.
 from typing import Dict, List, Optional, Tuple, Union
 
 import torch.utils.checkpoint
 from torch import nn
 from torch.nn import CrossEntropyLoss
 
-from weathon.utils.constants.metainfo import Models
-from weathon.utils.typing import Tensor
-from weathon.registry import MODELS
-from weathon.utils.output.nlp_outputs import AttentionTextGenerationModelOutput
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.utils.typing import Tensor
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.output.nlp_outputs import AttentionTextGenerationModelOutput
+from weathon.dl.utils.constants import Tasks
 from .backbone import LlamaModel, LlamaPreTrainedModel
 
 
 # This file is mainly copied from the llama code of transformers
 @MODELS.register_module(Tasks.text_generation, module_name=Models.llama)
 class LlamaForTextGeneration(LlamaPreTrainedModel):
     _keys_to_ignore_on_load_missing = [r'lm_head.weight']
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/llama/tokenization.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/tokenization.py`

 * *Files 0% similar despite different names*

```diff
@@ -21,15 +21,15 @@
 import os
 from shutil import copyfile
 from typing import Any, Dict, List, Optional, Tuple
 
 import sentencepiece as spm
 from transformers.tokenization_utils import AddedToken, PreTrainedTokenizer
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 # This file is mainly copied from the llama code of transformers
 logger = get_logger(__name__)
 
 VOCAB_FILES_NAMES = {'vocab_file': 'tokenizer.model'}
 
 PRETRAINED_VOCAB_FILES_MAP = {
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/llama/tokenization_fast.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/llama/tokenization_fast.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 from shutil import copyfile
 from typing import Optional, Tuple
 
 from transformers.tokenization_utils_fast import PreTrainedTokenizerFast
 from transformers.utils import is_sentencepiece_available
 from transformers.utils.versions import require_version
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 # This file is mainly copied from the llama code of transformers
 require_version('tokenizers>=0.13.3')
 
 if is_sentencepiece_available():
     from .tokenization import LlamaTokenizer
 else:
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/lstm/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/lstm/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .backbone import LSTMModel
     from .token_classification import LSTMForTokenClassificationWithCRF
 else:
     _import_structure = {
         'backbone': ['LSTM'],
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/lstm/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/lstm/backbone.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 """PyTorch LSTM model. """
 
 import torch.nn as nn
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.output.nlp_outputs import BackboneModelOutput
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.output.nlp_outputs import BackboneModelOutput
+from weathon.dl.utils.constants import Tasks
 
 
 @MODELS.register_module(group_key=Tasks.backbone, module_name=Models.lstm)
 class LSTMModel(TorchModel):
 
     def __init__(self, vocab_size, embed_width, hidden_size=100, **kwargs):
         super().__init__()
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/lstm/token_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/lstm/token_classification.py`

 * *Files 2% similar despite different names*

```diff
@@ -10,20 +10,20 @@
 #
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
-from weathon.utils.constants.metainfo import Heads, Models
-from weathon.registry import MODELS
-from weathon.models.nlp.task_models import (
+from weathon.dl.utils.constants.metainfo import Heads, Models
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.task_models import (
     ModelForTokenClassification, ModelForTokenClassificationWithCRF)
-from weathon.utils import logger as logging
-from weathon.utils.constants import Tasks
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants import Tasks
 
 logger = logging.get_logger()
 
 
 @MODELS.register_module(Tasks.token_classification, module_name=Models.lcrf)
 @MODELS.register_module(
     Tasks.named_entity_recognition, module_name=Models.lcrf)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/megatron_bert/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/megatron_bert/__init__.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import MegatronBertConfig
     from .backbone import MegatronBertModel
     from .fill_mask import MegatronBertForMaskedLM
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/megatron_bert/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/megatron_bert/backbone.py`

 * *Files 0% similar despite different names*

```diff
@@ -21,21 +21,21 @@
 from torch import nn
 from transformers.activations import ACT2FN
 from transformers.modeling_utils import (PreTrainedModel,
                                          apply_chunking_to_forward,
                                          find_pruneable_heads_and_indices,
                                          prune_linear_layer)
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.output.nlp_outputs import AttentionBackboneModelOutput
-from weathon.utils.constants import Tasks
-from weathon.utils.logger import get_logger
-from weathon.utils.nlp.utils import parse_labels_in_order
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.output.nlp_outputs import AttentionBackboneModelOutput
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.nlp.utils import parse_labels_in_order
 from .configuration import MegatronBertConfig
 
 logger = get_logger()
 
 _CONFIG_FOR_DOC = 'MegatronBertConfig'
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/megatron_bert/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/megatron_bert/configuration.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 
 from collections import OrderedDict
 from typing import Mapping
 
 from transformers.configuration_utils import PretrainedConfig
 from transformers.onnx import OnnxConfig
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 class MegatronBertConfig(PretrainedConfig):
     r"""
     This is the configuration class to store the configuration of a [`MegatronBertModel`]. It is used to instantiate a
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/megatron_bert/fill_mask.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/megatron_bert/fill_mask.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,19 +16,19 @@
 
 import torch
 import torch.nn as nn
 import torch.utils.checkpoint
 from torch.nn import CrossEntropyLoss
 from transformers.activations import ACT2FN
 
-from weathon.utils.constants.metainfo import Models
-from weathon.registry import MODELS
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.registry import MODELS
 from weathon.outputs import AttentionFillMaskModelOutput
-from weathon.utils import logger as logging
-from weathon.utils.constants import Tasks
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants import Tasks
 from .backbone import MegatronBertModel, MegatronBertPreTrainedModel
 from .configuration import MegatronBertConfig
 
 logger = logging.get_logger()
 
 
 # Copied from transformers.models.bert.modeling_bert.BertPredictionHeadTransform with Bert->MegatronBert
@@ -213,15 +213,15 @@
                 the loss is only computed for the tokens with labels in `[0, ...,
                 config.vocab_size]`
 
         Returns:
             Returns `modelscope.outputs.AttentionFillMaskModelOutput`
 
         Examples:
-            >>> from weathon.models import Model
+            >>> from weathon.dl.models import Model
             >>> from weathon.preprocessors import Preprocessor
             >>> model = Model.from_pretrained('damo/nlp_megatronbert_backbone_base_std')
             >>> preprocessor = Preprocessor.from_pretrained('damo/nlp_megatronbert_backbone_base_std')
             >>> print(model(**preprocessor(('This is a test', 'This is also a test'))))
         """
 
         return_dict = return_dict if return_dict is not None else self.config.use_return_dict
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # Modified by Zhipu.AI
 # Original Copyright (c) Alibaba, Inc. and its affiliates.
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .mglm_for_text_summarization import MGLMForTextSummarization
 else:
     _import_structure = {
         'mglm_for_text_summarization': ['MGLMForTextSummarization'],
     }
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/arguments.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/arguments.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/blocklm_utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/blocklm_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/configure_data.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/configure_data.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/__init__.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/corpora.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/corpora.py`

 * *Files 0% similar despite different names*

```diff
@@ -18,15 +18,15 @@
 from multiprocessing import Process, Queue
 from queue import Empty
 
 import json
 import tqdm
 from torch.utils import data
 
-from weathon.models.nlp.backbone.mglm.utils import print_rank_0
+from weathon.dl.models.nlp.backbone.mglm.utils import print_rank_0
 from .lazy_loader import LazyLoader
 
 NUM_PROCESSES = 100
 
 
 def punctuation_standardization(string: str):
     punctuation_dict = {
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/datasets.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/datasets.py`

 * *Files 0% similar despite different names*

```diff
@@ -24,15 +24,15 @@
 import nltk
 import numpy as np
 import pandas as pd
 import torch
 from nltk import tokenize
 from torch.utils import data
 
-from weathon.models.nlp.backbone.mglm.utils import print_rank_0
+from weathon.dl.models.nlp.backbone.mglm.utils import print_rank_0
 from .lazy_loader import LazyLoader
 
 
 class ShuffleDataset(data.Dataset):
 
     def __init__(self, ds):
         self.ds = ds
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/extraction.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/extraction.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/file_utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/file_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/lazy_loader.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/lazy_loader.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/samplers.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/samplers.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/sp_tokenizer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/sp_tokenizer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/tokenization.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/tokenization.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/tokenization_gpt2.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/tokenization_gpt2.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/data_utils/wordpiece.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/data_utils/wordpiece.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/generation_utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/generation_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/mglm_for_text_summarization.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/mglm_for_text_summarization.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,21 +3,21 @@
 from os import path as osp
 from typing import Dict
 
 import torch
 import torch.nn.functional as F
 from megatron_util import mpu
 
-from weathon.utils.constants.metainfo import Models
-from weathon.models.base import TorchModel
-from weathon.registry import MODELS
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.models.base import TorchModel
+from weathon.dl.registry import MODELS
 from weathon.outputs import OutputKeys
-from weathon.utils.config.config import Config
-from weathon.utils.constants import ModelFile, Tasks
-from weathon.utils.megatron_utils import init_megatron_util
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import ModelFile, Tasks
+from weathon.dl.utils.megatron_utils import init_megatron_util
 from .arguments import get_args
 from .train_utils import get_model
 from .utils import load_checkpoint
 
 __all__ = ['MGLMForTextSummarization']
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/__init__.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/distributed.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/distributed.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/downstream.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/downstream.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/modeling_bert.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/modeling_bert.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/modeling_glm.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/modeling_glm.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 """GPT-2 model."""
 
 import torch
 import torch.nn as nn
 import torch.nn.functional as F
 from megatron_util import mpu, print_rank_0
 
-from weathon.models.nlp.mglm.model.prompt import PromptSpell
+from weathon.dl.models.nlp.mglm.model.prompt import PromptSpell
 from .transformer import GPT2ParallelTransformer
 
 
 def init_method_normal(std=0.02):
     """Init method based on normal distribution.
 
     This is only used for embeddings. The transformer has its
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/prompt.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/prompt.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/model/transformer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/model/transformer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/process_grid.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/process_grid.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/data_utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/data_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/eval_utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/eval_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/language_model/dataset.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/language_model/dataset.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/language_model/detokenizer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/language_model/detokenizer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/language_model/finetune.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/language_model/finetune.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/seq2seq/dataset.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/seq2seq/dataset.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/seq2seq/evaluate.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/seq2seq/evaluate.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/seq2seq/finetune.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/seq2seq/finetune.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/dataset.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/dataset.py`

 * *Files 0% similar despite different names*

```diff
@@ -30,16 +30,16 @@
 from data_utils import (build_input_from_ids, build_sample,
                         num_special_tokens_to_add)
 from data_utils.corpora import punctuation_standardization
 from torch.utils.data import Dataset
 from tqdm import tqdm
 from utils import print_rank_0
 
-from weathon.models.nlp.mglm.tasks.data_utils import InputExample
-from weathon.models.nlp.mglm.tasks.superglue.pvp import PVPS
+from weathon.dl.models.nlp.mglm.tasks.data_utils import InputExample
+from weathon.dl.models.nlp.mglm.tasks.superglue.pvp import PVPS
 
 TRAIN_SET = 'train'
 DEV_SET = 'dev'
 TEST_SET = 'test'
 TRUE_DEV_SET = 'true_dev'
 UNLABELED_SET = 'unlabeled'
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/evaluate.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/evaluate.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/finetune.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/finetune.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/tasks/superglue/pvp.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/tasks/superglue/pvp.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/test/test_block.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/test/test_block.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/test/test_rel_shift.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/test/test_rel_shift.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/train_utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/train_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/mglm/utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/mglm/utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/palm_v2/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/palm_v2/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import PalmConfig
     from .text_generation import (
         AbsSummarizer,
         PalmForTextGeneration,
         Translator,
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/palm_v2/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/palm_v2/configuration.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """ PALM model configuration """
 
 from transformers.configuration_utils import PretrainedConfig
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 class PalmConfig(PretrainedConfig):
     r"""
     Configuration objects inherit from :class:`~transformers.PretrainedConfig` and can be used to control the model
@@ -61,15 +61,15 @@
         dec_hidden_layers (:obj:`int`, `optional`, defaults to 12):
             Number of hidden layers in the Transformer decoder.
         attn_separate (:obj:`bool`, `optional`, defaults to false):
             Whether or not to separate the q, k, v of attention.
 
     Examples:
 
-        >>> from weathon.models.nlp.palm_v2 import PalmForConditionalGeneration, PalmConfig
+        >>> from weathon.dl.models.nlp.palm_v2 import PalmForConditionalGeneration, PalmConfig
         >>> configuration = PalmConfig()
 
         >>> # Initializing a model from the configuration
         >>> model = PalmForConditionalGeneration(configuration)
 
         >>> # Accessing the model configuration
         >>> configuration = model.config
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/palm_v2/dureader_eval.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/palm_v2/dureader_eval.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/palm_v2/text_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/palm_v2/text_generation.py`

 * *Files 1% similar despite different names*

```diff
@@ -29,20 +29,20 @@
 from torch import Tensor, nn
 from torch.nn.init import xavier_uniform_
 from transformers import (BertConfig, BertModel, BertTokenizer, RobertaConfig,
                           RobertaModel, RobertaTokenizer)
 from transformers.activations import ACT2FN
 from transformers.modeling_utils import PreTrainedModel
 
-from weathon.base import TorchModel, BaseModel
-from weathon.utils.constants.metainfo import Models
-from weathon.registry import MODELS
-from weathon.utils import logger as logging
-from weathon.utils.constants import Tasks
-from weathon.utils.output.nlp_outputs import TextGenerationModelOutput, TokenGeneratorOutput
+from weathon.dl.base import TorchModel, BaseModel
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.registry import MODELS
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.output.nlp_outputs import TextGenerationModelOutput, TokenGeneratorOutput
 from .configuration import PalmConfig
 from .dureader_eval import compute_bleu_rouge, normalize
 
 CONFIG_NAME = 'config.json'
 WEIGHTS_NAME = 'pytorch_model.bin'
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/peer/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import PeerConfig
     from .text_classification import PeerForSequenceClassification
 else:
     _import_structure = {
         'configuration': ['PeerConfig'],
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/peer/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/backbone.py`

 * *Files 1% similar despite different names*

```diff
@@ -26,17 +26,17 @@
 from transformers.modeling_outputs import \
     BaseModelOutputWithPastAndCrossAttentions
 from transformers.modeling_utils import (PreTrainedModel,
                                          apply_chunking_to_forward,
                                          find_pruneable_heads_and_indices,
                                          prune_linear_layer)
 
-from weathon.base import TorchModel
-from weathon.utils import logger as logging
-from weathon.utils.nlp.utils import parse_labels_in_order
+from weathon.dl.base import TorchModel
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.nlp.utils import parse_labels_in_order
 from .configuration import PeerConfig
 from .sas_utils import SequenceSideInfo
 
 logger = logging.get_logger(__name__)
 
 PEER_PRETRAINED_MODEL_ARCHIVE_LIST = [
     'google/peer-small-generator',
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/peer/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/configuration.py`

 * *Files 0% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """ PEER model configuration """
 
 # modified the path according to the structure in my directory csssl_4_15/cssl/ and its env
 from transformers.configuration_utils import PretrainedConfig
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger(__name__)
 
 
 class PeerConfig(PretrainedConfig):
     r"""
     This is the configuration class to store the configuration of a :class:`~transformers.PeerModel` or a
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/peer/sas_utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/sas_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/peer/text_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/peer/text_classification.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,19 +15,19 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 import copy
 
 from torch.nn import CrossEntropyLoss, MSELoss
 
-from weathon.utils.constants.metainfo import Models
-from weathon.registry import MODELS
-from weathon.utils import logger as logging
-from weathon.utils.constants import Tasks
-from weathon.utils.output.nlp_outputs import AttentionTextClassificationModelOutput
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.registry import MODELS
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.output.nlp_outputs import AttentionTextClassificationModelOutput
 from .backbone import (PeerClassificationHead, PeerModel, PeerPreTrainedModel,
                        PeerTopModel)
 
 logger = logging.get_logger()
 
 
 @MODELS.register_module(Tasks.text_classification, module_name=Models.peer)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug/AnnealingLR.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/AnnealingLR.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import PlugNLGConfig
     from .backbone import PlugModel
     from .distributed_plug import DistributedPlug
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/backbone.py`

 * *Files 1% similar despite different names*

```diff
@@ -20,15 +20,15 @@
 import math
 
 import torch
 import torch.nn.functional as F
 from megatron_util import mpu
 from torch import nn
 
-from weathon.utils.nlp.distributed import (normal_init_method,
+from weathon.dl.utils.nlp.distributed import (normal_init_method,
                                               scaled_init_method)
 from .configuration import PlugNLGConfig, PlugNLUConfig
 
 logger = logging.getLogger(__name__)
 
 
 def gelu(x):
@@ -908,15 +908,15 @@
             Initializing with a config file does not load the weights associated with the model, only the
             configuration. Check out the [`~DistributedPlug.initialize_model`] method to load the model weights.
     Examples:
 
     >>> # The PLUG model has 27B parameters and usually need to run on multiple GPUs. The example given
     >>> # here only initializes a slice of the model on a single GPU.
     >>> # Check out the [`~DistributedPipeline.__init__`] method to initialize entire PLUG model.
-    >>> from weathon.models.nlp.plug import PlugNLGConfig, PlugModel
+    >>> from weathon.dl.models.nlp.plug import PlugNLGConfig, PlugModel
 
     >>> # Initializing a Plug configuration
     >>> configuration = PlugNLGConfig()
 
     >>> # Initializing a model from the configuration
     >>> model = PlugModel(configuration)
     """
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/configuration.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 # limitations under the License.
 
 import copy
 
 import json
 from transformers import PretrainedConfig
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 class PlugNLUConfig(PretrainedConfig):
     model_type = 'plugNLU'
 
@@ -182,15 +182,15 @@
             Whether or not to separate query-key-value to query, key, value in the Attention.
 
     Example:
 
     >>> # The PLUG model has 27B parameters and usually need to run on multiple GPUs. The example given
     >>> # here only initializes a slice of the model on a single GPU.
     >>> # Check out the [`~DistributedPipeline.__init__`] method to initialize entire PLUG model.
-    >>> from weathon.models.nlp.plug import PlugNLGConfig, PlugModel
+    >>> from weathon.dl.models.nlp.plug import PlugNLGConfig, PlugModel
 
     >>> # Initializing a Plug configuration
     >>> configuration = PlugNLGConfig()
 
     >>> # Initializing a model from the configuration
     >>> model = PlugModel(configuration)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug/distributed_plug.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/distributed_plug.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 from typing import Dict
 
 import torch
 from megatron_util import mpu, print_rank_0
 from megatron_util.fp16 import FP16_Module
 from torch.nn import functional as F
 
-from weathon.base import TorchModel
-from weathon.utils.logger import get_logger
-from weathon.utils.megatron_utils import init_megatron_util
-from weathon.utils.nlp.load_checkpoint import pre_load
-from weathon.utils.typing import Tensor
+from weathon.dl.base import TorchModel
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.megatron_utils import init_megatron_util
+from weathon.dl.utils.nlp.load_checkpoint import pre_load
+from weathon.dl.utils.typing import Tensor
 from . import PlugModel
 from .configuration import PlugNLGConfig
 
 logger = get_logger()
 
 
 class DistributedPlug(TorchModel):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug/generator.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug/generator.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .backbone import (PlugMentalModel, PlugMentalPreTrainedModel)
     from .configuration import PlugMentalConfig
     from .text_classification import PlugMentalForSequenceClassification
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/adv_utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/adv_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 import torch
 from torch import nn
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 def _symmetric_kl_div(logits1, logits2, attention_mask=None):
     """
     Calclate two logits' the KL div value symmetrically.
@@ -92,15 +92,15 @@
     loss = _symmetric_kl_div(ori_logits, v1_logits, attention_mask)
     emb_grad = torch.autograd.grad(loss, embedding_1)[0].data
     emb_grad_norm = emb_grad.norm(
         dim=2, keepdim=True, p=float('inf')).max(
             1, keepdim=True)[0]
     is_nan = torch.any(torch.isnan(emb_grad_norm))
     if is_nan:
-        logger.warning('Nan occured when calculating adv loss.')
+        logger.warning('Nan occurred when calculating adv loss.')
         return ori_loss
     emb_grad = emb_grad / (emb_grad_norm + 1e-6)
     embedding_2 = embedding_1 + adv_grad_factor * emb_grad
     embedding_2 = torch.max(embedding_1 - adv_bound, embedding_2)
     embedding_2 = torch.min(embedding_1 + adv_bound, embedding_2)
     outputs = model(**kwargs, inputs_embeds=embedding_2)
     adv_logits = outputs.logits
@@ -150,15 +150,15 @@
     loss = loss / 2
     emb_grad = torch.autograd.grad(loss, embedding_1)[0].data
     emb_grad_norm = emb_grad.norm(
         dim=2, keepdim=True, p=float('inf')).max(
             1, keepdim=True)[0]
     is_nan = torch.any(torch.isnan(emb_grad_norm))
     if is_nan:
-        logger.warning('Nan occured when calculating pair adv loss.')
+        logger.warning('Nan occurred when calculating pair adv loss.')
         return ori_loss
     emb_grad = emb_grad / emb_grad_norm
     embedding_2 = embedding_1 + adv_grad_factor * emb_grad
     embedding_2 = torch.max(embedding_1 - adv_bound, embedding_2)
     embedding_2 = torch.min(embedding_1 + adv_bound, embedding_2)
     outputs = model(**kwargs, inputs_embeds=embedding_2)
     adv_logits_start, adv_logits_end = outputs.logits
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/backbone.py`

 * *Files 0% similar despite different names*

```diff
@@ -26,21 +26,21 @@
 from packaging import version
 from transformers.activations import ACT2FN
 from transformers.modeling_utils import (PreTrainedModel,
                                          apply_chunking_to_forward,
                                          find_pruneable_heads_and_indices,
                                          prune_linear_layer)
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.output.nlp_outputs import AttentionBackboneModelOutput
-from weathon.utils.constants import Tasks
-from weathon.utils.logger import get_logger
-from weathon.utils.nlp.utils import parse_labels_in_order
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.output.nlp_outputs import AttentionBackboneModelOutput
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.nlp.utils import parse_labels_in_order
 from .configuration import PlugMentalConfig
 
 logger = get_logger()
 
 
 class SbertEmbeddings(nn.Module):
     """Construct the embeddings from word, position and token_type embeddings."""
@@ -946,15 +946,15 @@
                 If set to :obj:`True`, :obj:`past_key_values` key value states are returned and can be used to speed up
                 decoding (see :obj:`past_key_values`).
 
         Returns:
             Returns `modelscope.outputs.AttentionBackboneModelOutputWithEmbedding`
 
         Examples:
-            >>> from weathon.models import Model
+            >>> from weathon.dl.models import Model
             >>> from weathon.preprocessors import Preprocessor
             >>> model = Model.from_pretrained('damo/nlp_plug-mental_backbone_base_std', task='backbone')
             >>> preprocessor = Preprocessor.from_pretrained('damo/nlp_plug-mental_backbone_base_std')
             >>> print(model(**preprocessor('这是个测试')))
         """
 
         output_attentions = output_attentions if output_attentions is not None else self.config.output_attentions
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/configuration.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """ PLUG mental model configuration, mainly copied from :class:`~transformers.BertConfig` """
 from transformers import PretrainedConfig
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 class PlugMentalConfig(PretrainedConfig):
     r"""
     This is the configuration class to store the configuration
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/plug_mental/text_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/text_classification.py`

 * *Files 0% similar despite different names*

```diff
@@ -16,19 +16,19 @@
 # limitations under the License.
 
 import torch
 import torch.nn as nn
 import torch.utils.checkpoint
 from torch.nn import BCEWithLogitsLoss, CrossEntropyLoss, MSELoss
 
-from weathon.utils.constants.metainfo import Models
-from weathon.registry import MODELS
-from weathon.utils import logger as logging
-from weathon.utils.constants import Tasks
-from weathon.utils.output.nlp_outputs import AttentionTextClassificationModelOutput
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.registry import MODELS
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.output.nlp_outputs import AttentionTextClassificationModelOutput
 from .adv_utils import compute_adv_loss
 from .backbone import PlugMentalModel, PlugMentalPreTrainedModel
 from .configuration import PlugMentalConfig
 
 logger = logging.get_logger()
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import PoNetConfig
     from .backbone import (PoNetModel, PoNetPreTrainedModel)
     from .tokenization import PoNetTokenizer
     from .fill_mask import PoNetForMaskedLM
     from .document_segmentation import PoNetForDocumentSegmentation
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/backbone.py`

 * *Files 0% similar despite different names*

```diff
@@ -24,20 +24,20 @@
 from torch import nn
 from transformers.activations import ACT2FN
 from transformers.modeling_utils import (PreTrainedModel,
                                          apply_chunking_to_forward,
                                          find_pruneable_heads_and_indices,
                                          prune_linear_layer)
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.output.nlp_outputs import AttentionBackboneModelOutput
-from weathon.utils.constants import Tasks
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.output.nlp_outputs import AttentionBackboneModelOutput
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.logger import get_logger
 from .configuration import PoNetConfig
 
 logger = get_logger()
 
 is_pytorch_12plus = LooseVersion(torch.__version__) >= LooseVersion('1.12.0')
 
 CLS_ID = 101
@@ -781,15 +781,15 @@
                 If set to :obj:`True`, :obj:`past_key_values` key value states are returned and can be used to speed up
                 decoding (see :obj:`past_key_values`).
 
         Returns:
             Returns `modelscope.outputs.AttentionBackboneModelOutput`
 
         Examples:
-            >>> from weathon.models import Model
+            >>> from weathon.dl.models import Model
             >>> from weathon.preprocessors import Preprocessor
             >>> model = Model.from_pretrained('damo/nlp_ponet_fill-mask_chinese-base', task='backbone')
             >>> preprocessor = Preprocessor.from_pretrained('damo/nlp_ponet_fill-mask_chinese-base')
             >>> print(model(**preprocessor('这是个测试')))
         """
         output_attentions = output_attentions if output_attentions is not None else self.config.output_attentions
         output_hidden_states = (
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/configuration.py`

 * *Files 0% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """ PoNet model configuration, mainly copied from :class:`~transformers.BertConfig` """
 from transformers import PretrainedConfig
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 class PoNetConfig(PretrainedConfig):
     r"""
     This is the configuration class to store the configuration
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/document_segmentation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/document_segmentation.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 from typing import Any, Dict
 
 import torch
 from torch import nn
 from torch.nn import CrossEntropyLoss
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import BaseModel
-from weathon.registry import MODELS
-from weathon.models.nlp.bert import BertConfig
-from weathon.utils.constants import Tasks
-from weathon.utils.output.nlp_outputs import AttentionTokenClassificationModelOutput
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.bert import BertConfig
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.output.nlp_outputs import AttentionTokenClassificationModelOutput
 from .backbone import PoNetModel, PoNetPreTrainedModel
 from .configuration import PoNetConfig
 
 __all__ = ['PoNetForDocumentSegmentation']
 
 
 @MODELS.register_module(
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/fill_mask.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/fill_mask.py`

 * *Files 0% similar despite different names*

```diff
@@ -15,19 +15,19 @@
 # limitations under the License.
 
 import torch.utils.checkpoint
 from torch import nn
 from torch.nn import CrossEntropyLoss
 from transformers.activations import ACT2FN
 
-from weathon.utils.constants.metainfo import Models
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.logger import get_logger
-from weathon.utils.output.nlp_outputs import AttentionFillMaskModelOutput
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.output.nlp_outputs import AttentionFillMaskModelOutput
 from .backbone import PoNetModel, PoNetPreTrainedModel
 
 logger = get_logger()
 
 
 class PoNetPredictionHeadTransform(nn.Module):
 
@@ -196,15 +196,15 @@
                 config.vocab_size]`` (see ``input_ids`` docstring) Tokens with indices set to ``-100`` are ignored
                 (masked), the loss is only computed for the tokens with labels in ``[0, ..., config.vocab_size]``
 
         Returns:
             Returns `modelscope.outputs.AttentionFillMaskModelOutput`
 
         Examples:
-            >>> from weathon.models import Model
+            >>> from weathon.dl.models import Model
             >>> from weathon.preprocessors import Preprocessor
             >>> model = Model.from_pretrained('damo/nlp_ponet_fill-mask_chinese-base')
             >>> preprocessor = Preprocessor.from_pretrained('damo/nlp_ponet_fill-mask_chinese-base')
             >>> # Call the model, return some tensors
             >>> print(model(**preprocessor('你师父差得动你，你师父可[MASK]不动我。')))
             >>> # Call the pipeline
             >>> from weathon.pipelines import pipeline
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/ponet/tokenization.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/ponet/tokenization.py`

 * *Files 0% similar despite different names*

```diff
@@ -17,16 +17,16 @@
 
 from typing import TYPE_CHECKING, Any, Dict, List, Optional, Union
 
 from transformers.file_utils import PaddingStrategy
 from transformers.models.bert.tokenization_bert import BertTokenizer
 from transformers.tokenization_utils import BatchEncoding, EncodedInput
 
-from weathon.utils.constants import ModelFile
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants import ModelFile
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 VOCAB_FILES_NAMES = {'vocab_file': ModelFile.VOCAB_FILE}
 
 PRETRAINED_VOCAB_FILES_MAP = {'vocab_file': {}}
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .model import SpaceGenerator
     from .model import SpaceModelBase, SpaceTokenizer
     from .dialog_intent_prediction import SpaceForDialogIntent
     from .dialog_modeling import SpaceForDialogModeling
     from .dialog_state_tracking import SpaceForDST
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/configuration.py`

 * *Files 12% similar despite different names*

```diff
@@ -13,16 +13,16 @@
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """Space configuration, mainly copied from :class:`~transformers.configuration_xlm_roberta` """
 
-from weathon.models.nlp.backbone.structbert import SbertConfig
-from weathon.utils import logger as logging
+from weathon.dl.models.nlp.backbone.structbert import SbertConfig
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 class SpaceConfig(SbertConfig):
     """
     This class overrides [`SbertConfig`]. Please check the superclass for the appropriate
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/dialog_intent_prediction.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/dialog_intent_prediction.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 import os
 from typing import Dict
 
-from weathon.utils.constants import Tasks, ModelFile
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.models.nlp.space import SpaceGenerator, SpaceModelBase
+from weathon.dl.utils.constants import Tasks, ModelFile
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.space import SpaceGenerator, SpaceModelBase
 from weathon.preprocessors.nlp import IntentBPETextField
-from weathon.utils.config.config import Config
+from weathon.dl.utils.config.config import Config
 
 __all__ = ['SpaceForDialogIntent']
 
 
-from weathon.utils.typing import Tensor
+from weathon.dl.utils.typing import Tensor
 
 
 @MODELS.register_module(Tasks.task_oriented_conversation, module_name=Models.space_intent)
 class SpaceForDialogIntent(TorchModel):
 
     def __init__(self, model_dir: str, *args, **kwargs):
         """initialize the test generation model from the `model_dir` path.
@@ -26,15 +26,15 @@
             text_field (`BPETextField`, *optional*, defaults to `IntentBPETextField`):
                 The text field.
             config (`Config`, *optional*, defaults to config in model hub):
                 The config.
         """
 
         super().__init__(model_dir, *args, **kwargs)
-        from weathon.trainers.nlp.space.trainer.intent_trainer import \
+        from weathon.dl.trainers.nlp import \
             IntentTrainer
         self.model_dir = model_dir
         self.config = kwargs.pop(
             'config',
             Config.from_file(
                 os.path.join(self.model_dir, ModelFile.CONFIGURATION)))
         self.text_field = kwargs.pop('text_field', IntentBPETextField(self.model_dir, config=self.config))
@@ -74,16 +74,16 @@
                     {
                         'pred': array([2.62349960e-03 4.12110658e-03 4.12748595e-05 3.77560973e-05
                                 1.08599677e-04 1.72710388e-05 2.95618793e-05 1.93638436e-04
                                 6.45841064e-05 1.15997791e-04 5.11605394e-05 9.87020373e-01
                                 2.66957268e-05 4.72324500e-05 9.74208378e-05], dtype=float32),
                     }
         Example:
-            >>> from weathon.utils.hub.utils import snapshot_download
-            >>> from weathon.models.nlp import SpaceForDialogIntent
+            >>> from weathon.dl.utils.hub.utils import snapshot_download
+            >>> from weathon.dl.models.nlp import SpaceForDialogIntent
             >>> from weathon.preprocessors import DialogIntentPredictionPreprocessor
             >>> cache_path = snapshot_download('damo/nlp_space_dialog-intent-prediction')
             >>> preprocessor = DialogIntentPredictionPreprocessor(model_dir=cache_path)
             >>> model = SpaceForDialogIntent(
                     model_dir=cache_path,
                     text_field=preprocessor.text_field,
                     config=preprocessor.config)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/dialog_modeling.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/dialog_modeling.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 import os
 from typing import Dict
 
-from weathon.utils.constants import ModelFile, Tasks
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.models.nlp.space import SpaceGenerator, SpaceModelBase
+from weathon.dl.utils.constants import ModelFile, Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.space import SpaceGenerator, SpaceModelBase
 from weathon.preprocessors.nlp import MultiWOZBPETextField
-from weathon.utils.config.config import Config
+from weathon.dl.utils.config.config import Config
 
 __all__ = ['SpaceForDialogModeling']
 
-from weathon.utils.typing import Tensor
+from weathon.dl.utils.typing import Tensor
 
 
 @MODELS.register_module(Tasks.task_oriented_conversation, module_name=Models.space_modeling)
 class SpaceForDialogModeling(TorchModel):
 
     def __init__(self, model_dir: str, *args, **kwargs):
         """initialize the test generation model from the `model_dir` path.
@@ -26,15 +26,15 @@
             text_field (`BPETextField`, *optional*, defaults to `MultiWOZBPETextField`):
                 The text field.
             config (`Config`, *optional*, defaults to config in model hub):
                 The config.
         """
 
         super().__init__(model_dir, *args, **kwargs)
-        from weathon.trainers.nlp.space.trainer.gen_trainer import MultiWOZTrainer
+        from weathon.dl.trainers.nlp import MultiWOZTrainer
         self.model_dir = model_dir
         self.config = kwargs.pop(
             'config',
             Config.from_file(
                 os.path.join(self.model_dir, ModelFile.CONFIGURATION)))
 
         import torch
@@ -83,16 +83,16 @@
                         'resp': array([293,1023,123,1123]), #vocab label for response
                         'bspn': array([123,321,2,24,1 ]),
                         'aspn': array([47,8345,32,29,1983]),
                         'db': array([19, 24, 20]),
                     }
 
         Examples:
-            >>> from weathon.utils.hub.utils import snapshot_download
-            >>> from weathon.models.nlp import SpaceForDialogModeling
+            >>> from weathon.dl.utils.hub.utils import snapshot_download
+            >>> from weathon.dl.models.nlp import SpaceForDialogModeling
             >>> from weathon.preprocessors import DialogModelingPreprocessor
             >>> cache_path = snapshot_download('damo/nlp_space_dialog-modeling')
             >>> preprocessor = DialogModelingPreprocessor(model_dir=cache_path)
             >>> model = SpaceForDialogModeling(model_dir=cache_path,
                     text_field=preprocessor.text_field,
                     config=preprocessor.config)
             >>> print(model(preprocessor({
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/dialog_state_tracking.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/dialog_state_tracking.py`

 * *Files 2% similar despite different names*

```diff
@@ -20,20 +20,20 @@
 
 import torch
 from torch import nn
 from torch.nn import CrossEntropyLoss
 from transformers.file_utils import add_start_docstrings
 from transformers.modeling_utils import PreTrainedModel
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.utils.typing import Tensor
-from weathon.registry import MODELS
-from weathon.models.nlp.backbone.structbert import (SbertModel)
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.utils.typing import Tensor
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.backbone.structbert import (SbertModel)
+from weathon.dl.utils.constants import Tasks
 from .configuration import SpaceConfig
 
 SPACE_START_DOCSTRING = r"""
 
     This model inherits from [`PreTrainedModel`]. Check the superclass documentation for the generic
     methods the library implements for all its model (such as downloading or saving, resizing the input embeddings,
     pruning heads etc.)
@@ -196,16 +196,16 @@
                         'values': array([{'taxi-leaveAt': 'none', 'taxi-destination': 'none'}]),
                         'inform':  array([{'taxi-leaveAt': 'none', 'taxi-destination': 'none'}]),
                         'prefix': str('final'), #default value
                         'ds':  array([{'taxi-leaveAt': 'none', 'taxi-destination': 'none'}])
                     }
 
         Example:
-            >>> from weathon.utils.hub.utils import snapshot_download
-            >>> from weathon.models.nlp import SpaceForDST
+            >>> from weathon.dl.utils.hub.utils import snapshot_download
+            >>> from weathon.dl.models.nlp import SpaceForDST
             >>> from weathon.preprocessors import DialogStateTrackingPreprocessor
             >>> cache_path = snapshot_download('damo/nlp_space_dialog-state-tracking')
             >>> model = SpaceForDST.from_pretrained(cache_path)
             >>> preprocessor = DialogStateTrackingPreprocessor(model_dir=cache_path)
             >>> print(model(preprocessor({
                     'utter': {
                         'User-1': "Hi, I'm looking for a train that is going"
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/gen_unified_transformer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/gen_unified_transformer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/generator.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/generator.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/intent_unified_transformer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/intent_unified_transformer.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import torch
 import torch.nn as nn
 import torch.nn.functional as F
 
-from weathon.utils.nlp.space.criterions import compute_kl_loss
+from weathon.dl.utils.nlp.space.criterions import compute_kl_loss
 from .unified_transformer import UnifiedTransformer
 
 
 class IntentUnifiedTransformer(UnifiedTransformer):
     """
     Implement intent unified transformer.
     """
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/model_base.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/model_base.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import os
 
 import torch.nn as nn
 
-from weathon.utils.constants import ModelFile
+from weathon.dl.utils.constants import ModelFile
 
 
 class SpaceModelBase(nn.Module):
     """
     Basic model wrapper for static graph and dygrpah.
     """
     _registry = dict()
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/tokenization_space.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/tokenization_space.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License
 """Tokenization classes for Space. mainly copied from :module:`~transformers.tokenization_xlm_roberta`"""
 
 from transformers import BasicTokenizer, BertTokenizer, WordpieceTokenizer
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 class SpaceTokenizer(BertTokenizer):
     """
     This class overrides [`SpaceTokenizer`]. Please check the superclass for the appropriate
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/model/unified_transformer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/model/unified_transformer.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import numpy as np
 import torch
 import torch.nn as nn
 import torch.nn.functional as F
 
-from weathon.models.nlp.space.model.model_base import SpaceModelBase
-from weathon.models.nlp.space.modules.embedder import Embedder
-from weathon.models.nlp.space.modules.transformer_block import TransformerBlock
+from weathon.dl.models.nlp.space.model.model_base import SpaceModelBase
+from weathon.dl.models.nlp.space.modules.embedder import Embedder
+from weathon.dl.models.nlp.space.modules.transformer_block import TransformerBlock
 
 
 class UnifiedTransformer(SpaceModelBase):
     """
     Implement unified transformer.
     """
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/embedder.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/embedder.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/feedforward.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/feedforward.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/functions.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/functions.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/multihead_attention.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/multihead_attention.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space/modules/transformer_block.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space/modules/transformer_block.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_cn/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_cn/backbone.py`

 * *Files 1% similar despite different names*

```diff
@@ -23,17 +23,17 @@
 import tarfile
 import tempfile
 
 import numpy as np
 import torch
 from torch import nn
 
-from weathon.models.nlp.space_T_cn.configuration import SpaceTCnConfig
-from weathon.utils.constants import ModelFile
-from weathon.utils.logger import get_logger
+from weathon.dl.models.nlp.space_T_cn.configuration import SpaceTCnConfig
+from weathon.dl.utils.constants import ModelFile
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 CONFIG_NAME = ModelFile.CONFIGURATION
 WEIGHTS_NAME = ModelFile.TORCH_MODEL_BIN_FILE
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_cn/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_cn/configuration.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_cn/table_question_answering.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_cn/table_question_answering.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,20 +2,20 @@
 from typing import Dict
 
 import numpy
 import torch
 import torch.nn.functional as F
 from transformers import BertTokenizer
 
-from weathon.base import BaseModel
-from weathon.utils.constants.metainfo import Models
-from weathon.registry import MODELS
+from weathon.dl.base import BaseModel
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.registry import MODELS
 from weathon.preprocessors.nlp.space_T_cn.fields.struct import Constant
-from weathon.utils.constants import ModelFile, Tasks
-from weathon.utils.typing import Tensor
+from weathon.dl.utils.constants import ModelFile, Tasks
+from weathon.dl.utils.typing import Tensor
 from .backbone import Seq2SQL, SpaceTCnModel
 from .configuration import SpaceTCnConfig
 
 __all__ = ['TableQuestionAnswering']
 
 
 @MODELS.register_module(
@@ -763,15 +763,15 @@
                 >>>                 [0, 0, 0, 0, 0, 0]
                 >>>             ]
                 >>>         },
                 >>>     'history_sql': None
                 >>> }
 
         Example:
-            >>> from weathon.models.nlp import TableQuestionAnswering
+            >>> from weathon.dl.models.nlp import TableQuestionAnswering
             >>> from weathon.preprocessors import TableQuestionAnsweringPreprocessor
             >>> model = TableQuestionAnswering.from_pretrained('damo/nlp_convai_text2sql_pretrain_cn')
             >>> preprocessor = TableQuestionAnsweringPreprocessor(model_dir=model.model_dir)
             >>> print(model(preprocessor({'question': '有哪些风险类型？'})))
         """
         result = self.predict(input['datas'])[0]
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/space_T_en/text_to_sql.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/space_T_en/text_to_sql.py`

 * *Files 9% similar despite different names*

```diff
@@ -2,20 +2,20 @@
 from typing import Dict, Optional
 
 import torch
 from text2sql_lgesql.asdl.asdl import ASDLGrammar
 from text2sql_lgesql.asdl.transition_system import TransitionSystem
 from text2sql_lgesql.model.model_constructor import Text2SQL
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.utils.typing import Tensor
-from weathon.registry import MODELS
-from weathon.utils.config.config import Config
-from weathon.utils.constants import ModelFile, Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.utils.typing import Tensor
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import ModelFile, Tasks
 
 __all__ = ['StarForTextToSql']
 
 
 @MODELS.register_module(
     Tasks.table_question_answering, module_name=Models.space_T_en)
 class StarForTextToSql(TorchModel):
@@ -54,16 +54,16 @@
             input (Dict[str, Tensor]): the preprocessed data
 
         Returns:
             Dict[str, Tensor]: results
                 Example:
 
         Example:
-            >>> from weathon.utils.hub.utils import snapshot_download
-            >>> from weathon.models.nlp import StarForTextToSql
+            >>> from weathon.dl.utils.hub.utils import snapshot_download
+            >>> from weathon.dl.models.nlp import StarForTextToSql
             >>> from weathon.preprocessors import ConversationalTextToSqlPreprocessor
             >>> test_case = {
                     'database_id': 'employee_hire_evaluation',
                     'local_db_path': None,
                     'utterance': [
                         "I'd like to see Shop names.", 'Which of these are hiring?',
                         'Which shop is hiring the highest number of employees?'
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .backbone import (SbertModel, SbertPreTrainedModel)
     from .configuration import SbertConfig
     from .faq_question_answering import SbertForFaqQuestionAnswering
     from .fill_mask import SbertForMaskedLM
     from .text_classification import SbertForSequenceClassification
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/adv_utils.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/plug_mental/adv_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 import torch
 from torch import nn
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 def _symmetric_kl_div(logits1, logits2, attention_mask=None):
     """
     Calclate two logits' the KL div value symmetrically.
@@ -92,15 +92,15 @@
     loss = _symmetric_kl_div(ori_logits, v1_logits, attention_mask)
     emb_grad = torch.autograd.grad(loss, embedding_1)[0].data
     emb_grad_norm = emb_grad.norm(
         dim=2, keepdim=True, p=float('inf')).max(
             1, keepdim=True)[0]
     is_nan = torch.any(torch.isnan(emb_grad_norm))
     if is_nan:
-        logger.warning('Nan occurred when calculating adv loss.')
+        logger.warning('Nan occured when calculating adv loss.')
         return ori_loss
     emb_grad = emb_grad / (emb_grad_norm + 1e-6)
     embedding_2 = embedding_1 + adv_grad_factor * emb_grad
     embedding_2 = torch.max(embedding_1 - adv_bound, embedding_2)
     embedding_2 = torch.min(embedding_1 + adv_bound, embedding_2)
     outputs = model(**kwargs, inputs_embeds=embedding_2)
     adv_logits = outputs.logits
@@ -150,15 +150,15 @@
     loss = loss / 2
     emb_grad = torch.autograd.grad(loss, embedding_1)[0].data
     emb_grad_norm = emb_grad.norm(
         dim=2, keepdim=True, p=float('inf')).max(
             1, keepdim=True)[0]
     is_nan = torch.any(torch.isnan(emb_grad_norm))
     if is_nan:
-        logger.warning('Nan occurred when calculating pair adv loss.')
+        logger.warning('Nan occured when calculating pair adv loss.')
         return ori_loss
     emb_grad = emb_grad / emb_grad_norm
     embedding_2 = embedding_1 + adv_grad_factor * emb_grad
     embedding_2 = torch.max(embedding_1 - adv_bound, embedding_2)
     embedding_2 = torch.min(embedding_1 + adv_bound, embedding_2)
     outputs = model(**kwargs, inputs_embeds=embedding_2)
     adv_logits_start, adv_logits_end = outputs.logits
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/backbone.py`

 * *Files 2% similar despite different names*

```diff
@@ -26,20 +26,20 @@
 from packaging import version
 from transformers.activations import ACT2FN
 from transformers.modeling_utils import (PreTrainedModel,
                                          apply_chunking_to_forward,
                                          find_pruneable_heads_and_indices,
                                          prune_linear_layer)
 
-from weathon.base import TorchModel, BaseModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks, Models
-from weathon.utils.logger import get_logger
-from weathon.utils.nlp.utils import parse_labels_in_order
-from weathon.utils.output import AttentionBackboneModelOutput
+from weathon.dl.base import TorchModel, BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks, Models
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.nlp.utils import parse_labels_in_order
+from weathon.dl.utils.output import AttentionBackboneModelOutput
 from .configuration import SbertConfig
 
 logger = get_logger()
 
 
 class SbertEmbeddings(nn.Module):
     """Construct the embeddings from word, position and token_type embeddings."""
@@ -787,15 +787,15 @@
                 If set to :obj:`True`, :obj:`past_key_values` key value states are returned and can be used to speed up
                 decoding (see :obj:`past_key_values`).
 
         Returns:
             Returns `modelscope.outputs.AttentionBackboneModelOutputWithEmbedding`
 
         Examples:
-            >>> from weathon.base import BaseModel,BaseProcessor
+            >>> from weathon.dl.base import BaseModel,BaseProcessor
             >>> model = BaseModel.from_pretrained('damo/nlp_structbert_backbone_base_std', task='backbone')
             >>> preprocessor = BaseProcessor.from_pretrained('damo/nlp_structbert_backbone_base_std')
             >>> print(model(**preprocessor('这是个测试')))
         """
 
         output_attentions = output_attentions if output_attentions is not None else self.config.output_attentions
         output_hidden_states = (
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/configuration.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """ StructBERT model configuration, mainly copied from :class:`~transformers.BertConfig` """
 from transformers import PretrainedConfig
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 class SbertConfig(PretrainedConfig):
     r"""
     This is the configuration class to store the configuration
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/faq_question_answering.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/faq_question_answering.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,21 +5,21 @@
 
 import torch
 import torch.nn as nn
 import torch.nn.functional as F
 from torch import Tensor
 from torch.nn import BCEWithLogitsLoss
 
-from weathon.utils.config.config import Config
-from weathon.registry import MODELS
-from weathon.models.nlp.backbone.structbert import SbertConfig, SbertModel
-from weathon.models.nlp.task_models.task_model import BaseTaskModel
-from weathon.utils.constants import ModelFile, Tasks, ConfigFields, Models
-from weathon.utils.logger import get_logger
-from weathon.utils.output import FaqQuestionAnsweringOutput
+from weathon.dl.utils.config.config import Config
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.backbone.structbert import SbertConfig, SbertModel
+from weathon.dl.models.nlp.task_models.task_model import BaseTaskModel
+from weathon.dl.utils.constants import ModelFile, Tasks, ConfigFields, Models
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.output import FaqQuestionAnsweringOutput
 
 logger = get_logger()
 
 activations = {
     'relu': F.relu,
     'tanh': torch.tanh,
     'linear': lambda x: x,
@@ -228,15 +228,15 @@
         Returns:
             Dict[str, Tensor]: result, it contains the following key:
 
                 - scores(:obj:`torch.FloatTensor` of shape :obj:`(batch_size, num_cls)`):
                     Predicted scores of all classes for each query.
 
         Examples:
-            >>> from weathon.models.nlp import SbertForFaqQuestionAnswering
+            >>> from weathon.dl.models.nlp import SbertForFaqQuestionAnswering
             >>> model = SbertForFaqQuestionAnswering.from_pretrained(cache_path)
             >>> param = {
             >>>            'query_set': ['如何使用优惠券', '在哪里领券', '在哪里领券'],
             >>>            'support_set': [{
             >>>                    'text': '卖品代金券怎么用',
             >>>                    'label': '6527856'
             >>>               }, {
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/fill_mask.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/fill_mask.py`

 * *Files 2% similar despite different names*

```diff
@@ -17,18 +17,18 @@
 
 import torch
 import torch.nn as nn
 import torch.utils.checkpoint
 from torch.nn import CrossEntropyLoss
 from transformers.activations import ACT2FN
 
-from weathon.registry import MODELS
-from weathon.utils import logger as logging
-from weathon.utils.constants import Tasks, Models
-from weathon.utils.output import AttentionFillMaskModelOutput
+from weathon.dl.registry import MODELS
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants import Tasks, Models
+from weathon.dl.utils.output import AttentionFillMaskModelOutput
 from .backbone import SbertModel, SbertPreTrainedModel
 from .configuration import SbertConfig
 
 logger = logging.get_logger()
 
 
 class SbertPredictionHeadTransform(nn.Module):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/text_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/text_classification.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,18 +16,18 @@
 # limitations under the License.
 
 import torch
 import torch.nn as nn
 import torch.utils.checkpoint
 from torch.nn import BCEWithLogitsLoss, CrossEntropyLoss, MSELoss
 
-from weathon.registry import MODELS
-from weathon.utils import logger as logging
-from weathon.utils.constants import Tasks, Models
-from weathon.utils.output import AttentionTextClassificationModelOutput
+from weathon.dl.registry import MODELS
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants import Tasks, Models
+from weathon.dl.utils.output import AttentionTextClassificationModelOutput
 from .adv_utils import compute_adv_loss
 from .backbone import SbertModel, SbertPreTrainedModel
 from .configuration import SbertConfig
 
 logger = logging.get_logger()
 
 @MODELS.register_module(Tasks.text_classification, module_name=Models.structbert)
@@ -151,15 +151,15 @@
                 config.num_labels - 1]`. If :obj:`config.num_labels == 1` a regression loss is computed
                 (Mean-Square loss), If :obj:`config.num_labels > 1` a classification loss is computed (Cross-Entropy).
 
         Returns:
             Returns `modelscope.outputs.AttentionTextClassificationModelOutput`
 
         Examples:
-            >>> from weathon.base import BaseModel, BasePreprocessor
+            >>> from weathon.dl.base import BaseModel, BasePreprocessor
             >>> model = BaseModel.from_pretrained('damo/nlp_structbert_sentence-similarity_chinese-base')
             >>> preprocessor =BasePreprocessor.from_pretrained('damo/nlp_structbert_sentence-similarity_chinese-base')
             >>> # Call the model, return some tensors
             >>> print(model(**preprocessor(('这是个测试', '这也是个测试'))))
             >>> # Call the pipeline
             >>> from weathon.pipelines import pipeline
             >>> pipeline_ins = pipeline('text-classification', model=model, preprocessor=preprocessor)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/structbert/token_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/structbert/token_classification.py`

 * *Files 0% similar despite different names*

```diff
@@ -16,18 +16,18 @@
 # limitations under the License.
 
 import torch
 import torch.nn as nn
 import torch.utils.checkpoint
 from torch.nn import CrossEntropyLoss
 
-from weathon.registry import MODELS
-from weathon.utils import logger as logging
-from weathon.utils.constants import Tasks, Models
-from weathon.utils.output import AttentionTokenClassificationModelOutput
+from weathon.dl.registry import MODELS
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants import Tasks, Models
+from weathon.dl.utils.output import AttentionTokenClassificationModelOutput
 from .adv_utils import compute_adv_loss
 from .backbone import SbertModel, SbertPreTrainedModel
 from .configuration import SbertConfig
 
 logger = logging.get_logger()
 
 
@@ -166,15 +166,15 @@
                 - 1 for tokens that are **not masked**,
                 - 0 for tokens that are **masked**.
 
         Returns:
             Returns `modelscope.outputs.AttentionTokenClassificationModelOutput`
 
         Examples:
-            >>> from weathon.base import BaseModel,BasePreprocessor
+            >>> from weathon.dl.base import BaseModel,BasePreprocessor
             >>> model = BaseModel.from_pretrained('damo/nlp_structbert_word-segmentation_chinese-base')
             >>> preprocessor = BasePreprocessor.from_pretrained('damo/nlp_structbert_word-segmentation_chinese-base')
             >>> print(model(**preprocessor(('This is a test', 'This is also a test'))))
         """
         return_dict = return_dict if return_dict is not None else self.config.use_return_dict
         if not return_dict:
             logger.error('Return tuple in sbert is not supported now.')
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/unite/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/unite/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import UniTEConfig
     from .translation_evaluation import UniTEForTranslationEvaluation
 else:
     _import_structure = {
         'configuration': ['UniTEConfig'],
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/unite/translation_evaluation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/unite/translation_evaluation.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,21 +7,21 @@
 import torch.utils.checkpoint
 from torch.nn import (Dropout, Linear, Module, Parameter, Sequential)
 from torch.nn.functional import softmax
 from torch.nn.utils.rnn import pad_sequence
 from transformers import XLMRobertaConfig, XLMRobertaModel
 from transformers.activations import ACT2FN
 
-from weathon.base import TorchModel
-from weathon.utils.constants.metainfo import Models
-from weathon.registry import MODELS
-from weathon.models.nlp.backbone.unite import InputFormat
-from weathon.utils.output.nlp_outputs import TranslationEvaluationOutput
-from weathon.utils.constants import Tasks
-from weathon.utils.logger import get_logger
+from weathon.dl.base import TorchModel
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.backbone.unite import InputFormat
+from weathon.dl.utils.output.nlp_outputs import TranslationEvaluationOutput
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 __all__ = ['UniTEForTranslationEvaluation']
 
 
 def _layer_norm_all(tensor, mask_float):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/use/transformer.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/use/transformer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/use/user_satisfaction_estimation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/use/user_satisfaction_estimation.py`

 * *Files 3% similar despite different names*

```diff
@@ -4,20 +4,20 @@
 import numpy as np
 import torch
 import torch.nn as nn
 import torch.nn.functional as F
 from torch.nn.init import xavier_uniform_
 from transformers import BertModel
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.utils.output.nlp_outputs import DialogueUserSatisfactionEstimationModelOutput
-from weathon.utils.typing import Tensor
-from weathon.registry import MODELS
-from weathon.utils.constants import ModelFile, Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.utils.output.nlp_outputs import DialogueUserSatisfactionEstimationModelOutput
+from weathon.dl.utils.typing import Tensor
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import ModelFile, Tasks
 from .transformer import TransformerEncoder
 
 __all__ = ['UserSatisfactionEstimation']
 
 
 @MODELS.register_module(Tasks.text_classification, module_name=Models.use)
 class UserSatisfactionEstimation(TorchModel):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/veco/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import VecoConfig
     from .backbone import VecoModel
     from .text_classification import VecoForSequenceClassification
     from .token_classification import VecoForTokenClassification
     from .fill_mask import VecoForMaskedLM
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/veco/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/backbone.py`

 * *Files 4% similar despite different names*

```diff
@@ -14,20 +14,20 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """PyTorch Veco model. mainly copied from :module:`~transformers.modeling_xlm_roberta`"""
 
 from transformers import RobertaModel
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.output.nlp_outputs import AttentionBackboneModelOutput
-from weathon.utils import logger as logging
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.output.nlp_outputs import AttentionBackboneModelOutput
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants import Tasks
 from .configuration import VecoConfig
 
 logger = logging.get_logger()
 
 VECO_PRETRAINED_MODEL_ARCHIVE_LIST = []
 
 
@@ -61,15 +61,15 @@
 
     def forward(self, *args, **kwargs):
         """
         Returns:
             Returns `modelscope.outputs.AttentionBackboneModelOutputWithEmbedding`
 
         Examples:
-            >>> from weathon.models import Model
+            >>> from weathon.dl.models import Model
             >>> from weathon.preprocessors import Preprocessor
             >>> model = Model.from_pretrained('damo/nlp_veco_fill-mask-large', task='backbone')
             >>> preprocessor = Preprocessor.from_pretrained('damo/nlp_veco_fill-mask-large')
             >>> print(model(**preprocessor('这是个测试')))
 
         """
         kwargs['return_dict'] = True
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/veco/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/configuration.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 """Veco configuration, mainly copied from :class:`~transformers.configuration_xlm_roberta` """
 
 from transformers import RobertaConfig
 
-from weathon.utils import logger as logging
+from weathon.dl.utils import logger as logging
 
 logger = logging.get_logger()
 
 
 class VecoConfig(RobertaConfig):
     """
     This class overrides [`RobertaConfig`]. Please check the superclass for the appropriate
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/veco/fill_mask.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/fill_mask.py`

 * *Files 2% similar despite different names*

```diff
@@ -13,19 +13,19 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from transformers import RobertaForMaskedLM
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel, BaseModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.output.nlp_outputs import AttentionFillMaskModelOutput
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel, BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.output.nlp_outputs import AttentionFillMaskModelOutput
 from .configuration import VecoConfig
 
 
 @MODELS.register_module(Tasks.fill_mask, module_name=Models.veco)
 class VecoForMaskedLM(TorchModel, RobertaForMaskedLM):
     """Veco Model transformer with a masked language model head on top (a linear layer on top of the
     pooled output).
@@ -60,15 +60,15 @@
 
     def forward(self, *args, **kwargs):
         """
         Returns:
             Returns `modelscope.outputs.AttentionFillMaskModelOutput`
 
         Examples:
-            >>> from weathon.models import Model
+            >>> from weathon.dl.models import Model
             >>> from weathon.preprocessors import Preprocessor
             >>> model = Model.from_pretrained('damo/nlp_veco_fill-mask-large')
             >>> preprocessor = Preprocessor.from_pretrained('damo/nlp_veco_fill-mask-large')
             >>> # Call the model, return some tensors
             >>> print(model(**preprocessor('你师父差得动你，你师父可<mask>不动我。')))
             >>> # Call the pipeline
             >>> from weathon.pipelines import pipeline
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/veco/text_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/text_classification.py`

 * *Files 2% similar despite different names*

```diff
@@ -13,20 +13,20 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from transformers import RobertaForSequenceClassification
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel, BaseModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.nlp.utils import parse_labels_in_order
-from weathon.utils.output.nlp_outputs import AttentionTextClassificationModelOutput
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel, BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.nlp.utils import parse_labels_in_order
+from weathon.dl.utils.output.nlp_outputs import AttentionTextClassificationModelOutput
 from .configuration import VecoConfig
 
 
 @MODELS.register_module(Tasks.nli, module_name=Models.veco)
 @MODELS.register_module(
     Tasks.sentiment_classification, module_name=Models.veco)
 @MODELS.register_module(Tasks.sentence_similarity, module_name=Models.veco)
@@ -80,15 +80,15 @@
 
     def forward(self, *args, **kwargs):
         """
         Returns:
             Returns `modelscope.outputs.AttentionTextClassificationModelOutput`
 
         Examples:
-            >>> from weathon.base import BaseModel, BasePreprocessor
+            >>> from weathon.dl.base import BaseModel, BasePreprocessor
             >>> model = BaseModel.from_pretrained('damo/nlp_veco_fill-mask-large',
             >>>                               task='text-classification', num_labels=2)
             >>> preprocessor = BasePreprocessor.from_pretrained('damo/nlp_veco_fill-mask-large',
             >>>                                             label2id={'0': 0, '1': 1})
             >>> # Call the model, return some tensors
             >>> print(model(**preprocessor('这是个测试')))
             >>> # Call the pipeline, the result may be incorrect
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/veco/token_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/veco/token_classification.py`

 * *Files 6% similar despite different names*

```diff
@@ -14,20 +14,20 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 import torch
 from transformers import RobertaForTokenClassification
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel, BaseModel
-from weathon.registry import MODELS
-from weathon.utils.constants import Tasks
-from weathon.utils.nlp.utils import parse_labels_in_order
-from weathon.utils.output.nlp_outputs import AttentionTokenClassificationModelOutput
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel, BaseModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.nlp.utils import parse_labels_in_order
+from weathon.dl.utils.output.nlp_outputs import AttentionTokenClassificationModelOutput
 from .configuration import VecoConfig
 
 
 @MODELS.register_module(Tasks.token_classification, module_name=Models.veco)
 class VecoForTokenClassification(TorchModel, RobertaForTokenClassification):
     """Veco Model with a token classification head on top (a linear layer on top of the hidden-states output) e.g.
     for Named-Entity-Recognition (NER) tasks.
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/xlm_roberta/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/xlm_roberta/__init__.py`

 * *Files 18% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .configuration import XLMRobertaConfig
     from .backbone import XLMRobertaModel
 else:
     _import_structure = {
         'configuration': ['XLMRobertaConfig'],
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/xlm_roberta/backbone.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/xlm_roberta/backbone.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,21 +21,21 @@
 from torch import nn
 from transformers.activations import ACT2FN
 from transformers.modeling_utils import (PreTrainedModel,
                                          apply_chunking_to_forward,
                                          find_pruneable_heads_and_indices,
                                          prune_linear_layer)
 
-from weathon.utils.constants.metainfo import Models
-from weathon.base import TorchModel
-from weathon.registry import MODELS
-from weathon.utils.output.nlp_outputs import AttentionBackboneModelOutput
-from weathon.utils.constants import Tasks
-from weathon.utils.logger import get_logger
-from weathon.utils.nlp.utils import parse_labels_in_order
+from weathon.dl.utils.constants.metainfo import Models
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import MODELS
+from weathon.dl.utils.output.nlp_outputs import AttentionBackboneModelOutput
+from weathon.dl.utils.constants import Tasks
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.nlp.utils import parse_labels_in_order
 from .configuration import XLMRobertaConfig
 
 logger = get_logger()
 
 _CONFIG_FOR_DOC = 'XLMRobertaConfig'
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/backbone/xlm_roberta/configuration.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/backbone/xlm_roberta/configuration.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 """ XLM-RoBERTa configuration"""
 from collections import OrderedDict
 from typing import Mapping
 
 from transformers.configuration_utils import PretrainedConfig
 from transformers.onnx import OnnxConfig
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 class XLMRobertaConfig(PretrainedConfig):
     r"""
     This is the configuration class to store the configuration of a [`XLMRobertaModel`] or a [`TFXLMRobertaModel`]. It
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/heads/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/heads/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .text_classification_head import TextClassificationHead
     from .torch_pretrain_head import BertMLMHead, RobertaMLMHead
 else:
     _import_structure = {
         'text_classification_head': ['TextClassificationHead'],
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/heads/crf_head.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/heads/crf_head.py`

 * *Files 0% similar despite different names*

```diff
@@ -18,17 +18,17 @@
 
 import torch
 import torch.nn.functional as F
 from torch import nn
 from torch.nn import CrossEntropyLoss
 from transformers.activations import ACT2FN
 
-from weathon.base import TorchHead
-from weathon.registry import HEADS
-from weathon.utils.constants import Tasks, Heads
+from weathon.dl.base import TorchHead
+from weathon.dl.registry import HEADS
+from weathon.dl.utils.constants import Tasks, Heads
 
 
 @HEADS.register_module(Tasks.token_classification, module_name=Heads.lstm_crf)
 @HEADS.register_module(Tasks.named_entity_recognition, module_name=Heads.lstm_crf)
 @HEADS.register_module(Tasks.word_segmentation, module_name=Heads.lstm_crf)
 @HEADS.register_module(Tasks.part_of_speech, module_name=Heads.lstm_crf)
 class LSTMCRFHead(TorchHead):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/heads/fill_mask_head.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/heads/fill_mask_head.py`

 * *Files 1% similar despite different names*

```diff
@@ -18,17 +18,17 @@
 
 import torch
 import torch.nn.functional as F
 from torch import nn
 from torch.nn import CrossEntropyLoss
 from transformers.activations import ACT2FN, gelu
 
-from weathon.base import TorchHead
-from weathon.registry import HEADS
-from weathon.utils.constants import Tasks, Heads
+from weathon.dl.base import TorchHead
+from weathon.dl.registry import HEADS
+from weathon.dl.utils.constants import Tasks, Heads
 
 
 @HEADS.register_module(Tasks.fill_mask, module_name=Heads.bert_mlm)
 @HEADS.register_module(Tasks.fill_mask, module_name=Heads.fill_mask)
 class BertFillMaskHead(TorchHead):
 
     def __init__(self,
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/heads/infromation_extraction_head.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/heads/infromation_extraction_head.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from typing import Dict
 
 import torch
 from torch import nn
 
-from weathon.base import TorchHead
-from weathon.registry import HEADS
-from weathon.utils.constants import Tasks, Heads
+from weathon.dl.base import TorchHead
+from weathon.dl.registry import HEADS
+from weathon.dl.utils.constants import Tasks, Heads
 
 
 
 @HEADS.register_module(Tasks.information_extraction, module_name=Heads.information_extraction)
 @HEADS.register_module(Tasks.relation_extraction, module_name=Heads.information_extraction)
 class InformationExtractionHead(TorchHead):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/heads/text_classification_head.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/heads/text_classification_head.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from typing import Dict
 
 import torch
 import torch.nn.functional as F
 from torch import nn
 
-from weathon.base import TorchHead
-from weathon.registry import HEADS
-from weathon.utils.constants import Tasks, Heads
+from weathon.dl.base import TorchHead
+from weathon.dl.registry import HEADS
+from weathon.dl.utils.constants import Tasks, Heads
 
 
 @HEADS.register_module(Tasks.text_classification, module_name=Heads.text_classification)
 @HEADS.register_module(Tasks.sentence_similarity, module_name=Heads.text_classification)
 @HEADS.register_module(Tasks.nli, module_name=Heads.text_classification)
 @HEADS.register_module(Tasks.sentiment_classification, module_name=Heads.text_classification)
 class TextClassificationHead(TorchHead):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/heads/text_generation_head.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/heads/text_generation_head.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from typing import Dict
 
 import torch
 import torch.nn.functional as F
 from torch import nn
 
-from weathon.base import TorchHead
-from weathon.registry import HEADS
-from weathon.utils.constants import Tasks, Heads
+from weathon.dl.base import TorchHead
+from weathon.dl.registry import HEADS
+from weathon.dl.utils.constants import Tasks, Heads
 
 
 
 @HEADS.register_module(Tasks.text_generation, module_name=Heads.text_generation)
 class TextGenerationHead(TorchHead):
 
     def __init__(self, **kwargs):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/heads/text_ranking_head.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/heads/text_ranking_head.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from typing import Dict
 
 import torch
 from torch import nn
 
-from weathon.base import TorchHead
-from weathon.registry import HEADS
-from weathon.utils.constants import Tasks, Heads
+from weathon.dl.base import TorchHead
+from weathon.dl.registry import HEADS
+from weathon.dl.utils.constants import Tasks, Heads
 
 
 @HEADS.register_module(Tasks.text_ranking, module_name=Heads.text_ranking)
 class TextRankingHead(TorchHead):
 
     def __init__(self,
                  hidden_size=768,
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/heads/token_classification_head.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/heads/token_classification_head.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from typing import Dict
 
 import torch
 from torch import nn
 from torch.nn import CrossEntropyLoss
 
-from weathon.base import TorchHead
-from weathon.registry import HEADS
-from weathon.utils.constants import Tasks, Heads
+from weathon.dl.base import TorchHead
+from weathon.dl.registry import HEADS
+from weathon.dl.utils.constants import Tasks, Heads
 
 
 @HEADS.register_module(Tasks.token_classification, module_name=Heads.token_classification)
 @HEADS.register_module(Tasks.named_entity_recognition, module_name=Heads.token_classification)
 @HEADS.register_module(Tasks.part_of_speech, module_name=Heads.token_classification)
 class TokenClassificationHead(TorchHead):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/heads/torch_pretrain_head.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/heads/torch_pretrain_head.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from typing import Dict
 
 import torch
 from transformers.models.bert.modeling_bert import BertOnlyMLMHead
 from transformers.models.roberta.modeling_roberta import RobertaLMHead
 
-from weathon.base import TorchHead
-from weathon.registry import HEADS
-from weathon.utils.constants import Tasks, Heads
+from weathon.dl.base import TorchHead
+from weathon.dl.registry import HEADS
+from weathon.dl.utils.constants import Tasks, Heads
 
 
 @HEADS.register_module(Tasks.fill_mask, module_name=Heads.bert_mlm)
 class BertMLMHead(BertOnlyMLMHead, TorchHead):
 
     def compute_loss(self, outputs: Dict[str, torch.Tensor], labels) -> Dict[str, torch.Tensor]:
         raise NotImplementedError()
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/task_models/__init__.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/task_models/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .information_extraction import ModelForInformationExtraction
     from .feature_extraction import ModelForFeatureExtraction
     from .fill_mask import ModelForFillMask
     from .text_classification import ModelForTextClassification
     from .task_model import SingleBackboneTaskModelBase
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/task_models/feature_extraction.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/task_models/feature_extraction.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from typing import Any, Dict
 
 import numpy as np
 
-from weathon.utils.constants.metainfo import TaskModels
-from weathon.registry import MODELS
-from weathon.models.nlp.task_models.task_model import EncoderModel
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import TaskModels
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.task_models.task_model import EncoderModel
+from weathon.dl.utils.constants import Tasks
 
 __all__ = ['ModelForFeatureExtraction']
 
 
 @MODELS.register_module(
     Tasks.feature_extraction, module_name=TaskModels.feature_extraction)
 class ModelForFeatureExtraction(EncoderModel):
@@ -79,15 +79,15 @@
             config.num_labels - 1]`. If :obj:`config.num_labels == 1` a regression loss is computed (Mean-Square loss),
             If :obj:`config.num_labels > 1` a classification loss is computed (Cross-Entropy).
 
         Returns:
             Returns `modelscope.outputs.AttentionTextClassificationModelOutput`
 
         Examples:
-            >>> from weathon.base import BaseModel,BasePreprocessor
+            >>> from weathon.dl.base import BaseModel,BasePreprocessor
             >>> model = BaseModel.from_pretrained('damo/nlp_structbert_sentence-similarity_chinese-base')
             >>> preprocessor = BasePreprocessor.from_pretrained('damo/nlp_structbert_sentence-similarity_chinese-base')
             >>> print(model(**preprocessor(('This is a test', 'This is also a test'))))
         """
 
         # backbone do not need labels, only head need for loss compute
         feature = self.extract_feature(
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/task_models/fill_mask.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/task_models/fill_mask.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from typing import Any, Dict
 
 import numpy as np
 import torch
 
-from weathon.utils.constants.metainfo import Heads, TaskModels
-from weathon.registry import MODELS
-from weathon.models.nlp.task_models.task_model import EncoderModel
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Heads, TaskModels
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.task_models.task_model import EncoderModel
+from weathon.dl.utils.constants import Tasks
 
 __all__ = ['ModelForFillMask']
 
 
 @MODELS.register_module(Tasks.fill_mask, module_name=TaskModels.fill_mask)
 class ModelForFillMask(EncoderModel):
     task = Tasks.fill_mask
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/task_models/information_extraction.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/task_models/information_extraction.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from typing import Any, Dict
 
 import numpy as np
 
-from weathon.utils.constants.metainfo import Heads, TaskModels
-from weathon.registry import MODELS
-from weathon.models.nlp.task_models.task_model import EncoderModel
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants.metainfo import Heads, TaskModels
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.task_models.task_model import EncoderModel
+from weathon.dl.utils.constants import Tasks
 
 __all__ = ['ModelForInformationExtraction']
 
 
 @MODELS.register_module(
     Tasks.information_extraction,
     module_name=TaskModels.information_extraction)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/task_models/task_model.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/task_models/task_model.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,22 +3,22 @@
 from abc import ABC
 from collections import OrderedDict
 from typing import Any, Dict, Optional
 
 import torch
 from torch import nn
 
-from weathon.base import TorchModel
-from weathon.registry import build_backbone, build_head
-from weathon.utils.checkpoint import load_task_model_checkpoint
-from weathon.utils.config.config import Config, ConfigDict
-from weathon.utils.constants import ModelFile, DEFAULT_MODEL_REVISION
-from weathon.utils.constants.output_constant import OutputKeys
-from weathon.utils.fileio.file_utils import func_receive_dict_inputs
-from weathon.utils.logger import get_logger
+from weathon.dl.base import TorchModel
+from weathon.dl.registry import build_backbone, build_head
+from weathon.dl.utils.checkpoint import load_task_model_checkpoint
+from weathon.dl.utils.config.config import Config, ConfigDict
+from weathon.dl.utils.constants import ModelFile, DEFAULT_MODEL_REVISION
+from weathon.dl.utils.constants.output_constant import OutputKeys
+from weathon.dl.utils.fileio.file_utils import func_receive_dict_inputs
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 __all__ = ['EncoderModel', 'SingleBackboneTaskModelBase']
 
 
 def _repr(modules, depth=1):
@@ -649,15 +649,15 @@
         **kwargs:
             Accept additional kwargs in the children class
 
         Returns:
             Returns `modelscope.outputs.ModelOutput`
 
         Examples:
-            >>> from weathon.base import BaseModel,BasePreprocessor
+            >>> from weathon.dl.base import BaseModel,BasePreprocessor
             >>> model = BaseModel.from_pretrained('damo/nlp_structbert_sentence-similarity_chinese-base')
             >>> preprocessor = BasePreprocessor.from_pretrained('damo/nlp_structbert_sentence-similarity_chinese-base')
             >>> print(model(**preprocessor(('This is a test', 'This is also a test'))))
         """
 
         if OutputKeys.LABEL in kwargs and labels is None:
             labels = kwargs.pop(OutputKeys.LABEL, None)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/task_models/text_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/task_models/text_classification.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
-from weathon.utils.constants import Heads, TaskModels
-from weathon.registry import MODELS
-from weathon.models.nlp.task_models.task_model import EncoderModel
-from weathon.utils.constants import Tasks, Datasets
+from weathon.dl.utils.constants import Heads, TaskModels
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.task_models.task_model import EncoderModel
+from weathon.dl.utils.constants import Tasks, Datasets
 
 __all__ = ['ModelForTextClassification']
 
 
 
 @MODELS.register_module(Tasks.text_classification, module_name=Datasets.jd_sentiment_text_classification)
 @MODELS.register_module(Tasks.text_classification, module_name=TaskModels.text_classification)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/task_models/text_generation.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/task_models/text_generation.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 from typing import Dict
 
 import numpy as np
 import torch
 from transformers.modeling_utils import PreTrainedModel
 
-from weathon.utils.constants.metainfo import TaskModels
-from weathon.registry import MODELS
-from weathon.models.nlp.task_models.task_model import \
+from weathon.dl.utils.constants.metainfo import TaskModels
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.task_models.task_model import \
     SingleBackboneTaskModelBase
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants import Tasks
 
 __all__ = ['ModelForTextGeneration']
 
-from weathon.utils.constants.output_constant import OutputKeys
-from weathon.utils.output.nlp_outputs import TextGenerationModelOutput, TokenGeneratorOutput
+from weathon.dl.utils.constants.output_constant import OutputKeys
+from weathon.dl.utils.output.nlp_outputs import TextGenerationModelOutput, TokenGeneratorOutput
 
 
 @MODELS.register_module(
     Tasks.text_generation, module_name=TaskModels.text_generation)
 class ModelForTextGeneration(SingleBackboneTaskModelBase, PreTrainedModel):
 
     def __init__(self, model_dir: str, *args, **kwargs):
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/task_models/text_ranking.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/task_models/text_ranking.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from typing import Any, Dict
 
 import numpy as np
 
-from weathon.registry import MODELS
-from weathon.models.nlp.task_models.task_model import EncoderModel
-from weathon.utils.constants import Tasks, TaskModels, Heads
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.task_models.task_model import EncoderModel
+from weathon.dl.utils.constants import Tasks, TaskModels, Heads
 
 __all__ = ['ModelForTextRanking']
 
 
 
 @MODELS.register_module(
     Tasks.text_ranking, module_name=TaskModels.text_ranking)
```

### Comparing `weathon-0.0.0.17/weathon/models/nlp/task_models/token_classification.py` & `weathon-0.0.0.18/weathon/dl/models/nlp/task_models/token_classification.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from typing import Any, Dict
 
 import torch
 
-from weathon.registry import MODELS
-from weathon.models.nlp.task_models.task_model import EncoderModel
-from weathon.utils.constants import Tasks, TaskModels, Models, Heads
+from weathon.dl.registry import MODELS
+from weathon.dl.models.nlp.task_models.task_model import EncoderModel
+from weathon.dl.utils.constants import Tasks, TaskModels, Models, Heads
 
 __all__ = ['ModelForTokenClassification', 'ModelForTokenClassificationWithCRF']
 
 
 
 @MODELS.register_module(Tasks.token_classification, module_name=TaskModels.token_classification)
 @MODELS.register_module(Tasks.part_of_speech, module_name=TaskModels.token_classification)
```

### Comparing `weathon-0.0.0.17/weathon/optimizer/__init__.py` & `weathon-0.0.0.18/weathon/dl/optimizer/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 from .child_tuning_adamw_optimizer import ChildTuningAdamW
 
 if TYPE_CHECKING:
     from .warmup import BaseWarmup, ConstantWarmup, ExponentialWarmup, LinearWarmup
 
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/optimizer/child_tuning_adamw_optimizer.py` & `weathon-0.0.0.18/weathon/dl/optimizer/child_tuning_adamw_optimizer.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,17 +16,17 @@
 from typing import Callable, Iterable, Tuple
 
 import numpy as np
 import torch
 from torch.distributions.bernoulli import Bernoulli
 from torch.optim import Optimizer
 
-from weathon.registry import OPTIMIZERS
-from weathon.registry.registry import default_group
-from weathon.utils.logger import get_logger
+from weathon.dl.registry import OPTIMIZERS
+from weathon.dl.registry.registry import default_group
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 __all__ = ['calculate_fisher', 'ChildTuningAdamW']
 
 
 def calculate_fisher(model: torch.nn.Module,
```

### Comparing `weathon-0.0.0.17/weathon/optimizer/warmup.py` & `weathon-0.0.0.18/weathon/dl/optimizer/warmup.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-from weathon.base import BaseWarmup
-from weathon.registry import LR_SCHEDULER
-from weathon.utils.constants import LR_Schedulers
+from weathon.dl.base import BaseWarmup
+from weathon.dl.registry import LR_SCHEDULER
+from weathon.dl.utils.constants import LR_Schedulers
 
 @LR_SCHEDULER.register_module(module_name=LR_Schedulers.ConstantWarmup)
 class ConstantWarmup(BaseWarmup):
     """Linear warmup scheduler.
 
     Args:
         base_scheduler (torch.optim._LRScheduler): an instance of torch.optim._LRScheduler type
```

### Comparing `weathon-0.0.0.17/weathon/processors/__init__.py` & `weathon-0.0.0.18/weathon/dl/processors/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .nlp.text_classification.preprocessor import JDTextClassificationPreprocessor
     from .cv.ocr.preprocessor import Icdar2015Preprocessor
 
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/processors/cv/__init__.py` & `weathon-0.0.0.18/weathon/dl/processors/cv/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .video_super_resolution import (VideoReader)
     from .video_stabilization import (stabilization_preprocessor)
     from .mmcls_preprocessor import ImageClassificationMmcvPreprocessor
 
     from .image_quality_assessment_mos import ImageQualityAssessmentMosPreprocessor
```

### Comparing `weathon-0.0.0.17/weathon/processors/cv/ocr/postprocessors.py` & `weathon-0.0.0.18/weathon/dl/processors/cv/ocr/postprocessors.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import numpy as np
 import pyclipper
 from shapely.geometry import Polygon
 from pyclipper import PyclipperOffset
 import math
 import operator
 from functools import reduce
-from weathon.registry import POSTPROCESSORS
+from weathon.dl.registry import POSTPROCESSORS
 
 
 def clockwise_sort_points(_point_coordinates):
     """
         以左上角为起点的顺时针排序
         原理就是将笛卡尔坐标转换为极坐标，然后对极坐标的φ进行排序
     Args:
```

### Comparing `weathon-0.0.0.17/weathon/processors/cv/ocr/preprocessor.py` & `weathon-0.0.0.18/weathon/dl/processors/cv/ocr/preprocessor.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 from typing import Dict, Any
 
 from torchvision import transforms
 
-from weathon.base import BaseProcessor
-from weathon.registry import PREPROCESSORS
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Tasks, Datasets, ModeKeys
-from weathon.utils.processor.preprocessors.cv.ocr.process_module.augment import ResizeShortSize
-from weathon.utils.processor.preprocessors.cv.ocr.process_module.iaa_augment import IaaAugment
-from weathon.utils.processor.preprocessors.cv.ocr.process_module.make_border_map import MakeBorderMap
-from weathon.utils.processor.preprocessors.cv.ocr.process_module.make_shrink_map import MakeShrinkMap
-from weathon.utils.processor.preprocessors.cv.ocr.process_module.random_crop_data import EastRandomCropData
+from weathon.dl.base import BaseProcessor
+from weathon.dl.registry import PREPROCESSORS
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Tasks, Datasets, ModeKeys
+from weathon.dl.utils.processor.preprocessors.cv.ocr import ResizeShortSize
+from weathon.dl.utils.processor.preprocessors.cv.ocr import IaaAugment
+from weathon.dl.utils.processor.preprocessors.cv.ocr import MakeBorderMap
+from weathon.dl.utils.processor.preprocessors.cv.ocr import MakeShrinkMap
+from weathon.dl.utils.processor.preprocessors.cv.ocr import EastRandomCropData
 
 
 @PREPROCESSORS.register_module(group_key=Tasks.ocr_detection, module_name=Datasets.icdar2015_ocr_detection)
 class Icdar2015Preprocessor(BaseProcessor):
 
     def __init__(self, preprocessor_cfg: Config = None, *args, **kwargs):
         preprocessor_cfg = preprocessor_cfg if preprocessor_cfg else dict()
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/__init__.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .word_alignment_preprocessor import WordAlignmentPreprocessor
     from .text_error_correction import TextErrorCorrectionPreprocessor
     from .text_generation_preprocessor import TextGenerationJiebaPreprocessor
     from .bert_seq_cls_tokenizer import Tokenize
     from .document_segmentation_preprocessor import DocumentSegmentationTransformersPreprocessor
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/__init__.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .data_loader import DataLoader
     from .dialog_intent_prediction_preprocessor import \
         DialogIntentPredictionPreprocessor
     from .dialog_modeling_preprocessor import DialogModelingPreprocessor
     from .dialog_state_tracking_preprocessor import DialogStateTrackingPreprocessor
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/args.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/args.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/batch.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/batch.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/data_loader.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/data_loader.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/dialog_intent_prediction_preprocessor.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/dialog_intent_prediction_preprocessor.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 import os
 from typing import Any, Dict
 
 import json
 
-from weathon.utils.constants.metainfo import Preprocessors
-from weathon.base import BasePreprocessor
-from weathon.registry import PREPROCESSORS
+from weathon.dl.utils.constants.metainfo import Preprocessors
+from weathon.dl.base import BasePreprocessor
+from weathon.dl.registry import PREPROCESSORS
 from weathon.preprocessors.nlp import IntentBPETextField
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Fields, ModelFile
-from weathon.utils.type_assert import type_assert
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Fields, ModelFile
+from weathon.dl.utils.type_assert import type_assert
 
 __all__ = ['DialogIntentPredictionPreprocessor']
 
 
 @PREPROCESSORS.register_module(
     Fields.nlp, module_name=Preprocessors.dialog_intent_preprocessor)
 class DialogIntentPredictionPreprocessor(BasePreprocessor):
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/dialog_modeling_preprocessor.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/dialog_modeling_preprocessor.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 import os
 from typing import Any, Dict
 
-from weathon.utils.constants.metainfo import Preprocessors
-from weathon.base import BasePreprocessor
-from weathon.registry import PREPROCESSORS
+from weathon.dl.utils.constants.metainfo import Preprocessors
+from weathon.dl.base import BasePreprocessor
+from weathon.dl.registry import PREPROCESSORS
 from weathon.preprocessors.nlp import MultiWOZBPETextField
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Fields, ModelFile
-from weathon.utils.type_assert import type_assert
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Fields, ModelFile
+from weathon.dl.utils.type_assert import type_assert
 
 __all__ = ['DialogModelingPreprocessor']
 
 
 @PREPROCESSORS.register_module(
     Fields.nlp, module_name=Preprocessors.dialog_modeling_preprocessor)
 class DialogModelingPreprocessor(BasePreprocessor):
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/dialog_state_tracking_preprocessor.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/dialog_state_tracking_preprocessor.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from typing import Any, Dict
 
-from weathon.utils.constants.metainfo import Preprocessors
-from weathon.base import BasePreprocessor
-from weathon.registry import PREPROCESSORS
-from weathon.utils.constants import Fields
-from weathon.utils.type_assert import type_assert
+from weathon.dl.utils.constants.metainfo import Preprocessors
+from weathon.dl.base import BasePreprocessor
+from weathon.dl.registry import PREPROCESSORS
+from weathon.dl.utils.constants import Fields
+from weathon.dl.utils.type_assert import type_assert
 from .dst_processors import convert_examples_to_features, multiwoz22Processor
 
 __all__ = ['DialogStateTrackingPreprocessor']
 
 
 @PREPROCESSORS.register_module(
     Fields.nlp, module_name=Preprocessors.dialog_state_tracking_preprocessor)
@@ -18,15 +18,15 @@
         """preprocess the data
 
         Args:
             model_dir (str): model path
         """
         super().__init__(*args, **kwargs)
 
-        from weathon.models.nlp.space import SpaceConfig, SpaceTokenizer
+        from weathon.dl.models.nlp.space import SpaceConfig, SpaceTokenizer
         self.model_dir: str = model_dir
         self.config = SpaceConfig.from_pretrained(self.model_dir)
         self.tokenizer = SpaceTokenizer.from_pretrained(self.model_dir)
         self.processor = multiwoz22Processor()
 
     @type_assert(object, dict)
     def __call__(self, data: Dict[str, Any]) -> Dict[str, Any]:
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/dst_processors.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/dst_processors.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/fields/__init__.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/fields/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .gen_field import MultiWOZBPETextField
     from .intent_field import IntentBPETextField
 else:
     _import_structure = {
         'gen_field': ['MultiWOZBPETextField'],
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/fields/gen_field.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/fields/gen_field.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,19 +4,19 @@
 from collections import OrderedDict
 from itertools import chain
 
 import json
 import numpy as np
 
 from weathon.preprocessors.nlp.space.tokenizer import Tokenizer
-from weathon.utils.constants import ModelFile
-from weathon.utils.logger import get_logger
-from weathon.utils.nlp.space import ontology, utils
-from weathon.utils.nlp.space.db_ops import MultiWozDB
-from weathon.utils.nlp.space.utils import list2np
+from weathon.dl.utils.constants import ModelFile
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.nlp.space import ontology, utils
+from weathon.dl.utils.nlp.space.db_ops import MultiWozDB
+from weathon.dl.utils.nlp.space.utils import list2np
 
 logger = get_logger()
 
 
 class BPETextField(object):
 
     pad_token = '[PAD]'
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/fields/intent_field.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/fields/intent_field.py`

 * *Files 0% similar despite different names*

```diff
@@ -8,18 +8,18 @@
 from itertools import chain
 
 import json
 import numpy as np
 from tqdm import tqdm
 
 from weathon.preprocessors.nlp.space.tokenizer import Tokenizer
-from weathon.utils.constants import ModelFile
-from weathon.utils.nlp.space import ontology
-from weathon.utils.nlp.space.scores import hierarchical_set_score
-from weathon.utils.nlp.space.utils import list2np
+from weathon.dl.utils.constants import ModelFile
+from weathon.dl.utils.nlp.space import ontology
+from weathon.dl.utils.nlp.space.scores import hierarchical_set_score
+from weathon.dl.utils.nlp.space.utils import list2np
 
 
 class BPETextField(object):
 
     pad_token = '[PAD]'
     bos_token = '[BOS]'
     eos_token = '[EOS]'
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/lazy_dataset.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/lazy_dataset.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/preprocess.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/preprocess.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/sampler.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/sampler.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/tensorlistdataset.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/tensorlistdataset.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space/tokenizer.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space/tokenizer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/__init__.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .table_question_answering_preprocessor import TableQuestionAnsweringPreprocessor
     from .fields import MultiWOZBPETextField, IntentBPETextField
 
 else:
     _import_structure = {
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/fields/database.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/fields/database.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/fields/schema_link.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/fields/schema_link.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/fields/struct.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/fields/struct.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_cn/table_question_answering_preprocessor.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_cn/table_question_answering_preprocessor.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 import os
 from typing import Any, Dict
 
 import torch
 from transformers import BertTokenizer
 
-from weathon.utils.constants.metainfo import Preprocessors
-from weathon.base import BasePreprocessor
-from weathon.registry import PREPROCESSORS
+from weathon.dl.utils.constants.metainfo import Preprocessors
+from weathon.dl.base import BasePreprocessor
+from weathon.dl.registry import PREPROCESSORS
 from weathon.preprocessors.nlp.space_T_cn.fields.database import Database
 from weathon.preprocessors.nlp.space_T_cn.fields.schema_link import \
     SchemaLinker
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Fields, ModelFile
-from weathon.utils.type_assert import type_assert
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Fields, ModelFile
+from weathon.dl.utils.type_assert import type_assert
 
 __all__ = ['TableQuestionAnsweringPreprocessor']
 
 
 @PREPROCESSORS.register_module(
     Fields.nlp,
     module_name=Preprocessors.table_question_answering_preprocessor)
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_en/__init__.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .conversational_text_to_sql_preprocessor import \
         ConversationalTextToSqlPreprocessor
     from .fields import (get_label, SubPreprocessor, preprocess_dataset,
                          process_dataset)
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_en/conversational_text_to_sql_preprocessor.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/conversational_text_to_sql_preprocessor.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,25 +4,25 @@
 import json
 import torch
 from text2sql_lgesql.preprocess.graph_utils import GraphProcessor
 from text2sql_lgesql.preprocess.process_graphs import process_dataset_graph
 from text2sql_lgesql.utils.batch import Batch
 from text2sql_lgesql.utils.example import Example
 
-from weathon.utils.constants.metainfo import Preprocessors
-from weathon.base import BasePreprocessor
-from weathon.registry import PREPROCESSORS
+from weathon.dl.utils.constants.metainfo import Preprocessors
+from weathon.dl.base import BasePreprocessor
+from weathon.dl.registry import PREPROCESSORS
 from weathon.preprocessors.nlp.space_T_en.fields import SubPreprocessor
 from weathon.preprocessors.nlp.space_T_en.fields.preprocess_dataset import \
     preprocess_dataset
 from weathon.preprocessors.nlp.space_T_en.fields.process_dataset import (
     process_dataset, process_tables)
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Fields, ModelFile
-from weathon.utils.type_assert import type_assert
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Fields, ModelFile
+from weathon.dl.utils.type_assert import type_assert
 
 __all__ = ['ConversationalTextToSqlPreprocessor']
 
 
 @PREPROCESSORS.register_module(
     Fields.nlp, module_name=Preprocessors.conversational_text_to_sql)
 class ConversationalTextToSqlPreprocessor(BasePreprocessor):
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/__init__.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/__init__.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .common_utils import SubPreprocessor
     from .parse import get_label
     from .preprocess_dataset import \
         preprocess_dataset
     from .process_dataset import \
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/common_utils.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/common_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 import sqlite3
 from itertools import combinations, product
 
 import nltk
 import numpy as np
 from text2sql_lgesql.utils.constants import MAX_RELATIVE_DIST
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 mwtokenizer = nltk.MWETokenizer(separator='')
 mwtokenizer.add_mwe(('[', 'CLS', ']'))
 logger = get_logger()
 
 
 def is_number(s):
```

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/parse.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/parse.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/preprocess_dataset.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/preprocess_dataset.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/space_T_en/fields/process_dataset.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/space_T_en/fields/process_dataset.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/processors/nlp/text_classification/preprocessor.py` & `weathon-0.0.0.18/weathon/dl/processors/nlp/text_classification/preprocessor.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 from typing import Any, Dict, List, Tuple, Union
 
 import numpy as np
 
-from weathon.base import BaseProcessor
-from weathon.registry import PREPROCESSORS
-from weathon.utils.config.config import Config
-from weathon.utils.logger import get_logger
-from weathon.utils.constants import ModeKeys, Fields, Tasks, Datasets, Preprocessors
-from weathon.utils.pretrained.utils import get_model_type
-from weathon.utils.processor.preprocessors.preprocessor_utils import parse_text_and_label, labels_to_id
-from weathon.utils.processor.preprocessors.transformers_tokenizer import NLPTokenizer
+from weathon.dl.base import BaseProcessor
+from weathon.dl.registry import PREPROCESSORS
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.constants import ModeKeys, Fields, Tasks, Datasets, Preprocessors
+from weathon.dl.utils.pretrained.utils import get_model_type
+from weathon.dl.utils.processor.preprocessors.preprocessor_utils import parse_text_and_label, labels_to_id
+from weathon.dl.utils.processor.preprocessors.transformers_tokenizer import NLPTokenizer
 
 logger = get_logger()
 
 
 class TextClassificationPreprocessorBase(BaseProcessor):
 
     def __init__(self, model_dir=None, first_sequence: str = None, second_sequence: str = None, label: str = 'label',
```

### Comparing `weathon-0.0.0.17/weathon/registry/__init__.py` & `weathon-0.0.0.18/weathon/dl/registry/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,12 +1,12 @@
-from weathon.registry.dataset import build_custom_dataset, CUSTOM_DATASETS
-from weathon.registry.exporter import build_exporter, EXPORTERS
-from weathon.registry.metric import build_metric, METRICS
-from weathon.registry.model import build_backbone, build_head, build_model, MODELS, HEADS, BACKBONES
-from weathon.registry.optimizer import build_optimizer, OPTIMIZERS
-from weathon.registry.processor import PREPROCESSORS,POSTPROCESSORS, build_preprocessor, build_postprocessor
-from weathon.registry.trainer import build_trainer, TRAINERS
-from weathon.registry.hook import build_hook, HOOKS
-from weathon.registry.lr_scheduler import build_lr_scheduler, LR_SCHEDULER
-from weathon.registry.pipeline import build_pipeline, PIPELINES
-from weathon.registry.parallel import build_parallel, PARALLEL
-from weathon.registry.loss import build_loss, LOSS
+from .dataset import build_custom_dataset, CUSTOM_DATASETS
+from .exporter import build_exporter, EXPORTERS
+from .metric import build_metric, METRICS
+from .model import build_backbone, build_head, build_model, MODELS, HEADS, BACKBONES
+from .optimizer import build_optimizer, OPTIMIZERS
+from .trainer import build_trainer, TRAINERS
+from .hook import build_hook, HOOKS
+from .lr_scheduler import build_lr_scheduler, LR_SCHEDULER
+from .pipeline import build_pipeline, PIPELINES
+from .parallel import build_parallel, PARALLEL
+from .loss import build_loss, LOSS
+from .processor import build_preprocessor,build_postprocessor, POSTPROCESSORS,PREPROCESSORS
```

### Comparing `weathon-0.0.0.17/weathon/registry/dataset.py` & `weathon-0.0.0.18/weathon/dl/registry/dataset.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-from weathon.utils.config.config import ConfigDict
-from weathon.registry.registry import build_from_cfg,Registry
+from weathon.dl.utils.config.config import ConfigDict
+from weathon.dl.registry.registry import build_from_cfg,Registry
 
 
 CUSTOM_DATASETS = Registry('custom_datasets')
 
 
 def build_custom_dataset(cfg: ConfigDict,task_name: str, default_args: dict = None):
     """
```

### Comparing `weathon-0.0.0.17/weathon/registry/exporter.py` & `weathon-0.0.0.18/weathon/dl/registry/exporter.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-from weathon.registry.registry import build_from_cfg,Registry
-from weathon.utils.config.config import ConfigDict
+from weathon.dl.registry.registry import build_from_cfg,Registry
+from weathon.dl.utils.config.config import ConfigDict
 
 
 EXPORTERS = Registry('exporters')
 
 
 def build_exporter(cfg: ConfigDict,task_name: str = None,default_args: dict = None):
     """ build exporter by the given model config dict
```

### Comparing `weathon-0.0.0.17/weathon/registry/lr_scheduler.py` & `weathon-0.0.0.18/weathon/dl/registry/lr_scheduler.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import inspect
 
 import torch
 from packaging import version
 
-from weathon.utils.config.config import ConfigDict
-from weathon.registry.registry import Registry, build_from_cfg, default_group
+from weathon.dl.utils.config.config import ConfigDict
+from weathon.dl.registry.registry import Registry, build_from_cfg, default_group
 
 LR_SCHEDULER = Registry('lr_scheduler')
 
 
 def build_lr_scheduler(cfg: ConfigDict, task_name: str = default_group, default_args: dict = None):
     """ build lr scheduler from given lr scheduler config dict
```

### Comparing `weathon-0.0.0.17/weathon/registry/metric.py` & `weathon-0.0.0.18/weathon/dl/registry/metric.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from typing import Union, Dict, Mapping
 
-from weathon.utils.config.config import ConfigDict
-from weathon.registry.registry import Registry, default_group, build_from_cfg
+from weathon.dl.utils.config.config import ConfigDict
+from weathon.dl.registry.registry import Registry, default_group, build_from_cfg
 
 METRICS = Registry('metrics')
 
 
 def build_metric(metric_cfg: Union[str, Dict], task_name: str = default_group, default_args: dict = None):
     """ Build metric given metric_name and field.
```

### Comparing `weathon-0.0.0.17/weathon/registry/model.py` & `weathon-0.0.0.18/weathon/dl/registry/model.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,23 +1,23 @@
-from weathon.registry.registry import Registry, build_from_cfg
-from weathon.utils.constants import Tasks, Models
-from weathon.utils.config.config import ConfigDict
-from weathon.utils.logger import get_logger
-from weathon.utils.task_utils import get_task_by_subtask_name
+from weathon.dl.registry.registry import Registry, build_from_cfg
+from weathon.dl.utils.constants import Tasks, Models
+from weathon.dl.utils.config.config import ConfigDict
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.task_utils import get_task_by_subtask_name
 
 logger = get_logger()
 
 MODELS = Registry('models')
 HEADS = Registry('heads')
 BACKBONES = MODELS
 
 
 def register_models():
-    from weathon.utils.ast_utils import INDEX_KEY
-    from weathon.utils.import_utils import LazyImportModule
+    from weathon.dl.utils.ast_utils import INDEX_KEY
+    from weathon.dl.utils.import_utils import LazyImportModule
     modules = LazyImportModule.AST_INDEX[INDEX_KEY]
     for module_index in list(modules.keys()):
         if module_index[1] == Tasks.backbone and module_index[0] == 'BACKBONES':
             modules[(MODELS.name.upper(), module_index[1], module_index[2])] = modules[module_index]
 
 
 def build_model(cfg: ConfigDict, task_name: str = None, default_args: dict = None):
```

### Comparing `weathon-0.0.0.17/weathon/registry/optimizer.py` & `weathon-0.0.0.18/weathon/dl/registry/optimizer.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import inspect
 from typing import Union, Iterable
 
 import torch
 
-from weathon.utils.config.config import ConfigDict
-from weathon.registry.registry import Registry, default_group, build_from_cfg
+from weathon.dl.utils.config.config import ConfigDict
+from weathon.dl.registry.registry import Registry, default_group, build_from_cfg
 
 OPTIMIZERS = Registry('optimizer')
 
 for name, module in inspect.getmembers(torch.optim):
     if name.startswith('__'):
         continue
     if inspect.isclass(module) and issubclass(module, torch.optim.Optimizer):
```

### Comparing `weathon-0.0.0.17/weathon/registry/parallel.py` & `weathon-0.0.0.18/weathon/dl/registry/parallel.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from torch.nn.parallel.distributed import DistributedDataParallel
 
-from weathon.registry.registry import Registry, build_from_cfg
-from weathon.utils.config.config import ConfigDict
+from weathon.dl.registry.registry import Registry, build_from_cfg
+from weathon.dl.utils.config.config import ConfigDict
 
 PARALLEL = Registry('parallel')
 PARALLEL.register_module(module_name='DistributedDataParallel', module_cls=DistributedDataParallel)
 
 
 def build_parallel(cfg: ConfigDict, default_args: dict = None):
     """ build parallel
```

### Comparing `weathon-0.0.0.17/weathon/registry/pipeline.py` & `weathon-0.0.0.18/weathon/dl/registry/pipeline.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-from weathon.registry.registry import Registry, build_from_cfg
-from weathon.utils.config.config import ConfigDict
+from weathon.dl.registry.registry import Registry, build_from_cfg
+from weathon.dl.utils.config.config import ConfigDict
 
 PIPELINES = Registry('pipelines')
 
 
 def build_pipeline(cfg: ConfigDict, task_name: str = None, default_args: dict = None):
     """ build pipeline given model config dict.
```

### Comparing `weathon-0.0.0.17/weathon/registry/processor.py` & `weathon-0.0.0.18/weathon/dl/registry/processor.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-from weathon.registry.registry import Registry, build_from_cfg
-from weathon.utils.config.config import ConfigDict
+from weathon.dl.registry.registry import Registry, build_from_cfg
+from weathon.dl.utils.config.config import ConfigDict
 
 PREPROCESSORS = Registry('preprocessors')
 
 POSTPROCESSORS = Registry('postprocessors')
 
 
 def build_preprocessor(cfg: ConfigDict, task_name: str = None, default_args: dict = None):
```

### Comparing `weathon-0.0.0.17/weathon/registry/registry.py` & `weathon-0.0.0.18/weathon/dl/registry/registry.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import inspect
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 TYPE_NAME = 'type'
 default_group = 'default'
 logger = get_logger()
 AST_INDEX = None
 
 
@@ -129,15 +129,15 @@
             raise KeyError(f'`cfg` or `default_args` must contain the key "{TYPE_NAME}", but got {cfg}\n{default_args}')
     if not isinstance(registry, Registry):
         raise TypeError(f'registry must be an modelscope.Registry object, but got {type(registry)}')
     if not (isinstance(default_args, dict) or default_args is None):
         raise TypeError(f'default_args must be a dict or None, but got {type(default_args)}')
 
     # 根据模块所需，动态加载。 
-    from weathon.utils.import_utils import LazyImportModule
+    from weathon.dl.utils.import_utils import LazyImportModule
     sig = (registry.name.upper(), group_key, cfg['type'])
     LazyImportModule.import_module(sig)
 
     args = cfg.copy()
     if default_args is not None:
         for name, value in default_args.items():
             args.setdefault(name, value)
```

### Comparing `weathon-0.0.0.17/weathon/registry/trainer.py` & `weathon-0.0.0.18/weathon/dl/registry/trainer.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-from weathon.registry.registry import Registry, build_from_cfg
-from weathon.utils.config.config import ConfigDict
-from weathon.utils.constants import Trainers
+from weathon.dl.registry.registry import build_from_cfg, Registry
+from weathon.dl.utils.config.config import ConfigDict
+from weathon.dl.utils.constants import Trainers
 
 TRAINERS = Registry('trainers')
 
 
 def build_trainer(cfg: ConfigDict, task_name: str = None, default_args: dict = None):
     """ build trainers given a trainers name
```

### Comparing `weathon-0.0.0.17/weathon/train.py` & `weathon-0.0.0.18/weathon/train.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import argparse
 
-from weathon.registry import build_trainer
+from weathon.dl.registry import build_trainer
 
 
 def parse_args():
     parser = argparse.ArgumentParser(description='Train a model')
     parser.add_argument('config', help='config file path', type=str)
     parser.add_argument(
         'trainer_name', help='name for trainers', type=str, default=None)
```

### Comparing `weathon-0.0.0.17/weathon/trainers/__init__.py` & `weathon-0.0.0.18/weathon/dl/trainers/__init__.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TYPE_CHECKING
 
-from weathon.utils.import_utils import LazyImportModule
+from weathon.dl.utils.import_utils import LazyImportModule
 
 if TYPE_CHECKING:
     from .nlp.text_classification import JDTextClassificationTrainer
     from .cv.ocr import OcrDetectionTrainer
 else:
     _import_structure = {
         'nlp.text_classification': ['JDTextClassificationTrainer'],
```

### Comparing `weathon-0.0.0.17/weathon/trainers/cv/ocr/trainer.py` & `weathon-0.0.0.18/weathon/dl/trainers/cv/ocr/trainer.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 from functools import partial
 
 from torch.utils.data import DataLoader
 
-from weathon.base import TorchCustomDataset
-from weathon.base.trainer import ConfigTrainer
-from weathon.registry import TRAINERS
-from weathon.utils.config.config import ConfigDict
-from weathon.utils.constants import Tasks, ModeKeys, Datasets
-from weathon.utils.dataset.collate_fns.cv.ocr_collate_fn import DetCollectFN
-from weathon.utils.trainer_utils import worker_init_fn
+from weathon.dl.base import TorchCustomDataset
+from weathon.dl.base.trainer import ConfigTrainer
+from weathon.dl.registry import TRAINERS
+from weathon.dl.utils.config.config import ConfigDict
+from weathon.dl.utils.constants import Tasks, ModeKeys, Datasets
+from weathon.dl.utils.dataset.collate_fns.cv.ocr_collate_fn import DetCollectFN
+from weathon.dl.utils.trainer_utils import worker_init_fn
 
 
 @TRAINERS.register_module(group_key=Tasks.ocr_detection, module_name=Datasets.icdar2015_ocr_detection)
 class OcrDetectionTrainer(ConfigTrainer):
 
     def __init__(self, *args, **kwargs):
         super().__init__(*args, **kwargs)
```

### Comparing `weathon-0.0.0.17/weathon/trainers/nlp/text_classification/trainer.py` & `weathon-0.0.0.18/weathon/dl/trainers/nlp/text_classification/trainer.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from typing import Optional, Mapping, Union
 
-from weathon.base import BaseProcessor
-from weathon.base.trainer import ConfigTrainer
-from weathon.registry import TRAINERS
-from weathon.utils.config.config import Config
-from weathon.utils.constants import Tasks, Datasets
+from weathon.dl.base import BaseProcessor
+from weathon.dl.base.trainer import ConfigTrainer
+from weathon.dl.registry import TRAINERS
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import Tasks, Datasets
 
 
 @TRAINERS.register_module(group_key=Tasks.text_classification, module_name=Datasets.jd_sentiment_text_classification)
 class JDTextClassificationTrainer(ConfigTrainer):
 
     def __init__(self, *args, **kwargs):
         super().__init__(*args, **kwargs)
```

### Comparing `weathon-0.0.0.17/weathon/tuner/control_sd_lora.py` & `weathon-0.0.0.18/weathon/dl/tuner/control_sd_lora.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/tuner/lora.py` & `weathon-0.0.0.18/weathon/dl/tuner/lora.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/tuner/sd_lora.py` & `weathon-0.0.0.18/weathon/dl/tuner/sd_lora.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/ast_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/ast_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,42 +7,44 @@
 from functools import reduce
 from pathlib import Path
 from typing import Union
 
 import gast
 import json
 
-from weathon.utils.constants import Tasks, Fields, Datasets, ModeKeys
-from weathon.registry.registry import default_group
-from weathon.utils.constants.default_constant import DEFAULT_CACHE_DIR
-from weathon.utils.fileio import LocalStorage
-from weathon.utils.constants import (Trainers,
+from weathon.dl.registry.registry import default_group
+from weathon.dl.utils.constants.default_constant import DEFAULT_CACHE_DIR
+from weathon.dl.utils.fileio import LocalStorage
+from weathon.dl.utils.constants import (Trainers,
                                      Models,
                                      TaskModels,
                                      Heads,
                                      Preprocessors,
                                      Metrics,
                                      Pipelines,
                                      CustomDatasets,
                                      Hooks,
                                      LR_Schedulers,
+                                    Tasks,
+                                    Datasets,Fields
                                      )
 
-from weathon.utils.logger import get_logger
+
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 storage = LocalStorage()
 p = Path(__file__)
 
 # get the path of package 'weathon'
 SKIP_FUNCTION_SCANNING = True
-WEATHON_PATH = p.resolve().parents[1]
+WEATHON_PATH = p.resolve().parent.parent
 INDEXER_FILE_DIR = DEFAULT_CACHE_DIR
 REGISTER_MODULE = 'register_module'
-IGNORED_PACKAGES = ['weathon', '.']
+IGNORED_PACKAGES = ['weathon', '.', 'dl']
 SCAN_SUB_FOLDERS = [
     'base', 'dataset', 'error', 'hooks', 'loss', 'metrics', 'models', 'optimizer',
     'pipelines', 'processors', 'registry', 'trainers', 'tuner', 'utils'
 ]
 INDEXER_FILE = 'ast_indexer'
 DECORATOR_KEY = 'decorators'
 EXPRESS_KEY = 'express'
@@ -636,15 +638,15 @@
     updated_index = file_scanner.get_files_scan_results(updated_files)
     index[INDEX_KEY].update(updated_index[INDEX_KEY])
     index[REQUIREMENT_KEY].update(updated_index[REQUIREMENT_KEY])
 
 
 def load_index(
         file_list=None,
-        force_rebuild=False,
+        force_rebuild=True,
         indexer_file_dir=INDEXER_FILE_DIR,
         indexer_file=INDEXER_FILE,
 ):
     """get the index from scan results or cache
 
     Args:
         file_list: load indexer only from the file lists if provided, default as None
@@ -655,20 +657,20 @@
         dict: the index information for all registered modules, including key:
         index, requirements, files last modified time, weathon home path,
         version and md5, the detail is shown below example: {
             'index': {
                 ('MODELS', 'nlp', 'bert'):{
                     'filepath' : 'path/to/the/registered/model', 'imports':
                     ['os', 'torch', 'typing'] 'module':
-                    'weathon.models.nlp.bert'
+                    'weathon.dl.models.nlp.bert'
                 },
                 ...
             }, 'requirements': {
-                'weathon.models.nlp.bert': ['os', 'torch', 'typing'],
-                'weathon.models.nlp.structbert': ['os', 'torch', 'typing'],
+                'weathon.dl.models.nlp.bert': ['os', 'torch', 'typing'],
+                'weathon.dl.models.nlp.structbert': ['os', 'torch', 'typing'],
                 ...
             }, 'files_mtime' : {
                 '/User/Path/To/Your/Weathon/weathon/preprocessors/nlp/text_generation_preprocessor.py':
                 16554565445, ...
             },'version': '0.2.3', 'md5': '8616924970fe6bc119d1562832625612',
             'weathon_path': '/User/Path/To/Your/Weathon'
         }
@@ -692,16 +694,15 @@
 
     if index is None:
         full_index_flag = True
     elif index and local_changed and FILES_MTIME_KEY not in index:
         full_index_flag = True
     elif index and local_changed and WEATHON_PATH_KEY not in index:
         full_index_flag = True
-    elif index and local_changed and index[
-        WEATHON_PATH_KEY] != WEATHON_PATH.as_posix():
+    elif index and local_changed and index[WEATHON_PATH_KEY] != WEATHON_PATH.as_posix():
         full_index_flag = True
 
     if full_index_flag:
         if force_rebuild:
             logger.info('Force rebuilding ast index from scanning every file!')
             index = file_scanner.get_files_scan_results(file_list)
         else:
```

### Comparing `weathon-0.0.0.17/weathon/utils/audio/audio_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/audio/audio_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,16 +4,16 @@
 import sys
 import tempfile
 from typing import Union
 from urllib.parse import urlparse
 
 import numpy as np
 
-from weathon.utils.fileio.file import HTTPStorage
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.fileio.file import HTTPStorage
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 SEGMENT_LENGTH_TRAIN = 16000
 SUPPORT_AUDIO_TYPE_SETS = ('.flac', '.mp3', '.ogg', '.opus', '.wav', '.pcm')
```

### Comparing `weathon-0.0.0.17/weathon/utils/audio/tts_exceptions.py` & `weathon-0.0.0.18/weathon/dl/utils/audio/tts_exceptions.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/checkpoint.py` & `weathon-0.0.0.18/weathon/dl/utils/checkpoint.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,19 +8,19 @@
 
 import json
 import torch
 from torch import nn
 from torch.optim import Optimizer
 from torch.optim.lr_scheduler import LRScheduler
 
-from weathon.utils.constants import ConfigFields, ModelFile
-from weathon.utils.fileio import LocalStorage, File
-from weathon.utils.fileio.format.json_utils import JSONIteratorEncoder
-from weathon.utils.logger import get_logger
-from weathon.utils.torch_utils import is_master
+from weathon.dl.utils.constants import ConfigFields, ModelFile
+from weathon.dl.utils.fileio import LocalStorage, File
+from weathon.dl.utils.fileio.format.json_utils import JSONIteratorEncoder
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.torch_utils import is_master
 
 logger = get_logger()
 
 storage = LocalStorage()
 
 
 def weights_to_cpu(state_dict):
@@ -564,15 +564,15 @@
         'unexpected_keys': unexpected_keys,
         'mismatched_keys': mismatched_keys,
         'error_msgs': error_msgs,
     }
 
 
 def save_configuration(target_folder, config: Dict):
-    from weathon.utils.config.config import Config
+    from weathon.dl.utils.config.config import Config
     if isinstance(config, Config):
         config = config.to_dict()
     if ConfigFields.pipeline not in config:
         config[ConfigFields.pipeline] = {'type': config[ConfigFields.task]}
     cfg_str = json.dumps(config, indent=4, cls=JSONIteratorEncoder)
     config_file = os.path.join(target_folder, ModelFile.CONFIGURATION)
     storage.write(cfg_str.encode(), config_file)
```

### Comparing `weathon-0.0.0.17/weathon/utils/chinese_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/chinese_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/cli/cli.py` & `weathon-0.0.0.18/weathon/dl/utils/cli/cli.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import argparse
 
-from weathon.utils.cli.pipeline import PipelineCMD
-from weathon.utils.cli.plugins import PluginsCMD
+from .pipeline import PipelineCMD
+from .plugins import PluginsCMD
 
 
 def run_cmd():
     parser = argparse.ArgumentParser(
         'weathon Command Line tool', usage='weathon <command> [<args>]')
     subparsers = parser.add_subparsers(help='weathon commands helpers')
```

### Comparing `weathon-0.0.0.17/weathon/utils/cli/cli_argument_parser.py` & `weathon-0.0.0.18/weathon/dl/utils/cli/cli_argument_parser.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/cli/pipeline.py` & `weathon-0.0.0.18/weathon/dl/utils/cli/pipeline.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import os
 from argparse import ArgumentParser
 from string import Template
 
-from weathon.base.cli import CLICommand
-from weathon.utils.logger import get_logger
+from weathon.dl.base.cli import CLICommand
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 curren_path = os.path.dirname(os.path.abspath(__file__))
 template_path = os.path.join(curren_path, 'template')
```

### Comparing `weathon-0.0.0.17/weathon/utils/cli/plugins.py` & `weathon-0.0.0.18/weathon/dl/utils/cli/plugins.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from argparse import ArgumentParser
 
-from weathon.base.cli import CLICommand
-from weathon.utils.plugins import PluginsManager
+from weathon.dl.base.cli import CLICommand
+from weathon.dl.utils.plugins import PluginsManager
 
 plugins_manager = PluginsManager()
 
 
 def subparser_func(args):
     """ Function which will be called for a specific sub parser.
     """
```

### Comparing `weathon-0.0.0.17/weathon/utils/cli/training_args.py` & `weathon-0.0.0.18/weathon/dl/utils/cli/training_args.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,16 +2,16 @@
 from copy import deepcopy
 from dataclasses import dataclass, field, fields
 from typing import List, Union
 
 import addict
 import json
 
-from weathon.utils.cli.cli_argument_parser import CliArgumentParser
-from weathon.utils.config.config import Config
+from weathon.dl.utils.cli.cli_argument_parser import CliArgumentParser
+from weathon.dl.utils.config.config import Config
 
 
 def set_flatten_value(values: Union[str, List[str]]):
     pairs = values.split(',') if isinstance(values, str) else values
     _params = {}
     for kv in pairs or []:
         if len(kv.strip()) == 0:
```

### Comparing `weathon-0.0.0.17/weathon/utils/config/__init__.py` & `weathon-0.0.0.18/weathon/dl/utils/config/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,12 @@
 from http.cookiejar import CookieJar
-from typing import Tuple, Optional, Union, Sequence, Mapping
+from typing import Tuple, Optional, Union
 
 from datasets import DownloadConfig
 
-from weathon.utils.constants import DownloadMode
 
 
 class BaseAuthConfig(object):
     """Base authorization config class."""
 
     def __init__(self, cookies: CookieJar, git_token: str,
                  user_info: Tuple[str, str]):
```

### Comparing `weathon-0.0.0.17/weathon/utils/config/config.py` & `weathon-0.0.0.18/weathon/dl/utils/config/config.py`

 * *Files 0% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 import types
 from pathlib import Path
 from typing import Dict, Union
 
 import addict
 from yapf.yapflib.yapf_api import FormatCode
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 BASE_KEY = '_base_'
 DELETE_KEY = '_delete_'
 DEPRECATION_KEY = '_deprecation_'
 RESERVED_KEYS = ['filename', 'text', 'pretty_text']
@@ -93,28 +93,28 @@
                 dir=tmp_cfg_dir, suffix=fileExtname)
             if platform.system() == 'Windows':
                 tmp_cfg_file.close()
             tmp_cfg_name = osp.basename(tmp_cfg_file.name)
             shutil.copyfile(filename, tmp_cfg_file.name)
 
             if filename.endswith('.py'):
-                from weathon.utils.import_utils import import_modules_from_file
+                from weathon.dl.utils.import_utils import import_modules_from_file
                 module_nanme, mod = import_modules_from_file(
                     osp.join(tmp_cfg_dir, tmp_cfg_name))
                 cfg_dict = {}
                 for name, value in mod.__dict__.items():
                     if not name.startswith('__') and \
                        not isinstance(value, types.ModuleType) and \
                        not isinstance(value, types.FunctionType):
                         cfg_dict[name] = value
 
                 # delete imported module
                 del sys.modules[module_nanme]
             elif filename.endswith(('.yml', '.yaml', '.json')):
-                from weathon.utils.fileio import load
+                from weathon.dl.utils.fileio import load
                 cfg_dict = load(tmp_cfg_file.name)
             # close temp file
             tmp_cfg_file.close()
 
         cfg_text = filename + '\n'
         with open(filename, 'r', encoding='utf-8') as f:
             # Setting encoding explicitly to resolve coding issue on windows
@@ -394,15 +394,15 @@
             >>> dump_file = "a.py"
             >>> cfg.dump(dump_file)
 
         Args:
             file (str, optional): Path of the output file where the config
                 will be dumped. Defaults to None.
         """
-        from weathon.utils.fileio import dump
+        from weathon.dl.utils.fileio import dump
         cfg_dict = super(Config, self).__getattribute__('_cfg_dict').to_dict()
         if file is None:
             if self.filename is None or self.filename.endswith('.py'):
                 return self.pretty_text
             else:
                 file_format = self.filename.split('.')[-1]
                 return dump(cfg_dict, file_format=file_format)
```

### Comparing `weathon-0.0.0.17/weathon/utils/config/config_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/config/config_utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from typing import Union
 
-from weathon.utils.config.config import ConfigDict, Config
-from weathon.utils.constants import ModelFile, ConfigFields
+from .config import ConfigDict, Config
+from weathon.dl.utils.constants import ModelFile, ConfigFields
 
 
 def check_config(cfg: Union[str, ConfigDict], is_training=False):
     """ Check whether configuration file is valid, If anything wrong, exception will be raised.
 
     Args:
         cfg (str or ConfigDict): Config file path or config object.
```

### Comparing `weathon-0.0.0.17/weathon/utils/constants/constants.py` & `weathon-0.0.0.18/weathon/dl/utils/constants/constants.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/constants/hub_constant.py` & `weathon-0.0.0.18/weathon/dl/utils/constants/hub_constant.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/constants/map_constant.py` & `weathon-0.0.0.18/weathon/dl/utils/constants/map_constant.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from weathon.utils.constants.constants import Metrics, Preprocessors, TaskModels, Tasks, Models, Pipelines
+from weathon.dl.utils.constants.constants import Metrics, Preprocessors, TaskModels, Tasks, Models, Pipelines
 
 task_default_metrics = {
     Tasks.image_segmentation: [Metrics.image_ins_seg_coco_metric],
     Tasks.sentence_similarity: [Metrics.seq_cls_metric],
     Tasks.nli: [Metrics.seq_cls_metric],
     Tasks.sentiment_classification: [Metrics.seq_cls_metric],
     Tasks.token_classification: [Metrics.token_cls_metric],
```

### Comparing `weathon-0.0.0.17/weathon/utils/constants/output_constant.py` & `weathon-0.0.0.18/weathon/dl/utils/constants/output_constant.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from typing import List, Dict
 
 import numpy as np
 
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants import Tasks
 
 
 class OutputKeys(object):
     LOSS = 'loss'
     LOGITS = 'logits'
     SCORES = 'scores'
     SCORE = 'score'
```

### Comparing `weathon-0.0.0.17/weathon/utils/constants/pipeline_inputs.py` & `weathon-0.0.0.18/weathon/dl/utils/constants/pipeline_inputs.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import numpy as np
 
-from weathon.utils.constants import Tasks
+from weathon.dl.utils.constants import Tasks
 from PIL import Image
 
 
 class InputKeys(object):
     IMAGE = 'image'
     TEXT = 'text'
     VIDEO = 'video'
```

### Comparing `weathon-0.0.0.17/weathon/utils/cv/image_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/cv/image_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,16 +4,16 @@
 import matplotlib
 import matplotlib.cm as cm
 import matplotlib.pyplot as plt
 import numpy as np
 from PIL import Image
 
 # from weathon.preprocessors.image import load_image
-from weathon.utils import logger as logging
-from weathon.utils.constants.output_constant import OutputKeys
+from weathon.dl.utils import logger as logging
+from weathon.dl.utils.constants.output_constant import OutputKeys
 
 logger = logging.get_logger()
 
 
 def numpy_to_cv2img(img_array):
     """to convert a np.array with shape(h, w) to cv2 img
```

### Comparing `weathon-0.0.0.17/weathon/utils/cv/motion_utils/motion_process.py` & `weathon-0.0.0.18/weathon/dl/utils/cv/motion_utils/motion_process.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/cv/motion_utils/plot_script.py` & `weathon-0.0.0.18/weathon/dl/utils/cv/motion_utils/plot_script.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/cv/motion_utils/rotation_conversions.py` & `weathon-0.0.0.18/weathon/dl/utils/cv/motion_utils/rotation_conversions.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/cv/ocr/common_modules.py` & `weathon-0.0.0.18/weathon/dl/utils/cv/ocr/common_modules.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/cv/ocr/ocr_show_img.py` & `weathon-0.0.0.18/weathon/dl/utils/cv/ocr/ocr_show_img.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/cv/ocr/utils.py` & `weathon-0.0.0.18/weathon/dl/utils/cv/ocr/utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/data_collators.py` & `weathon-0.0.0.18/weathon/dl/utils/data_collators.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/data_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/data_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from collections.abc import Mapping
 
 import torch
 
-from weathon.base.model import BaseOutput
+from weathon.dl.base.model import BaseOutput
 
 
 def to_device(batch, device, non_blocking=False):
     """Put the data to the target cuda device just before the forward function.
     Args:
         batch: The batch data out of the dataloader.
         device: (str | torch.device): The target device for the data.
```

### Comparing `weathon-0.0.0.17/weathon/utils/dataset/collate_fns/cv/ocr_collate_fn.py` & `weathon-0.0.0.18/weathon/dl/utils/dataset/collate_fns/cv/ocr_collate_fn.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/dataset/dataset_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/dataset/dataset_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import os
 from typing import Optional, Union
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 def format_dataset_structure(dataset_structure):
     return {
         k: v
```

### Comparing `weathon-0.0.0.17/weathon/utils/dataset/maxcompute_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/dataset/maxcompute_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/device.py` & `weathon-0.0.0.18/weathon/dl/utils/device.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import os
 from contextlib import contextmanager
 
-from weathon.utils.constants import Devices, Frameworks
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants import Devices, Frameworks
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 def verify_device(device_name):
     """ Verify device is valid, device should be either cpu, cuda, gpu, cuda:X or gpu:X.
```

### Comparing `weathon-0.0.0.17/weathon/utils/exporter_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/exporter_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from contextlib import contextmanager
 
-from weathon.base.model import TorchModel
+from weathon.dl.base.model import TorchModel
 
 
 @contextmanager
 def replace_call():
     """This function is used to recover the original call method.
 
     The Model class of modelscope overrides the call method. When exporting to onnx or torchscript, torch will
```

### Comparing `weathon-0.0.0.17/weathon/utils/fileio/caching.py` & `weathon-0.0.0.18/weathon/dl/utils/fileio/caching.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import hashlib
 import os
 import pickle
 import tempfile
 from shutil import move, rmtree
 
-from weathon.utils.constants import MODEL_META_FILE_NAME, MODEL_META_MODEL_ID
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants import MODEL_META_FILE_NAME, MODEL_META_MODEL_ID
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 """Implements caching functionality, used internally only
 """
 
 
 class FileSystemCache(object):
```

### Comparing `weathon-0.0.0.17/weathon/utils/fileio/file.py` & `weathon-0.0.0.18/weathon/dl/utils/fileio/file.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,14 +3,16 @@
 import tempfile
 from abc import ABCMeta, abstractmethod
 from pathlib import Path
 from typing import Generator, Union
 
 import requests
 
+from weathon.dl.utils.fileio.file_utils import ensure_directory
+
 
 class Storage(metaclass=ABCMeta):
     """Abstract class of storage.
 
     All backends need to implement two apis: ``read()`` and ``read_text()``.
     ``read()`` reads the file as a byte stream and ``read_text()`` reads
     the file as texts.
@@ -110,15 +112,15 @@
         with open(filepath, 'w', encoding=encoding) as f:
             f.write(obj)
 
     @contextlib.contextmanager
     def as_local_path(
             self,
             filepath: Union[str,
-                            Path]) -> Generator[Union[str, Path], None, None]:
+            Path]) -> Generator[Union[str, Path], None, None]:
         """Only for unified API and do nothing."""
         yield filepath
 
 
 class HTTPStorage(Storage):
     """HTTP and HTTPS storage."""
 
@@ -246,15 +248,15 @@
             # local path
             storage_type = 'local'
         else:
             prefix, _ = uri.split('://')
             storage_type = prefix
 
         assert storage_type in File._prefix_to_storage, \
-            f'Unsupported uri {uri}, valid prefixs: '\
+            f'Unsupported uri {uri}, valid prefixs: ' \
             f'{list(File._prefix_to_storage.keys())}'
 
         if storage_type not in G_STORAGES:
             G_STORAGES[storage_type] = File._prefix_to_storage[storage_type]()
 
         return G_STORAGES[storage_type]
 
@@ -320,7 +322,8 @@
 
     @contextlib.contextmanager
     def as_local_path(uri: str) -> Generator[Union[str, Path], None, None]:
         """Only for unified API and do nothing."""
         storage = File._get_storage(uri)
         with storage.as_local_path(uri) as local_path:
             yield local_path
+
```

### Comparing `weathon-0.0.0.17/weathon/utils/fileio/file_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/fileio/file_utils.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 import inspect
+import shutil
 from pathlib import Path
 from typing import Union
 
 
 # TODO: remove this api, unify to flattened args
 def func_receive_dict_inputs(func):
     """to decide if a func could recieve dict inputs or not
@@ -24,30 +25,12 @@
 
     if len(args) == 1 and args[0] in ['input', 'inputs']:
         return True
 
     return False
 
 
-
-
-
 def read_file(path):
-
     with open(path, 'r') as f:
         text = f.read()
     return text
 
-
-
-def ensure_dir(dirname: Union[str, Path]) -> Path:
-    """
-    ensure dir path is exist,if not exist,make it
-    Args:
-        dirname: 文件夹 路径
-
-    Returns:
-    """
-    dirname = Path(dirname)
-    if not dirname.is_dir():
-        dirname.mkdir(parents=True, exist_ok=False)
-    return dirname
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `weathon-0.0.0.17/weathon/utils/fileio/format/json.py` & `weathon-0.0.0.18/weathon/dl/utils/fileio/format/json.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/fileio/format/json_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/fileio/format/json_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/fileio/format/jsonplus.py` & `weathon-0.0.0.18/weathon/dl/utils/fileio/format/jsonplus.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/fileio/format/yaml.py` & `weathon-0.0.0.18/weathon/dl/utils/fileio/format/yaml.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/fileio/io.py` & `weathon-0.0.0.18/weathon/dl/utils/fileio/io.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/git.py` & `weathon-0.0.0.18/weathon/dl/utils/git.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import os
 import subprocess
 from typing import List, Optional
 
-from weathon.utils.constants import MASTER_MODEL_BRANCH
-from weathon.utils.logger import get_logger
-from weathon.error.hub_error import GitError
+from weathon.dl.utils.constants import MASTER_MODEL_BRANCH
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.error.hub_error import GitError
 
 logger = get_logger()
 
 
 class Singleton(type):
     _instances = {}
```

### Comparing `weathon-0.0.0.17/weathon/utils/import_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/import_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -10,17 +10,17 @@
 from itertools import chain
 from pathlib import Path
 from types import ModuleType
 from typing import Any
 
 from packaging import version
 
-from weathon.utils.ast_utils import (INDEX_KEY, MODULE_KEY, REQUIREMENT_KEY, load_index)
-from weathon.error.error import *  # noqa
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.ast_utils import (INDEX_KEY, MODULE_KEY, REQUIREMENT_KEY, load_index)
+from weathon.dl.error import *  # noqa
+from weathon.dl.utils.logger import get_logger
 
 if sys.version_info < (3, 8):
     import importlib_metadata
 else:
     import importlib.metadata as importlib_metadata
 
 logger = get_logger()
```

### Comparing `weathon-0.0.0.17/weathon/utils/inference.py` & `weathon-0.0.0.18/weathon/dl/utils/inference.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,16 +4,16 @@
 import shutil
 from collections.abc import Mapping
 
 import torch
 from torch import distributed as dist
 from tqdm import tqdm
 
-from weathon.utils.data_utils import to_device
-from weathon.utils.torch_utils import (broadcast, get_dist_info, is_dist, is_master, make_tmp_dir)
+from weathon.dl.utils.data_utils import to_device
+from weathon.dl.utils.torch_utils import (broadcast, get_dist_info, is_dist, is_master, make_tmp_dir)
 
 
 def single_gpu_test(trainer,
                     data_loader,
                     device,
                     metric_classes=None,
                     vis_closure=None,
```

### Comparing `weathon-0.0.0.17/weathon/utils/input_output.py` & `weathon-0.0.0.18/weathon/dl/utils/input_output.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,20 +4,20 @@
 import inspect
 from io import BytesIO
 from typing import Any
 from urllib.parse import urlparse
 
 import numpy as np
 
-from weathon.utils.constants.output_constant import TASK_OUTPUTS, OutputTypeSchema, OutputTypes, OutputKeys
-from weathon.utils.constants.pipeline_inputs import (INPUT_TYPE, INPUT_TYPE_SCHEMA, TASK_INPUTS, InputType)
-from weathon.base import BasePipeline
-from weathon.utils.config.config import Config
-from weathon.utils.constants import ModelFile, Tasks
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants.output_constant import TASK_OUTPUTS, OutputTypeSchema, OutputTypes, OutputKeys
+from weathon.dl.utils.constants.pipeline_inputs import (INPUT_TYPE, INPUT_TYPE_SCHEMA, TASK_INPUTS, InputType)
+from weathon.dl.base import BasePipeline
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import ModelFile, Tasks
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 """Support webservice integration pipeline。
 
 This module provides a support library when webservice uses pipeline,
 converts webservice input into pipeline input, and converts pipeline
 output into webservice output, which automatically encodes and
```

### Comparing `weathon-0.0.0.17/weathon/utils/logger/log_buffer.py` & `weathon-0.0.0.18/weathon/dl/utils/logger/log_buffer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/logger/logger.py` & `weathon-0.0.0.18/weathon/dl/utils/logger/logger.py`

 * *Files 3% similar despite different names*

```diff
@@ -35,15 +35,15 @@
         if type(handler) is logging.StreamHandler:
             handler.setLevel(logging.ERROR)
 
     stream_handler = logging.StreamHandler()
     handlers = [stream_handler]
 
     if importlib.util.find_spec('torch') is not None:
-        from weathon.utils.torch_utils import is_master
+        from weathon.dl.utils.torch_utils import is_master
         is_worker0 = is_master()
     else:
         is_worker0 = True
 
     if is_worker0 and log_file is not None:
         file_handler = logging.FileHandler(log_file, file_mode)
         handlers.append(file_handler)
@@ -65,15 +65,15 @@
 
 def add_file_handler_if_needed(logger, log_file, file_mode, log_level):
     for handler in logger.handlers:
         if isinstance(handler, logging.FileHandler):
             return
 
     if importlib.util.find_spec('torch') is not None:
-        from weathon.utils.torch_utils import is_master
+        from weathon.dl.utils.torch_utils import is_master
         is_worker0 = is_master()
     else:
         is_worker0 = True
 
     if is_worker0 and log_file is not None:
         file_handler = logging.FileHandler(log_file, file_mode)
         file_handler.setFormatter(formatter)
```

### Comparing `weathon-0.0.0.17/weathon/utils/megatron_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/megatron_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 import os
 import shutil
 from typing import Dict, List, Union
 
 import torch
 from torch import nn
 
-from weathon.utils.config.config import Config
-from weathon.utils.constants import ModelFile
-from weathon.utils.logger import get_logger
-from weathon.utils.torch_utils import is_master
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import ModelFile
+from weathon.dl.utils.logger import get_logger
+from weathon.dl.utils.torch_utils import is_master
 
 logger = get_logger()
 
 _DEFAULT_CFG_WITH_MODEL_TYPE = {
     'gpt-moe': {
         'version': 'moe',
         'world_size': 8
```

### Comparing `weathon-0.0.0.17/weathon/utils/metric.py` & `weathon-0.0.0.18/weathon/dl/utils/metric.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/model_tag.py` & `weathon-0.0.0.18/weathon/dl/utils/model_tag.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/distributed.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/distributed.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/load_checkpoint.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/load_checkpoint.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/space/args.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/space/args.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/space/clean_dataset.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/space/clean_dataset.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/space/criterions.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/space/criterions.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/space/db_ops.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/space/db_ops.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/space/ontology.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/space/ontology.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/space/utils.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/space/utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import logging
 from collections import OrderedDict
 
 import json
 import numpy as np
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 from . import ontology
 
 logger = get_logger()
 
 
 def max_lens(X):
     lens = [len(X)]
```

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/space/utils_dst.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/space/utils_dst.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from typing import List
 
-from weathon.pipelines.nlp import DialogStateTrackingPipeline
-from weathon.utils.constants.output_constant import OutputKeys
+from weathon.dl.pipelines import DialogStateTrackingPipeline
+from weathon.dl.utils.constants.output_constant import OutputKeys
 
 
 def tracking_and_print_dialog_states(
         test_case, pipelines: List[DialogStateTrackingPipeline]):
     import json
     pipelines_len = len(pipelines)
     history_states = [{}]
```

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/space_T_en/utils.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/space_T_en/utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from typing import List
 
-from weathon.pipelines.nlp import ConversationalTextToSqlPipeline
-from weathon.utils.constants.output_constant import OutputKeys
+from weathon.dl.pipelines import ConversationalTextToSqlPipeline
+from weathon.dl.utils.constants.output_constant import OutputKeys
 
 
 def text2sql_tracking_and_print_results(
         test_case, pipelines: List[ConversationalTextToSqlPipeline]):
     for p in pipelines:
         last_sql, history = '', []
         for item in test_case['utterance']:
```

### Comparing `weathon-0.0.0.17/weathon/utils/nlp/utils.py` & `weathon-0.0.0.18/weathon/dl/utils/nlp/utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/ops/ailut/pyinterfaces.py` & `weathon-0.0.0.18/weathon/dl/utils/ops/ailut/pyinterfaces.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/functions/quadtree_attention.py` & `weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/functions/quadtree_attention.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/ops/quadtree_attention/modules/quadtree_attention.py` & `weathon-0.0.0.18/weathon/dl/utils/ops/quadtree_attention/modules/quadtree_attention.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import torch
 import torch.nn as nn
 from einops.einops import rearrange
 
-from weathon.utils.ops.quadtree_attention.functions.quadtree_attention import (
+from weathon.dl.utils.ops.quadtree_attention.functions.quadtree_attention import (
     score_computation_op, value_aggregation_op)
 
 
 class QTAttA(nn.Module):
 
     def __init__(
         self,
```

### Comparing `weathon-0.0.0.17/weathon/utils/output.py` & `weathon-0.0.0.18/weathon/dl/utils/output.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from dataclasses import dataclass
 from typing import List, Optional, Tuple, Union
 
 import numpy as np
 
-from weathon.base.model import BaseOutput
+from weathon.dl.base.model import BaseOutput
 
 Tensor = Union['torch.Tensor', 'tf.Tensor']
 
 @dataclass
 class DetectionOutput(BaseOutput):
     """The output class for object detection models.
```

### Comparing `weathon-0.0.0.17/weathon/utils/parallel_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/parallel_utils.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 from torch import nn
-from weathon.registry import PARALLEL
+from weathon.dl.registry import PARALLEL
 
 
 def is_parallel(module):
     """Check if a module is wrapped by parallel object.
 
     The following modules are regarded as parallel object:
      - torch.nn.parallel.DataParallel
```

### Comparing `weathon-0.0.0.17/weathon/utils/pipeline_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/pipeline_utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import os
 import os.path as osp
 from typing import List, Optional, Union
 
-from weathon.utils.constants import DEFAULT_MODEL_FOR_PIPELINE
-from weathon.utils.constants.pipeline_inputs import INPUT_TYPE, InputType
-from weathon.utils.config.config import Config
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants import DEFAULT_MODEL_FOR_PIPELINE
+from weathon.dl.utils.constants.pipeline_inputs import INPUT_TYPE, InputType
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 def check_input_type(input_type, input):
     expected_type = INPUT_TYPE[input_type]
     if input_type == InputType.VIDEO:
@@ -78,15 +78,15 @@
     Args:
         task (str): task name.
 
     Return:
         A tuple: first element is pipeline name(model_name), second element
             is modelhub name.
     """
-    from weathon.registry import PIPELINES
+    from weathon.dl.registry import PIPELINES
     if task not in DEFAULT_MODEL_FOR_PIPELINE:
         # support pipeline which does not register default model
         pipeline_name = list(PIPELINES.modules[task].keys())[0]
         default_model = None
     else:
         pipeline_name, default_model = DEFAULT_MODEL_FOR_PIPELINE[task]
     return pipeline_name, default_model
```

### Comparing `weathon-0.0.0.17/weathon/utils/plugins.py` & `weathon-0.0.0.18/weathon/dl/utils/plugins.py`

 * *Files 1% similar despite different names*

```diff
@@ -12,19 +12,19 @@
 from fnmatch import fnmatch
 from pathlib import Path
 from typing import Any, Iterable, List, Optional, Set, Union
 
 import json
 import pkg_resources
 
-from weathon.utils.ast_utils import FilesAstScanning
-from weathon.utils.constants import DEFAULT_MODEL_REVISION
-from weathon.utils.constants.default_constant import DEFAULT_CACHE_DIR
-from weathon.utils.fileio import LocalStorage
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.ast_utils import FilesAstScanning
+from weathon.dl.utils.constants import DEFAULT_MODEL_REVISION
+from weathon.dl.utils.constants.default_constant import DEFAULT_CACHE_DIR
+from weathon.dl.utils.fileio import LocalStorage
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 storage = LocalStorage()
 
 MODELSCOPE_FILE_DIR = DEFAULT_CACHE_DIR
 PLUGINS_FILENAME = '.weathon_plugins'
 OFFICIAL_PLUGINS = [
@@ -96,15 +96,15 @@
         Args:
         requirement_path: The file path of requirement
 
     """
     plugins: Set[str] = set()
     if requirement_path is None:
         if os.path.isfile(LOCAL_PLUGINS_FILENAME):
-            with push_python_path('.'):
+            with push_python_path(''):
                 for plugin in discover_file_plugins(LOCAL_PLUGINS_FILENAME):
                     if plugin in plugins:
                         continue
                     yield plugin
                     plugins.add(plugin)
         if os.path.isfile(GLOBAL_PLUGINS_FILENAME):
             for plugin in discover_file_plugins(GLOBAL_PLUGINS_FILENAME):
@@ -224,15 +224,15 @@
         return
 
     importlib.invalidate_caches()
 
     # For some reason, python doesn't always add this by default to your path, but you pretty much
     # always want it when using `--include-package`.  And if it's already there, adding it again at
     # the end won't hurt anything.
-    with push_python_path('.'):
+    with push_python_path(''):
         # Import at top level
         try:
             module = importlib.import_module(package_name)
             path = getattr(module, '__path__', [])
             path_string = '' if not path else path[0]
 
             # walk_packages only finds immediate children, so need to recurse.
```

### Comparing `weathon-0.0.0.17/weathon/utils/pretrained/converter/cv/ocr_detection/paddle_torch.py` & `weathon-0.0.0.18/weathon/dl/utils/pretrained/converter/cv/ocr_detection/paddle_torch.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/pretrained/utils.py` & `weathon-0.0.0.18/weathon/dl/utils/pretrained/utils.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import os.path as osp
 
-from weathon.utils.config.config import Config
-from weathon.utils.constants import ModelFile
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.config.config import Config
+from weathon.dl.utils.constants import ModelFile
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 
 def get_model_type(model_dir):
     """Get the model type from the configuration.
```

### Comparing `weathon-0.0.0.17/weathon/utils/print_info.py` & `weathon-0.0.0.18/weathon/dl/utils/print_info.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import json
 from copy import deepcopy
-from weathon.utils.torch_utils import is_master
-from weathon.utils.fileio.format.json_utils import JSONIteratorEncoder
+from weathon.dl.utils.torch_utils import is_master
+from weathon.dl.utils.fileio.format.json_utils import JSONIteratorEncoder
 def print_cfg(self):
     if is_master():
         cfg = deepcopy(self.cfg)
         cfg.train.work_dir = self.work_dir
         self.logger.info('==========================Training Config Start==========================')
         self.logger.info(json.dumps(cfg._cfg_dict, indent=4, cls=JSONIteratorEncoder))
         self.logger.info('===========================Training Config End===========================')
```

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/common.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/common.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 import time
 from collections.abc import Sequence
 from typing import Mapping
 
 import numpy as np
 import torch
 
-from weathon.registry import PREPROCESSORS, build_preprocessor
-from weathon.registry.registry import default_group
+from weathon.dl.registry import PREPROCESSORS, build_preprocessor
+from weathon.dl.registry.registry import default_group
 
 
 @PREPROCESSORS.register_module()
 class Compose(object):
     """Compose a data pipeline with a sequence of transforms.
     Args:
         transforms (list[dict | callable]):
```

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/augment.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/augment.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/fce_aug.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/fce_aug.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/fce_target.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/fce_target.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/iaa_augment.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/iaa_augment.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/make_border_map.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/make_border_map.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/make_shrink_map.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/make_shrink_map.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/cv/ocr/process_module/random_crop_data.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/cv/ocr/process_module/random_crop_data.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import random
 
 import cv2
 import numpy as np
 
 __all__ = ['EastRandomCropData', 'PSERandomCrop']
 
-from weathon.utils.config.config import ConfigDict
+from weathon.dl.utils.config.config import ConfigDict
 
 
 # random crop algorithm similar to https://github.com/argman/EAST
 class EastRandomCropData():
     def __init__(self, size= (640, 640),max_tries=50, min_crop_side_ratio=0.1, require_original_image=False, keep_ratio=True):
         self.size = size
         self.max_tries = max_tries
```

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/preprocessor_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/preprocessor_utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from typing import Mapping
 
-from weathon.utils.constants import ModeKeys
-from weathon.utils.constants.output_constant import OutputKeys
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants import ModeKeys
+from weathon.dl.utils.constants.output_constant import OutputKeys
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 __all__ = ['parse_text_and_label', 'labels_to_id']
 
 
 def parse_text_and_label(data,
```

### Comparing `weathon-0.0.0.17/weathon/utils/processor/preprocessors/transformers_tokenizer.py` & `weathon-0.0.0.18/weathon/dl/utils/processor/preprocessors/transformers_tokenizer.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import os
 
 import json
 from transformers import AutoTokenizer
 
-from weathon.utils.constants import Models
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.constants import Models
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 __all__ = [
     'NLPTokenizer',
 ]
 
@@ -75,15 +75,15 @@
             return tokenizer.from_pretrained(
                 model_dir) if model_dir is not None else tokenizer()
         elif model_type == Models.veco:
             from transformers import XLMRobertaTokenizer, XLMRobertaTokenizerFast
             tokenizer = XLMRobertaTokenizerFast if self.use_fast else XLMRobertaTokenizer
             return tokenizer.from_pretrained(model_dir) if model_dir is not None else tokenizer()
         elif model_type == Models.llama:
-            from weathon.models.nlp import LlamaTokenizer, LlamaTokenizerFast
+            from weathon.dl.models.nlp import LlamaTokenizer, LlamaTokenizerFast
             tokenizer = LlamaTokenizerFast if self.use_fast else LlamaTokenizer
             return tokenizer.from_pretrained(model_dir) if model_dir is not None else tokenizer()
 
         assert model_dir is not None
         return AutoTokenizer.from_pretrained(model_dir, use_fast=self.use_fast)
 
     def __call__(self, text, text_pair=None, **kwargs):
```

### Comparing `weathon-0.0.0.17/weathon/utils/service_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/service_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,17 +2,17 @@
 import mimetypes
 from io import BytesIO
 
 import json
 import numpy as np
 import requests
 
-from weathon.utils.constants.output_constant import TASK_OUTPUTS, OutputKeys
-from weathon.utils.constants.pipeline_inputs import TASK_INPUTS, InputType
-from weathon.utils.url_utils import valid_url
+from weathon.dl.utils.constants.output_constant import TASK_OUTPUTS, OutputKeys
+from weathon.dl.utils.constants.pipeline_inputs import TASK_INPUTS, InputType
+from weathon.dl.utils.url_utils import valid_url
 
 
 # service data decoder func decodes data from network and convert it to pipeline's input
 # for example
 def ExampleDecoder(data):
     # Assuming the pipeline inputs is a dict contains an image and a text,
     # to decode the data from network we decode the image as base64
```

### Comparing `weathon-0.0.0.17/weathon/utils/task_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/task_utils.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from weathon.utils.constants import Tasks, TaskModels
+from weathon.dl.utils.constants import Tasks, TaskModels
 
 SUB_TASKS = 'sub_tasks'
 PARENT_TASK = 'parent_task'
 TASK_MODEL = 'task_model'
 
 DEFAULT_TASKS_LEVEL = {
     Tasks.text_classification: {
```

### Comparing `weathon-0.0.0.17/weathon/utils/tensor_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/tensor_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/test_utils/regress_test_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/test_utils/regress_test_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/test_utils/test_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/test_utils/test_utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -12,16 +12,16 @@
 from collections import OrderedDict
 from collections.abc import Mapping
 from os.path import expanduser
 
 import numpy as np
 import requests
 
-from weathon.utils.constants.constants import DEFAULT_CREDENTIALS_PATH
-from weathon.utils.import_utils import is_tf_available, is_torch_available
+from weathon.dl.utils.constants.constants import DEFAULT_CREDENTIALS_PATH
+from weathon.dl.utils.import_utils import is_tf_available, is_torch_available
 
 TEST_LEVEL = 2
 TEST_LEVEL_STR = 'TEST_LEVEL'
 
 # for user citest and sdkdev
 TEST_ACCESS_TOKEN1 = os.environ.get('TEST_ACCESS_TOKEN_CITEST', None)
 TEST_ACCESS_TOKEN2 = os.environ.get('TEST_ACCESS_TOKEN_SDKDEV', None)
@@ -217,15 +217,15 @@
 
 _DIST_SCRIPT_TEMPLATE = """
 import ast
 import argparse
 import pickle
 import torch
 from torch import distributed as dist
-from weathon.utils.torch_utils import get_dist_info
+from weathon.dl.utils.torch_utils import get_dist_info
 import {}
 
 parser = argparse.ArgumentParser()
 parser.add_argument('--save_all_ranks', type=ast.literal_eval, help='save all ranks results')
 parser.add_argument('--save_file', type=str, help='save file')
 parser.add_argument('--local_rank', type=int, default=0)
 args = parser.parse_args()
@@ -250,15 +250,15 @@
 
 
 class DistributedTestCase(unittest.TestCase):
     """Distributed TestCase for test function with distributed mode.
     Examples:
         >>> import torch
         >>> from torch import distributed as dist
-        >>> from weathon.utils.torch_utils import init_dist
+        >>> from weathon.dl.utils.torch_utils import init_dist
 
         >>> def _test_func(*args, **kwargs):
         >>>     init_dist(launcher='pytorch')
         >>>     rank = dist.get_rank()
         >>>     if rank == 0:
         >>>         value = torch.tensor(1.0).cuda()
         >>>     else:
```

### Comparing `weathon-0.0.0.17/weathon/utils/timer.py` & `weathon-0.0.0.18/weathon/dl/utils/timer.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/torch_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/torch_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -125,15 +125,15 @@
     Args:
         group: The parallel group, default None, for the global group
 
     Returns:
         A tuple of the current rank and world_size of the group
     """
     if is_dist():
-        from weathon.utils.megatron_utils import is_megatron_initialized
+        from weathon.dl.utils.megatron_utils import is_megatron_initialized
         if group is None and is_megatron_initialized():
             from megatron_util import mpu
             group = mpu.get_data_parallel_group()
         rank = dist.get_rank(group)
         world_size = dist.get_world_size(group)
     else:
         rank = 0
```

### Comparing `weathon-0.0.0.17/weathon/utils/trie.py` & `weathon-0.0.0.18/weathon/dl/utils/trie.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/type_assert.py` & `weathon-0.0.0.18/weathon/dl/utils/type_assert.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils/url_utils.py` & `weathon-0.0.0.18/weathon/dl/utils/url_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from urllib.parse import urlparse
 
 import pandas as pd
 
-from weathon.utils.logger import get_logger
+from weathon.dl.utils.logger import get_logger
 
 logger = get_logger()
 
 
 def valid_url(url) -> bool:
     try:
         result = urlparse(url)
```

### Comparing `weathon-0.0.0.17/weathon/utils_/__init__.py` & `weathon-0.0.0.18/weathon/utils_/__init__.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,48 +1,48 @@
-# from weathon.utils.fileio.format.json_utils import JsonUtils  # Json 操作相关工具类
-# from weathon.utils.label_studio_utils import LabelStudioUtils  # Label Studio 相关操作工具类
-# from weathon.utils.fileio.file_utils import FileUtils  # 文件工具类
-# from weathon.utils.ip_utils import IpUtils  # IP相关操作工具类
+# from weathon.dl.utils.fileio.format.json_utils import JsonUtils  # Json 操作相关工具类
+# from weathon.dl.utils.label_studio_utils import LabelStudioUtils  # Label Studio 相关操作工具类
+# from weathon.dl.utils.fileio.file_utils import FileUtils  # 文件工具类
+# from weathon.dl.utils.ip_utils import IpUtils  # IP相关操作工具类
 # # --------------------------------------------- constants ---------------------------------------------
 #
 # # --------------------------------------------- string ---------------------------------------------
-# from weathon.utils.number_utils import NumberUtils  # 字符数值处理工具类
-# from weathon.utils.word_finder import AhoCorasick  # AC自动机:多模式匹配中的经典算法
-# from weathon.utils.word_discover import WordDiscoverer  # 新词发现 的工具包
-# from weathon.utils.encrypt_utils import EncryptUtils  # 字符串加密工具类
-# from weathon.utils.char_utils import CharUtils  # 字符处理
-# from weathon.utils.string_utils import StringUtils  # 字符串处理工具类
+# from weathon.dl.utils.number_utils import NumberUtils  # 字符数值处理工具类
+# from weathon.dl.utils.word_finder import AhoCorasick  # AC自动机:多模式匹配中的经典算法
+# from weathon.dl.utils.word_discover import WordDiscoverer  # 新词发现 的工具包
+# from weathon.dl.utils.encrypt_utils import EncryptUtils  # 字符串加密工具类
+# from weathon.dl.utils.char_utils import CharUtils  # 字符处理
+# from weathon.dl.utils.string_utils import StringUtils  # 字符串处理工具类
 #
 # # --------------------------------------------- deep learning ---------------------------------------------
 # # transformers 下载、权重转换相关
-# from weathon.utils.transformer_utils import TransformerUtils
+# from weathon.dl.utils.transformer_utils import TransformerUtils
 #
 # # 模型训练相关
-# from weathon.utils.sampler import ImbalancedDatasetSampler  # 模型采样
-# from weathon.utils.optimizer_utils import OptimizerUtils  # 优化器
-# from weathon.utils.schedule_utils import ScheduleUtils  # 优化器 scheduler
-# from weathon.utils.loss_utils import LossUtils  # 损失函数
-# from weathon.utils.attack import FGM, PGD  # 模型训练trick
-# from weathon.utils.ema import EMA  # 模型训练trick
+# from weathon.dl.utils.sampler import ImbalancedDatasetSampler  # 模型采样
+# from weathon.dl.utils.optimizer_utils import OptimizerUtils  # 优化器
+# from weathon.dl.utils.schedule_utils import ScheduleUtils  # 优化器 scheduler
+# from weathon.dl.utils.loss_utils import LossUtils  # 损失函数
+# from weathon.dl.utils.attack import FGM, PGD  # 模型训练trick
+# from weathon.dl.utils.ema import EMA  # 模型训练trick
 #
 # # 模型集成相关
 #
 # # 任务相关
-# from weathon.utils.ner_utils import NERUtils  # 命名实体识别
+# from weathon.dl.utils.ner_utils import NERUtils  # 命名实体识别
 #
 # # --------------------------------------------- music utils ---------------------------------------------
 # # 人声 转 钢琴 :
 # #   1. 录音: Recorder,
 # #   2. 切分: OnsetFrameSplitter , 将一个文件拆分成多个起始帧
 # #   3. 转谱: NotePoltter
 #
-# from weathon.utils.nextpow2 import next_pow2, get_next_power_2  # 辅助函数
-# from weathon.utils.noise_reduction import NoiseReduction        # 降噪
-# from weathon.utils.onset_frames_split import OnsetFrameSplitter # 端点检测
-# from weathon.utils.wav_utils import WaveProperties
-# from weathon.utils.sound_plot_utils import SoundPlotUtils
-# from weathon.utils.midi_detector import MIDIDetector            # 音符检测
-# from weathon.utils.note_plotter import NotePlotter              # 打谱
-# from weathon.utils.music import Music
+# from weathon.dl.utils.nextpow2 import next_pow2, get_next_power_2  # 辅助函数
+# from weathon.dl.utils.noise_reduction import NoiseReduction        # 降噪
+# from weathon.dl.utils.onset_frames_split import OnsetFrameSplitter # 端点检测
+# from weathon.dl.utils.wav_utils import WaveProperties
+# from weathon.dl.utils.sound_plot_utils import SoundPlotUtils
+# from weathon.dl.utils.midi_detector import MIDIDetector            # 音符检测
+# from weathon.dl.utils.note_plotter import NotePlotter              # 打谱
+# from weathon.dl.utils.music import Music
 #
 #
 # # TODO: 2. 下载类 3. 性能分析类 4. 日志类
```

### Comparing `weathon-0.0.0.17/weathon/utils_/attack.py` & `weathon-0.0.0.18/weathon/utils_/attack.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/char_utils.py` & `weathon-0.0.0.18/weathon/utils_/char_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/conlleval.py` & `weathon-0.0.0.18/weathon/utils_/conlleval.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/data_utils.py` & `weathon-0.0.0.18/weathon/utils_/data_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/dictionary.py` & `weathon-0.0.0.18/weathon/utils/dictionary.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/ema.py` & `weathon-0.0.0.18/weathon/utils_/ema.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/email_utils.py` & `weathon-0.0.0.18/weathon/utils_/email_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/encrypt_utils.py` & `weathon-0.0.0.18/weathon/utils/encrypt_utils.py`

 * *Files 20% similar despite different names*

```diff
@@ -4,24 +4,34 @@
 # @FileName: encrypt_utils.py
 # @github  : https://github.com/Lizhen0628
 # @Description:
 
 from hashlib import md5
 
 
-class EncryptUtils:
+class Encrypter:
     """
     加密工具类
     """
+    def __init__(self, instr:str, salt:str="CMyMxC4rHv"):
+        self.instr = instr
+        self.salt = salt
 
-    @staticmethod
-    def encry_md5(in_str: str, salt: str = "123456") -> str:
+    def encrypt(self,type='md5') -> str:
+        if type in ['md5']:
+            return self._md5()
+        else:
+            return self.instr
+
+
+
+
+    def _md5(self) -> str:
         """
         输入 字符串，对字符串采用md5算法加密，
         :param in_str:  需要加密的字符串
         :param salt:  盐，防止被撞库
         :return:  对字符串加密后的结果
         """
-
-        obj = md5(salt.encode("utf8"))
-        obj.update(in_str.encode("utf8"))
+        obj = md5(self.salt.encode("utf8"))
+        obj.update(self.instr.encode("utf8"))
         return obj.hexdigest()
```

### Comparing `weathon-0.0.0.17/weathon/utils_/environment_utils.py` & `weathon-0.0.0.18/weathon/utils_/environment_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/gpu_utils.py` & `weathon-0.0.0.18/weathon/utils_/gpu_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/ip_utils.py` & `weathon-0.0.0.18/weathon/utils_/ip_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/json_utils.py` & `weathon-0.0.0.18/weathon/utils_/json_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/keyword_extract.py` & `weathon-0.0.0.18/weathon/utils_/keyword_extract.py`

 * *Files 0% similar despite different names*

```diff
@@ -12,16 +12,16 @@
 
 import jieba.analyse
 import jieba.posseg
 import networkx as nx
 import pandas as pd
 
 from sklearn.feature_extraction.text import CountVectorizer, TfidfTransformer
-from weathon.utils.dictionary import Dictionary
-from weathon.utils.string_utils import StringUtils
+from weathon.dl.utils.dictionary import Dictionary
+from weathon.dl.utils.string_utils import StringUtils
 
 
 class KeywordExtractor:
 
     def __init__(self, stop_words: Set[str] = None, delim_words: Set[str] = None,
                  allow_pos: Set[str] = frozenset({'n', 'ns', 'nr', 'nt', 'nz', 'vn', 'v', 'an', 'a', 'i'}),
                  with_flag=False, with_weight=False, graph_weight=False):
```

### Comparing `weathon-0.0.0.17/weathon/utils_/label_studio_utils.py` & `weathon-0.0.0.18/weathon/utils_/label_studio_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/loss_utils.py` & `weathon-0.0.0.18/weathon/utils_/loss_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/midi_detector.py` & `weathon-0.0.0.18/weathon/utils_/midi_detector.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 # @github  : https://github.com/Lizhen0628
 # @Description:
 import scipy
 import numpy as np
 import pylab
 import scipy.io.wavfile as wav
 from scipy import signal
-from weathon.utils import WaveProperties, get_next_power_2
+from weathon.dl.utils import WaveProperties, get_next_power_2
 from itertools import product
 import math
 
 
 class MIDIDetector:
     """
     Class for MIDI notes detection given a .wav file.
```

### Comparing `weathon-0.0.0.17/weathon/utils_/minjoin.py` & `weathon-0.0.0.18/weathon/utils/minjoin.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/model_ensemble.py` & `weathon-0.0.0.18/weathon/utils_/model_ensemble.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/music.py` & `weathon-0.0.0.18/weathon/utils_/music.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/ner_utils.py` & `weathon-0.0.0.18/weathon/utils_/ner_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/nextpow2.py` & `weathon-0.0.0.18/weathon/utils_/nextpow2.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/noise_reduction.py` & `weathon-0.0.0.18/weathon/utils_/noise_reduction.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # @FileName: noise_reduction.py
 # @github  : https://github.com/Lizhen0628
 # @Description:
 
 import wave
 import numpy as np
 import math
-from weathon.utils import nextpow2
+from weathon.dl.utils import nextpow2
 
 
 class NoiseReduction:
 
     def __init__(self, input_file, output_file):
         self.input_file = str(input_file)
         self.output_file = str(output_file)
```

### Comparing `weathon-0.0.0.17/weathon/utils_/note_plotter.py` & `weathon-0.0.0.18/weathon/utils_/note_plotter.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 # @Time    : 2023/3/18 15:51
 # @Author  : LiZhen
 # @FileName: note_plotter.py
 # @github  : https://github.com/Lizhen0628
 # @Description:
 import os
 import numpy as np
-from weathon.utils import MIDIDetector, number2melody
+from weathon.dl.utils import MIDIDetector, number2melody
 from pathlib import Path
 
 
 class NotePlotter:
     """
         Class used for plotting sheet notes given MIDI note numbers.
     """
```

### Comparing `weathon-0.0.0.17/weathon/utils_/number_utils.py` & `weathon-0.0.0.18/weathon/utils_/number_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import random
 from typing import Union
 
-from weathon.utils.string_utils import StringUtils
+from weathon.dl.utils.string_utils import StringUtils
 
 
 class Number2Chinese():
     """
        codes reference: https://github.com/tyong920/a2c
     """
```

### Comparing `weathon-0.0.0.17/weathon/utils_/onset_frames_split.py` & `weathon-0.0.0.18/weathon/utils_/onset_frames_split.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 import wave
 import os
 from pathlib import Path
 
 import librosa
 import shutil
 
-from weathon.utils import NoiseReduction, FileUtils
+from weathon.dl.utils import NoiseReduction, FileUtils
 
 
 class OnsetFrameSplitter:
     """
         A class for splitting a file into onset frames.
     """
```

### Comparing `weathon-0.0.0.17/weathon/utils_/optimizer_utils.py` & `weathon-0.0.0.18/weathon/utils_/optimizer_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/pdf_utils.py` & `weathon-0.0.0.18/weathon/utils/fileio/pdf_reader.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,40 +1,40 @@
-# -*- coding: utf-8 -*-
-# @Time    : 2022/12/22 22:45
-# @Author  : LiZhen
-# @FileName: pdf_utils.py
-# @github  : https://github.com/Lizhen0628
-# @Description:
-
 import pdfplumber
 from typing import List
 from tqdm import tqdm
 from pdf2docx import Converter
 
 
-class PDFUtils:
+class PDFReader:
+
+    def __init__(self, file_path:str):
+        self.file_path = file_path
+
 
-    @staticmethod
-    def extract_text(pdf_file: str, pdf_pwd: str = None):
+    def extract_text(self,pdf_pwd:str):
         page_texts = []
-        with pdfplumber.open(pdf_file, password=pdf_pwd) as pdf_reader:
+        with pdfplumber.open(self.file_path, password=pdf_pwd) as pdf_reader:
             for page_id, page in enumerate(tqdm(pdf_reader.pages)):
                 page_text = page.extract_text()
                 page_texts.append((page_id, page_text))
         return page_texts
 
-    @staticmethod
-    def extract_tables(pdf_file:str,pdf_pwd:str = None):
+
+    def extract_tables(self,pdf_pwd:str):
         page_tables = []
-        with pdfplumber.open(pdf_file,password=pdf_pwd) as pdf_reader:
+        with pdfplumber.open(self.file_path, password=pdf_pwd) as pdf_reader:
             for page_id, page in enumerate(tqdm(pdf_reader.pages)):
-                page_tables.append((page_id,page.extract_tables()))
+                page_tables.append((page_id, page.extract_tables()))
         return page_tables
 
-    @staticmethod
-    def pdf2docx(pdf_file:str,docx_file:str,pdf_pwd:str=None, start:int=0,end:int = None,pages:List=None):
-        converter = Converter(pdf_file,pdf_pwd)
-        converter.convert(docx_file,start,end,pages)
 
+    def pdf2docx(self,
+                 docx_file: str,
+                 pdf_pwd: str = None,
+                 start: int = 0,
+                 end: int = None,
+                 pages: List = None
+                 ):
+
+        converter = Converter(self.file_path, pdf_pwd)
+        converter.convert(docx_file, start, end, pages)
 
-if __name__ == '__main__':
-    PDFUtils.extract_tables("")
```

### Comparing `weathon-0.0.0.17/weathon/utils_/prune.py` & `weathon-0.0.0.18/weathon/utils_/prune.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/sampler.py` & `weathon-0.0.0.18/weathon/utils_/sampler.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/schedule_utils.py` & `weathon-0.0.0.18/weathon/utils_/schedule_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/semantic_scholar.py` & `weathon-0.0.0.18/weathon/utils_/semantic_scholar.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/sound_plot_utils.py` & `weathon-0.0.0.18/weathon/utils_/sound_plot_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/sound_recorder.py` & `weathon-0.0.0.18/weathon/utils_/sound_recorder.py`

 * *Files 2% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 import logging
 import datetime
 import os
 import wave
 from pathlib import Path
 from threading import Thread
 
-from weathon.utils.fileio.file_utils import FileUtils
+from weathon.dl.utils.fileio.file_utils import FileUtils, ensure_directory
 
 from pyaudio import PyAudio, paInt16
 
 
 class Recorder:
 
     def __init__(self, chunk=2048, n_channels=1, rate=44100):
@@ -32,15 +32,15 @@
         """
         self.chunk = chunk
         self.n_channels = n_channels
         self.rate = rate
         self.format = paInt16
         self._running = True
         self.log = logging.getLogger()
-        self.record_dir = FileUtils.ensure_dir(Path(os.environ["DATA_DIR"]) / "weathon" / "record_wav")
+        self.record_dir = ensure_directory(Path(os.environ["DATA_DIR"]) / "weathon" / "record_wav")
 
     def _recording(self):
         self._running = True
         self._frames = []
         pa = PyAudio()
 
         stream = pa.open(format=self.format,
```

### Comparing `weathon-0.0.0.17/weathon/utils_/states_machine.py` & `weathon-0.0.0.18/weathon/utils_/states_machine.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/string_converter.py` & `weathon-0.0.0.18/weathon/utils_/string_converter.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # -*- coding: utf-8 -*-
 # @Time    : 2022/10/6 14:35
 # @Author  : LiZhen
 # @FileName: string_converter.py
 # @github  : https://github.com/Lizhen0628
 # @Description:
 
-from weathon.utils.states_machine import StatesMachine
+from weathon.dl.utils.states_machine import StatesMachine
 
 
 class Node(object):
     def __init__(self, from_word, to_word=None, is_tail=True,
                  have_child=False):
         self.from_word = from_word
         if to_word is None:
```

### Comparing `weathon-0.0.0.17/weathon/utils_/string_similarity.py` & `weathon-0.0.0.18/weathon/utils_/string_similarity.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/string_utils.py` & `weathon-0.0.0.18/weathon/utils_/string_utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -11,17 +11,17 @@
 import regex as re
 import unicodedata
 import urllib
 import urllib.parse
 import w3lib.html
 from typing import List, Union
 from opencc import OpenCC
-from weathon.utils.char_utils import CharUtils
-from weathon.utils.dictionary import Dictionary
-from weathon.utils.string_converter import ConvertMap, Converter
+from weathon.dl.utils.char_utils import CharUtils
+from weathon.dl.utils.dictionary import Dictionary
+from weathon.dl.utils.string_converter import ConvertMap, Converter
 
 
 def add_curr_dir(name):
     return os.path.join(os.path.dirname(__file__), name)
 
 
 class StringUtils:
```

### Comparing `weathon-0.0.0.17/weathon/utils_/text_cluster.py` & `weathon-0.0.0.18/weathon/utils_/text_cluster.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/textrank.py` & `weathon-0.0.0.18/weathon/utils_/textrank.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/transformer_utils.py` & `weathon-0.0.0.18/weathon/utils_/transformer_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,16 @@
 import re
 import os
 import torch
 import logging
 import numpy as np
 from transformers import AutoModel, AutoTokenizer, BertTokenizer
 
-from weathon.utils import FileUtils
+from weathon.dl.utils import FileUtils
+from weathon.dl.utils.fileio.file_utils import ensure_directory
 
 logger = logging.getLogger(__name__)
 
 
 class TransformerUtils:
     @staticmethod
     def recover_bert_token(token: str) -> str:
@@ -32,15 +33,15 @@
         """
         1. 下载可能会失败，重试即可
         2. 程序会缓存之前下载过的内容
         Examples:
             TransformerUtils.download_from_huggingface('clue/albert_chinese_small','/data/lizhen/pretrained_models')
         """
         path = os.path.join(root_path, model_name)
-        FileUtils.ensure_dir(path)
+        ensure_directory(path)
         try:
             tokenizer = AutoTokenizer.from_pretrained(model_name)
         except Exception as e:
             tokenizer = BertTokenizer.from_pretrained(model_name)
         tokenizer.save_pretrained(path)
 
         model = AutoModel.from_pretrained(model_name)
```

### Comparing `weathon-0.0.0.17/weathon/utils_/union_find.py` & `weathon-0.0.0.18/weathon/utils/union_find.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/wav_note.py` & `weathon-0.0.0.18/weathon/utils_/wav_note.py`

 * *Files 20% similar despite different names*

```diff
@@ -3,23 +3,17 @@
 # @Author  : LiZhen
 # @FileName: wav_note.py
 # @github  : https://github.com/Lizhen0628
 # @Description:
 import os
 from pathlib import Path
 
-from weathon.utils import FileUtils
-
-
-
-
-
-
+from weathon.dl.utils.fileio.file_utils import ensure_directory
 
 
 class WavNote:
     """音频转乐谱"""
 
     def __init__(self, wav_file, note_file):
-        self.record_dir = FileUtils.ensure_dir(Path(os.environ["DATA_DIR"]) / "weathon" / "record_wav")
-        self.note_dir = FileUtils.ensure_dir(Path(os.environ["DATA_DIR"]) / "weathon" / "melody_note")
+        self.record_dir = ensure_directory(Path(os.environ["DATA_DIR"]) / "weathon" / "record_wav")
+        self.note_dir = ensure_directory(Path(os.environ["DATA_DIR"]) / "weathon" / "melody_note")
```

### Comparing `weathon-0.0.0.17/weathon/utils_/wav_utils.py` & `weathon-0.0.0.18/weathon/utils_/wav_utils.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/word_discover.py` & `weathon-0.0.0.18/weathon/utils_/word_discover.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon/utils_/word_finder.py` & `weathon-0.0.0.18/weathon/utils_/word_finder.py`

 * *Files identical despite different names*

### Comparing `weathon-0.0.0.17/weathon.egg-info/PKG-INFO` & `weathon-0.0.0.18/weathon.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: weathon
-Version: 0.0.0.17
+Version: 0.0.0.18
 Summary: weathon: a personal Weapon Depot for python, so called weathon.
 Home-page: https://github.com/LiZhen0628
 Author: LiZhen
 Author-email: 16621660628@163.com
 License: UNKNOWN
 Description: # weathon_package
         a personal Weapon Depot for python, so called weathon.
```

