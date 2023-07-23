# Comparing `tmp/ConfigArgParse-1.5.5.tar.gz` & `tmp/ConfigArgParse-1.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ConfigArgParse-1.5.5.tar", last modified: Tue Jun 27 20:26:56 2023, max compression
+gzip compressed data, was "ConfigArgParse-1.7.tar", last modified: Sun Jul 23 16:20:00 2023, max compression
```

## Comparing `ConfigArgParse-1.5.5.tar` & `ConfigArgParse-1.7.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 weisburd   (502) staff       (20)        0 2023-06-27 20:26:56.870567 ConfigArgParse-1.5.5/
-drwxr-xr-x   0 weisburd   (502) staff       (20)        0 2023-06-27 20:26:56.866836 ConfigArgParse-1.5.5/ConfigArgParse.egg-info/
--rw-r--r--   0 weisburd   (502) staff       (20)    23633 2023-06-27 20:26:56.000000 ConfigArgParse-1.5.5/ConfigArgParse.egg-info/PKG-INFO
--rw-r--r--   0 weisburd   (502) staff       (20)      312 2023-06-27 20:26:56.000000 ConfigArgParse-1.5.5/ConfigArgParse.egg-info/SOURCES.txt
--rw-r--r--   0 weisburd   (502) staff       (20)        1 2023-06-27 20:26:56.000000 ConfigArgParse-1.5.5/ConfigArgParse.egg-info/dependency_links.txt
--rw-r--r--   0 weisburd   (502) staff       (20)       42 2023-06-27 20:26:56.000000 ConfigArgParse-1.5.5/ConfigArgParse.egg-info/requires.txt
--rw-r--r--   0 weisburd   (502) staff       (20)       15 2023-06-27 20:26:56.000000 ConfigArgParse-1.5.5/ConfigArgParse.egg-info/top_level.txt
--rw-r--r--   0 weisburd   (502) staff       (20)     1070 2018-02-04 17:57:28.000000 ConfigArgParse-1.5.5/LICENSE
--rw-r--r--   0 weisburd   (502) staff       (20)       51 2018-02-04 17:57:28.000000 ConfigArgParse-1.5.5/MANIFEST.in
--rw-r--r--   0 weisburd   (502) staff       (20)    23633 2023-06-27 20:26:56.870182 ConfigArgParse-1.5.5/PKG-INFO
--rw-r--r--   0 weisburd   (502) staff       (20)    22375 2023-06-27 20:24:25.000000 ConfigArgParse-1.5.5/README.rst
--rw-r--r--   0 weisburd   (502) staff       (20)    64519 2023-06-27 19:47:23.000000 ConfigArgParse-1.5.5/configargparse.py
--rw-r--r--   0 weisburd   (502) staff       (20)       38 2023-06-27 20:26:56.870681 ConfigArgParse-1.5.5/setup.cfg
--rw-r--r--   0 weisburd   (502) staff       (20)     4015 2023-06-27 20:20:39.000000 ConfigArgParse-1.5.5/setup.py
-drwxr-xr-x   0 weisburd   (502) staff       (20)        0 2023-06-27 20:26:56.868768 ConfigArgParse-1.5.5/tests/
--rw-r--r--   0 weisburd   (502) staff       (20)       46 2018-02-04 17:57:28.000000 ConfigArgParse-1.5.5/tests/__init__.py
--rw-r--r--   0 weisburd   (502) staff       (20)      140 2019-12-08 16:37:48.000000 ConfigArgParse-1.5.5/tests/__init__.pyc
--rw-r--r--   0 weisburd   (502) staff       (20)    70874 2023-06-27 19:58:08.000000 ConfigArgParse-1.5.5/tests/test_configargparse.py
+drwxr-xr-x   0 weisburd   (502) staff       (20)        0 2023-07-23 16:20:00.274346 ConfigArgParse-1.7/
+drwxr-xr-x   0 weisburd   (502) staff       (20)        0 2023-07-23 16:20:00.270352 ConfigArgParse-1.7/ConfigArgParse.egg-info/
+-rw-r--r--   0 weisburd   (502) staff       (20)    23677 2023-07-23 16:20:00.000000 ConfigArgParse-1.7/ConfigArgParse.egg-info/PKG-INFO
+-rw-r--r--   0 weisburd   (502) staff       (20)      312 2023-07-23 16:20:00.000000 ConfigArgParse-1.7/ConfigArgParse.egg-info/SOURCES.txt
+-rw-r--r--   0 weisburd   (502) staff       (20)        1 2023-07-23 16:20:00.000000 ConfigArgParse-1.7/ConfigArgParse.egg-info/dependency_links.txt
+-rw-r--r--   0 weisburd   (502) staff       (20)       42 2023-07-23 16:20:00.000000 ConfigArgParse-1.7/ConfigArgParse.egg-info/requires.txt
+-rw-r--r--   0 weisburd   (502) staff       (20)       15 2023-07-23 16:20:00.000000 ConfigArgParse-1.7/ConfigArgParse.egg-info/top_level.txt
+-rw-r--r--   0 weisburd   (502) staff       (20)     1070 2018-02-04 17:57:28.000000 ConfigArgParse-1.7/LICENSE
+-rw-r--r--   0 weisburd   (502) staff       (20)       51 2018-02-04 17:57:28.000000 ConfigArgParse-1.7/MANIFEST.in
+-rw-r--r--   0 weisburd   (502) staff       (20)    23677 2023-07-23 16:20:00.273988 ConfigArgParse-1.7/PKG-INFO
+-rw-r--r--   0 weisburd   (502) staff       (20)    22513 2023-07-23 14:26:23.000000 ConfigArgParse-1.7/README.rst
+-rw-r--r--   0 weisburd   (502) staff       (20)    64606 2023-07-23 14:36:35.000000 ConfigArgParse-1.7/configargparse.py
+-rw-r--r--   0 weisburd   (502) staff       (20)       38 2023-07-23 16:20:00.274445 ConfigArgParse-1.7/setup.cfg
+-rw-r--r--   0 weisburd   (502) staff       (20)     3922 2023-07-23 14:39:04.000000 ConfigArgParse-1.7/setup.py
+drwxr-xr-x   0 weisburd   (502) staff       (20)        0 2023-07-23 16:20:00.272655 ConfigArgParse-1.7/tests/
+-rw-r--r--   0 weisburd   (502) staff       (20)       46 2018-02-04 17:57:28.000000 ConfigArgParse-1.7/tests/__init__.py
+-rw-r--r--   0 weisburd   (502) staff       (20)      140 2019-12-08 16:37:48.000000 ConfigArgParse-1.7/tests/__init__.pyc
+-rw-r--r--   0 weisburd   (502) staff       (20)    70874 2023-06-27 19:58:08.000000 ConfigArgParse-1.7/tests/test_configargparse.py
```

### Comparing `ConfigArgParse-1.5.5/ConfigArgParse.egg-info/PKG-INFO` & `ConfigArgParse-1.7/ConfigArgParse.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,30 +1,29 @@
 Metadata-Version: 2.1
 Name: ConfigArgParse
