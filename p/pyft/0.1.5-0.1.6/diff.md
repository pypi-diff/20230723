# Comparing `tmp/pyft-0.1.5.tar.gz` & `tmp/pyft-0.1.6.tar.gz`

## Comparing `pyft-0.1.5.tar` & `pyft-0.1.6.tar`

### file list

```diff
@@ -1,91 +1,91 @@
--rw-r--r--   0        0        0      462 1970-01-01 00:00:00.000000 pyft-0.1.5/local_dependencies/bamlift/Cargo.toml
--rw-r--r--   0      501       20    11043 2023-07-23 00:01:50.000000 pyft-0.1.5/local_dependencies/bamlift/src/lib.rs
--rw-r--r--   0      501       20     1043 2023-07-22 20:22:41.000000 pyft-0.1.5/local_dependencies/bamlift/tests/test-liftover.rs
--rw-r--r--   0        0        0      636 1970-01-01 00:00:00.000000 pyft-0.1.5/local_dependencies/bio-io/Cargo.toml
--rw-r--r--   0      501       20    10927 2023-07-21 23:45:13.000000 pyft-0.1.5/local_dependencies/bio-io/src/lib.rs
--rw-r--r--   0        0        0     1733 1970-01-01 00:00:00.000000 pyft-0.1.5/local_dependencies/fibertools-rs/Cargo.toml
--rw-r--r--   0      501       20      231 2022-10-14 01:13:49.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.cargo/config
--rw-r--r--   0      501       20      210 2023-06-29 17:34:56.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.dockerignore
--rw-r--r--   0      501       20      467 2022-08-31 04:23:38.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.github/ISSUE_TEMPLATE/bug_report.md
--rw-r--r--   0      501       20     1366 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.github/workflows/CI.yml
--rw-r--r--   0      501       20     5839 2023-02-01 23:24:35.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.github/workflows/release.yml
--rw-r--r--   0      501       20      211 2023-07-22 20:39:35.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.gitignore
--rw-r--r--   0      501       20      475 2023-07-19 02:39:46.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.pre-commit-config.yaml
--rw-r--r--   0      501       20      383 2023-07-20 16:48:33.000000 pyft-0.1.5/local_dependencies/fibertools-rs/.readthedocs.yaml
--rw-------   0      501       20   122462 2023-07-21 08:31:15.000000 pyft-0.1.5/local_dependencies/fibertools-rs/CHANGELOG.md
--rw-r--r--   0      501       20    63353 2023-07-22 22:51:02.000000 pyft-0.1.5/local_dependencies/fibertools-rs/Cargo.lock
--rw-r--r--   0      501       20     1216 2023-07-03 16:43:59.000000 pyft-0.1.5/local_dependencies/fibertools-rs/Dockerfile
--rw-r--r--   0      501       20     1486 2023-06-14 05:56:02.000000 pyft-0.1.5/local_dependencies/fibertools-rs/INSTALL.md
--rw-r--r--   0      501       20      146 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/NOTES.md
--rw-r--r--   0      501       20     4471 2023-07-21 07:53:23.000000 pyft-0.1.5/local_dependencies/fibertools-rs/README.md
--rw-r--r--   0      501       20      297 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/_config.yml
--rw-r--r--   0      501       20   670134 2022-12-09 17:50:21.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/center.png
--rw-r--r--   0      501       20   160734 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png
--rw-r--r--   0      501       20   159267 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png
--rw-r--r--   0      501       20   220557 2022-12-09 17:50:21.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png
--rw-r--r--   0      501       20   303252 2022-12-09 17:50:21.000000 pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/logo.png
--rw-r--r--   0      501       20      761 2023-05-08 02:36:47.000000 pyft-0.1.5/local_dependencies/fibertools-rs/build.rs
--rw-r--r--   0      501       20     1181 2023-07-19 02:49:54.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft--help.md
--rw-r--r--   0      501       20     1035 2023-07-19 02:50:05.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md
--rw-r--r--   0      501       20      323 2023-07-19 02:50:14.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-all-columns.md
--rw-r--r--   0      501       20     1697 2023-07-19 02:50:00.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-center-help.md
--rw-r--r--   0      501       20      488 2023-07-19 02:50:08.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-clear-kinetics-help.md
--rw-r--r--   0      501       20     1436 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-extract-help.md
--rw-r--r--   0      501       20     2234 2023-07-19 02:50:03.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md
--rw-r--r--   0      501       20      627 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md
--rwxr-xr-x   0      501       20      675 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/docs/make_help_docs.sh
--rw-r--r--   0      501       20      294 2023-06-18 22:24:56.000000 pyft-0.1.5/local_dependencies/fibertools-rs/env.yaml
--rw-r--r--   0      501       20     5008 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_semi_torch.json
--rw-r--r--   0      501       20    26890 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt
--rw-r--r--   0      501       20    26136 2022-10-20 20:35:37.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_torch.pt
--rw-r--r--   0      501       20     8502 2023-02-27 20:16:15.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_semi_torch.json
--rw-r--r--   0      501       20    27030 2023-01-13 07:54:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt
--rw-r--r--   0      501       20    26136 2022-12-20 16:24:36.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_torch.pt
--rw-r--r--   0      501       20    15472 2023-04-25 19:19:04.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/3.2_semi_torch.json
--rw-r--r--   0      501       20    26130 2023-03-14 17:30:11.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt
--rw-r--r--   0      501       20     4491 2023-05-02 16:35:59.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/Revio_semi_torch.json
--rw-r--r--   0      501       20    32320 2023-05-02 16:35:43.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt
--rw-r--r--   0      501       20  2589234 2022-11-17 21:59:57.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json
--rw-r--r--   0      501       20  2579653 2022-11-17 21:59:57.000000 pyft-0.1.5/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json
--rw-r--r--   0      501       20    18323 2023-07-22 22:54:01.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/basemods/mod.rs
--rw-r--r--   0      501       20    12588 2023-07-22 20:33:30.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/center.rs
--rw-r--r--   0      501       20    10971 2023-07-22 19:51:25.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/cli.rs
--rw-r--r--   0      501       20    18362 2023-07-22 20:40:22.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/extract.rs
--rw-r--r--   0      501       20     4129 2023-07-22 01:59:45.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/lib.rs
--rw-r--r--   0      501       20     9233 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/main.rs
--rw-r--r--   0      501       20    12907 2023-07-21 05:47:41.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/nucleosomes.rs
--rw-r--r--   0      501       20     3476 2023-06-18 04:21:08.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs
--rw-r--r--   0      501       20    18361 2023-07-21 00:03:41.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs
--rw-r--r--   0      501       20     1684 2023-03-10 15:54:29.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs
--rw-r--r--   0      501       20     1588 2023-06-29 17:25:52.000000 pyft-0.1.5/local_dependencies/fibertools-rs/src/strip_basemods.rs
--rw-r--r--   0      501       20  1529300 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/all.bam
--rw-r--r--   0      501       20     1792 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/all.bam.bai
--rw-r--r--   0      501       20  4202969 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bam
--rw-r--r--   0      501       20   758264 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bam.bai
--rw-r--r--   0      501       20     3349 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bed
--rw-r--r--   0      501       20    17525 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam
--rw-r--r--   0      501       20       13 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/test.txt
--rw-r--r--   0      501       20       72 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/test.txt.gz
--rw-r--r--   0      501       20     1780 2023-07-21 22:42:46.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/extract_test.rs
--rw-r--r--   0      501       20     2216 2023-07-19 18:23:20.000000 pyft-0.1.5/local_dependencies/fibertools-rs/tests/run_test.rs
--rw-r--r--   0        0        0      565 1970-01-01 00:00:00.000000 pyft-0.1.5/Cargo.toml
--rw-r--r--   0      501       20     2807 2023-07-19 21:04:05.000000 pyft-0.1.5/.github/workflows/CI.yml
--rw-r--r--   0      501       20      692 2023-07-19 21:52:50.000000 pyft-0.1.5/.gitignore
--rw-r--r--   0      501       20     1488 2023-07-22 21:17:17.000000 pyft-0.1.5/README.md
--rw-r--r--   0      501       20      634 2023-07-20 03:00:42.000000 pyft-0.1.5/docs/Makefile
--rw-r--r--   0      501       20     2216 2023-07-20 18:11:44.000000 pyft-0.1.5/docs/_static/css/rtd_dark.css
--rw-r--r--   0      501       20   160734 2023-07-20 16:45:23.000000 pyft-0.1.5/docs/_static/img/fiber_tools_grey.png
--rw-r--r--   0      501       20      294 2023-07-20 17:07:50.000000 pyft-0.1.5/docs/_templates/layout.html
--rw-r--r--   0      501       20     1585 2023-07-22 21:50:16.000000 pyft-0.1.5/docs/conf.py
--rw-r--r--   0      501       20       76 2023-07-20 18:49:05.000000 pyft-0.1.5/docs/environment.yml
--rw-r--r--   0      501       20      598 2023-07-22 21:37:39.000000 pyft-0.1.5/docs/index.rst
--rw-r--r--   0      501       20      800 2023-07-20 03:00:42.000000 pyft-0.1.5/docs/make.bat
--rw-r--r--   0      501       20       46 2023-07-20 17:01:46.000000 pyft-0.1.5/docs/modules.rst
--rw-r--r--   0      501       20      141 2023-07-20 17:44:28.000000 pyft-0.1.5/docs/pyft.rst
--rw-r--r--   0      501       20       27 2023-07-22 21:30:24.000000 pyft-0.1.5/docs/requirements.txt
--rw-r--r--   0      501       20      404 2023-07-23 00:02:25.000000 pyft-0.1.5/example.py
--rw-r--r--   0      501       20      357 2023-07-20 17:34:33.000000 pyft-0.1.5/pyproject.toml
--rw-r--r--   0      501       20     9640 2023-07-23 00:03:55.000000 pyft-0.1.5/src/fiberdata.rs
--rw-r--r--   0      501       20      660 2023-07-20 23:34:28.000000 pyft-0.1.5/src/lib.rs
--rw-r--r--   0      501       20    49806 2023-07-23 00:04:28.000000 pyft-0.1.5/Cargo.lock
--rw-r--r--   0        0        0     1811 1970-01-01 00:00:00.000000 pyft-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0      462 1970-01-01 00:00:00.000000 pyft-0.1.6/local_dependencies/bamlift/Cargo.toml
+-rw-r--r--   0      501       20    11043 2023-07-23 00:01:50.000000 pyft-0.1.6/local_dependencies/bamlift/src/lib.rs
+-rw-r--r--   0      501       20     1043 2023-07-22 20:22:41.000000 pyft-0.1.6/local_dependencies/bamlift/tests/test-liftover.rs
+-rw-r--r--   0        0        0      636 1970-01-01 00:00:00.000000 pyft-0.1.6/local_dependencies/bio-io/Cargo.toml
+-rw-r--r--   0      501       20    10927 2023-07-21 23:45:13.000000 pyft-0.1.6/local_dependencies/bio-io/src/lib.rs
+-rw-r--r--   0        0        0     1733 1970-01-01 00:00:00.000000 pyft-0.1.6/local_dependencies/fibertools-rs/Cargo.toml
+-rw-r--r--   0      501       20      231 2022-10-14 01:13:49.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.cargo/config
+-rw-r--r--   0      501       20      210 2023-06-29 17:34:56.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.dockerignore
+-rw-r--r--   0      501       20      467 2022-08-31 04:23:38.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0      501       20     1366 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.github/workflows/CI.yml
+-rw-r--r--   0      501       20     5839 2023-02-01 23:24:35.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.github/workflows/release.yml
+-rw-r--r--   0      501       20      211 2023-07-22 20:39:35.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.gitignore
+-rw-r--r--   0      501       20      475 2023-07-19 02:39:46.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.pre-commit-config.yaml
+-rw-r--r--   0      501       20      383 2023-07-20 16:48:33.000000 pyft-0.1.6/local_dependencies/fibertools-rs/.readthedocs.yaml
+-rw-------   0      501       20   122462 2023-07-21 08:31:15.000000 pyft-0.1.6/local_dependencies/fibertools-rs/CHANGELOG.md
+-rw-r--r--   0      501       20    63353 2023-07-22 22:51:02.000000 pyft-0.1.6/local_dependencies/fibertools-rs/Cargo.lock
+-rw-r--r--   0      501       20     1216 2023-07-03 16:43:59.000000 pyft-0.1.6/local_dependencies/fibertools-rs/Dockerfile
+-rw-r--r--   0      501       20     1486 2023-06-14 05:56:02.000000 pyft-0.1.6/local_dependencies/fibertools-rs/INSTALL.md
+-rw-r--r--   0      501       20      146 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/NOTES.md
+-rw-r--r--   0      501       20     4471 2023-07-21 07:53:23.000000 pyft-0.1.6/local_dependencies/fibertools-rs/README.md
+-rw-r--r--   0      501       20      297 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/_config.yml
+-rw-r--r--   0      501       20   670134 2022-12-09 17:50:21.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/center.png
+-rw-r--r--   0      501       20   160734 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png
+-rw-r--r--   0      501       20   159267 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png
+-rw-r--r--   0      501       20   220557 2022-12-09 17:50:21.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png
+-rw-r--r--   0      501       20   303252 2022-12-09 17:50:21.000000 pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/logo.png
+-rw-r--r--   0      501       20      761 2023-05-08 02:36:47.000000 pyft-0.1.6/local_dependencies/fibertools-rs/build.rs
+-rw-r--r--   0      501       20     1181 2023-07-19 02:49:54.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft--help.md
+-rw-r--r--   0      501       20     1035 2023-07-19 02:50:05.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md
+-rw-r--r--   0      501       20      323 2023-07-19 02:50:14.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-all-columns.md
+-rw-r--r--   0      501       20     1697 2023-07-19 02:50:00.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-center-help.md
+-rw-r--r--   0      501       20      488 2023-07-19 02:50:08.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-clear-kinetics-help.md
+-rw-r--r--   0      501       20     1436 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-extract-help.md
+-rw-r--r--   0      501       20     2234 2023-07-19 02:50:03.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md
+-rw-r--r--   0      501       20      627 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md
+-rwxr-xr-x   0      501       20      675 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/docs/make_help_docs.sh
+-rw-r--r--   0      501       20      294 2023-06-18 22:24:56.000000 pyft-0.1.6/local_dependencies/fibertools-rs/env.yaml
+-rw-r--r--   0      501       20     5008 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_semi_torch.json
+-rw-r--r--   0      501       20    26890 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt
+-rw-r--r--   0      501       20    26136 2022-10-20 20:35:37.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_torch.pt
+-rw-r--r--   0      501       20     8502 2023-02-27 20:16:15.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_semi_torch.json
+-rw-r--r--   0      501       20    27030 2023-01-13 07:54:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt
+-rw-r--r--   0      501       20    26136 2022-12-20 16:24:36.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_torch.pt
+-rw-r--r--   0      501       20    15472 2023-04-25 19:19:04.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/3.2_semi_torch.json
+-rw-r--r--   0      501       20    26130 2023-03-14 17:30:11.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt
+-rw-r--r--   0      501       20     4491 2023-05-02 16:35:59.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/Revio_semi_torch.json
+-rw-r--r--   0      501       20    32320 2023-05-02 16:35:43.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt
+-rw-r--r--   0      501       20  2589234 2022-11-17 21:59:57.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json
+-rw-r--r--   0      501       20  2579653 2022-11-17 21:59:57.000000 pyft-0.1.6/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json
+-rw-r--r--   0      501       20    18323 2023-07-22 22:54:01.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/basemods/mod.rs
+-rw-r--r--   0      501       20    12588 2023-07-22 20:33:30.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/center.rs
+-rw-r--r--   0      501       20    10971 2023-07-22 19:51:25.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/cli.rs
+-rw-r--r--   0      501       20    18362 2023-07-22 20:40:22.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/extract.rs
+-rw-r--r--   0      501       20     4129 2023-07-22 01:59:45.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/lib.rs
+-rw-r--r--   0      501       20     9233 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/main.rs
+-rw-r--r--   0      501       20    12907 2023-07-21 05:47:41.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/nucleosomes.rs
+-rw-r--r--   0      501       20     3476 2023-06-18 04:21:08.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs
+-rw-r--r--   0      501       20    18361 2023-07-21 00:03:41.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs
+-rw-r--r--   0      501       20     1684 2023-03-10 15:54:29.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs
+-rw-r--r--   0      501       20     1588 2023-06-29 17:25:52.000000 pyft-0.1.6/local_dependencies/fibertools-rs/src/strip_basemods.rs
+-rw-r--r--   0      501       20  1529300 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/all.bam
+-rw-r--r--   0      501       20     1792 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/all.bam.bai
+-rw-r--r--   0      501       20  4202969 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bam
+-rw-r--r--   0      501       20   758264 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bam.bai
+-rw-r--r--   0      501       20     3349 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bed
+-rw-r--r--   0      501       20    17525 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam
+-rw-r--r--   0      501       20       13 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/test.txt
+-rw-r--r--   0      501       20       72 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/test.txt.gz
+-rw-r--r--   0      501       20     1780 2023-07-21 22:42:46.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/extract_test.rs
+-rw-r--r--   0      501       20     2216 2023-07-19 18:23:20.000000 pyft-0.1.6/local_dependencies/fibertools-rs/tests/run_test.rs
+-rw-r--r--   0        0        0      565 1970-01-01 00:00:00.000000 pyft-0.1.6/Cargo.toml
+-rw-r--r--   0      501       20     2807 2023-07-19 21:04:05.000000 pyft-0.1.6/.github/workflows/CI.yml
+-rw-r--r--   0      501       20      692 2023-07-19 21:52:50.000000 pyft-0.1.6/.gitignore
+-rw-r--r--   0      501       20      382 2023-07-23 16:19:13.000000 pyft-0.1.6/README.md
+-rw-r--r--   0      501       20      634 2023-07-20 03:00:42.000000 pyft-0.1.6/docs/Makefile
+-rw-r--r--   0      501       20     2216 2023-07-20 18:11:44.000000 pyft-0.1.6/docs/_static/css/rtd_dark.css
+-rw-r--r--   0      501       20   160734 2023-07-20 16:45:23.000000 pyft-0.1.6/docs/_static/img/fiber_tools_grey.png
+-rw-r--r--   0      501       20      294 2023-07-20 17:07:50.000000 pyft-0.1.6/docs/_templates/layout.html
+-rw-r--r--   0      501       20     1695 2023-07-23 14:42:32.000000 pyft-0.1.6/docs/conf.py
+-rw-r--r--   0      501       20       76 2023-07-20 18:49:05.000000 pyft-0.1.6/docs/environment.yml
+-rw-r--r--   0      501       20     1277 2023-07-23 16:17:21.000000 pyft-0.1.6/docs/index.rst
+-rw-r--r--   0      501       20      800 2023-07-20 03:00:42.000000 pyft-0.1.6/docs/make.bat
+-rw-r--r--   0      501       20       46 2023-07-20 17:01:46.000000 pyft-0.1.6/docs/modules.rst
+-rw-r--r--   0      501       20      141 2023-07-20 17:44:28.000000 pyft-0.1.6/docs/pyft.rst
+-rw-r--r--   0      501       20      113 2023-07-23 14:43:25.000000 pyft-0.1.6/docs/requirements.txt
+-rw-r--r--   0      501       20      651 2023-07-23 16:09:17.000000 pyft-0.1.6/example.py
+-rw-r--r--   0      501       20      357 2023-07-20 17:34:33.000000 pyft-0.1.6/pyproject.toml
+-rw-r--r--   0      501       20    10384 2023-07-23 15:56:41.000000 pyft-0.1.6/src/fiberdata.rs
+-rw-r--r--   0      501       20      698 2023-07-23 15:42:43.000000 pyft-0.1.6/src/lib.rs
+-rw-r--r--   0      501       20    49806 2023-07-23 16:18:07.000000 pyft-0.1.6/Cargo.lock
+-rw-r--r--   0        0        0      705 1970-01-01 00:00:00.000000 pyft-0.1.6/PKG-INFO
```

