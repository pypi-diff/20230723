# Comparing `tmp/localeet-0.0.5.tar.gz` & `tmp/localeet-0.1.0.tar.gz`

## Comparing `localeet-0.0.5.tar` & `localeet-0.1.0.tar`

### file list

```diff
@@ -1,17 +1,20 @@
--rw-r--r--   0        0        0      944 2020-02-02 00:00:00.000000 localeet-0.0.5/.pre-commit-config.yaml
--rw-r--r--   0        0        0     1884 2020-02-02 00:00:00.000000 localeet-0.0.5/README.md
--rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 localeet-0.0.5/.github/workflows/pr.yml
--rw-r--r--   0        0        0      672 2020-02-02 00:00:00.000000 localeet-0.0.5/.github/workflows/pypi.yaml
--rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.0.5/src/localeet/__init__.py
--rw-r--r--   0        0        0     1333 2020-02-02 00:00:00.000000 localeet-0.0.5/src/localeet/__main__.py
--rw-r--r--   0        0        0     5946 2020-02-02 00:00:00.000000 localeet-0.0.5/src/localeet/get_leetcode_problem.py
--rw-r--r--   0        0        0     1650 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/conftest.py
--rw-r--r--   0        0        0     2206 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/get_leetcode_problem_test.py
--rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/version_number_test.py
--rw-r--r--   0        0        0      844 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/data/two_sum.py
--rw-r--r--   0        0        0    20243 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/data/two_sum_details.json
--rw-r--r--   0        0        0      919 2020-02-02 00:00:00.000000 localeet-0.0.5/tests/data/two_sum_essentials.json
--rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.0.5/.gitignore
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.0.5/LICENSE
--rw-r--r--   0        0        0     3828 2020-02-02 00:00:00.000000 localeet-0.0.5/pyproject.toml
--rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.0.5/PKG-INFO
+-rw-r--r--   0        0        0      943 2020-02-02 00:00:00.000000 localeet-0.1.0/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     2255 2020-02-02 00:00:00.000000 localeet-0.1.0/README.md
+-rw-r--r--   0        0        0      735 2020-02-02 00:00:00.000000 localeet-0.1.0/.github/workflows/pr.yml
+-rw-r--r--   0        0        0      672 2020-02-02 00:00:00.000000 localeet-0.1.0/.github/workflows/pypi.yaml
+-rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 localeet-0.1.0/src/localeet/__init__.py
+-rw-r--r--   0        0        0     2052 2020-02-02 00:00:00.000000 localeet-0.1.0/src/localeet/__main__.py
+-rw-r--r--   0        0        0     6587 2020-02-02 00:00:00.000000 localeet-0.1.0/src/localeet/get_leetcode_problem.py
+-rw-r--r--   0        0        0     3740 2020-02-02 00:00:00.000000 localeet-0.1.0/src/localeet/language_maps.py
+-rw-r--r--   0        0        0     1497 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/conftest.py
+-rw-r--r--   0        0        0     2515 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/get_leetcode_problem_test.py
+-rw-r--r--   0        0        0     1361 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/version_number_test.py
+-rw-r--r--   0        0        0      851 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum.go
+-rw-r--r--   0        0        0      974 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum.py
+-rw-r--r--   0        0        0      895 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum.rs
+-rw-r--r--   0        0        0    20244 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum_details.json
+-rw-r--r--   0        0        0     5902 2020-02-02 00:00:00.000000 localeet-0.1.0/tests/data/two_sum_essentials.json
+-rw-r--r--   0        0        0     2745 2020-02-02 00:00:00.000000 localeet-0.1.0/.gitignore
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 localeet-0.1.0/LICENSE
+-rw-r--r--   0        0        0     3828 2020-02-02 00:00:00.000000 localeet-0.1.0/pyproject.toml
+-rw-r--r--   0        0        0      586 2020-02-02 00:00:00.000000 localeet-0.1.0/PKG-INFO
```

### Comparing `localeet-0.0.5/.pre-commit-config.yaml` & `localeet-0.1.0/.pre-commit-config.yaml`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,7 @@
-
 repos:
   - repo: https://github.com/pre-commit/pre-commit-hooks
     rev: v4.1.0
     hooks:
       - id: trailing-whitespace
       - id: check-added-large-files
       - id: check-ast
```

### Comparing `localeet-0.0.5/README.md` & `localeet-0.1.0/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -12,18 +12,18 @@
 # usage
 
 ```
 localeet
 ```
 
 This will find a random question from LeetCode's free question set.
-It will create a Python file shell with the question description and
-other metadata in it in your current working directory. It will finally
-pop open a code editor (VSCode by default) with the new file opened in
-it.
+It will create a code file shell (Python by default) with the question
+description and other metadata in it in your current working directory.
+It will then pop open a code editor (VSCode by default) with the new
+file opened in it.
 
 Using any of these CLI args will use the output path provided, and
 create any needed directories in that path as well.
 
 ```
 localeet --output_path ~/leetcode
 localeet --path problems
@@ -45,14 +45,57 @@
 
 ```
 localeet -e charm
 localeet --editor subl
 localeet --code_editor_open_command atom
 ```
 
+To specify a language other than Python, use one of the following CLI
+arg formats:
+
+```
+localeet --programming_language rust
+localeet --language go
+localeet -l ts
+```
+
+Valid language options:
+```
+c++
+cpp
+java
+python
+python3
+py
+c
+c#
+cs
+javascript
+js
+ruby
+rb
+swift
+go
+golang
+scala
+kotlin
+kt
+rust
+rs
+php
+typescript
+ts
+racket
+rkt
+erlang
+erl
+elixir
+ex
+dart
+```
 
 # contributions
 
 ## local setup
 
 ```
     git clone https://github.com/dannybrown37/localeet.git
