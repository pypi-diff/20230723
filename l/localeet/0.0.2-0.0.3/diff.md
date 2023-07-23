# Comparing `tmp/localeet-0.0.2.tar.gz` & `tmp/localeet-0.0.3.tar.gz`

## Comparing `localeet-0.0.2.tar` & `localeet-0.0.3.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0      938 2020-02-02 00:00:00.000000 localeet-0.0.2/.pre-commit-config.yaml
--rw-r--r--   0        0        0     1590 2020-02-02 00:00:00.000000 localeet-0.0.2/README.md
--rw-r--r--   0        0        0      643 2020-02-02 00:00:00.000000 localeet-0.0.2/.github/workflows/pr.yml
--rw-r--r--   0        0        0      608 2020-02-02 00:00:00.000000 localeet-0.0.2/.github/workflows/pypi.yaml
--rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.2/src/localeet/__init__.py
--rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 localeet-0.0.2/src/localeet/__main__.py
--rw-r--r--   0        0        0     5696 2020-02-02 00:00:00.000000 localeet-0.0.2/src/localeet/get_leetcode_problem.py
--rw-r--r--   0        0        0     1534 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/conftest.py
--rw-r--r--   0        0        0     2090 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/get_leetcode_problem_test.py
--rw-r--r--   0        0        0      881 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/version_number_test.py
--rw-r--r--   0        0        0      833 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/data/two_sum.py
--rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/data/two_sum_details.json
--rw-r--r--   0        0        0      918 2020-02-02 00:00:00.000000 localeet-0.0.2/tests/data/two_sum_essentials.json
--rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.2/.gitignore
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.2/LICENSE
--rw-r--r--   0        0        0     3527 2020-02-02 00:00:00.000000 localeet-0.0.2/pyproject.toml
--rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.2/PKG-INFO
+-rw-r--r--   0        0        0      944 2020-02-02 00:00:00.000000 localeet-0.0.3/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     1651 2020-02-02 00:00:00.000000 localeet-0.0.3/README.md
+-rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 localeet-0.0.3/.github/workflows/pr.yml
+-rw-r--r--   0        0        0      608 2020-02-02 00:00:00.000000 localeet-0.0.3/.github/workflows/pypi.yaml
+-rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.3/src/localeet/__init__.py
+-rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 localeet-0.0.3/src/localeet/__main__.py
+-rw-r--r--   0        0        0     5715 2020-02-02 00:00:00.000000 localeet-0.0.3/src/localeet/get_leetcode_problem.py
+-rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/conftest.py
+-rw-r--r--   0        0        0     2153 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/get_leetcode_problem_test.py
+-rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/version_number_test.py
+-rw-r--r--   0        0        0      834 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/data/two_sum.py
+-rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/data/two_sum_details.json
+-rw-r--r--   0        0        0      919 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/data/two_sum_essentials.json
+-rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.3/.gitignore
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.3/LICENSE
+-rw-r--r--   0        0        0     3828 2020-02-02 00:00:00.000000 localeet-0.0.3/pyproject.toml
+-rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.3/PKG-INFO
```

### Comparing `localeet-0.0.2/.pre-commit-config.yaml` & `localeet-0.0.3/.pre-commit-config.yaml`

 * *Files 1% similar despite different names*

```diff
@@ -29,10 +29,10 @@
         name: Pytest
         always_run: true
         entry: pytest tests -s -vvl
         language: system
         types: [python]
       - id: ruff
         name: Ruff
-        entry: ruff src --fix
+        entry: ruff src tests --fix
         language: system
         types: [python]
```

### Comparing `localeet-0.0.2/README.md` & `localeet-0.0.3/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -63,10 +63,11 @@
 7. Get approved & merged
 8. Ensure Publish to PyPI pipeline passes
 
 
 ## feature ideas
 
 * Support creating files for programming languages other than Python
+* Pop open code editor + support configurable editor command
 * Add commitizen for auto version updating
 * Support submitting responses to LeetCode via CLI as well
 * Whatever your imagination holds
```

### Comparing `localeet-0.0.2/.github/workflows/pr.yml` & `localeet-0.0.3/.github/workflows/pr.yml`

 * *Files 24% similar despite different names*

```diff
@@ -7,14 +7,17 @@
 
 jobs:
   test:
     name: Run Tests
     runs-on: ubuntu-latest
 
     steps:
+      - name: Set CI environment variable
+        run: echo "CI=true" >> $GITHUB_ENV
+
       - name: Checkout repository
         uses: actions/checkout@v2
 
       - name: Set up Python
         uses: actions/setup-python@v2
         with:
           python-version: 3.9
@@ -27,8 +30,8 @@
       - name: Run tests
         run: pytest tests -s -vvl
 
       - name: Install localeet dev dependencies
         run: pip install .[dev]
 
       - name: Run ruff
-        run: ruff src
+        run: ruff src tests
```

### Comparing `localeet-0.0.2/.github/workflows/pypi.yaml` & `localeet-0.0.3/.github/workflows/pypi.yaml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.2/src/localeet/__main__.py` & `localeet-0.0.3/src/localeet/__main__.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.2/src/localeet/get_leetcode_problem.py` & `localeet-0.0.3/src/localeet/get_leetcode_problem.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 """
 Module to get a random LeetCode question according to certain
 parameters and then output a local Python file to work on
 said question.
 """
 
-
 import random
 from pathlib import Path
 from typing import Literal
 
 import requests
 from bs4 import BeautifulSoup
 
+
 ROOT = 'https://leetcode.com'
 API_URL = f'{ROOT}/api/problems/all/'
 GQL_URL = f'{ROOT}/graphql'
 
 SLUG_KEY = 'question__title_slug'
 
 
@@ -139,14 +139,15 @@
     output_path.mkdir(parents=True, exist_ok=True)
     file_name = f'{title.lower().replace(" ", "_").replace("-", "_")}.py'
     output_path = output_path / file_name
     content = f'"""\n{qid} - {difficulty} - {title}\n\n{question}"""\n\n'
     content += """def main():\n    ..."""
     content += "\n\nif __name__ == '__main__':\n    main()\n"
     content += '\n'.join(['    # d' for d in test_case.split('\n')])
+    content += '\n'
     with output_path.open('w') as f:
         f.write(content)
     print(f'Created file for #{qid}: {title}')
 
 
 def run(
         max_difficulty: Literal[1, 2, 3],
@@ -158,8 +159,7 @@
         all_questions,
         max_difficulty,
         min_difficulty,
     )
     result = get_question_data(question_slug)
     question_details = parse_question_details(result)
     output_python_file(output_path, question_details)
-
```

### Comparing `localeet-0.0.2/tests/conftest.py` & `localeet-0.0.3/tests/conftest.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,34 +1,35 @@
 import json
 from pathlib import Path
+from typing import Any
 
 import pytest
 
 
 class MockValue:
     """Allows any of a datatype to pass comparison within dictionary"""
     def __init__(
             self,
-            name='MOCK_VALUE',
-            data_type=None,
-            validator=None,
+            name: str = 'MOCK_VALUE',
+            data_type: type = None,
+            validator: callable = None,
         ) -> None:
         self.name = name
         self.data_type = data_type
         self.validator = validator
 
-    def __eq__(self, item):
+    def __eq__(self, item: Any) -> bool:  # noqa: ANN401
         if (
             (self.data_type and not isinstance(item, self.data_type)) or
             (self.validator and not self.validator(item))
         ):
             return False
         return True
 
-    def __ne__(self, item):
+    def __ne__(self, item: Any) -> bool:  # noqa: ANN401
         return not self.__eq__(item)
 
     def __repr__(self) -> str:
         return f'<ANY_{self.name}>'
 
 
 @pytest.fixture(scope='session')
@@ -55,10 +56,10 @@
 @pytest.fixture(scope='session')
 def two_sum_essentials() -> dict:
     with Path('tests/data/two_sum_essentials.json').open() as f:
         return json.load(f)
 
 
 @pytest.fixture(scope='session')
-def sample_two_sum_python_file():
+def sample_two_sum_python_file() -> dict:
     with Path('tests/data/two_sum.py').open() as f:
         return f.read()
```

### Comparing `localeet-0.0.2/tests/get_leetcode_problem_test.py` & `localeet-0.0.3/tests/get_leetcode_problem_test.py`

 * *Files 7% similar despite different names*

```diff
@@ -5,18 +5,21 @@
     get_question_data,
     output_python_file,
     parse_question_details,
     query_all_questions,
 )
 
 
