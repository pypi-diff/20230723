# Comparing `tmp/FinQuant-0.3.2.tar.gz` & `tmp/FinQuant-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "FinQuant-0.3.2.tar", last modified: Wed Jul 19 11:29:29 2023, max compression
+gzip compressed data, was "FinQuant-0.4.0.tar", last modified: Sun Jul 23 20:38:51 2023, max compression
```

## Comparing `FinQuant-0.3.2.tar` & `FinQuant-0.4.0.tar`

### file list

```diff
@@ -1,34 +1,34 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 11:29:29.239527 FinQuant-0.3.2/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 11:29:29.235527 FinQuant-0.3.2/FinQuant.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    14840 2023-07-19 11:29:29.000000 FinQuant-0.3.2/FinQuant.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      655 2023-07-19 11:29:29.000000 FinQuant-0.3.2/FinQuant.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-19 11:29:29.000000 FinQuant-0.3.2/FinQuant.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      229 2023-07-19 11:29:29.000000 FinQuant-0.3.2/FinQuant.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-19 11:29:29.000000 FinQuant-0.3.2/FinQuant.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-07-19 11:28:51.000000 FinQuant-0.3.2/LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)    14840 2023-07-19 11:29:29.239527 FinQuant-0.3.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    13659 2023-07-19 11:28:51.000000 FinQuant-0.3.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 11:29:29.239527 FinQuant-0.3.2/finquant/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4738 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/asset.py
--rw-r--r--   0 runner    (1001) docker     (123)    16730 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/efficient_frontier.py
--rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/market.py
--rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/minimise_fun.py
--rw-r--r--   0 runner    (1001) docker     (123)    11041 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/monte_carlo.py
--rw-r--r--   0 runner    (1001) docker     (123)     7485 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/moving_average.py
--rw-r--r--   0 runner    (1001) docker     (123)    46879 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/portfolio.py
--rw-r--r--   0 runner    (1001) docker     (123)     3936 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/quants.py
--rw-r--r--   0 runner    (1001) docker     (123)     2219 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/returns.py
--rw-r--r--   0 runner    (1001) docker     (123)     4191 2023-07-19 11:28:51.000000 FinQuant-0.3.2/finquant/stock.py
--rw-r--r--   0 runner    (1001) docker     (123)      301 2023-07-19 11:28:51.000000 FinQuant-0.3.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      106 2023-07-19 11:29:29.239527 FinQuant-0.3.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2200 2023-07-19 11:28:51.000000 FinQuant-0.3.2/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 11:29:29.239527 FinQuant-0.3.2/tests/
--rw-r--r--   0 runner    (1001) docker     (123)      212 2023-07-19 11:28:51.000000 FinQuant-0.3.2/tests/test_efficient_frontier.py
--rw-r--r--   0 runner    (1001) docker     (123)     1007 2023-07-19 11:28:51.000000 FinQuant-0.3.2/tests/test_market.py
--rw-r--r--   0 runner    (1001) docker     (123)     6283 2023-07-19 11:28:51.000000 FinQuant-0.3.2/tests/test_moving_average.py
--rw-r--r--   0 runner    (1001) docker     (123)      212 2023-07-19 11:28:51.000000 FinQuant-0.3.2/tests/test_optimisation.py
--rw-r--r--   0 runner    (1001) docker     (123)    15920 2023-07-19 11:28:51.000000 FinQuant-0.3.2/tests/test_portfolio.py
--rw-r--r--   0 runner    (1001) docker     (123)     1278 2023-07-19 11:28:51.000000 FinQuant-0.3.2/tests/test_quants.py
--rw-r--r--   0 runner    (1001) docker     (123)     2244 2023-07-19 11:28:51.000000 FinQuant-0.3.2/tests/test_returns.py
--rw-r--r--   0 runner    (1001) docker     (123)     1928 2023-07-19 11:28:51.000000 FinQuant-0.3.2/tests/test_stock.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:38:51.294643 FinQuant-0.4.0/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:38:51.294643 FinQuant-0.4.0/FinQuant.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    14858 2023-07-23 20:38:51.000000 FinQuant-0.4.0/FinQuant.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      655 2023-07-23 20:38:51.000000 FinQuant-0.4.0/FinQuant.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 20:38:51.000000 FinQuant-0.4.0/FinQuant.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      229 2023-07-23 20:38:51.000000 FinQuant-0.4.0/FinQuant.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 20:38:51.000000 FinQuant-0.4.0/FinQuant.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-07-23 20:38:11.000000 FinQuant-0.4.0/LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    14858 2023-07-23 20:38:51.298643 FinQuant-0.4.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    13677 2023-07-23 20:38:11.000000 FinQuant-0.4.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:38:51.294643 FinQuant-0.4.0/finquant/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4738 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/asset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16730 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/efficient_frontier.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/market.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/minimise_fun.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11041 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/monte_carlo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7485 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/moving_average.py
+-rw-r--r--   0 runner    (1001) docker     (123)    48218 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/portfolio.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5283 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/quants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2219 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/returns.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4208 2023-07-23 20:38:11.000000 FinQuant-0.4.0/finquant/stock.py
+-rw-r--r--   0 runner    (1001) docker     (123)      301 2023-07-23 20:38:11.000000 FinQuant-0.4.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      106 2023-07-23 20:38:51.298643 FinQuant-0.4.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2200 2023-07-23 20:38:11.000000 FinQuant-0.4.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:38:51.294643 FinQuant-0.4.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      212 2023-07-23 20:38:11.000000 FinQuant-0.4.0/tests/test_efficient_frontier.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1007 2023-07-23 20:38:11.000000 FinQuant-0.4.0/tests/test_market.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6283 2023-07-23 20:38:11.000000 FinQuant-0.4.0/tests/test_moving_average.py
+-rw-r--r--   0 runner    (1001) docker     (123)      212 2023-07-23 20:38:11.000000 FinQuant-0.4.0/tests/test_optimisation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15920 2023-07-23 20:38:11.000000 FinQuant-0.4.0/tests/test_portfolio.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2468 2023-07-23 20:38:11.000000 FinQuant-0.4.0/tests/test_quants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2244 2023-07-23 20:38:11.000000 FinQuant-0.4.0/tests/test_returns.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1928 2023-07-23 20:38:11.000000 FinQuant-0.4.0/tests/test_stock.py
```

### Comparing `FinQuant-0.3.2/FinQuant.egg-info/PKG-INFO` & `FinQuant-0.4.0/FinQuant.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: FinQuant
-Version: 0.3.2
+Version: 0.4.0
 Summary: A program for financial portfolio management, analysis and optimisation
 Home-page: https://github.com/fmilthaler/FinQuant
