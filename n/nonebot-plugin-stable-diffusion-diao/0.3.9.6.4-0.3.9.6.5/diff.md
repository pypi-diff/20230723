# Comparing `tmp/nonebot_plugin_stable_diffusion_diao-0.3.9.6.4.tar.gz` & `tmp/nonebot_plugin_stable_diffusion_diao-0.3.9.6.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_stable_diffusion_diao-0.3.9.6.4.tar", last modified: Sat Jul 22 05:13:45 2023, max compression
+gzip compressed data, was "nonebot_plugin_stable_diffusion_diao-0.3.9.6.5.tar", last modified: Sun Jul 23 06:27:48 2023, max compression
```

## Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4.tar` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5.tar`

### file list

```diff
@@ -1,39 +1,39 @@
--rw-r--r--   0        0        0     1082 2023-05-28 09:58:15.375966 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/LICENSE
--rw-r--r--   0        0        0      692 2023-05-31 13:01:37.260789 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/__init__.py
--rw-r--r--   0        0        0    27841 2023-07-22 03:28:50.083794 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/aidraw.py
--rw-r--r--   0        0        0     6226 2023-07-22 03:14:33.094866 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/amusement/chatgpt_tagger.py
--rw-r--r--   0        0        0        0 2023-05-28 09:58:15.402430 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/amusement/ramdomgirl.py
--rw-r--r--   0        0        0    65703 2023-05-30 17:03:23.970846 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/amusement/today_girl.py
--rw-r--r--   0        0        0     3894 2023-06-12 05:12:59.000048 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/amusement/vits.py
--rw-r--r--   0        0        0        0 2023-05-28 09:58:15.402952 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/amusement/wordbank.py
--rw-r--r--   0        0        0      699 2023-05-28 09:58:15.404033 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/__init__.py
--rw-r--r--   0        0        0    16093 2023-07-16 04:28:25.749676 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/base.py
--rw-r--r--   0        0        0     1279 2023-05-28 09:58:15.404557 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/naifu.py
--rw-r--r--   0        0        0     1659 2023-05-28 09:58:15.405158 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/novelai.py
--rw-r--r--   0        0        0     6015 2023-07-17 06:15:44.003068 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/sd.py
--rw-r--r--   0        0        0    18828 2023-07-22 05:13:34.884393 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/config.py
--rw-r--r--   0        0        0    10771 2023-07-20 07:00:30.079891 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/aidraw_help.py
--rw-r--r--   0        0        0     3340 2023-05-28 09:58:15.406675 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/anlas.py
--rw-r--r--   0        0        0     1935 2023-05-28 09:58:15.406675 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/control_net.py
--rw-r--r--   0        0        0     2054 2023-07-10 12:39:09.576540 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/daylimit.py
--rw-r--r--   0        0        0     2709 2023-07-22 04:45:46.016686 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/deepdanbooru.py
--rw-r--r--   0        0        0    11332 2023-07-20 14:22:22.328291 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/explicit_api.py
--rw-r--r--   0        0        0     4139 2023-07-22 04:35:59.105979 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/safe_method.py
--rw-r--r--   0        0        0    41827 2023-07-22 04:01:57.684358 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/sd_extra_api_func.py
--rw-r--r--   0        0        0     6725 2023-07-22 05:13:24.953771 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/translation.py
--rw-r--r--   0        0        0      400 2023-05-28 09:58:15.409671 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/fifo.py
--rw-r--r--   0        0        0        0 2023-05-28 09:58:15.410176 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/locales/__init__.py
--rw-r--r--   0        0        0        0 2023-05-28 09:58:15.410176 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/locales/en.py
--rw-r--r--   0        0        0        0 2023-05-28 09:58:15.410176 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/locales/jp.py
--rw-r--r--   0        0        0        0 2023-05-28 09:58:15.410176 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/locales/moe_jp.py
--rw-r--r--   0        0        0        0 2023-05-28 09:58:15.411183 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/locales/moe_zh.py
--rw-r--r--   0        0        0        0 2023-05-28 09:58:15.411183 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/locales/zh.py
--rw-r--r--   0        0        0     1905 2023-05-28 09:58:15.411183 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/manage.py
--rw-r--r--   0        0        0     4677 2023-07-22 03:29:42.199501 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/__init__.py
--rw-r--r--   0        0        0     2111 2023-07-03 03:51:06.635888 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/data.py
--rw-r--r--   0        0        0     6163 2023-07-14 13:25:19.581758 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/load_balance.py
--rw-r--r--   0        0        0      726 2023-07-20 08:05:34.470705 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/prepocess.py
--rw-r--r--   0        0        0      733 2023-07-05 13:24:21.506297 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/save.py
--rw-r--r--   0        0        0     1985 2023-07-10 14:03:49.047428 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/version.py
--rw-r--r--   0        0        0      730 2023-07-22 05:13:45.929356 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/pyproject.toml
--rw-r--r--   0        0        0      487 1970-01-01 00:00:00.000000 nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/PKG-INFO
+-rw-r--r--   0        0        0     1082 2023-05-28 09:58:15.375966 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/LICENSE
+-rw-r--r--   0        0        0      692 2023-05-31 13:01:37.260789 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/__init__.py
+-rw-r--r--   0        0        0    27841 2023-07-22 03:28:50.083794 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/aidraw.py
+-rw-r--r--   0        0        0     6226 2023-07-22 03:14:33.094866 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/amusement/chatgpt_tagger.py
+-rw-r--r--   0        0        0        0 2023-05-28 09:58:15.402430 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/amusement/ramdomgirl.py
+-rw-r--r--   0        0        0    65703 2023-05-30 17:03:23.970846 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/amusement/today_girl.py
+-rw-r--r--   0        0        0     3894 2023-06-12 05:12:59.000048 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/amusement/vits.py
+-rw-r--r--   0        0        0        0 2023-05-28 09:58:15.402952 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/amusement/wordbank.py
+-rw-r--r--   0        0        0      699 2023-05-28 09:58:15.404033 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/__init__.py
+-rw-r--r--   0        0        0    16093 2023-07-16 04:28:25.749676 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/base.py
+-rw-r--r--   0        0        0     1279 2023-05-28 09:58:15.404557 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/naifu.py
+-rw-r--r--   0        0        0     1659 2023-05-28 09:58:15.405158 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/novelai.py
+-rw-r--r--   0        0        0     6015 2023-07-17 06:15:44.003068 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/sd.py
+-rw-r--r--   0        0        0    18828 2023-07-22 07:05:20.825247 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/config.py
+-rw-r--r--   0        0        0    10771 2023-07-20 07:00:30.079891 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/aidraw_help.py
+-rw-r--r--   0        0        0     3340 2023-05-28 09:58:15.406675 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/anlas.py
+-rw-r--r--   0        0        0     1935 2023-05-28 09:58:15.406675 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/control_net.py
+-rw-r--r--   0        0        0     2054 2023-07-10 12:39:09.576540 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/daylimit.py
+-rw-r--r--   0        0        0     2709 2023-07-22 04:45:46.016686 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/deepdanbooru.py
+-rw-r--r--   0        0        0    11332 2023-07-20 14:22:22.328291 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/explicit_api.py
+-rw-r--r--   0        0        0     4139 2023-07-22 04:35:59.105979 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/safe_method.py
+-rw-r--r--   0        0        0    41827 2023-07-22 04:01:57.684358 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/sd_extra_api_func.py
+-rw-r--r--   0        0        0     6353 2023-07-22 05:26:20.510066 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/translation.py
+-rw-r--r--   0        0        0      400 2023-05-28 09:58:15.409671 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/fifo.py
+-rw-r--r--   0        0        0        0 2023-05-28 09:58:15.410176 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/locales/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-28 09:58:15.410176 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/locales/en.py
+-rw-r--r--   0        0        0        0 2023-05-28 09:58:15.410176 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/locales/jp.py
+-rw-r--r--   0        0        0        0 2023-05-28 09:58:15.410176 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/locales/moe_jp.py
+-rw-r--r--   0        0        0        0 2023-05-28 09:58:15.411183 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/locales/moe_zh.py
+-rw-r--r--   0        0        0        0 2023-05-28 09:58:15.411183 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/locales/zh.py
+-rw-r--r--   0        0        0     1905 2023-05-28 09:58:15.411183 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/manage.py
+-rw-r--r--   0        0        0     4677 2023-07-22 03:29:42.199501 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/__init__.py
+-rw-r--r--   0        0        0     2111 2023-07-03 03:51:06.635888 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/data.py
+-rw-r--r--   0        0        0     6148 2023-07-23 06:26:49.415580 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/load_balance.py
+-rw-r--r--   0        0        0      726 2023-07-20 08:05:34.470705 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/prepocess.py
+-rw-r--r--   0        0        0      733 2023-07-05 13:24:21.506297 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/save.py
+-rw-r--r--   0        0        0     1985 2023-07-10 14:03:49.047428 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/version.py
+-rw-r--r--   0        0        0      730 2023-07-23 06:27:48.371619 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/pyproject.toml
+-rw-r--r--   0        0        0      487 1970-01-01 00:00:00.000000 nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/PKG-INFO
```

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/LICENSE` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/__init__.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/aidraw.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/aidraw.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/amusement/chatgpt_tagger.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/amusement/chatgpt_tagger.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/amusement/today_girl.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/amusement/today_girl.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/amusement/vits.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/amusement/vits.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/__init__.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/base.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/base.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/naifu.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/naifu.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/novelai.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/novelai.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/backend/sd.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/backend/sd.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/config.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/config.py`

 * *Files 1% similar despite different names*

```diff
@@ -52,15 +52,15 @@
     novelai_cd: int = 60  # 默认的cd
     novelai_group_cd: int = 3  # 默认的群共享cd
     novelai_on: bool = True  # 是否全局开启
     novelai_revoke: int = 0  # 是否自动撤回，该值不为0时，则为撤回时间
     novelai_random_ratio: bool = True  # 是否开启随机比例
     novelai_random_sampler: bool = False  # 是否开启随机采样器
     novelai_random_scale: bool = False  # 是否开启随机CFG
