# Comparing `tmp/JSEStocks-0.0.2.tar.gz` & `tmp/JSEStocks-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "JSEStocks-0.0.2.tar", last modified: Wed Feb  2 23:56:47 2022, max compression
+gzip compressed data, was "JSEStocks-0.0.3.tar", last modified: Sun Jul 23 21:56:01 2023, max compression
```

## Comparing `JSEStocks-0.0.2.tar` & `JSEStocks-0.0.3.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-02 23:56:47.217139 JSEStocks-0.0.2/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-02 23:56:47.217139 JSEStocks-0.0.2/JSEStocks/
--rw-r--r--   0 runner    (1001) docker     (121)    13085 2022-02-02 23:56:36.000000 JSEStocks-0.0.2/JSEStocks/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-02 23:56:47.217139 JSEStocks-0.0.2/JSEStocks.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)    20727 2022-02-02 23:56:46.000000 JSEStocks-0.0.2/JSEStocks.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      212 2022-02-02 23:56:47.000000 JSEStocks-0.0.2/JSEStocks.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-02-02 23:56:46.000000 JSEStocks-0.0.2/JSEStocks.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       15 2022-02-02 23:56:46.000000 JSEStocks-0.0.2/JSEStocks.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       10 2022-02-02 23:56:46.000000 JSEStocks-0.0.2/JSEStocks.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)     1082 2022-02-02 23:56:36.000000 JSEStocks-0.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)    20727 2022-02-02 23:56:47.217139 JSEStocks-0.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)    17117 2022-02-02 23:56:36.000000 JSEStocks-0.0.2/README.md
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-02-02 23:56:47.217139 JSEStocks-0.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)      816 2022-02-02 23:56:36.000000 JSEStocks-0.0.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:56:01.632626 JSEStocks-0.0.3/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:56:01.632626 JSEStocks-0.0.3/JSEStocks/
+-rw-r--r--   0 runner    (1001) docker     (123)    18927 2023-07-23 21:55:51.000000 JSEStocks-0.0.3/JSEStocks/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:56:01.632626 JSEStocks-0.0.3/JSEStocks.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    20727 2023-07-23 21:56:01.000000 JSEStocks-0.0.3/JSEStocks.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      212 2023-07-23 21:56:01.000000 JSEStocks-0.0.3/JSEStocks.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 21:56:01.000000 JSEStocks-0.0.3/JSEStocks.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 21:56:01.000000 JSEStocks-0.0.3/JSEStocks.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-23 21:56:01.000000 JSEStocks-0.0.3/JSEStocks.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1082 2023-07-23 21:55:51.000000 JSEStocks-0.0.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    20727 2023-07-23 21:56:01.632626 JSEStocks-0.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    17117 2023-07-23 21:55:51.000000 JSEStocks-0.0.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 21:56:01.632626 JSEStocks-0.0.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      816 2023-07-23 21:55:51.000000 JSEStocks-0.0.3/setup.py
```

### Comparing `JSEStocks-0.0.2/JSEStocks/__init__.py` & `JSEStocks-0.0.3/JSEStocks/__init__.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,18 +1,8 @@
 import yfinance as yf
-import os, sys
-
-class HiddenPrints:
-    def __enter__(self):
-        self._original_stdout = sys.stdout
-        sys.stdout = open(os.devnull, 'w')
-
-    def __exit__(self, exc_type, exc_val, exc_tb):
-        sys.stdout.close()
-        sys.stdout = self._original_stdout
 
 def ReturnListStocks():
     stocks = '''
         StockCode,CompanyNames
         PRX,Prosus N.V. 
         ANH,Anheuser-Busch Inbev 
         BTI,British American Tobacco 
@@ -354,11 +344,230 @@
         KDV,Kaydav Group Limited 
         MZR,Mazor Group Limited 
         MLE,Mettle Investments Limited 
         MNK,Montauk Holdings Limited 
         '''
     print(stocks)
 