-Download-URL: https://github.com/fmilthaler/FinQuant/archive/v0.3.2.tar.gz
+Download-URL: https://github.com/fmilthaler/FinQuant/archive/v0.4.0.tar.gz
 Author: Frank Milthaler
 Author-email: f.milthaler@gmail.com
 License: MIT
 Project-URL: Documentation, https://finquant.readthedocs.io
 Keywords: finance,portfolio,investment,numerical,optimisation,monte carlo,efficient frontier,quantitative,quant
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Education
@@ -32,15 +32,15 @@
 </p>
 
 <p align="center">
   <a href="https://GitHub.com/fmilthaler/FinQuant/stargazers/">
     <img src="https://img.shields.io/github/stars/fmilthaler/FinQuant.svg?style=social&label=Star" alt='pypi'>
   </a>
   <a href="https://pypi.org/project/FinQuant">
-    <img src="https://img.shields.io/badge/pypi-v0.3.2-brightgreen.svg?style=popout" alt='pypi'>
+    <img src="https://img.shields.io/badge/pypi-v0.4.0-brightgreen.svg?style=popout" alt='pypi'>
   </a>
   <a href="https://github.com/fmilthaler/FinQuant">
     <img src="https://github.com/fmilthaler/finquant/actions/workflows/pytest.yml/badge.svg?branch=master" alt='GitHub Actions'>
   </a>
   <a href="http://finquant.readthedocs.io/">
     <img src="https://img.shields.io/readthedocs/finquant.svg?style=popout" alt="docs">
   </a>
@@ -274,15 +274,16 @@
 ### Building a portfolio with preset data
 `./example/Example-Build-Portfolio-from-file.py`: Shows how to use *FinQuant* to build a financial portfolio by providing stock price data yourself, e.g. by reading data from disk/file.
 
 ### Analysis of a portfolio
 `./example/Example-Analysis.py`: This example shows how to use an instance of `finquant.portfolio.Portfolio`, get the portfolio's quantities, such as
  - Expected Returns,
  - Volatility,
