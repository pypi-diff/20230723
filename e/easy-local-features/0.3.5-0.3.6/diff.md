# Comparing `tmp/easy_local_features-0.3.5.tar.gz` & `tmp/easy_local_features-0.3.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "easy_local_features-0.3.5.tar", last modified: Sun Jul 23 02:13:36 2023, max compression
+gzip compressed data, was "easy_local_features-0.3.6.tar", last modified: Sun Jul 23 02:33:34 2023, max compression
```

## Comparing `easy_local_features-0.3.5.tar` & `easy_local_features-0.3.6.tar`

### file list

```diff
@@ -1,105 +1,105 @@
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.353920 easy_local_features-0.3.5/
--rw-r--r--   0 cadar      (501) staff       (20)     1520 2023-07-22 09:17:15.000000 easy_local_features-0.3.5/LICENSE_ALIKED.txt
--rw-r--r--   0 cadar      (501) staff       (20)    32722 2023-07-01 15:16:15.000000 easy_local_features-0.3.5/LICENSE_DISK.txt
--rw-r--r--   0 cadar      (501) staff       (20)    21121 2023-07-01 17:04:24.000000 easy_local_features-0.3.5/LICENSE_R2D2.txt
--rw-r--r--   0 cadar      (501) staff       (20)     7009 2023-07-01 16:24:52.000000 easy_local_features-0.3.5/LICENSE_SUPERGLUE.txt
--rw-r--r--   0 cadar      (501) staff       (20)     2312 2023-07-23 02:13:36.353597 easy_local_features-0.3.5/PKG-INFO
--rw-r--r--   0 cadar      (501) staff       (20)     2027 2023-07-23 02:13:11.000000 easy_local_features-0.3.5/README.md
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.313680 easy_local_features-0.3.5/easy_local_features/
--rw-r--r--   0 cadar      (501) staff       (20)        1 2023-07-01 15:35:14.000000 easy_local_features-0.3.5/easy_local_features/__init__.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.319564 easy_local_features-0.3.5/easy_local_features/datasets/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-06-12 19:58:13.000000 easy_local_features-0.3.5/easy_local_features/datasets/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)    10688 2023-07-11 20:37:33.000000 easy_local_features-0.3.5/easy_local_features/datasets/augmentor.py
--rw-r--r--   0 cadar      (501) staff       (20)     3034 2023-06-12 19:58:13.000000 easy_local_features-0.3.5/easy_local_features/datasets/download.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.323419 easy_local_features-0.3.5/easy_local_features/feature/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/feature/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     3774 2023-07-23 02:12:15.000000 easy_local_features-0.3.5/easy_local_features/feature/baseline_aliked.py
--rw-r--r--   0 cadar      (501) staff       (20)    34684 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/feature/baseline_dalf.py
--rw-r--r--   0 cadar      (501) staff       (20)     2624 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/feature/baseline_deal.py
--rw-r--r--   0 cadar      (501) staff       (20)     6746 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/feature/baseline_disk.py
--rw-r--r--   0 cadar      (501) staff       (20)     6012 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/feature/baseline_r2d2.py
--rw-r--r--   0 cadar      (501) staff       (20)     2857 2023-07-23 01:46:09.000000 easy_local_features-0.3.5/easy_local_features/feature/baseline_superpoint.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.326147 easy_local_features-0.3.5/easy_local_features/matching/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-04 21:59:23.000000 easy_local_features-0.3.5/easy_local_features/matching/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     2103 2023-07-04 22:47:59.000000 easy_local_features-0.3.5/easy_local_features/matching/baseline_loftr.py
--rw-r--r--   0 cadar      (501) staff       (20)     5116 2023-07-01 16:48:02.000000 easy_local_features-0.3.5/easy_local_features/matching/baseline_superglue.py
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-04 22:06:22.000000 easy_local_features-0.3.5/easy_local_features/matching/core.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.326395 easy_local_features-0.3.5/easy_local_features/submodules/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 15:42:35.000000 easy_local_features-0.3.5/easy_local_features/submodules/__init__.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.326645 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-22 08:58:42.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/__init__.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.327988 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/custom_ops/
--rw-r--r--   0 cadar      (501) staff       (20)     5503 2023-07-23 02:07:54.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/custom_ops/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)      599 2023-07-22 11:59:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/custom_ops/setup.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.330195 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-22 08:58:50.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     7454 2023-07-23 02:06:58.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/aliked.py
--rw-r--r--   0 cadar      (501) staff       (20)     9383 2023-07-22 12:01:18.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/blocks.py
--rw-r--r--   0 cadar      (501) staff       (20)      863 2023-07-22 08:46:52.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/padder.py
--rw-r--r--   0 cadar      (501) staff       (20)     8080 2023-07-22 08:46:52.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/soft_detect.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.330722 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 15:23:41.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/__init__.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.330962 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/
--rw-r--r--   0 cadar      (501) staff       (20)       24 2023-07-01 15:39:51.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/__init__.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.331656 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/common/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 15:40:58.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/common/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     2652 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/common/structs.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.333270 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/geom/
--rw-r--r--   0 cadar      (501) staff       (20)       79 2023-07-01 08:54:41.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/geom/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)      291 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/geom/distance_matrix.py
--rw-r--r--   0 cadar      (501) staff       (20)     2096 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/geom/epi.py
--rw-r--r--   0 cadar      (501) staff       (20)     3406 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/geom/pose.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.335869 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/
--rw-r--r--   0 cadar      (501) staff       (20)      113 2023-07-01 08:54:41.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     2732 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/consistent_matcher.py
--rw-r--r--   0 cadar      (501) staff       (20)     2566 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/cycle_matcher.py
--rw-r--r--   0 cadar      (501) staff       (20)     5454 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/detector.py
--rw-r--r--   0 cadar      (501) staff       (20)     2177 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/disk.py
--rw-r--r--   0 cadar      (501) staff       (20)      865 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/nms.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.337661 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/
--rw-r--r--   0 cadar      (501) staff       (20)      249 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     4159 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/blocks.py
--rw-r--r--   0 cadar      (501) staff       (20)     2070 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/ops.py
--rw-r--r--   0 cadar      (501) staff       (20)     3289 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/unet.py
--rw-r--r--   0 cadar      (501) staff       (20)     1291 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/utils.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.339584 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:53:50.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     6223 2023-07-01 17:01:09.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/extract.py
--rw-r--r--   0 cadar      (501) staff       (20)     9927 2023-07-01 16:26:30.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/extract_kapture.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.342856 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:54:54.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     2360 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/ap_loss.py
--rw-r--r--   0 cadar      (501) staff       (20)     1720 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/losses.py
--rw-r--r--   0 cadar      (501) staff       (20)     7158 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/patchnet.py
--rw-r--r--   0 cadar      (501) staff       (20)     1760 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/reliability_loss.py
--rw-r--r--   0 cadar      (501) staff       (20)     2006 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/repeatability_loss.py
--rw-r--r--   0 cadar      (501) staff       (20)    15031 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/sampler.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.345611 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:54:23.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     1080 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/common.py
--rw-r--r--   0 cadar      (501) staff       (20)    14318 2023-07-01 17:00:44.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/dataloader.py
--rw-r--r--   0 cadar      (501) staff       (20)     2208 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/trainer.py
--rw-r--r--   0 cadar      (501) staff       (20)    18298 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/transforms.py
--rw-r--r--   0 cadar      (501) staff       (20)     7160 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/transforms_tools.py
--rw-r--r--   0 cadar      (501) staff       (20)     5647 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/viz.py
--rw-r--r--   0 cadar      (501) staff       (20)     5018 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/train.py
--rw-r--r--   0 cadar      (501) staff       (20)     4203 2023-07-01 16:26:31.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/viz_heatmaps.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.345933 easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:22:28.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/__init__.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.350958 easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:16:09.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)     3417 2023-07-01 16:16:09.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/matching.py
--rw-r--r--   0 cadar      (501) staff       (20)    11537 2023-07-01 16:40:16.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/superglue.py
--rw-r--r--   0 cadar      (501) staff       (20)     8092 2023-07-01 16:40:03.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/superpoint.py
--rw-r--r--   0 cadar      (501) staff       (20)    20039 2023-07-01 16:16:09.000000 easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/utils.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.352691 easy_local_features-0.3.5/easy_local_features/utils/
--rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/utils/__init__.py
--rw-r--r--   0 cadar      (501) staff       (20)      293 2023-07-11 16:38:37.000000 easy_local_features-0.3.5/easy_local_features/utils/generic_match.py
-drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:13:36.317762 easy_local_features-0.3.5/easy_local_features.egg-info/
--rw-r--r--   0 cadar      (501) staff       (20)     2312 2023-07-23 02:13:36.000000 easy_local_features-0.3.5/easy_local_features.egg-info/PKG-INFO
--rw-r--r--   0 cadar      (501) staff       (20)     4188 2023-07-23 02:13:36.000000 easy_local_features-0.3.5/easy_local_features.egg-info/SOURCES.txt
--rw-r--r--   0 cadar      (501) staff       (20)        1 2023-07-23 02:13:36.000000 easy_local_features-0.3.5/easy_local_features.egg-info/dependency_links.txt
--rw-r--r--   0 cadar      (501) staff       (20)       73 2023-07-23 02:13:36.000000 easy_local_features-0.3.5/easy_local_features.egg-info/requires.txt
--rw-r--r--   0 cadar      (501) staff       (20)       20 2023-07-23 02:13:36.000000 easy_local_features-0.3.5/easy_local_features.egg-info/top_level.txt
--rw-r--r--   0 cadar      (501) staff       (20)       38 2023-07-23 02:13:36.354041 easy_local_features-0.3.5/setup.cfg
--rw-r--r--   0 cadar      (501) staff       (20)     1703 2023-07-23 02:12:39.000000 easy_local_features-0.3.5/setup.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.061481 easy_local_features-0.3.6/
+-rw-r--r--   0 cadar      (501) staff       (20)     1520 2023-07-22 09:17:15.000000 easy_local_features-0.3.6/LICENSE_ALIKED.txt
+-rw-r--r--   0 cadar      (501) staff       (20)    32722 2023-07-01 15:16:15.000000 easy_local_features-0.3.6/LICENSE_DISK.txt
+-rw-r--r--   0 cadar      (501) staff       (20)    21121 2023-07-01 17:04:24.000000 easy_local_features-0.3.6/LICENSE_R2D2.txt
+-rw-r--r--   0 cadar      (501) staff       (20)     7009 2023-07-01 16:24:52.000000 easy_local_features-0.3.6/LICENSE_SUPERGLUE.txt
+-rw-r--r--   0 cadar      (501) staff       (20)     2545 2023-07-23 02:33:34.061238 easy_local_features-0.3.6/PKG-INFO
+-rw-r--r--   0 cadar      (501) staff       (20)     2260 2023-07-23 02:24:00.000000 easy_local_features-0.3.6/README.md
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.032258 easy_local_features-0.3.6/easy_local_features/
+-rw-r--r--   0 cadar      (501) staff       (20)        1 2023-07-01 15:35:14.000000 easy_local_features-0.3.6/easy_local_features/__init__.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.034945 easy_local_features-0.3.6/easy_local_features/datasets/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-06-12 19:58:13.000000 easy_local_features-0.3.6/easy_local_features/datasets/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)    10688 2023-07-11 20:37:33.000000 easy_local_features-0.3.6/easy_local_features/datasets/augmentor.py
+-rw-r--r--   0 cadar      (501) staff       (20)     3034 2023-06-12 19:58:13.000000 easy_local_features-0.3.6/easy_local_features/datasets/download.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.037694 easy_local_features-0.3.6/easy_local_features/feature/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/feature/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     3774 2023-07-23 02:12:15.000000 easy_local_features-0.3.6/easy_local_features/feature/baseline_aliked.py
+-rw-r--r--   0 cadar      (501) staff       (20)    34684 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/feature/baseline_dalf.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2624 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/feature/baseline_deal.py
+-rw-r--r--   0 cadar      (501) staff       (20)     6746 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/feature/baseline_disk.py
+-rw-r--r--   0 cadar      (501) staff       (20)     6012 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/feature/baseline_r2d2.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2857 2023-07-23 01:46:09.000000 easy_local_features-0.3.6/easy_local_features/feature/baseline_superpoint.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.038824 easy_local_features-0.3.6/easy_local_features/matching/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-04 21:59:23.000000 easy_local_features-0.3.6/easy_local_features/matching/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2075 2023-07-23 02:33:04.000000 easy_local_features-0.3.6/easy_local_features/matching/baseline_loftr.py
+-rw-r--r--   0 cadar      (501) staff       (20)     5144 2023-07-23 02:32:46.000000 easy_local_features-0.3.6/easy_local_features/matching/baseline_superglue.py
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-04 22:06:22.000000 easy_local_features-0.3.6/easy_local_features/matching/core.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.038994 easy_local_features-0.3.6/easy_local_features/submodules/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 15:42:35.000000 easy_local_features-0.3.6/easy_local_features/submodules/__init__.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.039160 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-22 08:58:42.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/__init__.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.039755 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/custom_ops/
+-rw-r--r--   0 cadar      (501) staff       (20)     5503 2023-07-23 02:07:54.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/custom_ops/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)      599 2023-07-22 11:59:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/custom_ops/setup.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.042454 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-22 08:58:50.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     7454 2023-07-23 02:06:58.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/aliked.py
+-rw-r--r--   0 cadar      (501) staff       (20)     9383 2023-07-22 12:01:18.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/blocks.py
+-rw-r--r--   0 cadar      (501) staff       (20)      863 2023-07-22 08:46:52.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/padder.py
+-rw-r--r--   0 cadar      (501) staff       (20)     8080 2023-07-22 08:46:52.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/soft_detect.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.043023 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 15:23:41.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/__init__.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.043288 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/
+-rw-r--r--   0 cadar      (501) staff       (20)       24 2023-07-01 15:39:51.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/__init__.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.043946 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/common/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 15:40:58.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/common/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2652 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/common/structs.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.045186 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/geom/
+-rw-r--r--   0 cadar      (501) staff       (20)       79 2023-07-01 08:54:41.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/geom/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)      291 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/geom/distance_matrix.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2096 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/geom/epi.py
+-rw-r--r--   0 cadar      (501) staff       (20)     3406 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/geom/pose.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.046981 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/
+-rw-r--r--   0 cadar      (501) staff       (20)      113 2023-07-01 08:54:41.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2732 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/consistent_matcher.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2566 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/cycle_matcher.py
+-rw-r--r--   0 cadar      (501) staff       (20)     5454 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/detector.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2177 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/disk.py
+-rw-r--r--   0 cadar      (501) staff       (20)      865 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/nms.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.049264 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/
+-rw-r--r--   0 cadar      (501) staff       (20)      249 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     4159 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/blocks.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2070 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/ops.py
+-rw-r--r--   0 cadar      (501) staff       (20)     3289 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/unet.py
+-rw-r--r--   0 cadar      (501) staff       (20)     1291 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/utils.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.051344 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:53:50.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     6223 2023-07-01 17:01:09.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/extract.py
+-rw-r--r--   0 cadar      (501) staff       (20)     9927 2023-07-01 16:26:30.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/extract_kapture.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.053940 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:54:54.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2360 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/ap_loss.py
+-rw-r--r--   0 cadar      (501) staff       (20)     1720 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/losses.py
+-rw-r--r--   0 cadar      (501) staff       (20)     7158 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/patchnet.py
+-rw-r--r--   0 cadar      (501) staff       (20)     1760 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/reliability_loss.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2006 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/repeatability_loss.py
+-rw-r--r--   0 cadar      (501) staff       (20)    15031 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/sampler.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.056249 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:54:23.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     1080 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/common.py
+-rw-r--r--   0 cadar      (501) staff       (20)    14318 2023-07-01 17:00:44.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/dataloader.py
+-rw-r--r--   0 cadar      (501) staff       (20)     2208 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/trainer.py
+-rw-r--r--   0 cadar      (501) staff       (20)    18298 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/transforms.py
+-rw-r--r--   0 cadar      (501) staff       (20)     7160 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/transforms_tools.py
+-rw-r--r--   0 cadar      (501) staff       (20)     5647 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/viz.py
+-rw-r--r--   0 cadar      (501) staff       (20)     5018 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/train.py
+-rw-r--r--   0 cadar      (501) staff       (20)     4203 2023-07-01 16:26:31.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/viz_heatmaps.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.056511 easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:22:28.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/__init__.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.059843 easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-01 16:16:09.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)     3417 2023-07-01 16:16:09.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/matching.py
+-rw-r--r--   0 cadar      (501) staff       (20)    11537 2023-07-01 16:40:16.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/superglue.py
+-rw-r--r--   0 cadar      (501) staff       (20)     8092 2023-07-01 16:40:03.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/superpoint.py
+-rw-r--r--   0 cadar      (501) staff       (20)    20039 2023-07-01 16:16:09.000000 easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/utils.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.060768 easy_local_features-0.3.6/easy_local_features/utils/
+-rw-r--r--   0 cadar      (501) staff       (20)        0 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/utils/__init__.py
+-rw-r--r--   0 cadar      (501) staff       (20)      293 2023-07-11 16:38:37.000000 easy_local_features-0.3.6/easy_local_features/utils/generic_match.py
+drwxr-xr-x   0 cadar      (501) staff       (20)        0 2023-07-23 02:33:34.033716 easy_local_features-0.3.6/easy_local_features.egg-info/
+-rw-r--r--   0 cadar      (501) staff       (20)     2545 2023-07-23 02:33:33.000000 easy_local_features-0.3.6/easy_local_features.egg-info/PKG-INFO
+-rw-r--r--   0 cadar      (501) staff       (20)     4188 2023-07-23 02:33:33.000000 easy_local_features-0.3.6/easy_local_features.egg-info/SOURCES.txt
+-rw-r--r--   0 cadar      (501) staff       (20)        1 2023-07-23 02:33:33.000000 easy_local_features-0.3.6/easy_local_features.egg-info/dependency_links.txt
+-rw-r--r--   0 cadar      (501) staff       (20)       73 2023-07-23 02:33:33.000000 easy_local_features-0.3.6/easy_local_features.egg-info/requires.txt
+-rw-r--r--   0 cadar      (501) staff       (20)       20 2023-07-23 02:33:33.000000 easy_local_features-0.3.6/easy_local_features.egg-info/top_level.txt
+-rw-r--r--   0 cadar      (501) staff       (20)       38 2023-07-23 02:33:34.061551 easy_local_features-0.3.6/setup.cfg
+-rw-r--r--   0 cadar      (501) staff       (20)     1703 2023-07-23 02:33:15.000000 easy_local_features-0.3.6/setup.py
```

### Comparing `easy_local_features-0.3.5/LICENSE_ALIKED.txt` & `easy_local_features-0.3.6/LICENSE_ALIKED.txt`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/LICENSE_DISK.txt` & `easy_local_features-0.3.6/LICENSE_DISK.txt`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/LICENSE_R2D2.txt` & `easy_local_features-0.3.6/LICENSE_R2D2.txt`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/LICENSE_SUPERGLUE.txt` & `easy_local_features-0.3.6/LICENSE_SUPERGLUE.txt`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/PKG-INFO` & `easy_local_features-0.3.6/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,37 +1,46 @@
 Metadata-Version: 2.1
 Name: easy_local_features
