# Comparing `tmp/artifacts-20230413.tar.gz` & `tmp/artifacts-20230723.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "artifacts-20230413.tar", last modified: Tue Apr 18 03:49:47 2023, max compression
+gzip compressed data, was "artifacts-20230723.tar", last modified: Sun Jul 23 09:46:57 2023, max compression
```

## Comparing `artifacts-20230413.tar` & `artifacts-20230723.tar`

### file list

```diff
@@ -1,130 +1,129 @@
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.215101 artifacts-20230413/
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:46.955101 artifacts-20230413/.github/
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.053101 artifacts-20230413/.github/workflows/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2515 2023-04-13 07:50:17.000000 artifacts-20230413/.github/workflows/test_docker.yml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1365 2023-04-13 07:50:17.000000 artifacts-20230413/.github/workflows/test_docs.yml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     4068 2023-04-13 07:50:17.000000 artifacts-20230413/.github/workflows/test_tox.yml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    21911 2023-04-13 06:58:50.000000 artifacts-20230413/.pylintrc
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      149 2022-12-20 18:52:11.000000 artifacts-20230413/.yamllint.yaml
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      151 2021-11-01 18:53:11.000000 artifacts-20230413/ACKNOWLEDGEMENTS
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      488 2014-11-26 17:20:08.000000 artifacts-20230413/AUTHORS
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)    11325 2014-11-19 19:52:15.000000 artifacts-20230413/LICENSE
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      609 2022-12-20 18:52:11.000000 artifacts-20230413/MANIFEST.in
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      674 2023-04-18 03:49:47.215101 artifacts-20230413/PKG-INFO
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      303 2022-12-20 18:52:11.000000 artifacts-20230413/README
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      932 2022-12-20 18:52:11.000000 artifacts-20230413/README.md
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1230 2023-04-13 06:58:50.000000 artifacts-20230413/appveyor.yml
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.055101 artifacts-20230413/artifacts/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)       99 2023-04-18 03:49:23.000000 artifacts-20230413/artifacts/__init__.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     3274 2022-12-20 18:52:11.000000 artifacts-20230413/artifacts/artifact.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      946 2022-12-20 18:52:11.000000 artifacts-20230413/artifacts/definitions.py
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      387 2018-03-18 07:06:42.000000 artifacts-20230413/artifacts/errors.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    10920 2022-12-20 18:52:11.000000 artifacts-20230413/artifacts/reader.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     8516 2022-12-20 18:52:11.000000 artifacts-20230413/artifacts/registry.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    13704 2022-12-20 18:52:11.000000 artifacts-20230413/artifacts/source_type.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2733 2022-12-20 18:52:11.000000 artifacts-20230413/artifacts/writer.py
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.056101 artifacts-20230413/artifacts.egg-info/
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      674 2023-04-18 03:49:44.000000 artifacts-20230413/artifacts.egg-info/PKG-INFO
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)     2475 2023-04-18 03:49:46.000000 artifacts-20230413/artifacts.egg-info/SOURCES.txt
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)        1 2023-04-18 03:49:44.000000 artifacts-20230413/artifacts.egg-info/dependency_links.txt
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       24 2023-04-18 03:49:44.000000 artifacts-20230413/artifacts.egg-info/requires.txt
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       10 2023-04-18 03:49:44.000000 artifacts-20230413/artifacts.egg-info/top_level.txt
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      529 2022-12-20 18:52:11.000000 artifacts-20230413/artifacts.ini
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:46.956101 artifacts-20230413/config/
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.057101 artifacts-20230413/config/appveyor/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      834 2023-04-13 06:58:50.000000 artifacts-20230413/config/appveyor/install.ps1
--rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)      125 2023-04-13 06:58:50.000000 artifacts-20230413/config/appveyor/install.sh
--rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)      620 2023-04-13 06:58:50.000000 artifacts-20230413/config/appveyor/runtests.sh
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.106101 artifacts-20230413/config/dpkg/
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       21 2017-05-20 19:17:24.000000 artifacts-20230413/config/dpkg/artifacts-data.dirs
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       27 2017-07-01 08:08:23.000000 artifacts-20230413/config/dpkg/artifacts-data.install
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)        8 2017-05-21 20:05:37.000000 artifacts-20230413/config/dpkg/artifacts-tools.install
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      159 2023-04-18 03:49:23.000000 artifacts-20230413/config/dpkg/changelog
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       22 2017-05-20 19:17:24.000000 artifacts-20230413/config/dpkg/clean
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)        2 2023-04-13 06:58:50.000000 artifacts-20230413/config/dpkg/compat
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1304 2023-04-13 06:58:50.000000 artifacts-20230413/config/dpkg/control
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)     1017 2017-05-13 17:01:46.000000 artifacts-20230413/config/dpkg/copyright
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       99 2017-05-20 19:17:24.000000 artifacts-20230413/config/dpkg/python3-artifacts.install
--rwxrwxr-x   0 lordyesta  (1000) lordyesta  (1000)      122 2023-04-13 06:58:50.000000 artifacts-20230413/config/dpkg/rules
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.107101 artifacts-20230413/config/dpkg/source/
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       12 2017-05-20 19:17:24.000000 artifacts-20230413/config/dpkg/source/format
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.148101 artifacts-20230413/data/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    16384 2023-01-30 18:02:06.000000 artifacts-20230413/data/.windows.yaml.swp
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     6762 2022-12-20 18:52:11.000000 artifacts-20230413/data/antivirus.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     4248 2022-12-20 18:52:11.000000 artifacts-20230413/data/applications.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2787 2022-12-20 18:52:11.000000 artifacts-20230413/data/cloud_services.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1664 2022-12-20 18:52:11.000000 artifacts-20230413/data/config_files.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      812 2022-12-20 18:52:11.000000 artifacts-20230413/data/containerd.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     6324 2022-12-20 18:52:11.000000 artifacts-20230413/data/database_servers.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      522 2022-12-20 18:52:11.000000 artifacts-20230413/data/docker.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     3602 2022-12-20 18:52:11.000000 artifacts-20230413/data/esxi.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1030 2022-12-20 18:52:11.000000 artifacts-20230413/data/file_systems.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1258 2022-12-20 18:52:11.000000 artifacts-20230413/data/hadoop.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      838 2023-01-30 17:22:48.000000 artifacts-20230413/data/ics.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1958 2022-12-20 18:52:11.000000 artifacts-20230413/data/installed_module_paths.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5243 2022-12-20 18:52:11.000000 artifacts-20230413/data/installed_modules.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2316 2023-01-30 17:22:48.000000 artifacts-20230413/data/instant_messaging.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      558 2022-12-20 18:52:11.000000 artifacts-20230413/data/java.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5174 2022-12-20 18:52:11.000000 artifacts-20230413/data/kaspersky_careto.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5223 2022-12-20 18:52:11.000000 artifacts-20230413/data/kubernetes.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2743 2022-12-20 18:52:11.000000 artifacts-20230413/data/legacy.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    24973 2023-01-30 17:22:48.000000 artifacts-20230413/data/linux.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5117 2022-12-20 18:52:11.000000 artifacts-20230413/data/linux_proc.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1221 2022-12-20 18:52:11.000000 artifacts-20230413/data/linux_services.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    27748 2023-01-30 17:22:48.000000 artifacts-20230413/data/macos.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     8373 2022-12-20 18:52:11.000000 artifacts-20230413/data/shell.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     4201 2022-12-20 18:52:11.000000 artifacts-20230413/data/tomcat.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     8988 2022-12-20 18:52:11.000000 artifacts-20230413/data/triage.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2522 2022-12-20 18:52:11.000000 artifacts-20230413/data/unix_common.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      892 2023-01-30 17:22:48.000000 artifacts-20230413/data/user.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    71374 2023-04-13 03:32:57.000000 artifacts-20230413/data/webbrowser.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2884 2022-12-20 18:52:11.000000 artifacts-20230413/data/webservers.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)   167680 2022-12-20 18:52:11.000000 artifacts-20230413/data/windows.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     6174 2022-12-20 18:52:11.000000 artifacts-20230413/data/windows_dll_hijacking.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     8549 2022-12-20 18:52:11.000000 artifacts-20230413/data/wmi.yaml
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      150 2021-11-01 18:53:11.000000 artifacts-20230413/dependencies.ini
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.168101 artifacts-20230413/docs/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)       88 2022-12-20 18:52:11.000000 artifacts-20230413/docs/Artifacts definition format and style guide.asciidoc
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5127 2023-04-13 06:58:50.000000 artifacts-20230413/docs/conf.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      673 2022-12-20 18:52:11.000000 artifacts-20230413/docs/index.rst
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      105 2023-04-13 06:59:04.000000 artifacts-20230413/docs/requirements.txt
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.180101 artifacts-20230413/docs/sources/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    15892 2022-12-20 18:52:11.000000 artifacts-20230413/docs/sources/Format-specification.md
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.181101 artifacts-20230413/docs/sources/api/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1176 2022-12-20 18:52:11.000000 artifacts-20230413/docs/sources/api/artifacts.rst
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)       64 2022-12-20 18:52:11.000000 artifacts-20230413/docs/sources/api/modules.rst
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.181101 artifacts-20230413/docs/sources/background/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      726 2023-04-18 03:49:23.000000 artifacts-20230413/docs/sources/background/Stats.md
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      873 2022-12-20 18:52:11.000000 artifacts-20230413/docs/sources/background/Terminology.md
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1276 2022-12-20 18:52:11.000000 artifacts-20230413/docs/sources/background/index.rst
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.182101 artifacts-20230413/docs/sources/user/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1703 2022-12-20 18:52:11.000000 artifacts-20230413/docs/sources/user/Installation-instructions.md
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      311 2022-12-20 18:52:11.000000 artifacts-20230413/docs/sources/user/index.rst
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       28 2023-04-13 06:58:50.000000 artifacts-20230413/requirements.txt
--rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)     1018 2022-12-20 18:52:11.000000 artifacts-20230413/run_tests.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      320 2023-04-18 03:49:47.216101 artifacts-20230413/setup.cfg
--rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)     7313 2023-04-13 06:58:50.000000 artifacts-20230413/setup.py
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.182101 artifacts-20230413/test_data/
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2422 2022-12-20 18:52:11.000000 artifacts-20230413/test_data/definitions.json
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2312 2022-12-20 18:52:11.000000 artifacts-20230413/test_data/definitions.yaml
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)        0 2022-12-20 18:52:11.000000 artifacts-20230413/test_dependencies.ini
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-13 06:58:50.000000 artifacts-20230413/test_requirements.txt
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.195101 artifacts-20230413/tests/
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       24 2021-11-01 18:53:11.000000 artifacts-20230413/tests/__init__.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    11907 2022-12-20 18:52:11.000000 artifacts-20230413/tests/reader_test.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     4906 2022-12-20 18:52:11.000000 artifacts-20230413/tests/registry_test.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5365 2022-12-20 18:52:11.000000 artifacts-20230413/tests/source_type_test.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1720 2022-12-20 18:52:11.000000 artifacts-20230413/tests/test_lib.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1135 2022-12-20 18:52:11.000000 artifacts-20230413/tests/validator_test.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1837 2022-12-20 18:52:11.000000 artifacts-20230413/tests/writer_test.py
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.201101 artifacts-20230413/tools/
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       46 2021-11-01 18:53:12.000000 artifacts-20230413/tools/__init__.py
--rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)     3740 2022-12-20 18:52:11.000000 artifacts-20230413/tools/stats.py
--rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)    21201 2022-12-20 18:52:11.000000 artifacts-20230413/tools/validator.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1257 2023-04-13 07:50:17.000000 artifacts-20230413/tox.ini
-drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-18 03:49:47.215101 artifacts-20230413/utils/
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)        0 2018-03-18 07:06:41.000000 artifacts-20230413/utils/__init__.py
--rwxrwxr-x   0 lordyesta  (1000) lordyesta  (1000)      422 2023-04-13 06:58:50.000000 artifacts-20230413/utils/check_dependencies.py
--rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    11583 2023-04-13 06:58:50.000000 artifacts-20230413/utils/dependencies.py
--rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)     9073 2015-05-07 21:05:55.000000 artifacts-20230413/utils/pylintrc
--rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)      675 2022-12-20 18:52:11.000000 artifacts-20230413/utils/update_release.sh
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.869228 artifacts-20230723/
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.652227 artifacts-20230723/.github/
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.723227 artifacts-20230723/.github/workflows/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2515 2023-04-30 05:28:49.000000 artifacts-20230723/.github/workflows/test_docker.yml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1365 2023-04-30 05:13:17.000000 artifacts-20230723/.github/workflows/test_docs.yml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     4068 2023-04-30 05:13:17.000000 artifacts-20230723/.github/workflows/test_tox.yml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    21911 2023-04-30 05:13:17.000000 artifacts-20230723/.pylintrc
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      149 2022-12-20 18:52:11.000000 artifacts-20230723/.yamllint.yaml
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      151 2021-11-01 18:53:11.000000 artifacts-20230723/ACKNOWLEDGEMENTS
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      488 2014-11-26 17:20:08.000000 artifacts-20230723/AUTHORS
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)    11325 2014-11-19 19:52:15.000000 artifacts-20230723/LICENSE
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      609 2022-12-20 18:52:11.000000 artifacts-20230723/MANIFEST.in
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      674 2023-07-23 09:46:57.869228 artifacts-20230723/PKG-INFO
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      303 2022-12-20 18:52:11.000000 artifacts-20230723/README
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      932 2022-12-20 18:52:11.000000 artifacts-20230723/README.md
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1230 2023-04-30 05:13:17.000000 artifacts-20230723/appveyor.yml
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.724227 artifacts-20230723/artifacts/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)       99 2023-07-23 09:45:44.000000 artifacts-20230723/artifacts/__init__.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     3274 2022-12-20 18:52:11.000000 artifacts-20230723/artifacts/artifact.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      946 2022-12-20 18:52:11.000000 artifacts-20230723/artifacts/definitions.py
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      387 2018-03-18 07:06:42.000000 artifacts-20230723/artifacts/errors.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    10920 2022-12-20 18:52:11.000000 artifacts-20230723/artifacts/reader.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     8516 2022-12-20 18:52:11.000000 artifacts-20230723/artifacts/registry.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    13704 2022-12-20 18:52:11.000000 artifacts-20230723/artifacts/source_type.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2733 2022-12-20 18:52:11.000000 artifacts-20230723/artifacts/writer.py
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.725227 artifacts-20230723/artifacts.egg-info/
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      674 2023-07-23 09:46:55.000000 artifacts-20230723/artifacts.egg-info/PKG-INFO
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)     2452 2023-07-23 09:46:57.000000 artifacts-20230723/artifacts.egg-info/SOURCES.txt
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)        1 2023-07-23 09:46:55.000000 artifacts-20230723/artifacts.egg-info/dependency_links.txt
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       24 2023-07-23 09:46:55.000000 artifacts-20230723/artifacts.egg-info/requires.txt
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       10 2023-07-23 09:46:55.000000 artifacts-20230723/artifacts.egg-info/top_level.txt
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      529 2022-12-20 18:52:11.000000 artifacts-20230723/artifacts.ini
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.652227 artifacts-20230723/config/
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.726227 artifacts-20230723/config/appveyor/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      834 2023-04-30 05:13:17.000000 artifacts-20230723/config/appveyor/install.ps1
+-rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)      125 2023-04-30 05:13:17.000000 artifacts-20230723/config/appveyor/install.sh
+-rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)      620 2023-04-30 05:13:17.000000 artifacts-20230723/config/appveyor/runtests.sh
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.782227 artifacts-20230723/config/dpkg/
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       21 2017-05-20 19:17:24.000000 artifacts-20230723/config/dpkg/artifacts-data.dirs
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       27 2017-07-01 08:08:23.000000 artifacts-20230723/config/dpkg/artifacts-data.install
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)        8 2017-05-21 20:05:37.000000 artifacts-20230723/config/dpkg/artifacts-tools.install
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      159 2023-07-23 09:45:44.000000 artifacts-20230723/config/dpkg/changelog
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       22 2017-05-20 19:17:24.000000 artifacts-20230723/config/dpkg/clean
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)        2 2023-04-30 05:13:17.000000 artifacts-20230723/config/dpkg/compat
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1304 2023-04-30 05:13:17.000000 artifacts-20230723/config/dpkg/control
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)     1017 2017-05-13 17:01:46.000000 artifacts-20230723/config/dpkg/copyright
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       99 2017-05-20 19:17:24.000000 artifacts-20230723/config/dpkg/python3-artifacts.install
+-rwxrwxr-x   0 lordyesta  (1000) lordyesta  (1000)      122 2023-04-30 05:13:17.000000 artifacts-20230723/config/dpkg/rules
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.782227 artifacts-20230723/config/dpkg/source/
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       12 2017-05-20 19:17:24.000000 artifacts-20230723/config/dpkg/source/format
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.797227 artifacts-20230723/data/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     6762 2022-12-20 18:52:11.000000 artifacts-20230723/data/antivirus.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     4248 2022-12-20 18:52:11.000000 artifacts-20230723/data/applications.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2787 2022-12-20 18:52:11.000000 artifacts-20230723/data/cloud_services.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1664 2022-12-20 18:52:11.000000 artifacts-20230723/data/config_files.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      812 2022-12-20 18:52:11.000000 artifacts-20230723/data/containerd.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     6324 2022-12-20 18:52:11.000000 artifacts-20230723/data/database_servers.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      522 2022-12-20 18:52:11.000000 artifacts-20230723/data/docker.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     3602 2022-12-20 18:52:11.000000 artifacts-20230723/data/esxi.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1030 2022-12-20 18:52:11.000000 artifacts-20230723/data/file_systems.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1258 2022-12-20 18:52:11.000000 artifacts-20230723/data/hadoop.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      838 2023-01-30 17:22:48.000000 artifacts-20230723/data/ics.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1958 2022-12-20 18:52:11.000000 artifacts-20230723/data/installed_module_paths.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5243 2022-12-20 18:52:11.000000 artifacts-20230723/data/installed_modules.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2316 2023-01-30 17:22:48.000000 artifacts-20230723/data/instant_messaging.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      558 2022-12-20 18:52:11.000000 artifacts-20230723/data/java.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5174 2022-12-20 18:52:11.000000 artifacts-20230723/data/kaspersky_careto.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5223 2022-12-20 18:52:11.000000 artifacts-20230723/data/kubernetes.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2743 2022-12-20 18:52:11.000000 artifacts-20230723/data/legacy.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    24969 2023-07-23 09:17:05.000000 artifacts-20230723/data/linux.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5117 2022-12-20 18:52:11.000000 artifacts-20230723/data/linux_proc.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1221 2022-12-20 18:52:11.000000 artifacts-20230723/data/linux_services.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    27748 2023-01-30 17:22:48.000000 artifacts-20230723/data/macos.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     8373 2022-12-20 18:52:11.000000 artifacts-20230723/data/shell.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     4201 2022-12-20 18:52:11.000000 artifacts-20230723/data/tomcat.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     8988 2022-12-20 18:52:11.000000 artifacts-20230723/data/triage.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2855 2023-07-23 09:17:05.000000 artifacts-20230723/data/unix_common.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      892 2023-01-30 17:22:48.000000 artifacts-20230723/data/user.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    73282 2023-07-23 09:17:05.000000 artifacts-20230723/data/webbrowser.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2884 2022-12-20 18:52:11.000000 artifacts-20230723/data/webservers.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)   167703 2023-07-23 09:45:44.000000 artifacts-20230723/data/windows.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     6174 2022-12-20 18:52:11.000000 artifacts-20230723/data/windows_dll_hijacking.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     8549 2022-12-20 18:52:11.000000 artifacts-20230723/data/wmi.yaml
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)      150 2021-11-01 18:53:11.000000 artifacts-20230723/dependencies.ini
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.810227 artifacts-20230723/docs/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)       88 2022-12-20 18:52:11.000000 artifacts-20230723/docs/Artifacts definition format and style guide.asciidoc
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5127 2023-04-30 05:13:17.000000 artifacts-20230723/docs/conf.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      673 2022-12-20 18:52:11.000000 artifacts-20230723/docs/index.rst
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      105 2023-04-30 05:13:29.000000 artifacts-20230723/docs/requirements.txt
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.810227 artifacts-20230723/docs/sources/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    15892 2022-12-20 18:52:11.000000 artifacts-20230723/docs/sources/Format-specification.md
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.811227 artifacts-20230723/docs/sources/api/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1176 2022-12-20 18:52:11.000000 artifacts-20230723/docs/sources/api/artifacts.rst
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)       64 2022-12-20 18:52:11.000000 artifacts-20230723/docs/sources/api/modules.rst
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.811227 artifacts-20230723/docs/sources/background/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      726 2023-07-23 09:45:44.000000 artifacts-20230723/docs/sources/background/Stats.md
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      873 2022-12-20 18:52:11.000000 artifacts-20230723/docs/sources/background/Terminology.md
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1276 2022-12-20 18:52:11.000000 artifacts-20230723/docs/sources/background/index.rst
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.811227 artifacts-20230723/docs/sources/user/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1703 2022-12-20 18:52:11.000000 artifacts-20230723/docs/sources/user/Installation-instructions.md
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      311 2022-12-20 18:52:11.000000 artifacts-20230723/docs/sources/user/index.rst
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       28 2023-04-30 05:13:17.000000 artifacts-20230723/requirements.txt
+-rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)     1018 2022-12-20 18:52:11.000000 artifacts-20230723/run_tests.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)      320 2023-07-23 09:46:57.870227 artifacts-20230723/setup.cfg
+-rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)     7313 2023-04-30 05:13:17.000000 artifacts-20230723/setup.py
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.812227 artifacts-20230723/test_data/
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2422 2022-12-20 18:52:11.000000 artifacts-20230723/test_data/definitions.json
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     2312 2022-12-20 18:52:11.000000 artifacts-20230723/test_data/definitions.yaml
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)        0 2022-12-20 18:52:11.000000 artifacts-20230723/test_dependencies.ini
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)        0 2023-04-30 05:13:17.000000 artifacts-20230723/test_requirements.txt
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.825227 artifacts-20230723/tests/
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       24 2021-11-01 18:53:11.000000 artifacts-20230723/tests/__init__.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    11907 2022-12-20 18:52:11.000000 artifacts-20230723/tests/reader_test.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     4906 2022-12-20 18:52:11.000000 artifacts-20230723/tests/registry_test.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     5365 2022-12-20 18:52:11.000000 artifacts-20230723/tests/source_type_test.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1720 2022-12-20 18:52:11.000000 artifacts-20230723/tests/test_lib.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1135 2022-12-20 18:52:11.000000 artifacts-20230723/tests/validator_test.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1837 2022-12-20 18:52:11.000000 artifacts-20230723/tests/writer_test.py
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.832227 artifacts-20230723/tools/
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)       46 2021-11-01 18:53:12.000000 artifacts-20230723/tools/__init__.py
+-rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)     3740 2022-12-20 18:52:11.000000 artifacts-20230723/tools/stats.py
+-rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)    21201 2022-12-20 18:52:11.000000 artifacts-20230723/tools/validator.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)     1257 2023-04-30 05:13:17.000000 artifacts-20230723/tox.ini
+drwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)        0 2023-07-23 09:46:57.868227 artifacts-20230723/utils/
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)        0 2018-03-18 07:06:41.000000 artifacts-20230723/utils/__init__.py
+-rwxrwxr-x   0 lordyesta  (1000) lordyesta  (1000)      422 2023-04-30 05:13:17.000000 artifacts-20230723/utils/check_dependencies.py
+-rw-r--r--   0 lordyesta  (1000) lordyesta  (1000)    11583 2023-04-30 05:13:17.000000 artifacts-20230723/utils/dependencies.py
+-rw-rw-r--   0 lordyesta  (1000) lordyesta  (1000)     9073 2015-05-07 21:05:55.000000 artifacts-20230723/utils/pylintrc
+-rwxr-xr-x   0 lordyesta  (1000) lordyesta  (1000)      675 2022-12-20 18:52:11.000000 artifacts-20230723/utils/update_release.sh
```

### Comparing `artifacts-20230413/.github/workflows/test_docker.yml` & `artifacts-20230723/.github/workflows/test_docker.yml`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 on: [push]
 permissions: read-all
 jobs:
   test_fedora:
     runs-on: ubuntu-latest
     strategy:
       matrix:
-        version: ['37']
+        version: ['38']
     container:
       image: registry.fedoraproject.org/fedora:${{ matrix.version }}
     steps:
     - uses: actions/checkout@v3
     - name: Set up container
       run: |
         dnf install -y dnf-plugins-core langpacks-en
```