- - Sharpe Ratio.
+ - Sharpe Ratio,
+ - Value at Risk.
 
 It also shows how to extract individual stocks from the given portfolio. Moreover it shows how to compute and visualise:
  - the different Returns provided by the module `finquant.returns`,
  - *Moving Averages*, a band of *Moving Averages*, and a *Bollinger Band*.
 
 ### Optimisation of a portfolio
 `./example/Example-Optimisation.py`: This example focusses on the optimisation of a portfolio. To achieve this, the example shows the usage of `finquant.efficient_frontier.EfficientFrontier` for optimising the portfolio, for the
```

#### html2text {}

```diff
@@ -1,11 +1,11 @@
-Metadata-Version: 2.1 Name: FinQuant Version: 0.3.2 Summary: A program for
+Metadata-Version: 2.1 Name: FinQuant Version: 0.4.0 Summary: A program for
 financial portfolio management, analysis and optimisation Home-page: https://
 github.com/fmilthaler/FinQuant Download-URL: https://github.com/fmilthaler/
-FinQuant/archive/v0.3.2.tar.gz Author: Frank Milthaler Author-email:
+FinQuant/archive/v0.4.0.tar.gz Author: Frank Milthaler Author-email:
 f.milthaler@gmail.com License: MIT Project-URL: Documentation, https://
 finquant.readthedocs.io Keywords:
 finance,portfolio,investment,numerical,optimisation,monte carlo,efficient
 frontier,quantitative,quant Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Education Classifier: Intended Audience ::
 Financial and Insurance Industry Classifier: Intended Audience :: Other
 Audience Classifier: Intended Audience :: Science/Research Classifier:
@@ -153,21 +153,21 @@
 from-web.py`: Shows how to use *FinQuant* to build a financial portfolio by
 downloading stock price data through the Python package `quandl`/`yfinance`.
 ### Building a portfolio with preset data `./example/Example-Build-Portfolio-
 from-file.py`: Shows how to use *FinQuant* to build a financial portfolio by
 providing stock price data yourself, e.g. by reading data from disk/file. ###
 Analysis of a portfolio `./example/Example-Analysis.py`: This example shows how
 to use an instance of `finquant.portfolio.Portfolio`, get the portfolio's
-quantities, such as - Expected Returns, - Volatility, - Sharpe Ratio. It also
-shows how to extract individual stocks from the given portfolio. Moreover it
-shows how to compute and visualise: - the different Returns provided by the
-module `finquant.returns`, - *Moving Averages*, a band of *Moving Averages*,
-and a *Bollinger Band*. ### Optimisation of a portfolio `./example/Example-
-Optimisation.py`: This example focusses on the optimisation of a portfolio. To
-achieve this, the example shows the usage of
+quantities, such as - Expected Returns, - Volatility, - Sharpe Ratio, - Value
+at Risk. It also shows how to extract individual stocks from the given
+portfolio. Moreover it shows how to compute and visualise: - the different
+Returns provided by the module `finquant.returns`, - *Moving Averages*, a band
+of *Moving Averages*, and a *Bollinger Band*. ### Optimisation of a portfolio
+`./example/Example-Optimisation.py`: This example focusses on the optimisation
+of a portfolio. To achieve this, the example shows the usage of
 `finquant.efficient_frontier.EfficientFrontier` for optimising the portfolio,
 for the - Minimum Volatility - Maximum Sharpe Ratio - Minimum Volatility for a
 given target Return - Maximum Sharpe Ratio for a given target Volatility.
 Furthermore, it is also shown how the entire *Efficient Frontier* and the
 optimal portfolios can be computed and visualised. If needed, it also gives an
 example of plotting the individual stocks of the given portfolio within the
 computed *Efficient Frontier*. Also, the optimisation of a portfolio and its
```

### Comparing `FinQuant-0.3.2/FinQuant.egg-info/SOURCES.txt` & `FinQuant-0.4.0/FinQuant.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/LICENSE.txt` & `FinQuant-0.4.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/PKG-INFO` & `FinQuant-0.4.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: FinQuant
-Version: 0.3.2
+Version: 0.4.0
 Summary: A program for financial portfolio management, analysis and optimisation
 Home-page: https://github.com/fmilthaler/FinQuant
