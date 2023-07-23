# Comparing `tmp/canada_holiday-1.0.3.tar.gz` & `tmp/canada_holiday-1.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "canada_holiday-1.0.3.tar", max compression
+gzip compressed data, was "canada_holiday-1.1.3.tar", max compression
```

## Comparing `canada_holiday-1.0.3.tar` & `canada_holiday-1.1.3.tar`

### file list

```diff
@@ -1,25 +1,24 @@
--rw-r--r--   0        0        0     1067 2023-03-25 23:08:37.337469 canada_holiday-1.0.3/LICENSE
--rw-r--r--   0        0        0     1584 2023-04-07 23:30:13.551145 canada_holiday-1.0.3/README.md
--rw-r--r--   0        0        0      115 2023-03-25 23:51:39.116474 canada_holiday-1.0.3/canada_holiday/__init__.py
--rw-r--r--   0        0        0     5960 2023-04-08 00:08:50.178812 canada_holiday-1.0.3/canada_holiday/holiday_class.py
--rw-r--r--   0        0        0        0 2023-03-25 23:38:49.533730 canada_holiday-1.0.3/canada_holiday/holiday_info/__init__.py
--rw-r--r--   0        0        0      812 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/ab.py
--rw-r--r--   0        0        0      846 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/all.py
--rw-r--r--   0        0        0      862 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/bc.py
--rw-r--r--   0        0        0      670 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/mb.py
--rw-r--r--   0        0        0      453 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/national.py
--rw-r--r--   0        0        0      524 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/nb.py
--rw-r--r--   0        0        0      671 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/nl.py
--rw-r--r--   0        0        0      357 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/ns.py
--rw-r--r--   0        0        0      706 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/nt.py
--rw-r--r--   0        0        0      584 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/nu.py
--rw-r--r--   0        0        0      888 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/on.py
--rw-r--r--   0        0        0      384 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/pe.py
--rw-r--r--   0        0        0      658 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/qc.py
--rw-r--r--   0        0        0      686 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/sk.py
--rw-r--r--   0        0        0      876 2023-03-25 21:15:42.208475 canada_holiday-1.0.3/canada_holiday/holiday_info/yt.py
--rwxr-xr-x   0        0        0     2744 2023-04-08 00:08:50.178812 canada_holiday-1.0.3/canada_holiday/holidays.py
--rw-r--r--   0        0        0     4356 2023-04-08 00:08:50.178812 canada_holiday-1.0.3/canada_holiday/utils.py
--rw-r--r--   0        0        0      482 2023-04-08 00:18:58.919986 canada_holiday-1.0.3/pyproject.toml
--rw-r--r--   0        0        0     2257 1970-01-01 00:00:00.000000 canada_holiday-1.0.3/setup.py
--rw-r--r--   0        0        0     2182 1970-01-01 00:00:00.000000 canada_holiday-1.0.3/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-07-09 19:27:30.778904 canada_holiday-1.1.3/LICENSE
+-rw-r--r--   0        0        0     1584 2023-07-09 19:27:30.778996 canada_holiday-1.1.3/README.md
+-rw-r--r--   0        0        0      115 2023-07-09 19:27:30.779141 canada_holiday-1.1.3/canada_holiday/__init__.py
+-rw-r--r--   0        0        0     6456 2023-07-23 17:29:04.827449 canada_holiday-1.1.3/canada_holiday/holiday_class.py
+-rw-r--r--   0        0        0        0 2023-07-09 19:27:30.779340 canada_holiday-1.1.3/canada_holiday/holiday_info/__init__.py
+-rw-r--r--   0        0        0      812 2023-07-09 19:27:30.779448 canada_holiday-1.1.3/canada_holiday/holiday_info/ab.py
+-rw-r--r--   0        0        0      846 2023-07-09 19:27:30.779546 canada_holiday-1.1.3/canada_holiday/holiday_info/all.py
+-rw-r--r--   0        0        0      862 2023-07-09 19:27:30.779620 canada_holiday-1.1.3/canada_holiday/holiday_info/bc.py
+-rw-r--r--   0        0        0      670 2023-07-09 19:27:30.779709 canada_holiday-1.1.3/canada_holiday/holiday_info/mb.py
+-rw-r--r--   0        0        0      453 2023-07-09 19:27:30.779782 canada_holiday-1.1.3/canada_holiday/holiday_info/national.py
+-rw-r--r--   0        0        0      524 2023-07-09 19:27:30.779849 canada_holiday-1.1.3/canada_holiday/holiday_info/nb.py
+-rw-r--r--   0        0        0      671 2023-07-09 19:27:30.779923 canada_holiday-1.1.3/canada_holiday/holiday_info/nl.py
+-rw-r--r--   0        0        0      357 2023-07-09 19:27:30.780002 canada_holiday-1.1.3/canada_holiday/holiday_info/ns.py
+-rw-r--r--   0        0        0      706 2023-07-09 19:27:30.780089 canada_holiday-1.1.3/canada_holiday/holiday_info/nt.py
+-rw-r--r--   0        0        0      584 2023-07-09 19:27:30.780164 canada_holiday-1.1.3/canada_holiday/holiday_info/nu.py
+-rw-r--r--   0        0        0      888 2023-07-09 19:27:30.780244 canada_holiday-1.1.3/canada_holiday/holiday_info/on.py
+-rw-r--r--   0        0        0      384 2023-07-09 19:27:30.780328 canada_holiday-1.1.3/canada_holiday/holiday_info/pe.py
+-rw-r--r--   0        0        0      658 2023-07-09 19:27:30.780395 canada_holiday-1.1.3/canada_holiday/holiday_info/qc.py
+-rw-r--r--   0        0        0      686 2023-07-09 19:27:30.780468 canada_holiday-1.1.3/canada_holiday/holiday_info/sk.py
+-rw-r--r--   0        0        0      876 2023-07-09 19:27:30.780547 canada_holiday-1.1.3/canada_holiday/holiday_info/yt.py
+-rwxr-xr-x   0        0        0     2744 2023-07-09 19:27:30.780648 canada_holiday-1.1.3/canada_holiday/holidays.py
+-rw-r--r--   0        0        0     4599 2023-07-23 17:29:04.827740 canada_holiday-1.1.3/canada_holiday/utils.py
+-rw-r--r--   0        0        0      482 2023-07-23 17:29:19.855091 canada_holiday-1.1.3/pyproject.toml
+-rw-r--r--   0        0        0     2182 1970-01-01 00:00:00.000000 canada_holiday-1.1.3/PKG-INFO
```

### Comparing `canada_holiday-1.0.3/LICENSE` & `canada_holiday-1.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/README.md` & `canada_holiday-1.1.3/README.md`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_class.py` & `canada_holiday-1.1.3/canada_holiday/holiday_class.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 from calendar import Calendar
 import datetime
 
 from canada_holiday.utils import (
     DAY_TO_INDEX,
     find_easter_day,
+    get_day_of_the_week_idx,
     get_last_day_str_of_month,
     parse_preceding_day_str,
 )
 
 cal = Calendar()
 
 
@@ -34,14 +35,16 @@
         self._date = date  # ex: datetime.date(2023, 12, 25)
         self.nearest_day = nearest_day
         self.nth_day = nth_day
         self.preceding_date = preceding_date
         self.province = province
         self.succeeding_date = succeeding_date
 
+        self.validate_holiday_condition()
+
     def __repr__(self):
         return f"CanadaHoliday({self.name}, {self.date}, {self.day_of_the_week}, {self.province})"
 
     @property
     def date(self):
         return self._date
 
@@ -53,105 +56,115 @@
     def day_of_the_week(self):
         return self._day_of_the_week
 
     @day_of_the_week.setter
     def day_of_the_week(self, day_of_the_week: str):
         self._day_of_the_week = day_of_the_week
 
+    def validate_holiday_condition(self) -> None:
+        invalid = False
+        if self.nth_day:
+            invalid = any([self.preceding_date, self.succeeding_date, self.nearest_day])
+        elif self.nearest_day:
+            invalid = any([self.nth_day, self.preceding_date, self.succeeding_date])
+        elif self.preceding_date:
+            invalid = any([self.nth_day, self.succeeding_date, self.nearest_day])
+        elif self.succeeding_date:
+            invalid = any([self.nth_day, self.preceding_date, self.nearest_day])
+
+        if invalid:
+            raise Exception(
+                f"Cannot validate the Holiday. Please check the Holiday: {self.name}."
+            )
+
     def get_nth_day_holiday(self, year: int) -> datetime.date:
-        if self.preceding_date or self.succeeding_date or self.nearest_day:
-            raise Exception(f"Please check the Holiday: {self.name}.")
-        day_of_the_week, n = self.nth_day
-        day_of_the_week_idx = DAY_TO_INDEX[day_of_the_week]
+        """
+        Get holiday that has a rule of being nth day of a month.
+        ex: Thanksgiving Day is 2nd Monday in October.
+        """
+        day_of_the_week_idx, n = get_day_of_the_week_idx(self.nth_day)
         day_in_first_week = cal.monthdatescalendar(year, self.month)[0][
             day_of_the_week_idx
         ]
         if day_in_first_week.month == self.month:
             return cal.monthdatescalendar(year, self.month)[n - 1][day_of_the_week_idx]
         else:
             return cal.monthdatescalendar(year, self.month)[n][day_of_the_week_idx]
 
     def get_preceding_day_holiday(self, year: int) -> datetime.date:
-        if self.nth_day or self.succeeding_date or self.nearest_day:
-            raise Exception(f"Please check the Holiday: {self.name}.")
-
-        (
-            day_of_the_week,
-            preceding_day,
-        ) = self.preceding_date  # ex: Monday before May 25th
-        day_of_the_week_idx = DAY_TO_INDEX[day_of_the_week]
+        """
+        Get holiday that has a rule of being a day before a certain date
+        ex: Victoria Day is Monday before May 25th.
+        """
+        day_of_the_week_idx, preceding_day = get_day_of_the_week_idx(
+            self.preceding_date
+        )
+        precede_date = None
 
         if isinstance(preceding_day, str):
-            pre_day_str1, pre_day_str2 = parse_preceding_day_str(preceding_day)
-            if pre_day_str1.lower() == "last":
+            order_of_day, day_str = parse_preceding_day_str(preceding_day)
+            if order_of_day.lower() == "last":
                 precede_date = get_last_day_str_of_month(
-                    year, self.month, pre_day_str2.lower()
+                    year, self.month, day_str.lower()
                 )
             elif preceding_day == "Easter Sunday":
                 precede_date = find_easter_day(year)
         else:
             precede_date = datetime.date(year, self.month, preceding_day)
         precede_day_idx = precede_date.weekday()
         delta_days = abs(precede_day_idx - day_of_the_week_idx)
         # Find 'day_str' before easter_day
         return precede_date - datetime.timedelta(days=delta_days)
 
     def get_succeeding_day_holiday(self, year: int) -> datetime.date:
-        if self.nth_day or self.preceding_date or self.nearest_day:
-            raise Exception(f"Please check the Holiday: {self.name}.")
-
-        (
-            day_of_the_week,
-            succeeding_day,
-        ) = self.succeeding_date  # ex: Monday after Easter Sunday
-        day_of_the_week_idx = DAY_TO_INDEX[day_of_the_week]
+        """
+        Get holiday that has a rule of being a day after a certain date.
+        ex: Easter Monday is a Monday after Easter Sunday.
+        """
+        day_of_the_week_idx, succeeding_day = get_day_of_the_week_idx(
+            self.succeeding_date
+        )
 
         if succeeding_day == "Easter Sunday":
             succeed_date = find_easter_day(year)
         else:
             succeed_date = datetime.date(year, self.month, succeeding_day)
         succeed_day_idx = succeed_date.weekday()
         delta_days = abs(succeed_day_idx - day_of_the_week_idx)
         return succeed_date + datetime.timedelta(days=(7 - delta_days))
 
     def get_nearest_day_holiday(self, year: int) -> datetime.date:
         """
-        Example of calculating a nearest Monday:
-        - if holiday day is 23:
-            - if 23 is Sunday (6)    Monday (0) day + (7 - delta:6)
+        Get holiday that has a rule of being a day nearest to a certain date.
+        ex: St. George's Day is a Monday that's nearest to April 23rd.
+
+        Example of calculating a nearest Monday (0):
+        - if the given, certain date is on 23rd:
             - if 23 is Tuesday (1)   Monday (0) day - delta:1
             - if 23 is Wednesday (2) Monday (0) day - delta:2
             - if 23 is Thursday (3)  Monday (0) day - delta:3
             - if 23 is Friday (4)    Monday (0) day + (7 - delta:4)
             - if 23 is Saturday (5)  Monday (0) day + (7 - delta:5)
+            - if 23 is Sunday (6)    Monday (0) day + (7 - delta:6)
         """
-        if self.nth_day or self.preceding_date or self.succeeding_date:
-            raise Exception(f"Please check the Holiday: {self.name}.")
-
-        day_str, nearest_day = self.nearest_day
-        day_str_idx = DAY_TO_INDEX[day_str]
+        day_of_the_week_idx, _ = get_day_of_the_week_idx(self.nearest_day)
         nearest_date = datetime.date(year, self.month, self.nearest_day[1])
         nearest_day_str_idx = nearest_date.weekday()
-        delta_days = abs(day_str_idx - nearest_day_str_idx)
+        delta_days = abs(day_of_the_week_idx - nearest_day_str_idx)
 
         if delta_days < 4:
             return nearest_date - datetime.timedelta(delta_days)
         else:
             return nearest_date + datetime.timedelta(7 - delta_days)
 
     def to_date(self, year: int):
         """
-        Calculate the datetime.date of the given holiday
+        Calculate the datetime.date of the given holiday.
         """
-        if (
-            not self.nth_day
-            and not self.preceding_date
-            and not self.succeeding_date
-            and not self.nearest_day
-        ):
+        if self.month and self.day:
             return datetime.date(year, self.month, self.day)
 
         date = None
         if self.nth_day:
             date = self.get_nth_day_holiday(year)
         elif self.preceding_date:
             date = self.get_preceding_day_holiday(year)
```

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/ab.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/ab.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/all.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/all.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/bc.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/bc.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/mb.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/mb.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/nb.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/nb.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/nl.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/nl.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/nt.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/nt.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/nu.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/nu.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/on.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/on.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/qc.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/qc.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/sk.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/sk.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holiday_info/yt.py` & `canada_holiday-1.1.3/canada_holiday/holiday_info/yt.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/holidays.py` & `canada_holiday-1.1.3/canada_holiday/holidays.py`

 * *Files identical despite different names*

### Comparing `canada_holiday-1.0.3/canada_holiday/utils.py` & `canada_holiday-1.1.3/canada_holiday/utils.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 import calendar
 import datetime
 import math
+from typing import Union, Tuple
 
 
 cal = calendar.Calendar()
 DAY_TO_INDEX = {
     "mon": 0,
     "monday": 0,
     "tue": 1,
@@ -144,7 +145,14 @@
 def parse_preceding_day_str(preceding_day: str):
     preceding_day_str_list = preceding_day.split()
     if len(preceding_day_str_list) < 2:
         raise Exception(
             f"Please check the preceding day, ${preceding_day} of the month"
         )
     return preceding_day_str_list
+
+
+def get_day_of_the_week_idx(
+    day_condition: Tuple[str, Union[int, str]]
+) -> Tuple[int, Union[int, str]]:
+    day_of_the_week, condition = day_condition
+    return DAY_TO_INDEX[day_of_the_week], condition
```

### Comparing `canada_holiday-1.0.3/PKG-INFO` & `canada_holiday-1.1.3/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: canada-holiday
-Version: 1.0.3
+Version: 1.1.3
 Summary: Python package for Canadian holidays
 Home-page: https://github.com/kmsunmin/canada-holiday
 Author: Sunmin Kim
 Author-email: kmsunmin@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
```

