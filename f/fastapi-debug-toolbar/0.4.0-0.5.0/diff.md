# Comparing `tmp/fastapi_debug_toolbar-0.4.0.tar.gz` & `tmp/fastapi_debug_toolbar-0.5.0.tar.gz`

## Comparing `fastapi_debug_toolbar-0.4.0.tar` & `fastapi_debug_toolbar-0.5.0.tar`

### file list

```diff
@@ -1,52 +1,50 @@
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/__init__.py
--rw-r--r--   0        0        0      640 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/api.py
--rw-r--r--   0        0        0     4487 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/middleware.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/py.typed
--rw-r--r--   0        0        0      127 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/responses.py
--rw-r--r--   0        0        0     5294 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/settings.py
--rw-r--r--   0        0        0     4158 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/toolbar.py
--rw-r--r--   0        0        0      102 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/types.py
--rw-r--r--   0        0        0     2403 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/utils.py
--rw-r--r--   0        0        0     3032 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/__init__.py
--rw-r--r--   0        0        0      620 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/headers.py
--rw-r--r--   0        0        0     3425 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/logging.py
--rw-r--r--   0        0        0     1025 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/profiling.py
--rw-r--r--   0        0        0     3478 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/pydantic.py
--rw-r--r--   0        0        0      970 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/redirects.py
--rw-r--r--   0        0        0      750 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/request.py
--rw-r--r--   0        0        0      399 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/routes.py
--rw-r--r--   0        0        0      130 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/settings.py
--rw-r--r--   0        0        0     6100 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/sql.py
--rw-r--r--   0        0        0     2762 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/sqlalchemy.py
--rw-r--r--   0        0        0     3121 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/timer.py
--rw-r--r--   0        0        0     2850 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/tortoise.py
--rw-r--r--   0        0        0      947 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/versions.py
--rw-r--r--   0        0        0       45 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/css/print.css
--rw-r--r--   0        0        0    12616 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/css/toolbar.css
--rw-r--r--   0        0        0     1359 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/img/icon-green.svg
--rw-r--r--   0        0        0     1359 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/img/icon-white.svg
--rw-r--r--   0        0        0       48 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/redirect.js
--rw-r--r--   0        0        0     1141 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/refresh.js
--rw-r--r--   0        0        0     3007 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/timer.js
--rw-r--r--   0        0        0     8772 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/toolbar.js
--rw-r--r--   0        0        0     3544 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/utils.js
--rw-r--r--   0        0        0     3249 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/versions.js
--rw-r--r--   0        0        0     1494 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/base.html
--rw-r--r--   0        0        0      575 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/redirect.html
--rw-r--r--   0        0        0      805 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/includes/panel_button.html
--rw-r--r--   0        0        0      420 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/includes/panel_content.html
--rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/headers.html
--rw-r--r--   0        0        0      720 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/logging.html
--rw-r--r--   0        0        0      241 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/profiling.html
--rw-r--r--   0        0        0     1329 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/pydantic.html
--rw-r--r--   0        0        0     1495 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/request.html
--rw-r--r--   0        0        0      715 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/routes.html
--rw-r--r--   0        0        0      636 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/settings.html
--rw-r--r--   0        0        0     3579 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/sql.html
--rw-r--r--   0        0        0      839 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/timer.html
--rw-r--r--   0        0        0      716 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/versions.html
--rw-r--r--   0        0        0      135 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/.gitignore
--rw-r--r--   0        0        0     1537 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/LICENSE
--rw-r--r--   0        0        0     2322 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/README.md
--rw-r--r--   0        0        0     2469 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/pyproject.toml
--rw-r--r--   0        0        0     4988 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.4.0/PKG-INFO
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/__init__.py
+-rw-r--r--   0        0        0      640 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/api.py
+-rw-r--r--   0        0        0     4487 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/middleware.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/py.typed
+-rw-r--r--   0        0        0      127 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/responses.py
+-rw-r--r--   0        0        0     5288 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/settings.py
+-rw-r--r--   0        0        0     4158 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/toolbar.py
+-rw-r--r--   0        0        0      102 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/types.py
+-rw-r--r--   0        0        0     2415 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/utils.py
+-rw-r--r--   0        0        0     2996 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/__init__.py
+-rw-r--r--   0        0        0      620 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/headers.py
+-rw-r--r--   0        0        0     3425 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/logging.py
+-rw-r--r--   0        0        0     1025 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/profiling.py
+-rw-r--r--   0        0        0      970 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/redirects.py
+-rw-r--r--   0        0        0      750 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/request.py
+-rw-r--r--   0        0        0      399 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/routes.py
+-rw-r--r--   0        0        0      130 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/settings.py
+-rw-r--r--   0        0        0     6112 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/sql.py
+-rw-r--r--   0        0        0     2762 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/sqlalchemy.py
+-rw-r--r--   0        0        0     3080 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/timer.py
+-rw-r--r--   0        0        0     2850 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/tortoise.py
+-rw-r--r--   0        0        0      906 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/versions.py
+-rw-r--r--   0        0        0       45 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/css/print.css
+-rw-r--r--   0        0        0    12616 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/css/toolbar.css
+-rw-r--r--   0        0        0     1359 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/img/icon-green.svg
+-rw-r--r--   0        0        0     1359 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/img/icon-white.svg
+-rw-r--r--   0        0        0       48 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/redirect.js
+-rw-r--r--   0        0        0     1141 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/refresh.js
+-rw-r--r--   0        0        0     3007 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/timer.js
+-rw-r--r--   0        0        0     8772 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/toolbar.js
+-rw-r--r--   0        0        0     3544 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/utils.js
+-rw-r--r--   0        0        0     3249 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/versions.js
+-rw-r--r--   0        0        0     1494 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/base.html
+-rw-r--r--   0        0        0      575 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/redirect.html
+-rw-r--r--   0        0        0      805 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/includes/panel_button.html
+-rw-r--r--   0        0        0      420 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/includes/panel_content.html
+-rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/headers.html
+-rw-r--r--   0        0        0      720 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/logging.html
+-rw-r--r--   0        0        0      241 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/profiling.html
+-rw-r--r--   0        0        0     1495 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/request.html
+-rw-r--r--   0        0        0      715 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/routes.html
+-rw-r--r--   0        0        0      640 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/settings.html
+-rw-r--r--   0        0        0     3579 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/sql.html
+-rw-r--r--   0        0        0      839 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/timer.html
+-rw-r--r--   0        0        0      716 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/versions.html
+-rw-r--r--   0        0        0      135 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/.gitignore
+-rw-r--r--   0        0        0     1537 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/LICENSE
+-rw-r--r--   0        0        0     2322 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/README.md
+-rw-r--r--   0        0        0     2560 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/pyproject.toml
+-rw-r--r--   0        0        0     5100 2020-02-02 00:00:00.000000 fastapi_debug_toolbar-0.5.0/PKG-INFO
```

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/api.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/api.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/middleware.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/middleware.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/settings.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/settings.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,24 +1,30 @@
 import typing as t
 
 from jinja2 import BaseLoader, ChoiceLoader, Environment, PackageLoader
 from jinja2.ext import Extension