-Download-URL: https://github.com/fmilthaler/FinQuant/archive/v0.3.2.tar.gz
+Download-URL: https://github.com/fmilthaler/FinQuant/archive/v0.4.0.tar.gz
 Author: Frank Milthaler
 Author-email: f.milthaler@gmail.com
 License: MIT
 Project-URL: Documentation, https://finquant.readthedocs.io
 Keywords: finance,portfolio,investment,numerical,optimisation,monte carlo,efficient frontier,quantitative,quant
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Education
@@ -32,15 +32,15 @@
 </p>
 
 <p align="center">
   <a href="https://GitHub.com/fmilthaler/FinQuant/stargazers/">
     <img src="https://img.shields.io/github/stars/fmilthaler/FinQuant.svg?style=social&label=Star" alt='pypi'>
   </a>
   <a href="https://pypi.org/project/FinQuant">
-    <img src="https://img.shields.io/badge/pypi-v0.3.2-brightgreen.svg?style=popout" alt='pypi'>
+    <img src="https://img.shields.io/badge/pypi-v0.4.0-brightgreen.svg?style=popout" alt='pypi'>
   </a>
   <a href="https://github.com/fmilthaler/FinQuant">
     <img src="https://github.com/fmilthaler/finquant/actions/workflows/pytest.yml/badge.svg?branch=master" alt='GitHub Actions'>
   </a>
   <a href="http://finquant.readthedocs.io/">
     <img src="https://img.shields.io/readthedocs/finquant.svg?style=popout" alt="docs">
   </a>
@@ -274,15 +274,16 @@
 ### Building a portfolio with preset data
 `./example/Example-Build-Portfolio-from-file.py`: Shows how to use *FinQuant* to build a financial portfolio by providing stock price data yourself, e.g. by reading data from disk/file.
 
 ### Analysis of a portfolio
 `./example/Example-Analysis.py`: This example shows how to use an instance of `finquant.portfolio.Portfolio`, get the portfolio's quantities, such as
  - Expected Returns,
  - Volatility,
- - Sharpe Ratio.
+ - Sharpe Ratio,
+ - Value at Risk.
 
 It also shows how to extract individual stocks from the given portfolio. Moreover it shows how to compute and visualise:
  - the different Returns provided by the module `finquant.returns`,
  - *Moving Averages*, a band of *Moving Averages*, and a *Bollinger Band*.
 
 ### Optimisation of a portfolio
 `./example/Example-Optimisation.py`: This example focusses on the optimisation of a portfolio. To achieve this, the example shows the usage of `finquant.efficient_frontier.EfficientFrontier` for optimising the portfolio, for the
```

#### html2text {}

```diff
@@ -1,11 +1,11 @@
-Metadata-Version: 2.1 Name: FinQuant Version: 0.3.2 Summary: A program for
+Metadata-Version: 2.1 Name: FinQuant Version: 0.4.0 Summary: A program for
 financial portfolio management, analysis and optimisation Home-page: https://
 github.com/fmilthaler/FinQuant Download-URL: https://github.com/fmilthaler/
-FinQuant/archive/v0.3.2.tar.gz Author: Frank Milthaler Author-email:
+FinQuant/archive/v0.4.0.tar.gz Author: Frank Milthaler Author-email:
 f.milthaler@gmail.com License: MIT Project-URL: Documentation, https://
 finquant.readthedocs.io Keywords:
 finance,portfolio,investment,numerical,optimisation,monte carlo,efficient
 frontier,quantitative,quant Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Education Classifier: Intended Audience ::
 Financial and Insurance Industry Classifier: Intended Audience :: Other
 Audience Classifier: Intended Audience :: Science/Research Classifier:
