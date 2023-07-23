# Comparing `tmp/python_kasa-0.5.2.tar.gz` & `tmp/python_kasa-0.5.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "python_kasa-0.5.2.tar", max compression
+gzip compressed data, was "python_kasa-0.5.3.tar", max compression
```

## Comparing `python_kasa-0.5.2.tar` & `python_kasa-0.5.3.tar`

### file list

```diff
@@ -1,105 +1,106 @@
--rw-r--r--   0        0        0    66931 2023-07-02 14:29:08.870189 python_kasa-0.5.2/CHANGELOG.md
--rw-r--r--   0        0        0    33218 2023-07-02 14:29:08.870189 python_kasa-0.5.2/LICENSE
--rw-r--r--   0        0        0     6690 2023-07-02 14:29:08.870189 python_kasa-0.5.2/README.md
--rwxr-xr-x   0        0        0     1288 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/__init__.py
--rwxr-xr-x   0        0        0    21335 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/cli.py
--rwxr-xr-x   0        0        0     8514 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/discover.py
--rw-r--r--   0        0        0     7476 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/effects.py
--rw-r--r--   0        0        0     2311 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/emeterstatus.py
--rw-r--r--   0        0        0      115 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/exceptions.py
--rwxr-xr-x   0        0        0      262 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/json.py
--rw-r--r--   0        0        0      571 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/__init__.py
--rw-r--r--   0        0        0     1617 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/ambientlight.py
--rw-r--r--   0        0        0      234 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/antitheft.py
--rw-r--r--   0        0        0     1370 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/cloud.py
--rw-r--r--   0        0        0      158 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/countdown.py
--rw-r--r--   0        0        0     2947 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/emeter.py
--rw-r--r--   0        0        0     2351 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/module.py
--rw-r--r--   0        0        0     2294 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/motion.py
--rw-r--r--   0        0        0     1924 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/rulemodule.py
--rw-r--r--   0        0        0      150 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/schedule.py
--rw-r--r--   0        0        0     1417 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/time.py
--rw-r--r--   0        0        0     3476 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/modules/usage.py
--rwxr-xr-x   0        0        0     8733 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/protocol.py
--rw-r--r--   0        0        0        0 2023-07-02 14:29:08.870189 python_kasa-0.5.2/kasa/py.typed
--rw-r--r--   0        0        0    18768 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/smartbulb.py
--rwxr-xr-x   0        0        0    24405 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/smartdevice.py
--rw-r--r--   0        0        0     7217 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/smartdimmer.py
--rw-r--r--   0        0        0     4019 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/smartlightstrip.py
--rw-r--r--   0        0        0     2758 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/smartplug.py
--rwxr-xr-x   0        0        0    12649 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/smartstrip.py
--rw-r--r--   0        0        0        0 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/__init__.py
--rw-r--r--   0        0        0     6626 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/conftest.py
--rw-r--r--   0        0        0      974 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/EP10(US)_1.0_1.0.2.json
--rw-r--r--   0        0        0     1427 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/EP40(US)_1.0_1.0.2.json
--rw-r--r--   0        0        0     3677 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/ES20M(US)_1.0_1.0.8.json
--rw-r--r--   0        0        0     1305 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS100(US)_1.0_1.2.5.json
--rw-r--r--   0        0        0     1422 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS100(US)_2.0_1.5.6.json
--rw-r--r--   0        0        0     1552 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS103(US)_1.0_1.5.7.json
--rw-r--r--   0        0        0     1356 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS103(US)_2.1_1.1.2.json
--rw-r--r--   0        0        0      938 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS103(US)_2.1_1.1.4.json
--rw-r--r--   0        0        0     1425 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS105(US)_1.0_1.5.6.json
--rw-r--r--   0        0        0     1397 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS105(US)_1.0_mocked.json
--rw-r--r--   0        0        0     1729 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS107(US)_1.0_1.0.8.json
--rw-r--r--   0        0        0     1477 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS110(EU)_1.0_1.2.5.json
--rw-r--r--   0        0        0     1503 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS110(EU)_2.0_mocked.json
--rw-r--r--   0        0        0     1480 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS110(US)_1.0_mocked.json
--rw-r--r--   0        0        0     1388 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS200(US)_1.0_mocked.json
--rw-r--r--   0        0        0     1442 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS200(US)_2.0_1.5.7.json
--rw-r--r--   0        0        0      946 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS200(US)_5.0_1.0.2.json
--rw-r--r--   0        0        0     1476 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS210(US)_1.0_1.5.8.json
--rw-r--r--   0        0        0     2183 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS220(US)_1.0_1.5.7.json
--rw-r--r--   0        0        0     2175 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS220(US)_1.0_mocked.json
--rw-r--r--   0        0        0     1845 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS220(US)_2.0_1.0.3.json
--rw-r--r--   0        0        0     2964 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS300(US)_1.0_1.0.10.json
--rw-r--r--   0        0        0     2866 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/HS300(US)_2.0_1.0.3.json
--rw-r--r--   0        0        0     2664 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL110(US)_1.0_1.8.11.json
--rw-r--r--   0        0        0     2724 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL120(US)_1.0_1.8.6.json
--rw-r--r--   0        0        0     2627 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL125(US)_1.20_1.0.5.json
--rw-r--r--   0        0        0     2768 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL125(US)_2.0_1.0.7.json
--rw-r--r--   0        0        0     2537 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL130(EU)_1.0_1.8.8.json
--rw-r--r--   0        0        0     2667 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL130(US)_1.0_1.8.11.json
--rw-r--r--   0        0        0     2649 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL135(US)_1.0_1.0.6.json
--rw-r--r--   0        0        0     1717 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL400L5(US)_1.0_1.0.5.json
--rw-r--r--   0        0        0     1750 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL400L5(US)_1.0_1.0.8.json
--rw-r--r--   0        0        0     1721 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL420L5(US)_1.0_1.0.2.json
--rw-r--r--   0        0        0     2757 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL430(UN)_2.0_1.0.8.json
--rw-r--r--   0        0        0     2065 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL430(US)_1.0_1.0.10.json
--rw-r--r--   0        0        0     1787 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL430(US)_2.0_1.0.8.json
--rw-r--r--   0        0        0     1757 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL430(US)_2.0_1.0.9.json
--rw-r--r--   0        0        0     2661 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL50(US)_1.0_1.1.13.json
--rw-r--r--   0        0        0     3007 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL60(UN)_1.0_1.1.4.json
--rw-r--r--   0        0        0     2668 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KL60(US)_1.0_1.1.13.json
--rw-r--r--   0        0        0      940 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP100(US)_3.0_1.0.1.json
--rw-r--r--   0        0        0      997 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP105(UK)_1.0_1.0.7.json
--rw-r--r--   0        0        0     1227 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP115(EU)_1.0_1.0.16.json
--rw-r--r--   0        0        0     1213 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP115(US)_1.0_1.0.17.json
--rw-r--r--   0        0        0     1230 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP125(US)_1.0_1.0.6.json
--rw-r--r--   0        0        0     2036 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP303(UK)_1.0_1.0.3.json
--rw-r--r--   0        0        0     1738 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP303(US)_2.0_1.0.3.json
--rw-r--r--   0        0        0     1843 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP400(US)_1.0_1.0.10.json
--rw-r--r--   0        0        0     1431 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP400(US)_2.0_1.0.6.json
--rw-r--r--   0        0        0      966 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP401(US)_1.0_1.0.0.json
--rw-r--r--   0        0        0     1892 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KP405(US)_1.0_1.0.5.json
--rw-r--r--   0        0        0     2842 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KS200M(US)_1.0_1.0.8.json
--rw-r--r--   0        0        0     3684 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KS220M(US)_1.0_1.0.4.json
--rw-r--r--   0        0        0     1836 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/KS230(US)_1.0_1.0.14.json
--rw-r--r--   0        0        0     3062 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/LB100(US)_1.0_mocked.json
--rw-r--r--   0        0        0     2684 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/LB110(US)_1.0_1.8.11.json
--rw-r--r--   0        0        0     3067 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/LB120(US)_1.0_mocked.json
--rw-r--r--   0        0        0     3106 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/fixtures/LB130(US)_1.0_mocked.json
--rw-r--r--   0        0        0    16115 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/newfakes.py
--rw-r--r--   0        0        0     8947 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_bulb.py
--rw-r--r--   0        0        0     3210 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_cli.py
--rw-r--r--   0        0        0     3573 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_dimmer.py
--rw-r--r--   0        0        0     4241 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_discovery.py
--rw-r--r--   0        0        0     2997 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_emeter.py
--rw-r--r--   0        0        0     2142 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_lightstrip.py
--rw-r--r--   0        0        0      593 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_plug.py
--rw-r--r--   0        0        0     5611 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_protocol.py
--rw-r--r--   0        0        0     2545 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_readme_examples.py
--rw-r--r--   0        0        0     4014 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_smartdevice.py
--rw-r--r--   0        0        0     4056 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_strip.py
--rw-r--r--   0        0        0      576 2023-07-02 14:29:08.874189 python_kasa-0.5.2/kasa/tests/test_usage.py
--rw-r--r--   0        0        0     2410 2023-07-02 14:29:08.874189 python_kasa-0.5.2/pyproject.toml
--rw-r--r--   0        0        0     8043 1970-01-01 00:00:00.000000 python_kasa-0.5.2/PKG-INFO
+-rw-r--r--   0        0        0    67807 2023-07-23 13:53:28.687372 python_kasa-0.5.3/CHANGELOG.md
+-rw-r--r--   0        0        0    33218 2023-07-23 13:53:28.687372 python_kasa-0.5.3/LICENSE
+-rw-r--r--   0        0        0     6708 2023-07-23 13:53:28.687372 python_kasa-0.5.3/README.md
+-rwxr-xr-x   0        0        0     1288 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/__init__.py
+-rwxr-xr-x   0        0        0    21509 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/cli.py
+-rwxr-xr-x   0        0        0     8567 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/discover.py
+-rw-r--r--   0        0        0     7476 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/effects.py
+-rw-r--r--   0        0        0     2311 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/emeterstatus.py
+-rw-r--r--   0        0        0      115 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/exceptions.py
+-rwxr-xr-x   0        0        0      262 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/json.py
+-rw-r--r--   0        0        0      571 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/__init__.py
+-rw-r--r--   0        0        0     1617 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/ambientlight.py
+-rw-r--r--   0        0        0      234 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/antitheft.py
+-rw-r--r--   0        0        0     1370 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/cloud.py
+-rw-r--r--   0        0        0      158 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/countdown.py
+-rw-r--r--   0        0        0     2947 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/emeter.py
+-rw-r--r--   0        0        0     2351 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/module.py
+-rw-r--r--   0        0        0     2294 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/motion.py
+-rw-r--r--   0        0        0     1924 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/rulemodule.py
+-rw-r--r--   0        0        0      150 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/schedule.py
+-rw-r--r--   0        0        0     1417 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/time.py
+-rw-r--r--   0        0        0     3476 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/modules/usage.py
+-rwxr-xr-x   0        0        0     9010 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/protocol.py
+-rw-r--r--   0        0        0        0 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/py.typed
+-rw-r--r--   0        0        0    18810 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/smartbulb.py
+-rwxr-xr-x   0        0        0    24472 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/smartdevice.py
+-rw-r--r--   0        0        0     7259 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/smartdimmer.py
+-rw-r--r--   0        0        0     4061 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/smartlightstrip.py
+-rw-r--r--   0        0        0     2810 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/smartplug.py
+-rwxr-xr-x   0        0        0    12691 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/smartstrip.py
+-rw-r--r--   0        0        0        0 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/__init__.py
+-rw-r--r--   0        0        0     6635 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/conftest.py
+-rw-r--r--   0        0        0      974 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/EP10(US)_1.0_1.0.2.json
+-rw-r--r--   0        0        0     1427 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/EP40(US)_1.0_1.0.2.json
+-rw-r--r--   0        0        0     3677 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/ES20M(US)_1.0_1.0.8.json
+-rw-r--r--   0        0        0     1305 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS100(US)_1.0_1.2.5.json
+-rw-r--r--   0        0        0     1422 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS100(US)_2.0_1.5.6.json
+-rw-r--r--   0        0        0     1552 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS103(US)_1.0_1.5.7.json
+-rw-r--r--   0        0        0     1356 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS103(US)_2.1_1.1.2.json
+-rw-r--r--   0        0        0      938 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS103(US)_2.1_1.1.4.json
+-rw-r--r--   0        0        0     1425 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS105(US)_1.0_1.5.6.json
+-rw-r--r--   0        0        0     1397 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS105(US)_1.0_mocked.json
+-rw-r--r--   0        0        0     1729 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS107(US)_1.0_1.0.8.json
+-rw-r--r--   0        0        0     1477 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS110(EU)_1.0_1.2.5.json
+-rw-r--r--   0        0        0     1503 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS110(EU)_2.0_mocked.json
+-rw-r--r--   0        0        0     1480 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS110(US)_1.0_mocked.json
+-rw-r--r--   0        0        0     1388 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS200(US)_1.0_mocked.json
+-rw-r--r--   0        0        0     1442 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS200(US)_2.0_1.5.7.json
+-rw-r--r--   0        0        0      946 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS200(US)_5.0_1.0.2.json
+-rw-r--r--   0        0        0     1476 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS210(US)_1.0_1.5.8.json
+-rw-r--r--   0        0        0     2183 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS220(US)_1.0_1.5.7.json
+-rw-r--r--   0        0        0     2175 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS220(US)_1.0_mocked.json
+-rw-r--r--   0        0        0     1845 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS220(US)_2.0_1.0.3.json
+-rw-r--r--   0        0        0     2964 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS300(US)_1.0_1.0.10.json
+-rw-r--r--   0        0        0     2866 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/HS300(US)_2.0_1.0.3.json
+-rw-r--r--   0        0        0     2664 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL110(US)_1.0_1.8.11.json
+-rw-r--r--   0        0        0     2724 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL120(US)_1.0_1.8.6.json
+-rw-r--r--   0        0        0     2627 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL125(US)_1.20_1.0.5.json
+-rw-r--r--   0        0        0     2768 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL125(US)_2.0_1.0.7.json
+-rw-r--r--   0        0        0     2537 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL130(EU)_1.0_1.8.8.json
+-rw-r--r--   0        0        0     2667 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL130(US)_1.0_1.8.11.json
+-rw-r--r--   0        0        0     2649 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL135(US)_1.0_1.0.6.json
+-rw-r--r--   0        0        0     1717 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL400L5(US)_1.0_1.0.5.json
+-rw-r--r--   0        0        0     1750 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL400L5(US)_1.0_1.0.8.json
+-rw-r--r--   0        0        0     1721 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL420L5(US)_1.0_1.0.2.json
+-rw-r--r--   0        0        0     2757 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL430(UN)_2.0_1.0.8.json
+-rw-r--r--   0        0        0     2065 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL430(US)_1.0_1.0.10.json
+-rw-r--r--   0        0        0     1787 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL430(US)_2.0_1.0.8.json
+-rw-r--r--   0        0        0     1757 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL430(US)_2.0_1.0.9.json
+-rw-r--r--   0        0        0     2661 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL50(US)_1.0_1.1.13.json
+-rw-r--r--   0        0        0     3007 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL60(UN)_1.0_1.1.4.json
+-rw-r--r--   0        0        0     2668 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KL60(US)_1.0_1.1.13.json
+-rw-r--r--   0        0        0      940 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP100(US)_3.0_1.0.1.json
+-rw-r--r--   0        0        0      997 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP105(UK)_1.0_1.0.7.json
+-rw-r--r--   0        0        0     1227 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP115(EU)_1.0_1.0.16.json
+-rw-r--r--   0        0        0     1213 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP115(US)_1.0_1.0.17.json
+-rw-r--r--   0        0        0     1230 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP125(US)_1.0_1.0.6.json
+-rw-r--r--   0        0        0     1460 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP200(US)_3.0_1.0.3.json
+-rw-r--r--   0        0        0     2036 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP303(UK)_1.0_1.0.3.json
+-rw-r--r--   0        0        0     1738 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP303(US)_2.0_1.0.3.json
+-rw-r--r--   0        0        0     1843 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP400(US)_1.0_1.0.10.json
+-rw-r--r--   0        0        0     1431 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP400(US)_2.0_1.0.6.json
+-rw-r--r--   0        0        0      966 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP401(US)_1.0_1.0.0.json
+-rw-r--r--   0        0        0     1892 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KP405(US)_1.0_1.0.5.json
+-rw-r--r--   0        0        0     2842 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KS200M(US)_1.0_1.0.8.json
+-rw-r--r--   0        0        0     3684 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KS220M(US)_1.0_1.0.4.json
+-rw-r--r--   0        0        0     1836 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/KS230(US)_1.0_1.0.14.json
+-rw-r--r--   0        0        0     3062 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/LB100(US)_1.0_mocked.json
+-rw-r--r--   0        0        0     2684 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/LB110(US)_1.0_1.8.11.json
+-rw-r--r--   0        0        0     3067 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/LB120(US)_1.0_mocked.json
+-rw-r--r--   0        0        0     3106 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/fixtures/LB130(US)_1.0_mocked.json
+-rw-r--r--   0        0        0    16115 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/newfakes.py
+-rw-r--r--   0        0        0     8947 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_bulb.py
+-rw-r--r--   0        0        0     3210 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_cli.py
+-rw-r--r--   0        0        0     3573 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_dimmer.py
+-rw-r--r--   0        0        0     4358 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_discovery.py
+-rw-r--r--   0        0        0     2997 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_emeter.py
+-rw-r--r--   0        0        0     2142 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_lightstrip.py
+-rw-r--r--   0        0        0      593 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_plug.py
+-rw-r--r--   0        0        0     6732 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_protocol.py
+-rw-r--r--   0        0        0     2545 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_readme_examples.py
+-rw-r--r--   0        0        0     4014 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_smartdevice.py
+-rw-r--r--   0        0        0     4056 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_strip.py
+-rw-r--r--   0        0        0      576 2023-07-23 13:53:28.691372 python_kasa-0.5.3/kasa/tests/test_usage.py
+-rw-r--r--   0        0        0     2436 2023-07-23 13:53:28.695373 python_kasa-0.5.3/pyproject.toml
+-rw-r--r--   0        0        0     8100 1970-01-01 00:00:00.000000 python_kasa-0.5.3/PKG-INFO
```

### Comparing `python_kasa-0.5.2/CHANGELOG.md` & `python_kasa-0.5.3/CHANGELOG.md`

 * *Files 0% similar despite different names*

```diff
@@ -1,9 +1,28 @@
 # Changelog
 
