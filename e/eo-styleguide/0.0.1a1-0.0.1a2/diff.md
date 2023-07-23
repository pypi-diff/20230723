# Comparing `tmp/eo_styleguide-0.0.1a1.tar.gz` & `tmp/eo_styleguide-0.0.1a2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "eo_styleguide-0.0.1a1.tar", max compression
+gzip compressed data, was "eo_styleguide-0.0.1a2.tar", max compression
```

## Comparing `eo_styleguide-0.0.1a1.tar` & `eo_styleguide-0.0.1a2.tar`

### file list

```diff
@@ -1,6 +1,12 @@
--rw-r--r--   0        0        0     1847 2023-07-21 08:29:53.477181 eo_styleguide-0.0.1a1/README.md
--rw-r--r--   0        0        0       30 2023-07-21 21:02:00.734371 eo_styleguide-0.0.1a1/pyeo/__init__.py
--rw-r--r--   0        0        0      656 2023-07-21 22:10:48.285455 eo_styleguide-0.0.1a1/pyeo/main.py
--rw-r--r--   0        0        0        0 2023-07-21 21:17:44.927051 eo_styleguide-0.0.1a1/pyeo/py.typed
--rw-r--r--   0        0        0      771 2023-07-21 22:17:00.908799 eo_styleguide-0.0.1a1/pyproject.toml
--rw-r--r--   0        0        0     2702 1970-01-01 00:00:00.000000 eo_styleguide-0.0.1a1/PKG-INFO
+-rw-r--r--   0        0        0     3096 2023-07-23 14:12:32.395350 eo_styleguide-0.0.1a2/README.md
+-rw-r--r--   0        0        0     1237 2023-07-23 13:29:32.045996 eo_styleguide-0.0.1a2/pyeo/__init__.py
+-rw-r--r--   0        0        0     1118 2023-07-23 13:29:32.046205 eo_styleguide-0.0.1a2/pyeo/features/__init__.py
+-rw-r--r--   0        0        0     1307 2023-07-23 13:29:32.046339 eo_styleguide-0.0.1a2/pyeo/features/feature.py
+-rw-r--r--   0        0        0     1553 2023-07-23 14:12:32.395680 eo_styleguide-0.0.1a2/pyeo/features/final_object.py
+-rw-r--r--   0        0        0     2389 2023-07-23 13:29:32.046454 eo_styleguide-0.0.1a2/pyeo/features/method_has_protocol.py
+-rw-r--r--   0        0        0     1768 2023-07-23 13:29:32.046560 eo_styleguide-0.0.1a2/pyeo/features/object_has_protocol.py
+-rw-r--r--   0        0        0     2010 2023-07-23 13:29:32.046685 eo_styleguide-0.0.1a2/pyeo/features/protocol_method_code_free.py
+-rw-r--r--   0        0        0     2350 2023-07-23 14:12:32.396200 eo_styleguide-0.0.1a2/pyeo/main.py
+-rw-r--r--   0        0        0        0 2023-07-21 21:17:44.927051 eo_styleguide-0.0.1a2/pyeo/py.typed
+-rw-r--r--   0        0        0      797 2023-07-23 14:12:39.888892 eo_styleguide-0.0.1a2/pyproject.toml
+-rw-r--r--   0        0        0     3951 1970-01-01 00:00:00.000000 eo_styleguide-0.0.1a2/PKG-INFO
```

### Comparing `eo_styleguide-0.0.1a1/pyproject.toml` & `eo_styleguide-0.0.1a2/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 [tool.poetry]
 name = "eo-styleguide"
 packages = [
     {include = "pyeo"}
 ]
-version = "0.0.1-alpha1"
+version = "0.0.1-alpha2"
 description = "Pyeo is an advanced static analysis tool tailored specifically to enforce the principles advocated by Elegant Objects (elegantobjects.org) in Python projects. It serves as a quality control instrument to ensure that your Python code adheres to the core tenets of elegance, simplicity, and maintainability."
 authors = ["Almaz Ilaletdinov <a.ilaletdinov@yandex.ru>"]
 license = "MIT"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = ">=3.8,<4.0"
 mypy = "^1.0"
 
 [tool.poetry.group.dev.dependencies]
 wemake-python-styleguide = "0.17.0"
-pytest-mypy-plugins = "^2.0.0"
+pytest-mypy-plugins = "2.0.0"
+flake8-copyright = "0.2.4"
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `eo_styleguide-0.0.1a1/PKG-INFO` & `eo_styleguide-0.0.1a2/README.md`

 * *Files 18% similar despite different names*