```

### Comparing `localeet-0.0.5/.github/workflows/pr.yml` & `localeet-0.1.0/.github/workflows/pr.yml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.5/.github/workflows/pypi.yaml` & `localeet-0.1.0/.github/workflows/pypi.yaml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.5/src/localeet/__main__.py` & `localeet-0.1.0/src/localeet/__main__.py`

 * *Files 23% similar despite different names*

```diff
@@ -2,25 +2,28 @@
 Entry point for CLI. Define and parse CLI arguments.
 """
 from pathlib import Path
 
 import click
 
 from localeet.get_leetcode_problem import run
+from localeet.language_maps import LANGUAGE_TO_EXTENSION
 
 
 DIFFICULTY_MAP = {
     'easy': 1,
     'medium': 2,
     'hard': 3,
     '1': 1,
     '2': 2,
     '3': 3,
 }
 
+SUPPORTED_LANGUAGES = list(LANGUAGE_TO_EXTENSION.keys())
+
 
 @click.command()
 @click.option(
     '--max_difficulty', '--max',
     help='Max difficulty allowed',
     type=click.Choice(list(DIFFICULTY_MAP.keys())),
 )
@@ -36,19 +39,43 @@
     default='.',
 )
 @click.option(
     '--code_editor_open_command', '--editor', '-e',
     help='Will open the specified editor on the created file. VSCode default.',
     default='code',
 )
+@click.option(
+    '--programming_language', '--language', '-l',
+    help='The programming language you want to use for your output file',
+    default='python3',
+
+)
 def main(
         max_difficulty: str,
         min_difficulty: str,
         output_path: str,
         code_editor_open_command: str,
+        programming_language: str,
     ) -> None:
     """Entry point for CLI. Parse CLI arguments."""
+
     max_difficulty = DIFFICULTY_MAP.get(max_difficulty, 3)
     min_difficulty = DIFFICULTY_MAP.get(min_difficulty, 1)
+
     output_path = Path(output_path)
 
-    run(max_difficulty, min_difficulty, output_path, code_editor_open_command)
+    language = programming_language.lower()
+    if SUPPORTED_LANGUAGES.index(language) is None:
+        msg = f'{programming_language} is not a supported languge'
+        raise ValueError(msg)
+    if language == 'python':
+        language = 'python3'  # python2 is dead, long live python3
+    elif language == 'go':
+        language = 'golang'
+
+    run(
+        max_difficulty,
+        min_difficulty,
+        output_path,
+        code_editor_open_command,
+        language,
+    )
```

### Comparing `localeet-0.0.5/src/localeet/get_leetcode_problem.py` & `localeet-0.1.0/src/localeet/get_leetcode_problem.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,21 +1,27 @@
 """
 Module to get a random LeetCode question according to certain
 parameters and then output a local Python file to work on
 said question.
 """
 
 import random
+import re
 import subprocess
 from pathlib import Path
 from typing import Literal
 
 import requests
 from bs4 import BeautifulSoup
 
+from localeet.language_maps import (
+    LANGUAGE_TO_COMMENT,
+    LANGUAGE_TO_EXTENSION,
+)
+
 
 ROOT = 'https://leetcode.com'
 API_URL = f'{ROOT}/api/problems/all/'
 GQL_URL = f'{ROOT}/graphql'
 
 SLUG_KEY = 'question__title_slug'
 
@@ -113,41 +119,49 @@
     }).json()
 
 
 def parse_question_details(question_data: dict) -> dict[str, str]:
     """Parse response from GraphQL down into data needed for output"""
     soup = BeautifulSoup(question_data['data']['question']['content'], 'lxml')
     return {
+        'code_snippets': question_data['data']['question']['codeSnippets'],
         'difficulty': question_data['data']['question']['difficulty'],
         'question_id': question_data['data']['question']['questionId'],
         'question': soup.get_text(),
         'test_case': question_data['data']['question']['sampleTestCase'],
         'title': question_data['data']['question']['title'],
     }
 
 
-def output_python_file(
+def output_code_file(
         output_path: Path,
         question_details: dict[str, str],
+        language: str,
     ) -> str:
     """Take question details and output a python file shell"""
-    difficulty, qid, question, test_case, title = (
+    difficulty, qid, question, snippets, test_case, title = (
         question_details['difficulty'],
         question_details['question_id'],
         question_details['question'],
+        question_details['code_snippets'],
         question_details['test_case'],
         question_details['title'],
     )
+    extension = LANGUAGE_TO_EXTENSION[language]
+    oc = LANGUAGE_TO_COMMENT[language]['open_block']
+    cc = LANGUAGE_TO_COMMENT[language]['close_block']
+    lc = LANGUAGE_TO_COMMENT[language]['line']
+    snippet = next(i for i in snippets if i['langSlug'] == language)['code']
     output_path.mkdir(parents=True, exist_ok=True)
-    file_name = f'{title.lower().replace(" ", "_").replace("-", "_")}.py'
+    regex = r'[-\s]+'  # replace spaces and hyphens with underscores
+    file_name = f'{re.sub(regex, "_", title.lower())}.{extension}'
     output_path = output_path / file_name
-    content = f'"""\n{qid} - {difficulty} - {title}\n\n{question}"""\n\n'
-    content += """def main():\n    ...\n\n"""
-    content += "if __name__ == '__main__':\n    main()\n"
-    content += '\n'.join([f'    # {d}' for d in test_case.split('\n')])
+    header = f'{oc}\n{qid} - {difficulty} - {title}\n\n{question}\n{cc}\n\n'
+    content = header + snippet + f'\n{lc} Example test case:\n'
+    content += '\n'.join([f'{lc} {d}' for d in test_case.split('\n')])
     content += '\n'
     with output_path.open('w') as f:
         f.write(content)
     return str(output_path)
 
 
 def open_code_editor(command: str, file_path: str) -> None:
@@ -155,18 +169,23 @@
 
 
 def run(
         max_difficulty: Literal[1, 2, 3],
         min_difficulty: Literal[1, 2, 3],
         output_path: Path,
         code_editor_open_command: str,
+        programming_language: str,
     ) -> None:
     all_questions = query_all_questions()
     question_slug = choose_a_valid_question(
         all_questions,
         max_difficulty,
         min_difficulty,
     )
     result = get_question_data(question_slug)
     question_details = parse_question_details(result)
-    output_path = output_python_file(output_path, question_details)
+    output_path = output_code_file(
+        output_path,
+        question_details,
+        programming_language,
+    )
     open_code_editor(code_editor_open_command, output_path)
```

### Comparing `localeet-0.0.5/tests/conftest.py` & `localeet-0.1.0/tests/conftest.py`

 * *Files 10% similar despite different names*

```diff
@@ -53,13 +53,7 @@
         return json.load(f)
 
 
 @pytest.fixture(scope='session')
 def two_sum_essentials() -> dict:
     with Path('tests/data/two_sum_essentials.json').open() as f:
         return json.load(f)
-
-
-@pytest.fixture(scope='session')
-def sample_two_sum_python_file() -> dict:
-    with Path('tests/data/two_sum.py').open() as f:
-        return f.read()
```

### Comparing `localeet-0.0.5/tests/get_leetcode_problem_test.py` & `localeet-0.1.0/tests/get_leetcode_problem_test.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,13 +1,15 @@
 from pathlib import Path
 
+import pytest
+
 from localeet.get_leetcode_problem import (
     choose_a_valid_question,
     get_question_data,
-    output_python_file,
+    output_code_file,
     parse_question_details,
     query_all_questions,
 )
 
 
 NUMBER_OF_QUESTIONS_WHEN_WRITING = 2787
 
@@ -59,18 +61,32 @@
     assert get_question_data('two-sum') == two_sum_details_json
 
 
 def test_parse_question_details(two_sum_details_json, two_sum_essentials):
     assert parse_question_details(two_sum_details_json) == two_sum_essentials
 
 
-def test_output_python_file(two_sum_essentials, sample_two_sum_python_file):
+@pytest.mark.parametrize(
+        ('language', 'extension'),
+        [
+            ('python', 'py'),
+            ('rust', 'rs'),
+            ('golang', 'go'),
+        ],
+)
+def test_output_python_file(
+        two_sum_essentials,
+        language,
+        extension,
+    ):
+    with Path(f'tests/data/two_sum.{extension}').open() as f:
+        expected = f.read()
     path = Path('.')
-    new_file = path / 'two_sum.py'
-    output_path = output_python_file(path, two_sum_essentials)
-    assert output_path == 'two_sum.py'
+    new_file = path / f'two_sum.{extension}'
+    output_path = output_code_file(path, two_sum_essentials, language)
+    assert output_path == f'two_sum.{extension}'
     with new_file.open() as f:
         test_file = f.read()
     try:
-        assert test_file == sample_two_sum_python_file
+        assert test_file == expected
     finally:
         new_file.unlink()
```

### Comparing `localeet-0.0.5/tests/version_number_test.py` & `localeet-0.1.0/tests/version_number_test.py`

 * *Files identical despite different names*

### Comparing `localeet-0.0.5/tests/data/two_sum.py` & `localeet-0.1.0/tests/data/two_sum.go`

 * *Files 26% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-"""
