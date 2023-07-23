# Comparing `tmp/iman-0.0.90.tar.gz` & `tmp/iman-0.0.91.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\iman-0.0.90.tar", last modified: Sun Jul 23 08:02:45 2023, max compression
+gzip compressed data, was "dist\iman-0.0.91.tar", last modified: Sun Jul 23 08:03:53 2023, max compression
```

## Comparing `iman-0.0.90.tar` & `iman-0.0.91.tar`

### file list

```diff
@@ -1,79 +1,79 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:45.000000 iman-0.0.90/
--rw-rw-rw-   0        0        0     6772 2023-07-23 08:02:45.000000 iman-0.0.90/PKG-INFO
--rw-rw-rw-   0        0        0     6398 2023-07-23 08:01:53.000000 iman-0.0.90/README.rst
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:44.000000 iman-0.0.90/iman/
--rw-rw-rw-   0        0        0     2070 2022-12-25 10:45:05.000000 iman-0.0.90/iman/AUG.py
--rw-rw-rw-   0        0        0    17314 2023-07-16 08:57:47.000000 iman-0.0.90/iman/Audio.py
--rw-rw-rw-   0        0        0      124 2023-01-29 08:15:58.000000 iman-0.0.90/iman/Boors.py
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:44.000000 iman-0.0.90/iman/Features/
--rw-rw-rw-   0        0        0       42 2022-11-13 07:01:23.000000 iman-0.0.90/iman/Features/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:44.000000 iman-0.0.90/iman/Features/mfcc/
--rw-rw-rw-   0        0        0     2836 2022-11-13 07:05:02.000000 iman-0.0.90/iman/Features/mfcc/LS.py
--rw-rw-rw-   0        0        0      604 2022-12-12 11:32:38.000000 iman-0.0.90/iman/Features/mfcc/SB.py
--rw-rw-rw-   0        0        0        0 2022-11-13 06:42:54.000000 iman-0.0.90/iman/Features/mfcc/__init__.py
--rw-rw-rw-   0        0        0    11080 2021-12-01 10:31:39.000000 iman-0.0.90/iman/Features/mfcc/getmfcc_from_librosa.py
--rw-rw-rw-   0        0        0    41655 2022-12-12 11:33:13.000000 iman-0.0.90/iman/Features/mfcc/sb_mfcc_class.py
--rw-rw-rw-   0        0        0     1057 2022-12-25 10:05:56.000000 iman-0.0.90/iman/Image.py
--rw-rw-rw-   0        0        0      815 2022-12-20 06:25:42.000000 iman-0.0.90/iman/Report.py
--rw-rw-rw-   0        0        0     2640 2023-02-20 05:13:55.000000 iman-0.0.90/iman/Text.py
--rw-rw-rw-   0        0        0     4478 2023-07-22 04:52:36.000000 iman-0.0.90/iman/__init__.py
--rw-rw-rw-   0        0        0      686 2022-12-17 11:18:42.000000 iman-0.0.90/iman/examples.py
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:44.000000 iman-0.0.90/iman/examples_folder/
--rw-rw-rw-   0        0        0        0 2022-12-17 11:24:05.000000 iman-0.0.90/iman/examples_folder/__init__.py
--rw-rw-rw-   0        0        0      539 2023-01-01 11:18:41.000000 iman-0.0.90/iman/examples_folder/age.py
--rw-rw-rw-   0        0        0      100 2023-01-01 05:01:21.000000 iman-0.0.90/iman/examples_folder/ffmpeg.py
--rw-rw-rw-   0        0        0      490 2022-12-17 09:55:52.000000 iman-0.0.90/iman/examples_folder/flask.py
--rw-rw-rw-   0        0        0      262 2021-01-05 11:07:03.000000 iman-0.0.90/iman/examples_folder/gpu_allocate_tf.py
--rw-rw-rw-   0        0        0      299 2022-12-31 09:42:30.000000 iman-0.0.90/iman/examples_folder/graphviz_chart.py
--rw-rw-rw-   0        0        0      345 2022-12-17 11:09:10.000000 iman-0.0.90/iman/examples_folder/parallel.py
--rw-rw-rw-   0        0        0      217 2022-12-17 11:12:20.000000 iman-0.0.90/iman/examples_folder/post_by_python.py
--rw-rw-rw-   0        0        0      775 2019-12-03 03:31:26.000000 iman-0.0.90/iman/examples_folder/pyworldd.py
--rw-rw-rw-   0        0        0      406 2022-12-05 05:24:04.000000 iman-0.0.90/iman/examples_folder/queue_worker.py
--rw-rw-rw-   0        0        0     1607 2021-11-28 10:10:27.000000 iman-0.0.90/iman/examples_folder/save_docx.py
--rw-rw-rw-   0        0        0      478 2019-05-05 06:27:38.000000 iman-0.0.90/iman/examples_folder/stft_test.py
--rw-rw-rw-   0        0        0      276 2019-11-19 00:37:16.000000 iman-0.0.90/iman/examples_folder/threading_example.py
--rw-rw-rw-   0        0        0      454 2021-05-25 08:55:10.000000 iman-0.0.90/iman/examples_folder/wikipedia.py
--rw-rw-rw-   0        0        0    15323 2022-11-06 10:39:16.000000 iman-0.0.90/iman/gpu_info.py
--rw-rw-rw-   0        0        0     1862 2022-11-12 05:34:50.000000 iman-0.0.90/iman/info.py
--rw-rw-rw-   0        0        0      318 2022-11-08 10:24:41.000000 iman-0.0.90/iman/matlab.py
--rw-rw-rw-   0        0        0     3422 2022-12-26 10:35:15.000000 iman-0.0.90/iman/metrics.py
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:44.000000 iman-0.0.90/iman/num2fa/
--rw-rw-rw-   0        0        0     8938 2023-01-28 05:46:54.000000 iman-0.0.90/iman/num2fa/__init__.py
--rw-rw-rw-   0        0        0      506 2023-01-28 05:46:54.000000 iman-0.0.90/iman/num2fa/__main__.py
--rw-rw-rw-   0        0        0      237 2022-12-19 06:23:20.000000 iman-0.0.90/iman/par.py
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:44.000000 iman-0.0.90/iman/pyctcdecode/
--rw-rw-rw-   0        0        0      265 2023-07-11 05:28:53.000000 iman-0.0.90/iman/pyctcdecode/__init__.py
--rw-rw-rw-   0        0        0     6186 2023-07-11 05:28:53.000000 iman-0.0.90/iman/pyctcdecode/alphabet.py
--rw-rw-rw-   0        0        0      617 2023-07-11 05:28:53.000000 iman-0.0.90/iman/pyctcdecode/constants.py
--rw-rw-rw-   0        0        0    29784 2023-07-19 12:40:28.000000 iman-0.0.90/iman/pyctcdecode/decoder.py
--rw-rw-rw-   0        0        0    11420 2023-07-11 05:28:53.000000 iman-0.0.90/iman/pyctcdecode/language_model.py
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:45.000000 iman-0.0.90/iman/sad_tf/
--rw-rw-rw-   0        0        0      101 2023-07-23 07:12:34.000000 iman-0.0.90/iman/sad_tf/__init__.py
--rw-rw-rw-   0        0        0     5614 2023-07-17 06:10:42.000000 iman-0.0.90/iman/sad_tf/export_funcs.py
--rw-rw-rw-   0        0        0     2221 2023-07-05 11:06:11.000000 iman-0.0.90/iman/sad_tf/features.py
--rw-rw-rw-   0        0        0    18972 2023-07-23 07:08:02.000000 iman-0.0.90/iman/sad_tf/segmenter.py
--rw-rw-rw-   0        0        0    20025 2023-07-23 07:56:09.000000 iman-0.0.90/iman/sad_tf/segmentero.py
--rw-rw-rw-   0        0        0    13783 2022-11-30 10:00:38.000000 iman-0.0.90/iman/sad_tf/sidekit_mfcc.py
--rw-rw-rw-   0        0        0      553 2022-01-12 05:39:10.000000 iman-0.0.90/iman/sad_tf/thread_returning.py
--rw-rw-rw-   0        0        0     7808 2022-01-12 05:39:09.000000 iman-0.0.90/iman/sad_tf/viterbi.py
--rw-rw-rw-   0        0        0     1755 2022-01-12 05:39:10.000000 iman-0.0.90/iman/sad_tf/viterbi_utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:45.000000 iman-0.0.90/iman/sad_torch_mfcc/
--rw-rw-rw-   0        0        0      107 2022-12-26 10:21:43.000000 iman-0.0.90/iman/sad_torch_mfcc/__init__.py
--rw-rw-rw-   0        0        0     4645 2022-12-11 08:33:44.000000 iman-0.0.90/iman/sad_torch_mfcc/export_funcs.py
--rw-rw-rw-   0        0        0     2002 2023-07-05 11:08:54.000000 iman-0.0.90/iman/sad_torch_mfcc/features.py
--rw-rw-rw-   0        0        0     3098 2022-12-11 08:39:59.000000 iman-0.0.90/iman/sad_torch_mfcc/sad_model.py
--rw-rw-rw-   0        0        0    19324 2023-07-22 04:57:05.000000 iman-0.0.90/iman/sad_torch_mfcc/segmenter.py
--rw-rw-rw-   0        0        0      553 2022-01-12 05:39:10.000000 iman-0.0.90/iman/sad_torch_mfcc/thread_returning.py
--rw-rw-rw-   0        0        0     7808 2022-01-12 05:39:09.000000 iman-0.0.90/iman/sad_torch_mfcc/viterbi.py
--rw-rw-rw-   0        0        0     1755 2022-01-12 05:39:10.000000 iman-0.0.90/iman/sad_torch_mfcc/viterbi_utils.py
--rw-rw-rw-   0        0        0      422 2022-11-22 05:36:39.000000 iman-0.0.90/iman/tsne.py
--rw-rw-rw-   0        0        0     2234 2023-06-10 12:42:19.000000 iman-0.0.90/iman/web.py
--rw-rw-rw-   0        0        0     7159 2022-10-26 09:16:54.000000 iman-0.0.90/iman/xvector.py
-drwxrwxrwx   0        0        0        0 2023-07-23 08:02:44.000000 iman-0.0.90/iman.egg-info/
--rw-rw-rw-   0        0        0     6772 2023-07-23 08:02:43.000000 iman-0.0.90/iman.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1773 2023-07-23 08:02:43.000000 iman-0.0.90/iman.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 08:02:43.000000 iman-0.0.90/iman.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       34 2023-07-23 08:02:43.000000 iman-0.0.90/iman.egg-info/requires.txt
--rw-rw-rw-   0        0        0        5 2023-07-23 08:02:43.000000 iman-0.0.90/iman.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 08:02:45.000000 iman-0.0.90/setup.cfg
--rw-rw-rw-   0        0        0      903 2023-07-23 07:59:52.000000 iman-0.0.90/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:53.000000 iman-0.0.91/
+-rw-rw-rw-   0        0        0     6772 2023-07-23 08:03:53.000000 iman-0.0.91/PKG-INFO
+-rw-rw-rw-   0        0        0     6398 2023-07-23 08:01:53.000000 iman-0.0.91/README.rst
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:52.000000 iman-0.0.91/iman/
+-rw-rw-rw-   0        0        0     2070 2022-12-25 10:45:05.000000 iman-0.0.91/iman/AUG.py
+-rw-rw-rw-   0        0        0    17314 2023-07-16 08:57:47.000000 iman-0.0.91/iman/Audio.py
+-rw-rw-rw-   0        0        0      124 2023-01-29 08:15:58.000000 iman-0.0.91/iman/Boors.py
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:52.000000 iman-0.0.91/iman/Features/
+-rw-rw-rw-   0        0        0       42 2022-11-13 07:01:23.000000 iman-0.0.91/iman/Features/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:52.000000 iman-0.0.91/iman/Features/mfcc/
+-rw-rw-rw-   0        0        0     2836 2022-11-13 07:05:02.000000 iman-0.0.91/iman/Features/mfcc/LS.py
+-rw-rw-rw-   0        0        0      604 2022-12-12 11:32:38.000000 iman-0.0.91/iman/Features/mfcc/SB.py
+-rw-rw-rw-   0        0        0        0 2022-11-13 06:42:54.000000 iman-0.0.91/iman/Features/mfcc/__init__.py
+-rw-rw-rw-   0        0        0    11080 2021-12-01 10:31:39.000000 iman-0.0.91/iman/Features/mfcc/getmfcc_from_librosa.py
+-rw-rw-rw-   0        0        0    41655 2022-12-12 11:33:13.000000 iman-0.0.91/iman/Features/mfcc/sb_mfcc_class.py
+-rw-rw-rw-   0        0        0     1057 2022-12-25 10:05:56.000000 iman-0.0.91/iman/Image.py
+-rw-rw-rw-   0        0        0      815 2022-12-20 06:25:42.000000 iman-0.0.91/iman/Report.py
+-rw-rw-rw-   0        0        0     2640 2023-02-20 05:13:55.000000 iman-0.0.91/iman/Text.py
+-rw-rw-rw-   0        0        0     4478 2023-07-22 04:52:36.000000 iman-0.0.91/iman/__init__.py
+-rw-rw-rw-   0        0        0      686 2022-12-17 11:18:42.000000 iman-0.0.91/iman/examples.py
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:53.000000 iman-0.0.91/iman/examples_folder/
+-rw-rw-rw-   0        0        0        0 2022-12-17 11:24:05.000000 iman-0.0.91/iman/examples_folder/__init__.py
+-rw-rw-rw-   0        0        0      539 2023-01-01 11:18:41.000000 iman-0.0.91/iman/examples_folder/age.py
+-rw-rw-rw-   0        0        0      100 2023-01-01 05:01:21.000000 iman-0.0.91/iman/examples_folder/ffmpeg.py
+-rw-rw-rw-   0        0        0      490 2022-12-17 09:55:52.000000 iman-0.0.91/iman/examples_folder/flask.py
+-rw-rw-rw-   0        0        0      262 2021-01-05 11:07:03.000000 iman-0.0.91/iman/examples_folder/gpu_allocate_tf.py
+-rw-rw-rw-   0        0        0      299 2022-12-31 09:42:30.000000 iman-0.0.91/iman/examples_folder/graphviz_chart.py
+-rw-rw-rw-   0        0        0      345 2022-12-17 11:09:10.000000 iman-0.0.91/iman/examples_folder/parallel.py
+-rw-rw-rw-   0        0        0      217 2022-12-17 11:12:20.000000 iman-0.0.91/iman/examples_folder/post_by_python.py
+-rw-rw-rw-   0        0        0      775 2019-12-03 03:31:26.000000 iman-0.0.91/iman/examples_folder/pyworldd.py
+-rw-rw-rw-   0        0        0      406 2022-12-05 05:24:04.000000 iman-0.0.91/iman/examples_folder/queue_worker.py
+-rw-rw-rw-   0        0        0     1607 2021-11-28 10:10:27.000000 iman-0.0.91/iman/examples_folder/save_docx.py
+-rw-rw-rw-   0        0        0      478 2019-05-05 06:27:38.000000 iman-0.0.91/iman/examples_folder/stft_test.py
+-rw-rw-rw-   0        0        0      276 2019-11-19 00:37:16.000000 iman-0.0.91/iman/examples_folder/threading_example.py
+-rw-rw-rw-   0        0        0      454 2021-05-25 08:55:10.000000 iman-0.0.91/iman/examples_folder/wikipedia.py
+-rw-rw-rw-   0        0        0    15323 2022-11-06 10:39:16.000000 iman-0.0.91/iman/gpu_info.py
+-rw-rw-rw-   0        0        0     1862 2022-11-12 05:34:50.000000 iman-0.0.91/iman/info.py
+-rw-rw-rw-   0        0        0      318 2022-11-08 10:24:41.000000 iman-0.0.91/iman/matlab.py
+-rw-rw-rw-   0        0        0     3422 2022-12-26 10:35:15.000000 iman-0.0.91/iman/metrics.py
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:53.000000 iman-0.0.91/iman/num2fa/
+-rw-rw-rw-   0        0        0     8938 2023-01-28 05:46:54.000000 iman-0.0.91/iman/num2fa/__init__.py
+-rw-rw-rw-   0        0        0      506 2023-01-28 05:46:54.000000 iman-0.0.91/iman/num2fa/__main__.py
+-rw-rw-rw-   0        0        0      237 2022-12-19 06:23:20.000000 iman-0.0.91/iman/par.py
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:53.000000 iman-0.0.91/iman/pyctcdecode/
+-rw-rw-rw-   0        0        0      265 2023-07-11 05:28:53.000000 iman-0.0.91/iman/pyctcdecode/__init__.py
+-rw-rw-rw-   0        0        0     6186 2023-07-11 05:28:53.000000 iman-0.0.91/iman/pyctcdecode/alphabet.py
+-rw-rw-rw-   0        0        0      617 2023-07-11 05:28:53.000000 iman-0.0.91/iman/pyctcdecode/constants.py
+-rw-rw-rw-   0        0        0    29784 2023-07-19 12:40:28.000000 iman-0.0.91/iman/pyctcdecode/decoder.py
+-rw-rw-rw-   0        0        0    11420 2023-07-11 05:28:53.000000 iman-0.0.91/iman/pyctcdecode/language_model.py
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:53.000000 iman-0.0.91/iman/sad_tf/
+-rw-rw-rw-   0        0        0      101 2023-07-23 07:12:34.000000 iman-0.0.91/iman/sad_tf/__init__.py
+-rw-rw-rw-   0        0        0     5614 2023-07-17 06:10:42.000000 iman-0.0.91/iman/sad_tf/export_funcs.py
+-rw-rw-rw-   0        0        0     2221 2023-07-05 11:06:11.000000 iman-0.0.91/iman/sad_tf/features.py
+-rw-rw-rw-   0        0        0    18972 2023-07-23 07:08:02.000000 iman-0.0.91/iman/sad_tf/segmenter.py
+-rw-rw-rw-   0        0        0    20025 2023-07-23 08:03:31.000000 iman-0.0.91/iman/sad_tf/segmentero.py
+-rw-rw-rw-   0        0        0    13783 2022-11-30 10:00:38.000000 iman-0.0.91/iman/sad_tf/sidekit_mfcc.py
+-rw-rw-rw-   0        0        0      553 2022-01-12 05:39:10.000000 iman-0.0.91/iman/sad_tf/thread_returning.py
+-rw-rw-rw-   0        0        0     7808 2022-01-12 05:39:09.000000 iman-0.0.91/iman/sad_tf/viterbi.py
+-rw-rw-rw-   0        0        0     1755 2022-01-12 05:39:10.000000 iman-0.0.91/iman/sad_tf/viterbi_utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:53.000000 iman-0.0.91/iman/sad_torch_mfcc/
+-rw-rw-rw-   0        0        0      107 2022-12-26 10:21:43.000000 iman-0.0.91/iman/sad_torch_mfcc/__init__.py
+-rw-rw-rw-   0        0        0     4645 2022-12-11 08:33:44.000000 iman-0.0.91/iman/sad_torch_mfcc/export_funcs.py
+-rw-rw-rw-   0        0        0     2002 2023-07-05 11:08:54.000000 iman-0.0.91/iman/sad_torch_mfcc/features.py
+-rw-rw-rw-   0        0        0     3098 2022-12-11 08:39:59.000000 iman-0.0.91/iman/sad_torch_mfcc/sad_model.py
+-rw-rw-rw-   0        0        0    19324 2023-07-22 04:57:05.000000 iman-0.0.91/iman/sad_torch_mfcc/segmenter.py
+-rw-rw-rw-   0        0        0      553 2022-01-12 05:39:10.000000 iman-0.0.91/iman/sad_torch_mfcc/thread_returning.py
+-rw-rw-rw-   0        0        0     7808 2022-01-12 05:39:09.000000 iman-0.0.91/iman/sad_torch_mfcc/viterbi.py
+-rw-rw-rw-   0        0        0     1755 2022-01-12 05:39:10.000000 iman-0.0.91/iman/sad_torch_mfcc/viterbi_utils.py
+-rw-rw-rw-   0        0        0      422 2022-11-22 05:36:39.000000 iman-0.0.91/iman/tsne.py
+-rw-rw-rw-   0        0        0     2234 2023-06-10 12:42:19.000000 iman-0.0.91/iman/web.py
+-rw-rw-rw-   0        0        0     7159 2022-10-26 09:16:54.000000 iman-0.0.91/iman/xvector.py
+drwxrwxrwx   0        0        0        0 2023-07-23 08:03:52.000000 iman-0.0.91/iman.egg-info/
+-rw-rw-rw-   0        0        0     6772 2023-07-23 08:03:52.000000 iman-0.0.91/iman.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1773 2023-07-23 08:03:52.000000 iman-0.0.91/iman.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 08:03:52.000000 iman-0.0.91/iman.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       34 2023-07-23 08:03:52.000000 iman-0.0.91/iman.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        5 2023-07-23 08:03:52.000000 iman-0.0.91/iman.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 08:03:53.000000 iman-0.0.91/setup.cfg
+-rw-rw-rw-   0        0        0      903 2023-07-23 08:03:46.000000 iman-0.0.91/setup.py
```

### Comparing `iman-0.0.90/PKG-INFO` & `iman-0.0.91/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: iman
-Version: 0.0.90
+Version: 0.0.91
 Summary: Python package for daily Tasks
 Home-page: UNKNOWN
 Author: Iman Sarraf
 Author-email: imansarraf@gmail.com
 License: UNKNOWN
 Keywords: python,iman
 Platform: UNKNOWN