### Comparing `artifacts-20230413/.github/workflows/test_docs.yml` & `artifacts-20230723/.github/workflows/test_docs.yml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/.github/workflows/test_tox.yml` & `artifacts-20230723/.github/workflows/test_tox.yml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/.pylintrc` & `artifacts-20230723/.pylintrc`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/LICENSE` & `artifacts-20230723/LICENSE`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/MANIFEST.in` & `artifacts-20230723/MANIFEST.in`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/PKG-INFO` & `artifacts-20230723/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: artifacts
-Version: 20230413
+Version: 20230723
 Summary: ForensicArtifacts.com Artifact Repository.
 Home-page: https://github.com/ForensicArtifacts/artifacts
 Maintainer: Forensic artifacts
 Maintainer-email: forensicartifacts@googlegroups.com
 License: Apache License, Version 2.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Environment :: Console
```

### Comparing `artifacts-20230413/README.md` & `artifacts-20230723/README.md`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/appveyor.yml` & `artifacts-20230723/appveyor.yml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/artifacts/artifact.py` & `artifacts-20230723/artifacts/artifact.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/artifacts/definitions.py` & `artifacts-20230723/artifacts/definitions.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/artifacts/reader.py` & `artifacts-20230723/artifacts/reader.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/artifacts/registry.py` & `artifacts-20230723/artifacts/registry.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/artifacts/source_type.py` & `artifacts-20230723/artifacts/source_type.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/artifacts/writer.py` & `artifacts-20230723/artifacts/writer.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/artifacts.egg-info/PKG-INFO` & `artifacts-20230723/artifacts.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: artifacts
-Version: 20230413
+Version: 20230723
 Summary: ForensicArtifacts.com Artifact Repository.
 Home-page: https://github.com/ForensicArtifacts/artifacts
 Maintainer: Forensic artifacts
 Maintainer-email: forensicartifacts@googlegroups.com
 License: Apache License, Version 2.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Environment :: Console
```

