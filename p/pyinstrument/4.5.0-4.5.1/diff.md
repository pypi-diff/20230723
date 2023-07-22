# Comparing `tmp/pyinstrument-4.5.0.tar.gz` & `tmp/pyinstrument-4.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyinstrument-4.5.0.tar", last modified: Mon Jun  5 21:26:52 2023, max compression
+gzip compressed data, was "pyinstrument-4.5.1.tar", last modified: Sat Jul 22 22:23:17 2023, max compression
```

## Comparing `pyinstrument-4.5.0.tar` & `pyinstrument-4.5.1.tar`

### file list

```diff
@@ -1,103 +1,103 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.333772 pyinstrument-4.5.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1505 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    23583 2023-06-05 21:26:52.333772 pyinstrument-4.5.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    18894 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.325772 pyinstrument-4.5.0/bin/
--rwxr-xr-x   0 runner    (1001) docker     (123)     1541 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/bin/build_js_bundle.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     4285 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/bin/bump_version.py
--rwxr-xr-x   0 runner    (1001) docker     (123)       66 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/bin/serve_docs
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.325772 pyinstrument-4.5.0/html_renderer/
--rw-r--r--   0 runner    (1001) docker     (123)      696 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/index.html
--rw-r--r--   0 runner    (1001) docker     (123)   102671 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/package-lock.json
--rw-r--r--   0 runner    (1001) docker     (123)      577 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/package.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.325772 pyinstrument-4.5.0/html_renderer/public/
--rw-r--r--   0 runner    (1001) docker     (123)    39037 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/public/sample.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.325772 pyinstrument-4.5.0/html_renderer/src/
--rw-r--r--   0 runner    (1001) docker     (123)     1664 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/App.svelte
--rw-r--r--   0 runner    (1001) docker     (123)      235 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/app.css
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.325772 pyinstrument-4.5.0/html_renderer/src/assets/
--rw-r--r--   0 runner    (1001) docker     (123)     1483 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/assets/favicon.png
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.325772 pyinstrument-4.5.0/html_renderer/src/lib/
--rw-r--r--   0 runner    (1001) docker     (123)     6030 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/lib/Frame.svelte
--rw-r--r--   0 runner    (1001) docker     (123)     2045 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/lib/Header.svelte
--rw-r--r--   0 runner    (1001) docker     (123)      219 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/lib/appState.ts
--rw-r--r--   0 runner    (1001) docker     (123)      467 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/lib/dataTypes.ts
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.329772 pyinstrument-4.5.0/html_renderer/src/lib/model/
--rw-r--r--   0 runner    (1001) docker     (123)     1647 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/lib/model/Frame.ts
--rw-r--r--   0 runner    (1001) docker     (123)      996 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/lib/model/Group.ts
--rw-r--r--   0 runner    (1001) docker     (123)      584 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/lib/model/Session.ts
--rw-r--r--   0 runner    (1001) docker     (123)      335 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/main.ts
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/src/vite-env.d.ts
--rw-r--r--   0 runner    (1001) docker     (123)      207 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/svelte.config.js
--rw-r--r--   0 runner    (1001) docker     (123)      658 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/tsconfig.json
--rw-r--r--   0 runner    (1001) docker     (123)      142 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/tsconfig.node.json
--rw-r--r--   0 runner    (1001) docker     (123)      463 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/html_renderer/vite.config.ts
--rw-r--r--   0 runner    (1001) docker     (123)      151 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/noxfile.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.329772 pyinstrument-4.5.0/pyinstrument/
--rw-r--r--   0 runner    (1001) docker     (123)      564 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17945 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11961 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/frame.py
--rw-r--r--   0 runner    (1001) docker     (123)     1038 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/frame_info.py
--rw-r--r--   0 runner    (1001) docker     (123)     3903 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/frame_ops.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.329772 pyinstrument-4.5.0/pyinstrument/low_level/
--rw-r--r--   0 runner    (1001) docker     (123)    22285 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/low_level/stat_profile.c
--rw-r--r--   0 runner    (1001) docker     (123)      369 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/low_level/stat_profile.pyi
--rw-r--r--   0 runner    (1001) docker     (123)     3476 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/low_level/stat_profile_python.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.329772 pyinstrument-4.5.0/pyinstrument/magic/
--rw-r--r--   0 runner    (1001) docker     (123)       37 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/magic/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3096 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/magic/_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     5637 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/magic/magic.py
--rw-r--r--   0 runner    (1001) docker     (123)     3600 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/middleware.py
--rw-r--r--   0 runner    (1001) docker     (123)     9219 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/processors.py
--rw-r--r--   0 runner    (1001) docker     (123)    11123 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/profiler.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.329772 pyinstrument-4.5.0/pyinstrument/renderers/
--rw-r--r--   0 runner    (1001) docker     (123)      426 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3597 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     8373 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/console.py
--rw-r--r--   0 runner    (1001) docker     (123)     3231 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/html.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.329772 pyinstrument-4.5.0/pyinstrument/renderers/html_resources/
--rw-r--r--   0 runner    (1001) docker     (123)     2856 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/html_resources/app.css
--rw-r--r--   0 runner    (1001) docker     (123)    18767 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/html_resources/app.js
--rw-r--r--   0 runner    (1001) docker     (123)     3287 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/jsonrenderer.py
--rw-r--r--   0 runner    (1001) docker     (123)     3320 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/pstatsrenderer.py
--rw-r--r--   0 runner    (1001) docker     (123)      277 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/session.py
--rw-r--r--   0 runner    (1001) docker     (123)     8648 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/renderers/speedscope.py
--rw-r--r--   0 runner    (1001) docker     (123)     4935 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/session.py
--rw-r--r--   0 runner    (1001) docker     (123)     7272 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/stack_sampler.py
--rw-r--r--   0 runner    (1001) docker     (123)      539 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/typing.py
--rw-r--r--   0 runner    (1001) docker     (123)     2158 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.329772 pyinstrument-4.5.0/pyinstrument/vendor/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/vendor/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    25076 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/vendor/appdirs.py
--rw-r--r--   0 runner    (1001) docker     (123)    16323 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/vendor/decorator.py
--rw-r--r--   0 runner    (1001) docker     (123)     3202 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyinstrument/vendor/keypath.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.333772 pyinstrument-4.5.0/pyinstrument.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2358 2023-06-05 21:26:52.000000 pyinstrument-4.5.0/pyinstrument.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)      209 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      475 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/requirements-dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)       95 2023-06-05 21:26:52.333772 pyinstrument-4.5.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1530 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.333772 pyinstrument-4.5.0/test/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1437 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)     2303 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/fake_time_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:52.333772 pyinstrument-4.5.0/test/low_level/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/low_level/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1708 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/low_level/test_context.py
--rw-r--r--   0 runner    (1001) docker     (123)      616 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/low_level/test_custom_timer.py
--rw-r--r--   0 runner    (1001) docker     (123)     2052 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/low_level/test_frame_info.py
--rw-r--r--   0 runner    (1001) docker     (123)     1101 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/low_level/test_setstatprofile.py
--rw-r--r--   0 runner    (1001) docker     (123)     1226 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/low_level/test_threaded.py
--rw-r--r--   0 runner    (1001) docker     (123)      478 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/low_level/util.py
--rw-r--r--   0 runner    (1001) docker     (123)     7593 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_cmdline.py
--rw-r--r--   0 runner    (1001) docker     (123)     2567 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_cmdline_main.py
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_ipython_magic.py
--rw-r--r--   0 runner    (1001) docker     (123)     1318 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_overflow.py
--rw-r--r--   0 runner    (1001) docker     (123)    12960 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_processors.py
--rw-r--r--   0 runner    (1001) docker     (123)    10411 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_profiler.py
--rw-r--r--   0 runner    (1001) docker     (123)     6542 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_profiler_async.py
--rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_pstats_renderer.py
--rw-r--r--   0 runner    (1001) docker     (123)     3136 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_stack_sampler.py
--rw-r--r--   0 runner    (1001) docker     (123)     1102 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/test_threading.py
--rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-06-05 21:26:47.000000 pyinstrument-4.5.0/test/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.552302 pyinstrument-4.5.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1505 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    23925 2023-07-22 22:23:17.552302 pyinstrument-4.5.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    19172 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.544301 pyinstrument-4.5.1/bin/
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1541 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/bin/build_js_bundle.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4285 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/bin/bump_version.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)       66 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/bin/serve_docs
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.544301 pyinstrument-4.5.1/html_renderer/
+-rw-r--r--   0 runner    (1001) docker     (123)      696 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)   102671 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/package-lock.json
+-rw-r--r--   0 runner    (1001) docker     (123)      577 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/package.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.544301 pyinstrument-4.5.1/html_renderer/public/
+-rw-r--r--   0 runner    (1001) docker     (123)    39037 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/public/sample.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.544301 pyinstrument-4.5.1/html_renderer/src/
+-rw-r--r--   0 runner    (1001) docker     (123)     1664 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/App.svelte
+-rw-r--r--   0 runner    (1001) docker     (123)      235 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/app.css
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.544301 pyinstrument-4.5.1/html_renderer/src/assets/
+-rw-r--r--   0 runner    (1001) docker     (123)     1483 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/assets/favicon.png
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.544301 pyinstrument-4.5.1/html_renderer/src/lib/
+-rw-r--r--   0 runner    (1001) docker     (123)     6030 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/lib/Frame.svelte
+-rw-r--r--   0 runner    (1001) docker     (123)     2045 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/lib/Header.svelte
+-rw-r--r--   0 runner    (1001) docker     (123)      219 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/lib/appState.ts
+-rw-r--r--   0 runner    (1001) docker     (123)      467 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/lib/dataTypes.ts
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.544301 pyinstrument-4.5.1/html_renderer/src/lib/model/
+-rw-r--r--   0 runner    (1001) docker     (123)     1647 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/lib/model/Frame.ts
+-rw-r--r--   0 runner    (1001) docker     (123)      996 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/lib/model/Group.ts
+-rw-r--r--   0 runner    (1001) docker     (123)      584 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/lib/model/Session.ts
+-rw-r--r--   0 runner    (1001) docker     (123)      335 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/main.ts
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/src/vite-env.d.ts
+-rw-r--r--   0 runner    (1001) docker     (123)      207 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/svelte.config.js
+-rw-r--r--   0 runner    (1001) docker     (123)      658 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/tsconfig.json
+-rw-r--r--   0 runner    (1001) docker     (123)      142 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/tsconfig.node.json
+-rw-r--r--   0 runner    (1001) docker     (123)      463 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/html_renderer/vite.config.ts
+-rw-r--r--   0 runner    (1001) docker     (123)      151 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/noxfile.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.548302 pyinstrument-4.5.1/pyinstrument/
+-rw-r--r--   0 runner    (1001) docker     (123)      564 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17945 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12364 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/frame.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1038 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/frame_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4934 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/frame_ops.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.548302 pyinstrument-4.5.1/pyinstrument/low_level/
+-rw-r--r--   0 runner    (1001) docker     (123)    22285 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/low_level/stat_profile.c
+-rw-r--r--   0 runner    (1001) docker     (123)      369 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/low_level/stat_profile.pyi
+-rw-r--r--   0 runner    (1001) docker     (123)     3476 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/low_level/stat_profile_python.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.548302 pyinstrument-4.5.1/pyinstrument/magic/
+-rw-r--r--   0 runner    (1001) docker     (123)       37 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/magic/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3096 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/magic/_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5637 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/magic/magic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3600 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/middleware.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9219 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/processors.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11123 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/profiler.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.548302 pyinstrument-4.5.1/pyinstrument/renderers/
+-rw-r--r--   0 runner    (1001) docker     (123)      426 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3597 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8373 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/console.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3231 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/html.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.548302 pyinstrument-4.5.1/pyinstrument/renderers/html_resources/
+-rw-r--r--   0 runner    (1001) docker     (123)     2856 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/html_resources/app.css
+-rw-r--r--   0 runner    (1001) docker     (123)    18767 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/html_resources/app.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3287 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/jsonrenderer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3265 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/pstatsrenderer.py
+-rw-r--r--   0 runner    (1001) docker     (123)      277 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/session.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8593 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/renderers/speedscope.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4935 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/session.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7272 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/stack_sampler.py
+-rw-r--r--   0 runner    (1001) docker     (123)      539 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/typing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2158 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.548302 pyinstrument-4.5.1/pyinstrument/vendor/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/vendor/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25076 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/vendor/appdirs.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16323 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/vendor/decorator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3202 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyinstrument/vendor/keypath.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.552302 pyinstrument-4.5.1/pyinstrument.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2358 2023-07-22 22:23:17.000000 pyinstrument-4.5.1/pyinstrument.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      209 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      475 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/requirements-dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       95 2023-07-22 22:23:17.552302 pyinstrument-4.5.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1530 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.548302 pyinstrument-4.5.1/test/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1437 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2303 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/fake_time_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:17.552302 pyinstrument-4.5.1/test/low_level/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/low_level/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1708 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/low_level/test_context.py
+-rw-r--r--   0 runner    (1001) docker     (123)      616 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/low_level/test_custom_timer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2052 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/low_level/test_frame_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1101 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/low_level/test_setstatprofile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1226 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/low_level/test_threaded.py
+-rw-r--r--   0 runner    (1001) docker     (123)      478 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/low_level/util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7593 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_cmdline.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2567 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_cmdline_main.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_ipython_magic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1318 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_overflow.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12960 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_processors.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10411 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_profiler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6542 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_profiler_async.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1987 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_pstats_renderer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3136 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_stack_sampler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1102 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/test_threading.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-07-22 22:23:13.000000 pyinstrument-4.5.1/test/util.py
```

### Comparing `pyinstrument-4.5.0/LICENSE` & `pyinstrument-4.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/PKG-INFO` & `pyinstrument-4.5.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyinstrument
-Version: 4.5.0
+Version: 4.5.1
 Summary: Call stack profiler for Python. Shows you why your code is slow!
 Home-page: https://github.com/joerick/pyinstrument
 Author: Joe Rickerby
 Author-email: joerick@mac.com
 License: UNKNOWN
 Description: pyinstrument
         ============
