# Comparing `tmp/ykdl-1.8.1.post1.tar.gz` & `tmp/ykdl-1.8.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ykdl-1.8.1.post1.tar", last modified: Sun May 15 09:25:06 2022, max compression
+gzip compressed data, was "ykdl-1.8.2.tar", last modified: Sun Jul 23 01:52:01 2023, max compression
```

## Comparing `ykdl-1.8.1.post1.tar` & `ykdl-1.8.2.tar`

### file list

```diff
@@ -1,163 +1,155 @@
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.613576 ykdl-1.8.1.post1/
--rw-rw-rw-   0        0        0     6967 2022-05-15 09:24:53.000000 ykdl-1.8.1.post1/CHANGELOG.rst
--rw-rw-rw-   0        0        0     1368 2022-01-08 13:30:55.000000 ykdl-1.8.1.post1/LICENSE.txt
--rw-rw-rw-   0        0        0       61 2020-01-21 09:08:48.000000 ykdl-1.8.1.post1/MANIFEST.in
--rw-rw-rw-   0        0        0    10963 2022-05-15 09:25:06.614576 ykdl-1.8.1.post1/PKG-INFO
--rw-rw-rw-   0        0        0     2091 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/README.rst
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:05.150576 ykdl-1.8.1.post1/cykdl/
--rw-rw-rw-   0        0        0        0 2020-01-21 09:08:48.000000 ykdl-1.8.1.post1/cykdl/__init__.py
--rw-rw-rw-   0        0        0    14577 2022-05-14 13:09:09.000000 ykdl-1.8.1.post1/cykdl/__main__.py
--rw-rw-rw-   0        0        0      111 2022-05-15 09:25:06.615576 ykdl-1.8.1.post1/setup.cfg
--rw-rw-rw-   0        0        0     2539 2022-05-14 11:03:07.000000 ykdl-1.8.1.post1/setup.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:05.235576 ykdl-1.8.1.post1/ykdl/
--rw-rw-rw-   0        0        0       34 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/__init__.py
--rw-rw-rw-   0        0        0     3349 2022-04-06 01:33:10.000000 ykdl-1.8.1.post1/ykdl/common.py
--rw-rw-rw-   0        0        0     3895 2022-05-15 09:05:16.000000 ykdl-1.8.1.post1/ykdl/compact.py
--rw-rw-rw-   0        0        0     7918 2022-05-09 07:28:22.000000 ykdl-1.8.1.post1/ykdl/extractor.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:05.716576 ykdl-1.8.1.post1/ykdl/extractors/
--rw-rw-rw-   0        0        0        0 2020-01-21 09:08:48.000000 ykdl-1.8.1.post1/ykdl/extractors/__init__.py
--rw-rw-rw-   0        0        0     1957 2022-04-30 16:25:48.000000 ykdl-1.8.1.post1/ykdl/extractors/_byted.py
--rw-rw-rw-   0        0        0    71721 2021-03-04 08:04:12.000000 ykdl-1.8.1.post1/ykdl/extractors/_byted_acrawler.js
--rw-rw-rw-   0        0        0     1778 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/_common.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:05.748576 ykdl-1.8.1.post1/ykdl/extractors/acfun/
--rw-rw-rw-   0        0        0      178 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/acfun/__init__.py
--rw-rw-rw-   0        0        0     1295 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/acfun/acbase.py
--rw-rw-rw-   0        0        0      957 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/acfun/bangumi.py
--rw-rw-rw-   0        0        0     1135 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/acfun/video.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:05.761576 ykdl-1.8.1.post1/ykdl/extractors/baidu/
--rw-rw-rw-   0        0        0      174 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/baidu/__init__.py
--rw-rw-rw-   0        0        0     1258 2022-01-11 11:35:46.000000 ykdl-1.8.1.post1/ykdl/extractors/baidu/music.py
--rw-rw-rw-   0        0        0     1153 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/baomihua.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:05.879576 ykdl-1.8.1.post1/ykdl/extractors/bilibili/
--rw-rw-rw-   0        0        0     1141 2022-03-28 07:54:40.000000 ykdl-1.8.1.post1/ykdl/extractors/bilibili/__init__.py
--rw-rw-rw-   0        0        0     1582 2022-04-02 15:31:36.000000 ykdl-1.8.1.post1/ykdl/extractors/bilibili/bangumi.py
--rw-rw-rw-   0        0        0     2228 2022-05-03 12:37:36.000000 ykdl-1.8.1.post1/ykdl/extractors/bilibili/bilibase.py
--rw-rw-rw-   0        0        0     1046 2022-03-28 07:51:10.000000 ykdl-1.8.1.post1/ykdl/extractors/bilibili/idconvertor.py
--rw-rw-rw-   0        0        0     5094 2022-05-03 13:08:26.000000 ykdl-1.8.1.post1/ykdl/extractors/bilibili/live.py
--rw-rw-rw-   0        0        0      516 2022-04-30 18:50:42.000000 ykdl-1.8.1.post1/ykdl/extractors/bilibili/util.py
--rw-rw-rw-   0        0        0      804 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/bilibili/vc.py
--rw-rw-rw-   0        0        0     2291 2022-05-01 07:32:52.000000 ykdl-1.8.1.post1/ykdl/extractors/bilibili/video.py
--rw-rw-rw-   0        0        0     1883 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/cctv.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:05.926576 ykdl-1.8.1.post1/ykdl/extractors/douban/
--rw-rw-rw-   0        0        0      340 2022-02-10 15:32:04.000000 ykdl-1.8.1.post1/ykdl/extractors/douban/__init__.py
--rw-rw-rw-   0        0        0      849 2022-02-10 15:40:04.000000 ykdl-1.8.1.post1/ykdl/extractors/douban/movie.py
--rw-rw-rw-   0        0        0     1869 2022-05-12 21:47:08.000000 ykdl-1.8.1.post1/ykdl/extractors/douban/music.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:05.972576 ykdl-1.8.1.post1/ykdl/extractors/douyin/
--rw-rw-rw-   0        0        0      512 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/douyin/__init__.py
--rw-rw-rw-   0        0        0     2082 2022-04-08 12:48:22.000000 ykdl-1.8.1.post1/ykdl/extractors/douyin/live.py
--rw-rw-rw-   0        0        0     1048 2022-04-08 15:42:54.000000 ykdl-1.8.1.post1/ykdl/extractors/douyin/video.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.012576 ykdl-1.8.1.post1/ykdl/extractors/douyu/
--rw-rw-rw-   0        0        0      200 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/douyu/__init__.py
--rw-rw-rw-   0        0        0     6609 2020-01-21 09:08:48.000000 ykdl-1.8.1.post1/ykdl/extractors/douyu/crypto-js-md5.min.js
--rw-rw-rw-   0        0        0     3429 2022-03-29 12:16:36.000000 ykdl-1.8.1.post1/ykdl/extractors/douyu/live.py
--rw-rw-rw-   0        0        0     3356 2021-12-01 22:04:34.000000 ykdl-1.8.1.post1/ykdl/extractors/douyu/util.py
--rw-rw-rw-   0        0        0     1678 2022-05-10 06:45:10.000000 ykdl-1.8.1.post1/ykdl/extractors/douyu/video.py
--rw-rw-rw-   0        0        0     5550 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/fun.py
--rw-rw-rw-   0        0        0     5370 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/generalembed.py
--rw-rw-rw-   0        0        0     2463 2022-05-12 21:33:41.000000 ykdl-1.8.1.post1/ykdl/extractors/generalsimple.py
--rw-rw-rw-   0        0        0   111557 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/heibaizhibo.m.js
--rw-rw-rw-   0        0        0     2749 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/heibaizhibo.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.045576 ykdl-1.8.1.post1/ykdl/extractors/huajiao/
--rw-rw-rw-   0        0        0      172 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/huajiao/__init__.py
--rw-rw-rw-   0        0        0     2002 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/huajiao/live.py
--rw-rw-rw-   0        0        0      853 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/huajiao/video.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.066576 ykdl-1.8.1.post1/ykdl/extractors/huya/
--rw-rw-rw-   0        0        0      173 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/huya/__init__.py
--rw-rw-rw-   0        0        0     3718 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/huya/live.py
--rw-rw-rw-   0        0        0     1898 2022-03-27 09:40:26.000000 ykdl-1.8.1.post1/ykdl/extractors/huya/video.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.084576 ykdl-1.8.1.post1/ykdl/extractors/ifeng/
--rw-rw-rw-   0        0        0      238 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/ifeng/__init__.py
--rw-rw-rw-   0        0        0     1024 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/ifeng/gongkaike.py
--rw-rw-rw-   0        0        0     1461 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/ifeng/news.py
--rw-rw-rw-   0        0        0      900 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/ifeng/video.py
--rw-rw-rw-   0        0        0      571 2022-05-12 21:45:32.000000 ykdl-1.8.1.post1/ykdl/extractors/iqilu.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.156576 ykdl-1.8.1.post1/ykdl/extractors/iqiyi/
--rw-rw-rw-   0        0        0      337 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/iqiyi/__init__.py
--rw-rw-rw-   0        0        0   125305 2020-01-21 09:08:48.000000 ykdl-1.8.1.post1/ykdl/extractors/iqiyi/cmd5x.js
--rw-rw-rw-   0        0        0    91151 2019-10-24 05:42:40.000000 ykdl-1.8.1.post1/ykdl/extractors/iqiyi/cmd5x_iqiyi3.js
--rw-rw-rw-   0        0        0     3200 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/iqiyi/live.py
--rw-rw-rw-   0        0        0     1879 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/iqiyi/util.py
--rw-rw-rw-   0        0        0     8409 2022-05-12 21:48:26.000000 ykdl-1.8.1.post1/ykdl/extractors/iqiyi/video.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.230576 ykdl-1.8.1.post1/ykdl/extractors/ixigua/
--rw-rw-rw-   0        0        0      198 2022-04-08 10:30:38.000000 ykdl-1.8.1.post1/ykdl/extractors/ixigua/__init__.py
--rw-rw-rw-   0        0        0     1501 2022-04-08 12:13:16.000000 ykdl-1.8.1.post1/ykdl/extractors/ixigua/live.py
--rw-rw-rw-   0        0        0     2937 2022-05-01 06:44:54.000000 ykdl-1.8.1.post1/ykdl/extractors/ixigua/video.py
--rw-rw-rw-   0        0        0      721 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/joy.py
--rw-rw-rw-   0        0        0     1357 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/kankanews.py
--rw-rw-rw-   0        0        0      753 2022-05-12 21:45:56.000000 ykdl-1.8.1.post1/ykdl/extractors/ku6.py
--rw-rw-rw-   0        0        0     2123 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/kuwo.py
--rw-rw-rw-   0        0        0     1630 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/laifeng.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.282576 ykdl-1.8.1.post1/ykdl/extractors/le/
--rw-rw-rw-   0        0        0      532 2022-05-12 21:49:08.000000 ykdl-1.8.1.post1/ykdl/extractors/le/__init__.py
--rw-rw-rw-   0        0        0     4110 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/le/le.py
--rw-rw-rw-   0        0        0     2153 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/le/letvcloud.py
--rw-rw-rw-   0        0        0     2798 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/le/live.py
--rw-rw-rw-   0        0        0     1769 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/le/lunbo.py
--rw-rw-rw-   0        0        0     1173 2022-05-12 21:10:50.000000 ykdl-1.8.1.post1/ykdl/extractors/lizhi.py
--rw-rw-rw-   0        0        0     1119 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/longzhu.py
--rw-rw-rw-   0        0        0     3490 2022-05-03 12:56:27.000000 ykdl-1.8.1.post1/ykdl/extractors/mgtv.py
--rw-rw-rw-   0        0        0     2985 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/miaopai.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.325576 ykdl-1.8.1.post1/ykdl/extractors/netease/
--rw-rw-rw-   0        0        0      557 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/__init__.py
--rw-rw-rw-   0        0        0      897 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/live.py
--rw-rw-rw-   0        0        0     1526 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/livecc.py
--rw-rw-rw-   0        0        0      614 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/m3g.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.388576 ykdl-1.8.1.post1/ykdl/extractors/netease/music/
--rw-rw-rw-   0        0        0      341 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/music/__init__.py
--rw-rw-rw-   0        0        0     1232 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/music/music.py
--rw-rw-rw-   0        0        0     2902 2022-01-11 11:12:56.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/music/musicbase.py
--rw-rw-rw-   0        0        0     1312 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/music/mv.py
--rw-rw-rw-   0        0        0      877 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/music/program.py
--rw-rw-rw-   0        0        0     3926 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/openc.py
--rw-rw-rw-   0        0        0      874 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/netease/video.py
--rw-rw-rw-   0        0        0     2849 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/pps.py
--rw-rw-rw-   0        0        0     2513 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/pptv.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.412576 ykdl-1.8.1.post1/ykdl/extractors/qq/
--rw-rw-rw-   0        0        0      235 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/qq/__init__.py
--rw-rw-rw-   0        0        0     1650 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/qq/egame.py
--rw-rw-rw-   0        0        0     1054 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/qq/live.py
--rw-rw-rw-   0        0        0     8918 2022-05-03 12:49:24.000000 ykdl-1.8.1.post1/ykdl/extractors/qq/video.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.449576 ykdl-1.8.1.post1/ykdl/extractors/sina/
--rw-rw-rw-   0        0        0      242 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/sina/__init__.py
--rw-rw-rw-   0        0        0      666 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/sina/embed.py
--rw-rw-rw-   0        0        0     1334 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/sina/openc.py
--rw-rw-rw-   0        0        0     1556 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/sina/video.py
--rw-rw-rw-   0        0        0     3690 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/singlemultimedia.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.481576 ykdl-1.8.1.post1/ykdl/extractors/sohu/
--rw-rw-rw-   0        0        0      335 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/sohu/__init__.py
--rw-rw-rw-   0        0        0      281 2021-11-27 03:45:05.000000 ykdl-1.8.1.post1/ykdl/extractors/sohu/edu.py
--rw-rw-rw-   0        0        0      279 2021-11-27 03:45:06.000000 ykdl-1.8.1.post1/ykdl/extractors/sohu/my.py
--rw-rw-rw-   0        0        0     4692 2022-04-10 17:03:04.000000 ykdl-1.8.1.post1/ykdl/extractors/sohu/sohubase.py
--rw-rw-rw-   0        0        0      219 2021-11-27 03:45:06.000000 ykdl-1.8.1.post1/ykdl/extractors/sohu/tv.py
--rw-rw-rw-   0        0        0      313 2021-11-27 03:45:06.000000 ykdl-1.8.1.post1/ykdl/extractors/tudou.py
--rw-rw-rw-   0        0        0     3899 2022-02-18 13:12:14.000000 ykdl-1.8.1.post1/ykdl/extractors/weibo.py
--rw-rw-rw-   0        0        0      816 2022-05-03 12:37:06.000000 ykdl-1.8.1.post1/ykdl/extractors/yinyuetai.py
--rw-rw-rw-   0        0        0      826 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/yizhibo.py
--rw-rw-rw-   0        0        0     5991 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/youku.py
--rw-rw-rw-   0        0        0     5626 2021-11-27 03:45:06.000000 ykdl-1.8.1.post1/ykdl/extractors/youkujs.py
--rw-rw-rw-   0        0        0      578 2021-11-27 03:45:06.000000 ykdl-1.8.1.post1/ykdl/extractors/zhangyu.py
--rw-rw-rw-   0        0        0     2415 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/zhanqi.py
--rw-rw-rw-   0        0        0     2297 2022-01-08 13:30:25.000000 ykdl-1.8.1.post1/ykdl/extractors/zhuafan.py
--rw-rw-rw-   0        0        0    10484 2022-05-05 05:50:06.000000 ykdl-1.8.1.post1/ykdl/mediainfo.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:06.611576 ykdl-1.8.1.post1/ykdl/util/
--rw-rw-rw-   0        0        0        0 2020-01-21 09:08:48.000000 ykdl-1.8.1.post1/ykdl/util/__init__.py
--rw-rw-rw-   0        0        0    13625 2022-01-11 11:30:30.000000 ykdl-1.8.1.post1/ykdl/util/download.py
--rw-rw-rw-   0        0        0     6951 2022-05-05 06:08:50.000000 ykdl-1.8.1.post1/ykdl/util/external.py
--rw-rw-rw-   0        0        0     3169 2022-05-10 11:59:18.000000 ykdl-1.8.1.post1/ykdl/util/fs.py
--rw-rw-rw-   0        0        0    23741 2022-05-12 21:53:24.000000 ykdl-1.8.1.post1/ykdl/util/http.py
--rw-rw-rw-   0        0        0     5470 2022-05-12 21:51:22.000000 ykdl-1.8.1.post1/ykdl/util/human.py
--rw-rw-rw-   0        0        0     2366 2022-05-08 10:29:52.000000 ykdl-1.8.1.post1/ykdl/util/log.py
--rw-rw-rw-   0        0        0     3927 2022-04-30 17:19:20.000000 ykdl-1.8.1.post1/ykdl/util/m3u8.py
--rw-rw-rw-   0        0        0     2716 2022-05-12 22:11:50.000000 ykdl-1.8.1.post1/ykdl/util/match.py
--rw-rw-rw-   0        0        0    15633 2022-03-27 10:09:48.000000 ykdl-1.8.1.post1/ykdl/util/rangefetch_server.py
--rw-rw-rw-   0        0        0     5777 2022-04-06 01:13:16.000000 ykdl-1.8.1.post1/ykdl/util/wrap.py
--rw-rw-rw-   0        0        0     5149 2021-11-30 08:53:42.000000 ykdl-1.8.1.post1/ykdl/util/xml2dict.py
--rw-rw-rw-   0        0        0       28 2022-05-15 09:18:28.000000 ykdl-1.8.1.post1/ykdl/version.py
-drwxrwxrwx   0        0        0        0 2022-05-15 09:25:05.244576 ykdl-1.8.1.post1/ykdl.egg-info/
--rw-rw-rw-   0        0        0    10963 2022-05-15 09:25:04.000000 ykdl-1.8.1.post1/ykdl.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     3919 2022-05-15 09:25:04.000000 ykdl-1.8.1.post1/ykdl.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-05-15 09:25:04.000000 ykdl-1.8.1.post1/ykdl.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       46 2022-05-15 09:25:04.000000 ykdl-1.8.1.post1/ykdl.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      168 2022-05-15 09:25:04.000000 ykdl-1.8.1.post1/ykdl.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2022-05-15 09:25:04.000000 ykdl-1.8.1.post1/ykdl.egg-info/top_level.txt
--rw-rw-rw-   0        0        0        2 2022-01-06 16:51:32.000000 ykdl-1.8.1.post1/ykdl.egg-info/zip-safe
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.663990 ykdl-1.8.2/
+-rw-rw-rw-   0        0        0     7385 2023-07-23 01:50:13.000000 ykdl-1.8.2/CHANGELOG.rst
+-rw-rw-rw-   0        0        0     1368 2022-01-08 13:30:55.000000 ykdl-1.8.2/LICENSE.txt
+-rw-rw-rw-   0        0        0       61 2020-01-21 09:08:48.000000 ykdl-1.8.2/MANIFEST.in
+-rw-rw-rw-   0        0        0     4711 2023-07-23 01:52:01.705998 ykdl-1.8.2/PKG-INFO
+-rw-rw-rw-   0        0        0     2091 2022-01-08 13:30:25.000000 ykdl-1.8.2/README.rst
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.309940 ykdl-1.8.2/cykdl/
+-rw-rw-rw-   0        0        0        0 2020-01-21 09:08:48.000000 ykdl-1.8.2/cykdl/__init__.py
+-rw-rw-rw-   0        0        0    14748 2022-10-30 03:52:47.000000 ykdl-1.8.2/cykdl/__main__.py
+-rw-rw-rw-   0        0        0      230 2022-11-08 13:05:50.000000 ykdl-1.8.2/pyproject.toml
+-rw-rw-rw-   0        0        0      111 2023-07-23 01:52:01.707999 ykdl-1.8.2/setup.cfg
+-rw-rw-rw-   0        0        0     2653 2022-10-13 00:39:16.000000 ykdl-1.8.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.356940 ykdl-1.8.2/ykdl/
+-rw-rw-rw-   0        0        0       34 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/__init__.py
+-rw-rw-rw-   0        0        0     3321 2022-12-04 15:02:51.000000 ykdl-1.8.2/ykdl/common.py
+-rw-rw-rw-   0        0        0     4202 2022-12-10 09:07:58.000000 ykdl-1.8.2/ykdl/compact.py
+-rw-rw-rw-   0        0        0    11401 2023-06-13 14:35:24.000000 ykdl-1.8.2/ykdl/extractor.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.472952 ykdl-1.8.2/ykdl/extractors/
+-rw-rw-rw-   0        0        0        0 2020-01-21 09:08:48.000000 ykdl-1.8.2/ykdl/extractors/__init__.py
+-rw-rw-rw-   0        0        0     1855 2022-12-11 14:24:08.000000 ykdl-1.8.2/ykdl/extractors/_byted.py
+-rw-rw-rw-   0        0        0    71721 2021-03-04 08:04:12.000000 ykdl-1.8.2/ykdl/extractors/_byted_acrawler.js
+-rw-rw-rw-   0        0        0     1015 2022-12-10 09:01:14.000000 ykdl-1.8.2/ykdl/extractors/_common.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.478953 ykdl-1.8.2/ykdl/extractors/acfun/
+-rw-rw-rw-   0        0        0      235 2022-12-09 06:01:02.000000 ykdl-1.8.2/ykdl/extractors/acfun/__init__.py
+-rw-rw-rw-   0        0        0     1164 2022-12-08 17:18:00.000000 ykdl-1.8.2/ykdl/extractors/acfun/acbase.py
+-rw-rw-rw-   0        0        0     2128 2022-12-08 17:22:54.000000 ykdl-1.8.2/ykdl/extractors/acfun/bangumi.py
+-rw-rw-rw-   0        0        0     3043 2022-12-10 09:35:00.000000 ykdl-1.8.2/ykdl/extractors/acfun/live.py
+-rw-rw-rw-   0        0        0     1561 2022-12-08 17:20:18.000000 ykdl-1.8.2/ykdl/extractors/acfun/video.py
+-rw-rw-rw-   0        0        0     1145 2022-12-08 14:23:38.000000 ykdl-1.8.2/ykdl/extractors/baomihua.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.488955 ykdl-1.8.2/ykdl/extractors/bilibili/
+-rw-rw-rw-   0        0        0     1416 2022-11-04 14:46:14.000000 ykdl-1.8.2/ykdl/extractors/bilibili/__init__.py
+-rw-rw-rw-   0        0        0     2967 2023-07-23 01:13:20.000000 ykdl-1.8.2/ykdl/extractors/bilibili/bangumi.py
+-rw-rw-rw-   0        0        0     2127 2022-12-07 18:17:00.000000 ykdl-1.8.2/ykdl/extractors/bilibili/bilibase.py
+-rw-rw-rw-   0        0        0     1046 2022-03-28 07:51:10.000000 ykdl-1.8.2/ykdl/extractors/bilibili/idconvertor.py
+-rw-rw-rw-   0        0        0     5884 2022-12-10 09:29:22.000000 ykdl-1.8.2/ykdl/extractors/bilibili/live.py
+-rw-rw-rw-   0        0        0      596 2022-11-07 04:20:22.000000 ykdl-1.8.2/ykdl/extractors/bilibili/util.py
+-rw-rw-rw-   0        0        0      817 2022-12-08 14:33:00.000000 ykdl-1.8.2/ykdl/extractors/bilibili/vc.py
+-rw-rw-rw-   0        0        0     2446 2022-12-04 08:44:06.000000 ykdl-1.8.2/ykdl/extractors/bilibili/video.py
+-rw-rw-rw-   0        0        0     1727 2022-12-08 14:55:22.000000 ykdl-1.8.2/ykdl/extractors/cctv.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.492956 ykdl-1.8.2/ykdl/extractors/douban/
+-rw-rw-rw-   0        0        0      361 2022-10-31 22:02:18.000000 ykdl-1.8.2/ykdl/extractors/douban/__init__.py
+-rw-rw-rw-   0        0        0      842 2022-12-08 14:33:18.000000 ykdl-1.8.2/ykdl/extractors/douban/movie.py
+-rw-rw-rw-   0        0        0     1686 2022-12-08 20:46:42.000000 ykdl-1.8.2/ykdl/extractors/douban/music.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.495956 ykdl-1.8.2/ykdl/extractors/douyin/
+-rw-rw-rw-   0        0        0      296 2022-11-27 08:54:43.000000 ykdl-1.8.2/ykdl/extractors/douyin/__init__.py
+-rw-rw-rw-   0        0        0     3102 2023-07-23 00:58:45.000000 ykdl-1.8.2/ykdl/extractors/douyin/live.py
+-rw-rw-rw-   0        0        0     1633 2023-06-28 09:52:42.000000 ykdl-1.8.2/ykdl/extractors/douyin/video.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.501958 ykdl-1.8.2/ykdl/extractors/douyu/
+-rw-rw-rw-   0        0        0      200 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/douyu/__init__.py
+-rw-rw-rw-   0        0        0     6609 2020-01-21 09:08:48.000000 ykdl-1.8.2/ykdl/extractors/douyu/crypto-js-md5.min.js
+-rw-rw-rw-   0        0        0     3521 2022-12-08 14:44:56.000000 ykdl-1.8.2/ykdl/extractors/douyu/live.py
+-rw-rw-rw-   0        0        0     3338 2022-11-30 14:27:02.000000 ykdl-1.8.2/ykdl/extractors/douyu/util.py
+-rw-rw-rw-   0        0        0     1519 2022-12-08 14:46:26.000000 ykdl-1.8.2/ykdl/extractors/douyu/video.py
+-rw-rw-rw-   0        0        0     5550 2022-12-08 21:08:32.000000 ykdl-1.8.2/ykdl/extractors/fun.py
+-rw-rw-rw-   0        0        0     3955 2022-11-29 09:51:26.000000 ykdl-1.8.2/ykdl/extractors/generalembed.py
+-rw-rw-rw-   0        0        0     2718 2022-12-08 21:08:52.000000 ykdl-1.8.2/ykdl/extractors/generalsimple.py
+-rw-rw-rw-   0        0        0   111557 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/heibaizhibo.m.js
+-rw-rw-rw-   0        0        0     2745 2022-12-08 14:52:08.000000 ykdl-1.8.2/ykdl/extractors/heibaizhibo.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.504958 ykdl-1.8.2/ykdl/extractors/huajiao/
+-rw-rw-rw-   0        0        0      172 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/huajiao/__init__.py
+-rw-rw-rw-   0        0        0     2054 2022-12-08 21:38:20.000000 ykdl-1.8.2/ykdl/extractors/huajiao/live.py
+-rw-rw-rw-   0        0        0     1365 2022-12-08 14:34:22.000000 ykdl-1.8.2/ykdl/extractors/huajiao/video.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.508959 ykdl-1.8.2/ykdl/extractors/huya/
+-rw-rw-rw-   0        0        0      173 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/huya/__init__.py
+-rw-rw-rw-   0        0        0     3696 2022-12-08 21:42:48.000000 ykdl-1.8.2/ykdl/extractors/huya/live.py
+-rw-rw-rw-   0        0        0     1935 2022-12-08 20:52:03.000000 ykdl-1.8.2/ykdl/extractors/huya/video.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.512960 ykdl-1.8.2/ykdl/extractors/ifeng/
+-rw-rw-rw-   0        0        0      238 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/ifeng/__init__.py
+-rw-rw-rw-   0        0        0      725 2022-12-08 14:35:14.000000 ykdl-1.8.2/ykdl/extractors/ifeng/gongkaike.py
+-rw-rw-rw-   0        0        0     1355 2022-12-08 14:54:24.000000 ykdl-1.8.2/ykdl/extractors/ifeng/news.py
+-rw-rw-rw-   0        0        0      853 2022-12-08 14:35:44.000000 ykdl-1.8.2/ykdl/extractors/ifeng/video.py
+-rw-rw-rw-   0        0        0      571 2022-05-12 21:45:32.000000 ykdl-1.8.2/ykdl/extractors/iqilu.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.522962 ykdl-1.8.2/ykdl/extractors/iqiyi/
+-rw-rw-rw-   0        0        0      337 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/iqiyi/__init__.py
+-rw-rw-rw-   0        0        0   125305 2020-01-21 09:08:48.000000 ykdl-1.8.2/ykdl/extractors/iqiyi/cmd5x.js
+-rw-rw-rw-   0        0        0    91151 2019-10-24 05:42:40.000000 ykdl-1.8.2/ykdl/extractors/iqiyi/cmd5x_iqiyi3.js
+-rw-rw-rw-   0        0        0     3142 2022-12-08 14:35:58.000000 ykdl-1.8.2/ykdl/extractors/iqiyi/live.py
+-rw-rw-rw-   0        0        0     1879 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/iqiyi/util.py
+-rw-rw-rw-   0        0        0     9605 2023-07-23 01:24:24.000000 ykdl-1.8.2/ykdl/extractors/iqiyi/video.py
+-rw-rw-rw-   0        0        0     2915 2022-12-11 14:39:10.000000 ykdl-1.8.2/ykdl/extractors/ixigua.py
+-rw-rw-rw-   0        0        0      710 2022-12-08 14:26:02.000000 ykdl-1.8.2/ykdl/extractors/joy.py
+-rw-rw-rw-   0        0        0     1351 2022-12-08 14:26:08.000000 ykdl-1.8.2/ykdl/extractors/kankanews.py
+-rw-rw-rw-   0        0        0      790 2022-12-04 09:37:28.000000 ykdl-1.8.2/ykdl/extractors/ku6.py
+-rw-rw-rw-   0        0        0     2087 2022-12-08 21:10:24.000000 ykdl-1.8.2/ykdl/extractors/kuwo.py
+-rw-rw-rw-   0        0        0     1620 2022-12-08 14:26:40.000000 ykdl-1.8.2/ykdl/extractors/laifeng.py
+-rw-rw-rw-   0        0        0     4886 2022-12-08 21:11:26.000000 ykdl-1.8.2/ykdl/extractors/le.py
+-rw-rw-rw-   0        0        0     1201 2022-12-08 14:27:18.000000 ykdl-1.8.2/ykdl/extractors/lizhi.py
+-rw-rw-rw-   0        0        0     1126 2022-12-08 14:27:24.000000 ykdl-1.8.2/ykdl/extractors/longzhu.py
+-rw-rw-rw-   0        0        0     3327 2022-12-09 05:56:32.000000 ykdl-1.8.2/ykdl/extractors/mgtv.py
+-rw-rw-rw-   0        0        0     2851 2022-12-08 21:16:40.000000 ykdl-1.8.2/ykdl/extractors/miaopai.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.580973 ykdl-1.8.2/ykdl/extractors/netease/
+-rw-rw-rw-   0        0        0      557 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/netease/__init__.py
+-rw-rw-rw-   0        0        0     1026 2022-12-08 14:37:20.000000 ykdl-1.8.2/ykdl/extractors/netease/live.py
+-rw-rw-rw-   0        0        0     3056 2022-12-08 14:50:04.000000 ykdl-1.8.2/ykdl/extractors/netease/livecc.py
+-rw-rw-rw-   0        0        0      614 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/netease/m3g.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.587975 ykdl-1.8.2/ykdl/extractors/netease/music/
+-rw-rw-rw-   0        0        0      341 2022-01-08 13:30:25.000000 ykdl-1.8.2/ykdl/extractors/netease/music/__init__.py
+-rw-rw-rw-   0        0        0     1198 2022-12-07 06:36:36.000000 ykdl-1.8.2/ykdl/extractors/netease/music/music.py
+-rw-rw-rw-   0        0        0     3065 2022-12-08 14:38:00.000000 ykdl-1.8.2/ykdl/extractors/netease/music/musicbase.py
+-rw-rw-rw-   0        0        0     1211 2022-12-08 14:38:06.000000 ykdl-1.8.2/ykdl/extractors/netease/music/mv.py
+-rw-rw-rw-   0        0        0      819 2022-12-07 06:37:00.000000 ykdl-1.8.2/ykdl/extractors/netease/music/program.py
+-rw-rw-rw-   0        0        0     4405 2022-12-10 09:03:58.000000 ykdl-1.8.2/ykdl/extractors/netease/openc.py
+-rw-rw-rw-   0        0        0      878 2022-12-08 14:37:54.000000 ykdl-1.8.2/ykdl/extractors/netease/video.py
+-rw-rw-rw-   0        0        0     2830 2022-12-08 14:28:32.000000 ykdl-1.8.2/ykdl/extractors/pps.py
+-rw-rw-rw-   0        0        0     2545 2022-12-08 21:17:18.000000 ykdl-1.8.2/ykdl/extractors/pptv.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.591976 ykdl-1.8.2/ykdl/extractors/qq/
+-rw-rw-rw-   0        0        0      235 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/qq/__init__.py
+-rw-rw-rw-   0        0        0     1765 2022-12-07 10:32:58.000000 ykdl-1.8.2/ykdl/extractors/qq/egame.py
+-rw-rw-rw-   0        0        0     1030 2022-12-07 07:49:14.000000 ykdl-1.8.2/ykdl/extractors/qq/live.py
+-rw-rw-rw-   0        0        0     8831 2022-12-08 21:02:55.000000 ykdl-1.8.2/ykdl/extractors/qq/video.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.631984 ykdl-1.8.2/ykdl/extractors/sina/
+-rw-rw-rw-   0        0        0      242 2021-11-27 03:45:05.000000 ykdl-1.8.2/ykdl/extractors/sina/__init__.py
+-rw-rw-rw-   0        0        0      492 2022-12-08 15:10:56.000000 ykdl-1.8.2/ykdl/extractors/sina/embed.py
+-rw-rw-rw-   0        0        0     2399 2022-12-07 16:01:10.000000 ykdl-1.8.2/ykdl/extractors/sina/openc.py
+-rw-rw-rw-   0        0        0     1599 2022-12-08 15:11:54.000000 ykdl-1.8.2/ykdl/extractors/sina/video.py
+-rw-rw-rw-   0        0        0     3684 2022-12-08 14:28:48.000000 ykdl-1.8.2/ykdl/extractors/singlemultimedia.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.636984 ykdl-1.8.2/ykdl/extractors/sohu/
+-rw-rw-rw-   0        0        0      488 2022-12-08 08:13:42.000000 ykdl-1.8.2/ykdl/extractors/sohu/__init__.py
+-rw-rw-rw-   0        0        0      279 2021-11-27 03:45:06.000000 ykdl-1.8.2/ykdl/extractors/sohu/my.py
+-rw-rw-rw-   0        0        0     4289 2022-12-08 12:54:32.000000 ykdl-1.8.2/ykdl/extractors/sohu/sohubase.py
+-rw-rw-rw-   0        0        0     1172 2022-12-08 14:20:40.000000 ykdl-1.8.2/ykdl/extractors/sohu/tv.py
+-rw-rw-rw-   0        0        0      313 2021-11-27 03:45:06.000000 ykdl-1.8.2/ykdl/extractors/tudou.py
+-rw-rw-rw-   0        0        0     4227 2023-06-18 08:41:26.000000 ykdl-1.8.2/ykdl/extractors/weibo.py
+-rw-rw-rw-   0        0        0      804 2022-12-08 14:30:10.000000 ykdl-1.8.2/ykdl/extractors/yinyuetai.py
+-rw-rw-rw-   0        0        0      840 2022-12-08 14:30:16.000000 ykdl-1.8.2/ykdl/extractors/yizhibo.py
+-rw-rw-rw-   0        0        0     5849 2022-12-08 21:36:30.000000 ykdl-1.8.2/ykdl/extractors/youku.py
+-rw-rw-rw-   0        0        0     5626 2021-11-27 03:45:06.000000 ykdl-1.8.2/ykdl/extractors/youkujs.py
+-rw-rw-rw-   0        0        0      578 2021-11-27 03:45:06.000000 ykdl-1.8.2/ykdl/extractors/zhangyu.py
+-rw-rw-rw-   0        0        0     2385 2022-12-08 14:30:52.000000 ykdl-1.8.2/ykdl/extractors/zhanqi.py
+-rw-rw-rw-   0        0        0     1316 2022-12-08 14:31:38.000000 ykdl-1.8.2/ykdl/extractors/zhuafan.py
+-rw-rw-rw-   0        0        0    10403 2023-06-27 05:04:03.000000 ykdl-1.8.2/ykdl/mediainfo.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.661990 ykdl-1.8.2/ykdl/util/
+-rw-rw-rw-   0        0        0        0 2020-01-21 09:08:48.000000 ykdl-1.8.2/ykdl/util/__init__.py
+-rw-rw-rw-   0        0        0    13716 2022-11-08 16:05:15.000000 ykdl-1.8.2/ykdl/util/download.py
+-rw-rw-rw-   0        0        0     6957 2022-12-08 15:26:00.000000 ykdl-1.8.2/ykdl/util/external.py
+-rw-rw-rw-   0        0        0     3222 2022-12-01 10:38:46.000000 ykdl-1.8.2/ykdl/util/fs.py
+-rw-rw-rw-   0        0        0    24271 2023-06-12 16:27:46.000000 ykdl-1.8.2/ykdl/util/http.py
+-rw-rw-rw-   0        0        0     5597 2022-12-09 03:36:36.000000 ykdl-1.8.2/ykdl/util/human.py
+-rw-rw-rw-   0        0        0     1846 2023-05-01 17:21:28.000000 ykdl-1.8.2/ykdl/util/kt_player.py
+-rw-rw-rw-   0        0        0     5310 2023-06-20 16:43:20.000000 ykdl-1.8.2/ykdl/util/lazy.py
+-rw-rw-rw-   0        0        0     2366 2022-05-08 10:29:52.000000 ykdl-1.8.2/ykdl/util/log.py
+-rw-rw-rw-   0        0        0     3977 2023-06-12 16:34:59.000000 ykdl-1.8.2/ykdl/util/m3u8.py
+-rw-rw-rw-   0        0        0     3081 2022-12-07 10:32:34.000000 ykdl-1.8.2/ykdl/util/match.py
+-rw-rw-rw-   0        0        0    15633 2022-07-21 16:16:42.000000 ykdl-1.8.2/ykdl/util/rangefetch_server.py
+-rw-rw-rw-   0        0        0     7189 2022-12-08 21:35:20.000000 ykdl-1.8.2/ykdl/util/wrap.py
+-rw-rw-rw-   0        0        0     5149 2021-11-30 08:53:42.000000 ykdl-1.8.2/ykdl/util/xml2dict.py
+-rw-rw-rw-   0        0        0       22 2023-07-23 01:26:25.000000 ykdl-1.8.2/ykdl/version.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:52:01.366940 ykdl-1.8.2/ykdl.egg-info/
+-rw-rw-rw-   0        0        0     4711 2023-07-23 01:52:00.000000 ykdl-1.8.2/ykdl.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     3719 2023-07-23 01:52:00.000000 ykdl-1.8.2/ykdl.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 01:52:00.000000 ykdl-1.8.2/ykdl.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       46 2023-07-23 01:52:00.000000 ykdl-1.8.2/ykdl.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      168 2023-07-23 01:52:00.000000 ykdl-1.8.2/ykdl.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 01:52:00.000000 ykdl-1.8.2/ykdl.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0        2 2022-01-06 16:51:32.000000 ykdl-1.8.2/ykdl.egg-info/zip-safe
```

### Comparing `ykdl-1.8.1.post1/CHANGELOG.rst` & `ykdl-1.8.2/CHANGELOG.rst`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,25 @@
 Change Log for ykdl
 ===================
 
+1.8.2
+-----------
+
+- enable pep517
+- change API name from "vid" to "mid", step 1
+- add index item to MediaInfo for playlist
+- add util.lazy
+- fix compatibility with m3u8 3.5.0 (#621) @Joeky
+- fix default filename timestamp (#622) @a67878813
+- add new extractor: acfun.live
+- update GeneralSimple, Bilibili, Douban, DouYin, iQIYI, iXiGua, Huya, Weibo
+- move extractor from "le.le" to "le"
+- remove Baidu, iXiGua.live
+
+
 1.8.1.post1
 -----------
 
 - fix compatibility bug on Python 3.9 and below (#604)
 
 
 1.8.1
```