### Comparing `artifacts-20230413/artifacts.egg-info/SOURCES.txt` & `artifacts-20230723/artifacts.egg-info/SOURCES.txt`

 * *Files 5% similar despite different names*

```diff
@@ -42,15 +42,14 @@
 config/dpkg/clean
 config/dpkg/compat
 config/dpkg/control
 config/dpkg/copyright
 config/dpkg/python3-artifacts.install
 config/dpkg/rules
 config/dpkg/source/format
-data/.windows.yaml.swp
 data/antivirus.yaml
 data/applications.yaml
 data/cloud_services.yaml
 data/config_files.yaml
 data/containerd.yaml
 data/database_servers.yaml
 data/docker.yaml
```

### Comparing `artifacts-20230413/artifacts.ini` & `artifacts-20230723/artifacts.ini`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/config/appveyor/install.ps1` & `artifacts-20230723/config/appveyor/install.ps1`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/config/appveyor/runtests.sh` & `artifacts-20230723/config/appveyor/runtests.sh`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/config/dpkg/control` & `artifacts-20230723/config/dpkg/control`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/config/dpkg/copyright` & `artifacts-20230723/config/dpkg/copyright`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/antivirus.yaml` & `artifacts-20230723/data/antivirus.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/applications.yaml` & `artifacts-20230723/data/applications.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/cloud_services.yaml` & `artifacts-20230723/data/cloud_services.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/config_files.yaml` & `artifacts-20230723/data/config_files.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/containerd.yaml` & `artifacts-20230723/data/containerd.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/database_servers.yaml` & `artifacts-20230723/data/database_servers.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/docker.yaml` & `artifacts-20230723/data/docker.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/esxi.yaml` & `artifacts-20230723/data/esxi.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/file_systems.yaml` & `artifacts-20230723/data/file_systems.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/hadoop.yaml` & `artifacts-20230723/data/hadoop.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/ics.yaml` & `artifacts-20230723/data/ics.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/installed_module_paths.yaml` & `artifacts-20230723/data/installed_module_paths.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/installed_modules.yaml` & `artifacts-20230723/data/installed_modules.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/instant_messaging.yaml` & `artifacts-20230723/data/instant_messaging.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/java.yaml` & `artifacts-20230723/data/java.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/kaspersky_careto.yaml` & `artifacts-20230723/data/kaspersky_careto.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/kubernetes.yaml` & `artifacts-20230723/data/kubernetes.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/legacy.yaml` & `artifacts-20230723/data/legacy.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/linux.yaml` & `artifacts-20230723/data/linux.yaml`

 * *Files 0% similar despite different names*

