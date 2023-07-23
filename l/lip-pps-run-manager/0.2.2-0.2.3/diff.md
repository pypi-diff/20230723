# Comparing `tmp/lip-pps-run-manager-0.2.2.tar.gz` & `tmp/lip-pps-run-manager-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lip-pps-run-manager-0.2.2.tar", last modified: Tue Oct 25 14:40:52 2022, max compression
+gzip compressed data, was "lip-pps-run-manager-0.2.3.tar", last modified: Sun Jul 23 19:20:56 2023, max compression
```

## Comparing `lip-pps-run-manager-0.2.2.tar` & `lip-pps-run-manager-0.2.3.tar`

### file list

```diff
@@ -1,75 +1,75 @@
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.788124 lip-pps-run-manager-0.2.2/
--rw-r--r--   0 cristovao   (501) staff       (20)      639 2022-10-25 14:38:46.000000 lip-pps-run-manager-0.2.2/.bumpversion.cfg
--rw-r--r--   0 cristovao   (501) staff       (20)     3216 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/.cookiecutterrc
--rw-r--r--   0 cristovao   (501) staff       (20)      187 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/.coveragerc
--rw-r--r--   0 cristovao   (501) staff       (20)      353 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/.editorconfig
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.765709 lip-pps-run-manager-0.2.2/.github/
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.772078 lip-pps-run-manager-0.2.2/.github/workflows/
--rw-r--r--   0 cristovao   (501) staff       (20)     5045 2022-10-19 18:30:22.000000 lip-pps-run-manager-0.2.2/.github/workflows/github-actions.yml
--rw-r--r--   0 cristovao   (501) staff       (20)      637 2022-09-27 14:16:29.000000 lip-pps-run-manager-0.2.2/.pre-commit-config.yaml
--rw-r--r--   0 cristovao   (501) staff       (20)      231 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/.readthedocs.yml
--rw-r--r--   0 cristovao   (501) staff       (20)     1551 2022-10-19 18:30:44.000000 lip-pps-run-manager-0.2.2/.travis.yml
--rw-r--r--   0 cristovao   (501) staff       (20)       78 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/AUTHORS.rst
--rw-r--r--   0 cristovao   (501) staff       (20)     1142 2022-10-25 14:33:55.000000 lip-pps-run-manager-0.2.2/CHANGELOG.rst
--rw-r--r--   0 cristovao   (501) staff       (20)     2768 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/CONTRIBUTING.rst
--rw-r--r--   0 cristovao   (501) staff       (20)     1118 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/LICENSE
--rw-r--r--   0 cristovao   (501) staff       (20)      470 2022-10-19 21:18:35.000000 lip-pps-run-manager-0.2.2/MANIFEST.in
--rw-r--r--   0 cristovao   (501) staff       (20)     3338 2022-10-25 14:40:52.788349 lip-pps-run-manager-0.2.2/PKG-INFO
--rw-r--r--   0 cristovao   (501) staff       (20)     3073 2022-10-25 14:38:46.000000 lip-pps-run-manager-0.2.2/README.rst
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.773105 lip-pps-run-manager-0.2.2/ci/
--rwxr-xr-x   0 cristovao   (501) staff       (20)     3063 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/ci/bootstrap.py
--rw-r--r--   0 cristovao   (501) staff       (20)       66 2022-10-13 19:26:58.000000 lip-pps-run-manager-0.2.2/ci/requirements.txt
--rw-r--r--   0 cristovao   (501) staff       (20)       73 2022-10-13 19:27:51.000000 lip-pps-run-manager-0.2.2/ci/requirements_travis.txt
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.773446 lip-pps-run-manager-0.2.2/ci/templates/
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.766150 lip-pps-run-manager-0.2.2/ci/templates/.github/
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.773806 lip-pps-run-manager-0.2.2/ci/templates/.github/workflows/
--rw-r--r--   0 cristovao   (501) staff       (20)     2001 2022-10-13 19:03:29.000000 lip-pps-run-manager-0.2.2/ci/templates/.github/workflows/github-actions.yml
--rw-r--r--   0 cristovao   (501) staff       (20)     1363 2022-10-17 11:28:14.000000 lip-pps-run-manager-0.2.2/ci/templates/.travis.yml
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.777233 lip-pps-run-manager-0.2.2/docs/
--rw-r--r--   0 cristovao   (501) staff       (20)       28 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/docs/authors.rst
--rw-r--r--   0 cristovao   (501) staff       (20)       30 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/docs/changelog.rst
--rw-r--r--   0 cristovao   (501) staff       (20)     1271 2022-10-25 14:38:46.000000 lip-pps-run-manager-0.2.2/docs/conf.py
--rw-r--r--   0 cristovao   (501) staff       (20)       33 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/docs/contributing.rst
--rw-r--r--   0 cristovao   (501) staff       (20)      244 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/docs/index.rst
--rw-r--r--   0 cristovao   (501) staff       (20)       99 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/docs/installation.rst
--rw-r--r--   0 cristovao   (501) staff       (20)       27 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/docs/readme.rst
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.777938 lip-pps-run-manager-0.2.2/docs/reference/
--rw-r--r--   0 cristovao   (501) staff       (20)       71 2022-09-29 18:41:00.000000 lip-pps-run-manager-0.2.2/docs/reference/index.rst
--rw-r--r--   0 cristovao   (501) staff       (20)     1663 2022-10-24 20:46:28.000000 lip-pps-run-manager-0.2.2/docs/reference/lip_pps_run_manager.rst
--rw-r--r--   0 cristovao   (501) staff       (20)       29 2022-10-24 16:13:41.000000 lip-pps-run-manager-0.2.2/docs/requirements.txt
--rw-r--r--   0 cristovao   (501) staff       (20)      109 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/docs/spelling_wordlist.txt
--rw-r--r--   0 cristovao   (501) staff       (20)       90 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/docs/usage.rst
--rw-r--r--   0 cristovao   (501) staff       (20)      160 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/pyproject.toml
--rw-r--r--   0 cristovao   (501) staff       (20)      784 2022-09-27 14:13:20.000000 lip-pps-run-manager-0.2.2/pytest.ini
--rw-r--r--   0 cristovao   (501) staff       (20)      326 2022-10-25 14:40:52.789308 lip-pps-run-manager-0.2.2/setup.cfg
--rwxr-xr-x   0 cristovao   (501) staff       (20)     3102 2022-10-25 14:38:46.000000 lip-pps-run-manager-0.2.2/setup.py
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.766679 lip-pps-run-manager-0.2.2/src/
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.780190 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/
--rw-r--r--   0 cristovao   (501) staff       (20)      261 2022-10-25 14:38:46.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/__init__.py
--rw-r--r--   0 cristovao   (501) staff       (20)      385 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/__main__.py
--rw-r--r--   0 cristovao   (501) staff       (20)      950 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/cli.py
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.784309 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/instruments/
--rw-r--r--   0 cristovao   (501) staff       (20)      883 2022-10-24 20:26:54.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/instruments/Keithley6487.py
--rw-r--r--   0 cristovao   (501) staff       (20)      143 2022-10-24 19:59:38.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/instruments/__init__.py
--rw-r--r--   0 cristovao   (501) staff       (20)      166 2022-10-24 20:00:18.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/instruments/functions.py
--rw-r--r--   0 cristovao   (501) staff       (20)    53741 2022-10-25 10:51:56.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/run_manager.py
--rw-r--r--   0 cristovao   (501) staff       (20)     1253 2022-10-24 20:23:42.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/setup_manager.py
--rw-r--r--   0 cristovao   (501) staff       (20)     8202 2022-10-17 14:07:06.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/telegram_reporter.py
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.783078 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/
--rw-r--r--   0 cristovao   (501) staff       (20)     3338 2022-10-25 14:40:52.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/PKG-INFO
--rw-r--r--   0 cristovao   (501) staff       (20)     1618 2022-10-25 14:40:52.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/SOURCES.txt
--rw-r--r--   0 cristovao   (501) staff       (20)        1 2022-10-25 14:40:52.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/dependency_links.txt
--rw-r--r--   0 cristovao   (501) staff       (20)       69 2022-10-25 14:40:52.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/entry_points.txt
--rw-r--r--   0 cristovao   (501) staff       (20)        1 2022-10-25 14:40:52.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/not-zip-safe
--rw-r--r--   0 cristovao   (501) staff       (20)       25 2022-10-25 14:40:52.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/requires.txt
--rw-r--r--   0 cristovao   (501) staff       (20)       20 2022-10-25 14:40:52.000000 lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/top_level.txt
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.786749 lip-pps-run-manager-0.2.2/tests/
-drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2022-10-25 14:40:52.787644 lip-pps-run-manager-0.2.2/tests/intruments/
--rw-r--r--   0 cristovao   (501) staff       (20)      522 2022-10-24 20:24:13.000000 lip-pps-run-manager-0.2.2/tests/intruments/test_Keithley6487.py
--rw-r--r--   0 cristovao   (501) staff       (20)      513 2022-10-24 20:25:19.000000 lip-pps-run-manager-0.2.2/tests/intruments/test_functions.py
--rw-r--r--   0 cristovao   (501) staff       (20)       73 2022-09-28 09:54:24.000000 lip-pps-run-manager-0.2.2/tests/test_lip_pps_run_manager.py
--rw-r--r--   0 cristovao   (501) staff       (20)    46440 2022-10-24 14:34:09.000000 lip-pps-run-manager-0.2.2/tests/test_run_manager_class.py
--rw-r--r--   0 cristovao   (501) staff       (20)     3418 2022-10-24 13:35:25.000000 lip-pps-run-manager-0.2.2/tests/test_run_manager_functions.py
--rw-r--r--   0 cristovao   (501) staff       (20)    72145 2022-10-24 14:34:08.000000 lip-pps-run-manager-0.2.2/tests/test_task_manager_class.py
--rw-r--r--   0 cristovao   (501) staff       (20)     7306 2022-10-21 17:00:56.000000 lip-pps-run-manager-0.2.2/tests/test_telegram_reporter_class.py
--rw-r--r--   0 cristovao   (501) staff       (20)     1770 2022-10-24 16:12:29.000000 lip-pps-run-manager-0.2.2/tox.ini
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:56.007891 lip-pps-run-manager-0.2.3/
+-rw-r--r--   0 cristovao   (501) staff       (20)      639 2023-07-23 19:10:53.000000 lip-pps-run-manager-0.2.3/.bumpversion.cfg
+-rw-r--r--   0 cristovao   (501) staff       (20)     3216 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/.cookiecutterrc
+-rw-r--r--   0 cristovao   (501) staff       (20)      187 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/.coveragerc
+-rw-r--r--   0 cristovao   (501) staff       (20)      353 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/.editorconfig
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:55.988296 lip-pps-run-manager-0.2.3/.github/
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:55.994869 lip-pps-run-manager-0.2.3/.github/workflows/
+-rw-r--r--   0 cristovao   (501) staff       (20)     5615 2023-07-21 18:18:07.000000 lip-pps-run-manager-0.2.3/.github/workflows/github-actions.yml
+-rw-r--r--   0 cristovao   (501) staff       (20)      628 2023-07-21 18:08:44.000000 lip-pps-run-manager-0.2.3/.pre-commit-config.yaml
+-rw-r--r--   0 cristovao   (501) staff       (20)      231 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/.readthedocs.yml
+-rw-r--r--   0 cristovao   (501) staff       (20)     1614 2023-07-21 18:16:38.000000 lip-pps-run-manager-0.2.3/.travis.yml
+-rw-r--r--   0 cristovao   (501) staff       (20)       79 2023-07-23 19:13:39.000000 lip-pps-run-manager-0.2.3/AUTHORS.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)     1442 2023-07-23 19:17:42.000000 lip-pps-run-manager-0.2.3/CHANGELOG.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)     2763 2023-07-21 17:21:32.000000 lip-pps-run-manager-0.2.3/CONTRIBUTING.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)     1118 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/LICENSE
+-rw-r--r--   0 cristovao   (501) staff       (20)      470 2022-10-19 21:18:35.000000 lip-pps-run-manager-0.2.3/MANIFEST.in
+-rw-r--r--   0 cristovao   (501) staff       (20)     3719 2023-07-23 19:20:56.008036 lip-pps-run-manager-0.2.3/PKG-INFO
+-rw-r--r--   0 cristovao   (501) staff       (20)     3083 2023-07-23 19:10:53.000000 lip-pps-run-manager-0.2.3/README.rst
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:55.995726 lip-pps-run-manager-0.2.3/ci/
+-rwxr-xr-x   0 cristovao   (501) staff       (20)     3063 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/ci/bootstrap.py
+-rw-r--r--   0 cristovao   (501) staff       (20)       66 2022-10-13 19:26:58.000000 lip-pps-run-manager-0.2.3/ci/requirements.txt
+-rw-r--r--   0 cristovao   (501) staff       (20)       73 2022-10-13 19:27:51.000000 lip-pps-run-manager-0.2.3/ci/requirements_travis.txt
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:55.996055 lip-pps-run-manager-0.2.3/ci/templates/
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:55.988922 lip-pps-run-manager-0.2.3/ci/templates/.github/
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:55.996344 lip-pps-run-manager-0.2.3/ci/templates/.github/workflows/
+-rw-r--r--   0 cristovao   (501) staff       (20)     2001 2022-10-13 19:03:29.000000 lip-pps-run-manager-0.2.3/ci/templates/.github/workflows/github-actions.yml
+-rw-r--r--   0 cristovao   (501) staff       (20)     1363 2022-10-17 11:28:14.000000 lip-pps-run-manager-0.2.3/ci/templates/.travis.yml
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:55.999744 lip-pps-run-manager-0.2.3/docs/
+-rw-r--r--   0 cristovao   (501) staff       (20)       28 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/docs/authors.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)       30 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/docs/changelog.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)     1271 2023-07-23 19:10:53.000000 lip-pps-run-manager-0.2.3/docs/conf.py
+-rw-r--r--   0 cristovao   (501) staff       (20)       33 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/docs/contributing.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)      244 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/docs/index.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)       99 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/docs/installation.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)       27 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/docs/readme.rst
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:56.000303 lip-pps-run-manager-0.2.3/docs/reference/
+-rw-r--r--   0 cristovao   (501) staff       (20)       71 2022-09-29 18:41:00.000000 lip-pps-run-manager-0.2.3/docs/reference/index.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)     1663 2022-10-24 20:46:28.000000 lip-pps-run-manager-0.2.3/docs/reference/lip_pps_run_manager.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)       29 2022-10-24 16:13:41.000000 lip-pps-run-manager-0.2.3/docs/requirements.txt
+-rw-r--r--   0 cristovao   (501) staff       (20)      109 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/docs/spelling_wordlist.txt
+-rw-r--r--   0 cristovao   (501) staff       (20)       90 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/docs/usage.rst
+-rw-r--r--   0 cristovao   (501) staff       (20)      160 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/pyproject.toml
+-rw-r--r--   0 cristovao   (501) staff       (20)      784 2022-09-27 14:13:20.000000 lip-pps-run-manager-0.2.3/pytest.ini
+-rw-r--r--   0 cristovao   (501) staff       (20)      326 2023-07-23 19:20:56.008633 lip-pps-run-manager-0.2.3/setup.cfg
+-rwxr-xr-x   0 cristovao   (501) staff       (20)     3152 2023-07-23 19:10:53.000000 lip-pps-run-manager-0.2.3/setup.py
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:55.989506 lip-pps-run-manager-0.2.3/src/
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:56.002451 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/
+-rw-r--r--   0 cristovao   (501) staff       (20)      261 2023-07-23 19:10:53.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/__init__.py
+-rw-r--r--   0 cristovao   (501) staff       (20)      385 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/__main__.py
+-rw-r--r--   0 cristovao   (501) staff       (20)      950 2022-09-27 09:19:54.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/cli.py
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:56.005270 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/instruments/
+-rw-r--r--   0 cristovao   (501) staff       (20)      883 2022-10-24 20:26:54.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/instruments/Keithley6487.py
+-rw-r--r--   0 cristovao   (501) staff       (20)      143 2022-10-24 19:59:38.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/instruments/__init__.py
+-rw-r--r--   0 cristovao   (501) staff       (20)      166 2022-10-24 20:00:18.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/instruments/functions.py
+-rw-r--r--   0 cristovao   (501) staff       (20)    59999 2023-07-23 19:01:29.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/run_manager.py
+-rw-r--r--   0 cristovao   (501) staff       (20)     1328 2023-07-23 19:03:26.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/setup_manager.py
+-rw-r--r--   0 cristovao   (501) staff       (20)     8202 2022-10-17 14:07:06.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/telegram_reporter.py
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:56.004434 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/
+-rw-r--r--   0 cristovao   (501) staff       (20)     3719 2023-07-23 19:20:55.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/PKG-INFO
+-rw-r--r--   0 cristovao   (501) staff       (20)     1618 2023-07-23 19:20:55.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/SOURCES.txt
+-rw-r--r--   0 cristovao   (501) staff       (20)        1 2023-07-23 19:20:55.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/dependency_links.txt
+-rw-r--r--   0 cristovao   (501) staff       (20)       70 2023-07-23 19:20:55.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/entry_points.txt
+-rw-r--r--   0 cristovao   (501) staff       (20)        1 2023-07-23 19:19:04.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/not-zip-safe
+-rw-r--r--   0 cristovao   (501) staff       (20)       25 2023-07-23 19:20:55.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/requires.txt
+-rw-r--r--   0 cristovao   (501) staff       (20)       20 2023-07-23 19:20:55.000000 lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/top_level.txt
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:56.007066 lip-pps-run-manager-0.2.3/tests/
+drwxr-xr-x   0 cristovao   (501) staff       (20)        0 2023-07-23 19:20:56.007646 lip-pps-run-manager-0.2.3/tests/intruments/
+-rw-r--r--   0 cristovao   (501) staff       (20)     1421 2022-11-02 22:04:37.000000 lip-pps-run-manager-0.2.3/tests/intruments/test_Keithley6487.py
+-rw-r--r--   0 cristovao   (501) staff       (20)     1034 2022-11-02 18:32:03.000000 lip-pps-run-manager-0.2.3/tests/intruments/test_functions.py
+-rw-r--r--   0 cristovao   (501) staff       (20)       73 2022-09-28 09:54:24.000000 lip-pps-run-manager-0.2.3/tests/test_lip_pps_run_manager.py
+-rw-r--r--   0 cristovao   (501) staff       (20)    58081 2023-07-23 18:41:12.000000 lip-pps-run-manager-0.2.3/tests/test_run_manager_class.py
+-rw-r--r--   0 cristovao   (501) staff       (20)     3418 2022-10-24 13:35:25.000000 lip-pps-run-manager-0.2.3/tests/test_run_manager_functions.py
+-rw-r--r--   0 cristovao   (501) staff       (20)    75575 2023-07-23 19:00:24.000000 lip-pps-run-manager-0.2.3/tests/test_task_manager_class.py
+-rw-r--r--   0 cristovao   (501) staff       (20)     7306 2022-10-21 17:00:56.000000 lip-pps-run-manager-0.2.3/tests/test_telegram_reporter_class.py
+-rw-r--r--   0 cristovao   (501) staff       (20)     1809 2023-07-21 18:10:42.000000 lip-pps-run-manager-0.2.3/tox.ini
```

### Comparing `lip-pps-run-manager-0.2.2/.bumpversion.cfg` & `lip-pps-run-manager-0.2.3/.bumpversion.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 [bumpversion]
-current_version = 0.2.2
+current_version = 0.2.3
 commit = True
 tag = True
 
 [bumpversion:file:setup.py]
 search = version='{current_version}'
 replace = version='{new_version}'