-    novelai_random_ratio_list: list = [("p", 0.35), ("s", 0.10), ("l", 0.35), ("uw", 0.1), ("uwp", 0.1)] # 随机图片比例
+    novelai_random_ratio_list: list =  [("p", 0.55), ("s", 0.1), ("l", 0.2), ("uw", 0.05), ("uwp", 0.1)] # 随机图片比例
     novelai_random_sampler_list = [("Euler a", 0.35), ("DDIM", 0.3), ("DPM++ 2S a Karras", 0.05), ("DPM++ 2M Karras", 0.3)]
     novelai_random_scale_list = [(3, 0.05), (4, 0.2), (5, 0.05), (6, 0.4), (7, 0.1), (8, 0.18), (9, 0.02)]
     novelai_load_balance: bool = True  # 负载均衡, 使用前请先将队列限速关闭, 目前只支持stable-diffusion-webui, 所以目前只支持novelai_mode = "sd" 时可用, 目前已知问题, 很短很短时间内疯狂画图的话无法均匀分配任务
     novelai_load_balance_mode: int = 1  # 负载均衡模式, 1为随机, 2为加权随机选择
     novelai_load_balance_weight: list = []  # 设置列表, 列表长度为你的后端数量, 数值为随机权重, 例[0.2, 0.5, 0.3]
     novelai_backend_url_dict: dict = {"雕雕的后端": "la.iamdiao.lol:5938", "雕雕的后端2": "la.iamdiao.lol:1521"} # 你能用到的后端, 键为名称, 值为url, 例:backend_url_dict = {"NVIDIA P102-100": "192.168.5.197:7860","NVIDIA CMP 40HX": "127.0.0.1:7860"
     novelai_sampler: str = None  # 默认采样器,不写的话默认Euler a, Euler a系画人物可能比较好点, DDIM系, 如UniPC画出来的背景比较丰富, DPM系采样器一般速度较慢, 请你自己尝试(以上为个人感觉
