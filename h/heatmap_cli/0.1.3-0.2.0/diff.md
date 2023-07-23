# Comparing `tmp/heatmap_cli-0.1.3.tar.gz` & `tmp/heatmap_cli-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "heatmap_cli-0.1.3.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "heatmap_cli-0.2.0.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `heatmap_cli-0.1.3.tar` & `heatmap_cli-0.2.0.tar`

### file list

```diff
@@ -1,33 +1,35 @@
--rw-r--r--   0        0        0      143 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/.coveragerc
--rw-r--r--   0        0        0     3101 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/.gitignore
--rw-r--r--   0        0        0     2465 2023-07-12 17:30:43.846915 heatmap_cli-0.1.3/.pre-commit-config.yaml
--rw-r--r--   0        0        0       13 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/.prettierignore
--rw-r--r--   0        0        0       29 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/.python-version
--rw-r--r--   0        0        0      861 2023-07-16 01:33:45.437513 heatmap_cli-0.1.3/CHANGELOG.md
--rw-r--r--   0        0        0     2002 2023-07-14 00:05:31.556357 heatmap_cli-0.1.3/CONTRIBUTING.md
--rw-r--r--   0        0        0    31956 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/LICENSE.md
--rw-r--r--   0        0        0      502 2023-07-11 18:27:30.048786 heatmap_cli-0.1.3/Pipfile
--rw-r--r--   0        0        0   112832 2023-07-14 00:02:43.363808 heatmap_cli-0.1.3/Pipfile.lock
--rw-r--r--   0        0        0     1927 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/README.md
--rw-r--r--   0        0        0      638 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/docs/Makefile
--rw-r--r--   0        0        0      804 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/docs/make.bat
-lrwxr-xr-x   0        0        0        0 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/docs/source/CHANGELOG.md -> ../../CHANGELOG.md
-lrwxr-xr-x   0        0        0        0 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/docs/source/CONTRIBUTING.md -> ../../CONTRIBUTING.md
-lrwxr-xr-x   0        0        0        0 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/docs/source/LICENSE.md -> ../../LICENSE.md
-lrwxr-xr-x   0        0        0        0 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/docs/source/README.md -> ../../README.md
--rw-r--r--   0        0        0    14202 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/docs/source/_static/logo.jpg
--rw-r--r--   0        0        0     1555 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/docs/source/conf.py
--rw-r--r--   0        0        0      172 2023-07-10 15:24:28.645268 heatmap_cli-0.1.3/docs/source/index.rst
--rw-r--r--   0        0        0      779 2023-07-16 01:34:05.737145 heatmap_cli-0.1.3/heatmap_cli/__init__.py
--rw-r--r--   0        0        0      837 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/heatmap_cli/__main__.py
--rw-r--r--   0        0        0     5395 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/heatmap_cli/cli.py
--rw-r--r--   0        0        0     1077 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/tests/__init__.py
--rw-r--r--   0        0        0      845 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/tests/conftest.py
--rw-r--r--   0        0        0     5810 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/tests/fixtures/sample.csv
--rw-r--r--   0        0        0      303 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/tests/test_debug_flag.py
--rw-r--r--   0        0        0      326 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/tests/test_help_flag.py
--rw-r--r--   0        0        0      545 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/tests/test_verbose_flag.py
--rw-r--r--   0        0        0      306 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/tests/test_version_flag.py
--rw-r--r--   0        0        0      673 2023-07-10 15:24:28.649268 heatmap_cli-0.1.3/tox.ini
--rw-r--r--   0        0        0     2925 1970-01-01 00:00:00.000000 heatmap_cli-0.1.3/PKG-INFO
+-rw-r--r--   0        0        0      146 2023-07-19 03:38:50.545154 heatmap_cli-0.2.0/.coveragerc
+-rw-r--r--   0        0        0     3101 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/.gitignore
+-rw-r--r--   0        0        0     2589 2023-07-19 03:34:58.303707 heatmap_cli-0.2.0/.pre-commit-config.yaml
+-rw-r--r--   0        0        0       13 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/.prettierignore
+-rw-r--r--   0        0        0       29 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/.python-version
+-rw-r--r--   0        0        0     1338 2023-07-23 13:16:55.486422 heatmap_cli-0.2.0/CHANGELOG.md
+-rw-r--r--   0        0        0     1967 2023-07-22 05:51:16.547471 heatmap_cli-0.2.0/CONTRIBUTING.md
+-rw-r--r--   0        0        0    31956 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/LICENSE.md
+-rw-r--r--   0        0        0      509 2023-07-21 00:25:50.551442 heatmap_cli-0.2.0/Pipfile
+-rw-r--r--   0        0        0   126616 2023-07-22 05:38:41.247816 heatmap_cli-0.2.0/Pipfile.lock
+-rw-r--r--   0        0        0     2154 2023-07-19 10:02:05.708726 heatmap_cli-0.2.0/README.md
+-rw-r--r--   0        0        0      638 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/docs/Makefile
+-rw-r--r--   0        0        0      804 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/docs/make.bat
+lrwxr-xr-x   0        0        0        0 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/docs/source/CHANGELOG.md -> ../../CHANGELOG.md
+lrwxr-xr-x   0        0        0        0 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/docs/source/CONTRIBUTING.md -> ../../CONTRIBUTING.md
+lrwxr-xr-x   0        0        0        0 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/docs/source/LICENSE.md -> ../../LICENSE.md
+lrwxr-xr-x   0        0        0        0 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/docs/source/README.md -> ../../README.md
+-rw-r--r--   0        0        0    14202 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/docs/source/_static/logo.jpg
+-rw-r--r--   0        0        0     1555 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/docs/source/conf.py
+-rw-r--r--   0        0        0      172 2023-07-10 15:24:28.645268 heatmap_cli-0.2.0/docs/source/index.rst
+-rw-r--r--   0        0        0      779 2023-07-23 13:17:18.614611 heatmap_cli-0.2.0/heatmap_cli/__init__.py
+-rw-r--r--   0        0        0      837 2023-07-10 15:24:28.649268 heatmap_cli-0.2.0/heatmap_cli/__main__.py
+-rw-r--r--   0        0        0     6792 2023-07-19 10:08:43.813639 heatmap_cli-0.2.0/heatmap_cli/cli.py
+-rw-r--r--   0        0        0     1077 2023-07-17 23:52:03.000872 heatmap_cli-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-10 15:24:28.649268 heatmap_cli-0.2.0/tests/__init__.py
+-rw-r--r--   0        0        0      845 2023-07-10 15:24:28.649268 heatmap_cli-0.2.0/tests/conftest.py
+-rw-r--r--   0        0        0     5810 2023-07-10 15:24:28.649268 heatmap_cli-0.2.0/tests/fixtures/sample.csv
+-rw-r--r--   0        0        0      358 2023-07-19 03:58:00.025209 heatmap_cli-0.2.0/tests/test_debug_flag.py
+-rw-r--r--   0        0        0      326 2023-07-10 15:24:28.649268 heatmap_cli-0.2.0/tests/test_help_flag.py
+-rw-r--r--   0        0        0      545 2023-07-10 15:24:28.649268 heatmap_cli-0.2.0/tests/test_verbose_flag.py
+-rw-r--r--   0        0        0      306 2023-07-10 15:24:28.649268 heatmap_cli-0.2.0/tests/test_version_flag.py
+-rw-r--r--   0        0        0      306 2023-07-19 23:00:14.071564 heatmap_cli-0.2.0/tests/test_week_flag.py
+-rw-r--r--   0        0        0      516 2023-07-19 03:33:39.924975 heatmap_cli-0.2.0/tests/test_year_flag.py
+-rw-r--r--   0        0        0      682 2023-07-22 05:50:59.467336 heatmap_cli-0.2.0/tox.ini
+-rw-r--r--   0        0        0     3152 1970-01-01 00:00:00.000000 heatmap_cli-0.2.0/PKG-INFO
```

### Comparing `heatmap_cli-0.1.3/.gitignore` & `heatmap_cli-0.2.0/.gitignore`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/.pre-commit-config.yaml` & `heatmap_cli-0.2.0/.pre-commit-config.yaml`

 * *Files 4% similar despite different names*

```diff
@@ -1,17 +1,21 @@
 # See https://pre-commit.com for more information
 # See https://pre-commit.com/hooks.html for more hooks
 repos:
   - repo: https://github.com/pre-commit/pre-commit-hooks
     rev: v4.4.0
     hooks:
-      - id: trailing-whitespace
-      - id: end-of-file-fixer
-      - id: check-yaml
+      - id: check-case-conflict
+      - id: check-merge-conflict
       - id: check-toml
+      - id: check-yaml
+      - id: debug-statements
+      - id: end-of-file-fixer
+      - id: mixed-line-ending
+      - id: trailing-whitespace
 
   - repo: https://github.com/abravalheri/validate-pyproject
     rev: v0.13
     hooks:
       - id: validate-pyproject
         name: validate-pyproject
 
@@ -35,24 +39,24 @@
           - isort[pyproject]
         args:
           - --profile=black
           - --line-length=79
           - --py=311
 
   - repo: https://github.com/psf/black
-    rev: 23.3.0
+    rev: 23.7.0
     hooks:
       - id: black
         language_version: python3.11
         args:
           - --line-length=79
           - --target-version=py311
 
   - repo: https://github.com/asottile/blacken-docs
-    rev: 1.14.0
+    rev: 1.15.0
     hooks:
       - id: blacken-docs
         additional_dependencies:
           - black==22.8.0
 
   - repo: https://github.com/PyCQA/autoflake
     rev: v2.2.0
```

### Comparing `heatmap_cli-0.1.3/CHANGELOG.md` & `heatmap_cli-0.2.0/CHANGELOG.md`

 * *Files 12% similar despite different names*

```diff
@@ -3,27 +3,46 @@
 All notable changes to this project will be documented in this file.
 
 The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
 and this project adheres to [0-based versioning](https://0ver.org/).
 
 ## [Unreleased]
 
+## v0.2.0 (2023-07-23)
+
+## Added
+
+- Add `yr` or `--year` argument to filter CSV data by year
+- Add `wk` or `--week` argument to filter CSV data until week of the year
+- Add additional pre-commit default checks
+- Show generated PNG filename upon completion
+
+### Changed
+
+- Group all `sphinx` related deps under the `doc` category
+- Standardize `tox` environment names
+
+### Fixed
+
+- Fix incorrect ignored coverage module
+- Suppress logging from `matplotlib` in `debug` mode
+
 ## v0.1.3 (2023-07-16)
 
 ### Fixed
 
 - Fix missing `pylint` dependency when running `pre-commit`
-- Ignore word when running codespell pre-commit hook
+- Ignore word when running `codespell` pre-commit hook
 
 ## v0.1.2 (2023-07-11)
 
 ### Changed
 
 - Link to license from contributing doc
-- Use the same output folder for sphinx doc generation
+- Use the same output folder for `sphinx` doc generation
 - Revise `pyenv` installation with plugins in contributing doc
 - Install `heatmap_cli` as editable installation in `pipenv` dev env
 
 ## v0.1.1 (2023-07-09)
 
 ### Fixed
```

### Comparing `heatmap_cli-0.1.3/CONTRIBUTING.md` & `heatmap_cli-0.2.0/CONTRIBUTING.md`

 * *Files 3% similar despite different names*

```diff
@@ -46,22 +46,21 @@
 ```console
 tox -av
 ```
 
 ```console
 ...
 default environments:
-py37  -> testing against python3.7
 py38  -> testing against python3.8
 py39  -> testing against python3.9
 py310 -> testing against python3.10
 py311 -> testing against python3.11
 
 additional environments:
-cover -> generate code coverage report in html
+cov   -> generate code coverage report in html
 doc   -> generate sphinx documentation in html
 ```
 
 For code linting, we're using `pre-commit`:
 
 ```console
 pre-commit install # run once
