# Comparing `tmp/firefox_bookmarks-0.0.1.tar.gz` & `tmp/firefox_bookmarks-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "firefox_bookmarks-0.0.1.tar", max compression
+gzip compressed data, was "firefox_bookmarks-0.1.0.tar", max compression
```

## Comparing `firefox_bookmarks-0.0.1.tar` & `firefox_bookmarks-0.1.0.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0      137 2023-07-22 13:36:39.218944 firefox_bookmarks-0.0.1/firefox_bookmarks/__init__.py
--rw-r--r--   0        0        0      892 2023-07-22 16:41:48.207596 firefox_bookmarks-0.0.1/firefox_bookmarks/connect.py
--rw-r--r--   0        0        0      276 2023-07-22 14:07:55.049329 firefox_bookmarks-0.0.1/firefox_bookmarks/constants.py
--rw-r--r--   0        0        0     2280 2023-07-22 14:10:44.937368 firefox_bookmarks-0.0.1/firefox_bookmarks/locate.py
--rw-r--r--   0        0        0    35184 2023-07-21 16:18:12.325494 firefox_bookmarks-0.0.1/LICENSE
--rw-r--r--   0        0        0      684 2023-07-22 17:02:07.660368 firefox_bookmarks-0.0.1/pyproject.toml
--rw-r--r--   0        0        0      609 2023-07-22 17:20:34.631655 firefox_bookmarks-0.0.1/README.md
--rw-r--r--   0        0        0     1343 1970-01-01 00:00:00.000000 firefox_bookmarks-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0      137 2023-07-23 11:39:08.278273 firefox_bookmarks-0.1.0/firefox_bookmarks/__init__.py
+-rw-r--r--   0        0        0      892 2023-07-23 11:39:08.280116 firefox_bookmarks-0.1.0/firefox_bookmarks/connect.py
+-rw-r--r--   0        0        0      276 2023-07-22 14:07:55.049329 firefox_bookmarks-0.1.0/firefox_bookmarks/constants.py
+-rw-r--r--   0        0        0     2280 2023-07-22 14:10:44.937368 firefox_bookmarks-0.1.0/firefox_bookmarks/locate.py
+-rw-r--r--   0        0        0    35184 2023-07-21 16:18:12.325494 firefox_bookmarks-0.1.0/LICENSE
+-rw-r--r--   0        0        0     1235 2023-07-23 08:37:01.651455 firefox_bookmarks-0.1.0/pyproject.toml
+-rw-r--r--   0        0        0      616 2023-07-23 08:35:10.919927 firefox_bookmarks-0.1.0/README.md
+-rw-r--r--   0        0        0     1910 1970-01-01 00:00:00.000000 firefox_bookmarks-0.1.0/PKG-INFO
```

### Comparing `firefox_bookmarks-0.0.1/firefox_bookmarks/connect.py` & `firefox_bookmarks-0.1.0/firefox_bookmarks/connect.py`

 * *Files identical despite different names*

### Comparing `firefox_bookmarks-0.0.1/firefox_bookmarks/locate.py` & `firefox_bookmarks-0.1.0/firefox_bookmarks/locate.py`

 * *Files identical despite different names*

### Comparing `firefox_bookmarks-0.0.1/LICENSE` & `firefox_bookmarks-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `firefox_bookmarks-0.0.1/README.md` & `firefox_bookmarks-0.1.0/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -12,8 +12,8 @@
 
 See [the examples directory](https://github.com/BURG3R5/firefox-bookmarks/tree/main/examples)
 
 ## license
 
 Copyright (C) 2023 Aditya Rajput & other contributors
 
-This software is licensed under the Affero GPL v3. You should have received [a copy](https://github.com/BURG3R5/firefox-bookmarks/blob/main/LICENSE) of the GNU Affero General Public License along with this program. If not, see [this](https://www.gnu.org/licenses/agpl-3.0.html#license-text).
+This software is licensed under the **Affero GPL v3**. You should have received [a copy](https://github.com/BURG3R5/firefox-bookmarks/blob/main/LICENSE) of the Affero GPL v3 along with this program. If not, you can visit the original [here](https://www.gnu.org/licenses/agpl-3.0.html#license-text).
```