```

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/aidraw_help.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/aidraw_help.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/anlas.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/anlas.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/control_net.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/control_net.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/daylimit.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/daylimit.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/deepdanbooru.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/deepdanbooru.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/explicit_api.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/explicit_api.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/safe_method.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/safe_method.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/sd_extra_api_func.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/sd_extra_api_func.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/extension/translation.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/extension/translation.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import aiohttp
 from ..config import config
 from nonebot.log import logger
 
 
 async def translate(text: str, to: str):
     # en,jp,zh
-    is_translate = True
+    is_translate = False
     for i in range(config.novelai_retry):
         try:
             result = (await translate_deepl(text, to) or 
                       await translate_bing(text, to) or
                       await translate_baidu(text, to) or
                       await translate_youdao(text, to) or
                       await translate_google_proxy(text, to)
@@ -30,31 +30,28 @@
     """
     en,jp,zh_Hans
     """
     try:
         if to == "zh":
             to = "zh-Hans"
         key = config.bing_key
-        if not key:
-            return None
         header = {
             "Ocp-Apim-Subscription-Key": key,
             "Content-Type": "application/json",
         }
         async with aiohttp.ClientSession() as session:
             body = [{'text': text}]
             params = {
                 "api-version": "3.0",
                 "to": to,
                 "profanityAction": "Deleted",
             }
             async with session.post('https://api.cognitive.microsofttranslator.com/translate', json=body, params=params, headers=header) as resp:
                 if resp.status != 200:
                     logger.error(f"Bing翻译接口调用失败,错误代码{resp.status},{await resp.text()}")
-                    return None
                 jsonresult = await resp.json()
                 result=jsonresult[0]["translations"][0]["text"]
                 logger.debug(f"Bing翻译启动，获取到{text},翻译后{result}")
                 return result
     except Exception:
         return None
 
@@ -62,26 +59,23 @@
 async def translate_deepl(text: str, to: str):
     """
     EN,JA,ZH
     """
     try:
         to = to.upper()
         key = config.deepl_key
-        if not key:
-            return None
         async with aiohttp.ClientSession() as session:
             params = {
                 "auth_key":key,
                 "text": text,
                 "target_lang": to,
             }
             async with session.get('https://api-free.deepl.com/v2/translate', params=params) as resp:
                 if resp.status != 200:
                     logger.error(f"DeepL翻译接口调用失败,错误代码{resp.status},{await resp.text()}")
-                    return None
                 jsonresult = await resp.json()
                 result=jsonresult["translations"][0]["text"]
                 logger.debug(f"DeepL翻译启动，获取到{text},翻译后{result}")
                 return result
     except Exception:
         return None
 
@@ -102,15 +96,14 @@
                 'doctype': 'json',
                 'type': type,
                 'i': input
             }
             async with session.post("http://fanyi.youdao.com/translate", data=data) as resp:
                 if resp.status != 200:
                     logger.error(f"有道翻译接口调用失败,错误代码{resp.status},{await resp.text()}")
-                    return None
                 result = await resp.json()
                 result=result["translateResult"][0][0]["tgt"]
                 logger.debug(f"有道翻译启动，获取到{input},翻译后{result}")
                 return result
     except Exception:
         return None
 
@@ -125,19 +118,16 @@
         else:
             from_="zh"
         async with aiohttp.ClientSession()as session:
             data = {"data": [input, from_, to]}
             async with session.post("https://mikeee-gradio-gtr.hf.space/api/predict", json=data)as resp:
                 if resp.status != 200:
                     logger.error(f"谷歌代理翻译接口调用失败,错误代码{resp.status},{await resp.text()}")
-                    return None
                 result = await resp.json()
                 result=result["data"][0]
-                if "429" in result:
-                    return None
                 logger.debug(f"谷歌代理翻译启动，获取到{input},翻译后{result}")
                 return result
     except Exception:
         return None
 
 
 async def get_access_token():
@@ -155,25 +145,22 @@
             json = await resp.json()
     return json["access_token"]
 
 
 async def translate_baidu(input: str, to: str):
     try:
         key = config.baidu_translate_key
-        if not key:
-            return None
         token = await get_access_token()
         url = 'https://aip.baidubce.com/rpc/2.0/mt/texttrans/v1?access_token=' + token
         # For list of language codes, please refer to `https://ai.baidu.com/ai-doc/MT/4kqryjku9#语种列表`
         term_ids = '' # 术语库id，多个逗号隔开
         headers = {'Content-Type': 'application/json'}
         payload = {'q': input, 'from': 'zh', 'to': to, 'termIds' : term_ids}
         async with aiohttp.ClientSession(headers=headers) as session:
             async with session.post(url=url, json=payload) as resp:
                 if resp.status != 200:
                     logger.error(f"百度翻译接口错误, 错误代码{resp.status},{await resp.text()}")
