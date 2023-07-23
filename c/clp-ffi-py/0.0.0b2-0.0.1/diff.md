# Comparing `tmp/clp_ffi_py-0.0.0b2.tar.gz` & `tmp/clp_ffi_py-0.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "clp_ffi_py-0.0.0b2.tar", last modified: Wed Jul 12 05:41:36 2023, max compression
+gzip compressed data, was "clp_ffi_py-0.0.1.tar", last modified: Sun Jul 23 21:43:11 2023, max compression
```

## Comparing `clp_ffi_py-0.0.0b2.tar` & `clp_ffi_py-0.0.1.tar`

### file list

```diff
@@ -1,215 +1,206 @@
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:36.001352 clp_ffi_py-0.0.0b2/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      853 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/.clang-format
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1402 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/.clang-tidy
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.969351 clp_ffi_py-0.0.0b2/.github/
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.969351 clp_ffi_py-0.0.0b2/.github/ISSUE_TEMPLATE/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1113 2023-06-14 03:44:36.000000 clp_ffi_py-0.0.0b2/.github/ISSUE_TEMPLATE/bug-report.yml
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)       27 2023-06-14 03:44:36.000000 clp_ffi_py-0.0.0b2/.github/ISSUE_TEMPLATE/config.yml
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      557 2023-06-14 03:44:36.000000 clp_ffi_py-0.0.0b2/.github/ISSUE_TEMPLATE/feature-request.yml
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      283 2023-06-14 03:05:42.000000 clp_ffi_py-0.0.0b2/.github/PULL_REQUEST_TEMPLATE.md
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.969351 clp_ffi_py-0.0.0b2/.github/workflows/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      758 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/.github/workflows/build_wheels.yml
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      122 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/.gitignore
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)       80 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/.gitmodules
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    11356 2023-06-14 03:19:32.000000 clp_ffi_py-0.0.0b2/LICENSE
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      296 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/MANIFEST.in
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4278 2023-07-12 05:41:36.001352 clp_ffi_py-0.0.0b2/PKG-INFO
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3795 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/README.md
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.969351 clp_ffi_py-0.0.0b2/clp_ffi_py/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      303 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/clp_ffi_py/CLPFourByteEncoder.pyi
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      930 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/clp_ffi_py/CLPIRDecoder.pyi
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2765 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/clp_ffi_py/FileReader.py
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)        0 2023-06-14 03:05:42.000000 clp_ffi_py-0.0.0b2/clp_ffi_py/__init__.py
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)        0 2023-06-14 03:05:42.000000 clp_ffi_py-0.0.0b2/clp_ffi_py/py.typed
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1079 2023-07-02 19:45:23.000000 clp_ffi_py-0.0.0b2/clp_ffi_py/utils.py
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.973351 clp_ffi_py-0.0.0b2/clp_ffi_py.egg-info/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4278 2023-07-12 05:41:35.000000 clp_ffi_py-0.0.0b2/clp_ffi_py.egg-info/PKG-INFO
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8478 2023-07-12 05:41:35.000000 clp_ffi_py-0.0.0b2/clp_ffi_py.egg-info/SOURCES.txt
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)        1 2023-07-12 05:41:35.000000 clp_ffi_py-0.0.0b2/clp_ffi_py.egg-info/dependency_links.txt
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)       66 2023-07-12 05:41:35.000000 clp_ffi_py-0.0.0b2/clp_ffi_py.egg-info/requires.txt
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)       11 2023-07-12 05:41:35.000000 clp_ffi_py-0.0.0b2/clp_ffi_py.egg-info/top_level.txt
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      945 2023-07-12 05:41:02.000000 clp_ffi_py-0.0.0b2/pyproject.toml
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      166 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/requirements-dev.txt
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)       38 2023-07-12 05:41:36.001352 clp_ffi_py-0.0.0b2/setup.cfg
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2752 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/setup.py
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.965351 clp_ffi_py-0.0.0b2/src/
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.961351 clp_ffi_py-0.0.0b2/src/clp/
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.961351 clp_ffi_py-0.0.0b2/src/clp/components/
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.965351 clp_ffi_py-0.0.0b2/src/clp/components/core/
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.981351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5498 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ArrayBackedPosIntSet.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      914 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/CommandLineArgumentsBase.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1025 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/DictionaryEntry.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8995 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/DictionaryReader.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     9605 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/DictionaryWriter.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5003 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/EncodedVariableInterpreter.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      613 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ErrorCode.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3611 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/FileReader.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2681 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/FileWriter.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2463 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/GlobalMetadataDB.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1506 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/GlobalMetadataDBConfig.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3405 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/GlobalMySQLMetadataDB.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3184 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/GlobalSQLiteMetadataDB.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4847 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/Grep.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3297 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/LibarchiveFileReader.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5050 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/LibarchiveReader.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5344 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/LogTypeDictionaryEntry.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      423 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/LogTypeDictionaryReader.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1203 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/LogTypeDictionaryWriter.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2112 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/MessageParser.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3173 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/MySQLDB.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1427 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/MySQLParamBindings.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1657 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/MySQLPreparedStatement.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8341 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/PageAllocatedVector.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1764 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ParsedMessage.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1752 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/Platform.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     6593 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/Profiler.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     7759 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/Query.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5235 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ReaderInterface.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1222 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/SQLiteDB.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2338 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/SQLitePreparedStatement.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      474 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/Stopwatch.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2960 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/StringReader.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1511 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/Thread.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5288 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/TimestampPattern.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)       34 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/TraceableException.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1148 2023-06-03 03:52:34.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/TraceableException.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3517 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/Utils.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2247 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/VariableDictionaryEntry.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      432 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/VariableDictionaryReader.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1095 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/VariableDictionaryWriter.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1476 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/Writer.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2044 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/WriterInterface.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.981351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clg/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2130 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clg/CommandLineArguments.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.981351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clo/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1842 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clo/CommandLineArguments.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      780 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clo/ControllerMonitoringThread.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.985351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3152 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/CommandLineArguments.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4115 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/FileCompressor.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1193 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/FileDecompressor.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      935 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/FileToCompress.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      918 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/StructuredFileToCompress.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1605 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/compression.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      568 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/decompression.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      126 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/run.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3632 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/utils.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.985351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1303 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/Constants.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    13827 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/LALR1Parser.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    32949 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/LALR1Parser.tpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     6708 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/Lexer.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    24628 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/Lexer.tpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2496 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/LogParser.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3627 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/SchemaParser.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1718 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/Token.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.989351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    15948 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexAST.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    10255 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexAST.tpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2433 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexDFA.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1438 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexDFA.tpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4122 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexNFA.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8484 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexNFA.tpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5239 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/UnicodeIntervalTree.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8505 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/UnicodeIntervalTree.tpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      608 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/utils.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2239 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/database_utils.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      782 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/dictionary_utils.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.989351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3955 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/encoding_methods.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    13102 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/encoding_methods.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    24981 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/encoding_methods.tpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.989351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      323 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/byteswap.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    21845 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/decoding_methods.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5894 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/decoding_methods.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    12961 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/encoding_methods.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3080 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/encoding_methods.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2127 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/protocol_constants.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.989351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3645 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/CompositeWildcardToken.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1929 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/ExactVariableToken.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      805 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/QueryMethodFailed.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1553 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/QueryToken.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2512 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/QueryWildcard.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1905 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/Subquery.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3281 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/WildcardToken.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1559 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/fmtlib_specializations.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      584 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/query_methods.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.993352 clp_ffi_py-0.0.0b2/src/clp/components/core/src/networking/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      656 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/networking/SocketOperationFailed.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1542 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/networking/socket_utils.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.993352 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2467 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/Constants.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5475 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/MetadataDB.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.993352 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5228 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/Archive.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5376 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/File.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1042 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/Message.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2329 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/Segment.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1733 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/SegmentManager.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.993352 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/writer/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    13234 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/writer/Archive.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8361 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/writer/File.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3011 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/writer/Segment.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.993352 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1883 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/Compressor.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      324 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/Constants.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2217 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/Decompressor.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.993352 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/passthrough/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2389 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/passthrough/Compressor.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4064 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/passthrough/Decompressor.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.993352 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/zstd/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2908 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/zstd/Compressor.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      310 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/zstd/Constants.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5363 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/zstd/Decompressor.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     9576 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/string_utils.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3995 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/string_utils.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      446 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/string_utils.tpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1989 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/type_utils.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.965351 clp_ffi_py-0.0.0b2/src/clp/components/core/src/utils/
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.997352 clp_ffi_py-0.0.0b2/src/clp/components/core/src/utils/make_dictionaries_readable/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      986 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/utils/make_dictionaries_readable/CommandLineArguments.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)       99 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/src/version.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.965351 clp_ffi_py-0.0.0b2/src/clp/components/core/submodules/
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.965351 clp_ffi_py-0.0.0b2/src/clp/components/core/submodules/json/
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.965351 clp_ffi_py-0.0.0b2/src/clp/components/core/submodules/json/single_include/
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.997352 clp_ffi_py-0.0.0b2/src/clp/components/core/submodules/json/single_include/nlohmann/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)   914657 2023-06-01 22:18:57.000000 clp_ffi_py-0.0.0b2/src/clp/components/core/submodules/json/single_include/nlohmann/json.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:35.997352 clp_ffi_py-0.0.0b2/src/clp_ffi_py/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1758 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/ErrorMessage.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      653 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/ExceptionFFI.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      395 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/PyObjectDeleter.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1594 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/Py_utils.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      338 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/Py_utils.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      346 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/Python.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:36.001352 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/Message.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2777 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/Message.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2250 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/Metadata.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1299 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/Metadata.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     6070 2023-07-12 05:41:21.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/PyDecoderBuffer.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1158 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/PyDecoderBuffer.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    13262 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/PyMessage.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1201 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/PyMessage.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     6076 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/PyMetadata.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      708 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/PyMetadata.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    10717 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/PyQuery.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      461 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/PyQuery.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      570 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/Query.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2663 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/Query.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     9671 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/decoding_methods.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      524 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/decoder/decoding_methods.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:36.001352 clp_ffi_py-0.0.0b2/src/clp_ffi_py/encoder/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4981 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/encoder/encoding_methods.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      572 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/encoder/encoding_methods.hpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:36.001352 clp_ffi_py-0.0.0b2/src/clp_ffi_py/modules/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3997 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/modules/clp_four_byte_encoder.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2425 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/modules/clp_ir_decoder.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2458 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/utilities.cpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1052 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/utilities.hpp
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)      960 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/src/clp_ffi_py/utilities.tpp
-drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-12 05:41:36.001352 clp_ffi_py-0.0.0b2/tests/
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)    11209 2023-07-12 04:39:07.000000 clp_ffi_py-0.0.0b2/tests/TestCase.py
--rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1174 2023-07-03 02:57:46.000000 clp_ffi_py-0.0.0b2/tests/__init__.py
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.149960 clp_ffi_py-0.0.1/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4363 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/.clang-format
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1592 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/.clang-tidy
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.029958 clp_ffi_py-0.0.1/.github/
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.057958 clp_ffi_py-0.0.1/.github/ISSUE_TEMPLATE/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1113 2023-06-14 03:44:36.000000 clp_ffi_py-0.0.1/.github/ISSUE_TEMPLATE/bug-report.yml
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)       27 2023-06-14 03:44:36.000000 clp_ffi_py-0.0.1/.github/ISSUE_TEMPLATE/config.yml
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      557 2023-06-14 03:44:36.000000 clp_ffi_py-0.0.1/.github/ISSUE_TEMPLATE/feature-request.yml
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      283 2023-06-14 03:05:42.000000 clp_ffi_py-0.0.1/.github/PULL_REQUEST_TEMPLATE.md
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.057958 clp_ffi_py-0.0.1/.github/workflows/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      759 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/.github/workflows/build_wheels.yml
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      163 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/.gitignore
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)       80 2023-07-15 18:50:38.000000 clp_ffi_py-0.0.1/.gitmodules
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    11356 2023-06-14 03:19:32.000000 clp_ffi_py-0.0.1/LICENSE
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      320 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/MANIFEST.in
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4860 2023-07-23 21:43:11.149960 clp_ffi_py-0.0.1/PKG-INFO
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4379 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/README.md
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.057958 clp_ffi_py-0.0.1/clp_ffi_py/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)        0 2023-07-21 23:42:47.000000 clp_ffi_py-0.0.1/clp_ffi_py/__init__.py
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1380 2023-07-23 19:08:57.000000 clp_ffi_py-0.0.1/clp_ffi_py/ir.pyi
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)        0 2023-06-14 03:05:42.000000 clp_ffi_py-0.0.1/clp_ffi_py/py.typed
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1129 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/clp_ffi_py/utils.py
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.057958 clp_ffi_py-0.0.1/clp_ffi_py.egg-info/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4860 2023-07-23 21:43:10.000000 clp_ffi_py-0.0.1/clp_ffi_py.egg-info/PKG-INFO
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8100 2023-07-23 21:43:11.000000 clp_ffi_py-0.0.1/clp_ffi_py.egg-info/SOURCES.txt
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)        1 2023-07-23 21:43:10.000000 clp_ffi_py-0.0.1/clp_ffi_py.egg-info/dependency_links.txt
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)       66 2023-07-23 21:43:10.000000 clp_ffi_py-0.0.1/clp_ffi_py.egg-info/requires.txt
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)       11 2023-07-23 21:43:10.000000 clp_ffi_py-0.0.1/clp_ffi_py.egg-info/top_level.txt
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1086 2023-07-23 21:42:54.000000 clp_ffi_py-0.0.1/pyproject.toml
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      195 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/requirements-dev.txt
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)       38 2023-07-23 21:43:11.149960 clp_ffi_py-0.0.1/setup.cfg
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1173 2023-07-23 19:08:57.000000 clp_ffi_py-0.0.1/setup.py
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.025957 clp_ffi_py-0.0.1/src/
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.021957 clp_ffi_py-0.0.1/src/clp/
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.021957 clp_ffi_py-0.0.1/src/clp/components/
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.025957 clp_ffi_py-0.0.1/src/clp/components/core/
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.089959 clp_ffi_py-0.0.1/src/clp/components/core/src/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5498 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ArrayBackedPosIntSet.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      914 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/CommandLineArgumentsBase.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1025 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/DictionaryEntry.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8995 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/DictionaryReader.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     9605 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/DictionaryWriter.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5003 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/EncodedVariableInterpreter.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      613 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ErrorCode.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3611 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/FileReader.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2681 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/FileWriter.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2463 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/GlobalMetadataDB.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1506 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/GlobalMetadataDBConfig.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3405 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/GlobalMySQLMetadataDB.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3184 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/GlobalSQLiteMetadataDB.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4847 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/Grep.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3297 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/LibarchiveFileReader.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5050 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/LibarchiveReader.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5344 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/LogTypeDictionaryEntry.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      423 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/LogTypeDictionaryReader.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1203 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/LogTypeDictionaryWriter.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2112 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/MessageParser.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3173 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/MySQLDB.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1427 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/MySQLParamBindings.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1657 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/MySQLPreparedStatement.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8341 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/PageAllocatedVector.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1764 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ParsedMessage.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1752 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/Platform.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     6593 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/Profiler.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     7759 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/Query.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5235 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ReaderInterface.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1222 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/SQLiteDB.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2338 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/SQLitePreparedStatement.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      474 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/Stopwatch.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2960 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/StringReader.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1511 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/Thread.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5288 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/TimestampPattern.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)       34 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/TraceableException.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1148 2023-06-03 03:52:34.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/TraceableException.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3517 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/Utils.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2247 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/VariableDictionaryEntry.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      432 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/VariableDictionaryReader.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1095 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/VariableDictionaryWriter.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1476 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/Writer.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2044 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/WriterInterface.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.105959 clp_ffi_py-0.0.1/src/clp/components/core/src/clg/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2130 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clg/CommandLineArguments.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.105959 clp_ffi_py-0.0.1/src/clp/components/core/src/clo/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1842 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clo/CommandLineArguments.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      780 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clo/ControllerMonitoringThread.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.109959 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3152 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/CommandLineArguments.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4115 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/FileCompressor.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1193 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/FileDecompressor.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      935 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/FileToCompress.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      918 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/StructuredFileToCompress.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1605 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/compression.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      568 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/decompression.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      126 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/run.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3632 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/clp/utils.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.113959 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1303 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/Constants.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    13827 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/LALR1Parser.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    32949 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/LALR1Parser.tpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     6708 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/Lexer.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    24628 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/Lexer.tpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2496 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/LogParser.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3627 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/SchemaParser.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1718 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/Token.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.117959 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    15948 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexAST.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    10255 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexAST.tpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2433 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexDFA.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1438 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexDFA.tpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4122 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexNFA.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8484 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexNFA.tpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5239 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/UnicodeIntervalTree.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8505 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/UnicodeIntervalTree.tpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      608 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/utils.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2239 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/database_utils.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      782 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/dictionary_utils.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.121960 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3955 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/encoding_methods.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    13102 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/encoding_methods.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    24981 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/encoding_methods.tpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.121960 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      323 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/byteswap.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    21845 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/decoding_methods.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5894 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/decoding_methods.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    12961 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/encoding_methods.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3080 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/encoding_methods.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2127 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/protocol_constants.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.125959 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3645 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/CompositeWildcardToken.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1929 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/ExactVariableToken.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      805 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/QueryMethodFailed.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1553 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/QueryToken.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2512 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/QueryWildcard.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1905 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/Subquery.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3281 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/WildcardToken.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1559 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/fmtlib_specializations.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      584 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/query_methods.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.125959 clp_ffi_py-0.0.1/src/clp/components/core/src/networking/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      656 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/networking/SocketOperationFailed.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1542 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/networking/socket_utils.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.125959 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2467 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/Constants.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5475 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/MetadataDB.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.137960 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5228 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/Archive.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5376 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/File.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1042 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/Message.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2329 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/Segment.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1733 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/SegmentManager.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.137960 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/writer/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    13234 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/writer/Archive.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     8361 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/writer/File.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3011 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/writer/Segment.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.141960 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1883 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/Compressor.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      324 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/Constants.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2217 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/Decompressor.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.141960 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/passthrough/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2389 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/passthrough/Compressor.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4064 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/passthrough/Decompressor.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.141960 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/zstd/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2908 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/zstd/Compressor.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      310 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/zstd/Constants.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5363 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/zstd/Decompressor.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     9576 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/string_utils.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3995 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/string_utils.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      446 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/string_utils.tpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1989 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/type_utils.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.025957 clp_ffi_py-0.0.1/src/clp/components/core/src/utils/
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.141960 clp_ffi_py-0.0.1/src/clp/components/core/src/utils/make_dictionaries_readable/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      986 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/utils/make_dictionaries_readable/CommandLineArguments.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)       99 2023-05-24 22:29:59.000000 clp_ffi_py-0.0.1/src/clp/components/core/src/version.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.025957 clp_ffi_py-0.0.1/src/clp/components/core/submodules/
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.025957 clp_ffi_py-0.0.1/src/clp/components/core/submodules/json/
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.025957 clp_ffi_py-0.0.1/src/clp/components/core/submodules/json/single_include/
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.141960 clp_ffi_py-0.0.1/src/clp/components/core/submodules/json/single_include/nlohmann/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)   914657 2023-06-01 22:18:57.000000 clp_ffi_py-0.0.1/src/clp/components/core/submodules/json/single_include/nlohmann/json.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.145960 clp_ffi_py-0.0.1/src/clp_ffi_py/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      904 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ExceptionFFI.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     3440 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/PyObjectCast.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      914 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/PyObjectUtils.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2345 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/Py_utils.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1372 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/Py_utils.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      310 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/Python.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      660 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/error_messages.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.149960 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2395 2023-07-21 00:23:46.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/LogEvent.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2744 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/Metadata.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2438 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/Metadata.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5153 2023-07-23 19:08:57.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/PyFourByteEncoder.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      966 2023-07-23 19:08:57.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/PyFourByteEncoder.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    17612 2023-07-23 19:08:57.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/PyLogEvent.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     5584 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/PyLogEvent.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    10473 2023-07-23 19:08:57.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/PyMetadata.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4447 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/PyMetadata.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     4545 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/encoding_methods.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      696 2023-07-23 19:08:57.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/encoding_methods.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)      502 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/ir/error_messages.hpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.149960 clp_ffi_py-0.0.1/src/clp_ffi_py/modules/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1531 2023-07-23 19:08:57.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/modules/ir.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1746 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/utils.cpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     2199 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/utils.hpp
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)     1128 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/src/clp_ffi_py/utils.tpp
+drwxr-xr-x   0 lzh      (1000046) lzh      (1000000)        0 2023-07-23 21:43:11.149960 clp_ffi_py-0.0.1/tests/
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)        0 2023-07-21 00:21:12.000000 clp_ffi_py-0.0.1/tests/__init__.py
+-rw-r--r--   0 lzh      (1000046) lzh      (1000000)    12632 2023-07-23 19:08:57.000000 clp_ffi_py-0.0.1/tests/test_clpir.py
```

### Comparing `clp_ffi_py-0.0.0b2/.clang-tidy` & `clp_ffi_py-0.0.1/.clang-tidy`

 * *Files 27% similar despite different names*

```diff
@@ -1,24 +1,44 @@
 ---
