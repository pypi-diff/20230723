# Comparing `tmp/httprunner-4.3.0.tar.gz` & `tmp/httprunner-4.3.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "httprunner-4.3.0.tar", max compression
+gzip compressed data, was "httprunner-4.3.5.tar", max compression
```

## Comparing `httprunner-4.3.0.tar` & `httprunner-4.3.5.tar`

### file list

```diff
@@ -1,44 +1,43 @@
--rw-r--r--   0        0        0    11338 2022-04-27 14:15:23.886459 httprunner-4.3.0/LICENSE
--rw-r--r--   0        0        0     9721 2022-07-26 07:32:00.658151 httprunner-4.3.0/README.md
--rw-r--r--   0        0        0    22729 2022-10-21 13:51:37.172816 httprunner-4.3.0/docs/CHANGELOG.md
--rw-r--r--   0        0        0     3666 2022-05-18 08:39:37.982597 httprunner-4.3.0/httprunner/README.md
--rw-r--r--   0        0        0      946 2022-10-21 13:44:38.370877 httprunner-4.3.0/httprunner/__init__.py
--rw-r--r--   0        0        0       72 2022-04-27 14:15:24.014817 httprunner-4.3.0/httprunner/__main__.py
--rw-r--r--   0        0        0       88 2022-04-27 14:15:24.015650 httprunner-4.3.0/httprunner/builtin/__init__.py
--rw-r--r--   0        0        0     3997 2022-05-18 08:39:37.983645 httprunner-4.3.0/httprunner/builtin/comparators.py
--rw-r--r--   0        0        0      854 2022-05-18 08:39:37.984812 httprunner-4.3.0/httprunner/builtin/functions.py
--rw-r--r--   0        0        0     4124 2022-06-17 14:56:04.255896 httprunner-4.3.0/httprunner/cli.py
--rw-r--r--   0        0        0     1822 2022-05-18 08:39:37.988606 httprunner-4.3.0/httprunner/cli_test.py
--rw-r--r--   0        0        0     8811 2022-06-17 11:28:35.389286 httprunner-4.3.0/httprunner/client.py
--rw-r--r--   0        0        0     2760 2022-05-18 08:39:37.991110 httprunner-4.3.0/httprunner/client_test.py
--rw-r--r--   0        0        0    11810 2022-06-27 13:38:12.011933 httprunner-4.3.0/httprunner/compat.py
--rw-r--r--   0        0        0     9681 2022-06-27 13:38:12.013226 httprunner-4.3.0/httprunner/compat_test.py
--rw-r--r--   0        0        0     3795 2022-07-26 01:44:30.035598 httprunner-4.3.0/httprunner/config.py
--rw-r--r--   0        0        0     2844 2022-10-11 03:09:07.677708 httprunner-4.3.0/httprunner/database/engine.py
--rw-r--r--   0        0        0     1221 2022-05-18 08:39:37.999221 httprunner-4.3.0/httprunner/exceptions.py
--rw-r--r--   0        0        0      114 2022-04-27 14:15:24.023026 httprunner-4.3.0/httprunner/ext/__init__.py
--rw-r--r--   0        0        0     4880 2022-06-27 13:38:12.014786 httprunner-4.3.0/httprunner/ext/uploader/__init__.py
--rw-r--r--   0        0        0    12599 2022-05-18 08:39:38.003298 httprunner-4.3.0/httprunner/loader.py
--rw-r--r--   0        0        0     4645 2022-05-18 08:39:38.005876 httprunner-4.3.0/httprunner/loader_test.py
--rw-r--r--   0        0        0    18796 2022-06-26 05:16:55.654323 httprunner-4.3.0/httprunner/make.py
--rw-r--r--   0        0        0     8140 2022-05-18 08:39:38.010954 httprunner-4.3.0/httprunner/make_test.py
--rw-r--r--   0        0        0     7462 2022-07-26 01:44:30.036918 httprunner-4.3.0/httprunner/models.py
--rw-r--r--   0        0        0    20735 2022-05-18 08:39:38.013630 httprunner-4.3.0/httprunner/parser.py
--rw-r--r--   0        0        0    22238 2022-05-18 08:39:38.014864 httprunner-4.3.0/httprunner/parser_test.py
--rw-r--r--   0        0        0    10003 2022-07-26 07:32:00.711608 httprunner-4.3.0/httprunner/response.py
--rw-r--r--   0        0        0     3015 2022-06-17 14:56:04.260121 httprunner-4.3.0/httprunner/response_test.py
--rw-r--r--   0        0        0     8190 2022-07-10 16:53:24.287674 httprunner-4.3.0/httprunner/runner.py
--rw-r--r--   0        0        0     1700 2022-07-26 01:44:30.038141 httprunner-4.3.0/httprunner/step.py
--rw-r--r--   0        0        0    16569 2022-07-26 01:44:30.039198 httprunner-4.3.0/httprunner/step_request.py
--rw-r--r--   0        0        0      705 2022-05-18 08:39:38.023594 httprunner-4.3.0/httprunner/step_request_test.py
--rw-r--r--   0        0        0    10644 2022-06-22 06:58:58.316143 httprunner-4.3.0/httprunner/step_sql_request.py
--rw-r--r--   0        0        0     3344 2022-06-22 06:58:58.318610 httprunner-4.3.0/httprunner/step_testcase.py
--rw-r--r--   0        0        0      953 2022-06-17 14:56:04.264911 httprunner-4.3.0/httprunner/step_testcase_test.py
--rw-r--r--   0        0        0    10090 2022-06-22 06:58:58.319376 httprunner-4.3.0/httprunner/step_thrift_request.py
--rw-r--r--   0        0        0    16600 2022-05-24 12:55:47.480818 httprunner-4.3.0/httprunner/thrift/data_convertor.py
--rw-r--r--   0        0        0     4073 2022-05-18 08:39:38.027671 httprunner-4.3.0/httprunner/thrift/thrift_client.py
--rw-r--r--   0        0        0     9592 2022-10-17 03:47:21.611576 httprunner-4.3.0/httprunner/utils.py
--rw-r--r--   0        0        0     6121 2022-05-18 08:39:38.029352 httprunner-4.3.0/httprunner/utils_test.py
--rw-r--r--   0        0        0     2473 2022-10-21 13:44:38.376507 httprunner-4.3.0/pyproject.toml
--rw-r--r--   0        0        0    11512 2022-10-21 14:25:16.748935 httprunner-4.3.0/setup.py
--rw-r--r--   0        0        0    11925 2022-10-21 14:25:16.750017 httprunner-4.3.0/PKG-INFO
+-rw-r--r--   0        0        0    11338 2022-04-27 14:15:23.886459 httprunner-4.3.5/LICENSE
+-rw-r--r--   0        0        0     9204 2023-05-31 13:28:55.893809 httprunner-4.3.5/README.md
+-rw-r--r--   0        0        0    26458 2023-07-23 06:51:32.079997 httprunner-4.3.5/docs/CHANGELOG.md
+-rw-r--r--   0        0        0     3666 2022-05-18 08:39:37.982597 httprunner-4.3.5/httprunner/README.md
+-rw-r--r--   0        0        0      946 2023-07-21 12:13:31.710437 httprunner-4.3.5/httprunner/__init__.py
+-rw-r--r--   0        0        0       72 2022-04-27 14:15:24.014817 httprunner-4.3.5/httprunner/__main__.py
+-rw-r--r--   0        0        0       88 2022-04-27 14:15:24.015650 httprunner-4.3.5/httprunner/builtin/__init__.py
+-rw-r--r--   0        0        0     3997 2022-05-18 08:39:37.983645 httprunner-4.3.5/httprunner/builtin/comparators.py
+-rw-r--r--   0        0        0      854 2022-05-18 08:39:37.984812 httprunner-4.3.5/httprunner/builtin/functions.py
+-rw-r--r--   0        0        0     4110 2023-07-21 03:16:12.793042 httprunner-4.3.5/httprunner/cli.py
+-rw-r--r--   0        0        0     1822 2022-05-18 08:39:37.988606 httprunner-4.3.5/httprunner/cli_test.py
+-rw-r--r--   0        0        0     8811 2022-06-17 11:28:35.389286 httprunner-4.3.5/httprunner/client.py
+-rw-r--r--   0        0        0     2808 2023-07-22 03:39:10.932006 httprunner-4.3.5/httprunner/client_test.py
+-rw-r--r--   0        0        0    11810 2022-06-27 13:38:12.011933 httprunner-4.3.5/httprunner/compat.py
+-rw-r--r--   0        0        0     9705 2023-07-21 15:41:12.569632 httprunner-4.3.5/httprunner/compat_test.py
+-rw-r--r--   0        0        0     3795 2022-07-26 01:44:30.035598 httprunner-4.3.5/httprunner/config.py
+-rw-r--r--   0        0        0     2844 2022-10-23 08:30:51.239575 httprunner-4.3.5/httprunner/database/engine.py
+-rw-r--r--   0        0        0     1221 2022-05-18 08:39:37.999221 httprunner-4.3.5/httprunner/exceptions.py
+-rw-r--r--   0        0        0      114 2022-04-27 14:15:24.023026 httprunner-4.3.5/httprunner/ext/__init__.py
+-rw-r--r--   0        0        0     4863 2023-07-21 14:58:11.302331 httprunner-4.3.5/httprunner/ext/uploader/__init__.py
+-rw-r--r--   0        0        0    12599 2022-05-18 08:39:38.003298 httprunner-4.3.5/httprunner/loader.py
+-rw-r--r--   0        0        0     4645 2022-05-18 08:39:38.005876 httprunner-4.3.5/httprunner/loader_test.py
+-rw-r--r--   0        0        0    18781 2023-07-21 03:16:49.165471 httprunner-4.3.5/httprunner/make.py
+-rw-r--r--   0        0        0     8140 2022-05-18 08:39:38.010954 httprunner-4.3.5/httprunner/make_test.py
+-rw-r--r--   0        0        0     7462 2022-07-26 01:44:30.036918 httprunner-4.3.5/httprunner/models.py
+-rw-r--r--   0        0        0    20735 2022-05-18 08:39:38.013630 httprunner-4.3.5/httprunner/parser.py
+-rw-r--r--   0        0        0    22238 2023-07-21 14:56:58.409633 httprunner-4.3.5/httprunner/parser_test.py
+-rw-r--r--   0        0        0    10003 2022-07-26 07:32:00.711608 httprunner-4.3.5/httprunner/response.py
+-rw-r--r--   0        0        0     3053 2023-07-21 15:41:20.586488 httprunner-4.3.5/httprunner/response_test.py
+-rw-r--r--   0        0        0     8246 2023-07-21 11:13:43.189186 httprunner-4.3.5/httprunner/runner.py
+-rw-r--r--   0        0        0     1700 2022-07-26 01:44:30.038141 httprunner-4.3.5/httprunner/step.py
+-rw-r--r--   0        0        0    16569 2022-07-26 01:44:30.039198 httprunner-4.3.5/httprunner/step_request.py
+-rw-r--r--   0        0        0      705 2022-05-18 08:39:38.023594 httprunner-4.3.5/httprunner/step_request_test.py
+-rw-r--r--   0        0        0    10644 2022-06-22 06:58:58.316143 httprunner-4.3.5/httprunner/step_sql_request.py
+-rw-r--r--   0        0        0     3344 2022-06-22 06:58:58.318610 httprunner-4.3.5/httprunner/step_testcase.py
+-rw-r--r--   0        0        0      953 2022-06-17 14:56:04.264911 httprunner-4.3.5/httprunner/step_testcase_test.py
+-rw-r--r--   0        0        0    10090 2022-06-22 06:58:58.319376 httprunner-4.3.5/httprunner/step_thrift_request.py
+-rw-r--r--   0        0        0    16600 2022-05-24 12:55:47.480818 httprunner-4.3.5/httprunner/thrift/data_convertor.py
+-rw-r--r--   0        0        0     4073 2022-05-18 08:39:38.027671 httprunner-4.3.5/httprunner/thrift/thrift_client.py
+-rw-r--r--   0        0        0     9957 2023-07-21 15:40:37.785781 httprunner-4.3.5/httprunner/utils.py
+-rw-r--r--   0        0        0     6339 2023-07-22 03:39:37.113540 httprunner-4.3.5/httprunner/utils_test.py
+-rw-r--r--   0        0        0     2492 2023-07-23 06:47:14.127646 httprunner-4.3.5/pyproject.toml
+-rw-r--r--   0        0        0    11505 1970-01-01 00:00:00.000000 httprunner-4.3.5/PKG-INFO
```

### Comparing `httprunner-4.3.0/LICENSE` & `httprunner-4.3.5/LICENSE`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/README.md` & `httprunner-4.3.5/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -76,19 +76,21 @@
 Github: https://github.com/httprunner/httprunner
 Copyright 2017 debugtalk
 
 Usage:
   hrp [command]
 
 Available Commands:
+  adb          simple utils for android device management
   boom         run load test with boomer
   build        build plugin for testing
-  completion   generate the autocompletion script for the specified shell
-  convert      convert to JSON/YAML/gotest/pytest testcases
+  completion   Generate the autocompletion script for the specified shell
+  convert      convert multiple source format to HttpRunner JSON/YAML/gotest/pytest cases
   help         Help about any command
+  ios          simple utils for ios device management
   pytest       run API test with pytest
   run          run API test with go engine
   startproject create a scaffold project
   wiki         visit https://httprunner.com
 
 Flags:
   -h, --help               help for hrp
@@ -103,38 +105,27 @@
 ## 用户案例
 
 <a href="https://httprunner.com/docs/cases/dji-ibg"><img src="https://httprunner.com/image/logo/dji.jpeg" title="大疆 - 基于 HttpRunner 构建完整的自动化测试体系" width="60"></a>
 <a href="https://httprunner.com/docs/cases/youmi"><img src="https://httprunner.com/image/logo/youmi.png" title="有米科技 - 基于 HttpRunner 建设自动化测试平台" width="60"></a>
 <a href="https://httprunner.com/docs/cases/umcare"><img src="https://httprunner.com/image/logo/umcare.png" title="通用环球医疗 - 使用 HttpRunner 实践接口自动化测试" width="100"></a>
 <a href="https://httprunner.com/docs/cases/mihoyo"><img src="https://httprunner.com/image/logo/miHoYo.png" title="米哈游 - 基于 HttpRunner 搭建接口自动化测试体系" width="100"></a>
 
-## 赞助商
-
-### 金牌赞助商
-
-[<img src="https://httprunner.com/image/hogwarts.jpeg" alt="霍格沃兹测试开发学社" width="400">](https://ceshiren.com/)
-
-> [霍格沃兹测试开发学社](http://qrcode.testing-studio.com/f?from=httprunner&url=https://ceshiren.com)是业界领先的测试开发技术高端教育品牌，隶属于[测吧（北京）科技有限公司](http://qrcode.testing-studio.com/f?from=httprunner&url=https://www.testing-studio.com) 。学院课程由一线大厂测试经理与资深测试开发专家参与研发，实战驱动。课程涵盖 web/app 自动化测试、接口测试、性能测试、安全测试、持续集成/持续交付/DevOps，测试左移&右移、精准测试、测试平台开发、测试管理等内容，帮助测试工程师实现测试开发技术转型。通过优秀的学社制度（奖学金、内推返学费、行业竞赛等多种方式）来实现学员、学社及用人企业的三方共赢。
 
-> [进入测试开发技术能力测评!](http://qrcode.testing-studio.com/f?from=httprunner&url=https://ceshiren.com/t/topic/14940)
-
-### 开源服务赞助商
+## 赞助商
 
-[<img src="https://httprunner.com/image/sentry-logo-black.svg" alt="Sentry" width="150">](https://sentry.io/_/open-source/)
+[<img src="https://testing-studio.com/img/icon.png" alt="霍格沃兹测试开发学社" width="500">](https://qrcode.testing-studio.com/f?from=HttpRunner&url=https://testing-studio.com/)
 
-HttpRunner is in Sentry Sponsored plan.
+> 霍格沃兹测试开发学社是中国软件测试开发高端教育品牌，产品由国内顶尖软件测试开发技术专家携手打造，为企业与个人提供专业的技能培训与咨询、测试工具与测试平台、测试外包与测试众包服务。领域涵盖 App/Web 自动化测试、接口自动化测试、性能测试、安全测试、持续交付/DevOps、测试左移、测试右移、精准测试、测试平台开发、测试管理等方向。-> [**联系我们**](http://qrcode.testing-studio.com/f?from=HttpRunner&url=https://ceshiren.com/t/topic/23745)
 
 ## Subscribe
 
 关注 HttpRunner 的微信公众号，第一时间获得最新资讯。
 
 <img src="https://httprunner.com/image/qrcode.png" alt="HttpRunner" width="400">
 
-如果你期望加入 HttpRunner 用户群，请看这里：[HttpRunner v4 用户交流群，它来啦！](https://httprunner.com/blog/join-chat-group)
-
 [HttpRunner]: https://github.com/httprunner/httprunner
 [boomer]: https://github.com/myzhan/boomer
 [locust]: https://github.com/locustio/locust
 [jmespath]: https://jmespath.org/
 [allure]: https://docs.qameta.io/allure/
 [HAR]: https://en.wikipedia.org/wiki/HAR_(file_format)
 [hashicorp plugin]: https://github.com/hashicorp/go-plugin
```

