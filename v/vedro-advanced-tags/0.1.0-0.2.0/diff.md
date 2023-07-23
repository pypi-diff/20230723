# Comparing `tmp/vedro-advanced-tags-0.1.0.tar.gz` & `tmp/vedro-advanced-tags-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vedro-advanced-tags-0.1.0.tar", last modified: Fri Dec 30 15:17:55 2022, max compression
+gzip compressed data, was "vedro-advanced-tags-0.2.0.tar", last modified: Sun Jul 23 19:49:31 2023, max compression
```

## Comparing `vedro-advanced-tags-0.1.0.tar` & `vedro-advanced-tags-0.2.0.tar`

### file list

```diff
@@ -1,18 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2022-12-30 15:17:55.249270 vedro-advanced-tags-0.1.0/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2022-12-30 15:17:46.000000 vedro-advanced-tags-0.1.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1702 2022-12-30 15:17:55.249270 vedro-advanced-tags-0.1.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1120 2022-12-30 15:17:46.000000 vedro-advanced-tags-0.1.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      743 2022-12-30 15:17:55.253270 vedro-advanced-tags-0.1.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1115 2022-12-30 15:17:46.000000 vedro-advanced-tags-0.1.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2022-12-30 15:17:55.249270 vedro-advanced-tags-0.1.0/vedro_advanced_tags/
--rw-r--r--   0 runner    (1001) docker     (123)      160 2022-12-30 15:17:46.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2540 2022-12-30 15:17:46.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags/_grammar.py
--rw-r--r--   0 runner    (1001) docker     (123)      530 2022-12-30 15:17:46.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags/_tag_matcher.py
--rw-r--r--   0 runner    (1001) docker     (123)     2001 2022-12-30 15:17:46.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags/_vedro_advanced_tags.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2022-12-30 15:17:46.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2022-12-30 15:17:55.249270 vedro-advanced-tags-0.1.0/vedro_advanced_tags.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1702 2022-12-30 15:17:55.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      423 2022-12-30 15:17:55.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2022-12-30 15:17:55.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2022-12-30 15:17:55.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2022-12-30 15:17:55.000000 vedro-advanced-tags-0.1.0/vedro_advanced_tags.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:49:31.590914 vedro-advanced-tags-0.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3016 2023-07-23 19:49:31.590914 vedro-advanced-tags-0.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2394 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      743 2023-07-23 19:49:31.590914 vedro-advanced-tags-0.2.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:49:31.586914 vedro-advanced-tags-0.2.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     6976 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/tests/test_advanced_tags.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/tests/test_grammar.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:49:31.590914 vedro-advanced-tags-0.2.0/vedro_advanced_tags/
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2540 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags/_grammar.py
+-rw-r--r--   0 runner    (1001) docker     (123)      528 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags/_tag_matcher.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2570 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags/_vedro_advanced_tags.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:49:20.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:49:31.590914 vedro-advanced-tags-0.2.0/vedro_advanced_tags.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3016 2023-07-23 19:49:31.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      473 2023-07-23 19:49:31.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:49:31.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 19:49:31.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-07-23 19:49:31.000000 vedro-advanced-tags-0.2.0/vedro_advanced_tags.egg-info/top_level.txt
```

### Comparing `vedro-advanced-tags-0.1.0/LICENSE` & `vedro-advanced-tags-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `vedro-advanced-tags-0.1.0/setup.cfg` & `vedro-advanced-tags-0.2.0/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 [bumpversion]
-current_version = 0.1.0
+current_version = 0.2.0
 message = bump version → {new_version}
 commit = True
 tag = True
 sign_tags = True
 
 [bumpversion:file:setup.py]
```

### Comparing `vedro-advanced-tags-0.1.0/setup.py` & `vedro-advanced-tags-0.2.0/setup.py`

 * *Files 7% similar despite different names*

```diff
@@ -9,28 +9,29 @@
 def find_dev_required():
     with open("requirements-dev.txt") as f:
         return f.read().splitlines()
 
 
 setup(
     name="vedro-advanced-tags",
-    version="0.1.0",
+    version="0.2.0",
     description="Vedro tags with boolean logic",
     long_description=open("README.md").read(),
     long_description_content_type="text/markdown",
     author="Nikita Tsvetkov",
-    author_email="nikitanovosibirsk@yandex.com",
+    author_email="tsv1@fastmail.com",
     python_requires=">=3.8",
     url="https://github.com/vedro-universe/vedro-advanced-tags",
     license="Apache-2.0",
     packages=find_packages(exclude=["tests", "tests.*"]),
     package_data={"vedro_advanced_tags": ["py.typed"]},
     install_requires=find_required(),
     tests_require=find_dev_required(),
     classifiers=[
         "License :: OSI Approved :: Apache Software License",
         "Programming Language :: Python :: 3.8",
         "Programming Language :: Python :: 3.9",
         "Programming Language :: Python :: 3.10",
+        "Programming Language :: Python :: 3.11",
         "Typing :: Typed",
     ],
 )
```

