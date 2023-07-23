# Comparing `tmp/aiogram_i18n-1.1.tar.gz` & `tmp/aiogram_i18n-1.2.tar.gz`

## Comparing `aiogram_i18n-1.1.tar` & `aiogram_i18n-1.2.tar`

### file list

```diff
@@ -1,42 +1,43 @@
--rw-r--r--   0        0        0     1251 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/.github/workflows/python-package-tests.yml
--rw-r--r--   0        0        0     1757 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/.github/workflows/python-publish.yml
--rw-r--r--   0        0        0     2096 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/.github/workflows/tests.yml
--rw-r--r--   0        0        0      254 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/__init__.py
--rw-r--r--   0        0        0     2451 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/__main__.py
--rw-r--r--   0        0        0     1547 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/context.py
--rw-r--r--   0        0        0     1678 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/exceptions.py
--rw-r--r--   0        0        0     2052 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/middleware.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/py.typed
--rw-r--r--   0        0        0    22198 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/types.py
--rw-r--r--   0        0        0      757 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/cores/__init__.py
--rw-r--r--   0        0        0     2496 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/cores/base.py
--rw-r--r--   0        0        0     2128 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/cores/fluent_compile_core.py
--rw-r--r--   0        0        0     2600 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/cores/fluent_runtime_core.py
--rw-r--r--   0        0        0     1105 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/cores/gnu_text_core.py
--rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/lazy/__init__.py
--rw-r--r--   0        0        0      638 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/lazy/factory.py
--rw-r--r--   0        0        0     2388 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/lazy/proxy.py
--rw-r--r--   0        0        0      161 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/managers/__init__.py
--rw-r--r--   0        0        0      770 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/managers/base.py
--rw-r--r--   0        0        0      451 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/managers/const.py
--rw-r--r--   0        0        0      974 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/managers/fsm.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/utils/__init__.py
--rw-r--r--   0        0        0      349 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/utils/fluent_extract/__init__.py
--rw-r--r--   0        0        0     2660 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/utils/fluent_extract/models.py
--rw-r--r--   0        0        0     3162 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/utils/fluent_extract/parser.py
--rw-r--r--   0        0        0     2700 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/utils/fluent_stub/__init__.py
--rw-r--r--   0        0        0     1199 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/aiogram_i18n/utils/fluent_stub/visitor.py
--rw-r--r--   0        0        0     1618 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/examples/mre.py
--rw-r--r--   0        0        0      493 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/examples/stub.pyi
--rw-r--r--   0        0        0       99 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/examples/locales/en/LC_MESSAGES/mybot.ftl
--rw-r--r--   0        0        0      114 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/examples/locales/uk/LC_MESSAGES/mybot.ftl
--rw-r--r--   0        0        0     2383 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/tests/conftest.py
--rw-r--r--   0        0        0      748 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/tests/test_cores.py
--rw-r--r--   0        0        0       87 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/tests/data/locales/en/LC_MESSAGES/mybot.ftl
--rw-r--r--   0        0        0      555 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/tests/data/locales/en/LC_MESSAGES/mybot.mo
--rw-r--r--   0        0        0       90 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/tests/data/locales/uk/LC_MESSAGES/mybot.ftl
--rw-r--r--   0        0        0      632 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/tests/data/locales/uk/LC_MESSAGES/mybot.mo
--rw-r--r--   0        0        0       79 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/.gitignore
--rw-r--r--   0        0        0     1816 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/README.md
--rw-r--r--   0        0        0     1192 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/pyproject.toml
--rw-r--r--   0        0        0     2766 2020-02-02 00:00:00.000000 aiogram_i18n-1.1/PKG-INFO
+-rw-r--r--   0        0        0     1251 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/.github/workflows/python-package-tests.yml
+-rw-r--r--   0        0        0     1757 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/.github/workflows/python-publish.yml
+-rw-r--r--   0        0        0     2096 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/.github/workflows/tests.yml
+-rw-r--r--   0        0        0      254 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/__init__.py
+-rw-r--r--   0        0        0     2451 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/__main__.py
+-rw-r--r--   0        0        0     1612 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/context.py
+-rw-r--r--   0        0        0     1678 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/exceptions.py
+-rw-r--r--   0        0        0     2340 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/middleware.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/py.typed
+-rw-r--r--   0        0        0    18754 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/types.py
+-rw-r--r--   0        0        0      757 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/cores/__init__.py
+-rw-r--r--   0        0        0     2579 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/cores/base.py
+-rw-r--r--   0        0        0     2079 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/cores/fluent_compile_core.py
+-rw-r--r--   0        0        0     2685 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/cores/fluent_runtime_core.py
+-rw-r--r--   0        0        0     1110 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/cores/gnu_text_core.py
+-rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/lazy/__init__.py
+-rw-r--r--   0        0        0      757 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/lazy/factory.py
+-rw-r--r--   0        0        0     2348 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/lazy/proxy.py
+-rw-r--r--   0        0        0      161 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/managers/__init__.py
+-rw-r--r--   0        0        0      800 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/managers/base.py
+-rw-r--r--   0        0        0      468 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/managers/const.py
+-rw-r--r--   0        0        0     1023 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/managers/fsm.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/utils/__init__.py
+-rw-r--r--   0        0        0      602 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/utils/magic_proxy.py
+-rw-r--r--   0        0        0      349 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/utils/fluent_extract/__init__.py
+-rw-r--r--   0        0        0     2660 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/utils/fluent_extract/models.py
+-rw-r--r--   0        0        0     3162 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/utils/fluent_extract/parser.py
+-rw-r--r--   0        0        0     2687 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/utils/fluent_stub/__init__.py
+-rw-r--r--   0        0        0     1199 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/aiogram_i18n/utils/fluent_stub/visitor.py
+-rw-r--r--   0        0        0     1618 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/examples/mre.py
+-rw-r--r--   0        0        0      493 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/examples/stub.pyi
+-rw-r--r--   0        0        0       99 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/examples/locales/en/LC_MESSAGES/mybot.ftl
+-rw-r--r--   0        0        0      114 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/examples/locales/uk/LC_MESSAGES/mybot.ftl
+-rw-r--r--   0        0        0     2383 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/tests/conftest.py
+-rw-r--r--   0        0        0      753 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/tests/test_cores.py
+-rw-r--r--   0        0        0       87 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/tests/data/locales/en/LC_MESSAGES/mybot.ftl
+-rw-r--r--   0        0        0      555 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/tests/data/locales/en/LC_MESSAGES/mybot.mo
+-rw-r--r--   0        0        0       90 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/tests/data/locales/uk/LC_MESSAGES/mybot.ftl
+-rw-r--r--   0        0        0      632 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/tests/data/locales/uk/LC_MESSAGES/mybot.mo
+-rw-r--r--   0        0        0       79 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/.gitignore
+-rw-r--r--   0        0        0     1816 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/README.md
+-rw-r--r--   0        0        0     1249 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/pyproject.toml
+-rw-r--r--   0        0        0     2873 2020-02-02 00:00:00.000000 aiogram_i18n-1.2/PKG-INFO
```

