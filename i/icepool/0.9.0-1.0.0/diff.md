# Comparing `tmp/icepool-0.9.0.tar.gz` & `tmp/icepool-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "icepool-0.9.0.tar", last modified: Fri Apr 29 06:48:01 2022, max compression
+gzip compressed data, was "icepool-1.0.0.tar", last modified: Sat Jul 22 22:54:38 2023, max compression
```

## Comparing `icepool-0.9.0.tar` & `icepool-1.0.0.tar`

### file list

```diff
@@ -1,30 +1,59 @@
-drwxrwxrwx   0        0        0        0 2022-04-29 06:48:01.884327 icepool-0.9.0/
--rw-rw-rw-   0        0        0     1111 2022-04-16 23:05:39.000000 icepool-0.9.0/LICENSE.md
--rw-rw-rw-   0        0        0     4572 2022-04-29 06:48:01.884327 icepool-0.9.0/PKG-INFO
--rw-rw-rw-   0        0        0     3879 2022-04-24 06:44:50.000000 icepool-0.9.0/README.md
--rw-rw-rw-   0        0        0      110 2022-04-16 23:05:39.000000 icepool-0.9.0/pyproject.toml
--rw-rw-rw-   0        0        0      766 2022-04-29 06:48:01.896294 icepool-0.9.0/setup.cfg
-drwxrwxrwx   0        0        0        0 2022-04-29 06:48:01.845431 icepool-0.9.0/src/
-drwxrwxrwx   0        0        0        0 2022-04-29 06:48:01.857399 icepool-0.9.0/src/icepool/
--rw-rw-rw-   0        0        0     2313 2022-04-28 06:35:11.000000 icepool-0.9.0/src/icepool/__init__.py
--rw-rw-rw-   0        0        0     1983 2022-04-18 04:20:10.000000 icepool-0.9.0/src/icepool/collections.py
-drwxrwxrwx   0        0        0        0 2022-04-29 06:48:01.877345 icepool-0.9.0/src/icepool/die/
--rw-rw-rw-   0        0        0        0 2022-04-16 23:05:39.000000 icepool-0.9.0/src/icepool/die/__init__.py
--rw-rw-rw-   0        0        0    39366 2022-04-29 06:38:50.000000 icepool-0.9.0/src/icepool/die/base.py
--rw-rw-rw-   0        0        0    10773 2022-04-29 05:26:01.000000 icepool-0.9.0/src/icepool/die/create.py
--rw-rw-rw-   0        0        0     1044 2022-04-28 07:04:05.000000 icepool-0.9.0/src/icepool/die/empty.py
--rw-rw-rw-   0        0        0     5498 2022-04-28 06:33:19.000000 icepool-0.9.0/src/icepool/die/func.py
--rw-rw-rw-   0        0        0     8374 2022-04-28 06:57:16.000000 icepool-0.9.0/src/icepool/die/scalar.py
--rw-rw-rw-   0        0        0     7094 2022-04-28 06:57:17.000000 icepool-0.9.0/src/icepool/die/vector.py
--rw-rw-rw-   0        0        0      433 2022-04-16 23:05:39.000000 icepool-0.9.0/src/icepool/math.py
-drwxrwxrwx   0        0        0        0 2022-04-29 06:48:01.883329 icepool-0.9.0/src/icepool/pool/
--rw-rw-rw-   0        0        0        0 2022-04-17 22:24:24.000000 icepool-0.9.0/src/icepool/pool/__init__.py
--rw-rw-rw-   0        0        0     3834 2022-04-25 04:17:29.000000 icepool-0.9.0/src/icepool/pool/base.py
--rw-rw-rw-   0        0        0    18327 2022-04-25 04:11:13.000000 icepool-0.9.0/src/icepool/pool/eval.py
--rw-rw-rw-   0        0        0    26877 2022-04-25 04:15:15.000000 icepool-0.9.0/src/icepool/pool/pool.py
--rw-rw-rw-   0        0        0     2861 2022-04-25 04:13:58.000000 icepool-0.9.0/src/icepool/pool/roll.py
-drwxrwxrwx   0        0        0        0 2022-04-29 06:48:01.869366 icepool-0.9.0/src/icepool.egg-info/
--rw-rw-rw-   0        0        0     4572 2022-04-29 06:48:01.000000 icepool-0.9.0/src/icepool.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      564 2022-04-29 06:48:01.000000 icepool-0.9.0/src/icepool.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-04-29 06:48:01.000000 icepool-0.9.0/src/icepool.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2022-04-29 06:48:01.000000 icepool-0.9.0/src/icepool.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:38.806561 icepool-1.0.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1101 2023-07-22 22:54:24.000000 icepool-1.0.0/LICENSE.md
+-rw-r--r--   0 runner    (1001) docker     (123)    10576 2023-07-22 22:54:38.806561 icepool-1.0.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9759 2023-07-22 22:54:24.000000 icepool-1.0.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      104 2023-07-22 22:54:24.000000 icepool-1.0.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      893 2023-07-22 22:54:38.810561 icepool-1.0.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:38.798561 icepool-1.0.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:38.798561 icepool-1.0.0/src/icepool/
+-rw-r--r--   0 runner    (1001) docker     (123)     4182 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:38.802561 icepool-1.0.0/src/icepool/collection/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/collection/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5644 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/collection/counts.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13084 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/collection/vector.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3952 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/creation_args.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:38.802561 icepool-1.0.0/src/icepool/evaluator/
+-rw-r--r--   0 runner    (1001) docker     (123)     1761 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3392 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/basic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5134 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/compair.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3082 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/comparison.py
+-rw-r--r--   0 runner    (1001) docker     (123)      587 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/constant.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4378 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/expression.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4554 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/joint.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2232 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/keep.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19816 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/multiset_evaluator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5712 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/evaluator/poker.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:38.806561 icepool-1.0.0/src/icepool/expression/
+-rw-r--r--   0 runner    (1001) docker     (123)     1301 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/expression/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5203 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/expression/adjust_counts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4081 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/expression/binary_operator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5550 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/expression/filter_outcomes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7278 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/expression/keep.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33282 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/expression/multiset_expression.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4590 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/expression/multiset_function.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1287 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/expression/variable.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22522 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/function.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:38.806561 icepool-1.0.0/src/icepool/generator/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/generator/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1725 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/generator/alignment.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5273 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/generator/deal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7947 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/generator/multiset_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27209 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/generator/pool.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2991 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/generator/pool_cost.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1668 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/math.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:38.806561 icepool-1.0.0/src/icepool/population/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/population/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8598 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/population/again.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23604 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/population/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6126 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/population/deck.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44674 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/population/die.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2122 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/population/die_with_truth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8322 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/population/format.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6329 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/population/keep.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6383 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/population/markov_chain.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3607 2023-07-22 22:54:24.000000 icepool-1.0.0/src/icepool/typing.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:54:38.802561 icepool-1.0.0/src/icepool.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    10576 2023-07-22 22:54:38.000000 icepool-1.0.0/src/icepool.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-07-22 22:54:38.000000 icepool-1.0.0/src/icepool.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 22:54:38.000000 icepool-1.0.0/src/icepool.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-22 22:54:38.000000 icepool-1.0.0/src/icepool.egg-info/top_level.txt
```

### Comparing `icepool-0.9.0/LICENSE.md` & `icepool-1.0.0/LICENSE.md`

 * *Ordering differences only*

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-MIT License
-
-Copyright © 2021-2022, Albert Julius Liu.
-All rights reserved.
-
-Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
-
-The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
-
-THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
+MIT License
+
+Copyright © 2021-2022, Albert Julius Liu.
+All rights reserved.
+
+Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
+
+The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
+
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

