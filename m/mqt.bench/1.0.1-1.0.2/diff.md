# Comparing `tmp/mqt.bench-1.0.1.tar.gz` & `tmp/mqt.bench-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mqt.bench-1.0.1.tar", last modified: Tue Jul 18 06:32:22 2023, max compression
+gzip compressed data, was "mqt.bench-1.0.2.tar", last modified: Sun Jul 23 19:21:22 2023, max compression
```

## Comparing `mqt.bench-1.0.1.tar` & `mqt.bench-1.0.2.tar`

### file list

```diff
@@ -1,110 +1,110 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.580695 mqt.bench-1.0.1/
--rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.git_archival.txt
--rw-r--r--   0 runner    (1001) docker     (123)       31 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.gitattributes
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.540694 mqt.bench-1.0.1/.github/
--rw-r--r--   0 runner    (1001) docker     (123)      243 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.github/codecov.yml
--rw-r--r--   0 runner    (1001) docker     (123)      820 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.github/dependabot.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1040 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.github/release-drafter.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.540694 mqt.bench-1.0.1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      928 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.github/workflows/codeql.yml
--rw-r--r--   0 runner    (1001) docker     (123)      821 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.github/workflows/coverage.yml
--rw-r--r--   0 runner    (1001) docker     (123)     3135 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.github/workflows/deploy.yml
--rw-r--r--   0 runner    (1001) docker     (123)      493 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.github/workflows/mypy.yml
--rw-r--r--   0 runner    (1001) docker     (123)      467 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.github/workflows/release-drafter.yml
--rw-r--r--   0 runner    (1001) docker     (123)     4972 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     2386 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      135 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)    16307 2023-07-18 06:32:22.580695 mqt.bench-1.0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    13651 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     4272 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/config.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.544694 mqt.bench-1.0.1/img/
--rw-r--r--   0 runner    (1001) docker     (123)    21005 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/img/arch.png
--rw-r--r--   0 runner    (1001) docker     (123)    86005 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/img/level_1.png
--rw-r--r--   0 runner    (1001) docker     (123)    84500 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/img/level_2.png
--rw-r--r--   0 runner    (1001) docker     (123)    76051 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/img/level_3.png
--rw-r--r--   0 runner    (1001) docker     (123)   112485 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/img/level_4.png
--rw-r--r--   0 runner    (1001) docker     (123)    61137 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/img/mqt_dark.png
--rw-r--r--   0 runner    (1001) docker     (123)    57266 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/img/mqt_light.png
--rw-r--r--   0 runner    (1001) docker     (123)   196044 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/img/mqtbench.png
--rw-r--r--   0 runner    (1001) docker     (123)     4549 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-18 06:32:22.580695 mqt.bench-1.0.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.536694 mqt.bench-1.0.1/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.536694 mqt.bench-1.0.1/src/mqt/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.548694 mqt.bench-1.0.1/src/mqt/bench/
--rw-r--r--   0 runner    (1001) docker     (123)      460 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17832 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmark_generator.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.552694 mqt.bench-1.0.1/src/mqt/bench/benchmarks/
--rw-r--r--   0 runner    (1001) docker     (123)      470 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1988 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/ae.py
--rw-r--r--   0 runner    (1001) docker     (123)     1944 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/dj.py
--rw-r--r--   0 runner    (1001) docker     (123)      528 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/ghz.py
--rw-r--r--   0 runner    (1001) docker     (123)      693 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/graphstate.py
--rw-r--r--   0 runner    (1001) docker     (123)     1414 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/grover.py
--rw-r--r--   0 runner    (1001) docker     (123)     1162 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qaoa.py
--rw-r--r--   0 runner    (1001) docker     (123)      608 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qft.py
--rw-r--r--   0 runner    (1001) docker     (123)      692 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qftentangled.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.552694 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_finance/
--rw-r--r--   0 runner    (1001) docker     (123)     1966 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_finance/portfolioqaoa.py
--rw-r--r--   0 runner    (1001) docker     (123)     2079 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_finance/portfoliovqe.py
--rw-r--r--   0 runner    (1001) docker     (123)     2362 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_finance/pricingcall.py
--rw-r--r--   0 runner    (1001) docker     (123)     2907 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_finance/pricingput.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.552694 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_ml/
--rw-r--r--   0 runner    (1001) docker     (123)      987 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_ml/qnn.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.552694 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_nature/
--rw-r--r--   0 runner    (1001) docker     (123)     1973 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_nature/groundstate.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.552694 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_optimization/
--rw-r--r--   0 runner    (1001) docker     (123)     4963 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_optimization/routing.py
--rw-r--r--   0 runner    (1001) docker     (123)     1454 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_optimization/tsp.py
--rw-r--r--   0 runner    (1001) docker     (123)     1500 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qpeexact.py
--rw-r--r--   0 runner    (1001) docker     (123)     1535 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qpeinexact.py
--rw-r--r--   0 runner    (1001) docker     (123)     2980 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/qwalk.py
--rw-r--r--   0 runner    (1001) docker     (123)      719 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/random.py
--rw-r--r--   0 runner    (1001) docker     (123)      736 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/realamprandom.py
--rw-r--r--   0 runner    (1001) docker     (123)     8807 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/shor.py
--rw-r--r--   0 runner    (1001) docker     (123)      722 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/su2random.py
--rw-r--r--   0 runner    (1001) docker     (123)      731 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/twolocalrandom.py
--rw-r--r--   0 runner    (1001) docker     (123)     1287 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/vqe.py
--rw-r--r--   0 runner    (1001) docker     (123)      868 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/benchmarks/wstate.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.572695 mqt.bench-1.0.1/src/mqt/bench/evaluation/
--rw-r--r--   0 runner    (1001) docker     (123)      333 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/evaluation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2183 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/evaluation/evaluation.py
--rw-r--r--   0 runner    (1001) docker     (123) 15925096 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/evaluation/evaluation_data.pkl
--rw-r--r--   0 runner    (1001) docker     (123)     8133 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/evaluation/evaluation_visualization.ipynb
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.576695 mqt.bench-1.0.1/src/mqt/bench/evaluation/results/
--rw-r--r--   0 runner    (1001) docker     (123)    16461 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/evaluation/results/pie.pdf
--rw-r--r--   0 runner    (1001) docker     (123)    19421 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/evaluation/results/qubit_dist.pdf
--rw-r--r--   0 runner    (1001) docker     (123)    24774 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/evaluation/results/violins.pdf
--rw-r--r--   0 runner    (1001) docker     (123)       93 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)     8149 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/qiskit_helper.py
--rw-r--r--   0 runner    (1001) docker     (123)    11132 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/tket_helper.py
--rw-r--r--   0 runner    (1001) docker     (123)    12928 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/bench/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.576695 mqt.bench-1.0.1/src/mqt/benchviewer/
--rw-r--r--   0 runner    (1001) docker     (123)      232 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    26632 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/backend.py
--rw-r--r--   0 runner    (1001) docker     (123)     6257 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/main.py
--rw-r--r--   0 runner    (1001) docker     (123)       93 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.576695 mqt.bench-1.0.1/src/mqt/benchviewer/static/
--rw-r--r--   0 runner    (1001) docker     (123)     3438 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/static/favicon.ico
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.576695 mqt.bench-1.0.1/src/mqt/benchviewer/static/files/
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/static/files/MQTBench_all.zip
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.576695 mqt.bench-1.0.1/src/mqt/benchviewer/static/files/qasm_output/
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/static/files/qasm_output/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)    61137 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/static/mqt_dark.png
--rw-r--r--   0 runner    (1001) docker     (123)     1038 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/static/tum_logo.svg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.576695 mqt.bench-1.0.1/src/mqt/benchviewer/templates/
--rw-r--r--   0 runner    (1001) docker     (123)    16436 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/templates/benchmark_description.html
--rw-r--r--   0 runner    (1001) docker     (123)     7441 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/templates/description.html
--rw-r--r--   0 runner    (1001) docker     (123)    28232 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/templates/index.html
--rw-r--r--   0 runner    (1001) docker     (123)     7693 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/src/mqt/benchviewer/templates/legal.html
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.548694 mqt.bench-1.0.1/src/mqt.bench.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    16307 2023-07-18 06:32:22.000000 mqt.bench-1.0.1/src/mqt.bench.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2969 2023-07-18 06:32:22.000000 mqt.bench-1.0.1/src/mqt.bench.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-18 06:32:22.000000 mqt.bench-1.0.1/src/mqt.bench.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      179 2023-07-18 06:32:22.000000 mqt.bench-1.0.1/src/mqt.bench.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      308 2023-07-18 06:32:22.000000 mqt.bench-1.0.1/src/mqt.bench.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-18 06:32:22.000000 mqt.bench-1.0.1/src/mqt.bench.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 06:32:22.580695 mqt.bench-1.0.1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)    27066 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/tests/test_bench.py
--rw-r--r--   0 runner    (1001) docker     (123)    15180 2023-07-18 06:32:09.000000 mqt.bench-1.0.1/tests/test_benchviewer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.098525 mqt.bench-1.0.2/
+-rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.git_archival.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       31 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.gitattributes
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.066524 mqt.bench-1.0.2/.github/
+-rw-r--r--   0 runner    (1001) docker     (123)      243 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.github/codecov.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      820 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.github/dependabot.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1040 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.github/release-drafter.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.066524 mqt.bench-1.0.2/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      928 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.github/workflows/codeql.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      821 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.github/workflows/coverage.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     3135 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.github/workflows/deploy.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      493 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.github/workflows/mypy.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      467 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.github/workflows/release-drafter.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     4972 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     2363 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      135 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)    16437 2023-07-23 19:21:22.098525 mqt.bench-1.0.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    13781 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     4272 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/config.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.070525 mqt.bench-1.0.2/img/
+-rw-r--r--   0 runner    (1001) docker     (123)    21005 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/img/arch.png
+-rw-r--r--   0 runner    (1001) docker     (123)    86005 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/img/level_1.png
+-rw-r--r--   0 runner    (1001) docker     (123)    84500 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/img/level_2.png
+-rw-r--r--   0 runner    (1001) docker     (123)    76051 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/img/level_3.png
+-rw-r--r--   0 runner    (1001) docker     (123)   112485 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/img/level_4.png
+-rw-r--r--   0 runner    (1001) docker     (123)    61137 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/img/mqt_dark.png
+-rw-r--r--   0 runner    (1001) docker     (123)    57266 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/img/mqt_light.png
+-rw-r--r--   0 runner    (1001) docker     (123)   196044 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/img/mqtbench.png
+-rw-r--r--   0 runner    (1001) docker     (123)     4529 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 19:21:22.098525 mqt.bench-1.0.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.062524 mqt.bench-1.0.2/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.062524 mqt.bench-1.0.2/src/mqt/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.074524 mqt.bench-1.0.2/src/mqt/bench/
+-rw-r--r--   0 runner    (1001) docker     (123)      460 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17832 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmark_generator.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.074524 mqt.bench-1.0.2/src/mqt/bench/benchmarks/
+-rw-r--r--   0 runner    (1001) docker     (123)      470 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1988 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/ae.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1944 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/dj.py
+-rw-r--r--   0 runner    (1001) docker     (123)      528 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/ghz.py
+-rw-r--r--   0 runner    (1001) docker     (123)      693 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/graphstate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1414 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/grover.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1162 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qaoa.py
+-rw-r--r--   0 runner    (1001) docker     (123)      608 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qft.py
+-rw-r--r--   0 runner    (1001) docker     (123)      692 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qftentangled.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.078524 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_finance/
+-rw-r--r--   0 runner    (1001) docker     (123)     1966 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_finance/portfolioqaoa.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2079 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_finance/portfoliovqe.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2362 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_finance/pricingcall.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2907 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_finance/pricingput.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.078524 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_ml/
+-rw-r--r--   0 runner    (1001) docker     (123)      987 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_ml/qnn.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.078524 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_nature/
+-rw-r--r--   0 runner    (1001) docker     (123)     1973 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_nature/groundstate.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.078524 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_optimization/
+-rw-r--r--   0 runner    (1001) docker     (123)     4963 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_optimization/routing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1454 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_optimization/tsp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1500 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qpeexact.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1535 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qpeinexact.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2980 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/qwalk.py
+-rw-r--r--   0 runner    (1001) docker     (123)      719 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/random.py
+-rw-r--r--   0 runner    (1001) docker     (123)      736 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/realamprandom.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8807 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/shor.py
+-rw-r--r--   0 runner    (1001) docker     (123)      722 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/su2random.py
+-rw-r--r--   0 runner    (1001) docker     (123)      731 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/twolocalrandom.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1287 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/vqe.py
+-rw-r--r--   0 runner    (1001) docker     (123)      868 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/benchmarks/wstate.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.094525 mqt.bench-1.0.2/src/mqt/bench/evaluation/
+-rw-r--r--   0 runner    (1001) docker     (123)      333 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/evaluation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2183 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/evaluation/evaluation.py
+-rw-r--r--   0 runner    (1001) docker     (123) 15925096 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/evaluation/evaluation_data.pkl
+-rw-r--r--   0 runner    (1001) docker     (123)     8133 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/evaluation/evaluation_visualization.ipynb
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.094525 mqt.bench-1.0.2/src/mqt/bench/evaluation/results/
+-rw-r--r--   0 runner    (1001) docker     (123)    16461 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/evaluation/results/pie.pdf
+-rw-r--r--   0 runner    (1001) docker     (123)    19421 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/evaluation/results/qubit_dist.pdf
+-rw-r--r--   0 runner    (1001) docker     (123)    24774 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/evaluation/results/violins.pdf
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)     8149 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/qiskit_helper.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11132 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/tket_helper.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12928 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/bench/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.094525 mqt.bench-1.0.2/src/mqt/benchviewer/
+-rw-r--r--   0 runner    (1001) docker     (123)      232 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26632 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/backend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6257 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.098525 mqt.bench-1.0.2/src/mqt/benchviewer/static/
+-rw-r--r--   0 runner    (1001) docker     (123)     3438 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/static/favicon.ico
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.098525 mqt.bench-1.0.2/src/mqt/benchviewer/static/files/
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/static/files/MQTBench_all.zip
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.098525 mqt.bench-1.0.2/src/mqt/benchviewer/static/files/qasm_output/
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/static/files/qasm_output/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)    61137 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/static/mqt_dark.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1038 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/static/tum_logo.svg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.098525 mqt.bench-1.0.2/src/mqt/benchviewer/templates/
+-rw-r--r--   0 runner    (1001) docker     (123)    16436 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/templates/benchmark_description.html
+-rw-r--r--   0 runner    (1001) docker     (123)     7441 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/templates/description.html
+-rw-r--r--   0 runner    (1001) docker     (123)    28150 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/templates/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)     7693 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/src/mqt/benchviewer/templates/legal.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.070525 mqt.bench-1.0.2/src/mqt.bench.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    16437 2023-07-23 19:21:21.000000 mqt.bench-1.0.2/src/mqt.bench.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2969 2023-07-23 19:21:22.000000 mqt.bench-1.0.2/src/mqt.bench.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:21:21.000000 mqt.bench-1.0.2/src/mqt.bench.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      179 2023-07-23 19:21:21.000000 mqt.bench-1.0.2/src/mqt.bench.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      295 2023-07-23 19:21:21.000000 mqt.bench-1.0.2/src/mqt.bench.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-23 19:21:21.000000 mqt.bench-1.0.2/src/mqt.bench.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:21:22.098525 mqt.bench-1.0.2/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)    27066 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/tests/test_bench.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15180 2023-07-23 19:21:12.000000 mqt.bench-1.0.2/tests/test_benchviewer.py
```

### Comparing `mqt.bench-1.0.1/.github/dependabot.yml` & `mqt.bench-1.0.2/.github/dependabot.yml`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/.github/release-drafter.yml` & `mqt.bench-1.0.2/.github/release-drafter.yml`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/.github/workflows/codeql.yml` & `mqt.bench-1.0.2/.github/workflows/codeql.yml`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/.github/workflows/coverage.yml` & `mqt.bench-1.0.2/.github/workflows/coverage.yml`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/.github/workflows/deploy.yml` & `mqt.bench-1.0.2/.github/workflows/deploy.yml`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/.gitignore` & `mqt.bench-1.0.2/.gitignore`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/.pre-commit-config.yaml` & `mqt.bench-1.0.2/.pre-commit-config.yaml`

 * *Files 5% similar despite different names*

```diff
@@ -33,25 +33,25 @@
     rev: "0.5.0"
     hooks:
       - id: fix-ligatures
       - id: fix-smartquotes
 
   # Run code formatting with Black
   - repo: https://github.com/psf/black