@@ -153,21 +153,21 @@
 from-web.py`: Shows how to use *FinQuant* to build a financial portfolio by
 downloading stock price data through the Python package `quandl`/`yfinance`.
 ### Building a portfolio with preset data `./example/Example-Build-Portfolio-
 from-file.py`: Shows how to use *FinQuant* to build a financial portfolio by
 providing stock price data yourself, e.g. by reading data from disk/file. ###
 Analysis of a portfolio `./example/Example-Analysis.py`: This example shows how
 to use an instance of `finquant.portfolio.Portfolio`, get the portfolio's
-quantities, such as - Expected Returns, - Volatility, - Sharpe Ratio. It also
-shows how to extract individual stocks from the given portfolio. Moreover it
-shows how to compute and visualise: - the different Returns provided by the
-module `finquant.returns`, - *Moving Averages*, a band of *Moving Averages*,
-and a *Bollinger Band*. ### Optimisation of a portfolio `./example/Example-
-Optimisation.py`: This example focusses on the optimisation of a portfolio. To
-achieve this, the example shows the usage of
+quantities, such as - Expected Returns, - Volatility, - Sharpe Ratio, - Value
+at Risk. It also shows how to extract individual stocks from the given
+portfolio. Moreover it shows how to compute and visualise: - the different
+Returns provided by the module `finquant.returns`, - *Moving Averages*, a band
+of *Moving Averages*, and a *Bollinger Band*. ### Optimisation of a portfolio
+`./example/Example-Optimisation.py`: This example focusses on the optimisation
+of a portfolio. To achieve this, the example shows the usage of
 `finquant.efficient_frontier.EfficientFrontier` for optimising the portfolio,
 for the - Minimum Volatility - Maximum Sharpe Ratio - Minimum Volatility for a
 given target Return - Maximum Sharpe Ratio for a given target Volatility.
 Furthermore, it is also shown how the entire *Efficient Frontier* and the
 optimal portfolios can be computed and visualised. If needed, it also gives an
 example of plotting the individual stocks of the given portfolio within the
 computed *Efficient Frontier*. Also, the optimisation of a portfolio and its
```

### Comparing `FinQuant-0.3.2/README.md` & `FinQuant-0.4.0/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 </p>
 
 <p align="center">
   <a href="https://GitHub.com/fmilthaler/FinQuant/stargazers/">
     <img src="https://img.shields.io/github/stars/fmilthaler/FinQuant.svg?style=social&label=Star" alt='pypi'>
   </a>
   <a href="https://pypi.org/project/FinQuant">
-    <img src="https://img.shields.io/badge/pypi-v0.3.2-brightgreen.svg?style=popout" alt='pypi'>
+    <img src="https://img.shields.io/badge/pypi-v0.4.0-brightgreen.svg?style=popout" alt='pypi'>
   </a>
   <a href="https://github.com/fmilthaler/FinQuant">
     <img src="https://github.com/fmilthaler/finquant/actions/workflows/pytest.yml/badge.svg?branch=master" alt='GitHub Actions'>
   </a>
   <a href="http://finquant.readthedocs.io/">
     <img src="https://img.shields.io/readthedocs/finquant.svg?style=popout" alt="docs">
   </a>
@@ -245,15 +245,16 @@
 ### Building a portfolio with preset data
 `./example/Example-Build-Portfolio-from-file.py`: Shows how to use *FinQuant* to build a financial portfolio by providing stock price data yourself, e.g. by reading data from disk/file.
 
 ### Analysis of a portfolio
 `./example/Example-Analysis.py`: This example shows how to use an instance of `finquant.portfolio.Portfolio`, get the portfolio's quantities, such as
  - Expected Returns,
  - Volatility,
- - Sharpe Ratio.
+ - Sharpe Ratio,
+ - Value at Risk.
 
 It also shows how to extract individual stocks from the given portfolio. Moreover it shows how to compute and visualise:
  - the different Returns provided by the module `finquant.returns`,
  - *Moving Averages*, a band of *Moving Averages*, and a *Bollinger Band*.
 
 ### Optimisation of a portfolio
 `./example/Example-Optimisation.py`: This example focusses on the optimisation of a portfolio. To achieve this, the example shows the usage of `finquant.efficient_frontier.EfficientFrontier` for optimising the portfolio, for the