-Checks: 'cert-*,clang-analyzer-*,clang-diagnostic-*,cppcoreguidelines-*,modernize-*,performance-*,readability-*,-readability-identifier-length,-readability-simplify-boolean-expr'
+Checks: >- 
+  bugprone-*,
+  -bugprone-easily-swappable-parameters,
+  cert-*,
+  clang-analyzer-*,
+  clang-diagnostic-*,
+  concurrency-*,
+  cppcoreguidelines-*,
+  -cppcoreguidelines-avoid-non-const-global-variables,
+  -cppcoreguidelines-pro-type-cstyle-cast,
+  -cppcoreguidelines-pro-type-vararg,
+  misc-*,
+  modernize-*,
+  -modernize-avoid-c-arrays,
+  performance-*,
+  portability-*,
+  readability-*,
+  -readability-identifier-length,
+  -readability-simplify-boolean-expr
+
+WarningsAsErrors: >-
+  *
+
 FormatStyle: file
 CheckOptions:
   readability-identifier-naming.ClassCase: 'CamelCase'
   readability-identifier-naming.ClassMemberCase: 'lower_case'
   readability-identifier-naming.ClassMemberPrefix: 'm_'
   readability-identifier-naming.ClassMethodCase: 'lower_case'
   readability-identifier-naming.ConstexprVariableCase: 'CamelCase'
   readability-identifier-naming.ConstexprVariablePrefix: 'c'
   readability-identifier-naming.EnumCase: 'CamelCase'
   readability-identifier-naming.EnumConstantCase: 'CamelCase'
   readability-identifier-naming.GlobalConstantCase: 'CamelCase'
   readability-identifier-naming.GlobalConstantPrefix: 'c'
-  readability-identifier-naming.GlobalFunctionCase: 'lower_case'
-  readability-identifier-naming.GlobalVariableCase: 'lower_case'
   readability-identifier-naming.LocalVariableCase: 'lower_case'
   readability-identifier-naming.MemberCase: 'lower_case'
   readability-identifier-naming.MemberPrefix: 'm_'
   readability-identifier-naming.MethodCase: 'lower_case'
   readability-identifier-naming.ParameterCase: 'lower_case'
   readability-identifier-naming.StructCase: 'CamelCase'
   readability-identifier-naming.TypedefCase: 'CamelCase'
-  readability-identifier-naming.UnionCase: 'CamelCase'
+  readability-identifier-naming.UnionCase: 'CamelCase'
```

### Comparing `clp_ffi_py-0.0.0b2/.github/ISSUE_TEMPLATE/bug-report.yml` & `clp_ffi_py-0.0.1/.github/ISSUE_TEMPLATE/bug-report.yml`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/.github/ISSUE_TEMPLATE/feature-request.yml` & `clp_ffi_py-0.0.1/.github/ISSUE_TEMPLATE/feature-request.yml`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/.github/workflows/build_wheels.yml` & `clp_ffi_py-0.0.1/.github/workflows/build_wheels.yml`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -28,8 +28,8 @@
         uses: pypa/cibuildwheel@v2.12.3
         env:
           CIBW_ARCHS_LINUX: auto aarch64
           MACOSX_DEPLOYMENT_TARGET: 10.15
 
       - uses: actions/upload-artifact@v3
         with:
-          path: ./wheelhouse/*.whl
+          path: ./wheelhouse/*.whl
```