### Comparing `httprunner-4.3.0/docs/CHANGELOG.md` & `httprunner-4.3.5/docs/CHANGELOG.md`

 * *Files 12% similar despite different names*

```diff
@@ -1,16 +1,107 @@
 # Release History
 
-## v4.3.0 (2022-10-21)
+## v4.3.5 (2023-07-23)
+
+- refactor: send events to Google Analytics 4, replace GA v1
+- fix: failure unittests caused by httpbin.org, replace with docker service
+
+**go version**
+
+- fix #1603: ensure path suffix '/' exists
+
+**python version**
+
+- fix: upgrade pyyaml from 5.4.1 to 6.0.1, fix installing error
+- refactor: update httprunner dependencies
+
+## v4.3.4 (2023-06-01)
+
+**go version**
+
+- feat: add video crawler for feed and live
+- feat: cache screenshot ocr texts
+- feat: set testcase and request timeout in seconds
+- feat: catch interrupt signal
+- feat: add new exit code MobileUILaunchAppError/InterruptError/TimeoutError/MobileUIActivityNotMatchError/MobileUIPopupError/LoopActionNotFoundError
+- feat: find text with regex
+- feat: add UI ocr tags to summary
+- feat: check android device offline when running shell failed
+- feat: print hrp runner exit code when running finished
+- feat: add screen resolution and step start time in summary
+- refactor: replace OCR APIs with image APIs
+- refactor: FindText(s) returns OCRText(s)
+- refactor: merge ActionOption with DataOption
+- change: exit with AndroidShellExecError code for adb shell failure
+- change: request vedem ocr with uploading image
+- change: remove ping/dns sub commands
+
+## v4.3.3 (2023-04-19)
+
+**go version**
+
+- feat: add `sleep_random` to sleep random seconds, with weight for multiple time ranges
+- feat: input text with adb
+- feat: add adb `screencap` sub command
+- feat: add `AssertAppInForeground` to check if the given package is in foreground
+- feat: check if app is in foreground when step failed
+- feat: add validator AssertAppInForeground and AssertAppNotInForeground
+- feat: save screenshots of all steps including ocr and cv recognition process data
+- fix: adb driver for TapFloat
+- fix: stop logcat only when enabled
+- fix: do not fail case when kill logcat error
+- fix: take screenshot after each step
+- fix: screencap compatibility for shell v1 and v2 protocol
+- fix: display parsed url in html report
+- fix: fast fail not closing the websocket connection
+- fix #1467: failed to parse parameters with plugin functions
+- fix #1549: avoid duplicate creating plugins
+- fix #1547: generate html report failed for referenced testcases
+- fix: setup hooks compatible with v3
+
+## v4.3.2 (2022-12-26)
+
+**go version**
+
+- feat: run Android UI automation with adb by default, add `uixt.WithUIA2(true)` option to use uiautomator2
+- refactor: remove unused APIs in UI automation
+- refactor: convert cases by specifying from/to format
+- change: remove traceroute/curl sub commands
+
+## v4.3.1 (2022-12-22)
+
+**go version**
+
+- feat: add option WithScreenShot
+- feat: run xctest before start ios automation
+- feat: run step with specified loop times
+- feat: add options for FindTexts
+- feat: capture pcap file for iOS, including CLI `hrp ios pcap` and option `uixt.WithIOSPcapOptions(...)`
+- feat: add performance monitor for iOS, including CLI `hrp ios perf` and options `uixt.WithIOSPerfOptions(...)`
+- refactor: move all UI APIs to uixt pkg
+- docs: add examples for UI APIs
+
+## v4.3.0 (2022-10-27)
+
+Release hrp sub package `uixt` to support iOS/Android UI automation testing 🎉
+
+- feat: support iOS UI automation with [WebDriverAgent] and [gwda]
+- feat: support Android UI automation with [uiautomator2] and [guia2]
+- feat: support UI recognition with [OCR service] and [gwda-ext-opencv]
+
+For iOS/Android device management:
 
-- feat: support iOS UI automation with [WebDriverAgent]
-- feat support Android UI automation with [uiautomator2]
 - feat: integrage ios device management with [gidevice]
-- feat: add specified exit code for different exceptions
-- refactor: make boomer/uixt/httpstat as sub package
+- feat: integrage android device management with [gadb]
+- feat: add simple commands to interact with iOS/Android devices, try `hrp ios` and `hrp adb`
+
+Other improvements:
+
+- feat: exit with specified code for different exceptions
+- refactor: make uixt/gadb/gidevice/boomer/httpstat as hrp sub package
 
 ## v4.2.1 (2022-09-01)
 
 **go version**
 
 - fix: hrp boom duration still limited without specifying `--run-time`
 
@@ -677,7 +768,12 @@
 [locust]: https://locust.io/
 [black]: https://github.com/psf/black
 [loguru]: https://github.com/Delgan/loguru
 [v2-changelog]: https://github.com/httprunner/httprunner/blob/v2/docs/CHANGELOG.md
 [WebDriverAgent]: https://github.com/appium/WebDriverAgent
 [uiautomator2]: https://github.com/appium/appium-uiautomator2-server
 [gidevice]: https://github.com/electricbubble/gidevice
+[gwda]: https://github.com/electricbubble/gwda
+[guia2]: https://github.com/electricbubble/guia2
+[gadb]: https://github.com/electricbubble/gadb
+[OCR service]: https://www.volcengine.com/product/text-recognition
+[gwda-ext-opencv]: https://github.com/electricbubble/gwda-ext-opencv
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `httprunner-4.3.0/httprunner/README.md` & `httprunner-4.3.5/httprunner/README.md`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/__init__.py` & `httprunner-4.3.5/httprunner/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-__version__ = "v4.3.0"
+__version__ = "v4.3.5"
 __description__ = "One-stop solution for HTTP(S) testing."
 
 
 from httprunner.config import Config
 from httprunner.parser import parse_parameters as Parameters
 from httprunner.runner import HttpRunner
 from httprunner.step import Step
```

