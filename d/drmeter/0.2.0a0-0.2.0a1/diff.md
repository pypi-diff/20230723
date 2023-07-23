# Comparing `tmp/drmeter-0.2.0a0.tar.gz` & `tmp/drmeter-0.2.0a1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "drmeter-0.2.0a0.tar", max compression
+gzip compressed data, was "drmeter-0.2.0a1.tar", max compression
```

## Comparing `drmeter-0.2.0a0.tar` & `drmeter-0.2.0a1.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1084 2023-07-16 21:10:19.374586 drmeter-0.2.0a0/LICENSE
--rw-r--r--   0        0        0     1456 2018-06-24 09:02:50.666931 drmeter-0.2.0a0/README.md
--rw-r--r--   0        0        0       80 2023-07-21 20:39:45.543595 drmeter-0.2.0a0/drmeter/__init__.py
--rw-r--r--   0        0        0       37 2023-07-19 20:02:20.763480 drmeter-0.2.0a0/drmeter/__main__.py
--rw-r--r--   0        0        0     2118 2023-07-21 21:50:33.763279 drmeter-0.2.0a0/drmeter/algorithm.py
--rw-r--r--   0        0        0     1692 2023-07-21 20:33:40.498913 drmeter-0.2.0a0/drmeter/cli.py
--rw-r--r--   0        0        0     5306 2023-07-21 21:52:06.867148 drmeter-0.2.0a0/drmeter/models.py
--rw-r--r--   0        0        0      908 2023-07-21 21:28:54.083094 drmeter-0.2.0a0/drmeter/utils.py
--rw-r--r--   0        0        0     1415 2023-07-21 22:12:24.437006 drmeter-0.2.0a0/pyproject.toml
--rw-r--r--   0        0        0     2179 1970-01-01 00:00:00.000000 drmeter-0.2.0a0/PKG-INFO
+-rw-r--r--   0        0        0     1084 2023-07-23 13:57:29.690813 drmeter-0.2.0a1/LICENSE
+-rw-r--r--   0        0        0     1857 2023-07-23 13:57:29.690813 drmeter-0.2.0a1/README.md
+-rw-r--r--   0        0        0      262 2023-07-23 13:57:29.690813 drmeter-0.2.0a1/drmeter/__init__.py
+-rw-r--r--   0        0        0       37 2023-07-23 13:57:29.690813 drmeter-0.2.0a1/drmeter/__main__.py
+-rw-r--r--   0        0        0     2118 2023-07-23 13:57:29.690813 drmeter-0.2.0a1/drmeter/algorithm.py
+-rw-r--r--   0        0        0     4394 2023-07-23 13:57:29.690813 drmeter-0.2.0a1/drmeter/cli.py
+-rw-r--r--   0        0        0     5359 2023-07-23 13:57:29.690813 drmeter-0.2.0a1/drmeter/models.py
+-rw-r--r--   0        0        0      973 2023-07-23 13:57:29.690813 drmeter-0.2.0a1/drmeter/utils.py
+-rw-r--r--   0        0        0     1535 2023-07-23 13:57:29.690813 drmeter-0.2.0a1/pyproject.toml
+-rw-r--r--   0        0        0     2659 1970-01-01 00:00:00.000000 drmeter-0.2.0a1/PKG-INFO
```

### Comparing `drmeter-0.2.0a0/LICENSE` & `drmeter-0.2.0a1/LICENSE`

 * *Files identical despite different names*

### Comparing `drmeter-0.2.0a0/drmeter/algorithm.py` & `drmeter-0.2.0a1/drmeter/algorithm.py`

 * *Files identical despite different names*

### Comparing `drmeter-0.2.0a0/drmeter/models.py` & `drmeter-0.2.0a1/drmeter/models.py`

 * *Files 9% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 from pathlib import Path
 from typing import TYPE_CHECKING, Iterable
 
 import numpy as np
 import soundfile as sf
 from rich.table import Table
 
-from drmeter.utils import rich_box, rich_spinner, to_decibels
+from drmeter.utils import fmt_dr_score, rich_box, rich_spinner, to_decibels
 
 if TYPE_CHECKING:
     from rich.console import Console, ConsoleOptions, RenderableType
 
 
 @dataclass
 class DynamicRangeResult:
@@ -62,28 +62,29 @@
         with sf.SoundFile(self.path) as soundfile:
             self.result = dynamic_range(soundfile)
 
     def rich_table_render(self) -> tuple[RenderableType, ...]:
         if not self.result:
             return (rich_spinner, rich_spinner, rich_spinner, self.path.name)
         return (
-            f"DR{self.result.total_dr_score:02.0f}",
+            fmt_dr_score(self.result.total_dr_score),
             f"{self.result.total_peak_db:+6.2f} dB",
             f"{self.result.total_rms_db:+6.2f} dB",
             self.path.name,
         )
 
 
 @dataclass
 class AnalysisList:
     results: dict[Path, AnalysisItem] = field(default_factory=dict)
 
+    overall_result: DynamicRangeResult | None = None
+
     _table: Table | None = None
     _directory: Path | None = None
-    _overall: DynamicRangeResult | None = None
     _overall_count: int = 0
 
     def __len__(self) -> int:
         return len(self.results)
 
     @classmethod
     def from_paths(cls, paths: list[Path]) -> AnalysisList:
@@ -110,19 +111,19 @@
 
         if len(self.results) < 2:
             return
 
         self._table.add_section()
         desc = f"Overall ({self._overall_count} file{'s' if self._overall_count !=1 else ''})"
         style = "bold magenta"
-        if self._overall and self._overall_count:
+        if self.overall_result and self._overall_count:
             self._table.add_row(
-                f"DR{self._overall.total_dr_score:02.0f}",
-                f"{self._overall.total_peak_db:+6.2f} dB",
-                f"{self._overall.total_rms_db:+6.2f} dB",
+                fmt_dr_score(self.overall_result.total_dr_score),
+                f"{self.overall_result.total_peak_db:+6.2f} dB",
+                f"{self.overall_result.total_rms_db:+6.2f} dB",
                 desc,
                 style=style,
             )
         else:
             self._table.add_row(
                 rich_spinner, rich_spinner, rich_spinner, desc, style=style
             )
@@ -139,15 +140,15 @@
 
             dr_score += result.result.total_dr_score
             peak_pressure = max(result.result.total_peak_pressure, peak_pressure)
             rms_pressure += result.result.total_rms_pressure
             result_count += 1
 
         if result_count > 0:
-            self._overall = DynamicRangeResult(
+            self.overall_result = DynamicRangeResult(
                 dr_score=dr_score / result_count,
                 peak_pressure=peak_pressure,
                 rms_pressure=rms_pressure / result_count,
             )
             self._overall_count = result_count
 
     def __rich_console__(
```