### Comparing `aiogram_i18n-1.1/.github/workflows/python-package-tests.yml` & `aiogram_i18n-1.2/.github/workflows/python-package-tests.yml`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/.github/workflows/python-publish.yml` & `aiogram_i18n-1.2/.github/workflows/python-publish.yml`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/.github/workflows/tests.yml` & `aiogram_i18n-1.2/.github/workflows/tests.yml`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/aiogram_i18n/__main__.py` & `aiogram_i18n-1.2/aiogram_i18n/__main__.py`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/aiogram_i18n/context.py` & `aiogram_i18n-1.2/aiogram_i18n/context.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from contextlib import contextmanager
-from functools import partial
-from typing import Dict, Any, Generator, Callable
+from typing import Dict, Any, Generator
 
 from aiogram.utils.mixins import ContextInstanceMixin
 
 from aiogram_i18n.cores.base import BaseCore
 from aiogram_i18n.managers.base import BaseManager
+from aiogram_i18n.utils.magic_proxy import MagicProxy
 
 
 class I18nContext(ContextInstanceMixin["I18nContext"]):
     locale: str
     core: BaseCore[Any]
     manager: BaseManager
     data: Dict[str, Any]
@@ -26,26 +26,29 @@
         self.manager = manager
         self.data = data
         self.key_separator = key_separator
 
     def get(self, key: str, /, **kwargs: Any) -> str:
         return self.core.get(key, locale=self.locale, **kwargs)
 
+    __call__ = get
+
+    def __getattr__(self, item: str) -> MagicProxy[str]:
+        proxy = MagicProxy(self, key_separator=self.key_separator)
+        return proxy.__getattr__(item)
+
     async def set_locale(self, locale: str, **kwargs: Any) -> None:
         await self.manager.set_locale_mixin.call(
             locale,
             core=self.core,
             manager=self.manager,
             **self.data, **kwargs
         )
         self.locale = locale
 
-    def __getattr__(self, item: str) -> Callable[..., str]:
-        return partial(self.get, item.replace("_", self.key_separator))
-
     @contextmanager
     def use_locale(self, locale: str) -> Generator["I18nContext", None, None]:
         old_locale = self.locale
         self.locale = locale
         try:
             yield self
         finally:
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/exceptions.py` & `aiogram_i18n-1.2/aiogram_i18n/exceptions.py`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/aiogram_i18n/middleware.py` & `aiogram_i18n-1.2/aiogram_i18n/middleware.py`

 * *Files 12% similar despite different names*

