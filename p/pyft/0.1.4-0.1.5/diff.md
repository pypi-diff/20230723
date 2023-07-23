# Comparing `tmp/pyft-0.1.4.tar.gz` & `tmp/pyft-0.1.5.tar.gz`

## Comparing `pyft-0.1.4.tar` & `pyft-0.1.5.tar`

### file list

```diff
@@ -1,91 +1,91 @@
--rw-r--r--   0        0        0      462 1970-01-01 00:00:00.000000 pyft-0.1.4/local_dependencies/bamlift/Cargo.toml
--rw-r--r--   0      501       20    10705 2023-07-22 20:41:38.000000 pyft-0.1.4/local_dependencies/bamlift/src/lib.rs
--rw-r--r--   0      501       20     1043 2023-07-22 20:22:41.000000 pyft-0.1.4/local_dependencies/bamlift/tests/test-liftover.rs
--rw-r--r--   0        0        0      636 1970-01-01 00:00:00.000000 pyft-0.1.4/local_dependencies/bio-io/Cargo.toml
--rw-r--r--   0      501       20    10927 2023-07-21 23:45:13.000000 pyft-0.1.4/local_dependencies/bio-io/src/lib.rs
--rw-r--r--   0        0        0     1733 1970-01-01 00:00:00.000000 pyft-0.1.4/local_dependencies/fibertools-rs/Cargo.toml
--rw-r--r--   0      501       20      231 2022-10-14 01:13:49.000000 pyft-0.1.4/local_dependencies/fibertools-rs/.cargo/config
--rw-r--r--   0      501       20      210 2023-06-29 17:34:56.000000 pyft-0.1.4/local_dependencies/fibertools-rs/.dockerignore
--rw-r--r--   0      501       20      467 2022-08-31 04:23:38.000000 pyft-0.1.4/local_dependencies/fibertools-rs/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0      501       20     1366 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/.github/workflows/CI.yml
--rw-r--r--   0      501       20     5839 2023-02-01 23:24:35.000000 pyft-0.1.4/local_dependencies/fibertools-rs/.github/workflows/release.yml
--rw-r--r--   0      501       20      211 2023-07-22 20:39:35.000000 pyft-0.1.4/local_dependencies/fibertools-rs/.gitignore
--rw-r--r--   0      501       20      475 2023-07-19 02:39:46.000000 pyft-0.1.4/local_dependencies/fibertools-rs/.pre-commit-config.yaml
--rw-r--r--   0      501       20      383 2023-07-20 16:48:33.000000 pyft-0.1.4/local_dependencies/fibertools-rs/.readthedocs.yaml
--rw-------   0      501       20   122462 2023-07-21 08:31:15.000000 pyft-0.1.4/local_dependencies/fibertools-rs/CHANGELOG.md
--rw-r--r--   0      501       20    63059 2023-07-21 21:00:16.000000 pyft-0.1.4/local_dependencies/fibertools-rs/Cargo.lock
--rw-r--r--   0      501       20     1216 2023-07-03 16:43:59.000000 pyft-0.1.4/local_dependencies/fibertools-rs/Dockerfile
--rw-r--r--   0      501       20     1486 2023-06-14 05:56:02.000000 pyft-0.1.4/local_dependencies/fibertools-rs/INSTALL.md
--rw-r--r--   0      501       20      146 2023-01-13 07:54:36.000000 pyft-0.1.4/local_dependencies/fibertools-rs/NOTES.md
--rw-r--r--   0      501       20     4471 2023-07-21 07:53:23.000000 pyft-0.1.4/local_dependencies/fibertools-rs/README.md
--rw-r--r--   0      501       20      297 2023-01-13 07:54:36.000000 pyft-0.1.4/local_dependencies/fibertools-rs/_config.yml
--rw-r--r--   0      501       20   670134 2022-12-09 17:50:21.000000 pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/center.png
--rw-r--r--   0      501       20   160734 2023-01-13 07:54:36.000000 pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png
--rw-r--r--   0      501       20   159267 2023-01-13 07:54:36.000000 pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png
--rw-r--r--   0      501       20   220557 2022-12-09 17:50:21.000000 pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png
--rw-r--r--   0      501       20   303252 2022-12-09 17:50:21.000000 pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/logo.png
--rw-r--r--   0      501       20      761 2023-05-08 02:36:47.000000 pyft-0.1.4/local_dependencies/fibertools-rs/build.rs
--rw-r--r--   0      501       20     1181 2023-07-19 02:49:54.000000 pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft--help.md
--rw-r--r--   0      501       20     1035 2023-07-19 02:50:05.000000 pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md
--rw-r--r--   0      501       20      323 2023-07-19 02:50:14.000000 pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-all-columns.md
--rw-r--r--   0      501       20     1697 2023-07-19 02:50:00.000000 pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-center-help.md
--rw-r--r--   0      501       20      488 2023-07-19 02:50:08.000000 pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-clear-kinetics-help.md
--rw-r--r--   0      501       20     1436 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-extract-help.md
--rw-r--r--   0      501       20     2234 2023-07-19 02:50:03.000000 pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md
--rw-r--r--   0      501       20      627 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md
--rwxr-xr-x   0      501       20      675 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/docs/make_help_docs.sh
--rw-r--r--   0      501       20      294 2023-06-18 22:24:56.000000 pyft-0.1.4/local_dependencies/fibertools-rs/env.yaml
--rw-r--r--   0      501       20     5008 2023-01-13 07:54:36.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/2.0_semi_torch.json
--rw-r--r--   0      501       20    26890 2023-01-13 07:54:36.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt
--rw-r--r--   0      501       20    26136 2022-10-20 20:35:37.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/2.0_torch.pt
--rw-r--r--   0      501       20     8502 2023-02-27 20:16:15.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/2.2_semi_torch.json
--rw-r--r--   0      501       20    27030 2023-01-13 07:54:36.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt
--rw-r--r--   0      501       20    26136 2022-12-20 16:24:36.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/2.2_torch.pt
--rw-r--r--   0      501       20    15472 2023-04-25 19:19:04.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/3.2_semi_torch.json
--rw-r--r--   0      501       20    26130 2023-03-14 17:30:11.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt
--rw-r--r--   0      501       20     4491 2023-05-02 16:35:59.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/Revio_semi_torch.json
--rw-r--r--   0      501       20    32320 2023-05-02 16:35:43.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt
--rw-r--r--   0      501       20  2589234 2022-11-17 21:59:57.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json
--rw-r--r--   0      501       20  2579653 2022-11-17 21:59:57.000000 pyft-0.1.4/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json
--rw-r--r--   0      501       20    18323 2023-07-22 20:32:51.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/basemods/mod.rs
--rw-r--r--   0      501       20    12588 2023-07-22 20:33:30.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/center.rs
--rw-r--r--   0      501       20    10971 2023-07-22 19:51:25.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/cli.rs
--rw-r--r--   0      501       20    18362 2023-07-22 20:40:22.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/extract.rs
--rw-r--r--   0      501       20     4129 2023-07-22 01:59:45.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/lib.rs
--rw-r--r--   0      501       20     9233 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/main.rs
--rw-r--r--   0      501       20    12907 2023-07-21 05:47:41.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/nucleosomes.rs
--rw-r--r--   0      501       20     3476 2023-06-18 04:21:08.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs
--rw-r--r--   0      501       20    18361 2023-07-21 00:03:41.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs
--rw-r--r--   0      501       20     1684 2023-03-10 15:54:29.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs
--rw-r--r--   0      501       20     1588 2023-06-29 17:25:52.000000 pyft-0.1.4/local_dependencies/fibertools-rs/src/strip_basemods.rs
--rw-r--r--   0      501       20  1529300 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/all.bam
--rw-r--r--   0      501       20     1792 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/all.bam.bai
--rw-r--r--   0      501       20  4202969 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/center.bam
--rw-r--r--   0      501       20   758264 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/center.bam.bai
--rw-r--r--   0      501       20     3349 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/center.bed
--rw-r--r--   0      501       20    17525 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam
--rw-r--r--   0      501       20       13 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/test.txt
--rw-r--r--   0      501       20       72 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/test.txt.gz
--rw-r--r--   0      501       20     1780 2023-07-21 22:42:46.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/extract_test.rs
--rw-r--r--   0      501       20     2216 2023-07-19 18:23:20.000000 pyft-0.1.4/local_dependencies/fibertools-rs/tests/run_test.rs
--rw-r--r--   0        0        0      565 1970-01-01 00:00:00.000000 pyft-0.1.4/Cargo.toml
--rw-r--r--   0      501       20     2807 2023-07-19 21:04:05.000000 pyft-0.1.4/.github/workflows/CI.yml
--rw-r--r--   0      501       20      692 2023-07-19 21:52:50.000000 pyft-0.1.4/.gitignore
--rw-r--r--   0      501       20      924 2023-07-20 19:57:36.000000 pyft-0.1.4/README.md
--rw-r--r--   0      501       20      634 2023-07-20 03:00:42.000000 pyft-0.1.4/docs/Makefile
--rw-r--r--   0      501       20     2216 2023-07-20 18:11:44.000000 pyft-0.1.4/docs/_static/css/rtd_dark.css
--rw-r--r--   0      501       20   160734 2023-07-20 16:45:23.000000 pyft-0.1.4/docs/_static/img/fiber_tools_grey.png
--rw-r--r--   0      501       20      294 2023-07-20 17:07:50.000000 pyft-0.1.4/docs/_templates/layout.html
--rw-r--r--   0      501       20     1565 2023-07-20 19:08:31.000000 pyft-0.1.4/docs/conf.py
--rw-r--r--   0      501       20       76 2023-07-20 18:49:05.000000 pyft-0.1.4/docs/environment.yml
--rw-r--r--   0      501       20      596 2023-07-20 19:15:12.000000 pyft-0.1.4/docs/index.rst
--rw-r--r--   0      501       20      800 2023-07-20 03:00:42.000000 pyft-0.1.4/docs/make.bat
--rw-r--r--   0      501       20       46 2023-07-20 17:01:46.000000 pyft-0.1.4/docs/modules.rst
--rw-r--r--   0      501       20      141 2023-07-20 17:44:28.000000 pyft-0.1.4/docs/pyft.rst
--rw-r--r--   0      501       20        4 2023-07-20 16:47:52.000000 pyft-0.1.4/docs/requirements.txt
--rw-r--r--   0      501       20      407 2023-07-22 20:50:47.000000 pyft-0.1.4/example.py
--rw-r--r--   0      501       20      357 2023-07-20 17:34:33.000000 pyft-0.1.4/pyproject.toml
--rw-r--r--   0      501       20     9640 2023-07-22 20:54:03.000000 pyft-0.1.4/src/fiberdata.rs
--rw-r--r--   0      501       20      660 2023-07-20 23:34:28.000000 pyft-0.1.4/src/lib.rs
--rw-r--r--   0      501       20    49806 2023-07-22 20:53:46.000000 pyft-0.1.4/Cargo.lock
--rw-r--r--   0        0        0     1247 1970-01-01 00:00:00.000000 pyft-0.1.4/PKG-INFO
+-rw-r--r--   0        0        0      462 1970-01-01 00:00:00.000000 pyft-0.1.5/local_dependencies/bamlift/Cargo.toml
+-rw-r--r--   0      501       20    11043 2023-07-23 00:01:50.000000 pyft-0.1.5/local_dependencies/bamlift/src/lib.rs
+-rw-r--r--   0      501       20     1043 2023-07-22 20:22:41.000000 pyft-0.1.5/local_dependencies/bamlift/tests/test-liftover.rs
+-rw-r--r--   0        0        0      636 1970-01-01 00:00:00.000000 pyft-0.1.5/local_dependencies/bio-io/Cargo.toml
+-rw-r--r--   0      501       20    10927 2023-07-21 23:45:13.000000 pyft-0.1.5/local_dependencies/bio-io/src/lib.rs
+-rw-r--r--   0        0        0     1733 1970-01-01 00:00:00.000000 pyft-0.1.5/local_dependencies/fibertools-rs/Cargo.toml
+-rw-r--r--   0      501       20      231 2022-10-14 01:13:49.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.cargo/config
+-rw-r--r--   0      501       20      210 2023-06-29 17:34:56.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.dockerignore
+-rw-r--r--   0      501       20      467 2022-08-31 04:23:38.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0      501       20     1366 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.github/workflows/CI.yml
+-rw-r--r--   0      501       20     5839 2023-02-01 23:24:35.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.github/workflows/release.yml
+-rw-r--r--   0      501       20      211 2023-07-22 20:39:35.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.gitignore
+-rw-r--r--   0      501       20      475 2023-07-19 02:39:46.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.pre-commit-config.yaml
+-rw-r--r--   0      501       20      383 2023-07-20 16:48:33.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.readthedocs.yaml
+-rw-------   0      501       20   122462 2023-07-21 08:31:15.000000 pyft-0.1.5/local_dependencies/fibertools-rs/CHANGELOG.md
+-rw-r--r--   0      501       20    63353 2023-07-22 22:51:02.000000 pyft-0.1.5/local_dependencies/fibertools-rs/Cargo.lock
+-rw-r--r--   0      501       20     1216 2023-07-03 16:43:59.000000 pyft-0.1.5/local_dependencies/fibertools-rs/Dockerfile
+-rw-r--r--   0      501       20     1486 2023-06-14 05:56:02.000000 pyft-0.1.5/local_dependencies/fibertools-rs/INSTALL.md
+-rw-r--r--   0      501       20      146 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/NOTES.md
+-rw-r--r--   0      501       20     4471 2023-07-21 07:53:23.000000 pyft-0.1.5/local_dependencies/fibertools-rs/README.md
+-rw-r--r--   0      501       20      297 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/_config.yml
+-rw-r--r--   0      501       20   670134 2022-12-09 17:50:21.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/center.png
+-rw-r--r--   0      501       20   160734 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png
+-rw-r--r--   0      501       20   159267 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png
+-rw-r--r--   0      501       20   220557 2022-12-09 17:50:21.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png
+-rw-r--r--   0      501       20   303252 2022-12-09 17:50:21.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/logo.png
+-rw-r--r--   0      501       20      761 2023-05-08 02:36:47.000000 pyft-0.1.5/local_dependencies/fibertools-rs/build.rs
+-rw-r--r--   0      501       20     1181 2023-07-19 02:49:54.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft--help.md
+-rw-r--r--   0      501       20     1035 2023-07-19 02:50:05.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md
+-rw-r--r--   0      501       20      323 2023-07-19 02:50:14.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-all-columns.md
+-rw-r--r--   0      501       20     1697 2023-07-19 02:50:00.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-center-help.md
+-rw-r--r--   0      501       20      488 2023-07-19 02:50:08.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-clear-kinetics-help.md
+-rw-r--r--   0      501       20     1436 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-extract-help.md
+-rw-r--r--   0      501       20     2234 2023-07-19 02:50:03.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md
+-rw-r--r--   0      501       20      627 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md
+-rwxr-xr-x   0      501       20      675 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/make_help_docs.sh
+-rw-r--r--   0      501       20      294 2023-06-18 22:24:56.000000 pyft-0.1.5/local_dependencies/fibertools-rs/env.yaml
+-rw-r--r--   0      501       20     5008 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_semi_torch.json
+-rw-r--r--   0      501       20    26890 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt
+-rw-r--r--   0      501       20    26136 2022-10-20 20:35:37.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_torch.pt
+-rw-r--r--   0      501       20     8502 2023-02-27 20:16:15.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_semi_torch.json
+-rw-r--r--   0      501       20    27030 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt
+-rw-r--r--   0      501       20    26136 2022-12-20 16:24:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_torch.pt
+-rw-r--r--   0      501       20    15472 2023-04-25 19:19:04.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/3.2_semi_torch.json
+-rw-r--r--   0      501       20    26130 2023-03-14 17:30:11.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt
+-rw-r--r--   0      501       20     4491 2023-05-02 16:35:59.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/Revio_semi_torch.json
+-rw-r--r--   0      501       20    32320 2023-05-02 16:35:43.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt
+-rw-r--r--   0      501       20  2589234 2022-11-17 21:59:57.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json
+-rw-r--r--   0      501       20  2579653 2022-11-17 21:59:57.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json
+-rw-r--r--   0      501       20    18323 2023-07-22 22:54:01.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/basemods/mod.rs
+-rw-r--r--   0      501       20    12588 2023-07-22 20:33:30.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/center.rs
+-rw-r--r--   0      501       20    10971 2023-07-22 19:51:25.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/cli.rs
+-rw-r--r--   0      501       20    18362 2023-07-22 20:40:22.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/extract.rs
+-rw-r--r--   0      501       20     4129 2023-07-22 01:59:45.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/lib.rs
+-rw-r--r--   0      501       20     9233 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/main.rs
+-rw-r--r--   0      501       20    12907 2023-07-21 05:47:41.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/nucleosomes.rs
+-rw-r--r--   0      501       20     3476 2023-06-18 04:21:08.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs
+-rw-r--r--   0      501       20    18361 2023-07-21 00:03:41.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs
+-rw-r--r--   0      501       20     1684 2023-03-10 15:54:29.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs
+-rw-r--r--   0      501       20     1588 2023-06-29 17:25:52.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/strip_basemods.rs
+-rw-r--r--   0      501       20  1529300 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/all.bam
+-rw-r--r--   0      501       20     1792 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/all.bam.bai
+-rw-r--r--   0      501       20  4202969 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bam
+-rw-r--r--   0      501       20   758264 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bam.bai
+-rw-r--r--   0      501       20     3349 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bed
+-rw-r--r--   0      501       20    17525 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam
+-rw-r--r--   0      501       20       13 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/test.txt
+-rw-r--r--   0      501       20       72 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/test.txt.gz
+-rw-r--r--   0      501       20     1780 2023-07-21 22:42:46.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/extract_test.rs
+-rw-r--r--   0      501       20     2216 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/run_test.rs
+-rw-r--r--   0        0        0      565 1970-01-01 00:00:00.000000 pyft-0.1.5/Cargo.toml
+-rw-r--r--   0      501       20     2807 2023-07-19 21:04:05.000000 pyft-0.1.5/.github/workflows/CI.yml
+-rw-r--r--   0      501       20      692 2023-07-19 21:52:50.000000 pyft-0.1.5/.gitignore
+-rw-r--r--   0      501       20     1488 2023-07-22 21:17:17.000000 pyft-0.1.5/README.md
+-rw-r--r--   0      501       20      634 2023-07-20 03:00:42.000000 pyft-0.1.5/docs/Makefile
+-rw-r--r--   0      501       20     2216 2023-07-20 18:11:44.000000 pyft-0.1.5/docs/_static/css/rtd_dark.css
+-rw-r--r--   0      501       20   160734 2023-07-20 16:45:23.000000 pyft-0.1.5/docs/_static/img/fiber_tools_grey.png
+-rw-r--r--   0      501       20      294 2023-07-20 17:07:50.000000 pyft-0.1.5/docs/_templates/layout.html
+-rw-r--r--   0      501       20     1585 2023-07-22 21:50:16.000000 pyft-0.1.5/docs/conf.py
+-rw-r--r--   0      501       20       76 2023-07-20 18:49:05.000000 pyft-0.1.5/docs/environment.yml
+-rw-r--r--   0      501       20      598 2023-07-22 21:37:39.000000 pyft-0.1.5/docs/index.rst
+-rw-r--r--   0      501       20      800 2023-07-20 03:00:42.000000 pyft-0.1.5/docs/make.bat
+-rw-r--r--   0      501       20       46 2023-07-20 17:01:46.000000 pyft-0.1.5/docs/modules.rst
+-rw-r--r--   0      501       20      141 2023-07-20 17:44:28.000000 pyft-0.1.5/docs/pyft.rst
+-rw-r--r--   0      501       20       27 2023-07-22 21:30:24.000000 pyft-0.1.5/docs/requirements.txt
+-rw-r--r--   0      501       20      404 2023-07-23 00:02:25.000000 pyft-0.1.5/example.py
+-rw-r--r--   0      501       20      357 2023-07-20 17:34:33.000000 pyft-0.1.5/pyproject.toml
+-rw-r--r--   0      501       20     9640 2023-07-23 00:03:55.000000 pyft-0.1.5/src/fiberdata.rs
+-rw-r--r--   0      501       20      660 2023-07-20 23:34:28.000000 pyft-0.1.5/src/lib.rs
+-rw-r--r--   0      501       20    49806 2023-07-23 00:04:28.000000 pyft-0.1.5/Cargo.lock
+-rw-r--r--   0        0        0     1811 1970-01-01 00:00:00.000000 pyft-0.1.5/PKG-INFO
```

