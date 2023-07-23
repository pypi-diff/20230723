# Comparing `tmp/blankly-1.9.0b0.tar.gz` & `tmp/Blankly-v0.1.1-alpha.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/Users/emerson/WebstormProjects/Blankly/Blankly/dist/tmps27dzrae/blankly-1.9.0b0.tar", last modified: Thu Sep 30 21:33:26 2021, max compression
+gzip compressed data, was "dist/Blankly-v0.1.1-alpha.tar", last modified: Sun Mar 14 01:49:15 2021, max compression
```

## Comparing `blankly-1.9.0b0.tar` & `Blankly-v0.1.1-alpha.tar`

### file list

```diff
@@ -1,136 +1,14 @@
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/
--rw-r--r--   0 emerson    (501) staff       (20)     2187 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/__init__.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/deployment/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/deployment/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     3418 2021-08-18 17:51:40.000000 blankly-1.9.0b0/Blankly/deployment/api.py
--rw-r--r--   0 emerson    (501) staff       (20)    12273 2021-09-23 22:01:13.000000 blankly-1.9.0b0/Blankly/deployment/cli.py
--rw-r--r--   0 emerson    (501) staff       (20)      137 2021-09-23 22:01:13.000000 blankly-1.9.0b0/Blankly/deployment/cpp_test.py
--rw-r--r--   0 emerson    (501) staff       (20)     5102 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/deployment/reporter_headers.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     1239 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/abc_exchange.py
--rw-r--r--   0 emerson    (501) staff       (20)     1552 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/abc_exchange_websocket.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/auth/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/auth/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     2661 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/auth/abc_auth.py
--rw-r--r--   0 emerson    (501) staff       (20)     4120 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/auth/auth_constructor.py
--rw-r--r--   0 emerson    (501) staff       (20)     1729 2021-08-18 17:51:40.000000 blankly-1.9.0b0/Blankly/exchanges/auth/auth_factory.py
--rw-r--r--   0 emerson    (501) staff       (20)     1747 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/auth/utils.py
--rw-r--r--   0 emerson    (501) staff       (20)     6359 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/exchanges/exchange.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     7930 2021-08-23 20:12:25.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/abc_exchange_interface.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/alpaca/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/alpaca/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     1383 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/alpaca/alpaca.py
--rw-r--r--   0 emerson    (501) staff       (20)     1626 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/alpaca/alpaca_api.py
--rw-r--r--   0 emerson    (501) staff       (20)     1063 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/alpaca/alpaca_auth.py
--rw-r--r--   0 emerson    (501) staff       (20)    23055 2021-09-30 21:27:09.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/alpaca/alpaca_interface.py
--rw-r--r--   0 emerson    (501) staff       (20)     8770 2021-08-29 01:08:33.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/alpaca/alpaca_websocket.py
--rw-r--r--   0 emerson    (501) staff       (20)     3452 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/alpaca/alpaca_websocket_utils.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/binance/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/binance/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     1800 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/binance/binance.py
--rw-r--r--   0 emerson    (501) staff       (20)    15098 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/binance/binance_api.py
--rw-r--r--   0 emerson    (501) staff       (20)     1066 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/binance/binance_auth.py
--rw-r--r--   0 emerson    (501) staff       (20)    31981 2021-09-10 00:37:29.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/binance/binance_interface.py
--rw-r--r--   0 emerson    (501) staff       (20)     6834 2021-08-18 17:51:40.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/binance/binance_websocket.py
--rw-r--r--   0 emerson    (501) staff       (20)     3360 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/binance/binance_websocket_utils.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/coinbase_pro/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/coinbase_pro/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     3323 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/coinbase_pro/coinbase_pro.py
--rw-r--r--   0 emerson    (501) staff       (20)    45709 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/coinbase_pro/coinbase_pro_api.py
--rw-r--r--   0 emerson    (501) staff       (20)     1088 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/coinbase_pro/coinbase_pro_auth.py
--rw-r--r--   0 emerson    (501) staff       (20)    21869 2021-09-09 23:03:58.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/coinbase_pro/coinbase_pro_interface.py
--rw-r--r--   0 emerson    (501) staff       (20)     1673 2021-08-18 17:51:40.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/coinbase_pro/coinbase_pro_utils.py
--rw-r--r--   0 emerson    (501) staff       (20)     7710 2021-08-23 20:12:25.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/coinbase_pro/coinbase_pro_websocket.py
--rw-r--r--   0 emerson    (501) staff       (20)     2196 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/coinbase_pro/coinbase_pro_websocket_utils.py
--rw-r--r--   0 emerson    (501) staff       (20)     3110 2021-08-18 17:51:40.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/direct_calls_factory.py
--rw-r--r--   0 emerson    (501) staff       (20)    12526 2021-09-30 21:31:13.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/exchange_interface.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/oanda/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-08-18 17:51:40.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/oanda/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)      546 2021-08-18 17:51:40.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/oanda/oanda.py
--rw-r--r--   0 emerson    (501) staff       (20)     9344 2021-08-18 17:51:40.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/oanda/oanda_api.py
--rw-r--r--   0 emerson    (501) staff       (20)     1077 2021-08-18 17:51:40.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/oanda/oanda_auth.py
--rw-r--r--   0 emerson    (501) staff       (20)    18056 2021-08-23 20:12:25.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/oanda/oanda_interface.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)    35431 2021-09-30 21:23:23.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/backtest_controller.py
--rw-r--r--   0 emerson    (501) staff       (20)     2451 2021-09-30 21:23:23.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/backtest_result.py
--rw-r--r--   0 emerson    (501) staff       (20)     1633 2021-09-23 22:01:13.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/backtesting_wrapper.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/local_account/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/local_account/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)      841 2021-07-29 01:45:36.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/local_account/local_account.py
--rw-r--r--   0 emerson    (501) staff       (20)     5185 2021-09-22 02:55:26.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/local_account/trade_local.py
--rw-r--r--   0 emerson    (501) staff       (20)     3003 2021-08-06 16:03:44.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/metrics.py
--rw-r--r--   0 emerson    (501) staff       (20)     2680 2021-08-06 16:03:44.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/paper_trade.py
--rw-r--r--   0 emerson    (501) staff       (20)    25299 2021-09-22 02:58:45.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/paper_trade_interface.py
--rw-r--r--   0 emerson    (501) staff       (20)     1257 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/interfaces/paper_trade/utils.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/managers/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/managers/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     6596 2021-07-29 01:45:36.000000 blankly-1.9.0b0/Blankly/exchanges/managers/general_stream_manager.py
--rw-r--r--   0 emerson    (501) staff       (20)    14841 2021-07-29 01:45:36.000000 blankly-1.9.0b0/Blankly/exchanges/managers/orderbook_manager.py
--rw-r--r--   0 emerson    (501) staff       (20)     5696 2021-07-29 01:45:36.000000 blankly-1.9.0b0/Blankly/exchanges/managers/ticker_manager.py
--rw-r--r--   0 emerson    (501) staff       (20)     6677 2021-07-29 01:45:36.000000 blankly-1.9.0b0/Blankly/exchanges/managers/websocket_manager.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/exchanges/orders/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/orders/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     6134 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/orders/limit_order.py
--rw-r--r--   0 emerson    (501) staff       (20)     4874 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/orders/market_order.py
--rw-r--r--   0 emerson    (501) staff       (20)     4541 2021-08-23 20:12:25.000000 blankly-1.9.0b0/Blankly/exchanges/orders/order.py
--rw-r--r--   0 emerson    (501) staff       (20)     4517 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/exchanges/orders/stop_limit.py
--rw-r--r--   0 emerson    (501) staff       (20)     4777 2021-08-29 01:08:33.000000 blankly-1.9.0b0/Blankly/exchanges/strategy_logger.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/frameworks/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/__init__.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/frameworks/multiprocessing/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/multiprocessing/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     4966 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/multiprocessing/blankly_bot.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/frameworks/signal/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/signal/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     5831 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/signal/signal.py
--rw-r--r--   0 emerson    (501) staff       (20)     1490 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/signal/signal_runner.py
--rw-r--r--   0 emerson    (501) staff       (20)     2248 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/signal/signal_state.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/frameworks/strategy/
--rw-r--r--   0 emerson    (501) staff       (20)      113 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/strategy/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     1696 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/strategy/order.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/frameworks/strategy/recipes/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/strategy/recipes/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     1927 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/strategy/recipes/recipes.py
--rw-r--r--   0 emerson    (501) staff       (20)    23042 2021-09-16 21:16:01.000000 blankly-1.9.0b0/Blankly/frameworks/strategy/strategy_base.py
--rw-r--r--   0 emerson    (501) staff       (20)     2353 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/strategy/strategy_state.py
--rw-r--r--   0 emerson    (501) staff       (20)     2530 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/frameworks/strategy/strategy_usage_example.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/indicators/
--rw-r--r--   0 emerson    (501) staff       (20)      221 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/indicators/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     2892 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/indicators/indicators.py
--rw-r--r--   0 emerson    (501) staff       (20)     3605 2021-07-29 17:28:50.000000 blankly-1.9.0b0/Blankly/indicators/moving_averages.py
--rw-r--r--   0 emerson    (501) staff       (20)     3741 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/indicators/oscillators.py
--rw-r--r--   0 emerson    (501) staff       (20)     2296 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/indicators/statistics.py
--rw-r--r--   0 emerson    (501) staff       (20)     1233 2021-08-06 16:03:44.000000 blankly-1.9.0b0/Blankly/indicators/utils.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/metrics/
--rw-r--r--   0 emerson    (501) staff       (20)       40 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/metrics/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     2855 2021-08-06 16:03:44.000000 blankly-1.9.0b0/Blankly/metrics/portfolio.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly/utils/
--rw-r--r--   0 emerson    (501) staff       (20)       64 2021-08-23 20:12:25.000000 blankly-1.9.0b0/Blankly/utils/__init__.py
--rw-r--r--   0 emerson    (501) staff       (20)     2626 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/utils/calc.py
--rw-r--r--   0 emerson    (501) staff       (20)      880 2021-07-22 18:00:22.000000 blankly-1.9.0b0/Blankly/utils/exceptions.py
--rw-r--r--   0 emerson    (501) staff       (20)     4899 2021-09-06 16:05:01.000000 blankly-1.9.0b0/Blankly/utils/scheduler.py
--rw-r--r--   0 emerson    (501) staff       (20)      952 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/utils/time.py
--rw-r--r--   0 emerson    (501) staff       (20)     2585 2021-07-21 02:23:27.000000 blankly-1.9.0b0/Blankly/utils/time_builder.py
--rw-r--r--   0 emerson    (501) staff       (20)    24326 2021-09-16 21:15:49.000000 blankly-1.9.0b0/Blankly/utils/utils.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly.egg-info/
--rw-r--r--   0 emerson    (501) staff       (20)     9829 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly.egg-info/PKG-INFO
--rw-r--r--   0 emerson    (501) staff       (20)     5328 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly.egg-info/SOURCES.txt
--rw-r--r--   0 emerson    (501) staff       (20)        1 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly.egg-info/dependency_links.txt
--rw-r--r--   0 emerson    (501) staff       (20)       57 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly.egg-info/entry_points.txt
--rw-r--r--   0 emerson    (501) staff       (20)      167 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly.egg-info/requires.txt
--rw-r--r--   0 emerson    (501) staff       (20)       14 2021-09-30 21:33:26.000000 blankly-1.9.0b0/Blankly.egg-info/top_level.txt
--rw-r--r--   0 emerson    (501) staff       (20)     7651 2021-03-15 21:23:44.000000 blankly-1.9.0b0/LICENSE
--rw-r--r--   0 emerson    (501) staff       (20)     9829 2021-09-30 21:33:26.000000 blankly-1.9.0b0/PKG-INFO
--rw-r--r--   0 emerson    (501) staff       (20)     8959 2021-09-23 22:01:05.000000 blankly-1.9.0b0/README.md
--rw-r--r--   0 emerson    (501) staff       (20)       79 2021-09-30 21:33:26.000000 blankly-1.9.0b0/setup.cfg
--rw-r--r--   0 emerson    (501) staff       (20)     2287 2021-09-30 21:32:59.000000 blankly-1.9.0b0/setup.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/tests/
--rw-r--r--   0 emerson    (501) staff       (20)        0 2021-09-30 20:46:32.000000 blankly-1.9.0b0/tests/__init__.py
-drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-09-30 21:33:26.000000 blankly-1.9.0b0/tests/helpers/
--rw-r--r--   0 emerson    (501) staff       (20)      439 2021-08-18 17:51:40.000000 blankly-1.9.0b0/tests/helpers/comparisons.py
--rw-r--r--   0 emerson    (501) staff       (20)       73 2021-07-21 02:23:27.000000 blankly-1.9.0b0/tests/test_auth_constructor.py
+drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-03-14 01:49:15.000000 Blankly-v0.1.1-alpha/
+drwxr-xr-x   0 emerson    (501) staff       (20)        0 2021-03-14 01:49:15.000000 Blankly-v0.1.1-alpha/Blankly/
+-rw-r--r--   0 emerson    (501) staff       (20)     1816 2021-03-13 23:55:26.000000 Blankly-v0.1.1-alpha/Blankly/API_Interface.py
+-rw-r--r--   0 emerson    (501) staff       (20)      450 2021-03-09 18:47:28.000000 Blankly-v0.1.1-alpha/Blankly/Constants.py
+-rw-r--r--   0 emerson    (501) staff       (20)      437 2021-03-09 18:47:28.000000 Blankly-v0.1.1-alpha/Blankly/Exchange.py
+-rw-r--r--   0 emerson    (501) staff       (20)     4125 2021-03-09 18:58:12.000000 Blankly-v0.1.1-alpha/Blankly/ProfitManager.py
+-rw-r--r--   0 emerson    (501) staff       (20)     8139 2021-03-13 23:53:31.000000 Blankly-v0.1.1-alpha/Blankly/Purchase.py
+-rw-r--r--   0 emerson    (501) staff       (20)     3264 2021-03-13 23:53:31.000000 Blankly-v0.1.1-alpha/Blankly/Server.py
+-rw-r--r--   0 emerson    (501) staff       (20)     3864 2021-03-09 18:47:28.000000 Blankly-v0.1.1-alpha/Blankly/TradingBot.py
+-rw-r--r--   0 emerson    (501) staff       (20)     1978 2021-03-09 18:47:28.000000 Blankly-v0.1.1-alpha/Blankly/Utils.py
+-rw-r--r--   0 emerson    (501) staff       (20)      138 2021-03-14 00:57:55.000000 Blankly-v0.1.1-alpha/Blankly/__init__.py
+-rw-r--r--   0 emerson    (501) staff       (20)     3059 2021-03-09 18:47:28.000000 Blankly-v0.1.1-alpha/Blankly/calc.py
+-rw-r--r--   0 emerson    (501) staff       (20)      866 2021-03-14 01:49:15.000000 Blankly-v0.1.1-alpha/PKG-INFO
+-rw-r--r--   0 emerson    (501) staff       (20)       39 2021-03-14 01:40:35.000000 Blankly-v0.1.1-alpha/setup.cfg
```

### Comparing `blankly-1.9.0b0/Blankly/exchanges/interfaces/binance/binance_websocket.py` & `Blankly-v0.1.1-alpha/Blankly/Purchase.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,208 +1,208 @@
 """
-    binance ticker class.
-    Copyright (C) 2021  Emerson Dove
+Class to manage a purchase lifecycle - a way to determine individual information about each buy and sell
+    Copyright (C) <year>  <name of author>
 
     This program is free software: you can redistribute it and/or modify
-    it under the terms of the GNU Lesser General Public License as published
+    it under the terms of the GNU Affero General Public License as published
     by the Free Software Foundation, either version 3 of the License, or
     (at your option) any later version.
 
     This program is distributed in the hope that it will be useful,
     but WITHOUT ANY WARRANTY; without even the implied warranty of
     MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-    GNU Lesser General Public License for more details.
+    GNU Affero General Public License for more details.
 
-    You should have received a copy of the GNU Lesser General Public License
+    You should have received a copy of the GNU Affero General Public License
     along with this program.  If not, see <https://www.gnu.org/licenses/>.
 """
 