### Comparing `httprunner-4.3.0/httprunner/builtin/comparators.py` & `httprunner-4.3.5/httprunner/builtin/comparators.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/builtin/functions.py` & `httprunner-4.3.5/httprunner/builtin/functions.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/cli.py` & `httprunner-4.3.5/httprunner/cli.py`

 * *Files 3% similar despite different names*

```diff
@@ -5,28 +5,28 @@
 
 import pytest
 from loguru import logger
 
 from httprunner import __description__, __version__
 from httprunner.compat import ensure_cli_args
 from httprunner.make import init_make_parser, main_make
-from httprunner.utils import ga_client, init_logger, init_sentry_sdk
+from httprunner.utils import ga4_client, init_logger, init_sentry_sdk
 
 init_sentry_sdk()
 
 
 def init_parser_run(subparsers):
     sub_parser_run = subparsers.add_parser(
         "run", help="Make HttpRunner testcases and run with pytest."
     )
     return sub_parser_run
 
 
 def main_run(extra_args) -> enum.IntEnum:
-    ga_client.track_event("RunAPITests", "hrun")
+    ga4_client.send_event("hrun")
     # keep compatibility with v2
     extra_args = ensure_cli_args(extra_args)
 
     tests_path_list = []
     extra_args_new = []
     for item in extra_args:
         if not os.path.exists(item):
```