```

#### html2text {}

```diff
@@ -136,21 +136,21 @@
 from-web.py`: Shows how to use *FinQuant* to build a financial portfolio by
 downloading stock price data through the Python package `quandl`/`yfinance`.
 ### Building a portfolio with preset data `./example/Example-Build-Portfolio-
 from-file.py`: Shows how to use *FinQuant* to build a financial portfolio by
 providing stock price data yourself, e.g. by reading data from disk/file. ###
 Analysis of a portfolio `./example/Example-Analysis.py`: This example shows how
 to use an instance of `finquant.portfolio.Portfolio`, get the portfolio's
-quantities, such as - Expected Returns, - Volatility, - Sharpe Ratio. It also
-shows how to extract individual stocks from the given portfolio. Moreover it
-shows how to compute and visualise: - the different Returns provided by the
-module `finquant.returns`, - *Moving Averages*, a band of *Moving Averages*,
-and a *Bollinger Band*. ### Optimisation of a portfolio `./example/Example-
-Optimisation.py`: This example focusses on the optimisation of a portfolio. To
-achieve this, the example shows the usage of
+quantities, such as - Expected Returns, - Volatility, - Sharpe Ratio, - Value
+at Risk. It also shows how to extract individual stocks from the given
+portfolio. Moreover it shows how to compute and visualise: - the different
+Returns provided by the module `finquant.returns`, - *Moving Averages*, a band
+of *Moving Averages*, and a *Bollinger Band*. ### Optimisation of a portfolio
+`./example/Example-Optimisation.py`: This example focusses on the optimisation
+of a portfolio. To achieve this, the example shows the usage of
 `finquant.efficient_frontier.EfficientFrontier` for optimising the portfolio,
 for the - Minimum Volatility - Maximum Sharpe Ratio - Minimum Volatility for a
 given target Return - Maximum Sharpe Ratio for a given target Volatility.
 Furthermore, it is also shown how the entire *Efficient Frontier* and the
 optimal portfolios can be computed and visualised. If needed, it also gives an
 example of plotting the individual stocks of the given portfolio within the
 computed *Efficient Frontier*. Also, the optimisation of a portfolio and its
```

### Comparing `FinQuant-0.3.2/finquant/asset.py` & `FinQuant-0.4.0/finquant/asset.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/finquant/efficient_frontier.py` & `FinQuant-0.4.0/finquant/efficient_frontier.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/finquant/market.py` & `FinQuant-0.4.0/finquant/market.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/finquant/minimise_fun.py` & `FinQuant-0.4.0/finquant/minimise_fun.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/finquant/monte_carlo.py` & `FinQuant-0.4.0/finquant/monte_carlo.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/finquant/moving_average.py` & `FinQuant-0.4.0/finquant/moving_average.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/finquant/portfolio.py` & `FinQuant-0.4.0/finquant/portfolio.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,14 +14,15 @@
 
 - cumulative returns of the portfolio's stocks
 - daily returns of the portfolio's stocks (daily percentage change),
 - daily log returns of the portfolio's stocks,
 - Expected (annualised) Return,
 - Volatility,
 - Sharpe Ratio,
+- Value at Risk,
 - Beta parameter (optional),
 - skewness of the portfolio's stocks,
 - Kurtosis of the portfolio's stocks,
 - the portfolio's covariance matrix.
 
 Furthermore, the constructed portfolio can be optimised for
 
@@ -54,15 +55,15 @@
 import matplotlib.pylab as plt
 import numpy as np
 import pandas as pd
 
 from finquant.efficient_frontier import EfficientFrontier
 from finquant.market import Market
 from finquant.monte_carlo import MonteCarloOpt
-from finquant.quants import sharpe_ratio, weighted_mean, weighted_std
+from finquant.quants import sharpe_ratio, value_at_risk, weighted_mean, weighted_std
 from finquant.returns import (
     cumulative_returns,
     daily_log_returns,
     daily_returns,
     historical_mean_return,
 )
 from finquant.stock import Stock
@@ -81,17 +82,19 @@
         # initilisating instance variables
         self.portfolio = pd.DataFrame()
         self.stocks = {}
         self.data = pd.DataFrame()
         self.expected_return = None
         self.volatility = None
         self.sharpe = None
+        self.var = None
         self.skew = None
         self.kurtosis = None
         self.totalinvestment = None
+        self.var_confidence_level = 0.95
         self.risk_free_rate = 0.005
         self.freq = 252
         # instance variables for Efficient Frontier and
         # Monte Carlo optimisations
         self.ef = None
         self.mc = None
         # instance variable for Market class
@@ -150,14 +153,28 @@
     def market_index(self, index: Market) -> None:
         """Set the market index to the portfolio.
 
         :param index: An object of the ``Market`` class.
         """
         self.__market_index = index
 