```diff
@@ -559,15 +559,15 @@
 urls:
 - 'https://man7.org/linux/man-pages/man5/sysctl.conf.5.html'
 ---
 name: LinuxSysLogFiles
 doc: Linux syslog log files.
 sources:
 - type: FILE
-  attributes: {paths: ['/var/log/syslog.log*']}
+  attributes: {paths: ['/var/log/syslog*']}
 supported_os: [Linux]
 ---
 name: LinuxSyslogNgConfigs
 doc: Linux syslog-ng configurations.
 sources:
 - type: FILE
   attributes:
```

### Comparing `artifacts-20230413/data/linux_proc.yaml` & `artifacts-20230723/data/linux_proc.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/linux_services.yaml` & `artifacts-20230723/data/linux_services.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/macos.yaml` & `artifacts-20230723/data/macos.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/shell.yaml` & `artifacts-20230723/data/shell.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/tomcat.yaml` & `artifacts-20230723/data/tomcat.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/triage.yaml` & `artifacts-20230723/data/triage.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/unix_common.yaml` & `artifacts-20230723/data/unix_common.yaml`

 * *Files 2% similar despite different names*

```diff
@@ -55,14 +55,26 @@
   attributes: {paths: ['/etc/shadow']}
   supported_os: [Darwin, Linux]
 - type: FILE
   attributes: {paths: ['/private/etc/shadow']}
   supported_os: [Darwin]
 supported_os: [Darwin, Linux]
 ---
+name: UnixShadowBackupFile
+doc: Unix shadow backup file.
+sources:
+- type: FILE
+  attributes: {paths: ['/etc/shadow-']}
+  supported_os: [Darwin, Linux]
+- type: FILE
+  attributes: {paths: ['/private/etc/shadow-']}
+  supported_os: [Darwin]
+supported_os: [Darwin, Linux]
+urls: ['https://man7.org/linux/man-pages/man5/shadow.5.html']
+---
 name: UnixSudoersConfigurationFile
 aliases: [UnixSudoersConfiguration]
 doc: Unix sudoers configuration file.
 sources:
 - type: FILE
   attributes: {paths: ['/etc/sudoers']}
   supported_os: [Darwin, Linux]
```