-from pydantic import BaseSettings, Field, IPvAnyAddress, root_validator
-from pydantic.color import Color
+from pydantic import Field, IPvAnyAddress, model_validator
+from pydantic_extra_types.color import Color
+from pydantic_settings import BaseSettings, SettingsConfigDict
 
 
 class DebugToolbarSettings(BaseSettings):
+    model_config = SettingsConfigDict(
+        title="Debug Toolbar",
+        env_prefix="DT_",
+        case_sensitive=False,
+    )
+
     DEFAULT_PANELS: t.List[str] = Field(
         [
             "debug_toolbar.panels.versions.VersionsPanel",
             "debug_toolbar.panels.timer.TimerPanel",
             "debug_toolbar.panels.settings.SettingsPanel",
             "debug_toolbar.panels.request.RequestPanel",
             "debug_toolbar.panels.headers.HeadersPanel",
-            "debug_toolbar.panels.pydantic.PydanticPanel",
             "debug_toolbar.panels.routes.RoutesPanel",
             "debug_toolbar.panels.logging.LoggingPanel",
             "debug_toolbar.panels.profiling.ProfilingPanel",
             "debug_toolbar.panels.redirects.RedirectsPanel",
         ],
         description=(
             "Specifies the full Python path to each panel that you "
@@ -125,25 +131,20 @@
         500,
         description=(
             "The SQL panel highlights queries that took more that this amount of "
             "time, in milliseconds, to execute."
         ),
     )
 
-    class Config:
-        title = "Debug Toolbar"
-        env_prefix = "DT_"
-        case_sensitive = True
-
     def __init__(self, **settings: t.Any) -> None:
         super().__init__(**settings)
         loaders = self.JINJA_LOADERS + [PackageLoader("debug_toolbar", "templates")]
         self.JINJA_ENV.loader = ChoiceLoader(loaders)
         self.JINJA_ENV.trim_blocks = True
         self.JINJA_ENV.lstrip_blocks = True
 
         for extension in self.JINJA_EXTENSIONS:
             self.JINJA_ENV.add_extension(extension)
 
-    @root_validator(pre=True)
-    def ci(cls, values: t.Dict[str, t.Any]) -> t.Dict[str, t.Any]:
-        return {k.upper(): v for k, v in values.items()}
+    @model_validator(mode="before")
+    def ci(cls, data: dict):
+        return {k.upper(): v for k, v in data.items()}
```

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/toolbar.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/toolbar.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/utils.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 import functools
 import inspect
 import sys
 import typing as t
 
 from fastapi import Request
 from fastapi.routing import APIRoute
-from pydantic.color import Color
+from pydantic_extra_types.color import Color
 from starlette.routing import Match
 
 
 def import_string(import_name: str) -> t.Any:
     try:
         __import__(import_name)
     except ImportError:
```

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/__init__.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 import typing as t
 
 from fastapi import Request, Response
-from starlette.datastructures import URL
 from starlette.middleware.base import RequestResponseEndpoint
 
 from debug_toolbar.types import ServerTiming, Stats
 from debug_toolbar.utils import get_name_from_obj
 
 if t.TYPE_CHECKING:
     from debug_toolbar.toolbar import DebugToolbar
@@ -63,19 +62,19 @@
         if self.has_content:
             return self.render(**self.get_stats())
         return ""
 
     def render(self, **context: t.Any) -> str:
         return self.toolbar.render(self.template, **context)
 
-    def url_for(self, name: str, **path_params: t.Any) -> URL:
-        return self.toolbar.request.url_for(name, **path_params)
+    def url_for(self, name: str, **path_params: t.Any) -> str:
+        return str(self.toolbar.request.url_for(name, **path_params))
 
     @property
-    def scripts(self) -> t.List[URL]:
+    def scripts(self) -> t.List[str]:
         return []
 
     async def process_request(self, request: Request) -> Response:
         return await self.call_next(request)
 
     async def generate_stats(self, request: Request, response: Response) -> Stats:
         return {}
```

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/headers.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/headers.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/logging.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/logging.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/profiling.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/profiling.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/redirects.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/redirects.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/request.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/request.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/sql.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/sql.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import re
 import typing as t
 from collections import defaultdict
 
 import sqlparse
 from fastapi import Request, Response
 from fastapi.encoders import jsonable_encoder
-from pydantic.color import Color
+from pydantic_extra_types.color import Color
 from sqlparse import tokens as T
 
 from debug_toolbar.panels import Panel
 from debug_toolbar.types import ServerTiming, Stats
 from debug_toolbar.utils import color_generator
 
 __all__ = ["SQLPanel", "parse_sql", "raw_sql"]
```

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/sqlalchemy.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/sqlalchemy.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/timer.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/timer.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 import typing as t
 from time import perf_counter
 
 from fastapi import Request, Response
-from starlette.datastructures import URL
 
 from debug_toolbar.panels import Panel
 from debug_toolbar.types import ServerTiming, Stats
 
 try:
     import resource
 except ImportError:
@@ -42,15 +41,15 @@
                 "Context switches",
                 f"{stats['vcsw']} voluntary, {stats['ivcsw']} involuntary",
             ),
         )
         return self.render(rows=rows)
 
     @property