-Version: 0.3.5
+Version: 0.3.6
 Author: eucadar
 Author-email: python@eucadar.com
 Description-Content-Type: text/markdown
 License-File: LICENSE_ALIKED.txt
 License-File: LICENSE_DISK.txt
 License-File: LICENSE_R2D2.txt
 License-File: LICENSE_SUPERGLUE.txt
 
 # easy-local-features-baselines
 
 Just some scripts to make things easier for the local features baselines.
 
 # Installation
 
+```bash
+# make sure you have torch installed
+# pip install torch torchvision
+pip install easy-local-features
+```
+
+## Installing from source
+
+You may want to install from source if you want to modify the code or if you want to use the latest version. To do so, you can clone this repository and install the requirements.
 
 I suggest using a conda environment to install the requirements. You can create one using the following command.
 
 ```bash
 conda create -n elf python=3.9 # the python version is not so critical, but I used 3.9.
 conda activate elf
 ```
 
-Now we can insall the requirements using pip.
+Now we can install everything.
 
 ```bash
 pip install -r requirements.txt
-pip install .
+pip install -e .
 ```
 
 # How to use
 
 ```python
 from easy_local_features.feature.baseline_deal import DEAL_baseline
 # from easy_local_features.feature.baseline_dalf import DALF_baseline
@@ -58,24 +67,21 @@
   - The idea is to have a class that can match images using any local feature extractor and any matching method.
 - [ ] Fix requirements to install automatically with the package (maybe)
 - [ ] Add a script to download some datasets
 - [ ] Add a download script for the pretrained models
 - [ ] Add more baselines :)
   - [x] DEAL
     - [ ] Add LICENSE file
+  - [x] DALF
+    - [ ] Add LICENSE file
+  - [ ] DKM
+  - [ ] ASLFeat
   - [x] R2D2
   - [x] DISK
   - [x] SuperPoin
   - [x] SuperGlue
-  - [x] DALF
-    - [ ] Add LICENSE file
-  - [ ] ASLFeat
   - [x] LoFTR
-    - [ ] Add LICENSE file
-  - [ ] DKM
   - [ ] ALIKED
-    - NOT WORKING ON MAC M1
-    - [X] Add code 
-    - [X] Add LICENSE file
-    - [X] Test on MAC M1 with CPU
+    - [x] Add LICENSE file
+    - [x] Test on MAC M1 with CPU
     - [ ] Test on Linux with CPU
-    - [x] Test with CUDA
+    - [ ] Test with CUDA
```

