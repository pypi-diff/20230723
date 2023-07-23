# Comparing `tmp/pyqtribbon-0.7.3.tar.gz` & `tmp/pyqtribbon-0.7.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyqtribbon-0.7.3.tar", last modified: Sun Apr  9 16:25:55 2023, max compression
+gzip compressed data, was "pyqtribbon-0.7.4.tar", last modified: Sun Jul 23 08:51:28 2023, max compression
```

## Comparing `pyqtribbon-0.7.3.tar` & `pyqtribbon-0.7.4.tar`

### file list

```diff
@@ -1,134 +1,136 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.086497 pyqtribbon-0.7.3/
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/.flake8
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.058497 pyqtribbon-0.7.3/.github/
--rw-r--r--   0 runner    (1001) docker     (123)     1144 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/.github/release-drafter.yml
--rw-r--r--   0 runner    (1001) docker     (123)      522 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/.github/release.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.062497 pyqtribbon-0.7.3/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1061 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/.github/workflows/publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)      990 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/.github/workflows/release-drafter.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1085 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/.github/workflows/tests.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1876 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      231 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/.readthedocs.yml
--rw-r--r--   0 runner    (1001) docker     (123)     4525 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/CHANGE_LOG.md
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     5677 2023-04-09 16:25:55.086497 pyqtribbon-0.7.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4680 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.062497 pyqtribbon-0.7.3/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      638 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)      769 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)      139 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.062497 pyqtribbon-0.7.3/docs/source/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.066497 pyqtribbon-0.7.3/docs/source/_examples/
--rw-r--r--   0 runner    (1001) docker     (123)      161 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/build.py
--rw-r--r--   0 runner    (1001) docker     (123)    10141 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/category.png
--rw-r--r--   0 runner    (1001) docker     (123)     1656 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/category.py
--rw-r--r--   0 runner    (1001) docker     (123)    25735 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/panel.png
--rw-r--r--   0 runner    (1001) docker     (123)     2443 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/panel.py
--rw-r--r--   0 runner    (1001) docker     (123)     1904 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/python.png
--rw-r--r--   0 runner    (1001) docker     (123)     6713 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/ribbonbar-customize.png
--rw-r--r--   0 runner    (1001) docker     (123)      872 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/ribbonbar-customize.py
--rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/ribbonbar.png
--rw-r--r--   0 runner    (1001) docker     (123)      494 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/ribbonbar.py
--rw-r--r--   0 runner    (1001) docker     (123)    26937 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/tutorial-ribbonbar.png
--rw-r--r--   0 runner    (1001) docker     (123)     1656 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_examples/tutorial-ribbonbar.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.066497 pyqtribbon-0.7.3/docs/source/_images/
--rw-r--r--   0 runner    (1001) docker     (123)    44571 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_images/example.png
--rw-r--r--   0 runner    (1001) docker     (123)    57874 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_images/main-interface.png
--rw-r--r--   0 runner    (1001) docker     (123)    11093 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_images/ribbon.png
--rw-r--r--   0 runner    (1001) docker     (123)     6456 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/_images/ribbon_no_callouts.png
--rw-r--r--   0 runner    (1001) docker     (123)     5416 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)      367 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/getting-started.rst
--rw-r--r--   0 runner    (1001) docker     (123)      924 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2154 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/ribbon.rst
--rw-r--r--   0 runner    (1001) docker     (123)     5980 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/docs/source/user.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.074497 pyqtribbon-0.7.3/examples/
--rw-r--r--   0 runner    (1001) docker     (123)     2520 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/bold.png
--rw-r--r--   0 runner    (1001) docker     (123)     2095 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/copy-to-clipboard.png
--rw-r--r--   0 runner    (1001) docker     (123)      920 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/copy.png
--rw-r--r--   0 runner    (1001) docker     (123)     3198 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/cut.png
--rw-r--r--   0 runner    (1001) docker     (123)     2858 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/decrease-font.png
--rw-r--r--   0 runner    (1001) docker     (123)     3065 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/increase-font.png
--rw-r--r--   0 runner    (1001) docker     (123)     1793 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/italic.png
--rw-r--r--   0 runner    (1001) docker     (123)     1439 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/lowercase.png
--rw-r--r--   0 runner    (1001) docker     (123)     2416 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/painter.png
--rw-r--r--   0 runner    (1001) docker     (123)     1512 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/paste-as-text.png
--rw-r--r--   0 runner    (1001) docker     (123)     2151 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/paste-shortcut.png
--rw-r--r--   0 runner    (1001) docker     (123)     2301 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/paste-special.png
--rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/paste.png
--rw-r--r--   0 runner    (1001) docker     (123)     1728 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/redo.png
--rw-r--r--   0 runner    (1001) docker     (123)     2256 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/save.png
--rw-r--r--   0 runner    (1001) docker     (123)     1127 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/strikethrough.png
--rw-r--r--   0 runner    (1001) docker     (123)     3849 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/subscript.png
--rw-r--r--   0 runner    (1001) docker     (123)     3911 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/superscript.png
--rw-r--r--   0 runner    (1001) docker     (123)     2746 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/text-color.png
--rw-r--r--   0 runner    (1001) docker     (123)     2236 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/underline.png
--rw-r--r--   0 runner    (1001) docker     (123)     1973 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/undo.png
--rw-r--r--   0 runner    (1001) docker     (123)     2052 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/word.png
--rw-r--r--   0 runner    (1001) docker     (123)     3137 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/examples/word.py
--rw-r--r--   0 runner    (1001) docker     (123)    12500 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/main.py
--rw-r--r--   0 runner    (1001) docker     (123)     2113 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyproject.toml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.078498 pyqtribbon-0.7.3/pyqtribbon/
--rw-r--r--   0 runner    (1001) docker     (123)      181 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-04-09 16:25:54.000000 pyqtribbon-0.7.3/pyqtribbon/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)    15829 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/category.py
--rw-r--r--   0 runner    (1001) docker     (123)     1112 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)    12244 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/gallery.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.082497 pyqtribbon-0.7.3/pyqtribbon/icons/
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/backward.png
--rw-r--r--   0 runner    (1001) docker     (123)     2377 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/close.png
--rw-r--r--   0 runner    (1001) docker     (123)      487 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/down.png
--rw-r--r--   0 runner    (1001) docker     (123)      438 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/forward.png
--rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/help.png
--rw-r--r--   0 runner    (1001) docker     (123)      662 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/linking.png
--rw-r--r--   0 runner    (1001) docker     (123)      663 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/max.png
--rw-r--r--   0 runner    (1001) docker     (123)      751 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/min.png
--rw-r--r--   0 runner    (1001) docker     (123)      597 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/more.png
--rw-r--r--   0 runner    (1001) docker     (123)     1904 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/python.png
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/redo.png
--rw-r--r--   0 runner    (1001) docker     (123)     1036 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/save.png
--rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/undo.png
--rw-r--r--   0 runner    (1001) docker     (123)      492 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/icons/up.png
--rw-r--r--   0 runner    (1001) docker     (123)     2161 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     3610 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/menu.py
--rw-r--r--   0 runner    (1001) docker     (123)    24026 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/panel.py
--rw-r--r--   0 runner    (1001) docker     (123)    16461 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/panel.pyi
--rw-r--r--   0 runner    (1001) docker     (123)    22223 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/ribbonbar.py
--rw-r--r--   0 runner    (1001) docker     (123)     1076 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/screenshotwindow.py
--rw-r--r--   0 runner    (1001) docker     (123)     3522 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/separator.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.082497 pyqtribbon-0.7.3/pyqtribbon/styles/
--rw-r--r--   0 runner    (1001) docker     (123)      907 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/styles/base.qss
--rw-r--r--   0 runner    (1001) docker     (123)     1829 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/styles/debug.qss
--rw-r--r--   0 runner    (1001) docker     (123)      248 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/styles/default.qss
--rw-r--r--   0 runner    (1001) docker     (123)     3275 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/tabbar.py
--rw-r--r--   0 runner    (1001) docker     (123)    11359 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/titlewidget.py
--rw-r--r--   0 runner    (1001) docker     (123)     3670 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/toolbutton.py
--rw-r--r--   0 runner    (1001) docker     (123)      237 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1030 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/pyqtribbon/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.078498 pyqtribbon-0.7.3/pyqtribbon.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5677 2023-04-09 16:25:55.000000 pyqtribbon-0.7.3/pyqtribbon.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2939 2023-04-09 16:25:55.000000 pyqtribbon-0.7.3/pyqtribbon.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-09 16:25:55.000000 pyqtribbon-0.7.3/pyqtribbon.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      370 2023-04-09 16:25:55.000000 pyqtribbon-0.7.3/pyqtribbon.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-04-09 16:25:55.000000 pyqtribbon-0.7.3/pyqtribbon.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.082497 pyqtribbon-0.7.3/requirements/
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/requirements/PyQt5.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/requirements/PyQt6.txt
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/requirements/PySide2.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/requirements/PySide6.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/requirements/deps.txt
--rw-r--r--   0 runner    (1001) docker     (123)       58 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/requirements/dev.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.082497 pyqtribbon-0.7.3/screenshots/
--rw-r--r--   0 runner    (1001) docker     (123)    44120 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/screenshots/main.png
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-09 16:25:55.086497 pyqtribbon-0.7.3/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:55.086497 pyqtribbon-0.7.3/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1325 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/test_categories.py
--rw-r--r--   0 runner    (1001) docker     (123)      536 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/test_category.py
--rw-r--r--   0 runner    (1001) docker     (123)      731 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/test_filemenu.py
--rw-r--r--   0 runner    (1001) docker     (123)     1676 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/test_gallery.py
--rw-r--r--   0 runner    (1001) docker     (123)    12497 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/test_main.py
--rw-r--r--   0 runner    (1001) docker     (123)      919 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/test_panel.py
--rw-r--r--   0 runner    (1001) docker     (123)      417 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/test_ribbonbar.py
--rw-r--r--   0 runner    (1001) docker     (123)      874 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/test_titlewidget.py
--rw-r--r--   0 runner    (1001) docker     (123)     3503 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tests/test_use_dictionary_to_create_widgets.py
--rw-r--r--   0 runner    (1001) docker     (123)      499 2023-04-09 16:25:43.000000 pyqtribbon-0.7.3/tox.ini
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.206732 pyqtribbon-0.7.4/
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/.flake8
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.194732 pyqtribbon-0.7.4/.github/
+-rw-r--r--   0 runner    (1001) docker     (123)     1144 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/.github/release-drafter.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      522 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/.github/release.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.194732 pyqtribbon-0.7.4/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1061 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/.github/workflows/publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      990 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/.github/workflows/release-drafter.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1085 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/.github/workflows/tests.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1895 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      317 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      231 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/.readthedocs.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     4525 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/CHANGE_LOG.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     5677 2023-07-23 08:51:28.206732 pyqtribbon-0.7.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4680 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.194732 pyqtribbon-0.7.4/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      638 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)      769 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.194732 pyqtribbon-0.7.4/docs/source/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.198732 pyqtribbon-0.7.4/docs/source/_examples/
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/build.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10141 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/category.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1749 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/category.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25735 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/panel.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2443 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/panel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1904 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/python.png
+-rw-r--r--   0 runner    (1001) docker     (123)     6713 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/ribbonbar-customize.png
+-rw-r--r--   0 runner    (1001) docker     (123)      872 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/ribbonbar-customize.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/ribbonbar.png
+-rw-r--r--   0 runner    (1001) docker     (123)      494 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/ribbonbar.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26937 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/tutorial-ribbonbar.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1656 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_examples/tutorial-ribbonbar.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.198732 pyqtribbon-0.7.4/docs/source/_images/
+-rw-r--r--   0 runner    (1001) docker     (123)    44571 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_images/example.png
+-rw-r--r--   0 runner    (1001) docker     (123)    57874 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_images/main-interface.png
+-rw-r--r--   0 runner    (1001) docker     (123)    11093 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_images/ribbon.png
+-rw-r--r--   0 runner    (1001) docker     (123)     6456 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/_images/ribbon_no_callouts.png
+-rw-r--r--   0 runner    (1001) docker     (123)      122 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/apidoc.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     5443 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      367 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/getting-started.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      917 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2154 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/ribbon.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     5980 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/docs/source/user.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.202732 pyqtribbon-0.7.4/examples/
+-rw-r--r--   0 runner    (1001) docker     (123)     2520 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/bold.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2095 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/copy-to-clipboard.png
+-rw-r--r--   0 runner    (1001) docker     (123)      920 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/copy.png
+-rw-r--r--   0 runner    (1001) docker     (123)     3198 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/cut.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2858 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/decrease-font.png
+-rw-r--r--   0 runner    (1001) docker     (123)     3065 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/increase-font.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1793 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/italic.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1439 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/lowercase.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2416 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/painter.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1512 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/paste-as-text.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2151 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/paste-shortcut.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2301 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/paste-special.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/paste.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1728 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/redo.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2256 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/save.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1127 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/strikethrough.png
+-rw-r--r--   0 runner    (1001) docker     (123)     3849 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/subscript.png
+-rw-r--r--   0 runner    (1001) docker     (123)     3911 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/superscript.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2746 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/text-color.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2236 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/underline.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1973 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/undo.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2052 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/word.png
+-rw-r--r--   0 runner    (1001) docker     (123)     3054 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/examples/word.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12595 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2169 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.202732 pyqtribbon-0.7.4/pyqtribbon/
+-rw-r--r--   0 runner    (1001) docker     (123)      181 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-23 08:51:28.000000 pyqtribbon-0.7.4/pyqtribbon/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15829 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/category.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1112 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12244 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/gallery.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.206732 pyqtribbon-0.7.4/pyqtribbon/icons/
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/backward.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2377 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/close.png
+-rw-r--r--   0 runner    (1001) docker     (123)      487 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/down.png
+-rw-r--r--   0 runner    (1001) docker     (123)      438 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/forward.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/help.png
+-rw-r--r--   0 runner    (1001) docker     (123)      662 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/linking.png
+-rw-r--r--   0 runner    (1001) docker     (123)      663 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/max.png
+-rw-r--r--   0 runner    (1001) docker     (123)      751 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/min.png
+-rw-r--r--   0 runner    (1001) docker     (123)      597 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/more.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1904 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/python.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/redo.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1036 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/save.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/undo.png
+-rw-r--r--   0 runner    (1001) docker     (123)      492 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/icons/up.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2160 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3610 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/menu.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24026 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/panel.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16461 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/panel.pyi
+-rw-r--r--   0 runner    (1001) docker     (123)    22244 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/ribbonbar.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1076 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/screenshotwindow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3522 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/separator.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.206732 pyqtribbon-0.7.4/pyqtribbon/styles/
+-rw-r--r--   0 runner    (1001) docker     (123)      907 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/styles/base.qss
+-rw-r--r--   0 runner    (1001) docker     (123)     1829 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/styles/debug.qss
+-rw-r--r--   0 runner    (1001) docker     (123)      248 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/styles/default.qss
+-rw-r--r--   0 runner    (1001) docker     (123)     3273 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/tabbar.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11359 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/titlewidget.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3670 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/toolbutton.py
+-rw-r--r--   0 runner    (1001) docker     (123)      237 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1030 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/pyqtribbon/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.202732 pyqtribbon-0.7.4/pyqtribbon.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5677 2023-07-23 08:51:28.000000 pyqtribbon-0.7.4/pyqtribbon.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2986 2023-07-23 08:51:28.000000 pyqtribbon-0.7.4/pyqtribbon.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 08:51:28.000000 pyqtribbon-0.7.4/pyqtribbon.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      376 2023-07-23 08:51:28.000000 pyqtribbon-0.7.4/pyqtribbon.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-07-23 08:51:28.000000 pyqtribbon-0.7.4/pyqtribbon.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.206732 pyqtribbon-0.7.4/requirements/
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/requirements/PyQt5.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/requirements/PyQt6.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/requirements/PySide2.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/requirements/PySide6.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/requirements/deps.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       58 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/requirements/dev.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.206732 pyqtribbon-0.7.4/screenshots/
+-rw-r--r--   0 runner    (1001) docker     (123)    44120 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/screenshots/main.png
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 08:51:28.210732 pyqtribbon-0.7.4/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:28.206732 pyqtribbon-0.7.4/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1325 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/test_categories.py
+-rw-r--r--   0 runner    (1001) docker     (123)      536 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/test_category.py
+-rw-r--r--   0 runner    (1001) docker     (123)      731 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/test_filemenu.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1676 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/test_gallery.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12497 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/test_main.py
+-rw-r--r--   0 runner    (1001) docker     (123)      919 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/test_panel.py
+-rw-r--r--   0 runner    (1001) docker     (123)      417 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/test_ribbonbar.py
+-rw-r--r--   0 runner    (1001) docker     (123)      874 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/test_titlewidget.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3503 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tests/test_use_dictionary_to_create_widgets.py
+-rw-r--r--   0 runner    (1001) docker     (123)      499 2023-07-23 08:51:16.000000 pyqtribbon-0.7.4/tox.ini
```

### Comparing `pyqtribbon-0.7.3/.github/release-drafter.yml` & `pyqtribbon-0.7.4/.github/release-drafter.yml`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/.github/release.yml` & `pyqtribbon-0.7.4/.github/release.yml`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/.github/workflows/publish.yml` & `pyqtribbon-0.7.4/.github/workflows/publish.yml`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/.github/workflows/release-drafter.yml` & `pyqtribbon-0.7.4/.github/workflows/release-drafter.yml`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/.github/workflows/tests.yml` & `pyqtribbon-0.7.4/.github/workflows/tests.yml`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/.gitignore` & `pyqtribbon-0.7.4/.gitignore`

 * *Files 2% similar despite different names*

