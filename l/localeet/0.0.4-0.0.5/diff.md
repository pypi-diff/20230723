# Comparing `tmp/localeet-0.0.4.tar.gz` & `tmp/localeet-0.0.5.tar.gz`

## Comparing `localeet-0.0.4.tar` & `localeet-0.0.5.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0      944 2020-02-02 00:00:00.000000 localeet-0.0.4/.pre-commit-config.yaml
--rw-r--r--   0        0        0     1866 2020-02-02 00:00:00.000000 localeet-0.0.4/README.md
--rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 localeet-0.0.4/.github/workflows/pr.yml
--rw-r--r--   0        0        0      608 2020-02-02 00:00:00.000000 localeet-0.0.4/.github/workflows/pypi.yaml
--rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.4/src/localeet/__init__.py
--rw-r--r--   0        0        0     1333 2020-02-02 00:00:00.000000 localeet-0.0.4/src/localeet/__main__.py
--rw-r--r--   0        0        0     5943 2020-02-02 00:00:00.000000 localeet-0.0.4/src/localeet/get_leetcode_problem.py
--rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/conftest.py
--rw-r--r--   0        0        0     2206 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/get_leetcode_problem_test.py
--rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/version_number_test.py
--rw-r--r--   0        0        0      834 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/data/two_sum.py
--rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/data/two_sum_details.json
--rw-r--r--   0        0        0      919 2020-02-02 00:00:00.000000 localeet-0.0.4/tests/data/two_sum_essentials.json
--rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.4/.gitignore
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.4/LICENSE
--rw-r--r--   0        0        0     3828 2020-02-02 00:00:00.000000 localeet-0.0.4/pyproject.toml
--rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.4/PKG-INFO
+-rw-r--r--   0        0        0      944 2020-02-02 00:00:00.000000 localeet-0.0.5/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     1884 2020-02-02 00:00:00.000000 localeet-0.0.5/README.md
+-rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 localeet-0.0.5/.github/workflows/pr.yml
+-rw-r--r--   0        0        0      672 2020-02-02 00:00:00.000000 localeet-0.0.5/.github/workflows/pypi.yaml
+-rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.5/src/localeet/__init__.py
+-rw-r--r--   0        0        0     1333 2020-02-02 00:00:00.000000 localeet-0.0.5/src/localeet/__main__.py
+-rw-r--r--   0        0        0     5946 2020-02-02 00:00:00.000000 localeet-0.0.5/src/localeet/get_leetcode_problem.py
+-rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/conftest.py
+-rw-r--r--   0        0        0     2206 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/get_leetcode_problem_test.py
+-rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/version_number_test.py
+-rw-r--r--   0        0        0      844 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/data/two_sum.py
+-rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/data/two_sum_details.json
+-rw-r--r--   0        0        0      919 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/data/two_sum_essentials.json
+-rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.5/.gitignore
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.5/LICENSE
+-rw-r--r--   0        0        0     3828 2020-02-02 00:00:00.000000 localeet-0.0.5/pyproject.toml
+-rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.5/PKG-INFO
```

### Comparing `localeet-0.0.4/.pre-commit-config.yaml` & `localeet-0.0.5/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/README.md` & `localeet-0.0.5/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -7,14 +7,18 @@
 ```
 pip install localeet
 ```
 
 
 # usage
 
+```
+localeet
+```
+
 This will find a random question from LeetCode's free question set.
 It will create a Python file shell with the question description and
 other metadata in it in your current working directory. It will finally
 pop open a code editor (VSCode by default) with the new file opened in
 it.
 
 Using any of these CLI args will use the output path provided, and
```

### Comparing `localeet-0.0.4/.github/workflows/pr.yml` & `localeet-0.0.5/.github/workflows/pr.yml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/.github/workflows/pypi.yaml` & `localeet-0.0.5/.github/workflows/pypi.yaml`

 * *Files 8% similar despite different names*

```diff
@@ -22,7 +22,9 @@
     - name: Build distribution
       run: hatchling build
     - name: Publish to PyPI
       env:
         TWINE_USERNAME: __token__
         TWINE_PASSWORD: ${{ secrets.PYPI_API_TOKEN }}
       run: twine upload dist/*
+    - name: Confirm can install
+      run: pip install localeet
```

### Comparing `localeet-0.0.4/src/localeet/__main__.py` & `localeet-0.0.5/src/localeet/__main__.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/src/localeet/get_leetcode_problem.py` & `localeet-0.0.5/src/localeet/get_leetcode_problem.py`

 * *Files 2% similar despite different names*

```diff
@@ -137,17 +137,17 @@
         question_details['test_case'],
         question_details['title'],
     )
     output_path.mkdir(parents=True, exist_ok=True)
     file_name = f'{title.lower().replace(" ", "_").replace("-", "_")}.py'
     output_path = output_path / file_name
     content = f'"""\n{qid} - {difficulty} - {title}\n\n{question}"""\n\n'
-    content += """def main():\n    ..."""
-    content += "\n\nif __name__ == '__main__':\n    main()\n"
-    content += '\n'.join(['    # d' for d in test_case.split('\n')])
+    content += """def main():\n    ...\n\n"""
+    content += "if __name__ == '__main__':\n    main()\n"
+    content += '\n'.join([f'    # {d}' for d in test_case.split('\n')])
     content += '\n'
     with output_path.open('w') as f:
         f.write(content)
     return str(output_path)
 
 
 def open_code_editor(command: str, file_path: str) -> None:
```

### Comparing `localeet-0.0.4/tests/conftest.py` & `localeet-0.0.5/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/tests/get_leetcode_problem_test.py` & `localeet-0.0.5/tests/get_leetcode_problem_test.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/tests/version_number_test.py` & `localeet-0.0.5/tests/version_number_test.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/tests/data/two_sum.py` & `localeet-0.0.5/tests/data/two_sum.py`

 * *Files 4% similar despite different names*

```diff
@@ -33,9 +33,9 @@
 Follow-up: Can you come up with an algorithm that is less than O(n2) time complexity?"""
 
 def main():
     ...
 
 if __name__ == '__main__':
     main()
-    # d
-    # d
+    # [2,7,11,15]
+    # 9
```

### Comparing `localeet-0.0.4/tests/data/two_sum_details.json` & `localeet-0.0.5/tests/data/two_sum_details.json`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/tests/data/two_sum_essentials.json` & `localeet-0.0.5/tests/data/two_sum_essentials.json`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/.gitignore` & `localeet-0.0.5/.gitignore`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/LICENSE` & `localeet-0.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/pyproject.toml` & `localeet-0.0.5/pyproject.toml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.4/PKG-INFO` & `localeet-0.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: localeet
-Version: 0.0.4
+Version: 0.0.5
 Summary: A CLI tool to do LeetCode and LeetCode-like exercises
 Author-email: Danny Brown <dannybrown37@gmail.com>
 License-File: LICENSE
 Requires-Dist: bs4
 Requires-Dist: click
 Requires-Dist: lxml
 Requires-Dist: requests
```

