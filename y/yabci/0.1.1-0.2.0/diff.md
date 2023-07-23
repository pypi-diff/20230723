# Comparing `tmp/yabci-0.1.1.tar.gz` & `tmp/yabci-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "yabci-0.1.1.tar", last modified: Fri Jun 30 20:52:07 2023, max compression
+gzip compressed data, was "yabci-0.2.0.tar", last modified: Sun Jul 23 10:11:29 2023, max compression
```

## Comparing `yabci-0.1.1.tar` & `yabci-0.2.0.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 bob       (1000) bob       (1001)        0 2023-06-30 20:52:07.433999 yabci-0.1.1/
--rw-r--r--   0 bob       (1000) bob       (1001)    34523 2023-06-30 17:06:17.000000 yabci-0.1.1/LICENSE
--rw-r--r--   0 bob       (1000) bob       (1001)    47780 2023-06-30 20:52:07.433999 yabci-0.1.1/PKG-INFO
--rw-r--r--   0 bob       (1000) bob       (1001)     7240 2023-06-30 19:52:28.000000 yabci-0.1.1/README.md
--rw-r--r--   0 bob       (1000) bob       (1001)      899 2023-06-30 20:42:14.000000 yabci-0.1.1/pyproject.toml
--rw-r--r--   0 bob       (1000) bob       (1001)       38 2023-06-30 20:52:07.433999 yabci-0.1.1/setup.cfg
-drwxr-xr-x   0 bob       (1000) bob       (1001)        0 2023-06-30 20:52:07.430666 yabci-0.1.1/src/
--rw-r--r--   0 bob       (1000) bob       (1001)        0 2023-06-27 21:12:36.000000 yabci-0.1.1/src/__init__.py
--rw-r--r--   0 bob       (1000) bob       (1001)     9386 2023-06-30 19:36:45.000000 yabci-0.1.1/src/importer.py
--rw-r--r--   0 bob       (1000) bob       (1001)      426 2023-06-29 15:54:04.000000 yabci-0.1.1/src/logger.py
--rw-r--r--   0 bob       (1000) bob       (1001)     4258 2023-06-29 16:14:58.000000 yabci-0.1.1/src/utils.py
-drwxr-xr-x   0 bob       (1000) bob       (1001)        0 2023-06-30 20:52:07.430666 yabci-0.1.1/src/yabci.egg-info/
--rw-r--r--   0 bob       (1000) bob       (1001)    47780 2023-06-30 20:52:07.000000 yabci-0.1.1/src/yabci.egg-info/PKG-INFO
--rw-r--r--   0 bob       (1000) bob       (1001)      301 2023-06-30 20:52:07.000000 yabci-0.1.1/src/yabci.egg-info/SOURCES.txt
--rw-r--r--   0 bob       (1000) bob       (1001)        1 2023-06-30 20:52:07.000000 yabci-0.1.1/src/yabci.egg-info/dependency_links.txt
--rw-r--r--   0 bob       (1000) bob       (1001)       42 2023-06-30 20:52:07.000000 yabci-0.1.1/src/yabci.egg-info/requires.txt
--rw-r--r--   0 bob       (1000) bob       (1001)       31 2023-06-30 20:52:07.000000 yabci-0.1.1/src/yabci.egg-info/top_level.txt
-drwxr-xr-x   0 bob       (1000) bob       (1001)        0 2023-06-30 20:52:07.433999 yabci-0.1.1/tests/
--rw-r--r--   0 bob       (1000) bob       (1001)     2356 2023-06-30 16:10:49.000000 yabci-0.1.1/tests/test_examples.py
--rw-r--r--   0 bob       (1000) bob       (1001)     4413 2023-06-30 19:30:38.000000 yabci-0.1.1/tests/test_importer.py
+drwxr-xr-x   0 bob       (1000) bob       (1001)        0 2023-07-23 10:11:29.260493 yabci-0.2.0/
+-rw-r--r--   0 bob       (1000) bob       (1001)    34523 2023-06-30 17:06:17.000000 yabci-0.2.0/LICENSE
+-rw-r--r--   0 bob       (1000) bob       (1001)    51101 2023-07-23 10:11:29.260493 yabci-0.2.0/PKG-INFO
+-rw-r--r--   0 bob       (1000) bob       (1001)    10561 2023-07-23 10:04:40.000000 yabci-0.2.0/README.md
+-rw-r--r--   0 bob       (1000) bob       (1001)     1235 2023-07-23 10:10:57.000000 yabci-0.2.0/pyproject.toml
+-rw-r--r--   0 bob       (1000) bob       (1001)       38 2023-07-23 10:11:29.260493 yabci-0.2.0/setup.cfg
+drwxr-xr-x   0 bob       (1000) bob       (1001)        0 2023-07-23 10:11:29.260493 yabci-0.2.0/src/
+-rw-r--r--   0 bob       (1000) bob       (1001)        0 2023-06-27 21:12:36.000000 yabci-0.2.0/src/__init__.py
+-rw-r--r--   0 bob       (1000) bob       (1001)     9740 2023-07-18 21:49:47.000000 yabci-0.2.0/src/importer.py
+-rw-r--r--   0 bob       (1000) bob       (1001)      426 2023-06-29 15:54:04.000000 yabci-0.2.0/src/logger.py
+-rw-r--r--   0 bob       (1000) bob       (1001)     4419 2023-07-18 21:48:56.000000 yabci-0.2.0/src/utils.py
+drwxr-xr-x   0 bob       (1000) bob       (1001)        0 2023-07-23 10:11:29.260493 yabci-0.2.0/src/yabci.egg-info/
+-rw-r--r--   0 bob       (1000) bob       (1001)    51101 2023-07-23 10:11:29.000000 yabci-0.2.0/src/yabci.egg-info/PKG-INFO
+-rw-r--r--   0 bob       (1000) bob       (1001)      301 2023-07-23 10:11:29.000000 yabci-0.2.0/src/yabci.egg-info/SOURCES.txt
+-rw-r--r--   0 bob       (1000) bob       (1001)        1 2023-07-23 10:11:29.000000 yabci-0.2.0/src/yabci.egg-info/dependency_links.txt
+-rw-r--r--   0 bob       (1000) bob       (1001)       42 2023-07-23 10:11:29.000000 yabci-0.2.0/src/yabci.egg-info/requires.txt
+-rw-r--r--   0 bob       (1000) bob       (1001)       31 2023-07-23 10:11:29.000000 yabci-0.2.0/src/yabci.egg-info/top_level.txt
+drwxr-xr-x   0 bob       (1000) bob       (1001)        0 2023-07-23 10:11:29.260493 yabci-0.2.0/tests/
+-rw-r--r--   0 bob       (1000) bob       (1001)     2356 2023-06-30 16:10:49.000000 yabci-0.2.0/tests/test_examples.py
+-rw-r--r--   0 bob       (1000) bob       (1001)     4413 2023-06-30 19:30:38.000000 yabci-0.2.0/tests/test_importer.py
```

### Comparing `yabci-0.1.1/LICENSE` & `yabci-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `yabci-0.1.1/PKG-INFO` & `yabci-0.2.0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yabci
-Version: 0.1.1
+Version: 0.2.0
 Summary: Yet another beancount importer - import any file formats, with total customization
 Author: privatize-koala
 License:                     GNU AFFERO GENERAL PUBLIC LICENSE
                                Version 3, 19 November 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -679,27 +679,45 @@
 
 # yabci - yet another beancount importer
 
 **yabci** (*yet another beancount importer*) is a flexible & extensible [importer for beancount](https://beancount.github.io/docs/importing_external_data.html) (v2), aiming to replace any standard importer without the need to write custom python code.
 
 Its goal is to support as many import formats as possible, while giving you complete control over the conversion into beancount transactions. The conversion is configured by a config, eliminating the need to write custom python code (but which can be used for complex cases)
 
+## Motivation
+
+There are a lot of beancount importers available. Most of them are specifically tailored for a certain format of certain banks or payment providers. And depending on the author's needs, they map import data to beancount transactions in a certain way. Any additional data from your import files is discarded. If you want to finetune beancount transactions or want to use more advanced features like tags, most of the time you are out of luck.
+
+yabci tries to fill this gap: yabci is format-agnostic regarding input files (everything the underlying [benedict supports](https://github.com/fabiocaccamo/python-benedict), which means CSV, JSON, and [more](#todo)). On the beancount side, yabci supports all transaction properties, postings & balances (from the basic ones like date, payee, narration to tags, meta data & links).
+
+The only thing to do for the end user is to tell yabci, which input field shall be mapped into which beancount fields. yabci takes care of the rest, like parsing dates from strings, parsing numbers with currencies, duplicate detection, etc.
+
 **Features**:
 
 - support for a lot of input file formats out of the box, such as csv & json (anything that the fantastic [benedict](https://github.com/fabiocaccamo/python-benedict) supports)
 - complete control: you can decide specifically how your input data gets transformed into a beancount transaction
     + support for all beancount transaction properties (date, flag, payee, narration, tags, links)
     + support for all posting properties (account, amount, cost, price, flag)
     + support for transaction & post meta data
     + support for multiple postings per transaction
     + any field can be transformed while importing it, giving you total control over the output
 - conversion of data types: no more custom date or number parsing
 - duplication detection (optionally using existing identifiers in your input data)
 
-## Getting started
+## Getting started with beancount importers
+
+*If you already know beancount importers, you can skip to [Getting started with yabci]*
+
+To import external data into beancount, beancount uses so-called *importers*. You can install them from pip or write them on your own. If you are reading this, you probably want to use *yabci* to create one on your own.
+
+To tell beancount about your importers, you have to create *importer config*. This is a python file (with the ending `.py`) with the necessary importer code. While example importers can become complicated very easily (see the example at [https://github.com/beancount/beancount/blob/v2/examples/ingest/office/importers/utrade/utrade_csv.py]), importers using *yabci* should look a lot simpler.
+
+If you have your importer ready, you can run the beancount command `bean-extract` on your import files. `bean-extract` will use your importer to generate beancount transactions, which you can paste / redirect into your `*.beancount` files.
+
+## Getting started with yabci
 
 Say, you have the following csv from your bank, and want to import it into beancount:
 
 *bank-foo.csv*
 ```csv
 "ID","Datetime","Note","Type","From","To","Amount"
 "2394198259925614643","2017-04-25T03:15:53","foo service","Payment","Brian Taylor","Foo company","-220"