+    @property
+    def var_confidence_level(self):
+        return self.__var_confidence_level
+
+    @var_confidence_level.setter
+    def var_confidence_level(self, val):
+        if not isinstance(val, float):
+            raise ValueError("confidence level is expected to be a float.")
+        if val >= 1 or val <= 0:
+            raise ValueError("confidence level is expected to be between 0 and 1.")
+        self.__var_confidence_level = val
+        # now that this changed, update VaR
+        self._update()
+
     def add_stock(self, stock: Stock) -> None:
         """Adds a stock of type ``Stock`` to the portfolio. Each time ``add_stock``
         is called, the following instance variables are updated:
 
         - ``portfolio``: ``pandas.DataFrame``, adds a column with information from ``stock``
         - ``stocks``: ``dictionary``, adds an entry for ``stock``
         - ``data``: ``pandas.DataFrame``, adds a column of stock prices from ``stock``
@@ -206,14 +223,15 @@
     def _update(self):
         # sanity check (only update values if none of the below is empty):
         if not (self.portfolio.empty or not self.stocks or self.data.empty):
             self.totalinvestment = self.portfolio.Allocation.sum()
             self.expected_return = self.comp_expected_return(freq=self.freq)
             self.volatility = self.comp_volatility(freq=self.freq)
             self.sharpe = self.comp_sharpe()
+            self.var = self.comp_var()
             self.skew = self._comp_skew()
             self.kurtosis = self._comp_kurtosis()
             if self.market_index is not None:
                 self.beta = self.comp_beta()
 
     def get_stock(self, name):
         """Returns the instance of ``Stock`` with name ``name``.
@@ -351,14 +369,30 @@
         # compute the Sharpe Ratio of the portfolio
         sharpe = sharpe_ratio(
             self.expected_return, self.volatility, self.risk_free_rate
         )
         self.sharpe = sharpe
         return sharpe
 
+    def comp_var(self):
+        """Compute and return the Value at Risk of the portfolio.
+
+        :Output:
+         :VaR: ``float``, the Value at Risk of the portfolio
+        """
+        # compute the Value at Risk of the portfolio
+        var = value_at_risk(
+            investment=self.totalinvestment,
+            mu=self.expected_return,
+            sigma=self.volatility,
+            conf_level=self.var_confidence_level,
+        )
+        self.var = var
+        return var
+
     def comp_beta(self) -> float:
         """Compute and return the Beta parameter of the portfolio.
 
         :Output:
          :sharpe: ``float``, the Beta parameter of the portfolio
         """
 
@@ -627,14 +661,15 @@
 
     def properties(self):
         """Nicely prints out the properties of the portfolio:
 
         - Expected Return,
         - Volatility,
         - Sharpe Ratio,
+        - Value at Risk,
         - Beta (optional),
         - skewness,
         - Kurtosis
 
         as well as the allocation of the stocks across the portfolio.
         """
         # nicely printing out information and quantities of the portfolio
@@ -644,14 +679,17 @@
         if self.market_index is not None:
             string += f"\nMarket Index: {self.market_index.name}"
         string += f"\nTime window/frequency: {self.freq}"
         string += f"\nRisk free rate: {self.risk_free_rate}"
         string += f"\nPortfolio Expected Return: {self.expected_return:0.3f}"
         string += f"\nPortfolio Volatility: {self.volatility:0.3f}"
         string += f"\nPortfolio Sharpe Ratio: {self.sharpe:0.3f}"
+        string += f"\nPortfolio Value at Risk: {self.var:0.3f}"
+        string += f"\nConfidence level of Value at Risk: "
+        string += f"{self.var_confidence_level * 100:0.2f} %"
         if self.beta is not None:
             string += f"\nPortfolio Beta: {self.beta:0.3f}"
         string += "\n\nSkewness:"
         string += "\n" + str(self.skew.to_frame().transpose())
         string += "\n\nKurtosis:"
         string += "\n" + str(self.kurtosis.to_frame().transpose())
         string += "\n\nInformation:"
```

### Comparing `FinQuant-0.3.2/finquant/quants.py` & `FinQuant-0.4.0/finquant/quants.py`

 * *Files 19% similar despite different names*

```diff
@@ -2,14 +2,15 @@
 portfolios, e.g. a weighted average, which is the expected value/return, a
 weighted standard deviation (volatility), and the Sharpe ratio.
 """
 
 
 import numpy as np
 import pandas as pd
+from scipy.stats import norm
 
 
 def weighted_mean(means, weights):
     """Computes the weighted mean/average, or in the case of a
     financial portfolio, it can be used for the Expected Return
     of said portfolio.
 
@@ -70,14 +71,42 @@
     if not isinstance(
         risk_free_rate, (int, float, np.int32, np.int64, np.float32, np.float64)
     ):
         raise ValueError("risk_free_rate is expected to be an integer or float.")
     return (exp_return - risk_free_rate) / float(volatility)
 
 