```diff
@@ -131,7 +131,8 @@
 
 # app settings
 .idea/
 .vscode/
 .vs/
 
 pyqtribbon/_version.py
+docs/source/apidoc
```

### Comparing `pyqtribbon-0.7.3/CHANGE_LOG.md` & `pyqtribbon-0.7.4/CHANGE_LOG.md`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/LICENSE` & `pyqtribbon-0.7.4/LICENSE`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/PKG-INFO` & `pyqtribbon-0.7.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyqtribbon
-Version: 0.7.3
+Version: 0.7.4
 Summary: Ribbon Bar for PyQt or PySide applications
 Author-email: WANG Hailin <hailin.wang@connect.polyu.hk>
 Project-URL: GitHub, https://github.com/haiiliin/pyqtribbon
 Project-URL: Documentation, https://pyqtribbon.haiiliin.com/en/stable/
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `pyqtribbon-0.7.3/README.md` & `pyqtribbon-0.7.4/README.md`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/Makefile` & `pyqtribbon-0.7.4/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/make.bat` & `pyqtribbon-0.7.4/docs/make.bat`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_examples/category.png` & `pyqtribbon-0.7.4/docs/source/_examples/category.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_examples/panel.png` & `pyqtribbon-0.7.4/docs/source/_examples/panel.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_examples/panel.py` & `pyqtribbon-0.7.4/docs/source/_examples/panel.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 import sys
 
 from qtpy import QtGui
-from qtpy.QtWidgets import QApplication, QToolButton, QMenu, QLabel, QLineEdit
-from qtpy.QtGui import QIcon
 from qtpy.QtCore import Qt
+from qtpy.QtGui import QIcon
+from qtpy.QtWidgets import QApplication, QLabel, QLineEdit, QMenu, QToolButton
 
 from pyqtribbon import RibbonBar
 from pyqtribbon.screenshotwindow import RibbonScreenShotWindow
 
-if __name__ == '__main__':
+if __name__ == "__main__":
     app = QApplication(sys.argv)
     app.setFont(QtGui.QFont("Times New Roman", 8))
-    window = RibbonScreenShotWindow('panel.png')
+    window = RibbonScreenShotWindow("panel.png")
 
     # Ribbon bar
     ribbonbar = RibbonBar()
     window.setMenuBar(ribbonbar)
 
     category1 = ribbonbar.addCategory("Category 1")
     panel = category1.addPanel("Panel 1", showPanelOptionButton=False)
@@ -38,17 +38,17 @@
     menu.addAction(QIcon("python.png"), "Action 3")
     button.setMenu(menu)
     button.setPopupMode(QToolButton.InstantPopup)
     panel.addWidget(button, rowSpan=6)
 
     gallery = panel.addGallery(minimumWidth=500, popupHideOnClick=True)
     for i in range(100):
-        gallery.addToggleButton(f'item {i+1}', QIcon("python.png"))
+        gallery.addToggleButton(f"item {i+1}", QIcon("python.png"))
     popupMenu = gallery.popupMenu()
-    submenu = popupMenu.addMenu(QIcon("python.png"), 'Submenu')
+    submenu = popupMenu.addMenu(QIcon("python.png"), "Submenu")
     submenu.addAction(QIcon("python.png"), "Action 4")
     popupMenu.addAction(QIcon("python.png"), "Action 1")
     popupMenu.addAction(QIcon("python.png"), "Action 2")
     popupMenu.addSeparator()
     popupMenu.addWidget(QLabel("This is a custom widget"))
     formLayout = popupMenu.addFormLayoutWidget()
     formLayout.addRow(QLabel("Row 1"), QLineEdit())
```