### Comparing `artifacts-20230413/data/user.yaml` & `artifacts-20230723/data/user.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/webbrowser.yaml` & `artifacts-20230723/data/webbrowser.yaml`

 * *Files 2% similar despite different names*

```diff
@@ -923,14 +923,18 @@
 - type: FILE
   attributes:
     paths:
     - '%%users.homedir%%/Library/Caches/Firefox/Profiles/*.default/Cache/*'
     - '%%users.homedir%%/Library/Caches/Firefox/Profiles/*.default/cache2/*'
     - '%%users.homedir%%/Library/Caches/Firefox/Profiles/*.default/cache2/doomed/*'
     - '%%users.homedir%%/Library/Caches/Firefox/Profiles/*.default/cache2/entries/*'
+    - '%%users.homedir%%/Library/Caches/Firefox/Profiles/*.default-*/Cache/*'
+    - '%%users.homedir%%/Library/Caches/Firefox/Profiles/*.default-*/cache2/*'
+    - '%%users.homedir%%/Library/Caches/Firefox/Profiles/*.default-*/cache2/doomed/*'
+    - '%%users.homedir%%/Library/Caches/Firefox/Profiles/*.default-*/cache2/entries/*'
   supported_os: [Darwin]
 - type: FILE
   attributes:
     paths:
     - '%%users.homedir%%/.mozilla/firefox/*.default/Cache/*'
     - '%%users.homedir%%/.cache/mozilla/firefox/*.default/Cache/*'
     - '%%users.homedir%%/.cache/mozilla/firefox/*.default/cache2/*'
@@ -961,14 +965,42 @@
     - '%%users.localappdata%%\Mozilla\Firefox\Profiles\*.default-*\cache2\doomed\*'
     - '%%users.localappdata%%\Mozilla\Firefox\Profiles\*.default-*\cache2\entries\*'
     separator: '\'
   supported_os: [Windows]
 supported_os: [Darwin, Linux, Windows]
 urls: ['https://artifacts-kb.readthedocs.io/en/latest/sources/webbrowser/FirefoxCache.html']
 ---
+name: FirefoxCookies
+doc: Firefox browser cookies (cookies.sqlite).
+sources:
+- type: FILE
+  attributes:
+    paths:
+    - '%%users.homedir%%/Library/Application Support/Firefox/Profiles/*/cookies.sqlite'
+    - '%%users.homedir%%/Library/Application Support/Firefox/Profiles/*/cookies.sqlite-wal'
+  supported_os: [Darwin]
+- type: FILE
+  attributes:
+    paths:
+    - '%%users.homedir%%/.mozilla/firefox/*/cookies.sqlite'
+    - '%%users.homedir%%/.mozilla/firefox/*/cookies.sqlite-shm'
+    - '%%users.homedir%%/.mozilla/firefox/*/cookies.sqlite-wal'
+  supported_os: [Linux]
+- type: FILE
+  attributes:
+    paths:
+    - '%%users.localappdata%%\Mozilla\Firefox\Profiles\*\cookies.sqlite'
+    - '%%users.localappdata%%\Mozilla\Firefox\Profiles\*\cookies.sqlite-wal'
+    - '%%users.appdata%%\Mozilla\Firefox\Profiles\*\cookies.sqlite'
+    - '%%users.localappdata%%\Mozilla\Firefox\Profiles\*\cookies.sqlite-wal'
+    separator: '\'
+  supported_os: [Windows]
+supported_os: [Darwin, Linux, Windows]
+urls: ['https://forensics.wiki/mozilla_firefox']
+---
 name: FirefoxDownloads
 doc: Firefox browser downloads (downloads.sqlite).
 sources:
 - type: FILE
   attributes:
     paths:
     - '%%users.homedir%%/Library/Application Support/Firefox/Profiles/*/downloads.sqlite'
@@ -1235,23 +1267,36 @@
 doc: Safari browser cache (cache.db) SQLite database file.
 sources:
 - type: FILE
   attributes:
     paths:
     - '%%users.homedir%%/Library/Caches/com.apple.Safari/Cache.db'
     - '%%users.homedir%%/Library/Caches/com.apple.Safari/Cache.db-wal'
+    - '%%users.homedir%%/Library/Containers/com.apple.Safari/Data/Library/Caches/com.apple.Safari/Cache.db'
+    - '%%users.homedir%%/Library/Containers/com.apple.Safari/Data/Library/Caches/com.apple.Safari/Cache.db-wal'
   supported_os: [Darwin]
 - type: FILE
   attributes:
     paths: ['%%users.localappdata%%\Apple Computer\Safari\cache.db']
     separator: '\'
   supported_os: [Windows]
 supported_os: [Darwin, Windows]
 urls: ['https://forensics.wiki/apple_safari']
 ---
+name: SafariCookies
+doc: Safari Cookies database.
+sources:
+- type: FILE
+  attributes:
+    paths:
+    - '%%users.homedir%%/Library/Cookies/Cookies.binarycookies'
+    - '%%users.homedir%%/Library/Containers/com.apple.Safari/Data/Library/Cookies/Cookies.binarycookies'
+  supported_os: [Darwin]
+supported_os: [Darwin]
+---
 name: SafariDownloadsPlistFile
 aliases: [SafariDownloads]
 doc: Safari downloads history (Downloads.plist) property list (plist) file.
 sources:
 - type: FILE
   attributes: {paths: ['%%users.homedir%%/Library/Safari/Downloads.plist']}
   supported_os: [Darwin]
```