### Comparing `clp_ffi_py-0.0.0b2/LICENSE` & `clp_ffi_py-0.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/PKG-INFO` & `clp_ffi_py-0.0.1/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: clp_ffi_py
-Version: 0.0.0b2
+Version: 0.0.1
 Summary: Python interface to the CLP Core Features through CLP's FFI
 Author-email: zhihao lin <lin.zhihao@yscope.com>
 License: Apache License 2.0
 Project-URL: Homepage, https://github.com/y-scope/clp-ffi-py
 Project-URL: Bug Tracker, https://github.com/y-scope/clp-ffi-py/issues
 Classifier: License :: OSI Approved :: Apache Software License
 Requires-Python: >=3.6
@@ -51,14 +51,17 @@
 pip install -r requirements-dev.txt
 
 # 3. Pull all submodules in preparation for building
 git submodule update --init --recursive
 
 # 4. Install
 pip install -e .
+
+# 5. Run unit tests
+python -m unittest -bv
 ```
 
 ## Build and Test with cibuildwheel
 
 This project utilizes [cibuildwheel][7] configuration.
 Whenever modifications are made and committed to GitHub,
 the cibuildwheel Action will automatically initiate,
@@ -72,20 +75,27 @@
 Before submitting a pull request, run the following error-checking
 and formatting tools (found in [pyproject.toml]):
 
 * [mypy][3]: `mypy clp_ffi_py`
   * mypy checks for typing errors. You should resolve all typing errors or if an
     error cannot be resolved (e.g., it's due to a third-party library), you
     should add a comment `# type: ignore` to [silence][4] the error.
+* [docformatter][11]: `docformatter -i clp_ffi_py tests`
+  * This formats docstrings. You should review and add any changes to your PR.
 * [Black][5]: `black clp_ffi_py`
   * This formats the Python code according to Black's code-style rules. You should
     review and add any changes to your PR.
 * [clang-format][6]: `clang-format -i src/clp_ffi_py/**`
   * This formats the C++ code according to the code-style rules specified in `.clang-format`.
     You should review and add any changes to your PR.
+* [ruff][10]: `ruff check --fix clp_ffi_py tests`
+  * This performs linting according to PEPs. You should review and add any
+    changes to your PR.
+
+Note that `docformatter` should be run before `black` to give Black the [last][12].
 
 Additionally, the following tools can be useful during development. However, they cannot be installed
 using `pip`. Developers need to install them using other package management tools such as `apt-get`:
 
 * [clang-tidy][8]: `clang-tidy --extra-arg=-std=c++17 PATH_TO_THE_FILE`
   * This static analysis tool catches improper coding behaviors based on the rules specified in
     `.clang-tidy`, and sends suggestions corresponding to each warning. Developers should manually
@@ -100,7 +110,10 @@
 [3]: https://mypy.readthedocs.io/en/stable/index.html
 [4]: https://mypy.readthedocs.io/en/stable/common_issues.html#spurious-errors-and-locally-silencing-the-checker
 [5]: https://black.readthedocs.io/en/stable/index.html
 [6]: https://clang.llvm.org/docs/ClangFormatStyleOptions.html
 [7]: https://cibuildwheel.readthedocs.io/en/stable/
 [8]: https://clang.llvm.org/extra/clang-tidy/
 [9]: https://github.com/rizsotto/Bear
+[10]: https://beta.ruff.rs/docs/
+[11]: https://docformatter.readthedocs.io/en/latest/
+[12]: https://docformatter.readthedocs.io/en/latest/faq.html#interaction-with-black
```

### Comparing `clp_ffi_py-0.0.0b2/README.md` & `clp_ffi_py-0.0.1/README.md`

 * *Files 16% similar despite different names*

```diff
@@ -38,14 +38,17 @@
 pip install -r requirements-dev.txt
 
 # 3. Pull all submodules in preparation for building
 git submodule update --init --recursive
 
 # 4. Install
 pip install -e .
+
+# 5. Run unit tests
+python -m unittest -bv
 ```
 
 ## Build and Test with cibuildwheel
 
 This project utilizes [cibuildwheel][7] configuration.
 Whenever modifications are made and committed to GitHub,
 the cibuildwheel Action will automatically initiate,
@@ -59,20 +62,27 @@
 Before submitting a pull request, run the following error-checking
 and formatting tools (found in [pyproject.toml]):
 
 * [mypy][3]: `mypy clp_ffi_py`
   * mypy checks for typing errors. You should resolve all typing errors or if an
     error cannot be resolved (e.g., it's due to a third-party library), you
     should add a comment `# type: ignore` to [silence][4] the error.
+* [docformatter][11]: `docformatter -i clp_ffi_py tests`
+  * This formats docstrings. You should review and add any changes to your PR.
 * [Black][5]: `black clp_ffi_py`
   * This formats the Python code according to Black's code-style rules. You should
     review and add any changes to your PR.
 * [clang-format][6]: `clang-format -i src/clp_ffi_py/**`
   * This formats the C++ code according to the code-style rules specified in `.clang-format`.
     You should review and add any changes to your PR.
+* [ruff][10]: `ruff check --fix clp_ffi_py tests`
+  * This performs linting according to PEPs. You should review and add any
+    changes to your PR.
+
+Note that `docformatter` should be run before `black` to give Black the [last][12].
 
 Additionally, the following tools can be useful during development. However, they cannot be installed
 using `pip`. Developers need to install them using other package management tools such as `apt-get`:
 
 * [clang-tidy][8]: `clang-tidy --extra-arg=-std=c++17 PATH_TO_THE_FILE`
   * This static analysis tool catches improper coding behaviors based on the rules specified in
     `.clang-tidy`, and sends suggestions corresponding to each warning. Developers should manually
@@ -87,7 +97,10 @@
 [3]: https://mypy.readthedocs.io/en/stable/index.html
 [4]: https://mypy.readthedocs.io/en/stable/common_issues.html#spurious-errors-and-locally-silencing-the-checker
 [5]: https://black.readthedocs.io/en/stable/index.html
 [6]: https://clang.llvm.org/docs/ClangFormatStyleOptions.html
 [7]: https://cibuildwheel.readthedocs.io/en/stable/
 [8]: https://clang.llvm.org/extra/clang-tidy/
 [9]: https://github.com/rizsotto/Bear
+[10]: https://beta.ruff.rs/docs/
+[11]: https://docformatter.readthedocs.io/en/latest/
+[12]: https://docformatter.readthedocs.io/en/latest/faq.html#interaction-with-black
```

### Comparing `clp_ffi_py-0.0.0b2/clp_ffi_py/utils.py` & `clp_ffi_py-0.0.1/clp_ffi_py/utils.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,30 +1,33 @@
 import dateutil.tz
 from datetime import datetime, tzinfo
 from typing import Optional
 
 
 def get_formatted_timestamp(timestamp: int, timezone: Optional[tzinfo]) -> str:
     """
-    Gets the the formatted timestamp of the provided timestamp with the provided
-    timezone using isoformat.
-    :param timestamp: Timestamp to format
-    :param timezone: Given timezone. If None is given, UTC is used by default
-    :return: String of formatted timestamp
+    Gets the formatted timestamp string from the provided timestamp with the
+    provided timezone using isoformat.
+
+    :param timestamp: Timestamp to format.
+    :param timezone: Timezone of timestamp parameter. If None is given, UTC is
+        used by default.
+    :return: String of formatted timestamp.
     """
     if timezone is None:
         timezone = dateutil.tz.UTC
     dt: datetime = datetime.fromtimestamp(timestamp / 1000, timezone)
     return dt.isoformat(sep=" ", timespec="milliseconds")
 
 
 def get_timezone_from_timezone_id(timezone_id: str) -> tzinfo:
     """
     Gets the Python timezone object of the provided timezone id.
-    :param timezone_id
-    :raise RuntimeError: If the given timezone_id is invalid
-    :return: Timezone object
+
+    :param timezone_id: Timezone Id.
+    :return: Timezone object.
+    :raises: RuntimeError The given timestamp ID is invalid.
     """
     timezone: Optional[tzinfo] = dateutil.tz.gettz(timezone_id)
     if timezone is None:
         raise RuntimeError(f"Invalid timezone id: {timezone_id}")
     return timezone
```

### Comparing `clp_ffi_py-0.0.0b2/clp_ffi_py.egg-info/PKG-INFO` & `clp_ffi_py-0.0.1/clp_ffi_py.egg-info/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: clp-ffi-py
-Version: 0.0.0b2
+Version: 0.0.1
 Summary: Python interface to the CLP Core Features through CLP's FFI
 Author-email: zhihao lin <lin.zhihao@yscope.com>
 License: Apache License 2.0
 Project-URL: Homepage, https://github.com/y-scope/clp-ffi-py
 Project-URL: Bug Tracker, https://github.com/y-scope/clp-ffi-py/issues
 Classifier: License :: OSI Approved :: Apache Software License
 Requires-Python: >=3.6
@@ -51,14 +51,17 @@
 pip install -r requirements-dev.txt
 
 # 3. Pull all submodules in preparation for building
 git submodule update --init --recursive
 
 # 4. Install
 pip install -e .
+
+# 5. Run unit tests
+python -m unittest -bv
 ```
 
 ## Build and Test with cibuildwheel
 
 This project utilizes [cibuildwheel][7] configuration.
 Whenever modifications are made and committed to GitHub,
 the cibuildwheel Action will automatically initiate,
@@ -72,20 +75,27 @@
 Before submitting a pull request, run the following error-checking
 and formatting tools (found in [pyproject.toml]):
 
 * [mypy][3]: `mypy clp_ffi_py`
   * mypy checks for typing errors. You should resolve all typing errors or if an
     error cannot be resolved (e.g., it's due to a third-party library), you
     should add a comment `# type: ignore` to [silence][4] the error.
+* [docformatter][11]: `docformatter -i clp_ffi_py tests`
+  * This formats docstrings. You should review and add any changes to your PR.
 * [Black][5]: `black clp_ffi_py`
   * This formats the Python code according to Black's code-style rules. You should
     review and add any changes to your PR.
 * [clang-format][6]: `clang-format -i src/clp_ffi_py/**`
   * This formats the C++ code according to the code-style rules specified in `.clang-format`.
     You should review and add any changes to your PR.
+* [ruff][10]: `ruff check --fix clp_ffi_py tests`
+  * This performs linting according to PEPs. You should review and add any
+    changes to your PR.
+
+Note that `docformatter` should be run before `black` to give Black the [last][12].
 
 Additionally, the following tools can be useful during development. However, they cannot be installed
 using `pip`. Developers need to install them using other package management tools such as `apt-get`:
 
 * [clang-tidy][8]: `clang-tidy --extra-arg=-std=c++17 PATH_TO_THE_FILE`
   * This static analysis tool catches improper coding behaviors based on the rules specified in
     `.clang-tidy`, and sends suggestions corresponding to each warning. Developers should manually
@@ -100,7 +110,10 @@
 [3]: https://mypy.readthedocs.io/en/stable/index.html
 [4]: https://mypy.readthedocs.io/en/stable/common_issues.html#spurious-errors-and-locally-silencing-the-checker
 [5]: https://black.readthedocs.io/en/stable/index.html
 [6]: https://clang.llvm.org/docs/ClangFormatStyleOptions.html
 [7]: https://cibuildwheel.readthedocs.io/en/stable/
 [8]: https://clang.llvm.org/extra/clang-tidy/
 [9]: https://github.com/rizsotto/Bear
