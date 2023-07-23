# Comparing `tmp/wow_ai_mms-0.1.8.tar.gz` & `tmp/wow_ai_mms-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "wow_ai_mms-0.1.8.tar", max compression
+gzip compressed data, was "wow_ai_mms-0.1.9.tar", max compression
```

## Comparing `wow_ai_mms-0.1.8.tar` & `wow_ai_mms-0.1.9.tar`

### file list

```diff
@@ -1,403 +1,395 @@
--rw-r--r--   0        0        0    17529 2023-07-22 09:49:11.755219 wow_ai_mms-0.1.8/LICENSE
--rw-r--r--   0        0        0     4825 2023-07-22 09:49:11.756724 wow_ai_mms-0.1.8/README.md
--rw-r--r--   0        0        0      262 2023-07-23 08:07:21.374350 wow_ai_mms-0.1.8/pyproject.toml
--rw-r--r--   0        0        0     6148 2023-07-22 11:01:13.106052 wow_ai_mms-0.1.8/wow_ai_mms/.DS_Store
--rw-r--r--   0        0        0        0 2023-07-22 09:49:11.836893 wow_ai_mms-0.1.8/wow_ai_mms/__init__.py
--rw-r--r--   0        0        0      630 2023-07-22 09:49:11.837789 wow_ai_mms-0.1.8/wow_ai_mms/_logger.py
--rw-r--r--   0        0        0     5845 2023-07-22 09:49:11.838755 wow_ai_mms-0.1.8/wow_ai_mms/constants.py
--rw-r--r--   0        0        0   943341 2023-06-03 01:44:19.000000 wow_ai_mms-0.1.8/wow_ai_mms/data/mms_langs.json
--rw-r--r--   0        0        0     6148 2023-07-22 11:01:24.918084 wow_ai_mms-0.1.8/wow_ai_mms/examples/.DS_Store
--rw-r--r--   0        0        0     3264 2023-07-22 09:49:11.841220 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/MODEL_CARD.md
--rw-r--r--   0        0        0    13987 2023-07-22 09:49:11.842872 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/README.md
--rw-r--r--   0        0        0     6148 2023-07-14 14:23:35.567957 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/asr/.DS_Store
--rw-r--r--   0        0        0      697 2023-07-22 09:49:11.845855 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/asr/config/infer_common.yaml
--rw-r--r--   0        0        0      671 2023-07-22 09:49:11.846862 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/asr/infer/example_infer_adapter.sh
--rw-r--r--   0        0        0     2835 2023-07-22 09:49:11.848026 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/asr/infer/mms_infer.py
--rw-r--r--   0        0        0   639325 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/asr/tutorial/MMS_ASR_Inference_Colab.ipynb
--rw-r--r--   0        0        0     3366 2023-07-22 09:49:11.849095 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/README.md
--rw-r--r--   0        0        0     6241 2023-07-23 08:03:42.099825 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/align_and_segment.py
--rw-r--r--   0        0        0     5656 2023-07-22 09:49:11.851076 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/align_utils.py
--rw-r--r--   0        0        0     6532 2023-07-22 09:49:11.852153 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/norm_config.py
--rw-r--r--   0        0        0     6069 2023-07-22 09:49:11.853057 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/punctuations.lst
--rw-r--r--   0        0        0       23 2023-07-23 08:06:37.144498 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/HEAD
--rw-r--r--   0        0        0      302 2023-07-23 08:06:37.153959 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/config
--rw-r--r--   0        0        0       73 2023-07-23 08:06:03.045164 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/description
--rwxr-xr-x   0        0        0      478 2023-07-23 08:06:03.048651 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/applypatch-msg.sample
--rwxr-xr-x   0        0        0      896 2023-07-23 08:06:03.046322 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/commit-msg.sample
--rwxr-xr-x   0        0        0     4726 2023-07-23 08:06:03.049581 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/fsmonitor-watchman.sample
--rwxr-xr-x   0        0        0      189 2023-07-23 08:06:03.051365 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/post-update.sample
--rwxr-xr-x   0        0        0      424 2023-07-23 08:06:03.053734 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-applypatch.sample
--rwxr-xr-x   0        0        0     1643 2023-07-23 08:06:03.048105 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-commit.sample
--rwxr-xr-x   0        0        0      416 2023-07-23 08:06:03.052919 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-merge-commit.sample
--rwxr-xr-x   0        0        0     1374 2023-07-23 08:06:03.054569 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-push.sample
--rwxr-xr-x   0        0        0     4898 2023-07-23 08:06:03.047392 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-rebase.sample
--rwxr-xr-x   0        0        0      544 2023-07-23 08:06:03.050218 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-receive.sample
--rwxr-xr-x   0        0        0     1492 2023-07-23 08:06:03.050839 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/prepare-commit-msg.sample
--rwxr-xr-x   0        0        0     2783 2023-07-23 08:06:03.055764 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/push-to-checkout.sample
--rwxr-xr-x   0        0        0     3650 2023-07-23 08:06:03.055142 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/update.sample
--rw-r--r--   0        0        0    24628 2023-07-23 08:06:37.418472 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/index
--rw-r--r--   0        0        0      240 2023-07-23 08:06:03.043712 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/info/exclude
--rw-r--r--   0        0        0      179 2023-07-23 08:06:37.149117 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/logs/HEAD
--rw-r--r--   0        0        0      179 2023-07-23 08:06:37.150011 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/logs/refs/heads/master
--rw-r--r--   0        0        0      179 2023-07-23 08:06:37.141912 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/logs/refs/remotes/origin/HEAD
--rw-r--r--   0        0        0   601924 2023-07-23 08:06:37.090054 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/objects/pack/pack-7afb9b59823f4376441f898fda8968960e3a8c82.idx
--rw-r--r--   0        0        0  7535521 2023-07-23 08:06:37.057164 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/objects/pack/pack-7afb9b59823f4376441f898fda8968960e3a8c82.pack
--rw-r--r--   0        0        0     2159 2023-07-23 08:06:37.137820 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/packed-refs
--rw-r--r--   0        0        0       41 2023-07-23 08:06:37.148235 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/refs/heads/master
--rw-r--r--   0        0        0       32 2023-07-23 08:06:37.142089 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/refs/remotes/origin/HEAD
--rw-r--r--   0        0        0      297 2023-07-23 08:06:37.174399 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.gitignore
--rw-r--r--   0        0        0      308 2023-07-23 08:06:37.175367 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/AUTHORS
--rw-r--r--   0        0        0      548 2023-07-23 08:06:37.175886 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/COPYING
--rw-r--r--   0        0        0    82038 2023-07-23 08:06:37.178168 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/ChangeLog
--rw-r--r--   0        0        0    77175 2023-07-23 08:06:37.179479 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/Doxyfile
--rw-r--r--   0        0        0     5465 2023-07-23 08:06:37.180641 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/FEATURES.in
--rw-r--r--   0        0        0     6346 2023-07-23 08:06:37.181272 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/INSTALL
--rw-r--r--   0        0        0    17987 2023-07-23 08:06:37.182241 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/LICENSE.GPL
--rw-r--r--   0        0        0    26436 2023-07-23 08:06:37.183879 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/LICENSE.LGPL
--rw-r--r--   0        0        0     3752 2023-07-23 08:06:37.187778 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/Makefile.am
--rw-r--r--   0        0        0      465 2023-07-23 08:06:37.188987 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/NEWS
--rw-r--r--   0        0        0     4013 2023-07-23 08:06:37.190200 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/README.osx
--rwxr-xr-x   0        0        0     2377 2023-07-23 08:06:37.191217 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/README.sh
--rw-r--r--   0        0        0     5843 2023-07-23 08:06:37.191982 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/README.win32
--rw-r--r--   0        0        0     5678 2023-07-23 08:06:37.192461 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/configure.ac
--rwxr-xr-x   0        0        0     4033 2023-07-23 08:06:37.193045 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/cygbuild
--rw-r--r--   0        0        0    15290 2023-07-23 08:06:37.194358 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/libsox.3
--rw-r--r--   0        0        0       47 2023-07-23 08:06:37.195358 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/.gitignore
--rw-r--r--   0        0        0      844 2023-07-23 08:06:37.195764 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/Makefile.am
--rw-r--r--   0        0        0     2324 2023-07-23 08:06:37.196420 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/README
--rw-r--r--   0        0        0     4090 2023-07-23 08:06:37.197041 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/README.lib
--rw-r--r--   0        0        0    19502 2023-07-23 08:06:37.197869 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/analys.c
--rw-r--r--   0        0        0       40 2023-07-23 08:06:37.199404 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/bitio.c
--rw-r--r--   0        0        0       95 2023-07-23 08:06:37.200636 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/bitio.h
--rw-r--r--   0        0        0    11717 2023-07-23 08:06:37.203225 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/bsynz.c
--rw-r--r--   0        0        0     6701 2023-07-23 08:06:37.203801 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/chanwr.c
--rw-r--r--   0        0        0     1910 2023-07-23 08:06:37.205067 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/dcbias.c
--rw-r--r--   0        0        0    17236 2023-07-23 08:06:37.206355 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/decode.c
--rw-r--r--   0        0        0     3455 2023-07-23 08:06:37.207279 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/deemp.c
--rw-r--r--   0        0        0     2918 2023-07-23 08:06:37.207751 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/difmag.c
--rw-r--r--   0        0        0    11418 2023-07-23 08:06:37.208191 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/dyptrk.c
--rw-r--r--   0        0        0     9909 2023-07-23 08:06:37.208958 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/encode.c
--rw-r--r--   0        0        0     1794 2023-07-23 08:06:37.210451 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/energy.c
--rw-r--r--   0        0        0     4549 2023-07-23 08:06:37.211709 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/f2c.h
--rw-r--r--   0        0        0     1309 2023-07-23 08:06:37.213299 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/f2clib.c
--rw-r--r--   0        0        0     2797 2023-07-23 08:06:37.213958 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/ham84.c
--rw-r--r--   0        0        0     2796 2023-07-23 08:06:37.215401 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/hp100.c
--rw-r--r--   0        0        0     4205 2023-07-23 08:06:37.215984 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/invert.c
--rw-r--r--   0        0        0     2458 2023-07-23 08:06:37.216448 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/irc2pc.c
--rw-r--r--   0        0        0     2785 2023-07-23 08:06:37.217239 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/ivfilt.c
--rw-r--r--   0        0        0     8708 2023-07-23 08:06:37.220442 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpc10.h
--rw-r--r--   0        0        0     6973 2023-07-23 08:06:37.221249 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcdec.c
--rw-r--r--   0        0        0     3455 2023-07-23 08:06:37.221711 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcenc.c
--rw-r--r--   0        0        0     9540 2023-07-23 08:06:37.222230 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcini.c
--rw-r--r--   0        0        0     2878 2023-07-23 08:06:37.223955 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpfilt.c
--rw-r--r--   0        0        0     1258 2023-07-23 08:06:37.224535 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/median.c
--rw-r--r--   0        0        0     4446 2023-07-23 08:06:37.225308 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/mload.c
--rw-r--r--   0        0        0     8824 2023-07-23 08:06:37.226058 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/onset.c
--rw-r--r--   0        0        0    16158 2023-07-23 08:06:37.226619 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/pitsyn.c
--rw-r--r--   0        0        0     7658 2023-07-23 08:06:37.227115 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/placea.c
--rw-r--r--   0        0        0     7761 2023-07-23 08:06:37.227570 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/placev.c
--rw-r--r--   0        0        0     3452 2023-07-23 08:06:37.228077 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/preemp.c
--rw-r--r--   0        0        0     2487 2023-07-23 08:06:37.228531 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/prepro.c
--rw-r--r--   0        0        0     2605 2023-07-23 08:06:37.228990 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/random.c
--rw-r--r--   0        0        0     2277 2023-07-23 08:06:37.229510 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/rcchk.c
--rw-r--r--   0        0        0    11585 2023-07-23 08:06:37.230031 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/synths.c
--rw-r--r--   0        0        0     4950 2023-07-23 08:06:37.230442 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/tbdm.c
--rw-r--r--   0        0        0    26833 2023-07-23 08:06:37.232937 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/voicin.c
--rw-r--r--   0        0        0     8044 2023-07-23 08:06:37.233616 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/vparms.c
--rw-r--r--   0        0        0       63 2023-07-23 08:06:37.234200 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/m4/.gitignore
--rw-r--r--   0        0        0     8953 2023-07-23 08:06:37.234633 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/m4/sox.m4
--rwxr-xr-x   0        0        0     4615 2023-07-23 08:06:37.235075 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/mingwbuild
--rwxr-xr-x   0        0        0     6030 2023-07-23 08:06:37.235442 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/osxbuild
--rwxr-xr-x   0        0        0     8371 2023-07-23 08:06:37.236661 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/release.sh
--rw-r--r--   0        0        0     1431 2023-07-23 08:06:37.236994 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/screenshot1
--rwxr-xr-x   0        0        0     1618 2023-07-23 08:06:37.238066 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/alert.sh
--rw-r--r--   0        0        0      520 2023-07-23 08:06:37.238456 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/batch-example.bat
--rwxr-xr-x   0        0        0     4978 2023-07-23 08:06:37.240477 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/crossfade.sh
--rwxr-xr-x   0        0        0     4248 2023-07-23 08:06:37.241585 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/crossfade_cat.sh
--rwxr-xr-x   0        0        0     4969 2023-07-23 08:06:37.245639 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/synth.sh
--rwxr-xr-x   0        0        0     5629 2023-07-23 08:06:37.246163 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/testcd.sh
--rwxr-xr-x   0        0        0     7684 2023-07-23 08:06:37.247249 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/testtones.sh
--rwxr-xr-x   0        0        0      563 2023-07-23 08:06:37.249225 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/voice-cleanup.sh
--rw-r--r--   0        0        0   149613 2023-07-23 08:06:37.254223 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/sox.1
--rw-r--r--   0        0        0      264 2023-07-23 08:06:37.257506 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/sox.pc.in
--rw-r--r--   0        0        0    27442 2023-07-23 08:06:37.258196 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/soxformat.7
--rw-r--r--   0        0        0     3236 2023-07-23 08:06:37.258666 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/soxi.1
--rw-r--r--   0        0        0      193 2023-07-23 08:06:37.259150 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/.gitignore
--rw-r--r--   0        0        0    12163 2023-07-23 08:06:37.259733 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/8svx.c
--rw-r--r--   0        0        0     5667 2023-07-23 08:06:37.260576 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/Makefile.am
--rw-r--r--   0        0        0    12598 2023-07-23 08:06:37.261262 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/adpcm.c
--rw-r--r--   0        0        0     2839 2023-07-23 08:06:37.261855 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/adpcm.h
--rw-r--r--   0        0        0    11172 2023-07-23 08:06:37.262403 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/adpcms.c
--rw-r--r--   0        0        0     1989 2023-07-23 08:06:37.263255 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/adpcms.h
--rw-r--r--   0        0        0     1443 2023-07-23 08:06:37.264375 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/aifc-fmt.c
--rw-r--r--   0        0        0     1377 2023-07-23 08:06:37.264796 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/aiff-fmt.c
--rw-r--r--   0        0        0    39580 2023-07-23 08:06:37.266126 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/aiff.c
--rw-r--r--   0        0        0      916 2023-07-23 08:06:37.266622 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/aiff.h
--rw-r--r--   0        0        0      875 2023-07-23 08:06:37.267020 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/al-fmt.c
--rw-r--r--   0        0        0    13558 2023-07-23 08:06:37.267708 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/alsa.c
--rw-r--r--   0        0        0     3350 2023-07-23 08:06:37.269319 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/amr-nb.c
--rw-r--r--   0        0        0     3643 2023-07-23 08:06:37.270326 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/amr-wb.c
--rw-r--r--   0        0        0     8412 2023-07-23 08:06:37.271263 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/amr.h
--rw-r--r--   0        0        0     3760 2023-07-23 08:06:37.272366 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ao.c
--rw-r--r--   0        0        0     9412 2023-07-23 08:06:37.273028 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/au.c
--rw-r--r--   0        0        0     7106 2023-07-23 08:06:37.274502 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/avr.c
--rw-r--r--   0        0        0     1801 2023-07-23 08:06:37.275013 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/band.h
--rw-r--r--   0        0        0    11272 2023-07-23 08:06:37.275774 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bend.c
--rw-r--r--   0        0        0     5990 2023-07-23 08:06:37.276370 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/biquad.c
--rw-r--r--   0        0        0     2377 2023-07-23 08:06:37.276740 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/biquad.h
--rw-r--r--   0        0        0    13920 2023-07-23 08:06:37.277214 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/biquads.c
--rw-r--r--   0        0        0     8547 2023-07-23 08:06:37.278002 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/CoreAudio/CoreAudio.h
--rw-r--r--   0        0        0        0 2023-07-23 08:06:37.278136 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/mmreg.h
--rw-r--r--   0        0        0     2312 2023-07-23 08:06:37.278442 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/mmsystem.h
--rw-r--r--   0        0        0     4581 2023-07-23 08:06:37.280281 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/sndio.h
--rw-r--r--   0        0        0     8806 2023-07-23 08:06:37.280848 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/sys/audioio.h
--rw-r--r--   0        0        0      725 2023-07-23 08:06:37.281106 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/windows.h
--rw-r--r--   0        0        0     1332 2023-07-23 08:06:37.281529 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/caf.c
--rw-r--r--   0        0        0     1852 2023-07-23 08:06:37.281933 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cdr.c
--rw-r--r--   0        0        0    13028 2023-07-23 08:06:37.282765 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/chorus.c
--rw-r--r--   0        0        0    10057 2023-07-23 08:06:37.283070 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/compand.c
--rw-r--r--   0        0        0     6762 2023-07-23 08:06:37.283330 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/compandt.c
--rw-r--r--   0        0        0     1768 2023-07-23 08:06:37.283690 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/compandt.h
--rw-r--r--   0        0        0     1800 2023-07-23 08:06:37.284224 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/contrast.c
--rw-r--r--   0        0        0    12342 2023-07-23 08:06:37.284664 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/coreaudio.c
--rwxr-xr-x   0        0        0     2168 2023-07-23 08:06:37.284965 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/csox
--rw-r--r--   0        0        0     3678 2023-07-23 08:06:37.285331 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd-fmt.c
--rw-r--r--   0        0        0    23370 2023-07-23 08:06:37.286815 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd.c
--rw-r--r--   0        0        0     2312 2023-07-23 08:06:37.288647 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd.h
--rw-r--r--   0        0        0     5160 2023-07-23 08:06:37.289463 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cvsdfilt.h
--rw-r--r--   0        0        0     4685 2023-07-23 08:06:37.290439 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dat.c
--rw-r--r--   0        0        0     4982 2023-07-23 08:06:37.291291 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dcshift.c
--rw-r--r--   0        0        0     3602 2023-07-23 08:06:37.292512 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/deemph.plt
--rw-r--r--   0        0        0     5007 2023-07-23 08:06:37.292944 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/delay.c
--rw-r--r--   0        0        0     4386 2023-07-23 08:06:37.293334 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dft_filter.c
--rw-r--r--   0        0        0      396 2023-07-23 08:06:37.293653 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dft_filter.h
--rw-r--r--   0        0        0    15076 2023-07-23 08:06:37.294212 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dither.c
--rw-r--r--   0        0        0     2076 2023-07-23 08:06:37.296206 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dither.h
--rw-r--r--   0        0        0     2351 2023-07-23 08:06:37.296826 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/divide.c
--rw-r--r--   0        0        0     2553 2023-07-23 08:06:37.298464 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/downsample.c
--rw-r--r--   0        0        0     1373 2023-07-23 08:06:37.299182 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dvms-fmt.c
--rw-r--r--   0        0        0     4246 2023-07-23 08:06:37.299798 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/earwax.c
--rw-r--r--   0        0        0     9330 2023-07-23 08:06:37.303055 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/echo.c
--rw-r--r--   0        0        0     9998 2023-07-23 08:06:37.304650 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/echos.c
--rw-r--r--   0        0        0    23109 2023-07-23 08:06:37.306343 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/effects.c
--rw-r--r--   0        0        0     2031 2023-07-23 08:06:37.307058 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/effects.h
--rw-r--r--   0        0        0    13239 2023-07-23 08:06:37.311620 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/effects_i.c
--rw-r--r--   0        0        0    19837 2023-07-23 08:06:37.313686 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/effects_i_dsp.c
--rw-r--r--   0        0        0     3869 2023-07-23 08:06:37.314414 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example0.c
--rw-r--r--   0        0        0     6433 2023-07-23 08:06:37.317685 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example1.c
--rw-r--r--   0        0        0     4441 2023-07-23 08:06:37.318206 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example2.c
--rw-r--r--   0        0        0     3963 2023-07-23 08:06:37.318713 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example3.c
--rw-r--r--   0        0        0     3758 2023-07-23 08:06:37.320594 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example4.c
--rw-r--r--   0        0        0     2723 2023-07-23 08:06:37.321129 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example5.c
--rw-r--r--   0        0        0     3948 2023-07-23 08:06:37.322191 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example6.c
--rw-r--r--   0        0        0      887 2023-07-23 08:06:37.322589 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/f4-fmt.c
--rw-r--r--   0        0        0      887 2023-07-23 08:06:37.323558 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/f8-fmt.c
--rw-r--r--   0        0        0    11978 2023-07-23 08:06:37.324465 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fade.c
--rw-r--r--   0        0        0     1260 2023-07-23 08:06:37.325162 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fap.c
--rw-r--r--   0        0        0    37607 2023-07-23 08:06:37.325842 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fft4g.c
--rw-r--r--   0        0        0     1667 2023-07-23 08:06:37.326253 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fft4g.h
--rw-r--r--   0        0        0     2922 2023-07-23 08:06:37.326888 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fifo.h
--rw-r--r--   0        0        0     3371 2023-07-23 08:06:37.327418 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fir.c
--rw-r--r--   0        0        0     4643 2023-07-23 08:06:37.327769 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/firfit.c
--rw-r--r--   0        0        0    20871 2023-07-23 08:06:37.328484 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/flac.c
--rw-r--r--   0        0        0     8553 2023-07-23 08:06:37.328958 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/flanger.c
--rw-r--r--   0        0        0    43364 2023-07-23 08:06:37.330025 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/formats.c
--rw-r--r--   0        0        0     3530 2023-07-23 08:06:37.330425 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/formats.h
--rw-r--r--   0        0        0    16895 2023-07-23 08:06:37.330943 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/formats_i.c
--rw-r--r--   0        0        0   165842 2023-07-23 08:06:37.334262 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g711.c
--rw-r--r--   0        0        0      934 2023-07-23 08:06:37.338671 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g711.h
--rw-r--r--   0        0        0     5316 2023-07-23 08:06:37.339427 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g721.c
--rw-r--r--   0        0        0     4695 2023-07-23 08:06:37.340122 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g723_24.c
--rw-r--r--   0        0        0     5582 2023-07-23 08:06:37.340757 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g723_40.c
--rw-r--r--   0        0        0    21238 2023-07-23 08:06:37.342153 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g72x.c
--rw-r--r--   0        0        0     4861 2023-07-23 08:06:37.342872 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g72x.h
--rw-r--r--   0        0        0     9592 2023-07-23 08:06:37.343626 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/gain.c
--rw-r--r--   0        0        0    11726 2023-07-23 08:06:37.344339 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/getopt.c
--rw-r--r--   0        0        0     7017 2023-07-23 08:06:37.344774 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/gsm.c
--rw-r--r--   0        0        0     6471 2023-07-23 08:06:37.345239 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/gsrt.c
--rw-r--r--   0        0        0    15310 2023-07-23 08:06:37.346004 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/hcom.c
--rw-r--r--   0        0        0     3205 2023-07-23 08:06:37.346483 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/hilbert.c
--rw-r--r--   0        0        0     3128 2023-07-23 08:06:37.346858 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/htk.c
--rw-r--r--   0        0        0     6146 2023-07-23 08:06:37.347238 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/id3.c
--rw-r--r--   0        0        0      935 2023-07-23 08:06:37.347606 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/id3.h
--rw-r--r--   0        0        0     1329 2023-07-23 08:06:37.348136 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ima-fmt.c
--rw-r--r--   0        0        0    13813 2023-07-23 08:06:37.348694 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ima_rw.c
--rw-r--r--   0        0        0     3166 2023-07-23 08:06:37.349155 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ima_rw.h
--rw-r--r--   0        0        0     2087 2023-07-23 08:06:37.349630 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/input.c
--rw-r--r--   0        0        0      892 2023-07-23 08:06:37.350122 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/la-fmt.c
--rw-r--r--   0        0        0    15801 2023-07-23 08:06:37.352784 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ladspa.c
--rw-r--r--   0        0        0    27595 2023-07-23 08:06:37.353531 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ladspa.h
--rw-r--r--   0        0        0     6147 2023-07-23 08:06:37.354433 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/libsox.c
--rw-r--r--   0        0        0     1575 2023-07-23 08:06:37.354812 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/libsox.sym
--rw-r--r--   0        0        0     3264 2023-07-23 08:06:37.355283 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/libsox_i.c
--rw-r--r--   0        0        0     4669 2023-07-23 08:06:37.355770 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/loudness.c
--rw-r--r--   0        0        0     6729 2023-07-23 08:06:37.356307 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/lpc10.c
--rw-r--r--   0        0        0      892 2023-07-23 08:06:37.356787 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/lu-fmt.c
--rw-r--r--   0        0        0     1275 2023-07-23 08:06:37.357132 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mat4.c
--rw-r--r--   0        0        0     1268 2023-07-23 08:06:37.357440 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mat5.c
--rw-r--r--   0        0        0    11620 2023-07-23 08:06:37.357981 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/maud.c
--rw-r--r--   0        0        0    16130 2023-07-23 08:06:37.359233 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mcompand.c
--rw-r--r--   0        0        0     3704 2023-07-23 08:06:37.359716 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mcompand_xover.h
--rw-r--r--   0        0        0     1670 2023-07-23 08:06:37.360259 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/monkey.wav
--rw-r--r--   0        0        0     6478 2023-07-23 08:06:37.360733 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mp3-util.h
--rw-r--r--   0        0        0    40627 2023-07-23 08:06:37.361681 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mp3.c
--rw-r--r--   0        0        0     6065 2023-07-23 08:06:37.362323 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/noiseprof.c
--rw-r--r--   0        0        0    10178 2023-07-23 08:06:37.362939 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/noisered.c
--rw-r--r--   0        0        0     1028 2023-07-23 08:06:37.363369 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/noisered.h
--rw-r--r--   0        0        0     2086 2023-07-23 08:06:37.364113 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/nulfile.c
--rw-r--r--   0        0        0     7151 2023-07-23 08:06:37.364673 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/optional-fmts.am
--rw-r--r--   0        0        0     5903 2023-07-23 08:06:37.365131 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/opus.c
--rw-r--r--   0        0        0    14635 2023-07-23 08:06:37.366307 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/oss.c
--rw-r--r--   0        0        0     2120 2023-07-23 08:06:37.367121 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/output.c
--rw-r--r--   0        0        0     2266 2023-07-23 08:06:37.367506 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/overdrive.c
--rw-r--r--   0        0        0     6005 2023-07-23 08:06:37.368009 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/pad.c
--rw-r--r--   0        0        0     1257 2023-07-23 08:06:37.368364 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/paf.c
--rw-r--r--   0        0        0     4595 2023-07-23 08:06:37.368754 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/phaser.c
--rw-r--r--   0        0        0    14458 2023-07-23 08:06:37.369395 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/prc.c
--rw-r--r--   0        0        0     3854 2023-07-23 08:06:37.369802 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/pulseaudio.c
--rw-r--r--   0        0        0     1219 2023-07-23 08:06:37.370148 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/pvf.c
--rw-r--r--   0        0        0    26724 2023-07-23 08:06:37.370707 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate.c
--rw-r--r--   0        0        0     6398 2023-07-23 08:06:37.371075 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate_filters.h
--rw-r--r--   0        0        0     1474 2023-07-23 08:06:37.371376 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate_half_fir.h
--rw-r--r--   0        0        0     3190 2023-07-23 08:06:37.371574 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate_poly_fir.h
--rw-r--r--   0        0        0     1856 2023-07-23 08:06:37.372001 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate_poly_fir0.h
--rw-r--r--   0        0        0     2145 2023-07-23 08:06:37.372302 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/raw-fmt.c
--rw-r--r--   0        0        0     7874 2023-07-23 08:06:37.372581 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/raw.c
--rw-r--r--   0        0        0     2278 2023-07-23 08:06:37.372899 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/raw.h
--rw-r--r--   0        0        0     9453 2023-07-23 08:06:37.373114 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/remix.c
--rw-r--r--   0        0        0     3686 2023-07-23 08:06:37.373440 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/repeat.c
--rw-r--r--   0        0        0     9071 2023-07-23 08:06:37.373769 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/reverb.c
--rw-r--r--   0        0        0     2416 2023-07-23 08:06:37.374020 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/reverse.c
--rw-r--r--   0        0        0      891 2023-07-23 08:06:37.374297 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/s1-fmt.c
--rw-r--r--   0        0        0      893 2023-07-23 08:06:37.374736 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/s2-fmt.c
--rw-r--r--   0        0        0      887 2023-07-23 08:06:37.375019 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/s3-fmt.c
--rw-r--r--   0        0        0      893 2023-07-23 08:06:37.375282 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/s4-fmt.c
--rw-r--r--   0        0        0     1215 2023-07-23 08:06:37.375862 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sd2.c
--rw-r--r--   0        0        0     6043 2023-07-23 08:06:37.376213 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sf.c
--rw-r--r--   0        0        0    24152 2023-07-23 08:06:37.376702 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/silence.c
--rw-r--r--   0        0        0     5208 2023-07-23 08:06:37.377075 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sinc.c
--rw-r--r--   0        0        0     3690 2023-07-23 08:06:37.377537 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/skeleff.c
--rw-r--r--   0        0        0     6165 2023-07-23 08:06:37.377842 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/skelform.c
--rw-r--r--   0        0        0    15514 2023-07-23 08:06:37.378204 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/smp.c
--rw-r--r--   0        0        0    18260 2023-07-23 08:06:37.378614 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sndfile.c
--rw-r--r--   0        0        0     6557 2023-07-23 08:06:37.379057 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sndio.c
--rw-r--r--   0        0        0     2071 2023-07-23 08:06:37.379372 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sounder.c
--rw-r--r--   0        0        0     3290 2023-07-23 08:06:37.379689 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/soundtool.c
--rw-r--r--   0        0        0     4001 2023-07-23 08:06:37.380309 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox-fmt.c
--rw-r--r--   0        0        0   102002 2023-07-23 08:06:37.381961 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox.c
--rw-r--r--   0        0        0    91627 2023-07-23 08:06:37.385160 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox.h
--rw-r--r--   0        0        0    17985 2023-07-23 08:06:37.386589 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox_i.h
--rw-r--r--   0        0        0     7349 2023-07-23 08:06:37.387035 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox_sample_test.c
--rw-r--r--   0        0        0     1153 2023-07-23 08:06:37.387350 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/soxomp.h
--rw-r--r--   0        0        0    33632 2023-07-23 08:06:37.387796 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/spectrogram.c
--rw-r--r--   0        0        0     2300 2023-07-23 08:06:37.388196 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/speed.c
--rw-r--r--   0        0        0    11591 2023-07-23 08:06:37.388651 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/speexdsp.c
--rw-r--r--   0        0        0     6626 2023-07-23 08:06:37.388942 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sphere.c
--rw-r--r--   0        0        0    10728 2023-07-23 08:06:37.389158 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/splice.c
--rw-r--r--   0        0        0     9036 2023-07-23 08:06:37.389571 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/stat.c
--rw-r--r--   0        0        0    10006 2023-07-23 08:06:37.389986 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/stats.c
--rw-r--r--   0        0        0     8263 2023-07-23 08:06:37.390276 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/stretch.c
--rw-r--r--   0        0        0    16768 2023-07-23 08:06:37.391006 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sunaudio.c
--rw-r--r--   0        0        0     1834 2023-07-23 08:06:37.391452 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/swap.c
--rw-r--r--   0        0        0    22155 2023-07-23 08:06:37.392249 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/synth.c
--rw-r--r--   0        0        0    12311 2023-07-23 08:06:37.392720 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tempo.c
--rwxr-xr-x   0        0        0     1724 2023-07-23 08:06:37.392994 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/test-comments
--rwxr-xr-x   0        0        0     1326 2023-07-23 08:06:37.393358 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/test-srcs
--rw-r--r--   0        0        0     1182 2023-07-23 08:06:37.393638 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/testall.bat
--rwxr-xr-x   0        0        0      967 2023-07-23 08:06:37.393865 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/testall.sh
--rw-r--r--   0        0        0     1356 2023-07-23 08:06:37.394066 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tests.bat
--rwxr-xr-x   0        0        0     7452 2023-07-23 08:06:37.394483 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tests.sh
--rw-r--r--   0        0        0     1727 2023-07-23 08:06:37.394721 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tremolo.c
--rw-r--r--   0        0        0     6852 2023-07-23 08:06:37.394989 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/trim.c
--rw-r--r--   0        0        0    12100 2023-07-23 08:06:37.395290 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tx16w.c
--rw-r--r--   0        0        0      909 2023-07-23 08:06:37.395556 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/u1-fmt.c
--rw-r--r--   0        0        0      896 2023-07-23 08:06:37.396321 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/u2-fmt.c
--rw-r--r--   0        0        0      890 2023-07-23 08:06:37.396803 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/u3-fmt.c
--rw-r--r--   0        0        0      890 2023-07-23 08:06:37.397104 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/u4-fmt.c
--rw-r--r--   0        0        0      877 2023-07-23 08:06:37.397417 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ul-fmt.c
--rw-r--r--   0        0        0     2171 2023-07-23 08:06:37.397682 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/upsample.c
--rw-r--r--   0        0        0     8569 2023-07-23 08:06:37.397940 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/util.c
--rw-r--r--   0        0        0     4821 2023-07-23 08:06:37.398195 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/util.h
--rw-r--r--   0        0        0    13117 2023-07-23 08:06:37.398483 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vad.c
--rw-r--r--   0        0        0    23493 2023-07-23 08:06:37.399620 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-N.s8
--rw-r--r--   0        0        0    23493 2023-07-23 08:06:37.400342 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-X.s8
--rw-r--r--   0        0        0    23493 2023-07-23 08:06:37.400835 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-X_-N.s8
--rw-r--r--   0        0        0    23493 2023-07-23 08:06:37.402974 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_.s8
--rw-r--r--   0        0        0    29211 2023-07-23 08:06:37.403733 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/voc.c
--rw-r--r--   0        0        0     5695 2023-07-23 08:06:37.404356 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vol.c
--rw-r--r--   0        0        0    11579 2023-07-23 08:06:37.404845 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vorbis.c
--rw-r--r--   0        0        0     1349 2023-07-23 08:06:37.405388 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vox-fmt.c
--rw-r--r--   0        0        0     1269 2023-07-23 08:06:37.405830 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vox.c
--rw-r--r--   0        0        0     1097 2023-07-23 08:06:37.406213 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vox.h
--rw-r--r--   0        0        0     1452 2023-07-23 08:06:37.406624 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/w64.c
--rw-r--r--   0        0        0    54729 2023-07-23 08:06:37.408095 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/wav.c
--rw-r--r--   0        0        0    14964 2023-07-23 08:06:37.408759 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/waveaudio.c
--rw-r--r--   0        0        0     7371 2023-07-23 08:06:37.409113 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/wavpack.c
--rw-r--r--   0        0        0     3838 2023-07-23 08:06:37.409798 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/win32/glob.c
--rw-r--r--   0        0        0     1208 2023-07-23 08:06:37.410168 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/win32/glob.h
--rw-r--r--   0        0        0     2348 2023-07-23 08:06:37.410513 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/wve.c
--rw-r--r--   0        0        0    10794 2023-07-23 08:06:37.410991 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/xa.c
--rw-r--r--   0        0        0     1205 2023-07-23 08:06:37.411337 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/xi.c
--rw-r--r--   0        0        0     1944 2023-07-23 08:06:37.411737 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/xmalloc.c
--rw-r--r--   0        0        0     1438 2023-07-23 08:06:37.412554 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/xmalloc.h
--rw-r--r--   0        0        0      383 2023-07-23 08:06:37.413088 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/Makefile
--rw-r--r--   0        0        0     3471 2023-07-23 08:06:37.413697 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/README
--rw-r--r--   0        0        0     4121 2023-07-23 08:06:37.414124 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/corr.c
--rwxr-xr-x   0        0        0     3545 2023-07-23 08:06:37.414829 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/ltest.pl
--rw-r--r--   0        0        0     6717 2023-07-23 08:06:37.415327 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/model.c
--rw-r--r--   0        0        0      330 2023-07-23 08:06:37.416399 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/plotA
--rw-r--r--   0        0        0      465 2023-07-23 08:06:37.416962 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/plotAB
--rw-r--r--   0        0        0      337 2023-07-23 08:06:37.417446 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/responseAB
--rwxr-xr-x   0        0        0     2971 2023-07-23 08:06:37.417735 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/wtest.pl
--rw-r--r--   0        0        0     2790 2023-07-23 07:09:07.609855 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/text_normalization.py
--rw-r--r--   0        0        0     7071 2023-07-22 09:49:11.855224 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/lid/infer.py
--rw-r--r--   0        0        0    21322 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/lid/tutorial/MMS_LID_Inference_Colab.ipynb
--rw-r--r--   0        0        0      808 2023-07-22 09:49:11.856391 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/misc/get_sample_size.py
--rw-r--r--   0        0        0     5802 2023-07-22 09:49:11.857738 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/tts/infer.py
--rw-r--r--   0        0        0   369355 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/tts/tutorial/MMS_TTS_Inference_Colab.ipynb
--rw-r--r--   0        0        0        1 2023-07-22 09:49:11.858761 wow_ai_mms-0.1.8/wow_ai_mms/models/__init__.py
--rw-r--r--   0        0        0     7711 2023-07-23 06:30:49.679854 wow_ai_mms-0.1.8/wow_ai_mms/models/alignment.py
--rw-r--r--   0        0        0     9510 2023-07-22 11:19:05.801050 wow_ai_mms-0.1.8/wow_ai_mms/models/asr.py
--rw-r--r--   0        0        0     6148 2023-07-22 11:01:30.902596 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/.DS_Store
--rw-r--r--   0        0        0     5706 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/README.md
--rw-r--r--   0        0        0       48 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/__init__.py
--rw-r--r--   0        0        0     5879 2023-07-22 11:25:26.672742 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/criterions/ASG_loss.py
--rw-r--r--   0        0        0      519 2023-07-22 11:40:04.527684 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/criterions/__init__.py
--rw-r--r--   0        0        0     5372 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/criterions/cross_entropy_acc.py
--rw-r--r--   0        0        0      248 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/data/__init__.py
--rw-r--r--   0        0        0     3955 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/data/asr_dataset.py
--rw-r--r--   0        0        0     4796 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/data/collaters.py
--rw-r--r--   0        0        0     3429 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/data/data_utils.py
--rw-r--r--   0        0        0     1970 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/data/replabels.py
--rw-r--r--   0        0        0     3775 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/datasets/asr_prep_json.py
--rwxr-xr-x   0        0        0     3822 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/datasets/prepare-librispeech.sh
--rw-r--r--   0        0        0    14704 2023-07-22 11:32:42.123794 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/infer.py
--rw-r--r--   0        0        0        0 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/kaldi/__init__.py
--rw-r--r--   0        0        0     2866 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/kaldi/add-self-loop-simple.cc
--rw-r--r--   0        0        0      109 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/kaldi/config/kaldi_initializer.yaml
--rw-r--r--   0        0        0     8265 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/kaldi/kaldi_decoder.py
--rw-r--r--   0        0        0    23441 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/kaldi/kaldi_initializer.py
--rw-r--r--   0        0        0      285 2023-07-22 11:41:08.360473 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/models/__init__.py
--rw-r--r--   0        0        0    37269 2023-07-22 11:24:53.713031 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/models/vggtransformer.py
--rw-r--r--   0        0        0     6078 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/models/w2l_conv_glu_enc.py
--rw-r--r--   0        0        0     1107 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/README.md
--rw-r--r--   0        0        0        0 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/__init__.py
--rw-r--r--   0        0        0      673 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/hydra/sweeper/ax.yaml
--rw-r--r--   0        0        0      676 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/hydra/sweeper/ax_sil.yaml
--rw-r--r--   0        0        0      551 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/infer.yaml
--rw-r--r--   0        0        0      765 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/run_config/fb_slurm_1.yaml
--rw-r--r--   0        0        0      738 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/run_config/fb_slurm_2g.yaml
--rw-r--r--   0        0        0        0 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/__init__.py
--rw-r--r--   0        0        0     2093 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/base_decoder.py
--rw-r--r--   0        0        0      944 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/decoder.py
--rw-r--r--   0        0        0     2004 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/decoder_config.py
--rw-r--r--   0        0        0    14870 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/flashlight_decoder.py
--rw-r--r--   0        0        0      641 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/viterbi_decoder.py
--rw-r--r--   0        0        0    17875 2023-07-22 11:24:44.078193 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/infer.py
--rw-r--r--   0        0        0      282 2023-07-22 11:41:18.681437 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/tasks/__init__.py
--rw-r--r--   0        0        0     5442 2023-07-22 11:33:17.238637 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/tasks/speech_recognition.py
--rw-r--r--   0        0        0    11842 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/utils/wer_utils.py
--rw-r--r--   0        0        0    17405 2023-07-22 11:23:33.342608 wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/w2l_decoder.py
--rw-r--r--   0        0        0     6857 2023-07-22 09:49:11.863142 wow_ai_mms-0.1.8/wow_ai_mms/models/tts.py
--rw-r--r--   0        0        0     4332 2023-07-22 09:49:11.863901 wow_ai_mms-0.1.8/wow_ai_mms/utils.py
--rw-r--r--   0        0        0     5257 1970-01-01 00:00:00.000000 wow_ai_mms-0.1.8/PKG-INFO
+-rw-r--r--   0        0        0    17529 2023-07-22 09:49:11.755219 wow_ai_mms-0.1.9/LICENSE
+-rw-r--r--   0        0        0     4825 2023-07-22 09:49:11.756724 wow_ai_mms-0.1.9/README.md
+-rw-r--r--   0        0        0      262 2023-07-23 08:21:16.933462 wow_ai_mms-0.1.9/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-22 09:49:11.836893 wow_ai_mms-0.1.9/wow_ai_mms/__init__.py
+-rw-r--r--   0        0        0      630 2023-07-22 09:49:11.837789 wow_ai_mms-0.1.9/wow_ai_mms/_logger.py
+-rw-r--r--   0        0        0     5845 2023-07-22 09:49:11.838755 wow_ai_mms-0.1.9/wow_ai_mms/constants.py
+-rw-r--r--   0        0        0     3264 2023-07-22 09:49:11.841220 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/MODEL_CARD.md
+-rw-r--r--   0        0        0    13987 2023-07-22 09:49:11.842872 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/README.md
+-rw-r--r--   0        0        0      697 2023-07-22 09:49:11.845855 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/asr/config/infer_common.yaml
+-rw-r--r--   0        0        0      671 2023-07-22 09:49:11.846862 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/asr/infer/example_infer_adapter.sh
+-rw-r--r--   0        0        0     2835 2023-07-22 09:49:11.848026 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/asr/infer/mms_infer.py
+-rw-r--r--   0        0        0     3366 2023-07-22 09:49:11.849095 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/README.md
+-rw-r--r--   0        0        0     6245 2023-07-23 08:21:03.016810 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/align_and_segment.py
+-rw-r--r--   0        0        0     5656 2023-07-22 09:49:11.851076 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/align_utils.py
+-rw-r--r--   0        0        0     6532 2023-07-22 09:49:11.852153 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/norm_config.py
+-rw-r--r--   0        0        0     6069 2023-07-22 09:49:11.853057 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/punctuations.lst
+-rw-r--r--   0        0        0       23 2023-07-23 08:06:37.144498 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/HEAD
+-rw-r--r--   0        0        0      302 2023-07-23 08:06:37.153959 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/config
+-rw-r--r--   0        0        0       73 2023-07-23 08:06:03.045164 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/description
+-rwxr-xr-x   0        0        0      478 2023-07-23 08:06:03.048651 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/applypatch-msg.sample
+-rwxr-xr-x   0        0        0      896 2023-07-23 08:06:03.046322 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/commit-msg.sample
+-rwxr-xr-x   0        0        0     4726 2023-07-23 08:06:03.049581 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/fsmonitor-watchman.sample
+-rwxr-xr-x   0        0        0      189 2023-07-23 08:06:03.051365 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/post-update.sample
+-rwxr-xr-x   0        0        0      424 2023-07-23 08:06:03.053734 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-applypatch.sample
+-rwxr-xr-x   0        0        0     1643 2023-07-23 08:06:03.048105 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-commit.sample
+-rwxr-xr-x   0        0        0      416 2023-07-23 08:06:03.052919 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-merge-commit.sample
+-rwxr-xr-x   0        0        0     1374 2023-07-23 08:06:03.054569 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-push.sample
+-rwxr-xr-x   0        0        0     4898 2023-07-23 08:06:03.047392 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-rebase.sample
+-rwxr-xr-x   0        0        0      544 2023-07-23 08:06:03.050218 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-receive.sample
+-rwxr-xr-x   0        0        0     1492 2023-07-23 08:06:03.050839 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/prepare-commit-msg.sample
+-rwxr-xr-x   0        0        0     2783 2023-07-23 08:06:03.055764 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/push-to-checkout.sample
+-rwxr-xr-x   0        0        0     3650 2023-07-23 08:06:03.055142 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/update.sample
+-rw-r--r--   0        0        0    24628 2023-07-23 08:09:03.469531 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/index
+-rw-r--r--   0        0        0      240 2023-07-23 08:06:03.043712 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/info/exclude
+-rw-r--r--   0        0        0      179 2023-07-23 08:06:37.149117 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/logs/HEAD
+-rw-r--r--   0        0        0      179 2023-07-23 08:06:37.150011 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/logs/refs/heads/master
+-rw-r--r--   0        0        0      179 2023-07-23 08:06:37.141912 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/logs/refs/remotes/origin/HEAD
+-rw-r--r--   0        0        0   601924 2023-07-23 08:06:37.090054 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/objects/pack/pack-7afb9b59823f4376441f898fda8968960e3a8c82.idx
+-rw-r--r--   0        0        0  7535521 2023-07-23 08:06:37.057164 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/objects/pack/pack-7afb9b59823f4376441f898fda8968960e3a8c82.pack
+-rw-r--r--   0        0        0     2159 2023-07-23 08:06:37.137820 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/packed-refs
+-rw-r--r--   0        0        0       41 2023-07-23 08:06:37.148235 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/refs/heads/master
+-rw-r--r--   0        0        0       32 2023-07-23 08:06:37.142089 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/refs/remotes/origin/HEAD
+-rw-r--r--   0        0        0      297 2023-07-23 08:06:37.174399 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.gitignore
+-rw-r--r--   0        0        0      308 2023-07-23 08:06:37.175367 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/AUTHORS
+-rw-r--r--   0        0        0      548 2023-07-23 08:06:37.175886 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/COPYING
+-rw-r--r--   0        0        0    82038 2023-07-23 08:06:37.178168 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/ChangeLog
+-rw-r--r--   0        0        0    77175 2023-07-23 08:06:37.179479 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/Doxyfile
+-rw-r--r--   0        0        0     5465 2023-07-23 08:06:37.180641 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/FEATURES.in
+-rw-r--r--   0        0        0     6346 2023-07-23 08:06:37.181272 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/INSTALL
+-rw-r--r--   0        0        0    17987 2023-07-23 08:06:37.182241 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/LICENSE.GPL
+-rw-r--r--   0        0        0    26436 2023-07-23 08:06:37.183879 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/LICENSE.LGPL
+-rw-r--r--   0        0        0     3752 2023-07-23 08:06:37.187778 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/Makefile.am
+-rw-r--r--   0        0        0      465 2023-07-23 08:06:37.188987 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/NEWS
+-rw-r--r--   0        0        0     4013 2023-07-23 08:06:37.190200 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/README.osx
+-rwxr-xr-x   0        0        0     2377 2023-07-23 08:06:37.191217 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/README.sh
+-rw-r--r--   0        0        0     5843 2023-07-23 08:06:37.191982 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/README.win32
+-rw-r--r--   0        0        0     5678 2023-07-23 08:06:37.192461 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/configure.ac
+-rwxr-xr-x   0        0        0     4033 2023-07-23 08:06:37.193045 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/cygbuild
+-rw-r--r--   0        0        0    15290 2023-07-23 08:06:37.194358 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/libsox.3
+-rw-r--r--   0        0        0       47 2023-07-23 08:06:37.195358 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/.gitignore
+-rw-r--r--   0        0        0      844 2023-07-23 08:06:37.195764 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/Makefile.am
+-rw-r--r--   0        0        0     2324 2023-07-23 08:06:37.196420 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/README
+-rw-r--r--   0        0        0     4090 2023-07-23 08:06:37.197041 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/README.lib
+-rw-r--r--   0        0        0    19502 2023-07-23 08:06:37.197869 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/analys.c
+-rw-r--r--   0        0        0       40 2023-07-23 08:06:37.199404 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/bitio.c
+-rw-r--r--   0        0        0       95 2023-07-23 08:06:37.200636 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/bitio.h
+-rw-r--r--   0        0        0    11717 2023-07-23 08:06:37.203225 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/bsynz.c
+-rw-r--r--   0        0        0     6701 2023-07-23 08:06:37.203801 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/chanwr.c
+-rw-r--r--   0        0        0     1910 2023-07-23 08:06:37.205067 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/dcbias.c
+-rw-r--r--   0        0        0    17236 2023-07-23 08:06:37.206355 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/decode.c
+-rw-r--r--   0        0        0     3455 2023-07-23 08:06:37.207279 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/deemp.c
+-rw-r--r--   0        0        0     2918 2023-07-23 08:06:37.207751 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/difmag.c
+-rw-r--r--   0        0        0    11418 2023-07-23 08:06:37.208191 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/dyptrk.c
+-rw-r--r--   0        0        0     9909 2023-07-23 08:06:37.208958 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/encode.c
+-rw-r--r--   0        0        0     1794 2023-07-23 08:06:37.210451 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/energy.c
+-rw-r--r--   0        0        0     4549 2023-07-23 08:06:37.211709 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/f2c.h
+-rw-r--r--   0        0        0     1309 2023-07-23 08:06:37.213299 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/f2clib.c
+-rw-r--r--   0        0        0     2797 2023-07-23 08:06:37.213958 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/ham84.c
+-rw-r--r--   0        0        0     2796 2023-07-23 08:06:37.215401 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/hp100.c
+-rw-r--r--   0        0        0     4205 2023-07-23 08:06:37.215984 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/invert.c
+-rw-r--r--   0        0        0     2458 2023-07-23 08:06:37.216448 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/irc2pc.c
+-rw-r--r--   0        0        0     2785 2023-07-23 08:06:37.217239 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/ivfilt.c
+-rw-r--r--   0        0        0     8708 2023-07-23 08:06:37.220442 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpc10.h
+-rw-r--r--   0        0        0     6973 2023-07-23 08:06:37.221249 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcdec.c
+-rw-r--r--   0        0        0     3455 2023-07-23 08:06:37.221711 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcenc.c
+-rw-r--r--   0        0        0     9540 2023-07-23 08:06:37.222230 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcini.c
+-rw-r--r--   0        0        0     2878 2023-07-23 08:06:37.223955 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpfilt.c
+-rw-r--r--   0        0        0     1258 2023-07-23 08:06:37.224535 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/median.c
+-rw-r--r--   0        0        0     4446 2023-07-23 08:06:37.225308 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/mload.c
+-rw-r--r--   0        0        0     8824 2023-07-23 08:06:37.226058 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/onset.c
+-rw-r--r--   0        0        0    16158 2023-07-23 08:06:37.226619 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/pitsyn.c
+-rw-r--r--   0        0        0     7658 2023-07-23 08:06:37.227115 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/placea.c
+-rw-r--r--   0        0        0     7761 2023-07-23 08:06:37.227570 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/placev.c
+-rw-r--r--   0        0        0     3452 2023-07-23 08:06:37.228077 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/preemp.c
+-rw-r--r--   0        0        0     2487 2023-07-23 08:06:37.228531 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/prepro.c
+-rw-r--r--   0        0        0     2605 2023-07-23 08:06:37.228990 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/random.c
+-rw-r--r--   0        0        0     2277 2023-07-23 08:06:37.229510 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/rcchk.c
+-rw-r--r--   0        0        0    11585 2023-07-23 08:06:37.230031 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/synths.c
+-rw-r--r--   0        0        0     4950 2023-07-23 08:06:37.230442 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/tbdm.c
+-rw-r--r--   0        0        0    26833 2023-07-23 08:06:37.232937 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/voicin.c
+-rw-r--r--   0        0        0     8044 2023-07-23 08:06:37.233616 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/vparms.c
+-rw-r--r--   0        0        0       63 2023-07-23 08:06:37.234200 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/m4/.gitignore
+-rw-r--r--   0        0        0     8953 2023-07-23 08:06:37.234633 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/m4/sox.m4
+-rwxr-xr-x   0        0        0     4615 2023-07-23 08:06:37.235075 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/mingwbuild
+-rwxr-xr-x   0        0        0     6030 2023-07-23 08:06:37.235442 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/osxbuild
+-rwxr-xr-x   0        0        0     8371 2023-07-23 08:06:37.236661 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/release.sh
+-rw-r--r--   0        0        0     1431 2023-07-23 08:06:37.236994 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/screenshot1
+-rwxr-xr-x   0        0        0     1618 2023-07-23 08:06:37.238066 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/alert.sh
+-rw-r--r--   0        0        0      520 2023-07-23 08:06:37.238456 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/batch-example.bat
+-rwxr-xr-x   0        0        0     4978 2023-07-23 08:06:37.240477 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/crossfade.sh
+-rwxr-xr-x   0        0        0     4248 2023-07-23 08:06:37.241585 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/crossfade_cat.sh
+-rwxr-xr-x   0        0        0     4969 2023-07-23 08:06:37.245639 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/synth.sh
+-rwxr-xr-x   0        0        0     5629 2023-07-23 08:06:37.246163 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/testcd.sh
+-rwxr-xr-x   0        0        0     7684 2023-07-23 08:06:37.247249 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/testtones.sh
+-rwxr-xr-x   0        0        0      563 2023-07-23 08:06:37.249225 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/voice-cleanup.sh
+-rw-r--r--   0        0        0   149613 2023-07-23 08:06:37.254223 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/sox.1
+-rw-r--r--   0        0        0      264 2023-07-23 08:06:37.257506 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/sox.pc.in
+-rw-r--r--   0        0        0    27442 2023-07-23 08:06:37.258196 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/soxformat.7
+-rw-r--r--   0        0        0     3236 2023-07-23 08:06:37.258666 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/soxi.1
+-rw-r--r--   0        0        0      193 2023-07-23 08:06:37.259150 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/.gitignore
+-rw-r--r--   0        0        0    12163 2023-07-23 08:06:37.259733 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/8svx.c
+-rw-r--r--   0        0        0     5667 2023-07-23 08:06:37.260576 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/Makefile.am
+-rw-r--r--   0        0        0    12598 2023-07-23 08:06:37.261262 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/adpcm.c
+-rw-r--r--   0        0        0     2839 2023-07-23 08:06:37.261855 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/adpcm.h
+-rw-r--r--   0        0        0    11172 2023-07-23 08:06:37.262403 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/adpcms.c
+-rw-r--r--   0        0        0     1989 2023-07-23 08:06:37.263255 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/adpcms.h
+-rw-r--r--   0        0        0     1443 2023-07-23 08:06:37.264375 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/aifc-fmt.c
+-rw-r--r--   0        0        0     1377 2023-07-23 08:06:37.264796 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/aiff-fmt.c
+-rw-r--r--   0        0        0    39580 2023-07-23 08:06:37.266126 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/aiff.c
+-rw-r--r--   0        0        0      916 2023-07-23 08:06:37.266622 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/aiff.h
+-rw-r--r--   0        0        0      875 2023-07-23 08:06:37.267020 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/al-fmt.c
+-rw-r--r--   0        0        0    13558 2023-07-23 08:06:37.267708 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/alsa.c
+-rw-r--r--   0        0        0     3350 2023-07-23 08:06:37.269319 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/amr-nb.c
+-rw-r--r--   0        0        0     3643 2023-07-23 08:06:37.270326 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/amr-wb.c
+-rw-r--r--   0        0        0     8412 2023-07-23 08:06:37.271263 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/amr.h
+-rw-r--r--   0        0        0     3760 2023-07-23 08:06:37.272366 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ao.c
+-rw-r--r--   0        0        0     9412 2023-07-23 08:06:37.273028 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/au.c
+-rw-r--r--   0        0        0     7106 2023-07-23 08:06:37.274502 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/avr.c
+-rw-r--r--   0        0        0     1801 2023-07-23 08:06:37.275013 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/band.h
+-rw-r--r--   0        0        0    11272 2023-07-23 08:06:37.275774 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bend.c
+-rw-r--r--   0        0        0     5990 2023-07-23 08:06:37.276370 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/biquad.c
+-rw-r--r--   0        0        0     2377 2023-07-23 08:06:37.276740 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/biquad.h
+-rw-r--r--   0        0        0    13920 2023-07-23 08:06:37.277214 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/biquads.c
+-rw-r--r--   0        0        0     8547 2023-07-23 08:06:37.278002 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/CoreAudio/CoreAudio.h
+-rw-r--r--   0        0        0        0 2023-07-23 08:06:37.278136 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/mmreg.h
+-rw-r--r--   0        0        0     2312 2023-07-23 08:06:37.278442 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/mmsystem.h
+-rw-r--r--   0        0        0     4581 2023-07-23 08:06:37.280281 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/sndio.h
+-rw-r--r--   0        0        0     8806 2023-07-23 08:06:37.280848 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/sys/audioio.h
+-rw-r--r--   0        0        0      725 2023-07-23 08:06:37.281106 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/windows.h
+-rw-r--r--   0        0        0     1332 2023-07-23 08:06:37.281529 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/caf.c
+-rw-r--r--   0        0        0     1852 2023-07-23 08:06:37.281933 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cdr.c
+-rw-r--r--   0        0        0    13028 2023-07-23 08:06:37.282765 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/chorus.c
+-rw-r--r--   0        0        0    10057 2023-07-23 08:06:37.283070 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/compand.c
+-rw-r--r--   0        0        0     6762 2023-07-23 08:06:37.283330 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/compandt.c
+-rw-r--r--   0        0        0     1768 2023-07-23 08:06:37.283690 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/compandt.h
+-rw-r--r--   0        0        0     1800 2023-07-23 08:06:37.284224 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/contrast.c
+-rw-r--r--   0        0        0    12342 2023-07-23 08:06:37.284664 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/coreaudio.c
+-rwxr-xr-x   0        0        0     2168 2023-07-23 08:06:37.284965 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/csox
+-rw-r--r--   0        0        0     3678 2023-07-23 08:06:37.285331 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd-fmt.c
+-rw-r--r--   0        0        0    23370 2023-07-23 08:06:37.286815 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd.c
+-rw-r--r--   0        0        0     2312 2023-07-23 08:06:37.288647 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd.h
+-rw-r--r--   0        0        0     5160 2023-07-23 08:06:37.289463 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cvsdfilt.h
+-rw-r--r--   0        0        0     4685 2023-07-23 08:06:37.290439 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dat.c
+-rw-r--r--   0        0        0     4982 2023-07-23 08:06:37.291291 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dcshift.c
+-rw-r--r--   0        0        0     3602 2023-07-23 08:06:37.292512 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/deemph.plt
+-rw-r--r--   0        0        0     5007 2023-07-23 08:06:37.292944 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/delay.c
+-rw-r--r--   0        0        0     4386 2023-07-23 08:06:37.293334 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dft_filter.c
+-rw-r--r--   0        0        0      396 2023-07-23 08:06:37.293653 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dft_filter.h
+-rw-r--r--   0        0        0    15076 2023-07-23 08:06:37.294212 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dither.c
+-rw-r--r--   0        0        0     2076 2023-07-23 08:06:37.296206 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dither.h
+-rw-r--r--   0        0        0     2351 2023-07-23 08:06:37.296826 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/divide.c
+-rw-r--r--   0        0        0     2553 2023-07-23 08:06:37.298464 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/downsample.c
+-rw-r--r--   0        0        0     1373 2023-07-23 08:06:37.299182 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dvms-fmt.c
+-rw-r--r--   0        0        0     4246 2023-07-23 08:06:37.299798 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/earwax.c
+-rw-r--r--   0        0        0     9330 2023-07-23 08:06:37.303055 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/echo.c
+-rw-r--r--   0        0        0     9998 2023-07-23 08:06:37.304650 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/echos.c
+-rw-r--r--   0        0        0    23109 2023-07-23 08:06:37.306343 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/effects.c
+-rw-r--r--   0        0        0     2031 2023-07-23 08:06:37.307058 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/effects.h
+-rw-r--r--   0        0        0    13239 2023-07-23 08:06:37.311620 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/effects_i.c
+-rw-r--r--   0        0        0    19837 2023-07-23 08:06:37.313686 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/effects_i_dsp.c
+-rw-r--r--   0        0        0     3869 2023-07-23 08:06:37.314414 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example0.c
+-rw-r--r--   0        0        0     6433 2023-07-23 08:06:37.317685 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example1.c
+-rw-r--r--   0        0        0     4441 2023-07-23 08:06:37.318206 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example2.c
+-rw-r--r--   0        0        0     3963 2023-07-23 08:06:37.318713 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example3.c
+-rw-r--r--   0        0        0     3758 2023-07-23 08:06:37.320594 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example4.c
+-rw-r--r--   0        0        0     2723 2023-07-23 08:06:37.321129 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example5.c
+-rw-r--r--   0        0        0     3948 2023-07-23 08:06:37.322191 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example6.c
+-rw-r--r--   0        0        0      887 2023-07-23 08:06:37.322589 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/f4-fmt.c
+-rw-r--r--   0        0        0      887 2023-07-23 08:06:37.323558 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/f8-fmt.c
+-rw-r--r--   0        0        0    11978 2023-07-23 08:06:37.324465 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fade.c
+-rw-r--r--   0        0        0     1260 2023-07-23 08:06:37.325162 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fap.c
+-rw-r--r--   0        0        0    37607 2023-07-23 08:06:37.325842 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fft4g.c
+-rw-r--r--   0        0        0     1667 2023-07-23 08:06:37.326253 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fft4g.h
+-rw-r--r--   0        0        0     2922 2023-07-23 08:06:37.326888 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fifo.h
+-rw-r--r--   0        0        0     3371 2023-07-23 08:06:37.327418 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fir.c
+-rw-r--r--   0        0        0     4643 2023-07-23 08:06:37.327769 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/firfit.c
+-rw-r--r--   0        0        0    20871 2023-07-23 08:06:37.328484 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/flac.c
+-rw-r--r--   0        0        0     8553 2023-07-23 08:06:37.328958 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/flanger.c
+-rw-r--r--   0        0        0    43364 2023-07-23 08:06:37.330025 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/formats.c
+-rw-r--r--   0        0        0     3530 2023-07-23 08:06:37.330425 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/formats.h
+-rw-r--r--   0        0        0    16895 2023-07-23 08:06:37.330943 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/formats_i.c
+-rw-r--r--   0        0        0   165842 2023-07-23 08:06:37.334262 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g711.c
+-rw-r--r--   0        0        0      934 2023-07-23 08:06:37.338671 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g711.h
+-rw-r--r--   0        0        0     5316 2023-07-23 08:06:37.339427 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g721.c
+-rw-r--r--   0        0        0     4695 2023-07-23 08:06:37.340122 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g723_24.c
+-rw-r--r--   0        0        0     5582 2023-07-23 08:06:37.340757 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g723_40.c
+-rw-r--r--   0        0        0    21238 2023-07-23 08:06:37.342153 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g72x.c
+-rw-r--r--   0        0        0     4861 2023-07-23 08:06:37.342872 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g72x.h
+-rw-r--r--   0        0        0     9592 2023-07-23 08:06:37.343626 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/gain.c
+-rw-r--r--   0        0        0    11726 2023-07-23 08:06:37.344339 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/getopt.c
+-rw-r--r--   0        0        0     7017 2023-07-23 08:06:37.344774 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/gsm.c
+-rw-r--r--   0        0        0     6471 2023-07-23 08:06:37.345239 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/gsrt.c
+-rw-r--r--   0        0        0    15310 2023-07-23 08:06:37.346004 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/hcom.c
+-rw-r--r--   0        0        0     3205 2023-07-23 08:06:37.346483 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/hilbert.c
+-rw-r--r--   0        0        0     3128 2023-07-23 08:06:37.346858 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/htk.c
+-rw-r--r--   0        0        0     6146 2023-07-23 08:06:37.347238 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/id3.c
+-rw-r--r--   0        0        0      935 2023-07-23 08:06:37.347606 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/id3.h
+-rw-r--r--   0        0        0     1329 2023-07-23 08:06:37.348136 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ima-fmt.c
+-rw-r--r--   0        0        0    13813 2023-07-23 08:06:37.348694 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ima_rw.c
+-rw-r--r--   0        0        0     3166 2023-07-23 08:06:37.349155 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ima_rw.h
+-rw-r--r--   0        0        0     2087 2023-07-23 08:06:37.349630 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/input.c
+-rw-r--r--   0        0        0      892 2023-07-23 08:06:37.350122 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/la-fmt.c
+-rw-r--r--   0        0        0    15801 2023-07-23 08:06:37.352784 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ladspa.c
+-rw-r--r--   0        0        0    27595 2023-07-23 08:06:37.353531 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ladspa.h
+-rw-r--r--   0        0        0     6147 2023-07-23 08:06:37.354433 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/libsox.c
+-rw-r--r--   0        0        0     1575 2023-07-23 08:06:37.354812 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/libsox.sym
+-rw-r--r--   0        0        0     3264 2023-07-23 08:06:37.355283 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/libsox_i.c
+-rw-r--r--   0        0        0     4669 2023-07-23 08:06:37.355770 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/loudness.c
+-rw-r--r--   0        0        0     6729 2023-07-23 08:06:37.356307 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/lpc10.c
+-rw-r--r--   0        0        0      892 2023-07-23 08:06:37.356787 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/lu-fmt.c
+-rw-r--r--   0        0        0     1275 2023-07-23 08:06:37.357132 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mat4.c
+-rw-r--r--   0        0        0     1268 2023-07-23 08:06:37.357440 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mat5.c
+-rw-r--r--   0        0        0    11620 2023-07-23 08:06:37.357981 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/maud.c
+-rw-r--r--   0        0        0    16130 2023-07-23 08:06:37.359233 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mcompand.c
+-rw-r--r--   0        0        0     3704 2023-07-23 08:06:37.359716 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mcompand_xover.h
+-rw-r--r--   0        0        0     1670 2023-07-23 08:06:37.360259 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/monkey.wav
+-rw-r--r--   0        0        0     6478 2023-07-23 08:06:37.360733 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mp3-util.h
+-rw-r--r--   0        0        0    40627 2023-07-23 08:06:37.361681 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mp3.c
+-rw-r--r--   0        0        0     6065 2023-07-23 08:06:37.362323 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/noiseprof.c
+-rw-r--r--   0        0        0    10178 2023-07-23 08:06:37.362939 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/noisered.c
+-rw-r--r--   0        0        0     1028 2023-07-23 08:06:37.363369 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/noisered.h
+-rw-r--r--   0        0        0     2086 2023-07-23 08:06:37.364113 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/nulfile.c
+-rw-r--r--   0        0        0     7151 2023-07-23 08:06:37.364673 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/optional-fmts.am
+-rw-r--r--   0        0        0     5903 2023-07-23 08:06:37.365131 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/opus.c
+-rw-r--r--   0        0        0    14635 2023-07-23 08:06:37.366307 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/oss.c
+-rw-r--r--   0        0        0     2120 2023-07-23 08:06:37.367121 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/output.c
+-rw-r--r--   0        0        0     2266 2023-07-23 08:06:37.367506 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/overdrive.c
+-rw-r--r--   0        0        0     6005 2023-07-23 08:06:37.368009 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/pad.c
+-rw-r--r--   0        0        0     1257 2023-07-23 08:06:37.368364 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/paf.c
+-rw-r--r--   0        0        0     4595 2023-07-23 08:06:37.368754 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/phaser.c
+-rw-r--r--   0        0        0    14458 2023-07-23 08:06:37.369395 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/prc.c
+-rw-r--r--   0        0        0     3854 2023-07-23 08:06:37.369802 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/pulseaudio.c
+-rw-r--r--   0        0        0     1219 2023-07-23 08:06:37.370148 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/pvf.c
+-rw-r--r--   0        0        0    26724 2023-07-23 08:06:37.370707 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate.c
+-rw-r--r--   0        0        0     6398 2023-07-23 08:06:37.371075 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate_filters.h
+-rw-r--r--   0        0        0     1474 2023-07-23 08:06:37.371376 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate_half_fir.h
+-rw-r--r--   0        0        0     3190 2023-07-23 08:06:37.371574 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate_poly_fir.h
+-rw-r--r--   0        0        0     1856 2023-07-23 08:06:37.372001 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate_poly_fir0.h
+-rw-r--r--   0        0        0     2145 2023-07-23 08:06:37.372302 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/raw-fmt.c
+-rw-r--r--   0        0        0     7874 2023-07-23 08:06:37.372581 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/raw.c
+-rw-r--r--   0        0        0     2278 2023-07-23 08:06:37.372899 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/raw.h
+-rw-r--r--   0        0        0     9453 2023-07-23 08:06:37.373114 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/remix.c
+-rw-r--r--   0        0        0     3686 2023-07-23 08:06:37.373440 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/repeat.c
+-rw-r--r--   0        0        0     9071 2023-07-23 08:06:37.373769 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/reverb.c
+-rw-r--r--   0        0        0     2416 2023-07-23 08:06:37.374020 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/reverse.c
+-rw-r--r--   0        0        0      891 2023-07-23 08:06:37.374297 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/s1-fmt.c
+-rw-r--r--   0        0        0      893 2023-07-23 08:06:37.374736 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/s2-fmt.c
+-rw-r--r--   0        0        0      887 2023-07-23 08:06:37.375019 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/s3-fmt.c
+-rw-r--r--   0        0        0      893 2023-07-23 08:06:37.375282 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/s4-fmt.c
+-rw-r--r--   0        0        0     1215 2023-07-23 08:06:37.375862 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sd2.c
+-rw-r--r--   0        0        0     6043 2023-07-23 08:06:37.376213 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sf.c
+-rw-r--r--   0        0        0    24152 2023-07-23 08:06:37.376702 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/silence.c
+-rw-r--r--   0        0        0     5208 2023-07-23 08:06:37.377075 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sinc.c
+-rw-r--r--   0        0        0     3690 2023-07-23 08:06:37.377537 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/skeleff.c
+-rw-r--r--   0        0        0     6165 2023-07-23 08:06:37.377842 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/skelform.c
+-rw-r--r--   0        0        0    15514 2023-07-23 08:06:37.378204 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/smp.c
+-rw-r--r--   0        0        0    18260 2023-07-23 08:06:37.378614 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sndfile.c
+-rw-r--r--   0        0        0     6557 2023-07-23 08:06:37.379057 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sndio.c
+-rw-r--r--   0        0        0     2071 2023-07-23 08:06:37.379372 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sounder.c
+-rw-r--r--   0        0        0     3290 2023-07-23 08:06:37.379689 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/soundtool.c
+-rw-r--r--   0        0        0     4001 2023-07-23 08:06:37.380309 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox-fmt.c
+-rw-r--r--   0        0        0   102002 2023-07-23 08:06:37.381961 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox.c
+-rw-r--r--   0        0        0    91627 2023-07-23 08:06:37.385160 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox.h
+-rw-r--r--   0        0        0    17985 2023-07-23 08:06:37.386589 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox_i.h
+-rw-r--r--   0        0        0     7349 2023-07-23 08:06:37.387035 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox_sample_test.c
+-rw-r--r--   0        0        0     1153 2023-07-23 08:06:37.387350 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/soxomp.h
+-rw-r--r--   0        0        0    33632 2023-07-23 08:06:37.387796 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/spectrogram.c
+-rw-r--r--   0        0        0     2300 2023-07-23 08:06:37.388196 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/speed.c
+-rw-r--r--   0        0        0    11591 2023-07-23 08:06:37.388651 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/speexdsp.c
+-rw-r--r--   0        0        0     6626 2023-07-23 08:06:37.388942 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sphere.c
+-rw-r--r--   0        0        0    10728 2023-07-23 08:06:37.389158 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/splice.c
+-rw-r--r--   0        0        0     9036 2023-07-23 08:06:37.389571 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/stat.c
+-rw-r--r--   0        0        0    10006 2023-07-23 08:06:37.389986 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/stats.c
+-rw-r--r--   0        0        0     8263 2023-07-23 08:06:37.390276 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/stretch.c
+-rw-r--r--   0        0        0    16768 2023-07-23 08:06:37.391006 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sunaudio.c
+-rw-r--r--   0        0        0     1834 2023-07-23 08:06:37.391452 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/swap.c
+-rw-r--r--   0        0        0    22155 2023-07-23 08:06:37.392249 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/synth.c
+-rw-r--r--   0        0        0    12311 2023-07-23 08:06:37.392720 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tempo.c
+-rwxr-xr-x   0        0        0     1724 2023-07-23 08:06:37.392994 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/test-comments
+-rwxr-xr-x   0        0        0     1326 2023-07-23 08:06:37.393358 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/test-srcs
+-rw-r--r--   0        0        0     1182 2023-07-23 08:06:37.393638 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/testall.bat
+-rwxr-xr-x   0        0        0      967 2023-07-23 08:06:37.393865 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/testall.sh
+-rw-r--r--   0        0        0     1356 2023-07-23 08:06:37.394066 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tests.bat
+-rwxr-xr-x   0        0        0     7452 2023-07-23 08:06:37.394483 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tests.sh
+-rw-r--r--   0        0        0     1727 2023-07-23 08:06:37.394721 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tremolo.c
+-rw-r--r--   0        0        0     6852 2023-07-23 08:06:37.394989 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/trim.c
+-rw-r--r--   0        0        0    12100 2023-07-23 08:06:37.395290 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tx16w.c
+-rw-r--r--   0        0        0      909 2023-07-23 08:06:37.395556 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/u1-fmt.c
+-rw-r--r--   0        0        0      896 2023-07-23 08:06:37.396321 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/u2-fmt.c
+-rw-r--r--   0        0        0      890 2023-07-23 08:06:37.396803 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/u3-fmt.c
+-rw-r--r--   0        0        0      890 2023-07-23 08:06:37.397104 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/u4-fmt.c
+-rw-r--r--   0        0        0      877 2023-07-23 08:06:37.397417 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ul-fmt.c
+-rw-r--r--   0        0        0     2171 2023-07-23 08:06:37.397682 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/upsample.c
+-rw-r--r--   0        0        0     8569 2023-07-23 08:06:37.397940 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/util.c
+-rw-r--r--   0        0        0     4821 2023-07-23 08:06:37.398195 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/util.h
+-rw-r--r--   0        0        0    13117 2023-07-23 08:06:37.398483 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vad.c
+-rw-r--r--   0        0        0    23493 2023-07-23 08:06:37.399620 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-N.s8
+-rw-r--r--   0        0        0    23493 2023-07-23 08:06:37.400342 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-X.s8
+-rw-r--r--   0        0        0    23493 2023-07-23 08:06:37.400835 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-X_-N.s8
+-rw-r--r--   0        0        0    23493 2023-07-23 08:06:37.402974 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_.s8
+-rw-r--r--   0        0        0    29211 2023-07-23 08:06:37.403733 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/voc.c
+-rw-r--r--   0        0        0     5695 2023-07-23 08:06:37.404356 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vol.c
+-rw-r--r--   0        0        0    11579 2023-07-23 08:06:37.404845 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vorbis.c
+-rw-r--r--   0        0        0     1349 2023-07-23 08:06:37.405388 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vox-fmt.c
+-rw-r--r--   0        0        0     1269 2023-07-23 08:06:37.405830 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vox.c
+-rw-r--r--   0        0        0     1097 2023-07-23 08:06:37.406213 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vox.h
+-rw-r--r--   0        0        0     1452 2023-07-23 08:06:37.406624 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/w64.c
+-rw-r--r--   0        0        0    54729 2023-07-23 08:06:37.408095 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/wav.c
+-rw-r--r--   0        0        0    14964 2023-07-23 08:06:37.408759 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/waveaudio.c
+-rw-r--r--   0        0        0     7371 2023-07-23 08:06:37.409113 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/wavpack.c
+-rw-r--r--   0        0        0     3838 2023-07-23 08:06:37.409798 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/win32/glob.c
+-rw-r--r--   0        0        0     1208 2023-07-23 08:06:37.410168 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/win32/glob.h
+-rw-r--r--   0        0        0     2348 2023-07-23 08:06:37.410513 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/wve.c
+-rw-r--r--   0        0        0    10794 2023-07-23 08:06:37.410991 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/xa.c
+-rw-r--r--   0        0        0     1205 2023-07-23 08:06:37.411337 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/xi.c
+-rw-r--r--   0        0        0     1944 2023-07-23 08:06:37.411737 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/xmalloc.c
+-rw-r--r--   0        0        0     1438 2023-07-23 08:06:37.412554 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/xmalloc.h
+-rw-r--r--   0        0        0      383 2023-07-23 08:06:37.413088 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/Makefile
+-rw-r--r--   0        0        0     3471 2023-07-23 08:06:37.413697 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/README
+-rw-r--r--   0        0        0     4121 2023-07-23 08:06:37.414124 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/corr.c
+-rwxr-xr-x   0        0        0     3545 2023-07-23 08:06:37.414829 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/ltest.pl
+-rw-r--r--   0        0        0     6717 2023-07-23 08:06:37.415327 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/model.c
+-rw-r--r--   0        0        0      330 2023-07-23 08:06:37.416399 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/plotA
+-rw-r--r--   0        0        0      465 2023-07-23 08:06:37.416962 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/plotAB
+-rw-r--r--   0        0        0      337 2023-07-23 08:06:37.417446 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/responseAB
+-rwxr-xr-x   0        0        0     2971 2023-07-23 08:06:37.417735 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/wtest.pl
+-rw-r--r--   0        0        0     2790 2023-07-23 07:09:07.609855 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/text_normalization.py
+-rw-r--r--   0        0        0     7071 2023-07-22 09:49:11.855224 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/lid/infer.py
+-rw-r--r--   0        0        0      808 2023-07-22 09:49:11.856391 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/misc/get_sample_size.py
+-rw-r--r--   0        0        0     5802 2023-07-22 09:49:11.857738 wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/tts/infer.py
+-rw-r--r--   0        0        0        1 2023-07-22 09:49:11.858761 wow_ai_mms-0.1.9/wow_ai_mms/models/__init__.py
+-rw-r--r--   0        0        0     7711 2023-07-23 06:30:49.679854 wow_ai_mms-0.1.9/wow_ai_mms/models/alignment.py
+-rw-r--r--   0        0        0     9510 2023-07-22 11:19:05.801050 wow_ai_mms-0.1.9/wow_ai_mms/models/asr.py
+-rw-r--r--   0        0        0     5706 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/README.md
+-rw-r--r--   0        0        0       48 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/__init__.py
+-rw-r--r--   0        0        0     5879 2023-07-22 11:25:26.672742 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/criterions/ASG_loss.py
+-rw-r--r--   0        0        0      519 2023-07-22 11:40:04.527684 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/criterions/__init__.py
+-rw-r--r--   0        0        0     5372 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/criterions/cross_entropy_acc.py
+-rw-r--r--   0        0        0      248 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/data/__init__.py
+-rw-r--r--   0        0        0     3955 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/data/asr_dataset.py
+-rw-r--r--   0        0        0     4796 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/data/collaters.py
+-rw-r--r--   0        0        0     3429 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/data/data_utils.py
+-rw-r--r--   0        0        0     1970 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/data/replabels.py
+-rw-r--r--   0        0        0     3775 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/datasets/asr_prep_json.py
+-rwxr-xr-x   0        0        0     3822 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/datasets/prepare-librispeech.sh
+-rw-r--r--   0        0        0    14704 2023-07-22 11:32:42.123794 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/infer.py
+-rw-r--r--   0        0        0        0 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/kaldi/__init__.py
+-rw-r--r--   0        0        0     2866 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/kaldi/add-self-loop-simple.cc
+-rw-r--r--   0        0        0      109 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/kaldi/config/kaldi_initializer.yaml
+-rw-r--r--   0        0        0     8265 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/kaldi/kaldi_decoder.py
+-rw-r--r--   0        0        0    23441 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/kaldi/kaldi_initializer.py
+-rw-r--r--   0        0        0      285 2023-07-22 11:41:08.360473 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/models/__init__.py
+-rw-r--r--   0        0        0    37269 2023-07-22 11:24:53.713031 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/models/vggtransformer.py
+-rw-r--r--   0        0        0     6078 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/models/w2l_conv_glu_enc.py
+-rw-r--r--   0        0        0     1107 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/README.md
+-rw-r--r--   0        0        0        0 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/__init__.py
+-rw-r--r--   0        0        0      673 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/hydra/sweeper/ax.yaml
+-rw-r--r--   0        0        0      676 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/hydra/sweeper/ax_sil.yaml
+-rw-r--r--   0        0        0      551 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/infer.yaml
+-rw-r--r--   0        0        0      765 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/run_config/fb_slurm_1.yaml
+-rw-r--r--   0        0        0      738 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/run_config/fb_slurm_2g.yaml
+-rw-r--r--   0        0        0        0 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/__init__.py
+-rw-r--r--   0        0        0     2093 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/base_decoder.py
+-rw-r--r--   0        0        0      944 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/decoder.py
+-rw-r--r--   0        0        0     2004 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/decoder_config.py
+-rw-r--r--   0        0        0    14870 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/flashlight_decoder.py
+-rw-r--r--   0        0        0      641 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/viterbi_decoder.py
+-rw-r--r--   0        0        0    17875 2023-07-22 11:24:44.078193 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/infer.py
+-rw-r--r--   0        0        0      282 2023-07-22 11:41:18.681437 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/tasks/__init__.py
+-rw-r--r--   0        0        0     5442 2023-07-22 11:33:17.238637 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/tasks/speech_recognition.py
+-rw-r--r--   0        0        0    11842 2023-06-23 17:31:52.000000 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/utils/wer_utils.py
+-rw-r--r--   0        0        0    17405 2023-07-22 11:23:33.342608 wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/w2l_decoder.py
+-rw-r--r--   0        0        0     6857 2023-07-22 09:49:11.863142 wow_ai_mms-0.1.9/wow_ai_mms/models/tts.py
+-rw-r--r--   0        0        0     4332 2023-07-22 09:49:11.863901 wow_ai_mms-0.1.9/wow_ai_mms/utils.py
+-rw-r--r--   0        0        0     5257 1970-01-01 00:00:00.000000 wow_ai_mms-0.1.9/PKG-INFO
```

### Comparing `wow_ai_mms-0.1.8/LICENSE` & `wow_ai_mms-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/README.md` & `wow_ai_mms-0.1.9/README.md`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/_logger.py` & `wow_ai_mms-0.1.9/wow_ai_mms/_logger.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/constants.py` & `wow_ai_mms-0.1.9/wow_ai_mms/constants.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/MODEL_CARD.md` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/MODEL_CARD.md`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/README.md` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/README.md`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/asr/config/infer_common.yaml` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/asr/config/infer_common.yaml`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/asr/infer/example_infer_adapter.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/asr/infer/example_infer_adapter.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/asr/infer/mms_infer.py` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/asr/infer/mms_infer.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/README.md` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/README.md`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/align_and_segment.py` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/align_and_segment.py`

 * *Files 0% similar despite different names*

