# Comparing `tmp/tox_gh-1.2.0.tar.gz` & `tmp/tox_gh-1.3.0.tar.gz`

## Comparing `tox_gh-1.2.0.tar` & `tox_gh-1.3.0.tar`

### file list

```diff
@@ -1,12 +1,12 @@
--rw-r--r--   0        0        0      148 2020-02-02 00:00:00.000000 tox_gh-1.2.0/src/tox_gh/__init__.py
--rw-r--r--   0        0        0     4328 2020-02-02 00:00:00.000000 tox_gh-1.2.0/src/tox_gh/plugin.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 tox_gh-1.2.0/src/tox_gh/py.typed
--rw-r--r--   0        0        0      160 2020-02-02 00:00:00.000000 tox_gh-1.2.0/src/tox_gh/version.py
--rw-r--r--   0        0        0       75 2020-02-02 00:00:00.000000 tox_gh-1.2.0/tests/conftest.py
--rw-r--r--   0        0        0     4267 2020-02-02 00:00:00.000000 tox_gh-1.2.0/tests/test_tox_gh.py
--rw-r--r--   0        0        0      124 2020-02-02 00:00:00.000000 tox_gh-1.2.0/tests/test_version.py
--rw-r--r--   0        0        0      116 2020-02-02 00:00:00.000000 tox_gh-1.2.0/.gitignore
--rw-r--r--   0        0        0     1023 2020-02-02 00:00:00.000000 tox_gh-1.2.0/LICENSE
--rw-r--r--   0        0        0     2914 2020-02-02 00:00:00.000000 tox_gh-1.2.0/README.md
--rw-r--r--   0        0        0     3213 2020-02-02 00:00:00.000000 tox_gh-1.2.0/pyproject.toml
--rw-r--r--   0        0        0     4484 2020-02-02 00:00:00.000000 tox_gh-1.2.0/PKG-INFO
+-rw-r--r--   0        0        0      148 2020-02-02 00:00:00.000000 tox_gh-1.3.0/src/tox_gh/__init__.py
+-rw-r--r--   0        0        0     5091 2020-02-02 00:00:00.000000 tox_gh-1.3.0/src/tox_gh/plugin.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 tox_gh-1.3.0/src/tox_gh/py.typed
+-rw-r--r--   0        0        0      160 2020-02-02 00:00:00.000000 tox_gh-1.3.0/src/tox_gh/version.py
+-rw-r--r--   0        0        0       75 2020-02-02 00:00:00.000000 tox_gh-1.3.0/tests/conftest.py
+-rw-r--r--   0        0        0     5174 2020-02-02 00:00:00.000000 tox_gh-1.3.0/tests/test_tox_gh.py
+-rw-r--r--   0        0        0      124 2020-02-02 00:00:00.000000 tox_gh-1.3.0/tests/test_version.py
+-rw-r--r--   0        0        0      116 2020-02-02 00:00:00.000000 tox_gh-1.3.0/.gitignore
+-rw-r--r--   0        0        0     1023 2020-02-02 00:00:00.000000 tox_gh-1.3.0/LICENSE
+-rw-r--r--   0        0        0     2983 2020-02-02 00:00:00.000000 tox_gh-1.3.0/README.md
+-rw-r--r--   0        0        0     3213 2020-02-02 00:00:00.000000 tox_gh-1.3.0/pyproject.toml
+-rw-r--r--   0        0        0     4553 2020-02-02 00:00:00.000000 tox_gh-1.3.0/PKG-INFO
```

### Comparing `tox_gh-1.2.0/src/tox_gh/plugin.py` & `tox_gh-1.3.0/src/tox_gh/plugin.py`

 * *Files 12% similar despite different names*

