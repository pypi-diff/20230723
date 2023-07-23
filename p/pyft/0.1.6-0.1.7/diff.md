# Comparing `tmp/pyft-0.1.6.tar.gz` & `tmp/pyft-0.1.7.tar.gz`

## Comparing `pyft-0.1.6.tar` & `pyft-0.1.7.tar`

### file list

```diff
@@ -1,91 +1,91 @@
--rw-r--r--   0        0        0      462 1970-01-01 00:00:00.000000 pyft-0.1.6/local_dependencies/bamlift/Cargo.toml
--rw-r--r--   0      501       20    11043 2023-07-23 00:01:50.000000 pyft-0.1.6/local_dependencies/bamlift/src/lib.rs
--rw-r--r--   0      501       20     1043 2023-07-22 20:22:41.000000 pyft-0.1.6/local_dependencies/bamlift/tests/test-liftover.rs
--rw-r--r--   0        0        0      636 1970-01-01 00:00:00.000000 pyft-0.1.6/local_dependencies/bio-io/Cargo.toml
--rw-r--r--   0      501       20    10927 2023-07-21 23:45:13.000000 pyft-0.1.6/local_dependencies/bio-io/src/lib.rs
--rw-r--r--   0        0        0     1733 1970-01-01 00:00:00.000000 pyft-0.1.6/local_dependencies/fibertools-rs/Cargo.toml
--rw-r--r--   0      501       20      231 2022-10-14 01:13:49.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.cargo/config
--rw-r--r--   0      501       20      210 2023-06-29 17:34:56.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.dockerignore
--rw-r--r--   0      501       20      467 2022-08-31 04:23:38.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0      501       20     1366 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.github/workflows/CI.yml
--rw-r--r--   0      501       20     5839 2023-02-01 23:24:35.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.github/workflows/release.yml
--rw-r--r--   0      501       20      211 2023-07-22 20:39:35.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.gitignore
--rw-r--r--   0      501       20      475 2023-07-19 02:39:46.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.pre-commit-config.yaml
--rw-r--r--   0      501       20      383 2023-07-20 16:48:33.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.readthedocs.yaml
--rw-------   0      501       20   122462 2023-07-21 08:31:15.000000 pyft-0.1.6/local_dependencies/fibertools-rs/CHANGELOG.md
--rw-r--r--   0      501       20    63353 2023-07-22 22:51:02.000000 pyft-0.1.6/local_dependencies/fibertools-rs/Cargo.lock
--rw-r--r--   0      501       20     1216 2023-07-03 16:43:59.000000 pyft-0.1.6/local_dependencies/fibertools-rs/Dockerfile
--rw-r--r--   0      501       20     1486 2023-06-14 05:56:02.000000 pyft-0.1.6/local_dependencies/fibertools-rs/INSTALL.md
--rw-r--r--   0      501       20      146 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/NOTES.md
--rw-r--r--   0      501       20     4471 2023-07-21 07:53:23.000000 pyft-0.1.6/local_dependencies/fibertools-rs/README.md
--rw-r--r--   0      501       20      297 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/_config.yml
--rw-r--r--   0      501       20   670134 2022-12-09 17:50:21.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/center.png
--rw-r--r--   0      501       20   160734 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png
--rw-r--r--   0      501       20   159267 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png
--rw-r--r--   0      501       20   220557 2022-12-09 17:50:21.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png
--rw-r--r--   0      501       20   303252 2022-12-09 17:50:21.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/logo.png
--rw-r--r--   0      501       20      761 2023-05-08 02:36:47.000000 pyft-0.1.6/local_dependencies/fibertools-rs/build.rs
--rw-r--r--   0      501       20     1181 2023-07-19 02:49:54.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft--help.md
--rw-r--r--   0      501       20     1035 2023-07-19 02:50:05.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md
--rw-r--r--   0      501       20      323 2023-07-19 02:50:14.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-all-columns.md
--rw-r--r--   0      501       20     1697 2023-07-19 02:50:00.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-center-help.md
--rw-r--r--   0      501       20      488 2023-07-19 02:50:08.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-clear-kinetics-help.md
--rw-r--r--   0      501       20     1436 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-extract-help.md
--rw-r--r--   0      501       20     2234 2023-07-19 02:50:03.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md
--rw-r--r--   0      501       20      627 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md
--rwxr-xr-x   0      501       20      675 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/make_help_docs.sh
--rw-r--r--   0      501       20      294 2023-06-18 22:24:56.000000 pyft-0.1.6/local_dependencies/fibertools-rs/env.yaml
--rw-r--r--   0      501       20     5008 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_semi_torch.json
--rw-r--r--   0      501       20    26890 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt
--rw-r--r--   0      501       20    26136 2022-10-20 20:35:37.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_torch.pt
--rw-r--r--   0      501       20     8502 2023-02-27 20:16:15.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_semi_torch.json
--rw-r--r--   0      501       20    27030 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt
--rw-r--r--   0      501       20    26136 2022-12-20 16:24:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_torch.pt
--rw-r--r--   0      501       20    15472 2023-04-25 19:19:04.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/3.2_semi_torch.json
--rw-r--r--   0      501       20    26130 2023-03-14 17:30:11.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt
--rw-r--r--   0      501       20     4491 2023-05-02 16:35:59.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/Revio_semi_torch.json
--rw-r--r--   0      501       20    32320 2023-05-02 16:35:43.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt
--rw-r--r--   0      501       20  2589234 2022-11-17 21:59:57.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json
--rw-r--r--   0      501       20  2579653 2022-11-17 21:59:57.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json
--rw-r--r--   0      501       20    18323 2023-07-22 22:54:01.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/basemods/mod.rs
--rw-r--r--   0      501       20    12588 2023-07-22 20:33:30.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/center.rs
--rw-r--r--   0      501       20    10971 2023-07-22 19:51:25.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/cli.rs
--rw-r--r--   0      501       20    18362 2023-07-22 20:40:22.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/extract.rs
--rw-r--r--   0      501       20     4129 2023-07-22 01:59:45.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/lib.rs
--rw-r--r--   0      501       20     9233 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/main.rs
--rw-r--r--   0      501       20    12907 2023-07-21 05:47:41.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/nucleosomes.rs
--rw-r--r--   0      501       20     3476 2023-06-18 04:21:08.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs
--rw-r--r--   0      501       20    18361 2023-07-21 00:03:41.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs
--rw-r--r--   0      501       20     1684 2023-03-10 15:54:29.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs
--rw-r--r--   0      501       20     1588 2023-06-29 17:25:52.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/strip_basemods.rs
--rw-r--r--   0      501       20  1529300 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/all.bam
--rw-r--r--   0      501       20     1792 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/all.bam.bai
--rw-r--r--   0      501       20  4202969 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bam
--rw-r--r--   0      501       20   758264 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bam.bai
--rw-r--r--   0      501       20     3349 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bed
--rw-r--r--   0      501       20    17525 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam
--rw-r--r--   0      501       20       13 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/test.txt
--rw-r--r--   0      501       20       72 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/test.txt.gz
--rw-r--r--   0      501       20     1780 2023-07-21 22:42:46.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/extract_test.rs
--rw-r--r--   0      501       20     2216 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/run_test.rs
--rw-r--r--   0        0        0      565 1970-01-01 00:00:00.000000 pyft-0.1.6/Cargo.toml
--rw-r--r--   0      501       20     2807 2023-07-19 21:04:05.000000 pyft-0.1.6/.github/workflows/CI.yml
--rw-r--r--   0      501       20      692 2023-07-19 21:52:50.000000 pyft-0.1.6/.gitignore
--rw-r--r--   0      501       20      382 2023-07-23 16:19:13.000000 pyft-0.1.6/README.md
--rw-r--r--   0      501       20      634 2023-07-20 03:00:42.000000 pyft-0.1.6/docs/Makefile
--rw-r--r--   0      501       20     2216 2023-07-20 18:11:44.000000 pyft-0.1.6/docs/_static/css/rtd_dark.css
--rw-r--r--   0      501       20   160734 2023-07-20 16:45:23.000000 pyft-0.1.6/docs/_static/img/fiber_tools_grey.png
--rw-r--r--   0      501       20      294 2023-07-20 17:07:50.000000 pyft-0.1.6/docs/_templates/layout.html
--rw-r--r--   0      501       20     1695 2023-07-23 14:42:32.000000 pyft-0.1.6/docs/conf.py
--rw-r--r--   0      501       20       76 2023-07-20 18:49:05.000000 pyft-0.1.6/docs/environment.yml
--rw-r--r--   0      501       20     1277 2023-07-23 16:17:21.000000 pyft-0.1.6/docs/index.rst
--rw-r--r--   0      501       20      800 2023-07-20 03:00:42.000000 pyft-0.1.6/docs/make.bat
--rw-r--r--   0      501       20       46 2023-07-20 17:01:46.000000 pyft-0.1.6/docs/modules.rst
--rw-r--r--   0      501       20      141 2023-07-20 17:44:28.000000 pyft-0.1.6/docs/pyft.rst
--rw-r--r--   0      501       20      113 2023-07-23 14:43:25.000000 pyft-0.1.6/docs/requirements.txt
--rw-r--r--   0      501       20      651 2023-07-23 16:09:17.000000 pyft-0.1.6/example.py
--rw-r--r--   0      501       20      357 2023-07-20 17:34:33.000000 pyft-0.1.6/pyproject.toml
--rw-r--r--   0      501       20    10384 2023-07-23 15:56:41.000000 pyft-0.1.6/src/fiberdata.rs
--rw-r--r--   0      501       20      698 2023-07-23 15:42:43.000000 pyft-0.1.6/src/lib.rs
--rw-r--r--   0      501       20    49806 2023-07-23 16:18:07.000000 pyft-0.1.6/Cargo.lock
--rw-r--r--   0        0        0      705 1970-01-01 00:00:00.000000 pyft-0.1.6/PKG-INFO
+-rw-r--r--   0        0        0      462 1970-01-01 00:00:00.000000 pyft-0.1.7/local_dependencies/bamlift/Cargo.toml
+-rw-r--r--   0      501       20    11043 2023-07-23 00:01:50.000000 pyft-0.1.7/local_dependencies/bamlift/src/lib.rs
+-rw-r--r--   0      501       20     1043 2023-07-22 20:22:41.000000 pyft-0.1.7/local_dependencies/bamlift/tests/test-liftover.rs
+-rw-r--r--   0        0        0      636 1970-01-01 00:00:00.000000 pyft-0.1.7/local_dependencies/bio-io/Cargo.toml
+-rw-r--r--   0      501       20    10927 2023-07-21 23:45:13.000000 pyft-0.1.7/local_dependencies/bio-io/src/lib.rs
+-rw-r--r--   0        0        0     1733 1970-01-01 00:00:00.000000 pyft-0.1.7/local_dependencies/fibertools-rs/Cargo.toml
+-rw-r--r--   0      501       20      231 2022-10-14 01:13:49.000000 pyft-0.1.7/local_dependencies/fibertools-rs/.cargo/config
+-rw-r--r--   0      501       20      210 2023-06-29 17:34:56.000000 pyft-0.1.7/local_dependencies/fibertools-rs/.dockerignore
+-rw-r--r--   0      501       20      467 2022-08-31 04:23:38.000000 pyft-0.1.7/local_dependencies/fibertools-rs/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0      501       20     1366 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/.github/workflows/CI.yml
+-rw-r--r--   0      501       20     5839 2023-02-01 23:24:35.000000 pyft-0.1.7/local_dependencies/fibertools-rs/.github/workflows/release.yml
+-rw-r--r--   0      501       20      211 2023-07-22 20:39:35.000000 pyft-0.1.7/local_dependencies/fibertools-rs/.gitignore
+-rw-r--r--   0      501       20      475 2023-07-19 02:39:46.000000 pyft-0.1.7/local_dependencies/fibertools-rs/.pre-commit-config.yaml
+-rw-r--r--   0      501       20      383 2023-07-20 16:48:33.000000 pyft-0.1.7/local_dependencies/fibertools-rs/.readthedocs.yaml
+-rw-------   0      501       20   122462 2023-07-21 08:31:15.000000 pyft-0.1.7/local_dependencies/fibertools-rs/CHANGELOG.md
+-rw-r--r--   0      501       20    63353 2023-07-22 22:51:02.000000 pyft-0.1.7/local_dependencies/fibertools-rs/Cargo.lock
+-rw-r--r--   0      501       20     1216 2023-07-03 16:43:59.000000 pyft-0.1.7/local_dependencies/fibertools-rs/Dockerfile
+-rw-r--r--   0      501       20     1486 2023-06-14 05:56:02.000000 pyft-0.1.7/local_dependencies/fibertools-rs/INSTALL.md
+-rw-r--r--   0      501       20      146 2023-01-13 07:54:36.000000 pyft-0.1.7/local_dependencies/fibertools-rs/NOTES.md
+-rw-r--r--   0      501       20     4471 2023-07-21 07:53:23.000000 pyft-0.1.7/local_dependencies/fibertools-rs/README.md
+-rw-r--r--   0      501       20      297 2023-01-13 07:54:36.000000 pyft-0.1.7/local_dependencies/fibertools-rs/_config.yml
+-rw-r--r--   0      501       20   670134 2022-12-09 17:50:21.000000 pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/center.png
+-rw-r--r--   0      501       20   160734 2023-01-13 07:54:36.000000 pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png
+-rw-r--r--   0      501       20   159267 2023-01-13 07:54:36.000000 pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png
+-rw-r--r--   0      501       20   220557 2022-12-09 17:50:21.000000 pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png
+-rw-r--r--   0      501       20   303252 2022-12-09 17:50:21.000000 pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/logo.png
+-rw-r--r--   0      501       20      761 2023-05-08 02:36:47.000000 pyft-0.1.7/local_dependencies/fibertools-rs/build.rs
+-rw-r--r--   0      501       20     1181 2023-07-19 02:49:54.000000 pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft--help.md
+-rw-r--r--   0      501       20     1035 2023-07-19 02:50:05.000000 pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md
+-rw-r--r--   0      501       20      323 2023-07-19 02:50:14.000000 pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-all-columns.md
+-rw-r--r--   0      501       20     1697 2023-07-19 02:50:00.000000 pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-center-help.md
+-rw-r--r--   0      501       20      488 2023-07-19 02:50:08.000000 pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-clear-kinetics-help.md
+-rw-r--r--   0      501       20     1436 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-extract-help.md
+-rw-r--r--   0      501       20     2234 2023-07-19 02:50:03.000000 pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md
+-rw-r--r--   0      501       20      627 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md
+-rwxr-xr-x   0      501       20      675 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/docs/make_help_docs.sh
+-rw-r--r--   0      501       20      294 2023-06-18 22:24:56.000000 pyft-0.1.7/local_dependencies/fibertools-rs/env.yaml
+-rw-r--r--   0      501       20     5008 2023-01-13 07:54:36.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/2.0_semi_torch.json
+-rw-r--r--   0      501       20    26890 2023-01-13 07:54:36.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt
+-rw-r--r--   0      501       20    26136 2022-10-20 20:35:37.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/2.0_torch.pt
+-rw-r--r--   0      501       20     8502 2023-02-27 20:16:15.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/2.2_semi_torch.json
+-rw-r--r--   0      501       20    27030 2023-01-13 07:54:36.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt
+-rw-r--r--   0      501       20    26136 2022-12-20 16:24:36.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/2.2_torch.pt
+-rw-r--r--   0      501       20    15472 2023-04-25 19:19:04.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/3.2_semi_torch.json
+-rw-r--r--   0      501       20    26130 2023-03-14 17:30:11.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt
+-rw-r--r--   0      501       20     4491 2023-05-02 16:35:59.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/Revio_semi_torch.json
+-rw-r--r--   0      501       20    32320 2023-05-02 16:35:43.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt
+-rw-r--r--   0      501       20  2589234 2022-11-17 21:59:57.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json
+-rw-r--r--   0      501       20  2579653 2022-11-17 21:59:57.000000 pyft-0.1.7/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json
+-rw-r--r--   0      501       20    18323 2023-07-22 22:54:01.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/basemods/mod.rs
+-rw-r--r--   0      501       20    12588 2023-07-22 20:33:30.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/center.rs
+-rw-r--r--   0      501       20    10971 2023-07-22 19:51:25.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/cli.rs
+-rw-r--r--   0      501       20    18362 2023-07-22 20:40:22.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/extract.rs
+-rw-r--r--   0      501       20     4129 2023-07-22 01:59:45.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/lib.rs
+-rw-r--r--   0      501       20     9233 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/main.rs
+-rw-r--r--   0      501       20    12907 2023-07-21 05:47:41.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/nucleosomes.rs
+-rw-r--r--   0      501       20     3476 2023-06-18 04:21:08.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs
+-rw-r--r--   0      501       20    18361 2023-07-21 00:03:41.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs
+-rw-r--r--   0      501       20     1684 2023-03-10 15:54:29.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs
+-rw-r--r--   0      501       20     1588 2023-06-29 17:25:52.000000 pyft-0.1.7/local_dependencies/fibertools-rs/src/strip_basemods.rs
+-rw-r--r--   0      501       20  1529300 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/all.bam
+-rw-r--r--   0      501       20     1792 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/all.bam.bai
+-rw-r--r--   0      501       20  4202969 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/center.bam
+-rw-r--r--   0      501       20   758264 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/center.bam.bai
+-rw-r--r--   0      501       20     3349 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/center.bed
+-rw-r--r--   0      501       20    17525 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam
+-rw-r--r--   0      501       20       13 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/test.txt
+-rw-r--r--   0      501       20       72 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/test.txt.gz
+-rw-r--r--   0      501       20     1780 2023-07-21 22:42:46.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/extract_test.rs
+-rw-r--r--   0      501       20     2216 2023-07-19 18:23:20.000000 pyft-0.1.7/local_dependencies/fibertools-rs/tests/run_test.rs
+-rw-r--r--   0        0        0      565 1970-01-01 00:00:00.000000 pyft-0.1.7/Cargo.toml
+-rw-r--r--   0      501       20     2807 2023-07-19 21:04:05.000000 pyft-0.1.7/.github/workflows/CI.yml
+-rw-r--r--   0      501       20      692 2023-07-19 21:52:50.000000 pyft-0.1.7/.gitignore
+-rw-r--r--   0      501       20      382 2023-07-23 16:19:13.000000 pyft-0.1.7/README.md
+-rw-r--r--   0      501       20      634 2023-07-20 03:00:42.000000 pyft-0.1.7/docs/Makefile
+-rw-r--r--   0      501       20     2216 2023-07-20 18:11:44.000000 pyft-0.1.7/docs/_static/css/rtd_dark.css
+-rw-r--r--   0      501       20   160734 2023-07-20 16:45:23.000000 pyft-0.1.7/docs/_static/img/fiber_tools_grey.png
+-rw-r--r--   0      501       20      294 2023-07-20 17:07:50.000000 pyft-0.1.7/docs/_templates/layout.html
+-rw-r--r--   0      501       20     1695 2023-07-23 14:42:32.000000 pyft-0.1.7/docs/conf.py
+-rw-r--r--   0      501       20       76 2023-07-20 18:49:05.000000 pyft-0.1.7/docs/environment.yml
+-rw-r--r--   0      501       20     1277 2023-07-23 16:17:21.000000 pyft-0.1.7/docs/index.rst
+-rw-r--r--   0      501       20      800 2023-07-20 03:00:42.000000 pyft-0.1.7/docs/make.bat
+-rw-r--r--   0      501       20       46 2023-07-20 17:01:46.000000 pyft-0.1.7/docs/modules.rst
+-rw-r--r--   0      501       20      141 2023-07-20 17:44:28.000000 pyft-0.1.7/docs/pyft.rst
+-rw-r--r--   0      501       20      113 2023-07-23 14:43:25.000000 pyft-0.1.7/docs/requirements.txt
+-rw-r--r--   0      501       20      651 2023-07-23 17:34:01.000000 pyft-0.1.7/example.py
+-rw-r--r--   0      501       20      357 2023-07-20 17:34:33.000000 pyft-0.1.7/pyproject.toml
+-rw-r--r--   0      501       20    10263 2023-07-23 17:46:37.000000 pyft-0.1.7/src/fiberdata.rs
+-rw-r--r--   0      501       20      700 2023-07-23 17:48:37.000000 pyft-0.1.7/src/lib.rs
+-rw-r--r--   0      501       20    49806 2023-07-23 17:46:30.000000 pyft-0.1.7/Cargo.lock
+-rw-r--r--   0        0        0      705 1970-01-01 00:00:00.000000 pyft-0.1.7/PKG-INFO
```