+
+def ReturnSouthAfricanETFs():
+    companyNames = [
+        "1nvest Top 40 ETF",
+        "1nvest SWIX 40 ETF",
+        "FNB Top 40 ETF",
+        "Satrix 40 ETF",
+        "Satrix SWIX Top 40 ETF",
+        "Sygnia Itrix SWIX 40 ETF",
+        "Sygnia Itrix Top 40 ETF",
+        "CoreShares Next 40",
+        "CoreShares Wealth Top 20",
+        "CoreShares Top 50 ETF",
+        "CoreShares DivTrax ETF",
+        "FNB Mid Cap ETF",
+        "Satrix S&P GIVI SA Top 50 ETF",
+        "Satrix Volatility Managed Defensive Equity ETF",
+        "Satrix Volatility Managed High Growth Equity ETF",
+        "Satrix Volatility Managed Moderate Equity ETF",
+        "Satrix Equity Momentum  ETF",
+        "Satrix Value Equity ETF",
+        "Satrix Low Volatility Equity ETF",
+        "Satrix Shari'ah Top 40 ETF",
+        "CoreShares Scientific Beta Mult-Factor ETF",
+        "Satrix Capped All Share ETF",
+        "Satrix DIVI ETF",
+        "Satrix FINI ETF",
+        "Satrix Inclusion & Diversity ETF",
+        "Satrix INDI ETF",
+        "Satrix Momentum ETF",
+        "Satrix  Quality South Africa ETF",
+        "Satrix RAFI 40 ETF",
+        "Satrix RESI ETF",
+        "CoreShares S&P 500 ETF",
+        "1nvest S&P 500 Index Feeder ETF",
+        "1nvest S&P 500 Info Tech Index Feeder ETF",
+        "1nvest MSCI EM Asia Index Feeder ETF",
+        "1nvest MSCI Wordld Socially Responsible Investment Index Feeder ETF",
+        "1nvest MSCI World Index Feeder ETF",
+        "FNB Global 1200 Equity Fund of Funds ETF",
+        "CoreShares Total World Stock Feeder ETF",
+        "CoreShares S&P Global Dividend Aristocrats ETF",
+        "Satrix S&P 500 ETF",
+        "Satrix MSCI China ETF",
+        "Satrix Smart City Infrastructure Feeder ETF",
+        "Satrix MSCI EM ESG Enhanced ETF",
+        "Satrix MSCI Emerging Markets ETF",
+        "Satrix MSCI World ESG Enhanced ETF",
+        "Satrix Healthcare Innovation Feeder ETF",
+        "Satrix Global Infrastucture ETF",
+        "Satrix MSCI India ETF",
+        "Satrix Nasdaq 100 ETF",
+        "Satrix MSCI World ETF",
+        "Sygnia Itrix 4th Industrial Revolution Global Equity ETF",
+        "Sygnia Itrix S&P 500",
+        "Sygnia Itrix New China Sectors ETF",
+        "Sygnia Itrix MSCI Emerging Markets 50 ETF",
+        "Sygnia Itrix S&P Global 1200 ESG ETF",
+        "Sygnia DJ EuroStoxx 50 ETF",
+        "Sygnia Itrix Solactive Healthcare 150 ETF",
+        "Sygnia Itrix MSCI Japan ETF",
+        "Sygnia Itrix Sustainable Economy ETF",
+        "Sygnia Itrix FTSE 100 ETF",
+        "Sygnia Itrix MSCI USA ETF",
+        "Sygnia Itrix MSCI World ETF",
+        "1nvestGold ETF",
+        "1nvestPalladium ETF",
+        "1nvestPlatinum ETF",
+        "1nvestRhodium ETF",
+        "NewGold ETF",
+        "Krugerrand  Custodial Certificate",
+        "NewPalladium ETF",
+        "NewPlat ETF",
+        "CoreShares Wealth GOVI ETF",
+        "CoreShares Yield Selected Bond ETF",
+        "1nvest SA Bond ETF",
+        "FNB Inflation ETF",
+        "Satrix GOVI ETF",
+        "Satrix ILBI ETF",
+        "Satrix SA Bond ETF",
+        "Satrix ILBI ETF",
+        "Dollar Custodial Certificate  - 10 Year",
+        "Dollar Custodial Certificate - 2 Year",
+        "1nvest Global Government Bond Index Feeder ETF",
+        "1nvest ICE US Treasury Short Bond Index ETF",
+        "FNB World Government Bond ETF",
+        "Satrix S&P Namibia Bond ETF",
+        "Satrix Global Aggregate Bond ETF",
+        "Satrix TRACI 3 Month  ETF",
+        "Satrix Multi Asset Passive Portfolios Solutions Growth ETF",
+        "Satrix Multi Asset Passive Portfolios Solutions Protect ETF",
+        "CoreShares SA Property Income ETF",
+        "1nvest SA Property ETF",
+        "Satrix Property ETF",
+        "1nvest Global REIT Index Feeder ETF",
+        "Satrix Reitway Global Property ETF",
+        "Coreshares  S&P Global Property ETF",
+        "Reitway Global Property ESG Prescient ETF",
+        "Reitway Global Property Diversified Prescient ETF",
+        "Sygnia Itrix Global Property ETF",
+    ]
+
+    codes = [
+        "ETFT40",
+        "ETFSWX",
+        "FNBT40",
+        "STX40",
+        "STXSWX",
+        "SYGSW4",
+        "SYGT40",
+        "CSNT40",
+        "CTOP20",
+        "CTOP50",
+        "DIVTRX",
+        "FNBMID",
+        "STXT50",
+        "STXDEQ",
+        "STXGEQ",
+        "STXMEQ",
+        "STXEQM",
+        "STXVEQ",
+        "STXLVL",
+        "STXSHA",
+        "SMART",
+        "STXCAP",
+        "STXDIV",
+        "STXFIN",
+        "STXID",
+        "STXIND",
+        "STXMMT",
+        "STXQUA",
+        "STXRAF",
+        "STXRES",
+        "CSP500",
+        "ETF500",
+        "ETF5IT",
+        "ETFEMA",
+        "ETFSRI",
+        "ETFWLD",
+        "FNBEQF",
+        "GLOBAL",
+        "GLODIV",
+        "STX500",
+        "STXCHN",
+        "STXCTY",
+        "STXEME",
+        "STXEMG",
+        "STXESG",
+        "STXHLT",
+        "STXIFR",
+        "STXNDA",
+        "STXNDQ",
+        "STXWDM",
+        "SYG4IR",
+        "SYG500",
+        "SYGCN",
+        "SYGEMF",
+        "SYGESG",
+        "SYGEU",
+        "SYGH",
+        "SYGJP",
+        "SYGSE",
+        "SYGUK",
+        "SYGUS",
+        "SYGWD",
+        "ETFGLD",
+        "ETFPLD",
+        "ETFPLT",
+        "ETFRHO",
+        "GLD",
+        "KCCGLD",
+        "NGPLD",
+        "NGPLT",
+        "CSGOVI",
+        "CSYSB",
+        "ETFBND",
+        "FNBINF",
+        "STXGVI",
+        "STXIFL",
+        "STXGOV",
+        "STXILB",
+        "DCCUSD",
+        "DCCUS2",
+        "ETFGGB",
+        "ETFUSD",
+        "FNBWGB",
+        "STXNAM",
+        "STXGBD",
+        "STXTRA",
+        "STXMAG",
+        "STXMAP ",
+        "CSPROP",
+        "ETFSAP",
+        "STXPRO",
+        "ETFGRE",
+        "STXGPR",
+        "GLPROP",
+        "RWESG",
+        "RWDVF",
+        "SYGP",
+    ]
+
+    for i in range(len(companyNames)):
+        print(companyNames[i] + " - " + codes[i])
+
+
 def GetStockHistory(Code):
     df = yf.download(Code+'.JO')
     df['Date'] = df.index