```diff
@@ -11,34 +11,40 @@
 
 class I18nMiddleware(BaseMiddleware):
     core: BaseCore[Any]
     manager: BaseManager
     context_key: str
     locale_key: str
     middleware_key: str
-    default_locale: str
     key_separator: str
+    with_context: bool
 
     def __init__(
         self,
         core: BaseCore[Any],
         manager: Optional[BaseManager] = None,
         context_key: str = "i18n",
-        locale_key: str = "locale",
+        locale_key: Optional[str] = None,
         middleware_key: str = "i18n_middleware",
         default_locale: str = "en",
-        key_separator: str = "-"
+        key_separator: str = "-",
+        with_context: bool = True
     ) -> None:
         self.core = core
-        self.manager = manager or FSMManager(default_locale=default_locale, key=locale_key)
+        self.manager = manager or FSMManager(key=locale_key)
         self.context_key = context_key
         self.locale_key = locale_key
         self.middleware_key = middleware_key
-        self.default_locale = default_locale
         self.key_separator = key_separator
+        self.with_context = with_context
+
+        if self.core.default_locale is None:
+            self.core.default_locale = default_locale
+        if self.manager.default_locale is None:
+            self.manager.default_locale = default_locale
 
     def setup(self, dispatcher: Dispatcher) -> None:
         dispatcher.update.outer_middleware.register(self)
         dispatcher.startup.register(self.core.startup)
         dispatcher.shutdown.register(self.core.shutdown)
 
     async def __call__(
@@ -51,12 +57,14 @@
         data[self.context_key] = context = I18nContext(
             locale=locale,
             core=self.core,
             manager=self.manager,
             data=data,
             key_separator=self.key_separator
         )
-        data[self.locale_key] = locale
+        if self.locale_key is not None:
+            data[self.locale_key] = locale
         data[self.middleware_key] = self
 
-        I18nContext.set_current(context)
+        if self.with_context:
+            I18nContext.set_current(context)
         return await handler(event, data)
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/types.py` & `aiogram_i18n-1.2/aiogram_i18n/types.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,485 +1,463 @@
 """
 All mutable models from aiogram are listed here and LazyProxy is allowed in string fields.
 This code is generated automatically.
 """
 from __future__ import annotations
 
-from typing import Optional
+from typing import Optional, List, Union, Literal
 
-from aiogram.types import (
-    BotCommand as _BotCommand,
-    ChatPermissions as _ChatPermissions,
-    ErrorEvent as _ErrorEvent,
-    ForceReply as _ForceReply,
-    InlineKeyboardButton as _InlineKeyboardButton,
-    InlineKeyboardMarkup as _InlineKeyboardMarkup,
-    InlineQueryResult as _InlineQueryResult,
-    InlineQueryResultArticle as _InlineQueryResultArticle,
-    InlineQueryResultAudio as _InlineQueryResultAudio,
-    InlineQueryResultCachedAudio as _InlineQueryResultCachedAudio,
-    InlineQueryResultCachedDocument as _InlineQueryResultCachedDocument,
-    InlineQueryResultCachedGif as _InlineQueryResultCachedGif,
-    InlineQueryResultCachedMpeg4Gif as _InlineQueryResultCachedMpeg4Gif,
-    InlineQueryResultCachedPhoto as _InlineQueryResultCachedPhoto,
-    InlineQueryResultCachedSticker as _InlineQueryResultCachedSticker,
-    InlineQueryResultCachedVideo as _InlineQueryResultCachedVideo,
-    InlineQueryResultCachedVoice as _InlineQueryResultCachedVoice,
-    InlineQueryResultContact as _InlineQueryResultContact,
-    InlineQueryResultDocument as _InlineQueryResultDocument,
-    InlineQueryResultGame as _InlineQueryResultGame,
-    InlineQueryResultGif as _InlineQueryResultGif,
-    InlineQueryResultLocation as _InlineQueryResultLocation,
-    InlineQueryResultMpeg4Gif as _InlineQueryResultMpeg4Gif,
-    InlineQueryResultPhoto as _InlineQueryResultPhoto,
-    InlineQueryResultVenue as _InlineQueryResultVenue,
-    InlineQueryResultVideo as _InlineQueryResultVideo,
-    InlineQueryResultVoice as _InlineQueryResultVoice,
-    InputContactMessageContent as _InputContactMessageContent,
-    InputInvoiceMessageContent as _InputInvoiceMessageContent,
-    InputLocationMessageContent as _InputLocationMessageContent,
-    InputMedia as _InputMedia,
-    InputMediaAnimation as _InputMediaAnimation,
-    InputMediaAudio as _InputMediaAudio,
-    InputMediaDocument as _InputMediaDocument,
-    InputMediaPhoto as _InputMediaPhoto,
-    InputMediaVideo as _InputMediaVideo,
-    InputMessageContent as _InputMessageContent,
-    InputTextMessageContent as _InputTextMessageContent,
-    InputVenueMessageContent as _InputVenueMessageContent,
-    KeyboardButton as _KeyboardButton,
-    KeyboardButtonPollType as _KeyboardButtonPollType,
-    LabeledPrice as _LabeledPrice,
-    MenuButton as _MenuButton,
-    MenuButtonCommands as _MenuButtonCommands,
-    MenuButtonDefault as _MenuButtonDefault,
-    MenuButtonWebApp as _MenuButtonWebApp,
-    MessageEntity as _MessageEntity,
-    PassportElementError as _PassportElementError,
-    PassportElementErrorDataField as _PassportElementErrorDataField,
-    PassportElementErrorFile as _PassportElementErrorFile,
-    PassportElementErrorFiles as _PassportElementErrorFiles,
-    PassportElementErrorFrontSide as _PassportElementErrorFrontSide,
-    PassportElementErrorReverseSide as _PassportElementErrorReverseSide,
-    PassportElementErrorSelfie as _PassportElementErrorSelfie,
-    PassportElementErrorTranslationFile as _PassportElementErrorTranslationFile,
-    PassportElementErrorTranslationFiles as _PassportElementErrorTranslationFiles,
-    PassportElementErrorUnspecified as _PassportElementErrorUnspecified,
-    ReplyKeyboardMarkup as _ReplyKeyboardMarkup,
-    ReplyKeyboardRemove as _ReplyKeyboardRemove,
-)
+from aiogram import types
 
 from aiogram_i18n.lazy import LazyProxy
 
 
-class BotCommand(_BotCommand):
+class BotCommand(types.BotCommand):
     command: str | LazyProxy  # type: ignore[assignment]
     description: str | LazyProxy  # type: ignore[assignment]
 
 
-class ChatPermissions(_ChatPermissions):
+class ChatPermissions(types.ChatPermissions):
     ...
 
 
-class ErrorEvent(_ErrorEvent):
-    ...
-
-
-class ForceReply(_ForceReply):
+class ForceReply(types.ForceReply):
     input_field_placeholder: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineKeyboardButton(_InlineKeyboardButton):
+class InlineKeyboardButton(types.InlineKeyboardButton):
     text: str | LazyProxy  # type: ignore[assignment]
     url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     callback_data: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     switch_inline_query: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     switch_inline_query_current_chat: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineKeyboardMarkup(_InlineKeyboardMarkup):
+class InlineKeyboardMarkup(types.InlineKeyboardMarkup):
     ...
 
 
-class InlineQueryResult(_InlineQueryResult):
+class InlineQueryResult(types.InlineQueryResult):
     ...
 
 
-class InlineQueryResultArticle(_InlineQueryResultArticle):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultArticle(types.InlineQueryResultArticle):
     id: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
     url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     description: Optional[str | LazyProxy] = None  # type: ignore[assignment]
-    thumb_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+    thumbnail_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultAudio(_InlineQueryResultAudio):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultAudio(types.InlineQueryResultAudio):
     id: str | LazyProxy  # type: ignore[assignment]
     audio_url: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     performer: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultCachedAudio(_InlineQueryResultCachedAudio):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultCachedAudio(types.InlineQueryResultCachedAudio):
     id: str | LazyProxy  # type: ignore[assignment]
     audio_file_id: str | LazyProxy  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultCachedDocument(_InlineQueryResultCachedDocument):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultCachedDocument(types.InlineQueryResultCachedDocument):
     id: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
     document_file_id: str | LazyProxy  # type: ignore[assignment]
     description: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultCachedGif(_InlineQueryResultCachedGif):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultCachedGif(types.InlineQueryResultCachedGif):
     id: str | LazyProxy  # type: ignore[assignment]
     gif_file_id: str | LazyProxy  # type: ignore[assignment]
     title: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultCachedMpeg4Gif(_InlineQueryResultCachedMpeg4Gif):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultCachedMpeg4Gif(types.InlineQueryResultCachedMpeg4Gif):
     id: str | LazyProxy  # type: ignore[assignment]
     mpeg4_file_id: str | LazyProxy  # type: ignore[assignment]
     title: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultCachedPhoto(_InlineQueryResultCachedPhoto):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultCachedPhoto(types.InlineQueryResultCachedPhoto):
     id: str | LazyProxy  # type: ignore[assignment]
     photo_file_id: str | LazyProxy  # type: ignore[assignment]
     title: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     description: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultCachedSticker(_InlineQueryResultCachedSticker):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultCachedSticker(types.InlineQueryResultCachedSticker):
     id: str | LazyProxy  # type: ignore[assignment]
     sticker_file_id: str | LazyProxy  # type: ignore[assignment]
 
 
-class InlineQueryResultCachedVideo(_InlineQueryResultCachedVideo):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultCachedVideo(types.InlineQueryResultCachedVideo):
     id: str | LazyProxy  # type: ignore[assignment]
     video_file_id: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
     description: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultCachedVoice(_InlineQueryResultCachedVoice):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultCachedVoice(types.InlineQueryResultCachedVoice):
     id: str | LazyProxy  # type: ignore[assignment]
     voice_file_id: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultContact(_InlineQueryResultContact):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultContact(types.InlineQueryResultContact):
     id: str | LazyProxy  # type: ignore[assignment]
     phone_number: str | LazyProxy  # type: ignore[assignment]
     first_name: str | LazyProxy  # type: ignore[assignment]
     last_name: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     vcard: Optional[str | LazyProxy] = None  # type: ignore[assignment]
-    thumb_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+    thumbnail_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultDocument(_InlineQueryResultDocument):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultDocument(types.InlineQueryResultDocument):
     id: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
     document_url: str | LazyProxy  # type: ignore[assignment]
     mime_type: str | LazyProxy  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     description: Optional[str | LazyProxy] = None  # type: ignore[assignment]
-    thumb_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+    thumbnail_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultGame(_InlineQueryResultGame):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultGame(types.InlineQueryResultGame):
     id: str | LazyProxy  # type: ignore[assignment]
     game_short_name: str | LazyProxy  # type: ignore[assignment]
 
 
-class InlineQueryResultGif(_InlineQueryResultGif):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultGif(types.InlineQueryResultGif):
     id: str | LazyProxy  # type: ignore[assignment]
     gif_url: str | LazyProxy  # type: ignore[assignment]
-    thumb_url: str | LazyProxy  # type: ignore[assignment]
-    thumb_mime_type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+    thumbnail_url: str | LazyProxy  # type: ignore[assignment]
+    thumbnail_mime_type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     title: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultLocation(_InlineQueryResultLocation):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultLocation(types.InlineQueryResultLocation):
     id: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
-    thumb_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+    thumbnail_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultMpeg4Gif(_InlineQueryResultMpeg4Gif):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultMpeg4Gif(types.InlineQueryResultMpeg4Gif):
     id: str | LazyProxy  # type: ignore[assignment]
     mpeg4_url: str | LazyProxy  # type: ignore[assignment]
-    thumb_url: str | LazyProxy  # type: ignore[assignment]
-    thumb_mime_type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+    thumbnail_url: str | LazyProxy  # type: ignore[assignment]
+    thumbnail_mime_type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     title: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultPhoto(_InlineQueryResultPhoto):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultPhoto(types.InlineQueryResultPhoto):
     id: str | LazyProxy  # type: ignore[assignment]
     photo_url: str | LazyProxy  # type: ignore[assignment]
-    thumb_url: str | LazyProxy  # type: ignore[assignment]
+    thumbnail_url: str | LazyProxy  # type: ignore[assignment]
     title: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     description: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultVenue(_InlineQueryResultVenue):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultVenue(types.InlineQueryResultVenue):
     id: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
     address: str | LazyProxy  # type: ignore[assignment]
     foursquare_id: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     foursquare_type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     google_place_id: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     google_place_type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
-    thumb_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+    thumbnail_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultVideo(_InlineQueryResultVideo):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultVideo(types.InlineQueryResultVideo):
     id: str | LazyProxy  # type: ignore[assignment]
     video_url: str | LazyProxy  # type: ignore[assignment]
     mime_type: str | LazyProxy  # type: ignore[assignment]
-    thumb_url: str | LazyProxy  # type: ignore[assignment]
+    thumbnail_url: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     description: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InlineQueryResultVoice(_InlineQueryResultVoice):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InlineQueryResultVoice(types.InlineQueryResultVoice):
     id: str | LazyProxy  # type: ignore[assignment]
     voice_url: str | LazyProxy  # type: ignore[assignment]
     title: str | LazyProxy  # type: ignore[assignment]
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InputContactMessageContent(_InputContactMessageContent):
+class InputContactMessageContent(types.InputContactMessageContent):
     phone_number: str | LazyProxy  # type: ignore[assignment]
     first_name: str | LazyProxy  # type: ignore[assignment]
     last_name: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     vcard: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InputInvoiceMessageContent(_InputInvoiceMessageContent):
+class InputInvoiceMessageContent(types.InputInvoiceMessageContent):
     title: str | LazyProxy  # type: ignore[assignment]
     description: str | LazyProxy  # type: ignore[assignment]
     payload: str | LazyProxy  # type: ignore[assignment]
     provider_token: str | LazyProxy  # type: ignore[assignment]
     currency: str | LazyProxy  # type: ignore[assignment]
     provider_data: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     photo_url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InputLocationMessageContent(_InputLocationMessageContent):
+class InputLocationMessageContent(types.InputLocationMessageContent):
     ...
 
 
-class InputMedia(_InputMedia):
+class InputMedia(types.InputMedia):
     ...
 
 
-class InputMediaAnimation(_InputMediaAnimation):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InputMediaAnimation(types.InputMediaAnimation):
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InputMediaAudio(_InputMediaAudio):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InputMediaAudio(types.InputMediaAudio):
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     performer: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     title: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InputMediaDocument(_InputMediaDocument):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InputMediaDocument(types.InputMediaDocument):
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InputMediaPhoto(_InputMediaPhoto):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InputMediaPhoto(types.InputMediaPhoto):
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InputMediaVideo(_InputMediaVideo):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class InputMediaVideo(types.InputMediaVideo):
     caption: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InputMessageContent(_InputMessageContent):
+class InputMessageContent(types.InputMessageContent):
     ...
 
 
-class InputTextMessageContent(_InputTextMessageContent):
+class InputTextMessageContent(types.InputTextMessageContent):
     message_text: str | LazyProxy  # type: ignore[assignment]
     parse_mode: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class InputVenueMessageContent(_InputVenueMessageContent):
+class InputVenueMessageContent(types.InputVenueMessageContent):
     title: str | LazyProxy  # type: ignore[assignment]
     address: str | LazyProxy  # type: ignore[assignment]
     foursquare_id: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     foursquare_type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     google_place_id: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     google_place_type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class KeyboardButton(_KeyboardButton):
+class KeyboardButton(types.KeyboardButton):
     text: str | LazyProxy  # type: ignore[assignment]
 
 
-class KeyboardButtonPollType(_KeyboardButtonPollType):
+class KeyboardButtonPollType(types.KeyboardButtonPollType):
     type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class LabeledPrice(_LabeledPrice):
+class LabeledPrice(types.LabeledPrice):
     label: str | LazyProxy  # type: ignore[assignment]
 
 
-class MenuButton(_MenuButton):
+class MenuButton(types.MenuButton):
     type: str | LazyProxy  # type: ignore[assignment]
     text: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class MenuButtonCommands(_MenuButtonCommands):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class MenuButtonCommands(types.MenuButtonCommands):
     text: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class MenuButtonDefault(_MenuButtonDefault):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class MenuButtonDefault(types.MenuButtonDefault):
     text: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class MenuButtonWebApp(_MenuButtonWebApp):
-    type: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class MenuButtonWebApp(types.MenuButtonWebApp):
     text: str | LazyProxy  # type: ignore[assignment]
 
 
-class MessageEntity(_MessageEntity):
+class MessageEntity(types.MessageEntity):
     type: str | LazyProxy  # type: ignore[assignment]
     url: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     language: Optional[str | LazyProxy] = None  # type: ignore[assignment]
     custom_emoji_id: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class PassportElementError(_PassportElementError):
+class PassportElementError(types.PassportElementError):
     ...
 
 
-class PassportElementErrorDataField(_PassportElementErrorDataField):
-    source: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class PassportElementErrorDataField(types.PassportElementErrorDataField):
     type: str | LazyProxy  # type: ignore[assignment]
     field_name: str | LazyProxy  # type: ignore[assignment]
     data_hash: str | LazyProxy  # type: ignore[assignment]
     message: str | LazyProxy  # type: ignore[assignment]
 
 
-class PassportElementErrorFile(_PassportElementErrorFile):
-    source: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class PassportElementErrorFile(types.PassportElementErrorFile):
     type: str | LazyProxy  # type: ignore[assignment]
     file_hash: str | LazyProxy  # type: ignore[assignment]
     message: str | LazyProxy  # type: ignore[assignment]
 
 
-class PassportElementErrorFiles(_PassportElementErrorFiles):
-    source: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class PassportElementErrorFiles(types.PassportElementErrorFiles):
     type: str | LazyProxy  # type: ignore[assignment]
-    file_hashes: str | LazyProxy  # type: ignore[assignment]
     message: str | LazyProxy  # type: ignore[assignment]
 
 
-class PassportElementErrorFrontSide(_PassportElementErrorFrontSide):
-    source: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class PassportElementErrorFrontSide(types.PassportElementErrorFrontSide):
     type: str | LazyProxy  # type: ignore[assignment]
     file_hash: str | LazyProxy  # type: ignore[assignment]
     message: str | LazyProxy  # type: ignore[assignment]
 
 
-class PassportElementErrorReverseSide(_PassportElementErrorReverseSide):
-    source: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class PassportElementErrorReverseSide(types.PassportElementErrorReverseSide):
     type: str | LazyProxy  # type: ignore[assignment]
     file_hash: str | LazyProxy  # type: ignore[assignment]
     message: str | LazyProxy  # type: ignore[assignment]
 
 
-class PassportElementErrorSelfie(_PassportElementErrorSelfie):
-    source: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class PassportElementErrorSelfie(types.PassportElementErrorSelfie):
     type: str | LazyProxy  # type: ignore[assignment]
     file_hash: str | LazyProxy  # type: ignore[assignment]
     message: str | LazyProxy  # type: ignore[assignment]
 
 
-class PassportElementErrorTranslationFile(_PassportElementErrorTranslationFile):
-    source: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class PassportElementErrorTranslationFile(types.PassportElementErrorTranslationFile):
     type: str | LazyProxy  # type: ignore[assignment]
     file_hash: str | LazyProxy  # type: ignore[assignment]
     message: str | LazyProxy  # type: ignore[assignment]
 
 
-class PassportElementErrorTranslationFiles(_PassportElementErrorTranslationFiles):
-    source: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class PassportElementErrorTranslationFiles(types.PassportElementErrorTranslationFiles):
     type: str | LazyProxy  # type: ignore[assignment]
-    file_hashes: str | LazyProxy  # type: ignore[assignment]
     message: str | LazyProxy  # type: ignore[assignment]
 
 
-class PassportElementErrorUnspecified(_PassportElementErrorUnspecified):
-    source: Optional[str | LazyProxy] = None  # type: ignore[assignment]
+class PassportElementErrorUnspecified(types.PassportElementErrorUnspecified):
     type: str | LazyProxy  # type: ignore[assignment]
     element_hash: str | LazyProxy  # type: ignore[assignment]
     message: str | LazyProxy  # type: ignore[assignment]
 
 
-class ReplyKeyboardMarkup(_ReplyKeyboardMarkup):
+class ReplyKeyboardMarkup(types.ReplyKeyboardMarkup):
     input_field_placeholder: Optional[str | LazyProxy] = None  # type: ignore[assignment]
 
 
-class ReplyKeyboardRemove(_ReplyKeyboardRemove):
+class ReplyKeyboardRemove(types.ReplyKeyboardRemove):
     ...
+
+
+__all__ = (
+    "BotCommand",
+    "ChatPermissions",
+    "ForceReply",
+    "InlineKeyboardButton",
+    "InlineKeyboardMarkup",
+    "InlineQueryResult",
+    "InlineQueryResultArticle",
+    "InlineQueryResultAudio",
+    "InlineQueryResultCachedAudio",
+    "InlineQueryResultCachedDocument",
+    "InlineQueryResultCachedGif",
+    "InlineQueryResultCachedMpeg4Gif",
+    "InlineQueryResultCachedPhoto",
+    "InlineQueryResultCachedSticker",
+    "InlineQueryResultCachedVideo",
+    "InlineQueryResultCachedVoice",
+    "InlineQueryResultContact",
+    "InlineQueryResultDocument",
+    "InlineQueryResultGame",
+    "InlineQueryResultGif",
+    "InlineQueryResultLocation",
+    "InlineQueryResultMpeg4Gif",
+    "InlineQueryResultPhoto",
+    "InlineQueryResultVenue",
+    "InlineQueryResultVideo",
+    "InlineQueryResultVoice",
+    "InputContactMessageContent",
+    "InputInvoiceMessageContent",
+    "InputLocationMessageContent",
+    "InputMedia",
+    "InputMediaAnimation",
+    "InputMediaAudio",
+    "InputMediaDocument",
+    "InputMediaPhoto",
+    "InputMediaVideo",
+    "InputMessageContent",
+    "InputTextMessageContent",
+    "InputVenueMessageContent",
+    "KeyboardButton",
+    "KeyboardButtonPollType",
+    "LabeledPrice",
+    "MenuButton",
+    "MenuButtonCommands",
+    "MenuButtonDefault",
+    "MenuButtonWebApp",
+    "MessageEntity",
+    "PassportElementError",
+    "PassportElementErrorDataField",
+    "PassportElementErrorFile",
+    "PassportElementErrorFiles",
+    "PassportElementErrorFrontSide",
+    "PassportElementErrorReverseSide",
+    "PassportElementErrorSelfie",
+    "PassportElementErrorTranslationFile",
+    "PassportElementErrorTranslationFiles",
+    "PassportElementErrorUnspecified",
+    "ReplyKeyboardMarkup",
+    "ReplyKeyboardRemove",
+)
+
+
+# Load typing forward refs for every TelegramObject
+for _entity_name in __all__:
+    _entity = globals()[_entity_name]
+    if not hasattr(_entity, "model_rebuild"):
+        continue
+    _entity.model_rebuild(
+        _types_namespace={
+            "List": List,
+            "Optional": Optional,
+            "Union": Union,
+            "Literal": Literal,
+            **{k: v for k, v in vars(types).items() if k in types.__all__},
+        }
+    )
+
+del _entity
+del _entity_name
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/cores/__init__.py` & `aiogram_i18n-1.2/aiogram_i18n/cores/__init__.py`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/aiogram_i18n/cores/base.py` & `aiogram_i18n-1.2/aiogram_i18n/cores/base.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,36 +1,37 @@
 import os
 from abc import abstractmethod, ABC