@@ -820,14 +838,44 @@
 ```
 
 Notes:
 
 - `"date"` only accepts `datetime.date`. If a string is passed, *yabci* tries to convert it via [dateutil.parser](https://dateutil.readthedocs.io/en/stable/parser.html)
 - `"amount"` must be a 2-element list, containing numeric amount & currency
 
+## More advanced features
+
+### benedict arguments
+
+If you need to pass special parameters to benedict (for example how your CSV is formatted), you can use the config entry `benedict_kwargs`. This dict gets passed to benedict and determines how you input file is parsed. See [](https://github.com/fabiocaccamo/python-benedict#io-methods) for available options.
+
+Example for passing options about CSV format:
+```py
+CONFIG = [
+    yabci.Importer(
+        benedict_kwargs={"delimiter": ";"},
+        # ...
+    )
+]
+```
+
+### date parsing
+
+Transaction dates are parsed using [dateutil](https://dateutil.readthedocs.io/en/stable/parser.html#dateutil.parser.parse). If you need to pass certain options to `parse()`, you can use `        parse_date_options`:
+
+Example for european dates (`"01.06.2023"` is parsed as "January 6th" by default, if you want it to be interpreted as `"June 1st"`, you have to pass the `dayfirst` option)
+```py
+CONFIG = [
+    yabci.Importer(
+        parse_date_options={"dayfirst": True},
+        # ...
+    )
+]
+```
+
 ## Detecting duplicate transactions
 
 If your input data contains some form of unique id, you can use it to prevent importing the same transaction twice.
 
 Therefore, you must import the unique id into a meta field, and let *yabci* know it should be used to identifiy duplicates. Beancount will not re-import these transactions.
 
 *confiy.py*
@@ -847,17 +895,24 @@
                 # use the value of "transaction_id"
                 "duplication_key": "transaction_id",
             },
         },
     },
 })
 
-# must be called explicitely to disable beancount's own duplication detection
-# (which interfers with the configured one above)
-ingest(CONFIG, hooks=[])
+# beancount uses its own duplicate detection by default, which interferes with
+# yabci's approach. Disable it therefore. The variable `HOOKS` is needed to
+# disable it within fava as well, see
+# https://github.com/beancount/fava/issues/1197 and
+# https://github.com/beancount/fava/issues/1184
+
+HOOKS = []
+
+if __name__ == "main":
+    ingest(CONFIG, hooks=[])
 
 ```
 
 This creates transactions with meta data `duplication_key`:
 
 ```beancount
 2023-01-01 * "foo transaction"
```