```

### Comparing `iman-0.0.90/README.rst` & `iman-0.0.91/README.rst`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/AUG.py` & `iman-0.0.91/iman/AUG.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/Audio.py` & `iman-0.0.91/iman/Audio.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/Features/mfcc/LS.py` & `iman-0.0.91/iman/Features/mfcc/LS.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/Features/mfcc/SB.py` & `iman-0.0.91/iman/Features/mfcc/SB.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/Features/mfcc/getmfcc_from_librosa.py` & `iman-0.0.91/iman/Features/mfcc/getmfcc_from_librosa.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/Features/mfcc/sb_mfcc_class.py` & `iman-0.0.91/iman/Features/mfcc/sb_mfcc_class.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/Image.py` & `iman-0.0.91/iman/Image.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/Report.py` & `iman-0.0.91/iman/Report.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/Text.py` & `iman-0.0.91/iman/Text.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/__init__.py` & `iman-0.0.91/iman/__init__.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/examples.py` & `iman-0.0.91/iman/examples.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/examples_folder/age.py` & `iman-0.0.91/iman/examples_folder/age.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/examples_folder/pyworldd.py` & `iman-0.0.91/iman/examples_folder/pyworldd.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/examples_folder/save_docx.py` & `iman-0.0.91/iman/examples_folder/save_docx.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/gpu_info.py` & `iman-0.0.91/iman/gpu_info.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/info.py` & `iman-0.0.91/iman/info.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/metrics.py` & `iman-0.0.91/iman/metrics.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/num2fa/__init__.py` & `iman-0.0.91/iman/num2fa/__init__.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/pyctcdecode/alphabet.py` & `iman-0.0.91/iman/pyctcdecode/alphabet.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/pyctcdecode/constants.py` & `iman-0.0.91/iman/pyctcdecode/constants.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/pyctcdecode/decoder.py` & `iman-0.0.91/iman/pyctcdecode/decoder.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/pyctcdecode/language_model.py` & `iman-0.0.91/iman/pyctcdecode/language_model.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_tf/export_funcs.py` & `iman-0.0.91/iman/sad_tf/export_funcs.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_tf/features.py` & `iman-0.0.91/iman/sad_tf/features.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_tf/segmenter.py` & `iman-0.0.91/iman/sad_tf/segmenter.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_tf/segmentero.py` & `iman-0.0.91/iman/sad_tf/segmentero.py`

 * *Files 1% similar despite different names*