```diff
@@ -21,16 +21,16 @@
 DEVICE = torch.device('cuda' if torch.cuda.is_available() else 'cpu')
 
 def generate_emissions(model, audio_file):
     waveform, _ = torchaudio.load(audio_file)  # waveform: channels X T
     waveform = waveform.to(DEVICE)
     total_duration = float(ffmpeg.probe(audio_file)["format"]["duration"])  #sox.file_info.duration(audio_file)
 
-    audio_sf = float(ffmpeg.probe(audio_file)["format"]["bit_rate"]) #sox.file_info.sample_rate(audio_file)
-    assert audio_sf == SAMPLING_FREQ
+    # audio_sf = float(ffmpeg.probe(audio_file)["format"]["bit_rate"]) #sox.file_info.sample_rate(audio_file)
+    # assert audio_sf == SAMPLING_FREQ
 
     emissions_arr = []
     with torch.inference_mode():
         i = 0
         while i < total_duration:
             segment_start_time, segment_end_time = (i, i + EMISSION_INTERVAL)
```

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/align_utils.py` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/align_utils.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/norm_config.py` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/norm_config.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/punctuations.lst` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/punctuations.lst`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/commit-msg.sample` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/commit-msg.sample`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/fsmonitor-watchman.sample` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/fsmonitor-watchman.sample`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-commit.sample` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-commit.sample`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-push.sample` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-push.sample`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-rebase.sample` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-rebase.sample`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-receive.sample` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/pre-receive.sample`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/prepare-commit-msg.sample` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/prepare-commit-msg.sample`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/push-to-checkout.sample` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/push-to-checkout.sample`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/update.sample` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/hooks/update.sample`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/index` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/index`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/objects/pack/pack-7afb9b59823f4376441f898fda8968960e3a8c82.idx` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/objects/pack/pack-7afb9b59823f4376441f898fda8968960e3a8c82.idx`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/objects/pack/pack-7afb9b59823f4376441f898fda8968960e3a8c82.pack` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/objects/pack/pack-7afb9b59823f4376441f898fda8968960e3a8c82.pack`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/.git/packed-refs` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/.git/packed-refs`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/COPYING` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/COPYING`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/ChangeLog` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/ChangeLog`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/Doxyfile` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/Doxyfile`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/FEATURES.in` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/FEATURES.in`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/INSTALL` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/INSTALL`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/LICENSE.GPL` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/LICENSE.GPL`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/LICENSE.LGPL` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/LICENSE.LGPL`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/Makefile.am` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/Makefile.am`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/README.osx` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/README.osx`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/README.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/README.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/README.win32` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/README.win32`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/configure.ac` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/configure.ac`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/cygbuild` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/cygbuild`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/libsox.3` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/libsox.3`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/Makefile.am` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/Makefile.am`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/README` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/README`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/README.lib` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/README.lib`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/analys.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/analys.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/bsynz.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/bsynz.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/chanwr.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/chanwr.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/dcbias.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/dcbias.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/decode.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/decode.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/deemp.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/deemp.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/difmag.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/difmag.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/dyptrk.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/dyptrk.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/encode.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/encode.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/energy.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/energy.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/f2c.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/f2c.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/f2clib.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/f2clib.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/ham84.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/ham84.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/hp100.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/hp100.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/invert.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/invert.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/irc2pc.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/irc2pc.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/ivfilt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/ivfilt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpc10.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpc10.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcdec.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcdec.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcenc.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcenc.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcini.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpcini.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpfilt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/lpfilt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/median.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/median.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/mload.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/mload.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/onset.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/onset.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/pitsyn.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/pitsyn.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/placea.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/placea.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/placev.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/placev.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/preemp.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/preemp.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/prepro.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/prepro.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/random.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/random.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/rcchk.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/rcchk.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/synths.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/synths.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/tbdm.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/tbdm.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/voicin.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/voicin.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/lpc10/vparms.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/lpc10/vparms.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/m4/sox.m4` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/m4/sox.m4`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/mingwbuild` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/mingwbuild`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/osxbuild` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/osxbuild`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/release.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/release.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/screenshot1` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/screenshot1`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/alert.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/alert.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/batch-example.bat` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/batch-example.bat`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/crossfade.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/crossfade.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/crossfade_cat.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/crossfade_cat.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/synth.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/synth.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/testcd.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/testcd.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/testtones.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/testtones.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/scripts/voice-cleanup.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/scripts/voice-cleanup.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/sox.1` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/sox.1`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/soxformat.7` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/soxformat.7`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/soxi.1` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/soxi.1`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/8svx.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/8svx.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/Makefile.am` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/Makefile.am`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/adpcm.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/adpcm.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/adpcm.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/adpcm.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/adpcms.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/adpcms.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/adpcms.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/adpcms.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/aifc-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/aifc-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/aiff-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/aiff-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/aiff.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/aiff.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/aiff.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/aiff.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/al-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/al-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/alsa.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/alsa.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/amr-nb.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/amr-nb.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/amr-wb.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/amr-wb.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/amr.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/amr.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ao.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ao.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/au.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/au.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/avr.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/avr.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/band.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/band.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bend.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bend.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/biquad.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/biquad.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/biquad.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/biquad.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/biquads.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/biquads.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/CoreAudio/CoreAudio.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/CoreAudio/CoreAudio.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/mmsystem.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/mmsystem.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/sndio.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/sndio.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/sys/audioio.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/sys/audioio.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/windows.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/bit-rot/windows.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/caf.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/caf.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cdr.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cdr.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/chorus.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/chorus.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/compand.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/compand.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/compandt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/compandt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/compandt.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/compandt.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/contrast.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/contrast.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/coreaudio.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/coreaudio.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/csox` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/csox`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cvsd.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/cvsdfilt.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/cvsdfilt.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dat.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dat.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dcshift.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dcshift.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/deemph.plt` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/deemph.plt`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/delay.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/delay.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dft_filter.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dft_filter.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dither.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dither.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dither.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dither.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/divide.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/divide.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/downsample.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/downsample.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/dvms-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/dvms-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/earwax.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/earwax.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/echo.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/echo.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/echos.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/echos.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/effects.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/effects.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/effects.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/effects.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/effects_i.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/effects_i.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/effects_i_dsp.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/effects_i_dsp.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example0.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example0.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example1.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example1.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example2.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example2.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example3.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example3.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example4.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example4.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example5.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example5.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/example6.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/example6.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/f4-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/f4-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/f8-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/f8-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fade.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fade.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fap.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fap.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fft4g.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fft4g.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fft4g.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fft4g.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fifo.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fifo.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/fir.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/fir.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/firfit.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/firfit.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/flac.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/flac.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/flanger.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/flanger.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/formats.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/formats.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/formats.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/formats.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/formats_i.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/formats_i.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g711.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g711.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g711.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g711.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g721.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g721.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g723_24.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g723_24.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g723_40.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g723_40.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g72x.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g72x.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/g72x.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/g72x.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/gain.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/gain.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/getopt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/getopt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/gsm.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/gsm.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/gsrt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/gsrt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/hcom.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/hcom.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/hilbert.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/hilbert.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/htk.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/htk.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/id3.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/id3.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/id3.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/id3.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ima-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ima-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ima_rw.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ima_rw.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ima_rw.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ima_rw.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/input.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/input.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/la-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/la-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ladspa.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ladspa.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ladspa.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ladspa.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/libsox.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/libsox.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/libsox.sym` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/libsox.sym`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/libsox_i.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/libsox_i.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/loudness.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/loudness.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/lpc10.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/lpc10.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/lu-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/lu-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mat4.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mat4.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mat5.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mat5.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/maud.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/maud.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mcompand.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mcompand.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mcompand_xover.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mcompand_xover.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/monkey.wav` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/monkey.wav`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mp3-util.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mp3-util.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/mp3.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/mp3.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/noiseprof.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/noiseprof.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/noisered.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/noisered.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/noisered.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/noisered.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/nulfile.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/nulfile.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/optional-fmts.am` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/optional-fmts.am`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/opus.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/opus.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/oss.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/oss.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/output.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/output.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/overdrive.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/overdrive.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/pad.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/pad.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/paf.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/paf.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/phaser.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/phaser.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/prc.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/prc.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/pulseaudio.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/pulseaudio.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/pvf.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/pvf.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate_filters.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate_filters.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate_half_fir.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate_half_fir.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate_poly_fir.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate_poly_fir.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/rate_poly_fir0.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/rate_poly_fir0.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/raw-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/raw-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/raw.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/raw.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/raw.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/raw.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/remix.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/remix.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/repeat.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/repeat.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/reverb.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/reverb.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/reverse.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/reverse.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/s1-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/s1-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/s2-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/s2-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/s3-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/s3-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/s4-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/s4-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sd2.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sd2.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sf.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sf.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/silence.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/silence.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sinc.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sinc.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/skeleff.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/skeleff.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/skelform.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/skelform.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/smp.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/smp.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sndfile.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sndfile.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sndio.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sndio.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sounder.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sounder.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/soundtool.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/soundtool.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox_i.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox_i.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sox_sample_test.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sox_sample_test.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/soxomp.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/soxomp.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/spectrogram.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/spectrogram.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/speed.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/speed.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/speexdsp.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/speexdsp.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sphere.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sphere.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/splice.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/splice.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/stat.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/stat.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/stats.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/stats.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/stretch.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/stretch.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/sunaudio.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/sunaudio.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/swap.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/swap.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/synth.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/synth.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tempo.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tempo.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/test-comments` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/test-comments`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/test-srcs` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/test-srcs`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/testall.bat` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/testall.bat`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/testall.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/testall.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tests.bat` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tests.bat`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tests.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tests.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tremolo.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tremolo.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/trim.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/trim.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/tx16w.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/tx16w.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/u1-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/u1-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/u2-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/u2-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/u3-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/u3-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/u4-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/u4-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/ul-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/ul-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/upsample.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/upsample.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/util.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/util.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/util.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/util.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vad.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vad.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-N.s8` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-N.s8`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-X.s8` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-X.s8`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-X_-N.s8` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_-X_-N.s8`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_.s8` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vectors/intermediate1_44100_-e_unsigned_-b_8_wav_.s8`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/voc.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/voc.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vol.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vol.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vorbis.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vorbis.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vox-fmt.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vox-fmt.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vox.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vox.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/vox.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/vox.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/w64.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/w64.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/wav.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/wav.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/waveaudio.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/waveaudio.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/wavpack.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/wavpack.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/win32/glob.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/win32/glob.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/win32/glob.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/win32/glob.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/wve.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/wve.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/xa.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/xa.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/xi.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/xi.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/xmalloc.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/xmalloc.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/src/xmalloc.h` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/src/xmalloc.h`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/README` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/README`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/corr.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/corr.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/ltest.pl` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/ltest.pl`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/model.c` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/model.c`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/sox/test/wtest.pl` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/sox/test/wtest.pl`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/data_prep/text_normalization.py` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/data_prep/text_normalization.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/lid/infer.py` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/lid/infer.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/misc/get_sample_size.py` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/misc/get_sample_size.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/examples/mms/tts/infer.py` & `wow_ai_mms-0.1.9/wow_ai_mms/examples/mms/tts/infer.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/alignment.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/alignment.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/asr.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/asr.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/README.md` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/README.md`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/criterions/ASG_loss.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/criterions/ASG_loss.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/criterions/__init__.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/criterions/__init__.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/criterions/cross_entropy_acc.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/criterions/cross_entropy_acc.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/data/asr_dataset.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/data/asr_dataset.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/data/collaters.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/data/collaters.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/data/data_utils.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/data/data_utils.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/data/replabels.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/data/replabels.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/datasets/asr_prep_json.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/datasets/asr_prep_json.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/datasets/prepare-librispeech.sh` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/datasets/prepare-librispeech.sh`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/infer.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/infer.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/kaldi/add-self-loop-simple.cc` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/kaldi/add-self-loop-simple.cc`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/kaldi/kaldi_decoder.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/kaldi/kaldi_decoder.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/kaldi/kaldi_initializer.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/kaldi/kaldi_initializer.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/models/vggtransformer.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/models/vggtransformer.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/models/w2l_conv_glu_enc.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/models/w2l_conv_glu_enc.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/README.md` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/README.md`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/hydra/sweeper/ax.yaml` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/hydra/sweeper/ax.yaml`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/hydra/sweeper/ax_sil.yaml` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/hydra/sweeper/ax_sil.yaml`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/infer.yaml` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/infer.yaml`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/run_config/fb_slurm_1.yaml` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/run_config/fb_slurm_1.yaml`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/conf/run_config/fb_slurm_2g.yaml` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/conf/run_config/fb_slurm_2g.yaml`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/base_decoder.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/base_decoder.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/decoder.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/decoder.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/decoder_config.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/decoder_config.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/flashlight_decoder.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/flashlight_decoder.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/decoders/viterbi_decoder.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/decoders/viterbi_decoder.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/new/infer.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/new/infer.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/tasks/speech_recognition.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/tasks/speech_recognition.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/utils/wer_utils.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/utils/wer_utils.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/speech_recognition/w2l_decoder.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/speech_recognition/w2l_decoder.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/models/tts.py` & `wow_ai_mms-0.1.9/wow_ai_mms/models/tts.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/wow_ai_mms/utils.py` & `wow_ai_mms-0.1.9/wow_ai_mms/utils.py`

 * *Files identical despite different names*

### Comparing `wow_ai_mms-0.1.8/PKG-INFO` & `wow_ai_mms-0.1.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: wow-ai-mms
-Version: 0.1.8
+Version: 0.1.9
 Summary: 
 Author: TonyShark
 Author-email: quoi@wow-ai.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