-Version: 1.5.5
+Version: 1.7
 Summary: A drop-in replacement for argparse that allows options to also be set via config files and/or environment variables.
 Home-page: https://github.com/bw2/ConfigArgParse
 License: MIT
 Keywords: options,argparse,ConfigArgParse,config,environment variables,envvars,ENV,environment,optparse,YAML,INI
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
-Classifier: Programming Language :: Python :: 2
-Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.5
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
-Requires-Python: >=2.7, !=3.0.*, !=3.1.*, !=3.2.*, !=3.3.*, !=3.4.*
+Requires-Python: >=3.5
 Provides-Extra: yaml
 Provides-Extra: test
 License-File: LICENSE
 
 ConfigArgParse
 --------------
 
@@ -32,18 +31,23 @@
     :alt: PyPI version
     :target: https://pypi.python.org/pypi/ConfigArgParse
 
 .. image:: https://img.shields.io/pypi/pyversions/ConfigArgParse.svg
     :alt: Supported Python versions
     :target: https://pypi.python.org/pypi/ConfigArgParse
 
+.. image:: https://static.pepy.tech/badge/configargparse/week
+    :alt: Downloads per week
+    :target: https://pepy.tech/project/configargparse
+
 .. image:: https://img.shields.io/badge/-API_Documentation-blue
     :alt: API Documentation
     :target: https://bw2.github.io/ConfigArgParse/
 
