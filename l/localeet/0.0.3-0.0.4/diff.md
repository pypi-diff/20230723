# Comparing `tmp/localeet-0.0.3.tar.gz` & `tmp/localeet-0.0.4.tar.gz`

## Comparing `localeet-0.0.3.tar` & `localeet-0.0.4.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0      944 2020-02-02 00:00:00.000000 localeet-0.0.3/.pre-commit-config.yaml
--rw-r--r--   0        0        0     1651 2020-02-02 00:00:00.000000 localeet-0.0.3/README.md
--rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 localeet-0.0.3/.github/workflows/pr.yml
--rw-r--r--   0        0        0      608 2020-02-02 00:00:00.000000 localeet-0.0.3/.github/workflows/pypi.yaml
--rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.3/src/localeet/__init__.py
--rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 localeet-0.0.3/src/localeet/__main__.py
--rw-r--r--   0        0        0     5715 2020-02-02 00:00:00.000000 localeet-0.0.3/src/localeet/get_leetcode_problem.py
--rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/conftest.py
--rw-r--r--   0        0        0     2153 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/get_leetcode_problem_test.py
--rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/version_number_test.py
--rw-r--r--   0        0        0      834 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/data/two_sum.py
--rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/data/two_sum_details.json
--rw-r--r--   0        0        0      919 2020-02-02 00:00:00.000000 localeet-0.0.3/tests/data/two_sum_essentials.json
--rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.3/.gitignore
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.3/LICENSE
--rw-r--r--   0        0        0     3828 2020-02-02 00:00:00.000000 localeet-0.0.3/pyproject.toml
--rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0      944 2020-02-02 00:00:00.000000 localeet-0.0.4/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     1866 2020-02-02 00:00:00.000000 localeet-0.0.4/README.md
+-rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 localeet-0.0.4/.github/workflows/pr.yml
+-rw-r--r--   0        0        0      608 2020-02-02 00:00:00.000000 localeet-0.0.4/.github/workflows/pypi.yaml
+-rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.4/src/localeet/__init__.py
+-rw-r--r--   0        0        0     1333 2020-02-02 00:00:00.000000 localeet-0.0.4/src/localeet/__main__.py
+-rw-r--r--   0        0        0     5943 2020-02-02 00:00:00.000000 localeet-0.0.4/src/localeet/get_leetcode_problem.py
+-rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/conftest.py
+-rw-r--r--   0        0        0     2206 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/get_leetcode_problem_test.py
+-rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/version_number_test.py
+-rw-r--r--   0        0        0      834 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/data/two_sum.py
+-rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/data/two_sum_details.json
+-rw-r--r--   0        0        0      919 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/data/two_sum_essentials.json
+-rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.4/.gitignore
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.4/LICENSE
+-rw-r--r--   0        0        0     3828 2020-02-02 00:00:00.000000 localeet-0.0.4/pyproject.toml
+-rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.4/PKG-INFO
```

### Comparing `localeet-0.0.3/.pre-commit-config.yaml` & `localeet-0.0.4/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/README.md` & `localeet-0.0.4/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -7,21 +7,19 @@
 ```
 pip install localeet
 ```
 
 
 # usage
 
-```
-localeet
-```
-
 This will find a random question from LeetCode's free question set.
 It will create a Python file shell with the question description and
-other metadata in it in your current working directory.
+other metadata in it in your current working directory. It will finally
+pop open a code editor (VSCode by default) with the new file opened in
+it.
 
 Using any of these CLI args will use the output path provided, and
 create any needed directories in that path as well.
 
 ```
 localeet --output_path ~/leetcode
 localeet --path problems
@@ -31,15 +29,24 @@
 You can set the max or min difficulty of the problem selected using a
 string or an int `{1: easy, 2: medium, 3: hard}`.
 
 ```
 localeet --max_difficulty medium
 localeet --max 1
 localeet --min_difficulty 3
-localeet --min HARD
+localeet --min hard
+```
+
+To specify a code editor other than VSCode, pass the CLI arg used to
+open said editor using one of these args:
+
+```
+localeet -e charm
+localeet --editor subl
+localeet --code_editor_open_command atom
 ```
 
 
 # contributions
 
 ## local setup
 
@@ -63,11 +70,10 @@
 7. Get approved & merged
 8. Ensure Publish to PyPI pipeline passes
 
 
 ## feature ideas
 
 * Support creating files for programming languages other than Python
-* Pop open code editor + support configurable editor command
 * Add commitizen for auto version updating
 * Support submitting responses to LeetCode via CLI as well
 * Whatever your imagination holds
```