### Comparing `pyft-0.1.4/local_dependencies/bamlift/src/lib.rs` & `pyft-0.1.5/local_dependencies/bamlift/src/lib.rs`

 * *Files 8% similar despite different names*

```diff
@@ -160,23 +160,29 @@
     // skip empty
     if positions.is_empty() {
         return vec![];
     }
     if aligned_block_pairs.is_empty() {
         return positions.iter().map(|_x| -1).collect();
     }
-    assert!(is_sorted(positions));
+    assert!(
+        is_sorted(positions),
+        "Positions must be sorted before calling liftover!"
+    );
 
     // find the closest position for every position
     let mut starting_block = 0;
+    let ending_block = aligned_block_pairs.len();
     let mut pos_mapping = HashMap::new();
     for cur_pos in positions {
         pos_mapping.insert(cur_pos, (-1, i64::MAX));
         let mut current_block = 0;
-        for ([q_st, q_en], [r_st, r_en]) in &aligned_block_pairs[starting_block..] {
+        for block_index in starting_block..ending_block {
+            // get the current alignment block
+            let ([q_st, q_en], [r_st, r_en]) = &aligned_block_pairs[block_index];
             // get the previous closest position
             let (best_r_pos, best_diff) = pos_mapping.get_mut(cur_pos).unwrap();
             // exact match found
             if cur_pos >= &q_st && cur_pos < &q_en {
                 let dist_from_start = cur_pos - q_st;
                 *best_diff = 0;
                 *best_r_pos = r_st + dist_from_start;
@@ -276,14 +282,19 @@
 
 /// liftover positions using the cigar string
 pub fn liftover_exact(
     aligned_block_pairs: &Vec<([i64; 2], [i64; 2])>,
     positions: &[i64],
     lift_reference_to_query: bool,
 ) -> Vec<i64> {
+    assert!(
+        is_sorted(positions),
+        "Positions must be sorted before calling liftover!"
+    );
+
     // find the shared positions in the reference
     let mut return_positions = vec![];
     let mut cur_idx = 0;
     // ends are not inclusive, I checked.
     for ([q_st, q_en], [r_st, r_en]) in aligned_block_pairs {
         let (st, en) = if !lift_reference_to_query {
             (q_st, q_en)
```

