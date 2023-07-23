# Comparing `tmp/advanced-ta-0.1.2.tar.gz` & `tmp/advanced-ta-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "advanced-ta-0.1.2.tar", max compression
+gzip compressed data, was "advanced-ta-0.1.3.tar", max compression
```

## Comparing `advanced-ta-0.1.2.tar` & `advanced-ta-0.1.3.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     2234 2023-07-20 22:06:54.818226 advanced-ta-0.1.2/README.md
--rw-r--r--   0        0        0    26037 2023-07-20 21:47:44.968749 advanced-ta-0.1.2/advanced_ta/LorentzianClassification/Classifier.py
--rw-r--r--   0        0        0     2689 2023-07-20 17:14:25.348338 advanced-ta-0.1.2/advanced_ta/LorentzianClassification/KernelFunctions.py
--rw-r--r--   0        0        0     7252 2023-07-20 17:16:02.641151 advanced-ta-0.1.2/advanced_ta/LorentzianClassification/MLExtensions.py
--rw-r--r--   0        0        0     1891 2023-07-20 15:20:39.939402 advanced-ta-0.1.2/advanced_ta/LorentzianClassification/Types.py
--rw-r--r--   0        0        0       73 2023-07-20 15:29:10.313143 advanced-ta-0.1.2/advanced_ta/__init__.py
--rw-r--r--   0        0        0      581 2023-07-20 22:11:02.592268 advanced-ta-0.1.2/pyproject.toml
--rw-r--r--   0        0        0     3215 2023-07-20 22:11:27.006567 advanced-ta-0.1.2/setup.py
--rw-r--r--   0        0        0     2971 2023-07-20 22:11:27.006803 advanced-ta-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0     2464 2023-07-22 17:40:01.872548 advanced-ta-0.1.3/README.md
+-rw-r--r--   0        0        0    24598 2023-07-22 17:44:37.350764 advanced-ta-0.1.3/advanced_ta/LorentzianClassification/Classifier.py
+-rw-r--r--   0        0        0     2689 2023-07-20 17:14:25.348338 advanced-ta-0.1.3/advanced_ta/LorentzianClassification/KernelFunctions.py
+-rw-r--r--   0        0        0     7252 2023-07-20 17:16:02.641151 advanced-ta-0.1.3/advanced_ta/LorentzianClassification/MLExtensions.py
+-rw-r--r--   0        0        0     2937 2023-07-22 17:04:01.800969 advanced-ta-0.1.3/advanced_ta/LorentzianClassification/Types.py
+-rw-r--r--   0        0        0       73 2023-07-20 15:29:10.313143 advanced-ta-0.1.3/advanced_ta/__init__.py
+-rw-r--r--   0        0        0      609 2023-07-23 07:42:18.147642 advanced-ta-0.1.3/pyproject.toml
+-rw-r--r--   0        0        0     3451 2023-07-23 07:42:49.599049 advanced-ta-0.1.3/setup.py
+-rw-r--r--   0        0        0     3201 2023-07-23 07:42:49.599290 advanced-ta-0.1.3/PKG-INFO
```

### Comparing `advanced-ta-0.1.2/README.md` & `advanced-ta-0.1.3/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -35,22 +35,28 @@
             LorentzianClassification.Feature("RSI", 9, 2),   # f5
             ta.MFI(df['open'], df['high'], df['low'], df['close'], df['volume']) #f6
         ],
         settings=LorentzianClassification.Settings(
             source='close',
             neighborsCount=8,
             maxBarsBack=2000,
-            showDefaultExits=False,
             useDynamicExits=False
         ),
         filterSettings=LorentzianClassification.FilterSettings(
             useVolatilityFilter=True,
             useRegimeFilter=True,
             useAdxFilter=False,
             regimeThreshold=-0.1,
-            adxThreshold=20
+            adxThreshold=20,
+            kernelFilter = LorentzianClassification.KernelFilter(
+                useKernelSmoothing = False
+                lookbackWindow = 8
+                relativeWeight = 8.0
+                regressionLevel = 25
+                crossoverLag = 2
+            )
         ))
     lc.dump('output/result.csv')
     lc.plot('output/result.jpg')
 .
 .
 ```
```