### Comparing `pyft-0.1.5/local_dependencies/bamlift/src/lib.rs` & `pyft-0.1.6/local_dependencies/bamlift/src/lib.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/bamlift/tests/test-liftover.rs` & `pyft-0.1.6/local_dependencies/bamlift/tests/test-liftover.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/bio-io/Cargo.toml` & `pyft-0.1.6/local_dependencies/bio-io/Cargo.toml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/bio-io/src/lib.rs` & `pyft-0.1.6/local_dependencies/bio-io/src/lib.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/Cargo.toml` & `pyft-0.1.6/local_dependencies/fibertools-rs/Cargo.toml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/.github/workflows/CI.yml` & `pyft-0.1.6/local_dependencies/fibertools-rs/.github/workflows/CI.yml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/.github/workflows/release.yml` & `pyft-0.1.6/local_dependencies/fibertools-rs/.github/workflows/release.yml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/CHANGELOG.md` & `pyft-0.1.6/local_dependencies/fibertools-rs/CHANGELOG.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/Cargo.lock` & `pyft-0.1.6/local_dependencies/fibertools-rs/Cargo.lock`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/Dockerfile` & `pyft-0.1.6/local_dependencies/fibertools-rs/Dockerfile`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/INSTALL.md` & `pyft-0.1.6/local_dependencies/fibertools-rs/INSTALL.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/README.md` & `pyft-0.1.6/local_dependencies/fibertools-rs/README.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/center.png` & `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/center.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png` & `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/fiber_tools_grey.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png` & `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/fiber_tools_teal.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png` & `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/ft-extract-all.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/assets/img/logo.png` & `pyft-0.1.6/local_dependencies/fibertools-rs/assets/img/logo.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/build.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/build.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft--help.md` & `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft--help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md` & `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-add-nucleosomes-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-center-help.md` & `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-center-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-extract-help.md` & `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-extract-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md` & `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-predict-m6a-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md` & `pyft-0.1.6/local_dependencies/fibertools-rs/docs/ft-strip-basemods-help.md`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/docs/make_help_docs.sh` & `pyft-0.1.6/local_dependencies/fibertools-rs/docs/make_help_docs.sh`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_semi_torch.json` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.0_torch.pt` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.0_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_semi_torch.json` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/2.2_torch.pt` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/2.2_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/3.2_semi_torch.json` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/3.2_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/3.2_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/Revio_semi_torch.json` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/Revio_semi_torch.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/Revio_semi_torch.pt`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.0.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json` & `pyft-0.1.6/local_dependencies/fibertools-rs/models/gbdt_0.81_p2.2.json`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/basemods/mod.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/basemods/mod.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/center.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/center.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/cli.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/cli.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/extract.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/extract.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/lib.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/lib.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/main.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/main.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/nucleosomes.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/nucleosomes.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/cnn.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/mod.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/predict_m6a/xgb.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/src/strip_basemods.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/src/strip_basemods.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/all.bam` & `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/all.bam`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/all.bam.bai` & `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/all.bam.bai`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bam` & `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bam`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bam.bai` & `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bam.bai`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/center.bed` & `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/center.bed`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam` & `pyft-0.1.6/local_dependencies/fibertools-rs/tests/data/msp_nuc.bam`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/tests/extract_test.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/tests/extract_test.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/local_dependencies/fibertools-rs/tests/run_test.rs` & `pyft-0.1.6/local_dependencies/fibertools-rs/tests/run_test.rs`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/Cargo.toml` & `pyft-0.1.6/Cargo.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [package]
 edition = "2021"
 name = "pyft"