+/*
 1 - Easy - Two Sum
 
 Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
 You may assume that each input would have exactly one solution, and you may not use the same element twice.
 You can return the answer in any order.
  
 Example 1:
@@ -26,16 +26,16 @@
 
 2 <= nums.length <= 104
 -109 <= nums[i] <= 109
 -109 <= target <= 109
 Only one valid answer exists.
 
  
-Follow-up: Can you come up with an algorithm that is less than O(n2) time complexity?"""
+Follow-up: Can you come up with an algorithm that is less than O(n2) time complexity?
+*/
 
-def main():
-    ...
-
-if __name__ == '__main__':
-    main()
-    # [2,7,11,15]
-    # 9
+func twoSum(nums []int, target int) []int {
+    
+}
+// Example test case:
+// [2,7,11,15]
+// 9
```

### Comparing `localeet-0.0.5/tests/data/two_sum_details.json` & `localeet-0.1.0/tests/data/two_sum_details.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9848484848484849%*

 * *Differences: {"'data'": '{\'question\': {\'likes\': 49019, \'dislikes\': 1598, \'stats\': \'{"totalAccepted": '*

 * *           '"10.2M", "totalSubmission": "20.3M", "totalAcceptedRaw": 10221744, '*

 * *           '"totalSubmissionRaw": 20338203, "acRate": "50.3%"}\', \'judgeType\': \'small\'}}'}*