-import collections
-import json
-import threading
-import traceback
+import Constants, time, Local_Account.LocalAccount, Local_Account.Trade_Local as Trade_Local
+from Utils import Utils
+class Exchange:
+    """ (Buying or selling (string), amount in currency (BTC/XLM), ticker object (so we can get time and value),
+    limit if there is one) """
+    def __init__(self, order, coinTicker, ApiCalls=None):
+        self.__buyOrSell = order["side"]
+        self.__purchaseTime = (coinTicker.getMostRecentTick())["time"]
+        # Assigned below if there is an ApiCall attached
+        self.__coinBaseId = None
+        self.__calls = ApiCalls
 
-import websocket
-
-import blankly
-import blankly.exchanges.interfaces.binance.binance_websocket_utils as websocket_utils
-from blankly.exchanges.abc_exchange_websocket import ABCExchangeWebsocket
+        try:
+            self.__limit = order["price"]
+        except Exception as e:
+            self.__limit = None
 
 
-class Tickers(ABCExchangeWebsocket):
-    def __init__(self, symbol, stream, log=None, initially_stopped=False,
-                 WEBSOCKET_URL="wss://stream.binance.com:9443/ws"):
+        self.__valueAtTime = float((coinTicker.getMostRecentTick())["price"])
+        # This is the amount before fees
+        self.__amountCurrency = order["size"]
+        self.__ticker = coinTicker
+        self.__active = True
+        self.__utils = Utils()
+        """ 
+        self.__profitable is for any degree of profitability
+        self.__reachedPastSellMin is if it's gone up a significant amount
         """
