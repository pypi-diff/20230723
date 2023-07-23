# Comparing `tmp/statprocon-0.0.8.tar.gz` & `tmp/statprocon-0.0.9.tar.gz`

## Comparing `statprocon-0.0.8.tar` & `statprocon-0.0.9.tar`

### file list

```diff
@@ -1,24 +1,24 @@
--rw-r--r--   0        0        0      581 2020-02-02 00:00:00.000000 statprocon-0.0.8/CHANGELOG.md
--rw-r--r--   0        0        0       19 2020-02-02 00:00:00.000000 statprocon-0.0.8/CODEOWNERS
--rw-r--r--   0        0        0      691 2020-02-02 00:00:00.000000 statprocon-0.0.8/requirements-dev.txt
--rw-r--r--   0        0        0      176 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/.gitignore
--rw-r--r--   0        0        0      145 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/dataSources.local.xml
--rw-r--r--   0        0        0      199 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/misc.xml
--rw-r--r--   0        0        0      258 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/modules.xml
--rw-r--r--   0        0        0      180 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/vcs.xml
--rw-r--r--   0        0        0     5833 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/workspace.xml
--rw-r--r--   0        0        0      516 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/xmr.iml
--rw-r--r--   0        0        0      149 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/codeStyles/codeStyleConfig.xml
--rw-r--r--   0        0        0      438 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/inspectionProfiles/Project_Default.xml
--rw-r--r--   0        0        0      174 2020-02-02 00:00:00.000000 statprocon-0.0.8/.idea/inspectionProfiles/profiles_settings.xml
--rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 statprocon-0.0.8/statprocon/__init__.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 statprocon-0.0.8/statprocon/py.typed
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 statprocon-0.0.8/statprocon/charts/__init__.py
--rw-r--r--   0        0        0     9652 2020-02-02 00:00:00.000000 statprocon-0.0.8/statprocon/charts/xmr.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 statprocon-0.0.8/tests/__init__.py
--rw-r--r--   0        0        0     9111 2020-02-02 00:00:00.000000 statprocon-0.0.8/tests/test_xmr.py
--rw-r--r--   0        0        0       11 2020-02-02 00:00:00.000000 statprocon-0.0.8/.gitignore
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 statprocon-0.0.8/LICENSE
--rw-r--r--   0        0        0     3128 2020-02-02 00:00:00.000000 statprocon-0.0.8/README.md
--rw-r--r--   0        0        0      863 2020-02-02 00:00:00.000000 statprocon-0.0.8/pyproject.toml
--rw-r--r--   0        0        0     3909 2020-02-02 00:00:00.000000 statprocon-0.0.8/PKG-INFO
+-rw-r--r--   0        0        0      691 2020-02-02 00:00:00.000000 statprocon-0.0.9/CHANGELOG.md
+-rw-r--r--   0        0        0       19 2020-02-02 00:00:00.000000 statprocon-0.0.9/CODEOWNERS
+-rw-r--r--   0        0        0      691 2020-02-02 00:00:00.000000 statprocon-0.0.9/requirements-dev.txt
+-rw-r--r--   0        0        0      176 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/.gitignore
+-rw-r--r--   0        0        0      145 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/dataSources.local.xml
+-rw-r--r--   0        0        0      199 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/misc.xml
+-rw-r--r--   0        0        0      258 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/modules.xml
+-rw-r--r--   0        0        0      180 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/vcs.xml
+-rw-r--r--   0        0        0     5863 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/workspace.xml
+-rw-r--r--   0        0        0      516 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/xmr.iml
+-rw-r--r--   0        0        0      149 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/codeStyles/codeStyleConfig.xml
+-rw-r--r--   0        0        0      438 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/inspectionProfiles/Project_Default.xml
+-rw-r--r--   0        0        0      174 2020-02-02 00:00:00.000000 statprocon-0.0.9/.idea/inspectionProfiles/profiles_settings.xml
+-rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 statprocon-0.0.9/statprocon/__init__.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 statprocon-0.0.9/statprocon/py.typed
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 statprocon-0.0.9/statprocon/charts/__init__.py
+-rw-r--r--   0        0        0    10005 2020-02-02 00:00:00.000000 statprocon-0.0.9/statprocon/charts/xmr.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 statprocon-0.0.9/tests/__init__.py
+-rw-r--r--   0        0        0     9292 2020-02-02 00:00:00.000000 statprocon-0.0.9/tests/test_xmr.py
+-rw-r--r--   0        0        0       11 2020-02-02 00:00:00.000000 statprocon-0.0.9/.gitignore
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 statprocon-0.0.9/LICENSE
+-rw-r--r--   0        0        0     4334 2020-02-02 00:00:00.000000 statprocon-0.0.9/README.md
+-rw-r--r--   0        0        0      864 2020-02-02 00:00:00.000000 statprocon-0.0.9/pyproject.toml
+-rw-r--r--   0        0        0     5116 2020-02-02 00:00:00.000000 statprocon-0.0.9/PKG-INFO
```