```diff
@@ -2,15 +2,16 @@
 from __future__ import annotations
 
 import logging
 import os
 import pathlib
 import shutil
 import sys
-from typing import TYPE_CHECKING, Dict
+import threading
+from typing import TYPE_CHECKING, Any, Dict
 
 from tox.config.loader.memory import MemoryLoader
 from tox.config.loader.section import Section
 from tox.config.sets import ConfigSet
 from tox.config.types import EnvList
 from tox.execute import Outcome
 from tox.plugin import impl
@@ -76,22 +77,45 @@
 
     env_list = next((python_mapping[i] for i in get_python_version_keys() if i in python_mapping), None)
     if env_list is not None:  # override the env_list core configuration with our values
         logging.warning("tox-gh set %s", ", ".join(env_list))
         state.conf.core.loaders.insert(0, MemoryLoader(env_list=env_list))
 
 
+_STATE = threading.local()
+
+
+@impl
+def tox_on_install(tox_env: ToxEnv, arguments: Any, section: str, of_type: str) -> None:  # noqa: ANN401, ARG001
+    """
+    Run before installing to prepare an environment.
+
+    :param tox_env: the tox environment
+    :param arguments: installation arguments
+    :param section: section of the installation
+    :param of_type: type of the installation
+    """
+    if tox_env.core["is_on_gh_action"]:
+        installing = getattr(_STATE, "installing", False)
+        if not installing:
+            _STATE.installing = True
+            print("::group::tox:install")  # noqa: T201
+
+
 @impl
 def tox_before_run_commands(tox_env: ToxEnv) -> None:
     """
     Run logic before tox run commands.
 
     :param tox_env: the tox environment
     """
     if tox_env.core["is_on_gh_action"]:
+        assert _STATE.installing  # noqa: S101
+        _STATE.installing = False
+        print("::endgroup::")  # noqa: T201
         print(f"::group::tox:{tox_env.name}")  # noqa: T201
 
 
 @impl
 def tox_after_run_commands(tox_env: ToxEnv, exit_code: int, outcomes: list[Outcome]) -> None:  # noqa: ARG001
     """
     Run logic before after run commands.
```

### Comparing `tox_gh-1.2.0/tests/test_tox_gh.py` & `tox_gh-1.3.0/tests/test_tox_gh.py`

 * *Files 17% similar despite different names*

```diff
@@ -37,40 +37,58 @@
     result.assert_success()
     assert "tox-gh won't override envlist because envlist is explicitly given via TOXENV" in result.out
 
 
 def test_gh_ok(monkeypatch: MonkeyPatch, tox_project: ToxProjectCreator, tmp_path: Path) -> None:
     step_output_file = tmp_path / "gh_out"
     step_output_file.touch()
+    empty_requirements = tmp_path / "empty.txt"
+    empty_requirements.touch()
     monkeypatch.setenv("GITHUB_ACTIONS", "true")
     monkeypatch.delenv("TOXENV", raising=False)
     monkeypatch.setattr(plugin, "GITHUB_STEP_SUMMARY", str(step_output_file))
     ini = f"""
     [testenv]
-    package = skip
+    package = editable
+    deps = -r {empty_requirements}
     [gh]
     python =
         {sys.version_info[0]} = a, b
     """
     project = tox_project({"tox.ini": ini})
     result = project.run()
     result.assert_success()
-
     assert result.out.splitlines() == [
         "ROOT: running tox-gh",
         "ROOT: tox-gh set a, b",
+        "::group::tox:install",
+        f"a: install_deps> python -I -m pip install -r {empty_requirements}",
+        ANY,  # pip install setuptools wheel
+        ANY,  # .pkg: _optional_hooks
+        ANY,  # .pkg: get_requires_for_build_editable
+        ANY,  # .pkg: install_requires_for_build_editable
+        ".pkg: freeze> python -m pip freeze --all",
+        ANY,  # freeze list
+        ANY,  # .pkg: build_editable
+        ANY,  # a: install_package
         "a: freeze> python -m pip freeze --all",
         ANY,  # freeze list
+        "::endgroup::",
         "::group::tox:a",
         "::endgroup::",
         ANY,  # a finished
+        "::group::tox:install",
+        f"b: install_deps> python -I -m pip install -r {empty_requirements}",
+        ANY,  # b: install_package
         "b: freeze> python -m pip freeze --all",
         ANY,  # freeze list
+        "::endgroup::",
         "::group::tox:b",
         "::endgroup::",
+        ANY,  # .pkg: _exit
         ANY,  # a status
         ANY,  # b status
         ANY,  # outcome
     ]
 
     assert "a: OK" in result.out
     assert "b: OK" in result.out
@@ -97,23 +115,27 @@
     project = tox_project({"tox.ini": ini})
     result = project.run()
     result.assert_failed()
 
     assert result.out.splitlines() == [
         "ROOT: running tox-gh",
         "ROOT: tox-gh set a, b",
+        "::group::tox:install",
         "a: freeze> python -m pip freeze --all",
         ANY,  # freeze list
+        "::endgroup::",
         "::group::tox:a",
         ANY,  # "a: commands[0]> python -c 'exit(1)'", but without the quotes on Windows.
         ANY,  # process details
         "::endgroup::",
         ANY,  # a finished
+        "::group::tox:install",
         "b: freeze> python -m pip freeze --all",
         ANY,  # freeze list
+        "::endgroup::",
         "::group::tox:b",
         ANY,  # "b: commands[0]> python -c 'exit(1)'", but without the quotes on Windows.
         ANY,  # b process details
         "::endgroup::",
         ANY,  # a status
         ANY,  # b status
         ANY,  # outcome
```