### Comparing `yabci-0.1.1/README.md` & `yabci-0.2.0/README.md`

 * *Files 22% similar despite different names*

```diff
@@ -1,26 +1,44 @@
 # yabci - yet another beancount importer
 
 **yabci** (*yet another beancount importer*) is a flexible & extensible [importer for beancount](https://beancount.github.io/docs/importing_external_data.html) (v2), aiming to replace any standard importer without the need to write custom python code.
 
 Its goal is to support as many import formats as possible, while giving you complete control over the conversion into beancount transactions. The conversion is configured by a config, eliminating the need to write custom python code (but which can be used for complex cases)
 
+## Motivation
+
+There are a lot of beancount importers available. Most of them are specifically tailored for a certain format of certain banks or payment providers. And depending on the author's needs, they map import data to beancount transactions in a certain way. Any additional data from your import files is discarded. If you want to finetune beancount transactions or want to use more advanced features like tags, most of the time you are out of luck.
+
+yabci tries to fill this gap: yabci is format-agnostic regarding input files (everything the underlying [benedict supports](https://github.com/fabiocaccamo/python-benedict), which means CSV, JSON, and [more](#todo)). On the beancount side, yabci supports all transaction properties, postings & balances (from the basic ones like date, payee, narration to tags, meta data & links).
+
+The only thing to do for the end user is to tell yabci, which input field shall be mapped into which beancount fields. yabci takes care of the rest, like parsing dates from strings, parsing numbers with currencies, duplicate detection, etc.
+
 **Features**:
 
 - support for a lot of input file formats out of the box, such as csv & json (anything that the fantastic [benedict](https://github.com/fabiocaccamo/python-benedict) supports)
 - complete control: you can decide specifically how your input data gets transformed into a beancount transaction
     + support for all beancount transaction properties (date, flag, payee, narration, tags, links)
     + support for all posting properties (account, amount, cost, price, flag)
     + support for transaction & post meta data
     + support for multiple postings per transaction
     + any field can be transformed while importing it, giving you total control over the output
 - conversion of data types: no more custom date or number parsing
 - duplication detection (optionally using existing identifiers in your input data)
 
-## Getting started
+## Getting started with beancount importers
+
+*If you already know beancount importers, you can skip to [Getting started with yabci]*
+
+To import external data into beancount, beancount uses so-called *importers*. You can install them from pip or write them on your own. If you are reading this, you probably want to use *yabci* to create one on your own.
+
+To tell beancount about your importers, you have to create *importer config*. This is a python file (with the ending `.py`) with the necessary importer code. While example importers can become complicated very easily (see the example at [https://github.com/beancount/beancount/blob/v2/examples/ingest/office/importers/utrade/utrade_csv.py]), importers using *yabci* should look a lot simpler.
+
+If you have your importer ready, you can run the beancount command `bean-extract` on your import files. `bean-extract` will use your importer to generate beancount transactions, which you can paste / redirect into your `*.beancount` files.
+
+## Getting started with yabci
 
 Say, you have the following csv from your bank, and want to import it into beancount:
 
 *bank-foo.csv*
 ```csv
 "ID","Datetime","Note","Type","From","To","Amount"
 "2394198259925614643","2017-04-25T03:15:53","foo service","Payment","Brian Taylor","Foo company","-220"