### Comparing `pyft-0.1.4/local_dependencies/bamlift/tests/test-liftover.rs` & `pyft-0.1.5/local_dependencies/bamlift/tests/test-liftover.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/bio-io/Cargo.toml` & `pyft-0.1.5/local_dependencies/bio-io/Cargo.toml`

 * *Files 21% similar despite different names*

```diff
@@ -15,9 +15,9 @@
 gzp = "0.11.3"
 #indicatif = {version = "0.17.0", features = ["rayon"]}
 #env_logger = "0.9.0"
 itertools = "0.10.5"
 lazy_static = "1.4.0"
 log = "0.4"
 niffler = {version = "2.5.0", default-features = false, features = ["gz"]}
-regex = "1.5.4"
+regex = "1.9.1"
 rust-htslib = "0.44.1"
```

### Comparing `pyft-0.1.4/local_dependencies/bio-io/src/lib.rs` & `pyft-0.1.5/local_dependencies/bio-io/src/lib.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/Cargo.toml` & `pyft-0.1.5/local_dependencies/fibertools-rs/Cargo.toml`

 * *Files 4% similar despite different names*

```diff
@@ -31,15 +31,15 @@
 gbdt = {version = "0.1.1", optional = true}
 indicatif = {version = "0.17.0", features = ["rayon"]}
 itertools = "0.10.5"
 lazy_static = "1.4.0"
 log = "0.4"
 ordered-float = "3.4.0"
 rayon = "1.5"
-regex = "1.5.4"
+regex = "1.9.1"
 rust-htslib = "0.44.1"
 serde = {version = "1.0.104", features = ["derive"], optional = true}
 serde_json = {version = "1.0.48", optional = true}
 spin = "0.9.8"
 tch = {version = "0.13.0", optional = true}
 tempfile = "3.3.0"
```

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/.github/workflows/CI.yml` & `pyft-0.1.5/local_dependencies/fibertools-rs/.github/workflows/CI.yml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/.github/workflows/release.yml` & `pyft-0.1.5/local_dependencies/fibertools-rs/.github/workflows/release.yml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/CHANGELOG.md` & `pyft-0.1.5/local_dependencies/fibertools-rs/CHANGELOG.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/Cargo.lock` & `pyft-0.1.5/local_dependencies/fibertools-rs/Cargo.lock`

 * *Files 1% similar despite different names*

```diff
@@ -250,15 +250,15 @@
 name = "bstr"
 version = "1.5.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "a246e68bb43f6cd9db24bea052a53e40405417c5fb372e3d1a8a7f770a564ef5"
 dependencies = [
  "memchr",
  "once_cell",
- "regex-automata",
+ "regex-automata 0.1.10",
  "serde",
 ]
 
 [[package]]
 name = "bumpalo"
 version = "3.13.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