### Comparing `easy_local_features-0.3.5/README.md` & `easy_local_features-0.3.6/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -1,26 +1,35 @@
 # easy-local-features-baselines
 
 Just some scripts to make things easier for the local features baselines.
 
 # Installation
 
+```bash
+# make sure you have torch installed
+# pip install torch torchvision
+pip install easy-local-features
+```
+
+## Installing from source
+
+You may want to install from source if you want to modify the code or if you want to use the latest version. To do so, you can clone this repository and install the requirements.
 
 I suggest using a conda environment to install the requirements. You can create one using the following command.
 
 ```bash
 conda create -n elf python=3.9 # the python version is not so critical, but I used 3.9.
 conda activate elf
 ```
 
-Now we can insall the requirements using pip.
+Now we can install everything.
 
 ```bash
 pip install -r requirements.txt
-pip install .
+pip install -e .
 ```
 
 # How to use
 
 ```python
 from easy_local_features.feature.baseline_deal import DEAL_baseline
 # from easy_local_features.feature.baseline_dalf import DALF_baseline
@@ -47,24 +56,21 @@
   - The idea is to have a class that can match images using any local feature extractor and any matching method.
 - [ ] Fix requirements to install automatically with the package (maybe)
 - [ ] Add a script to download some datasets
 - [ ] Add a download script for the pretrained models
 - [ ] Add more baselines :)
   - [x] DEAL
     - [ ] Add LICENSE file
+  - [x] DALF
+    - [ ] Add LICENSE file
+  - [ ] DKM
+  - [ ] ASLFeat
   - [x] R2D2
   - [x] DISK
   - [x] SuperPoin
   - [x] SuperGlue
-  - [x] DALF
-    - [ ] Add LICENSE file
-  - [ ] ASLFeat
   - [x] LoFTR
-    - [ ] Add LICENSE file
-  - [ ] DKM
   - [ ] ALIKED
-    - NOT WORKING ON MAC M1
-    - [X] Add code 
-    - [X] Add LICENSE file
-    - [X] Test on MAC M1 with CPU
+    - [x] Add LICENSE file
+    - [x] Test on MAC M1 with CPU
     - [ ] Test on Linux with CPU
-    - [x] Test with CUDA
+    - [ ] Test with CUDA
```