@@ -58,14 +58,22 @@
           serialized with `pickle`, you might encounter errors because the
           serialisation machinery doesn't know where `__main__` is. [See this issue
           for workarounds](https://github.com/joerick/pyinstrument/issues/109#issuecomment-722276263)
         
         Changelog
         ---------
         
+        ### v4.5.1
+        
+        _22 July 2023_
+        
+        -   Fix a bug that caused `[X frames hidden]` in the output when frames were deleted due to `__tracebackhide__` (#255)
+        -   Fix a bug causing built-in code to display the filepath `None` in the console output (#254)
+        -   Some docs improvements (#251)
+        
         ### v4.5.0
         
         _5 June 2023_
         
         -   Adds a flat mode to the console renderer, which can be enabled by passing `-p flat` on the command line. This mode shows the heaviest frame as measured by self-time, which can be useful in some codebases. (#240)
         -   Adds the ability to save `pstats` files. This is the file format used by cprofile in the stdlib. It's less detailed than pyinstrument profiles, but it's compatible with more tools. (#236)
         -   Fixes a detail of the `--show-all` option - pyinstrument will no longer remove Python-internal frames when this option is supplied. (#239)
```

### Comparing `pyinstrument-4.5.0/README.md` & `pyinstrument-4.5.1/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -50,14 +50,22 @@
   serialized with `pickle`, you might encounter errors because the
   serialisation machinery doesn't know where `__main__` is. [See this issue
   for workarounds](https://github.com/joerick/pyinstrument/issues/109#issuecomment-722276263)
 
 Changelog
 ---------
 
+### v4.5.1
+
+_22 July 2023_
+
+-   Fix a bug that caused `[X frames hidden]` in the output when frames were deleted due to `__tracebackhide__` (#255)
+-   Fix a bug causing built-in code to display the filepath `None` in the console output (#254)
+-   Some docs improvements (#251)
+
 ### v4.5.0
 
 _5 June 2023_
 
 -   Adds a flat mode to the console renderer, which can be enabled by passing `-p flat` on the command line. This mode shows the heaviest frame as measured by self-time, which can be useful in some codebases. (#240)
 -   Adds the ability to save `pstats` files. This is the file format used by cprofile in the stdlib. It's less detailed than pyinstrument profiles, but it's compatible with more tools. (#236)
 -   Fixes a detail of the `--show-all` option - pyinstrument will no longer remove Python-internal frames when this option is supplied. (#239)
```

### Comparing `pyinstrument-4.5.0/bin/build_js_bundle.py` & `pyinstrument-4.5.1/bin/build_js_bundle.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/bin/bump_version.py` & `pyinstrument-4.5.1/bin/bump_version.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/index.html` & `pyinstrument-4.5.1/html_renderer/index.html`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/package-lock.json` & `pyinstrument-4.5.1/html_renderer/package-lock.json`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/package.json` & `pyinstrument-4.5.1/html_renderer/package.json`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/public/sample.json` & `pyinstrument-4.5.1/html_renderer/public/sample.json`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/src/App.svelte` & `pyinstrument-4.5.1/html_renderer/src/App.svelte`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/src/assets/favicon.png` & `pyinstrument-4.5.1/html_renderer/src/assets/favicon.png`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/src/lib/Frame.svelte` & `pyinstrument-4.5.1/html_renderer/src/lib/Frame.svelte`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/src/lib/Header.svelte` & `pyinstrument-4.5.1/html_renderer/src/lib/Header.svelte`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/src/lib/model/Frame.ts` & `pyinstrument-4.5.1/html_renderer/src/lib/model/Frame.ts`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/src/lib/model/Group.ts` & `pyinstrument-4.5.1/html_renderer/src/lib/model/Group.ts`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/src/lib/model/Session.ts` & `pyinstrument-4.5.1/html_renderer/src/lib/model/Session.ts`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/html_renderer/tsconfig.json` & `pyinstrument-4.5.1/html_renderer/tsconfig.json`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/__init__.py` & `pyinstrument-4.5.1/pyinstrument/__init__.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import warnings
 
 from pyinstrument.profiler import Profiler
 
 __all__ = ["__version__", "Profiler", "load_ipython_extension"]
-__version__ = "4.5.0"
+__version__ = "4.5.1"
 
 # enable deprecation warnings
 warnings.filterwarnings("once", ".*", DeprecationWarning, r"pyinstrument\..*")
 
 
 def load_ipython_extension(ipython):
     """
```

### Comparing `pyinstrument-4.5.0/pyinstrument/__main__.py` & `pyinstrument-4.5.1/pyinstrument/__main__.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/frame.py` & `pyinstrument-4.5.1/pyinstrument/frame.py`

 * *Files 1% similar despite different names*

```diff
@@ -147,32 +147,37 @@
     @property
     def file_path_short(self) -> str | None:
         """Return the path resolved against the closest entry in sys.path"""
         if self.is_synthetic and self.parent:
             return self.parent.file_path_short
 
         if not hasattr(self, "_file_path_short"):
-            if self.file_path:
-                result = None
+            result = None
 
-                for path in sys.path:
-                    # On Windows, if self.file_path and path are on different drives, relpath
-                    # will result in exception, because it cannot compute a relpath in this case.
-                    # The root cause is that on Windows, there is no root dir like '/' on Linux.
-                    try:
-                        candidate = os.path.relpath(self.file_path, path)
-                    except ValueError:
-                        continue
+            if self.file_path:
+                if len(self.file_path.split(os.sep)) == 1:
+                    # probably not a file path at all, more likely <built-in>
+                    # or similar
+                    result = self.file_path
+                else:
+                    for path in sys.path:
+                        # On Windows, if self.file_path and path are on
+                        # different drives, relpath will result in exception,
+                        # because it cannot compute a relpath in this case.
+                        # The root cause is that on Windows, there is no root
+                        # dir like '/' on Linux.
+                        try:
+                            candidate = os.path.relpath(self.file_path, path)
+                        except ValueError:
+                            continue
 
-                    if not result or (len(candidate.split(os.sep)) < len(result.split(os.sep))):
-                        result = candidate
+                        if not result or (len(candidate.split(os.sep)) < len(result.split(os.sep))):
+                            result = candidate
 
-                self._file_path_short = result
-            else:
-                self._file_path_short = None
+            self._file_path_short = result
 
         return self._file_path_short
 
     @property
     def is_application_code(self) -> bool:
         if self.is_synthetic:
             return False
@@ -200,14 +205,15 @@
 
         return True
 
     @property
     def code_position_short(self) -> str | None:
         if self.file_path_short and self.line_no:
             return "%s:%i" % (self.file_path_short, self.line_no)
+        return self.file_path_short
 
     _children: list[Frame]
     attributes: dict[str, float]
 
     def add_child(self, frame: Frame, after: Frame | None = None):
         """
         Adds a child frame, updating the parent link.
@@ -357,22 +363,26 @@
 
         return self._libraries
 
     @property
     def frames(self) -> Sequence[Frame]:
         return tuple(self._frames)
 
-    # pylint: disable=W0212
     def add_frame(self, frame: Frame):
         if frame.group:
-            frame.group._frames.remove(frame)
+            frame.group.remove_frame(frame)
 
         self._frames.append(frame)
         frame.group = self
 
+    def remove_frame(self, frame: Frame):
+        assert frame.group is self
+        self._frames.remove(frame)
+        frame.group = None
+
     @property
     def exit_frames(self):
         """
         Returns a list of frames whose children include a frame outside of the group
         """
         if self._exit_frames is None:
             exit_frames: list[Frame] = []
```

### Comparing `pyinstrument-4.5.0/pyinstrument/frame_info.py` & `pyinstrument-4.5.1/pyinstrument/frame_info.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/frame_ops.py` & `pyinstrument-4.5.1/pyinstrument/frame_ops.py`

 * *Files 15% similar despite different names*

```diff
@@ -93,14 +93,19 @@
         parent.absorbed_time += frame.time
     else:
         assert_never(replace_with)
 
     parent.absorbed_time += frame.absorbed_time
 
     frame.remove_from_parent()
+    # in this call, recursive is true, even when replace_with is 'children'.
+    # When replace_with is 'self_time' or 'nothing', that's what we want. But
+    # when it's 'children', by now, the children have been removed and added
+    # to the parent, so recursive is irrelevant.
+    remove_frame_from_groups(frame, recursive=True)
 
 
 def combine_frames(frame: Frame, into: Frame):
     """
     Combine two frames into one. The frames must have the same parent.
 
     :param frame: the frame to remove
@@ -115,7 +120,28 @@
         try:
             into.attributes[attribute] += time
         except KeyError:
             into.attributes[attribute] = time
 
     into.add_children(frame.children)
     frame.remove_from_parent()
+    remove_frame_from_groups(frame, recursive=False)
+
+
+def remove_frame_from_groups(frame: Frame, recursive: bool):
+    """
+    Removes frame from any groups that it is a member of. Should be used when
+    removing a frame from a tree, so groups don't keep references to removed
+    frames.
+    """
+    if recursive and frame.children:
+        for child in frame.children:
+            remove_frame_from_groups(child, recursive=True)
+
+    if frame.group:
+        group = frame.group
+        group.remove_frame(frame)
+
+        if len(group.frames) == 1:
+            # a group with only one frame is meaningless, we'll remove it
+            # entirely.
+            group.remove_frame(group.frames[0])
```

### Comparing `pyinstrument-4.5.0/pyinstrument/low_level/stat_profile.c` & `pyinstrument-4.5.1/pyinstrument/low_level/stat_profile.c`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/low_level/stat_profile_python.py` & `pyinstrument-4.5.1/pyinstrument/low_level/stat_profile_python.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/magic/_utils.py` & `pyinstrument-4.5.1/pyinstrument/magic/_utils.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/magic/magic.py` & `pyinstrument-4.5.1/pyinstrument/magic/magic.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/middleware.py` & `pyinstrument-4.5.1/pyinstrument/middleware.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/processors.py` & `pyinstrument-4.5.1/pyinstrument/processors.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/profiler.py` & `pyinstrument-4.5.1/pyinstrument/profiler.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/renderers/base.py` & `pyinstrument-4.5.1/pyinstrument/renderers/base.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/renderers/console.py` & `pyinstrument-4.5.1/pyinstrument/renderers/console.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -208,18 +208,18 @@
 
     def default_processors(self) -> ProcessorList:
         return [
             processors.remove_importlib,
             processors.remove_tracebackhide,
             processors.merge_consecutive_self_time,
             processors.aggregate_repeated_calls,
-            processors.group_library_frames_processor,
             processors.remove_unnecessary_self_time_nodes,
             processors.remove_irrelevant_nodes,
             processors.remove_first_pyinstrument_frames_processor,
+            processors.group_library_frames_processor,
         ]
 
     class colors_enabled:
         red = "\033[31m"
         green = "\033[32m"
         yellow = "\033[33m"
         blue = "\033[34m"
```

### Comparing `pyinstrument-4.5.0/pyinstrument/renderers/html.py` & `pyinstrument-4.5.1/pyinstrument/renderers/html.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -92,12 +92,12 @@
 
     def default_processors(self) -> ProcessorList:
         return [
             processors.remove_importlib,
             processors.remove_tracebackhide,
             processors.merge_consecutive_self_time,
             processors.aggregate_repeated_calls,
-            processors.group_library_frames_processor,
             processors.remove_unnecessary_self_time_nodes,
             processors.remove_irrelevant_nodes,
             processors.remove_first_pyinstrument_frames_processor,
+            processors.group_library_frames_processor,
         ]
```

### Comparing `pyinstrument-4.5.0/pyinstrument/renderers/html_resources/app.css` & `pyinstrument-4.5.1/pyinstrument/renderers/html_resources/app.css`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/renderers/html_resources/app.js` & `pyinstrument-4.5.1/pyinstrument/renderers/html_resources/app.js`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/renderers/jsonrenderer.py` & `pyinstrument-4.5.1/pyinstrument/renderers/jsonrenderer.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -76,12 +76,12 @@
 
     def default_processors(self) -> ProcessorList:
         return [
             processors.remove_importlib,
             processors.remove_tracebackhide,
             processors.merge_consecutive_self_time,
             processors.aggregate_repeated_calls,
-            processors.group_library_frames_processor,
             processors.remove_unnecessary_self_time_nodes,
             processors.remove_irrelevant_nodes,
             processors.remove_first_pyinstrument_frames_processor,
+            processors.group_library_frames_processor,
         ]
```

### Comparing `pyinstrument-4.5.0/pyinstrument/renderers/pstatsrenderer.py` & `pyinstrument-4.5.1/pyinstrument/renderers/pstatsrenderer.py`

 * *Files 1% similar despite different names*

```diff
@@ -86,12 +86,11 @@
 
     def default_processors(self) -> ProcessorList:
         return [
             processors.remove_importlib,
             processors.remove_tracebackhide,
             processors.merge_consecutive_self_time,
             processors.aggregate_repeated_calls,
-            processors.group_library_frames_processor,
             processors.remove_unnecessary_self_time_nodes,
             processors.remove_irrelevant_nodes,
             processors.remove_first_pyinstrument_frames_processor,
         ]
```

### Comparing `pyinstrument-4.5.0/pyinstrument/renderers/speedscope.py` & `pyinstrument-4.5.1/pyinstrument/renderers/speedscope.py`

 * *Files 1% similar despite different names*

```diff
@@ -232,12 +232,11 @@
         processors.aggregate_repeated_calls is removed because
         speedscope is a timeline-based format.
         """
         return [
             processors.remove_importlib,
             processors.remove_tracebackhide,
             processors.merge_consecutive_self_time,
-            processors.group_library_frames_processor,
             processors.remove_unnecessary_self_time_nodes,
             processors.remove_irrelevant_nodes,
             processors.remove_first_pyinstrument_frames_processor,
         ]
```

### Comparing `pyinstrument-4.5.0/pyinstrument/session.py` & `pyinstrument-4.5.1/pyinstrument/session.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/stack_sampler.py` & `pyinstrument-4.5.1/pyinstrument/stack_sampler.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/typing.py` & `pyinstrument-4.5.1/pyinstrument/typing.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/util.py` & `pyinstrument-4.5.1/pyinstrument/util.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/vendor/appdirs.py` & `pyinstrument-4.5.1/pyinstrument/vendor/appdirs.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/vendor/decorator.py` & `pyinstrument-4.5.1/pyinstrument/vendor/decorator.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument/vendor/keypath.py` & `pyinstrument-4.5.1/pyinstrument/vendor/keypath.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/pyinstrument.egg-info/SOURCES.txt` & `pyinstrument-4.5.1/pyinstrument.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/setup.py` & `pyinstrument-4.5.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 
 PROJECT_ROOT = Path(__file__).parent
 long_description = (PROJECT_ROOT / "README.md").read_text(encoding="utf8")
 
 setup(
     name="pyinstrument",
     packages=find_namespace_packages(include=["pyinstrument*"]),
-    version="4.5.0",
+    version="4.5.1",
     ext_modules=[
         Extension(
             "pyinstrument.low_level.stat_profile",
             sources=["pyinstrument/low_level/stat_profile.c"],
         )
     ],
     description="Call stack profiler for Python. Shows you why your code is slow!",
```

### Comparing `pyinstrument-4.5.0/test/conftest.py` & `pyinstrument-4.5.1/test/conftest.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/fake_time_util.py` & `pyinstrument-4.5.1/test/fake_time_util.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/low_level/test_context.py` & `pyinstrument-4.5.1/test/low_level/test_context.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/low_level/test_custom_timer.py` & `pyinstrument-4.5.1/test/low_level/test_custom_timer.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/low_level/test_frame_info.py` & `pyinstrument-4.5.1/test/low_level/test_frame_info.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/low_level/test_setstatprofile.py` & `pyinstrument-4.5.1/test/low_level/test_setstatprofile.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/low_level/test_threaded.py` & `pyinstrument-4.5.1/test/low_level/test_threaded.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_cmdline.py` & `pyinstrument-4.5.1/test/test_cmdline.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_cmdline_main.py` & `pyinstrument-4.5.1/test/test_cmdline_main.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_ipython_magic.py` & `pyinstrument-4.5.1/test/test_ipython_magic.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_overflow.py` & `pyinstrument-4.5.1/test/test_overflow.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_processors.py` & `pyinstrument-4.5.1/test/test_processors.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_profiler.py` & `pyinstrument-4.5.1/test/test_profiler.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_profiler_async.py` & `pyinstrument-4.5.1/test/test_profiler_async.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_pstats_renderer.py` & `pyinstrument-4.5.1/test/test_pstats_renderer.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_stack_sampler.py` & `pyinstrument-4.5.1/test/test_stack_sampler.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/test_threading.py` & `pyinstrument-4.5.1/test/test_threading.py`

 * *Files identical despite different names*

### Comparing `pyinstrument-4.5.0/test/util.py` & `pyinstrument-4.5.1/test/util.py`

 * *Files identical despite different names*