-    def scripts(self) -> t.List[URL]:
+    def scripts(self) -> t.List[str]:
         scripts = super().scripts
         scripts.append(self.url_for("debug_toolbar.static", path="js/timer.js"))
         return scripts
 
     async def process_request(self, request: Request) -> Response:
         self._start_time = perf_counter()
         if self.has_content:
```

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/tortoise.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/tortoise.py`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/panels/versions.py` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/panels/versions.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,26 +1,25 @@
 import typing as t
 
 from fastapi import Request, Response, __version__
-from starlette.datastructures import URL
 
 from debug_toolbar.panels import Panel
 from debug_toolbar.types import Stats
 
 
 class VersionsPanel(Panel):
     title = "Versions"
     template = "panels/versions.html"
 
     @property
     def nav_subtitle(self) -> str:
         return f"FastAPI {__version__}"
 
     @property
-    def scripts(self) -> t.List[URL]:
+    def scripts(self) -> t.List[str]:
         scripts = super().scripts
         scripts.append(self.url_for("debug_toolbar.static", path="js/versions.js"))
         return scripts
 
     async def generate_stats(self, request: Request, response: Response) -> Stats:
         try:
             import pkg_resources
```

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/css/toolbar.css` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/css/toolbar.css`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/img/icon-green.svg` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/img/icon-green.svg`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/img/icon-white.svg` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/img/icon-white.svg`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/refresh.js` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/refresh.js`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/timer.js` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/timer.js`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/toolbar.js` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/toolbar.js`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/utils.js` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/utils.js`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/statics/js/versions.js` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/statics/js/versions.js`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/base.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/base.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/redirect.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/redirect.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/includes/panel_button.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/includes/panel_button.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/headers.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/headers.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/logging.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/logging.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/request.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/request.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/routes.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/routes.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/sql.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/sql.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/timer.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/timer.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/debug_toolbar/templates/panels/versions.html` & `fastapi_debug_toolbar-0.5.0/debug_toolbar/templates/panels/versions.html`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/LICENSE` & `fastapi_debug_toolbar-0.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/README.md` & `fastapi_debug_toolbar-0.5.0/README.md`

 * *Files identical despite different names*