### Comparing `artifacts-20230413/data/webservers.yaml` & `artifacts-20230723/data/webservers.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/windows.yaml` & `artifacts-20230723/data/windows.yaml`

 * *Files 0% similar despite different names*

```diff
@@ -2906,19 +2906,19 @@
 ---
 name: WindowsSystemRegistryFiles
 doc: Windows system Registry files.
 sources:
 - type: FILE
   attributes:
     paths:
+    - '%%environ_systemdrive%%\System Volume Information\Syscache.hve'
     - '%%environ_systemroot%%\System32\config\SAM'
     - '%%environ_systemroot%%\System32\config\SECURITY'
     - '%%environ_systemroot%%\System32\config\SOFTWARE'
     - '%%environ_systemroot%%\System32\config\SYSTEM'
-    - '\System Volume Information\Syscache.hve'
     separator: '\'
 supported_os: [Windows]
 urls: ['https://artifacts-kb.readthedocs.io/en/latest/sources/windows/RegistryFiles.html']
 ---
 name: WindowsSystemRegistryTransactionLogFiles
 doc: Windows system Registry transaction log files.
 sources:
```

### Comparing `artifacts-20230413/data/windows_dll_hijacking.yaml` & `artifacts-20230723/data/windows_dll_hijacking.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/data/wmi.yaml` & `artifacts-20230723/data/wmi.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/docs/conf.py` & `artifacts-20230723/docs/conf.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/docs/index.rst` & `artifacts-20230723/docs/index.rst`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/docs/sources/Format-specification.md` & `artifacts-20230723/docs/sources/Format-specification.md`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/docs/sources/api/artifacts.rst` & `artifacts-20230723/docs/sources/api/artifacts.rst`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/docs/sources/background/Stats.md` & `artifacts-20230723/docs/sources/background/Stats.md`

 * *Files 6% similar despite different names*