### Comparing `pyqtribbon-0.7.3/docs/source/_examples/python.png` & `pyqtribbon-0.7.4/docs/source/_examples/python.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_examples/ribbonbar-customize.png` & `pyqtribbon-0.7.4/docs/source/_examples/ribbonbar-customize.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_examples/ribbonbar-customize.py` & `pyqtribbon-0.7.4/docs/source/_examples/ribbonbar-customize.py`

 * *Files 10% similar despite different names*

```diff
@@ -2,34 +2,34 @@
 
 from qtpy import QtGui
 from qtpy.QtWidgets import QApplication, QToolButton
 
 from pyqtribbon import RibbonBar
 from pyqtribbon.screenshotwindow import RibbonScreenShotWindow
 
-if __name__ == '__main__':
+if __name__ == "__main__":
     app = QApplication(sys.argv)
     app.setFont(QtGui.QFont("Times New Roman", 8))
-    window = RibbonScreenShotWindow('ribbonbar-customize.png')
+    window = RibbonScreenShotWindow("ribbonbar-customize.png")
 
     # Ribbon bar
     ribbonbar = RibbonBar()
     window.setMenuBar(ribbonbar)
 
     # Title of the ribbon
-    ribbonbar.setTitle('This is my custom title')
+    ribbonbar.setTitle("This is my custom title")
 
     # Quick Access Bar
     qbutton = QToolButton()
-    qbutton.setText('Quick Button')
+    qbutton.setText("Quick Button")
     ribbonbar.addQuickAccessButton(qbutton)
 
     # Right toolbar
     rbutton = QToolButton()
-    rbutton.setText('Right Button')
+    rbutton.setText("Right Button")
     ribbonbar.addRightToolButton(rbutton)
 
     # Show the window
     window.resize(1000, 250)
     window.show()
 
     sys.exit(app.exec_())
```

### Comparing `pyqtribbon-0.7.3/docs/source/_examples/ribbonbar.png` & `pyqtribbon-0.7.4/docs/source/_examples/ribbonbar.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_examples/tutorial-ribbonbar.png` & `pyqtribbon-0.7.4/docs/source/_examples/tutorial-ribbonbar.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_examples/tutorial-ribbonbar.py` & `pyqtribbon-0.7.4/docs/source/_examples/tutorial-ribbonbar.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 import sys
 