@@ -1753,34 +1753,46 @@
 checksum = "567664f262709473930a4bf9e51bf2ebf3348f2e748ccc50dea20646858f8f29"
 dependencies = [
  "bitflags",
 ]
 
 [[package]]
 name = "regex"
-version = "1.8.4"
+version = "1.9.1"
 source = "registry+https://github.com/rust-lang/crates.io-index"
-checksum = "d0ab3ca65655bb1e41f2a8c8cd662eb4fb035e67c3f78da1d61dffe89d07300f"
+checksum = "b2eae68fc220f7cf2532e4494aded17545fce192d59cd996e0fe7887f4ceb575"
 dependencies = [
  "aho-corasick",
  "memchr",
+ "regex-automata 0.3.3",
  "regex-syntax",
 ]
 
 [[package]]
 name = "regex-automata"
 version = "0.1.10"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "6c230d73fb8d8c1b9c0b3135c5142a8acee3a0558fb8db5cf1cb65f8d7862132"
 
 [[package]]
+name = "regex-automata"
+version = "0.3.3"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "39354c10dd07468c2e73926b23bb9c2caca74c5501e38a35da70406f1d923310"
+dependencies = [
+ "aho-corasick",
+ "memchr",
+ "regex-syntax",
+]
+
+[[package]]
 name = "regex-syntax"
