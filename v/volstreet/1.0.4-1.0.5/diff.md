# Comparing `tmp/volstreet-1.0.4.tar.gz` & `tmp/volstreet-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "volstreet-1.0.4.tar", last modified: Mon Jul 17 11:47:39 2023, max compression
+gzip compressed data, was "volstreet-1.0.5.tar", last modified: Sun Jul 23 12:50:36 2023, max compression
```

## Comparing `volstreet-1.0.4.tar` & `volstreet-1.0.5.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxrwxrwx   0        0        0        0 2023-07-17 11:47:39.162629 volstreet-1.0.4/
--rw-rw-rw-   0        0        0      497 2023-07-17 11:47:39.164013 volstreet-1.0.4/PKG-INFO
--rw-rw-rw-   0        0        0      124 2023-06-07 14:47:58.000000 volstreet-1.0.4/README.md
--rw-rw-rw-   0        0        0       91 2023-05-24 02:09:11.000000 volstreet-1.0.4/pyproject.toml
--rw-rw-rw-   0        0        0     1391 2023-07-17 11:47:39.164013 volstreet-1.0.4/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-17 11:47:39.157669 volstreet-1.0.4/volstreet/
--rw-rw-rw-   0        0        0    16121 2023-05-24 02:09:11.000000 volstreet-1.0.4/volstreet/SmartWebSocketV2.py
--rw-rw-rw-   0        0        0       37 2023-06-07 15:08:38.000000 volstreet-1.0.4/volstreet/__init__.py
--rw-rw-rw-   0        0        0     9094 2023-07-16 12:56:47.000000 volstreet-1.0.4/volstreet/blackscholes.py
--rw-rw-rw-   0        0        0     2685 2023-06-26 20:11:40.000000 volstreet-1.0.4/volstreet/constants.py
--rw-rw-rw-   0        0        0    42479 2023-07-16 12:56:47.000000 volstreet-1.0.4/volstreet/datamodule.py
--rw-rw-rw-   0        0        0   192075 2023-07-17 11:46:59.000000 volstreet-1.0.4/volstreet/dealingroom.py
--rw-rw-rw-   0        0        0     1683 2023-05-24 02:09:11.000000 volstreet-1.0.4/volstreet/discord_bot.py
--rw-rw-rw-   0        0        0      211 2023-07-16 12:56:47.000000 volstreet-1.0.4/volstreet/exceptions.py
--rw-rw-rw-   0        0        0    39664 2023-05-24 02:09:11.000000 volstreet-1.0.4/volstreet/nsefunctions.py
--rw-rw-rw-   0        0        0    13257 2023-07-17 06:22:53.000000 volstreet-1.0.4/volstreet/strategies.py
-drwxrwxrwx   0        0        0        0 2023-07-17 11:47:39.162629 volstreet-1.0.4/volstreet.egg-info/
--rw-rw-rw-   0        0        0      497 2023-07-17 11:47:39.000000 volstreet-1.0.4/volstreet.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      447 2023-07-17 11:47:39.000000 volstreet-1.0.4/volstreet.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-17 11:47:39.000000 volstreet-1.0.4/volstreet.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      801 2023-07-17 11:47:39.000000 volstreet-1.0.4/volstreet.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-07-17 11:47:39.000000 volstreet-1.0.4/volstreet.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 12:50:36.402143 volstreet-1.0.5/
+-rw-rw-rw-   0        0        0      497 2023-07-23 12:50:36.402143 volstreet-1.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0      124 2023-06-07 14:47:58.000000 volstreet-1.0.5/README.md
+-rw-rw-rw-   0        0        0       91 2023-05-24 02:09:11.000000 volstreet-1.0.5/pyproject.toml
+-rw-rw-rw-   0        0        0     1391 2023-07-23 12:50:36.403140 volstreet-1.0.5/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 12:50:36.395166 volstreet-1.0.5/volstreet/
+-rw-rw-rw-   0        0        0    16121 2023-05-24 02:09:11.000000 volstreet-1.0.5/volstreet/SmartWebSocketV2.py
+-rw-rw-rw-   0        0        0       37 2023-06-07 15:08:38.000000 volstreet-1.0.5/volstreet/__init__.py
+-rw-rw-rw-   0        0        0     9094 2023-07-16 12:56:47.000000 volstreet-1.0.5/volstreet/blackscholes.py
+-rw-rw-rw-   0        0        0     2685 2023-06-26 20:11:40.000000 volstreet-1.0.5/volstreet/constants.py
+-rw-rw-rw-   0        0        0    42857 2023-07-23 12:48:19.000000 volstreet-1.0.5/volstreet/datamodule.py
+-rw-rw-rw-   0        0        0   192083 2023-07-21 17:03:46.000000 volstreet-1.0.5/volstreet/dealingroom.py
+-rw-rw-rw-   0        0        0     1683 2023-05-24 02:09:11.000000 volstreet-1.0.5/volstreet/discord_bot.py
+-rw-rw-rw-   0        0        0      211 2023-07-16 12:56:47.000000 volstreet-1.0.5/volstreet/exceptions.py
+-rw-rw-rw-   0        0        0    39664 2023-05-24 02:09:11.000000 volstreet-1.0.5/volstreet/nsefunctions.py
+-rw-rw-rw-   0        0        0    13257 2023-07-17 06:22:53.000000 volstreet-1.0.5/volstreet/strategies.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:50:36.401147 volstreet-1.0.5/volstreet.egg-info/
+-rw-rw-rw-   0        0        0      497 2023-07-23 12:50:36.000000 volstreet-1.0.5/volstreet.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      447 2023-07-23 12:50:36.000000 volstreet-1.0.5/volstreet.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:50:36.000000 volstreet-1.0.5/volstreet.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      801 2023-07-23 12:50:36.000000 volstreet-1.0.5/volstreet.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-07-23 12:50:36.000000 volstreet-1.0.5/volstreet.egg-info/top_level.txt
```

### Comparing `volstreet-1.0.4/setup.cfg` & `volstreet-1.0.5/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2076 6f6c 7374 7265 6574 0d0a 7665   = volstreet..ve
-00000020: 7273 696f 6e20 3d20 312e 302e 340d 0a61  rsion = 1.0.4..a
+00000020: 7273 696f 6e20 3d20 312e 302e 350d 0a61  rsion = 1.0.5..a
 00000030: 7574 686f 7220 3d20 5261 6875 6c20 5468  uthor = Rahul Th
 00000040: 616b 6b61 720d 0a61 7574 686f 725f 656d  akkar..author_em
 00000050: 6169 6c20 3d20 722e 7468 616b 6b61 7231  ail = r.thakkar1
 00000060: 3540 676d 6169 6c2e 636f 6d0d 0a64 6573  5@gmail.com..des
 00000070: 6372 6970 7469 6f6e 203d 2056 6f6c 5374  cription = VolSt
 00000080: 7265 6574 2069 7320 6120 5079 7468 6f6e  reet is a Python
 00000090: 206c 6962 7261 7279 2066 6f72 2061 7574   library for aut