### Comparing `tox_gh-1.2.0/LICENSE` & `tox_gh-1.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `tox_gh-1.2.0/README.md` & `tox_gh-1.3.0/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -54,46 +54,50 @@
 name: check
 on:
   push:
   pull_request:
   schedule:
     - cron: "0 8 * * *"
 
+concurrency:
+  group: check-${{ github.ref }}
+  cancel-in-progress: true
+
 jobs:
   test:
-    name: test ${{ matrix.py }} - ${{ matrix.os }}
-    runs-on: ${{ matrix.os }}-latest
+    name: test with ${{ matrix.py }} on ${{ matrix.os }}
+    runs-on: ${{ matrix.os }}
     strategy:
       fail-fast: false
       matrix:
-        os:
-          - Ubuntu
-          - Windows
-          - MacOs
         py:
           - "3.12"
           - "3.11"
           - "3.10"
           - "3.9"
           - "3.8"
           - "3.7"
+        os:
+          - ubuntu-latest
+          - macos-latest
+          - windows-latest
     steps:
+      - uses: actions/checkout@v3
+        with:
+          fetch-depth: 0
       - name: Setup python for test ${{ matrix.py }}
-        uses: actions/setup-python@v2
+        uses: actions/setup-python@v4
         with:
           python-version: ${{ matrix.py }}
-      - uses: actions/checkout@v2
-      - name: Install tox-gh
-        run: python -m pip install tox-gh
+      - name: Install tox
+        run: python -m pip install tox-gh>=1.2
       - name: Setup test suite
-        run: tox4 r -vv --notest
+        run: tox -vv --notest
       - name: Run test suite
-        run: tox4 r --skip-pkg-install
-        env:
-          PYTEST_ADDOPTS: "-vv --durations=10"
+        run: tox --skip-pkg-install
 ```
 
 ## FAQ
 
 - When a list of environments to run is specified explicitly via `-e` option or `TOXENV` environment variable `tox-gh`
   respects the given environments and simply runs the given environments without enforcing its configuration.
 - The plugin only activates if the environment variable `GITHUB_ACTIONS` is `true`.
```

### Comparing `tox_gh-1.2.0/pyproject.toml` & `tox_gh-1.3.0/pyproject.toml`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -58,28 +58,14 @@
 build.hooks.vcs.version-file = "src/tox_gh/version.py"
 build.targets.sdist.include = ["/src", "/tests"]
 version.source = "vcs"
 
 [tool.black]
 line-length = 120
 