### Comparing `easy_local_features-0.3.5/easy_local_features/datasets/augmentor.py` & `easy_local_features-0.3.6/easy_local_features/datasets/augmentor.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/datasets/download.py` & `easy_local_features-0.3.6/easy_local_features/datasets/download.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/feature/baseline_aliked.py` & `easy_local_features-0.3.6/easy_local_features/feature/baseline_aliked.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/feature/baseline_dalf.py` & `easy_local_features-0.3.6/easy_local_features/feature/baseline_dalf.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/feature/baseline_deal.py` & `easy_local_features-0.3.6/easy_local_features/feature/baseline_deal.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/feature/baseline_disk.py` & `easy_local_features-0.3.6/easy_local_features/feature/baseline_disk.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/feature/baseline_r2d2.py` & `easy_local_features-0.3.6/easy_local_features/feature/baseline_r2d2.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/feature/baseline_superpoint.py` & `easy_local_features-0.3.6/easy_local_features/feature/baseline_superpoint.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/matching/baseline_loftr.py` & `easy_local_features-0.3.6/easy_local_features/matching/baseline_loftr.py`

 * *Files 5% similar despite different names*

```diff
@@ -66,9 +66,8 @@
     img = cv2.imread(str(root / "assets" / "notredame.png"))
 
     img = cv2.resize(img, (0,0), fx=0.2, fy=0.2)
 
 
     matcher = LoFTR_baseline()
     res = matcher.match(img, img)
-
-    import pdb; pdb.set_trace()
+
```