```

### Comparing `lip-pps-run-manager-0.2.2/.cookiecutterrc` & `lip-pps-run-manager-0.2.3/.cookiecutterrc`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/.github/workflows/github-actions.yml` & `lip-pps-run-manager-0.2.3/.github/workflows/github-actions.yml`

 * *Files 13% similar despite different names*

```diff
@@ -87,14 +87,32 @@
             os: 'windows-latest'
           - name: 'py310 (macos)'
             python: '3.10'
             toxpython: 'python3.10'
             python_arch: 'x64'
             tox_env: 'py310'
             os: 'macos-latest'
+          - name: 'py311 (ubuntu)'
+            python: '3.11'
+            toxpython: 'python3.11'
+            python_arch: 'x64'
+            tox_env: 'py311'
+            os: 'ubuntu-latest'
+          - name: 'py311 (windows)'
+            python: '3.11'
+            toxpython: 'python3.11'
+            python_arch: 'x64'
+            tox_env: 'py311'
+            os: 'windows-latest'
+          - name: 'py311 (macos)'
+            python: '3.11'
+            toxpython: 'python3.11'
+            python_arch: 'x64'
+            tox_env: 'py311'
+            os: 'macos-latest'
           - name: 'pypy37 (ubuntu)'
             python: 'pypy-3.7'
             toxpython: 'pypy3.7'
             python_arch: 'x64'
             tox_env: 'pypy37'
             os: 'ubuntu-latest'
           - name: 'pypy37 (windows)'
```