-from PyQt5.QtWidgets import QApplication, QLabel, QWidget, QVBoxLayout
-from PyQt5.QtGui import QIcon, QFont
 from PyQt5.QtCore import Qt
+from PyQt5.QtGui import QFont, QIcon
+from PyQt5.QtWidgets import QApplication, QLabel, QVBoxLayout, QWidget
 
 from pyqtribbon import RibbonBar
 from pyqtribbon.screenshotwindow import RibbonScreenShotWindow
 from pyqtribbon.utils import DataFile
 
 if __name__ == "__main__":
     app = QApplication(sys.argv)
     app.setFont(QFont("Times New Roman", 8))
 
     # Central widget
-    window = RibbonScreenShotWindow('tutorial-ribbonbar.png')
+    window = RibbonScreenShotWindow("tutorial-ribbonbar.png")
     window.setWindowIcon(QIcon(DataFile("icons/python.png")))
     centralWidget = QWidget()
     window.setCentralWidget(centralWidget)
     layout = QVBoxLayout(centralWidget)
 
     # Ribbon bar
     ribbonbar = RibbonBar()
```

### Comparing `pyqtribbon-0.7.3/docs/source/_images/example.png` & `pyqtribbon-0.7.4/docs/source/_images/example.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_images/main-interface.png` & `pyqtribbon-0.7.4/docs/source/_images/main-interface.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_images/ribbon.png` & `pyqtribbon-0.7.4/docs/source/_images/ribbon.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/_images/ribbon_no_callouts.png` & `pyqtribbon-0.7.4/docs/source/_images/ribbon_no_callouts.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/conf.py` & `pyqtribbon-0.7.4/docs/source/conf.py`

 * *Files 12% similar despite different names*

```diff
@@ -9,71 +9,72 @@
 # If extensions (or modules to document with autodoc) are in another directory,
 # add these directories to sys.path here. If the directory is relative to the
 # documentation root, use os.path.abspath to make it absolute, like shown here.
 #
 import inspect
 import os
 import sys
+
 import pyqtribbon
 
-sys.path.insert(0, os.path.abspath('../../'))
+sys.path.insert(0, os.path.abspath("../../"))
 
 # -- Project information -----------------------------------------------------
 
-project = 'pyqtribbon'
-copyright = '2022, WANG Hailin'
-author = 'WANG Hailin'
+project = "pyqtribbon"
+copyright = "2022, WANG Hailin"
+author = "WANG Hailin"
 
 # The full version, including alpha/beta/rc tags
 release = version = pyqtribbon.__version__
 
 
 # -- General configuration ---------------------------------------------------
 
 # Add any Sphinx extension module names here, as strings. They can be
 # extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
 # ones.
 extensions = [
-    'autoapi.extension',
-    'hoverxref.extension',
-    'sphinx.ext.autosummary',
-    'sphinx.ext.autodoc',
-    'sphinx.ext.intersphinx',
-    'sphinx.ext.linkcode',
-    'sphinx.ext.napoleon',
-    'sphinx.ext.githubpages',
-    'sphinx_copybutton',
-    'sphinx_codeautolink',
-    'sphinx_toolbox.more_autodoc.overloads',
-    'sphinx_qt_documentation',
+    "hoverxref.extension",
+    "sphinx.ext.autosummary",
+    "sphinx.ext.autodoc",
+    "sphinx.ext.intersphinx",
+    "sphinx.ext.linkcode",
+    "sphinx.ext.napoleon",
+    "sphinx.ext.githubpages",
+    "sphinx_copybutton",
+    "sphinx_codeautolink",
+    "sphinx_toolbox.more_autodoc.overloads",
+    "sphinx_qt_documentation",
+    "sphinxcontrib.apidoc",
 ]
 
-qt_documentation = 'Qt5'
-autodoc_typehints_format = 'short'
+qt_documentation = "Qt5"
+autodoc_typehints_format = "short"
 numpydoc_show_inherited_class_members = False
 
 # sphinx.ext.intersphinx configuration
 intersphinx_mapping = {
-    'jinjia2': ('https://jinja.palletsprojects.com/en/3.0.x/', None),
-    'matplotlib': ('https://matplotlib.org/stable/', None),
-    'numpy': ('https://numpy.org/doc/stable/', None),
-    'pandas': ('https://pandas.pydata.org/pandas-docs/stable/', None),
-    'pytest': ('https://pytest.org/en/stable/', None),
-    'python': ('https://docs.python.org/3/', None),
-    'readthedocs': ('https://docs.readthedocs.io/en/stable/', None),
-    'scipy': ('https://docs.scipy.org/doc/scipy/', None),
+    "jinjia2": ("https://jinja.palletsprojects.com/en/3.0.x/", None),
+    "matplotlib": ("https://matplotlib.org/stable/", None),
+    "numpy": ("https://numpy.org/doc/stable/", None),
+    "pandas": ("https://pandas.pydata.org/pandas-docs/stable/", None),
+    "pytest": ("https://pytest.org/en/stable/", None),
+    "python": ("https://docs.python.org/3/", None),
+    "readthedocs": ("https://docs.readthedocs.io/en/stable/", None),
+    "scipy": ("https://docs.scipy.org/doc/scipy/", None),
 }
 
 # Hoverxref configuration
 hoverxref_auto_ref = True
 hoverxref_domains = ["py"]
 hoverxref_roles = [
-    'numref',
-    'confval',
-    'setting',
+    "numref",
+    "confval",
+    "setting",
     "option",
     "doc",  # Documentation pages
     "term",  # Glossary terms
 ]
 hoverxref_role_types = {
     "doc": "modal",  # for whole docs
     "mod": "modal",  # for Python Sphinx Domain
@@ -85,27 +86,30 @@
     "obj": "tooltip",  # for Python Sphinx Domain
     "ref": "tooltip",  # for hoverxref_auto_ref config
     "confval": "tooltip",  # for custom object
     "term": "tooltip",  # for glossaries
     "numref": "tooltip",
 }
 hoverxref_intersphinx = [
-    'numpy',
-    'pytest',
-    'python',
-    'readthedocs',
+    "numpy",
+    "pytest",
+    "python",
+    "readthedocs",
 ]
 
-# sphinx-autoapi configuration
-autoapi_options = ['members', 'show-inheritance', 'show-module-summary', 'special-members']
-autoapi_dirs = ['../../pyqtribbon']
-autoapi_ignore = ["*_version.py"]
+# sphinxcontrib-apidoc configuration
+apidoc_module_dir = "../../pyqtribbon"
+apidoc_output_dir = "apidoc"
+apidoc_excluded_paths = []
+apidoc_separate_modules = True
+apidoc_toc_file = False
+apidoc_extra_args = ["-d 1"]
 
 # sphinx.ext.autodoc configuration
-autoclass_content = 'both'
+autoclass_content = "both"
 
 
 # linkcode source
 def linkcode_resolve(domain: str, info: dict):
     """Resolve linkcode source
     Parameters
     ----------
@@ -119,54 +123,54 @@
         - cpp: names (list of names for the object)
         - javascript: object (name of the object), fullname (name of the item)
 
     Returns
     -------
     source url of the object
     """
-    if domain != 'py':
+    if domain != "py":
         return None
 
-    modname = info['module']
-    fullname = info['fullname']
+    modname = info["module"]
+    fullname = info["fullname"]
 
-    filename = modname.replace('.', '/')
-    baseurl = f'https://github.com/haiiliin/pyqtribbon/blob/main/{filename}.py'
+    filename = modname.replace(".", "/")
+    baseurl = f"https://github.com/haiiliin/pyqtribbon/blob/main/{filename}.py"
 
     submod = sys.modules.get(modname)
     if submod is None:
         return baseurl
 
     obj = submod
-    for part in fullname.split('.'):
+    for part in fullname.split("."):
         try:
             obj = getattr(obj, part)
         except Exception:
             return baseurl
     try:
         source, lineno = inspect.getsourcelines(obj)
     except Exception:
         return baseurl
 