-                    return None
                 json_ = await resp.json()
                 result = json_["result"]["trans_result"][0]["dst"]
         return result
     except Exception:
         return None
```

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/manage.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/manage.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/__init__.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/data.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/data.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/load_balance.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/load_balance.py`

 * *Files 1% similar despite different names*

```diff
@@ -129,15 +129,15 @@
         normal_backend_len = len(normal_backend)
         if weight_list_len != backend_url_list_len:
             logger.warning("权重列表长度不一致, 请重新配置!")
             ava_url = random.choice(normal_backend)
         else:
             from ..backend import AIDRAW
             if weight_list_len != normal_backend_len:
-                multi = weight_list_len / (weight_list_len - normal_backend_len)
+                multi = backend_url_list_len / normal_backend_len
                 for weight, backend_site in zip(weight_list, backend_url_list):
                     if backend_site in normal_backend:
                         list_tuple.append((backend_site, weight*multi))
             else:
                 for backend, weight in zip(normal_backend, weight_list):
                     list_tuple.append((backend, weight))
             print(list_tuple)
```

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/prepocess.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/prepocess.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/utils/save.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/utils/save.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/nonebot_plugin_stable_diffusion_diao/version.py` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/nonebot_plugin_stable_diffusion_diao/version.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_stable_diffusion_diao-0.3.9.6.4/pyproject.toml` & `nonebot_plugin_stable_diffusion_diao-0.3.9.6.5/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "nonebot-plugin-stable-diffusion-diao"
-version = "0.3.9.6.4"
+version = "0.3.9.6.5"
 description = "主要面对stable-diffusion-webui-api的nonebot2插件"
 authors = [
     { name = "DiaoDaiaChan", email = "diaodaiachan@qq.com" },
 ]
 dependencies = [
     "aiofiles>=23.1.0",
     "aiohttp>=3.8.4",
```

