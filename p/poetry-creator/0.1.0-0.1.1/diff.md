# Comparing `tmp/poetry creator-0.1.0.tar.gz` & `tmp/poetry-creator-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "poetry creator-0.1.0.tar", last modified: Sun Jul 23 19:56:38 2023, max compression
+gzip compressed data, was "poetry-creator-0.1.1.tar", last modified: Sun Jul 23 20:03:43 2023, max compression
```

## Comparing `poetry creator-0.1.0.tar` & `poetry-creator-0.1.1.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 georgepickett   (502) staff       (20)        0 2023-07-23 19:56:38.985106 poetry creator-0.1.0/
--rw-r--r--   0 georgepickett   (502) staff       (20)       58 2023-07-23 19:56:38.984838 poetry creator-0.1.0/PKG-INFO
--rw-r--r--   0 georgepickett   (502) staff       (20)     1401 2023-07-23 19:54:02.000000 poetry creator-0.1.0/README.md
-drwxr-xr-x   0 georgepickett   (502) staff       (20)        0 2023-07-23 19:56:38.982751 poetry creator-0.1.0/poetry_creator/
--rw-r--r--   0 georgepickett   (502) staff       (20)        0 2023-07-23 19:48:17.000000 poetry creator-0.1.0/poetry_creator/__init__.py
--rw-r--r--   0 georgepickett   (502) staff       (20)     2262 2023-07-23 19:41:41.000000 poetry creator-0.1.0/poetry_creator/create_poetry.py
-drwxr-xr-x   0 georgepickett   (502) staff       (20)        0 2023-07-23 19:56:38.984476 poetry creator-0.1.0/poetry_creator.egg-info/
--rw-r--r--   0 georgepickett   (502) staff       (20)       58 2023-07-23 19:56:38.000000 poetry creator-0.1.0/poetry_creator.egg-info/PKG-INFO
--rw-r--r--   0 georgepickett   (502) staff       (20)      307 2023-07-23 19:56:38.000000 poetry creator-0.1.0/poetry_creator.egg-info/SOURCES.txt
--rw-r--r--   0 georgepickett   (502) staff       (20)        1 2023-07-23 19:56:38.000000 poetry creator-0.1.0/poetry_creator.egg-info/dependency_links.txt
--rw-r--r--   0 georgepickett   (502) staff       (20)       68 2023-07-23 19:56:38.000000 poetry creator-0.1.0/poetry_creator.egg-info/entry_points.txt
--rw-r--r--   0 georgepickett   (502) staff       (20)        7 2023-07-23 19:56:38.000000 poetry creator-0.1.0/poetry_creator.egg-info/requires.txt
--rw-r--r--   0 georgepickett   (502) staff       (20)       15 2023-07-23 19:56:38.000000 poetry creator-0.1.0/poetry_creator.egg-info/top_level.txt
--rw-r--r--   0 georgepickett   (502) staff       (20)       38 2023-07-23 19:56:38.985191 poetry creator-0.1.0/setup.cfg
--rw-r--r--   0 georgepickett   (502) staff       (20)      311 2023-07-23 19:49:06.000000 poetry creator-0.1.0/setup.py
+drwxr-xr-x   0 georgepickett   (502) staff       (20)        0 2023-07-23 20:03:43.060336 poetry-creator-0.1.1/
+-rw-r--r--   0 georgepickett   (502) staff       (20)     1860 2023-07-23 20:03:43.060023 poetry-creator-0.1.1/PKG-INFO
+-rw-r--r--   0 georgepickett   (502) staff       (20)     1401 2023-07-23 19:54:02.000000 poetry-creator-0.1.1/README.md
+drwxr-xr-x   0 georgepickett   (502) staff       (20)        0 2023-07-23 20:03:43.057371 poetry-creator-0.1.1/poetry_creator/
+-rw-r--r--   0 georgepickett   (502) staff       (20)        0 2023-07-23 19:48:17.000000 poetry-creator-0.1.1/poetry_creator/__init__.py
+-rw-r--r--   0 georgepickett   (502) staff       (20)     2565 2023-07-23 20:02:49.000000 poetry-creator-0.1.1/poetry_creator/create_poetry.py
+drwxr-xr-x   0 georgepickett   (502) staff       (20)        0 2023-07-23 20:03:43.059600 poetry-creator-0.1.1/poetry_creator.egg-info/
+-rw-r--r--   0 georgepickett   (502) staff       (20)     1860 2023-07-23 20:03:42.000000 poetry-creator-0.1.1/poetry_creator.egg-info/PKG-INFO
+-rw-r--r--   0 georgepickett   (502) staff       (20)      307 2023-07-23 20:03:43.000000 poetry-creator-0.1.1/poetry_creator.egg-info/SOURCES.txt
+-rw-r--r--   0 georgepickett   (502) staff       (20)        1 2023-07-23 20:03:42.000000 poetry-creator-0.1.1/poetry_creator.egg-info/dependency_links.txt
+-rw-r--r--   0 georgepickett   (502) staff       (20)       68 2023-07-23 20:03:42.000000 poetry-creator-0.1.1/poetry_creator.egg-info/entry_points.txt
+-rw-r--r--   0 georgepickett   (502) staff       (20)        7 2023-07-23 20:03:42.000000 poetry-creator-0.1.1/poetry_creator.egg-info/requires.txt
+-rw-r--r--   0 georgepickett   (502) staff       (20)       15 2023-07-23 20:03:42.000000 poetry-creator-0.1.1/poetry_creator.egg-info/top_level.txt
+-rw-r--r--   0 georgepickett   (502) staff       (20)       38 2023-07-23 20:03:43.060435 poetry-creator-0.1.1/setup.cfg
+-rw-r--r--   0 georgepickett   (502) staff       (20)      811 2023-07-23 20:03:35.000000 poetry-creator-0.1.1/setup.py
```

### Comparing `poetry creator-0.1.0/README.md` & `poetry-creator-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `poetry creator-0.1.0/poetry_creator/create_poetry.py` & `poetry-creator-0.1.1/poetry_creator/create_poetry.py`

 * *Files 9% similar despite different names*

```diff
@@ -68,21 +68,29 @@
     project_dir = Path(project_name)
     subprocess.run(["poetry", "install"], check=True, cwd=project_dir)
 
 def run_uvicorn(project_name):
     project_dir = Path(project_name)
     os.system(f"cd {project_dir} && poetry run uvicorn main:app --reload")
 
+def check_poetry_installed():
+    try:
+        subprocess.run(["poetry", "--version"], check=True)
+    except subprocess.CalledProcessError:
+        print("Poetry is not installed, installing it now...")
+        subprocess.run(["pip", "install", "poetry"], check=True)
+
 def main():
     parser = argparse.ArgumentParser(description='Create a new Python project with Poetry.')
     parser.add_argument('project_name', type=str, help='The name of the project.')
 
     args = parser.parse_args()
 
     try:
+        check_poetry_installed()
         create_project(args.project_name)
         install_dependencies(args.project_name)
         run_uvicorn(args.project_name)
     except Exception as e:
         print(f"Error: {e}")
         exit(1)
```

