# Comparing `tmp/mytimer-0.6.tar.gz` & `tmp/mytimer-0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mytimer-0.6.tar", last modified: Tue Jul  4 19:07:01 2023, max compression
+gzip compressed data, was "mytimer-0.7.tar", last modified: Sun Jul 23 16:55:34 2023, max compression
```

## Comparing `mytimer-0.6.tar` & `mytimer-0.7.tar`

### file list

```diff
@@ -1,28 +1,38 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-04 19:07:01.832521 mytimer-0.6/
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-07-04 19:06:51.000000 mytimer-0.6/AUTHORS.md
--rw-r--r--   0 runner    (1001) docker     (123)     1706 2023-07-04 19:06:51.000000 mytimer-0.6/CHANGELOG.md
--rw-r--r--   0 runner    (1001) docker     (123)     6818 2023-07-04 19:06:51.000000 mytimer-0.6/FACES.md
--rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-07-04 19:06:51.000000 mytimer-0.6/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-04 19:06:51.000000 mytimer-0.6/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     9328 2023-07-04 19:07:01.832521 mytimer-0.6/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1581 2023-07-04 19:06:51.000000 mytimer-0.6/PROGRAMS.md
--rw-r--r--   0 runner    (1001) docker     (123)     6327 2023-07-04 19:06:51.000000 mytimer-0.6/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       74 2023-07-04 19:06:51.000000 mytimer-0.6/dev-requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-04 19:07:01.828521 mytimer-0.6/mytimer/
--rw-r--r--   0 runner    (1001) docker     (123)      122 2023-07-04 19:06:51.000000 mytimer-0.6/mytimer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1215 2023-07-04 19:06:51.000000 mytimer-0.6/mytimer/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6977 2023-07-04 19:06:51.000000 mytimer-0.6/mytimer/functions.py
--rw-r--r--   0 runner    (1001) docker     (123)     2913 2023-07-04 19:06:51.000000 mytimer-0.6/mytimer/params.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-04 19:07:01.832521 mytimer-0.6/mytimer/sounds/
--rw-r--r--   0 runner    (1001) docker     (123)     8114 2023-07-04 19:06:51.000000 mytimer-0.6/mytimer/sounds/1.wav
--rw-r--r--   0 runner    (1001) docker     (123)   602412 2023-07-04 19:06:51.000000 mytimer-0.6/mytimer/sounds/2.wav
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-04 19:07:01.832521 mytimer-0.6/mytimer.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     9328 2023-07-04 19:07:01.000000 mytimer-0.6/mytimer.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      430 2023-07-04 19:07:01.000000 mytimer-0.6/mytimer.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-04 19:07:01.000000 mytimer-0.6/mytimer.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       50 2023-07-04 19:07:01.000000 mytimer-0.6/mytimer.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-04 19:07:01.000000 mytimer-0.6/mytimer.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-04 19:07:01.000000 mytimer-0.6/mytimer.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-04 19:06:51.000000 mytimer-0.6/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-04 19:07:01.832521 mytimer-0.6/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2300 2023-07-04 19:06:51.000000 mytimer-0.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:55:34.441024 mytimer-0.7/
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-07-23 16:55:24.000000 mytimer-0.7/AUTHORS.md
+-rw-r--r--   0 runner    (1001) docker     (123)     2075 2023-07-23 16:55:24.000000 mytimer-0.7/CHANGELOG.md
+-rw-r--r--   0 runner    (1001) docker     (123)     7322 2023-07-23 16:55:24.000000 mytimer-0.7/FACES.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-07-23 16:55:24.000000 mytimer-0.7/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-23 16:55:24.000000 mytimer-0.7/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     9892 2023-07-23 16:55:34.441024 mytimer-0.7/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1786 2023-07-23 16:55:24.000000 mytimer-0.7/PROGRAMS.md
+-rw-r--r--   0 runner    (1001) docker     (123)     6522 2023-07-23 16:55:24.000000 mytimer-0.7/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     2322 2023-07-23 16:55:24.000000 mytimer-0.7/TONES.md
+-rw-r--r--   0 runner    (1001) docker     (123)       74 2023-07-23 16:55:24.000000 mytimer-0.7/dev-requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:55:34.437024 mytimer-0.7/mytimer/
+-rw-r--r--   0 runner    (1001) docker     (123)      122 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1369 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7399 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/functions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3337 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/params.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:55:34.441024 mytimer-0.7/mytimer/sounds/
+-rw-r--r--   0 runner    (1001) docker     (123)     8114 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/1.wav
+-rw-r--r--   0 runner    (1001) docker     (123)    16494 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/10.wav
+-rw-r--r--   0 runner    (1001) docker     (123)    11468 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/11.wav
+-rw-r--r--   0 runner    (1001) docker     (123)   602412 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/2.wav
+-rw-r--r--   0 runner    (1001) docker     (123)     5170 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/3.wav
+-rw-r--r--   0 runner    (1001) docker     (123)     5382 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/4.wav
+-rw-r--r--   0 runner    (1001) docker     (123)    15186 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/5.wav
+-rw-r--r--   0 runner    (1001) docker     (123)     9992 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/6.wav
+-rw-r--r--   0 runner    (1001) docker     (123)    10754 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/7.wav
+-rw-r--r--   0 runner    (1001) docker     (123)     5400 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/8.wav
+-rw-r--r--   0 runner    (1001) docker     (123)     7044 2023-07-23 16:55:24.000000 mytimer-0.7/mytimer/sounds/9.wav
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:55:34.437024 mytimer-0.7/mytimer.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     9892 2023-07-23 16:55:34.000000 mytimer-0.7/mytimer.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      630 2023-07-23 16:55:34.000000 mytimer-0.7/mytimer.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 16:55:34.000000 mytimer-0.7/mytimer.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       50 2023-07-23 16:55:34.000000 mytimer-0.7/mytimer.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 16:55:34.000000 mytimer-0.7/mytimer.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 16:55:34.000000 mytimer-0.7/mytimer.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-23 16:55:24.000000 mytimer-0.7/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 16:55:34.441024 mytimer-0.7/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2300 2023-07-23 16:55:24.000000 mytimer-0.7/setup.py
```

### Comparing `mytimer-0.6/CHANGELOG.md` & `mytimer-0.7/CHANGELOG.md`

 * *Files 12% similar despite different names*

```diff
@@ -1,14 +1,26 @@
 # Changelog
 All notable changes to this project will be documented in this file.
 
 The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
 and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).
 
 ## [Unreleased]