### Comparing `lip-pps-run-manager-0.2.2/.pre-commit-config.yaml` & `lip-pps-run-manager-0.2.3/.pre-commit-config.yaml`

 * *Files 20% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 # To install the git pre-commit hook run:
 #   pre-commit install
 # To update the pre-commit hooks run:
 #   pre-commit install-hooks
 exclude: '^(\.tox|ci/templates|\.bumpversion\.cfg)(/|$)'
 repos:
   - repo: https://github.com/pre-commit/pre-commit-hooks
-    rev: v4.3.0
+    rev: v4.4.0
     hooks:
       - id: trailing-whitespace
       - id: end-of-file-fixer
       - id: debug-statements
-  - repo: https://github.com/timothycrosley/isort
-    rev: 5.10.1
+  - repo: https://github.com/PyCQA/isort
+    rev: 5.12.0
     hooks:
       - id: isort
   - repo: https://github.com/psf/black
-    rev: 22.8.0
+    rev: 23.7.0
     hooks:
       - id: black
   - repo: https://gitlab.com/pycqa/flake8
     rev: 3.9.2
     hooks:
       - id: flake8
```

### Comparing `lip-pps-run-manager-0.2.2/.travis.yml` & `lip-pps-run-manager-0.2.3/.travis.yml`

 * *Files 11% similar despite different names*

```diff
@@ -29,14 +29,17 @@
     - env:
         - TOXENV=py39,codecov
       python: '3.9'
     - env:
         - TOXENV=py310,codecov
       python: '3.10'
     - env:
+        - TOXENV=py311,codecov
+      python: '3.11'
+    - env:
         - TOXENV=pypy37,codecov
         - TOXPYTHON=pypy3
       python: 'pypy3'
     - env:
         - TOXENV=pypy38,codecov
         - TOXPYTHON=pypy3
       python: 'pypy3'
```

### Comparing `lip-pps-run-manager-0.2.2/CHANGELOG.rst` & `lip-pps-run-manager-0.2.3/CHANGELOG.rst`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,25 @@
 
 Changelog
 =========
 
-Current (2022-10-24)
+Current (2023-07-23)
 --------------------
 
+0.2.3 (2023-07-23)
+--------------------
+
+* Added a backup_directory property to the RunManager
+* Added the copy_file_to method to the RunManager
+* Added the backup_file method to the RunManager
+
+Not numbered (2022-10-24)
+-------------------------
+
+* Added a data_directory property to the RunManager
 
 0.2.2 (2022-10-25)
 ------------------
 
 * Added common functions for the instruments
 * Started adding SetupManager to hold the experimental setup
 * Started tests for instruments
```

### Comparing `lip-pps-run-manager-0.2.2/CONTRIBUTING.rst` & `lip-pps-run-manager-0.2.3/CONTRIBUTING.rst`

 * *Files 2% similar despite different names*

```diff
@@ -45,15 +45,15 @@
 
 3. Create a branch for local development::
 
     git checkout -b name-of-your-bugfix-or-feature
 
    Now you can make your changes locally.
 
-4. When you're done making changes run all the checks and docs builder with `tox <https://tox.readthedocs.io/en/latest/install.html>`_ one command::
+4. When you're done making changes run all the checks and docs builder with `tox <https://tox.wiki/en/latest/installation.html>`_ one command::
 
     tox
 
 5. Commit your changes and push your branch to GitHub::
 
     git add .
     git commit -m "Your detailed description of your changes."
```

### Comparing `lip-pps-run-manager-0.2.2/LICENSE` & `lip-pps-run-manager-0.2.3/LICENSE`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/PKG-INFO` & `lip-pps-run-manager-0.2.3/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,31 +1,33 @@
 Metadata-Version: 2.1
 Name: lip-pps-run-manager
-Version: 0.2.2
+Version: 0.2.3
 Summary: Run Manager used in the LIP PPS software stack for handling data taking and analysis
 Home-page: https://github.com/cbeiraod/LIP_PPS_Run_Manager
 Author: Cristóvão B. da Cruz e Silva
 Author-email: cbeiraod@cern.ch
 License: MIT
-Project-URL: Documentation, https://LIP_PPS_Run_Manager.readthedocs.io/
-Project-URL: Changelog, https://LIP_PPS_Run_Manager.readthedocs.io/en/latest/changelog.html
+Project-URL: Documentation, https://lip-pps-run-manager.readthedocs.io/
+Project-URL: Changelog, https://lip-pps-run-manager.readthedocs.io/en/latest/changelog.html
 Project-URL: Issue Tracker, https://github.com/cbeiraod/LIP_PPS_Run_Manager/issues
+Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: Unix
 Classifier: Operating System :: POSIX
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Utilities
 Requires-Python: >=3.7
 License-File: LICENSE
 License-File: AUTHORS.rst
 
@@ -51,15 +53,15 @@
     pip install https://github.com/cbeiraod/LIP_PPS_Run_Manager/archive/main.zip
 
 
 Documentation
 =============
 
 
-https://LIP_PPS_Run_Manager.readthedocs.io/
+https://lip-pps-run-manager.readthedocs.io/en/latest/
 
 
 Development
 ===========
 
 To run all the tests run::
 
@@ -82,17 +84,28 @@
 
             PYTEST_ADDOPTS=--cov-append tox
 
 
 Changelog
 =========
 
-Current (2022-10-24)
+Current (2023-07-23)
 --------------------
 
+0.2.3 (2023-07-23)
+--------------------
+
+* Added a backup_directory property to the RunManager
+* Added the copy_file_to method to the RunManager
+* Added the backup_file method to the RunManager
+
+Not numbered (2022-10-24)
+-------------------------
+
+* Added a data_directory property to the RunManager
 
 0.2.2 (2022-10-25)
 ------------------
 
 * Added common functions for the instruments
 * Started adding SetupManager to hold the experimental setup
 * Started tests for instruments
@@ -119,7 +132,9 @@
 * First fully functional version
 
 
 0.0.0 (2022-09-27)
 ------------------
 
 * First release on PyPI.
+
+
```

### Comparing `lip-pps-run-manager-0.2.2/README.rst` & `lip-pps-run-manager-0.2.3/README.rst`

 * *Files 8% similar despite different names*

```diff
@@ -12,15 +12,15 @@
     * - tests
       - | |github-actions| |travis| |requires|
         | |codecov|
     * - package
       - | |version| |wheel| |supported-versions| |supported-implementations|
         | |commits-since|
 .. |docs| image:: https://readthedocs.org/projects/lip-pps-run-manager/badge/?version=latest
-    :target: https://LIP_PPS_Run_Manager.readthedocs.io/
+    :target: https://lip-pps-run-manager.readthedocs.io/
     :alt: Documentation Status
 
 .. |travis| image:: https://api.travis-ci.com/cbeiraod/LIP_PPS_Run_Manager.svg?branch=main
     :alt: Travis-CI Build Status
     :target: https://travis-ci.com/github/cbeiraod/LIP_PPS_Run_Manager
 
 .. |github-actions| image:: https://github.com/cbeiraod/LIP_PPS_Run_Manager/actions/workflows/github-actions.yml/badge.svg
@@ -47,17 +47,17 @@
     :alt: Supported versions
     :target: https://pypi.org/project/lip-pps-run-manager
 
 .. |supported-implementations| image:: https://img.shields.io/pypi/implementation/lip-pps-run-manager.svg
     :alt: Supported implementations
     :target: https://pypi.org/project/lip-pps-run-manager
 
-.. |commits-since| image:: https://img.shields.io/github/commits-since/cbeiraod/LIP_PPS_Run_Manager/v0.2.2.svg
+.. |commits-since| image:: https://img.shields.io/github/commits-since/cbeiraod/LIP_PPS_Run_Manager/v0.2.3.svg
     :alt: Commits since latest release
-    :target: https://github.com/cbeiraod/LIP_PPS_Run_Manager/compare/v0.2.2...main
+    :target: https://github.com/cbeiraod/LIP_PPS_Run_Manager/compare/v0.2.3...main
 
 
 
 .. end-badges
 
 Run Manager used in the LIP PPS software stack for handling data taking and analysis
 
@@ -75,15 +75,15 @@
     pip install https://github.com/cbeiraod/LIP_PPS_Run_Manager/archive/main.zip
 
 
 Documentation
 =============
 
 
-https://LIP_PPS_Run_Manager.readthedocs.io/
+https://lip-pps-run-manager.readthedocs.io/en/latest/
 
 
 Development
 ===========
 
 To run all the tests run::
```

