# Comparing `tmp/localeet-0.0.1.tar.gz` & `tmp/localeet-0.0.2.tar.gz`

## Comparing `localeet-0.0.1.tar` & `localeet-0.0.2.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0      913 2020-02-02 00:00:00.000000 localeet-0.0.1/.pre-commit-config.yaml
--rw-r--r--   0        0        0      941 2020-02-02 00:00:00.000000 localeet-0.0.1/README.md
--rw-r--r--   0        0        0      643 2020-02-02 00:00:00.000000 localeet-0.0.1/.github/workflows/pr.yml
--rw-r--r--   0        0        0      608 2020-02-02 00:00:00.000000 localeet-0.0.1/.github/workflows/pypi.yaml
--rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.1/src/localeet/__init__.py
--rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 localeet-0.0.1/src/localeet/__main__.py
--rw-r--r--   0        0        0     5696 2020-02-02 00:00:00.000000 localeet-0.0.1/src/localeet/get_leetcode_problem.py
--rw-r--r--   0        0        0     1534 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/conftest.py
--rw-r--r--   0        0        0     2090 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/get_leetcode_problem_test.py
--rw-r--r--   0        0        0      881 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/version_number_test.py
--rw-r--r--   0        0        0      833 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/data/two_sum.py
--rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/data/two_sum_details.json
--rw-r--r--   0        0        0      918 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/data/two_sum_essentials.json
--rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.1/.gitignore
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.1/LICENSE
--rw-r--r--   0        0        0     3527 2020-02-02 00:00:00.000000 localeet-0.0.1/pyproject.toml
--rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0      938 2020-02-02 00:00:00.000000 localeet-0.0.2/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     1590 2020-02-02 00:00:00.000000 localeet-0.0.2/README.md
+-rw-r--r--   0        0        0      643 2020-02-02 00:00:00.000000 localeet-0.0.2/.github/workflows/pr.yml
+-rw-r--r--   0        0        0      608 2020-02-02 00:00:00.000000 localeet-0.0.2/.github/workflows/pypi.yaml
+-rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.2/src/localeet/__init__.py
+-rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 localeet-0.0.2/src/localeet/__main__.py
+-rw-r--r--   0        0        0     5696 2020-02-02 00:00:00.000000 localeet-0.0.2/src/localeet/get_leetcode_problem.py
+-rw-r--r--   0        0        0     1534 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/conftest.py
+-rw-r--r--   0        0        0     2090 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/get_leetcode_problem_test.py
+-rw-r--r--   0        0        0      881 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/version_number_test.py
+-rw-r--r--   0        0        0      833 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/data/two_sum.py
+-rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/data/two_sum_details.json
+-rw-r--r--   0        0        0      918 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/data/two_sum_essentials.json
+-rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.2/.gitignore
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.2/LICENSE
+-rw-r--r--   0        0        0     3527 2020-02-02 00:00:00.000000 localeet-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.2/PKG-INFO
```

### Comparing `localeet-0.0.1/.pre-commit-config.yaml` & `localeet-0.0.2/.pre-commit-config.yaml`

 * *Files 1% similar despite different names*

```diff
@@ -23,14 +23,15 @@
       - id: name-tests-test
       - id: trailing-whitespace
 
   - repo: local
     hooks:
       - id: pytest
         name: Pytest
+        always_run: true
         entry: pytest tests -s -vvl
         language: system
         types: [python]
       - id: ruff
         name: Ruff
         entry: ruff src --fix
         language: system
```

### Comparing `localeet-0.0.1/.github/workflows/pr.yml` & `localeet-0.0.2/.github/workflows/pr.yml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/.github/workflows/pypi.yaml` & `localeet-0.0.2/.github/workflows/pypi.yaml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/src/localeet/__main__.py` & `localeet-0.0.2/src/localeet/__main__.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/src/localeet/get_leetcode_problem.py` & `localeet-0.0.2/src/localeet/get_leetcode_problem.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/tests/conftest.py` & `localeet-0.0.2/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/tests/get_leetcode_problem_test.py` & `localeet-0.0.2/tests/get_leetcode_problem_test.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/tests/version_number_test.py` & `localeet-0.0.2/tests/version_number_test.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/tests/data/two_sum.py` & `localeet-0.0.2/tests/data/two_sum.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/tests/data/two_sum_details.json` & `localeet-0.0.2/tests/data/two_sum_details.json`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/tests/data/two_sum_essentials.json` & `localeet-0.0.2/tests/data/two_sum_essentials.json`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/.gitignore` & `localeet-0.0.2/.gitignore`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/LICENSE` & `localeet-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/pyproject.toml` & `localeet-0.0.2/pyproject.toml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.1/PKG-INFO` & `localeet-0.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: localeet
-Version: 0.0.1
+Version: 0.0.2
 Summary: A CLI tool to do LeetCode and LeetCode-like exercises
 Author-email: Danny Brown <dannybrown37@gmail.com>
 License-File: LICENSE
 Requires-Dist: bs4
 Requires-Dist: click
 Requires-Dist: lxml
 Requires-Dist: requests
```