+[10]: https://beta.ruff.rs/docs/
+[11]: https://docformatter.readthedocs.io/en/latest/
+[12]: https://docformatter.readthedocs.io/en/latest/faq.html#interaction-with-black
```

### Comparing `clp_ffi_py-0.0.0b2/clp_ffi_py.egg-info/SOURCES.txt` & `clp_ffi_py-0.0.1/clp_ffi_py.egg-info/SOURCES.txt`

 * *Files 17% similar despite different names*

```diff
@@ -9,18 +9,16 @@
 requirements-dev.txt
 setup.py
 .github/PULL_REQUEST_TEMPLATE.md
 .github/ISSUE_TEMPLATE/bug-report.yml
 .github/ISSUE_TEMPLATE/config.yml
 .github/ISSUE_TEMPLATE/feature-request.yml
 .github/workflows/build_wheels.yml
-clp_ffi_py/CLPFourByteEncoder.pyi
-clp_ffi_py/CLPIRDecoder.pyi
-clp_ffi_py/FileReader.py
 clp_ffi_py/__init__.py
+clp_ffi_py/ir.pyi
 clp_ffi_py/py.typed
 clp_ffi_py/utils.py
 clp_ffi_py.egg-info/PKG-INFO
 clp_ffi_py.egg-info/SOURCES.txt
 clp_ffi_py.egg-info/dependency_links.txt
 clp_ffi_py.egg-info/requires.txt
 clp_ffi_py.egg-info/top_level.txt
@@ -139,38 +137,32 @@
 src/clp/components/core/src/streaming_compression/passthrough/Compressor.hpp
 src/clp/components/core/src/streaming_compression/passthrough/Decompressor.hpp
 src/clp/components/core/src/streaming_compression/zstd/Compressor.hpp
 src/clp/components/core/src/streaming_compression/zstd/Constants.hpp
 src/clp/components/core/src/streaming_compression/zstd/Decompressor.hpp
 src/clp/components/core/src/utils/make_dictionaries_readable/CommandLineArguments.hpp
 src/clp/components/core/submodules/json/single_include/nlohmann/json.hpp
-src/clp_ffi_py/ErrorMessage.hpp
 src/clp_ffi_py/ExceptionFFI.hpp
-src/clp_ffi_py/PyObjectDeleter.hpp
+src/clp_ffi_py/PyObjectCast.hpp
+src/clp_ffi_py/PyObjectUtils.hpp
 src/clp_ffi_py/Py_utils.cpp
 src/clp_ffi_py/Py_utils.hpp
 src/clp_ffi_py/Python.hpp
-src/clp_ffi_py/utilities.cpp
-src/clp_ffi_py/utilities.hpp
-src/clp_ffi_py/utilities.tpp
-src/clp_ffi_py/decoder/Message.cpp
-src/clp_ffi_py/decoder/Message.hpp
-src/clp_ffi_py/decoder/Metadata.cpp
-src/clp_ffi_py/decoder/Metadata.hpp
-src/clp_ffi_py/decoder/PyDecoderBuffer.cpp
-src/clp_ffi_py/decoder/PyDecoderBuffer.hpp
-src/clp_ffi_py/decoder/PyMessage.cpp
-src/clp_ffi_py/decoder/PyMessage.hpp
-src/clp_ffi_py/decoder/PyMetadata.cpp
-src/clp_ffi_py/decoder/PyMetadata.hpp
-src/clp_ffi_py/decoder/PyQuery.cpp
-src/clp_ffi_py/decoder/PyQuery.hpp
-src/clp_ffi_py/decoder/Query.cpp
-src/clp_ffi_py/decoder/Query.hpp
-src/clp_ffi_py/decoder/decoding_methods.cpp
-src/clp_ffi_py/decoder/decoding_methods.hpp
-src/clp_ffi_py/encoder/encoding_methods.cpp
-src/clp_ffi_py/encoder/encoding_methods.hpp
-src/clp_ffi_py/modules/clp_four_byte_encoder.cpp
-src/clp_ffi_py/modules/clp_ir_decoder.cpp
-tests/TestCase.py
-tests/__init__.py
+src/clp_ffi_py/error_messages.hpp
+src/clp_ffi_py/utils.cpp
+src/clp_ffi_py/utils.hpp
+src/clp_ffi_py/utils.tpp
+src/clp_ffi_py/ir/LogEvent.hpp
+src/clp_ffi_py/ir/Metadata.cpp
+src/clp_ffi_py/ir/Metadata.hpp
+src/clp_ffi_py/ir/PyFourByteEncoder.cpp
+src/clp_ffi_py/ir/PyFourByteEncoder.hpp
+src/clp_ffi_py/ir/PyLogEvent.cpp
+src/clp_ffi_py/ir/PyLogEvent.hpp
+src/clp_ffi_py/ir/PyMetadata.cpp
+src/clp_ffi_py/ir/PyMetadata.hpp
+src/clp_ffi_py/ir/encoding_methods.cpp
+src/clp_ffi_py/ir/encoding_methods.hpp
+src/clp_ffi_py/ir/error_messages.hpp
+src/clp_ffi_py/modules/ir.cpp
+tests/__init__.py
+tests/test_clpir.py
```

### Comparing `clp_ffi_py-0.0.0b2/pyproject.toml` & `clp_ffi_py-0.0.1/pyproject.toml`

 * *Files 25% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
-requires = ["setuptools >= 57.0", "setuptools_scm", "wheel"]
+requires = ["setuptools >= 59.0", "setuptools_scm", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "clp_ffi_py"
-version = "0.0.0.beta.2"
+version = "0.0.1"
 license = { text = "Apache License 2.0" }
 authors = [
     { name="zhihao lin", email="lin.zhihao@yscope.com" },
 ]
 description = "Python interface to the CLP Core Features through CLP's FFI"
 readme = "README.md"
 requires-python = ">=3.6"
@@ -21,21 +21,30 @@
 "License :: OSI Approved :: Apache Software License",
 ]
 
 [project.urls]
 "Homepage" = "https://github.com/y-scope/clp-ffi-py"
 "Bug Tracker" = "https://github.com/y-scope/clp-ffi-py/issues"
 
-[tool.setuptools_scm]
-
-[tool.mypy]
-strict = true
-pretty = true
-
 [tool.black]
 line-length = 100
 target-version = ["py311"]
 color = true
 preview = true
 
 [tool.cibuildwheel.macos]
 archs = ["x86_64", "universal2", "arm64"]
+
+[tool.docformatter]
+make-summary-multi-line = true
+pre-summary-newline = true
+recursive = true
+wrap-summaries = 80
+wrap-descriptions = 80
+
+[tool.mypy]
+strict = true
+pretty = true
+
+[tool.ruff]
+line-length = 100
+
```

### Comparing `clp_ffi_py-0.0.0b2/setup.py` & `clp_ffi_py-0.0.1/setup.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,93 +1,40 @@
 import os
 from setuptools import setup, Extension
 