-[tool.coverage]
-html.show_contexts = true
-html.skip_covered = false
-paths.source = ["src", ".tox/*/lib/*/site-packages", ".tox\\*\\Lib\\site-packages", "**/src", "**\\src"]
-paths.other = [".", "*/tox_gh", "*\\tox_gh"]
-report.fail_under = 96
-run.parallel = true
-run.plugins = ["covdefaults"]
-
-[tool.mypy]
-python_version = "3.11"
-show_error_codes = true
-strict = true
-
 [tool.ruff]
 select = ["ALL"]
 line-length = 120
 target-version = "py37"
 isort = {known-first-party = ["platformdirs", "tests"], required-imports = ["from __future__ import annotations"]}
 ignore = [
     "ANN101",  # Missing type annotation for `self` in method
@@ -95,7 +81,21 @@
     "S101",  # asserts allowed in tests...
     "FBT",  # don"t care about booleans as positional arguments in tests
     "INP001", # no implicit namespace
     "D",  # don"t care about documentation in tests
     "S603",  # `subprocess` call: check for execution of untrusted input
     "PLR2004",  # Magic value used in comparison, consider replacing with a constant variable
 ]
+
+[tool.coverage]
+html.show_contexts = true
+html.skip_covered = false
+paths.source = ["src", ".tox/*/lib/*/site-packages", ".tox\\*\\Lib\\site-packages", "**/src", "**\\src"]
+paths.other = [".", "*/tox_gh", "*\\tox_gh"]
+report.fail_under = 96
+run.parallel = true
+run.plugins = ["covdefaults"]
+
+[tool.mypy]
+python_version = "3.11"
+show_error_codes = true
+strict = true
```

### Comparing `tox_gh-1.2.0/PKG-INFO` & `tox_gh-1.3.0/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tox-gh
-Version: 1.2.0
+Version: 1.3.0
 Summary: Seamless integration of tox into GitHub Actions.
 Project-URL: Documentation, https://github.com/tox-dev/tox-gh#tox-gh
 Project-URL: Homepage, https://github.com/tox-dev/tox-gh
 Project-URL: Source, https://github.com/tox-dev/tox-gh
 Project-URL: Tracker, https://github.com/tox-dev/tox-gh/issues
 Maintainer-email: Bernát Gábor <gaborjbernat@gmail.com>
 License-Expression: MIT
@@ -91,46 +91,50 @@
 name: check
 on:
   push:
   pull_request:
   schedule:
     - cron: "0 8 * * *"
 
+concurrency:
+  group: check-${{ github.ref }}
+  cancel-in-progress: true
+
 jobs:
   test:
-    name: test ${{ matrix.py }} - ${{ matrix.os }}
-    runs-on: ${{ matrix.os }}-latest
+    name: test with ${{ matrix.py }} on ${{ matrix.os }}
+    runs-on: ${{ matrix.os }}
     strategy:
       fail-fast: false
       matrix:
-        os:
-          - Ubuntu
-          - Windows
-          - MacOs
         py:
           - "3.12"
           - "3.11"
           - "3.10"
           - "3.9"
           - "3.8"
           - "3.7"
+        os:
+          - ubuntu-latest
+          - macos-latest
+          - windows-latest
     steps:
+      - uses: actions/checkout@v3
+        with:
+          fetch-depth: 0
       - name: Setup python for test ${{ matrix.py }}
-        uses: actions/setup-python@v2
+        uses: actions/setup-python@v4
         with:
           python-version: ${{ matrix.py }}
-      - uses: actions/checkout@v2
-      - name: Install tox-gh
-        run: python -m pip install tox-gh
+      - name: Install tox
+        run: python -m pip install tox-gh>=1.2
       - name: Setup test suite
-        run: tox4 r -vv --notest
+        run: tox -vv --notest
       - name: Run test suite
-        run: tox4 r --skip-pkg-install
-        env:
-          PYTEST_ADDOPTS: "-vv --durations=10"
+        run: tox --skip-pkg-install
 ```
 
 ## FAQ
 
 - When a list of environments to run is specified explicitly via `-e` option or `TOXENV` environment variable `tox-gh`
   respects the given environments and simply runs the given environments without enforcing its configuration.
 - The plugin only activates if the environment variable `GITHUB_ACTIONS` is `true`.
```