```

### Comparing `volstreet-1.0.4/volstreet/SmartWebSocketV2.py` & `volstreet-1.0.5/volstreet/SmartWebSocketV2.py`

 * *Files identical despite different names*

### Comparing `volstreet-1.0.4/volstreet/blackscholes.py` & `volstreet-1.0.5/volstreet/blackscholes.py`

 * *Files identical despite different names*

### Comparing `volstreet-1.0.4/volstreet/constants.py` & `volstreet-1.0.5/volstreet/constants.py`

 * *Files identical despite different names*

### Comparing `volstreet-1.0.4/volstreet/datamodule.py` & `volstreet-1.0.5/volstreet/datamodule.py`

 * *Files 1% similar despite different names*

```diff
@@ -714,14 +714,17 @@
 
     if return_all:
         return index_monthly_data
     else:
         summary_df = index_monthly_data[
             ["index_abs_change", "sum_constituent_movement", "ratio_of_movements"]
         ]
+        summary_df['index_rolling'] = summary_df['index_abs_change'].rolling(12, min_periods=1).mean()
+        summary_df['cons_rolling'] = summary_df['sum_constituent_movement'].rolling(12, min_periods=1).mean()
+        summary_df['rolling_ratio'] = summary_df['cons_rolling'] / summary_df['index_rolling']
         return summary_df
 
 
 def get_greenlit_kite(
     kite_api_key,
     kite_api_secret,
     kite_user_id,
@@ -855,14 +858,15 @@
     for ticker in tickers:
         print(f"Fetching data for {ticker}")
         get_1m_data(kite_object, ticker, path=path)
 
 
 def backtest_intraday_trend(
     one_min_df,
+    open_nth=0,
     beta=1,
     trend_threshold=1,
     max_entries=3,
     eod_client=None,
     rolling_days=60,
 ):
     one_min_df = one_min_df.copy()
@@ -893,24 +897,24 @@
     vix["close"] = vix["close"] * beta
 
     one_min_df.drop(
         one_min_df[one_min_df["date"].dt.date.isin(unavailable_dates)].index,
         inplace=True,
     )
     open_prices = (
-        one_min_df.groupby(one_min_df["date"].dt.date).close.first().to_frame()
+        one_min_df.groupby(one_min_df["date"].dt.date).apply(lambda x: x.iloc[open_nth]).open.to_frame()
     )
     open_data = open_prices.merge(
-        vix["open"].to_frame(), left_index=True, right_index=True
+        vix["open"].to_frame(), left_index=True, right_index=True, suffixes=("", "_vix")
     )
-    open_data["threshold_movement"] = (open_data["open"] / 48) * trend_threshold
-    open_data["upper_bound"] = open_data["close"] * (
+    open_data["threshold_movement"] = (open_data["open_vix"] / 48) * trend_threshold
+    open_data["upper_bound"] = open_data["open"] * (
         1 + open_data["threshold_movement"] / 100
     )
-    open_data["lower_bound"] = open_data["close"] * (
+    open_data["lower_bound"] = open_data["open"] * (
         1 - open_data["threshold_movement"] / 100
     )
     open_data["day_close"] = one_min_df.groupby(one_min_df["date"].dt.date).close.last()
     open_data.columns = [
         "day_open",
         "open_vix",
         "threshold_movement",
```

### Comparing `volstreet-1.0.4/volstreet/dealingroom.py` & `volstreet-1.0.5/volstreet/dealingroom.py`

 * *Files 0% similar despite different names*

```diff
@@ -2947,16 +2947,16 @@
                     stop_loss_order_ids,
                     context=side,
                     notify_url=self.webhook_url,
                 )
                 if orders_triggered:
                     justify_stop_loss(info_dict, side)
                     info_dict[f"{side}_sl"] = True
-                if not orders_complete:
-                    info_dict[f"{side}_stop_loss_order_ids"] = None
+                    if not orders_complete:
+                        info_dict[f"{side}_stop_loss_order_ids"] = None
 
         def process_stop_loss(info_dict, sl_type):
             if (
                 info_dict["call_sl"] and info_dict["put_sl"]
             ):  # Check to avoid double processing
                 return
 
@@ -3366,15 +3366,15 @@
     def intraday_trend(
         self,
         quantity_in_lots,
         start_time=(9, 15, 58),
         exit_time=(15, 27),
         sleep_time=5,
         threshold_movement=None,
-        minutes_to_avg=45,
+        seconds_to_avg=45,
         beta=0.8,
         max_entries=3,
     ):
         while currenttime().time() < time(*start_time):
             print(f"{self.name} trender sleeping till {start_time}")
             sleep(1)
 
@@ -3388,15 +3388,15 @@
             datetime.combine(currenttime().date(), exit_time) - timedelta(minutes=10)
         ).time()
         price_boundaries = [
             open_price * (1 + ((-1) ** i) * threshold_movement / 100) for i in range(2)
         ]
 
         # Price deque
-        n_prices = max(int(minutes_to_avg / sleep_time), 1)
+        n_prices = max(int(seconds_to_avg / sleep_time), 1)
         price_deque = deque(maxlen=n_prices)
 
         notifier(
             f"{self.name} trender starting with {threshold_movement:0.2f} threshold movement\n"
             f"Current Price: {open_price}\nUpper limit: {price_boundaries[0]:0.2f}\n"
             f"Lower limit: {price_boundaries[1]:0.2f}.",
             self.webhook_url,
```

### Comparing `volstreet-1.0.4/volstreet/discord_bot.py` & `volstreet-1.0.5/volstreet/discord_bot.py`

 * *Files identical despite different names*

### Comparing `volstreet-1.0.4/volstreet/nsefunctions.py` & `volstreet-1.0.5/volstreet/nsefunctions.py`

 * *Files identical despite different names*

### Comparing `volstreet-1.0.4/volstreet/strategies.py` & `volstreet-1.0.5/volstreet/strategies.py`

 * *Files identical despite different names*

### Comparing `volstreet-1.0.4/volstreet.egg-info/requires.txt` & `volstreet-1.0.5/volstreet.egg-info/requires.txt`

 * *Files identical despite different names*