-version = "0.7.2"
+version = "0.7.4"
 source = "registry+https://github.com/rust-lang/crates.io-index"
-checksum = "436b050e76ed2903236f032a59761c1eb99e1b0aead2c257922771dab1fc8c78"
+checksum = "e5ea92a5b6195c6ef2a0295ea818b312502c6fc94dde986c5553242e18fd4ce2"
 
 [[package]]
 name = "roff"
 version = "0.2.1"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "b833d8d034ea094b1ea68aa6d5c740e0d04bad9d16568d08ba6f76823a114316"
```

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/Dockerfile` & `pyft-0.1.5/local_dependencies/fibertools-rs/Dockerfile`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/INSTALL.md` & `pyft-0.1.5/local_dependencies/fibertools-rs/INSTALL.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/README.md` & `pyft-0.1.5/local_dependencies/fibertools-rs/README.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/center.png` & `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/center.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png` & `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png` & `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png` & `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/assets/img/logo.png` & `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/logo.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/build.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/build.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft--help.md` & `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft--help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md` & `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-center-help.md` & `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-center-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-extract-help.md` & `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-extract-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md` & `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md` & `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/docs/make_help_docs.sh` & `pyft-0.1.5/local_dependencies/fibertools-rs/docs/make_help_docs.sh`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/2.0_semi_torch.json` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/2.0_torch.pt` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/2.2_semi_torch.json` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/2.2_torch.pt` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/3.2_semi_torch.json` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/3.2_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/Revio_semi_torch.json` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/Revio_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json` & `pyft-0.1.5/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/basemods/mod.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/basemods/mod.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/center.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/center.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/cli.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/cli.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/extract.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/extract.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/lib.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/lib.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/main.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/main.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/nucleosomes.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/nucleosomes.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/src/strip_basemods.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/src/strip_basemods.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/all.bam` & `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/all.bam`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/all.bam.bai` & `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/all.bam.bai`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/center.bam` & `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bam`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/center.bam.bai` & `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bam.bai`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/center.bed` & `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bed`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam` & `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/tests/extract_test.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/tests/extract_test.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/local_dependencies/fibertools-rs/tests/run_test.rs` & `pyft-0.1.5/local_dependencies/fibertools-rs/tests/run_test.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/Cargo.toml` & `pyft-0.1.5/Cargo.toml`

 * *Files 26% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [package]
 edition = "2021"
 name = "pyft"
-version = "0.1.4"
+version = "0.1.5"
 
 # See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html
 [lib]
 crate-type = ["cdylib"]
 name = "pyft"
 
 [dependencies]
@@ -15,9 +15,9 @@
 colored = "2.0.0"
 env_logger = "0.10"
 fibertools-rs = {path = "local_dependencies/fibertools-rs", default-features = false}
 itertools = "0.10.5"
 lazy_static = "1.4.0"
 log = "0.4"
 pyo3 = "0.19.0"
-regex = "1.5.4"
+regex = "1.9.1"
 rust-htslib = "0.44.1"
```