### Comparing `drmeter-0.2.0a0/drmeter/utils.py` & `drmeter-0.2.0a1/drmeter/utils.py`

 * *Files 12% similar despite different names*

```diff
@@ -28,14 +28,18 @@
 
 def to_decibels(val: float) -> float:
     if val == 0:
         return -math.inf
     return 20 * math.log10(val)
 
 
+def fmt_dr_score(val: float) -> str:
+    return f"DR{val:.0f}"
+
+
 rich_box = Box(
     """\
 ╭──╮
 │  │
 ├──┤
 │  │
 ├──┤
```

### Comparing `drmeter-0.2.0a0/pyproject.toml` & `drmeter-0.2.0a1/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -1,36 +1,39 @@
 [tool.poetry]
 name = "drmeter"
-version = "0.2.0a0"
+version = "0.2.0a1"
 description = "Dynamic Range (DR) algorithm implementation in python"
 authors = ["Jan Willhaus <mail@janwillhaus.de>"]
 license = "MIT"
 readme = "README.md"
 repository = "https://github.com/janw/drmeter"
 
 [tool.poetry.scripts]
 drmeter = 'drmeter.cli:main'
 
 [tool.poetry.dependencies]
 python = "^3.9"
 soundfile = "^0.12.1"
 numpy = "^1.25"
 rich = "^13.4.2"
+rich-click = "^1.6.1"
+tox = "^4.6.4"
 
 [tool.poetry.group.dev.dependencies]
 pre-commit = "^3.3.3"
 black = "^23.7.0"
 ruff = "^0.0.278"
 tox = "^4.6.4"
 ipython = "^8.14.0"
 ipdb = "^0.13.13"
 mypy = "^1.4.1"
 
 [tool.poetry.group.tests.dependencies]
 pytest = "^7.4.0"
+pytest-cov = "^4.1.0"
 
 [tool.ruff]
 line-length = 120
 target-version = "py39"
 extend-select = [
     "I",   # isort
     "B",   # bugbear
@@ -62,10 +65,16 @@
 strict_optional = true
 packages = ["drmeter", "tests"]
 
 [[tool.mypy.overrides]]
 module = "soundfile.*"
 ignore_missing_imports = true
 
+[tool.coverage.run]
+omit = [
+    "tests/*",
+    "venv/*",
+]
+
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

