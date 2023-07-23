# Comparing `tmp/localeet-0.1.0.tar.gz` & `tmp/localeet-0.1.1.tar.gz`

## Comparing `localeet-0.1.0.tar` & `localeet-0.1.1.tar`

### file list

```diff
@@ -1,20 +1,20 @@
--rw-r--r--   0        0        0      943 2020-02-02 00:00:00.000000 localeet-0.1.0/.pre-commit-config.yaml
--rw-r--r--   0        0        0     2255 2020-02-02 00:00:00.000000 localeet-0.1.0/README.md
--rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 localeet-0.1.0/.github/workflows/pr.yml
--rw-r--r--   0        0        0      672 2020-02-02 00:00:00.000000 localeet-0.1.0/.github/workflows/pypi.yaml
--rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.1.0/src/localeet/__init__.py
--rw-r--r--   0        0        0     2052 2020-02-02 00:00:00.000000 localeet-0.1.0/src/localeet/__main__.py
--rw-r--r--   0        0        0     6587 2020-02-02 00:00:00.000000 localeet-0.1.0/src/localeet/get_leetcode_problem.py
--rw-r--r--   0        0        0     3740 2020-02-02 00:00:00.000000 localeet-0.1.0/src/localeet/language_maps.py
--rw-r--r--   0        0        0     1497 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/conftest.py
--rw-r--r--   0        0        0     2515 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/get_leetcode_problem_test.py
--rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/version_number_test.py
--rw-r--r--   0        0        0      851 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum.go
--rw-r--r--   0        0        0      974 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum.py
--rw-r--r--   0        0        0      895 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum.rs
--rw-r--r--   0        0        0    20244 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum_details.json
--rw-r--r--   0        0        0     5902 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum_essentials.json
--rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.1.0/.gitignore
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.1.0/LICENSE
--rw-r--r--   0        0        0     3828 2020-02-02 00:00:00.000000 localeet-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0      943 2020-02-02 00:00:00.000000 localeet-0.1.1/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     2186 2020-02-02 00:00:00.000000 localeet-0.1.1/README.md
+-rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 localeet-0.1.1/.github/workflows/pr.yml
+-rw-r--r--   0        0        0      672 2020-02-02 00:00:00.000000 localeet-0.1.1/.github/workflows/pypi.yaml
+-rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.1.1/src/localeet/__init__.py
+-rw-r--r--   0        0        0     2052 2020-02-02 00:00:00.000000 localeet-0.1.1/src/localeet/__main__.py
+-rw-r--r--   0        0        0     6587 2020-02-02 00:00:00.000000 localeet-0.1.1/src/localeet/get_leetcode_problem.py
+-rw-r--r--   0        0        0     3740 2020-02-02 00:00:00.000000 localeet-0.1.1/src/localeet/language_maps.py
+-rw-r--r--   0        0        0     1497 2020-02-02 00:00:00.000000 localeet-0.1.1/tests/conftest.py
+-rw-r--r--   0        0        0     2515 2020-02-02 00:00:00.000000 localeet-0.1.1/tests/get_leetcode_problem_test.py
+-rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 localeet-0.1.1/tests/version_number_test.py
+-rw-r--r--   0        0        0      851 2020-02-02 00:00:00.000000 localeet-0.1.1/tests/data/two_sum.go
+-rw-r--r--   0        0        0      974 2020-02-02 00:00:00.000000 localeet-0.1.1/tests/data/two_sum.py
+-rw-r--r--   0        0        0      895 2020-02-02 00:00:00.000000 localeet-0.1.1/tests/data/two_sum.rs
+-rw-r--r--   0        0        0    20244 2020-02-02 00:00:00.000000 localeet-0.1.1/tests/data/two_sum_details.json
+-rw-r--r--   0        0        0     5902 2020-02-02 00:00:00.000000 localeet-0.1.1/tests/data/two_sum_essentials.json
+-rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.1.1/.gitignore
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.1.1/LICENSE
+-rw-r--r--   0        0        0     3828 2020-02-02 00:00:00.000000 localeet-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.1.1/PKG-INFO
```

### Comparing `localeet-0.1.0/.pre-commit-config.yaml` & `localeet-0.1.1/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/README.md` & `localeet-0.1.1/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -116,11 +116,10 @@
 6. Ensure Pull Request Verification CI/CD pipeline passes
 7. Get approved & merged
 8. Ensure Publish to PyPI pipeline passes
 
 
 ## feature ideas
 
-* Support creating files for programming languages other than Python
 * Add commitizen for auto version updating
 * Support submitting responses to LeetCode via CLI as well
 * Whatever your imagination holds
```

### Comparing `localeet-0.1.0/.github/workflows/pr.yml` & `localeet-0.1.1/.github/workflows/pr.yml`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/.github/workflows/pypi.yaml` & `localeet-0.1.1/.github/workflows/pypi.yaml`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/src/localeet/__main__.py` & `localeet-0.1.1/src/localeet/__main__.py`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/src/localeet/get_leetcode_problem.py` & `localeet-0.1.1/src/localeet/get_leetcode_problem.py`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/src/localeet/language_maps.py` & `localeet-0.1.1/src/localeet/language_maps.py`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/tests/conftest.py` & `localeet-0.1.1/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/tests/get_leetcode_problem_test.py` & `localeet-0.1.1/tests/get_leetcode_problem_test.py`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/tests/version_number_test.py` & `localeet-0.1.1/tests/version_number_test.py`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/tests/data/two_sum.go` & `localeet-0.1.1/tests/data/two_sum.go`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/tests/data/two_sum.py` & `localeet-0.1.1/tests/data/two_sum.py`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/tests/data/two_sum.rs` & `localeet-0.1.1/tests/data/two_sum.rs`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/tests/data/two_sum_details.json` & `localeet-0.1.1/tests/data/two_sum_details.json`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/tests/data/two_sum_essentials.json` & `localeet-0.1.1/tests/data/two_sum_essentials.json`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/.gitignore` & `localeet-0.1.1/.gitignore`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/LICENSE` & `localeet-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/pyproject.toml` & `localeet-0.1.1/pyproject.toml`

 * *Files identical despite different names*

### Comparing `localeet-0.1.0/PKG-INFO` & `localeet-0.1.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: localeet
-Version: 0.1.0
+Version: 0.1.1
 Summary: A CLI tool to do LeetCode and LeetCode-like exercises
 Author-email: Danny Brown <dannybrown37@gmail.com>
 License-File: LICENSE
 Requires-Dist: bs4
 Requires-Dist: click
 Requires-Dist: lxml
 Requires-Dist: requests
```

