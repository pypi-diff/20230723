# Comparing `tmp/tradezero_api-0.3.0.tar.gz` & `tmp/tradezero_api-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tradezero_api-0.3.0.tar", max compression
+gzip compressed data, was "tradezero_api-0.3.1.tar", max compression
```

## Comparing `tradezero_api-0.3.0.tar` & `tradezero_api-0.3.1.tar`

### file list

```diff
@@ -1,12 +1,12 @@
--rw-r--r--   0        0        0     1092 2023-03-09 22:58:53.153717 tradezero_api-0.3.0/LICENSE
--rw-r--r--   0        0        0     1120 2023-03-09 23:24:42.796849 tradezero_api-0.3.0/pyproject.toml
--rw-r--r--   0        0        0     4348 2023-03-09 23:22:33.065876 tradezero_api-0.3.0/README.md
--rw-r--r--   0        0        0      123 2023-03-09 23:08:55.266662 tradezero_api-0.3.0/tradezero_api/__init__.py
--rw-r--r--   0        0        0     2357 2023-03-09 22:58:53.156718 tradezero_api-0.3.0/tradezero_api/account.py
--rw-r--r--   0        0        0      816 2023-03-09 22:58:53.157718 tradezero_api-0.3.0/tradezero_api/enums.py
--rw-r--r--   0        0        0    21395 2023-03-09 22:58:53.157718 tradezero_api-0.3.0/tradezero_api/main.py
--rw-r--r--   0        0        0     2920 2023-03-09 22:58:53.158720 tradezero_api-0.3.0/tradezero_api/notification.py
--rw-r--r--   0        0        0     4827 2023-03-09 22:58:53.159723 tradezero_api-0.3.0/tradezero_api/portfolio.py
--rw-r--r--   0        0        0     1518 2023-03-09 22:58:53.160716 tradezero_api-0.3.0/tradezero_api/time_helpers.py
--rw-r--r--   0        0        0     4705 2023-03-09 22:58:53.160716 tradezero_api-0.3.0/tradezero_api/watchlist.py
--rw-r--r--   0        0        0     5488 1970-01-01 00:00:00.000000 tradezero_api-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0     1071 2023-07-22 13:52:10.301013 tradezero_api-0.3.1/LICENSE
+-rw-r--r--   0        0        0     4235 2023-07-22 13:52:10.301013 tradezero_api-0.3.1/README.md
+-rw-r--r--   0        0        0     1082 2023-07-23 00:32:45.058098 tradezero_api-0.3.1/pyproject.toml
+-rw-r--r--   0        0        0      119 2023-07-22 13:52:10.301013 tradezero_api-0.3.1/tradezero_api/__init__.py
+-rw-r--r--   0        0        0     2293 2023-07-22 13:52:10.301013 tradezero_api-0.3.1/tradezero_api/account.py
+-rw-r--r--   0        0        0      779 2023-07-22 13:52:10.301013 tradezero_api-0.3.1/tradezero_api/enums.py
+-rw-r--r--   0        0        0    20908 2023-07-22 13:52:10.301013 tradezero_api-0.3.1/tradezero_api/main.py
+-rw-r--r--   0        0        0     2848 2023-07-22 13:52:10.301013 tradezero_api-0.3.1/tradezero_api/notification.py
+-rw-r--r--   0        0        0     5175 2023-07-22 14:14:38.851606 tradezero_api-0.3.1/tradezero_api/portfolio.py
+-rw-r--r--   0        0        0     1464 2023-07-22 13:52:10.301013 tradezero_api-0.3.1/tradezero_api/time_helpers.py
+-rw-r--r--   0        0        0     4576 2023-07-22 13:52:10.301013 tradezero_api-0.3.1/tradezero_api/watchlist.py
+-rw-r--r--   0        0        0     5484 1970-01-01 00:00:00.000000 tradezero_api-0.3.1/PKG-INFO
```

### Comparing `tradezero_api-0.3.0/LICENSE` & `tradezero_api-0.3.1/LICENSE`

 * *Ordering differences only*

 * *Files 23% similar despite different names*

```diff
@@ -1,21 +1,21 @@
-MIT License
-
-Copyright (c) 2022 Shneor Elmaleh
-
-Permission is hereby granted, free of charge, to any person obtaining a copy
-of this software and associated documentation files (the "Software"), to deal
-in the Software without restriction, including without limitation the rights
-to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
-copies of the Software, and to permit persons to whom the Software is
-furnished to do so, subject to the following conditions:
-
-The above copyright notice and this permission notice shall be included in all
-copies or substantial portions of the Software.
-
-THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
-IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
-FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
-AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
-LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
-OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
-SOFTWARE.
+MIT License
+
+Copyright (c) 2022 Shneor Elmaleh
+
+Permission is hereby granted, free of charge, to any person obtaining a copy
+of this software and associated documentation files (the "Software"), to deal
+in the Software without restriction, including without limitation the rights
+to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+copies of the Software, and to permit persons to whom the Software is
+furnished to do so, subject to the following conditions:
+
+The above copyright notice and this permission notice shall be included in all
+copies or substantial portions of the Software.
+
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+SOFTWARE.
```

### Comparing `tradezero_api-0.3.0/pyproject.toml` & `tradezero_api-0.3.1/pyproject.toml`

 * *Files 22% similar despite different names*

```diff
@@ -1,38 +1,38 @@
-[tool.poetry]
-name = "tradezero-api"
-version = "0.3.0"
-description = "A package for executing orders and retrieving data through the TradeZero web platform"
-authors = ["shner-elmo <770elmo@gmail.com>"]
-license = "MIT"
-readme = "README.md"
-packages = [{include = "tradezero_api"}]
-repository = "https://github.com/shner-elmo/db-wrapper"
-documentation = "https://github.com/shner-elmo/tradezero-api/blob/master/README.md"
-classifiers = [
-    "License :: OSI Approved :: MIT License",
-    "Operating System :: OS Independent",
-    "Environment :: Console",
-    "Programming Language :: Python",
-    "Programming Language :: Python :: 3",
-    "Programming Language :: Python :: 3 :: Only",
-]
-
-[tool.poetry.urls]
-issues = "https://github.com/shner-elmo/tradezero-api/issues"
-
-[tool.poetry.dependencies]
-python = "^3.10"
-selenium = "^4.8.2"
-webdriver-manager = "^3.8.5"
-pandas = "^1.5.3"
-lxml = "^4.9.2"
-pytz = "^2022.7.1"
-termcolor = "^2.2.0"
-
-
-[tool.poetry.group.dev.dependencies]
-ipython = "^8.11.0"
-
-[build-system]
-requires = ["poetry-core"]
-build-backend = "poetry.core.masonry.api"
+[tool.poetry]
+name = "tradezero-api"
+version = "0.3.1"
+description = "A package for executing orders and retrieving data through the TradeZero web platform"
+authors = ["shner-elmo <770elmo@gmail.com>"]
+license = "MIT"
+readme = "README.md"
+packages = [{include = "tradezero_api"}]
+repository = "https://github.com/shner-elmo/db-wrapper"
+documentation = "https://github.com/shner-elmo/tradezero-api/blob/master/README.md"
+classifiers = [
+    "License :: OSI Approved :: MIT License",
+    "Operating System :: OS Independent",
+    "Environment :: Console",
+    "Programming Language :: Python",
+    "Programming Language :: Python :: 3",
+    "Programming Language :: Python :: 3 :: Only",
+]
+
+[tool.poetry.urls]
+issues = "https://github.com/shner-elmo/tradezero-api/issues"
+
+[tool.poetry.dependencies]
+python = ">=3.9"
+selenium = "^4.8.2"
+webdriver-manager = "^3.8.5"
+pandas = "^1.5.3"
+lxml = "^4.9.2"
+pytz = "^2022.7.1"
+termcolor = "^2.2.0"
+
+
+[tool.poetry.group.dev.dependencies]
+ipython = "^8.11.0"
+
+[build-system]
+requires = ["poetry-core"]
+build-backend = "poetry.core.masonry.api"
```

### Comparing `tradezero_api-0.3.0/README.md` & `tradezero_api-0.3.1/README.md`

 * *Ordering differences only*

 * *Files 11% similar despite different names*

```diff
@@ -1,113 +1,113 @@
-# tradezero-api
-
-### Non-official TradeZero API
-
-
----
-[![PyPi](https://img.shields.io/badge/PyPi-0.3.0-yellow)](https://pypi.org/project/tradezero-api/)
-[![Downloads](https://pepy.tech/badge/tradezero-api)](https://pepy.tech/project/tradezero-api)
-[![Downloads](https://pepy.tech/badge/tradezero-api/month)](https://pepy.tech/project/tradezero-api)
-
-You can get the package directly from [PyPI](https://pypi.org/project/tradezero-api/)
-```
-pip install tradezero-api
-```
----
-
-
-<br />
-This connection is obtained by logging onto TZ's ZeroFree web platform with Selenium, and therefore the window must always remain open for the driver to interact with the elements.<br />
-The following guide will show you how to get started using the TradeZero API, and how to use some of the most common methods, if you still want to learn more check out the docs, good luck!<br /><br />
-To create the connection you must instantiate the TradeZero class and provide the following arguments:
-
-```python
-from tradezero_api import TradeZero
-
-tz = TradeZero(user_name='username', password='password')
-tz.login()
-```
-If some time has passed since we've logged in and we want to execute something, we can make sure the connection is still active by calling tz.conn() like so:
-```python
-tz.conn()
-```
-Popular data Property Values
-```python
-aapl = tz.data('AAPL')
-print(f'bid: {aapl.bid}, ask: {aapl.ask}, volume: {aapl.volume}')
-```
-```
-'bid: 145.18, ask: 145.21, volume: 86473580.0'
-```
-For more properties check out the docstring for this method.  
-
-Place a Market Order:
-```python
-from tradezero_api import Order
-
-tz.market_order(Order.SHORT, 'AAPL', 200)  
-```
-Check if we alredy own a Stock, otherwise: place a Buy Limit order:
-```python
-if not tz.Portfolio.invested('AMD'):
-    limit_price = tz.data('AMD').ask + 0.02
-    tz.limit_order(Order.BUY, 'AMD', 100, limit_price)
-```
-Get last three Notifications:
-```python
-notifications = tz.Notification.get_notifications(3)
-print(notifications)
-# returns a nested list with time, title, and message
-```
-```
-[['17:57:22', 'Level 2', 'You are not authorized for symbol: AMD'],
- ['17:57:22', 'Error', 'You are not authorized for symbol: AMD'],
- ['17:50:04', 'Level 2', 'You are not authorized for symbol: AAPL']]
-```
-Locate 100 shares of UBER
-```python
-# max_price is the max amount in USD we're willing to pay for the shares
-tz.locate_stock('uber', 100, max_price=0.10)
-```
-To credit located shares:
-```python
-tz.credit_locates('uber')
-```
-Finally, once you're done using the module, before closing it you should close the driver like so:
-```python
-tz.exit()
-```
-
-### Accessing Bid, Ask and Last prices faster
-So far we have covered accessing data for a given stock with ```tz.data(stock)```  
-but there is another way to access the Bid, Ask and Last prices, and that is directly from  
-the attributes:
-```python
-print(f'Bid: {tz.bid}, Ask: {tz.ask}, Last: {tz.last}')
-```
-```
-Bid: 22.11, Ask: 22.13, Last: 22.12
-```
-The advantage of using the attribute instead of tz.data(), is that its much faster, 
-as it takes about 20ms to locate each property, and tz.data() will locate all eight properties
-even if youre just going to use one of them.  
-tz.bid on the other hand locates only one property so it will take about 20ms 
-to fetch the price.  
-However the disadvantage of using tz.bid is that it will simply show the 
-bid of the symbol that is currently present in the top panel, which in our case is UBER 
-because we called tz.locate_stock()  
-But we can make sure that the current symbol is what we expect like so:  
-```python
-symbol = 'amd'
-if tz.current_symbol() == symbol.upper():
-    print(f'Bid: {tz.bid}')
-```
-The current_symbol() method will add about 25ms, so in total it will be roughly 50ms 
-using our previous example.  
-
-In conclusion, when should we use tz.data().bid ? and when should we use the faster tz.bid method ?  
-if we are sure that the current symbol is the correct one, use: ```tz.bid```  
-But if we are not sure whats the current symbol, then use: ```tz.data(stock).bid```  
-
-Although we can still use tz.bid in combination with tz.current_symbol() like the example above,  
-but if the symbol isnt what we expect than it will do nothing, so better to stick with those
-two options.
+# tradezero-api
+
+### Non-official TradeZero API
+
+
+---
+[![PyPi](https://img.shields.io/badge/PyPi-0.3.0-yellow)](https://pypi.org/project/tradezero-api/)
+[![Downloads](https://pepy.tech/badge/tradezero-api)](https://pepy.tech/project/tradezero-api)
+[![Downloads](https://pepy.tech/badge/tradezero-api/month)](https://pepy.tech/project/tradezero-api)
+
+You can get the package directly from [PyPI](https://pypi.org/project/tradezero-api/)
+```
+pip install tradezero-api
+```
+---
+
+
+<br />
+This connection is obtained by logging onto TZ's ZeroFree web platform with Selenium, and therefore the window must always remain open for the driver to interact with the elements.<br />
+The following guide will show you how to get started using the TradeZero API, and how to use some of the most common methods, if you still want to learn more check out the docs, good luck!<br /><br />
+To create the connection you must instantiate the TradeZero class and provide the following arguments:
+
+```python
+from tradezero_api import TradeZero
+
+tz = TradeZero(user_name='username', password='password')
+tz.login()
+```
+If some time has passed since we've logged in and we want to execute something, we can make sure the connection is still active by calling tz.conn() like so:
+```python
+tz.conn()
+```
+Popular data Property Values
+```python
+aapl = tz.data('AAPL')
+print(f'bid: {aapl.bid}, ask: {aapl.ask}, volume: {aapl.volume}')
+```
+```
+'bid: 145.18, ask: 145.21, volume: 86473580.0'
+```
+For more properties check out the docstring for this method.  
+
+Place a Market Order:
+```python
+from tradezero_api import Order
+
+tz.market_order(Order.SHORT, 'AAPL', 200)  
+```
+Check if we alredy own a Stock, otherwise: place a Buy Limit order:
+```python
+if not tz.Portfolio.invested('AMD'):
+    limit_price = tz.data('AMD').ask + 0.02
+    tz.limit_order(Order.BUY, 'AMD', 100, limit_price)
+```
+Get last three Notifications:
+```python
+notifications = tz.Notification.get_notifications(3)
+print(notifications)
+# returns a nested list with time, title, and message
+```
+```
+[['17:57:22', 'Level 2', 'You are not authorized for symbol: AMD'],
+ ['17:57:22', 'Error', 'You are not authorized for symbol: AMD'],
+ ['17:50:04', 'Level 2', 'You are not authorized for symbol: AAPL']]
+```
+Locate 100 shares of UBER
+```python
+# max_price is the max amount in USD we're willing to pay for the shares
+tz.locate_stock('uber', 100, max_price=0.10)
+```
+To credit located shares:
+```python
+tz.credit_locates('uber')
+```
+Finally, once you're done using the module, before closing it you should close the driver like so:
+```python
+tz.exit()
+```
+
+### Accessing Bid, Ask and Last prices faster
+So far we have covered accessing data for a given stock with ```tz.data(stock)```  
+but there is another way to access the Bid, Ask and Last prices, and that is directly from  
+the attributes:
+```python
+print(f'Bid: {tz.bid}, Ask: {tz.ask}, Last: {tz.last}')
+```
+```
+Bid: 22.11, Ask: 22.13, Last: 22.12
+```
+The advantage of using the attribute instead of tz.data(), is that its much faster, 
+as it takes about 20ms to locate each property, and tz.data() will locate all eight properties
+even if youre just going to use one of them.  
+tz.bid on the other hand locates only one property so it will take about 20ms 
+to fetch the price.  
+However the disadvantage of using tz.bid is that it will simply show the 
+bid of the symbol that is currently present in the top panel, which in our case is UBER 
+because we called tz.locate_stock()  
+But we can make sure that the current symbol is what we expect like so:  
+```python
+symbol = 'amd'
+if tz.current_symbol() == symbol.upper():
+    print(f'Bid: {tz.bid}')
+```
+The current_symbol() method will add about 25ms, so in total it will be roughly 50ms 
+using our previous example.  
+
+In conclusion, when should we use tz.data().bid ? and when should we use the faster tz.bid method ?  
+if we are sure that the current symbol is the correct one, use: ```tz.bid```  
+But if we are not sure whats the current symbol, then use: ```tz.data(stock).bid```  
+
+Although we can still use tz.bid in combination with tz.current_symbol() like the example above,  
+but if the symbol isnt what we expect than it will do nothing, so better to stick with those
+two options.
```

### Comparing `tradezero_api-0.3.0/tradezero_api/account.py` & `tradezero_api-0.3.1/tradezero_api/account.py`

 * *Ordering differences only*

 * *Files 24% similar despite different names*

```diff
@@ -1,64 +1,64 @@
-from __future__ import annotations
-
-import warnings
-from collections import namedtuple
-
-from selenium.webdriver.common.by import By
-
-
-class Account:
-    def __init__(self, driver):
-        self.driver = driver
-        self.attribute_ids = [
-            "h-realized-value",
-            "h-unrealizd-pl-value",
-            "h-total-pl-value",
-            "p-bp",
-            "h-cash-value",
-            "h-exposure-value",
-            "h-equity-value",
-            "h-equity-ratio-value",
-            "h-used-lvg-value",
-            "p-allowed-lev",
-            "h-select-account",
-            "h-loginId",
-            "trading-order-label-account",
-        ]
-
-    def hide_attributes(self):
-        """
-        Hides all account attributes i.e, account username, equity-value, cash-value, realized-value...
-        """
-        for id_ in self.attribute_ids:
-            element = self.driver.find_element(By.ID, id_)
-            self.driver.execute_script("arguments[0].setAttribute('style', 'display: none;')", element)
-
-    @property
-    def attributes(self):
-        """
-        returns a namedtuple with the account following properties:
-        realized_pnl, unrealized_pnl, total_pnl, buying_power, cash,
-        exposure, equity, equity_ratio, used_lvg, allowed_lvg.
-        note that if one or more of the attributes have been hidden; either by
-        setting self.hide_attributes = True or by calling hide_attributes(),
-        a namedtuple will be returned with None values.
-
-        :return: namedtuple
-        """
-        Data = namedtuple('Data', ['realized_pnl', 'unrealized_pnl', 'total_pnl', 'buying_power', 'cash',
-                                   'exposure', 'equity', 'equity_ratio', 'used_lvg', 'allowed_lvg'])
-
-        attribute_ids = self.attribute_ids[:-3]
-        values = []
-        for id_ in attribute_ids:
-            element = self.driver.find_element(By.ID, id_)
-
-            if element.get_attribute('style') == 'display: none;':
-                warnings.warn('cannot fetch attribute that has been hidden')
-
-                empty_list = [None] * len(attribute_ids)
-                return Data._make(empty_list)
-
-            value = element.text.translate(str.maketrans('', '', '$%x,'))
-            values.append(float(value))
-        return Data._make(values)
+from __future__ import annotations
+
+import warnings
+from collections import namedtuple
+
+from selenium.webdriver.common.by import By
+
+
+class Account:
+    def __init__(self, driver):
+        self.driver = driver
+        self.attribute_ids = [
+            "h-realized-value",
+            "h-unrealizd-pl-value",
+            "h-total-pl-value",
+            "p-bp",
+            "h-cash-value",
+            "h-exposure-value",
+            "h-equity-value",
+            "h-equity-ratio-value",
+            "h-used-lvg-value",
+            "p-allowed-lev",
+            "h-select-account",
+            "h-loginId",
+            "trading-order-label-account",
+        ]
+
+    def hide_attributes(self):
+        """
+        Hides all account attributes i.e, account username, equity-value, cash-value, realized-value...
+        """
+        for id_ in self.attribute_ids:
+            element = self.driver.find_element(By.ID, id_)
+            self.driver.execute_script("arguments[0].setAttribute('style', 'display: none;')", element)
+
+    @property
+    def attributes(self):
+        """
+        returns a namedtuple with the account following properties:
+        realized_pnl, unrealized_pnl, total_pnl, buying_power, cash,
+        exposure, equity, equity_ratio, used_lvg, allowed_lvg.
+        note that if one or more of the attributes have been hidden; either by
+        setting self.hide_attributes = True or by calling hide_attributes(),
+        a namedtuple will be returned with None values.
+
+        :return: namedtuple
+        """
+        Data = namedtuple('Data', ['realized_pnl', 'unrealized_pnl', 'total_pnl', 'buying_power', 'cash',
+                                   'exposure', 'equity', 'equity_ratio', 'used_lvg', 'allowed_lvg'])
+
+        attribute_ids = self.attribute_ids[:-3]
+        values = []
+        for id_ in attribute_ids:
+            element = self.driver.find_element(By.ID, id_)
+
+            if element.get_attribute('style') == 'display: none;':
+                warnings.warn('cannot fetch attribute that has been hidden')
+
+                empty_list = [None] * len(attribute_ids)
+                return Data._make(empty_list)
+
+            value = element.text.translate(str.maketrans('', '', '$%x,'))
+            values.append(float(value))
+        return Data._make(values)
```

### Comparing `tradezero_api-0.3.0/tradezero_api/enums.py` & `tradezero_api-0.3.1/tradezero_api/enums.py`

 * *Ordering differences only*

 * *Files 23% similar despite different names*

```diff
@@ -1,37 +1,37 @@
-from __future__ import annotations
-
-from enum import Enum
-
-
-class OrderType(str, Enum):
-    """All the order-types available in the drop-down menu"""
-    market = 'MKT'
-    limit = 'LMT'
-    stop = 'Stop-MKT'
-    stop_limit = 'Stop-LMT'
-    market_on_close = 'MKT-Close'
-    limit_on_close = 'LMT-Close'
-    range = 'RANGE'
-
-
-class TIF(str, Enum):
-    """Time-in-force values"""
-    DAY = 'DAY'
-    GTC = 'GTC'
-    GTX = 'GTX'
-
-
-class Order(str, Enum):
-    """Order types"""
-    BUY = 'buy'
-    SELL = 'sell'
-    SHORT = 'short'
-    COVER = 'cover'
-
-
-class PortfolioTab(str, Enum):
-    """The ID for each """
-    open_positions = 'portfolio-tab-op-1'
-    closed_positions = 'portfolio-tab-cp-1'
-    active_orders = 'portfolio-tab-ao-1'
-    inactive_orders = 'portfolio-tab-io-1'
+from __future__ import annotations
+
+from enum import Enum
+
+
+class OrderType(str, Enum):
+    """All the order-types available in the drop-down menu"""
+    market = 'MKT'
+    limit = 'LMT'
+    stop = 'Stop-MKT'
+    stop_limit = 'Stop-LMT'
+    market_on_close = 'MKT-Close'
+    limit_on_close = 'LMT-Close'
+    range = 'RANGE'
+
+
+class TIF(str, Enum):
+    """Time-in-force values"""
+    DAY = 'DAY'
+    GTC = 'GTC'
+    GTX = 'GTX'
+
+
+class Order(str, Enum):
+    """Order types"""
+    BUY = 'buy'
+    SELL = 'sell'
+    SHORT = 'short'
+    COVER = 'cover'
+
+
+class PortfolioTab(str, Enum):
+    """The ID for each """
+    open_positions = 'portfolio-tab-op-1'
+    closed_positions = 'portfolio-tab-cp-1'
+    active_orders = 'portfolio-tab-ao-1'
+    inactive_orders = 'portfolio-tab-io-1'
```

### Comparing `tradezero_api-0.3.0/tradezero_api/main.py` & `tradezero_api-0.3.1/tradezero_api/main.py`

 * *Ordering differences only*

 * *Files 15% similar despite different names*

```diff
@@ -1,487 +1,487 @@
-from __future__ import annotations
-
-import time
-import os
-import warnings
-from collections import namedtuple
-
-from selenium.webdriver.chrome.service import Service as ChromeService
-from webdriver_manager.chrome import ChromeDriverManager
-from selenium import webdriver
-from selenium.webdriver.common.by import By
-from selenium.webdriver.common.keys import Keys
-from selenium.webdriver.support.ui import Select
-from selenium.common.exceptions import NoSuchElementException, WebDriverException, StaleElementReferenceException
-from termcolor import colored
-
-from .time_helpers import Time, Timer, time_it
-from .watchlist import Watchlist
-from .portfolio import Portfolio
-from .notification import Notification
-from .account import Account
-from .enums import Order, TIF
-
-os.system('color')
-
-TZ_HOME_URL = 'https://standard.tradezeroweb.us/'
-
-
-class TradeZero(Time):
-    def __init__(self, user_name: str, password: str, headless: bool = False,
-                 hide_attributes: bool = False):
-        """
-        :param user_name: TradeZero user_name
-        :param password: TradeZero password
-        :param headless: default: False, True will run the browser in headless mode, which means it won't be visible
-        :param hide_attributes: bool, if True: Hide account attributes (acc username, equity, total exposure...)
-        """
-        super().__init__()
-        self.user_name = user_name
-        self.password = password
-        self.hide_attributes = hide_attributes
-
-        service = ChromeService(ChromeDriverManager().install())
-        options = webdriver.ChromeOptions()
-        options.add_experimental_option('excludeSwitches', ['enable-logging'])
-        if headless is True:
-            options.headless = headless
-
-        self.driver = webdriver.Chrome(service=service, options=options)
-        self.driver.get(TZ_HOME_URL)
-
-        self.Watchlist = Watchlist(self.driver)
-        self.Portfolio = Portfolio(self.driver)
-        self.Notification = Notification(self.driver)
-        self.Account = Account(self.driver)
-
-        # to instantiate the time, pytz, and datetime modules:
-        Timer()
-        self.time_between(time1=(9, 30), time2=(10, 30))
-
-    def _dom_fully_loaded(self, iter_amount: int = 1):
-        """
-        check that webpage elements are fully loaded/visible.
-        there is no need to call this method, but instead call tz_conn() and that will take care of all the rest.
-
-        :param iter_amount: int, default: 1, number of times it will iterate.
-        :return: if the elements are fully loaded: return True, else: return False.
-        """
-        container_xpath = "//*[contains(@id,'portfolio-container')]//div//div//h2"
-        for i in range(iter_amount):
-            elements = self.driver.find_elements(By.XPATH, container_xpath)
-            text_elements = [x.text for x in elements]
-            if 'Portfolio' in text_elements:
-                return True
-            time.sleep(0.5)
-        return False
-
-    @time_it
-    def login(self, log_time_elapsed: bool = False):
-        """
-        log-in TradeZero's website
-
-        :param log_time_elapsed: bool, if True it will print time elapsed for login
-        """
-        login_form = self.driver.find_element(By.ID, "login")
-        login_form.send_keys(self.user_name)
-
-        password_form = self.driver.find_element(By.ID, "password")
-        password_form.send_keys(self.password, Keys.RETURN)
-
-        self._dom_fully_loaded(150)
-        if self.hide_attributes:
-            self.Account.hide_attributes()
-
-        Select(self.driver.find_element(By.ID, "trading-order-select-type")).select_by_index(1)
-
-    def conn(self, log_tz_conn: bool = False):
-        """
-        make sure that the website stays connected and is fully loaded.
-        TradeZero will ask for a Login twice a day, and sometimes it will require the page to be reloaded,
-        so this will make sure that its fully loaded, by reloading or doing the login.
-
-        :param log_tz_conn: bool, default: False. if True it will print if it reconnects through the login or refresh.
-        :return: True if connected
-        :raises Exception: if it fails to reconnect after a while
-        """
-        if self._dom_fully_loaded(1):
-            return True
-
-        try:
-            self.driver.find_element(By.ID, "login")
-            self.login()
-
-            self.Watchlist.restore()
-
-            if log_tz_conn is True:
-                print(colored('tz_conn(): Login worked', 'cyan'))
-            return True
-
-        except NoSuchElementException:
-            self.driver.get("https://standard.tradezeroweb.us/")
-            if self._dom_fully_loaded(150):
-
-                if self.hide_attributes:
-                    self.Account.hide_attributes()
-
-                self.Watchlist.restore()
-
-                if log_tz_conn is True:
-                    print(colored('tz_conn(): Refresh worked', 'cyan'))
-                return True
-
-        raise Exception('@ tz_conn(): Error: not able to reconnect, max retries exceeded')
-
-    def exit(self):
-        """close Selenium window and driver"""
-        try:
-            self.driver.close()
-        except WebDriverException:
-            pass
-
-        self.driver.quit()
-
-    def load_symbol(self, symbol: str):
-        """
-        make sure the data for the symbol is fully loaded and that the symbol itself is valid
-
-        :param symbol: str
-        :return: True if symbol data loaded, False if prices == 0.00 (mkt closed), Error if symbol not found
-        :raises Exception: if symbol not found
-        """
-        if symbol.upper() == self.current_symbol():
-            price = self.driver.find_element(By.ID, "trading-order-ask").text.replace('.', '').replace(',', '')
-            if price.isdigit() and float(price) > 0:
-                return True
-
-        input_symbol = self.driver.find_element(By.ID, "trading-order-input-symbol")
-        input_symbol.send_keys(symbol.lower(), Keys.RETURN)
-        time.sleep(0.04)
-
-        for i in range(300):
-            price = self.driver.find_element(By.ID, "trading-order-ask").text.replace('.', '').replace(',', '')
-            if price == '':
-                time.sleep(0.01)
-
-            elif price.isdigit() and float(price) == 0:
-                warnings.warn(f"Market Closed, ask/bid = {price}")
-                return False
-
-            elif price.isdigit():
-                return True
-
-            elif i == 15 or i == 299:
-                last_notif = self.Notification.get_last_notification_message()
-                message = f'Symbol not found: {symbol.upper()}'
-                if message == last_notif:
-                    raise Exception(f"ERROR: {symbol=} Not found")
-
-    def current_symbol(self):
-        """get current symbol"""
-        return self.driver.find_element(By.ID, 'trading-order-symbol').text.replace('(USD)', '')
-
-    @property
-    def bid(self):
-        """get bid price"""
-        return float(self.driver.find_element(By.ID, 'trading-order-bid').text.replace(',', ''))
-
-    @property
-    def ask(self):
-        """get ask price"""
-        return float(self.driver.find_element(By.ID, 'trading-order-ask').text.replace(',', ''))
-
-    @property
-    def last(self):
-        """get last price"""
-        return float(self.driver.find_element(By.ID, 'trading-order-p').text.replace(',', ''))
-
-    def data(self, symbol: str):
-        """
-        return a namedtuple with data for the given symbol, the properties are:
-        'open', 'high', 'low', 'close', 'volume', 'last', 'ask', 'bid'.
-
-        :param symbol: str: ex: 'aapl', 'amd', 'NVDA', 'GM'
-        :return: namedtuple = (open, high, low, close, volume, last, ask, bid)
-        """
-        Data = namedtuple('Data', ['open', 'high', 'low', 'close', 'volume', 'last', 'ask', 'bid'])
-
-        if self.load_symbol(symbol) is False:
-            return Data(0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0)
-
-        element_ids = [
-            'trading-order-open',
-            'trading-order-high',
-            'trading-order-low',
-            'trading-order-close',
-            'trading-order-vol',
-            'trading-order-p',
-            'trading-order-ask',
-            'trading-order-bid',
-        ]
-        lst = []
-        for id_ in element_ids:
-            val = self.driver.find_element(By.ID, id_).text
-            val = float(val.replace(',', ''))  # replace comma for volume, and when prices > 999
-            lst.append(val)
-
-        return Data._make(lst)
-
-    def calculate_order_quantity(self, symbol: str, buying_power: float, float_option: bool = False):
-        """
-        returns the amount of shares you can buy with the given buying_power as int(), but if float_option is True,
-        it will return the amount as a float.
-
-        :param symbol: str
-        :param buying_power: float,
-        :param float_option: bool, default: False, if True returns the original number as float
-        :return: int or float
-        """
-        if self.load_symbol(symbol) is False:
-            return
-        quantity = (buying_power / self.last)
-
-        if float_option is True:
-            return quantity
-        return int(quantity)
-
-    def locate_stock(self, symbol: str, share_amount: int, max_price: float = 0, debug_info: bool = False):
-        """
-        Locate a stock, requires: stock symbol, and share_amount. optional: max_price.
-        if the locate_price is less than max_price: it will accept, else: decline.
-
-        :param symbol: str, symbol to locate.
-        :param share_amount: int, must be a multiple of 100 (100, 200, 300...)
-        :param max_price: float, default: 0, total price you are willing to pay for locates
-        :param debug_info: bool, if True it will print info about the locates in the console
-        :return: named tuple with the following attributes: 'price_per_share' and 'total'
-        :raises Exception: if share_amount is not divisible by 100
-        """
-        Data = namedtuple('Data', ['price_per_share', 'total'])
-
-        if share_amount is not None and share_amount % 100 != 0:
-            raise Exception(f'ERROR: share_amount is not divisible by 100 ({share_amount=})')
-
-        if not self.load_symbol(symbol):
-            return
-
-        if self.last <= 1.00:
-            print(f'Error: Cannot locate stocks priced under $1.00 ({symbol=}, price={self.last})')
-
-        self.driver.find_element(By.ID, "locate-tab-1").click()
-        input_symbol = self.driver.find_element(By.ID, "short-list-input-symbol")
-        input_symbol.clear()
-        input_symbol.send_keys(symbol, Keys.RETURN)
-
-        input_shares = self.driver.find_element(By.ID, "short-list-input-shares")
-        input_shares.clear()
-        input_shares.send_keys(share_amount)
-
-        while self.driver.find_element(By.ID, "short-list-locate-status").text == '':
-            time.sleep(0.1)
-
-        if self.driver.find_element(By.ID, "short-list-locate-status").text == 'Easy to borrow':
-            locate_pps = 0.00
-            locate_total = 0.00
-            if debug_info:
-                print(colored(f'Stock ({symbol}) is "Easy to borrow"', 'green'))
-            return Data(locate_pps, locate_total)
-
-        self.driver.find_element(By.ID, "short-list-button-locate").click()
-
-        for i in range(300):
-            try:
-                locate_pps = float(self.driver.find_element(By.ID, f"oitem-l-{symbol.upper()}-cell-2").text)
-                locate_total = float(self.driver.find_element(By.ID, f"oitem-l-{symbol.upper()}-cell-6").text)
-                break
-
-            except (ValueError, NoSuchElementException, StaleElementReferenceException):
-                time.sleep(0.15)
-                if i == 15 or i == 299:
-                    insufficient_bp = 'Insufficient BP to short a position with requested quantity.'
-                    last_notif = self.Notification.get_last_notification_message()
-                    if insufficient_bp in last_notif:
-                        warnings.warn(f"ERROR! {insufficient_bp}")
-                        return
-        else:
-            raise Exception(f'Error: not able to locate symbol element ({symbol=})')
-
-        if locate_total <= max_price:
-            self.driver.find_element(By.XPATH, f'//*[@id="oitem-l-{symbol.upper()}-cell-8"]/span[1]').click()
-            if debug_info:
-                print(colored(f'HTB Locate accepted ({symbol}, $ {locate_total})', 'cyan'))
-        else:
-            self.driver.find_element(By.XPATH, f'//*[@id="oitem-l-{symbol.upper()}-cell-8"]/span[2]').click()
-
-        return Data(locate_pps, locate_total)
-        # TODO create a function to get the pps and another one that just locates the shares
-
-    def credit_locates(self, symbol: str, quantity=None):
-        """
-        sell/ credit stock locates, if no value is given in 'quantity', it will credit all the shares
-        available of the given symbol.
-
-        :param symbol: str
-        :param quantity: amount of shares to sell, must be a multiple of 100, ie: 100, 200, 300
-        :return:
-        :raises Exception: if given symbol in not already located
-        :raises ValueError: if quantity is not divisible by 100 or quantity > located shares
-        """
-        located_symbols = self.driver.find_elements(By.XPATH, '//*[@id="locate-inventory-table"]/tbody/tr/td[1]')
-        located_symbols = [x.text for x in located_symbols]
-
-        if symbol.upper() not in located_symbols:
-            raise Exception(f"ERROR! cannot find {symbol} in located symbols")
-
-        if quantity is not None:
-            if quantity % 100 != 0:
-                raise ValueError(f"ERROR! quantity is not divisible by 100 ({quantity=})")
-
-            located_shares = float(self.driver.find_element(By.ID, f"inv-{symbol.upper()}-cell-1").text)
-            if quantity > located_shares:
-                raise ValueError(f"ERROR! you cannot credit more shares than u already have "
-                                 f"({quantity} vs {located_shares}")
-
-            input_quantity = self.driver.find_element(By.ID, f"inv-{symbol.upper()}-sell-qty")
-            input_quantity.clear()
-            input_quantity.send_keys(quantity)
-
-        self.driver.find_element(By.XPATH, f'//*[@id="inv-{symbol.upper()}-sell"]/button').click()
-        return
-
-    @time_it
-    def limit_order(self, order_direction: Order, symbol: str, share_amount: int, limit_price: float,
-                    time_in_force: TIF = TIF.DAY, log_info: bool = False):
-        """
-        Place a Limit Order, the following params are required: order_direction, symbol, share_amount, and limit_price.
-
-        :param order_direction: str: 'buy', 'sell', 'short', 'cover'
-        :param symbol: str: e.g: 'aapl', 'amd', 'NVDA', 'GM'
-        :param limit_price: float
-        :param share_amount: int
-        :param time_in_force: str, default: 'DAY', must be one of the following: 'DAY', 'GTC', or 'GTX'
-        :param log_info: bool, if True it will print information about the order
-        :return: True if operation succeeded
-        :raises AttributeError: if time_in_force argument not one of the following: 'DAY', 'GTC', 'GTX'
-        """
-        symbol = symbol.lower()
-        order_direction = order_direction.value
-        time_in_force = time_in_force.value
-
-        if time_in_force not in ['DAY', 'GTC', 'GTX']:
-            raise AttributeError(f"Error: time_in_force argument must be one of the following: 'DAY', 'GTC', 'GTX'")
-
-        self.load_symbol(symbol)
-
-        order_menu = Select(self.driver.find_element(By.ID, "trading-order-select-type"))
-        order_menu.select_by_index(1)
-
-        tif_menu = Select(self.driver.find_element(By.ID, "trading-order-select-time"))
-        tif_menu.select_by_visible_text(time_in_force)
-
-        input_quantity = self.driver.find_element(By.ID, "trading-order-input-quantity")
-        input_quantity.clear()
-        input_quantity.send_keys(share_amount)
-
-        price_input = self.driver.find_element(By.ID, "trading-order-input-price")
-        price_input.clear()
-        price_input.send_keys(limit_price)
-
-        self.driver.find_element(By.ID, f"trading-order-button-{order_direction}").click()
-
-        if log_info is True:
-            print(f"Time: {self.time}, Order direction: {order_direction}, Symbol: {symbol}, "
-                  f"Limit Price: {limit_price}, Shares amount: {share_amount}")
-
-    @time_it
-    def market_order(self, order_direction: Order, symbol: str, share_amount: int,
-                     time_in_force: TIF = TIF.DAY, log_info: bool = False):
-        """
-        Place a Market Order, The following params are required: order_direction, symbol, and share_amount
-
-        :param order_direction: str: 'buy', 'sell', 'short', 'cover'
-        :param symbol: str: e.g: 'aapl', 'amd', 'NVDA', 'GM'
-        :param share_amount: int
-        :param time_in_force: str, default: 'DAY', must be one of the following: 'DAY', 'GTC', or 'GTX'
-        :param log_info: bool, if True it will print information about the order
-        :return:
-        :raises Exception: if time not during market hours (9:30 - 16:00)
-        :raises AttributeError: if time_in_force argument not one of the following: 'DAY', 'GTC', 'GTX'
-        """
-        symbol = symbol.lower()
-        order_direction = order_direction.value
-        time_in_force = time_in_force.value
-
-        if not self.time_between((9, 30), (16, 0)):
-            raise Exception(f'Error: Market orders are not allowed at this time ({self.time})')
-
-        if time_in_force not in ['DAY', 'GTC', 'GTX']:
-            raise AttributeError(f"Error: time_in_force argument must be one of the following: 'DAY', 'GTC', 'GTX'")
-
-        self.load_symbol(symbol)
-
-        order_menu = Select(self.driver.find_element(By.ID, "trading-order-select-type"))
-        order_menu.select_by_index(0)
-
-        tif_menu = Select(self.driver.find_element(By.ID, "trading-order-select-time"))
-        tif_menu.select_by_visible_text(time_in_force)
-
-        input_quantity = self.driver.find_element(By.ID, "trading-order-input-quantity")
-        input_quantity.clear()
-        input_quantity.send_keys(share_amount)
-
-        self.driver.find_element(By.ID, f"trading-order-button-{order_direction}").click()
-
-        if log_info is True:
-            print(f"Time: {self.time}, Order direction: {order_direction}, Symbol: {symbol}, "
-                  f"Price: {self.last}, Shares amount: {share_amount}")
-
-    @time_it
-    def stop_market_order(self, order_direction: Order, symbol: str, share_amount: int, stop_price: float,
-                          time_in_force: TIF = TIF.DAY, log_info: bool = False):
-        """
-        Place a Stop Market Order, the following params are required: order_direction, symbol,
-        share_amount, and stop_price.
-        note that a Stop Market Order can only be placed during market-hours (09:30:00 - 16:00:00), therefore if a
-        Stop Market Order is placed outside market hours it will raise an error.
-
-        :param order_direction: str: 'buy', 'sell', 'short', 'cover'
-        :param symbol: str: e.g: 'aapl', 'amd', 'NVDA', 'GM'
-        :param stop_price: float
-        :param share_amount: int
-        :param time_in_force: str, default: 'DAY', must be one of the following: 'DAY', 'GTC', or 'GTX'
-        :param log_info: bool, if True it will print information about the order
-        :return: True if operation succeeded
-        :raises Exception: if time not during market hours (9:30 - 16:00)
-        :raises AttributeError: if time_in_force argument not one of the following: 'DAY', 'GTC', 'GTX'
-        """
-        symbol = symbol.lower()
-        order_direction = order_direction.value
-        time_in_force = time_in_force.value
-
-        if not self.time_between((9, 30), (16, 0)):
-            raise Exception(f'Error: Stop Market orders are not allowed at this time ({self.time})')
-
-        if time_in_force not in ['DAY', 'GTC', 'GTX']:
-            raise AttributeError(f"Error: time_in_force argument must be one of the following: 'DAY', 'GTC', 'GTX'")
-
-        self.load_symbol(symbol)
-
-        order_menu = Select(self.driver.find_element(By.ID, "trading-order-select-type"))
-        order_menu.select_by_index(2)
-
-        tif_menu = Select(self.driver.find_element(By.ID, "trading-order-select-time"))
-        tif_menu.select_by_visible_text(time_in_force)
-
-        input_quantity = self.driver.find_element(By.ID, "trading-order-input-quantity")
-        input_quantity.clear()
-        input_quantity.send_keys(share_amount)
-
-        price_input = self.driver.find_element(By.ID, "trading-order-input-sprice")
-        price_input.clear()
-        price_input.send_keys(stop_price)
-
-        self.driver.find_element(By.ID, f"trading-order-button-{order_direction}").click()
-
-        if log_info is True:
-            print(f"Time: {self.time}, Order direction: {order_direction}, Symbol: {symbol}, "
-                  f"Stop Price: {stop_price}, Shares amount: {share_amount}")
+from __future__ import annotations
+
+import time
+import os
+import warnings
+from collections import namedtuple
+
+from selenium.webdriver.chrome.service import Service as ChromeService
+from webdriver_manager.chrome import ChromeDriverManager
+from selenium import webdriver
+from selenium.webdriver.common.by import By
+from selenium.webdriver.common.keys import Keys
+from selenium.webdriver.support.ui import Select
+from selenium.common.exceptions import NoSuchElementException, WebDriverException, StaleElementReferenceException
+from termcolor import colored
+
+from .time_helpers import Time, Timer, time_it
+from .watchlist import Watchlist
+from .portfolio import Portfolio
+from .notification import Notification
+from .account import Account
+from .enums import Order, TIF
+
+os.system('color')
+
+TZ_HOME_URL = 'https://standard.tradezeroweb.us/'
+
+
+class TradeZero(Time):
+    def __init__(self, user_name: str, password: str, headless: bool = False,
+                 hide_attributes: bool = False):
+        """
+        :param user_name: TradeZero user_name
+        :param password: TradeZero password
+        :param headless: default: False, True will run the browser in headless mode, which means it won't be visible
+        :param hide_attributes: bool, if True: Hide account attributes (acc username, equity, total exposure...)
+        """
+        super().__init__()
+        self.user_name = user_name
+        self.password = password
+        self.hide_attributes = hide_attributes
+
+        service = ChromeService(ChromeDriverManager().install())
+        options = webdriver.ChromeOptions()
+        options.add_experimental_option('excludeSwitches', ['enable-logging'])
+        if headless is True:
+            options.headless = headless
+
+        self.driver = webdriver.Chrome(service=service, options=options)
+        self.driver.get(TZ_HOME_URL)
+
+        self.Watchlist = Watchlist(self.driver)
+        self.Portfolio = Portfolio(self.driver)
+        self.Notification = Notification(self.driver)
+        self.Account = Account(self.driver)
+
+        # to instantiate the time, pytz, and datetime modules:
+        Timer()
+        self.time_between(time1=(9, 30), time2=(10, 30))
+
+    def _dom_fully_loaded(self, iter_amount: int = 1):
+        """
+        check that webpage elements are fully loaded/visible.
+        there is no need to call this method, but instead call tz_conn() and that will take care of all the rest.
+
+        :param iter_amount: int, default: 1, number of times it will iterate.
+        :return: if the elements are fully loaded: return True, else: return False.
+        """
+        container_xpath = "//*[contains(@id,'portfolio-container')]//div//div//h2"
+        for i in range(iter_amount):
+            elements = self.driver.find_elements(By.XPATH, container_xpath)
+            text_elements = [x.text for x in elements]
+            if 'Portfolio' in text_elements:
+                return True
+            time.sleep(0.5)
+        return False
+
+    @time_it
+    def login(self, log_time_elapsed: bool = False):
+        """
+        log-in TradeZero's website
+
+        :param log_time_elapsed: bool, if True it will print time elapsed for login
+        """
+        login_form = self.driver.find_element(By.ID, "login")
+        login_form.send_keys(self.user_name)
+
+        password_form = self.driver.find_element(By.ID, "password")
+        password_form.send_keys(self.password, Keys.RETURN)
+
+        self._dom_fully_loaded(150)
+        if self.hide_attributes:
+            self.Account.hide_attributes()
+
+        Select(self.driver.find_element(By.ID, "trading-order-select-type")).select_by_index(1)
+
+    def conn(self, log_tz_conn: bool = False):
+        """
+        make sure that the website stays connected and is fully loaded.
+        TradeZero will ask for a Login twice a day, and sometimes it will require the page to be reloaded,
+        so this will make sure that its fully loaded, by reloading or doing the login.
+
+        :param log_tz_conn: bool, default: False. if True it will print if it reconnects through the login or refresh.
+        :return: True if connected
+        :raises Exception: if it fails to reconnect after a while
+        """
+        if self._dom_fully_loaded(1):
+            return True
+
+        try:
+            self.driver.find_element(By.ID, "login")
+            self.login()
+
+            self.Watchlist.restore()
+
+            if log_tz_conn is True:
+                print(colored('tz_conn(): Login worked', 'cyan'))
+            return True
+
+        except NoSuchElementException:
+            self.driver.get("https://standard.tradezeroweb.us/")
+            if self._dom_fully_loaded(150):
+
+                if self.hide_attributes:
+                    self.Account.hide_attributes()
+
+                self.Watchlist.restore()
+
+                if log_tz_conn is True:
+                    print(colored('tz_conn(): Refresh worked', 'cyan'))
+                return True
+
+        raise Exception('@ tz_conn(): Error: not able to reconnect, max retries exceeded')
+
+    def exit(self):
+        """close Selenium window and driver"""
+        try:
+            self.driver.close()
+        except WebDriverException:
+            pass
+
+        self.driver.quit()
+
+    def load_symbol(self, symbol: str):
+        """
+        make sure the data for the symbol is fully loaded and that the symbol itself is valid
+
+        :param symbol: str
+        :return: True if symbol data loaded, False if prices == 0.00 (mkt closed), Error if symbol not found
+        :raises Exception: if symbol not found
+        """
+        if symbol.upper() == self.current_symbol():
+            price = self.driver.find_element(By.ID, "trading-order-ask").text.replace('.', '').replace(',', '')
+            if price.isdigit() and float(price) > 0:
+                return True
+
+        input_symbol = self.driver.find_element(By.ID, "trading-order-input-symbol")
+        input_symbol.send_keys(symbol.lower(), Keys.RETURN)
+        time.sleep(0.04)
+
+        for i in range(300):
+            price = self.driver.find_element(By.ID, "trading-order-ask").text.replace('.', '').replace(',', '')
+            if price == '':
+                time.sleep(0.01)
+
+            elif price.isdigit() and float(price) == 0:
+                warnings.warn(f"Market Closed, ask/bid = {price}")
+                return False
+
+            elif price.isdigit():
+                return True
+
+            elif i == 15 or i == 299:
+                last_notif = self.Notification.get_last_notification_message()
+                message = f'Symbol not found: {symbol.upper()}'
+                if message == last_notif:
+                    raise Exception(f"ERROR: {symbol=} Not found")
+
+    def current_symbol(self):
+        """get current symbol"""
+        return self.driver.find_element(By.ID, 'trading-order-symbol').text.replace('(USD)', '')
+
+    @property
+    def bid(self):
+        """get bid price"""
+        return float(self.driver.find_element(By.ID, 'trading-order-bid').text.replace(',', ''))
+
+    @property
+    def ask(self):
+        """get ask price"""
+        return float(self.driver.find_element(By.ID, 'trading-order-ask').text.replace(',', ''))
+
+    @property
+    def last(self):
+        """get last price"""
+        return float(self.driver.find_element(By.ID, 'trading-order-p').text.replace(',', ''))
+
+    def data(self, symbol: str):
+        """
+        return a namedtuple with data for the given symbol, the properties are:
+        'open', 'high', 'low', 'close', 'volume', 'last', 'ask', 'bid'.
+
+        :param symbol: str: ex: 'aapl', 'amd', 'NVDA', 'GM'
+        :return: namedtuple = (open, high, low, close, volume, last, ask, bid)
+        """
+        Data = namedtuple('Data', ['open', 'high', 'low', 'close', 'volume', 'last', 'ask', 'bid'])
+
+        if self.load_symbol(symbol) is False:
+            return Data(0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0)
+
+        element_ids = [
+            'trading-order-open',
+            'trading-order-high',
+            'trading-order-low',
+            'trading-order-close',
+            'trading-order-vol',
+            'trading-order-p',
+            'trading-order-ask',
+            'trading-order-bid',
+        ]
+        lst = []
+        for id_ in element_ids:
+            val = self.driver.find_element(By.ID, id_).text
+            val = float(val.replace(',', ''))  # replace comma for volume, and when prices > 999
+            lst.append(val)
+
+        return Data._make(lst)
+
+    def calculate_order_quantity(self, symbol: str, buying_power: float, float_option: bool = False):
+        """
+        returns the amount of shares you can buy with the given buying_power as int(), but if float_option is True,
+        it will return the amount as a float.
+
+        :param symbol: str
+        :param buying_power: float,
+        :param float_option: bool, default: False, if True returns the original number as float
+        :return: int or float
+        """
+        if self.load_symbol(symbol) is False:
+            return
+        quantity = (buying_power / self.last)
+
+        if float_option is True:
+            return quantity
+        return int(quantity)
+
+    def locate_stock(self, symbol: str, share_amount: int, max_price: float = 0, debug_info: bool = False):
+        """
+        Locate a stock, requires: stock symbol, and share_amount. optional: max_price.
+        if the locate_price is less than max_price: it will accept, else: decline.
+
+        :param symbol: str, symbol to locate.
+        :param share_amount: int, must be a multiple of 100 (100, 200, 300...)
+        :param max_price: float, default: 0, total price you are willing to pay for locates
+        :param debug_info: bool, if True it will print info about the locates in the console
+        :return: named tuple with the following attributes: 'price_per_share' and 'total'
+        :raises Exception: if share_amount is not divisible by 100
+        """
+        Data = namedtuple('Data', ['price_per_share', 'total'])
+
+        if share_amount is not None and share_amount % 100 != 0:
+            raise Exception(f'ERROR: share_amount is not divisible by 100 ({share_amount=})')
+
+        if not self.load_symbol(symbol):
+            return
+
+        if self.last <= 1.00:
+            print(f'Error: Cannot locate stocks priced under $1.00 ({symbol=}, price={self.last})')
+
+        self.driver.find_element(By.ID, "locate-tab-1").click()
+        input_symbol = self.driver.find_element(By.ID, "short-list-input-symbol")
+        input_symbol.clear()
+        input_symbol.send_keys(symbol, Keys.RETURN)
+
+        input_shares = self.driver.find_element(By.ID, "short-list-input-shares")
+        input_shares.clear()
+        input_shares.send_keys(share_amount)
+
+        while self.driver.find_element(By.ID, "short-list-locate-status").text == '':
+            time.sleep(0.1)
+
+        if self.driver.find_element(By.ID, "short-list-locate-status").text == 'Easy to borrow':
+            locate_pps = 0.00
+            locate_total = 0.00
+            if debug_info:
+                print(colored(f'Stock ({symbol}) is "Easy to borrow"', 'green'))
+            return Data(locate_pps, locate_total)
+
+        self.driver.find_element(By.ID, "short-list-button-locate").click()
+
+        for i in range(300):
+            try:
+                locate_pps = float(self.driver.find_element(By.ID, f"oitem-l-{symbol.upper()}-cell-2").text)
+                locate_total = float(self.driver.find_element(By.ID, f"oitem-l-{symbol.upper()}-cell-6").text)
+                break
+
+            except (ValueError, NoSuchElementException, StaleElementReferenceException):
+                time.sleep(0.15)
+                if i == 15 or i == 299:
+                    insufficient_bp = 'Insufficient BP to short a position with requested quantity.'
+                    last_notif = self.Notification.get_last_notification_message()
+                    if insufficient_bp in last_notif:
+                        warnings.warn(f"ERROR! {insufficient_bp}")
+                        return
+        else:
+            raise Exception(f'Error: not able to locate symbol element ({symbol=})')
+
+        if locate_total <= max_price:
+            self.driver.find_element(By.XPATH, f'//*[@id="oitem-l-{symbol.upper()}-cell-8"]/span[1]').click()
+            if debug_info:
+                print(colored(f'HTB Locate accepted ({symbol}, $ {locate_total})', 'cyan'))
+        else:
+            self.driver.find_element(By.XPATH, f'//*[@id="oitem-l-{symbol.upper()}-cell-8"]/span[2]').click()
+
+        return Data(locate_pps, locate_total)
+        # TODO create a function to get the pps and another one that just locates the shares
+
+    def credit_locates(self, symbol: str, quantity=None):
+        """
+        sell/ credit stock locates, if no value is given in 'quantity', it will credit all the shares
+        available of the given symbol.
+
+        :param symbol: str
+        :param quantity: amount of shares to sell, must be a multiple of 100, ie: 100, 200, 300
+        :return:
+        :raises Exception: if given symbol in not already located
+        :raises ValueError: if quantity is not divisible by 100 or quantity > located shares
+        """
+        located_symbols = self.driver.find_elements(By.XPATH, '//*[@id="locate-inventory-table"]/tbody/tr/td[1]')
+        located_symbols = [x.text for x in located_symbols]
+
+        if symbol.upper() not in located_symbols:
+            raise Exception(f"ERROR! cannot find {symbol} in located symbols")
+
+        if quantity is not None:
+            if quantity % 100 != 0:
+                raise ValueError(f"ERROR! quantity is not divisible by 100 ({quantity=})")
+
+            located_shares = float(self.driver.find_element(By.ID, f"inv-{symbol.upper()}-cell-1").text)
+            if quantity > located_shares:
+                raise ValueError(f"ERROR! you cannot credit more shares than u already have "
+                                 f"({quantity} vs {located_shares}")
+
+            input_quantity = self.driver.find_element(By.ID, f"inv-{symbol.upper()}-sell-qty")
+            input_quantity.clear()
+            input_quantity.send_keys(quantity)
+
+        self.driver.find_element(By.XPATH, f'//*[@id="inv-{symbol.upper()}-sell"]/button').click()
+        return
+
+    @time_it
+    def limit_order(self, order_direction: Order, symbol: str, share_amount: int, limit_price: float,
+                    time_in_force: TIF = TIF.DAY, log_info: bool = False):
+        """
+        Place a Limit Order, the following params are required: order_direction, symbol, share_amount, and limit_price.
+
+        :param order_direction: str: 'buy', 'sell', 'short', 'cover'
+        :param symbol: str: e.g: 'aapl', 'amd', 'NVDA', 'GM'
+        :param limit_price: float
+        :param share_amount: int
+        :param time_in_force: str, default: 'DAY', must be one of the following: 'DAY', 'GTC', or 'GTX'
+        :param log_info: bool, if True it will print information about the order
+        :return: True if operation succeeded
+        :raises AttributeError: if time_in_force argument not one of the following: 'DAY', 'GTC', 'GTX'
+        """
+        symbol = symbol.lower()
+        order_direction = order_direction.value
+        time_in_force = time_in_force.value
+
+        if time_in_force not in ['DAY', 'GTC', 'GTX']:
+            raise AttributeError(f"Error: time_in_force argument must be one of the following: 'DAY', 'GTC', 'GTX'")
+
+        self.load_symbol(symbol)
+
+        order_menu = Select(self.driver.find_element(By.ID, "trading-order-select-type"))
+        order_menu.select_by_index(1)
+
+        tif_menu = Select(self.driver.find_element(By.ID, "trading-order-select-time"))
+        tif_menu.select_by_visible_text(time_in_force)
+
+        input_quantity = self.driver.find_element(By.ID, "trading-order-input-quantity")
+        input_quantity.clear()
+        input_quantity.send_keys(share_amount)
+
+        price_input = self.driver.find_element(By.ID, "trading-order-input-price")
+        price_input.clear()
+        price_input.send_keys(limit_price)
+
+        self.driver.find_element(By.ID, f"trading-order-button-{order_direction}").click()
+
+        if log_info is True:
+            print(f"Time: {self.time}, Order direction: {order_direction}, Symbol: {symbol}, "
+                  f"Limit Price: {limit_price}, Shares amount: {share_amount}")
+
+    @time_it
+    def market_order(self, order_direction: Order, symbol: str, share_amount: int,
+                     time_in_force: TIF = TIF.DAY, log_info: bool = False):
+        """
+        Place a Market Order, The following params are required: order_direction, symbol, and share_amount
+
+        :param order_direction: str: 'buy', 'sell', 'short', 'cover'
+        :param symbol: str: e.g: 'aapl', 'amd', 'NVDA', 'GM'
+        :param share_amount: int
+        :param time_in_force: str, default: 'DAY', must be one of the following: 'DAY', 'GTC', or 'GTX'
+        :param log_info: bool, if True it will print information about the order
+        :return:
+        :raises Exception: if time not during market hours (9:30 - 16:00)
+        :raises AttributeError: if time_in_force argument not one of the following: 'DAY', 'GTC', 'GTX'
+        """
+        symbol = symbol.lower()
+        order_direction = order_direction.value
+        time_in_force = time_in_force.value
+
+        if not self.time_between((9, 30), (16, 0)):
+            raise Exception(f'Error: Market orders are not allowed at this time ({self.time})')
+
+        if time_in_force not in ['DAY', 'GTC', 'GTX']:
+            raise AttributeError(f"Error: time_in_force argument must be one of the following: 'DAY', 'GTC', 'GTX'")
+
+        self.load_symbol(symbol)
+
+        order_menu = Select(self.driver.find_element(By.ID, "trading-order-select-type"))
+        order_menu.select_by_index(0)
+
+        tif_menu = Select(self.driver.find_element(By.ID, "trading-order-select-time"))
+        tif_menu.select_by_visible_text(time_in_force)
+
+        input_quantity = self.driver.find_element(By.ID, "trading-order-input-quantity")
+        input_quantity.clear()
+        input_quantity.send_keys(share_amount)
+
+        self.driver.find_element(By.ID, f"trading-order-button-{order_direction}").click()
+
+        if log_info is True:
+            print(f"Time: {self.time}, Order direction: {order_direction}, Symbol: {symbol}, "
+                  f"Price: {self.last}, Shares amount: {share_amount}")
+
+    @time_it
+    def stop_market_order(self, order_direction: Order, symbol: str, share_amount: int, stop_price: float,
+                          time_in_force: TIF = TIF.DAY, log_info: bool = False):
+        """
+        Place a Stop Market Order, the following params are required: order_direction, symbol,
+        share_amount, and stop_price.
+        note that a Stop Market Order can only be placed during market-hours (09:30:00 - 16:00:00), therefore if a
+        Stop Market Order is placed outside market hours it will raise an error.
+
+        :param order_direction: str: 'buy', 'sell', 'short', 'cover'
+        :param symbol: str: e.g: 'aapl', 'amd', 'NVDA', 'GM'
+        :param stop_price: float
+        :param share_amount: int
+        :param time_in_force: str, default: 'DAY', must be one of the following: 'DAY', 'GTC', or 'GTX'
+        :param log_info: bool, if True it will print information about the order
+        :return: True if operation succeeded
+        :raises Exception: if time not during market hours (9:30 - 16:00)
+        :raises AttributeError: if time_in_force argument not one of the following: 'DAY', 'GTC', 'GTX'
+        """
+        symbol = symbol.lower()
+        order_direction = order_direction.value
+        time_in_force = time_in_force.value
+
+        if not self.time_between((9, 30), (16, 0)):
+            raise Exception(f'Error: Stop Market orders are not allowed at this time ({self.time})')
+
+        if time_in_force not in ['DAY', 'GTC', 'GTX']:
+            raise AttributeError(f"Error: time_in_force argument must be one of the following: 'DAY', 'GTC', 'GTX'")
+
+        self.load_symbol(symbol)
+
+        order_menu = Select(self.driver.find_element(By.ID, "trading-order-select-type"))
+        order_menu.select_by_index(2)
+
+        tif_menu = Select(self.driver.find_element(By.ID, "trading-order-select-time"))
+        tif_menu.select_by_visible_text(time_in_force)
+
+        input_quantity = self.driver.find_element(By.ID, "trading-order-input-quantity")
+        input_quantity.clear()
+        input_quantity.send_keys(share_amount)
+
+        price_input = self.driver.find_element(By.ID, "trading-order-input-sprice")
+        price_input.clear()
+        price_input.send_keys(stop_price)
+
+        self.driver.find_element(By.ID, f"trading-order-button-{order_direction}").click()
+
+        if log_info is True:
+            print(f"Time: {self.time}, Order direction: {order_direction}, Symbol: {symbol}, "
+                  f"Stop Price: {stop_price}, Shares amount: {share_amount}")
```

### Comparing `tradezero_api-0.3.0/tradezero_api/notification.py` & `tradezero_api-0.3.1/tradezero_api/notification.py`

 * *Ordering differences only*

 * *Files 11% similar despite different names*

```diff
@@ -1,72 +1,72 @@
-from __future__ import annotations
-
-from selenium.webdriver.common.by import By
-
-from .time_helpers import Time
-
-
-class Notification(Time):
-    """A class for retrieving notifications from the web-app"""
-
-    def __init__(self, driver):
-        self.driver = driver
-
-    def get_last_notification_message(self):
-        """
-        return last notification message
-
-        :return: str
-        """
-        return self.driver.find_element(By.CSS_SELECTOR, 'span.message').text
-
-    def get_notifications(self, notif_amount: int = 1):
-        """
-        return a nested list with each sublist containing [time, title, message],
-        note that u can only view the amount of notifications that are visible in the box/widget
-        without scrolling down (which usually is around 6-9 depending on each message length)
-        example of nested list: (see the docs for a better look):
-        [['11:34:49', 'Order canceled', 'Your Limit Buy order of 1 AMD was canceled.'],
-        ['11:23:34', 'Level 2', 'You are not authorized for symbol: AMD'],
-        ['11:23:34', 'Error', 'You are not authorized for symbol: AMD']].
-
-        :param notif_amount: int amount of notifications to retrieve sorted by most recent
-        :return: nested list
-        """
-        notif_lst = self.driver.find_elements(By.XPATH,
-                                              '//*[@id="notifications-list-1"]/li')
-        notif_lst_text = [x.text.split('\n') for x in notif_lst[0:notif_amount] if x.text != '']
-
-        notifications = []
-        for (notification, i) in zip(notif_lst_text, range(notif_amount)):
-            if len(notification) == 2:
-                notification.insert(0, str(self.time))
-
-            elif notification[0] == '' or notification[0] == '-':
-                notification[0] = str(self.time)
-
-            notifications.append(notification)
-        return notifications
-    
-    def notifications_generator(self):
-        """
-        A notification generator, similarly to get_notifications(), this yields one notification at a time,
-        on each next() it will yield a list like so: 
-        ['11:34:49', 'Order canceled', 'Your Limit Buy order of 1 AMD was canceled.']
-        You can think of it as a more dynamic version of get_notifications(), on each next(); it gets 
-        one notification message.
-
-        :return: list
-        """
-        notif_lst = self.driver.find_elements(By.XPATH, '//*[@id="notifications-list-1"]/li')
-        for item in notif_lst:
-            if item.text == '':
-                continue
-                
-            notification = item.text.split('\n')
-            if len(notification) == 2:
-                notification.insert(0, str(self.time))
-
-            elif notification[0] == '' or notification[0] == '-':
-                notification[0] = str(self.time)
-
-            yield notification
+from __future__ import annotations
+
+from selenium.webdriver.common.by import By
+
+from .time_helpers import Time
+
+
+class Notification(Time):
+    """A class for retrieving notifications from the web-app"""
+
+    def __init__(self, driver):
+        self.driver = driver
+
+    def get_last_notification_message(self):
+        """
+        return last notification message
+
+        :return: str
+        """
+        return self.driver.find_element(By.CSS_SELECTOR, 'span.message').text
+
+    def get_notifications(self, notif_amount: int = 1):
+        """
+        return a nested list with each sublist containing [time, title, message],
+        note that u can only view the amount of notifications that are visible in the box/widget
+        without scrolling down (which usually is around 6-9 depending on each message length)
+        example of nested list: (see the docs for a better look):
+        [['11:34:49', 'Order canceled', 'Your Limit Buy order of 1 AMD was canceled.'],
+        ['11:23:34', 'Level 2', 'You are not authorized for symbol: AMD'],
+        ['11:23:34', 'Error', 'You are not authorized for symbol: AMD']].
+
+        :param notif_amount: int amount of notifications to retrieve sorted by most recent
+        :return: nested list
+        """
+        notif_lst = self.driver.find_elements(By.XPATH,
+                                              '//*[@id="notifications-list-1"]/li')
+        notif_lst_text = [x.text.split('\n') for x in notif_lst[0:notif_amount] if x.text != '']
+
+        notifications = []
+        for (notification, i) in zip(notif_lst_text, range(notif_amount)):
+            if len(notification) == 2:
+                notification.insert(0, str(self.time))
+
+            elif notification[0] == '' or notification[0] == '-':
+                notification[0] = str(self.time)
+
+            notifications.append(notification)
+        return notifications
+    
+    def notifications_generator(self):
+        """
+        A notification generator, similarly to get_notifications(), this yields one notification at a time,
+        on each next() it will yield a list like so: 
+        ['11:34:49', 'Order canceled', 'Your Limit Buy order of 1 AMD was canceled.']
+        You can think of it as a more dynamic version of get_notifications(), on each next(); it gets 
+        one notification message.
+
+        :return: list
+        """
+        notif_lst = self.driver.find_elements(By.XPATH, '//*[@id="notifications-list-1"]/li')
+        for item in notif_lst:
+            if item.text == '':
+                continue
+                
+            notification = item.text.split('\n')
+            if len(notification) == 2:
+                notification.insert(0, str(self.time))
+
+            elif notification[0] == '' or notification[0] == '-':
+                notification[0] = str(self.time)
+
+            yield notification
```

### Comparing `tradezero_api-0.3.0/tradezero_api/portfolio.py` & `tradezero_api-0.3.1/tradezero_api/portfolio.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,129 +1,143 @@
-from __future__ import annotations
-
-import warnings
-
-import pandas as pd
-from selenium.webdriver.common.by import By
-from selenium.webdriver.remote.webdriver import WebDriver
-
-from .enums import PortfolioTab, OrderType
-
-
-class Portfolio:
-    def __init__(self, driver: WebDriver):
-        self.driver = driver
-
-    def portfolio(self, return_type: str = 'df'):
-        """
-        return the Portfolio table as a pandas.DataFrame or nested dict, with the symbol column as index.
-        the column names are the following: 'type', 'qty', 'p_close', 'entry',
-        'price', 'change', '%change', 'day_pnl', 'pnl', 'overnight'
-        note that if the portfolio is empty Pandas won't be able to locate the table,
-        and therefore will return None
-
-        :param return_type: 'df' or 'dict'
-        :return: pandas.DataFrame or None if table empty
-        """
-        portfolio_symbols = self.driver.find_elements(By.XPATH, '//*[@id="opTable-1"]/tbody/tr/td[1]')
-        if len(portfolio_symbols) == 0:
-            warnings.warn('Portfolio is empty')
-            return None
-
-        df = pd.read_html(self.driver.page_source, attrs={'id': 'opTable-1'})[0]
-        df.columns = [
-            'symbol', 'type', 'qty', 'p_close', 'entry', 'price', 'change', '%change', 'day_pnl', 'pnl', 'overnight'
-        ]
-        df = df.set_index('symbol')
-        if return_type == 'dict':
-            return df.to_dict('index')
-        return df
-
-    def open_orders(self):
-        """
-        return DF with only positions that were opened today (intraday positions)
-
-        :return: pandas.DataFrame
-        """
-        df = self.portfolio()
-        filt = df['overnight'] == 'Yes'
-        return df.loc[~filt]
-
-    def invested(self, symbol):
-        """
-        returns True if the given symbol is in portfolio, else: false
-
-        :param symbol: str: e.g: 'aapl', 'amd', 'NVDA', 'GM'
-        :return: bool
-        """
-        data = self.portfolio('dict')
-        symbols_list = list(data.keys())
-
-        if symbol.upper() in symbols_list:
-            return True
-        return False
-
-    def _switch_portfolio_tab(self, tab: PortfolioTab) -> None:
-        """
-        Switch the focus to a given tab
-
-        Note that this is idem-potent, meaning you can switch twice consecutively in the same tab.
-
-        :param tab: enum of PortfolioTab
-        :return: None
-        """
-        portfolio_tab = self.driver.find_element(By.ID, tab)
-        portfolio_tab.click()
-
-    def get_active_orders(self, return_type: str = 'df'):
-        """
-        Get a dataframe with all the active orders and their info
-
-        :param return_type: 'df' or 'dict'
-        :return: dataframe or dictionary (based on the return_type parameter)
-        """
-        active_orders = self.driver.find_elements(By.XPATH, '//*[@id="aoTable-1"]/tbody/tr[@order-id]')
-        if len(active_orders) == 0:
-            warnings.warn('There are no active orders')
-            return None
-
-        df = pd.read_html(self.driver.page_source, attrs={'id': 'aoTable-1'})[0]
-        df = df.drop(0, axis=1)  # remove the first column which contains the button "CANCEL"
-        df.columns = ['ref_number', 'symbol', 'side', 'qty', 'type', 'status', 'tif', 'limit', 'stop', 'placed']
-        # df = df.set_index('symbol')  # cant set it as a column since its not always unique
-
-        if return_type == 'dict':
-            return df.to_dict('index')
-        return df
-
-    def symbol_present_in_active_orders(self, symbol: str) -> bool:
-        """
-        Check if a given symbol is present in the active orders tab
-
-        :param symbol:
-        :return: True or False
-        """
-        return symbol.upper() in self.get_active_orders()['symbol'].values
-
-    def cancel_active_order(self, symbol: str, order_type: OrderType) -> None:
-        """
-        Cancel a pending order
-
-        :param symbol:
-        :param order_type: enum of OrderType
-        :return: None
-        """
-        symbol = symbol.upper()
-        self._switch_portfolio_tab(tab=PortfolioTab.active_orders)
-
-        df = self.get_active_orders()
-        assert symbol in df['symbol'].values, f'Given symbol {symbol} is not present in the active orders tab'
-
-        # find the ref-id of all the orders we have to cancel:
-        filt = (df['symbol'] == symbol) & (df['type'] == order_type)
-        ids_to_cancel = df[filt]['ref_number'].values
-        ids_to_cancel = [x.replace('S.', '') for x in ids_to_cancel]
-
-        for order_id in ids_to_cancel:
-            cancel_button = self.driver.find_element(
-                By.XPATH, f'//div[@id="portfolio-content-tab-ao-1"]//*[@order-id="{order_id}"]/td[@class="red"]')
-            cancel_button.click()
+from __future__ import annotations
+
+import warnings
+from typing import overload, Optional, Literal
+
+import pandas as pd
+from selenium.webdriver.common.by import By
+from selenium.webdriver.remote.webdriver import WebDriver
+
+from .enums import PortfolioTab, OrderType
+
+
+class Portfolio:
+    def __init__(self, driver: WebDriver):
+        self.driver = driver
+
+    @overload
+    def portfolio(self, return_type: Literal['df'] = 'df') -> Optional[pd.DataFrame]:
+        ...
+
+    @overload
+    def portfolio(self, return_type: Literal['dict']) -> Optional[dict]:
+        ...
+
+    def portfolio(self, return_type: Literal['df', 'dict'] = 'df') -> pd.DataFrame | dict | None:
+        """
+        return the Portfolio table as a pandas.DataFrame or nested dict, with the symbol column as index.
+        the column names are the following: 'type', 'qty', 'p_close', 'entry',
+        'price', 'change', '%change', 'day_pnl', 'pnl', 'overnight'
+        note that if the portfolio is empty Pandas won't be able to locate the table,
+        and therefore will return None
+
+        :param return_type: 'df' or 'dict'
+        :return: pandas.DataFrame or None if table empty
+        """
+        portfolio_symbols = self.driver.find_elements(By.XPATH, '//*[@id="opTable-1"]/tbody/tr/td[1]')
+        df = pd.read_html(self.driver.page_source, attrs={'id': 'opTable-1'})[0]
+
+        if len(portfolio_symbols) == 0 or df.loc[0, 0].lower() == "you have no open positions.":
+            warnings.warn('Portfolio is empty')
+            return None
+
+        df.columns = [
+            'symbol', 'type', 'qty', 'p_close', 'entry', 'price', 'change', '%change', 'day_pnl', 'pnl', 'overnight'
+        ]
+        df = df.set_index('symbol')
+        if return_type == 'dict':
+            return df.to_dict('index')
+        return df
+
+    def open_orders(self) -> pd.DataFrame:
+        """
+        return DF with only positions that were opened today (intraday positions)
+
+        :return: pandas.DataFrame
+        """
+        df = self.portfolio()
+
+        # if there are no open position: return an empty dataframe
+        if df is None:
+            return pd.DataFrame()
+
+        filt = df['overnight'] == 'Yes'
+        return df.loc[~filt]
+
+    def invested(self, symbol) -> bool:
+        """
+        returns True if the given symbol is in portfolio, else: false
+
+        :param symbol: str: e.g: 'aapl', 'amd', 'NVDA', 'GM'
+        :return: bool
+        """
+        data = self.portfolio('dict')
+        if data is None:
+            return False
+
+        return symbol.upper() in data.keys()
+
+    def _switch_portfolio_tab(self, tab: PortfolioTab) -> None:
+        """
+        Switch the focus to a given tab
+
+        Note that this is idem-potent, meaning you can switch twice consecutively in the same tab.
+
+        :param tab: enum of PortfolioTab
+        :return: None
+        """
+        portfolio_tab = self.driver.find_element(By.ID, tab)
+        portfolio_tab.click()
+
+    def get_active_orders(self, return_type: str = 'df'):
+        """
+        Get a dataframe with all the active orders and their info
+
+        :param return_type: 'df' or 'dict'
+        :return: dataframe or dictionary (based on the return_type parameter)
+        """
+        active_orders = self.driver.find_elements(By.XPATH, '//*[@id="aoTable-1"]/tbody/tr[@order-id]')
+        if len(active_orders) == 0:
+            warnings.warn('There are no active orders')
+            return
+
+        df = pd.read_html(self.driver.page_source, attrs={'id': 'aoTable-1'})[0]
+        df = df.drop(0, axis=1)  # remove the first column which contains the button "CANCEL"
+        df.columns = ['ref_number', 'symbol', 'side', 'qty', 'type', 'status', 'tif', 'limit', 'stop', 'placed']
+        # df = df.set_index('symbol')  # cant set it as a column since its not always unique
+
+        if return_type == 'dict':
+            return df.to_dict('index')
+        return df
+
+    def symbol_present_in_active_orders(self, symbol: str) -> bool:
+        """
+        Check if a given symbol is present in the active orders tab
+
+        :param symbol:
+        :return: True or False
+        """
+        return symbol.upper() in self.get_active_orders()['symbol'].values
+
+    def cancel_active_order(self, symbol: str, order_type: OrderType) -> None:
+        """
+        Cancel a pending order
+
+        :param symbol:
+        :param order_type: enum of OrderType
+        :return: None
+        """
+        symbol = symbol.upper()
+        self._switch_portfolio_tab(tab=PortfolioTab.active_orders)
+
+        df = self.get_active_orders()
+        assert symbol in df['symbol'].values, f'Given symbol {symbol} is not present in the active orders tab'
+
+        # find the ref-id of all the orders we have to cancel:
+        filt = (df['symbol'] == symbol) & (df['type'] == order_type)
+        ids_to_cancel = df[filt]['ref_number'].values
+        ids_to_cancel = [x.replace('S.', '') for x in ids_to_cancel]
+
+        for order_id in ids_to_cancel:
+            cancel_button = self.driver.find_element(
+                By.XPATH, f'//div[@id="portfolio-content-tab-ao-1"]//*[@order-id="{order_id}"]/td[@class="red"]')
+            cancel_button.click()
```

### Comparing `tradezero_api-0.3.0/tradezero_api/time_helpers.py` & `tradezero_api-0.3.1/tradezero_api/time_helpers.py`

 * *Ordering differences only*

 * *Files 22% similar despite different names*

```diff
@@ -1,54 +1,54 @@
-from __future__ import annotations
-
-import time
-import datetime as dt
-
-import pytz
-
-
-class Time:
-    @property
-    def time(self):
-        """ return current EST time as a datetime object """
-        tz_ny = pytz.timezone('US/Eastern')
-        time1 = dt.datetime.now(tz=tz_ny).time()
-        return time1
-
-    def time_between(self, time1: tuple, time2: tuple):
-        """
-        return True if current time between: time1, and time2, else: return False
-
-        :param time1: tuple, ex: (10, 30), or with sec and micro-sec: (10, 30, 0, 250000)
-        :param time2: tuple, ex: (12, 45)
-        :return: bool
-        """
-        if dt.time(*time1) < self.time < dt.time(*time2):
-            return True
-        return False
-
-
-class Timer:
-    """
-    A class that behaves like a stopwatch, when initialized the counter starts,
-    and at any given moment you can check the total time elapsed
-    with the time_elapsed property
-    """
-    def __init__(self):
-        self.timer_start = time.perf_counter()
-
-    @property
-    def time_elapsed(self):
-        return time.perf_counter() - self.timer_start
-
-
-def time_it(func):
-    """Decorator for debugging the time taken to run a function"""
-    def wrapper(*args, **kwargs):
-        timer = Timer()
-        rv = func(*args, **kwargs)
-
-        if kwargs.get('log_time_elapsed') or kwargs.get('log_info'):
-            print(f'Time elapsed: {timer.time_elapsed:.2f} seconds')
-
-        return rv
-    return wrapper
+from __future__ import annotations
+
+import time
+import datetime as dt
+
+import pytz
+
+
+class Time:
+    @property
+    def time(self):
+        """ return current EST time as a datetime object """
+        tz_ny = pytz.timezone('US/Eastern')
+        time1 = dt.datetime.now(tz=tz_ny).time()
+        return time1
+
+    def time_between(self, time1: tuple, time2: tuple):
+        """
+        return True if current time between: time1, and time2, else: return False
+
+        :param time1: tuple, ex: (10, 30), or with sec and micro-sec: (10, 30, 0, 250000)
+        :param time2: tuple, ex: (12, 45)
+        :return: bool
+        """
+        if dt.time(*time1) < self.time < dt.time(*time2):
+            return True
+        return False
+
+
+class Timer:
+    """
+    A class that behaves like a stopwatch, when initialized the counter starts,
+    and at any given moment you can check the total time elapsed
+    with the time_elapsed property
+    """
+    def __init__(self):
+        self.timer_start = time.perf_counter()
+
+    @property
+    def time_elapsed(self):
+        return time.perf_counter() - self.timer_start
+
+
+def time_it(func):
+    """Decorator for debugging the time taken to run a function"""
+    def wrapper(*args, **kwargs):
+        timer = Timer()
+        rv = func(*args, **kwargs)
+
+        if kwargs.get('log_time_elapsed') or kwargs.get('log_info'):
+            print(f'Time elapsed: {timer.time_elapsed:.2f} seconds')
+
+        return rv
+    return wrapper
```

### Comparing `tradezero_api-0.3.0/PKG-INFO` & `tradezero_api-0.3.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 Metadata-Version: 2.1
 Name: tradezero-api
-Version: 0.3.0
+Version: 0.3.1
 Summary: A package for executing orders and retrieving data through the TradeZero web platform
 Home-page: https://github.com/shner-elmo/db-wrapper
 License: MIT
 Author: shner-elmo
 Author-email: 770elmo@gmail.com
-Requires-Python: >=3.10,<4.0
+Requires-Python: >=3.9
 Classifier: Environment :: Console
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
 Requires-Dist: lxml (>=4.9.2,<5.0.0)
 Requires-Dist: pandas (>=1.5.3,<2.0.0)
 Requires-Dist: pytz (>=2022.7.1,<2023.0.0)
 Requires-Dist: selenium (>=4.8.2,<5.0.0)
 Requires-Dist: termcolor (>=2.2.0,<3.0.0)
 Requires-Dist: webdriver-manager (>=3.8.5,<4.0.0)
```