-version = "0.1.5"
+version = "0.1.6"
 
 # See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html
 [lib]
 crate-type = ["cdylib"]
 name = "pyft"
 
 [dependencies]
```

### Comparing `pyft-0.1.5/.github/workflows/CI.yml` & `pyft-0.1.6/.github/workflows/CI.yml`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/.gitignore` & `pyft-0.1.6/.gitignore`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/docs/Makefile` & `pyft-0.1.6/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/docs/_static/css/rtd_dark.css` & `pyft-0.1.6/docs/_static/css/rtd_dark.css`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/docs/_static/img/fiber_tools_grey.png` & `pyft-0.1.6/docs/_static/img/fiber_tools_grey.png`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/docs/conf.py` & `pyft-0.1.6/docs/conf.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 # Configuration file for the Sphinx documentation builder.
 #
 # For the full list of built-in configuration values, see the documentation:
 # https://www.sphinx-doc.org/en/master/usage/configuration.html
 import os
-import sphinx
 import re
 import sys
-import sphinx.ext.autosummary as autosummary
+#import sphinx
+#import sphinx.ext.autosummary as autosummary
 sys.path.insert(0, os.path.abspath("../"))
 import pyft
 
 # -- Project information -----------------------------------------------------
 # https://www.sphinx-doc.org/en/master/usage/configuration.html#project-information
 # The short X.Y version.
 project = "pyft"
