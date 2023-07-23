# Comparing `tmp/localeet-0.0.0.tar.gz` & `tmp/localeet-0.0.1.tar.gz`

## Comparing `localeet-0.0.0.tar` & `localeet-0.0.1.tar`

### file list

```diff
@@ -1,16 +1,17 @@
--rw-r--r--   0        0        0      913 2020-02-02 00:00:00.000000 localeet-0.0.0/.pre-commit-config.yaml
--rw-r--r--   0        0        0      941 2020-02-02 00:00:00.000000 localeet-0.0.0/README.md
--rw-r--r--   0        0        0      601 2020-02-02 00:00:00.000000 localeet-0.0.0/.github/workflows/pr.yml
--rw-r--r--   0        0        0      607 2020-02-02 00:00:00.000000 localeet-0.0.0/.github/workflows/pypi.yaml
--rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.0/src/localeet/__init__.py
--rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 localeet-0.0.0/src/localeet/__main__.py
--rw-r--r--   0        0        0     5696 2020-02-02 00:00:00.000000 localeet-0.0.0/src/localeet/get_leetcode_problem.py
--rw-r--r--   0        0        0     1563 2020-02-02 00:00:00.000000 localeet-0.0.0/tests/conftest.py
--rw-r--r--   0        0        0     2088 2020-02-02 00:00:00.000000 localeet-0.0.0/tests/get_leetcode_problem_test.py
--rw-r--r--   0        0        0      833 2020-02-02 00:00:00.000000 localeet-0.0.0/tests/data/two_sum.py
--rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.0/tests/data/two_sum_details.json
--rw-r--r--   0        0        0      918 2020-02-02 00:00:00.000000 localeet-0.0.0/tests/data/two_sum_essentials.json
--rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.0/.gitignore
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.0/LICENSE
--rw-r--r--   0        0        0     3503 2020-02-02 00:00:00.000000 localeet-0.0.0/pyproject.toml
--rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.0/PKG-INFO
+-rw-r--r--   0        0        0      913 2020-02-02 00:00:00.000000 localeet-0.0.1/.pre-commit-config.yaml
+-rw-r--r--   0        0        0      941 2020-02-02 00:00:00.000000 localeet-0.0.1/README.md
+-rw-r--r--   0        0        0      643 2020-02-02 00:00:00.000000 localeet-0.0.1/.github/workflows/pr.yml
+-rw-r--r--   0        0        0      608 2020-02-02 00:00:00.000000 localeet-0.0.1/.github/workflows/pypi.yaml
+-rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.1/src/localeet/__init__.py
+-rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 localeet-0.0.1/src/localeet/__main__.py
+-rw-r--r--   0        0        0     5696 2020-02-02 00:00:00.000000 localeet-0.0.1/src/localeet/get_leetcode_problem.py
+-rw-r--r--   0        0        0     1534 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/conftest.py
+-rw-r--r--   0        0        0     2090 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/get_leetcode_problem_test.py
+-rw-r--r--   0        0        0      881 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/version_number_test.py
+-rw-r--r--   0        0        0      833 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/data/two_sum.py
+-rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/data/two_sum_details.json
+-rw-r--r--   0        0        0      918 2020-02-02 00:00:00.000000 localeet-0.0.1/tests/data/two_sum_essentials.json
+-rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.1/.gitignore
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.1/LICENSE
+-rw-r--r--   0        0        0     3527 2020-02-02 00:00:00.000000 localeet-0.0.1/pyproject.toml
+-rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.1/PKG-INFO
```

### Comparing `localeet-0.0.0/.pre-commit-config.yaml` & `localeet-0.0.1/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.0/README.md` & `localeet-0.0.1/README.md`

 * *Files identical despite different names*

### Comparing `localeet-0.0.0/.github/workflows/pr.yml` & `localeet-0.0.1/.github/workflows/pr.yml`

 * *Files 21% similar despite different names*

```diff
@@ -16,17 +16,19 @@
 
       - name: Set up Python
         uses: actions/setup-python@v2
         with:
           python-version: 3.9
 
       - name: Install localeet test dependencies
-        run: pip install .[test]
+        run: |
+          pip install -U pip
+          pip install .[test]
 
       - name: Run tests
         run: pytest tests -s -vvl
 
       - name: Install localeet dev dependencies
         run: pip install .[dev]
 
       - name: Run ruff
-        run: ruff src
+        run: ruff src
```

### Comparing `localeet-0.0.0/src/localeet/__main__.py` & `localeet-0.0.1/src/localeet/__main__.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.0/src/localeet/get_leetcode_problem.py` & `localeet-0.0.1/src/localeet/get_leetcode_problem.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.0/tests/conftest.py` & `localeet-0.0.1/tests/conftest.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,15 +1,21 @@
 import json
+from pathlib import Path
 
 import pytest
 
 
 class MockValue:
     """Allows any of a datatype to pass comparison within dictionary"""
-    def __init__(self, name='MOCK_VALUE', data_type=None, validator=None):
+    def __init__(
+            self,
+            name='MOCK_VALUE',
+            data_type=None,
+            validator=None,
+        ) -> None:
         self.name = name
         self.data_type = data_type
         self.validator = validator
 
     def __eq__(self, item):
         if (
             (self.data_type and not isinstance(item, self.data_type)) or
@@ -17,51 +23,42 @@
         ):
             return False
         return True
 
     def __ne__(self, item):
         return not self.__eq__(item)
 