### Comparing `fastapi_debug_toolbar-0.4.0/pyproject.toml` & `fastapi_debug_toolbar-0.5.0/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -41,14 +41,17 @@
     "Topic :: Utilities",
 ]
 
 dependencies = [
     "fastapi >=0.70.0",
     "anyio >=3.0.0",
     "Jinja2 >=2.9",
+    "pydantic >=2.0",
+    "pydantic-extra-types >=2.0.0",
+    "pydantic-settings >=2.0.0",
     "pyinstrument >=3.0.0",
     "sqlparse >=0.2.0",
 ]
 
 [project.urls]
 homepage = "https://github.com/mongkok/fastapi-debug-toolbar"
 repository = "https://github.com/mongkok/fastapi-debug-toolbar"
```

### Comparing `fastapi_debug_toolbar-0.4.0/PKG-INFO` & `fastapi_debug_toolbar-0.5.0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fastapi-debug-toolbar
-Version: 0.4.0
+Version: 0.5.0
 Summary: A debug toolbar for FastAPI.
 Project-URL: homepage, https://github.com/mongkok/fastapi-debug-toolbar
 Project-URL: repository, https://github.com/mongkok/fastapi-debug-toolbar
 Project-URL: documentation, https://fastapi-debug-toolbar.domake.io
 Project-URL: changelog, https://fastapi-debug-toolbar.domake.io/changelog/
 Author-email: Dani <dani@domake.io>
 License-Expression: BSD-3-Clause
@@ -34,14 +34,17 @@
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Classifier: Topic :: Utilities
 Classifier: Typing :: Typed
 Requires-Python: >=3.7
 Requires-Dist: anyio>=3.0.0
 Requires-Dist: fastapi>=0.70.0
 Requires-Dist: jinja2>=2.9
+Requires-Dist: pydantic-extra-types>=2.0.0
+Requires-Dist: pydantic-settings>=2.0.0
+Requires-Dist: pydantic>=2.0
 Requires-Dist: pyinstrument>=3.0.0
 Requires-Dist: sqlparse>=0.2.0
 Provides-Extra: doc
 Requires-Dist: markdown-include; extra == 'doc'
 Requires-Dist: mkdocs; extra == 'doc'
 Requires-Dist: mkdocs-material; extra == 'doc'
 Requires-Dist: mkdocstrings[python]; extra == 'doc'
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: fastapi-debug-toolbar Version: 0.4.0 Summary: A
+Metadata-Version: 2.1 Name: fastapi-debug-toolbar Version: 0.5.0 Summary: A
 debug toolbar for FastAPI. Project-URL: homepage, https://github.com/mongkok/
 fastapi-debug-toolbar Project-URL: repository, https://github.com/mongkok/
 fastapi-debug-toolbar Project-URL: documentation, https://fastapi-debug-
 toolbar.domake.io Project-URL: changelog, https://fastapi-debug-
 toolbar.domake.io/changelog/ Author-email: Dani
 domake.io> License-Expression: BSD-3-Clause License-File: LICENSE Keywords:
 debug,fastapi,profiling Classifier: Development Status :: 2 - Pre-Alpha