+	     
 Overview
 ~~~~~~~~
 
 Applications with more than a handful of user-settable options are best
 configured through a combination of command line args, config files,
 hard-coded defaults, and in some cases, environment variables.
 
@@ -73,15 +77,15 @@
    in the -h help message
 -  new method :code:`print_values()` can report keys & values and where
    they were set (eg. command line, env var, config file, or default).
 -  lite-weight (no 3rd-party library dependencies except (optionally) PyYAML)
 -  extensible (:code:`ConfigFileParser` can be subclassed to define a new
    config file format)
 -  unittested by running the unittests that came with argparse but on
-   configargparse, and using tox to test with Python 2.7 and Python 3+
+   configargparse, and using tox to test with Python 3.5+
 
 Example
 ~~~~~~~
 
 *config_test.py*:
 
 Script that defines 4 options and a positional arg and then parses and prints the values. Also,
@@ -591,15 +595,15 @@
    have the same dest. Instead, since multiple options can't use the
    same long arg (eg. "--long-arg-x"), let the config key be either
    "--long-arg-x" or "long-arg-x". This means the developer can allow
    only a subset of the command-line args to be specified via config
    file (eg. short args like -x would be excluded). Also, that way
    config keys are automatically documented whenever the command line
    args are documented in the help message.
-5. > don't force users to put config file settings in the right .ini [sections].
+5. don't force users to put config file settings in the right .ini [sections].
    This doesn't have a clear benefit since all options are command-line settable,
    and so have a globally unique key anyway.
    Enforcing sections just makes things harder for the user and adds complexity to the implementation.
    NOTE: This design choice was preventing configargparse from integrating with common Python project
    config files like setup.cfg or pyproject.toml,
    so additional parser classes were added that parse only a subset of the values defined in INI or
    TOML config files.
```

### Comparing `ConfigArgParse-1.5.5/LICENSE` & `ConfigArgParse-1.7/LICENSE`

 * *Files identical despite different names*

### Comparing `ConfigArgParse-1.5.5/PKG-INFO` & `ConfigArgParse-1.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,30 +1,29 @@
 Metadata-Version: 2.1
 Name: ConfigArgParse
-Version: 1.5.5
+Version: 1.7
 Summary: A drop-in replacement for argparse that allows options to also be set via config files and/or environment variables.
 Home-page: https://github.com/bw2/ConfigArgParse
 License: MIT
 Keywords: options,argparse,ConfigArgParse,config,environment variables,envvars,ENV,environment,optparse,YAML,INI
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
-Classifier: Programming Language :: Python :: 2
-Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.5
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
-Requires-Python: >=2.7, !=3.0.*, !=3.1.*, !=3.2.*, !=3.3.*, !=3.4.*
+Requires-Python: >=3.5
 Provides-Extra: yaml
 Provides-Extra: test
 License-File: LICENSE
 
 ConfigArgParse
 --------------
 
@@ -32,18 +31,23 @@
     :alt: PyPI version
     :target: https://pypi.python.org/pypi/ConfigArgParse
 
 .. image:: https://img.shields.io/pypi/pyversions/ConfigArgParse.svg
     :alt: Supported Python versions
     :target: https://pypi.python.org/pypi/ConfigArgParse
 
+.. image:: https://static.pepy.tech/badge/configargparse/week
+    :alt: Downloads per week
+    :target: https://pepy.tech/project/configargparse
+
 .. image:: https://img.shields.io/badge/-API_Documentation-blue
     :alt: API Documentation
     :target: https://bw2.github.io/ConfigArgParse/
 
+	     
 Overview
 ~~~~~~~~
 
 Applications with more than a handful of user-settable options are best
 configured through a combination of command line args, config files,
 hard-coded defaults, and in some cases, environment variables.
 