### Comparing `advanced-ta-0.1.2/advanced_ta/LorentzianClassification/Classifier.py` & `advanced-ta-0.1.3/advanced_ta/LorentzianClassification/Classifier.py`

 * *Files 4% similar despite different names*

```diff
@@ -102,15 +102,15 @@
 # (2) The warping effect of Lorentzian distance reduces the overall influence  
 #     of outliers and noise.
 # (3) Lorentzian Distance becomes increasingly different from Euclidean Distance 
 #     as the number of nearest neighbors used for comparison increases.
 
 class LorentzianClassification:
     
-    from .Types import Feature, Settings, FilterSettings
+    from .Types import Feature, Settings, KernelFilter, FilterSettings
 
     df: pd.DataFrame = None
     features = list[pd.Series]()
     settings: Settings
     filterSettings: FilterSettings
     # Filter object for filtering the ML predictions
     filter: Filter
@@ -133,102 +133,79 @@
                 return ml.n_cci(data['high'], data['low'], data['close'], f_paramA, f_paramB)
             case "ADX":
                 return ml.n_adx(data['high'], data['low'], data['close'], f_paramA)
 
 
     def __init__(self, data: pd.DataFrame, features: list = [], settings: Settings = None, filterSettings: FilterSettings = None):
         self.df = data.copy()
+
         if len(features) == 0:
             features = [
                 Feature("RSI", 14, 2),  # f1
                 Feature("WT", 10, 11),  # f2
                 Feature("CCI", 20, 2),  # f3
                 Feature("ADX", 20, 2),  # f4
                 Feature("RSI", 9, 2),   # f5
             ]
         if settings == None:
-            settings = Settings(
-                source='close',
-                neighborsCount = 8,
-                maxBarsBack = 2000,
-                featureCount = 5,
-                colorCompression = 1,
-                showDefaultExits = False,
-                useDynamicExits = False
-            )
+            settings = Settings(source=data['close'])
+
         if filterSettings == None:
             filterSettings = FilterSettings(
                 useVolatilityFilter = True,
                 useRegimeFilter = True,
                 useAdxFilter = False,
                 regimeThreshold=-0.1,
-                adxThreshold = 20
+                adxThreshold = 20,
+                kernelFilter = KernelFilter()
             )
+        if hasattr(filterSettings, 'kernelFilter'):
+            self.useKernelFilter = True
+        else:
+            self.useKernelFilter = False
+            filterSettings.kernelFilter = KernelFilter()
+
         for f in features:
             if type(f) == Feature:
                 self.features.append(LorentzianClassification.series_from(data, f.type, f.param1, f.param2))
             else:
                 self.features.append(f)
         self.settings = settings
         self.filterSettings = filterSettings
         self.filter = Filter(
             volatility = ml.filter_volatility(data['high'], data['low'], data['close'], filterSettings.useVolatilityFilter, 1, 10),
             regime = ml.regime_filter((data['open'] + data['high'] + data['low'] + data['close']) / 4, data['high'], data['low'], filterSettings.useRegimeFilter, filterSettings.regimeThreshold),
-            adx = ml.filter_adx(data[settings.source], data['high'], data['low'], filterSettings.adxThreshold, filterSettings.useAdxFilter, 14)
+            adx = ml.filter_adx(settings.source, data['high'], data['low'], filterSettings.adxThreshold, filterSettings.useAdxFilter, 14)
         )
         self.__classify()
 
 
     def __get_lorentzian_distance(self, i, bar_index, features: list[pd.Series]):
         retVal = 0
         for feature in features:
             retVal += math.log(1 + abs(feature[bar_index] - feature[i]))
         return retVal
 
 
     def __classify(self):
         # Derived from General Settings
         maxBarsBackIndex = (len(self.df.index) - self.settings.maxBarsBack) if (len(self.df.index) >= self.settings.maxBarsBack) else 0
-        # EMA Settings
-        useEmaFilter = False
-        emaPeriod = 200
-        self.df["isEmaUptrend"] = (self.df["close"] > ta.EMA(self.df["close"], emaPeriod)) if useEmaFilter else True
-        self.df["isEmaDowntrend"] = (self.df["close"] < ta.EMA(self.df["close"], emaPeriod)) if useEmaFilter else True
-
-        # SMA Settings
-        useSmaFilter = False
-        smaPeriod = 200
-        self.df["isSmaUptrend"] = (self.df["close"] > ta.SMA(self.df["close"], smaPeriod)) if useSmaFilter else True
-        self.df["isSmaDowntrend"] = (self.df["close"] < ta.SMA(self.df["close"], smaPeriod)) if useSmaFilter else True
-
-
-        # Nadaraya-Watson Kernel Regression Settings
-        useKernelFilter = True  # Trade with Kernel
-        showKernelEstimate = True  # Show Kernel Estimate
-        useKernelSmoothing = False  # Enhance Kernel Smoothing: Uses a crossover based mechanism to smoothen kernel color changes. This often results in less color transitions overall and may result in more ML entry signals being generated.
-        h = 8  # Lookback Window: The number of bars used for the estimation. This is a sliding value that represents the most recent historical bars. Recommended range: 3-50
-        r = 8.0  # Relative Weighting: Relative weighting of time frames. As this value approaches zero, the longer time frames will exert more influence on the estimation. As this value approaches infinity, the behavior of the Rational Quadratic Kernel will become identical to the Gaussian kernel. Recommended range: 0.25-25
-        x = 25  # Regression Level: Bar index on which to start regression. Controls how tightly fit the kernel estimate is to the data. Smaller values are a tighter fit. Larger values are a looser fit. Recommended range: 2-25
-        lag = 2  # Lag: Lag for crossover detection. Lower values result in earlier crossovers. Recommended range: 1-2
-
-
-        # Display Settings
-        showBarColors = True  # Whether to show the bar colors.
-        showBarPredictions = True  # Will show the ML model's evaluation of each bar as an integer.
-        useAtrOffset = False  # Will use the ATR offset instead of the bar prediction offset.
-        barPredictionsOffset = 0.0  # The offset of the bar predictions as a percentage from the bar high or close.
 
+        self.df["isEmaUptrend"] = (self.df["close"] > ta.EMA(self.df["close"], self.settings.emaPeriod)) if self.settings.useEmaFilter else True
+        self.df["isEmaDowntrend"] = (self.df["close"] < ta.EMA(self.df["close"], self.settings.emaPeriod)) if self.settings.useEmaFilter else True
+        self.df["isSmaUptrend"] = (self.df["close"] > ta.SMA(self.df["close"], self.settings.smaPeriod)) if self.settings.useSmaFilter else True
+        self.df["isSmaDowntrend"] = (self.df["close"] < ta.SMA(self.df["close"], self.settings.smaPeriod)) if self.settings.useSmaFilter else True
 
         # =================================
         # ==== Next Bar Classification ====
         # =================================
 
         # This model specializes specifically in predicting the direction of price action over the course of the next 4 bars. 
         # To avoid complications with the ML model, this value is hardcoded to 4 bars but support for other training lengths may be added in the future.
-        src = self.df[self.settings.source]
+        src = self.settings.source
         y_train_array = np.where(src.shift(4) < src.shift(0), Direction.SHORT, np.where(src.shift(4) > src.shift(0), Direction.LONG, Direction.NEUTRAL))
 
         # Variables used for ML Logic
         predictions = []
         self.df["prediction"] = 0
         self.df["signal"] = Direction.NEUTRAL
         distances = []
@@ -330,16 +307,17 @@
 
         crossover   = lambda s1, s2: (s1 > s2) & (s1.shift(1) < s2.shift(1))
         crossunder  = lambda s1, s2: (s1 < s2) & (s1.shift(1) > s2.shift(1))
 
         # Kernel Regression Filters: Filters based on Nadaraya-Watson Kernel Regression using the Rational Quadratic Kernel
         # For more information on this technique refer to my other open source indicator located here:
         # https://www.tradingview.com/script/AWNvbPRM-Nadaraya-Watson-Rational-Quadratic-Kernel-Non-Repainting/
-        self.yhat1 = kernels.rationalQuadratic(src, h, r, x)
-        self.yhat2 = kernels.gaussian(src, h-lag, x)
+        kFilter = self.filterSettings.kernelFilter
+        self.yhat1 = kernels.rationalQuadratic(src, kFilter.lookbackWindow, kFilter.relativeWeight, kFilter.regressionLevel)
+        self.yhat2 = kernels.gaussian(src, kFilter.lookbackWindow-kFilter.crossoverLag, kFilter.regressionLevel)
         # Kernel Rates of Change
         wasBearishRate = np.where(self.yhat1.shift(2) > self.yhat1.shift(1), True, False)
         wasBullishRate = np.where(self.yhat1.shift(2) < self.yhat1.shift(1), True, False)
         isBearishRate = np.where(self.yhat1.shift(1) > self.yhat1, True, False)
         isBullishRate = np.where(self.yhat1.shift(1) < self.yhat1, True, False)
         isBearishChange = isBearishRate & wasBullishRate
         isBullishChange = isBullishRate & wasBearishRate
@@ -347,19 +325,19 @@
         isBullishCrossAlert = crossover(self.yhat2, self.yhat1)
         isBearishCrossAlert = crossunder(self.yhat2, self.yhat1)
         isBullishSmooth = (self.yhat2 >= self.yhat1)
         isBearishSmooth = (self.yhat2 <= self.yhat1)
         # Kernel Colors
         # plot(kernelEstimate, color=plotColor, linewidth=2, title="Kernel Regression Estimate")
         # Alert Variables
-        alertBullish = np.where(useKernelSmoothing, isBullishCrossAlert, isBullishChange)
-        alertBearish = np.where(useKernelSmoothing, isBearishCrossAlert, isBearishChange)
+        alertBullish = np.where(kFilter.useKernelSmoothing, isBullishCrossAlert, isBullishChange)
+        alertBearish = np.where(kFilter.useKernelSmoothing, isBearishCrossAlert, isBearishChange)
         # Bullish and Bearish Filters based on Kernel
-        isBullish = np.where(useKernelFilter, np.where(useKernelSmoothing, isBullishSmooth, isBullishRate), True)
-        isBearish = np.where(useKernelFilter, np.where(useKernelSmoothing, isBearishSmooth, isBearishRate) , True)
+        isBullish = np.where(self.useKernelFilter, np.where(kFilter.useKernelSmoothing, isBullishSmooth, isBullishRate), True)
+        isBearish = np.where(self.useKernelFilter, np.where(kFilter.useKernelSmoothing, isBearishSmooth, isBearishRate) , True)
 
         # ===========================
         # ==== Entries and Exits ====
         # ===========================
 
         def barssince(s: pd.Series):
             if not isinstance(s, pd.Series): s = pd.Series(s)
@@ -375,29 +353,29 @@
         startLongTrade = self.df["isNewBuySignal"] & isBullish & self.df["isEmaUptrend"] & self.df["isSmaUptrend"]
         startShortTrade = self.df["isNewSellSignal"] & isBearish & self.df["isEmaDowntrend"] & self.df["isSmaDowntrend"]
 
         self.df["startLongTrade"] = np.where(startLongTrade, self.df['low'], np.NaN)
         self.df["startShortTrade"] = np.where(startShortTrade, self.df['high'], np.NaN)
 
         # Dynamic Exit Conditions: Booleans for ML Model Position Exits based on Fractal Filters and Kernel Regression Filters
-        lastSignalWasBullish = barssince(startLongTrade) < barssince(startShortTrade)
-        lastSignalWasBearish = barssince(startShortTrade) < barssince(startLongTrade)
+        # lastSignalWasBullish = barssince(startLongTrade) < barssince(startShortTrade)
+        # lastSignalWasBearish = barssince(startShortTrade) < barssince(startLongTrade)
         barsSinceRedEntry = barssince(startShortTrade)
         barsSinceRedExit = barssince(alertBullish)
         barsSinceGreenEntry = barssince(startLongTrade)
         barsSinceGreenExit = barssince(alertBearish)
         isValidShortExit = barsSinceRedExit > barsSinceRedEntry
         isValidLongExit = barsSinceGreenExit > barsSinceGreenEntry
         endLongTradeDynamic = isBearishChange & pd.Series(isValidLongExit).shift(1)
         endShortTradeDynamic = isBullishChange & pd.Series(isValidShortExit).shift(1)
 
         # Fixed Exit Conditions: Booleans for ML Model Position Exits based on Bar-Count Filters
         endLongTradeStrict = ((isHeldFourBars & self.df["isLastSignalBuy"]) | (isHeldLessThanFourBars & self.df["isNewSellSignal"] & self.df["isLastSignalBuy"])) & startLongTrade.shift(4)
         endShortTradeStrict = ((isHeldFourBars & self.df["isLastSignalSell"]) | (isHeldLessThanFourBars & self.df["isNewBuySignal"] & self.df["isLastSignalSell"])) & startShortTrade.shift(4)
-        isDynamicExitValid = ~useEmaFilter & ~useSmaFilter & ~useKernelSmoothing
+        isDynamicExitValid = ~self.settings.useEmaFilter & ~self.settings.useSmaFilter & ~kFilter.useKernelSmoothing
         self.df["endLongTrade"] = self.settings.useDynamicExits & isDynamicExitValid & endLongTradeDynamic | endLongTradeStrict
         self.df["endShortTrade"] = self.settings.useDynamicExits & isDynamicExitValid & endShortTradeDynamic | endShortTradeStrict
 
 
     # =============================
     # ==== Dump or Return Data ====
     # =============================
```