-clp_four_byte_encoder: Extension = Extension(
-    name="clp_ffi_py.CLPFourByteEncoder",
+ir: Extension = Extension(
+    name="clp_ffi_py.ir",
     language="c++",
     include_dirs=[
         "src"
     ],
     sources=[
+        "src/clp/components/core/src/ffi/ir_stream/decoding_methods.cpp",
         "src/clp/components/core/src/ffi/ir_stream/encoding_methods.cpp",
         "src/clp/components/core/src/ffi/encoding_methods.cpp",
         "src/clp/components/core/src/string_utils.cpp",
         "src/clp/components/core/src/TraceableException.cpp",
-        "src/clp_ffi_py/modules/clp_four_byte_encoder.cpp",
-        "src/clp_ffi_py/encoder/encoding_methods.cpp"
-    ],
-    extra_compile_args=[
-        '-std=c++17',
-        "-O3"
-    ],
-    define_macros=[
-        ("SOURCE_PATH_SIZE", 256)
-    ]
-)
-
-clp_ir_decoder: Extension = Extension(
-    name="clp_ffi_py.CLPIRDecoder",
-    language="c++",
-    include_dirs=[
-        "src"
-    ],
-    sources=[
-        "src/clp/components/core/src/TraceableException.cpp",
-        "src/clp/components/core/src/ffi/encoding_methods.cpp",
-        "src/clp/components/core/src/string_utils.cpp",
-        "src/clp/components/core/src/ffi/ir_stream/decoding_methods.cpp",
-        "src/clp_ffi_py/modules/clp_ir_decoder.cpp",
-        "src/clp_ffi_py/decoder/decoding_methods.cpp",
-        "src/clp_ffi_py/decoder/PyDecoderBuffer.cpp",
-        "src/clp_ffi_py/decoder/Message.cpp",
-        "src/clp_ffi_py/decoder/Metadata.cpp",
-        "src/clp_ffi_py/decoder/PyMessage.cpp",
-        "src/clp_ffi_py/decoder/PyMetadata.cpp",
-        "src/clp_ffi_py/decoder/PyQuery.cpp",
-        "src/clp_ffi_py/decoder/Query.cpp",
-        "src/clp_ffi_py/utilities.cpp",
-        "src/clp_ffi_py/Py_utils.cpp",
-    ],
-    extra_compile_args=[
-        '-std=c++17',
-        "-O3"
-    ],
-    define_macros=[
-        ("SOURCE_PATH_SIZE", 256)
-    ]
-)
 
-ir: Extension = Extension(
-    name="clp_ffi_py.IRComponents",
-    language="c++",
-    include_dirs=[
-        "src"
-    ],
-    sources=[
-        "src/clp/components/core/src/TraceableException.cpp",
-        "src/clp/components/core/src/string_utils.cpp",
-        "src/clp_ffi_py/modules/ir_components.cpp",
-        "src/clp_ffi_py/decoder/Message.cpp",
-        "src/clp_ffi_py/decoder/Metadata.cpp",
-        "src/clp_ffi_py/decoder/PyMessage.cpp",
-        "src/clp_ffi_py/decoder/PyMetadata.cpp",
-        "src/clp_ffi_py/decoder/PyQuery.cpp",
-        "src/clp_ffi_py/decoder/Query.cpp",
-        "src/clp_ffi_py/utilities.cpp",
+        "src/clp_ffi_py/ir/encoding_methods.cpp",
+        "src/clp_ffi_py/ir/Metadata.cpp",
+        "src/clp_ffi_py/ir/PyFourByteEncoder.cpp",
+        "src/clp_ffi_py/ir/PyLogEvent.cpp",
+        "src/clp_ffi_py/ir/PyMetadata.cpp",
+        "src/clp_ffi_py/modules/ir.cpp",
         "src/clp_ffi_py/Py_utils.cpp",
+        "src/clp_ffi_py/utils.cpp",
     ],
     extra_compile_args=[
         '-std=c++17',
-        "-O3"
+        "-O3",
     ],
     define_macros=[
-        ("SOURCE_PATH_SIZE", 256)
+        ("SOURCE_PATH_SIZE", str(len(os.path.abspath("./src/clp/components/core"))))
     ]
 )
 
-
 setup(
     name="clp_ffi_py",
     description="CLP FFI Python Interface",
-    ext_modules=[clp_ir_decoder, clp_four_byte_encoder],
+    ext_modules=[ir],
     packages=["clp_ffi_py"],
 )
```

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ArrayBackedPosIntSet.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ArrayBackedPosIntSet.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/CommandLineArgumentsBase.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/CommandLineArgumentsBase.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/DictionaryEntry.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/DictionaryEntry.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/DictionaryReader.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/DictionaryReader.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/DictionaryWriter.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/DictionaryWriter.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/EncodedVariableInterpreter.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/EncodedVariableInterpreter.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ErrorCode.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ErrorCode.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/FileReader.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/FileReader.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/FileWriter.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/FileWriter.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/GlobalMetadataDB.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/GlobalMetadataDB.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/GlobalMetadataDBConfig.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/GlobalMetadataDBConfig.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/GlobalMySQLMetadataDB.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/GlobalMySQLMetadataDB.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/GlobalSQLiteMetadataDB.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/GlobalSQLiteMetadataDB.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/Grep.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/Grep.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/LibarchiveFileReader.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/LibarchiveFileReader.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/LibarchiveReader.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/LibarchiveReader.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/LogTypeDictionaryEntry.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/LogTypeDictionaryEntry.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/LogTypeDictionaryWriter.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/LogTypeDictionaryWriter.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/MessageParser.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/MessageParser.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/MySQLDB.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/MySQLDB.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/MySQLParamBindings.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/MySQLParamBindings.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/MySQLPreparedStatement.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/MySQLPreparedStatement.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/PageAllocatedVector.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/PageAllocatedVector.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ParsedMessage.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ParsedMessage.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/Platform.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/Platform.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/Profiler.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/Profiler.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/Query.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/Query.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ReaderInterface.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ReaderInterface.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/SQLiteDB.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/SQLiteDB.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/SQLitePreparedStatement.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/SQLitePreparedStatement.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/StringReader.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/StringReader.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/Thread.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/Thread.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/TimestampPattern.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/TimestampPattern.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/TraceableException.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/TraceableException.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/Utils.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/Utils.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/VariableDictionaryEntry.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/VariableDictionaryEntry.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/VariableDictionaryWriter.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/VariableDictionaryWriter.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/Writer.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/Writer.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/WriterInterface.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/WriterInterface.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clg/CommandLineArguments.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clg/CommandLineArguments.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clo/CommandLineArguments.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clo/CommandLineArguments.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clo/ControllerMonitoringThread.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clo/ControllerMonitoringThread.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/CommandLineArguments.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clp/CommandLineArguments.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/FileCompressor.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clp/FileCompressor.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/FileDecompressor.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clp/FileDecompressor.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/FileToCompress.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clp/FileToCompress.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/StructuredFileToCompress.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clp/StructuredFileToCompress.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/compression.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clp/compression.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/decompression.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clp/decompression.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/clp/utils.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/clp/utils.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/Constants.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/Constants.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/LALR1Parser.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/LALR1Parser.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/LALR1Parser.tpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/LALR1Parser.tpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/Lexer.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/Lexer.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/Lexer.tpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/Lexer.tpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/LogParser.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/LogParser.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/SchemaParser.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/SchemaParser.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/Token.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/Token.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexAST.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexAST.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexAST.tpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexAST.tpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexDFA.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexDFA.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexDFA.tpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexDFA.tpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexNFA.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexNFA.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/RegexNFA.tpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/RegexNFA.tpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/UnicodeIntervalTree.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/UnicodeIntervalTree.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/finite_automata/UnicodeIntervalTree.tpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/finite_automata/UnicodeIntervalTree.tpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/compressor_frontend/utils.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/compressor_frontend/utils.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/database_utils.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/database_utils.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/dictionary_utils.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/dictionary_utils.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/encoding_methods.cpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/encoding_methods.cpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/encoding_methods.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/encoding_methods.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/encoding_methods.tpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/encoding_methods.tpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/decoding_methods.cpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/decoding_methods.cpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/decoding_methods.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/decoding_methods.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/encoding_methods.cpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/encoding_methods.cpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/encoding_methods.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/encoding_methods.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/ir_stream/protocol_constants.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/ir_stream/protocol_constants.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/CompositeWildcardToken.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/CompositeWildcardToken.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/ExactVariableToken.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/ExactVariableToken.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/QueryMethodFailed.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/QueryMethodFailed.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/QueryToken.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/QueryToken.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/QueryWildcard.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/QueryWildcard.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/Subquery.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/Subquery.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/WildcardToken.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/WildcardToken.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/fmtlib_specializations.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/fmtlib_specializations.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/ffi/search/query_methods.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/ffi/search/query_methods.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/networking/SocketOperationFailed.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/networking/SocketOperationFailed.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/networking/socket_utils.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/networking/socket_utils.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/Constants.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/Constants.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/MetadataDB.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/MetadataDB.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/Archive.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/Archive.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/File.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/File.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/Message.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/Message.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/Segment.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/Segment.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/reader/SegmentManager.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/reader/SegmentManager.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/writer/Archive.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/writer/Archive.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/writer/File.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/writer/File.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_archive/writer/Segment.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_archive/writer/Segment.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/Compressor.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/Compressor.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/Decompressor.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/Decompressor.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/passthrough/Compressor.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/passthrough/Compressor.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/passthrough/Decompressor.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/passthrough/Decompressor.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/zstd/Compressor.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/zstd/Compressor.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/streaming_compression/zstd/Decompressor.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/streaming_compression/zstd/Decompressor.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/string_utils.cpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/string_utils.cpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/string_utils.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/string_utils.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/type_utils.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/type_utils.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/src/utils/make_dictionaries_readable/CommandLineArguments.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/src/utils/make_dictionaries_readable/CommandLineArguments.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp/components/core/submodules/json/single_include/nlohmann/json.hpp` & `clp_ffi_py-0.0.1/src/clp/components/core/submodules/json/single_include/nlohmann/json.hpp`

 * *Files identical despite different names*

### Comparing `clp_ffi_py-0.0.0b2/src/clp_ffi_py/ExceptionFFI.hpp` & `clp_ffi_py-0.0.1/src/clp_ffi_py/ExceptionFFI.hpp`

 * *Files 18% similar despite different names*

```diff
@@ -1,26 +1,32 @@
 #ifndef CLP_FFI_PY_EXCEPTION_FFI
 #define CLP_FFI_PY_EXCEPTION_FFI
 
-#include <clp/components/core/src/TraceableException.hpp>
-
 #include <string>
 
+#include <clp/components/core/src/TraceableException.hpp>
+
 namespace clp_ffi_py {
+/**
+ * A class that represents a traceable exception during the native code
+ * execution. Note: for exceptions of CPython execution, please use CPython
+ * interface to set the exception instead.
+ */
 class ExceptionFFI : public TraceableException {
 public:
     ExceptionFFI(
             ErrorCode error_code,
             char const* const filename,
             int line_number,
-            std::string message)
-        : TraceableException(error_code, filename, line_number),
-          m_message(std::move(message)) {}
+            std::string message
+    )
+            : TraceableException{error_code, filename, line_number},
+              m_message{std::move(message)} {};
 
-    [[nodiscard]] char const* what() const noexcept override { return m_message.c_str(); }
+    [[nodiscard]] auto what() const noexcept -> char const* override { return m_message.c_str(); }
 
 private:
     std::string m_message;
 };
-} // namespace clp_ffi_py
+}  // namespace clp_ffi_py
 
-#endif
+#endif  // CLP_FFI_PY_EXCEPTION_FFI
```

### Comparing `clp_ffi_py-0.0.0b2/src/clp_ffi_py/Py_utils.cpp` & `clp_ffi_py-0.0.1/src/clp_ffi_py/Py_utils.cpp`

 * *Files 25% similar despite different names*

```diff
@@ -1,44 +1,67 @@
-#include <clp_ffi_py/Python.hpp> // Must always be included before any other header files
-#include <clp_ffi_py/Py_utils.hpp>
+#include <clp_ffi_py/Python.hpp>  // Must always be included before any other header file
 
-#include <clp_ffi_py/ErrorMessage.hpp>
-#include <clp_ffi_py/PyObjectDeleter.hpp>
-#include <clp_ffi_py/utilities.hpp>
+#include "Py_utils.hpp"
 
-namespace clp_ffi_py {
-static std::unique_ptr<PyObject, PyObjectDeleter<PyObject>> Py_get_formatted_timestamp;
-static std::unique_ptr<PyObject, PyObjectDeleter<PyObject>> Py_get_timezone_from_timezone_id;
+#include <clp_ffi_py/PyObjectUtils.hpp>
 
-static inline auto Py_utils_function_call(PyObject* func, PyObject* args) -> PyObject* {
-    assert(func);
+namespace clp_ffi_py {
+namespace {
+constexpr char const* const cPyFuncNameGetFormattedTimestamp{"get_formatted_timestamp"};
+PyObjectPtr<PyObject> Py_func_get_formatted_timestamp;
+
+constexpr char const* const cPyFuncNameGetTimezoneFromTimezoneId{"get_timezone_from_timezone_id"};
+PyObjectPtr<PyObject> Py_func_get_timezone_from_timezone_id;
+
+/**
+ * Wrapper of PyObject_CallObject.
+ * @param func PyObject that points to the calling function.
+ * @param args Function arguments.
+ * @return PyObject* returned from PyObject_CallObject.
+ */
+auto py_utils_function_call_wrapper(PyObject* func, PyObject* args) -> PyObject* {
     return PyObject_CallObject(func, args);
 }
+}  // namespace
 
-auto Py_utils_get_formatted_timestamp(PyObject* args) -> PyObject* {
-    return Py_utils_function_call(Py_get_formatted_timestamp.get(), args);
-}
-
-auto Py_utils_get_timezone_from_timezone_id(PyObject* args) -> PyObject* {
-    return Py_utils_function_call(Py_get_timezone_from_timezone_id.get(), args);
-}
-
-auto Py_utils_init() -> bool {
-    std::unique_ptr<PyObject, PyObjectDeleter<PyObject>> utils_module(
-            PyImport_ImportModule("clp_ffi_py.utils"));
-    auto py_utils{utils_module.get()};
+auto py_utils_init() -> bool {
+    PyObjectPtr<PyObject> const utils_module(PyImport_ImportModule("clp_ffi_py.utils"));
+    auto* py_utils{utils_module.get()};
     if (nullptr == py_utils) {
         return false;
     }
-    Py_get_timezone_from_timezone_id.reset(
-            PyObject_GetAttrString(py_utils, "get_timezone_from_timezone_id"));
-    if (nullptr == Py_get_timezone_from_timezone_id.get()) {
+
+    Py_func_get_timezone_from_timezone_id.reset(
+            PyObject_GetAttrString(py_utils, cPyFuncNameGetTimezoneFromTimezoneId)
+    );
+    if (nullptr == Py_func_get_timezone_from_timezone_id.get()) {
         return false;
     }
-    Py_get_formatted_timestamp.reset(
-            PyObject_GetAttrString(py_utils, "get_formatted_timestamp"));
-    if (nullptr == Py_get_formatted_timestamp.get()) {
+
+    Py_func_get_formatted_timestamp.reset(
+            PyObject_GetAttrString(py_utils, cPyFuncNameGetFormattedTimestamp)
+    );
+    if (nullptr == Py_func_get_formatted_timestamp.get()) {
         return false;
     }
     return true;
 }
-}
+
+auto py_utils_get_formatted_timestamp(ffi::epoch_time_ms_t timestamp, PyObject* timezone)
+        -> PyObject* {
+    PyObjectPtr<PyObject> const func_args_ptr{Py_BuildValue("LO", timestamp, timezone)};
+    auto* func_args{func_args_ptr.get()};
+    if (nullptr == func_args) {
+        return nullptr;
+    }
+    return py_utils_function_call_wrapper(Py_func_get_formatted_timestamp.get(), func_args);
+}
+
+auto py_utils_get_timezone_from_timezone_id(std::string const& timezone_id) -> PyObject* {
+    PyObjectPtr<PyObject> const func_args_ptr{Py_BuildValue("(s)", timezone_id.c_str())};
+    auto* func_args{func_args_ptr.get()};
+    if (nullptr == func_args) {
+        return nullptr;
+    }
+    return py_utils_function_call_wrapper(Py_func_get_timezone_from_timezone_id.get(), func_args);
+}
+}  // namespace clp_ffi_py
```

### Comparing `clp_ffi_py-0.0.0b2/src/clp_ffi_py/encoder/encoding_methods.cpp` & `clp_ffi_py-0.0.1/src/clp_ffi_py/ir/encoding_methods.cpp`

 * *Files 10% similar despite different names*

```diff
@@ -1,139 +1,133 @@
-#include <clp_ffi_py/Python.hpp> // Must always be included before any other header files
+#include <clp_ffi_py/Python.hpp>  // Must always be included before any other header files
 
-#include <clp_ffi_py/encoder/encoding_methods.hpp>
+#include "encoding_methods.hpp"
 
 #include <clp/components/core/src/ffi/encoding_methods.hpp>
 #include <clp/components/core/src/ffi/ir_stream/encoding_methods.hpp>
 #include <clp/components/core/src/type_utils.hpp>
 
-#include <clp_ffi_py/ErrorMessage.hpp>
+#include <clp_ffi_py/ir/error_messages.hpp>
 
-// NOLINTBEGIN(cppcoreguidelines-init-variables)
-// NOLINTBEGIN(cppcoreguidelines-pro-type-vararg)
-
-namespace clp_ffi_py::encoder::four_byte_encoding {
-auto encode_preamble(PyObject* Py_UNUSED(self), PyObject* args) -> PyObject* {
-    ffi::epoch_time_ms_t ref_timestamp;
-    char const* input_timestamp_format;
-    char const* input_timezone;
-    Py_ssize_t input_timestamp_format_size;
-    Py_ssize_t input_timezone_size;
-
-    if (0 == PyArg_ParseTuple(
-                     args,
-                     "Ls#s#",
-                     &ref_timestamp,
-                     &input_timestamp_format,
-                     &input_timestamp_format_size,
-                     &input_timezone,
-                     &input_timezone_size)) {
+namespace clp_ffi_py::ir {
+auto encode_four_byte_preamble(PyObject* Py_UNUSED(self), PyObject* args) -> PyObject* {
+    ffi::epoch_time_ms_t ref_timestamp{};
+    char const* input_timestamp_format{};
+    char const* input_timezone{};
+    Py_ssize_t input_timestamp_format_size{};
+    Py_ssize_t input_timezone_size{};
+
+    if (0
+        == PyArg_ParseTuple(
+                args,
+                "Ls#s#",
+                &ref_timestamp,
+                &input_timestamp_format,
+                &input_timestamp_format_size,
+                &input_timezone,
+                &input_timezone_size
+        ))
+    {
         return nullptr;
     }
 
-    std::string_view timestamp_format{
+    std::string_view const timestamp_format{
             input_timestamp_format,
             static_cast<size_t>(input_timestamp_format_size)};
-    std::string_view timezone{input_timezone, static_cast<size_t>(input_timezone_size)};
+    std::string_view const timezone{input_timezone, static_cast<size_t>(input_timezone_size)};
     std::vector<int8_t> ir_buf;
 
-    if (false == ffi::ir_stream::four_byte_encoding::encode_preamble(
-                         timestamp_format,
-                         {},
-                         timezone,
-                         ref_timestamp,
-                         ir_buf)) {
-        PyErr_SetString(
-                PyExc_NotImplementedError,
-                clp_ffi_py::error_messages::encoder::cPreambleError);
+    if (false
+        == ffi::ir_stream::four_byte_encoding::encode_preamble(
+                timestamp_format,
+                {},
+                timezone,
+                ref_timestamp,
+                ir_buf
+        ))
+    {
+        PyErr_SetString(PyExc_NotImplementedError, clp_ffi_py::ir::cEncodePreambleError);
         return nullptr;
     }
 
     return PyByteArray_FromStringAndSize(
             size_checked_pointer_cast<char>(ir_buf.data()),
-            static_cast<Py_ssize_t>(ir_buf.size()));
+            static_cast<Py_ssize_t>(ir_buf.size())
+    );
 }
 
-auto encode_message_and_timestamp_delta(PyObject* Py_UNUSED(self), PyObject* args) -> PyObject* {
-    ffi::epoch_time_ms_t delta;
-    char const* input_buffer;
-    Py_ssize_t input_buffer_size;
+auto encode_four_byte_message_and_timestamp_delta(PyObject* Py_UNUSED(self), PyObject* args)
+        -> PyObject* {
+    ffi::epoch_time_ms_t delta{};
+    char const* input_buffer{};
+    Py_ssize_t input_buffer_size{};
     if (0 == PyArg_ParseTuple(args, "Ly#", &delta, &input_buffer, &input_buffer_size)) {
         return nullptr;
     }
 
     std::string logtype;
     std::vector<int8_t> ir_buf;
-    std::string_view msg{input_buffer, static_cast<size_t>(input_buffer_size)};
+    std::string_view const msg{input_buffer, static_cast<size_t>(input_buffer_size)};
 
     // To avoid the frequent expansion of ir_buf,
     // allocate sufficient space in advance
     ir_buf.reserve(input_buffer_size * 2);
 
     if (false == ffi::ir_stream::four_byte_encoding::encode_message(msg, logtype, ir_buf)) {
-        PyErr_SetString(
-                PyExc_NotImplementedError,
-                clp_ffi_py::error_messages::encoder::cMessageError);
+        PyErr_SetString(PyExc_NotImplementedError, clp_ffi_py::ir::cEncodeMessageError);
         return nullptr;
     }
 
     if (false == ffi::ir_stream::four_byte_encoding::encode_timestamp(delta, ir_buf)) {
-        PyErr_SetString(
-                PyExc_NotImplementedError,
-                clp_ffi_py::error_messages::encoder::cTimestampError);
+        PyErr_SetString(PyExc_NotImplementedError, clp_ffi_py::ir::cEncodeTimestampError);
         return nullptr;
     }
 
     return PyByteArray_FromStringAndSize(
             size_checked_pointer_cast<char>(ir_buf.data()),
-            static_cast<Py_ssize_t>(ir_buf.size()));
+            static_cast<Py_ssize_t>(ir_buf.size())
+    );
 }
 
-auto encode_message(PyObject* Py_UNUSED(self), PyObject* args) -> PyObject* {
-    char const* input_buffer;
-    Py_ssize_t input_buffer_size;
+auto encode_four_byte_message(PyObject* Py_UNUSED(self), PyObject* args) -> PyObject* {
+    char const* input_buffer{};
+    Py_ssize_t input_buffer_size{};
     if (0 == PyArg_ParseTuple(args, "y#", &input_buffer, &input_buffer_size)) {
         return nullptr;
     }
 
     std::string log_type;
     std::vector<int8_t> ir_buf;
-    std::string_view msg{input_buffer, static_cast<size_t>(input_buffer_size)};
+    std::string_view const msg{input_buffer, static_cast<size_t>(input_buffer_size)};
 
-    // To avoid the frequent expansion of ir_buf,
-    // allocate sufficient space in advance
+    // To avoid frequent resize of ir_buf, allocate sufficient space in advance
     ir_buf.reserve(input_buffer_size * 2);
 
     if (false == ffi::ir_stream::four_byte_encoding::encode_message(msg, log_type, ir_buf)) {
-        PyErr_SetString(
-                PyExc_NotImplementedError,
-                clp_ffi_py::error_messages::encoder::cMessageError);
+        PyErr_SetString(PyExc_NotImplementedError, clp_ffi_py::ir::cEncodeMessageError);
         return nullptr;
     }
 
     return PyByteArray_FromStringAndSize(
             size_checked_pointer_cast<char>(ir_buf.data()),
-            static_cast<Py_ssize_t>(ir_buf.size()));
+            static_cast<Py_ssize_t>(ir_buf.size())
+    );
 }
 
-auto encode_timestamp_delta(PyObject* Py_UNUSED(self), PyObject* args) -> PyObject* {
-    ffi::epoch_time_ms_t delta;
+auto encode_four_byte_timestamp_delta(PyObject* Py_UNUSED(self), PyObject* args) -> PyObject* {
+    ffi::epoch_time_ms_t delta{};
     if (0 == PyArg_ParseTuple(args, "L", &delta)) {
         return nullptr;
     }
 
     std::vector<int8_t> ir_buf;
     if (false == ffi::ir_stream::four_byte_encoding::encode_timestamp(delta, ir_buf)) {
-        PyErr_SetString(
-                PyExc_NotImplementedError,
-                clp_ffi_py::error_messages::encoder::cTimestampError);
+        PyErr_SetString(PyExc_NotImplementedError, clp_ffi_py::ir::cEncodeTimestampError);
         return nullptr;
     }
 
     return PyByteArray_FromStringAndSize(
             size_checked_pointer_cast<char>(ir_buf.data()),
-            static_cast<Py_ssize_t>(ir_buf.size()));
+            static_cast<Py_ssize_t>(ir_buf.size())
+    );
 }
-} // namespace clp_ffi_py::encoder::four_byte_encoding
-
-// NOLINTEND(cppcoreguidelines-pro-type-vararg)
-// NOLINTEND(cppcoreguidelines-init-variables)
+}  // namespace clp_ffi_py::ir
```

### Comparing `clp_ffi_py-0.0.0b2/src/clp_ffi_py/modules/clp_four_byte_encoder.cpp` & `clp_ffi_py-0.0.1/src/clp_ffi_py/ir/PyFourByteEncoder.cpp`

 * *Files 21% similar despite different names*

```diff
@@ -1,103 +1,128 @@
-#include <clp_ffi_py/Python.hpp> // Must always be included before any other header files
-#include <clp_ffi_py/encoder/encoding_methods.hpp>
+#include <clp_ffi_py/Python.hpp>  // Must always be included before any other header files
 
-// NOLINTBEGIN(*-avoid-c-arrays)
-// NOLINTBEGIN(cppcoreguidelines-avoid-non-const-global-variables)
-// NOLINTBEGIN(modernize-use-trailing-return-type)
-// NOLINTBEGIN(readability-identifier-naming)
+#include "PyFourByteEncoder.hpp"
 
+#include <clp_ffi_py/ir/encoding_methods.hpp>
+#include <clp_ffi_py/PyObjectCast.hpp>
+#include <clp_ffi_py/utils.hpp>
+
+namespace clp_ffi_py::ir {
+namespace {
+// NOLINTNEXTLINE(cppcoreguidelines-avoid-c-arrays)
 PyDoc_STRVAR(
         cEncodePreambleDoc,
         "encode_preamble(ref_timestamp, timestamp_format, timezone)\n"
         "--\n\n"
         "Creates the encoded CLP preamble for a stream of encoded log messages"
         " using the 4-byte encoding.\n"
         ":param ref_timestamp: Reference timestamp used to calculate deltas emitted with each "
         "message.\n"
         ":param timestamp_format: Timestamp format to be use when generating the logs with a "
         "reader.\n"
         ":param timezone: Timezone in TZID format to be use when generating the timestamp "
         "from Unix epoch time.\n"
         ":raises NotImplementedError: If metadata length too large.\n"
-        ":return: The encoded preamble.\n");
+        ":return: The encoded preamble.\n"
+);
 
+// NOLINTNEXTLINE(cppcoreguidelines-avoid-c-arrays)
 PyDoc_STRVAR(
         cEncodeMessageAndTimestampDeltaDoc,
         "encode_message_and_timestamp_delta(timestamp_delta, msg)\n"
         "--\n\n"
         "Encodes the log `msg` along with the timestamp delta using the 4-byte encoding.\n"
         ":param timestamp_delta: Timestamp difference in milliseconds between the current log "
         "message and the previous log message.\n"
         ":param msg: Log message to encode.\n"
         ":raises NotImplementedError: If the log message failed to encode, or the timestamp delta "
         "exceeds the supported size.\n"
-        ":return: The encoded message and timestamp.\n");
+        ":return: The encoded message and timestamp.\n"
+);
 
+// NOLINTNEXTLINE(cppcoreguidelines-avoid-c-arrays)
 PyDoc_STRVAR(
         cEncodeMessageDoc,
         "encode_message(msg)\n"
         "--\n\n"
         "Encodes the log `msg` using the 4-byte encoding.\n"
         ":param msg: Log message to encode.\n"
         ":raises NotImplementedError: If the log message failed to encode.\n"
-        ":return: The encoded message.\n");
+        ":return: The encoded message.\n"
+);
 
+// NOLINTNEXTLINE(cppcoreguidelines-avoid-c-arrays)
 PyDoc_STRVAR(
         cEncodeTimestampDeltaDoc,
         "encode_timestamp_delta(timestamp_delta)\n"
         "--\n\n"
         "Encodes the timestamp using the 4-byte encoding.\n"
         ":param timestamp_delta: Timestamp difference in milliseconds between the current log "
         "message and the previous log message.\n"
         ":raises NotImplementedError: If the timestamp failed to encode.\n"
-        ":return: The encoded timestamp.\n");
-
-PyDoc_STRVAR(cModuleDoc, "Python interface to the CLP IR 4-byte encoding methods.");
+        ":return: The encoded timestamp.\n"
+);
 
-/**
- * Method table
- */
-static PyMethodDef encoder_method_table[]{
+// NOLINTNEXTLINE(cppcoreguidelines-avoid-c-arrays)
+PyMethodDef PyFourByteEncoder_method_table[]{
         {"encode_preamble",
-         clp_ffi_py::encoder::four_byte_encoding::encode_preamble,
-         METH_VARARGS,
+         clp_ffi_py::ir::encode_four_byte_preamble,
+         METH_VARARGS | METH_STATIC,
          static_cast<char const*>(cEncodePreambleDoc)},
 
         {"encode_message_and_timestamp_delta",
-         clp_ffi_py::encoder::four_byte_encoding::encode_message_and_timestamp_delta,
-         METH_VARARGS,
+         clp_ffi_py::ir::encode_four_byte_message_and_timestamp_delta,
+         METH_VARARGS | METH_STATIC,
          static_cast<char const*>(cEncodeMessageAndTimestampDeltaDoc)},
 
         {"encode_message",
-         clp_ffi_py::encoder::four_byte_encoding::encode_message,
-         METH_VARARGS,
+         clp_ffi_py::ir::encode_four_byte_message,
+         METH_VARARGS | METH_STATIC,
          static_cast<char const*>(cEncodeMessageDoc)},
 
         {"encode_timestamp_delta",
-         clp_ffi_py::encoder::four_byte_encoding::encode_timestamp_delta,
-         METH_VARARGS,
+         clp_ffi_py::ir::encode_four_byte_timestamp_delta,
+         METH_VARARGS | METH_STATIC,
          static_cast<char const*>(cEncodeTimestampDeltaDoc)},
 
         {nullptr, nullptr, 0, nullptr}};
 
-/**
- * Module definition
- */
-static PyModuleDef clp_four_byte_encoder{
-        PyModuleDef_HEAD_INIT,
-        "CLPFourByteEncoder",
-        static_cast<char const*>(cModuleDoc),
-        0,
-        static_cast<PyMethodDef*>(encoder_method_table)};
+// NOLINTNEXTLINE(cppcoreguidelines-avoid-c-arrays)
+PyDoc_STRVAR(
+        cPyFourByteEncoderDoc,
+        "Namespace for all CLP four byte IR encoding methods.\n\n"
+        "Methods encode bytes from the log record to create a CLP log message. This class should "
+        "never be instantiated since it only contains static methods.\n"
+);
+
+// NOLINTBEGIN(cppcoreguidelines-avoid-c-arrays, cppcoreguidelines-pro-type-const-cast)
+PyType_Slot PyFourByteEncoder_slots[]{
+        {Py_tp_methods, static_cast<void*>(PyFourByteEncoder_method_table)},
+        {Py_tp_doc, const_cast<void*>(static_cast<void const*>(cPyFourByteEncoderDoc))},
+        {0, nullptr}};
+// NOLINTEND(cppcoreguidelines-avoid-c-arrays, cppcoreguidelines-pro-type-const-cast)
 
 /**
- * Module initialization
+ * PyFourByteEncoder Python type specifications.
  */
-PyMODINIT_FUNC PyInit_CLPFourByteEncoder() {
-    return PyModule_Create(&clp_four_byte_encoder);
+PyType_Spec PyFourByteEncoder_type_spec{
+        "clp_ffi_py.ir.FourByteEncoder",
+        sizeof(PyFourByteEncoder),
+        0,
+        Py_TPFLAGS_DEFAULT,
+        static_cast<PyType_Slot*>(PyFourByteEncoder_slots)};
+}  // namespace
+
+PyObjectPtr<PyTypeObject> PyFourByteEncoder::m_py_type{nullptr};
+
+auto PyFourByteEncoder::module_level_init(PyObject* py_module) -> bool {
+    static_assert(std::is_trivially_destructible<PyFourByteEncoder>());
+    auto* type{py_reinterpret_cast<PyTypeObject>(PyType_FromSpec(&PyFourByteEncoder_type_spec))};
+    m_py_type.reset(type);
+    if (nullptr == type) {
+        return false;
+    }
+    // Explicitly set the tp_new to nullptr to mark this type non-instantiable.
+    type->tp_new = nullptr;
+    return add_python_type(type, "FourByteEncoder", py_module);
 }
-
-// NOLINTEND(readability-identifier-naming)
-// NOLINTEND(modernize-use-trailing-return-type)
-// NOLINTEND(cppcoreguidelines-avoid-non-const-global-variables)
-// NOLINTEND(*-avoid-c-arrays)
+}  // namespace clp_ffi_py::ir
```

### Comparing `clp_ffi_py-0.0.0b2/tests/TestCase.py` & `clp_ffi_py-0.0.1/tests/test_clpir.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,300 +1,319 @@
 import dateutil.tz
 import pickle
 import unittest
 
-from clp_ffi_py.CLPIRDecoder import Message, Metadata
+from clp_ffi_py.ir import FourByteEncoder, LogEvent, Metadata
 from datetime import tzinfo
 from typing import Optional
 
 
-class TestCaseBase(unittest.TestCase):
+class TestCaseMetadata(unittest.TestCase):
     """
-    Functionally abstract base class for testing handlers, etc.
-
-    Functionally abstract as we use `load_tests` to avoid adding `TestBase`
-    itself to the test suite. However, we cannot mark it as abstract as
-    `unittest` will still `__init__` an instance before `load_tests` is run (and
-    will error out if any method is marked abstract).
-    """
-
-
-class TestCaseMetadata(TestCaseBase):
+    Class for testing clp_ffi_py.ir.Metadata.
     """
-    Class for testing clp_ffi_py.CLPIRDecoder.Metadata
-    """
-
-    def check_metadata(
-        self,
-        metadata: Metadata,
-        expected_ref_timestamp: int,
-        expected_timestamp_format: str,
-        expected_timezone_id: str,
-    ) -> None:
-        """
-        Given a Metadata object, check if the content matches the reference
-        :param metadata: Metadata object to be checked
-        :param expected_ref_timestamp
-        :param expected_timestamp_format
-        :param expected_timezone_id
-        """
-        ref_timestamp: int = metadata.get_ref_timestamp()
-        timestamp_format: str = metadata.get_timestamp_format()
-        timezone_id: str = metadata.get_timezone_id()
-        self.assertEqual(
-            ref_timestamp,
-            expected_ref_timestamp,
-            f'Reference Timestamp: "{ref_timestamp}", Expected: "{expected_ref_timestamp}"',
-        )
-        self.assertEqual(
-            timestamp_format,
-            expected_timestamp_format,
-            f'Timestamp Format: "{timestamp_format}", Expected: "{expected_timestamp_format}"',
-        )
-        self.assertEqual(
-            timezone_id,
-            expected_timezone_id,
-            f'Timezone ID: "{timezone_id}", Expected: "{expected_timezone_id}"',
-        )
-
-        expected_tzinfo: Optional[tzinfo] = dateutil.tz.gettz(expected_timezone_id)
-        assert expected_tzinfo is not None
-        is_the_same_tz: bool = expected_tzinfo is metadata.timezone
-        self.assertEqual(
-            is_the_same_tz,
-            True,
-            f"Timezone does not match timezone id. Timezone ID: {timezone_id}, Timezone:"
-            f' {str(metadata.timezone)}"',
-        )
 
     def test_init(self) -> None:
         """
-        Test the initialization of Message object without using keyword
+        Test the initialization of Metadata object without using keyword.
         """
         ref_timestamp: int = 2005689603190
         timestamp_format: str = "yy/MM/dd HH:mm:ss"
         timezone_id: str = "America/Chicago"
         metadata: Metadata = Metadata(ref_timestamp, timestamp_format, timezone_id)
-        self.check_metadata(metadata, ref_timestamp, timestamp_format, timezone_id)
+        self.__check_metadata(metadata, ref_timestamp, timestamp_format, timezone_id)
 
     def test_keyword_init(self) -> None:
         """
-        Test the initialization of Message object using keyword
+        Test the initialization of Metadata object using keyword.
         """
         ref_timestamp: int = 2005689603270
         timestamp_format: str = "MM/dd/yy HH:mm:ss"
         timezone_id: str = "America/New_York"
         metadata: Metadata
 
         metadata = Metadata(
             ref_timestamp=ref_timestamp, timestamp_format=timestamp_format, timezone_id=timezone_id
         )
-        self.check_metadata(metadata, ref_timestamp, timestamp_format, timezone_id)
+        self.__check_metadata(metadata, ref_timestamp, timestamp_format, timezone_id)
 
         metadata = Metadata(
             timestamp_format=timestamp_format, ref_timestamp=ref_timestamp, timezone_id=timezone_id
         )
-        self.check_metadata(metadata, ref_timestamp, timestamp_format, timezone_id)
+        self.__check_metadata(metadata, ref_timestamp, timestamp_format, timezone_id)
 
-    def test_timezone_readonly(self) -> None:
+    def test_timezone_new_reference(self) -> None:
         """
-        Test the timezone is properly set as readonly and will trigger exception
-        for any modification
+        Test the timezone is a new reference returned.
         """
         ref_timestamp: int = 2005689603190
         timestamp_format: str = "yy/MM/dd HH:mm:ss"
         timezone_id: str = "America/Chicago"
         metadata: Metadata = Metadata(ref_timestamp, timestamp_format, timezone_id)
-        self.check_metadata(metadata, ref_timestamp, timestamp_format, timezone_id)
+        self.__check_metadata(metadata, ref_timestamp, timestamp_format, timezone_id)
 
-        exception_captured: bool
-        wrong_tz: Optional[tzinfo]
+        wrong_tz: Optional[tzinfo] = metadata.get_timezone()
+        self.assertEqual(wrong_tz is metadata.get_timezone(), True)
 
-        exception_captured = False
         wrong_tz = dateutil.tz.gettz("America/New_York")
-        try:
-            assert wrong_tz is not None
-            metadata.timezone = wrong_tz
-        except AttributeError:
-            exception_captured = True
-        self.assertEqual(
-            exception_captured, True, "Timezone is overwritten by another valid tzinfo object"
-        )
-
-        exception_captured = False
-        wrong_tz = metadata.timezone
-        try:
-            assert wrong_tz is not None
-            metadata.timezone = wrong_tz
-        except AttributeError:
-            exception_captured = True
-        self.assertEqual(exception_captured, True, "Timezone is overwritten by itself")
-
-        exception_captured = False
-        try:
-            metadata.timezone = None  # type: ignore
-        except AttributeError:
-            exception_captured = True
-        self.assertEqual(exception_captured, True, "Timezone is overwritten by None")
+        self.assertEqual(wrong_tz is not metadata.get_timezone(), True)
 
+        self.__check_metadata(metadata, ref_timestamp, timestamp_format, timezone_id)
 
-class TestCaseMessage(TestCaseBase):
-    """
-    Class for testing clp_ffi_py.CLPIRDecoder.Message
-    """
-
-    def check_message(
+    def __check_metadata(
         self,
-        msg: Message,
-        expected_log_message: str,
-        expected_timestamp: int,
-        expected_msg_idx: int,
+        metadata: Metadata,
+        expected_ref_timestamp: int,
+        expected_timestamp_format: str,
+        expected_timezone_id: str,
     ) -> None:
         """
-        Given a Message object, check if the content matches the reference
-        :param msg: Message object to be checked
-        :param expected_log_message
-        :param expected_timestamp
-        :param expected_msg_idx
-        """
-        log_message: str = msg.get_message()
-        timestamp: int = msg.get_timestamp()
-        msg_idx: int = msg.get_message_idx()
+        Given a Metadata object, check if the content matches the reference.
+
+        :param metadata: Metadata object to be checked.
+        :param expected_ref_timestamp: Expected reference timestamp.
+        :param expected_timestamp_format: Expected timestamp format.
+        :param expected_timezone_id: Expected timezone ID.
+        """
+        ref_timestamp: int = metadata.get_ref_timestamp()
+        timestamp_format: str = metadata.get_timestamp_format()
+        timezone_id: str = metadata.get_timezone_id()
+        timezone: tzinfo = metadata.get_timezone()
+
         self.assertEqual(
-            log_message,
-            expected_log_message,
-            f'Log message: "{log_message}", Expected: "{expected_log_message}"',
+            ref_timestamp,
+            expected_ref_timestamp,
+            f'Reference Timestamp: "{ref_timestamp}", Expected: "{expected_ref_timestamp}"',
         )
         self.assertEqual(
-            timestamp,
-            expected_timestamp,
-            f'Timestamp: "{timestamp}", Expected: "{expected_log_message}"',
+            timestamp_format,
+            expected_timestamp_format,
+            f'Timestamp Format: "{timestamp_format}", Expected: "{expected_timestamp_format}"',
         )
         self.assertEqual(
-            msg_idx, expected_msg_idx, f"Message idx: {msg_idx}, Expected: {expected_msg_idx}"
+            timezone_id,
+            expected_timezone_id,
+            f'Timezone ID: "{timezone_id}", Expected: "{expected_timezone_id}"',
         )
 
+        expected_tzinfo: Optional[tzinfo] = dateutil.tz.gettz(expected_timezone_id)
+        assert expected_tzinfo is not None
+        is_the_same_tz: bool = expected_tzinfo is timezone
+        self.assertEqual(
+            is_the_same_tz,
+            True,
+            f"Timezone does not match timezone id. Timezone ID: {timezone_id}, Timezone:"
+            f' {str(timezone)}"',
+        )
+
+
+class TestCaseLogEvent(unittest.TestCase):
+    """
+    Class for testing clp_ffi_py.ir.LogEvent.
+    """
+
     def test_init(self) -> None:
         """
-        Test the initialization of Message object without using keyword
+        Test the initialization of LogEvent object without using keyword.
         """
         log_message: str = " This is a test log message"
         timestamp: int = 2005689603190
-        msg_idx: int = 3270
+        idx: int = 3270
         metadata: Optional[Metadata] = None
 
-        msg: Message
+        log_event: LogEvent
 
-        msg = Message(log_message, timestamp, msg_idx, metadata)
-        self.check_message(msg, log_message, timestamp, msg_idx)
+        log_event = LogEvent(log_message, timestamp, idx, metadata)
+        self.__check_log_event(log_event, log_message, timestamp, idx)
 
-        msg = Message(log_message, timestamp)
-        self.check_message(msg, log_message, timestamp, 0)
+        log_event = LogEvent(log_message, timestamp)
+        self.__check_log_event(log_event, log_message, timestamp, 0)
 
     def test_keyword_init(self) -> None:
         """
-        Test the initialization of Message object using keyword
+        Test the initialization of LogEvent object using keyword.
         """
         log_message: str = " This is a test log message"
         timestamp: int = 932724000000
-        msg_idx: int = 14111813
+        idx: int = 14111813
         metadata: Optional[Metadata] = None
 
         # Initialize with keyword (in-order)
-        msg = Message(
-            message=log_message, timestamp=timestamp, message_idx=msg_idx, metadata=metadata
+        log_event = LogEvent(
+            log_message=log_message, timestamp=timestamp, index=idx, metadata=metadata
         )
-        self.check_message(msg, log_message, timestamp, msg_idx)
+        self.__check_log_event(log_event, log_message, timestamp, idx)
 
         # Initialize with keyword (out-of-order)
-        msg = Message(
-            message_idx=msg_idx, timestamp=timestamp, message=log_message, metadata=metadata
+        log_event = LogEvent(
+            index=idx, timestamp=timestamp, log_message=log_message, metadata=metadata
         )
-        self.check_message(msg, log_message, timestamp, msg_idx)
+        self.__check_log_event(log_event, log_message, timestamp, idx)
 
         # Initialize with keyword and default argument (out-of-order)
-        msg = Message(timestamp=timestamp, message=log_message)
-        self.check_message(msg, log_message, timestamp, 0)
+        log_event = LogEvent(timestamp=timestamp, log_message=log_message)
+        self.__check_log_event(log_event, log_message, timestamp, 0)
 
-    def test_raw_message(self) -> None:
+    def test_formatted_message(self) -> None:
         """
-        Test the reconstruction of the raw message. In particular, it checks if
-        the timestamp is properly formatted with the expected tzinfo
+        Test the reconstruction of the raw message.
+
+        In particular, it checks if the timestamp is properly formatted with the
+        expected tzinfo
         """
         log_message: str = " This is a test log message"
         timestamp: int = 932724000000
-        msg_idx: int = 3190
+        idx: int = 3190
         metadata: Optional[Metadata] = Metadata(0, "yy/MM/dd HH:mm:ss", "Asia/Hong_Kong")
-        msg: Message
-        expected_raw_message: str
-        raw_message: str
+        log_event: LogEvent
+        expected_formatted_message: str
+        formatted_message: str
 
         # If metadata is given, use the metadata's timezone as default
-        msg = Message(
-            message=log_message, timestamp=timestamp, message_idx=msg_idx, metadata=metadata
+        log_event = LogEvent(
+            log_message=log_message, timestamp=timestamp, index=idx, metadata=metadata
         )
-        self.check_message(msg, log_message, timestamp, msg_idx)
-        expected_raw_message = f"1999-07-23 18:00:00.000+08:00{log_message}"
-        raw_message = msg.get_raw_message()
+        self.__check_log_event(log_event, log_message, timestamp, idx)
+        expected_formatted_message = f"1999-07-23 18:00:00.000+08:00{log_message}"
+        formatted_message = log_event.get_formatted_message()
 
         self.assertEqual(
-            raw_message,
-            expected_raw_message,
-            f"Raw message: {raw_message}; Expected: {expected_raw_message}",
+            formatted_message,
+            expected_formatted_message,
+            f"Raw message: {formatted_message}; Expected: {expected_formatted_message}",
         )
 
         # If metadata is given but another timestamp is specified, use the given
         # timestamp
         test_tz: Optional[tzinfo] = dateutil.tz.gettz("America/New_York")
         assert test_tz is not None
-        expected_raw_message = f"1999-07-23 06:00:00.000-04:00{log_message}"
-        raw_message = msg.get_raw_message(test_tz)
+        expected_formatted_message = f"1999-07-23 06:00:00.000-04:00{log_message}"
+        formatted_message = log_event.get_formatted_message(test_tz)
         self.assertEqual(
-            raw_message,
-            expected_raw_message,
-            f"Raw message: {raw_message}; Expected: {expected_raw_message}",
+            formatted_message,
+            expected_formatted_message,
+            f"Raw message: {formatted_message}; Expected: {expected_formatted_message}",
         )
 
         # If the metadata is initialized as None, and no tzinfo passed in, UTC
         # will be used as default
-        msg = Message(message=log_message, timestamp=timestamp, message_idx=msg_idx, metadata=None)
-        self.check_message(msg, log_message, timestamp, msg_idx)
-        expected_raw_message = f"1999-07-23 10:00:00.000+00:00{log_message}"
-        raw_message = msg.get_raw_message()
-        self.assertEqual(
-            raw_message,
-            expected_raw_message,
-            f"Raw message: {raw_message}; Expected: {expected_raw_message}",
+        log_event = LogEvent(log_message=log_message, timestamp=timestamp, index=idx, metadata=None)
+        self.__check_log_event(log_event, log_message, timestamp, idx)
+        expected_formatted_message = f"1999-07-23 10:00:00.000+00:00{log_message}"
+        formatted_message = log_event.get_formatted_message()
+        self.assertEqual(
+            formatted_message,
+            expected_formatted_message,
+            f"Raw message: {formatted_message}; Expected: {expected_formatted_message}",
         )
 
     def test_pickle(self) -> None:
         """
-        Test the reconstruction of Message object from pickling data.
-        For unpickled Message object, even though the metadata is set to None,
+        Test the reconstruction of LogEvent object from pickling data.
+
+        For unpickled LogEvent object, even though the metadata is set to None,
         it should still format the timestamp with the original tz before
         pickling
         """
         log_message: str = " This is a test log message"
         timestamp: int = 932724000000
-        msg_idx: int = 3190
+        idx: int = 3190
         metadata: Optional[Metadata] = Metadata(0, "yy/MM/dd HH:mm:ss", "Asia/Hong_Kong")
-        msg = Message(
-            message=log_message, timestamp=timestamp, message_idx=msg_idx, metadata=metadata
+        log_event = LogEvent(
+            log_message=log_message, timestamp=timestamp, index=idx, metadata=metadata
         )
-        self.check_message(msg, log_message, timestamp, msg_idx)
-        reconstructed_msg: Message = pickle.loads(pickle.dumps(msg))
-        self.check_message(reconstructed_msg, log_message, timestamp, msg_idx)
+        self.__check_log_event(log_event, log_message, timestamp, idx)
+        reconstructed_log_event: LogEvent = pickle.loads(pickle.dumps(log_event))
+        self.__check_log_event(reconstructed_log_event, log_message, timestamp, idx)
 
-        # For unpickled Message object, even though the metadata is set to None,
-        # it should still format the timestamp with the original tz before
+        # For unpickled LogEvent object, even though the metadata is set to
+        # None, it should still format the timestamp with the original tz before
         # pickling
-        expected_raw_message = f"1999-07-23 18:00:00.000+08:00{log_message}"
-        raw_message = reconstructed_msg.get_raw_message()
+        expected_formatted_message = f"1999-07-23 18:00:00.000+08:00{log_message}"
+        formatted_message = reconstructed_log_event.get_formatted_message()
+        self.assertEqual(
+            formatted_message,
+            expected_formatted_message,
+            f"Raw message: {formatted_message}; Expected: {expected_formatted_message}",
+        )
+
+        # If we pickle it again, we should still have the same results
+        reconstructed_log_event = pickle.loads(pickle.dumps(reconstructed_log_event))
+        formatted_message = reconstructed_log_event.get_formatted_message()
         self.assertEqual(
-            raw_message,
-            expected_raw_message,
-            f"Raw message: {raw_message}; Expected: {expected_raw_message}",
+            formatted_message,
+            expected_formatted_message,
+            f"Raw message: {formatted_message}; Expected: {expected_formatted_message}",
+        )
+
+    def __check_log_event(
+        self,
+        log_event: LogEvent,
+        expected_log_message: str,
+        expected_timestamp: int,
+        expected_idx: int,
+    ) -> None:
+        """
+        Given a LogEvent object, check if the content matches the reference.
+
+        :param log_event: LogEvent object to be checked.
+        :param expected_log_message: Expected log message.
+        :param expected_timestamp: Expected timestamp.
+        :param expected_idx: Expected log event index.
+        """
+        log_message: str = log_event.get_log_message()
+        timestamp: int = log_event.get_timestamp()
+        idx: int = log_event.get_index()
+        self.assertEqual(
+            log_message,
+            expected_log_message,
+            f'Log message: "{log_message}", Expected: "{expected_log_message}"',
+        )
+        self.assertEqual(
+            timestamp,
+            expected_timestamp,
+            f'Timestamp: "{timestamp}", Expected: "{expected_log_message}"',
+        )
+        self.assertEqual(idx, expected_idx, f"Message idx: {idx}, Expected: {expected_idx}")
+
+
+class TestCaseFourByteEncoder(unittest.TestCase):
+    """
+    Class for testing clp_ffi_py.ir.FourByteEncoder.
+
+    The actual functionality should also be covered by the unittest of CLP
+    Python logging library.
+    TODO: When the decoder is implemented, add some more tests to ensure the
+    encoded bytes can be successfully decoded to recover the original log event.
+    """
+
+    def test_init(self) -> None:
+        type_error_exception_captured: bool = False
+        four_byte_encoder: FourByteEncoder
+        try:
+            four_byte_encoder = FourByteEncoder()  # noqa
+        except TypeError:
+            type_error_exception_captured = True
+        self.assertEqual(
+            type_error_exception_captured, True, "FourByteEncoder should be non-instantiable."
+        )
+
+    def test_encoding_methods_consistency(self) -> None:
+        """
+        This test checks if the result of encode_message_and_timestamp_delta is
+        consistent with the combination of encode_message and
+        encode_timestamp_delta.
+        """
+        timestamp_delta: int = -3190
+        log_message: str = "This is a test message: Do NOT Reply!"
+        encoded_message_and_ts_delta: bytearray = (
+            FourByteEncoder.encode_message_and_timestamp_delta(
+                timestamp_delta, log_message.encode()
+            )
         )
+        encoded_message: bytearray = FourByteEncoder.encode_message(log_message.encode())
+        encoded_ts_delta: bytearray = FourByteEncoder.encode_timestamp_delta(timestamp_delta)
+        self.assertEqual(encoded_message_and_ts_delta, encoded_message + encoded_ts_delta)
 
 
 if __name__ == "__main__":
     unittest.main()
```