### Comparing `pyft-0.1.4/.github/workflows/CI.yml` & `pyft-0.1.5/.github/workflows/CI.yml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/.gitignore` & `pyft-0.1.5/.gitignore`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/docs/Makefile` & `pyft-0.1.5/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/docs/_static/css/rtd_dark.css` & `pyft-0.1.5/docs/_static/css/rtd_dark.css`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/docs/_static/img/fiber_tools_grey.png` & `pyft-0.1.5/docs/_static/img/fiber_tools_grey.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/docs/conf.py` & `pyft-0.1.5/docs/conf.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,38 +1,39 @@
 # Configuration file for the Sphinx documentation builder.
 #
 # For the full list of built-in configuration values, see the documentation:
 # https://www.sphinx-doc.org/en/master/usage/configuration.html
 import os
+import sphinx
+import re
 import sys
-
+import sphinx.ext.autosummary as autosummary
 sys.path.insert(0, os.path.abspath("../"))
-
 import pyft
 
 # -- Project information -----------------------------------------------------
 # https://www.sphinx-doc.org/en/master/usage/configuration.html#project-information
 # The short X.Y version.
 project = "pyft"
 copyright = "2023, Mitchell R. Vollger"
 author = "Mitchell R. Vollger"
 version = pyft.__version__