+## [0.5.3](https://github.com/python-kasa/python-kasa/tree/0.5.3) (2023-07-23)
+
+[Full Changelog](https://github.com/python-kasa/python-kasa/compare/0.5.2...0.5.3)
+
+This release adds support for defining the device port and introduces dependency on async-timeout which improves timeout handling.
+
+**Implemented enhancements:**
+
+- Make device port configurable [\#471](https://github.com/python-kasa/python-kasa/pull/471) (@karpach)
+
+**Fixed bugs:**
+
+- Replace asyncio.wait\_for with async-timeout [\#480](https://github.com/python-kasa/python-kasa/pull/480) (@bdraco)
+
+**Merged pull requests:**
+
+- Add tests for KP200 [\#483](https://github.com/python-kasa/python-kasa/pull/483) (@bdraco)
+- Update pyyaml to fix CI [\#482](https://github.com/python-kasa/python-kasa/pull/482) (@bdraco)
+
 ## [0.5.2](https://github.com/python-kasa/python-kasa/tree/0.5.2) (2023-07-02)
 
 [Full Changelog](https://github.com/python-kasa/python-kasa/compare/0.5.1...0.5.2)
 
 Besides some small improvements, this release:
 * Adds optional dependency for for `orjson` and `kasa-crypt` to speed-up protocol handling by an order of magnitude.
 * Drops Python 3.7 support as it is no longer maintained.
@@ -37,14 +56,15 @@
 - bulb.turn\_off making device undiscoverable [\#444](https://github.com/python-kasa/python-kasa/issues/444)
 - best privacy practices for Kasa devices [\#438](https://github.com/python-kasa/python-kasa/issues/438)
 - Access device from different network [\#424](https://github.com/python-kasa/python-kasa/issues/424)
 - Lots of test failure with 0.5.0 [\#411](https://github.com/python-kasa/python-kasa/issues/411)
 
 **Merged pull requests:**
 
+- Release 0.5.2 [\#475](https://github.com/python-kasa/python-kasa/pull/475) (@rytilahti)
 - Add benchmarks for speedups [\#473](https://github.com/python-kasa/python-kasa/pull/473) (@bdraco)
 - Add fixture for KP405 Smart Dimmer Plug [\#470](https://github.com/python-kasa/python-kasa/pull/470) (@xinud190)
 - Remove importlib-metadata dependency [\#457](https://github.com/python-kasa/python-kasa/pull/457) (@rytilahti)
 - Update dependencies to fix CI [\#454](https://github.com/python-kasa/python-kasa/pull/454) (@rytilahti)
 - Cleanup fixture filenames [\#448](https://github.com/python-kasa/python-kasa/pull/448) (@rytilahti)
 
 ## [0.5.1](https://github.com/python-kasa/python-kasa/tree/0.5.1) (2023-02-18)
```

### Comparing `python_kasa-0.5.2/LICENSE` & `python_kasa-0.5.3/LICENSE`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/README.md` & `python_kasa-0.5.3/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -141,14 +141,15 @@
 * EP10
 
 ### Power Strips
 
 * EP40
 * HS300
 * KP303
+* KP200 (in wall)
 * KP400
 * KP405 (dimmer)
 
 ### Wall switches
 
 * ES20M
 * HS200
```

### Comparing `python_kasa-0.5.2/kasa/__init__.py` & `python_kasa-0.5.3/kasa/__init__.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/cli.py` & `python_kasa-0.5.3/kasa/cli.py`

 * *Files 2% similar despite different names*

```diff
@@ -96,14 +96,20 @@
 @click.option(
     "--host",
     envvar="KASA_HOST",
     required=False,
     help="The host name or IP address of the device to connect to.",
 )
 @click.option(
+    "--port",
+    envvar="KASA_PORT",
+    required=False,
+    help="The port of the device to connect to.",
+)
+@click.option(
     "--alias",
     envvar="KASA_NAME",
     required=False,
     help="The device name, or alias, of the device to connect to.",
 )
 @click.option(
     "--target",
@@ -121,15 +127,15 @@
     type=click.Choice(list(TYPE_TO_CLASS), case_sensitive=False),
 )
 @click.option(
     "--json", default=False, is_flag=True, help="Output raw device response as JSON."
 )
 @click.version_option(package_name="python-kasa")
 @click.pass_context
-async def cli(ctx, host, alias, target, debug, type, json):
+async def cli(ctx, host, port, alias, target, debug, type, json):
     """A tool for controlling TP-Link smart home devices."""  # noqa
     # no need to perform any checks if we are just displaying the help
     if sys.argv[-1] == "--help":
         # Context object is required to avoid crashing on sub-groups
         ctx.obj = SmartDevice(None)
         return
 
@@ -175,15 +181,15 @@
         echo("No host name given, trying discovery..")
         return await ctx.invoke(discover)
 
     if type is not None:
         dev = TYPE_TO_CLASS[type](host)
     else:
         echo("No --type defined, discovering..")
-        dev = await Discover.discover_single(host)
+        dev = await Discover.discover_single(host, port=port)
 
     await dev.update()
     ctx.obj = dev
 
     if ctx.invoked_subcommand is None:
         return await ctx.invoke(state)
 
@@ -271,14 +277,15 @@
 
 @cli.command()
 @pass_dev
 async def state(dev: SmartDevice):
     """Print out device state and versions."""
     echo(f"[bold]== {dev.alias} - {dev.model} ==[/bold]")
     echo(f"\tHost: {dev.host}")
+    echo(f"\tPort: {dev.port}")
     echo(f"\tDevice state: {dev.is_on}")
     if dev.is_strip:
         echo("\t[bold]== Plugs ==[/bold]")
         for plug in dev.children:  # type: ignore
             echo(f"\t* Socket '{plug.alias}' state: {plug.is_on} since {plug.on_since}")
         echo()
```

### Comparing `python_kasa-0.5.2/kasa/discover.py` & `python_kasa-0.5.3/kasa/discover.py`

 * *Files 2% similar despite different names*

```diff
@@ -189,27 +189,27 @@
             transport.close()
 
         _LOGGER.debug("Discovered %s devices", len(protocol.discovered_devices))
 
         return protocol.discovered_devices
 
     @staticmethod
-    async def discover_single(host: str) -> SmartDevice:
+    async def discover_single(host: str, *, port: Optional[int] = None) -> SmartDevice:
         """Discover a single device by the given IP address.
 
         :param host: Hostname of device to query
         :rtype: SmartDevice
         :return: Object for querying/controlling found device.
         """
-        protocol = TPLinkSmartHomeProtocol(host)
+        protocol = TPLinkSmartHomeProtocol(host, port=port)
 
         info = await protocol.query(Discover.DISCOVERY_QUERY)
 
         device_class = Discover._get_device_class(info)
-        dev = device_class(host)
+        dev = device_class(host, port=port)
         await dev.update()
 
         return dev
 
     @staticmethod
     def _get_device_class(info: dict) -> Type[SmartDevice]:
         """Find SmartDevice subclass for device described by passed data."""
```

### Comparing `python_kasa-0.5.2/kasa/effects.py` & `python_kasa-0.5.3/kasa/effects.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/emeterstatus.py` & `python_kasa-0.5.3/kasa/emeterstatus.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/modules/__init__.py` & `python_kasa-0.5.3/kasa/modules/__init__.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/modules/ambientlight.py` & `python_kasa-0.5.3/kasa/modules/ambientlight.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/modules/cloud.py` & `python_kasa-0.5.3/kasa/modules/cloud.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/modules/emeter.py` & `python_kasa-0.5.3/kasa/modules/emeter.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/modules/module.py` & `python_kasa-0.5.3/kasa/modules/module.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/modules/motion.py` & `python_kasa-0.5.3/kasa/modules/motion.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/modules/rulemodule.py` & `python_kasa-0.5.3/kasa/modules/rulemodule.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/modules/time.py` & `python_kasa-0.5.3/kasa/modules/time.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/modules/usage.py` & `python_kasa-0.5.3/kasa/modules/usage.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/protocol.py` & `python_kasa-0.5.3/kasa/protocol.py`

 * *Files 9% similar despite different names*

```diff
@@ -13,14 +13,18 @@
 import contextlib
 import errno
 import logging
 import struct
 from pprint import pformat as pf
 from typing import Dict, Generator, Optional, Union
 
+# When support for cpython older than 3.11 is dropped
+# async_timeout can be replaced with asyncio.timeout
+from async_timeout import timeout as asyncio_timeout
+
 from .exceptions import SmartDeviceException
 from .json import dumps as json_dumps
 from .json import loads as json_loads
 
 _LOGGER = logging.getLogger(__name__)
 _NO_RETRY_ERRORS = {errno.EHOSTDOWN, errno.EHOSTUNREACH, errno.ECONNREFUSED}
 
@@ -29,17 +33,18 @@
     """Implementation of the TP-Link Smart Home protocol."""
 
     INITIALIZATION_VECTOR = 171
     DEFAULT_PORT = 9999
     DEFAULT_TIMEOUT = 5
     BLOCK_SIZE = 4
 
-    def __init__(self, host: str) -> None:
+    def __init__(self, host: str, *, port: Optional[int] = None) -> None:
         """Create a protocol object."""
         self.host = host
+        self.port = port or TPLinkSmartHomeProtocol.DEFAULT_PORT
         self.reader: Optional[asyncio.StreamReader] = None
         self.writer: Optional[asyncio.StreamWriter] = None
         self.query_lock: Optional[asyncio.Lock] = None
         self.loop: Optional[asyncio.AbstractEventLoop] = None
 
     def _detect_event_loop_change(self) -> None:
         """Check if this object has been reused betwen event loops."""
@@ -74,16 +79,18 @@
             return await self._query(request, retry_count, timeout)
 
     async def _connect(self, timeout: int) -> None:
         """Try to connect or reconnect to the device."""
         if self.writer:
             return
         self.reader = self.writer = None
-        task = asyncio.open_connection(self.host, TPLinkSmartHomeProtocol.DEFAULT_PORT)
-        self.reader, self.writer = await asyncio.wait_for(task, timeout=timeout)
+
+        task = asyncio.open_connection(self.host, self.port)
+        async with asyncio_timeout(timeout):
+            self.reader, self.writer = await task
 
     async def _execute_query(self, request: str) -> Dict:
         """Execute a query on the device and wait for the response."""
         assert self.writer is not None
         assert self.reader is not None
         debug_log = _LOGGER.isEnabledFor(logging.DEBUG)
 
@@ -129,44 +136,43 @@
         #
         for retry in range(retry_count + 1):
             try:
                 await self._connect(timeout)
             except ConnectionRefusedError as ex:
                 await self.close()
                 raise SmartDeviceException(
-                    f"Unable to connect to the device: {self.host}: {ex}"
+                    f"Unable to connect to the device: {self.host}:{self.port}: {ex}"
                 )
             except OSError as ex:
                 await self.close()
                 if ex.errno in _NO_RETRY_ERRORS or retry >= retry_count:
                     raise SmartDeviceException(
-                        f"Unable to connect to the device: {self.host}: {ex}"
+                        f"Unable to connect to the device: {self.host}:{self.port}: {ex}"
                     )
                 continue
             except Exception as ex:
                 await self.close()
                 if retry >= retry_count:
                     _LOGGER.debug("Giving up on %s after %s retries", self.host, retry)
                     raise SmartDeviceException(
-                        f"Unable to connect to the device: {self.host}: {ex}"
+                        f"Unable to connect to the device: {self.host}:{self.port}: {ex}"
                     )
                 continue
 
             try:
                 assert self.reader is not None
                 assert self.writer is not None
-                return await asyncio.wait_for(
-                    self._execute_query(request), timeout=timeout
-                )
+                async with asyncio_timeout(timeout):
+                    return await self._execute_query(request)
             except Exception as ex:
                 await self.close()
                 if retry >= retry_count:
                     _LOGGER.debug("Giving up on %s after %s retries", self.host, retry)
                     raise SmartDeviceException(
-                        f"Unable to query the device {self.host}: {ex}"
+                        f"Unable to query the device {self.host}:{self.port}: {ex}"
                     ) from ex
 
                 _LOGGER.debug(
                     "Unable to query the device %s, retrying: %s", self.host, ex
                 )
 
         # make mypy happy, this should never be reached..
```

### Comparing `python_kasa-0.5.2/kasa/smartbulb.py` & `python_kasa-0.5.3/kasa/smartbulb.py`

 * *Files 1% similar despite different names*

```diff
@@ -195,16 +195,16 @@
 
     """
 
     LIGHT_SERVICE = "smartlife.iot.smartbulb.lightingservice"
     SET_LIGHT_METHOD = "transition_light_state"
     emeter_type = "smartlife.iot.common.emeter"
 
-    def __init__(self, host: str) -> None:
-        super().__init__(host=host)
+    def __init__(self, host: str, *, port: Optional[int] = None) -> None:
+        super().__init__(host=host, port=port)
         self._device_type = DeviceType.Bulb
         self.add_module("schedule", Schedule(self, "smartlife.iot.common.schedule"))
         self.add_module("usage", Usage(self, "smartlife.iot.common.schedule"))
         self.add_module("antitheft", Antitheft(self, "smartlife.iot.common.anti_theft"))
         self.add_module("time", Time(self, "smartlife.iot.common.timesetting"))
         self.add_module("emeter", Emeter(self, self.emeter_type))
         self.add_module("countdown", Countdown(self, "countdown"))
```

### Comparing `python_kasa-0.5.2/kasa/smartdevice.py` & `python_kasa-0.5.3/kasa/smartdevice.py`

 * *Files 1% similar despite different names*

```diff
@@ -187,22 +187,23 @@
         >>> asyncio.run(dev.get_emeter_daily(year=2016, month=11))
         {24: 0.026, 25: 0.109}
 
     """
 
     emeter_type = "emeter"
 
-    def __init__(self, host: str) -> None:
+    def __init__(self, host: str, *, port: Optional[int] = None) -> None:
         """Create a new SmartDevice instance.
 
         :param str host: host name or ip address on which the device listens
         """
         self.host = host
+        self.port = port
 
-        self.protocol = TPLinkSmartHomeProtocol(host)
+        self.protocol = TPLinkSmartHomeProtocol(host, port=port)
         _LOGGER.debug("Initializing %s of type %s", self.host, type(self))
         self._device_type = DeviceType.Unknown
         # TODO: typing Any is just as using Optional[Dict] would require separate checks in
         #       accessors. the @updated_required decorator does not ensure mypy that these
         #       are not accessed incorrectly.
         self._last_update: Any = None
         self._sys_info: Any = None  # TODO: this is here to avoid changing tests
```

### Comparing `python_kasa-0.5.2/kasa/smartdimmer.py` & `python_kasa-0.5.3/kasa/smartdimmer.py`

 * *Files 1% similar despite different names*

```diff
@@ -58,16 +58,16 @@
     50
 
     Refer to :class:`SmartPlug` for the full API.
     """
 
     DIMMER_SERVICE = "smartlife.iot.dimmer"
 
-    def __init__(self, host: str) -> None:
-        super().__init__(host)
+    def __init__(self, host: str, *, port: Optional[int] = None) -> None:
+        super().__init__(host, port=port)
         self._device_type = DeviceType.Dimmer
         # TODO: need to be verified if it's okay to call these on HS220 w/o these
         # TODO: need to be figured out what's the best approach to detect support for these
         self.add_module("motion", Motion(self, "smartlife.iot.PIR"))
         self.add_module("ambient", AmbientLight(self, "smartlife.iot.LAS"))
 
     @property  # type: ignore
```

### Comparing `python_kasa-0.5.2/kasa/smartlightstrip.py` & `python_kasa-0.5.3/kasa/smartlightstrip.py`

 * *Files 2% similar despite different names*

```diff
@@ -37,16 +37,16 @@
 
     See :class:`SmartBulb` for more examples.
     """
 
     LIGHT_SERVICE = "smartlife.iot.lightStrip"
     SET_LIGHT_METHOD = "set_light_state"
 
-    def __init__(self, host: str) -> None:
-        super().__init__(host)
+    def __init__(self, host: str, *, port: Optional[int] = None) -> None:
+        super().__init__(host, port=port)
         self._device_type = DeviceType.LightStrip
 
     @property  # type: ignore
     @requires_update
     def length(self) -> int:
         """Return length of the strip."""
         return self.sys_info["length"]
```

### Comparing `python_kasa-0.5.2/kasa/smartplug.py` & `python_kasa-0.5.3/kasa/smartplug.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 """Module for smart plugs (HS100, HS110, ..)."""
 import logging
-from typing import Any, Dict
+from typing import Any, Dict, Optional
 
 from kasa.modules import Antitheft, Cloud, Schedule, Time, Usage
 from kasa.smartdevice import DeviceType, SmartDevice, requires_update
 
 _LOGGER = logging.getLogger(__name__)
 
 
@@ -33,16 +33,16 @@
         >>> asyncio.run(plug.update())
         >>> plug.led
         True
 
     For more examples, see the :class:`SmartDevice` class.
     """
 
-    def __init__(self, host: str) -> None:
-        super().__init__(host)
+    def __init__(self, host: str, *, port: Optional[int] = None) -> None:
+        super().__init__(host, port=port)
         self._device_type = DeviceType.Plug
         self.add_module("schedule", Schedule(self, "schedule"))
         self.add_module("usage", Usage(self, "schedule"))
         self.add_module("antitheft", Antitheft(self, "anti_theft"))
         self.add_module("time", Time(self, "time"))
         self.add_module("cloud", Cloud(self, "cnCloud"))
```

### Comparing `python_kasa-0.5.2/kasa/smartstrip.py` & `python_kasa-0.5.3/kasa/smartstrip.py`

 * *Files 0% similar despite different names*

```diff
@@ -75,16 +75,16 @@
         >>> asyncio.run(strip.update())
         >>> strip.is_on
         True
 
     For more examples, see the :class:`SmartDevice` class.
     """
 
-    def __init__(self, host: str) -> None:
-        super().__init__(host=host)
+    def __init__(self, host: str, *, port: Optional[int] = None) -> None:
+        super().__init__(host=host, port=port)
         self.emeter_type = "emeter"
         self._device_type = DeviceType.Strip
         self.add_module("antitheft", Antitheft(self, "anti_theft"))
         self.add_module("schedule", Schedule(self, "schedule"))
         self.add_module("usage", Usage(self, "schedule"))
         self.add_module("time", Time(self, "time"))
         self.add_module("countdown", Countdown(self, "countdown"))
```

### Comparing `python_kasa-0.5.2/kasa/tests/conftest.py` & `python_kasa-0.5.3/kasa/tests/conftest.py`

 * *Files 0% similar despite different names*

```diff
@@ -51,15 +51,15 @@
     "KP100",
     "KP105",
     "KP115",
     "KP125",
     "KP401",
     "KS200M",
 }
-STRIPS = {"HS107", "HS300", "KP303", "KP400", "EP40"}
+STRIPS = {"HS107", "HS300", "KP303", "KP200", "KP400", "EP40"}
 DIMMERS = {"ES20M", "HS220", "KS220M", "KS230", "KP405"}
 
 DIMMABLE = {*BULBS, *DIMMERS}
 WITH_EMETER = {"HS110", "HS300", "KP115", "KP125", *BULBS}
 
 ALL_DEVICES = BULBS.union(PLUGS).union(STRIPS).union(DIMMERS)
```

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/EP10(US)_1.0_1.0.2.json` & `python_kasa-0.5.3/kasa/tests/fixtures/EP10(US)_1.0_1.0.2.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/EP40(US)_1.0_1.0.2.json` & `python_kasa-0.5.3/kasa/tests/fixtures/EP40(US)_1.0_1.0.2.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/ES20M(US)_1.0_1.0.8.json` & `python_kasa-0.5.3/kasa/tests/fixtures/ES20M(US)_1.0_1.0.8.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS100(US)_1.0_1.2.5.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS100(US)_1.0_1.2.5.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS100(US)_2.0_1.5.6.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS100(US)_2.0_1.5.6.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS103(US)_1.0_1.5.7.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS103(US)_1.0_1.5.7.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS103(US)_2.1_1.1.2.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS103(US)_2.1_1.1.2.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS103(US)_2.1_1.1.4.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS103(US)_2.1_1.1.4.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS105(US)_1.0_1.5.6.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS105(US)_1.0_1.5.6.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS105(US)_1.0_mocked.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS105(US)_1.0_mocked.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS107(US)_1.0_1.0.8.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS107(US)_1.0_1.0.8.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS110(EU)_1.0_1.2.5.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS110(EU)_1.0_1.2.5.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS110(EU)_2.0_mocked.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS110(EU)_2.0_mocked.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS110(US)_1.0_mocked.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS110(US)_1.0_mocked.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS200(US)_1.0_mocked.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS200(US)_1.0_mocked.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS200(US)_2.0_1.5.7.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS200(US)_2.0_1.5.7.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS200(US)_5.0_1.0.2.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS200(US)_5.0_1.0.2.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS210(US)_1.0_1.5.8.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS210(US)_1.0_1.5.8.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS220(US)_1.0_1.5.7.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS220(US)_1.0_1.5.7.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS220(US)_1.0_mocked.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS220(US)_1.0_mocked.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS220(US)_2.0_1.0.3.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS220(US)_2.0_1.0.3.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS300(US)_1.0_1.0.10.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS300(US)_1.0_1.0.10.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/HS300(US)_2.0_1.0.3.json` & `python_kasa-0.5.3/kasa/tests/fixtures/HS300(US)_2.0_1.0.3.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL110(US)_1.0_1.8.11.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL110(US)_1.0_1.8.11.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL120(US)_1.0_1.8.6.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL120(US)_1.0_1.8.6.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL125(US)_1.20_1.0.5.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL125(US)_1.20_1.0.5.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL125(US)_2.0_1.0.7.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL125(US)_2.0_1.0.7.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL130(EU)_1.0_1.8.8.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL130(EU)_1.0_1.8.8.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL130(US)_1.0_1.8.11.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL130(US)_1.0_1.8.11.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL135(US)_1.0_1.0.6.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL135(US)_1.0_1.0.6.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL400L5(US)_1.0_1.0.5.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL400L5(US)_1.0_1.0.5.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL400L5(US)_1.0_1.0.8.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL400L5(US)_1.0_1.0.8.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL420L5(US)_1.0_1.0.2.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL420L5(US)_1.0_1.0.2.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL430(UN)_2.0_1.0.8.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL430(UN)_2.0_1.0.8.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL430(US)_1.0_1.0.10.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL430(US)_1.0_1.0.10.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL430(US)_2.0_1.0.8.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL430(US)_2.0_1.0.8.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL430(US)_2.0_1.0.9.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL430(US)_2.0_1.0.9.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL50(US)_1.0_1.1.13.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL50(US)_1.0_1.1.13.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL60(UN)_1.0_1.1.4.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL60(UN)_1.0_1.1.4.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KL60(US)_1.0_1.1.13.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KL60(US)_1.0_1.1.13.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP100(US)_3.0_1.0.1.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP100(US)_3.0_1.0.1.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP105(UK)_1.0_1.0.7.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP105(UK)_1.0_1.0.7.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP115(EU)_1.0_1.0.16.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP115(EU)_1.0_1.0.16.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP115(US)_1.0_1.0.17.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP115(US)_1.0_1.0.17.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP125(US)_1.0_1.0.6.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP125(US)_1.0_1.0.6.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP303(UK)_1.0_1.0.3.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP303(UK)_1.0_1.0.3.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP303(US)_2.0_1.0.3.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP303(US)_2.0_1.0.3.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP400(US)_1.0_1.0.10.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP400(US)_1.0_1.0.10.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP400(US)_2.0_1.0.6.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP400(US)_2.0_1.0.6.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP401(US)_1.0_1.0.0.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP401(US)_1.0_1.0.0.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KP405(US)_1.0_1.0.5.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KP405(US)_1.0_1.0.5.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KS200M(US)_1.0_1.0.8.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KS200M(US)_1.0_1.0.8.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KS220M(US)_1.0_1.0.4.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KS220M(US)_1.0_1.0.4.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/KS230(US)_1.0_1.0.14.json` & `python_kasa-0.5.3/kasa/tests/fixtures/KS230(US)_1.0_1.0.14.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/LB100(US)_1.0_mocked.json` & `python_kasa-0.5.3/kasa/tests/fixtures/LB100(US)_1.0_mocked.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/LB110(US)_1.0_1.8.11.json` & `python_kasa-0.5.3/kasa/tests/fixtures/LB110(US)_1.0_1.8.11.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/LB120(US)_1.0_mocked.json` & `python_kasa-0.5.3/kasa/tests/fixtures/LB120(US)_1.0_mocked.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/fixtures/LB130(US)_1.0_mocked.json` & `python_kasa-0.5.3/kasa/tests/fixtures/LB130(US)_1.0_mocked.json`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/newfakes.py` & `python_kasa-0.5.3/kasa/tests/newfakes.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_bulb.py` & `python_kasa-0.5.3/kasa/tests/test_bulb.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_cli.py` & `python_kasa-0.5.3/kasa/tests/test_cli.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_dimmer.py` & `python_kasa-0.5.3/kasa/tests/test_dimmer.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_discovery.py` & `python_kasa-0.5.3/kasa/tests/test_discovery.py`

 * *Files 3% similar despite different names*

```diff
@@ -48,20 +48,22 @@
 
 async def test_type_unknown():
     invalid_info = {"system": {"get_sysinfo": {"type": "nosuchtype"}}}
     with pytest.raises(SmartDeviceException):
         Discover._get_device_class(invalid_info)
 
 
-async def test_discover_single(discovery_data: dict, mocker):
+@pytest.mark.parametrize("custom_port", [123, None])
+async def test_discover_single(discovery_data: dict, mocker, custom_port):
     """Make sure that discover_single returns an initialized SmartDevice instance."""
     mocker.patch("kasa.TPLinkSmartHomeProtocol.query", return_value=discovery_data)
-    x = await Discover.discover_single("127.0.0.1")
+    x = await Discover.discover_single("127.0.0.1", port=custom_port)
     assert issubclass(x.__class__, SmartDevice)
     assert x._sys_info is not None
+    assert x.port == custom_port
 
 
 INVALIDS = [
     ("No 'system' or 'get_sysinfo' in response", {"no": "data"}),
     (
         "Unable to find the device type field",
         {"system": {"get_sysinfo": {"missing_type": 1}}},
```

### Comparing `python_kasa-0.5.2/kasa/tests/test_emeter.py` & `python_kasa-0.5.3/kasa/tests/test_emeter.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_lightstrip.py` & `python_kasa-0.5.3/kasa/tests/test_lightstrip.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_plug.py` & `python_kasa-0.5.3/kasa/tests/test_plug.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_protocol.py` & `python_kasa-0.5.3/kasa/tests/test_protocol.py`

 * *Files 3% similar despite different names*

```diff
@@ -125,14 +125,44 @@
     assert response == {"great": "success"}
     if log_level == logging.DEBUG:
         assert "success" in caplog.text
     else:
         assert "success" not in caplog.text
 
 
+@pytest.mark.parametrize("custom_port", [123, None])
+async def test_protocol_custom_port(mocker, custom_port):
+    encrypted = TPLinkSmartHomeProtocol.encrypt('{"great":"success"}')[
+        TPLinkSmartHomeProtocol.BLOCK_SIZE :
+    ]
+
+    async def _mock_read(byte_count):
+        nonlocal encrypted
+        if byte_count == TPLinkSmartHomeProtocol.BLOCK_SIZE:
+            return struct.pack(">I", len(encrypted))
+        if byte_count == len(encrypted):
+            return encrypted
+        raise ValueError(f"No mock for {byte_count}")
+
+    def aio_mock_writer(_, port):
+        reader = mocker.patch("asyncio.StreamReader")
+        writer = mocker.patch("asyncio.StreamWriter")
+        if custom_port is None:
+            assert port == 9999
+        else:
+            assert port == custom_port
+        mocker.patch.object(reader, "readexactly", _mock_read)
+        return reader, writer
+
+    protocol = TPLinkSmartHomeProtocol("127.0.0.1", port=custom_port)
+    mocker.patch("asyncio.open_connection", side_effect=aio_mock_writer)
+    response = await protocol.query({})
+    assert response == {"great": "success"}
+
+
 def test_encrypt():
     d = json.dumps({"foo": 1, "bar": 2})
     encrypted = TPLinkSmartHomeProtocol.encrypt(d)
     # encrypt adds a 4 byte header
     encrypted = encrypted[4:]
     assert d == TPLinkSmartHomeProtocol.decrypt(encrypted)
```

### Comparing `python_kasa-0.5.2/kasa/tests/test_readme_examples.py` & `python_kasa-0.5.3/kasa/tests/test_readme_examples.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_smartdevice.py` & `python_kasa-0.5.3/kasa/tests/test_smartdevice.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_strip.py` & `python_kasa-0.5.3/kasa/tests/test_strip.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/kasa/tests/test_usage.py` & `python_kasa-0.5.3/kasa/tests/test_usage.py`

 * *Files identical despite different names*

### Comparing `python_kasa-0.5.2/pyproject.toml` & `python_kasa-0.5.3/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "python-kasa"
-version = "0.5.2"
+version = "0.5.3"
 description = "Python API for TP-Link Kasa Smarthome devices"
 license = "GPL-3.0-or-later"
 authors = ["python-kasa developers"]
 repository = "https://github.com/python-kasa/python-kasa"
 readme = "README.md"
 packages = [
   { include = "kasa" }
@@ -30,14 +30,15 @@
 
 # required only for docs
 sphinx = { version = "^4", optional = true }
 sphinx_rtd_theme = { version = "^0", optional = true }
 sphinxcontrib-programoutput = { version = "^0", optional = true }
 myst-parser = { version = "*", optional = true }
 docutils = { version = ">=0.17", optional = true }
+async-timeout = ">=3.0.0"
 
 [tool.poetry.dev-dependencies]
 pytest = "*"
 pytest-cov = "*"
 pytest-asyncio = "*"
 pytest-sugar = "*"
 pre-commit = "*"
```

### Comparing `python_kasa-0.5.2/PKG-INFO` & `python_kasa-0.5.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,24 +1,25 @@
 Metadata-Version: 2.1
 Name: python-kasa
-Version: 0.5.2
+Version: 0.5.3
 Summary: Python API for TP-Link Kasa Smarthome devices
 Home-page: https://github.com/python-kasa/python-kasa
 License: GPL-3.0-or-later
 Author: python-kasa developers
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Provides-Extra: docs
 Provides-Extra: speedups
 Requires-Dist: anyio
+Requires-Dist: async-timeout (>=3.0.0)
 Requires-Dist: asyncclick (>=8)
 Requires-Dist: docutils (>=0.17) ; extra == "docs"
 Requires-Dist: kasa-crypt (>=0.2.0) ; extra == "speedups"
 Requires-Dist: myst-parser ; extra == "docs"
 Requires-Dist: orjson (>=3.9.1) ; extra == "speedups"
 Requires-Dist: pydantic (>=1,<2)
 Requires-Dist: sphinx (>=4,<5) ; extra == "docs"
@@ -172,14 +173,15 @@
 * EP10
 
 ### Power Strips
 
 * EP40
 * HS300
 * KP303
+* KP200 (in wall)
 * KP400
 * KP405 (dimmer)
 
 ### Wall switches
 
 * ES20M
 * HS200
```