### Comparing `easy_local_features-0.3.5/easy_local_features/matching/baseline_superglue.py` & `easy_local_features-0.3.6/easy_local_features/matching/baseline_superglue.py`

 * *Files 2% similar despite different names*

```diff
@@ -105,15 +105,15 @@
         matches1to2 = [cv2.DMatch(i,j,1/s) for i,[j,s] in enumerate(zip(matches0, matching_scores0))]
         matches2to1 = [cv2.DMatch(i,j,1/s) for i,[j,s] in enumerate(zip(matches1, matching_scores1))]
 
         return matches1to2, matches2to1
 
 if __name__ == "__main__":
     import pdb
-    from baseline_superpoint import SuperPoint_baseline
+    from easy_local_features.feature.baseline_superpoint import SuperPoint_baseline
 
     img = cv2.imread(str(root / "assets" / "notredame.png"))
     extractor = SuperPoint_baseline()
     matcher = SuperGlue_baseline()
 
     keypoints0, descriptors0 = extractor.detectAndCompute(img)
```

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/custom_ops/__init__.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/custom_ops/__init__.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/custom_ops/setup.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/custom_ops/setup.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/aliked.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/aliked.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/blocks.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/blocks.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/padder.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/padder.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_aliked/nets/soft_detect.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_aliked/nets/soft_detect.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/common/structs.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/common/structs.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/geom/epi.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/geom/epi.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/geom/pose.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/geom/pose.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/consistent_matcher.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/consistent_matcher.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/cycle_matcher.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/cycle_matcher.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/detector.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/detector.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/disk.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/disk.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/model/nms.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/model/nms.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/blocks.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/blocks.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/ops.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/ops.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/unet.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/unet.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_disk/disk/unets/utils.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_disk/disk/unets/utils.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/extract.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/extract.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/extract_kapture.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/extract_kapture.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/ap_loss.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/ap_loss.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/losses.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/losses.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/patchnet.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/patchnet.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/reliability_loss.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/reliability_loss.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/repeatability_loss.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/repeatability_loss.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/nets/sampler.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/nets/sampler.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/common.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/common.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/dataloader.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/dataloader.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/trainer.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/trainer.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/transforms.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/transforms.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/transforms_tools.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/transforms_tools.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/tools/viz.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/tools/viz.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/train.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/train.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_r2d2/viz_heatmaps.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_r2d2/viz_heatmaps.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/matching.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/matching.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/superglue.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/superglue.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/superpoint.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/superpoint.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features/submodules/git_superglue/models/utils.py` & `easy_local_features-0.3.6/easy_local_features/submodules/git_superglue/models/utils.py`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/easy_local_features.egg-info/PKG-INFO` & `easy_local_features-0.3.6/easy_local_features.egg-info/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,37 +1,46 @@
 Metadata-Version: 2.1
 Name: easy-local-features
-Version: 0.3.5
+Version: 0.3.6
 Author: eucadar
 Author-email: python@eucadar.com
 Description-Content-Type: text/markdown
 License-File: LICENSE_ALIKED.txt
 License-File: LICENSE_DISK.txt
 License-File: LICENSE_R2D2.txt
 License-File: LICENSE_SUPERGLUE.txt
 
 # easy-local-features-baselines
 
 Just some scripts to make things easier for the local features baselines.
 
 # Installation
 
+```bash
+# make sure you have torch installed
+# pip install torch torchvision
+pip install easy-local-features
+```
+
+## Installing from source
+
+You may want to install from source if you want to modify the code or if you want to use the latest version. To do so, you can clone this repository and install the requirements.
 
 I suggest using a conda environment to install the requirements. You can create one using the following command.
 
 ```bash
 conda create -n elf python=3.9 # the python version is not so critical, but I used 3.9.
 conda activate elf
 ```
 
-Now we can insall the requirements using pip.
+Now we can install everything.
 
 ```bash
 pip install -r requirements.txt