### Comparing `lip-pps-run-manager-0.2.2/ci/bootstrap.py` & `lip-pps-run-manager-0.2.3/ci/bootstrap.py`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/ci/templates/.github/workflows/github-actions.yml` & `lip-pps-run-manager-0.2.3/ci/templates/.github/workflows/github-actions.yml`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/ci/templates/.travis.yml` & `lip-pps-run-manager-0.2.3/ci/templates/.travis.yml`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/docs/conf.py` & `lip-pps-run-manager-0.2.3/docs/conf.py`

 * *Files 1% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 ]
 source_suffix = '.rst'
 master_doc = 'index'
 project = 'LIP_PPS_Run_Manager'
 year = '2022'
 author = 'Cristóvão B. da Cruz e Silva'
 copyright = '{0}, {1}'.format(year, author)
-version = release = '0.2.2'
+version = release = '0.2.3'
 
 pygments_style = 'trac'
 templates_path = ['.']
 extlinks = {
     'issue': ('https://github.com/cbeiraod/LIP_PPS_Run_Manager/issues/%s', '#'),
     'pr': ('https://github.com/cbeiraod/LIP_PPS_Run_Manager/pull/%s', 'PR #'),
 }
```

### Comparing `lip-pps-run-manager-0.2.2/docs/reference/lip_pps_run_manager.rst` & `lip-pps-run-manager-0.2.3/docs/reference/lip_pps_run_manager.rst`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/pytest.ini` & `lip-pps-run-manager-0.2.3/pytest.ini`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/setup.py` & `lip-pps-run-manager-0.2.3/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 def read(*names, **kwargs):
     with io.open(join(dirname(__file__), *names), encoding=kwargs.get('encoding', 'utf8')) as fh:
         return fh.read()
 
 
 setup(
     name='lip-pps-run-manager',
-    version='0.2.2',
+    version='0.2.3',
     license='MIT',
     description='Run Manager used in the LIP PPS software stack for handling data taking and analysis',
     long_description='{}\n{}'.format(
         re.compile('^.. start-badges.*^.. end-badges', re.M | re.S).sub('', read('README.rst')),
         re.sub(':[a-z]+:`~?(.*?)`', r'``\1``', read('CHANGELOG.rst')),
     ),
     author='Cristóvão B. da Cruz e Silva',
@@ -46,25 +46,26 @@
         'Programming Language :: Python',
         'Programming Language :: Python :: 3',
         'Programming Language :: Python :: 3 :: Only',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
+        'Programming Language :: Python :: 3.11',
         'Programming Language :: Python :: Implementation :: CPython',
         'Programming Language :: Python :: Implementation :: PyPy',
         # uncomment if you test on these interpreters:
         # 'Programming Language :: Python :: Implementation :: IronPython',
         # 'Programming Language :: Python :: Implementation :: Jython',
         # 'Programming Language :: Python :: Implementation :: Stackless',
         'Topic :: Utilities',
     ],
     project_urls={
-        'Documentation': 'https://LIP_PPS_Run_Manager.readthedocs.io/',
-        'Changelog': 'https://LIP_PPS_Run_Manager.readthedocs.io/en/latest/changelog.html',
+        'Documentation': 'https://lip-pps-run-manager.readthedocs.io/',
+        'Changelog': 'https://lip-pps-run-manager.readthedocs.io/en/latest/changelog.html',
         'Issue Tracker': 'https://github.com/cbeiraod/LIP_PPS_Run_Manager/issues',
     },
     keywords=[
         # eg: 'keyword1', 'keyword2', 'keyword3',
     ],
     python_requires='>=3.7',
     install_requires=[
```

### Comparing `lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/cli.py` & `lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/cli.py`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/instruments/Keithley6487.py` & `lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/instruments/Keithley6487.py`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/run_manager.py` & `lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/run_manager.py`

 * *Files 4% similar despite different names*

```diff
@@ -374,14 +374,42 @@
     #    """
     #    This is the setter method
     #    where I can check it's not assigned a value < 0
     #    """
     #    self._path_directory = value
 
     @property
+    def data_directory(self) -> Path:
+        """The data directory property getter method
+
+        This method fetches the data directory path attribute,
+        which points to the path containing the run data of this run.
+
+        Returns
+        -------
+        Path
+            The path to the directory where the data is stored.
+        """
+        return self._path_directory / "data"
+
+    @property
+    def backup_directory(self) -> Path:
+        """The backup directory property getter method
+
+        This method fetches the backup directory path attribute,
+        which points to the path containing the backup data of this run.
+
+        Returns
+        -------
+        Path
+            The path to the directory where the backup data is stored.
+        """
+        return self._path_directory / "backup"
+
+    @property
     def run_name(self) -> str:
         """The name of the run property getter method"""
         return self._path_directory.parts[-1]
 
     def __enter__(self):
         """This is the method that is called when using the "with" syntax"""
         self._in_run_context = True
@@ -803,14 +831,117 @@
         try:
             self._telegram_response = self._telegram_reporter.edit_message(message, message_id)
         except Exception as e:
             warnings.warn("Could not connect to Telegram to send the message. Reason: {}".format(repr(e)), category=RuntimeWarning)
 
         return self._telegram_response['result']['message_id']
 
+    def copy_file_to(self, source: Path, destination: Path, overwrite: bool = False):
+        """Creates a copy of the source file to the destination.
+
+        Parameters
+        ----------
+        source
+            The path to the source file. The file must exist
+        destination
+            The path to the destination. If the destination does not exist, the
+            parent must exist and the file will be created. If the destination
+            does exist, it must be a directory and a file with the same name as
+            the source will be created. If the destination exists and is a file,
+            action will only be taken if the `overwrite` flag is set.
+        overwrite
+            Whether to overwrite the destination file in case it already exists
+
+        Raises
+        ------
+        TypeError
+            If the type of one of the parameters is not correct
+        RuntimeError
+            If the `source` does not exist, if the `destination` does not exist
+            and the parent directory does not exist or if the `destination`
+            does exist and `overwrite` is not set.
+        SameFileError
+            If `source` and `destination` are the same file, a SameFileError
+            will be raised.
+
+        Examples
+        --------
+        >>> import lip_pps_run_manager as RM
+        >>> from pathlib import Path
+        >>> with RM.RunManager("Run0001") as John
+        ...   John.create_run(True)
+        ...   John.copy_file_to(Path("src.file"), Path("copy_of.file"))
+
+        The above code should create a copy of the `src.file` in the
+        `copy_of.file`, if the `src.file` exists. If not, a RuntimeError
+        will be raised.
+
+        """
+        if not isinstance(source, Path):
+            raise TypeError(f"The `source` must be a Path type object, received object of type {type(source)} instead")
+
+        if not isinstance(destination, Path):
+            raise TypeError(f"The `destination` must be a Path type object, received object of type {type(destination)} instead")
+
+        if not source.exists() or not source.is_file():
+            raise RuntimeError("The source file does not exist or it is not a file.")
+
+        if not destination.exists():
+            if not destination.parent.exists():
+                raise RuntimeError("The parent of the destination file does not exist, unable to create the destination file")
+        else:  # Destination exists
+            if destination.is_file():
+                if not overwrite:
+                    raise RuntimeError("The destination file already exists and the overwrite flag is not set")
+            else:
+                destination = destination / source.name
+
+        shutil.copy(source, destination)
+
+    def backup_file(self, source: Path):
+        """Creates a backup of the file inside the run directory under the
+        backup subdirectory.
+
+        Parameters
+        ----------
+        source
+            The path to the source file. The file must exist
+
+        Raises
+        ------
+        TypeError
+            If the type of one of the parameters is not correct
+        RuntimeError
+            If the `source` does not exist.
+
+        Examples
+        --------
+        >>> import lip_pps_run_manager as RM
+        >>> from pathlib import Path
+        >>> with RM.RunManager("Run0001") as John
+        ...   John.create_run(True)
+        ...   John.backup_file(Path("src.file"))
+
+        The above code should create a backup copy of the `src.file` in the
+        backup directory of the run, if the `src.file` exists. If not, a
+        RuntimeError will be raised.
+
+        """
+        if not isinstance(source, Path):
+            raise TypeError(f"The `source` must be a Path type object, received object of type {type(source)} instead")
+
+        if not source.exists() or not source.is_file():
+            raise RuntimeError("The source file does not exist or it is not a file.")
+
+        backup_path = self.backup_directory
+        if not backup_path.exists():
+            backup_path.mkdir()
+
+        self.copy_file_to(source, backup_path, overwrite=True)
+
 
 class TaskManager(RunManager):
     """Class to manage PPS Tasks
 
     This Class initializes the on disk structures if necessary.
 
     Parameters
@@ -1325,7 +1456,47 @@
                             message_to_send += "Received the following warning {} times:\n".format(count)
                         message_to_send += msg
                 self.send_message(message_to_send, self._task_status_message_id)
                 self._accumulated_warnings = {}
         else:
             self._supposedly_just_sent_warnings = self._accumulated_warnings  # Do this just because of the testing
             self._accumulated_warnings = {}
+
+    def backup_file(self, source: Path):
+        """Creates a backup of the source file inside the task directory.
+
+        Parameters
+        ----------
+        source
+            The path to the source file. The file must exist
+
+        Raises
+        ------
+        TypeError
+            If the type of one of the parameters is not correct
+        RuntimeError
+            If the `source` does not exist.
+
+        Examples
+        --------
+        >>> import lip_pps_run_manager as RM
+        >>> from pathlib import Path
+        >>> with RM.RunManager("Run0001") as John
+        ...   John.create_run(True)
+        ...   John.backup_file(Path("src.file"))
+
+        TODO: Fix this examples
+
+        The above code should create a backup copy of the `src.file` in the
+        backup directory of the run, if the `src.file` exists. If not, a
+        RuntimeError will be raised.
+
+        """
+        if not isinstance(source, Path):
+            raise TypeError(f"The `source` must be a Path type object, received object of type {type(source)} instead")
+
+        if not source.exists() or not source.is_file():
+            raise RuntimeError("The source file does not exist or it is not a file.")
+
+        backup_path = self.task_path
+
+        self.copy_file_to(source, backup_path / (source.name + ".bak"), overwrite=True)
```

### Comparing `lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/setup_manager.py` & `lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/setup_manager.py`

 * *Files 8% similar despite different names*

```diff
@@ -5,15 +5,15 @@
     _name = None
 
     def __init__(self, device_name: str, device_type: str):
         self._type = device_type
         self._name = device_name
 
     def safe_shutdown(self):
-        raise RuntimeError("The device type {} has not had its safe shutdown set...".format(self._type))
+        raise RuntimeError("The device type {} has not had its safe shutdown set...".format(self._type))  # pragma: no cover
 
 
 class VISADevice(DeviceBase):
     """This is the base class for implementing a device for an experimental setup which communicates with the VISA interface"""
 
     _VISA_ResourceManager = None
     _VISA_Handle = None
@@ -32,8 +32,9 @@
 
 class SetupManager:
     """This class holds details about the experimental setup (particularly useful for device configuration)"""
 
     _devices = {}
 
     def __init__(self):
-        pass
+        pass  # pragma: no cover
+        # Still under construction
```

### Comparing `lip-pps-run-manager-0.2.2/src/lip_pps_run_manager/telegram_reporter.py` & `lip-pps-run-manager-0.2.3/src/lip_pps_run_manager/telegram_reporter.py`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/PKG-INFO` & `lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,31 +1,33 @@
 Metadata-Version: 2.1
 Name: lip-pps-run-manager
-Version: 0.2.2
+Version: 0.2.3
 Summary: Run Manager used in the LIP PPS software stack for handling data taking and analysis
 Home-page: https://github.com/cbeiraod/LIP_PPS_Run_Manager
 Author: Cristóvão B. da Cruz e Silva
 Author-email: cbeiraod@cern.ch
 License: MIT
-Project-URL: Documentation, https://LIP_PPS_Run_Manager.readthedocs.io/
-Project-URL: Changelog, https://LIP_PPS_Run_Manager.readthedocs.io/en/latest/changelog.html
+Project-URL: Documentation, https://lip-pps-run-manager.readthedocs.io/
+Project-URL: Changelog, https://lip-pps-run-manager.readthedocs.io/en/latest/changelog.html
 Project-URL: Issue Tracker, https://github.com/cbeiraod/LIP_PPS_Run_Manager/issues
+Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: Unix
 Classifier: Operating System :: POSIX
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Utilities
 Requires-Python: >=3.7
 License-File: LICENSE
 License-File: AUTHORS.rst
 
@@ -51,15 +53,15 @@
     pip install https://github.com/cbeiraod/LIP_PPS_Run_Manager/archive/main.zip
 
 
 Documentation
 =============
 
 
-https://LIP_PPS_Run_Manager.readthedocs.io/
+https://lip-pps-run-manager.readthedocs.io/en/latest/
 
 
 Development
 ===========
 
 To run all the tests run::
 
@@ -82,17 +84,28 @@
 
             PYTEST_ADDOPTS=--cov-append tox
 
 
 Changelog
 =========
 
-Current (2022-10-24)
+Current (2023-07-23)
 --------------------
 
+0.2.3 (2023-07-23)
+--------------------
+
+* Added a backup_directory property to the RunManager
+* Added the copy_file_to method to the RunManager
+* Added the backup_file method to the RunManager
+
+Not numbered (2022-10-24)
+-------------------------
+
+* Added a data_directory property to the RunManager
 
 0.2.2 (2022-10-25)
 ------------------
 
 * Added common functions for the instruments
 * Started adding SetupManager to hold the experimental setup
 * Started tests for instruments
@@ -119,7 +132,9 @@
 * First fully functional version
 
 
 0.0.0 (2022-09-27)
 ------------------
 
 * First release on PyPI.
+
+
```

### Comparing `lip-pps-run-manager-0.2.2/src/lip_pps_run_manager.egg-info/SOURCES.txt` & `lip-pps-run-manager-0.2.3/src/lip_pps_run_manager.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/tests/test_run_manager_class.py` & `lip-pps-run-manager-0.2.3/tests/test_run_manager_class.py`

 * *Files 20% similar despite different names*

```diff
@@ -10,14 +10,19 @@
 
 
 def ensure_clean(path: Path):  # pragma: no cover
     if path.exists() and path.is_dir():
         shutil.rmtree(path)
 
 
+def ensure_exists(path: Path):  # pragma: no cover
+    if not path.exists():
+        path.mkdir()
+
+
 def prepare_config_file(bot_name, bot_token, chat_name, chat_id):  # pragma: no cover
     config_file = Path.cwd() / "run_manager_telegram_config.json"
     with config_file.open("w", encoding="utf-8") as file:
         file.write("{\n")
         file.write('  "bots": {\n')
         file.write('    "{}": "{}"\n'.format(bot_name, bot_token))
         file.write("  },\n")
@@ -36,14 +41,16 @@
     runPath = Path(tmpdir) / run_name
     ensure_clean(runPath)
 
     John = RM.RunManager(runPath, rate_limit=False)
 
     assert John._path_directory == runPath
     assert John.path_directory == runPath
+    assert John.data_directory == runPath / "data"
+    assert John.backup_directory == runPath / "backup"
     assert John.run_name == run_name
     assert John._bot_token is None
     assert John._chat_id is None
     assert John._rate_limit
 
 
 @patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
@@ -1240,7 +1247,376 @@
     with RM.RunManager(runPath, telegram_bot_token=bot_token, telegram_chat_id=chat_id, rate_limit=rate_limit) as John:
         David = John.handle_task("myTask1", backup_python_file=True)
 
         assert David._bot_token == John._bot_token
         assert David._chat_id == John._chat_id
         assert David._telegram_reporter == John._telegram_reporter
         assert David._status_message_id == John._status_message_id
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_copy_file_to_destination_is_file_to_create():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+    destination = runPath / "copied_file.txt"
+
+    assert not destination.exists()
+    assert not source.exists()
+
+    with open(source, "w") as file:
+        file.write("Hello!\n")
+        file.write("This is a test file\n")
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+
+        John.copy_file_to(source, destination)
+
+        assert destination.exists()
+
+        import filecmp
+
+        assert filecmp.cmp(source, destination)
+
+    source.unlink()
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_copy_file_to_destination_is_dir():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+    destination = runPath
+
+    assert not source.exists()
+
+    with open(source, "w") as file:
+        file.write("Hello!\n")
+        file.write("This is a test file\n")
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+        assert destination.exists()
+        assert destination.is_dir()
+
+        John.copy_file_to(source, destination)
+
+        assert (destination / "test_in_file.txt").exists()
+
+        import filecmp
+
+        assert filecmp.cmp(source, (destination / "test_in_file.txt"))
+
+    source.unlink()
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_copy_file_to_destination_is_file_to_overwrite():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+    destination = runPath / "copied_file.txt"
+
+    assert not destination.exists()
+    assert not source.exists()
+
+    with open(source, "w") as file:
+        file.write("Hello!\n")
+        file.write("This is a test file\n")
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+
+        with open(destination, "w") as file:
+            file.write("This is a mostly empty file.\n")
+
+        assert destination.exists()
+
+        John.copy_file_to(source, destination, overwrite=True)
+
+        assert destination.exists()
+
+        import filecmp
+
+        assert filecmp.cmp(source, destination)
+
+    source.unlink()
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_copy_file_to_destination_is_file_no_overwrite():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+    destination = runPath / "copied_file.txt"
+
+    assert not destination.exists()
+    assert not source.exists()
+
+    with open(source, "w") as file:
+        file.write("Hello!\n")
+        file.write("This is a test file\n")
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+
+        with open(destination, "w") as file:
+            file.write("This is a mostly empty file.\n")
+
+        assert destination.exists()
+
+        try:
+            John.copy_file_to(source, destination)
+        except RuntimeError as e:
+            assert str(e) == "The destination file already exists and the overwrite flag is not set"
+
+    source.unlink()
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_copy_file_to_bad_type_source():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = 2
+    destination = runPath / "copied_file.txt"
+
+    assert not destination.exists()
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+        try:
+            John.copy_file_to(source, destination)
+            raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+        except TypeError as e:
+            assert str(e) == "The `source` must be a Path type object, received object of type <class 'int'> instead"
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_copy_file_to_bad_type_destination():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+    destination = 2
+
+    assert not source.exists()
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+        try:
+            John.copy_file_to(source, destination)
+            raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+        except TypeError as e:
+            assert str(e) == "The `destination` must be a Path type object, received object of type <class 'int'> instead"
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_copy_file_to_source_does_not_exist():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+    destination = runPath / "copied_file.txt"
+
+    assert not destination.exists()
+    assert not source.exists()
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+        try:
+            John.copy_file_to(source, destination)
+            raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+        except RuntimeError as e:
+            assert str(e) == "The source file does not exist or it is not a file."
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_copy_file_to_source_is_not_file():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir)
+    destination = runPath / "copied_file.txt"
+
+    assert not destination.exists()
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+        try:
+            John.copy_file_to(source, destination)
+            raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+        except RuntimeError as e:
+            assert str(e) == "The source file does not exist or it is not a file."
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_copy_file_to_destination_parent_does_not_exist():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+    destination = runPath / "this_dir_does_not_exist" / "copied_file.txt"
+
+    assert not destination.exists()
+    assert not destination.parent.exists()
+    assert not source.exists()
+
+    with open(source, "w") as file:
+        file.write("Hello!\n")
+        file.write("This is a test file\n")
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+        try:
+            John.copy_file_to(source, destination)
+            raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+        except RuntimeError as e:
+            assert str(e) == "The parent of the destination file does not exist, unable to create the destination file"
+
+    source.unlink()
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_backup_file():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+
+    assert not source.exists()
+
+    with open(source, "w") as file:
+        file.write("Hello!\n")
+        file.write("This is a test file\n")
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+
+        assert not John.backup_directory.exists()
+
+        John.backup_file(source)
+
+        assert John.backup_directory.exists()
+
+        assert (John.backup_directory / source.name).exists()
+
+        import filecmp
+
+        assert filecmp.cmp(source, (John.backup_directory / source.name))
+
+    source.unlink()
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_backup_file_backup_dir_exists():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+
+    assert not source.exists()
+
+    with open(source, "w") as file:
+        file.write("Hello!\n")
+        file.write("This is a test file\n")
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+
+        assert not John.backup_directory.exists()
+        John.backup_directory.mkdir()
+        assert John.backup_directory.exists()
+
+        John.backup_file(source)
+
+        assert (John.backup_directory / source.name).exists()
+
+        import filecmp
+
+        assert filecmp.cmp(source, (John.backup_directory / source.name))
+
+    source.unlink()
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_backup_file_bad_type_source():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = 2
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+
+        try:
+            John.backup_file(source)
+            raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+        except TypeError as e:
+            assert str(e) == "The `source` must be a Path type object, received object of type <class 'int'> instead"
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_backup_file_source_does_not_exist():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir) / "test_in_file.txt"
+
+    assert not source.exists()
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+        try:
+            John.backup_file(source)
+            raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+        except RuntimeError as e:
+            assert str(e) == "The source file does not exist or it is not a file."
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_backup_file_source_is_not_file():
+    tmpdir = tempfile.gettempdir()
+    run_name = "Run0001"
+    runPath = Path(tmpdir) / run_name
+    ensure_clean(runPath)
+
+    source = Path(tmpdir)
+
+    with RM.RunManager(runPath) as John:
+        John.create_run(raise_error=True)
+        try:
+            John.backup_file(source)
+            raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+        except RuntimeError as e:
+            assert str(e) == "The source file does not exist or it is not a file."
```

### Comparing `lip-pps-run-manager-0.2.2/tests/test_run_manager_functions.py` & `lip-pps-run-manager-0.2.3/tests/test_run_manager_functions.py`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/tests/test_task_manager_class.py` & `lip-pps-run-manager-0.2.3/tests/test_task_manager_class.py`

 * *Files 2% similar despite different names*

```diff
@@ -1821,7 +1821,99 @@
                 in Tobias._telegram_reporter._session["data"]["text"]
             )
             assert "Received the following warning {} times:\n".format(1) not in Tobias._telegram_reporter._session["data"]["text"]
             assert "Received the following warning {} times:\n".format(repeats) in Tobias._telegram_reporter._session["data"]["text"]
             assert message1 in Tobias._telegram_reporter._session["data"]["text"]
             assert message2 in Tobias._telegram_reporter._session["data"]["text"]
             assert Tobias._accumulated_warnings == {}
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_backup_file():
+    with PrepareRunDir() as handler:
+        task_name = "testTask"
+        drop_old_data = True
+        script_to_backup = None
+        loop_iterations = None
+
+        source = handler.run_path / "test_in_file.txt"
+
+        assert not source.exists()
+
+        with open(source, "w") as file:
+            file.write("Hello!\n")
+            file.write("This is a test file\n")
+
+        with RM.TaskManager(
+            handler.run_path, task_name, drop_old_data=drop_old_data, script_to_backup=script_to_backup, loop_iterations=loop_iterations
+        ) as Tobias:
+            Tobias.backup_file(source)
+
+            assert (Tobias.task_path / (source.name + ".bak")).exists()
+
+            import filecmp
+
+            assert filecmp.cmp(source, (Tobias.task_path / (source.name + ".bak")))
+
+        source.unlink()
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_backup_file_bad_type_source():
+    with PrepareRunDir() as handler:
+        task_name = "testTask"
+        drop_old_data = True
+        script_to_backup = None
+        loop_iterations = None
+
+        source = 2
+
+        with RM.TaskManager(
+            handler.run_path, task_name, drop_old_data=drop_old_data, script_to_backup=script_to_backup, loop_iterations=loop_iterations
+        ) as Tobias:
+            try:
+                Tobias.backup_file(source)
+                raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+            except TypeError as e:
+                assert str(e) == "The `source` must be a Path type object, received object of type <class 'int'> instead"
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_backup_file_source_does_not_exist():
+    with PrepareRunDir() as handler:
+        task_name = "testTask"
+        drop_old_data = True
+        script_to_backup = None
+        loop_iterations = None
+
+        source = handler.run_path / "test_in_file.txt"
+
+        assert not source.exists()
+
+        with RM.TaskManager(
+            handler.run_path, task_name, drop_old_data=drop_old_data, script_to_backup=script_to_backup, loop_iterations=loop_iterations
+        ) as Tobias:
+            try:
+                Tobias.backup_file(source)
+                raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+            except RuntimeError as e:
+                assert str(e) == "The source file does not exist or it is not a file."
+
+
+@patch('requests.Session', new=SessionReplacement)  # To avoid sending actual http requests
+def test_backup_file_source_is_not_file():
+    with PrepareRunDir() as handler:
+        task_name = "testTask"
+        drop_old_data = True
+        script_to_backup = None
+        loop_iterations = None
+
+        source = handler.run_path
+
+        with RM.TaskManager(
+            handler.run_path, task_name, drop_old_data=drop_old_data, script_to_backup=script_to_backup, loop_iterations=loop_iterations
+        ) as Tobias:
+            try:
+                Tobias.backup_file(source)
+                raise Exception("Passed through a fail condition without failing")  # pragma: no cover
+            except RuntimeError as e:
+                assert str(e) == "The source file does not exist or it is not a file."
```

### Comparing `lip-pps-run-manager-0.2.2/tests/test_telegram_reporter_class.py` & `lip-pps-run-manager-0.2.3/tests/test_telegram_reporter_class.py`

 * *Files identical despite different names*

### Comparing `lip-pps-run-manager-0.2.2/tox.ini` & `lip-pps-run-manager-0.2.3/tox.ini`

 * *Files 4% similar despite different names*

```diff
@@ -10,36 +10,38 @@
 ; a generative tox configuration, see: https://tox.readthedocs.io/en/latest/config.html#generative-envlist
 
 [tox]
 envlist =
     clean,
     check,
     docs,
-    {py37,py38,py39,py310,pypy37,pypy38,pypy39},
+    {py37,py38,py39,py310,py311,pypy37,pypy38,pypy39},
     report
 ignore_basepython_conflict = true
 
 [testenv]
 basepython =
     pypy37: {env:TOXPYTHON:pypy3.7}
     pypy38: {env:TOXPYTHON:pypy3.8}
     pypy39: {env:TOXPYTHON:pypy3.9}
     py37: {env:TOXPYTHON:python3.7}
     py38: {env:TOXPYTHON:python3.8}
     py39: {env:TOXPYTHON:python3.9}
     py310: {env:TOXPYTHON:python3.10}
+    py311: {env:TOXPYTHON:python3.11}
     {bootstrap,clean,check,report,docs,codecov}: {env:TOXPYTHON:python3}
 setenv =
     PYTHONPATH={toxinidir}/tests
     PYTHONUNBUFFERED=yes
 passenv =
     *
 usedevelop = false
 deps =
     pytest
+    py
     pytest-travis-fold
     pytest-cov
     requests
     humanize
     pyvisa
 commands =
     {posargs:pytest --cov --cov-report=term-missing -vv tests}
@@ -51,15 +53,15 @@
     flake8
     readme-renderer
     pygments
     isort
 skip_install = true
 commands =
     python setup.py check --strict --metadata --restructuredtext
-    check-manifest '{toxinidir}'
+    check-manifest .
     flake8
     isort --verbose --check-only --diff --filter-files .
 
 [testenv:docs]
 usedevelop = true
 deps =
     -r{toxinidir}/docs/requirements.txt
```