### Comparing `ykdl-1.8.1.post1/LICENSE.txt` & `ykdl-1.8.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/README.rst` & `ykdl-1.8.2/README.rst`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/cykdl/__main__.py` & `ykdl-1.8.2/cykdl/__main__.py`

 * *Files 3% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 
 from argparse import ArgumentParser
 import socket
 import ssl
 import json
 import ast
 from urllib.request import ProxyHandler, HTTPSHandler, getproxies
-from urllib.parse import urlparse
+from urllib.parse import urlsplit
 from tempfile import NamedTemporaryFile
 from types import GeneratorType
 
 import logging
 logger = logging.getLogger('YKDL')
 
 from ykdl.common import url_to_module
@@ -55,14 +55,16 @@
     parser.add_argument('--no-http-cache', action='store_true', default=False, help='Do not allow HTTP cache')
     parser.add_argument('-s', '--start', type=int, default=-1, metavar='INDEX_NUM', help='Start from INDEX to play/download playlist, default -1, index at media of current URL')
     parser.add_argument('-j', '--jobs', type=int, default=8, metavar='NUM', help='Number of jobs for multiprocess download')
     parser.add_argument('--debug', action='store_true', default=False, help='Print debug messages from ykdl')
     parser.add_argument('video_urls', type=str, nargs='*', help='video urls, leave empty then enter interactive mode')
     global args
     args = parser.parse_args(argv)
+    if args.start > 0:
+        args.start -= 1
 
 def clean_slices(name, ext, lenth):
     for i in range(lenth):
         file_name = '%s_%d.%s' % (name, i, ext)
         os.remove(file_name)
 
 def fix_sa_name(name, ext, lenth):
@@ -84,15 +86,15 @@
     if m3u8:
         m3u8_crypto = crypto_m3u8(url)
         # rebuild m3u8 urls when use internal downloader,
         # change the ext to segment's ext, default is "ts",
         # otherwise change the ext to "flv" or "mp4".
         if internal:
             urls, audio, subtitle = load_m3u8(url)
-            ext = urlparse(urls[0])[2].split('.')[-1]
+            ext = urlsplit(urls[0]).path.split('.')[-1]
             if ext not in ['ts', 'm4s', 'mp4', 'm4a']:
                 ext = 'ts'
         elif live:
             ext = 'flv'
         else:
             ext = 'mp4'
     elif ext == 'mpd':
@@ -185,15 +187,15 @@
         return
     urls = info.streams[stream_id]['src']
     name = args.output_name
     if name:
         if '\\u' in name:
             name = literalize(name)
         if info.index is not None:
-            name = name + '_' + str(info.index)
+            name = name + '_' + str(info.index[0])
     else:
         name = info.build_file_name(stream_id)
 
     ext = info.streams[stream_id]['container']
     live = info.live
     if args.player:
         player_args = info.extra
@@ -334,15 +336,19 @@
     while True:
         try:
             video = input('YKDL> ').strip()
         except KeyboardInterrupt:
              sys.exit()
         if not video:
             continue
-        if video == 'exit':
+        cmd = video.strip().lower()
+        if cmd == 'cache clear':
+            http.cache_clear()
+            continue
+        if cmd == 'exit':
             sys.exit()
         try:
             handle_video(video)
         except KeyboardInterrupt:
             logger.warning('\nInterrupted by Ctrl-C, press Ctrl-C again to exit YKDL.')
         except Exception as e:
             errmsg = str(e)
```

### Comparing `ykdl-1.8.1.post1/setup.py` & `ykdl-1.8.2/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -27,29 +27,33 @@
   'br': ['BrotliCFFI'],
 }
 EXT['net'] = sum(EXT.values(), [])
 EXT['js'] = ['quickjs']
 EXT['all'] = list(set(sum((EXT.values()), [])))
 
 here = os.path.abspath(os.path.dirname(__file__))
-README = read_file('README.rst')
-CHANGES = read_file('CHANGELOG.rst')
+LONGS = '\n\n'.join((
+    read_file('README.rst'),
+    *read_file('CHANGELOG.rst').split('\n\n\n')[:4],
+    '`See full change log '
+    '<https://github.com/SeaHOH/ykdl/blob/master/CHANGELOG.rst>`_.\n'
+))
 
 
 setup(
     name = 'ykdl',
     version = get_version(),
     author = 'Zhang Ning',
     author_email = 'zhangn1985@gmail.com',
     maintainer = 'SeaHOH',
     maintainer_email = 'seahoh@gmail.com',
     url = 'https://github.com/SeaHOH/ykdl',
     license = 'MIT',
     description = 'a video downloader written in Python',
-    long_description = README + '\n\n' +  CHANGES,
+    long_description = LONGS,
     keywords = 'video download youku acfun bilibili',
     packages = find_packages(here),
     install_requires = REQ,
     extras_require = EXT,
     platforms = 'any',
     zip_safe = True,
     package_data = {
```

### Comparing `ykdl-1.8.1.post1/ykdl/common.py` & `ykdl-1.8.2/ykdl/common.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,15 +11,14 @@
 # TODO: add support to find module via mid@site[.type]
 
 alias = reverse_list_dict({
     'acfun'     : ['aixifan'],
     'cctv'      : ['cntv'],
     'douyin'    : ['amemv', 'iesdouyin'],
     'douyu'     : ['douyutv'],
-    'le'        : ['letv'],
     'netease'   : ['163'],
     'qq'        : ['wetv'],
     'sina'      : ['iask'],
     'weibo'     : ['weibocdn'],
 })
 exclude_list = {'com', 'net', 'org'}
```

### Comparing `ykdl-1.8.1.post1/ykdl/compact.py` & `ykdl-1.8.2/ykdl/compact.py`

 * *Files 4% similar despite different names*

```diff
@@ -2,21 +2,36 @@
 import sys
 import io
 import socket
 import random
 import inspect
 import logging
 import tempfile
+import builtins
+import functools
 
 from .util.log import ColorHandler
 
 
 logging.basicConfig(handlers=[ColorHandler()])
 
 
+builtins.Infinity = float('inf')
+
+
+try:
+    functools.cache
+except AttributeError:
+    exec('''\
+def cache(user_function, /):
+    'Simple lightweight unbounded cache.  Sometimes called "memoize".'
+    return lru_cache(maxsize=None)(user_function)
+''', functools.__dict__)
+
+
 if sys.version_info < (3, 10):
     import types
     types.NoneType = type(None)
 
 
 def bound_monkey_patch(orig, new):
     '''Monkey patch the original function with new, and bind the original
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/_byted.py` & `ykdl-1.8.2/ykdl/extractors/_byted.py`

 * *Files 16% similar despite different names*

```diff
@@ -11,17 +11,14 @@
 '''
 js_acrawler = None
 
 def get_cookies_d(url):
     return {c.name: c.value
             for c in get_cookies(urlsplit(url).hostname, '/')}
 
-def cd2cs(cd):
-    return ';'.join('='.join(kv) for kv in cd.items())
-
 def get_signer(url):
     assert JSEngine, "No JS Interpreter found, can't load byted acrawler!"
     global js_acrawler
     if js_acrawler is None:
         js_acrawler = get_pkgdata_str(__name__, '_byted_acrawler.js',
                       'https://lf3-cdn-tos.bytescm.com/obj/rc-web-sdk/acrawler.js')
 
@@ -30,39 +27,36 @@
 
     def sign(*args):
         return js_ctx.call('byted_acrawler.sign', *args)
 
     return sign
 
 def get_signed_cookies(url):
-    assert JSEngine, "No JS Interpreter found, can't load byted acrawler!"
-    install_cookie()
-    get_response(url)
-    cookies = get_cookies_d(url)
-    cookies.update({
-        '__ac_signature': get_signer(url)('', cookies['__ac_nonce']),
-        '__ac_referer': '__ac_blank'
-    })
-    uninstall_cookie()
-    return cd2cs(cookies)
+    #assert JSEngine, "No JS Interpreter found, can't load byted acrawler!"
+    __ac_nonce = get_random_id(21)
+    _cookies['signed'] = cookies = {
+        '__ac_nonce': __ac_nonce,
+        #'__ac_signature': get_signer(url)('', __ac_nonce),
+        #'__ac_referer': '__ac_blank'
+    }
+    return cookies
 
 def get_ttwid_cookies(url):
     install_cookie()
-    get_response(url)
-    cookies = get_cookies_d(url)
-    cookies['ttwid_date'] = '1'
-    get_response(url, headers={'Cookie': cd2cs(cookies)})
-    cookies = get_cookies_d(url)
+    _cookies['ttwid'] = cookies = {
+        '__ac_nonce': get_random_id(21),
+        'ttwid_date': '1'
+    }
+    get_response(url, headers={'Cookie': cookies})
+    cookies.update(get_cookies_d(url))
     uninstall_cookie()
-    return cd2cs(cookies)
+    return cookies
 
-cookies = None
+_cookies = {}
 _get_content = get_content
 
 def get_content(url):
-    global cookies
-    if cookies is None:
-        if 'douyin.' in url:
-            cookies = get_signed_cookies(url)
-        elif 'ixigua.' in url:
-            cookies = get_ttwid_cookies(url)
+    if 'douyin.' in url:
+        cookies = _cookies.get('signed') or get_signed_cookies(url)
+    elif 'ixigua.' in url:
+        cookies = _cookies.get('ttwid') or get_ttwid_cookies(url)
     return _get_content(url, headers={'Cookie': cookies})
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/_byted_acrawler.js` & `ykdl-1.8.2/ykdl/extractors/_byted_acrawler.js`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/acfun/acbase.py` & `ykdl-1.8.2/ykdl/extractors/acfun/acbase.py`

 * *Files 15% similar despite different names*

```diff
@@ -12,33 +12,32 @@
          540: 'HD',
          360: 'SD',
          270: 'LD'
     }
 
     def prepare(self):
         info = MediaInfo(self.name)
+
+        self.mid  # scan & check
         html = get_content(self.url)
-        info.title, info.artist, sourceVid, m3u8Info = self.get_page_info(html)
+        info.title, info.artist, sourceVid, data = self.get_page_info(html)
+
+        data = json.loads(data)['adaptationSet'][0]['representation']
+        self.logger.debug('data:\n%s', data)
 
-        m3u8Info = json.loads(m3u8Info)['adaptationSet'][0]['representation']
-        self.logger.debug('m3u8Info:\n%s', m3u8Info)
         url = random.choice(['url', 'backupUrl'])
-        for q in m3u8Info:
+        for q in data:
             quality = int(match1(q['qualityType'], '(\d+)'))
-            stream_type = self.quality_2_id[quality]
+            stream_id = self.quality_2_id[quality]
             if q['frameRate'] > 30:
-                stream_type += '-f' + str(int(q['frameRate'] + 0.1))
+                stream_id += '-f' + str(int(q['frameRate'] + 0.1))
             stream_profile = q['qualityLabel']
             urls = q[url]
             if not isinstance(urls, list):
                 urls = [urls]
-            info.streams[stream_type] = {
+            info.streams[stream_id] = {
                 'container': 'm3u8',
-                'video_profile': stream_profile,
-                'src': urls,
-                'size': 0
+                'profile': stream_profile,
+                'src': urls
             }
 
         return info
-
-    def prepare_list(self):
-        return ['https://www.acfun.cn' + p for p in self.get_path_list()]
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/acfun/video.py` & `ykdl-1.8.2/ykdl/extractors/acfun/video.py`

 * *Files 14% similar despite different names*

```diff
@@ -25,13 +25,25 @@
         if m3u8Info:
             m3u8Info = m3u8Info[0]
         else:
             m3u8Info = videoInfo.get('ksPlayJson')
 
         return title, artist, sourceVid, m3u8Info
 
-    def get_path_list(self):
+    def format_mid(self, mid):
+        assert fullmatch(mid, '(ac)?\d+')
+        mid = match1(mid, '(\d+)')
+        # force rebuild url for list index
+        self.url = 'https://www.acfun.cn/v/ac{mid}'.format(**vars())
+        return mid
+
+    def prepare_mid(self):
+        return match1(self.url, 'v/ac(\d+)', r'\bac=(\d+)')
+
+    def prepare_list(self):
         html = get_content(self.url)
-        videos = matchall(html, 'href=[\'"](/v/[a-zA-Z0-9_]+)[\'"] title=[\'"]')
+        videos = ['https://www.acfun.cn' + path for path in
+                  matchall(html, 'href=[\'"](/v/ac[0-9_]+)[\'"] title=[\'"]')]
+        self.set_index(self.url, videos)
         return videos
 
 site = AcVideo()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/baidu/music.py` & `ykdl-1.8.2/ykdl/extractors/netease/video.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,45 +1,34 @@
 # -*- coding: utf-8 -*-
 
 from .._common import *
 
 
-class BaiduMusic(Extractor):
-    name = 'BaiduMusic (百度音乐)'
+class NeteaseVideo(Extractor):
+    name = '网易视频 (163)'
 
+    def prepare_mid(self):
+        return match1(self.url, '(\w+)\.html')
 
     def prepare(self):
         info = MediaInfo(self.name)
-        if not self.vid:
-            self.vid = match1(self.url, 'http://music.baidu.com/song/([\d]+)')
-
-        api = 'http://play.baidu.com/data/music/songlink'
-        data = {'songIds': self.vid}
-        song_data = get_response(api, data=data).json()['data']['songList'][0]
-
-        info.title = song_data['songName']
-        info.artist = song_data['artistName']
 
+        data = get_response('https://so.v.163.com/v6/video/videodetail.do',
+                            params={
+                               'vid': self.mid,
+                               'adapter': 1
+                            }).json()
+        assert data['code'] == 1, data['msg']
+        data = data['data']
+
+        info.title = data['title']
+        info.artist = data.get('username')
+        info.add_comment(data['keywords'])
         info.streams['current'] = {
-            'container': song_data['format'],
-            'video_profile': 'current',
-            'src' : [song_data['songLink']],
-            'size': song_data['size']
-        }
-        return info
-
-    def prepare_list(self):
-
-        album_id = match1(self.url, 'http://music.baidu.com/album/([\d]+)')
-        api = 'http://play.baidu.com/data/music/box/album'
-        params = {
-            'albumId': album_id,
-            'type': 'album',
-            '_': time.time()
+            'container': 'mp4',
+            'profile': 'current',
+            'src': [data['url']]
         }
-        data = get_response(api, params=params).json()
 
-        self.logger.info('album:\n\t%s', data['data']['albumName'])
-
-        return data['data']['songIdList']
+        return info
 
-site = BaiduMusic()
+site = NeteaseVideo()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/baomihua.py` & `ykdl-1.8.2/ykdl/extractors/baomihua.py`

 * *Files 13% similar despite different names*

```diff
@@ -3,38 +3,38 @@
 from ._common import *
 
 
 class Baomihua(Extractor):
     # https://www.baomihua.com/
     name = '爆米花（Baomihua)'
 
-    def prepare(self):
+    def prepare_mid(self):
+        return match1(self.url, '_(\d+)', 'm/(\d+)', 'v/(\d+)')
 
+    def prepare(self):
         info = MediaInfo(self.name)
-        if self.url:
-            self.vid = match1(self.url, '_(\d+)', 'm/(\d+)', 'v/(\d+)')
 
-        add_header('Referer', 'https://m.video.baomihua.com/')
+        add_header('Referer', 'https://m.mideo.baomihua.com/')
         data = get_response('https://play.baomihua.com/getvideourl.aspx',
                             params={
-                                'flvid': self.vid,
+                                'flvid': self.mid,
                                 'datatype': 'json',
                                 'devicetype': 'wap'
                             }).json()
 
         info.title = data['title']
         host = data['host']
         stream_name = data['stream_name']
         t = data['videofiletype']
         size = int(data['videofilesize'])
 
         hls = data['ishls']
         url = 'http://{host}/{hls}/{stream_name}.{t}'.format(**vars())
         info.streams['current'] = {
-            'video_profile': 'current',
             'container': t,
-            'src': [url],
-            'size' : size
+            'profile': 'current',
+            'src' : [url],
+            'size': size
         }
         return info
 
 site = Baomihua()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/bilibili/__init__.py` & `ykdl-1.8.2/ykdl/extractors/bilibili/__init__.py`

 * *Files 11% similar despite different names*

```diff
@@ -15,27 +15,31 @@
         return s.site, url
     elif '/bangumi/' in url:
         from . import bangumi as s
         return s.site, url
 
     page_index = match1(url, '(?:page|\?p)=(\d+)', 'index_(\d+)\.') or '1'
 
-    av_id = match1(url, '(?:/av|aid=)(\d+)')
-    if av_id:
-        bv_id = av2bv(av_id)
-    else:
-        bv_id = match1(url, '((?:BV|bv)[0-9A-Za-z]{10})')
+    bv_id = match1(url, r'\b((?:BV|bv)[0-9A-Za-z]{10})')
+    if not bv_id:
+        av_id = match1(url, r'\b(?:av|aid=)(\d+)')
+        if av_id:
+            bv_id = av2bv(av_id)
 
     if bv_id:
-        try:
-            url = get_media_data(bv_id)['redirect_url']
-        except AssertionError:
-            raise
-        except:
-            url = 'https://www.bilibili.com/video/' + bv_id
+        data = get_media_data(bv_id)
+        forward = data.get('forward')
+        if forward:
+            from .video import site
+            forward = av2bv(forward)
+            site.logger.warning('视频撞车了! 从 %s 跳转至首发 %s', bv_id, forward)
+            bv_id = forward
+            data = get_media_data(bv_id)
+        url = data.get('redirect_url') or \
+              'https://www.bilibili.com/video/{bv_id}/'.format(**vars())
     else:
         url = get_location(url)
 
     if '/bangumi/' in url:
         from . import bangumi as s
     else:
         if page_index > '1':
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/bilibili/bilibase.py` & `ykdl-1.8.2/ykdl/extractors/bilibili/bilibase.py`

 * *Files 4% similar despite different names*

```diff
@@ -17,17 +17,15 @@
         }
 
     def prepare(self):
         info = MediaInfo(self.name)
         info.extra.referer = 'https://www.bilibili.com/'
         info.extra['ua'] = fake_headers['User-Agent']
 
-        self.vid, info.title, info.artist = self.get_page_info()
-
-        assert self.vid, "can't play this video: " + self.url
+        self.get_page_info(info)
 
         def get_video_info(qn=0):
             # need login with high qn
             if qn == 74 or qn > 80:
                 return
 
             api_url = self.get_api_url(qn)
@@ -47,15 +45,15 @@
             elif 'flv' in fmt:
                 ext = 'flv'
             st, prf = self.format_2_type_profile[fmt]
             if urls:
                 st += '-' + str(data['quality'])
                 info.streams[st] = {
                     'container': ext,
-                    'video_profile': prf,
+                    'profile': prf,
                     'src' : urls,
                     'size': size
                 }
 
             if qn == 0:
                 aqlts = data['accept_quality'].split(',')
                 aqlts.remove(str(data['quality']))
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/bilibili/idconvertor.py` & `ykdl-1.8.2/ykdl/extractors/bilibili/idconvertor.py`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/bilibili/live.py` & `ykdl-1.8.2/ykdl/extractors/bilibili/live.py`

 * *Files 20% similar despite different names*

```diff
@@ -13,50 +13,64 @@
         '蓝光': 'BD',
         '超清': 'TD',
         '高清': 'HD',
         '流畅': 'SD'
     }
 
     def live_status(self):
-        id = match1(self.url, '/(\d+)')
+        mid = self.mid[0]
         data = get_response(
                 'https://api.live.bilibili.com/room/v1/Room/room_init',
-                params={'id': id}, cache=False).json()
+                params={'id': mid}, cache=False).json()
         assert data['code'] == 0, data['msg']
         data = data['data']
 
-        self.vid = data['room_id'], str(data['uid'])
+        self.mid = mid, data['room_id'], str(data['uid'])
         live_status = data['live_status']
 
         assert not data['is_locked'], '房间已封禁'
         assert not data['encrypted'], '房间已加密'
         assert live_status > 0, '主播正在觅食......'
 
         return live_status
 
     def list_only(self):
         return self.live_status() == 2
 
+    @staticmethod
+    def format_mid(mid):
+        # [0]:  web room id
+        # [1]: real room id
+        # [2]:      user id
+        if not isinstance(mid, tuple):
+            mid = (mid, )
+        wrid = fullmatch(mid[0], '\d+')
+        assert wrid
+        return wrid, *mid[1:]
+
+    def prepare_mid(self):
+        return match1(self.url, '/(\d+)')
+
     def prepare(self):
         info = MediaInfo(self.name, True)
-        room_id, uid = self.vid
 
+        _, room_id, uid = self.mid
         data = get_response(
                 'https://api.live.bilibili.com/room/v1/Room/get_status_info_by_uids',
                 params={'uids[]': uid}, cache=False).json()
         assert data['code'] == 0, data['msg']
         data = data['data'][uid]
 
-        info.title = '{data[title]} - {data[uname]}'.format(**vars())
+        info.title = '{title} - {uname}'.format(**data)
+        info.artist = data['uname']
         info.add_comment(data['tag_name'])
 
         g_qn_desc = None
         aqlts = set()
         aqlts_p = set()
