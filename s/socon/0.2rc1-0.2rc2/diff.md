# Comparing `tmp/socon-0.2rc1.tar.gz` & `tmp/socon-0.2rc2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "socon-0.2rc1.tar", last modified: Sun Jul 23 13:12:12 2023, max compression
+gzip compressed data, was "socon-0.2rc2.tar", last modified: Sun Jul 23 16:48:49 2023, max compression
```

## Comparing `socon-0.2rc1.tar` & `socon-0.2rc2.tar`

### file list

```diff
@@ -1,294 +1,294 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.321789 socon-0.2rc1/
--rw-rw-rw-   0        0        0      206 2023-07-15 18:49:23.000000 socon-0.2rc1/.coveragerc
--rw-rw-rw-   0        0        0       87 2023-03-14 20:24:24.000000 socon-0.2rc1/.gitattributes
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.242290 socon-0.2rc1/.github/
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.393287 socon-0.2rc1/.github/workflows/
--rw-rw-rw-   0        0        0     1079 2023-03-09 17:46:46.000000 socon-0.2rc1/.github/workflows/coverage.yml
--rw-rw-rw-   0        0        0      747 2023-03-03 16:16:37.000000 socon-0.2rc1/.github/workflows/docs.yml
--rw-rw-rw-   0        0        0     1110 2023-03-05 23:21:53.000000 socon-0.2rc1/.github/workflows/linters.yml
--rw-rw-rw-   0        0        0      959 2023-03-05 23:21:53.000000 socon-0.2rc1/.github/workflows/tests.yml
--rw-rw-rw-   0        0        0      950 2023-03-14 20:24:24.000000 socon-0.2rc1/.gitignore
--rw-rw-rw-   0        0        0      709 2023-07-22 17:41:15.000000 socon-0.2rc1/.pre-commit-config.yaml
--rw-rw-rw-   0        0        0       71 2023-07-15 18:49:23.000000 socon-0.2rc1/AUTHORS
--rw-rw-rw-   0        0        0     5352 2023-03-05 10:52:09.000000 socon-0.2rc1/CODE_OF_CONDUCT.md
--rw-rw-rw-   0        0        0    10127 2023-03-14 20:24:24.000000 socon-0.2rc1/CONTRIBUTING.rst
--rw-rw-rw-   0        0        0     1556 2023-03-14 20:24:24.000000 socon-0.2rc1/LICENSE
--rw-rw-rw-   0        0        0     7378 2023-07-23 13:12:12.317789 socon-0.2rc1/PKG-INFO
--rw-rw-rw-   0        0        0     6178 2023-07-15 18:52:40.000000 socon-0.2rc1/README.rst
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.442788 socon-0.2rc1/docs/
--rw-rw-rw-   0        0        0      654 2023-03-03 16:15:01.000000 socon-0.2rc1/docs/Makefile
--rw-rw-rw-   0        0        0      858 2023-03-03 16:15:28.000000 socon-0.2rc1/docs/README.rst
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.447289 socon-0.2rc1/docs/_ext/
--rw-rw-rw-   0        0        0      724 2023-03-05 10:49:33.000000 socon-0.2rc1/docs/_ext/socondoc.py
--rw-rw-rw-   0        0        0     3976 2023-07-23 13:05:46.000000 socon-0.2rc1/docs/conf.py
--rw-rw-rw-   0        0        0      344 2023-03-03 16:16:32.000000 socon-0.2rc1/docs/contents.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.462788 socon-0.2rc1/docs/how-to/
--rw-rw-rw-   0        0        0    18633 2023-07-21 19:23:29.000000 socon-0.2rc1/docs/how-to/custom-commands.txt
--rw-rw-rw-   0        0        0    11457 2023-07-21 19:23:29.000000 socon-0.2rc1/docs/how-to/custom-managers-and-hooks.txt
--rw-rw-rw-   0        0        0      185 2023-03-05 17:30:59.000000 socon-0.2rc1/docs/how-to/index.txt
--rw-rw-rw-   0        0        0     2836 2023-03-05 16:48:03.000000 socon-0.2rc1/docs/index.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.490787 socon-0.2rc1/docs/internals/
--rw-rw-rw-   0        0        0     3205 2023-07-23 13:03:02.000000 socon-0.2rc1/docs/internals/changelog.txt
--rw-rw-rw-   0        0        0     2885 2023-03-14 20:24:24.000000 socon-0.2rc1/docs/internals/coding-style.txt
--rw-rw-rw-   0        0        0       58 2023-03-14 20:24:24.000000 socon-0.2rc1/docs/internals/contributing.txt
--rw-rw-rw-   0        0        0      450 2023-03-03 17:12:46.000000 socon-0.2rc1/docs/internals/deprecations.txt
--rw-rw-rw-   0        0        0      282 2023-03-03 16:16:32.000000 socon-0.2rc1/docs/internals/index.txt
--rw-rw-rw-   0        0        0     3020 2023-03-03 17:24:11.000000 socon-0.2rc1/docs/internals/release-process.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.513287 socon-0.2rc1/docs/intro/
--rw-rw-rw-   0        0        0     2714 2023-03-04 16:09:31.000000 socon-0.2rc1/docs/intro/environment.txt
--rw-rw-rw-   0        0        0      279 2023-03-04 10:06:27.000000 socon-0.2rc1/docs/intro/index.txt
--rw-rw-rw-   0        0        0     2883 2023-03-05 16:46:16.000000 socon-0.2rc1/docs/intro/install.txt
--rw-rw-rw-   0        0        0     2263 2023-03-04 10:07:25.000000 socon-0.2rc1/docs/intro/overview.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.535789 socon-0.2rc1/docs/intro/tutorials/
--rw-rw-rw-   0        0        0    19350 2023-07-15 18:49:23.000000 socon-0.2rc1/docs/intro/tutorials/1_project_and_command.txt
--rw-rw-rw-   0        0        0     3772 2023-03-09 21:40:52.000000 socon-0.2rc1/docs/intro/tutorials/2_change_behavior.txt
--rw-rw-rw-   0        0        0     8150 2023-07-15 18:49:23.000000 socon-0.2rc1/docs/intro/tutorials/3_manager.txt
--rw-rw-rw-   0        0        0     6099 2023-07-15 18:49:23.000000 socon-0.2rc1/docs/intro/tutorials/4_plugins.txt
--rw-rw-rw-   0        0        0      372 2023-03-04 10:17:03.000000 socon-0.2rc1/docs/intro/tutorials/index.txt
--rwxrwxrwx   0        0        0      795 2023-03-03 16:15:01.000000 socon-0.2rc1/docs/make.bat
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.609787 socon-0.2rc1/docs/ref/
--rw-rw-rw-   0        0        0     8182 2023-07-21 19:23:29.000000 socon-0.2rc1/docs/ref/commands.txt
--rw-rw-rw-   0        0        0     1577 2023-07-15 18:49:23.000000 socon-0.2rc1/docs/ref/exceptions.txt
--rw-rw-rw-   0        0        0      346 2023-03-03 16:16:32.000000 socon-0.2rc1/docs/ref/index.txt
--rw-rw-rw-   0        0        0     4653 2023-03-04 16:09:31.000000 socon-0.2rc1/docs/ref/list-of-settings.txt
--rw-rw-rw-   0        0        0     1537 2023-03-03 16:16:21.000000 socon-0.2rc1/docs/ref/logging.txt
--rw-rw-rw-   0        0        0     4567 2023-07-15 18:49:23.000000 socon-0.2rc1/docs/ref/manager.txt
--rw-rw-rw-   0        0        0    15314 2023-03-09 21:40:52.000000 socon-0.2rc1/docs/ref/registry.txt
--rw-rw-rw-   0        0        0     5331 2023-03-09 21:40:52.000000 socon-0.2rc1/docs/ref/settings.txt
--rw-rw-rw-   0        0        0     9757 2023-07-15 18:49:23.000000 socon-0.2rc1/docs/ref/socon-admin.txt
--rw-rw-rw-   0        0        0     3755 2023-07-21 19:23:29.000000 socon-0.2rc1/docs/ref/terminal.txt
--rw-rw-rw-   0        0        0     3169 2023-07-15 18:49:23.000000 socon-0.2rc1/docs/ref/utils.txt
--rw-rw-rw-   0        0        0       63 2023-03-03 16:16:32.000000 socon-0.2rc1/docs/requirements.txt
--rw-rw-rw-   0        0        0      604 2023-07-23 13:03:26.000000 socon-0.2rc1/docs/spelling_wordlist
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.632287 socon-0.2rc1/licenses/
--rw-rw-rw-   0        0        0     1579 2023-03-14 20:24:24.000000 socon-0.2rc1/licenses/LicenseRef-BSD3-Clause-Django.txt
--rw-rw-rw-   0        0        0     1112 2023-03-14 20:24:24.000000 socon-0.2rc1/licenses/LicenseRef-MIT-Pytest.txt
--rw-rw-rw-   0        0        0     1509 2023-07-23 08:42:30.000000 socon-0.2rc1/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 13:12:12.321789 socon-0.2rc1/setup.cfg
--rw-rw-rw-   0        0        0       73 2023-03-03 16:16:34.000000 socon-0.2rc1/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.640788 socon-0.2rc1/socon/
--rw-rw-rw-   0        0        0     1380 2023-07-23 13:04:58.000000 socon-0.2rc1/socon/__init__.py
--rw-rw-rw-   0        0        0      239 2023-03-05 10:41:34.000000 socon-0.2rc1/socon/__main__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.667288 socon-0.2rc1/socon/conf/
--rw-rw-rw-   0        0        0    10683 2023-03-03 16:16:34.000000 socon-0.2rc1/socon/conf/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.253789 socon-0.2rc1/socon/conf/basecommand_template/
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.254290 socon-0.2rc1/socon/conf/basecommand_template/management/
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.671286 socon-0.2rc1/socon/conf/basecommand_template/management/commands/
--rw-rw-rw-   0        0        0     1069 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/conf/basecommand_template/management/commands/basecommand_name.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.675287 socon-0.2rc1/socon/conf/container_template/
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.681788 socon-0.2rc1/socon/conf/container_template/container_name/
--rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/conf/container_template/container_name/__init__.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.686288 socon-0.2rc1/socon/conf/container_template/container_name/management/
--rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/conf/container_template/container_name/management/__init__.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.688288 socon-0.2rc1/socon/conf/container_template/container_name/management/commands/
--rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/conf/container_template/container_name/management/commands/__init__.py-tpl
--rw-rw-rw-   0        0        0      773 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/conf/container_template/container_name/settings.py-tpl
--rw-rw-rw-   0        0        0      694 2023-03-03 16:15:57.000000 socon-0.2rc1/socon/conf/container_template/manage.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.690288 socon-0.2rc1/socon/conf/container_template/projects/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:15:30.000000 socon-0.2rc1/socon/conf/container_template/projects/__init__.py-tpl
--rw-rw-rw-   0        0        0     1180 2023-03-03 16:16:34.000000 socon-0.2rc1/socon/conf/global_settings.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.695789 socon-0.2rc1/socon/conf/plugin_template/
--rw-rw-rw-   0        0        0       91 2023-03-03 16:16:21.000000 socon-0.2rc1/socon/conf/plugin_template/README.rst-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.702288 socon-0.2rc1/socon/conf/plugin_template/plugin_name/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:15:51.000000 socon-0.2rc1/socon/conf/plugin_template/plugin_name/__init__.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.706288 socon-0.2rc1/socon/conf/plugin_template/plugin_name/management/
--rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/conf/plugin_template/plugin_name/management/__init__.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.708288 socon-0.2rc1/socon/conf/plugin_template/plugin_name/management/commands/
--rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/conf/plugin_template/plugin_name/management/commands/__init__.py-tpl
--rw-rw-rw-   0        0        0      146 2023-03-03 16:16:15.000000 socon-0.2rc1/socon/conf/plugin_template/plugin_name/plugins.py-tpl
--rw-rw-rw-   0        0        0      313 2023-03-03 16:16:25.000000 socon-0.2rc1/socon/conf/plugin_template/setup.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.712288 socon-0.2rc1/socon/conf/project_template/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:14:20.000000 socon-0.2rc1/socon/conf/project_template/__init__.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.718789 socon-0.2rc1/socon/conf/project_template/management/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:15:51.000000 socon-0.2rc1/socon/conf/project_template/management/__init__.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.722288 socon-0.2rc1/socon/conf/project_template/management/commands/
--rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/conf/project_template/management/commands/__init__.py-tpl
--rw-rw-rw-   0        0        0      267 2023-03-03 16:16:17.000000 socon-0.2rc1/socon/conf/project_template/management/config.py-tpl
--rw-rw-rw-   0        0        0      202 2023-03-03 16:15:55.000000 socon-0.2rc1/socon/conf/project_template/projects.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.265287 socon-0.2rc1/socon/conf/projectcommand_template/
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.265788 socon-0.2rc1/socon/conf/projectcommand_template/management/
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.724788 socon-0.2rc1/socon/conf/projectcommand_template/management/commands/
--rw-rw-rw-   0        0        0     1453 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/conf/projectcommand_template/management/commands/projectcommand_name.py-tpl
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.735788 socon-0.2rc1/socon/core/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:14:15.000000 socon-0.2rc1/socon/core/__init__.py
--rw-rw-rw-   0        0        0      574 2023-03-03 16:16:34.000000 socon-0.2rc1/socon/core/exceptions.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.759788 socon-0.2rc1/socon/core/management/
--rw-rw-rw-   0        0        0     9301 2023-07-21 19:23:29.000000 socon-0.2rc1/socon/core/management/__init__.py
--rw-rw-rw-   0        0        0    19678 2023-07-21 19:40:47.000000 socon-0.2rc1/socon/core/management/base.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.791288 socon-0.2rc1/socon/core/management/commands/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:15:01.000000 socon-0.2rc1/socon/core/management/commands/__init__.py
--rw-rw-rw-   0        0        0     3057 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/core/management/commands/check.py
--rw-rw-rw-   0        0        0     4868 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/core/management/commands/createcommand.py
--rw-rw-rw-   0        0        0      947 2023-03-03 16:16:34.000000 socon-0.2rc1/socon/core/management/commands/createcontainer.py
--rw-rw-rw-   0        0        0      936 2023-03-03 16:16:34.000000 socon-0.2rc1/socon/core/management/commands/createplugin.py
--rw-rw-rw-   0        0        0     2412 2023-05-04 09:58:38.000000 socon-0.2rc1/socon/core/management/commands/createproject.py
--rw-rw-rw-   0        0        0     3863 2023-07-21 19:23:29.000000 socon-0.2rc1/socon/core/management/subcommand.py
--rw-rw-rw-   0        0        0     6166 2023-07-15 20:06:51.000000 socon-0.2rc1/socon/core/management/templates.py
--rw-rw-rw-   0        0        0    12197 2023-07-15 21:29:48.000000 socon-0.2rc1/socon/core/manager.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.814789 socon-0.2rc1/socon/core/registry/
--rw-rw-rw-   0        0        0      137 2023-03-03 16:16:04.000000 socon-0.2rc1/socon/core/registry/__init__.py
--rw-rw-rw-   0        0        0     8043 2023-03-05 21:26:25.000000 socon-0.2rc1/socon/core/registry/base.py
--rw-rw-rw-   0        0        0    10082 2023-03-05 21:30:59.000000 socon-0.2rc1/socon/core/registry/config.py
--rw-rw-rw-   0        0        0     3495 2023-03-05 21:31:27.000000 socon-0.2rc1/socon/core/registry/core.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.823789 socon-0.2rc1/socon/test/
--rw-rw-rw-   0        0        0       56 2023-03-03 16:16:16.000000 socon-0.2rc1/socon/test/__init__.py
--rw-rw-rw-   0        0        0     3004 2023-04-30 13:24:41.000000 socon-0.2rc1/socon/test/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.853789 socon-0.2rc1/socon/utils/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:14:15.000000 socon-0.2rc1/socon/utils/__init__.py
--rw-rw-rw-   0        0        0     1007 2023-04-30 13:24:41.000000 socon-0.2rc1/socon/utils/func.py
--rw-rw-rw-   0        0        0      716 2023-03-03 16:16:34.000000 socon-0.2rc1/socon/utils/log.py
--rw-rw-rw-   0        0        0     1475 2023-03-03 16:16:34.000000 socon-0.2rc1/socon/utils/module_loading.py
--rw-rw-rw-   0        0        0     2468 2023-07-15 18:49:23.000000 socon-0.2rc1/socon/utils/reshape.py
--rw-rw-rw-   0        0        0    10157 2023-07-21 19:23:29.000000 socon-0.2rc1/socon/utils/terminal.py
--rw-rw-rw-   0        0        0     2556 2023-03-03 21:53:01.000000 socon-0.2rc1/socon/utils/version.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.659788 socon-0.2rc1/socon.egg-info/
--rw-rw-rw-   0        0        0     7378 2023-07-23 13:12:10.000000 socon-0.2rc1/socon.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     7902 2023-07-23 13:12:11.000000 socon-0.2rc1/socon.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 13:12:10.000000 socon-0.2rc1/socon.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       74 2023-07-23 13:12:10.000000 socon-0.2rc1/socon.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0        6 2023-07-23 13:12:10.000000 socon-0.2rc1/socon.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.870289 socon-0.2rc1/tests/
--rw-rw-rw-   0        0        0      561 2023-03-05 10:31:40.000000 socon-0.2rc1/tests/README.rst
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.879790 socon-0.2rc1/tests/admin_scripts/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:14:24.000000 socon-0.2rc1/tests/admin_scripts/__init__.py
--rw-rw-rw-   0        0        0      270 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/configured_settings_manage.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.273289 socon-0.2rc1/tests/admin_scripts/management/
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.902789 socon-0.2rc1/tests/admin_scripts/management/commands/
--rw-rw-rw-   0        0        0     1218 2023-03-03 16:16:36.000000 socon-0.2rc1/tests/admin_scripts/management/commands/base_command.py
--rw-rw-rw-   0        0        0      391 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/management/commands/custom_createcontainer.py
--rw-rw-rw-   0        0        0      324 2023-03-03 21:31:31.000000 socon-0.2rc1/tests/admin_scripts/management/commands/extras_args_command.py
--rw-rw-rw-   0        0        0      376 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/management/commands/noargs_command.py
--rw-rw-rw-   0        0        0      377 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/management/commands/project_commands.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.908789 socon-0.2rc1/tests/admin_scripts/project_with_command/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc1/tests/admin_scripts/project_with_command/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.912790 socon-0.2rc1/tests/admin_scripts/project_with_command/management/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc1/tests/admin_scripts/project_with_command/management/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.917289 socon-0.2rc1/tests/admin_scripts/project_with_command/management/commands/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc1/tests/admin_scripts/project_with_command/management/commands/__init__.py
--rw-rw-rw-   0        0        0      212 2023-04-30 13:24:41.000000 socon-0.2rc1/tests/admin_scripts/project_with_command/management/commands/simple_command.py
--rw-rw-rw-   0        0        0      149 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/project_with_command/projects.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.923287 socon-0.2rc1/tests/admin_scripts/project_with_error/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc1/tests/admin_scripts/project_with_error/__init__.py
--rw-rw-rw-   0        0        0      253 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/project_with_error/projects.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.937288 socon-0.2rc1/tests/admin_scripts/project_with_manager/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc1/tests/admin_scripts/project_with_manager/__init__.py
--rw-rw-rw-   0        0        0      150 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/project_with_manager/manager_error.py
--rw-rw-rw-   0        0        0      149 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/project_with_manager/managers.py
--rw-rw-rw-   0        0        0      149 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/project_with_manager/projects.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.943288 socon-0.2rc1/tests/admin_scripts/simple_project/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:15:04.000000 socon-0.2rc1/tests/admin_scripts/simple_project/__init__.py
--rw-rw-rw-   0        0        0      138 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/admin_scripts/simple_project/projects.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.949288 socon-0.2rc1/tests/admin_scripts/subcommands/
--rw-rw-rw-   0        0        0        0 2023-07-21 19:23:29.000000 socon-0.2rc1/tests/admin_scripts/subcommands/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.953287 socon-0.2rc1/tests/admin_scripts/subcommands/management/
--rw-rw-rw-   0        0        0        0 2023-07-21 19:23:29.000000 socon-0.2rc1/tests/admin_scripts/subcommands/management/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.962788 socon-0.2rc1/tests/admin_scripts/subcommands/management/commands/
--rw-rw-rw-   0        0        0        0 2023-07-21 19:23:29.000000 socon-0.2rc1/tests/admin_scripts/subcommands/management/commands/__init__.py
--rw-rw-rw-   0        0        0      164 2023-07-21 19:23:29.000000 socon-0.2rc1/tests/admin_scripts/subcommands/management/commands/command_with_subcommand.py
--rw-rw-rw-   0        0        0      157 2023-07-21 19:23:29.000000 socon-0.2rc1/tests/admin_scripts/subcommands/management/commands/no_subcommands.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.969288 socon-0.2rc1/tests/admin_scripts/subcommands/management/commands/subcommands/
--rw-rw-rw-   0        0        0        0 2023-07-21 19:23:29.000000 socon-0.2rc1/tests/admin_scripts/subcommands/management/commands/subcommands/__init__.py
--rw-rw-rw-   0        0        0      496 2023-07-21 19:23:29.000000 socon-0.2rc1/tests/admin_scripts/subcommands/management/commands/subcommands/sub.py
--rw-rw-rw-   0        0        0      232 2023-07-21 19:23:29.000000 socon-0.2rc1/tests/admin_scripts/subcommands/managers.py
--rw-rw-rw-   0        0        0    57311 2023-07-21 19:40:47.000000 socon-0.2rc1/tests/admin_scripts/tests.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.981789 socon-0.2rc1/tests/common/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:11.000000 socon-0.2rc1/tests/common/__init__.py
--rw-rw-rw-   0        0        0      178 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/common/lookup.py
--rw-rw-rw-   0        0        0      305 2023-03-03 16:16:11.000000 socon-0.2rc1/tests/common/settings.py
--rw-rw-rw-   0        0        0     3826 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/conftest.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:11.997789 socon-0.2rc1/tests/manager/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc1/tests/manager/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.004287 socon-0.2rc1/tests/manager/duplicate_hooks/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:19.000000 socon-0.2rc1/tests/manager/duplicate_hooks/__init__.py
--rw-rw-rw-   0        0        0      173 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/manager/duplicate_hooks/lookup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.010789 socon-0.2rc1/tests/manager/duplicate_managers/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc1/tests/manager/duplicate_managers/__init__.py
--rw-rw-rw-   0        0        0      208 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/manager/duplicate_managers/managers.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.016789 socon-0.2rc1/tests/manager/hook_not_linked/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:19.000000 socon-0.2rc1/tests/manager/hook_not_linked/__init__.py
--rw-rw-rw-   0        0        0      145 2023-03-03 16:16:19.000000 socon-0.2rc1/tests/manager/hook_not_linked/managers.py
--rw-rw-rw-   0        0        0      242 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/manager/lookup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.025788 socon-0.2rc1/tests/manager/manager_not_hooked/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:19.000000 socon-0.2rc1/tests/manager/manager_not_hooked/__init__.py
--rw-rw-rw-   0        0        0      147 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/manager/manager_not_hooked/managers.py
--rw-rw-rw-   0        0        0      100 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/manager/manager_not_hooked/not_hooked.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.033789 socon-0.2rc1/tests/manager/manager_with_abstract/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc1/tests/manager/manager_with_abstract/__init__.py
--rw-rw-rw-   0        0        0      210 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/manager/manager_with_abstract/lookup.py
--rw-rw-rw-   0        0        0      221 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/manager/managers.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.059789 socon-0.2rc1/tests/manager/missing_attr/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc1/tests/manager/missing_attr/__init__.py
--rw-rw-rw-   0        0        0       98 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/manager/missing_attr/managers.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.069790 socon-0.2rc1/tests/manager/outside_project/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc1/tests/manager/outside_project/__init__.py
--rw-rw-rw-   0        0        0      114 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/manager/outside_project/lookup.py
--rw-rw-rw-   0        0        0     6685 2023-07-15 18:49:23.000000 socon-0.2rc1/tests/manager/tests.py
--rw-rw-rw-   0        0        0      161 2023-03-03 16:16:10.000000 socon-0.2rc1/tests/pytest.ini
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.080288 socon-0.2rc1/tests/registry/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc1/tests/registry/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.088287 socon-0.2rc1/tests/registry/config_with_manager/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:11.000000 socon-0.2rc1/tests/registry/config_with_manager/__init__.py
--rw-rw-rw-   0        0        0      202 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/registry/config_with_manager/managers.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.094788 socon-0.2rc1/tests/registry/config_with_settings/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc1/tests/registry/config_with_settings/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.102290 socon-0.2rc1/tests/registry/config_with_settings/management/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc1/tests/registry/config_with_settings/management/__init__.py
--rw-rw-rw-   0        0        0      151 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/registry/config_with_settings/management/config.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.108789 socon-0.2rc1/tests/registry/config_with_settings/management/config_folder/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc1/tests/registry/config_with_settings/management/config_folder/__init__.py
--rw-rw-rw-   0        0        0      215 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/registry/config_with_settings/management/config_folder/config.py
--rw-rw-rw-   0        0        0      418 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/registry/config_with_settings/projects.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.119289 socon-0.2rc1/tests/registry/default_config/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc1/tests/registry/default_config/__init__.py
--rw-rw-rw-   0        0        0      505 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/registry/default_config/projects.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.124789 socon-0.2rc1/tests/registry/no_config_project/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc1/tests/registry/no_config_project/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.130287 socon-0.2rc1/tests/registry/one_config_project/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc1/tests/registry/one_config_project/__init__.py
--rw-rw-rw-   0        0        0      133 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/registry/one_config_project/projects.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.138789 socon-0.2rc1/tests/registry/plugins/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:29.000000 socon-0.2rc1/tests/registry/plugins/__init__.py
--rw-rw-rw-   0        0        0      123 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/registry/plugins/plugins.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.147288 socon-0.2rc1/tests/registry/registry_config/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc1/tests/registry/registry_config/__init__.py
--rw-rw-rw-   0        0        0      133 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/registry/registry_config/config.py
--rw-rw-rw-   0        0        0    17655 2023-07-15 18:49:23.000000 socon-0.2rc1/tests/registry/tests.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.159287 socon-0.2rc1/tests/registry/two_configs_project/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc1/tests/registry/two_configs_project/__init__.py
--rw-rw-rw-   0        0        0      217 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/registry/two_configs_project/projects.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.187788 socon-0.2rc1/tests/requirement/
--rw-rw-rw-   0        0        0       62 2023-03-14 20:24:24.000000 socon-0.2rc1/tests/requirement/requirements.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.200790 socon-0.2rc1/tests/reshape/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:15:51.000000 socon-0.2rc1/tests/reshape/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.211288 socon-0.2rc1/tests/reshape/datafixtures/
--rw-rw-rw-   0        0        0      257 2023-07-21 19:34:23.000000 socon-0.2rc1/tests/reshape/datafixtures/example.txt
--rw-rw-rw-   0        0        0      257 2023-03-14 20:24:24.000000 socon-0.2rc1/tests/reshape/datafixtures/template.txt
--rw-rw-rw-   0        0        0     1892 2023-07-15 18:49:23.000000 socon-0.2rc1/tests/reshape/tests.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.226288 socon-0.2rc1/tests/settings_tests/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:14:21.000000 socon-0.2rc1/tests/settings_tests/__init__.py
--rw-rw-rw-   0        0        0      139 2023-03-03 16:16:36.000000 socon-0.2rc1/tests/settings_tests/test_settings.py
--rw-rw-rw-   0        0        0     9681 2023-07-15 18:49:23.000000 socon-0.2rc1/tests/settings_tests/tests.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.234289 socon-0.2rc1/tests/user_commands/
--rw-rw-rw-   0        0        0        0 2023-04-30 13:24:41.000000 socon-0.2rc1/tests/user_commands/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.241288 socon-0.2rc1/tests/user_commands/management/
--rw-rw-rw-   0        0        0        0 2023-04-30 13:24:41.000000 socon-0.2rc1/tests/user_commands/management/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.247299 socon-0.2rc1/tests/user_commands/management/commands/
--rw-rw-rw-   0        0        0        0 2023-04-30 13:24:41.000000 socon-0.2rc1/tests/user_commands/management/commands/__init__.py
--rw-rw-rw-   0        0        0     1131 2023-04-30 13:24:41.000000 socon-0.2rc1/tests/user_commands/management/commands/launch.py
--rw-rw-rw-   0        0        0     3888 2023-07-21 19:40:47.000000 socon-0.2rc1/tests/user_commands/tests.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.279288 socon-0.2rc1/tests/utils/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:15:51.000000 socon-0.2rc1/tests/utils/__init__.py
--rw-rw-rw-   0        0        0      573 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/utils/test_log.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.304287 socon-0.2rc1/tests/utils/test_module/
--rw-rw-rw-   0        0        0       60 2023-03-03 16:16:11.000000 socon-0.2rc1/tests/utils/test_module/__init__.py
--rw-rw-rw-   0        0        0      165 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/utils/test_module/another_bad_module.py
--rw-rw-rw-   0        0        0      125 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/utils/test_module/another_good_module.py
--rw-rw-rw-   0        0        0       77 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/utils/test_module/bad_module.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:12:12.312288 socon-0.2rc1/tests/utils/test_module/child_module/
--rw-rw-rw-   0        0        0        0 2023-03-03 16:16:11.000000 socon-0.2rc1/tests/utils/test_module/child_module/__init__.py
--rw-rw-rw-   0        0        0       31 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/utils/test_module/child_module/grandchild_module.py
--rw-rw-rw-   0        0        0       25 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/utils/test_module/good_module.py
--rw-rw-rw-   0        0        0     2541 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/utils/test_module_loading.py
--rw-rw-rw-   0        0        0     7493 2023-07-21 19:23:29.000000 socon-0.2rc1/tests/utils/test_terminal.py
--rw-rw-rw-   0        0        0     2462 2023-03-03 16:16:34.000000 socon-0.2rc1/tests/utils/test_version.py
--rw-rw-rw-   0        0        0     1420 2023-03-14 20:24:24.000000 socon-0.2rc1/tox.ini
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.641446 socon-0.2rc2/
+-rw-rw-rw-   0        0        0      206 2023-07-15 18:49:23.000000 socon-0.2rc2/.coveragerc
+-rw-rw-rw-   0        0        0       87 2023-03-14 20:24:24.000000 socon-0.2rc2/.gitattributes
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.617943 socon-0.2rc2/.github/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.756444 socon-0.2rc2/.github/workflows/
+-rw-rw-rw-   0        0        0     1079 2023-03-09 17:46:46.000000 socon-0.2rc2/.github/workflows/coverage.yml
+-rw-rw-rw-   0        0        0      747 2023-03-03 16:16:37.000000 socon-0.2rc2/.github/workflows/docs.yml
+-rw-rw-rw-   0        0        0     1110 2023-03-05 23:21:53.000000 socon-0.2rc2/.github/workflows/linters.yml
+-rw-rw-rw-   0        0        0      959 2023-03-05 23:21:53.000000 socon-0.2rc2/.github/workflows/tests.yml
+-rw-rw-rw-   0        0        0      950 2023-03-14 20:24:24.000000 socon-0.2rc2/.gitignore
+-rw-rw-rw-   0        0        0      709 2023-07-22 17:41:15.000000 socon-0.2rc2/.pre-commit-config.yaml
+-rw-rw-rw-   0        0        0       71 2023-07-15 18:49:23.000000 socon-0.2rc2/AUTHORS
+-rw-rw-rw-   0        0        0     5352 2023-03-05 10:52:09.000000 socon-0.2rc2/CODE_OF_CONDUCT.md
+-rw-rw-rw-   0        0        0    10127 2023-03-14 20:24:24.000000 socon-0.2rc2/CONTRIBUTING.rst
+-rw-rw-rw-   0        0        0     1556 2023-03-14 20:24:24.000000 socon-0.2rc2/LICENSE
+-rw-rw-rw-   0        0        0     7378 2023-07-23 16:48:49.634945 socon-0.2rc2/PKG-INFO
+-rw-rw-rw-   0        0        0     6178 2023-07-15 18:52:40.000000 socon-0.2rc2/README.rst
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.802944 socon-0.2rc2/docs/
+-rw-rw-rw-   0        0        0      654 2023-03-03 16:15:01.000000 socon-0.2rc2/docs/Makefile
+-rw-rw-rw-   0        0        0      858 2023-03-03 16:15:28.000000 socon-0.2rc2/docs/README.rst
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.806444 socon-0.2rc2/docs/_ext/
+-rw-rw-rw-   0        0        0      724 2023-03-05 10:49:33.000000 socon-0.2rc2/docs/_ext/socondoc.py
+-rw-rw-rw-   0        0        0     3976 2023-07-23 13:05:46.000000 socon-0.2rc2/docs/conf.py
+-rw-rw-rw-   0        0        0      344 2023-03-03 16:16:32.000000 socon-0.2rc2/docs/contents.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.819443 socon-0.2rc2/docs/how-to/
+-rw-rw-rw-   0        0        0    18633 2023-07-21 19:23:29.000000 socon-0.2rc2/docs/how-to/custom-commands.txt
+-rw-rw-rw-   0        0        0    11457 2023-07-21 19:23:29.000000 socon-0.2rc2/docs/how-to/custom-managers-and-hooks.txt
+-rw-rw-rw-   0        0        0      185 2023-03-05 17:30:59.000000 socon-0.2rc2/docs/how-to/index.txt
+-rw-rw-rw-   0        0        0     2836 2023-03-05 16:48:03.000000 socon-0.2rc2/docs/index.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.842446 socon-0.2rc2/docs/internals/
+-rw-rw-rw-   0        0        0     3315 2023-07-23 16:02:46.000000 socon-0.2rc2/docs/internals/changelog.txt
+-rw-rw-rw-   0        0        0     2885 2023-03-14 20:24:24.000000 socon-0.2rc2/docs/internals/coding-style.txt
+-rw-rw-rw-   0        0        0       58 2023-03-14 20:24:24.000000 socon-0.2rc2/docs/internals/contributing.txt
+-rw-rw-rw-   0        0        0      450 2023-03-03 17:12:46.000000 socon-0.2rc2/docs/internals/deprecations.txt
+-rw-rw-rw-   0        0        0      282 2023-03-03 16:16:32.000000 socon-0.2rc2/docs/internals/index.txt
+-rw-rw-rw-   0        0        0     3020 2023-03-03 17:24:11.000000 socon-0.2rc2/docs/internals/release-process.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.863443 socon-0.2rc2/docs/intro/
+-rw-rw-rw-   0        0        0     2714 2023-03-04 16:09:31.000000 socon-0.2rc2/docs/intro/environment.txt
+-rw-rw-rw-   0        0        0      279 2023-03-04 10:06:27.000000 socon-0.2rc2/docs/intro/index.txt
+-rw-rw-rw-   0        0        0     2883 2023-03-05 16:46:16.000000 socon-0.2rc2/docs/intro/install.txt
+-rw-rw-rw-   0        0        0     2263 2023-03-04 10:07:25.000000 socon-0.2rc2/docs/intro/overview.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.892945 socon-0.2rc2/docs/intro/tutorials/
+-rw-rw-rw-   0        0        0    19350 2023-07-15 18:49:23.000000 socon-0.2rc2/docs/intro/tutorials/1_project_and_command.txt
+-rw-rw-rw-   0        0        0     3772 2023-03-09 21:40:52.000000 socon-0.2rc2/docs/intro/tutorials/2_change_behavior.txt
+-rw-rw-rw-   0        0        0     8150 2023-07-15 18:49:23.000000 socon-0.2rc2/docs/intro/tutorials/3_manager.txt
+-rw-rw-rw-   0        0        0     6099 2023-07-15 18:49:23.000000 socon-0.2rc2/docs/intro/tutorials/4_plugins.txt
+-rw-rw-rw-   0        0        0      372 2023-03-04 10:17:03.000000 socon-0.2rc2/docs/intro/tutorials/index.txt
+-rwxrwxrwx   0        0        0      795 2023-03-03 16:15:01.000000 socon-0.2rc2/docs/make.bat
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.965944 socon-0.2rc2/docs/ref/
+-rw-rw-rw-   0        0        0     8182 2023-07-21 19:23:29.000000 socon-0.2rc2/docs/ref/commands.txt
+-rw-rw-rw-   0        0        0     1577 2023-07-15 18:49:23.000000 socon-0.2rc2/docs/ref/exceptions.txt
+-rw-rw-rw-   0        0        0      346 2023-03-03 16:16:32.000000 socon-0.2rc2/docs/ref/index.txt
+-rw-rw-rw-   0        0        0     4653 2023-03-04 16:09:31.000000 socon-0.2rc2/docs/ref/list-of-settings.txt
+-rw-rw-rw-   0        0        0     1537 2023-03-03 16:16:21.000000 socon-0.2rc2/docs/ref/logging.txt
+-rw-rw-rw-   0        0        0     4567 2023-07-15 18:49:23.000000 socon-0.2rc2/docs/ref/manager.txt
+-rw-rw-rw-   0        0        0    15314 2023-03-09 21:40:52.000000 socon-0.2rc2/docs/ref/registry.txt
+-rw-rw-rw-   0        0        0     5331 2023-03-09 21:40:52.000000 socon-0.2rc2/docs/ref/settings.txt
+-rw-rw-rw-   0        0        0     9757 2023-07-15 18:49:23.000000 socon-0.2rc2/docs/ref/socon-admin.txt
+-rw-rw-rw-   0        0        0     3755 2023-07-21 19:23:29.000000 socon-0.2rc2/docs/ref/terminal.txt
+-rw-rw-rw-   0        0        0     3169 2023-07-15 18:49:23.000000 socon-0.2rc2/docs/ref/utils.txt
+-rw-rw-rw-   0        0        0       63 2023-03-03 16:16:32.000000 socon-0.2rc2/docs/requirements.txt
+-rw-rw-rw-   0        0        0      604 2023-07-23 13:03:26.000000 socon-0.2rc2/docs/spelling_wordlist
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.987944 socon-0.2rc2/licenses/
+-rw-rw-rw-   0        0        0     1579 2023-03-14 20:24:24.000000 socon-0.2rc2/licenses/LicenseRef-BSD3-Clause-Django.txt
+-rw-rw-rw-   0        0        0     1112 2023-03-14 20:24:24.000000 socon-0.2rc2/licenses/LicenseRef-MIT-Pytest.txt
+-rw-rw-rw-   0        0        0     1509 2023-07-23 08:42:30.000000 socon-0.2rc2/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 16:48:49.641946 socon-0.2rc2/setup.cfg
+-rw-rw-rw-   0        0        0       73 2023-03-03 16:16:34.000000 socon-0.2rc2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.995443 socon-0.2rc2/socon/
+-rw-rw-rw-   0        0        0     1380 2023-07-23 16:04:16.000000 socon-0.2rc2/socon/__init__.py
+-rw-rw-rw-   0        0        0      239 2023-03-05 10:41:34.000000 socon-0.2rc2/socon/__main__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.020446 socon-0.2rc2/socon/conf/
+-rw-rw-rw-   0        0        0    10683 2023-03-03 16:16:34.000000 socon-0.2rc2/socon/conf/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.626945 socon-0.2rc2/socon/conf/basecommand_template/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.627445 socon-0.2rc2/socon/conf/basecommand_template/management/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.023945 socon-0.2rc2/socon/conf/basecommand_template/management/commands/
+-rw-rw-rw-   0        0        0     1069 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/conf/basecommand_template/management/commands/basecommand_name.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.027943 socon-0.2rc2/socon/conf/container_template/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.033445 socon-0.2rc2/socon/conf/container_template/container_name/
+-rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/conf/container_template/container_name/__init__.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.037443 socon-0.2rc2/socon/conf/container_template/container_name/management/
+-rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/conf/container_template/container_name/management/__init__.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.039445 socon-0.2rc2/socon/conf/container_template/container_name/management/commands/
+-rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/conf/container_template/container_name/management/commands/__init__.py-tpl
+-rw-rw-rw-   0        0        0      773 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/conf/container_template/container_name/settings.py-tpl
+-rw-rw-rw-   0        0        0      694 2023-03-03 16:15:57.000000 socon-0.2rc2/socon/conf/container_template/manage.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.041444 socon-0.2rc2/socon/conf/container_template/projects/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:15:30.000000 socon-0.2rc2/socon/conf/container_template/projects/__init__.py-tpl
+-rw-rw-rw-   0        0        0     1180 2023-03-03 16:16:34.000000 socon-0.2rc2/socon/conf/global_settings.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.046444 socon-0.2rc2/socon/conf/plugin_template/
+-rw-rw-rw-   0        0        0       91 2023-03-03 16:16:21.000000 socon-0.2rc2/socon/conf/plugin_template/README.rst-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.051943 socon-0.2rc2/socon/conf/plugin_template/plugin_name/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:15:51.000000 socon-0.2rc2/socon/conf/plugin_template/plugin_name/__init__.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.055944 socon-0.2rc2/socon/conf/plugin_template/plugin_name/management/
+-rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/conf/plugin_template/plugin_name/management/__init__.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.057945 socon-0.2rc2/socon/conf/plugin_template/plugin_name/management/commands/
+-rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/conf/plugin_template/plugin_name/management/commands/__init__.py-tpl
+-rw-rw-rw-   0        0        0      146 2023-03-03 16:16:15.000000 socon-0.2rc2/socon/conf/plugin_template/plugin_name/plugins.py-tpl
+-rw-rw-rw-   0        0        0      313 2023-03-03 16:16:25.000000 socon-0.2rc2/socon/conf/plugin_template/setup.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.061443 socon-0.2rc2/socon/conf/project_template/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:14:20.000000 socon-0.2rc2/socon/conf/project_template/__init__.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.067444 socon-0.2rc2/socon/conf/project_template/management/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:15:51.000000 socon-0.2rc2/socon/conf/project_template/management/__init__.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.070943 socon-0.2rc2/socon/conf/project_template/management/commands/
+-rw-rw-rw-   0        0        0        0 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/conf/project_template/management/commands/__init__.py-tpl
+-rw-rw-rw-   0        0        0      267 2023-03-03 16:16:17.000000 socon-0.2rc2/socon/conf/project_template/management/config.py-tpl
+-rw-rw-rw-   0        0        0      202 2023-03-03 16:15:55.000000 socon-0.2rc2/socon/conf/project_template/projects.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.637444 socon-0.2rc2/socon/conf/projectcommand_template/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.637944 socon-0.2rc2/socon/conf/projectcommand_template/management/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.072444 socon-0.2rc2/socon/conf/projectcommand_template/management/commands/
+-rw-rw-rw-   0        0        0     1453 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/conf/projectcommand_template/management/commands/projectcommand_name.py-tpl
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.082444 socon-0.2rc2/socon/core/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:14:15.000000 socon-0.2rc2/socon/core/__init__.py
+-rw-rw-rw-   0        0        0      574 2023-03-03 16:16:34.000000 socon-0.2rc2/socon/core/exceptions.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.099944 socon-0.2rc2/socon/core/management/
+-rw-rw-rw-   0        0        0     9068 2023-07-23 15:53:43.000000 socon-0.2rc2/socon/core/management/__init__.py
+-rw-rw-rw-   0        0        0    19827 2023-07-23 15:53:43.000000 socon-0.2rc2/socon/core/management/base.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.125944 socon-0.2rc2/socon/core/management/commands/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:15:01.000000 socon-0.2rc2/socon/core/management/commands/__init__.py
+-rw-rw-rw-   0        0        0     3057 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/core/management/commands/check.py
+-rw-rw-rw-   0        0        0     4868 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/core/management/commands/createcommand.py
+-rw-rw-rw-   0        0        0      947 2023-03-03 16:16:34.000000 socon-0.2rc2/socon/core/management/commands/createcontainer.py
+-rw-rw-rw-   0        0        0      936 2023-03-03 16:16:34.000000 socon-0.2rc2/socon/core/management/commands/createplugin.py
+-rw-rw-rw-   0        0        0     2412 2023-05-04 09:58:38.000000 socon-0.2rc2/socon/core/management/commands/createproject.py
+-rw-rw-rw-   0        0        0     3822 2023-07-23 15:53:28.000000 socon-0.2rc2/socon/core/management/subcommand.py
+-rw-rw-rw-   0        0        0     6166 2023-07-15 20:06:51.000000 socon-0.2rc2/socon/core/management/templates.py
+-rw-rw-rw-   0        0        0    12197 2023-07-15 21:29:48.000000 socon-0.2rc2/socon/core/manager.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.145446 socon-0.2rc2/socon/core/registry/
+-rw-rw-rw-   0        0        0      137 2023-03-03 16:16:04.000000 socon-0.2rc2/socon/core/registry/__init__.py
+-rw-rw-rw-   0        0        0     8043 2023-03-05 21:26:25.000000 socon-0.2rc2/socon/core/registry/base.py
+-rw-rw-rw-   0        0        0    10082 2023-03-05 21:30:59.000000 socon-0.2rc2/socon/core/registry/config.py
+-rw-rw-rw-   0        0        0     3495 2023-03-05 21:31:27.000000 socon-0.2rc2/socon/core/registry/core.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.154444 socon-0.2rc2/socon/test/
+-rw-rw-rw-   0        0        0       56 2023-03-03 16:16:16.000000 socon-0.2rc2/socon/test/__init__.py
+-rw-rw-rw-   0        0        0     3004 2023-04-30 13:24:41.000000 socon-0.2rc2/socon/test/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.186945 socon-0.2rc2/socon/utils/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:14:15.000000 socon-0.2rc2/socon/utils/__init__.py
+-rw-rw-rw-   0        0        0     1007 2023-04-30 13:24:41.000000 socon-0.2rc2/socon/utils/func.py
+-rw-rw-rw-   0        0        0      716 2023-03-03 16:16:34.000000 socon-0.2rc2/socon/utils/log.py
+-rw-rw-rw-   0        0        0     1475 2023-03-03 16:16:34.000000 socon-0.2rc2/socon/utils/module_loading.py
+-rw-rw-rw-   0        0        0     2468 2023-07-15 18:49:23.000000 socon-0.2rc2/socon/utils/reshape.py
+-rw-rw-rw-   0        0        0    10157 2023-07-21 19:23:29.000000 socon-0.2rc2/socon/utils/terminal.py
+-rw-rw-rw-   0        0        0     2556 2023-03-03 21:53:01.000000 socon-0.2rc2/socon/utils/version.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.013445 socon-0.2rc2/socon.egg-info/
+-rw-rw-rw-   0        0        0     7378 2023-07-23 16:48:48.000000 socon-0.2rc2/socon.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     7902 2023-07-23 16:48:48.000000 socon-0.2rc2/socon.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 16:48:48.000000 socon-0.2rc2/socon.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       74 2023-07-23 16:48:48.000000 socon-0.2rc2/socon.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0        6 2023-07-23 16:48:48.000000 socon-0.2rc2/socon.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.205446 socon-0.2rc2/tests/
+-rw-rw-rw-   0        0        0      561 2023-03-05 10:31:40.000000 socon-0.2rc2/tests/README.rst
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.216019 socon-0.2rc2/tests/admin_scripts/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:14:24.000000 socon-0.2rc2/tests/admin_scripts/__init__.py
+-rw-rw-rw-   0        0        0      270 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/configured_settings_manage.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:48.645445 socon-0.2rc2/tests/admin_scripts/management/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.241446 socon-0.2rc2/tests/admin_scripts/management/commands/
+-rw-rw-rw-   0        0        0     1218 2023-03-03 16:16:36.000000 socon-0.2rc2/tests/admin_scripts/management/commands/base_command.py
+-rw-rw-rw-   0        0        0      391 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/management/commands/custom_createcontainer.py
+-rw-rw-rw-   0        0        0      324 2023-03-03 21:31:31.000000 socon-0.2rc2/tests/admin_scripts/management/commands/extras_args_command.py
+-rw-rw-rw-   0        0        0      376 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/management/commands/noargs_command.py
+-rw-rw-rw-   0        0        0      377 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/management/commands/project_commands.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.247444 socon-0.2rc2/tests/admin_scripts/project_with_command/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc2/tests/admin_scripts/project_with_command/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.252444 socon-0.2rc2/tests/admin_scripts/project_with_command/management/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc2/tests/admin_scripts/project_with_command/management/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.256948 socon-0.2rc2/tests/admin_scripts/project_with_command/management/commands/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc2/tests/admin_scripts/project_with_command/management/commands/__init__.py
+-rw-rw-rw-   0        0        0      212 2023-04-30 13:24:41.000000 socon-0.2rc2/tests/admin_scripts/project_with_command/management/commands/simple_command.py
+-rw-rw-rw-   0        0        0      149 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/project_with_command/projects.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.264445 socon-0.2rc2/tests/admin_scripts/project_with_error/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc2/tests/admin_scripts/project_with_error/__init__.py
+-rw-rw-rw-   0        0        0      253 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/project_with_error/projects.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.281445 socon-0.2rc2/tests/admin_scripts/project_with_manager/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:25.000000 socon-0.2rc2/tests/admin_scripts/project_with_manager/__init__.py
+-rw-rw-rw-   0        0        0      150 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/project_with_manager/manager_error.py
+-rw-rw-rw-   0        0        0      149 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/project_with_manager/managers.py
+-rw-rw-rw-   0        0        0      149 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/project_with_manager/projects.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.287446 socon-0.2rc2/tests/admin_scripts/simple_project/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:15:04.000000 socon-0.2rc2/tests/admin_scripts/simple_project/__init__.py
+-rw-rw-rw-   0        0        0      138 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/admin_scripts/simple_project/projects.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.292943 socon-0.2rc2/tests/admin_scripts/subcommands/
+-rw-rw-rw-   0        0        0        0 2023-07-21 19:23:29.000000 socon-0.2rc2/tests/admin_scripts/subcommands/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.298444 socon-0.2rc2/tests/admin_scripts/subcommands/management/
+-rw-rw-rw-   0        0        0        0 2023-07-21 19:23:29.000000 socon-0.2rc2/tests/admin_scripts/subcommands/management/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.307446 socon-0.2rc2/tests/admin_scripts/subcommands/management/commands/
+-rw-rw-rw-   0        0        0        0 2023-07-21 19:23:29.000000 socon-0.2rc2/tests/admin_scripts/subcommands/management/commands/__init__.py
+-rw-rw-rw-   0        0        0      164 2023-07-21 19:23:29.000000 socon-0.2rc2/tests/admin_scripts/subcommands/management/commands/command_with_subcommand.py
+-rw-rw-rw-   0        0        0      157 2023-07-21 19:23:29.000000 socon-0.2rc2/tests/admin_scripts/subcommands/management/commands/no_subcommands.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.313945 socon-0.2rc2/tests/admin_scripts/subcommands/management/commands/subcommands/
+-rw-rw-rw-   0        0        0        0 2023-07-21 19:23:29.000000 socon-0.2rc2/tests/admin_scripts/subcommands/management/commands/subcommands/__init__.py
+-rw-rw-rw-   0        0        0      496 2023-07-21 19:23:29.000000 socon-0.2rc2/tests/admin_scripts/subcommands/management/commands/subcommands/sub.py
+-rw-rw-rw-   0        0        0      232 2023-07-21 19:23:29.000000 socon-0.2rc2/tests/admin_scripts/subcommands/managers.py
+-rw-rw-rw-   0        0        0    58466 2023-07-23 15:53:28.000000 socon-0.2rc2/tests/admin_scripts/tests.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.324444 socon-0.2rc2/tests/common/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:11.000000 socon-0.2rc2/tests/common/__init__.py
+-rw-rw-rw-   0        0        0      178 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/common/lookup.py
+-rw-rw-rw-   0        0        0      305 2023-03-03 16:16:11.000000 socon-0.2rc2/tests/common/settings.py
+-rw-rw-rw-   0        0        0     3826 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/conftest.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.339945 socon-0.2rc2/tests/manager/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc2/tests/manager/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.346444 socon-0.2rc2/tests/manager/duplicate_hooks/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:19.000000 socon-0.2rc2/tests/manager/duplicate_hooks/__init__.py
+-rw-rw-rw-   0        0        0      173 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/manager/duplicate_hooks/lookup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.352944 socon-0.2rc2/tests/manager/duplicate_managers/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc2/tests/manager/duplicate_managers/__init__.py
+-rw-rw-rw-   0        0        0      208 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/manager/duplicate_managers/managers.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.360945 socon-0.2rc2/tests/manager/hook_not_linked/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:19.000000 socon-0.2rc2/tests/manager/hook_not_linked/__init__.py
+-rw-rw-rw-   0        0        0      145 2023-03-03 16:16:19.000000 socon-0.2rc2/tests/manager/hook_not_linked/managers.py
+-rw-rw-rw-   0        0        0      242 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/manager/lookup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.373446 socon-0.2rc2/tests/manager/manager_not_hooked/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:19.000000 socon-0.2rc2/tests/manager/manager_not_hooked/__init__.py
+-rw-rw-rw-   0        0        0      147 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/manager/manager_not_hooked/managers.py
+-rw-rw-rw-   0        0        0      100 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/manager/manager_not_hooked/not_hooked.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.379944 socon-0.2rc2/tests/manager/manager_with_abstract/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc2/tests/manager/manager_with_abstract/__init__.py
+-rw-rw-rw-   0        0        0      210 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/manager/manager_with_abstract/lookup.py
+-rw-rw-rw-   0        0        0      221 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/manager/managers.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.385444 socon-0.2rc2/tests/manager/missing_attr/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc2/tests/manager/missing_attr/__init__.py
+-rw-rw-rw-   0        0        0       98 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/manager/missing_attr/managers.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.391944 socon-0.2rc2/tests/manager/outside_project/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:12.000000 socon-0.2rc2/tests/manager/outside_project/__init__.py
+-rw-rw-rw-   0        0        0      114 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/manager/outside_project/lookup.py
+-rw-rw-rw-   0        0        0     6685 2023-07-15 18:49:23.000000 socon-0.2rc2/tests/manager/tests.py
+-rw-rw-rw-   0        0        0      161 2023-03-03 16:16:10.000000 socon-0.2rc2/tests/pytest.ini
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.398445 socon-0.2rc2/tests/registry/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc2/tests/registry/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.405944 socon-0.2rc2/tests/registry/config_with_manager/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:11.000000 socon-0.2rc2/tests/registry/config_with_manager/__init__.py
+-rw-rw-rw-   0        0        0      202 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/registry/config_with_manager/managers.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.411445 socon-0.2rc2/tests/registry/config_with_settings/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc2/tests/registry/config_with_settings/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.419944 socon-0.2rc2/tests/registry/config_with_settings/management/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc2/tests/registry/config_with_settings/management/__init__.py
+-rw-rw-rw-   0        0        0      151 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/registry/config_with_settings/management/config.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.426444 socon-0.2rc2/tests/registry/config_with_settings/management/config_folder/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc2/tests/registry/config_with_settings/management/config_folder/__init__.py
+-rw-rw-rw-   0        0        0      215 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/registry/config_with_settings/management/config_folder/config.py
+-rw-rw-rw-   0        0        0      418 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/registry/config_with_settings/projects.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.438447 socon-0.2rc2/tests/registry/default_config/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc2/tests/registry/default_config/__init__.py
+-rw-rw-rw-   0        0        0      505 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/registry/default_config/projects.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.444944 socon-0.2rc2/tests/registry/no_config_project/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc2/tests/registry/no_config_project/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.449445 socon-0.2rc2/tests/registry/one_config_project/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc2/tests/registry/one_config_project/__init__.py
+-rw-rw-rw-   0        0        0      133 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/registry/one_config_project/projects.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.455944 socon-0.2rc2/tests/registry/plugins/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:29.000000 socon-0.2rc2/tests/registry/plugins/__init__.py
+-rw-rw-rw-   0        0        0      123 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/registry/plugins/plugins.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.462944 socon-0.2rc2/tests/registry/registry_config/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc2/tests/registry/registry_config/__init__.py
+-rw-rw-rw-   0        0        0      133 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/registry/registry_config/config.py
+-rw-rw-rw-   0        0        0    17655 2023-07-15 18:49:23.000000 socon-0.2rc2/tests/registry/tests.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.469944 socon-0.2rc2/tests/registry/two_configs_project/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:00.000000 socon-0.2rc2/tests/registry/two_configs_project/__init__.py
+-rw-rw-rw-   0        0        0      217 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/registry/two_configs_project/projects.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.475945 socon-0.2rc2/tests/requirement/
+-rw-rw-rw-   0        0        0       62 2023-03-14 20:24:24.000000 socon-0.2rc2/tests/requirement/requirements.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.482447 socon-0.2rc2/tests/reshape/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:15:51.000000 socon-0.2rc2/tests/reshape/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.490944 socon-0.2rc2/tests/reshape/datafixtures/
+-rw-rw-rw-   0        0        0      257 2023-07-23 15:55:22.000000 socon-0.2rc2/tests/reshape/datafixtures/example.txt
+-rw-rw-rw-   0        0        0      257 2023-03-14 20:24:24.000000 socon-0.2rc2/tests/reshape/datafixtures/template.txt
+-rw-rw-rw-   0        0        0     1892 2023-07-15 18:49:23.000000 socon-0.2rc2/tests/reshape/tests.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.501444 socon-0.2rc2/tests/settings_tests/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:14:21.000000 socon-0.2rc2/tests/settings_tests/__init__.py
+-rw-rw-rw-   0        0        0      139 2023-03-03 16:16:36.000000 socon-0.2rc2/tests/settings_tests/test_settings.py
+-rw-rw-rw-   0        0        0     9681 2023-07-15 18:49:23.000000 socon-0.2rc2/tests/settings_tests/tests.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.508444 socon-0.2rc2/tests/user_commands/
+-rw-rw-rw-   0        0        0        0 2023-04-30 13:24:41.000000 socon-0.2rc2/tests/user_commands/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.513445 socon-0.2rc2/tests/user_commands/management/
+-rw-rw-rw-   0        0        0        0 2023-04-30 13:24:41.000000 socon-0.2rc2/tests/user_commands/management/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.518444 socon-0.2rc2/tests/user_commands/management/commands/
+-rw-rw-rw-   0        0        0        0 2023-04-30 13:24:41.000000 socon-0.2rc2/tests/user_commands/management/commands/__init__.py
+-rw-rw-rw-   0        0        0     1131 2023-04-30 13:24:41.000000 socon-0.2rc2/tests/user_commands/management/commands/launch.py
+-rw-rw-rw-   0        0        0     3888 2023-07-21 19:40:47.000000 socon-0.2rc2/tests/user_commands/tests.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.547445 socon-0.2rc2/tests/utils/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:15:51.000000 socon-0.2rc2/tests/utils/__init__.py
+-rw-rw-rw-   0        0        0      573 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/utils/test_log.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.571944 socon-0.2rc2/tests/utils/test_module/
+-rw-rw-rw-   0        0        0       60 2023-03-03 16:16:11.000000 socon-0.2rc2/tests/utils/test_module/__init__.py
+-rw-rw-rw-   0        0        0      165 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/utils/test_module/another_bad_module.py
+-rw-rw-rw-   0        0        0      125 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/utils/test_module/another_good_module.py
+-rw-rw-rw-   0        0        0       77 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/utils/test_module/bad_module.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:48:49.578944 socon-0.2rc2/tests/utils/test_module/child_module/
+-rw-rw-rw-   0        0        0        0 2023-03-03 16:16:11.000000 socon-0.2rc2/tests/utils/test_module/child_module/__init__.py
+-rw-rw-rw-   0        0        0       31 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/utils/test_module/child_module/grandchild_module.py
+-rw-rw-rw-   0        0        0       25 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/utils/test_module/good_module.py
+-rw-rw-rw-   0        0        0     2541 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/utils/test_module_loading.py
+-rw-rw-rw-   0        0        0     7493 2023-07-21 19:23:29.000000 socon-0.2rc2/tests/utils/test_terminal.py
+-rw-rw-rw-   0        0        0     2462 2023-03-03 16:16:34.000000 socon-0.2rc2/tests/utils/test_version.py
+-rw-rw-rw-   0        0        0     1420 2023-03-14 20:24:24.000000 socon-0.2rc2/tox.ini
```

### Comparing `socon-0.2rc1/.github/workflows/coverage.yml` & `socon-0.2rc2/.github/workflows/coverage.yml`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/.github/workflows/docs.yml` & `socon-0.2rc2/.github/workflows/docs.yml`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/.github/workflows/linters.yml` & `socon-0.2rc2/.github/workflows/linters.yml`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/.github/workflows/tests.yml` & `socon-0.2rc2/.github/workflows/tests.yml`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/.gitignore` & `socon-0.2rc2/.gitignore`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/.pre-commit-config.yaml` & `socon-0.2rc2/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/CODE_OF_CONDUCT.md` & `socon-0.2rc2/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/CONTRIBUTING.rst` & `socon-0.2rc2/CONTRIBUTING.rst`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/LICENSE` & `socon-0.2rc2/LICENSE`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/PKG-INFO` & `socon-0.2rc2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: socon
-Version: 0.2rc1
+Version: 0.2rc2
 Summary: A high-level Python framework that enables you to develop a generic, robust and reliable framework for your different projects.
 Author-email: Stephane Capponi <stephane.capponi@gmail.com>
 License: BSD-3-Clause
 Project-URL: homepage, https://socon.readthedocs.io/en/latest/
 Project-URL: repository, https://github.com/socon-dev/socon
 Project-URL: changelog, https://github.com/socon-dev/socon/blob/master/docs/internals/changelog.txt
 Keywords: projects,socon,scripts,commands
```