-    return baseurl + f'#L{lineno}-L{lineno + len(source) - 1}'
+    return baseurl + f"#L{lineno}-L{lineno + len(source) - 1}"
 
 
 # Add any paths that contain templates here, relative to this directory.
-templates_path = ['_templates']
+templates_path = ["_templates"]
 
 # List of patterns, relative to source directory, that match files and
 # directories to ignore when looking for source files.
 # This pattern also affects html_static_path and html_extra_path.
 exclude_patterns = []
 
 
 # -- Options for HTML output -------------------------------------------------
 
 # The theme to use for HTML and HTML Help pages.  See the documentation for
 # a list of builtin themes.
 #
-html_theme = 'sphinx_rtd_theme'
+html_theme = "sphinx_rtd_theme"
 
 # Add any paths that contain custom static files (such as style sheets) here,
 # relative to this directory. They are copied after the builtin static files,
 # so a file named "default.css" will overwrite the builtin "default.css".
-html_static_path = ['_static']
+html_static_path = ["_static"]
```

### Comparing `pyqtribbon-0.7.3/docs/source/index.rst` & `pyqtribbon-0.7.4/docs/source/index.rst`

 * *Files 11% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 .. toctree::
    :maxdepth: 2
    :caption: Contents:
 
    getting-started
    ribbon
    user
-   autoapi/index
+   apidoc
 
 Indices and tables
 ==================
 
 * :ref:`genindex`
 * :ref:`modindex`
 * :ref:`search`
```

### Comparing `pyqtribbon-0.7.3/docs/source/ribbon.rst` & `pyqtribbon-0.7.4/docs/source/ribbon.rst`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/docs/source/user.rst` & `pyqtribbon-0.7.4/docs/source/user.rst`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/bold.png` & `pyqtribbon-0.7.4/examples/bold.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/copy-to-clipboard.png` & `pyqtribbon-0.7.4/examples/copy-to-clipboard.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/copy.png` & `pyqtribbon-0.7.4/examples/copy.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/cut.png` & `pyqtribbon-0.7.4/examples/cut.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/decrease-font.png` & `pyqtribbon-0.7.4/examples/decrease-font.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/increase-font.png` & `pyqtribbon-0.7.4/examples/increase-font.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/italic.png` & `pyqtribbon-0.7.4/examples/italic.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/lowercase.png` & `pyqtribbon-0.7.4/examples/lowercase.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/painter.png` & `pyqtribbon-0.7.4/examples/painter.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/paste-as-text.png` & `pyqtribbon-0.7.4/examples/paste-as-text.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/paste-shortcut.png` & `pyqtribbon-0.7.4/examples/paste-shortcut.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/paste-special.png` & `pyqtribbon-0.7.4/examples/paste-special.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/paste.png` & `pyqtribbon-0.7.4/examples/paste.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/redo.png` & `pyqtribbon-0.7.4/examples/redo.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/save.png` & `pyqtribbon-0.7.4/examples/save.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/strikethrough.png` & `pyqtribbon-0.7.4/examples/strikethrough.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/subscript.png` & `pyqtribbon-0.7.4/examples/subscript.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/superscript.png` & `pyqtribbon-0.7.4/examples/superscript.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/text-color.png` & `pyqtribbon-0.7.4/examples/text-color.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/underline.png` & `pyqtribbon-0.7.4/examples/underline.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/undo.png` & `pyqtribbon-0.7.4/examples/undo.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/word.png` & `pyqtribbon-0.7.4/examples/word.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/examples/word.py` & `pyqtribbon-0.7.4/examples/word.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import sys
 
-from qtpy import QtWidgets, QtGui
+from qtpy import QtGui, QtWidgets
 from qtpy.QtGui import QIcon
+
 from pyqtribbon import RibbonBar
 
 if __name__ == "__main__":
     app = QtWidgets.QApplication(sys.argv)
     app.setFont(QtGui.QFont("Times New Roman", 8))
 
     window = QtWidgets.QMainWindow()
@@ -26,33 +27,37 @@
     homeCategory = ribbonbar.addCategory("Home")
     undoPanel = homeCategory.addPanel("Undo")
     undoPanel.addMediumButton("Undo", icon=QIcon("undo.png"))
     undoPanel.addMediumButton("Redo", icon=QIcon("redo.png"))
 
     clipboardPanel = homeCategory.addPanel("Clipboard")
     pasteButton = clipboardPanel.addLargeButton("Paste", icon=QIcon("paste.png"), tooltip="Paste")
-    pasteButton.addAction(QtWidgets.QAction(QIcon('paste-special.png'), "Paste Special"))
-    pasteButton.addAction(QtWidgets.QAction(QIcon('paste-as-text.png'), "Paste as Text"))
+    pasteButton.addAction(QtWidgets.QAction(QIcon("paste-special.png"), "Paste Special"))
+    pasteButton.addAction(QtWidgets.QAction(QIcon("paste-as-text.png"), "Paste as Text"))
     clipboardPanel.addSmallButton("Cut", icon=QIcon("cut.png"), showText=False, tooltip="Cut")
     clipboardPanel.addSmallButton("Copy", icon=QIcon("copy.png"), showText=False, tooltip="Copy")
     clipboardPanel.addSmallButton("Painter", icon=QIcon("painter.png"), showText=False, tooltip="Format Painter")
 
     fontPanel = homeCategory.addPanel("Font")
     fontComboBox = fontPanel.addFontComboBox(rowSpan=3, colSpan=6)
     fontPanel.addSmallToggleButton("Bold", icon=QIcon("bold.png"), showText=False, tooltip="Bold")
     fontPanel.addSmallToggleButton("Italic", icon=QIcon("italic.png"), showText=False, tooltip="Italic")
     fontPanel.addSmallToggleButton("Underline", icon=QIcon("underline.png"), showText=False, tooltip="Underline")
-    fontPanel.addSmallToggleButton("Strikethrough", icon=QIcon("strikethrough.png"), showText=False,
-                                   tooltip="Strikethrough")
+    fontPanel.addSmallToggleButton(
+        "Strikethrough", icon=QIcon("strikethrough.png"), showText=False, tooltip="Strikethrough"
+    )
     fontPanel.addSmallToggleButton("Superscript", icon=QIcon("superscript.png"), showText=False, tooltip="Superscript")
     fontPanel.addSmallToggleButton("Subscript", icon=QIcon("subscript.png"), showText=False, tooltip="Subscript")
-    fontSizeComboBox = fontPanel.addComboBox(['8', '9', '10'], rowSpan=3, colSpan=2)
-    fontPanel.addSmallToggleButton("Increase Font Size", icon=QIcon("increase-font.png"),
-                                   showText=False, tooltip="Increase Font Size")
-    fontPanel.addSmallToggleButton("Decrease Font Size", icon=QIcon("decrease-font.png"),
-                                   showText=False, tooltip="Decrease Font Size")
-    fontPanel.addSmallToggleButton("Decrease Font Size", icon=QIcon("decrease-font.png"),
-                                   showText=False, tooltip="Decrease Font Size")
+    fontSizeComboBox = fontPanel.addComboBox(["8", "9", "10"], rowSpan=3, colSpan=2)
+    fontPanel.addSmallToggleButton(
+        "Increase Font Size", icon=QIcon("increase-font.png"), showText=False, tooltip="Increase Font Size"
+    )
+    fontPanel.addSmallToggleButton(
+        "Decrease Font Size", icon=QIcon("decrease-font.png"), showText=False, tooltip="Decrease Font Size"
+    )
+    fontPanel.addSmallToggleButton(
+        "Decrease Font Size", icon=QIcon("decrease-font.png"), showText=False, tooltip="Decrease Font Size"
+    )
 
     window.resize(1500, 1000)
     window.show()
     sys.exit(app.exec_())
```

### Comparing `pyqtribbon-0.7.3/main.py` & `pyqtribbon-0.7.4/main.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import sys
 
-from qtpy import QtWidgets, QtGui, QtCore
+from qtpy import QtCore, QtGui, QtWidgets
 from qtpy.QtGui import QIcon
 