### Comparing `httprunner-4.3.0/httprunner/cli_test.py` & `httprunner-4.3.5/httprunner/cli_test.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/client.py` & `httprunner-4.3.5/httprunner/client.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/client_test.py` & `httprunner-4.3.5/httprunner/client_test.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,72 +1,73 @@
 import unittest
 
 from httprunner.client import HttpSession
+from httprunner.utils import HTTP_BIN_URL
 
 
 class TestHttpSession(unittest.TestCase):
     def setUp(self):
         self.session = HttpSession()
 
     def test_request_http(self):
-        self.session.request("get", "http://httpbin.org/get")
+        self.session.request("get", f"{HTTP_BIN_URL}/get")
         address = self.session.data.address
         self.assertGreater(len(address.server_ip), 0)
         self.assertEqual(address.server_port, 80)
         self.assertGreater(len(address.client_ip), 0)
         self.assertGreater(address.client_port, 10000)
 
     def test_request_https(self):
-        self.session.request("get", "https://httpbin.org/get")
+        self.session.request("get", "https://postman-echo.com/get")
         address = self.session.data.address
         self.assertGreater(len(address.server_ip), 0)
         self.assertEqual(address.server_port, 443)
         self.assertGreater(len(address.client_ip), 0)
         self.assertGreater(address.client_port, 10000)
 
     def test_request_http_allow_redirects(self):
         self.session.request(
             "get",
-            "http://httpbin.org/redirect-to?url=https%3A%2F%2Fgithub.com",
+            f"{HTTP_BIN_URL}/redirect-to?url=https%3A%2F%2Fgithub.com",
             allow_redirects=True,
         )
         address = self.session.data.address
         self.assertNotEqual(address.server_ip, "N/A")
         self.assertEqual(address.server_port, 443)
         self.assertNotEqual(address.server_ip, "N/A")
         self.assertGreater(address.client_port, 10000)
 
     def test_request_https_allow_redirects(self):
         self.session.request(
             "get",
-            "https://httpbin.org/redirect-to?url=https%3A%2F%2Fgithub.com",
+            "https://postman-echo.com/redirect-to?url=https%3A%2F%2Fgithub.com",
             allow_redirects=True,
         )
         address = self.session.data.address
         self.assertNotEqual(address.server_ip, "N/A")
         self.assertEqual(address.server_port, 443)
         self.assertNotEqual(address.server_ip, "N/A")
         self.assertGreater(address.client_port, 10000)
 
     def test_request_http_not_allow_redirects(self):
         self.session.request(
             "get",
-            "http://httpbin.org/redirect-to?url=https%3A%2F%2Fgithub.com",
+            f"{HTTP_BIN_URL}/redirect-to?url=https%3A%2F%2Fgithub.com",
             allow_redirects=False,
         )
         address = self.session.data.address
         self.assertEqual(address.server_ip, "N/A")
         self.assertEqual(address.server_port, 0)
         self.assertEqual(address.client_ip, "N/A")
         self.assertEqual(address.client_port, 0)
 
     def test_request_https_not_allow_redirects(self):
         self.session.request(
             "get",
-            "https://httpbin.org/redirect-to?url=https%3A%2F%2Fgithub.com",
+            "https://postman-echo.com/redirect-to?url=https%3A%2F%2Fgithub.com",
             allow_redirects=False,
         )
         address = self.session.data.address
         self.assertEqual(address.server_ip, "N/A")
         self.assertEqual(address.server_port, 0)
         self.assertEqual(address.client_ip, "N/A")
         self.assertEqual(address.client_port, 0)