@@ -141,14 +159,44 @@
 ```
 
 Notes:
 
 - `"date"` only accepts `datetime.date`. If a string is passed, *yabci* tries to convert it via [dateutil.parser](https://dateutil.readthedocs.io/en/stable/parser.html)
 - `"amount"` must be a 2-element list, containing numeric amount & currency
 
+## More advanced features
+
+### benedict arguments
+
+If you need to pass special parameters to benedict (for example how your CSV is formatted), you can use the config entry `benedict_kwargs`. This dict gets passed to benedict and determines how you input file is parsed. See [](https://github.com/fabiocaccamo/python-benedict#io-methods) for available options.
+
+Example for passing options about CSV format:
+```py
+CONFIG = [
+    yabci.Importer(
+        benedict_kwargs={"delimiter": ";"},
+        # ...
+    )
+]
+```
+
+### date parsing
+
+Transaction dates are parsed using [dateutil](https://dateutil.readthedocs.io/en/stable/parser.html#dateutil.parser.parse). If you need to pass certain options to `parse()`, you can use `        parse_date_options`:
+
+Example for european dates (`"01.06.2023"` is parsed as "January 6th" by default, if you want it to be interpreted as `"June 1st"`, you have to pass the `dayfirst` option)
+```py
+CONFIG = [
+    yabci.Importer(
+        parse_date_options={"dayfirst": True},
+        # ...
+    )
+]
+```
+
 ## Detecting duplicate transactions
 
 If your input data contains some form of unique id, you can use it to prevent importing the same transaction twice.
 
 Therefore, you must import the unique id into a meta field, and let *yabci* know it should be used to identifiy duplicates. Beancount will not re-import these transactions.
 
 *confiy.py*
@@ -168,17 +216,24 @@
                 # use the value of "transaction_id"
                 "duplication_key": "transaction_id",
             },
         },
     },
 })
 
-# must be called explicitely to disable beancount's own duplication detection
-# (which interfers with the configured one above)
-ingest(CONFIG, hooks=[])
+# beancount uses its own duplicate detection by default, which interferes with
+# yabci's approach. Disable it therefore. The variable `HOOKS` is needed to
+# disable it within fava as well, see
+# https://github.com/beancount/fava/issues/1197 and
+# https://github.com/beancount/fava/issues/1184
+
+HOOKS = []
+
+if __name__ == "main":
+    ingest(CONFIG, hooks=[])
 
 ```
 
 This creates transactions with meta data `duplication_key`:
 
 ```beancount
 2023-01-01 * "foo transaction"
```