-        Create and initialize the ticker
-        Args:
-            symbol: Currency to initialize on such as "btcusdt"
-            stream: Stream to use, such as "depth" or "trade"
-            log: Fill this with a path to a log file that should be created
-            WEBSOCKET_URL: Default websocket URL feed.
-        """
-        self.__id = symbol
-        self.__stream = stream
-        self.__logging_callback, self.__interface_callback, log_message = websocket_utils.switch_type(stream)
-
-        # Initialize log file
-        if log is not None:
-            self.__log = True
-            self.__filePath = log
-            try:
-                self.__file = open(log, 'x+')
-                self.__file.write(log_message)
-            except FileExistsError:
-                self.__file = open(log, 'a')
+        self.__profitable = False
+        self.__reachedPastMinToSell = False
+        self.__sold = False
+        if self.__calls is None:
+            print("Buying locally")
+            # Fees are calculated in the tradelocal function
+            Trade_Local.tradeLocal(order["side"], self.__ticker.getCoinID(), order["size"], self.__ticker)
         else:
-            self.__log = False
+            response = self.__calls.placeOrder(order, self.__ticker, show=False)
+            self.__coinBaseId = response["id"]
 
-        self.URL = WEBSOCKET_URL
-        self.ws = None
-        self.__response = None
-        self.__most_recent_tick = None
-        self.__most_recent_time = None
-        # Create the thread object here
-        self.__thread = threading.Thread(target=self.read_websocket)
-        self.__callbacks = []
-        # This is created so that we know when a message has come back that we're waiting for
-        self.__message_count = 0
-
-        # Reload preferences
-        self.__preferences = blankly.utils.load_user_preferences()
-        buffer_size = self.__preferences["settings"]["websocket_buffer_size"]
-        self.__ticker_feed = collections.deque(maxlen=buffer_size)
-        self.__time_feed = collections.deque(maxlen=buffer_size)
-
-        # Start the websocket
-        if not initially_stopped:
-            self.start_websocket()
+    def getPurchaseTime(self):
+        return self.__purchaseTime
 
-    def start_websocket(self):
-        """
-        Restart websocket if it was asked to stop.
-        """
-        if self.ws is None:
-            self.ws = websocket.WebSocketApp(self.URL,
-                                             on_open=self.on_open,
-                                             on_message=self.on_message,
-                                             on_error=self.on_error,
-                                             on_close=self.on_close)
-            self.__thread = threading.Thread(target=self.read_websocket)
-            self.__thread.start()
+    def getSetLimit(self):
+        return self.__limit
+
+    """
+    When these orders are used the amount of currency changes throughout the lifetime by the fee rate each time
+    """
+    def getAmountCurrencyExchanged(self):
+        return self.__amountCurrency
+
+    """
+    On sell, we want to know how many dollars we got back.
+    """
+    def getDollarReturnOnSell(self):
+        # TODO
+        return None
+
+    def getBoughtOrSold(self):
+        return self.__buyOrSell
+
+    def getValueAtTime(self):
+        return self.__valueAtTime
+
+    def getCoinBaseId(self):
+        return self.__coinBaseId
+
+    def getIfActive(self):
+        return self.__active
+
+    """ Returns true if the buy order can be sold at a profit or the sell order didn't loose money """
+    def isProfitable(self, show=False):
+        if self.__buyOrSell == "buy":
+            if self.getProfitableSellPrice() < float(self.__ticker.getMostRecentTick()["price"]):
+                if show:
+                    print (True)
+                return True
+            else:
+                if show:
+                    print (False)
+                return False
         else:
-            if self.__thread.is_alive():
-                print("Already running...")
-                pass
+            if self.getProfitableSellPrice() > float(self.__ticker.getMostRecentTick()["price"]):
+                if show:
+                    print (True)
+                return True
             else:
-                # Use recursion to restart, continue appending to time feed and ticker feed
-                self.ws = None
-                self.start_websocket()
-
-    def read_websocket(self):
-        # Main thread to sit here and run
-        self.ws.run_forever()
-        # This repeats the close behavior just in case something happens
-
-    def on_message(self, ws, message):
-        self.__message_count += 1
-        message = json.loads(message)
-        try:
-            self.__most_recent_time = message['E']
-            self.__time_feed.append(self.__most_recent_time)
-
-            # Run callbacks on message
-            if self.__log:
-                if self.__message_count % 100 == 0:
-                    self.__file.close()
-                    self.__file = open(self.__filePath, 'a')
-                line = self.__logging_callback(message)
-                self.__file.write(line)
-
-            interface_message = self.__interface_callback(message)
-            self.__ticker_feed.append(interface_message)
-            self.__most_recent_tick = interface_message
-            for i in self.__callbacks:
-                i(interface_message)
-        except KeyError:
-            # If the try below figures this out then we don't have to traceback
-            error_found = False
+                if show:
+                    print (False)
+                return False
+
+        # Old algorithm that didn't take into account the change in amount actually bought because of the fee
+        # print("Before fees: " + str((self.__valueAtTime * self.__amountCurrency)))
+        # then = (self.__valueAtTime * self.__amountCurrency)
+        # now = (float((self.__ticker.getMostRecentTick())["price"]) * self.__amountCurrency)
+        # if show:
+        #     print("Before fees now: " + str(now))
+        #     print("Before fees then: " + str(then))
+        #     print("Difference with fees: " + str(((now - (now * Constants.PRETEND_FEE_RATE)) - (then - (then * Constants.PRETEND_FEE_RATE)))))
+        #
+        # if self.__buyOrSell == "buy":
+        #     if ((now - (now * Constants.PRETEND_FEE_RATE)) - (then - (then * Constants.PRETEND_FEE_RATE))) > 0:
+        #         return True
+        #     else:
+        #         return False
+        # else:
+        #     if ((then - (then * Constants.PRETEND_FEE_RATE)) - (now - (now * Constants.PRETEND_FEE_RATE))) > 0:
+        #         return True
+        #     else:
+        #         return False
+
+    def getFee(self, show=False):
+        fee = (self.__valueAtTime * self.__amountCurrency) * Constants.PRETEND_FEE_RATE
+        if (show):
+            print (fee)
+        return fee
+
+    def cancelOrder(self):
+        if self.__calls is not None:
+            response = self.__calls.deleteOrder(self.__coinBaseId, show=False)
             try:
-                if message['result'] is None:
-                    self.__response = message
-                    error_found = True
-            except KeyError:
-                traceback.print_exc()
-
-            if not error_found:
-                traceback.print_exc()
-
-    def on_error(self, ws, error):
-        print(error)
-
-    def on_close(self, ws):
-        # This repeats the close behavior just in case something happens
-        pass
-
-    def on_open(self, ws):
-        request = """
-        {
-            "method": "SUBSCRIBE",
-            "params": [
-                \"""" + self.__id + "@" + self.__stream + """\"
-            ],
-            "id": 1
-        }
-        """
-        ws.send(request)
-
-    """ Required in manager """
-
-    def is_websocket_open(self):
-        return self.__thread.is_alive()
-
-    def get_currency_id(self):
-        return self.__id
-
-    """ Required in manager """
-
-    def append_callback(self, obj):
-        self.__callbacks.append(obj)
-
-    """ Define a variable each time so there is no array manipulation """
-    """ Required in manager """
-
-    def get_most_recent_tick(self):
-        return self.__most_recent_tick
-
-    """ Required in manager """
-
-    def get_most_recent_time(self):
-        return self.__most_recent_time
-
-    """ Required in manager """
-
-    def get_time_feed(self):
-        return list(self.__time_feed)
-
-    """ Parallel with time feed """
-    """ Required in manager """
-
-    def get_feed(self):
-        return list(self.__ticker_feed)
-
-    """ Required in manager """
-
-    def get_response(self):
-        return self.__response
-
-    """ Required in manager """
+                if response["message"] == "Unauthorized.":
+                    print("Not authorized to delete order: " + self.__coinBaseId)
+            except TypeError as e:
+                print("Canceled Order " + response)
+            except Exception as e:
+                print("FAILED to cancel order " + self.__coinBaseId)
+            self.__active = False
+        else:
+            print("Cannot cancel order")
 