-from typing import List, Dict, Optional, Any, Tuple, TypeVar, Generic
+from typing import List, Dict, Optional, Any, Tuple, TypeVar, Generic, cast
 from aiogram_i18n.exceptions import NoTranslateFileExistsError, NoLocalesFoundError, NoLocalesError
 
 
 Translator = TypeVar("Translator")
 
 
 class BaseCore(Generic[Translator], ABC):
-    default_locale: str
+    default_locale: Optional[str]
     locales: Dict[str, Translator]
 
-    def __init__(self) -> None:
+    def __init__(self, default_locale: Optional[str] = None) -> None:
+        self.default_locale = default_locale
         self.locales = {}
 
     @abstractmethod
     def get(self, key: str, /, locale: str, **kwargs: Any) -> str:
         ...
 
     def get_translator(self, locale: str) -> Translator:
         if locale not in self.locales:
-            locale = self.default_locale
+            locale = cast(str, self.default_locale)
         return self.locales[locale]
 
     async def startup(self) -> None:
         self.locales.update(self.find_locales())
 
-    async def shutdown(self, *args: Any, **kwargs: Any) -> None:
+    async def shutdown(self) -> None:
         self.locales.clear()
 
     @staticmethod
     def _extract_locales(path: str) -> List[str]:
         if "{locale}" in path:
             path = path.split("{locale}")[0]
         locales: List[str] = []
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/cores/fluent_compile_core.py` & `aiogram_i18n-1.2/aiogram_i18n/cores/fluent_compile_core.py`

 * *Files 10% similar despite different names*

```diff
@@ -8,38 +8,37 @@
     raise NoModuleError(name="FluentCompileCore", module_name="fluent_compiler")
 
 from aiogram_i18n.cores.base import BaseCore
 
 
 class FluentCompileCore(BaseCore[FluentBundle]):
     def __init__(
-            self,
-            path: str,
-            default_locale: str = "en",
-            use_isolating: bool = True,
-            functions: Optional[Dict[str, Callable[..., Any]]] = None,
-            raise_key_error: bool = True
+        self,
+        path: str,
+        default_locale: Optional[str] = None,
+        use_isolating: bool = False,
+        functions: Optional[Dict[str, Callable[..., Any]]] = None,
+        raise_key_error: bool = True
     ) -> None:
-        super().__init__()
+        super().__init__(default_locale=default_locale)
         self.path = path
         self.use_isolating = use_isolating
         self.functions = functions
-        self.default_locale = default_locale
         self.raise_key_error = raise_key_error
 
     def get(self, key: str, /, locale: str, **kwargs: Any) -> str:
         translator: FluentBundle = self.get_translator(locale=locale)
         try:
             text, errors = translator.format(message_id=key, args=kwargs)
         except KeyError:
             if self.raise_key_error:
                 raise KeyNotFound(key)
             return key
         if errors:
-            raise ValueError("\n".join(errors))
+            raise errors[0]
         return cast(str, text)  # 'cause fluent_compiler type-ignored
 
     def find_locales(self) -> Dict[str, FluentBundle]:
         """
         Load all compiled locales from path
 
         :return: dict with locales
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/cores/fluent_runtime_core.py` & `aiogram_i18n-1.2/aiogram_i18n/cores/fluent_runtime_core.py`

 * *Files 10% similar despite different names*

```diff
@@ -9,32 +9,35 @@
 
 from aiogram_i18n.cores.base import BaseCore
 
 
 class FluentRuntimeCore(BaseCore[FluentBundle]):
     def __init__(
         self,
-        path: str, default_locale: str = "en",
-        use_isolating: bool = True,
+        path: str,
+        default_locale: Optional[str] = None,
+        use_isolating: bool = False,
         functions: Optional[Dict[str, Callable[..., Any]]] = None,
         pre_compile: bool = True,
         raise_key_error: bool = True
     ) -> None:
-        super().__init__()
+        super().__init__(default_locale=default_locale)
         self.path = path
         self.use_isolating = use_isolating
         self.functions = functions
-        self.default_locale = default_locale
         self.pre_compile = pre_compile,
         self.raise_key_error = raise_key_error
 
     def get(self, key: str, /, locale: str, **kwargs: Any) -> str:
         translator: FluentBundle = self.get_translator(locale=locale)
-        message = translator.get_message(message_id=key)
-        if message.value is None:
+        try:
+            message = translator.get_message(message_id=key)
+            if message.value is None:
+                raise KeyError(key)
+        except KeyError:
             if self.raise_key_error:
                 raise KeyNotFound(key)
             return key
         text, errors = translator.format_pattern(
             pattern=message.value,
             args=kwargs
         )
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/cores/gnu_text_core.py` & `aiogram_i18n-1.2/aiogram_i18n/cores/gnu_text_core.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,22 +1,21 @@
 from gettext import GNUTranslations
-from typing import Dict, Any
+from typing import Dict, Any, Optional
 
 from aiogram_i18n.cores.base import BaseCore
 
 
 class GNUTextCore(BaseCore[GNUTranslations]):
     def __init__(
         self, *,
         path: str,
-        default_locale: str = "en"
+        default_locale: Optional[str] = None,
     ) -> None:
-        super().__init__()
+        super().__init__(default_locale=default_locale)
         self.path = path
-        self.default_locale = default_locale
 
     def find_locales(self) -> Dict[str, GNUTranslations]:
         """
         Load all compiled locales from path
 
         :return: dict with locales
         """
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/lazy/proxy.py` & `aiogram_i18n-1.2/aiogram_i18n/lazy/proxy.py`

 * *Files 4% similar despite different names*

```diff
@@ -3,37 +3,32 @@
 from typing import Any, Dict, Tuple, Union
 
 from pydantic import BaseModel
 
 from aiogram_i18n.context import I18nContext
 
 
-class LazyProxy(BaseModel):
+class LazyProxy(BaseModel):  # type: ignore[no-redef]
     key: str
     kwargs: Dict[str, Any]
 
-    class Config:
-        arbitrary_types_allowed = True
-
-    def __init__(
-        self, key: str, /, **kwargs: Dict[str, Any]
-    ) -> None:
+    def __init__(self, key: str, /, **kwargs: Any) -> None:
         super().__init__(key=key, kwargs=kwargs)
 
     @property
     def data(self) -> str:
         context = I18nContext.get_current()
         if context:
             return context.get(self.key, **self.kwargs)
         return self.key
 
-    def dict(self, **kwargs: Any) -> str:  # type: ignore[override]
+    def model_dump(self, **kwargs: Any) -> str:  # type: ignore[override]
         return self.data
 
-    def json(self, **kwargs: Any) -> str:
+    def model_dump_json(self, **kwargs: Any) -> str:
         return self.data
 
     def __repr__(self) -> str:
         return f"{self.__class__.__name__}<'{self.key}'>"
 
     def __int__(self) -> int:
         return int(self.data)
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/managers/base.py` & `aiogram_i18n-1.2/aiogram_i18n/managers/base.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 from abc import abstractmethod, ABC
-from typing import Dict, Any, TYPE_CHECKING, Awaitable, Callable
+from typing import Dict, Any, TYPE_CHECKING, Awaitable, Callable, Optional
 
 from aiogram.dispatcher.event.handler import CallableMixin
 from aiogram.types import TelegramObject
 
 
 class BaseManager(ABC):
-    default_locale: str
+    default_locale: Optional[str]
     set_locale_mixin: CallableMixin
 
-    def __init__(self, default_locale: str = "en") -> None:
+    def __init__(self, default_locale: Optional[str] = None) -> None:
         self.default_locale = default_locale
         self.set_locale_mixin = CallableMixin(self.set_locale)
 
     @abstractmethod
     async def get_locale(self, event: TelegramObject, data: Dict[str, Any]) -> str:
         ...
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/managers/fsm.py` & `aiogram_i18n-1.2/aiogram_i18n/managers/fsm.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,29 +1,31 @@
-from typing import Dict, Any, Optional
+from typing import Dict, Any, Optional, cast
 
 from aiogram.fsm.context import FSMContext
 from aiogram.types import TelegramObject
 
 from aiogram_i18n.managers.base import BaseManager
 
 
 class FSMManager(BaseManager):
     key: str
 
-    def __init__(self, key: str = "locale", default_locale: str = "en"):
+    def __init__(
+        self, key: str = "locale", default_locale: Optional[str] = None
+    ) -> None:
         super().__init__(default_locale=default_locale)
         self.key = key
 
     async def get_locale(self, event: TelegramObject, data: Dict[str, Any]) -> str:
         state: Optional[FSMContext] = data.get("state")
         locale: Optional[str] = None
         if state:
             fsm_data = await state.get_data()
             locale = fsm_data.get(self.key, None)
         if locale is None:
-            locale = self.default_locale
+            locale = cast(str, self.default_locale)
             if state:
                 await state.update_data(data={self.key: locale})
         return locale
 
     async def set_locale(self, locale: str, state: FSMContext) -> None:
         await state.update_data(data={self.key: locale})
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/utils/fluent_extract/models.py` & `aiogram_i18n-1.2/aiogram_i18n/utils/fluent_extract/models.py`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/aiogram_i18n/utils/fluent_extract/parser.py` & `aiogram_i18n-1.2/aiogram_i18n/utils/fluent_extract/parser.py`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/aiogram_i18n/utils/fluent_stub/__init__.py` & `aiogram_i18n-1.2/aiogram_i18n/utils/fluent_stub/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 try:
     from fluent.syntax import FluentParser
     from .visitor import FluentVisitor
 except ImportError:
     raise NoModuleError(name="Fluent stub generator", module_name="fluent.syntax")
 
 
-STUB_HEADER = """from typing import Any, Union
+STUB_HEADER = """from typing import Any
 
 from aiogram_i18n import I18nContext as _I18nContext
 from aiogram_i18n.lazy import LazyProxy, LazyFactory as _LazyFactory
 
 
 class I18nStubs:
 """