@@ -73,15 +77,15 @@
    in the -h help message
 -  new method :code:`print_values()` can report keys & values and where
    they were set (eg. command line, env var, config file, or default).
 -  lite-weight (no 3rd-party library dependencies except (optionally) PyYAML)
 -  extensible (:code:`ConfigFileParser` can be subclassed to define a new
    config file format)
 -  unittested by running the unittests that came with argparse but on
-   configargparse, and using tox to test with Python 2.7 and Python 3+
+   configargparse, and using tox to test with Python 3.5+
 
 Example
 ~~~~~~~
 
 *config_test.py*:
 
 Script that defines 4 options and a positional arg and then parses and prints the values. Also,
@@ -591,15 +595,15 @@
    have the same dest. Instead, since multiple options can't use the
    same long arg (eg. "--long-arg-x"), let the config key be either
    "--long-arg-x" or "long-arg-x". This means the developer can allow
    only a subset of the command-line args to be specified via config
    file (eg. short args like -x would be excluded). Also, that way
    config keys are automatically documented whenever the command line
    args are documented in the help message.
-5. > don't force users to put config file settings in the right .ini [sections].
+5. don't force users to put config file settings in the right .ini [sections].
    This doesn't have a clear benefit since all options are command-line settable,
    and so have a globally unique key anyway.
    Enforcing sections just makes things harder for the user and adds complexity to the implementation.
    NOTE: This design choice was preventing configargparse from integrating with common Python project
    config files like setup.cfg or pyproject.toml,
    so additional parser classes were added that parse only a subset of the values defined in INI or
    TOML config files.
```

### Comparing `ConfigArgParse-1.5.5/README.rst` & `ConfigArgParse-1.7/README.rst`

 * *Files 1% similar despite different names*

```diff
@@ -5,18 +5,23 @@
     :alt: PyPI version
     :target: https://pypi.python.org/pypi/ConfigArgParse
 
 .. image:: https://img.shields.io/pypi/pyversions/ConfigArgParse.svg
     :alt: Supported Python versions
     :target: https://pypi.python.org/pypi/ConfigArgParse
 
+.. image:: https://static.pepy.tech/badge/configargparse/week
+    :alt: Downloads per week
+    :target: https://pepy.tech/project/configargparse
+
 .. image:: https://img.shields.io/badge/-API_Documentation-blue
     :alt: API Documentation
     :target: https://bw2.github.io/ConfigArgParse/
 
+	     
 Overview
 ~~~~~~~~
 
 Applications with more than a handful of user-settable options are best
 configured through a combination of command line args, config files,
 hard-coded defaults, and in some cases, environment variables.
 
@@ -46,15 +51,15 @@
    in the -h help message
 -  new method :code:`print_values()` can report keys & values and where
    they were set (eg. command line, env var, config file, or default).
 -  lite-weight (no 3rd-party library dependencies except (optionally) PyYAML)
 -  extensible (:code:`ConfigFileParser` can be subclassed to define a new
    config file format)
 -  unittested by running the unittests that came with argparse but on
-   configargparse, and using tox to test with Python 2.7 and Python 3+
+   configargparse, and using tox to test with Python 3.5+
 
 Example
 ~~~~~~~
 
 *config_test.py*:
 
 Script that defines 4 options and a positional arg and then parses and prints the values. Also,
@@ -564,15 +569,15 @@
    have the same dest. Instead, since multiple options can't use the
    same long arg (eg. "--long-arg-x"), let the config key be either
    "--long-arg-x" or "long-arg-x". This means the developer can allow
    only a subset of the command-line args to be specified via config
    file (eg. short args like -x would be excluded). Also, that way
    config keys are automatically documented whenever the command line
    args are documented in the help message.
-5. > don't force users to put config file settings in the right .ini [sections].
+5. don't force users to put config file settings in the right .ini [sections].
    This doesn't have a clear benefit since all options are command-line settable,
    and so have a globally unique key anyway.
    Enforcing sections just makes things harder for the user and adds complexity to the implementation.
    NOTE: This design choice was preventing configargparse from integrating with common Python project
    config files like setup.cfg or pyproject.toml,
    so additional parser classes were added that parse only a subset of the values defined in INI or
    TOML config files.