-pip install .
+pip install -e .
 ```
 
 # How to use
 
 ```python
 from easy_local_features.feature.baseline_deal import DEAL_baseline
 # from easy_local_features.feature.baseline_dalf import DALF_baseline
@@ -58,24 +67,21 @@
   - The idea is to have a class that can match images using any local feature extractor and any matching method.
 - [ ] Fix requirements to install automatically with the package (maybe)
 - [ ] Add a script to download some datasets
 - [ ] Add a download script for the pretrained models
 - [ ] Add more baselines :)
   - [x] DEAL
     - [ ] Add LICENSE file
+  - [x] DALF
+    - [ ] Add LICENSE file
+  - [ ] DKM
+  - [ ] ASLFeat
   - [x] R2D2
   - [x] DISK
   - [x] SuperPoin
   - [x] SuperGlue
-  - [x] DALF
-    - [ ] Add LICENSE file
-  - [ ] ASLFeat
   - [x] LoFTR
-    - [ ] Add LICENSE file
-  - [ ] DKM
   - [ ] ALIKED
-    - NOT WORKING ON MAC M1
-    - [X] Add code 
-    - [X] Add LICENSE file
-    - [X] Test on MAC M1 with CPU
+    - [x] Add LICENSE file
+    - [x] Test on MAC M1 with CPU
     - [ ] Test on Linux with CPU
-    - [x] Test with CUDA
+    - [ ] Test with CUDA
```

### Comparing `easy_local_features-0.3.5/easy_local_features.egg-info/SOURCES.txt` & `easy_local_features-0.3.6/easy_local_features.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `easy_local_features-0.3.5/setup.py` & `easy_local_features-0.3.6/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -31,15 +31,15 @@
                 name='easy_local_features.submodules.git_aliked.custom_ops.get_patches', 
                 sources=[CUSTOM_OPS+'get_patches_cpu.cpp']
             )
         ]
 
 setup(
     name='easy_local_features',
-    version='0.3.5',
+    version='0.3.6',
     author='eucadar',
     author_email='python@eucadar.com',
     packages=find_packages(exclude=('tests', 'docs', 'assets', 'custom_ops')),
     include_package_data=True,
     install_requires=[
         'numpy',
         'scipy',
```

