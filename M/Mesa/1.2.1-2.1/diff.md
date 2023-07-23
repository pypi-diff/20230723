# Comparing `tmp/Mesa-1.2.1.tar.gz` & `tmp/Mesa-2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Mesa-1.2.1.tar", last modified: Sat Mar 18 16:19:21 2023, max compression
+gzip compressed data, was "Mesa-2.1.tar", last modified: Sun Jul 23 12:54:25 2023, max compression
```

## Comparing `Mesa-1.2.1.tar` & `Mesa-2.1.tar`

### file list

```diff
@@ -1,217 +1,218 @@
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.743033 Mesa-1.2.1/
--rw-r--r--   0 jk         (501) staff       (20)    35263 2023-03-18 16:14:31.000000 Mesa-1.2.1/HISTORY.rst
--rw-r--r--   0 jk         (501) staff       (20)      572 2023-03-06 14:25:55.000000 Mesa-1.2.1/LICENSE
--rw-r--r--   0 jk         (501) staff       (20)      441 2023-03-18 16:14:31.000000 Mesa-1.2.1/MANIFEST.in
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.436664 Mesa-1.2.1/Mesa.egg-info/
--rw-r--r--   0 jk         (501) staff       (20)     6671 2023-03-18 16:19:21.000000 Mesa-1.2.1/Mesa.egg-info/PKG-INFO
--rw-r--r--   0 jk         (501) staff       (20)    12229 2023-03-18 16:19:21.000000 Mesa-1.2.1/Mesa.egg-info/SOURCES.txt
--rw-r--r--   0 jk         (501) staff       (20)        1 2023-03-18 16:19:21.000000 Mesa-1.2.1/Mesa.egg-info/dependency_links.txt
--rw-r--r--   0 jk         (501) staff       (20)       39 2023-03-18 16:19:21.000000 Mesa-1.2.1/Mesa.egg-info/entry_points.txt
--rw-r--r--   0 jk         (501) staff       (20)        1 2023-03-10 00:33:58.000000 Mesa-1.2.1/Mesa.egg-info/not-zip-safe
--rw-r--r--   0 jk         (501) staff       (20)      143 2023-03-18 16:19:21.000000 Mesa-1.2.1/Mesa.egg-info/requires.txt
--rw-r--r--   0 jk         (501) staff       (20)       11 2023-03-18 16:19:21.000000 Mesa-1.2.1/Mesa.egg-info/top_level.txt
--rw-r--r--   0 jk         (501) staff       (20)     6671 2023-03-18 16:19:21.742487 Mesa-1.2.1/PKG-INFO
--rw-r--r--   0 jk         (501) staff       (20)     5658 2023-03-06 14:25:55.000000 Mesa-1.2.1/README.rst
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.444542 Mesa-1.2.1/mesa/
--rw-r--r--   0 jk         (501) staff       (20)      664 2023-03-18 16:14:31.000000 Mesa-1.2.1/mesa/__init__.py
--rw-r--r--   0 jk         (501) staff       (20)     1081 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/agent.py
--rw-r--r--   0 jk         (501) staff       (20)    27850 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/batchrunner.py
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.445979 Mesa-1.2.1/mesa/cookiecutter-mesa/
--rw-r--r--   0 jk         (501) staff       (20)      337 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/cookiecutter-mesa/cookiecutter.json
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.449594 Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/
--rw-r--r--   0 jk         (501) staff       (20)       80 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/README.md
--rw-r--r--   0 jk         (501) staff       (20)       74 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/run.py
--rw-r--r--   0 jk         (501) staff       (20)      214 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/setup.py
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.451989 Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/
--rw-r--r--   0 jk         (501) staff       (20)        0 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/__init__.py
--rw-r--r--   0 jk         (501) staff       (20)     1842 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/model.py
--rw-r--r--   0 jk         (501) staff       (20)      823 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/server.py
--rw-r--r--   0 jk         (501) staff       (20)    10665 2023-03-18 16:14:31.000000 Mesa-1.2.1/mesa/datacollection.py
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.454191 Mesa-1.2.1/mesa/flat/
--rw-r--r--   0 jk         (501) staff       (20)      218 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/flat/__init__.py
--rw-r--r--   0 jk         (501) staff       (20)      298 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/flat/visualization.py
--rw-r--r--   0 jk         (501) staff       (20)     1147 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/main.py
--rw-r--r--   0 jk         (501) staff       (20)     2595 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/model.py
--rw-r--r--   0 jk         (501) staff       (20)    39673 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/space.py
--rw-r--r--   0 jk         (501) staff       (20)    10665 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/time.py
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.461796 Mesa-1.2.1/mesa/visualization/
--rw-r--r--   0 jk         (501) staff       (20)    14637 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/ModularVisualization.py
--rw-r--r--   0 jk         (501) staff       (20)     3792 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/TextVisualization.py
--rw-r--r--   0 jk         (501) staff       (20)     8688 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/UserParam.py
--rw-r--r--   0 jk         (501) staff       (20)      268 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/__init__.py
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.467962 Mesa-1.2.1/mesa/visualization/modules/
--rw-r--r--   0 jk         (501) staff       (20)     3698 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/modules/BarChartVisualization.py
--rw-r--r--   0 jk         (501) staff       (20)     4742 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/modules/CanvasGridVisualization.py
--rw-r--r--   0 jk         (501) staff       (20)     3144 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/modules/ChartVisualization.py
--rw-r--r--   0 jk         (501) staff       (20)     3541 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/modules/HexGridVisualization.py
--rw-r--r--   0 jk         (501) staff       (20)      838 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/modules/NetworkVisualization.py
--rw-r--r--   0 jk         (501) staff       (20)     2450 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/modules/PieChartVisualization.py
--rw-r--r--   0 jk         (501) staff       (20)      726 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/modules/__init__.py
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.468838 Mesa-1.2.1/mesa/visualization/templates/
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.469861 Mesa-1.2.1/mesa/visualization/templates/css/
--rw-r--r--   0 jk         (501) staff       (20)      377 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/css/visualization.css
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.419095 Mesa-1.2.1/mesa/visualization/templates/external/
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.418764 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.578079 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/
--rw-r--r--   0 jk         (501) staff       (20)    72279 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.css
--rw-r--r--   0 jk         (501) staff       (20)   201507 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.css.map
--rw-r--r--   0 jk         (501) staff       (20)    52805 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.min.css
--rw-r--r--   0 jk         (501) staff       (20)   122306 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.min.css.map
--rw-r--r--   0 jk         (501) staff       (20)    72353 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.css
--rw-r--r--   0 jk         (501) staff       (20)   201511 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.css.map
--rw-r--r--   0 jk         (501) staff       (20)    52880 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.min.css
--rw-r--r--   0 jk         (501) staff       (20)   122383 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.min.css.map
--rw-r--r--   0 jk         (501) staff       (20)     7578 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.css
--rw-r--r--   0 jk         (501) staff       (20)   109619 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.css.map
--rw-r--r--   0 jk         (501) staff       (20)     6120 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.min.css
--rw-r--r--   0 jk         (501) staff       (20)    39730 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.min.css.map
--rw-r--r--   0 jk         (501) staff       (20)     7555 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.css
--rw-r--r--   0 jk         (501) staff       (20)   109632 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.css.map
--rw-r--r--   0 jk         (501) staff       (20)     6192 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.min.css
--rw-r--r--   0 jk         (501) staff       (20)    47717 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.min.css.map
--rw-r--r--   0 jk         (501) staff       (20)    71560 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.css
--rw-r--r--   0 jk         (501) staff       (20)   192717 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.css.map
--rw-r--r--   0 jk         (501) staff       (20)    53455 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.min.css
--rw-r--r--   0 jk         (501) staff       (20)   111849 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.min.css.map
--rw-r--r--   0 jk         (501) staff       (20)    71427 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.css
--rw-r--r--   0 jk         (501) staff       (20)   192660 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.css.map
--rw-r--r--   0 jk         (501) staff       (20)    53383 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.min.css
--rw-r--r--   0 jk         (501) staff       (20)   111684 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.min.css.map
--rw-r--r--   0 jk         (501) staff       (20)   205484 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.css
--rw-r--r--   0 jk         (501) staff       (20)   538014 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.css.map
--rw-r--r--   0 jk         (501) staff       (20)   163873 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.min.css
--rw-r--r--   0 jk         (501) staff       (20)   451427 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.min.css.map
--rw-r--r--   0 jk         (501) staff       (20)   205151 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.css
--rw-r--r--   0 jk         (501) staff       (20)   537928 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.css.map
--rw-r--r--   0 jk         (501) staff       (20)   163978 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.min.css
--rw-r--r--   0 jk         (501) staff       (20)   663486 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.min.css.map
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.617715 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/
--rw-r--r--   0 jk         (501) staff       (20)   209719 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.js
--rw-r--r--   0 jk         (501) staff       (20)   427637 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.js.map
--rw-r--r--   0 jk         (501) staff       (20)    78129 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.min.js
--rw-r--r--   0 jk         (501) staff       (20)   331017 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.min.js.map
--rw-r--r--   0 jk         (501) staff       (20)   139773 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.js
--rw-r--r--   0 jk         (501) staff       (20)   289576 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.js.map
--rw-r--r--   0 jk         (501) staff       (20)    72614 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.min.js
--rw-r--r--   0 jk         (501) staff       (20)   223558 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.min.js.map
--rw-r--r--   0 jk         (501) staff       (20)   148892 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.js
--rw-r--r--   0 jk         (501) staff       (20)   290776 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.js.map
--rw-r--r--   0 jk         (501) staff       (20)    59219 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.min.js
--rw-r--r--   0 jk         (501) staff       (20)   219918 2023-03-10 00:33:56.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.min.js.map
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.635890 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.639536 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/
--rw-r--r--   0 jk         (501) staff       (20)      451 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/CONTRIBUTING.md
--rw-r--r--   0 jk         (501) staff       (20)      512 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/ISSUE_TEMPLATE.md
--rw-r--r--   0 jk         (501) staff       (20)      747 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/PULL_REQUEST_TEMPLATE.md
--rw-r--r--   0 jk         (501) staff       (20)      127 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.gitignore
--rw-r--r--   0 jk         (501) staff       (20)      103 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.npmignore
--rw-r--r--   0 jk         (501) staff       (20)       19 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.npmrc
--rw-r--r--   0 jk         (501) staff       (20)        7 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.nvmrc
--rw-r--r--   0 jk         (501) staff       (20)      774 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.sass-lint.yml
--rw-r--r--   0 jk         (501) staff       (20)      108 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.travis.yml
--rw-r--r--   0 jk         (501) staff       (20)    22936 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/CHANGELOG.md
--rw-r--r--   0 jk         (501) staff       (20)     8974 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/Gruntfile.js
--rw-r--r--   0 jk         (501) staff       (20)     1207 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/LICENSE.md
--rw-r--r--   0 jk         (501) staff       (20)    15619 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/README.md
--rw-r--r--   0 jk         (501) staff       (20)      527 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/bower.json
--rw-r--r--   0 jk         (501) staff       (20)     1087 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/composer.json
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.420218 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.640636 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/css/
--rw-r--r--   0 jk         (501) staff       (20)      872 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/css/highlightjs-github-theme.css
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.644387 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/
--rw-r--r--   0 jk         (501) staff       (20)    44793 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/highlight.min.js
--rw-r--r--   0 jk         (501) staff       (20)    84280 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/jquery.min.js
--rw-r--r--   0 jk         (501) staff       (20)    51351 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/modernizr.js
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.648913 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/
--rw-r--r--   0 jk         (501) staff       (20)    71582 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/bootstrap-slider.js
--rw-r--r--   0 jk         (501) staff       (20)    38829 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/bootstrap-slider.min.js
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.651013 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/
--rw-r--r--   0 jk         (501) staff       (20)    12347 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/bootstrap-slider.css
--rw-r--r--   0 jk         (501) staff       (20)    11184 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/bootstrap-slider.min.css
--rw-r--r--   0 jk         (501) staff       (20)     3510 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/package.json
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.654038 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/
--rw-r--r--   0 jk         (501) staff       (20)      383 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/build-preview.sh
--rw-r--r--   0 jk         (501) staff       (20)     1320 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/release.sh
--rw-r--r--   0 jk         (501) staff       (20)     1246 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/update-gh-pages.sh
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.422765 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.655605 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/js/
--rw-r--r--   0 jk         (501) staff       (20)    70254 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/js/bootstrap-slider.js
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.660711 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/
--rw-r--r--   0 jk         (501) staff       (20)     1033 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_mixins.scss
--rw-r--r--   0 jk         (501) staff       (20)     6652 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_rules.scss
--rw-r--r--   0 jk         (501) staff       (20)      930 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_variables.scss
--rw-r--r--   0 jk         (501) staff       (20)     1638 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/bootstrap-slider.scss
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.661552 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/
--rw-r--r--   0 jk         (501) staff       (20)     1130 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/phantom_bind_polyfill.js
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.710769 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/
--rw-r--r--   0 jk         (501) staff       (20)     3442 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AccessibilitySpec.js
--rw-r--r--   0 jk         (501) staff       (20)     4389 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AriaValueTextFormatterSpec.js
--rw-r--r--   0 jk         (501) staff       (20)      660 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AutoRegisterDataProvideSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     1949 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ConflictingOptionsSpec.js
--rw-r--r--   0 jk         (501) staff       (20)    13555 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/DestroyMethodTests.js
--rw-r--r--   0 jk         (501) staff       (20)    10331 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/DraggingHandlesSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     6587 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ElementDataAttributesSpec.js
--rw-r--r--   0 jk         (501) staff       (20)    15075 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/EventsSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     1532 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/FocusOptionSpec.js
--rw-r--r--   0 jk         (501) staff       (20)    22847 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/KeyboardSupportSpec.js
--rw-r--r--   0 jk         (501) staff       (20)    20361 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LockToTicksSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     2248 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LogarithmicScaleSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     5513 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LowAndHighTrackSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     2270 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/NamespaceSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     2188 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/OrientationSpec.js
--rw-r--r--   0 jk         (501) staff       (20)    23704 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/PublicMethodsSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     6450 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RangeHighlightsSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     3402 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RefreshMethodSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     2131 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ResizeSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     2519 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RtlOptionsSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     5305 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ScrollableBodySpec.js
--rw-r--r--   0 jk         (501) staff       (20)     3085 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ScrollableContainerSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     1696 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/StepReachMaxValueSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     2712 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickClickingBehaviorSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     7767 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickLabelSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     7107 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickMarksSpec.js
--rw-r--r--   0 jk         (501) staff       (20)    13937 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipMouseOverOptionSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     5640 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipPositionOptionSpec.js
--rw-r--r--   0 jk         (501) staff       (20)     2649 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipSplitOptionSpec.js
--rw-r--r--   0 jk         (501) staff       (20)    18834 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TouchCapableSpec.js
--rw-r--r--   0 jk         (501) staff       (20)      893 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/offMethodSpec.js
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.712572 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/
--rw-r--r--   0 jk         (501) staff       (20)     4245 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/SpecRunner.tpl
--rw-r--r--   0 jk         (501) staff       (20)    44636 2023-03-10 00:33:57.000000 Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/index.tpl
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.720951 Mesa-1.2.1/mesa/visualization/templates/js/
--rw-r--r--   0 jk         (501) staff       (20)     4644 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/BarChartModule.js
--rw-r--r--   0 jk         (501) staff       (20)     1610 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/CanvasHexModule.js
--rw-r--r--   0 jk         (501) staff       (20)     1689 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/CanvasModule.js
--rw-r--r--   0 jk         (501) staff       (20)     2175 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/ChartModule.js
--rw-r--r--   0 jk         (501) staff       (20)    12943 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/GridDraw.js
--rw-r--r--   0 jk         (501) staff       (20)     8609 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/HexDraw.js
--rw-r--r--   0 jk         (501) staff       (20)     5295 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/InteractionHandler.js
--rw-r--r--   0 jk         (501) staff       (20)     3002 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/NetworkModule_d3.js
--rw-r--r--   0 jk         (501) staff       (20)     2826 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/PieChartModule.js
--rw-r--r--   0 jk         (501) staff       (20)      327 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/TextModule.js
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.725590 Mesa-1.2.1/mesa/visualization/templates/js/external/
--rw-r--r--   0 jk         (501) staff       (20)   193884 2023-03-10 00:33:58.000000 Mesa-1.2.1/mesa/visualization/templates/js/external/chart-3.6.1.min.js
--rw-r--r--   0 jk         (501) staff       (20)   277072 2023-03-10 00:33:58.000000 Mesa-1.2.1/mesa/visualization/templates/js/external/d3-7.4.3.min.js
--rw-r--r--   0 jk         (501) staff       (20)    10100 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/js/runcontrol.js
--rw-r--r--   0 jk         (501) staff       (20)     4546 2023-03-06 14:25:55.000000 Mesa-1.2.1/mesa/visualization/templates/modular_template.html
--rw-r--r--   0 jk         (501) staff       (20)     1550 2023-03-18 16:14:31.000000 Mesa-1.2.1/pyproject.toml
--rw-r--r--   0 jk         (501) staff       (20)       38 2023-03-18 16:19:21.743171 Mesa-1.2.1/setup.cfg
--rw-r--r--   0 jk         (501) staff       (20)     4800 2023-03-18 16:14:31.000000 Mesa-1.2.1/setup.py
-drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-03-18 16:19:21.741463 Mesa-1.2.1/tests/
--rw-r--r--   0 jk         (501) staff       (20)        0 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/__init__.py
--rw-r--r--   0 jk         (501) staff       (20)     5052 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_batch_run.py
--rw-r--r--   0 jk         (501) staff       (20)    11434 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_batchrunner.py
--rw-r--r--   0 jk         (501) staff       (20)     9107 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_batchrunnerMP.py
--rw-r--r--   0 jk         (501) staff       (20)     6616 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_datacollector.py
--rw-r--r--   0 jk         (501) staff       (20)     2506 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_examples.py
--rw-r--r--   0 jk         (501) staff       (20)    16738 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_grid.py
--rw-r--r--   0 jk         (501) staff       (20)      724 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_import_namespace.py
--rw-r--r--   0 jk         (501) staff       (20)     2834 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_lifespan.py
--rw-r--r--   0 jk         (501) staff       (20)      984 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_main.py
--rw-r--r--   0 jk         (501) staff       (20)      970 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_model.py
--rw-r--r--   0 jk         (501) staff       (20)      539 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_scaffold.py
--rw-r--r--   0 jk         (501) staff       (20)    15928 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_space.py
--rw-r--r--   0 jk         (501) staff       (20)     8559 2023-03-18 16:14:31.000000 Mesa-1.2.1/tests/test_time.py
--rw-r--r--   0 jk         (501) staff       (20)     1270 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_tornado.py
--rw-r--r--   0 jk         (501) staff       (20)     2564 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_usersettableparam.py
--rw-r--r--   0 jk         (501) staff       (20)     2783 2023-03-06 14:25:55.000000 Mesa-1.2.1/tests/test_visualization.py
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.744420 Mesa-2.1/
+-rw-r--r--   0 jk         (501) staff       (20)    39212 2023-07-23 12:49:52.000000 Mesa-2.1/HISTORY.rst
+-rw-r--r--   0 jk         (501) staff       (20)      572 2023-05-15 02:11:02.000000 Mesa-2.1/LICENSE
+-rw-r--r--   0 jk         (501) staff       (20)      441 2023-04-25 15:49:54.000000 Mesa-2.1/MANIFEST.in
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.319167 Mesa-2.1/Mesa.egg-info/
+-rw-r--r--   0 jk         (501) staff       (20)     6663 2023-07-23 12:54:25.000000 Mesa-2.1/Mesa.egg-info/PKG-INFO
+-rw-r--r--   0 jk         (501) staff       (20)    12238 2023-07-23 12:54:25.000000 Mesa-2.1/Mesa.egg-info/SOURCES.txt
+-rw-r--r--   0 jk         (501) staff       (20)        1 2023-07-23 12:54:25.000000 Mesa-2.1/Mesa.egg-info/dependency_links.txt
+-rw-r--r--   0 jk         (501) staff       (20)       39 2023-07-23 12:54:25.000000 Mesa-2.1/Mesa.egg-info/entry_points.txt
+-rw-r--r--   0 jk         (501) staff       (20)        1 2023-03-10 00:33:58.000000 Mesa-2.1/Mesa.egg-info/not-zip-safe
+-rw-r--r--   0 jk         (501) staff       (20)      199 2023-07-23 12:54:25.000000 Mesa-2.1/Mesa.egg-info/requires.txt
+-rw-r--r--   0 jk         (501) staff       (20)       11 2023-07-23 12:54:25.000000 Mesa-2.1/Mesa.egg-info/top_level.txt
+-rw-r--r--   0 jk         (501) staff       (20)     6663 2023-07-23 12:54:25.743772 Mesa-2.1/PKG-INFO
+-rw-r--r--   0 jk         (501) staff       (20)     5652 2023-04-25 15:49:54.000000 Mesa-2.1/README.rst
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.332900 Mesa-2.1/mesa/
+-rw-r--r--   0 jk         (501) staff       (20)      682 2023-07-23 12:49:52.000000 Mesa-2.1/mesa/__init__.py
+-rw-r--r--   0 jk         (501) staff       (20)     1081 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/agent.py
+-rw-r--r--   0 jk         (501) staff       (20)     6120 2023-07-17 03:55:09.000000 Mesa-2.1/mesa/batchrunner.py
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.335357 Mesa-2.1/mesa/cookiecutter-mesa/
+-rw-r--r--   0 jk         (501) staff       (20)      337 2023-03-06 14:25:55.000000 Mesa-2.1/mesa/cookiecutter-mesa/cookiecutter.json
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.339124 Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/
+-rw-r--r--   0 jk         (501) staff       (20)       80 2023-03-06 14:25:55.000000 Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/README.md
+-rw-r--r--   0 jk         (501) staff       (20)       74 2023-03-06 14:25:55.000000 Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/run.py
+-rw-r--r--   0 jk         (501) staff       (20)      214 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/setup.py
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.342468 Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/
+-rw-r--r--   0 jk         (501) staff       (20)        0 2023-03-06 14:25:55.000000 Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/__init__.py
+-rw-r--r--   0 jk         (501) staff       (20)     1842 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/model.py
+-rw-r--r--   0 jk         (501) staff       (20)      823 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/server.py
+-rw-r--r--   0 jk         (501) staff       (20)    11512 2023-05-28 15:25:59.000000 Mesa-2.1/mesa/datacollection.py
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.344952 Mesa-2.1/mesa/experimental/
+-rw-r--r--   0 jk         (501) staff       (20)       55 2023-07-21 03:13:23.000000 Mesa-2.1/mesa/experimental/__init__.py
+-rw-r--r--   0 jk         (501) staff       (20)     6456 2023-07-21 03:13:23.000000 Mesa-2.1/mesa/experimental/jupyter_viz.py
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.346970 Mesa-2.1/mesa/flat/
+-rw-r--r--   0 jk         (501) staff       (20)      218 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/flat/__init__.py
+-rw-r--r--   0 jk         (501) staff       (20)      298 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/flat/visualization.py
+-rw-r--r--   0 jk         (501) staff       (20)     1468 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/main.py
+-rw-r--r--   0 jk         (501) staff       (20)     2708 2023-05-28 15:25:59.000000 Mesa-2.1/mesa/model.py
+-rw-r--r--   0 jk         (501) staff       (20)    38769 2023-07-17 03:55:09.000000 Mesa-2.1/mesa/space.py
+-rw-r--r--   0 jk         (501) staff       (20)    10415 2023-07-17 03:55:09.000000 Mesa-2.1/mesa/time.py
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.352789 Mesa-2.1/mesa/visualization/
+-rw-r--r--   0 jk         (501) staff       (20)    14730 2023-07-17 03:55:09.000000 Mesa-2.1/mesa/visualization/ModularVisualization.py
+-rw-r--r--   0 jk         (501) staff       (20)     3792 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/TextVisualization.py
+-rw-r--r--   0 jk         (501) staff       (20)     4127 2023-07-17 03:55:09.000000 Mesa-2.1/mesa/visualization/UserParam.py
+-rw-r--r--   0 jk         (501) staff       (20)      268 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/__init__.py
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.364117 Mesa-2.1/mesa/visualization/modules/
+-rw-r--r--   0 jk         (501) staff       (20)     3736 2023-07-17 03:55:09.000000 Mesa-2.1/mesa/visualization/modules/BarChartVisualization.py
+-rw-r--r--   0 jk         (501) staff       (20)     4742 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/modules/CanvasGridVisualization.py
+-rw-r--r--   0 jk         (501) staff       (20)     3144 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/modules/ChartVisualization.py
+-rw-r--r--   0 jk         (501) staff       (20)     3541 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/modules/HexGridVisualization.py
+-rw-r--r--   0 jk         (501) staff       (20)      838 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/modules/NetworkVisualization.py
+-rw-r--r--   0 jk         (501) staff       (20)     2450 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/modules/PieChartVisualization.py
+-rw-r--r--   0 jk         (501) staff       (20)      726 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/modules/__init__.py
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.365283 Mesa-2.1/mesa/visualization/templates/
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.366566 Mesa-2.1/mesa/visualization/templates/css/
+-rw-r--r--   0 jk         (501) staff       (20)      377 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/css/visualization.css
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.286666 Mesa-2.1/mesa/visualization/templates/external/
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.286205 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.466330 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/
+-rw-r--r--   0 jk         (501) staff       (20)    72279 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.css
+-rw-r--r--   0 jk         (501) staff       (20)   201507 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.css.map
+-rw-r--r--   0 jk         (501) staff       (20)    52805 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.min.css
+-rw-r--r--   0 jk         (501) staff       (20)   122306 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.min.css.map
+-rw-r--r--   0 jk         (501) staff       (20)    72353 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.css
+-rw-r--r--   0 jk         (501) staff       (20)   201511 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.css.map
+-rw-r--r--   0 jk         (501) staff       (20)    52880 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.min.css
+-rw-r--r--   0 jk         (501) staff       (20)   122383 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.min.css.map
+-rw-r--r--   0 jk         (501) staff       (20)     7578 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.css
+-rw-r--r--   0 jk         (501) staff       (20)   109619 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.css.map
+-rw-r--r--   0 jk         (501) staff       (20)     6120 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.min.css
+-rw-r--r--   0 jk         (501) staff       (20)    39730 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.min.css.map
+-rw-r--r--   0 jk         (501) staff       (20)     7555 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.css
+-rw-r--r--   0 jk         (501) staff       (20)   109632 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.css.map
+-rw-r--r--   0 jk         (501) staff       (20)     6192 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.min.css
+-rw-r--r--   0 jk         (501) staff       (20)    47717 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.min.css.map
+-rw-r--r--   0 jk         (501) staff       (20)    71560 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.css
+-rw-r--r--   0 jk         (501) staff       (20)   192717 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.css.map
+-rw-r--r--   0 jk         (501) staff       (20)    53455 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.min.css
+-rw-r--r--   0 jk         (501) staff       (20)   111849 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.min.css.map
+-rw-r--r--   0 jk         (501) staff       (20)    71427 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.css
+-rw-r--r--   0 jk         (501) staff       (20)   192660 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.css.map
+-rw-r--r--   0 jk         (501) staff       (20)    53383 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.min.css
+-rw-r--r--   0 jk         (501) staff       (20)   111684 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.min.css.map
+-rw-r--r--   0 jk         (501) staff       (20)   205484 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.css
+-rw-r--r--   0 jk         (501) staff       (20)   538014 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.css.map
+-rw-r--r--   0 jk         (501) staff       (20)   163873 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.min.css
+-rw-r--r--   0 jk         (501) staff       (20)   451427 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.min.css.map
+-rw-r--r--   0 jk         (501) staff       (20)   205151 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.css
+-rw-r--r--   0 jk         (501) staff       (20)   537928 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.css.map
+-rw-r--r--   0 jk         (501) staff       (20)   163978 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.min.css
+-rw-r--r--   0 jk         (501) staff       (20)   663486 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.min.css.map
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.512711 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/
+-rw-r--r--   0 jk         (501) staff       (20)   209719 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.js
+-rw-r--r--   0 jk         (501) staff       (20)   427637 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.js.map
+-rw-r--r--   0 jk         (501) staff       (20)    78129 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.min.js
+-rw-r--r--   0 jk         (501) staff       (20)   331017 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.min.js.map
+-rw-r--r--   0 jk         (501) staff       (20)   139773 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.js
+-rw-r--r--   0 jk         (501) staff       (20)   289576 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.js.map
+-rw-r--r--   0 jk         (501) staff       (20)    72614 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.min.js
+-rw-r--r--   0 jk         (501) staff       (20)   223558 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.min.js.map
+-rw-r--r--   0 jk         (501) staff       (20)   148892 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.js
+-rw-r--r--   0 jk         (501) staff       (20)   290776 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.js.map
+-rw-r--r--   0 jk         (501) staff       (20)    59219 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.min.js
+-rw-r--r--   0 jk         (501) staff       (20)   219918 2023-03-10 00:33:56.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.min.js.map
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.539038 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.544731 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/
+-rw-r--r--   0 jk         (501) staff       (20)      451 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/CONTRIBUTING.md
+-rw-r--r--   0 jk         (501) staff       (20)      512 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/ISSUE_TEMPLATE.md
+-rw-r--r--   0 jk         (501) staff       (20)      747 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/PULL_REQUEST_TEMPLATE.md
+-rw-r--r--   0 jk         (501) staff       (20)      127 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.gitignore
+-rw-r--r--   0 jk         (501) staff       (20)      103 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.npmignore
+-rw-r--r--   0 jk         (501) staff       (20)       19 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.npmrc
+-rw-r--r--   0 jk         (501) staff       (20)        7 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.nvmrc
+-rw-r--r--   0 jk         (501) staff       (20)      774 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.sass-lint.yml
+-rw-r--r--   0 jk         (501) staff       (20)      108 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.travis.yml
+-rw-r--r--   0 jk         (501) staff       (20)    22936 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/CHANGELOG.md
+-rw-r--r--   0 jk         (501) staff       (20)     8974 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/Gruntfile.js
+-rw-r--r--   0 jk         (501) staff       (20)     1207 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/LICENSE.md
+-rw-r--r--   0 jk         (501) staff       (20)    15619 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/README.md
+-rw-r--r--   0 jk         (501) staff       (20)      527 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/bower.json
+-rw-r--r--   0 jk         (501) staff       (20)     1087 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/composer.json
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.294844 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.546102 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/css/
+-rw-r--r--   0 jk         (501) staff       (20)      872 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/css/highlightjs-github-theme.css
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.552271 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/
+-rw-r--r--   0 jk         (501) staff       (20)    44793 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/highlight.min.js
+-rw-r--r--   0 jk         (501) staff       (20)    84280 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/jquery.min.js
+-rw-r--r--   0 jk         (501) staff       (20)    51351 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/modernizr.js
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.563063 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/
+-rw-r--r--   0 jk         (501) staff       (20)    71582 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/bootstrap-slider.js
+-rw-r--r--   0 jk         (501) staff       (20)    38829 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/bootstrap-slider.min.js
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.566892 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/
+-rw-r--r--   0 jk         (501) staff       (20)    12347 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/bootstrap-slider.css
+-rw-r--r--   0 jk         (501) staff       (20)    11184 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/bootstrap-slider.min.css
+-rw-r--r--   0 jk         (501) staff       (20)     3510 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/package.json
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.584389 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/
+-rw-r--r--   0 jk         (501) staff       (20)      383 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/build-preview.sh
+-rw-r--r--   0 jk         (501) staff       (20)     1320 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/release.sh
+-rw-r--r--   0 jk         (501) staff       (20)     1246 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/update-gh-pages.sh
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.297639 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.585952 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/js/
+-rw-r--r--   0 jk         (501) staff       (20)    70254 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/js/bootstrap-slider.js
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.605828 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/
+-rw-r--r--   0 jk         (501) staff       (20)     1033 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_mixins.scss
+-rw-r--r--   0 jk         (501) staff       (20)     6652 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_rules.scss
+-rw-r--r--   0 jk         (501) staff       (20)      930 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_variables.scss
+-rw-r--r--   0 jk         (501) staff       (20)     1638 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/bootstrap-slider.scss
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.611435 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/
+-rw-r--r--   0 jk         (501) staff       (20)     1130 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/phantom_bind_polyfill.js
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.701203 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/
+-rw-r--r--   0 jk         (501) staff       (20)     3442 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AccessibilitySpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     4389 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AriaValueTextFormatterSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)      660 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AutoRegisterDataProvideSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     1949 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ConflictingOptionsSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)    13555 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/DestroyMethodTests.js
+-rw-r--r--   0 jk         (501) staff       (20)    10331 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/DraggingHandlesSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     6587 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ElementDataAttributesSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)    15075 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/EventsSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     1532 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/FocusOptionSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)    22847 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/KeyboardSupportSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)    20361 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LockToTicksSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     2248 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LogarithmicScaleSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     5513 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LowAndHighTrackSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     2270 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/NamespaceSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     2188 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/OrientationSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)    23704 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/PublicMethodsSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     6450 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RangeHighlightsSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     3402 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RefreshMethodSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     2131 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ResizeSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     2519 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RtlOptionsSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     5305 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ScrollableBodySpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     3085 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ScrollableContainerSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     1696 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/StepReachMaxValueSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     2712 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickClickingBehaviorSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     7767 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickLabelSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     7107 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickMarksSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)    13937 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipMouseOverOptionSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     5640 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipPositionOptionSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)     2649 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipSplitOptionSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)    18834 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TouchCapableSpec.js
+-rw-r--r--   0 jk         (501) staff       (20)      893 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/offMethodSpec.js
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.703198 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/
+-rw-r--r--   0 jk         (501) staff       (20)     4245 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/SpecRunner.tpl
+-rw-r--r--   0 jk         (501) staff       (20)    44636 2023-03-10 00:33:57.000000 Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/index.tpl
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.716973 Mesa-2.1/mesa/visualization/templates/js/
+-rw-r--r--   0 jk         (501) staff       (20)     4644 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/js/BarChartModule.js
+-rw-r--r--   0 jk         (501) staff       (20)     1610 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/js/CanvasHexModule.js
+-rw-r--r--   0 jk         (501) staff       (20)     1689 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/js/CanvasModule.js
+-rw-r--r--   0 jk         (501) staff       (20)     2204 2023-05-15 02:11:02.000000 Mesa-2.1/mesa/visualization/templates/js/ChartModule.js
+-rw-r--r--   0 jk         (501) staff       (20)    12943 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/js/GridDraw.js
+-rw-r--r--   0 jk         (501) staff       (20)     8609 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/js/HexDraw.js
+-rw-r--r--   0 jk         (501) staff       (20)     5295 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/js/InteractionHandler.js
+-rw-r--r--   0 jk         (501) staff       (20)     3002 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/js/NetworkModule_d3.js
+-rw-r--r--   0 jk         (501) staff       (20)     2826 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/js/PieChartModule.js
+-rw-r--r--   0 jk         (501) staff       (20)      327 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/js/TextModule.js
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.721713 Mesa-2.1/mesa/visualization/templates/js/external/
+-rw-r--r--   0 jk         (501) staff       (20)   193884 2023-03-10 00:33:58.000000 Mesa-2.1/mesa/visualization/templates/js/external/chart-3.6.1.min.js
+-rw-r--r--   0 jk         (501) staff       (20)   277072 2023-03-10 00:33:58.000000 Mesa-2.1/mesa/visualization/templates/js/external/d3-7.4.3.min.js
+-rw-r--r--   0 jk         (501) staff       (20)    10100 2023-05-15 02:11:02.000000 Mesa-2.1/mesa/visualization/templates/js/runcontrol.js
+-rw-r--r--   0 jk         (501) staff       (20)     4546 2023-04-25 15:49:54.000000 Mesa-2.1/mesa/visualization/templates/modular_template.html
+-rw-r--r--   0 jk         (501) staff       (20)     1895 2023-07-17 03:55:09.000000 Mesa-2.1/pyproject.toml
+-rw-r--r--   0 jk         (501) staff       (20)       38 2023-07-23 12:54:25.744590 Mesa-2.1/setup.cfg
+-rw-r--r--   0 jk         (501) staff       (20)     5264 2023-07-21 03:13:23.000000 Mesa-2.1/setup.py
+drwxr-xr-x   0 jk         (501) staff       (20)        0 2023-07-23 12:54:25.742442 Mesa-2.1/tests/
+-rw-r--r--   0 jk         (501) staff       (20)        0 2023-03-06 14:25:55.000000 Mesa-2.1/tests/__init__.py
+-rw-r--r--   0 jk         (501) staff       (20)     5092 2023-07-17 03:55:09.000000 Mesa-2.1/tests/test_batch_run.py
+-rw-r--r--   0 jk         (501) staff       (20)     8726 2023-05-28 15:25:59.000000 Mesa-2.1/tests/test_datacollector.py
+-rw-r--r--   0 jk         (501) staff       (20)     2506 2023-04-25 15:49:54.000000 Mesa-2.1/tests/test_examples.py
+-rw-r--r--   0 jk         (501) staff       (20)    15776 2023-07-17 03:55:09.000000 Mesa-2.1/tests/test_grid.py
+-rw-r--r--   0 jk         (501) staff       (20)      780 2023-07-17 03:55:09.000000 Mesa-2.1/tests/test_import_namespace.py
+-rw-r--r--   0 jk         (501) staff       (20)     2834 2023-04-25 15:49:54.000000 Mesa-2.1/tests/test_lifespan.py
+-rw-r--r--   0 jk         (501) staff       (20)      984 2023-04-25 15:49:54.000000 Mesa-2.1/tests/test_main.py
+-rw-r--r--   0 jk         (501) staff       (20)      970 2023-04-25 15:49:54.000000 Mesa-2.1/tests/test_model.py
+-rw-r--r--   0 jk         (501) staff       (20)      539 2023-04-25 15:49:54.000000 Mesa-2.1/tests/test_scaffold.py
+-rw-r--r--   0 jk         (501) staff       (20)    15823 2023-07-17 03:55:09.000000 Mesa-2.1/tests/test_space.py
+-rw-r--r--   0 jk         (501) staff       (20)     8717 2023-07-17 03:55:09.000000 Mesa-2.1/tests/test_time.py
+-rw-r--r--   0 jk         (501) staff       (20)     1270 2023-04-25 15:49:54.000000 Mesa-2.1/tests/test_tornado.py
+-rw-r--r--   0 jk         (501) staff       (20)     1780 2023-07-17 03:55:09.000000 Mesa-2.1/tests/test_usersettableparam.py
+-rw-r--r--   0 jk         (501) staff       (20)     3011 2023-07-17 03:55:09.000000 Mesa-2.1/tests/test_visualization.py
```

### Comparing `Mesa-1.2.1/HISTORY.rst` & `Mesa-2.1/HISTORY.rst`

 * *Files 4% similar despite different names*

```diff
@@ -1,21 +1,101 @@
 .. :changelog:
 
 Release History
 ---------------
 