### Comparing `localeet-0.0.3/.github/workflows/pr.yml` & `localeet-0.0.4/.github/workflows/pr.yml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/.github/workflows/pypi.yaml` & `localeet-0.0.4/.github/workflows/pypi.yaml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/src/localeet/get_leetcode_problem.py` & `localeet-0.0.4/src/localeet/get_leetcode_problem.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 """
 Module to get a random LeetCode question according to certain
 parameters and then output a local Python file to work on
 said question.
 """
 
 import random
+import subprocess
 from pathlib import Path
 from typing import Literal
 
 import requests
 from bs4 import BeautifulSoup
 
 
@@ -123,15 +124,15 @@
         'title': question_data['data']['question']['title'],
     }
 
 
 def output_python_file(
         output_path: Path,
         question_details: dict[str, str],
-    ) -> None:
+    ) -> str:
     """Take question details and output a python file shell"""
     difficulty, qid, question, test_case, title = (
         question_details['difficulty'],
         question_details['question_id'],
         question_details['question'],
         question_details['test_case'],
         question_details['title'],
@@ -142,24 +143,30 @@
     content = f'"""\n{qid} - {difficulty} - {title}\n\n{question}"""\n\n'
     content += """def main():\n    ..."""
     content += "\n\nif __name__ == '__main__':\n    main()\n"
     content += '\n'.join(['    # d' for d in test_case.split('\n')])
     content += '\n'
     with output_path.open('w') as f:
         f.write(content)
-    print(f'Created file for #{qid}: {title}')
+    return str(output_path)
+
+
+def open_code_editor(command: str, file_path: str) -> None:
+    subprocess.run([command, file_path])  # noqa: S603
 
 
 def run(
         max_difficulty: Literal[1, 2, 3],
         min_difficulty: Literal[1, 2, 3],
         output_path: Path,
+        code_editor_open_command: str,
     ) -> None:
     all_questions = query_all_questions()
     question_slug = choose_a_valid_question(
         all_questions,
         max_difficulty,
         min_difficulty,
     )
     result = get_question_data(question_slug)
     question_details = parse_question_details(result)
-    output_python_file(output_path, question_details)
+    output_path = output_python_file(output_path, question_details)
+    open_code_editor(code_editor_open_command, output_path)
```

### Comparing `localeet-0.0.3/tests/conftest.py` & `localeet-0.0.4/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/tests/get_leetcode_problem_test.py` & `localeet-0.0.4/tests/get_leetcode_problem_test.py`

 * *Files 2% similar despite different names*

```diff
@@ -62,14 +62,15 @@
 def test_parse_question_details(two_sum_details_json, two_sum_essentials):
     assert parse_question_details(two_sum_details_json) == two_sum_essentials
 
 
 def test_output_python_file(two_sum_essentials, sample_two_sum_python_file):
     path = Path('.')
     new_file = path / 'two_sum.py'
-    output_python_file(path, two_sum_essentials)
+    output_path = output_python_file(path, two_sum_essentials)
+    assert output_path == 'two_sum.py'
     with new_file.open() as f:
         test_file = f.read()
     try:
         assert test_file == sample_two_sum_python_file
     finally:
         new_file.unlink()
```

### Comparing `localeet-0.0.3/tests/version_number_test.py` & `localeet-0.0.4/tests/version_number_test.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/tests/data/two_sum.py` & `localeet-0.0.4/tests/data/two_sum.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/tests/data/two_sum_details.json` & `localeet-0.0.4/tests/data/two_sum_details.json`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/tests/data/two_sum_essentials.json` & `localeet-0.0.4/tests/data/two_sum_essentials.json`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/.gitignore` & `localeet-0.0.4/.gitignore`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/LICENSE` & `localeet-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/pyproject.toml` & `localeet-0.0.4/pyproject.toml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.3/PKG-INFO` & `localeet-0.0.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: localeet
-Version: 0.0.3
+Version: 0.0.4
 Summary: A CLI tool to do LeetCode and LeetCode-like exercises
 Author-email: Danny Brown <dannybrown37@gmail.com>
 License-File: LICENSE
 Requires-Dist: bs4
 Requires-Dist: click
 Requires-Dist: lxml
 Requires-Dist: requests
```

