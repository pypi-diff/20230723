# Comparing `tmp/spotPython-0.6.6.tar.gz` & `tmp/spotPython-0.6.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "spotPython-0.6.6.tar", last modified: Wed Jul 19 09:57:54 2023, max compression
+gzip compressed data, was "spotPython-0.6.8.tar", last modified: Sun Jul 23 21:39:14 2023, max compression
```

## Comparing `spotPython-0.6.6.tar` & `spotPython-0.6.8.tar`

### file list

```diff
@@ -1,203 +1,202 @@
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.204684 spotPython-0.6.6/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.112803 spotPython-0.6.6/.github/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.119069 spotPython-0.6.6/.github/workflows/
--rw-r--r--   0 bartz      (501) staff       (20)      557 2023-02-05 01:17:02.000000 spotPython-0.6.6/.github/workflows/test.yml
--rw-r--r--   0 bartz      (501) staff       (20)    17867 2023-07-04 13:42:00.000000 spotPython-0.6.6/.gitignore
--rw-r--r--   0 bartz      (501) staff       (20)        0 2023-05-18 20:25:57.000000 spotPython-0.6.6/.nojekyll
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.133642 spotPython-0.6.6/Figures.d/
--rw-r--r--   0 bartz      (501) staff       (20)    21113 2023-04-26 21:46:16.000000 spotPython-0.6.6/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_contour_1_2.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     5878 2023-04-26 21:46:16.000000 spotPython-0.6.6/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_importance.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     6563 2023-04-26 21:46:16.000000 spotPython-0.6.6/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_progress.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    26562 2023-04-26 21:46:16.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_contour_2_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     8850 2023-04-26 21:46:16.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_importance.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     6569 2023-04-26 21:46:16.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_progress.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    20478 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_1.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    20590 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_2.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    23054 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22138 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_4.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    21534 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_2.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22805 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22098 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_4.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    23275 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_2_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    21965 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_2_4.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22913 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_3_4.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     9680 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_importance.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     6536 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_progress.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    21132 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_1.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    21651 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_2.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22154 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    21347 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_4.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22265 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_2.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22056 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22224 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_4.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    23950 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_2_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    23161 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_2_4.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22297 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_3_4.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     9681 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_importance.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     8189 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_progress.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    22759 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_1_2.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    24775 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_1_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    23126 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_2_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     8905 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_importance.pdf
--rw-r--r--   0 bartz      (501) staff       (20)     7635 2023-05-08 15:19:19.000000 spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_progress.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    24695 2023-05-07 19:44:11.000000 spotPython-0.6.6/Figures.d/13-torch_s7cfd16_600min_20init_2023-05-05_18-52-19_contour_2_3.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    34523 2023-01-30 12:58:45.000000 spotPython-0.6.6/LICENSE.txt
--rw-r--r--   0 bartz      (501) staff       (20)       71 2023-04-23 10:59:22.000000 spotPython-0.6.6/MANIFEST.in
--rw-r--r--   0 bartz      (501) staff       (20)     7578 2023-07-19 09:57:54.204135 spotPython-0.6.6/PKG-INFO
--rw-r--r--   0 bartz      (501) staff       (20)     6808 2023-06-09 14:13:36.000000 spotPython-0.6.6/README.md
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.135733 spotPython-0.6.6/docs/
--rw-r--r--   0 bartz      (501) staff       (20)    46499 2023-07-13 14:40:46.000000 spotPython-0.6.6/docs/about.md
--rw-r--r--   0 bartz      (501) staff       (20)       49 2023-07-13 14:40:46.000000 spotPython-0.6.6/docs/download.md
--rw-r--r--   0 bartz      (501) staff       (20)      802 2023-07-17 08:56:18.000000 spotPython-0.6.6/docs/examples.md
--rw-r--r--   0 bartz      (501) staff       (20)      947 2023-07-13 14:40:46.000000 spotPython-0.6.6/docs/gen_ref_pages.py
--rw-r--r--   0 bartz      (501) staff       (20)      350 2023-07-17 08:56:18.000000 spotPython-0.6.6/docs/hyperparameter-tuning-cookbook.md
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.136329 spotPython-0.6.6/docs/images/
--rw-r--r--   0 bartz      (501) staff       (20)    11605 2023-07-13 14:40:46.000000 spotPython-0.6.6/docs/images/favicon.png
--rw-r--r--   0 bartz      (501) staff       (20)    11605 2023-07-13 14:40:46.000000 spotPython-0.6.6/docs/images/spotlogo.png
--rw-r--r--   0 bartz      (501) staff       (20)      392 2023-07-17 08:56:18.000000 spotPython-0.6.6/docs/index.md
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.136917 spotPython-0.6.6/img/
--rw-r--r--   0 bartz      (501) staff       (20)    11605 2023-07-17 08:56:18.000000 spotPython-0.6.6/img/favicon.png
--rw-r--r--   0 bartz      (501) staff       (20)    67674 2023-06-09 14:13:36.000000 spotPython-0.6.6/img/spotLogo.png
--rwxr-xr-x   0 bartz      (501) staff       (20)      146 2023-07-17 08:56:18.000000 spotPython-0.6.6/makeSpot.sh
--rw-r--r--   0 bartz      (501) staff       (20)     1487 2023-07-17 08:56:18.000000 spotPython-0.6.6/mkdocs.yml
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.139315 spotPython-0.6.6/notebooks/
--rw-r--r--   0 bartz      (501) staff       (20)    64826 2023-07-17 08:56:18.000000 spotPython-0.6.6/notebooks/14_spot_ray_hpt_torch_cifar10.ipynb
--rw-r--r--   0 bartz      (501) staff       (20)   953519 2023-07-04 13:42:01.000000 spotPython-0.6.6/notebooks/31_spot_lightning_csv.ipynb
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.113691 spotPython-0.6.6/notebooks/data/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.139673 spotPython-0.6.6/notebooks/data/torch/
--rw-r--r--   0 bartz      (501) staff       (20)    77195 2023-05-15 06:42:12.000000 spotPython-0.6.6/notebooks/data/torch/model_spot_trained.pt
--rw-r--r--   0 bartz      (501) staff       (20)      359 2023-03-25 23:35:15.000000 spotPython-0.6.6/notebooks/data.json
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.161995 spotPython-0.6.6/notebooks/figures/
--rw-r--r--   0 bartz      (501) staff       (20)   114797 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/12-torch_p040025_1min_5init_2023-06-07_19-09-30_contour_0_1.png
--rw-r--r--   0 bartz      (501) staff       (20)   117891 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_contour_0_1.png
--rw-r--r--   0 bartz      (501) staff       (20)    35435 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_importance.png
--rw-r--r--   0 bartz      (501) staff       (20)    41877 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_progress.png
--rw-r--r--   0 bartz      (501) staff       (20)   117933 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_contour_0_1.png
--rw-r--r--   0 bartz      (501) staff       (20)    29392 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_progress.png
--rw-r--r--   0 bartz      (501) staff       (20)   770688 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_tensorboard_01.png
--rw-r--r--   0 bartz      (501) staff       (20)   305679 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_tensorboard_02.png
--rw-r--r--   0 bartz      (501) staff       (20)    34252 2023-06-26 10:36:37.000000 spotPython-0.6.6/notebooks/figures/29-torch_bartz09_1min_5init_2023-06-24_21-45-17_importance.png
--rw-r--r--   0 bartz      (501) staff       (20)    44029 2023-06-26 10:36:37.000000 spotPython-0.6.6/notebooks/figures/29-torch_bartz09_1min_5init_2023-06-24_21-45-17_progress.png
--rw-r--r--   0 bartz      (501) staff       (20)    88272 2023-05-27 21:08:47.000000 spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_1.png
--rw-r--r--   0 bartz      (501) staff       (20)    84164 2023-05-27 21:08:47.000000 spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_3.png
--rw-r--r--   0 bartz      (501) staff       (20)    93300 2023-05-27 21:08:47.000000 spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_4.png
--rw-r--r--   0 bartz      (501) staff       (20)    84900 2023-05-27 21:08:47.000000 spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_1_3.png
--rw-r--r--   0 bartz      (501) staff       (20)    94821 2023-05-27 21:08:47.000000 spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_1_4.png
--rw-r--r--   0 bartz      (501) staff       (20)    92856 2023-05-27 21:08:47.000000 spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_3_4.png
--rw-r--r--   0 bartz      (501) staff       (20)    21443 2023-05-27 21:08:47.000000 spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_importance.png
--rw-r--r--   0 bartz      (501) staff       (20)    26414 2023-05-27 21:08:47.000000 spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_progress.png
--rw-r--r--   0 bartz      (501) staff       (20)   121376 2023-05-28 04:57:10.000000 spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_20init_2023-05-27_23-10-01_parallel.png
--rw-r--r--   0 bartz      (501) staff       (20)   116976 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_contour_0_3.png
--rw-r--r--   0 bartz      (501) staff       (20)    28703 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_importance.png
--rw-r--r--   0 bartz      (501) staff       (20)   161701 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_parallel.png
--rw-r--r--   0 bartz      (501) staff       (20)    41471 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_progress.png
--rw-r--r--   0 bartz      (501) staff       (20)   115822 2023-01-30 12:58:45.000000 spotPython-0.6.6/notebooks/figures/spotModel.graffle
--rw-r--r--   0 bartz      (501) staff       (20)    26289 2023-01-30 12:58:45.000000 spotPython-0.6.6/notebooks/figures/spotModel.pdf
--rw-r--r--   0 bartz      (501) staff       (20)    64603 2023-01-30 12:58:45.000000 spotPython-0.6.6/notebooks/figures/spotModel.png
--rw-r--r--   0 bartz      (501) staff       (20)   434803 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/tensorboard_0.png
--rw-r--r--   0 bartz      (501) staff       (20)   145933 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/tensorboard_1.png
--rw-r--r--   0 bartz      (501) staff       (20)   751199 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/tensorboard_hdparams.png
--rw-r--r--   0 bartz      (501) staff       (20)  2025087 2023-06-09 14:13:36.000000 spotPython-0.6.6/notebooks/figures/tensorboard_parallel.png
--rw-r--r--   0 bartz      (501) staff       (20)     1545 2023-07-19 09:57:41.000000 spotPython-0.6.6/pyproject.toml
--rw-r--r--   0 bartz      (501) staff       (20)       38 2023-07-19 09:57:54.204801 spotPython-0.6.6/setup.cfg
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.114181 spotPython-0.6.6/src/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.166392 spotPython-0.6.6/src/spotPython/
--rw-r--r--   0 bartz      (501) staff       (20)      214 2023-07-19 09:57:53.000000 spotPython-0.6.6/src/spotPython/_version.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.168897 spotPython-0.6.6/src/spotPython/budget/
--rw-r--r--   0 bartz      (501) staff       (20)     3475 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/budget/ocba.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.169779 spotPython-0.6.6/src/spotPython/build/
--rw-r--r--   0 bartz      (501) staff       (20)    55706 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/build/kriging.py
--rw-r--r--   0 bartz      (501) staff       (20)      342 2023-01-30 12:58:45.000000 spotPython-0.6.6/src/spotPython/build/surrogates.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.174688 spotPython-0.6.6/src/spotPython/data/
--rw-r--r--   0 bartz      (501) staff       (20)      317 2023-04-23 10:59:22.000000 spotPython-0.6.6/src/spotPython/data/__init__.py
--rw-r--r--   0 bartz      (501) staff       (20)    23267 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/data/base.py
--rw-r--r--   0 bartz      (501) staff       (20)     6159 2023-07-19 07:52:35.000000 spotPython-0.6.6/src/spotPython/data/light_hyper_dict.json
--rw-r--r--   0 bartz      (501) staff       (20)     1036 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/data/light_hyper_dict.py
--rw-r--r--   0 bartz      (501) staff       (20)    20975 2023-05-30 11:46:53.000000 spotPython-0.6.6/src/spotPython/data/sklearn_hyper_dict.json
--rw-r--r--   0 bartz      (501) staff       (20)     1282 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/data/sklearn_hyper_dict.py
--rw-r--r--   0 bartz      (501) staff       (20)     9208 2023-06-09 14:13:36.000000 spotPython-0.6.6/src/spotPython/data/torch_hyper_dict.json
--rw-r--r--   0 bartz      (501) staff       (20)     1262 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/data/torch_hyper_dict.py
--rw-r--r--   0 bartz      (501) staff       (20)     1471 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/data/torchdata.py
--rw-r--r--   0 bartz      (501) staff       (20)     2912 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/data/vbdp.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.175994 spotPython-0.6.6/src/spotPython/design/
--rw-r--r--   0 bartz      (501) staff       (20)     1223 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/design/designs.py
--rw-r--r--   0 bartz      (501) staff       (20)     1225 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/design/factorial.py
--rw-r--r--   0 bartz      (501) staff       (20)     2213 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/design/spacefilling.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.177766 spotPython-0.6.6/src/spotPython/fun/
--rw-r--r--   0 bartz      (501) staff       (20)     4643 2023-07-19 09:00:32.000000 spotPython-0.6.6/src/spotPython/fun/hyperlight.py
--rw-r--r--   0 bartz      (501) staff       (20)     5720 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/fun/hypersklearn.py
--rw-r--r--   0 bartz      (501) staff       (20)     7435 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/fun/hypertorch.py
--rw-r--r--   0 bartz      (501) staff       (20)    26824 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/fun/objectivefunctions.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.179297 spotPython-0.6.6/src/spotPython/hyperparameters/
--rw-r--r--   0 bartz      (501) staff       (20)     4851 2023-03-25 23:35:15.000000 spotPython-0.6.6/src/spotPython/hyperparameters/categorical.py
--rw-r--r--   0 bartz      (501) staff       (20)     5113 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/hyperparameters/optimizer.py
--rw-r--r--   0 bartz      (501) staff       (20)    34602 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/hyperparameters/values.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.184867 spotPython-0.6.6/src/spotPython/light/
--rw-r--r--   0 bartz      (501) staff       (20)     3426 2023-07-19 08:08:13.000000 spotPython-0.6.6/src/spotPython/light/cifar10datamodule.py
--rw-r--r--   0 bartz      (501) staff       (20)     4898 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/light/crossvalidationdatamodule.py
--rw-r--r--   0 bartz      (501) staff       (20)     4128 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/light/csvdatamodule.py
--rw-r--r--   0 bartz      (501) staff       (20)     3313 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/light/csvdataset.py
--rw-r--r--   0 bartz      (501) staff       (20)     5546 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/light/litmodel.py
--rw-r--r--   0 bartz      (501) staff       (20)     1659 2023-06-26 10:36:37.000000 spotPython-0.6.6/src/spotPython/light/mnistdatamodule.py
--rw-r--r--   0 bartz      (501) staff       (20)    12288 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/light/netlightbase.py
--rw-r--r--   0 bartz      (501) staff       (20)    13445 2023-07-19 09:48:01.000000 spotPython-0.6.6/src/spotPython/light/netlinearbase.py
--rw-r--r--   0 bartz      (501) staff       (20)    11131 2023-07-19 09:54:04.000000 spotPython-0.6.6/src/spotPython/light/traintest.py
--rw-r--r--   0 bartz      (501) staff       (20)    11435 2023-07-19 08:08:09.000000 spotPython-0.6.6/src/spotPython/light/traintest_NEW.py
--rw-r--r--   0 bartz      (501) staff       (20)    11131 2023-07-18 07:18:07.000000 spotPython-0.6.6/src/spotPython/light/traintest_OLD.py
--rw-r--r--   0 bartz      (501) staff       (20)      255 2023-07-02 19:29:48.000000 spotPython-0.6.6/src/spotPython/light/utils.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.185612 spotPython-0.6.6/src/spotPython/plot/
--rw-r--r--   0 bartz      (501) staff       (20)     1707 2023-01-30 12:58:45.000000 spotPython-0.6.6/src/spotPython/plot/contour.py
--rw-r--r--   0 bartz      (501) staff       (20)     5949 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/plot/validation.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.186063 spotPython-0.6.6/src/spotPython/sklearn/
--rw-r--r--   0 bartz      (501) staff       (20)     3715 2023-06-09 14:13:36.000000 spotPython-0.6.6/src/spotPython/sklearn/traintest.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.186529 spotPython-0.6.6/src/spotPython/spot/
--rw-r--r--   0 bartz      (501) staff       (20)    39594 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/spot/spot.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.190965 spotPython-0.6.6/src/spotPython/torch/
--rw-r--r--   0 bartz      (501) staff       (20)     1018 2023-06-26 10:36:37.000000 spotPython-0.6.6/src/spotPython/torch/activation.py
--rw-r--r--   0 bartz      (501) staff       (20)      517 2023-05-31 23:03:53.000000 spotPython-0.6.6/src/spotPython/torch/dataframedataset.py
--rw-r--r--   0 bartz      (501) staff       (20)      692 2023-06-27 23:06:07.000000 spotPython-0.6.6/src/spotPython/torch/initialization.py
--rw-r--r--   0 bartz      (501) staff       (20)     4570 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/torch/mapk.py
--rw-r--r--   0 bartz      (501) staff       (20)     1012 2023-05-27 21:08:47.000000 spotPython-0.6.6/src/spotPython/torch/netcifar10.py
--rw-r--r--   0 bartz      (501) staff       (20)      425 2023-05-27 21:08:47.000000 spotPython-0.6.6/src/spotPython/torch/netcore.py
--rw-r--r--   0 bartz      (501) staff       (20)      803 2023-05-27 21:08:47.000000 spotPython-0.6.6/src/spotPython/torch/netfashionMNIST.py
--rw-r--r--   0 bartz      (501) staff       (20)     1071 2023-06-09 14:13:36.000000 spotPython-0.6.6/src/spotPython/torch/netregression.py
--rw-r--r--   0 bartz      (501) staff       (20)     1565 2023-06-02 14:39:41.000000 spotPython-0.6.6/src/spotPython/torch/netvbdp.py
--rw-r--r--   0 bartz      (501) staff       (20)    14987 2023-06-18 09:30:24.000000 spotPython-0.6.6/src/spotPython/torch/traintest.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.196275 spotPython-0.6.6/src/spotPython/utils/
--rw-r--r--   0 bartz      (501) staff       (20)     2003 2023-04-11 06:36:10.000000 spotPython-0.6.6/src/spotPython/utils/aggregate.py
--rw-r--r--   0 bartz      (501) staff       (20)      498 2023-05-14 07:02:46.000000 spotPython-0.6.6/src/spotPython/utils/classes.py
--rw-r--r--   0 bartz      (501) staff       (20)     1162 2023-04-14 08:08:49.000000 spotPython-0.6.6/src/spotPython/utils/compare.py
--rw-r--r--   0 bartz      (501) staff       (20)     3764 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/utils/convert.py
--rw-r--r--   0 bartz      (501) staff       (20)      628 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/utils/device.py
--rw-r--r--   0 bartz      (501) staff       (20)     9289 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/utils/eda.py
--rw-r--r--   0 bartz      (501) staff       (20)     3299 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/utils/file.py
--rw-r--r--   0 bartz      (501) staff       (20)     5846 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/utils/init.py
--rw-r--r--   0 bartz      (501) staff       (20)     5028 2023-06-26 11:21:46.000000 spotPython-0.6.6/src/spotPython/utils/metrics.py
--rw-r--r--   0 bartz      (501) staff       (20)      912 2023-06-02 14:39:41.000000 spotPython-0.6.6/src/spotPython/utils/progress.py
--rw-r--r--   0 bartz      (501) staff       (20)     1379 2023-04-14 08:08:49.000000 spotPython-0.6.6/src/spotPython/utils/repair.py
--rw-r--r--   0 bartz      (501) staff       (20)     6826 2023-07-17 08:56:18.000000 spotPython-0.6.6/src/spotPython/utils/transform.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.168594 spotPython-0.6.6/src/spotPython.egg-info/
--rw-r--r--   0 bartz      (501) staff       (20)     7578 2023-07-19 09:57:54.000000 spotPython-0.6.6/src/spotPython.egg-info/PKG-INFO
--rw-r--r--   0 bartz      (501) staff       (20)     8300 2023-07-19 09:57:54.000000 spotPython-0.6.6/src/spotPython.egg-info/SOURCES.txt
--rw-r--r--   0 bartz      (501) staff       (20)        1 2023-07-19 09:57:54.000000 spotPython-0.6.6/src/spotPython.egg-info/dependency_links.txt
--rw-r--r--   0 bartz      (501) staff       (20)      196 2023-07-19 09:57:54.000000 spotPython-0.6.6/src/spotPython.egg-info/requires.txt
--rw-r--r--   0 bartz      (501) staff       (20)       11 2023-07-19 09:57:54.000000 spotPython-0.6.6/src/spotPython.egg-info/top_level.txt
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-19 09:57:54.203484 spotPython-0.6.6/test/
--rw-r--r--   0 bartz      (501) staff       (20)      873 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_aggregate_mean_var.py
--rw-r--r--   0 bartz      (501) staff       (20)     4546 2023-04-11 06:36:10.000000 spotPython-0.6.6/test/test_build_Psi.py
--rw-r--r--   0 bartz      (501) staff       (20)     4511 2023-04-11 06:36:10.000000 spotPython-0.6.6/test/test_build_U.py
--rw-r--r--   0 bartz      (501) staff       (20)      797 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_build_psi_vec.py
--rw-r--r--   0 bartz      (501) staff       (20)      917 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_evaluate_new_X.py
--rw-r--r--   0 bartz      (501) staff       (20)     1319 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_evaluate_new_solutions.py
--rw-r--r--   0 bartz      (501) staff       (20)    10337 2023-04-11 06:36:10.000000 spotPython-0.6.6/test/test_extract_from_bounds.py
--rw-r--r--   0 bartz      (501) staff       (20)     2263 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_generate_design.py
--rw-r--r--   0 bartz      (501) staff       (20)     2223 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_infill.py
--rw-r--r--   0 bartz      (501) staff       (20)      643 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_nat_to_cod.py
--rw-r--r--   0 bartz      (501) staff       (20)     1330 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_nat_to_cod_init.py
--rw-r--r--   0 bartz      (501) staff       (20)     1603 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_ocba.py
--rw-r--r--   0 bartz      (501) staff       (20)     1208 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_repair_non_numeric.py
--rw-r--r--   0 bartz      (501) staff       (20)     4887 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_set_de_bounds.py
--rw-r--r--   0 bartz      (501) staff       (20)     2223 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_show_progress.py
--rw-r--r--   0 bartz      (501) staff       (20)     1131 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_suggest_new_X.py
--rw-r--r--   0 bartz      (501) staff       (20)     1765 2023-01-30 12:58:45.000000 spotPython-0.6.6/test/test_update_surrogate.py
--rw-r--r--   0 bartz      (501) staff       (20)      130 2023-05-19 13:13:30.000000 spotPython-0.6.6/tox.ini
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.984879 spotPython-0.6.8/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.954779 spotPython-0.6.8/.github/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.958699 spotPython-0.6.8/.github/workflows/
+-rw-r--r--   0 bartz      (501) staff       (20)      557 2023-02-02 20:30:23.000000 spotPython-0.6.8/.github/workflows/test.yml
+-rw-r--r--   0 bartz      (501) staff       (20)    17867 2023-07-04 14:15:14.000000 spotPython-0.6.8/.gitignore
+-rw-r--r--   0 bartz      (501) staff       (20)        0 2023-05-18 22:04:43.000000 spotPython-0.6.8/.nojekyll
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.964192 spotPython-0.6.8/Figures.d/
+-rw-r--r--   0 bartz      (501) staff       (20)    21113 2023-04-26 21:03:04.000000 spotPython-0.6.8/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_contour_1_2.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     5878 2023-04-26 21:03:04.000000 spotPython-0.6.8/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_importance.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     6563 2023-04-26 21:03:04.000000 spotPython-0.6.8/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_progress.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    26562 2023-04-26 22:09:11.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_contour_2_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     8850 2023-04-26 22:09:11.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_importance.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     6569 2023-04-26 22:09:11.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_progress.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    20478 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_1.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    20590 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_2.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    23054 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22138 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_4.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    21534 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_2.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22805 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22098 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_4.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    23275 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_2_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    21965 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_2_4.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22913 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_3_4.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     9680 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_importance.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     6536 2023-04-28 06:03:36.000000 spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_progress.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    21132 2023-05-08 04:46:15.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_1.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    21651 2023-05-08 04:46:16.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_2.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22154 2023-05-08 04:46:18.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    21347 2023-05-08 04:46:19.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_4.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22265 2023-05-08 04:46:20.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_2.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22056 2023-05-08 04:46:21.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22224 2023-05-08 04:46:22.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_4.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    23950 2023-05-08 04:46:23.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_2_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    23161 2023-05-08 04:46:24.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_2_4.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22297 2023-05-08 04:46:25.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_3_4.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     9681 2023-05-08 04:37:14.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_importance.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     8189 2023-05-08 04:37:14.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_progress.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    22759 2023-05-07 21:33:09.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_1_2.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    24775 2023-05-07 21:33:09.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_1_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    23126 2023-05-07 21:33:10.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_2_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     8905 2023-05-07 21:23:58.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_importance.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)     7635 2023-05-07 21:23:58.000000 spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_progress.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    24695 2023-05-06 06:36:55.000000 spotPython-0.6.8/Figures.d/13-torch_s7cfd16_600min_20init_2023-05-05_18-52-19_contour_2_3.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    34523 2023-02-01 14:33:52.000000 spotPython-0.6.8/LICENSE.txt
+-rw-r--r--   0 bartz      (501) staff       (20)       71 2023-04-20 20:35:14.000000 spotPython-0.6.8/MANIFEST.in
+-rw-r--r--   0 bartz      (501) staff       (20)     7578 2023-07-23 21:39:14.984708 spotPython-0.6.8/PKG-INFO
+-rw-r--r--   0 bartz      (501) staff       (20)     6808 2023-06-08 16:18:46.000000 spotPython-0.6.8/README.md
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.965068 spotPython-0.6.8/docs/
+-rw-r--r--   0 bartz      (501) staff       (20)    46499 2022-10-31 16:48:05.000000 spotPython-0.6.8/docs/about.md
+-rw-r--r--   0 bartz      (501) staff       (20)       49 2023-07-12 23:09:54.000000 spotPython-0.6.8/docs/download.md
+-rw-r--r--   0 bartz      (501) staff       (20)      802 2023-07-16 08:32:11.000000 spotPython-0.6.8/docs/examples.md
+-rw-r--r--   0 bartz      (501) staff       (20)      947 2022-10-31 16:48:05.000000 spotPython-0.6.8/docs/gen_ref_pages.py
+-rw-r--r--   0 bartz      (501) staff       (20)      350 2023-07-14 22:03:54.000000 spotPython-0.6.8/docs/hyperparameter-tuning-cookbook.md
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.965337 spotPython-0.6.8/docs/images/
+-rw-r--r--   0 bartz      (501) staff       (20)    11605 2022-10-31 16:48:05.000000 spotPython-0.6.8/docs/images/favicon.png
+-rw-r--r--   0 bartz      (501) staff       (20)    11605 2022-10-31 16:48:05.000000 spotPython-0.6.8/docs/images/spotlogo.png
+-rw-r--r--   0 bartz      (501) staff       (20)      392 2023-07-15 18:25:23.000000 spotPython-0.6.8/docs/index.md
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.965586 spotPython-0.6.8/img/
+-rw-r--r--   0 bartz      (501) staff       (20)    11605 2023-07-13 05:52:18.000000 spotPython-0.6.8/img/favicon.png
+-rw-r--r--   0 bartz      (501) staff       (20)    67674 2023-05-27 21:03:27.000000 spotPython-0.6.8/img/spotLogo.png
+-rwxr-xr-x   0 bartz      (501) staff       (20)      146 2023-07-15 09:35:47.000000 spotPython-0.6.8/makeSpot.sh
+-rw-r--r--   0 bartz      (501) staff       (20)     1822 2023-07-23 20:44:39.000000 spotPython-0.6.8/mkdocs.yml
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.966482 spotPython-0.6.8/notebooks/
+-rw-r--r--   0 bartz      (501) staff       (20)    64826 2023-07-15 20:49:26.000000 spotPython-0.6.8/notebooks/14_spot_ray_hpt_torch_cifar10.ipynb
+-rw-r--r--   0 bartz      (501) staff       (20)   953519 2023-07-04 14:15:14.000000 spotPython-0.6.8/notebooks/31_spot_lightning_csv.ipynb
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.955493 spotPython-0.6.8/notebooks/data/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.966606 spotPython-0.6.8/notebooks/data/torch/
+-rw-r--r--   0 bartz      (501) staff       (20)    77195 2023-05-14 08:03:00.000000 spotPython-0.6.8/notebooks/data/torch/model_spot_trained.pt
+-rw-r--r--   0 bartz      (501) staff       (20)      359 2023-03-21 18:40:04.000000 spotPython-0.6.8/notebooks/data.json
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.972498 spotPython-0.6.8/notebooks/figures/
+-rw-r--r--   0 bartz      (501) staff       (20)   114797 2023-06-07 17:28:19.000000 spotPython-0.6.8/notebooks/figures/12-torch_p040025_1min_5init_2023-06-07_19-09-30_contour_0_1.png
+-rw-r--r--   0 bartz      (501) staff       (20)   117891 2023-06-08 12:22:25.000000 spotPython-0.6.8/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_contour_0_1.png
+-rw-r--r--   0 bartz      (501) staff       (20)    35435 2023-06-08 12:22:25.000000 spotPython-0.6.8/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_importance.png
+-rw-r--r--   0 bartz      (501) staff       (20)    41877 2023-06-08 12:22:25.000000 spotPython-0.6.8/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_progress.png
+-rw-r--r--   0 bartz      (501) staff       (20)   117933 2023-06-07 11:49:47.000000 spotPython-0.6.8/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_contour_0_1.png
+-rw-r--r--   0 bartz      (501) staff       (20)    29392 2023-06-07 11:04:53.000000 spotPython-0.6.8/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_progress.png
+-rw-r--r--   0 bartz      (501) staff       (20)   770688 2023-06-07 11:10:20.000000 spotPython-0.6.8/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_tensorboard_01.png
+-rw-r--r--   0 bartz      (501) staff       (20)   305679 2023-06-07 11:11:28.000000 spotPython-0.6.8/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_tensorboard_02.png
+-rw-r--r--   0 bartz      (501) staff       (20)    34252 2023-06-24 19:48:27.000000 spotPython-0.6.8/notebooks/figures/29-torch_bartz09_1min_5init_2023-06-24_21-45-17_importance.png
+-rw-r--r--   0 bartz      (501) staff       (20)    44029 2023-06-24 19:48:27.000000 spotPython-0.6.8/notebooks/figures/29-torch_bartz09_1min_5init_2023-06-24_21-45-17_progress.png
+-rw-r--r--   0 bartz      (501) staff       (20)    88272 2023-05-26 10:05:04.000000 spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_1.png
+-rw-r--r--   0 bartz      (501) staff       (20)    84164 2023-05-26 10:04:55.000000 spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_3.png
+-rw-r--r--   0 bartz      (501) staff       (20)    93300 2023-05-26 10:04:39.000000 spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_4.png
+-rw-r--r--   0 bartz      (501) staff       (20)    84900 2023-05-26 10:04:25.000000 spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_1_3.png
+-rw-r--r--   0 bartz      (501) staff       (20)    94821 2023-05-26 10:04:11.000000 spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_1_4.png
+-rw-r--r--   0 bartz      (501) staff       (20)    92856 2023-05-26 10:03:52.000000 spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_3_4.png
+-rw-r--r--   0 bartz      (501) staff       (20)    21443 2023-05-26 10:02:53.000000 spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_importance.png
+-rw-r--r--   0 bartz      (501) staff       (20)    26414 2023-05-26 10:02:27.000000 spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_progress.png
+-rw-r--r--   0 bartz      (501) staff       (20)   121376 2023-05-28 06:32:18.000000 spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_20init_2023-05-27_23-10-01_parallel.png
+-rw-r--r--   0 bartz      (501) staff       (20)   116976 2023-06-07 05:09:22.000000 spotPython-0.6.8/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_contour_0_3.png
+-rw-r--r--   0 bartz      (501) staff       (20)    28703 2023-06-06 21:13:57.000000 spotPython-0.6.8/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_importance.png
+-rw-r--r--   0 bartz      (501) staff       (20)   161701 2023-06-07 06:30:18.000000 spotPython-0.6.8/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_parallel.png
+-rw-r--r--   0 bartz      (501) staff       (20)    41471 2023-06-06 21:13:56.000000 spotPython-0.6.8/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_progress.png
+-rw-r--r--   0 bartz      (501) staff       (20)   115822 2023-02-01 14:33:52.000000 spotPython-0.6.8/notebooks/figures/spotModel.graffle
+-rw-r--r--   0 bartz      (501) staff       (20)    26289 2023-02-01 14:33:52.000000 spotPython-0.6.8/notebooks/figures/spotModel.pdf
+-rw-r--r--   0 bartz      (501) staff       (20)    64603 2023-02-01 14:33:52.000000 spotPython-0.6.8/notebooks/figures/spotModel.png
+-rw-r--r--   0 bartz      (501) staff       (20)   434803 2023-06-07 06:48:45.000000 spotPython-0.6.8/notebooks/figures/tensorboard_0.png
+-rw-r--r--   0 bartz      (501) staff       (20)   145933 2023-06-07 06:46:35.000000 spotPython-0.6.8/notebooks/figures/tensorboard_1.png
+-rw-r--r--   0 bartz      (501) staff       (20)   751199 2023-06-07 06:51:03.000000 spotPython-0.6.8/notebooks/figures/tensorboard_hdparams.png
+-rw-r--r--   0 bartz      (501) staff       (20)  2025087 2023-06-07 06:53:15.000000 spotPython-0.6.8/notebooks/figures/tensorboard_parallel.png
+-rw-r--r--   0 bartz      (501) staff       (20)     1507 2023-07-23 20:48:02.000000 spotPython-0.6.8/pyproject.toml
+-rw-r--r--   0 bartz      (501) staff       (20)       38 2023-07-23 21:39:14.984922 spotPython-0.6.8/setup.cfg
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.955880 spotPython-0.6.8/src/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.956995 spotPython-0.6.8/src/spotPython/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.974392 spotPython-0.6.8/src/spotPython/budget/
+-rw-r--r--   0 bartz      (501) staff       (20)     3888 2023-07-23 20:55:05.000000 spotPython-0.6.8/src/spotPython/budget/ocba.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.974674 spotPython-0.6.8/src/spotPython/build/
+-rw-r--r--   0 bartz      (501) staff       (20)    55582 2023-07-23 21:27:59.000000 spotPython-0.6.8/src/spotPython/build/kriging.py
+-rw-r--r--   0 bartz      (501) staff       (20)      342 2023-02-02 22:52:12.000000 spotPython-0.6.8/src/spotPython/build/surrogates.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.975925 spotPython-0.6.8/src/spotPython/data/
+-rw-r--r--   0 bartz      (501) staff       (20)      317 2023-04-20 20:18:46.000000 spotPython-0.6.8/src/spotPython/data/__init__.py
+-rw-r--r--   0 bartz      (501) staff       (20)    23267 2023-07-17 19:56:10.000000 spotPython-0.6.8/src/spotPython/data/base.py
+-rw-r--r--   0 bartz      (501) staff       (20)     6159 2023-07-18 19:53:58.000000 spotPython-0.6.8/src/spotPython/data/light_hyper_dict.json
+-rw-r--r--   0 bartz      (501) staff       (20)     1036 2023-07-17 20:01:02.000000 spotPython-0.6.8/src/spotPython/data/light_hyper_dict.py
+-rw-r--r--   0 bartz      (501) staff       (20)    20975 2023-05-30 15:26:52.000000 spotPython-0.6.8/src/spotPython/data/sklearn_hyper_dict.json
+-rw-r--r--   0 bartz      (501) staff       (20)     1282 2023-07-17 20:05:39.000000 spotPython-0.6.8/src/spotPython/data/sklearn_hyper_dict.py
+-rw-r--r--   0 bartz      (501) staff       (20)     9208 2023-06-06 20:04:52.000000 spotPython-0.6.8/src/spotPython/data/torch_hyper_dict.json
+-rw-r--r--   0 bartz      (501) staff       (20)     1262 2023-07-17 20:07:25.000000 spotPython-0.6.8/src/spotPython/data/torch_hyper_dict.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1471 2023-07-17 20:09:39.000000 spotPython-0.6.8/src/spotPython/data/torchdata.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2912 2023-07-17 20:14:22.000000 spotPython-0.6.8/src/spotPython/data/vbdp.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.976302 spotPython-0.6.8/src/spotPython/design/
+-rw-r--r--   0 bartz      (501) staff       (20)     1223 2023-07-17 22:31:41.000000 spotPython-0.6.8/src/spotPython/design/designs.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1299 2023-07-23 21:35:33.000000 spotPython-0.6.8/src/spotPython/design/factorial.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2227 2023-07-23 21:36:02.000000 spotPython-0.6.8/src/spotPython/design/spacefilling.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.976762 spotPython-0.6.8/src/spotPython/fun/
+-rw-r--r--   0 bartz      (501) staff       (20)     4647 2023-07-23 21:36:25.000000 spotPython-0.6.8/src/spotPython/fun/hyperlight.py
+-rw-r--r--   0 bartz      (501) staff       (20)     5720 2023-07-18 05:26:06.000000 spotPython-0.6.8/src/spotPython/fun/hypersklearn.py
+-rw-r--r--   0 bartz      (501) staff       (20)     7435 2023-07-17 20:59:08.000000 spotPython-0.6.8/src/spotPython/fun/hypertorch.py
+-rw-r--r--   0 bartz      (501) staff       (20)    26824 2023-07-15 21:02:46.000000 spotPython-0.6.8/src/spotPython/fun/objectivefunctions.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.977118 spotPython-0.6.8/src/spotPython/hyperparameters/
+-rw-r--r--   0 bartz      (501) staff       (20)     4856 2023-07-23 21:37:39.000000 spotPython-0.6.8/src/spotPython/hyperparameters/categorical.py
+-rw-r--r--   0 bartz      (501) staff       (20)     5113 2023-07-17 21:02:24.000000 spotPython-0.6.8/src/spotPython/hyperparameters/optimizer.py
+-rw-r--r--   0 bartz      (501) staff       (20)    34602 2023-07-17 21:26:45.000000 spotPython-0.6.8/src/spotPython/hyperparameters/values.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.978817 spotPython-0.6.8/src/spotPython/light/
+-rw-r--r--   0 bartz      (501) staff       (20)     3426 2023-07-20 07:13:47.000000 spotPython-0.6.8/src/spotPython/light/cifar10datamodule.py
+-rw-r--r--   0 bartz      (501) staff       (20)     4882 2023-07-20 07:13:47.000000 spotPython-0.6.8/src/spotPython/light/crossvalidationdatamodule.py
+-rw-r--r--   0 bartz      (501) staff       (20)     4120 2023-07-20 07:13:47.000000 spotPython-0.6.8/src/spotPython/light/csvdatamodule.py
+-rw-r--r--   0 bartz      (501) staff       (20)     3313 2023-07-17 21:43:36.000000 spotPython-0.6.8/src/spotPython/light/csvdataset.py
+-rw-r--r--   0 bartz      (501) staff       (20)     5546 2023-07-17 21:54:43.000000 spotPython-0.6.8/src/spotPython/light/litmodel.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1659 2023-06-25 16:06:47.000000 spotPython-0.6.8/src/spotPython/light/mnistdatamodule.py
+-rw-r--r--   0 bartz      (501) staff       (20)    12288 2023-07-18 19:40:25.000000 spotPython-0.6.8/src/spotPython/light/netlightbase.py
+-rw-r--r--   0 bartz      (501) staff       (20)    13445 2023-07-20 07:13:47.000000 spotPython-0.6.8/src/spotPython/light/netlinearbase.py
+-rw-r--r--   0 bartz      (501) staff       (20)    11119 2023-07-20 07:13:47.000000 spotPython-0.6.8/src/spotPython/light/traintest.py
+-rw-r--r--   0 bartz      (501) staff       (20)    11435 2023-07-20 07:13:47.000000 spotPython-0.6.8/src/spotPython/light/traintest_NEW.py
+-rw-r--r--   0 bartz      (501) staff       (20)    11131 2023-07-20 07:13:47.000000 spotPython-0.6.8/src/spotPython/light/traintest_OLD.py
+-rw-r--r--   0 bartz      (501) staff       (20)      255 2023-07-02 17:23:44.000000 spotPython-0.6.8/src/spotPython/light/utils.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.979033 spotPython-0.6.8/src/spotPython/plot/
+-rw-r--r--   0 bartz      (501) staff       (20)     1708 2023-07-23 21:37:57.000000 spotPython-0.6.8/src/spotPython/plot/contour.py
+-rw-r--r--   0 bartz      (501) staff       (20)     5949 2023-07-15 21:05:52.000000 spotPython-0.6.8/src/spotPython/plot/validation.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.979150 spotPython-0.6.8/src/spotPython/sklearn/
+-rw-r--r--   0 bartz      (501) staff       (20)     3715 2023-06-07 16:26:19.000000 spotPython-0.6.8/src/spotPython/sklearn/traintest.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.979267 spotPython-0.6.8/src/spotPython/spot/
+-rw-r--r--   0 bartz      (501) staff       (20)    39594 2023-07-15 20:52:28.000000 spotPython-0.6.8/src/spotPython/spot/spot.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.980500 spotPython-0.6.8/src/spotPython/torch/
+-rw-r--r--   0 bartz      (501) staff       (20)     1018 2023-06-23 13:29:53.000000 spotPython-0.6.8/src/spotPython/torch/activation.py
+-rw-r--r--   0 bartz      (501) staff       (20)      517 2023-05-31 19:01:06.000000 spotPython-0.6.8/src/spotPython/torch/dataframedataset.py
+-rw-r--r--   0 bartz      (501) staff       (20)      692 2023-06-27 22:26:23.000000 spotPython-0.6.8/src/spotPython/torch/initialization.py
+-rw-r--r--   0 bartz      (501) staff       (20)     4570 2023-07-15 20:49:35.000000 spotPython-0.6.8/src/spotPython/torch/mapk.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1012 2023-05-27 19:17:19.000000 spotPython-0.6.8/src/spotPython/torch/netcifar10.py
+-rw-r--r--   0 bartz      (501) staff       (20)      425 2023-05-27 19:21:33.000000 spotPython-0.6.8/src/spotPython/torch/netcore.py
+-rw-r--r--   0 bartz      (501) staff       (20)      803 2023-05-27 19:17:19.000000 spotPython-0.6.8/src/spotPython/torch/netfashionMNIST.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1071 2023-06-06 19:59:34.000000 spotPython-0.6.8/src/spotPython/torch/netregression.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1565 2023-06-01 18:55:33.000000 spotPython-0.6.8/src/spotPython/torch/netvbdp.py
+-rw-r--r--   0 bartz      (501) staff       (20)    14987 2023-06-20 05:35:32.000000 spotPython-0.6.8/src/spotPython/torch/traintest.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.981839 spotPython-0.6.8/src/spotPython/utils/
+-rw-r--r--   0 bartz      (501) staff       (20)     2019 2023-07-23 21:38:32.000000 spotPython-0.6.8/src/spotPython/utils/aggregate.py
+-rw-r--r--   0 bartz      (501) staff       (20)      498 2023-05-12 15:45:09.000000 spotPython-0.6.8/src/spotPython/utils/classes.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1484 2023-07-23 21:33:07.000000 spotPython-0.6.8/src/spotPython/utils/compare.py
+-rw-r--r--   0 bartz      (501) staff       (20)     3764 2023-07-15 20:51:00.000000 spotPython-0.6.8/src/spotPython/utils/convert.py
+-rw-r--r--   0 bartz      (501) staff       (20)      628 2023-07-15 21:01:58.000000 spotPython-0.6.8/src/spotPython/utils/device.py
+-rw-r--r--   0 bartz      (501) staff       (20)     9289 2023-07-15 20:33:18.000000 spotPython-0.6.8/src/spotPython/utils/eda.py
+-rw-r--r--   0 bartz      (501) staff       (20)     3299 2023-07-15 20:40:43.000000 spotPython-0.6.8/src/spotPython/utils/file.py
+-rw-r--r--   0 bartz      (501) staff       (20)     5846 2023-07-15 20:53:33.000000 spotPython-0.6.8/src/spotPython/utils/init.py
+-rw-r--r--   0 bartz      (501) staff       (20)     5028 2023-05-30 21:09:07.000000 spotPython-0.6.8/src/spotPython/utils/metrics.py
+-rw-r--r--   0 bartz      (501) staff       (20)      912 2023-06-01 22:37:01.000000 spotPython-0.6.8/src/spotPython/utils/progress.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1381 2023-07-23 21:38:50.000000 spotPython-0.6.8/src/spotPython/utils/repair.py
+-rw-r--r--   0 bartz      (501) staff       (20)     6826 2023-07-15 20:54:18.000000 spotPython-0.6.8/src/spotPython/utils/transform.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.974252 spotPython-0.6.8/src/spotPython.egg-info/
+-rw-r--r--   0 bartz      (501) staff       (20)     7578 2023-07-23 21:39:14.000000 spotPython-0.6.8/src/spotPython.egg-info/PKG-INFO
+-rw-r--r--   0 bartz      (501) staff       (20)     8273 2023-07-23 21:39:14.000000 spotPython-0.6.8/src/spotPython.egg-info/SOURCES.txt
+-rw-r--r--   0 bartz      (501) staff       (20)        1 2023-07-23 21:39:14.000000 spotPython-0.6.8/src/spotPython.egg-info/dependency_links.txt
+-rw-r--r--   0 bartz      (501) staff       (20)      216 2023-07-23 21:39:14.000000 spotPython-0.6.8/src/spotPython.egg-info/requires.txt
+-rw-r--r--   0 bartz      (501) staff       (20)       11 2023-07-23 21:39:14.000000 spotPython-0.6.8/src/spotPython.egg-info/top_level.txt
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 21:39:14.984480 spotPython-0.6.8/test/
+-rw-r--r--   0 bartz      (501) staff       (20)      873 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_aggregate_mean_var.py
+-rw-r--r--   0 bartz      (501) staff       (20)     4546 2023-04-09 19:57:56.000000 spotPython-0.6.8/test/test_build_Psi.py
+-rw-r--r--   0 bartz      (501) staff       (20)     4511 2023-04-09 19:58:12.000000 spotPython-0.6.8/test/test_build_U.py
+-rw-r--r--   0 bartz      (501) staff       (20)      797 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_build_psi_vec.py
+-rw-r--r--   0 bartz      (501) staff       (20)      917 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_evaluate_new_X.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1319 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_evaluate_new_solutions.py
+-rw-r--r--   0 bartz      (501) staff       (20)    10337 2023-04-09 19:58:51.000000 spotPython-0.6.8/test/test_extract_from_bounds.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2263 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_generate_design.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2223 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_infill.py
+-rw-r--r--   0 bartz      (501) staff       (20)      643 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_nat_to_cod.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1330 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_nat_to_cod_init.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1603 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_ocba.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1208 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_repair_non_numeric.py
+-rw-r--r--   0 bartz      (501) staff       (20)     4887 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_set_de_bounds.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2223 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_show_progress.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1131 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_suggest_new_X.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1765 2023-02-01 14:33:52.000000 spotPython-0.6.8/test/test_update_surrogate.py
+-rw-r--r--   0 bartz      (501) staff       (20)      130 2023-05-19 10:19:58.000000 spotPython-0.6.8/tox.ini
```

### Comparing `spotPython-0.6.6/.github/workflows/test.yml` & `spotPython-0.6.8/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/.gitignore` & `spotPython-0.6.8/.gitignore`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_contour_1_2.pdf` & `spotPython-0.6.8/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_contour_1_2.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_importance.pdf` & `spotPython-0.6.8/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_importance.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_progress.pdf` & `spotPython-0.6.8/Figures.d/11-torch_p040025_1min_3init_2023-04-26_22-37-22_progress.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_contour_2_3.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_contour_2_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_importance.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_importance.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_progress.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_1min_3init_2023-04-26_22-57-45_progress.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_1.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_1.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_2.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_2.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_3.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_4.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_0_4.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_2.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_2.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_3.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_4.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_1_4.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_2_3.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_2_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_2_4.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_2_4.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_3_4.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_contour_3_4.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_importance.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_importance.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_progress.pdf` & `spotPython-0.6.8/Figures.d/11-torch_s7cfd16_360min_10init_2023-04-27_07-25-12_progress.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_1.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_1.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_2.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_2.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_3.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_4.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_0_4.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_2.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_2.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_3.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_4.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_1_4.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_2_3.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_2_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_2_4.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_2_4.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_3_4.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_contour_3_4.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_importance.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_importance.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_progress.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_360min_20init_2023-05-07_23-36-22_progress.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_1_2.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_1_2.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_1_3.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_1_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_2_3.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_contour_2_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_importance.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_importance.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_progress.pdf` & `spotPython-0.6.8/Figures.d/12-torch_p040025_60min_20init_2023-05-07_21-33-26_progress.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/Figures.d/13-torch_s7cfd16_600min_20init_2023-05-05_18-52-19_contour_2_3.pdf` & `spotPython-0.6.8/Figures.d/13-torch_s7cfd16_600min_20init_2023-05-05_18-52-19_contour_2_3.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/LICENSE.txt` & `spotPython-0.6.8/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/PKG-INFO` & `spotPython-0.6.8/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotPython
-Version: 0.6.6
+Version: 0.6.8
 Summary: spotPython - Sequential Parameter Optimization in Python
 Author-email: "T. Bartz-Beielstein" <tbb@bartzundbartz.de>
 License: AGPL-3.0-or-later
 Project-URL: Homepage, https://www.spotseven.de
 Project-URL: Issues, https://github.com/sequential-parameter-optimization/spotPython/issues
 Project-URL: Repository, https://github.com/sequential-parameter-optimization/spotPython
 Classifier: Programming Language :: Python :: 3.10
```