### Comparing `yabci-0.1.1/src/importer.py` & `yabci-0.2.0/src/importer.py`

 * *Files 9% similar despite different names*

```diff
@@ -28,25 +28,29 @@
         file_pattern: str = None,
         target_account: str = None,
         duplication_key=None,
         mapping_transactions=None,
         mapping_transaction=None,
         mapping_balances=None,
         mapping_balance=None,
-        hook_prepare_data: callable = None
+        hook_prepare_data: callable = None,
+        benedict_kwargs: dict = {},
+        parse_date_options: dict = {},
     ):
         self._name = name
         self._file_pattern = file_pattern
         self._target_account = target_account
         self._duplication_key = duplication_key
         self._mapping_transactions = mapping_transactions
         self._mapping_transaction = mapping_transaction
         self._mapping_balances = mapping_balances
         self._mapping_balance = mapping_balance
         self._hook_prepare_data = hook_prepare_data
+        self._benedict_kwargs = benedict_kwargs
+        self._parse_date_options = parse_date_options
 
     def name(self):
         if self._name:
             return self._name
         return "Generic yabci Importer"
 
     def identifier(self, filename) -> str:
@@ -59,15 +63,16 @@
         return '{}'.format(os.path.basename(filename))
 
     def identify(self, file: cache._FileMemo):
         if self._file_pattern:
 
             filename = file.name.lower()
 
-            if not re.match(self._file_pattern, filename):
+            # match with ignore case, because beancount lowercases the filename
+            if not re.match(self._file_pattern, filename, re.IGNORECASE):
                 logger.debug("Filename %s does not match pattern (%s)" % (filename, self._file_pattern))
                 return False
 
         return True
 
     def file_name(self, file):
         return self.basename(file.name)
@@ -132,15 +137,15 @@
 
             mapped = map_dict(self._mapping_transaction, raw)
 
             # create a beancount object from the mapped values, with sensible
             # defaults
             transaction = data.Transaction(
                 mapped.get("meta", data.EMPTY_SET),
-                parse_date(mapped.get("date")),
+                parse_date(mapped.get("date"), **self._parse_date_options),
                 mapped.get("flag", flags.FLAG_OKAY),
                 mapped.get("payee", None),
                 mapped.get("narration", None),
                 mapped.get("tags", data.EMPTY_SET),
                 mapped.get("links", data.EMPTY_SET),
                 [],
             )
@@ -175,15 +180,15 @@
             if not self._mapping_balance:
                 raise Exception("Mapping for single balance is not defined (key 'mapping_balance')")
 
             mapped = map_dict(self._mapping_balance, raw)
 
             return data.Balance(
                 mapped.get("meta", data.EMPTY_SET),
-                parse_date(mapped.get("date")),
+                parse_date(mapped.get("date"), **self._parse_date_options),
                 mapped.get("account", self._target_account),
                 parse_amount(mapped.get("amount")),
                 mapped.get("tolerance", None),
                 parse_amount(mapped.get("diff_amount", None)),
             )
 
         except Exception as e:
@@ -226,15 +231,15 @@
 
         # if a hook is given, execute it
         if self._hook_prepare_data:
             logger.info("running prepare_data hook")
             benedict_input = self._hook_prepare_data(benedict_input)
 
         # load it into a benedict
-        data_raw = benedict.benedict(benedict_input)
+        data_raw = benedict.benedict(benedict_input, **self._benedict_kwargs)
 
         counter = itertools.count()
         new_entries = []
 
         for entry in self.get_transactions(data_raw):
             metadata = self.new_metadata(file.name, counter, entry.meta or {})
```