```diff
@@ -119,42 +119,42 @@
                     "langSlug": "dart"
                 }
             ],
             "companyTagStats": null,
             "content": "<p>Given an array of integers <code>nums</code>&nbsp;and an integer <code>target</code>, return <em>indices of the two numbers such that they add up to <code>target</code></em>.</p>\n\n<p>You may assume that each input would have <strong><em>exactly</em> one solution</strong>, and you may not use the <em>same</em> element twice.</p>\n\n<p>You can return the answer in any order.</p>\n\n<p>&nbsp;</p>\n<p><strong class=\"example\">Example 1:</strong></p>\n\n<pre>\n<strong>Input:</strong> nums = [2,7,11,15], target = 9\n<strong>Output:</strong> [0,1]\n<strong>Explanation:</strong> Because nums[0] + nums[1] == 9, we return [0, 1].\n</pre>\n\n<p><strong class=\"example\">Example 2:</strong></p>\n\n<pre>\n<strong>Input:</strong> nums = [3,2,4], target = 6\n<strong>Output:</strong> [1,2]\n</pre>\n\n<p><strong class=\"example\">Example 3:</strong></p>\n\n<pre>\n<strong>Input:</strong> nums = [3,3], target = 6\n<strong>Output:</strong> [0,1]\n</pre>\n\n<p>&nbsp;</p>\n<p><strong>Constraints:</strong></p>\n\n<ul>\n\t<li><code>2 &lt;= nums.length &lt;= 10<sup>4</sup></code></li>\n\t<li><code>-10<sup>9</sup> &lt;= nums[i] &lt;= 10<sup>9</sup></code></li>\n\t<li><code>-10<sup>9</sup> &lt;= target &lt;= 10<sup>9</sup></code></li>\n\t<li><strong>Only one valid answer exists.</strong></li>\n</ul>\n\n<p>&nbsp;</p>\n<strong>Follow-up:&nbsp;</strong>Can you come up with an algorithm that is less than&nbsp;<code>O(n<sup>2</sup>)&nbsp;</code>time complexity?",
             "contributors": [],
             "difficulty": "Easy",
-            "dislikes": 1596,
+            "dislikes": 1598,
             "enableRunCode": true,
             "enableTestMode": false,
             "envInfo": "{\"cpp\": [\"C++\", \"<p>Compiled with <code> clang 11 </code> using the latest C++ 17 standard.</p>\\r\\n\\r\\n<p>Your code is compiled with level two optimization (<code>-O2</code>). <a href=\\\"https://github.com/google/sanitizers/wiki/AddressSanitizer\\\" target=\\\"_blank\\\">AddressSanitizer</a> is also enabled to help detect out-of-bounds and use-after-free bugs.</p>\\r\\n\\r\\n<p>Most standard library headers are already included automatically for your convenience.</p>\"], \"java\": [\"Java\", \"<p><code>OpenJDK 17</code>. Java 8 features such as lambda expressions and stream API can be used. </p>\\r\\n\\r\\n<p>Most standard library headers are already included automatically for your convenience.</p>\\r\\n<p>Includes <code>Pair</code> class from https://docs.oracle.com/javase/8/javafx/api/javafx/util/Pair.html.</p>\"], \"python\": [\"Python\", \"<p><code>Python 2.7.12</code>.</p>\\r\\n\\r\\n<p>Most libraries are already imported automatically for your convenience, such as <a href=\\\"https://docs.python.org/2/library/array.html\\\" target=\\\"_blank\\\">array</a>, <a href=\\\"https://docs.python.org/2/library/bisect.html\\\" target=\\\"_blank\\\">bisect</a>, <a href=\\\"https://docs.python.org/2/library/collections.html\\\" target=\\\"_blank\\\">collections</a>. If you need more libraries, you can import it yourself.</p>\\r\\n\\r\\n<p>For Map/TreeMap data structure, you may use <a href=\\\"http://www.grantjenks.com/docs/sortedcontainers/\\\" target=\\\"_blank\\\">sortedcontainers</a> library.</p>\\r\\n\\r\\n<p>Note that Python 2.7 <a href=\\\"https://www.python.org/dev/peps/pep-0373/\\\" target=\\\"_blank\\\">will not be maintained past 2020</a>. For the latest Python, please choose Python3 instead.</p>\"], \"c\": [\"C\", \"<p>Compiled with <code>gcc 8.2</code> using the gnu11 standard.</p>\\r\\n\\r\\n<p>Your code is compiled with level one optimization (<code>-O1</code>). <a href=\\\"https://github.com/google/sanitizers/wiki/AddressSanitizer\\\" target=\\\"_blank\\\">AddressSanitizer</a> is also enabled to help detect out-of-bounds and use-after-free bugs.</p>\\r\\n\\r\\n<p>Most standard library headers are already included automatically for your convenience.</p>\\r\\n\\r\\n<p>For hash table operations, you may use <a href=\\\"https://troydhanson.github.io/uthash/\\\" target=\\\"_blank\\\">uthash</a>. \\\"uthash.h\\\" is included by default. Below are some examples:</p>\\r\\n\\r\\n<p><b>1. Adding an item to a hash.</b>\\r\\n<pre>\\r\\nstruct hash_entry {\\r\\n    int id;            /* we'll use this field as the key */\\r\\n    char name[10];\\r\\n    UT_hash_handle hh; /* makes this structure hashable */\\r\\n};\\r\\n\\r\\nstruct hash_entry *users = NULL;\\r\\n\\r\\nvoid add_user(struct hash_entry *s) {\\r\\n    HASH_ADD_INT(users, id, s);\\r\\n}\\r\\n</pre>\\r\\n</p>\\r\\n\\r\\n<p><b>2. Looking up an item in a hash:</b>\\r\\n<pre>\\r\\nstruct hash_entry *find_user(int user_id) {\\r\\n    struct hash_entry *s;\\r\\n    HASH_FIND_INT(users, &user_id, s);\\r\\n    return s;\\r\\n}\\r\\n</pre>\\r\\n</p>\\r\\n\\r\\n<p><b>3. Deleting an item in a hash:</b>\\r\\n<pre>\\r\\nvoid delete_user(struct hash_entry *user) {\\r\\n    HASH_DEL(users, user);  \\r\\n}\\r\\n</pre>\\r\\n</p>\"], \"csharp\": [\"C#\", \"<p><a href=\\\"https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10\\\" target=\\\"_blank\\\">C# 10 with .NET 6 runtime</a></p>\"], \"javascript\": [\"JavaScript\", \"<p><code>Node.js 16.13.2</code>.</p>\\r\\n\\r\\n<p>Your code is run with <code>--harmony</code> flag, enabling <a href=\\\"http://node.green/\\\" target=\\\"_blank\\\">new ES6 features</a>.</p>\\r\\n\\r\\n<p><a href=\\\"https://lodash.com\\\" target=\\\"_blank\\\">lodash.js</a> library is included by default.</p>\\r\\n\\r\\n<p>For Priority Queue / Queue data structures, you may use 5.3.0 version of <a href=\\\"https://github.com/datastructures-js/priority-queue/tree/fb4fdb984834421279aeb081df7af624d17c2a03\\\" target=\\\"_blank\\\">datastructures-js/priority-queue</a> and 4.2.1 version of <a href=\\\"https://github.com/datastructures-js/queue/tree/e63563025a5a805aa16928cb53bcd517bfea9230\\\" target=\\\"_blank\\\">datastructures-js/queue</a>.</p>\"], \"ruby\": [\"Ruby\", \"<p><code>Ruby 3.1</code></p>\\r\\n\\r\\n<p>Some common data structure implementations are provided in the Algorithms module: https://www.rubydoc.info/github/kanwei/algorithms/Algorithms</p>\"], \"swift\": [\"Swift\", \"<p><code>Swift 5.5.2</code>.</p>\"], \"golang\": [\"Go\", \"<p><code>Go 1.18</code></p>\\r\\n<p>Support <a href=\\\"https://github.com/emirpasic/gods/tree/v1.18.1\\\" target=\\\"_blank\\\">https://godoc.org/github.com/emirpasic/gods@v1.18.1</a> library.</p>\"], \"python3\": [\"Python3\", \"<p><code>Python 3.10</code>.</p>\\r\\n\\r\\n<p>Most libraries are already imported automatically for your convenience, such as <a href=\\\"https://docs.python.org/3/library/array.html\\\" target=\\\"_blank\\\">array</a>, <a href=\\\"https://docs.python.org/3/library/bisect.html\\\" target=\\\"_blank\\\">bisect</a>, <a href=\\\"https://docs.python.org/3/library/collections.html\\\" target=\\\"_blank\\\">collections</a>. If you need more libraries, you can import it yourself.</p>\\r\\n\\r\\n<p>For Map/TreeMap data structure, you may use <a href=\\\"http://www.grantjenks.com/docs/sortedcontainers/\\\" target=\\\"_blank\\\">sortedcontainers</a> library.</p>\"], \"scala\": [\"Scala\", \"<p><code>Scala 2.13.7</code>.</p>\"], \"kotlin\": [\"Kotlin\", \"<p><code>Kotlin 1.3.10</code>.</p>\"], \"rust\": [\"Rust\", \"<p><code>Rust 1.58.1</code></p>\\r\\n\\r\\n<p>Supports <a href=\\\"https://crates.io/crates/rand\\\" target=\\\"_blank\\\">rand </a> v0.6\\u00a0from crates.io</p>\"], \"php\": [\"PHP\", \"<p><code>PHP 8.1</code>.</p>\\r\\n<p>With bcmath module</p>\"], \"typescript\": [\"Typescript\", \"<p><code>TypeScript 5.1.6, Node.js 16.13.2</code>.</p>\\r\\n\\r\\n<p>Your code is run with <code>--harmony</code> flag, enabling <a href=\\\"http://node.green/\\\" target=\\\"_blank\\\">new ES2022 features</a>.</p>\\r\\n\\r\\n<p><a href=\\\"https://lodash.com\\\" target=\\\"_blank\\\">lodash.js</a> library is included by default.</p>\"], \"racket\": [\"Racket\", \"<p>Run with <code>Racket 8.3</code>.</p>\"], \"erlang\": [\"Erlang\", \"Erlang/OTP 25.0\"], \"elixir\": [\"Elixir\", \"Elixir 1.13.4 with Erlang/OTP 25.0\"], \"dart\": [\"Dart\", \"<p>Dart 2.17.3</p>\\r\\n\\r\\n<p>Your code will be run directly without compiling</p>\"]}",
             "hints": [
                 "A really brute force way would be to search for all possible pairs of numbers but that would be too slow. Again, it's best to try out brute force solutions for just for completeness. It is from these brute force solutions that you can come up with optimizations.",
                 "So, if we fix one of the numbers, say <code>x</code>, we have to scan the entire array to find the next number <code>y</code> which is <code>value - x</code> where value is the input parameter. Can we change our array somehow so that this search becomes faster?",
                 "The second train of thought is, without changing the array, can we use additional space somehow? Like maybe a hash map to speed up the search?"
             ],
             "isLiked": null,
             "isPaidOnly": false,
-            "judgeType": "large",
+            "judgeType": "small",
             "judgerAvailable": true,
             "langToValidPlayground": "{\"cpp\": true, \"java\": true, \"python\": true, \"python3\": true, \"mysql\": false, \"mssql\": false, \"oraclesql\": false, \"c\": false, \"csharp\": false, \"javascript\": false, \"ruby\": false, \"bash\": false, \"swift\": false, \"golang\": false, \"scala\": false, \"html\": false, \"pythonml\": false, \"kotlin\": false, \"rust\": false, \"php\": false, \"typescript\": false, \"racket\": false, \"erlang\": false, \"elixir\": false, \"dart\": false, \"pythondata\": false, \"react\": false}",
             "libraryUrl": null,
-            "likes": 48981,
+            "likes": 49019,
             "metaData": "{\n  \"name\": \"twoSum\",\n  \"params\": [\n    {\n      \"name\": \"nums\",\n      \"type\": \"integer[]\"\n    },\n    {\n      \"name\": \"target\",\n      \"type\": \"integer\"\n    }\n  ],\n  \"return\": {\n    \"type\": \"integer[]\",\n    \"size\": 2\n  },\n  \"manual\": false\n}",
             "mysqlSchemas": [],
             "questionFrontendId": "1",
             "questionId": "1",
             "sampleTestCase": "[2,7,11,15]\n9",
             "similarQuestions": "[{\"title\": \"3Sum\", \"titleSlug\": \"3sum\", \"difficulty\": \"Medium\", \"translatedTitle\": null}, {\"title\": \"4Sum\", \"titleSlug\": \"4sum\", \"difficulty\": \"Medium\", \"translatedTitle\": null}, {\"title\": \"Two Sum II - Input Array Is Sorted\", \"titleSlug\": \"two-sum-ii-input-array-is-sorted\", \"difficulty\": \"Medium\", \"translatedTitle\": null}, {\"title\": \"Two Sum III - Data structure design\", \"titleSlug\": \"two-sum-iii-data-structure-design\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"Subarray Sum Equals K\", \"titleSlug\": \"subarray-sum-equals-k\", \"difficulty\": \"Medium\", \"translatedTitle\": null}, {\"title\": \"Two Sum IV - Input is a BST\", \"titleSlug\": \"two-sum-iv-input-is-a-bst\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"Two Sum Less Than K\", \"titleSlug\": \"two-sum-less-than-k\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"Max Number of K-Sum Pairs\", \"titleSlug\": \"max-number-of-k-sum-pairs\", \"difficulty\": \"Medium\", \"translatedTitle\": null}, {\"title\": \"Count Good Meals\", \"titleSlug\": \"count-good-meals\", \"difficulty\": \"Medium\", \"translatedTitle\": null}, {\"title\": \"Count Number of Pairs With Absolute Difference K\", \"titleSlug\": \"count-number-of-pairs-with-absolute-difference-k\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"Number of Pairs of Strings With Concatenation Equal to Target\", \"titleSlug\": \"number-of-pairs-of-strings-with-concatenation-equal-to-target\", \"difficulty\": \"Medium\", \"translatedTitle\": null}, {\"title\": \"Find All K-Distant Indices in an Array\", \"titleSlug\": \"find-all-k-distant-indices-in-an-array\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"First Letter to Appear Twice\", \"titleSlug\": \"first-letter-to-appear-twice\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"Number of Excellent Pairs\", \"titleSlug\": \"number-of-excellent-pairs\", \"difficulty\": \"Hard\", \"translatedTitle\": null}, {\"title\": \"Number of Arithmetic Triplets\", \"titleSlug\": \"number-of-arithmetic-triplets\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"Node With Highest Edge Score\", \"titleSlug\": \"node-with-highest-edge-score\", \"difficulty\": \"Medium\", \"translatedTitle\": null}, {\"title\": \"Check Distances Between Same Letters\", \"titleSlug\": \"check-distances-between-same-letters\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"Find Subarrays With Equal Sum\", \"titleSlug\": \"find-subarrays-with-equal-sum\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"Largest Positive Integer That Exists With Its Negative\", \"titleSlug\": \"largest-positive-integer-that-exists-with-its-negative\", \"difficulty\": \"Easy\", \"translatedTitle\": null}, {\"title\": \"Number of Distinct Averages\", \"titleSlug\": \"number-of-distinct-averages\", \"difficulty\": \"Easy\", \"translatedTitle\": null}]",
             "solution": {
                 "__typename": "ArticleNode",
                 "canSeeDetail": true,
                 "id": "7"
             },
-            "stats": "{\"totalAccepted\": \"10.2M\", \"totalSubmission\": \"20.3M\", \"totalAcceptedRaw\": 10215794, \"totalSubmissionRaw\": 20327979, \"acRate\": \"50.3%\"}",
+            "stats": "{\"totalAccepted\": \"10.2M\", \"totalSubmission\": \"20.3M\", \"totalAcceptedRaw\": 10221744, \"totalSubmissionRaw\": 20338203, \"acRate\": \"50.3%\"}",
             "status": null,
             "title": "Two Sum",
             "titleSlug": "two-sum",
             "topicTags": [
                 {
                     "__typename": "TopicTagNode",
                     "name": "Array",
```