### Comparing `spotPython-0.6.6/README.md` & `spotPython-0.6.8/README.md`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/docs/about.md` & `spotPython-0.6.8/docs/about.md`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/docs/examples.md` & `spotPython-0.6.8/docs/examples.md`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/docs/gen_ref_pages.py` & `spotPython-0.6.8/docs/gen_ref_pages.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/docs/images/favicon.png` & `spotPython-0.6.8/docs/images/favicon.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/docs/images/spotlogo.png` & `spotPython-0.6.8/docs/images/spotlogo.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/img/favicon.png` & `spotPython-0.6.8/img/favicon.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/img/spotLogo.png` & `spotPython-0.6.8/img/spotLogo.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/mkdocs.yml` & `spotPython-0.6.8/mkdocs.yml`

 * *Files 8% similar despite different names*

```diff
@@ -1,39 +1,57 @@
 site_name: spotPython
+site_description: spotPython - Sequential Parameter Optimization Toolbox in Python
 site_url: https://github.com/sequential-parameter-optimization/spotPython
 repo_url: https://github.com/sequential-parameter-optimization/spotPython/tree/main
+
+# Copyright
+copyright: Copyright &copy; 2004 - 2023
+
 nav:
 - Home: index.md
+- Code Reference: reference/
 - Documentation: hyperparameter-tuning-cookbook.md
 - Download: download.md
 - Examples: examples.md
-- Code Reference: reference/
 - About: about.md
+
 theme:
   name: material
   locale: en
   highlightjs: true
   favicon: images/favicon.png
   logo: images/spotlogo.png
+
   palette:
     # Palette toggle for light mode
     - media: "(prefers-color-scheme: light)"
       scheme: default
       primary: grey
+      accent: orange
       toggle:
         icon: material/brightness-7
         name: Switch to dark mode
 
     # Palette toggle for dark mode
     - media: "(prefers-color-scheme: dark)"
       scheme: slate
       primary: blue grey
+      accent: orange
       toggle:
         icon: material/brightness-4
         name: Switch to light mode
+  font:
+    text: Roboto
+    code: Fira Code
+  features:
+    - content.code.copy
+    - navigation.tabs
+    - navigation.instant
+    - navigation.indexes
+
 plugins:
     - search:
     - exclude:
         glob:
         - src/spotPython/_version.py
     - gen-files:
         scripts:
```

