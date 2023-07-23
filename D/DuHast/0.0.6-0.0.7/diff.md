# Comparing `tmp/DuHast-0.0.6.tar.gz` & `tmp/DuHast-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "DuHast-0.0.6.tar", last modified: Sat Mar 25 01:49:38 2023, max compression
+gzip compressed data, was "DuHast-0.0.7.tar", last modified: Sun Jul 23 12:29:59 2023, max compression
```

## Comparing `DuHast-0.0.6.tar` & `DuHast-0.0.7.tar`

### file list

```diff
@@ -1,136 +1,476 @@
-drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-03-25 01:49:38.472393 DuHast-0.0.6/
--rw-r--r--   0 janchristel   (501) staff       (20)     7652 2023-01-08 05:16:07.000000 DuHast-0.0.6/LICENSE
--rw-r--r--   0 janchristel   (501) staff       (20)      772 2023-03-25 01:49:38.472757 DuHast-0.0.6/PKG-INFO
--rw-r--r--   0 janchristel   (501) staff       (20)      407 2023-02-21 09:07:03.000000 DuHast-0.0.6/README.md
--rw-r--r--   0 janchristel   (501) staff       (20)      643 2023-03-25 01:47:07.000000 DuHast-0.0.6/pyproject.toml
--rw-r--r--   0 janchristel   (501) staff       (20)      454 2023-03-25 01:49:38.473770 DuHast-0.0.6/setup.cfg
--rw-r--r--   0 janchristel   (501) staff       (20)      474 2023-02-21 09:10:18.000000 DuHast-0.0.6/setup.py
-drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-03-25 01:49:38.387750 DuHast-0.0.6/src/
-drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-03-25 01:49:38.391022 DuHast-0.0.6/src/DuHast.egg-info/
--rw-r--r--   0 janchristel   (501) staff       (20)      772 2023-03-25 01:49:38.000000 DuHast-0.0.6/src/DuHast.egg-info/PKG-INFO
--rw-r--r--   0 janchristel   (501) staff       (20)     5319 2023-03-25 01:49:38.000000 DuHast-0.0.6/src/DuHast.egg-info/SOURCES.txt
--rw-r--r--   0 janchristel   (501) staff       (20)        1 2023-03-25 01:49:38.000000 DuHast-0.0.6/src/DuHast.egg-info/dependency_links.txt
--rw-r--r--   0 janchristel   (501) staff       (20)        7 2023-03-25 01:49:38.000000 DuHast-0.0.6/src/DuHast.egg-info/top_level.txt
-drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-03-25 01:49:38.391391 DuHast-0.0.6/src/duHast/
-drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-03-25 01:49:38.446512 DuHast-0.0.6/src/duHast/APISamples/
--rw-r--r--   0 janchristel   (501) staff       (20)     1318 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/APISamples/IFamilyAction.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3030 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/APISamples/IFamilyData.py
--rw-r--r--   0 janchristel   (501) staff       (20)     7841 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/IFamilyProcessor.py
--rw-r--r--   0 janchristel   (501) staff       (20)    24757 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitAnnotation.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4148 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitBIM360.py
--rw-r--r--   0 janchristel   (501) staff       (20)     9668 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitBuildingPads.py
--rw-r--r--   0 janchristel   (501) staff       (20)    51961 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitCategories.py
--rw-r--r--   0 janchristel   (501) staff       (20)    10887 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitCategoryData.py
--rw-r--r--   0 janchristel   (501) staff       (20)     8206 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/RevitCategoryDataProcessor.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3671 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/RevitCategoryDataPurgeUnused.py
--rw-r--r--   0 janchristel   (501) staff       (20)    18976 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitCeilings.py
--rw-r--r--   0 janchristel   (501) staff       (20)    70365 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitCommonAPI.py
--rw-r--r--   0 janchristel   (501) staff       (20)    13567 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitCurtainWallElements.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3469 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/APISamples/RevitCustomElementFilter.py
--rw-r--r--   0 janchristel   (501) staff       (20)     5642 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitDesignSetOptions.py
--rw-r--r--   0 janchristel   (501) staff       (20)    14038 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitDetailItems.py
--rw-r--r--   0 janchristel   (501) staff       (20)    18237 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitElementParameterGetUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)     8853 2023-03-24 09:23:19.000000 DuHast-0.0.6/src/duHast/APISamples/RevitElementParameterSetUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)    23911 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitExport.py
--rw-r--r--   0 janchristel   (501) staff       (20)    29788 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/APISamples/RevitExportIFCConfig.py
--rw-r--r--   0 janchristel   (501) staff       (20)    12743 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/APISamples/RevitExportIFCSettings.py
--rw-r--r--   0 janchristel   (501) staff       (20)     6448 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyBaseData.py
--rw-r--r--   0 janchristel   (501) staff       (20)    13761 2023-02-19 05:34:49.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyBaseDataAnalysisCircularReferencing.py
--rw-r--r--   0 janchristel   (501) staff       (20)    10505 2023-02-19 05:32:49.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyBaseDataAnalysisMissingFamilies.py
--rw-r--r--   0 janchristel   (501) staff       (20)    10803 2023-02-19 05:32:49.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyBaseDataAnalysisReloadAdvanced.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3128 2023-02-19 05:34:41.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyBaseDataProcessor.py
--rw-r--r--   0 janchristel   (501) staff       (20)    15154 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyBaseDataUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)    22419 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyCategoryDataUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)     8706 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyDataCollector.py
--rw-r--r--   0 janchristel   (501) staff       (20)     1541 2023-01-26 02:09:50.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyLoadOption.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4511 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyParameterUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)     7707 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyReload.py
--rw-r--r--   0 janchristel   (501) staff       (20)     5943 2023-02-19 05:32:49.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyReloadAdvancedUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)     6192 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyRenameFiles.py
--rw-r--r--   0 janchristel   (501) staff       (20)     5099 2023-02-19 05:32:49.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyRenameFilesUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)     6883 2023-02-19 05:32:49.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyRenameFindHostFamilies.py
--rw-r--r--   0 janchristel   (501) staff       (20)     6575 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyRenameLoadedFamilies.py
--rw-r--r--   0 janchristel   (501) staff       (20)    18505 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyReportUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)    35731 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFamilyUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)    12047 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/APISamples/RevitFloors.py
--rw-r--r--   0 janchristel   (501) staff       (20)     6601 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitGenericAnnotation.py
--rw-r--r--   0 janchristel   (501) staff       (20)    29104 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/APISamples/RevitGeometry.py
--rw-r--r--   0 janchristel   (501) staff       (20)    25285 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitGrids.py
--rw-r--r--   0 janchristel   (501) staff       (20)     7826 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/APISamples/RevitGroups.py
--rw-r--r--   0 janchristel   (501) staff       (20)    20201 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitLevels.py
--rw-r--r--   0 janchristel   (501) staff       (20)    11020 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitLinePatternData.py
--rw-r--r--   0 janchristel   (501) staff       (20)     5678 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/RevitLinePatternDataProcessor.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3353 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/RevitLinePatternDataPurgeUnused.py
--rw-r--r--   0 janchristel   (501) staff       (20)    11385 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitLineStylesPatterns.py
--rw-r--r--   0 janchristel   (501) staff       (20)    31316 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitLinks.py
--rw-r--r--   0 janchristel   (501) staff       (20)    50511 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/APISamples/RevitMEPSystems.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4539 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitMaterials.py
--rw-r--r--   0 janchristel   (501) staff       (20)    25869 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitModelHealth.py
--rw-r--r--   0 janchristel   (501) staff       (20)     5571 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/APISamples/RevitModelHealthReportFileNames.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3512 2023-01-26 09:09:15.000000 DuHast-0.0.6/src/duHast/APISamples/RevitParameterGrouping.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2262 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/APISamples/RevitPhases.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2704 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/APISamples/RevitPurgeAction.py
--rw-r--r--   0 janchristel   (501) staff       (20)    25184 2023-02-19 05:32:49.000000 DuHast-0.0.6/src/duHast/APISamples/RevitPurgeUnused.py
--rw-r--r--   0 janchristel   (501) staff       (20)     6852 2023-02-19 05:32:49.000000 DuHast-0.0.6/src/duHast/APISamples/RevitPurgeUnusedeTransmit.py
--rw-r--r--   0 janchristel   (501) staff       (20)    21629 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/APISamples/RevitRailings.py
--rw-r--r--   0 janchristel   (501) staff       (20)     7433 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/APISamples/RevitRamps.py
--rw-r--r--   0 janchristel   (501) staff       (20)    11915 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitRevisions.py
--rw-r--r--   0 janchristel   (501) staff       (20)    11618 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/APISamples/RevitRoofs.py
--rw-r--r--   0 janchristel   (501) staff       (20)    12999 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitRooms.py
--rw-r--r--   0 janchristel   (501) staff       (20)    12269 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitSharedParameterAdd.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4222 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitSharedParameterData.py
--rw-r--r--   0 janchristel   (501) staff       (20)     5271 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/RevitSharedParameterDataProcessor.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4509 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/RevitSharedParameterDataPurgeUnused.py
--rw-r--r--   0 janchristel   (501) staff       (20)     6885 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitSharedParameterSwap.py
--rw-r--r--   0 janchristel   (501) staff       (20)    20549 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitSharedParameters.py
--rw-r--r--   0 janchristel   (501) staff       (20)     1213 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/APISamples/RevitSharedParametersTuple.py
--rw-r--r--   0 janchristel   (501) staff       (20)    26525 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitStairs.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2730 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitTransaction.py
--rw-r--r--   0 janchristel   (501) staff       (20)    19090 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitViewReferencing.py
--rw-r--r--   0 janchristel   (501) staff       (20)    32496 2023-03-23 01:47:57.000000 DuHast-0.0.6/src/duHast/APISamples/RevitViews.py
--rw-r--r--   0 janchristel   (501) staff       (20)    19802 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/APISamples/RevitWalls.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2385 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/APISamples/RevitWarnings.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4300 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/RevitWarningsData.py
--rw-r--r--   0 janchristel   (501) staff       (20)     1959 2023-01-26 02:09:50.000000 DuHast-0.0.6/src/duHast/APISamples/RevitWarningsDataProcessor.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4405 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/RevitWarningsSolver.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3916 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitWarningsSolverDuplicateMark.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2641 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/APISamples/RevitWarningsSolverRoomTagToRoom.py
--rw-r--r--   0 janchristel   (501) staff       (20)    15009 2023-03-24 09:14:58.000000 DuHast-0.0.6/src/duHast/APISamples/RevitWorksets.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3352 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/APISamples/UtilBIM360.py
--rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/APISamples/__init__.py
-drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-03-25 01:49:38.458144 DuHast-0.0.6/src/duHast/DataSamples/
--rw-r--r--   0 janchristel   (501) staff       (20)     1917 2023-03-15 20:28:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataBase.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4816 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataCeiling.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2528 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataDesignSetOption.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3529 2023-03-15 20:28:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataExport.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3037 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataGeometry.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2326 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataInstanceProperties.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2458 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataLevel.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2311 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataPhasing.py
--rw-r--r--   0 janchristel   (501) staff       (20)     5339 2023-03-16 09:10:39.000000 DuHast-0.0.6/src/duHast/DataSamples/DataReadFromFile.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2095 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataRevitModel.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4351 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataRoom.py
--rw-r--r--   0 janchristel   (501) staff       (20)     9623 2023-03-18 01:18:21.000000 DuHast-0.0.6/src/duHast/DataSamples/DataToShapely.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2454 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/DataSamples/DataTypeProperties.py
--rw-r--r--   0 janchristel   (501) staff       (20)    20361 2023-03-18 09:04:55.000000 DuHast-0.0.6/src/duHast/DataSamples/ProcessCeilingsToRooms.py
--rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/DataSamples/__init__.py
-drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-03-25 01:49:38.464111 DuHast-0.0.6/src/duHast/UI/
--rw-r--r--   0 janchristel   (501) staff       (20)     1953 2023-01-26 09:09:15.000000 DuHast-0.0.6/src/duHast/UI/FileItem.py
--rw-r--r--   0 janchristel   (501) staff       (20)     9404 2023-02-19 05:27:16.000000 DuHast-0.0.6/src/duHast/UI/FileList.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2165 2023-01-26 09:09:15.000000 DuHast-0.0.6/src/duHast/UI/FileSelectSettings.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4096 2023-01-26 09:09:15.000000 DuHast-0.0.6/src/duHast/UI/UIFileSelect.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2086 2023-01-26 09:09:15.000000 DuHast-0.0.6/src/duHast/UI/WorkloadBucket.py
--rw-r--r--   0 janchristel   (501) staff       (20)     3528 2023-02-18 09:35:46.000000 DuHast-0.0.6/src/duHast/UI/Workloader.py
--rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-01-26 09:09:15.000000 DuHast-0.0.6/src/duHast/UI/__init__.py
--rw-r--r--   0 janchristel   (501) staff       (20)     9544 2023-01-27 01:00:14.000000 DuHast-0.0.6/src/duHast/UI/script.py
-drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-03-25 01:49:38.471756 DuHast-0.0.6/src/duHast/Utilities/
--rw-r--r--   0 janchristel   (501) staff       (20)    26993 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/Utilities/BatchProcessorLogUtils.py
--rw-r--r--   0 janchristel   (501) staff       (20)     4033 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/Utilities/Result.py
--rw-r--r--   0 janchristel   (501) staff       (20)     7158 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/Utilities/SolibriIFCOptimizer.py
--rw-r--r--   0 janchristel   (501) staff       (20)     6646 2023-02-19 05:28:35.000000 DuHast-0.0.6/src/duHast/Utilities/SystemProcess.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2860 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/Utilities/UtilBatchP.py
--rw-r--r--   0 janchristel   (501) staff       (20)    36903 2023-03-24 07:58:08.000000 DuHast-0.0.6/src/duHast/Utilities/Utility.py
--rw-r--r--   0 janchristel   (501) staff       (20)     8090 2023-02-19 05:31:43.000000 DuHast-0.0.6/src/duHast/Utilities/WorksharingMonitorProcess.py
--rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/Utilities/__init__.py
--rw-r--r--   0 janchristel   (501) staff       (20)     2436 2023-01-19 11:06:36.000000 DuHast-0.0.6/src/duHast/Utilities/timer.py
--rw-r--r--   0 janchristel   (501) staff       (20)      243 2023-03-16 09:06:41.000000 DuHast-0.0.6/src/duHast/__init__.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.976572 DuHast-0.0.7/
+-rw-r--r--   0 janchristel   (501) staff       (20)       66 2023-07-23 08:19:28.000000 DuHast-0.0.7/MANIFEST.in
+-rw-r--r--   0 janchristel   (501) staff       (20)      780 2023-07-23 12:29:59.976797 DuHast-0.0.7/PKG-INFO
+-rw-r--r--   0 janchristel   (501) staff       (20)      407 2023-07-12 08:39:01.000000 DuHast-0.0.7/README.md
+-rw-r--r--   0 janchristel   (501) staff       (20)      643 2023-07-23 08:17:02.000000 DuHast-0.0.7/pyproject.toml
+-rw-r--r--   0 janchristel   (501) staff       (20)      394 2023-07-23 12:29:59.977592 DuHast-0.0.7/setup.cfg
+-rw-r--r--   0 janchristel   (501) staff       (20)      474 2023-07-12 08:39:01.000000 DuHast-0.0.7/setup.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.717942 DuHast-0.0.7/src/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.736434 DuHast-0.0.7/src/DuHast.egg-info/
+-rw-r--r--   0 janchristel   (501) staff       (20)      780 2023-07-23 12:29:59.000000 DuHast-0.0.7/src/DuHast.egg-info/PKG-INFO
+-rw-r--r--   0 janchristel   (501) staff       (20)    18294 2023-07-23 12:29:59.000000 DuHast-0.0.7/src/DuHast.egg-info/SOURCES.txt
+-rw-r--r--   0 janchristel   (501) staff       (20)        1 2023-07-23 12:29:59.000000 DuHast-0.0.7/src/DuHast.egg-info/dependency_links.txt
+-rw-r--r--   0 janchristel   (501) staff       (20)        7 2023-07-23 12:29:59.000000 DuHast-0.0.7/src/DuHast.egg-info/top_level.txt
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.736894 DuHast-0.0.7/src/duHast/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.738489 DuHast-0.0.7/src/duHast/Data/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.739980 DuHast-0.0.7/src/duHast/Data/Objects/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.742822 DuHast-0.0.7/src/duHast/Data/Objects/Properties/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.745192 DuHast-0.0.7/src/duHast/Data/Objects/Properties/Geometry/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/Geometry/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7149 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/Geometry/from_revit_conversion.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2144 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/Geometry/from_revit_elements.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3723 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/Geometry/geometry_base.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3136 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/Geometry/geometry_polygon.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2823 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/Geometry/geometry_topo_cell.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3339 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/data_design_set_option.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4205 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/data_element_geometry.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3092 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/data_instance_properties.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3218 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/data_level.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3075 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/data_phasing.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2897 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/data_revit_model.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3218 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/Properties/data_type_properties.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6000 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/data_ceiling.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5422 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Objects/data_room.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.748239 DuHast-0.0.7/src/duHast/Data/Utils/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Data/Utils/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2455 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Utils/data_base.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2871 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Utils/data_export.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6204 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Utils/data_import.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2735 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/Utils/data_to_file.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Data/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    10866 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/data_to_shapely.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    22887 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Data/process_ceilings_to_rooms.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.750506 DuHast-0.0.7/src/duHast/Revit/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.761051 DuHast-0.0.7/src/duHast/Revit/Annotation/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.764721 DuHast-0.0.7/src/duHast/Revit/Annotation/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1296 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/Reporting/annotations_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2612 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/Reporting/gen_annotations_instance_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1278 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/Reporting/gen_annotations_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7001 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/Reporting/tags_independent_report.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.766079 DuHast-0.0.7/src/duHast/Revit/Annotation/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3696 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/Utility/gen_annotation_type_sorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3081 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/annotation.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5152 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/arrow_heads.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4372 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/dimensions.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3687 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/generic_annotation.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3081 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/independent_tags.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6458 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/independent_tags_elbow_properties.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7455 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/independent_tags_modify_properties.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6138 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/independent_tags_tagged_elements.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3982 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/multi_ref_annotation.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    12895 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/purge_unused_annotation_types.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4337 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/spot_dimensions.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2882 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/stair_path.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3663 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Annotation/text.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.768052 DuHast-0.0.7/src/duHast/Revit/BIM360/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/BIM360/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5107 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/BIM360/bim_360.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4375 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/BIM360/util_bim_360.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.769872 DuHast-0.0.7/src/duHast/Revit/BuildingPads/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.771217 DuHast-0.0.7/src/duHast/Revit/BuildingPads/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/BuildingPads/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2047 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/BuildingPads/Reporting/building_pads_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.773826 DuHast-0.0.7/src/duHast/Revit/BuildingPads/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)     3953 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/BuildingPads/Utility/RevitBuildingPadTypeSorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2324 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/BuildingPads/Utility/RevitBuildingPadsFilter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/BuildingPads/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/BuildingPads/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5679 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/BuildingPads/building_pads.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4790 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/BuildingPads/purge_unused_building_pad_types.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.775663 DuHast-0.0.7/src/duHast/Revit/Categories/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.778486 DuHast-0.0.7/src/duHast/Revit/Categories/Data/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Data/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    12627 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Data/category_data.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    10651 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Data/category_data_processor.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4711 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Data/category_data_purge_unused.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.780704 DuHast-0.0.7/src/duHast/Revit/Categories/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3055 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Reporting/categories_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6772 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Reporting/categories_report_utils.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.784998 DuHast-0.0.7/src/duHast/Revit/Categories/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7333 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Utility/category_properties_get_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    12564 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Utility/category_properties_set_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2769 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Utility/category_property_names.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    12743 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/Utility/elements_by_category_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    10421 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/categories.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3675 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/change_family_category.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    13463 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Categories/family_sub_categories.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.786858 DuHast-0.0.7/src/duHast/Revit/Ceilings/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.787893 DuHast-0.0.7/src/duHast/Revit/Ceilings/Export/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/Export/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6363 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/Export/to_data_ceiling.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.788864 DuHast-0.0.7/src/duHast/Revit/Ceilings/Geometry/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/Geometry/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3239 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/Geometry/geometry.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.789763 DuHast-0.0.7/src/duHast/Revit/Ceilings/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1221 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/Reporting/ceilings_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.791994 DuHast-0.0.7/src/duHast/Revit/Ceilings/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2330 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/Utility/ceilings_filter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3013 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/Utility/ceilings_type_sorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6721 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/ceilings.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6184 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ceilings/purge_unused_ceiling_types.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.804353 DuHast-0.0.7/src/duHast/Revit/Common/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.806578 DuHast-0.0.7/src/duHast/Revit/Common/Geometry/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/Geometry/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    24242 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/Geometry/geometry.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2318 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/Geometry/solids.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.808971 DuHast-0.0.7/src/duHast/Revit/Common/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2033 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/Reporting/groups_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2022 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/Reporting/worksets_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2740 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/Reporting/worksets_report_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    15681 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/common.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4954 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/custom_element_filter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4276 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/custom_element_filter_actions.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4551 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/custom_element_filter_tests.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5122 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/delete.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5636 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/design_set_options.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7991 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/element_filtering.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    11442 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/file_io.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8015 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/groups.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    19927 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/parameter_get_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4360 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/parameter_grouping.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     9998 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/parameter_set_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2274 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/phases.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8919 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/purge_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)      289 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/revit_version.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3522 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/transaction.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    15172 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Common/worksets.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.810468 DuHast-0.0.7/src/duHast/Revit/DetailItems/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.811369 DuHast-0.0.7/src/duHast/Revit/DetailItems/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/DetailItems/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1207 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/DetailItems/Reporting/detail_items_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.812680 DuHast-0.0.7/src/duHast/Revit/DetailItems/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/DetailItems/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2673 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/DetailItems/Utility/detail_items_type_sorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/DetailItems/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6438 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/DetailItems/detail_items.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8656 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/DetailItems/purge_unused_detail_item_types.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.815031 DuHast-0.0.7/src/duHast/Revit/Exports/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.822382 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7956 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/export_ifc_config_2019.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8071 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/export_ifc_config_2020.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8108 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/export_ifc_config_2021.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    13564 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/export_ifc_config_2022.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    13567 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/export_ifc_config_2023.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2308 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/ifc_export_coordinates.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    14056 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/ifc_export_settings.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2108 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/Utility/ifc_export_space_boundaries.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2834 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/export.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    17685 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/export_ifc.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    10792 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Exports/export_navis.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.829625 DuHast-0.0.7/src/duHast/Revit/Family/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.841049 DuHast-0.0.7/src/duHast/Revit/Family/Data/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7892 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_base_data.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    15524 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_base_data_circular_referencing.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    11956 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_base_data_missing_families.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4386 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_base_data_processor.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    12685 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_base_data_reload_advanced.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    16818 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_base_data_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    23832 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_category_data_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    10975 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_data_collector.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6758 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_reload_advanced_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7795 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_rename_files.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8669 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_rename_find_host_families.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8086 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_rename_loaded_families.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    19924 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/family_report_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2349 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/ifamily_action.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4281 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/ifamily_data.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     9219 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Data/ifamily_processor.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.842092 DuHast-0.0.7/src/duHast/Revit/Family/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    10442 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/Utility/loadable_family_categories.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3785 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/family_element_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1734 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/family_load_option.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5740 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/family_parameter_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7611 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/family_reference_elements.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     9409 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/family_reload.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5996 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/family_rename_files_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    16259 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/family_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7404 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Family/purge_unused_family_types.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.844236 DuHast-0.0.7/src/duHast/Revit/Floors/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.845123 DuHast-0.0.7/src/duHast/Revit/Floors/Export/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Floors/Export/__init__.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.845837 DuHast-0.0.7/src/duHast/Revit/Floors/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Floors/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1213 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Floors/Reporting/floors_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.847682 DuHast-0.0.7/src/duHast/Revit/Floors/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Floors/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2376 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Floors/Utility/floors_filter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2993 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Floors/Utility/floors_type_sorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Floors/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6966 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Floors/floors.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5625 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Floors/purge_unused_floor_types.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.851306 DuHast-0.0.7/src/duHast/Revit/Grids/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.853174 DuHast-0.0.7/src/duHast/Revit/Grids/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Grids/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2852 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Grids/Reporting/grid_report_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2062 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Grids/Reporting/grids_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Grids/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8259 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Grids/grids.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    14879 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Grids/grids_appearance.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6617 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Grids/grids_worksets.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3459 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Grids/purge_unused_grid_types.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7652 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/LICENSE
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.855970 DuHast-0.0.7/src/duHast/Revit/Levels/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.858068 DuHast-0.0.7/src/duHast/Revit/Levels/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Levels/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2024 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Levels/Reporting/levels_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2917 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Levels/Reporting/levels_report_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Levels/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4732 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Levels/levels.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    14801 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Levels/levels_appearance.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4499 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Levels/purge_unused_level_types.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.862894 DuHast-0.0.7/src/duHast/Revit/LinePattern/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/LinePattern/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2224 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/LinePattern/fill_patterns.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    12830 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/LinePattern/line_pattern_data.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7540 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/LinePattern/line_pattern_data_processor.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4315 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/LinePattern/line_pattern_data_purge_unused.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    10624 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/LinePattern/line_patterns.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3363 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/LinePattern/line_styles.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.866842 DuHast-0.0.7/src/duHast/Revit/Links/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.869983 DuHast-0.0.7/src/duHast/Revit/Links/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2065 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/Reporting/cad_links_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5071 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/Reporting/cad_links_report_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2124 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/Reporting/links_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5075 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/Reporting/links_report_utils.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.871229 DuHast-0.0.7/src/duHast/Revit/Links/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1562 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/Utility/link_path.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     9375 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/cad_links.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3458 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/cad_links_geometry.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5382 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/image_links.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    11466 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/links.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3415 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Links/purge_unused_image_link_types.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.876971 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.878043 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1979 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Reporting/mep_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.881772 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)     2490 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Utility/MergeLists.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3488 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Utility/RevitMEPSystemCategories.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3817 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Utility/RevitMEPSystemNames.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3766 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Utility/RevitMEPTypeSorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6510 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Utility/SymbolsInSystemTypes.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6369 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/cable_trays.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6281 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/conduits.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6369 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/ducts.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6483 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/flex_ducts.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6152 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/pipes.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    11395 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/purge_unused_mep_symbols.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    14334 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/MEP_Systems/purge_unused_mep_types.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.882611 DuHast-0.0.7/src/duHast/Revit/Materials/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.884447 DuHast-0.0.7/src/duHast/Revit/Materials/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Materials/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2067 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Materials/Reporting/materials_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3474 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Materials/Reporting/materials_report_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Materials/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3557 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Materials/materials.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.885376 DuHast-0.0.7/src/duHast/Revit/ModelHealth/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.887022 DuHast-0.0.7/src/duHast/Revit/ModelHealth/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/ModelHealth/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5675 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/ModelHealth/Reporting/report_file_names.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/ModelHealth/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    27455 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/ModelHealth/model_health.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.889557 DuHast-0.0.7/src/duHast/Revit/Purge/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Purge/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3738 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Purge/purge_action.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    25813 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Purge/purge_unused.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7872 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Purge/purge_unused_e_transmit.py
+-rw-r--r--   0 janchristel   (501) staff       (20)      402 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/README.md
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.891672 DuHast-0.0.7/src/duHast/Revit/Railings/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.892652 DuHast-0.0.7/src/duHast/Revit/Railings/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2027 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/Reporting/railings_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.896560 DuHast-0.0.7/src/duHast/Revit/Railings/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2490 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/Utility/merge_lists.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2434 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/Utility/railing_categories.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2233 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/Utility/railing_family_names.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4330 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/Utility/railings_filter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3776 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/Utility/railings_type_sorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7018 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/balusters.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7825 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/purge_unused_railing_and_baluster_types.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8388 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Railings/railings.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.898327 DuHast-0.0.7/src/duHast/Revit/Ramps/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.899254 DuHast-0.0.7/src/duHast/Revit/Ramps/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ramps/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2016 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Ramps/Reporting/ramps_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.901430 DuHast-0.0.7/src/duHast/Revit/Ramps/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)     1996 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Ramps/Utility/RevitRampsFamilyNames.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2359 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Ramps/Utility/RevitRampsFilter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3592 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Ramps/Utility/RevitRampsTypeSorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ramps/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ramps/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4005 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Ramps/purge_unused_ramp_types.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3591 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Ramps/ramps.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.903969 DuHast-0.0.7/src/duHast/Revit/Revisions/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Revisions/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6701 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Revisions/new_revision.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    18324 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Revisions/revisions.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4527 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Revisions/sequence.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.905275 DuHast-0.0.7/src/duHast/Revit/Roofs/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.906501 DuHast-0.0.7/src/duHast/Revit/Roofs/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Roofs/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2016 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Roofs/Reporting/roofs_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.909520 DuHast-0.0.7/src/duHast/Revit/Roofs/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)     2124 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Roofs/Utility/RevitRoofsFamilyNames.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3038 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Roofs/Utility/RevitRoofsFilter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3719 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Roofs/Utility/RevitRoofsTypeSorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Roofs/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Roofs/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5651 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Roofs/purge_unused_roof_types.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6315 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Roofs/roofs.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.911100 DuHast-0.0.7/src/duHast/Revit/Rooms/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.912158 DuHast-0.0.7/src/duHast/Revit/Rooms/Export/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Rooms/Export/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6048 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Rooms/Export/to_data_room.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.913282 DuHast-0.0.7/src/duHast/Revit/Rooms/Geometry/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Rooms/Geometry/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5568 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Rooms/Geometry/geometry.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.914354 DuHast-0.0.7/src/duHast/Revit/Rooms/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Rooms/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1194 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Rooms/Reporting/revit_rooms_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Rooms/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3701 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Rooms/room_tags.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4476 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Rooms/rooms.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.919913 DuHast-0.0.7/src/duHast/Revit/SharedParameters/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.921522 DuHast-0.0.7/src/duHast/Revit/SharedParameters/Data/
+-rw-r--r--   0 janchristel   (501) staff       (20)     5298 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/Data/shared_parameter_data.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7836 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/Data/shared_parameter_data_processor.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5767 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/Data/shared_parameter_data_purge_Unused.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.923001 DuHast-0.0.7/src/duHast/Revit/SharedParameters/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4835 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/Reporting/shared_parameter_report.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2077 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/Reporting/shared_parameter_report_header.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    13905 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameter_add.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5298 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameter_data.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8096 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameter_swap.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8196 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameter_type_change.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    10845 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameters.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6670 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameters_delete.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1215 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameters_tuple.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.927387 DuHast-0.0.7/src/duHast/Revit/Stairs/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.928374 DuHast-0.0.7/src/duHast/Revit/Stairs/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2022 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/Reporting/stairs_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.929693 DuHast-0.0.7/src/duHast/Revit/Stairs/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2448 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/Utility/stairs_filter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3607 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/Utility/stairs_type_sorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2210 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/cut_marks.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2223 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/landings.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2574 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/path.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    15680 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/purge_unused_stair_types.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2170 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/runs.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5819 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/stairs.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2539 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Stairs/stringers_carriages.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.936446 DuHast-0.0.7/src/duHast/Revit/Views/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.940400 DuHast-0.0.7/src/duHast/Revit/Views/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7429 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Reporting/schedules_report.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6828 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Reporting/sheets_report.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3144 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Reporting/view_property_filter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2544 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Reporting/view_property_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7505 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Reporting/views_report.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4727 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Reporting/views_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.942063 DuHast-0.0.7/src/duHast/Revit/Views/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2742 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Utility/data_category_override.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1527 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/Utility/view_types.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     9097 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/delete.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5923 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/filters.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    15057 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/referencing.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3622 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/schedules.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5904 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/sheets.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7019 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/templates.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6548 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/views.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8148 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/views_purge_unused.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4852 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Views/visibility_graphics_utils.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.946363 DuHast-0.0.7/src/duHast/Revit/Walls/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.948077 DuHast-0.0.7/src/duHast/Revit/Walls/Reporting/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/Reporting/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3909 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/Reporting/walls_report.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     1299 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/Reporting/walls_report_header.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.949933 DuHast-0.0.7/src/duHast/Revit/Walls/Utility/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/Utility/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2052 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/Utility/walls_filter.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2967 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/Utility/walls_type_sorting.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     9609 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/curtain_wall_elements.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3207 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/curtain_walls.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5681 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/purge_unused_curtain_wall_element_types.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7760 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/purge_unused_wall_types.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2912 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/stacked_walls.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6331 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Walls/walls.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.952891 DuHast-0.0.7/src/duHast/Revit/Warnings/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.954641 DuHast-0.0.7/src/duHast/Revit/Warnings/Data/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Warnings/Data/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4864 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Warnings/Data/warnings_data.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3728 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Warnings/Data/warnings_data_processor.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Warnings/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5501 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Warnings/solver.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5493 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Warnings/solver_duplicate_mark.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3644 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Revit/Warnings/solver_room_tag_to_room.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2413 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/Warnings/warnings.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Revit/__init__.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.960524 DuHast-0.0.7/src/duHast/UI/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:01.000000 DuHast-0.0.7/src/duHast/UI/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3004 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/UI/file_item.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     9641 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/UI/file_list.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3243 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/UI/file_select_settings.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    13350 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/UI/script.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7559 2023-07-12 08:39:01.000000 DuHast-0.0.7/src/duHast/UI/ui.xaml
+-rw-r--r--   0 janchristel   (501) staff       (20)     4910 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/UI/ui_file_select.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3285 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/UI/workload_bucket.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4352 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/UI/workloader.py
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.973214 DuHast-0.0.7/src/duHast/Utilities/
+drwxr-xr-x   0 janchristel   (501) staff       (20)        0 2023-07-23 12:29:59.975753 DuHast-0.0.7/src/duHast/Utilities/Objects/
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/Utilities/Objects/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2875 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/Objects/base.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4899 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/Objects/result.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3672 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/Objects/timer.py
+-rw-r--r--   0 janchristel   (501) staff       (20)        0 2023-07-12 08:39:01.000000 DuHast-0.0.7/src/duHast/Utilities/__init__.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    30001 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/batch_processor_log_utils.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3503 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/compare.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4919 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/console_out.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     4821 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/date_stamps.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5346 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/directory_io.py
+-rw-r--r--   0 janchristel   (501) staff       (20)    12864 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/files_combine.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5428 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/files_csv.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8434 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/files_get.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8553 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/files_io.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3816 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/files_json.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5064 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/files_tab.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     5056 2023-07-23 08:28:07.000000 DuHast-0.0.7/src/duHast/Utilities/padding.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     8758 2023-07-23 08:28:07.000000 DuHast-0.0.7/src/duHast/Utilities/solibri_ifc_optimizer.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     7528 2023-07-23 08:28:07.000000 DuHast-0.0.7/src/duHast/Utilities/system_process.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     2668 2023-07-23 08:28:07.000000 DuHast-0.0.7/src/duHast/Utilities/unit_conversion.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     3776 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/util_batch_p.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     6654 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/utility.py
+-rw-r--r--   0 janchristel   (501) staff       (20)     9175 2023-07-23 08:28:08.000000 DuHast-0.0.7/src/duHast/Utilities/worksharing_monitor_process.py
+-rw-r--r--   0 janchristel   (501) staff       (20)      246 2023-07-12 08:39:08.000000 DuHast-0.0.7/src/duHast/__init__.py
```

### Comparing `DuHast-0.0.6/LICENSE` & `DuHast-0.0.7/src/duHast/Revit/LICENSE`

 * *Files identical despite different names*

### Comparing `DuHast-0.0.6/PKG-INFO` & `DuHast-0.0.7/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 Metadata-Version: 2.1
 Name: DuHast
-Version: 0.0.6
+Version: 0.0.7
 Summary: Revit API sample snippets and Revit Batch Processor flows.
 Home-page: UNKNOWN
 Author: Jan Christel
 Author-email: jan.r.christel@gmail.com
-License: GPL3
+License: BSD-3-Clause
 Description: # Code samples for the Revit Batch Processor
         This repository contains code samples for the [Revit Batch Processor](https://github.com/bvn-architecture/RevitBatchProcessor)
         
         A more detailed description of the varies modules, is available through the online [docs](https://jchristel.github.io/SampleCodeRevitBatchProcessor/) and in the [wiki](https://github.com/jchristel/SampleCodeRevitBatchProcessor/wiki).
         
 Keywords: "Revit","API","Batchprocessor","sample"
 Platform: UNKNOWN
```

### Comparing `DuHast-0.0.6/pyproject.toml` & `DuHast-0.0.7/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 requires = ["setuptools==43.0.0", "wheel==0.33.6"]
 build-backend = "setuptools.build_meta"
 
 [project.urls]
 Homepage = "https://github.com/jchristel/SampleCodeRevitBatchProcessor"
 
 [tool.bumpver]
-current_version = "0.0.6"
+current_version = "0.0.7"
 version_pattern = "MAJOR.MINOR.PATCH"
 commit_message  = "Bump version {old_version} -> {new_version}"
 commit          = true
 tag             = true
 push            = false
 
 [tool.bumpver.file_patterns]
```

### Comparing `DuHast-0.0.6/src/DuHast.egg-info/PKG-INFO` & `DuHast-0.0.7/src/DuHast.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 Metadata-Version: 2.1
 Name: DuHast
-Version: 0.0.6
+Version: 0.0.7
 Summary: Revit API sample snippets and Revit Batch Processor flows.
 Home-page: UNKNOWN
 Author: Jan Christel
 Author-email: jan.r.christel@gmail.com
-License: GPL3
+License: BSD-3-Clause
 Description: # Code samples for the Revit Batch Processor
         This repository contains code samples for the [Revit Batch Processor](https://github.com/bvn-architecture/RevitBatchProcessor)
         
         A more detailed description of the varies modules, is available through the online [docs](https://jchristel.github.io/SampleCodeRevitBatchProcessor/) and in the [wiki](https://github.com/jchristel/SampleCodeRevitBatchProcessor/wiki).
         
 Keywords: "Revit","API","Batchprocessor","sample"
 Platform: UNKNOWN
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/IFamilyAction.py` & `DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameters_tuple.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,20 +1,19 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Interface for family data storage / processing class.
+This module contains a tuple used to store settings retrieved from a file.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
-
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
@@ -23,22 +22,12 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-class IFamilyAction():
-
-    def __init__(self, actionType):
-        self.data = []
-        
-        if(actionType != None):
-            self.dataType = actionType
-        else:
-            self.dataType = 'not declared'
+from collections import namedtuple
 
-    def process(self, doc):
-        pass
 
-    def get_Data(self):
-        pass
+# tuples containing base family data read from file
+PARAMETER_DATA = namedtuple("parameterData", "name isInstance builtInParameterGroup")
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/IFamilyProcessor.py` & `DuHast-0.0.7/src/duHast/Revit/Family/Data/ifamily_processor.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,238 +1,262 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Interface for family processing class.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 
 #!/usr/bin/python
 # -*- coding: utf-8 -*-
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import System
 import Autodesk.Revit.DB as rdb
 import json
-from duHast.APISamples import IFamilyData as IFamData
-from duHast.Utilities import Result as res
+from duHast.Revit.Family.Data import ifamily_data as IFamData
+from duHast.Utilities.Objects import result as res
+from duHast.Utilities.Objects import base
+
+
+class IFamilyProcessor(base.Base):
+    def __init__(
+        self,
+        data_type="not declared",
+        pre_actions=None,
+        post_actions=None,
+        string_report_headers=[],
+        **kwargs
+    ):
+
+        # forwards all unused arguments
+        # ini super class to allow multi inheritance in children!
+        super(IFamilyProcessor, self).__init__(**kwargs)
 
-class IFamilyProcessor():
-    
-    def __init__(self, preActions = None, postActions = None):
         self.data = []
-        self.dataType = 'not declared'
-        self.stringReportHeaders = []
-        self.preActions = preActions
-        self.postActions = postActions
+        self.data_type = data_type
+        self.string_report_headers = string_report_headers
+        self.pre_actions = pre_actions
+        self.post_actions = post_actions
 
     # -------------------------------------- utility ----------------------
 
-    def _updateData(self, processor, identifyByThisPropertyName, identifyByThisPropertyValue, updateByPropertyName, updatedToThisPropertyValue):
-        updateStatus = processor.update_Data(identifyByThisPropertyName, identifyByThisPropertyValue, updateByPropertyName, updatedToThisPropertyValue)
-        return updateStatus
+    def _update_Data(
+        self,
+        processor,
+        identify_by_this_property_name,
+        identify_by_this_property_value,
+        update_by_property_name,
+        updated_to_this_property_value,
+    ):
+        update_status = processor.update_Data(
+            identify_by_this_property_name,
+            identify_by_this_property_value,
+            update_by_property_name,
+            updated_to_this_property_value,
+        )
+        return update_status
 
-
-    def _findRootFamilyProcessor(self):
-        '''
+    def _find_root_family_processor(self):
+        """
         Finds the processor instance which processed the root family.
 
         :return: Processor instance
         :rtype: IFamilyProcessor
-        '''
+        """
 
         for processor in self.data:
             for d in processor.get_Data():
-                if ' :: ' not in d[IFamData.ROOT]:
+                if " :: " not in d[IFamData.ROOT]:
                     return processor
 
-    def _findRootFamilyData(self):
-        '''
+    def _find_root_family_data(self):
+        """
         Returns all data from root families (top most in tree) from all processor instances.
 
         :param data: List of dictionaries.
         :type data: [{}]
 
         :return: List of dictionaries.
         :rtype: [{}]
-        '''
+        """
 
-        familyData = []
+        family_data = []
         for processor in self.data:
             for d in processor.get_Data():
-                if ' :: ' not in d[IFamData.ROOT]:
-                    familyData.append (d)
-        return familyData
-    
-    def _findNestedFamiliesData(self):
-        '''
+                if " :: " not in d[IFamData.ROOT]:
+                    family_data.append(d)
+        return family_data
+
+    def _find_nested_families_data(self):
+        """
         Returns all data from nested families from each processor instances.
 
         :param data: List of dictionaries.
         :type data: [{}]
 
         :return: List of dictionaries.
         :rtype: [{}]
-        '''
+        """
 
-        nestedFamilyData = []
+        nested_family_data = []
         for processor in self.data:
             for d in processor.get_Data():
-                if ' :: ' in d[IFamData.ROOT]:
-                    nestedFamilyData.append (d)
-        return nestedFamilyData
+                if " :: " in d[IFamData.ROOT]:
+                    nested_family_data.append(d)
+        return nested_family_data
 
-    def _fixDataTypes(self, flattenedDic):
-        '''
+    def _fix_data_types(self, flattened_dic):
+        """
         Replace any ElementId and Byte values with int or string respectively to have JSON working ok.
         Any other type of values are not changed.
 
-        :param flattenedDic: Dictionary of which values are to be converted.
-        :type flattenedDic: {}
+        :param flattened_dic: Dictionary of which values are to be converted.
+        :type flattened_dic: {}
         :return: Dictionary with converted values.
         :rtype: {}
-        '''
-        
-        dic= {}
-        for key in flattenedDic:
-            if(type(flattenedDic[key]) is rdb.ElementId):
-                dic[key] = flattenedDic[key].IntegerValue
-            elif (type(flattenedDic[key]) is System.Byte):
-                dic[key] = str(flattenedDic[key])
+        """
+
+        dic = {}
+        for key in flattened_dic:
+            if type(flattened_dic[key]) is rdb.ElementId:
+                dic[key] = flattened_dic[key].IntegerValue
+            elif type(flattened_dic[key]) is System.Byte:
+                dic[key] = str(flattened_dic[key])
             else:
-                dic[key] = flattenedDic[key]
+                dic[key] = flattened_dic[key]
         return dic
-    
+
     # -------------------------------------- pre process actions ----------------------
 
-    def preProcessActions(self, doc):
-        '''
+    def pre_process_actions(self, doc):
+        """
         Actions any pre processing before family data will be collected.
 
-        :param doc: The family document. 
+        :param doc: The family document.
         :type doc: Autodesk.Revit.DB.Document
 
         :return: _description_
         :rtype: _type_
-        '''
+        """
+
+        return_value = res.Result()
+        if self.pre_actions != None:
+            for pre_action in self.pre_actions:
+                result_action = pre_action(doc)
+                return_value.update(result_action)
+        return return_value
 
-        returnValue = res.Result()
-        if(self.preActions != None):
-            for preAction in self.preActions:
-                resultAction = preAction(doc)
-                returnValue.Update(resultAction)
-        return returnValue
-    
     # -------------------------------------- process actions ----------------------
 
-    def process(self, doc, rootPath, rootCategoryPath):
-        '''
+    def process(self, doc, root_path, root_category_path):
+        """
         Gather data on the root family and any nested families
 
         :param doc: The family document. 
         :type doc: Autodesk.Revit.DB.Document
 
-        :param rootPath: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
+        :param root_path: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
             This includes the actual family name as the last node.
-        :type rootPath: str
-        :param rootCategoryPath: The path of the nested family category in a tree: rootFamilyCategory::nestedFamilyOneCategory::nestedFamilyTwoCategory\
+        :type root_path: str
+        :param root_category_path: The path of the nested family category in a tree: rootFamilyCategory::nestedFamilyOneCategory::nestedFamilyTwoCategory\
             This includes the actual family category as the last node.
-        :type rootCategoryPath: str
-        '''
+        :type root_category_path: str
+        """
 
         pass
 
     # -------------------------------------- post process actions ----------------------
 
-    def postProcessActions(self, doc):
-        '''
+    def post_process_actions(self, doc):
+        """
         Actions any post processing after family data has been collected.
 
-        :param doc: The family document. 
+        :param doc: The family document.
         :type doc: Autodesk.Revit.DB.Document
-        '''
+        """
 
-        returnValue = res.Result()
-        if(self.postActions != None):
-            for postAction in self.postActions:
-                resultAction = postAction(doc)
-                returnValue.Update(resultAction)
-        return returnValue
+        return_value = res.Result()
+        if self.post_actions != None:
+            for post_action in self.post_actions:
+                result_action = post_action(doc)
+                return_value.update(result_action)
+        return return_value
 
     # -------------------------------------- get data ----------------------
 
-    def get_Data(self):
-        '''
+    def get_data(self):
+        """
         Returns list of flattened dictionaries. One dictionary for each document processed.
 
         :return: List of dictionaries.
         :rtype: [{}]
-        '''
+        """
 
-        dataOut = []
+        data_out = []
         for data in self.data:
             for d in data.get_Data():
-                dataOut.append(d)
-        return dataOut
+                data_out.append(d)
+        return data_out
 
-    def get_Data_JSON(self):
-        '''
+    def get_data_json(self):
+        """
         Returns data objects as JSON formatted strings.
 
         :return: JSON formatted string.
         :rtype: str
-        '''
+        """
 
-        outValue = ''
-        flattenedData = self.get_Data()
-        for d in flattenedData:
-            dFixedTypes = self._fixDataTypes(d)
-            json_object = json.dumps(dict(dFixedTypes))
-            outValue = outValue + '\n' + json_object
-        return outValue
+        out_value = ""
+        flattened_data = self.get_data()
+        for d in flattened_data:
+            d_fixed_types = self._fix_data_types(d)
+            json_object = json.dumps(dict(d_fixed_types))
+            out_value = out_value + "\n" + json_object
+        return out_value
 
-    def get_Data_StringList(self):
-        '''
+    def get_data_string_list(self):
+        """
         Returns data objects as list of strings in order of headers list of this class.
 
         - Strings are UTF 8 encoded
         - Unknown header values are marked as 'null'
 
         :return: list of string.
         :rtype: [str]
-        '''
-        outValue = []
-        flattenedData = self.get_Data()
-        for d in flattenedData:
+        """
+        out_value = []
+        flattened_data = self.get_data()
+        for d in flattened_data:
             row = []
-            for headerKey in self.stringReportHeaders:
-                if(headerKey in d):
+            for header_key in self.string_report_headers:
+                if header_key in d:
                     value = None
-                    if(type(d[headerKey]) == str):
+                    if type(d[header_key]) == str:
                         # make sure string is utf-8 encoded
-                        value = d[headerKey].encode('utf-8', 'ignore')
+                        value = d[header_key].encode("utf-8", "ignore")
                     else:
-                        value = str(d[headerKey])
+                        value = str(d[header_key])
                     row.append(value)
                 else:
-                    row.append('null')
-            outValue.append(row)
-        return outValue
+                    row.append("null")
+            out_value.append(row)
+        return out_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitBuildingPads.py` & `DuHast-0.0.7/src/duHast/Revit/Walls/curtain_wall_elements.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
-~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Revit building pads helper functions.
-~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
+~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+Revit curtain walls helper functions.
+~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -24,251 +24,271 @@
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
 import System
+from System.Collections.Generic import List
 
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.Utilities import Result as res
-from duHast.APISamples import RevitFamilyUtils as rFam
-from duHast.Utilities import Utility as util
+from duHast.Revit.Common import common as com
+from duHast.Revit.Common import parameter_get_utils as rParaGet
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
+
 # -------------------------------------------- common variables --------------------
 #: header used in reports
-REPORT_BUILDING_PAD_HEADER = ['HOSTFILE', 'BUILDINGPADTYPEID', 'BUILDINGPADTYPENAME']
-#: Built in family name for pad
-BASIC_BUILDING_PAD_FAMILY_NAME = 'Pad'
-#: List of all Built in pad family names
-BUILTIN_BUILDING_PAD_TYPE_FAMILY_NAMES = [
-    BASIC_BUILDING_PAD_FAMILY_NAME
+REPORT_CURTAINWALL_ELEMENTS_HEADER = [
+    "HOSTFILE",
+    "CURTAINWALL_ELEMENT_TYPEID",
+    "ReplaceMeTYPENAME",
+]
+#: Built in family name for empty system panel
+CURTAINWALL_PANEL_EMPTY_FAMILY_NAME = "Empty System Panel"
+#: Built in family name for empty system panel
+CURTAINWALL_PANEL_SYSTEM_FAMILY_NAME = "Empty System Panel"
+#: Built in family name for V-shaped mullion
+CURTAINWALL_MULLION_V_FAMILY_NAME = "V Corner Mullion"
+#: Built in family name for circular mullion
+CURTAINWALL_MULLION_CIRCULAR_FAMILY_NAME = "Circular Mullion"
+#: Built in family name for quad corner mullion
+CURTAINWALL_MULLION_QUAD_FAMILY_NAME = "Quad Corner Mullion"
+#: Built in family name for L-shaped corner mullion
+CURTAINWALL_MULLION_L_FAMILY_NAME = "L Corner Mullion"
+#: Built in family name for rectangular mullion
+CURTAINWALL_MULLION_RECT_FAMILY_NAME = "Rectangular Mullion"
+#: Built in family name for trapezoid corner mullion
+CURTAINWALL_MULLION_TRAPEZ_FAMILY_NAME = "Trapezoid Corner Mullion"
+
+BUILTIN_TYPE_FAMILY_NAMES = [
+    CURTAINWALL_PANEL_EMPTY_FAMILY_NAME,
+    CURTAINWALL_PANEL_SYSTEM_FAMILY_NAME,
+    CURTAINWALL_MULLION_V_FAMILY_NAME,
+    CURTAINWALL_MULLION_CIRCULAR_FAMILY_NAME,
+    CURTAINWALL_MULLION_QUAD_FAMILY_NAME,
+    CURTAINWALL_MULLION_L_FAMILY_NAME,
+    CURTAINWALL_MULLION_RECT_FAMILY_NAME,
+    CURTAINWALL_MULLION_TRAPEZ_FAMILY_NAME,
 ]
 
-# --------------------------------------------- utility functions ------------------
-
-def GetAllBuildingPadTypesByCategory(doc):
-    '''
-    Gets a filtered element collector of all BuildingPad types in the model.
-    
-    - Basic BuildingPad
-    
-    Filters by category.
+#: category filter for all element filters by category
+CURTAINWALL_ELEMENTS_CATEGORY_FILTER = List[rdb.BuiltInCategory](
+    [
+        rdb.BuiltInCategory.OST_CurtainWallPanels,
+        rdb.BuiltInCategory.OST_CurtainWallMullions,
+    ]
+)
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+# --------------------------------------------- utility functions ------------------
 
-    :return: A filtered element collector containing building pad types.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
 
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_BuildingPad).WhereElementIsElementType()
-    return collector
+def get_all_curtain_wall_element_types_by_category(doc):
+    """
+    Gets a filtered element collector of all curtain wall element types in the model:
+
+    Filters by multiple categories.
+
+    - curtain wall panels
+    - curtain wall mullions
+    - in place family symbols!
 
-def GetBuildingPadTypesByClass(doc):
-    '''
-    Gets a filtered element collector of all building pad types in the model:
-
-    - Basic BuildingPad
-    
-    Filters by class.
-    Since there are no in place families of type building pad possible, this should return the same elements as the by category filter.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: A filtered element collector containing building pad types.
+    :return: A filtered element collector containing curtain wall element types.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
+
+    multi_cat_filter = rdb.ElementMulticategoryFilter(
+        CURTAINWALL_ELEMENTS_CATEGORY_FILTER
+    )
+    collector = (
+        rdb.FilteredElementCollector(doc)
+        .WherePasses(multi_cat_filter)
+        .WhereElementIsElementType()
+    )
+    return collector
 
-    return  rdb.FilteredElementCollector(doc).OfClass(rdb.BuildingPadType)
 
-def BuildBuildingPadTypeDictionary(collector, dic):
-    '''
+def build_curtain_wall_element_type_dictionary(collector, dic):
+    """
     Returns the dictionary past in with keys and or values added retrieved from collector past in.
 
-    Keys are built in building pad family type names.
-
-    TODO: Use more generic code.
+    Keys are built in curtain wall element type names.
+    TODO: this code repeats across a number of modules. Use generic instead!
 
-    :param collector: A filtered element collector containing building pad types.
+    :param collector: A filtered element collector containing curtain wall element types.
     :type collector: Autodesk.Revit.DB.FilteredElementCollector
-    :param dic: A dictionary containing key:  building pad type family name, value: list of ids belonging to that type.
+    :param dic: A dictionary containing key: curtain wall element type name, value: list of ids belonging to that type.
     :type dic: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
 
-    :return: A dictionary containing key: built in building pad type family name, value: list of ids belonging to that type.
+    :return: A dictionary containing key: built in curtain wall element type  name, value: list of ids belonging to that type.
     :rtype: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
-    '''
+    """
 
     for c in collector:
-        if(dic.has_key(c.FamilyName)):
-            if(c.Id not in dic[c.FamilyName]):
+        if dic.has_key(c.FamilyName):
+            if c.Id not in dic[c.FamilyName]:
                 dic[c.FamilyName].append(c.Id)
         else:
             dic[c.FamilyName] = [c.Id]
     return dic
 
-def SortBuildingPadTypesByFamilyName(doc):
-    '''
-    Returns a dictionary of all building pad types in the model where key is the build in wall family name, values are ids of associated wall types.
 
-    TODO: Use more generic code.
+def sort_curtain_wall_element_types_by_family_name(doc):
+    """
+    Returns a dictionary containing all curtain wall element types in the model.
+
+    Key values are as per BUILTIN_TYPE_FAMILY_NAMES.
+    TODO: This code repeats across a number of modules. Use generic instead!
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: A dictionary containing key: built in building pad type family name, value: list of ids belonging to that type.
-    :rtype: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
-    '''
+    :return: A dictionary containing key: curtain wall element type family name, value: list of ids.
+    :rtype: dic { str: [Autodesk.Revit.DB.ElementId]}
+    """
 
-    # get all building pad Type Elements
-    wts = GetBuildingPadTypesByClass(doc)
-    # get all pad types including in place pad families
-    wts_two = GetAllBuildingPadTypesByCategory(doc)
-    usedWts = {}
-    usedWts = BuildBuildingPadTypeDictionary(wts, usedWts)
-    usedWts = BuildBuildingPadTypeDictionary(wts_two, usedWts)
-    return usedWts
-
-# -------------------------------- none in place BuildingPad types -------------------------------------------------------
-
-def GetAllBuildingPadInstancesInModelByCategory(doc):
-    '''
-    Gets all building pad elements placed in model.
+    # get all CurtainWallElement types including in place wall families
+    wts_two = get_all_curtain_wall_element_types_by_category(doc)
+    used_wts = {}
+    used_wts = build_curtain_wall_element_type_dictionary(wts_two, used_wts)
+    return used_wts
 
-    Filters by category.
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+# -------------------------------- none in place or loadable Curtain Wall Element types -------------------------------------------------------
 
-    :return: A filtered element collector containing ceiling instances.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-    
-    return rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_BuildingPad).WhereElementIsNotElementType()
-    
-def GetAllBuildingPadInstancesInModelByClass(doc):
-    '''
-    Gets all building pad elements placed in model.
 
-    Filters by class.
-    Since there are no in place families of type building pad possible, this should return the same elements as the by category filter.
+def get_curtain_wall_element_instances_by_category(doc):
+    """
+    Gets all CurtainWallElement elements instances placed in model.
+
+    Includes:
+
+    - curtain wall panels
+    - curtain wall mullions
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: A filtered element collector containing ceiling instances.
+    :return: A filtered element collector containing curtain wall element types.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-   
-    return rdb.FilteredElementCollector(doc).OfClass(rdb.BuildingPad).WhereElementIsNotElementType()
-
-def GetAllBuildingPadTypeIdsInModelByCategory(doc):
-    '''
-    Gets all building pad element type ids available in model.
+    """
+
+    multi_cat_filter = rdb.ElementMulticategoryFilter(
+        CURTAINWALL_ELEMENTS_CATEGORY_FILTER
+    )
+    return (
+        rdb.FilteredElementCollector(doc)
+        .WherePasses(multi_cat_filter)
+        .WhereElementIsNotElementType()
+    )
+
+
+def get_all_curtain_wall_element_type_ids_by_category(doc):
+    """
+    Gets all Curtain Wall Element element type ids available in model.
 
-    Filters by category.
+    Includes:
+
+    - curtain wall panels
+    - curtain wall mullions
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: A filtered element collector containing building pad type ids.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    :return: List of element ids representing curtain wall element types.
+    :rtype: list of Autodesk.Revit.DB.ElementId
+    """
 
     ids = []
-    colCat = GetAllBuildingPadTypesByCategory(doc)
-    ids = com.GetIdsFromElementCollector (colCat)
+    col_cat = get_all_curtain_wall_element_types_by_category(doc)
+    ids = com.get_ids_from_element_collector(col_cat)
     return ids
 
-def GetAllBuildingPadTypeIdsInModelByClass(doc):
-    '''
-    Gets all building pad element type ids available in model.
 
-    Filters by class.
-    Since there are no in place families of type building pad possible, this should return the same elements as the by category filter.
+def get_all_curtain_wall_element_types_by_category_excl_in_place(doc):
+    """
+    Gets all Curtain Wall Element element type available in model. Excludes in place family symbols.
+
+    Includes:
+
+    - curtain wall panels
+    - curtain wall mullions
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    
-    :return: A filtered element collector containing building pad type ids.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
 
-    ids = []
-    colClass = GetBuildingPadTypesByClass(doc)
-    ids = com.GetIdsFromElementCollector (colClass)
-    return ids
+    :return: List of curtain wall element types.
+    :rtype: list of Autodesk.Revit.DB.ElementType
+    """
+
+    collector = get_all_curtain_wall_element_types_by_category(doc)
+    elements = []
+    for c in collector:
+        if c.GetType() != rdb.FamilySymbol:
+            elements.append(c)
+    return elements
 
-def GetUsedBuildingPadTypeIds(doc):
-    '''
-    Gets all used building pad type ids.
 
-    Filters by category.
-    Used: at least one instance of this type is placed in the model.
+def get_all_curtain_wall_element_type_ids_by_category_excl_symbols(doc):
+    """
+    Gets all Curtain Wall Element element type ids available in model. Excludes in place family symbols.
+
+    Includes:
+
+    - curtain wall panels
+    - curtain wall mullions
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: List of element ids representing used building pad types.
+    :return: List of element ids representing curtain wall element types.
     :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllBuildingPadTypeIdsInModelByCategory, 1)
+    collector = get_all_curtain_wall_element_types_by_category(doc)
+    ids = []
+    for c in collector:
+        if c.GetType() != rdb.FamilySymbol:
+            ids.append(c.Id)
     return ids
 
-def FamilyNoTypesInUse(famTypeIds,unUsedTypeIds):
-    '''
-    Compares two lists of ids. True if any id is not in unUsedTypeIds.
-
-    TODO: check for more generic list comparison and remove this function.
-
-    :param famTypeIds: List of family type ids to check.
-    :type famTypeIds: List of Autodesk.Revit.DB.ElementId
-    :param unUsedTypeIds: Reference list of ids.
-    :type unUsedTypeIds: List of Autodesk.Revit.DB.ElementId
-
-    :return: True if any id from famTypeIds is not in unUsedTypeIds.
-    :rtype: bool
-    '''
-
-    match = True
-    for famTypeId in famTypeIds:
-        if (famTypeId not in unUsedTypeIds):
-            match = False
-            break
-    return match
- 
-# doc   current document
-def GetUnusedNonInPlaceBuildingPadTypeIdsToPurge(doc):
-    '''
-    Gets all unused building pad type id's.
-    
-    - Basic BuildingPad
-    
-    This method can be used to safely delete unused building pad types:
-    In the case that no building pad instance using any of the types is placed this will return all but one type id since\
-        Revit requires at least one building pad type definition to be in the model.
+
+# -------------------------------- loadable Curtain Wall Element types -------------------------------------------------------
+
+
+def get_all_curtain_wall_non_shared_symbol_ids_by_category(doc):
+    """
+    Gets a list of all loadable, non shared, family symbols (types) in the model of categories:
+
+    - curtain wall panels
+    - curtain wall mullions
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: List of element ids representing not used building pad types.
+    :return: List of element ids representing curtain wall family symbols.
     :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
-    # get unused type ids
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllBuildingPadTypeIdsInModelByClass, 0)
-    # make sure there is at least on BuildingPad type per system family left in model
-    BuildingPadTypes = SortBuildingPadTypesByFamilyName(doc)
-    for key, value in BuildingPadTypes.items():
-        if(key in BUILTIN_BUILDING_PAD_TYPE_FAMILY_NAMES):
-            if(FamilyNoTypesInUse(value,ids) == True):
-                # remove one type of this system family from unused list
-                ids.remove(value[0])
+    ids = []
+    multi_cat_filter = rdb.ElementMulticategoryFilter(
+        CURTAINWALL_ELEMENTS_CATEGORY_FILTER
+    )
+    collector = (
+        rdb.FilteredElementCollector(doc)
+        .WherePasses(multi_cat_filter)
+        .WhereElementIsElementType()
+    )
+    for c in collector:
+        if c.GetType() == rdb.FamilySymbol:
+            fam = c.Family
+            p_value = rParaGet.get_built_in_parameter_value(
+                fam, rdb.BuiltInParameter.FAMILY_SHARED
+            )
+            if p_value != None and p_value == "No" and c.Id not in ids:
+                ids.append(c.Id)
     return ids
- 
-# -------------------------------- In place BuildingPad types -------------------------------------------------------
-# no such thing
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitCategoryData.py` & `DuHast-0.0.7/src/duHast/Revit/Categories/Data/category_data_processor.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,267 +1,242 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Family category data class.
+Family category data processor class.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
-#
-#
-
-from duHast.APISamples import IFamilyData as IFamData
-from duHast.Utilities import Utility as util
-from duHast.APISamples import RevitCategories as rCat
-
-# import Autodesk
-#import Autodesk.Revit.DB as rdb
-
-# data dictionary key values specific to this class
-CATEGORY_NAME = 'categoryName'
-SUB_CATEGORY_NAME = 'subCategoryName'
-SUB_CATEGORY_ID = 'subCategoryId' 
-GRAPHIC_PROPERTY_KEY_PREFIX = 'graphicProperty'
-GRAPHIC_PROPERTY_KEY_PREFIX_DELIMITER = '_'
-
-class CategoryData(IFamData.IFamilyData):
-    
-    def __init__(self, rootPath=None, rootCategoryPath=None, dataType=None):
-        '''
-        Class constructor
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
+#
+#
+#
+
+from duHast.Revit.Family.Data.ifamily_processor import IFamilyProcessor
+from duHast.Revit.Categories.Data import category_data as rCatData
+from duHast.Revit.Family.Data import ifamily_data as IFamData
+from duHast.Utilities.Objects import result as res
+from duHast.Revit.Categories.Utility import category_property_names as rCatPropNames
+
+
+class CategoryProcessor(IFamilyProcessor):
+    def __init__(self, pre_actions=None, post_actions=None):
+        """
+        Class constructor.
+        """
+
+        # setup report header
+        key_prefix = (
+            rCatData.GRAPHIC_PROPERTY_KEY_PREFIX
+            + rCatData.GRAPHIC_PROPERTY_KEY_PREFIX_DELIMITER
+        )
+        string_report_headers = [
+            IFamData.ROOT,
+            IFamData.ROOT_CATEGORY,
+            IFamData.FAMILY_NAME,
+            IFamData.FAMILY_FILE_PATH,
+            IFamData.USAGE_COUNTER,
+            IFamData.USED_BY,
+            rCatData.CATEGORY_NAME,
+            rCatData.SUB_CATEGORY_NAME,
+            rCatData.SUB_CATEGORY_ID,
+            key_prefix + rCatPropNames.CATEGORY_GRAPHIC_STYLE_3D,
+            key_prefix + rCatPropNames.CATEGORY_GRAPHIC_STYLE_CUT,
+            key_prefix + rCatPropNames.CATEGORY_GRAPHIC_STYLE_PROJECTION,
+            key_prefix + rCatPropNames.PROPERTY_MATERIAL_NAME,
+            key_prefix + rCatPropNames.PROPERTY_MATERIAL_ID,
+            key_prefix + rCatPropNames.PROPERTY_LINE_WEIGHT_CUT_NAME,
+            key_prefix + rCatPropNames.PROPERTY_LINE_WEIGHT_PROJECTION_NAME,
+            key_prefix + rCatPropNames.PROPERTY_LINE_COLOUR_RED_NAME,
+            key_prefix + rCatPropNames.PROPERTY_LINE_COLOUR_GREEN_NAME,
+            key_prefix + rCatPropNames.PROPERTY_LINE_COLOUR_BLUE_NAME,
+        ]
+
+        # store data type  in base class
+        super(CategoryProcessor, self).__init__(
+            pre_actions=pre_actions,
+            post_actions=[self._post_action_update_used_subcategories],
+            data_type="Category",
+            string_report_headers=string_report_headers,
+        )
+
+        # self.data = []
+        # self.dataType = 'Category'
+
+        # list of corner cases when it comes to category checking: imports in families or Reference planes ... ( english language specific!! )
+        self.category_check_corner_cases = ["Imports in Families", "Reference Planes"]
+
+        # self.preActions = preActions
+        # set default post action to updated categories used in root processor with any categories found in nested
+        # families
+        # self.postActions = [self._postActionUpdateUsedSubcategories]
+        # add any other post actions
+        if post_actions != None:
+            for p_action in post_actions:
+                self.post_actions.append(p_action)
+
+    def process(self, doc, root_path, root_category_path):
+        """
+        Calls processor instance with the document and root path provided and adds processor instance to class property .data
 
-        :param rootPath: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
-            This includes the actual family name as the last node.
-        :type rootPath: str
-        :param dataType: Human readable data type descriptor
-        :type dataType: str
-        '''
-        # todo: check inheritance!!
-        # super(CategoryData, self).__init__(rootPath, dataType)
-
-        self.data = []
-        
-        if(dataType != None):
-            self.dataType = dataType
-        else:
-            self.dataType = 'not declared'
-        
-        if(rootPath != None):
-            self.rootPath = rootPath
-        else:
-            self.rootPath = '-'
-        
-        if(rootCategoryPath != None):
-            self.rootCategoryPath = rootCategoryPath
-        else:
-            self.rootCategoryPath = '-'
-
-
-    def add_Data(self,root, rootCategoryPath, famName, famPath, useCounter, usedBy, famCatName, subCatName, subCatId, catGraStyleThreeD,
-        catGraStyleCut, catGraStylePro, propMatName, propMatId, propLineWeightCutName, propLineWeightProjectionName, propLineColRed, propLineColGreen, propLineColBlue):
-        
-        dic = {
-            IFamData.ROOT: root,
-            IFamData.ROOT_CATEGORY: rootCategoryPath,
-            IFamData.FAMILY_NAME: famName,
-            IFamData.FAMILY_FILE_PATH : famPath,
-            IFamData.USAGE_COUNTER: useCounter,
-            IFamData.USED_BY : usedBy,
-            CATEGORY_NAME : famCatName,
-            SUB_CATEGORY_NAME : subCatName,
-            SUB_CATEGORY_ID : subCatId,
-            rCat.CATEGORY_GRAPHIC_STYLE_3D : catGraStyleThreeD,
-            rCat.CATEGORY_GRAPHIC_STYLE_CUT : catGraStyleCut,
-            rCat.CATEGORY_GRAPHIC_STYLE_PROJECTION : catGraStylePro,
-            rCat.PROPERTY_MATERIAL_NAME : propMatName,
-            rCat.PROPERTY_MATERIAL_ID : propMatId,
-            rCat.PROPERTY_LINE_WEIGHT_CUT_NAME : propLineWeightCutName,
-            rCat.PROPERTY_LINE_WEIGHT_PROJECTION_NAME : propLineWeightProjectionName,
-            rCat.PROPERTY_LINE_COLOUR_RED_NAME : propLineColRed,
-            rCat.PROPERTY_LINE_COLOUR_GREEN_NAME : propLineColGreen,
-            rCat.PROPERTY_LINE_COLOUR_BLUE_NAME : propLineColBlue
-            }
-
-        self.data.append(dic)
-    
-    def _createData(self,root, rootCategoryPath, famName, famPath, useCounter, usedBy, famCatName, subCatName, subCatId, categoryGraphicProperties):
-        '''
-        Generates dictionary object from data past in.
-
-        CategoryGraphicProperties will be flattened with prefix 'graphicProperty'
-
-        :param root: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
-            This includes the actual family name as the last node.
-        :type root: str
-        :param famName: The family name
-        :type famName: str
-        :param famPath: The family saved file path
-        :type famPath: str
-        :param useCounter: Counter of how many objects in the family are of this category
-        :type useCounter: int
-        :param usedBy: List of element ids of elements of this category.
-        :type usedBy: [Autodesk.Revit.DB.ElementId]
-        :param famCatName: The families category.
-        :type famCatName: str
-        :param subCatName: The subcategory name.
-        :type subCatName: str
-        :param subCatId: The subcategory id.
-        :type subCatId: Autodesk.Revit.DB.ElementId
-        :param categoryGraphicProperties: List of dictionaries describing the graphic properties of this category.
-        :type categoryGraphicProperties: [dict]
-        
-        :return: A flatt dictionary describing key values and properties of a category.
-        :rtype: dict
-        '''
-
-        dic = {
-            IFamData.ROOT: root,
-            IFamData.ROOT_CATEGORY: rootCategoryPath,
-            IFamData.FAMILY_NAME: famName,
-            IFamData.FAMILY_FILE_PATH : famPath,
-            IFamData.USAGE_COUNTER: useCounter,
-            IFamData.USED_BY : usedBy,
-            CATEGORY_NAME : famCatName,
-            SUB_CATEGORY_NAME : subCatName,
-            SUB_CATEGORY_ID : subCatId
-            }
-        
-        # flatten dictionary
-        for  d in categoryGraphicProperties:
-            dummy = util.flatten(d, GRAPHIC_PROPERTY_KEY_PREFIX, GRAPHIC_PROPERTY_KEY_PREFIX_DELIMITER)
-            dic.update(dummy)
-
-        return dic
-
-    def _buildData(self, mainSubCats, mainCatName, doc):
-        '''
-        Extracts for each category past in, its properties and usage and adds that data to class property .data
-
-        :param mainSubCats: List of sub categories to be processed.
-        :type mainSubCats: [Autodesk.Revit.DB.Category]
-        :param mainCatName: The parent category name.
-        :type mainCatName: str
-        :param doc: Current family document
+        :param doc: Current family document.
         :type doc: Autodesk.Revit.DB.Document
-        '''
-
-        # get usage of each main sub category
-        for key,subCat in mainSubCats.items():
-            # get elements using category
-            elementDic = rCat.GetElementsByCategory(doc, subCat)
-            # get category property
-            catProps = rCat.GetCategoryProperties(subCat, doc)
-            # add element counter for 3D, Cut, Elevation style
-            useCounter = 0
-            for key in elementDic:
-                useCounter = useCounter + len (elementDic[key])        
-            # add element ids integer value in 3D, Cut, Elevation style
-            usedByIds = []
-            for key in elementDic:
-                for id in elementDic[key]:
-                    usedByIds.append(id.IntegerValue)
-
-            # build data dictionary   
-            dic = self._createData(
-                self.rootPath,
-                self.rootCategoryPath,
-                self._stripFileExtension(doc.Title),
-                doc.PathName,
-                useCounter,
-                usedByIds,
-                mainCatName,
-                subCat.Name,
-                subCat.Id.IntegerValue,
-                catProps
+        :param root_path: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
+            This includes the actual family name as the last node.
+        :type root_path: str
+        :param root_category_path: The category path of the nested family in a tree: rootFamilyCategory::nestedFamilyOneCategory::nestedFamilyTwoCategory\
+            This includes the actual family category as the last node.
+        :type root_category_path: str
+        """
+
+        dummy = rCatData.CategoryData(root_path, root_category_path, self.data_type)
+        dummy.process(doc)
+        self.data.append(dummy)
+
+    # --------------------------------------------- post action ----------------------------------------------------------
+
+    def _add_data(
+        self,
+        processor,
+        root,
+        root_category_path,
+        fam_name,
+        fam_path,
+        use_counter,
+        used_by,
+        fam_cat_name,
+        sub_cat_name,
+        sub_cat_id,
+        cat_gra_style_three_d,
+        cat_gra_style_cut,
+        cat_gra_style_pro,
+        prop_mat_name,
+        prop_mat_id,
+        prop_line_weight_cut_name,
+        prop_line_weight_projection_name,
+        prop_line_col_red,
+        prop_line_col_green,
+        prop_line_col_blue,
+    ):
+
+        processor.add_Data(
+            root,
+            root_category_path,
+            fam_name,
+            fam_path,
+            use_counter,
+            used_by,
+            fam_cat_name,
+            sub_cat_name,
+            sub_cat_id,
+            cat_gra_style_three_d,
+            cat_gra_style_cut,
+            cat_gra_style_pro,
+            prop_mat_name,
+            prop_mat_id,
+            prop_line_weight_cut_name,
+            prop_line_weight_projection_name,
+            prop_line_col_red,
+            prop_line_col_green,
+            prop_line_col_blue,
+        )
+
+    def _is_sub_category_present(self, root_family_data, nested_family_sub_category):
+        match = None
+        # check whether sub category is present
+        for root_fam in root_family_data:
+            if (
+                root_fam[rCatData.CATEGORY_NAME]
+                == nested_family_sub_category[rCatData.CATEGORY_NAME]
+                and root_fam[rCatData.SUB_CATEGORY_NAME]
+                == nested_family_sub_category[rCatData.SUB_CATEGORY_NAME]
+            ):
+                match = root_fam
+                break
+        return match
+
+    def _update_root_family_data(
+        self, root_family_data, nested_families_sub_categories
+    ):
+        # loop over nested family subcategory data
+        for nested_sub_category in nested_families_sub_categories:
+            # check if sub category is already in root family
+            matching_root_fam_category = self._is_sub_category_present(
+                root_family_data, nested_sub_category
             )
-            self.data.append(dic)
-
-    def _buildDataNonMainSubCats(self, mainSubCats, mainCatName, doc):
-        '''
-        Extracts for each category past in, its properties and usage and adds that data to class property .data
-
-        :param mainSubCats: List of sub categories to be processed.
-        :type mainSubCats: [Autodesk.Revit.DB.Category]
-        :param mainCatName: The parent category name.
-        :type mainCatName: str
-        :param doc: Current family document
-        :type doc: Autodesk.Revit.DB.Document
-        '''
-
-        # get usage of each main sub category
-        for key,subCat in mainSubCats.items():
-            # set up an empty dic for any sub category not belonging to the main category (no elements in this family can be on those)
-            # Exception: the only elements will be Imports and reference planes
-            elementDic = {}
-            if(mainCatName == 'Imports in Families' or mainCatName == 'Reference Planes'):
-                # get elements using category
-                elementDic = rCat.GetElementsByCategory(doc, subCat)
-            # get category property
-            catProps = rCat.GetCategoryProperties(subCat, doc)
-            # add element counter for 3D, Cut, Elevation style
-            useCounter = 0
-            for key in elementDic:
-                useCounter = useCounter + len (elementDic[key])        
-            # add element ids integer value in 3D, Cut, Elevation style
-            usedByIds = []
-            for key in elementDic:
-                for id in elementDic[key]:
-                    usedByIds.append(id.IntegerValue)
-
-            # build data dictionary   
-            dic = self._createData(
-                self.rootPath,
-                self.rootCategoryPath,
-                self._stripFileExtension(doc.Title),
-                doc.PathName,
-                useCounter,
-                usedByIds,
-                mainCatName,
-                subCat.Name,
-                subCat.Id.IntegerValue,
-                catProps
+            if matching_root_fam_category != None:
+                # update used by list
+                if (
+                    nested_sub_category[IFamData.FAMILY_NAME]
+                    not in matching_root_fam_category[IFamData.USED_BY]
+                ):
+                    # add the root path to the used by list for ease of identification of the origin of this subcategory usage
+                    matching_root_fam_category[IFamData.USED_BY].append(
+                        nested_sub_category[IFamData.ROOT]
+                    )
+                    # update used by counter
+                    matching_root_fam_category[IFamData.USAGE_COUNTER] = (
+                        matching_root_fam_category[IFamData.USAGE_COUNTER] + 1
+                    )
+            else:
+                pass
+                # nothing to do if that category has not been reported to start off with
+                # this category could, for example, belong to the section marker family present in most 3d families
+
+    def _get_used_subcategories(self, data):
+        used_subcategories = []
+        for d in data:
+            if d[IFamData.USAGE_COUNTER] > 0:
+                # get the family category
+                category_path = d[IFamData.ROOT_CATEGORY].split(" :: ")
+                # which is the last entry in the root category path
+                category = category_path[len(category_path) - 1]
+                # select only items which either belong to the category of the family or
+                # are corner cases like imports in families or Reference planes ... ( english language specific!! )
+                if (
+                    category == d[rCatData.CATEGORY_NAME]
+                    or d[rCatData.CATEGORY_NAME] in self.category_check_corner_cases
+                ):
+                    used_subcategories.append(d)
+        return used_subcategories
+
+    def _post_action_update_used_subcategories(self, doc):
+        return_value = res.Result()
+        try:
+            # find all subcategories of nested families
+            nested_family_data = self._find_nested_families_data()
+            # get used sub categories from nested data
+            nested_family_used_sub_categories = self._get_used_subcategories(
+                nested_family_data
             )
-            self.data.append(dic)
-
-    def process(self, doc):
-        '''
-        Collects all category data from the document and stores it in the class property .data
-
-        :param doc: Current family document
-        :type doc: Autodesk.Revit.DB.Document
-        '''
-
-        # get the family category name:
-        famCatName = list(rCat.GetFamilyCategory(doc))[0]
-        # get all sub categories of the family category
-        mainSubCats = rCat.GetMainSubCategories(doc)
-        # get all sub categories of non family category with a positive Id (indicates a custom category)
-        # this include imported element categories
-        otherCustomSubCats = rCat.GetOtherCustomSubCategories(doc)
-        # get usage of each main sub category
-        self._buildData(mainSubCats, famCatName, doc)
-         # add any other sub category if exist
-        if(len(otherCustomSubCats) > 0):
-            for categoryKey, otherSubMainCat in otherCustomSubCats.items():
-                if(len(otherSubMainCat) > 0):
-                    # get usage of each other sub category
-                    self._buildDataNonMainSubCats(otherSubMainCat, categoryKey, doc)
-        
-    def get_Data(self):
-        return self.data
+            # update root family data only
+            root_family_data = self._find_root_family_data()
+            # update root processor data as required
+            self._update_root_family_data(
+                root_family_data, nested_family_used_sub_categories
+            )
+            return_value.update_sep(
+                True, "Post Action Update subcategories data successful completed."
+            )
+        except Exception as e:
+            return_value.update_sep(
+                False,
+                "Post Action Update subcategories data failed with exception: {}".format(
+                    e
+                ),
+            )
+        return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitCategoryDataProcessor.py` & `DuHast-0.0.7/src/duHast/Revit/Family/Data/family_rename_find_host_families.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,178 +1,195 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Family category data processor class.
+Finds host families of nested families requiring to be renamed.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+
+- read file rename change list:
+-   text file (tab separated) with columns: currentFamilyName   currentFamilyFilePath	categoryName newFamilyName
+-   note: current family file path could be blank in situations where just a rename of a nested family is required...
+- read base data file processing list (created by RevitFamilyBaseDataProcessor module)
+- extract all root families (no :: in root path)
+- extract all nested families ( :: in root path)
+- loop over nested families and find any family where:
+    - family at first nesting level is in rename list by name and category
+    - extract root family name and add to identified host family list
+
+- loop over root families
+-   find match in identified host families
+- write out root family date: family file path, family name, category
+
+"""
+
+
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
-#
-#
-
-from duHast.APISamples.IFamilyProcessor import IFamilyProcessor
-from duHast.APISamples import RevitCategories as rCat
-from duHast.APISamples import RevitCategoryData as rCatData
-from duHast.APISamples import IFamilyData as IFamData
-from duHast.Utilities import Result as res
-
-class CategoryProcessor(IFamilyProcessor):
-
-    def __init__(self, preActions = None, postActions = None):
-        '''
-        Class constructor.
-        '''
-        self.data = []
-        self.dataType = 'Category'
-
-        # list of corner cases when it comes to category checking: imports in families or Reference planes ... ( english language specific!! )
-        self.CategoryCheckCornerCases = [
-            'Imports in Families',
-            'Reference Planes'
-        ]
-
-        keyPrefix = rCatData.GRAPHIC_PROPERTY_KEY_PREFIX + rCatData.GRAPHIC_PROPERTY_KEY_PREFIX_DELIMITER
-        self.stringReportHeaders = [
-            IFamData.ROOT,
-            IFamData.ROOT_CATEGORY,
-            IFamData.FAMILY_NAME,
-            IFamData.FAMILY_FILE_PATH,
-            IFamData.USAGE_COUNTER,
-            IFamData.USED_BY,
-            rCatData.CATEGORY_NAME,
-            rCatData.SUB_CATEGORY_NAME,
-            rCatData.SUB_CATEGORY_ID,
-            keyPrefix + rCat.CATEGORY_GRAPHIC_STYLE_3D,
-            keyPrefix + rCat.CATEGORY_GRAPHIC_STYLE_CUT,
-            keyPrefix + rCat.CATEGORY_GRAPHIC_STYLE_PROJECTION,
-            keyPrefix + rCat.PROPERTY_MATERIAL_NAME,
-            keyPrefix + rCat.PROPERTY_MATERIAL_ID,
-            keyPrefix + rCat.PROPERTY_LINE_WEIGHT_CUT_NAME,
-            keyPrefix + rCat.PROPERTY_LINE_WEIGHT_PROJECTION_NAME,
-            keyPrefix + rCat.PROPERTY_LINE_COLOUR_RED_NAME,
-            keyPrefix + rCat.PROPERTY_LINE_COLOUR_GREEN_NAME,
-            keyPrefix + rCat.PROPERTY_LINE_COLOUR_BLUE_NAME
-        ]
-        self.preActions = preActions
-        # set default post action to updated categories used in root processor with any categories found in nested 
-        # families
-        self.postActions = [self._postActionUpdateUsedSubcategories]
-        # add any other post actions
-        if (postActions != None):
-            for pAction in postActions:
-                self.postActions.append(pAction)
-
-
-    def process(self, doc, rootPath, rootCategoryPath):
-        '''
-        Calls processor instance with the document and root path provided and adds processor instance to class property .data
-
-        :param doc: Current family document.
-        :type doc: Autodesk.Revit.DB.Document
-        :param rootPath: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
-            This includes the actual family name as the last node.
-        :type rootPath: str
-        '''
-
-        dummy = rCatData.CategoryData(rootPath, rootCategoryPath, self.dataType)
-        dummy.process(doc)
-        self.data.append(dummy)
-    
-    # --------------------------------------------- post action ----------------------------------------------------------
-
-    def _add_Data(self, processor, root, rootCategoryPath, famName, famPath, useCounter, usedBy, famCatName, subCatName, subCatId, catGraStyleThreeD,
-        catGraStyleCut, catGraStylePro, propMatName, propMatId, propLineWeightCutName, propLineWeightProjectionName, propLineColRed, propLineColGreen, propLineColBlue):
-        
-        processor.add_Data(
-            root,
-            rootCategoryPath, 
-            famName, 
-            famPath, 
-            useCounter, 
-            usedBy, 
-            famCatName, 
-            subCatName, 
-            subCatId,
-            catGraStyleThreeD,
-            catGraStyleCut,
-            catGraStylePro,
-            propMatName,
-            propMatId,
-            propLineWeightCutName,
-            propLineWeightProjectionName,
-            propLineColRed,
-            propLineColGreen,
-            propLineColBlue)
-        
-
-    def _isSubCategoryPresent(self,rootFamilyData, nestedFamilySubCategory):
-        match = None
-        # check whether sub category is present
-        for rootFam in rootFamilyData:
-            if (rootFam[rCatData.CATEGORY_NAME] == nestedFamilySubCategory[rCatData.CATEGORY_NAME] and rootFam[rCatData.SUB_CATEGORY_NAME] == nestedFamilySubCategory[rCatData.SUB_CATEGORY_NAME]):
-                match = rootFam
-                break
-        return match
-
-    def _updateRootFamilyData(self, rootFamilyData, nestedFamiliesSubCategories):
-        # loop over nested family subcategory data
-        for nestedSubCategory in nestedFamiliesSubCategories:
-            # check if sub category is already in root family
-            matchingRootFamCategory = self._isSubCategoryPresent(rootFamilyData, nestedSubCategory)
-            if(matchingRootFamCategory != None):
-                # update used by list
-                if(nestedSubCategory[IFamData.FAMILY_NAME] not in matchingRootFamCategory[IFamData.USED_BY]):
-                    # add the root path to the used by list for ease of identification of the origin of this subcategory usage
-                    matchingRootFamCategory[IFamData.USED_BY].append(nestedSubCategory[IFamData.ROOT])
-                    # update used by counter
-                    matchingRootFamCategory[IFamData.USAGE_COUNTER] = matchingRootFamCategory[IFamData.USAGE_COUNTER] + 1
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
+#
+#
+#
+
+# import clr
+# import System
+from duHast.Utilities.Objects.timer import Timer
+
+from duHast.Utilities.Objects import result as res
+
+# from duHast.Utilities import Utility as util
+from duHast.Revit.Family.Data import family_base_data_utils as rFamBaseDataUtils
+from duHast.Revit.Family import family_rename_files_utils as rFamRenameUtils
+
+# ---------------------------------------------------------------------------------------------------------------
+#                      find families containing nested families needing to be renamed
+# ---------------------------------------------------------------------------------------------------------------
+
+
+def _find_host_families(overall_family_base_nested_data, file_rename_list):
+    """
+    Finds all root family names and categories where the first level nested family is one which needs to be renamed.
+
+    :param overall_family_base_nested_data: A list containing all root families.
+    :type overall_family_base_nested_data: [rootFamily]
+    :param file_rename_list: A list containing all families needing to be renamed.
+    :type file_rename_list: [renameFamily]
+
+    :return: A dictionary where:
+
+        - key is the family name and category concatenated and
+        - value is a tuple in format 0: family name, 1: family category
+
+    :rtype: {str: (str,str)}
+    """
+
+    host_families = {}
+    for file_rename_family in file_rename_list:
+        hosts = rFamBaseDataUtils.find_direct_host_families(
+            file_rename_family, overall_family_base_nested_data
+        )
+        # update dictionary with new hosts only
+        for h in hosts:
+            if h not in host_families:
+                host_families[h] = hosts[h]
+    return host_families
+
+
+def find_host_families_with_nested_families_requiring_rename(input_directory_path):
+    """
+    Finds all host families in data set containing nested families needing to be renamed.
+
+    :param input_directory_path: Fully qualified directory path containing rename directives and family base data report.
+    :type input_directory_path: str
+
+    :return:
+        Result class instance.
+
+        - result.status: True if any host families are found with nested families needing renaming, otherwise False.
+        - result.message: processing steps with time stamps
+        - result.result: [rootFamily]
+
+        On exception:
+
+        - result.status (bool) will be False.
+        - result.message will contain an exception message
+        - result.result will be empty
+
+    :rtype: :class:`.Result`
+    """
+
+    # set up a timer
+    t_process = Timer()
+    t_process.start()
+
+    return_value = res.Result()
+    # read overall family base data from file
+    try:
+        (
+            overall_family_base_root_data,
+            overall_family_base_nested_data,
+        ) = rFamBaseDataUtils.read_overall_family_data_list_from_directory(
+            input_directory_path
+        )
+        return_value.append_message(
+            "{} Read overall family base data report. {} root entries found and {} nested entries found.".format(
+                t_process.stop(),
+                len(overall_family_base_root_data),
+                len(overall_family_base_nested_data),
+            )
+        )
+        # check if input file existed and contained data
+        if len(overall_family_base_root_data) > 0:
+            t_process.start()
+            file_rename_list_status = rFamRenameUtils.get_rename_directives(
+                input_directory_path
+            )
+            return_value.append_message(
+                "{} Read data from file! Rename family entries [{} ] found.".format(
+                    t_process.stop(), len(file_rename_list_status.result)
+                )
+            )
+            # check if any rename directives
+            if len(file_rename_list_status.result) > 0:
+                before = len(overall_family_base_nested_data)
+                t_process.start()
+                # reduce workload by culling not needed nested family data
+                overall_family_base_nested_data = (
+                    rFamBaseDataUtils.cull_nested_base_data_blocks(
+                        overall_family_base_nested_data
+                    )
+                )
+                return_value.append_message(
+                    "{} Culled nested family base data from : {} to: {} families.".format(
+                        t_process.stop(), before
+                    ),
+                    len(overall_family_base_nested_data),
+                )
+
+                t_process.start()
+                # get a list of simplified root data families extracted from nested family path data
+                root_fam_simple = rFamBaseDataUtils.find_all_direct_host_families(
+                    file_rename_list_status.result, overall_family_base_nested_data
+                )
+                return_value.append_message(
+                    "{} Found simplified root families: {}".format(
+                        t_process.stop(), len(root_fam_simple)
+                    )
+                )
+
+                t_process.start()
+                # identify actual root families with nested families at top level which require renaming.
+                root_families = rFamBaseDataUtils.find_root_families_from_hosts(
+                    root_fam_simple, overall_family_base_root_data
+                )
+                return_value.append_message(
+                    "{} Found {} root families.".format(
+                        t_process.stop(), len(root_families)
+                    )
+                )
+                return_value.result = root_families
             else:
-                pass
-                # nothing to do if that category has not been reported to start off with 
-                # this category could, for example, belong to the section marker family present in most 3d families
-
-    def _getUsedSubcategories(self, data):
-        usedSubcategories = []
-        for d in data:
-            if(d[IFamData.USAGE_COUNTER] > 0):
-                # get the family category
-                categoryPath = d[IFamData.ROOT_CATEGORY].split(' :: ')
-                # which is the last entry in the root category path
-                category = categoryPath[len(categoryPath)-1]
-                # select only items which either belong to the category of the family or 
-                # are corner cases like imports in families or Reference planes ... ( english language specific!! )
-                if (category == d[rCatData.CATEGORY_NAME] or d[rCatData.CATEGORY_NAME] in self.CategoryCheckCornerCases):
-                    usedSubcategories.append(d)
-        return usedSubcategories
-
-    def _postActionUpdateUsedSubcategories(self, doc):
-        returnValue = res.Result()
-        try:
-            # find all subcategories of nested families
-            nestedFamilyData = self._findNestedFamiliesData()
-            # get used sub categories from nested data
-            nestedFamilyUsedSubCategories = self._getUsedSubcategories(nestedFamilyData)
-            # update root family data only
-            rootFamilyData = self._findRootFamilyData()
-            # update root processor data as required
-            self._updateRootFamilyData(rootFamilyData, nestedFamilyUsedSubCategories)
-            returnValue.UpdateSep(True, 'Post Action Update subcategories data successful completed.')
-        except Exception as e:
-            returnValue.UpdateSep(False, 'Post Action Update subcategories data failed with exception: ' + str(e))
-        return returnValue
+                return_value.update_sep(
+                    False, "No rename directives found. Aborted operation!"
+                )
+        else:
+            return_value.update_sep(
+                False, "No base family data found. Aborted operation!"
+            )
+    except Exception as e:
+        return_value.update_sep(
+            False, "Failed to find host families with exception: ".format(e)
+        )
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitCategoryDataPurgeUnused.py` & `DuHast-0.0.7/src/duHast/Revit/Categories/Data/category_data_purge_unused.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,85 +1,98 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Family category purge unused utilities.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 This will delete all subcategories which are user created ( id greater then 0) and are not used by any element in the family or nested families.
 
 - requires a revit category processor object
 
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 # class used for stats reporting
-from duHast.Utilities import Result as res
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import IFamilyData as IFamData
-from duHast.APISamples import RevitCategoryData as rCatData
+from duHast.Utilities.Objects import result as res
+from duHast.Revit.Common import delete as rDel
+from duHast.Revit.Family.Data import ifamily_data as IFamData
+from duHast.Revit.Categories.Data import category_data as rCatData
 
 import Autodesk.Revit.DB as rdb
 
-def PurgeUnused(doc, processor):
-    '''
+
+def purge_unused_sub_categories(doc, processor):
+    """
     This will delete all subcategories which are user created ( id greater then 0) and are not used by any element in the family or nested families.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :param processor: An CategoryProcessor object containing all subcategory information of the family document and any nested families.
     :type processor: :class:`.CategoryProcessor'
 
-    :return: 
+    :return:
         Result class instance.
 
         - True if all unused subcategories where deleted successfully or none needed to be deleted. Otherwise False.
-        - Result.message property updated in format: Found unused sub category: family category Name : subcategory Name [subcategory Id] 
-        
+        - Result.message property updated in format: Found unused sub category: family category Name : subcategory Name [subcategory Id]
+
         On exception:
-        
+
         - status (bool) will be False.
         - message will contain the exception message.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     # from processor instance get all root category entries where usage counter == 0 and subCategoryId > 0 (pointing to a custom sub category and not a built in one).
     # delete those subcategories by id
 
-    returnValue = res.Result()
+    return_value = res.Result()
 
-    idsToDelete = []
+    ids_to_delete = []
     # get categories found in root processor data only
-    rootFamData = processor._findRootFamilyData()
+    root_fam_data = processor._findRootFamilyData()
     # get all root category entries where usage counter == 0 and subCategoryId > 0 (pointing to a custom sub category and not a built in one).
-    for rootFam in rootFamData:
-        if (rootFam[IFamData.USAGE_COUNTER] == 0 and rootFam[rCatData.SUB_CATEGORY_ID] > 0):
-            returnValue.AppendMessage('Found unused sub category: ' + rootFam[rCatData.CATEGORY_NAME] + ':' + rootFam[rCatData.SUB_CATEGORY_NAME] +' ['+str(rootFam[rCatData.SUB_CATEGORY_ID])+']')
-            idsToDelete.append(rdb.ElementId(rootFam[rCatData.SUB_CATEGORY_ID]))
+    for root_fam in root_fam_data:
+        if (
+            root_fam[IFamData.USAGE_COUNTER] == 0
+            and root_fam[rCatData.SUB_CATEGORY_ID] > 0
+        ):
+            return_value.append_message(
+                "Found unused sub category: {} : {} [{}]".format(
+                    root_fam[rCatData.CATEGORY_NAME],
+                    root_fam[rCatData.SUB_CATEGORY_NAME],
+                    (root_fam[rCatData.SUB_CATEGORY_ID]),
+                )
+            )
+            ids_to_delete.append(rdb.ElementId(root_fam[rCatData.SUB_CATEGORY_ID]))
     # delete any subcategories found
-    if(len(idsToDelete) > 0):
-        resultDelete = com.DeleteByElementIds(doc, idsToDelete, 'Deleting unused sub categories.', 'Subcategories')
-        returnValue.Update(resultDelete)
+    if len(ids_to_delete) > 0:
+        result_delete = rDel.delete_by_element_ids(
+            doc, ids_to_delete, "Deleting unused sub categories.", "Subcategories"
+        )
+        return_value.update(result_delete)
     else:
-        returnValue.UpdateSep(True, 'No unused categories found. Nothing was deleted.')
-    return returnValue
-    
+        return_value.update_sep(
+            True, "No unused categories found. Nothing was deleted."
+        )
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitCeilings.py` & `DuHast-0.0.7/src/duHast/Revit/Family/family_utils.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,516 +1,461 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Revit ceilings helper functions.
+Revit families helper functions.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2021  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
 import System
 
-# import common library modules
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.APISamples import RevitFamilyUtils as rFam
-from duHast.APISamples import RevitGeometry as rGeo
-from duHast.APISamples import RevitDesignSetOptions as rDesignO
-from duHast.DataSamples import DataCeiling as dCeiling
-from duHast.APISamples import RevitPhases as rPhase
 
-# import Autodesk
-import Autodesk.Revit.DB as rdb
+clr.AddReference("System.Core")
+clr.ImportExtensions(System.Linq)
+clr.AddReference("System")
 
-# -------------------------------------------- common variables --------------------
-#: header used in reports
-REPORT_CEILINGS_HEADER = ['HOSTFILE', 'CEILINGTYPEID', 'CEILINGTYPENAME']
-#: Built in family name for compound ceilings
-COMPOUND_CEILING_FAMILY_NAME = 'Compound Ceiling'
-#: Built in family name for basic ceilings
-BASIC_CEILING_FAMILY_NAME = 'Basic Ceiling'
-#: Built in family name for roof soffits
-ROOF_SOFFIT_FAMILY_NAME = 'Roof Soffit'
-#: List of all Built in ceiling family names
-BUILTIN_CEILING_TYPE_FAMILY_NAMES = [
-    COMPOUND_CEILING_FAMILY_NAME,
-    BASIC_CEILING_FAMILY_NAME,
-    ROOF_SOFFIT_FAMILY_NAME
-]
-
-# --------------------------------------------- utility functions ------------------
-
-def GetAllCeilingTypesByCategory(doc):
-    '''
-    Gets a filtered element collector of all ceiling types in the model:
-
-    - Compound Ceiling
-    - In place families or loaded families
-    - Basic Ceiling
 
-    Filters by category.
-    It will therefore not return any roof soffit types ..
+# import common library
+# utility functions for most commonly used Revit API tasks
+from duHast.Revit.Common import parameter_get_utils as rParaGet
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+# utilities
+from duHast.Utilities import files_io as fileIO
 
-    :return: A filtered element collector containing ceiling types.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Ceilings).WhereElementIsElementType()
-    return collector
+# class used for stats reporting
+from duHast.Utilities.Objects import result as res
 
-def GetCeilingTypesByClass(doc):
-    '''
-    Gets a filtered element collector of all ceiling types in the model:
+# implementation of Revit API callback required when loading families into a Revit model
+from duHast.Revit.Family import family_load_option as famLoadOpt
 
-    - Roof Soffit
-    - Compound Ceiling
-    - Basic Ceiling
+# load everything required from family load call back
+from duHast.Revit.Family.family_load_option import *
+from duHast.Revit.Common import transaction as rTran
 
-    Filters by class.
-    It will therefore not return any in place family types.
+# import Autodesk Revit DataBase namespace
+import Autodesk.Revit.DB as rdb
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+from duHast.Revit.Family.Utility.loadable_family_categories import (
+    CATEGORIES_LOADABLE_3D,
+    CATEGORIES_LOADABLE_TAGS,
+)
+
+# --------------------------------------------------- Family Loading / inserting -----------------------------------------
+
+
+def load_family(doc, family_file_path):
+    """
+    Loads or reloads a single family into a Revit document.
+
+    Will load/ reload family provided in in path. By default the parameter values in the project file will be overwritten
+    with parameter values in family.
+
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param family_file_path: The fully qualified file path of the family to be loaded.
+    :type family_file_path: str
+    :raise: None
+
+    :return:
+        Result class instance.
+
+        - Reload status (bool) returned in result.status.
+        - Reload status returned from Revit in result.message property.
+        - Return family reference stored in result.result property on successful reload only
+
+        On exception
+
+        - Reload.status (bool) will be False
+        - Reload.message will contain the exception message
+
+    :rtype: :class:`.Result`
+    """
+
+    result = res.Result()
+    try:
+        # set up load / reload action to be run within a transaction
+        def action():
+            # set up return value for the load / reload
+            return_family = clr.Reference[rdb.Family]()
+            action_return_value = res.Result()
+            try:
+                reload_status = doc.LoadFamily(
+                    family_file_path,
+                    famLoadOpt.FamilyLoadOption(),  # overwrite parameter values etc
+                    return_family,
+                )
+                action_return_value.update_sep(
+                    reload_status,
+                    "Loaded family: " + family_file_path + " :: " + str(reload_status),
+                )
+                if reload_status:
+                    action_return_value.result.append(return_family.Value)
+            except Exception as e:
+                action_return_value.update_sep(
+                    False,
+                    "Failed to load family "
+                    + family_file_path
+                    + " with exception: "
+                    + str(e),
+                )
+            return action_return_value
+
+        transaction = rdb.Transaction(
+            doc,
+            "Loading Family: "
+            + str(fileIO.get_file_name_without_ext(family_file_path)),
+        )
+        dummy = rTran.in_transaction(transaction, action)
+        result.update(dummy)
+    except Exception as e:
+        result.update_sep(False, "Failed to load families with exception: " + str(e))
+    return result
+
+
+# ------------------------ filter functions -------------------------------------------------------------------------------------
+
+
+def get_family_symbols(doc, cats):
+    """
+    Filters all family symbols (Revit family types) of given built in categories from the Revit model.
+
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param cats: ICollection of Autodesk.Revit.DB.BuiltInCategory values.
+    :type cats: ICollection
+        :cats sample: cats = List[rdb.BuiltInCategory] ([rdb.BuiltInCategory.OST_Furniture, rdb.BuiltInCategory.OST_Parking])
 
-    :return: A filtered element collector containing ceiling types.
+    :return: A collector of Autodesk.Revit.DB.Element matching filter.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-
-    return  rdb.FilteredElementCollector(doc).OfClass(rdb.CeilingType)
+    """
 
-def BuildCeilingTypeDictionary(collector, dic):
-    '''
-    Returns the dictionary past in with keys and or values added retrieved from collector past in.
+    elements = []
+    try:
+        multi_cat_filter = rdb.ElementMulticategoryFilter(cats)
+        elements = (
+            rdb.FilteredElementCollector(doc)
+            .OfClass(rdb.FamilySymbol)
+            .WherePasses(multi_cat_filter)
+            .ToElements()
+        )
+        return elements
+    except Exception:
+        return elements
 
-    Keys are built in ceiling family type names.
 
-    TODO: Use more generic code.
+def get_family_instances_by_built_in_categories(doc, cats):
+    """
+    Filters all family instances of given built in categories from the Revit model.
 
-    :param collector: A filtered element collector containing ceiling types.
-    :type collector: Autodesk.Revit.DB.FilteredElementCollector
-    :param dic: A dictionary containing key: ceiling type family name, value: list of ids belonging to that type.
-    :type dic: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param cats: ICollection of Autodesk.Revit.DB.BuiltInCategory values:
+    :type cats: ICollection
+        :cats sample: cats = List[rdb.BuiltInCategory] ([rdb.BuiltInCategory.OST_Furniture, rdb.BuiltInCategory.OST_Parking])
 
-    :return: A dictionary containing key: built in ceiling type family name, value: list of ids belonging to that type.
-    :rtype: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
-    '''
+    :return: A collector of Autodesk.Revit.DB.Element matching filter.
+    :rtype: Autodesk.Revit.DB.FilteredElementCollector
+    """
 
-    for c in collector:
-        if(dic.has_key(c.FamilyName)):
-            if(c.Id not in dic[c.FamilyName]):
-                dic[c.FamilyName].append(c.Id)
-        else:
-            dic[c.FamilyName] = [c.Id]
-    return dic
+    elements = []
+    try:
+        multi_cat_filter = rdb.ElementMulticategoryFilter(cats)
+        elements = (
+            rdb.FilteredElementCollector(doc)
+            .OfClass(rdb.FamilyInstance)
+            .WherePasses(multi_cat_filter)
+            .ToElements()
+        )
+        return elements
+    except Exception:
+        return elements
 
-def SortCeilingTypesByFamilyName(doc):
-    '''
-    Returns a dictionary of all ceiling types in the model where key is the build in wall family name, values are ids of associated wall types.
 
-    TODO: Use more generic code.
+def get_family_instances_of_built_in_category(doc, builtin_cat):
+    """
+    Filters all family instances of a single given built in category from the Revit model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :param builtin_cat: single revit builtInCategory Enum value.
+    :type builtin_cat: Autodesk.Revit.DB.BuiltInCategory
 
-    :return: A dictionary containing key: built in ceiling type family name, value: list of ids belonging to that type.
-    :rtype: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
-    '''
+    :return: A collector of Autodesk.Revit.DB.FamilyInstance matching filter.
+    :rtype: Autodesk.Revit.DB.FilteredElementCollector
+    """
 
-    # get all ceiling Type Elements
-    wts = GetCeilingTypesByClass(doc)
-    # get all ceiling types including in place ceiling families
-    wts_two = GetAllCeilingTypesByCategory(doc)
-    usedWts = {}
-    usedWts = BuildCeilingTypeDictionary(wts, usedWts)
-    usedWts = BuildCeilingTypeDictionary(wts_two, usedWts)
-    return usedWts
+    filter = rdb.ElementCategoryFilter(builtin_cat)
+    col = (
+        rdb.FilteredElementCollector(doc)
+        .OfClass(rdb.FamilyInstance)
+        .WherePasses(filter)
+    )
+    return col
 
-# -------------------------------- none in place ceiling types -------------------------------------------------------
 
-def GetAllCeilingInstancesInModelByCategory(doc):
-    '''
-    Gets all ceiling elements placed in model. Ignores roof soffits.
+def get_all_loadable_families(doc):
+    """
+    Filters all families in revit model by whether it is not an InPlace family.
 
-    Filters by category.
+    Note: slow filter due to use of lambda and cast to list.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: A filtered element collector containing ceiling instances.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    :return: A list of families matching filter.
+    :rtype: list Autodesk.Revit.DB.Family
+    """
 
-    return rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Ceilings).WhereElementIsNotElementType()
+    collector = rdb.FilteredElementCollector(doc)
+    families = (
+        collector.OfClass(rdb.Family).Where(lambda e: (e.IsInPlace == False)).ToList()
+    )
+    return families
 
-def GetAllCeilingInstancesInModelByClass(doc):
-    '''
-    Gets all ceiling elements placed in model. Ignores in place families.
 
-    Filters by class.
+def get_all_loadable_family_ids_through_types(doc):
+    """
+    Get all loadable family ids in file.
 
-    :param doc: Current Revit model document.
+    :param doc: Current family document.
     :type doc: Autodesk.Revit.DB.Document
+    :return: list of family ids
+    :rtype: [Autodesk.Revit.DB.ElementId]
+    """
 
-    :return: A filtered element collector containing ceiling instances.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    family_ids = []
+    col = rdb.FilteredElementCollector(doc).OfClass(rdb.FamilySymbol)
+    # get families from symbols and filter out in place families
+    for fam_symbol in col:
+        if (
+            fam_symbol.Family.Id not in family_ids
+            and fam_symbol.Family.IsInPlace == False
+        ):
+            family_ids.append(fam_symbol.Family.Id)
+    return family_ids
 
-    return rdb.FilteredElementCollector(doc).OfClass(rdb.Ceiling).WhereElementIsNotElementType()
 
-def GetAllCeilingTypeIdsInModelByCategory(doc):
-    '''
-    Gets all ceiling element type ids available in model.
+def get_all_in_place_families(doc):
+    """
+    Filters all families in revit model by whether it is an InPlace family.
 
-    Filters by category.
+    Note: slow filter due to use of lambda and cast to list
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: A filtered element collector containing ceiling type ids.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    :return: A list of families matching filter.
+    :rtype: list Autodesk.Revit.DB.Family
+    """
 
-    ids = []
-    colCat = GetAllCeilingTypesByCategory(doc)
-    ids = com.GetIdsFromElementCollector(colCat)
-    return ids
+    collector = rdb.FilteredElementCollector(doc)
+    families = (
+        collector.OfClass(rdb.Family).Where(lambda e: (e.IsInPlace == True)).ToList()
+    )
+    return families
 
-def GetAllCeilingTypeIdsInModelByClass(doc):
-    '''
-    Gets all ceiling element type ids available in model.
 
-    Filters by class.
+def get_all_family_instances(doc):
+    """
+    Returns all family instances in document.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    
-    :return: A filtered element collector containing ceiling type ids.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
 
-    ids = []
-    colClass = GetCeilingTypesByClass(doc)
-    ids = com.GetIdsFromElementCollector(colClass)
-    return ids
+    :return: A collector with all family instances in document.
+    :rtype: Autodesk.Revit.DB.Collector
+    """
 
-def GetUsedCeilingTypeIds(doc):
-    '''
-    Gets all used ceiling type ids.
+    col = rdb.FilteredElementCollector(doc).OfClass(rdb.FamilyInstance)
+    return col
 
-    Filters by category.
-    Used: at least one instance of this type is placed in the model.
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+# --------------------------family data ----------------
 
-    :return: List of element ids representing used ceiling types.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
 
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllCeilingTypeIdsInModelByCategory, 1)
-    return ids
+def is_any_nested_family_instance_label_driven(doc):
+    """
+    Checks whether any family isntance in document is driven by the 'Label' property.
 
-def FamilyNoTypesInUse(famTypeIds,unUsedTypeIds):
-    '''
-    Compares two lists of ids. True if any id is not in unUsedTypeIds.
-
-    TODO: check for more generic list comparison and remove this function.
-
-    :param famTypeIds: List of family type ids to check.
-    :type famTypeIds: List of Autodesk.Revit.DB.ElementId
-    :param unUsedTypeIds: Reference list of ids.
-    :type unUsedTypeIds: List of Autodesk.Revit.DB.ElementId
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
 
-    :return: True if any id from famTypeIds is not in unUsedTypeIds.
+    :return: True if at least one instance is driven by label property. Othewise False
     :rtype: bool
-    '''
-
-    match = True
-    for famTypeId in famTypeIds:
-        if (famTypeId not in unUsedTypeIds):
-            match = False
-            break
-    return match
- 
-def GetUnusedNonInPlaceCeilingTypeIdsToPurge(doc):
-    '''
-    Gets all unused ceiling type id's.
-    
-    - Roof Soffit
-    - Compound Ceiling
-    - Basic Ceiling
+    """
 
-    This method can be used to safely delete unused ceiling types:
-    In the case that no ceiling instance using any of the types is placed this will return all but one type id since\
-        Revit requires at least one ceiling type definition to be in the model.
+    flag = False
+    fam_instances = get_all_family_instances(doc)
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+    for fam_instance in fam_instances:
+        # get the Label parameter value
+        p_value = rParaGet.get_built_in_parameter_value(
+            fam_instance,
+            rdb.BuiltInParameter.ELEM_TYPE_LABEL,
+            rParaGet.get_parameter_value_as_element_id,
+        )
+        # a valid Element Id means family instance is driven by Label
+        if p_value != rdb.ElementId.InvalidElementId:
+            flag = True
+            break
 
-    :return: List of element ids representing not used ceiling types.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    return flag
 
-    # get unused type ids
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllCeilingTypeIdsInModelByClass, 0)
-    # make sure there is at least on ceiling type per system family left in model
-    ceilingTypes = SortCeilingTypesByFamilyName(doc)
-    for key, value in ceilingTypes.items():
-        if(key in BUILTIN_CEILING_TYPE_FAMILY_NAMES):
-            if(FamilyNoTypesInUse(value,ids) == True):
-                # remove one type of this system family from unused list
-                ids.remove(value[0])
-    return ids
- 
-# -------------------------------- In place ceiling types -------------------------------------------------------
 
-def GetInPlaceCeilingFamilyInstances(doc):
-    '''
-    Gets all instances of in place families of category ceiling.
+def get_symbols_from_type(doc, type_ids):
+    """
+    Get all family types belonging to the same family as types past in.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :param type_ids: - list of element id's representing family symbols (family types)
+    :type type_ids: list of Autodesk.Revit.DB.ElementId
 
-    :return: A filtered element collector containing in place ceiling instances.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-    
-    filter = rdb.ElementCategoryFilter(rdb.BuiltInCategory.OST_Ceilings)
-    return rdb.FilteredElementCollector(doc).OfClass(rdb.FamilyInstance).WherePasses(filter)
+    :return: dictionary:
+        where key is the family id as Autodesk.Revit.DB.ElementId
+        value is a list of all symbol(family type) ids as Autodesk.Revit.DB.ElementId belonging to the family
+    :rtype: dic {Autodesk.Revit.DB.ElementId: list[Autodesk.Revit.DB.ElementId]}
+    """
+
+    families = {}
+    for t_id in type_ids:
+        # get family element
+        type_el = doc.GetElement(t_id)
+        fam_el = type_el.Family
+        # check whether family was already processed
+        if fam_el.Id not in families:
+            # get all available family types
+            s_ids = fam_el.GetFamilySymbolIds().ToList()
+            families[fam_el.Id] = s_ids
+    return families
 
-def GetAllInPlaceCeilingTypeIdsInModel(doc):
-    '''
-    Gets all type ids off all available in place families of category ceiling.
+
+def get_family_instances_by_symbol_type_id(doc, type_id):
+    """
+    Filters all family instances of a single given family symbol (type).
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :param Autodesk.Revit.DB.ElementId type_id: The symbol (type) id
 
-    :return: List of element ids representing in place ceiling types.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    :return: A collector of Autodesk.Revit.DB.FamilyInstance matching filter.
+    :rtype: Autodesk.Revit.DB.FilteredElementCollector
+    """
 
-    ids = rFam.GetAllInPlaceTypeIdsInModelOfCategory(doc, rdb.BuiltInCategory.OST_Ceilings)
-    return ids
+    pvp_symbol = rdb.ParameterValueProvider(
+        rdb.ElementId(rdb.BuiltInParameter.SYMBOL_ID_PARAM)
+    )
+    equals = rdb.FilterNumericEquals()
+    id_filter = rdb.FilterElementIdRule(pvp_symbol, equals, type_id)
+    element_filter = rdb.ElementParameterFilter(id_filter)
+    collector = rdb.FilteredElementCollector(doc).WherePasses(element_filter)
+    return collector
 
-def GetUsedInPlaceCeilingTypeIds(doc):
-    '''
-    Gets all used in place ceiling type ids in the model.
 
-    Used: at least one instance of this type is placed in the model.
+def get_all_in_place_type_ids_in_model_of_category(doc, fam_built_in_category):
+    """
+    Filters family symbol (type) ids off all available in place families of single given built in category.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :param fam_built_in_category: built in revit category
+    :type fam_built_in_category: Autodesk.Revit.DB.BuiltInCategory
 
-    :return: List of element ids representing used in place ceiling types.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    :return: A list of Element Ids representing the family symbols matching filter.
+    :rtype: list Autodesk.Revit.DB.ElementId
+    """
 
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllInPlaceCeilingTypeIdsInModel, 1)
+    # filter model for family symbols of given built in category
+    filter = rdb.ElementCategoryFilter(fam_built_in_category)
+    col = (
+        rdb.FilteredElementCollector(doc).OfClass(rdb.FamilySymbol).WherePasses(filter)
+    )
+    ids = []
+    for c in col:
+        fam = c.Family
+        # check if this an in place or loaded family!
+        if fam.IsInPlace == True:
+            ids.append(c.Id)
     return ids
 
-def GetUnusedInPlaceCeilingTypeIds(doc):
-    '''
-    Gets all unused in place ceiling type ids in the model.
 
-    Unused: Not one instance of this type is placed in the model.
+# --------------------------family purge  ----------------
+
+
+def get_family_symbols_ids(doc, cats, exclude_shared_fam=True):
+    """
+    Filters family symbols belonging to list of built in categories past in.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :param ICollection cats: ICollection of Autodesk.Revit.DB.BuiltInCategory values.
+    :type cats: cats = List[rdb.BuiltInCategory] ([rdb.BuiltInCategory.OST_Furniture, rdb.BuiltInCategory.OST_Parking])
 
-    :return: List of element ids representing unused in place ceiling types.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    :return: A list of Element Ids representing the family symbols matching filter.
+    :rtype: list Autodesk.Revit.DB.ElementId
+    """
 
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllInPlaceCeilingTypeIdsInModel, 0)
-    return ids
-
-def GetUnusedInPlaceCeilingIdsForPurge(doc):
-    '''
-    Gets symbol(type) ids and family ids (when no type is in use) of in place ceiling families which can be safely deleted from the model.
+    ids = []
+    try:
+        multi_cat_filter = rdb.ElementMulticategoryFilter(cats)
+        elements = (
+            rdb.FilteredElementCollector(doc)
+            .OfClass(rdb.FamilySymbol)
+            .WherePasses(multi_cat_filter)
+        )
+        for el in elements:
+            # check if shared families are to be excluded from return list
+            if exclude_shared_fam:
+                fam = el.Family
+                p_value = rParaGet.get_built_in_parameter_value(
+                    fam, rdb.BuiltInParameter.FAMILY_SHARED
+                )
+                if p_value != None:
+                    if p_value == "No" and el.Id not in ids:
+                        ids.append(el.Id)
+                else:
+                    # some revit families cant be of type shared...()
+                    ids.append(el.Id)
+            else:
+                ids.append(el.Id)
+        return ids
+    except Exception:
+        return ids
+
+
+def get_all_non_shared_family_symbol_ids(doc):
+    """
+    Filters family symbols (types) belonging to hard coded categories lists (catsLoadableThreeD, catsLoadableTags)
 
-    This method can be used to safely delete unused in place ceiling types. There is no requirement by Revit to have at least one\
-        in place ceiling definition in the model.
-    
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: List of element ids representing unused in place ceiling types and families.
+    :return: A list of Element Ids representing the family symbols matching filter.
     :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
-    ids = rFam.GetUnusedInPlaceIdsForPurge(doc, GetUnusedInPlaceCeilingTypeIds)
+    ids = []
+    all_loadable_three_d_type_ids = get_family_symbols_ids(doc, CATEGORIES_LOADABLE_3D)
+    all_loadable_tags_type_ids = get_family_symbols_ids(doc, CATEGORIES_LOADABLE_TAGS)
+    ids = all_loadable_three_d_type_ids + all_loadable_tags_type_ids
     return ids
-
-# -------------------------------- ceiling geometry -------------------------------------------------------
-
-def Get2DPointsFromRevitCeiling(ceiling):
-    '''
-    Returns a list of lists of points representing the flattened(2D geometry) of the ceiling
-    List of Lists because a ceiling can be made up of multiple sketches. Each nested list represents one ceiling sketch.
-    Does not work with in place ceilings
-
-    :param ceiling: A revit ceiling instance.
-    :type ceiling: Autodesk.Revit.DB.Ceiling
-
-    :return: A list of data geometry instances.
-    :rtype: list of :class:`.DataGeometry`
-    '''
-
-    allCeilingPoints = []
-    # get geometry from ceiling
-    opt = rdb.Options()
-    fr1_geom = ceiling.get_Geometry(opt)
-    solids = []
-    # check geometry for Solid elements
-    # todo check for FamilyInstance geometry ( in place families!)
-    for item in fr1_geom:
-        if(type(item) is rdb.Solid):
-            solids.append(item)
-   
-    # process solids to points 
-    # in place families may have more then one solid
-    for s in solids:
-        pointPerCeilings = rGeo.ConvertSolidToFlattened2DPoints(s)
-        if(len(pointPerCeilings) > 0):
-            for pLists in pointPerCeilings:
-                allCeilingPoints.append(pLists)
-    return allCeilingPoints
-
-def Get2DPointsFromRevitCeilingsInModel(doc):
-    '''
-    Returns a list of lists of points representing the flattened(2D geometry) of the ceiling
-    List of Lists because a ceiling can be made up of multiple sketches. Each nested list represents one ceiling sketch.
-    Does not work with in place ceilings
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of data geometry instances.
-    :rtype: list of :class:`.DataGeometry`
-    '''
-
-    ceilingInstances =  GetAllCeilingInstancesInModelByCategory(doc)
-    allCeilingPoints = []
-    for cI in ceilingInstances:
-       ceilingPoints = Get2DPointsFromRevitCeiling(cI)
-       if(len(ceilingPoints) > 0 ):
-           allCeilingPoints.append (ceilingPoints)
-    return allCeilingPoints
-
-# -------------------------------- ceiling data -------------------------------------------------------
-
-def GetAllCeilingData(doc):
-    '''
-    Gets a list of ceiling data objects for each ceiling element in the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of data ceiling instances.
-    :rtype: list of :class:`.DataCeiling`
-    '''
-
-    allCeilingData = []
-    ceilings = GetAllCeilingInstancesInModelByCategory(doc)
-    for ceiling in ceilings:
-        cd = PopulateDataCeilingObject(doc, ceiling)
-        if(cd is not None):
-            allCeilingData.append(cd)
-    return allCeilingData
-
-
-def PopulateDataCeilingObject(doc, revitCeiling):
-    '''
-    Returns a custom ceiling data objects populated with some data from the revit model ceiling past in.
-
-    - ceiling id
-    - ceiling type name
-    - ceiling mark
-    - ceiling type mark
-    - ceiling level name
-    - ceiling level id
-    - ceiling offset from level
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    :param revitCeiling: A revit ceiling instance.
-    :type revitCeiling: Autodesk.Revit.DB.Ceiling
-
-    :return: A data ceiling object instance.
-    :rtype: :class:`.DataCeiling`
-    '''
-
-    # set up data class object
-    dataC = dCeiling.DataCeiling() 
-    # get ceiling geometry (boundary points)
-    revitGeometryPointGroups = Get2DPointsFromRevitCeiling(revitCeiling)
-    if(len(revitGeometryPointGroups) > 0):
-        ceilingPointGroupsAsDoubles = []
-        for allCeilingPointGroups in revitGeometryPointGroups:
-            dataGeoConverted = rGeo.ConvertXYZInDataGeometry(doc, allCeilingPointGroups)
-            ceilingPointGroupsAsDoubles.append(dataGeoConverted)
-        dataC.geometry = ceilingPointGroupsAsDoubles
-        # get design set data
-        design_set_data = rDesignO.GetDesignSetOptionInfo(doc, revitCeiling)
-        dataC.designSetAndOption.designOptionName = design_set_data['designOptionName']
-        dataC.designSetAndOption.designSetName = design_set_data['designSetName']
-        dataC.designSetAndOption.isPrimary = design_set_data['isPrimary']
-        
-        # get type properties
-        dataC.typeProperties.typeId = revitCeiling.GetTypeId().IntegerValue
-        dataC.typeProperties.typeName = rdb.Element.Name.GetValue(revitCeiling).encode('utf-8')
-        ceilingType = doc.GetElement(revitCeiling.GetTypeId())
-        
-        # custom parameter value getters
-        value_getter = {
-            rdb.StorageType.Double : rParaGet.getter_double_as_double_converted_to_millimeter, 
-            rdb.StorageType.Integer : rParaGet.getter_int_as_int, 
-            rdb.StorageType.String : rParaGet.getter_string_as_UTF8_string, # encode ass utf 8 just in case
-            rdb.StorageType.ElementId : rParaGet.getter_element_id_as_element_int # needs to be an integer for JSON encoding
-        }
-        dataC.typeProperties.properties = rParaGet.get_all_parameters_and_values_wit_custom_getters(ceilingType, value_getter)
-        
-        # get instance properties
-        dataC.instanceProperties.instanceId = revitCeiling.Id.IntegerValue
-        dataC.instanceProperties.properties = rParaGet.get_all_parameters_and_values_wit_custom_getters(revitCeiling, value_getter)
-        
-        # get level properties
-        dataC.level.levelName = rdb.Element.Name.GetValue(doc.GetElement(revitCeiling.LevelId)).encode('utf-8')
-        dataC.level.levelId = revitCeiling.LevelId.IntegerValue
-        dataC.level.offsetFromLevel = rParaGet.get_built_in_parameter_value(revitCeiling, rdb.BuiltInParameter.CEILING_HEIGHTABOVELEVEL_PARAM)   # offset from level
-        
-        # get the model name
-        if(doc.IsDetached):
-            dataC.revitModel.modelName = 'Detached Model'
-        else:
-            dataC.revitModel.modelName = doc.Title
-        
-        # get phasing information
-        dataC.phasing.phaseCreated = rPhase.GetPhaseNameById(doc, rParaGet.get_built_in_parameter_value(revitCeiling, rdb.BuiltInParameter.PHASE_CREATED, rParaGet.get_parameter_value_as_element_id)).encode('utf-8')
-        dataC.phasing.phaseDemolished = rPhase.GetPhaseNameById(doc, rParaGet.get_built_in_parameter_value(revitCeiling, rdb.BuiltInParameter.PHASE_DEMOLISHED, rParaGet.get_parameter_value_as_element_id)).encode('utf-8')
-
-        return dataC
-    else:
-        return None
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitCurtainWallElements.py` & `DuHast-0.0.7/src/duHast/Revit/Stairs/purge_unused_stair_types.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Revit curtain walls helper functions.
+This module contains a number of helper functions relating to purging Revit stairs and stair sub element types.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -22,359 +22,399 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-import clr
-import System
-from System.Collections.Generic import List
-
-
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.APISamples import RevitFamilyUtils as rFam
-
-# import Autodesk
-import Autodesk.Revit.DB as rdb
-
-# -------------------------------------------- common variables --------------------
-#: header used in reports
-REPORT_CURTAINWALL_ELEMENTS_HEADER = ['HOSTFILE', 'CURTAINWALL_ELEMENT_TYPEID', 'ReplaceMeTYPENAME']
-
-#: Built in family name for empty system panel
-CURTAINWALL_PANEL_EMPTY_FAMILY_NAME = 'Empty System Panel'
-#: Built in family name for empty system panel
-CURTAINWALL_PANEL_SYSTEM_FAMILY_NAME = 'Empty System Panel'
-#: Built in family name for V-shaped mullion
-CURTAINWALL_MULLION_V_FAMILY_NAME = 'V Corner Mullion'
-#: Built in family name for circular mullion
-CURTAINWALL_MULLION_CIRCULAR_FAMILY_NAME = 'Circular Mullion'
-#: Built in family name for quad corner mullion
-CURTAINWALL_MULLION_QUAD_FAMILY_NAME = 'Quad Corner Mullion'
-#: Built in family name for L-shaped corner mullion
-CURTAINWALL_MULLION_L_FAMILY_NAME = 'L Corner Mullion'
-#: Built in family name for rectangular mullion
-CURTAINWALL_MULLION_RECT_FAMILY_NAME = 'Rectangular Mullion'
-#: Built in family name for trapezoid corner mullion
-CURTAINWALL_MULLION_TRAPEZ_FAMILY_NAME = 'Trapezoid Corner Mullion'
-
-BUILTIN_TYPE_FAMILY_NAMES = [
-    CURTAINWALL_PANEL_EMPTY_FAMILY_NAME,
-    CURTAINWALL_PANEL_SYSTEM_FAMILY_NAME,
-    CURTAINWALL_MULLION_V_FAMILY_NAME,
-    CURTAINWALL_MULLION_CIRCULAR_FAMILY_NAME,
-    CURTAINWALL_MULLION_QUAD_FAMILY_NAME,
-    CURTAINWALL_MULLION_L_FAMILY_NAME,
-    CURTAINWALL_MULLION_RECT_FAMILY_NAME,
-    CURTAINWALL_MULLION_TRAPEZ_FAMILY_NAME
+from duHast.Revit.Family import purge_unused_family_types as rFamPurge
+from duHast.Revit.Common import purge_utils as rPurgeUtils
+from duHast.Revit.Common import parameter_get_utils as rParaGet
+from duHast.Revit.Stairs import stairs as rStair
+from duHast.Revit.Stairs.Utility import stairs_type_sorting as rStairSort
+from duHast.Revit.Stairs import cut_marks as rStairCut
+from duHast.Revit.Stairs import landings as rStairLanding
+from duHast.Revit.Stairs import path as rStairPath
+from duHast.Revit.Stairs import runs as rStairRun
+from duHast.Revit.Stairs import stringers_carriages as rStairStringersAndCarriages
+
+#: Built in stair family name for basic stairs
+BASIC_STAIR_FAMILY_NAME = "Stair"
+
+#: Built in stair family name for assembled stairs
+ASSEMBLED_STAIR_FAMILY_NAME = "Assembled Stair"
+
+#: Built in stair family name for precast stairs
+PRECAST_STAIR_FAMILY_NAME = "Precast Stair"
+
+#: Built in stair family name for cast in place stairs
+CAST_IN_PLACE_STAIR_FAMILY_NAME = "Cast-In-Place Stair"
+
+#: List of all Built in stair family names
+BUILTIN_STAIR_TYPE_FAMILY_NAMES = [
+    BASIC_STAIR_FAMILY_NAME,
+    ASSEMBLED_STAIR_FAMILY_NAME,
+    PRECAST_STAIR_FAMILY_NAME,
+    CAST_IN_PLACE_STAIR_FAMILY_NAME,
 ]
 
-#: category filter for all element filters by category
-CURTAINWALL_ELEMENTS_CATEGORY_FILTER = List[rdb.BuiltInCategory] ([
-        rdb.BuiltInCategory.OST_CurtainWallPanels,
-        rdb.BuiltInCategory.OST_CurtainWallMullions
-    ])
-
-
-# --------------------------------------------- utility functions ------------------
-
-def GetAllCurtainWallElementTypesByCategory(doc):
-    '''
-    Gets a filtered element collector of all curtain wall element types in the model:
-
-    Filters by multiple categories.
-
-    - curtain wall panels
-    - curtain wall mullions
-    - in place family symbols!
-    
 
+def get_used_stair_type_ids(doc):
+    """
+    Gets all used in Stair type ids.
+    Used: at least one instance of this type is placed in the model.
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :return: List of element ids representing stair types.
+    :rtype: list of Autodesk.Revit.DB.ElementId
+    """
 
-    :return: A filtered element collector containing curtain wall element types.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-
-    multiCatFilter = rdb.ElementMulticategoryFilter(CURTAINWALL_ELEMENTS_CATEGORY_FILTER )
-    collector = rdb.FilteredElementCollector(doc).WherePasses(multiCatFilter).WhereElementIsElementType()
-    return collector
-
-def BuildCurtainWallElementTypeDictionary(collector, dic):
-    '''
-    Returns the dictionary past in with keys and or values added retrieved from collector past in.
-
-    Keys are built in curtain wall element type names.
-    TODO: this code repeats across a number of modules. Use generic instead!
+    ids = rPurgeUtils.get_used_unused_type_ids(
+        doc, rStair.get_all_stair_type_ids_by_category, 1
+    )
+    return ids
 
-    :param collector: A filtered element collector containing curtain wall element types.
-    :type collector: Autodesk.Revit.DB.FilteredElementCollector
-    :param dic: A dictionary containing key: curtain wall element type name, value: list of ids belonging to that type.
-    :type dic: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
 
-    :return: A dictionary containing key: built in curtain wall element type  name, value: list of ids belonging to that type.
-    :rtype: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
-    '''
+def family_no_types_in_use(fam_type_ids, un_used_type_ids):
+    """
+    Compares two lists of ids. True if any id is not in un_used_type_ids.
+    TODO: check for more generic list comparison and remove this function.
+    :param fam_type_ids: List of family type ids to check.
+    :type fam_type_ids: List of Autodesk.Revit.DB.ElementId
+    :param un_used_type_ids: Reference list of ids.
+    :type un_used_type_ids: List of Autodesk.Revit.DB.ElementId
+    :return: True if any id from amTypeIds is not in un_used_type_ids.
+    :rtype: bool
+    """
 
-    for c in collector:
-        if(dic.has_key(c.FamilyName)):
-            if(c.Id not in dic[c.FamilyName]):
-                dic[c.FamilyName].append(c.Id)
-        else:
-            dic[c.FamilyName] = [c.Id]
-    return dic
+    match = True
+    for fam_type_id in fam_type_ids:
+        if fam_type_id not in un_used_type_ids:
+            match = False
+            break
+    return match
 
-def SortCurtainWallElementTypesByFamilyName(doc):
-    '''
-    Returns a dictionary containing all curtain wall element types in the model.
 
-    Key values are as per BUILTIN_TYPE_FAMILY_NAMES.
-    TODO: This code repeats across a number of modules. Use generic instead!
-    
+# -------------------------------- none in place Stair types purge -------------------------------------------------------
+def get_unused_non_in_place_stair_type_ids_to_purge(doc):
+    """
+    Gets all unused Stair type ids for.
+    Included are:
+    - Stair Soffit
+    - Compound Stair
+    - Basic Stair
+    It will therefore not return any in place family types.
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :return: List of element ids representing unused stair types.
+    :rtype: list of Autodesk.Revit.DB.ElementId
+    """
 
-    :return: A dictionary containing key: curtain wall element type family name, value: list of ids.
-    :rtype: dic { str: [Autodesk.Revit.DB.ElementId]}
-    '''
-
-    # get all CurtainWallElement types including in place wall families
-    wts_two = GetAllCurtainWallElementTypesByCategory(doc)
-    usedWts = {}
-    usedWts = BuildCurtainWallElementTypeDictionary(wts_two, usedWts)
-    return usedWts
-
-# -------------------------------- none in place or loadable Curtain Wall Element types -------------------------------------------------------
-
-def GetCurtainWallElementInstancesInModelByCategory(doc):
-    '''
-    Gets all CurtainWallElement elements instances placed in model.
-
-    Includes:
-
-    - curtain wall panels
-    - curtain wall mullions
+    # get unused type ids
+    ids = rPurgeUtils.get_used_unused_type_ids(
+        doc, rStair.get_all_stair_type_ids_by_class, 0
+    )
+    # make sure there is at least on Stair type per system family left in model
+    stair_types = rStairSort.sort_stair_types_by_family_name(doc)
+    for key, value in stair_types.items():
+        if key in BUILTIN_STAIR_TYPE_FAMILY_NAMES:
+            if family_no_types_in_use(value, ids) == True:
+                # remove one type of this system family from unused list
+                ids.remove(value[0])
+    return ids
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
 
-    :return: A filtered element collector containing curtain wall element types.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-    
-    multiCatFilter = rdb.ElementMulticategoryFilter(CURTAINWALL_ELEMENTS_CATEGORY_FILTER )
-    return rdb.FilteredElementCollector(doc).WherePasses(multiCatFilter).WhereElementIsNotElementType()
+# --------------------------------utility functions to get unused sub types ----------------------
 
-def GetAllCurtainWallElementTypeIdsInModelByCategory(doc):
-    '''
-    Gets all Curtain Wall Element element type ids available in model.
 
-    Includes:
+def get_used_sub_type_ids_from_stair_type(doc, stair_type_id, paras):
+    """
+    Gets the id of types making up a stair.
+    These could be stair landing types, stringer and carriage types etc.
+    Types returned depend on parameter definitions past in.
+    Refer to:
+    - STAIR_LANDING_TYPE_PARAS,
+    - STAIR_CUTMARK_TYPE_PARAS,
+    - STAIR_SUPPORT_TYPE_PARAS
 
-    - curtain wall panels
-    - curtain wall mullions
-    
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids representing curtain wall element types.
+    :param stair_type_id: An element id representing a stair type.
+    :type stair_type_id: Autodesk.Revit.DB.ElementId
+    :param paras: Parameters containing a type making up a stair.
+    :type paras: list Autodesk.Revit.DB.BuiltInParameterDefinition
+    :return: List of element ids representing stair types.
     :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     ids = []
-    colCat = GetAllCurtainWallElementTypesByCategory(doc)
-    ids = com.GetIdsFromElementCollector (colCat)
+    stair_type = doc.GetElement(stair_type_id)
+    for p_def in paras:
+        p_value = rParaGet.get_built_in_parameter_value(stair_type, p_def)
+        if p_value != None and p_value not in ids:
+            ids.append(p_value)
     return ids
 
-def GetAllCurtainWallElementTypesByCategoryExclInPlace(doc):
-    '''
-    Gets all Curtain Wall Element element type available in model. Excludes in place family symbols.
 
-    Includes:
-
-    - curtain wall panels
-    - curtain wall mullions
-    
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of curtain wall element types.
-    :rtype: list of Autodesk.Revit.DB.ElementType
-    '''
+def get_all_similar_type_ids(doc, ids):
+    """
+    Gets all unique ids of similar types of element ids passed in.
+    TODO: check for similar function elsewhere!
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param ids: list of type ids to be added to.
+    :type ids: list of Autodesk.Revit.ElementIds
+    :return: List of unique ids of similar types.
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    sim_ids = []
+    for id in ids:
+        el = doc.GetElement(id)
+        sim_types = el.GetSimilarTypes()
+        for st in sim_types:
+            if st not in sim_ids:
+                sim_ids.append(st)
+    return sim_ids
+
+
+def build_system_family_dictionary(doc, ids):
+    """
+    Returns dictionary where key is the system family name and values list of available type ids of that system family.
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param ids: List of system family ids.
+    :type ids: list of Autodesk.Revit.ElementIds
+    :return: Dictionary of unique ids of similar types.
+    :rtype: dictionary {str: list of Autodesk.Revit.ElementIds }
+    """
+
+    dic = {}
+    for id in ids:
+        el = doc.GetElement(id)
+        if dic.has_key(el.FamilyName):
+            dic[el.FamilyName].append(id)
+        else:
+            dic[el.FamilyName] = [id]
+    return dic
 
-    collector = GetAllCurtainWallElementTypesByCategory(doc)
-    elements=[]
-    for c in collector:
-        if(c.GetType() != rdb.FamilySymbol):
-            elements.append(c)
-    return elements
 
-def GetAllCurtainWallElementTypeIdsByCategoryExclSymbols(doc):
-    '''
-    Gets all Curtain Wall Element element type ids available in model. Excludes in place family symbols.
+def check_system_families(doc, ids, leave_one_behind):
+    """
+    Check whether a list of ids of system family is the entire list of types available in the model. If so it will remove one\
+    type id per system family to allow safe purging.
+    Revit requires at least one type definition per system family to be in the model.
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param ids: List of ids to check
+    :type ids: list of Autodesk.Revit.ElementIds
+    :param leave_one_behind: True: at least one type will be omitted from list.
+    :type leave_one_behind: bool
+    :return: List of unique ids of similar types.
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    dic_to_check = build_system_family_dictionary(doc, ids)
+    similar_ids = get_all_similar_type_ids(doc, ids)
+    dic_reference = build_system_family_dictionary(doc, similar_ids)
+    ids = []
+    for key, value in dic_to_check.items():
+        if dic_reference.has_key(key):
+            if len(dic_reference[key]) == len(dic_to_check[key]) and leave_one_behind:
+                # need to leave one behind...
+                if len(dic_to_check[key]) > 0:
+                    dic_to_check[key].pop(0)
+                    ids = ids + dic_to_check[key]
+            else:
+                ids = ids + dic_to_check[key]
+        else:
+            ids = ids + dic_to_check[key]
+    return ids
 
-    Includes:
 
-    - curtain wall panels
-    - curtain wall mullions
-    
+def get_used_sub_types(doc, available_ids_getter, paras, leave_one_behind=True):
+    """
+    Returns a list of type ids which are not used in any stair types.
+    Type ids are provided via an id getter function
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :param available_ids_getter: function returning available type ids
+    :type available_ids_getter: func(doc)
+    :param paras: list of built in parameters attached to a stair type for given sub types (stringers, path, run, landing)
+    :type paras: list of Autodesk.Revit.DB.BuiltInParameter
+    :param leave_one_behind: _description_, defaults to True
+    :type leave_one_behind: bool, optional
+    :return: List of element ids
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
 
-    :return: List of element ids representing curtain wall element types.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    collector = GetAllCurtainWallElementTypesByCategory(doc)
-    ids=[]
-    for c in collector:
-        if(c.GetType() != rdb.FamilySymbol):
-            ids.append(c.Id)
+    ids = []
+    # get all available type ids and then check against all Stair type ids
+    ids_available = available_ids_getter(doc)
+    all_used_stair_type_ids = rStair.get_all_stair_type_ids_by_category(doc)
+    ids_used_types = []
+    for used in all_used_stair_type_ids:
+        ids_used = get_used_sub_type_ids_from_stair_type(doc, used, paras)
+        for id in ids_used:
+            if id not in ids_used_types:
+                ids_used_types.append(id)
+    for id_available in ids_available:
+        if id_available not in ids_used_types:
+            ids.append(id_available)
+    # need to check that we are not trying to delete last type of a system family....
+    ids = check_system_families(doc, ids, leave_one_behind)
     return ids
 
-def GetUsedCurtainWallElementTypeIds(doc):
-    '''
-    Gets all used Curtain Wall Element element type ids available in model.
-
-    Used: at least one instance of this type is placed in the model.
-    Includes:
 
-    - curtain wall panels
-    - curtain wall mullions
-    
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+# --------------------------------- purging subtypes ------------------------------------------------
 
-    :return: List of element ids representing curtain wall element types.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
 
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllCurtainWallElementTypeIdsInModelByCategory, 1)
+def get_unused_stair_path_type_ids_to_purge(doc):
+    """
+    Gets all unused Stair path ids to purge, will omit on path type id per system family if none are used.
+    This method can be used to safely delete unused stair path types. In the case that no stair\
+        path instance using any of the types is placed, this will return all but one type id since\
+        Revit requires at least one stair path type definition to be in the model.
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :return: List of element ids 
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    ids_used = []
+    available_types = rStairPath.get_stair_path_types_ids_by_class(doc)
+    col = rStairPath.get_all_stair_path_instances(doc)
+    for c in col:
+        if c.GetTypeId() not in ids_used:
+            ids_used.append(c.GetTypeId())
+    ids = []
+    for at in available_types:
+        if at not in ids_used:
+            ids.append(at)
+    ids = check_system_families(doc, ids, True)
     return ids
 
-def FamilyNoTypesInUse(famTypeIds,unUsedTypeIds):
-    '''
-    Compares two lists of ids. True if any id is not in unUsedTypeIds.
-
-    TODO: check for more generic list comparison and remove this function.
-
-    :param famTypeIds: List of family type ids to check.
-    :type famTypeIds: List of Autodesk.Revit.DB.ElementId
-    :param unUsedTypeIds: Reference list of ids.
-    :type unUsedTypeIds: List of Autodesk.Revit.DB.ElementId
 
-    :return: True if any id from famTypeIds is not in unUsedTypeIds.
-    :rtype: bool
-    '''
+def get_unused_stair_landing_type_ids_to_purge(doc):
+    """
+    Gets all unused Stair landing type ids.
+    This method can be used to safely delete unused stair landing types. In the case that no stair\
+        landing instance using any of the types is placed, this will return all but one type id since\
+        Revit requires at least one stair landing type definition to be in the model.
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :return: List of element ids 
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    ids = get_used_sub_types(
+        doc,
+        rStairLanding.get_stair_landing_types_ids_by_class,
+        rStairLanding.STAIR_LANDING_TYPE_PARAS,
+    )
+    return ids
 
-    match = True
-    for famTypeId in famTypeIds:
-        if (famTypeId not in unUsedTypeIds):
-            match = False
-            break
-    return match
- 
-def GetUnusedNonSymbolCurtainWallElementTypeIdsToPurge(doc):
-    '''
-    Gets all unused Curtain Wall Element element type ids which can be safely deleted from the model.
 
-    This method can be used to safely delete unused in curtain wall element types. There is no requirement by Revit to have at least one\
-        curtain wall element definition in the model.
-    
-    
+def get_unused_stair_run_type_ids_to_purge(doc):
+    """
+    Gets all unused Stair run type ids.
+    This method can be used to safely delete unused stair run types. In the case that no stair\
+        run instance using any of the types is placed, this will return all but one type id since\
+        Revit requires at least one stair run type definition to be in the model.
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids representing unused in curtain wall element types.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    # get unused type ids
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllCurtainWallElementTypeIdsByCategoryExclSymbols, 0)
-    # unlike other element types, here I do NOT make sure there is at least on curtain wall element type per system family left in model!!
+    :return: List of element ids 
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    ids = get_used_sub_types(
+        doc, rStairRun.get_stair_run_types_ids_by_class, rStairRun.STAIR_RUN_TYPE_PARAS
+    )
     return ids
 
 
-# -------------------------------- loadable Curtain Wall Element types -------------------------------------------------------
-
-def GetAllCurtainWallNonSharedSymbolIdsByCategory(doc):
-    '''
-    Gets a list of all loadable, non shared, family symbols (types) in the model of categories:
-
-    - curtain wall panels
-    - curtain wall mullions
-    
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+def get_unused_stair_cut_mark_type_ids_to_purge(doc):
+    """
+    Gets all unused Stair cut mark type ids.
+    This method can be used to safely delete unused stair cut mark types. In the case that no stair\
+        cut mark instance using any of the types is placed, this will return all but one type id since\
+        Revit requires at least one stair cut mark type definition to be in the model.
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :return: List of element ids 
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    ids = get_used_sub_types(
+        doc,
+        rStairCut.get_stair_cut_mark_types_ids_by_class,
+        rStairCut.STAIR_CUT_MARK_TYPE_PARAS,
+    )
+    return ids
 
-    :return: List of element ids representing curtain wall family symbols.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
 
-    ids = []
-    multiCatFilter = rdb.ElementMulticategoryFilter(CURTAINWALL_ELEMENTS_CATEGORY_FILTER )
-    collector = rdb.FilteredElementCollector(doc).WherePasses(multiCatFilter).WhereElementIsElementType()
-    for c in collector:
-        if(c.GetType() == rdb.FamilySymbol):
-            fam = c.Family
-            pValue = rParaGet.get_built_in_parameter_value(fam, rdb.BuiltInParameter.FAMILY_SHARED)
-            if(pValue != None and  pValue == 'No' and c.Id not in ids):
-                ids.append(c.Id)
+def get_unused_stair_stringers_carriage_type_ids_to_purge(doc):
+    """
+    Gets all unused Stair stringer / carriage type ids.
+    This method can be used to safely delete unused stair stringer / carriage types. In the case that no stair\
+        string carriage instance using any of the types is placed, this will return all but one type id since\
+        Revit requires at least one stringer carriage type definition to be in the model.
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :return: List of element ids 
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    ids = get_used_sub_types(
+        doc,
+        rStairStringersAndCarriages.get_all_stair_stringers_carriage_type_ids_by_category,
+        rStairStringersAndCarriages.STAIR_SUPPORT_TYPE_PARAS,
+    )
     return ids
 
-def GetUsedCurtainWallSymbolIds(doc):
-    '''
-    Gets a list of all used loadable, non shared, family symbols (types) in the model of categories:
 
-    - curtain wall panels
-    - curtain wall mullions
+# -------------------------------- In place Stair types -------------------------------------------------------
+
 
-    Used: at least one family instance of this symbol (type) is placed in the model.
-    
+def get_used_in_place_stair_type_ids(doc):
+    """
+    Gets all used in place stair type ids.
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :return: List of element ids
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
 
-    :return: List of element ids representing curtain wall family symbols.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllCurtainWallNonSharedSymbolIdsByCategory, 1)
+    ids = rPurgeUtils.get_used_unused_type_ids(
+        doc, rStair.get_all_in_place_stair_type_ids, 1
+    )
     return ids
 
-def GetUnusedCurtainWallSymbolIds(doc):
-    '''
-    Gets a list of all used loadable, non shared, family symbols (types) in the model of categories:
-
-    - curtain wall panels
-    - curtain wall mullions
 
-    Unused: Not one family instance of this symbol (type) is placed in the model.
-    
+def get_unused_in_place_stair_type_ids(doc):
+    """
+    Gets all unused in place stair type ids.
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids representing curtain wall family symbols.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllCurtainWallNonSharedSymbolIdsByCategory, 0)
+    :return: List of element ids
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    ids = rPurgeUtils.get_used_unused_type_ids(
+        doc, rStair.get_all_in_place_stair_type_ids, 0
+    )
     return ids
 
-# doc   current document
-def GetUnusedICurtainWallSymbolIdsForPurge(doc):
-    '''
-    Gets symbol(type) ids and family ids (when no type is in use) of curtain wall element families which can be safely deleted from the model.
 
-    This method can be used to safely delete unused curtain wall element types. There is no requirement by Revit to have at least one\
-        in place wall definition in the model.
-    
+def get_unused_in_place_stair_type_ids_for_purge(doc):
+    """
+    Gets symbol (type) ids and family ids (when no type is in use) of in place Stair families which can be purged.
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids representing unused curtain wall element symbols (types) and families.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = rFam.GetUnusedInPlaceIdsForPurge(doc, GetUnusedCurtainWallSymbolIds)
+    :return: List of element ids
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    ids = rFamPurge.get_unused_in_place_ids_for_purge(
+        doc, get_unused_in_place_stair_type_ids
+    )
     return ids
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitCustomElementFilter.py` & `DuHast-0.0.7/src/duHast/Revit/Floors/Utility/floors_type_sorting.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,19 +1,19 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Customizable element filter class.
+This module contains a Revit floor utility functions. 
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2020  Jan Christel
+# Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
@@ -22,59 +22,51 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-# import Autodesk
-#import Autodesk.Revit.DB as rdb
+from duHast.Revit.Floors.Utility import floors_filter as rFloorsFilter
 
-class RevitCustomElementFilter:
 
-    def __init__(self, elementFilters = [] , isLogicalANDFilter = True):
-        '''
-        Constructor: This takes a list of element filters and a flag whether this class instance is a logical AND filter (default)
-
-        :param elementFilters: List of element filter functions which will need to accept document and elementId as their arguments, defaults to []
-        :type elementFilters: list of functions, optional
-        :param isLogicalANDFilter: Flag indicating whether list of filters are logical AND filters or logical OR, defaults to True (logical AND)
-        :type isLogicalANDFilter: bool, optional
-        '''
-
-        self.elementFilters = elementFilters
-        self.isLogicalANDFilter = isLogicalANDFilter
-    
-    def CheckElement(self, doc, elementId):
-        '''
-        Filter checking whether element meets criteria.
-
-        This function will loop over all the filters past in through the class constructor and test the element for each filter.
-        Depending on whether these filters are logical and filters it will return True if all of them evaluate to True or, if logical or filter
-        it will return True if one of them evaluates to True, otherwise False will be returned.
-
-        :param doc: Current Revit model document.
-        :type doc: Autodesk.Revit.DB.Document
-        :param elementId: The id of the element to be checked against the filter.
-        :type elementId: Autodesk.Revit.DB.ElementId
-        :return: True if it matches the filter(s), otherwise False
-        :rtype: bool
-        '''
-
-        if(self.isLogicalANDFilter):
-            filterOverAll = True
+def build_floor_type_dictionary(collector, dic):
+    """
+    Returns the dictionary past in with keys and or values added retrieved from collector past in.
+    Keys are built in floor family type names.
+    TODO: This code repeats across a number of modules. Use generic instead!
+    :param collector: A filtered element collector containing floor types.
+    :type collector: Autodesk.Revit.DB.FilteredElementCollector
+    :param dic: A dictionary containing key: floor type family name, value: list of ids belonging to that type.
+    :type dic: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
+    :return: A dictionary containing key: built in floor type family name, value: list of ids belonging to that type.
+    :rtype: dictionary (key str, value list of Autodesk.Revit.DB.ElementId)
+    """
+
+    for c in collector:
+        if dic.has_key(c.FamilyName):
+            if c.Id not in dic[c.FamilyName]:
+                dic[c.FamilyName].append(c.Id)
         else:
-            filterOverAll = False
-        
-        for filter in self.elementFilters:
-            filterResult = filter(doc, elementId)
-            if(self.isLogicalANDFilter == False and filterResult == True):
-                filterOverAll = True
-                # can leave the loop at this point since only one of the tests need to result true in OR filter mode
-                break
-            elif(self.isLogicalANDFilter == True and filterResult == False):
-                filterOverAll = False
-                # can leave the loop at this point since only one of the tests need to result false in AND filter mode
-                break
-            else:
-                filterOverAll = filterOverAll and filterResult
-        return filterOverAll
+            dic[c.FamilyName] = [c.Id]
+    return dic
+
+
+def sort_floor_types_by_family_name(doc):
+    """
+    Returns a dictionary containing all floor types in the model.
+    Key values are as per BUILTIN_FLOOR_TYPE_FAMILY_NAMES.
+    TODO: This code repeats across a number of modules. Use generic instead!
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :return: A dictionary containing key: floor type family name, value: list of ids.
+    :rtype: dic { str: [Autodesk.Revit.DB.ElementId]}
+    """
+
+    # get all floor Type Elements
+    wts = rFloorsFilter._get_floor_types_by_class(doc)
+    # get all floor types including in place floor families
+    wts_two = rFloorsFilter._get_all_floor_types_by_category(doc)
+    used_wts = {}
+    used_wts = build_floor_type_dictionary(wts, used_wts)
+    used_wts = build_floor_type_dictionary(wts_two, used_wts)
+    return used_wts
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitDesignSetOptions.py` & `DuHast-0.0.7/src/duHast/Revit/Common/design_set_options.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,15 +1,15 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 This module contains a number of functions around Revit Design Sets and Design Options.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -27,121 +27,130 @@
 #
 #
 
 import clr
 import System
 
 # import common library modules
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
+from duHast.Revit.Common import parameter_get_utils as rParaGet
 
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
 # -------------------------------------------- common variables --------------------
 #: header used in reports
-REPORT_DESIGNSET_HEADER = ['HOSTFILE','ID', 'NAME', 'PRIMARY OPTION', 'OTHER OPTIONS']
+REPORT_DESIGNSET_HEADER = ["HOSTFILE", "ID", "NAME", "PRIMARY OPTION", "OTHER OPTIONS"]
 
 # --------------------------------------------- utility functions ------------------
 
-def GetDesignOptions(doc):
-    '''
+
+def get_design_options(doc):
+    """
     Gets all design options in a model,
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: Design options in current model
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
 
     collector = rdb.FilteredElementCollector(doc).OfClass(rdb.DesignOption)
     return collector
 
-def GetDesignSets(doc):
-    '''
+
+def get_design_sets(doc):
+    """
     Gets all the design sets in a model,
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: Design sets in the current model
     :rtype: list of Autodesk.Revit.DB.Element
-    '''
+    """
 
     collector = rdb.FilteredElementCollector(doc).OfClass(rdb.DesignOption)
-    designSets = []
-    designSetNames = []
+    design_sets = []
+    design_set_names = []
     for do in collector:
-        e = doc.GetElement(do.get_Parameter(rdb.BuiltInParameter.OPTION_SET_ID).AsElementId())
+        e = doc.GetElement(
+            do.get_Parameter(rdb.BuiltInParameter.OPTION_SET_ID).AsElementId()
+        )
         designSetName = rdb.Element.Name.GetValue(e)
-        if(designSetName not in designSetNames):
-            designSets.append(e)
-            designSetNames.append(designSetName)
-    return designSets
+        if designSetName not in design_set_names:
+            design_sets.append(e)
+            design_set_names.append(designSetName)
+    return design_sets
+
 
-def IsDesignOptionPrimary(doc, designSetName, designOptionName):
-    '''
+def is_design_option_primary(doc, design_set_name, design_option_name):
+    """
     Checks whether a design option is the primary option within a design set.
-    
+
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param designSetName: The name of the design set the option belongs to,
-    :type designSetName: str
-    :param designOptionName: The name of the design option to be checked,
-    :type designOptionName: str
+    :param design_set_name: The name of the design set the option belongs to,
+    :type design_set_name: str
+    :param design_option_name: The name of the design option to be checked,
+    :type design_option_name: str
     :return: True if this option is primary otherwise False
     :rtype: bool
-    '''
+    """
 
     collector = rdb.FilteredElementCollector(doc).OfClass(rdb.DesignOption)
-    isPrimary = False
+    is_primary = False
     # loop over all design options in model, get the set they belong to and check for matches on both, set and option, by name
     for do in collector:
-        designOName = rdb.Element.Name.GetValue(do)
+        design_o_name = rdb.Element.Name.GetValue(do)
         # check if '< 'in name indicating a primary option, if so remove from name
-        index_chevron = designOName.find('<')
-        if (index_chevron > 0):
-            designOName = designOName[:index_chevron-2]
+        index_chevron = design_o_name.find("<")
+        if index_chevron > 0:
+            design_o_name = design_o_name[: index_chevron - 2]
         # design set
-        design_set = doc.GetElement(do.get_Parameter(rdb.BuiltInParameter.OPTION_SET_ID).AsElementId())
+        design_set = doc.GetElement(
+            do.get_Parameter(rdb.BuiltInParameter.OPTION_SET_ID).AsElementId()
+        )
         design_set_name = rdb.Element.Name.GetValue(design_set)
         # check for match on both set and option
-        if(design_set_name == designSetName and designOName == designOptionName):
+        if design_set_name == design_set_name and design_o_name == design_option_name:
             # get isPrimary property on design option
-            isPrimary = do.IsPrimary
+            is_primary = do.IsPrimary
             break
-    return isPrimary
+    return is_primary
+
 
-def GetDesignSetOptionInfo(doc, element):
-    '''
+def get_design_set_option_info(doc, element):
+    """
     Get the design set, design option information of an element.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :param element: The element of which the design set/option data is to be returned.
     :type element: Autodesk.Revit.DB.Element
     :return: Dictionary
         Design Set Name: (can be either Main Model or the design set name)
         designOptionName:    Design Option Name (empty string if Main Model
         isPrimary:           Indicating whether design option is primary (true also if Main Model)
     :rtype: Dictionary
         designSetName:str
         designOptionName:str
         isPrimary:bool
-    '''
+    """
 
     # keys match properties in DataDesignSetOption class!!
-    new_key= ['designSetName','designOptionName','isPrimary']
-    new_value= ['Main Model','-',True]
-    dic = dict(zip(new_key,new_value))
-    # get design option data from element
-    pValue = rParaGet.get_built_in_parameter_value(element, rdb.BuiltInParameter.DESIGN_OPTION_PARAM)
-    if(pValue != None):
-        designOptionData = pValue.split(':')
-        # check if main model ( length is 1! )
-        if(len(designOptionData) > 1):
-            dic['designSetName'] = designOptionData[0].Trim()
-            dic['designOptionName'] = designOptionData[1].Trim()
-            dic['isPrimary'] = IsDesignOptionPrimary(doc, dic['designSetName'], dic['designOptionName'])
-        else:
-            # use default values
-            pass
+    new_key = ["designSetName", "designOptionName", "isPrimary"]
+    new_value = ["Main Model", "-", True]
+    dic = dict(zip(new_key, new_value))
+    try:
+        # this only works for objects inheriting from Autodesk.Revit.DB.Element
+        design_option = element.DesignOption
+        dic["designOptionName"] = design_option.Name
+        dic["isPrimary"] = design_option.IsPrimary
+        e = doc.GetElement(
+            design_option.get_Parameter(
+                rdb.BuiltInParameter.OPTION_SET_ID
+            ).AsElementId()
+        )
+        dic["designSetName"] = rdb.Element.Name.GetValue(e)
+    except Exception as e:
+        pass
     return dic
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitDetailItems.py` & `DuHast-0.0.7/src/duHast/Revit/Categories/Utility/elements_by_category_utils.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,415 +1,282 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-This module contains a number of functions around Revit detail items.
+Revit elements to category helper functions.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2021  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
-#
-
-import clr
-clr.AddReference("System.Core")
-from System import Linq
-clr.ImportExtensions(Linq)
-import System
-
-# import common library modules
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.APISamples import RevitFamilyUtils as rFam
 
-# import Autodesk
 import Autodesk.Revit.DB as rdb
 
-# -------------------------------------------- common variables --------------------
-#: header used in reports
-REPORT_GROUPS_HEADER = ['HOSTFILE','ID', 'ITEM TYPE']
-
-# --------------------------------------------- utility functions ------------------
-
-def GetFilledRegionsInModel(doc):
-    '''
-    Gets all filled region instances in a model.
-
-    Filters by class.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list containing floor instances.
-    :rtype: list Autodesk.Revit.DB.FilledRegion
-    '''
-
-    return rdb.FilteredElementCollector(doc).OfClass(rdb.FilledRegion).ToList()
-
-'''
-TODO: check for actual class...
-'''
-#: class name Autodesk.Revit.DB.ElementType
-ELEMENT_TYPE = 'Autodesk.Revit.DB.ElementType'
-#: class name Autodesk.Revit.DB.FilledRegionType
-FILLED_REGION_TYPE = 'Autodesk.Revit.DB.FilledRegionType'
-#: class name Autodesk.Revit.DB.FamilySymbol
-FAMILY_SYMBOL = 'Autodesk.Revit.DB.FamilySymbol'
-
-#: List of class names which can be detailed components
-DETAIL_COMPONENT_TYPES = [
-    ELEMENT_TYPE,
-    FILLED_REGION_TYPE,
-    FAMILY_SYMBOL
-]
-
-def GetAllDetailTypesByCategory(doc):
-    '''
-    Gets all detail component types in the model.
-
-    Filters by built in category.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A filtered element collector containing detail component types.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_DetailComponents).WhereElementIsElementType()
-    return collector
-
-def BuildDetailTypeIdsDictionary(collector):
-    '''
-    Returns the dictionary keys is autodesk.revit.db element type as string and values are available type ids.
-
-    :param collector: A filtered element collector containing detail component types.
-    :type collector: Autodesk.Revit.DB.FilteredElementCollector
-
-    :return: Dictionary where key is the element type as string and value is a list of all type ids belonging to the element type.
-    :rtype: dic{str:list[Autodesk.Revit.DB.ElementId]}
-    '''
-
-    dic = {}
-    for c in collector:
-        if(dic.has_key(str(c.GetType()))):
-            if(c.Id not in dic[str(c.GetType())]):
-                dic[str(c.GetType())].append(c.Id)
+from duHast.Revit.Common import parameter_set_utils as rParaSet
+from duHast.Utilities.Objects import result as res
+from duHast.Revit.Links import cad_links_geometry as rCadLinkGeo
+from duHast.Revit.Common import parameter_get_utils as rParaGet
+
+from duHast.Revit.Categories.categories import (
+    ELEMENTS_PARAS_SUB,
+    get_main_sub_categories,
+)
+from duHast.Revit.Categories.Utility.category_properties_get_utils import (
+    get_category_graphic_style_ids,
+)
+from duHast.Revit.Categories.Utility.category_property_names import (
+    CATEGORY_GRAPHIC_STYLE_3D,
+)
+from duHast.Revit.Family import family_element_utils as rFamElementUtils
+
+
+def sort_elements_by_category(elements, element_dic):
+    """
+    Returns a dictionary of element ids where key is the category they belong to.
+    :param elements:  List of revit elements.
+    :type elements: [Autodesk.Revit.DB.Element]
+    :param element_dic:  Dictionary where key is subcategory and values are element ids.
+    :type element_dic: {Autodesk.Revit.DB.Category: [Autodesk.Revit.DB.ElementId]}
+    :return: Dictionary where key is subcategory id and values are element ids.
+    :rtype: {Autodesk.Revit.DB.ElementId: [Autodesk.Revit.DB.ElementId]}
+    """
+
+    for el in elements:
+        for builtin_def in ELEMENTS_PARAS_SUB:
+            value = rParaGet.get_built_in_parameter_value(
+                el, builtin_def, rParaGet.get_parameter_value_as_element_id
+            )
+            if value != None:
+                if value in element_dic:
+                    element_dic[value].append(el.Id)
+                else:
+                    element_dic[value] = [el.Id]
+                break
+    return element_dic
+
+
+def sort_geometry_elements_by_category(elements, element_dic, doc):
+    counter = 0
+    for el in elements:
+        counter = counter + 1
+        graphic_style_id = rdb.ElementId.InvalidElementId
+        if type(el) is rdb.Solid:
+            # get graphic style id from edges
+            edge_array = el.Edges
+            if edge_array.IsEmpty == False:
+                for edge in edge_array:
+                    graphic_style_id = edge.GraphicsStyleId
         else:
-            dic[str(c.GetType())] = [c.Id]
-    return dic
-
-def BuildDependentElementsDictionary(doc, collector):
-    '''
-    Returns the dictionary keys is autodesk.revit.db element type as string and values are elements of that type.
+            graphic_style_id = el.GraphicsStyleId
+        # failed to get an id?
+        if graphic_style_id != rdb.ElementId.InvalidElementId:
+            graphic_style = doc.GetElement(graphic_style_id)
+            graph_cat_id = graphic_style.GraphicsStyleCategory.Id
+            # geometry elements have no Id property ... Doh!! pass in invalid element id...
+            if graph_cat_id != None:
+                if graph_cat_id in element_dic:
+                    element_dic[graph_cat_id].append(rdb.ElementId.InvalidElementId)
+                else:
+                    element_dic[graph_cat_id] = [rdb.ElementId.InvalidElementId]
+    return element_dic
+
+
+def _sort_all_elements_by_category(doc):
+    """
+    Sorts all elements in a family by category.
+    :param doc: Current Revit family document.
+    :type doc: Autodesk.Revit.DB.Document
+    :return: Dictionary where key is subcategory id and values are element ids.
+    :rtype: {Autodesk.Revit.DB.ElementId: [Autodesk.Revit.DB.ElementId]}
+    """
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    :param collector: A filtered element collector containing elements.
-    :type collector: Autodesk.Revit.DB.FilteredElementCollector
-
-    :return: Dictionary where key is the element type as string and value is a list of all elements belonging to the element type.
-    :rtype: dic{str:list[Autodesk.Revit.DB.Element]}
-    '''
-   
+    # get all elements in family
     dic = {}
-    for c in collector:
-        el = doc.GetElement(c)
-        if(dic.has_key(str(el.GetType()))):
-            if(c not in dic[str(el.GetType())]):
-                dic[str(el.GetType())].append(c)
-        else:
-            dic[str(el.GetType())] = [c]
+    el_curve = rFamElementUtils.get_all_curve_based_elements_in_family(doc)
+    el_forms = rFamElementUtils.get_all_generic_forms_in_family(doc)
+    el_m_text = rFamElementUtils.get_all_model_text_elements_in_family(doc)
+    el_ref_planes = rFamElementUtils.get_all_reference_planes_in_family(doc)
+    # get import Instance elements
+    el_import = rCadLinkGeo.get_all_cad_import_instances_geometry(doc)
+    # build dictionary where key is category or graphic style id of  a category
+    dic = sort_elements_by_category(el_curve, dic)
+    dic = sort_elements_by_category(el_forms, dic)
+    dic = sort_elements_by_category(el_m_text, dic)
+    dic = sort_elements_by_category(el_ref_planes, dic)
+    # geometry instances use a property rather then a parameter to store the category style Id
+    dic = sort_geometry_elements_by_category(el_import, dic, doc)
     return dic
-    
-# -------------------------------- repeating detail types -------------------------------------------------------
-
-def GetAllRepeatingDetailTypeIdsAvailable(doc):
-    '''
-    Get all repeating detail type id's in model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of element ids representing repeating detail types.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    dic = BuildDetailTypeIdsDictionary(GetAllDetailTypesByCategory(doc))
-    if (dic.has_key(ELEMENT_TYPE)):
-        return dic[ELEMENT_TYPE]
-    else:
-        return []
 
-def GetUsedRepeatingDetailTypeIds(doc):
-    '''
-    Gets all used repeating detail type ids in the model.
 
-    Used: at least one instance of this type is placed in the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of element ids representing repeating detail types.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllRepeatingDetailTypeIdsAvailable, 1, 1)
-    return ids
-
-def GetUnUsedRepeatingDetailTypeIds(doc):
-    '''
-    Gets all unused repeating detail type ids in the model.
-
-    Unused: not one instance of this type is placed in the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    
-    :return: A list of element ids representing repeating detail types.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllRepeatingDetailTypeIdsAvailable, 0, 1)
-    return ids
-
-def GetUnUsedRepeatingDetailTypeIdsForPurge(doc):
-    '''
-    Gets type ids off all unused repeating detail types in model.
-
-    This method can be used to safely delete unused repeating detail types. In the case that no basic\
-        wall instance using any of the types is placed, this will return all but one type id since\
-        Revit requires at least one repeating detail type definition to be in the model.
-    
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids representing all repeating detail types not in use.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllRepeatingDetailTypeIdsAvailable, 0, 1)
-    allIds = GetAllRepeatingDetailTypeIdsAvailable(doc)
-    # need to keep at least one
-    if(len(allIds) == len(ids)):
-        ids.pop(0)
-    return ids
-
-# -------------------------------- Detail families -------------------------------------------------------
-
-def GetAllDetailSymbolIdsAvailable(doc):
-    '''
-    Gets all detail symbol (types) ids in model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of element ids representing detail symbols.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    dic = BuildDetailTypeIdsDictionary(GetAllDetailTypesByCategory(doc))
-    if (dic.has_key(FAMILY_SYMBOL)):
-        return dic[FAMILY_SYMBOL]
-    else:
-        return []
-
-def GetDetailSymbolsUsedInRepeatingDetails(doc, idsRepeatDet):
-    '''
-    Gets the ids of all symbols used in repeating details.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    :param idsRepeatDet: List of repeating detail type ids.
-    :type idsRepeatDet: list Autodesk.Revit.DB.ElementIds
-
-    :return: List of family symbol (type) ids.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    ids = []
-    for idR in idsRepeatDet:
-        repeatDetail = doc.GetElement(idR)
-        id = rParaGet.get_built_in_parameter_value(repeatDetail, rdb.BuiltInParameter.REPEATING_DETAIL_ELEMENT)
-        if(id not in ids and id != rdb.ElementId.InvalidElementId and id != None):
-            ids.append(id)
-    return ids
-
-def GetAllUsedDetailSymbolIds(doc):
-    '''
-    Gets all used detail symbol type ids in model.
-
-    Used: at least one instance of this type is placed in the model.
+def get_elements_by_category(doc, cat):
+    """
+    Returns elements in family assigned to a specific category
+    :param doc: Current Revit family document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param cat: A category.
+    :type cat: Autodesk.Revit.DB.Category
+    :return: Dictionary where key is subcategory and values are element ids.
+    :rtype: {Autodesk.Revit.DB.Category: [Autodesk.Revit.DB.ElementId]}
+    """
+
+    # get all elements in family
+    dic = _sort_all_elements_by_category(doc)
+    # get id and graphic style id of category to be filtered by
+    category_ids = get_category_graphic_style_ids(cat)
+    # check whether category past in is same as owner family category
+    if doc.OwnerFamily.FamilyCategory.Name == cat.Name:
+        # 3d elements within family which have subcategory set to 'none' belong to owner family
+        # category. Revit uses a None value as id rather then the actual category id
+        # my get parameter value translates that into -1 (invalid element id)
+        category_ids[CATEGORY_GRAPHIC_STYLE_3D] = rdb.ElementId.InvalidElementId
+    dic_filtered = {}
+    # filter elements by category ids
+    for key, value in category_ids.items():
+        # print (key + ' ' + str(value))
+        if value in dic:
+            dic_filtered[key] = dic[value]
+        else:
+            dic_filtered[key] = []
+    return dic_filtered
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
 
-    :return: List of family symbol (type) ids.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    ids = []
-    dic = BuildDetailTypeIdsDictionary(GetAllDetailTypesByCategory(doc))
-    if (dic.has_key(ELEMENT_TYPE)):
-        idsUnfiltered = dic[FAMILY_SYMBOL]
-        # check if used in repeating details
-        idsRepeatDet = GetAllRepeatingDetailTypeIdsAvailable(doc)
-        #print('ids used in repeating details ' + str(len(idsRepeatDet)))
-        # get detail types used in repeating details only
-        idsOfDetailsUsedRepeatDetails = GetDetailSymbolsUsedInRepeatingDetails(doc, idsRepeatDet)
-        # get detail types used in model
-        idsUsedInModel = com.GetUsedUnusedTypeIds(doc, GetAllDetailSymbolIdsAvailable, 1)
-        print('ids used in model ' + str(len(idsUsedInModel)))
-        # built overall ids list
-        for id in idsOfDetailsUsedRepeatDetails:
-            if (id not in ids):
-                ids.append(id)
-        for id in idsUsedInModel:
-            if(id not in ids):
-                ids.append(id)
-        return ids
+def move_elements_to_category(doc, elements, to_category_name, destination_cat_ids):
+    """
+    Moves elements provided in dictionary to another category specified by name.
+    :param doc: Current Revit family document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param elements: Dictionary of elements, key are graphic style names.
+    :type elements: {Autodesk.Revit.DB.Category: [Autodesk.Revit.DB.ElementId]}
+    :param to_category_name: The name of the subcategory elements are to be moved to.
+    :type to_category_name: str
+    :param destination_cat_ids: Dictionary of ids of graphic style, key are graphic style names
+    :type destination_cat_ids: dictionary {str: Autodesk.Revit.DB.ElementId}
+    :return:
+        Result class instance.
+        - result.status. True if all elements where moved to destination subcategories, otherwise False.
+        - result.message will contain the name of the destination subcategory by element.
+        - result.result empty list
+        On exception:
+        - result.status (bool) will be False.
+        - result.message will contain generic exception message.
+        - result.result will be empty
+    :rtype: :class:`.Result`
+    """
+
+    return_value = res.Result()
+    # check whether destination category exist in file
+    cats = get_main_sub_categories(doc)
+    if to_category_name in cats:
+        for key, value in elements.items():
+            # anything needing moving?
+            if len(value) > 0:
+                for el_id in value:
+                    el = doc.GetElement(el_id)
+                    paras = el.GetOrderedParameters()
+                    # find the parameter driving the subcategory
+                    for p in paras:
+                        if p.Definition.BuiltInParameter in ELEMENTS_PARAS_SUB:
+                            # get the subcategory style id
+                            target_id = destination_cat_ids[key]
+                            # check if a 'cut' style id exists...if not move to 'projection' instead
+                            # not sure how this works in none - english versions of Revit...
+                            if (
+                                key == "Cut"
+                                and target_id == rdb.ElementId.InvalidElementId
+                            ):
+                                target_id = destination_cat_ids["Projection"]
+                                return_value.append_message(
+                                    "No cut style present in family, using projection style instead"
+                                )
+                            updated_para = rParaSet.set_parameter_value(
+                                p, str(target_id), doc
+                            )
+                            return_value.update(updated_para)
+                            break
     else:
-        return []
-
-def GetAllUnUsedDetailSymbolIds(doc):
-    '''
-    Gets all unused detail symbol type ids in model.
-
-    Unused: Not one instance of this type is placed in the model.
-    
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of family symbol (type) ids.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    ids = []
-    allAvailableIds = GetAllDetailSymbolIdsAvailable(doc)
-    allUsedIds = GetAllUsedDetailSymbolIds(doc)
-    for id in allAvailableIds:
-        if(id not in allUsedIds):
-            ids.append(id)
-    return ids
-
-def GetAllUnUsedDetailSymbolIdsForPurge(doc):
-    '''
-    Gets type ids off all unused detail symbols (types) in model.
-
-    This method can be used to safely delete all unused detail symbols (types) and families.
-    
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids representing all unused detail symbols and families not in use.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = rFam.GetUnusedInPlaceIdsForPurge(doc, GetAllUnUsedDetailSymbolIds)
-    return ids
-    #ids = GetAllUnUsedDetailSymbolIds(doc)
-    #allAvailableIds = GetAllDetailSymbolIdsAvailable(doc)
-    # need to keep at least one
-    #if(len(allAvailableIds) == len(ids)):
-    #    ids.pop(0)
-    #return ids
-
-# -------------------------------- filled region types -------------------------------------------------------
-
-def GetAllFilledRegionTypeIdsAvailable(doc):
-    '''
-    Gets all filled region types ids in model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of element ids representing filled region types.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    dic = BuildDetailTypeIdsDictionary(GetAllDetailTypesByCategory(doc))
-    if (dic.has_key(FILLED_REGION_TYPE)):
-        return dic[FILLED_REGION_TYPE]
+        return_value.update_sep(
+            False,
+            "Destination category: {} does not exist in file!".format(to_category_name),
+        )
+    return return_value
+
+
+def move_elements_from_sub_category_to_sub_category(
+    doc, from_category_name, to_category_name
+):
+    """
+    Moves elements from one subcategory to another one identified by their names.
+    :param doc: Current Revit family document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param from_category_name: The source subcategory name.
+    :type from_category_name: str
+    :param to_category_name: The destination subcategory name.
+    :type to_category_name: str
+    :return:
+        Result class instance.
+        - result.status. True if all elements from source subcategory where moved to destination subcategory, otherwise False.
+        - result.message will contain the name of the destination subcategory by element.
+        - result.result empty list
+        On exception:
+        - result.status (bool) will be False.
+        - result.message will contain generic exception message.
+        - result.result will be empty
+    :rtype: :class:`.Result`
+    """
+
+    return_value = res.Result()
+    # check whether source and destination category exist in file
+    cats = get_main_sub_categories(doc)
+    if from_category_name in cats:
+        if to_category_name in cats:
+            # dictionary containing destination category ids (3D, cut and projection)
+            destination_cat_ids = get_category_graphic_style_ids(cats[to_category_name])
+            # get elements on source category
+            dic = get_elements_by_category(doc, cats[from_category_name])
+            # move elements
+            return_value = move_elements_to_category(
+                doc, dic, to_category_name, destination_cat_ids
+            )
+        else:
+            return_value.update_sep(
+                False,
+                "Destination category: {} does not exist in file!".format(
+                    to_category_name
+                ),
+            )
     else:
-        return []
-
-def GetUsedFilledRegionTypeIds(doc):
-    '''
-    Gets all used filled region type ids in model.
-
-    Used: at least one instance of this type is placed in the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of filled region type ids.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    ids = []
-    idsAll = GetAllFilledRegionTypeIdsAvailable(doc)
-    for id in idsAll:
-        el = doc.GetElement(id)
-        dic = BuildDependentElementsDictionary(doc, el.GetDependentElements(None))
-        if(dic.has_key('Autodesk.Revit.DB.FilledRegion')):
-            ids.append(id)
-    return ids
-
-def GetUnUsedFilledRegionTypeIds(doc):
-    ''''
-    Gets all unused filled region type ids in model.
-
-    Unused: Not one instance of this type is placed in the model.
-    
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of filled region type ids.
-    :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
-
-    ids = []
-    idsAll = GetAllFilledRegionTypeIdsAvailable(doc)
-    for id in idsAll:
-        el = doc.GetElement(id)
-        dic = BuildDependentElementsDictionary(doc, el.GetDependentElements(None))
-        if(dic.has_key('Autodesk.Revit.DB.FilledRegion') == False):
-            ids.append(id)
-    return ids
-
-def GetUnUsedFilledRegionTypeIdsForPurge(doc):
-    '''
-    Gets ids off all unused filled region types in model.
-
-    This method can be used to safely delete all unused filled region types in model. In the case that no filled\
-        region instance using any of the types is placed, this will return all but one type id since\
-        Revit requires at least one filled region type definition to be in the model.
-    
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids representing all unused filled region types not in use.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = GetUnUsedFilledRegionTypeIds(doc)
-    idsAll = GetAllFilledRegionTypeIdsAvailable(doc)
-    # need to keep at least one
-    if(len(idsAll) == len(ids)):
-        ids.pop(0)
-    return ids
+        return_value.update_sep(
+            False,
+            "Source category: {} does not exist in file!".format(from_category_name),
+        )
+    return return_value
+
+
+def get_used_category_ids(doc):
+    """
+    Returns all category ids in a family which have an element assigned to them
+    :param doc: Current Revit family document.
+    :type doc: Autodesk.Revit.DB.Document
+    :return: List of categories.
+    :rtype: [Autodesk.Revit.DB.Category]
+    """
+
+    # get all elements in family
+    dic = _sort_all_elements_by_category(doc)
+    return dic.keys()
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitElementParameterGetUtils.py` & `DuHast-0.0.7/src/duHast/Revit/Common/parameter_get_utils.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,515 +1,558 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Revit API utility functions to get parameter values.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 
 #!/usr/bin/python
 # -*- coding: utf-8 -*-
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2023  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 
 import System
 import clr
+
 clr.AddReference("System.Core")
 from System import Linq
+
 clr.ImportExtensions(Linq)
 
 # import everything from Autodesk Revit DataBase namespace (Revit API)
 import Autodesk.Revit.DB as rdb
 
 # utilities
-from duHast.Utilities import Utility as util
+from duHast.Utilities import utility as util
+from duHast.Utilities import unit_conversion as unitConversion
 
 # type checker
-#from typing import List, Callable
+# from typing import List, Callable
+
 
+# ----------------------------------------parameters-----------------------------------------------
 
-#----------------------------------------parameters-----------------------------------------------
 
 def check_parameter_value(
-    para, 
-    para_condition, # type: Callable[[str,str],bool]
-    condition_value):
+    para,
+    para_condition,  # type: Callable[[str,str],bool]
+    condition_value,
+):
     # type: (...) -> bool
-    '''
+    """
     Checks a parameter value based on passed in condition function.
 
-    This extracts the value of the past in parameter and compares it against a past in value using 
-    the also past in compare function. 
+    This extracts the value of the past in parameter and compares it against a past in value using
+    the also past in compare function.
     Note that values will be past into compare function as ASCII encoded.
 
     :param para: Parameter of which the value is to be checked.
-    :type para: Autodesk.Revit.DB.Parameter 
+    :type para: Autodesk.Revit.DB.Parameter
     :param para_condition:
         Function taking 2 arguments:
         First argument is the value to be checked against
         Second argument is the actual parameter value
         Needs to return a bool!
         Both arguments will be ASCII encoded at passing in.
     :type para_condition: function
     :param condition_value: The value to be checked for
-    :type condition_value: var 
+    :type condition_value: var
     :raise: Any exception will need to be managed by the function caller.
 
     :return:
         True if condition value is evaluated to be True by past in function paraCondition.
         Will return False if compare function returns None or a False.
     :rtype: bool
-    
-    '''
+
+    """
     # set default return value
     is_match = False
     parameter_value = get_parameter_value(para)
     # evaluate parameter value with past in value using past in function
-    compare_outcome = para_condition(util.EncodeAscii(condition_value), util.EncodeAscii(parameter_value))
+    compare_outcome = para_condition(
+        util.encode_ascii(condition_value), util.encode_ascii(parameter_value)
+    )
     # check the return value for a bool (True) only. Everything else will return False
-    if (compare_outcome == True):
+    if compare_outcome == True:
         is_match = True
     return is_match
 
-#----------------------------------------parameters value getter over loads-----------------------------------------------
+
+# ----------------------------------------parameters value getter over loads-----------------------------------------------
+
 
 def getter_none(para):
-    '''
+    """
     Used for parameters where the storage type is None
-    
+
     :param para: _description_
     :type para: _type_
-    '''
+    """
+
+    return "Invalid storage type: (NONE)"
 
-    return 'Invalid storage type: (NONE)'
 
 def getter_double_or_int_as_string(para):
-    '''
+    """
     Returns a parameter value of type double or integer as string.
 
     :param para: The parameter.
     :type para: Autodesk.Revit.DB.Parameter
 
     :return: String representation of double or integer value. If value is empty it will return None
     :rtype: str or None
-    '''
+    """
 
-    parameter_value = None
-    if(para.AsValueString() != None and para.AsValueString() != ''):
+    parameter_value = "None"
+    if para.AsValueString() != None and para.AsValueString() != "":
         parameter_value = para.AsValueString()
     return parameter_value
 
+
 def getter_double_as_double(para):
-    '''
+    """
     Returns a parameter value of type double as a double.
 
     :param para: The parameter.
     :type para: Autodesk.Revit.DB.Parameter
 
     :return: Double value. If value is empty it will return None
     :rtype: Double or None
-    '''
+    """
 
     parameter_value = None
-    if(para.AsValueString() != None and para.AsValueString() != ''):
+    if para.AsValueString() != None and para.AsValueString() != "":
         parameter_value = para.AsDouble()
     return parameter_value
 
-def getter_double_as_double_converted_to_millimeter(para):
-    '''
-    Returns a parameter value of type double as a double converted to mm (if required).
-    Revit uses feet internally for any length value!
+
+def getter_double_as_double_converted_to_metric(para):
+    """
+    Returns a parameter value of type double to metric if required.
+    Revit uses feet internally for any length value.
+    Revit uses square feet for areas
 
     :param para: The parameter.
     :type para: Autodesk.Revit.DB.Parameter
 
     :return: Double value. If value is empty it will return None
     :rtype: Double or None
-    '''
+    """
 
     parameter_value = None
-    if(para.AsValueString() != None and para.AsValueString() != ''):
-        if(para.Definition.ParameterType == rdb.ParameterType.Length):
-            parameter_value = para.AsDouble() * 304.8
+    if para.AsValueString() != None and para.AsValueString() != "":
+        if para.Definition.ParameterType == rdb.ParameterType.Length:
+            parameter_value = unitConversion.convert_imperial_feet_to_metric_mm(
+                para.AsDouble()
+            )
+        elif para.Definition.ParameterType == rdb.ParameterType.Area:
+            parameter_value = (
+                unitConversion.convert_imperial_square_feet_to_metric_square_metre(
+                    para.AsDouble()
+                )
+            )
+        elif para.Definition.ParameterType == rdb.ParameterType.Volume:
+            parameter_value = (
+                unitConversion.convert_imperial_cubic_feet_to_metric_cubic_metre(
+                    para.AsDouble()
+                )
+            )
         else:
             parameter_value = para.AsDouble()
     return parameter_value
 
+
 def getter_int_as_int(para):
-    '''
+    """
     Returns a parameter value of type integer as a integer.
 
     :param para: The parameter.
     :type para: Autodesk.Revit.DB.Parameter
 
     :return: Integer value. If value is empty it will return None
     :rtype: Integer or None
-    '''
+    """
 
     parameter_value = None
-    if(para.AsValueString() != None and para.AsValueString() != ''):
+    if para.AsValueString() != None and para.AsValueString() != "":
         parameter_value = para.AsInteger()
     return parameter_value
 
+
 def getter_string_as_UTF8_string(para):
-    '''
+    """
     Returns a parameter value of type string as a utf-8 formatted string.
-    
+
     :param para: The parameter.
     :type para: Autodesk.Revit.DB.Parameter
 
     :return: String value. If value is empty it will return None
     :rtype: String or None
-    '''
+    """
 
-    parameter_value = None
-    if(para.StorageType == rdb.StorageType.String):
-        if(para.AsString() != None and para.AsString() != ''):
-            parameter_value = para.AsString().encode('utf-8')
+    parameter_value = "None"
+    if para.StorageType == rdb.StorageType.String:
+        if para.AsString() != None and para.AsString() != "":
+            parameter_value = para.AsString().encode("utf-8")
     return parameter_value
 
+
 def getter_string_as_string(para):
-    '''
+    """
     Returns a parameter value of type string as a string.
 
     :param para: The parameter.
     :type para: Autodesk.Revit.DB.Parameter
 
     :return: String value. If value is empty it will return None
     :rtype: String or None
-    '''
+    """
 
-    parameter_value = None
-    if(para.StorageType == rdb.StorageType.String):
-        if(para.AsString() != None and para.AsString() != ''):
+    parameter_value = "None"
+    if para.StorageType == rdb.StorageType.String:
+        if para.AsString() != None and para.AsString() != "":
             parameter_value = para.AsString()
     return parameter_value
 
+
 def getter_element_id_as_string(para):
-    '''
+    """
     Returns a parameter value of type element id as a string.
 
     :param para: The parameter.
     :type para: Autodesk.Revit.DB.Parameter
 
     :return: String value. If value is empty it will return None
     :rtype: String or None
-    '''
+    """
 
-    parameter_value = None
-    if(para.StorageType == rdb.StorageType.ElementId):
-        if(para.AsElementId() != None):
+    parameter_value = "None"
+    if para.StorageType == rdb.StorageType.ElementId:
+        if para.AsElementId() != None:
             parameter_value = str(para.AsElementId())
-    return parameter_value     
+    return parameter_value
+
 
 def getter_element_id_as_element_id(para):
-    '''
+    """
     Returns a parameter value of type element id as a element id.
 
     :param para: The parameter.
     :type para: Autodesk.Revit.DB.Parameter
 
     :return: Element id value. If value is empty it will return None
     :rtype: Element id or None
-    '''
+    """
 
     parameter_value = None
-    if(para.StorageType == rdb.StorageType.ElementId):
-        if(para.AsElementId() != None):
+    if para.StorageType == rdb.StorageType.ElementId:
+        if para.AsElementId() != None:
             parameter_value = para.AsElementId()
     return parameter_value
 
+
 def getter_element_id_as_element_int(para):
-    '''
+    """
     Returns a parameter value of type element id as an integer.
 
     :param para: The parameter.
     :type para: Autodesk.Revit.DB.Parameter
 
     :return: Integer value. If value is empty it will return None
     :rtype: Integer or None
-    '''
+    """
 
     parameter_value = None
-    if(para.StorageType == rdb.StorageType.ElementId):
-        if(para.AsElementId() != None):
+    if para.StorageType == rdb.StorageType.ElementId:
+        if para.AsElementId() != None:
             parameter_value = para.AsElementId().IntegerValue
-    return parameter_value 
+    return parameter_value
+
 
-#----------------------------------------parameters value getters -----------------------------------------------
+# ----------------------------------------parameters value getters -----------------------------------------------
 
-def get_parameter_value_with_over_load (para, parameter_value_getters):
-    '''
+
+def get_parameter_value_with_over_load(para, parameter_value_getters):
+    """
     Returns a parameter value in format depending on storage type.
-    
+
     Storage type can be:
 
     - Double
     - Integer
     - String
     - ElementId
 
     Will throw an exception if a storage type is not covered by parameter value getter functions.
 
     :param para: The Parameter.
     :type para: Autodesk.Revit.DB.Parameter
-
+    :param parameter_value_getters: Dictionary containing the functions returning the parameter value depending on parameter storage type
+    :type parameter_value_getters: {Autodesk.Revit.DB.StorageType: func()}
     :return: The parameter value or if empty: None.
     :rtype: Depends on value getters functions
-    '''
+    """
 
-    # set return value default 
+    # set return value default ( default value should never be used...!)
     parameter_value = None
     try:
         # extract parameter value depending on its storage type
-        if(para.StorageType == rdb.StorageType.Double):
-            if(para.AsValueString()!= None and para.AsValueString() != ''):
-                if(rdb.StorageType.Double in parameter_value_getters):
-                    parameter_value = parameter_value_getters[rdb.StorageType.Double](para)
-                else:
-                    raise ValueError('No parameter value getter for storage type Double provided')
-        elif(para.StorageType == rdb.StorageType.Integer):
-            if(para.AsValueString()!= None and para.AsValueString() != ''):
-                if(rdb.StorageType.Integer in parameter_value_getters):
-                    parameter_value = parameter_value_getters[rdb.StorageType.Integer](para)
-                else:
-                    raise ValueError('No parameter value getter for storage type Integer provided')
-        elif(para.StorageType == rdb.StorageType.String):
-            if(para.AsString() != None and para.AsString() != ''):
-                if(rdb.StorageType.String in parameter_value_getters):
-                    parameter_value = parameter_value_getters[rdb.StorageType.String](para)
-                else:
-                    raise ValueError('No parameter value getter for storage type String provided')
-        elif(para.StorageType == rdb.StorageType.ElementId):
-            if(para.AsElementId() != None):
-                if(rdb.StorageType.ElementId in parameter_value_getters):
-                    parameter_value = parameter_value_getters[rdb.StorageType.ElementId](para)
-                else:
-                    raise ValueError('No parameter value getter for storage type Element Id provided')
+        if para.StorageType == rdb.StorageType.Double:
+            if rdb.StorageType.Double in parameter_value_getters:
+                parameter_value = parameter_value_getters[rdb.StorageType.Double](para)
+            else:
+                raise ValueError(
+                    "No parameter value getter for storage type Double provided"
+                )
+        elif para.StorageType == rdb.StorageType.Integer:
+            if rdb.StorageType.Integer in parameter_value_getters:
+                parameter_value = parameter_value_getters[rdb.StorageType.Integer](para)
+            else:
+                raise ValueError(
+                    "No parameter value getter for storage type Integer provided"
+                )
+        elif para.StorageType == rdb.StorageType.String:
+            if rdb.StorageType.String in parameter_value_getters:
+                parameter_value = parameter_value_getters[rdb.StorageType.String](para)
+            else:
+                raise ValueError(
+                    "No parameter value getter for storage type String provided"
+                )
+        elif para.StorageType == rdb.StorageType.ElementId:
+            if rdb.StorageType.ElementId in parameter_value_getters:
+                parameter_value = parameter_value_getters[rdb.StorageType.ElementId](
+                    para
+                )
+            else:
+                raise ValueError(
+                    "No parameter value getter for storage type Element Id provided"
+                )
         else:
             # this should be invalid storage type only
             parameter_value = parameter_value_getters[str(None)](para)
 
-    except  Exception as e:
-        parameter_value = 'Exception: {}'.format(e)
+    except Exception as e:
+        parameter_value = "Exception: {}".format(e)
     return parameter_value
 
-def get_parameter_value(
-    para
-    ):
+
+def get_parameter_value(para):
     # type: (...) -> str
-    '''
+    """
     Returns a parameter value as string independent of its storage type.
 
     :param para: Parameter of which the value is to be returned.
     :type para: Autodesk.Revit.DB.Parameter
     :raise: If an exception occurs the exception message will be returned as the parameter value prefixed with 'Exception: '
 
     :return:
         Default value is 'no Value' if parameter value is empty.
         Otherwise the actual parameter value.
         Will return 'Exception: ' + exception message if an exception occurred.
     :rtype: str
-    '''
+    """
 
-    # set return value default 
-    parameter_value = 'no Value'
+    # set return value default
+    parameter_value = "no Value"
     try:
         value_getter = {
-            rdb.StorageType.Double : getter_double_or_int_as_string,
-            rdb.StorageType.Integer : getter_double_or_int_as_string,
-            rdb.StorageType.String : getter_string_as_string,
-            rdb.StorageType.ElementId : getter_element_id_as_string,
-            str(None) : getter_none
+            rdb.StorageType.Double: getter_double_or_int_as_string,
+            rdb.StorageType.Integer: getter_double_or_int_as_string,
+            rdb.StorageType.String: getter_string_as_string,
+            rdb.StorageType.ElementId: getter_element_id_as_string,
+            str(None): getter_none,
         }
 
-        parameter_value = get_parameter_value_with_over_load (para, value_getter)
+        parameter_value = get_parameter_value_with_over_load(para, value_getter)
+
+    except Exception as e:
+        parameter_value = "Exception: " + str(e)
 
-    except  Exception as e:
-        parameter_value = 'Exception: '+str(e)
-    
     return parameter_value
 
-def get_parameter_value_utf8_string(
-    para
-    ):
+
+def get_parameter_value_utf8_string(para):
     # type: (...) -> str
-    '''
+    """
     Returns the parameter value as utf-8 string independent of its storage type.
 
     :param para: Parameter of which the value is to be returned.
-    :type para: Autodesk.Revit.DB.Parameter 
+    :type para: Autodesk.Revit.DB.Parameter
     :raise: If an exception occurs the exception message will be returned as the parameter value prefixed with 'Exception: '
 
     :return:
         Default value is 'no Value' if parameter value is empty.
         Otherwise the actual parameter value.
         Will return 'Exception: ' + exception message if an exception occurred.
     :rtype: str
-    '''
+    """
 
-    # set return value default 
-    parameter_value = 'no Value'
+    # set return value default
+    parameter_value = "no Value"
 
     value_getter = {
-            rdb.StorageType.Double : getter_double_or_int_as_string, # no specific utf encoding required
-            rdb.StorageType.Integer : getter_double_or_int_as_string, # no specific utf encoding required
-            rdb.StorageType.String : getter_string_as_UTF8_string,
-            rdb.StorageType.ElementId : getter_element_id_as_string, # no specific utf encoding required
-            str(None) : getter_none
-        }
-    
-    parameter_value = get_parameter_value_with_over_load (para, value_getter)
+        rdb.StorageType.Double: getter_double_or_int_as_string,  # no specific utf encoding required
+        rdb.StorageType.Integer: getter_double_or_int_as_string,  # no specific utf encoding required
+        rdb.StorageType.String: getter_string_as_UTF8_string,
+        rdb.StorageType.ElementId: getter_element_id_as_string,  # no specific utf encoding required
+        str(None): getter_none,
+    }
+
+    parameter_value = get_parameter_value_with_over_load(para, value_getter)
 
     return parameter_value
 
-def get_parameter_value_as_integer(
-    para
-    ):
+
+def get_parameter_value_as_integer(para):
     # type: (...) -> int
-    '''
+    """
     Returns the parameter value as integer only if the storage type is integer. Otherwise -1 will be returned.
 
     :param para: Parameter of which the value is to be returned.
-    :type para: Autodesk.Revit.DB.Parameter 
+    :type para: Autodesk.Revit.DB.Parameter
     :raise: Any exception will need to be managed by the function caller.
 
     :return:
         Default value is -1 if parameter value is empty or storage type is not integer.
         Otherwise the actual parameter value.
     :rtype: int
-    '''
+    """
 
     # set return value default
     parameter_value = -1
 
-    value_getter = {
-            rdb.StorageType.Integer : getter_int_as_int
-        }
-    
+    value_getter = {rdb.StorageType.Integer: getter_int_as_int}
+
     # extract parameter value depending on whether its storage type is integer, otherwise default value
-    if(para.StorageType == rdb.StorageType.Integer):
-        parameter_value = get_parameter_value_with_over_load (para, value_getter)
+    if para.StorageType == rdb.StorageType.Integer:
+        parameter_value = get_parameter_value_with_over_load(para, value_getter)
     return parameter_value
 
-def get_parameter_value_as_element_id(
-    para
-    ):
-    '''
+
+def get_parameter_value_as_element_id(para):
+    """
     Returns the parameter value as element Id only if the storage type is ElementId. Otherwise InvalidElementId (-1) will be returned.
 
     :param para: Parameter of which the value is to be returned.
-    :type para: Autodesk.Revit.DB.Parameter 
+    :type para: Autodesk.Revit.DB.Parameter
     :raise: Any exception will need to be managed by the function caller.
 
     :return:
         Default value is -1 if parameter value is empty or storage type is not integer.
         Otherwise the actual parameter value.
     :rtype: int
-    '''
+    """
 
     # set return value default
     parameter_value = rdb.ElementId.InvalidElementId
 
-    value_getter = {
-            rdb.StorageType.ElementId : getter_element_id_as_element_id
-        }
-    
+    value_getter = {rdb.StorageType.ElementId: getter_element_id_as_element_id}
+
     # check if element id...otherwise return the default value
-    if(para.StorageType == rdb.StorageType.ElementId):
-        parameter_value = get_parameter_value_with_over_load (para, value_getter)
+    if para.StorageType == rdb.StorageType.ElementId:
+        parameter_value = get_parameter_value_with_over_load(para, value_getter)
     return parameter_value
 
+
 def get_all_parameters_and_values_wit_custom_getters(element, parameter_value_getters):
-    '''
+    """
     Returns all parameters and their values as using custom value getter associated with provided element in form of a dictionary.
 
     :param element: The element
     :type element: var
+    :param parameter_value_getters: Dictionary containing the functions returning the parameter value depending on parameter storage type
+    :type parameter_value_getters: {Autodesk.Revit.DB.StorageType: func()}
 
     :return: Dictionary where key is the parameter name, and the value is the parameter value.
     :rtype: {str:var}
-    '''
+    """
     return_value = {}
     paras = element.GetOrderedParameters()
     for p in paras:
-        p_value =  get_parameter_value_with_over_load (p, parameter_value_getters)
+        p_value = get_parameter_value_with_over_load(p, parameter_value_getters)
         return_value[p.Definition.Name] = p_value
     return return_value
 
-def get_built_in_parameter_value(element, builtInParameterDef, parameterValueGetter = get_parameter_value_utf8_string):
-    '''
+
+def get_built_in_parameter_value(
+    element,
+    built_in_parameter_def,
+    parameter_value_getter=get_parameter_value_utf8_string,
+):
+    """
     Returns the built-in parameter value. Return value type depends on past in value getter function. Default is UTF-8 encoded string.
 
     :param element: Element to which the built-in parameter belongs.
-    :type element: Autodesk.Revit.DB.Element 
-    :param builtInParameterDef: The parameters built-in definition of which the value is to be returned.
-    :type builtInParameterDef: Autodesk.Revit.DB.Definition 
-    :param parameterValueGetter:
+    :type element: Autodesk.Revit.DB.Element
+    :param built_in_parameter_def: The parameters built-in definition of which the value is to be returned.
+    :type built_in_parameter_def: Autodesk.Revit.DB.Definition
+    :param parameter_value_getter:
         The function which takes the parameter as an argument and returns it's value.
-    :type parameterValueGetter: function
+    :type parameter_value_getter: function
     :raise: As per value getter method.
 
     :return:
         Default value is None if parameter does not exist on element.
         Otherwise the actual parameter value as per value getter method.
     :rtype: var
-    '''
+    """
 
     # set return value default
     parameter_value = None
     paras = element.GetOrderedParameters()
     for para in paras:
-        if(para.Definition.BuiltInParameter == builtInParameterDef):
-            parameter_value = parameterValueGetter(para)
+        if para.Definition.BuiltInParameter == built_in_parameter_def:
+            parameter_value = parameter_value_getter(para)
             break
     return parameter_value
 
+
 def get_parameter_value_by_name(
-    element, 
-    parameterName, # type: str
-    parameterValueGetter = get_parameter_value_utf8_string
-    ):
-    '''
+    element,
+    parameter_name,  # type: str
+    parameter_value_getter=get_parameter_value_utf8_string,
+):
+    """
     Returns the parameter value by parameter name.
 
     Return value type depends on past in value getter function. Default is UTF-8 encoded string.
 
     :param element: Element to which the built-in parameter belongs.
     :type element: Autodesk.Revit.DB.Element
-    :param parameterName: The parameters name of which the value is to be returned.
-    :type parameterName: str
-    :param parameterValueGetter:
+    :param parameter_name: The parameters name of which the value is to be returned.
+    :type parameter_name: str
+    :param parameter_value_getter:
         The function which takes the parameter as an argument and returns it's value.
-    :type parameterValueGetter: function
+    :type parameter_value_getter: function
     :raise: As per value getter method.
 
     :return:
         Default value is None if parameter does not exist on element.
         Otherwise the actual parameter value as per value getter method.
     :rtype: var
-    '''
+    """
 
     # set return value default
     parameter_value = None
     paras = element.GetOrderedParameters()
     for para in paras:
-        if(para.Definition.Name == parameterName):
-            parameter_value = parameterValueGetter(para)
+        if para.Definition.Name == parameter_name:
+            parameter_value = parameter_value_getter(para)
             break
-    return parameter_value
+    return parameter_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitElementParameterSetUtils.py` & `DuHast-0.0.7/src/duHast/Revit/Common/parameter_set_utils.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,57 +1,59 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Revit API utility functions to set parameter values.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 
 #!/usr/bin/python
 # -*- coding: utf-8 -*-
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2023  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 
 # class used for stats reporting
-from duHast.Utilities import Result as res
+from duHast.Utilities.Objects import result as res
 
 # import everything from Autodesk Revit DataBase namespace (Revit API)
 import Autodesk.Revit.DB as rdb
+
 # utilities
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.APISamples import RevitTransaction as rTran
+from duHast.Revit.Common import parameter_get_utils as rParaGet
+from duHast.Revit.Common import transaction as rTran
 
 # type checker
-#from typing import List, Callable
+# from typing import List, Callable
+
+# ----------------------------------------parameters value setters -----------------------------------------------
 
-#----------------------------------------parameters value setters -----------------------------------------------
 
 def set_parameter_value(
-    para, 
-    value_as_string, # type: str
+    para,
+    value_as_string,  # type: str
     doc,
-    in_transaction = rTran.in_transaction
-    ):
-    '''
+    in_transaction=rTran.in_transaction,
+):
+    """
     Sets the parameter value by trying to convert the past in string representing the value into the appropriate value type.
 
     Changing a parameter value requires this action to run inside a transaction.
 
     :param para: Parameter of which the value is to be set.
     :type para: Autodesk.Revit.DB.Parameter
     :param value_as_string: The new parameter value.
@@ -61,99 +63,127 @@
     :param in_transaction: The transaction wrapper function to be used.
     :type in_transaction: func(Autodesk.Revit.DB.Transaction, action(), Autodesk.Revit.DB.Document)
 
     :raise: Any exception will need to be managed by the function caller.
 
     ToDo: This needs updating for Revit 2022+ to take into account changes in Revit API: Forge Parameters
 
-    :return: 
+    :return:
         Result class instance.
 
         - Set parameter status (bool) returned in result.status. False if an exception occurred, otherwise True.
         - Result.message property updated in format: Changed parameter value of type x ['parameter name'] : 'old value' to: 'new value'.
-        
+
         On exception:
-        
+
         - Set parameter.status (bool) will be False.
         - Set parameter.message will contain the exception message.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
     old_value = rParaGet.get_parameter_value(para)
-    transaction_name = 'Update to parameter value'
+    transaction_name = "Update to parameter value"
     # different parameter storage types will require different actions due to value type past in is a string which will need converting
     # first before applied to the parameter
-    if(para.StorageType == rdb.StorageType.ElementId):
+    if para.StorageType == rdb.StorageType.ElementId:
         new_id = rdb.ElementId(int(value_as_string))
         # changing parameter value is required to run inside a transaction
         def action():
             # set up a result instance to be returned to caller with transaction outcome
             action_return_value = res.Result()
             try:
                 para.Set(new_id)
-                action_return_value.message = 'Changed parameter value of type Id.[ {} ] from: {} to: {}'.format(para.Definition.Name ,old_value ,value_as_string)
+                action_return_value.message = (
+                    "Changed parameter value of type Id.[ {} ] from: {} to: {}".format(
+                        para.Definition.Name, old_value, value_as_string
+                    )
+                )
             except Exception as e:
-                action_return_value.UpdateSep(False, 'Failed with exception: ' + str(e))
+                action_return_value.update_sep(
+                    False, "Failed with exception: {}".format(e)
+                )
             return action_return_value
-        transaction = rdb.Transaction(doc,transaction_name)
+
+        transaction = rdb.Transaction(doc, transaction_name)
         return_value = in_transaction(transaction, action)
-    elif(para.StorageType == rdb.StorageType.Double):
+    elif para.StorageType == rdb.StorageType.Double:
         # THIS IS THE KEY:  Use SetValueString instead of Set.  Set requires your data to be in
-        # whatever internal units of measure Revit uses. SetValueString expects your value to 
-        # be in whatever the current DisplayUnitType (units of measure) the document is set to 
+        # whatever internal units of measure Revit uses. SetValueString expects your value to
+        # be in whatever the current DisplayUnitType (units of measure) the document is set to
         # for the UnitType associated with the parameter.
         #
         # So SetValueString is basically how the Revit GUI works.
         def action():
             action_return_value = res.Result()
             try:
                 para.SetValueString(value_as_string)
-                action_return_value.message = 'Changed parameter value of type double.[ {} ] from: {} to: {}'.format(para.Definition.Name ,old_value ,value_as_string)
+                action_return_value.message = "Changed parameter value of type double.[ {} ] from: {} to: {}".format(
+                    para.Definition.Name, old_value, value_as_string
+                )
             except Exception as e:
-                action_return_value.UpdateSep(False, 'Failed with exception: {}'.format(e))
+                action_return_value.update_sep(
+                    False, "Failed with exception: {}".format(e)
+                )
             return action_return_value
-        transaction = rdb.Transaction(doc,transaction_name)
+
+        transaction = rdb.Transaction(doc, transaction_name)
         return_value = in_transaction(transaction, action)
-    elif (para.StorageType == rdb.StorageType.Integer):
+    elif para.StorageType == rdb.StorageType.Integer:
+
         def action():
             action_return_value = res.Result()
             try:
                 para.Set(int(value_as_string))
-                action_return_value.message = 'Changed parameter value of type integer.[ {} ] from: {} to: {}'.format(para.Definition.Name ,old_value ,value_as_string)
+                action_return_value.message = "Changed parameter value of type integer.[ {} ] from: {} to: {}".format(
+                    para.Definition.Name, old_value, value_as_string
+                )
             except Exception as e:
-                action_return_value.UpdateSep(False, 'Failed with exception: {}'.format(e))
+                action_return_value.update_sep(
+                    False, "Failed with exception: {}".format(e)
+                )
             return action_return_value
-        transaction = rdb.Transaction(doc,transaction_name)
+
+        transaction = rdb.Transaction(doc, transaction_name)
         return_value = in_transaction(transaction, action)
-    elif (para.StorageType == rdb.StorageType.String):
+    elif para.StorageType == rdb.StorageType.String:
+
         def action():
             action_return_value = res.Result()
             try:
                 para.Set(value_as_string)
-                action_return_value.message = 'Changed parameter value of type string.[ {} ] from: {} to: {}'.format(para.Definition.Name ,old_value ,value_as_string)
+                action_return_value.message = "Changed parameter value of type string.[ {} ] from: {} to: {}".format(
+                    para.Definition.Name, old_value, value_as_string
+                )
             except Exception as e:
-                action_return_value.UpdateSep(False, 'Failed with exception: {}'.format(e))
+                action_return_value.update_sep(
+                    False, "Failed with exception: {}".format(e)
+                )
             return action_return_value
-        transaction = rdb.Transaction(doc,transaction_name)
+
+        transaction = rdb.Transaction(doc, transaction_name)
         return_value = in_transaction(transaction, action, doc)
-    else:  
+    else:
         # dead end
-        return_value.UpdateSep(False, 'Dont know what to do with this storage type: {}'.format(para.StorageType))
+        return_value.update_sep(
+            False,
+            "Dont know what to do with this storage type: {}".format(para.StorageType),
+        )
     return return_value
 
+
 def set_built_in_parameter_value(
-    doc, 
-    element, 
-    built_in_parameter_def, 
-    value_as_string, # type: str
-    parameter_value_setter = set_parameter_value
-    ):
-    '''
+    doc,
+    element,
+    built_in_parameter_def,
+    value_as_string,  # type: str
+    parameter_value_setter=set_parameter_value,
+):
+    """
     Sets the built-in parameter value by trying to convert the past in string representing the value into the appropriate value type.
 
     Changing a parameter value requires this action to run inside a transaction.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :param element: Element to which the built-in parameter belongs.
@@ -161,34 +191,34 @@
     :param built_in_parameter_def: The parameters built-in definition of which the value is to be returned.
     :type built_in_parameter_def: Autodesk.Revit.DB.Definition
     :param value_as_string: The new parameter value.
     :type value_as_string: str
     :param parameter_value_setter:
         The function which takes the parameter as an argument and changes it's value to.
         The function needs to accept these args: parameter, new parameter value as string, document
-    :type parameter_value_setter: function 
+    :type parameter_value_setter: function
     :raise: As per value setter method.
-    
+
     ToDo: This needs updating for Revit 2022+ to take into account changes in Revit API: Forge Parameters
 
-    :return: 
+    :return:
         Result class instance.
 
         - Set parameter status (bool) returned in result.status. False if an exception occurred, or parameter does not exist on element, otherwise True.
         - Result.message property updated in format: Changed parameter value of type x ['parameter name'] : 'old value' to: 'new value'.
-        
+
         On exception:
-        
+
         - Set parameter.status (bool) will be False.
         - Set parameter.message will contain the exception message.
-        
+
     :rtype: :class:`.Result`
-    '''
-    
+    """
+
     return_value = res.Result()
-    return_value.UpdateSep(False, 'Parameter not found')
+    return_value.update_sep(False, "Parameter not found")
     paras = element.GetOrderedParameters()
     for para in paras:
-        if(para.Definition.BuiltInParameter == built_in_parameter_def):
+        if para.Definition.BuiltInParameter == built_in_parameter_def:
             return_value = parameter_value_setter(para, value_as_string, doc)
             break
-    return return_value
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitExportIFCSettings.py` & `DuHast-0.0.7/src/duHast/Revit/Exports/Utility/ifc_export_settings.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,108 +1,110 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 IFC export settings class.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import System
+from duHast.Utilities.Objects import base
+
+
+class IFCSettings(base.Base):
+
+    supported_ifc_versions = {
+        "Default": "The Autodesk Revit applications default export format. Note that this may change as the defaults change in the Revit user interface.",
+        "IFCBCA": "IFC BCA file format. This is a certified variant of IFC 2x2 used for submitting files to the Singapore BCA ePlan Check Server.",
+        "IFC2x2": "IFC 2x2 file format.",
+        "IFC2x3": "IFC 2x3 file format.",
+        "IFCCOBIE": "IFC GSA COBIE 2010 file format. This is a variant of IFC 2x3 used for submitting files that are COBIE 2010-complaint.",
+        "IFC2x3CV2": "IFC 2x3 Coordination View 2.0 file format. This is a variant of IFC 2x3 used for exporting files using the Coordination View 2.0 model view.",
+        "IFC4": "IFC 4 file format.",
+        "IFC2x3FM": "IFC2x3 Extended FM Handover View",
+        "IFC4RV": "IFC4 Reference View",
+        "IFC4DTV": "IFC4 Design Transfer View",
+        "IFC2x3BFM": "IFC2x3 Basic FM Handover View",
+    }
 
-class IFCSettings():
-    
-    supportedIfcVersions = {
-            'Default' : 'The Autodesk Revit applications default export format. Note that this may change as the defaults change in the Revit user interface.',
-            'IFCBCA' : 'IFC BCA file format. This is a certified variant of IFC 2x2 used for submitting files to the Singapore BCA ePlan Check Server.',
-            'IFC2x2' : 'IFC 2x2 file format.',
-            'IFC2x3' : 'IFC 2x3 file format.',
-            'IFCCOBIE' : 'IFC GSA COBIE 2010 file format. This is a variant of IFC 2x3 used for submitting files that are COBIE 2010-complaint.',
-            'IFC2x3CV2' : 'IFC 2x3 Coordination View 2.0 file format. This is a variant of IFC 2x3 used for exporting files using the Coordination View 2.0 model view.',
-            'IFC4' : 'IFC 4 file format.',
-            'IFC2x3FM' : 'IFC2x3 Extended FM Handover View',
-            'IFC4RV' : 'IFC4 Reference View',
-            'IFC4DTV' : 'IFC4 Design Transfer View',
-            'IFC2x3BFM' : 'IFC2x3 Basic FM Handover View'
-        }
-    
-    sitePlacementOptions = {
-        'SiteTransformBasis.Shared' :'shared', 
-        'SiteTransformBasis.Site' : 'site', 
-        'SiteTransformBasis.Project' : 'project',
-        'SiteTransformBasis.Internal' : 'internal', 
-        'SiteTransformBasis.ProjectInTN' : 'projectInTN',
-        'SiteTransformBasis.InternalInTN' : 'internalInTN'
+    site_placement_options = {
+        "SiteTransformBasis.Shared": "shared",
+        "SiteTransformBasis.Site": "site",
+        "SiteTransformBasis.Project": "project",
+        "SiteTransformBasis.Internal": "internal",
+        "SiteTransformBasis.ProjectInTN": "projectInTN",
+        "SiteTransformBasis.InternalInTN": "internalInTN",
     }
 
     def __init__(
-        self, 
-        name, 
-        ifcVersion, 
-        spaceBoundaries,
-        activePhaseId,
-        activeViewId,
-        exportBaseQuantities,
-        splitWallsAndColumns,
-        visibleElementsOfCurrentView,
-        use2DRoomBoundaryForVolume,
-        useFamilyAndTypeNameForReference,
-        exportInternalRevitPropertySets,
-        exportIFCCommonPropertySets,
-        export2DElements,
-        exportPartsAsBuildingElements,
-        exportBoundingBox,
-        exportSolidModelRep,
-        exportSchedulesAsPsets,
-        exportUserDefinedPsets,
-        exportUserDefinedPsetsFileName,
-        exportLinkedFiles,
-        includeSiteElevation,
-        useActiveViewGeometry,
-        exportSpecificSchedules,
-        tessellationLevelOfDetail,
-        storeIFCGUID,
-        exportRoomsInView,
-        useOnlyTriangulation,
-        includeSteelElements,
-        cOBieCompanyInfo,
-        cOBieProjectInfo,
-        useTypeNameOnlyForIfcType,
-        useVisibleRevitNameAsEntityName,
-        sitePlacement,
-        selectedSite,
-        geoRefCRSName,
-        geoRefCRSDesc,
-        geoRefEPSGCode,
-        geoRefGeodeticDatum,
-        geoRefMapUnit,
-        excludeFilter
-        ):
+        self,
+        name,
+        ifc_version,
+        space_boundaries,
+        active_phase_id,
+        active_view_id,
+        export_base_quantities,
+        split_walls_and_columns,
+        visible_elements_of_current_view,
+        use2_d_room_boundary_for_volume,
+        use_family_and_type_name_for_reference,
+        export_internal_revit_property_sets,
+        export_ifc_common_property_sets,
+        export_2d_elements,
+        export_parts_as_building_elements,
+        export_bounding_box,
+        export_solid_model_rep,
+        export_schedules_as_psets,
+        export_user_defined_psets,
+        export_user_defined_psets_file_name,
+        export_linked_files,
+        include_site_elevation,
+        use_active_view_geometry,
+        export_specific_schedules,
+        tessellation_level_of_detail,
+        store_ifc_guid,
+        export_rooms_in_view,
+        use_only_triangulation,
+        include_steel_elements,
+        cobie_company_info,
+        cobie_project_info,
+        use_type_name_only_for_ifc_type,
+        use_visible_revit_name_as_entity_name,
+        site_placement,
+        selected_site,
+        geo_ref_crs_name,
+        geo_ref_crs_desc,
+        geo_ref_epsg_code,
+        geo_ref_geodetic_datum,
+        geo_ref_map_unit,
+        exclude_filter,
+    ):
 
-        '''
+        """
         _summary_
 
         :param name: The name of the configuration.
         :type name:
         :param ifcVersion: The IFCFileFormat of the configuration.
         :type ifcVersion:
         :param spaceBoundaries: The level of space boundaries of the configuration.
@@ -179,61 +181,69 @@
         :type geoRefGeodeticDatum: str
         :param geoRefMapUnit: The Map Unit of the ProjectedCRS
         :type geoRefMapUnit: str
         :param excludeFilter: Exclude filter string (element list in an array, separated with semicolon ';')
         :type excludeFilter: str
 
         :raises Exception: _description_
-        '''
+        """
+
+        # forwards all unused arguments
+        # ini super class to allow multi inheritance in children!
+        super(IFCSettings, self).__init__()
 
         self.name = name
 
         # check the IFC version
-        if(ifcVersion in self.supportedIfcVersions):
-            self.ifcVersion = ifcVersion
+        if ifc_version in self.supported_ifc_versions:
+            self.ifc_version = ifc_version
         else:
-            raise Exception('Unsupported IFC version:' + ifcVersion)
+            raise Exception("Unsupported IFC version:" + ifc_version)
+
+        self.space_boundaries = space_boundaries
+        self.active_phase_id = active_phase_id
+        self.active_view_id = active_view_id
+        self.export_base_quantities = export_base_quantities
+        self.split_walls_and_columns = split_walls_and_columns
+        self.visible_elements_of_current_view = visible_elements_of_current_view
+        self.use2_d_room_boundary_for_volume = use2_d_room_boundary_for_volume
+        self.use_family_and_type_name_for_reference = (
+            use_family_and_type_name_for_reference
+        )
+        self.export_internal_revit_property_sets = export_internal_revit_property_sets
+        self.export_ifc_common_property_sets = export_ifc_common_property_sets
+        self.export_2d_elements = export_2d_elements
+        self.export_parts_as_building_elements = export_parts_as_building_elements
+        self.export_bounding_box = export_bounding_box
+        self.export_solid_model_rep = export_solid_model_rep
+        self.export_schedules_as_psets = export_schedules_as_psets
+        self.export_user_defined_psets = export_user_defined_psets
+        self.export_user_defined_psets_file_name = export_user_defined_psets_file_name
+        self.export_linked_files = export_linked_files
+        self.include_site_elevation = include_site_elevation
+        self.use_active_view_geometry = use_active_view_geometry
+        self.export_specific_schedules = export_specific_schedules
+        self.tessellation_level_of_detail = tessellation_level_of_detail
+        self.store_ifc_guid = store_ifc_guid
+        self.export_rooms_in_view = export_rooms_in_view
+        self.use_only_triangulation = use_only_triangulation
+        self.include_steel_elements = include_steel_elements
+        self.cobie_company_info = cobie_company_info
+        self.cobie_project_info = cobie_project_info
+        self.use_type_name_only_for_ifc_type = (use_type_name_only_for_ifc_type,)
+        self.use_visible_revit_name_as_entity_name = (
+            use_visible_revit_name_as_entity_name
+        )
 
-        self.spaceBoundaries = spaceBoundaries
-        self.activePhaseId = activePhaseId
-        self.activeViewId = activeViewId
-        self.exportBaseQuantities = exportBaseQuantities
-        self.splitWallsAndColumns = splitWallsAndColumns
-        self.visibleElementsOfCurrentView = visibleElementsOfCurrentView
-        self.use2DRoomBoundaryForVolume = use2DRoomBoundaryForVolume
-        self.useFamilyAndTypeNameForReference = useFamilyAndTypeNameForReference
-        self.exportInternalRevitPropertySets = exportInternalRevitPropertySets
-        self.exportIFCCommonPropertySets = exportIFCCommonPropertySets
-        self.export2DElements = export2DElements
-        self.exportPartsAsBuildingElements = exportPartsAsBuildingElements
-        self.exportBoundingBox = exportBoundingBox
-        self.exportSolidModelRep = exportSolidModelRep
-        self.exportSchedulesAsPsets = exportSchedulesAsPsets
-        self.exportUserDefinedPsets = exportUserDefinedPsets
-        self.exportUserDefinedPsetsFileName = exportUserDefinedPsetsFileName
-        self.exportLinkedFiles = exportLinkedFiles
-        self.includeSiteElevation = includeSiteElevation
-        self.useActiveViewGeometry = useActiveViewGeometry
-        self.exportSpecificSchedules = exportSpecificSchedules
-        self.tessellationLevelOfDetail = tessellationLevelOfDetail
-        self.storeIFCGUID = storeIFCGUID
-        self.exportRoomsInView = exportRoomsInView
-        self.useOnlyTriangulation = useOnlyTriangulation
-        self.includeSteelElements = includeSteelElements
-        self.cOBieCompanyInfo = cOBieCompanyInfo
-        self.cOBieProjectInfo = cOBieProjectInfo
-        self.useTypeNameOnlyForIfcType = useTypeNameOnlyForIfcType,
-        self.useVisibleRevitNameAsEntityName = useVisibleRevitNameAsEntityName
-        
         # check site placement option
-        if(sitePlacement in self.sitePlacementOptions):
-            self.sitePlacement =  self.sitePlacementOptions[sitePlacement]
+        if site_placement in self.site_placement_options:
+            self.site_placement = self.site_placement_options[site_placement]
         else:
-            raise Exception('Unsupported site placement option:' + sitePlacement)
-        
-        self.selectedSite = selectedSite
-        self.geoRefCRSName = geoRefCRSName
-        self.geoRefCRSDesc = geoRefCRSDesc
-        self.geoRefEPSGCode = geoRefEPSGCode
-        self.geoRefGeodeticDatum = geoRefGeodeticDatum
-        self.geoRefMapUnit = geoRefMapUnit
-        self.excludeFilter = excludeFilter
+            raise Exception("Unsupported site placement option:" + site_placement)
+
+        self.selected_site = selected_site
+        self.geo_ref_crs_name = geo_ref_crs_name
+        self.geo_ref_crs_desc = geo_ref_crs_desc
+        self.geo_ref_epsg_code = geo_ref_epsg_code
+        self.geo_ref_geodetic_datum = geo_ref_geodetic_datum
+        self.geo_ref_map_unit = geo_ref_map_unit
+        self.exclude_filter = exclude_filter
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyBaseData.py` & `DuHast-0.0.7/src/duHast/Revit/Family/Data/family_base_data.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,63 +1,69 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Family base data class.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-from duHast.APISamples import IFamilyData as IFamData
-from duHast.Utilities import Utility as util
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import RevitFamilyBaseDataUtils as rFamBaseDataUtils
+from duHast.Revit.Family.Data import ifamily_data as IFamData
+from duHast.Utilities import directory_io as dirIO, files_io as fileIO
+from duHast.Revit.Common import file_io as rFile
+from duHast.Revit.Family.Data import family_base_data_utils as rFamBaseDataUtils
 
 # import Autodesk
-#import Autodesk.Revit.DB as rdb
+# import Autodesk.Revit.DB as rdb
 
 # data dictionary key values specific to this class
-CATEGORY_NAME = 'categoryName'
+CATEGORY_NAME = "categoryName"
+
 
 class FamilyBaseData(IFamData.IFamilyData):
-    
-    def __init__(self, rootPath=None, rootCategoryPath=None, dataType=None):
-        '''
+    def __init__(self, root_path=None, root_category_path=None, data_type=None):
+        """
         Class constructor
 
         :param rootPath: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
             This includes the actual family name as the last node.
         :type rootPath: str
         :param dataType: Human readable data type descriptor
         :type dataType: str
-        '''
+        """
 
-        # todo: check inheritance!!
+        # store data type  in base class
+        super(FamilyBaseData, self).__init__(
+            root_path=root_path,
+            root_category_path=root_category_path,
+            data_type=data_type,
+        )
         # super(CategoryData, self).__init__(rootPath, dataType)
 
+        """
         self.data = []
         
         if(dataType != None):
             self.dataType = dataType
         else:
             self.dataType = 'not declared'
         
@@ -66,23 +72,32 @@
         else:
             self.rootPath = '-'
 
         if(rootCategoryPath != None):
             self.rootCategoryPath = rootCategoryPath
         else:
             self.rootCategoryPath = '-'
-        
-        if(rootCategoryPath != None):
-            categoryChunks = rootCategoryPath.split(' :: ')
-            self.category = categoryChunks[-1]
+        """
+
+        if root_category_path != None:
+            category_chunks = root_category_path.split(" :: ")
+            self.category = category_chunks[-1]
         else:
-            self.category = 'unknown'
+            self.category = "unknown"
 
-    def _saveOut(self, doc, referenceFilePath, docName, docCategory, familyOutFolderPath, sessionId):
-        '''
+    def _save_out(
+        self,
+        doc,
+        reference_file_path,
+        doc_name,
+        doc_category,
+        family_out_folder_path,
+        session_id,
+    ):
+        """
         Saves a family to file if there is no match for it in the provided reference file. 
         The reference file is a FamilyBaseDataCombinedReport and is read into tuples using RevitFamilyBaseDataUtils.
 
         :param doc: Current family document
         :type doc: Autodesk.Revit.DB.Document
         :param referenceFilePath: Fully qualified file path to FamilyBaseDataCombinedReport file.
         :type referenceFilePath: str
@@ -92,69 +107,82 @@
         :type docCategory: str
         :param familyOutFolderPath: The root directory path to which a family is saved. The script will create a sub directory\
             based on the revit batch processor session id and within that folder another sub directory based on the family Revit category:\
                 familyOutFolderPath\\SessionId\\RevitCategory\\Myfamily.rfa
         :type familyOutFolderPath: str
         :param sessionId: The batchprocessor session Id (formatted so it can be used as a folder name)
         :type sessionId: str
-        '''
+        """
 
         # process reference file list and look for a match:
         # based on file name and category
-        if(util.FileExist(referenceFilePath)):
-            # read overall family base data from file 
-            overallFamilyBaseRootData, overallFamilyBaseNestedData = rFamBaseDataUtils.ReadOverallFamilyDataList(referenceFilePath)
-            foundMatch = False
-            for rootFam in overallFamilyBaseRootData:
+        if fileIO.file_exist(reference_file_path):
+            # read overall family base data from file
+            (
+                overall_family_base_root_data,
+                overall_family_base_nested_data,
+            ) = rFamBaseDataUtils.read_overall_family_data_list(reference_file_path)
+            found_match = False
+            for root_fam in overall_family_base_root_data:
                 # check whether name and category are a match
-                if(rootFam.name == docName and rootFam.category == docCategory):
-                    foundMatch = True
+                if root_fam.name == doc_name and root_fam.category == doc_category:
+                    found_match = True
                     break
             # check if family needs saving out
-            if(foundMatch == False):
+            if found_match == False:
                 # check session id folder exists
-                if(util.CreateTargetFolder(familyOutFolderPath, sessionId)):
+                if dirIO.create_target_directory(family_out_folder_path, session_id):
                     # check category folder exists
-                    if(util.CreateTargetFolder(familyOutFolderPath + '\\' + sessionId, docCategory)):
+                    if dirIO.create_target_directory(
+                        family_out_folder_path + "\\" + session_id, doc_category
+                    ):
                         # save family out
-                        com.SaveAsFamily(
+                        rFile.save_as_family(
                             doc,
-                            familyOutFolderPath + '\\' + sessionId + '\\'+ docCategory,
-                            docName,
-                            [[docName, docName]]
-                            )
+                            family_out_folder_path
+                            + "\\"
+                            + session_id
+                            + "\\"
+                            + doc_category,
+                            doc_name,
+                            [[doc_name, doc_name]],
+                        )
 
-    def process(self, doc, referenceFilePath, familyOutFolderPath, sessionId):
-        '''
+    def process(self, doc, reference_file_path, family_out_directory_path, session_id):
+        """
         Collects all base data from the document and stores it in the class property .data
 
         :param doc: Current family document
         :type doc: Autodesk.Revit.DB.Document
-        '''
+        """
 
-        # get the family category name 
-        #famCatName = doc.OwnerFamily.FamilyCategory.Name
+        # get the family category name
+        # famCatName = doc.OwnerFamily.FamilyCategory.Name
 
         # check if a reference file list was provided and if so if family needs to be saved out
-        if (referenceFilePath != None and familyOutFolderPath != None and sessionId != None):
-            self._saveOut(
-                doc, 
-                referenceFilePath, 
-                self._stripFileExtension(doc.Title), 
-                self.category, 
-                familyOutFolderPath, 
-                sessionId
-                )
-        
+        if (
+            reference_file_path != None
+            and family_out_directory_path != None
+            and session_id != None
+        ):
+            self._save_out(
+                doc,
+                reference_file_path,
+                self._strip_file_extension(doc.Title),
+                self.category,
+                family_out_directory_path,
+                session_id,
+            )
+
         # build data
         self.data.append(
             {
-                IFamData.ROOT : self.rootPath,
-                IFamData.ROOT_CATEGORY : self.rootCategoryPath,
-                IFamData.FAMILY_NAME : self._stripFileExtension(doc.Title),
-                IFamData.FAMILY_FILE_PATH : doc.PathName, # this property will often be an empty string in nested families
-                CATEGORY_NAME : self.category
+                IFamData.ROOT: self.root_path,
+                IFamData.ROOT_CATEGORY: self.root_category_path,
+                IFamData.FAMILY_NAME: self._strip_file_extension(doc.Title),
+                IFamData.FAMILY_FILE_PATH: doc.PathName,  # this property will often be an empty string in nested families
+                CATEGORY_NAME: self.category,
             }
         )
 
-    def get_Data(self):
-        return self.data
+    def get_data(self):
+        return self.data
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyBaseDataAnalysisCircularReferencing.py` & `DuHast-0.0.7/src/duHast/Revit/Family/Data/family_base_data_circular_referencing.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Family Base data analysis module containing functions to find circular family referencing in extracted data.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 A circular reference is when a family A has a family B nested but family B has also family A nested.
 
 Algorithm description:
@@ -19,312 +19,365 @@
             - get all families lower in root path of nested family and add to child property of root family if not already
             -   TODO: Check this theory: families always have the same children...once children are identified there is no need to check over and over again!
 
 - loop over root family 
     -   check whether any family exist in parent and child family
         - YES: found circular reference
 
-'''
+"""
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import threading
 import os
 
-from duHast.APISamples import RevitFamilyBaseDataUtils as rFamBaseDataUtils
-from duHast.Utilities.timer import Timer
-from duHast.Utilities import Result as res
+from duHast.Revit.Family.Data import family_base_data_utils as rFamBaseDataUtils
+from duHast.Utilities.Objects.timer import Timer
+from duHast.Utilities.Objects import result as res
+
 
-def _ExtractParentFamilies(currentParent, treePath):
-    '''
+def _extract_parent_families(current_parent, tree_path):
+    """
     Find the index of the match in the root tree, any entries in the root tree list with a lower index are parents
 
-    Note: Changes currentParent.parent property of the currentParent variable!
+    Note: Changes current_parent.parent property of the current_parent variable!
 
-    :param currentParent: A tuple containing family root data
-    :type currentParent: named tuple rootFamily
-    :param treePath: list of family names describing the nesting tree of a family
-    :type treePath: [str]
+    :param current_parent: A tuple containing family root data
+    :type current_parent: named tuple rootFamily
+    :param tree_path: list of family names describing the nesting tree of a family
+    :type tree_path: [str]
     :return: Nothing
     :rtype: None
-    '''
-   
-    indexMatch = treePath.index(currentParent.name)
+    """
+
+    index_match = tree_path.index(current_parent.name)
     # double check...it exists and it is not root itself
-    if(indexMatch > 0):
+    if index_match > 0:
         # add all parents
-        for i in range (indexMatch):
-            if(treePath[i] not in currentParent.parent):
-                currentParent.parent.append(treePath[i])
+        for i in range(index_match):
+            if tree_path[i] not in current_parent.parent:
+                current_parent.parent.append(tree_path[i])
 
 
-def _ExtractChildFamilies(currentParent, treePath):
-    '''
+def _extract_child_families(current_parent, tree_path):
+    """
     Find the index of the match in the root tree, any entries in the root tree list with a lower index are children
 
-    Note: Changes currentParent.child property of the currentParent variable!
+    Note: Changes current_parent.child property of the current_parent variable!
 
-    :param currentParent: A tuple containing family root data
-    :type currentParent: named tuple rootFamily
-    :param treePath: list of family names describing the nesting tree of a family
-    :type treePath: [str]
+    :param current_parent: A tuple containing family root data
+    :type current_parent: named tuple rootFamily
+    :param tree_path: list of family names describing the nesting tree of a family
+    :type tree_path: [str]
     :return: Nothing
     :rtype: None
-    '''
+    """
 
-    indexMatch = treePath.index(currentParent.name)
+    index_match = tree_path.index(current_parent.name)
     # double check...it exists and it is not root itself and its not the last item in tree path
-    if(indexMatch > 0 and indexMatch != len(treePath)):
+    if index_match > 0 and index_match != len(tree_path):
         # add all children
-        for i in range (indexMatch + 1, len(treePath)):
-            if(treePath[i] not in currentParent.child):
-                currentParent.child.append(treePath[i])
+        for i in range(index_match + 1, len(tree_path)):
+            if tree_path[i] not in current_parent.child:
+                current_parent.child.append(tree_path[i])
 
 
-def _CheckDataBlocksForOverLap(blockOne, blockTwo):
-    '''
+def _check_data_blocks_for_over_lap(block_one, block_two):
+    """
     Checks whether the root path of families in the first block overlaps with the root path of any family in the second block.
     Overlap is checked from the start of the root path. Any families from block one which are not overlapping any family in\
         block two are returned.
 
-    :param blockOne: List of family tuples of type nestedFamily
-    :type blockOne: [nestedFamily]
-    :param blockTwo: List of family tuples of type nestedFamily
-    :type blockTwo: [nestedFamily]
+    :param block_one: List of family tuples of type nestedFamily
+    :type block_one: [nestedFamily]
+    :param block_two: List of family tuples of type nestedFamily
+    :type block_two: [nestedFamily]
     :return: List of family tuples of type nestedFamily
     :rtype: [nestedFamily]
-    '''
+    """
 
-    uniqueTreeNodes = []
-    for fam in blockOne:
+    unique_tree_nodes = []
+    for fam in block_one:
         match = False
-        for famUp in blockTwo:
-            if(' :: '.join(famUp.rootPath).startswith(' :: '.join(fam.rootPath))):
+        for fam_up in block_two:
+            if " :: ".join(fam_up.rootPath).startswith(" :: ".join(fam.rootPath)):
                 match = True
                 break
-        if(match == False):
-            uniqueTreeNodes.append(fam)
-    return uniqueTreeNodes
+        if match == False:
+            unique_tree_nodes.append(fam)
+    return unique_tree_nodes
+
 
-def _CullDataBlock(familyBaseNestedDataBlock):
-    '''
+def _cull_data_block(family_base_nested_data_block):
+    """
     Sorts family data blocks into a dictionary where key, from 1 onwards, is the level of nesting indicated by number of '::' in root path string.
 
     After sorting it compares adjacent blocks in the dictionary (key and key + 1) for overlaps in the root path string. Only unique families will be returned.
 
-    :param familyBaseNestedDataBlock: A list containing all nested families belonging to a single root host family.
-    :type familyBaseNestedDataBlock: [nestedFamily]
+    :param family_base_nested_data_block: A list containing all nested families belonging to a single root host family.
+    :type family_base_nested_data_block: [nestedFamily]
     :return: A list of unique families in terms of root path.
     :rtype: [nestedFamily]
-    '''
+    """
 
-    culledFamilyBaseNestedDataBlocks = []
-    dataBlocksByLength = {}
+    culled_family_base_nested_data_blocks = []
+    data_blocks_by_length = {}
     # build dic by root path length
     # start at 1 because for nesting level ( 1 based rather then 0 based )
-    for family in familyBaseNestedDataBlock:
-        if(len(family.rootPath) -1 in dataBlocksByLength):
-            dataBlocksByLength[len(family.rootPath) -1 ].append(family)
+    for family in family_base_nested_data_block:
+        if len(family.rootPath) - 1 in data_blocks_by_length:
+            data_blocks_by_length[len(family.rootPath) - 1].append(family)
         else:
-            dataBlocksByLength[len(family.rootPath)- 1 ] = [family]
-    
+            data_blocks_by_length[len(family.rootPath) - 1] = [family]
+
     # loop over dictionary and check block entries against next entry up blocks
-    for i in range(1, len(dataBlocksByLength) + 1):
+    for i in range(1, len(data_blocks_by_length) + 1):
         # last block get automatically added
-        if(i == len(dataBlocksByLength)):
-            culledFamilyBaseNestedDataBlocks = culledFamilyBaseNestedDataBlocks + dataBlocksByLength[i]
+        if i == len(data_blocks_by_length):
+            culled_family_base_nested_data_blocks = (
+                culled_family_base_nested_data_blocks + data_blocks_by_length[i]
+            )
         else:
             # check for matches in next one up
-            uniqueNodes = _CheckDataBlocksForOverLap(dataBlocksByLength[i], dataBlocksByLength[i + 1])
+            unique_nodes = _check_data_blocks_for_over_lap(
+                data_blocks_by_length[i], data_blocks_by_length[i + 1]
+            )
             # only add non overlapping blocks
-            culledFamilyBaseNestedDataBlocks = culledFamilyBaseNestedDataBlocks + uniqueNodes
-    return culledFamilyBaseNestedDataBlocks
+            culled_family_base_nested_data_blocks = (
+                culled_family_base_nested_data_blocks + unique_nodes
+            )
+    return culled_family_base_nested_data_blocks
+
 
-def _CullNestedBaseDataBlocks(overallFamilyBaseNestedData):
-    '''
-    Reduce base data families for parent / child finding purposes. Keep the nodes with the root path longes branch only.
+def _cull_nested_base_data_blocks(overall_family_base_nested_data):
+    """
+    Reduce base data families for parent / child finding purposes. Keep the nodes with the root path longest branch only.
 
     Sample:
-    
+
     famA :: famB :: famC
     famA :: famB
 
     The second of the above examples can be culled since the first contains the same information.
 
-    :param overallFamilyBaseNestedData: A list containing all nested families with the longest nesting levels per branch per host family.
-    :type overallFamilyBaseNestedData: [nestedFamily]
-    '''
+    :param overall_family_base_nested_data: A list containing all nested families with the longest nesting levels per branch per host family.
+    :type overall_family_base_nested_data: [nestedFamily]
+    """
 
-    currentRootFamName = ''
-    familyBlocks = []
+    current_root_fam_name = ""
+    family_blocks = []
     block = []
     # read families into blocks
-    for nested in overallFamilyBaseNestedData:
-        if(nested.rootPath[0] != currentRootFamName):
+    for nested in overall_family_base_nested_data:
+        if nested.rootPath[0] != current_root_fam_name:
             # read family block
-            if(len(block) > 0):
-                familyBlocks.append(block)
+            if len(block) > 0:
+                family_blocks.append(block)
                 # reset block
                 block = []
                 block.append(nested)
-                currentRootFamName = nested.rootPath[0]
+                current_root_fam_name = nested.rootPath[0]
             else:
                 block.append(nested)
-                currentRootFamName = nested.rootPath[0]
+                current_root_fam_name = nested.rootPath[0]
         else:
             block.append(nested)
-    
-    retainedFamilyBaseNestedData = []
+
+    retained_family_base_nested_data = []
     # cull data per block
-    for familyBlock in familyBlocks:
-        d = _CullDataBlock(familyBlock)
-        retainedFamilyBaseNestedData = retainedFamilyBaseNestedData + d
-        
-    return retainedFamilyBaseNestedData
+    for family_block in family_blocks:
+        d = _cull_data_block(family_block)
+        retained_family_base_nested_data = retained_family_base_nested_data + d
 
+    return retained_family_base_nested_data
 
-def FindParentsAndChildren(overallFamilyBaseRootData, overallFamilyBaseNestedData):
-    '''
+
+def find_parents_and_children(
+    overall_family_base_root_data, overall_family_base_nested_data
+):
+    """
     Loop over all root families and check if they exist in root path of any nested families.
     if so extract families higher up the root path tree as parents and families further down the root path tree as children
 
-    :param overallFamilyBaseRootData: List of tuples containing root family data.
-    :type overallFamilyBaseRootData: [rootFamily]
-    :param overallFamilyBaseNestedData: List of tuples containing nested family data.
-    :type overallFamilyBaseNestedData: [nestedFamily]
+    :param overall_family_base_root_data: List of tuples containing root family data.
+    :type overall_family_base_root_data: [rootFamily]
+    :param overall_family_base_nested_data: List of tuples containing nested family data.
+    :type overall_family_base_nested_data: [nestedFamily]
 
     :return: List of tuples containing root family data.
     :rtype: [rootFamily]
-    '''
-    
-    for i in range(len(overallFamilyBaseRootData)):
-        #print ('checking family :' , i, ' ', overallFamilyBaseRootData[i].name)
-        for nestedFam in overallFamilyBaseNestedData:
+    """
+
+    for i in range(len(overall_family_base_root_data)):
+        # print ('checking family :' , i, ' ', overall_family_base_root_data[i].name)
+        for nested_fam in overall_family_base_nested_data:
             try:
                 # get the index of the match
-                indexMatch = nestedFam.rootPath.index(overallFamilyBaseRootData[i].name)
-                if(indexMatch > 0):
-                    
-                    #print('found ', overallFamilyBaseRootData[i].name ,' in ', nestedFam.rootPath)
-                    _ExtractParentFamilies(overallFamilyBaseRootData[i], nestedFam.rootPath)
-                    
-                    _ExtractChildFamilies(overallFamilyBaseRootData[i], nestedFam.rootPath)
+                index_match = nested_fam.rootPath.index(
+                    overall_family_base_root_data[i].name
+                )
+                if index_match > 0:
+
+                    # print('found ', overall_family_base_root_data[i].name ,' in ', nested_fam.rootPath)
+                    _extract_parent_families(
+                        overall_family_base_root_data[i], nested_fam.rootPath
+                    )
+
+                    _extract_child_families(
+                        overall_family_base_root_data[i], nested_fam.rootPath
+                    )
 
-                    #print('after: ', overallFamilyBaseRootData[i].child)
+                    # print('after: ', overall_family_base_root_data[i].child)
             except:
                 pass
-    return overallFamilyBaseRootData
+    return overall_family_base_root_data
 
-def FindCircularReferences(overallFamilyBaseRootData):
-    '''
+
+def find_circular_references(overall_family_base_root_data):
+    """
     Loops over family data and returns any families which appear in circular references.
     (A family appears in their parent and child collection)
 
-    :param overallFamilyBaseRootData: List of tuples containing root family data.
-    :type overallFamilyBaseRootData: [rootFamily]
-    
+    :param overall_family_base_root_data: List of tuples containing root family data.
+    :type overall_family_base_root_data: [rootFamily]
+
     :return: List of tuples containing root family data.
     :rtype: [rootFamily]
-    '''
+    """
 
-    circularReferences = []
+    circular_references = []
     # loop over all families and check whether there are any families in both the parent as well as child collection
-    for family in overallFamilyBaseRootData:
-        for parentFamily in family.parent:
-            if (parentFamily in family.child):
-                circularReferences.append(family)
-    return circularReferences
+    for family in overall_family_base_root_data:
+        for parent_family in family.parent:
+            if parent_family in family.child:
+                circular_references.append(family)
+    return circular_references
 
-def CheckFamiliesHaveCircularReferences(familyBaseDataReportFilePath):
-    '''
+
+def check_families_have_circular_references(family_base_data_report_file_path):
+    """
     Processes a family base data report and identifies any families which contain circular reference.
 
     Makes use of multithreading when more then 2 cores are present.
 
-    :param familyBaseDataReportFilePath: Fully qualified file path to family base data report file. 
-    :type familyBaseDataReportFilePath: str
+    :param family_base_data_report_file_path: Fully qualified file path to family base data report file.
+    :type family_base_data_report_file_path: str
 
-    :return: 
+    :return:
         Result class instance.
 
         - result.status. True if circular referencing file was written successfully, otherwise False.
         - result.message will contain the summary messages of the process including time stamps.
         - result.result empty list
-        
+
         On exception:
-        
+
         - result.status (bool) will be False.
         - result.message will contain generic exception message.
         - result.result will be empty
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     # set up a timer
-    tProcess = Timer()
-    tProcess.start()
+    t_process = Timer()
+    t_process.start()
 
-    returnValue = res.Result()
-    # read overall family base data and nested data from file 
-    overallFamilyBaseRootData, overallFamilyBaseNestedData = rFamBaseDataUtils.ReadOverallFamilyDataList(familyBaseDataReportFilePath)
-    returnValue.AppendMessage(tProcess.stop() +  ' Read overall family base data report. ' + str(len(overallFamilyBaseRootData)) + ' root entries found and '\
-        + str(len(overallFamilyBaseNestedData)) + ' nested entries found.')
-    tProcess.start()
+    return_value = res.Result()
+    # read overall family base data and nested data from file
+    (
+        overall_family_base_root_data,
+        overall_family_base_nested_data,
+    ) = rFamBaseDataUtils.read_overall_family_data_list(
+        family_base_data_report_file_path
+    )
+    return_value.append_message(
+        "{} Read overall family base data report. {} root entries found and {} nested entries found.".format(
+            t_process.stop(),
+            len(overall_family_base_root_data, len(overall_family_base_nested_data)),
+        )
+    )
+    t_process.start()
 
-    before = len(overallFamilyBaseNestedData)
+    before = len(overall_family_base_nested_data)
     # reduce workload by culling not needed nested family data
-    overallFamilyBaseNestedData = _CullNestedBaseDataBlocks(overallFamilyBaseNestedData)
-    returnValue.AppendMessage(tProcess.stop() +  ' culled nested family base data from : ' + str(before) +' to: ' + str(len(overallFamilyBaseNestedData)) + ' families.' )
-    tProcess.start()
+    overall_family_base_nested_data = _cull_nested_base_data_blocks(
+        overall_family_base_nested_data
+    )
+    return_value.append_message(
+        " {} culled nested family base data from : {} to: {} families.".format(
+            t_process.stop(), before
+        ),
+        len(overall_family_base_nested_data),
+    )
+    t_process.start()
 
     # set up some multithreading
-    coreCount = int(os.environ['NUMBER_OF_PROCESSORS'])
-    if (coreCount > 2):
-        returnValue.AppendMessage('cores: '  + str(coreCount))
+    core_count = int(os.environ["NUMBER_OF_PROCESSORS"])
+    if core_count > 2:
+        return_value.append_message("cores: ".format(core_count))
         # leave some room for other processes
-        coreCount = coreCount - 1
-        chunkSize = len(overallFamilyBaseRootData)/coreCount
+        core_count = core_count - 1
+        chunk_size = len(overall_family_base_root_data) / core_count
         threads = []
         # set up threads
-        for i in range(coreCount):
-            t = threading.Thread(target=FindParentsAndChildren, args=(overallFamilyBaseRootData[i*chunkSize:(i+1) * chunkSize],overallFamilyBaseNestedData))
+        for i in range(core_count):
+            t = threading.Thread(
+                target=find_parents_and_children,
+                args=(
+                    overall_family_base_root_data[
+                        i * chunk_size : (i + 1) * chunk_size
+                    ],
+                    overall_family_base_nested_data,
+                ),
+            )
             threads.append(t)
         # start up threads
         for t in threads:
             t.start()
         # wait for results
         for t in threads:
             t.join()
     else:
         # find parents and children
-        overallFamilyBaseRootData = FindParentsAndChildren(overallFamilyBaseRootData, overallFamilyBaseNestedData)
-    
-    returnValue.AppendMessage(tProcess.stop() +  ' Populated parents and children properties of: ' + str(len(overallFamilyBaseRootData)) +' root families.' )
-    tProcess.start()
+        overall_family_base_root_data = find_parents_and_children(
+            overall_family_base_root_data, overall_family_base_nested_data
+        )
+
+    return_value.append_message(
+        "{} Populated parents and children properties of: {} root families".format(
+            t_process.stop(), len(overall_family_base_root_data)
+        )
+    )
+    t_process.start()
 
     # identify circular references
-    circularReferences = FindCircularReferences(overallFamilyBaseRootData)
-    returnValue.AppendMessage(tProcess.stop() +  ' Found ' + str(len(circularReferences)) +' circular references in families.' )
-    if(len(circularReferences) > 0):
-        returnValue.result = circularReferences
-    return returnValue
+    circular_references = find_circular_references(overall_family_base_root_data)
+    return_value.append_message(
+        "{} Found: {} circular references in families.".format(
+            t_process.stop(), len(circular_references)
+        )
+    )
+    if len(circular_references) > 0:
+        return_value.result = circular_references
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyBaseDataAnalysisMissingFamilies.py` & `DuHast-0.0.7/src/duHast/Revit/Family/Data/family_base_data_missing_families.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Family Base data analysis module containing functions to find missing families.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 A missing family is a family which is not present in the family base data report as a root family but present as a nested family.
 
 Algorithm description:
@@ -17,120 +17,128 @@
     - loop over root families 
         - check if nested family exists in root families ( by name and category)
             - no
             - add to missing families list
             - stop processing since one match is enough per missing family
 - write out missing families data ( host family filepath,)
 
-'''
+"""
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-#from collections import namedtuple
+# from collections import namedtuple
+
+from duHast.Revit.Family.Data import family_base_data_utils as rFamBaseDataUtils
+from duHast.Utilities.Objects.timer import Timer
+from duHast.Utilities.Objects import result as res
 
-from duHast.APISamples import RevitFamilyBaseDataUtils as rFamBaseDataUtils
-from duHast.Utilities.timer import Timer
-from duHast.Utilities import Result as res
-from duHast.Utilities import Utility as util
 
-def _BuildUniqueNestedFamilyDic(overallFamilyBaseNestedData):
-    '''
+def _build_unique_nested_family_dic(overallFamilyBaseNestedData):
+    """
     Builds a dictionary containing unique nested families only. Key is the family name and category concatenated.
 
     :param overallFamilyBaseNestedData: List of tuples containing nested family data.
     :type overallFamilyBaseNestedData: [nestedFamily]
-    
+
     :return: A dictionary where:
-    
+
         - Key is the family name and category concatenated.
         - value is a tuple representing one instance of the nested family data.
     :rtype:{ str : nestedFamily }
-    '''
-    
+    """
+
     uniqueDic = {}
 
     for nested in overallFamilyBaseNestedData:
         keyNew = nested.name + nested.category
-        if(keyNew not in uniqueDic):
+        if keyNew not in uniqueDic:
             uniqueDic[keyNew] = nested
-    
+
     return uniqueDic
 
-def _checkNestedAgainstRootFamilies(uniqNestedDictionary, overallFamilyBaseRootData):
-    '''
+
+def _check_nested_against_root_families(
+    uniqNestedDictionary, overallFamilyBaseRootData
+):
+    """
     Compared a dictionary containing tuples containing nested family data against list of root family data.
     Any nested family without a match in the root family data list will be returned (missing from list).
 
     :param uniqNestedDictionary: A dictionary where:
-    
+
         - Key is the family name and category concatenated.
         - value is a tuple representing one instance of the nested family data.
 
     :type uniqNestedDictionary: { str : nestedFamily }
     :param overallFamilyBaseRootData: List of tuples containing root family data.
     :type overallFamilyBaseRootData: [rootFamily]
-    
+
     :return: List of tuples containing nested family data.
     :rtype: [nestedFamily]
-    '''
+    """
 
     missingFamilies = []
     for nestedId, nestedFam in uniqNestedDictionary.items():
         match = False
         for baseRootFam in overallFamilyBaseRootData:
-            if (nestedFam.name == baseRootFam.name and nestedFam.category == baseRootFam.category):
+            if (
+                nestedFam.name == baseRootFam.name
+                and nestedFam.category == baseRootFam.category
+            ):
                 match = True
                 break
-        if (match == False):
+        if match == False:
             missingFamilies.append(nestedFam)
     return missingFamilies
 
-def _getUniqueNestedFamilies(overallFamilyBaseNestedData):
-    '''
+
+def _get_unique_nested_families(overallFamilyBaseNestedData):
+    """
     Loops over family nested base data and creates a unique list of nested families based on name and category.
     This is done to make search faster (reduce the to be searched data set)
 
     :param overallFamilyBaseNestedData: List of tuples containing nested family data.
     :type overallFamilyBaseNestedData: [nestedFamily]
     :return: Unique list of tuples containing nested family data.
     :rtype: [nestedFamily]
-    '''
+    """
 
     uniqueNestedFamiliesCompare = []
     uniqueNestedFamilies = []
     for nestedFam in overallFamilyBaseNestedData:
-        if (nestedFam.name + nestedFam.category not in uniqueNestedFamiliesCompare):
+        if nestedFam.name + nestedFam.category not in uniqueNestedFamiliesCompare:
             uniqueNestedFamilies.append(nestedFam)
             uniqueNestedFamiliesCompare.append(nestedFam.name + nestedFam.category)
 
     return uniqueNestedFamilies
 
-def CheckFamiliesMissingFromLibrary(familyBaseDataReportFilePath):
-    '''
+
+def check_families_missing_from_library(familyBaseDataReportFilePath):
+    """
     Processes a family base data report and identifies any nested families which have not been processed as a root family\
         and therefore do not exist in the library.
     
     :param familyBaseDataReportFilePath: Fully qualified file path to family base data report file. 
     :type familyBaseDataReportFilePath: str
     
     :return: 
@@ -143,99 +151,153 @@
         On exception:
         
         - result.status (bool) will be False.
         - result.message will contain generic exception message.
         - result.result will be empty
 
     :rtype: :class:`.Result`
-    '''
+    """
     returnValue = res.Result()
     try:
         # set up a timer
         tProcess = Timer()
         tProcess.start()
 
-    
-        # read overall family base data from file 
-        overallFamilyBaseRootData, overallFamilyBaseNestedData = rFamBaseDataUtils.ReadOverallFamilyDataList(familyBaseDataReportFilePath)
-        returnValue.AppendMessage(tProcess.stop() +  ' Read overall family base data report. ' + str(len(overallFamilyBaseRootData)) + ' root entries found and '\
-            + str(len(overallFamilyBaseNestedData)) + ' nested entries found.')
-    
+        # read overall family base data from file
+        (
+            overallFamilyBaseRootData,
+            overallFamilyBaseNestedData,
+        ) = rFamBaseDataUtils.read_overall_family_data_list(
+            familyBaseDataReportFilePath
+        )
+        returnValue.append_message(
+            "{} Read overall family base data report. {} root entries found and {} nested entries found.".format(
+                tProcess.stop(),
+                len(overallFamilyBaseRootData),
+                len(overallFamilyBaseNestedData),
+            )
+        )
+
         tProcess.start()
         # get a list of unique families from the nested family data
-        uniqueFamilyBaseNestedData = _getUniqueNestedFamilies(overallFamilyBaseNestedData)
-        returnValue.AppendMessage(tProcess.stop() +  ' culled nested family base data from : ' + str(len(overallFamilyBaseNestedData)) +' to: ' + str(len(uniqueFamilyBaseNestedData )) + ' families.' )
+        uniqueFamilyBaseNestedData = _get_unique_nested_families(
+            overallFamilyBaseNestedData
+        )
+        returnValue.append_message(
+            "{} Culled nested family base data from : {} to: {} families".format(
+                tProcess.stop(), len(overallFamilyBaseNestedData)
+            ),
+            len(uniqueFamilyBaseNestedData),
+        )
 
         tProcess.start()
         # read over nested data and built a list of unique families ( name + category )
-        uniqueDic = _BuildUniqueNestedFamilyDic(uniqueFamilyBaseNestedData)
-        returnValue.AppendMessage(tProcess.stop() + ' found unique nested families ['+ str(len(uniqueDic))+']')
+        uniqueDic = _build_unique_nested_family_dic(uniqueFamilyBaseNestedData)
+        returnValue.append_message(
+            "{} Found unique nested families [{}]".format(
+                tProcess.stop(), len(uniqueDic)
+            )
+        )
 
         tProcess.start()
         # identify missing families in unique list of nested families
-        missingFamilies = _checkNestedAgainstRootFamilies(uniqueDic, overallFamilyBaseRootData)
-        returnValue.AppendMessage(tProcess.stop() +  ' Found ' + str(len(missingFamilies)) +' missing families.' )
-        if(len(missingFamilies) > 0):
+        missingFamilies = _check_nested_against_root_families(
+            uniqueDic, overallFamilyBaseRootData
+        )
+        returnValue.append_message(
+            "{} Found: {} missing families.".format(
+                tProcess.stop(), len(missingFamilies)
+            )
+        )
+        if len(missingFamilies) > 0:
             returnValue.result = missingFamilies
     except Exception as e:
-        returnValue.UpdateSep(False, 'Failed to retrieve missing families with exception: ' + str(e))
+        returnValue.update_sep(
+            False, "Failed to retrieve missing families with exception: {}".format(e)
+        )
     return returnValue
 
+
 # ----------------------------missing families: direct host files -----------------------------------------
 
-def FindMissingFamiliesDirectHostFamilies (familyBaseDataReportFilePath, missingFamilies):
-    '''
+
+def find_missing_families_direct_host_families(
+    familyBaseDataReportFilePath, missingFamilies
+):
+    """
     Returns a list of root family tuples which represent the direct parents (host families) of the missing families.
 
     :param missingFamilies: A list of tuple containing nested family data representing missing families(no base root family entry)
     :type missingFamilies: [nestedFamily]
-    :param familyBaseDataReportFilePath: Fully qualified file path to family base data report file. 
+    :param familyBaseDataReportFilePath: Fully qualified file path to family base data report file.
     :type familyBaseDataReportFilePath: str
-    
-    :return: 
+
+    :return:
         Result class instance.
 
         - result.status. True if host families of missing families where found without an exception occurring.
         - result.message will contain the summary messages of the process including time stamps.
         - result.result [rootFamily]
-        
+
         On exception:
-        
+
         - result.status (bool) will be False.
         - result.message will contain generic exception message.
         - result.result will be empty
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     # loop over missing families
     # loop over base nested data
     #   - check if missing fam is in root path (name and category) if so:
     #   - get the direct parent (make sure missing family isn't first entry!)
     #   - check if direct parent is already in dictionary (key is name + category) ? if not:
     #       - add direct parent to dictionary
     #
     # loop over direct host data:
     #   - loop over root fam data and check for match in name and category; If so:
-    #       - add to root family data to be returned. 
+    #       - add to root family data to be returned.
 
     returnValue = res.Result()
     try:
         # set up a timer
         tProcess = Timer()
         tProcess.start()
 
         returnValue = res.Result()
-        # read overall family base data from file 
-        overallFamilyBaseRootData, overallFamilyBaseNestedData = rFamBaseDataUtils.ReadOverallFamilyDataList(familyBaseDataReportFilePath)
-        returnValue.AppendMessage(tProcess.stop() +  ' Read overall family base data report. ' + str(len(overallFamilyBaseRootData)) + ' root entries found and '\
-            + str(len(overallFamilyBaseNestedData)) + ' nested entries found.')
-    
+        # read overall family base data from file
+        (
+            overallFamilyBaseRootData,
+            overallFamilyBaseNestedData,
+        ) = rFamBaseDataUtils.read_overall_family_data_list(
+            familyBaseDataReportFilePath
+        )
+        returnValue.append_message(
+            "{} Read overall family base data report. {} root entries found and {} nested entries found.".format(
+                tProcess.stop(), len(overallFamilyBaseRootData)
+            ),
+            len(overallFamilyBaseNestedData),
+        )
+
         tProcess.start()
-        hostFamilies = rFamBaseDataUtils.FindAllDirectHostFamilies(missingFamilies, overallFamilyBaseNestedData)
+        hostFamilies = rFamBaseDataUtils.find_all_direct_host_families(
+            missingFamilies, overallFamilyBaseNestedData
+        )
         # get the root families from host family data
-        rootHosts = rFamBaseDataUtils.FindRootFamsFromHosts(hostFamilies, overallFamilyBaseRootData)
+        rootHosts = rFamBaseDataUtils.find_root_families_from_hosts(
+            hostFamilies, overallFamilyBaseRootData
+        )
         returnValue.result = rootHosts
-        returnValue.AppendMessage(tProcess.stop() +  ' Found direct host families of missing families: ' + str(len(rootHosts)))
-    except  Exception as e:
-        returnValue.UpdateSep(False, 'Failed to retrieve host families of missing families with exception: ' + str(e))
+        returnValue.append_message(
+            "{} Found direct host families of missing families: {}".format(
+                tProcess.stop(), len(rootHosts)
+            )
+        )
+    except Exception as e:
+        returnValue.update_sep(
+            False,
+            "Failed to retrieve host families of missing families with exception: ".format(
+                e
+            ),
+        )
     return returnValue
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyDataCollector.py` & `DuHast-0.0.7/src/duHast/Revit/LinePattern/line_pattern_data_processor.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,196 +1,164 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Family data collector class.
+Family line pattern data processor class.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-
-- Collects data from current family document and then recursively from any nested family.
-
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-from duHast.Utilities import Result as res
-# import Autodesk
-import Autodesk.Revit.DB as rdb
 
-class RevitFamilyDataCollector():
-
-    def __init__(self, dataProcessors):
-        '''
-        Class constructor taking a list of processor instances as argument.
-
-        :param dataProcessors: List of processor instances
-        :type dataProcessors: [IFamilyProcessor]
-        '''
-
-        self.dataProcessors = dataProcessors
-    
-    def _getFamilyIds(self,doc):
-        '''
-        Get all loadable family ids in file.
+from duHast.Revit.Family.Data.ifamily_processor import IFamilyProcessor
+from duHast.Revit.LinePattern import line_pattern_data as rLinePatData
+from duHast.Revit.Family.Data import ifamily_data as IFamData
+from duHast.Utilities.Objects import result as res
+
+
+class LinePatternProcessor(IFamilyProcessor):
+    def __init__(self, pre_actions=None, post_actions=None):
+        """
+        Class constructor.
+        """
+
+        # setup report header
+        string_report_headers = [
+            IFamData.ROOT,
+            IFamData.ROOT_CATEGORY,
+            IFamData.FAMILY_NAME,
+            IFamData.FAMILY_FILE_PATH,
+            IFamData.USAGE_COUNTER,
+            IFamData.USED_BY,
+            rLinePatData.PATTERN_NAME,
+            rLinePatData.PATTERN_ID,
+        ]
+
+        # store data type  in base class
+        super(LinePatternProcessor, self).__init__(
+            pre_actions=pre_actions,
+            post_actions=[self._post_action_update_used_line_patterns],
+            data_type="LinePattern",
+            string_report_headers=string_report_headers,
+        )
+
+        # set default post action to updated line patterns used in root processor with any line patterns found in nested
+        # families
+        # self.postActions = [self._postActionUpdateUsedLinePatterns]
+        # add any other post actions
+        if post_actions != None:
+            for post_action in post_actions:
+                self.post_actions.append(post_action)
+
+    def process(self, doc, root_path, root_category_path):
+        """
+        Calls processor instance with the document and root path provided and adds processor instance to class property .data
 
         :param doc: Current family document.
         :type doc: Autodesk.Revit.DB.Document
-        :return: list of family ids
-        :rtype: [Autodesk.Revit.DB.ElementId]
-        '''
-
-        familyIds = []
-        col = rdb.FilteredElementCollector(doc).OfClass(rdb.FamilySymbol) 
-        # get families from symbols and filter out in place families
-        for famSymbol in col:
-            if (famSymbol.Family.Id not in familyIds and famSymbol.Family.IsInPlace == False):
-                familyIds.append(famSymbol.Family.Id)
-        return familyIds
-
-    def _dive(self, doc, rootName, rootCategory, isRoot = False):
-        '''
-        Loops recursively over each family nested into root family document and and calls processor instance\
-             with the current family document.
-
-        :param doc: The family document. 
-        :type doc: Autodesk.Revit.DB.Document
-        :param rootName: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
-            This includes the actual family name as the last node.
-        :type rootName: str
-        :param isRoot: Indicates whether document is that of the root family, defaults to False
-        :type isRoot: bool, optional
-        '''
-
-        returnValue = res.Result()
-        # only process current doc if not the root family
-        # that family is processed already
-        if(isRoot == False):
-            for pro in self.dataProcessors:
-                try:
-                    pro.process(doc, rootName, rootCategory)
-                    returnValue.AppendMessage('Processor [' + pro.dataType + '] of family: ' + str(doc.Title) + ' [OK]')
-                except Exception as e:
-                    returnValue.UpdateSep(False, 'Processor [' + pro.dataType + '] of family: ' + str(doc.Title) + ' [EXCEPTION] ' + str(e))
-        
-        # check if family doc 
-        if(doc.IsFamilyDocument):
-            # get any nested families
-            familyIds = self._getFamilyIds(doc)
-            # if there are any nested families open those for processing
-            if(len(familyIds) > 0):
-                for familyId in familyIds:
-                    family = doc.GetElement(familyId)
-                    try:
-                        if(family.IsEditable and family.IsValidObject):
-                            familyDoc = doc.EditFamily(family)
-                            famName = family.Name
-                            # strip .rfa of name
-                            if(famName.lower().endswith('.rfa')):
-                                famName = famName[:-4]
-                            # get category
-                            famCategoryName = family.FamilyCategory.Name
-                            # go recursive
-                            diveResult = self._dive(
-                                familyDoc, 
-                                rootName + ' :: ' + famName,
-                                rootCategory + ' :: ' + famCategoryName
-                            )
-                            returnValue.Update(diveResult)
-                    except Exception as e:
-                        message = ''
-                        if(family != None):
-                            message = 'An exception occurred when opening family ' + rdb.Element.Name.GetValue(family) + '. Exception: ' + str(e)
-                        else:
-                            message = 'An exception occurred when attempting the get family element by id:' + str(familyId) + '. Exception: ' + str(e)
-                        returnValue.UpdateSep(False, message)
-            else:
-                # only close any nested family document...not the root one
-                # since that is closed by batch processor!
-                if(isRoot == False):
-                    try:
-                        # no more families found. Close the active doc
-                        doc.Close(False)
-                    except Exception as e:
-                        message = ''
-                        if(doc != None):
-                            message = 'An exception occurred when closing document: ' + doc.Title + '. Exception: ' + str(e)
-                        else:
-                            message = 'An exception occurred when closing document: ' + str(e)
-                        returnValue.UpdateSep(False, message)
-        return returnValue
-
-    def processFamily(self, doc, rootName, rootCategory):
-        '''
-        Entry point for recursive family looper.
-
-        Processes root family as well as actions any post processing.
-
-        :param doc: The family document. 
-        :type doc: Autodesk.Revit.DB.Document
-        :param rootName: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
+        :param rootPath: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
             This includes the actual family name as the last node.
-        :type rootName: str
-        :param rootCategory: The path of the nested family category in a tree: rootFamilyCategory::nestedFamilyOneCategory::nestedFamilyTwoCategory\
+        :type rootPath: str
+        :param rootCategoryPath: The categroy path of the nested family in a tree: rootFamilyCategory::nestedFamilyOneCategory::nestedFamilyTwoCategory\
             This includes the actual family category as the last node.
-        :type rootCategory: str
+        :type rootCategoryPath: str
+        """
 
-        :return: 
-            Result class instance.
-            
-            - .result = True if all data processor instances ran without an exception. Otherwise False.
-            - .message will contain each processor type and its processing status'
-        
-        :rtype: :class:`.Result`
-        '''
-
-        returnValue = res.Result()
-
-        #TODO:
-        # action any pre processing actions
-        # loop over fam processor instances and process family with each of them
-        for pro in self.dataProcessors:
-            try:
-                preActionResult =  pro.preProcessActions(doc)
-                returnValue.Update(preActionResult)
-            except Exception as e:
-                returnValue.UpdateSep(False, 'PreProcessor [' + pro.dataType + '] of family: ' + str(doc.Title) + ' [EXCEPTION] ' + str(e))
-
-        # loop over fam processor instances and process family with each of them
-        for pro in self.dataProcessors:
-            try:
-                pro.process(doc, rootName, rootCategory)
-                returnValue.AppendMessage('Processor [' + pro.dataType + '] of family: ' + str(doc.Title) + ' [OK]')
-            except Exception as e:
-                returnValue.UpdateSep(False, 'Processor [' + pro.dataType + '] of family: ' + str(doc.Title) + ' [EXCEPTION] ' + str(e))
-        
-        # check out any nested families
-        diveResult = self._dive(doc, rootName, rootCategory, True)
-        returnValue.Update(diveResult)
-        
-        #TODO:
-        # action any post processing actions
-        # loop over fam processor instances and process family with each of them
-        for pro in self.dataProcessors:
-            try:
-                proActionResult =  pro.postProcessActions(doc)
-                returnValue.Update(proActionResult)
-            except Exception as e:
-                returnValue.UpdateSep(False, 'PostProcessor [' + pro.dataType + '] of family: ' + str(doc.Title) + ' [EXCEPTION] ' + str(e))
-
-        return returnValue
+        dummy = rLinePatData.LinePatternData(
+            root_path, root_category_path, self.data_type
+        )
+        dummy.process(doc)
+        self.data.append(dummy)
+
+    def _is_sub_line_pattern_present(
+        self, root_family_data, nested_family_line_pattern
+    ):
+        match = None
+        for root_fam in root_family_data:
+            if (
+                root_fam[rLinePatData.PATTERN_NAME]
+                == nested_family_line_pattern[rLinePatData.PATTERN_NAME]
+            ):
+                match = root_fam
+                break
+        return match
+
+    def _update_root_family_data(self, root_family_data, nested_families_line_patterns):
+        # loop over nested family line pattern data
+        for nested_line_pattern in nested_families_line_patterns:
+            # check if pattern is already in root family
+            matching_root_fam_pattern = self._is_sub_line_pattern_present(
+                root_family_data, nested_line_pattern
+            )
+            if matching_root_fam_pattern != None:
+                # update used by list
+                if (
+                    nested_line_pattern[rLinePatData.PATTERN_NAME]
+                    not in matching_root_fam_pattern[IFamData.USED_BY]
+                ):
+                    # add the root path to the used by list for ease of identification of the origin of this pattern usage
+                    matching_root_fam_pattern[IFamData.USED_BY].append(
+                        {
+                            rLinePatData.PATTERN_ID: nested_line_pattern[
+                                rLinePatData.PATTERN_ID
+                            ],
+                            IFamData.ROOT: nested_line_pattern[IFamData.ROOT],
+                        }
+                    )
+                    # update used by counter
+                    matching_root_fam_pattern[IFamData.USAGE_COUNTER] = (
+                        matching_root_fam_pattern[IFamData.USAGE_COUNTER] + 1
+                    )
+            else:
+                pass
+                # nothing to do if that pattern has not been reported to start off with
+                # this patter could, for example, belong to the section marker family present in most 3d families
+
+    def _get_used_line_patterns(self, data):
+        used_line_patterns = []
+        for d in data:
+            if d[IFamData.USAGE_COUNTER] > 0:
+                used_line_patterns.append(d)
+        return used_line_patterns
+
+    def _post_action_update_used_line_patterns(self, doc):
+        return_value = res.Result()
+        try:
+            # find all line patterns of nested families
+            nested_family_data = self._find_nested_families_data()
+            # get used sub categories from nested data
+            nested_family_used_line_patterns = self._get_used_line_patterns(
+                nested_family_data
+            )
+            # update root family data only
+            rootFamilyData = self._find_root_family_data()
+            # update root processor data as required
+            self._update_root_family_data(
+                rootFamilyData, nested_family_used_line_patterns
+            )
+            return_value.update_sep(
+                True, "Post Action Update line pattern data successful completed."
+            )
+        except Exception as e:
+            return_value.update_sep(
+                False,
+                "Post Action Update line pattern data failed with exception: " + str(e),
+            )
+        return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyLoadOption.py` & `DuHast-0.0.7/src/duHast/Revit/Family/family_load_option.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,48 +1,50 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 This class is the default implementation for family load call backs.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 
 import clr
 
 import Autodesk.Revit.DB as rdb
 
-class FamilyLoadOption(rdb.IFamilyLoadOptions):
 
-	def OnFamilyFound(self, familyInUse, overwriteParameterValues):
-		'''
-		Defines behavior when a family is found in the model.
-
-		Overwrite parameter values is set to True.
-
-		:param familyInUse: _description_
-		:type familyInUse: _type_
-		:param overwriteParameterValues: _description_
-		:type overwriteParameterValues: _type_
-		:return: True
-		:rtype: bool
-		'''
-		overwriteParameterValues = True
-		return True
-
-	def OnSharedFamilyFound(self, sharedFamily, familyInUse, source, overwriteParameterValues):
-		'''
-		Defines behavior when a shared family is found in the model.
-		
-		Overwrite parameter values is set to True. In case of any shared sub components already in the model but different in family loaded, the project version will be used.
-
-		:param sharedFamily: _description_
-		:type sharedFamily: _type_
-		:param familyInUse: _description_
-		:type familyInUse: _type_
-		:param source: _description_
-		:type source: _type_
-		:param overwriteParameterValues: _description_
-		:type overwriteParameterValues: _type_
-		:return: True
-		:rtype: bool
-		'''
-		source = rdb.FamilySource.Project
-		overwriteParameterValues = True
-		return True
+class FamilyLoadOption(rdb.IFamilyLoadOptions):
+    def OnFamilyFound(self, familyInUse, overwriteParameterValues):
+        """
+        Defines behavior when a family is found in the model.
+
+        Overwrite parameter values is set to True.
+
+        :param familyInUse: _description_
+        :type familyInUse: _type_
+        :param overwriteParameterValues: _description_
+        :type overwriteParameterValues: _type_
+        :return: True
+        :rtype: bool
+        """
+        overwriteParameterValues = True
+        return True
+
+    def OnSharedFamilyFound(
+        self, sharedFamily, familyInUse, source, overwriteParameterValues
+    ):
+        """
+        Defines behavior when a shared family is found in the model.
+
+        Overwrite parameter values is set to True. In case of any shared sub components already in the model but different in family loaded, the project version will be used.
+
+        :param sharedFamily: _description_
+        :type sharedFamily: _type_
+        :param familyInUse: _description_
+        :type familyInUse: _type_
+        :param source: _description_
+        :type source: _type_
+        :param overwriteParameterValues: _description_
+        :type overwriteParameterValues: _type_
+        :return: True
+        :rtype: bool
+        """
+        source = rdb.FamilySource.Project
+        overwriteParameterValues = True
+        return True
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyParameterUtils.py` & `DuHast-0.0.7/src/duHast/Revit/Family/family_parameter_utils.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,100 +1,128 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Revit families parameter helper functions.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2020  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
 import System
 
 # import common library
 # utility functions for most commonly used Revit API tasks
-from duHast.APISamples import RevitTransaction as rTran
+from duHast.Revit.Common import transaction as rTran
+
 # class used for stats reporting
-from duHast.Utilities import Result as res
+from duHast.Utilities.Objects import result as res
 
 # import Autodesk Revit DataBase namespace
 import Autodesk.Revit.DB as rdb
 
-def SetFamilyParameterValueByStorageType(paramW, manager, value):
-    returnValue = res.Result()
+
+def set_family_parameter_value_by_storage_type(param_w, manager, value):
+    return_value = res.Result()
     try:
-        if(paramW.StorageType == rdb.StorageType.Double):
+        if param_w.StorageType == rdb.StorageType.Double:
             # THIS IS THE KEY:  Use SetValueString instead of Set.  Set requires your data to be in
-            # whatever internal units of measure Revit uses. SetValueString expects your value to 
-            # be in whatever the current DisplayUnitType (units of measure) the document is set to 
+            # whatever internal units of measure Revit uses. SetValueString expects your value to
+            # be in whatever the current DisplayUnitType (units of measure) the document is set to
             # for the UnitType associated with the parameter.
             #
             # So SetValueString is basically how the Revit GUI works.
-            manager.SetValueString(paramW, value)
-            returnValue.UpdateSep(True, 'Updated '+ paramW.Definition.Name + ' to value: ' + str(value))
-        elif(paramW.StorageType == rdb.StorageType.ElementId):
-            manager.Set(paramW, value)
-            returnValue.UpdateSep(True, 'Updated '+ paramW.Definition.Name + ' to value: ' + str(value))
-        elif(paramW.StorageType == rdb.StorageType.Integer):
-            manager.Set(paramW, value)
-            returnValue.UpdateSep(True, 'Updated '+ paramW.Definition.Name + ' to value: ' + str(value))
-        elif(paramW.StorageType == rdb.StorageType.String):
-            manager.Set(paramW, value)
-            returnValue.UpdateSep(True, 'Updated '+ paramW.Definition.Name + ' to value: ' + value)
+            manager.SetValueString(param_w, value)
+            return_value.update_sep(
+                True, "Updated {} to value: {}".format(param_w.Definition.Name, value)
+            )
+        elif param_w.StorageType == rdb.StorageType.ElementId:
+            manager.Set(param_w, value)
+            return_value.update_sep(
+                True, "Updated {} to value: {}".format(param_w.Definition.Name, value)
+            )
+        elif param_w.StorageType == rdb.StorageType.Integer:
+            manager.Set(param_w, value)
+            return_value.update_sep(
+                True, "Updated {} to value: {}".format(param_w.Definition.Name, value)
+            )
+        elif param_w.StorageType == rdb.StorageType.String:
+            manager.Set(param_w, value)
+            return_value.update_sep(
+                True, "Updated {} to value: {}".format(param_w.Definition.Name, value)
+            )
         else:
-            returnValue.UpdateSep(False, 'Parameter storage type is not supported!')
-        
+            return_value.update_sep(False, "Parameter storage type is not supported!")
+
     except Exception as e:
-        returnValue.UpdateSep(False, 'failed to set parameter value with exception: '+ str(e))
-    return returnValue
+        return_value.update_sep(
+            False, "failed to set parameter value with exception: {}".format(e)
+        )
+    return return_value
 
-def SetFamilyParameterValue(doc, manager, famPara, value):
-    #get the parameter
-    paramW = manager.get_Parameter(famPara.Definition.Name)
+
+def set_family_parameter_value(doc, manager, fam_para, value):
+    # get the parameter
+    param_w = manager.get_Parameter(fam_para.Definition.Name)
     # set-up action to be executed in transaction
     def action():
-        actionReturnValue = res.Result()
+        action_return_value = res.Result()
         try:
             # attempt to change parameter value
-            actionReturnValue = SetFamilyParameterValueByStorageType(paramW, manager, value)
+            action_return_value = set_family_parameter_value_by_storage_type(
+                param_w, manager, value
+            )
         except Exception as e:
-            actionReturnValue.status = False
-            actionReturnValue.message = famPara.Definition.Name + ' : Failed to set parameter value: with exception: ' + str(e)
-        return actionReturnValue
+            action_return_value.status = False
+            action_return_value.message = (
+                fam_para.Definition.Name
+                + " : Failed to set parameter value: with exception: "
+                + str(e)
+            )
+        return action_return_value
+
     transaction = rdb.Transaction(doc, "Setting parameter value")
-    returnValue = rTran.in_transaction(transaction, action)
-    return returnValue
+    return_value = rTran.in_transaction(transaction, action)
+    return return_value
 
-def SetParameterFormula(doc, manager, famPara, formula):
+
+def set_parameter_formula(doc, manager, fam_para, formula):
     def action():
-        actionReturnValue = res.Result()
+        action_return_value = res.Result()
         try:
             # set parameter formula
-            manager.SetFormula(famPara, formula)
-            actionReturnValue.message = famPara.Definition.Name + ' : parameter formulas successfully set.'
-            actionReturnValue.result.append(famPara)
+            manager.SetFormula(fam_para, formula)
+            action_return_value.message = (
+                fam_para.Definition.Name + " : parameter formulas successfully set."
+            )
+            action_return_value.result.append(fam_para)
         except Exception as e:
-            actionReturnValue.status = False
-            actionReturnValue.message = famPara.Definition.Name + ' : Failed to set parameter formula: with exception: ' + str(e)
-        return actionReturnValue
+            action_return_value.status = False
+            action_return_value.message = (
+                fam_para.Definition.Name
+                + " : Failed to set parameter formula: with exception: "
+                + str(e)
+            )
+        return action_return_value
+
     transaction = rdb.Transaction(doc, "Setting parameter formula")
-    returnValue = rTran.in_transaction(transaction, action)
-    return returnValue
+    return_value = rTran.in_transaction(transaction, action)
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyReloadAdvancedUtils.py` & `DuHast-0.0.7/src/duHast/Revit/Family/Data/family_reload_advanced_utils.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,174 +1,180 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Reload using advanced tools collection.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 This module provides utility functions to read and write reload task lists for the Revit Batch Processor.
 
-'''
+"""
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 from collections import namedtuple
 
-from duHast.Utilities.timer import Timer
-from duHast.Utilities import Result as res
-from duHast.Utilities import Utility as util
-from duHast.APISamples import RevitFamilyBaseDataUtils as rFamBaseDataUtils
+from duHast.Utilities import (
+    files_csv as fileCSV,
+    files_get as fileGet,
+    files_io as fileIO,
+    files_tab as fileTab,
+)
 
 # tuples containing base family data and changed family data read from files
-changedFamily = namedtuple('changedFamily', 'name category filePath')
-#baseFamily = namedtuple('baseFamily', 'name category rootPath filePath')
+changed_family = namedtuple("changed_family", "name category filePath")
+# baseFamily = namedtuple('baseFamily', 'name category rootPath filePath')
 
 # row structure of family change data file
-_CHANGE_LIST_INDEX_FAMILY_NAME = 0
-_CHANGE_LIST_INDEX_FAMILY_FILE_PATH = 1
-_CHANGE_LIST_INDEX_CATEGORY = 2
+CHANGE_LIST_INDEX_FAMILY_NAME = 0
+CHANGE_LIST_INDEX_FAMILY_FILE_PATH = 1
+CHANGE_LIST_INDEX_CATEGORY = 2
 
-_TASK_COUNTER_FILE_PREFIX = 'TaskOutput'
+TASK_COUNTER_FILE_PREFIX = "TaskOutput"
 
 
-def WriteReloadListToFile(reloadFamilies, directoryPath, counter = 0):
-    '''
+def write_reload_list_to_file(reload_families, directory_path, counter=0):
+    """
     Writes task list file to disk. File contains single column of fully qualified file path.
 
-    :param reloadFamilies: List of tuples representing families requiring their nested families to be re-loaded.
-    :type reloadFamilies: [baseFamily]
-    :param directoryPath: Fully qualified directory path to which the task files will be written.
-    :type directoryPath: str
+    :param reload_families: List of tuples representing families requiring their nested families to be re-loaded.
+    :type reload_families: [baseFamily]
+    :param directory_path: Fully qualified directory path to which the task files will be written.
+    :type directory_path: str
     :param counter: Task file name suffix, defaults to 0
     :type counter: int, optional
     :return: True if file was written successfully, otherwise False.
     :rtype: bool
-    '''
+    """
 
     # write out file list without header
     header = []
     # data to be written to file
-    overallData = []
-    fileName = directoryPath + '\\' + _TASK_COUNTER_FILE_PREFIX + str(counter)+ ".txt"
+    overall_data = []
+    file_name = directory_path + "\\" + TASK_COUNTER_FILE_PREFIX + str(counter) + ".txt"
     # loop over families to get file path
-    for r in reloadFamilies:
+    for r in reload_families:
         # row data
         data = []
         data.append(r.filePath)
-        overallData.append(data)
+        overall_data.append(data)
     try:
         # write data
-        util.writeReportData(fileName, header, overallData, writeType = 'w')
+        fileTab.write_report_data(file_name, header, overall_data, writeType="w")
         return True
     except Exception:
         return False
 
-def DeleteOldTaskLists(directoryPath):
-    '''
+
+def delete_old_task_lists(directory_path):
+    """
     Deletes all overall task files in given directory.
 
-    :param directoryPath: Fully qualified directory path containing the task files to be deleted.
-    :type directoryPath: str
+    :param directory_path: Fully qualified directory path containing the task files to be deleted.
+    :type directory_path: str
     :return: True if all files got deleted successfully, otherwise False.
     :rtype: bool
-    '''
+    """
 
     flag = True
     # find all files in folder starting with and delete them
-    files = util.GetFiles(directoryPath, '.txt')
-    if (len(files) > 0):
+    files = fileGet.get_files(directory_path, ".txt")
+    if len(files) > 0:
         for f in files:
-            if (util.GetFileNameWithoutExt(f).startswith(_TASK_COUNTER_FILE_PREFIX)):
-                flag = flag & util.FileDelete(f)
+            if fileIO.get_file_name_without_ext(f).startswith(TASK_COUNTER_FILE_PREFIX):
+                flag = flag & fileIO.file_delete(f)
     return flag
 
-def WriteOutEmptyTaskList(directoryPath, counter = 0):
-    '''
+
+def write_out_empty_task_list(directory_path, counter=0):
+    """
     Writes out an empty task list in case nothing is to be reloaded.
 
-    :param directoryPath: Fully qualified directory path to which the task files will be written.
-    :type directoryPath: str
+    :param directory_path: Fully qualified directory path to which the task files will be written.
+    :type directory_path: str
     :param counter: Task file name suffix, defaults to 0
     :type counter: int, optional
     :return: True if file was written successfully, otherwise False.
     :rtype: bool
-    '''
+    """
 
-    fileName = directoryPath + '\\' + 'TaskOutput' + str(counter)+ ".txt"
+    file_name = directory_path + "\\" + "TaskOutput" + str(counter) + ".txt"
     # write out file list without header
     header = []
     # write out empty data
-    overallData = []
+    overall_data = []
     try:
         # write data
-        util.writeReportData(fileName, header, overallData, writeType = 'w')
+        fileTab.write_report_data(file_name, header, overall_data, writeType="w")
         return True
     except Exception:
         return False
 
-def _RemoveRFAFromFileName(familyName):
-    '''
+
+def _remove_rfa_from_file_name(family_name):
+    """
     Removes any .rfa file extensions from the family name. (not sure why these are sometimes present)
 
-    :param familyName: the family name
-    :type familyName: str
+    :param family_name: the family name
+    :type family_name: str
     :return: the family name with out .rfa (if present in the first place.)
     :rtype: str
-    '''
+    """
+
+    if family_name.lower().endswith(".rfa"):
+        family_name = family_name[: -len(".rfa")]
+    return family_name
 
-    if(familyName.lower().endswith('.rfa')):
-        familyName = familyName[:-len('.rfa')]
-    return familyName
 
-def ReadChangeList(filePath):
-    '''
+def read_change_list(file_path):
+    """
     Reads list of changed families from file into named tuples.
 
-    :param filePath: Fully qualified file path to change list  file.
-    :type filePath: str
+    :param file_path: Fully qualified file path to change list  file.
+    :type file_path: str
     :raises Exception: "Changed families list files does not exist."
     :raises Exception: "Empty families list file!"
     :return: list of named tuples
-    :rtype: [changedFamily]
-    '''
+    :rtype: [changed_family]
+    """
 
     rows = []
-    if(util.FileExist(filePath)):
-        rows = util.ReadCSVfile(filePath)
+    if fileIO.file_exist(file_path):
+        rows = fileCSV.read_csv_file(file_path)
     else:
         raise Exception("Changed families list files does not exist.")
-    if(len(rows) > 0):
+    if len(rows) > 0:
         pass
     else:
         raise Exception("Empty families list file!")
-    
-    returnValue = []
+
+    return_value = []
     # skip header row
     for i in range(1, len(rows)):
-        #TODO: do i need any .rfa from end of family name?
-        famName = _RemoveRFAFromFileName(rows[i][_CHANGE_LIST_INDEX_FAMILY_NAME])
-        data = changedFamily(
-            famName, 
-            rows[i][_CHANGE_LIST_INDEX_CATEGORY], 
-            rows[i][_CHANGE_LIST_INDEX_FAMILY_FILE_PATH]
-            )
-        returnValue.append(data)
-    return returnValue
+        # TODO: do i need any .rfa from end of family name?
+        fam_name = _remove_rfa_from_file_name(rows[i][CHANGE_LIST_INDEX_FAMILY_NAME])
+        data = changed_family(
+            fam_name,
+            rows[i][CHANGE_LIST_INDEX_CATEGORY],
+            rows[i][CHANGE_LIST_INDEX_FAMILY_FILE_PATH],
+        )
+        return_value.append(data)
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyRenameFiles.py` & `DuHast-0.0.7/src/duHast/Revit/Family/Data/family_rename_files.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,147 +1,176 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Helper functions to rename family files on a local or network drive.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 This helper function expect a folder containing rename directive files. For format of those files refer to module RevitFamilyRenameFilesUtils
 
 Note:
 
 - The revit category is not used when renaming files but when renaming nested families.
 - Any associated type catalogue files will also be renamed to match the new family name.
 - Rename directives may not have the filePath property set if the directive is only meant to be used on loaded families.
 
-'''
-
+"""
 
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-import clr
-import System
+# import clr
+# import System
 import os
 
-from duHast.APISamples import RevitFamilyRenameFilesUtils as rFamRenameUtils
-from duHast.Utilities import Result as res
-from duHast.Utilities import Utility as util
+from duHast.Revit.Family import family_rename_files_utils as rFamRenameUtils
+from duHast.Utilities.Objects import result as res
+from duHast.Utilities import files_io as fileIO
+
 
-def _renameFiles(renameDirectives):
-    '''
+def _rename_files(rename_directives):
+    """
     Renames family files and any associated catalogue files based on rename directives.
-    
-    :param renameDirectives: List of tuples representing rename directives.
-    :type renameDirectives: [renameDirective]
 
-    :return: 
+    :param rename_directives: List of tuples representing rename directives.
+    :type rename_directives: [rename_directive]
+
+    :return:
         Result class instance.
 
         - result.status. True if files where renamed successfully, otherwise False.
         - result.message will contain each rename messages in format 'old name -> new name'.
         - result.result empty list
-        
+
         On exception:
-        
+
         - result.status (bool) will be False.
         - result.message will contain an exception message.
         - result.result will be empty
 
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
-    returnValue.UpdateSep(True, 'Renaming families:')
+    return_value = res.Result()
+    return_value.update_sep(True, "Renaming families:")
 
-    for renameDirective in renameDirectives:
+    for rename_directive in rename_directives:
         try:
             # check if rename directive includes a file path ( might be empty if nested families only are to be renamed)
-            if(renameDirective.filePath != ''):
+            if rename_directive.filePath != "":
                 # attempt to rename family file
                 try:
                     # build the new file name
-                    newFullName = os.path.join(os.path.dirname(renameDirective.filePath), renameDirective.newName + '.rfa')
-                    if(util.FileExist(renameDirective.filePath)):
-                        os.rename(renameDirective.filePath, newFullName)
-                        returnValue.AppendMessage(renameDirective.name + ' -> ' + renameDirective.newName)
+                    new_full_name = os.path.join(
+                        os.path.dirname(rename_directive.filePath),
+                        rename_directive.newName + ".rfa",
+                    )
+                    if fileIO.file_exist(rename_directive.filePath):
+                        os.rename(rename_directive.filePath, new_full_name)
+                        return_value.append_message(
+                            "{} -> {}".format(
+                                rename_directive.name, rename_directive.newName
+                            )
+                        )
                     else:
-                        returnValue.UpdateSep(False, 'File not found: '+ renameDirective.name)
+                        return_value.update_sep(
+                            False, "File not found: ".format(rename_directive.name)
+                        )
                 except Exception as e:
-                    returnValue.UpdateSep(False, 'Failed to rename file: ' + renameDirective.name + ' with exception: ' + str(e))
+                    return_value.update_sep(
+                        False,
+                        "Failed to rename file: {} with exception: {}".format(
+                            rename_directive.name, e
+                        ),
+                    )
 
                 # take care of catalogue files as well
-                oldFullName = renameDirective.filePath[:-4] + '.txt'
-                newFullName = os.path.join(os.path.dirname(renameDirective.filePath), renameDirective.newName + '.txt')
-                oldname = renameDirective.name + '.txt'
-                newname = renameDirective.newName + '.txt'
+                old_full_name = rename_directive.filePath[:-4] + ".txt"
+                new_full_name = os.path.join(
+                    os.path.dirname(rename_directive.filePath),
+                    rename_directive.newName + ".txt",
+                )
+                oldname = rename_directive.name + ".txt"
+                newname = rename_directive.newName + ".txt"
                 try:
-                    if(util.FileExist(oldFullName)):
-                        os.rename(oldFullName, newFullName)
-                        returnValue.AppendMessage(oldname + ' -> ' + newname)
+                    if fileIO.file_exist(old_full_name):
+                        os.rename(old_full_name, new_full_name)
+                        return_value.append_message("{} -> {}".format(oldname, newname))
                     else:
-                        returnValue.UpdateSep(True, 'No catalogue file found: ' + oldname) # nothing gone wrong here...just no catalogue file present
+                        return_value.update_sep(
+                            True, "No catalogue file found: {}".format(oldname)
+                        )  # nothing gone wrong here...just no catalogue file present
                 except Exception as e:
-                    returnValue.UpdateSep(False, 'Failed to rename file: ' + oldFullName + ' with exception: ' + str(e))
+                    return_value.update_sep(
+                        False,
+                        "Failed to rename file: {} with exception: {}".format(
+                            old_full_name, e
+                        ),
+                    )
             else:
-                returnValue.UpdateSep(True, 'No file path found: ' + renameDirective.name) # nothing gone wrong here...just not required to rename a file
+                return_value.update_sep(
+                    True, "No file path found: {}".format(rename_directive.name)
+                )  # nothing gone wrong here...just not required to rename a file
         except Exception as e:
-            returnValue.UpdateSep(False, 'Failed to rename files with exception: ' + str(e))
-    return returnValue
+            return_value.update_sep(
+                False, "Failed to rename files with exception: ".format(e)
+            )
+    return return_value
+
 
-def RenameFamilyFiles(directoryPath):
-    '''
+def rename_family_files(directory_path):
+    """
     Entry point for this module. Will read rename directives files in given directory and attempt to rename
     family files and any associated catalogue files accordingly.
 
     Note: Rename directive may not include a file path in situations where a loaded family only is to be renamed. This \
         will still return True in such a case.
 
-    :param directoryPath: Fully qualified directory path to where rename directive files are located.
-    :type directoryPath: str
+    :param directory_path: Fully qualified directory path to where rename directive files are located.
+    :type directory_path: str
     :return: 
         Result class instance.
 
         - result.status. True if files where renamed successfully, otherwise False.
         - result.message will contain each rename messages in format 'old name -> new name'.
         - result.result empty list
         
         On exception:
         
         - result.status (bool) will be False.
         - result.message will contain an exception message.
         - result.result will be empty
 
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
+    return_value = res.Result()
     # get directives from folder
-    renameDirectivesResult = rFamRenameUtils.GetRenameDirectives(directoryPath)
+    rename_directives_result = rFamRenameUtils.get_rename_directives(directory_path)
     # check if anything came back
-    if(renameDirectivesResult.status):
-        renameDirectives = renameDirectivesResult.result
+    if rename_directives_result.status:
+        rename_directives = rename_directives_result.result
         # rename files as per directives
-        returnValue = _renameFiles(renameDirectives)
+        return_value = _rename_files(rename_directives)
     else:
-        returnValue = renameDirectivesResult
+        return_value = rename_directives_result
 
-    return returnValue
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyRenameLoadedFamilies.py` & `DuHast-0.0.7/src/duHast/Revit/Family/Data/family_rename_loaded_families.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,153 +1,177 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Helper functions to rename family loaded families in a project file or family file.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 This helper function expect a folder containing rename directive files. For format of those files refer to module RevitFamilyRenameFilesUtils
 
 
-'''
-
+"""
 
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-import clr
-import System
+# import clr
+# import System
 
-from duHast.APISamples import RevitFamilyRenameFilesUtils as rFamRenameUtils
-from duHast.APISamples import RevitFamilyUtils as rFamUtils
-from duHast.APISamples import RevitTransaction as rTran
-from duHast.Utilities import Result as res
+from duHast.Revit.Family import family_rename_files_utils as rFamRenameUtils
+from duHast.Revit.Family import family_utils as rFamUtils
+from duHast.Revit.Common import transaction as rTran
+from duHast.Utilities.Objects import result as res
 
 # import Autodesk Revit DataBase namespace
 import Autodesk.Revit.DB as rdb
 
-def _renameLoadedFamilies(doc, renameDirectives, familyIds):
-    '''
+
+def _rename_loaded_families(doc, rename_directives, family_ids):
+    """
     Loops over nested families and if a match in rename directives is found will rename the family accordingly.
 
     :param doc: The current family document.
     :type doc: Autodesk.Revit.DB.Document
-    :param renameDirectives: List of rename directives.
-    :type renameDirectives: [renameDirective]
-    :param familyIds: List of all nested family ids.
-    :type familyIds: [Autodesk.Revit.DB.ElementId]
+    :param rename_directives: List of rename directives.
+    :type rename_directives: [rename_directive]
+    :param family_ids: List of all nested family ids.
+    :type family_ids: [Autodesk.Revit.DB.ElementId]
 
-    :return: 
+    :return:
         Result class instance.
 
         - result.status. True if all families where renamed successfully, otherwise False.
         - result.message will contain each rename messages in format 'Renamed family from :' +current Name + ' to ' + newName.
         - result.result empty list
-        
+
         On exception:
-        
+
         - result.status (bool) will be False.
         - result.message will contain an exception message in format: 'Failed to rename family from :' + currentName + ' to ' + newName
         - result.result will be empty
 
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
-    returnValue.status = False
-    renameMatchCounter = 0
+    return_value = res.Result()
+    return_value.status = False
+    rename_match_counter = 0
     # loop over families and check for match in rename directives
-    for famId in familyIds:
-        family = doc.GetElement(famId)
-        familyName = family.Name
-        if(family.IsEditable and family.IsValidObject):
-            familyCategoryName = family.FamilyCategory.Name
+    for fam_id in family_ids:
+        family = doc.GetElement(fam_id)
+        family_name = family.Name
+        if family.IsEditable and family.IsValidObject:
+            family_category_name = family.FamilyCategory.Name
             # loop over rename directives and look for match in family name and category
-            for renameDirective in renameDirectives:
-                if(renameDirective.name == familyName and renameDirective.category == familyCategoryName):
-                    renameMatchCounter = renameMatchCounter + 1
+            for rename_directive in rename_directives:
+                if (
+                    rename_directive.name == family_name
+                    and rename_directive.category == family_category_name
+                ):
+                    rename_match_counter = rename_match_counter + 1
                     # rename this family
                     def action():
-                        actionReturnValue = res.Result()
+                        action_return_value = res.Result()
                         try:
-                            family.Name = renameDirective.newName
-                            actionReturnValue.UpdateSep(
-                                True, 
-                                'Renamed family of category [' + familyCategoryName + '] vs directive category [' + renameDirective.category + '] from: ' + renameDirective.name + ' to: ' + renameDirective.newName)
+                            family.Name = rename_directive.newName
+                            action_return_value.update_sep(
+                                True,
+                                "Renamed family of category ["
+                                + family_category_name
+                                + "] vs directive category ["
+                                + rename_directive.category
+                                + "] from: "
+                                + rename_directive.name
+                                + " to: "
+                                + rename_directive.newName,
+                            )
                         except Exception as e:
-                            actionReturnValue.UpdateSep(
-                                False, 
-                                'Failed to rename family of category [' + familyCategoryName + '] vs directive category [' + renameDirective.category + '] from: ' + renameDirective.name + ' to: ' + renameDirective.newName)
-                        return actionReturnValue
-                    transaction = rdb.Transaction(doc, 'Renaming: ' + renameDirective.name)
-                    renameResult = rTran.in_transaction(transaction, action)
-                    if(renameResult.status):
+                            action_return_value.update_sep(
+                                False,
+                                "Failed to rename family of category ["
+                                + family_category_name
+                                + "] vs directive category ["
+                                + rename_directive.category
+                                + "] from: "
+                                + rename_directive.name
+                                + " to: "
+                                + rename_directive.newName,
+                            )
+                        return action_return_value
+
+                    transaction = rdb.Transaction(
+                        doc, "Renaming: " + rename_directive.name
+                    )
+                    rename_result = rTran.in_transaction(transaction, action)
+                    if rename_result.status:
                         # make sure that this returns true as soon as one family renamed successfully
-                        returnValue.status = True
+                        return_value.status = True
                     # update messages
-                    returnValue.AppendMessage(renameResult.message)
+                    return_value.append_message(rename_result.message)
                     break
     # check if anything got renamed at all
-    if(renameMatchCounter == 0):
-        returnValue.AppendMessage('No match for rename directives found. Nothing was renamed.')
-    return returnValue
+    if rename_match_counter == 0:
+        return_value.append_message(
+            "No match for rename directives found. Nothing was renamed."
+        )
+    return return_value
 
 
-def RenameLoadedFamilies(doc, directoryPath):
-    '''
+def rename_loaded_families(doc, directory_path):
+    """
     Entry point for this module. Will read rename directives files in given directory and attempt to rename
     loaded families accordingly.
 
-    :param directoryPath: Fully qualified directory path to where rename directive files are located.
-    :type directoryPath: str
-    :return: 
+    :param directory_path: Fully qualified directory path to where rename directive files are located.
+    :type directory_path: str
+    :return:
         Result class instance.
 
         - result.status. True if a single families was renamed successfully, otherwise False.
         - result.message will contain each rename messages in format 'Renamed family from :' +current Name + ' to ' + newName.
         - result.result empty list
-        
+
         On exception:
-        
+
         - result.status (bool) will be False.
         - result.message will contain an exception message in format: 'Failed to rename family from :' + currentName + ' to ' + newName
         - result.result will be empty
 
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
+    return_value = res.Result()
     # get directives from folder
-    renameDirectivesResult = rFamRenameUtils.GetRenameDirectives(directoryPath)
+    rename_directives_result = rFamRenameUtils.get_rename_directives(directory_path)
     # check if anything came back
-    if(renameDirectivesResult.status):
-        renameDirectives = renameDirectivesResult.result
+    if rename_directives_result.status:
+        rename_directives = rename_directives_result.result
         # get all family ids in file
-        familyIds = rFamUtils.GetAllLoadableFamilyIdsThroughTypes(doc)
-        if(len(familyIds) > 0):
+        family_ids = rFamUtils.get_all_loadable_family_ids_through_types(doc)
+        if len(family_ids) > 0:
             # rename files as per directives
-            returnValue = _renameLoadedFamilies(doc, renameDirectives, familyIds)
+            return_value = _rename_loaded_families(doc, rename_directives, family_ids)
         else:
-            returnValue.UpdateSep(True, 'Mo loadable families in file.')
+            return_value.update_sep(True, "Mo loadable families in file.")
     else:
-        returnValue = renameDirectivesResult
+        return_value = rename_directives_result
 
-    return returnValue
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitFamilyReportUtils.py` & `DuHast-0.0.7/src/duHast/Revit/Family/Data/family_report_utils.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Family report data utility module containing functions to read the data from file.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 Reads family base data into two list of named tuples.
 
 rootFamily:
@@ -16,343 +16,380 @@
 
 - name 
 - category 
 - filePath 
 - rootPath  [str]
 - categoryPath [str]
 
-'''
+"""
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 
 from collections import namedtuple
 
-from duHast.Utilities import Utility as util
-from duHast.Utilities import Result as res
+from duHast.Utilities.Objects import result as res
+from duHast.Utilities import files_csv as fileCSV, files_io as fileIO
 
 # tuples containing base family data read from file
-rootFamily = namedtuple('rootFamily', 'name category filePath')
-nestedFamily = namedtuple('nestedFamily', 'name category filePath rootPath categoryPath')
+rootFamily = namedtuple("rootFamily", "name category filePath")
+nestedFamily = namedtuple(
+    "nestedFamily", "name category filePath rootPath categoryPath"
+)
 
 # row structure of report data file
-_BASE_DATA_LIST_INDEX_ROOT_PATH = 0
-_BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH = 1
-_BASE_DATA_LIST_INDEX_FAMILY_NAME = 2
-_BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH = 3
+BASE_DATA_LIST_INDEX_ROOT_PATH = 0
+BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH = 1
+BASE_DATA_LIST_INDEX_FAMILY_NAME = 2
+BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH = 3
 
 # exceptions
-_EXCEPTION_NO_FAMILY_BASE_DATA_FILES = 'Report data list files do not exist.'
-_EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES = 'Empty report data list file!'
+EXCEPTION_NO_FAMILY_BASE_DATA_FILES = "Report data list files do not exist."
+EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES = "Empty report data list file!"
+
 
-def ReadUniqueFamiliesFromReport(filePath):
-    '''
-    Reads list of families from any report file into list of unique named tuples. 
+def read_unique_families_from_report(filePath):
+    """
+    Reads list of families from any report file into list of unique named tuples.
     Reports needs:
-    
+
     - to contain the following columns (in this order):  root path, category path , family name, family file path
     - a tab separated file
 
     :param filePath: Fully qualified file path to family base data report file.
     :type filePath: str
     :raises Exception: "Families base data list files does not exist."
     :raises Exception: "Empty Families base data list file!"
     :return: Two lists: first list of named tuples contain family root data, second list contains family nested data.
     :rtype: [rootFamily], [nestedFamily]
-    '''
+    """
 
     rows = []
-    if(util.FileExist(filePath)):
-        rows = util.ReadCSVfile(filePath)
+    if fileIO.file_exist(filePath):
+        rows = fileCSV.read_csv_file(filePath)
     else:
-        raise Exception(_EXCEPTION_NO_FAMILY_BASE_DATA_FILES)
-    if(len(rows) > 0):
+        raise Exception(EXCEPTION_NO_FAMILY_BASE_DATA_FILES)
+    if len(rows) > 0:
         pass
     else:
-        raise Exception(_EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES)
-    
+        raise Exception(EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES)
+
     returnValueRootFamily = []
     returnValueNestedFamily = []
     for i in range(1, len(rows)):
         # check if root family
-        if( '::' not in rows[i][_BASE_DATA_LIST_INDEX_ROOT_PATH]):
+        if "::" not in rows[i][BASE_DATA_LIST_INDEX_ROOT_PATH]:
             data = rootFamily(
-                rows[i][_BASE_DATA_LIST_INDEX_FAMILY_NAME], 
-                rows[i][_BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH], 
-                rows[i][_BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH]
+                rows[i][BASE_DATA_LIST_INDEX_FAMILY_NAME],
+                rows[i][BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH],
+                rows[i][BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH],
             )
             # only add unique occurrences
-            if (data not in returnValueRootFamily):
+            if data not in returnValueRootFamily:
                 returnValueRootFamily.append(data)
         else:
             # the category is the last entry in the category root path
-            categories = rows[i][_BASE_DATA_LIST_INDEX_ROOT_PATH].split(' :: ')
+            categories = rows[i][BASE_DATA_LIST_INDEX_ROOT_PATH].split(" :: ")
             category = categories[len(categories) - 1]
             # found a child family
             data = nestedFamily(
-                rows[i][_BASE_DATA_LIST_INDEX_FAMILY_NAME], 
-                category, 
-                rows[i][_BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH],
-                rows[i][_BASE_DATA_LIST_INDEX_ROOT_PATH].split(' :: '), # split root path into list for ease of searching
-                rows[i][_BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH].split(' :: '), # split category path into list for ease of searching
+                rows[i][BASE_DATA_LIST_INDEX_FAMILY_NAME],
+                category,
+                rows[i][BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH],
+                rows[i][BASE_DATA_LIST_INDEX_ROOT_PATH].split(
+                    " :: "
+                ),  # split root path into list for ease of searching
+                rows[i][BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH].split(
+                    " :: "
+                ),  # split category path into list for ease of searching
             )
             # only add unique occurrences
-            if (data not in returnValueNestedFamily):
+            if data not in returnValueNestedFamily:
                 returnValueNestedFamily.append(data)
     return returnValueRootFamily, returnValueNestedFamily
 
-def ReadUniqueFamiliesWithRowDataFromReport(filePath):
-    '''
+
+def read_unique_families_with_row_data_from_report(filePath):
+    """
     Reads list of families from any report file into dictionaries where key is a named tuple and values are the rows associated with that family
     Reports needs:
-    
+
     - to contain the following columns (in this order):  root path, category path , family name, family file path
     - a tab separated file
 
     :param filePath: Fully qualified file path to family base data report file.
     :type filePath: str
     :raises Exception: "Families base data list files does not exist."
     :raises Exception: "Empty Families base data list file!"
     :return: Two dictionaries: first dictionary contain family root data, second dictionary contains family nested data.
     :rtype: {rootFamily:[[str]]}, {nestedFamily:[[str]]}
-    '''
+    """
 
     rows = []
-    if(util.FileExist(filePath)):
-        rows = util.ReadCSVfile(filePath, True)
+    if fileIO.file_exist(filePath):
+        rows = fileCSV.read_csv_file(filePath, True)
     else:
-        raise Exception(_EXCEPTION_NO_FAMILY_BASE_DATA_FILES)
-    if(len(rows) > 0):
+        raise Exception(EXCEPTION_NO_FAMILY_BASE_DATA_FILES)
+    if len(rows) > 0:
         pass
     else:
-        raise Exception(_EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES)
-    
+        raise Exception(EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES)
+
     returnValueRootFamily = {}
     returnValueNestedFamily = {}
     for i in range(1, len(rows)):
         # check if root family
-        if( '::' not in rows[i][_BASE_DATA_LIST_INDEX_ROOT_PATH]):
+        if "::" not in rows[i][BASE_DATA_LIST_INDEX_ROOT_PATH]:
             data = rootFamily(
-                rows[i][_BASE_DATA_LIST_INDEX_FAMILY_NAME], 
-                rows[i][_BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH], 
-                rows[i][_BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH]
+                rows[i][BASE_DATA_LIST_INDEX_FAMILY_NAME],
+                rows[i][BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH],
+                rows[i][BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH],
             )
             # add row to dictionary
-            if (data not in returnValueRootFamily):
+            if data not in returnValueRootFamily:
                 returnValueRootFamily[data] = [rows[i]]
             else:
                 returnValueRootFamily[data].append(rows[i])
         else:
             # the category is the last entry in the category root path
-            categories = rows[i][_BASE_DATA_LIST_INDEX_ROOT_PATH].split(' :: ')
+            categories = rows[i][BASE_DATA_LIST_INDEX_ROOT_PATH].split(" :: ")
             category = categories[len(categories) - 1]
             # found a child family
             data = nestedFamily(
-                rows[i][_BASE_DATA_LIST_INDEX_FAMILY_NAME], 
-                category, 
-                rows[i][_BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH],
-                rows[i][_BASE_DATA_LIST_INDEX_ROOT_PATH], 
-                rows[i][_BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH], 
+                rows[i][BASE_DATA_LIST_INDEX_FAMILY_NAME],
+                category,
+                rows[i][BASE_DATA_LIST_INDEX_FAMILY_FILE_PATH],
+                rows[i][BASE_DATA_LIST_INDEX_ROOT_PATH],
+                rows[i][BASE_DATA_LIST_INDEX_ROOT_CATEGORY_PATH],
             )
             returnValueNestedFamily[data] = [rows[i]]
     return returnValueRootFamily, returnValueNestedFamily
 
+
 # ------------------------------------- combining reports --------------------------------------------
 
-def _getDataRowsFromDictionary(dic):
-    '''
+
+def _get_data_rows_from_dictionary(dic):
+    """
     Builds list of data rows from dictionary past in
 
     :param dic: Dictionary where key is a tuple and values is a list of list of strings
     :type dic: {named tuple: [[str]]}
     :param dataList: List of list of strings
     :type dataList: [[str]]
-    
+
     :return: List of list of strings
     :rtype: [[str]]
-    '''
+    """
 
     dataList = []
     # get rows from dictionary
-    for k,v in dic.items():
+    for k, v in dic.items():
         # get data rows for root family
         for rootData in v[0]:
             dataList.append(rootData)
         # get data rows for any nested families
         for nestedFamRowValue in v[1]:
             dataList.append(nestedFamRowValue)
     return dataList
 
 
-def _compareFamilyDictionaries(previousAgData, newAgData):
-    '''
-    Compares two aggregate data dictionaries. Any new root family from newAgData ( root family occurring in newAgData only) will be add to the previousAgData dictionary. 
+def _compare_family_dictionaries(previousAgData, newAgData):
+    """
+    Compares two aggregate data dictionaries. Any new root family from newAgData ( root family occurring in newAgData only) will be add to the previousAgData dictionary.
     Any existing root family (root family occurring in previous and new aggregate data dictionaries) will be updated in the previousAgData dictionary with row data from the newAgData data dictionary.
 
-    
+
     :param previousAgData: A dictionary containing aggregated family data from the previous report.
     :type previousAgData: {key:str, value ([str],[str])}
     :param newAgData: A dictionary containing aggregated family data from the new report.
     :type newAgData: {key:str, value ([str],[str])}
     :return:
 
         If previousAgData is empty and newAgData contains data, newAgData will be returned unchanged.
         If newAgData is empty and previousAgData contains data, previousAgData will be returned unchanged.
         if both dictionary are empty an empty dictionary will be returned.
 
     :rtype: {key:str, value ([str],[str])}
-    '''
-    
+    """
+
     returnValue = res.Result()
     # check corner cases:
-    if(len(newAgData) == 0 and len(previousAgData) > 0):
+    if len(newAgData) == 0 and len(previousAgData) > 0:
         # new is empty, but previous has data
-        returnValue.UpdateSep(True, 'New report data is empty, using previous report data only')
+        returnValue.update_sep(
+            True, "New report data is empty, using previous report data only"
+        )
         returnValue.result.append(previousAgData)
-    elif(len(newAgData) > 0 and len(previousAgData) == 0):
+    elif len(newAgData) > 0 and len(previousAgData) == 0:
         # new has data, but previous is empty
-        returnValue.UpdateSep(True, 'Previous report data is empty, using new report data only')
+        returnValue.update_sep(
+            True, "Previous report data is empty, using new report data only"
+        )
         returnValue.result.append(newAgData)
-    elif(len(newAgData) == 0 and len (previousAgData) == 0):
+    elif len(newAgData) == 0 and len(previousAgData) == 0:
         # new is empty, previous is empty
-        returnValue.UpdateSep(True, 'Previous report data and new report data are empty!')
+        returnValue.update_sep(
+            True, "Previous report data and new report data are empty!"
+        )
         returnValue.result.append({})
     else:
         # other and current have data
         for newData in newAgData:
-            if(newData in previousAgData):
-                returnValue.AppendMessage('Substituting family data: ' + newData)
+            if newData in previousAgData:
+                returnValue.append_message(
+                    "Substituting family data: {}".format(newData)
+                )
             else:
-                returnValue.AppendMessage('Adding new family data: ' + newData)
+                returnValue.append_message("Adding new family data: {}".format(newData))
             previousAgData[newData] = newAgData[newData]
         returnValue.result.append(previousAgData)
     return returnValue
 
-def _getNestedFamiliesBelongingToRootFamilies(rootFam, nestedFamilies):
-    '''
+
+def _get_nested_families_belonging_to_root_families(rootFam, nestedFamilies):
+    """
     Returns a list of all row data of nested families belonging to a given root family.
 
     :param rootFam: A tuple of a root family from a report.
     :type rootFam: tuple of type 'rootFamily'
     :param nestedFamilies: A list of tuples of all nested families in a report
     :type nestedFamilies: [tuple of type 'nestedFamily']
 
     :return: _description_
     :rtype: _type_
-    '''
+    """
 
     nestedFamiliesBelongingToRootFamRowData = []
     for nf in nestedFamilies:
         # split path in order to get to top most root family
-        nestedFamRootPath = nf.rootPath.split(' :: ')
-        nestedFamCatPath = nf.categoryPath.split(' :: ')
-        if(rootFam.name == nestedFamRootPath[0] and rootFam.category == nestedFamCatPath[0]):
+        nestedFamRootPath = nf.rootPath.split(" :: ")
+        nestedFamCatPath = nf.categoryPath.split(" :: ")
+        if (
+            rootFam.name == nestedFamRootPath[0]
+            and rootFam.category == nestedFamCatPath[0]
+        ):
             nestedFamiliesBelongingToRootFamRowData.append(nestedFamilies[nf][0])
     return nestedFamiliesBelongingToRootFamRowData
 
-def _aggregateFamilyData(rootFamilies, nestedFamilies):
-    '''
+
+def _aggregate_family_data(rootFamilies, nestedFamilies):
+    """
     Returns a dictionary where key are all the root family file path from a report and value is a tuple of two list of strings containing
     the row data read from report file for the root family itself (first list) and the row data read from report file for any nested families (second list).
 
     :param rootFamilies: A list containing tuples of all root families in a report.
     :type rootFamilies: [tuple of type 'rootFamily']
     :param nestedFamilies: A list of tuples of all nested families in a report
     :type nestedFamilies: [tuple of type 'nestedFamily']
-    
+
     :return: Returns a dictionary where key is the root family file path and value is a tuple of two list of strings containing the row data for root family itself (first list) and the row data for any nested families (second list)
     :rtype: {key:str, value ([str],[str])}
-    '''
+    """
 
     # key is root family, value is tuple of csv row representing the root family data and list of rows each representing a nested family data
     aggregatedFamilyData = {}
     for rf in rootFamilies:
-        nestedFamiliesOfRootFamilyRowData = _getNestedFamiliesBelongingToRootFamilies(rf, nestedFamilies)
+        nestedFamiliesOfRootFamilyRowData = (
+            _get_nested_families_belonging_to_root_families(rf, nestedFamilies)
+        )
         # key is the unique family file path of the root family
         # value is a tuple of two lists : root data rows at index 0, nested fam data rows at index 1
-        aggregatedFamilyData[rf.filePath] = (rootFamilies[rf], nestedFamiliesOfRootFamilyRowData)
+        aggregatedFamilyData[rf.filePath] = (
+            rootFamilies[rf],
+            nestedFamiliesOfRootFamilyRowData,
+        )
     return aggregatedFamilyData
 
-def _checkFamiliesStillExist(famData):
-    '''
+
+def _check_families_still_exist(famData):
+    """
     Checks whether families still exist on file server.
 
     Reason why families no longer exist:
 
     - family got deleted or moved
     - family got renamed
 
     :param famData: A dictionary containing aggregated family data from the a report.
     :type famData: {key:str, value ([str],[str])}
 
-    :return: 
+    :return:
         Result class instance.
-        
+
         - .result = True if successfully removed any outdated family data or None needed removing. Otherwise False.
         - .message will contain list of families removed or message nothing needed to be removed.
         - . result will contain past in dictionary at index 0
 
         On exception:
-        
+
         - result.status (bool) will be False.
         - result.message will contain generic exception message.
         - result.result will be empty
     :rtype: :class:`.Result`
-    '''
+    """
 
     returnValue = res.Result()
     try:
         removeKeys = []
         # get keys from dic as a list
         # check which ones do not exist anymore
         for filePath in famData.keys():
-            if (util.FileExist(filePath) == False):
+            if fileIO.file_exist(filePath) == False:
                 removeKeys.append(filePath)
-        
+
         # check if any family requires to be removed from the data set
-        if(len(removeKeys) > 0):
+        if len(removeKeys) > 0:
             # remove those keys from dictionary
             for dKey in removeKeys:
                 removeSingleKey = famData.pop(dKey, None)
-                if (removeSingleKey != None):
-                    returnValue.AppendMessage('Removed family from data: {}'.format(dKey))
+                if removeSingleKey != None:
+                    returnValue.append_message(
+                        "Removed family from data: {}".format(dKey)
+                    )
                 else:
-                    returnValue.AppendMessage('Failed to removed family from data: {}'.format(dKey))
+                    returnValue.append_message(
+                        "Failed to removed family from data: {}".format(dKey)
+                    )
         else:
-            returnValue.AppendMessage('No family required removing from data.')
+            returnValue.append_message("No family required removing from data.")
 
         # update return data
-        returnValue.UpdateSep(True, 'Successfully updated family data.')
+        returnValue.update_sep(True, "Successfully updated family data.")
         returnValue.result.append(famData)
 
     except Exception as e:
-        returnValue.UpdateSep(False, 'Failed to check whether families still exist with exception: ' + str(e))
+        returnValue.update_sep(
+            False,
+            "Failed to check whether families still exist with exception: {}".format(e),
+        )
     return returnValue
 
-def CombineReports (previousReportPath, newReportPath):
-    '''
+
+def combine_reports(previousReportPath, newReportPath):
+    """
     This combines two reports by:
 
     - building an aggregate data dictionary of each report (key root family file path, values lists containing the row data read from file for the root family as well as any nested families)
     - comparing the previous report dictionary with the new report dictionary and
         - adding any new families found in the new report dictionary
         - updating any previous report families found with data matching the root family in the new report dictionary
 
@@ -365,66 +402,82 @@
     :param previousReportPath: A fully qualified file path to the previous report file.
     :type previousReportPath: str
     :param newReportPath: A fully qualified file path to the new report file.
     :type newReportPath: str
 
     :return: list of lists of report rows
     :rtype: [[str]]
-    '''
+    """
 
     returnValue = res.Result()
     # read families from both reports
     # ...compare them:
     # take all families from current report and all none matching families from the other report
 
     previousAggregatedFamilies = {}
     newAggregatedFamilies = {}
 
     # previous report
     try:
-        previousRoot, previousNested = ReadUniqueFamiliesWithRowDataFromReport(previousReportPath)
-        returnValue.AppendMessage('Previous report: found ' + str(len(previousRoot)) + ' root families.')
-        returnValue.AppendMessage('Previous report: found ' + str(len(previousNested)) + ' nested families.')
+        previousRoot, previousNested = read_unique_families_with_row_data_from_report(
+            previousReportPath
+        )
+        returnValue.append_message(
+            "Previous report: found {} root families.".format(len(previousRoot))
+        )
+        returnValue.append_message(
+            "Previous report: found {} nested families.".format(len(previousNested))
+        )
         # build dictionary containing all family data per root family
-        previousAggregatedFamilies = _aggregateFamilyData(previousRoot, previousNested)
+        previousAggregatedFamilies = _aggregate_family_data(
+            previousRoot, previousNested
+        )
     except Exception as e:
         # check whether empty file exception
-        if (str(e) != _EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES):
+        if str(e) != EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES:
             raise e
-    
+
     # new report
     try:
-        newRoot, newNested = ReadUniqueFamiliesWithRowDataFromReport(newReportPath)
+        newRoot, newNested = read_unique_families_with_row_data_from_report(
+            newReportPath
+        )
         # build dictionary containing all family data per root family
-        newAggregatedFamilies = _aggregateFamilyData(newRoot, newNested)
-        returnValue.AppendMessage('New report: found ' + str(len(newRoot)) + ' root families.')
-        returnValue.AppendMessage('New report: found ' + str(len(newNested)) + ' nested families.')
+        newAggregatedFamilies = _aggregate_family_data(newRoot, newNested)
+        returnValue.append_message(
+            "New report: found {} root families.".format(len(newRoot)) + ""
+        )
+        returnValue.append_message(
+            "New report: found {} nested families.".format(len(newNested)) + ""
+        )
     except Exception as e:
         # check whether empty file exception
-        if (str(e) != _EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES):
+        if str(e) != EXCEPTION_EMPTY_FAMILY_BASE_DATA_FILES:
             raise e
 
     # compare dictionaries: build unique list of families
-    uniqueFamDataStatus = _compareFamilyDictionaries(previousAggregatedFamilies, newAggregatedFamilies)
-    returnValue.Update(uniqueFamDataStatus)
+    uniqueFamDataStatus = _compare_family_dictionaries(
+        previousAggregatedFamilies, newAggregatedFamilies
+    )
+    returnValue.update(uniqueFamDataStatus)
     uniqueFamData = uniqueFamDataStatus.result[0]
 
     # check whether families still exist on file server
-    removeNoneExistingFamilies = _checkFamiliesStillExist(uniqueFamData)
-    returnValue.Update(removeNoneExistingFamilies)
+    removeNoneExistingFamilies = _check_families_still_exist(uniqueFamData)
+    returnValue.update(removeNoneExistingFamilies)
     # only update family data if culling occurred without any exceptions
-    if(removeNoneExistingFamilies.status):
+    if removeNoneExistingFamilies.status:
         uniqueFamData = removeNoneExistingFamilies.result[0]
 
     # get report header row (there should be a previous report file...otherwise this will write an empty header row)
-    header = util.GetFirstRowInCSVFile(previousReportPath)
-    headerRow = header.split(',')
-    
+    header = fileCSV.get_first_row_in_csv_file(previousReportPath)
+    headerRow = header.split(",")
+
     # build list of data rows
-    rowsCurrent = _getDataRowsFromDictionary(uniqueFamData)
+    rowsCurrent = _get_data_rows_from_dictionary(uniqueFamData)
     # sort rows by root ( first entry ) since other code (circ reference checker for instance) expects data sorted
     rowsCurrent.sort()
     # start with header row
     rowsCurrent.insert(0, headerRow)
     # overwrite return result value since it is already containing data from previous operations
     returnValue.result = rowsCurrent
-    return returnValue
+    return returnValue
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitGenericAnnotation.py` & `DuHast-0.0.7/src/duHast/Revit/Stairs/stairs.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Revit generic annotation helper functions.
+This module contains a number of helper functions relating to Revit stairs. 
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -25,165 +25,177 @@
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
 import System
 
-import sys
-#sys.path.append('C:\Users\jchristel\Documents\deployRevitBP')
-
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.APISamples import RevitFamilyUtils as rFam
-from duHast.APISamples import RevitAnnotation as rAnno
+from duHast.Revit.Common import common as com
+from duHast.Revit.Family import family_utils as rFam
+from duHast.Revit.Stairs.Utility import stairs_filter as rStairsFilter
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
+import Autodesk.Revit.DB.Architecture as rdbA
+
+
+def get_all_stair_types_by_category(doc):
+    """
+    Gets a filtered element collector of all Stair types in the model.
+
+    Return includes:
+    - Stair
+    - Assembled Stair
+    - Precast Stair
+    - Cast-In-Place Stair
+    - In place families or loaded families
+
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
 
-# -------------------------------------------- common variables --------------------
-#: header used in reports
-REPORT_GENERIC_ANNOTATIONS_HEADER = ['HOSTFILE', 'GENERICANNOTATIONTYPEID', 'GENERICANNOTATIONTYPENAME']
+    :return: A filtered element collector containing stair types.
+    :rtype: Autodesk.Revit.DB.FilteredElementCollector
+    """
+
+    collector = rStairsFilter._get_all_stair_types_by_category(doc)
+    return collector
 
 
-# --------------------------------------------- utility functions ------------------
+def get_all_stair_types_by_class(doc):
+    """
+    Gets a filtered element collector of all Stair types in the model.
 
-# returns all  GenericAnnotation types in a model
-# doc:   current model document
-def GetAllGenericAnnotationTypesByCategory(doc):
-    '''
-    This will return a filtered element collector of all GenericAnnotation types in the model.
+    Return includes:
+
+    - Assembled Stair
+    - Precast Stair
+    - Cast-In-Place Stair
+
+    It will not return any in place family or Stair types! These are internally treated as Families or Family Symbols class objects.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :return: _description_
+
+    :return: A filtered element collector containing stair types.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
 
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_GenericAnnotation).WhereElementIsElementType()
+    collector = rStairsFilter._get_stair_types_by_class(doc)
     return collector
 
-# returns all  GenericAnnotation types in a model
-# doc:   current model document
-def GetAllGenericAnnotationTypeIdsByCategory(doc):
-    '''
-    This will return a list of all GenericAnnotation types (symbols) id's in the model excluding shared families.
+
+# -------------------------------- none in place Stair types -------------------------------------------------------
+
+
+def get_all_stair_instances_by_category(doc):
+    """
+    Gets a filtered element collector of all Stair elements placed in model.
+
+    TODO: Confirm it  ignores in place families?
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    
-    :return: _description_
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
 
-    ids = []
-    col = GetAllGenericAnnotationTypesByCategory(doc)
-    for c in col:
-        parameterMatch = False
-        # get the family object to check whether it is a shared family
-        fam = c.Family
-        id =  rParaGet.get_built_in_parameter_value(fam, rdb.BuiltInParameter.FAMILY_SHARED)
-        if(id != None):
-            parameterMatch = True
-            if(id == 'No' and c.Id not in ids):
-                ids.append(c.Id)
-        if(parameterMatch == False):
-            # family cant be of type shared...
-            ids.append(c.Id)
-    return ids
+    :return: A filtered element collector containing stair instances.
+    :rtype: Autodesk.Revit.DB.FilteredElementCollector
+    """
+
+    return (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_Stairs)
+        .WhereElementIsNotElementType()
+    )
+
+
+def get_all_stair_instances_by_class(doc):
+    """
+    Gets a filtered element collection all Stair elements placed in model...
 
-def BuildGenericAnnotationTypesDictionary(collector, dic):
-    '''
-    Returns the dictionary past in with keys and or values added retrieved from collector past in.
-
-    :param collector: Filtered element collector containing GenericAnnotation type elements of family symbols.
-    :type collector: Autodesk.Revit.DB.FilteredElementCollector
-    :param dic: Dictionary, the key is the family name and the value a list of element ids representing annotation types.
-    :type dic: dic: key str, values list of Autodesk.Revit.DB.ElementId
-    
-    :return: Past in expanded by values from collector. Dictionary the key is the Family name and the value a list of element ids.
-    :rtype: dic: key str, values list of Autodesk.Revit.DB.ElementId
-    '''
-
-    for c in collector:
-        if(dic.has_key(c.FamilyName)):
-            if(c.Id not in dic[c.FamilyName]):
-                dic[c.FamilyName].append(c.Id)
-        else:
-            dic[c.FamilyName] = [c.Id]
-    return dic
-
-# doc   current model document
-def SortGenericAnnotationTypesByFamilyName(doc):
-    # get all GenericAnnotation types
-    wts_two = GetAllGenericAnnotationTypesByCategory(doc)
-    usedWts = {}
-    usedWts = BuildGenericAnnotationTypesDictionary(wts_two, usedWts)
-    return usedWts
-
-
-# doc   current model document
-def GetUsedGenericAnnotationTypeIds(doc):
-    '''
-    Returns all used generic annotation symbol ids ( used in model as well as dimension types)
+    TODO: Confirm it ignores Stair soffits.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    
-    :return: _description_
+
+    :return: A filtered element collector containing stair instances.
+    :rtype: Autodesk.Revit.DB.FilteredElementCollector
+    """
+
+    return (
+        rdb.FilteredElementCollector(doc)
+        .OfClass(rdbA.Stairs)
+        .WhereElementIsNotElementType()
+    )
+
+
+def get_all_stair_type_ids_by_category(doc):
+    """
+    Gets all Stair element type ids available in model.
+
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+
+    :return: List of element ids representing stair types.
     :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     ids = []
-    # get ids from symbols used in dim types
-    idsDimTypes = rAnno.GetSymbolIdsFromDimTypes(doc)
-    # get ids from symbols used in spots
-    idsSpots = rAnno.GetSymbolIdsFromSpotTypes(doc)
-    # get detail types used in model
-    idsUsedInModel = com.GetUsedUnusedTypeIds(doc, GetAllGenericAnnotationTypeIdsByCategory, 1)
-    # build overall list
-    for id in idsUsedInModel:
-        ids.append(id)
-    for id in idsDimTypes:
-        if(id not in ids):
-            ids.append(id)
-    for id in idsSpots:
-        if (id not in ids):
-            ids.append(id)
+    col_cat = get_all_stair_types_by_category(doc)
+    ids = com.get_ids_from_element_collector(col_cat)
     return ids
-    
-# doc   current model document
-def GetUnusedGenericAnnotationTypeIds(doc):
-    '''
-    Returns all unused annotation symbol ids ( unused in model as well as dimension types)
+
+
+def get_all_stair_type_ids_by_class(doc):
+    """
+    Gets all Stair element type ids available in model.
+
+    Ignores in place families of category stair.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: _description_
+    :return: List of element ids representing stair types.
     :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     ids = []
-    idsUsed = GetUsedGenericAnnotationTypeIds(doc)
-    idsAll = GetAllGenericAnnotationTypeIdsByCategory(doc)
-    for id in idsAll:
-        if (id not in idsUsed):
-            ids.append(id)
+    col_class = get_all_stair_types_by_class(doc)
+    ids = com.get_ids_from_element_collector(col_class)
     return ids
 
-# --------------------------------------------- purge functions ------------------
 
-# doc   current document
-def GetUnusedGenericAnnotationIdsForPurge(doc):
-    '''
-    returns symbol(type) ids and family ids (when no type is in use) of in generic anno families which can be purged
+# -------------------------------- In place Stair types -------------------------------------------------------
+
+
+def get_in_place_stair_family_instances(doc):
+    """
+    Gets all instances in place families of category stair.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: _description_
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
+    :return: A filtered element collector containing in place stair family instances.
+    :rtype: Autodesk.Revit.DB.FilteredElementCollector
+    """
+
+    filter = rdb.ElementCategoryFilter(rdb.BuiltInCategory.OST_Stairs)
+    return (
+        rdb.FilteredElementCollector(doc)
+        .OfClass(rdb.FamilyInstance)
+        .WherePasses(filter)
+    )
+
 
-    ids = rFam.GetUnusedInPlaceIdsForPurge(doc, GetUnusedGenericAnnotationTypeIds)
-    return ids
+def get_all_in_place_stair_type_ids(doc):
+    """
+    Gets all type ids off all available in place families of category stair.
+
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+
+    :return: List of element ids
+    :rtype: list of Autodesk.Revit.ElementIds
+    """
+
+    ids = rFam.get_all_in_place_type_ids_in_model_of_category(
+        doc, rdb.BuiltInCategory.OST_Stairs
+    )
+    return ids
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitGeometry.py` & `DuHast-0.0.7/src/duHast/Revit/Common/Geometry/geometry.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Revit geometry extraction helper functions
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -22,293 +22,306 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-from collections import namedtuple
 import clr
+
 clr.AddReference("System.Core")
 from System import Linq
+
 clr.ImportExtensions(Linq)
 
 import Autodesk.Revit.DB as rdb
 
-from duHast.DataSamples import DataGeometry as dGeometry
 
 # ---------------------------- debug ----------------------------
-def GetPointAsString (point):
-    '''
+def get_point_as_string(point):
+    """
     Returns Revit point as a string.
 
     :param point: A revit point.
     :type point: Autodesk.Revit.DB.XYZ
 
     :return: String in format 'X:Y:Z'
     :rtype: str
-    '''
+    """
 
-    return str(point.X) + ' : ' + str(point.Y) + ' : ' + str(point.Z)
-    
-def GetEdgeAsString(edge):
-    '''
+    return str(point.X) + " : " + str(point.Y) + " : " + str(point.Z)
+
+
+def get_edge_as_string(edge):
+    """
     Returns a revit edge as a string.
 
     :param edge: A revit edge.
-    :type edge: Autodesk.Revit.DB.Edge 
+    :type edge: Autodesk.Revit.DB.Edge
 
-    :return: String where each row represents a point on the edge. 
+    :return: String where each row represents a point on the edge.
     :rtype: str
-    '''
+    """
 
-    returnValue = ''
+    returnValue = ""
     for p in edge.Tessellate():
-        returnValue = returnValue + '\n' + GetPointAsString (p)
+        returnValue = returnValue + "\n" + get_point_as_string(p)
     return returnValue
 
+
 # ---------------------------- math utility ----------------------------
 
-def IsClose(a, b, rel_tol=1e-09, abs_tol=0.0):
-    '''
+
+def is_close(a, b, rel_tol=1e-09, abs_tol=0.0):
+    """
     Compares two floats with a tolerance. Returns True if they are close enough, otherwise False
-    
+
     refer to: https://stackoverflow.com/questions/5595425/what-is-the-best-way-to-compare-floats-for-almost-equality-in-python
 
     :param a: A float
     :type a: float
     :param b: A float
     :type b: float
     :param rel_tol: Relative tolerance used to compare the two floats, defaults to 1e-09
     :type rel_tol: float, optional
     :param abs_tol: Absolute tolerance used to compare the two floats, defaults to 0.0
     :type abs_tol: float, optional
 
     :return: Returns True if they are close enough to be considered equal, otherwise False
     :rtype: bool
-    '''
+    """
+
+    return abs(a - b) <= max(rel_tol * max(abs(a), abs(b)), abs_tol)
 
-    return abs(a-b) <= max(rel_tol * max(abs(a), abs(b)), abs_tol)
 
-def ArePointsIdentical(p1, p2):
-    '''
+def are_points_identical(p1, p2):
+    """
     Compares the X,Y,Z values of two revit point and returns True if they are the same, otherwise False
-    
+
     :param p1: A revit point.
     :type p1: Autodesk.Revit.DB.XYZ
     :param p2: A revit point.
     :type p2: Autodesk.Revit.DB.XYZ
 
     :return: True if they are the same, otherwise False.
     :rtype: bool
-    '''
+    """
 
-    if (IsClose(p1.X,p2.X) and IsClose(p1.Y, p2.Y) and IsClose(p1.Z,p2.Z)):
+    if is_close(p1.X, p2.X) and is_close(p1.Y, p2.Y) and is_close(p1.Z, p2.Z):
         return True
     else:
         return False
 
-def CheckDuplicatePoint(points, point):
-    '''
+
+def check_duplicate_point(points, point):
+    """
     Checks whether a collection of points contains another given point and returns True if that is the case.
 
     :param points: List of revit points
     :type points: list Autodesk.Revit.DB.XYZ
     :param point: A revit point.
     :type point: Autodesk.Revit.DB.XYZ
 
     :return: True if point is in collection, otherwise False.
     :rtype: bool
-    '''
+    """
 
     for p1 in points:
-        if(ArePointsIdentical(p1, point)):
+        if are_points_identical(p1, point):
             return True
     return False
 
-def GetPointAsDoubles(point):
-    '''
+
+def get_point_as_doubles(point):
+    """
     Converts a revit XYZ to a list of doubles in order x,y,z.
 
     :param point: A revit point.
     :type point: Autodesk.Revit.DB.XYZ
 
     :return: List of doubles in order of x,y,z
     :rtype: list double
-    '''
+    """
 
     return [point.X, point.Y, point.Z]
 
-def FlattenXYZPoint(point):
-    '''
+
+def flatten_xyz_point(point):
+    """
     Flattens a XYZ point to a UV by omitting the Z value of the XYZ.
 
     https://thebuildingcoder.typepad.com/blog/2008/12/2d-polygon-areas-and-outer-loop.html
 
     :param point: A revit point.
     :type point: Autodesk.Revit.DB.XYZ
 
     :return: A 2D point (UV)
     :rtype:  Autodesk.Revit.DB.UV
-    '''
+    """
 
-    return rdb.UV( point.X, point.Y )
+    return rdb.UV(point.X, point.Y)
 
-def FlattenXYZPointList(polygon):
-    '''
+
+def flatten_xyz_point_list(polygon):
+    """
     Flattens a list of XYZ points to a list of UV points by omitting the Z value of each XYZ.
 
     https://thebuildingcoder.typepad.com/blog/2008/12/2d-polygon-areas-and-outer-loop.html
 
     :param polygon: list of XYZ points
     :type polygon: list Autodesk.Revit.DB.XYZ
-    
+
     :return: list of UV points
     :rtype: list Autodesk.Revit.DB.UV
-    '''
+    """
 
-    z = polygon[0].Z;
+    z = polygon[0].Z
     a = []
-    for p in polygon :
-        if(IsClose(p.Z, z)):
-            #print("expected horizontal polygon" )
+    for p in polygon:
+        if is_close(p.Z, z):
+            # print("expected horizontal polygon" )
             pass
-        a.append( FlattenXYZPoint( p ) )
+        a.append(flatten_xyz_point(p))
     return a
 
-def FlattenXYZPointListOfLists(  polygons ):
-    '''
+
+def flatten_xyz_point_list_of_lists(polygons):
+    """
     Flattens a list lists of XYZ points to a list of lists of UV points by omitting the Z value of each XYZ.
 
     https://thebuildingcoder.typepad.com/blog/2008/12/2d-polygon-areas-and-outer-loop.html
 
     :param polygon: list of lists of XYZ points
     :type polygon: list [list Autodesk.Revit.DB.XYZ]
-    
+
     :return: list of lists of UV points
     :rtype: list [list Autodesk.Revit.DB.UV]
-    '''
-    
+    """
+
     z = polygons[0][0].Z
     a = []
     for polygon in polygons:
-        if IsClose(polygon[0].Z, z ):
-            #print("expected horizontal polygon" )
+        if is_close(polygon[0].Z, z):
+            # print("expected horizontal polygon" )
             pass
-        a.append( FlattenXYZPointList( polygon ) )
+        a.append(flatten_xyz_point_list(polygon))
     return a
 
 
-def GetCoordinateSystemTranslationAndRotation(doc):
-    '''
+def get_coordinate_system_translation_and_rotation(doc):
+    """
     Returns the rotation as a 3 x 3 matrix and the translation as a 1 x 3 matrix of the shared coordinate system active in document.
 
     :param doc: _description_
     :type doc: _type_
 
-    :return: 3 x 3 matrix describing rotation, 1 x 3 matrix describing translation  
+    :return: 3 x 3 matrix describing rotation, 1 x 3 matrix describing translation
     :rtype: list (3) [list(3) int], list [int]
-    '''
+    """
 
     projectLocationActive = doc.ActiveProjectLocation
     # get the inverse because we need to go back to origin
     totalTransform = projectLocationActive.GetTotalTransform().Inverse
-    nBasisX = GetPointAsDoubles(totalTransform.BasisX)
-    nBasisY = GetPointAsDoubles(totalTransform.BasisY)
-    nBasisZ = GetPointAsDoubles(totalTransform.BasisZ)
-    nOrigin = GetPointAsDoubles(totalTransform.Origin)
-    return [nBasisX, nBasisY, nBasisZ],nOrigin
+    nBasisX = get_point_as_doubles(totalTransform.BasisX)
+    nBasisY = get_point_as_doubles(totalTransform.BasisY)
+    nBasisZ = get_point_as_doubles(totalTransform.BasisZ)
+    nOrigin = get_point_as_doubles(totalTransform.Origin)
+    return [nBasisX, nBasisY, nBasisZ], nOrigin
+
 
 # --------------------------------------- is point in polygon ---------------------------------------
 # from  https://thebuildingcoder.typepad.com/blog/2010/12/point-in-polygon-containment-algorithm.html
 # ---------------------------------------------------------------------------------------------------
 
-def GetQuadrant(vertex,  p ):
-    '''
+
+def get_quadrant(vertex, p):
+    """
     Determines the quadrant of a polygon vertex relative to the test point.
 
     https://thebuildingcoder.typepad.com/blog/2010/12/point-in-polygon-containment-algorithm.html
 
     :param vertex: Revit UV element describing a vertex
     :type vertex: Autodesk.Revit.DB.UV
     :param p: Revit UV point
     :type p: Autodesk.Revit.DB.UV
 
     :return: An integer of range 0 - 4 describing the quadrant.
     :rtype: int
-    '''
+    """
 
     returnValue = None
-    if(vertex.U > p.U):
-        if( vertex.V > p.V ):
+    if vertex.U > p.U:
+        if vertex.V > p.V:
             returnValue = 0
         else:
             returnValue = 3
     else:
-        if( vertex.V > p.V ):
+        if vertex.V > p.V:
             returnValue = 1
         else:
             returnValue = 2
     return returnValue
 
-def X_intercept(p, q, y ):
-    '''
+
+def x_intercept(p, q, y):
+    """
     Determine the X intercept of a polygon edge with a horizontal line at the Y value of the test point.
 
     https://thebuildingcoder.typepad.com/blog/2010/12/point-in-polygon-containment-algorithm.html
 
     :param p: Revit UV point
     :type p: Autodesk.Revit.DB.UV
     :param q: Revit UV point
     :type q: Autodesk.Revit.DB.UV
     :param y: _description_
     :type y: double
 
     :return: _description_
     :rtype: double
-    '''
-    if(0 != ( p.V - q.V )):
-        #print('unexpected horizontal segment')
+    """
+    if 0 != (p.V - q.V):
+        # print('unexpected horizontal segment')
         pass
-    
-    return q.U - ( ( q.V - y ) * ( ( p.U - q.U ) / ( p.V - q.V ) ) )
+
+    return q.U - ((q.V - y) * ((p.U - q.U) / (p.V - q.V)))
 
 
-def AdjustDelta(delta, vertex, next_vertex, p ):
-    '''
+def adjust_delta(delta, vertex, next_vertex, p):
+    """
     https://thebuildingcoder.typepad.com/blog/2010/12/point-in-polygon-containment-algorithm.html
 
     :param delta: _description_
     :type delta: _type_
     :param vertex: _description_
     :type vertex: _type_
     :param next_vertex: _description_
     :type next_vertex: _type_
     :param p: _description_
     :type p: _type_
     :return: _description_
     :rtype: _type_
-    '''
+    """
 
     returnValue = delta
     # make quadrant deltas wrap around:
-    if( delta == 3):
+    if delta == 3:
         returnValue = -1
-    elif(delta == -3):
+    elif delta == -3:
         returnValue = 1
     # check if went around point cw or ccw:
-    elif(delta == 2):
+    elif delta == 2:
         returnValue = 2
-    elif(delta == -2):
-        if( X_intercept( vertex, next_vertex, p.V ) > p.U ):
+    elif delta == -2:
+        if x_intercept(vertex, next_vertex, p.V) > p.U:
             returnValue = -delta
     return returnValue
-      
-def IsPointWithinPolygon(polygon, point):
-    '''
+
+
+def is_point_within_polygon(polygon, point):
+    """
     Checks whether a point is within a polygon.
 
     https://thebuildingcoder.typepad.com/blog/2010/12/point-in-polygon-containment-algorithm.html
     odd number of windings rule:
     if (angle & 4) return INSIDE else return OUTSIDE
     non-zero winding rule:
     if (angle != 0) return INSIDE else return OUTSIDE
@@ -316,552 +329,457 @@
     :param polygon: A polygon
     :type polygon: list of Autodesk.Revit.DB.UV
     :param point: A point
     :type point: Autodesk.Revit.DB.UV
 
     :return: Refer winding rules above.
     :rtype: bool
-    '''
+    """
 
     # initialize
-    quad = GetQuadrant(polygon[ 0 ], point )
+    quad = get_quadrant(polygon[0], point)
     angle = 0
 
     # loop on all vertices of polygon
     next_quad = 0
     delta = 0
     n = len(polygon)
     for i in range(n):
-        vertex = polygon[ i ]
+        vertex = polygon[i]
         next_vertex = None
-        if(i + 1 < n):
-            next_vertex = polygon[ i + 1 ]
+        if i + 1 < n:
+            next_vertex = polygon[i + 1]
         else:
             next_vertex = polygon[0]
         # calculate quadrant and delta from last quadrant
-        next_quad = GetQuadrant( next_vertex, point )
+        next_quad = get_quadrant(next_vertex, point)
         delta = next_quad - quad
-        delta = AdjustDelta(delta, vertex, next_vertex, point )
+        delta = adjust_delta(delta, vertex, next_vertex, point)
         # add delta to total angle sum
         angle = angle + delta
         # increment for next step
         quad = next_quad
-    ''' 
+    """ 
     odd number of windings rule:
     if (angle & 4) return INSIDE; else return OUTSIDE;
     non-zero winding rule:
     if (angle != 0) return INSIDE; else return OUTSIDE;
-    '''
+    """
     # complete 360 degrees (angle of + 4 or -4 ) means inside
-    return ( angle == +4 ) or ( angle == -4 )
+    return (angle == +4) or (angle == -4)
+
 
 # --------------------------------------- END --------------------------------------------------
 
-def GetSignedPolygonArea( UVpoints ):
-    '''
+
+def get_signed_polygon_area(uv_points):
+    """
     Calculates the area of a signed UV polygon.
 
     https://thebuildingcoder.typepad.com/blog/2008/12/2d-polygon-areas-and-outer-loop.html
 
-    :param UVpoints: list of points defining the polygon.
-    :type UVpoints: list Autodesk.Revit.DB.UV
+    :param uv_points: list of points defining the polygon.
+    :type uv_points: list Autodesk.Revit.DB.UV
 
     :return: The area of the polygon.
     :rtype: double
-    '''
+    """
 
-    n = len(UVpoints)
-    sum = UVpoints[0].U * ( UVpoints[1].V - UVpoints[n - 1].V )
+    n = len(uv_points)
+    sum = uv_points[0].U * (uv_points[1].V - uv_points[n - 1].V)
     for i in range(1, n - 1):
-        sum += UVpoints[i].U * ( UVpoints[i + 1].V - UVpoints[i - 1].V )
-    sum += UVpoints[n - 1].U * ( UVpoints[0].V - UVpoints[n - 2].V );
+        sum += uv_points[i].U * (uv_points[i + 1].V - uv_points[i - 1].V)
+    sum += uv_points[n - 1].U * (uv_points[0].V - uv_points[n - 2].V)
     return 0.5 * sum
 
-def ConvertEdgeArraysIntoListOfPoints(edgeArrays):
-    '''
+
+def convert_edge_arrays_into_list_of_points(edge_arrays):
+    """
     Converts an edge array into a list of list of revit XYZ points.
 
-    :param edgeArrays: A revit edge array.
-    :type edgeArrays: Autodesk.Revit.DB.EdgeArrayArray ( no not a spelling mistake :) )
+    :param edge_arrays: A revit edge array.
+    :type edge_arrays: Autodesk.Revit.DB.EdgeArrayArray ( no not a spelling mistake :) )
 
     :return: A List of list of revit XYZ points.
     :rtype: list of list Autodesk.Revit.DB.XYZ
-    '''
+    """
 
     polygons = []
-    for loop in edgeArrays:
+    for loop in edge_arrays:
         vertices = []
         q = None
-        firstPoint = True
+        (first_point) = True
         for edge in loop:
             points = edge.Tessellate()
-            if(firstPoint):
+            if first_point:
                 q = points[0]
             n = len(points)
-            for i in range (n-1):
-                vertices.append( points[ i ] )
-            firstPoint = False
+            for i in range(n - 1):
+                vertices.append(points[i])
+            (first_point) = False
         # close the loop by ending with first point...not required(?)
         # vertices.append(q)
         polygons.append(vertices)
     return polygons
 
-def GetEdgePoints(edge):
-    '''
+
+def get_edge_points(edge):
+    """
     Retrieves the revit XYZ points defining an edge (curves get tessellated!)
 
     :param edge: An edge of a solid.
-    :type edge: Autodesk.Revit.DB.Edge 
+    :type edge: Autodesk.Revit.DB.Edge
 
     :return: A list of revit XYZ points.
     :rtype: list Autodesk.Revit.DB.XYZ
-    '''
+    """
 
     points = []
-    for p in  edge.Tessellate():
+    for p in edge.Tessellate():
         points.append(p)
     return points
 
-def ConvertXYZInDataGeometry(doc, dgObject):
-    '''
-    Converts revit XYZ objects stored in a data geometry object into groups of doubles for inner and outer loops\
-        and stores them in new data geometry object. It also populates translation and rotation matrix data of\
-            coordinate system information.
 
-    :param doc: _description_
-    :type doc: _type_
-    :param dgObject: A data geometry object.
-    :type dgObject: :class:`.DataGeometry`
-    
-    :return: A data geometry object.
-    :rtype: :class:`.DataGeometry`
-    '''
-
-    dataGeometry = dGeometry.DataGeometry()
-    outerLoop = []
-    for xyzPoint in dgObject.outerLoop:
-        pointDouble = GetPointAsDoubles(xyzPoint)
-        outerLoop.append(pointDouble)
-    innerLoops = []
-    for innerLoop in dgObject.innerLoops:
-        innerLoopPoints = []
-        for xyzPoint in innerLoop:
-            pointDouble = GetPointAsDoubles(xyzPoint)
-            innerLoopPoints.append(pointDouble)
-        innerLoops.append(innerLoopPoints)
-    dataGeometry.outerLoop = outerLoop
-    dataGeometry.innerLoops = innerLoops
-    # add coordinate system translation and rotation data
-    dataGeometry.rotationCoord, dataGeometry.translationCoord = GetCoordinateSystemTranslationAndRotation(doc)
-    return dataGeometry
-
-def CheckDuplicateEdge(edges, edge):
-    '''
+def check_duplicate_edge(edges, edge):
+    """
     Checks whether a collection contains a given edge and returns True if that is the case.
 
     :param edges: List of edges toi check against.
     :type edges: list of Autodesk.Revit.DB.Edge
     :param edge: An edge
     :type edge: Autodesk.Revit.DB.Edge
 
     :return: True if edge is already in collection, otherwise False.
     :rtype: bool
-    '''
+    """
 
-    flagOverAll = False
-    compPoints = GetEdgePoints(edge)
-    if(len(edges) > 0):
+    flag_over_all = False
+    comp_points = get_edge_points(edge)
+    if len(edges) > 0:
         for e in edges:
-            listPoints = GetEdgePoints(e)
-            if (len(compPoints) == len(listPoints)):
-                edgeSameFlag = True
-                for p1 in compPoints:
-                    if(CheckDuplicatePoint(listPoints, p1) == False):
-                        edgeSameFlag = False
-                if(edgeSameFlag):
-                    flagOverAll = True
+            list_points = get_edge_points(e)
+            if len(comp_points) == len(list_points):
+                edge_same_flag = True
+                for p1 in comp_points:
+                    if check_duplicate_point(list_points, p1) == False:
+                        edge_same_flag = False
+                if edge_same_flag:
+                    flag_over_all = True
                     break
             else:
-              pass
+                pass
     else:
-        pass # flag is already False
-    return flagOverAll
-        
-def CheckSolidIsZeroHeight(solid):
-    '''
+        pass  # flag is already False
+    return flag_over_all
+
+
+def check_solid_is_zero_height(solid):
+    """
     Checks if points making up a solid have multiple Z values.
 
     :param solid: A revit solid object.
     :type solid: Autodesk.Revit.DB.Solid
 
     :return: False if points collection of a solid has multiple z values, True if only one Z value in points collection (2D solid...??)
     :rtype: bool
-    '''
-    
-    return  CheckEdgesAreZeroHeight(solid.Edges)
+    """
+
+    return check_edges_are_zero_height(solid.Edges)
 
-def CheckEdgesAreZeroHeight(edges):
-    '''
+
+def check_edges_are_zero_height(edges):
+    """
     Checks if points making up a edges have multiple Z values.
 
     :param edges: A list of edges.
     :type edges: list Autodesk.Revit.DB.Edge
 
     :return: False if points collection of a edges has multiple z values, True if only one Z value in points collection (2D edges...??)
     :rtype: bool
-    '''
+    """
 
-    lowestZ = 0.0
+    lowest_z = 0.0
     counter = 0
     for edge in edges:
         for p in edge.Tessellate():
-            if (counter == 0):
-                lowestZ = p.Z
+            if counter == 0:
+                lowest_z = p.Z
             else:
-                if(IsClose(p.Z, lowestZ) == False):
+                if is_close(p.Z, lowest_z) == False:
                     # found multiple z
                     return False
             counter = counter + 1
     return True
 
-def GetLowestZFromSolidsPointCollection(solid):
-    '''
+
+def get_lowest_z_from_solid(solid):
+    """
     Gets the lowest Z value in a solids point collection.
 
     :param solid: A solid.
     :type solid: Autodesk.Revit.DB.Solid
 
     :return: The lowest Z value of any point in the solids vertex collection.
     :rtype: double
-    '''
-    
-    return GetLowestZFromSolidsPointCollection(solid.Edges)
+    """
 
-def GetLowestZFromEdgesPointCollection(edges):
-    '''
+    return get_lowest_z_from_edges_point_collection(solid.Edges)
+
+
+def get_lowest_z_from_edges_point_collection(edges):
+    """
     Gets the lowest Z value in a edges collection
 
     :param edges: A list of edges.
     :type edges: list Autodesk.Revit.DB.Edge
 
     :return: The lowest Z value of any point in the edges vertex collection.
     :rtype: double
-    '''
+    """
 
-    lowestZ = 0.0
+    lowest_z = 0.0
     counter = 0
     for edge in edges:
         for p in edge.Tessellate():
             # make sure lowest z is initialized with the first point z values
-            if (counter == 0):
-                lowestZ = p.Z
+            if counter == 0:
+                lowest_z = p.Z
             else:
-                if(IsClose(p.Z, lowestZ) == False and p.Z < lowestZ):
-                    lowestZ = p.Z
-            counter = counter + 1 
-    return lowestZ
+                if is_close(p.Z, lowest_z) == False and p.Z < lowest_z:
+                    lowest_z = p.Z
+            counter = counter + 1
+    return lowest_z
 
-def EdgesAreConnected(edge1, edge2):
-    '''
+
+def edges_are_connected(edge1, edge2):
+    """
     Checks whether edges are connected by comparing their points. If there is an identical point in both\
         then they are connected.
 
     Revit solids dont have crossing edges!
 
     :param edge1: An edge.
     :type edge1: Autodesk.Revit.DB.Edge
     :param edge2: Another edge.
     :type edge2: Autodesk.Revit.DB.Edge
 
     :return: _description_
     :rtype: bool
-    '''
+    """
 
     for p1 in edge1.Tessellate():
         for p2 in edge2.Tessellate():
-            if (ArePointsIdentical(p1, p2)):
+            if are_points_identical(p1, p2):
                 return True
     return False
 
-def GetFacesSortedByAreaFromSolid(solid):
-    '''
+
+def get_faces_sorted_by_area_from_solid(solid):
+    """
     Returns all faces from a solid sorted descending from biggest to smallest by area.
 
     :param solid: A solid.
     :type solid: Autodesk.Revit.DB.Solid
 
     :return: A list of faces, sorted biggest to smallest by area.
     :rtype: list Autodesk.Revit.DB.Face
-    '''
+    """
 
     fl = []
     for face in solid.Faces:
         fl.append(face)
     return sorted(fl, key=lambda x: x.Area, reverse=True)
 
-def PairFacesByArea(faces):
-    '''
+
+def pair_faces_by_area(faces):
+    """
     Returns a list of lists of face pairs, where a nested list contains faces with the same measured area.
-    
+
     Sample would be a ceiling solid. The top and bottom face of that ceiling would be an area pair.
 
     :param faces: A list of faces.
     :type faces: list Autodesk.Revit.DB.Face
 
     :return: A list of lists of faces.
     :rtype: list of list Autodesk.Revit.DB.Face
-    '''
+    """
 
-    returnValue = []
+    return_value = []
     # duplicate faces list since it will be manipulated
-    copyFaces = list(faces)
+    copy_faces = list(faces)
     flag = True
     while flag:
         # loop over faces and try to find some with the same area measured
-        sameArea = [copyFaces[0]]
-        f = copyFaces[0]
-        for i in range (1, len(copyFaces)):
-            if (IsClose(f.Area, copyFaces[i].Area)):
-                sameArea.append(copyFaces[i])
-        returnValue.append(sameArea)
+        same_area = [copy_faces[0]]
+        f = copy_faces[0]
+        for i in range(1, len(copy_faces)):
+            if is_close(f.Area, copy_faces[i].Area):
+                same_area.append(copy_faces[i])
+        return_value.append(same_area)
         # removes faces accounted for
-        for a in sameArea:
-            copyFaces.remove(a)
-        if(len(copyFaces) < 2):
+        for a in same_area:
+            copy_faces.remove(a)
+        if len(copy_faces) < 2:
             flag = False
-    return returnValue
-                    
-def GetFacesWithLowestZFromPairs(facePairs):
-    '''
+    return return_value
+
+
+def get_faces_with_lowest_z_from_pairs(face_pairs):
+    """
     Gets the face with the lowest Z value from list of faces.
 
-    :param facePairs: A list of lists of face pairs, where a nested list contains faces with the same measured area.
-    :type facePairs: list of list Autodesk.Revit.DB.Face
+    :param face_pairs: A list of lists of face pairs, where a nested list contains faces with the same measured area.
+    :type face_pairs: list of list Autodesk.Revit.DB.Face
 
     :return: A list of faces.
     :rtype: list Autodesk.Revit.DB.Face
-    '''
+    """
 
     faces = []
-    for faceP in facePairs:
+    for faceP in face_pairs:
         lowestZ = 0.0
         counter = 0
-        currentFace = None
+        current_face = None
         for face in faceP:
-            currentZ = GetLowestZFromEdgesPointCollection(face.EdgeLoops[0])
-            if(counter == 0):
-                currentFace = face
-                lowestZ = currentZ
+            current_z = get_lowest_z_from_edges_point_collection(face.EdgeLoops[0])
+            if counter == 0:
+                current_face = face
+                lowestZ = current_z
                 counter = counter + 1
             else:
-                if(currentZ < lowestZ):
-                    currentFace = face
-                    lowestZ = currentZ
-        faces.append(currentFace)
+                if current_z < lowestZ:
+                    current_face = face
+                    lowestZ = current_z
+        faces.append(current_face)
     return faces
 
-def GetUniqueHorizontalFaces(faces):
-    '''
+
+def get_unique_horizontal_faces(faces):
+    """
     Filters out any horizontal faces from list of faces past in.
-    
+
     Will also further filter by: faces with the same area only the face with the lower Z value will be returned.
     Note: works only on planar faces
-    
+
     TODO: It could be way simpler just to check for the face with a negative face normal Z value...
 
     :param faces: A list of faces.
     :type faces: list Autodesk.Revit.DB.Face
 
     :return: A list of faces.
     :rtype: list Autodesk.Revit.DB.Face
-    '''
+    """
 
-    facesHorizontal = []
+    faces_horizontal = []
     for f in faces:
         # non planar faces are ignored for the moment...
-        if(type(f) is rdb.PlanarFace):
-            if (f.FaceNormal.Z != 0.0):
-                facesHorizontal.append(f)
-    
-    facesFiltered = []
-    if(len(facesHorizontal) > 1):
+        if type(f) is rdb.PlanarFace:
+            if f.FaceNormal.Z != 0.0:
+                faces_horizontal.append(f)
+
+    faces_filtered = []
+    if len(faces_horizontal) > 1:
         # pair faces by area
-        pairedFaces = PairFacesByArea(facesHorizontal)
+        paired_faces = pair_faces_by_area(faces_horizontal)
         # get faces with lowest Z value for each pair
-        facesFiltered =  GetFacesWithLowestZFromPairs(pairedFaces)
-    return facesFiltered
+        faces_filtered = get_faces_with_lowest_z_from_pairs(paired_faces)
+    return faces_filtered
 
-def IsLoopWithinOtherLoopButNotReferenceLoops(exteriorLoop, otherLoop, holeLoops):
-    '''
+
+def is_loop_within_other_loop_but_not_reference_loops(
+    exterior_loop, other_loop, hole_loops
+):
+    """
     Checks whether any of the other loops is within the exterior loop and if so\
         if it is not also within one of the holeLoops ...that would be an island
     
-    :param exteriorLoop: A polygon loop describing the external boundary of a face.
-    :type exteriorLoop: list of Autodesk.Revit.DB.UV
-    :param otherLoop: A polygon loop which is to be checked as to whether it is within the exterior loop and the any hole loops.
-    :type otherLoop: list of Autodesk.Revit.DB.UV
-    :param holeLoops: A list of named tuples containing .loop property which is a list of UV points forming a polygon which have been identified\
+    :param exterior_loop: A polygon loop describing the external boundary of a face.
+    :type exterior_loop: list of Autodesk.Revit.DB.UV
+    :param other_loop: A polygon loop which is to be checked as to whether it is within the exterior loop and the any hole loops.
+    :type other_loop: list of Autodesk.Revit.DB.UV
+    :param hole_loops: A list of named tuples containing .loop property which is a list of UV points forming a polygon which have been identified\
          as creating a hole in the exteriorLoop.
-    :type holeLoops: namedtuple('uvLoop', 'loop area id threeDPoly')\
+    :type hole_loops: namedtuple('uvLoop', 'loop area id threeDPoly')\
         .Loop is a list of UV points defining a polygon loop
         .area is a double describing the polygon area
         .id is an integer
         .threeDPoly is an edge loop
     
     :return: True if within exterior loop but not within hole loops, otherwise False.
     :rtype: bool
-    '''
+    """
 
-    returnValue = False
+    return_value = False
     # get any point on the loop to check...if it is within the other loop then the entire loop is within the other loop
     # since revit does not allow for overlapping sketches
-    point = otherLoop[0]
+    point = other_loop[0]
     # check whether point is within the other polygon loop
-    if (IsPointWithinPolygon(exteriorLoop, point)):
-        returnValue = True
+    if is_point_within_polygon(exterior_loop, point):
+        return_value = True
         # check whether this point is within the polygon loops identified as holes
         # if so it is actually an island and will be accounted for separately
-        if(len(holeLoops) > 0):
-            for hLoop in holeLoops:
-                if (IsPointWithinPolygon(hLoop.loop, point)):
-                    returnValue = False
+        if len(hole_loops) > 0:
+            for hole_loop in hole_loops:
+                if is_point_within_polygon(hole_loop.loop, point):
+                    return_value = False
                     break
-    return returnValue
+    return return_value
+
 
-def BuildLoopsDictionary(loops):
-    '''
+def build_loops_dictionary(loops):
+    """
     Will return a dic where:
 
     - key is the outer loop of a polygon id
     - values is a list of tuples describing holes in the key polygon
 
     :param loops: A list of named tuples describing polygons.\
         .Loop is a list of UV points defining a polygon loop
         .area is a double describing the polygon area
         .id is an integer
         .threeDPoly is an edge loop
     :type loops: list[namedtuple('uvLoop', 'loop area id threeDPoly')]
 
     :return: A dictionary.
     :rtype: dic {int: list[namedtuple('uvLoop', 'loop area id threeDPoly')]}
-    '''
+    """
 
     # duplicate list since I'am about to manipulate it...
-    copyLoops = list(loops)
+    copy_loops = list(loops)
     flag = False
-    returnValue = {}
+    return_value = {}
     counter = 0
     # check if there is more then one loop  to start with
-    if(len(copyLoops) > 1):
-        loopFlag = True
-        while loopFlag:
+    if len(copy_loops) > 1:
+        loop_flag = True
+        while loop_flag:
             # add the biggest loop as exterior to dictionary (first one in list)
-            key = copyLoops[0].id
-            returnValue[key] = []
+            key = copy_loops[0].id
+            return_value[key] = []
             # assign loop to be checked for holes
-            refLoop = copyLoops[0]
+            reference_loop = copy_loops[0]
             # remove the first exterior loop from list of loops
-            copyLoops.pop(0)
+            copy_loops.pop(0)
             # loop over remaining loops and work out which ones are holes ... if any
-            for loop in copyLoops:
+            for loop in copy_loops:
                 # build list of hole loops already known belonging to this exterior loop
-                holeLoops = []
-                for geoLoop in returnValue[key]:
-                    holeLoops.append(geoLoop)
+                hole_loops = []
+                for geo_loop in return_value[key]:
+                    hole_loops.append(geo_loop)
                 # check whether this is another hole loop
-                flag = IsLoopWithinOtherLoopButNotReferenceLoops(refLoop.loop, loop.loop, holeLoops)
-                if(flag):
-                    returnValue[key].append(loop)
+                flag = is_loop_within_other_loop_but_not_reference_loops(
+                    reference_loop.loop, loop.loop, hole_loops
+                )
+                if flag:
+                    return_value[key].append(loop)
             # remove loops identified as holes from overall list as to avoid double counting
-            for hole in returnValue[key]:
+            for hole in return_value[key]:
                 counter = counter + 1
-                copyLoops.remove(hole)
+                copy_loops.remove(hole)
             # check whether all loops are accounted for
-            if(len(copyLoops) == 0):
-                loopFlag = False
-    elif(len(copyLoops) == 1):
-        key = copyLoops[0].id
+            if len(copy_loops) == 0:
+                loop_flag = False
+    elif len(copy_loops) == 1:
+        key = copy_loops[0].id
         # only one exterior loop exists, no interior loops
-        returnValue[key]=[]
-    return returnValue
-
-
-def ConvertSolidToFlattened2DPoints(solid):
-    '''
-    Converts a solid into a 2D polygon by projecting it onto a plane.( Removes Z values...)
-
-    First nested list is the outer loop, any other following lists describe holes within the area of the polygon defined be points in first list.
-    Arcs, circles will be tessellated to polygons.
-
-    :param solid: A solid.
-    :type solid: Autodesk.Revit.DB.Solid
-
-    :return: A list of data geometry instances.
-    :rtype: list of :class:`.DataGeometry`
-    '''
-
-    '''
-    sample for a sold with multiple sketches:
-    [
-        [
-            [external poly line],[hole],[hole]
-        ],
-        [
-            [external poly line] # without any holes
-        ]
-    ]
-    
-    sort faces into groups by volume:
-    This may be required because a solid can be made up of multiple volumes (extrusion, sweeps etc)
-    Turns out a solid returns a single face for multiple sketches. In order to work out whether these are multiple non overlapping polygons I will need to check
-    whether a point from one polygon is within the other if so it may represents a hole or an island within a hole...to avoid misreading an island for a whole I will need to sort the faces by area
-    and check from largest down to smallest.
-    Also poly lines send back will always only represent: first list: exterior boundary as polygon any follow list is a hole within the polygon. Any islands in those holes will get their own top level representation
-    i.e. no further list nesting!
-
-    Within the faces groups: identify faces which are horizontal: its normal is facing up or down
-    select the face with the lower Z coordinates and
-    group all edges of the above face which form a closed loop (first loop of edges to describe the extend of that face, any secondary loops define holes in face)
-    
-    - > sort all edges by their connections (need to be connected by a point) so they describe a loop <- seems to be ok as revit provides them
-    
-    extract points of edges
-    '''
-
-    ceilingGeos = []
-    # sort faces by size
-    sortedBySizeFaces = GetFacesSortedByAreaFromSolid(solid)
-    # get all faces which are horizontal only
-    horizontalFaces = GetUniqueHorizontalFaces(sortedBySizeFaces)
-    # loop of all horizontal faces and extract loops
-    for hf in horizontalFaces:
-        edgeLoops = ConvertEdgeArraysIntoListOfPoints(hf.EdgeLoops)
-        # convert in UV coordinates
-        edgeLoopsFlattened = FlattenXYZPointListOfLists(edgeLoops)
-        #set up a named tuple to store data in it
-        uvLoops = []
-        uvLoop = namedtuple('uvLoop', 'loop area id threeDPoly')
-        counter = 0
-        for edgeLoopFlat in edgeLoopsFlattened:
-            areaLoop = GetSignedPolygonArea( edgeLoopFlat )
-            uvTuple = uvLoop(edgeLoopFlat, abs(areaLoop), counter, edgeLoops[counter])
-            uvLoops.append(uvTuple)
-            counter += 1
-        uvLoops = sorted(uvLoops, key=lambda x: x.area, reverse=True)
-        # sort loops into exterior and hole loops
-        loopDic = BuildLoopsDictionary(uvLoops)
-        for key in loopDic:
-            dataGeometry = dGeometry.DataGeometry()
-            keyList =[]
-            # find matching loop by id
-            for x in uvLoops:
-                if x.id == key:
-                    keyList = x
-                    break
-            dataGeometry.outerLoop = keyList.threeDPoly
-            if(len(loopDic[key])>0):
-                for hole in loopDic[key]:
-                    dataGeometry.innerLoops.append(hole.threeDPoly)
-            else:
-                dataGeometry.innerLoops = []
-            ceilingGeos.append(dataGeometry)
-    return ceilingGeos
+        return_value[key] = []
+    return return_value
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitGroups.py` & `DuHast-0.0.7/src/duHast/Revit/Common/groups.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Revit groups helper functions.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -23,223 +23,269 @@
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
+
 clr.AddReference("System.Core")
 from System import Linq
+
 clr.ImportExtensions(Linq)
 import System
 
 # import common library modules
-from duHast.APISamples import RevitCommonAPI as com
+from duHast.Revit.Common import common as com
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
-# -------------------------------------------- common variables --------------------
-#: header used in reports
-REPORT_GROUPS_HEADER = ['HOSTFILE','ID', 'NAME', 'GROUP TYPE', 'NUMBER OF INSTANCES']
-
 # --------------------------------------------- utility functions ------------------
 
 # doc   current document
-def GetModelGroups(doc):
-    '''
+def get_model_groups(doc):
+    """
     Get all model group types from the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: list of model group types in the model
     :rtype: list of Autodesk.Revit.DB.
-    '''
+    """
 
-    return rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_IOSModelGroups).WhereElementIsElementType().ToList()
+    return (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_IOSModelGroups)
+        .WhereElementIsElementType()
+        .ToList()
+    )
 
-def GetDetailGroups(doc):
-    '''
+
+def get_detail_groups(doc):
+    """
     Gets all detail groups in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: A list containing detail group types.
     :rtype: list
-    '''
+    """
+
+    return (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_IOSDetailGroups)
+        .WhereElementIsElementType()
+        .ToList()
+    )
 
-    return rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_IOSDetailGroups).WhereElementIsElementType().ToList()
 
-def GetNestedDetailGroups(doc):
-    '''
+def get_nested_detail_groups(doc):
+    """
     Gets all nested detail groups in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: A list containing nested detail group types.
     :rtype: list
-    '''
+    """
+
+    return (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_IOSAttachedDetailGroups)
+        .WhereElementIsElementType()
+        .ToList()
+    )
 
-    return rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_IOSAttachedDetailGroups).WhereElementIsElementType().ToList()
 
-def GetModelGroupIds(doc):
-    '''
+def get_model_group_ids(doc):
+    """
     Gets a list of all model group type ids in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: List of model group type ids
     :rtype: List of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     ids = []
-    col = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_IOSModelGroups).WhereElementIsElementType()
-    ids = com.GetIdsFromElementCollector(col)
+    col = (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_IOSModelGroups)
+        .WhereElementIsElementType()
+    )
+    ids = com.get_ids_from_element_collector(col)
     return ids
 
-def GetDetailGroupIds(doc):
-    '''
+
+def get_detail_group_ids(doc):
+    """
     Gets a list of all detail group types from the model.
 
     This will not include any attached detail groups.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: List of detail group type ids
     :rtype: List of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     ids = []
-    col = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_IOSDetailGroups).WhereElementIsElementType()
-    ids = com.GetIdsFromElementCollector(col)
+    col = (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_IOSDetailGroups)
+        .WhereElementIsElementType()
+    )
+    ids = com.get_ids_from_element_collector(col)
     return ids
 
-def GetNestedDetailGroupIds(doc):
-    '''
+
+def get_nested_detail_group_ids(doc):
+    """
     Gets a list of all nested detail group types from the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: List of nested detail group type ids
     :rtype: List of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     ids = []
-    col = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_IOSAttachedDetailGroups).WhereElementIsElementType()
-    ids = com.GetIdsFromElementCollector(col)
+    col = (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_IOSAttachedDetailGroups)
+        .WhereElementIsElementType()
+    )
+    ids = com.get_ids_from_element_collector(col)
     return ids
-   
-def GetNotPlacedGroups(doc, groupCategory):
-    '''
+
+
+def get_unplaced_groups(doc, group_category):
+    """
     Gets a list of unplaced groups from the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param groupCategory: A built in category defining the group category (model vs detail)
-    :type groupCategory: either BuiltInCategory.OST_IOSDetailGroups or BuiltInCategory.OST_IOSModelGroups
-    
+    :param group_category: A built in category defining the group category (model vs detail)
+    :type group_category: either BuiltInCategory.OST_IOSDetailGroups or BuiltInCategory.OST_IOSModelGroups
+
     :return: List of unplaced group types
     :rtype: list
-    '''
+    """
+
+    def getter_types(doc):
+        return (
+            rdb.FilteredElementCollector(doc)
+            .OfCategory(group_category)
+            .WhereElementIsElementType()
+        )
+
+    def getter_instances(doc):
+        return (
+            rdb.FilteredElementCollector(doc)
+            .OfCategory(group_category)
+            .WhereElementIsNotElementType()
+        )
 
-    def getterTypes(doc):
-        return rdb.FilteredElementCollector(doc).OfCategory(groupCategory).WhereElementIsElementType()
-    def getterInstances(doc):
-        return rdb.FilteredElementCollector(doc).OfCategory(groupCategory).WhereElementIsNotElementType()
     # get unplaced groups
-    return com.GetNotPlacedTypes(
-        doc, 
-        getterTypes, 
-        getterInstances)
+    return com.get_not_placed_types(doc, getter_types, getter_instances)
+
 
-def GetUnplacedDetailGroups(doc):
-    '''
+def get_unplaced_detail_groups(doc):
+    """
     Gets a list of unplaced detail groups from the model
-    
+
     This will not include any attached detail groups.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: List of unplaced detail group types
     :rtype: list
-    '''
+    """
 
-    return GetNotPlacedGroups(doc, rdb.BuiltInCategory.OST_IOSDetailGroups)
+    return get_unplaced_groups(doc, rdb.BuiltInCategory.OST_IOSDetailGroups)
 
-def GetUnplacedDetailGroupIds(doc):
-    '''
+
+def get_unplaced_detail_group_ids(doc):
+    """
     Gets a list of unplaced detail groups type Ids from the model.
-    
+
     This will not include any attached detail groups.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: List of unplaced detail group type ids
     :rtype: List of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
-    unplacedGroups = GetNotPlacedGroups(doc, rdb.BuiltInCategory.OST_IOSDetailGroups)
+    unplaced_groups = get_unplaced_groups(doc, rdb.BuiltInCategory.OST_IOSDetailGroups)
     ids = []
-    for unplaced in unplacedGroups:
+    for unplaced in unplaced_groups:
         ids.append(unplaced.Id)
     return ids
 
-def GetUnplacedNestedDetailGroups(doc):
-    '''
+
+def get_unplaced_nested_detail_groups(doc):
+    """
     Gets a list of unplaced nested detail groups from the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: List of unplaced nested detail group types
     :rtype: list
-    '''
+    """
 
-    return GetNotPlacedGroups(doc, rdb.BuiltInCategory.OST_IOSAttachedDetailGroups)
+    return get_unplaced_groups(doc, rdb.BuiltInCategory.OST_IOSAttachedDetailGroups)
+
+
+def get_unplaced_nested_detail_group_ids(doc):
+    """
+    Gets a list of unplaced nested detail group Ids from the model.
 
-def GetUnplacedNestedDetailGroupIds(doc):
-    '''
-    Gets a list of unplaced nested detail group Ids from the model. 
-    
     This will not list any none nested detail groups.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: List of unplaced model group type ids
     :rtype: List of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
-    unplacedGroups = GetNotPlacedGroups(doc, rdb.BuiltInCategory.OST_IOSAttachedDetailGroups)
+    unplaced_groups = get_unplaced_groups(
+        doc, rdb.BuiltInCategory.OST_IOSAttachedDetailGroups
+    )
     ids = []
-    for unplaced in unplacedGroups:
+    for unplaced in unplaced_groups:
         ids.append(unplaced.Id)
     return ids
 
-def GetUnplacedModelGroups(doc):
-    '''
+
+def get_unplaced_model_groups(doc):
+    """
     Gets a list of unplaced model groups types from the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: List of unplaced model group types
     :rtype: list
-    '''
+    """
 
-    return GetNotPlacedGroups(doc, rdb.BuiltInCategory.OST_IOSModelGroups)
+    return get_unplaced_groups(doc, rdb.BuiltInCategory.OST_IOSModelGroups)
 
-def GetUnplacedModelGroupIds(doc):
-    '''
+
+def get_unplaced_model_group_ids(doc):
+    """
     Gets a list of unplaced model group type Ids from the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: List of unplaced model group type ids
     :rtype: List of Autodesk.Revit.DB.ElementId
-    '''
+    """
 
-    unplacedGroups = GetNotPlacedGroups(doc, rdb.BuiltInCategory.OST_IOSModelGroups)
+    unplaced_groups = get_unplaced_groups(doc, rdb.BuiltInCategory.OST_IOSModelGroups)
     ids = []
-    for unplaced in unplacedGroups:
+    for unplaced in unplaced_groups:
         ids.append(unplaced.Id)
-    return ids
+    return ids
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitLevels.py` & `DuHast-0.0.7/src/duHast/Revit/Levels/levels_appearance.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,544 +1,355 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Revit levels helper functions.
+Revit levels appearance modifier functions.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+
+Note: Any level appearance modification in a view will throw an exception if the level is not actually visible in the view.
+
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2021  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-import clr
-import System
-clr.AddReference("System.Core")
-from System import Linq
-clr.ImportExtensions(Linq)
-
-# import common library modules
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.APISamples import RevitWorksets as rWork
-from duHast.APISamples import RevitFamilyUtils as rFamU
-from duHast.Utilities import Result as res
-from duHast.APISamples import RevitTransaction as rTran
-from duHast.Utilities import Utility as util
-
-# import Autodesk
 import Autodesk.Revit.DB as rdb
 
-# -------------------------------------------- common variables --------------------
-#: header used in reports
-REPORT_LEVELS_HEADER = ['HOSTFILE', 'ID', 'NAME', 'WORKSETNAME', 'ELEVATION']
-
-def get_levels_in_model(doc):
-  '''
-  Get all levels in model
-
-  :param doc: The current model document.
-  :type doc: Autodesk.Revit.DB.Document
-  :return: A collector with all levels in model.
-  :rtype: Autodesk.Revit.DB.FilteredElementCollector
-  '''
-
-  collector = rdb.FilteredElementCollector(doc).OfClass(rdb.Level)
-  return collector
+from duHast.Utilities.Objects import result as res
+from duHast.Revit.Common import transaction as rTran
 
-# --------------------------------------------- visibility functions ------------------
 
-def change_levels_2D (doc, levels, view):
-    '''
+def change_levels_2D(doc, levels, view):
+    """
     Changes all levels in view to 2D
 
+    Note: Any level past in, which is not visible in the view, will throw an exception when attempting to set to 2D.
+
     :param doc: The current model document.
     :type doc: Autodesk.Revit.DB.Document
     :param levels: List of levels to be changed to 2D.
     :type levels: [Autodesk.Revit.DB.Level]
     :param view: The view in which to change the levels
     :type view: Autodesk.Revit.DB.View
-
-    :return: 
+    :return:
         Result class instance.
-
         - result.status. True if all levels where set to 2D, otherwise False.
         - result.message will contain the name(s) of the level(s) changed to 2D
         - result.result empty list
-        
         On exception:
-        
         - result.status (bool) will be False.
         - result.message will contain generic exception message including the level name.
         - result.result will be empty
-
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
+
     # needs to run in a transaction
     def action():
         action_return_value = res.Result()
         level_counter = 0
         for g in levels:
             level_counter = level_counter + 1
             try:
-                g.SetDatumExtentType(rdb.DatumEnds.End1, view, rdb.DatumExtentType.ViewSpecific)
-                g.SetDatumExtentType(rdb.DatumEnds.End0, view, rdb.DatumExtentType.ViewSpecific)
-                action_return_value.UpdateSep(True, 'Changed level {} to 2D.'.format(g.Name))
+                g.SetDatumExtentType(
+                    rdb.DatumEnds.End1, view, rdb.DatumExtentType.ViewSpecific
+                )
+                g.SetDatumExtentType(
+                    rdb.DatumEnds.End0, view, rdb.DatumExtentType.ViewSpecific
+                )
+                action_return_value.update_sep(
+                    True, "Changed level {} to 2D.".format(g.Name)
+                )
             except Exception as e:
-                action_return_value.UpdateSep(False, 'Failed to change level {} to 2D with exception: {}'.format(g.Name, e))
-        if(level_counter == 0):
-            action_return_value.UpdateSep(True, 'No levels visible in view {}'.format(view.Name))
+                action_return_value.update_sep(
+                    False,
+                    "Failed to change level {} to 2D with exception: {}".format(
+                        g.Name, e
+                    ),
+                )
+        if level_counter == 0:
+            action_return_value.update_sep(
+                True, "No levels visible in view {}".format(view.Name)
+            )
         return action_return_value
+
     transaction = rdb.Transaction(doc, "levels to 2D")
     return_value = rTran.in_transaction(transaction, action)
     return return_value
 
-def show_head_end (doc, level, view, end_identifier, show_head):
-    '''
+
+def show_head_end(doc, level, view, end_identifier, show_head):
+    """
     Toggles level head visibility on specified end for given level.
 
     :param doc: The current model document.
     :type doc: Autodesk.Revit.DB.Document
     :param level: The level of which a heads visibility is to be toggled.
     :type level: Autodesk.Revit.DB.Level
     :param view: The view in which a level heads visibility is to be toggled.
     :type view: Autodesk.Revit.DB.View
+    :param end_identifier: which end.
+    :type end_identifier:
     :param show_head: True head will switched on, False it will be switched off
     :type show_head: bool
-
-    :return: 
+    :return:
         Result class instance.
-
         - result.status. True if all levels head(s) visibility was set successfully, otherwise False.
         - result.message will contain the name(s) of the level(s) where a head visibility was set.
         - result.result empty list
-        
         On exception:
-        
         - result.status (bool) will be False.
         - result.message will contain generic exception message including the level name.
         - result.result will be empty
-
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
+
     # needs to run in a transaction
     def action():
         action_return_value = res.Result()
         try:
-            if (show_head):
+            if show_head:
                 level.ShowBubbleInView(end_identifier, view)
-                action_return_value.UpdateSep(True, 'Set level {} head to visible at end: {}'.format(level.Name, end_identifier))
+                action_return_value.update_sep(
+                    True,
+                    "Set level {} head to visible at end: {}".format(
+                        level.Name, end_identifier
+                    ),
+                )
             else:
                 level.HideBubbleInView(end_identifier, view)
-                action_return_value.UpdateSep(True, 'Set level {} head to invisible at end: {}'.format(level.Name, end_identifier))
+                action_return_value.update_sep(
+                    True,
+                    "Set level {} head to invisible at end: {}".format(
+                        level.Name, end_identifier
+                    ),
+                )
         except Exception as e:
-            action_return_value.UpdateSep(False, 'Failed to change level {} head visibility at end {} with exception: {}'.format(level.Name, end_identifier, e))
+            action_return_value.update_sep(
+                False,
+                "Failed to change level {} head visibility at end {} with exception: {}".format(
+                    level.Name, end_identifier, e
+                ),
+            )
         return action_return_value
-    
+
     transaction = rdb.Transaction(doc, "Toggle head. {}".format(show_head))
     return_value = rTran.in_transaction(transaction, action)
     return return_value
 
-def hide_both_heads (doc, levels, view):
-    '''
-    Hides both heads of levels in given view.
 
+def hide_both_heads(doc, levels, view):
+    """
+    Hides both heads of levels in given view.
     :param doc: The current model document.
     :type doc: Autodesk.Revit.DB.Document
     :param level: The level of which a heads visibility is to be toggled.
     :type level: Autodesk.Revit.DB.Level
     :param view: The view in which a level heads visibility is to be toggled.
     :type view: Autodesk.Revit.DB.View
-
-    :return: 
+    :return:
         Result class instance.
-
         - result.status. True if all levels head(s) visibility was switched off successfully, otherwise False.
         - result.message will contain the name(s) of the level(s) where a head visibility was set.
         - result.result empty list
-        
         On exception:
-        
         - result.status (bool) will be False.
         - result.message will contain generic exception message including the level name.
         - result.result will be empty
-
     :rtype: :class:`.Result`
-    '''
-  
+    """
+
     return_value = res.Result()
     for l in levels:
-        return_value.Update(show_head_end(doc, l, view, rdb.DatumEnds.End1, False))
-        return_value.Update( show_head_end(doc, l, view, rdb.DatumEnds.End0, False))
-    
+        return_value.update(show_head_end(doc, l, view, rdb.DatumEnds.End1, False))
+        return_value.update(show_head_end(doc, l, view, rdb.DatumEnds.End0, False))
+
     return return_value
 
-def show_head_zero_end (doc, levels, view):
-    '''
-    Turns on level heads at zero end in specified view.
 
+def show_head_zero_end(doc, levels, view):
+    """
+    Turns on level heads at zero end in specified view.
     :param doc: The current model document.
     :type doc: Autodesk.Revit.DB.Document
     :param level: The levels of which a heads visibility is to be toggled.
     :type level: [Autodesk.Revit.DB.Level]
     :param view: The view in which a level heads visibility is to be toggled.
     :type view: Autodesk.Revit.DB.View
-    
-    :return: 
+    :return:
         Result class instance.
-
         - result.status. True if all levels head(s) visibility at zero end was set to visible successfully, otherwise False.
         - result.message will contain the name(s) of the level(s) where a head visibility was set.
         - result.result empty list
-        
         On exception:
-        
         - result.status (bool) will be False.
         - result.message will contain generic exception message including the level name.
         - result.result will be empty
-
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
     for l in levels:
-        return_value.Update(show_head_end(doc, l, view, rdb.DatumEnds.End0, True))
-    
+        return_value.update(show_head_end(doc, l, view, rdb.DatumEnds.End0, True))
+
     return return_value
 
-def show_head_one_end (doc, levels, view):
-    '''
-    Turns on level heads at One end in specified view.
 
+def show_head_one_end(doc, levels, view):
+    """
+    Turns on level heads at One end in specified view.
     :param doc: The current model document.
     :type doc: Autodesk.Revit.DB.Document
     :param level: The levels of which a heads visibility is to be toggled.
     :type level: [Autodesk.Revit.DB.Level]
     :param view: The view in which a level heads visibility is to be toggled.
     :type view: Autodesk.Revit.DB.View
-    
-    :return: 
+    :return:
         Result class instance.
-
         - result.status. True if all levels head(s) visibility at one end was set to visible successfully, otherwise False.
         - result.message will contain the name(s) of the level(s) where a head visibility was set.
         - result.result empty list
-        
         On exception:
-        
         - result.status (bool) will be False.
         - result.message will contain generic exception message including the level name.
         - result.result will be empty
-
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
     for l in levels:
-        return_value.Update( show_head_end(doc, l, view, rdb.DatumEnds.End1, True))
-    
+        return_value.update(show_head_end(doc, l, view, rdb.DatumEnds.End1, True))
+
     return return_value
 
-def toggle_head_end (doc, level, view, end_identifier):
-    '''
-    Toggles level head visibility on specified end for given level in given views.
 
+def toggle_head_end(doc, level, view, end_identifier):
+    """
+    Toggles level head visibility on specified end for given level in given views.
     :param doc: The current model document.
     :type doc: Autodesk.Revit.DB.Document
     :param level: The level of which a heads visibility is to be toggled.
     :type level: Autodesk.Revit.DB.Level
     :param view: The view in which a level heads visibility is to be toggled.
     :type view: Autodesk.Revit.DB.View
     :param end_identifier: The end of the level to be modified.
     :type view: Autodesk.Revit.DB.DatumEnds
-    
-    
-    :return: 
+    :return:
         Result class instance.
-
         - result.status. True if all levels head(s) visibility was changed successfully, otherwise False.
         - result.message will contain the name(s) of the level(s) where a head visibility was changed.
         - result.result empty list
-        
         On exception:
-        
         - result.status (bool) will be False.
         - result.message will contain generic exception message including the level name.
         - result.result will be empty
-
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
+
     def action():
         try:
             action_return_value = res.Result()
-            end_head_one = level.IsBubbleVisibleInView(end_identifier,view)
-            if(end_head_one == False):
+            end_head_one = level.IsBubbleVisibleInView(end_identifier, view)
+            if end_head_one == False:
                 level.ShowBubbleInView(end_identifier, view)
-                action_return_value.UpdateSep(True, 'Set level {} head to visible at end: {}.'.format(level.Name, end_identifier))
+                action_return_value.update_sep(
+                    True,
+                    "Set level {} head to visible at end: {}.".format(
+                        level.Name, end_identifier
+                    ),
+                )
             else:
                 level.HideBubbleInView(end_identifier, view)
-                action_return_value.UpdateSep(True, 'Set level {} head to not visible at end: {}.'.format(level.Name, end_identifier))
+                action_return_value.update_sep(
+                    True,
+                    "Set level {} head to not visible at end: {}.".format(
+                        level.Name, end_identifier
+                    ),
+                )
         except Exception as e:
-            action_return_value.UpdateSep(False, 'Failed to change level {} head visibility at end: {} with exception: {}'.format(level.Name, end_identifier, e))
+            action_return_value.update_sep(
+                False,
+                "Failed to change level {} head visibility at end: {} with exception: {}".format(
+                    level.Name, end_identifier, e
+                ),
+            )
         return action_return_value
+
     transaction = rdb.Transaction(doc, "Toggle head.")
     return_value = rTran.in_transaction(transaction, action)
     return return_value
 
-def toggle_head_one_end (doc, levels, view ):
-    '''
-    Toggles level head visibility on one end for given levels
 
+def toggle_head_one_end(doc, levels, view):
+    """
+    Toggles level head visibility on one end for given levels
     :param doc: The current model document.
     :type doc: Autodesk.Revit.DB.Document
     :param levels: The levels of which a heads visibility at one end is to be toggled.
     :type levels: [Autodesk.Revit.DB.Level]
     :param view: The view in which a level heads visibility is to be toggled.
     :type view: Autodesk.Revit.DB.View
-    
-    :return: 
+    :return:
         Result class instance.
-
         - result.status. True if all levels head(s) visibility at one end was changed successfully, otherwise False.
         - result.message will contain the name(s) of the level(s) where a head visibility was changed.
         - result.result empty list
-        
         On exception:
-        
         - result.status (bool) will be False.
         - result.message will contain generic exception message including the level name.
         - result.result will be empty
-
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
     for l in levels:
-        return_value.Update( toggle_head_end(doc, l, view, rdb.DatumEnds.End1))
+        return_value.update(toggle_head_end(doc, l, view, rdb.DatumEnds.End1))
     return return_value
-    
-def toggle_head_zero_end (doc, levels, view ):
-    '''
-    Toggles level head visibility on zero end for given levels
 
+
+def toggle_head_zero_end(doc, levels, view):
+    """
+    Toggles level head visibility on zero end for given levels
     :param doc: The current model document.
     :type doc: Autodesk.Revit.DB.Document
     :param levels: The levels of which a head visibility at zero end is to be toggled.
     :type levels: [Autodesk.Revit.DB.Level]
     :param view: The view in which a level heads visibility is to be toggled.
     :type view: Autodesk.Revit.DB.View
-    
-    :return: 
+    :return:
         Result class instance.
-
         - result.status. True if all level head(s) visibility at one end was changed successfully, otherwise False.
         - result.message will contain the name(s) of the level(s) where a head visibility was changed.
         - result.result empty list
-        
         On exception:
-        
         - result.status (bool) will be False.
         - result.message will contain generic exception message including the level name.
         - result.result will be empty
-
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
     for l in levels:
-        return_value.Update(toggle_head_end(doc, l, view, rdb.DatumEnds.End0))
+        return_value.update(toggle_head_end(doc, l, view, rdb.DatumEnds.End0))
     return return_value
-
-# --------------------------------------------- utility functions ------------------
-
-def GetLevelsListAscending(doc):
-    '''
-    Gets a filtered element collector of all levels in the model ascending by project elevation.
-
-    Filters by category.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    :return: A filtered element collector of levels
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Levels).WhereElementIsNotElementType().ToList().OrderBy(lambda l: l.ProjectElevation)
-    return collector
-
-# ------------------------------------------------------- Level reporting --------------------------------------------------------------------
-
-def GetLevelReportData(doc, revitFilePath):
-    '''
-    Gets level data ready for being printed to file.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    :param revitFilePath: The file hostname, which is added to data returned.
-    :type revitFilePath: str
-
-    :return: list of list of revit level properties.
-    :rtype: list of list of str
-    '''
-
-    data = []
-    for p in rdb.FilteredElementCollector(doc).OfClass(rdb.Level):
-        data.append([
-            util.GetFileNameWithoutExt(revitFilePath), 
-            str(p.Id.IntegerValue), 
-            util.EncodeAscii(p.Name), 
-            util.EncodeAscii(rWork.GetWorksetNameById(doc, p.WorksetId.IntegerValue)), 
-            str(p.Elevation)])
-    return data
-
-# ------------------------------------------------- filters --------------------------------------------------------------------
-
-def GetAllLevelHeadsByCategory(doc):
-    '''
-    Gets a filtered element collector of all level head types in the model.
-
-    Filters by category.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A filtered element collector of level heads
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_LevelHeads).WhereElementIsElementType()
-    return collector
-
-def GetAllLevelTypesByCategory(doc):
-    '''
-    Gets a filtered element collector of all level types in the model.
-
-    Filters by category.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A filtered element collector of level types.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Levels).WhereElementIsElementType()
-    return collector
-
-def GetAllLevelTypeIdsByCategory(doc):
-    '''
-    Gets a list of all level type ids in the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of all level type ids.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Levels).WhereElementIsElementType()
-    ids = com.GetIdsFromElementCollector(collector)
-    return ids
-
-# -------------------------------------------------  purge --------------------------------------------------------------------
-
-def GetUnusedLevelTypesForPurge(doc):
-    '''
-    Gets all ids of unused level types in the model.
-
-    Unused: not one instance per level type is placed in the model.
-    This method can be used to safely delete unused level types from the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of level type ids.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    return com.GetUsedUnusedTypeIds(doc, GetAllLevelTypeIdsByCategory, 0, 6)
-
-def GetUnusedLevelHeadFamilies(doc):
-    '''
-    Gets all ids of unused family symbols (types) of level head families.
-
-    Unused: not one instance per symbol is placed in the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of symbol ids.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    usedTypes = com.GetUsedUnusedTypeIds(doc, GetAllLevelTypeIdsByCategory, 1, 6)
-    headsInUseIds = []
-    # get family symbol in use at level as symbol
-    for lId in usedTypes:
-        type = doc.GetElement(lId)
-        id = rParaGet.get_built_in_parameter_value(type, rdb.BuiltInParameter.LEVEL_HEAD_TAG)
-        if(id != None and id not in headsInUseIds):
-            headsInUseIds.append(id)
-    # get all level head symbols available
-    allSymbolsInModel = GetAllLevelHeadsByCategory(doc)
-    unusedSymbolIds = []
-    # filter out unused level head symbols and add to list to be returned
-    for  levelSymbolInModel in  allSymbolsInModel:
-        if(levelSymbolInModel.Id not in headsInUseIds ):
-            unusedSymbolIds.append(levelSymbolInModel.Id)
-    return unusedSymbolIds
-
-def GetAllLevelHeadFamilyTypeIds(doc):
-    '''
-    Gets ids of all level head family symbols (types) in the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of symbol ids.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = []
-    filter = rdb.ElementCategoryFilter(rdb.BuiltInCategory.OST_LevelHeads)
-    col = rdb.FilteredElementCollector(doc).OfClass(rdb.FamilySymbol).WherePasses(filter)
-    ids = com.GetIdsFromElementCollector(col)
-    return ids
-
-# doc             current document
-def GetUnusedLevelHeadFamiliesForPurge(doc):
-    '''
-    Gets ids of all unused level head symbols and families.
-
-    Unused: not one instance per level symbol is placed in the model.
-    This method can be used to safely delete unused level symbols or families from the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    
-    :return: A list of symbol and or family ids.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    return rFamU.GetUnusedInPlaceIdsForPurge(doc, GetUnusedLevelHeadFamilies)
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitLinePatternData.py` & `DuHast-0.0.7/src/duHast/Revit/LinePattern/line_pattern_data.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,65 +1,73 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Family line pattern data class.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-from duHast.APISamples import IFamilyData as IFamData
-from duHast.Utilities import Utility as util
-from duHast.APISamples import RevitCategories as rCats
-from duHast.APISamples import RevitLineStylesPatterns as rPat
-from duHast.APISamples import RevitLevels as rLevel
+from duHast.Revit.Family.Data import ifamily_data as IFamData
+from duHast.Utilities import utility as util
+from duHast.Revit.Categories import categories as rCats
+from duHast.Revit.LinePattern.line_patterns import (
+    get_line_pattern_from_category,
+    get_line_pattern_from_level_element,
+    PROPERTY_PATTERN_ID,
+)
+from duHast.Revit.Levels.levels import get_levels_list_ascending
 
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
 # data dictionary key values specific to this class
-PATTERN_NAME = 'patternName'
-PATTERN_ID = 'patternId'
+PATTERN_NAME = "patternName"
+PATTERN_ID = "patternId"
+
 
 class LinePatternData(IFamData.IFamilyData):
-    
-    def __init__(self, rootPath=None, rootCategoryPath=None, dataType=None):
-        '''
+    def __init__(self, root_path=None, root_category_path=None, data_type=None):
+        """
         Class constructor
 
         :param rootPath: The path of the nested family in a tree: rootFamilyName::nestedFamilyNameOne::nestedFamilyTwo\
             This includes the actual family name as the last node.
         :type rootPath: str
         :param dataType: Human readable data type descriptor
         :type dataType: str
-        '''
+        """
 
-        # todo: check inheritance!!
+        super(LinePatternData, self).__init__(
+            root_path=root_path,
+            root_category_path=root_category_path,
+            data_type=data_type,
+        )
         # super(CategoryData, self).__init__(rootPath, dataType)
-
+        """
         self.data = []
         
         if(dataType != None):
             self.dataType = dataType
         else:
             self.dataType = 'not declared'
         
@@ -68,202 +76,235 @@
         else:
             self.rootPath = '-'
 
         if(rootCategoryPath != None):
             self.rootCategoryPath = rootCategoryPath
         else:
             self.rootCategoryPath = '-'
-    
+        """
 
-    def _addCategoryToDic(self, linePatternIds, patternId, category):
-        '''
+    def _add_category_to_dic(self, line_pattern_ids, pattern_id, category):
+        """
         Adds a category to a dictionary using the line pattern ID as value
 
         :param linePatternIds: dictionary in format: Key: line Pattern Id, value list of categories using that line pattern
         :type linePatternIds: {ElementId:[Autodesk.revit.DB.Category]}
         :param patternId: the pattern element id
         :type patternId: Autodesk.Revit.DB.ElementId
         :param category: the category using the line pattern
         :type category: Autodesk.Revit.DB.Category
-        '''
+        """
 
-        if(patternId in linePatternIds):
-            linePatternIds[patternId].append(category)
+        if pattern_id in line_pattern_ids:
+            line_pattern_ids[pattern_id].append(category)
         else:
-            linePatternIds[patternId] = [category]
+            line_pattern_ids[pattern_id] = [category]
 
-    def _get_LinePatternFromCategories(self, doc):
-        '''
+    def _get_line_pattern_from_categories(self, doc):
+        """
         Loops over all family categories and sub categories and any other categories and sub categories with a positive Id (custom sub category) and
         returns a dictionary of line pattern ids to categories using them.
 
         :param doc: Current family document
         :type doc: Autodesk.Revit.DB.Document
         :return: a dictionary in format: Key: line Pattern Id, value list of categories using that line pattern
         :rtype: {ElementId:[Autodesk.revit.DB.Category]}
-        '''
+        """
 
-        linePatternIdsToCategories = {}
+        line_pattern_ids_to_categories = {}
 
         # get any line pattern added to the family category itself
-        mainCat = rCats.GetFamilyCategory(doc)
-        for mCatName in mainCat:
-            lStyle = rPat.GetLinePatternFromCategory (mainCat[mCatName], doc)
+        main_cat = rCats.get_family_category(doc)
+        for m_cat_name in main_cat:
+            l_style = get_line_pattern_from_category(main_cat[m_cat_name], doc)
             # update dictionary
-            self._addCategoryToDic(linePatternIdsToCategories, lStyle[rPat.PROPERTY_PATTERN_ID], mainCat[mCatName])
-        
+            self._add_category_to_dic(
+                line_pattern_ids_to_categories,
+                l_style[PROPERTY_PATTERN_ID],
+                main_cat[m_cat_name],
+            )
+
         # get line patterns from sub categories of the family category
-        mainCats = rCats.GetMainSubCategories(doc)
-        for mCatName in mainCats:
-            lStyle = rPat.GetLinePatternFromCategory (mainCats[mCatName], doc)
+        main_cats = rCats.get_main_sub_categories(doc)
+        for m_cat_name in main_cats:
+            l_style = get_line_pattern_from_category(main_cats[m_cat_name], doc)
             # update dictionary
-            self._addCategoryToDic(linePatternIdsToCategories, lStyle[rPat.PROPERTY_PATTERN_ID], mainCats[mCatName])
-        
+            self._add_category_to_dic(
+                line_pattern_ids_to_categories,
+                l_style[PROPERTY_PATTERN_ID],
+                main_cats[m_cat_name],
+            )
+
         # get line pattern from unrelated sub categories
-        subCatsOther = rCats.GetOtherSubCategories(doc)
-        for sCatName in subCatsOther:
-            for sCatItem in subCatsOther[sCatName]:
+        sub_cats_other = rCats.get_other_sub_categories(doc)
+        for s_cat_name in sub_cats_other:
+            for s_cat_item in sub_cats_other[s_cat_name]:
                 # only use custom categories not build in ones (id smaller then 0)
-                if(subCatsOther[sCatName][sCatItem].Id.IntegerValue > 0):
-                    lStyle = rPat.GetLinePatternFromCategory (subCatsOther[sCatName][sCatItem], doc)
+                if sub_cats_other[s_cat_name][s_cat_item].Id.IntegerValue > 0:
+                    l_style = get_line_pattern_from_category(
+                        sub_cats_other[s_cat_name][s_cat_item], doc
+                    )
                     # update dictionary
-                    self._addCategoryToDic(linePatternIdsToCategories, lStyle[rPat.PROPERTY_PATTERN_ID], subCatsOther[sCatName][sCatItem])
-        
+                    self._add_category_to_dic(
+                        line_pattern_ids_to_categories,
+                        l_style[PROPERTY_PATTERN_ID],
+                        sub_cats_other[s_cat_name][s_cat_item],
+                    )
+
         # get line pattern from reference lines and planes categories import in families main cat
-        otherCats = rCats.GetCategoryByBuiltInDefName(
-            doc, [
-            rdb.BuiltInCategory.OST_ReferenceLines, # reference lines
-            rdb.BuiltInCategory.OST_CLines,     # reference planes
-            rdb.BuiltInCategory.OST_ImportObjectStyles] # import in families
+        other_cats = rCats.get_category_by_built_in_def_name(
+            doc,
+            [
+                rdb.BuiltInCategory.OST_ReferenceLines,  # reference lines
+                rdb.BuiltInCategory.OST_CLines,  # reference planes
+                rdb.BuiltInCategory.OST_ImportObjectStyles,
+            ],  # import in families
         )
-        for oCat in otherCats:
-            lStyle = rPat.GetLinePatternFromCategory (oCat, doc)
+        for o_cat in other_cats:
+            l_style = get_line_pattern_from_category(o_cat, doc)
             # update dictionary
-            self._addCategoryToDic(linePatternIdsToCategories, lStyle[rPat.PROPERTY_PATTERN_ID], oCat)
-        
-        return linePatternIdsToCategories
+            self._add_category_to_dic(
+                line_pattern_ids_to_categories, l_style[PROPERTY_PATTERN_ID], o_cat
+            )
 
+        return line_pattern_ids_to_categories
 
-    def _getPatternFromLevelElement(self, doc):
-        '''
+    def _get_pattern_from_level_element(self, doc):
+        """
         Gets the pattern data from all level types in document.
 
         :param doc: Current family document
         :type doc: Autodesk.Revit.DB.Document
 
         :return: a dictionary in format: Key: line Pattern Id, value list of levels using that line pattern
         :rtype: {ElementId:[Autodesk.revit.DB.Category]}
-        '''
-        
-        levelPatternData = {}
-        levels = rLevel.GetLevelsListAscending(doc)
+        """
+
+        level_pattern_data = {}
+        levels = get_levels_list_ascending(doc)
         for level in levels:
-            patternData = rPat.GetLinePatternFromLevelElement(doc, level)
-            self._addCategoryToDic(levelPatternData, patternData[rPat.PROPERTY_PATTERN_ID], level)
-        return levelPatternData
+            pattern_data = get_line_pattern_from_level_element(doc, level)
+            self._add_category_to_dic(
+                level_pattern_data, pattern_data[PROPERTY_PATTERN_ID], level
+            )
+        return level_pattern_data
 
-    def _getPatternName(self, element):
-        '''
+    def _get_pattern_name(self, element):
+        """
         Get the element name.
 
         :param element: _description_
         :type element: _type_
         :return: Element name, or exception stating name is not unicode
         :rtype: str
-        '''
+        """
 
-        elementName = 'unknown_notUnicode'
-        try:   
-            elementName = util.EncodeAscii(rdb.Element.Name.GetValue(element))
+        element_name = "unknown_notUnicode"
+        try:
+            element_name = util.encode_ascii(rdb.Element.Name.GetValue(element))
         except Exception as ex:
-            elementName = elementName + ' Exception: ' + str(ex)
-        return elementName
+            element_name = element_name + " Exception: " + str(ex)
+        return element_name
 
-    def _getPatternUsageDataFromCategories(self, linePatternIds, element):
-        '''
+    def _get_pattern_usage_data_from_categories(self, line_pattern_ids, element):
+        """
         Returns how often and on which category a line pattern is used
 
         :param linePatternIds: a dictionary in format: Key: line Pattern Id, value list of categories using that line pattern
         :type linePatternIds: {ElementId:[Autodesk.revit.DB.Category]}
         :param element: The line pattern element.
         :type element: _type_
-        
+
         :return: counter and  a list of dictionaries in format {categoryId: int, categoryName: str}
         :rtype: int, [{categoryId:int, categoryName:str}]
-        '''
+        """
 
         counter = 0
-        patternNames = []
+        pattern_names = []
         # how often used
-        if (element.Id in linePatternIds):
-            counter = len(linePatternIds[element.Id])
-            for pat in  linePatternIds[element.Id]:
-                patternNames.append({"categoryId" : pat.Id.IntegerValue, "categoryName" : pat.Name})
-        return counter, patternNames
+        if element.Id in line_pattern_ids:
+            counter = len(line_pattern_ids[element.Id])
+            for pat in line_pattern_ids[element.Id]:
+                pattern_names.append(
+                    {"categoryId": pat.Id.IntegerValue, "categoryName": pat.Name}
+                )
+        return counter, pattern_names
 
-    def _getPatternUsageDataFromLevel(self, linePatternIds, element):
-        '''
+    def _get_pattern_usage_data_from_level(self, line_pattern_ids, element):
+        """
         Returns how often and on which Level type a line pattern is used
 
-        :param linePatternIds: 
+        :param linePatternIds:
         :type linePatternIds: {ElementId:[Autodesk.revit.DB.Category]}
         :param element: The line pattern element.
         :type element: _type_
-        
+
         :return: counter and  a list of dictionaries in format {categoryId: int, categoryName: str}
         :rtype: int, [{categoryId:int, categoryName:str}]
-        '''
+        """
 
         counter = 0
-        patternNames = []
+        pattern_names = []
 
         # how often used
-        if (element.Id in linePatternIds):
-            counter = len(linePatternIds[element.Id])
-            for pat in  linePatternIds[element.Id]:
-                patternNames.append({"levelId" : pat.Id.IntegerValue, "levelTypeName" : rdb.Element.Name.GetValue(pat)})
-        return counter, patternNames
+        if element.Id in line_pattern_ids:
+            counter = len(line_pattern_ids[element.Id])
+            for pat in line_pattern_ids[element.Id]:
+                pattern_names.append(
+                    {
+                        "levelId": pat.Id.IntegerValue,
+                        "levelTypeName": rdb.Element.Name.GetValue(pat),
+                    }
+                )
+        return counter, pattern_names
 
     def process(self, doc):
-        '''
+        """
         Collects all line pattern data from the document and stores it in the class property .data
 
         :param doc: Current family document
         :type doc: Autodesk.Revit.DB.Document
-        '''
+        """
 
-        # get all line patterns used in categories (includes sub categories of family category and any custom subcategories of non family category present, includes also 
+        # get all line patterns used in categories (includes sub categories of family category and any custom subcategories of non family category present, includes also
         # ref planes , ref lines, import styles)
-        linePatternIdsByCategory = self._get_LinePatternFromCategories(doc)
+        line_pattern_ids_by_category = self._get_line_pattern_from_categories(doc)
         # get line pattern used on level element
-        linePatternIdsByFromLevel = self._getPatternFromLevelElement(doc)
+        line_pattern_ids_by_from_level = self._get_pattern_from_level_element(doc)
 
         collector = rdb.FilteredElementCollector(doc).OfClass(rdb.LinePatternElement)
         for element in collector:
             # just in case parameter name is not unicode
-            elementName = self._getPatternName(element)
+            element_name = self._get_pattern_name(element)
             # get usage data from categories
-            counter, patternNames = self._getPatternUsageDataFromCategories(linePatternIdsByCategory, element)
+            counter, pattern_names = self._get_pattern_usage_data_from_categories(
+                line_pattern_ids_by_category, element
+            )
             # get usage data from levels
-            counterLevel, patternNamesLevel = self._getPatternUsageDataFromLevel(linePatternIdsByFromLevel, element)
-            
+            (
+                counter_level,
+                pattern_names_level,
+            ) = self._get_pattern_usage_data_from_level(
+                line_pattern_ids_by_from_level, element
+            )
+
             # get overall count
-            counter = counter + counterLevel
+            counter = counter + counter_level
             # get overall usage data
-            usageAll = patternNames + patternNamesLevel
+            usage_all = pattern_names + pattern_names_level
 
             # build data
             self.data.append(
                 {
-                    IFamData.ROOT : self.rootPath,
-                    IFamData.ROOT_CATEGORY : self.rootCategoryPath,
-                    IFamData.FAMILY_NAME : self._stripFileExtension(doc.Title),
-                    IFamData.FAMILY_FILE_PATH : doc.PathName,
-                    IFamData.USAGE_COUNTER : counter,
-                    IFamData.USED_BY : usageAll,
-                    PATTERN_NAME : elementName,
-                    PATTERN_ID : element.Id.IntegerValue
+                    IFamData.ROOT: self.root_path,
+                    IFamData.ROOT_CATEGORY: self.root_category_path,
+                    IFamData.FAMILY_NAME: self._strip_file_extension(doc.Title),
+                    IFamData.FAMILY_FILE_PATH: doc.PathName,
+                    IFamData.USAGE_COUNTER: counter,
+                    IFamData.USED_BY: usage_all,
+                    PATTERN_NAME: element_name,
+                    PATTERN_ID: element.Id.IntegerValue,
                 }
             )
-    
-    def get_Data(self):
+
+    def get_data(self):
         return self.data
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitLineStylesPatterns.py` & `DuHast-0.0.7/src/duHast/Revit/LinePattern/line_patterns.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,298 +1,285 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Revit line styles and line patterns helper functions. 
+Revit line line patterns helper functions. 
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2020  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
+
 clr.AddReference("System.Core")
 from System import Linq
+
 clr.ImportExtensions(Linq)
 import System
 
 # import common library modules
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.Utilities import Result as res
+from duHast.Revit.Common import delete as rDel, parameter_get_utils as rParaGet
+from duHast.Utilities.Objects import result as res
 
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
 # -------------------------------------------------PATTERN PROPERTIES ------------
 
 #: pattern name
-PROPERTY_PATTERN_NAME = 'PatternName'
+PROPERTY_PATTERN_NAME = "PatternName"
 #: pattern name default value, hard coded solid line pattern name
-PROPERTY_PATTERN_NAME_VALUE_DEFAULT = 'Solid'
+PROPERTY_PATTERN_NAME_VALUE_DEFAULT = "Solid"
 #: pattern id
-PROPERTY_PATTERN_ID = 'PatternId'
+PROPERTY_PATTERN_ID = "PatternId"
 
-def GetLinePatternFromCategory(cat, doc):
-    '''
+
+def get_line_pattern_from_category(cat, doc):
+    """
     Returns the line pattern properties as a dictionary\
          where keys are pattern name and pattern id.
 
     :param cat: A category.
     :type cat: Autodesk.REvit.DB.Category
     :param doc: Current Revit family document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: A dictionary.
     :rtype: dictionary {str: str, str: Autodesk.Revit.DB.ElementId}
-    '''
+    """
 
-    dicPattern = {}
-    dicPattern[PROPERTY_PATTERN_NAME] = PROPERTY_PATTERN_NAME_VALUE_DEFAULT
-    dicPattern[PROPERTY_PATTERN_ID] = patternId = cat.GetLinePatternId(rdb.GraphicsStyleType.Projection)
-    '''check for 'solid' pattern which apparently is not a pattern at all
+    dic_pattern = {}
+    dic_pattern[PROPERTY_PATTERN_NAME] = PROPERTY_PATTERN_NAME_VALUE_DEFAULT
+    dic_pattern[PROPERTY_PATTERN_ID] = pattern_id = cat.GetLinePatternId(
+        rdb.GraphicsStyleType.Projection
+    )
+    """check for 'solid' pattern which apparently is not a pattern at all
     *The RevitAPI.chm documents says: Note that Solid is special. It isn't a line pattern at all -- 
     * it is a special code that tells drawing and export code to use solid lines rather than patterned lines. 
     * Solid is visible to the user when selecting line patterns. 
-    '''
-    if(patternId != rdb.LinePatternElement.GetSolidPatternId()):
+    """
+    if pattern_id != rdb.LinePatternElement.GetSolidPatternId():
         # not a solid line pattern
         collector = rdb.FilteredElementCollector(doc).OfClass(rdb.LinePatternElement)
-        linePatternElement = None
+        line_pattern_element = None
         for c in collector:
-            if(patternId == c.Id):
-                dicPattern[PROPERTY_PATTERN_NAME] = rdb.Element.Name.GetValue(c)         
-    return dicPattern
+            if pattern_id == c.Id:
+                dic_pattern[PROPERTY_PATTERN_NAME] = rdb.Element.Name.GetValue(c)
+    return dic_pattern
+
 
-def GetLinePatternFromLevelElement(doc, level):
-    '''
+def get_line_pattern_from_level_element(doc, level):
+    """
     Returns the line pattern properties as a dictionary\
          where keys are pattern name and pattern id.
 
     :param doc: Current Revit family document.
     :type doc: Current Revit family document.
     :param level: a level element
     :type level: Autodesk.Revit.DB.Level
 
     :return: A dictionary.
     :rtype: dictionary {str: str, str: Autodesk.Revit.DB.ElementId}
-    '''
+    """
 
-    dicPattern = {}
-    dicPattern[PROPERTY_PATTERN_NAME] = PROPERTY_PATTERN_NAME_VALUE_DEFAULT
-    dicPattern[PROPERTY_PATTERN_ID] = rdb.ElementId.InvalidElementId
+    dic_pattern = {}
+    dic_pattern[PROPERTY_PATTERN_NAME] = PROPERTY_PATTERN_NAME_VALUE_DEFAULT
+    dic_pattern[PROPERTY_PATTERN_ID] = rdb.ElementId.InvalidElementId
     try:
-        lTypeId = level.GetTypeId()
-        levelType = doc.GetElement(lTypeId)
-        linePatternIdString = rParaGet.get_built_in_parameter_value(levelType, rdb.BuiltInParameter.LINE_PATTERN)
-        dicPattern[PROPERTY_PATTERN_ID] = rdb.ElementId(int(linePatternIdString))
-        dicPattern[PROPERTY_PATTERN_NAME] = rdb.Element.Name.GetValue(levelType)
+        l_type_id = level.GetTypeId()
+        level_type = doc.GetElement(l_type_id)
+        line_pattern_id_string = rParaGet.get_built_in_parameter_value(
+            level_type, rdb.BuiltInParameter.LINE_PATTERN
+        )
+        dic_pattern[PROPERTY_PATTERN_ID] = rdb.ElementId(int(line_pattern_id_string))
+        dic_pattern[PROPERTY_PATTERN_NAME] = rdb.Element.Name.GetValue(level_type)
     except Exception as ex:
-        dicPattern[PROPERTY_PATTERN_NAME] = str(ex)
-    return dicPattern
+        dic_pattern[PROPERTY_PATTERN_NAME] = str(ex)
+    return dic_pattern
+
 
 # ------------------------------------------------ DELETE LINE PATTERNS ----------------------------------------------
 
-def DeleteLinePatternsContains(doc, contains):
-    '''
+
+def delete_line_patterns_contains(doc, contains):
+    """
     Deletes all line patterns where the names contains a provided string
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :param contains: Filter: pattern name needs to contain this string to be deleted.
     :type contains: str
 
-    :return: 
+    :return:
         Result class instance.
-           
+
         - .result = True if line pattern where deleted successfully. Otherwise False.
         - .message will contain delete status per pattern.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     lps = rdb.FilteredElementCollector(doc).OfClass(rdb.LinePatternElement).ToList()
-    ids = list(lp.Id for lp in lps if lp.GetLinePattern().Name.Contains(contains)).ToList[rdb.ElementId]()
-    result = com.DeleteByElementIds(doc,ids, 'Deleting line patterns where name contains: ' + str(contains),'line patterns containing: ' + str(contains))
+    ids = list(
+        lp.Id for lp in lps if lp.GetLinePattern().Name.Contains(contains)
+    ).ToList[rdb.ElementId]()
+    result = rDel.delete_by_element_ids(
+        doc,
+        ids,
+        "Deleting line patterns where name contains: " + str(contains),
+        "line patterns containing: " + str(contains),
+    )
     return result
 
-def DeleteLinePatternStartsWith(doc, startsWith):
-    '''
+
+def delete_line_pattern_starts_with(doc, starts_with):
+    """
     Deletes all line patterns where the name starts with provided string.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param startsWith: Filter: pattern name needs to start with this string to be deleted.
-    :type startsWith: str
+    :param starts_with: Filter: pattern name needs to start with this string to be deleted.
+    :type starts_with: str
 
-    :return: 
+    :return:
         Result class instance.
 
         - .result = True if line pattern where deleted successfully. Otherwise False.
         - .message will contain delete status per pattern.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     lps = rdb.FilteredElementCollector(doc).OfClass(rdb.LinePatternElement).ToList()
-    ids = list(lp.Id for lp in lps if lp.GetLinePattern().Name.StartsWith(startsWith)).ToList[rdb.ElementId]()
-    result = com.DeleteByElementIds(doc,ids, 'Delete line patterns where name starts with: ' + str(startsWith),'line patterns starting with: ' + str(startsWith))
+    ids = list(
+        lp.Id for lp in lps if lp.GetLinePattern().Name.StartsWith(starts_with)
+    ).ToList[rdb.ElementId]()
+    result = rDel.delete_by_element_ids(
+        doc,
+        ids,
+        "Delete line patterns where name starts with: " + str(starts_with),
+        "line patterns starting with: " + str(starts_with),
+    )
     return result
 
-def DeleteLinePatternsWithout(doc, contains):
-    '''
+
+def delete_line_patterns_without(doc, contains):
+    """
     Deletes all line patterns where the name does not contain the provided string.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :param contains: Filter: pattern name needs not to contain this string to be deleted.
     :type contains: str
 
-    :return: 
+    :return:
         Result class instance.
 
         - .result = True if line pattern where deleted successfully. Otherwise False.
         - .message will contain delete status per pattern.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     lps = rdb.FilteredElementCollector(doc).OfClass(rdb.LinePatternElement).ToList()
     ids = list(lp.Id for lp in lps).ToList[rdb.ElementId]()
-    idsContain = list(lp.Id for lp in lps if lp.GetLinePattern().Name.Contains(contains)).ToList[rdb.ElementId]()
-    deleteIds = list(set(ids)-set(idsContain))
-    result = com.DeleteByElementIds(doc,deleteIds, 'Delete line patterns where name does not contain: ' + str(contains),'line patterns without: ' + str(contains))
+    ids_contain = list(
+        lp.Id for lp in lps if lp.GetLinePattern().Name.Contains(contains)
+    ).ToList[rdb.ElementId]()
+    delete_ids = list(set(ids) - set(ids_contain))
+    result = rDel.delete_by_element_ids(
+        doc,
+        delete_ids,
+        "Delete line patterns where name does not contain: " + str(contains),
+        "line patterns without: " + str(contains),
+    )
     return result
 
-def GetAllLinePatterns(doc):
-    '''
+
+def get_all_line_patterns(doc):
+    """
     Gets all line patterns in the model.
 
     :param doc: _description_
     :type doc: _type_
 
     :return: List of all line pattern elements in model.
     :rtype: list of Autodesk.Revit.DB.LinePatternElement
-    '''
+    """
     return rdb.FilteredElementCollector(doc).OfClass(rdb.LinePatternElement).ToList()
 
-def BuildPatternsDictionaryByName(doc):
-    '''
+
+def build_patterns_dictionary_by_name(doc):
+    """
     Returns a dictionary where line pattern name is key, values are all ids of line patterns with the exact same name.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: A dictionary where line pattern name is key, values are all ids of line patterns with the exact same name
     :rtype: dictionary(key str, value list of Autodesk.Revit.DB.ElementId)
-    '''
+    """
 
-    lpDic = {}
+    lp_dic = {}
     lps = rdb.FilteredElementCollector(doc).OfClass(rdb.LinePatternElement)
     for lp in lps:
-        if(lpDic.has_key(lp.GetLinePattern().Name)):
-            lpDic[lp.GetLinePattern().Name].append(lp.Id)
+        if lp_dic.has_key(lp.GetLinePattern().Name):
+            lp_dic[lp.GetLinePattern().Name].append(lp.Id)
         else:
-            lpDic[lp.GetLinePattern().Name] = [lp.Id]
-    return lpDic
+            lp_dic[lp.GetLinePattern().Name] = [lp.Id]
+    return lp_dic
 
-def DeleteDuplicatLinePatterNames(doc):
-    '''
+
+def delete_duplicate_line_patter_names(doc):
+    """
     Deletes all but the first line pattern by Id with the exact same name.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: 
+    :return:
         Result class instance.
 
         - .result = True if all views where deleted. Otherwise False.
         - .message will contain deletion status.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
-    returnValue.AppendMessage('Deletes all but the first line pattern by Id with the exact same name...start')
+    return_value = res.Result()
+    return_value.append_message(
+        "Deletes all but the first line pattern by Id with the exact same name...start"
+    )
     # get a dictionary: Key pattern name, value all ids of line patterns with the same name
     # anything where the value list is greater then 1 means duplicates of the same name...
-    linePatterns = BuildPatternsDictionaryByName(doc)
-    for key, value in linePatterns.items():
-        if(len(value) > 1):
+    line_patterns = build_patterns_dictionary_by_name(doc)
+    for key, value in line_patterns.items():
+        if len(value) > 1:
             # keep the first one (original)
             value.remove(value[0])
-            flagDelete = com.DeleteByElementIds(doc,value, 'Deleting duplicate line patterns names: ' + str(key),'line patterns duplicates: ' + str(key))
-            returnValue.Update (flagDelete)
-    return returnValue
-
-# ------------------------------------------------ DELETE LINE STYLES ----------------------------------------------
-
-def DeleteLineStylesStartsWith(doc, startsWith):
-    '''
-    Deletes all line styles where the name starts with provided string
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    :param startsWith: Filter: style name needs to start with this string to be deleted.
-    :type startsWith: str
-
-    :return: 
-        Result class instance.
-
-        - .result = True if all views where deleted. Otherwise False.
-        - .message will contain deletion status.
-
-    :rtype: :class:`.Result`
-    '''
-
-    lc = doc.Settings.Categories[rdb.BuiltInCategory.OST_Lines]
-    ids = list(c.Id for c in lc.SubCategories if c.Name.StartsWith(startsWith)).ToList[rdb.ElementId]()
-    result = com.DeleteByElementIds(doc,ids, 'Delete line styles where name starts with: ' + str(startsWith),'line styles starting with: ' + str(startsWith))
-    return result
-
-def GetAllLineStyleIds(doc):
-    '''
-    Gets all line styles ids in the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of all line style ids.
-    :rtype: list of Autodesk.Revit.DB.ElementId
-    '''
-
-    lc = doc.Settings.Categories[rdb.BuiltInCategory.OST_Lines]
-    ids = list(c.Id for c in lc.SubCategories).ToList[rdb.ElementId]()
-    return ids
-
-# ------------------------------------------------ Fill Patterns ----------------------------------------------
-
-def GetAllFillPattern(doc):
-    '''
-    Gets all fill pattern element ids in the model.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A list of all fill pattern elements.
-    :rtype: list of Autodesk.Revit.DB.FillPatternElement
-    '''
-
-    return rdb.FilteredElementCollector(doc).OfClass(rdb.FillPatternElement).ToList()
+            flag_delete = rDel.delete_by_element_ids(
+                doc,
+                value,
+                "Deleting duplicate line patterns names: {}".format(key),
+                "line patterns duplicates: {}".format(key),
+            )
+            return_value.update(flag_delete)
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitModelHealth.py` & `DuHast-0.0.7/src/duHast/Revit/ModelHealth/model_health.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,18 +1,18 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Model health report functions.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 Model health report metrics can either be displayed in a family where each parameter is assigned to a metric 
 and or data can be exported to text files which can be used to visualize key metrics over time.
 
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -27,768 +27,908 @@
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
+import os
+
 clr.AddReference("System.Core")
 from System import Linq
+
 clr.ImportExtensions(Linq)
 import System
 
-from duHast.Utilities import Utility as util
-from duHast.APISamples import RevitBIM360 as b360
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.Utilities import Result as res
-from duHast.APISamples import RevitDesignSetOptions as rDoS
-from duHast.APISamples import RevitWarnings as rWarn
-from duHast.APISamples import RevitWorksets as rWork
-from duHast.APISamples import RevitViews as rViews
-from duHast.APISamples import RevitLineStylesPatterns as rLsp
-from duHast.APISamples import RevitLinks as rLinks
-from duHast.APISamples import RevitModelHealthReportFileNames as rFns
-from duHast.APISamples import RevitFamilyUtils as rFams
-from duHast.APISamples import RevitGroups as rGrp
-from duHast.APISamples import RevitRooms as rRooms
-from duHast.APISamples import RevitDetailItems as rDetItems
-from duHast.APISamples import RevitElementParameterSetUtils as rParaSet
+from duHast.Revit.BIM360 import bim_360 as b360
+
+# from duHast.APISamples.Common import RevitCommonAPI as com
+from duHast.Utilities.Objects import result as res
+from duHast.Utilities import date_stamps as dateStamp, files_io as fileIO
+from duHast.Revit.Common import design_set_options as rDoS
+from duHast.Revit.Warnings import warnings as rWarn
+from duHast.Revit.Common import worksets as rWork
+from duHast.Revit.Views import sheets as rViewSheets
+from duHast.Revit.Views import views as rViews
+from duHast.Revit.LinePattern import line_patterns as rLinePat
+from duHast.Revit.LinePattern import fill_patterns as rFill
+from duHast.Revit.LinePattern import line_styles as rLineStyle
+from duHast.Revit.Links import cad_links as rCadLink
+from duHast.Revit.Links import image_links as rImageLink
+from duHast.Revit.ModelHealth.Reporting import report_file_names as rFns
+from duHast.Revit.Family import family_utils as rFams
+from duHast.Revit.Common import groups as rGrp
+from duHast.Revit.Rooms import rooms as rRooms
+from duHast.Revit.DetailItems import detail_items as rDetItems
+from duHast.Revit.Common import parameter_set_utils as rParaSet
+from duHast.Utilities.files_csv import write_report_data_as_csv
 
 import Autodesk.Revit.DB as rdb
 from System.Collections.Generic import List
 from collections import namedtuple
 
 # constants
 
 #: A revit family displaying the health metrics retrieved by this code.
-MODEL_HEALTH_TRACKER_FAMILY = 'Symbol_GraphicModelHealth_ANN'
+MODEL_HEALTH_TRACKER_FAMILY = "Symbol_GraphicModelHealth_ANN"
 #: Default value if unable to retrieve a health metric value from model
 FAILED_TO_RETRIEVE_VALUE = -1
 
-def _castParameterValue(pValue):
-    '''
+
+def _cast_parameter_value(p_value):
+    """
     Check if parameter is of type string ( currently the date only)
     and only cast to string if not...
 
-    :param pValue: The parameter value
-    :type pValue: unknown
+    :param p_value: The parameter value
+    :type p_value: unknown
     :return: The parameter value as a string
     :rtype: str
-    '''
-    
-    newParaValue = ''
-    if(pValue.GetType() != System.String):
-        newParaValue = str(pValue)
+    """
+
+    new_para_value = ""
+    if p_value.GetType() != System.String:
+        new_para_value = str(p_value)
     else:
-        newParaValue = pValue
-    return newParaValue
+        new_para_value = p_value
+    return new_para_value
+
 
-def GetInstancesOfModelHealth(doc):
-    '''
+def get_instances_of_model_health(doc):
+    """
     Gets all instances of the model health tracker family in a model.
 
     Built in parameter containing family name when filtering familyInstance elements:
     BuiltInParameter.ELEM_FAMILY_PARAM
     This is a faster filter in terms of performance then LINQ query refer to:
     https://jeremytammik.github.io/tbc/a/1382_filter_shortcuts.html
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: A list containing all model health tracker families in the model.
     :rtype: list of Autodesk.Revit.DB.FamilyInstance
-    '''
+    """
 
-    provider = rdb.ParameterValueProvider(rdb.ElementId(rdb.BuiltInParameter.ELEM_FAMILY_PARAM))
+    provider = rdb.ParameterValueProvider(
+        rdb.ElementId(rdb.BuiltInParameter.ELEM_FAMILY_PARAM)
+    )
     evaluator = rdb.FilterStringEquals()
-    rule = rdb.FilterStringRule( provider, evaluator, MODEL_HEALTH_TRACKER_FAMILY, True )
-    filter = rdb.ElementParameterFilter( rule )
-    return rdb.FilteredElementCollector(doc).OfClass(rdb.FamilyInstance).WherePasses(filter).ToList()
+    rule = rdb.FilterStringRule(provider, evaluator, MODEL_HEALTH_TRACKER_FAMILY, True)
+    filter = rdb.ElementParameterFilter(rule)
+    return (
+        rdb.FilteredElementCollector(doc)
+        .OfClass(rdb.FamilyInstance)
+        .WherePasses(filter)
+        .ToList()
+    )
+
 
-def GetParametersOfInstance(famInstance, doc):
-    '''
+def get_parameters_of_instance(fam_instance, doc):
+    """
     Updates parameter values of model tracker family instance.
 
-    :param famInstance: An instance of the model health tracker family.
-    :type famInstance: Autodesk.Revit.DB.FamilyInstance
+    :param fam_instance: An instance of the model health tracker family.
+    :type fam_instance: Autodesk.Revit.DB.FamilyInstance
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: 
+    :return:
         Result class instance.
-        
+
         - .result = True if all parameters where found on the family and got updated successfully or no update at all was required. Otherwise False.
         - .message will be 'Failed to get value for'
-    
+
     :rtype: :class:`.Result`
-    '''
+    """
 
-    resultValue = res.Result()
-    flagUpdate = False
-    for p in famInstance.GetOrderedParameters():
+    result_value = res.Result()
+    flag_update = False
+    for p in fam_instance.GetOrderedParameters():
         # check if parameter is read only
-        if(p.IsReadOnly == False):
+        if p.IsReadOnly == False:
             # check an action to update this parameter value exists
-            if(PARAM_ACTIONS.ContainsKey(p.Definition.Name)):
-                parameterValue = PARAM_ACTIONS[p.Definition.Name].getData(doc)
-                if(parameterValue != FAILED_TO_RETRIEVE_VALUE):
-                    flag = rParaSet.set_parameter_value (p, _castParameterValue(parameterValue), doc)
-                    resultValue.Update(flag)
-                    flagUpdate = True
+            if PARAM_ACTIONS.ContainsKey(p.Definition.Name):
+                parameter_value = PARAM_ACTIONS[p.Definition.Name].get_data(doc)
+                if parameter_value != FAILED_TO_RETRIEVE_VALUE:
+                    flag = rParaSet.set_parameter_value(
+                        p, _cast_parameter_value(parameter_value), doc
+                    )
+                    result_value.update(flag)
+                    flag_update = True
                 else:
-                    resultValue.UpdateSep(False, 'Failed to get value for ' + p.Definition.Name)
-    if(flagUpdate == False):
-        resultValue.message = 'No family parameters where updated'
-        resultValue.status = True
-    return resultValue
+                    result_value.update_sep(
+                        False, "Failed to get value for " + p.Definition.Name
+                    )
+    if flag_update == False:
+        result_value.message = "No family parameters where updated"
+        result_value.status = True
+    return result_value
+
 
 # ----------------------------------------------
-# model properties 
+# model properties
 # ----------------------------------------------
 
 # --------------------------------------------- GENERAL ---------------------------------------------
 
-def GetCurrentDate(doc):
-    '''
+
+def get_current_date(doc):
+    """
     Get the current date
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: The current date in format YYYY_MM_DD.
     :rtype: str
 
-    '''
-    return util.GetFileDateStamp(util.FILE_DATE_STAMP_YYYY_MM_DD)
+    """
+    return dateStamp.get_file_date_stamp(dateStamp.FILE_DATE_STAMP_YYYY_MM_DD)
 
-def GetWorksetNumber(doc):
-    '''
+
+def get_workset_number(doc):
+    """
     Gets the number of worksets in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: The number of worksets in a model.
     :rtype: int
-    '''
+    """
+
+    return len(rWork.get_worksets(doc))
 
-    return len(rWork.GetWorksets(doc))
 
-def GetFileSize(doc):
-    '''
+def get_file_size(doc):
+    """
     Gets the file size in MB.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: File size in MB. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     size = FAILED_TO_RETRIEVE_VALUE
     try:
         # get the path from the document
         # this will fail if not a file based doc or the document is detached
-        revitFilePath = doc.PathName
+        revit_file_path = doc.PathName
         # check if bim 360 file
-        if (revitFilePath.StartsWith('BIM 360')):
-            size = b360.GetModelFileSize(doc)
+        if revit_file_path.StartsWith("BIM 360"):
+            size = b360.get_model_file_size(doc)
         else:
-            if(util.FileExist(revitFilePath)):
+            if fileIO.file_exist(revit_file_path):
                 # get file size in MB
-                size = util.GetFileSize(revitFilePath)
+                size = fileIO.get_file_size(revit_file_path)
     except:
         pass
     return size
 
-def GetNumberOfWarnings(doc):
-    '''
+
+def get_number_of_warnings(doc):
+    """
     Gets the number of warnings in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of warnings in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rWarn.GetWarnings(doc))
+        number = len(rWarn.get_warnings(doc))
     except:
         pass
     return number
 
-def GetNumberOfDesignSets(doc):
-    '''
+
+def get_number_of_design_sets(doc):
+    """
     Gets the number of design sets in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of design sets in model. On exception it will return -1
     :rtype: int
-    '''
+    """
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rDoS.GetDesignSets(doc))
+        number = len(rDoS.get_design_sets(doc))
     except:
         pass
     return number
 
-def GetNumberOfDesignOptions(doc):
-    '''
+
+def get_number_of_design_options(doc):
+    """
     Gets the number of design options in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of design option in model. On exception it will return -1
     :rtype: int
-    '''
+    """
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rDoS.GetDesignOptions(doc).ToList())
+        number = len(rDoS.get_design_options(doc).ToList())
     except:
         pass
     return number
 
+
 # --------------------------------------------- VIEWS ---------------------------------------------
 
-def GetNumberOfSheets(doc):
-    '''
+
+def get_number_of_sheets(doc):
+    """
     Gets the number of sheets in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of sheets in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rViews.GetSheetsInModel(doc))
+        number = len(rViewSheets.get_all_sheets(doc).ToList())
     except:
         pass
     return number
 
-def _ViewFilter(view):
-    '''
+
+def _view_filter(view):
+    """
     generic view filter allowing all views to be selected
 
     :param view: not used!
     :type view: Autodesk.Revit.DB.View
 
     :return: returns always True
     :rtype: bool
-    '''
+    """
     return True
 
-def GetViewsInTheModel(doc):
-    '''
+
+def get_number_of_views(doc):
+    """
     Gets the number of views in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of views in model. On exception it will return -1
     :rtype: int
-    '''
+    """
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rViews.GetViewsInModel(doc, _ViewFilter))
+        number = len(rViews.get_views_in_model(doc, _view_filter))
     except:
         pass
     return number
 
-def GetUnplacedViews(doc):
-    '''
+
+def get_number_of_unplaced_views(doc):
+    """
     Gets the number of unplaced views in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of unplaced views in model. On exception it will return -1
     :rtype: int
-    '''
+    """
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rViews.GetViewsNotOnSheet(doc))
+        number = len(rViews.get_views_not_on_sheet(doc))
     except:
         pass
     return number
 
+
 # --------------------------------------------- LINE STYLES / TYPES  ---------------------------------------------
 
-def GetNumberOfLineStyles(doc):
-    '''
+
+def get_number_of_line_styles(doc):
+    """
     Gets the number of line styles in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of line styles in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rLsp.GetAllLineStyleIds(doc))
+        number = len(rLineStyle.get_all_line_style_ids(doc))
     except:
         pass
     return number
 
-def GetNumberOfLinePatterns(doc):
-    '''
+
+def get_number_of_line_patterns(doc):
+    """
     Gets the number of line patterns in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of line patterns in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rLsp.GetAllLinePatterns(doc))
+        number = len(rLinePat.get_all_line_patterns(doc))
     except:
         pass
     return number
 
-def GetNumberOfFillPatterns(doc):
-    '''
+
+def get_number_of_fill_patterns(doc):
+    """
     Gets the number of fill pattern in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of fill pattern in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rLsp.GetAllFillPattern(doc))
+        number = len(rFill.get_all_fill_pattern(doc))
     except Exception as e:
         pass
     return number
 
+
 # --------------------------------------------- CAD links  ---------------------------------------------
 
-def GetNumberOfCADImports(doc):
-    '''
+
+def get_number_of_cad_imports(doc):
+    """
     Gets the number of CAD imports in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of CAD imports in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rLinks.GetCADTypeImportsOnly(doc))
+        number = len(rCadLink.get_cad_type_imports_only(doc))
     except:
         pass
     return number
 
-def GetNumberOfCADLinksToModel(doc):
-    '''
+
+def get_number_of_cad_links_to_model(doc):
+    """
     Gets the number of CAD links by model in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of CAD links by model in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rLinks.GetAllCADLinkTypeInModelOnly(doc))
+        number = len(rCadLink.get_all_cad_link_type_in_model_only(doc))
     except:
         pass
     return number
 
-def GetNumberOfCADLinksToView(doc):
-    '''
+
+def get_number_of_cad_links_to_view(doc):
+    """
     Gets the number of CAD links by view in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of CAD links by view in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rLinks.GetAllCADLinkTypeByViewOnly(doc))
+        number = len(rCadLink.get_all_cad_link_type_by_view_only(doc))
     except:
         pass
     return number
 
+
 # ---------------------------------------------  images  ---------------------------------------------
 
-def GetNumberOfImageImports(doc):
-    '''
+
+def get_number_of_image_imports(doc):
+    """
     Gets the number of image imports in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of image imports in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rLinks.GetAllImageLinkTypeImportedInModel(doc))
+        number = len(rImageLink.get_all_image_link_type_imported_in_model(doc))
     except:
         pass
     return number
 
-def GetNumberOfImageLinks(doc):
-    '''
+
+def get_number_of_image_links(doc):
+    """
     Gets the number of image links in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of image links in model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rLinks.GetAllImageLinkTypeLinkedInModel(doc))
+        number = len(rImageLink.get_all_image_link_type_linked_in_model(doc))
     except:
         pass
     return number
 
+
 # ---------------------------------------------  Families  ---------------------------------------------
 
-def GetNumberOfFamiliesInModel(doc):
-    '''
+
+def get_number_of_families(doc):
+    """
     Gets the number of families loaded into the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of families loaded into model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rFams.GetAllLoadableFamilies(doc))
+        number = len(rFams.get_all_loadable_families(doc))
     except:
         pass
     return number
 
-def GetNumberOfInPlaceFamiliesInModel(doc):
-    '''
+
+def get_number_of_in_place_families(doc):
+    """
     Gets the number of in-place families the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of in-place in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rFams.GetAllInPlaceFamilies(doc))
+        number = len(rFams.get_all_in_place_families(doc))
     except:
         pass
     return number
 
+
 # ---------------------------------------------  Groups  ---------------------------------------------
 
-def GetNumberOfDetailGroupsInModel(doc):
-    '''
+
+def get_number_of_detail_groups(doc):
+    """
     Gets the number of detail group definitions the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of detail group definitions in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rGrp.GetDetailGroups(doc))
+        number = len(rGrp.get_detail_groups(doc))
     except:
         pass
     return number
 
-def GetNumberOfModelGroupsInModel(doc):
-    '''
+
+def get_number_of_model_groups(doc):
+    """
     Gets the number of model group definitions in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of model group definitions in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rGrp.GetModelGroups(doc))
+        number = len(rGrp.get_model_groups(doc))
     except:
         pass
     return number
 
-def GetNumberOfUnplacedDetailGroupsInModel(doc):
-    '''
+
+def get_number_of_unplaced_detail_groups(doc):
+    """
     Gets the number of unplaced detail group definitions in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of unplaced detail group definitions in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rGrp.GetUnplacedDetailGroups(doc))
+        number = len(rGrp.get_unplaced_detail_groups(doc))
     except:
         pass
     return number
 
-def GetNumberOfUnplacedModelGroupsInModel(doc):
-    '''
+
+def get_number_of_unplaced_model_groups(doc):
+    """
     Gets the number of unplaced model group definitions in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of unplaced model group definitions in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rGrp.GetUnplacedModelGroups(doc))
+        number = len(rGrp.get_unplaced_model_groups(doc))
     except:
         pass
     return number
 
+
 # ---------------------------------------------  Rooms  ---------------------------------------------
 
-def GetNumberOfRoomsInModel(doc):
-    '''
+
+def get_number_of_rooms(doc):
+    """
     Gets the number of rooms in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of rooms in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rRooms.GetAllRooms(doc))
+        number = len(rRooms.get_all_rooms(doc))
     except:
         pass
     return number
 
-def GetNumberOfUnplacedRoomsInModel(doc):
-    '''
+
+def get_number_of_unplaced_rooms(doc):
+    """
     Gets the number of unplaced rooms in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of unplaced rooms in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rRooms.GetUnplacedRooms(doc))
+        number = len(rRooms.get_unplaced_rooms(doc))
     except:
         pass
     return number
 
-def GetNumberOfRedundantRoomsInModel(doc):
-    '''
+
+def get_number_of_redundant_rooms(doc):
+    """
     Gets the number of redundant rooms in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of redundant rooms in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rRooms.GetRedundantRooms(doc))
+        number = len(rRooms.get_redundant_rooms(doc))
     except:
         pass
     return number
 
-def GetNumberOfNotEnclosedRoomsInModel(doc):
-    '''
+
+def get_number_of_not_enclosed_rooms(doc):
+    """
     Gets the not enclosed number of rooms in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of not enclosed rooms in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
 
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rRooms.GetNotEnclosedRooms(doc))
+        number = len(rRooms.get_not_enclosed_rooms(doc))
     except:
         pass
     return number
 
+
 # ---------------------------------------------  Detail Items  ---------------------------------------------
 
-def GetNumberOfFilledRegionInModel(doc):
-    '''
+
+def get_number_of_filled_regions(doc):
+    """
     Gets the number of filled region instances in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: Number of filled region instances in the model. On exception it will return -1
     :rtype: int
-    '''
+    """
     number = FAILED_TO_RETRIEVE_VALUE
     try:
-        number = len(rDetItems.GetFilledRegionsInModel(doc))
+        number = len(rDetItems.get_filled_regions_in_model(doc))
     except:
         pass
     return number
 
+
 # ----------------------------------------------
-# main 
+# main
 # ----------------------------------------------
 
-#set up a named tuple to store data in it
-healthDataAction = namedtuple('healthDataAction', 'getData reportFileName')
+# set up a named tuple to store data in it
+health_data_action = namedtuple("healthDataAction", "get_data report_file_name")
 
 #: List of actions reporting model health metrics and their associated parameter name
 PARAM_ACTIONS = {
-    'ValueWorksets': healthDataAction(GetWorksetNumber, rFns.PARAM_ACTIONS_FILENAME_NO_OF_WORKSETS),
-    'ValueFileSize': healthDataAction(GetFileSize, rFns.PARAM_ACTIONS_FILENAME_FILE_SIZE),
-    'ValueWarnings': healthDataAction(GetNumberOfWarnings, rFns.PARAM_ACTIONS_FILENAME_NO_OF_WARNINGS),
-    'ValueDesignSets': healthDataAction(GetNumberOfDesignSets, rFns.PARAM_ACTIONS_FILENAME_NO_OF_DESIGN_SETS),
-    'ValueDesignOptions': healthDataAction(GetNumberOfDesignOptions, rFns.PARAM_ACTIONS_FILENAME_NO_OF_DESIGN_OPTIONS),
-    'ValueSheets': healthDataAction(GetNumberOfSheets, rFns.PARAM_ACTIONS_FILENAME_NO_OF_SHEETS),
-    'ValueViews': healthDataAction(GetViewsInTheModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_VIEWS),
-    'ValueViewsNotPlaced': healthDataAction(GetUnplacedViews, rFns.PARAM_ACTIONS_FILENAME_NO_OF_VIEWS_NOT_PLACED),
-    'ValueLineStyles': healthDataAction(GetNumberOfLineStyles, rFns.PARAM_ACTIONS_FILENAME_NO_OF_LINE_STYLES),
-    'ValueLinePatterns': healthDataAction(GetNumberOfLinePatterns, rFns.PARAM_ACTIONS_FILENAME_NO_OF_LINE_PATTERNS),
-    'ValueFillPatterns': healthDataAction(GetNumberOfFillPatterns, rFns.PARAM_ACTIONS_FILENAME_NO_OF_FILL_PATTERNS),
-    'ValueCADImports': healthDataAction(GetNumberOfCADImports, rFns.PARAM_ACTIONS_FILENAME_NO_OF_CAD_IMPORTS),
-    'ValueCADLinksToModel': healthDataAction(GetNumberOfCADLinksToModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_CAD_LINKS_MODEL),
-    'ValueCADLinksToView': healthDataAction(GetNumberOfCADLinksToView, rFns.PARAM_ACTIONS_FILENAME_NO_OF_CAD_LINKS_VIEW),
-    'ValueImageImports': healthDataAction(GetNumberOfImageImports, rFns.PARAM_ACTIONS_FILENAME_NO_OF_IMAGE_IMPORTS),
-    'ValueImageLinks': healthDataAction(GetNumberOfImageLinks, rFns.PARAM_ACTIONS_FILENAME_NO_OF_IMAGE_LINKS),
-    'ValueFamilies': healthDataAction(GetNumberOfFamiliesInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_FAMILIES),
-    'ValueFamiliesInPlace': healthDataAction(GetNumberOfInPlaceFamiliesInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_FAMILIES_IN_PLACE),
-    'ValueModelGroups': healthDataAction(GetNumberOfModelGroupsInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_MODEL_GROUPS),
-    'ValueModelGroupsUnplaced': healthDataAction(GetNumberOfUnplacedModelGroupsInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_MODEL_GROUPS_UNPLACED),
-    'ValueDetailGroups': healthDataAction(GetNumberOfDetailGroupsInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS),
-    'ValueDetailGroupsUnplaced': healthDataAction(GetNumberOfUnplacedDetailGroupsInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS_UNPLACED),
-    'ValueRooms': healthDataAction(GetNumberOfRoomsInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_ROOMS),
-    'ValueRoomsUnplaced': healthDataAction(GetNumberOfUnplacedRoomsInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNPLACED),
-    'ValueRoomsNotEnclosed': healthDataAction(GetNumberOfNotEnclosedRoomsInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNENCLOSED),
-    'ValueRoomsRedundant': healthDataAction(GetNumberOfRedundantRoomsInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_REDUNDANT),
-    'ValueFilledRegions': healthDataAction(GetNumberOfFilledRegionInModel, rFns.PARAM_ACTIONS_FILENAME_NO_OF_FILLED_REGIONS),
-    'ValueDateLastUpdated' : healthDataAction(GetCurrentDate, rFns.PARAM_ACTIONS_FILENAME_DATE_LAST_UPDATED)
+    "ValueWorksets": health_data_action(
+        get_workset_number, rFns.PARAM_ACTIONS_FILENAME_NO_OF_WORKSETS
+    ),
+    "ValueFileSize": health_data_action(
+        get_file_size, rFns.PARAM_ACTIONS_FILENAME_FILE_SIZE
+    ),
+    "ValueWarnings": health_data_action(
+        get_number_of_warnings, rFns.PARAM_ACTIONS_FILENAME_NO_OF_WARNINGS
+    ),
+    "ValueDesignSets": health_data_action(
+        get_number_of_design_sets, rFns.PARAM_ACTIONS_FILENAME_NO_OF_DESIGN_SETS
+    ),
+    "ValueDesignOptions": health_data_action(
+        get_number_of_design_options, rFns.PARAM_ACTIONS_FILENAME_NO_OF_DESIGN_OPTIONS
+    ),
+    "ValueSheets": health_data_action(
+        get_number_of_sheets, rFns.PARAM_ACTIONS_FILENAME_NO_OF_SHEETS
+    ),
+    "ValueViews": health_data_action(
+        get_number_of_views, rFns.PARAM_ACTIONS_FILENAME_NO_OF_VIEWS
+    ),
+    "ValueViewsNotPlaced": health_data_action(
+        get_number_of_unplaced_views, rFns.PARAM_ACTIONS_FILENAME_NO_OF_VIEWS_NOT_PLACED
+    ),
+    "ValueLineStyles": health_data_action(
+        get_number_of_line_styles, rFns.PARAM_ACTIONS_FILENAME_NO_OF_LINE_STYLES
+    ),
+    "ValueLinePatterns": health_data_action(
+        get_number_of_line_patterns, rFns.PARAM_ACTIONS_FILENAME_NO_OF_LINE_PATTERNS
+    ),
+    "ValueFillPatterns": health_data_action(
+        get_number_of_fill_patterns, rFns.PARAM_ACTIONS_FILENAME_NO_OF_FILL_PATTERNS
+    ),
+    "ValueCADImports": health_data_action(
+        get_number_of_cad_imports, rFns.PARAM_ACTIONS_FILENAME_NO_OF_CAD_IMPORTS
+    ),
+    "ValueCADLinksToModel": health_data_action(
+        get_number_of_cad_links_to_model,
+        rFns.PARAM_ACTIONS_FILENAME_NO_OF_CAD_LINKS_MODEL,
+    ),
+    "ValueCADLinksToView": health_data_action(
+        get_number_of_cad_links_to_view,
+        rFns.PARAM_ACTIONS_FILENAME_NO_OF_CAD_LINKS_VIEW,
+    ),
+    "ValueImageImports": health_data_action(
+        get_number_of_image_imports, rFns.PARAM_ACTIONS_FILENAME_NO_OF_IMAGE_IMPORTS
+    ),
+    "ValueImageLinks": health_data_action(
+        get_number_of_image_links, rFns.PARAM_ACTIONS_FILENAME_NO_OF_IMAGE_LINKS
+    ),
+    "ValueFamilies": health_data_action(
+        get_number_of_families, rFns.PARAM_ACTIONS_FILENAME_NO_OF_FAMILIES
+    ),
+    "ValueFamiliesInPlace": health_data_action(
+        get_number_of_in_place_families,
+        rFns.PARAM_ACTIONS_FILENAME_NO_OF_FAMILIES_IN_PLACE,
+    ),
+    "ValueModelGroups": health_data_action(
+        get_number_of_model_groups, rFns.PARAM_ACTIONS_FILENAME_NO_OF_MODEL_GROUPS
+    ),
+    "ValueModelGroupsUnplaced": health_data_action(
+        get_number_of_unplaced_model_groups,
+        rFns.PARAM_ACTIONS_FILENAME_NO_OF_MODEL_GROUPS_UNPLACED,
+    ),
+    "ValueDetailGroups": health_data_action(
+        get_number_of_detail_groups, rFns.PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS
+    ),
+    "ValueDetailGroupsUnplaced": health_data_action(
+        get_number_of_unplaced_detail_groups,
+        rFns.PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS_UNPLACED,
+    ),
+    "ValueRooms": health_data_action(
+        get_number_of_rooms, rFns.PARAM_ACTIONS_FILENAME_NO_OF_ROOMS
+    ),
+    "ValueRoomsUnplaced": health_data_action(
+        get_number_of_unplaced_rooms, rFns.PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNPLACED
+    ),
+    "ValueRoomsNotEnclosed": health_data_action(
+        get_number_of_not_enclosed_rooms,
+        rFns.PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNENCLOSED,
+    ),
+    "ValueRoomsRedundant": health_data_action(
+        get_number_of_redundant_rooms, rFns.PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_REDUNDANT
+    ),
+    "ValueFilledRegions": health_data_action(
+        get_number_of_filled_regions, rFns.PARAM_ACTIONS_FILENAME_NO_OF_FILLED_REGIONS
+    ),
+    "ValueDateLastUpdated": health_data_action(
+        get_current_date, rFns.PARAM_ACTIONS_FILENAME_DATE_LAST_UPDATED
+    ),
 }
 
-def UpdateModelHealthTracerFamily(doc, revitFilePath):
-    '''
+
+def update_model_health_tracer_family(doc, revit_file_path):
+    """
     Updates instances of model health tracker family in project.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param revitFilePath: Fully qualified revit model file path.
-    :type revitFilePath: str
+    :param revit_file_path: Fully qualified revit model file path.
+    :type revit_file_path: str
 
-    :return: 
+    :return:
         Result class instance.
-           
+
         - .result = True if all model key health metric where updated successfully. Otherwise False.
         - .message will be listing each parameter update: old value to new value
-    
+
     :rtype: :class:`.Result`
-    '''
+    """
 
-    revitFileName = util.GetFileNameWithoutExt(revitFilePath)
-    resultValue = res.Result()
-    instances = GetInstancesOfModelHealth(doc)
-    if(len(instances) > 0):
+    revit_file_name = fileIO.get_file_name_without_ext(revit_file_path)
+    result_value = res.Result()
+    instances = get_instances_of_model_health(doc)
+    if len(instances) > 0:
         for instance in instances:
-            updateFlag = GetParametersOfInstance(instance, doc)
-            resultValue.Update(updateFlag)
+            update_flag = get_parameters_of_instance(instance, doc)
+            result_value.update(update_flag)
     else:
-        resultValue.UpdateSep(False, 'Family to update ' + MODEL_HEALTH_TRACKER_FAMILY + ' was not found in model: '+ revitFileName)
-    return resultValue
+        result_value.update_sep(
+            False,
+            "Family to update: {} was not found in model: {}".format(
+                MODEL_HEALTH_TRACKER_FAMILY, revit_file_name
+            ),
+        )
+    return result_value
+
 
 # doc   current document
 # revitFilePath     path of the current document
-def WriteModelHealthReport(doc, revitFilePath, outputDirectory):
-    '''
+def write_model_health_report(doc, revit_file_path, output_directory):
+    """
     Write out health tracker data to file.
 
     Each value gets written to a separate file. The file name is made up of time stamp and the revit file name.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param revitFilePath: Fully qualified revit model file path.
-    :type revitFilePath: str
-    :param outputDirectory: The directory path of where to write the data to.
-    :type outputDirectory: str
+    :param revit_file_path: Fully qualified revit model file path.
+    :type revit_file_path: str
+    :param output_directory: The directory path of where to write the data to.
+    :type output_directory: str
 
-    :return: 
+    :return:
         Result class instance.
-        
+
         - .result = True if data was written to files successfully. Otherwise False.
         - .message will be contain data file path for each file.
-    
+
     :rtype: :class:`.Result`
-    '''
-    
-    revitFileName = util.GetFileNameWithoutExt(revitFilePath)
-    resultValue = res.Result()
+    """
+
+    revit_file_name = fileIO.get_file_name_without_ext(revit_file_path)
+    result_value = res.Result()
     # get values and write them out
     for key, value in PARAM_ACTIONS.items():
-        parameterValue = PARAM_ACTIONS[key].getData(doc)
-        fileName = util.GetFileDateStamp() + revitFileName + PARAM_ACTIONS[key].reportFileName + '.temp'
-        resExport = res.Result()
+        parameter_value = PARAM_ACTIONS[key].get_data(doc)
+        file_name = (
+            dateStamp.get_file_date_stamp()
+            + revit_file_name
+            + PARAM_ACTIONS[key].report_file_name
+            + ".temp"
+        )
+        res_export = res.Result()
         try:
-            util.writeReportData(
-                outputDirectory + '\\' + fileName,
-                '',
+            write_report_data_as_csv(
+                os.path.join(output_directory, file_name),
+                rFns.LOG_FILE_HEADER,
                 [
                     [
-                        revitFileName, 
-                        key, 
-                        util.GetDateStamp(util.FILE_DATE_STAMP_YYYYMMDD_SPACE), 
-                        util.GetDateStamp(util.TIME_STAMP_HHMMSEC_COLON), 
-                        _castParameterValue(parameterValue)
-                        ]
+                        revit_file_name,
+                        key,
+                        dateStamp.get_date_stamp(
+                            dateStamp.FILE_DATE_STAMP_YYYYMMDD_SPACE
+                        ),
+                        dateStamp.get_date_stamp(dateStamp.TIME_STAMP_HHMMSEC_COLON),
+                        _cast_parameter_value(parameter_value),
                     ]
-                )
-                
-            resExport.UpdateSep(True, 'Exported: ' + str(key))
+                ],
+            )
+
+            res_export.update_sep(True, "Exported: {}".format(key))
         except Exception as e:
-                resExport.UpdateSep(True, 'Export failed: ' + str(key)+ ' ' + str(e))
-        resultValue.Update(resExport)
-    return resultValue
+            res_export.update_sep(
+                False, "Export failed: {} with exception: {}".format(key, e)
+            )
+        result_value.update(res_export)
+    return result_value
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitModelHealthReportFileNames.py` & `DuHast-0.0.7/src/duHast/Revit/ModelHealth/Reporting/report_file_names.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Contains file names used by model health report.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -22,73 +22,77 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
+#: header for each report file
+LOG_FILE_HEADER = ["HOSTFILE", "REPORT", "DATE", "TIME", "VALUE"]
+
+
 #: report file name suffix : date last updated
-PARAM_ACTIONS_FILENAME_DATE_LAST_UPDATED = '_DateLastUpdated'
+PARAM_ACTIONS_FILENAME_DATE_LAST_UPDATED = "_DateLastUpdated"
 #: report file name suffix : worksets
-PARAM_ACTIONS_FILENAME_NO_OF_WORKSETS = '_NumberOfWorksets'
+PARAM_ACTIONS_FILENAME_NO_OF_WORKSETS = "_NumberOfWorksets"
 #: report file name suffix : file size
-PARAM_ACTIONS_FILENAME_FILE_SIZE = '_FileSize'
+PARAM_ACTIONS_FILENAME_FILE_SIZE = "_FileSize"
 #: report file name suffix : warnings
-PARAM_ACTIONS_FILENAME_NO_OF_WARNINGS = '_NumberOfWarnings'
+PARAM_ACTIONS_FILENAME_NO_OF_WARNINGS = "_NumberOfWarnings"
 #: report file name suffix : design sets
-PARAM_ACTIONS_FILENAME_NO_OF_DESIGN_SETS = '_NumberOfDesignSets'
+PARAM_ACTIONS_FILENAME_NO_OF_DESIGN_SETS = "_NumberOfDesignSets"
 #: report file name suffix : design options
-PARAM_ACTIONS_FILENAME_NO_OF_DESIGN_OPTIONS ='_NumberOfDesignOptions'
+PARAM_ACTIONS_FILENAME_NO_OF_DESIGN_OPTIONS = "_NumberOfDesignOptions"
 #: report file name suffix : sheet
-PARAM_ACTIONS_FILENAME_NO_OF_SHEETS = '_NumberOfSheets'
+PARAM_ACTIONS_FILENAME_NO_OF_SHEETS = "_NumberOfSheets"
 #: report file name suffix : views
-PARAM_ACTIONS_FILENAME_NO_OF_VIEWS = '_NumberOfViews'
+PARAM_ACTIONS_FILENAME_NO_OF_VIEWS = "_NumberOfViews"
 #: report file name suffix : views not placed
-PARAM_ACTIONS_FILENAME_NO_OF_VIEWS_NOT_PLACED = '_NumberOfViewsNotPlaced'
+PARAM_ACTIONS_FILENAME_NO_OF_VIEWS_NOT_PLACED = "_NumberOfViewsNotPlaced"
 #: report file name suffix : line styles
-PARAM_ACTIONS_FILENAME_NO_OF_LINE_STYLES = '_NumberOfLineStyles'
+PARAM_ACTIONS_FILENAME_NO_OF_LINE_STYLES = "_NumberOfLineStyles"
 #: report file name suffix : line patterns
-PARAM_ACTIONS_FILENAME_NO_OF_LINE_PATTERNS = '_NumberOfLinePatterns'
+PARAM_ACTIONS_FILENAME_NO_OF_LINE_PATTERNS = "_NumberOfLinePatterns"
 #: report file name suffix : fill patterns
-PARAM_ACTIONS_FILENAME_NO_OF_FILL_PATTERNS ='_NumberOfFillPatterns'
+PARAM_ACTIONS_FILENAME_NO_OF_FILL_PATTERNS = "_NumberOfFillPatterns"
 #: report file name suffix : CAD imports
-PARAM_ACTIONS_FILENAME_NO_OF_CAD_IMPORTS ='_NumberOfCadImports'
+PARAM_ACTIONS_FILENAME_NO_OF_CAD_IMPORTS = "_NumberOfCadImports"
 #: report file name suffix : CAD links in model
-PARAM_ACTIONS_FILENAME_NO_OF_CAD_LINKS_MODEL = '_NumberOfCadLinksModel'
+PARAM_ACTIONS_FILENAME_NO_OF_CAD_LINKS_MODEL = "_NumberOfCadLinksModel"
 #: report file name suffix : CAD links in view
-PARAM_ACTIONS_FILENAME_NO_OF_CAD_LINKS_VIEW = '_NumberOfCadLinksView'
+PARAM_ACTIONS_FILENAME_NO_OF_CAD_LINKS_VIEW = "_NumberOfCadLinksView"
 #: report file name suffix : image imports
-PARAM_ACTIONS_FILENAME_NO_OF_IMAGE_IMPORTS = '_NumberOfImageImports'
+PARAM_ACTIONS_FILENAME_NO_OF_IMAGE_IMPORTS = "_NumberOfImageImports"
 #: report file name suffix : image links
-PARAM_ACTIONS_FILENAME_NO_OF_IMAGE_LINKS = '_NumberOfImageLinks'
+PARAM_ACTIONS_FILENAME_NO_OF_IMAGE_LINKS = "_NumberOfImageLinks"
 #: report file name suffix : families in model
-PARAM_ACTIONS_FILENAME_NO_OF_FAMILIES = '_NumberOfFamilies'
+PARAM_ACTIONS_FILENAME_NO_OF_FAMILIES = "_NumberOfFamilies"
 #: report file name suffix : in place families in model
-PARAM_ACTIONS_FILENAME_NO_OF_FAMILIES_IN_PLACE = '_NumberOfInPlaceFamilies'
+PARAM_ACTIONS_FILENAME_NO_OF_FAMILIES_IN_PLACE = "_NumberOfInPlaceFamilies"
 #: report file name suffix : model groups
-PARAM_ACTIONS_FILENAME_NO_OF_MODEL_GROUPS = '_NumberOfModelGroups'
+PARAM_ACTIONS_FILENAME_NO_OF_MODEL_GROUPS = "_NumberOfModelGroups"
 #: report file name suffix : model groups unplaced
-PARAM_ACTIONS_FILENAME_NO_OF_MODEL_GROUPS_UNPLACED = '_NumberOfUnplacedModelGroups'
+PARAM_ACTIONS_FILENAME_NO_OF_MODEL_GROUPS_UNPLACED = "_NumberOfUnplacedModelGroups"
 #: report file name suffix : detail groups
-PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS = '_NumberOfDetailGroups'
+PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS = "_NumberOfDetailGroups"
 #: report file name suffix : detail groups unplaced
-PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS_UNPLACED = '_NumberOfUnplacedDetailGroups'
+PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS_UNPLACED = "_NumberOfUnplacedDetailGroups"
 #: report file name suffix : rooms
-PARAM_ACTIONS_FILENAME_NO_OF_ROOMS = '_NumberOfRooms'
+PARAM_ACTIONS_FILENAME_NO_OF_ROOMS = "_NumberOfRooms"
 #: report file name suffix : unplaced rooms
-PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNPLACED = '_NumberOfUnplacedRooms'
+PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNPLACED = "_NumberOfUnplacedRooms"
 #: report file name suffix : not enclosed rooms
-PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNENCLOSED = '_NumberOfNotEnclosedRooms'
+PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNENCLOSED = "_NumberOfNotEnclosedRooms"
 #: report file name suffix : redundant rooms
-PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_REDUNDANT = '_NumberOfRedundantRooms'
+PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_REDUNDANT = "_NumberOfRedundantRooms"
 #: report file name suffix : filled regions
-PARAM_ACTIONS_FILENAME_NO_OF_FILLED_REGIONS = '_NumberOfRegions'
+PARAM_ACTIONS_FILENAME_NO_OF_FILLED_REGIONS = "_NumberOfRegions"
 
 # combined log file for all reports
-PARAM_ACTIONS_FILENAME_MOTHER = '_AllLogs'
+PARAM_ACTIONS_FILENAME_MOTHER = "_AllLogs"
 
 
 #: list of report file name extensions
 PARAM_ACTIONS_FILENAMES = {
     PARAM_ACTIONS_FILENAME_NO_OF_WORKSETS,
     PARAM_ACTIONS_FILENAME_FILE_SIZE,
     PARAM_ACTIONS_FILENAME_NO_OF_WARNINGS,
@@ -112,9 +116,9 @@
     PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS,
     PARAM_ACTIONS_FILENAME_NO_OF_DETAIL_GROUPS_UNPLACED,
     PARAM_ACTIONS_FILENAME_NO_OF_ROOMS,
     PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNPLACED,
     PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_UNENCLOSED,
     PARAM_ACTIONS_FILENAME_NO_OF_ROOMS_REDUNDANT,
     PARAM_ACTIONS_FILENAME_NO_OF_FILLED_REGIONS,
-    PARAM_ACTIONS_FILENAME_DATE_LAST_UPDATED
+    PARAM_ACTIONS_FILENAME_DATE_LAST_UPDATED,
 }
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitPhases.py` & `DuHast-0.0.7/src/duHast/Revit/Common/phases.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,15 +1,15 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Model phase functions.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -24,46 +24,47 @@
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 
-def GetAllPhases(doc):
-    '''
+def get_all_phases(doc):
+    """
     Returns a dictionary where key is the id and value is the name of the phase.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    
+
     :return: A dictionary where key is the id and value is the name of the phase. Dictionary will be empty if no phases exist (family doc?)
     :rtype: dic{key Autodesk.Revit.DB.ElementId: value str}
-    '''
+    """
 
-    returnValue = {}
+    return_value = {}
     phases = doc.Phases
-    if (phases.Size > 0):
+    if phases.Size > 0:
         for phase in phases:
-            returnValue[phase.Id] = phase.Name
-    return returnValue
+            return_value[phase.Id] = phase.Name
+    return return_value
+
 
-def GetPhaseNameById(doc, phaseId):
-    '''
+def get_phase_name_by_id(doc, phase_id):
+    """
     Returns the name of a phase by Id
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param phaseId: The phase element id.
-    :type phaseId: Autodesk.Revit.DB.ElementId
-    
+    :param phase_id: The phase element id.
+    :type phase_id: Autodesk.Revit.DB.ElementId
+
     :return: Name of the phase, otherwise 'No phase in document' if no phase exists or 'Invalid phase id.' if no phase matching the id was found.
     :rtype: str
-    '''
+    """
 
-    returnValue = 'No phase in document'
-    phases = GetAllPhases(doc)
-    if(len(phases) > 0):
-        if phaseId in phases:
-            returnValue = phases[phaseId]
+    return_value = "No phase in document"
+    phases = get_all_phases(doc)
+    if len(phases) > 0:
+        if phase_id in phases:
+            return_value = phases[phase_id]
         else:
-            returnValue = 'Invalid phase id.'
-    return returnValue
+            return_value = "Invalid phase id."
+    return return_value
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitPurgeAction.py` & `DuHast-0.0.7/src/duHast/Revit/Purge/purge_action.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,62 +1,69 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Purge action storage class for Revit purge unused.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2020  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 
-import System
-import clr
+# import System
+# import clr
 
-class PurgeAction: 
+from duHast.Utilities.Objects import base
+
+
+class PurgeAction(base.Base):
     def __init__(
-        self, 
-        purgeTransactionName, # the function which returns all element ids to be purged
-        purgeIdsGetter, # the function which returns all element ids to be purged
-        purgeReportHeader, # human readable report header for each test action
-        testReportHeader, # human readable report header for each test action
-        testIdsGetter # functions which returns all available type ids in model of same category as purge action. To be used to compare ids before and after coded purge with ids before and after revit built in purge
-    ): 
-        '''
+        self,
+        purgeTransactionName,  # the function which returns all element ids to be purged
+        purgeIdsGetter,  # the function which returns all element ids to be purged
+        purgeReportHeader,  # human readable report header for each test action
+        testReportHeader,  # human readable report header for each test action
+        testIdsGetter,  # functions which returns all available type ids in model of same category as purge action. To be used to compare ids before and after coded purge with ids before and after revit built in purge
+    ):
+        """
         Class constructor.
 
         :param purgeTransactionName: The name of the transaction to purge elements under.
         :type purgeTransactionName: str
         :param purgeIdsGetter: The function which returns all element ids to be purged
         :type purgeIdsGetter: func
         :param purgeReportHeader: Human readable report header for each purge action
         :type purgeReportHeader: str
         :param testReportHeader: Human readable report header for each test action
         :type testReportHeader: str
         :param testIdsGetter: functions which returns all available type ids in model of same category as purge action.\
             To be used to compare ids before and after code purge with ids before and after revit built in purge
         :type testIdsGetter: func
-        '''
+        """
+
+        # forwards all unused arguments
+        # ini super class to allow multi inheritance in children!
+        super(PurgeAction, self).__init__()
 
-        self.purgeTransactionName = purgeTransactionName
-        self.purgeIdsGetter = purgeIdsGetter
-        self.purgeReportHeader = purgeReportHeader
-        self.testReportHeader = testReportHeader
-        self.testIdsGetter = testIdsGetter
+        self.purge_transaction_name = purgeTransactionName
+        self.purge_ids_getter = purgeIdsGetter
+        self.purge_report_header = purgeReportHeader
+        self.test_report_header = testReportHeader
+        self.test_ids_getter = testIdsGetter
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitPurgeUnusedeTransmit.py` & `DuHast-0.0.7/src/duHast/Revit/Purge/purge_unused_e_transmit.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,182 +1,208 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 This module contains a purge unused function using Autodesk's own eTransmit plug in.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Based on the building coder article:
 https://thebuildingcoder.typepad.com/blog/2022/03/purge-unused-and-the-autodesk-camel.html
-'''
+"""
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 
 import clr
 
-import Autodesk.Revit.DB as rdb
+# import Autodesk.Revit.DB as rdb
+
+from duHast.Utilities.Objects import result as res
+from duHast.Utilities.Objects.timer import Timer
 
-from duHast.Utilities import Result as res
-from duHast.Utilities.timer import Timer
 
-def _purge(doc, dllPath):
-    '''
+def _purge(doc, dll_path):
+    """
     Purges the document using the purge unused functionality of the eTransmit tool provided by Autodesk.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param dllPath: Fully qualified file path to the revit version specific eTransmitForRevitDB.dll installed by eTransmit
-    :type dllPath: str
+    :param dll_path: Fully qualified file path to the revit version specific eTransmitForRevitDB.dll installed by eTransmit
+    :type dll_path: str
 
     :return: True purge was successful, otherwise False.
     :rtype: bool
-    '''
-    
-    clr.AddReferenceToFileAndPath(dllPath)
-    # import the eTransmit name space which includes 
+    """
+
+    clr.AddReferenceToFileAndPath(dll_path)
+    # import the eTransmit name space which includes
     # purge unused functionality
     from eTransmitForRevitDB import eTransmitUpgradeOMatic, UpgradeFailureType
+
     # purge the document
-    eTransmitUpgradeOMaticThing = eTransmitUpgradeOMatic(doc.Application)
-    result = eTransmitUpgradeOMaticThing.purgeUnused(doc)
-    return (result == UpgradeFailureType.UpgradeSucceeded)
+    e_transmit_upgrade_o_matic_thing = eTransmitUpgradeOMatic(doc.Application)
+    result = e_transmit_upgrade_o_matic_thing.purgeUnused(doc)
+    return result == UpgradeFailureType.UpgradeSucceeded
+
+
+# -------------------------------------------- Purge Unused using eTransmit for Revit 2019 -------------------------------------
 
-#-------------------------------------------- Purge Unused using eTransmit for Revit 2019 -------------------------------------
 
-def _PurgeUnused2019(doc):
-    '''
+def _purge_unused_2019(doc):
+    """
     Purges the document, revit version 2019, using the purge unused functionality of the eTransmit tool provided by Autodesk
-    
+
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: True purge was successful, otherwise False.
     :rtype: bool
-    '''
+    """
 
     # path to e-Transmit dll for Revit 2019
-    eTransmitFilePath = r'C:\Program Files\Autodesk\eTransmit for Revit 2019\eTransmitForRevitDB.dll'
-    value = _purge(doc, eTransmitFilePath)
+    e_transmit_file_path = (
+        r"C:\Program Files\Autodesk\eTransmit for Revit 2019\eTransmitForRevitDB.dll"
+    )
+    value = _purge(doc, e_transmit_file_path)
     return value
 
-#-------------------------------------------- Purge Unused using eTransmit for Revit 2020 -------------------------------------
 
-def _PurgeUnused2020(doc):
-    '''
+# -------------------------------------------- Purge Unused using eTransmit for Revit 2020 -------------------------------------
+
+
+def _purge_unused_2020(doc):
+    """
     Purges the document, revit version 2020, using the purge unused functionality of the eTransmit tool provided by Autodesk
-    
+
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: True purge was successful, otherwise False.
     :rtype: bool
-    '''
+    """
 
     # path to e-Transmit dll for Revit 2019
-    eTransmitFilePath = r'C:\Program Files\Autodesk\eTransmit for Revit 2020\eTransmitForRevitDB.dll'
-    value = _purge(doc, eTransmitFilePath)
+    e_transmit_file_path = (
+        r"C:\Program Files\Autodesk\eTransmit for Revit 2020\eTransmitForRevitDB.dll"
+    )
+    value = _purge(doc, e_transmit_file_path)
     return value
 
-#-------------------------------------------- Purge Unused using eTransmit for Revit 2021 -------------------------------------
 
-def _PurgeUnused2021(doc):
-    '''
+# -------------------------------------------- Purge Unused using eTransmit for Revit 2021 -------------------------------------
+
+
+def _purge_unused_2021(doc):
+    """
     Purges the document, revit version 2021, using the purge unused functionality of the eTransmit tool provided by Autodesk
-    
+
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: True purge was successful, otherwise False.
     :rtype: bool
-    '''
+    """
 
     # path to e-Transmit dll for Revit 2019
-    eTransmitFilePath = r'C:\Program Files\Autodesk\eTransmit for Revit 2021\eTransmitForRevitDB.dll'
-    value = _purge(doc, eTransmitFilePath)
+    e_transmit_file_path = (
+        r"C:\Program Files\Autodesk\eTransmit for Revit 2021\eTransmitForRevitDB.dll"
+    )
+    value = _purge(doc, e_transmit_file_path)
     return value
 
-#-------------------------------------------- Purge Unused using eTransmit for Revit 2021 -------------------------------------
 
-def _PurgeUnused2022(doc):
-    '''
+# -------------------------------------------- Purge Unused using eTransmit for Revit 2021 -------------------------------------
+
+
+def _purge_unused_2022(doc):
+    """
     Purges the document, revit version 2022, using the purge unused functionality of the eTransmit tool provided by Autodesk
-    
+
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: True purge was successful, otherwise False.
     :rtype: bool
-    '''
+    """
 
     # path to e-Transmit dll for Revit 2019
-    eTransmitFilePath = r'C:\Program Files\Autodesk\eTransmit for Revit 2022\eTransmitForRevitDB.dll'
-    value = _purge(doc, eTransmitFilePath)
+    e_transmit_file_path = (
+        r"C:\Program Files\Autodesk\eTransmit for Revit 2022\eTransmitForRevitDB.dll"
+    )
+    value = _purge(doc, e_transmit_file_path)
     return value
 
-#-------------------------------------------- Purge Unused using eTransmit for Revit 2021 -------------------------------------
 
-def PurgeUnusedETransmit(doc):
-    '''
+# -------------------------------------------- Purge Unused using eTransmit for Revit 2021 -------------------------------------
+
+
+def purge_unused_e_transmit(doc):
+    """
     Purges the document using the purge unused functionality of the eTransmit tool provided by Autodesk.
-    
+
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return:  
+    :return:
         Result class instance.
-        
+
         - Purge status returned in result.status. False if an exception occurred, purge command returned False, unsupported Revit version, otherwise True.
         - result.message will contain the purge status.
-        
+
         On exception:
-        
+
         - result.status (bool) will be False.
         - result.message will contain the exception message.
-    
+
     :rtype: :class:`.Result`
-    '''
+    """
 
-    resultValue = res.Result()
-    tOverall = Timer()
-    tOverall.start()
+    result_value = res.Result()
+    t_overall = Timer()
+    t_overall.start()
     # get the revit version:
-    revitVersion = doc.Application.VersionNumber
+    revit_version = doc.Application.VersionNumber
     try:
-        if (revitVersion == '2019'):
-            resultValue.status = _PurgeUnused2019(doc)
-        elif (revitVersion == '2020'):
-            resultValue.status = _PurgeUnused2020(doc)
-        elif (revitVersion == '2021'):
-            resultValue.status = _PurgeUnused2021(doc)
-        elif (revitVersion == '2022'):
-            resultValue.status = _PurgeUnused2022(doc)
+        if revit_version == "2019":
+            result_value.status = _purge_unused_2019(doc)
+        elif revit_version == "2020":
+            result_value.status = _purge_unused_2020(doc)
+        elif revit_version == "2021":
+            result_value.status = _purge_unused_2021(doc)
+        elif revit_version == "2022":
+            result_value.status = _purge_unused_2022(doc)
         else:
             # this is a non supported revit version!
-            raise ValueError('Revit version ' + revitVersion + ' is currently not supported by purge unused!')
+            raise ValueError(
+                "Revit version: {} is currently not supported by purge unused!".format(
+                    revit_version
+                )
+            )
         # update messaging
-        if( resultValue.status == True):
-            resultValue.message = 'Successfully purged model!'
+        if result_value.status == True:
+            result_value.message = "Successfully purged model!"
         else:
-            resultValue.message = 'Failed to purge model!'
+            result_value.message = "Failed to purge model!"
     except Exception as e:
-            resultValue.UpdateSep(False,'Terminated purge unused actions with exception: '+ str(e))
-    resultValue.AppendMessage('purge duration: '+ str(tOverall.stop()))
-    return resultValue
+        result_value.update_sep(
+            False, "Terminated purge unused actions with exception: {}".format(e)
+        )
+    result_value.append_message("purge duration: {}".format(t_overall.stop()))
+    return result_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitRamps.py` & `DuHast-0.0.7/src/duHast/Revit/DetailItems/detail_items.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,212 +1,190 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-This module contains a number of helper functions relating to Revit ramps.
+This module contains a number of functions around Revit detail items.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2021  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
-import System
 
-from duHast.APISamples import RevitCommonAPI as com
+clr.AddReference("System.Core")
+from System import Linq
 
+clr.ImportExtensions(Linq)
 
+# import common library modules
+from duHast.Revit.Common import parameter_get_utils as rParaGet
+from duHast.Revit.DetailItems.Utility import (
+    detail_items_type_sorting as rDetailItemTypeSort,
+)
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
-# -------------------------------------------- common variables --------------------
-#: header used in reports
-REPORT_RAMPS_HEADER = ['HOSTFILE', 'RAMPTYPEID', 'RAMPTYPENAME']
 
+#: class name Autodesk.Revit.DB.ElementType
+ELEMENT_TYPE = "Autodesk.Revit.DB.ElementType"
+#: class name Autodesk.Revit.DB.FilledRegionType
+FILLED_REGION_TYPE = "Autodesk.Revit.DB.FilledRegionType"
+#: class name Autodesk.Revit.DB.FamilySymbol
+FAMILY_SYMBOL = "Autodesk.Revit.DB.FamilySymbol"
 
-#: Built in ramp family name for ramp
-BASIC_RAMP_FAMILY_NAME = 'Ramp'
-#: List of all built in ramp family names
-BUILTIN_RAMP_TYPE_FAMILY_NAMES = [
-    BASIC_RAMP_FAMILY_NAME,
-]
+#: List of class names which can be detailed components
+DETAIL_COMPONENT_TYPES = [ELEMENT_TYPE, FILLED_REGION_TYPE, FAMILY_SYMBOL]
 
-# --------------------------------------------- utility functions ------------------
+# --------------------------------------------- filled region ------------------
 
-def GetAllRampTypesByCategory(doc):
-    '''
-    Gets a filtered element collector of all Ramp types in the model.
 
-    :param doc: _description_
-    :type doc: _type_
+def get_filled_regions_in_model(doc):
+    """
+    Gets all filled region instances in a model.
 
-    :return: A filtered element collector containing ramp types.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    Filters by class.
 
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Ramps).WhereElementIsElementType()
-    return collector
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+
+    :return: A list containing floor instances.
+    :rtype: list Autodesk.Revit.DB.FilledRegion
+    """
 
-def BuildRampTypeDictionary(collector, dic):
-    '''
-    Returns the dictionary past in with keys and or values added retrieved from collector past in.
+    return rdb.FilteredElementCollector(doc).OfClass(rdb.FilledRegion).ToList()
 
-    TODO: similar function exists in Walls module. Consider more generic function.
 
-    :param collector: A filtered element collector containing ramp type elements of family symbols representing in place families
-    :type collector: Autodesk.Revit.DB.FilteredElementCollector
-    :param dic: dictionary containing key: ramp type family name, value: list of ids
-    :type dic: Dictionary {str:[Autodesk.Revit.DB.ElementId]}
+def get_all_filled_region_type_ids_available(doc):
+    """
+    Gets all filled region types ids in model.
 
-    :return: A dictionary where key is the family name and values are ids of types belonging to that family.
-    :rtype: Dictionary {str:[Autodesk.Revit.DB.ElementId]}
-    '''
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
 
-    for c in collector:
-        if(dic.has_key(c.FamilyName)):
-            if(c.Id not in dic[c.FamilyName]):
-                dic[c.FamilyName].append(c.Id)
-        else:
-            dic[c.FamilyName] = [c.Id]
-    return dic
+    :return: A list of element ids representing filled region types.
+    :rtype: list Autodesk.Revit.DB.ElementIds
+    """
 
-def SortRampTypesByFamilyName(doc):
-    '''
-    Returns a dictionary where key is the family name and values are ids of types belonging to that family.
+    dic = rDetailItemTypeSort.build_detail_type_ids_dictionary(
+        get_all_detail_types_by_category(doc)
+    )
+    if dic.has_key(FILLED_REGION_TYPE):
+        return dic[FILLED_REGION_TYPE]
+    else:
+        return []
 
-    TODO: similar function exists in Walls module. Consider more generic function.
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+"""
+TODO: check for actual class...
+"""
 
-    :return: A dictionary where key is the family name and values are ids of types belonging to that family.
-    :rtype: Dictionary {str:[Autodesk.Revit.DB.ElementId]}
-    '''
+# -------------------------------- detail components -------------------------------------------------------
 
-    # get all ramp types including in place ramp families
-    wts_two = GetAllRampTypesByCategory(doc)
-    usedWts = {}
-    usedWts = BuildRampTypeDictionary(wts_two, usedWts)
-    return usedWts
 
-# -------------------------------- none in place Ramp types -------------------------------------------------------
+def get_all_detail_types_by_category(doc):
+    """
+    Gets all detail component types in the model.
 
-def GetAllRampInstancesInModelByCategory(doc):
-    '''
-    Gets all ramp elements placed in model...ignores in place families (to be confirmed!)
+    Filters by built in category.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: A filtered element collector containing ramp instances.
+    :return: A filtered element collector containing detail component types.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
+
+    collector = (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_DetailComponents)
+        .WhereElementIsElementType()
+    )
+    return collector
 
-    return rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Ramps).WhereElementIsNotElementType()
 
-def GetAllRampTypeIdsInModelByCategory(doc):
-    '''
-    Gets all ramp element type ids available in model.
+# -------------------------------- repeating detail types -------------------------------------------------------
+
+
+def get_all_repeating_detail_type_ids_available(doc):
+    """
+    Get all repeating detail type id's in model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: List of element ids of ramp types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
+    :return: A list of element ids representing repeating detail types.
+    :rtype: list Autodesk.Revit.DB.ElementIds
+    """
 
-    ids = []
-    colCat = GetAllRampTypesByCategory(doc)
-    ids = com.GetIdsFromElementCollector (colCat)
-    return ids
+    dic = rDetailItemTypeSort.build_detail_type_ids_dictionary(
+        get_all_detail_types_by_category(doc)
+    )
+    if dic.has_key(ELEMENT_TYPE):
+        return dic[ELEMENT_TYPE]
+    else:
+        return []
 
-def GetUsedRampTypeIds(doc):
-    '''
-    Gets all used ramp element type ids available in model.
 
-    Used: at least one instance of this type is placed in the model.
+# -------------------------------- Detail families -------------------------------------------------------
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
 
-    :return: List of element ids of ramp types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
+def get_all_detail_symbol_ids_available(doc):
+    """
+    Gets all detail symbol (types) ids in model.
 
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllRampTypeIdsInModelByCategory, 1, 4)
-    return ids
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
 
-def FamilyNoTypesInUse(famTypeIds,unUsedTypeIds):
-    '''
-    Compares two lists of element ids and returns False if any element id in first list is not in the second list.
-    
-    Returns False if any symbols (types) of a family (first lists) are in use in a model (second list).
-    TODO: repetitive code...Consider generic function!
-
-    :param famTypeIds: List of family symbols (types).
-    :type famTypeIds: List of Autodesk.Revit.DB.ElementId
-    :param unUsedTypeIds: List of unused family symbols (types)
-    :type unUsedTypeIds: List of Autodesk.Revit.DB.ElementId
-
-    :return: True if all ids in first list are also in second list, otherwise False.
-    :rtype: bool
-    '''
-
-    match = True
-    for famTypeId in famTypeIds:
-        if (famTypeId not in unUsedTypeIds):
-            match = False
-            break
-    return match
- 
-def GetUnusedNonInPlaceRampTypeIdsToPurge(doc):
-    '''
-    Gets all unused ramp type ids in the model.
-
-    This method can be used to safely delete unused ramp types. In the case that no ramp\
-        instance using any of the types is placed, this will return all but one type id since\
-        Revit requires at least one ramp type definition to be in the model.
-
-    Unused: Not one instance of this type is placed in the model.
-
-    - Ramp
-
-    It will therefore not return any in place family types. (No such thing in Revit?)
+    :return: A list of element ids representing detail symbols.
+    :rtype: list Autodesk.Revit.DB.ElementIds
+    """
+
+    dic = rDetailItemTypeSort.build_detail_type_ids_dictionary(
+        get_all_detail_types_by_category(doc)
+    )
+    if dic.has_key(FAMILY_SYMBOL):
+        return dic[FAMILY_SYMBOL]
+    else:
+        return []
+
+
+def get_detail_symbols_used_in_repeating_details(doc, ids_repeat_det):
+    """
+    Gets the ids of all symbols used in repeating details.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :param idsRepeatDet: List of repeating detail type ids.
+    :type idsRepeatDet: list Autodesk.Revit.DB.ElementIds
 
-    :return: List of element ids of roof types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
-
-    # get unused type ids
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllRampTypeIdsInModelByCategory, 0, 4)
-    # make sure there is at least on Ramp type per system family left in model
-    RampTypes = SortRampTypesByFamilyName(doc)
-    for key, value in RampTypes.items():
-        if(key in BUILTIN_RAMP_TYPE_FAMILY_NAMES):
-            if(FamilyNoTypesInUse(value,ids) == True):
-                # remove one type of this system family from unused list
-                ids.remove(value[0])
-    return ids
+    :return: List of family symbol (type) ids.
+    :rtype: list Autodesk.Revit.DB.ElementIds
+    """
 
-# -------------------------------- In place Ramp types -------------------------------------------------------
-# no such thing in Revit!!
+    ids = []
+    for id_r in ids_repeat_det:
+        repeat_detail = doc.GetElement(id_r)
+        id = rParaGet.get_built_in_parameter_value(
+            repeat_detail, rdb.BuiltInParameter.REPEATING_DETAIL_ELEMENT
+        )
+        if id not in ids and id != rdb.ElementId.InvalidElementId and id != None:
+            ids.append(id)
+    return ids
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitRoofs.py` & `DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameters.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-This module contains a number of helper functions relating to Revit roofs. 
+This module contains a number of helper functions relating to Revit shared parameters.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -25,322 +25,307 @@
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
 import System
 
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import RevitFamilyUtils as rFam
+# import common library modules
+from duHast.Revit.Common.revit_version import get_revit_version_number
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
-# -------------------------------------------- common variables --------------------
-#: header used in reports
-REPORT_ROOFS_HEADER = ['HOSTFILE', 'ROOFTYPEID', 'ROOFTYPENAME']
-
-#: Built in roof family name for basic roof
-BASIC_ROOF_FAMILY_NAME = 'Basic Roof'
-#: Built in roof family name for sloped glazing
-SLOPED_GLAZING_FAMILY_NAME = 'Sloped Glazing'
-#: List of all Built in roof family names
-BUILTIN_ROOF_TYPE_FAMILY_NAMES = [
-    BASIC_ROOF_FAMILY_NAME,
-    SLOPED_GLAZING_FAMILY_NAME
-]
 
 # --------------------------------------------- utility functions ------------------
 
-def GetAllRoofTypesByCategory(doc):
-    '''
-    Gets a filtered element collector of all roof types in the model.
-
-    - Basic Roof
-    - In place families or loaded families
-    - sloped glazing
+
+def get_all_shared_parameters(doc):
+    """
+    Gets all shared parameters in a model
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
-    :return: A filtered element collector containing roof types.
+    :return: A filtered element collector containing shared parameter elements
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
 
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Roofs).WhereElementIsElementType()
+    collector = rdb.FilteredElementCollector(doc).OfClass(rdb.SharedParameterElement)
     return collector
 
-def GetRoofTypesByClass(doc):
-    '''
-    Gets a filtered element collector of all Roof types in the model:
-
-    - Basic Roof
-    - sloped glazing
 
-    Since this is based of class roof it will therefore not return any in place family types!
+def get_family_shared_parameters(doc):
+    """
+    Gets all family parameters which are shared parameters.
 
-    :param doc: Current Revit model document.
+    :param doc: Current Revit family document.
     :type doc: Autodesk.Revit.DB.Document
+    :raises Exception: "Document is not a family document." when a non family document is past in.
 
-    :return: A filtered element collector containing roof types.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-
-    return  rdb.FilteredElementCollector(doc).OfClass(rdb.RoofType)
+    :return: A list of family parameters
+    :rtype: [Autodesk.Revit.DB.FamilyParameter]
+    """
 
-def BuildRoofTypeDictionary(collector, dic):
-    '''
-    Returns the dictionary past in with keys and or values added retrieved from collector past in.
-
-    TODO: similar function exists in Walls module. Consider more generic function.
-
-    :param collector: A filtered element collector containing roof type elements of family symbols
-    :type collector: Autodesk.Revit.DB.FilteredElementCollector
-    :param dic: dictionary containing key: roof type family name, value: list of ids
-    :type dic: Dictionary {str:[Autodesk.Revit.DB.ElementId]}
-
-    :return: A dictionary where key is the family name and values are ids of types belonging to that family.
-    :rtype: Dictionary {str:[Autodesk.Revit.DB.ElementId]}
-    '''
-
-    for c in collector:
-        if(dic.has_key(c.FamilyName)):
-            if(c.Id not in dic[c.FamilyName]):
-                dic[c.FamilyName].append(c.Id)
-        else:
-            dic[c.FamilyName] = [c.Id]
-    return dic
-
-def SortRoofTypesByFamilyName(doc):
-    '''
-    Returns a dictionary where key is the family name and values are ids of types belonging to that family.
+    if doc.IsFamilyDocument:
+        fam_manager = doc.FamilyManager
+        shared_fam_paras = []
+        for fam_para in fam_manager.GetParameters():
+            try:
+                # only shared parameters hav .GUID property...
+                if str(fam_para.GUID) != "":
+                    shared_fam_paras.append(fam_para)
+            except Exception as e:
+                pass
+    else:
+        raise Exception("Document is not a family document.")
+    return shared_fam_paras
 
-    TODO: similar function exists in Walls module. Consider more generic function.
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: A dictionary where key is the family name and values are ids of types belonging to that family.
-    :rtype: Dictionary {str:[Autodesk.Revit.DB.ElementId]}
-    '''
-
-    # get all Roof Type Elements
-    rts = GetRoofTypesByClass(doc)
-    # get all roof types including in place roof families
-    rts_two = GetAllRoofTypesByCategory(doc)
-    usedRts = {}
-    usedRts = BuildRoofTypeDictionary(rts, usedRts)
-    usedRts = BuildRoofTypeDictionary(rts_two, usedRts)
-    return usedRts
-
-# -------------------------------- none in place Roof types -------------------------------------------------------
-
-def GetAllRoofInstancesInModelByCategory(doc):
-    '''
-    Gets all Roof elements placed in model...ignores in place families (to be confirmed!)
+def get_family_parameters(doc):
+    """
+    Gets all family parameters.
 
-    :param doc: Current Revit model document.
+    :param doc: Current Revit family document.
     :type doc: Autodesk.Revit.DB.Document
+    :raises Exception: "Document is not a family document." when a non family document is past in.
 
-    :return: A filtered element collector containing roof instances.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-
-    return rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Roofs).WhereElementIsNotElementType()
+    :return: A list of family parameters
+    :rtype: [Autodesk.Revit.DB.FamilyParameter]
+    """
 
-def GetAllRoofInstancesInModelByClass(doc):
-    '''
-    Gets all Roof elements placed in model...ignores roof soffits(???)
+    if doc.IsFamilyDocument:
+        fam_manager = doc.FamilyManager
+        shared_fam_paras = []
+        for fam_para in fam_manager.GetParameters():
+            shared_fam_paras.append(fam_para)
+    else:
+        raise Exception("Document is not a family document.")
+    return shared_fam_paras
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
 
-    :return: A filtered element collector containing roof instances.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+# ------------------------------------------------------- parameter utilities --------------------------------------------------------------------
 
-    return rdb.FilteredElementCollector(doc).OfClass(rdb.Roof).WhereElementIsNotElementType()
 
-def GetAllRoofTypeIdsInModelByCategory(doc):
-    '''
-    Gets all Roof element type ids available in model.
+def check_whether_shared_parameters_are_in_file(doc, parameter_gui_ds):
+    """
+    Filters the past in list of shared parameter GUIDs by using the shared parameters in the document.
+        Only parameter in both will be returned.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :param parameter_gui_ds: list of shared parameter GUIDs as string values
+    :type parameter_gui_ds: list str
 
-    :return: List of element ids of roof types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = []
-    colCat = GetAllRoofTypesByCategory(doc)
-    ids = com.GetIdsFromElementCollector (colCat)
-    return ids
-
-def GetAllRoofTypeIdsInModelByClass(doc):
-    '''
-    Gets all Roof element type ids available in model.
-
-    :param doc: _description_
-    :type doc: _type_
-
-    :return: List of element ids of roof types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = []
-    colClass = GetRoofTypesByClass(doc)
-    ids = com.GetIdsFromElementCollector(colClass)
-    return ids
-
-def GetUsedRoofTypeIds(doc):
-    '''
-    Gets all used in Roof type ids in the model.
-
-    Used: at least one instance of this type is placed in the model.
+    :return: list of shared parameter GUIDs as string values
+    :rtype: list str
+    """
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+    filtered_gui_ds = []
+    paras = get_all_shared_parameters(doc)
+    for p in paras:
+        if p.GuidValue.ToString() in parameter_gui_ds:
+            filtered_gui_ds.append(p.GuidValue.ToString())
+    return filtered_gui_ds
 
-    :return: List of element ids of roof types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllRoofTypeIdsInModelByCategory, 1)
-    return ids
-
-def FamilyNoTypesInUse(famTypeIds,unUsedTypeIds):
-    '''
-    Compares two lists of element ids and returns False if any element id in first list is not in the second list.
-    
-    Returns False if any symbols (types) of a family (first lists) are in use in a model (second list).
-    
-    TODO: repetitive code...Consider generic function!
-
-    :param famTypeIds: List of family symbols (types).
-    :type famTypeIds: List of Autodesk.Revit.DB.ElementId
-    :param unUsedTypeIds: List of unused family symbols (types)
-    :type unUsedTypeIds: List of Autodesk.Revit.DB.ElementId
 
-    :return: True if all ids in first list are also in second list, otherwise False.
-    :rtype: bool
-    '''
+def check_whether_shared_parameters_by_name_is_family_parameter(doc, parameter_name):
+    """
+    Checks, by name, whether a shared parameter exists as a family parameter in a family.
 
-    match = True
-    for famTypeId in famTypeIds:
-        if (famTypeId not in unUsedTypeIds):
-            match = False
-            break
-    return match
- 
-def GetUnusedNonInPlaceRoofTypeIdsToPurge(doc):
-    '''
-    Gets all unused Roof type ids in the model.
-
-    This method can be used to safely delete unused roof types. In the case that no roof\
-        instance using any of the types is placed, this will return all but one type id since\
-        Revit requires at least one roof type definition to be in the model.
-
-    Unused: Not one instance of this type is placed in the model.
-
-    - Roof Soffit
-    - Compound Roof
-    - Basic Roof
-
-    It will therefore not return any in place family types.
-
-    :param doc: Current Revit model document.
+    param doc: Current Revit family document.
     :type doc: Autodesk.Revit.DB.Document
+    :param parameter_name: The name of the parameter.
+    :type parameter_name: str
 
-    :return: List of element ids of roof types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
-
-    # get unused type ids
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllRoofTypeIdsInModelByClass, 0)
-    # make sure there is at least on Roof type per system family left in model
-    RoofTypes = SortRoofTypesByFamilyName(doc)
-    for key, value in RoofTypes.items():
-        if(key in BUILTIN_ROOF_TYPE_FAMILY_NAMES):
-            if(FamilyNoTypesInUse(value,ids) == True):
-                # remove one type of this system family from unused list
-                ids.remove(value[0])
-    return ids
- 
-# -------------------------------- In place Roof types -------------------------------------------------------
-
-def GetInPlaceRoofFamilyInstances(doc):
-    '''
-    Gets all instances of in place families of category roof in the model.
+    :return: A family parameter if match was found, otherwise None
+    :rtype: Autodesk.Revit.DB.FamilyParameter
+    """
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+    para = None
+    paras = get_family_parameters(doc)
+    for fam_para in paras:
+        if fam_para.Definition.Name == parameter_name:
+            try:
+                # only shared parameters hav .GUID property...
+                if str(fam_para.GUID) != "":
+                    para = fam_para
+                    break
+            except Exception as e:
+                pass
+    return para
 
-    :return: A filtered element collector containing roof family instances.
-    :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
-    
-    filter = rdb.ElementCategoryFilter(rdb.BuiltInCategory.OST_Roofs)
-    return rdb.FilteredElementCollector(doc).OfClass(rdb.FamilyInstance).WherePasses(filter)
-
-def GetAllInPlaceRoofTypeIdsInModel(doc):
-    '''
-    Gets type ids off all available in place families of category roof in the model.
+
+def is_shared_parameter_definition_used(doc, shared_para):
+    """
+    Tests if a shared parameter GUID is used by a family parameter.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
+    :param shared_para: A shared parameter
+    :type shared_para: Autodesk.Revit.DB.SharedParameterElement
 
-    :return: List of element ids of in place roof types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = rFam.GetAllInPlaceTypeIdsInModelOfCategory(doc, rdb.BuiltInCategory.OST_Roofs)
-    return ids
-
-def GetUsedInPlaceRoofTypeIds(doc):
-    '''
-    Gets all used in place roof type ids in the model.
-
-    Used: at least one instance of this type is placed in the model.
+    :return: True is match is found, otherwise False
+    :rtype: bool
+    """
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
+    fam_shared_paras = get_family_shared_parameters(doc)
+    match = False
+    for fam_shared_para in fam_shared_paras:
+        if fam_shared_para.GUID == shared_para.GuidValue:
+            match = True
+            break
+    return match
 
-    :return: List of element ids of in place roof types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllInPlaceRoofTypeIdsInModel, 1)
-    return ids
-
-def GetUnusedInPlaceRoofTypeIds(doc):
-    '''
-    Gets all unused in place roof type ids in the model.
 
-    Unused: Not one instance of this type is placed in the model.
+def get_unused_shared_parameter_definitions(doc):
+    """
+    Returns all unused shard parameter definitions in a family document.
+
+    Note: These shared parameters might be used in any nested family!
+
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+
+    :return: A list of shared parameters
+    :rtype: [Autodesk.Revit.DB.SharedParameterElement]
+    """
+
+    fam_shared_paras = get_family_shared_parameters(doc)
+    shared_paras = get_all_shared_parameters(doc)
+    unused_shared_parameter_definition = []
+    for shared_para in shared_paras:
+        match = False
+        for fam_shared_para in fam_shared_paras:
+            if fam_shared_para.GUID == shared_para.GuidValue:
+                match = True
+                break
+        if match == False:
+            unused_shared_parameter_definition.append(shared_para)
+    return unused_shared_parameter_definition
+
+
+def get_shared_parameter_definition(parameter_name, def_file):
+    """
+    Returns a shared parameter definition from a shared parameter file.
+
+    :param parameter_name: The shared parameter name.
+    :type parameter_name: str
+    :param def_file: The shared parameter file definition.
+    :type def_file: Autodesk.Revit.DB.DefinitionFile
+
+    :return: The shared parameter definition. None if no parameter with a matching name was found.
+    :rtype: Autodesk.Revit.DB.ExternalDefinition
+    """
+
+    parameter_definition = None
+    try:
+        # loop through parameters and try to find matching one
+        # loop through all definition groups
+        for group in def_file.Groups:
+            # loop through para's within definition group
+            for def_para in group.Definitions:
+                # check whether this is the parameter we are after
+                if def_para.Name == parameter_name:
+                    # match and out
+                    parameter_definition = def_para
+                    break
+            if parameter_definition != None:
+                break
+    except Exception as e:
+        pass
+    return parameter_definition
+
+
+# ------------------------------------------------------- parameter reporting --------------------------------------------------------------------
+
+
+def param_binding_exists(doc, param_name, param_type):
+    """
+    Gets all parameter bindings for a given parameter depending on revit version.
+
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param param_name: The name of the parameter.
+    :type param_name: str
+    :param param_type: The parameter type. (Area, vs text vs... (deprecated in Revit 2022!)
+    :type param_type: Autodesk.Revit.DB.ParameterType
+
+    :return: List of categories a parameter is attached to.
+    :rtype: list of str
+    """
+
+    revit_version = get_revit_version_number(doc)
+    data = []
+    if revit_version <= 2022:
+        data = param_binding_exists_2022(
+            doc=doc, param_name=param_name, param_type=param_type
+        )
+    else:
+        data = param_binding_exists_2023(
+            doc=doc, param_name=param_name, type_id=param_type
+        )
+    return data
+
+
+def param_binding_exists_2022(doc, param_name, param_type):
+    """
+    Gets all parameter bindings for a given parameter fro Revit versions up to 2022.
+
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param param_name: The name of the parameter.
+    :type param_name: str
+    :param param_type: The parameter type. (Area, vs text vs... (deprecated in Revit 2022!)
+    :type param_type: Autodesk.Revit.DB.ParameterType
+
+    :return: List of categories a parameter is attached to.
+    :rtype: list of str
+    """
+
+    categories = []
+    map = doc.ParameterBindings
+    iterator = map.ForwardIterator()
+    iterator.Reset()
+    while iterator.MoveNext():
+        if (
+            iterator.Key != None
+            and iterator.Key.Name == param_name
+            and iterator.Key.ParameterType == param_type
+        ):
+            elem_bind = iterator.Current
+            for cat in elem_bind.Categories:
+                categories.append(cat.Name)
+            break
+    return categories
 
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
 
-    :return: List of element ids of in place roof types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = com.GetUsedUnusedTypeIds(doc, GetAllInPlaceRoofTypeIdsInModel, 0)
-    return ids
-
-# doc   current document
-def GetUnusedInPlaceRoofIdsForPurge(doc):
-    '''
-    Gets symbol(type) ids and family ids (when no type is in use of a family) of in place Roof families which can be purged.
-    
-    This method can be used to safely delete unused in place roof types.
+def param_binding_exists_2023(doc, param_name, type_id):
+    """
+    Gets all parameter bindings for a given parameter for Revit 2023 onwards
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids of in place roof types.
-    :rtype: List Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = rFam.GetUnusedInPlaceIdsForPurge(doc, GetUnusedInPlaceRoofTypeIds)
-    return ids
+    :param param_name: The name of the parameter.
+    :type param_name: str
+    :param type_id: Forge type id
+    :type type_id: Autodesk.Revit.DB.ForgeTypeId
+
+    :return: List of categories a parameter is attached to.
+    :rtype: list of str
+    """
+
+    categories = []
+    map = doc.ParameterBindings
+    iterator = map.ForwardIterator()
+    iterator.Reset()
+    while iterator.MoveNext():
+        if (
+            iterator.Key != None
+            and iterator.Key.Name == param_name
+            and iterator.Key.GetDataType() == type_id
+        ):
+            elem_bind = iterator.Current
+            for cat in elem_bind.Categories:
+                categories.append(cat.Name)
+            break
+    return categories
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitSharedParameterData.py` & `DuHast-0.0.7/src/duHast/Revit/SharedParameters/Data/shared_parameter_data.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,54 +1,59 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Family shared parameter data class.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-from duHast.APISamples import IFamilyData as IFamData
-from duHast.Utilities import Utility as util
-from duHast.APISamples import RevitSharedParameters as rSharedPara
+from duHast.Revit.Family.Data import ifamily_data as IFamData
+from duHast.Utilities import utility as util
+from duHast.Revit.SharedParameters import shared_parameters as rSharedPara
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
 
-PARAMETER_GUID = 'parameterGUID' 
-PARAMETER_NAME = 'parameterName' 
-PARAMETER_ID = 'parameterId' 
+PARAMETER_GUID = "parameterGUID"
+PARAMETER_NAME = "parameterName"
+PARAMETER_ID = "parameterId"
+
 
 class SharedParameterData(IFamData.IFamilyData):
-    
-    def __init__(self, rootPath=None, rootCategoryPath=None, dataType=None):
+    def __init__(self, root_path=None, root_category_path=None, data_type=None):
 
-        # todo: check inheritance!!
+        super(SharedParameterData, self).__init__(
+            root_path=root_path,
+            root_category_path=root_category_path,
+            data_type=data_type,
+        )
         # super(CategoryData, self).__init__(rootPath, dataType)
 
+        """
         self.data = []
         
         if(dataType != None):
             self.dataType = dataType
         else:
             self.dataType = 'not declared'
         
@@ -57,62 +62,64 @@
         else:
             self.rootPath = '-'
 
         if(rootCategoryPath != None):
             self.rootCategoryPath = rootCategoryPath
         else:
             self.rootCategoryPath = '-'
-    
+        """
+
     def process(self, doc):
-        collector = rSharedPara.GetAllSharedParameters(doc)
+        collector = rSharedPara.get_all_shared_parameters(doc)
         for para in collector:
             # just in case parameter name is not unicode
-            parameterName = 'unknown'
-            try:   
-                parameterName = util.EncodeAscii(rdb.Element.Name.GetValue(para))
+            parameter_name = "unknown"
+            try:
+                parameter_name = util.encode_ascii(rdb.Element.Name.GetValue(para))
             except Exception as ex:
-                parameterName = 'Exception: ' + str(ex)
+                parameter_name = "Exception: " + str(ex)
             # check if used:
-            useCounter = 0
-            usedByData = {}
-            if(rSharedPara.IsSharedParameterDefinitionUsed(doc, para)):
-                useCounter = 1
+            use_counter = 0
+            used_by_data = {}
+            if rSharedPara.is_shared_parameter_definition_used(doc, para):
+                use_counter = 1
                 # build used by data as required to be the same as post process update
-                usedByData = { 
-                    PARAMETER_GUID : para.GuidValue.ToString(),
-                    PARAMETER_NAME : parameterName,
-                    IFamData.ROOT : self.rootPath
-            }
-            
+                used_by_data = {
+                    PARAMETER_GUID: para.GuidValue.ToString(),
+                    PARAMETER_NAME: parameter_name,
+                    IFamData.ROOT: self.root_path,
+                }
+
             # build data
-            self.data.append({
-                IFamData.ROOT : self.rootPath,
-                IFamData.ROOT_CATEGORY : self.rootCategoryPath,
-                IFamData.FAMILY_NAME : self._stripFileExtension(doc.Title),
-                IFamData.FAMILY_FILE_PATH : doc.PathName,
-                PARAMETER_GUID : para.GuidValue.ToString(),
-                PARAMETER_NAME : parameterName,
-                PARAMETER_ID : para.Id.IntegerValue,
-                IFamData.USAGE_COUNTER : useCounter,
-                IFamData.USED_BY : [usedByData]
+            self.data.append(
+                {
+                    IFamData.ROOT: self.root_path,
+                    IFamData.ROOT_CATEGORY: self.root_category_path,
+                    IFamData.FAMILY_NAME: self._strip_file_extension(doc.Title),
+                    IFamData.FAMILY_FILE_PATH: doc.PathName,
+                    PARAMETER_GUID: para.GuidValue.ToString(),
+                    PARAMETER_NAME: parameter_name,
+                    PARAMETER_ID: para.Id.IntegerValue,
+                    IFamData.USAGE_COUNTER: use_counter,
+                    IFamData.USED_BY: [used_by_data],
                 }
             )
-        
+
         # check if any shared parameter was found
-        if(len(self.data) == 0):
+        if len(self.data) == 0:
             # add message no shared parameter found
-            self.data.append({
-                IFamData.ROOT : self.rootPath,
-                IFamData.ROOT_CATEGORY : self.rootCategoryPath,
-                IFamData.FAMILY_NAME : self._stripFileExtension(doc.Title),
-                IFamData.FAMILY_FILE_PATH : doc.PathName,
-                PARAMETER_GUID : '',
-                PARAMETER_NAME : 'No shared parameter present in family.',
-                PARAMETER_ID : -1,
-                IFamData.USAGE_COUNTER : 0,
-                IFamData.USED_BY : []
+            self.data.append(
+                {
+                    IFamData.ROOT: self.root_path,
+                    IFamData.ROOT_CATEGORY: self.root_category_path,
+                    IFamData.FAMILY_NAME: self._strip_file_extension(doc.Title),
+                    IFamData.FAMILY_FILE_PATH: doc.PathName,
+                    PARAMETER_GUID: "",
+                    PARAMETER_NAME: "No shared parameter present in family.",
+                    PARAMETER_ID: -1,
+                    IFamData.USAGE_COUNTER: 0,
+                    IFamData.USED_BY: [],
                 }
             )
 
-        
-    def get_Data(self):
-        return self.data
+    def get_data(self):
+        return self.data
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitSharedParameterDataPurgeUnused.py` & `DuHast-0.0.7/src/duHast/Revit/SharedParameters/Data/shared_parameter_data_purge_Unused.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,98 +1,121 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Family shared parameters purge unused utilities.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 This will delete all shared parameter definitions which are not used by any family parameter.
 
 - requires a revit shared parameter processor object
 
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 # class used for stats reporting
-from duHast.Utilities import Result as res
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import IFamilyData as IFamData
-from duHast.APISamples import RevitSharedParameterData as rSharedData
-from duHast.APISamples import RevitCategories as rCat
+from duHast.Utilities.Objects import result as res
+from duHast.Revit.Family.Data import ifamily_data as IFamData
+from duHast.Revit.SharedParameters import shared_parameter_data as rSharedParaData
+from duHast.Revit.Categories import categories as rCat
+from duHast.Revit.Common import delete as rDel
 
 import Autodesk.Revit.DB as rdb
 
-def PurgeUnused(doc, processor):
-    '''
+
+def purge_unused(doc, processor):
+    """
     This will delete all shared parameter definitions which are not used by any family parameter in the family or nested families.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :param processor: An RevitSharedParameterDataProcessor object containing all shared parameter information of the family document and any nested families.
     :type processor: :class:`.SharedParameterProcessor`
 
-    :return: 
+    :return:
         Result class instance.
 
         - True if all unused shared parameters where deleted successfully or none needed to be deleted. Otherwise False.
-        - Result.message property updated in format: Found unused shared parameter: shared parameter Name [GUID] 
-        
+        - Result.message property updated in format: Found unused shared parameter: shared parameter Name [GUID]
+
         On exception:
-        
+
         - status (bool) will be False.
         - message will contain the exception message.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     # from processor instance get all root line pattern entries where usage counter == 0.
     # delete those line patterns by id
 
-    returnValue = res.Result()
+    return_value = res.Result()
 
     # check the category of the family first:
     # Tags and generic annotations (may) contain labels which in turn use shared parameters to drive them
     # there is currently no way in the api (Revit 2022) to find out what parameter is driving the label...
 
     # get the family category name:
-    famCatName = list(rCat.GetFamilyCategory(doc))[0]
-    if(famCatName != 'Generic Annotations' and famCatName.endswith( 'Tags') == False):
-        idsToDelete = []
+    fam_cat_name = list(rCat.get_family_category(doc))[0]
+    if fam_cat_name != "Generic Annotations" and fam_cat_name.endswith("Tags") == False:
+        ids_to_delete = []
         # get categories found in root processor data only
-        rootFamData = processor._findRootFamilyData()
+        root_fam_data = processor._findRootFamilyData()
         # get all root line pattern entries where usage counter == 0.
-        for rootFam in rootFamData:
-            if (rootFam[IFamData.USAGE_COUNTER] == 0 ):
-                returnValue.AppendMessage('Found unused shared parameter: ' + rootFam[rSharedParaData.PARAMETER_NAME] + ' [' +str(rootFam[rSharedParaData.PARAMETER_GUID])+']')
-                idsToDelete.append(rdb.ElementId(rootFam[rSharedParaData.PARAMETER_ID]))
+        for root_fam in root_fam_data:
+            if root_fam[IFamData.USAGE_COUNTER] == 0:
+                return_value.append_message(
+                    "Found unused shared parameter: {} [{}]".format(
+                        root_fam[rSharedParaData.PARAMETER_NAME],
+                        root_fam[rSharedParaData.PARAMETER_GUID],
+                    )
+                )
+                ids_to_delete.append(
+                    rdb.ElementId(root_fam[rSharedParaData.PARAMETER_ID])
+                )
         # delete any subcategories found
-        if(len(idsToDelete) > 0):
-            resultDelete = com.DeleteByElementIds(doc, idsToDelete, 'Deleting unused shared parameters.', 'Shared Parameters')
-            returnValue.Update(resultDelete)
+        if len(ids_to_delete) > 0:
+            result_delete = rDel.delete_by_element_ids(
+                doc,
+                ids_to_delete,
+                "Deleting unused shared parameters.",
+                "Shared Parameters",
+            )
+            return_value.update(result_delete)
             # may need to delete shared parameters one by one if one or more cant be deleted
-            if (resultDelete.status == False):
-                resultDeleteOneByOne = com.DeleteByElementIdsOneByOne(doc, idsToDelete, 'Deleting unused shared parameters: one by one.', 'Shared Parameters')
-                returnValue.Update(resultDeleteOneByOne)
+            if result_delete.status == False:
+                result_delete_one_by_one = rDel.delete_by_element_ids_one_by_one(
+                    doc,
+                    ids_to_delete,
+                    "Deleting unused shared parameters: one by one.",
+                    "Shared Parameters",
+                )
+                return_value.update(result_delete_one_by_one)
         else:
-            returnValue.UpdateSep(True, 'No unused shared parameters found. Nothing was deleted.')
+            return_value.update_sep(
+                True, "No unused shared parameters found. Nothing was deleted."
+            )
     else:
-        returnValue.UpdateSep(True, 'This is an annotation family (tag or generic annotation). Due to limitations in the Revit API no shared parameter was purged.')
-    return returnValue
+        return_value.update_sep(
+            True,
+            "This is an annotation family (tag or generic annotation). Due to limitations in the Revit API no shared parameter was purged.",
+        )
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitSharedParameterSwap.py` & `DuHast-0.0.7/src/duHast/Revit/SharedParameters/shared_parameter_swap.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 This module contains a function to swap out one shard parameter for another.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 The swap is done by:
 - changing current shared parameter to a family parameter (dummy)
 - deleting the old shared parameter definition
@@ -15,18 +15,18 @@
 - header row: yes
 - column 1: current shared parameter name
 - column 2: new shared parameter name
 - column 3: fully qualified file path of shared parameter file
 - column 4: Is parameter instance (True / False)
 - column 5: parameter grouping name ( refer to module: RevitParameterGrouping)
 
-'''
+"""
 
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -44,114 +44,157 @@
 #
 #
 
 import clr
 import System
 
 # import common library modules
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.Utilities import Result as res
-from duHast.Utilities import Utility as util
-from duHast.APISamples import RevitSharedParameterAdd as rSharedPAdd
-from duHast.APISamples import RevitSharedParametersTuple as rSharedT
-from duHast.APISamples import RevitParameterGrouping as rPG
-from duHast.APISamples import RevitSharedParameters as rSharedPara
+# from duHast.APISamples.Common import RevitCommonAPI as com
+from duHast.Utilities.Objects import result as res
+from duHast.Utilities import files_csv as fileCSV
+from duHast.Revit.SharedParameters import shared_parameter_add as rSharedPAdd
+from duHast.Revit.SharedParameters import shared_parameters_tuple as rSharedT
+from duHast.Revit.Common import parameter_grouping as rPG
+from duHast.Revit.SharedParameters import shared_parameters as rSharedPara
+from duHast.Revit.SharedParameters import shared_parameters_delete as rSharedParaDelete
+from duHast.Revit.SharedParameters import (
+    shared_parameter_type_change as rSharedTypeChange,
+)
 
 from collections import namedtuple
 
-'''
+
+"""
 Tuple containing settings data on how to swap a shared parameter retrieved from a file.
-'''
+"""
+
+PARAMETER_SETTINGS_DATA = namedtuple(
+    "parameterSettingsData", "oldParameterName newParameterData sharedParameterPath"
+)
 
-parameterSettingsData = namedtuple('parameterSettingsData', 'oldParameterName newParameterData sharedParameterPath')
 
-def _loadSharedParameterDataFromFile(filePath):
-    '''
+def _load_shared_parameter_data_from_file(file_path):
+    """
     _summary_
 
-    :param filePath: Fully qualified file path to shared parameter change directive file.
-    :type filePath: str
+    :param file_path: Fully qualified file path to shared parameter change directive file.
+    :type file_path: str
 
     :return: A dictionary in format; key: current parameter name, value: named tuple of type parameterSettingsData
     :rtype: {str:named tuple}
-    '''
+    """
 
-    parameterMapper = {}
-    fileData = util.ReadCSVfile(filePath)
-    for i in range (1, len(fileData)):
-        row = fileData[i]
-        if(len(row) == 5):
+    parameter_mapper = {}
+    file_data = fileCSV.read_csv_file(file_path)
+    for i in range(1, len(file_data)):
+        row = file_data[i]
+        if len(row) == 5:
             flag = False
-            if(row[3].upper() == "TRUE"):
+            if row[3].upper() == "TRUE":
                 flag = True
-            t = rSharedT.parameterData (row[1], flag, rPG.ParameterGroupingToBuiltInParameterGroups[row[4]])
-            parameterMapper[row[0]] = parameterSettingsData(row[0], t, row[2])
-    return parameterMapper
+            t = rSharedT.PARAMETER_DATA(
+                row[1], flag, rPG.PRAMETER_GROPUING_TO_BUILD_IN_PARAMETER_GROUPS[row[4]]
+            )
+            parameter_mapper[row[0]] = PARAMETER_SETTINGS_DATA(row[0], t, row[2])
+    return parameter_mapper
 
-def SwapSharedParameters(doc, changeDirectiveFilePath):
-    '''
+
+def swap_shared_parameters(doc, change_directive_file_path):
+    """
     Swaps out a shared parameter for another. (refer to module header for details)
 
     :param doc: Current Revit family document.
     :type doc: Autodesk.Revit.DB.Document
-    :param changeDirectiveFilePath: Fully qualified file path to shared parameter change directive.
-    :type changeDirectiveFilePath: str
+    :param change_directive_file_path: Fully qualified file path to shared parameter change directive.
+    :type change_directive_file_path: str
 
-    :return: 
+    :return:
         Result class instance.
 
         - False if an exception occurred, otherwise True.
         - result.message will contain the names of the changed shared parameter(s).
         - result status will contain lists of new shared parameters
-        
+
         On exception (handled by optimizer itself!):
-        
+
         - result.status (bool) will be False.
         - result.message will contain exception message.
-    
+
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
-    _parameterPrefix_ = "_dummy_"
+    return_value = res.Result()
+    _parameter_prefix_ = "_dummy_"
     # load change directive
-    parameterDirectives = _loadSharedParameterDataFromFile(changeDirectiveFilePath)
-    if(len(parameterDirectives) > 0):
+    parameter_directives = _load_shared_parameter_data_from_file(
+        change_directive_file_path
+    )
+    if len(parameter_directives) > 0:
         # loop over directive and
-        for pDirective in parameterDirectives:
+        for p_directive in parameter_directives:
             # load shared para file
-            sharedParaDefFile = rSharedPAdd.LoadSharedParameterFile(doc, parameterDirectives[pDirective].sharedParameterPath)
-            returnValue.AppendMessage('Read shared parameter file: ' + parameterDirectives[pDirective].sharedParameterPath)
-            if(sharedParaDefFile != None):
+            shared_para_def_file = rSharedPAdd.load_shared_parameter_file(
+                doc, parameter_directives[p_directive].sharedParameterPath
+            )
+            return_value.append_message(
+                "Read shared parameter file: {}".format(
+                    parameter_directives[p_directive].sharedParameterPath
+                )
+            )
+            if shared_para_def_file != None:
                 #   - swap shared parameter to family parameter
-                statusChangeToFamPara = rSharedPara.ChangeSharedParameterToFamilyParameter(doc, pDirective, _parameterPrefix_)
-                returnValue.Update(statusChangeToFamPara)
-                if(statusChangeToFamPara.status):
+                status_change_to_fam_para = (
+                    rSharedTypeChange.change_shared_parameter_to_family_parameter(
+                        doc, p_directive, _parameter_prefix_
+                    )
+                )
+                return_value.update(status_change_to_fam_para)
+                if status_change_to_fam_para.status:
                     #   - delete all shared parameter definition
-                    statusDeleteOldSharedParaDef = rSharedPara.DeleteSharedParameterByName(doc, pDirective)
-                    returnValue.Update(statusDeleteOldSharedParaDef)
-                    if(statusDeleteOldSharedParaDef.status):
+                    status_delete_old_shared_para_def = (
+                        rSharedParaDelete.delete_shared_parameter_by_name(
+                            doc, p_directive
+                        )
+                    )
+                    return_value.update(status_delete_old_shared_para_def)
+                    if status_delete_old_shared_para_def.status:
                         # get shared parameter definition
-                        sParaDef = rSharedPara.GetSharedParameterDefinition(parameterDirectives[pDirective].newParameterData.name, sharedParaDefFile)
+                        s_para_def = rSharedPara.get_shared_parameter_definition(
+                            parameter_directives[p_directive].newParameterData.name,
+                            shared_para_def_file,
+                        )
                         #   - add new shared parameter
-                        if(sParaDef != None):
-                            returnValue.AppendMessage('Retrieved shared parameter definition for: ' + parameterDirectives[pDirective].newParameterData.name) 
-                            #   - swap family parameter to shared parameter
-                            statusSwapFamToSharedP = rSharedPara.ChangeFamilyParameterToSharedParameter(
-                                doc, 
-                                _parameterPrefix_ + pDirective, # add prefix
-                                parameterDirectives[pDirective].newParameterData, 
-                                sParaDef
+                        if s_para_def != None:
+                            return_value.append_message(
+                                "Retrieved shared parameter definition for: {}".format(
+                                    parameter_directives[
+                                        p_directive
+                                    ].newParameterData.name
                                 )
-                            returnValue.Update(statusSwapFamToSharedP)
+                            )
+                            #   - swap family parameter to shared parameter
+                            status_swap_fam_to_shared_p = rSharedTypeChange.change_family_parameter_to_shared_parameter(
+                                doc,
+                                _parameter_prefix_ + p_directive,  # add prefix
+                                parameter_directives[p_directive].newParameterData,
+                                s_para_def,
+                            )
+                            return_value.update(status_swap_fam_to_shared_p)
                         else:
-                            returnValue.UpdateSep(False, 'Failed to get shared parameter definition from file.')
+                            return_value.update_sep(
+                                False,
+                                "Failed to get shared parameter definition from file.",
+                            )
                     else:
-                        returnValue.Update(statusDeleteOldSharedParaDef)
+                        return_value.update(status_delete_old_shared_para_def)
                 else:
-                    returnValue.Update(statusChangeToFamPara)
+                    return_value.update(status_change_to_fam_para)
             else:
-                returnValue.UpdateSep(False, 'Failed to load shared parameter def file from: ' + parameterDirectives[pDirective].sharedParameterPath)
+                return_value.update_sep(
+                    False,
+                    "Failed to load shared parameter def file from: "
+                    + parameter_directives[p_directive].sharedParameterPath,
+                )
     else:
-        returnValue.status = False
-        returnValue.message = 'No change directives in file.'
-    return returnValue
+        return_value.status = False
+        return_value.message = "No change directives in file."
+    return return_value
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitSharedParametersTuple.py` & `DuHast-0.0.7/src/duHast/Revit/Annotation/Reporting/gen_annotations_report_header.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-This module contains a tuple used to store settings retrieved from a file.
+This module contains the header row for any (future) generic annotation reports. 
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -22,12 +22,14 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-from collections import namedtuple
-
-
-# tuples containing base family data read from file
-parameterData = namedtuple('parameterData', 'name isInstance builtInParameterGroup')
+# -------------------------------------------- common variables --------------------
+#: header used in reports
+REPORT_GENERIC_ANNOTATIONS_HEADER = [
+    "HOSTFILE",
+    "GENERICANNOTATIONTYPEID",
+    "GENERICANNOTATIONTYPENAME",
+]
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitViewReferencing.py` & `DuHast-0.0.7/src/duHast/Revit/Views/referencing.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 This module contains a number of helper functions relating to Revit view referencing. 
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -23,499 +23,431 @@
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
+
 clr.AddReference("System.Core")
 from System import Linq
+
 clr.ImportExtensions(Linq)
 import System
 from System.Collections.Generic import List
 
-from duHast.APISamples import RevitCommonAPI as com
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.APISamples import RevitFamilyUtils as rFamU
-from duHast.APISamples import RevitViews as rView
+from duHast.Revit.Common import common as com
+from duHast.Revit.Common import parameter_get_utils as rParaGet
+from duHast.Revit.Family import family_utils as rFamUPurge
+from duHast.Revit.Views import views as rView
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
 # ------------------------ deprecated -----------------------
 # the following element collectors dont seem to return any types ...
 
 # doc:   current model document
-def Deprecated_GetAllCallOutTypesByCategory(doc):
-    ''' this will return an EMPTY filtered element collector of all call out types in the model in Revit 2019'''
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_Callouts).WhereElementIsElementType()
+def deprecated__get_all_call_out_types_by_category(doc):
+    """this will return an EMPTY filtered element collector of all call out types in the model in Revit 2019"""
+    collector = (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_Callouts)
+        .WhereElementIsElementType()
+    )
     return collector
 
+
 # doc:   current model document
-def Deprecated_GetAllReferenceViewTypesByCategory(doc):
-    '''this will return an EMPTY filtered element collector of all reference view types in the model in Revit 2019'''
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_ReferenceViewer).WhereElementIsElementType()
+def deprecated__get_all_reference_view_types_by_category(doc):
+    """this will return an EMPTY filtered element collector of all reference view types in the model in Revit 2019"""
+    collector = (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_ReferenceViewer)
+        .WhereElementIsElementType()
+    )
     return collector
- 
+
+
 # doc:   current model document
-def Deprecated_GetAllCallOutTypeIdsByCategory(doc):
-    ''' this will return an EMPTY filtered element collector of all call out type ids in the model'''
-    collector = Deprecated_GetAllCallOutTypesByCategory(doc)
-    ids = com.GetIdsFromElementCollector(collector)
+def deprecated__get_all_call_out_type_ids_by_category(doc):
+    """this will return an EMPTY filtered element collector of all call out type ids in the model"""
+    collector = deprecated__get_all_call_out_types_by_category(doc)
+    ids = com.get_ids_from_element_collector(collector)
     return ids
 
+
 # doc:   current model document
-def Deprecated_GetAllReferenceViewTypeIdsByCategory(doc):
-    ''' this will return an EMPTY filtered element collector of all reference view types in the model'''
-    collector = Deprecated_GetAllReferenceViewTypesByCategory(doc)
-    ids = com.GetIdsFromElementCollector(collector)
+def deprecated__get_all_reference_view_type_ids_by_category(doc):
+    """this will return an EMPTY filtered element collector of all reference view types in the model"""
+    collector = deprecated__get_all_reference_view_types_by_category(doc)
+    ids = com.get_ids_from_element_collector(collector)
     return ids
 
+
 # ---------------------- utility -----------------------
 
-def GetAllCallOutHeadsByCategory(doc):
-    '''
+
+def get_all_call_out_heads_by_category(doc):
+    """
     Gets a filtered element collector of all callOut Head symbol (types) in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: A filtered element collector containing call out head symbols.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
 
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_CalloutHeads).WhereElementIsElementType()
+    collector = (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_CalloutHeads)
+        .WhereElementIsElementType()
+    )
     return collector
 
-def GetAllElevationHeadsByCategory(doc):
-    '''
+
+def get_all_elevation_heads_by_category(doc):
+    """
     Gets a filtered element collector of all elevation symbols (types) in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: A filtered element collector containing elevation symbols.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
 
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_ElevationMarks).WhereElementIsElementType()
+    collector = (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_ElevationMarks)
+        .WhereElementIsElementType()
+    )
     return collector
 
-def GetAllSectionHeadsByCategory(doc):
-    '''
+
+def get_all_section_heads_by_category(doc):
+    """
     Gets a filtered element collector of all section symbols (types) in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :return: A filtered element collector containing section symbols.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
 
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_SectionHeads).WhereElementIsElementType()
+    collector = (
+        rdb.FilteredElementCollector(doc)
+        .OfCategory(rdb.BuiltInCategory.OST_SectionHeads)
+        .WhereElementIsElementType()
+    )
     return collector
 
-def GetAllViewContinuationMarkersByCategory(doc):
-    '''
+
+def get_all_view_continuation_markers_by_category(doc):
+    """
     Gets a filtered element collector of all view continuation symbols (types) in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: A filtered element collector containing Continuation Marker symbols.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
 
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_ReferenceViewerSymbol)
+    collector = rdb.FilteredElementCollector(doc).OfCategory(
+        rdb.BuiltInCategory.OST_ReferenceViewerSymbol
+    )
     return collector
 
-def GetAllReferenceViewElementsByCategory(doc):
-    '''
+
+def get_all_reference_view_elements_by_category(doc):
+    """
     Gets filtered element collector of all reference view elements in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: A filtered element collector containing reference view elements.
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
 
-    collector = rdb.FilteredElementCollector(doc).OfCategory(rdb.BuiltInCategory.OST_ReferenceViewer)
+    collector = rdb.FilteredElementCollector(doc).OfCategory(
+        rdb.BuiltInCategory.OST_ReferenceViewer
+    )
     return collector
 
+
 # ---------------------- view ref types  -----------------------
 
 #: contains the builtin parameter definitions for Call out type ids, section type ids, elevation type ids
 VIEW_REFERENCE_PARAMETER_DEF_NAMES = [
     rdb.BuiltInParameter.ELEVATN_TAG,
     rdb.BuiltInParameter.CALLOUT_TAG,
-    rdb.BuiltInParameter.SECTION_TAG
+    rdb.BuiltInParameter.SECTION_TAG,
 ]
 
 #: contains the builtin parameter definitions for call out symbol tag ids, section symbol tag ids, elevation symbol tag ids
 VIEW_TAG_SYMBOL_PARAMETER_DEF = [
     rdb.BuiltInParameter.CALLOUT_ATTR_HEAD_TAG,
     rdb.BuiltInParameter.ELEV_SYMBOL_ID,
     rdb.BuiltInParameter.SECTION_ATTR_HEAD_TAG,
     rdb.BuiltInParameter.SECTION_ATTR_TAIL_TAG,
-    rdb.BuiltInParameter.REFERENCE_VIEWER_ATTR_TAG
+    rdb.BuiltInParameter.REFERENCE_VIEWER_ATTR_TAG,
 ]
 
 #: category filter for all view ref categories
-VIEW_REF_CATEGORY_FILTER = List[rdb.BuiltInCategory] ([
+VIEW_REF_CATEGORY_FILTER = List[rdb.BuiltInCategory](
+    [
         rdb.BuiltInCategory.OST_CalloutHeads,
         rdb.BuiltInCategory.OST_ElevationMarks,
         rdb.BuiltInCategory.OST_SectionHeads,
-        rdb.BuiltInCategory.OST_ReferenceViewerSymbol
-    ])
+        rdb.BuiltInCategory.OST_ReferenceViewerSymbol,
+    ]
+)
 
-def GetReferenceTypeIdsFromViewType(viewType):
-    '''
+
+def get_reference_type_ids_from_view_type(view_type):
+    """
     Gets all reference type ids used in view type.
 
-    :param viewType: The view type.
-    :type viewType: Autodesk.Revit.DB.ViewType
+    :param view_type: The view type.
+    :type view_type: Autodesk.Revit.DB.ViewType
 
     :return: dictionary, key: BuiltinParameterDefinition, value: id of a tag
     :rtype: dic{Autodesk.Revit.DB.BuiltinParameterDefinition:[Autodesk.Revit.DB.ElementId]}
-    '''
+    """
 
     dic = {}
-    for pDef in VIEW_REFERENCE_PARAMETER_DEF_NAMES:
-        pValue = rParaGet.get_built_in_parameter_value(viewType, pDef)
-        if(pValue != None):
+    for p_def in VIEW_REFERENCE_PARAMETER_DEF_NAMES:
+        p_value = rParaGet.get_built_in_parameter_value(view_type, p_def)
+        if p_value != None:
             # there should only ever be one value per key!
-            if(dic.has_key(pDef)):
-                dic[pDef].append(pValue)
+            if dic.has_key(p_def):
+                dic[p_def].append(p_value)
             else:
-                dic[pDef] = [pValue]
+                dic[p_def] = [p_value]
     return dic
 
-def GetUsedViewReferenceTypeIdData(doc):
-    '''
+
+def get_used_view_reference_type_id_data(doc):
+    """
     Gets all view references types in use in the model in a dictionary.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: key is the reference tag type: call out, section or elevation, values are the type ids in use
     :rtype: dictionary {reference tag type: list Autodesk.Revit.DB.ElementIds}
-    '''
+    """
 
     dic = {}
-    col = rView.GetViewTypes(doc)
+    col = rView.get_view_types(doc)
     for c in col:
         # get reference types from view types
-        referenceTypeByViewType = GetReferenceTypeIdsFromViewType(c)
+        reference_type_by_view_type = get_reference_type_ids_from_view_type(c)
         # check if already in dictionary , if not append
-        for key, value in referenceTypeByViewType.items():
-            if(dic.has_key(key)):
+        for key, value in reference_type_by_view_type.items():
+            if dic.has_key(key):
                 for v in value:
-                    if(v not in dic[key]):
+                    if v not in dic[key]:
                         dic[key].append(v)
             else:
-              dic[key] = value
+                dic[key] = value
     return dic
 
-def GetAllViewReferenceTypeIdData(doc):
-    '''
+
+def get_all_view_reference_type_id_data(doc):
+    """
     Gets all view references types available in the model in a dictionary.
-    
+
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: key is the reference type: call out, section or elevation, values are the type ids in use
     :rtype: dictionary {reference tag type: list Autodesk.Revit.DB.ElementIds}
-    '''
+    """
 
     dic = {}
-    col = rView.GetViewTypes(doc)
+    col = rView.get_view_types(doc)
     for c in col:
         # get reference types from view types
-        referenceTypeByViewType = GetReferenceTypeIdsFromViewType(c)
+        reference_type_by_view_type = get_reference_type_ids_from_view_type(c)
         # get all similar types
-        for key, value in referenceTypeByViewType.items():
-            for v in referenceTypeByViewType[key]:
+        for key, value in reference_type_by_view_type.items():
+            for v in reference_type_by_view_type[key]:
                 type = doc.GetElement(v)
-                if(type !=None):
-                    allSimTypeIds = type.GetSimilarTypes()
-                    for simTypeId in allSimTypeIds:
-                        if(dic.has_key(key)):
-                            if(simTypeId not in dic[key]):
-                                dic[key].append(simTypeId)
+                if type != None:
+                    all_sim_type_ids = type.GetSimilarTypes()
+                    for sim_type_id in all_sim_type_ids:
+                        if dic.has_key(key):
+                            if sim_type_id not in dic[key]:
+                                dic[key].append(sim_type_id)
                         else:
-                            dic[key] = [simTypeId]
+                            dic[key] = [sim_type_id]
     return dic
 
-def GetAllViewReferenceTypeIdDataAsList(doc):
-    '''
+
+def get_all_view_reference_type_id_data_as_list(doc):
+    """
     Gets all view references type ids available in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: A list of element ids representing view reference types
     :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
+    """
 
-    dic = GetAllViewReferenceTypeIdData(doc)
+    dic = get_all_view_reference_type_id_data(doc)
     ids = []
     for key, value in dic.items():
-        if(len(dic[key]) > 0):
+        if len(dic[key]) > 0:
             ids = ids + dic[key]
     return ids
 
-def GetAllViewContinuationTypeIds(doc):
-    '''
+
+def get_all_view_continuation_type_ids(doc):
+    """
     Gets all view continuation type ids available in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: List of view continuation type ids.
     :rtype: list Autodesk.Revit.DB.ElementIds
-    '''
+    """
 
     ids = []
-    syms = GetAllReferenceViewElementsByCategory(doc)
+    syms = get_all_reference_view_elements_by_category(doc)
     for sym in syms:
-        simTypeIds = sym.GetValidTypes()
-        for simType in simTypeIds:
-            if (simType not in ids):
-                ids.append (simType)
+        sim_type_ids = sym.GetValidTypes()
+        for sim_type in sim_type_ids:
+            if sim_type not in ids:
+                ids.append(sim_type)
     return ids
 
-def GetUsedViewContinuationTypeIds(doc):
-    '''returns all view continuation types available in the model'''
+
+def get_used_view_continuation_type_ids(doc):
+    """returns all view continuation types available in the model"""
+
     ids = []
-    syms = GetAllReferenceViewElementsByCategory(doc)
+    syms = get_all_reference_view_elements_by_category(doc)
     for sym in syms:
-        if (sym.GetTypeId() not in ids):
-                ids.append (sym.GetTypeId())
+        if sym.GetTypeId() not in ids:
+            ids.append(sym.GetTypeId())
     return ids
 
-def GetAllViewReferenceSymbolIds(doc):
-    '''
+
+def get_all_view_reference_symbol_ids(doc):
+    """
     Gets the ids of all view reference family symbols(types) in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: List of view reference family symbols(types) ids.
     :rtype:  list Autodesk.Revit.DB.ElementIds
-    '''
+    """
 
     ids = []
-    multiCatFilter = rdb.ElementMulticategoryFilter(VIEW_REF_CATEGORY_FILTER)
-    collector = rdb.FilteredElementCollector(doc).WherePasses(multiCatFilter).WhereElementIsElementType()
-    ids = com.GetIdsFromElementCollector(collector)
+    multi_cat_filter = rdb.ElementMulticategoryFilter(VIEW_REF_CATEGORY_FILTER)
+    collector = (
+        rdb.FilteredElementCollector(doc)
+        .WherePasses(multi_cat_filter)
+        .WhereElementIsElementType()
+    )
+    ids = com.get_ids_from_element_collector(collector)
     return ids
 
+
 # ---------------------- view refs and continuation symbols -----------------------
 
-def GetSymbolIdsFromTypeIds(doc, viewRefTypesIds):
-    '''
+
+def get_symbol_ids_from_type_ids(doc, view_ref_types_ids):
+    """
     'Gets the ids of all view family symbols(types) from given view ref types or continuation types the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param viewRefTypesIds: list of ids representing view reference types or continuation types
-    :type viewRefTypesIds: list Autodesk.Revit.DB.ElementId
+    :param view_ref_types_ids: list of ids representing view reference types or continuation types
+    :type view_ref_types_ids: list Autodesk.Revit.DB.ElementId
 
     :return: List of ids of all view family symbols(types).
     :rtype: list Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     ids = []
-    for vrtId in viewRefTypesIds:
-        el = doc.GetElement(vrtId)
-        for pDef in VIEW_TAG_SYMBOL_PARAMETER_DEF:
-            pValue = rParaGet.get_built_in_parameter_value(el, pDef)
-            if (pValue != None and pValue not in ids):
-                ids.append(pValue)
+    for vrt_id in view_ref_types_ids:
+        el = doc.GetElement(vrt_id)
+        for p_def in VIEW_TAG_SYMBOL_PARAMETER_DEF:
+            p_value = rParaGet.get_built_in_parameter_value(el, p_def)
+            if p_value != None and p_value not in ids:
+                ids.append(p_value)
     return ids
 
-def GetUsedViewReferenceAndContinuationMarkerSymbolIds(doc):
-    '''
-    Get the ids of all view reference symbols(types) and view continuations symbols (types) used by 
+
+def get_used_view_reference_and_continuation_marker_symbol_ids(doc):
+    """
+    Get the ids of all view reference symbols(types) and view continuations symbols (types) used by
     view reference types and view continuation types in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    
+
     :return: List of ids of all view family symbols(types).
     :rtype: list Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     ids = []
-    viewContTypes = GetAllViewContinuationTypeIds(doc)
-    viewRefTypes = GetAllViewReferenceTypeIdData(doc)
+    view_cont_types = get_all_view_continuation_type_ids(doc)
+    view_ref_types = get_all_view_reference_type_id_data(doc)
     # get ids of symbols used in view ref types
-    idsCont = GetSymbolIdsFromTypeIds(doc, viewContTypes)
-    idsViewRefs = []
-    for key,value in viewRefTypes.items():
-        idsViewRefs = idsViewRefs + GetSymbolIdsFromTypeIds(doc, viewRefTypes[key])
+    ids_cont = get_symbol_ids_from_type_ids(doc, view_cont_types)
+    ids_view_refs = []
+    for key, value in view_ref_types.items():
+        ids_view_refs = ids_view_refs + get_symbol_ids_from_type_ids(
+            doc, view_ref_types[key]
+        )
     # build unique dictionary
-    for idC in idsCont:
-        ids.append(idC)
-    for idV in idsViewRefs:
-        if(idV not in ids):
-            ids.append(idV)
+    for id_c in ids_cont:
+        ids.append(id_c)
+    for id_v in ids_view_refs:
+        if id_v not in ids:
+            ids.append(id_v)
     return ids
 
-def GetNestedFamilyMarkerNames(doc, usedIds):
-    '''
+
+def get_nested_family_marker_names(doc, used_ids):
+    """
     Gets nested family names from provided symbols.
 
-    - Retrieves a families from the symbols provided. 
+    - Retrieves a families from the symbols provided.
     - Opens the family document and extracts the names off all nested families within.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param usedIds: List of symbol ids.
-    :type usedIds: list of Autodesk.Revit.DB.ElementId
+    :param used_ids: List of symbol ids.
+    :type used_ids: list of Autodesk.Revit.DB.ElementId
 
     :return: List of all unique nested family names.
     :rtype: list str
-    '''
+    """
 
     names = []
-    for usedSymbolId in usedIds:
-        if(usedSymbolId != rdb.ElementId.InvalidElementId):
+    for used_symbol_id in used_ids:
+        if used_symbol_id != rdb.ElementId.InvalidElementId:
             # get the family
-            elSymbol = doc.GetElement(usedSymbolId)
-            fam = elSymbol.Family
+            el_symbol = doc.GetElement(used_symbol_id)
+            fam = el_symbol.Family
             # open family
             try:
-                famDoc = doc.EditFamily(fam)
-                nestedFamCol = rFamU.GetAllLoadableFamilies(famDoc)
-                for nFam in nestedFamCol:
-                    if(nFam.Name not in names and nFam.Name != ''):
-                        names.append(nFam.Name)        
-                famDoc.Close(False)
+                fam_doc = doc.EditFamily(fam)
+                nested_fam_col = rFamUPurge.get_all_loadable_families(fam_doc)
+                for n_fam in nested_fam_col:
+                    if n_fam.Name not in names and n_fam.Name != "":
+                        names.append(n_fam.Name)
+                fam_doc.Close(False)
             except Exception as e:
-                print (e)
-    #print (names)
+                print(e)
+    # print (names)
     return names
-
-def IsNestedFamilySymbol(doc, id, nestedFamilyNames):
-    '''
-    Returns true if symbol belongs to family in list past in.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    :param id: The element id of a symbol.
-    :type id: Autodesk.Revit.DB.ElementId
-    :param nestedFamilyNames: list of family names know to be nested families.
-    :type nestedFamilyNames: list str
-    
-    :return: True if family name derived from symbol is in list past in, otherwise False.
-    :rtype: bool
-    '''
-
-    flag = False
-    famSymbol = doc.GetElement(id)
-    fam = famSymbol.Family
-    if(fam.Name in nestedFamilyNames):
-        flag = True
-    return flag
-
-def GetUnusedViewRefAndContinuationMarkerSymbolIds(doc):
-    '''
-    Gets the ids of all view reference symbols(types) and view continuation symbols (types) not used in the model.
-
-    Not used: These symbols are not used in any view reference types, or nested in any symbols used in view reference types.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids.
-    :rtype: list Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = []
-    # compare used vs available in view ref types
-    # whatever is marked as unused: check for any instances in the model...placed on legends!
-    availableIds = GetAllViewReferenceSymbolIds(doc) # check: does this really return all continuation marker types??
-    usedIds = GetUsedViewReferenceAndContinuationMarkerSymbolIds(doc)
-    # elevation marker families might use nested families...check!
-    nestedFamilyNames = GetNestedFamilyMarkerNames(doc, usedIds)
-    checkIds = []
-    for aId in availableIds:
-        if (aId not in usedIds):
-            checkIds.append(aId)
-    # check for any instances
-    for id in checkIds:
-        instances = rFamU.GetFamilyInstancesBySymbolTypeId(doc, id).ToList()
-        if(len(instances) == 0):
-            if(IsNestedFamilySymbol(doc, id, nestedFamilyNames) == False):
-                ids.append(id)
-    return ids
-
-# ---------------------- purge unused view ref types and symbols -----------------------
-
-def GetUnusedViewReferenceTypeIdsForPurge(doc):
-    '''
-    Gets all unused view references type ids in model for purge.
-
-    This method can be used to safely delete all unused view reference types.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids.
-    :rtype: list Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = []
-    allAvailableTypeIds = GetAllViewReferenceTypeIdData(doc)
-    allUsedTypeIds = GetUsedViewReferenceTypeIdData(doc)
-    for key,value in allAvailableTypeIds.items():
-        if(allUsedTypeIds.has_key(key)):
-            for availableTypeId in allAvailableTypeIds[key]:
-                if(availableTypeId not in allUsedTypeIds[key]):
-                    ids.append(availableTypeId)
-        else:
-            # add all types under this key to be purge list...might need to check whether I need to leave one behind...
-            if(len(allAvailableTypeIds[key])>0):
-                ids = ids + allAvailableTypeIds[key]
-    return ids
-
-# ---------------------- purge unused view continuation types-----------------------
-
-def GetUnusedContinuationMarkerTypeIdsForPurge(doc):
-    '''
-    Gets all unused view continuation type ids in model for purge.
-
-    This method can be used to safely delete all unused view continuation marker types.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids.
-    :rtype: list Autodesk.Revit.DB.ElementId
-    '''
-
-    ids = []
-    allAvailableTypeIds = GetAllViewContinuationTypeIds(doc)
-    allUsedTypeIds = GetUsedViewContinuationTypeIds(doc)
-    for aId in allAvailableTypeIds:
-        if( aId not in allUsedTypeIds):
-            ids.append(aId)
-    return ids
-
-# ---------------------- purge unused view ref symbol and continuation symbols -----------------------
-
-def GetUnusedViewRefAndContinuationMarkerFamiliesForPurge(doc):
-    '''
-    Gets the ids of all view reference symbols(types) ids and or family ids not used in the model for purging.
-
-    This method can be used to safely delete all unused view reference and continuation marker family symbols\
-        or families.
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-
-    :return: List of element ids.
-    :rtype: list Autodesk.Revit.DB.ElementId
-    '''
-
-    return rFamU.GetUnusedInPlaceIdsForPurge(doc, GetUnusedViewRefAndContinuationMarkerSymbolIds)
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitWarnings.py` & `DuHast-0.0.7/src/duHast/Revit/Warnings/warnings.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 This module contains a number of helper functions relating to Revit warnings. 
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -27,44 +27,51 @@
 #
 
 import clr
 import System
 
 # -------------------------------------------- common variables --------------------
 #: header used in reports
-REPORT_WARNINGS_HEADER = ['HOSTFILE','ID', 'NAME', 'WARNING TYPE', 'NUMBER OF WARNINGS']
+REPORT_WARNINGS_HEADER = [
+    "HOSTFILE",
+    "ID",
+    "NAME",
+    "WARNING TYPE",
+    "NUMBER OF WARNINGS",
+]
 
 # --------------------------------------------- utility functions ------------------
 
-def GetWarnings(doc):
-    '''
+
+def get_warnings(doc):
+    """
     Returns a list of warnings from the model
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: List of all failure messages in model.
     :rtype: list of Autodesk.Revit.DB.FailureMessage
-    '''
+    """
 
     return doc.GetWarnings()
 
-def GetWarningsByGuid(doc, guid):
-    '''
+
+def get_warnings_by_guid(doc, guid):
+    """
     Returns all failure message objects where failure definition has matching GUID
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :param guid: Filter: Identifying a specific failure of which the corresponding messages are to be returned.
     :type guid: Autodesk.Revit.DB.Guid
-    
+
     :return: list of all failure messages with matching guid
     :rtype: list of Autodesk.Revit.DB.FailureMessage
-    '''
+    """
 
-    filteredWarnings = []
+    filtered_warnings = []
     warnings = doc.GetWarnings()
     for warning in warnings:
-        if(str(warning.GetFailureDefinitionId().Guid) == guid):
-            filteredWarnings.append(warning)
-    return filteredWarnings
-
+        if str(warning.GetFailureDefinitionId().Guid) == guid:
+            filtered_warnings.append(warning)
+    return filtered_warnings
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitWarningsSolverDuplicateMark.py` & `DuHast-0.0.7/src/duHast/Revit/Warnings/solver_duplicate_mark.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,95 +1,118 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Duplicate mark warnings solver class.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2020  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.APISamples import RevitElementParameterSetUtils as rParaSet
-from duHast.Utilities import Result as res
+from duHast.Revit.Common import parameter_get_utils as rParaGet
+from duHast.Revit.Common import parameter_set_utils as rParaSet
+from duHast.Utilities.Objects import result as res
 
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
+from duHast.Utilities.Objects import base
 
-class RevitWarningsSolverDuplicateMark:
 
-    def __init__(self, filterFunc, filterValues = []):
-        '''
+class RevitWarningsSolverDuplicateMark(base.Base):
+    def __init__(self, filter_func, filter_values=[]):
+        """
         Constructor: this solver takes two arguments: a filter function and a list of values to filter by
 
-        :param filterFunc: A function to filter elements in warnings by
-        :type filterFunc: func(document, elementId, list of filter values)
-        :param filterValues: A list of filter values, defaults to []
-        :type filterValues: list, optional
-        '''
-
-        self.filter = filterFunc
-        self.filterValues = filterValues
-        self.filterName = 'Duplicate mark value.'
+        :param filter_func: A function to filter elements in warnings by
+        :type filter_func: func(document, elementId, list of filter values)
+        :param filter_values: A list of filter values, defaults to []
+        :type filter_values: list, optional
+        """
+
+        # ini super class to allow multi inheritance in children!
+        super(RevitWarningsSolverDuplicateMark, self).__init__()
+
+        self.filter = filter_func
+        self.filter_values = filter_values
+        self.filter_name = "Duplicate mark value."
 
     # --------------------------- duplicate mark guid ---------------------------
     #: guid identifying this specific warning
-    GUID = '6e1efefe-c8e0-483d-8482-150b9f1da21a'
-    
-    def SolveWarnings(self, doc, warnings):
-        '''
+    GUID = "6e1efefe-c8e0-483d-8482-150b9f1da21a"
+
+    def solve_warnings(self, doc, warnings):
+        """
         Solver setting element mark to nothing, provided it passes the filter.
 
         :param doc: Current Revit model document.
         :type doc: Autodesk.Revit.DB.Document
         :param warnings: List of warnings to be solved.
         :type warnings: Autodesk.Revit.DB.FailureMessage
 
-        :return: 
+        :return:
             Result class instance.
-            
+
             - .result = True if all duplicate mark warnings could be solved. Otherwise False.
             - .message will contain stats in format parameter value set to ''
-        
+
         :rtype: :class:`.Result`
-        '''
+        """
 
-        returnValue = res.Result()
-        if(len(warnings) > 0):
+        return_value = res.Result()
+        if len(warnings) > 0:
             for warning in warnings:
-                elementIds = warning.GetFailingElements()
-                for elId in elementIds:
-                    element = doc.GetElement(elId)
+                element_ids = warning.GetFailingElements()
+                for el_id in element_ids:
+                    element = doc.GetElement(el_id)
                     # check whether element passes filter
-                    if(self.filter(doc, elId, self.filterValues)):
+                    if self.filter(doc, el_id, self.filter_values):
                         try:
-                            pValue = rParaGet.get_built_in_parameter_value(element, rdb.BuiltInParameter.ALL_MODEL_MARK)
-                            if (pValue != None):
-                                result = rParaSet.set_built_in_parameter_value(doc, element, rdb.BuiltInParameter.ALL_MODEL_MARK, '')
-                                returnValue.Update(result)
+                            p_value = rParaGet.get_built_in_parameter_value(
+                                element, rdb.BuiltInParameter.ALL_MODEL_MARK
+                            )
+                            if p_value != None:
+                                result = rParaSet.set_built_in_parameter_value(
+                                    doc,
+                                    element,
+                                    rdb.BuiltInParameter.ALL_MODEL_MARK,
+                                    "",
+                                )
+                                return_value.update(result)
                         except Exception as e:
-                            returnValue.UpdateSep(False, 'Failed to solve warning duplicate mark with exception: ' + str(e))
+                            return_value.update_sep(
+                                False,
+                                "Failed to solve warning duplicate mark with exception: {}".format(
+                                    e
+                                ),
+                            )
                     else:
-                        returnValue.UpdateSep(True,'Element removed by filter:' + self.filterName + ' : ' + rdb.Element.Name.GetValue(element))
+                        return_value.update_sep(
+                            True,
+                            "Element removed by filter: {} : {}".format(
+                                self.filter_name, rdb.Element.Name.GetValue(element)
+                            ),
+                        )
         else:
-            returnValue.UpdateSep(True,'No warnings of type: duplicate mark in model.')
-        return returnValue
+            return_value.update_sep(
+                True, "No warnings of type: duplicate mark in model."
+            )
+        return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/APISamples/RevitWorksets.py` & `DuHast-0.0.7/src/duHast/Revit/Common/worksets.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 A number of helper functions relating to Revit worksets.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -23,382 +23,412 @@
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
+
 clr.AddReference("System.Core")
 from System import Linq
+
 clr.ImportExtensions(Linq)
 
 import System
 
 # import common library modules
-from duHast.APISamples import RevitElementParameterGetUtils as rParaGet
-from duHast.Utilities import Result as res
-from duHast.APISamples import RevitTransaction as rTran
-from duHast.Utilities import Utility as util
+from duHast.Revit.Common import parameter_get_utils as rParaGet
+from duHast.Utilities.Objects import result as res
+from duHast.Revit.Common import transaction as rTran
+from duHast.Utilities import utility as util
+from duHast.Utilities import files_io as filesIO
+from duHast.Utilities import files_tab as filesTab
 
 # import Autodesk
 import Autodesk.Revit.DB as rdb
 
-# -------------------------------------------- common variables --------------------
-#: header used in reports
-REPORT_WORKSETS_HEADER = ['HOSTFILE','ID', 'NAME', 'ISVISIBLEBYDEFAULT']
-
 # --------------------------------------------- utility functions ------------------
 
-def GetWorksetIdByName(doc, worksetName):
-    '''
+
+def get_workset_id_by_name(doc, workset_name):
+    """
     Returns the element id of a workset identified by its name, otherwise invalid Id (-1) if no such workset exists
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param worksetName: The name of the workset of which to retrieve the Element Id
-    :type worksetName: str
-    
+    :param workset_name: The name of the workset of which to retrieve the Element Id
+    :type workset_name: str
+
     :return: The workset element id, otherwise invalid Id (-1) if no such workset exists
     :rtype: Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     id = rdb.ElementId.InvalidElementId
     for p in rdb.FilteredWorksetCollector(doc).OfKind(rdb.WorksetKind.UserWorkset):
-        if(p.Name == worksetName):
+        if p.Name == workset_name:
             id = p.Id
             break
     return id
 
-def GetWorksetNameById(doc, idInteger):
-    '''
+
+def get_workset_name_by_id(doc, id_integer):
+    """
     Returns the name of the workset identified by its Element Id, otherwise 'unknown' if no such workset exists
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param idInteger: The element id as integer value.
-    :type idInteger: int
-    
+    :param id_integer: The element id as integer value.
+    :type id_integer: int
+
     :return: The name of the workset identified by its Id, otherwise 'unknown'
     :rtype: str
-    '''
+    """
 
-    name = 'unknown'
+    name = "unknown"
     for p in rdb.FilteredWorksetCollector(doc).OfKind(rdb.WorksetKind.UserWorkset):
-        if(p.Id.IntegerValue == idInteger):
+        if p.Id.IntegerValue == id_integer:
             name = p.Name
             break
     return name
 
-def GetWorksetIds(doc):
-    '''
+
+def get_workset_ids(doc):
+    """
     Gets all ids of all user defined worksets in a model
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    
+
     :return: List of all user defined workset element ids
     :rtype: list Autodesk.Revit.DB.ElementId
-    '''
+    """
 
     id = []
     for p in rdb.FilteredWorksetCollector(doc).OfKind(rdb.WorksetKind.UserWorkset):
-      id.append(p.Id)
+        id.append(p.Id)
     return id
 
-def GetWorksets(doc):
-    '''
+
+def get_worksets(doc):
+    """
     Returns all user defined worksets in the model as list.
 
     Will return a list of zero length if no worksets in the model.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    
+
     :return: List of worksets
     :rtype: list of Autodesk.Revit.DB.Workset
-    '''
+    """
 
-    worksets = rdb.FilteredWorksetCollector(doc).OfKind(rdb.WorksetKind.UserWorkset).ToList()
+    worksets = (
+        rdb.FilteredWorksetCollector(doc).OfKind(rdb.WorksetKind.UserWorkset).ToList()
+    )
     return worksets
 
-def GetWorksetsFromCollector(doc):
-    '''
+
+def get_worksets_from_collector(doc):
+    """
     Returns all user defined worksets in the model as collector.
-    
+
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
 
     :return: A filtered elements collector of user defined worksets
     :rtype: Autodesk.Revit.DB.FilteredElementCollector
-    '''
+    """
 
     collector = rdb.FilteredWorksetCollector(doc).OfKind(rdb.WorksetKind.UserWorkset)
     return collector
 
-def OpenWorksetsWithElementsHack(doc):
-    '''
+
+def open_worksets_with_elements_hack(doc):
+    """
     This is based on a hack from the AutoDesk forum and an article from the building coder:
 
     - https://forums.autodesk.com/t5/revit-api-forum/open-closed-worksets-in-open-document/td-p/6238121
     - https://thebuildingcoder.typepad.com/blog/2018/03/switch-view-or-document-by-showing-elements.html
 
     this method will open worksets in a model containing elements only
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    '''
+    """
 
     # get worksets in model
-    worksetIds = GetWorksetIds(doc)
+    workset_ids = get_workset_ids(doc)
     # loop over workset and open if anything is on them
-    for wId in worksetIds:
-        workset = rdb.ElementWorksetFilter(wId)
-        elemIds = rdb.FilteredElementCollector(doc).WherePasses(workset).ToElementIds()
-        if (len(elemIds)>0):
+    for w_id in workset_ids:
+        workset = rdb.ElementWorksetFilter(w_id)
+        elem_ids = rdb.FilteredElementCollector(doc).WherePasses(workset).ToElementIds()
+        if len(elem_ids) > 0:
             # this will force Revit to open the workset containing this element
-           rdb.uidoc.ShowElements(elemIds.First())
+            rdb.uidoc.ShowElements(elem_ids.First())
+
 
-def ModifyElementWorkset(doc, defaultWorksetName, collector, elementTypeName):
-    '''
+def modify_element_workset(doc, default_workset_name, collector, element_type_name):
+    """
     Attempts to change the worksets of elements provided through an element collector.
 
     Will return false if target workset does not exist in file.
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param defaultWorksetName: The name of the workset the elements are to be moved to.
-    :type defaultWorksetName: str
+    :param default_workset_name: The name of the workset the elements are to be moved to.
+    :type default_workset_name: str
     :param collector: The element collector containing the elements.
     :type collector: Autodesk.Revit.DB.FilteredElementCollector
-    :param elementTypeName: A description used in the status message returned.
-    :type elementTypeName: str
-    
-    :return: 
+    :param element_type_name: A description used in the status message returned.
+    :type element_type_name: str
+
+    :return:
         Result class instance.
-        
+
         - .result = True if successfully moved all elements to new workset. Otherwise False.
         - .message will contain stats in format [success :: failure]
-    
+
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
-    returnValue.message = 'Changing ' + elementTypeName + ' workset to '+ defaultWorksetName
+    return_value = res.Result()
+    return_value.message = "Changing: {} workset to: {} ".format(
+        element_type_name, default_workset_name
+    )
     # get the ID of the default grids workset
-    defaultId = GetWorksetIdByName(doc, defaultWorksetName)
-    counterSuccess = 0
-    counterFailure = 0
+    default_id = get_workset_id_by_name(doc, default_workset_name)
+    counter_success = 0
+    counter_failure = 0
     # check if invalid id came back..workset no longer exists..
-    if(defaultId != rdb.ElementId.InvalidElementId):
+    if default_id != rdb.ElementId.InvalidElementId:
         # get all elements in collector and check their workset
         for p in collector:
-            if (p.WorksetId != defaultId):
+            if p.WorksetId != default_id:
                 # get the element name
-                elementName = 'Unknown Element Name'
+                element_name = "Unknown Element Name"
                 try:
-                    elementName = rdb.Element.Name.GetValue(p)
-                except Exception :
+                    element_name = rdb.Element.Name.GetValue(p)
+                except Exception:
                     pass
                 # move element to new workset
-                transaction = rdb.Transaction(doc, "Changing workset: " + elementName)
-                trannyStatus = rTran.in_transaction(transaction, GetActionChangeElementWorkset(p, defaultId))
-                if (trannyStatus.status == True):
-                    counterSuccess += 1
+                transaction = rdb.Transaction(
+                    doc, "Changing workset: ".format(element_name)
+                )
+                tranny_status = rTran.in_transaction(
+                    transaction, get_action_change_element_workset(p, default_id)
+                )
+                if tranny_status.status == True:
+                    counter_success += 1
                 else:
-                    counterFailure += 1
-                returnValue.status = returnValue.status & trannyStatus.status
+                    counter_failure += 1
+                return_value.status = return_value.status & tranny_status.status
             else:
-                counterSuccess += 1
-                returnValue.status = returnValue.status & True 
+                counter_success += 1
+                return_value.status = return_value.status & True
     else:
-        returnValue.UpdateSep(False, 'Default workset '+ defaultWorksetName + ' does no longer exists in file!')
-    returnValue.AppendMessage('Moved ' + elementTypeName + ' to workset ' + defaultWorksetName + ' [' + str(counterSuccess) + ' :: ' + str(counterFailure) +']')
-    return returnValue
+        return_value.update_sep(
+            False,
+            "Default workset: {} does no longer exists in file!".format(
+                default_workset_name
+            ),
+        )
+    return_value.append_message(
+        "Moved: {} to workset: {} [ {} :: {}]".format(
+            element_type_name, default_workset_name, counter_success, counter_failure
+        )
+    )
+    return return_value
 
-def GetActionChangeElementWorkset(el, defaultId):
-    '''
+
+def get_action_change_element_workset(el, default_id):
+    """
     Contains the required action to change a single elements workset
 
     :param el: The element
     :type el: Autodesk.Revit.DB.Element
-    :param defaultId: The workset element Id
-    :type defaultId: Autodesk.Revit.DB.ElementId
-    '''
+    :param default_id: The workset element Id
+    :type default_id: Autodesk.Revit.DB.ElementId
+    """
 
     def action():
-        actionReturnValue = res.Result()
+        action_return_value = res.Result()
         try:
-            wsParam = el.get_Parameter(rdb.BuiltInParameter.ELEM_PARTITION_PARAM)
-            wsParam.Set(defaultId.IntegerValue)
-            actionReturnValue.message = 'Changed element workset.'
+            ws_param = el.get_Parameter(rdb.BuiltInParameter.ELEM_PARTITION_PARAM)
+            ws_param.Set(default_id.IntegerValue)
+            action_return_value.message = "Changed element workset."
         except Exception as e:
-            actionReturnValue.UpdateSep(False, 'Failed with exception: ' + str(e))
-        return actionReturnValue
+            action_return_value.update_sep(False, "Failed with exception: {}".format(e))
+        return action_return_value
+
     return action
 
-def IsElementOnWorksetById(doc, el, worksetId):
-    '''
+
+def is_element_on_workset_by_id(doc, el, workset_id):
+    """
     Checks whether an element is on a given workset
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
     :param el: The element.
     :type el: Autodesk.Revit.DB.Element
-    :param worksetId: The workset element Id
-    :type worksetId: Autodesk.Revit.DB.ElementId
-    
+    :param workset_id: The workset element Id
+    :type workset_id: Autodesk.Revit.DB.ElementId
+
     :return: True if element is on given workset, otherwise False
     :rtype: bool
-    '''
+    """
 
     flag = True
     try:
-        wsParam = el.get_Parameter(rdb.BuiltInParameter.ELEM_PARTITION_PARAM)
-        currentWorksetName = rParaGet.get_parameter_value(wsParam)
-        compareToWorksetName = GetWorksetNameById(doc, worksetId.IntegerValue)
-        if(compareToWorksetName != currentWorksetName):
+        ws_param = el.get_Parameter(rdb.BuiltInParameter.ELEM_PARTITION_PARAM)
+        current_workset_name = rParaGet.get_parameter_value(ws_param)
+        compare_to_workset_name = get_workset_name_by_id(doc, workset_id.IntegerValue)
+        if compare_to_workset_name != current_workset_name:
             flag = False
     except Exception as e:
-        print (e)
+        print(e)
         flag = False
     return flag
 
-def IsElementOnWorksetByName(el, worksetName):
-    '''
+
+def is_element_on_workset_by_name(el, workset_name):
+    """
     Checks whether an element is on a workset identified by name
 
     :param el: The element
     :type el: Autodesk.Revit.DB.Element
-    :param worksetName: The name of the workset
-    :type worksetName: str
+    :param workset_name: The name of the workset
+    :type workset_name: str
 
     :return: True if element is on given workset, otherwise False
     :rtype: bool
-    '''
+    """
 
     flag = True
     try:
-        wsParam = el.get_Parameter(rdb.BuiltInParameter.ELEM_PARTITION_PARAM)
-        currentWorksetName = rParaGet.get_parameter_value(wsParam)
-        if(worksetName != currentWorksetName):
+        ws_param = el.get_Parameter(rdb.BuiltInParameter.ELEM_PARTITION_PARAM)
+        current_workset_name = rParaGet.get_parameter_value(ws_param)
+        if workset_name != current_workset_name:
             flag = False
     except Exception as e:
-        print ("IsElementOnWorksetByName: " + str(e))
+        print("IsElementOnWorksetByName: " + str(e))
         flag = False
     return flag
 
-def GetElementWorksetName(el):
-    '''
+
+def get_element_workset_name(el):
+    """
     Returns the name of the workset an element is on, or 'invalid workset'.
 
     :param el: The element.
     :type el: Autodesk.Revit.DB.Element
     :return: The name of the workset. If an exception occurred it wil return 'invalid workset'.
     :rtype: str
-    '''
+    """
 
-    workSetname = 'invalid workset'
+    work_setname = "invalid workset"
     try:
-        wsParam = el.get_Parameter(rdb.BuiltInParameter.ELEM_PARTITION_PARAM)
-        workSetname = rParaGet.get_parameter_value(wsParam)
+        ws_param = el.get_Parameter(rdb.BuiltInParameter.ELEM_PARTITION_PARAM)
+        work_setname = rParaGet.get_parameter_value(ws_param)
     except Exception as e:
-        print ("GetElementWorksetName: " + str(e))
-    return workSetname
+        print("GetElementWorksetName: " + str(e))
+    return work_setname
+
 
-def UpdateWorksetDefaultVisibilityFromReport(doc, reportPath, revitFilePath):
-    '''
+def update_workset_default_visibility_from_report(doc, report_path, revit_file_path):
+    """
     Updates the default visibility of worksets based on a workset report file.
 
     The data for the report files is generated by GetWorksetReportData() function in this module
 
     :param doc: Current Revit model document.
     :type doc: Autodesk.Revit.DB.Document
-    :param reportPath: The fully qualified file path to tab separated report text file containing workset data.
-    :type reportPath: str
-    :param revitFilePath: The fully qualified file path of the Revit file. Will be used to identify the file in the report data.
-    :type revitFilePath: str
+    :param report_path: The fully qualified file path to tab separated report text file containing workset data.
+    :type report_path: str
+    :param revit_file_path: The fully qualified file path of the Revit file. Will be used to identify the file in the report data.
+    :type revit_file_path: str
 
-    :return: 
+    :return:
         Result class instance.
-        
+
         - .result = True if:
 
             - successfully updated all workset default visibility where different to report
-            - or none needed updating. 
-        
+            - or none needed updating.
+
         - Otherwise False:
 
             - An exception occurred.
             - A workset has no matching data in the report.
-        
+
         - Common:
-        
+
             - .message will contain each workset and whether it needed updating or not
-    
+
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
+    return_value = res.Result()
     # read report
-    worksetData = util.ReadTabSeparatedFile(reportPath)
-    fileName = util.GetFileNameWithoutExt(revitFilePath)
-    worksetDataForFile = {}
-    for row in worksetData:
-        if(util.GetFileNameWithoutExt(row[0]).startswith(fileName) and len(row) > 3):
-            worksetDataForFile[row[1]] = util.ParsStringToBool(row[3])
-    if(len(worksetDataForFile) > 0): 
+    workset_data = filesTab.read_tab_separated_file(report_path)
+    file_name = filesIO.get_file_name_without_ext(revit_file_path)
+    workset_data_for_file = {}
+    for row in workset_data:
+        if (
+            filesIO.get_file_name_without_ext(row[0]).startswith(file_name)
+            and len(row) > 3
+        ):
+            workset_data_for_file[row[1]] = util.parse_string_to_bool(row[3])
+    if len(workset_data_for_file) > 0:
         # updates worksets
-        worksets = GetWorksets(doc)
+        worksets = get_worksets(doc)
         for workset in worksets:
-            if(str(workset.Id) in worksetDataForFile):
-                if (workset.IsVisibleByDefault != worksetDataForFile[str(workset.Id)]):
+            if str(workset.Id) in workset_data_for_file:
+                if workset.IsVisibleByDefault != workset_data_for_file[str(workset.Id)]:
+
                     def action():
-                        actionReturnValue = res.Result()
-                        defaultVisibility  = rdb.WorksetDefaultVisibilitySettings.GetWorksetDefaultVisibilitySettings(doc)
+                        action_return_value = res.Result()
+                        default_visibility = rdb.WorksetDefaultVisibilitySettings.GetWorksetDefaultVisibilitySettings(
+                            doc
+                        )
                         try:
-                            defaultVisibility.SetWorksetVisibility(workset.Id, worksetDataForFile[str(workset.Id)])
-                            actionReturnValue.UpdateSep(True, workset.Name + ': default visibility settings changed to: \t[' + str(worksetDataForFile[str(workset.Id)]) + ']')
+                            default_visibility.SetWorksetVisibility(
+                                workset.Id, workset_data_for_file[str(workset.Id)]
+                            )
+                            action_return_value.update_sep(
+                                True,
+                                "{}: default visibility settings changed to: \t[{}]".format(
+                                    workset.Name, workset_data_for_file[str(workset.Id)]
+                                ),
+                            )
                         except Exception as e:
-                            actionReturnValue.UpdateSep(False, 'Failed with exception: ' + str(e))
-                        return actionReturnValue
+                            action_return_value.update_sep(
+                                False, "Failed with exception: {}".format(e)
+                            )
+                        return action_return_value
+
                     # move element to new workset
-                    transaction = rdb.Transaction(doc, workset.Name + ": Changing default workset visibility")
-                    trannyStatus = rTran.in_transaction(transaction, action)
-                    returnValue.Update(trannyStatus)
+                    transaction = rdb.Transaction(
+                        doc,
+                        "{}: Changing default workset visibility".format(workset.Name),
+                    )
+                    tranny_status = rTran.in_transaction(transaction, action)
+                    return_value.update(tranny_status)
                 else:
-                    returnValue.UpdateSep(True, util.EncodeAscii(workset.Name) + ': default visibility settings unchanged.')
+                    return_value.update_sep(
+                        True,
+                        "{}: default visibility settings unchanged.".format(
+                            util.encode_ascii(workset.Name)
+                        ),
+                    )
             else:
-                returnValue.UpdateSep(False, util.EncodeAscii(workset.Name) + ': has no corresponding setting in settings file.')
+                return_value.update_sep(
+                    False,
+                    "{}: has no corresponding setting in settings file.".format(
+                        util.encode_ascii(workset.Name)
+                    ),
+                )
     else:
-        returnValue.UpdateSep(True, 'No settings found for file: ' + fileName)
-    return returnValue
-
-# ------------------------------------------------------- workset reporting --------------------------------------------------------------------
-
-
-def GetWorksetReportData(doc, revitFilePath):
-    '''
-    Gets workset data ready for being written to file.
-
-    - HOSTFILE
-    - ID
-    - NAME
-    - ISVISIBLEBYDEFAULT
-
-    :param doc: Current Revit model document.
-    :type doc: Autodesk.Revit.DB.Document
-    :param revitFilePath: The fully qualified file path of Revit file.
-    :type revitFilePath: str
-    
-    :return: The workset data in a nested list of string
-    :rtype: list of list of str
-    '''
-
-    data = []
-    worksets = GetWorksetsFromCollector(doc)
-    for ws in worksets:
-        data.append([
-            revitFilePath, 
-            str(ws.Id.IntegerValue), 
-            util.EncodeAscii(ws.Name), 
-            str(ws.IsVisibleByDefault)])
-    return data
+        return_value.update_sep(
+            True, "No settings found for file: {}".format(file_name)
+        )
+    return return_value
```

### Comparing `DuHast-0.0.6/src/duHast/DataSamples/DataBase.py` & `DuHast-0.0.7/src/duHast/Data/Objects/Properties/Geometry/from_revit_elements.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,20 +1,19 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Data base class for Revit object properties.
+Utility function getting 2D points from element solids.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
-
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2023  Jan Christel
+# Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
@@ -23,44 +22,32 @@
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-import json
-
-class DataBase(object):
-
-    def __init__(self, data_type):
-        self.dataType = data_type
+from duHast.Revit.Common.Geometry import solids as rSolid
 
-    def __repr__(self):
-        '''
-        Enables detailed debug output of all class properties using: rep(obj)
-
-        :return: A string listing class properties and their respective values.
-        :rtype: string
-        '''
-
-        return '{}({})'.format(self.__class__.__name__, ', '.join('{}={!r}'.format(k, v) for k, v in self.__dict__.items()))
-    
-    def to_json(self):
-        '''
-        Convert the instance of this class to json.
-        
-        :return: A Json object.
-        :rtype: json
-        '''
-
-        return json.dumps(self, indent = None, default=lambda o: o.__dict__)
-    
-    @property
-    def DataType(self):
-        '''
-        Property: returns the data type of this class.
-
-        :return: 'ceiling'
-        :rtype: str
-        '''
 
-        return self.dataType
+def get_2d_points_from_revit_element_type_in_model(doc, element_instance_getter):
+    """
+    Returns a list of lists of points representing the flattened(2D geometry) of the elements
+    List of Lists because a elements can be made up of multiple solids. Each nested list represents one solid within the elements geometry.
+    Does not work with in place elements.
+
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param element_instance_getter: Function returning all element instances of a particular category in the model as an element collector
+    :type element_instance_getter: func(doc)
+
+    :return: A list of data geometry instances.
+    :rtype: list of :class:`.DataGeometry`
+    """
+
+    element_instances = element_instance_getter(doc)
+    all_element_points = []
+    for element_instance in element_instances:
+        element_points = rSolid.get_2d_points_from_solid(element_instance)
+        if len(element_points) > 0:
+            all_element_points.append(element_points)
+    return all_element_points
```

### Comparing `DuHast-0.0.6/src/duHast/DataSamples/DataCeiling.py` & `DuHast-0.0.7/src/duHast/Data/Objects/data_room.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,124 +1,118 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Data storage class for Revit ceiling properties.
+Data storage class for Revit room properties.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import json
-from duHast.DataSamples import DataGeometry
-from duHast.DataSamples import DataDesignSetOption
-from duHast.DataSamples import DataPhasing
-from duHast.DataSamples import DataLevel
-from duHast.DataSamples import DataTypeProperties
-from duHast.DataSamples import DataInstanceProperties
-from duHast.DataSamples import DataRevitModel
-from duHast.DataSamples import DataBase
-
-class DataCeiling(DataBase.DataBase):
-
-    dataType = 'ceiling'
-    
-    def __init__(self, j = {}):
-        '''
+
+from duHast.Data.Objects.Properties import data_design_set_option
+from duHast.Data.Objects.Properties import data_phasing
+from duHast.Data.Objects.Properties import data_level
+from duHast.Data.Objects.Properties import data_instance_properties
+from duHast.Data.Objects.Properties import data_revit_model
+from duHast.Data.Utils import data_base
+from duHast.Data.Objects.Properties import data_element_geometry
+
+
+class DataRoom(data_base.DataBase, data_element_geometry.DataElementGeometryBase):
+    data_type = "room"
+
+    def __init__(self, j={}):
+        """
         Class constructor.
 
         :param j: A json formatted dictionary of this class, defaults to {}
         :type j: dict, optional
-        '''
+        """
 
+        # initialise parent classes with values
+        super(DataRoom, self).__init__(data_type=DataRoom.data_type, j=j)
 
-        # store data type  in base class
-        super(DataCeiling, self).__init__('ceiling')
-        
         # check if any data was past in with constructor!
-        if(j != None and len(j) > 0 ):
-            # check type of data that came in: 
-            if(type(j) == str):
+        if j != None and len(j) > 0:
+            # check type of data that came in:
+            if type(j) == str:
                 # a string
                 j = json.loads(j)
-            elif(type(j) == dict):
+            elif type(j) == dict:
                 # no action required
                 pass
             else:
-                raise  ValueError ('Argument supplied must be of type string or type dictionary')
-            
-            if ('instanceProperties' in j):
-                self.instanceProperties = DataInstanceProperties.DataInstanceProperties(j['instanceProperties'])
-            else:
-                self.instanceProperties = DataInstanceProperties.DataInstanceProperties()
-            
-            if('designSetAndOption' in j):
-                self.designSetAndOption = DataDesignSetOption.DataDesignSetOption(j['designSetAndOption'])
-            else:
-                self.designSetAndOption = DataDesignSetOption.DataDesignSetOption()            
-            
-            if('typeProperties' in j):
-                self.typeProperties = DataTypeProperties.DataTypeProperties(j['typeProperties'])
-            else:
-                self.typeProperties = DataTypeProperties.DataTypeProperties()       
-
-            if('level' in j):
-                self.level = DataLevel.DataLevel(j['level'])
-            else:
-                self.level = DataLevel.DataLevel()
-
-            if('revitModel' in j):
-                self.revitModel = DataRevitModel.DataRevitModel(j['revitModel'])
-            else:
-                self.revitModel = DataRevitModel.DataRevitModel()  
-
-            if('phasing' in j):
-                self.phasing = DataPhasing.DataPhasing(j['phasing'])
-            else:
-                self.phasing = DataPhasing.DataPhasing() 
-
-            # load geometry
-            geometry_data_list = []
-            if('geometry' in j):
-                for item in j['geometry']:
-                    if('dataType' in item):
-                        if(item['dataType']):
-                            dummy = DataGeometry.DataGeometry(item)
-                            geometry_data_list.append(dummy)
-                        else:
-                            print('no data type in geometry item')
-            self.geometry = geometry_data_list
-
-            # load associated elements
-            if('associatedElements' in j):
-                self.associatedElements = j['associatedElements']
+                raise ValueError(
+                    "Argument supplied must be of type string or type dictionary"
+                )
+
+            if data_instance_properties.DataInstanceProperties.data_type in j:
+                self.instance_properties = (
+                    data_instance_properties.DataInstanceProperties(
+                        j[data_instance_properties.DataInstanceProperties.data_type]
+                    )
+                )
+            else:
+                self.instance_properties = (
+                    data_instance_properties.DataInstanceProperties()
+                )
+
+            if data_design_set_option.DataDesignSetOption.data_type in j:
+                self.design_set_and_option = data_design_set_option.DataDesignSetOption(
+                    j[data_design_set_option.DataDesignSetOption.data_type]
+                )
             else:
-                self.associatedElements =[] 
+                self.design_set_and_option = (
+                    data_design_set_option.DataDesignSetOption()
+                )
 
+            if "associated_elements" in j:
+                self.associated_elements = j["associated_elements"]
+            else:
+                self.associated_elements = []
+
+            if data_level.DataLevel.data_type in j:
+                self.level = data_level.DataLevel(j[data_level.DataLevel.data_type])
+            else:
+                self.level = data_level.DataLevel()
+
+            if data_revit_model.DataRevitModel.data_type in j:
+                self.revit_model = data_revit_model.DataRevitModel(
+                    j[data_revit_model.DataRevitModel.data_type]
+                )
+            else:
+                self.revit_model = data_revit_model.DataRevitModel()
+
+            if data_phasing.DataPhasing.data_type in j:
+                self.phasing = data_phasing.DataPhasing(
+                    j[data_phasing.DataPhasing.data_type]
+                )
+            else:
+                self.phasing = data_phasing.DataPhasing()
         else:
-            self.associatedElements = []
-            self.geometry = [[]]
             # initialise classes with default values
-            self.instanceProperties = DataInstanceProperties.DataInstanceProperties()
-            self.typeProperties = DataTypeProperties.DataTypeProperties()
-            self.level = DataLevel.DataLevel()
-            self.revitModel = DataRevitModel.DataRevitModel()
-            self.phasing = DataPhasing.DataPhasing()
-            self.designSetAndOption = DataDesignSetOption.DataDesignSetOption()
+            self.associated_elements = []
+            self.instance_properties = data_instance_properties.DataInstanceProperties()
+            self.level = data_level.DataLevel()
+            self.revit_model = data_revit_model.DataRevitModel()
+            self.phasing = data_phasing.DataPhasing()
+            self.design_set_and_option = data_design_set_option.DataDesignSetOption()
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/DataSamples/DataExport.py` & `DuHast-0.0.7/src/duHast/Revit/Materials/materials.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,107 +1,95 @@
-'''
-~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Utility functions writing revit geometry data to file.
-~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
+~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+Revit materials helper functions.
+~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2023  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
-from duHast.Utilities import Utility as util
-from duHast.APISamples import RevitCeilings as rCeil
-from duHast.APISamples import RevitRooms as rRoom
-from duHast.Utilities import Result as res
+import clr
+import System
 
-from duHast.DataSamples import DataCeiling as dc
-from duHast.DataSamples import DataRoom as dr
+# import common library modules
 
-import json
-import codecs
+# import Autodesk
+import Autodesk.Revit.DB as rdb
 
-# -------------------------------- write data to file -------------------------------------------------------
+# --------------------------------------------- utility functions ------------------
 
-def get_data_from_model(doc):
-    '''
-    Gets element data from the model. This is currently limited to
 
-    - rooms
-    - ceilings
+def get_all_materials(doc):
+    """
+    Gets all materials in a model.
 
-    :param doc: The current model document.
-    :type doc: Autodeks.Revit.DB.Document
+    Filter by class.
 
-    :return: A dictionary in format {file name: str, date processed : str, room:[], ceiling:[]}
-    :rtype: {}
-    '''
+    :param doc: _description_
+    :type doc: _type_
 
-    # get data
-    allRoomData = rRoom.GetAllRoomData(doc)
-    allCeilingData = rCeil.GetAllCeilingData(doc)
+    :return: A filtered element collector of materials
+    :rtype: Autodesk.Revit.DB.FilteredElementCollector
+    """
 
-    data_json = {
-        "file name": doc.Title,
-        "date processed": util.GetDateStamp(util.FILE_DATE_STAMP_YYYY_MM_DD_HH_MM_SEC),
-        dr.DataRoom.dataType: allRoomData,
-        dc.DataCeiling.dataType: allCeilingData
-    }
+    collector = rdb.FilteredElementCollector(doc).OfClass(rdb.Material)
+    return collector
 
-    return data_json
 
+def get_material_by_id(doc, id):
+    """
+    Gets a material element based on a material id.
 
-def write_json_to_file (json_data, dataOutPutFileName):
-    '''
-    Writes collected data to a new json formatted file.
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param id: The id of material to be returned.
+    :type id: Autodesk.Revit.DB.ElementId
 
-    :param json_data: A dictionary to be written to file.
-    :type json_data: json object (dictionary)
-    :param dataOutPutFileName: Fully qualified file path to json data file.
-    :type dataOutPutFileName: str
+    :return: A material if matching id was found. Otherwise nothing gets returned!
+    :rtype: Autodesk.Revit.DB.Material
+    """
 
-    :return: 
-        Result class instance.
-        
-        - result.status. True if json data file was written successfully, otherwise False.
-        - result.message will confirm path of json data file.
-        - result.result empty list
+    mats = get_all_materials(doc)
+    for m in mats:
+        if m.Id.IntegerValue == id.IntegerValue:
+            return m
 
-        On exception:
-        
-        - result.status (bool) will be False.
-        - result.message will contain exception message.
-        - result.result will be empty
 
-    :rtype: :class:`.Result`
-    '''
+def get_material_name_by_id(doc, id):
+    """
+    Gets a material name based on a material id.
 
-    result = res.Result()
-   
+    :param doc: Current Revit model document.
+    :type doc: Autodesk.Revit.DB.Document
+    :param id: Id of material of which the name is to be returned.
+    :type id: Autodesk.Revit.DB.ElementId
 
-    try:
-        json_object = json.dumps(json_data, indent = None, default=lambda o: o.__dict__)
-        with codecs.open(dataOutPutFileName, 'w', encoding='utf-8') as f:
-            f.write(json_object)
-            f.close()
+    :return: The material name if matching id was found or the default value: '<By Category>'
+    :rtype: str
+    """
 
-        result.UpdateSep(True, 'Data written to file: ' + dataOutPutFileName)
-    except  Exception as e:
-        result.UpdateSep(False, 'Failed to write data to file with exception: ' + str(e))
-    return result
+    name = "<By Category>"
+    mats = get_all_materials(doc)
+    for m in mats:
+        if m.Id.IntegerValue == id.IntegerValue:
+            m_name = rdb.Element.Name.GetValue(m)
+            name = "" if m_name == None else m_name
+    return name
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/DataSamples/DataRevitModel.py` & `DuHast-0.0.7/src/duHast/Data/Objects/Properties/data_phasing.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,64 +1,73 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-Data storage class for Revit elements model properties.
+Data storage class for Revit element phasing properties.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2023  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import json
-from duHast.DataSamples import DataBase
+from duHast.Data.Utils import data_base
+
+
+class DataPhasing(data_base.DataBase):
 
-class DataRevitModel(DataBase.DataBase):
-    
-    dataType = 'revit model'
+    data_type = "phasing"
 
-    def __init__(self, j = {}):
-        '''
+    def __init__(self, j={}):
+        """
         Class constructor
 
         :param j:  json formatted dictionary of this class, defaults to {}
         :type j: dict, optional
-        '''
+        """
 
         # store data type  in base class
-        super(DataRevitModel, self).__init__('revit model')
-        
+        super(DataPhasing, self).__init__(DataPhasing.data_type)
+
         # check if any data was past in with constructor!
-        if(j != None and len(j) > 0 ):
-            # check type of data that came in: 
-            if(type(j) == str):
+        if j != None and len(j) > 0:
+            # check type of data that came in:
+            if type(j) == str:
                 # a string
                 j = json.loads(j)
-            elif(type(j) == dict):
+            elif type(j) == dict:
                 # no action required
                 pass
             else:
-                raise  ValueError ('Argument supplied must be of type string or type dictionary')
-        
-            if('modelName' in j ):
-                self.modelName = j['modelName']
+                raise ValueError(
+                    "Argument supplied must be of type string or type dictionary"
+                )
+
+            if "created" in j:
+                self.created = j["created"]
+            else:
+                self.created = "-"
+
+            if "demolished" in j:
+                self.demolished = j["demolished"]
             else:
-                self.modelName = '-'
+                self.demolished = "-"
         else:
-            self.modelName = '-'     
+            self.created = "-"
+            self.demolished = "-"
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/DataSamples/DataToShapely.py` & `DuHast-0.0.7/src/duHast/Data/data_to_shapely.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,235 +1,262 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Utility functions converting data retrieved from Revit into shapely geometry and processing it.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 This module requires python >3.9 due to dependencies:
 
 - numpy
 - shapely
 
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 # these packages are not available in an iron python environment .e.g. Revit Python shell
 # to avoid an exception stopping the entire package to load these are within a try catch block
 
 import shapely.geometry as sg
 import numpy as np
 
-from duHast.DataSamples import DataCeiling as dc
-from duHast.DataSamples import DataRoom as dr
+from duHast.Data.Objects import data_ceiling as dc
+from duHast.Data.Objects import data_room as dr
+
+from duHast.Data.Objects.Properties.Geometry import geometry_polygon
 
 # --------------- shapely polygon creation ------------------
 
+
 def get_translation_matrix(geometry_object):
-    '''
+    """
     Gets the rotation/ translation matrix from the geometry object
 
     :param geometry_object: A data geometry object instance.
     :type geometry_object: :class:`.DataGeometry`
 
     :return: A translation matrix.
     :rtype: numpy array
-    '''
+    """
 
-    translation_matrix = [] # translation only matrix
+    translation_matrix = []  # translation only matrix
     # note numpy creates arrays by row!
     # need to append one more row since matrix dot multiplication rule:
     # number of columns in first matrix must match number of rows in second matrix (point later on)
-    for vector in geometry_object.rotationCoord:
+    for vector in geometry_object.rotation_coord:
         vector.append(0.0)
         translation_matrix.append(vector)
-    rotation_matrix = geometry_object.translationCoord # rotation matrix
+    rotation_matrix = geometry_object.translation_coord  # rotation matrix
     # adding extra row here
     rotation_matrix.append(1.0)
     translation_matrix.append(rotation_matrix)
     # build combined rotation and translation matrix
     combined_matrix = np.array(translation_matrix)
     # transpose matrix (translation matrix in json file is stored by columns not by rows!)
     combined_matrix = np.transpose(combined_matrix)
     return combined_matrix
 
+
 def get_outer_loop_as_shapely_points(geometry_object, translation_matrix):
-    '''
-    Returns the boundary loop of an object as list of shapely points. 
-    
+    """
+    Returns the boundary loop of an object as list of shapely points.
+
     Points are translated with passed in matrix.
     Any loops containing less then 3 points will be ignored. (Empty list will be returned)
 
     :param geometry_object: A data geometry object instance.
     :type geometry_object: :class:`.DataGeometry`
     :param translation_matrix: A translation matrix.
     :type translation_matrix: numpy array
 
     :return: List of shapely points defining a polygon. (Empty list will be returned if less then 3 points in loop.)
     :rtype: List[shapely.point]
-    '''
+    """
 
     single_polygon_loop = []
-    if(geometry_object.dataType == 'polygons'):
-        for point_double in geometry_object.outerLoop:
+    if geometry_object.data_type == geometry_polygon.DataPolygon.data_type:
+        for point_double in geometry_object.outer_loop:
             # need to add 1 to list for matrix multiplication
             # number of columns in first matrix (translation) must match number of rows in second matrix (point)
-            translated_point = np.dot(translation_matrix,[point_double[0], point_double[1], point_double[2], 1.0])
-            p = sg.Point(translated_point[0],translated_point[1],translated_point[2])
+            translated_point = np.dot(
+                translation_matrix,
+                [point_double[0], point_double[1], point_double[2], 1.0],
+            )
+            p = sg.Point(translated_point[0], translated_point[1], translated_point[2])
             single_polygon_loop.append(p)
     # ignore any poly loops with less then 3 sides (less then 3 points)
-    if(len(single_polygon_loop) > 2):
+    if len(single_polygon_loop) > 2:
         return single_polygon_loop
     else:
         return []
 
+
 def get_inner_loops_as_shapely_points(geometry_object, translation_matrix):
-    '''
-    Returns the inner loops (holes) of an object as list of lists of shapely points. 
-    
+    """
+    Returns the inner loops (holes) of an object as list of lists of shapely points.
+
     Points are translated with passed in matrix.
     Any inner loops containing less then 3 points will be ignored. (Empty list will be returned)
 
     :param geoObject: A data geometry object instance.
     :type geoObject: :class:`.DataGeometry`
     :param translationM: A translation matrix.
     :type translationM: numpy array
 
     :return: List of lists of shapely points defining a polygon.
     :rtype: list [list[shapely.point]]
-    '''
-    
+    """
+
     shapely_points = []
     # get inner loops
-    if(len(geometry_object.innerLoops) > 0):
+    if len(geometry_object.inner_loops) > 0:
         # there might be more then one inner loop
-        for inner_loop in geometry_object.innerLoops:
+        for inner_loop in geometry_object.inner_loops:
             single_polygon_loop = []
             for point_double in inner_loop:
                 # need to add 1 to list for matrix multiplication
                 # number of columns in first matrix (translation) must match number of rows in second matrix (point)
-                translated_point = np.dot(translation_matrix,[point_double[0], point_double[1], point_double[2], 1.0])
-                p = sg.Point(translated_point[0],translated_point[1],translated_point[2])
+                translated_point = np.dot(
+                    translation_matrix,
+                    [point_double[0], point_double[1], point_double[2], 1.0],
+                )
+                p = sg.Point(
+                    translated_point[0], translated_point[1], translated_point[2]
+                )
                 single_polygon_loop.append(p)
             # ignore any poly loops with less then 3 sides ( less then 3 points)
-            if(len(single_polygon_loop)>2):
+            if len(single_polygon_loop) > 2:
                 shapely_points.append(single_polygon_loop)
     return shapely_points
 
+
 def build_shapely_polygon(shapely_polygons):
-    '''
+    """
     Creates shapely polygon with nested polygons from list of shapely polygons past in.
 
     Assumptions is: first polygon describes the boundary loop and any subsequent polygons are describing\
          holes within the boundary 
 
     :param shapely_polygons: list of shapely polygons
     :type shapely_polygons: list[shapely.polygon]
 
     :return: A shapely polygon.
     :rtype: shapely.polygon
-    '''
+    """
 
     # convert to shapely
     poly = None
     # check if we got multiple polygons
-    if(len(shapely_polygons) == 1):
+    if len(shapely_polygons) == 1:
         # single exterior boundary ... no holes
         poly = sg.Polygon(shapely_polygons[0])
-    elif(len(shapely_polygons) > 1):
+    elif len(shapely_polygons) > 1:
         # got holes...
         # set up interior holes to be added to polygon
         # (remember exterior point order is ccw, holes cw else
         # holes may not appear as holes.)
         interiors = {}
-        for i in range(1,len(shapely_polygons)):
-            interiors[i-1] = shapely_polygons[i]
+        for i in range(1, len(shapely_polygons)):
+            interiors[i - 1] = shapely_polygons[i]
         i_p = {k: sg.Polygon(v) for k, v in interiors.items()}
         # create polygon with holes
-        poly = sg.Polygon(shapely_polygons[0], [poly.exterior.coords for poly in i_p.values() \
-            if poly.within(sg.Polygon(shapely_polygons[0])) is True])
+        poly = sg.Polygon(
+            shapely_polygons[0],
+            [
+                poly.exterior.coords
+                for poly in i_p.values()
+                if poly.within(sg.Polygon(shapely_polygons[0])) is True
+            ],
+        )
     return poly
 
+
 def get_shapely_polygons_from_data_instance(data_instance):
-    '''
+    """
     Returns a list of of shapely polygons from data instances past in.
-    
+
     Polygons may contain holes
 
     :param data_instance: _description_
     :type data_instance: A class with .geometry property returning a :class:`.DataGeometry` instance.
-    
+
     :return: A list of shapely polygons.
     :rtype: list [shapely.polygon]
-    '''
+    """
 
     all_polygons = []
     # loop over data geometry and convert into shapely polygons
 
-    for geometry_object in data_instance.geometry:
-        if(geometry_object.dataType == 'polygons'):
+    for geometry_object in data_instance.polygon:
+        if geometry_object.data_type == geometry_polygon.DataPolygon.data_type:
             translation_matrix = get_translation_matrix(geometry_object)
             shape_shapely = []
-            outer_loop = get_outer_loop_as_shapely_points(geometry_object, translation_matrix)
+            outer_loop = get_outer_loop_as_shapely_points(
+                geometry_object, translation_matrix
+            )
             shape_shapely.append(outer_loop)
-            if(len(outer_loop) > 0):
-                inner_loops = get_inner_loops_as_shapely_points(geometry_object, translation_matrix)
-                if(len(inner_loops) > 0):
+            if len(outer_loop) > 0:
+                inner_loops = get_inner_loops_as_shapely_points(
+                    geometry_object, translation_matrix
+                )
+                if len(inner_loops) > 0:
                     for l in inner_loops:
                         shape_shapely.append(l)
             poly = build_shapely_polygon(shape_shapely)
             all_polygons.append(poly)
         else:
-            print('Not a polygon data instance!')
+            print("Not a polygon data instance: {}".format(geometry_object))
     return all_polygons
 
+
 # --------------- end generics ------------------
 
 #: List of available geometry (from revit to shapely ) converters
 GEOMETRY_CONVERTER = {
-    dr.DataRoom.dataType : get_shapely_polygons_from_data_instance,
-    dc.DataCeiling.dataType: get_shapely_polygons_from_data_instance
+    dr.DataRoom.data_type: get_shapely_polygons_from_data_instance,
+    dc.DataCeiling.data_type: get_shapely_polygons_from_data_instance,
 }
- 
+
+
 def get_shapely_polygons_from_geo_object(geometry_objects, data_type):
-    '''
+    """
     Converts polygon points from DataGeometry instances to shapely polygon instances and returns them as a dictionary where:
 
     - key is the geometry objects id
     - value is a list of shapely polygons
 
     :param geometry_objects: A list of instances of the the same type (i.e DataRoom)
     :type geometry_objects: list[data object]
     :param data_type: string human readable identifying the data type ( each Data... class has this as a static field: dr.DataRoom.dataType)
     :type data_type: str
 
     :return: A dictionary.
     :rtype: {int:[shapely.polygon]}
-    '''
+    """
 
     multi_polygons = {}
-    for i in range (len(geometry_objects)):
-        multi_polygons[geometry_objects[i].instanceProperties.instanceId] = []
+    for i in range(len(geometry_objects)):
+        multi_polygons[geometry_objects[i].instance_properties.id] = []
         poly = GEOMETRY_CONVERTER[data_type](geometry_objects[i])
         for p in poly:
-            if(p != None):
-                multi_polygons[geometry_objects[i].instanceProperties.instanceId].append(p)
-    return multi_polygons
+            if p != None:
+                multi_polygons[geometry_objects[i].instance_properties.id].append(p)
+    return multi_polygons
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/DataSamples/ProcessCeilingsToRooms.py` & `DuHast-0.0.7/src/duHast/Data/process_ceilings_to_rooms.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Sample showing how to find which ceilings are in which rooms.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 
 This module requires python >3.9 due to dependencies:
 
     - numpy
@@ -12,213 +12,257 @@
 
     - collects ceiling and room data instances by level ( assume a ceiling is always modelled as the room it is in )
     - converts room and ceiling outlines to shapely polygons
     - test for intersection of all ceilings on a given level with all rooms on a given level
     - stores any intersections found ( does a check how much area is  intersecting...if to small its assumed its not an intended intersection)
     - reports all rooms and any associated ceiling(s) found
 
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2022  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import codecs
 import csv
 
 
-from duHast.Utilities import Result as res
-from duHast.DataSamples import DataCeiling as dc
-from duHast.DataSamples import DataRoom as dr
-from duHast.DataSamples import DataReadFromFile as dReader
-from duHast.DataSamples import DataToShapely as dToS
+from duHast.Utilities.Objects import result as res
+from duHast.Data.Objects import data_ceiling as dc
+from duHast.Data.Objects import data_room as dr
+from duHast.Data.Utils import data_import as dReader
+from duHast.Data import data_to_shapely as dToS
 
 # --------------- writing out data ------------------
 
+
 def _read_data(file_path):
-    '''
+    """
     Reads text files into data objects within data reader class which is returned
 
     Data file to be json formatted. (one json entry per row)
 
     :param filePath: Fully qualified path to json formatted data file.
     :type filePath: str
 
     :return: A file data reader instance.
     :rtype: :class:`.ReadDataFromFile`
-    '''
+    """
 
     # read json file and convert into data objects
     dataReader = dReader.ReadDataFromFile(file_path)
     dataReader.load_data()
     return dataReader
 
+
 # --------------- writing out data ------------------
 
-def _write_report_data(file_name, header, data,):
-    '''
+
+def _write_report_data(
+    file_name,
+    header,
+    data,
+):
+    """
     Method writing out report information to csv file.
- 
+
     :param file_name: Fully qualified file path to data file.
     :type file_name: str
     :param header: List of column headers, provide empty list if not required!
     :type header: list[str]
     :param data: List of list of strings representing row data
     :type data: list[list[str]]
 
-    :return: 
+    :return:
         Result class instance.
 
         - result.status False if an exception occurred, otherwise True.
         - result.message will contain file name of file written.
         - result.result: empty list
-        
+
         On exception:
 
         - result.status (bool) will be False.
         - result.message will contain the exception message.
         - result.result: will be an empty list
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
     try:
         # open the file in the write mode
-        with codecs.open(file_name, 'w', encoding='utf-8') as f:
-         # create the csv writer
+        with codecs.open(file_name, "w", encoding="utf-8") as f:
+            # create the csv writer
             writer = csv.writer(f)
             # check header
-            if(len(header) > 0):
+            if len(header) > 0:
                 writer.writerow(header)
-            if(len(data) > 0):
+            if len(data) > 0:
                 for d in data:
                     # write a row to the csv file
                     writer.writerow(d)
             f.close()
-        return_value.UpdateSep(True, 'Successfully wrote data to: {}'.format(file_name))
-    except  Exception as e:
-        return_value.UpdateSep(False, 'Failed to write data to: {}'.format(file_name))
+        return_value.update_sep(
+            True, "Successfully wrote data to: {}".format(file_name)
+        )
+    except Exception as e:
+        return_value.update_sep(False, "Failed to write data to: {}".format(file_name))
     return return_value
 
+
 # --------------- data processing ------------------
 
-def _build_dictionary_by_level_and_data_type(dataReader):
-    '''
+
+def _build_dictionary_by_level_and_data_type(data_reader):
+    """
     Returns a dictionary where:
 
     - key: is the level name
     - values is a list of list of data objects
     -       first list room data objects
     -       second list ceilings data objects
 
-    :param dataReader: A data reader class instance
-    :type dataReader: :class:`.ReadDataFromFile`
+    :param data_reader: A data reader class instance
+    :type data_reader: :class:`.ReadDataFromFile`
 
     :return: A dictionary where key is the level name, value is a tuple of two lists: first one are rooms, second ones are ceiling data objects.
     :rtype: dic{str:[[:class:`.DataRoom],[:class:`.DataCeiling`]]}
-    '''
+    """
 
     dic = {}
-    for dObject in dataReader.data:
-        if(dObject.level.levelName not in dic):
-            roomsByLevel = dataReader.get_data_by_level_and_data_type(dObject.level.levelName, dr.DataRoom.dataType)
-            ceilingsByLevel = dataReader.get_data_by_level_and_data_type(dObject.level.levelName, dc.DataCeiling.dataType)
-            dic[dObject.level.levelName] = (roomsByLevel, ceilingsByLevel)
+    for d_object in data_reader.data:
+        if d_object.level.name not in dic:
+            rooms_by_level = data_reader.get_data_by_level_and_data_type(
+                d_object.level.name, dr.DataRoom.data_type
+            )
+            ceilings_by_level = data_reader.get_data_by_level_and_data_type(
+                d_object.level.name, dc.DataCeiling.data_type
+            )
+            dic[d_object.level.name] = (rooms_by_level, ceilings_by_level)
     return dic
 
+
 def _get_property_values_as_list(properties, property_keys):
-    '''
+    """
     _summary_
 
     :param properties: _description_
     :type properties: _type_
     :param property_keys: _description_
     :type property_keys: _type_
 
     :return: _description_
     :rtype: _type_
-    '''
+    """
 
     values = []
     for property_key in property_keys:
-        if(property_key in properties):
+        if property_key in properties:
             values.append(str(properties[property_key]))
         else:
-            values.append('null')
+            values.append("null")
     return values
 
-def _convert_object_data_into_report_data(dic_object, room_instance_property_keys, ceiling_type_property_keys, ceiling_instance_property_keys):
-    '''
+
+def _convert_object_data_into_report_data(
+    dic_object,
+    room_instance_property_keys,
+    ceiling_type_property_keys,
+    ceiling_instance_property_keys,
+):
+    """
     Converts a dictionary of DataRoom objects by level into list of lists of data entries per room so it can be written to file.
 
     :param dic_object:  A dictionary where key is the level name and values is a list of DataRoom instances.
     :type dic_object: {str:[:class: `.DataRoom`]}
 
     :return: List of list of strings representing room data
     :rtype: list of list [str]
-    '''
+    """
 
     data = []
     for levelName in dic_object:
         for room in dic_object[levelName][0]:
             # put fixed (always exported ) values first
-            dataRow = [
-                room.level.levelName,
-                room.revitModel.modelName,
-                str(room.instanceProperties.instanceId),
-                room.designSetAndOption.designSetName,
-                room.designSetAndOption.designOptionName,
-                str(room.designSetAndOption.isPrimary)
+            data_row = [
+                room.level.name,
+                room.revit_model.name,
+                str(room.instance_properties.id),
+                room.design_set_and_option.set_name,
+                room.design_set_and_option.option_name,
+                str(room.design_set_and_option.is_primary),
             ]
             # get custom values
-            dataRow = dataRow + _get_property_values_as_list(room.instanceProperties.properties, room_instance_property_keys)
-            
-            #data.append (dataRow)
+            data_row = data_row + _get_property_values_as_list(
+                room.instance_properties.properties, room_instance_property_keys
+            )
 
-            associatedDataRows = []
-            for associatedElement in room.associatedElements:
+            # data.append (data_row)
+
+            associated_data_rows = []
+            for associated_element in room.associated_elements:
                 # only add ceiling data for now
-                if(associatedElement.dataType == dc.DataCeiling.dataType):
-                    associatedDataRow = [
-                        associatedElement.level.levelName,
-                        room.revitModel.modelName,
-                        str(associatedElement.instanceProperties.instanceId),
-                        associatedElement.designSetAndOption.designSetName,
-                        associatedElement.designSetAndOption.designOptionName,
-                        str(associatedElement.designSetAndOption.isPrimary)
+                if associated_element.data_type == dc.DataCeiling.data_type:
+                    associated_data_row = [
+                        associated_element.level.name,
+                        room.revit_model.name,
+                        str(associated_element.instance_properties.id),
+                        associated_element.design_set_and_option.set_name,
+                        associated_element.design_set_and_option.option_name,
+                        str(associated_element.design_set_and_option.is_primary),
                     ]
-                    
-                    associatedDataRow = associatedDataRow + _get_property_values_as_list(associatedElement.typeProperties.properties, ceiling_type_property_keys)
-                    associatedDataRow = associatedDataRow + _get_property_values_as_list(associatedElement.instanceProperties.properties, ceiling_instance_property_keys)
-                    associatedDataRows.append(associatedDataRow)
-            
-                    data.append( dataRow + associatedDataRow )
+
+                    associated_data_row = (
+                        associated_data_row
+                        + _get_property_values_as_list(
+                            associated_element.type_properties.properties,
+                            ceiling_type_property_keys,
+                        )
+                    )
+                    associated_data_row = (
+                        associated_data_row
+                        + _get_property_values_as_list(
+                            associated_element.instance_properties.properties,
+                            ceiling_instance_property_keys,
+                        )
+                    )
+                    associated_data_rows.append(associated_data_row)
+
+                    data.append(data_row + associated_data_row)
     return data
 
-def _intersect_ceiling_vs_room(ceiling_poly_id, ceiling_polygon, room_poly_id, room_polygon, data_objects, level_name):
-    '''
+
+def _intersect_ceiling_vs_room(
+    ceiling_poly_id,
+    ceiling_polygon,
+    room_poly_id,
+    room_polygon,
+    data_objects,
+    level_name,
+):
+    """
     Does an intersection check of a ceiling polygon with a room polygon. If there is an intersection, the ceiling object will be added to the associated elements list of the room object.
 
     Note:
 
     - To avoid false positives: only ceiling which overlap a room by an area greater then 0.1 percent of the ceiling area will be considered as intersecting.
     - Manipulates the past in data_objects by reference!
 
@@ -231,74 +275,113 @@
     :param room_polygon: A polygon representing the room element.
     :type room_polygon: shapely.polygon
     :param data_objects: A dictionary where key is the level name, value is a tuple of two lists: first one are rooms, second ones are ceiling data objects.
     :type data_objects: [str:([:class:`.DataRoom`],[:class:`.DataCeiling`])]
     :type  level_name: The level name where room and ceiling are on.
     :param room_polygon: str
 
-    :return: 
+    :return:
         Result class instance.
 
         - result.status False if an exception occurred, otherwise True.
         - result.message will contain processing messages.
         - result.result: empty list
-        
+
         On exception:
 
         - result.status (bool) will be False.
         - result.message will contain the exception message.
         - result.result will be an empty list
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
     # add some exception handling here in case intersect check throws an error
     try:
         # check what exactly is happening
-        if(ceiling_polygon.intersects(room_polygon)):
+        if ceiling_polygon.intersects(room_polygon):
             # calculates percentage of overlapping ceiling area vs room area
             # anything less then 0.1 will be ignored...
-            area_intersection_percentage_of_ceiling_vs_room = (ceiling_polygon.intersection(room_polygon).area/room_polygon.area)*100
+            area_intersection_percentage_of_ceiling_vs_room = (
+                ceiling_polygon.intersection(room_polygon).area / room_polygon.area
+            ) * 100
             # check what percentage the overlap area is...if less then 0.1 percent ignore!
-            if(area_intersection_percentage_of_ceiling_vs_room < 0.1):
+            if area_intersection_percentage_of_ceiling_vs_room < 0.1:
                 # ceiling overlap area is to small...not in room
-                return_value.AppendMessage('Ceiling {} has an overlap of {} % with  room {}. Ignored!'.format(ceiling_poly_id, area_intersection_percentage_of_ceiling_vs_room, room_poly_id, ))
+                return_value.append_message(
+                    "Ceiling {} has an overlap of {} % with  room {}. Ignored!".format(
+                        ceiling_poly_id,
+                        area_intersection_percentage_of_ceiling_vs_room,
+                        room_poly_id,
+                    )
+                )
             else:
                 # ceiling is within the room: add to room data object
                 # get the room object by its Revit ID
-                data_object_room =  list(filter(lambda x: (x.instanceProperties.instanceId == room_poly_id ) , data_objects[level_name][0]))[0]
+                data_object_room = list(
+                    filter(
+                        lambda x: (x.instance_properties.id == room_poly_id),
+                        data_objects[level_name][0],
+                    )
+                )[0]
                 # get the ceiling object by its Revit id
-                data_object_Ceiling =  list(filter(lambda x: (x.instanceProperties.instanceId == ceiling_poly_id ) , data_objects[level_name][1]))[0]
-                # add ceiling object to associated elements list of room object 
-                data_object_room.associatedElements.append(data_object_Ceiling)
-                return_value.AppendMessage('Added ceiling {} to room {}'.format(room_poly_id, ceiling_poly_id))
+                data_object__ceiling = list(
+                    filter(
+                        lambda x: (x.instance_properties.id == ceiling_poly_id),
+                        data_objects[level_name][1],
+                    )
+                )[0]
+                # add ceiling object to associated elements list of room object
+                data_object_room.associated_elements.append(data_object__ceiling)
+                return_value.append_message(
+                    "Added ceiling {} to room {}".format(room_poly_id, ceiling_poly_id)
+                )
     except Exception as e:
         # get the offending elements:
-        data_object_room =  list(filter(lambda x: (x.instanceProperties.instanceId == room_poly_id ) , data_objects[level_name][0]))[0]
-        data_object_Ceiling =  list(filter(lambda x: (x.instanceProperties.instanceId == ceiling_poly_id ) , data_objects[level_name][1]))[0]
-        return_value.AppendMessage(
-            'Exception: {} \n' +
-            'offending room: room name: {} , room number: {} , room id: {} , is valid polygon: {}\n' +
-            'offending ceiling id: {} , is valid polygon: {}').format(
-                e.message, 
-                data_object_room.instanceProperties.properties['Name'],
-                data_object_room.instanceProperties.properties['Number'],
-                data_object_room.instanceProperties.instanceId,
-                room_polygon.is_valid,
-                data_object_Ceiling.instanceProperties.instanceId,
-                ceiling_polygon.is_valid
-                )
+        data_object_room = list(
+            filter(
+                lambda x: (x.instance_properties.id == room_poly_id),
+                data_objects[level_name][0],
+            )
+        )[0]
+        data_object__ceiling = list(
+            filter(
+                lambda x: (x.instance_properties.id == ceiling_poly_id),
+                data_objects[level_name][1],
+            )
+        )[0]
+        return_value.append_message(
+            "Exception: {} \n"
+            + "offending room: room name: {} , room number: {} , room id: {} , is valid polygon: {}\n"
+            + "offending ceiling id: {} , is valid polygon: {}"
+        ).format(
+            e.message,
+            data_object_room.instance_properties.properties["Name"],
+            data_object_room.instance_properties.properties["Number"],
+            data_object_room.instance_properties.id,
+            room_polygon.is_valid,
+            data_object__ceiling.instance_properties.id,
+            ceiling_polygon.is_valid,
+        )
     return return_value
 
+
 # --------------- main functions ------------------
 
-def write_data_to_file(data, output_file_path, room_instance_property_keys= ['Number', 'Name'], ceiling_type_property_keys = ['Type Mark'], ceiling_instance_property_keys =['Height Offset From Level'] ):
-    '''
-    Writes Room data to file. 
+
+def write_data_to_file(
+    data,
+    output_file_path,
+    room_instance_property_keys=["Number", "Name"],
+    ceiling_type_property_keys=["Type Mark"],
+    ceiling_instance_property_keys=["Height Offset From Level"],
+):
+    """
+    Writes Room data to file.
 
     Note:
 
     - Room data consists of fixed (always reported) instance properties and custom instance properties defined in room_instance_property_keys
     - Ceiling data consists of fixed (always reported) instance properties, custom type properties defined in ceiling_type_property_keys and custom instance properties defined in ceiling_instance_property_keys
     - the report contains a row per associated element per room ( if 2 ceilings are in a room, the report will contain 2 rows)
 
@@ -309,124 +392,167 @@
     :param room_instance_property_keys: Names of room instance properties to be reported, defaults to ['Number', 'Name']
     :type room_instance_property_keys: list, optional
     :param ceiling_type_property_keys: Names of ceiling type properties to be reported, defaults to ['Type Mark']
     :type ceiling_type_property_keys: list, optional
     :param ceiling_instance_property_keys: Names of ceiling instance properties to be reported, defaults to ['Height Offset From Level']
     :type ceiling_instance_property_keys: list, optional
 
-    :return: 
+    :return:
         Result class instance.
 
         - Export status returned in result.status. False if an exception occurred, otherwise True.
         - result.message will contain the processing messages.
         - result.result will be an empty list
-        
+
         On exception:
 
         - result.status (bool) will be False.
         - result.message will contain the exception message.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
     try:
-        converted_data =  _convert_object_data_into_report_data(
+        converted_data = _convert_object_data_into_report_data(
             data,
             room_instance_property_keys,
             ceiling_type_property_keys,
-            ceiling_instance_property_keys)
-    
+            ceiling_instance_property_keys,
+        )
+
         # create header for report file
         # rooms always written values first
-        data_header = ['room level name', 'room model name', 'room revit id','room design set name','room design option name', 'room design option is primary']
+        data_header = [
+            "room level name",
+            "room model name",
+            "room revit id",
+            "room design set name",
+            "room design option name",
+            "room design option is primary",
+        ]
         # rooms custom data next
         data_header = data_header + room_instance_property_keys
         # ceilings always written values first
-        data_header = data_header + ['ceiling level name', 'ceiling model name','ceiling revit id','ceiling design set name','ceiling design option name', 'ceiling design option is primary']
+        data_header = data_header + [
+            "ceiling level name",
+            "ceiling model name",
+            "ceiling revit id",
+            "ceiling design set name",
+            "ceiling design option name",
+            "ceiling design option is primary",
+        ]
         # ceilings custom data next
-        data_header = data_header + ceiling_type_property_keys + ceiling_instance_property_keys
+        data_header = (
+            data_header + ceiling_type_property_keys + ceiling_instance_property_keys
+        )
         # write data to file
-        return_value.Update(_write_report_data(output_file_path, data_header, converted_data))
+        return_value.update(
+            _write_report_data(output_file_path, data_header, converted_data)
+        )
 
     except Exception as e:
-        return_value.UpdateSep(False, 'Failed to write report with exception {}'.format(e))
+        return_value.update_sep(
+            False, "Failed to write report with exception {}".format(e)
+        )
     return return_value
 
+
 def get_ceilings_by_room(data_source_path):
-    '''
+    """
     Reads Revit data from file and runs an intersection check of each ceiling on a level with each room on the same level.
 
     Note:
     DataRoom instance will contain any ceilings in that room in associated elements property.
 
     :param data_source_path: Fully qualified file path to json formatted file containing DataRoom and DataCeiling objects.
     :type data_source_path: str
 
-    :return: 
+    :return:
         Result class instance.
 
         - result.status False if an exception occurred, otherwise True.
         - result.message will contain processing messages.
         - result.result A dictionary where key is the level name, value is a tuple of two lists: first one are rooms, second ones are ceiling data objects.
-        
+
         On exception:
 
         - result.status (bool) will be False.
         - result.message will contain the exception message.
         - result.result will be an empty list
 
     :rtype: :class:`.Result`
-    '''
+    """
 
     return_value = res.Result()
     # read exported ceiling and room data from file
     data_reader = _read_data(data_source_path)
     # check if read returned anything
-    if(len(data_reader.data) > 0):
+    if len(data_reader.data) > 0:
         # build dictionary of objects by level and object type
         data_objects = _build_dictionary_by_level_and_data_type(data_reader)
         # key level name, value tuple ( rooms [index 0] and ceilings [index 1])
         # loop over dic and process each key (level):
         #       - check if rooms and ceilings
         #       - intersection check
         #       - update room object with ceiling match
+        # print(data_objects)
         for level_name in data_objects:
             # check rooms are on this level
-            if(len(data_objects[level_name][0]) > 0):
+            if len(data_objects[level_name][0]) > 0:
                 # check ceilings are on this level
-                if(len(data_objects[level_name][1]) > 0):
+                if len(data_objects[level_name][1]) > 0:
                     polygons_by_type = {}
                     # convert geometry data off all rooms and ceilings into dictionaries : key is Revit element id, values are shapely polygons
-                    room_polygons = dToS.get_shapely_polygons_from_geo_object(data_objects[level_name][0], dr.DataRoom.dataType)
-                    ceiling_polygons = dToS.get_shapely_polygons_from_geo_object(data_objects[level_name][1], dc.DataCeiling.dataType)
-                    polygons_by_type[dr.DataRoom.dataType] = room_polygons
-                    polygons_by_type[dc.DataCeiling.dataType] = ceiling_polygons
+                    room_polygons = dToS.get_shapely_polygons_from_geo_object(
+                        data_objects[level_name][0], dr.DataRoom.data_type
+                    )
+                    ceiling_polygons = dToS.get_shapely_polygons_from_geo_object(
+                        data_objects[level_name][1], dc.DataCeiling.data_type
+                    )
+                    polygons_by_type[dr.DataRoom.data_type] = room_polygons
+                    polygons_by_type[dc.DataCeiling.data_type] = ceiling_polygons
                     # loop over rooms ids and find intersecting ceilings
-                    for room_poly_id in polygons_by_type[dr.DataRoom.dataType]:
+                    for room_poly_id in polygons_by_type[dr.DataRoom.data_type]:
                         # check if valid room poly ( just in case that is a room in schedule only >> not placed in model , or unbound, or overlapping with other room)
-                        if(len(room_polygons[room_poly_id]) > 0):
+                        if len(room_polygons[room_poly_id]) > 0:
                             # loop over each room polygon per room...there should only be one...
                             for room_polygon in room_polygons[room_poly_id]:
                                 # find overlapping ceiling polygons
-                                for ceiling_poly_id in polygons_by_type[dc.DataCeiling.dataType]:
-                                    for ceiling_polygon in ceiling_polygons[ceiling_poly_id]:
-                                        return_value.Update(   
+                                for ceiling_poly_id in polygons_by_type[
+                                    dc.DataCeiling.data_type
+                                ]:
+                                    for ceiling_polygon in ceiling_polygons[
+                                        ceiling_poly_id
+                                    ]:
+                                        return_value.update(
                                             _intersect_ceiling_vs_room(
-                                                ceiling_poly_id, 
-                                                ceiling_polygon, 
-                                                room_poly_id, 
-                                                room_polygon, 
-                                                data_objects, 
-                                                level_name
-                                                )
+                                                ceiling_poly_id,
+                                                ceiling_polygon,
+                                                room_poly_id,
+                                                room_polygon,
+                                                data_objects,
+                                                level_name,
                                             )
+                                        )
                         else:
-                            return_value.AppendMessage('Room with id {} has no valid room poly lines.'.format(room_poly_id))
+                            return_value.append_message(
+                                "Room with id {} has no valid room poly lines.".format(
+                                    room_poly_id
+                                )
+                            )
                 else:
-                    return_value.AppendMessage('No ceilings found for level: {}'.format(data_objects[level_name][0][0].level.levelName))
+                    return_value.append_message(
+                        "No ceilings found for level: {}".format(
+                            data_objects[level_name][0][0].level.name
+                        )
+                    )
             else:
-                return_value.AppendMessage('No rooms found for level: {}'.format(data_objects[level_name]))
+                return_value.append_message(
+                    "No rooms found for level: {}".format(data_objects[level_name])
+                )
         return_value.result = data_objects
     else:
-        return_value.UpdateSep(False, 'File: {} did not contain any valid data.'.format(data_source_path))
-    return return_value
+        return_value.update_sep(
+            False, "File: {} did not contain any valid data.".format(data_source_path)
+        )
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/UI/FileList.py` & `DuHast-0.0.7/src/duHast/UI/file_list.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,17 +1,17 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Helper functions for the file selection GUI.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 
 #!/usr/bin/python
 # -*- coding: utf-8 -*-
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
 # Copyright (c) 2021  Jan Christel
 #
 # This program is free software: you can redistribute it and/or modify
@@ -33,246 +33,270 @@
 
 import clr
 import System
 import os
 
 
 # import file item class
-from duHast.UI import FileItem as fi
+from duHast.UI import file_item as fi
+
 # import workloader utils
-from duHast.UI import Workloader as wl
+from duHast.UI import workloader as wl
 
 # custom result class
-from duHast.Utilities import Result as res
+from duHast.Utilities.Objects import result as res
 
 # -------------
 # my code here:
 # -------------
 
-def getRevitFiles(directory, fileExtension):
-    '''
+
+def get_revit_files(directory, file_extension):
+    """
     Returns files in a given directory and of a given file extension.
 
     :param directory: The fully qualified directory path.
     :type directory: str
-    :param fileExtension: The file extension filter in format '.ext'
-    :type fileExtension: str
+    :param file_extension: The file extension filter in format '.ext'
+    :type file_extension: str
 
     :return: List of file items
     :rtype: [:class:`.FileItem`]
-    '''
+    """
 
     files = []
-    listOfFiles = os.listdir(directory)
-    for f in listOfFiles:
+    list_of_files = os.listdir(directory)
+    for f in list_of_files:
         # check for file extension match
-        if(f.lower().endswith(fileExtension.lower())):
-            # check if this is a back up file, remove the file extension
-            filePath = f[:-len(fileExtension)]
-            if(isBackUpFile(filePath) == False):
+        if f.lower().endswith(file_extension.lower()):
+            # check if this is a back up file
+            if is_back_up_file(f) == False:
                 # Use join to get full file path.
                 location = os.path.join(directory, f)
                 # Get size and add to list of files.
                 size = os.path.getsize(location)
-                files.append(fi.MyFileItem(location,size))
+                files.append(fi.MyFileItem(location, size))
     return files
 
-def getRevitFilesInclSubDirs(directory, fileExtension):
-    '''
+
+def get_revit_files_incl_sub_dirs(directory, file_extension):
+    """
     Returns files in a given directory and its sub directories of a given file extension.
 
     :param directory: The fully qualified directory path.
     :type directory: str
-    :param fileExtension: The file extension filter in format '.ext'
-    :type fileExtension: str
+    :param file_extension: The file extension filter in format '.ext'
+    :type file_extension: str
 
     :return: List of file items
     :rtype: [:class:`.FileItem`]
-    '''
+    """
 
     files = []
     # Get the list of all files in directory tree at given path
-    listOfFiles = list()
+    list_of_files = list()
     for (dirpath, dirnames, filenames) in os.walk(directory):
-        listOfFiles += [os.path.join(dirpath, file) for file in filenames]
-    for f in listOfFiles:
+        list_of_files += [os.path.join(dirpath, file) for file in filenames]
+    for f in list_of_files:
         # check for file extension match
-        if(f.lower().endswith(fileExtension.lower())):
-            # check if this is a back up file, remove the file extension
-            filePath = f[:-len(fileExtension)]
-            if(isBackUpFile(filePath) == False):
+        if f.lower().endswith(file_extension.lower()):
+            # check if this is a back up file,
+            if is_back_up_file(f) == False:
                 # Get size and add to list of files.
                 size = os.path.getsize(f)
-                files.append(fi.MyFileItem(f,size))
+                files.append(fi.MyFileItem(f, size))
     return files
 
-def isBackUpFile(filePath):
-    '''
+
+def is_back_up_file(file_path):
+    """
     Checks whether a file is a Revit back up file.
-    
+
     Backup files are usually in format 'filename.01234.ext'
-    
+
     Method of checking:
 
     - splitting file name at every full stop
     - check whether a list with more more then 2 entries came back ?
-    
-        - no: 
+
+        - no:
             - not a back up
-        - yes: 
+        - yes:
             - check last list entry whether it is 4 characters in length and can it be convert it into an integer?
-        
-                - yes: 
+
+                - yes:
                     - backup file
                 - no
                     - normal file
-    
-    :param filePath: A fully qualified file path.
-    :type filePath: str
+
+    :param file_path: A fully qualified file path.
+    :type file_path: str
 
     :return: True if a back up file, otherwise False.
     :rtype: bool
-    '''
+    """
 
-    isBackup = False
-    chunks = filePath.split('.')
-    if(len(chunks)>2):
-        lastChunk = chunks[len(chunks)-2]
+    is_backup = False
+    chunks = file_path.split(".")
+    if len(chunks) > 2:
+        last_chunk = chunks[len(chunks) - 2]
         try:
-            converted_num = int(lastChunk)
-            isBackup = True
+            converted_num = int(last_chunk)
+            is_backup = True
         except Exception:
             pass
-    return isBackup
+    return is_backup
+
 
-def getFileSize(item):
-    '''
+def get_file_size(item):
+    """
     Helper used to define workload size (same as file size)
 
     :param item: A file item object instance.
     :type item: :class:`.FileItem`
 
     :return: The file size.
     :rtype: int
-    '''
+    """
 
     return item.size
 
-def BucketToTaskListFileSystem(item):
-    '''
+
+def bucket_to_task_list_file_system(item):
+    """
     Default task list content for files on a file server location.
 
     :param item: A file item object instance.
     :type item: :class:`.FileItem`
 
     :return: The item name.(fully qualified file path)
     :rtype: str
-    '''
+    """
 
     return item.name
 
-def BucketToTaskListBIM360(item):
-    '''
+
+def bucket_to_task_list_bim_360(item):
+    """
     Default task list content for files on a BIM 360 cloud drive.
 
     :param item: A file item object instance.
     :type item: :class:`.FileItem`
 
     :return: The revit version, project guid, file guid separated by a space ' '
     :rtype: str
-    '''
+    """
+
+    return " ".join(
+        [item.bim_360_revit_version, item.bim_360_project_guid, item.bim_360_file_guid]
+    )
 
-    return ' '.join([item.BIM360RevitVersion, item.BIM360ProjectGUID, item.BIM360FileGUID])
 
-def writeRevitTaskFile(fileName, bucket, GetData = BucketToTaskListFileSystem):
-    '''
+def write_revit_task_file(file_name, bucket, get_data=bucket_to_task_list_file_system):
+    """
     Writes out a task list file.
 
-    :param fileName: Fully qualified file path of the task file name including extension.
-    :type fileName: str
+    :param file_name: Fully qualified file path of the task file name including extension.
+    :type file_name: str
     :param bucket: Workload bucket object instance.
     :type bucket: :class:`.WorkloadBucket`
-    :param GetData: Returns data from file item object to be written to file, defaults to BucketToTaskListFileSystem
-    :type GetData: func(:class:`.FileItem`) -> str, optional
+    :param get_data: Returns data from file item object to be written to file, defaults to BucketToTaskListFileSystem
+    :type get_data: func(:class:`.FileItem`) -> str, optional
 
-    :return: 
+    :return:
         Result class instance.
 
         - Write file status (bool) returned in result.status. False if an exception occurred, otherwise True.
         - Result.message property contains fully qualified file path to task list file.
-        
+
         On exception:
-        
+
         - .status (bool) will be False.
         - .message will contain the exception message.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
+    return_value = res.Result()
     try:
-        f = open(fileName, 'w')
-        rowCounter = 0
+        f = open(file_name, "w")
+        row_counter = 0
         for p in bucket.items:
-            data = GetData(p)
+            data = get_data(p)
             # check whether first row
-            if(rowCounter != 0):
+            if row_counter != 0:
                 # if not first row add line feed character before data written
-                data = '\n' + data
+                data = "\n" + data
             else:
-                rowCounter += 1
-            f.write(data.encode('utf-8'))
+                row_counter += 1
+            # this looks horrible: but:
+            # string.encode('utf-8') returns a byte string b''
+            # so it needs to be converted to an actual string again
+            f.write(data.encode("utf-8").decode("utf-8"))
         f.close()
-        returnValue.AppendMessage('wrote task list: ' + fileName + ' [TRUE]')
+        return_value.append_message("wrote task list: {} [TRUE]".format(file_name))
     except Exception as e:
-        returnValue.UpdateSep(False, 'Failed to write task list: ' + fileName + ' with exception ' + str(e))
-    return returnValue
-
-def WriteFileList(directoryPath, fileExtension, taskListDirectory, taskFilesNumber, fileGetter, fileDataProcessor = BucketToTaskListFileSystem):
-    '''
+        return_value.update_sep(
+            False,
+            "Failed to write task list: {} with exception {}".format(file_name, e),
+        )
+    return return_value
+
+
+def write_file_list(
+    directory_path,
+    file_extension,
+    task_list_directory,
+    task_files_number,
+    file_getter,
+    file_data_processor=bucket_to_task_list_file_system,
+):
+    """
     Writes out all task list(s) to file(s).
 
-    :param directoryPath: Fully qualified directory path containing files to be added to task lists.
-    :type directoryPath: str
-    :param fileExtension: A file extension filter in format '.ext'
-    :type fileExtension: str
-    :param taskListDirectory: The fully qualified directory path where the task files will be written .
-    :type taskListDirectory: str
-    :param taskFilesNumber: The number of task files to be written.
-    :type taskFilesNumber: int
-    :param fileGetter: Function accepting a directory and file extension filter and returns file items from directory.
-    :type fileGetter: func(str, str) -> :class:`.FileItem`
-    :param fileDataProcessor: Function processing file item and returns a string to be written to task list file, defaults to BucketToTaskListFileSystem
-    :type fileDataProcessor: func(:class:`.FileItem`) -> str, optional
-    
-    :return: 
+    :param directory_path: Fully qualified directory path containing files to be added to task lists.
+    :type directory_path: str
+    :param file_extension: A file extension filter in format '.ext'
+    :type file_extension: str
+    :param task_list_directory: The fully qualified directory path where the task files will be written .
+    :type task_list_directory: str
+    :param task_files_number: The number of task files to be written.
+    :type task_files_number: int
+    :param file_getter: Function accepting a directory and file extension filter and returns file items from directory.
+    :type file_getter: func(str, str) -> :class:`.FileItem`
+    :param file_data_processor: Function processing file item and returns a string to be written to task list file, defaults to BucketToTaskListFileSystem
+    :type file_data_processor: func(:class:`.FileItem`) -> str, optional
+
+    :return:
         Result class instance.
 
         - Write file status (bool) returned in result.status. False if an exception occurred, otherwise True.
         - Result.message property contains fully qualified file path for each task list file.
-        
+
         On exception:
-        
+
         - .status (bool) will be False.
         - .message will contain the exception message.
 
     :rtype: :class:`.Result`
-    '''
+    """
 
-    returnValue = res.Result()
-    returnValue.status = True
+    return_value = res.Result()
+    return_value.status = True
     # get revit files in input dir
-    revitFiles = fileGetter(directoryPath, fileExtension)
+    revit_files = file_getter(directory_path, file_extension)
     # build bucket list
-    buckets = wl.DistributeWorkload(taskFilesNumber, revitFiles, getFileSize)
+    buckets = wl.distribute_workload(task_files_number, revit_files, get_file_size)
     try:
         # write out file lists
         counter = 0
         for bucket in buckets:
-            fileName =  os.path.join(taskListDirectory, 'Tasklist_' + str(counter)+ '.txt')
-            statusWrite = writeRevitTaskFile(fileName, bucket, fileDataProcessor)
-            returnValue.Update(statusWrite)
+            file_name = os.path.join(
+                task_list_directory, "Tasklist_" + str(counter) + ".txt"
+            )
+            status_write = write_revit_task_file(file_name, bucket, file_data_processor)
+            return_value.update(status_write)
             counter += 1
-        returnValue.AppendMessage('Finished writing out task files')
+        return_value.append_message("Finished writing out task files")
     except Exception as e:
-        returnValue.UpdateSep(False, 'Failed to save file list! '  + str(e))
-    return returnValue
+        return_value.update_sep(False, "Failed to save file list! " + str(e))
+    return return_value
```

### Comparing `DuHast-0.0.6/src/duHast/UI/UIFileSelect.py` & `DuHast-0.0.7/src/duHast/UI/ui_file_select.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,127 +1,128 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 A file selection GUI.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2020  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 import clr
-clr.AddReference('System.Windows.Forms')
-clr.AddReference('IronPython.Wpf')
+
+clr.AddReference("System.Windows.Forms")
+clr.AddReference("IronPython.Wpf")
 
 # import WPF creator and base window
 import wpf
 from System import Windows
 import ctypes
 
 # import settings class
-#from duHast.UI import FileSelectSettings as set
-
+# from duHast.UI import FileSelectSettings as set
 def Mbox(title, text, style):
-    '''
+    """
     A simple win forms message box.
 
     :param title: The title of the message box.
     :type title: str
     :param text: The text displayed in the message box.
     :type text: str
     :param style: An int representing the type of buttons shown.
         (https://docs.microsoft.com/en-us/dotnet/api/system.windows.forms.messageboxbuttons?view=windowsdesktop-6.0)
     :type style: int
 
     :return: A win form message box.
     :rtype: _type_
-    '''
+    """
 
     return ctypes.windll.user32.MessageBoxW(0, text, title, style)
 
+
 # UI class
-class MyWindow (Windows.Window):
-    def __init__(self, xamlFullFileName, revitFiles, settings):
-        '''
+class MyWindow(Windows.Window):
+    def __init__(self, xaml_full_file_name, revitFiles, settings):
+        """
         Class constructor
 
-        :param xamlFullFileName: Fully qualified file path to wpf XAML file.
-        :type xamlFullFileName: str
+        :param xaml_full_file_name: Fully qualified file path to wpf XAML file.
+        :type xaml_full_file_name: str
         :param revitFiles: List containing path to files.
         :type revitFiles: [str]
         :param settings: A settings object.
         :type settings: :class:`.FileSelectionSettings`
-        '''
-        
-        wpf.LoadComponent(self,xamlFullFileName)
+        """
+
+        wpf.LoadComponent(self, xaml_full_file_name)
 
         # populate fields
         self.selectedFiles = []
         self.revitfiles = revitFiles
         self.files.ItemsSource = revitFiles
-        self.tbSourceFolder.Text = settings.inputDir
-        self.tbDestinationFolder.Text = settings.outputDir
-        self.tbFileType.Text = settings.revitFileExtension
-        self.tbNoOfFiles.Text = str(settings.outputFileNum)
-        self.cbInclSubDirs.IsChecked = settings.inclSubDirs
-        
+        self.tbSourceFolder.Text = settings.input_directory
+        self.tbDestinationFolder.Text = settings.output_dir
+        self.tbFileType.Text = settings.revit_file_extension
+        self.tbNoOfFiles.Text = str(settings.output_file_num)
+        self.cbInclSubDirs.IsChecked = settings.incl_sub_dirs
+
     def BtnOK(self, sender, EventArgs):
-        '''
+        """
         Ok button event handler.
 
         Gets the selected rows of files and adds them to .selectedFiles property
         Sets the dialog result value to True.
 
         :param sender: _description_
         :type sender: _type_
         :param EventArgs: _description_
         :type EventArgs: _type_
-        '''
+        """
 
         # get selected items
         rows = self.files.SelectedItems
-        if(rows != None and len(rows) > 0):
+        if rows != None and len(rows) > 0:
             self.selectedFiles = []
             for row in rows:
                 # get the original file element
-                for oRev in self.revitfiles:
-                    if(oRev.name == row.name):
-                        self.selectedFiles.append(oRev)
+                for o_rev in self.revitfiles:
+                    if o_rev.name == row.name:
+                        self.selectedFiles.append(o_rev)
                         break
             # Mbox('ok',str(len(self.selectedFiles)), 1)
             self.DialogResult = True
             self.Close()
         else:
-            Mbox('Attention','No files selected', 1)
-    
+            Mbox("Attention", "No files selected", 1)
+
     def BtnCancel(self, sender, EventArgs):
-        '''
+        """
         Cancel button event handler.
         Sets the dialogue result value to False.
 
         :param sender: _description_
         :type sender: _type_
         :param EventArgs: _description_
         :type EventArgs: _type_
-        '''
-        
-        #print('cancel')
+        """
+
+        # print('cancel')
         self.DialogResult = False
-        self.Close()
+        self.Close()
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/Utilities/BatchProcessorLogUtils.py` & `DuHast-0.0.7/src/duHast/Utilities/batch_processor_log_utils.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,52 +1,52 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Helper functions to process Revit BatchProcessor log files.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+"""
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2020  Jan Christel
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
+#
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
-#
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
-#
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
 # collection of tools used to process batch processor log files
 
 # todo:
 # write out current process IDs (empty text file with process id as file name)
 #       script_util.GetSessionId()
 # read out process ID from text file and find matching log files
 # process log file:
 #   - find files processed:
 #            11/12/2020 18:01:40 : Processing Revit file (1 of 1) in Revit 2020 session.
-#            11/12/2020 18:01:40 : 
+#            11/12/2020 18:01:40 :
 #            11/12/2020 18:01:40 : 	P:\something\FileName.rvt
 #            ....
 #            25/11/2020 09:37:34 : 	- Operation completed.
 #   - check whether an exception occurred when processing any of the above files:
-#       - file(s) not found 
+#       - file(s) not found
 #           "WARNING: The following Revit Files do not exist"
-#       - .net exception 
+#       - .net exception
 #           "ERROR: An error occurred while executing the task script!"
 #       - timed out occurred and revit process got killed
 #           "WARNING: Timed-out"
 #   - delete process id pointer file
 #   - show user processing results (only when something went wrong(?))
 
 import clr
@@ -54,384 +54,436 @@
 from System.IO import Path
 import glob
 import time
 import os
 import json
 
 # custom result class from common library
-from duHast.Utilities import Result as res
+from duHast.Utilities.Objects import result as res
+
 # library from common library
-from duHast.Utilities import Utility as util
+from duHast.Utilities import files_io as fileIO, files_get as fileGet
 
 #: global variable controlling debug output
-debugMode_ = False
+debug_mode_ = False
 
 #: Message snippets which indicate processing of a file went bad
 EXCEPTION_MESSAGES = [
-    'ERROR: An error occurred while executing the task script! Operation', # revit batch p message when script is buggy
-    'WARNING: Timed-out', # revit batch p message when revit times out
-    'Exception: [Exception]', # Revit Batch P message when an exception occurs
-    '\t- \tMessage: An unrecoverable error has occurred.  The program will now be terminated.', # Revit message when it crashes out
-    'Script Exception:' # custom script message...something the script was meant to do failed
+    "ERROR: An error occurred while executing the task script! Operation",  # revit batch p message when script is buggy
+    "WARNING: Timed-out",  # revit batch p message when revit times out
+    "Exception: [Exception]",  # Revit Batch P message when an exception occurs
+    "\t- \tMessage: An unrecoverable error has occurred.  The program will now be terminated.",  # Revit message when it crashes out
+    "Script Exception:",  # custom script message...something the script was meant to do failed
 ]
 
 # output...
-def Output(message = ''):
-    if debugMode_:
-        print (message)
-        
-def AdjustSessionIdForFileName(id):
-    '''
+def output(message=""):
+    if debug_mode_:
+        print(message)
+
+
+def delete_log_data_files(directory_path):
+    """
+    Deletes all log marker files in a directory.
+
+    :param directory_path: The directory path containing marker files to be deleted.
+    :type directory_path: str
+
+    :return: True if all files where deleted successfully, otherwise False.
+    :rtype: bool
+    """
+
+    status = True
+    # get files in directory
+    files_to_delete = fileGet.get_files_with_filter(directory_path, ".txt")
+    if len(files_to_delete) > 0:
+        status_delete = True
+        for file in files_to_delete:
+            status_delete = status_delete and fileIO.file_delete(file)
+    return status
+
+
+def adjust_session_id_for_file_name(id):
+    """
     Removes chevrons and replace colons with underscores in session id supplied by revit batch processor so it\
         can be used in a file name.
 
     :param id: Session id supplied by revit batch processor.
     :type id: str
 
     :return: Re-formatted session id.
     :rtype: str
-    '''
+    """
 
     # remove colons
-    sessionIdChanged = id.replace(':','_')
+    session_id_changed = id.replace(":", "_")
     # remove chevrons
-    sessionIdChanged = sessionIdChanged[1:-1]
-    return sessionIdChanged
+    session_id_changed = session_id_changed[1:-1]
+    return session_id_changed
+
 
-def AdjustSessionIdFileNameBack(fileNameId):
-    '''
+def adjust_session_id_file_name_back(file_name_id):
+    """
     Re-introduces chevrons and replaces underscores with colons to match session Id format used in batch processor to a\
         file name using a batch processor supplied id.
 
-    :param fileNameId: A file name containing a session id with all illegal characters replaced.
-    :type fileNameId: str
+    :param file_name_id: A file name containing a session id with all illegal characters replaced.
+    :type file_name_id: str
 
     :return: A session id.
     :rtype: str
-    '''
+    """
 
     # re-instate colons
-    sessionIdChanged = fileNameId.replace('_',':')
+    session_id_changed = file_name_id.replace("_", ":")
     # remove chevrons
-    sessionIdChanged = '<' + sessionIdChanged + '>'
-    return sessionIdChanged
+    session_id_changed = "<" + session_id_changed + ">"
+    return session_id_changed
+
+
+def write_session_id_marker_file(folder_path, session_id):
+    """
+    Writes out an empty marker file in given directory.
 
-def WriteSessionIdMarkerFile(folderPath, sessionId):
-    '''
-    Writes out an empty marker file in given directory. 
-    
     - File is of type .txt
-    - File name is the batch processor sessionId used to identify the log file belonging to this process.
+    - File name is the batch processor session_id used to identify the log file belonging to this process.
 
-    :param folderPath: Directory of where the file will be written to.
-    :type folderPath: str
-    :param sessionId: Session id supplied by revit batch processor.
-    :type sessionId: str
+    :param folder_path: Directory of where the file will be written to.
+    :type folder_path: str
+    :param session_id: Session id supplied by revit batch processor.
+    :type session_id: str
 
     :return: True if marker file was written successfully, otherwise False.
     :rtype: bool
-    '''
+    """
 
-    fileName = os.path.join(folderPath, str(sessionId)+'.txt')
+    file_name = os.path.join(folder_path, str(session_id) + ".txt")
     status = True
     try:
-        f = open(fileName, "w")
+        f = open(file_name, "w")
         f.close()
     except:
         status = False
     return status
 
-def GetCurrentSessionIds(folderPath):
-    '''
+
+def get_current_session_ids(folder_path):
+    """
     Returns file names of all text files in a given directory representing session Ids.
 
     Files will be deleted immediately after reading
 
-    :param folderPath: Directory of where test files are located
-    :type folderPath: str
+    :param folder_path: Directory of where test files are located
+    :type folder_path: str
 
     :return: A list of ids in string format.
     :rtype: [str]
-    '''
+    """
     ids = []
-    file_list = glob.glob(folderPath + '\\*' + '.txt')
+    file_list = glob.glob(folder_path + "\\*" + ".txt")
     # delete marker files
-    resultDelete = True
+    result_delete = True
     for fd in file_list:
-        if(debugMode_ == False):
-            resultDelete = resultDelete & util.FileDelete(fd)
-    if(not resultDelete):
-        Output ('Failed to delete a marker file!')
+        if debug_mode_ == False:
+            result_delete = result_delete & fileIO.file_delete(fd)
+    if not result_delete:
+        output("Failed to delete a marker file!")
     for f in file_list:
-        ids.append(AdjustSessionIdFileNameBack(Path.GetFileNameWithoutExtension(f)))
+        ids.append(
+            adjust_session_id_file_name_back(Path.GetFileNameWithoutExtension(f))
+        )
     return ids
 
-def GetLogFiles(listOfSessionIds):
-    '''
+
+def get_log_files(list_of_session_ids):
+    """
     Returns a list of fully qualified filepath to log files matching the provided session Ids.
 
-    :param listOfSessionIds: List of session ids.
-    :type listOfSessionIds: [str]
+    :param list_of_session_ids: List of session ids.
+    :type list_of_session_ids: [str]
 
     :return: List of fully qualified file path.
     :rtype: [str]
-    '''
+    """
 
     # save the current file in epoch
-    timeNow = time.time()
-    fileList = glob.glob(os.path.join(os.getenv('LOCALAPPDATA'),'BatchRvt') + '\\*' + '.log')
-    logFiles = []
-    if len(fileList) > 0:
-        for l in fileList:
+    time_now = time.time()
+    file_list = glob.glob(
+        os.path.join(os.getenv("LOCALAPPDATA"), "BatchRvt") + "\\*" + ".log"
+    )
+    log_files = []
+    if len(file_list) > 0:
+        for l in file_list:
             # check whether file is older than 24h
-            fileTime = os.path.getmtime(l)
+            file_time = os.path.getmtime(l)
             # 24 hr are 86400 seconds
-            timeOut = 86400
-            if debugMode_ == True:
-                timeOut = 8640000
-            if timeNow - fileTime < timeOut:
+            time_out = 86400
+            if debug_mode_ == True:
+                time_out = 8640000
+            if time_now - file_time < time_out:
                 # read the first two rows of the file to get the id
-                idString = GetSessionIdFromLogFile(l)
-                for idToMatch in listOfSessionIds:
-                    if idToMatch == idString:
-                        logFiles.append(l)
+                id_string = get_session_id_from_log_file(l)
+                for id_to_match in list_of_session_ids:
+                    if id_to_match == id_string:
+                        log_files.append(l)
             else:
-                Output('File is to old: ' + str(l))
-    return logFiles
+                output("File is to old: " + str(l))
+    return log_files
+
 
-def GetSessionIdFromLogFile(filePath):
-    '''
+def get_session_id_from_log_file(file_path):
+    """
     Reads the first two rows of a log file to get the session Id used.
 
-    :param filePath: Fully qualified file path to log file
-    :type filePath: str
+    :param file_path: Fully qualified file path to log file
+    :type file_path: str
 
     :return: The session id, or if not not a log file: an empty string.
     :rtype: str
-    '''
+    """
 
-    rowCounter = 0
-    retrievedId = ''
-    for line in open( filePath, 'r' ):
+    row_counter = 0
+    retrieved_id = ""
+    for line in open(file_path, "r"):
         # read row 2 only
-        if(rowCounter == 1):
+        if row_counter == 1:
             data = json.loads(line)
-            message = GetMessageFromJson(data)
-            retrievedId = GetIdFromRow(message)
+            message = get_message_from_json(data)
+            retrieved_id = get_id_from_row(message)
             break
-        rowCounter += 1
-    return retrievedId
+        row_counter += 1
+    return retrieved_id
+
 
-def GetIdFromRow(row):
-    '''
+def get_id_from_row(row):
+    """
     Extracts the session Id from logfile row.
 
-    sample: 
+    sample:
     {"date":{"local":"17/12/2020","utc":"17/12/2020"},"time":{"local":"16:49:27","utc":"05:49:27"},"sessionId":"235e2180-dc33-4d61-8773-1005a59344c0","message":{"msgId":"","message":"Session ID: <2020-12-17T05:49:27.559Z>"}}
 
     Note: There are two session id fields in thi string!
-    
+
     TODO: Do some error handling!
 
     :param row: A json formatted string with the session id in chevrons.
     :type row: str
 
     :return: The session id.
     :rtype: str
-    '''
+    """
 
-    first = '<'
-    last = '>'
-    t = GetTextBetween(row, first, last)
+    first = "<"
+    last = ">"
+    t = get_text_between(row, first, last)
     return first + t + last
 
-def GetTextBetween(text, first, last):
-    '''
+
+def get_text_between(text, first, last):
+    """
     Returns text in between characters
 
     :param text: Text to parse
     :type text: str
     :param first: String indicating start
     :type first: str
     :param last: String indicating end
     :type last: str
 
     :return: string in between start and end.
     :rtype: str
-    '''
+    """
 
     start = text.index(first) + len(first)
     end = text.index(last, start)
     return text[start:end]
 
-def GetMessageFromJson(data):
-    '''
+
+def get_message_from_json(data):
+    """
     Returns the outer message string from json formatted message field in log file.
 
-    sample: 
+    sample:
     {"date":{"local":"17/12/2020","utc":"17/12/2020"},"time":{"local":"16:49:27","utc":"05:49:27"},"sessionId":"235e2180-dc33-4d61-8773-1005a59344c0","message":{"msgId":"","message":"Session ID: <2020-12-17T05:49:27.559Z>"}}
 
     This includes leading tab characters
 
     :param data: json formatted row of logfile
     :type data: str
 
     :return: The message string
     :rtype: str
-    '''
-    outerMessage = data['message']
-    return outerMessage['message']
+    """
+    outer_message = data["message"]
+    return outer_message["message"]
+
 
-def ProcessLogFile(filePath):
-    '''
+def process_log_file(file_path):
+    """
     Process revit batch processor session log file.
-    
+
     - find Revit files processed:
     - check whether an exception occurred when processing any of the above files.
 
-    :param filePath: Fully qualified file path to json formatted log file
-    :type filePath: str
+    :param file_path: Fully qualified file path to json formatted log file
+    :type file_path: str
 
     :return: returns list of arrays in format:
         [[processed Revit file name, status of processing (true or false), message]]
     :rtype: [[str]]
-    '''
+    """
 
-    filesProcessStatus = []
+    files_process_status = []
     # get all files processed
     try:
-        filesProcessed = GetFilesProcessed(filePath)
+        files_processed = get_files_processed(file_path)
         # check whether any file not founds came back
         try:
-            filesNotFound = GetFilesNotFound(filesProcessed)
+            files_not_found = get_files_not_found(files_processed)
             try:
-                # filter filesProcessed by files not found
-                filesToCheck = filterFilesNotFound(filesProcessed, filesNotFound)
+                # filter files_processed by files not found
+                files_to_check = filter_files_not_found(
+                    files_processed, files_not_found
+                )
                 # check for exceptions during file processing
-                for fileToCheck in filesToCheck:
+                for file_to_check in files_to_check:
                     try:
-                        status, message = GetProcessStatus(fileToCheck, filePath)
+                        status, message = get_process_status(file_to_check, file_path)
                     except Exception as e:
-                        Output ('GetProcessStatus: ' + str(e))
-                    dummy = [fileToCheck, status, message]
-                    filesProcessStatus.append(dummy)
+                        output("GetProcessStatus: " + str(e))
+                    dummy = [file_to_check, status, message]
+                    files_process_status.append(dummy)
                 # add files not found
-                for f in filesNotFound:
-                    dummy = [f[0], False, ['File not found']]
-                    filesProcessStatus.append(dummy)
+                for f in files_not_found:
+                    dummy = [f[0], False, ["File not found"]]
+                    files_process_status.append(dummy)
             except Exception as e:
-                Output ('FileToCheck: ' + str(e))
+                output("FileToCheck: " + str(e))
         except Exception as e:
-            Output ('GetFilesNotFound: ' + str(e))
+            output("GetFilesNotFound: " + str(e))
     except Exception as e:
-        Output ('GetFilesProcessed: ' + str(e))
-    return filesProcessStatus
+        output("GetFilesProcessed: " + str(e))
+    return files_process_status
+
 
 # filtering files not found from overall file list
 #
 # filesProcessed: list of arrays, first entry in array is fully qualified file path
 # filesNotFound: list of fully qualified file path
 # returns a list of fully qualified file path (of files marked as found)
-def filterFilesNotFound(filesProcessed, filesNotFound):
-    filteredList = []
-    for fileName,status in filesProcessed:
+def filter_files_not_found(files_processed, files_not_found):
+    filtered_list = []
+    for file_name, status in files_processed:
         flag = False
-        for fn, fnStatus in filesNotFound:
-            if(fn == fileName):
+        for fn, fnStatus in files_not_found:
+            if fn == file_name:
                 flag = True
                 break
-        if (not flag):
-            filteredList.append(fileName)
-    return filteredList
+        if not flag:
+            filtered_list.append(file_name)
+    return filtered_list
+
 
-def GetProcessStatus(fileToCheck, logFilePath):
-    '''
+def get_process_status(file_to_check, log_file_path):
+    """
     Reads a log file and checks whether any exception occurred when processing a specific revit file.
 
-    :param fileToCheck: Fully qualified file path of Revit file which was processed
-    :type fileToCheck: str
-    :param logFilePath: The fully qualified batch processor session log file path.
-    :type logFilePath: str
+    :param file_to_check: Fully qualified file path of Revit file which was processed
+    :type file_to_check: str
+    :param log_file_path: The fully qualified batch processor session log file path.
+    :type log_file_path: str
 
     :return: A process status and a message.
 
         - process status: True if no exception occurred during revit file processing, otherwise false
         - message: the exception message recorded in the log file.
 
     :rtype: bool, str
-    '''
+    """
 
-    message = ['Found no match in log file']
+    message = ["Found no match in log file"]
     # flag indicating whether we managed to retrieve processing data for a file
-    foundMatch = False
-    jsonData = ReadLogFile(logFilePath)
+    found_match = False
+    json_data = read_log_file(log_file_path)
     # get data block showing how each file was processed
-    unformattedRevitFileProcessMessages = GetLogBlocks(jsonData, '\t- Processing file (', ['\t- Task script operation completed.','\t- Operation aborted.'], True)
-    processStatus = True
+    unformatted_revit_file_process_messages = get_log_blocks(
+        json_data,
+        "\t- Processing file (",
+        ["\t- Task script operation completed.", "\t- Operation aborted."],
+        True,
+    )
+    process_status = True
     # loop over messages in this block and check for time out, and exception messages
-    for messageBlock in  unformattedRevitFileProcessMessages:
+    for message_block in unformatted_revit_file_process_messages:
         # check if right file the file name
         # todo
-        fileName = GetFileNameFromDataBlock(messageBlock)
-        if(fileName == fileToCheck):
-            Output('file to check: ' +str(fileToCheck + '     file found: '+fileName) +'    is match '  +str(fileName == fileToCheck))
-            foundMatch = True
+        file_name = get_file_name_from_data_block(message_block)
+        if file_name == file_to_check:
+            output(
+                "file to check: "
+                + str(file_to_check + "     file found: " + file_name)
+                + "    is match "
+                + str(file_name == file_to_check)
+            )
+            found_match = True
             # flag to show whether logs show any issues
-            foundProblem = False
-            for m in messageBlock:
-                Output(m)
+            found_problem = False
+            for m in message_block:
+                output(m)
                 # check for exceptions
-                for exceptionMessage in EXCEPTION_MESSAGES:
-                    if(exceptionMessage in m):
-                        processStatus = False
-                        foundProblem = True
+                for exception_message in EXCEPTION_MESSAGES:
+                    if exception_message in m:
+                        process_status = False
+                        found_problem = True
                         message = [m.strip()]
                         break
-            if (foundProblem == False):
-                message = '[ok]'
-                processStatus = True
+            if found_problem == False:
+                message = "[ok]"
+                process_status = True
     # check if a match for given file was found in log data
-    if(foundMatch == False):
-        processStatus = False
-        message = '[Failed to retrieve processing data for file.]'
-    return processStatus, message
-        
-def GetFileNameFromDataBlock(messageBlock):
-    '''
+    if found_match == False:
+        process_status = False
+        message = "[Failed to retrieve processing data for file.]"
+    return process_status, message
+
+
+def get_file_name_from_data_block(message_block):
+    """
     Extracts the file name from a process message block.
 
-    :param messageBlock: list of json formatted rows representing all messages received during file process
-    :type messageBlock: [str]
+    :param message_block: list of json formatted rows representing all messages received during file process
+    :type message_block: [str]
 
     :return: The fully qualified file path of the file processed
     :rtype: str
-    '''
+    """
 
     # check if this is a cloud model
-    if('CLOUD MODEL' in messageBlock[0]):
-        #['\t- Processing file (1 of 1): CLOUD MODEL', '\t- ', '\t- \tProject ID: GUID', '\t- \tModel ID: GUID',...]
-        messageStarter = '\t- \t'
-        fileName = messageBlock[3].Trim()[len(messageStarter)-1:]
+    if "CLOUD MODEL" in message_block[0]:
+        # ['\t- Processing file (1 of 1): CLOUD MODEL', '\t- ', '\t- \tProject ID: GUID', '\t- \tModel ID: GUID',...]
+        message_starter = "\t- \t"
+        file_name = message_block[3].Trim()[len(message_starter) - 1 :]
     else:
         # ["\t- Processing file (x of y): file path"}},...]
-        messageStarter = '\t- Processing file (x of y): '
-        fileName = messageBlock[0].Trim()[len(messageStarter)-1:]
-    return fileName
+        message_starter = "\t- Processing file (x of y): "
+        file_name = message_block[0].Trim()[len(message_starter) - 1 :]
+    return file_name
+
 
-def GetFilesProcessed(filePath):
-    '''
+def get_files_processed(file_path):
+    """
     Reads a batch processor logfile and extracts all file names of files processed.
-    
-    :param filePath: The fully qualified file path to log file.
-    :type filePath: str
+
+    :param file_path: The fully qualified file path to log file.
+    :type file_path: str
 
     :return: a list lists containing The fully qualified file path for each file processed and their process status. True for no exception encountered, otherwise false.
         [[filepath, status]]
     :rtype: [[str, bool]]
-    '''
+    """
     # log file structure:
     # start of file list (file server):
     #   {"date":{"local":"17/12/2020","utc":"17/12/2020"},"time":{"local":"16:49:28","utc":"05:49:28"},"sessionId":"235e2180-dc33-4d61-8773-1005a59344c0","message":{"msgId":"","message":"Revit Files for processing (1):"}}
     #   {"date":{"local":"17/12/2020","utc":"17/12/2020"},"time":{"local":"16:49:28","utc":"05:49:28"},"sessionId":"235e2180-dc33-4d61-8773-1005a59344c0","message":{"msgId":"","message":""}}
     #   {"date":{"local":"17/12/2020","utc":"17/12/2020"},"time":{"local":"16:49:28","utc":"05:49:28"},"sessionId":"235e2180-dc33-4d61-8773-1005a59344c0","message":{"msgId":"","message":"\tP:\\something\\FileName.rvt"}}
     #   {"date":{"local":"17/12/2020","utc":"17/12/2020"},"time":{"local":"16:49:28","utc":"05:49:28"},"sessionId":"235e2180-dc33-4d61-8773-1005a59344c0","message":{"msgId":"","message":"\tFile exists: YES"}}
     #   {"date":{"local":"17/12/2020","utc":"17/12/2020"},"time":{"local":"16:49:28","utc":"05:49:28"},"sessionId":"235e2180-dc33-4d61-8773-1005a59344c0","message":{"msgId":"","message":"\tFile size: 86.93MB"}}
@@ -444,204 +496,246 @@
     #   {"date":{"local":"18/05/2021","utc":"18/05/2021"},"time":{"local":"19:20:00","utc":"09:20:00"},"sessionId":"e8a39f45-ca88-464f-a32f-278f0414280f","message":{"msgId":"","message":""}}
     #   {"date":{"local":"18/05/2021","utc":"18/05/2021"},"time":{"local":"19:20:00","utc":"09:20:00"},"sessionId":"e8a39f45-ca88-464f-a32f-278f0414280f","message":{"msgId":"","message":"\tCLOUD MODEL"}}
     #   {"date":{"local":"18/05/2021","utc":"18/05/2021"},"time":{"local":"19:20:00","utc":"09:20:00"},"sessionId":"e8a39f45-ca88-464f-a32f-278f0414280f","message":{"msgId":"","message":"\tProject ID: ee514b99-fac1-441a-ba98-6912c4aa4fdb"}}
     #   {"date":{"local":"18/05/2021","utc":"18/05/2021"},"time":{"local":"19:20:00","utc":"09:20:00"},"sessionId":"e8a39f45-ca88-464f-a32f-278f0414280f","message":{"msgId":"","message":"\tModel ID: c15a664d-fab8-4153-8532-b8fa04402528"}}
     #   {"date":{"local":"18/05/2021","utc":"18/05/2021"},"time":{"local":"19:20:00","utc":"09:20:00"},"sessionId":"e8a39f45-ca88-464f-a32f-278f0414280f","message":{"msgId":"","message":"\tRevit version: 2020"}}
     #   {"date":{"local":"18/05/2021","utc":"18/05/2021"},"time":{"local":"19:20:00","utc":"09:20:00"},"sessionId":"e8a39f45-ca88-464f-a32f-278f0414280f","message":{"msgId":"","message":""}}
     # end of file list
-    listOfFiles = []
-    jsonData = ReadLogFile(filePath)
+    list_of_files = []
+    json_data = read_log_file(file_path)
     # get data block showing which files are to be processed
     # there should just be one ...
-    logBlocks = GetLogBlocks(jsonData, 'Revit Files for processing', ['Starting batch operation...'], False)
-    if(len(logBlocks) > 0):
-        unformattedRevitFileProcessMessages = logBlocks[0]
+    log_blocks = get_log_blocks(
+        json_data, "Revit Files for processing", ["Starting batch operation..."], False
+    )
+    if len(log_blocks) > 0:
+        unformatted_revit_file_process_messages = log_blocks[0]
         # parse data block and get list of files and file exists status
         # each file block is proceeded by an empty message row
         # last entry is also an empty message block!
-        for x in range(len(unformattedRevitFileProcessMessages)):
-            # check for start of data block 
-            # Output('unformatted messages '+str(unformattedRevitFileProcessMessages))
-            if(unformattedRevitFileProcessMessages[x] == '' and x + 3 <= len(unformattedRevitFileProcessMessages)):
+        for x in range(len(unformatted_revit_file_process_messages)):
+            # check for start of data block
+            # Output('unformatted messages '+str(unformatted_revit_file_process_messages))
+            if unformatted_revit_file_process_messages[x] == "" and x + 3 <= len(
+                unformatted_revit_file_process_messages
+            ):
                 # check whether cloud model or file server model
-                if('CLOUD MODEL' in unformattedRevitFileProcessMessages[x + 1]):
+                if "CLOUD MODEL" in unformatted_revit_file_process_messages[x + 1]:
                     # get file data from next two rows
                     # substitute file name with file GUID, fake the status always exists
-                    dummy = [unformattedRevitFileProcessMessages[x + 3],'File exists: YES']
+                    dummy = [
+                        unformatted_revit_file_process_messages[x + 3],
+                        "File exists: YES",
+                    ]
                 else:
                     # get file data from next two rows
-                    dummy = [unformattedRevitFileProcessMessages[x + 1],unformattedRevitFileProcessMessages[x + 2]]
-                listOfFiles.append(GetFileData(dummy))
-    return listOfFiles
+                    dummy = [
+                        unformatted_revit_file_process_messages[x + 1],
+                        unformatted_revit_file_process_messages[x + 2],
+                    ]
+                list_of_files.append(get_file_data(dummy))
+    return list_of_files
+
 
 # method parsing two rows of json formatted data
 #
 # data list of 2 rows of Json formatted data
 # sample of file system:
-#18/05/2021 15:57:53 : 	File exists: YES
-#18/05/2021 15:57:53 : 	File size: 199.38MB
+# 18/05/2021 15:57:53 : 	File exists: YES
+# 18/05/2021 15:57:53 : 	File size: 199.38MB
 # sample of BIM360:
-#18/05/2021 15:37:23 : 	Project ID: a valid guid
-#18/05/2021 15:37:23 : 	Model ID: a valid guid
+# 18/05/2021 15:37:23 : 	Project ID: a valid guid
+# 18/05/2021 15:37:23 : 	Model ID: a valid guid
 # note: when processing BIM360 files batch processor is not checking whether the file exists upfront!
 # returns list in format
 # [filename, file exists status as bool]
-def GetFileData(data):
+def get_file_data(data):
     # trim white spaces from file name
-    fileName = data[0].Trim()
-    fileStatus = False
-    # check whether file status contains a YES or whether this is a cloud model 
+    file_name = data[0].Trim()
+    file_status = False
+    # check whether file status contains a YES or whether this is a cloud model
     # (RBP does not check upfront whether a cloud model exists!)
-    if ('YES' in data[1] or 'Project ID' in data[1]):
-        fileStatus = True
-    return [fileName,fileStatus]  
+    if "YES" in data[1] or "Project ID" in data[1]:
+        file_status = True
+    return [file_name, file_status]
+
 
-def GetFilesNotFound(filesProcessed):
-    '''
+def get_files_not_found(files_processed):
+    """
     Filters list of all files meant to be processed and returns the ones flagged as file not found.
 
-    :param filesProcessed: array of lists in format: [[filename, status as bool],[filename, status as bool],...]
-    :type filesProcessed: [[str, bool]]
+    :param files_processed: array of lists in format: [[filename, status as bool],[filename, status as bool],...]
+    :type files_processed: [[str, bool]]
 
     :return: array of lists in format: [[filename, status as bool],[filename, status as bool],...]
     :rtype: [[str, bool]]
-    '''
+    """
 
-    fileNotFound = []
-    for f in filesProcessed:
-        if f[1]==False:
-            fileNotFound.append(f)
-    return fileNotFound
+    file_not_found = []
+    for f in files_processed:
+        if f[1] == False:
+            file_not_found.append(f)
+    return file_not_found
 
-def GetLogBlocks(jsonData, startMarker, endMarkers, multipleBlocks):
-    '''
+
+def get_log_blocks(json_data, start_marker, end_markers, multiple_blocks):
+    """
     Reads json formatted data into blocks per files processed.
 
     Returns the message sections per row entry only.
 
-    :param jsonData: List of logfile rows in json data format
-    :type jsonData: [str]
-    :param startMarker: String in messages indicating start of block.
-    :type startMarker: str
-    :param endMarkers: String in messages indicating end of block.
-    :type endMarkers: str
-    :param multipleBlocks: Flag indicating whether there are multiple data block in log file to be returned
-    :type multipleBlocks: bool
+    :param json_data: List of logfile rows in json data format
+    :type json_data: [str]
+    :param start_marker: String in messages indicating start of block.
+    :type start_marker: str
+    :param end_markers: String in messages indicating end of block.
+    :type end_markers: str
+    :param multiple_blocks: Flag indicating whether there are multiple data block in log file to be returned
+    :type multiple_blocks: bool
 
     :return: List of list of str
     :rtype: [[str]]
-    '''
+    """
 
-    unformattedBlockData = []
-    dataBlock = []
-    messageString = ''
+    unformatted_block_data = []
+    data_block = []
+    message_string = ""
     # extract rows belonging to blocks
-    fileBlock = False
-    #Output('json data: ' + str(jsonData))
-    for data in jsonData:
-        messageString = GetMessageFromJson(data)
-        if messageString.startswith(startMarker) and fileBlock == False:
-            fileBlock = True
+    file_block = False
+    # Output('json data: ' + str(json_data))
+    for data in json_data:
+        message_string = get_message_from_json(data)
+        if message_string.startswith(start_marker) and file_block == False:
+            file_block = True
         # flag to indicate we found a match for end of block
-        matchEndBlock = False
-        for endMarker in endMarkers:
+        match_end_block = False
+        for end_marker in end_markers:
             match = False
-            if messageString.startswith(endMarker) and fileBlock == True:
-                matchEndBlock = True
-                unformattedBlockData.append(dataBlock)
-                dataBlock = []
-                fileBlock = False
+            if message_string.startswith(end_marker) and file_block == True:
+                match_end_block = True
+                unformatted_block_data.append(data_block)
+                data_block = []
+                file_block = False
                 match = True
                 break
-        if(not multipleBlocks and match):
+        if not multiple_blocks and match:
             break
-        if (fileBlock):
-            dataBlock.append(messageString)
+        if file_block:
+            data_block.append(message_string)
     # check for open block
-    if (fileBlock == True and matchEndBlock == False):
+    if file_block == True and match_end_block == False:
         # append this data...hopefully there is an exception message in there!!
-        unformattedBlockData.append(dataBlock)
-        Output('Added open data block')
-        Output(dataBlock)
-        Output('')
-    return unformattedBlockData
+        unformatted_block_data.append(data_block)
+        output("Added open data block")
+        output(data_block)
+        output("")
+    return unformatted_block_data
+
 
-def ReadLogFile(filePath):
-    '''
+def read_log_file(file_path):
+    """
     Reads batch processor log file into lists of json objects.
-    
+
     Sample row:
         {'sessionId': '778e87a5-4b94-4552-9e7e-c9ed38b5caee', 'time': {'local': '09:35:45', 'utc': '22:35:45'}, 'date': {'local': '25/11/2020', 'utc': '24/11/2020'}, 'message': {'msgId': '', 'message': ''}}
-    
-    :param filePath: The fully qualified file path to log file in json format
-    :type filePath: str
+
+    :param file_path: The fully qualified file path to log file in json format
+    :type file_path: str
 
     :return: list of json objects
     :rtype: [json]
-    '''
+    """
 
     data = []
-    with open(filePath) as f:
+    with open(file_path) as f:
         for line in f:
             data.append(json.loads(line))
     return data
 
-def ProcessLogFiles(folderPath, debug = False):
-    '''
+
+def process_log_files(folder_path, debug=False):
+    """
     Loops over log files and checks whether any exceptions occurred during revit files processing.
 
-    :param folderPath: Fully qualified directory path where marker files are stored.
-    :type folderPath: str
+    :param folder_path: Fully qualified directory path where marker files are stored.
+    :type folder_path: str
     :param debug: Flag indicating whether this is running in debug mode which will output some debug messages, defaults to False
     :type debug: bool, optional
 
-    :return: List of lists of revit files processed in format:
-        [logId,[processed Revit file name, status of processing (true or false), message]]
-    :rtype: [str,[str, bool, str]]
-    '''
-
-    returnValue = res.Result()
-    debugMode_ = debug
-    logfileResults = []
+    :return:
+        Result class instance.
+
+        - Process status returned in result.status. False if an exception occurred, otherwise True.
+        - result.message will contain message(s) for each revit file found in logs and whether an exception occurred during processing
+        - result.result will be an empty list.
+
+        On exception:
+
+        - result.status (bool) will be False.
+        - result.message will contain the exception message.
+        - result.status will be an empty list.
+
+    :rtype: :class:`.Result`
+
+    """
+
+    return_value = res.Result()
+    debug_mode_ = debug
+    logfile_results = []
     try:
         # get all marker files
-        markerFileIds = GetCurrentSessionIds(folderPath)
-        if(debugMode_):
-            returnValue.AppendMessage('Found marker file(s): ' + str(len(markerFileIds)))
-        if(len(markerFileIds) > 0):
+        marker_file_ids = get_current_session_ids(folder_path)
+        if debug_mode_:
+            return_value.append_message(
+                "Found marker file(s): {}".format(len(marker_file_ids))
+            )
+        if len(marker_file_ids) > 0:
             # find log files matching markers
-            logFiles = GetLogFiles(markerFileIds)
-            if(debugMode_):
-                returnValue.AppendMessage('Found log file(s): ' + str(len(logFiles)))
-            if(len(logFiles) == len(markerFileIds)):
+            log_files = get_log_files(marker_file_ids)
+            if debug_mode_:
+                return_value.append_message(
+                    "Found log file(s): {}".format(len(log_files))
+                )
+            if len(log_files) == len(marker_file_ids):
                 data = []
-                for lf in logFiles:
+                for lf in log_files:
                     # debug output
-                    message = 'Processing log file(s): ' + lf
-                    #returnValue.AppendMessage('Processing log files: ' + lf)
+                    message = "Processing log file(s): {}".format(lf)
+                    # return_value.AppendMessage('Processing log files: ' + lf)
                     try:
-                        data = ProcessLogFile(lf)
-                        if (len(data) > 0):
-                            message = message + ' [Got processed Revit file(s) data: ' + str(len(data)) +']'
+                        data = process_log_file(lf)
+                        if len(data) > 0:
+                            message = (
+                                "{} [Got processed Revit file(s) data: {}]".format(
+                                    message, len(data)
+                                )
+                            )
                         else:
                             # dummy run no files processed!
-                            message = message + ' [No Revit file(s) processed!]'
+                            message = "{} [No Revit file(s) processed!]".format(message)
                     except Exception as e:
-                        message = message + ' [An exception occurred: ' + str(e) + ']'
-                    if(debugMode_):
-                        returnValue.AppendMessage(message)
+                        message = "{} [An exception occurred: {}]".format(message, e)
+                    if debug_mode_:
+                        return_value.append_message(message)
                     for d in data:
-                        logfileResults.append(d)
-                returnValue.AppendMessage('\n')
-                returnValue.AppendMessage('Processed file(s) results:')
+                        logfile_results.append(d)
+                return_value.append_message("\n")
+                return_value.append_message("Processed file(s) results:")
                 # store results in return object
-                for lfResults in logfileResults:
-                    listToStr = '\t'.join(map(str, lfResults)) 
-                    returnValue.AppendMessage(listToStr)
-                returnValue.status = True
+                for lf_results in logfile_results:
+                    list_to_str = "\t".join(map(str, lf_results))
+                    return_value.append_message(list_to_str)
+                return_value.status = True
             else:
-                returnValue.UpdateSep(False,'Number of log files [' + str(len(logFiles)) + '] does not match required number: ' + str(len(markerFileIds))) 
+                return_value.update_sep(
+                    False,
+                    "Number of log files [{}] does not match required number: {}".format(
+                        len(log_files), len(marker_file_ids)
+                    ),
+                )
         else:
-            returnValue.UpdateSep(False,'No marker files found in location: ' + str(folderPath))
+            return_value.update_sep(
+                False, "No marker files found in location: {}".format(folder_path)
+            )
     except Exception as e:
-        returnValue.UpdateSep(False, 'Terminated with Exception '+ str(e))    
-    return returnValue
+        return_value.update_sep(False, "Terminated with Exception: {}".format(e))
+    return return_value
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `DuHast-0.0.6/src/duHast/Utilities/Result.py` & `DuHast-0.0.7/src/duHast/Utilities/Objects/result.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,122 +1,134 @@
-'''
+"""
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 A class used to return status, messages and objects back to a caller.
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
-'''
+
+
+A class used to return the value if any, a message and the status of a method (true if everything is ok or false if something went wrong).
+
+"""
+
+
 #
-#License:
+# License:
 #
 #
 # Revit Batch Processor Sample Code
 #
-# Copyright (c) 2020  Jan Christel
-#
-# This program is free software: you can redistribute it and/or modify
-# it under the terms of the GNU General Public License as published by
-# the Free Software Foundation, either version 3 of the License, or
-# (at your option) any later version.
+# BSD License
+# Copyright © 2023, Jan Christel
+# All rights reserved.
+
+# Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
+
+# - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
+# - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
+# - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
 #
-# This program is distributed in the hope that it will be useful,
-# but WITHOUT ANY WARRANTY; without even the implied warranty of
-# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
-# GNU General Public License for more details.
+# This software is provided by the copyright holder "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. 
+# In no event shall the copyright holder be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; 
+# or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
 #
-# You should have received a copy of the GNU General Public License
-# along with this program.  If not, see <http://www.gnu.org/licenses/>.
 #
 #
 
+from duHast.Utilities.Objects import base
 
-#a class used to return the value  if any, a message and the status of a method (true if everything is ok or false if something went wrong)
-class Result: 
+
+class Result(base.Base):
     def __init__(self):
-        '''
+        """
         Class constructor.
 
         - message default value is -
         - status default value is True
         - result default value is []
-        
-        '''
 
-        self.message = '-'
+        """
+
+        super(Result, self).__init__()
+
+        self.message = "-"
         self.status = True
         self.result = []
-    
-    def AppendMessage(self, message):
-        '''
+
+    def append_message(self, message):
+        """
         Appends a new line and new message string to the existing message.
 
         First message appended will replace the default value of -
 
         :param message: The new message to be appended.
         :type message: str
-        '''
+        """
+
         try:
-            if(self.message == '-'):
+            if self.message == "-":
                 self.message = message
             else:
-                self.message = self.message + '\n' + message
+                self.message = self.message + "\n" + message
         except Exception as e:
-            print (str(e))
+            print(str(e))
             pass
 
-    def Update(self, otherResult):
-        '''
+    def update(self, otherResult):
+        """
         Will use the past in result instance to update the instance.
 
-        - .status is using a logical AND 
+        - .status is using a logical AND
         - .message is using append (unless other message is default '-')
         - .result is looping over past in result and adding it one by one to this .result list (ignores None)
 
         :param otherResult: Another result class instance.
         :type otherResult: SampleBatchProcessorCode.Result
-        '''
+        """
+
         try:
             # check if default message string, if so do not update
-            if(otherResult.message != '-'):
-                self.AppendMessage(otherResult.message)
+            if otherResult.message != "-":
+                self.append_message(otherResult.message)
             self.status = self.status & otherResult.status
             # check if result property that was passed in has values
-            if(otherResult.result is not None and len(otherResult.result)>0):
+            if otherResult.result is not None and len(otherResult.result) > 0:
                 for item in otherResult.result:
                     self.result.append(item)
         except Exception as e:
-            print (str(e))
+            print(str(e))
             pass
-    
-    def UpdateSep (self, status, message):
-        '''
+
+    def update_sep(self, status, message):
+        """
         Updates the .status and .message property only.
-        
-        - .status is using a logical AND 
+
+        - .status is using a logical AND
         - .message is using append (unless other message is default '-')
-        
+
         :param status: The status to be added.
         :type status: bool
         :param message: The message to be appended.
         :type message: str
-        '''
-        
+        """
+
         try:
-            self.AppendMessage(message)
+            self.append_message(message)
             # self.message = self.message + '\n' + message
             self.status = self.status & status
         except Exception as e:
-            print (str(e))
+            print(str(e))
             pass
 
-    def UpdateStatus(self, status):
-        '''
+    def update_status(self, status):
+        """
         Update .status only.
 
-        - .status is using a logical AND 
+        - .status is using a logical AND
 
         :param status: The status to be added.
         :type status: bool
-        '''
+        """
+
         try:
             self.status = self.status & status
         except Exception as e:
-            print (str(e))
+            print(str(e))
             pass
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