### Comparing `vedro-advanced-tags-0.1.0/vedro_advanced_tags/_grammar.py` & `vedro-advanced-tags-0.2.0/vedro_advanced_tags/_grammar.py`

 * *Files identical despite different names*

### Comparing `vedro-advanced-tags-0.1.0/vedro_advanced_tags/_tag_matcher.py` & `vedro-advanced-tags-0.2.0/vedro_advanced_tags/_tag_matcher.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 from abc import ABC, abstractmethod
 
 from ._grammar import TagsType, parse
 
-__all__ = ("AdvancdedTagMatcher", "TagMatcher",)
+__all__ = ("AdvancedTagMatcher", "TagMatcher",)
 
 
 class TagMatcher(ABC):
     def __init__(self, expr: str) -> None:
         self._expr = expr
 
     @abstractmethod
     def match(self, tags: TagsType) -> bool:
         pass
 
 
-class AdvancdedTagMatcher(TagMatcher):
+class AdvancedTagMatcher(TagMatcher):
     def __init__(self, expr: str) -> None:
         super().__init__(expr)
         self._grammar = parse(expr)
 
     def match(self, tags: TagsType) -> bool:
         return self._grammar(tags)
```

### Comparing `vedro-advanced-tags-0.1.0/vedro_advanced_tags/_vedro_advanced_tags.py` & `vedro-advanced-tags-0.2.0/vedro_advanced_tags/_vedro_advanced_tags.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,20 +1,20 @@
-from typing import Callable, Type, Union
+from typing import Any, Callable, Type, Union
 
-from vedro.core import Dispatcher, Plugin, PluginConfig
+from vedro.core import Dispatcher, Plugin, PluginConfig, VirtualScenario
 from vedro.events import ArgParsedEvent, ArgParseEvent, CleanupEvent, StartupEvent
 
-from ._tag_matcher import AdvancdedTagMatcher, TagMatcher
+from ._tag_matcher import AdvancedTagMatcher, TagMatcher
 
 __all__ = ("VedroAdvancedTags", "VedroAdvancedTagsPlugin",)
 
 
 class VedroAdvancedTagsPlugin(Plugin):
     def __init__(self, config: Type["VedroAdvancedTags"], *,
-                 tag_matcher_factory: Callable[[str], TagMatcher] = AdvancdedTagMatcher) -> None:
+                 tag_matcher_factory: Callable[[str], TagMatcher] = AdvancedTagMatcher) -> None:
         super().__init__(config)
         self._show_parsed = config.show_parsed
         self._matcher_factory = tag_matcher_factory
         self._matcher: Union[TagMatcher, None] = None
         self._tags: Union[str, None] = None
 
     def subscribe(self, dispatcher: Dispatcher) -> None:
@@ -25,28 +25,41 @@
 
     def on_arg_parse(self, event: ArgParseEvent) -> None:
         event.arg_parser.add_argument("-t", "--tags", help="Set tags")
 
     def on_arg_parsed(self, event: ArgParsedEvent) -> None:
         self._tags = event.args.tags
 
+    def _validate_tags(self, scenario: VirtualScenario, tags: Any) -> bool:
+        if not isinstance(tags, (list, tuple, set)):
+            raise TypeError(f"Scenario '{scenario.rel_path}' tags must be a list, tuple or set, "
+                            f"got {type(tags)}")
+
+        for tag in tags:
+            if not tag.isidentifier():
+                raise ValueError(
+                    f"Scenario '{scenario.rel_path}' tag '{tag}' is not a valid identifier")
+
+        return True
+
     async def on_startup(self, event: StartupEvent) -> None:
         if self._tags is None:
             return
 
         self._matcher = self._matcher_factory(self._tags)
         async for scenario in event.scheduler:
-            tags = list(getattr(scenario._orig_scenario, "tags", ()))
-            if not self._matcher.match(tags):
+            tags = getattr(scenario._orig_scenario, "tags", ())
+            self._validate_tags(scenario, tags)
+            if not self._matcher.match(list(tags)):
                 event.scheduler.ignore(scenario)
 
     def on_cleanup(self, event: CleanupEvent) -> None:
         if self._tags and self._matcher and self._show_parsed:
             event.report.add_summary(
                 f'--tags "{self._tags}" -> {self._matcher._grammar!r}')  # type: ignore
 
 
 class VedroAdvancedTags(PluginConfig):
     plugin = VedroAdvancedTagsPlugin
 
-    # Show parsed tags
+    # Show parsed tags in summary
     show_parsed: bool = False
```