```diff
@@ -354,15 +354,15 @@
     viterbi_arg = 80
 
 
 
 class Segmenter:
 
 
-    def __init__(self, vad_type = 'sad' , vad_engine='smn', detect_gender=False, sr=16000, batch_size=32 , complete_output=False,model_path="c:\\keras_speech_music_noise_cnn.hdf5",gender_path="c:\\keras_male_female_cnn.hdf5" , ffmpeg_path='c:\\ffmpeg.exe',device='cuda'):
+    def __init__(self, vad_type = 'sad' , vad_engine='smn', detect_gender=False, sr=16000, batch_size=32 , complete_output=False,model_path="c:\\keras_speech_music_noise_cnn.onnx",gender_path="c:\\keras_male_female_cnn.onnx" , ffmpeg_path='c:\\ffmpeg.exe',device='cuda'):
         """
         Load neural network models
         
         Input:
 
         'vad_engine' can be 'sm' (speech/music) or 'smn' (speech/music/noise)
                 'sm' was used in the results presented in ICASSP 2017 paper
```

### Comparing `iman-0.0.90/iman/sad_tf/sidekit_mfcc.py` & `iman-0.0.91/iman/sad_tf/sidekit_mfcc.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_tf/thread_returning.py` & `iman-0.0.91/iman/sad_tf/thread_returning.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_tf/viterbi.py` & `iman-0.0.91/iman/sad_tf/viterbi.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_tf/viterbi_utils.py` & `iman-0.0.91/iman/sad_tf/viterbi_utils.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_torch_mfcc/export_funcs.py` & `iman-0.0.91/iman/sad_torch_mfcc/export_funcs.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_torch_mfcc/features.py` & `iman-0.0.91/iman/sad_torch_mfcc/features.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_torch_mfcc/sad_model.py` & `iman-0.0.91/iman/sad_torch_mfcc/sad_model.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_torch_mfcc/segmenter.py` & `iman-0.0.91/iman/sad_torch_mfcc/segmenter.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_torch_mfcc/thread_returning.py` & `iman-0.0.91/iman/sad_torch_mfcc/thread_returning.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_torch_mfcc/viterbi.py` & `iman-0.0.91/iman/sad_torch_mfcc/viterbi.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/sad_torch_mfcc/viterbi_utils.py` & `iman-0.0.91/iman/sad_torch_mfcc/viterbi_utils.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/web.py` & `iman-0.0.91/iman/web.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman/xvector.py` & `iman-0.0.91/iman/xvector.py`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/iman.egg-info/PKG-INFO` & `iman-0.0.91/iman.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: iman
-Version: 0.0.90
+Version: 0.0.91
 Summary: Python package for daily Tasks
 Home-page: UNKNOWN
 Author: Iman Sarraf
 Author-email: imansarraf@gmail.com
 License: UNKNOWN
 Keywords: python,iman
 Platform: UNKNOWN
```

### Comparing `iman-0.0.90/iman.egg-info/SOURCES.txt` & `iman-0.0.91/iman.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `iman-0.0.90/setup.py` & `iman-0.0.91/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 from setuptools import setup, find_packages
 def read(fname):
     return open(os.path.join(os.path.dirname(__file__), fname)).read()
 
 setup(
         # the name must match the folder name 'verysimplemodule'
         name="iman", 
-        version='0.0.90',
+        version='0.0.91',
         author="Iman Sarraf",
         author_email="imansarraf@gmail.com",
         description='Python package for daily Tasks',
         long_description=read('README.rst'),
         packages=find_packages(),
         
         # add any additional packages that
```

