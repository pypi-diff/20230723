# Comparing `tmp/pyquizrd-0.1.5.tar.gz` & `tmp/pyquizrd-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyquizrd-0.1.5.tar", max compression
+gzip compressed data, was "pyquizrd-0.1.6.tar", max compression
```

## Comparing `pyquizrd-0.1.5.tar` & `pyquizrd-0.1.6.tar`

### file list

```diff
@@ -1,20 +1,20 @@
--rw-r--r--   0        0        0       98 2023-07-23 10:34:43.549162 pyquizrd-0.1.5/README.md
--rw-r--r--   0        0        0      425 2023-07-23 11:49:43.727292 pyquizrd-0.1.5/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-22 17:17:17.006420 pyquizrd-0.1.5/pyquizrd/__init__.py
--rw-r--r--   0        0        0        0 2023-07-22 18:11:49.069651 pyquizrd-0.1.5/pyquizrd/gpt/__init__.py
--rw-r--r--   0        0        0     2354 2023-07-23 11:44:15.765177 pyquizrd-0.1.5/pyquizrd/gpt/gpt.py
--rw-r--r--   0        0        0     1651 2023-07-23 09:59:48.550229 pyquizrd-0.1.5/pyquizrd/gpt/prompt.txt
--rw-r--r--   0        0        0      155 2023-07-23 10:00:37.082356 pyquizrd-0.1.5/pyquizrd/gpt/x.py
--rw-r--r--   0        0        0        0 2023-07-22 18:26:18.049474 pyquizrd-0.1.5/pyquizrd/jeopardy/__init__.py
--rw-r--r--   0        0        0     1614 2023-07-23 11:47:30.029432 pyquizrd-0.1.5/pyquizrd/jeopardy/jeopardy.py
--rw-r--r--   0        0        0  5256096 2023-07-22 18:26:18.051795 pyquizrd-0.1.5/pyquizrd/jeopardy/pruned_jeopardy.json
--rw-r--r--   0        0        0  1922867 2023-07-22 18:27:06.494033 pyquizrd-0.1.5/pyquizrd/jeopardy/pruned_jeopardy.json.Z
--rw-r--r--   0        0        0        0 2023-07-22 18:11:51.787936 pyquizrd-0.1.5/pyquizrd/manual/__init__.py
--rw-r--r--   0        0        0      480 2023-07-22 19:34:54.128923 pyquizrd-0.1.5/pyquizrd/manual/manual.py
--rw-r--r--   0        0        0        0 2023-07-22 18:11:54.929318 pyquizrd-0.1.5/pyquizrd/opentrivia/__init__.py
--rw-r--r--   0        0        0     1919 2023-07-22 19:26:29.744147 pyquizrd-0.1.5/pyquizrd/opentrivia/opentrivia.py
--rw-r--r--   0        0        0        0 2023-07-22 18:11:58.225280 pyquizrd-0.1.5/pyquizrd/palm/__init__.py
--rw-r--r--   0        0        0     1886 2023-07-23 11:43:45.582603 pyquizrd-0.1.5/pyquizrd/palm/palm.py
--rw-r--r--   0        0        0     1651 2023-07-22 17:28:49.452163 pyquizrd-0.1.5/pyquizrd/palm/prompt.txt
--rw-r--r--   0        0        0     1429 2023-07-23 10:33:33.092773 pyquizrd-0.1.5/pyquizrd/pyquizrd.py
--rw-r--r--   0        0        0      430 1970-01-01 00:00:00.000000 pyquizrd-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0      157 2023-07-23 16:32:47.584427 pyquizrd-0.1.6/README.md
+-rw-r--r--   0        0        0      425 2023-07-23 16:33:00.333559 pyquizrd-0.1.6/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-22 17:17:17.006420 pyquizrd-0.1.6/pyquizrd/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-22 18:11:49.069651 pyquizrd-0.1.6/pyquizrd/gpt/__init__.py
+-rw-r--r--   0        0        0     2354 2023-07-23 11:44:15.765177 pyquizrd-0.1.6/pyquizrd/gpt/gpt.py
+-rw-r--r--   0        0        0     1651 2023-07-23 09:59:48.550229 pyquizrd-0.1.6/pyquizrd/gpt/prompt.txt
+-rw-r--r--   0        0        0      155 2023-07-23 10:00:37.082356 pyquizrd-0.1.6/pyquizrd/gpt/x.py
+-rw-r--r--   0        0        0        0 2023-07-22 18:26:18.049474 pyquizrd-0.1.6/pyquizrd/jeopardy/__init__.py
+-rw-r--r--   0        0        0     1614 2023-07-23 11:47:30.029432 pyquizrd-0.1.6/pyquizrd/jeopardy/jeopardy.py
+-rw-r--r--   0        0        0  5256096 2023-07-22 18:26:18.051795 pyquizrd-0.1.6/pyquizrd/jeopardy/pruned_jeopardy.json
+-rw-r--r--   0        0        0  1922867 2023-07-22 18:27:06.494033 pyquizrd-0.1.6/pyquizrd/jeopardy/pruned_jeopardy.json.Z
+-rw-r--r--   0        0        0        0 2023-07-22 18:11:51.787936 pyquizrd-0.1.6/pyquizrd/manual/__init__.py
+-rw-r--r--   0        0        0      480 2023-07-22 19:34:54.128923 pyquizrd-0.1.6/pyquizrd/manual/manual.py
+-rw-r--r--   0        0        0        0 2023-07-22 18:11:54.929318 pyquizrd-0.1.6/pyquizrd/opentrivia/__init__.py
+-rw-r--r--   0        0        0     1919 2023-07-22 19:26:29.744147 pyquizrd-0.1.6/pyquizrd/opentrivia/opentrivia.py
+-rw-r--r--   0        0        0        0 2023-07-22 18:11:58.225280 pyquizrd-0.1.6/pyquizrd/palm/__init__.py
+-rw-r--r--   0        0        0     1886 2023-07-23 11:43:45.582603 pyquizrd-0.1.6/pyquizrd/palm/palm.py
+-rw-r--r--   0        0        0     1651 2023-07-22 17:28:49.452163 pyquizrd-0.1.6/pyquizrd/palm/prompt.txt
+-rw-r--r--   0        0        0     1429 2023-07-23 10:33:33.092773 pyquizrd-0.1.6/pyquizrd/pyquizrd.py
+-rw-r--r--   0        0        0      489 1970-01-01 00:00:00.000000 pyquizrd-0.1.6/PKG-INFO
```

### Comparing `pyquizrd-0.1.5/pyquizrd/gpt/gpt.py` & `pyquizrd-0.1.6/pyquizrd/gpt/gpt.py`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.5/pyquizrd/gpt/prompt.txt` & `pyquizrd-0.1.6/pyquizrd/gpt/prompt.txt`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.5/pyquizrd/jeopardy/jeopardy.py` & `pyquizrd-0.1.6/pyquizrd/jeopardy/jeopardy.py`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.5/pyquizrd/jeopardy/pruned_jeopardy.json` & `pyquizrd-0.1.6/pyquizrd/jeopardy/pruned_jeopardy.json`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.5/pyquizrd/jeopardy/pruned_jeopardy.json.Z` & `pyquizrd-0.1.6/pyquizrd/jeopardy/pruned_jeopardy.json.Z`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.5/pyquizrd/opentrivia/opentrivia.py` & `pyquizrd-0.1.6/pyquizrd/opentrivia/opentrivia.py`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.5/pyquizrd/palm/palm.py` & `pyquizrd-0.1.6/pyquizrd/palm/palm.py`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.5/pyquizrd/palm/prompt.txt` & `pyquizrd-0.1.6/pyquizrd/palm/prompt.txt`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.5/pyquizrd/pyquizrd.py` & `pyquizrd-0.1.6/pyquizrd/pyquizrd.py`

 * *Files identical despite different names*