-1.2.1 (2023-03-16)
+2.1.0 (2023-07-22) Youngtown
++++++++++++++++++++++++++++++
+
+This release creates `mesa.experimental` namespace, this solves the issue that PyPI release will not allow git-based install.
+
+**Users should read the Mesa 2.0.0 release note (directly below this), as this contains the details about the breaking
+changes and other major changes that were part of Mesa 2.0 release.**
+
+Changes:
+   * Creates `mesa.experimental` namespace #1736
+   * Fix Ruff lint error #1737
+   * Update permissions for PyPI #1732
+
+2.0.0 (2023-07-15) Wellton
+++++++++++++++++++++++++++
+
+**Special notes**
+
+Mesa 2.0 includes:
+    * **an experimental pure python user interface/ visualization that is also jupyter compatible please see the** `visualization tutorial`_
+    * an improved `datacollector` that allows collection by agent type
+    * several breaking changes that provide significant improvements to Mesa.
+
+.. _visualization tutorial: https://mesa.readthedocs.io/en/latest/tutorials/visualization_tutorial.html
+**Breaking Changes:**
+
+* space: change `coord_iter` to return `(content,(x,y))` instead of `(content, x,y)`; this reduces known errors of scheduler to grid mismatch #1566, #1723
+* space: change NetworkGrid `get_neighbors` to `get_neighborhood`; improves performance #1542
+* space: raise exception when pos is out of bounds in `Grid.get_neighborhood` #1524
+* space: remove deprecations (#1520, #1687, #1688):
+    * `find_empty()`: convert this to `move_to_empty()`
+    * `num_agents`: removed parameter from `move_to_empty()`
+    * `position_agent()`: convert this to `place_agent`
+    * `neighbor_iter()`: convert this to `iter_neighborhood()`
+* batchrunner: remove deprecations #1627
+    * `class BatchRunner` and `class BatchRunnerMP`: convert these to `batch_run()`
+    * Please see this `batch_run() example`_ if you would like to see an an implementation.
+* visualization: easier visualization creation #1693
+    * `UserSettableParameter(['number', 'slider','checkbox', 'choice', 'StaticText'])`: convert to `NumberInput` , `Slider`, `CheckBox`, `Choice`, `StaticText`
+    * Please see this `visualization example`_ if you would like to see an implementation.
+
+.. _batch_run() example: https://github.com/projectmesa/mesa-examples/blob/db2ec0383eb3b1868e91c828101e84cce97bbb63/examples/bank_reserves/batch_run.py#L188-L221
+.. _visualization example: https://github.com/projectmesa/mesa-examples/blob/db2ec0383eb3b1868e91c828101e84cce97bbb63/examples/boltzmann_wealth_model/boltzmann_wealth_model/server.py#L25-L32.)
+
+
+**New Features:**
+
+* datacollector: can now handle data collection by agent type #1419, #1702
+* time: allows for model level `StageActivation` #1709
+* visualization: `ChartModule` can have dynamically named properties #1685
+* visualization: improved stop server to end visualizations #1646
+* *experimental* python front end option: integrated the initial prototype of the pure python front end option #1698, #1726
+
+
+**Improvements**
+
+
+* update HexGrid and create HexSingleGrid and HexMultiGrid #1581
+* correct `get_heading` for toroidal space #1686
+* update slider to start at 1FPS #1674
+* update links to examples repo due to creation of mesa_examples #1636, #1637
+* ** CI Improvements**
+    * update Ruff #1724
+    * remove Pipfile and Pipfile.lock #1692
+    * enable Codespell in Jupyter #1695
+    * improve regex for better build #1669, #1671
+    * exclude notebooks form linter #1670
+    * updated pip for zsh #1644
+    * CLI quality of life improvements #1640
+* **Docs Improvements**
+    * update to PyData theme #1699
+    * remove .rst to create simpler build #1363, #1624
+    * use seaborn in tutorials #1718
+    * fix types and errors in docs #1624, #1705, #1706, #1720
+    * improve tutorials #1636, #1637, #1639, #1641, #1647, #1648, #1650, #1656, #1658, #1659, #1695, #1697,
+    * add nbsphinx to adv_tutorial #1694
+    * replace `const chart` for `var chart` in advanced tutorial #1679
+* update LICENSE to 2023 #1683
+
+1.2.1 (2023-03-18)
 ++++++++++++++++++
 
 This release fixes https://github.com/projectmesa/mesa/issues/1606, where `mesa startproject` doesn't work.
 
 Changes:
-- fix: Include cookiecutter folders in install content #1611
-- Fix Ruff errors and pin Ruff version #1609
-- datacollector: Add warning when returning empty dataframe with no reporters defined #1614
+
+* fix: Include cookiecutter folders in install content #1611
+* Fix Ruff errors and pin Ruff version #1609
+* datacollector: Add warning when returning empty dataframe with no reporters defined #1614
 
 1.2.0 (2023-03-09) Taylor
 ++++++++++++++++++++++++++
 
 **Special notes**
 
 New features:
```

### Comparing `Mesa-1.2.1/LICENSE` & `Mesa-2.1/LICENSE`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-Copyright 2022 Core Mesa Team and contributors
+Copyright 2023 Core Mesa Team and contributors
 
 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at
 
     http://www.apache.org/licenses/LICENSE-2.0
```

### Comparing `Mesa-1.2.1/Mesa.egg-info/PKG-INFO` & `Mesa-2.1/Mesa.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Mesa
-Version: 1.2.1
+Version: 2.1
 Summary: Agent-based modeling (ABM) in Python 3+
 Home-page: https://github.com/projectmesa/mesa
 Author: Project Mesa Team
 Author-email: projectmesa@googlegroups.com
 License: Apache 2.0
 Keywords: agent based modeling model ABM simulation multi-agent
 Classifier: Topic :: Scientific/Engineering
@@ -65,27 +65,27 @@
 Using Mesa
 ------------
 
 Getting started quickly:
 
 .. code-block:: bash
 
-    $ pip install mesa
+    pip install mesa
 
 You can also use `pip` to install the github version:
 
 .. code-block:: bash
 
-    $ pip install -U -e git+https://github.com/projectmesa/mesa@main#egg=mesa
+    pip install -U -e git+https://github.com/projectmesa/mesa@main#egg=mesa
 
 Or any other (development) branch on this repo or your own fork:
 
 .. code-block:: bash
 
-    $ pip install -U -e git+https://github.com/YOUR_FORK/mesa@YOUR_BRANCH#egg=mesa
+    pip install -U -e git+https://github.com/YOUR_FORK/mesa@YOUR_BRANCH#egg=mesa
 
 For resources or help on using Mesa, check out the following:
 
 * `Intro to Mesa Tutorial`_ (An introductory model, the Boltzmann Wealth Model, for beginners or those new to Mesa.)
 * `Complexity Explorer Tutorial`_ (An advanced-beginner model, SugarScape with Traders, with instructional videos)
 * `Mesa Examples`_ (A repository of seminal ABMs using Mesa and examples of employing specific Mesa Features)
 * `Docs`_ (Mesa's documentation, API and useful snippets)
```

### Comparing `Mesa-1.2.1/Mesa.egg-info/SOURCES.txt` & `Mesa-2.1/Mesa.egg-info/SOURCES.txt`

 * *Files 0% similar despite different names*

```diff
@@ -22,14 +22,16 @@
 mesa/cookiecutter-mesa/cookiecutter.json
 mesa/cookiecutter-mesa/{{cookiecutter.snake}}/README.md
 mesa/cookiecutter-mesa/{{cookiecutter.snake}}/run.py
 mesa/cookiecutter-mesa/{{cookiecutter.snake}}/setup.py
 mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/__init__.py
 mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/model.py
 mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/server.py
+mesa/experimental/__init__.py
+mesa/experimental/jupyter_viz.py
 mesa/flat/__init__.py
 mesa/flat/visualization.py
 mesa/visualization/ModularVisualization.py
 mesa/visualization/TextVisualization.py
 mesa/visualization/UserParam.py
 mesa/visualization/__init__.py
 mesa/visualization/modules/BarChartVisualization.py
@@ -162,16 +164,14 @@
 mesa/visualization/templates/js/PieChartModule.js
 mesa/visualization/templates/js/TextModule.js
 mesa/visualization/templates/js/runcontrol.js
 mesa/visualization/templates/js/external/chart-3.6.1.min.js
 mesa/visualization/templates/js/external/d3-7.4.3.min.js
 tests/__init__.py
 tests/test_batch_run.py
-tests/test_batchrunner.py
-tests/test_batchrunnerMP.py
 tests/test_datacollector.py
 tests/test_examples.py
 tests/test_grid.py
 tests/test_import_namespace.py
 tests/test_lifespan.py
 tests/test_main.py
 tests/test_model.py
```

### Comparing `Mesa-1.2.1/PKG-INFO` & `Mesa-2.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Mesa
-Version: 1.2.1
+Version: 2.1
 Summary: Agent-based modeling (ABM) in Python 3+
 Home-page: https://github.com/projectmesa/mesa
 Author: Project Mesa Team
 Author-email: projectmesa@googlegroups.com
 License: Apache 2.0
 Keywords: agent based modeling model ABM simulation multi-agent
 Classifier: Topic :: Scientific/Engineering
@@ -65,27 +65,27 @@
 Using Mesa
 ------------
 
 Getting started quickly:
 
 .. code-block:: bash
 
-    $ pip install mesa
+    pip install mesa
 
 You can also use `pip` to install the github version:
 
 .. code-block:: bash
 
-    $ pip install -U -e git+https://github.com/projectmesa/mesa@main#egg=mesa
+    pip install -U -e git+https://github.com/projectmesa/mesa@main#egg=mesa
 
 Or any other (development) branch on this repo or your own fork:
 
 .. code-block:: bash
 
-    $ pip install -U -e git+https://github.com/YOUR_FORK/mesa@YOUR_BRANCH#egg=mesa
+    pip install -U -e git+https://github.com/YOUR_FORK/mesa@YOUR_BRANCH#egg=mesa
 
 For resources or help on using Mesa, check out the following:
 
 * `Intro to Mesa Tutorial`_ (An introductory model, the Boltzmann Wealth Model, for beginners or those new to Mesa.)
 * `Complexity Explorer Tutorial`_ (An advanced-beginner model, SugarScape with Traders, with instructional videos)
 * `Mesa Examples`_ (A repository of seminal ABMs using Mesa and examples of employing specific Mesa Features)
 * `Docs`_ (Mesa's documentation, API and useful snippets)
```

### Comparing `Mesa-1.2.1/README.rst` & `Mesa-2.1/README.rst`

 * *Files 1% similar despite different names*

```diff
@@ -39,27 +39,27 @@
 Using Mesa
 ------------
 
 Getting started quickly:
 
 .. code-block:: bash
 
-    $ pip install mesa
+    pip install mesa
 
 You can also use `pip` to install the github version:
 
 .. code-block:: bash
 
-    $ pip install -U -e git+https://github.com/projectmesa/mesa@main#egg=mesa
+    pip install -U -e git+https://github.com/projectmesa/mesa@main#egg=mesa
 
 Or any other (development) branch on this repo or your own fork:
 
 .. code-block:: bash
 
-    $ pip install -U -e git+https://github.com/YOUR_FORK/mesa@YOUR_BRANCH#egg=mesa
+    pip install -U -e git+https://github.com/YOUR_FORK/mesa@YOUR_BRANCH#egg=mesa
 
 For resources or help on using Mesa, check out the following:
 
 * `Intro to Mesa Tutorial`_ (An introductory model, the Boltzmann Wealth Model, for beginners or those new to Mesa.)
 * `Complexity Explorer Tutorial`_ (An advanced-beginner model, SugarScape with Traders, with instructional videos)
 * `Mesa Examples`_ (A repository of seminal ABMs using Mesa and examples of employing specific Mesa Features)
 * `Docs`_ (Mesa's documentation, API and useful snippets)
```

### Comparing `Mesa-1.2.1/mesa/__init__.py` & `Mesa-2.1/mesa/__init__.py`

 * *Files 14% similar despite different names*

```diff
@@ -17,14 +17,15 @@
     "Model",
     "Agent",
     "time",
     "space",
     "visualization",
     "DataCollector",
     "batch_run",
+    "experimental",
 ]
 
 __title__ = "mesa"
-__version__ = "1.2.1"
+__version__ = "2.1"
 __license__ = "Apache 2.0"
 _this_year = datetime.datetime.now(tz=datetime.timezone.utc).date().year
 __copyright__ = f"Copyright {_this_year} Project Mesa Team"
```

### Comparing `Mesa-1.2.1/mesa/agent.py` & `Mesa-2.1/mesa/agent.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/model.py` & `Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/model.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/server.py` & `Mesa-2.1/mesa/cookiecutter-mesa/{{cookiecutter.snake}}/{{cookiecutter.snake}}/server.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/datacollection.py` & `Mesa-2.1/mesa/datacollection.py`

 * *Files 18% similar despite different names*

```diff
@@ -32,15 +32,14 @@
 The default DataCollector here makes several assumptions:
     * The model has a schedule object called 'schedule'
     * The schedule has an agent list called agents
     * For collecting agent-level variables, agents must have a unique_id
 """
 import itertools
 import types
-from functools import partial
 from operator import attrgetter
 
 import pandas as pd
 
 
 class DataCollector:
     """Class for collecting data generated by a Mesa model.
@@ -48,15 +47,21 @@
     A DataCollector is instantiated with dictionaries of names of model- and
     agent-level variables to collect, associated with attribute names or
     functions which actually collect them. When the collect(...) method is
     called, it collects these attributes and executes these functions one by
     one and stores the results.
     """
 
-    def __init__(self, model_reporters=None, agent_reporters=None, tables=None):
+    def __init__(
+        self,
+        model_reporters=None,
+        agent_reporters=None,
+        tables=None,
+        exclude_none_values=False,
+    ):
         """Instantiate a DataCollector with lists of model and agent reporters.
         Both model_reporters and agent_reporters accept a dictionary mapping a
         variable name to either an attribute name, or a method.
         For example, if there was only one model-level reporter for number of
         agents, it might look like:
             {"agent_count": lambda m: m.schedule.get_agent_count() }
         If there was only one agent-level reporter (e.g. the agent's energy),
@@ -71,14 +76,16 @@
         like:
             {"Lifespan": ["unique_id", "age"]}
 
         Args:
             model_reporters: Dictionary of reporter names and attributes/funcs
             agent_reporters: Dictionary of reporter names and attributes/funcs.
             tables: Dictionary of table names to lists of column names.
+            exclude_none_values: Boolean of whether to drop records which values
+            are None, in the final result.
 
         Notes:
             If you want to pickle your model you must not use lambda functions.
             If your model includes a large number of agents, you should *only*
             use attribute names for the agent reporter, it will be much faster.
 
             Model reporters can take four types of arguments:
@@ -94,14 +101,15 @@
         """
         self.model_reporters = {}
         self.agent_reporters = {}
 
         self.model_vars = {}
         self._agent_records = {}
         self.tables = {}
+        self.exclude_none_values = exclude_none_values
 
         if model_reporters is not None:
             for name, reporter in model_reporters.items():
                 self._new_model_reporter(name, reporter)
 
         if agent_reporters is not None:
             for name, reporter in agent_reporters.items():
@@ -128,15 +136,18 @@
         Args:
             name: Name of the agent-level variable to collect.
             reporter: Attribute string, or function object that returns the
                       variable when given a model instance.
         """
         if type(reporter) is str:
             attribute_name = reporter
-            reporter = partial(self._getattr, reporter)
+
+            def reporter(agent):
+                return getattr(agent, attribute_name, None)
+
             reporter.attribute_name = attribute_name
         self.agent_reporters[name] = reporter
 
     def _new_table(self, table_name, table_columns):
         """Add a new table that objects can write to.
 
         Args:
@@ -145,15 +156,31 @@
         """
         new_table = {column: [] for column in table_columns}
         self.tables[table_name] = new_table
 
     def _record_agents(self, model):
         """Record agents data in a mapping of functions and agents."""
         rep_funcs = self.agent_reporters.values()
+        if self.exclude_none_values:
+            # Drop records which values are None.
+
+            def get_reports(agent):
+                _prefix = (agent.model.schedule.steps, agent.unique_id)
+                reports = (rep(agent) for rep in rep_funcs)
+                reports_without_none = tuple(r for r in reports if r is not None)
+                if len(reports_without_none) == 0:
+                    return None
+                return _prefix + reports_without_none
+
+            agent_records = (get_reports(agent) for agent in model.schedule.agents)
+            agent_records_without_none = (r for r in agent_records if r is not None)
+            return agent_records_without_none
+
         if all(hasattr(rep, "attribute_name") for rep in rep_funcs):
+            # This branch is for performance optimization purpose.
             prefix = ["model.schedule.steps", "unique_id"]
             attributes = [func.attribute_name for func in rep_funcs]
             get_reports = attrgetter(*prefix + attributes)
         else:
 
             def get_reports(agent):
                 _prefix = (agent.model.schedule.steps, agent.unique_id)
@@ -201,19 +228,14 @@
             if column in row:
                 self.tables[table_name][column].append(row[column])
             elif ignore_missing:
                 self.tables[table_name][column].append(None)
             else:
                 raise Exception("Could not insert row with missing column")
 
-    @staticmethod
-    def _getattr(name, _object):
-        """Turn around arguments of getattr to make it partially callable."""
-        return getattr(_object, name, None)
-
     def get_model_vars_dataframe(self):
         """Create a pandas DataFrame from the model variables.
 
         The DataFrame has one column for each model variable, and the index is
         (implicitly) the model tick.
         """
         # Check if self.model_reporters dictionary is empty, if so raise warning
```

### Comparing `Mesa-1.2.1/mesa/main.py` & `Mesa-2.1/mesa/main.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,48 +1,60 @@
 import os
 import sys
+from pathlib import Path
 from subprocess import call
 
 import click
 
+from mesa import __version__
+
 PROJECT_PATH = click.Path(
     exists=True, file_okay=False, dir_okay=True, resolve_path=True
 )
 COOKIECUTTER_DIR = "mesa/cookiecutter-mesa"
 SCRIPTS_DIR = os.path.dirname(os.path.abspath(__file__))
 COOKIECUTTER_PATH = os.path.join(os.path.dirname(SCRIPTS_DIR), COOKIECUTTER_DIR)
 
+CONTEXT_SETTINGS = {"help_option_names": ["-h", "--help"]}
+
 
-@click.group()
+@click.group(context_settings=CONTEXT_SETTINGS)
 def cli():
     "Manage Mesa projects"
 
 
 @cli.command()
 @click.argument("project", type=PROJECT_PATH, default=".")
 def runserver(project):
     """Run mesa project PROJECT
 
     PROJECT is the path to the directory containing `run.py`, or the current
     directory if not specified.
     """
-    sys.path.insert(0, project)
-    os.chdir(project)
-
-    with open("run.py") as f:
-        code = compile(f.read(), "run.py", "exec")
-        exec(code, {}, {})  # noqa: S102
+    run_path = Path(project) / "run.py"
+    if not run_path.exists():
+        sys.exit(f"ERROR: file {run_path} does not exist")
+    args = [sys.executable, str(run_path)]
+    call(args)
 
 
 @click.command()
 @click.option(
     "--no-input", is_flag=True, help="Do not prompt user for custom mesa model input."
 )
 def startproject(no_input):
+    """Create a new mesa project"""
     args = ["cookiecutter", COOKIECUTTER_PATH]
     if no_input:
         args.append("--no-input")
     call(args)
 
 
+@click.command()
+def version():
+    """Show the version of mesa"""
+    print(f"mesa {__version__}")
+
+
 cli.add_command(runserver)
 cli.add_command(startproject)
+cli.add_command(version)
```

### Comparing `Mesa-1.2.1/mesa/model.py` & `Mesa-2.1/mesa/model.py`

 * *Files 5% similar despite different names*

```diff
@@ -62,24 +62,29 @@
 
         if seed is None:
             seed = self._seed
         self.random.seed(seed)
         self._seed = seed
 
     def initialize_data_collector(
-        self, model_reporters=None, agent_reporters=None, tables=None
+        self,
+        model_reporters=None,
+        agent_reporters=None,
+        tables=None,
+        exclude_none_values=False,
     ) -> None:
         if not hasattr(self, "schedule") or self.schedule is None:
             raise RuntimeError(
                 "You must initialize the scheduler (self.schedule) before initializing the data collector."
             )
         if self.schedule.get_agent_count() == 0:
             raise RuntimeError(
                 "You must add agents to the scheduler before initializing the data collector."
             )
         self.datacollector = DataCollector(
             model_reporters=model_reporters,
             agent_reporters=agent_reporters,
             tables=tables,
+            exclude_none_values=exclude_none_values,
         )
         # Collect data for the first time during initialization.
         self.datacollector.collect(self)
```

### Comparing `Mesa-1.2.1/mesa/space.py` & `Mesa-2.1/mesa/space.py`

 * *Files 2% similar despite different names*

```diff
@@ -115,14 +115,19 @@
         # _empties as set() because in this case it would become impossible to discern
         # if the set hasn't still being built or if it has become empty after creation.
         self._empties_built = False
 
         # Neighborhood Cache
         self._neighborhood_cache: dict[Any, list[Coordinate]] = {}
 
+        # Cutoff used inside self.move_to_empty. The parameters are fitted on Python
+        # 3.11 and it was verified that they are roughly the same for 3.10. Refer to
+        # the code in PR#1565 to check for their stability when a new release gets out.
+        self.cutoff_empties = 7.953 * self.num_cells**0.384
+
     @staticmethod
     def default_val() -> None:
         """Default value for new cell elements."""
         return None
 
     @property
     def empties(self) -> set:
@@ -136,31 +141,24 @@
                 self.is_cell_empty,
                 itertools.product(range(self.width), range(self.height)),
             )
         )
         self._empties_built = True
 
     @overload
-    def __getitem__(self, index: int) -> list[GridContent]:
+    def __getitem__(self, index: int | Sequence[Coordinate]) -> list[GridContent]:
         ...
 
     @overload
     def __getitem__(
         self, index: tuple[int | slice, int | slice]
     ) -> GridContent | list[GridContent]:
         ...
 
-    @overload
-    def __getitem__(self, index: Sequence[Coordinate]) -> list[GridContent]:
-        ...
-
-    def __getitem__(
-        self,
-        index: int | Sequence[Coordinate] | tuple[int | slice, int | slice],
-    ) -> GridContent | list[GridContent]:
+    def __getitem__(self, index):
         """Access contents from the grid."""
 
         if isinstance(index, int):
             # grid[x]
             return self._grid[index]
         elif isinstance(index[0], tuple):
             # grid[(x1, y1), (x2, y2), ...]
@@ -191,34 +189,19 @@
             return [cell for rows in self._grid[x] for cell in rows[y]]
 
     def __iter__(self) -> Iterator[GridContent]:
         """Create an iterator that chains the rows of the grid together
         as if it is one list:"""
         return itertools.chain(*self._grid)
 
-    def coord_iter(self) -> Iterator[tuple[GridContent, int, int]]:
-        """An iterator that returns coordinates as well as cell contents."""
+    def coord_iter(self) -> Iterator[tuple[GridContent, Coordinate]]:
+        """An iterator that returns positions as well as cell contents."""
         for row in range(self.width):
             for col in range(self.height):
-                yield self._grid[row][col], row, col  # agent, x, y
-
-    def neighbor_iter(self, pos: Coordinate, moore: bool = True) -> Iterator[Agent]:
-        """Iterate over position neighbors.
-
-        Args:
-            pos: (x,y) coords tuple for the position to get the neighbors of.
-            moore: Boolean for whether to use Moore neighborhood (including
-                   diagonals) or Von Neumann (only up/down/left/right).
-        """
-
-        warn(
-            "`neighbor_iter` is deprecated in favor of `iter_neighbors` "
-            "and will be removed in the subsequent version."
-        )
-        return self.iter_neighbors(pos, moore)
+                yield self._grid[row][col], (row, col)  # agent, position
 
     def iter_neighborhood(
         self,
         pos: Coordinate,
         moore: bool,
         include_center: bool = False,
         radius: int = 1,
@@ -271,14 +254,17 @@
         """
         cache_key = (pos, moore, include_center, radius)
         neighborhood = self._neighborhood_cache.get(cache_key, None)
 
         if neighborhood is not None:
             return neighborhood
 
+        if self.out_of_bounds(pos):
+            raise Exception("The `pos` tuple passed is out of bounds.")
+
         # We use a list instead of a dict for the neighborhood because it would
         # be easier to port the code to Cython or Numba (for performance
         # purpose), with minimal changes. To better understand how the
         # algorithm was conceived, look at
         # https://github.com/projectmesa/mesa/pull/1476#issuecomment-1306220403
         # and the discussion in that PR in general.
         neighborhood = []
@@ -312,15 +298,15 @@
             for nx in x_range:
                 for ny in y_range:
                     if not moore and abs(nx - x) + abs(ny - y) > radius:
                         continue
 
                     neighborhood.append((nx, ny))
 
-        if not include_center and neighborhood:
+        if not include_center:
             neighborhood.remove(pos)
 
         self._neighborhood_cache[cache_key] = neighborhood
 
         return neighborhood
 
     def iter_neighbors(
@@ -464,68 +450,38 @@
         self.place_agent(agent_b, pos_a)
 
     def is_cell_empty(self, pos: Coordinate) -> bool:
         """Returns a bool of the contents of a cell."""
         x, y = pos
         return self._grid[x][y] == self.default_val()
 
-    def move_to_empty(
-        self, agent: Agent, cutoff: float = 0.998, num_agents: int | None = None
-    ) -> None:
+    def move_to_empty(self, agent: Agent) -> None:
         """Moves agent to a random empty cell, vacating agent's old cell."""
-        if num_agents is not None:
-            warn(
-                (
-                    "`num_agents` is being deprecated since it's no longer used "
-                    "inside `move_to_empty`. It shouldn't be passed as a parameter."
-                ),
-                DeprecationWarning,
-            )
         num_empty_cells = len(self.empties)
         if num_empty_cells == 0:
             raise Exception("ERROR: No empty cells")
 
         # This method is based on Agents.jl's random_empty() implementation. See
         # https://github.com/JuliaDynamics/Agents.jl/pull/541. For the discussion, see
-        # https://github.com/projectmesa/mesa/issues/1052. The default cutoff value
-        # provided is the break-even comparison with the time taken in the else
-        # branching point.
-        if 1 - num_empty_cells / self.num_cells < cutoff:
+        # https://github.com/projectmesa/mesa/issues/1052 and
+        # https://github.com/projectmesa/mesa/pull/1565. The cutoff value provided
+        # is the break-even comparison with the time taken in the else branching point.
+        if num_empty_cells > self.cutoff_empties:
             while True:
                 new_pos = (
                     agent.random.randrange(self.width),
                     agent.random.randrange(self.height),
                 )
                 if self.is_cell_empty(new_pos):
                     break
         else:
             new_pos = agent.random.choice(sorted(self.empties))
         self.remove_agent(agent)
         self.place_agent(agent, new_pos)
 
-    def find_empty(self) -> Coordinate | None:
-        """Pick a random empty cell."""
-        import random
-
-        warn(
-            (
-                "`find_empty` is being phased out since it uses the global "
-                "`random` instead of the model-level random-number generator. "
-                "Consider replacing it with having a model or agent object "
-                "explicitly pick one of the grid's list of empty cells."
-            ),
-            DeprecationWarning,
-        )
-
-        if self.exists_empty_cells():
-            pos = random.choice(sorted(self.empties))
-            return pos
-        else:
-            return None
-
     def exists_empty_cells(self) -> bool:
         """Return True if any cells empty else False."""
         return len(self.empties) > 0
 
 
 class SingleGrid(_Grid):
     """Rectangular grid where each cell contains exactly at most one agent.
@@ -535,50 +491,14 @@
     toroidal, the top and bottom, and left and right, edges wrap to each other.
 
     Properties:
         width, height: The grid's width and height.
         torus: Boolean which determines whether to treat the grid as a torus.
     """
 
-    def position_agent(
-        self, agent: Agent, x: int | str = "random", y: int | str = "random"
-    ) -> None:
-        """Position an agent on the grid.
-        This is used when first placing agents! Setting either x or y to "random"
-        gives the same behavior as 'move_to_empty()' to get a random position.
-        If x or y are positive, they are used.
-        Use 'swap_pos()' to swap agents positions.
-        """
-        warn(
-            (
-                "`position_agent` is being deprecated; use instead "
-                "`place_agent` to place an agent at a specified "
-                "location or `move_to_empty` to place an agent "
-                "at a random empty cell."
-            ),
-            DeprecationWarning,
-        )
-
-        if not (isinstance(x, int) or x == "random"):
-            raise Exception(
-                "x must be an integer or a string 'random'."
-                f" Actual type: {type(x)}. Actual value: {x}."
-            )
-        if not (isinstance(y, int) or y == "random"):
-            raise Exception(
-                "y must be an integer or a string 'random'."
-                f" Actual type: {type(y)}. Actual value: {y}."
-            )
-
-        if x == "random" or y == "random":
-            self.move_to_empty(agent)
-        else:
-            coords = (x, y)
-            self.place_agent(agent, coords)
-
     def place_agent(self, agent: Agent, pos: Coordinate) -> None:
         """Place the agent at the specified location, and set its pos variable."""
         if self.is_cell_empty(pos):
             x, y = pos
             self._grid[x][y] = agent
             if self._empties_built:
                 self._empties.discard(pos)
@@ -649,16 +569,16 @@
         """
         return itertools.chain.from_iterable(
             self._grid[x][y]
             for x, y in itertools.filterfalse(self.is_cell_empty, cell_list)
         )
 
 
-class HexGrid(SingleGrid):
-    """Hexagonal Grid: Extends SingleGrid to handle hexagonal neighbors.
+class _HexGrid:
+    """Hexagonal Grid which handles hexagonal neighbors.
 
     Functions according to odd-q rules.
     See http://www.redblobgames.com/grids/hexagons/#coordinates for more.
 
     Properties:
         width, height: The grid's width and height.
         torus: Boolean which determines whether to treat the grid as a torus.
@@ -758,27 +678,14 @@
             coordinates.discard(pos)
 
         neighborhood = sorted(coordinates)
         self._neighborhood_cache[cache_key] = neighborhood
 
         return neighborhood
 
-    def neighbor_iter(self, pos: Coordinate) -> Iterator[Agent]:
-        """Iterate over position neighbors.
-
-        Args:
-            pos: (x,y) coords tuple for the position to get the neighbors of.
-        """
-
-        warn(
-            "`neighbor_iter` is deprecated in favor of `iter_neighbors` "
-            "and will be removed in the subsequent version."
-        )
-        return self.iter_neighbors(pos)
-
     def iter_neighborhood(
         self, pos: Coordinate, include_center: bool = False, radius: int = 1
     ) -> Iterator[Coordinate]:
         """Return an iterator over cell coordinates that are in the
         neighborhood of a certain point.
 
         Args:
@@ -824,14 +731,64 @@
 
         Returns:
             A list of non-None objects in the given neighborhood
         """
         return list(self.iter_neighbors(pos, include_center, radius))
 
 
+class HexSingleGrid(_HexGrid, SingleGrid):
+    """Hexagonal SingleGrid: a SingleGrid where neighbors are computed
+    according to a hexagonal tiling of the grid.
+
+    Functions according to odd-q rules.
+    See http://www.redblobgames.com/grids/hexagons/#coordinates for more.
+
+    Properties:
+        width, height: The grid's width and height.
+        torus: Boolean which determines whether to treat the grid as a torus.
+    """
+
+
+class HexMultiGrid(_HexGrid, MultiGrid):
+    """Hexagonal MultiGrid: a MultiGrid where neighbors are computed
+    according to a hexagonal tiling of the grid.
+
+    Functions according to odd-q rules.
+    See http://www.redblobgames.com/grids/hexagons/#coordinates for more.
+
+    Properties:
+        width, height: The grid's width and height.
+        torus: Boolean which determines whether to treat the grid as a torus.
+    """
+
+
+class HexGrid(HexSingleGrid):
+    """Hexagonal Grid: a Grid where neighbors are computed
+    according to a hexagonal tiling of the grid.
+
+    Functions according to odd-q rules.
+    See http://www.redblobgames.com/grids/hexagons/#coordinates for more.
+
+    Properties:
+        width, height: The grid's width and height.
+        torus: Boolean which determines whether to treat the grid as a torus.
+    """
+
+    def __init__(self, width: int, height: int, torus: bool) -> None:
+        super().__init__(width, height, torus)
+        warn(
+            (
+                "HexGrid is being deprecated; use instead HexSingleGrid or HexMultiGrid "
+                "depending on your use case."
+            ),
+            DeprecationWarning,
+            stacklevel=2,
+        )
+
+
 class ContinuousSpace:
     """Continuous space where each agent can have an arbitrary position.
 
     Assumes that all agents have a pos property storing their position as
     an (x, y) tuple.
 
     This class uses a numpy array internally to store agents in order to speed
@@ -960,19 +917,29 @@
         result.
 
         Args:
             pos_1, pos_2: Coordinate tuples for both points.
         """
         one = np.array(pos_1)
         two = np.array(pos_2)
-        if self.torus:
-            one = (one - self.center) % self.size
-            two = (two - self.center) % self.size
         heading = two - one
-        if isinstance(pos_1, tuple):
+        if self.torus:
+            inverse_heading = heading - np.sign(heading) * self.size
+
+            def get_min_abs(x, y):
+                return x if abs(x) < abs(y) else y
+
+            # Choose the smaller heading based on their absolute value for
+            # each dimension independently.
+            heading = tuple(
+                get_min_abs(heading[i], inverse_heading[i]) for i in range(2)
+            )
+        if isinstance(pos_1, np.ndarray):
+            heading = np.ndarray(heading)
+        else:
             heading = tuple(heading)
         return heading
 
     def get_distance(self, pos_1: FloatCoordinate, pos_2: FloatCoordinate) -> float:
         """Get the distance between two point, accounting for toroidal space.
 
         Args:
@@ -1035,30 +1002,35 @@
         return []
 
     def place_agent(self, agent: Agent, node_id: int) -> None:
         """Place an agent in a node."""
         self.G.nodes[node_id]["agent"].append(agent)
         agent.pos = node_id
 
-    def get_neighbors(
+    def get_neighborhood(
         self, node_id: int, include_center: bool = False, radius: int = 1
     ) -> list[int]:
         """Get all adjacent nodes within a certain radius"""
         if radius == 1:
-            neighbors = list(self.G.neighbors(node_id))
+            neighborhood = list(self.G.neighbors(node_id))
             if include_center:
-                neighbors.append(node_id)
+                neighborhood.append(node_id)
         else:
             neighbors_with_distance = nx.single_source_shortest_path_length(
                 self.G, node_id, radius
             )
             if not include_center:
                 del neighbors_with_distance[node_id]
-            neighbors = sorted(neighbors_with_distance.keys())
-        return neighbors
+            neighborhood = sorted(neighbors_with_distance.keys())
+        return neighborhood
+
+    def get_neighbors(self, node_id: int, include_center: bool = False) -> list[Agent]:
+        """Get all agents in adjacent nodes."""
+        neighborhood = self.get_neighborhood(node_id, include_center)
+        return self.get_cell_list_contents(neighborhood)
 
     def move_agent(self, agent: Agent, node_id: int) -> None:
         """Move an agent from its current node to a new node."""
         self.remove_agent(agent)
         self.place_agent(agent, node_id)
 
     def remove_agent(self, agent: Agent) -> None:
```

### Comparing `Mesa-1.2.1/mesa/time.py` & `Mesa-2.1/mesa/time.py`

 * *Files 15% similar despite different names*

```diff
@@ -24,15 +24,15 @@
 # Mypy; for the `|` operator purpose
 # Remove this __future__ import once the oldest supported Python is 3.10
 from __future__ import annotations
 
 from collections import defaultdict
 
 # mypy
-from typing import Iterator, Union
+from typing import Union
 
 from mesa.agent import Agent
 from mesa.model import Model
 
 # BaseScheduler has a self.time of int, while
 # StagedActivation has a self.time of float
 TimeT = Union[float, int]
@@ -59,55 +59,59 @@
 
         Args:
             agent: An Agent to be added to the schedule. NOTE: The agent must
             have a step() method.
         """
         if agent.unique_id in self._agents:
             raise Exception(
-                f"Agent with unique id {repr(agent.unique_id)} already added to scheduler"
+                f"Agent with unique id {agent.unique_id!r} already added to scheduler"
             )
 
         self._agents[agent.unique_id] = agent
 
     def remove(self, agent: Agent) -> None:
         """Remove all instances of a given agent from the schedule.
 
         Args:
             agent: An agent object.
         """
         del self._agents[agent.unique_id]
 
     def step(self) -> None:
         """Execute the step of all the agents, one at a time."""
-        for agent in self.agent_buffer(shuffled=False):
-            agent.step()
+        # To be able to remove and/or add agents during stepping
+        # it's necessary for the keys view to be a list.
+        self.do_each("step")
         self.steps += 1
         self.time += 1
 
     def get_agent_count(self) -> int:
         """Returns the current number of agents in the queue."""
         return len(self._agents)
 
     @property
     def agents(self) -> list[Agent]:
         return list(self._agents.values())
 
-    def agent_buffer(self, shuffled: bool = False) -> Iterator[Agent]:
-        """Simple generator that yields the agents while letting the user
-        remove and/or add agents during stepping.
-        """
+    def get_agent_keys(self, shuffle: bool = False) -> list[int]:
         # To be able to remove and/or add agents during stepping
         # it's necessary to cast the keys view to a list.
         agent_keys = list(self._agents.keys())
-        if shuffled:
+        if shuffle:
             self.model.random.shuffle(agent_keys)
+        return agent_keys
 
+    def do_each(self, method, agent_keys=None, shuffle=False):
+        if agent_keys is None:
+            agent_keys = self.get_agent_keys()
+        if shuffle:
+            self.model.random.shuffle(agent_keys)
         for agent_key in agent_keys:
             if agent_key in self._agents:
-                yield self._agents[agent_key]
+                getattr(self._agents[agent_key], method)()
 
 
 class RandomActivation(BaseScheduler):
     """A scheduler which activates each agent once per step, in random order,
     with the order reshuffled every step.
 
     This is equivalent to the NetLogo 'ask agents...' and is generally the
@@ -117,40 +121,34 @@
     """
 
     def step(self) -> None:
         """Executes the step of all agents, one at a time, in
         random order.
 
         """
-        for agent in self.agent_buffer(shuffled=True):
-            agent.step()
+        self.do_each("step", shuffle=True)
         self.steps += 1
         self.time += 1
 
 
 class SimultaneousActivation(BaseScheduler):
     """A scheduler to simulate the simultaneous activation of all the agents.
 
     This scheduler requires that each agent have two methods: step and advance.
     step() activates the agent and stages any necessary changes, but does not
     apply them yet. advance() then applies the changes.
     """
 
     def step(self) -> None:
         """Step all agents, then advance them."""
-        # To be able to remove and/or add agents during stepping
-        # it's necessary to cast the keys view to a list.
-        agent_keys = list(self._agents.keys())
-        for agent_key in agent_keys:
-            self._agents[agent_key].step()
-        # We recompute the keys because some agents might have been removed in
+        self.do_each("step")
+        # do_each recomputes the agent_keys from scratch whenever it is called.
+        # It can handle the case when some agents might have been removed in
         # the previous loop.
-        agent_keys = list(self._agents.keys())
-        for agent_key in agent_keys:
-            self._agents[agent_key].advance()
+        self.do_each("advance")
         self.steps += 1
         self.time += 1
 
 
 class StagedActivation(BaseScheduler):
     """A scheduler which allows agent activation to be divided into several
     stages instead of a single `step` method. All agents execute one stage
@@ -186,27 +184,24 @@
         self.shuffle = shuffle
         self.shuffle_between_stages = shuffle_between_stages
         self.stage_time = 1 / len(self.stage_list)
 
     def step(self) -> None:
         """Executes all the stages for all agents."""
         # To be able to remove and/or add agents during stepping
-        # it's necessary to cast the keys view to a list.
-        agent_keys = list(self._agents.keys())
-        if self.shuffle:
-            self.model.random.shuffle(agent_keys)
+        # it's necessary for the keys view to be a list.
+        agent_keys = self.get_agent_keys(self.shuffle)
         for stage in self.stage_list:
-            for agent_key in agent_keys:
-                if agent_key in self._agents:
-                    getattr(self._agents[agent_key], stage)()  # Run stage
+            if stage.startswith("model."):
+                getattr(self.model, stage[6:])()
+            else:
+                self.do_each(stage, agent_keys=agent_keys)
             # We recompute the keys because some agents might have been removed
             # in the previous loop.
-            agent_keys = list(self._agents.keys())
-            if self.shuffle_between_stages:
-                self.model.random.shuffle(agent_keys)
+            agent_keys = self.get_agent_keys(self.shuffle_between_stages)
             self.time += self.stage_time
 
         self.steps += 1
 
 
 class RandomActivationByType(BaseScheduler):
     """
```

### Comparing `Mesa-1.2.1/mesa/visualization/ModularVisualization.py` & `Mesa-2.1/mesa/visualization/ModularVisualization.py`

 * *Files 2% similar despite different names*

```diff
@@ -94,40 +94,39 @@
     "type": "get_params"
     }
 """
 import asyncio
 import os
 import platform
 import webbrowser
+from typing import ClassVar
 
 import tornado.autoreload
 import tornado.escape
 import tornado.gen
 import tornado.ioloop
 import tornado.web
 import tornado.websocket
 
-from mesa.visualization.UserParam import UserParam, UserSettableParameter
+from mesa.visualization.UserParam import UserParam
 
 # Suppress several pylint warnings for this file.
 # Attributes being defined outside of init is a Tornado feature.
 # pylint: disable=attribute-defined-outside-init
 
 # Change the event loop policy for windows
 if platform.system() == "Windows" and platform.python_version_tuple() >= ("3", "7"):
     asyncio.set_event_loop_policy(asyncio.WindowsSelectorEventLoopPolicy())
 
 D3_JS_FILE = "external/d3-7.4.3.min.js"
 CHART_JS_FILE = "external/chart-3.6.1.min.js"
 
 
 def is_user_param(val):
-    return isinstance(val, UserSettableParameter) or issubclass(
-        val.__class__, UserParam
-    )
+    return issubclass(val.__class__, UserParam)
 
 
 class VisualizationElement:
     """
     Defines an element of the visualization.
 
     Attributes:
@@ -143,18 +142,18 @@
                    directory.
 
     Methods:
         render: Takes a model object, and produces JSON data which can be sent
                 to the client.
     """
 
-    package_includes = []
-    local_includes = []
+    package_includes: ClassVar = []
+    local_includes: ClassVar = []
     js_code = ""
-    render_args = {}
+    render_args: ClassVar = {}
     local_dir = ""
 
     def __init__(self):
         pass
 
     def render(self, model):
         """Build visualization data from a model object.
@@ -169,15 +168,15 @@
 
 
 class TextElement(VisualizationElement):
     """
     Module for drawing live-updating text.
     """
 
-    package_includes = ["TextModule.js"]
+    package_includes: ClassVar = ["TextModule.js"]
     js_code = "elements.push(new TextModule());"
 
 
 # =============================================================================
 # Actual Tornado code starts here:
 
 
@@ -281,15 +280,15 @@
         self.verbose = True
         self.max_steps = 100000
 
         if port is not None:
             self.port = port
         else:
             # Default port to listen on
-            self.port = int(os.getenv("PORT", 8521))
+            self.port = int(os.getenv("PORT", "8521"))
 
         # Handlers and other globals:
         page_handler = (r"/", PageHandler)
         socket_handler = (r"/ws", SocketHandler)
         static_handler = (
             r"/static/(.*)",
             tornado.web.StaticFileHandler,
@@ -400,15 +399,18 @@
             self.port = port
         url = f"http://127.0.0.1:{self.port}"
         print(f"Interface starting at {url}")
         self.listen(self.port)
         if open_browser:
             webbrowser.open(url)
         tornado.autoreload.start()
-        tornado.ioloop.IOLoop.current().start()
+        try:
+            tornado.ioloop.IOLoop.current().start()
+        except KeyboardInterrupt:
+            tornado.ioloop.IOLoop.current().stop()
 
     @staticmethod
     def _is_stylesheet(filename):
         return filename.lower().endswith(".css")
 
     def _auto_convert_fn_to_TextElement(self, x):
         """
```

### Comparing `Mesa-1.2.1/mesa/visualization/TextVisualization.py` & `Mesa-2.1/mesa/visualization/TextVisualization.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/modules/BarChartVisualization.py` & `Mesa-2.1/mesa/visualization/modules/BarChartVisualization.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 """
 Pie Chart Module
 ============
 
 Module for drawing live-updating bar charts using d3.js
 """
 import json
+from typing import ClassVar
 
 from mesa.visualization.ModularVisualization import D3_JS_FILE, VisualizationElement
 
 
 class BarChartModule(VisualizationElement):
     """Each bar chart can either visualize model-level or agent-level fields from a datcollector
         with a bar chart.
@@ -22,15 +23,15 @@
         sorting: Whether to sort ascending, descending, or neither when charting agent fields
         sort_by: The agent field to sort by
         canvas_height, canvas_width: The width and height to draw the chart on the page, in pixels.
                                     Default to 800 x 400
         data_collector_name: Name of the DataCollector object in the model to retrieve data from.
     """
 
-    package_includes = [D3_JS_FILE, "BarChartModule.js"]
+    package_includes: ClassVar = [D3_JS_FILE, "BarChartModule.js"]
 
     def __init__(
         self,
         fields,
         scope="model",
         sorting="none",
         sort_by="none",
```

### Comparing `Mesa-1.2.1/mesa/visualization/modules/CanvasGridVisualization.py` & `Mesa-2.1/mesa/visualization/modules/CanvasGridVisualization.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/modules/ChartVisualization.py` & `Mesa-2.1/mesa/visualization/modules/ChartVisualization.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/modules/HexGridVisualization.py` & `Mesa-2.1/mesa/visualization/modules/HexGridVisualization.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/modules/NetworkVisualization.py` & `Mesa-2.1/mesa/visualization/modules/NetworkVisualization.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/modules/PieChartVisualization.py` & `Mesa-2.1/mesa/visualization/modules/PieChartVisualization.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/modules/__init__.py` & `Mesa-2.1/mesa/visualization/modules/__init__.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.min.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.min.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.min.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.min.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.min.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.min.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.min.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-grid.rtl.min.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.min.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.min.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.min.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.min.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.min.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.min.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.min.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-reboot.rtl.min.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.min.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.min.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.min.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.min.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.min.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.min.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.min.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap-utilities.rtl.min.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.min.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.min.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.min.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.min.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.min.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.min.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.min.css.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/css/bootstrap.rtl.min.css.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.js.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.js.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.min.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.min.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.min.js.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.bundle.min.js.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.js.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.js.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.min.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.min.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.min.js.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.esm.min.js.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.js.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.js.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.min.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.min.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.min.js.map` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-5.1.3-dist/js/bootstrap.min.js.map`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/ISSUE_TEMPLATE.md` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/ISSUE_TEMPLATE.md`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/PULL_REQUEST_TEMPLATE.md` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.github/PULL_REQUEST_TEMPLATE.md`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.sass-lint.yml` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/.sass-lint.yml`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/CHANGELOG.md` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/CHANGELOG.md`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/Gruntfile.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/Gruntfile.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/LICENSE.md` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/LICENSE.md`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/README.md` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/README.md`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/bower.json` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/bower.json`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/composer.json` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/composer.json`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/css/highlightjs-github-theme.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/css/highlightjs-github-theme.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/highlight.min.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/highlight.min.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/jquery.min.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/jquery.min.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/modernizr.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dependencies/js/modernizr.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/bootstrap-slider.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/bootstrap-slider.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/bootstrap-slider.min.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/bootstrap-slider.min.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/bootstrap-slider.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/bootstrap-slider.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/bootstrap-slider.min.css` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/dist/css/bootstrap-slider.min.css`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/package.json` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/package.json`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/release.sh` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/release.sh`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/update-gh-pages.sh` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/scripts/update-gh-pages.sh`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/js/bootstrap-slider.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/js/bootstrap-slider.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_mixins.scss` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_mixins.scss`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_rules.scss` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_rules.scss`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_variables.scss` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/_variables.scss`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/bootstrap-slider.scss` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/src/sass/bootstrap-slider.scss`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/phantom_bind_polyfill.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/phantom_bind_polyfill.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AccessibilitySpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AccessibilitySpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AriaValueTextFormatterSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AriaValueTextFormatterSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AutoRegisterDataProvideSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/AutoRegisterDataProvideSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ConflictingOptionsSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ConflictingOptionsSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/DestroyMethodTests.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/DestroyMethodTests.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/DraggingHandlesSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/DraggingHandlesSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ElementDataAttributesSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ElementDataAttributesSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/EventsSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/EventsSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/FocusOptionSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/FocusOptionSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/KeyboardSupportSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/KeyboardSupportSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LockToTicksSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LockToTicksSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LogarithmicScaleSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LogarithmicScaleSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LowAndHighTrackSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/LowAndHighTrackSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/NamespaceSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/NamespaceSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/OrientationSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/OrientationSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/PublicMethodsSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/PublicMethodsSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RangeHighlightsSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RangeHighlightsSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RefreshMethodSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RefreshMethodSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ResizeSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ResizeSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RtlOptionsSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/RtlOptionsSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ScrollableBodySpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ScrollableBodySpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ScrollableContainerSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/ScrollableContainerSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/StepReachMaxValueSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/StepReachMaxValueSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickClickingBehaviorSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickClickingBehaviorSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickLabelSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickLabelSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickMarksSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TickMarksSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipMouseOverOptionSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipMouseOverOptionSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipPositionOptionSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipPositionOptionSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipSplitOptionSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TooltipSplitOptionSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TouchCapableSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/TouchCapableSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/offMethodSpec.js` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/test/specs/offMethodSpec.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/SpecRunner.tpl` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/SpecRunner.tpl`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/index.tpl` & `Mesa-2.1/mesa/visualization/templates/external/bootstrap-slider-11.0.2/tpl/index.tpl`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/BarChartModule.js` & `Mesa-2.1/mesa/visualization/templates/js/BarChartModule.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/CanvasHexModule.js` & `Mesa-2.1/mesa/visualization/templates/js/CanvasHexModule.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/CanvasModule.js` & `Mesa-2.1/mesa/visualization/templates/js/CanvasModule.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/ChartModule.js` & `Mesa-2.1/mesa/visualization/templates/js/ChartModule.js`

 * *Files 16% similar despite different names*

#### js-beautify {}

```diff
@@ -24,19 +24,20 @@
     };
 
     // Prep the chart properties and series:
     const datasets = [];
     for (const i in series) {
         const s = series[i];
         const new_series = {
-            label: s.Label,
-            borderColor: s.Color,
             backgroundColor: convertColorOpacity(s.Color),
             data: [],
         };
+        for (const property in s) {
+            new_series[property] = s[property];
+        }
         datasets.push(new_series);
     }
 
     const chartData = {
         labels: [],
         datasets: datasets,
     };
```

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/GridDraw.js` & `Mesa-2.1/mesa/visualization/templates/js/GridDraw.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/HexDraw.js` & `Mesa-2.1/mesa/visualization/templates/js/HexDraw.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/InteractionHandler.js` & `Mesa-2.1/mesa/visualization/templates/js/InteractionHandler.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/NetworkModule_d3.js` & `Mesa-2.1/mesa/visualization/templates/js/NetworkModule_d3.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/PieChartModule.js` & `Mesa-2.1/mesa/visualization/templates/js/PieChartModule.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/external/chart-3.6.1.min.js` & `Mesa-2.1/mesa/visualization/templates/js/external/chart-3.6.1.min.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/external/d3-7.4.3.min.js` & `Mesa-2.1/mesa/visualization/templates/js/external/d3-7.4.3.min.js`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/mesa/visualization/templates/js/runcontrol.js` & `Mesa-2.1/mesa/visualization/templates/js/runcontrol.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -100,19 +100,19 @@
 }
 
 /*
  * Set up the the FPS control
  */
 const fpsControl = new Slider("#fps", {
     max: 20,
-    min: 0,
+    min: 1,
     value: controller.fps,
-    ticks: [0, 20],
-    ticks_labels: [0, 20],
-    ticks_position: [0, 100],
+    ticks: [1, 20],
+    ticks_labels: [1, 20],
+    ticks_position: [1, 100],
 });
 fpsControl.on("change", () => controller.updateFPS(fpsControl.getValue()));
 
 /*
  * Button logic for start, stop and reset buttons
  */
 startModelButton.onclick = () => {
```

### Comparing `Mesa-1.2.1/mesa/visualization/templates/modular_template.html` & `Mesa-2.1/mesa/visualization/templates/modular_template.html`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/pyproject.toml` & `Mesa-2.1/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -37,11 +37,15 @@
     "E501",
     "S101", # Use of `assert` detected
     "B017", # `assertRaises(Exception)` should be considered evil TODO
     "PGH004", # Use specific rule codes when using `noqa` TODO
     "B905", # `zip()` without an explicit `strict=` parameter
     "N802", # Function name should be lowercase
     "N999",  # Invalid module name. We should revisit this in the future, TODO
+    "RUF012",  # Mutable class attributes should be annotated with `typing.ClassVar` TODO
+    "S310",  # Audit URL open for permitted schemes. Allowing use of `file:` or custom schemes is often unexpected.
+    "S603",  # `subprocess` call: check for execution of untrusted input
 ]
 extend-exclude = ["docs", "build"]
 # Hardcode to Python 3.8.
+# Reminder to update mesa-examples if the value below is changed.
 target-version = "py38"
```

### Comparing `Mesa-1.2.1/setup.py` & `Mesa-2.1/setup.py`

 * *Files 9% similar despite different names*

```diff
@@ -4,26 +4,47 @@
 import shutil
 import urllib.request
 import zipfile
 from codecs import open
 
 from setuptools import find_packages, setup
 
-requires = ["click", "cookiecutter", "networkx", "numpy", "pandas", "tornado", "tqdm"]
+requires = [
+    "click",
+    "cookiecutter",
+    "networkx",
+    "numpy",
+    "pandas",
+    "solara",
+    "tornado",
+    "tqdm",
+]
 
 extras_require = {
     "dev": [
         "black",
         "ruff==0.0.254",
         "coverage",
         "pytest >= 4.6",
         "pytest-cov",
         "sphinx",
     ],
-    "docs": ["sphinx", "ipython"],
+    # Constrain sphinx version until https://github.com/readthedocs/readthedocs.org/issues/10279
+    # is fixed.
+    # Explicitly install ipykernel for Python 3.8.
+    # See https://stackoverflow.com/questions/28831854/how-do-i-add-python3-kernel-to-jupyter-ipython
+    # Could be removed in the future
+    "docs": [
+        "sphinx<7",
+        "ipython",
+        "nbsphinx",
+        "ipykernel",
+        "pydata_sphinx_theme",
+        "seaborn",
+    ],
 }
 
 version = ""
 with open("mesa/__init__.py") as fd:
     version = re.search(
         r'^__version__\s*=\s*[\'"]([^\'"]*)[\'"]', fd.read(), re.MULTILINE
     ).group(1)
```

### Comparing `Mesa-1.2.1/tests/test_batch_run.py` & `Mesa-2.1/tests/test_batch_run.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,9 +1,10 @@
+import mesa
 from mesa.agent import Agent
-from mesa.batchrunner import _make_model_kwargs, batch_run
+from mesa.batchrunner import _make_model_kwargs
 from mesa.datacollection import DataCollector
 from mesa.model import Model
 from mesa.time import BaseScheduler
 
 
 def test_make_model_kwargs():
     assert _make_model_kwargs({"a": 3, "b": 5}) == [{"a": 3, "b": 5}]
@@ -83,15 +84,15 @@
 
     def step(self):
         self.datacollector.collect(self)
         self.schedule.step()
 
 
 def test_batch_run():
-    result = batch_run(MockModel, {}, number_processes=2)
+    result = mesa.batch_run(MockModel, {}, number_processes=2)
     assert result == [
         {
             "RunId": 0,
             "iteration": 0,
             "Step": 1000,
             "reported_model_param": 42,
             "AgentID": 0,
@@ -116,44 +117,46 @@
             "agent_id": 2,
             "agent_local": 250.0,
         },
     ]
 
 
 def test_batch_run_with_params():
-    batch_run(
+    mesa.batch_run(
         MockModel,
         {
             "variable_model_params": range(5),
             "variable_agent_params": ["H", "E", "L", "L", "O"],
         },
         number_processes=2,
     )
 
 
 def test_batch_run_no_agent_reporters():
-    result = batch_run(MockModel, {"enable_agent_reporters": False}, number_processes=2)
+    result = mesa.batch_run(
+        MockModel, {"enable_agent_reporters": False}, number_processes=2
+    )
     print(result)
     assert result == [
         {
             "RunId": 0,
             "iteration": 0,
             "Step": 1000,
             "enable_agent_reporters": False,
             "reported_model_param": 42,
         }
     ]
 
 
 def test_batch_run_single_core():
-    batch_run(MockModel, {}, number_processes=1, iterations=10)
+    mesa.batch_run(MockModel, {}, number_processes=1, iterations=10)
 
 
 def test_batch_run_unhashable_param():
-    result = batch_run(
+    result = mesa.batch_run(
         MockModel,
         {
             "n_agents": 2,
             "variable_model_params": [{"key": "value"}],
         },
         iterations=2,
     )
```

### Comparing `Mesa-1.2.1/tests/test_datacollector.py` & `Mesa-2.1/tests/test_datacollector.py`

 * *Files 19% similar despite different names*

```diff
@@ -28,38 +28,54 @@
         """
         Write the final value to the appropriate table.
         """
         row = {"agent_id": self.unique_id, "final_value": self.val}
         self.model.datacollector.add_table_row("Final_Values", row)
 
 
+class DifferentMockAgent(MockAgent):
+    # We define a different MockAgent to test for attributes that are present
+    # only in 1 type of agent, but not the other.
+    def __init__(self, unique_id, model, val=0):
+        super().__init__(unique_id, model, val=val)
+        self.val3 = val + 42
+
+
 class MockModel(Model):
     """
     Minimalistic model for testing purposes.
     """
 
     schedule = BaseScheduler(None)
 
-    def __init__(self):
+    def __init__(self, test_exclude_none_values=False):
         self.schedule = BaseScheduler(self)
         self.model_val = 100
 
-        for i in range(10):
-            a = MockAgent(i, self, val=i)
-            self.schedule.add(a)
+        self.n = 10
+        for i in range(self.n):
+            self.schedule.add(MockAgent(i, self, val=i))
+            if test_exclude_none_values:
+                self.schedule.add(DifferentMockAgent(self.n + i, self, val=i))
+        if test_exclude_none_values:
+            # Only DifferentMockAgent has val3.
+            agent_reporters = {"value": lambda a: a.val, "value3": "val3"}
+        else:
+            agent_reporters = {"value": lambda a: a.val, "value2": "val2"}
         self.initialize_data_collector(
             {
                 "total_agents": lambda m: m.schedule.get_agent_count(),
                 "model_value": "model_val",
                 "model_calc": self.schedule.get_agent_count,
                 "model_calc_comp": [self.test_model_calc_comp, [3, 4]],
                 "model_calc_fail": [self.test_model_calc_comp, [12, 0]],
             },
-            {"value": lambda a: a.val, "value2": "val2"},
+            agent_reporters,
             {"Final_Values": ["agent_id", "final_value"]},
+            exclude_none_values=test_exclude_none_values,
         )
 
     def test_model_calc_comp(self, input1, input2):
         if input2 > 0:
             return (self.model_val * input1) / input2
         else:
             assert ValueError
@@ -191,9 +207,48 @@
             self.model.initialize_data_collector()
         self.assertEqual(
             str(cm.exception),
             "You must add agents to the scheduler before initializing the data collector.",
         )
 
 
+class TestDataCollectorExcludeNone(unittest.TestCase):
+    def setUp(self):
+        """
+        Create the model and run it a set number of steps.
+        """
+        self.model = MockModel(test_exclude_none_values=True)
+        for i in range(7):
+            if i == 4:
+                self.model.schedule.remove(self.model.schedule._agents[3])
+            self.model.step()
+
+    def test_agent_records(self):
+        """
+        Test agent-level variable collection.
+        """
+        data_collector = self.model.datacollector
+        agent_table = data_collector.get_agent_vars_dataframe()
+
+        assert len(data_collector._agent_records) == 8
+        for step, records in data_collector._agent_records.items():
+            if step < 5:
+                assert len(records) == 20
+            else:
+                assert len(records) == 19
+
+            for values in records:
+                agent_id = values[1]
+                if agent_id < self.model.n:
+                    assert len(values) == 3
+                else:
+                    # Agents with agent_id >= self.model.n are
+                    # DifferentMockAgent, which additionally contains val3.
+                    assert len(values) == 4
+
+        assert "value" in list(agent_table.columns)
+        assert "value2" not in list(agent_table.columns)
+        assert "value3" in list(agent_table.columns)
+
+
 if __name__ == "__main__":
     unittest.main()
```

### Comparing `Mesa-1.2.1/tests/test_examples.py` & `Mesa-2.1/tests/test_examples.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/tests/test_grid.py` & `Mesa-2.1/tests/test_grid.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 """
 Test the Grid objects.
 """
 import random
 import unittest
 from unittest.mock import Mock, patch
 
-from mesa.space import HexGrid, MultiGrid, SingleGrid
+from mesa.space import HexSingleGrid, MultiGrid, SingleGrid
 
 # Initial agent positions for testing
 #
 # --- visual aid ----
 #   0 0 0
 #   1 1 0
 #   0 1 0
@@ -115,49 +115,44 @@
 
         neighborhood = self.grid.get_neighborhood((1, 4), moore=True)
         assert len(neighborhood) == 8
 
         neighborhood = self.grid.get_neighborhood((0, 0), moore=False)
         assert len(neighborhood) == 2
 
-        neighbors = self.grid.get_neighbors((4, 1), moore=False)
-        assert len(neighbors) == 0
-
-        neighbors = self.grid.get_neighbors((4, 1), moore=True)
-        assert len(neighbors) == 0
+        with self.assertRaises(Exception):
+            neighbors = self.grid.get_neighbors((4, 1), moore=False)
 
         neighbors = self.grid.get_neighbors((1, 1), moore=False, include_center=True)
         assert len(neighbors) == 3
 
         neighbors = self.grid.get_neighbors((1, 3), moore=False, radius=2)
         assert len(neighbors) == 3
 
     def test_coord_iter(self):
         ci = self.grid.coord_iter()
 
         # no agent in first space
         first = next(ci)
         assert first[0] is None
-        assert first[1] == 0
-        assert first[2] == 0
+        assert first[1] == (0, 0)
 
         # first agent in the second space
         second = next(ci)
         assert second[0].unique_id == 1
         assert second[0].pos == (0, 1)
-        assert second[1] == 0
-        assert second[2] == 1
+        assert second[1] == (0, 1)
 
     def test_agent_move(self):
         # get the agent at [0, 1]
         agent = self.agents[0]
         self.grid.move_agent(agent, (1, 0))
         assert agent.pos == (1, 0)
         # move it off the torus and check for the exception
-        if not self.torus:
+        if not self.grid.torus:
             with self.assertRaises(Exception):
                 self.grid.move_agent(agent, [-1, 1])
             with self.assertRaises(Exception):
                 self.grid.move_agent(agent, [1, self.grid.height + 1])
         else:
             self.grid.move_agent(agent, [0, -1])
             assert agent.pos == (0, self.grid.height - 1)
@@ -265,67 +260,48 @@
                 # Create and place the mock agent
                 a = MockAgent(counter, None)
                 self.agents.append(a)
                 self.grid.place_agent(a, (x, y))
         self.num_agents = len(self.agents)
 
     @patch.object(MockAgent, "model", create=True)
-    def test_position_agent(self, mock_model):
-        a = MockAgent(100, None)
-        with self.assertRaises(Exception) as exc_info:
-            self.grid.position_agent(a, (1, 1))
-        expected = (
-            "x must be an integer or a string 'random'."
-            " Actual type: <class 'tuple'>. Actual value: (1, 1)."
-        )
-        assert str(exc_info.exception) == expected
-        with self.assertRaises(Exception) as exc_info:
-            self.grid.position_agent(a, "(1, 1)")
-        expected = (
-            "x must be an integer or a string 'random'."
-            " Actual type: <class 'str'>. Actual value: (1, 1)."
-        )
-        assert str(exc_info.exception) == expected
-        self.grid.position_agent(a, "random")
-
-    @patch.object(MockAgent, "model", create=True)
     def test_enforcement(self, mock_model):
         """
         Test the SingleGrid empty count and enforcement.
         """
 
         assert len(self.grid.empties) == 9
         a = MockAgent(100, None)
         with self.assertRaises(Exception):
             self.grid.place_agent(a, (0, 1))
 
         # Place the agent in an empty cell
         mock_model.schedule.get_agent_count = Mock(side_effect=lambda: len(self.agents))
-        self.grid.position_agent(a)
+        self.grid.move_to_empty(a)
         self.num_agents += 1
         # Test whether after placing, the empty cells are reduced by 1
         assert a.pos not in self.grid.empties
         assert len(self.grid.empties) == 8
         for _i in range(10):
-            self.grid.move_to_empty(a, num_agents=self.num_agents)
+            self.grid.move_to_empty(a)
         assert len(self.grid.empties) == 8
 
         # Place agents until the grid is full
         empty_cells = len(self.grid.empties)
         for i in range(empty_cells):
             a = MockAgent(101 + i, None)
-            self.grid.position_agent(a)
+            self.grid.move_to_empty(a)
             self.num_agents += 1
         assert len(self.grid.empties) == 0
 
         a = MockAgent(110, None)
         with self.assertRaises(Exception):
-            self.grid.position_agent(a)
+            self.grid.move_to_empty(a)
         with self.assertRaises(Exception):
-            self.move_to_empty(self.agents[0], num_agents=self.num_agents)
+            self.move_to_empty(self.agents[0])
 
 
 # Number of agents at each position for testing
 # Initial agent positions for testing
 #
 # --- visual aid ----
 #   0 0 0
@@ -393,26 +369,26 @@
         neighbors = self.grid.get_neighbors((1, 1), moore=False, include_center=True)
         assert len(neighbors) == 7
 
         neighbors = self.grid.get_neighbors((1, 3), moore=False, radius=2)
         assert len(neighbors) == 11
 
 
-class TestHexGrid(unittest.TestCase):
+class TestHexSingleGrid(unittest.TestCase):
     """
     Testing a hexagonal singlegrid.
     """
 
     def setUp(self):
         """
         Create a test non-toroidal grid and populate it with Mock Agents
         """
         width = 3
         height = 5
-        self.grid = HexGrid(width, height, torus=False)
+        self.grid = HexSingleGrid(width, height, torus=False)
         self.agents = []
         counter = 0
         for x in range(width):
             for y in range(height):
                 if TEST_GRID[x][y] == 0:
                     continue
                 counter += 1
@@ -421,15 +397,14 @@
                 self.agents.append(a)
                 self.grid.place_agent(a, (x, y))
 
     def test_neighbors(self):
         """
         Test the hexagonal neighborhood methods on the non-toroid.
         """
-
         neighborhood = self.grid.get_neighborhood((1, 1))
         assert len(neighborhood) == 6
 
         neighborhood = self.grid.get_neighborhood((0, 2))
         assert len(neighborhood) == 4
 
         neighborhood = self.grid.get_neighborhood((1, 0))
@@ -448,28 +423,26 @@
         assert len(neighborhood) == 7
 
         neighborhood = self.grid.get_neighborhood((0, 0), radius=4)
         assert len(neighborhood) == 13
         assert sum(x + y for x, y in neighborhood) == 39
 
 
-class TestHexGridTorus(TestSingleGrid):
+class TestHexSingleGridTorus(TestSingleGrid):
     """
     Testing a hexagonal toroidal singlegrid.
     """
 
-    torus = True
-
     def setUp(self):
         """
         Create a test non-toroidal grid and populate it with Mock Agents
         """
         width = 3
         height = 5
-        self.grid = HexGrid(width, height, torus=True)
+        self.grid = HexSingleGrid(width, height, torus=True)
         self.agents = []
         counter = 0
         for x in range(width):
             for y in range(height):
                 if TEST_GRID[x][y] == 0:
                     continue
                 counter += 1
@@ -478,15 +451,14 @@
                 self.agents.append(a)
                 self.grid.place_agent(a, (x, y))
 
     def test_neighbors(self):
         """
         Test the hexagonal neighborhood methods on the toroid.
         """
-
         neighborhood = self.grid.get_neighborhood((1, 1))
         assert len(neighborhood) == 6
 
         neighborhood = self.grid.get_neighborhood((1, 1), include_center=True)
         assert len(neighborhood) == 7
 
         neighborhood = self.grid.get_neighborhood((0, 0))
@@ -502,16 +474,17 @@
         assert len(neighborhood) == 14
         assert sum(x + y for x, y in neighborhood) == 45
 
 
 class TestIndexing:
     # Create a grid where the content of each coordinate is a tuple of its coordinates
     grid = SingleGrid(3, 5, True)
-    for _, x, y in grid.coord_iter():
-        grid._grid[x][y] = (x, y)
+    for _, pos in grid.coord_iter():
+        x, y = pos
+        grid._grid[x][y] = pos
 
     def test_int(self):
         assert self.grid[0][0] == (0, 0)
 
     def test_tuple(self):
         assert self.grid[1, 1] == (1, 1)
```

### Comparing `Mesa-1.2.1/tests/test_lifespan.py` & `Mesa-2.1/tests/test_lifespan.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/tests/test_main.py` & `Mesa-2.1/tests/test_main.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/tests/test_model.py` & `Mesa-2.1/tests/test_model.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/tests/test_scaffold.py` & `Mesa-2.1/tests/test_scaffold.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/tests/test_space.py` & `Mesa-2.1/tests/test_space.py`

 * *Files 2% similar despite different names*

```diff
@@ -302,19 +302,17 @@
             assert self.space[pos[0]][pos[1]] == a
             self.space.remove_agent(a)
             assert a.pos is None
             assert self.space[pos[0]][pos[1]] is None
 
     def test_empty_cells(self):
         if self.space.exists_empty_cells():
-            pytest.deprecated_call(self.space.find_empty)
             for i, pos in enumerate(list(self.space.empties)):
                 a = MockAgent(-i, pos)
-                self.space.position_agent(a, x=pos[0], y=pos[1])
-        assert self.space.find_empty() is None
+                self.space.place_agent(a, pos)
         with self.assertRaises(Exception):
             self.space.move_to_empty(a)
 
     def move_agent(self):
         agent_number = 0
         initial_pos = TEST_AGENTS_GRID[agent_number]
         final_pos = (7, 7)
@@ -350,18 +348,18 @@
         Ensure that the agents are all placed properly.
         """
         for i, pos in enumerate(TEST_AGENTS_NETWORK_SINGLE):
             a = self.agents[i]
             assert a.pos == pos
 
     def test_get_neighbors(self):
-        assert len(self.space.get_neighbors(0, include_center=True)) == 3
-        assert len(self.space.get_neighbors(0, include_center=False)) == 2
-        assert len(self.space.get_neighbors(2, include_center=True, radius=3)) == 7
-        assert len(self.space.get_neighbors(2, include_center=False, radius=3)) == 6
+        assert len(self.space.get_neighborhood(0, include_center=True)) == 3
+        assert len(self.space.get_neighborhood(0, include_center=False)) == 2
+        assert len(self.space.get_neighborhood(2, include_center=True, radius=3)) == 7
+        assert len(self.space.get_neighborhood(2, include_center=False, radius=3)) == 6
 
     def test_move_agent(self):
         initial_pos = 1
         agent_number = 1
         final_pos = TestSingleNetworkGrid.GRAPH_SIZE - 1
 
         _agent = self.agents[agent_number]
@@ -422,19 +420,19 @@
         """
         for i, pos in enumerate(TEST_AGENTS_NETWORK_MULTIPLE):
             a = self.agents[i]
             assert a.pos == pos
 
     def test_get_neighbors(self):
         assert (
-            len(self.space.get_neighbors(0, include_center=True))
+            len(self.space.get_neighborhood(0, include_center=True))
             == TestMultipleNetworkGrid.GRAPH_SIZE
         )
         assert (
-            len(self.space.get_neighbors(0, include_center=False))
+            len(self.space.get_neighborhood(0, include_center=False))
             == TestMultipleNetworkGrid.GRAPH_SIZE - 1
         )
 
     def test_move_agent(self):
         initial_pos = 1
         agent_number = 1
         final_pos = 0
```

### Comparing `Mesa-1.2.1/tests/test_time.py` & `Mesa-2.1/tests/test_time.py`

 * *Files 7% similar despite different names*

```diff
@@ -71,15 +71,15 @@
                               The default scheduler is a BaseScheduler.
         """
         self.log = []
         self.enable_kill_other_agent = enable_kill_other_agent
 
         # Make scheduler
         if activation == STAGED:
-            model_stages = ["stage_one", "stage_two"]
+            model_stages = ["stage_one", "model.model_stage", "stage_two"]
             self.schedule = StagedActivation(self, model_stages, shuffle=shuffle)
         elif activation == RANDOM:
             self.schedule = RandomActivation(self)
         elif activation == SIMULTANEOUS:
             self.schedule = SimultaneousActivation(self)
         elif activation == RANDOM_BY_TYPE:
             self.schedule = RandomActivationByType(self)
@@ -90,41 +90,45 @@
         for name in ["A", "B"]:
             agent = MockAgent(name, self)
             self.schedule.add(agent)
 
     def step(self):
         self.schedule.step()
 
+    def model_stage(self):
+        self.log.append("model_stage")
+
 
 class TestStagedActivation(TestCase):
     """
     Test the staged activation.
     """
 
-    expected_output = ["A_1", "B_1", "A_2", "B_2"]
+    expected_output = ["A_1", "B_1", "model_stage", "A_2", "B_2"]
 
     def test_no_shuffle(self):
         """
         Testing the staged activation without shuffling.
         """
         model = MockModel(shuffle=False)
         model.step()
         model.step()
-        assert all(i == j for i, j in zip(model.log[:4], model.log[4:]))
+        assert all(i == j for i, j in zip(model.log[:5], model.log[5:]))
 
     def test_shuffle(self):
         """
         Test the staged activation with shuffling
         """
         model = MockModel(shuffle=True)
         model.step()
         for output in self.expected_output[:2]:
             assert output in model.log[:2]
-        for output in self.expected_output[2:]:
-            assert output in model.log[2:]
+        for output in self.expected_output[3:]:
+            assert output in model.log[3:]
+        assert self.expected_output[2] == model.log[2]
 
     def test_shuffle_shuffles_agents(self):
         model = MockModel(shuffle=True)
         model.random = mock.Mock()
         assert model.random.shuffle.call_count == 0
         model.step()
         assert model.random.shuffle.call_count == 1
@@ -142,15 +146,15 @@
     def test_intrastep_remove(self):
         """
         Test the staged activation can remove an agent in a
         step of another agent so that the one removed doesn't step.
         """
         model = MockModel(shuffle=True, enable_kill_other_agent=True)
         model.step()
-        assert len(model.log) == 2
+        assert len(model.log) == 3
 
     def test_add_existing_agent(self):
         model = MockModel()
         agent = model.schedule.agents[0]
         with self.assertRaises(Exception):
             model.schedule.add(agent)
```

### Comparing `Mesa-1.2.1/tests/test_tornado.py` & `Mesa-2.1/tests/test_tornado.py`

 * *Files identical despite different names*

### Comparing `Mesa-1.2.1/tests/test_usersettableparam.py` & `Mesa-2.1/tests/test_usersettableparam.py`

 * *Files 18% similar despite different names*

```diff
@@ -2,67 +2,56 @@
 
 from mesa.visualization.UserParam import (
     Checkbox,
     Choice,
     NumberInput,
     Slider,
     StaticText,
-    UserSettableParameter,
 )
 
 
 class TestOption(TestCase):
     def setUp(self):
-        self.number_option = UserSettableParameter("number", value=123)
-        self.number_option_standalone = NumberInput("number", value=123)
-        self.checkbox_option = UserSettableParameter("checkbox", value=True)
-        self.checkbox_option_standalone = Checkbox(value=True)
-        self.choice_option = UserSettableParameter(
-            "choice",
+        self.number_option = NumberInput("number", value=123)
+        self.checkbox_option = Checkbox(value=True)
+        self.choice_option = Choice(
             value="I am your default choice",
             choices=["I am your default choice", "I am your other choice"],
         )
-        self.choice_option_standalone = Choice(
-            value="I am your default choice",
-            choices=["I am your default choice", "I am your other choice"],
-        )
-        self.slider_option = UserSettableParameter(
-            "slider", value=123, min_value=100, max_value=200
-        )
-        self.slider_option_standalone = Slider(value=123, min_value=100, max_value=200)
+        self.slider_option = Slider(value=123, min_value=100, max_value=200)
         self.static_text_option = StaticText("Hurr, Durr Im'a Sheep")
 
     def test_number(self):
-        for option in [self.number_option, self.number_option_standalone]:
-            assert option.value == 123
-            option.value = 321
-            assert option.value == 321
+        option = self.number_option
+        assert option.value == 123
+        option.value = 321
+        assert option.value == 321
 
     def test_checkbox(self):
-        for option in [self.checkbox_option, self.checkbox_option_standalone]:
-            assert option.value
-            option.value = False
-            assert not option.value
+        option = self.checkbox_option
+        assert option.value
+        option.value = False
+        assert not option.value
 
     def test_choice(self):
-        for option in [self.choice_option, self.choice_option_standalone]:
-            assert option.value == "I am your default choice"
-            option.value = "I am your other choice"
-            assert option.value == "I am your other choice"
-            option.value = "I am not an available choice"
-            assert option.value == "I am your default choice"
+        option = self.choice_option
+        assert option.value == "I am your default choice"
+        option.value = "I am your other choice"
+        assert option.value == "I am your other choice"
+        option.value = "I am not an available choice"
+        assert option.value == "I am your default choice"
 
     def test_slider(self):
-        for option in [self.slider_option, self.slider_option_standalone]:
-            assert option.value == 123
-            option.value = 150
-            assert option.value == 150
-            option.value = 0
-            assert option.value == 100
-            option.value = 300
-            assert option.value == 200
-            assert option.json["value"] == 200
+        option = self.slider_option
+        assert option.value == 123
+        option.value = 150
+        assert option.value == 150
+        option.value = 0
+        assert option.value == 100
+        option.value = 300
+        assert option.value == 200
+        assert option.json["value"] == 200
         with self.assertRaises(ValueError):
             Slider()
 
     def test_static_text(self):
         assert self.static_text_option.value == "Hurr, Durr Im'a Sheep"
```

### Comparing `Mesa-1.2.1/tests/test_visualization.py` & `Mesa-2.1/tests/test_visualization.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,31 +1,51 @@
 from collections import defaultdict
 from unittest import TestCase
 
+import mesa
 from mesa.model import Model
 from mesa.space import MultiGrid
 from mesa.time import SimultaneousActivation
 from mesa.visualization.ModularVisualization import ModularServer
 from mesa.visualization.modules import CanvasGrid, TextElement
-from mesa.visualization.UserParam import UserSettableParameter
-from tests.test_batchrunner import MockAgent
+from mesa.visualization.UserParam import (
+    NumberInput,
+    Slider,
+)
+
+
+class MockAgent(mesa.Agent):
+    """
+    Minimalistic agent implementation for testing purposes
+    """
+
+    def __init__(self, unique_id, model, val):
+        super().__init__(unique_id, model)
+        self.unique_id = unique_id
+        self.val = val
+        self.local = 0
+
+    def step(self):
+        self.val += 1
+        self.local += 0.25
 
 
 class MockModel(Model):
     """Test model for testing"""
 
     def __init__(self, width, height, key1=103, key2=104):
         self.width = width
         self.height = height
         self.key1 = (key1,)
         self.key2 = key2
         self.schedule = SimultaneousActivation(self)
         self.grid = MultiGrid(width, height, torus=True)
 
-        for _c, x, y in self.grid.coord_iter():
+        for _c, pos in self.grid.coord_iter():
+            x, y = pos
             a = MockAgent(x + y * 100, self, x * y * 3)
             self.grid.place_agent(a, (x, y))
             self.schedule.add(a)
 
     def step(self):
         self.schedule.step()
 
@@ -45,16 +65,16 @@
             "Color": "black",
         }
 
     def setUp(self):
         self.user_params = {
             "width": 1,
             "height": 1,
-            "key1": UserSettableParameter("number", "Test Parameter", 101),
-            "key2": UserSettableParameter("slider", "Test Parameter", 200, 0, 300, 10),
+            "key1": NumberInput("Test Parameter", 101),
+            "key2": Slider("Test Parameter", 200, 0, 300, 10),
         }
 
         self.viz_elements = [
             CanvasGrid(self.portrayal, 10, 10, 20, 20),
             TextElement(),
             # ChartModule([{"Label": "Wolves", "Color": "#AA0000"},  # Todo - test chart module
             #              {"Label": "Sheep", "Color": "#666666"}])
@@ -75,12 +95,10 @@
     def test_text_render_model_state(self):
         state = self.server.render_model()
         assert state[1] == "<b>VisualizationElement goes here</b>."
 
     def test_user_params(self):
         print(self.server.user_params)
         assert self.server.user_params == {
-            "key1": UserSettableParameter("number", "Test Parameter", 101).json,
-            "key2": UserSettableParameter(
-                "slider", "Test Parameter", 200, 0, 300, 10
-            ).json,
+            "key1": NumberInput("Test Parameter", 101).json,
+            "key2": Slider("Test Parameter", 200, 0, 300, 10).json,
         }
```