+def value_at_risk(investment, mu, sigma, conf_level=0.95) -> float:
+    """Computes and returns the expected value at risk of an investment/assets.
+
+    :Input:
+     :investment: ``float``/``int``, total value of the investment
+     :mu: ``float``/``int`` average/mean return of the investment
+     :sigma: ``float``/``int`` standard deviation of the investment
+     :conf_level: ``float`` (default= ``0.95``), confidence level of the VaR
+
+    :Output:
+     :Value at Risk: ``float``, VaR of the investment
+    """
+    if not isinstance(
+        investment, (int, float, np.int32, np.int64, np.float32, np.float64)
+    ):
+        raise ValueError("investment is expected to be an integer or float.")
+    if not isinstance(mu, (int, float, np.int32, np.int64, np.float32, np.float64)):
+        raise ValueError("mu is expected to be an integer or float")
+    if not isinstance(sigma, (int, float, np.int32, np.int64, np.float32, np.float64)):
+        raise ValueError("sigma is expected to be an integer or float")
+    if not isinstance(conf_level, float):
+        raise ValueError("confidence level is expected to be a float.")
+    if conf_level >= 1 or conf_level <= 0:
+        raise ValueError("confidence level is expected to be between 0 and 1.")
+
+    return investment * (mu - sigma * norm.ppf(1 - conf_level))
+
+
 def annualised_portfolio_quantities(
     weights, means, cov_matrix, risk_free_rate=0.005, freq=252
 ):
     """Computes and returns the expected annualised return, volatility
     and Sharpe Ratio of a portfolio.
 
     :Input:
```

### Comparing `FinQuant-0.3.2/finquant/returns.py` & `FinQuant-0.4.0/finquant/returns.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/finquant/stock.py` & `FinQuant-0.4.0/finquant/stock.py`

 * *Files 2% similar despite different names*

```diff
@@ -41,15 +41,14 @@
 
     In addition to the attributes inherited from the ``Asset`` class, the ``Stock`` class provides
     a method to compute the beta parameter specific to stocks in a portfolio when compared to
     the market index.
 
     """
 
-
     def __init__(self, investmentinfo: pd.DataFrame, data: pd.Series) -> None:
         """
         :Input:
          :investmentinfo: ``pandas.DataFrame`` of investment information
          :data: ``pandas.Series`` of stock price
         """
         self.name = investmentinfo.Name
@@ -74,23 +73,23 @@
 
         beta = cov_mat[0, 1] / cov_mat[1, 1]
         self.beta = beta
         return beta
 
     def properties(self):
         """Nicely prints out the properties of the stock: Expected Return,
-        Volatility, Skewness, Kurtosis as well as the ``Allocation`` (and other
+        Volatility, Beta (optional), Skewness, Kurtosis as well as the ``Allocation`` (and other
         information provided in investmentinfo.)
         """
         # nicely printing out information and quantities of the stock
         string = "-" * 50
         string += f"\n{self.asset_type}: {self.name}"
         string += f"\nExpected Return: {self.expected_return:0.3f}"
         string += f"\nVolatility: {self.volatility:0.3f}"
-        string += f"\nSkewness: {self.skew:0.5f}"
-        string += f"\nKurtosis: {self.kurtosis:0.5f}"
         if self.beta is not None:
             string += f"\n{self.asset_type} Beta: {self.beta:0.3f}"
+        string += f"\nSkewness: {self.skew:0.5f}"
+        string += f"\nKurtosis: {self.kurtosis:0.5f}"
         string += "\nInformation:"
         string += "\n" + str(self.investmentinfo.to_frame().transpose())
         string += "\n" + "-" * 50
-        print(string)
+        print(string)
```

### Comparing `FinQuant-0.3.2/setup.py` & `FinQuant-0.4.0/setup.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/tests/test_market.py` & `FinQuant-0.4.0/tests/test_market.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/tests/test_moving_average.py` & `FinQuant-0.4.0/tests/test_moving_average.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/tests/test_portfolio.py` & `FinQuant-0.4.0/tests/test_portfolio.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/tests/test_returns.py` & `FinQuant-0.4.0/tests/test_returns.py`

 * *Files identical despite different names*

### Comparing `FinQuant-0.3.2/tests/test_stock.py` & `FinQuant-0.4.0/tests/test_stock.py`

 * *Files identical despite different names*