### Comparing `socon-0.2rc1/README.rst` & `socon-0.2rc2/README.rst`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/Makefile` & `socon-0.2rc2/docs/Makefile`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/README.rst` & `socon-0.2rc2/docs/README.rst`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/_ext/socondoc.py` & `socon-0.2rc2/docs/_ext/socondoc.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/conf.py` & `socon-0.2rc2/docs/conf.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/how-to/custom-commands.txt` & `socon-0.2rc2/docs/how-to/custom-commands.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/how-to/custom-managers-and-hooks.txt` & `socon-0.2rc2/docs/how-to/custom-managers-and-hooks.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/index.txt` & `socon-0.2rc2/docs/index.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/internals/changelog.txt` & `socon-0.2rc2/docs/internals/changelog.txt`

 * *Files 4% similar despite different names*

```diff
@@ -42,14 +42,16 @@
 
 * `#6 <https://github.com/socon-dev/socon/issues/6>`_: Add a new admin command called `createcommand`.
   This command automatically create a ProjectCommand or a BaseCommand in the common space or the specified project.
 
 Bug Fixes:
 ----------
 
+* `#37 <https://github.com/socon-dev/socon/issues/37>`_: Fixed by calling parse_args of the called command
+
 * `#32 <https://github.com/socon-dev/socon/issues/32>`_: Fixed by adding \n (newline) to the CommandError exception handler
 
 Improved Documentation
 ----------------------
 
 * `#27 <https://github.com/socon-dev/socon/issues/27>`_: Fix indentation in the custom-managers-and-hooks documentation.