### Comparing `statprocon-0.0.8/requirements-dev.txt` & `statprocon-0.0.9/requirements-dev.txt`

 * *Files identical despite different names*

### Comparing `statprocon-0.0.8/.idea/workspace.xml` & `statprocon-0.0.9/.idea/workspace.xml`

 * *Files 2% similar despite different names*

#### Comparing `statprocon-0.0.8/.idea/workspace.xml` & `statprocon-0.0.9/.idea/workspace.xml`

```diff
@@ -1,15 +1,14 @@
 <?xml version="1.0" encoding="utf-8"?>
 <project version="4">
   <component name="AutoImportSettings">
     <option name="autoReloadType" value="SELECTIVE"/>
   </component>
   <component name="ChangeListManager">
     <list default="true" id="6b007249-c07a-402d-ab76-cd0adebb4623" name="Default Changelist" comment="">
-      <change beforePath="$PROJECT_DIR$/CHANGELOG.md" beforeDir="false" afterPath="$PROJECT_DIR$/CHANGELOG.md" afterDir="false"/>
       <change beforePath="$PROJECT_DIR$/statprocon/charts/xmr.py" beforeDir="false" afterPath="$PROJECT_DIR$/statprocon/charts/xmr.py" afterDir="false"/>
     </list>
     <option name="SHOW_DIALOG" value="false"/>
     <option name="HIGHLIGHT_CONFLICTS" value="true"/>
     <option name="HIGHLIGHT_NON_ACTIVE_CHANGELIST" value="false"/>
     <option name="LAST_RESOLUTION" value="IGNORE"/>
   </component>
@@ -28,14 +27,17 @@
     <file-type-list>
       <filtered-out-file-type name="LOCAL_BRANCH"/>
       <filtered-out-file-type name="REMOTE_BRANCH"/>
       <filtered-out-file-type name="TAG"/>
       <filtered-out-file-type name="COMMIT_BY_MESSAGE"/>
     </file-type-list>
   </component>
+  <component name="ProblemsViewState">
+    <option name="selectedIndex" value="2"/>
+  </component>
   <component name="ProjectId" id="2SIH9DVr992iTq0PjX0glZoo5QS"/>
   <component name="ProjectLevelVcsManager" settingsEditedManually="true">
     <ConfirmationsSetting value="1" id="Add"/>
   </component>
   <component name="ProjectViewState">
     <option name="autoscrollFromSource" value="true"/>
     <option name="hideEmptyMiddlePackages" value="true"/>
@@ -50,14 +52,15 @@
     <property name="node.js.detected.package.tslint" value="true"/>
     <property name="node.js.selected.package.eslint" value="(autodetect)"/>
     <property name="node.js.selected.package.tslint" value="(autodetect)"/>
     <property name="settings.editor.selected.configurable" value="preferences.externalTools"/>
   </component>
   <component name="RecentsManager">
     <key name="MoveFile.RECENT_KEYS">
+      <recent name="$PROJECT_DIR$/statprocon/charts/xmr"/>
       <recent name="$PROJECT_DIR$/statprocon/charts"/>
       <recent name="$PROJECT_DIR$"/>
     </key>
   </component>
   <component name="RunManager">
     <configuration name="Unittests for test_xmr.XmRTestCase.test_rule_1_points_beyond_both_limits" type="tests" factoryName="Unittests" temporary="true" nameIsGenerated="true">
       <module name="xmr"/>
@@ -87,15 +90,15 @@
       <created>1688827023388</created>
       <option name="number" value="Default"/>
       <option name="presentableId" value="Default"/>
       <updated>1688827023388</updated>
       <workItem from="1688827024910" duration="1917000"/>
       <workItem from="1688848868641" duration="17704000"/>
       <workItem from="1688944372544" duration="17391000"/>
-      <workItem from="1690054614395" duration="3077000"/>
+      <workItem from="1690054614395" duration="20831000"/>
     </task>
     <servers/>
   </component>
   <component name="TypeScriptGeneratedFilesManager">
     <option name="version" value="3"/>
   </component>
   <component name="Vcs.Log.Tabs.Properties">
```