-    def close_websocket(self):
-        if self.__thread.is_alive():
-            self.ws.close()
+    def confirmCanceled(self):
+        if self.__calls is not None:
+            response = self.__calls.getOpenOrders()
+            for i in range(len(response)):
+                if (response[i]["id"] == self.__coinBaseId):
+                    return False
+            self.__active = False
+            return True
         else:
-            print("Websocket for " + self.__id + '@' + self.__stream + " is already closed")
+            return "Cannot confirm cancellation"
 
-    """ Required in manager """
+    """ 
+    Returns the price that a BUY needs to reach to be profitable
+    Ths can be used to set limit orders
+    """
+    def getProfitableSellPrice(self, show=False):
+        # price = self.__valueAtTime/(1 - Constants.PRETEND_FEE_RATE)
+        # This one didn't work for the USD amount modified
+        # price = self.__valueAtTime/(1 - (2 * Constants.PRETEND_FEE_RATE) + (Constants.PRETEND_FEE_RATE * Constants.PRETEND_FEE_RATE))
+        price = ((Constants.PRETEND_FEE_RATE + 1)*(self.__valueAtTime)/(1-Constants.PRETEND_FEE_RATE))
+        if show:
+            print(price)
+        return price
+
+    """ 
+    This allows this to be checked if this buy became profitable 
+    """
+    def inProfitableSellZone(self, show=False):
+        self.__profitable = float((self.__ticker.getMostRecentTick()["price"])) > self.getProfitableSellPrice()
+        if show:
+            print(self.__profitable)
+        return self.__profitable
+
+    """ 
+    Allows this exchange to be sold back in its entirety 
+    """
+    # TODO - This has turned into spaghetti code, fix it
+    def sellSelf(self):
+        if self.__calls is not None:
+            # This doesn't need the fee calculation because that happens anyway
+            self.__calls.placeOrder(self.__utils.generateMarketOrder(self.__amountCurrency, "sell", self.__ticker.getCoinID()))
+            Trade_Local.tradeLocal("sell", self.__ticker.getCoinID(), self.__amountCurrency, self.__ticker)
+        else:
+            print("Selling locally only")
+            # This one needs to include fees before and after
+            self.__utils.tradeLocal("sell", self.__ticker.getCoinID(), self.__amountCurrency, self.__ticker)
+        self.__sold = True
+
+
+    def setIfPastSellMin(self, val):
+        self.__reachedPastMinToSell = val
+
+    def getIfPastSellMin(self, show=False):
+        if show:
+            print(self.__reachedPastMinToSell)
+        return self.__reachedPastMinToSell
 
-    def restart_ticker(self):
-        self.start_websocket()
+    def getIfSold(self):
+        return self.__sold
```