```

### Comparing `socon-0.2rc1/docs/internals/coding-style.txt` & `socon-0.2rc2/docs/internals/coding-style.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/internals/release-process.txt` & `socon-0.2rc2/docs/internals/release-process.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/intro/environment.txt` & `socon-0.2rc2/docs/intro/environment.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/intro/install.txt` & `socon-0.2rc2/docs/intro/install.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/intro/overview.txt` & `socon-0.2rc2/docs/intro/overview.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/intro/tutorials/1_project_and_command.txt` & `socon-0.2rc2/docs/intro/tutorials/1_project_and_command.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/intro/tutorials/2_change_behavior.txt` & `socon-0.2rc2/docs/intro/tutorials/2_change_behavior.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/intro/tutorials/3_manager.txt` & `socon-0.2rc2/docs/intro/tutorials/3_manager.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/intro/tutorials/4_plugins.txt` & `socon-0.2rc2/docs/intro/tutorials/4_plugins.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/make.bat` & `socon-0.2rc2/docs/make.bat`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/commands.txt` & `socon-0.2rc2/docs/ref/commands.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/exceptions.txt` & `socon-0.2rc2/docs/ref/exceptions.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/list-of-settings.txt` & `socon-0.2rc2/docs/ref/list-of-settings.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/logging.txt` & `socon-0.2rc2/docs/ref/logging.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/manager.txt` & `socon-0.2rc2/docs/ref/manager.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/registry.txt` & `socon-0.2rc2/docs/ref/registry.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/settings.txt` & `socon-0.2rc2/docs/ref/settings.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/socon-admin.txt` & `socon-0.2rc2/docs/ref/socon-admin.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/terminal.txt` & `socon-0.2rc2/docs/ref/terminal.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/ref/utils.txt` & `socon-0.2rc2/docs/ref/utils.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/docs/spelling_wordlist` & `socon-0.2rc2/docs/spelling_wordlist`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/licenses/LicenseRef-BSD3-Clause-Django.txt` & `socon-0.2rc2/licenses/LicenseRef-BSD3-Clause-Django.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/licenses/LicenseRef-MIT-Pytest.txt` & `socon-0.2rc2/licenses/LicenseRef-MIT-Pytest.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/pyproject.toml` & `socon-0.2rc2/pyproject.toml`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/__init__.py` & `socon-0.2rc2/socon/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 # SPDX-License-Identifier: BSD-3-Clause
 # Copyright (c) 2023, Stephane Capponi and Others
 
 from socon.utils.version import get_version
 
-VERSION = (0, 2, 0, "rc", 1)
+VERSION = (0, 2, 0, "rc", 2)
 
 __version__ = get_version(VERSION)
 
 
 def setup() -> None:
     """
     Configure the settings (this happens as a side effect of accessing the
```