### Comparing `advanced-ta-0.1.2/advanced_ta/LorentzianClassification/KernelFunctions.py` & `advanced-ta-0.1.3/advanced_ta/LorentzianClassification/KernelFunctions.py`

 * *Files identical despite different names*

### Comparing `advanced-ta-0.1.2/advanced_ta/LorentzianClassification/MLExtensions.py` & `advanced-ta-0.1.3/advanced_ta/LorentzianClassification/MLExtensions.py`

 * *Files identical despite different names*

### Comparing `advanced-ta-0.1.2/pyproject.toml` & `advanced-ta-0.1.3/pyproject.toml`

 * *Files 23% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 [tool.poetry]
 name = "advanced-ta"
-version = "0.1.2"
+version = "0.1.3"
 description = "Python implementation of Lorentzian Classification algorithm."
 authors = ["Loki Arya <loki.arya+osdev@gmail.com>"]
 readme = "README.md"
 repository = "https://bitbucket.org/lokiarya/advanced-ta"
 
 [tool.poetry.dependencies]
 python = "^3.10"
 numpy = "^1.25.1"
 pandas = "^2.0.3"
-TA-Lib = "^0.4.27"
+TA-Lib = "^0.4.24"
 python-dotenv = "^1.0.0"
 scikit-learn = "^1.3.0"
 mplfinance = "^0.12.9-beta.7"
 
 [tool.poetry.dev-dependencies]
 pytest = "^7.4"