@@ -21,14 +21,15 @@
 
 
 # -- General configuration ---------------------------------------------------
 # https://www.sphinx-doc.org/en/master/usage/configuration.html#general-configuration
 
 extensions = [
     "sphinx.ext.autodoc",
+    "sphinx_autodoc_typehints",
     "sphinx.ext.viewcode",
     #"sphinx.ext.napoleon",
     "sphinx_rtd_theme",
     "sphinx.ext.intersphinx",
     #"edit_on_github",
     "m2r2",
 ]
@@ -39,16 +40,18 @@
 templates_path = ["_templates"]
 exclude_patterns = ["_build", "Thumbs.db", ".DS_Store"]
 
 
 # -- Options for HTML output -------------------------------------------------
 # https://www.sphinx-doc.org/en/master/usage/configuration.html#options-for-html-output
 
-# html_theme = "alabaster"
+#html_theme = "alabaster"
 html_theme = "sphinx_rtd_theme"
+#html_permalinks_icon = '<span>#</span>'
+#html_theme = 'sphinxawesome_theme'
 html_static_path = ["_static"]
 html_css_files = [
     "css/rtd_dark.css",
 ]
 html_logo = "_static/img/fiber_tools_grey.png"
```

### Comparing `pyft-0.1.5/docs/make.bat` & `pyft-0.1.6/docs/make.bat`

 * *Files identical despite different names*

### Comparing `pyft-0.1.5/src/fiberdata.rs` & `pyft-0.1.6/src/fiberdata.rs`

 * *Files 9% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 use fibertools_rs::extract::FiberseqData;
 use pyo3::iter::IterNextOutput;
 use pyo3::prelude::*;
 use rust_htslib::{bam, bam::ext::BamRecordExtensions, bam::record::Aux, bam::Read};
+use std::time;
 use std::vec::IntoIter;
 
 #[pyclass]
 /// Record class for fiberseq data, corresponding to a single bam record
 pub struct Fiberdata {
     /// Number of ccs passes
     #[pyo3(get, set)]
@@ -189,56 +190,97 @@
     }
 }
 
 #[pyclass]
 /// Create a fibertools iterator from an indexed bam file.
 /// Must provide a valid chrom, start, and end.
 /// Returns an iterator over :class:`~pyft.Fiberdata` objects.
-pub struct FiberdataFetch {
-    fiberdata: IntoIter<FiberseqData>,
-    //_inner: Rc<RefCell<bam::IndexedReader>>,
-    //fiberdata: Box<dyn Iterator<Item = FiberseqData> + Send + 'static>,
-    //fiberdata: Box<dyn Iterator<Item = FiberseqData> + Send + 'static>,
+pub struct Fiberbam {
+    bam: bam::IndexedReader,
+    header: bam::Header,
+    start: time::Instant,
 }
 
 #[pymethods]
-impl FiberdataFetch {
+/// Open a fiberseq bam file. Must have an index.
+impl Fiberbam {
     #[new]
-    pub fn new(f: &str, chrom: &str, start: i64, end: i64) -> Self {
+    pub fn new(f: &str) -> Self {
         let mut bam = bam::IndexedReader::from_path(f).expect("unable to open indexed bam file");
         bam.set_threads(8).unwrap();
         let header = bam::Header::from_template(bam.header());
-        let head_view = bam::HeaderView::from_header(&header);
-        bam.fetch((chrom, start, end))
+        let start = time::Instant::now();
+        Self { bam, header, start }
+    }
+
+    /// Returns an iterator over :class:`~pyft.Fiberdata` objects for the selected region.
+    pub fn fetch(&mut self, chrom: &str, start: i64, end: i64) -> Fiberiter {
+        let head_view = bam::HeaderView::from_header(&self.header);
+        self.bam
+            .fetch((chrom, start, end))
             .expect("unable to fetch region");
-        let records: Vec<bam::Record> = bam.records().map(|r| r.unwrap()).collect();
-        log::info!("{} records fetched", records.len());
-        let fiberdata = FiberseqData::from_records(records, &head_view, 0).into_iter();
-        log::info!("fiberdata created from records");
-        /*let fiberdata = bam
-        .records()
-        .map(|rec| FiberseqData::new(&rec.unwrap(), None, 0))
-        .into_iter();*/
-        Self { fiberdata }
+        let records: Vec<bam::Record> = self.bam.records().map(|r| r.unwrap()).collect();
+
+        log::info!(
+            "{} records fetched in {:.2}s",
+            records.len(),
+            self.time_from_last()
+        );
+        let fiberdata = FiberseqData::from_records(records, &head_view, 0);
+        log::info!(
+            "Fiberdata made for {} records in {:.2}s",
+            fiberdata.len(),
+            self.time_from_last()
+        );
+        build_fiberdata_iter(fiberdata)
+    }
+
+    fn time_from_last(&mut self) -> f64 {
+        let elapsed = self.start.elapsed().as_secs_f64();
+        self.start = time::Instant::now();
+        elapsed
     }
+}
+
+fn build_fiberdata_iter(fiberdata: Vec<FiberseqData>) -> Fiberiter {
+    let length = fiberdata.len();
+    Fiberiter {
+        fiberdata: fiberdata.into_iter(),
+        length,
+    }
+}
 
+#[pyclass]
+/// An iterator over :class:`~pyft.Fiberdata` objects.
+pub struct Fiberiter {
+    fiberdata: IntoIter<FiberseqData>,
+    length: usize,
+}
+
+#[pymethods]
+impl Fiberiter {
     fn __next__(&mut self) -> IterNextOutput<Fiberdata, &'static str> {
         let data = self.fiberdata.next();
         match data {
             Some(fiber) => IterNextOutput::Yield(new_py_fiberdata(fiber)),
-            None => {
-                log::info!("\n\nDone iterating over fibers");
-                IterNextOutput::Return("Ended")
-            }
+            None => IterNextOutput::Return("Ended"),
         }
     }
 
     fn __iter__(slf: PyRef<'_, Self>) -> PyRef<'_, Self> {
         slf
     }
+
+    fn __len__(&self) -> usize {
+        self.length
+    }
+
+    fn len(&self) -> usize {
+        self.length
+    }
 }
 
 /// Class for describing base modifications within fiberseq data.
 /// For example, m6a and 5mC (cpg) features.
 #[pyclass]
 #[derive(Clone)]
 pub struct Basemods {
```