```

### Comparing `heatmap_cli-0.1.3/LICENSE.md` & `heatmap_cli-0.2.0/LICENSE.md`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/Pipfile.lock` & `heatmap_cli-0.2.0/Pipfile.lock`

 * *Files 4% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.7062789351851853%*

 * *Differences: {"'_meta'": "{'hash': {'sha256': "*

 * *            "'d95a8d076e13eb367097bca6d3fffc026d70ba6e605d6a565ceef9fb7a4bfd50'}}",*

 * * "'default'": "{'fonttools': {'hashes': "*

 * *              "['sha256:1df1b6f4c7c4bc8201eb47f3b268adbf2539943aa43c400f84556557e3e109c0', "*

 * *              "'sha256:2a22b2c425c698dcd5d6b0ff0b566e8e9663172118db6fd5f1941f9b8063da9b', "*

 * *              "'sha256:33191f062549e6bb1a4782c22a04ebd37009c09360e2d6686ac5083774d06d95', "*

 * *              "'sha256:38cdecd8f1fd4bf4daae7fed1b3170dfc1b523388d6664b2204 […]*

```diff
@@ -1,11 +1,11 @@
 {
     "_meta": {
         "hash": {
-            "sha256": "ed8ff138dfd0bd29c1c47d73779ecdf62e73179a3358a78ba95d6e5b5c266bcf"
+            "sha256": "d95a8d076e13eb367097bca6d3fffc026d70ba6e605d6a565ceef9fb7a4bfd50"
         },
         "pipfile-spec": 6,
         "requires": {
             "python_version": "3.8"
         },
         "sources": [
             {
@@ -67,51 +67,51 @@
                 "sha256:9c87405839a19696e837b3b818fed3f5f69f16f1eec1a1ad77e043dcea9c772f"
             ],
             "markers": "python_version >= '3.6'",
             "version": "==0.11.0"
         },
         "fonttools": {
             "hashes": [
-                "sha256:0614b6348866092d00df3dfb37e037fc06412ca67087de361a2777ea5ed62c16",
-                "sha256:06eac087ea55b3ebb2207d93b5ac56c847163899f05f5a77e1910f688fe10030",
-                "sha256:19d461c801b8904d201c6c38a99bfcfef673bfdfe0c7f026f582ef78896434e0",
-                "sha256:381558eafffc1432d08ca58063e71c7376ecaae48e9318354a90a1049a644845",
-                "sha256:3ee75b8ca48f6c48af25e967dce995ef94e46872b35c7d454b983c62c9c7006d",
-                "sha256:415cf7c806a3f56fb280dadcf3c92c85c0415e75665ca957b4a2a2e39c17a5c9",
-                "sha256:465d0f24bf4f75160f441793b55076b7a080a57d3a1f738390af2c20bee24fbb",
-                "sha256:4c654b1facf1f3b742e4d9b2dcdf0fa867b1f007b1b4981cc58a75ef5dca2a3c",
-                "sha256:50f8bdb421270f71b54695c62785e300fab4bb6127be40bf9f3084962a0c3adb",
-                "sha256:5448a87f6ed57ed844b64a05d3792827af584a8584613f6289867f4e77eb603b",
-                "sha256:560ea1a604c927399f36742abf342a4c5f3fee8e8e8a484b774dfe9630bd9a91",
-                "sha256:5b1c2b21b40229166a864f2b0aec06d37f0a204066deb1734c93370e0c76339d",
-                "sha256:69178674505ec81adf4af2a3bbacd0cb9a37ba7831bc3fca307f80e48ab2767b",
-                "sha256:69dbe0154e15b68dd671441ea8f23dad87488b24a6e650d45958f4722819a443",
-                "sha256:6faff25991dec48f8cac882055a09ae1a29fd15bc160bc3d663e789e994664c2",
-                "sha256:72d40a32d6443871ea0d147813caad58394b48729dfa4fbc45dcaac54f9506f2",
-                "sha256:7e22d0144d735f6c7df770509b8c0c33414bf460df0d5dddc98a159e5dbb10eb",
-                "sha256:841c491fa3e9c54e8f9cd5dae059e88f45e086aea090c28be9d42f59c8b99e01",
-                "sha256:86edb95c4d1fe4fae2111d7e0c10c6e42b7790b377bcf1952303469eee5b52bb",
-                "sha256:8f602dd5bcde7e4241419924f23c6f0d66723dd5408a58c3a2f781745c693f45",
-                "sha256:9387b09694fbf8ac7dcf887069068f81fb4124d05e09557ac7daabfbec1744bd",
-                "sha256:b329ae7ce971b5c4148d6cdb8119c0ce4587265b2330d4f2f3776ef851bee020",
-                "sha256:ba2a367ff478cd108d5319c0dc4fd4eb4ea3476dbfc45b00c45718e889cd9463",
-                "sha256:bc9e7b1e268be7a23fc66471b615c324e99c5db39ce8c49dd6dd8e962c7bc1b8",
-                "sha256:c890061915e95b619c1d3cc3c107c6fb021406b701c0c24b03e74830d522f210",
-                "sha256:cc3324e4159e6d1f55c3615b4c1c211f87cc96cc0cc7c946c8447dc1319f2e9d",
-                "sha256:d2dae84a3d0f76884a6102c62f2795b2d6602c2c95cfcce74c8a590b6200e533",
-                "sha256:d45f28c20bb67dee0f4a4caae709f40b0693d764b7b2bf2d58890f36b1bfcef0",
-                "sha256:e38bd91eae257f36c2b7245c0278e9cd9d754f3a66b8d2b548c623ba66e387b6",
-                "sha256:e43f6c7f9ba4f9d29edee530e45f9aa162872ec9549398b85971477a99f2a806",
-                "sha256:ea879afd1d6189fca02a85a7868560c9bb8415dccff6b7ae6d81e4f06b3ab30d",
-                "sha256:eb9dfa87152bd97019adc387b2f29ef6af601de4386f36570ca537ace96d96ed",
-                "sha256:efd59e83223cb77952997fb850c7a7c2a958c9af0642060f536722c2a9e9d53b",
-                "sha256:f3fe90dfb297bd8265238c06787911cd81c2cb89ac5b13e1c911928bdabfce0f"
+                "sha256:1df1b6f4c7c4bc8201eb47f3b268adbf2539943aa43c400f84556557e3e109c0",
+                "sha256:2a22b2c425c698dcd5d6b0ff0b566e8e9663172118db6fd5f1941f9b8063da9b",
+                "sha256:33191f062549e6bb1a4782c22a04ebd37009c09360e2d6686ac5083774d06d95",
+                "sha256:38cdecd8f1fd4bf4daae7fed1b3170dfc1b523388d6664b2204b351820aa78a7",
+                "sha256:3ae64303ba670f8959fdaaa30ba0c2dabe75364fdec1caeee596c45d51ca3425",
+                "sha256:3d1f9471134affc1e3b1b806db6e3e2ad3fa99439e332f1881a474c825101096",
+                "sha256:4e3334d51f0e37e2c6056e67141b2adabc92613a968797e2571ca8a03bd64773",
+                "sha256:4edc795533421e98f60acee7d28fc8d941ff5ac10f44668c9c3635ad72ae9045",
+                "sha256:547ab36a799dded58a46fa647266c24d0ed43a66028cd1cd4370b246ad426cac",
+                "sha256:59eba8b2e749a1de85760da22333f3d17c42b66e03758855a12a2a542723c6e7",
+                "sha256:704bccd69b0abb6fab9f5e4d2b75896afa48b427caa2c7988792a2ffce35b441",
+                "sha256:73ef0bb5d60eb02ba4d3a7d23ada32184bd86007cb2de3657cfcb1175325fc83",
+                "sha256:7763316111df7b5165529f4183a334aa24c13cdb5375ffa1dc8ce309c8bf4e5c",
+                "sha256:849ec722bbf7d3501a0e879e57dec1fc54919d31bff3f690af30bb87970f9784",
+                "sha256:891cfc5a83b0307688f78b9bb446f03a7a1ad981690ac8362f50518bc6153975",
+                "sha256:952cb405f78734cf6466252fec42e206450d1a6715746013f64df9cbd4f896fa",
+                "sha256:a7bbb290d13c6dd718ec2c3db46fe6c5f6811e7ea1e07f145fd8468176398224",
+                "sha256:a9b3cc10dc9e0834b6665fd63ae0c6964c6bc3d7166e9bc84772e0edd09f9fa2",
+                "sha256:aaaef294d8e411f0ecb778a0aefd11bb5884c9b8333cc1011bdaf3b58ca4bd75",
+                "sha256:afce2aeb80be72b4da7dd114f10f04873ff512793d13ce0b19d12b2a4c44c0f0",
+                "sha256:b0938ebbeccf7c80bb9a15e31645cf831572c3a33d5cc69abe436e7000c61b14",
+                "sha256:b2d1ee95be42b80d1f002d1ee0a51d7a435ea90d36f1a5ae331be9962ee5a3f1",
+                "sha256:b927e5f466d99c03e6e20961946314b81d6e3490d95865ef88061144d9f62e38",
+                "sha256:bdd729744ae7ecd7f7311ad25d99da4999003dcfe43b436cf3c333d4e68de73d",
+                "sha256:c2071267deaa6d93cb16288613419679c77220543551cbe61da02c93d92df72f",
+                "sha256:cac73bbef7734e78c60949da11c4903ee5837168e58772371bd42a75872f4f82",
+                "sha256:da2c2964bdc827ba6b8a91dc6de792620be4da3922c4cf0599f36a488c07e2b2",
+                "sha256:e16a9449f21a93909c5be2f5ed5246420f2316e94195dbfccb5238aaa38f9751",
+                "sha256:e5c2b0a95a221838991e2f0e455dec1ca3a8cc9cd54febd68cc64d40fdb83669",
+                "sha256:ec453a45778524f925a8f20fd26a3326f398bfc55d534e37bab470c5e415caa1",
+                "sha256:edee0900cf0eedb29d17c7876102d6e5a91ee333882b1f5abc83e85b934cadb5",
+                "sha256:f14f3ccea4cc7dd1b277385adf3c3bf18f9860f87eab9c2fb650b0af16800f55",
+                "sha256:f240d9adf0583ac8fc1646afe7f4ac039022b6f8fa4f1575a2cfa53675360b69",
+                "sha256:f48602c0b3fd79cd83a34c40af565fe6db7ac9085c8823b552e6e751e3a5b8be"
             ],
             "markers": "python_version >= '3.8'",
-            "version": "==4.41.0"
+            "version": "==4.41.1"
         },
         "heatmap-cli": {
             "editable": true,
             "path": "."
         },
         "importlib-resources": {
             "hashes": [
@@ -422,46 +422,30 @@
                 "sha256:7e65763eef3120314099b6939b5546db7adce1e7d6f2e179e3df563c70511eda"
             ],
             "markers": "python_version >= '2'",
             "version": "==2023.3"
         },
         "zipp": {
             "hashes": [
-                "sha256:0b37c326d826d5ca35f2b9685cd750292740774ef16190008b00a0227c256fe0",
-                "sha256:857b158da2cbf427b376da1c24fd11faecbac5a4ac7523c3607f8a01f94c2ec0"
+                "sha256:679e51dd4403591b2d6838a48de3d283f3d188412a9782faadf845f298736ba0",
+                "sha256:ebc15946aa78bd63458992fc81ec3b6f7b1e92d51c35e6de1c3804e73b799147"
             ],
             "markers": "python_version < '3.10'",
-            "version": "==3.16.1"
+            "version": "==3.16.2"
         }
     },
     "develop": {
-        "alabaster": {
-            "hashes": [
-                "sha256:1ee19aca801bbabb5ba3f5f258e4422dfa86f82f3e9cefb0859b283cdd7f62a3",
-                "sha256:a27a4a084d5e690e16e01e03ad2b2e552c61a65469419b907243193de1a84ae2"
-            ],
-            "markers": "python_version >= '3.6'",
-            "version": "==0.7.13"
-        },
         "astroid": {
             "hashes": [
                 "sha256:389656ca57b6108f939cf5d2f9a2a825a3be50ba9d589670f393236e0a03b91c",
                 "sha256:903f024859b7c7687d7a7f3a3f73b17301f8e42dfd9cc9df9d4418172d3e2dbd"
             ],
             "markers": "python_full_version >= '3.7.2'",
             "version": "==2.15.6"
         },
-        "babel": {
-            "hashes": [
-                "sha256:b4246fb7677d3b98f501a39d43396d3cafdc8eadb045f4a31be01863f655c610",
-                "sha256:cc2d99999cd01d44420ae725a21c9e3711b3aadc7976d6147f622d8581963455"
-            ],
-            "markers": "python_version >= '3.7'",
-            "version": "==2.12.1"
-        },
         "certifi": {
             "hashes": [
                 "sha256:0f0d56dc5a6ad56fd4ba36484d6cc34451e1c6548c61daad8c320169f91eddc7",
                 "sha256:c6c2e98f5c7869efca1f8916fed228dd91539f9f1b444c314c06eef02980c716"
             ],
             "markers": "python_version >= '3.6'",
             "version": "==2023.5.7"
@@ -683,18 +667,18 @@
                 "sha256:e5db55f3687856d8fbdab002ed78544e1c4559a130302693d839dfe8f93f2373"
             ],
             "markers": "python_version < '3.11'",
             "version": "==0.3.6"
         },
         "distlib": {
             "hashes": [
-                "sha256:14bad2d9b04d3a36127ac97f30b12a19268f211063d8f8ee4f47108896e11b46",
-                "sha256:f35c4b692542ca110de7ef0bea44d73981caeb34ca0b9b6b2e6d7790dda8f80e"
+                "sha256:2e24928bc811348f0feb63014e97aaae3037f2cf48712d51ae61df7fd6075057",
+                "sha256:9dafe54b34a028eafd95039d5e5d4851a13734540f1331060d31c9916e7147a8"
             ],
-            "version": "==0.3.6"
+            "version": "==0.3.7"
         },
         "docutils": {
             "hashes": [
                 "sha256:96f387a2c5562db4476f09f13bbab2192e764cac08ebbf3a34a95d9b1e4a59d6",
                 "sha256:f08a4e276c3a1583a86dce3e34aba3fe04d02bba2dd51ed16106244e8a923e3b"
             ],
             "markers": "python_version >= '3.7'",
@@ -738,80 +722,72 @@
                 "sha256:7aada352fb0c7f5538c4fafeddf314d3a6a92ee8e2b1de70482329e42de70301"
             ],
             "markers": "python_version >= '3.6'",
             "version": "==3.9.0"
         },
         "fonttools": {
             "hashes": [
-                "sha256:0614b6348866092d00df3dfb37e037fc06412ca67087de361a2777ea5ed62c16",
-                "sha256:06eac087ea55b3ebb2207d93b5ac56c847163899f05f5a77e1910f688fe10030",
-                "sha256:19d461c801b8904d201c6c38a99bfcfef673bfdfe0c7f026f582ef78896434e0",
-                "sha256:381558eafffc1432d08ca58063e71c7376ecaae48e9318354a90a1049a644845",
-                "sha256:3ee75b8ca48f6c48af25e967dce995ef94e46872b35c7d454b983c62c9c7006d",
-                "sha256:415cf7c806a3f56fb280dadcf3c92c85c0415e75665ca957b4a2a2e39c17a5c9",
-                "sha256:465d0f24bf4f75160f441793b55076b7a080a57d3a1f738390af2c20bee24fbb",
-                "sha256:4c654b1facf1f3b742e4d9b2dcdf0fa867b1f007b1b4981cc58a75ef5dca2a3c",
-                "sha256:50f8bdb421270f71b54695c62785e300fab4bb6127be40bf9f3084962a0c3adb",
-                "sha256:5448a87f6ed57ed844b64a05d3792827af584a8584613f6289867f4e77eb603b",
-                "sha256:560ea1a604c927399f36742abf342a4c5f3fee8e8e8a484b774dfe9630bd9a91",
-                "sha256:5b1c2b21b40229166a864f2b0aec06d37f0a204066deb1734c93370e0c76339d",
-                "sha256:69178674505ec81adf4af2a3bbacd0cb9a37ba7831bc3fca307f80e48ab2767b",
-                "sha256:69dbe0154e15b68dd671441ea8f23dad87488b24a6e650d45958f4722819a443",
-                "sha256:6faff25991dec48f8cac882055a09ae1a29fd15bc160bc3d663e789e994664c2",
-                "sha256:72d40a32d6443871ea0d147813caad58394b48729dfa4fbc45dcaac54f9506f2",
-                "sha256:7e22d0144d735f6c7df770509b8c0c33414bf460df0d5dddc98a159e5dbb10eb",
-                "sha256:841c491fa3e9c54e8f9cd5dae059e88f45e086aea090c28be9d42f59c8b99e01",
-                "sha256:86edb95c4d1fe4fae2111d7e0c10c6e42b7790b377bcf1952303469eee5b52bb",
-                "sha256:8f602dd5bcde7e4241419924f23c6f0d66723dd5408a58c3a2f781745c693f45",
-                "sha256:9387b09694fbf8ac7dcf887069068f81fb4124d05e09557ac7daabfbec1744bd",
-                "sha256:b329ae7ce971b5c4148d6cdb8119c0ce4587265b2330d4f2f3776ef851bee020",
-                "sha256:ba2a367ff478cd108d5319c0dc4fd4eb4ea3476dbfc45b00c45718e889cd9463",
-                "sha256:bc9e7b1e268be7a23fc66471b615c324e99c5db39ce8c49dd6dd8e962c7bc1b8",
-                "sha256:c890061915e95b619c1d3cc3c107c6fb021406b701c0c24b03e74830d522f210",
-                "sha256:cc3324e4159e6d1f55c3615b4c1c211f87cc96cc0cc7c946c8447dc1319f2e9d",
-                "sha256:d2dae84a3d0f76884a6102c62f2795b2d6602c2c95cfcce74c8a590b6200e533",
-                "sha256:d45f28c20bb67dee0f4a4caae709f40b0693d764b7b2bf2d58890f36b1bfcef0",
-                "sha256:e38bd91eae257f36c2b7245c0278e9cd9d754f3a66b8d2b548c623ba66e387b6",
-                "sha256:e43f6c7f9ba4f9d29edee530e45f9aa162872ec9549398b85971477a99f2a806",
-                "sha256:ea879afd1d6189fca02a85a7868560c9bb8415dccff6b7ae6d81e4f06b3ab30d",
-                "sha256:eb9dfa87152bd97019adc387b2f29ef6af601de4386f36570ca537ace96d96ed",
-                "sha256:efd59e83223cb77952997fb850c7a7c2a958c9af0642060f536722c2a9e9d53b",
-                "sha256:f3fe90dfb297bd8265238c06787911cd81c2cb89ac5b13e1c911928bdabfce0f"
+                "sha256:1df1b6f4c7c4bc8201eb47f3b268adbf2539943aa43c400f84556557e3e109c0",
+                "sha256:2a22b2c425c698dcd5d6b0ff0b566e8e9663172118db6fd5f1941f9b8063da9b",
+                "sha256:33191f062549e6bb1a4782c22a04ebd37009c09360e2d6686ac5083774d06d95",
+                "sha256:38cdecd8f1fd4bf4daae7fed1b3170dfc1b523388d6664b2204b351820aa78a7",
+                "sha256:3ae64303ba670f8959fdaaa30ba0c2dabe75364fdec1caeee596c45d51ca3425",
+                "sha256:3d1f9471134affc1e3b1b806db6e3e2ad3fa99439e332f1881a474c825101096",
+                "sha256:4e3334d51f0e37e2c6056e67141b2adabc92613a968797e2571ca8a03bd64773",
+                "sha256:4edc795533421e98f60acee7d28fc8d941ff5ac10f44668c9c3635ad72ae9045",
+                "sha256:547ab36a799dded58a46fa647266c24d0ed43a66028cd1cd4370b246ad426cac",
+                "sha256:59eba8b2e749a1de85760da22333f3d17c42b66e03758855a12a2a542723c6e7",
+                "sha256:704bccd69b0abb6fab9f5e4d2b75896afa48b427caa2c7988792a2ffce35b441",
+                "sha256:73ef0bb5d60eb02ba4d3a7d23ada32184bd86007cb2de3657cfcb1175325fc83",
+                "sha256:7763316111df7b5165529f4183a334aa24c13cdb5375ffa1dc8ce309c8bf4e5c",
+                "sha256:849ec722bbf7d3501a0e879e57dec1fc54919d31bff3f690af30bb87970f9784",
+                "sha256:891cfc5a83b0307688f78b9bb446f03a7a1ad981690ac8362f50518bc6153975",
+                "sha256:952cb405f78734cf6466252fec42e206450d1a6715746013f64df9cbd4f896fa",
+                "sha256:a7bbb290d13c6dd718ec2c3db46fe6c5f6811e7ea1e07f145fd8468176398224",
+                "sha256:a9b3cc10dc9e0834b6665fd63ae0c6964c6bc3d7166e9bc84772e0edd09f9fa2",
+                "sha256:aaaef294d8e411f0ecb778a0aefd11bb5884c9b8333cc1011bdaf3b58ca4bd75",
+                "sha256:afce2aeb80be72b4da7dd114f10f04873ff512793d13ce0b19d12b2a4c44c0f0",
+                "sha256:b0938ebbeccf7c80bb9a15e31645cf831572c3a33d5cc69abe436e7000c61b14",
+                "sha256:b2d1ee95be42b80d1f002d1ee0a51d7a435ea90d36f1a5ae331be9962ee5a3f1",
+                "sha256:b927e5f466d99c03e6e20961946314b81d6e3490d95865ef88061144d9f62e38",
+                "sha256:bdd729744ae7ecd7f7311ad25d99da4999003dcfe43b436cf3c333d4e68de73d",
+                "sha256:c2071267deaa6d93cb16288613419679c77220543551cbe61da02c93d92df72f",
+                "sha256:cac73bbef7734e78c60949da11c4903ee5837168e58772371bd42a75872f4f82",
+                "sha256:da2c2964bdc827ba6b8a91dc6de792620be4da3922c4cf0599f36a488c07e2b2",
+                "sha256:e16a9449f21a93909c5be2f5ed5246420f2316e94195dbfccb5238aaa38f9751",
+                "sha256:e5c2b0a95a221838991e2f0e455dec1ca3a8cc9cd54febd68cc64d40fdb83669",
+                "sha256:ec453a45778524f925a8f20fd26a3326f398bfc55d534e37bab470c5e415caa1",
+                "sha256:edee0900cf0eedb29d17c7876102d6e5a91ee333882b1f5abc83e85b934cadb5",
+                "sha256:f14f3ccea4cc7dd1b277385adf3c3bf18f9860f87eab9c2fb650b0af16800f55",
+                "sha256:f240d9adf0583ac8fc1646afe7f4ac039022b6f8fa4f1575a2cfa53675360b69",
+                "sha256:f48602c0b3fd79cd83a34c40af565fe6db7ac9085c8823b552e6e751e3a5b8be"
             ],
             "markers": "python_version >= '3.8'",
-            "version": "==4.41.0"
+            "version": "==4.41.1"
         },
         "heatmap-cli": {
             "editable": true,
             "path": "."
         },
         "identify": {
             "hashes": [
-                "sha256:0aac67d5b4812498056d28a9a512a483f5085cc28640b02b258a59dac34301d4",
-                "sha256:986dbfb38b1140e763e413e6feb44cd731faf72d1909543178aa79b0e258265d"
+                "sha256:9df2489842707d431b38ce3410ef8df40da5b10a3e28a3fcac1a42523e956409",
+                "sha256:db4de0e758c0db8f81996816cd2f3f2f8c5c8d49a7fd02f3b4109aac6fd80e29"
             ],
-            "markers": "python_version >= '3.7'",
-            "version": "==2.5.24"
+            "markers": "python_version >= '3.8'",
+            "version": "==2.5.25"
         },
         "idna": {
             "hashes": [
                 "sha256:814f528e8dead7d329833b91c5faa87d60bf71824cd12a7530b5526063d02cb4",
                 "sha256:90b77e79eaa3eba6de819a0c442c0b4ceefc341a7a2ab77d7562bf49f425c5c2"
             ],
             "markers": "python_version >= '3.5'",
             "version": "==3.4"
         },
-        "imagesize": {
-            "hashes": [
-                "sha256:0d8d18d08f840c19d0ee7ca1fd82490fdc3729b7ac93f49870406ddde8ef8d8b",
-                "sha256:69150444affb9cb0d5cc5a92b3676f0b2fb7cd9ae39e947a5e11a36b4497cd4a"
-            ],
-            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3'",
-            "version": "==1.4.1"
-        },
         "importlib-metadata": {
             "hashes": [
                 "sha256:3ebb78df84a805d7698245025b975d9d67053cd94c79245ba4b3eb694abe68bb",
                 "sha256:dbace7892d8c0c4ac1ad096662232f831d4e64f4c4545bd53016a3e9d4654743"
             ],
             "markers": "python_version < '3.10'",
             "version": "==6.8.0"
@@ -836,22 +812,14 @@
             "hashes": [
                 "sha256:8bef7dde241278824a6d83f44a544709b065191b95b6e50894bdc722fcba0504",
                 "sha256:f84c2818376e66cf843d497486ea8fed8700b340f308f076c6fb1229dff318b6"
             ],
             "markers": "python_full_version >= '3.8.0'",
             "version": "==5.12.0"
         },
-        "jinja2": {
-            "hashes": [
-                "sha256:31351a702a408a9e7595a8fc6150fc3f43bb6bf7e319770cbc0db9df9437e852",
-                "sha256:6088930bfe239f0e6710546ab9c19c9ef35e29792895fed6e6e31a023a182a61"
-            ],
-            "markers": "python_version >= '3.7'",
-            "version": "==3.1.2"
-        },
         "kiwisolver": {
             "hashes": [
                 "sha256:02f79693ec433cb4b5f51694e8477ae83b3205768a6fb48ffba60549080e295b",
                 "sha256:03baab2d6b4a54ddbb43bba1a3a2d1627e82d205c5cf8f4c924dc49284b87166",
                 "sha256:1041feb4cda8708ce73bb4dcb9ce1ccf49d553bf87c3954bdfa46f0c3f77252c",
                 "sha256:10ee06759482c78bdb864f4109886dff7b8a56529bc1609d4f1112b93fe6423c",
                 "sha256:1d1573129aa0fd901076e2bfb4275a35f5b7aa60fbfb984499d661ec950320b0",
@@ -960,78 +928,14 @@
                 "sha256:f12ad7126ae0c98d601a7ee504c1122bcef553d1d5e0c3bfa77b16b3968d2734",
                 "sha256:f2457189d8257dd41ae9b434ba33298aec198e30adf2dcdaaa3a28b9994f6adb",
                 "sha256:f699ac1c768270c9e384e4cbd268d6e67aebcfae6cd623b4d7c3bfde5a35db59"
             ],
             "markers": "python_version >= '3.7'",
             "version": "==1.9.0"
         },
-        "markdown-it-py": {
-            "hashes": [
-                "sha256:355216845c60bd96232cd8d8c40e8f9765cc86f46880e43a8fd22dc1a1a8cab1",
-                "sha256:e3f60a94fa066dc52ec76661e37c851cb232d92f9886b15cb560aaada2df8feb"
-            ],
-            "markers": "python_version >= '3.8'",
-            "version": "==3.0.0"
-        },
-        "markupsafe": {
-            "hashes": [
-                "sha256:05fb21170423db021895e1ea1e1f3ab3adb85d1c2333cbc2310f2a26bc77272e",
-                "sha256:0a4e4a1aff6c7ac4cd55792abf96c915634c2b97e3cc1c7129578aa68ebd754e",
-                "sha256:10bbfe99883db80bdbaff2dcf681dfc6533a614f700da1287707e8a5d78a8431",
-                "sha256:134da1eca9ec0ae528110ccc9e48041e0828d79f24121a1a146161103c76e686",
-                "sha256:1577735524cdad32f9f694208aa75e422adba74f1baee7551620e43a3141f559",
-                "sha256:1b40069d487e7edb2676d3fbdb2b0829ffa2cd63a2ec26c4938b2d34391b4ecc",
-                "sha256:282c2cb35b5b673bbcadb33a585408104df04f14b2d9b01d4c345a3b92861c2c",
-                "sha256:2c1b19b3aaacc6e57b7e25710ff571c24d6c3613a45e905b1fde04d691b98ee0",
-                "sha256:2ef12179d3a291be237280175b542c07a36e7f60718296278d8593d21ca937d4",
-                "sha256:338ae27d6b8745585f87218a3f23f1512dbf52c26c28e322dbe54bcede54ccb9",
-                "sha256:3c0fae6c3be832a0a0473ac912810b2877c8cb9d76ca48de1ed31e1c68386575",
-                "sha256:3fd4abcb888d15a94f32b75d8fd18ee162ca0c064f35b11134be77050296d6ba",
-                "sha256:42de32b22b6b804f42c5d98be4f7e5e977ecdd9ee9b660fda1a3edf03b11792d",
-                "sha256:504b320cd4b7eff6f968eddf81127112db685e81f7e36e75f9f84f0df46041c3",
-                "sha256:525808b8019e36eb524b8c68acdd63a37e75714eac50e988180b169d64480a00",
-                "sha256:56d9f2ecac662ca1611d183feb03a3fa4406469dafe241673d521dd5ae92a155",
-                "sha256:5bbe06f8eeafd38e5d0a4894ffec89378b6c6a625ff57e3028921f8ff59318ac",
-                "sha256:65c1a9bcdadc6c28eecee2c119465aebff8f7a584dd719facdd9e825ec61ab52",
-                "sha256:68e78619a61ecf91e76aa3e6e8e33fc4894a2bebe93410754bd28fce0a8a4f9f",
-                "sha256:69c0f17e9f5a7afdf2cc9fb2d1ce6aabdb3bafb7f38017c0b77862bcec2bbad8",
-                "sha256:6b2b56950d93e41f33b4223ead100ea0fe11f8e6ee5f641eb753ce4b77a7042b",
-                "sha256:787003c0ddb00500e49a10f2844fac87aa6ce977b90b0feaaf9de23c22508b24",
-                "sha256:7ef3cb2ebbf91e330e3bb937efada0edd9003683db6b57bb108c4001f37a02ea",
-                "sha256:8023faf4e01efadfa183e863fefde0046de576c6f14659e8782065bcece22198",
-                "sha256:8758846a7e80910096950b67071243da3e5a20ed2546e6392603c096778d48e0",
-                "sha256:8afafd99945ead6e075b973fefa56379c5b5c53fd8937dad92c662da5d8fd5ee",
-                "sha256:8c41976a29d078bb235fea9b2ecd3da465df42a562910f9022f1a03107bd02be",
-                "sha256:8e254ae696c88d98da6555f5ace2279cf7cd5b3f52be2b5cf97feafe883b58d2",
-                "sha256:9402b03f1a1b4dc4c19845e5c749e3ab82d5078d16a2a4c2cd2df62d57bb0707",
-                "sha256:962f82a3086483f5e5f64dbad880d31038b698494799b097bc59c2edf392fce6",
-                "sha256:9dcdfd0eaf283af041973bff14a2e143b8bd64e069f4c383416ecd79a81aab58",
-                "sha256:aa7bd130efab1c280bed0f45501b7c8795f9fdbeb02e965371bbef3523627779",
-                "sha256:ab4a0df41e7c16a1392727727e7998a467472d0ad65f3ad5e6e765015df08636",
-                "sha256:ad9e82fb8f09ade1c3e1b996a6337afac2b8b9e365f926f5a61aacc71adc5b3c",
-                "sha256:af598ed32d6ae86f1b747b82783958b1a4ab8f617b06fe68795c7f026abbdcad",
-                "sha256:b076b6226fb84157e3f7c971a47ff3a679d837cf338547532ab866c57930dbee",
-                "sha256:b7ff0f54cb4ff66dd38bebd335a38e2c22c41a8ee45aa608efc890ac3e3931bc",
-                "sha256:bfce63a9e7834b12b87c64d6b155fdd9b3b96191b6bd334bf37db7ff1fe457f2",
-                "sha256:c011a4149cfbcf9f03994ec2edffcb8b1dc2d2aede7ca243746df97a5d41ce48",
-                "sha256:c9c804664ebe8f83a211cace637506669e7890fec1b4195b505c214e50dd4eb7",
-                "sha256:ca379055a47383d02a5400cb0d110cef0a776fc644cda797db0c5696cfd7e18e",
-                "sha256:cb0932dc158471523c9637e807d9bfb93e06a95cbf010f1a38b98623b929ef2b",
-                "sha256:cd0f502fe016460680cd20aaa5a76d241d6f35a1c3350c474bac1273803893fa",
-                "sha256:ceb01949af7121f9fc39f7d27f91be8546f3fb112c608bc4029aef0bab86a2a5",
-                "sha256:d080e0a5eb2529460b30190fcfcc4199bd7f827663f858a226a81bc27beaa97e",
-                "sha256:dd15ff04ffd7e05ffcb7fe79f1b98041b8ea30ae9234aed2a9168b5797c3effb",
-                "sha256:df0be2b576a7abbf737b1575f048c23fb1d769f267ec4358296f31c2479db8f9",
-                "sha256:e09031c87a1e51556fdcb46e5bd4f59dfb743061cf93c4d6831bf894f125eb57",
-                "sha256:e4dd52d80b8c83fdce44e12478ad2e85c64ea965e75d66dbeafb0a3e77308fcc",
-                "sha256:fec21693218efe39aa7f8599346e90c705afa52c5b31ae019b2e57e8f6542bb2"
-            ],
-            "markers": "python_version >= '3.7'",
-            "version": "==2.1.3"
-        },
         "matplotlib": {
             "hashes": [
                 "sha256:070f8dddd1f5939e60aacb8fa08f19551f4b0140fab16a3669d5cd6e9cb28fc8",
                 "sha256:0c3cca3e842b11b55b52c6fb8bd6a4088693829acbfcdb3e815fa9b7d5c92c1b",
                 "sha256:0f506a1776ee94f9e131af1ac6efa6e5bc7cb606a3e389b0ccb6e657f60bb676",
                 "sha256:12f01b92ecd518e0697da4d97d163b2b3aa55eb3eb4e2c98235b3396d7dad55f",
                 "sha256:152ee0b569a37630d8628534c628456b28686e085d51394da6b71ef84c4da201",
@@ -1079,38 +983,14 @@
             "hashes": [
                 "sha256:348e0240c33b60bbdf4e523192ef919f28cb2c3d7d5c7794f74009290f236325",
                 "sha256:6c2d30ab6be0e4a46919781807b4f0d834ebdd6c6e3dca0bda5a15f863427b6e"
             ],
             "markers": "python_version >= '3.6'",
             "version": "==0.7.0"
         },
-        "mdit-py-plugins": {
-            "hashes": [
-                "sha256:b51b3bb70691f57f974e257e367107857a93b36f322a9e6d44ca5bf28ec2def9",
-                "sha256:d8ab27e9aed6c38aa716819fedfde15ca275715955f8a185a8e1cf90fb1d2c1b"
-            ],
-            "markers": "python_version >= '3.8'",
-            "version": "==0.4.0"
-        },
-        "mdurl": {
-            "hashes": [
-                "sha256:84008a41e51615a49fc9966191ff91509e3c40b939176e643fd50a5c2196b8f8",
-                "sha256:bb413d29f5eea38f31dd4754dd7377d4465116fb207585f97bf925588687c1ba"
-            ],
-            "markers": "python_version >= '3.7'",
-            "version": "==0.1.2"
-        },
-        "myst-parser": {
-            "hashes": [
-                "sha256:7c36344ae39c8e740dad7fdabf5aa6fc4897a813083c6cc9990044eb93656b14",
-                "sha256:ea929a67a6a0b1683cdbe19b8d2e724cd7643f8aa3e7bb18dd65beac3483bead"
-            ],
-            "index": "pypi",
-            "version": "==2.0.0"
-        },
         "nodeenv": {
             "hashes": [
                 "sha256:d51e0c37e64fbf47d017feac3145cdbb58836d7eee8c6f6d3b6880c5456227d2",
                 "sha256:df865724bb3c3adc86b3876fa209771517b0cfe596beff01a92700e0e8be4cec"
             ],
             "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4, 3.5, 3.6'",
             "version": "==1.8.0"
@@ -1248,19 +1128,19 @@
                 "sha256:faaf07ea35355b01a35cb442dd950d8f1bb5b040a7787791a535de13db15ed90"
             ],
             "markers": "python_version >= '3.8'",
             "version": "==10.0.0"
         },
         "platformdirs": {
             "hashes": [
-                "sha256:cec7b889196b9144d088e4c57d9ceef7374f6c39694ad1577a0aab50d27ea28c",
-                "sha256:f87ca4fcff7d2b0f81c6a748a77973d7af0f4d526f98f308477c3c436c74d528"
+                "sha256:1b42b450ad933e981d56e59f1b97495428c9bd60698baab9f3eb3d00d5822421",
+                "sha256:ad8291ae0ae5072f66c16945166cb11c63394c7a3ad1b1bc9828ca3162da8c2f"
             ],
             "markers": "python_version >= '3.7'",
-            "version": "==3.8.1"
+            "version": "==3.9.1"
         },
         "pluggy": {
             "hashes": [
                 "sha256:c2fd55a7d7a3863cba1a013e4e2414658b1d07b6bc57b3919e0c63c9abb99849",
                 "sha256:d12f0c4b579b15f5e054301bb226ee85eeeba08ffec228092f8defbaa3a4c4b3"
             ],
             "markers": "python_version >= '3.7'",
@@ -1278,22 +1158,14 @@
             "hashes": [
                 "sha256:51c75c4126074b472f746a24399ad32f6053d1b34b68d2fa41e558e6f4a98719",
                 "sha256:607c53218732647dff4acdfcd50cb62615cedf612e72d1724fb1a0cc6405b378"
             ],
             "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4'",
             "version": "==1.11.0"
         },
-        "pygments": {
-            "hashes": [
-                "sha256:8ace4d3c1dd481894b2005f560ead0f9f19ee64fe983366be1a21e171d12775c",
-                "sha256:db2db3deb4b4179f399a09054b023b6a586b76499d36965813c71aa8ed7b5fd1"
-            ],
-            "markers": "python_version >= '3.7'",
-            "version": "==2.15.1"
-        },
         "pylint": {
             "hashes": [
                 "sha256:5dcf1d9e19f41f38e4e85d10f511e5b9c35e1aa74251bf95cdd8cb23584e2db1",
                 "sha256:7a1145fb08c251bdb5cca11739722ce64a63db479283d10ce718b2460e54123c"
             ],
             "index": "pypi",
             "version": "==2.17.4"
@@ -1351,57 +1223,57 @@
                 "sha256:1d8ce29db189191fb55338ee6d0387d82ab59f3d00eac103412d64e0ebd0c588",
                 "sha256:a151b3abb88eda1d4e34a9814df37de2a80e301e68ba0fd856fb9b46bfbbbffb"
             ],
             "version": "==2023.3"
         },
         "pyyaml": {
             "hashes": [
-                "sha256:01b45c0191e6d66c470b6cf1b9531a771a83c1c4208272ead47a3ae4f2f603bf",
-                "sha256:0283c35a6a9fbf047493e3a0ce8d79ef5030852c51e9d911a27badfde0605293",
-                "sha256:055d937d65826939cb044fc8c9b08889e8c743fdc6a32b33e2390f66013e449b",
-                "sha256:07751360502caac1c067a8132d150cf3d61339af5691fe9e87803040dbc5db57",
-                "sha256:0b4624f379dab24d3725ffde76559cff63d9ec94e1736b556dacdfebe5ab6d4b",
-                "sha256:0ce82d761c532fe4ec3f87fc45688bdd3a4c1dc5e0b4a19814b9009a29baefd4",
-                "sha256:1e4747bc279b4f613a09eb64bba2ba602d8a6664c6ce6396a4d0cd413a50ce07",
-                "sha256:213c60cd50106436cc818accf5baa1aba61c0189ff610f64f4a3e8c6726218ba",
-                "sha256:231710d57adfd809ef5d34183b8ed1eeae3f76459c18fb4a0b373ad56bedcdd9",
-                "sha256:277a0ef2981ca40581a47093e9e2d13b3f1fbbeffae064c1d21bfceba2030287",
-                "sha256:2cd5df3de48857ed0544b34e2d40e9fac445930039f3cfe4bcc592a1f836d513",
-                "sha256:40527857252b61eacd1d9af500c3337ba8deb8fc298940291486c465c8b46ec0",
-                "sha256:432557aa2c09802be39460360ddffd48156e30721f5e8d917f01d31694216782",
-                "sha256:473f9edb243cb1935ab5a084eb238d842fb8f404ed2193a915d1784b5a6b5fc0",
-                "sha256:48c346915c114f5fdb3ead70312bd042a953a8ce5c7106d5bfb1a5254e47da92",
-                "sha256:50602afada6d6cbfad699b0c7bb50d5ccffa7e46a3d738092afddc1f9758427f",
-                "sha256:68fb519c14306fec9720a2a5b45bc9f0c8d1b9c72adf45c37baedfcd949c35a2",
-                "sha256:77f396e6ef4c73fdc33a9157446466f1cff553d979bd00ecb64385760c6babdc",
-                "sha256:81957921f441d50af23654aa6c5e5eaf9b06aba7f0a19c18a538dc7ef291c5a1",
-                "sha256:819b3830a1543db06c4d4b865e70ded25be52a2e0631ccd2f6a47a2822f2fd7c",
-                "sha256:897b80890765f037df3403d22bab41627ca8811ae55e9a722fd0392850ec4d86",
-                "sha256:98c4d36e99714e55cfbaaee6dd5badbc9a1ec339ebfc3b1f52e293aee6bb71a4",
-                "sha256:9df7ed3b3d2e0ecfe09e14741b857df43adb5a3ddadc919a2d94fbdf78fea53c",
-                "sha256:9fa600030013c4de8165339db93d182b9431076eb98eb40ee068700c9c813e34",
-                "sha256:a80a78046a72361de73f8f395f1f1e49f956c6be882eed58505a15f3e430962b",
-                "sha256:afa17f5bc4d1b10afd4466fd3a44dc0e245382deca5b3c353d8b757f9e3ecb8d",
-                "sha256:b3d267842bf12586ba6c734f89d1f5b871df0273157918b0ccefa29deb05c21c",
-                "sha256:b5b9eccad747aabaaffbc6064800670f0c297e52c12754eb1d976c57e4f74dcb",
-                "sha256:bfaef573a63ba8923503d27530362590ff4f576c626d86a9fed95822a8255fd7",
-                "sha256:c5687b8d43cf58545ade1fe3e055f70eac7a5a1a0bf42824308d868289a95737",
-                "sha256:cba8c411ef271aa037d7357a2bc8f9ee8b58b9965831d9e51baf703280dc73d3",
-                "sha256:d15a181d1ecd0d4270dc32edb46f7cb7733c7c508857278d3d378d14d606db2d",
-                "sha256:d4b0ba9512519522b118090257be113b9468d804b19d63c71dbcf4a48fa32358",
-                "sha256:d4db7c7aef085872ef65a8fd7d6d09a14ae91f691dec3e87ee5ee0539d516f53",
-                "sha256:d4eccecf9adf6fbcc6861a38015c2a64f38b9d94838ac1810a9023a0609e1b78",
-                "sha256:d67d839ede4ed1b28a4e8909735fc992a923cdb84e618544973d7dfc71540803",
-                "sha256:daf496c58a8c52083df09b80c860005194014c3698698d1a57cbcfa182142a3a",
-                "sha256:dbad0e9d368bb989f4515da330b88a057617d16b6a8245084f1b05400f24609f",
-                "sha256:e61ceaab6f49fb8bdfaa0f92c4b57bcfbea54c09277b1b4f7ac376bfb7a7c174",
-                "sha256:f84fbc98b019fef2ee9a1cb3ce93e3187a6df0b2538a651bfb890254ba9f90b5"
+                "sha256:062582fca9fabdd2c8b54a3ef1c978d786e0f6b3a1510e0ac93ef59e0ddae2bc",
+                "sha256:1635fd110e8d85d55237ab316b5b011de701ea0f29d07611174a1b42f1444741",
+                "sha256:184c5108a2aca3c5b3d3bf9395d50893a7ab82a38004c8f61c258d4428e80206",
+                "sha256:18aeb1bf9a78867dc38b259769503436b7c72f7a1f1f4c93ff9a17de54319b27",
+                "sha256:1d4c7e777c441b20e32f52bd377e0c409713e8bb1386e1099c2415f26e479595",
+                "sha256:1e2722cc9fbb45d9b87631ac70924c11d3a401b2d7f410cc0e3bbf249f2dca62",
+                "sha256:1fe35611261b29bd1de0070f0b2f47cb6ff71fa6595c077e42bd0c419fa27b98",
+                "sha256:28c119d996beec18c05208a8bd78cbe4007878c6dd15091efb73a30e90539696",
+                "sha256:42f8152b8dbc4fe7d96729ec2b99c7097d656dc1213a3229ca5383f973a5ed6d",
+                "sha256:4fb147e7a67ef577a588a0e2c17b6db51dda102c71de36f8549b6816a96e1867",
+                "sha256:50550eb667afee136e9a77d6dc71ae76a44df8b3e51e41b77f6de2932bfe0f47",
+                "sha256:510c9deebc5c0225e8c96813043e62b680ba2f9c50a08d3724c7f28a747d1486",
+                "sha256:5773183b6446b2c99bb77e77595dd486303b4faab2b086e7b17bc6bef28865f6",
+                "sha256:596106435fa6ad000c2991a98fa58eeb8656ef2325d7e158344fb33864ed87e3",
+                "sha256:6965a7bc3cf88e5a1c3bd2e0b5c22f8d677dc88a455344035f03399034eb3007",
+                "sha256:69b023b2b4daa7548bcfbd4aa3da05b3a74b772db9e23b982788168117739938",
+                "sha256:704219a11b772aea0d8ecd7058d0082713c3562b4e271b849ad7dc4a5c90c13c",
+                "sha256:7e07cbde391ba96ab58e532ff4803f79c4129397514e1413a7dc761ccd755735",
+                "sha256:81e0b275a9ecc9c0c0c07b4b90ba548307583c125f54d5b6946cfee6360c733d",
+                "sha256:9046c58c4395dff28dd494285c82ba00b546adfc7ef001486fbf0324bc174fba",
+                "sha256:9eb6caa9a297fc2c2fb8862bc5370d0303ddba53ba97e71f08023b6cd73d16a8",
+                "sha256:a0cd17c15d3bb3fa06978b4e8958dcdc6e0174ccea823003a106c7d4d7899ac5",
+                "sha256:afd7e57eddb1a54f0f1a974bc4391af8bcce0b444685d936840f125cf046d5bd",
+                "sha256:b1275ad35a5d18c62a7220633c913e1b42d44b46ee12554e5fd39c70a243d6a3",
+                "sha256:b786eecbdf8499b9ca1d697215862083bd6d2a99965554781d0d8d1ad31e13a0",
+                "sha256:ba336e390cd8e4d1739f42dfe9bb83a3cc2e80f567d8805e11b46f4a943f5515",
+                "sha256:baa90d3f661d43131ca170712d903e6295d1f7a0f595074f151c0aed377c9b9c",
+                "sha256:bc1bf2925a1ecd43da378f4db9e4f799775d6367bdb94671027b73b393a7c42c",
+                "sha256:bd4af7373a854424dabd882decdc5579653d7868b8fb26dc7d0e99f823aa5924",
+                "sha256:bf07ee2fef7014951eeb99f56f39c9bb4af143d8aa3c21b1677805985307da34",
+                "sha256:bfdf460b1736c775f2ba9f6a92bca30bc2095067b8a9d77876d1fad6cc3b4a43",
+                "sha256:c8098ddcc2a85b61647b2590f825f3db38891662cfc2fc776415143f599bb859",
+                "sha256:d2b04aac4d386b172d5b9692e2d2da8de7bfb6c387fa4f801fbf6fb2e6ba4673",
+                "sha256:d858aa552c999bc8a8d57426ed01e40bef403cd8ccdd0fc5f6f04a00414cac2a",
+                "sha256:f003ed9ad21d6a4713f0a9b5a7a0a79e08dd0f221aff4525a2be4c346ee60aab",
+                "sha256:f22ac1c3cac4dbc50079e965eba2c1058622631e526bd9afd45fedd49ba781fa",
+                "sha256:faca3bdcf85b2fc05d06ff3fbc1f83e1391b3e724afa3feba7d13eeab355484c",
+                "sha256:fca0e3a251908a499833aa292323f32437106001d436eca0e6e7833256674585",
+                "sha256:fd1592b3fdf65fff2ad0004b5e363300ef59ced41c2e6b3a99d4089fa8c5435d",
+                "sha256:fd66fc5d0da6d9815ba2cebeb4205f95818ff4b79c3ebe268e75d961704af52f"
             ],
             "markers": "python_version >= '3.6'",
-            "version": "==6.0"
+            "version": "==6.0.1"
         },
         "requests": {
             "hashes": [
                 "sha256:58cd2187c01e70e6e26505bca751777aa9f2ee0b7f4300988b709f44e013003f",
                 "sha256:942c5a758f98d790eaed1a29cb6eefc7ffb0d1cf7af05c3d2791656dbd6ad1e1"
             ],
             "markers": "python_version >= '3.7'",
@@ -1427,93 +1299,14 @@
             "hashes": [
                 "sha256:1e61c37477a1626458e36f7b1d82aa5c9b094fa4802892072e49de9c60c4c926",
                 "sha256:8abb2f1d86890a2dfb989f9a77cfcfd3e47c2a354b01111771326f8aa26e0254"
             ],
             "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3'",
             "version": "==1.16.0"
         },
-        "snowballstemmer": {
-            "hashes": [
-                "sha256:09b16deb8547d3412ad7b590689584cd0fe25ec8db3be37788be3810cbf19cb1",
-                "sha256:c8e1716e83cc398ae16824e5572ae04e0d9fc2c6b985fb0f900f5f0c96ecba1a"
-            ],
-            "version": "==2.2.0"
-        },
-        "sphinx": {
-            "hashes": [
-                "sha256:60c5e04756c1709a98845ed27a2eed7a556af3993afb66e77fec48189f742616",
-                "sha256:61e025f788c5977d9412587e733733a289e2b9fdc2fef8868ddfbfc4ccfe881d"
-            ],
-            "index": "pypi",
-            "version": "==7.0.1"
-        },
-        "sphinx-autodoc-typehints": {
-            "hashes": [
-                "sha256:8fb8dfc4b010505c850f4ef395fc80222ebfd8fd1b40149f8862f2396f623760",
-                "sha256:ec913d93e915b4dae6a8758cd95baecc70ed77fcdfe050601fc6b12afd0fc059"
-            ],
-            "index": "pypi",
-            "version": "==1.23.3"
-        },
-        "sphinx-copybutton": {
-            "hashes": [
-                "sha256:4cf17c82fb9646d1bc9ca92ac280813a3b605d8c421225fd9913154103ee1fbd",
-                "sha256:fb543fd386d917746c9a2c50360c7905b605726b9355cd26e9974857afeae06e"
-            ],
-            "index": "pypi",
-            "version": "==0.5.2"
-        },
-        "sphinxcontrib-applehelp": {
-            "hashes": [
-                "sha256:29d341f67fb0f6f586b23ad80e072c8e6ad0b48417db2bde114a4c9746feb228",
-                "sha256:828f867945bbe39817c210a1abfd1bc4895c8b73fcaade56d45357a348a07d7e"
-            ],
-            "markers": "python_version >= '3.8'",
-            "version": "==1.0.4"
-        },
-        "sphinxcontrib-devhelp": {
-            "hashes": [
-                "sha256:8165223f9a335cc1af7ffe1ed31d2871f325254c0423bc0c4c7cd1c1e4734a2e",
-                "sha256:ff7f1afa7b9642e7060379360a67e9c41e8f3121f2ce9164266f61b9f4b338e4"
-            ],
-            "markers": "python_version >= '3.5'",
-            "version": "==1.0.2"
-        },
-        "sphinxcontrib-htmlhelp": {
-            "hashes": [
-                "sha256:0cbdd302815330058422b98a113195c9249825d681e18f11e8b1f78a2f11efff",
-                "sha256:c38cb46dccf316c79de6e5515e1770414b797162b23cd3d06e67020e1d2a6903"
-            ],
-            "markers": "python_version >= '3.8'",
-            "version": "==2.0.1"
-        },
-        "sphinxcontrib-jsmath": {
-            "hashes": [
-                "sha256:2ec2eaebfb78f3f2078e73666b1415417a116cc848b72e5172e596c871103178",
-                "sha256:a9925e4a4587247ed2191a22df5f6970656cb8ca2bd6284309578f2153e0c4b8"
-            ],
-            "markers": "python_version >= '3.5'",
-            "version": "==1.0.1"
-        },
-        "sphinxcontrib-qthelp": {
-            "hashes": [
-                "sha256:4c33767ee058b70dba89a6fc5c1892c0d57a54be67ddd3e7875a18d14cba5a72",
-                "sha256:bd9fc24bcb748a8d51fd4ecaade681350aa63009a347a8c14e637895444dfab6"
-            ],
-            "markers": "python_version >= '3.5'",
-            "version": "==1.0.3"
-        },
-        "sphinxcontrib-serializinghtml": {
-            "hashes": [
-                "sha256:352a9a00ae864471d3a7ead8d7d79f5fc0b57e8b3f95e9867eb9eb28999b92fd",
-                "sha256:aa5f6de5dfdf809ef505c4895e51ef5c9eac17d0f287933eb49ec495280b6952"
-            ],
-            "markers": "python_version >= '3.5'",
-            "version": "==1.1.5"
-        },
         "tomli": {
             "hashes": [
                 "sha256:939de3e7a6161af0c887ef91b7d41a53e7c5a1ca976325f429cb46ea9bc30ecc",
                 "sha256:de526c12914f0c550d15924c62d72abc48d6fe7364aa87328337a31007fe8a4f"
             ],
             "markers": "python_version < '3.11'",
             "version": "==2.0.1"
@@ -1564,27 +1357,27 @@
                 "sha256:7e65763eef3120314099b6939b5546db7adce1e7d6f2e179e3df563c70511eda"
             ],
             "markers": "python_version >= '2'",
             "version": "==2023.3"
         },
         "urllib3": {
             "hashes": [
-                "sha256:48e7fafa40319d358848e1bc6809b208340fafe2096f1725d05d67443d0483d1",
-                "sha256:bee28b5e56addb8226c96f7f13ac28cb4c301dd5ea8a6ca179c0b9835e032825"
+                "sha256:8d22f86aae8ef5e410d4f539fde9ce6b2113a001bb4d189e0aed70642d602b11",
+                "sha256:de7df1803967d2c2a98e4b11bb7d6bd9210474c46e8a0401514e3a42a75ebde4"
             ],
             "markers": "python_version >= '3.7'",
-            "version": "==2.0.3"
+            "version": "==2.0.4"
         },
         "virtualenv": {
             "hashes": [
-                "sha256:34da10f14fea9be20e0fd7f04aba9732f84e593dac291b757ce42e3368a39419",
-                "sha256:8ff19a38c1021c742148edc4f81cb43d7f8c6816d2ede2ab72af5b84c749ade1"
+                "sha256:01aacf8decd346cf9a865ae85c0cdc7f64c8caa07ff0d8b1dfc1733d10677442",
+                "sha256:2ef6a237c31629da6442b0bcaa3999748108c7166318d1f55cc9f8d7294e97bd"
             ],
             "markers": "python_version >= '3.7'",
-            "version": "==20.23.1"
+            "version": "==20.24.1"
         },
         "wrapt": {
             "hashes": [
                 "sha256:02fce1852f755f44f95af51f69d22e45080102e9d00258053b79367d07af39c0",
                 "sha256:077ff0d1f9d9e4ce6476c1a924a3332452c1406e59d90a2cf24aeb29eeac9420",
                 "sha256:078e2a1a86544e644a68422f881c48b84fef6d18f8c7a957ffd3f2e0a74a0d4a",
                 "sha256:0970ddb69bba00670e58955f8019bec4a42d1785db3faa043c33d81de2bf843c",
@@ -1661,15 +1454,422 @@
                 "sha256:fd69666217b62fa5d7c6aa88e507493a34dec4fa20c5bd925e4bc12fce586639"
             ],
             "markers": "python_version < '3.11'",
             "version": "==1.15.0"
         },
         "zipp": {
             "hashes": [
-                "sha256:0b37c326d826d5ca35f2b9685cd750292740774ef16190008b00a0227c256fe0",
-                "sha256:857b158da2cbf427b376da1c24fd11faecbac5a4ac7523c3607f8a01f94c2ec0"
+                "sha256:679e51dd4403591b2d6838a48de3d283f3d188412a9782faadf845f298736ba0",
+                "sha256:ebc15946aa78bd63458992fc81ec3b6f7b1e92d51c35e6de1c3804e73b799147"
+            ],
+            "markers": "python_version < '3.10'",
+            "version": "==3.16.2"
+        }
+    },
+    "doc": {
+        "alabaster": {
+            "hashes": [
+                "sha256:1ee19aca801bbabb5ba3f5f258e4422dfa86f82f3e9cefb0859b283cdd7f62a3",
+                "sha256:a27a4a084d5e690e16e01e03ad2b2e552c61a65469419b907243193de1a84ae2"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==0.7.13"
+        },
+        "babel": {
+            "hashes": [
+                "sha256:b4246fb7677d3b98f501a39d43396d3cafdc8eadb045f4a31be01863f655c610",
+                "sha256:cc2d99999cd01d44420ae725a21c9e3711b3aadc7976d6147f622d8581963455"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.12.1"
+        },
+        "certifi": {
+            "hashes": [
+                "sha256:0f0d56dc5a6ad56fd4ba36484d6cc34451e1c6548c61daad8c320169f91eddc7",
+                "sha256:c6c2e98f5c7869efca1f8916fed228dd91539f9f1b444c314c06eef02980c716"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==2023.5.7"
+        },
+        "charset-normalizer": {
+            "hashes": [
+                "sha256:04e57ab9fbf9607b77f7d057974694b4f6b142da9ed4a199859d9d4d5c63fe96",
+                "sha256:09393e1b2a9461950b1c9a45d5fd251dc7c6f228acab64da1c9c0165d9c7765c",
+                "sha256:0b87549028f680ca955556e3bd57013ab47474c3124dc069faa0b6545b6c9710",
+                "sha256:1000fba1057b92a65daec275aec30586c3de2401ccdcd41f8a5c1e2c87078706",
+                "sha256:1249cbbf3d3b04902ff081ffbb33ce3377fa6e4c7356f759f3cd076cc138d020",
+                "sha256:1920d4ff15ce893210c1f0c0e9d19bfbecb7983c76b33f046c13a8ffbd570252",
+                "sha256:193cbc708ea3aca45e7221ae58f0fd63f933753a9bfb498a3b474878f12caaad",
+                "sha256:1a100c6d595a7f316f1b6f01d20815d916e75ff98c27a01ae817439ea7726329",
+                "sha256:1f30b48dd7fa1474554b0b0f3fdfdd4c13b5c737a3c6284d3cdc424ec0ffff3a",
+                "sha256:203f0c8871d5a7987be20c72442488a0b8cfd0f43b7973771640fc593f56321f",
+                "sha256:246de67b99b6851627d945db38147d1b209a899311b1305dd84916f2b88526c6",
+                "sha256:2dee8e57f052ef5353cf608e0b4c871aee320dd1b87d351c28764fc0ca55f9f4",
+                "sha256:2efb1bd13885392adfda4614c33d3b68dee4921fd0ac1d3988f8cbb7d589e72a",
+                "sha256:2f4ac36d8e2b4cc1aa71df3dd84ff8efbe3bfb97ac41242fbcfc053c67434f46",
+                "sha256:3170c9399da12c9dc66366e9d14da8bf7147e1e9d9ea566067bbce7bb74bd9c2",
+                "sha256:3b1613dd5aee995ec6d4c69f00378bbd07614702a315a2cf6c1d21461fe17c23",
+                "sha256:3bb3d25a8e6c0aedd251753a79ae98a093c7e7b471faa3aa9a93a81431987ace",
+                "sha256:3bb7fda7260735efe66d5107fb7e6af6a7c04c7fce9b2514e04b7a74b06bf5dd",
+                "sha256:41b25eaa7d15909cf3ac4c96088c1f266a9a93ec44f87f1d13d4a0e86c81b982",
+                "sha256:45de3f87179c1823e6d9e32156fb14c1927fcc9aba21433f088fdfb555b77c10",
+                "sha256:46fb8c61d794b78ec7134a715a3e564aafc8f6b5e338417cb19fe9f57a5a9bf2",
+                "sha256:48021783bdf96e3d6de03a6e39a1171ed5bd7e8bb93fc84cc649d11490f87cea",
+                "sha256:4957669ef390f0e6719db3613ab3a7631e68424604a7b448f079bee145da6e09",
+                "sha256:5e86d77b090dbddbe78867a0275cb4df08ea195e660f1f7f13435a4649e954e5",
+                "sha256:6339d047dab2780cc6220f46306628e04d9750f02f983ddb37439ca47ced7149",
+                "sha256:681eb3d7e02e3c3655d1b16059fbfb605ac464c834a0c629048a30fad2b27489",
+                "sha256:6c409c0deba34f147f77efaa67b8e4bb83d2f11c8806405f76397ae5b8c0d1c9",
+                "sha256:7095f6fbfaa55defb6b733cfeb14efaae7a29f0b59d8cf213be4e7ca0b857b80",
+                "sha256:70c610f6cbe4b9fce272c407dd9d07e33e6bf7b4aa1b7ffb6f6ded8e634e3592",
+                "sha256:72814c01533f51d68702802d74f77ea026b5ec52793c791e2da806a3844a46c3",
+                "sha256:7a4826ad2bd6b07ca615c74ab91f32f6c96d08f6fcc3902ceeedaec8cdc3bcd6",
+                "sha256:7c70087bfee18a42b4040bb9ec1ca15a08242cf5867c58726530bdf3945672ed",
+                "sha256:855eafa5d5a2034b4621c74925d89c5efef61418570e5ef9b37717d9c796419c",
+                "sha256:8700f06d0ce6f128de3ccdbc1acaea1ee264d2caa9ca05daaf492fde7c2a7200",
+                "sha256:89f1b185a01fe560bc8ae5f619e924407efca2191b56ce749ec84982fc59a32a",
+                "sha256:8b2c760cfc7042b27ebdb4a43a4453bd829a5742503599144d54a032c5dc7e9e",
+                "sha256:8c2f5e83493748286002f9369f3e6607c565a6a90425a3a1fef5ae32a36d749d",
+                "sha256:8e098148dd37b4ce3baca71fb394c81dc5d9c7728c95df695d2dca218edf40e6",
+                "sha256:94aea8eff76ee6d1cdacb07dd2123a68283cb5569e0250feab1240058f53b623",
+                "sha256:95eb302ff792e12aba9a8b8f8474ab229a83c103d74a750ec0bd1c1eea32e669",
+                "sha256:9bd9b3b31adcb054116447ea22caa61a285d92e94d710aa5ec97992ff5eb7cf3",
+                "sha256:9e608aafdb55eb9f255034709e20d5a83b6d60c054df0802fa9c9883d0a937aa",
+                "sha256:a103b3a7069b62f5d4890ae1b8f0597618f628b286b03d4bc9195230b154bfa9",
+                "sha256:a386ebe437176aab38c041de1260cd3ea459c6ce5263594399880bbc398225b2",
+                "sha256:a38856a971c602f98472050165cea2cdc97709240373041b69030be15047691f",
+                "sha256:a401b4598e5d3f4a9a811f3daf42ee2291790c7f9d74b18d75d6e21dda98a1a1",
+                "sha256:a7647ebdfb9682b7bb97e2a5e7cb6ae735b1c25008a70b906aecca294ee96cf4",
+                "sha256:aaf63899c94de41fe3cf934601b0f7ccb6b428c6e4eeb80da72c58eab077b19a",
+                "sha256:b0dac0ff919ba34d4df1b6131f59ce95b08b9065233446be7e459f95554c0dc8",
+                "sha256:baacc6aee0b2ef6f3d308e197b5d7a81c0e70b06beae1f1fcacffdbd124fe0e3",
+                "sha256:bf420121d4c8dce6b889f0e8e4ec0ca34b7f40186203f06a946fa0276ba54029",
+                "sha256:c04a46716adde8d927adb9457bbe39cf473e1e2c2f5d0a16ceb837e5d841ad4f",
+                "sha256:c0b21078a4b56965e2b12f247467b234734491897e99c1d51cee628da9786959",
+                "sha256:c1c76a1743432b4b60ab3358c937a3fe1341c828ae6194108a94c69028247f22",
+                "sha256:c4983bf937209c57240cff65906b18bb35e64ae872da6a0db937d7b4af845dd7",
+                "sha256:c4fb39a81950ec280984b3a44f5bd12819953dc5fa3a7e6fa7a80db5ee853952",
+                "sha256:c57921cda3a80d0f2b8aec7e25c8aa14479ea92b5b51b6876d975d925a2ea346",
+                "sha256:c8063cf17b19661471ecbdb3df1c84f24ad2e389e326ccaf89e3fb2484d8dd7e",
+                "sha256:ccd16eb18a849fd8dcb23e23380e2f0a354e8daa0c984b8a732d9cfaba3a776d",
+                "sha256:cd6dbe0238f7743d0efe563ab46294f54f9bc8f4b9bcf57c3c666cc5bc9d1299",
+                "sha256:d62e51710986674142526ab9f78663ca2b0726066ae26b78b22e0f5e571238dd",
+                "sha256:db901e2ac34c931d73054d9797383d0f8009991e723dab15109740a63e7f902a",
+                "sha256:e03b8895a6990c9ab2cdcd0f2fe44088ca1c65ae592b8f795c3294af00a461c3",
+                "sha256:e1c8a2f4c69e08e89632defbfabec2feb8a8d99edc9f89ce33c4b9e36ab63037",
+                "sha256:e4b749b9cc6ee664a3300bb3a273c1ca8068c46be705b6c31cf5d276f8628a94",
+                "sha256:e6a5bf2cba5ae1bb80b154ed68a3cfa2fa00fde979a7f50d6598d3e17d9ac20c",
+                "sha256:e857a2232ba53ae940d3456f7533ce6ca98b81917d47adc3c7fd55dad8fab858",
+                "sha256:ee4006268ed33370957f55bf2e6f4d263eaf4dc3cfc473d1d90baff6ed36ce4a",
+                "sha256:eef9df1eefada2c09a5e7a40991b9fc6ac6ef20b1372abd48d2794a316dc0449",
+                "sha256:f058f6963fd82eb143c692cecdc89e075fa0828db2e5b291070485390b2f1c9c",
+                "sha256:f25c229a6ba38a35ae6e25ca1264621cc25d4d38dca2942a7fce0b67a4efe918",
+                "sha256:f2a1d0fd4242bd8643ce6f98927cf9c04540af6efa92323e9d3124f57727bfc1",
+                "sha256:f7560358a6811e52e9c4d142d497f1a6e10103d3a6881f18d04dbce3729c0e2c",
+                "sha256:f779d3ad205f108d14e99bb3859aa7dd8e9c68874617c72354d7ecaec2a054ac",
+                "sha256:f87f746ee241d30d6ed93969de31e5ffd09a2961a051e60ae6bddde9ec3583aa"
+            ],
+            "markers": "python_full_version >= '3.7.0'",
+            "version": "==3.2.0"
+        },
+        "docutils": {
+            "hashes": [
+                "sha256:96f387a2c5562db4476f09f13bbab2192e764cac08ebbf3a34a95d9b1e4a59d6",
+                "sha256:f08a4e276c3a1583a86dce3e34aba3fe04d02bba2dd51ed16106244e8a923e3b"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==0.20.1"
+        },
+        "idna": {
+            "hashes": [
+                "sha256:814f528e8dead7d329833b91c5faa87d60bf71824cd12a7530b5526063d02cb4",
+                "sha256:90b77e79eaa3eba6de819a0c442c0b4ceefc341a7a2ab77d7562bf49f425c5c2"
+            ],
+            "markers": "python_version >= '3.5'",
+            "version": "==3.4"
+        },
+        "imagesize": {
+            "hashes": [
+                "sha256:0d8d18d08f840c19d0ee7ca1fd82490fdc3729b7ac93f49870406ddde8ef8d8b",
+                "sha256:69150444affb9cb0d5cc5a92b3676f0b2fb7cd9ae39e947a5e11a36b4497cd4a"
+            ],
+            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3'",
+            "version": "==1.4.1"
+        },
+        "importlib-metadata": {
+            "hashes": [
+                "sha256:3ebb78df84a805d7698245025b975d9d67053cd94c79245ba4b3eb694abe68bb",
+                "sha256:dbace7892d8c0c4ac1ad096662232f831d4e64f4c4545bd53016a3e9d4654743"
+            ],
+            "markers": "python_version < '3.10'",
+            "version": "==6.8.0"
+        },
+        "jinja2": {
+            "hashes": [
+                "sha256:31351a702a408a9e7595a8fc6150fc3f43bb6bf7e319770cbc0db9df9437e852",
+                "sha256:6088930bfe239f0e6710546ab9c19c9ef35e29792895fed6e6e31a023a182a61"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==3.1.2"
+        },
+        "markdown-it-py": {
+            "hashes": [
+                "sha256:355216845c60bd96232cd8d8c40e8f9765cc86f46880e43a8fd22dc1a1a8cab1",
+                "sha256:e3f60a94fa066dc52ec76661e37c851cb232d92f9886b15cb560aaada2df8feb"
+            ],
+            "markers": "python_version >= '3.8'",
+            "version": "==3.0.0"
+        },
+        "markupsafe": {
+            "hashes": [
+                "sha256:05fb21170423db021895e1ea1e1f3ab3adb85d1c2333cbc2310f2a26bc77272e",
+                "sha256:0a4e4a1aff6c7ac4cd55792abf96c915634c2b97e3cc1c7129578aa68ebd754e",
+                "sha256:10bbfe99883db80bdbaff2dcf681dfc6533a614f700da1287707e8a5d78a8431",
+                "sha256:134da1eca9ec0ae528110ccc9e48041e0828d79f24121a1a146161103c76e686",
+                "sha256:1577735524cdad32f9f694208aa75e422adba74f1baee7551620e43a3141f559",
+                "sha256:1b40069d487e7edb2676d3fbdb2b0829ffa2cd63a2ec26c4938b2d34391b4ecc",
+                "sha256:282c2cb35b5b673bbcadb33a585408104df04f14b2d9b01d4c345a3b92861c2c",
+                "sha256:2c1b19b3aaacc6e57b7e25710ff571c24d6c3613a45e905b1fde04d691b98ee0",
+                "sha256:2ef12179d3a291be237280175b542c07a36e7f60718296278d8593d21ca937d4",
+                "sha256:338ae27d6b8745585f87218a3f23f1512dbf52c26c28e322dbe54bcede54ccb9",
+                "sha256:3c0fae6c3be832a0a0473ac912810b2877c8cb9d76ca48de1ed31e1c68386575",
+                "sha256:3fd4abcb888d15a94f32b75d8fd18ee162ca0c064f35b11134be77050296d6ba",
+                "sha256:42de32b22b6b804f42c5d98be4f7e5e977ecdd9ee9b660fda1a3edf03b11792d",
+                "sha256:504b320cd4b7eff6f968eddf81127112db685e81f7e36e75f9f84f0df46041c3",
+                "sha256:525808b8019e36eb524b8c68acdd63a37e75714eac50e988180b169d64480a00",
+                "sha256:56d9f2ecac662ca1611d183feb03a3fa4406469dafe241673d521dd5ae92a155",
+                "sha256:5bbe06f8eeafd38e5d0a4894ffec89378b6c6a625ff57e3028921f8ff59318ac",
+                "sha256:65c1a9bcdadc6c28eecee2c119465aebff8f7a584dd719facdd9e825ec61ab52",
+                "sha256:68e78619a61ecf91e76aa3e6e8e33fc4894a2bebe93410754bd28fce0a8a4f9f",
+                "sha256:69c0f17e9f5a7afdf2cc9fb2d1ce6aabdb3bafb7f38017c0b77862bcec2bbad8",
+                "sha256:6b2b56950d93e41f33b4223ead100ea0fe11f8e6ee5f641eb753ce4b77a7042b",
+                "sha256:787003c0ddb00500e49a10f2844fac87aa6ce977b90b0feaaf9de23c22508b24",
+                "sha256:7ef3cb2ebbf91e330e3bb937efada0edd9003683db6b57bb108c4001f37a02ea",
+                "sha256:8023faf4e01efadfa183e863fefde0046de576c6f14659e8782065bcece22198",
+                "sha256:8758846a7e80910096950b67071243da3e5a20ed2546e6392603c096778d48e0",
+                "sha256:8afafd99945ead6e075b973fefa56379c5b5c53fd8937dad92c662da5d8fd5ee",
+                "sha256:8c41976a29d078bb235fea9b2ecd3da465df42a562910f9022f1a03107bd02be",
+                "sha256:8e254ae696c88d98da6555f5ace2279cf7cd5b3f52be2b5cf97feafe883b58d2",
+                "sha256:9402b03f1a1b4dc4c19845e5c749e3ab82d5078d16a2a4c2cd2df62d57bb0707",
+                "sha256:962f82a3086483f5e5f64dbad880d31038b698494799b097bc59c2edf392fce6",
+                "sha256:9dcdfd0eaf283af041973bff14a2e143b8bd64e069f4c383416ecd79a81aab58",
+                "sha256:aa7bd130efab1c280bed0f45501b7c8795f9fdbeb02e965371bbef3523627779",
+                "sha256:ab4a0df41e7c16a1392727727e7998a467472d0ad65f3ad5e6e765015df08636",
+                "sha256:ad9e82fb8f09ade1c3e1b996a6337afac2b8b9e365f926f5a61aacc71adc5b3c",
+                "sha256:af598ed32d6ae86f1b747b82783958b1a4ab8f617b06fe68795c7f026abbdcad",
+                "sha256:b076b6226fb84157e3f7c971a47ff3a679d837cf338547532ab866c57930dbee",
+                "sha256:b7ff0f54cb4ff66dd38bebd335a38e2c22c41a8ee45aa608efc890ac3e3931bc",
+                "sha256:bfce63a9e7834b12b87c64d6b155fdd9b3b96191b6bd334bf37db7ff1fe457f2",
+                "sha256:c011a4149cfbcf9f03994ec2edffcb8b1dc2d2aede7ca243746df97a5d41ce48",
+                "sha256:c9c804664ebe8f83a211cace637506669e7890fec1b4195b505c214e50dd4eb7",
+                "sha256:ca379055a47383d02a5400cb0d110cef0a776fc644cda797db0c5696cfd7e18e",
+                "sha256:cb0932dc158471523c9637e807d9bfb93e06a95cbf010f1a38b98623b929ef2b",
+                "sha256:cd0f502fe016460680cd20aaa5a76d241d6f35a1c3350c474bac1273803893fa",
+                "sha256:ceb01949af7121f9fc39f7d27f91be8546f3fb112c608bc4029aef0bab86a2a5",
+                "sha256:d080e0a5eb2529460b30190fcfcc4199bd7f827663f858a226a81bc27beaa97e",
+                "sha256:dd15ff04ffd7e05ffcb7fe79f1b98041b8ea30ae9234aed2a9168b5797c3effb",
+                "sha256:df0be2b576a7abbf737b1575f048c23fb1d769f267ec4358296f31c2479db8f9",
+                "sha256:e09031c87a1e51556fdcb46e5bd4f59dfb743061cf93c4d6831bf894f125eb57",
+                "sha256:e4dd52d80b8c83fdce44e12478ad2e85c64ea965e75d66dbeafb0a3e77308fcc",
+                "sha256:fec21693218efe39aa7f8599346e90c705afa52c5b31ae019b2e57e8f6542bb2"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.1.3"
+        },
+        "mdit-py-plugins": {
+            "hashes": [
+                "sha256:b51b3bb70691f57f974e257e367107857a93b36f322a9e6d44ca5bf28ec2def9",
+                "sha256:d8ab27e9aed6c38aa716819fedfde15ca275715955f8a185a8e1cf90fb1d2c1b"
+            ],
+            "markers": "python_version >= '3.8'",
+            "version": "==0.4.0"
+        },
+        "mdurl": {
+            "hashes": [
+                "sha256:84008a41e51615a49fc9966191ff91509e3c40b939176e643fd50a5c2196b8f8",
+                "sha256:bb413d29f5eea38f31dd4754dd7377d4465116fb207585f97bf925588687c1ba"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==0.1.2"
+        },
+        "myst-parser": {
+            "hashes": [
+                "sha256:7c36344ae39c8e740dad7fdabf5aa6fc4897a813083c6cc9990044eb93656b14",
+                "sha256:ea929a67a6a0b1683cdbe19b8d2e724cd7643f8aa3e7bb18dd65beac3483bead"
+            ],
+            "index": "pypi",
+            "version": "==2.0.0"
+        },
+        "packaging": {
+            "hashes": [
+                "sha256:994793af429502c4ea2ebf6bf664629d07c1a9fe974af92966e4b8d2df7edc61",
+                "sha256:a392980d2b6cffa644431898be54b0045151319d1e7ec34f0cfed48767dd334f"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==23.1"
+        },
+        "pygments": {
+            "hashes": [
+                "sha256:8ace4d3c1dd481894b2005f560ead0f9f19ee64fe983366be1a21e171d12775c",
+                "sha256:db2db3deb4b4179f399a09054b023b6a586b76499d36965813c71aa8ed7b5fd1"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.15.1"
+        },
+        "pytz": {
+            "hashes": [
+                "sha256:1d8ce29db189191fb55338ee6d0387d82ab59f3d00eac103412d64e0ebd0c588",
+                "sha256:a151b3abb88eda1d4e34a9814df37de2a80e301e68ba0fd856fb9b46bfbbbffb"
+            ],
+            "version": "==2023.3"
+        },
+        "pyyaml": {
+            "hashes": [
+                "sha256:062582fca9fabdd2c8b54a3ef1c978d786e0f6b3a1510e0ac93ef59e0ddae2bc",
+                "sha256:1635fd110e8d85d55237ab316b5b011de701ea0f29d07611174a1b42f1444741",
+                "sha256:184c5108a2aca3c5b3d3bf9395d50893a7ab82a38004c8f61c258d4428e80206",
+                "sha256:18aeb1bf9a78867dc38b259769503436b7c72f7a1f1f4c93ff9a17de54319b27",
+                "sha256:1d4c7e777c441b20e32f52bd377e0c409713e8bb1386e1099c2415f26e479595",
+                "sha256:1e2722cc9fbb45d9b87631ac70924c11d3a401b2d7f410cc0e3bbf249f2dca62",
+                "sha256:1fe35611261b29bd1de0070f0b2f47cb6ff71fa6595c077e42bd0c419fa27b98",
+                "sha256:28c119d996beec18c05208a8bd78cbe4007878c6dd15091efb73a30e90539696",
+                "sha256:42f8152b8dbc4fe7d96729ec2b99c7097d656dc1213a3229ca5383f973a5ed6d",
+                "sha256:4fb147e7a67ef577a588a0e2c17b6db51dda102c71de36f8549b6816a96e1867",
+                "sha256:50550eb667afee136e9a77d6dc71ae76a44df8b3e51e41b77f6de2932bfe0f47",
+                "sha256:510c9deebc5c0225e8c96813043e62b680ba2f9c50a08d3724c7f28a747d1486",
+                "sha256:5773183b6446b2c99bb77e77595dd486303b4faab2b086e7b17bc6bef28865f6",
+                "sha256:596106435fa6ad000c2991a98fa58eeb8656ef2325d7e158344fb33864ed87e3",
+                "sha256:6965a7bc3cf88e5a1c3bd2e0b5c22f8d677dc88a455344035f03399034eb3007",
+                "sha256:69b023b2b4daa7548bcfbd4aa3da05b3a74b772db9e23b982788168117739938",
+                "sha256:704219a11b772aea0d8ecd7058d0082713c3562b4e271b849ad7dc4a5c90c13c",
+                "sha256:7e07cbde391ba96ab58e532ff4803f79c4129397514e1413a7dc761ccd755735",
+                "sha256:81e0b275a9ecc9c0c0c07b4b90ba548307583c125f54d5b6946cfee6360c733d",
+                "sha256:9046c58c4395dff28dd494285c82ba00b546adfc7ef001486fbf0324bc174fba",
+                "sha256:9eb6caa9a297fc2c2fb8862bc5370d0303ddba53ba97e71f08023b6cd73d16a8",
+                "sha256:a0cd17c15d3bb3fa06978b4e8958dcdc6e0174ccea823003a106c7d4d7899ac5",
+                "sha256:afd7e57eddb1a54f0f1a974bc4391af8bcce0b444685d936840f125cf046d5bd",
+                "sha256:b1275ad35a5d18c62a7220633c913e1b42d44b46ee12554e5fd39c70a243d6a3",
+                "sha256:b786eecbdf8499b9ca1d697215862083bd6d2a99965554781d0d8d1ad31e13a0",
+                "sha256:ba336e390cd8e4d1739f42dfe9bb83a3cc2e80f567d8805e11b46f4a943f5515",
+                "sha256:baa90d3f661d43131ca170712d903e6295d1f7a0f595074f151c0aed377c9b9c",
+                "sha256:bc1bf2925a1ecd43da378f4db9e4f799775d6367bdb94671027b73b393a7c42c",
+                "sha256:bd4af7373a854424dabd882decdc5579653d7868b8fb26dc7d0e99f823aa5924",
+                "sha256:bf07ee2fef7014951eeb99f56f39c9bb4af143d8aa3c21b1677805985307da34",
+                "sha256:bfdf460b1736c775f2ba9f6a92bca30bc2095067b8a9d77876d1fad6cc3b4a43",
+                "sha256:c8098ddcc2a85b61647b2590f825f3db38891662cfc2fc776415143f599bb859",
+                "sha256:d2b04aac4d386b172d5b9692e2d2da8de7bfb6c387fa4f801fbf6fb2e6ba4673",
+                "sha256:d858aa552c999bc8a8d57426ed01e40bef403cd8ccdd0fc5f6f04a00414cac2a",
+                "sha256:f003ed9ad21d6a4713f0a9b5a7a0a79e08dd0f221aff4525a2be4c346ee60aab",
+                "sha256:f22ac1c3cac4dbc50079e965eba2c1058622631e526bd9afd45fedd49ba781fa",
+                "sha256:faca3bdcf85b2fc05d06ff3fbc1f83e1391b3e724afa3feba7d13eeab355484c",
+                "sha256:fca0e3a251908a499833aa292323f32437106001d436eca0e6e7833256674585",
+                "sha256:fd1592b3fdf65fff2ad0004b5e363300ef59ced41c2e6b3a99d4089fa8c5435d",
+                "sha256:fd66fc5d0da6d9815ba2cebeb4205f95818ff4b79c3ebe268e75d961704af52f"
+            ],
+            "markers": "python_version >= '3.6'",
+            "version": "==6.0.1"
+        },
+        "requests": {
+            "hashes": [
+                "sha256:58cd2187c01e70e6e26505bca751777aa9f2ee0b7f4300988b709f44e013003f",
+                "sha256:942c5a758f98d790eaed1a29cb6eefc7ffb0d1cf7af05c3d2791656dbd6ad1e1"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.31.0"
+        },
+        "snowballstemmer": {
+            "hashes": [
+                "sha256:09b16deb8547d3412ad7b590689584cd0fe25ec8db3be37788be3810cbf19cb1",
+                "sha256:c8e1716e83cc398ae16824e5572ae04e0d9fc2c6b985fb0f900f5f0c96ecba1a"
+            ],
+            "version": "==2.2.0"
+        },
+        "sphinx": {
+            "hashes": [
+                "sha256:60c5e04756c1709a98845ed27a2eed7a556af3993afb66e77fec48189f742616",
+                "sha256:61e025f788c5977d9412587e733733a289e2b9fdc2fef8868ddfbfc4ccfe881d"
+            ],
+            "index": "pypi",
+            "version": "==7.0.1"
+        },
+        "sphinx-autodoc-typehints": {
+            "hashes": [
+                "sha256:6a73c0c61a9144ce2ed5ef2bed99d615254e5005c1cc32002017d72d69fb70e6",
+                "sha256:94e440066941bb237704bb880785e2d05e8ae5406c88674feefbb938ad0dc6af"
+            ],
+            "index": "pypi",
+            "version": "==1.24.0"
+        },
+        "sphinx-copybutton": {
+            "hashes": [
+                "sha256:4cf17c82fb9646d1bc9ca92ac280813a3b605d8c421225fd9913154103ee1fbd",
+                "sha256:fb543fd386d917746c9a2c50360c7905b605726b9355cd26e9974857afeae06e"
+            ],
+            "index": "pypi",
+            "version": "==0.5.2"
+        },
+        "sphinxcontrib-applehelp": {
+            "hashes": [
+                "sha256:29d341f67fb0f6f586b23ad80e072c8e6ad0b48417db2bde114a4c9746feb228",
+                "sha256:828f867945bbe39817c210a1abfd1bc4895c8b73fcaade56d45357a348a07d7e"
+            ],
+            "markers": "python_version >= '3.8'",
+            "version": "==1.0.4"
+        },
+        "sphinxcontrib-devhelp": {
+            "hashes": [
+                "sha256:8165223f9a335cc1af7ffe1ed31d2871f325254c0423bc0c4c7cd1c1e4734a2e",
+                "sha256:ff7f1afa7b9642e7060379360a67e9c41e8f3121f2ce9164266f61b9f4b338e4"
+            ],
+            "markers": "python_version >= '3.5'",
+            "version": "==1.0.2"
+        },
+        "sphinxcontrib-htmlhelp": {
+            "hashes": [
+                "sha256:0cbdd302815330058422b98a113195c9249825d681e18f11e8b1f78a2f11efff",
+                "sha256:c38cb46dccf316c79de6e5515e1770414b797162b23cd3d06e67020e1d2a6903"
+            ],
+            "markers": "python_version >= '3.8'",
+            "version": "==2.0.1"
+        },
+        "sphinxcontrib-jsmath": {
+            "hashes": [
+                "sha256:2ec2eaebfb78f3f2078e73666b1415417a116cc848b72e5172e596c871103178",
+                "sha256:a9925e4a4587247ed2191a22df5f6970656cb8ca2bd6284309578f2153e0c4b8"
+            ],
+            "markers": "python_version >= '3.5'",
+            "version": "==1.0.1"
+        },
+        "sphinxcontrib-qthelp": {
+            "hashes": [
+                "sha256:4c33767ee058b70dba89a6fc5c1892c0d57a54be67ddd3e7875a18d14cba5a72",
+                "sha256:bd9fc24bcb748a8d51fd4ecaade681350aa63009a347a8c14e637895444dfab6"
+            ],
+            "markers": "python_version >= '3.5'",
+            "version": "==1.0.3"
+        },
+        "sphinxcontrib-serializinghtml": {
+            "hashes": [
+                "sha256:352a9a00ae864471d3a7ead8d7d79f5fc0b57e8b3f95e9867eb9eb28999b92fd",
+                "sha256:aa5f6de5dfdf809ef505c4895e51ef5c9eac17d0f287933eb49ec495280b6952"
+            ],
+            "markers": "python_version >= '3.5'",
+            "version": "==1.1.5"
+        },
+        "urllib3": {
+            "hashes": [
+                "sha256:8d22f86aae8ef5e410d4f539fde9ce6b2113a001bb4d189e0aed70642d602b11",
+                "sha256:de7df1803967d2c2a98e4b11bb7d6bd9210474c46e8a0401514e3a42a75ebde4"
+            ],
+            "markers": "python_version >= '3.7'",
+            "version": "==2.0.4"
+        },
+        "zipp": {
+            "hashes": [
+                "sha256:679e51dd4403591b2d6838a48de3d283f3d188412a9782faadf845f298736ba0",
+                "sha256:ebc15946aa78bd63458992fc81ec3b6f7b1e92d51c35e6de1c3804e73b799147"
             ],
             "markers": "python_version < '3.10'",
-            "version": "==3.16.1"
+            "version": "==3.16.2"
         }
     }
 }
```

### Comparing `heatmap_cli-0.1.3/README.md` & `heatmap_cli-0.2.0/README.md`

 * *Files 15% similar despite different names*

```diff
@@ -25,29 +25,31 @@
 ## Usage
 
 ```console
 heatmap_cli -h
 ```
 
 ```console
-usage: heatmap_cli [-d] [-v] [-h] [-V] CSV_FILENAME
+usage: heatmap_cli [-yr YEAR] [-wk WEEK] [-d] [-v] [-h] [-V] CSV_FILENAME
 
 A console program that generates yearly calendar heatmap.
 
   website: https://github.com/kianmeng/heatmap_cli
   issues: https://github.com/kianmeng/heatmap_cli/issues
 
 positional arguments:
-  CSV_FILENAME   csv filename
+  CSV_FILENAME           csv filename
 
 optional arguments:
-  -d, --debug    show debugging log and stacktrace
-  -v, --verbose  show verbosity of debugging log, use -vv, -vvv for more details
-  -h, --help     show this help message and exit
-  -V, --version  show program's version number and exit
+  -yr YEAR, --year YEAR  filter by year from the CSV file (default: '2023')
+  -wk WEEK, --week WEEK  filter until week of the year from the CSV file (default: '29')
+  -d, --debug            show debugging log and stacktrace
+  -v, --verbose          show verbosity of debugging log, use -vv, -vvv for more details
+  -h, --help             show this help message and exit
+  -V, --version          show program's version number and exit
 ```
 
 ## Copyright and License
 
 Copyright (C) 2023 Kian-Meng Ang
 
 This program is free software: you can redistribute it and/or modify it under
```

### Comparing `heatmap_cli-0.1.3/docs/Makefile` & `heatmap_cli-0.2.0/docs/Makefile`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/docs/make.bat` & `heatmap_cli-0.2.0/docs/make.bat`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/docs/source/_static/logo.jpg` & `heatmap_cli-0.2.0/docs/source/_static/logo.jpg`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/docs/source/conf.py` & `heatmap_cli-0.2.0/docs/source/conf.py`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/heatmap_cli/__init__.py` & `heatmap_cli-0.2.0/heatmap_cli/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,8 +11,8 @@
 # details.
 #
 # You should have received a copy of the GNU Affero General Public License
 # along with this program. If not, see <https://www.gnu.org/licenses/>.
 
 """A console program that generates yearly calendar heatmap."""
 
-__version__ = "0.1.3"
+__version__ = "0.2.0"
```

### Comparing `heatmap_cli-0.1.3/heatmap_cli/__main__.py` & `heatmap_cli-0.2.0/heatmap_cli/__main__.py`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/heatmap_cli/cli.py` & `heatmap_cli-0.2.0/heatmap_cli/cli.py`

 * *Files 19% similar despite different names*

```diff
@@ -28,35 +28,63 @@
 import matplotlib as mpl
 import matplotlib.pyplot as plt
 import pandas as pd
 import seaborn as sns
 
 from heatmap_cli import __version__
 
+# Suppress logging from matplotlib in debug mode
+logging.getLogger("matplotlib").propagate = False
 _logger = logging.getLogger(__name__)
 
 
 def _build_parser(
     _args: Optional[Sequence[str]] = None,
 ) -> argparse.ArgumentParser:
     """Build the CLI parser."""
     parser = argparse.ArgumentParser(
         add_help=False,
         description=__doc__,
-        formatter_class=argparse.RawTextHelpFormatter,
+        formatter_class=lambda prog: argparse.RawTextHelpFormatter(
+            prog,
+            max_help_position=25,
+        ),
     )
 
     parser.add_argument(
         "input_filename",
         help="csv filename",
         type=argparse.FileType("rb"),
         metavar="CSV_FILENAME",
     )
 
     parser.add_argument(
+        "-yr",
+        "--year",
+        dest="year",
+        type=int,
+        default=datetime.datetime.today().year,
+        help="filter by year from the CSV file (default: '%(default)s')",
+        metavar="YEAR",
+    )
+
+    parser.add_argument(
+        "-wk",
+        "--week",
+        dest="week",
+        type=int,
+        default=datetime.datetime.today().strftime("%W"),
+        help=(
+            "filter until week of the year from the CSV file "
+            "(default: '%(default)s')"
+        ),
+        metavar="WEEK",
+    )
+
+    parser.add_argument(
         "-d",
         "--debug",
         default=False,
         action="store_true",
         dest="debug",
         help="show debugging log and stacktrace",
     )
@@ -108,23 +136,43 @@
         config.input_filename, header=None, names=["date", "count"]
     )
     dataframe["date"] = pd.to_datetime(dataframe["date"])
     dataframe["weekday"] = dataframe["date"].dt.weekday + 1
     dataframe["week"] = dataframe["date"].dt.strftime("%W")
     dataframe["count"] = round(dataframe["count"], -2) / 100
 
-    steps = dataframe[dataframe["date"].dt.year == 2023]
+    steps = dataframe[
+        (dataframe["date"].dt.year == config.year)
+        & (dataframe["week"] <= str(config.week).zfill(2))
+    ]
+    if steps.empty:
+        raise ValueError("no data extracted from csv file")
+
+    _logger.debug(max(steps["date"]).date())
+    missing_df = pd.DataFrame(
+        {
+            "date": pd.date_range(
+                start=max(steps["date"]).date() + datetime.timedelta(days=1),
+                end=f"{config.year}-12-31",
+            )
+        }
+    )
+    missing_df["weekday"] = missing_df["date"].dt.weekday + 1
+    missing_df["week"] = missing_df["date"].dt.strftime("%W")
+    missing_df["count"] = 0
+
+    steps = pd.concat([steps, missing_df], ignore_index=True)
     year_dataframe = steps.pivot_table(
         values="count", index=["weekday"], columns=["week"], fill_value=0
     )
     return year_dataframe
 
 
 def _generate_heatmap(
-    _config: argparse.Namespace, dataframe: pd.core.frame.DataFrame
+    config: argparse.Namespace, dataframe: pd.core.frame.DataFrame
 ) -> None:
     # generating matplotlib graphs without a x-server
     # see http://stackoverflow.com/a/4935945
     mpl.use("Agg")
 
     cmap = "RdYlGn_r"
     _fig, axis = plt.subplots(figsize=(8, 5))
@@ -142,35 +190,34 @@
         cbar_kws={
             "orientation": "horizontal",
             "label": f"colourmap: {cmap}, count: by hundred",
             "pad": 0.15,
         },
     )
 
-    this_week = datetime.datetime.today().strftime("%W")
-
     png_filename = (
-        f"2023_week_{this_week}_{cmap}"
+        f"{config.year}_week_{config.week}_{cmap}"
         "_annotated_heatmap_of_total_daily_walked_steps.png"
     )
 
     plt.title(
         (
             "Total Daily Walking Steps Count Up to Week "
-            f"{this_week} 2023 (kianmeng.org)"
+            f"{config.week} {config.year} (kianmeng.org)"
         ),
         fontsize=10,
     )
     plt.tight_layout()
     plt.savefig(
         png_filename,
         bbox_inches="tight",
         transparent=False,
         dpi=76,
     )
+    _logger.info("generate heatmap png file: %s", png_filename)
 
 
 def _run(config: argparse.Namespace) -> None:
     """Run the main flow.
 
     Args:
         config (argparse.Namespace): Config from command line arguments or
@@ -184,12 +231,12 @@
 def main(args: Optional[Sequence[str]] = None) -> None:
     """Run the main program flow."""
     try:
         parser = _build_parser(args)
         parsed_args = parser.parse_args(args)
         _setup_logging(parsed_args.debug)
         _run(parsed_args)
-    except Exception as error:  # pragma: no cover
+    except Exception as error:
         _logger.error(
             "error: %s", getattr(error, "message", str(error)), exc_info=True
         )
         raise SystemExit(1) from None
```

### Comparing `heatmap_cli-0.1.3/pyproject.toml` & `heatmap_cli-0.2.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/tests/conftest.py` & `heatmap_cli-0.2.0/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/tests/fixtures/sample.csv` & `heatmap_cli-0.2.0/tests/fixtures/sample.csv`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/tests/test_verbose_flag.py` & `heatmap_cli-0.2.0/tests/test_verbose_flag.py`

 * *Files identical despite different names*

### Comparing `heatmap_cli-0.1.3/tox.ini` & `heatmap_cli-0.2.0/tox.ini`

 * *Files 10% similar despite different names*

```diff
@@ -5,21 +5,21 @@
 [testenv]
 description = testing against {basepython}
 deps = pipenv
 commands=
     pipenv install --dev
     pipenv run pytest tests
 
-[testenv:cover]
+[testenv:cov]
 description = generate code coverage report in html
 deps = pipenv
 commands=
     pipenv install --dev
     pipenv run pytest tests --cov-fail-under=100 --numprocesses auto --cov=heatmap_cli --cov-report term-missing --cov-report html {toxinidir}/tests
 
 [testenv:doc]
 description = generate sphinx documentation in html
 basepython = python3.11
 deps = pipenv
 commands =
-    pipenv install --dev
+    pipenv install --categories doc
     pipenv run sphinx-build {toxinidir}/docs/source/ {toxinidir}/docs/build/html
```

### Comparing `heatmap_cli-0.1.3/PKG-INFO` & `heatmap_cli-0.2.0/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: heatmap_cli
-Version: 0.1.3
+Version: 0.2.0
 Summary: A console program that generates yearly calendar heatmap.
 Keywords: heatmap,cli
 Author-email: Kian-Meng Ang <kianmeng@cpan.org>
 Description-Content-Type: text/markdown
 Classifier: Development Status :: 3 - Alpha
 Classifier: Environment :: Console
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3 or later (AGPLv3+)
@@ -48,29 +48,31 @@
 ## Usage
 
 ```console
 heatmap_cli -h
 ```
 
 ```console
-usage: heatmap_cli [-d] [-v] [-h] [-V] CSV_FILENAME
+usage: heatmap_cli [-yr YEAR] [-wk WEEK] [-d] [-v] [-h] [-V] CSV_FILENAME
 
 A console program that generates yearly calendar heatmap.
 
   website: https://github.com/kianmeng/heatmap_cli
   issues: https://github.com/kianmeng/heatmap_cli/issues
 
 positional arguments:
-  CSV_FILENAME   csv filename
+  CSV_FILENAME           csv filename
 
 optional arguments:
-  -d, --debug    show debugging log and stacktrace
-  -v, --verbose  show verbosity of debugging log, use -vv, -vvv for more details
-  -h, --help     show this help message and exit
-  -V, --version  show program's version number and exit
+  -yr YEAR, --year YEAR  filter by year from the CSV file (default: '2023')
+  -wk WEEK, --week WEEK  filter until week of the year from the CSV file (default: '29')
+  -d, --debug            show debugging log and stacktrace
+  -v, --verbose          show verbosity of debugging log, use -vv, -vvv for more details
+  -h, --help             show this help message and exit
+  -V, --version          show program's version number and exit
 ```
 
 ## Copyright and License
 
 Copyright (C) 2023 Kian-Meng Ang
 
 This program is free software: you can redistribute it and/or modify it under
```