+pytest-profiling = "^1.7.0"
 
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `advanced-ta-0.1.2/setup.py` & `advanced-ta-0.1.3/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -4,26 +4,26 @@
 packages = \
 ['advanced_ta', 'advanced_ta.LorentzianClassification']
 
 package_data = \
 {'': ['*']}
 
 install_requires = \
-['TA-Lib>=0.4.27,<0.5.0',
+['TA-Lib>=0.4.24,<0.5.0',
  'mplfinance>=0.12.9-beta.7,<0.13.0',
  'numpy>=1.25.1,<2.0.0',
  'pandas>=2.0.3,<3.0.0',
  'python-dotenv>=1.0.0,<2.0.0',
  'scikit-learn>=1.3.0,<2.0.0']
 
 setup_kwargs = {
     'name': 'advanced-ta',
-    'version': '0.1.2',
+    'version': '0.1.3',
     'description': 'Python implementation of Lorentzian Classification algorithm.',
-    'long_description': 'This module is a python implementation of Lorentzian Classification algorithm developed by @jdehorty in pinescript. The original work can be found here - https://www.tradingview.com/script/WhBzgfDu-Machine-Learning-Lorentzian-Classification/\n\n## Prerequisites\n> Ensure that [TA-Lib](https://ta-lib.org/hdr_dw.html) is downloaded and built for your platform. Set `TA_INCLUDE_PATH` and `TA_LIBRARY_PATH` as mentioned in [ta-lib-python](https://github.com/TA-Lib/ta-lib-python#installation). TA-Lib package itself will be installed as a dependency of `advanced-ta`.\n\n## Usage\n\nAt the most simplest, you can just do this:\n```python\nfrom advanced_ta import LorentzianClassification\n.\n.\n    # df here is the dataframe containing stock data as [[\'open\', \'high\', \'low\', \'close\', \'volume\']]. Notice that the column names are in lower case.\n    lc = LorentzianClassification(df)\n    lc.dump(\'output/result.csv\')\n    lc.plot(\'output/result.jpg\')\n.\n.\n```\n\nFor advanced use, you can do:\n```python\nfrom advanced_ta import LorentzianClassification\nimport TA-Lib as ta\n.\n.\n    # df here is the dataframe containing stock data as [[\'open\', \'high\', \'low\', \'close\', \'volume\']]. Notice that the column names are in lower case.\n    lc = LorentzianClassification(\n        df,\n        features=[\n            LorentzianClassification.Feature("RSI", 14, 2),  # f1\n            LorentzianClassification.Feature("WT", 10, 11),  # f2\n            LorentzianClassification.Feature("CCI", 20, 2),  # f3\n            LorentzianClassification.Feature("ADX", 20, 2),  # f4\n            LorentzianClassification.Feature("RSI", 9, 2),   # f5\n            ta.MFI(df[\'open\'], df[\'high\'], df[\'low\'], df[\'close\'], df[\'volume\']) #f6\n        ],\n        settings=LorentzianClassification.Settings(\n            source=\'close\',\n            neighborsCount=8,\n            maxBarsBack=2000,\n            showDefaultExits=False,\n            useDynamicExits=False\n        ),\n        filterSettings=LorentzianClassification.FilterSettings(\n            useVolatilityFilter=True,\n            useRegimeFilter=True,\n            useAdxFilter=False,\n            regimeThreshold=-0.1,\n            adxThreshold=20\n        ))\n    lc.dump(\'output/result.csv\')\n    lc.plot(\'output/result.jpg\')\n.\n.\n```',
+    'long_description': 'This module is a python implementation of Lorentzian Classification algorithm developed by @jdehorty in pinescript. The original work can be found here - https://www.tradingview.com/script/WhBzgfDu-Machine-Learning-Lorentzian-Classification/\n\n## Prerequisites\n> Ensure that [TA-Lib](https://ta-lib.org/hdr_dw.html) is downloaded and built for your platform. Set `TA_INCLUDE_PATH` and `TA_LIBRARY_PATH` as mentioned in [ta-lib-python](https://github.com/TA-Lib/ta-lib-python#installation). TA-Lib package itself will be installed as a dependency of `advanced-ta`.\n\n## Usage\n\nAt the most simplest, you can just do this:\n```python\nfrom advanced_ta import LorentzianClassification\n.\n.\n    # df here is the dataframe containing stock data as [[\'open\', \'high\', \'low\', \'close\', \'volume\']]. Notice that the column names are in lower case.\n    lc = LorentzianClassification(df)\n    lc.dump(\'output/result.csv\')\n    lc.plot(\'output/result.jpg\')\n.\n.\n```\n\nFor advanced use, you can do:\n```python\nfrom advanced_ta import LorentzianClassification\nimport TA-Lib as ta\n.\n.\n    # df here is the dataframe containing stock data as [[\'open\', \'high\', \'low\', \'close\', \'volume\']]. Notice that the column names are in lower case.\n    lc = LorentzianClassification(\n        df,\n        features=[\n            LorentzianClassification.Feature("RSI", 14, 2),  # f1\n            LorentzianClassification.Feature("WT", 10, 11),  # f2\n            LorentzianClassification.Feature("CCI", 20, 2),  # f3\n            LorentzianClassification.Feature("ADX", 20, 2),  # f4\n            LorentzianClassification.Feature("RSI", 9, 2),   # f5\n            ta.MFI(df[\'open\'], df[\'high\'], df[\'low\'], df[\'close\'], df[\'volume\']) #f6\n        ],\n        settings=LorentzianClassification.Settings(\n            source=\'close\',\n            neighborsCount=8,\n            maxBarsBack=2000,\n            useDynamicExits=False\n        ),\n        filterSettings=LorentzianClassification.FilterSettings(\n            useVolatilityFilter=True,\n            useRegimeFilter=True,\n            useAdxFilter=False,\n            regimeThreshold=-0.1,\n            adxThreshold=20,\n            kernelFilter = LorentzianClassification.KernelFilter(\n                useKernelSmoothing = False\n                lookbackWindow = 8\n                relativeWeight = 8.0\n                regressionLevel = 25\n                crossoverLag = 2\n            )\n        ))\n    lc.dump(\'output/result.csv\')\n    lc.plot(\'output/result.jpg\')\n.\n.\n```',
     'author': 'Loki Arya',
     'author_email': 'loki.arya+osdev@gmail.com',
     'maintainer': None,
     'maintainer_email': None,
     'url': 'https://bitbucket.org/lokiarya/advanced-ta',
     'packages': packages,
     'package_data': package_data,