@@ -17,29 +17,31 @@
 Programming Language :: Python :: 3.11 Classifier: Topic :: Internet
 Classifier: Topic :: Internet :: WWW/HTTP Classifier: Topic :: Internet :: WWW/
 HTTP :: HTTP Servers Classifier: Topic :: Software Development Classifier:
 Topic :: Software Development :: Debuggers Classifier: Topic :: Software
 Development :: Libraries Classifier: Topic :: Software Development :: Libraries
 :: Python Modules Classifier: Topic :: Utilities Classifier: Typing :: Typed
 Requires-Python: >=3.7 Requires-Dist: anyio>=3.0.0 Requires-Dist:
-fastapi>=0.70.0 Requires-Dist: jinja2>=2.9 Requires-Dist: pyinstrument>=3.0.0
-Requires-Dist: sqlparse>=0.2.0 Provides-Extra: doc Requires-Dist: markdown-
-include; extra == 'doc' Requires-Dist: mkdocs; extra == 'doc' Requires-Dist:
-mkdocs-material; extra == 'doc' Requires-Dist: mkdocstrings[python]; extra ==
-'doc' Provides-Extra: test Requires-Dist: black; extra == 'test' Requires-Dist:
-codecov; extra == 'test' Requires-Dist: flake8; extra == 'test' Requires-Dist:
-httpx; extra == 'test' Requires-Dist: isort; extra == 'test' Requires-Dist:
-itsdangerous; extra == 'test' Requires-Dist: mypy; extra == 'test' Requires-
-Dist: pytest; extra == 'test' Requires-Dist: pytest-asyncio; extra == 'test'
-Requires-Dist: pytest-cov; extra == 'test' Requires-Dist: python-multipart;
-extra == 'test' Requires-Dist: sqlalchemy; extra == 'test' Requires-Dist:
-tortoise-orm>=0.19.0; extra == 'test' Requires-Dist: types-setuptools; extra ==
-'test' Description-Content-Type: text/markdown # ![FastAPI](https://
-raw.githubusercontent.com/mongkok/fastapi-debug-toolbar/main/debug_toolbar/
-statics/img/icon-green.svg) Debug Toolbar
+fastapi>=0.70.0 Requires-Dist: jinja2>=2.9 Requires-Dist: pydantic-extra-
+types>=2.0.0 Requires-Dist: pydantic-settings>=2.0.0 Requires-Dist:
+pydantic>=2.0 Requires-Dist: pyinstrument>=3.0.0 Requires-Dist: sqlparse>=0.2.0
+Provides-Extra: doc Requires-Dist: markdown-include; extra == 'doc' Requires-
+Dist: mkdocs; extra == 'doc' Requires-Dist: mkdocs-material; extra == 'doc'
+Requires-Dist: mkdocstrings[python]; extra == 'doc' Provides-Extra: test
+Requires-Dist: black; extra == 'test' Requires-Dist: codecov; extra == 'test'
+Requires-Dist: flake8; extra == 'test' Requires-Dist: httpx; extra == 'test'
+Requires-Dist: isort; extra == 'test' Requires-Dist: itsdangerous; extra ==
+'test' Requires-Dist: mypy; extra == 'test' Requires-Dist: pytest; extra ==
+'test' Requires-Dist: pytest-asyncio; extra == 'test' Requires-Dist: pytest-
+cov; extra == 'test' Requires-Dist: python-multipart; extra == 'test' Requires-
+Dist: sqlalchemy; extra == 'test' Requires-Dist: tortoise-orm>=0.19.0; extra ==
+'test' Requires-Dist: types-setuptools; extra == 'test' Description-Content-
+Type: text/markdown # ![FastAPI](https://raw.githubusercontent.com/mongkok/
+fastapi-debug-toolbar/main/debug_toolbar/statics/img/icon-green.svg) Debug
+Toolbar
                             [FastAPI_Debug_Toolbar]
 ðA debug toolbar for FastAPI based on the original django-debug-toolbar.ð
 
                       Swagger UI & GraphQL are supported.
                  [Test] [Coverage] [Codacy] [Package_version]
 --- **Documentation**: [https://fastapi-debug-toolbar.domake.io](https://
 fastapi-debug-toolbar.domake.io) --- ## Installation ```sh pip install fastapi-
```