### Comparing `pyft-0.1.6/local_dependencies/bamlift/src/lib.rs` & `pyft-0.1.7/local_dependencies/bamlift/src/lib.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/bamlift/tests/test-liftover.rs` & `pyft-0.1.7/local_dependencies/bamlift/tests/test-liftover.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/bio-io/Cargo.toml` & `pyft-0.1.7/local_dependencies/bio-io/Cargo.toml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/bio-io/src/lib.rs` & `pyft-0.1.7/local_dependencies/bio-io/src/lib.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/Cargo.toml` & `pyft-0.1.7/local_dependencies/fibertools-rs/Cargo.toml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/.github/workflows/CI.yml` & `pyft-0.1.7/local_dependencies/fibertools-rs/.github/workflows/CI.yml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/.github/workflows/release.yml` & `pyft-0.1.7/local_dependencies/fibertools-rs/.github/workflows/release.yml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/CHANGELOG.md` & `pyft-0.1.7/local_dependencies/fibertools-rs/CHANGELOG.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/Cargo.lock` & `pyft-0.1.7/local_dependencies/fibertools-rs/Cargo.lock`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/Dockerfile` & `pyft-0.1.7/local_dependencies/fibertools-rs/Dockerfile`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/INSTALL.md` & `pyft-0.1.7/local_dependencies/fibertools-rs/INSTALL.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/README.md` & `pyft-0.1.7/local_dependencies/fibertools-rs/README.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/center.png` & `pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/center.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png` & `pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png` & `pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png` & `pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/logo.png` & `pyft-0.1.7/local_dependencies/fibertools-rs/assets/img/logo.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/build.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/build.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft--help.md` & `pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft--help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md` & `pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-center-help.md` & `pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-center-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-extract-help.md` & `pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-extract-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md` & `pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md` & `pyft-0.1.7/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/docs/make_help_docs.sh` & `pyft-0.1.7/local_dependencies/fibertools-rs/docs/make_help_docs.sh`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_semi_torch.json` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/2.0_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_torch.pt` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/2.0_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_semi_torch.json` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/2.2_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_torch.pt` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/2.2_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/3.2_semi_torch.json` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/3.2_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/Revio_semi_torch.json` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/Revio_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json` & `pyft-0.1.7/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/basemods/mod.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/basemods/mod.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/center.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/center.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/cli.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/cli.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/extract.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/extract.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/lib.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/lib.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/main.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/main.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/nucleosomes.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/nucleosomes.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/src/strip_basemods.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/src/strip_basemods.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/all.bam` & `pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/all.bam`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/all.bam.bai` & `pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/all.bam.bai`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bam` & `pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/center.bam`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bam.bai` & `pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/center.bam.bai`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bed` & `pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/center.bed`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam` & `pyft-0.1.7/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/tests/extract_test.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/tests/extract_test.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/local_dependencies/fibertools-rs/tests/run_test.rs` & `pyft-0.1.7/local_dependencies/fibertools-rs/tests/run_test.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/.github/workflows/CI.yml` & `pyft-0.1.7/.github/workflows/CI.yml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/.gitignore` & `pyft-0.1.7/.gitignore`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/docs/Makefile` & `pyft-0.1.7/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/docs/_static/css/rtd_dark.css` & `pyft-0.1.7/docs/_static/css/rtd_dark.css`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/docs/_static/img/fiber_tools_grey.png` & `pyft-0.1.7/docs/_static/img/fiber_tools_grey.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/docs/conf.py` & `pyft-0.1.7/docs/conf.py`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/docs/index.rst` & `pyft-0.1.7/docs/index.rst`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/docs/make.bat` & `pyft-0.1.7/docs/make.bat`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/example.py` & `pyft-0.1.7/example.py`

 * *Files identical despite different names*