### Comparing `socon-0.2rc1/socon/conf/__init__.py` & `socon-0.2rc2/socon/conf/__init__.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/conf/basecommand_template/management/commands/basecommand_name.py-tpl` & `socon-0.2rc2/socon/conf/basecommand_template/management/commands/basecommand_name.py-tpl`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/conf/container_template/container_name/settings.py-tpl` & `socon-0.2rc2/socon/conf/container_template/container_name/settings.py-tpl`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/conf/container_template/manage.py-tpl` & `socon-0.2rc2/socon/conf/container_template/manage.py-tpl`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/conf/global_settings.py` & `socon-0.2rc2/socon/conf/global_settings.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/conf/projectcommand_template/management/commands/projectcommand_name.py-tpl` & `socon-0.2rc2/socon/conf/projectcommand_template/management/commands/projectcommand_name.py-tpl`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/exceptions.py` & `socon-0.2rc2/socon/core/exceptions.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/management/__init__.py` & `socon-0.2rc2/socon/core/management/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -201,35 +201,26 @@
         parse_args.append(str(arg))
         if arg == "--project":
             try:
                 project = args[i + 1]
             except IndexError:
                 raise CommandError("Project was passed but not defined")
 
-    # Search for the command
-    command = command_manager.search_command(name, project)()
-
-    # Create the parser and save the args
-    parser = command.create_parser("", name)
-
-    # Parser the args
-    extras_args = []
-    if command.keep_extras_args:
-        cmd_args, extras_args = parser.parse_known_args(parse_args)
-    else:
-        cmd_args = parser.parse_args(parse_args)
-
-    # Create the conmand config object
-    config = command.set_config(cmd_args, extras_args)
-
     # We change the active project for the command using a context manager. This is
     # important as the execute command for a ProjectCommand, will look for
     # the SOCON_ACTIVE_PROJECT environment to set the project_config of that command.
     project = project if project else os.environ.get("SOCON_ACTIVE_PROJECT", "")