-from pyqtribbon import RibbonBar, Large, Normal
+from pyqtribbon import Large, Normal, RibbonBar
 from pyqtribbon.ribbonbar import RibbonStyle
 
 if __name__ == "__main__":
     app = QtWidgets.QApplication(sys.argv)
     app.setFont(QtGui.QFont("Times New Roman", 10))
     app.setStyle("Windows")
 
@@ -43,17 +43,17 @@
     panel = category1.addPanel("Panel 1", showPanelOptionButton=False)
     panel.addSmallButton("Button 1", icon=QIcon("pyqtribbon/icons/close.png"))
     panel.addSmallButton("Button 2", icon=QIcon("pyqtribbon/icons/close.png"))
     panel.addSmallButton("Button 3", icon=QIcon("pyqtribbon/icons/close.png"))
     showCategoryButton2 = panel.addMediumToggleButton("Show/Hide Category 2", icon=QIcon("pyqtribbon/icons/close.png"))
     panel.addVerticalSeparator()
     showCategoryButton3 = panel.addMediumToggleButton("Show/Hide Category 3", icon=QIcon("pyqtribbon/icons/close.png"))
-    showCategoryButton45 = panel.addMediumToggleButton("Show/Hide Category 4/5",
-                                                       icon=QIcon("pyqtribbon/icons/close.png"),
-                                                       colSpan=2, alignment=QtCore.Qt.AlignLeft)
+    showCategoryButton45 = panel.addMediumToggleButton(
+        "Show/Hide Category 4/5", icon=QIcon("pyqtribbon/icons/close.png"), colSpan=2, alignment=QtCore.Qt.AlignLeft
+    )
     panel.addLargeButton("Button 6", icon=QIcon("pyqtribbon/icons/close.png"))
     panel.addVerticalSeparator()
     panel.addMediumButton("Button 7", icon=QIcon("pyqtribbon/icons/close.png"))
     panel.addMediumButton("Button 8", icon=QIcon("pyqtribbon/icons/close.png"))
 
     saveButton = panel.addLargeButton("Button 8", icon=QIcon("pyqtribbon/icons/close.png"))
     menu = QtWidgets.QMenu()
@@ -80,15 +80,15 @@
     saveButton.setPopupMode(QtWidgets.QToolButton.DelayedPopup)
 
     saveButton = panel.addLargeButton("Button 11", icon=QIcon("pyqtribbon/icons/close.png"))
     menu = saveButton.addRibbonMenu()
     menu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 1")
     menu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 2")
     menu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 3")
-    submenu = menu.addMenu(QIcon("pyqtribbon/icons/close.png"), 'Submenu')
+    submenu = menu.addMenu(QIcon("pyqtribbon/icons/close.png"), "Submenu")
     submenu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 4")
     submenu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 5")
     submenu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 6")
     menu.addSpacing()
     menu.addLabel("This is a custom widget")
     formLayout = menu.addFormLayoutWidget()
     formLayout.addRow(QtWidgets.QLabel("Row 1"), QtWidgets.QLineEdit())
@@ -99,26 +99,28 @@
     button = panel.addMediumButton("Button 8", icon=QIcon("pyqtribbon/icons/close.png"))
     menu = QtWidgets.QMenu()
     menu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 1")
     menu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 2")
     menu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 3")
     button.setMenu(menu)
     panel.addMediumButton("Button 9", icon=QIcon("pyqtribbon/icons/close.png"))
-    panel.addSmallButton("This is a very very very very very long button",
-                         icon=QIcon("pyqtribbon/icons/close.png"), colSpan=3)
+    panel.addSmallButton(
+        "This is a very very very very very long button", icon=QIcon("pyqtribbon/icons/close.png"), colSpan=3
+    )
     button = panel.addSmallToggleButton("Button 10", icon=QIcon("pyqtribbon/icons/close.png"))
     menu = QtWidgets.QMenu()
     menu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 1")
     menu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 2")
     menu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 3")
     button.setMenu(menu)
     panel.addSmallToggleButton("Button 11", icon=QIcon("pyqtribbon/icons/close.png"))
     panel.addSmallToggleButton("Button 12", icon=QIcon("pyqtribbon/icons/close.png"))
-    panel.addSmallButton("This is a very very very very very long button",
-                         icon=QIcon("pyqtribbon/icons/close.png"), colSpan=3)
+    panel.addSmallButton(
+        "This is a very very very very very long button", icon=QIcon("pyqtribbon/icons/close.png"), colSpan=3
+    )
 
     category2 = ribbon.addContextCategory("Context 2")
     panel = category2.addPanel("Panel 1")
     panel.addSmallButton("Button 1", icon=QIcon("pyqtribbon/icons/close.png"))
     panel.addSmallButton("Button 2", icon=QIcon("pyqtribbon/icons/close.png"))
     panel.addSmallButton("Button 3", icon=QIcon("pyqtribbon/icons/close.png"))
     panel.addMediumButton("Button 4", icon=QIcon("pyqtribbon/icons/close.png"))
@@ -164,87 +166,89 @@
     panel.addLargeButton("Button 3", icon=QIcon("pyqtribbon/icons/close.png"))
 
     showCategoryButton2.clicked.connect(category2.setCategoryVisible)  # type: ignore
     showCategoryButton3.clicked.connect(lambda checked: category3.setCategoryVisible(not category3.categoryVisible()))  # type: ignore
 
     gallery = panel.addGallery(popupHideOnClick=True)
     for i in range(100):
-        gallery.addToggleButton(f'item {i+1}', QIcon("pyqtribbon/icons/close.png"))
+        gallery.addToggleButton(f"item {i+1}", QIcon("pyqtribbon/icons/close.png"))
     popupMenu = gallery.popupMenu()
-    submenu = popupMenu.addMenu(QIcon("pyqtribbon/icons/close.png"), 'Submenu')
+    submenu = popupMenu.addMenu(QIcon("pyqtribbon/icons/close.png"), "Submenu")
     submenu.addAction(QIcon("pyqtribbon/icons/close.png"), "Action 4")
     popupMenu.addAction(QtGui.QIcon("pyqtribbon/icons/close.png"), "Action 1")
     popupMenu.addAction(QtGui.QIcon("pyqtribbon/icons/close.png"), "Action 2")
     popupMenu.addSeparator()
     popupMenu.addWidget(QtWidgets.QLabel("This is a custom widget"))
     formLayout = popupMenu.addFormLayoutWidget()
     formLayout.addRow(QtWidgets.QLabel("Row 1"), QtWidgets.QLineEdit())
 
-    categories = ribbon.addContextCategories('name', ['Context 4', 'Context 5'])
+    categories = ribbon.addContextCategories("name", ["Context 4", "Context 5"])
     showCategoryButton45.clicked.connect(lambda v: categories.setCategoriesVisible(v))  # PySide2 Bug: use lambda
 