### Comparing `pyft-0.1.6/src/fiberdata.rs` & `pyft-0.1.7/src/fiberdata.rs`

 * *Files 6% similar despite different names*

```diff
@@ -135,27 +135,15 @@
     };
 
     // fiberseq features
     let m6a = fiber.base_mods.m6a();
     let m6a = Basemods::new(m6a.0, m6a.1, m6a.2);
     let cpg = fiber.base_mods.cpg();
     let cpg = Basemods::new(cpg.0, cpg.1, cpg.2);
-    let msp_starts = fiber.get_msp(false, true);
-    let msp_lengths = fiber.get_msp(false, false);
-    let ref_msp_starts = fiber.get_msp(true, true);
-    let ref_msp_lengths = fiber.get_msp(true, false);
-    let msp = Ranges::new(msp_starts, msp_lengths, ref_msp_starts, ref_msp_lengths);
-
-    let nuc_starts = fiber.get_nuc(false, true);
-    let nuc_lengths = fiber.get_nuc(false, false);
-    let ref_nuc_starts = fiber.get_nuc(true, true);
-    let ref_nuc_lengths = fiber.get_nuc(true, false);
-    let nuc = Ranges::new(nuc_starts, nuc_lengths, ref_nuc_starts, ref_nuc_lengths);
 
-    /*
     let nuc = Ranges {
         starts: fiber.nuc.starts,
         ends: fiber.nuc.ends,
         lengths: fiber.nuc.lengths,
         reference_starts: fiber.nuc.reference_starts,
         reference_ends: fiber.nuc.reference_ends,
         reference_lengths: fiber.nuc.reference_lengths,
@@ -164,15 +152,15 @@
         starts: fiber.msp.starts,
         ends: fiber.msp.ends,
         lengths: fiber.msp.lengths,
         reference_starts: fiber.msp.reference_starts,
         reference_ends: fiber.msp.reference_ends,
         reference_lengths: fiber.msp.reference_lengths,
     };
-    */
+
     let aligned_block_pairs = fiber.record.aligned_block_pairs().collect();
     Fiberdata {
         ec,
         qname: qname.to_string(),
         sam_flag,
         rq,
         hp,
@@ -187,58 +175,70 @@
         msp,
         nuc,
         aligned_block_pairs,
     }
 }
 
 #[pyclass]
-/// Create a fibertools iterator from an indexed bam file.
-/// Must provide a valid chrom, start, and end.
-/// Returns an iterator over :class:`~pyft.Fiberdata` objects.
+/// Open a fiberseq bam file. Must have an index.
 pub struct Fiberbam {
     bam: bam::IndexedReader,
     header: bam::Header,
     start: time::Instant,
 }
 
 #[pymethods]
-/// Open a fiberseq bam file. Must have an index.
 impl Fiberbam {
     #[new]
-    pub fn new(f: &str) -> Self {
-        let mut bam = bam::IndexedReader::from_path(f).expect("unable to open indexed bam file");
-        bam.set_threads(8).unwrap();
+    #[pyo3(signature = (bam_file, threads = 8))]
+    fn new(bam_file: &str, threads: usize) -> Self {
+        let mut bam =
+            bam::IndexedReader::from_path(bam_file).expect("unable to open indexed bam file");
+        bam.set_threads(threads).unwrap();
         let header = bam::Header::from_template(bam.header());
         let start = time::Instant::now();
         Self { bam, header, start }
     }
 
     /// Returns an iterator over :class:`~pyft.Fiberdata` objects for the selected region.
-    pub fn fetch(&mut self, chrom: &str, start: i64, end: i64) -> Fiberiter {
+    /// Arguments for the region to fetch can be provided in multiple ways, e.g.:
+    ///
+    ///     fiberdata.fetch("chr1", 100, 200)
+    ///
+    ///     fiberdata.fetch("chr1", start=100, end=200)
+    ///
+    ///     fiberdata.fetch("chr1:100-200")
+    ///
+    ///     fiberdata.fetch("chr1")
+    #[pyo3(signature = (chrom, start = None, end=None))]
+    pub fn fetch(&mut self, chrom: &str, start: Option<i64>, end: Option<i64>) -> Fiberiter {
+        let fetch_args = if start.is_none() || end.is_none() {
+            bam::FetchDefinition::from(chrom)
+        } else {
+            bam::FetchDefinition::from((chrom, start.unwrap(), end.unwrap()))
+        };
         let head_view = bam::HeaderView::from_header(&self.header);
-        self.bam
-            .fetch((chrom, start, end))
-            .expect("unable to fetch region");
+        self.bam.fetch(fetch_args).expect("unable to fetch region");
         let records: Vec<bam::Record> = self.bam.records().map(|r| r.unwrap()).collect();
 
         log::info!(
             "{} records fetched in {:.2}s",
             records.len(),
-            self.time_from_last()
+            self._time_from_last()
         );
         let fiberdata = FiberseqData::from_records(records, &head_view, 0);
         log::info!(
             "Fiberdata made for {} records in {:.2}s",
             fiberdata.len(),
-            self.time_from_last()
+            self._time_from_last()
         );
         build_fiberdata_iter(fiberdata)
     }
 
-    fn time_from_last(&mut self) -> f64 {
+    fn _time_from_last(&mut self) -> f64 {
         let elapsed = self.start.elapsed().as_secs_f64();
         self.start = time::Instant::now();
         elapsed
     }
 }
 
 fn build_fiberdata_iter(fiberdata: Vec<FiberseqData>) -> Fiberiter {
```