-        size = float('inf')
 
         def get_live_info(qn=1):
             data = get_response(
                     'https://api.live.bilibili.com/xlive/web-room/v2/index/getRoomPlayInfo',
                     params={
                         'room_id': room_id,
                         'protocol': '0,1',    # 0 = http_stream, 1 = http_hls
@@ -88,26 +102,27 @@
                             ext = 'm3u8'
                             st += '-hls'
                         else:
                             ext = format['format_name']
                         if codec['codec_name'] == 'hevc':
                             st += '-h265'
                         if st in info.streams:
-                            self.logger.debug('skip stream: [ %s %s %s ]',
-                                              stream['protocol_name'],
-                                              format['format_name'],
-                                              codec['codec_name'],)
-                            continue
+                            st += '-bak'
+                        #    self.logger.debug('skip stream: [ %s %s %s ]',
+                        #                      stream['protocol_name'],
+                        #                      format['format_name'],
+                        #                      codec['codec_name'],)
+                        #    continue
                         url_info = random.choice(codec['url_info'])
                         url = url_info['host'] + codec['base_url'] + url_info['extra']
                         info.streams[st] = {
                             'container': ext,
-                            'video_profile': prf,
+                            'profile': prf,
                             'src' : [url],
-                            'size': size
+                            'size': Infinity
                         }
 
             if qn == 1:
                 aqlts.remove(qlt)
                 aqlts_p.add(qlt)
                 while aqlts:
                     qlt = aqlts.pop()
@@ -117,26 +132,39 @@
         get_live_info()
         info.extra.referer= 'https://live.bilibili.com/'
         return info
 
     def prepare_list(self):
         from .video import site
 
-        if self.vid is None:
+        try:
+            room_id = self.mid[1]
+        except IndexError:
             self.live_status()
-        room_id, uid = self.vid
+            room_id = self.mid[1]
         self.start = -1  # skip is not allowed
+        self.end = 0     # never show index
 
+        bvid_url_last = None
+        repeat_times = 0
+        stop_threshold = 2
         while True:
             data = get_response(
                     'https://api.live.bilibili.com/live/getRoundPlayVideo',
                     params={'room_id': room_id}, cache=False).json()
             assert data['code'] == 0, data['msg']
             bvid_url = data['data'].get('bvid_url')
             assert bvid_url, '轮播结束'
 
+            if bvid_url == bvid_url_last:
+                repeat_times += 1
+                assert repeat_times < stop_threshold, 'repeat'
+            else:
+                bvid_url_last = bvid_url
+                repeat_times = 0
+
             info = site.parser(bvid_url)
             info.site = '哔哩哔哩轮播'
             info.title = '(轮播) ' + info.title
             yield info
 
 site = BiliLive()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/bilibili/vc.py` & `ykdl-1.8.2/ykdl/extractors/bilibili/vc.py`

 * *Files 14% similar despite different names*

```diff
@@ -3,28 +3,29 @@
 from .._common import *
 
 
 class BiliVC(Extractor):
     name = '哔哩哔哩 小视频 (Bili VC)'
 
     def prepare(self):
-        info = MediaInfo(self.name)
+        return match1(self.url, 'video/(\d+)')
 
-        self.vid = match1(self.url, 'video/(\d+)')
+    def prepare(self):
+        info = MediaInfo(self.name)
 
         video_data = get_response(
                 'https://api.vc.bilibili.com/clip/v1/video/detail',
-                params={'video_id': self.vid}).json()
+                params={'video_id': self.mid}).json()
 
         info.title = video_data['data']['item']['description']
         info.artist = video_data['data']['user']['name']
 
         info.streams['current'] = {
             'container': 'mp4',
-            'video_profile': 'current',
+            'profile': 'current',
             'src' : [video_data['data']['item']['video_playurl']],
             'size': int(video_data['data']['item']['video_size'])
         }
 
         return info
 
 site = BiliVC()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/bilibili/video.py` & `ykdl-1.8.2/ykdl/extractors/bilibili/video.py`

 * *Files 19% similar despite different names*

```diff
@@ -8,61 +8,64 @@
 APPKEY = 'iVGUTjsxvpLeuDCf'
 SECRETKEY = 'aHRmhWMLkdeMuILqORnYZocwMBpMEOdt'
 api_url = 'https://interface.bilibili.com/v2/playurl'
 
 class BiliVideo(BiliBase):
     name = '哔哩哔哩 (Bilibili)'
 
-    def get_page_info(self):
+    def get_page_info(self, info):
         page_index = match1(self.url, '\?p=(\d+)', 'index_(\d+)\.') or '1'
         html = get_content(self.url)
-        date = json.loads(match1(html, '__INITIAL_STATE__=({.+?});'))['videoData']
-        title = date['title']
-        artist = date['owner']['name']
-        pages = date['pages']
+        data = match1(html, '__INITIAL_STATE__=({.+?});')
+        self.logger.debug('data:\n%s', data)
+        data = json.loads(data)['videoData']
+        title = data['title']
+        pages = data['pages']
         for page in pages:
-           index = str(page['page'])
-           subtitle = page['part']
-           if index == page_index:
-               vid = page['cid']
-               if len(pages) > 1:
-                   title = '{title} - {index} - {subtitle}'.format(**vars())
-               elif subtitle and subtitle != title:
-                   title = '{title} - {subtitle}'.format(**vars())
-               break
-
-        return vid, title, artist
+            index = str(page['page'])
+            subtitle = page['part']
+            if index == page_index:
+                self.mid = page['cid']
+                if len(pages) > 1:
+                    title = '{title} - {index} - {subtitle}'.format(**vars())
+                elif subtitle and subtitle != title:
+                    title = '{title} - {subtitle}'.format(**vars())
+                info.duration = page['duration']
+                break
+        info.title = title
+        info.artist = data['owner']['name']
+        info.add_comment(data['tname'])
 
     def get_api_url(self, qn):
-        params_str = urlencode([
-            ('appkey', APPKEY),
-            ('cid', self.vid),
-            ('platform', 'html5'),
-            ('player', 0),
-            ('qn', qn)
-        ])
-        return sign_api_url(api_url, params_str, SECRETKEY)
+        params = {
+            'appkey': APPKEY,
+            'cid': self.mid,
+            'platform': 'html5',
+            'player': 0,
+            'qn': qn
+        }
+        return sign_api_url(api_url, params, SECRETKEY)
 
     def prepare_list(self):
         vid = match1(self.url, '/(av\d+|(?:BV|bv)[0-9A-Za-z]{10})')
         if vid[:2] == 'av':
             vid = av2bv(vid)
         data = get_media_data(vid)
 
         if 'ugc_season' in data:
-            bvids = [section['bvid'] for section in
-                     data['ugc_season']['sections'][0]['episodes']]
-            if self.start < 0:
-                self.start = bvids.index(vid)
+            bvids = [episode['bvid'] for episode in
+                        sum((section['episodes'] for section in
+                            data['ugc_season']['sections']), [])]
+            self.set_index(vid, bvids)
             for bvid in bvids:
-                yield 'https://www.bilibili.com/video/{bvid}'.format(**vars())
+                yield 'https://www.bilibili.com/video/{bvid}/'.format(**vars())
 
         else:
-            if self.start < 0:
-                page = int(match1(self.url, '[^a-z]p(?:age)?=(\d+)',
-                                            'index_(\d+)\.')
-                           or '1')
-                self.start = page - 1
-            for p in range(1, data['videos'] + 1):
-                yield 'https://www.bilibili.com/video/{vid}?p={p}'.format(**vars())
+            page = int(match1(self.url, '[^a-z]p(?:age)?=(\d+)',
+                                        'index_(\d+)\.')
+                       or '1')
+            self.set_index(page, data['videos'])
+            for p in range(data['videos']):
+                p = p + 1
+                yield 'https://www.bilibili.com/video/{vid}/?p={p}'.format(**vars())
 
 site = BiliVideo()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/cctv.py` & `ykdl-1.8.2/ykdl/extractors/cctv.py`

 * *Files 10% similar despite different names*

```diff
@@ -10,44 +10,46 @@
         ['chapters6',   'BD', '超高清 1080P'],
         ['chapters5',   'TD', '超高清 720P'],
         ['chapters4',   'TD', '超清'],
         ['chapters3',   'HD', '高清'],
         ['chapters2',   'SD', '标清'],
         ['lowChapters', 'LD', '流畅']]
 
+    def prepare_mid(self):
+        mid = match1(self.url, '(?:guid|videoCenterId)=(\w+)',
+                               '(\w+)/index\.shtml')
+        if mid is None:
+            html = get_content(self.url)
+            mid = match1(html, 'guid\s*=\s*[\'"]([^\'"]+)',
+                               '"videoCenterId","([^"]+)',
+                               'initMyAray\s*=\s*[\'"]([^\'"]+)')
+        return mid
+
     def prepare(self):
         info = MediaInfo(self.name)
-        self.vid = match1(self.url, '(?:guid|videoCenterId)=(\w+)',
-                                    '(\w+)/index\.shtml')
-        if self.url and not self.vid:
-            content = get_content(self.url)
-            self.vid = match1(content, 'guid\s*=\s*[\'"]([^\'"]+)',
-                                       '"videoCenterId","([^"]+)',
-                                       'initMyAray\s*=\s*[\'"]([^\'"]+)')
-        assert self.vid, 'cant find vid'
-
-        data = get_response('http://vdn.apps.cntv.cn/api/getHttpVideoInfo.do',
-                            params={
-                                'pid': self.vid,
-                                'tsp': int(time.time()),
-                                'vn': 2054,
-                                'pcv': 152438790
-                            }).json()
+
+        data = get_response(
+            'http://vdn.apps.cntv.cn/api/getHttpVideoInfo.do',
+            params={
+                'pid': self.mid,
+                'tsp': int(time.time()),
+                'vn' : 2054,
+                'pcv': 152438790
+            }).json()
 
         info.title = '{} - {}'.format(data['title'], data['play_channel'])
 
         video_data = data['video']
-        for chapters, stream_type, profile in self.supported_chapters:
+        for chapters, stream_id, stream_profile in self.supported_chapters:
             stream_data = video_data.get(chapters)
             if stream_data:
                 urls = []
                 for v in stream_data:
                    urls.append(v['url'])