-    return df
+    return df
+
+
+def GetStockHistoryAllMarkets(Code):
+    df = yf.download(Code)
+    df['Date'] = df.index
+    return df
+
+
+if __name__ == '__main__':
+    ReturnSouthAfricanETFs()
+    # GetStockHistoryAllMarkets('AAPL')
+    # GetStockHistory('AAPL')
+    # ReturnListStocks()
```

### Comparing `JSEStocks-0.0.2/JSEStocks.egg-info/PKG-INFO` & `JSEStocks-0.0.3/JSEStocks.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 Metadata-Version: 2.1
 Name: JSEStocks
-Version: 0.0.2
+Version: 0.0.3
 Summary: a module that returns all the stock data in JSE
 Home-page: https://www.adgstudios.co.za
 Author: Ashlin Darius Govindasamy
-Author-email: adg@adgstudios.co.ZA
+Author-email: adg@adgstudios.co.za
 License: MIT
 Description: ![](data:image/png;base64,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)
         
         # JSE STOCK Python Module
         
         this module returns stock history for any given module
```

### Comparing `JSEStocks-0.0.2/LICENSE` & `JSEStocks-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `JSEStocks-0.0.2/PKG-INFO` & `JSEStocks-0.0.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 Metadata-Version: 2.1
 Name: JSEStocks
-Version: 0.0.2
+Version: 0.0.3
 Summary: a module that returns all the stock data in JSE
 Home-page: https://www.adgstudios.co.za
 Author: Ashlin Darius Govindasamy
-Author-email: adg@adgstudios.co.ZA
+Author-email: adg@adgstudios.co.za
 License: MIT
 Description: ![](data:image/png;base64,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)
         
         # JSE STOCK Python Module
         
         this module returns stock history for any given module
```

### Comparing `JSEStocks-0.0.2/README.md` & `JSEStocks-0.0.3/README.md`

 * *Files identical despite different names*

### Comparing `JSEStocks-0.0.2/setup.py` & `JSEStocks-0.0.3/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -4,17 +4,17 @@
 long_description = (this_directory / "README.md").read_text()
 
 setup(
     #metadata here
     name="JSEStocks",
     long_description=long_description,
     long_description_content_type='text/markdown',
-    version="0.0.2",
+    version="0.0.3",
     author="Ashlin Darius Govindasamy",
-    author_email="adg@adgstudios.co.ZA",
+    author_email="adg@adgstudios.co.za",
     url="https://www.adgstudios.co.za",
     description="a module that returns all the stock data in JSE",
     packages=find_packages(),
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
```