-    panel1 = categories['Context 4'].addPanel('Context 4 Panel 1')
-    panel1.addLargeButton('Button 1', icon=QIcon('pyqtribbon/icons/close.png'))
-    panel1.addLargeButton('Button 2', icon=QIcon('pyqtribbon/icons/close.png'))
-    panel1.addLargeButton('Button 3', icon=QIcon('pyqtribbon/icons/close.png'))
-
-    panel2 = categories['Context 5'].addPanel('Context 5 Panel 1')
-    panel2.addLargeButton('Button 4', icon=QIcon('pyqtribbon/icons/close.png'))
-    panel2.addLargeButton('Button 5', icon=QIcon('pyqtribbon/icons/close.png'))
-    panel2.addLargeButton('Button 6', icon=QIcon('pyqtribbon/icons/close.png'))
-
-    categories1 = ribbon.addCategoriesBy({
-        'Category 6': {
-            "style": Normal,
-            "panels": {
-                "Panel 1": {
-                    "showPanelOptionButton": True,
-                    "widgets": {
-                        "Button 1": {
-                            "type": "Button",
-                            "arguments": {
-                                "icon": QIcon("pyqtribbon/icons/close.png"),
-                                "text": "Button",
-                                "tooltip": "This is a tooltip",
-                            }
+    panel1 = categories["Context 4"].addPanel("Context 4 Panel 1")
+    panel1.addLargeButton("Button 1", icon=QIcon("pyqtribbon/icons/close.png"))
+    panel1.addLargeButton("Button 2", icon=QIcon("pyqtribbon/icons/close.png"))
+    panel1.addLargeButton("Button 3", icon=QIcon("pyqtribbon/icons/close.png"))
+
+    panel2 = categories["Context 5"].addPanel("Context 5 Panel 1")
+    panel2.addLargeButton("Button 4", icon=QIcon("pyqtribbon/icons/close.png"))
+    panel2.addLargeButton("Button 5", icon=QIcon("pyqtribbon/icons/close.png"))
+    panel2.addLargeButton("Button 6", icon=QIcon("pyqtribbon/icons/close.png"))
+
+    categories1 = ribbon.addCategoriesBy(
+        {
+            "Category 6": {
+                "style": Normal,
+                "panels": {
+                    "Panel 1": {
+                        "showPanelOptionButton": True,
+                        "widgets": {
+                            "Button 1": {
+                                "type": "Button",
+                                "arguments": {
+                                    "icon": QIcon("pyqtribbon/icons/close.png"),
+                                    "text": "Button",
+                                    "tooltip": "This is a tooltip",
+                                },
+                            },
+                            "Button 2": {
+                                "type": "Button",
+                                "arguments": {
+                                    "icon": QIcon("pyqtribbon/icons/close.png"),
+                                    "text": "Button 2",
+                                    "tooltip": "This is a tooltip",
+                                },
+                            },
                         },
-                        "Button 2": {
-                            "type": "Button",
-                            "arguments": {
-                                "icon": QIcon("pyqtribbon/icons/close.png"),
-                                "text": "Button 2",
-                                "tooltip": "This is a tooltip",
-                            }
+                    },
+                    "Panel 2": {
+                        "showPanelOptionButton": True,
+                        "widgets": {
+                            "Button 3": {
+                                "type": "Button",
+                                "arguments": {
+                                    "icon": QIcon("pyqtribbon/icons/close.png"),
+                                    "text": "Button 3",
+                                    "tooltip": "This is a tooltip",
+                                },
+                            },
+                            "Button 4": {
+                                "type": "Button",
+                                "arguments": {
+                                    "icon": QIcon("pyqtribbon/icons/close.png"),
+                                    "text": "Button 4",
+                                    "tooltip": "This is a tooltip",
+                                },
+                            },
                         },
-                    }
-                },
-                "Panel 2": {
-                    "showPanelOptionButton": True,
-                    "widgets": {
-                        "Button 3": {
-                            "type": "Button",
-                            "arguments": {
-                                "icon": QIcon("pyqtribbon/icons/close.png"),
-                                "text": "Button 3",
-                                "tooltip": "This is a tooltip",
-                            }
-                        },
-                        "Button 4": {
-                            "type": "Button",
-                            "arguments": {
-                                "icon": QIcon("pyqtribbon/icons/close.png"),
-                                "text": "Button 4",
-                                "tooltip": "This is a tooltip",
-                            }
-                        },
-                    }
+                    },
                 },
             }
         }
-    })
+    )
 
     label = QtWidgets.QLabel("Ribbon Test Window")
     label.setFont(QtGui.QFont("Arial", 20))
     label.setAlignment(QtCore.Qt.AlignCenter)
     layout.addWidget(label, 1)
 
     window.resize(1800, 350)
```

### Comparing `pyqtribbon-0.7.3/pyproject.toml` & `pyqtribbon-0.7.4/pyproject.toml`

 * *Files 7% similar despite different names*

```diff
@@ -57,8 +57,11 @@
 [tool.pytest.ini_options]
 testpaths = ["pyqtribbon", "tests"]
 addopts = "-rf -s --cov=pyqtribbon --cov-report=xml --cov-report=html --cov-report=term-missing --doctest-modules"
 
 [tool.black]
 line-length = 120
 target-version = ['py37', 'py38', 'py39', 'py310', 'py311']
-include = '(pyqtribbon/.*\.py|tests/.*\.py)'
+include = '(pyqtribbon/.*\.py|tests/.*\.py|docs/source/conf\.py)'
+
+[tool.isort]
+profile = "black"
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/category.py` & `pyqtribbon-0.7.4/pyqtribbon/category.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import typing
 
-from qtpy import QtWidgets, QtCore, QtGui
+from qtpy import QtCore, QtGui, QtWidgets
 
 from .constants import RibbonCategoryStyle
 from .panel import RibbonPanel
 from .separator import RibbonSeparator
 from .utils import DataFile
 
 if typing.TYPE_CHECKING:
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/constants.py` & `pyqtribbon-0.7.4/pyqtribbon/constants.py`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/gallery.py` & `pyqtribbon-0.7.4/pyqtribbon/gallery.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import typing
 
-from qtpy import QtWidgets, QtGui, QtCore
+from qtpy import QtCore, QtGui, QtWidgets
 
 from .menu import RibbonPermanentMenu
 from .separator import RibbonHorizontalSeparator
 from .toolbutton import RibbonToolButton
 from .utils import DataFile
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/close.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/close.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/help.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/help.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/linking.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/linking.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/max.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/max.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/min.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/min.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/more.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/more.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/python.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/python.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/redo.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/redo.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/save.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/save.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/icons/undo.png` & `pyqtribbon-0.7.4/pyqtribbon/icons/undo.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/logger.py` & `pyqtribbon-0.7.4/pyqtribbon/logger.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,14 @@
 """
 import logging
 import sys
 import traceback
 
 from qtpy import QtCore, QtWidgets
 
-
 log = logging.getLogger(__name__)
 log.addHandler(logging.StreamHandler(stream=sys.stdout))
 
 
 class UncaughtHook(QtCore.QObject):
     def __init__(self, *args, **kwargs):
         super(UncaughtHook, self).__init__(*args, **kwargs)
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/menu.py` & `pyqtribbon-0.7.4/pyqtribbon/menu.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import typing
 
-from qtpy import QtWidgets, QtCore, QtGui
+from qtpy import QtCore, QtGui, QtWidgets
 
 
 class RibbonMenu(QtWidgets.QMenu):
     @typing.overload
     def __init__(self, title: str = "", parent=None):
         pass
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/panel.py` & `pyqtribbon-0.7.4/pyqtribbon/panel.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 from __future__ import annotations
 
 import functools
 import re
-from typing import List, Callable, overload, Any, Union, Dict
+from typing import Any, Callable, Dict, List, Union, overload
 
 import numpy as np
-from qtpy import QtWidgets, QtGui, QtCore
+from qtpy import QtCore, QtGui, QtWidgets
 
-from .constants import ColumnWise, RibbonButtonStyle, Large, Medium, Small
+from .constants import ColumnWise, Large, Medium, RibbonButtonStyle, Small
 from .gallery import RibbonGallery
 from .separator import RibbonSeparator
 from .toolbutton import RibbonToolButton
 from .utils import DataFile
 
 
 class RibbonPanelTitle(QtWidgets.QLabel):
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/panel.pyi` & `pyqtribbon-0.7.4/pyqtribbon/panel.pyi`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from __future__ import annotations
 
-from typing import List, Callable, overload, Any, Union, Dict, Iterable
+from typing import Any, Callable, Dict, Iterable, List, Union, overload
 
 import numpy as np
-from qtpy import QtWidgets, QtGui, QtCore
+from qtpy import QtCore, QtGui, QtWidgets
 
-from .constants import ColumnWise, RibbonButtonStyle, Large, Small
+from .constants import ColumnWise, Large, RibbonButtonStyle, Small
 from .gallery import RibbonGallery
 from .separator import RibbonSeparator
 from .toolbutton import RibbonToolButton
 
 class RibbonPanelTitle(QtWidgets.QLabel): ...
 
 class RibbonGridLayoutManager(object):
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/ribbonbar.py` & `pyqtribbon-0.7.4/pyqtribbon/ribbonbar.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,16 +1,21 @@
 import typing
 
-from qtpy import QtWidgets, QtCore, QtGui
+from qtpy import QtCore, QtGui, QtWidgets
 
-from .category import RibbonCategory, RibbonContextCategory, RibbonNormalCategory, RibbonContextCategories
-from .constants import RibbonStyle, RibbonCategoryStyle, contextColors
+from .category import (
+    RibbonCategory,
+    RibbonContextCategories,
+    RibbonContextCategory,
+    RibbonNormalCategory,
+)
+from .constants import RibbonCategoryStyle, RibbonStyle, contextColors
 from .menu import RibbonMenu
 from .tabbar import RibbonTabBar
-from .titlewidget import RibbonTitleWidget, RibbonApplicationButton
+from .titlewidget import RibbonApplicationButton, RibbonTitleWidget
 from .utils import DataFile
 
 
 class RibbonStackedWidget(QtWidgets.QStackedWidget):
     """Stacked widget that is used to display the ribbon."""
 
     def __init__(self, parent=None):
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/screenshotwindow.py` & `pyqtribbon-0.7.4/pyqtribbon/screenshotwindow.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from qtpy import QtWidgets, QtCore
+from qtpy import QtCore, QtWidgets
 
 
 class RibbonScreenShotWindow(QtWidgets.QMainWindow):
     """This class is just for taking a screenshot of the window, the window will be closed 0.1s after it is shown."""
 
     _fileName = "shot.jpg"
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/separator.py` & `pyqtribbon-0.7.4/pyqtribbon/separator.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import typing
 
-from qtpy import QtCore, QtWidgets, QtGui
+from qtpy import QtCore, QtGui, QtWidgets
 
 
 class RibbonSeparator(QtWidgets.QFrame):
     """The RibbonSeparator is a separator that can be used to separate widgets in a ribbon."""
 
     _topMargins: int = 4
     _bottomMargins: int = 4
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/styles/base.qss` & `pyqtribbon-0.7.4/pyqtribbon/styles/base.qss`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/styles/debug.qss` & `pyqtribbon-0.7.4/pyqtribbon/styles/debug.qss`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon/tabbar.py` & `pyqtribbon-0.7.4/pyqtribbon/tabbar.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import typing
 
-from qtpy import QtWidgets, QtGui, QtCore
+from qtpy import QtCore, QtGui, QtWidgets
 
 
 class RibbonTabBar(QtWidgets.QTabBar):
     """The TabBar for the title widget."""
 
     #: context category top margin
     _contextCategoryTopMargin = 0
@@ -16,14 +16,16 @@
 
     def __init__(self, parent=None):
         """Create a new tab bar.
 
         :param parent: The parent widget.
         """
         super().__init__(parent)
+
+        self.currentChanged.connect(self.changeColor)
         self.setDrawBase(False)
 
     def indexOf(self, tabName: str) -> int:
         """Return the index of the tab with the given name.
 
         :param tabName: The name of the tab.
         :return: The index of the tab.
@@ -79,17 +81,17 @@
     def currentTabColor(self) -> QtGui.QColor:
         """Current tab color
 
         :return: Current tab color
         """
         return self._tabColors[self.tabText(self.currentIndex())]
 
-    def paintEvent(self, a0: QtGui.QPaintEvent) -> None:
-        """Paint the tab bar."""
+    def changeColor(self, inx: int) -> None:
+        """Change tab's color."""
+
         if self.count() > 0:
-            currentTabText = self.tabText(self.currentIndex())
+            currentTabText = self.tabText(inx)
             currentTabColor = self._tabColors[currentTabText]
             if currentTabColor is not None:
                 self.setStyleSheet("RibbonTabBar::tab:selected {color: %s;}" % QtGui.QColor(currentTabColor).name())
             else:
                 self.setStyleSheet("RibbonTabBar::tab:selected {color: black;}")
-        super().paintEvent(a0)
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/titlewidget.py` & `pyqtribbon-0.7.4/pyqtribbon/titlewidget.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import typing
 
-from qtpy import QtWidgets, QtCore, QtGui
+from qtpy import QtCore, QtGui, QtWidgets
 
 from .menu import RibbonMenu
 from .tabbar import RibbonTabBar
 from .utils import DataFile
 
 
 class RibbonApplicationButton(QtWidgets.QToolButton):
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/toolbutton.py` & `pyqtribbon-0.7.4/pyqtribbon/toolbutton.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from qtpy import QtWidgets, QtCore
+from qtpy import QtCore, QtWidgets
 
 from .constants import RibbonButtonStyle
 from .menu import RibbonMenu
 
 
 class RibbonToolButton(QtWidgets.QToolButton):
     """Tool button that is showed in the ribbon."""
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon/version.py` & `pyqtribbon-0.7.4/pyqtribbon/version.py`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/pyqtribbon.egg-info/PKG-INFO` & `pyqtribbon-0.7.4/pyqtribbon.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyqtribbon
-Version: 0.7.3
+Version: 0.7.4
 Summary: Ribbon Bar for PyQt or PySide applications
 Author-email: WANG Hailin <hailin.wang@connect.polyu.hk>
 Project-URL: GitHub, https://github.com/haiiliin/pyqtribbon
 Project-URL: Documentation, https://pyqtribbon.haiiliin.com/en/stable/
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `pyqtribbon-0.7.3/pyqtribbon.egg-info/SOURCES.txt` & `pyqtribbon-0.7.4/pyqtribbon.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 .flake8
 .gitignore
+.pre-commit-config.yaml
 .readthedocs.yml
 CHANGE_LOG.md
 LICENSE
 README.md
 main.py
 pyproject.toml
 tox.ini
@@ -11,14 +12,15 @@
 .github/release.yml
 .github/workflows/publish.yml
 .github/workflows/release-drafter.yml
 .github/workflows/tests.yml
 docs/Makefile
 docs/make.bat
 docs/requirements.txt
+docs/source/apidoc.rst
 docs/source/conf.py
 docs/source/getting-started.rst
 docs/source/index.rst
 docs/source/ribbon.rst
 docs/source/user.rst
 docs/source/_examples/build.py
 docs/source/_examples/category.png
```

### Comparing `pyqtribbon-0.7.3/screenshots/main.png` & `pyqtribbon-0.7.4/screenshots/main.png`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/tests/test_categories.py` & `pyqtribbon-0.7.4/tests/test_categories.py`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/tests/test_category.py` & `pyqtribbon-0.7.4/tests/test_category.py`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/tests/test_filemenu.py` & `pyqtribbon-0.7.4/tests/test_filemenu.py`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/tests/test_gallery.py` & `pyqtribbon-0.7.4/tests/test_gallery.py`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/tests/test_main.py` & `pyqtribbon-0.7.4/tests/test_main.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from pytestqt.qtbot import QtBot
-from qtpy import QtWidgets, QtGui, QtCore
+from qtpy import QtCore, QtGui, QtWidgets
 from qtpy.QtGui import QIcon
 
-from pyqtribbon import RibbonBar, Large, Normal
+from pyqtribbon import Large, Normal, RibbonBar
 from pyqtribbon.ribbonbar import RibbonStyle
 
 
 def test_main(qtbot: QtBot):
     window = QtWidgets.QMainWindow()
     window.show()
     qtbot.addWidget(window)
```

### Comparing `pyqtribbon-0.7.3/tests/test_panel.py` & `pyqtribbon-0.7.4/tests/test_panel.py`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/tests/test_titlewidget.py` & `pyqtribbon-0.7.4/tests/test_titlewidget.py`

 * *Files identical despite different names*

### Comparing `pyqtribbon-0.7.3/tests/test_use_dictionary_to_create_widgets.py` & `pyqtribbon-0.7.4/tests/test_use_dictionary_to_create_widgets.py`

 * *Files identical despite different names*