-    rev: "23.3.0" # Keep in sync with blacken-docs
+    rev: "23.7.0" # Keep in sync with blacken-docs
     hooks:
       - id: black-jupyter
 
   # Also run Black on examples in the documentation
   - repo: https://github.com/asottile/blacken-docs
-    rev: "1.14.0"
+    rev: "1.15.0"
     hooks:
       - id: blacken-docs
         additional_dependencies:
-          - black==23.3.0 # keep in sync with black hook
+          - black==23.7.0 # keep in sync with black hook
 
   # Clean jupyter notebooks
   - repo: https://github.com/srstevenson/nb-clean
     rev: "2.4.0"
     hooks:
       - id: nb-clean
   # Check for spelling
@@ -60,21 +60,21 @@
     hooks:
       - id: codespell
         args: ["-L", "wille,linz"]
         exclude: "mqt/benchviewer/templates/legal.html"
 
   # Format configuration files with prettier
   - repo: https://github.com/pre-commit/mirrors-prettier
-    rev: "v3.0.0-alpha.9-for-vscode"
+    rev: "v3.0.0"
     hooks:
       - id: prettier
         types_or: [yaml, markdown, html, css, javascript, json]
 
-  - repo: https://github.com/charliermarsh/ruff-pre-commit
-    rev: v0.0.275
+  - repo: https://github.com/astral-sh/ruff-pre-commit
+    rev: v0.0.278
     hooks:
       - id: ruff
         args: ["--fix"]
 
   - repo: https://github.com/pre-commit/mirrors-mypy
     rev: v1.4.1
     hooks:
```

### Comparing `mqt.bench-1.0.1/LICENSE` & `mqt.bench-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/PKG-INFO` & `mqt.bench-1.0.2/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mqt.bench
-Version: 1.0.1
+Version: 1.0.2
 Summary: MQT Bench - A MQT tool for Benchmarking Quantum Software Tools
 Author-email: Nils Quetschlich <nils.quetschlich@tum.de>, Lukas Burgholzer <lukas.burgholzer@jku.at>
 License: MIT License
         
         Copyright (c) 2022 Nils Quetschlich, Lukas Burgholzer, and Robert Wille
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -335,20 +335,21 @@
 Afterwards, the package can be used as described [above](#Usage via pip package).
 
 # References:
 
 In case you are using MQT Bench in your work, we would be thankful if you referred to it by citing the following publication:
 
 ```bibtex
-@misc{quetschlich2022mqtbench,
-  title={{{MQT Bench}}: Benchmarking Software and Design Automation Tools for Quantum Computing},
-  shorttitle = {{{MQT Bench}}},
+@article{quetschlich2023mqtbench,
+  title={{{MQT Bench}}: {Benchmarking Software and Design Automation Tools for Quantum Computing}},
+  shorttitle = {{MQT Bench}},
+  journal = {{Quantum}},
   author={Quetschlich, Nils and Burgholzer, Lukas and Wille, Robert},
-  year={2022},
-  eprint = {2204.13719},
-  eprinttype = {arxiv},
-  publisher = {arXiv},
+  year={2023},
   note={{{MQT Bench}} is available at \url{https://www.cda.cit.tum.de/mqtbench/}},
 }
 ```
 
+which is also available on arXiv:
+[![a](https://img.shields.io/static/v1?label=arXiv&message=2204.13719&color=inactive&style=flat-square)](https://arxiv.org/abs/2204.13719)
+
 [1] A.Cross et al., OpenQASM 3: A broader and deeper quantum assembly language, [arXiv:2104.14722](https://arxiv.org/abs/2104.14722), 2021
```

### Comparing `mqt.bench-1.0.1/README.md` & `mqt.bench-1.0.2/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -283,20 +283,21 @@
 Afterwards, the package can be used as described [above](#Usage via pip package).
 
 # References:
 
 In case you are using MQT Bench in your work, we would be thankful if you referred to it by citing the following publication:
 
 ```bibtex
-@misc{quetschlich2022mqtbench,
-  title={{{MQT Bench}}: Benchmarking Software and Design Automation Tools for Quantum Computing},
-  shorttitle = {{{MQT Bench}}},
+@article{quetschlich2023mqtbench,
+  title={{{MQT Bench}}: {Benchmarking Software and Design Automation Tools for Quantum Computing}},
+  shorttitle = {{MQT Bench}},
+  journal = {{Quantum}},
   author={Quetschlich, Nils and Burgholzer, Lukas and Wille, Robert},
-  year={2022},
-  eprint = {2204.13719},
-  eprinttype = {arxiv},
-  publisher = {arXiv},
+  year={2023},
   note={{{MQT Bench}} is available at \url{https://www.cda.cit.tum.de/mqtbench/}},
 }
 ```
 
+which is also available on arXiv:
+[![a](https://img.shields.io/static/v1?label=arXiv&message=2204.13719&color=inactive&style=flat-square)](https://arxiv.org/abs/2204.13719)
+
 [1] A.Cross et al., OpenQASM 3: A broader and deeper quantum assembly language, [arXiv:2104.14722](https://arxiv.org/abs/2104.14722), 2021
```

### Comparing `mqt.bench-1.0.1/config.json` & `mqt.bench-1.0.2/config.json`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/img/arch.png` & `mqt.bench-1.0.2/img/arch.png`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/img/level_1.png` & `mqt.bench-1.0.2/img/level_1.png`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/img/level_2.png` & `mqt.bench-1.0.2/img/level_2.png`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/img/level_3.png` & `mqt.bench-1.0.2/img/level_3.png`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/img/level_4.png` & `mqt.bench-1.0.2/img/level_4.png`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/img/mqt_dark.png` & `mqt.bench-1.0.2/img/mqt_dark.png`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/img/mqt_light.png` & `mqt.bench-1.0.2/img/mqt_light.png`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/img/mqtbench.png` & `mqt.bench-1.0.2/img/mqtbench.png`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/pyproject.toml` & `mqt.bench-1.0.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -20,16 +20,15 @@
 
 dependencies = [
     "pytket-qiskit>=0.40.0,<0.42.0",  #  manages the dependencies for qiskit and tket in a combined fashion
     "qiskit[all]",  # this is merely to get the [all] dependencies. The versioning is covered by pytket-qiskit
     "pandas>=1.0.0",
     "flask>=2.0.0",
     "networkx>=2.0.0",
-    "scipy<1.11.0",
-    "pyscf>=2.1.0",
+    "pyscf>=2.3.0",
     "packaging>=21.0",
     "tqdm>=4.0.0",
     "importlib_metadata>=3.6; python_version < '3.10'",
     "importlib_resources>=5.9; python_version < '3.10'",
 ]
 
 classifiers = [
```

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmark_generator.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmark_generator.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/ae.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/ae.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/dj.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/dj.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/ghz.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/ghz.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/graphstate.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/graphstate.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/grover.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/grover.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qaoa.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qaoa.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qft.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qft.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qftentangled.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qftentangled.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_finance/portfolioqaoa.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_finance/portfolioqaoa.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_finance/portfoliovqe.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_finance/portfoliovqe.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_finance/pricingcall.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_finance/pricingcall.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_finance/pricingput.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_finance/pricingput.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_ml/qnn.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_ml/qnn.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_nature/groundstate.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_nature/groundstate.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_optimization/routing.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_optimization/routing.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qiskit_application_optimization/tsp.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qiskit_application_optimization/tsp.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qpeexact.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qpeexact.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qpeinexact.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qpeinexact.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/qwalk.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/qwalk.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/random.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/random.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/realamprandom.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/realamprandom.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/shor.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/shor.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/su2random.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/su2random.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/twolocalrandom.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/twolocalrandom.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/vqe.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/vqe.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/benchmarks/wstate.py` & `mqt.bench-1.0.2/src/mqt/bench/benchmarks/wstate.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/evaluation/evaluation.py` & `mqt.bench-1.0.2/src/mqt/bench/evaluation/evaluation.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/evaluation/evaluation_data.pkl` & `mqt.bench-1.0.2/src/mqt/bench/evaluation/evaluation_data.pkl`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/evaluation/evaluation_visualization.ipynb` & `mqt.bench-1.0.2/src/mqt/bench/evaluation/evaluation_visualization.ipynb`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/evaluation/results/pie.pdf` & `mqt.bench-1.0.2/src/mqt/bench/evaluation/results/pie.pdf`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/evaluation/results/qubit_dist.pdf` & `mqt.bench-1.0.2/src/mqt/bench/evaluation/results/qubit_dist.pdf`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/evaluation/results/violins.pdf` & `mqt.bench-1.0.2/src/mqt/bench/evaluation/results/violins.pdf`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/qiskit_helper.py` & `mqt.bench-1.0.2/src/mqt/bench/qiskit_helper.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/tket_helper.py` & `mqt.bench-1.0.2/src/mqt/bench/tket_helper.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/bench/utils.py` & `mqt.bench-1.0.2/src/mqt/bench/utils.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/benchviewer/backend.py` & `mqt.bench-1.0.2/src/mqt/benchviewer/backend.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/benchviewer/main.py` & `mqt.bench-1.0.2/src/mqt/benchviewer/main.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/benchviewer/static/favicon.ico` & `mqt.bench-1.0.2/src/mqt/benchviewer/static/favicon.ico`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/benchviewer/static/mqt_dark.png` & `mqt.bench-1.0.2/src/mqt/benchviewer/static/mqt_dark.png`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/benchviewer/static/tum_logo.svg` & `mqt.bench-1.0.2/src/mqt/benchviewer/static/tum_logo.svg`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/benchviewer/templates/benchmark_description.html` & `mqt.bench-1.0.2/src/mqt/benchviewer/templates/benchmark_description.html`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/benchviewer/templates/description.html` & `mqt.bench-1.0.2/src/mqt/benchviewer/templates/description.html`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt/benchviewer/templates/index.html` & `mqt.bench-1.0.2/src/mqt/benchviewer/templates/index.html`

 * *Files 1% similar despite different names*

```diff
@@ -633,24 +633,22 @@
         <strong
           >In case you are using MQT Bench in your work, we would be thankful if
           you referred to it by citing the following publication:</strong
         >
       </p>
 
       <p>
-        @misc{quetschlich2022mqtbench, <br />
+        @misc{quetschlich2023mqtbench, <br />
         &nbsp; title=&#123;&#123;&#123;MQT Bench}}: Benchmarking Software and
         Design Automation Tools for Quantum Computing},<br />
-        &nbsp; shorttitle = &#123;&#123;&#123;MQT Bench}}},<br />
+        &nbsp; shorttitle = &#123;&#123;MQT Bench}},<br />
+        &nbsp; journal = &#123;&#123;Quantum}},<br />
         &nbsp; author={Quetschlich, Nils and Burgholzer, Lukas and Wille,
         Robert},<br />
-        &nbsp; year={2022},<br />
-        &nbsp; eprint = {2204.13719},<br />
-        &nbsp; eprinttype = {arxiv},<br />
-        &nbsp; publisher = {arXiv},<br />
+        &nbsp; year={2023},<br />
         &nbsp; note=&#123;&#123;&#123;MQT Bench}} is available at
         \url{https://www.cda.cit.tum.de/mqtbench/}},<br />
         }
       </p>
 
       <p>
         In case you have any problems or questions feel free to contact us via
```

#### html2text {}

```diff
@@ -87,23 +87,21 @@
  Download selected Benchmarks
 *** Reference ***
 For a more detailed description of MQT Bench, we are referring to the
 corresponding paper "MQT_Bench:_Benchmarking_Software_and_Design_Automation
 Tools_for_Quantum_Computing". Our implementation is available on Github. In
 case you are using MQT Bench in your work, we would be thankful if you referred
 to it by citing the following publication:
-@misc{quetschlich2022mqtbench,
+@misc{quetschlich2023mqtbench,
   title={{{MQT Bench}}: Benchmarking Software and Design Automation Tools for
 Quantum Computing},
-  shorttitle = {{{MQT Bench}}},
+  shorttitle = {{MQT Bench}},
+  journal = {{Quantum}},
   author={Quetschlich, Nils and Burgholzer, Lukas and Wille, Robert},
-  year={2022},
-  eprint = {2204.13719},
-  eprinttype = {arxiv},
-  publisher = {arXiv},
+  year={2023},
   note={{{MQT Bench}} is available at \url{https://www.cda.cit.tum.de/mqtbench/
 }},
 }
 In case you have any problems or questions feel free to contact us via
 quantum.cda@xcit.tum.de. More on our work on quantum computation is summarized
 on this_page.
```

### Comparing `mqt.bench-1.0.1/src/mqt/benchviewer/templates/legal.html` & `mqt.bench-1.0.2/src/mqt/benchviewer/templates/legal.html`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/src/mqt.bench.egg-info/PKG-INFO` & `mqt.bench-1.0.2/src/mqt.bench.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mqt.bench
-Version: 1.0.1
+Version: 1.0.2
 Summary: MQT Bench - A MQT tool for Benchmarking Quantum Software Tools
 Author-email: Nils Quetschlich <nils.quetschlich@tum.de>, Lukas Burgholzer <lukas.burgholzer@jku.at>
 License: MIT License
         
         Copyright (c) 2022 Nils Quetschlich, Lukas Burgholzer, and Robert Wille
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
@@ -335,20 +335,21 @@
 Afterwards, the package can be used as described [above](#Usage via pip package).
 
 # References:
 
 In case you are using MQT Bench in your work, we would be thankful if you referred to it by citing the following publication:
 
 ```bibtex
-@misc{quetschlich2022mqtbench,
-  title={{{MQT Bench}}: Benchmarking Software and Design Automation Tools for Quantum Computing},
-  shorttitle = {{{MQT Bench}}},
+@article{quetschlich2023mqtbench,
+  title={{{MQT Bench}}: {Benchmarking Software and Design Automation Tools for Quantum Computing}},
+  shorttitle = {{MQT Bench}},
+  journal = {{Quantum}},
   author={Quetschlich, Nils and Burgholzer, Lukas and Wille, Robert},
-  year={2022},
-  eprint = {2204.13719},
-  eprinttype = {arxiv},
-  publisher = {arXiv},
+  year={2023},
   note={{{MQT Bench}} is available at \url{https://www.cda.cit.tum.de/mqtbench/}},
 }
 ```
 
+which is also available on arXiv:
+[![a](https://img.shields.io/static/v1?label=arXiv&message=2204.13719&color=inactive&style=flat-square)](https://arxiv.org/abs/2204.13719)
+
 [1] A.Cross et al., OpenQASM 3: A broader and deeper quantum assembly language, [arXiv:2104.14722](https://arxiv.org/abs/2104.14722), 2021
```

### Comparing `mqt.bench-1.0.1/src/mqt.bench.egg-info/SOURCES.txt` & `mqt.bench-1.0.2/src/mqt.bench.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/tests/test_bench.py` & `mqt.bench-1.0.2/tests/test_bench.py`

 * *Files identical despite different names*

### Comparing `mqt.bench-1.0.1/tests/test_benchviewer.py` & `mqt.bench-1.0.2/tests/test_benchviewer.py`

 * *Files identical despite different names*