### Comparing `spotPython-0.6.6/notebooks/14_spot_ray_hpt_torch_cifar10.ipynb` & `spotPython-0.6.8/notebooks/14_spot_ray_hpt_torch_cifar10.ipynb`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/31_spot_lightning_csv.ipynb` & `spotPython-0.6.8/notebooks/31_spot_lightning_csv.ipynb`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/data/torch/model_spot_trained.pt` & `spotPython-0.6.8/notebooks/data/torch/model_spot_trained.pt`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/12-torch_p040025_1min_5init_2023-06-07_19-09-30_contour_0_1.png` & `spotPython-0.6.8/notebooks/figures/12-torch_p040025_1min_5init_2023-06-07_19-09-30_contour_0_1.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_contour_0_1.png` & `spotPython-0.6.8/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_contour_0_1.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_importance.png` & `spotPython-0.6.8/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_importance.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_progress.png` & `spotPython-0.6.8/notebooks/figures/14-torch_maans05_60min_20init_2023-06-08_10-52-59_progress.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_contour_0_1.png` & `spotPython-0.6.8/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_contour_0_1.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_progress.png` & `spotPython-0.6.8/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_progress.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_tensorboard_01.png` & `spotPython-0.6.8/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_tensorboard_01.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_tensorboard_02.png` & `spotPython-0.6.8/notebooks/figures/14-torch_p040025_10min_5init_2023-06-07_12-41-06_tensorboard_02.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/29-torch_bartz09_1min_5init_2023-06-24_21-45-17_importance.png` & `spotPython-0.6.8/notebooks/figures/29-torch_bartz09_1min_5init_2023-06-24_21-45-17_importance.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/29-torch_bartz09_1min_5init_2023-06-24_21-45-17_progress.png` & `spotPython-0.6.8/notebooks/figures/29-torch_bartz09_1min_5init_2023-06-24_21-45-17_progress.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_1.png` & `spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_1.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_3.png` & `spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_3.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_4.png` & `spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_0_4.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_1_3.png` & `spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_1_3.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_1_4.png` & `spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_1_4.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_3_4.png` & `spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_contour_3_4.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_importance.png` & `spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_importance.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_progress.png` & `spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_10init_2023-05-19_16-34-33_progress.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures14-torch_maans03_60min_20init_2023-05-27_23-10-01_parallel.png` & `spotPython-0.6.8/notebooks/figures/figures14-torch_maans03_60min_20init_2023-05-27_23-10-01_parallel.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_contour_0_3.png` & `spotPython-0.6.8/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_contour_0_3.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_importance.png` & `spotPython-0.6.8/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_importance.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_parallel.png` & `spotPython-0.6.8/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_parallel.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_progress.png` & `spotPython-0.6.8/notebooks/figures/figures24-torch_bartz09_10min_20init_2023-06-06_22-50-23_progress.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/spotModel.graffle` & `spotPython-0.6.8/notebooks/figures/spotModel.graffle`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/spotModel.pdf` & `spotPython-0.6.8/notebooks/figures/spotModel.pdf`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/spotModel.png` & `spotPython-0.6.8/notebooks/figures/spotModel.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/tensorboard_0.png` & `spotPython-0.6.8/notebooks/figures/tensorboard_0.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/tensorboard_1.png` & `spotPython-0.6.8/notebooks/figures/tensorboard_1.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/tensorboard_hdparams.png` & `spotPython-0.6.8/notebooks/figures/tensorboard_hdparams.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/notebooks/figures/tensorboard_parallel.png` & `spotPython-0.6.8/notebooks/figures/tensorboard_parallel.png`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/pyproject.toml` & `spotPython-0.6.8/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -3,15 +3,15 @@
   "setuptools>=61.0",
   "setuptools_scm[toml]"
 ]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "spotPython"