```

### Comparing `advanced-ta-0.1.2/PKG-INFO` & `advanced-ta-0.1.3/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 Metadata-Version: 2.1
 Name: advanced-ta
-Version: 0.1.2
+Version: 0.1.3
 Summary: Python implementation of Lorentzian Classification algorithm.
 Home-page: https://bitbucket.org/lokiarya/advanced-ta
 Author: Loki Arya
 Author-email: loki.arya+osdev@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
-Requires-Dist: TA-Lib (>=0.4.27,<0.5.0)
+Requires-Dist: TA-Lib (>=0.4.24,<0.5.0)
 Requires-Dist: mplfinance (>=0.12.9-beta.7,<0.13.0)
 Requires-Dist: numpy (>=1.25.1,<2.0.0)
 Requires-Dist: pandas (>=2.0.3,<3.0.0)
 Requires-Dist: python-dotenv (>=1.0.0,<2.0.0)
 Requires-Dist: scikit-learn (>=1.3.0,<2.0.0)
 Project-URL: Repository, https://bitbucket.org/lokiarya/advanced-ta
 Description-Content-Type: text/markdown
@@ -54,22 +54,28 @@
             LorentzianClassification.Feature("RSI", 9, 2),   # f5
             ta.MFI(df['open'], df['high'], df['low'], df['close'], df['volume']) #f6
         ],
         settings=LorentzianClassification.Settings(
             source='close',
             neighborsCount=8,
             maxBarsBack=2000,
-            showDefaultExits=False,
             useDynamicExits=False
         ),
         filterSettings=LorentzianClassification.FilterSettings(
             useVolatilityFilter=True,
             useRegimeFilter=True,
             useAdxFilter=False,
             regimeThreshold=-0.1,
-            adxThreshold=20
+            adxThreshold=20,
+            kernelFilter = LorentzianClassification.KernelFilter(
+                useKernelSmoothing = False
+                lookbackWindow = 8
+                relativeWeight = 8.0
+                regressionLevel = 25
+                crossoverLag = 2
+            )
         ))
     lc.dump('output/result.csv')
     lc.plot('output/result.jpg')
 .
 .
 ```
```