+
+    # Patch the current environment
     with set_env(SOCON_ACTIVE_PROJECT=project):
+        # Search for the command
+        command = command_manager.search_command(name, project)()
+
+        # Parse the arguments and create a config object
+        config = command.parse_args(("", name, *parse_args))
         return command.execute(config)
 
 
 def execute_from_command_line(argv: list = None) -> None:
     """Run a ManagementUtility."""
     utility = ManagementUtility(argv)
     utility.execute()
```

### Comparing `socon-0.2rc1/socon/core/management/base.py` & `socon-0.2rc2/socon/core/management/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -358,15 +358,19 @@
         self, prog_name: str, subcommand: str, **kwargs: Any
     ) -> ArgumentParser:
         """
         Create and return the ``ArgumentParser`` which will be used to
         parse the arguments to this command.
         """
         parser = CommandParser(
-            prog="%s %s" % (os.path.basename(prog_name), subcommand),
+            prog="{prog_name}{space}{subcommand}".format(
+                prog_name=os.path.basename(prog_name),
+                space=" " if prog_name else "",
+                subcommand=subcommand,
+            ),
             description=self.help or None,
             formatter_class=CustomHelpFormatter,
             missing_args_message=getattr(self, "missing_args_message", None),
             called_from_command_line=getattr(self, "_called_from_command_line", None),
             **kwargs,
         )
         parser.add_argument("--version", action="version", version=self.get_version())