### Comparing `yabci-0.1.1/src/utils.py` & `yabci-0.2.0/src/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -63,38 +63,42 @@
     '0beec7b5ea3f0fdbc95d0dd47f3c5bc275da8a33'
     """
     # https://death.andgravity.com/stable-hashing
     hash_value = sha1(s.encode("utf-8")).hexdigest()
     return hash_value
 
 
-def parse_date(thing) -> datetime.date:
+def parse_date(thing, **kwargs) -> datetime.date:
     """
     Turn a random variable into a date
 
     - date: return unchanged
     - datetime -> datetime's date
     - string: gets parsed via dateutil
 
     >>> parse_date(datetime.date(2023,2,3))
     datetime.date(2023, 2, 3)
     >>> parse_date(datetime.datetime(2023,1,1,12,34,56))
     datetime.date(2023, 1, 1)
     >>> parse_date("2017-11-05T00:06:18")
     datetime.date(2017, 11, 5)
+    >>> parse_date("01.06.2023")
+    datetime.date(2023, 1, 6)
+    >>> parse_date("01.06.2023", dayfirst=True)
+    datetime.date(2023, 6, 1)
     """
 
     try:
         if isinstance(thing, datetime.datetime):
             return thing.date()
 
         if isinstance(thing, datetime.date):
             return thing
 
-        return dateutil.parser.parse(thing).date()
+        return dateutil.parser.parse(thing, **kwargs).date()
     except Exception as e:
         raise type(e)("parse_date: %s" % str(e))
 
 
 def parse_amount(thing, default_currency="EUR") -> amount.Amount:
     """
     Create a beancount amount object from any values