+## [0.7] - 2023-07-23
+### Added
+- `--tone` argument
+- `TONES.md`
+- 9 new tones
+### Changed
+- Test system modified
+- `input_check` decorator renamed to `input_handler`
+- `countup_timer` function inputs modified
+- `countdown_timer` function inputs modified
+- `PROGRAMS.md` updated
+- `FACES.md` updated
 ## [0.6] - 2023-07-04
 ### Added
 - `--program` argument
 - `PROGRAMS.md`
 - `run_timer` function
 ### Changed
 - Inputs type changed to `int`
@@ -46,15 +58,16 @@
 - `countup_timer` function modified
 ## [0.1] - 2022-10-18
 ### Added
 - Countdown mode
 - Count-up mode
 - Alarm
 
-[Unreleased]: https://github.com/sepandhaghighi/mytimer/compare/v0.6...dev
+[Unreleased]: https://github.com/sepandhaghighi/mytimer/compare/v0.7...dev
+[0.7]: https://github.com/sepandhaghighi/mytimer/compare/v0.6...v0.7
 [0.6]: https://github.com/sepandhaghighi/mytimer/compare/v0.5...v0.6
 [0.5]: https://github.com/sepandhaghighi/mytimer/compare/v0.4...v0.5
 [0.4]: https://github.com/sepandhaghighi/mytimer/compare/v0.3...v0.4
 [0.3]: https://github.com/sepandhaghighi/mytimer/compare/v0.2...v0.3
 [0.2]: https://github.com/sepandhaghighi/mytimer/compare/v0.1...v0.2
 [0.1]: https://github.com/sepandhaghighi/mytimer/compare/daa2be6...v0.1
```

### Comparing `mytimer-0.6/LICENSE` & `mytimer-0.7/LICENSE`

 * *Files identical despite different names*

### Comparing `mytimer-0.6/PKG-INFO` & `mytimer-0.7/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: mytimer
-Version: 0.6
+Version: 0.7
 Summary: Simple Timer for Your Terminal
 Home-page: https://github.com/sepandhaghighi/mytimer
-Download-URL: https://github.com/sepandhaghighi/mytimer/tarball/v0.6
+Download-URL: https://github.com/sepandhaghighi/mytimer/tarball/v0.7
 Author: Sepand Haghighi
 Author-email: sepand@pyrgg.ir
 License: MIT
 Project-URL: Source, https://github.com/sepandhaghighi/mytimer
 Keywords: python3 python timer terminal stopwatch
 Classifier: Development Status :: 4 - Beta
 Classifier: Natural Language :: English
@@ -111,21 +111,21 @@
 	</tr>
 </table>
 
 
 ## Installation		
 
 ### Source Code