-# The full version, including alpha/beta/rc tags.
 release = pyft.__version__
 
+
 # -- General configuration ---------------------------------------------------
 # https://www.sphinx-doc.org/en/master/usage/configuration.html#general-configuration
 
 extensions = [
     "sphinx.ext.autodoc",
     "sphinx.ext.viewcode",
-    "sphinx.ext.napoleon",
+    #"sphinx.ext.napoleon",
     "sphinx_rtd_theme",
     "sphinx.ext.intersphinx",
-    # "edit_on_github",
+    #"edit_on_github",
     "m2r2",
 ]
 
 # source_suffix = '.rst'
 source_suffix = [".rst", ".md"]
 
 templates_path = ["_templates"]
@@ -46,9 +47,11 @@
 html_theme = "sphinx_rtd_theme"
 html_static_path = ["_static"]
 html_css_files = [
     "css/rtd_dark.css",
 ]
 html_logo = "_static/img/fiber_tools_grey.png"
 
+
 # other options
 autodoc_member_order = 'bysource'
+
```

### Comparing `pyft-0.1.4/docs/index.rst` & `pyft-0.1.5/docs/index.rst`

 * *Files 19% similar despite different names*

```diff
@@ -20,13 +20,15 @@
 .. automodule:: pyft
    :members:
    :undoc-members:
    :show-inheritance:
    :member-order: bysource
 
 
+
+
 Indices and tables
 ==================
 
 * :ref:`genindex`
 * :ref:`modindex`
 * :ref:`search`
```

### Comparing `pyft-0.1.4/docs/make.bat` & `pyft-0.1.5/docs/make.bat`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/src/fiberdata.rs` & `pyft-0.1.5/src/fiberdata.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/src/lib.rs` & `pyft-0.1.5/src/lib.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.4/Cargo.lock` & `pyft-0.1.5/Cargo.lock`

 * *Files 0% similar despite different names*

```diff
@@ -1198,15 +1198,15 @@
 checksum = "18fb31db3f9bddb2ea821cde30a9f70117e3f119938b5ee630b7403aa6e2ead9"
 dependencies = [
  "unicode-ident",
 ]
 
 [[package]]
 name = "pyft"
-version = "0.1.4"
+version = "0.1.5"
 dependencies = [
  "anyhow",
  "bamlift",
  "bio-io",
  "colored",
  "env_logger 0.10.0",
  "fibertools-rs",
```