```diff
@@ -1,34 +1,34 @@
 ## Statistics
 
 The artifact definitions can be found in the
 [data directory](https://github.com/ForensicArtifacts/artifacts/tree/main/data) and the format is described in detail
 in the [Style Guide](https://artifacts.readthedocs.io/en/latest/sources/Format-specification.html).
 
-Status of the repository as of 2023-04-13
+Status of the repository as of 2023-07-23
 
 Description | Number
 --- | ---
-Number of artifact definitions: | 757
-Number of file paths: | 1970
+Number of artifact definitions: | 763
+Number of file paths: | 1989
 Number of Windows Registry key paths: | 677
 
 ### Artifact definition source types
 
 Identifier | Number
 --- | ---
 ARTIFACT_GROUP | 47
 COMMAND | 10
-FILE | 472
+FILE | 478
 PATH | 28
 REGISTRY_KEY | 57
 REGISTRY_VALUE | 116
 WMI | 27
 
 ### Operating systems
 
 Identifier | Number
 --- | ---
-Darwin | 72
-Linux | 68
-Windows | 58
+Darwin | 76
+Linux | 70
+Windows | 59
```

### Comparing `artifacts-20230413/docs/sources/background/Terminology.md` & `artifacts-20230723/docs/sources/background/Terminology.md`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/docs/sources/background/index.rst` & `artifacts-20230723/docs/sources/background/index.rst`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/docs/sources/user/Installation-instructions.md` & `artifacts-20230723/docs/sources/user/Installation-instructions.md`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/run_tests.py` & `artifacts-20230723/run_tests.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/setup.py` & `artifacts-20230723/setup.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/test_data/definitions.json` & `artifacts-20230723/test_data/definitions.json`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/test_data/definitions.yaml` & `artifacts-20230723/test_data/definitions.yaml`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/tests/reader_test.py` & `artifacts-20230723/tests/reader_test.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/tests/registry_test.py` & `artifacts-20230723/tests/registry_test.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/tests/source_type_test.py` & `artifacts-20230723/tests/source_type_test.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/tests/test_lib.py` & `artifacts-20230723/tests/test_lib.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/tests/validator_test.py` & `artifacts-20230723/tests/validator_test.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/tests/writer_test.py` & `artifacts-20230723/tests/writer_test.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/tools/stats.py` & `artifacts-20230723/tools/stats.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/tools/validator.py` & `artifacts-20230723/tools/validator.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/tox.ini` & `artifacts-20230723/tox.ini`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/utils/dependencies.py` & `artifacts-20230723/utils/dependencies.py`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/utils/pylintrc` & `artifacts-20230723/utils/pylintrc`

 * *Files identical despite different names*

### Comparing `artifacts-20230413/utils/update_release.sh` & `artifacts-20230723/utils/update_release.sh`

 * *Files identical despite different names*