### Comparing `localeet-0.0.5/tests/data/two_sum_essentials.json` & `localeet-0.1.0/tests/data/two_sum.rs`

 * *Files 24% similar despite different names*

```diff
@@ -1,58 +1,56 @@
-00000000: 7b0a 2020 2020 2264 6966 6669 6375 6c74  {.    "difficult
-00000010: 7922 3a20 2245 6173 7922 2c0a 2020 2020  y": "Easy",.    
-00000020: 2271 7565 7374 696f 6e5f 6964 223a 2022  "question_id": "
-00000030: 3122 2c0a 2020 2020 2271 7565 7374 696f  1",.    "questio
-00000040: 6e22 3a20 2247 6976 656e 2061 6e20 6172  n": "Given an ar
-00000050: 7261 7920 6f66 2069 6e74 6567 6572 7320  ray of integers 
-00000060: 6e75 6d73 5c75 3030 6130 616e 6420 616e  nums\u00a0and an
-00000070: 2069 6e74 6567 6572 2074 6172 6765 742c   integer target,
-00000080: 2072 6574 7572 6e20 696e 6469 6365 7320   return indices 
-00000090: 6f66 2074 6865 2074 776f 206e 756d 6265  of the two numbe
-000000a0: 7273 2073 7563 6820 7468 6174 2074 6865  rs such that the
-000000b0: 7920 6164 6420 7570 2074 6f20 7461 7267  y add up to targ
-000000c0: 6574 2e5c 6e59 6f75 206d 6179 2061 7373  et.\nYou may ass
-000000d0: 756d 6520 7468 6174 2065 6163 6820 696e  ume that each in
-000000e0: 7075 7420 776f 756c 6420 6861 7665 2065  put would have e
-000000f0: 7861 6374 6c79 206f 6e65 2073 6f6c 7574  xactly one solut
-00000100: 696f 6e2c 2061 6e64 2079 6f75 206d 6179  ion, and you may
-00000110: 206e 6f74 2075 7365 2074 6865 2073 616d   not use the sam
-00000120: 6520 656c 656d 656e 7420 7477 6963 652e  e element twice.
-00000130: 5c6e 596f 7520 6361 6e20 7265 7475 726e  \nYou can return
-00000140: 2074 6865 2061 6e73 7765 7220 696e 2061   the answer in a
-00000150: 6e79 206f 7264 6572 2e5c 6e5c 7530 3061  ny order.\n\u00a
-00000160: 305c 6e45 7861 6d70 6c65 2031 3a5c 6e5c  0\nExample 1:\n\
-00000170: 6e49 6e70 7574 3a20 6e75 6d73 203d 205b  nInput: nums = [
-00000180: 322c 372c 3131 2c31 355d 2c20 7461 7267  2,7,11,15], targ
-00000190: 6574 203d 2039 5c6e 4f75 7470 7574 3a20  et = 9\nOutput: 
-000001a0: 5b30 2c31 5d5c 6e45 7870 6c61 6e61 7469  [0,1]\nExplanati
-000001b0: 6f6e 3a20 4265 6361 7573 6520 6e75 6d73  on: Because nums
-000001c0: 5b30 5d20 2b20 6e75 6d73 5b31 5d20 3d3d  [0] + nums[1] ==
-000001d0: 2039 2c20 7765 2072 6574 7572 6e20 5b30   9, we return [0
-000001e0: 2c20 315d 2e5c 6e5c 6e45 7861 6d70 6c65  , 1].\n\nExample
-000001f0: 2032 3a5c 6e5c 6e49 6e70 7574 3a20 6e75   2:\n\nInput: nu
-00000200: 6d73 203d 205b 332c 322c 345d 2c20 7461  ms = [3,2,4], ta
-00000210: 7267 6574 203d 2036 5c6e 4f75 7470 7574  rget = 6\nOutput
-00000220: 3a20 5b31 2c32 5d5c 6e5c 6e45 7861 6d70  : [1,2]\n\nExamp
-00000230: 6c65 2033 3a5c 6e5c 6e49 6e70 7574 3a20  le 3:\n\nInput: 
-00000240: 6e75 6d73 203d 205b 332c 335d 2c20 7461  nums = [3,3], ta
-00000250: 7267 6574 203d 2036 5c6e 4f75 7470 7574  rget = 6\nOutput
-00000260: 3a20 5b30 2c31 5d5c 6e5c 6e5c 7530 3061  : [0,1]\n\n\u00a
-00000270: 305c 6e43 6f6e 7374 7261 696e 7473 3a5c  0\nConstraints:\
-00000280: 6e5c 6e32 203c 3d20 6e75 6d73 2e6c 656e  n\n2 <= nums.len
-00000290: 6774 6820 3c3d 2031 3034 5c6e 2d31 3039  gth <= 104\n-109
-000002a0: 203c 3d20 6e75 6d73 5b69 5d20 3c3d 2031   <= nums[i] <= 1
-000002b0: 3039 5c6e 2d31 3039 203c 3d20 7461 7267  09\n-109 <= targ
-000002c0: 6574 203c 3d20 3130 395c 6e4f 6e6c 7920  et <= 109\nOnly 
-000002d0: 6f6e 6520 7661 6c69 6420 616e 7377 6572  one valid answer
-000002e0: 2065 7869 7374 732e 5c6e 5c6e 5c75 3030   exists.\n\n\u00
-000002f0: 6130 5c6e 466f 6c6c 6f77 2d75 703a 5c75  a0\nFollow-up:\u
-00000300: 3030 6130 4361 6e20 796f 7520 636f 6d65  00a0Can you come
-00000310: 2075 7020 7769 7468 2061 6e20 616c 676f   up with an algo
-00000320: 7269 7468 6d20 7468 6174 2069 7320 6c65  rithm that is le
-00000330: 7373 2074 6861 6e5c 7530 3061 304f 286e  ss than\u00a0O(n
-00000340: 3229 5c75 3030 6130 7469 6d65 2063 6f6d  2)\u00a0time com
-00000350: 706c 6578 6974 793f 222c 0a20 2020 2022  plexity?",.    "
-00000360: 7465 7374 5f63 6173 6522 3a20 225b 322c  test_case": "[2,
-00000370: 372c 3131 2c31 355d 5c6e 3922 2c0a 2020  7,11,15]\n9",.  
-00000380: 2020 2274 6974 6c65 223a 2022 5477 6f20    "title": "Two 
-00000390: 5375 6d22 0a7d 0a                        Sum".}.
+00000000: 2f2a 0a31 202d 2045 6173 7920 2d20 5477  /*.1 - Easy - Tw
+00000010: 6f20 5375 6d0a 0a47 6976 656e 2061 6e20  o Sum..Given an 
+00000020: 6172 7261 7920 6f66 2069 6e74 6567 6572  array of integer
+00000030: 7320 6e75 6d73 c2a0 616e 6420 616e 2069  s nums..and an i
+00000040: 6e74 6567 6572 2074 6172 6765 742c 2072  nteger target, r
+00000050: 6574 7572 6e20 696e 6469 6365 7320 6f66  eturn indices of
+00000060: 2074 6865 2074 776f 206e 756d 6265 7273   the two numbers
+00000070: 2073 7563 6820 7468 6174 2074 6865 7920   such that they 
+00000080: 6164 6420 7570 2074 6f20 7461 7267 6574  add up to target
+00000090: 2e0a 596f 7520 6d61 7920 6173 7375 6d65  ..You may assume
+000000a0: 2074 6861 7420 6561 6368 2069 6e70 7574   that each input
+000000b0: 2077 6f75 6c64 2068 6176 6520 6578 6163   would have exac
+000000c0: 746c 7920 6f6e 6520 736f 6c75 7469 6f6e  tly one solution
+000000d0: 2c20 616e 6420 796f 7520 6d61 7920 6e6f  , and you may no
+000000e0: 7420 7573 6520 7468 6520 7361 6d65 2065  t use the same e
+000000f0: 6c65 6d65 6e74 2074 7769 6365 2e0a 596f  lement twice..Yo
+00000100: 7520 6361 6e20 7265 7475 726e 2074 6865  u can return the
+00000110: 2061 6e73 7765 7220 696e 2061 6e79 206f   answer in any o
+00000120: 7264 6572 2e0a c2a0 0a45 7861 6d70 6c65  rder.....Example
+00000130: 2031 3a0a 0a49 6e70 7574 3a20 6e75 6d73   1:..Input: nums
+00000140: 203d 205b 322c 372c 3131 2c31 355d 2c20   = [2,7,11,15], 
+00000150: 7461 7267 6574 203d 2039 0a4f 7574 7075  target = 9.Outpu
+00000160: 743a 205b 302c 315d 0a45 7870 6c61 6e61  t: [0,1].Explana
+00000170: 7469 6f6e 3a20 4265 6361 7573 6520 6e75  tion: Because nu
+00000180: 6d73 5b30 5d20 2b20 6e75 6d73 5b31 5d20  ms[0] + nums[1] 
+00000190: 3d3d 2039 2c20 7765 2072 6574 7572 6e20  == 9, we return 
+000001a0: 5b30 2c20 315d 2e0a 0a45 7861 6d70 6c65  [0, 1]...Example
+000001b0: 2032 3a0a 0a49 6e70 7574 3a20 6e75 6d73   2:..Input: nums
+000001c0: 203d 205b 332c 322c 345d 2c20 7461 7267   = [3,2,4], targ
+000001d0: 6574 203d 2036 0a4f 7574 7075 743a 205b  et = 6.Output: [
+000001e0: 312c 325d 0a0a 4578 616d 706c 6520 333a  1,2]..Example 3:
+000001f0: 0a0a 496e 7075 743a 206e 756d 7320 3d20  ..Input: nums = 
+00000200: 5b33 2c33 5d2c 2074 6172 6765 7420 3d20  [3,3], target = 
+00000210: 360a 4f75 7470 7574 3a20 5b30 2c31 5d0a  6.Output: [0,1].
+00000220: 0ac2 a00a 436f 6e73 7472 6169 6e74 733a  ....Constraints:
+00000230: 0a0a 3220 3c3d 206e 756d 732e 6c65 6e67  ..2 <= nums.leng
+00000240: 7468 203c 3d20 3130 340a 2d31 3039 203c  th <= 104.-109 <
+00000250: 3d20 6e75 6d73 5b69 5d20 3c3d 2031 3039  = nums[i] <= 109
+00000260: 0a2d 3130 3920 3c3d 2074 6172 6765 7420  .-109 <= target 
+00000270: 3c3d 2031 3039 0a4f 6e6c 7920 6f6e 6520  <= 109.Only one 
+00000280: 7661 6c69 6420 616e 7377 6572 2065 7869  valid answer exi
+00000290: 7374 732e 0a0a c2a0 0a46 6f6c 6c6f 772d  sts......Follow-
+000002a0: 7570 3ac2 a043 616e 2079 6f75 2063 6f6d  up:..Can you com
+000002b0: 6520 7570 2077 6974 6820 616e 2061 6c67  e up with an alg
+000002c0: 6f72 6974 686d 2074 6861 7420 6973 206c  orithm that is l
+000002d0: 6573 7320 7468 616e c2a0 4f28 6e32 29c2  ess than..O(n2).
+000002e0: a074 696d 6520 636f 6d70 6c65 7869 7479  .time complexity
+000002f0: 3f0a 2a2f 0a0a 696d 706c 2053 6f6c 7574  ?.*/..impl Solut
+00000300: 696f 6e20 7b0a 2020 2020 7075 6220 666e  ion {.    pub fn
+00000310: 2074 776f 5f73 756d 286e 756d 733a 2056   two_sum(nums: V
+00000320: 6563 3c69 3332 3e2c 2074 6172 6765 743a  ec<i32>, target:
+00000330: 2069 3332 2920 2d3e 2056 6563 3c69 3332   i32) -> Vec<i32
+00000340: 3e20 7b0a 2020 2020 2020 2020 0a20 2020  > {.        .   
+00000350: 207d 0a7d 0a2f 2f20 4578 616d 706c 6520   }.}.// Example 
+00000360: 7465 7374 2063 6173 653a 0a2f 2f20 5b32  test case:.// [2
+00000370: 2c37 2c31 312c 3135 5d0a 2f2f 2039 0a    ,7,11,15].// 9.
```

### Comparing `localeet-0.0.5/.gitignore` & `localeet-0.1.0/.gitignore`

 * *Files identical despite different names*

### Comparing `localeet-0.0.5/LICENSE` & `localeet-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `localeet-0.0.5/pyproject.toml` & `localeet-0.1.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `localeet-0.0.5/PKG-INFO` & `localeet-0.1.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: localeet
-Version: 0.0.5
+Version: 0.1.0
 Summary: A CLI tool to do LeetCode and LeetCode-like exercises
 Author-email: Danny Brown <dannybrown37@gmail.com>
 License-File: LICENSE
 Requires-Dist: bs4
 Requires-Dist: click
 Requires-Dist: lxml
 Requires-Dist: requests
```