### Comparing `statprocon-0.0.8/.idea/xmr.iml` & `statprocon-0.0.9/.idea/xmr.iml`

 * *Files identical despite different names*

### Comparing `statprocon-0.0.8/statprocon/charts/xmr.py` & `statprocon-0.0.9/statprocon/charts/xmr.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 import csv
 import io
 
 from decimal import Decimal
-from typing import cast, Union, Optional, Sequence
+from typing import cast, Union, Optional, Sequence, TypeAlias
 
-TYPE_COUNT_VALUE = Decimal | int
-TYPE_MOVING_RANGE_VALUE = Decimal | int | None
+TYPE_COUNT_VALUE: TypeAlias = Decimal | int
+TYPE_MOVING_RANGE_VALUE: TypeAlias = Decimal | int | None
 
-TYPE_COUNTS = Sequence[TYPE_COUNT_VALUE | float]
-TYPE_MOVING_RANGES = Sequence[TYPE_MOVING_RANGE_VALUE]
+TYPE_COUNTS: TypeAlias = Sequence[TYPE_COUNT_VALUE | float]
+TYPE_MOVING_RANGES: TypeAlias = Sequence[TYPE_MOVING_RANGE_VALUE]
 
 
 class XmR:
     ROUNDING = 3
 
     def __init__(
             self,
@@ -46,32 +46,29 @@
             result += f'{k_format}: {values}\n'
         return result
 
     def x_to_dict(self) -> dict:
         """
         Return the values needed for the X chart as a dictionary
         """
-        n = len(self.counts)
         return {
             'values': self.counts,
-            'unpl': [self.upper_natural_process_limit()] * n,
-            'cl': [self.x_central_line()] * n,
-            'lnpl': [self.lower_natural_process_limit()] * n,
+            'unpl': self.upper_natural_process_limit(),
+            'cl': self.x_central_line(),
+            'lnpl': self.lower_natural_process_limit(),
         }
 
     def mr_to_dict(self) -> dict:
         """
         Return the values needed for the MR chart as a dictionary
         """
-        mr = self.moving_ranges()
-        n = len(mr)
         return {
-            'values': mr,
-            'url': [self.upper_range_limit()] * n,
-            'cl': [self.mr_central_line()] * n,
+            'values': self.moving_ranges(),
+            'url': self.upper_range_limit(),
+            'cl': self.mr_central_line(),
         }
 
     def to_dict(self) -> dict:
         # Naming comes from pg. 163
         #   So Which Way Should You Compute Limits? from Making Sense of Data
         result = {}
         for k, v in self.x_to_dict().items():
@@ -81,26 +78,24 @@
 
         return result
 
     def to_csv(self) -> str:
         output = io.StringIO()
         writer = csv.writer(output)
 
-        unpl = self.upper_natural_process_limit()
-        x_bar = self.x_central_line()
-        lnpl = self.lower_natural_process_limit()
-        moving_ranges = self.moving_ranges()
-        url = self.upper_range_limit()
-        mr_bar = self.mr_central_line()
-
         writer.writerow(['x_values', 'x_unpl', 'x_cl', 'x_lnpl', 'mr_values', 'mr_url', 'mr_cl'])
-        for i, x in enumerate(self.counts):
-            row = [x, unpl, x_bar, lnpl, moving_ranges[i], url, mr_bar]
-            writer.writerow(row)
-
+        writer.writerows(zip(
+            self.counts,
+            self.upper_natural_process_limit(),
+            self.x_central_line(),
+            self.lower_natural_process_limit(),
+            self.moving_ranges(),
+            self.upper_range_limit(),
+            self.mr_central_line()
+        ))
         return output.getvalue()
 
     def moving_ranges(self) -> TYPE_MOVING_RANGES:
         """
         Moving ranges are the absolute differences between successive count values.
         The first element will always be None
         """
@@ -113,39 +108,41 @@
                 result.append(None)
             else:
                 value = cast(Union[Decimal | int], abs(c - self.counts[i - 1]))
                 result.append(value)
         self._mr = result
         return self._mr
 
-    def x_central_line(self) -> Decimal:
+    def x_central_line(self) -> Sequence[Decimal]:
         avg = self.mean(self.counts[self.i:self.j])
-        return self.round(avg)
+        return [self.round(avg)] * len(self.counts)
 
-    def mr_central_line(self) -> Decimal:
-        assert self.moving_ranges()[0] is None
-        valid_values = cast(TYPE_COUNTS, self.moving_ranges()[self.i+1:self.j])
+    def mr_central_line(self) -> Sequence[Decimal]:
+        mr = self.moving_ranges()
+        assert mr[0] is None
+        valid_values = cast(TYPE_COUNTS, mr[self.i+1:self.j])
         avg = self.mean(valid_values)
-        return self.round(avg)
-
-    def upper_range_limit(self) -> Decimal:
-        limit = Decimal('3.268') * self.mr_central_line()
-        return self.round(limit)
+        return [self.round(avg)] * len(mr)
 
-    def upper_natural_process_limit(self) -> Decimal:
-        limit = self.x_central_line() + (Decimal('2.660') * self.mr_central_line())
-        return self.round(limit)
+    def upper_range_limit(self) -> Sequence[Decimal]:
+        mr_cl = self.mr_central_line()
+        limit = Decimal('3.268') * mr_cl[0]
+        return [self.round(limit)] * len(mr_cl)
+
+    def upper_natural_process_limit(self) -> Sequence[Decimal]:
+        limit = self.x_central_line()[0] + (Decimal('2.660') * self.mr_central_line()[0])
+        return [self.round(limit)] * len(self.counts)
 
-    def lower_natural_process_limit(self) -> Decimal:
+    def lower_natural_process_limit(self) -> Sequence[Decimal]:
         """
         LNPL can be negative.
         It's the caller's responsibility to take max(LNPL, 0) if a negative LNPL does not make sense
         """
-        limit = self.x_central_line() - (Decimal('2.660') * self.mr_central_line())
-        return self.round(limit)
+        limit = self.x_central_line()[0] - (Decimal('2.660') * self.mr_central_line()[0])
+        return [self.round(limit)] * len(self.counts)
 
     def rule_1_x_indices_beyond_limits(
             self,
             upper_limit: Optional[Decimal] = None,
             lower_limit: Optional[Decimal] = None
     ) -> list[bool]:
         """
@@ -158,17 +155,22 @@
 
         :param upper_limit: Optional - Will default to the Upper Natural Process Limit
         :param lower_limit: Optional - Will default to the Lower Natural Process Limit
 
         :return: list[bool] A list of boolean values of length(counts)
             True at index i means that self.counts[i] is above the upper_limit or below the lower_limit
         """
-
-        upper = upper_limit or self.upper_natural_process_limit()
-        lower = lower_limit or self.lower_natural_process_limit()
+        n = len(self.counts)
+        upper = self.upper_natural_process_limit()
+        if upper_limit:
+            upper = [upper_limit] * n
+
+        lower = self.lower_natural_process_limit()
+        if lower_limit:
+            lower = [lower_limit] * n
 
         return self._points_beyond_limits(self.counts, upper, lower)
 
     def rule_1_mr_indices_beyond_limits(self) -> list[bool]:
         """
         Points Outside the Limits
 
@@ -230,53 +232,55 @@
         all within the upper 25% of the region between the limits, or
         all within the lower 25% of the region between the limits,
         may be interpreted as an indication of the presence
         of an assignable cause which has a *moderate* but sustained effect.
         """
         result = [False] * len(self.counts)
 
-        unpl = self.upper_natural_process_limit()
-        lnpl = self.lower_natural_process_limit()
-        upper_25 = ((unpl - lnpl) * Decimal('.75')) + lnpl
-        lower_25 = ((unpl - lnpl) * Decimal('.25')) + lnpl
-
         # positive value is point near upper limit
         # negative value is point near lower limit
         near_limits = [0] * len(self.counts)
 
-        for i, x in enumerate(self.counts):
+        values = zip(self.counts, self.upper_natural_process_limit(), self.lower_natural_process_limit())
+        for i, (x, unpl, lnpl) in enumerate(values):
+            upper_25 = ((unpl - lnpl) * Decimal('.75')) + lnpl
+            lower_25 = ((unpl - lnpl) * Decimal('.25')) + lnpl
             if x < lower_25:
                 near_limits[i] = -1
 
             if x > upper_25:
                 near_limits[i] = 1
 
             if i >= 3:
                 successive_values = near_limits[i - 3:i + 1]
                 if abs(sum(successive_values)) >= 3:
                     for j in range(i - 3, i + 1):
                         result[j] = True
 
         return result
 
-    def round(self, value: Decimal):
+    def round(self, value: Decimal) -> Decimal:
         return round(value, self.ROUNDING)
 
     @staticmethod
     def _points_beyond_limits(
             data: TYPE_COUNTS | TYPE_MOVING_RANGES,
-            upper_limit: Decimal,
-            lower_limit: Decimal = Decimal('0')
+            upper_limits: Sequence[Decimal],
+            lower_limits: Optional[Sequence[Decimal]] = None
     ) -> list[bool]:
         result = [False] * len(data)
-        for i, val in enumerate(data):
-            if val is None:
+
+        if lower_limits is None:
+            lower_limits = [Decimal('-Inf')] * len(upper_limits)
+
+        for i, (x, w, y) in enumerate(zip(data, lower_limits, upper_limits)):
+            if x is None:  # first index of Moving Ranges
                 continue
 
-            if not lower_limit <= val <= upper_limit:
+            if not w <= x <= y:
                 result[i] = True
 
         return result
 
     @staticmethod
     def mean(nums: TYPE_COUNTS) -> Decimal:
         s = sum(nums)
```

### Comparing `statprocon-0.0.8/tests/test_xmr.py` & `statprocon-0.0.9/tests/test_xmr.py`

 * *Files 8% similar despite different names*

```diff
@@ -36,15 +36,15 @@
 5,6.660,4.000,1.340,1,3.268,1.000\r
 """
         self.assertEqual(xmr.to_csv(), expected)
 
     def test_average_contains_one_more_exponent_as_input(self):
         counts = [3, 3, 4]
         xmr = XmR(counts)
-        self.assertEqual(xmr.x_central_line(), Decimal('3.333'))
+        self._assert_line_equals(xmr, 'x_central_line', Decimal('3.333'))
 
     def test_moving_range_ints(self):
         counts = [1, 10, 100, 50]
         xmr = XmR(counts)
         mr = xmr.moving_ranges()
         self.assertEqual(mr, [None, 9, 90, 50])
 
@@ -60,42 +60,39 @@
         mr = xmr.moving_ranges()
         expected = [None, Decimal('1.6'), Decimal('4.95'), Decimal('5.15'), Decimal('0.6'), Decimal('3'), Decimal('1.4'), Decimal('2.6'), Decimal('4.2'), Decimal('0.8'), Decimal('3.6'), Decimal('5.8')]
         self.assertListEqual(mr, expected)
 
     def test_upper_range_limit(self):
         counts = [1,51, 100, 50]
         xmr = XmR(counts)
-        url = xmr.upper_range_limit()
-        self.assertEqual(url, Decimal('162.312'))
+        self._assert_line_equals(xmr, 'upper_range_limit', Decimal('162.312'))
 
     def test_upper_natural_process_limit(self):
         counts = [1, 10, 100, 50]
         xmr = XmR(counts)
-        limit = xmr.upper_natural_process_limit()
-        self.assertEqual(limit, Decimal('172.364'))
+        self._assert_line_equals(xmr, 'upper_natural_process_limit', Decimal('172.364'))
 
     def test_lower_natural_process_limit(self):
         counts = [1, 10, 100, 50]
         xmr = XmR(counts)
-        limit = xmr.lower_natural_process_limit()
-        self.assertEqual(limit, Decimal('-91.864'))
+        self._assert_line_equals(xmr, 'lower_natural_process_limit', Decimal('-91.864'))
 
     def test_limits_with_subsets(self):
         counts = [1] * 25
         counts[1] = 10
         counts[2] = 100
         counts[3] = 50
 
         xmr = XmR(counts, subset_end_index=24)
-        self.assertEqual(xmr.upper_natural_process_limit(), Decimal('30.442'))
-        self.assertEqual(xmr.upper_range_limit(), Decimal('28.134'))
+        self._assert_line_equals(xmr, 'upper_natural_process_limit', Decimal('30.442'))
+        self._assert_line_equals(xmr, 'upper_range_limit', Decimal('28.134'))
 
         # Adjust manually so that all subset values should be 1
         xmr.i = 4
-        self.assertEqual(xmr.x_central_line(), 1)
+        self._assert_line_equals(xmr, 'x_central_line', 1)
         self.assertEqual(xmr.lower_natural_process_limit(), xmr.upper_natural_process_limit())
 
     def test_rule_1_points_beyond_upper_limits(self):
         """
         This test dataset comes from Table 9.1: Accident Rates in Making Sense of Data
         """
 
@@ -207,18 +204,18 @@
         unpl = Decimal('5082.28')
         url = Decimal('1163.19')
 
         xmr = XmR(counts)
 
         self.assertListEqual(xmr.moving_ranges(), moving_ranges)
         self.assertEqual(x_avg, xmr.mean(counts))
-        self.assertEqual(mr_avg, round(xmr.mr_central_line(), 2))
-        self.assertEqual(lnpl, round(xmr.lower_natural_process_limit(), 2))
-        self.assertEqual(unpl, round(xmr.upper_natural_process_limit(), 2))
-        self.assertEqual(url, round(xmr.upper_range_limit(), 2))
+        self.assertEqual(mr_avg, round(xmr.mr_central_line()[0], 2))
+        self.assertEqual(lnpl, round(xmr.lower_natural_process_limit()[0], 2))
+        self.assertEqual(unpl, round(xmr.upper_natural_process_limit()[0], 2))
+        self.assertEqual(url, round(xmr.upper_range_limit()[0], 2))
 
     def test_peak_flow_rates(self):
         """
         Data comes from pg 130 of "Making Sense of Data"
         Figure 9.9 XmR Chart for AM Premedication Peak Flow Rates for Days 1 to 18
         """
 
@@ -232,11 +229,15 @@
         lnpl = Decimal('43.8')  # 43.7 in book
         url = Decimal('171.1')  # 171.3 in book
 
         xmr = XmR(x_values)
 
         self.assertListEqual(xmr.moving_ranges(), mr_values)
         self.assertEqual(x_avg, round(xmr.mean(x_values), 1))
-        self.assertEqual(mr_avg, round(xmr.mr_central_line(), 1))
-        self.assertEqual(lnpl, round(xmr.lower_natural_process_limit(), 1))
-        self.assertEqual(unpl, round(xmr.upper_natural_process_limit(), 1))
-        self.assertEqual(url, round(xmr.upper_range_limit(), 1))
+        self.assertEqual(mr_avg, round(xmr.mr_central_line()[0], 1))
+        self.assertEqual(lnpl, round(xmr.lower_natural_process_limit()[0], 1))
+        self.assertEqual(unpl, round(xmr.upper_natural_process_limit()[0], 1))
+        self.assertEqual(url, round(xmr.upper_range_limit()[0], 1))
+
+    def _assert_line_equals(self, xmr, func, value):
+        actual = getattr(xmr, func)()
+        self.assertListEqual(actual, [value] * len(xmr.counts))
```

### Comparing `statprocon-0.0.8/LICENSE` & `statprocon-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `statprocon-0.0.8/README.md` & `statprocon-0.0.9/README.md`

 * *Files 25% similar despite different names*

```diff
@@ -14,62 +14,91 @@
 ```python
 from statprocon import XmR
 
 counts = [10, 50, 40, 30]
 
 xmr = XmR(counts)
 moving_ranges = xmr.moving_ranges()
-unpl = xmr.upper_natural_process_limit()
-lnpl = xmr.lower_natural_process_limit()
-x_bar = xmr.x_central_line()
+unpl = xmr.upper_natural_process_limit()[0]  # 85.7
+lnpl = xmr.lower_natural_process_limit()[0]  # -20.7
+x_cl = xmr.x_central_line()[0]  # 32.5
 
-url = xmr.upper_range_limit()
-mr_bar = xmr.mr_central_line()
+url = xmr.upper_range_limit()[0]  # 65.36
+mr_cl = xmr.mr_central_line()[0]  # 20
 
 ```
 
 Currently, this library only supports the data for generating an XmR chart.
 An XmR chart is the simplest type of process behaviour chart.
 XmR is short for individual values (X) and a moving range (mR).
 More chart data options can be added via pull requests.
 
 For more information, please read [Making Sense of Data by Donald Wheeler](https://www.amazon.com/Making-Sense-Data-Donald-Wheeler/dp/0945320728).
 
+### pandas
+
+Visualize XmR charts using Jupyter Notebooks and [pandas](https://pandas.pydata.org/)
+
+```python
+import pandas as pd
+from statprocon import XmR
+
+xmr = XmR(counts)
+
+pd.DataFrame(xmr.x_to_dict()).astype(float).plot()
+pd.DataFrame(xmr.mr_to_dict()).astype(float).plot()
+```
+
+![Screenshot from 2023-07-22 13-53-22](https://github.com/mattmccormick/statprocon/assets/436801/b6a83903-4bb9-4935-9acb-c086d3420fd2)
+
+
 ### CSV
 
-Quickly generate a CSV of all the data needed to create XmR charts.
+Generate a CSV of all the data needed to create XmR charts.
 
 ```python
 print(xmr.to_csv())
 ```
 
 ### Google Sheets Charts
 
-Quickly generate XmR Charts in Google Sheets
+Generate XmR Charts in Google Sheets
 
 https://github.com/mattmccormick/statprocon/assets/436801/0de1a9f3-a8ad-4047-8c9d-0f890e0bf453
 
 1. Make a copy of the [statprocon XmR Template sheet](https://docs.google.com/spreadsheets/d/1IdCBpE8FK4qP8B7qHQeXX6amLZ8oyhc8OjlBlGHmWTg/edit?usp=sharing)
 1. Paste the CSV output from above into cell A1
 1. Click `Data -> Split Text to Columns`
 
 The X and MR charts will appear on the right.
 
 Note that the Lower Natural Process Limit may not make sense if your count data could not possibly go negative.
-If LNPL is not needed remove it by:
+If LNPL is not needed, remove it with the following steps:
 
-1. Double click on the X Chart
+1. Double-click on the X Chart
 1. Click the `Setup` tab
 1. Under `Series`, find `LNPL`
 1. Click the 3 dot menu on the right next to `LNPL`
 1. Click `Remove`
 
 The LNPL line will be removed from the X Chart.
 
+## Advanced Usage
+
+### Calculate Limits from Subset of Counts
+
+The central lines and limits calculations can be restricted to a subset of the count data.
+Use the `subset_start_index` and `subset_end_index` parameters when instantiating the XmR object:
+
+```python
+xmr = XmR(counts, subset_start_index=10, subset_end_index=34)  # 24 points of data starting at index 10
+```
 
+When one or both of these optional arguments are provided, the the X and MR central line calculations will be modified to only use the data from `subset_start_index` up to, but not including, `subset_end_index`.
+When these optional arguments are not provided, `subset_start_index` defaults to 0 and `subset_end_index` defaults to the length of `counts`.
 
 ## Dependencies
 
 There are a few other Python libraries for generating SPC charts but they all contain large dependencies in order to include the ability to graph the chart.
 This package will remain small and light and not require large dependencies.
 The user will need to convert the data into charts on their own.
```

### Comparing `statprocon-0.0.8/pyproject.toml` & `statprocon-0.0.9/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "statprocon"
-version = "0.0.8"
+version = "0.0.9"
 authors = [
   { name="Matt McCormick", email="mattmccor@gmail.com" },
 ]
 description = "A Python helper library for generating Process Behaviour Charts"
 readme = "README.md"
-requires-python = ">=3.7"
+requires-python = ">=3.10"
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
 keywords = ["Statistical Process Control", "SPC", "Quality Control Chart", "QCC", "Process Behaviour Chart", "Process Behavior Chart", "XmR", "Shewhart", "Wheeler"]
```

### Comparing `statprocon-0.0.8/PKG-INFO` & `statprocon-0.0.9/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 Metadata-Version: 2.1
 Name: statprocon
-Version: 0.0.8
+Version: 0.0.9
 Summary: A Python helper library for generating Process Behaviour Charts
 Project-URL: Homepage, https://github.com/mattmccormick/statprocon
 Project-URL: Bug Tracker, https://github.com/mattmccormick/statprocon/issues
 Project-URL: Changelog, https://github.com/mattmccormick/statprocon/blob/main/CHANGELOG.md
 Author-email: Matt McCormick <mattmccor@gmail.com>
 License-File: LICENSE
 Keywords: Process Behavior Chart,Process Behaviour Chart,QCC,Quality Control Chart,SPC,Shewhart,Statistical Process Control,Wheeler,XmR
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
-Requires-Python: >=3.7
+Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 
 # statprocon
 
 **statprocon** is a Python helper library for generating data for use in **Stat**istical **Pro**cess **Con**trol charts.
 SPC charts are also known as Process Behaviour Charts, Control charts or Shewhart charts.
 
@@ -30,62 +30,91 @@
 ```python
 from statprocon import XmR
 
 counts = [10, 50, 40, 30]
 
 xmr = XmR(counts)
 moving_ranges = xmr.moving_ranges()
-unpl = xmr.upper_natural_process_limit()
-lnpl = xmr.lower_natural_process_limit()
-x_bar = xmr.x_central_line()
+unpl = xmr.upper_natural_process_limit()[0]  # 85.7
+lnpl = xmr.lower_natural_process_limit()[0]  # -20.7
+x_cl = xmr.x_central_line()[0]  # 32.5
 
-url = xmr.upper_range_limit()
-mr_bar = xmr.mr_central_line()
+url = xmr.upper_range_limit()[0]  # 65.36
+mr_cl = xmr.mr_central_line()[0]  # 20
 
 ```
 
 Currently, this library only supports the data for generating an XmR chart.
 An XmR chart is the simplest type of process behaviour chart.
 XmR is short for individual values (X) and a moving range (mR).
 More chart data options can be added via pull requests.
 
 For more information, please read [Making Sense of Data by Donald Wheeler](https://www.amazon.com/Making-Sense-Data-Donald-Wheeler/dp/0945320728).
 
+### pandas
+
+Visualize XmR charts using Jupyter Notebooks and [pandas](https://pandas.pydata.org/)
+
+```python
+import pandas as pd
+from statprocon import XmR
+
+xmr = XmR(counts)
+
+pd.DataFrame(xmr.x_to_dict()).astype(float).plot()
+pd.DataFrame(xmr.mr_to_dict()).astype(float).plot()
+```
+
+![Screenshot from 2023-07-22 13-53-22](https://github.com/mattmccormick/statprocon/assets/436801/b6a83903-4bb9-4935-9acb-c086d3420fd2)
+
+
 ### CSV
 
-Quickly generate a CSV of all the data needed to create XmR charts.
+Generate a CSV of all the data needed to create XmR charts.
 
 ```python
 print(xmr.to_csv())
 ```
 
 ### Google Sheets Charts
 
-Quickly generate XmR Charts in Google Sheets
+Generate XmR Charts in Google Sheets
 
 https://github.com/mattmccormick/statprocon/assets/436801/0de1a9f3-a8ad-4047-8c9d-0f890e0bf453
 
 1. Make a copy of the [statprocon XmR Template sheet](https://docs.google.com/spreadsheets/d/1IdCBpE8FK4qP8B7qHQeXX6amLZ8oyhc8OjlBlGHmWTg/edit?usp=sharing)
 1. Paste the CSV output from above into cell A1
 1. Click `Data -> Split Text to Columns`
 
 The X and MR charts will appear on the right.
 
 Note that the Lower Natural Process Limit may not make sense if your count data could not possibly go negative.
-If LNPL is not needed remove it by:
+If LNPL is not needed, remove it with the following steps:
 
-1. Double click on the X Chart
+1. Double-click on the X Chart
 1. Click the `Setup` tab
 1. Under `Series`, find `LNPL`
 1. Click the 3 dot menu on the right next to `LNPL`
 1. Click `Remove`
 
 The LNPL line will be removed from the X Chart.
 
+## Advanced Usage
+
+### Calculate Limits from Subset of Counts
+
+The central lines and limits calculations can be restricted to a subset of the count data.
+Use the `subset_start_index` and `subset_end_index` parameters when instantiating the XmR object:
+
+```python
+xmr = XmR(counts, subset_start_index=10, subset_end_index=34)  # 24 points of data starting at index 10
+```
 
+When one or both of these optional arguments are provided, the the X and MR central line calculations will be modified to only use the data from `subset_start_index` up to, but not including, `subset_end_index`.
+When these optional arguments are not provided, `subset_start_index` defaults to 0 and `subset_end_index` defaults to the length of `counts`.
 
 ## Dependencies
 
 There are a few other Python libraries for generating SPC charts but they all contain large dependencies in order to include the ability to graph the chart.
 This package will remain small and light and not require large dependencies.
 The user will need to convert the data into charts on their own.
```