### Comparing `pyft-0.1.5/src/lib.rs` & `pyft-0.1.6/src/lib.rs`

 * *Files 10% similar despite different names*

```diff
@@ -11,13 +11,14 @@
     Builder::new()
         .format_timestamp_secs()
         .target(Target::Stderr)
         .filter(None, LevelFilter::Info)
         .init();
 
     m.add("__version__", env!("CARGO_PKG_VERSION"))?;
-    m.add_class::<fiberdata::FiberdataFetch>()?;
+    m.add_class::<fiberdata::Fiberbam>()?;
+    m.add_class::<fiberdata::Fiberiter>()?;
     m.add_class::<fiberdata::Fiberdata>()?;
     m.add_class::<fiberdata::Basemods>()?;
     m.add_class::<fiberdata::Ranges>()?;
     Ok(())
 }
```

### Comparing `pyft-0.1.5/Cargo.lock` & `pyft-0.1.6/Cargo.lock`

 * *Files 0% similar despite different names*

```diff
@@ -1198,15 +1198,15 @@
 checksum = "18fb31db3f9bddb2ea821cde30a9f70117e3f119938b5ee630b7403aa6e2ead9"
 dependencies = [
  "unicode-ident",
 ]
 
 [[package]]
 name = "pyft"
-version = "0.1.5"
+version = "0.1.6"
 dependencies = [
  "anyhow",
  "bamlift",
  "bio-io",
  "colored",
  "env_logger 0.10.0",
  "fibertools-rs",
```