### Comparing `pyft-0.1.6/src/lib.rs` & `pyft-0.1.7/src/lib.rs`

 * *Files 2% similar despite different names*

```diff
@@ -12,13 +12,13 @@
         .format_timestamp_secs()
         .target(Target::Stderr)
         .filter(None, LevelFilter::Info)
         .init();
 
     m.add("__version__", env!("CARGO_PKG_VERSION"))?;
     m.add_class::<fiberdata::Fiberbam>()?;
-    m.add_class::<fiberdata::Fiberiter>()?;
+    //m.add_class::<fiberdata::Fiberiter>()?;
     m.add_class::<fiberdata::Fiberdata>()?;
     m.add_class::<fiberdata::Basemods>()?;
     m.add_class::<fiberdata::Ranges>()?;
     Ok(())
 }
```

### Comparing `pyft-0.1.6/Cargo.lock` & `pyft-0.1.7/Cargo.lock`

 * *Files 0% similar despite different names*

```diff
@@ -1198,15 +1198,15 @@
 checksum = "18fb31db3f9bddb2ea821cde30a9f70117e3f119938b5ee630b7403aa6e2ead9"
 dependencies = [
  "unicode-ident",
 ]
 
 [[package]]
 name = "pyft"
-version = "0.1.6"
+version = "0.1.7"
 dependencies = [
  "anyhow",
  "bamlift",
  "bio-io",
  "colored",
  "env_logger 0.10.0",
  "fibertools-rs",
```

### Comparing `pyft-0.1.6/PKG-INFO` & `pyft-0.1.7/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyft
-Version: 0.1.6
+Version: 0.1.7
 Classifier: Programming Language :: Rust
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown; charset=UTF-8; variant=GFM
 
 # pyft: python bindings for fibertools-rs
```