@@ -54,15 +54,15 @@
 def stub_from_messages(messages: Dict[str, List[str]], kw_only: bool = True) -> str:
     stub_text = STUB_HEADER
     for name, params in messages.items():
         params = list(map(lambda x: f'{x}: Any', params))
         if params and kw_only:
             params.insert(0, "*")
         params.insert(0, "self")
-        stub_text += f"    def {name.replace('-', '_')}({', '.join(params)}) -> Union[str, LazyProxy]: ...\n"
+        stub_text += f"    def {name.replace('-', '_')}({', '.join(params)}) -> str | LazyProxy: ...\n"
     return stub_text + STUB_FOOTER
 
 
 def stub_from_file(file: str, kw_only: bool = True) -> str:
     return stub_from_messages(messages=parse_file(file=file), kw_only=kw_only)
```

### Comparing `aiogram_i18n-1.1/aiogram_i18n/utils/fluent_stub/visitor.py` & `aiogram_i18n-1.2/aiogram_i18n/utils/fluent_stub/visitor.py`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/examples/mre.py` & `aiogram_i18n-1.2/examples/mre.py`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/tests/conftest.py` & `aiogram_i18n-1.2/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/tests/test_cores.py` & `aiogram_i18n-1.2/tests/test_cores.py`

 * *Files 18% similar despite different names*

```diff
@@ -12,12 +12,12 @@
     lazy_fixture("fluent_compile_core"),
 ])
 @pytest.mark.asyncio
 class Test:
     async def test_startup(self, core: BaseCore[Any]) -> None:
         assert core.available_locales == ()
         await core.startup()