```diff
@@ -1,37 +1,39 @@
-Metadata-Version: 2.1
-Name: eo-styleguide
-Version: 0.0.1a1
-Summary: Pyeo is an advanced static analysis tool tailored specifically to enforce the principles advocated by Elegant Objects (elegantobjects.org) in Python projects. It serves as a quality control instrument to ensure that your Python code adheres to the core tenets of elegance, simplicity, and maintainability.
-License: MIT
-Author: Almaz Ilaletdinov
-Author-email: a.ilaletdinov@yandex.ru
-Requires-Python: >=3.8,<4.0
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: mypy (>=1.0,<2.0)
-Description-Content-Type: text/markdown
-
 # pyeo
 
 [![wemake-python-styleguide](https://img.shields.io/badge/style-wemake-000000.svg)](https://github.com/wemake-services/wemake-python-styleguide)
 
 Pyeo  is an advanced static analysis tool tailored specifically to enforce the principles advocated by
 Elegant Objects (elegantobjects.org) in Python projects. It serves as a quality control instrument to ensure
 that your Python code adheres to the core tenets of elegance, simplicity, and maintainability.
 
-- No null ([why?](http://www.yegor256.com/2014/05/13/why-null-is-bad.html))
-- No code in constructors ([why?](http://www.yegor256.com/2015/05/07/ctors-must-be-code-free.html))
-- No getters and setters ([why?](http://www.yegor256.com/2014/09/16/getters-and-setters-are-evil.html))
-- No mutable objects ([why?](http://www.yegor256.com/2014/06/09/objects-should-be-immutable.html))
-- No readers, parsers, controllers, sorters, and so on ([why?](https://www.yegor256.com/2015/03/09/objects-end-with-er.html))
-- No static methods, not even private ones ([why?](http://www.yegor256.com/2017/02/07/private-method-is-new-class.html))
-- No instanceof, type casting, or reflection ([why?](http://www.yegor256.com/2015/04/02/class-casting-is-anti-pattern.html))
-- No public methods without a contract (interface) ([why?](https://www.yegor256.com/2014/11/20/seven-virtues-of-good-object.html#2-he-works-by-contracts))
-- No statements in test methods except assertThat ([why?](http://www.yegor256.com/2017/05/17/single-statement-unit-tests.html))
-- No ORM or ActiveRecord ([why?](https://www.yegor256.com/2014/12/01/orm-offensive-anti-pattern.html) and [why?](https://www.yegor256.com/2016/07/26/active-record.html))
-- No implementation inheritance ([why?](http://www.yegor256.com/2017/01/31/decorating-envelopes.html) and [why?](http://www.yegor256.com/2016/09/13/inheritance-is-procedural.html))
+- [x] ~~No null~~ ([why?](http://www.yegor256.com/2014/05/13/why-null-is-bad.html))
+
+Mypy helps prevent AttributeError and other type-related errors by providing static type checking for Python code. It allows specifying variable types, function arguments, and return types to catch potential type issues before the program runs. By using Mypy, developers can identify and fix problems related to attribute access and other type mismatches, leading to improved code quality and easier maintenance.
+
+- [ ] No code in constructors ([why?](http://www.yegor256.com/2015/05/07/ctors-must-be-code-free.html))
+
+- [ ] No getters and setters ([why?](http://www.yegor256.com/2014/09/16/getters-and-setters-are-evil.html))
+
+- [x] No mutable objects ([why?](http://www.yegor256.com/2014/06/09/objects-should-be-immutable.html))
+
+`attrs.define(frozen=True)` is a parameter used in the attrs library to create classes with attributes that cannot be modified after the instance is created (i.e., immutable or "frozen" classes).
+The [attrs](https://www.attrs.org/en/stable/) library allows defining classes using the `@attr.s` decorator or by explicitly calling the `attr.define` function, and `frozen=True` is one of the parameters for specifying attribute behavior in the class. 
+When you use `attrs.define(frozen=True)` for a class, all its attributes become read-only after the instance is created, making the class "frozen" or "immutable," preventing any changes to its attribute values.
+
+- [ ] No readers, parsers, controllers, sorters, and so on ([why?](https://www.yegor256.com/2015/03/09/objects-end-with-er.html))
+
+- [ ] No static methods, not even private ones ([why?](http://www.yegor256.com/2017/02/07/private-method-is-new-class.html))
+
+- [ ] No instanceof, type casting, or reflection ([why?](http://www.yegor256.com/2015/04/02/class-casting-is-anti-pattern.html))
+
+- [x] No public methods without a contract (interface) ([why?](https://www.yegor256.com/2014/11/20/seven-virtues-of-good-object.html#2-he-works-by-contracts))
+
+- [ ] No statements in test methods except assert ([why?](http://www.yegor256.com/2017/05/17/single-statement-unit-tests.html))
+
+- [ ] No ORM or ActiveRecord ([why?](https://www.yegor256.com/2014/12/01/orm-offensive-anti-pattern.html) and [why?](https://www.yegor256.com/2016/07/26/active-record.html))
+
+Detect using ORM or ActiveRecord tools on project by design/code review
+
+- [x] No implementation inheritance ([why?](http://www.yegor256.com/2017/01/31/decorating-envelopes.html) and [why?](http://www.yegor256.com/2016/09/13/inheritance-is-procedural.html))
 
+Each `@elegant` object must be `typing.final`
```