+NUMBER_OF_QUESTIONS_WHEN_WRITING = 2787
+
+
 def test_query_all_questions(any_int):
     """Test that query for question list works"""
     result = query_all_questions()
-    assert len(result) >= 2787  # assuming number never goes down..
+    assert len(result) >= NUMBER_OF_QUESTIONS_WHEN_WRITING
     assert result[-1] == {  # assuming order never changes...
         'difficulty': {'level': 1},
         'frequency': 0,
         'is_favor': False,
         'paid_only': False,
         'progress': 0,
         'stat': {
@@ -62,9 +65,11 @@
 
 def test_output_python_file(two_sum_essentials, sample_two_sum_python_file):
     path = Path('.')
     new_file = path / 'two_sum.py'
     output_python_file(path, two_sum_essentials)
     with new_file.open() as f:
         test_file = f.read()
-    assert test_file == sample_two_sum_python_file
-    new_file.unlink()
+    try:
+        assert test_file == sample_two_sum_python_file
+    finally:
+        new_file.unlink()
```

### Comparing `localeet-0.0.2/tests/data/two_sum.py` & `localeet-0.0.3/tests/data/two_sum.py`

 * *Ordering differences only*

 * *Files 1% similar despite different names*

```diff
@@ -34,8 +34,8 @@
 
 def main():
     ...
 
 if __name__ == '__main__':
     main()
     # d
-    # d
+    # d
```

### Comparing `localeet-0.0.2/tests/data/two_sum_details.json` & `localeet-0.0.3/tests/data/two_sum_details.json`

 * *Files identical despite different names*

### Comparing `localeet-0.0.2/tests/data/two_sum_essentials.json` & `localeet-0.0.3/tests/data/two_sum_essentials.json`

 * *Format-specific differences are supported for JSON files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: JSON text data*

 * *Files 0% similar despite different names*

```diff
@@ -51,8 +51,8 @@
 00000320: 7269 7468 6d20 7468 6174 2069 7320 6c65  rithm that is le
 00000330: 7373 2074 6861 6e5c 7530 3061 304f 286e  ss than\u00a0O(n
 00000340: 3229 5c75 3030 6130 7469 6d65 2063 6f6d  2)\u00a0time com
 00000350: 706c 6578 6974 793f 222c 0a20 2020 2022  plexity?",.    "
 00000360: 7465 7374 5f63 6173 6522 3a20 225b 322c  test_case": "[2,
 00000370: 372c 3131 2c31 355d 5c6e 3922 2c0a 2020  7,11,15]\n9",.  
 00000380: 2020 2274 6974 6c65 223a 2022 5477 6f20    "title": "Two 
-00000390: 5375 6d22 0a7d                           Sum".}
+00000390: 5375 6d22 0a7d 0a                        Sum".}.
```

### Comparing `localeet-0.0.2/.gitignore` & `localeet-0.0.3/.gitignore`

 * *Files identical despite different names*

### Comparing `localeet-0.0.2/LICENSE` & `localeet-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `localeet-0.0.2/pyproject.toml` & `localeet-0.0.3/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -87,13 +87,24 @@
     "W",  # https://beta.ruff.rs/docs/rules/#warning-w
     "UP",  # https://beta.ruff.rs/docs/rules/#pyupgrade-up
     "YTT",  # https://beta.ruff.rs/docs/rules/#flake8-2020-ytt
 ]
 ignore = [
   "S311",  # not using randomness for cryptography
   "S101",  # assert is awesome
+  "ANN101",  # self does not need a type annotation
+  "I001",  # I do not care for its sorting choices
+]
+exclude = [
+  "tests/data/*",
 ]
 show-fixes = true
 target-version = "py39"
 
 [tool.ruff.flake8-quotes]
 inline-quotes = "single"
+
+[tool.ruff.per-file-ignores]
+"tests/get_leetcode_problem_test.py" = [
+  "ANN001",  # no fixture annotations
+  "ANN201",  # no return annotatons for test functions
+]
```

### Comparing `localeet-0.0.2/PKG-INFO` & `localeet-0.0.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: localeet
-Version: 0.0.2
+Version: 0.0.3
 Summary: A CLI tool to do LeetCode and LeetCode-like exercises
 Author-email: Danny Brown <dannybrown37@gmail.com>
 License-File: LICENSE
 Requires-Dist: bs4
 Requires-Dist: click
 Requires-Dist: lxml
 Requires-Dist: requests
```