```

### Comparing `ConfigArgParse-1.5.5/configargparse.py` & `ConfigArgParse-1.7/configargparse.py`

 * *Files 0% similar despite different names*

```diff
@@ -1443,29 +1443,32 @@
 # wrap ArgumentParser's add_argument(..) method with the one above
 argparse._ActionsContainer.original_add_argument_method = argparse._ActionsContainer.add_argument
 argparse._ActionsContainer.add_argument = add_argument
 
 
 # add all public classes and constants from argparse module's namespace to this
 # module's namespace so that the 2 modules are truly interchangeable
-HelpFormatter = argparse.HelpFormatter
-RawDescriptionHelpFormatter = argparse.RawDescriptionHelpFormatter
-RawTextHelpFormatter = argparse.RawTextHelpFormatter
+Action = argparse.Action
 ArgumentDefaultsHelpFormatter = argparse.ArgumentDefaultsHelpFormatter
 ArgumentError = argparse.ArgumentError
 ArgumentTypeError = argparse.ArgumentTypeError
-Action = argparse.Action
 FileType = argparse.FileType
+HelpFormatter = argparse.HelpFormatter
+MetavarTypeHelpFormatter = argparse.MetavarTypeHelpFormatter
 Namespace = argparse.Namespace
+RawDescriptionHelpFormatter = argparse.RawDescriptionHelpFormatter
+RawTextHelpFormatter = argparse.RawTextHelpFormatter
 ONE_OR_MORE = argparse.ONE_OR_MORE
 OPTIONAL = argparse.OPTIONAL
+PARSER = argparse.PARSER
 REMAINDER = argparse.REMAINDER
 SUPPRESS = argparse.SUPPRESS
 ZERO_OR_MORE = argparse.ZERO_OR_MORE
 
+
 # deprecated PEP-8 incompatible API names.
 initArgumentParser = init_argument_parser
 getArgumentParser = get_argument_parser
 getArgParser = get_argument_parser
 getParser = get_argument_parser
 
 # create shorter aliases for the key methods and class names
```

### Comparing `ConfigArgParse-1.5.5/setup.py` & `ConfigArgParse-1.7/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -78,43 +78,42 @@
     'PyYAML',
     'pytest',
 ]
 
 
 setup(
     name='ConfigArgParse',
-    version="1.5.5",
+    version="1.7",
     description='A drop-in replacement for argparse that allows options to '
                 'also be set via config files and/or environment variables.',
     long_description=long_description,
     url='https://github.com/bw2/ConfigArgParse',
     py_modules=['configargparse'],
     include_package_data=True,
     license="MIT",
     keywords='options, argparse, ConfigArgParse, config, environment variables, '
              'envvars, ENV, environment, optparse, YAML, INI',
     classifiers=[
         'Development Status :: 4 - Beta',
         'Intended Audience :: Developers',
         'License :: OSI Approved :: MIT License',
         'Natural Language :: English',
-        "Programming Language :: Python :: 2",
-        'Programming Language :: Python :: 2.7',
         'Programming Language :: Python :: 3',
         'Programming Language :: Python :: 3.5',
         'Programming Language :: Python :: 3.6',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
+        'Programming Language :: Python :: 3.11',
         'Programming Language :: Python :: Implementation :: CPython',
         'Programming Language :: Python :: Implementation :: PyPy',
     ],
     test_suite='tests',
-    python_requires='>=2.7, !=3.0.*, !=3.1.*, !=3.2.*, !=3.3.*, !=3.4.*',
+    python_requires='>=3.5',
     install_requires=install_requires,
     tests_require=tests_require,
     extras_require = {
         'yaml': ["PyYAML"],
         'test': tests_require,
     }
 )
```

### Comparing `ConfigArgParse-1.5.5/tests/test_configargparse.py` & `ConfigArgParse-1.7/tests/test_configargparse.py`

 * *Files identical despite different names*