```

### Comparing `socon-0.2rc1/socon/core/management/commands/check.py` & `socon-0.2rc2/socon/core/management/commands/check.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/management/commands/createcommand.py` & `socon-0.2rc2/socon/core/management/commands/createcommand.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/management/commands/createcontainer.py` & `socon-0.2rc2/socon/core/management/commands/createcontainer.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/management/commands/createplugin.py` & `socon-0.2rc2/socon/core/management/commands/createplugin.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/management/commands/createproject.py` & `socon-0.2rc2/socon/core/management/commands/createproject.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/management/subcommand.py` & `socon-0.2rc2/socon/core/management/subcommand.py`

 * *Files 4% similar despite different names*

```diff
@@ -6,15 +6,14 @@
 from socon.core.management import get_commands
 from socon.core.management.base import (
     BaseCommand,
     CommandManager,
     Config,
     handle_default_options,
 )
-from socon.utils.terminal import terminal
 
 
 class SubcommandManager(CommandManager):
     name = "subcommands"
     lookup_module = "management.commands.subcommands"
 
     def get_usage_message(self, prog_name: str) -> List[str]:
@@ -55,15 +54,15 @@
             self.print_help(argv[0], f"{argv[1]} SUBCOMMAND")
             sys.exit(1)
 
     def print_help(self, prog_name, subcommand):
         commands = self.get_subcommands()
         usage = commands.get_commands_usage(prog_name, show_registry=False)
         super().print_help(prog_name, subcommand)