-- Download [Version 0.6](https://github.com/sepandhaghighi/mytimer/archive/v0.6.zip) or [Latest Source ](https://github.com/sepandhaghighi/mytimer/archive/dev.zip)
+- Download [Version 0.7](https://github.com/sepandhaghighi/mytimer/archive/v0.7.zip) or [Latest Source ](https://github.com/sepandhaghighi/mytimer/archive/dev.zip)
 - `pip install .`				
 
 ### PyPI
 
 - Check [Python Packaging User Guide](https://packaging.python.org/installing/)     
-- `pip install mytimer==0.6`						
+- `pip install mytimer==0.7`						
 
 
 ## Usage
 
 ⚠️ You can use `mytimer` or `python -m mytimer` to run this program
 
 ### Version
@@ -168,14 +168,23 @@
 
 ⚠️ This mode may not be supported on all systems
 
 ```console
 mytimer --minute=7 --second=30 --countdown --alarm
 ```
 
+### Tone
+
+⚠️ The default tone is `1`
+
+```console
+mytimer --minute=7 --second=30 --countdown --alarm --tone=2
+```
+* [Tones List](https://github.com/sepandhaghighi/mytimer/blob/main/TONES.md)
+
 ### Face
 
 
 ```console
 mytimer --minute=7 --second=30 --face=3
 ```
 * [Faces List](https://github.com/sepandhaghighi/mytimer/blob/main/FACES.md)
@@ -259,14 +268,26 @@
 # Changelog
 All notable changes to this project will be documented in this file.
 
 The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
 and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).
 
 ## [Unreleased]
+## [0.7] - 2023-07-23
+### Added
+- `--tone` argument
+- `TONES.md`
+- 9 new tones
+### Changed
+- Test system modified
+- `input_check` decorator renamed to `input_handler`
+- `countup_timer` function inputs modified
+- `countdown_timer` function inputs modified
+- `PROGRAMS.md` updated
+- `FACES.md` updated
 ## [0.6] - 2023-07-04
 ### Added
 - `--program` argument
 - `PROGRAMS.md`
 - `run_timer` function
 ### Changed
 - Inputs type changed to `int`
@@ -304,15 +325,16 @@
 - `countup_timer` function modified
 ## [0.1] - 2022-10-18
 ### Added
 - Countdown mode
 - Count-up mode
 - Alarm
 
-[Unreleased]: https://github.com/sepandhaghighi/mytimer/compare/v0.6...dev
+[Unreleased]: https://github.com/sepandhaghighi/mytimer/compare/v0.7...dev
+[0.7]: https://github.com/sepandhaghighi/mytimer/compare/v0.6...v0.7
 [0.6]: https://github.com/sepandhaghighi/mytimer/compare/v0.5...v0.6
 [0.5]: https://github.com/sepandhaghighi/mytimer/compare/v0.4...v0.5
 [0.4]: https://github.com/sepandhaghighi/mytimer/compare/v0.3...v0.4
 [0.3]: https://github.com/sepandhaghighi/mytimer/compare/v0.2...v0.3
 [0.2]: https://github.com/sepandhaghighi/mytimer/compare/v0.1...v0.2
 [0.1]: https://github.com/sepandhaghighi/mytimer/compare/daa2be6...v0.1
```

#### html2text {}

```diff
@@ -1,10 +1,10 @@
-Metadata-Version: 2.1 Name: mytimer Version: 0.6 Summary: Simple Timer for Your
+Metadata-Version: 2.1 Name: mytimer Version: 0.7 Summary: Simple Timer for Your
 Terminal Home-page: https://github.com/sepandhaghighi/mytimer Download-URL:
-https://github.com/sepandhaghighi/mytimer/tarball/v0.6 Author: Sepand Haghighi
+https://github.com/sepandhaghighi/mytimer/tarball/v0.7 Author: Sepand Haghighi
 Author-email: sepand@pyrgg.ir License: MIT Project-URL: Source, https://
 github.com/sepandhaghighi/mytimer Keywords: python3 python timer terminal
 stopwatch Classifier: Development Status :: 4 - Beta Classifier: Natural
 Language :: English Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent Classifier: Programming Language
 :: Python :: 3.5 Classifier: Programming Language :: Python :: 3.6 Classifier:
 Programming Language :: Python :: 3.7 Classifier: Programming Language ::
@@ -48,31 +48,34 @@
 Branch                        main                                 dev
        [https://github.com/sepandhaghighi/ [https://github.com/sepandhaghighi/
    CI         mytimer/workflows/CI/               mytimer/workflows/CI/
              badge.svg?branch=main]               badge.svg?branch=dev]
                           [https://app.codacy.com/project/
 Code Quality [CodeFactor]           badge/Grade/            [codebeat_badge]
                           1bf28500431a498998ac79891cd79cda]
-## Installation ### Source Code - Download [Version 0.6](https://github.com/
-sepandhaghighi/mytimer/archive/v0.6.zip) or [Latest Source ](https://
+## Installation ### Source Code - Download [Version 0.7](https://github.com/
+sepandhaghighi/mytimer/archive/v0.7.zip) or [Latest Source ](https://
 github.com/sepandhaghighi/mytimer/archive/dev.zip) - `pip install .` ### PyPI -
 Check [Python Packaging User Guide](https://packaging.python.org/installing/) -
-`pip install mytimer==0.6` ## Usage â ï¸ You can use `mytimer` or `python -
+`pip install mytimer==0.7` ## Usage â ï¸ You can use `mytimer` or `python -
 m mytimer` to run this program ### Version ```console mytimer --version ``` ###
 Basic â ï¸ Press `Ctrl + C` to exit ```console mytimer ``` ### Time Limit
 ```console mytimer --minute=7 --second=30 ``` ```console mytimer --hour=2 --
 minute=20 ``` ### Timer Mode â ï¸ The default mode is `count-up` ```console
 mytimer --minute=7 --second=30 --countdown ``` ```console mytimer --minute=7 --
 second=30 --countup ``` ### Alarm â ï¸ This mode may not be supported on all
 systems ```console mytimer --minute=7 --second=30 --countdown --alarm ``` ###
-Face ```console mytimer --minute=7 --second=30 --face=3 ``` * [Faces List]
-(https://github.com/sepandhaghighi/mytimer/blob/main/FACES.md) ### Program
-```console mytimer --program=black-tea ``` * [Programs List](https://
-github.com/sepandhaghighi/mytimer/blob/main/PROGRAMS.md) ### Message ```console
-mytimer --minute=7 --second=30 --message="Test message" ```
+Tone â ï¸ The default tone is `1` ```console mytimer --minute=7 --second=30 -
+-countdown --alarm --tone=2 ``` * [Tones List](https://github.com/
+sepandhaghighi/mytimer/blob/main/TONES.md) ### Face ```console mytimer --
+minute=7 --second=30 --face=3 ``` * [Faces List](https://github.com/
+sepandhaghighi/mytimer/blob/main/FACES.md) ### Program ```console mytimer --
+program=black-tea ``` * [Programs List](https://github.com/sepandhaghighi/
+mytimer/blob/main/PROGRAMS.md) ### Message ```console mytimer --minute=7 --
+second=30 --message="Test message" ```
    [https://github.com/sepandhaghighi/mytimer/raw/main/otherfiles/help.gif]
                                  Screen Record
 ## Issues & Bug Reports Just fill an issue and describe it. We'll check it
 ASAP! - Please complete the issue template ## References
      1- Mixkit_Free_Alarm_Sound_Effects
      2- Online_Timer
      3- Media_College
@@ -103,27 +106,32 @@
 *** Zilliqa ***
 zil1knmz8zj88cf0exr2ry7nav9elehxfcgqu3c5e5
 *** Coffeete ***
 [http://www.coffeete.ir/images/buttons/lemonchiffon.png] # Changelog All
 notable changes to this project will be documented in this file. The format is
 based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) and this
 project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).
-## [Unreleased] ## [0.6] - 2023-07-04 ### Added - `--program` argument -
+## [Unreleased] ## [0.7] - 2023-07-23 ### Added - `--tone` argument -
+`TONES.md` - 9 new tones ### Changed - Test system modified - `input_check`
+decorator renamed to `input_handler` - `countup_timer` function inputs modified
+- `countdown_timer` function inputs modified - `PROGRAMS.md` updated -
+`FACES.md` updated ## [0.6] - 2023-07-04 ### Added - `--program` argument -
 `PROGRAMS.md` - `run_timer` function ### Changed - Inputs type changed to `int`
 - `README.md` updated - `WRONG_INPUT_ERROR` renamed to `INPUT_ERROR_MESSAGE` -
 Alarm tone changed ## [0.5] - 2023-05-25 ### Added - 5 new faces - `--message`
 argument ### Changed - `play_sound` function modified - `playsound` removed
 from `requirements.txt` - `README.md` updated ## [0.4] - 2023-02-10 ### Added -
 4 new faces - Infinite timer mode ### Changed - `README.md` updated -
 Parameters moved to `params.py` ## [0.3] - 2022-11-25 ### Added - `--face`
 argument - `FACES.md` ### Changed - `README.md` updated - Minimum `art` library
 version changed from `1.8` to `2.9` ## [0.2] - 2022-11-03 ### Added - `--
 version` flag ### Changed - Test system modified - `countdown_timer` function
 modified - `countup_timer` function modified ## [0.1] - 2022-10-18 ### Added -
 Countdown mode - Count-up mode - Alarm [Unreleased]: https://github.com/
-sepandhaghighi/mytimer/compare/v0.6...dev [0.6]: https://github.com/
+sepandhaghighi/mytimer/compare/v0.7...dev [0.7]: https://github.com/
+sepandhaghighi/mytimer/compare/v0.6...v0.7 [0.6]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.5...v0.6 [0.5]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.4...v0.5 [0.4]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.3...v0.4 [0.3]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.2...v0.3 [0.2]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.1...v0.2 [0.1]: https://github.com/
 sepandhaghighi/mytimer/compare/daa2be6...v0.1
```

### Comparing `mytimer-0.6/PROGRAMS.md` & `mytimer-0.7/PROGRAMS.md`

 * *Files 22% similar despite different names*

```diff
@@ -1,78 +1,92 @@
 # Programs List
 
 ⚠️ By default, the **alarm** is **active** for all programs
 
 <table>
 	<tr align="center">
-		<td><b>Title</b></td>
-		<td><b>Code</b></td>
-		<td><b>Time</b></td>
+		<th>Title</th>
+		<th>Code</th>
+		<th>Duration</th>
+		<th>Version</th>
 	</tr>
 	<tr align="center">
 		<td>Poached egg</td>
 		<td><code>poached-egg</code></td>
-		<td>1.5 mins</td>
+		<td>01:30</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Boiled egg</td>
 		<td><code>boiled-egg</code></td>
-		<td>3 mins</td>
+		<td>03:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Soft-boiled egg</td>
 		<td><code>soft-boiled-egg</code></td>
-		<td>5 mins</td>
+		<td>05:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Hard-boiled egg</td>
 		<td><code>hard-boiled-egg</code></td>
-		<td>10 mins</td>
+		<td>10:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Pasta</td>
 		<td><code>pasta</code></td>
-		<td>8 mins</td>
+		<td>08:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Quick cooking rice</td>
 		<td><code>quick-rice</code></td>
-		<td>10 mins</td>
+		<td>10:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Japanese green tea</td>
 		<td><code>japanese-green-tea</code></td>
-		<td>2 mins</td>
+		<td>02:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Tea bag</td>
 		<td><code>tea-bag</code></td>
-		<td>2 mins</td>
+		<td>02:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Chinese green tea</td>
 		<td><code>chinese-green-tea</code></td>
-		<td>5 mins</td>
+		<td>05:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Black tea</td>
 		<td><code>black-tea</code></td>
-		<td>5 mins</td>
+		<td>05:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Oolong tea</td>
 		<td><code>oolong-tea</code></td>
-		<td>5 mins</td>
+		<td>05:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>Fruit tea</td>
 		<td><code>fruit-tea</code></td>
-		<td>8 mins</td>
+		<td>08:00</td>
+		<td>>=0.6</td>
 	</tr>
 	<tr align="center">
 		<td>White tea</td>
 		<td><code>white-tea</code></td>
-		<td>10 mins</td>
+		<td>10:00</td>
+		<td>>=0.6</td>
 	</tr>
 </table>
```

#### html2text {}

```diff
@@ -1,15 +1,15 @@
 # Programs List â ï¸ By default, the **alarm** is **active** for all programs
-         Title               Code        Time
-     Poached egg        poached-egg   1.5 mins
-      Boiled egg         boiled-egg    3 mins
-  Soft-boiled egg    soft-boiled-egg   5 mins
-  Hard-boiled egg    hard-boiled-egg  10 mins
-         Pasta              pasta      8 mins
-Quick cooking rice       quick-rice   10 mins
-Japanese green tea japanese-green-tea  2 mins
-        Tea bag            tea-bag     2 mins
-Chinese green tea  chinese-green-tea   5 mins
-      Black tea          black-tea     5 mins
-      Oolong tea         oolong-tea    5 mins
-      Fruit tea          fruit-tea     8 mins
-      White tea          white-tea    10 mins
+         Title               Code     Duration Version
+     Poached egg        poached-egg     01:30   >=0.6
+      Boiled egg         boiled-egg     03:00   >=0.6
+  Soft-boiled egg    soft-boiled-egg    05:00   >=0.6
+  Hard-boiled egg    hard-boiled-egg    10:00   >=0.6
+         Pasta              pasta       08:00   >=0.6
+Quick cooking rice       quick-rice     10:00   >=0.6
+Japanese green tea japanese-green-tea   02:00   >=0.6
+        Tea bag            tea-bag      02:00   >=0.6
+Chinese green tea  chinese-green-tea    05:00   >=0.6
+      Black tea          black-tea      05:00   >=0.6
+      Oolong tea         oolong-tea     05:00   >=0.6
+      Fruit tea          fruit-tea      08:00   >=0.6
+      White tea          white-tea      10:00   >=0.6
```

### Comparing `mytimer-0.6/README.md` & `mytimer-0.7/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -77,21 +77,21 @@
 	</tr>
 </table>
 
 
 ## Installation		
 
 ### Source Code
-- Download [Version 0.6](https://github.com/sepandhaghighi/mytimer/archive/v0.6.zip) or [Latest Source ](https://github.com/sepandhaghighi/mytimer/archive/dev.zip)
+- Download [Version 0.7](https://github.com/sepandhaghighi/mytimer/archive/v0.7.zip) or [Latest Source ](https://github.com/sepandhaghighi/mytimer/archive/dev.zip)
 - `pip install .`				
 
 ### PyPI
 
 - Check [Python Packaging User Guide](https://packaging.python.org/installing/)     
-- `pip install mytimer==0.6`						
+- `pip install mytimer==0.7`						
 
 
 ## Usage
 
 ⚠️ You can use `mytimer` or `python -m mytimer` to run this program
 
 ### Version
@@ -134,14 +134,23 @@
 
 ⚠️ This mode may not be supported on all systems
 
 ```console
 mytimer --minute=7 --second=30 --countdown --alarm
 ```
 
+### Tone
+
+⚠️ The default tone is `1`
+
+```console
+mytimer --minute=7 --second=30 --countdown --alarm --tone=2
+```
+* [Tones List](https://github.com/sepandhaghighi/mytimer/blob/main/TONES.md)
+
 ### Face
 
 
 ```console
 mytimer --minute=7 --second=30 --face=3
 ```
 * [Faces List](https://github.com/sepandhaghighi/mytimer/blob/main/FACES.md)
```

#### html2text {}

```diff
@@ -30,31 +30,34 @@
 Branch                        main                                 dev
        [https://github.com/sepandhaghighi/ [https://github.com/sepandhaghighi/
    CI         mytimer/workflows/CI/               mytimer/workflows/CI/
              badge.svg?branch=main]               badge.svg?branch=dev]
                           [https://app.codacy.com/project/
 Code Quality [CodeFactor]           badge/Grade/            [codebeat_badge]
                           1bf28500431a498998ac79891cd79cda]
-## Installation ### Source Code - Download [Version 0.6](https://github.com/
-sepandhaghighi/mytimer/archive/v0.6.zip) or [Latest Source ](https://
+## Installation ### Source Code - Download [Version 0.7](https://github.com/
+sepandhaghighi/mytimer/archive/v0.7.zip) or [Latest Source ](https://
 github.com/sepandhaghighi/mytimer/archive/dev.zip) - `pip install .` ### PyPI -
 Check [Python Packaging User Guide](https://packaging.python.org/installing/) -
-`pip install mytimer==0.6` ## Usage â ï¸ You can use `mytimer` or `python -
+`pip install mytimer==0.7` ## Usage â ï¸ You can use `mytimer` or `python -
 m mytimer` to run this program ### Version ```console mytimer --version ``` ###
 Basic â ï¸ Press `Ctrl + C` to exit ```console mytimer ``` ### Time Limit
 ```console mytimer --minute=7 --second=30 ``` ```console mytimer --hour=2 --
 minute=20 ``` ### Timer Mode â ï¸ The default mode is `count-up` ```console
 mytimer --minute=7 --second=30 --countdown ``` ```console mytimer --minute=7 --
 second=30 --countup ``` ### Alarm â ï¸ This mode may not be supported on all
 systems ```console mytimer --minute=7 --second=30 --countdown --alarm ``` ###
-Face ```console mytimer --minute=7 --second=30 --face=3 ``` * [Faces List]
-(https://github.com/sepandhaghighi/mytimer/blob/main/FACES.md) ### Program
-```console mytimer --program=black-tea ``` * [Programs List](https://
-github.com/sepandhaghighi/mytimer/blob/main/PROGRAMS.md) ### Message ```console
-mytimer --minute=7 --second=30 --message="Test message" ```
+Tone â ï¸ The default tone is `1` ```console mytimer --minute=7 --second=30 -
+-countdown --alarm --tone=2 ``` * [Tones List](https://github.com/
+sepandhaghighi/mytimer/blob/main/TONES.md) ### Face ```console mytimer --
+minute=7 --second=30 --face=3 ``` * [Faces List](https://github.com/
+sepandhaghighi/mytimer/blob/main/FACES.md) ### Program ```console mytimer --
+program=black-tea ``` * [Programs List](https://github.com/sepandhaghighi/
+mytimer/blob/main/PROGRAMS.md) ### Message ```console mytimer --minute=7 --
+second=30 --message="Test message" ```
    [https://github.com/sepandhaghighi/mytimer/raw/main/otherfiles/help.gif]
                                  Screen Record
 ## Issues & Bug Reports Just fill an issue and describe it. We'll check it
 ASAP! - Please complete the issue template ## References
      1- Mixkit_Free_Alarm_Sound_Effects
      2- Online_Timer
      3- Media_College
```

### Comparing `mytimer-0.6/mytimer/__main__.py` & `mytimer-0.7/mytimer/__main__.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # -*- coding: utf-8 -*-
 """mytimer main."""
-from mytimer.params import FACES_MAP, PROGRAMS_MAP
+from mytimer.params import FACES_MAP, PROGRAMS_MAP, TONES_MAP
 from mytimer.functions import run_timer
 import argparse
 
 
 def main():
     """
     CLI main function.
@@ -19,14 +19,20 @@
     parser.add_argument(
         '--face',
         help='face',
         type=int,
         choices=sorted(
             FACES_MAP.keys()))
     parser.add_argument(
+        '--tone',
+        help='alarm tone',
+        type=int,
+        choices=sorted(
+            TONES_MAP.keys()))
+    parser.add_argument(
         '--program',
         help='program',
         type=str,
         choices=sorted(
             PROGRAMS_MAP.keys()))
     parser.add_argument(
         '--countdown',
```

### Comparing `mytimer-0.6/mytimer/functions.py` & `mytimer-0.7/mytimer/functions.py`

 * *Files 11% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 """mytimer functions."""
 import os
 import sys
 import subprocess
 import time
 from mytimer.params import INPUT_ERROR_MESSAGE, SOUND_ERROR_MESSAGE
 from mytimer.params import INPUT_EXAMPLE, TIME_ELEMENTS, MESSAGE_TEMPLATE
-from mytimer.params import FACES_MAP, PROGRAMS_MAP
+from mytimer.params import FACES_MAP, PROGRAMS_MAP, TONES_MAP
 from mytimer.params import MY_TIMER_VERSION
 from art import tprint
 
 
 def check_null_time(args):
     """
     Check that all time elements are null or not.
@@ -35,14 +35,15 @@
     """
     params = {
         "minute": 0,
         "hour": 0,
         "second": 0,
         "alarm": 0,
         "face": 1,
+        "tone": 1,
         "message": ""}
     if args.program:
         params = PROGRAMS_MAP[args.program]
     for item in params:
         if getattr(args, item) is not None:
             if item not in TIME_ELEMENTS:
                 params[item] = getattr(args, item)
@@ -51,53 +52,63 @@
                     params[item] = getattr(args, item)
     if not args.countdown:
         if check_null_time(args) and not args.program:
             params["hour"] = 100000000
     return params
 
 
-def input_check(func):
+def input_handler(func):
     """
-    Input check decorator for timer functions.
+    Input handler decorator for timer functions.
 
     :param func: input function
     :type func: function
     :return: inner function
     """
-    def inner_function(hour, minute, second, alarm, face, message):
+    def inner_function(
+            hour,
+            minute,
+            second,
+            alarm,
+            face,
+            message,
+            tone):
         """
         Inner function.
 
         :param hour: hour
         :type hour: int
         :param minute: minute
         :type minute: int
         :param second: second
         :type second: int
         :param alarm: alarm flag
         :type alarm: bool
-        :param face: face number
+        :param face: face index
         :type face: int
         :param message: message
         :type message: str
+        :param tone: tone index
+        :type tone: int
         :return: None
         """
         message = message.strip()
         if len(message) > 0:
             message = MESSAGE_TEMPLATE.format(message)
-        font = FACES_MAP[face]
+        face = FACES_MAP[face]
+        tone = TONES_MAP[tone]
         items_list = [hour, minute, second]
         if sum(items_list) != 0 and all(map(lambda x: x >= 0, items_list)):
             if second >= 60:
                 minute += second // 60
                 second %= 60
             if minute >= 60:
                 hour += minute // 60
                 minute %= 60
-            func(hour, minute, second, alarm, font, message)
+            func(hour, minute, second, alarm, face, message, tone)
         else:
             print(INPUT_ERROR_MESSAGE)
             print(INPUT_EXAMPLE)
     return inner_function
 
 
 def clear_screen():
@@ -151,106 +162,118 @@
                                       stderr=subprocess.PIPE,
                                       stdin=subprocess.PIPE,
                                       stdout=subprocess.PIPE)
     except Exception:
         print(SOUND_ERROR_MESSAGE)
 
 
-@input_check
-def countup_timer(hour, minute, second, alarm, font=FACES_MAP[1], message=""):
+@input_handler
+def countup_timer(
+        hour,
+        minute,
+        second,
+        alarm,
+        face=FACES_MAP[1],
+        message="",
+        tone=TONES_MAP[1]):
     """
     Count-up timer function.
 
     :param hour: hour
     :type hour: int
     :param minute: minute
     :type minute: int
     :param second: second
     :type second: int
     :param alarm: alarm flag
     :type alarm: bool
-    :param font: font name
-    :type font: str
+    :param face: face name
+    :type face: str
     :param message: message
     :type message: str
+    :param tone: tone file name
+    :type tone: str
     :return: None
     """
     timer_second = 0
     timer_minute = 0
     timer_hour = 0
     while True:
         start = time.perf_counter()
         clear_screen()
         print('\n' * 5)
         tprint(
             '\t\t\t\t  %d : %d : %d ' %
             (timer_hour,
              timer_minute,
              timer_second),
-            font=font)
+            font=face)
         print(message)
         if timer_hour == hour and timer_minute == minute and timer_second == second:
             print("End!")
             if alarm:
-                play_sound(get_sound_path("1.wav"))
+                play_sound(get_sound_path(tone))
             break
         timer_second += 1
         if timer_second == 60:
             timer_second = 0
             timer_minute += 1
         if timer_minute == 60:
             timer_minute = 0
             timer_hour += 1
         end = time.perf_counter()
         time.sleep(max(0, 1 - (end - start)))
 
 
-@input_check
+@input_handler
 def countdown_timer(
         hour,
         minute,
         second,
         alarm,
-        font=FACES_MAP[1],
-        message=""):
+        face=FACES_MAP[1],
+        message="",
+        tone=TONES_MAP[1]):
     """
     Countdown timer function.
 
     :param hour: hour
     :type hour: int
     :param minute: minute
     :type minute: int
     :param second: second
     :type second: int
     :param alarm: alarm flag
     :type alarm: bool
-    :param font: font name
-    :type font: str
+    :param face: face name
+    :type face: str
     :param message: message
     :type message: str
+    :param tone: tone file name
+    :type tone: str
     :return: None
     """
     while True:
         start = time.perf_counter()
         clear_screen()
         print('\n' * 5)
         tprint('\t\t\t\t  %d : %d : %d ' %
-               (hour, minute, second), font=font)
+               (hour, minute, second), font=face)
         print(message)
         second -= 1
         if second == -1:
             second = 59
             minute -= 1
         if minute == -1:
             minute = 59
             hour -= 1
         if hour == -1:
             print("End!")
             if alarm:
-                play_sound(get_sound_path("1.wav"))
+                play_sound(get_sound_path(tone))
             break
         end = time.perf_counter()
         time.sleep(max(0, 1 - (end - start)))
 
 
 def run_timer(args):
     """
```

### Comparing `mytimer-0.6/mytimer/params.py` & `mytimer-0.7/mytimer/params.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,16 +1,30 @@
 # -*- coding: utf-8 -*-
 """mytimer params."""
 
-MY_TIMER_VERSION = "0.6"
+MY_TIMER_VERSION = "0.7"
 INPUT_ERROR_MESSAGE = "[Error] Wrong input"
 SOUND_ERROR_MESSAGE = "[Error] Unable to play sound"
 INPUT_EXAMPLE = "Example: python -m mytimer --hour=1 --minute=1 --second=1"
 TIME_ELEMENTS = ["minute", "second", "hour"]
 MESSAGE_TEMPLATE = "Message: {0}"
+
+TONES_MAP = {
+    1: '1.wav',
+    2: '2.wav',
+    3: '3.wav',
+    4: '4.wav',
+    5: '5.wav',
+    6: '6.wav',
+    7: '7.wav',
+    8: '8.wav',
+    9: '9.wav',
+    10: '10.wav',
+    11: '11.wav'}
+
 FACES_MAP = {
     1: 'bulbhead',
     2: 'soft',
     3: '4max',
     4: '5x7',
     5: 'charact4',
     6: 'o8',
@@ -33,96 +47,108 @@
 PROGRAMS_MAP = {
     "poached-egg": {
         "hour": 0,
         "minute": 1,
         "second": 30,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Poached egg (1.5 mins)"},
     "boiled-egg": {
         "hour": 0,
         "minute": 3,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Boiled egg (3 mins)"},
     "soft-boiled-egg": {
         "hour": 0,
         "minute": 5,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Soft-boiled egg (5 mins)"},
     "hard-boiled-egg": {
         "hour": 0,
         "minute": 10,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Hard-boiled egg (10 mins)"},
     "pasta": {
         "hour": 0,
         "minute": 8,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Pasta (8 mins)"},
     "quick-rice": {
         "hour": 0,
         "minute": 10,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Quick cooking rice (10 mins)"},
     "japanese-green-tea": {
         "hour": 0,
         "minute": 2,
         "second": 0,
         "alarm": 1,
         "face": 1,
         "message": "Japanese green tea (2 mins)"},
     "tea-bag": {
         "hour": 0,
         "minute": 2,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Tea bag (2 mins)"},
     "chinese-green-tea": {
         "hour": 0,
         "minute": 5,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Chinese green tea (5 mins)"},
     "black-tea": {
         "hour": 0,
         "minute": 5,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Black tea (5 mins)"},
     "oolong-tea": {
         "hour": 0,
         "minute": 5,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Oolong tea (5 mins)"},
     "fruit-tea": {
         "hour": 0,
         "minute": 8,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "Fruit tea (8 mins)"},
     "white-tea": {
         "hour": 0,
         "minute": 10,
         "second": 0,
         "alarm": 1,
         "face": 1,
+        "tone": 1,
         "message": "White tea (10 mins)"},
 
 
 
 }
```

### Comparing `mytimer-0.6/mytimer/sounds/1.wav` & `mytimer-0.7/mytimer/sounds/1.wav`

 * *Files identical despite different names*

### Comparing `mytimer-0.6/mytimer/sounds/2.wav` & `mytimer-0.7/mytimer/sounds/2.wav`

 * *Files identical despite different names*

### Comparing `mytimer-0.6/mytimer.egg-info/PKG-INFO` & `mytimer-0.7/mytimer.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: mytimer
-Version: 0.6
+Version: 0.7
 Summary: Simple Timer for Your Terminal
 Home-page: https://github.com/sepandhaghighi/mytimer
-Download-URL: https://github.com/sepandhaghighi/mytimer/tarball/v0.6
+Download-URL: https://github.com/sepandhaghighi/mytimer/tarball/v0.7
 Author: Sepand Haghighi
 Author-email: sepand@pyrgg.ir
 License: MIT
 Project-URL: Source, https://github.com/sepandhaghighi/mytimer
 Keywords: python3 python timer terminal stopwatch
 Classifier: Development Status :: 4 - Beta
 Classifier: Natural Language :: English
@@ -111,21 +111,21 @@
 	</tr>
 </table>
 
 
 ## Installation		
 
 ### Source Code
-- Download [Version 0.6](https://github.com/sepandhaghighi/mytimer/archive/v0.6.zip) or [Latest Source ](https://github.com/sepandhaghighi/mytimer/archive/dev.zip)
+- Download [Version 0.7](https://github.com/sepandhaghighi/mytimer/archive/v0.7.zip) or [Latest Source ](https://github.com/sepandhaghighi/mytimer/archive/dev.zip)
 - `pip install .`				
 
 ### PyPI
 
 - Check [Python Packaging User Guide](https://packaging.python.org/installing/)     
-- `pip install mytimer==0.6`						
+- `pip install mytimer==0.7`						
 
 
 ## Usage
 
 ⚠️ You can use `mytimer` or `python -m mytimer` to run this program
 
 ### Version
@@ -168,14 +168,23 @@
 
 ⚠️ This mode may not be supported on all systems
 
 ```console
 mytimer --minute=7 --second=30 --countdown --alarm
 ```
 
+### Tone
+
+⚠️ The default tone is `1`
+
+```console
+mytimer --minute=7 --second=30 --countdown --alarm --tone=2
+```
+* [Tones List](https://github.com/sepandhaghighi/mytimer/blob/main/TONES.md)
+
 ### Face
 
 
 ```console
 mytimer --minute=7 --second=30 --face=3
 ```
 * [Faces List](https://github.com/sepandhaghighi/mytimer/blob/main/FACES.md)
@@ -259,14 +268,26 @@
 # Changelog
 All notable changes to this project will be documented in this file.
 
 The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
 and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).
 
 ## [Unreleased]
+## [0.7] - 2023-07-23
+### Added
+- `--tone` argument
+- `TONES.md`
+- 9 new tones
+### Changed
+- Test system modified
+- `input_check` decorator renamed to `input_handler`
+- `countup_timer` function inputs modified
+- `countdown_timer` function inputs modified
+- `PROGRAMS.md` updated
+- `FACES.md` updated
 ## [0.6] - 2023-07-04
 ### Added
 - `--program` argument
 - `PROGRAMS.md`
 - `run_timer` function
 ### Changed
 - Inputs type changed to `int`
@@ -304,15 +325,16 @@
 - `countup_timer` function modified
 ## [0.1] - 2022-10-18
 ### Added
 - Countdown mode
 - Count-up mode
 - Alarm
 
-[Unreleased]: https://github.com/sepandhaghighi/mytimer/compare/v0.6...dev
+[Unreleased]: https://github.com/sepandhaghighi/mytimer/compare/v0.7...dev
+[0.7]: https://github.com/sepandhaghighi/mytimer/compare/v0.6...v0.7
 [0.6]: https://github.com/sepandhaghighi/mytimer/compare/v0.5...v0.6
 [0.5]: https://github.com/sepandhaghighi/mytimer/compare/v0.4...v0.5
 [0.4]: https://github.com/sepandhaghighi/mytimer/compare/v0.3...v0.4
 [0.3]: https://github.com/sepandhaghighi/mytimer/compare/v0.2...v0.3
 [0.2]: https://github.com/sepandhaghighi/mytimer/compare/v0.1...v0.2
 [0.1]: https://github.com/sepandhaghighi/mytimer/compare/daa2be6...v0.1
```

#### html2text {}

```diff
@@ -1,10 +1,10 @@
-Metadata-Version: 2.1 Name: mytimer Version: 0.6 Summary: Simple Timer for Your
+Metadata-Version: 2.1 Name: mytimer Version: 0.7 Summary: Simple Timer for Your
 Terminal Home-page: https://github.com/sepandhaghighi/mytimer Download-URL:
-https://github.com/sepandhaghighi/mytimer/tarball/v0.6 Author: Sepand Haghighi
+https://github.com/sepandhaghighi/mytimer/tarball/v0.7 Author: Sepand Haghighi
 Author-email: sepand@pyrgg.ir License: MIT Project-URL: Source, https://
 github.com/sepandhaghighi/mytimer Keywords: python3 python timer terminal
 stopwatch Classifier: Development Status :: 4 - Beta Classifier: Natural
 Language :: English Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent Classifier: Programming Language
 :: Python :: 3.5 Classifier: Programming Language :: Python :: 3.6 Classifier:
 Programming Language :: Python :: 3.7 Classifier: Programming Language ::
@@ -48,31 +48,34 @@
 Branch                        main                                 dev
        [https://github.com/sepandhaghighi/ [https://github.com/sepandhaghighi/
    CI         mytimer/workflows/CI/               mytimer/workflows/CI/
              badge.svg?branch=main]               badge.svg?branch=dev]
                           [https://app.codacy.com/project/
 Code Quality [CodeFactor]           badge/Grade/            [codebeat_badge]
                           1bf28500431a498998ac79891cd79cda]
-## Installation ### Source Code - Download [Version 0.6](https://github.com/
-sepandhaghighi/mytimer/archive/v0.6.zip) or [Latest Source ](https://
+## Installation ### Source Code - Download [Version 0.7](https://github.com/
+sepandhaghighi/mytimer/archive/v0.7.zip) or [Latest Source ](https://
 github.com/sepandhaghighi/mytimer/archive/dev.zip) - `pip install .` ### PyPI -
 Check [Python Packaging User Guide](https://packaging.python.org/installing/) -
-`pip install mytimer==0.6` ## Usage â ï¸ You can use `mytimer` or `python -
+`pip install mytimer==0.7` ## Usage â ï¸ You can use `mytimer` or `python -
 m mytimer` to run this program ### Version ```console mytimer --version ``` ###
 Basic â ï¸ Press `Ctrl + C` to exit ```console mytimer ``` ### Time Limit
 ```console mytimer --minute=7 --second=30 ``` ```console mytimer --hour=2 --
 minute=20 ``` ### Timer Mode â ï¸ The default mode is `count-up` ```console
 mytimer --minute=7 --second=30 --countdown ``` ```console mytimer --minute=7 --
 second=30 --countup ``` ### Alarm â ï¸ This mode may not be supported on all
 systems ```console mytimer --minute=7 --second=30 --countdown --alarm ``` ###
-Face ```console mytimer --minute=7 --second=30 --face=3 ``` * [Faces List]
-(https://github.com/sepandhaghighi/mytimer/blob/main/FACES.md) ### Program
-```console mytimer --program=black-tea ``` * [Programs List](https://
-github.com/sepandhaghighi/mytimer/blob/main/PROGRAMS.md) ### Message ```console
-mytimer --minute=7 --second=30 --message="Test message" ```
+Tone â ï¸ The default tone is `1` ```console mytimer --minute=7 --second=30 -
+-countdown --alarm --tone=2 ``` * [Tones List](https://github.com/
+sepandhaghighi/mytimer/blob/main/TONES.md) ### Face ```console mytimer --
+minute=7 --second=30 --face=3 ``` * [Faces List](https://github.com/
+sepandhaghighi/mytimer/blob/main/FACES.md) ### Program ```console mytimer --
+program=black-tea ``` * [Programs List](https://github.com/sepandhaghighi/
+mytimer/blob/main/PROGRAMS.md) ### Message ```console mytimer --minute=7 --
+second=30 --message="Test message" ```
    [https://github.com/sepandhaghighi/mytimer/raw/main/otherfiles/help.gif]
                                  Screen Record
 ## Issues & Bug Reports Just fill an issue and describe it. We'll check it
 ASAP! - Please complete the issue template ## References
      1- Mixkit_Free_Alarm_Sound_Effects
      2- Online_Timer
      3- Media_College
@@ -103,27 +106,32 @@
 *** Zilliqa ***
 zil1knmz8zj88cf0exr2ry7nav9elehxfcgqu3c5e5
 *** Coffeete ***
 [http://www.coffeete.ir/images/buttons/lemonchiffon.png] # Changelog All
 notable changes to this project will be documented in this file. The format is
 based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) and this
 project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).
-## [Unreleased] ## [0.6] - 2023-07-04 ### Added - `--program` argument -
+## [Unreleased] ## [0.7] - 2023-07-23 ### Added - `--tone` argument -
+`TONES.md` - 9 new tones ### Changed - Test system modified - `input_check`
+decorator renamed to `input_handler` - `countup_timer` function inputs modified
+- `countdown_timer` function inputs modified - `PROGRAMS.md` updated -
+`FACES.md` updated ## [0.6] - 2023-07-04 ### Added - `--program` argument -
 `PROGRAMS.md` - `run_timer` function ### Changed - Inputs type changed to `int`
 - `README.md` updated - `WRONG_INPUT_ERROR` renamed to `INPUT_ERROR_MESSAGE` -
 Alarm tone changed ## [0.5] - 2023-05-25 ### Added - 5 new faces - `--message`
 argument ### Changed - `play_sound` function modified - `playsound` removed
 from `requirements.txt` - `README.md` updated ## [0.4] - 2023-02-10 ### Added -
 4 new faces - Infinite timer mode ### Changed - `README.md` updated -
 Parameters moved to `params.py` ## [0.3] - 2022-11-25 ### Added - `--face`
 argument - `FACES.md` ### Changed - `README.md` updated - Minimum `art` library
 version changed from `1.8` to `2.9` ## [0.2] - 2022-11-03 ### Added - `--
 version` flag ### Changed - Test system modified - `countdown_timer` function
 modified - `countup_timer` function modified ## [0.1] - 2022-10-18 ### Added -
 Countdown mode - Count-up mode - Alarm [Unreleased]: https://github.com/
-sepandhaghighi/mytimer/compare/v0.6...dev [0.6]: https://github.com/
+sepandhaghighi/mytimer/compare/v0.7...dev [0.7]: https://github.com/
+sepandhaghighi/mytimer/compare/v0.6...v0.7 [0.6]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.5...v0.6 [0.5]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.4...v0.5 [0.4]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.3...v0.4 [0.3]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.2...v0.3 [0.2]: https://github.com/
 sepandhaghighi/mytimer/compare/v0.1...v0.2 [0.1]: https://github.com/
 sepandhaghighi/mytimer/compare/daa2be6...v0.1
```

### Comparing `mytimer-0.6/setup.py` & `mytimer-0.7/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -25,23 +25,23 @@
     except Exception:
         return '''Simple Timer for Your Terminal'''
 
 
 setup(
     name='mytimer',
     packages=['mytimer'],
-    version='0.6',
+    version='0.7',
     description='Simple Timer for Your Terminal',
     long_description=read_description(),
     long_description_content_type='text/markdown',
     include_package_data=True,
     author='Sepand Haghighi',
     author_email='sepand@pyrgg.ir',
     url='https://github.com/sepandhaghighi/mytimer',
-    download_url='https://github.com/sepandhaghighi/mytimer/tarball/v0.6',
+    download_url='https://github.com/sepandhaghighi/mytimer/tarball/v0.7',
     keywords="python3 python timer terminal stopwatch",
     project_urls={
         'Source': 'https://github.com/sepandhaghighi/mytimer'
     },
     install_requires=get_requires(),
     python_requires='>=3.5',
     classifiers=[
```

