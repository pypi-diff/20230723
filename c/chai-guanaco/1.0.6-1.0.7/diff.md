# Comparing `tmp/chai-guanaco-1.0.6.tar.gz` & `tmp/chai-guanaco-1.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/chai-guanaco-1.0.6.tar", last modified: Mon Jul 17 01:53:51 2023, max compression
+gzip compressed data, was "dist/chai-guanaco-1.0.7.tar", last modified: Sun Jul 23 20:10:57 2023, max compression
```

## Comparing `chai-guanaco-1.0.6.tar` & `chai-guanaco-1.0.7.tar`

### file list

```diff
@@ -1,49 +1,49 @@
-drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/
--rw-rw-r--   0 tom       (1002) tom       (1002)       47 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/MANIFEST.in
--rw-rw-r--   0 tom       (1002) tom       (1002)    11015 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/PKG-INFO
--rw-rw-r--   0 tom       (1002) tom       (1002)     9305 2023-07-16 03:02:29.000000 chai-guanaco-1.0.6/README.md
--rw-rw-r--   0 tom       (1002) tom       (1002)       46 2023-07-15 23:09:11.000000 chai-guanaco-1.0.6/requirements.txt
--rw-rw-r--   0 tom       (1002) tom       (1002)       38 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/setup.cfg
--rw-rw-r--   0 tom       (1002) tom       (1002)      988 2023-07-17 01:53:46.000000 chai-guanaco-1.0.6/setup.py
-drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/
-drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco/
--rw-rw-r--   0 tom       (1002) tom       (1002)      270 2023-07-15 23:09:11.000000 chai-guanaco-1.0.6/src/chai_guanaco/__init__.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     4841 2023-07-17 01:52:36.000000 chai-guanaco-1.0.6/src/chai_guanaco/chat.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     3259 2023-07-16 03:02:29.000000 chai-guanaco-1.0.6/src/chai_guanaco/feedback.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     1756 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/formatters.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     1966 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/login_cli.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     6109 2023-07-17 01:52:36.000000 chai-guanaco-1.0.6/src/chai_guanaco/metrics.py
-drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/
-drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/
--rw-rw-r--   0 tom       (1002) tom       (1002)     1332 2023-07-15 21:49:57.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/blade.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     1529 2023-07-15 21:49:57.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/captain_wyatt.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     2031 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/coffee_shop_girl.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     1305 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/filbert.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     1050 2023-07-15 21:49:57.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/leo.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     1053 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/levi.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     1821 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/mr_wilson.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     1094 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/nerd_girl.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     2205 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/scaramouche.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     1386 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/story_teller.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     2510 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/vampire_queen.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     2246 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/wednesday_addams.json
--rw-rw-r--   0 tom       (1002) tom       (1002)     5426 2023-07-15 23:09:11.000000 chai-guanaco-1.0.6/src/chai_guanaco/submit.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     1894 2023-07-16 03:02:29.000000 chai-guanaco-1.0.6/src/chai_guanaco/utils.py
-drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco.egg-info/
--rw-rw-r--   0 tom       (1002) tom       (1002)    11015 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco.egg-info/PKG-INFO
--rw-rw-r--   0 tom       (1002) tom       (1002)     1430 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco.egg-info/SOURCES.txt
--rw-rw-r--   0 tom       (1002) tom       (1002)        1 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco.egg-info/dependency_links.txt
--rw-rw-r--   0 tom       (1002) tom       (1002)       61 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco.egg-info/entry_points.txt
--rw-rw-r--   0 tom       (1002) tom       (1002)        1 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco.egg-info/not-zip-safe
--rw-rw-r--   0 tom       (1002) tom       (1002)       46 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco.egg-info/requires.txt
--rw-rw-r--   0 tom       (1002) tom       (1002)       13 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/src/chai_guanaco.egg-info/top_level.txt
-drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/tests/
-drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-17 01:53:51.000000 chai-guanaco-1.0.6/tests/resources/
--rw-rw-r--   0 tom       (1002) tom       (1002) 10541478 2023-07-15 23:09:11.000000 chai-guanaco-1.0.6/tests/resources/test_get_leaderboard.yaml
--rw-rw-r--   0 tom       (1002) tom       (1002)  9300316 2023-07-15 23:09:11.000000 chai-guanaco-1.0.6/tests/resources/test_get_submission_metrics.yaml
--rw-rw-r--   0 tom       (1002) tom       (1002)     3537 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/tests/test_chat.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     3454 2023-06-27 20:36:12.000000 chai-guanaco-1.0.6/tests/test_feedback.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     1629 2023-07-16 03:02:29.000000 chai-guanaco-1.0.6/tests/test_guanaco_python_utils.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     2842 2023-07-13 18:06:47.000000 chai-guanaco-1.0.6/tests/test_login.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     3884 2023-07-17 01:52:36.000000 chai-guanaco-1.0.6/tests/test_metrics.py
--rw-rw-r--   0 tom       (1002) tom       (1002)     5607 2023-07-16 02:17:04.000000 chai-guanaco-1.0.6/tests/test_submit.py
+drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/
+-rw-rw-r--   0 tom       (1002) tom       (1002)       47 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/MANIFEST.in
+-rw-rw-r--   0 tom       (1002) tom       (1002)    11015 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/PKG-INFO
+-rw-rw-r--   0 tom       (1002) tom       (1002)     9305 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/README.md
+-rw-rw-r--   0 tom       (1002) tom       (1002)       46 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/requirements.txt
+-rw-rw-r--   0 tom       (1002) tom       (1002)       38 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/setup.cfg
+-rw-rw-r--   0 tom       (1002) tom       (1002)      988 2023-07-23 20:10:50.000000 chai-guanaco-1.0.7/setup.py
+drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/src/
+drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/src/chai_guanaco/
+-rw-rw-r--   0 tom       (1002) tom       (1002)      270 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/__init__.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     4841 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/chat.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     3259 2023-07-23 20:07:04.000000 chai-guanaco-1.0.7/src/chai_guanaco/feedback.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1756 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/formatters.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1966 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/login_cli.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     6220 2023-07-23 19:56:10.000000 chai-guanaco-1.0.7/src/chai_guanaco/metrics.py
+drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/
+drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1332 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/blade.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1529 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/captain_wyatt.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     2031 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/coffee_shop_girl.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1305 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/filbert.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1050 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/leo.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1053 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/levi.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1821 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/mr_wilson.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1094 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/nerd_girl.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     2205 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/scaramouche.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1386 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/story_teller.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     2510 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/vampire_queen.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     2246 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/wednesday_addams.json
+-rw-rw-r--   0 tom       (1002) tom       (1002)     5426 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/src/chai_guanaco/submit.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1945 2023-07-23 20:07:04.000000 chai-guanaco-1.0.7/src/chai_guanaco/utils.py
+drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/src/chai_guanaco.egg-info/
+-rw-rw-r--   0 tom       (1002) tom       (1002)    11015 2023-07-23 20:10:56.000000 chai-guanaco-1.0.7/src/chai_guanaco.egg-info/PKG-INFO
+-rw-rw-r--   0 tom       (1002) tom       (1002)     1430 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/src/chai_guanaco.egg-info/SOURCES.txt
+-rw-rw-r--   0 tom       (1002) tom       (1002)        1 2023-07-23 20:10:56.000000 chai-guanaco-1.0.7/src/chai_guanaco.egg-info/dependency_links.txt
+-rw-rw-r--   0 tom       (1002) tom       (1002)       61 2023-07-23 20:10:56.000000 chai-guanaco-1.0.7/src/chai_guanaco.egg-info/entry_points.txt
+-rw-rw-r--   0 tom       (1002) tom       (1002)        1 2023-07-23 20:10:56.000000 chai-guanaco-1.0.7/src/chai_guanaco.egg-info/not-zip-safe
+-rw-rw-r--   0 tom       (1002) tom       (1002)       46 2023-07-23 20:10:56.000000 chai-guanaco-1.0.7/src/chai_guanaco.egg-info/requires.txt
+-rw-rw-r--   0 tom       (1002) tom       (1002)       13 2023-07-23 20:10:56.000000 chai-guanaco-1.0.7/src/chai_guanaco.egg-info/top_level.txt
+drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/tests/
+drwxrwxr-x   0 tom       (1002) tom       (1002)        0 2023-07-23 20:10:57.000000 chai-guanaco-1.0.7/tests/resources/
+-rw-rw-r--   0 tom       (1002) tom       (1002) 10541478 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/tests/resources/test_get_leaderboard.yaml
+-rw-rw-r--   0 tom       (1002) tom       (1002)  9300316 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/tests/resources/test_get_submission_metrics.yaml
+-rw-rw-r--   0 tom       (1002) tom       (1002)     3537 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/tests/test_chat.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     3454 2023-07-23 20:07:04.000000 chai-guanaco-1.0.7/tests/test_feedback.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     2062 2023-07-23 16:39:07.000000 chai-guanaco-1.0.7/tests/test_guanaco_python_utils.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     2842 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/tests/test_login.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     3943 2023-07-23 16:39:07.000000 chai-guanaco-1.0.7/tests/test_metrics.py
+-rw-rw-r--   0 tom       (1002) tom       (1002)     5607 2023-07-23 16:39:02.000000 chai-guanaco-1.0.7/tests/test_submit.py
```

### Comparing `chai-guanaco-1.0.6/PKG-INFO` & `chai-guanaco-1.0.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chai-guanaco
-Version: 1.0.6
+Version: 1.0.7
 Summary: Chai Guanaco
 Home-page: https://www.chai-research.com
 Author: Chai Research Corp.
 Author-email: hello@chai-research.com
 License: MIT
 Description: [![Guanaco Banner](https://imgur.com/wJHIeAU.png)](https://www.chai-research.com/competition.html)
```

### Comparing `chai-guanaco-1.0.6/README.md` & `chai-guanaco-1.0.7/README.md`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/setup.py` & `chai-guanaco-1.0.7/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 
 with open('requirements.txt') as f:
     requirements = f.read().splitlines()
 
 if os.environ.get('CI_COMMIT_TAG', None):
     version = os.environ['CI_COMMIT_TAG']
 else:
-    version = "1.0.6"
+    version = "1.0.7"
 
 setup(
     name='chai-guanaco',
     version=version,
     description='Chai Guanaco',
     author='Chai Research Corp.',
     author_email='hello@chai-research.com',
```

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/chat.py` & `chai-guanaco-1.0.7/src/chai_guanaco/chat.py`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/feedback.py` & `chai-guanaco-1.0.7/src/chai_guanaco/feedback.py`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/formatters.py` & `chai-guanaco-1.0.7/src/chai_guanaco/formatters.py`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/login_cli.py` & `chai-guanaco-1.0.7/src/chai_guanaco/login_cli.py`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/metrics.py` & `chai-guanaco-1.0.7/src/chai_guanaco/metrics.py`

 * *Files 4% similar despite different names*

```diff
@@ -14,24 +14,24 @@
 LEADERBOARD_ENDPOINT = "/leaderboard"
 FEEDBACK_CUTOFF_DAYS = 7
 MINIMUM_FEEDBACK_NUMBER_TO_DISPLAY = 50
 SUBMISSION_CUTOFF = datetime(2023, 7, 15)
 
 
 @auto_authenticate
-def display_leaderboard(developer_key=None):
-    df = get_leaderboard(developer_key)
+def display_leaderboard(developer_key=None, regenerate=False):
+    df = cache(get_leaderboard, regenerate)(developer_key)
     _print_formatted_leaderboard(df)
     return df
 
 
-@cache
 @auto_authenticate
 def get_leaderboard(developer_key=None):
-    submission_ids = _get_leaderboard_submission_ids(developer_key)
+    submission_ids = get_all_historical_submissions(developer_key)
+    submission_ids = _filter_old_submissions(submission_ids)
     leaderboard = []
     for submission_id in tqdm(submission_ids, 'Getting Metrics'):
         metrics = get_submission_metrics(submission_id, developer_key)
         leaderboard.append({'submission_id': submission_id, **metrics})
     return pd.DataFrame(leaderboard)
 
 
@@ -45,14 +45,24 @@
         'mcl': feedback_metrics.mcl,
         'user_response_length': feedback_metrics.user_response_length,
         'total_feedback_count': feedback_metrics.total_feedback_count
     }
     return metrics
 
 
+def get_all_historical_submissions(developer_key):
+    headers = {
+        "developer_key": developer_key,
+    }
+    url = get_url(LEADERBOARD_ENDPOINT)
+    resp = requests.get(url, headers=headers)
+    assert resp.status_code == 200, resp.json()
+    return list(resp.json().keys())
+
+
 class FeedbackMetrics():
     def __init__(self, feedback_data):
         feedbacks = _filter_feedbacks(feedback_data['feedback'])
         self.feedbacks = feedbacks.values()
 
     @property
     def convo_metrics(self):
@@ -91,51 +101,41 @@
         response_length = [len(m['content']) for m in self.messages if self._is_from_user(m)]
         return np.mean(response_length)
 
     def _is_from_user(self, message):
         return '_bot' not in message['sender']['uid']
 
 
-def _get_leaderboard_submission_ids(developer_key):
-    headers = {
-        "developer_key": developer_key,
-    }
-    url = get_url(LEADERBOARD_ENDPOINT)
-    resp = requests.get(url, headers=headers)
-    assert resp.status_code == 200, resp.json()
-    return resp.json().keys()
-
-
 def _print_formatted_leaderboard(df):
-    df = _filter_old_submissions(df)
     df = _filter_duplicated_submissions(df)
     df = _get_filtered_leaderboard(df)
     df['engagement_score'] = _get_engagement_score(df.mcl, df.user_response_length)
     df['overall_rank'] = _get_overall_rank(df.engagement_score, df.thumbs_up_ratio)
     df = df.sort_values('overall_rank').reset_index(drop=True)
     _print_grand_prize(df)
     _print_engagement_prize(df)
     _print_thumbs_up_prize(df)
     return df
 
 
-def _filter_old_submissions(df):
-    timestamps = df.submission_id.apply(lambda x: x.split('_')[-1])
-    return df[timestamps.apply(_is_after_submission_start_time)]
+def _filter_old_submissions(submission_ids):
+    filtered_submissions = [k for k in submission_ids if _is_after_submission_start_time(k)]
+    return filtered_submissions
 
 
 def _filter_duplicated_submissions(df):
     df = df.sort_values(['total_feedback_count'], ascending=False)
     df['model_name'] = df.submission_id.apply(lambda x: '_'.join(x.split('_')[:-1]))
     df = df.drop_duplicates('model_name', keep='first')
     df.drop('model_name', axis=1, inplace=True)
     return df
 
 
-def _is_after_submission_start_time(timestamp):
+def _is_after_submission_start_time(submission_id):
+    timestamp = submission_id.split('_')[-1]
     try:
         timestamp = datetime.fromtimestamp(int(timestamp))
         is_after_cutoff = timestamp >= SUBMISSION_CUTOFF
     except ValueError:
         is_after_cutoff = False
     return is_after_cutoff
```

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/blade.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/blade.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/captain_wyatt.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/captain_wyatt.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/coffee_shop_girl.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/coffee_shop_girl.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/filbert.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/filbert.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/leo.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/leo.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/levi.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/levi.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/mr_wilson.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/mr_wilson.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/nerd_girl.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/nerd_girl.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/scaramouche.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/scaramouche.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/story_teller.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/story_teller.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/vampire_queen.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/vampire_queen.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/resources/bot_config/wednesday_addams.json` & `chai-guanaco-1.0.7/src/chai_guanaco/resources/bot_config/wednesday_addams.json`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/submit.py` & `chai-guanaco-1.0.7/src/chai_guanaco/submit.py`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco/utils.py` & `chai-guanaco-1.0.7/src/chai_guanaco/utils.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import os
 import inspect
 import pickle
 from time import time
 
-CACHE_UPDATE_HOURS = 12
+CACHE_UPDATE_HOURS = 6
 
 
 def guanaco_data_dir():
     home_dir = os.path.expanduser("~")
     data_dir = os.environ.get('GUANACO_DATA_DIR', f'{home_dir}/.chai-guanaco')
     os.makedirs(data_dir, exist_ok=True)
     return data_dir
@@ -19,19 +19,20 @@
               'green': '\033[92m',
               'yellow': '\033[93m',
               'red': '\033[91m'}
     assert color in colors.keys()
     print(f'{colors[color]}{text}\033[0m')
 
 
-def cache(func):
+def cache(func, regenerate=False):
     def wrapper(*args, **kwargs):
         file_path = _get_cache_file_path(func, args, kwargs)
         try:
             result = _load_from_cache(file_path)
+            assert not regenerate
             # ensuring file is less than N hours old, otherwise regenerate
             assert (time() - os.path.getmtime(file_path)) < 3600 * CACHE_UPDATE_HOURS
         except (FileNotFoundError, AssertionError):
             result = func(*args, **kwargs)
             _save_to_cache(file_path, result)
         return result
     return wrapper
```

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco.egg-info/PKG-INFO` & `chai-guanaco-1.0.7/src/chai_guanaco.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chai-guanaco
-Version: 1.0.6
+Version: 1.0.7
 Summary: Chai Guanaco
 Home-page: https://www.chai-research.com
 Author: Chai Research Corp.
 Author-email: hello@chai-research.com
 License: MIT
 Description: [![Guanaco Banner](https://imgur.com/wJHIeAU.png)](https://www.chai-research.com/competition.html)
```

### Comparing `chai-guanaco-1.0.6/src/chai_guanaco.egg-info/SOURCES.txt` & `chai-guanaco-1.0.7/src/chai_guanaco.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/tests/resources/test_get_leaderboard.yaml` & `chai-guanaco-1.0.7/tests/resources/test_get_leaderboard.yaml`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/tests/resources/test_get_submission_metrics.yaml` & `chai-guanaco-1.0.7/tests/resources/test_get_submission_metrics.yaml`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/tests/test_chat.py` & `chai-guanaco-1.0.7/tests/test_chat.py`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/tests/test_feedback.py` & `chai-guanaco-1.0.7/tests/test_feedback.py`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/tests/test_guanaco_python_utils.py` & `chai-guanaco-1.0.7/tests/test_guanaco_python_utils.py`

 * *Files 12% similar despite different names*

```diff
@@ -7,14 +7,18 @@
 
 
 @cache
 def add(a, b):
     return a + b
 
 
+def subtract(a, b):
+    return a - b
+
+
 def test_cache_leaderboard_returns_from_cache(tmpdir):
     with patch('chai_guanaco.utils.guanaco_data_dir', return_value=tmpdir):
         assert add(1, 2) == 3
         cache_file = os.path.join(tmpdir, 'cache', 'add(a=1, b=2).pkl')
         assert load_from_file(cache_file) == 3
 
         # on second run, get_leaderboard loads from cache
@@ -37,14 +41,24 @@
         # on second run, get leaderboard does not read from cache as it is
         # after 12 hour
         dump_to_file(cache_file, 4)
         assert add(1, 2) == 3
         assert load_from_file(cache_file) == 3
 
 
+def test_cache_leaderboard_can_regenerate(tmpdir):
+    with patch('chai_guanaco.utils.guanaco_data_dir', return_value=tmpdir):
+        assert cache(subtract)(1, 2) == -1
+        cache_file = os.path.join(tmpdir, 'cache', 'subtract(a=1, b=2).pkl')
+        dump_to_file(cache_file, 8)
+
+        assert cache(subtract, regenerate=True)(1, 2) == -1
+        assert load_from_file(cache_file) == -1
+
+
 def load_from_file(filepath):
     with open(filepath, 'rb') as f:
         return pickle.load(f)
 
 
 def dump_to_file(filepath, data):
     with open(filepath, 'wb') as f:
```

### Comparing `chai-guanaco-1.0.6/tests/test_login.py` & `chai-guanaco-1.0.7/tests/test_login.py`

 * *Files identical despite different names*

### Comparing `chai-guanaco-1.0.6/tests/test_metrics.py` & `chai-guanaco-1.0.7/tests/test_metrics.py`

 * *Files 6% similar despite different names*

```diff
@@ -7,15 +7,16 @@
 
 import chai_guanaco as chai
 from chai_guanaco import metrics
 
 RESOURCE_DIR = os.path.join(os.path.abspath(os.path.join(__file__, '..')), 'resources')
 
 
-@mock.patch('chai_guanaco.metrics._get_leaderboard_submission_ids')
+@mock.patch('chai_guanaco.metrics.get_all_historical_submissions')
+@mock.patch('chai_guanaco.metrics._filter_old_submissions')
 @mock.patch('chai_guanaco.utils.guanaco_data_dir')
 @freeze_time('2023-07-14 19:00:00')
 @vcr.use_cassette(os.path.join(RESOURCE_DIR, 'test_get_leaderboard.yaml'))
 def test_get_leaderboard(data_dir_mock, get_ids_mock, tmpdir):
     data_dir_mock.return_value = str(tmpdir)
     get_ids_mock.return_value = [
             'wizard-vicuna-13b-bo4',
@@ -95,15 +96,15 @@
         'user_response_length': [500, 600, 700, 800],
         'thumbs_up_ratio': [0.1, 0.5, 0.8, 0.2],
     }
     all_metrics_df = pd.DataFrame(data)
 
     df = metrics._print_formatted_leaderboard(all_metrics_df)
 
-    assert len(df) == 2
+    assert len(df) == 3
     expected_columns = [
             'submission_id', 'mcl', 'user_response_length',
             'thumbs_up_ratio', 'engagement_score', 'overall_rank'
         ]
     assert list(df.columns) == expected_columns
     assert pd.api.types.is_integer_dtype(df['overall_rank'])
     pd.testing.assert_frame_equal(all_metrics_df, pd.DataFrame(data))
```

### Comparing `chai-guanaco-1.0.6/tests/test_submit.py` & `chai-guanaco-1.0.7/tests/test_submit.py`

 * *Files identical despite different names*