-    def __repr__(self):
+    def __repr__(self) -> str:
         return f'<ANY_{self.name}>'
 
 
 @pytest.fixture(scope='session')
-def any_int():
+def any_int() -> MockValue:
     return MockValue('INT', int)
 
 
 @pytest.fixture(scope='session')
-def any_str():
+def any_str() -> MockValue:
     return MockValue('STR', str)
 
 
 @pytest.fixture(scope='session')
-def any_json_str():
+def any_json_str() -> MockValue:
     return MockValue('JSON_STR', str, lambda x: json.loads(x))
 
 
 @pytest.fixture(scope='session')
-def two_sum_start():
-    return MockValue(
-        'TWO_SUM_DESCRIPTION',
-        str,
-        lambda x: x.startswith('Given an array of integers'),
-    )
-
-
-@pytest.fixture(scope='session')
-def two_sum_details_json():
-    with open('tests/data/two_sum_details.json', 'r') as f:
+def two_sum_details_json() -> dict:
+    with Path('tests/data/two_sum_details.json').open() as f:
         return json.load(f)
 
 
 @pytest.fixture(scope='session')
-def two_sum_essentials():
-    with open('tests/data/two_sum_essentials.json', 'r') as f:
+def two_sum_essentials() -> dict:
+    with Path('tests/data/two_sum_essentials.json').open() as f:
         return json.load(f)
 
 
 @pytest.fixture(scope='session')
 def sample_two_sum_python_file():
-    with open('tests/data/two_sum.py', 'r') as f:
-        return f.read()
+    with Path('tests/data/two_sum.py').open() as f:
+        return f.read()
```

### Comparing `localeet-0.0.0/tests/get_leetcode_problem_test.py` & `localeet-0.0.1/tests/get_leetcode_problem_test.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from pathlib import Path
 
 from localeet.get_leetcode_problem import (
-    query_all_questions,
     choose_a_valid_question,
     get_question_data,
-    parse_question_details,
     output_python_file,
+    parse_question_details,
+    query_all_questions,
 )
 
 
 def test_query_all_questions(any_int):
     """Test that query for question list works"""
     result = query_all_questions()
     assert len(result) >= 2787  # assuming number never goes down..
@@ -26,15 +26,15 @@
             'question__article__live': True,
             'question__article__slug': 'two-sum',
             'question__hide': False,
             'question__title': 'Two Sum',
             'question__title_slug': 'two-sum',
             'question_id': 1,
             'total_acs': any_int,
-            'total_submitted': any_int
+            'total_submitted': any_int,
         },
         'status': None,
     }
 
 
 def test_choose_a_valid_question():
     result = choose_a_valid_question(query_all_questions(), 1, 1)
@@ -60,11 +60,11 @@
     assert parse_question_details(two_sum_details_json) == two_sum_essentials
 
 
 def test_output_python_file(two_sum_essentials, sample_two_sum_python_file):
     path = Path('.')
     new_file = path / 'two_sum.py'
     output_python_file(path, two_sum_essentials)
-    with open(new_file) as f:
+    with new_file.open() as f:
         test_file = f.read()
     assert test_file == sample_two_sum_python_file
     new_file.unlink()
```

### Comparing `localeet-0.0.0/tests/data/two_sum.py` & `localeet-0.0.1/tests/data/two_sum.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.0/tests/data/two_sum_details.json` & `localeet-0.0.1/tests/data/two_sum_details.json`

 * *Files identical despite different names*

### Comparing `localeet-0.0.0/tests/data/two_sum_essentials.json` & `localeet-0.0.1/tests/data/two_sum_essentials.json`

 * *Files identical despite different names*

### Comparing `localeet-0.0.0/.gitignore` & `localeet-0.0.1/.gitignore`

 * *Files identical despite different names*

### Comparing `localeet-0.0.0/LICENSE` & `localeet-0.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `localeet-0.0.0/pyproject.toml` & `localeet-0.0.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -85,14 +85,15 @@
     "TID",  # https://beta.ruff.rs/docs/rules/#flake8-tidy-imports-tid
     "TRY",  # https://beta.ruff.rs/docs/rules/#tryceratops-try
     "W",  # https://beta.ruff.rs/docs/rules/#warning-w
     "UP",  # https://beta.ruff.rs/docs/rules/#pyupgrade-up
     "YTT",  # https://beta.ruff.rs/docs/rules/#flake8-2020-ytt
 ]
 ignore = [
-  "S311",  # we are not using randomness for cryptography
+  "S311",  # not using randomness for cryptography
+  "S101",  # assert is awesome
 ]
 show-fixes = true
 target-version = "py39"
 
 [tool.ruff.flake8-quotes]
 inline-quotes = "single"
```

### Comparing `localeet-0.0.0/PKG-INFO` & `localeet-0.0.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: localeet
-Version: 0.0.0
+Version: 0.0.1
 Summary: A CLI tool to do LeetCode and LeetCode-like exercises
 Author-email: Danny Brown <dannybrown37@gmail.com>
 License-File: LICENSE
 Requires-Dist: bs4
 Requires-Dist: click
 Requires-Dist: lxml
 Requires-Dist: requests
```