-        assert core.available_locales == ("en", "uk")
+        assert set(core.available_locales) == {"en", "uk"}
 
     async def test_get(self, core: BaseCore[Any]) -> None:
         assert core.get("hello", locale="en", user="Bob") == "Hello, <b>Bob</b>!"
         assert core.get("cur-lang", locale="uk", language="uk") == "Твоя мова: <i>uk</i>"
```

### Comparing `aiogram_i18n-1.1/tests/data/locales/en/LC_MESSAGES/mybot.mo` & `aiogram_i18n-1.2/tests/data/locales/en/LC_MESSAGES/mybot.mo`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/tests/data/locales/uk/LC_MESSAGES/mybot.mo` & `aiogram_i18n-1.2/tests/data/locales/uk/LC_MESSAGES/mybot.mo`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/README.md` & `aiogram_i18n-1.2/README.md`

 * *Files identical despite different names*

### Comparing `aiogram_i18n-1.1/pyproject.toml` & `aiogram_i18n-1.2/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "aiogram_i18n"
-version = "1.1"
+version = "1.2"
 authors = [
   { name="RootShinobi" },
 ]
 description = "small translation tools for aiogram"
 readme = "README.md"
 license = {text = "MIT License"}
 requires-python = ">=3.8"
@@ -16,15 +16,15 @@
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
 
 dependencies = [
     "aiogram~=3.0.0b7",
-    "click==8.1.4"
+    "click~=8.1.4"
 ]
 
 keywords = [
     "telegram",
     "bot",
     "api",
     "framework",
@@ -49,15 +49,17 @@
 runtime = [
     "fluent.runtime~=0.4.0",
 ]
 test = [
     "pytest~=7.4.0",
     "pytest-asyncio~=0.21.1",
     "pytest-lazy-fixture~=0.6.3",
-    "flake8~=6.0.0"
+    "flake8~=6.0.0",
+    "fluent_compiler~=1.0",
+    "fluent.runtime~=0.4.0"
 ]
 
 [tool.mypy]
 plugins = ["pydantic.mypy"]
 exclude = [
     "\\.?venv",
     "\\.idea",
```

### Comparing `aiogram_i18n-1.1/PKG-INFO` & `aiogram_i18n-1.2/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,27 +1,29 @@
 Metadata-Version: 2.1
 Name: aiogram_i18n
-Version: 1.1
+Version: 1.2
 Summary: small translation tools for aiogram
 Project-URL: Repository, https://github.com/RootShinobi/aiogram_i18n
 Author: RootShinobi
 License: MIT License
 Keywords: aiogram,api,asyncio,bot,fluent,framework,gnutext,i18n,telegram,wrapper
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.8
 Requires-Dist: aiogram~=3.0.0b7
-Requires-Dist: click==8.1.4
+Requires-Dist: click~=8.1.4
 Provides-Extra: compiler
 Requires-Dist: fluent-compiler~=1.0; extra == 'compiler'
 Provides-Extra: runtime
 Requires-Dist: fluent-runtime~=0.4.0; extra == 'runtime'
 Provides-Extra: test
 Requires-Dist: flake8~=6.0.0; extra == 'test'
+Requires-Dist: fluent-compiler~=1.0; extra == 'test'
+Requires-Dist: fluent-runtime~=0.4.0; extra == 'test'
 Requires-Dist: pytest-asyncio~=0.21.1; extra == 'test'
 Requires-Dist: pytest-lazy-fixture~=0.6.3; extra == 'test'
 Requires-Dist: pytest~=7.4.0; extra == 'test'
 Description-Content-Type: text/markdown
 
 # aiogram_i18n
```