-version = "0.6.6"
+version = "0.6.8"
 authors = [
   { name="T. Bartz-Beielstein", email="tbb@bartzundbartz.de" }
 ]
 description = "spotPython - Sequential Parameter Optimization in Python"
 readme = "README.md"
 license = { text="AGPL-3.0-or-later" }
 requires-python = ">=3.10"
@@ -22,23 +22,24 @@
   "Operating System :: OS Independent",
 ]
 # PEP 621 dependencies declaration
 # adapt to your dependencies manager
 dependencies = [
   "lightning>=2.0.0rc0",
   "matplotlib",
+  "mkdocstrings-python",
   "numpy",
   "nbformat",
   "pandas",
   "plotly",
   "pytorch-lightning>=1.4",
   "river",
   "scikit-learn",
   "scipy",
-  "spotriver",
+  "spotRiver",
   "seaborn",
   "tabulate",
   "tensorboard",
   "torch",
   "torch-tb-profiler",
   "torchmetrics",
   "torchvision"
@@ -56,15 +57,12 @@
 [tool.setuptools.packages.find]
 where = ["src"]
 
 [tool.black]
 line-length = 120
 target-version = ["py310"]
 
-[tool.setuptools_scm]
-write_to = "src/spotPython/_version.py"
-
 [tool.pytest.ini_options]
 addopts = [
     "--import-mode=importlib",
 ]
```

### Comparing `spotPython-0.6.6/src/spotPython/budget/ocba.py` & `spotPython-0.6.8/src/spotPython/budget/ocba.py`

 * *Files 19% similar despite different names*

```diff
@@ -12,44 +12,36 @@
     """
     Optimal Computer Budget Allocation (OCBA)
 
     This function calculates the budget recommendations for a given set of means,
     variances, and incremental budget using the OCBA algorithm.
 
     References:
-        Chun-Hung Chen and Loo Hay Lee:
-        Stochastic Simulation Optimization: An Optimal Computer Budget Allocation,
-        pp. 49 and pp. 215
-
-        C.S.M Currie and T. Monks:
-        How to choose the best setup for a system. A tutorial for the Simulation Workshop 2021,
-        see:
-        https://colab.research.google.com/github/TomMonks/sim-tools/blob/master/examples/sw21_tutorial.ipynb
-        and
-        https://github.com/TomMonks/sim-tools
+        [1]: Chun-Hung Chen and Loo Hay Lee: Stochastic Simulation Optimization: An Optimal Computer Budget Allocation, pp. 49 and pp. 215
+        [2]: C.S.M Currie and T. Monks: How to choose the best setup for a system. A tutorial for the Simulation Workshop 2021, see:
+        [sw21_tutorial.ipynb](https://colab.research.google.com/github/TomMonks/sim-tools/blob/master/examples/sw21_tutorial.ipynb) and
+        [sim-tools](https://github.com/TomMonks/sim-tools)
 
     Args:
         means (numpy.array): An array of means.
         vars (numpy.array): An array of variances.
         delta (int): The incremental budget.
 
     Returns:
-        numpy.array: An array of budget recommendations.
+        (numpy.array): An array of budget recommendations.
 
     Note:
-        The implementation is based on the pseudo-code in the Chen et al. book (p. 49).
+        The implementation is based on the pseudo-code in the Chen et al. (p. 49), see [1].
 
     Examples:
-
         From the Chen et al. book (p. 49):
-        mean_y = np.array([1,2,3,4,5])
-        var_y = np.array([1,1,9,9,4])
-        get_ocba(mean_y, var_y, 50)
-
-        [11  9 19  9  2]
+        >>> mean_y = np.array([1,2,3,4,5])
+            var_y = np.array([1,1,9,9,4])
+            get_ocba(mean_y, var_y, 50)
+            [11  9 19  9  2]
     """
     n_designs = means.shape[0]
     allocations = zeros(n_designs, int32)
     ratios = zeros(n_designs, float64)
     budget = delta
     ranks = get_ranks(means)
     best, second_best = argpartition(ranks, 2)[:2]
@@ -88,12 +80,25 @@
     Args:
         X (numpy.ndarray): Input array to be repeated.
         means (list): List of means for each alternative.
         vars (list): List of variances for each alternative.
         delta (float): Indifference zone parameter.
 
     Returns:
-        numpy.ndarray: Repeated array of X along the specified axis based on the OCBA allocation.
+        (numpy.ndarray): Repeated array of X along the specified axis based on the OCBA allocation.
+
+    Examples:
+        >>> X = np.array([[1,2,3],[4,5,6]])
+            means = [1,2,3]
+            vars = [1,1,1]
+            delta = 50
+            get_ocba_X(X, means, vars, delta)
+            array([[1, 2, 3],
+                     [1, 2, 3],
+                        [1, 2, 3],
+                        [4, 5, 6],
+                        [4, 5, 6],
+                        [4, 5, 6]])
 
     """
     o = get_ocba(means=means, vars=vars, delta=delta)
     return repeat(X, o, axis=0)
```

### Comparing `spotPython-0.6.6/src/spotPython/build/kriging.py` & `spotPython-0.6.8/src/spotPython/build/kriging.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,7 @@
-from __future__ import annotations
-
-# google-style docstring documentation, type information, an example, and return values: 2023, July, 15th
-# tests: None
-
 import copy
 from math import erf
 import matplotlib.pyplot as plt
 from numpy import min, std, var, mean
 from numpy import sqrt
 from numpy import exp
 from numpy import array
@@ -43,14 +38,53 @@
 # add formatter to the handler
 py_handler.setFormatter(py_formatter)
 # add handler to the logger
 logger.addHandler(py_handler)
 
 
 class Kriging(surrogates):
+    """Kriging surrogate.
+
+    Attributes:
+        nat_range_X (list):
+            List of X natural ranges.
+        nat_range_y (list):
+            List of y nat ranges.
+        noise (bool):
+            noisy objective function. Default: False. If `True`, regression kriging will be used.
+        var_type (str):
+            variable type. Can be either `"num`" (numerical) of `"factor"` (factor).
+        num_mask (array):
+            array of bool variables. `True` represent numerical (float) variables.
+        factor_mask (array):
+            array of factor variables. `True` represents factor (unordered) variables.
+        int_mask (array):
+            array of integer variables. `True` represents integers (ordered) variables.
+        ordered_mask (array):
+            array of ordered variables. `True` represents integers or float (ordered) variables.
+            Set of veriables which an order relation, i.e., they are either num (float) or int.
+        name (str):
+            Surrogate name
+        seed (int):
+            Random seed.
+        use_cod_y (bool):
+            Use coded y values.
+        sigma (float):
+            Kriging sigma.
+        gen (method):
+            Design generator, e.g., spotPython.design.spacefilling.spacefilling.
+        min_theta (float):
+            min log10 theta value. Defaults: -6.
+        max_theta (float):
+            max log10 theta value. Defaults: 3.
+        min_p (float):
+            min p value. Default: 1.
+        max_p (float):
+            max p value. Default: 2.
+    """
     def __init__(
             self: object,
             noise: bool = False,
             cod_type: Optional[str] = "norm",
             var_type: List[str] = ["num"],
             use_cod_y: bool = False,
             name: str = "kriging",
@@ -64,15 +98,15 @@
             optim_p: bool = False,
             log_level: int = 50,
             spot_writer=None,
             counter=None,
             **kwargs
     ):
         """
-        Kriging surrogate.
+        Initialize the Kriging surrogate.
 
         Args:
             noise (bool): Use regression instead of interpolation kriging. Defaults to False.
             cod_type (Optional[str]):
                 Normalize or standardize X and values.
                 Can be None, "norm", or "std". Defaults to "norm".
             var_type (List[str]):
@@ -88,81 +122,47 @@
             n_theta (int): Number of theta values. Defaults to 1.
             n_p (int): Number of p values. Defaults to 1.
             optim_p (bool): Determines whether p should be optimized.
             log_level (int): Logging level, e.g., 20 is "INFO". Defaults to 50 ("CRITICAL").
             spot_writer : Spot writer.
             counter : Counter.
 
-        Attributes:
-            nat_range_X (list):
-                List of X natural ranges.
-            nat_range_y (list):
-                List of y nat ranges.
-            noise (bool):
-                noisy objective function. Default: False. If `True`, regression kriging will be used.
-            var_type (str):
-                variable type. Can be either `"num`" (numerical) of `"factor"` (factor).
-            num_mask (array):
-                array of bool variables. `True` represent numerical (float) variables.
-            factor_mask (array):
-                array of factor variables. `True` represents factor (unordered) variables.
-            int_mask (array):
-                array of integer variables. `True` represents integers (ordered) variables.
-            ordered_mask (array):
-                array of ordered variables. `True` represents integers or float (ordered) variables.
-                Set of veriables which an order relation, i.e., they are either num (float) or int.
-            name (str):
-                Surrogate name
-            seed (int):
-                Random seed.
-            use_cod_y (bool):
-                Use coded y values.
-            sigma (float):
-                Kriging sigma.
-            gen (method):
-                Design generator, e.g., spotPython.design.spacefilling.spacefilling.
-            min_theta (float):
-                min log10 theta value. Defaults: -6.
-            max_theta (float):
-                max log10 theta value. Defaults: 3.
-            min_p (float):
-                min p value. Default: 1.
-            max_p (float):
-                max p value. Default: 2.
-
         Examples:
-            Surrogate of the x*sin(x) function.
-            See:
-            [scikit-learn](https://scikit-learn.org/stable/auto_examples/gaussian_process/plot_gpr_noisy_targets.html)
+            Surrogate of the x*sin(x) function, see [1].
 
             >>> from spotPython.build.kriging import Kriging
-            >>> import numpy as np
-            >>> import matplotlib.pyplot as plt
-            >>> rng = np.random.RandomState(1)
-            >>> X = linspace(start=0, stop=10, num=1_000).reshape(-1, 1)
-            >>> y = np.squeeze(X * np.sin(X))
-            >>> training_indices = rng.choice(arange(y.size), size=6, replace=False)
-            >>> X_train, y_train = X[training_indices], y[training_indices]
-            >>> S = Kriging(name='kriging', seed=124)
-            >>> S.fit(X_train, y_train)
-            >>> mean_prediction, std_prediction = S.predict(X)
-            >>> plt.plot(X, y, label=r"$f(x)$", linestyle="dotted")
-            >>> plt.scatter(X_train, y_train, label="Observations")
-            >>> plt.plot(X, mean_prediction, label="Mean prediction")
-            >>> plt.fill_between(
-                X.ravel(),
-                mean_prediction - 1.96 * std_prediction,
-                mean_prediction + 1.96 * std_prediction,
-                alpha=0.5,
-                label=r"95% confidence interval",
-                )
-            >>> plt.legend()
-            >>> plt.xlabel("$x$")
-            >>> plt.ylabel("$f(x)$")
-            >>> _ = plt.title("Gaussian process regression on noise-free dataset")
+                import numpy as np
+                import matplotlib.pyplot as plt
+                rng = np.random.RandomState(1)
+                X = linspace(start=0, stop=10, num=1_000).reshape(-1, 1)
+                y = np.squeeze(X * np.sin(X))
+                training_indices = rng.choice(arange(y.size), size=6, replace=False)
+                X_train, y_train = X[training_indices], y[training_indices]
+                S = Kriging(name='kriging', seed=124)
+                S.fit(X_train, y_train)
+                mean_prediction, std_prediction = S.predict(X)
+                plt.plot(X, y, label=r"$f(x)$", linestyle="dotted")
+                plt.scatter(X_train, y_train, label="Observations")
+                plt.plot(X, mean_prediction, label="Mean prediction")
+                plt.fill_between(
+                    X.ravel(),
+                    mean_prediction - 1.96 * std_prediction,
+                    mean_prediction + 1.96 * std_prediction,
+                    alpha=0.5,
+                    label=r"95% confidence interval",
+                    )
+                plt.legend()
+                plt.xlabel("$x$")
+                plt.ylabel("$f(x)$")
+                _ = plt.title("Gaussian process regression on noise-free dataset")
+                plt.show()
+
+        References:
+
+            [[1](https://scikit-learn.org/stable/auto_examples/gaussian_process/plot_gpr_noisy_targets.html)] scikit-learn: Gaussian Processes regression: basic introductory example
 
         """
         super().__init__(name, seed, log_level)
 
         self.noise = noise
         self.var_type = var_type
         self.cod_type = cod_type
```

### Comparing `spotPython-0.6.6/src/spotPython/data/base.py` & `spotPython-0.6.8/src/spotPython/data/base.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/data/light_hyper_dict.json` & `spotPython-0.6.8/src/spotPython/data/light_hyper_dict.json`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/data/light_hyper_dict.py` & `spotPython-0.6.8/src/spotPython/data/light_hyper_dict.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/data/sklearn_hyper_dict.json` & `spotPython-0.6.8/src/spotPython/data/sklearn_hyper_dict.json`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/data/sklearn_hyper_dict.py` & `spotPython-0.6.8/src/spotPython/data/sklearn_hyper_dict.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/data/torch_hyper_dict.json` & `spotPython-0.6.8/src/spotPython/data/torch_hyper_dict.json`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/data/torch_hyper_dict.py` & `spotPython-0.6.8/src/spotPython/data/torch_hyper_dict.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/data/torchdata.py` & `spotPython-0.6.8/src/spotPython/data/torchdata.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/data/vbdp.py` & `spotPython-0.6.8/src/spotPython/data/vbdp.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/design/designs.py` & `spotPython-0.6.8/src/spotPython/design/designs.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/design/factorial.py` & `spotPython-0.6.8/src/spotPython/design/factorial.py`

 * *Files 9% similar despite different names*

```diff
@@ -28,17 +28,18 @@
 
         Args:
             p (int): The number of levels for each factor.
 
         Returns:
             numpy.ndarray: A 2D array representing the full factorial design.
 
-        Example:
-            >>> factorial_design = factorial(k=2)
-            >>> factorial_design.full_factorial(p=2)
-            array([[0., 0.],
-                   [0., 1.],
-                   [1., 0.],
-                   [1., 1.]])
+        Examples:
+            >>> from spotPython.design.factorial import factorial
+                factorial_design = factorial(k=2)
+                factorial_design.full_factorial(p=2)
+                array([[0., 0.],
+                    [0., 1.],
+                    [1., 0.],
+                    [1., 1.]])
         """
         i = (slice(0, 1, p * 1j),) * self.k
         return mgrid[i].reshape(self.k, p**self.k).T
```

### Comparing `spotPython-0.6.6/src/spotPython/design/spacefilling.py` & `spotPython-0.6.8/src/spotPython/design/spacefilling.py`

 * *Files 2% similar despite different names*

```diff
@@ -35,29 +35,29 @@
             repeats (int): number of repeats (replicates)
             lower (int or float, optional): lower bound. Defaults to 0.
             upper (int or float, optional): upper bound. Defaults to 1.
 
         Returns:
             (ndarray): Latin hypercube design.
 
-        Example:
+        Examples:
             >>> from spotPython.design.spacefilling import spacefilling
-            >>> import numpy as np
-            >>> lhd = spacefilling(k=2, seed=123)
-            >>> lhd.scipy_lhd(n=5, repeats=2, lower=np.array([0,0]), upper=np.array([1,1]))
-            array([[0.66352963, 0.5892358 ],
-                   [0.66352963, 0.5892358 ],
-                   [0.55592803, 0.96312564],
-                   [0.55592803, 0.96312564],
-                   [0.16481882, 0.0375811 ],
-                   [0.16481882, 0.0375811 ],
-                   [0.215331  , 0.34468512],
-                   [0.215331  , 0.34468512],
-                   [0.83604909, 0.62202146],
-                   [0.83604909, 0.62202146]])
+                import numpy as np
+                lhd = spacefilling(k=2, seed=123)
+                lhd.scipy_lhd(n=5, repeats=2, lower=np.array([0,0]), upper=np.array([1,1]))
+                array([[0.66352963, 0.5892358 ],
+                    [0.66352963, 0.5892358 ],
+                    [0.55592803, 0.96312564],
+                    [0.55592803, 0.96312564],
+                    [0.16481882, 0.0375811 ],
+                    [0.16481882, 0.0375811 ],
+                    [0.215331  , 0.34468512],
+                    [0.215331  , 0.34468512],
+                    [0.83604909, 0.62202146],
+                    [0.83604909, 0.62202146]])
         """
         if lower is None:
             lower = zeros(self.k)
         if upper is None:
             upper = ones(self.k)
         sample = self.sampler.random(n=n)
         des = scale(sample, lower, upper)
```

### Comparing `spotPython-0.6.6/src/spotPython/fun/hyperlight.py` & `spotPython-0.6.8/src/spotPython/fun/hyperlight.py`

 * *Files 1% similar despite different names*

```diff
@@ -99,18 +99,18 @@
 
         Returns:
             (np.ndarray):
                 array containing the evaluation results.
 
         Examples:
             >>> hyper_light = HyperLight(seed=126, log_level=50)
-            >>> X = np.array([[1, 2], [3, 4]])
-            >>> fun_control = {"weights": np.array([1, 0, 0])}
-            >>> hyper_light.fun(X, fun_control)
-            array([nan, nan])
+                X = np.array([[1, 2], [3, 4]])
+                fun_control = {"weights": np.array([1, 0, 0])}
+                hyper_light.fun(X, fun_control)
+                array([nan, nan])
         """
         z_res = np.array([], dtype=float)
         if fun_control is not None:
             self.fun_control.update(fun_control)
         self.check_X_shape(X)
         var_dict = assign_values(X, self.fun_control["var_name"])
         # type information and transformations are considered in generate_one_config_from_var_dict:
```

### Comparing `spotPython-0.6.6/src/spotPython/fun/hypersklearn.py` & `spotPython-0.6.8/src/spotPython/fun/hypersklearn.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/fun/hypertorch.py` & `spotPython-0.6.8/src/spotPython/fun/hypertorch.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/fun/objectivefunctions.py` & `spotPython-0.6.8/src/spotPython/fun/objectivefunctions.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/hyperparameters/categorical.py` & `spotPython-0.6.8/src/spotPython/hyperparameters/categorical.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 def one_hot_encode(strings) -> dict:
     """One hot encode a list of strings.
     Arguments:
         strings (list): List of strings to encode.
     Returns:
         dict: Dictionary of strings and their one hot encoded values.
-    Example:
+    Examples:
         >>> one_hot_encode(['a', 'b', 'c'])
         {'a': [1, 0, 0], 'b': [0, 1, 0], 'c': [0, 0, 1]}
     """
     n = len(strings)
     encoding_dict = {}
     for i, string in enumerate(strings):
         one_hot_encoded_value = [0] * n
@@ -26,15 +26,15 @@
     Args:
         strings (list): List of strings to encode.
         encoding_dict (dict): Dictionary of strings and their one hot encoded values.
 
     Returns:
         int: Decimal value of the sum of the encoded values.
 
-    Example:
+    Examples:
         >>> encoding_dict = {'a': [1, 0, 0], 'b': [0, 1, 0], 'c': [0, 0, 1]}
             sum_encoded_values(['a', 'b', 'c'], encoding_dict)
             7
             sum_encoded_values(['a', 'c'], encoding_dict)
             5
     """
     result = [0] * len(list(encoding_dict.values())[0])
@@ -53,15 +53,15 @@
     Arguments:
         alg (str): Name of the algorithm.
         hyper_param (str): Name of the hyper parameter.
         d (dict): Dictionary of algorithms and their hyperparameters.
         filename (str): Name of the file containing the dictionary.
     Returns:
         dict: Dictionary of hyper parameter values and their one hot encoded values.
-    Example:
+    Examples:
         >>> alg = "HoeffdingAdaptiveTreeClassifier"
             hyper_param = "split_criterion"
             d = {
                 "HoeffdingAdaptiveTreeClassifier": {
                     "split_criterion": ["gini", "info_gain", "hellinger"],
                     "leaf_prediction": ["mc", "nb", "nba"],
                     "bootstrap_sampling": ["0", "1"]
@@ -89,15 +89,15 @@
     Arguments:
         a (list): List of elements to check.
         b (list): List of elements to add to.
 
     Returns:
         list: List of elements with missing elements from list a added.
 
-    Example:
+    Examples:
         >>> a = [1, 4]
             b = [1, 2]
             add_missing_elements(a, b)
             [1, 2, 4]
     """
     for element in a:
         if element not in b:
@@ -112,15 +112,15 @@
 
     Arguments:
         integer_value (int): The integer value to find the closest key for.
         encoding_dict (dict): The encoding dictionary that maps keys to binary values.
     Returns:
         str: The key in the encoding dictionary whose binary value is
         closest to the binary representation of the integer value.
-    Example:
+    Examples:
         >>> encoding_dict = {'A': [1, 0, 0], 'B': [0, 1, 0], 'C': [0, 0, 1]}
             find_closest_key(6, encoding_dict)
             'B'
     """
     binary_value = [int(x) for x in format(integer_value, f"0{len(list(encoding_dict.values())[0])}b")]
     min_distance = float("inf")
     closest_key = None
```

### Comparing `spotPython-0.6.6/src/spotPython/hyperparameters/optimizer.py` & `spotPython-0.6.8/src/spotPython/hyperparameters/optimizer.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/hyperparameters/values.py` & `spotPython-0.6.8/src/spotPython/hyperparameters/values.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/light/cifar10datamodule.py` & `spotPython-0.6.8/src/spotPython/light/cifar10datamodule.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/light/crossvalidationdatamodule.py` & `spotPython-0.6.8/src/spotPython/light/crossvalidationdatamodule.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,15 +11,15 @@
     A LightningDataModule for handling cross-validation data splits.
 
     Args:
         batch_size (int): The size of the batch. Defaults to 64.
         k (int): The fold number. Defaults to 1.
         split_seed (int): The random seed for splitting the data. Defaults to 42.
         num_splits (int): The number of splits for cross-validation. Defaults to 10.
-        DATASET_PATH (str): The path to the dataset. Defaults to "./data".
+        data_dir (str): The path to the dataset. Defaults to "./data".
         num_workers (int): The number of workers for data loading. Defaults to 0.
         pin_memory (bool): Whether to pin memory for data loading. Defaults to False.
 
     Attributes:
         data_train (Optional[Dataset]): The training dataset.
         data_val (Optional[Dataset]): The validation dataset.
     Examples:
@@ -36,21 +36,21 @@
 
     def __init__(
         self,
         batch_size=64,
         k: int = 1,
         split_seed: int = 42,
         num_splits: int = 10,
-        DATASET_PATH: str = "./data",
+        data_dir: str = "./data",
         num_workers: int = 0,
         pin_memory: bool = False,
     ):
         super().__init__()
         self.batch_size = batch_size
-        self.DATASET_PATH = DATASET_PATH
+        self.data_dir = data_dir
         self.num_workers = num_workers
         self.k = k
         self.split_seed = split_seed
         self.num_splits = num_splits
         self.pin_memory = pin_memory
         self.save_hyperparameters(logger=False)
         assert 0 <= self.k < self.num_splits, "incorrect fold number"
```

### Comparing `spotPython-0.6.6/src/spotPython/light/csvdatamodule.py` & `spotPython-0.6.8/src/spotPython/light/csvdatamodule.py`

 * *Files 8% similar despite different names*

```diff
@@ -6,24 +6,24 @@
 
 class CSVDataModule(L.LightningDataModule):
     """
     A LightningDataModule for handling CSV data.
 
     Args:
         batch_size (int): The size of the batch.
-        DATASET_PATH (str): The path to the dataset. Defaults to "./data".
+        data_dir (str): The path to the dataset. Defaults to "./data".
         num_workers (int): The number of workers for data loading. Defaults to 0.
 
     Attributes:
         data_train (Dataset): The training dataset.
         data_val (Dataset): The validation dataset.
         data_test (Dataset): The test dataset.
     """
 
-    def __init__(self, batch_size: int, DATASET_PATH: str = "./data", num_workers: int = 0):
+    def __init__(self, batch_size: int, data_dir: str = "./data", num_workers: int = 0):
         super().__init__()
         self.batch_size = batch_size
         self.num_workers = num_workers
 
     def prepare_data(self) -> None:
         """Prepares the data for use."""
         # download
```

### Comparing `spotPython-0.6.6/src/spotPython/light/csvdataset.py` & `spotPython-0.6.8/src/spotPython/light/csvdataset.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/light/litmodel.py` & `spotPython-0.6.8/src/spotPython/light/litmodel.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/light/mnistdatamodule.py` & `spotPython-0.6.8/src/spotPython/light/mnistdatamodule.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/light/netlightbase.py` & `spotPython-0.6.8/src/spotPython/light/netlightbase.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/light/netlinearbase.py` & `spotPython-0.6.8/src/spotPython/light/netlinearbase.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/light/traintest.py` & `spotPython-0.6.8/src/spotPython/light/traintest_OLD.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/light/traintest_NEW.py` & `spotPython-0.6.8/src/spotPython/light/traintest_NEW.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/light/traintest_OLD.py` & `spotPython-0.6.8/src/spotPython/light/traintest.py`

 * *Files 2% similar despite different names*

```diff
@@ -58,15 +58,15 @@
         pass
     # print(f"model: {model}")
 
     # Init DataModule
     dm = CSVDataModule(
         batch_size=config["batch_size"],
         num_workers=fun_control["num_workers"],
-        DATASET_PATH=fun_control["DATASET_PATH"],
+        data_dir=fun_control["DATASET_PATH"],
     )
 
     # Init trainer
     trainer = L.Trainer(
         # Where to save models
         default_root_dir=os.path.join(fun_control["CHECKPOINT_PATH"], config_id),
         max_epochs=model.hparams.epochs,
@@ -126,15 +126,15 @@
         enable_progress_bar = fun_control["enable_progress_bar"]
     # Add "TEST" postfix to config_id
     config_id = generate_config_id(config) + "_TEST"
     # Init DataModule
     dm = CSVDataModule(
         batch_size=config["batch_size"],
         num_workers=fun_control["num_workers"],
-        DATASET_PATH=fun_control["DATASET_PATH"],
+        data_dir=fun_control["DATASET_PATH"],
     )
     # Init model from datamodule's attributes
     model = fun_control["core_model"](**config, _L_in=_L_in, _L_out=_L_out)
     initialization = config["initialization"]
     if initialization == "Xavier":
         xavier_init(model)
     elif initialization == "Kaiming":
@@ -220,15 +220,15 @@
         # print(f"model: {model}")
 
         dm = CrossValidationDataModule(
             k=k,
             num_splits=num_folds,
             split_seed=split_seed,
             batch_size=config["batch_size"],
-            DATASET_PATH=fun_control["DATASET_PATH"],
+            data_dir=fun_control["DATASET_PATH"],
         )
         dm.prepare_data()
         dm.setup()
 
         # Init trainer
         trainer = L.Trainer(
             # Where to save models
```

### Comparing `spotPython-0.6.6/src/spotPython/plot/contour.py` & `spotPython-0.6.8/src/spotPython/plot/contour.py`

 * *Files 6% similar despite different names*

```diff
@@ -23,20 +23,20 @@
         min_y (int, optional): _description_. Defaults to -1.
         max_y (int, optional): _description_. Defaults to 1.
         min_z (int, optional): _description_. Defaults to 0.
         max_z (int, optional): _description_. Defaults to 1.
         n_samples (int, optional): _description_. Defaults to 100.
         n_levels (int, optional): _description_. Defaults to 5.
 
-    Example:
+    Examples:
         >>> import matplotlib.pyplot as plt
-        >>> import numpy as np
-        >>> from spotPython.fun.objectivefunctions import analytical
-        >>> fun = analytical().fun_branin
-        >>> simple_contour(fun=fun, n_levels=30, min_x=-5, max_x=10, min_y=0, max_y=15)
+            import numpy as np
+            from spotPython.fun.objectivefunctions import analytical
+            fun = analytical().fun_branin
+            simple_contour(fun=fun, n_levels=30, min_x=-5, max_x=10, min_y=0, max_y=15)
 
     """
     XX, YY = np.meshgrid(np.linspace(min_x, max_x, n_samples), np.linspace(min_y, max_y, n_samples))
     zz = np.array([fun(np.array([xi, yi]).reshape(-1, 2)) for xi, yi in zip(np.ravel(XX), np.ravel(YY))]).reshape(
         n_samples, n_samples
     )
     fig, ax = plt.subplots(figsize=(5, 2.7), layout="constrained")
```

### Comparing `spotPython-0.6.6/src/spotPython/plot/validation.py` & `spotPython-0.6.8/src/spotPython/plot/validation.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/sklearn/traintest.py` & `spotPython-0.6.8/src/spotPython/sklearn/traintest.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/spot/spot.py` & `spotPython-0.6.8/src/spotPython/spot/spot.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/torch/activation.py` & `spotPython-0.6.8/src/spotPython/torch/activation.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/torch/dataframedataset.py` & `spotPython-0.6.8/src/spotPython/torch/dataframedataset.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/torch/initialization.py` & `spotPython-0.6.8/src/spotPython/torch/initialization.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/torch/mapk.py` & `spotPython-0.6.8/src/spotPython/torch/mapk.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/torch/netcifar10.py` & `spotPython-0.6.8/src/spotPython/torch/netcifar10.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/torch/netfashionMNIST.py` & `spotPython-0.6.8/src/spotPython/torch/netfashionMNIST.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/torch/netregression.py` & `spotPython-0.6.8/src/spotPython/torch/netregression.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/torch/netvbdp.py` & `spotPython-0.6.8/src/spotPython/torch/netvbdp.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/torch/traintest.py` & `spotPython-0.6.8/src/spotPython/torch/traintest.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/utils/aggregate.py` & `spotPython-0.6.8/src/spotPython/utils/aggregate.py`

 * *Files 2% similar despite different names*

```diff
@@ -12,25 +12,25 @@
         sort (bool): Whether to sort the resulting DataFrame by the group keys.
 
     Returns:
         (numpy.ndarray): aggregated `X` values, shape `(n-m, k)`, if `m` duplicates in `X`.
         (numpy.ndarray): aggregated (mean per group) `y` values, shape `(1,)`, if `m` duplicates in `X`.
         (numpy.ndarray): aggregated (variance per group) `y` values, shape `(1,)`, if `m` duplicates in `X`.
 
-    Example:
+    Examples:
         >>> X = np.array([[1, 2], [3, 4], [1, 2]])
-        >>> y = np.array([1, 2, 3])
-        >>> X_agg, y_mean, y_var = aggregate_mean_var(X, y)
-        >>> print(X_agg)
-        [[1. 2.]
-         [3. 4.]]
-        >>> print(y_mean)
-        [2. 2.]
-        >>> print(y_var)
-        [1. 0.]
+            y = np.array([1, 2, 3])
+            X_agg, y_mean, y_var = aggregate_mean_var(X, y)
+            print(X_agg)
+            [[1. 2.]
+            [3. 4.]]
+            print(y_mean)
+            [2. 2.]
+            print(y_var)
+            [1. 0.]
     """
     # Create a DataFrame from X and y
     df = pd.DataFrame(X)
     df["y"] = y
 
     # Group by all columns except 'y' and calculate the mean and variance of 'y' for each group
     grouped = df.groupby(list(df.columns.difference(["y"])), as_index=False, sort=sort)
```

### Comparing `spotPython-0.6.6/src/spotPython/utils/compare.py` & `spotPython-0.6.8/src/spotPython/utils/compare.py`

 * *Files 12% similar despite different names*

```diff
@@ -12,14 +12,22 @@
         A (numpy.ndarray): A array with new values
         X (numpy.ndarray): X array with known values
         tolerance (float): tolerance value for comparison
 
     Returns:
         (numpy.ndarray): array with unknown (new) values
         (numpy.ndarray): array with `True` if value is new, otherwise `False`.
+
+    Examples:
+        >>> from spotPython.utils.compare import selectNew
+            A = np.array([[1,2,3],[4,5,6]])
+            X = np.array([[1,2,3],[4,5,6]])
+            selectNew(A, X)
+            (array([], shape=(0, 3), dtype=int64), array([], dtype=bool))
+
     """
     B = np.abs(A[:, None] - X)
     ind = np.any(np.all(B <= tolerance, axis=2), axis=1)
     return A[~ind], ~ind
 
 
 def find_equal_in_lists(a: List[int], b: List[int]) -> List[int]:
@@ -27,16 +35,16 @@
 
     Args:
         a (list): list with a values
         b (list): list with b values
 
     Returns:
         list: list with 1 if equal, otherwise 0
-    Example:
-        >>> a = [1, 2, 3, 4, 5]
-        >>> b = [1, 2, 3, 4, 5]
-        >>> find_equal_in_lists(a, b)
-        [1, 1, 1, 1, 1]
+    Examples:
+        >>> from spotPython.utils.compare import find_equal_in_lists
+            a = [1, 2, 3, 4, 5]
+            b = [1, 2, 3, 4, 5]
+            find_equal_in_lists(a, b)
+            [1, 1, 1, 1, 1]
     """
     equal = [1 if a[i] == b[i] else 0 for i in range(len(a))]
     return equal
-    return equal
```

### Comparing `spotPython-0.6.6/src/spotPython/utils/convert.py` & `spotPython-0.6.8/src/spotPython/utils/convert.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/utils/device.py` & `spotPython-0.6.8/src/spotPython/utils/device.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/utils/eda.py` & `spotPython-0.6.8/src/spotPython/utils/eda.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/utils/file.py` & `spotPython-0.6.8/src/spotPython/utils/file.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/utils/init.py` & `spotPython-0.6.8/src/spotPython/utils/init.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/utils/metrics.py` & `spotPython-0.6.8/src/spotPython/utils/metrics.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/utils/progress.py` & `spotPython-0.6.8/src/spotPython/utils/progress.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython/utils/repair.py` & `spotPython-0.6.8/src/spotPython/utils/repair.py`

 * *Files 17% similar despite different names*

```diff
@@ -10,15 +10,15 @@
     Args:
         X (numpy.ndarray): X array
         var_type (list): list with type information
 
     Returns:
         numpy.ndarray: X array with non-numeric values rounded to integers
 
-    Example:
+    Examples:
         >>> X = np.array([[1.2, 2.3], [3.4, 4.5]])
         >>> var_type = ["num", "factor"]
         >>> repair_non_numeric(X, var_type)
         array([[1., 2.],
                [3., 4.]])
     """
     mask = np.isin(var_type, ["num", "float"], invert=True)
@@ -33,15 +33,15 @@
     Args:
         X (numpy.ndarray): X array
         y (numpy.ndarray): y array
 
     Returns:
         Tuple[numpy.ndarray, numpy.ndarray]: X and y arrays with rows containing NaN values in y removed
 
-    Example:
+    Examples:
         >>> X = np.array([[1, 2], [3, 4], [5, 6]])
         >>> y = np.array([1, np.nan, 2])
         >>> remove_nan(X, y)
         (array([[1, 2],
                 [5, 6]]), array([1., 2.]))
     """
     ind = np.isfinite(y)
```

### Comparing `spotPython-0.6.6/src/spotPython/utils/transform.py` & `spotPython-0.6.8/src/spotPython/utils/transform.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/src/spotPython.egg-info/PKG-INFO` & `spotPython-0.6.8/src/spotPython.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotPython
-Version: 0.6.6
+Version: 0.6.8
 Summary: spotPython - Sequential Parameter Optimization in Python
 Author-email: "T. Bartz-Beielstein" <tbb@bartzundbartz.de>
 License: AGPL-3.0-or-later
 Project-URL: Homepage, https://www.spotseven.de
 Project-URL: Issues, https://github.com/sequential-parameter-optimization/spotPython/issues
 Project-URL: Repository, https://github.com/sequential-parameter-optimization/spotPython
 Classifier: Programming Language :: Python :: 3.10
```

### Comparing `spotPython-0.6.6/src/spotPython.egg-info/SOURCES.txt` & `spotPython-0.6.8/src/spotPython.egg-info/SOURCES.txt`

 * *Files 0% similar despite different names*

```diff
@@ -84,15 +84,14 @@
 notebooks/figures/spotModel.graffle
 notebooks/figures/spotModel.pdf
 notebooks/figures/spotModel.png
 notebooks/figures/tensorboard_0.png
 notebooks/figures/tensorboard_1.png
 notebooks/figures/tensorboard_hdparams.png
 notebooks/figures/tensorboard_parallel.png
-src/spotPython/_version.py
 src/spotPython.egg-info/PKG-INFO
 src/spotPython.egg-info/SOURCES.txt
 src/spotPython.egg-info/dependency_links.txt
 src/spotPython.egg-info/requires.txt
 src/spotPython.egg-info/top_level.txt
 src/spotPython/budget/ocba.py
 src/spotPython/build/kriging.py
```

### Comparing `spotPython-0.6.6/test/test_aggregate_mean_var.py` & `spotPython-0.6.8/test/test_aggregate_mean_var.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_build_Psi.py` & `spotPython-0.6.8/test/test_build_Psi.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_build_U.py` & `spotPython-0.6.8/test/test_build_U.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_build_psi_vec.py` & `spotPython-0.6.8/test/test_build_psi_vec.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_evaluate_new_X.py` & `spotPython-0.6.8/test/test_evaluate_new_X.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_evaluate_new_solutions.py` & `spotPython-0.6.8/test/test_evaluate_new_solutions.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_extract_from_bounds.py` & `spotPython-0.6.8/test/test_extract_from_bounds.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_generate_design.py` & `spotPython-0.6.8/test/test_generate_design.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_infill.py` & `spotPython-0.6.8/test/test_infill.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_nat_to_cod.py` & `spotPython-0.6.8/test/test_nat_to_cod.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_nat_to_cod_init.py` & `spotPython-0.6.8/test/test_nat_to_cod_init.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_ocba.py` & `spotPython-0.6.8/test/test_ocba.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_repair_non_numeric.py` & `spotPython-0.6.8/test/test_repair_non_numeric.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_set_de_bounds.py` & `spotPython-0.6.8/test/test_set_de_bounds.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_show_progress.py` & `spotPython-0.6.8/test/test_show_progress.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_suggest_new_X.py` & `spotPython-0.6.8/test/test_suggest_new_X.py`

 * *Files identical despite different names*

### Comparing `spotPython-0.6.6/test/test_update_surrogate.py` & `spotPython-0.6.8/test/test_update_surrogate.py`

 * *Files identical despite different names*