-                info.streams[stream_type] = {
+                info.streams[stream_id] = {
                     'container': 'mp4',
-                    'video_profile': profile,
-                    'src': urls, 
-                    'size' : 0
+                    'profile': stream_profile,
+                    'src': urls
                 }
         return info
 
 site = CNTV()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/douban/movie.py` & `ykdl-1.8.2/ykdl/extractors/douban/movie.py`

 * *Files 3% similar despite different names*

```diff
@@ -11,16 +11,16 @@
         html = get_content(self.url)
         info.title = match1(html, '<meta name="description" content='
                                   '"(.+?) 在线观看"/>')
         url = match1(html,'"embedUrl": "(.+?)"')
 
         info.streams['current'] = {
             'container': 'mp4',
-            'video_profile': 'current',
-            'src' : [url]
+            'profile': 'current',
+            'src': [url]
         }
         return info
 
     def list_only(self):
         return '/subject/' in self.url
 
     def prepare_list(self):
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/douban/music.py` & `ykdl-1.8.2/ykdl/extractors/douban/music.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,64 +1,58 @@
 # -*- coding: utf-8 -*-
 
 from .._common import *
 
 
 def get_info_list(sids):
+    if not sids: return
+
     data = get_response('https://music.douban.com/j/artist/playlist',
                         data={
                             'source' : '',
                             'sids' : sids,
                             'ck' : ''
                         }).json()
 
-    info = None
     for song in data['songs']:
         info = MediaInfo(site.name)
         artist = song['artist']
         info.title = song['title']
         info.artist = artist['name']
         info.duration = song['play_length']
         info.add_comment(song['label'])
         info.add_comment(artist['style'])
         info.extra.referer = artist['url']
         info.streams['current'] = {
             'container': 'mp3',
-            'video_profile': 'current',
+            'profile': 'current',
             'src' : [song['url']],
         }
         yield info
 
-    assert info, "can't find songs of %r, may has been removed!" % sids
-
 class DoubanMusic(Extractor):
     name = 'Douban Music (豆瓣音乐)'
 
-    def prepare(self):
-        if not self.vid:
-            self.vid = match1(self.url, 's(?:id)?=(\d+)')
-        assert self.vid, 'No sid has been found!'
+    def prepare_mid(self):
+        return match1(self.url, 's(?:id)?=(\d+)')
 
-        for info in get_info_list(self.vid):
-            return info
+    def prepare(self):
+        return next(get_info_list(self.mid))
 
     def list_only(self):
         return 'site.douban' in self.url and not match(self.url, 's=\d+') or \
                 match(self.url, 'sid=\d+,\d')
 
     def prepare_list(self):
-
         if 'site.douban' in self.url:
             sids = matchall(get_content(self.url), 'sid="(\d+)"')
         else:
             sids = matchall(match1(self.url, 'sid=([\d,]+)') or '', '(\d+)')
-        assert sids, 'No sid has been found!'
 
         sids, osids = [], sids
         for sid in osids:
             if sid not in sids:
                 sids.append(sid)
-        sids = ','.join(sids)
-        return get_info_list(sids)
-
+        self.set_index(None, sids)
+        return get_info_list(','.join(sids))
 
 site = DoubanMusic()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/douyin/live.py` & `ykdl-1.8.2/ykdl/extractors/douyin/live.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,61 +1,81 @@
 # -*- coding: utf-8 -*-
 
 from .._common import *
 from .. import _byted
 
 
-class TikTok(Extractor):
-    name = '抖音直播 (TikTok)'
+class Douyin(Extractor):
+    name = '抖音直播 (Douyin)'
 
     quality_2_profile_id = {
-          'ORIGIN': ['原画', 'OG'],
+         'ORIGION': ['原画', 'OG'],
         'FULL_HD1': ['蓝光', 'BD'],
              'HD1': ['超清', 'TD'],
              'SD1': ['高清', 'HD'],
              'SD2': ['标清', 'SD']
      }
 
     def prepare(self):
-        info = MediaInfo(self.name)
+        info = MediaInfo(self.name, True)
+
+        if 'amemv.com' in self.url:
+            data = get_response('https://webcast.amemv.com/webcast/room/reflow/info/',
+                                params={
+                                    'verifyFp': '',
+                                     'type_id': 0,
+                                     'live_id': 1,
+                                 'sec_user_id': '',
+                                      'app_id': 1128,
+                                     'msToken': '',
+                                     'X-Bogus': '',  # 1
+                                     'room_id': match1(self.url, '/reflow/(\d+)')
+                                }).json()
+            video_info = data['data'].get('room')
+        else:
+            html = _byted.get_content(self.url)
+            data = match1(html,
+                         'id="RENDER_DATA" type="application/json">(.+?)</script>',
+                         '__INIT_PROPS__ = (.+?)</script>')
+            data = json.loads(unquote(data))
+            self.logger.debug('data: \n%s', data)
+
+            try:
+                video_info = data['app']['initialState']['roomStore']['roomInfo'].get('room')
+            except KeyError:
+                video_info = data['/webcast/reflow/:id'].get('room')
 
-        html = _byted.get_content(self.url)
-        data = match1(html,
-                     'id="RENDER_DATA" type="application/json">(.+?)</script>',
-                     '__INIT_PROPS__ = (.+?)</script>')
-        data = json.loads(unquote(data))
-        self.logger.debug('data: \n%s', data)
-
-        try:
-            video_info = data['initialState']['roomStore']['roomInfo'].get('room')
-        except KeyError:
-            video_info = data['/webcast/reflow/:id'].get('room')
         assert video_info and video_info['status'] == 2, 'live is off!!!'
 
         title = video_info['title']
         info.artist = nickName = video_info['owner']['nickname']
         info.title = '{title} - {nickName}'.format(**vars())
 
         stream_info = video_info['stream_url']
         stream_urls = []
         if 'flv_pull_url' in stream_info:
             for ql, url in stream_info['flv_pull_url'].items():
                 stream_urls.append(['flv', ql, url])
-            stream_urls.append(['flv', 'ORIGIN', stream_info.get('rtmp_pull_url')])
+            orig = stream_info.get('rtmp_pull_url')
+            if orig and orig not in stream_info['flv_pull_url'].values():
+                stream_urls.append(['flv', 'ORIGION', orig])
         if 'hls_pull_url_map' in stream_info:
             for ql, url in stream_info['hls_pull_url_map'].items():
                 stream_urls.append(['m3u8', ql, url])
-            stream_urls.append(['m3u8', 'ORIGIN', stream_info.get('hls_pull_url')])
+            orig = stream_info.get('hls_pull_url')
+            if orig and orig not in stream_info['hls_pull_url_map'].values():
+                stream_urls.append(['m3u8', 'ORIGION', orig])
 
         for ext, ql, url in stream_urls:
             if not url:
                 continue
-            video_profile, stream = self.quality_2_profile_id[ql]
-            info.streams[stream + '-' + ext[:3]] = {
+            stream_profile, stream_id = self.quality_2_profile_id[ql]
+            info.streams[stream_id + '-' + ext[:3]] = {
                 'container': ext,
-                'video_profile': video_profile,
+                'profile': stream_profile,
                 'src' : [url],
+                'size': Infinity
             }
 
         return info
 
-site = TikTok()
+site = Douyin()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/douyu/crypto-js-md5.min.js` & `ykdl-1.8.2/ykdl/extractors/douyu/crypto-js-md5.min.js`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/douyu/live.py` & `ykdl-1.8.2/ykdl/extractors/douyu/live.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,103 +1,105 @@
 # -*- coding: utf-8 -*-
 
 from .._common import *
 from .util import get_h5enc, ub98484234
 
 
-douyu_match_pattern = [
-    'class="hroom_id" value="([^"]+)',
-    'data-room_id="([^"]+)'
-]
-
 class Douyutv(Extractor):
     name = '斗鱼直播 (DouyuTV)'
 
     profile_2_id = {
         '原画':    'OG',
         '蓝光10M': 'BD10M',
         '蓝光8M':  'BD8M',
         '蓝光4M':  'BD4M',
         '蓝光':    'BD',
         '超清':    'TD',
         '高清':    'HD',
         '流畅':    'SD'
      }
 
+    def prepare_mid(self):
+        html = get_content(self.url)
+        mid = match1(html, '\$ROOM\.room_id\s*=\s*(\d+)',
+                           'room_id\s*=\s*(\d+)',
+                           '"room_id.?":(\d+)',
+                           'data-onlineid=(\d+)',
+                           '(房间已被关闭)')
+        assert mid != '房间已被关闭', '房间已被关闭'
+        return mid
+
     def prepare(self):
         info = MediaInfo(self.name, True)
-        add_header('Referer', 'https://www.douyu.com')
 
+        add_header('Referer', 'https://www.douyu.com')
         html = get_content(self.url)
-        self.vid = match1(html, '\$ROOM\.room_id\s*=\s*(\d+)',
-                                'room_id\s*=\s*(\d+)',
-                                '"room_id.?":(\d+)',
-                                'data-onlineid=(\d+)',
-                                '(房间已被关闭)')
 
-        assert self.vid != '房间已被关闭', '房间已被关闭'
         title = match1(html, 'Title-head\w*">([^<]+)<')
         artist = match1(html, 'Title-anchorName\w*" title="([^"]+)"')
         if not title or not artist:
             room_data = get_response(
-                    'https://open.douyucdn.cn/api/RoomApi/room/' + self.vid
+                    'https://open.douyucdn.cn/api/RoomApi/room/' + self.mid
                     ).json()
             if room_data['error'] == 0:
                 room_data = room_data['data']
                 title = room_data['room_name']
                 artist = room_data['owner_name']
 
         info.title = '{title} - {artist}'.format(**vars())
         info.artist = artist
 
-        js_enc = get_h5enc(html, self.vid)
+        js_enc = get_h5enc(html, self.mid)
         params = {
             'cdn': '',
             'iar': 0,
             'ive': 0,
         }
-        ub98484234(js_enc, self, params)
+        ub98484234(js_enc, self.mid, self.logger, params)
 
         def get_live_info(rate=0):
             params['rate'] = rate
             live_data = get_response(
-                        'https://www.douyu.com/lapi/live/getH5Play/' + self.vid,
+                        'https://www.douyu.com/lapi/live/getH5Play/' + self.mid,
                         data=params).json()
             if live_data['error']:
                 return live_data['msg']
 
             live_data = live_data['data']
             real_url = '/'.join([live_data['rtmp_url'], live_data['rtmp_live']])
             rate_2_profile = {rate['rate']: rate['name']
                               for rate in live_data['multirates']}
-            video_profile = rate_2_profile[live_data['rate']]
-            if '原画' in video_profile:
-                stream = 'OG'
+            stream_profile = rate_2_profile[live_data['rate']]
+            if '原画' in stream_profile:
+                stream_id = 'OG'
             else:
-                stream = self.profile_2_id[video_profile]
-            info.streams[stream] = {
+                stream_id = self.profile_2_id[stream_profile]
+            info.streams[stream_id] = {
                 'container': match1(live_data['rtmp_live'], '\.(\w+)\?'),
-                'video_profile': video_profile,
+                'profile': stream_profile,
                 'src' : [real_url],
-                'size': float('inf')
+                'size': Infinity
             }
 
             error_msges = []
             if rate == 0:
                 rate_2_profile.pop(0, None)
                 rate_2_profile.pop(live_data['rate'], None)
                 for rate in rate_2_profile:
                     error_msg = get_live_info(rate)
                     if error_msg:
                         error_msges.append(error_msg)
             if error_msges:
                 return ', '.join(error_msges)
 
         error_msg = get_live_info()
-        assert info.streams, error_msg
+        if error_msg:
+            self.logger.debug('error_msg:\n\t' + error_msg)
+
         return info
 
     def prepare_list(self):
         html = get_content(self.url)
-        return matchall(html, *douyu_match_pattern)
+        return matchall(html, 'class="hroom_id" value="([^"]+)',
+                              'data-room_id="([^"]+)')
 
 site = Douyutv()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/douyu/util.py` & `ykdl-1.8.2/ykdl/extractors/douyu/util.py`

 * *Files 6% similar despite different names*

```diff
@@ -5,24 +5,24 @@
 assert JSEngine, "No JS Interpreter found, can't extract douyu live/video!"
 
 
 # REF: https://cdnjs.com/libraries/crypto-js
 js_md5 = get_pkgdata_str(__name__, 'crypto-js-md5.min.js',
         'https://cdnjs.cloudflare.com/ajax/libs/crypto-js/3.1.9-1/crypto-js.min.js')
 
-def get_h5enc(html, vid):
+def get_h5enc(html, rid):
     js_enc = match1(html, '(var vdwdae325w_64we =[\s\S]+?)\s*</script>')
     if js_enc is None or 'ub98484234(' not in js_enc:
         data = get_response('https://www.douyu.com/swf_api/homeH5Enc',
-                            params={'rids': vid}).json()
+                            params={'rids': rid}).json()
         assert data['error'] == 0, data['msg']
-        js_enc = data['data']['room' + vid]
+        js_enc = data['data']['room' + rid]
     return js_enc
 
-def ub98484234(js_enc, extractor, params):
+def ub98484234(js_enc, rid, logger, params):
     names_dict = {
         'debugMessages': get_random_name(8),
         'decryptedCodes': get_random_name(8),
         'patchCode': get_random_name(8),
         'resoult': get_random_name(8),
         '_ub98484234': get_random_name(8),
         'workflow': match1(js_enc, 'function ub98484234\(.+?\Weval\((\w+)\);'),
@@ -73,20 +73,20 @@
         js_ctx.append(js_enc.replace('eval({workflow});'.format(**names_dict), js_patch[1]))
     else:
         js_ctx.append(js_enc)
     js_ctx.append(js_debug)
 
     did = get_random_uuid_hex()
     tt = str(int(time.time()))
-    ub98484234 = js_ctx.call('ub98484234', extractor.vid, did, tt)
+    ub98484234 = js_ctx.call('ub98484234', rid, did, tt)
     ub98484234 = {
         'decryptedCodes': ub98484234[names_dict['decryptedCodes']],
         'resoult': ub98484234[names_dict['resoult']]
     }
-    extractor.logger.debug('ub98484234: %s', ub98484234)
+    logger.debug('ub98484234: %s', ub98484234)
     ub98484234 = ub98484234['resoult']
     params.update({
         'v': match1(ub98484234, 'v=(\d+)'),
         'did': did,
         'tt': tt,
         'sign': match1(ub98484234, 'sign=(\w{32})')
     })
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/fun.py` & `ykdl-1.8.2/ykdl/extractors/fun.py`

 * *Files 1% similar despite different names*

```diff
@@ -133,15 +133,15 @@
                                 'ctime': ct,
                                 'app_code': 'web'
                             }).json()
         assert data['retcode'] == '200', data['retmsg']
 
         fetch_mozecname(vid)
         for vinfos in data['playlist']:
-            stream = self.quality_2_id[vinfos['code']]
+            stream_id = self.quality_2_id[vinfos['code']]
             for vinfo in vinfos['playinfo']:
                 if vinfo.get('isvip') == '1':
                     continue
                 if vinfo['codec'] == 'h.264':
                     codec = '-h264'
                 elif vinfo['codec'] == 'h.265':
                     codec = '-h265'
@@ -153,17 +153,17 @@
                 url = (
                     'https://jobsfe.funshion.com/play/v1/mp4/{}.mp4?'.
                     format(vinfo['infohash']) +
                     urlencode({
                         'token': vinfo['token'],
                         'vf': vinfo['vf']
                     }))
-                info.streams[stream + codec] = {
+                info.streams[stream_id + codec] = {
                     'container': 'mp4',
-                    'video_profile': vinfos['name'],
+                    'profile': vinfos['name'],
                     'src' : [url],
                     'size': int(vinfo['filesize'])
                 }
 
         return info
 
 site = Funshion()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/generalembed.py` & `ykdl-1.8.2/ykdl/extractors/generalembed.py`

 * *Files 23% similar despite different names*

```diff
@@ -2,185 +2,158 @@
 
 from ._common import *
 
 
 '''
 refer to http://open.youku.com/tools
 '''
-youku_embed_patterns = [ 'youku\.com/v_show/id_([a-zA-Z0-9=]+)',
-                         'player\.youku\.com/player\.php/sid/([a-zA-Z0-9=]+)/v\.swf',
-                         'loader\.swf\?VideoIDS=([a-zA-Z0-9=]+)',
-                         'player\.youku\.com/embed/([a-zA-Z0-9=]+)',
-                         'YKU.Player\(\'[a-zA-Z0-9]+\',{ client_id: \'[a-zA-Z0-9]+\', vid: \'([a-zA-Z0-9]+)\'',
-                         'data-youku=\"[a-zA-Z0-9,:]+vid:([a-zA-Z0-9=]+)\"'
-                       ]
+youku_embed_patterns = [
+    'youku\.com/v_show/id_([a-zA-Z0-9=]+)',
+    'player\.youku\.com/player\.php/sid/([a-zA-Z0-9=]+)/v\.swf',
+    'loader\.swf\?VideoIDS=([a-zA-Z0-9=]+)',
+    'player\.youku\.com/embed/([a-zA-Z0-9=]+)',
+    'YKU.Player\(\'[a-zA-Z0-9]+\',{ client_id: \'[a-zA-Z0-9]+\', vid: \'([a-zA-Z0-9]+)\'',
+    'data-youku=\"[a-zA-Z0-9,:]+vid:([a-zA-Z0-9=]+)\"'
+]
 
 '''
 v.qq.com
 '''
-qq_embed_patterns = [ 'v\.qq\.com[a-zA-Z0-9\/\?\.\;]+vid=([a-zA-Z0-9]+)',
-                      'TPout\.swf[a-zA-Z0-9=\?\&_]+vid=([a-zA-Z0-9]+)'
-                    ]
+qq_embed_patterns = [
+    'v\.qq\.com[a-zA-Z0-9\/\?\.\;]+vid=([a-zA-Z0-9]+)',
+    'TPout\.swf[a-zA-Z0-9=\?\&_]+vid=([a-zA-Z0-9]+)'
+]
 
 
 '''
 tv.sohu.com
 '''
-sohu_embed_patterns = [ 'tv\.sohu\.com[a-zA-Z0-9\/\?=]+\&vid=([a-zA-Z0-9]+)\&',
-                        'share\.vrs\.sohu\.com\/my\/v.swf[&+=a-zA-z0-9]+&id=(\d+)',
-                        'my\.tv\.sohu\.com\/[a-zA-Z0-9\/]+/(\d+)'
-                      ]
+sohu_embed_patterns = [
+    'tv\.sohu\.com[a-zA-Z0-9\/\?=]+\&vid=([a-zA-Z0-9]+)\&',
+    'share\.vrs\.sohu\.com\/my\/v.swf[&+=a-zA-z0-9]+&id=(\d+)',
+    'my\.tv\.sohu\.com\/[a-zA-Z0-9\/]+/(\d+)'
+]
 
 '''
 Ku6
 '''
-ku6_embed_url = [ '(http://v.ku6vms.com/[^\"]+)'
-                     ]
-
-ku6_embed_patterns = [ 'http://player.ku6.com/refer/(.*)/v.swf'
-                     ]
+ku6_embed_url = [
+    '(http://v.ku6vms.com/[^\"]+)'
+]
+
+ku6_embed_patterns = [
+    'http://player.ku6.com/refer/(.*)/v.swf'
+]
 '''
 163
 '''
-netease_embed_patterns = [ 'v\.163\.com\/[0-9a-zA-Z\/\?\.]+topicid=([^&]+)&amp\;vid=([^&]+)',
-                           'topicid=([a-zA-Z0-9]+)&amp;vid=([a-zA-Z0-9]+)&amp'
-                     ]
+netease_embed_patterns = [
+    'v\.163\.com\/[0-9a-zA-Z\/\?\.]+topicid=([^&]+)&amp\;vid=([^&]+)',
+    'topicid=([a-zA-Z0-9]+)&amp;vid=([a-zA-Z0-9]+)&amp'
+]
 
 '''
 iqiyi
 '''
-iqiyi_embed_patterns = [ 'definitionID=([^&]+)&tvId=([^&]+)'
-                     ]
+iqiyi_embed_patterns = [
+    'definitionID=([^&]+)&tvId=([^&]+)'
+]
 
 '''
 Letv Cloud
 '''
-lecloud_embed_patterns = [ '{"uu":"([^\"]+)","vu":"([^\"]+)"',
-                           'bcloud.swf\?uu=([^&]+)&amp;vu=([^&]+)',
-                           'uu=([^&]+)&amp;vu=([^&]+)'
-                     ]
+lecloud_embed_patterns = [
+    '{"uu":"([^\"]+)","vu":"([^\"]+)"',
+    'bcloud.swf\?uu=([^&]+)&amp;vu=([^&]+)',
+    'uu=([^&]+)&amp;vu=([^&]+)'
+]
 
 '''
 ifeng
 '''
-ifeng_embed_patterns = [ 'v\.ifeng\.com\/[a-zA-Z\=\/\?\&\.]+guid=([^\"]+)'
-                     ]
+ifeng_embed_patterns = [
+    'v\.ifeng\.com\/[a-zA-Z\=\/\?\&\.]+guid=([^\"&]+)'
+]
 
 '''
 weibo
 '''
-weibo_embed_patterns = [ 'http://video.weibo.com/player/1034:(\w{32})\w*'
-                     ]
+weibo_embed_patterns = [
+    'http://video.weibo.com/player/1034:(\w{32})\w*'
+]
 
 '''
 Sina
 '''
-sina_embed_patterns = [ 'http://video.sina.com.cn/share/video/(\d+).swf'
-                     ]
-
-'''
-Dilidili
-'''
-dilidili_embed_patterns = [ 'vid=([^&]+)&v=([^&]+)&'
-                     ]
+sina_embed_patterns = [
+    'http://video.sina.com.cn/share/video/(\d+).swf'
+]
 
 '''
 Bilibili
 '''
-bilibili_embed_patterns = [ 'flashvars="aid=(\d+)'
-                     ]
+bilibili_embed_patterns = [
+    'flashvars="aid=(\d+)'
+]
 
 class GeneralEmbed(EmbedExtractor):
     name = 'GeneralEmbed (通用嵌入视频)'
 
     def prepare_playlist(self):
 
-        def append_media_info(site, vid):
-            media_info = self.new_media_info()
-            media_info['site'] = site
-            media_info['vid'] = vid
-            self.media_info_list.append(media_info)
-
-        content = get_content(self.url)
-
-        vids = matchall(content, *youku_embed_patterns)
-        for vid in vids:
-            append_media_info('youku',vid)
-
-        vids = matchall(content, *qq_embed_patterns)
-        for vid in vids:
-            append_media_info('qq.video',vid)
-
-        vids = matchall(content, *sohu_embed_patterns)
-        for vid in vids:
-            append_media_info('sohu.my',vid)
-
-        urls = matchall(content, *ku6_embed_url)
-        for url in urls:
-            html = get_content(url)
-            flashvars = matchall(html, 'vid=([^&]+)', 'style=([^&]+)', 'sn=([^&]+)')
+        def append_media_info(site, mid):
+            media_info = self.new_media_info({
+                'site': site,
+                'mid': mid
+            })
+            if media_info not in self.media_info_list:
+                self.media_info_list.append(media_info)
+
+        html = get_content(self.url)
+
+        for mid in matchall(html, *youku_embed_patterns):
+            append_media_info('youku', mid)
+
+        for mid in matchall(html, *qq_embed_patterns):
+            append_media_info('qq.video', mid)
+
+        for mid in matchall(html, *sohu_embed_patterns):
+            append_media_info('sohu.my', mid)
+
+        for url in matchall(html, *ku6_embed_url):
+            flashvars = matchall(get_content(url),'vid=([^&]+)',
+                                                  'style=([^&]+)',
+                                                  'sn=([^&]+)')
             data = get_response(
                     'http://v.ku6vms.com/phpvms/player/forplayer/vid/'
                     '{}/style/{}/sn/{}'
-                    .format(flashvars[0], flashvars[1],flashvars[2])).json()
-            vid = data['ku6vid']
-            append_media_info('ku6',vid)
-
-        vids = matchall(content, *ku6_embed_patterns)
-        for v in vids:
-            append_media_info('ku6', v)
-
-        vids = matchall(content, *netease_embed_patterns)
-        for v in vids:
-            append_media_info('netease.video', v)
-
-        vids = matchall(content, *iqiyi_embed_patterns)
-        for v in vids:
-            videoid, tvid = v
-            append_media_info('iqiyi', (tvid, videoid))
-
-        vids = matchall(content, *lecloud_embed_patterns)
-        for v in vids:
-            uu, vu = v
-            append_media_info('le.letvcloud', (vu, uu))
-
-        vids = matchall(content, *ifeng_embed_patterns)
-        for v in vids:
-            v  = v.split('&')[0]
-            append_media_info('ifeng.news', v)
-
-        vids = matchall(content, *weibo_embed_patterns)
-        for v in vids:
-            append_media_info('weibo', 'http://weibo.com/p/' + v)
-
-        vids = matchall(content, *sina_embed_patterns)
-        for v in vids:
-            v  = v.split('&')[0]
-            append_media_info('sina.video', v)
-
-        vids = matchall(content, *bilibili_embed_patterns)
-        for v in vids:
-            v = 'https://www.bilibili.com/video/av{}'.format(v)
-            append_media_info('bilibili.video', v)
-
-
-        vids = matchall(content, *dilidili_embed_patterns)
-        for v in vids:
-            v,site  = v
-            if site == 'bilibili':
-                site = 'bilibili.video'
-            elif site == 'qq':
-                site = 'qq.video'
-            elif site =='yun':
-                site = 'le.letvcloud'
-                v = v.split(':')
-            append_media_info(site, v)
-
-        tmp = []
-        for v in self.media_info_list:
-            if not v in tmp:
-                tmp.append(v)
-        self.media_info_list = tmp
+                    .format(*flashvars)).json()
+            mid = data['ku6vid']
+            append_media_info('ku6', mid)
+
+        for mid in matchall(html, *ku6_embed_patterns):
+            append_media_info('ku6', mid)
+
+        for mid in matchall(html, *netease_embed_patterns):
+            append_media_info('netease.video', mid)
+
+        for mid in matchall(html, *iqiyi_embed_patterns):
+            append_media_info('iqiyi', mid)
+
+        for mid in matchall(html, *lecloud_embed_patterns):
+            append_media_info('le.letvcloud', mid)
+
+        for mid in matchall(html, *ifeng_embed_patterns):
+            append_media_info('ifeng.news', mid)
+
+        for mid in matchall(html, *weibo_embed_patterns):
+            append_media_info('weibo', 'http://weibo.com/p/' + mid)
+
+        for mid in matchall(html, *sina_embed_patterns):
+            append_media_info('sina.video', mid)
+
+        for mid in matchall(html, *bilibili_embed_patterns):
+            append_media_info('bilibili.video', mid)
 
     parser = EmbedExtractor.parser_list
 
 site = GeneralEmbed()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/generalsimple.py` & `ykdl-1.8.2/ykdl/extractors/generalsimple.py`

 * *Files 6% similar despite different names*

```diff
@@ -12,24 +12,24 @@
     (?:https?:|\\?/)[^"'#]+?\.
     (
         m3u8?                       | # HLS
         mpd                         | # DASH
         mp4|webm                    | # video/audio
         f4v|flv|ts                  | # video
         mov|qt|m4[pv]|og[mv]        | # video
-        ogg|3gp|mpe?g               | # video/audio
+        ogg|vid|3gp|mpe?g           | # video/audio
         mp3|flac|wave?|oga|aac|weba   # audio
     )
-    /?(?:\?.+?)?
+    /?(?:[\?&].+?)?
 )["'#]
 '''
 pattern_src = r'''(?ix)
 <(?:video|audio|source)[^>]+?
-src=["']((?:https?:|\\?/)[^"']+)["']
-[^>]+?
+src=["']?((?:https?:|\\?/)[^"' ]+)["' ]
+[^>]*?
 (?:
     type=["']((?:video|audio|application)/[^"']+)["']
     |
     [^>](?!type)*>
 )
 '''
 
@@ -40,14 +40,20 @@
         info = MediaInfo(self.name)
 
         html = get_content(self.url)
 
         info.title = match1(html, '<meta property="og:title" content="([^"]+)',
                                   '<title>(.+?)</title>')
 
+        streams = get_kt_playlist(html)
+        if streams:
+            info.streams = streams
+            info.extra.referer = self.url
+            return info
+
         ext = ctype = None
         for i in range(2):
             url, ctype = matchm(html, pattern_src)
             if url is None:
                 url, ext = matchm(html, pattern_ext)
             if url:
                 if not i:
@@ -59,24 +65,26 @@
         if url:
             url = literalize(url, True)
             url = match1(url, '.+(https?://.+)') or url  # redirect clear
             if url[:2] == '//':
                 url = self.url[:self.url.find('/')] + url
             elif url[0] == '/':
                 url = self.url[:self.url.find('/', 9)] + url
+            if '?' not in url and '&' in url:
+                url = url.replace('&', '?', 1)
             if ext is None or ctype:
                 ctype = str(ctype).lower()
                 ext = contentTypes.get(ctype) or url_info(url)[1] or (
                             ctype.startswith('audio') and 'mp3' or 'mp4')
             if ext[:3] == 'm3u':
                 info.streams = load_m3u8_playlist(url, headers={'Referer': self.url})
             else:
                 info.streams['current'] = {
                     'container': ext,
-                    'video_profile': 'current',
+                    'profile': 'current',
                     'src': [url],
                     'size': 0
                 }
             info.extra.referer = self.url
             return info
 
 site = GeneralSimple()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/heibaizhibo.m.js` & `ykdl-1.8.2/ykdl/extractors/heibaizhibo.m.js`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/heibaizhibo.py` & `ykdl-1.8.2/ykdl/extractors/heibaizhibo.py`

 * *Files 6% similar despite different names*

```diff
@@ -64,19 +64,19 @@
                 'https://sig.heibaizhibo.com/signal-front/live/matchLiveInfo?',
                 params=params).json()
             msg = data_live['msg']
             assert '成功' in msg, msg
             data_live = data_live['data'][0]
             assert data_live['score'] >= 0, 'live video is offline!'
             url = js_ctx.call('vp', data_live['liveUrl'])
-            stream = ql['defi'].upper()
-            info.streams[stream] = {
+            stream_id = ql['defi'].upper()
+            info.streams[stream_id] = {
                 'container': 'flv',
-                'video_profile': ql['name'],
+                'profile': ql['name'],
                 'src' : [url],
-                'size': float('inf')
+                'size': Infinity
             }
             break  # seems the same quality?
 
         return info
 
 site = Heibai()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/huajiao/live.py` & `ykdl-1.8.2/ykdl/extractors/huajiao/live.py`

 * *Files 9% similar despite different names*

```diff
@@ -2,51 +2,54 @@
 
 from .._common import *
 
 
 class Huajiao(Extractor):
     name = 'huajiao (花椒直播)'
 
+    def prepare_mid(self):
+        html = get_content(self.url)
+        return match1(html, '"sn":"([^"]+)')
+
     def prepare(self):
         info = MediaInfo(self.name, True)
         html = get_content(self.url)
         t_a = match1(html, '"keywords" content="([^"]+)')
         info.title = t_a.split(',')[0]
         info.artist = t_a.split(',')[1]
 
         replay_url = match1(html, '"m3u8":\s?("[^"]+)"')
         if replay_url and len(replay_url) > 2:
             replay_url = json.loads(replay_url)
             info.live = False
             info.streams = load_m3u8_playlist(replay_url)
             return info
 
-        self.vid = match1(html, '"sn":"([^"]+)')
         channel = match1(html, '"channel":"([^"]+)')
         encoded_json = get_response('http://g2.live.360.cn/liveplay',
                                     params={
                                         'stype': 'flv',
                                         'channel': channel,
                                         'bid': 'huajiao',
-                                        'sn': self.vid,
+                                        'sn': self.mid,
                                         'sid': get_random_uuid_hex('SID'),
                                         '_rate': 'xd',
                                         'ts': time.time(),
                                         'r': random.random(),
                                         '_ostype': 'flash',
                                         '_delay': 0,
                                         '_sign': 'null',
                                         '_ver': 13
                                     }).content
-        decoded_json = base64.b64decode(encoded_json[0:3] + encoded_json[6:])
-        video_data = json.loads(decoded_json.decode())
-        live_url = video_data['main']
+        decoded_json = unb64(encoded_json[0:3] + encoded_json[6:])
+        self.logger.debug('decoded_json:\n%s', decoded_json)
+        data = json.loads(decoded_json)
         info.live = True
         info.streams['current'] = {
             'container': 'flv',
-            'video_profile': 'current',
-            'src' : [live_url],
-            'size': float('inf')
+            'profile': 'current',
+            'src' : [data['main']],
+            'size': Infinity
         }
         return info
 
 site = Huajiao()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/huya/live.py` & `ykdl-1.8.2/ykdl/extractors/huya/live.py`

 * *Files 8% similar despite different names*

```diff
@@ -18,19 +18,19 @@
             }[profile]
 
     def prepare(self):
         info = MediaInfo(self.name, True)
 
         html  = get_content(self.url)
 
-        json_stream = match1(html, '"stream": "([a-zA-Z0-9+=/]+)"')
-        assert json_stream, 'live video is offline'
-        data = json.loads(base64.b64decode(json_stream).decode())
+        data = match1(html, 'stream: ({.+)\n.*?};')
+        assert data, "can't found video!!"
         self.logger.debug('data:\n%s', data)
-        assert data['status'] == 200, data['msg']
+        data = json.loads(data)
+        assert data['vMultiStreamInfo'], 'live video is offline'
 
         room_info = data['data'][0]['gameLiveInfo']
         info.title = '{}「{} - {}」'.format(
             room_info['roomName'], room_info['nick'], room_info['introduction'])
         info.artist = room_info['nick']
         screenType = room_info['screenType']
         liveSourceType = room_info['liveSourceType']
@@ -47,50 +47,50 @@
         sUrlSuffix = stream_info['sFlvUrlSuffix']
         _url = '{sUrl}/{sStreamName}.{sUrlSuffix}?'.format(**vars())
 
         reSecret = not screenType and liveSourceType in (0, 8, 13)
         params = dict(parse_qsl(unescape(stream_info['sFlvAntiCode'])))
         if reSecret:
             params.setdefault('t', '100')  # 102
-            ct = int(params['wsTime'], 16) + random.random()
+            ct = int((int(params['wsTime'], 16) + random.random()) * 1000)
             lPresenterUid = stream_info['lPresenterUid']
-            if not sStreamName.startswith(str(lPresenterUid)):
+            if liveSourceType and not sStreamName.startswith(str(lPresenterUid)):
                 uid = lPresenterUid
             else:
-                uid = int(ct % 1e7 * 1e6 % 0xffffffff)
+                uid = int(ct % 1e10 * 1e3 % 0xffffffff)
             u1 = uid & 0xffffffff00000000
             u2 = uid & 0xffffffff
             u3 = uid & 0xffffff
             u = u1 | u2 >> 24 | u3 << 8
             params.update({
                  'u': str(u),
-                 'seqid': str(int(ct * 1000) + uid),
+                 'seqid': str(ct + uid),
                  'ver': '1',
-                 'uuid': int(ct % 1e7 * 1e6 % 0xffffffff),
+                 'uuid': int((ct % 1e10 + random.random()) * 1e3 % 0xffffffff),
              })
-            fm = base64.b64decode(params['fm']).decode().split('_', 1)[0]
+            fm = unb64(params['fm']).split('_', 1)[0]
             ss = hash.md5('|'.join([params['seqid'], params['ctype'], params['t']]))
 
         for si in data['vMultiStreamInfo']:
-            video_profile = si['sDisplayName']
-            stream = self.profile_2_id(video_profile)
+            stream_profile = si['sDisplayName']
+            stream_id = self.profile_2_id(stream_profile)
             rate = si['iBitRate']
             if rate:
                 params['ratio'] = rate
             else:
                 params.pop('ratio', None)
             if reSecret:
                 params['wsSecret'] = hash.md5('_'.join(
                             [fm, params['u'], sStreamName, ss, params['wsTime']]))
-            url = _url + urlencode(params, safe='*')
-            info.streams[stream] = {
+            url = _url + urlencode(params, safe=',*')
+            info.streams[stream_id] = {
                 'container': 'flv',
-                'video_profile': video_profile,
+                'profile': stream_profile,
                 'src': [url],
-                'size' : float('inf')
+                'size': Infinity
             }
         fake_headers.update({
             'Accept': '*/*',
             'Origin': 'https://www.huya.com',
             'Referer': 'https://www.huya.com/',
             'Sec-Fetch-Dest': 'empty',
             'Sec-Fetch-Mode': 'cors',
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/huya/video.py` & `ykdl-1.8.2/ykdl/extractors/huya/video.py`

 * *Files 15% similar despite different names*

```diff
@@ -9,49 +9,51 @@
     quality_2_id_profile = {
         'yuanhua': ['BD', '原画'],
            '1300': ['TD', '超清'],
           #'TODO': ['HD', '高清'],
             '350': ['SD', '流畅']
     }
 
+    def prepare_mid(self):
+        mid = match1(self.url, 'play/(\d+)')
+        if mid is None:
+            html = get_content(self.url)
+            mid = match1(html, 'vid = (\d+)', 'data-vid="(\d+)')
+        return mid
+
     def prepare(self):
         info = MediaInfo(self.name)
 
-        self.vid = match1(self.url, 'play/(\d+)')
         html = get_content(self.url)
-        if not self.vid:
-            self.vid = match1(html, 'vid = (\d+)', 'data-vid="(\d+)')
-        assert self.vid, "can't find VID!!"
-
         info.title = match1(html, '<h1 class="video-title">(.+?)</h1>')
         info.artist = match1(html, '<div class="video-author">[\s\S]+?<h3>(.+?)</h3>')
 
         t1 = int(time.time() * 1000)
         t2 = t1 + random.randrange(5, 10)
         rnd = str(random.random()).replace('.', '')
         data = get_response('https://v-api-player-ssl.huya.com/',
                         params={
                             'callback': 'jQuery1124{rnd}_{t1}'.format(**vars()),
                             'r': 'vhuyaplay/video',
-                            'vid': self.vid,
+                            'vid': self.mid,
                             'format': 'mp4,m3u8',
                             '_': t2
                         }).json()
         assert data['code'] == 1, data['message']
         data = data['result']['items']
 
         for stream_date in data:
             ext = stream_date['format']
             quality =stream_date['definition']
-            stream, video_profile = self.quality_2_id_profile[quality]
-            stream += '-' + ext
+            stream_id, stream_profile = self.quality_2_id_profile[quality]
+            stream_id += '-' + ext
             url = stream_date['transcode']['urls'][0]
-            info.streams[stream] = {
+            info.streams[stream_id] = {
                 'container': ext,
-                'video_profile': video_profile,
-                'src': [url],
-                'size' : int(stream_date['size'])
+                'profile': stream_profile,
+                'src' : [url],
+                'size': int(stream_date['size'])
             }
 
         return info
 
 site = HuyaVideo()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/ifeng/video.py` & `ykdl-1.8.2/ykdl/extractors/ifeng/video.py`

 * *Files 14% similar despite different names*

```diff
@@ -3,30 +3,31 @@
 from .._common import *
 
 
 class IfengVideo(Extractor):
     name = '凤凰视频 (ifeng video)'  # Expired
 
     def prepare(self):
+        return self.url[-13: -6]
+
+    def prepare(self):
         info = MediaInfo(self.name)
-        self.vid = self.url[-13: -6]
-        info.title = self.name + '-' + self.vid
+
+        info.title = self.name + '-' + self.mid
         data = get_response(
-                'http://tv.ifeng.com/html5/{self.vid}/video.json'
+                'http://tv.ifeng.com/html5/{self.mid}/video.json'
                 .format(**vars())).json()
         if 'bqSrc' in data:
             info.streams['SD'] = {
                 'container': 'mp4',
-                'video_profile': '标清',
-                'src' : [data['bqSrc']],
-                'size': 0
+                'profile': '标清',
+                'src': [data['bqSrc']]
             }
         if 'gqSrc' in data:
             info.streams['HD'] = {
                 'container': 'mp4',
-                'video_profile': '高清',
-                'src' : [data['gqSrc']],
-                'size': 0
+                'profile': '高清',
+                'src': [data['gqSrc']]
             }
         return info
 
 site = IfengVideo()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/iqilu.py` & `ykdl-1.8.2/ykdl/extractors/iqilu.py`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/iqiyi/cmd5x.js` & `ykdl-1.8.2/ykdl/extractors/iqiyi/cmd5x.js`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/iqiyi/cmd5x_iqiyi3.js` & `ykdl-1.8.2/ykdl/extractors/iqiyi/cmd5x_iqiyi3.js`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/iqiyi/live.py` & `ykdl-1.8.2/ykdl/extractors/iqiyi/live.py`

 * *Files 8% similar despite different names*

```diff
@@ -40,23 +40,25 @@
         'RESOLUTION_1080P': 'BD',
         'RESOLUTION_720P': 'TD',
         'HIGH_DEFINITION': 'HD',
         'SMOOTH': 'SD',
         #'': 'LD'
     }
 
+    def prepare_mid(self):
+        html = get_content(self.url)
+        return match1(html, '"qpId":(\d+)')
+
     def prepare(self):
         info = MediaInfo(self.name, True)
-        html = get_content(self.url)
-        self.vid = match1(html, '"qpId":(\d+)')
 
-        data = getlive(self.vid)
-        assert data['code'] == 'A00000', data.get('msg', "can't play this live video!!")
+        data = getlive(self.mid)
+        assert data['code'] == 'A00000', data.get('msg', "can't play this live video!")
         data = data['data']
-        assert data['liveType'] != 2, "can't play this live video!!"
+        assert data['liveType'] != 2, 'this live is off!'
         info.title = data['name']
 
         for stream in data['streams']:
             stream_type = stream['steamType']  # typo 'streamType' to 'steamType'
             stream_id = self.type_2_id[stream_type]
 
             if stream['formatType'] == 'HLFLV':
@@ -81,17 +83,16 @@
                 continue
             elif stream['formatType'] == 'TS':
                 url = stream['url']
                 ext = 'm3u8'
 
             stream_profile = stream['screenSize']
             info.streams[stream_id] = {
-                'video_profile': stream_profile,
                 'container': ext,
+                'profile': stream_profile,
                 'src' : [url],
-                'size': float('inf')
+                'size': Infinity
             }
 
-        assert info.streams, "can't play this live video!!"
         return info
 
 site = IqiyiLive()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/iqiyi/util.py` & `ykdl-1.8.2/ykdl/extractors/iqiyi/util.py`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/iqiyi/video.py` & `ykdl-1.8.2/ykdl/extractors/iqiyi/video.py`

 * *Files 21% similar despite different names*

```diff
@@ -8,14 +8,36 @@
 # src=1702633101b340d8917a69cf8a4b8c7c
 # salt=t6hrq6k0n6n6k6qdh6tje6wpb62v7654
 # salt=u6fnp3eok0dpftcq9qbr4n9svk8tqh7u
 
 # src=02020031010000000000
 # salt=3sj8xof48xof4tk9f4tk9ypgk9ypg5ul
 
+def get_epsodelist(tvid):
+    secret_key = 'howcuteitis'
+    params = {
+        'entity_id': tvid,
+        'timestamp': int(time.time() * 1000),
+        'src': 'pcw_tvg',
+        'vip_status': '0',
+        'vip_type': '',
+        'auth_cookie': '',
+        'device_id': get_random_id(32, 'device_id'),
+        'user_id': '',
+        'app_version': '3.0.0'
+    }
+    src = urlencode(sorted(params.items()) + [('secret_key', secret_key)])
+    params['sign'] = hash.md5(src).upper()
+    data = get_response('https://mesh.if.iqiyi.com/tvg/pcw/base_info',
+                        params=params).json()
+    return sorted(sum(data['data']['template']['pure_data']['selector_bk'][0]
+                          ['videos']['feature_paged']
+                          .values(), []),
+                  key=lambda ep: ep['album_order'])
+
 def gettmts(tvid, vid):
     tm = int(time.time() * 1000)
     key = 'd5fb4bd9d50c4be6948c97edd7254b0e'
     host = 'https://cache.m.iqiyi.com'
     params = {
         'src': '76f90cbd92f94a2e925d83e8ccd22cb7',
         'sc': md5(str(tm) + key + vid),
@@ -107,93 +129,98 @@
         'BD': '1080p',
         'TD': '720p',
         'HD': '540p',
         'SD': '360p',
         'LD': '210p'
     }
 
+    def format_mid(self, mid):
+        if isinstance(mid, (str, bytes)):
+            mid = fullmatch(mid, '[av]_[0-9a-z]+')
+            assert mid
+            self.url = 'https://www.iqiyi.com/{mid}.html'.format(**vars())
+            return None
+        assert isinstance(mid, tuple)
+        mid = mid[:2]
+        assert len(mid) == 2 and all(mid)
+        return mid
+
+    def parse_html(self):
+        html = get_content(self.url, headers={
+            'User-Agent': 'Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:60.1) Gecko/20100101 Firefox/60.1',
+        })
+        data = match1(html, "playPageInfo=({.+?});")
+        if data:
+            return json.loads(data)
+
+        url = match1(html, '(www\.iqiyi\.com/v_[0-9a-z]+\.html)')
+        if url:
+            self.url = 'https://' + url
+            return self.parse_html()
+
+    def prepare_mid(self):
+        mid = matchm(self.url, 'curid=([^_]+)_([\w]+)')
+        if all(mid):
+            return mid
+        data = self.parse_html()
+        return data and (str(data['tvId']), data['vid'])
+
     def prepare(self):
         info = MediaInfo(self.name)
 
-        if self.url and not self.vid:
-            vid = matchm(self.url, 'curid=([^_]+)_([\w]+)')
-            if vid[0]:
-                self.vid = vid
-                try:
-                    info_json = get_response(
-                            'http://pcw-api.iqiyi.com/video/video/playervideoinfo',
-                            params={'tvid': self.vid[0]}).json()
-                    info.title = info_json['data']['vn']
-                except:
-                    self.vid = None
-
-        def get_vid():
-            html = get_content(self.url)
-            video_info = match1(html, ":video-info='(.+?)'")
-
-            if video_info:
-                video_info = json.loads(video_info)
-                self.vid = str(video_info['tvId']), str(video_info['vid'])
-                info.title = video_info['name']
-
-            else:
-                tvid = match1(html,
-                              'tvId:\s*"([^"]+)',
-                              'data-video-tvId="([^"]+)',
-                              '''\['tvid'\]\s*=\s*"([^"]+)''',
-                              '"tvId":\s*([^,]+)')
-                videoid = match1(html,
-                                'data-video-vid="([^"]+)',
-                                'vid"?\'?\]?\s*(?:=|:)\s*"?\'?([^"\',]+)')
-                if not (tvid and videoid):
-                    url = match1(html, '(www\.iqiyi\.com/v_\w+\.html)')
-                    if url:
-                        self.url = 'https://' + url
-                        return get_vid()
-                self.vid = (tvid, videoid)
-                info.title = match1(html, '<title>([^<]+)').split('-')[0]
-
-        if self.url and not self.vid:
-            get_vid()
-        tvid, vid = self.vid
-        assert tvid and vid, "can't play this video!!"
+        try:
+            info_data = self.parse_html()
+            assert info_data
+        except:
+            tvid, vid = self.mid
+            info_data = get_response(
+                    'http://pcw-api.iqiyi.com/video/video/playervideoinfo',
+                    params={'tvid': tvid}).json()['data']
+            info.title = info_data['vn']
+            info.duration = info_data['plg']
+        else:
+            tvid = str(info_data['tvId'])
+            vid = info_data['vid']
+            info.title = info_data['name']
+            info.duration = info_data['duration']
+
+        if info_data['payMark']:
+            self.logger.warning('<%s> is a VIP video!', info.title)
 
         def push_stream_vd(vs):
             vd = vs['vd']
-            stream = self.vd_2_id[vd]
-            stream_profile = self.id_2_profile[stream]
+            stream_id = self.vd_2_id[vd]
+            stream_profile = self.id_2_profile[stream_id]
             fmt = vs.get('fileFormat')
             if fmt:
-                stream += '-' + fmt
+                stream_id += '-' + fmt
             m3u8 = vs['m3utx']
-            info.streams[stream] = {
-                'video_profile': stream_profile,
+            info.streams[stream_id] = {
                 'container': 'm3u8',
-                'src': [m3u8],
-                'size': 0
+                'profile': stream_profile,
+                'src': [m3u8]
             }
 
         def push_stream_bid(url_prefix, bid, container, fs_array, size):
-            stream = self.vd_2_id[bid]
+            stream_id = self.vd_2_id[bid]
             real_urls = []
             for seg_info in fs_array:
                 url = url_prefix + seg_info['l']
                 json_data = get_response(url).json()
                 down_url = json_data['l']
                 real_urls.append(down_url)
-            stream_profile = self.id_2_profile[stream]
-            info.streams[stream] = {
-                'video_profile': stream_profile,
+            stream_profile = self.id_2_profile[stream_id]
+            info.streams[stream_id] = {
                 'container': container,
-                'src': real_urls,
+                'profile': stream_profile,
+                'src' : real_urls,
                 'size': size
             }
 
         def fetch_tmts():
-            raise
             # try use tmts first
             # less http requests, get results quickly
             tmts_data = gettmts(tvid, vid)
             assert tmts_data['code'] == 'A00000'
             vs_array = tmts_data['data']['vidl']
             for vs in vs_array:
                 push_stream_vd(vs)
@@ -201,15 +228,15 @@
             if vip_conf:
                 for vds in (('5', '18'), ('10', '19')):
                     for vd in vds:
                         if vd in vip_conf:
                             tmts_data = gettmts(tvid, vip_conf[vd]['vid'])
                             if tmts_data['code'] == 'A00000':
                                 push_stream_vd(tmts_data['data'])
-                                break
+
         def fetch_vps():
             # use vps as preferred fallback
             vps_data = getvps(tvid, vid)
             assert vps_data['code'] == 'A00000'
             url_prefix = vps_data['data']['vp'].get('du')
             assert url_prefix
             vs_array = vps_data['data']['vp']['tkl'][0]['vs']
@@ -231,28 +258,41 @@
                 for stream in streams:
                     if 'fs' in stream:
                         _bid = stream['bid']
                         container = stream['ff']
                         fs_array = stream['fs']
                         size = stream['vsize']
                         push_stream_bid(url_prefix, _bid, container, fs_array, size)
-                        break
 
         for fetch in (fetch_tmts, fetch_vps, fetch_dash):
             try:
                 fetch()
                 break
             except AssertionError:
                 break
             except Exception as e:
                 self.logger.debug(e, exc_info=True)
                 continue
 
-        assert info.streams, "can't play this video!!"
         return info
 
+    def list_only(self):
+        return self.url and match(self.url, 'a_[0-9a-z]+\.html')
+
     def prepare_list(self):
         html = get_content(self.url)
 
-        return matchall(html, 'data-tvid=\"([^\"]+)\" data-vid=\"([^\"]+)\"')
+        if self.list_only():
+            data = matchall(html, "value='({.+})'/>")
+            data = json.loads(data)
+            epsodelist = data['epsodelist'] + data['updateprevuelist']
+            self.set_index(None, epsodelist)
+            for ep in epsodelist:
+                yield ep['tvId'], ep['vid']
+        else:
+            mids = [matchall(ep['play_url'], 'tvid=(\d+).+vid=(\w+)')[0]
+                    for ep in get_epsodelist(self.mid[0])]
+            self.set_index(self.mid, mids)
+            for mid in mids:
+                yield mid
 
 site = Iqiyi()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/ixigua/video.py` & `ykdl-1.8.2/ykdl/extractors/ixigua.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 # -*- coding: utf-8 -*-
 
-from .._common import *
-from .. import _byted
+from ._common import *
+from . import _byted
 
 
 class IXiGua(Extractor):
     name = '西瓜视频 (IXiGua)'
 
     @staticmethod
     def profile_2_id(profile):
@@ -49,33 +49,32 @@
             else:
                 info.title = '{al_title} - {ep_title}'.format(**vars())
 
         videoResource = video_info['videoResource']['normal']
         info.duration = videoResource['video_duration']
 
         for v in videoResource['video_list'].values():
-            video_profile = v['definition']
-            stream = self.profile_2_id(video_profile)
-            info.streams[stream] = {
+            stream_profile = v['definition']
+            stream_id = self.profile_2_id(stream_profile)
+            info.streams[stream_id] = {
                 'container': v['vtype'],
-                'video_profile': video_profile,
-                'size': v['size'],
-                'src' : [unb64(v['main_url'])],
+                'profile': stream_profile,
+                'src' : [unb64(v['backup_url_1'])],  # main_url status 403
+                'size': v['size']
             }
 
         return info
 
     def prepare_list(self):
         albumId, episodeId = matchall(self.url, '.ixigua.com/(\d+)(?:.+?id=(\d+))?')[0]
         data = get_response('https://www.ixigua.com/api/albumv2/details',
                             headers={'Referer': 'https://www.ixigua.com/'},
                             params={'albumId': albumId}).json()
         assert data['code'] == 200, "can't fetch playlist!"
 
         ep_ids = [b for a, b in sorted((ep['seq'], ep['episodeId'])
                                        for ep in data['data']['playlist'])]
-        if episodeId and self.start <= 0:
-            self.start = ep_ids.index(episodeId)
+        self.set_index(episodeId, ep_ids)
         for ep_id in ep_ids:
             yield 'https://www.ixigua.com/{albumId}?id={ep_id}'.format(**vars())
 
 site = IXiGua()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/joy.py` & `ykdl-1.8.2/ykdl/extractors/joy.py`

 * *Files 7% similar despite different names*

```diff
@@ -3,29 +3,30 @@
 from ._common import *
 
 
 class Joy(Extractor):
 
     name = '激动网 (Joy)'
 
+    def prepare_mid(self):
+        return match1(self.url, 'resourceId=([0-9]+)')
+
     def prepare(self):
         info = MediaInfo(self.name)
-        if not self.vid:
-            self.vid = match1(self.url, 'resourceId=([0-9]+)')
 
         data= get_response('https://api.joy.cn/v1/video',
-                           params={'id': self.vid}).json()
+                           params={'id': self.mid}).json()
         assert data['code'] > 0, data['message']
         data = data['data']
 
         info.title = data['title']
         url = data['res_url']
         _, ext, _ = url_info(url)
 
         info.streams['current'] = {
             'container': ext,
-            'video_profile': 'current',
+            'profile': 'current',
             'src': [url]
         }
         return info
 
 site = Joy()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/kankanews.py` & `ykdl-1.8.2/ykdl/extractors/kankanews.py`

 * *Files 8% similar despite different names*

```diff
@@ -32,14 +32,14 @@
         data = get_response('https://api-app.kankanews.com/kankan/pc/getvideo',
                             params=params).json()
         assert data['code'] == '10000', data['error']['message']
         data = data['result']['video']
 
         info.streams['current'] = {
             'container': 'mp4',
-            'video_profile': 'current',
+            'profile': 'current',
             'src' : [data['videourl']],
             'size': int(data['filesize'])
         }
         return info
 
 site = KankanNews()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/ku6.py` & `ykdl-1.8.2/ykdl/extractors/ku6.py`

 * *Files 8% similar despite different names*

```diff
@@ -14,14 +14,15 @@
     def list_only(self):
         return match(self.url, 'https://www.ku6.com/detail/\d+')
 
     def prepare_list(self):
         html = get_content(self.url)
         videos = matchall(html, "'title': '(.+?)',[\s\S]+?'playUrl': '(.+?)',")
         videos.reverse()
+        self.set_index(None, videos)
         for title, url in videos:
             info = MediaInfo(self.name)
             info.title = title
             info.streams['current'] = {
                 'container': 'mp4',
                 'src': [url]
             }
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/kuwo.py` & `ykdl-1.8.2/ykdl/extractors/kuwo.py`

 * *Files 8% similar despite different names*

```diff
@@ -2,41 +2,41 @@
 
 from ._common import *
 
 
 class Kuwo(Extractor):
     name = 'KuWo (酷我音乐)'
 
+    def prepare_mid(self):
+        return match1(self.url, '/play_detail/(\d+)')
+
     def prepare(self):
         info = MediaInfo(self.name)
         install_cookie()
 
-        if not self.vid:
-            self.vid = match1(self.url, '/play_detail/(\d+)')
-
         if not self.is_list:
             resp = get_response('https://www.kuwo.cn/favicon.ico?v=1')
         kw_token = get_cookie('www.kuwo.cn', '/', 'kw_token').value
         params = {
-            'mid': self.vid,
+            'mid': self.mid,
             'httpsStatus': 1,
             'reqId': get_random_uuid()
         }
         data = get_response('https://www.kuwo.cn/api/www/music/musicInfo',
                             headers={'csrf': kw_token},
                             params=params).json()
         assert data.get('code') == 200, data['message']
         data = data['data']
 
         pay = data['isListenFee']
         if pay:
             if self.is_list:  # just skip pay when extract from list
-                self.logger.warning('Skip pay song: %s', self.vid)
+                self.logger.warning('Skip pay song: %s', self.mid)
                 return
-            raise AssertionError('Pay song: %s' % self.vid)
+            raise AssertionError('Pay song: %s' % self.mid)
 
         albumpic = data['albumpic']
         album = data['album']
         title = data['name']
         info.title = album in title and title or '{title} - {album}'.format(**vars())
         info.artist = data['artist']
         info.album = data['album']
@@ -47,17 +47,16 @@
         data = get_response('https://www.kuwo.cn/api/v1/www/music/playUrl',
                             params=params).json()
         assert data.get('code') == 200, data['message']
 
         url = data['data']['url']
         info.streams['current'] = {
             'container': 'mp3',
-            'video_profile': 'current',
-            'src' : [url],
-            'size': 0
+            'profile': 'current',
+            'src': [url]
         }
         return info
 
     def list_only(self):
         return 'playlist_detail' in self.url
 
     def prepare_list(self):
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/laifeng.py` & `ykdl-1.8.2/ykdl/extractors/laifeng.py`

 * *Files 3% similar despite different names*

```diff
@@ -33,14 +33,14 @@
                                 'rd': random.randint(10000, 99999),
                             }).json()
         assert data['Code'] == 'Success', data['Message']
 
         stream_url = data['HttpFlv'][0]['Url']
         info.streams['current'] = {
             'container': 'flv',
-            'video_profile': 'current',
+            'profile': 'current',
             'src' : [stream_url],
-            'size': float('inf')
+            'size': Infinity
         }
         return info
 
 site = Laifeng()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/le/le.py` & `ykdl-1.8.2/ykdl/extractors/le.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 # -*- coding: utf-8 -*-
 
-from .._common import *
+from ._common import *
 
 
 def calcTimeKey(t):
     ror = lambda val, r_bits: ((val & (2**32-1)) >> r_bits%32) | \
                               (val << (32-(r_bits%32)) & (2**32-1))
     magic = 185025305
     return ror(t, magic % 17) ^ magic
 
-def decode(data):
+def decode_m3u8(data):
     version = data[0:5]
     if version.lower() == b'vc_01':
         #get real m3u8
         loc2 = bytearray(data[5:])
         length = len(loc2)
         loc4 = [0]*(2*length)
         for i in range(length):
@@ -24,88 +24,116 @@
         for i in range(length):
             loc7[i] = (loc6[2 * i] << 4) +loc6[2*i+1]
         return loc7
     else:
         # directly return
         return data
 
+headers = {
+    'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_12_4) '
+                  'AppleWebKit/603.1.30 (KHTML, like Gecko) '
+                  'Version/10.1 Safari/603.1.30'
+}
+
 class Letv(Extractor):
-    name = '乐视 (Letv)'
+    name = '乐视视频 (Letv)'
 
     stream_2_id_profile = {
         '1080p': ['BD', '1080P'],
          '1300': ['TD', '超清'],
          '1000': ['HD', '高清'],
          '720p': ['SD', '标清'],
           '350': ['LD', '流畅']
     }
 
     __STREAM_TEMP__ = []
 
+    def prepare_mid(self):
+        return match1(self.url, '/vplay/(\d+).html', '#record/(\d+)')
 
     def prepare(self):
         info = MediaInfo(self.name)
         stream_temp = {st: None for st in self.stream_2_id_profile.keys()}
         self.__STREAM_TEMP__.append(stream_temp)
-        if not self.vid:
-            self.vid = match1(self.url, 'vplay/(\d+).html', '#record/(\d+)')
 
         #normal process
-        data = get_response('http://player-pc.le.com/mms/out/video/playJson',
+        data = get_response('https://player-pc.le.com/mms/out/video/playJson',
                             params={
-                                'id': self.vid,
+                                'id': self.mid,
                                 'platid': 1,
                                 'splatid': 105,
                                 'format': 1,
                                 'tkey': calcTimeKey(int(time.time())),
                                 'domain': 'www.le.com',
                                 'region': 'cn',
                                 'source': 1000,
                                 'accessyx': 1
-                            }).json()['msgs']
+                            },
+                            headers=headers).json()['msgs']['playurl']
 
-        info.title = data['playurl']['title']
-        for stream, sdp in data['playurl']['dispatch'].items():
-            s_url = data['playurl']['domain'][0] + sdp[0]
-            data2 = get_response(s_url, params={
-                                            'm3v': 1,
-                                            'termid': 1,
-                                            'format': 1,
-                                            'hwtype': 'un',
-                                            'ostype': 'MacOS10.12.4',
-                                            'p1': 1,
-                                            'p2': 10,
-                                            'p3': '-',
-                                            'expect': '3',
-                                            'tn': random.random(),
-                                            'vid': self.vid,
-                                            'uuid': hash.sha1(s_url) + '_0',
-                                            'tss': 'ios'
-                                        }).json()
+        info.title = data['title']
+        info.duration = data['duration']
+        for stream, sdp in data['dispatch'].items():
+            s_url = data['domain'][0] + sdp[0]
+            data2 = get_response(s_url,
+                                 params={
+                                     'm3v': 1,
+                                     'termid': 1,
+                                     'format': 1,
+                                     'hwtype': 'un',
+                                     'ostype': 'MacOS10.12.4',
+                                     'p1': 1,
+                                     'p2': 10,
+                                     'p3': '-',
+                                     'expect': '3',
+                                     'tn': random.random(),
+                                     'vid': self.mid,
+                                     'uuid': hash.sha1(s_url) + '_0',
+                                     'tss': 'ios'
+                                 },
+                                 headers=headers).json()
 
             # hold on ! more things to do
             # to decode m3u8 (encoded)
             m3u8 = get_content(data2['location'],
                                params={
                                    'r': int(time.time() * 1000),
                                    'appid': 500
                                },
-                               charset='ignore')
-            m3u8_list = decode(m3u8)
-            stream_id, video_profile = self.stream_2_id_profile[stream]
+                               headers=headers, encoding=decode_m3u8)
+            stream_id, stream_profile = self.stream_2_id_profile[stream]
             info.streams[stream_id] = {
                 'container': 'm3u8',
-                'video_profile': video_profile,
-                'size' : 0
+                'profile': stream_profile
             }
-            stream_temp[stream] = compact_tempfile(mode='w+b', suffix='.m3u8')
-            stream_temp[stream].write(m3u8_list)
+            stream_temp[stream] = NamedTemporaryFile(mode='w+b', suffix='.m3u8')
+            stream_temp[stream].write(m3u8)
             info.streams[stream_id]['src'] = [stream_temp[stream].name]
             stream_temp[stream].flush()
 
         return info
 
+    def list_only(self):
+        return bool(match1(self.url, '/tv/\d+.html'))
+
     def prepare_list(self):
+        if self.list_only():
+            mid = None
+        else:
+            mid = self.mid
+            html = get_content(self.url)
+            pid = match1(html, r'\bpid: ?(\d+)')
+            if pid is None:
+                 return
+            self.url = 'https://www.le.com/tv/{pid}.html'.format(**vars())
+
         html = get_content(self.url)
-        return matchall(html, 'vid="(\d+)"')
+        vids = matchall(html, '/vplay/(\d+).html"')
+        mids = []
+        for vid in vids:
+            if vid in mids:
+                continue
+            mids.append(vid)
+        self.set_index(mid, mids)
+        return mids
 
 site = Letv()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/le/letvcloud.py` & `ykdl-1.8.2/ykdl/extractors/netease/livecc.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,65 +1,96 @@
 # -*- coding: utf-8 -*-
 
 from .._common import *
 
 
-class Letvcloud(Extractor):
-    name = '乐视云 (Letvcloud)'
+class NeteaseLive(Extractor):
+    name = '网易CC直播 (163)'
 
-    stream_2_id_profile = {
-        'yuanhua': ['BD', '原画'],
-          'super': ['TD', '超清'],
-           'high': ['HD', '高清'],
-            'low': ['SD', '标清']
+    profile_2_id = {
+        '原画': 'OG',
+        '蓝光': 'BD',
+        '超清': 'TD',
+        '高清': 'HD',
+        '标清': 'SD',
     }
 
-    def letvcloud_download_by_vu(self):
-        info = MediaInfo(self.name)
-        #ran = float('0.' + str(random.randint(0, 9999999999999999))) # For ver 2.1
-        #str2Hash = 'cfflashformatjsonran{ran}uu{uu}ver2.2vu{vu}bie^#@(%27eib58'.format(vu = vu, uu = uu, ran = ran)  #Magic!/ In ver 2.1
-        vu, uu = self.vid
-        params ={
-            'cf' : 'flash',
-            'format': 'json',
-            'ran': int(time.time()),
-            'uu': uu,
-            'ver': '2.2',
-            'vu': vu
-        }
-        sign_key = '2f9d6924b33a165a6d8b5d3d42f4f987'  #ALL YOUR BASE ARE BELONG TO US
-        str2Hash = ''.join([i + str(params[i]) for i in sorted(params)])
-        params['sign'] = hash.md5(str2Hash + sign_key)
-        data = get_response('http://api.letvcloud.com/gpc.php',
-                            params=params).json()
-        assert data['code'] == 0, data['message']
-        data = data['data']['video_info']
-
-        video_name = data['video_name']
-        if '.' in video_name:
-            ext = video_name.split('.')[-1]
-            info.title = video_name[0:-len(ext)-1]
-        else:
-            ext = 'mp4'
-            info.title = video_name
+    quality_2_profile = {
+     'blueray': '蓝光',
+       'ultra': '超清',
+        'high': '高清',
+    'standard': '标清',
+    }
 
-        media = data['media']
-        for st, (stream, profile) in self.stream_2_id_profile.items():
-            if st not in media:
-                continue
-            url = base64.b64decode(media[st]['play_url']['main_url']).decode()
-            info.streams[stream] = {
-                'container': ext,
-                'video_profile': profile,
-                'src': [url],
-                'size' : 0
-            }
-        return info
+    def prepare_mid(self):
+        return match1(self.url, '\D/(\d+)/?$')
 
     def prepare(self):
+        info = MediaInfo(self.name, True)
+
+        html = get_content(self.url, headers={'Referer': 'https://cc.163.com/'})
+        data = match1(html, '<script id="__NEXT_DATA__".*?>(.*?)</script>')
+        #self.logger.debug('data:\n%s', data)  # too long
+        data = json.loads(data)
+
+        def get_live_info(vbr=0):
+            params = vbr and {'vbr': vbr} or None
+            data = get_response('http://cgi.v.cc.163.com/video_play_url/{self.mid}'
+                                .format(**vars()), params=params).json()
+
+            stream_profile = data['vbrname_mapping'][data['pc_vbr_sel']]
+            stream_id = self.profile_2_id[stream_profile]
+            info.streams[stream_id] = {
+                'container': 'flv',
+                'profile': stream_profile,
+                'src' : [data['videourl']],
+                'size': Infinity
+            }
+
+            if vbr == 0:
+                vbr_sel = data['vbr_sel']
+                for vbr in data['vbr_list']:
+                    if vbr != vbr_sel:
+                        get_live_info(vbr)
+
+        try:
+            # project, select first living room
+            data = data['props']['pageProps']['data']
+            rooms = data['module_infos'][0]['content']
+
+        except KeyError:
+            data = data['props']['pageProps']['roomInfoInitData']
+            assert 'micfirst' in data, 'unsupported live!'
+
+            info.title = data['live']['title']
+            info.artist = data['micfirst']['nickname']
+
+            try:
+                streams = data['live']['quickplay']['resolution']
+            except KeyError:
+                get_live_info()
+            else:
+                for quality, stream in streams.items():
+                    stream_profile = self.quality_2_profile[quality]
+                    stream_id = self.profile_2_id[stream_profile]
+                    cdn = stream['cdn']
+                    cdn.pop('wy', None)  # UDP
+                    url = random.choice(list(cdn.values()))
+                    info.streams[stream_id] = {
+                        'container': 'flv',
+                        'profile': stream_profile,
+                        'src' : [url],
+                        'size': Infinity
+                    }
 
-        if self.url and not self.vid:
-            #maybe error!!
-            self.vid = (vu, uu) = matchall(self.url, 'vu=([^&]+)','uu=([^&]+)')
-        return self.letvcloud_download_by_vu()
+        else:
+            for room in rooms:
+                if room['is_living']:
+                    self.mid = room['ccid']
+                    info.artist = room['name']
+                    break
+            info.title = data['share_title']
+            get_live_info()
+
+        return info
 
-site = Letvcloud()
+site = NeteaseLive()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/le/live.py` & `ykdl-1.8.2/ykdl/extractors/acfun/live.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,83 +1,99 @@
 # -*- coding: utf-8 -*-
 
 from .._common import *
 
 
-def get_playback(vid):
-    from .le import Letv
-    site = Letv()
-    site.name = 'Le Live(乐视直播回看)'
-    site.vid = vid
-    return site.prepare()
-
-class LeLive(Extractor):
-    name = 'Le Live(乐视直播)'
-
-    stream_2_id_profile = {
-        'flv_1080p3m': ['BD', '1080p'],
-        'flv_1080p'  : ['BD', '1080p'],
-        'flv_1300'   : ['TD',  '超清'],
-        'flv_1000'   : ['HD',  '高清'],
-        'flv_720p'   : ['SD',  '标清'],
-        'flv_350'    : ['LD',  '流畅']
+class AcLive(Extractor):
+    name = 'AcFun 弹幕视频网 (直播)'
+
+    headers = {
+        'Accept': 'application/json, text/plain, */*',
+        'Referer': 'https://live.acfun.cn/'
     }
 
-    def prepare(self):
-        self.vid = match1(self.url, 'd=(\d+)', 'live/(\d+)')
-        if '/izt/' in self.url:
-            vid = self.vid
-            if not vid:
-                html = get_content(self.url)
-                vid = match1(html, 'vid\s*:\s*"(\d+)",', 'vid="(\d+)"')
-            return get_playback(vid)
-        else:
-            if not self.vid:
-                html = get_content(self.url)
-                self.vid = match1(html, 'liveId\s*:\s*"(\d+)"')
-
-        live_data = get_response(
-                'http://api.live.letv.com/v1/liveRoom/single/1001', 
-                params={'id': self.vid}).json()
-        if live_data.get('status') != 2:
-            return get_playback(live_data['recordingId'])
-
-        # live video is dead, the followed code will not be used
-        live_data = get_response(
-                'http://player.pc.le.com/player/startup_by_pid/1001/'
-                + self.vid,
-                params={'host': 'live.le.com'}).json()
+    @staticmethod
+    def profile_2_id(profile):
+        p1, p2 = matchm(profile, '(\S+) ?(\d+M)?')
+        id = {
+            '蓝光': 'BD',
+            '超清': 'TD',
+            '高清': 'HD'
+        }[p1]
+        if p2:
+            id += p2
+        return id
+
+    @staticmethod
+    def format_mid(mid):
+        mid = fullmatch(mid, '\d+')
+        assert mid
+        return mid
+
+    def prepare_mid(self):
+        return match1(self.url, '/live/(\d+)')
+
+    @functools.cache
+    def prepare_auth(self):
+        self.mid  # scan & check
+        did = 'web_{}{}{}'.format(random.randrange(1, 10),       # 9
+                                  random.randrange(1, 10 ** 7),  # 9999999
+                                  get_random_hex(8).upper())     # FFFFFFFF
+        self.headers['Cookie'] = {'_did': did}
+        data = get_response(
+                'https://id.app.acfun.cn/rest/app/visitor/login',
+                data=b'sid=acfun.api.visitor',
+                headers=self.headers
+            ).json()
+        assert data['result'] == 0, data['error_msg']
+        return did, data['userId'], data['acfun.api.visitor_st']
 
+    def prepare(self):
         info = MediaInfo(self.name, True)
-        info.title = live_data['title']
 
-        for st in live_data['rows']:
-            stream, profile = self.stream_2_id_profile[st['rateType']]
-            data = get_response(st['streamUrl'],
-                                params={
-                                    'format': 1,
-                                    'expect': 2,
-                                    'termid': 1,
-                                    'platid': 10,
-                                    'playid': 1,
-                                    'sign': 'live_web',
-                                    'splatid': 1001,
-                                    'vkit': 20161017,
-                                    'station': self.vid
-                                }).json()
-            src = data['location']
-            info.streams[stream] = {
-                'container': 'm3u8',
-                'video_profile': profile,
-                'size' : float('inf'),
-                'src' : [src]
+        did, user_id, visitor_st = self.prepare_auth()
+        data = get_response(
+                'https://api.kuaishouzt.com/rest/zt/live/web/startPlay',
+                params={
+                    'subBiz': 'mainApp',
+                    'kpn': 'ACFUN_APP',
+                    'kpf': 'PC_WEB',
+                    'userId': user_id,
+                    'did': did,
+                    'acfun.api.visitor_st': visitor_st
+                },
+                data={
+                    'authorId': self.mid,
+                    'pullstreamType': 'FLV'
+                },
+                headers=self.headers
+            ).json()
+        assert data['result'] == 1, data['error_msg']
+        data = data['data']
+
+        info.title = data['caption']
+
+        data = json.loads(data['videoPlayRes'])
+        for stream in data['liveAdaptiveManifest'][0]['adaptationSet']['representation']:
+            stream_profile = stream['name']
+            stream_id = self.profile_2_id(stream_profile)
+            info.streams[stream_id] = {
+                'container': 'flv',
+                'profile': stream_profile,
+                'src' : [stream['url']],
+                'size': Infinity
             }
 
-        return info
+        data = get_response(
+                'https://live.acfun.cn/rest/pc-direct/user/userInfo',
+                params={'userId': self.mid},
+                headers=self.headers
+            ).json()
+        assert data['result'] == 0, data['error_msg']
+        data = data['profile']
+
+        info.artist = data['name']
+        info.add_comment(data['signature'])
 
-    def prepare_list(self):
-        html = get_content(self.url)
-        vids = matchall(html, 'vid="(\d+)"')
-        # fake urls
-        return ['http://live.le.com/izt/vid={}'.format(vid) for vid in vids]
+        return info
 
-site = LeLive()
+site = AcLive()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/le/lunbo.py` & `ykdl-1.8.2/ykdl/extractors/netease/music/mv.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,53 +1,42 @@
 # -*- coding: utf-8 -*-
 
-from .._common import *
+from ..._common import *
 
 
-class LeLunbo(Extractor):
-    name = 'Le Lunbo (乐视轮播)'
+class NeteaseMv(Extractor):
+    name = 'Netease MV (网易音乐 MV)'
 
-    stream_2_id_profile = {
-        'flv_1080p3m': ['BD', '1080p'],
-        'flv_1080p'  : ['BD', '1080p'],
-        'flv_1300'   : ['TD',  '超清'],
-        'flv_1000'   : ['HD',  '高清'],
-        'flv_720p'   : ['SD',  '标清'],
-        'flv_350'    : ['LD',  '流畅']
+    resolution_2_id_profile = {
+        '1080': ['BD', '1080P'],
+         '720': ['TD', '超清'],
+         '480': ['HD', '高清'],
+         '240': ['SD', '标清']
     }
 
+    def prepare_mid(self):
+        return match1(self.url, '\?id=(.*)', 'mv/(\d+)')
+
     def prepare(self):
-        info = MediaInfo(self.name, True)
-        if not self.vid:
-            self.vid = match1(self.url, 'channel=([\d]+)')
-
-        live_data = get_response(
-                'http://player.pc.le.com/player/startup_by_channel_id/1001/'
-                + self.vid,
-                params={'host': 'live.le.com'}).json()
-        info.title = live_data['channelName']
-
-        for st in live_data['streams']:
-            stream, profile = self.stream_2_id_profile[st['rateType']]
-            data = get_response(st['streamUrl'],
-                                params={
-                                    'format': 1,
-                                    'expect': 2,
-                                    'termid': 1,
-                                    'platid': 10,
-                                    'playid': 1,
-                                    'sign': 'live_web',
-                                    'splatid': 1001,
-                                    'vkit': 20161017,
-                                    'station': self.vid
-                                }).json()
-            src = data['location']
-            info.streams[stream] = {
-                'container': 'm3u8',
-                'video_profile': profile,
-                'size' : float('inf'),
-                'src' : [src]
-            }
+        info = MediaInfo(self.name)
+
+        data = get_response('http://music.163.com/api/mv/detail/',
+                          params={
+                              'id': self.mid,
+                             'ids': self.mid,
+                      'csrf_token': ''
+                          }).json()['data']
+
+        info.title = data['name']
+        info.artist = data['artistName']
+        for resolution in self.resolution_2_id_profile.keys():
+            if resolution in data['brs']:
+                stream_id, stream_profile = self.resolution_2_id_profile[id]
+                info.streams[stream_id] = {
+                    'container': 'mp4',
+                    'profile': stream_profile,
+                    'src': [data['brs'][id]]
+                }
 
         return info
 
-site = LeLunbo()
+site = NeteaseMv()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/lizhi.py` & `ykdl-1.8.2/ykdl/extractors/lizhi.py`

 * *Files 16% similar despite different names*

```diff
@@ -2,32 +2,34 @@
 
 from ._common import *
 
 
 class Lizhi(Extractor):
     name = 'Lizhi FM (荔枝电台)'
 
+    def prepare_mid(self):
+        pass
+
     def prepare(self):
         info = MediaInfo(self.name)
 
         html = get_content(self.url)
-        self.vid, info.artist, _, info.title = matchm(html,
+        self.mid, info.artist, _, info.title = matchm(html,
                 'data-hidden-ph\s?=\s?"(.+?)" '
                 'data-user-name\s?=\s?"(.+?)" '
                 'data-radio-name\s?=\s?"(.+?)" '
                 'data-title\s?=\s?"(.+?)"')
-        data = get_response('https://www.lizhi.fm/hidden_ph/' +
-                            self.vid).json()
+        data = get_response('https://www.lizhi.fm/hidden_ph/{self.mid}'
+                            .format(**vars())).json()
         assert data['rcode'] == 0, data['msg']
 
         info.streams['current'] = {
             'container': 'mp3',
-            'video_profile': 'current',
-            'src' : [data['data']['url']],
-            'size': 0
+            'profile': 'current',
+            'src': [data['data']['url']]
         }
         return info
 
     def list_only(self):
         return 'user' in self.url
 
     def prepare_list(self):
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/longzhu.py` & `ykdl-1.8.2/ykdl/extractors/longzhu.py`

 * *Files 7% similar despite different names*

```diff
@@ -2,36 +2,37 @@
 
 from ._common import *
 
 
 class LongzhuLive(Extractor):
     name = 'Longzhu Live (龙珠直播)'
 
+    def prepare_mid(self):
+        return match1(get_content(self.url), '(?i)"roomid":(\d+)')
+
     def prepare(self):
         info = MediaInfo(self.name, True)
 
         html = get_content(self.url)
-        self.vid = match1(html, '(?i)"roomid":(\d+)')
         info.title = match1(html, '"title":"([^"]+)', '<title>([^>]+)<')
         info.artist = match1(html, '"Name":"([^"]+)')
 
         data = get_response('http://livestream.longzhu.com/live/getlivePlayurl',
                             params={
-                                'roomId': self.vid,
+                                'roomId': self.mid,
                                 'utmSr': '',
                                 'platform': 'h5',
                                 'device': 'pc'
                             }).json()['playLines']
         assert data, 'Live is offline!!'
 
         for i in data[0]['urls']:
             ext = i['ext']
             info.streams[ext] = {
                 'container': ext,
-                'video_profile': i['description'],
-                'src' : [i['securityUrl']],
-                'size': 0
+                'profile': i['description'],
+                'src': [i['securityUrl']]
             }
 
         return info
 
 site = LongzhuLive()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/mgtv.py` & `ykdl-1.8.2/ykdl/extractors/mgtv.py`

 * *Files 13% similar despite different names*

```diff
@@ -22,50 +22,50 @@
 def generate_tk2(did):
     s = 'did={}|pno=1030|ver=0.3.0301|clit={}'.format(did, int(time.time()))
     return encode_tk2(s)
 
 class Hunantv(Extractor):
     name = '芒果TV (HunanTV)'
 
-    profile_2_types = {
-        '复刻版': 'BD',
+    profile_2_id = {
+      '复刻版': 'BD',
         '蓝光': 'BD',
         '超清': 'TD',
         '高清': 'HD',
         '标清': 'SD'
     }
 
+    def prepare_mid(self):
+        mid = match1(self.url, 'com/[bl]/\d+/(\d+).html',
+                               'com/s/(\d+).html')
+        if mid is None:
+            html = get_content(self.url)
+            if match1(self.url, 'com/h/(\d+).html'):
+                assert JSEngine, 'No JS Interpreter found!!!'
+                js_ctx = JSEngine()
+                js = match1(html, '<script>window.__NUXT__=(.+);</script>')
+                data = js_ctx.eval(js)
+                mid = match1(data, "PartId': '(\d+)'")
+            else:
+                mid = match1(html,
+                             'window.location = "/b/\d+/(\d+).html"',
+                            r'routePath:"\\u002Fl\\u002F\d+\\u002F(\d+).html"',
+                             'vid[=:]\D?(\d+)')
+        return mid
+
     def prepare(self):
         info = MediaInfo(self.name)
-        install_cookie()
         info.extra.referer = self.url
-
-        if self.url and not self.vid:
-            self.vid = match1(self.url, 'com/[bl]/\d+/(\d+).html')
-            if self.vid is None:
-                self.vid = match1(self.url, 'com/s/(\d+).html')
-            if self.vid is None:
-                html = get_content(self.url)
-                if match1(self.url, 'com/h/(\d+).html'):
-                    assert JSEngine, 'No JS Interpreter found!!!'
-                    js_ctx = JSEngine()
-                    js = match1(html, '<script>window.__NUXT__=(.+);</script>')
-                    data = str(js_ctx.eval(js))
-                    self.vid = match1(data, "PartId': '(\d+)'")
-                else:
-                    self.vid = match1(html, 'window.location = "/b/\d+/(\d+).html"',
-                                           r'routePath:"\\u002Fl\\u002F\d+\\u002F(\d+).html"',
-                                            'vid[=:]\D?(\d+)')
-        assert self.vid, 'can not find video!!!'
+        install_cookie()
 
         did = get_random_uuid()
         tk2 = generate_tk2(did)
         params = {
             'tk2': tk2,
-            'video_id': self.vid,
+            'video_id': self.mid,
             'type': 'pch5'
         }
         data = get_response('https://pcweb.api.mgtv.com/player/video',
                             params=params).json()
         assert data['code'] == 200, ('[failed] code: {}, msg: {}'
                                      .format(data['code'], data['msg']))
         assert data['data'], '[Failed] Video info not found.'
@@ -83,18 +83,18 @@
 
         domain = data['stream_domain'][0]
         for lstream in data['stream']:
             lurl = lstream['url']
             if lurl:
                 url = get_response(domain + lurl,
                                    params={'did': did}).json()['info']
-                video_profile = lstream['name']
-                stream = self.profile_2_types[video_profile]
-                info.streams[stream] = {
+                stream_profile = lstream['name']
+                stream_id = self.profile_2_id[stream_profile]
+                info.streams[stream_id] = {
                     'container': 'm3u8',
-                    'video_profile': video_profile,
-                    'src' : [url]
+                    'profile': stream_profile,
+                    'src': [url]
                 }
 
         return info
 
 site = Hunantv()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/miaopai.py` & `ykdl-1.8.2/ykdl/extractors/miaopai.py`

 * *Files 20% similar despite different names*

```diff
@@ -9,82 +9,77 @@
 api_info2 = 'http://api.miaopai.com/m/v2_channel.json?fillType=259&scid={}&vend='
 api_stream = 'http://gslb.miaopai.com/stream/{}.json?vend='
 
 class Miaopai(Extractor):
 
     name = '秒拍 (Miaopai)'
 
+    def prepare_mid(self):
+        mid = match1(self.url, '/media/([^\./]+)')
+        if mid is None:
+            html = get_content(self.url)
+            mid = match1(html, 's[cm]id ?= ?[\'"]([^\'"]+)[\'"]')
+        return mid
+
     def prepare(self):
         info = MediaInfo(self.name)
-        html = None
         title = None
 
         if 'show' in self.url:
             new_url = get_location(self.url)
             if new_url != self.url:
                 self.logger.debug('redirect to' + new_url)
                 self.url = new_url
 
-        if not self.vid:
-            self.vid = match1(self.url, '/media/([^\./]+)')
-        if not self.vid:
-            html = get_content(self.url)
-            self.vid = match1(html, 's[cm]id ?= ?[\'"]([^\'"]+)[\'"]')
-        assert self.vid, 'No VID match!'
-        info.title = self.name + '_' + self.vid
-
-
-        if len(self.vid) > 24:
+        if len(self.mid) > 24:
             add_header('Referer', self.url)
-            cb = '_jsonp{}'.format(get_random_str(10))
-            json_html = get_content(api_info1.format(self.vid, cb))
+            cb = '_jsonp{}'.format(get_random_str(10).lower())
+            data = get_response(api_info1.format(self.mid, cb)).json()
             data = json.loads(json_html[json_html.find('{'):-2])
             assert data['code'] == 200, data['msg']
 
             data = data['data']
             title = data['description']
             url = data['meta_data'][0]['play_urls']['m']
             _, ext, _ = url_info(url)
         
         else:
             try:
-                data = get_response(api_info2.format(self.vid)).json()
+                data = get_response(api_info2.format(self.mid)).json()
                 assert data['status'] == 200, data['msg']
 
                 data = data['result']
                 title = data['ext']['t']
-                scid = data['scid'] or self.vid
+                scid = data['scid'] or self.mid
                 ext = data['stream']['and']
                 base = data['stream']['base']
                 vend = data['stream']['vend']
                 url = '{base}{scid}.{ext}?vend={vend}'.format(**vars())
             except:
                 # fallback
-                data = get_response(api_stream.format(self.vid)).json()
+                data = get_response(api_stream.format(self.mid)).json()
                 assert data['status'] == 200, data['msg']
 
                 data = data['result'][0]
                 ext = None
                 scheme = data['scheme']
                 host = data['host']
                 path = data['path']
                 sign = data['sign']
                 url = '{scheme}{host}{path}{sign}'.format(**vars())
 
         if not title:
-            if not html:
-                html = get_content(self.url)
+            html = get_content(self.url)
             title = match1(html, '<meta name="description" content="([^"]+)">')
-        if title:
-            info.title = title
+        info.title = title
 
         info.streams['current'] = {
             'container': ext or 'mp4',
-            'src': [url],
-            'size' : 0
+            'profile': 'current',
+            'src': [url]
         }
         return info
 
     def prepare_list(self):
         html = get_content(self.url)
         video_list = match1(html, 'video_list=\[([^\]]+)')
         return matchall(video_list, '"([^",]+)')
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/netease/__init__.py` & `ykdl-1.8.2/ykdl/extractors/netease/__init__.py`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/netease/live.py` & `ykdl-1.8.2/ykdl/extractors/netease/live.py`

 * *Files 13% similar despite different names*

```diff
@@ -2,34 +2,37 @@
 
 from .._common import *
 
 
 class NeteaseLive(Extractor):
     name = '网易直播 (163)'
 
+    def prepare_mid(self):
+        return match1(self.url, 'room/(\d+)')
+
     def prepare(self):
         info = MediaInfo(self.name, True)
 
-        if self.vid is None:
-            self.vid = match1(self.url, 'room/(\d+)')
-
-        tt = int(time.time() * 1000)
-        url = 'https://data.live.126.net/liveAll/{self.vid}.json?{tt}'.format(**vars())
-        data = get_response(url).json()
+        data = get_response(
+            'https://data.live.126.net/liveAll/{self.mid}.json'.format(**vars()),
+            params={'tt': int(time.time() * 1000)}
+        ).json()
         assert 'liveVideoUrl' in data, 'live video is offline'
 
         info.title = data['roomName']
         try:
             info.artist = data['sourceinfo']['tname']
         except KeyError:
             pass
+        info.duration = duration = data.get('duration')
+        info.add_comment = data['channal']['name']
 
         url = data['liveVideoUrl']
         info.streams['current'] = {
             'container': url.split('.')[-1],
-            'video_profile': 'current',
+            'profile': 'current',
             'src': [url],
-            'size': 0
+            not duration and 'size': Infinity
         }
         return info
 
 site = NeteaseLive()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/netease/m3g.py` & `ykdl-1.8.2/ykdl/extractors/netease/m3g.py`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/netease/music/music.py` & `ykdl-1.8.2/ykdl/extractors/netease/music/music.py`

 * *Files 19% similar despite different names*

```diff
@@ -2,34 +2,35 @@
 
 from ..._common import *
 from .musicbase import NeteaseMusicBase
 
 
 class NeteaseMusic(NeteaseMusicBase):
     name = 'Netease Music (网易云音乐)'
-    api_url = 'http://music.163.com/api/song/detail/?id={}&ids=[{}]&csrf_token='
+    api_url = 'http://music.163.com/api/song/detail/'
 
     def get_music(self, data):
         return data['songs'][0]
 
     def prepare_list(self):
-        vid =  match1(self.url, '\?id=(.*)')
         params = {
-            'id': vid,
+            'id': self.mid,
             'csrf_token': ''
         }
         if 'album' in self.url:
-            listdata =  get_response('http://music.163.com/api/album/' + vid,
-                                     params=params).json()
-            playlist = listdata['album']['songs']
+            data =  get_response('http://music.163.com/api/album/' + self.mid,
+                                 params=params).json()
+            playlist = data['album']['songs']
         elif 'playlist' in self.url or 'toplist' in self.url:
-            listdata =  get_response('http://music.163.com/api/playlist/detail',
-                                     params=params).json()
-            playlist = listdata['result']['tracks']
+            data =  get_response('http://music.163.com/api/playlist/detail',
+                                 params=params).json()
+            playlist = data['result']['tracks']
         elif 'artist' in self.url:
-            listdata =  get_response('http://music.163.com/api/artist/' + vid,
-                                     params=params).json()
-            playlist = listdata['hotSongs']
-
-        return [p['id'] for p in playlist]
+            data =  get_response('http://music.163.com/api/artist/' + self.mid,
+                                 params=params).json()
+            playlist = data['hotSongs']
+
+        mids = [p['id'] for p in playlist]
+        self.set_index(self.mid, mids)
+        return mids
 
 site = NeteaseMusic()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/netease/music/musicbase.py` & `ykdl-1.8.2/ykdl/extractors/netease/music/musicbase.py`

 * *Files 14% similar despite different names*

```diff
@@ -52,34 +52,41 @@
     payload['params'] = second_pass
     payload['encSecKey'] = encSecKey
 
     return payload
 
 class NeteaseMusicBase(Extractor):
 
-    mp3_api = 'http://music.163.com/weapi/song/enhance/player/url?csrf_token='
+    def prepare_mid(self):
+        return match1(self.url, r'\bid=(\w+)', 'song/(\d+)')
 
     def prepare(self):
         info = MediaInfo(self.name)
-        if not self.vid:
-            self.vid =  match1(self.url, 'song/(\d+)', '\?id=(.*)')
-        api_url = self.api_url.format(self.vid, self.vid)
-        music = self.get_music(get_response(api_url).json())
-        self.logger.debug('music info:\n%s', music)
-        info.title = music['name']
-        info.artist = music['artists'][0]['name']
 
-        real_id = music['id']
+        data = get_response(self.api_url, params={
+                                              'id': self.mid,
+                                             'ids': self.mid,
+                                      'csrf_token': ''
+                                          }).json()
+        data = self.get_music(data)
+        self.logger.debug('data:\n%s', data)
 
+        info.title = data['name']
+        info.artist = data['artists'][0]['name']
+
+        real_id = data['id']
         snd_key = get_random_str(16, 'snd_key')
         encSecKey = RSA_string(snd_key)
         payload = netease_req(real_id, snd_key, encSecKey)
+        data = get_response(
+            'http://music.163.com/weapi/song/enhance/player/url?csrf_token=',
+            data=payload).json()['data'][0]
+        self.logger.debug('mp3 data:\n%s', data)
 
-        mp3_info = get_response(self.mp3_api, data=payload).json()['data'][0]
-        self.logger.debug('mp3:\n%s', mp3_info)
         info.streams['current'] =  {
-            'container': mp3_info['type'],
-            'video_profile': 'current',
-            'src' : [mp3_info['url']],
-            'size': mp3_info['size']
+            'container': data['type'],
+            'profile': 'current',
+            'src' : [data['url']],
+            'size': data['size']
         }
+
         return info
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/netease/openc.py` & `ykdl-1.8.2/ykdl/extractors/netease/openc.py`

 * *Files 17% similar despite different names*

```diff
@@ -15,45 +15,59 @@
     ]
     name2lang = {
         '中文': 'zh',
         '英文': 'en'
     }
 
     def list_only(self):
-        self.vid = match1(self.url, 'mid=(\w+)')
-        return self.vid is None
+        return self.mid[1] is None
 
-    def prepare_data(self):
-        html = get_content(self.url)
+    @staticmethod
+    def format_mid(mid):
+        if not isinstance(mid, tuple):
+            mid = mid, None
+        mid = mid[:2]
+        assert len(mid) == 2 and mid[0]
+        return mid
+
+    def prepare_mid(self):
+        return match1(self.url, r'\bpid=(\w+)'), match1(self.url, r'\bmid=(\w+)')
+
+    @functools.cache
+    def parse_html(self, url):
+        html = get_content(url)
         js = match1(html, 'window\.__NUXT__=(.+);</script>')
-        js_ctx = JSEngine()
-        data = js_ctx.eval(js)
-        self.logger.debug('video_data: \n%s', data)
+        data = JSEngine().eval(js)
+        self.logger.debug('data: \n%s', data)
+        return data
+
+    def prepare_data(self):
+        url = 'https://open.163.com/newview/movie/free?pid={}'.format(self.mid[0])
+        data = self.parse_html(url)
         try:
             self.url = data['data'][0]['playUrl']
         except KeyError:
-            self.data = data
+            return data
         else:
-            self.prepare_data()
+            self.mid = None
+            return self.prepare_data()
 
     def prepare(self):
         info = MediaInfo(self.name)
 
-        if self.data is None:
-            self.prepare_data()
-        data = self.data
+        data = self.prepare_data()
         moiveList = data['state']['movie']['moiveList']
-        if self.vid is None:
-            movie = moiveList[0]
-        else:
-            for movie in moiveList:
-                mid = movie['mid']
-                if mid == self.vid:
-                    break
-            assert mid == self.vid, "can't found mid %r" % mid
+        if not moiveList:
+            return
+
+        mid = self.mid[1]
+        for movie in moiveList:
+            if movie['mid'] == mid:
+                break
+        assert movie['mid'] == mid, "can't found mid %r" % mid
 
         title = data['data'][0]['title']
         mtitle = movie['title'].rpartition(title)[-1]
         if mtitle:
             for sp in ['：', '】']:
                 t1, _, t2 = mtitle.partition(sp)
                 if title.startswith(t1):
@@ -78,27 +92,27 @@
         else:
             director = school
         if school not in title:
             title = '[{school}] {title}'.format(**vars())
         info.title = title
         info.artist = director
 
-        for stream, tp, profile in self.sopported_stream_types:
+        for stream_id, tp, stream_profile in self.sopported_stream_types:
             for ext in ['mp4', 'm3u8']:
                 for orig in ['', 'Orign']:
-                    if stream in info.streams:
+                    if stream_id in info.streams:
                         continue
                     url = movie['{ext}{tp}Url{orig}'.format(**vars())]
                     if not url:
                         continue
                     size = movie['{ext}{tp}Size{orig}'.format(**vars())]
-                    info.streams[stream] = {
+                    info.streams[stream_id] = {
                         'container': ext,
-                        'video_profile': profile,
-                        'src': [url],
+                        'profile': stream_profile,
+                        'src' : [url],
                         'size': size
                     }
 
         nlang = 0
         for sub in movie['subList']:
             name = sub['subName']
             if not name:
@@ -108,18 +122,22 @@
                     name = '中文'
                 nlang += 1
             lang = self.name2lang[name]
             info.subtitles.append({
                 'lang': lang,
                 'name': name,
                 'format': 'srt',
-                'src': sub['subUrl'],
+                'src' : sub['subUrl'],
                 'size': sub['subSize']
             })
 
         return info
 
     def prepare_list(self):
-        self.prepare_data()
-        return [movie['mid'] for movie in self.data['state']['movie']['moiveList']]
+        data = self.prepare_data()
+        pid, mid = self.mid
+        mids = [movie['mid'] for movie in data['state']['movie']['moiveList']]
+        self.set_index(mid, mids)
+        for mid in mids:
+            yield pid, mid
 
 site = OpenC()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/pps.py` & `ykdl-1.8.2/ykdl/extractors/pps.py`

 * *Files 4% similar despite different names*

```diff
@@ -6,19 +6,19 @@
 def gsign(params):
     s = []
     for key in sorted(params.keys()):
         s.append('{}:{}'.format(key, params[key]))
     s.append('w!ytDgy#lEXWoJmN4HPf')
     return hash.sha1(''.join(s))
 
-def getlive(uid, rate='source'):
+def getlive(mid, rate='source'):
     params = {
         'type_id': 1,
         'vid': 1,
-        'anchor_id': uid,
+        'anchor_id': mid,
         'app_key': 'show_web_h5',
         'version': '1.0.0',
         'platform': '1_10_101',
         'time': int(time.time()),
         'netstat': 'wifi',
         'device_id': get_random_id(32, 'device'),
         'bit_rate_type': rate,
@@ -33,41 +33,45 @@
 
     rate_2_id_profile = {
         'source': ['TD', '超清'],
           'high': ['HD', '高清'],
         'smooth': ['SD', '标清']
     }
 
+    def prepare_mid(self):
+        html = get_content(self.url)
+        return match1(html, '"user_id":"([^"]+)",')
+
     def prepare(self):
         info = MediaInfo(self.name, True)
+
         html = get_content(self.url)
-        self.vid = match1(html, '"user_id":"([^"]+)",')
         title = json.loads(match1(html, '"room_name":("[^"]*"),'))
         artist = json.loads(match1(html, '"nick_name":("[^"]+"),'))
         info.title = '{title} - {artist}'.format(**vars())
         info.artist = artist
 
         def get_live_info(rate='source'):
-            data = getlive(self.vid, rate)
+            data = getlive(self.mid, rate)
             if data['code'] != 'A00000':
                 return data.get('msg')
 
             data = data['data']
             url = data.get('https_flv') or data.get('flv') or data.get('rtmp')
             if url:
                 url = url.replace('rtmp://', 'http://')
                 ran = random.randrange(1e4)
                 sep = '?' in url and '&' or '?'
                 url = '{url}{sep}ran={ran}'.format(**vars())
                 stream_id, stream_profile = self.rate_2_id_profile[rate]
                 info.streams[stream_id] = {
-                    'video_profile': stream_profile,
                     'container': 'flv',
+                    'profile': stream_profile,
                     'src' : [url],
-                    'size': float('inf')
+                    'size': Infinity
                 }
 
             error_msges = []
             if rate == 'source':
                 rate_list = data['rate_list']
                 if 'source' in rate_list:
                     rate_list.remove('source')
@@ -76,13 +80,12 @@
                         if error_msg:
                             error_msges.append(error_msg)
             if error_msges:
                 return ', '.join(error_msges)
 
         error_msg = get_live_info()
         if error_msg:
-            self.logger.debug('error_msg:\n' + error_msg)
-        assert info.streams, error_msg or "can't play this live video!!"
+            self.logger.debug('error_msg:\n\t' + error_msg)
 
         return info
 
 site = PPS()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/pptv.py` & `ykdl-1.8.2/ykdl/extractors/pptv.py`

 * *Files 18% similar despite different names*

```diff
@@ -11,22 +11,23 @@
         'BD': '蓝光',
         'TD': '超清',
         'HD': '高清',
         'SD': '高清',
         'LD': '流畅'
     }
 
+    def prepare_mid(self):
+        html = get_content(self.url)
+        return match1(html, '"(?:c|ps)id":"?(\d+)')
+
     def prepare(self):
         info = MediaInfo(self.name)
 
-        html = get_content(self.url)
-        self.vid = match1(html, '"(?:c|ps)id":"?(\d+)')
-
         #key = gen_key(int(time.time()) - 60)
-        data = get_response('https://web-play.pptv.com/webplay3-0-{self.vid}.xml'
+        data = get_response('https://web-play.pptv.com/webplay3-0-{self.mid}.xml'
                             .format(**vars()),
                             params={
                                 'zone': 8,
                                 'version': 4,
                                 'username': '',
                                 'ppi': '302c3333',
                                 'type': 'ppbox.launcher',
@@ -55,19 +56,19 @@
                 'type': 'ppbox.launcher'
             })
             urls = []
             for seg in drag['sgm']:
                 no = seg['@no']
                 urls.append('http://{host}/{no}/{rid}?{params}'.format(**vars()))
 
-            stype = format_vps(item['@width'], item['@height'])[0]
-            video_profile = self.id_2_profile[stype]
-            info.streams[stype] = {
+            stream_id = format_vps(item['@width'], item['@height'])[0]
+            stream_profile = self.id_2_profile[stream_id]
+            info.streams[stream_id] = {
                 'container': 'mp4',
-                'video_profile': video_profile,
-                'size': int(item['@filesize']),
-                'src': urls
+                'profile': stream_profile,
+                'src' : urls,
+                'size': int(item['@filesize'])
             }
 
         return info
 
 site = PPTV()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/qq/egame.py` & `ykdl-1.8.2/ykdl/extractors/qq/egame.py`

 * *Files 16% similar despite different names*

```diff
@@ -15,20 +15,28 @@
          6: 'BD6M',
          4: 'BD4M',
          3: 'TD',
          2: 'HD',
          1: 'SD',
     }
 
+    @staticmethod
+    def format_mid(mid):
+        mid = fullmatch(mid, '\d+')
+        assert mid
+        return mid
+
+    def prepare_mid(self):
+        return match1(self.url, '/(\d+)')
+
     def prepare(self):
         info = MediaInfo(self.name, True)
-        if not self.vid:
-            self.vid = match1(self.url, '/(\d+)')
-        if not self.url:
-            self.url = 'https://egame.qq.com/' + self.vid
+
+        if self.url is None:
+            self.url = 'https://egame.qq.com/' + self.mid
         html = get_content(self.url)
 
         js_nuxt = match1(html, '<script>window.__NUXT__=(.+?)</script>')
         js_ctx = JSEngine()
         data = js_ctx.eval(js_nuxt)
         self.logger.debug('data:\n%s', data)
 
@@ -42,19 +50,19 @@
         assert profileInfo['isLive'], 'error: live show is not on line!!'
 
         title = videoInfo['title']
         info.artist = artist = profileInfo['nickName']
         info.title = '{title} - {artist}'.format(**vars())
 
         for s in videoInfo['streamInfos']:
-            stream = self.lv_2_id[s['levelType']]
-            info.streams[stream] = {
+            stream_id = self.lv_2_id[s['levelType']]
+            info.streams[stream_id] = {
                 'container': 'flv',
-                'video_profile': s['desc'],
-                'src': [s['playUrl']],
-                'size': float('inf')
+                'profile': s['desc'],
+                'src' : [s['playUrl']],
+                'size': Infinity
             }
 
         return info
 
 
 site = QQEGame()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/qq/live.py` & `ykdl-1.8.2/ykdl/extractors/zhuafan.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,36 +1,48 @@
 # -*- coding: utf-8 -*-
 
-from .._common import *
+from ._common import *
 
 
-class QQLive(Extractor):
-    name = 'QQ Live (企鹅直播)'
+class JustFunLive(Extractor):
+    name = '抓饭直播 (JustFun Live)'
+
+    def prepare_mid(self):
+        return match1(self.url, 'live/(\d+)')
 
     def prepare(self):
         info = MediaInfo(self.name, True)
-        if not self.vid:
-            self.vid = match1(self.url, '/(\d+)')
-        if not self.vid:
-            html = get_content(self.url)
-            self.vid = match1(html, '"room_id":(\d+)')
 
-        #from upstream!!
-        data = get_response('http://www.qie.tv/api/v1/room/' + self.vid).json()
-        assert data['error'] == 0, 'error {}: {}'.format(data['error'], data['data'])
+        try:
+            data = get_response(
+                    'https://www.zhuafan.tech/live-channel-info/channel/v2/info',
+                    params={
+                        'cid': self.mid,
+                        'decrypt': 1
+                    }).json()
+        except:
+            html = get_content(self.url)
+            data = match1(html, 'window\.__INITIAL_STATE__ = ({.+})</script>')
+            self.logger.debug('data:\n%s', data)
+            data = json.loads(data)['channel']
 
-        livedata = data['data']
-        assert livedata['show_status'] == '1', 'error: live show is not on line!!'
+        assert data['playStatusCode'] == 0, data['playStatusCodeDesc']
 
-        info.title = livedata['room_name']
-        info.artist = livedata['nickname']
+        info.artist = data['uname']
+        info.title = data['cname']
 
-        info.streams['current'] = {
+        info.streams['OG-FLV'] = {
             'container': 'flv',
-            'video_profile': 'current',
-            'src' : ['{}/{}'.format(livedata['rtmp_url'], livedata['rtmp_live'])],
-            'size': float('inf')
+            'profile': 'current',
+            'src' : [data['httpsPlayInfo']],
+            'size': Infinity
         }
+        info.streams['OG-HLS'] = {
+            'container': 'm3u8',
+            'profile': 'current',
+            'src' : [data['hlsPlayInfo']],
+            'size': Infinity
+        }
+
         return info
 
-site = QQLive()
-            
+site = JustFunLive()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/qq/video.py` & `ykdl-1.8.2/ykdl/extractors/qq/video.py`

 * *Files 8% similar despite different names*

```diff
@@ -29,51 +29,46 @@
 
 class QQ(Extractor):
 
     name = '腾讯视频 (QQ)'
     vip = None
 
     stream_2_id = {
-        'fhd': 'BD',
-        'shd': 'TD',
+        'fhd': 'BD',  #
+        'shd': 'TD',  # null
          'hd': 'HD',
         'mp4': 'HD',
         'flv': 'HD',
          'sd': 'SD',
         'msd': 'LD'
     }
 
 
-    def get_streams_info(self, profile='shd'):
+    def get_streams_info(self, vid, profile='shd'):
         for PLAYER_PLATFORM in PLAYER_PLATFORMS.copy():
-            params = {
-                'otype': 'json',
-                'platform': PLAYER_PLATFORM,
-                'vid': self.vid,
-                'defnpayver': 1,
-                'appver': PLAYER_VERSION,
-                'defn': profile,
-            }
-
-            resp = get_response('https://vv.video.qq.com/getinfo',
-                               params=params)
-            data = resp.json()
+            data = get_response('https://vv.video.qq.com/getinfo',
+                                params={
+                                    'otype': 'json',
+                                    'platform': PLAYER_PLATFORM,
+                                    'vid': vid,
+                                    'defnpayver': 1,
+                                    'appver': PLAYER_VERSION,
+                                    'defn': profile,
+                                }).json()
             if 'msg' in data:
-                assert data['msg'] not in ('vid is wrong', 'vid status wrong'), \
-                       'wrong vid'
-                PLAYER_PLATFORMS.remove(PLAYER_PLATFORM)
                 continue
 
-            if PLAYER_PLATFORMS and \
-                    profile == 'shd' and \
-                    '"name":"shd"' not in resp.text and \
-                    '"name":"fhd"' not in resp.text:
-                for infos in self.get_streams_info('hd'):
-                    yield infos
-                return
+            #if PLAYER_PLATFORMS and \
+            #        profile == 'shd' and \
+            #        '"name":"shd"' not in resp.text and \
+            #        '"name":"fhd"' not in resp.text:
+            #    for infos in self.get_streams_info(vid, 'hd'):
+            #        yield infos
+            #    return
+
             break
 
         assert 'msg' not in data, data['msg']
         video = data['vl']['vi'][0]
         fn = video['fn']
         title = video['ti']
         td = float(video['td'])
@@ -104,19 +99,19 @@
             cdn_url = cdn_url_3 or cdn_url_1 or cdn_url_2
         else:
             cdn_url = cdn_url_1 or cdn_url_2 or cdn_url_3
         #cdn_url = cdn_url_1 or cdn_url_2 or cdn_url_3
 
         dt = cdn['dt']
         if dt == 1:
-            type_name = 'flv'
+            ext = 'flv'
         elif dt == 2:
-            type_name = 'mp4'
+            ext = 'mp4'
         else:
-            type_name = fn.split('.')[-1]
+            ext = fn.split('.')[-1]
 
         _num_clips = video['cl']['fc']
         #self.limit = video.get('type', 0) > 1000
         #if self.limit:
         #    if _num_clips > 1:
         #        self.logger.warning('Only parsed first video part!')
         #    for fmt in data['fl']['fi']:
@@ -126,15 +121,15 @@
         #            break
         #    fns = fn.split('.')
         #    fns.insert(-1, '1')
         #    filename = '.'.join(fns)
         #    url = '{}{}?vkey={}'.format(cdn_url, filename, fvkey)
         #    size = video['cl']['ci'][0]['cs'] # not correct, real size is smaller.
         #    rate = size // float(video['cl']['ci'][0]['cd'])
-        #    yield title, fmt_name, fmt_cname, type_name, [url], size, rate
+        #    yield title, fmt_name, fmt_cname, ext, [url], size, rate
         #    return
 
         for fmt in data['fl']['fi']:
             fmt_id = fmt['id']
             fmt_name = fmt['name']
             fmt_cname = fmt['cname']
             size = fmt['fs']
@@ -159,104 +154,116 @@
             elif fns[1][0] in ('p', 'm') and not fns[1].startswith('mp'):
                 del fns[1]
 
             urls =[]
 
             if num_clips == 0:
                 filename = '.'.join(fns)
-                url, vip = qq_get_final_url(cdn_url, self.vid, fmt_id,
+                url, vip = qq_get_final_url(cdn_url, vid, fmt_id,
                                             filename, fvkey, PLAYER_PLATFORM)
                 if vip:
                     self.vip = vip
                 elif url:
                     urls.append(url)
             else:
                 fns.insert(-1, '1')
                 for idx in range(1, num_clips + 1):
                     fns[-2] = str(idx)
                     filename = '.'.join(fns)
-                    url, vip = qq_get_final_url(cdn_url, self.vid, fmt_id,
+                    url, vip = qq_get_final_url(cdn_url, vid, fmt_id,
                                             filename, fvkey, PLAYER_PLATFORM)
                     if vip:
                         self.vip = vip
                         break
                     elif url:
                         urls.append(url)
 
-            yield title, fmt_name, fmt_cname, type_name, urls, size, rate
+            yield title, fmt_name, fmt_cname, ext, urls, size, rate
+
+    def list_only(self):
+        cid, vid = self.mid
+        return cid and not vid
+
+    @staticmethod
+    def format_mid(mid):
+        # [0] cover id, length 15
+        # [1] video id, length 11
+        if not isinstance(mid, tuple):
+            mid = mid, None
+        mid = mid[:2]
+        if len(mid) == 1:
+            mid += (None, )
+        assert any(mid)
+        if mid[0] and len(mid[0]) == 11:
+            mid = mid[::-1]
+        assert not mid[0] or len(mid[0]) == 15
+        assert not mid[1] or len(mid[1]) == 11
+        return mid
+
+    def parse_html(self):
+        html = get_content(self.url)
+        return match1(html, r'\bvid[\"\']?\s*[=:]\s*[\"\']?(\w+)')
+
+    def prepare_mid(self):
+        mid = matchm(self.url, '/x/page/(\w+)\.html',
+                               r'\bvid=(\w+)',
+                               '/x/cover/(\w+)\.html',
+                               '/x/cover/(\w+)/(\w+)\.html',
+                               '/(\w+)/?$')
+        if any(mid):
+            return mid
+        return self.parse_html()
 
     def prepare(self):
         info = MediaInfo(self.name)
-        if not self.vid:
-            self.vid = match1(self.url,
-                              'vid=(\w+)',
-                              '/(\w+)\.html',
-                              '/(\w+)$')
-
-        if self.vid and match1(self.url, '(^https?://film\.qq\.com)'):
-            self.url = 'https://v.qq.com/x/cover/%s.html' % self.vid
-
-        if not self.vid or len(self.vid) != 11:
-            html = get_content(self.url)
-            self.vid = match1(html,
-                              '&vid=(\w+)',
-                              'vid:\s*[\"\'](\w+)',
-                              'vid\s*=\s*[\"\']\s*(\w+)',
-                              '"vid":"(\w+)"')
-
-            if not self.vid and '<body class="page_404">' in html:
-                self.logger.warning('This video has been deleted!')
-                return info
+
+        cid, vid = self.mid
+        if vid is None:
+            if self.url is None:
+                self.url = 'https://v.qq.com/x/cover/{cid}.html'.format(**vars())
+            vid = self.parse_html()
 
         video_rate = {}
-        for _ in range(2):
-            try:
-                for (title, fmt_name, stream_profile, type_name,
-                            urls, size, rate) in self.get_streams_info():
-                    stream_id = self.stream_2_id[fmt_name]
-                    if urls:
-                        info.streams[stream_id] = {
-                            'container': type_name,
-                            'video_profile': stream_profile,
-                            'src' : urls,
-                            'size': size
-                        }
-                        video_rate[stream_id] = rate
-                break
-            except AssertionError as e:
-                if 'wrong vid' in str(e):
-                    html = get_content(self.url)
-                    self.vid = match1(html,
-                                      '&vid=(\w+)',
-                                      'vid:\s*[\"\'](\w+)',
-                                      'vid\s*=\s*[\"\']\s*(\w+)',
-                                      '"vid":"(\w+)"')
-                    continue
-                raise e
+        for (title, fmt_name, stream_profile, ext, urls, size, rate) in self.get_streams_info(vid):
+            if urls:
+                stream_id = self.stream_2_id[fmt_name]
+                info.streams[stream_id] = {
+                    'container': ext,
+                    'profile': stream_profile,
+                    'src' : urls,
+                    'size': size
+                }
+                video_rate[stream_id] = rate
 
         if self.vip:
             self.logger.warning('This is a VIP video!')
             #self.limit = False
 
-        assert info.streams, "can't play this video!!"
-        info.title = title
-
         #if self.limit:
         #    # Downloading some videos is very slow, use multithreading range fetch to speed up.
         #    # Only for video players now.
         #    info.extra['rangefetch'] = {
         #        'first_size': 1024 * 16,
         #        'max_size': 1024 * 32,
         #        'threads': 10,
         #        'video_rate': video_rate
         #    }
         #    self.logger.warning('This is a restricted video!')
 
+        info.title = title
         info.extra.referer = 'https://v.qq.com/'
         return info
 
     def prepare_list(self):
-        html = get_content(self.url)
-        vids = [a.strip('"') for a in match1(html, '\"vid\":\[([^\]]+)').split(',')]
+        cid, vid = self.mid
+        html = get_content('https://v.qq.com/x/cover/{cid}.html'.format(**vars()))
+        vids = match1(html, '"video_ids":(\[.+?\])')
+        if vids:
+            vids = json.loads(vids)
+        else:
+            vids = matchall(html, r'\bdata-vid="(\w+)"') or \
+                   matchall(html, '"vid":"(\w+)"')
+        # FIXME some covers are reversed
+        self.set_index(vid, vids)
         return vids
 
 site = QQ()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/sina/openc.py` & `ykdl-1.8.2/ykdl/extractors/sina/openc.py`

 * *Files 24% similar despite different names*

```diff
@@ -7,42 +7,78 @@
     t = str(int(time.time()) >> 6)
     s = '{vid}Z6prk18aWxP278cVAH{t}{rand}'.format(**vars())
     return hash.md5(s)[:16] + t
 
 class OpenC(Extractor):
     name = 'Sina openCourse (新浪公开课)'
 
+    def format_mid(self, mid):
+        # [0] course id
+        # [1] lesson id
+        if not isinstance(mid, tuple):
+            mid = mid, None
+        mid = mid[:2]
+        if len(mid) == 1:
+            mid += (None, )
+        cid, lid = mid
+        cid = fullmatch(cid, '\d+')
+        lid = fullmatch(lid, '\d+')
+        assert cid
+        return cid, lid
+
+    def prepare_mid(self):
+        mid = matchm(self.url, '/course/id_(\d+)/lesson_(\d+)',
+                               '/course/id_(\d+)')
+        if mid[0]:
+            return mid
+
+    def list_only(self):
+        return not self.mid[1]
+
     def prepare(self):
         info = MediaInfo(self.name)
 
-        if self.url:
-            html = get_content(self.url)
-            self.vid = match1(html, 'playVideo\("(\d+)')
-            info.artist = match1(html, '讲师：(.+?)<br/>')
+        cid, lid = self.mid
+        if lid is None:
+            url = 'https://open.sina.com.cn/course/id_{cid}/'
+        else:
+            url = 'https://open.sina.com.cn/course/id_{cid}/lesson_{lid}/'
+        html = get_content(url.format(**vars()))
+        vid = match1(html, 'playVideo\("(\d+)')
+        info.artist = match1(html, '讲师：(.+?)<br/>')
 
-        self.logger.debug('VID: %s', self.vid)
+        assert vid, "can't find vid!"
 
         rand = str(random.random())[:18]
         data = get_response('http://ask.ivideo.sina.com.cn/v_play.php',
                             params={
-                               'vid': self.vid,
+                               'vid': vid,
                                'ran': rand,
                                'p': 'i',
-                               'k': get_k(self.vid, rand),
+                               'k': get_k(vid, rand),
                             }).xml()['root']
 
         info.title = data['vname']
         urls = []
         size = 0
         for durl in data['durl']:
             urls.append(durl['url'])
             size += durl['filesize']
 
         info.streams['current'] = {
             'container': 'hlv',
-            'video_profile': 'current',
-            'src': urls,
+            'profile': 'current',
+            'src' : urls,
             'size': size
         }
         return info
 
+    def prepare_list(self):
+        cid, lid = self.mid
+        url = 'https://open.sina.com.cn/course/id_{cid}/'
+        html = get_content(url.format(**vars()))
+        lids = [None] + matchall(html, '/lesson_(\d+)/">')
+        self.set_index(lid, lids)
+        for lid in lids:
+            yield cid, lid
+
 site = OpenC()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/sina/video.py` & `ykdl-1.8.2/ykdl/extractors/sina/video.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,52 +1,56 @@
 # -*- coding: utf-8 -*-
 
 from .._common import *
 
 
 def get_realurl(url, vid):
-    resp = get_response(url, params={'vid': vid})
-    if resp.locations:
-        return resp.url
-    else:
-       return matchall(resp, 'CDATA\[([^\]]+)')[1]
+    params = urlencode({'vid': vid})
+    url = '{url}?{params}'.format(**vars())
+    if get_location(url) != url:
+        return url  # redirect url will be expired, keep origin
+    html = get_content(url)
+    print(html)
+    return matchall(html, 'CDATA\[([^\]]+)')[1]
 
 class Sina(Extractor):
     name = '新浪视频 (sina)'
 
+    def prepare_mid(self):
+        mid = match1(self.url, 'video_id=(\d+)', '(\d{5,})\.swf')
+        if mid:
+            return mid
+        html = get_content(self.url)
+        return match1(html, '[vV]ideo_?[iI]d[\'"]?\s*[:=]\s*[\'"]?(\d+)')
+
     def prepare(self):
         info = MediaInfo(self.name)
-        if not self.vid:
-            self.vid = match1(self.url, 'video_id=(\d+)',
-                                        '#(\d{5,})',
-                                        '(\d{5,})\.swf')
-            if not self.vid:
-                html = get_content(self.url)
-                self.vid = match1(html, 'video_id[\'"]?\s*[:=]\s*[\'"]?(\d+)')
-
-        assert self.vid, "can't get vid"
 
-        data = get_response('http://s.video.sina.com.cn/video/h5play',
-                            params={'video_id': self.vid}).json()
+        data = get_response('https://s.video.sina.com.cn/video/h5play',
+                            params={'video_id': self.mid}).json()
+        assert data['code'] == 1, data['message']
         data = data['data']
+
         info.title = data['title']
-        for t in ['mp4', 'flv', '3gp']:
+        info.duration = int(data['length']) // 1000
+
+        for t in ['mp4', 'flv', 'hlv', '3gp']:
             video_info = data['videos'].get(t)
             if video_info:
                 break
 
         for profile in video_info:
             v = video_info[profile]
-            r_url = get_realurl(v['file_api'], v['file_id'])
+            url = get_realurl(v['file_api'], v['file_id'])
             info.streams[profile] = {
                 'container': v['type'],
-                'video_profile': profile,
-                'src': [r_url],
-                'size' : 0
+                'profile': profile,
+                'src': [url]
             }
+
         return info
 
     def prepare_list(self):
         html = get_content(self.url)
         return matchall(html, 'video_id: ([^,]+)')
 
 site = Sina()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/singlemultimedia.py` & `ykdl-1.8.2/ykdl/extractors/singlemultimedia.py`

 * *Files 0% similar despite different names*

```diff
@@ -99,14 +99,14 @@
         info = MediaInfo(self.name)
         info.title = title
         if ext[:3] == 'm3u':
             info.streams = load_m3u8_playlist(self.url)
         else:
             info.streams['current'] = {
                 'container': ext,
-                'video_profile': 'current',
+                'profile': 'current',
                 'src': [self.url],
                 'size': int(self.resinfo.get('Content-Length', 0))
             }
         return info
 
 site = Multimedia()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/sohu/sohubase.py` & `ykdl-1.8.2/ykdl/extractors/sohu/sohubase.py`

 * *Files 16% similar despite different names*

```diff
@@ -35,21 +35,21 @@
         '4K': '4K',
         'BD': '原画',
         'TD': '超清',
         'HD': '高清',
         'SD': '标清'
     }
 
-    def parser_info(self, video, info, stream, lvid, uid):
-        if not 'allot' in info or lvid != info['id']:
+    def parser_info(self, info, data, stream, lvid, uid):
+        if not 'allot' in data or lvid != data['id']:
             return
         stream_id = self.types_2_id[stream]
         stream_profile = self.id_2_profile[stream_id]
-        host = info['allot']
-        data = info['data']
+        host = data['allot']
+        data = data['data']
         size = sum(map(int, data['clipsBytes']))
         urls = []
         assert len(data['clipsURL']) == len(data['clipsBytes']) == len(data['su'])
         for new, ck, in zip(data['su'], data['ck']):
             if urlparse(new).netloc == '':
                 url = get_response('https://{host}/ip'.format(**vars()),
                                    params={
@@ -61,76 +61,71 @@
                                        'prod': 'h5n',
                                        'pt': 1,
                                        'pg': 2,
                                    }).json()['servers'][0]['url']
             else:
                 url = new
             urls.append(url)
-        video.streams[stream_id] = {
+        info.streams[stream_id] = {
             'container': 'mp4',
-            'video_profile': stream_profile,
-            'src': urls,
-            'size' : size
+            'profile': stream_profile,
+            'src' : urls,
+            'size': size
         }
 
     def fetch_info(self, vid):
         self.apiparams['vid'] = vid
         return get_response(self.apiurl, params=self.apiparams).json()
 
-    def prepare(self):
-        if self.url and not self.vid:
-            self.vid = match1(self.url, '\W[b|v]?id=(\d+)',
-                                        'share_play.html#(\d+)_')
-            if not self.vid:
-                html = get_content(self.url)
-                self.vid = match1(html, '/(\d+)/v\.swf',
-                                        'vid="(\d+)"',
-                                        "bid:'(\d+)'",
-                                        '&id=(\d+)')
-
-        info = self.fetch_info(self.vid)
-        if info['status'] == 6:
-            from .my import site
-            self.name = site.name
-            self.apiurl = site.apiurl
-            self.apiparams = site.apiparams
-            info = self.fetch_info(self.vid)
+    def prepare_mid(self):
+        mid = match1(self.url, '\d/(\d+)\.s?html',
+                              r'\b[bv]?id=(\d+)',
+                               'share_play.html#(\d+)_')
+        if mid is None:
+            html = get_content(self.url)
+            mid = match1(html, r'\b[bv]id\s*[=:]\s*["\']?(\d+)',
+                               r'(?:&|\x26)[bv]?id=(\d+)'
+                                '/(\d+)/v\.swf')
+        return mid
 
-        video = MediaInfo(self.name)
+    def prepare(self):
+        info = MediaInfo(self.name)
         # this is needless now, uid well be registered in the the following code
-        #video.extra['header'] = 'Range: '
-        if info['status'] == 1:
-            now = time.time()
-            uid = int(now * 1000)
-            get_response('http://z.m.tv.sohu.com/h5_cc.gif',
-                         params={
-                             'vid': self.vid,
-                             'url': self.url,
-                             'refer': self.url,
-                             't': int(now),
-                             'uid': uid,
-                             #'nid': nid,
-                             #'pid': pid,
-                             #'screen': '1366x768',
-                             #'channeled': channeled,
-                             #'MTV_SRC': MTV_SRC,
-                             #'position': 'page_adbanner',
-                             #'op': 'click',
-                             #'details': '{}',
-                             #'os': 'linux',
-                             #'platform': 'linux',
-                             #'passport': '',
-                         })
-
-            data = info['data']
-            video.title = data['tvName']
-            for stream in self.supported_stream_types:
-                lvid = data.get(stream)
-                if lvid == 0 or not lvid:
-                    continue
-                if lvid != self.vid:
-                    _info = self.fetch_info(lvid)
-                else:
-                    _info = info
+        #info.extra['header'] = 'Range: '
+
+        data = self.fetch_info(self.mid)
+        assert data['status'] == 1, data
+
+        # report
+        now = time.time()
+        uid = int(now * 1000)
+        get_response('http://z.m.tv.sohu.com/h5_cc.gif',
+                     params={
+                         'vid': self.mid,
+                         'url': self.url,
+                         'refer': self.url,
+                         't': int(now),
+                         'uid': uid,
+                         #'nid': nid,
+                         #'pid': pid,
+                         #'screen': '1366x768',
+                         #'channeled': channeled,
+                         #'MTV_SRC': MTV_SRC,
+                         #'position': 'page_adbanner',
+                         #'op': 'click',
+                         #'details': '{}',
+                         #'os': 'linux',
+                         #'platform': 'linux',
+                         #'passport': '',
+                     })
+
+        _data = data['data']
+        info.title = _data['tvName']
+        for stream in self.supported_stream_types:
+            lvid = _data.get(stream)
+            if lvid == 0 or not lvid:
+                continue
+            if lvid != self.mid:
+                data = self.fetch_info(lvid)
+            self.parser_info(info, data, stream, lvid, uid)
 
-                self.parser_info(video, _info, stream, lvid, uid)
-        return video
+        return info
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/weibo.py` & `ykdl-1.8.2/ykdl/extractors/weibo.py`

 * *Files 26% similar despite different names*

```diff
@@ -11,87 +11,104 @@
            '2': '2K',
         '1080': 'BD',
          '720': 'TD',
          '480': 'HD',
          '360': 'SD'
     }
 
+    def prepare_mid(self):
+        patterns = '(?:object|f)_?id"?\s*[=:]\s*"?(\d{4}:(?:\d{16}|\w{32}))\W', \
+                   'media_id=(\d{16}|\w{32})'
+        mid = match1(self.url, '\D(\d{4}:(?:\d{16}|\w{32}))(?:\W|$)',
+                               *patterns)
+        if mid:
+            return mid
+
+        rurl = get_location(self.url)
+        page = match1(rurl, 'https?://[^/]+(/\d+/\w+)')
+        if page is None or match1(page, '/(\d+)$'):
+            html = get_content(rurl.replace('//weibo.', '//hk.weibo.')
+                                   .replace('/user/', '/'))
+            mid = match1(html, *patterns)
+            if mid:
+                return mid
+            page = match1(html, '"og:url".+weibo.com(/\d+/\w+)')
+
+        assert page, 'can not find any video!!!'
+        self.url = 'https://weibo.com' + page
+
+        html = get_content(self.url)
+        return match1(html, *patterns)
+
     def prepare(self):
         if 'passport.weibo' in self.url:
             url = parse_qs(self.url.split('?', 1)[-1]).get('url')
             assert url, 'lost the url param in a link of "passport.weibo"'
             self.url = url[0]
 
         info = MediaInfo(self.name)
-
         add_header('User-Agent', 'Baiduspider')
 
-        self.vid = match1(self.url, '\D(\d{4}:(?:\d{16}|\w{32}))(?:\W|$)',
-                                    'media_id=(\d{16})')
+        if '.weibocdn.com' not in self.url:
+            rurl = get_location(self.url)
+            assert '/sorry?' not in rurl, 'can not find any video!!!'
 
-        def append_stream(video_profile, video_quality, url):
-            stream_id = self.quality_2_id[video_quality]
+        def append_stream(stream_profile, stream_quality, url):
+            stream_id = self.quality_2_id[stream_quality]
             info.streams[stream_id] = {
-                'video_profile': video_profile,
                 'container': 'mp4',
-                'src' : [url]
+                'profile': stream_profile,
+                'src': [url]
             }
 
-        if self.vid is None:
-            rurl = get_location(self.url)
-            assert '/sorry?' not in rurl, 'can not find any video!!!'
-            page = match1(rurl, 'https?://[^/]+(/\d+/\w+)')
-            if page is None or match1(page, '/(\d+)$'):
-                html = get_content(rurl.replace('//weibo.', '//hk.weibo.')
-                                       .replace('/user/', '/'))
-                page = match1(html, '"og:url".+weibo.com(/\d+/\w+)')
-            assert page, 'can not find any video!!!'
-            html = get_content('https://weibo.com' + page)
+        try:
+            self.mid
+        except AssertionError:
+            html = get_content(self.url)
             streams = match1(html, 'quality_label_list=([^"]+)').split('&')[0]
             if streams:
                 streams = json.loads(unquote(streams))
                 for stream in streams:
-                    video_quality = stream['quality_label'].upper()
-                    video_profile = stream['quality_desc'] + ' ' + video_quality
-                    video_quality = match1(video_quality, '(\d+)')
-                    append_stream(video_profile, video_quality, stream['url'])
+                    stream_quality = stream['quality_label'].upper()
+                    stream_profile = stream['quality_desc'] + ' ' + stream_quality
+                    stream_quality = match1(stream_quality, '(\d+)')
+                    append_stream(stream_profile, stream_quality, stream['url'])
             else:
                 url = match1(html, 'action-data="[^"]+?&video_src=([^"&]+)')
                 if url:
                     info.streams['current'] = {
-                        'video_profile': 'current',
                         'container': 'mp4',
-                        'src' : [unquote(url)]
+                        'profile': 'current',
+                        'src': [unquote(url)]
                     }
             if info.streams:
                 info.title = match1(html, '<meta content="([^"]+)" name="description"').split('\n')[0]
                 info.artist = match1(html, '<meta content="([^"]+)" name="keywords"').split(',')[0]
                 i = info.title.find('】') + 1
                 if i:
                     info.title = info.title[:i]
-            else:
-                self.vid = match1(html, 'objectid=(\d{4}:(?:\d{16}|\w{32}))\W')
-                assert self.vid, 'can not find any video!!!'
-
-        if self.vid:
-            if ':' not in self.vid:
-                self.vid = '1034:' + self.vid  # oid, the prefix is not necessary and would not be checked
-            vdata = get_response('https://weibo.com/tv/api/component',
-                        headers={
-                            'Referer': 'https://weibo.com/tv/show/' + self.vid
-                        },
-                        data={
-                            'data': json.dumps({
-                                'Component_Play_Playinfo': {'oid': self.vid}
-                            })
-                        }).json()['data']['Component_Play_Playinfo']
-
-            info.title = vdata['title']
-            info.artist = vdata['author']
-            for video_profile, url in vdata['urls'].items():
-                if url:
-                    video_quality = match1(video_profile, '(\d+)')
-                    append_stream(video_profile, video_quality, 'https:' + url)
+                return info
 
+        if ':' not in self.mid:
+            self.mid = '1034:' + self.mid  # oid, the prefix is not necessary and would not be checked
+        vdata = get_response('https://weibo.com/tv/api/component',
+                    headers={
+                        'Referer': 'https://weibo.com/tv/show/' + self.mid
+                    },
+                    data={
+                        'data': json.dumps({
+                            'Component_Play_Playinfo': {'oid': self.mid}
+                        })
+                    }).json()['data']['Component_Play_Playinfo']
+
+        for stream_profile, url in vdata['urls'].items():
+            if url:
+                stream_quality = match1(stream_profile, '(\d+)')
+                append_stream(stream_profile, stream_quality, 'https:' + url)
+
+        info.title = vdata['title']
+        info.artist = vdata['author']
+        info.duration = vdata['duration']
+        info.add_comment(vdata['text'])
         return info
 
 site = Weibo()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/yinyuetai.py` & `ykdl-1.8.2/ykdl/extractors/yizhibo.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,31 +1,32 @@
 # -*- coding: utf-8 -*-
 
 from ._common import *
 
 
-class YinYueTai(Extractor):
-    name = '音悦台 (YinYueTai)'
+class Yizhibo(Extractor):
+    name = 'Yizhibo (一直播)'
+
+    def prepare_mid(self):
+        return self.url[self.url.rfind('/')+1:].split('.')[0]
 
     def prepare(self):
         info = MediaInfo(self.name)
-        info.extra.referer = 'https://www.yinyuetai.com/'
-        if not self.vid:
-            self.vid = match1(self.url,'\Wid=(\d+)')
-
-        data = get_response('https://data.yinyuetai.com/video/getVideoInfo',
-                            params={'id': self.vid}).json()
-        assert not data['delFlag'], 'MTV has been deleted!'
+        info.live = True
 
-        info.title = data['videoName']
-        info.artist = data['artistName']
+        data = get_response(
+                    'http://www.yizhibo.com/live/h5api/get_basic_live_info',
+                    params={'scid': self.mid}).json()
+        assert content['result'] == 1, 'Error : ' + data['result']
+        data = data['data']
 
-        url = data['videoUrl']
+        info.title = data['live_title']
+        info.artist = data['nickname']
         info.streams['current'] = {
-            'container': url_info(url)[1],
-            'video_profile': 'current',
-            'src' : [url]
+            'container': 'm3u8',
+            'profile': 'current',
+            'src' : [data['play_url']],
+            'size': Infinity
         }
-
         return info
 
-site = YinYueTai()
+site = Yizhibo()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/youku.py` & `ykdl-1.8.2/ykdl/extractors/youku.py`

 * *Files 5% similar despite different names*

```diff
@@ -35,49 +35,44 @@
     ckey_mobile = '7B19C0AB12633B22E7FE81271162026020570708D6CC189E4924503C49D243A0DE6CD84A766832C2C99898FC5ED31F3709BB3CDD82C96492E721BDD381735026'
     params = (
         ('0532', ref_youku, ckey_default),
         ('0590', ref_youku, ckey_default),
         ('0505', ref_tudou, ckey_default),
         )
 
-    def prepare(self):
-        info = MediaInfo(self.name)
-
-        if not self.vid:
-             self.vid = match1(self.url.split('//', 1)[1],
-                               '^v[^\.]?\.[^/]+/v_show/id_([a-zA-Z0-9=]+)',
-                               '^player[^/]+/(?:player\.php/sid|embed)/([a-zA-Z0-9=]+)',
-                               '^static.+loader\.swf\?VideoIDS=([a-zA-Z0-9=]+)',
-                               '^(?:new-play|video)\.tudou\.com/v/([a-zA-Z0-9=]+)')
-
-        if not self.vid:
+    def prepare_mid(self):
+        mid = match1(self.url.split('//', 1)[1],
+                    '^v[^\.]?\.[^/]+/v_show/id_([a-zA-Z0-9=]+)',
+                    '^player[^/]+/(?:player\.php/sid|embed)/([a-zA-Z0-9=]+)',
+                    '^static.+loader\.swf\?VideoIDS=([a-zA-Z0-9=]+)',
+                    '^(?:new-play|video)\.tudou\.com/v/([a-zA-Z0-9=]+)')
+        if mid is None:
             html = get_content(self.url)
-            self.vid = match1(html, '''videoIds?["']?\s*[:=]\s*["']?([a-zA-Z0-9=]+)''')
+            mid = match1(html, '''videoIds?["']?\s*[:=]\s*["']?([a-zA-Z0-9=]+)''')
+        elif mid.isdigit():
+            mid = 'X' + b64('%d' % (int(mid) * 4))
+        return mid
 
-        if self.vid.isdigit():
-            vid = base64.b64encode(b'%d' % (int(self.vid) * 4))
-            if not isinstance(vid, str):
-                vid = vid.decode()
-            self.vid = 'X' + vid
-        self.logger.debug('VID: ' + self.vid)
+    def prepare(self):
+        info = MediaInfo(self.name)
 
         install_cookie()
         get_response('https://gm.mmstat.com/yt/ykcomment.play.commentInit?cna=',
                      {'Cookie': '__ysuid=%d' % time.time()})
         utid = get_cookie('.mmstat.com', '/', 'cna').value
         uninstall_cookie()
 
         for ccode, ref, ckey in self.params:
             add_header('Referer', ref)
             if len(ccode) > 4:
                _utid = generateUtdid()
             else:
                _utid = utid
             params = {
-                'vid': self.vid,
+                'vid': self.mid,
                 'ccode': ccode,
                 'utid': _utid,
                 'ckey': ckey,
                 'client_ip': '192.168.1.1',
                 'client_ts': int(time.time()),
             }
             data = None
@@ -113,43 +108,44 @@
             # 未提供相关信息，如 https://v.youku.com/v_show/id_XOTI0MTE2NDg4.html
             stage = ''
         info.title = '{} {}'.format(stage, data['video']['title']).lstrip()
 
         audio_lang = 'default'
         if 'dvd' in data and 'audiolang' in data['dvd']:
             for l in data['dvd']['audiolang']:
-                if l['vid'].startswith(self.vid):
+                if l['vid'].startswith(self.mid):
                     audio_lang = l['langcode']
                     break
 
         streams = data['stream']
         for s in streams:
             if not audio_lang == s['audio_lang']:
                 continue
             self.logger.debug('stream> ' + str(s))
-            t = stream_code_to_id[s['stream_type']]
+            stream_id = stream_code_to_id[s['stream_type']]
+            stream_profile = stream_code_to_profiles[stream_id]
             urls = []
             for u in s['segs']:
                 self.logger.debug('seg> ' + str(u))
                 if u['key'] != -1:
                     if 'cdn_url' in u:
                         urls.append(u['cdn_url'])
                 else:
                     self.logger.warning('VIP video, ignore unavailable seg: {}'
                                         .format(s['segs'].index(u)))
             if len(urls) == 0:
                 urls = [s['m3u8_url']]
                 c = 'm3u8'
             else:
-                c = id_to_container[t]
+                c = id_to_container[stream_id]
             size = s['size']
-            info.streams[t] =  {
+            info.streams[stream_id] =  {
                     'container': c,
-                    'video_profile': stream_code_to_profiles[t],
-                    'size': size,
-                    'src' : urls
+                    'profile': stream_profile,
+                    'src' : urls,
+                    'size': size
                 }
 
         return info
 
 
 site = Youku()
```

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/youkujs.py` & `ykdl-1.8.2/ykdl/extractors/youkujs.py`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/zhangyu.py` & `ykdl-1.8.2/ykdl/extractors/zhangyu.py`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/extractors/zhanqi.py` & `ykdl-1.8.2/ykdl/extractors/zhanqi.py`

 * *Files 6% similar despite different names*

```diff
@@ -54,14 +54,13 @@
                     'ipFrom': 1,
                     'clientIp': '',
                     'fhost': 'h5',
                     'platform': 128
                 }))
         info.streams['current'] = {
             'container': 'flv',
-            'video_profile': 'current',
-            'src' : [url],
-            'size': 0
+            'profile': 'current',
+            'src': [url]
         }
         return info
 
 site = Zhanqi()
```

### Comparing `ykdl-1.8.1.post1/ykdl/mediainfo.py` & `ykdl-1.8.2/ykdl/mediainfo.py`

 * *Files 4% similar despite different names*

```diff
@@ -7,16 +7,15 @@
 from html import unescape
 from urllib.parse import unquote
 
 from .util import log
 from .util.fs import legitimize, compress_strip
 from .util.http import fake_headers
 from .util.human import human_size, _format_time, human_time, stream_index
-from .util.match import match, match1
-from .util.wrap import get_random_str
+from .util.wrap import get_random_str, hash
 
 logger = logging.getLogger(__name__)
 
 
 class MediaInfo:
     def __init__(self, site, live=False):
         self.site = site
@@ -30,15 +29,15 @@
         self._comments = []
         self.streams = MediaStreams()
         self.subtitles = []
         self.extra = ExtraDict()
 
     @property
     def title(self):
-        return self._title
+        return self._title or '_'.join([self.site, hash.crc32(self.orig_url)])
 
     @title.setter
     def title(self, value):
         if value:
             self._title = compress_strip(unquote(unescape(value)))
 
     @property
@@ -79,34 +78,33 @@
             value = unquote(unescape(value))
             self._comments.append(value)
 
     def print_stream_info(self, stream_id, show_full=False):
         stream = self.streams[stream_id]
         fmt, id = self.streams._split_id(stream_id)
         stream_fmt = id and self.streams[fmt] is stream and fmt
-        size = stream.get('size', 0) not in (0, float('inf')) and stream['size']
+        size = stream.get('size', 0) not in (0, Infinity) and stream['size']
         self.lprint(
         ['    - format:         {}', (stream_fmt and
                                       log.sprint(stream_fmt, log.NEGATIVE) + ' '
                                       or '')
                                    + log.sprint(stream_id, log.NEGATIVE)],
         ['      container:      {}', stream.get('container')],
-        ['      video-profile:  {}', stream.get('video_profile')],
-        ['      quality:        {}', stream.get('quality')],
+        ['      profile:        {}', stream.get('profile')],
         ['      size:           {} ({:d} Bytes)', size and human_size(size), size],
         ['    # download-with:  {}', stream_id != 'current' and
                 log.sprint('ykdl --format=%s [URL]' % stream_id, log.UNDERLINE)])
         if show_full:
             print('Real urls:')
             for url in stream['src']:
                 print(url)
         print('')
 
     def print_subtitle_info(self, subtitle, show_full=False):
-        size = subtitle.get('size', 0) not in (0, float('inf')) and subtitle['size']
+        size = subtitle.get('size', 0) not in (0, Infinity) and subtitle['size']
         self.lprint(
         ['    - language:       {}', log.sprint(subtitle['lang'], log.NEGATIVE)],
         ['      name:           {}', subtitle['name']],
         ['      format:         {}', subtitle['format']],
         ['      size:           {} ({:d} Bytes)', size and human_size(size), size])
         if show_full:
             print('Real url:')
@@ -122,21 +120,22 @@
             'duration'      : self.duration,
             'comments'      : self.comments,
             'streams'       : dict(self.streams.items()),
             'subtitles'     : self.subtitles,
             'extra'         : self.extra,
         }
         for s in json_dict['streams']:
-            if json_dict['streams'][s].get('size') == float('inf'):
+            if json_dict['streams'][s].get('size') == Infinity:
                 json_dict['streams'][s].pop('size')
         return json_dict
 
     def print_info(self, stream_id=None, show_all=False, show_full=False):
         self.lprint(
         ['site:                 {}', self.site],
+        ['index:                {}', self.index and '{} / {}'.format(*self.index)],
         ['title:                {}', self.title],
         ['album:                {}', self.album],
         ['artist:               {}', self.artist],
         ['duration:             {}', self.duration and human_time(self.duration)],
         ['comments:             {}', self.comments],
         ['streams:', 1])
         if show_all:
@@ -147,32 +146,27 @@
             self.print_stream_info(stream_id, show_full)
         if self.subtitles:
             print('subtitles:')
             for subtitle in self.subtitles:
                 self.print_subtitle_info(subtitle, show_full)
 
     def build_file_name(self, stream_id):
-        unique_title = []
-        if self.title:
-            unique_title.append(self.title)
-            if self.album and self.album not in self.title:
-                unique_title.append(self.album)
-            if self.artist and self.artist not in self.title:
-                unique_title.append(self.artist)
-        else:
-            unique_title += [self.site, get_random_str(8)]
-        unique_title = [*legitimize('_'.join(unique_title))]
-        if not unique_title[-1]:
-            unique_title.pop()
+        title = self.title
+        unique_title = [title]
+        if self.album and self.album not in title:
+            unique_title.append(self.album)
+        if self.artist and self.artist not in title:
+            unique_title.append(self.artist)
+        unique_title = [legitimize('_'.join(unique_title))]
         if not stream_id == 'current':
             unique_title.append(stream_id)
         if self.live:
             unique_title.append(legitimize(
                     datetime.now().isoformat().split('.')[0]
-                    )[0])
+                    ))
         return '_'.join(unique_title)
 
     @staticmethod
     def lprint(*ll):
         for l, *v in ll:
             if v[0]:
                 print(l.format(*v))
@@ -260,14 +254,16 @@
 
     def set(self, name, value):
         fmt, id = self._split_id(name)
         if not id:
             id = str(self._formats[fmt])
         if (fmt, id) in self._streams:
             raise KeyError(name)
+        value.setdefault('video_profile', value['profile'])
+        value.setdefault('size', 0)
         self._streamids.append((stream_index(fmt), fmt, id))
         self._streams[(fmt, id)] = value
         self._formats[fmt] += 1
         self._sorted = False
 
     def check_index(self):
         if not self._sorted:
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/download.py` & `ykdl-1.8.2/ykdl/util/download.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,18 +15,20 @@
       5. download end        (['end']) => (downloaded, filessize, totalsize, costtime)
 '''
 
 import os
 import sys
 import time
 import socket
+import string
 import threading
 from logging import getLogger
 from shutil import get_terminal_size
 from concurrent.futures import ThreadPoolExecutor
+from urllib.parse import quote
 from urllib.request import Request, urlopen
 from http.client import IncompleteRead
 
 from .http import hit_conn_cache, clear_conn_cache, fake_headers
 from .human import *
 from .log import IS_ANSI_TERMINAL
 
@@ -206,14 +208,15 @@
     size = -1
     filesize = 0
     downloaded = 0
     open_mode = 'wb'
     response = None
     timeout_q = min(socket.getdefaulttimeout() or 30, 30)
     timeout_r = max(socket.getdefaulttimeout() or 0, 60)
+    url = quote(url, safe=string.punctuation)
     req = Request(url, headers=fake_headers)
     req.remove_header('Accept-encoding')
     try:
         reporthook(['part'], part=part)
         if os.path.exists(name):
             filesize = os.path.getsize(name)
             if filesize:
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/external.py` & `ykdl-1.8.2/ykdl/util/external.py`

 * *Files 0% similar despite different names*

```diff
@@ -157,15 +157,15 @@
                 '-y', '-hide_banner',
                 '-i', '-',
                 '-c', 'copy',
                 outputfile ]
         pipe_input = subprocess.Popen(cmd, stdin=subprocess.PIPE).stdin
 
         # use pipe pass data does not need to wait subprocess
-        bufsize = 1024 * 64
+        bufsize = 1024 * 1024 * 4
         for i in range(lenth):
             inputfile = '%s_%d.%s' % (basename, i, ext)
             with open(inputfile, 'rb') as fp:
                 data = fp.read(bufsize)
                 while data:
                     pipe_input.write(data)
                     data = fp.read(bufsize)
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/fs.py` & `ykdl-1.8.2/ykdl/util/fs.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # -*- coding: utf-8 -*-
 
 import sys
-import zlib
 import platform
+from .wrap import hash
 
 
 if sys.platform.startswith(('msys', 'cygwin')):
     system = 'Windows'
 else:
     system = platform.system()
 
@@ -73,18 +73,20 @@
     '''
     _ensure_translate_table()
     text = text.translate(translate_table)
     text = compress_strip(text, compress, strip, True)
 
     assert text, 'the given filename could not be legalized!'
 
-    crc = zlib.crc32(text[trim:].encode())
-    if crc:
-        crc = '{crc:x}'.format(**vars())
-    return text[:trim], crc
+    result = text[:trim]
+    overflow = text[trim:]
+    if overflow:
+        crc = hash.crc32(overflow)
+        result += '_{crc}'.format(**vars())
+    return result
 
 def compress_strip(text, compress='', strip='', translated=False):
     '''Compress same characters, and then strip.
     Dot, Minus, Underline and whole characters of Unicode Category Separator
     will always be compressed and stripped.
     '''
     if not translated:
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/http.py` & `ykdl-1.8.2/ykdl/util/http.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 import socket
 import functools
 from io import BytesIO
 from types import NoneType
 from logging import getLogger
 from collections import defaultdict
 from http.client import HTTPResponse as _HTTPResponse
-from urllib.parse import parse_qs, urlencode
+from urllib.parse import parse_qs, urlencode, urlsplit
 from urllib.request import Request as _Request, install_opener, build_opener, \
                            AbstractHTTPHandler, HTTPCookieProcessor, \
                            HTTPRedirectHandler as _HTTPRedirectHandler, \
                            URLError, HTTPError
 try:
     from queue import SimpleQueue as Queue, Empty  # py37 and above
 except ImportError:
@@ -25,15 +25,15 @@
     try:
         import brotlicffi as brotli
     except ImportError:
         import brotli
 except ImportError:
     brotli =None
 
-from .match import match1
+from .match import match, match1
 from .xml2dict import xml2dict
 
 logger = getLogger(__name__)
 
 
 # Add HTTP persistent connections feature into urllib.request
 
@@ -178,15 +178,15 @@
 
         method = req.get_method()
         if method not in self.rmethod:
             raise HTTPError(req.full_url, code, msg, headers, fp)
 
         data = req.data  # is used by fixedly method redirections
         newheaders = {k.lower(): v for k, v in req.headers.items()}
-        if code in self.rmethod:
+        if code in self.amcodes:
             for header in ('content-length', 'content-type', 'transfer-encoding'):
                 newheaders.pop(header, None)
             data = None
             if method != 'HEAD':
                 method = 'GET'
 
         # Useless in our modules, memo for somebody may needs
@@ -237,15 +237,15 @@
 # Custom HTTP response
 
 class HTTPResponse:
     def __init__(self, request, response, encoding=None, *, finish=True):
         '''Wrap urllib.request.Request and http.client.HTTPResponse.
 
         Params:
-            `encoding` is used by decode responsed content.
+            `encoding`, a string/callable object used for decode responsed content.
 
             `finish`, only has effect on redirections.
 
                 `True` (default)
                     is used by last response which return from opener.
                 `False` (explicit)
                     is used by redirections which call from our handler.
@@ -331,14 +331,17 @@
                     else:
                         self._text = self.content.decode(encoding, errors='replace')
                 except:
                     logger.debug('Try decode with encoding %r fail', encoding)
                 else:
                     self._encoding = encoding
                     return True
+            if callable(encoding):
+                self._text = encoding(self.content)
+                return True
         decode(self._encoding) or \
         decode(self.headers.get_content_charset()) or \
         'json' in self.headers.get_content_subtype().lower() and \
         decode('utf-8') or \
         decode(match1(self.content[:1024],
                       b'(?i)<meta[^>]+charset=["\']?([\w-]+)',
                       b'(?i)<\\?xml[^>]+encoding=["\']?([\w-]+)')) or \
@@ -371,15 +374,15 @@
 
 # utils
 # TODO: implement session
 
 __all__ = ['add_default_handler', 'install_default_handlers', 'install_cookie',
            'uninstall_cookie', 'get_cookie', 'get_cookies', 'fake_headers',
            'reset_headers', 'add_header', 'get_response', 'get_head_response',
-           'get_location', 'get_content', 'url_info', 'CACHED']
+           'get_location', 'get_content', 'url_info', 'cache_clear', 'CACHED']
 
 _opener = None
 _cookiejar = None
 _default_handlers = []
 
 class Bool:
     def __init__(self, o):
@@ -399,15 +402,18 @@
     try:
         response = HTTPResponse(req, _opener.open(req), encoding)
     finally:
         for r in req.responses:
             del r.request.responses  # clear circular reference
     return response
 
-_opener_open_cached = functools.lru_cache(maxsize=None)(_opener_open)
+_opener_open_cached = functools.cache(_opener_open)
+
+def cache_clear():
+    _opener_open_cached.cache_clear()
 
 def add_default_handler(handler):
     '''Added handlers will be used via install_default_handlers().
 
     Notice:
         this is use to setting GLOBAL (urllib) HTTP proxy and HTTPS verify,
         use it carefully.
@@ -443,15 +449,15 @@
 
 def install_default_handlers():
     '''Install the default handlers to urllib.request as its opener.'''
     global _opener
     # Always use our custom HTTPRedirectHandler
     _opener = build_opener(HTTPRedirectHandler, *_default_handlers)
     install_opener(_opener)
-    _opener_open_cached.cache_clear()
+    cache_clear()
 
 def install_cookie():
     '''Install HTTPCookieProcessor to default opener.'''
     if _cookiejar is None:
         add_default_handler(HTTPCookieProcessor)
         install_default_handlers()
 
@@ -527,36 +533,38 @@
         except EOFError:
             logger.info(' Ignoring a bad checksum of gzip.')
 
 def ungzip(data):
     '''Decompresses data for Content-Encoding: gzip.'''
     return GzipReader(BytesIO(data)).read()
 
-def undeflate(data):
+def inflate(data):
     '''Decompresses data for Content-Encoding: deflate.'''
     decompressor = zlib.decompressobj(-zlib.MAX_WBITS)
     return decompressor.decompress(data) + decompressor.flush()
 
 def unbrotli(data):
     '''Decompresses data for Content-Encoding: br.'''
     return brotli.decompress(data)
 
 decompressors = {
     'gzip': ungzip,
-    'deflate': undeflate
+    'deflate': inflate
 }
 if brotli:
     decompressors['br'] = unbrotli
 
 def get_response(url, headers={}, data=None, params=None, method='GET',
                       max_redirections=None, encoding=None,
                       default_headers=fake_headers, cache=CACHED):
     '''Fetch the response of giving URL.
 
-    Params: both `params` and `data` always use "UTF-8" as encoding.
+    Params:
+        both `params` and `data` always use "UTF-8" as encoding.
+        `encoding` can be a callable object used for decode content
 
     Returns response, when redirections > max_redirections > 0 (stop on limit),
     it is a fake response except the attribute `url`.
     '''
     url = url.split('#', 1)[0]  # remove fragment if exist, it's useless
     if params: 
         url, _, query = url.partition('?')
@@ -581,14 +589,16 @@
         method = 'GET'
     elif method != 'HEAD':
         logger.debug('get_response> URL: %s', url)
     if data and method == 'GET':
         method = 'POST'
     req = Request(url, headers=default_headers, method=method)
     for k, v in headers.items():
+        if k.lower() == 'cookie' and isinstance(v, dict):
+            v = ';'.join('='.join(c) for c in v.items())
         req.add_header(k, v)
     if data:
         form = False
         if isinstance(data, str):
             data = data.encode()
         if not hasattr(data, 'read'):
             try:
@@ -622,32 +632,38 @@
         response = _opener_open_cached(req, encoding)
         if _opener_open_cached.cache_info().hits - hits:
             logger.debug('get_response> hit cache URL: %s', url)
         return response
     else:
         return _opener_open(req, encoding)
 
+def _check_hostname_badhead(url, set=set('''
+    ask.ivideo.sina.com.cn
+    aweme.snssdk.com
+    t.cn
+    '''.split())):
+    return urlsplit(url).hostname.lower() in set
+
 def get_head_response(url, headers={}, params=None, max_redirections=0,
                       default_headers=fake_headers):
     '''Fetch the response of giving URL in HEAD mode.
 
     Returns response, when redirections > max_redirections > 0 (stop on limit),
     it is a fake response except the attribute `url`.
     '''
     logger.debug('get_head_response> URL: ' + url)
-    # Bad HEAD response: t.cn
-    method = '//t.cn/' in url and 'HEADGET' or 'HEAD'
+    method = _check_hostname_badhead(url) and 'HEADGET' or 'HEAD'
     try:
         response = get_response(url, headers=headers, params=params,
                                 method=method,
                                 max_redirections=max_redirections,
                                 default_headers=default_headers)
     except IOError as e:
         # Maybe HEAD method is not supported, retry
-        if method != 'HEADGET' and match1(str(e), 'HTTP Error (40[345]|520)'):
+        if method != 'HEADGET' and match(str(e), 'HTTP Error (40[345]|520)'):
             logger.debug('get_head_response> HEAD failed, try GET')
             response = get_response(url, headers=headers, params=params,
                                     method='HEADGET',
                                     max_redirections=max_redirections,
                                     default_headers=default_headers)
         else:
             raise
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/human.py` & `ykdl-1.8.2/ykdl/util/human.py`

 * *Files 3% similar despite different names*

```diff
@@ -74,14 +74,18 @@
             if unit != 'TiB' and n >= 1024:
                 n /= 1024
             else:
                 break
     return ' '.join(['{:.3f}'.format(n).rstrip('0').rstrip('.'), unit])
 
 def _format_time(s):
+    try:
+        return int(_format_str(s))
+    except ValueError:
+        pass
     s = match1(s, '''(?x)
                   (?:^|[^:\.\d])
                   (
                       (?:
                           (?:\d{1,3}:)?  # on limits 1K
                           [0-5]?\d:
                           |
@@ -95,18 +99,15 @@
                   (?:$|[^:\.\d])
                   ''')
     if s:
         t = 0
         for i, n in enumerate(reversed(s.split(':'))):
             t += int(n) * 60 ** i
         return t
-    try:
-        return int(_format_str(s))
-    except ValueError:
-        return -1
+    return -1
 
 def human_time(t, days=False):
     '''Convert giving number to a hunman read timestamp.
 
     Params:
         `days`, wethere to show days or not.
     '''
@@ -128,40 +129,42 @@
 def format_vps(*wh):
     '''Convert giving width/height to stream Format and progressive scan marking.
 
     e.g.
         1920, 1080      => 'BD', '1080P'
         '720x540'       => 'HD', '540P'
         '540', '960'    => 'HD', '540P'
+        '540P'          => 'HD', '540P'
     '''
     if len(wh) == 1 and isinstance(wh[0], str):
         wh = wh[0].lower().split('x')
-    assert len(wh) == 2, 'need width and height.'
+    assert str(wh[0])[-1:].upper() == 'P' or len(wh) == 2, 'need width and height.'
     def get_n(n):
         try:
             return int(n)
         except ValueError:
             return int(n[:-1])
     wh = list(map(get_n, wh))
     max_ps, min_ps = max(wh), min(wh)
-    ps = abs(max_ps / min_ps * 3 - 4) < 0.5 and max_ps * 4 / 3 or max_ps
-    if ps <= 480:
+    if len(wh) == 1 or not 2.4 > max_ps / min_ps > 1.5:
+        max_ps = min_ps * 16 / 9
+    if max_ps <= 480:
         fmt = 'LD'
-    elif ps <= 640:
+    elif max_ps <= 640:
         fmt = 'SD'
-    elif ps <= 960:
+    elif max_ps <= 960:
         fmt = 'HD'
-    elif ps <= 1280:
+    elif max_ps <= 1280:
         fmt = 'TD'
-    elif ps <= 1920:
+    elif max_ps <= 1920:
         fmt = 'BD'
-    elif ps <= 2560:
+    elif max_ps <= 2560:
         fmt = '2K'
     else:
-        fmt = '{:.1f}'.format(ps/1000).rstrip('0').rstrip('.') + 'K'
+        fmt = '{:.1f}'.format(max_ps/1000).rstrip('0').rstrip('.') + 'K'
     return fmt, str(min_ps) + 'P'
 
 _stream_index = 'OG', '*K', 'BD', 'TD', 'HD', 'SD', 'LD'
 
 def stream_index(fmt):
     '''Used by ..mediainfo.MediaStreams.'''
     if fmt.isdecimal():
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/log.py` & `ykdl-1.8.2/ykdl/util/log.py`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl/util/m3u8.py` & `ykdl-1.8.2/ykdl/util/m3u8.py`

 * *Files 4% similar despite different names*

```diff
@@ -18,15 +18,15 @@
 def load_live_m3u8(url):
     live_error()
 
 def live_m3u8_lenth():
     live_error()
 
 import m3u8
-from m3u8.parser import urljoin
+from urllib.parse import urljoin
 
 class HTTPClient():
     hkwargs = {}
     def download(self, uri, timeout=None, headers={}, *args, **kwargs):
         # live is disabled, results can be cached safely
         response = get_response(uri, headers, cache=True, **self.hkwargs)
         return response.text, urljoin(response.url, '.')
@@ -58,31 +58,33 @@
         m = _load(ll[0].absolute_uri, **kwargs)
     return not (m.is_endlist or m.playlist_type == 'VOD')
 
 def crypto_m3u8(url, **kwargs):
     '''Params: as same as _load().'''
     m = _load(url, **kwargs)
     for k in m.keys:
-        assert not (k and k.uri.startswith('skd:')), 'Unsupported FairPlay Streaming'
+        try:
+            assert not k.uri.startswith('skd:'), 'Unsupported FairPlay Streaming'
+        except AttributeError:
+            pass
     return any(m.keys + m.session_keys)  # ignore method NONE
 
 def _get_stream_info(l, name):
     return getattr(getattr(l, 'stream_info',
                            getattr(l, 'iframe_stream_info', None)),
                    name)
 
 def load_m3u8_playlist(url, **kwargs):
     '''Params: as same as _load().'''
 
-    def append_stream(stype, profile, urls):
-        streams[stype] = {
+    def append_stream(stream_id, stream_profile, urls):
+        streams[stream_id] = {
             'container': 'm3u8',
-            'video_profile': profile,
-            'src' : urls,
-            'size': 0
+            'profile': stream_profile,
+            'src': urls
         }
 
     streams = MediaStreams()
     m = _load(url, **kwargs)
     ll = m.playlists or m.iframe_playlists
     if ll:
         for l in ll:
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/match.py` & `ykdl-1.8.2/ykdl/util/match.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import re
 
 
-__all__ = ['match', 'match1', 'matchm', 'matchall']
+__all__ = ['match', 'fullmatch', 'match1', 'matchm', 'matchall']
 
 def _format_str(pattern, string):
     '''Format the target which will be scanned, makes the worker happy.'''
     strtype = type(pattern)
     if not isinstance(string, strtype):
         try:
             string = strtype(string, 'utf-8')
@@ -44,14 +44,28 @@
     for pattern in patterns:
         string = _format_str(pattern, obj)
         m = re.search(pattern, string)
         if m:
             return m
     return None
 
+def fullmatch(obj, *patterns):
+    '''Scans a object for fully matched some patterns (matches first).
+
+    Params: same as match()
+
+    Returns the match string, or None.
+    '''
+    for pattern in patterns:
+        string = _format_str(pattern, obj)
+        m = re.fullmatch(pattern, string)
+        if m:
+            return m.string
+    return None
+
 def match1(obj, *patterns):
     '''Scans a object for matched some patterns with capture mode.
 
     Params: same as match()
 
     Returns the first captured substring, or None.
     '''
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/rangefetch_server.py` & `ykdl-1.8.2/ykdl/util/rangefetch_server.py`

 * *Files 0% similar despite different names*

```diff
@@ -94,15 +94,15 @@
 class RangeFetch():
 
     _expect_begin = 0
     _started_order = -1
     ssl_context = None
     proxy = None
     http = None
-    timeout = urllib3.Timeout(connect=1, read=2)
+    timeout = urllib3.Timeout(connect=2, read=5)
     pool_size = 24
 
     down_rate_min = 1024 * 160 # B/s
     down_rate_max = 1024 * 360
     check_size = 1024 * 512
     first_size = 1024 * 32
     max_size = 1024 * 32
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/wrap.py` & `ykdl-1.8.2/ykdl/util/wrap.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,36 +1,57 @@
 '''Wrap the functions of official packages which have been frequent used.'''
 
 import os
 import ast
+import sys
 import json
+import zlib
 import base64
 import random
 import string
 import pkgutil
+import traceback
 
 
-__all__ = ['reverse_list_dict', 'unb64', 'hash', 'literalize',
-           'get_pkgdata_str', 'get_pkgdata_bytes',
+__all__ = ['reverse_list_dict', 'b64', 'unb64', 'hash', 'literalize',
+           'deprecated', 'get_pkgdata_str', 'get_pkgdata_bytes',
            'get_random_hex', 'get_random_str', 'get_random_name',
            'get_random_id', 'get_random_uuid', 'get_random_uuid_hex']
 
 def reverse_list_dict(d):
     '''Reverse {key: values[List]} to {value: key}'''
     return dict(sum([[(v, k) for v in vs] for k, vs in d.items()], []))
 
-def unb64(b64, target='str'):
+def b64(s, target=str, urlsafe=False):
+    '''Encode string/bytes-like object to Base64.
+
+    Params:
+        `target` is `str` or `bytes`
+        `urlsafe` to use `urlsafe_b64encode`
+    '''
+    encode = getattr(base64, urlsafe and 'urlsafe_b64encode' or 'b64encode')
+    if isinstance(s, str):
+        s = s.encode()
+    if target is str:
+        return encode(s).decode()
+    if target is bytes:
+        return encode(s)
+
+def unb64(b64, target=str, urlsafe=False):
     '''Decode Base64 object to string/bytes.
 
-    Params: `target` is 'str' or 'bytes'
+    Params:
+        `target` is `str` or `bytes`
+        `urlsafe` to use `urlsafe_b64decode`
     '''
-    if target == 'str':
-        return base64.b64decode(b64).decode()
-    if target == 'bytes':
-        return base64.b64decode(b64)
+    decode = getattr(base64, urlsafe and 'urlsafe_b64decode' or 'b64decode')
+    if target is str:
+        return decode(b64).decode()
+    if target is bytes:
+        return decode(b64)
 
 def get_pkgdata_str(package, resource, url=None, encoding=None):
     '''Fetch the resource data from package, or from a fallback URL if give.
 
     Params: `package` package name usually the `__name__` attribute with
             current module.
 
@@ -62,20 +83,24 @@
     Return: bytes of requested resource.
     '''
     return get_pkgdata_str(package, resource, url, 'ignore')
 
 class HASH:
     '''Supported hash algorithm constructors are provided via attribute name,
     just likes hashlib, but only return hex digest.
+    And the object is also compatible with built-in function `hash`.
 
     For example:
 
         >>> hash.md5('1234567890')
         'e807f1fcf82d132f9bb018ca6738a19f'
-    '''
+        >>> hash(1.0)
+        1
+
+    ----------------------------------------------------------------------'''
 
     algorithms_available = {'MD5', 'SHA1', 'SHA224', 'SHA256', 'SHA384', 'SHA512'}
     init = None
 
     def __getattr__(self, name):
         import hashlib
         if self.init is None:
@@ -107,24 +132,50 @@
         hash.__doc__ = '''
             Return the resoult of a new hashing object {name}().hexdigest().
 
             Params: same as hashlib.{name}(), but string/data can be a str.
             '''.format(name=name)
         return hash
 
-hash = HASH()  # ISSUE: same name as built-in function
+    @staticmethod
+    def crc32(data):
+        '''Return the CRC-32 hexdigest of data.
+
+        `data`: string or bytes-like object
+        '''
+        if hasattr(data, 'encode'):
+            data = data.encode()
+        return '{:0>8x}'.format(zlib.crc32(data))
+
+    def __call__(self, obj):
+        return _hash(obj)
+
+_hash = hash
+hash = HASH()
 del HASH
 
 def literalize(s, JSON=False):
     '''Literalize the giving string as a Python/JSON literal.'''
     if JSON:
         return json.loads('"{}"'.format(s))
     else:
         return ast.literal_eval('"""{}"""'.format(s))
 
+_deprecated_once = set()
+
+def deprecated(msg):
+    '''Forced deprecated warning.'''
+    f = sys._getframe(2)
+    key = msg, f.f_code.co_filename, f.f_lineno
+    if key in _deprecated_once:
+        return
+    _deprecated_once.add(key)
+    print('DeprecationWarning: ', msg, '\n', *traceback.format_stack(f),
+          sep='', file=sys.stderr)
+
 _id_cache = {}
 _ascii_letters_digits = string.ascii_letters + string.digits
 
 def get_random_hex(l):
     '''Return a random hex string with specified length.'''
     l, r = divmod(l, 2)
     if r:
```

### Comparing `ykdl-1.8.1.post1/ykdl/util/xml2dict.py` & `ykdl-1.8.2/ykdl/util/xml2dict.py`

 * *Files identical despite different names*

### Comparing `ykdl-1.8.1.post1/ykdl.egg-info/SOURCES.txt` & `ykdl-1.8.2/ykdl.egg-info/SOURCES.txt`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 CHANGELOG.rst
 LICENSE.txt
 MANIFEST.in
 README.rst
+pyproject.toml
 setup.cfg
 setup.py
 cykdl/__init__.py
 cykdl/__main__.py
 ykdl/__init__.py
 ykdl/common.py
 ykdl/compact.py
@@ -27,19 +28,21 @@
 ykdl/extractors/cctv.py
 ykdl/extractors/fun.py
 ykdl/extractors/generalembed.py
 ykdl/extractors/generalsimple.py
 ykdl/extractors/heibaizhibo.m.js
 ykdl/extractors/heibaizhibo.py
 ykdl/extractors/iqilu.py
+ykdl/extractors/ixigua.py
 ykdl/extractors/joy.py
 ykdl/extractors/kankanews.py
 ykdl/extractors/ku6.py
 ykdl/extractors/kuwo.py
 ykdl/extractors/laifeng.py
+ykdl/extractors/le.py
 ykdl/extractors/lizhi.py
 ykdl/extractors/longzhu.py
 ykdl/extractors/mgtv.py
 ykdl/extractors/miaopai.py
 ykdl/extractors/pps.py
 ykdl/extractors/pptv.py
 ykdl/extractors/singlemultimedia.py
@@ -51,17 +54,16 @@
 ykdl/extractors/youkujs.py
 ykdl/extractors/zhangyu.py
 ykdl/extractors/zhanqi.py
 ykdl/extractors/zhuafan.py
 ykdl/extractors/acfun/__init__.py
 ykdl/extractors/acfun/acbase.py
 ykdl/extractors/acfun/bangumi.py
+ykdl/extractors/acfun/live.py
 ykdl/extractors/acfun/video.py
-ykdl/extractors/baidu/__init__.py
-ykdl/extractors/baidu/music.py
 ykdl/extractors/bilibili/__init__.py
 ykdl/extractors/bilibili/bangumi.py
 ykdl/extractors/bilibili/bilibase.py
 ykdl/extractors/bilibili/idconvertor.py
 ykdl/extractors/bilibili/live.py
 ykdl/extractors/bilibili/util.py
 ykdl/extractors/bilibili/vc.py
@@ -89,22 +91,14 @@
 ykdl/extractors/ifeng/video.py
 ykdl/extractors/iqiyi/__init__.py
 ykdl/extractors/iqiyi/cmd5x.js
 ykdl/extractors/iqiyi/cmd5x_iqiyi3.js
 ykdl/extractors/iqiyi/live.py
 ykdl/extractors/iqiyi/util.py
 ykdl/extractors/iqiyi/video.py
-ykdl/extractors/ixigua/__init__.py
-ykdl/extractors/ixigua/live.py
-ykdl/extractors/ixigua/video.py
-ykdl/extractors/le/__init__.py
-ykdl/extractors/le/le.py
-ykdl/extractors/le/letvcloud.py
-ykdl/extractors/le/live.py
-ykdl/extractors/le/lunbo.py
 ykdl/extractors/netease/__init__.py
 ykdl/extractors/netease/live.py
 ykdl/extractors/netease/livecc.py
 ykdl/extractors/netease/m3g.py
 ykdl/extractors/netease/openc.py
 ykdl/extractors/netease/video.py
 ykdl/extractors/netease/music/__init__.py
@@ -117,23 +111,24 @@
 ykdl/extractors/qq/live.py
 ykdl/extractors/qq/video.py
 ykdl/extractors/sina/__init__.py
 ykdl/extractors/sina/embed.py
 ykdl/extractors/sina/openc.py
 ykdl/extractors/sina/video.py
 ykdl/extractors/sohu/__init__.py
-ykdl/extractors/sohu/edu.py
 ykdl/extractors/sohu/my.py
 ykdl/extractors/sohu/sohubase.py
 ykdl/extractors/sohu/tv.py
 ykdl/util/__init__.py
 ykdl/util/download.py
 ykdl/util/external.py
 ykdl/util/fs.py
 ykdl/util/http.py
 ykdl/util/human.py
+ykdl/util/kt_player.py
+ykdl/util/lazy.py
 ykdl/util/log.py
 ykdl/util/m3u8.py
 ykdl/util/match.py
 ykdl/util/rangefetch_server.py
 ykdl/util/wrap.py
 ykdl/util/xml2dict.py
```