```

### Comparing `yabci-0.1.1/src/yabci.egg-info/PKG-INFO` & `yabci-0.2.0/src/yabci.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yabci
-Version: 0.1.1
+Version: 0.2.0
 Summary: Yet another beancount importer - import any file formats, with total customization
 Author: privatize-koala
 License:                     GNU AFFERO GENERAL PUBLIC LICENSE
                                Version 3, 19 November 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -679,27 +679,45 @@
 
 # yabci - yet another beancount importer
 
 **yabci** (*yet another beancount importer*) is a flexible & extensible [importer for beancount](https://beancount.github.io/docs/importing_external_data.html) (v2), aiming to replace any standard importer without the need to write custom python code.
 
 Its goal is to support as many import formats as possible, while giving you complete control over the conversion into beancount transactions. The conversion is configured by a config, eliminating the need to write custom python code (but which can be used for complex cases)
 
+## Motivation
+
+There are a lot of beancount importers available. Most of them are specifically tailored for a certain format of certain banks or payment providers. And depending on the author's needs, they map import data to beancount transactions in a certain way. Any additional data from your import files is discarded. If you want to finetune beancount transactions or want to use more advanced features like tags, most of the time you are out of luck.
+
+yabci tries to fill this gap: yabci is format-agnostic regarding input files (everything the underlying [benedict supports](https://github.com/fabiocaccamo/python-benedict), which means CSV, JSON, and [more](#todo)). On the beancount side, yabci supports all transaction properties, postings & balances (from the basic ones like date, payee, narration to tags, meta data & links).
+
+The only thing to do for the end user is to tell yabci, which input field shall be mapped into which beancount fields. yabci takes care of the rest, like parsing dates from strings, parsing numbers with currencies, duplicate detection, etc.
+
 **Features**:
 
 - support for a lot of input file formats out of the box, such as csv & json (anything that the fantastic [benedict](https://github.com/fabiocaccamo/python-benedict) supports)
 - complete control: you can decide specifically how your input data gets transformed into a beancount transaction
     + support for all beancount transaction properties (date, flag, payee, narration, tags, links)
     + support for all posting properties (account, amount, cost, price, flag)
     + support for transaction & post meta data
     + support for multiple postings per transaction
     + any field can be transformed while importing it, giving you total control over the output
 - conversion of data types: no more custom date or number parsing
 - duplication detection (optionally using existing identifiers in your input data)
 
-## Getting started
+## Getting started with beancount importers
+
+*If you already know beancount importers, you can skip to [Getting started with yabci]*
+
+To import external data into beancount, beancount uses so-called *importers*. You can install them from pip or write them on your own. If you are reading this, you probably want to use *yabci* to create one on your own.
+
+To tell beancount about your importers, you have to create *importer config*. This is a python file (with the ending `.py`) with the necessary importer code. While example importers can become complicated very easily (see the example at [https://github.com/beancount/beancount/blob/v2/examples/ingest/office/importers/utrade/utrade_csv.py]), importers using *yabci* should look a lot simpler.
+
+If you have your importer ready, you can run the beancount command `bean-extract` on your import files. `bean-extract` will use your importer to generate beancount transactions, which you can paste / redirect into your `*.beancount` files.
+
+## Getting started with yabci
 
 Say, you have the following csv from your bank, and want to import it into beancount:
 
 *bank-foo.csv*
 ```csv
 "ID","Datetime","Note","Type","From","To","Amount"
 "2394198259925614643","2017-04-25T03:15:53","foo service","Payment","Brian Taylor","Foo company","-220"
@@ -820,14 +838,44 @@
 ```
 
 Notes:
 
 - `"date"` only accepts `datetime.date`. If a string is passed, *yabci* tries to convert it via [dateutil.parser](https://dateutil.readthedocs.io/en/stable/parser.html)
 - `"amount"` must be a 2-element list, containing numeric amount & currency
 
+## More advanced features
+
+### benedict arguments
+
+If you need to pass special parameters to benedict (for example how your CSV is formatted), you can use the config entry `benedict_kwargs`. This dict gets passed to benedict and determines how you input file is parsed. See [](https://github.com/fabiocaccamo/python-benedict#io-methods) for available options.
+
+Example for passing options about CSV format:
+```py
+CONFIG = [
+    yabci.Importer(
+        benedict_kwargs={"delimiter": ";"},
+        # ...
+    )
+]
+```
+
+### date parsing
+
+Transaction dates are parsed using [dateutil](https://dateutil.readthedocs.io/en/stable/parser.html#dateutil.parser.parse). If you need to pass certain options to `parse()`, you can use `        parse_date_options`:
+
+Example for european dates (`"01.06.2023"` is parsed as "January 6th" by default, if you want it to be interpreted as `"June 1st"`, you have to pass the `dayfirst` option)
+```py
+CONFIG = [
+    yabci.Importer(
+        parse_date_options={"dayfirst": True},
+        # ...
+    )
+]
+```
+
 ## Detecting duplicate transactions
 
 If your input data contains some form of unique id, you can use it to prevent importing the same transaction twice.
 
 Therefore, you must import the unique id into a meta field, and let *yabci* know it should be used to identifiy duplicates. Beancount will not re-import these transactions.
 
 *confiy.py*
@@ -847,17 +895,24 @@
                 # use the value of "transaction_id"
                 "duplication_key": "transaction_id",
             },
         },
     },
 })
 
-# must be called explicitely to disable beancount's own duplication detection
-# (which interfers with the configured one above)
-ingest(CONFIG, hooks=[])
+# beancount uses its own duplicate detection by default, which interferes with
+# yabci's approach. Disable it therefore. The variable `HOOKS` is needed to
+# disable it within fava as well, see
+# https://github.com/beancount/fava/issues/1197 and
+# https://github.com/beancount/fava/issues/1184
+
+HOOKS = []
+
+if __name__ == "main":
+    ingest(CONFIG, hooks=[])
 
 ```
 
 This creates transactions with meta data `duplication_key`:
 
 ```beancount
 2023-01-01 * "foo transaction"
```

### Comparing `yabci-0.1.1/tests/test_examples.py` & `yabci-0.2.0/tests/test_examples.py`

 * *Files identical despite different names*

### Comparing `yabci-0.1.1/tests/test_importer.py` & `yabci-0.2.0/tests/test_importer.py`

 * *Files identical despite different names*