-        terminal.write("{}\n\n".format(usage))
+        sys.stdout.write("{}\n\n".format(usage))
 
     def parse_args(self, argv: tuple) -> Config:
         """Parse command line arguments for subcommands"""
         self.argv = argv
         subcommand = None
         if len(argv) > 2 and not argv[2].startswith("-"):
             subcommand = argv[2]
```

### Comparing `socon-0.2rc1/socon/core/management/templates.py` & `socon-0.2rc2/socon/core/management/templates.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/manager.py` & `socon-0.2rc2/socon/core/manager.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/registry/base.py` & `socon-0.2rc2/socon/core/registry/base.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/registry/config.py` & `socon-0.2rc2/socon/core/registry/config.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/core/registry/core.py` & `socon-0.2rc2/socon/core/registry/core.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/test/utils.py` & `socon-0.2rc2/socon/test/utils.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/utils/func.py` & `socon-0.2rc2/socon/utils/func.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/utils/log.py` & `socon-0.2rc2/socon/utils/log.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/utils/module_loading.py` & `socon-0.2rc2/socon/utils/module_loading.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/utils/reshape.py` & `socon-0.2rc2/socon/utils/reshape.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/utils/terminal.py` & `socon-0.2rc2/socon/utils/terminal.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon/utils/version.py` & `socon-0.2rc2/socon/utils/version.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/socon.egg-info/PKG-INFO` & `socon-0.2rc2/socon.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: socon
-Version: 0.2rc1
+Version: 0.2rc2
 Summary: A high-level Python framework that enables you to develop a generic, robust and reliable framework for your different projects.
 Author-email: Stephane Capponi <stephane.capponi@gmail.com>
 License: BSD-3-Clause
 Project-URL: homepage, https://socon.readthedocs.io/en/latest/
 Project-URL: repository, https://github.com/socon-dev/socon
 Project-URL: changelog, https://github.com/socon-dev/socon/blob/master/docs/internals/changelog.txt
 Keywords: projects,socon,scripts,commands
