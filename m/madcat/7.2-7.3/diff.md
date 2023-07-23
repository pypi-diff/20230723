# Comparing `tmp/madcat-7.2.tar.gz` & `tmp/madcat-7.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "madcat-7.2.tar", last modified: Thu Jul 20 13:52:06 2023, max compression
+gzip compressed data, was "madcat-7.3.tar", last modified: Sun Jul 23 08:38:45 2023, max compression
```

## Comparing `madcat-7.2.tar` & `madcat-7.3.tar`

### file list

```diff
@@ -1,172 +1,172 @@
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.644204 madcat-7.2/
--rw-r--r--   0 amitosi    (501) staff       (20)      189 2023-07-20 13:52:06.644066 madcat-7.2/PKG-INFO
--rw-r--r--   0 amitosi    (501) staff       (20)     1367 2023-03-22 15:02:11.000000 madcat-7.2/README.md
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.616498 madcat-7.2/chester/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/__init__.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.617478 madcat-7.2/chester/cleaning/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/cleaning/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1726 2023-02-14 11:01:28.000000 madcat-7.2/chester/cleaning/cleaner_handler.py
--rw-r--r--   0 amitosi    (501) staff       (20)     8913 2023-02-14 11:10:19.000000 madcat-7.2/chester/cleaning/cleaning_func.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.617795 madcat-7.2/chester/data/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-16 07:01:02.000000 madcat-7.2/chester/data/__init__.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.618044 madcat-7.2/chester/data_loader/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/data_loader/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)      693 2023-02-10 12:03:58.000000 madcat-7.2/chester/data_loader/webtext_data.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.618470 madcat-7.2/chester/feature_analyzing/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/feature_analyzing/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     7767 2023-02-12 13:00:40.000000 madcat-7.2/chester/feature_analyzing/feature_correlation.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.620101 madcat-7.2/chester/feature_stats/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/feature_stats/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     6078 2023-07-20 13:21:31.000000 madcat-7.2/chester/feature_stats/categorical_stats.py
--rw-r--r--   0 amitosi    (501) staff       (20)      214 2023-02-08 10:13:48.000000 madcat-7.2/chester/feature_stats/feature_stats.py
--rw-r--r--   0 amitosi    (501) staff       (20)     5521 2023-02-14 12:45:27.000000 madcat-7.2/chester/feature_stats/numeric_stats.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2152 2023-03-21 07:33:39.000000 madcat-7.2/chester/feature_stats/text_stats.py
--rw-r--r--   0 amitosi    (501) staff       (20)     7362 2023-07-20 13:46:16.000000 madcat-7.2/chester/feature_stats/time_series_stats.py
--rw-r--r--   0 amitosi    (501) staff       (20)      646 2023-02-14 14:21:02.000000 madcat-7.2/chester/feature_stats/utils.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.621585 madcat-7.2/chester/features_engineering/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/features_engineering/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2222 2023-02-05 11:09:58.000000 madcat-7.2/chester/features_engineering/bag_of_words.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2218 2023-03-07 08:09:18.000000 madcat-7.2/chester/features_engineering/corex.py
--rw-r--r--   0 amitosi    (501) staff       (20)     6275 2023-03-07 06:57:19.000000 madcat-7.2/chester/features_engineering/fe_nlp.py
--rw-r--r--   0 amitosi    (501) staff       (20)     4745 2023-03-21 07:33:39.000000 madcat-7.2/chester/features_engineering/feature_handler.py
--rw-r--r--   0 amitosi    (501) staff       (20)     3355 2023-03-07 07:20:49.000000 madcat-7.2/chester/features_engineering/features_handler.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1970 2023-02-05 11:09:58.000000 madcat-7.2/chester/features_engineering/tfidf.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.624077 madcat-7.2/chester/features_engineering/time_series/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-15 07:10:16.000000 madcat-7.2/chester/features_engineering/time_series/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1829 2023-02-17 09:22:41.000000 madcat-7.2/chester/features_engineering/time_series/cyclic_features_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     4455 2023-02-16 13:45:22.000000 madcat-7.2/chester/features_engineering/time_series/event_counter.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1909 2023-02-27 19:09:23.000000 madcat-7.2/chester/features_engineering/time_series/feature_elimination_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     5399 2023-07-20 13:34:44.000000 madcat-7.2/chester/features_engineering/time_series/frequencies_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     5317 2023-02-18 11:46:20.000000 madcat-7.2/chester/features_engineering/time_series/get_time_freqeuency_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     4379 2023-02-16 14:20:54.000000 madcat-7.2/chester/features_engineering/time_series/moving_metric_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     3355 2023-07-20 13:32:39.000000 madcat-7.2/chester/features_engineering/time_series/static_features_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     4977 2023-07-20 13:40:26.000000 madcat-7.2/chester/features_engineering/time_series/ts_feature_extraction.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1103 2023-07-20 13:41:21.000000 madcat-7.2/chester/features_engineering/time_series/ts_features_extraction.py
--rw-r--r--   0 amitosi    (501) staff       (20)      379 2023-02-17 14:38:52.000000 madcat-7.2/chester/features_engineering/time_series/ts_utils.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.624400 madcat-7.2/chester/model_analyzer/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/model_analyzer/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)    11364 2023-02-19 08:56:08.000000 madcat-7.2/chester/model_analyzer/model_analysis.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.625366 madcat-7.2/chester/model_monitor/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/model_monitor/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)      887 2023-02-10 12:10:10.000000 madcat-7.2/chester/model_monitor/calculate_scores_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     5339 2023-07-19 14:00:30.000000 madcat-7.2/chester/model_monitor/error_prediction.py
--rw-r--r--   0 amitosi    (501) staff       (20)     4219 2023-07-19 14:00:30.000000 madcat-7.2/chester/model_monitor/model_boostrap.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.626059 madcat-7.2/chester/model_training/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/model_training/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     3427 2023-02-05 19:57:36.000000 madcat-7.2/chester/model_training/data_preparation.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2149 2023-02-11 16:14:05.000000 madcat-7.2/chester/model_training/model_utils.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.626831 madcat-7.2/chester/model_training/models/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/model_training/models/__init__.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.628872 madcat-7.2/chester/model_training/models/chester_models/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/model_training/models/chester_models/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1977 2023-02-11 10:13:40.000000 madcat-7.2/chester/model_training/models/chester_models/base_model.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2160 2023-02-10 12:10:10.000000 madcat-7.2/chester/model_training/models/chester_models/base_model_utils.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.629535 madcat-7.2/chester/model_training/models/chester_models/baseline/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/model_training/models/chester_models/baseline/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1012 2023-02-12 12:18:36.000000 madcat-7.2/chester/model_training/models/chester_models/baseline/baseline_model.py
--rw-r--r--   0 amitosi    (501) staff       (20)     3519 2023-02-10 12:10:10.000000 madcat-7.2/chester/model_training/models/chester_models/baseline/baseline_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1965 2023-02-12 12:18:36.000000 madcat-7.2/chester/model_training/models/chester_models/best_baseline_model.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1659 2023-07-20 13:04:51.000000 madcat-7.2/chester/model_training/models/chester_models/best_linear_regression.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1917 2023-02-14 15:09:08.000000 madcat-7.2/chester/model_training/models/chester_models/best_logistic_regression.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2354 2023-07-19 14:09:20.000000 madcat-7.2/chester/model_training/models/chester_models/best_model.py
--rw-r--r--   0 amitosi    (501) staff       (20)     5160 2023-07-19 14:09:20.000000 madcat-7.2/chester/model_training/models/chester_models/compare_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1750 2023-02-10 12:10:30.000000 madcat-7.2/chester/model_training/models/chester_models/hp_generator.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.630056 madcat-7.2/chester/model_training/models/chester_models/linear_regression/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/model_training/models/chester_models/linear_regression/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2429 2023-02-17 12:12:20.000000 madcat-7.2/chester/model_training/models/chester_models/linear_regression/linear_regression.py
--rw-r--r--   0 amitosi    (501) staff       (20)     6891 2023-02-10 12:10:10.000000 madcat-7.2/chester/model_training/models/chester_models/linear_regression/linear_regression_utils.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.630571 madcat-7.2/chester/model_training/models/chester_models/logistic_regression/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/model_training/models/chester_models/logistic_regression/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2542 2023-02-14 15:54:46.000000 madcat-7.2/chester/model_training/models/chester_models/logistic_regression/logistic_regression_model.py
--rw-r--r--   0 amitosi    (501) staff       (20)     6637 2023-02-10 12:10:10.000000 madcat-7.2/chester/model_training/models/chester_models/logistic_regression/logistic_regression_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2040 2023-02-05 11:09:58.000000 madcat-7.2/chester/model_training/models/cv_training.py
--rw-r--r--   0 amitosi    (501) staff       (20)     4764 2023-02-05 11:09:58.000000 madcat-7.2/chester/model_training/models/lstm.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1155 2023-02-10 12:20:48.000000 madcat-7.2/chester/model_training/models/scoring.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.631087 madcat-7.2/chester/post_model_analysis/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/post_model_analysis/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)    12668 2023-02-23 10:52:06.000000 madcat-7.2/chester/post_model_analysis/post_model_analysis_class.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1492 2023-02-11 16:14:05.000000 madcat-7.2/chester/post_model_analysis/post_regression.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.632262 madcat-7.2/chester/pre_model_analysis/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/pre_model_analysis/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)    15538 2023-03-11 12:30:17.000000 madcat-7.2/chester/pre_model_analysis/categorical.py
--rw-r--r--   0 amitosi    (501) staff       (20)    15136 2023-03-21 11:25:00.000000 madcat-7.2/chester/pre_model_analysis/numerics.py
--rw-r--r--   0 amitosi    (501) staff       (20)     9856 2023-02-19 19:27:25.000000 madcat-7.2/chester/pre_model_analysis/target.py
--rw-r--r--   0 amitosi    (501) staff       (20)     3383 2023-02-20 16:04:59.000000 madcat-7.2/chester/pre_model_analysis/time_series.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.632914 madcat-7.2/chester/preprocessing/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/preprocessing/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     5096 2023-02-14 11:12:55.000000 madcat-7.2/chester/preprocessing/preprocessing_func.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1661 2023-03-07 06:13:34.000000 madcat-7.2/chester/preprocessing/preprocessor_handler.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.633900 madcat-7.2/chester/run/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-08 09:40:57.000000 madcat-7.2/chester/run/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1786 2023-02-11 11:52:10.000000 madcat-7.2/chester/run/chapter_titles.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2779 2023-02-08 21:21:02.000000 madcat-7.2/chester/run/feature_attention_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)    16206 2023-03-21 07:53:41.000000 madcat-7.2/chester/run/full_run.py
--rw-r--r--   0 amitosi    (501) staff       (20)     5035 2023-03-21 07:33:39.000000 madcat-7.2/chester/run/user_classes.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.634715 madcat-7.2/chester/run_manual_chester/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 13:32:50.000000 madcat-7.2/chester/run_manual_chester/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)    19378 2023-07-20 13:06:20.000000 madcat-7.2/chester/run_manual_chester/manual_run.py
--rw-r--r--   0 amitosi    (501) staff       (20)      399 2023-07-20 10:55:05.000000 madcat-7.2/chester/run_manual_chester/pg.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.636764 madcat-7.2/chester/text_stats_analysis/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/text_stats_analysis/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1261 2023-02-14 11:53:21.000000 madcat-7.2/chester/text_stats_analysis/common_words.py
--rw-r--r--   0 amitosi    (501) staff       (20)     3708 2023-07-20 11:01:12.000000 madcat-7.2/chester/text_stats_analysis/corex_topics.py
--rw-r--r--   0 amitosi    (501) staff       (20)     4446 2023-03-21 07:33:39.000000 madcat-7.2/chester/text_stats_analysis/data_quality.py
--rw-r--r--   0 amitosi    (501) staff       (20)     3466 2023-02-14 12:12:27.000000 madcat-7.2/chester/text_stats_analysis/key_sentences.py
--rw-r--r--   0 amitosi    (501) staff       (20)     3663 2023-02-14 12:20:36.000000 madcat-7.2/chester/text_stats_analysis/keywords_extraction.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1951 2023-02-14 14:04:54.000000 madcat-7.2/chester/text_stats_analysis/sentiment.py
--rw-r--r--   0 amitosi    (501) staff       (20)    10355 2023-03-21 07:33:39.000000 madcat-7.2/chester/text_stats_analysis/smart_text_analyzer.py
--rw-r--r--   0 amitosi    (501) staff       (20)     4118 2023-03-21 07:33:39.000000 madcat-7.2/chester/text_stats_analysis/text_summary.py
--rw-r--r--   0 amitosi    (501) staff       (20)      526 2023-02-11 16:14:05.000000 madcat-7.2/chester/text_stats_analysis/word_cloud.py
--rw-r--r--   0 amitosi    (501) staff       (20)     5304 2023-02-19 09:26:17.000000 madcat-7.2/chester/util.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.637262 madcat-7.2/chester/utils/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.2/chester/utils/__init__.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.637855 madcat-7.2/chester/zero_break/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.2/chester/zero_break/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)       89 2023-02-05 11:09:58.000000 madcat-7.2/chester/zero_break/get_or_else.py
--rw-r--r--   0 amitosi    (501) staff       (20)     8904 2023-07-19 14:09:20.000000 madcat-7.2/chester/zero_break/problem_specification.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1694 2023-03-11 12:21:56.000000 madcat-7.2/chester/zero_break/text_detector.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.638175 madcat-7.2/example_notebooks/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-03-11 13:38:57.000000 madcat-7.2/example_notebooks/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2981 2023-03-11 15:08:39.000000 madcat-7.2/example_notebooks/main.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.638857 madcat-7.2/madcat.egg-info/
--rw-r--r--   0 amitosi    (501) staff       (20)      189 2023-07-20 13:52:06.000000 madcat-7.2/madcat.egg-info/PKG-INFO
--rw-r--r--   0 amitosi    (501) staff       (20)     5766 2023-07-20 13:52:06.000000 madcat-7.2/madcat.egg-info/SOURCES.txt
--rw-r--r--   0 amitosi    (501) staff       (20)        1 2023-07-20 13:52:06.000000 madcat-7.2/madcat.egg-info/dependency_links.txt
--rw-r--r--   0 amitosi    (501) staff       (20)      273 2023-07-20 13:52:06.000000 madcat-7.2/madcat.egg-info/requires.txt
--rw-r--r--   0 amitosi    (501) staff       (20)       33 2023-07-20 13:52:06.000000 madcat-7.2/madcat.egg-info/top_level.txt
--rw-r--r--   0 amitosi    (501) staff       (20)       38 2023-07-20 13:52:06.644258 madcat-7.2/setup.cfg
--rw-r--r--   0 amitosi    (501) staff       (20)      559 2023-07-20 13:51:32.000000 madcat-7.2/setup.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.639263 madcat-7.2/tamtam/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 07:37:31.000000 madcat-7.2/tamtam/__init__.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.640326 madcat-7.2/tamtam/ab_feature_analysis/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-23 10:02:44.000000 madcat-7.2/tamtam/ab_feature_analysis/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)      541 2023-02-23 10:19:25.000000 madcat-7.2/tamtam/ab_feature_analysis/ab_catboost.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1923 2023-03-21 07:53:41.000000 madcat-7.2/tamtam/ab_feature_analysis/ab_feature_analysis_class.py
--rw-r--r--   0 amitosi    (501) staff       (20)      348 2023-02-23 10:19:25.000000 madcat-7.2/tamtam/ab_feature_analysis/ab_partial_plot.py
--rw-r--r--   0 amitosi    (501) staff       (20)      402 2023-02-23 10:19:25.000000 madcat-7.2/tamtam/ab_feature_analysis/ab_tree_class.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.640710 madcat-7.2/tamtam/ab_info/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 07:44:45.000000 madcat-7.2/tamtam/ab_info/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     4011 2023-02-23 21:52:11.000000 madcat-7.2/tamtam/ab_info/ab_class.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.641240 madcat-7.2/tamtam/allocation_calculation/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 13:01:46.000000 madcat-7.2/tamtam/allocation_calculation/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1937 2023-02-22 14:13:02.000000 madcat-7.2/tamtam/allocation_calculation/bias_class.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.641637 madcat-7.2/tamtam/delta_analysis/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-23 07:37:32.000000 madcat-7.2/tamtam/delta_analysis/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     6199 2023-02-23 21:48:17.000000 madcat-7.2/tamtam/delta_analysis/delta_class.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2517 2023-02-23 21:45:56.000000 madcat-7.2/tamtam/manual_run.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.641975 madcat-7.2/tamtam/metrics_correlation/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 14:27:03.000000 madcat-7.2/tamtam/metrics_correlation/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2350 2023-02-23 14:45:57.000000 madcat-7.2/tamtam/metrics_correlation/metric_class.py
--rw-r--r--   0 amitosi    (501) staff       (20)      964 2023-02-23 14:45:57.000000 madcat-7.2/tamtam/run.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.642332 madcat-7.2/tamtam/user_class/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 07:41:13.000000 madcat-7.2/tamtam/user_class/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)     1895 2023-02-23 11:53:41.000000 madcat-7.2/tamtam/user_class/user_class.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.642917 madcat-7.2/tamtam/utils/
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 10:08:15.000000 madcat-7.2/tamtam/utils/__init__.py
--rw-r--r--   0 amitosi    (501) staff       (20)       54 2023-02-22 16:12:56.000000 madcat-7.2/tamtam/utils/column_utils.py
--rw-r--r--   0 amitosi    (501) staff       (20)       59 2023-02-22 16:24:31.000000 madcat-7.2/tamtam/utils/utils.py
-drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-20 13:52:06.643839 madcat-7.2/tests/
--rw-r--r--   0 amitosi    (501) staff       (20)     2501 2023-02-05 11:09:51.000000 madcat-7.2/tests/test_cleaning.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2119 2023-02-05 11:09:51.000000 madcat-7.2/tests/test_preprocessing.py
--rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:51.000000 madcat-7.2/tests/test_util.py
--rw-r--r--   0 amitosi    (501) staff       (20)     2843 2023-02-05 11:09:58.000000 madcat-7.2/tests/test_zero_break.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.395571 madcat-7.3/
+-rw-r--r--   0 amitosi    (501) staff       (20)      189 2023-07-23 08:38:45.395419 madcat-7.3/PKG-INFO
+-rw-r--r--   0 amitosi    (501) staff       (20)     1367 2023-03-22 15:02:11.000000 madcat-7.3/README.md
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.347810 madcat-7.3/chester/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/__init__.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.348690 madcat-7.3/chester/cleaning/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/cleaning/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1726 2023-02-14 11:01:28.000000 madcat-7.3/chester/cleaning/cleaner_handler.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     8913 2023-02-14 11:10:19.000000 madcat-7.3/chester/cleaning/cleaning_func.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.348947 madcat-7.3/chester/data/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-16 07:01:02.000000 madcat-7.3/chester/data/__init__.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.349129 madcat-7.3/chester/data_loader/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/data_loader/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      693 2023-02-10 12:03:58.000000 madcat-7.3/chester/data_loader/webtext_data.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.349444 madcat-7.3/chester/feature_analyzing/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/feature_analyzing/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     7767 2023-02-12 13:00:40.000000 madcat-7.3/chester/feature_analyzing/feature_correlation.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.351122 madcat-7.3/chester/feature_stats/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/feature_stats/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     6078 2023-07-20 13:21:31.000000 madcat-7.3/chester/feature_stats/categorical_stats.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      214 2023-02-08 10:13:48.000000 madcat-7.3/chester/feature_stats/feature_stats.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     5521 2023-02-14 12:45:27.000000 madcat-7.3/chester/feature_stats/numeric_stats.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2152 2023-03-21 07:33:39.000000 madcat-7.3/chester/feature_stats/text_stats.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     7362 2023-07-20 13:46:16.000000 madcat-7.3/chester/feature_stats/time_series_stats.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      646 2023-02-14 14:21:02.000000 madcat-7.3/chester/feature_stats/utils.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.352704 madcat-7.3/chester/features_engineering/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/features_engineering/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2222 2023-02-05 11:09:58.000000 madcat-7.3/chester/features_engineering/bag_of_words.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2218 2023-03-07 08:09:18.000000 madcat-7.3/chester/features_engineering/corex.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     6275 2023-03-07 06:57:19.000000 madcat-7.3/chester/features_engineering/fe_nlp.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     4745 2023-03-21 07:33:39.000000 madcat-7.3/chester/features_engineering/feature_handler.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     3355 2023-03-07 07:20:49.000000 madcat-7.3/chester/features_engineering/features_handler.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1970 2023-02-05 11:09:58.000000 madcat-7.3/chester/features_engineering/tfidf.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.355387 madcat-7.3/chester/features_engineering/time_series/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-15 07:10:16.000000 madcat-7.3/chester/features_engineering/time_series/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1829 2023-02-17 09:22:41.000000 madcat-7.3/chester/features_engineering/time_series/cyclic_features_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     4455 2023-02-16 13:45:22.000000 madcat-7.3/chester/features_engineering/time_series/event_counter.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1909 2023-02-27 19:09:23.000000 madcat-7.3/chester/features_engineering/time_series/feature_elimination_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     5399 2023-07-20 13:34:44.000000 madcat-7.3/chester/features_engineering/time_series/frequencies_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     5317 2023-02-18 11:46:20.000000 madcat-7.3/chester/features_engineering/time_series/get_time_freqeuency_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     4379 2023-02-16 14:20:54.000000 madcat-7.3/chester/features_engineering/time_series/moving_metric_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     3355 2023-07-20 13:32:39.000000 madcat-7.3/chester/features_engineering/time_series/static_features_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     4977 2023-07-20 13:40:26.000000 madcat-7.3/chester/features_engineering/time_series/ts_feature_extraction.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1103 2023-07-20 13:41:21.000000 madcat-7.3/chester/features_engineering/time_series/ts_features_extraction.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      379 2023-02-17 14:38:52.000000 madcat-7.3/chester/features_engineering/time_series/ts_utils.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.355701 madcat-7.3/chester/model_analyzer/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/model_analyzer/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)    11364 2023-02-19 08:56:08.000000 madcat-7.3/chester/model_analyzer/model_analysis.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.356628 madcat-7.3/chester/model_monitor/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/model_monitor/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      887 2023-02-10 12:10:10.000000 madcat-7.3/chester/model_monitor/calculate_scores_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     5339 2023-07-19 14:00:30.000000 madcat-7.3/chester/model_monitor/error_prediction.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     4219 2023-07-19 14:00:30.000000 madcat-7.3/chester/model_monitor/model_boostrap.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.357208 madcat-7.3/chester/model_training/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/model_training/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     3427 2023-02-05 19:57:36.000000 madcat-7.3/chester/model_training/data_preparation.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2149 2023-02-11 16:14:05.000000 madcat-7.3/chester/model_training/model_utils.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.357931 madcat-7.3/chester/model_training/models/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/model_training/models/__init__.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.360049 madcat-7.3/chester/model_training/models/chester_models/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/model_training/models/chester_models/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1977 2023-02-11 10:13:40.000000 madcat-7.3/chester/model_training/models/chester_models/base_model.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2160 2023-02-10 12:10:10.000000 madcat-7.3/chester/model_training/models/chester_models/base_model_utils.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.360721 madcat-7.3/chester/model_training/models/chester_models/baseline/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/model_training/models/chester_models/baseline/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1012 2023-02-12 12:18:36.000000 madcat-7.3/chester/model_training/models/chester_models/baseline/baseline_model.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     3519 2023-02-10 12:10:10.000000 madcat-7.3/chester/model_training/models/chester_models/baseline/baseline_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1965 2023-02-12 12:18:36.000000 madcat-7.3/chester/model_training/models/chester_models/best_baseline_model.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1659 2023-07-20 13:04:51.000000 madcat-7.3/chester/model_training/models/chester_models/best_linear_regression.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1917 2023-02-14 15:09:08.000000 madcat-7.3/chester/model_training/models/chester_models/best_logistic_regression.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2354 2023-07-19 14:09:20.000000 madcat-7.3/chester/model_training/models/chester_models/best_model.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     5160 2023-07-19 14:09:20.000000 madcat-7.3/chester/model_training/models/chester_models/compare_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1750 2023-02-10 12:10:30.000000 madcat-7.3/chester/model_training/models/chester_models/hp_generator.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.361300 madcat-7.3/chester/model_training/models/chester_models/linear_regression/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/model_training/models/chester_models/linear_regression/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2429 2023-02-17 12:12:20.000000 madcat-7.3/chester/model_training/models/chester_models/linear_regression/linear_regression.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     6891 2023-02-10 12:10:10.000000 madcat-7.3/chester/model_training/models/chester_models/linear_regression/linear_regression_utils.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.361833 madcat-7.3/chester/model_training/models/chester_models/logistic_regression/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/model_training/models/chester_models/logistic_regression/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2542 2023-02-14 15:54:46.000000 madcat-7.3/chester/model_training/models/chester_models/logistic_regression/logistic_regression_model.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     6637 2023-02-10 12:10:10.000000 madcat-7.3/chester/model_training/models/chester_models/logistic_regression/logistic_regression_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2040 2023-02-05 11:09:58.000000 madcat-7.3/chester/model_training/models/cv_training.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     4764 2023-02-05 11:09:58.000000 madcat-7.3/chester/model_training/models/lstm.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1155 2023-02-10 12:20:48.000000 madcat-7.3/chester/model_training/models/scoring.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.362412 madcat-7.3/chester/post_model_analysis/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/post_model_analysis/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)    12668 2023-02-23 10:52:06.000000 madcat-7.3/chester/post_model_analysis/post_model_analysis_class.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1492 2023-02-11 16:14:05.000000 madcat-7.3/chester/post_model_analysis/post_regression.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.363594 madcat-7.3/chester/pre_model_analysis/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/pre_model_analysis/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)    15538 2023-03-11 12:30:17.000000 madcat-7.3/chester/pre_model_analysis/categorical.py
+-rw-r--r--   0 amitosi    (501) staff       (20)    15136 2023-03-21 11:25:00.000000 madcat-7.3/chester/pre_model_analysis/numerics.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     9856 2023-02-19 19:27:25.000000 madcat-7.3/chester/pre_model_analysis/target.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     3383 2023-02-20 16:04:59.000000 madcat-7.3/chester/pre_model_analysis/time_series.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.364185 madcat-7.3/chester/preprocessing/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/preprocessing/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     5096 2023-02-14 11:12:55.000000 madcat-7.3/chester/preprocessing/preprocessing_func.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1661 2023-03-07 06:13:34.000000 madcat-7.3/chester/preprocessing/preprocessor_handler.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.365322 madcat-7.3/chester/run/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-08 09:40:57.000000 madcat-7.3/chester/run/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1786 2023-02-11 11:52:10.000000 madcat-7.3/chester/run/chapter_titles.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2779 2023-02-08 21:21:02.000000 madcat-7.3/chester/run/feature_attention_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)    16206 2023-03-21 07:53:41.000000 madcat-7.3/chester/run/full_run.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     5035 2023-03-21 07:33:39.000000 madcat-7.3/chester/run/user_classes.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.366074 madcat-7.3/chester/run_manual_chester/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 13:32:50.000000 madcat-7.3/chester/run_manual_chester/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)    19378 2023-07-20 13:06:20.000000 madcat-7.3/chester/run_manual_chester/manual_run.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      204 2023-07-21 11:54:17.000000 madcat-7.3/chester/run_manual_chester/pg.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.386504 madcat-7.3/chester/text_stats_analysis/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/text_stats_analysis/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1261 2023-02-14 11:53:21.000000 madcat-7.3/chester/text_stats_analysis/common_words.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     3708 2023-07-20 11:01:12.000000 madcat-7.3/chester/text_stats_analysis/corex_topics.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     4446 2023-03-21 07:33:39.000000 madcat-7.3/chester/text_stats_analysis/data_quality.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     3466 2023-02-14 12:12:27.000000 madcat-7.3/chester/text_stats_analysis/key_sentences.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     3663 2023-02-14 12:20:36.000000 madcat-7.3/chester/text_stats_analysis/keywords_extraction.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1951 2023-02-14 14:04:54.000000 madcat-7.3/chester/text_stats_analysis/sentiment.py
+-rw-r--r--   0 amitosi    (501) staff       (20)    10355 2023-03-21 07:33:39.000000 madcat-7.3/chester/text_stats_analysis/smart_text_analyzer.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     4118 2023-03-21 07:33:39.000000 madcat-7.3/chester/text_stats_analysis/text_summary.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      526 2023-02-11 16:14:05.000000 madcat-7.3/chester/text_stats_analysis/word_cloud.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     5304 2023-02-19 09:26:17.000000 madcat-7.3/chester/util.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.387055 madcat-7.3/chester/utils/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:59.000000 madcat-7.3/chester/utils/__init__.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.387874 madcat-7.3/chester/zero_break/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:58.000000 madcat-7.3/chester/zero_break/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)       89 2023-02-05 11:09:58.000000 madcat-7.3/chester/zero_break/get_or_else.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     8904 2023-07-19 14:09:20.000000 madcat-7.3/chester/zero_break/problem_specification.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1694 2023-03-11 12:21:56.000000 madcat-7.3/chester/zero_break/text_detector.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.388765 madcat-7.3/example_notebooks/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-03-11 13:38:57.000000 madcat-7.3/example_notebooks/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2981 2023-03-11 15:08:39.000000 madcat-7.3/example_notebooks/main.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.389635 madcat-7.3/madcat.egg-info/
+-rw-r--r--   0 amitosi    (501) staff       (20)      189 2023-07-23 08:38:45.000000 madcat-7.3/madcat.egg-info/PKG-INFO
+-rw-r--r--   0 amitosi    (501) staff       (20)     5766 2023-07-23 08:38:45.000000 madcat-7.3/madcat.egg-info/SOURCES.txt
+-rw-r--r--   0 amitosi    (501) staff       (20)        1 2023-07-23 08:38:45.000000 madcat-7.3/madcat.egg-info/dependency_links.txt
+-rw-r--r--   0 amitosi    (501) staff       (20)      260 2023-07-23 08:38:45.000000 madcat-7.3/madcat.egg-info/requires.txt
+-rw-r--r--   0 amitosi    (501) staff       (20)       33 2023-07-23 08:38:45.000000 madcat-7.3/madcat.egg-info/top_level.txt
+-rw-r--r--   0 amitosi    (501) staff       (20)       38 2023-07-23 08:38:45.395608 madcat-7.3/setup.cfg
+-rw-r--r--   0 amitosi    (501) staff       (20)      558 2023-07-23 08:38:22.000000 madcat-7.3/setup.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.390166 madcat-7.3/tamtam/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 07:37:31.000000 madcat-7.3/tamtam/__init__.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.391638 madcat-7.3/tamtam/ab_feature_analysis/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-23 10:02:44.000000 madcat-7.3/tamtam/ab_feature_analysis/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      541 2023-02-23 10:19:25.000000 madcat-7.3/tamtam/ab_feature_analysis/ab_catboost.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1923 2023-03-21 07:53:41.000000 madcat-7.3/tamtam/ab_feature_analysis/ab_feature_analysis_class.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      348 2023-02-23 10:19:25.000000 madcat-7.3/tamtam/ab_feature_analysis/ab_partial_plot.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      402 2023-02-23 10:19:25.000000 madcat-7.3/tamtam/ab_feature_analysis/ab_tree_class.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.392024 madcat-7.3/tamtam/ab_info/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 07:44:45.000000 madcat-7.3/tamtam/ab_info/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     4011 2023-02-23 21:52:11.000000 madcat-7.3/tamtam/ab_info/ab_class.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.392527 madcat-7.3/tamtam/allocation_calculation/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 13:01:46.000000 madcat-7.3/tamtam/allocation_calculation/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1937 2023-02-22 14:13:02.000000 madcat-7.3/tamtam/allocation_calculation/bias_class.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.392869 madcat-7.3/tamtam/delta_analysis/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-23 07:37:32.000000 madcat-7.3/tamtam/delta_analysis/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     6199 2023-02-23 21:48:17.000000 madcat-7.3/tamtam/delta_analysis/delta_class.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2517 2023-02-23 21:45:56.000000 madcat-7.3/tamtam/manual_run.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.393197 madcat-7.3/tamtam/metrics_correlation/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 14:27:03.000000 madcat-7.3/tamtam/metrics_correlation/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2350 2023-02-23 14:45:57.000000 madcat-7.3/tamtam/metrics_correlation/metric_class.py
+-rw-r--r--   0 amitosi    (501) staff       (20)      964 2023-02-23 14:45:57.000000 madcat-7.3/tamtam/run.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.393567 madcat-7.3/tamtam/user_class/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 07:41:13.000000 madcat-7.3/tamtam/user_class/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     1895 2023-02-23 11:53:41.000000 madcat-7.3/tamtam/user_class/user_class.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.394164 madcat-7.3/tamtam/utils/
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-22 10:08:15.000000 madcat-7.3/tamtam/utils/__init__.py
+-rw-r--r--   0 amitosi    (501) staff       (20)       54 2023-02-22 16:12:56.000000 madcat-7.3/tamtam/utils/column_utils.py
+-rw-r--r--   0 amitosi    (501) staff       (20)       59 2023-02-22 16:24:31.000000 madcat-7.3/tamtam/utils/utils.py
+drwxr-xr-x   0 amitosi    (501) staff       (20)        0 2023-07-23 08:38:45.395012 madcat-7.3/tests/
+-rw-r--r--   0 amitosi    (501) staff       (20)     2501 2023-02-05 11:09:51.000000 madcat-7.3/tests/test_cleaning.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2119 2023-02-05 11:09:51.000000 madcat-7.3/tests/test_preprocessing.py
+-rw-r--r--   0 amitosi    (501) staff       (20)        0 2023-02-05 11:09:51.000000 madcat-7.3/tests/test_util.py
+-rw-r--r--   0 amitosi    (501) staff       (20)     2843 2023-02-05 11:09:58.000000 madcat-7.3/tests/test_zero_break.py
```

### Comparing `madcat-7.2/README.md` & `madcat-7.3/README.md`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/cleaning/cleaner_handler.py` & `madcat-7.3/chester/cleaning/cleaner_handler.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/cleaning/cleaning_func.py` & `madcat-7.3/chester/cleaning/cleaning_func.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/data_loader/webtext_data.py` & `madcat-7.3/chester/data_loader/webtext_data.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/feature_analyzing/feature_correlation.py` & `madcat-7.3/chester/feature_analyzing/feature_correlation.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/feature_stats/categorical_stats.py` & `madcat-7.3/chester/feature_stats/categorical_stats.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/feature_stats/numeric_stats.py` & `madcat-7.3/chester/feature_stats/numeric_stats.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/feature_stats/text_stats.py` & `madcat-7.3/chester/feature_stats/text_stats.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/feature_stats/time_series_stats.py` & `madcat-7.3/chester/feature_stats/time_series_stats.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/feature_stats/utils.py` & `madcat-7.3/chester/feature_stats/utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/bag_of_words.py` & `madcat-7.3/chester/features_engineering/bag_of_words.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/corex.py` & `madcat-7.3/chester/features_engineering/corex.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/fe_nlp.py` & `madcat-7.3/chester/features_engineering/fe_nlp.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/feature_handler.py` & `madcat-7.3/chester/features_engineering/feature_handler.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/features_handler.py` & `madcat-7.3/chester/features_engineering/features_handler.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/tfidf.py` & `madcat-7.3/chester/features_engineering/tfidf.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/time_series/cyclic_features_utils.py` & `madcat-7.3/chester/features_engineering/time_series/cyclic_features_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/time_series/event_counter.py` & `madcat-7.3/chester/features_engineering/time_series/event_counter.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/time_series/feature_elimination_utils.py` & `madcat-7.3/chester/features_engineering/time_series/feature_elimination_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/time_series/frequencies_utils.py` & `madcat-7.3/chester/features_engineering/time_series/frequencies_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/time_series/get_time_freqeuency_utils.py` & `madcat-7.3/chester/features_engineering/time_series/get_time_freqeuency_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/time_series/moving_metric_utils.py` & `madcat-7.3/chester/features_engineering/time_series/moving_metric_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/time_series/static_features_utils.py` & `madcat-7.3/chester/features_engineering/time_series/static_features_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/time_series/ts_feature_extraction.py` & `madcat-7.3/chester/features_engineering/time_series/ts_feature_extraction.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/features_engineering/time_series/ts_features_extraction.py` & `madcat-7.3/chester/features_engineering/time_series/ts_features_extraction.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_analyzer/model_analysis.py` & `madcat-7.3/chester/model_analyzer/model_analysis.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_monitor/calculate_scores_utils.py` & `madcat-7.3/chester/model_monitor/calculate_scores_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_monitor/error_prediction.py` & `madcat-7.3/chester/model_monitor/error_prediction.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_monitor/model_boostrap.py` & `madcat-7.3/chester/model_monitor/model_boostrap.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/data_preparation.py` & `madcat-7.3/chester/model_training/data_preparation.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/model_utils.py` & `madcat-7.3/chester/model_training/model_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/base_model.py` & `madcat-7.3/chester/model_training/models/chester_models/base_model.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/base_model_utils.py` & `madcat-7.3/chester/model_training/models/chester_models/base_model_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/baseline/baseline_model.py` & `madcat-7.3/chester/model_training/models/chester_models/baseline/baseline_model.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/baseline/baseline_utils.py` & `madcat-7.3/chester/model_training/models/chester_models/baseline/baseline_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/best_baseline_model.py` & `madcat-7.3/chester/model_training/models/chester_models/best_baseline_model.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/best_linear_regression.py` & `madcat-7.3/chester/model_training/models/chester_models/best_linear_regression.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/best_logistic_regression.py` & `madcat-7.3/chester/model_training/models/chester_models/best_logistic_regression.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/best_model.py` & `madcat-7.3/chester/model_training/models/chester_models/best_model.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/compare_utils.py` & `madcat-7.3/chester/model_training/models/chester_models/compare_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/hp_generator.py` & `madcat-7.3/chester/model_training/models/chester_models/hp_generator.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/linear_regression/linear_regression.py` & `madcat-7.3/chester/model_training/models/chester_models/linear_regression/linear_regression.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/linear_regression/linear_regression_utils.py` & `madcat-7.3/chester/model_training/models/chester_models/linear_regression/linear_regression_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/logistic_regression/logistic_regression_model.py` & `madcat-7.3/chester/model_training/models/chester_models/logistic_regression/logistic_regression_model.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/chester_models/logistic_regression/logistic_regression_utils.py` & `madcat-7.3/chester/model_training/models/chester_models/logistic_regression/logistic_regression_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/cv_training.py` & `madcat-7.3/chester/model_training/models/cv_training.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/lstm.py` & `madcat-7.3/chester/model_training/models/lstm.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/model_training/models/scoring.py` & `madcat-7.3/chester/model_training/models/scoring.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/post_model_analysis/post_model_analysis_class.py` & `madcat-7.3/chester/post_model_analysis/post_model_analysis_class.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/post_model_analysis/post_regression.py` & `madcat-7.3/chester/post_model_analysis/post_regression.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/pre_model_analysis/categorical.py` & `madcat-7.3/chester/pre_model_analysis/categorical.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/pre_model_analysis/numerics.py` & `madcat-7.3/chester/pre_model_analysis/numerics.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/pre_model_analysis/target.py` & `madcat-7.3/chester/pre_model_analysis/target.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/pre_model_analysis/time_series.py` & `madcat-7.3/chester/pre_model_analysis/time_series.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/preprocessing/preprocessing_func.py` & `madcat-7.3/chester/preprocessing/preprocessing_func.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/preprocessing/preprocessor_handler.py` & `madcat-7.3/chester/preprocessing/preprocessor_handler.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/run/chapter_titles.py` & `madcat-7.3/chester/run/chapter_titles.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/run/feature_attention_utils.py` & `madcat-7.3/chester/run/feature_attention_utils.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/run/full_run.py` & `madcat-7.3/chester/run/full_run.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/run/user_classes.py` & `madcat-7.3/chester/run/user_classes.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/run_manual_chester/manual_run.py` & `madcat-7.3/chester/run_manual_chester/manual_run.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/text_stats_analysis/common_words.py` & `madcat-7.3/chester/text_stats_analysis/common_words.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/text_stats_analysis/corex_topics.py` & `madcat-7.3/chester/text_stats_analysis/corex_topics.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/text_stats_analysis/data_quality.py` & `madcat-7.3/chester/text_stats_analysis/data_quality.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/text_stats_analysis/key_sentences.py` & `madcat-7.3/chester/text_stats_analysis/key_sentences.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/text_stats_analysis/keywords_extraction.py` & `madcat-7.3/chester/text_stats_analysis/keywords_extraction.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/text_stats_analysis/sentiment.py` & `madcat-7.3/chester/text_stats_analysis/sentiment.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/text_stats_analysis/smart_text_analyzer.py` & `madcat-7.3/chester/text_stats_analysis/smart_text_analyzer.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/text_stats_analysis/text_summary.py` & `madcat-7.3/chester/text_stats_analysis/text_summary.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/text_stats_analysis/word_cloud.py` & `madcat-7.3/chester/text_stats_analysis/word_cloud.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/util.py` & `madcat-7.3/chester/util.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/zero_break/problem_specification.py` & `madcat-7.3/chester/zero_break/problem_specification.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/chester/zero_break/text_detector.py` & `madcat-7.3/chester/zero_break/text_detector.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/example_notebooks/main.py` & `madcat-7.3/example_notebooks/main.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/madcat.egg-info/SOURCES.txt` & `madcat-7.3/madcat.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `madcat-7.2/setup.py` & `madcat-7.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open('requirements.txt') as f:
     install_requires = f.read().strip().split('\n')
 
 setuptools.setup(
     name="madcat",
-    version="7.02",
+    version="7.3",
     author="Amit Osi",
     author_email="amitosi6666@gmail.com",
     description=open('README.md').read(),
     url="https://github.com/amito-ds/chester",
     packages=setuptools.find_packages(exclude=["tests*"]),
     include_package_data=True,
     python_requires=">=3.8",
```

### Comparing `madcat-7.2/tamtam/ab_feature_analysis/ab_catboost.py` & `madcat-7.3/tamtam/ab_feature_analysis/ab_catboost.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tamtam/ab_feature_analysis/ab_feature_analysis_class.py` & `madcat-7.3/tamtam/ab_feature_analysis/ab_feature_analysis_class.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tamtam/ab_info/ab_class.py` & `madcat-7.3/tamtam/ab_info/ab_class.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tamtam/allocation_calculation/bias_class.py` & `madcat-7.3/tamtam/allocation_calculation/bias_class.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tamtam/delta_analysis/delta_class.py` & `madcat-7.3/tamtam/delta_analysis/delta_class.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tamtam/manual_run.py` & `madcat-7.3/tamtam/manual_run.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tamtam/metrics_correlation/metric_class.py` & `madcat-7.3/tamtam/metrics_correlation/metric_class.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tamtam/run.py` & `madcat-7.3/tamtam/run.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tamtam/user_class/user_class.py` & `madcat-7.3/tamtam/user_class/user_class.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tests/test_cleaning.py` & `madcat-7.3/tests/test_cleaning.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tests/test_preprocessing.py` & `madcat-7.3/tests/test_preprocessing.py`

 * *Files identical despite different names*

### Comparing `madcat-7.2/tests/test_zero_break.py` & `madcat-7.3/tests/test_zero_break.py`

 * *Files identical despite different names*