```

### Comparing `httprunner-4.3.0/httprunner/compat.py` & `httprunner-4.3.5/httprunner/compat.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/compat_test.py` & `httprunner-4.3.5/httprunner/compat_test.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import os
 import unittest
 
 from httprunner import compat, exceptions, loader
+from httprunner.utils import HTTP_BIN_URL
 
 
 class TestCompat(unittest.TestCase):
     def setUp(self):
         loader.project_meta = None
 
     def test_convert_variables(self):
@@ -151,15 +152,15 @@
                     }
                 ],
             },
         )
 
     def test_ensure_testcase_v4(self):
         testcase_content = {
-            "config": {"name": "xxx", "base_url": "https://httpbin.org"},
+            "config": {"name": "xxx", "base_url": HTTP_BIN_URL},
             "teststeps": [
                 {
                     "name": "get with params",
                     "request": {
                         "method": "GET",
                         "url": "/get",
                         "params": {"foo1": "bar1", "foo2": "bar2"},
@@ -175,15 +176,15 @@
                     ],
                 }
             ],
         }
         self.assertEqual(
             compat.ensure_testcase_v4(testcase_content),
             {
-                "config": {"name": "xxx", "base_url": "https://httpbin.org"},
+                "config": {"name": "xxx", "base_url": HTTP_BIN_URL},
                 "teststeps": [
                     {
                         "name": "get with params",
                         "request": {
                             "method": "GET",
                             "url": "/get",
                             "params": {"foo1": "bar1", "foo2": "bar2"},
```

### Comparing `httprunner-4.3.0/httprunner/config.py` & `httprunner-4.3.5/httprunner/config.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/database/engine.py` & `httprunner-4.3.5/httprunner/database/engine.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/exceptions.py` & `httprunner-4.3.5/httprunner/exceptions.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/ext/uploader/__init__.py` & `httprunner-4.3.5/httprunner/ext/uploader/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 - filetype
 
 Then you can write upload test script as below:
 
     - test:
         name: upload file
         request:
-            url: http://httpbin.org/upload
+            url: https://httpbin.org/upload
             method: POST
             headers:
                 Cookie: session=AAA-BBB-CCC
             upload:
                 file: "data/file_to_upload"
                 field1: "value1"
                 field2: "value2"
@@ -27,15 +27,15 @@
         name: upload file
         variables:
             file: "data/file_to_upload"
             field1: "value1"
             field2: "value2"
             m_encoder: ${multipart_encoder(file=$file, field1=$field1, field2=$field2)}
         request:
-            url: http://httpbin.org/upload
+            url: https://httpbin.org/upload
             method: POST
             headers:
                 Content-Type: ${multipart_content_type($m_encoder)}
                 Cookie: session=AAA-BBB-CCC
             data: $m_encoder
         validate:
             - eq: ["status_code", 200]
@@ -43,15 +43,15 @@
 """
 
 import os
 import sys
 from typing import Text
 
 from httprunner.models import VariablesMapping, FunctionsMapping, TStep
-from httprunner.parser import parse_data, parse_variables_mapping
+from httprunner.parser import parse_data
 from loguru import logger
 
 try:
     import filetype
     from requests_toolbelt import MultipartEncoder
 
     UPLOAD_READY = True
@@ -71,24 +71,26 @@
     or you can install httprunner with optional upload dependencies:
     $ pip install "httprunner[upload]"
     """
     logger.error(msg)
     sys.exit(1)
 
 
-def prepare_upload_step(step: TStep, step_variables: VariablesMapping, functions: FunctionsMapping):
+def prepare_upload_step(
+    step: TStep, step_variables: VariablesMapping, functions: FunctionsMapping
+):
     """preprocess for upload test
         replace `upload` info with MultipartEncoder
 
     Args:
         step: teststep
             {
                 "variables": {},
                 "request": {
-                    "url": "http://httpbin.org/upload",
+                    "url": "https://httpbin.org/upload",
                     "method": "POST",
                     "headers": {
                         "Cookie": "session=AAA-BBB-CCC"
                     },
                     "upload": {
                         "file": "data/file_to_upload"
                         "md5": "123"
@@ -132,15 +134,14 @@
             return file_type.mime
         else:
             return "text/html"
 
     ensure_upload_ready()
     fields_dict = {}
     for key, value in kwargs.items():
-
         if os.path.isabs(value):
             # value is absolute file path
             _file_path = value
             is_exists_file = os.path.isfile(value)
         else:
             # value is not absolute file path, check if it is relative file path
             from httprunner.loader import load_project_meta
```

### Comparing `httprunner-4.3.0/httprunner/loader.py` & `httprunner-4.3.5/httprunner/loader.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/loader_test.py` & `httprunner-4.3.5/httprunner/loader_test.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/make.py` & `httprunner-4.3.5/httprunner/make.py`

 * *Files 1% similar despite different names*

```diff
@@ -18,15 +18,15 @@
     convert_relative_project_root_dir,
     load_folder_files,
     load_project_meta,
     load_test_file,
     load_testcase,
 )
 from httprunner.response import uniform_validator
-from httprunner.utils import ga_client, is_support_multiprocessing
+from httprunner.utils import ga4_client, is_support_multiprocessing
 
 """ cache converted pytest files, avoid duplicate making
 """
 pytest_files_made_cache_mapping: Dict[Text, Text] = {}
 
 """ save generated pytest files to run, except referenced testcase
 """
@@ -537,15 +537,15 @@
             continue
 
 
 def main_make(tests_paths: List[Text]) -> List[Text]:
     if not tests_paths:
         return []
 
-    ga_client.track_event("ConvertTests", "hmake")
+    ga4_client.send_event("hmake")
 
     for tests_path in tests_paths:
         tests_path = ensure_path_sep(tests_path)
         if not os.path.isabs(tests_path):
             tests_path = os.path.join(os.getcwd(), tests_path)
 
         try:
```

### Comparing `httprunner-4.3.0/httprunner/make_test.py` & `httprunner-4.3.5/httprunner/make_test.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/models.py` & `httprunner-4.3.5/httprunner/models.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/parser.py` & `httprunner-4.3.5/httprunner/parser.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/parser_test.py` & `httprunner-4.3.5/httprunner/parser_test.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/response.py` & `httprunner-4.3.5/httprunner/response.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/response_test.py` & `httprunner-4.3.5/httprunner/response_test.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,19 +1,20 @@
 import unittest
 
 import requests
 
 from httprunner.parser import Parser
 from httprunner.response import ResponseObject, uniform_validator
+from httprunner.utils import HTTP_BIN_URL
 
 
 class TestResponse(unittest.TestCase):
     def setUp(self) -> None:
         resp = requests.post(
-            "https://httpbin.org/anything",
+            f"{HTTP_BIN_URL}/anything",
             json={
                 "locations": [
                     {"name": "Seattle", "state": "WA"},
                     {"name": "New York", "state": "NY"},
                     {"name": "Bellevue", "state": "WA"},
                     {"name": "Olympia", "state": "WA"},
                 ]
```

### Comparing `httprunner-4.3.0/httprunner/runner.py` & `httprunner-4.3.5/httprunner/runner.py`

 * *Files 2% similar despite different names*

```diff
@@ -23,15 +23,15 @@
     TConfig,
     TestCaseInOut,
     TestCaseSummary,
     TestCaseTime,
     VariablesMapping,
 )
 from httprunner.parser import Parser
-from httprunner.utils import LOGGER_FORMAT, merge_variables
+from httprunner.utils import LOGGER_FORMAT, merge_variables, ga4_client
 
 
 class SessionRunner(object):
     config: Config
     teststeps: List[object]  # list of Step
 
     parser: Parser = None
@@ -206,14 +206,15 @@
         # update testcase summary
         self.__step_results.append(step_result)
 
         logger.info(f"run step end: {step.name()} <<<<<<\n")
 
     def test_start(self, param: Dict = None) -> "SessionRunner":
         """main entrance, discovered by pytest"""
+        ga4_client.send_event("test_start")
         print("\n")
         self.__init()
         self.__parse_config(param)
 
         if ALLURE is not None and not self.__is_referenced:
             # update allure report meta
             ALLURE.dynamic.title(self.__config.name)
```

### Comparing `httprunner-4.3.0/httprunner/step.py` & `httprunner-4.3.5/httprunner/step.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/step_request.py` & `httprunner-4.3.5/httprunner/step_request.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/step_request_test.py` & `httprunner-4.3.5/httprunner/step_request_test.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/step_sql_request.py` & `httprunner-4.3.5/httprunner/step_sql_request.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/step_testcase.py` & `httprunner-4.3.5/httprunner/step_testcase.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/step_testcase_test.py` & `httprunner-4.3.5/httprunner/step_testcase_test.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/step_thrift_request.py` & `httprunner-4.3.5/httprunner/step_thrift_request.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/thrift/data_convertor.py` & `httprunner-4.3.5/httprunner/thrift/data_convertor.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/thrift/thrift_client.py` & `httprunner-4.3.5/httprunner/thrift/thrift_client.py`

 * *Files identical despite different names*

### Comparing `httprunner-4.3.0/httprunner/utils.py` & `httprunner-4.3.5/httprunner/utils.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,95 +1,133 @@
 import collections
 import copy
 import itertools
 import json
 import os
 import os.path
 import platform
+import random
 import sys
+import time
 import uuid
 from multiprocessing import Queue
-from typing import Any, Dict, List, Text
+from typing import Any, Dict, List
 
 import requests
 import sentry_sdk
 from loguru import logger
 
 from httprunner import __version__, exceptions
 from httprunner.models import VariablesMapping
 
 
+""" run httpbin as test service
+https://github.com/postmanlabs/httpbin
+
+$ docker pull kennethreitz/httpbin
+$ docker run -p 80:80 kennethreitz/httpbin
+"""
+HTTP_BIN_URL = "http://127.0.0.1:80"
+
+
+def get_platform():
+    return {
+        "httprunner_version": __version__,
+        "python_version": "{} {}".format(
+            platform.python_implementation(), platform.python_version()
+        ),
+        "platform": platform.platform(),
+    }
+
+
 def init_sentry_sdk():
     if os.getenv("DISABLE_SENTRY") == "true":
         return
 
     sentry_sdk.init(
         dsn="https://460e31339bcb428c879aafa6a2e78098@sentry.io/5263855",
         release="httprunner@{}".format(__version__),
     )
     with sentry_sdk.configure_scope() as scope:
         scope.set_user({"id": uuid.getnode()})
 
 
-class GAClient(object):
-
-    version = "1"  # GA API Version
-    report_url = "https://www.google-analytics.com/collect"
-    report_debug_url = (
-        "https://www.google-analytics.com/debug/collect"  # used for debug
-    )
+class GA4Client(object):
+    """send events to Google Analytics 4 via Measurement Protocol.
+    get details in hrp/internal/sdk/ga4.go
+    """
 
-    def __init__(self, tracking_id: Text):
+    def __init__(
+        self, measurement_id: str, api_secret: str, debug: bool = False
+    ) -> None:
         self.http_client = requests.Session()
-        self.label = f"v{__version__}"
-        self.common_params = {
-            "v": self.version,
-            "tid": tracking_id,  # Tracking ID / Property ID, XX-XXXXXXX-X
-            "cid": uuid.getnode(),  # Anonymous Client ID
-            "ua": f"HttpRunner/{__version__}",
-        }
+
+        self.debug = debug
+        if debug:
+            uri = "https://www.google-analytics.com/debug/mp/collect"
+        else:
+            uri = "https://www.google-analytics.com/mp/collect"
+
+        self.uri = f"{uri}?measurement_id={measurement_id}&api_secret={api_secret}"
+        self.user_id = str(uuid.getnode())
+        self.common_event_params = get_platform()
+
         # do not send GA events in CI environment
         self.__is_ci = os.getenv("DISABLE_GA") == "true"
 
-    def track_event(self, category: Text, action: Text, value: int = 0):
+    def send_event(self, name: str, event_params: dict = None) -> None:
         if self.__is_ci:
             return
 
-        data = {
-            "t": "event",  # Event hit type = event
-            "ec": category,  # Required. Event Category.
-            "ea": action,  # Required. Event Action.
-            "el": self.label,  # Optional. Event label, used as version.
-            "ev": value,  # Optional. Event value, must be non-negative integer
+        event_params = event_params or {}
+        event_params.update(self.common_event_params)
+        event = {
+            "name": name,
+            "params": event_params,
+        }
+
+        payload = {
+            "client_id": f"{int(random.random() * 10**8)}.{int(time.time())}",
+            "user_id": self.user_id,
+            "timestamp_micros": int(time.time() * 10**6),
+            "events": [event],
         }
-        data.update(self.common_params)
+
+        if self.debug:
+            logger.debug(f"send GA4 event, uri: {self.uri}, payload: {payload}")
+
         try:
-            self.http_client.post(self.report_url, data=data, timeout=5)
-        except Exception:  # ProxyError, SSLError, ConnectionError
-            pass
+            resp = self.http_client.post(self.uri, json=payload, timeout=5)
+        except Exception as err:  # ProxyError, SSLError, ConnectionError
+            logger.error(f"request GA4 failed, error: {err}")
+            return
 
-    def track_user_timing(self, category: Text, variable: Text, duration: int):
-        if self.__is_ci:
+        if resp.status_code >= 300:
+            logger.error(
+                f"validation response got unexpected status: {resp.status_code}"
+            )
+            return
+
+        if not self.debug:
             return
 
-        data = {
-            "t": "timing",  # Event hit type = timing
-            "utc": category,  # Required. user timing category. e.g. jsonLoader
-            "utv": variable,  # Required. timing variable. e.g. load
-            "utt": duration,  # Required. time took duration.
-            "utl": self.label,  # Optional. user timing label, used as version.
-        }
-        data.update(self.common_params)
         try:
-            self.http_client.post(self.report_url, data=data, timeout=5)
-        except Exception:  # ProxyError, SSLError, ConnectionError
+            resp_body = resp.json()
+            logger.debug(
+                "get GA4 validation response, "
+                f"status code: {resp.status_code}, body: {resp_body}"
+            )
+        except Exception:
             pass
 
 
-ga_client = GAClient("UA-114587036-1")
+GA4_MEASUREMENT_ID = "G-9KHR3VC2LN"
+GA4_API_SECRET = "w7lKNQIrQsKNS4ikgMPp0Q"
+
+ga4_client = GA4Client(GA4_MEASUREMENT_ID, GA4_API_SECRET, False)
 
 
 def set_os_environ(variables_mapping):
     """set variables mapping to os.environ"""
     for variable in variables_mapping:
         os.environ[variable] = variables_mapping[variable]
         logger.debug(f"Set OS environment variable: {variable}")
@@ -215,24 +253,14 @@
     appendix_str = f" ... OMITTED {body_len - omit_len} CHARACTORS ..."
     if isinstance(body, bytes):
         appendix_str = appendix_str.encode("utf-8")
 
     return omitted_body + appendix_str
 
 
-def get_platform():
-    return {
-        "httprunner_version": __version__,
-        "python_version": "{} {}".format(
-            platform.python_implementation(), platform.python_version()
-        ),
-        "platform": platform.platform(),
-    }
-
-
 def sort_dict_by_custom_order(raw_dict: Dict, custom_order: List):
     def get_index_from_list(lst: List, item: Any):
         try:
             return lst.index(item)
         except ValueError:
             # item is not in lst
             return len(lst) + 1
```

### Comparing `httprunner-4.3.0/httprunner/utils_test.py` & `httprunner-4.3.5/httprunner/utils_test.py`

 * *Files 4% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import os
 import unittest
 from pathlib import Path
 
 import toml
 
 from httprunner import __version__, loader, utils
-from httprunner.utils import ExtendJSONEncoder, merge_variables
+from httprunner.utils import ExtendJSONEncoder, merge_variables, ga4_client
 
 
 class TestUtils(unittest.TestCase):
     def test_set_os_environ(self):
         self.assertNotIn("abc", os.environ)
         variables_mapping = {"abc": "123"}
         utils.set_os_environ(variables_mapping)
@@ -117,18 +117,18 @@
         with self.assertRaises(TypeError):
             json.dumps(data)
 
         json.dumps(data, cls=ExtendJSONEncoder)
 
     def test_override_config_variables(self):
         step_variables = {"base_url": "$base_url", "foo1": "bar1"}
-        config_variables = {"base_url": "https://httpbin.org", "foo1": "bar111"}
+        config_variables = {"base_url": "https://postman-echo.com", "foo1": "bar111"}
         self.assertEqual(
             merge_variables(step_variables, config_variables),
-            {"base_url": "https://httpbin.org", "foo1": "bar1"},
+            {"base_url": "https://postman-echo.com", "foo1": "bar1"},
         )
 
     def test_cartesian_product_one(self):
         parameters_content_list = [[{"a": 1}, {"a": 2}]]
         product_list = utils.gen_cartesian_product(*parameters_content_list)
         self.assertEqual(product_list, [{"a": 1}, {"a": 2}])
 
@@ -156,7 +156,16 @@
     def test_versions_are_in_sync(self):
         """Checks if the pyproject.toml and __version__ in __init__.py are in sync."""
 
         path = Path(__file__).resolve().parents[1] / "pyproject.toml"
         pyproject = toml.loads(open(str(path)).read())
         pyproject_version = pyproject["tool"]["poetry"]["version"]
         self.assertEqual(pyproject_version, __version__)
+
+    def test_ga4_send_event(self):
+        ga4_client.send_event(
+            "httprunner_debug_event",
+            {
+                "a": 123,
+                "b": 456,
+            },
+        )
```

### Comparing `httprunner-4.3.0/pyproject.toml` & `httprunner-4.3.5/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "httprunner"
-version = "v4.3.0"
+version = "v4.3.5"
 description = "One-stop solution for HTTP(S) testing."
 license = "Apache-2.0"
 readme = "README.md"
 authors = ["debugtalk <debugtalk@gmail.com>"]
 
 homepage = "https://httprunner.com"
 repository = "https://github.com/httprunner/httprunner"
@@ -26,34 +26,35 @@
     "Programming Language :: Python :: 3.10"
 ]
 
 include = ["docs/CHANGELOG.md"]
 
 [tool.poetry.dependencies]
 python = "^3.7"
-requests = "^2.22.0"
-pyyaml = "^5.4.1"
 pydantic = "~1.8"   # >=1.8.0 <1.9.0
 loguru = "^0.4.1"
 jmespath = "^0.9.5"
 black = "^22.3.0"
 pytest = "^7.1.1"
 pytest-html = "^3.1.1"
 sentry-sdk = "^0.14.4"
 allure-pytest = {version = "^2.8.16", optional = true}
-requests-toolbelt = {version = "^0.9.1", optional = true}
+requests-toolbelt = {version = "^0.10.1", optional = true}
 filetype = {version = "^1.0.7", optional = true}
 Brotli = "^1.0.9"
 jinja2 = "^3.0.3"
 toml = "^0.10.2"
 sqlalchemy = {version = "^1.4.36", optional = true}
 pymysql = {version = "^1.0.2",optional = true}
 cython = {version = "^0.29.28", optional = true}
 thriftpy2 = {version = "^0.4.14", optional = true}
 thrift = {version = "^0.16.0", optional = true}
+pyyaml = "^6.0.1"
+requests = "^2.31.0"
+urllib3 = "^1.26"
 
 [tool.poetry.extras]
 allure = ["allure-pytest"]                  # pip install "httprunner[allure]", poetry install -E allure
 upload = ["requests-toolbelt", "filetype"]  # pip install "httprunner[upload]", poetry install -E upload
 sql = ["sqlalchemy","pymysql"]              # pip install "httprunner[sql]", poetry install -E sql
 thrift = ["cython","thrift","thriftpy2"]    # pip install "httprunner[thrift]", poetry install -E sql
```

### Comparing `httprunner-4.3.0/PKG-INFO` & `httprunner-4.3.5/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,54 +1,56 @@
 Metadata-Version: 2.1
 Name: httprunner
-Version: 4.3.0
+Version: 4.3.5
 Summary: One-stop solution for HTTP(S) testing.
 Home-page: https://httprunner.com
 License: Apache-2.0
 Keywords: HTTP,apitest,perftest,requests
 Author: debugtalk
 Author-email: debugtalk@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: MacOS
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX :: Linux
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Classifier: Topic :: Software Development :: Quality Assurance
 Classifier: Topic :: Software Development :: Testing
 Provides-Extra: allure
 Provides-Extra: sql
 Provides-Extra: thrift
 Provides-Extra: upload
 Requires-Dist: Brotli (>=1.0.9,<2.0.0)
-Requires-Dist: allure-pytest (>=2.8.16,<3.0.0); extra == "allure"
+Requires-Dist: allure-pytest (>=2.8.16,<3.0.0) ; extra == "allure"
 Requires-Dist: black (>=22.3.0,<23.0.0)
-Requires-Dist: cython (>=0.29.28,<0.30.0); extra == "thrift"
-Requires-Dist: filetype (>=1.0.7,<2.0.0); extra == "upload"
+Requires-Dist: cython (>=0.29.28,<0.30.0) ; extra == "thrift"
+Requires-Dist: filetype (>=1.0.7,<2.0.0) ; extra == "upload"
 Requires-Dist: jinja2 (>=3.0.3,<4.0.0)
 Requires-Dist: jmespath (>=0.9.5,<0.10.0)
 Requires-Dist: loguru (>=0.4.1,<0.5.0)
 Requires-Dist: pydantic (>=1.8,<1.9)
-Requires-Dist: pymysql (>=1.0.2,<2.0.0); extra == "sql"
+Requires-Dist: pymysql (>=1.0.2,<2.0.0) ; extra == "sql"
 Requires-Dist: pytest (>=7.1.1,<8.0.0)
 Requires-Dist: pytest-html (>=3.1.1,<4.0.0)
-Requires-Dist: pyyaml (>=5.4.1,<6.0.0)
-Requires-Dist: requests (>=2.22.0,<3.0.0)
-Requires-Dist: requests-toolbelt (>=0.9.1,<0.10.0); extra == "upload"
+Requires-Dist: pyyaml (>=6.0.1,<7.0.0)
+Requires-Dist: requests (>=2.31.0,<3.0.0)
+Requires-Dist: requests-toolbelt (>=0.10.1,<0.11.0) ; extra == "upload"
 Requires-Dist: sentry-sdk (>=0.14.4,<0.15.0)
-Requires-Dist: sqlalchemy (>=1.4.36,<2.0.0); extra == "sql"
-Requires-Dist: thrift (>=0.16.0,<0.17.0); extra == "thrift"
-Requires-Dist: thriftpy2 (>=0.4.14,<0.5.0); extra == "thrift"
+Requires-Dist: sqlalchemy (>=1.4.36,<2.0.0) ; extra == "sql"
+Requires-Dist: thrift (>=0.16.0,<0.17.0) ; extra == "thrift"
+Requires-Dist: thriftpy2 (>=0.4.14,<0.5.0) ; extra == "thrift"
 Requires-Dist: toml (>=0.10.2,<0.11.0)
+Requires-Dist: urllib3 (>=1.26,<2.0)
 Project-URL: Documentation, https://httprunner.com/docs
 Project-URL: Repository, https://github.com/httprunner/httprunner
 Description-Content-Type: text/markdown
 
 # HttpRunner
 
 [![Github Actions](https://github.com/httprunner/httprunner/actions/workflows/unittest.yml/badge.svg)](https://github.com/httprunner/httprunner/actions)
@@ -127,19 +129,21 @@
 Github: https://github.com/httprunner/httprunner
 Copyright 2017 debugtalk
 
 Usage:
   hrp [command]
 
 Available Commands:
+  adb          simple utils for android device management
   boom         run load test with boomer
   build        build plugin for testing
-  completion   generate the autocompletion script for the specified shell
-  convert      convert to JSON/YAML/gotest/pytest testcases
+  completion   Generate the autocompletion script for the specified shell
+  convert      convert multiple source format to HttpRunner JSON/YAML/gotest/pytest cases
   help         Help about any command
+  ios          simple utils for ios device management
   pytest       run API test with pytest
   run          run API test with go engine
   startproject create a scaffold project
   wiki         visit https://httprunner.com
 
 Flags:
   -h, --help               help for hrp
@@ -154,38 +158,27 @@
 ## 用户案例
 
 <a href="https://httprunner.com/docs/cases/dji-ibg"><img src="https://httprunner.com/image/logo/dji.jpeg" title="大疆 - 基于 HttpRunner 构建完整的自动化测试体系" width="60"></a>
 <a href="https://httprunner.com/docs/cases/youmi"><img src="https://httprunner.com/image/logo/youmi.png" title="有米科技 - 基于 HttpRunner 建设自动化测试平台" width="60"></a>
 <a href="https://httprunner.com/docs/cases/umcare"><img src="https://httprunner.com/image/logo/umcare.png" title="通用环球医疗 - 使用 HttpRunner 实践接口自动化测试" width="100"></a>
 <a href="https://httprunner.com/docs/cases/mihoyo"><img src="https://httprunner.com/image/logo/miHoYo.png" title="米哈游 - 基于 HttpRunner 搭建接口自动化测试体系" width="100"></a>
 
-## 赞助商
-
-### 金牌赞助商
-
-[<img src="https://httprunner.com/image/hogwarts.jpeg" alt="霍格沃兹测试开发学社" width="400">](https://ceshiren.com/)
 
-> [霍格沃兹测试开发学社](http://qrcode.testing-studio.com/f?from=httprunner&url=https://ceshiren.com)是业界领先的测试开发技术高端教育品牌，隶属于[测吧（北京）科技有限公司](http://qrcode.testing-studio.com/f?from=httprunner&url=https://www.testing-studio.com) 。学院课程由一线大厂测试经理与资深测试开发专家参与研发，实战驱动。课程涵盖 web/app 自动化测试、接口测试、性能测试、安全测试、持续集成/持续交付/DevOps，测试左移&右移、精准测试、测试平台开发、测试管理等内容，帮助测试工程师实现测试开发技术转型。通过优秀的学社制度（奖学金、内推返学费、行业竞赛等多种方式）来实现学员、学社及用人企业的三方共赢。
-
-> [进入测试开发技术能力测评!](http://qrcode.testing-studio.com/f?from=httprunner&url=https://ceshiren.com/t/topic/14940)
-
-### 开源服务赞助商
+## 赞助商
 
-[<img src="https://httprunner.com/image/sentry-logo-black.svg" alt="Sentry" width="150">](https://sentry.io/_/open-source/)
+[<img src="https://testing-studio.com/img/icon.png" alt="霍格沃兹测试开发学社" width="500">](https://qrcode.testing-studio.com/f?from=HttpRunner&url=https://testing-studio.com/)
 
-HttpRunner is in Sentry Sponsored plan.
+> 霍格沃兹测试开发学社是中国软件测试开发高端教育品牌，产品由国内顶尖软件测试开发技术专家携手打造，为企业与个人提供专业的技能培训与咨询、测试工具与测试平台、测试外包与测试众包服务。领域涵盖 App/Web 自动化测试、接口自动化测试、性能测试、安全测试、持续交付/DevOps、测试左移、测试右移、精准测试、测试平台开发、测试管理等方向。-> [**联系我们**](http://qrcode.testing-studio.com/f?from=HttpRunner&url=https://ceshiren.com/t/topic/23745)
 
 ## Subscribe
 
 关注 HttpRunner 的微信公众号，第一时间获得最新资讯。
 
 <img src="https://httprunner.com/image/qrcode.png" alt="HttpRunner" width="400">
 
-如果你期望加入 HttpRunner 用户群，请看这里：[HttpRunner v4 用户交流群，它来啦！](https://httprunner.com/blog/join-chat-group)
-
 [HttpRunner]: https://github.com/httprunner/httprunner
 [boomer]: https://github.com/myzhan/boomer
 [locust]: https://github.com/locustio/locust
 [jmespath]: https://jmespath.org/
 [allure]: https://docs.qameta.io/allure/
 [HAR]: https://en.wikipedia.org/wiki/HAR_(file_format)
 [hashicorp plugin]: https://github.com/hashicorp/go-plugin
```