```

### Comparing `socon-0.2rc1/socon.egg-info/SOURCES.txt` & `socon-0.2rc2/socon.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/README.rst` & `socon-0.2rc2/tests/README.rst`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/admin_scripts/management/commands/base_command.py` & `socon-0.2rc2/tests/admin_scripts/management/commands/base_command.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/admin_scripts/tests.py` & `socon-0.2rc2/tests/admin_scripts/tests.py`

 * *Files 0% similar despite different names*

```diff
@@ -11,16 +11,18 @@
 from argparse import Namespace
 from pathlib import Path
 
 import pytest
 
 from socon import conf, get_version
 from socon.core.exceptions import ImproperlyConfigured
+from socon.core.management import call_command
 from socon.core.management.base import Config
 from socon.core.management.subcommand import Subcommand
+from socon.test.utils import override_settings
 
 
 class AdminScriptTestCase:
     def run_test(self, args, test_dir, settings_file=None, projects=None):
         """Start a subprocess using either the manage.py or the socon module"""
         base_dir = os.path.dirname(test_dir)
         # The base dir for Socon's tests is one level up.
@@ -1386,14 +1388,34 @@
             "--extras",
             "test",
         ]
         out, err = self.run_manage(args, test_dir)
         assert err == ""
         assert "['--extras', 'test']" in out
 
-    def test_subcommand_manager_not_found(self, test_dir):
+    def test_subcommand_manager_not_found(self):
         """Each subcommand must be attached to a manager"""
         msg = "NoSubcommandManager class must link a subcommand manager"
         with pytest.raises(ImproperlyConfigured, match=msg):
 
             class NoSubcommandManager(Subcommand):
                 name = "no-sub-manager"
+
+    @override_settings(INSTALLED_PROJECTS=["admin_scripts.subcommands"])
+    def test_call_subcommand_with_call_command(self, capsys):
+        """Call a subcommand from call_command method"""
+        call_command("base-subcommand", "sub1", "--project", "subcommands")
+        captured = capsys.readouterr()
+        assert captured.out == "Subcommand of base-subcommand\n"
+
+    @override_settings(INSTALLED_PROJECTS=["admin_scripts.subcommands"])
+    def test_call_main_sub_command_with_call_command(self, capsys):
+        """Call a subcommand from call_command method"""
+        with pytest.raises(SystemExit) as pytest_wrapped_e:
+            call_command("base-subcommand", "--project", "subcommands")
+        assert pytest_wrapped_e.type == SystemExit
+        assert pytest_wrapped_e.value.code == 0
+        captured = capsys.readouterr()
+        assert "usage: base-subcommand SUBCOMMAND" in captured.out
+        assert "List of available subcommands:" in captured.out
+        assert "sub1" in captured.out
+        assert "sub2" in captured.out
```

### Comparing `socon-0.2rc1/tests/conftest.py` & `socon-0.2rc2/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/manager/tests.py` & `socon-0.2rc2/tests/manager/tests.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/registry/tests.py` & `socon-0.2rc2/tests/registry/tests.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/reshape/tests.py` & `socon-0.2rc2/tests/reshape/tests.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/settings_tests/tests.py` & `socon-0.2rc2/tests/settings_tests/tests.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/user_commands/management/commands/launch.py` & `socon-0.2rc2/tests/user_commands/management/commands/launch.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/user_commands/tests.py` & `socon-0.2rc2/tests/user_commands/tests.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/utils/test_log.py` & `socon-0.2rc2/tests/utils/test_log.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/utils/test_module_loading.py` & `socon-0.2rc2/tests/utils/test_module_loading.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/utils/test_terminal.py` & `socon-0.2rc2/tests/utils/test_terminal.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tests/utils/test_version.py` & `socon-0.2rc2/tests/utils/test_version.py`

 * *Files identical despite different names*

### Comparing `socon-0.2rc1/tox.ini` & `socon-0.2rc2/tox.ini`

 * *Files identical despite different names*

