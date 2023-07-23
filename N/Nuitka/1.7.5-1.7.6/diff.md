# Comparing `tmp/Nuitka-1.7.5.tar.gz` & `tmp/Nuitka-1.7.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Nuitka-1.7.5.tar", last modified: Fri Jul 14 13:29:19 2023, max compression, from Unix
+gzip compressed data, was "Nuitka-1.7.6.tar", last modified: Sun Jul 23 17:50:52 2023, max compression, from Unix
```

## Comparing `Nuitka-1.7.5.tar` & `Nuitka-1.7.6.tar`

### file list

```diff
@@ -1,1807 +1,1808 @@
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)  2833663 2023-07-14 13:29:15.000000 Nuitka-1.7.5/Changelog.pdf
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   843525 2023-07-14 13:29:02.000000 Nuitka-1.7.5/Changelog.rst
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   812243 2023-07-14 13:29:09.000000 Nuitka-1.7.5/Developer_Manual.pdf
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   152515 2023-07-14 13:29:02.000000 Nuitka-1.7.5/Developer_Manual.rst
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11348 2023-07-14 13:29:02.000000 Nuitka-1.7.5/LICENSE.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1723 2023-07-14 13:29:02.000000 Nuitka-1.7.5/MANIFEST.in
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.255159 Nuitka-1.7.5/Nuitka.egg-info/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    79137 2023-07-14 13:29:18.000000 Nuitka-1.7.5/Nuitka.egg-info/PKG-INFO
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76769 2023-07-14 13:29:18.000000 Nuitka-1.7.5/Nuitka.egg-info/SOURCES.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        1 2023-07-14 13:29:18.000000 Nuitka-1.7.5/Nuitka.egg-info/dependency_links.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      393 2023-07-14 13:29:18.000000 Nuitka-1.7.5/Nuitka.egg-info/entry_points.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        1 2023-07-14 13:29:18.000000 Nuitka-1.7.5/Nuitka.egg-info/not-zip-safe
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        7 2023-07-14 13:29:18.000000 Nuitka-1.7.5/Nuitka.egg-info/top_level.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    79137 2023-07-14 13:29:18.375159 Nuitka-1.7.5/PKG-INFO
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   345695 2023-07-14 13:29:08.000000 Nuitka-1.7.5/README.pdf
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76929 2023-07-14 13:29:02.000000 Nuitka-1.7.5/README.rst
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.255159 Nuitka-1.7.5/bin/
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1135 2023-07-14 13:29:02.000000 Nuitka-1.7.5/bin/autoformat-nuitka-source
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1134 2023-07-14 13:29:02.000000 Nuitka-1.7.5/bin/check-nuitka-with-pylint
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1150 2023-07-14 13:29:02.000000 Nuitka-1.7.5/bin/compare_with_cpython
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3079 2023-07-14 13:29:02.000000 Nuitka-1.7.5/bin/compare_with_xml
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1163 2023-07-14 13:29:02.000000 Nuitka-1.7.5/bin/measure-construct-performance
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1685 2023-07-14 13:29:02.000000 Nuitka-1.7.5/bin/nuitka
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1685 2023-07-14 13:29:02.000000 Nuitka-1.7.5/bin/nuitka-run
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.255159 Nuitka-1.7.5/doc/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.255159 Nuitka-1.7.5/doc/Logo/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7321 2023-07-14 13:29:02.000000 Nuitka-1.7.5/doc/Logo/Nuitka-Logo-Horizontal.svg
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7401 2023-07-14 13:29:02.000000 Nuitka-1.7.5/doc/Logo/Nuitka-Logo-Symbol.svg
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17917 2023-07-14 13:29:02.000000 Nuitka-1.7.5/doc/Logo/Nuitka-Logo-Vertical.svg
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.255159 Nuitka-1.7.5/doc/images/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7585 2023-07-14 13:29:02.000000 Nuitka-1.7.5/doc/images/Nuitka-Logo-Horizontal.png
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4452 2023-07-14 13:29:02.000000 Nuitka-1.7.5/doc/images/Nuitka-Logo-Symbol.png
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9828 2023-07-14 13:29:02.000000 Nuitka-1.7.5/doc/images/Nuitka-Logo-Vertical.png
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31239 2023-07-14 13:29:17.000000 Nuitka-1.7.5/doc/nuitka2-run.1
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31263 2023-07-14 13:29:17.000000 Nuitka-1.7.5/doc/nuitka2.1
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31252 2023-07-14 13:29:18.000000 Nuitka-1.7.5/doc/nuitka3-run.1
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31276 2023-07-14 13:29:18.000000 Nuitka-1.7.5/doc/nuitka3.1
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.255159 Nuitka-1.7.5/lib/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4250 2023-07-14 13:29:02.000000 Nuitka-1.7.5/lib/hints.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.255159 Nuitka-1.7.5/misc/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      901 2023-07-14 13:29:02.000000 Nuitka-1.7.5/misc/nuitka-run.bat
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1038 2023-07-14 13:29:02.000000 Nuitka-1.7.5/misc/nuitka.bat
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.255159 Nuitka-1.7.5/nuitka/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7529 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Builtins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5437 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/BytecodeCaching.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3440 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Bytecodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1884 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/CacheCleanup.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11148 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Constants.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2447 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Errors.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    37438 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/MainControl.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8064 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/ModuleRegistry.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    55485 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/OptionParsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    65509 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Options.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5022 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/OutputDirectories.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14550 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/PostProcessing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5770 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Progress.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7472 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/PythonFlavors.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4061 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/PythonOperators.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12179 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/PythonVersions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9062 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Serialization.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4670 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/SourceCodeReferences.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11235 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Tracing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3395 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/TreeXML.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15235 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Variables.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2055 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/Version.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5615 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/__main__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5295 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/__past__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.255159 Nuitka-1.7.5/nuitka/build/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34131 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/Backend.scons
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8300 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/CCompilerVersion.scons
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2716 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/DataComposerInterface.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18756 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/Onefile.scons
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15698 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/SconsCaching.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31010 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/SconsCompilerSettings.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5527 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/SconsHacks.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15827 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/SconsInterface.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2671 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/SconsProgress.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12022 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/SconsSpawn.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24338 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/SconsUtils.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.235159 Nuitka-1.7.5/nuitka/build/include/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/include/nuitka/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7972 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/allocator.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3470 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/builtins.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4604 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/calling.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1977 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/checkers.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1261 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/checksum_tools.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9571 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_asyncgen.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2002 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_cell.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9325 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_coroutine.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16949 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_frame.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5972 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_function.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9136 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_generator.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1838 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_method.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7408 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/constants.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1293 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/constants_blob.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34083 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/exceptions.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3473 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/filesystem_paths.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6253 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/freelists.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    86326 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/hedley.h
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3393 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/attributes.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2663 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/boolean.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1181 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/bytearrays.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1135 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/bytes.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9335 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/calling_generated.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13140 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_eq.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10616 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_ge.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10615 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_gt.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13140 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_le.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13139 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_lt.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10616 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_ne.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1743 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/complex.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13109 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/dictionaries.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1206 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/floats.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3897 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/import_hard.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1798 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/indexes.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2941 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/ints.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9992 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/iterators.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3411 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/lists.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1633 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/lists_generated.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1328 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/mappings.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4573 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12685 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_add.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5663 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_bitand.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5641 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_bitor.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5663 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_bitxor.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5422 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_divmod.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5460 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_floordiv.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5115 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_lshift.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2799 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_matmult.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15778 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_mod.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13210 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_mult.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5791 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_olddiv.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4714 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_pow.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5115 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_rshift.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5824 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_sub.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5438 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_truediv.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15100 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_builtin_types.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8670 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_add.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3767 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_bitand.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3753 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_bitor.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3767 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_bitxor.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4846 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_floordiv.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3011 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_lshift.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2727 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_matmult.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10626 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_mod.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9201 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_mult.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5147 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_olddiv.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4349 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_pow.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3011 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_rshift.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4975 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_sub.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4826 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_truediv.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3297 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/raising.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2178 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/rangeobjects.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1146 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/richcomparisons.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1112 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/sequences.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1025 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/sets.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8419 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/slices.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1242 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/strings.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17575 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/subscripts.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5720 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helper/tuples.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14411 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/helpers.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5375 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/importing.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12979 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/incbin.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14427 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/prelude.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2870 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/printing.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1761 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/python_pgo.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2243 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/safe_string_ops.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3840 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/threading.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3144 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/tracing.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2936 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/include/nuitka/unfreezing.h
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.245159 Nuitka-1.7.5/nuitka/build/inline_copy/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/appdirs/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1097 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/appdirs/LICENSE.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24824 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/appdirs/appdirs.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/atomicwrites/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1069 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/atomicwrites/LICENSE
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6794 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/atomicwrites/atomicwrites.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/bin/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1331 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/bin/scons.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.235159 Nuitka-1.7.5/nuitka/build/inline_copy/clcache/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/clcache/clcache/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1585 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/clcache/clcache/LICENSE
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       93 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/clcache/clcache/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    65424 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/clcache/clcache/caching.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/colorama/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1491 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/colorama/LICENSE.txt
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      243 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2522 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/ansi.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10517 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/ansitowin32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1915 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/initialise.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5404 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/win32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6438 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/winterm.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/glob2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1359 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/glob2/LICENSE
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/glob2/glob2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       82 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/glob2/glob2/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6859 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/glob2/glob2/compat.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4463 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/glob2/glob2/fnmatch.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8304 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/glob2/glob2/impl.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1467 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/LICENSE.rst
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       85 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/README.rst
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2423 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2685 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/_compat.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1726 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/_identifier.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12719 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/bccache.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    65386 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/compiler.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1626 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/constants.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12281 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/debug.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1400 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/defaults.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    50849 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/environment.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4428 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/exceptions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24500 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/ext.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36528 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/filters.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9197 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/idtracking.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28559 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/lexer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17473 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/loaders.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4340 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/meta.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7308 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/nativetypes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30853 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/nodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1722 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/optimizer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35875 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/parser.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27644 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/runtime.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17080 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/sandbox.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4214 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/tests.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20501 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/utils.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3316 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/visitor.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.265159 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1466 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/LICENSE.rst
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       84 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/README.rst
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.275159 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2616 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2685 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/_compat.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1726 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/_identifier.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12719 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/bccache.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    65386 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/compiler.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1626 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/constants.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12281 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/debug.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1400 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/defaults.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    50849 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/environment.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4428 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/exceptions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24500 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/ext.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36528 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/filters.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9197 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/idtracking.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28559 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/lexer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17474 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/loaders.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4340 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/meta.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7308 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/nativetypes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30853 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/nodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1722 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/optimizer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35875 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/parser.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27644 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/runtime.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17080 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/sandbox.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4214 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/tests.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20501 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/utils.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3316 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/visitor.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.235159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.235159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.275159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    47844 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Action.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    33996 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Builder.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8083 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/CacheDir.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27693 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Conftest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6938 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Debug.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17622 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Defaults.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    96183 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Environment.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7358 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Errors.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21540 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Executor.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16000 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Job.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9589 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Memoize.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.275159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4197 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/Alias.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   121420 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/FS.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4164 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/Python.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    49503 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.275159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1950 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/BoolOption.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1950 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/EnumOption.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1950 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/ListOption.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1965 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/PackageOption.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2736 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/PathOption.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2614 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8467 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/PathList.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.275159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9314 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3131 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/aix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1989 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/cygwin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2483 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/darwin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1718 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/hpux.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1605 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/irix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2170 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/os2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4179 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/posix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1882 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/sunos.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14948 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/win32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39700 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/SConf.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12950 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/SConsign.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.275159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4810 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/C.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3751 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/Dir.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3233 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/Prog.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2011 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/RC.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14663 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.275159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14029 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/Interactive.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    52665 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/Main.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    40719 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/SConsOptions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24133 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/SConscript.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14053 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2305 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Sig.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34903 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Subst.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    40510 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Taskmaster.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2166 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/386asm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2433 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/BitKeeper.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2859 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/CVS.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18084 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/GettextCommon.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2078 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2004 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/arch.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9248 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/common.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2784 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/netframework.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14869 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/sdk.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19499 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/vc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20832 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/vs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3763 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/Perforce.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5149 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/PharLapCommon.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2290 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/RCS.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2328 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/SCCS.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2657 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/Subversion.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31283 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2379 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixc++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2267 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2681 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixf77.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2720 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixlink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2796 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/applelink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2147 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2936 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/as.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2935 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/bcc32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3432 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/c++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3785 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/cc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2777 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/cyglink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1711 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/default.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      142 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/dmd.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/docbook/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    29618 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/docbook/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3428 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/filesystem.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2681 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/g++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2433 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/g77.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1844 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gas.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3472 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4782 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gdc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2025 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gettext.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2256 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gfortran.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2460 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gnulink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2639 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hpc++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1810 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hpcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2333 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hplink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2140 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/icc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1902 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/icl.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2077 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ilink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2043 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ilink32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18600 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/install.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25816 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/intelc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3328 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/lex.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8394 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/link.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3953 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/linkloc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2309 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/m4.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2945 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/masm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6919 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mingw.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4381 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msgfmt.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4658 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msginit.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4224 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msgmerge.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2168 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mslib.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13881 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mslink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1804 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mssdk.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11380 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msvc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    72761 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msvs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6841 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mwcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3579 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mwld.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2618 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/nasm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4375 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/rmic.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2827 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/rpcgen.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2513 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgiar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1991 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgic++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1819 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgicc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2123 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgilink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2502 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4695 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunc++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1927 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/suncc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2349 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunlink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2473 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/tar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5992 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/textfile.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1831 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/tlib.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3730 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/wix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13016 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/xgettext.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3415 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/zip.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    48938 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Util.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3007 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/BoolVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3784 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/EnumVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4404 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/ListVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3557 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/PackageVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5612 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/PathVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11034 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6824 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Warnings.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1563 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8120 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3596 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_builtins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1818 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_collections.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1742 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_dbm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2465 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_hashlib.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1776 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_io.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19253 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_sets.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    44500 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_subprocess.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19664 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/cpp.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7509 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/dblite.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2107 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/exitfuncs.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.235159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53545 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Action.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34985 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Builder.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13596 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/CacheDir.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28403 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Conftest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7533 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Debug.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20988 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Defaults.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    96818 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Environment.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7752 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Errors.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22350 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Executor.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16068 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Job.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9565 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Memoize.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5239 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/Alias.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   135413 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/FS.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5758 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/Python.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    63474 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8354 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/PathList.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11500 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3180 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/aix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2227 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/cygwin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2739 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/darwin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1767 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/hpux.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1654 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/irix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1460 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/mingw.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2219 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/os2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4476 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/posix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1931 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/sunos.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4003 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/virtualenv.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16962 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/win32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    41186 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/SConf.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13880 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/SConsign.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4853 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/C.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3812 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/Dir.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3643 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/Prog.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2328 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/RC.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15053 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.285159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13779 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/Interactive.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53260 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/Main.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39394 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/SConsOptions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26467 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/SConscript.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14489 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35863 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Subst.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42204 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Taskmaster.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2211 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/386asm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18207 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/GettextCommon.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2152 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2057 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/arch.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10674 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/common.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2855 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/netframework.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15165 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/sdk.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    33537 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/vc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21762 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/vs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4464 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/PharLapCommon.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    50660 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1667 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixc++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2316 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2475 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixcxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2840 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixlink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8618 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/applelink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2226 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2978 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/as.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2977 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/bcc32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1653 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/c++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3827 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3389 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clang.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clangCommon/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      313 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clangCommon/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3631 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clangxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3444 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8494 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cyglink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1753 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/default.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/docbook/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    29765 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/docbook/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3472 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/filesystem.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1630 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/g++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1977 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gas.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3686 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2580 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gettext_tool.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2948 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gnulink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2655 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1645 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpc++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1859 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2765 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpcxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2386 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hplink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2189 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/icc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1944 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/icl.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2123 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ilink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2085 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ilink32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15791 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/install.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26195 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/intelc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13924 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/link.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4041 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/linkloc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2351 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/m4.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2987 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/masm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7808 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mingw.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4956 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msgfmt.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5235 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msginit.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4808 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msgmerge.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2475 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mslib.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14751 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mslink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1847 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mssdk.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12588 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msvc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    82939 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msvs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6883 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mwcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3663 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mwld.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2660 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/nasm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4904 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/rmic.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2877 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/rpcgen.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2567 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgiar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1652 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgic++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1868 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgicc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2088 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgicxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2176 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgilink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2366 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1658 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunc++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1976 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/suncc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5335 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/suncxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2583 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunlink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2515 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/tar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6756 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/textfile.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1873 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/tlib.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3773 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/wix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13982 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/xgettext.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3201 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/zip.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53803 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Util.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3064 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/BoolVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3818 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/EnumVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4459 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/ListVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3643 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/PackageVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5579 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/PathVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11655 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6504 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Warnings.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1647 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6869 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1784 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/_scons_dbm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19816 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/cpp.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9002 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/dblite.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2149 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/exitfuncs.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.235159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    56578 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Action.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35213 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Builder.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11061 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/CacheDir.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27408 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Conftest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7884 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Debug.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21423 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Defaults.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    97269 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Environment.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3979 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/EnvironmentValues.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7515 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Errors.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21937 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Executor.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16583 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Job.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9430 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Memoize.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5126 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/Alias.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   136271 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/FS.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6167 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/Python.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    63768 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8183 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/PathList.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12836 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3087 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/aix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2107 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/cygwin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2630 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/darwin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1674 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/hpux.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1536 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/irix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1311 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/mingw.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2076 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/os2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4356 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/posix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1805 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/sunos.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3860 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/virtualenv.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14831 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/win32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    41983 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/SConf.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14673 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/SConsign.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7394 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/C.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4357 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/Dir.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3546 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/Prog.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1972 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/RC.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15577 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.295159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13597 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/Interactive.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53509 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/Main.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42760 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/SConsOptions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26676 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/SConscript.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14272 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36753 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Subst.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    41191 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Taskmaster.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2122 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/386asm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15570 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/GettextCommon.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2014 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1943 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/arch.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13182 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/common.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2734 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/netframework.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15027 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/sdk.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    38783 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/vc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22570 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/vs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4368 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/PharLapCommon.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    32724 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1578 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixc++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2228 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2386 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixcxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2616 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixlink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7993 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/applelink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2141 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1661 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/as.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2893 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/asm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2889 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/bcc32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1567 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/c++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3742 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3296 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clang.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clangCommon/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      343 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clangCommon/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3534 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clangxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3259 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7461 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cyglink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1663 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/default.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3379 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/filesystem.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1544 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/g++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1891 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gas.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3616 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2377 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gettext_tool.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2437 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gnulink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2526 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1557 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpc++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1772 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2677 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpcxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2206 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hplink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2096 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/icc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1851 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/icl.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1954 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ilink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1995 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ilink32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19180 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/install.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25826 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/intelc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2588 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/link.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4649 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/LoadableModule.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7652 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/SharedLibrary.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6064 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3931 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkloc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2266 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/m4.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2900 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/masm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8622 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mingw.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4577 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msgfmt.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4517 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msginit.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4113 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msgmerge.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2387 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mslib.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14473 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mslink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1752 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mssdk.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12902 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msvc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    84784 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msvs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6788 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mwcc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3576 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mwld.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2573 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/nasm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4817 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/rmic.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2788 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/rpcgen.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2479 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgiar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1563 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgic++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1780 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgicc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1999 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgicxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2006 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgilink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2271 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1569 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunc++.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1888 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/suncc.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4879 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/suncxx.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2419 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunlink.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2429 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/tar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6412 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/textfile.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1786 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/tlib.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3687 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/wix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12548 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/xgettext.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4076 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/zip.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    71693 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Util.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6632 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/ConfigureCache.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15278 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/sconsign.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3134 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/BoolVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3896 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/EnumVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4672 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/ListVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3536 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/PackageVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5588 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/PathVariable.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12708 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6785 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Warnings.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      353 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4307 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1644 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/_scons_dbm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3395 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/win32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21614 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/cpp.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9295 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/dblite.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2032 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/exitfuncs.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1467 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/LICENSE.rst
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/markupsafe/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10126 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/markupsafe/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      558 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/markupsafe/_compat.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4690 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/markupsafe/_constants.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1873 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/markupsafe/_native.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.235159 Nuitka-1.7.5/nuitka/build/inline_copy/pkg_resources/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/pkg_resources/pkg_resources/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   107452 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/pkg_resources/pkg_resources/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      538 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/pkg_resources/pkg_resources/py31compat.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.235159 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1591 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      283 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_main.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3687 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_monitor.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      283 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_tqdm.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      287 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_tqdm_gui.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      307 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_tqdm_notebook.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      888 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_tqdm_pandas.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      596 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_utils.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1106 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/auto.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      857 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/autonotebook.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1376 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/dask.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5943 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/gui.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10790 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/notebook.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    57572 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/std.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6948 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/tk.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9533 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/utils.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      333 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/version.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1101 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/LICENSE
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13170 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4883 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/composer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28639 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/constructor.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3851 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/cyaml.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2837 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/dumper.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    43006 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/emitter.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2533 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/error.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2445 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/events.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2061 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/loader.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1440 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/nodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25495 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/parser.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6794 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/reader.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14184 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/representer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8999 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/resolver.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51277 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/scanner.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4165 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/serializer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2573 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/tokens.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.305159 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1101 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/LICENSE
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.315159 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9776 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4921 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/composer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25145 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/constructor.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3290 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/cyaml.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2719 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/dumper.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    43298 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/emitter.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2559 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/error.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2445 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/events.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1132 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/loader.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1440 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/nodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25542 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/parser.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6746 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/reader.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17711 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/representer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9122 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/resolver.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    52446 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/scanner.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4171 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/serializer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2573 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/tokens.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.315159 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1101 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/LICENSE
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.315159 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9607 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4881 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/composer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25554 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/constructor.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3294 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/cyaml.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2723 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/dumper.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42954 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/emitter.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2533 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/error.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2445 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/events.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1138 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/loader.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1440 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/nodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25495 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/parser.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6854 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/reader.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14097 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/representer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8970 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/resolver.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51695 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/scanner.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4165 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/serializer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2573 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/tokens.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.315159 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1530 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/LICENSE.txt
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.315159 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18198 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/bitstream.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10157 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/compiler.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4455 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/cpu.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3763 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/debug.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13662 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/entropy_common.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3009 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/error_private.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2441 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/error_private.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34422 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/fse.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14748 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/fse_decompress.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20216 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/huf.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13930 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/mem.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26976 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/xxhash.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11706 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/xxhash.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2728 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/zstd_common.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2497 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/zstd_deps.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3828 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/zstd_errors.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15880 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/zstd_internal.h
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.315159 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    54982 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/huf_decompress.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9164 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_ddict.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1321 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_ddict.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    80283 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_decompress.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    66784 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_block.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2253 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_block.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7906 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_internal.h
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   138334 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/inline_copy/zstd/zstd.h
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.325159 Nuitka-1.7.5/nuitka/build/static_src/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    82114 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/CompiledAsyncgenType.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8250 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/CompiledCellType.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    56307 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/CompiledCodeHelpers.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    70973 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/CompiledCoroutineType.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35861 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/CompiledFrameType.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   100376 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/CompiledFunctionType.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    60649 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/CompiledGeneratorType.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    48526 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/CompiledGeneratorTypeUncompiledIntegration.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21638 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/CompiledMethodType.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18993 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersAllocator.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    37540 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersAttributes.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21783 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersBuiltin.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   107641 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersBuiltinTypeMethods.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3033 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersBytes.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13057 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersCalling.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   470655 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersCallingGenerated.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1617 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersChecksumTools.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2991 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersClasses.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   317872 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonEq.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4673 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonEqUtils.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   313003 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonGe.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   312414 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonGt.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   316217 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonLe.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   315628 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonLt.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   314618 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonNe.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36068 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersConstantsBlob.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19313 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersDeepcopy.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    38364 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersDictionaries.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24295 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersDictionariesGenerated.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7035 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersExceptions.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6668 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersFiles.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28131 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersFilesystemPaths.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2426 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersFloats.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1774 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersHeapStorage.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14585 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersImport.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14756 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersImportHard.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18433 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersLists.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13915 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersListsGenerated.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1640 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersMappings.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3513 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersMatching.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   181243 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryAdd.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16700 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryAddUtils.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    77943 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryBitand.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    77782 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryBitor.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    77943 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryBitxor.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    67487 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryDivmod.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1236 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryDivmodUtils.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    68748 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryFloordiv.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6274 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryInplaceAdd.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    83405 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryLshift.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13776 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryMatmult.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   183202 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryMod.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   188514 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryMult.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3404 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryMultUtils.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    66453 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryOlddiv.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    78891 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryPow.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1023 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryPowUtils.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    77305 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryRshift.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    70465 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinarySub.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    68005 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryTruediv.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   149580 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceAdd.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4071 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceAddUtils.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53224 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceBitand.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53122 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceBitor.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53224 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceBitxor.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76512 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceFloordiv.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    47568 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceLshift.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17742 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceMatmult.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   136100 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceMod.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   142211 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceMult.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    74142 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceOlddiv.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    82669 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplacePow.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    45052 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceRshift.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    82842 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceSub.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76343 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceTruediv.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3219 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersProfiling.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3805 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersPythonPgo.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15369 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersRaising.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3758 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersSafeStrings.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3730 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersSequences.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1946 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersSlices.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26642 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersStrings.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4037 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersTuples.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5578 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/HelpersTypes.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11986 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/InspectPatcher.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    47833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/MainProgram.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    58634 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/MetaPathBasedLoader.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4537 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/MetaPathBasedLoaderImportlibMetadataDistribution.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6427 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/MetaPathBasedLoaderResourceReader.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17285 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/MetaPathBasedLoaderResourceReaderFiles.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30910 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/OnefileBootstrap.c
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8021 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/build/static_src/OnefileSplashScreen.cpp
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.325159 Nuitka-1.7.5/nuitka/code_generation/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6414 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/AsyncgenCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10599 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/AttributeCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21864 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/BinaryOperationHelperDefinitions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2339 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/BranchCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16009 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/BuiltinCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35905 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/CallCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4896 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ClassCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51441 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/CodeGeneration.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2375 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/CodeHelperSelection.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14392 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/CodeHelpers.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4879 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/CodeObjectCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17570 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ComparisonCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4446 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ComparisonHelperDefinitions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7335 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ConditionalCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6539 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ConstantCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31186 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/Contexts.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8484 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/CoroutineCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1574 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/CtypesCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28478 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/DictCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2125 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/Emission.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9325 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ErrorCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12304 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/EvalCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8975 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ExceptionCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7350 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ExpressionCTypeSelectionHelpers.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2093 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ExpressionCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17725 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/FrameCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27968 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/FunctionCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7690 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/GeneratorCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5943 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/GlobalConstants.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6911 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/GlobalsLocalsCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1794 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/IdCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13318 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ImportCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1396 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/Indentation.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1506 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/IndexCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1033 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/InjectCCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3432 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/IntegerCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12010 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/IteratorCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2022 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/LabelCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2612 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/LineNumberCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15906 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ListCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6375 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/LoaderCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9951 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/LocalsDictCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3135 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/LoopCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1597 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/MatchCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6291 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ModuleCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8118 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/Namify.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12777 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/OperationCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    29459 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/PackageResourceCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3021 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/PrintCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5474 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/PythonAPICodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13095 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/RaisingCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3443 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/Reports.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5234 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/ReturnCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6517 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/SetCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13949 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/SliceCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9809 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/StringCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8188 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/SubscriptCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11176 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/TryCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3786 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/TupleCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14717 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/VariableCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9121 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/VariableDeclarations.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8099 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/YieldCodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.325159 Nuitka-1.7.5/nuitka/code_generation/c_types/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6069 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeBases.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3399 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeBooleans.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1804 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeCFloats.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1378 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeCLongs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3610 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeModuleDictVariables.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5128 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeNuitkaBooleans.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5211 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeNuitkaInts.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3955 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeNuitkaVoids.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19628 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypePyObjectPointers.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2852 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeVoids.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/c_types/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.325159 Nuitka-1.7.5/nuitka/code_generation/templates/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2845 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesAsyncgens.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5865 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesConstants.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2921 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesCoroutines.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2290 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesExceptions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6339 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesFrames.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3321 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesFunction.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3306 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesGeneratorFunction.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2335 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesIterators.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4217 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesLoader.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21244 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesModules.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6640 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesVariables.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2475 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/TemplateDebugWrapper.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.335159 Nuitka-1.7.5/nuitka/code_generation/templates_c/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11231 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateCallsMethodPositional.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5847 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateCallsMixed.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    23760 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateCallsPositional.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5238 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateCallsPositionalMethodDescr.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1905 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateMakeListHinted.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1843 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateMakeListSmall.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2817 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperBuiltinMethodOperation.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12819 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperDictionaryCopy.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2044 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperImportHard.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2762 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperLongTools.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1544 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperObjectTools.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7197 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationBinary.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12850 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparison.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4288 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonBytes.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2088 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonFloat.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2118 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonInt.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3933 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonList.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7407 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonLong.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4292 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonStr.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3860 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonTuple.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4487 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonUnicode.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11579 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationInplace.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19317 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsBinary.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2843 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsBytes.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3635 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsCommon.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11102 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsFloat.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15380 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsInt.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2979 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsList.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10421 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsLong.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2557 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsSet.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3020 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsStr.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2984 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsTuple.c.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3173 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsUnicode.c.j2
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.335159 Nuitka-1.7.5/nuitka/containers/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1435 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/containers/Namedtuples.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6553 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/containers/OrderedDicts.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      554 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/containers/OrderedSets.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4397 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/containers/OrderedSetsFallback.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/containers/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.335159 Nuitka-1.7.5/nuitka/distutils/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1964 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/distutils/Build.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14219 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/distutils/DistutilCommands.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/distutils/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.335159 Nuitka-1.7.5/nuitka/finalizations/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1224 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/finalizations/Finalization.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6110 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/finalizations/FinalizeMarkups.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/finalizations/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.335159 Nuitka-1.7.5/nuitka/freezer/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7311 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/DependsExe.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2584 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/DllDependenciesCommon.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11494 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/DllDependenciesMacOS.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7211 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/DllDependenciesPosix.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6620 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/DllDependenciesWin32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17058 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/IncludedDataFiles.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9492 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/IncludedEntryPoints.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9015 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/Onefile.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26319 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/Standalone.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/freezer/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.335159 Nuitka-1.7.5/nuitka/importing/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11007 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/importing/IgnoreListing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2899 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/importing/ImportCache.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6719 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/importing/ImportResolving.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28463 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/importing/Importing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4738 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/importing/PreloadedPackages.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14918 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/importing/Recursion.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10981 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/importing/StandardLibrary.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/importing/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/nodes/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3637 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/AsyncgenNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4082 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/AttributeLookupNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13567 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/AttributeNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   378745 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/AttributeNodesGenerated.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3823 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinAllNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4098 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinAnyNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2496 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinComplexNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1698 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinDecodingNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2727 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinDecoratorNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4694 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinDictNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4948 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinFormatNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2142 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinHashNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5334 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinIntegerNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12723 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinIteratorNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1996 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinLenNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3606 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinNextNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3240 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinOpenNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   245536 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinOperationNodeBasesGenerated.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18589 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinRangeNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9067 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinRefNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3307 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinSumNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13543 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinTypeNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1573 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BuiltinVarsNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26113 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/BytesNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6478 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/CallNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1550 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/Checkers.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   604445 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ChildrenHavingMixins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8448 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ClassNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6585 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/CodeObjectSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21683 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ComparisonNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30314 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ConditionalNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    46536 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ConstantRefNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12213 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ContainerMakingNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2834 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ContainerOperationNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4581 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/CoroutineNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1714 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/CtypesNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51021 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/DictionaryNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7856 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ExceptionNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7317 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ExecEvalNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    44996 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ExpressionBases.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    49273 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ExpressionBasesGenerated.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21278 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ExpressionShapeMixins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12156 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/FrameNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3544 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/FunctionAttributeNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39803 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/FunctionNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5376 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/FutureSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6256 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/GeneratorNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6850 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/GlobalsLocalsNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76798 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/HardImportNodesGenerated.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5508 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ImportHardNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    45942 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ImportNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2733 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/IndicatorMixins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1502 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/InjectCNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11228 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/IterationHandles.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11002 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/KeyValuePairNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16320 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ListOperationNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    23094 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/LocalsDictNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14922 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/LocalsScopes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15581 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/LoopNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1712 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/MatchNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6534 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ModuleAttributeNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30972 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ModuleNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24899 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/NodeBases.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15128 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/NodeMakingHelpers.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5550 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/NodeMetaClasses.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31894 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/OperatorNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9134 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/OperatorNodesUnary.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4202 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/OsSysNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12442 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/OutlineNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31534 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/PackageMetadataNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7901 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/PackageResourceNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3407 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/PrintNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6772 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/ReturnNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4715 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/SideEffectNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12501 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/SliceNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    94880 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/StatementBasesGenerated.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9430 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/StatementNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28658 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/StrNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3504 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/StringConcatenationNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8640 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/SubscriptNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17853 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/TryNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2405 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/TypeMatchNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11061 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/TypeNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39522 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/VariableAssignNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10746 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/VariableDelNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4574 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/VariableNameNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30982 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/VariableRefNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4748 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/VariableReleaseNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3902 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/YieldNodes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/nodes/shapes/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   156243 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/shapes/BuiltinTypeShapes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4387 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/shapes/ControlFlowDescriptions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4567 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/shapes/ShapeMixins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42374 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/shapes/StandardShapes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/nodes/shapes/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/optimizations/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3279 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/optimizations/BytecodeDemotion.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3920 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/optimizations/FunctionInlining.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2144 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/optimizations/Graphs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10762 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/optimizations/Optimization.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    52058 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/optimizations/OptimizeBuiltinCalls.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2272 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/optimizations/Tags.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    40896 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/optimizations/TraceCollections.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    23977 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/optimizations/ValueTraces.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/optimizations/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/pgo/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4663 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/pgo/PGO.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/pgo/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/plugins/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    40838 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/PluginBase.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    57611 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/Plugins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/plugins/standard/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22510 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/AntiBloatPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3460 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/ConsiderPyLintAnnotationsPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10383 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/DataFilesPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4404 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/DelvewheelPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5675 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/DillPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13744 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/DllFilesPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2062 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/EnumPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1905 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/EventletPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1880 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/GeventPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3482 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/GiPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5027 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/GlfwPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18335 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/ImplicitImports.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4948 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/KivyPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7239 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/MatplotlibPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6352 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/MultiprocessingPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1187 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/NumpyPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6595 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/OptionsNannyPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1917 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/PbrPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4665 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/PkgResourcesPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6992 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/PmwPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    50293 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/PySidePyQtPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2986 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/PywebViewPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1160 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/TensorflowPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12242 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/TkinterPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1140 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/TorchPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10191 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/TransformersPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1073 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/TrioPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5640 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/UpxPlugin.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   164577 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/standard.nuitka-package.config.yml
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2221 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/stdlib2.nuitka-package.config.yml
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9940 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/plugins/standard/stdlib3.nuitka-package.config.yml
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/reports/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2209 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/reports/LicenseReport.rst.j2
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17538 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/reports/Reports.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/reports/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/specs/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5911 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/BuiltinBytesOperationSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2786 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/BuiltinDictOperationSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2541 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/BuiltinListOperationSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26455 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/BuiltinParameterSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6065 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/BuiltinStrOperationSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1159 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/BuiltinTypeOperationSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4802 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/BuiltinUnicodeOperationSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5263 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/HardImportSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18740 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/ParameterSpecs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/specs/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1603 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/Basics.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/commercial/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      815 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/commercial/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/data_composer/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14250 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/data_composer/DataComposer.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/data_composer/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1306 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/data_composer/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/environments/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2449 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/environments/CreateEnvironment.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3735 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/environments/Virtualenv.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/environments/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/general/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/general/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/general/dll_report/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/general/dll_report/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2366 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/general/dll_report/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/general/find_module/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3920 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/general/find_module/FindModuleCode.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/general/find_module/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/onefile_compressor/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10194 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/onefile_compressor/OnefileCompressor.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/onefile_compressor/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1311 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/onefile_compressor/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/podman/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1872 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/podman/Podman.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/podman/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6685 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/podman/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/profiler/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/profiler/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2529 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/profiler/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/scanning/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3344 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/scanning/DisplayPackageDLLs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2095 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/scanning/DisplayPackageData.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/scanning/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/specialize/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51143 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/specialize/CTypeDescriptions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7685 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/specialize/Common.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39625 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/specialize/SpecializeC.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34664 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/specialize/SpecializePython.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/specialize/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.345159 Nuitka-1.7.5/nuitka/tools/testing/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    55396 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/Common.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1483 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/Constructs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8940 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/OutputComparison.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1278 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/Pythons.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8024 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/RuntimeTracing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5371 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/SearchModes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3375 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/Valgrind.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.355159 Nuitka-1.7.5/nuitka/tools/testing/check_reference_counts/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/check_reference_counts/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3064 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/check_reference_counts/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.355159 Nuitka-1.7.5/nuitka/tools/testing/compare_with_cpython/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/compare_with_cpython/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    29429 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/compare_with_cpython/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.355159 Nuitka-1.7.5/nuitka/tools/testing/find_sxs_modules/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/find_sxs_modules/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1949 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/find_sxs_modules/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.355159 Nuitka-1.7.5/nuitka/tools/testing/measure_construct_performance/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/measure_construct_performance/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8755 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/measure_construct_performance/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.355159 Nuitka-1.7.5/nuitka/tools/testing/run_nuitka_tests/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/run_nuitka_tests/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36321 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/testing/run_nuitka_tests/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.355159 Nuitka-1.7.5/nuitka/tools/watch/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/watch/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9503 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tools/watch/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.355159 Nuitka-1.7.5/nuitka/tree/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    47135 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/Building.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    74608 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ComplexCallHelperFunctions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1700 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/Extractions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2572 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/InternalModule.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1511 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/Operations.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2807 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationAssertStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42768 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationAssignmentStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2948 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationBooleanExpressions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11693 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationCallExpressions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15072 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationClasses.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    37638 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationClasses3.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6430 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationComparisonExpressions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22111 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationContractionExpressions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11061 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationDictionaryCreation.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14607 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationExecStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7782 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationForLoopStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    29594 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationFunctionStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13437 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationImportStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6577 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationLambdaExpressions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20962 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationMatchStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2409 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationMultidist.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8194 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationNamespacePackages.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4658 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationPrintStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15371 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationSequenceCreation.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4824 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationSubscriptExpressions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14615 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationTryExceptStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6982 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationTryFinallyStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5674 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationWhileLoopStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14341 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationWithStatements.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3088 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/ReformulationYieldExpressions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12746 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/SourceHandling.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3757 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/SyntaxErrors.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22973 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/TreeHelpers.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20012 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/VariableClosure.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/tree/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.355159 Nuitka-1.7.5/nuitka/utils/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2655 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/AppDirs.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3248 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/CStrings.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3653 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/CommandLineOptions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4297 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Distributions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5794 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Download.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12645 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Execution.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36129 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/FileOperations.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2885 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Hashing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2362 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Images.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6816 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Importing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8149 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/InstalledPythons.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2224 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/InstanceCounters.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4336 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Jinja2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1238 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Json.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4304 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/MacOSApp.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5040 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/MemoryUsage.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9062 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/ModuleNames.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4309 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/ReExecute.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3815 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Rest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22701 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/SharedLibraries.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3664 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Shebang.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2591 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Signing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6207 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/StaticLibraries.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2602 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/ThreadedExecutor.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2772 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Timing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10826 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Utils.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10574 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/WindowsFileUsage.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19540 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/WindowsResources.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6108 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/Yaml.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-14 13:29:02.000000 Nuitka-1.7.5/nuitka/utils/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      834 2023-07-14 13:29:02.000000 Nuitka-1.7.5/pyproject.toml
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       38 2023-07-14 13:29:18.375159 Nuitka-1.7.5/setup.cfg
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15624 2023-07-14 13:29:02.000000 Nuitka-1.7.5/setup.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.355159 Nuitka-1.7.5/tests/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/basics/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1766 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/AssertsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5934 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/AssignmentsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5866 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/AssignmentsTest32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4055 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/BranchingTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1104 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/BuiltinOverload.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3749 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/BuiltinSuperTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17080 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/BuiltinsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      866 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ClassMinimalTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4764 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ClassesTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3414 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ClassesTest32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1406 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ClassesTest34.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4698 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ComparisonChainsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4639 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ConstantsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      995 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ConstantsTest27.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1628 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/DecoratorsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2317 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/DefaultParametersTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1127 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/DoubleDeletionsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      806 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/EmptyModuleTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14387 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ExceptionRaisingTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      961 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ExceptionRaisingTest32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1458 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ExceptionRaisingTest33.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6747 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ExecEvalTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1417 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ExtremeClosureTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1658 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/FunctionObjectsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12335 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/FunctionsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3603 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/FunctionsTest32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2627 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/FunctionsTest_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      890 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/FutureTest32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5809 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/GeneratorExpressionsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1041 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/GeneratorExpressionsTest_37.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3824 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/GlobalStatementTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1286 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/HelloWorldTest_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2469 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ImportingTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1296 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/InplaceOperationsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4227 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/InspectionTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1504 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/InspectionTest_35.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1618 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/InspectionTest_36.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1671 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/LambdasTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2731 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/LateClosureAssignmentTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2923 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ListContractionsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3329 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/LoopingTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1536 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/MainProgramsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1925 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ModuleAttributesTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1988 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/OperatorsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14903 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/OrderChecksTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1827 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/OrderChecksTest27.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1452 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/OverflowFunctionsTest_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5853 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ParameterErrorsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1899 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ParameterErrorsTest32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      863 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/PrintFutureTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1413 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/PrintingTest_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      878 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/RecursionTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    23840 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ReferencingTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2076 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ReferencingTest27.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7819 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ReferencingTest33.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4902 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ReferencingTest35.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5092 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ReferencingTest36.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2899 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ReferencingTest_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1630 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/SlotsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1159 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/ThreadedGeneratorsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22966 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/TrickAssignmentsTest32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1541 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/TrickAssignmentsTest35.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1788 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/TrickAssignmentsTest_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2086 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/TryContinueFinallyTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2212 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/TryExceptContinueTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2275 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/TryExceptFinallyTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2304 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/TryExceptFramesTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2842 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/TryReturnFinallyTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2328 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/TryYieldFinallyTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1093 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/UnicodeTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1877 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/UnpackingTest35.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2095 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/VarargsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4879 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/WithStatementsTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3070 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/YieldFromTest33.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3821 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/run_all.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2271 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/basics/run_xml.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/onefile/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1213 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/onefile/HelloWorldTest.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1307 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/onefile/KeyboardInterruptTest.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5816 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/onefile/run_all.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/optimizations/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      958 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/ArgumentTypes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1055 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/Attributes.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1021 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/Calls.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      921 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/Conditions.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      909 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/DecodingOperations.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1212 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/FormatStrings36.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1150 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/HardImports.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      974 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/HardImports_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      918 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/Iterations.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1260 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/Len.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2262 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/Operations.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1333 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/Subscripts.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8736 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/optimizations/run_all.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/packages/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/packages/package_import_success_after_failure/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2382 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/package_import_success_after_failure/PackageImportSuccessAfterFailure.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/packages/package_import_success_after_failure/variable_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      942 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/package_import_success_after_failure/variable_package/SomeModule.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1168 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/package_import_success_after_failure/variable_package/__init__.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3671 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/run_all.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.245159 Nuitka-1.7.5/tests/packages/sub_package/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/packages/sub_package/kitty/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1230 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/sub_package/kitty/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      908 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/sub_package/kitty/bigkitty.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      910 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/sub_package/kitty/smallkitty.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/packages/sub_package/kitty/speak/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      929 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/sub_package/kitty/speak/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1053 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/sub_package/kitty/speak/hello.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      966 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/sub_package/kitty/speak/miau.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      968 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/sub_package/kitty/speak/purr.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.245159 Nuitka-1.7.5/tests/packages/top_level_attributes_3/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/packages/top_level_attributes_3/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2336 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/top_level_attributes_3/some_package/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      907 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/packages/top_level_attributes_3/some_package/some_module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/plugins/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/plugins/code_signing/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1170 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/plugins/code_signing/CodeSigningMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/plugins/data_files/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1332 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/plugins/data_files/DataFilesMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/plugins/data_files/data_files_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      924 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/plugins/data_files/data_files_package/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/plugins/data_files/data_files_package/lala.txt
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/plugins/data_files/data_files_package/sub_dir/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/plugins/data_files/data_files_package/sub_dir/lulu.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      255 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/plugins/data_files/test_case.nuitka-package.config.yml
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/plugins/parameters/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1019 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/plugins/parameters/ParametersMain.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2168 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/plugins/parameters/parameter-using-plugin.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3861 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/plugins/run_all.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/absolute_import/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      867 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/absolute_import/AbsoluteImportMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/absolute_import/foobar/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      796 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/absolute_import/foobar/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1043 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/absolute_import/foobar/foobar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      879 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/absolute_import/foobar/local.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      860 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/absolute_import/foobar/util.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports1/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      808 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports1/CasedImportingMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports1/path1/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports1/path1/Some_Module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports1/path1/Some_Package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports1/path1/Some_Package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports1/path2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports1/path2/some_module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports1/path2/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports1/path2/some_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      808 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports2/CasedImportingMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports2/path1/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports2/path1/some_module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports2/path1/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports2/path1/some_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports2/path2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports2/path2/Some_Module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports2/path2/Some_Package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports2/path2/Some_Package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports3/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1075 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports3/CasedImportingMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports3/path1/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports3/path1/Some_Module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports3/path1/Some_Package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports3/path1/Some_Package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports3/path2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports3/path2/Some_Module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/case_imports3/path2/Some_Package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/case_imports3/path2/Some_Package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/cyclic_imports/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      801 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/cyclic_imports/CyclicImportsMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/cyclic_imports/cyclic_importing_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      875 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/cyclic_imports/cyclic_importing_package/Child1.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      875 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/cyclic_imports/cyclic_importing_package/Child2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      842 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/cyclic_imports/cyclic_importing_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/dash_import/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      888 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/dash_import/DashImportMain.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      817 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/dash_import/dash-module.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      817 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/dash_import/plus+module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/dash_main/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/dash_main/Dash-Main.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/deep/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      898 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/deep/DeepProgramMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/deep/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      980 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/deep/some_package/DeepBrother.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      909 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/deep/some_package/DeepChild.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/deep/some_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/deep/some_package/deep_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      876 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/deep/some_package/deep_package/DeepDeepChild.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      952 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/deep/some_package/deep_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/dunderinit_imports/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      794 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/dunderinit_imports/DunderInitImportsMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/dunderinit_imports/package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      797 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/dunderinit_imports/package/SubModule.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      857 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/dunderinit_imports/package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/import_variants/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1005 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/import_variants/ImportVariationsMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/import_variants/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      946 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/import_variants/some_package/Child1.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1098 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/import_variants/some_package/Child2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      822 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/import_variants/some_package/Child3.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      994 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/import_variants/some_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/main_raises/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      911 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/main_raises/ErrorMain.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      808 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/main_raises/ErrorRaising.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/main_raises2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1080 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/main_raises2/ErrorInFunctionMain.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      808 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/main_raises2/ErrorRaising.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/module_attributes/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1529 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_attributes/ModuleAttributesMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/module_attributes/package_level1/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1744 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_attributes/package_level1/Nearby1.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1611 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_attributes/package_level1/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1744 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/Nearby2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1611 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/package_level3/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1744 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/package_level3/Nearby3.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1611 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/package_level3/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/module_exits/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      869 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_exits/ErrorExitingModule.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      867 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_exits/Main.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/module_object_replacing/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1078 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_object_replacing/ModuleObjectReplacingMain.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1359 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/module_object_replacing/SelfReplacingModule.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/multiprocessing_using/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      990 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/multiprocessing_using/MultiprocessingUsingMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/multiprocessing_using/foo/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/multiprocessing_using/foo/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      836 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/multiprocessing_using/foo/__main__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1758 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/multiprocessing_using/foo/entry.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/named_imports/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      846 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/named_imports/NamedImportsMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/named_imports/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/named_imports/some_package/SomeModule.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      824 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/named_imports/some_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/named_imports/some_package/sub_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/named_imports/some_package/sub_package/SomeModule.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_code/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      800 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_code/PackageInitCodeMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_code/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_code/some_package/SomeModule.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_code/some_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_contains_main/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      789 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_contains_main/PackageContainsMain.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_contains_main/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      801 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_contains_main/local.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_init_import/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      823 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_init_import/PackageInitImportMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_init_import/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1008 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_init_import/some_package/PackageLocal.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1169 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_init_import/some_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_init_issue/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      789 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_init_issue/PackageInitIssueMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_init_issue/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_init_issue/some_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_init_issue/some_package/child_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_init_issue/some_package/child_package/SomeModule.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      795 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_init_issue/some_package/child_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_missing_init/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      926 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_missing_init/PackageMissingInitMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_missing_init/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      965 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_missing_init/some_package/some_module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.365159 Nuitka-1.7.5/tests/programs/package_missing_init/some_package/sub_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      977 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_missing_init/some_package/sub_package/some_sub_module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/package_module_collision/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      901 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_module_collision/PackageAndModuleNamedSameMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/package_module_collision/Something/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_module_collision/Something/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      801 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_module_collision/something.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/package_overload/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      852 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_overload/Main.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/package_overload/foo/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_overload/foo/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_overload/foo/bar.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_overload/foo/bar2.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/package_prevents_submodule/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2972 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_prevents_submodule/PackagePreventsSubmoduleMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/package_prevents_submodule/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1078 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_prevents_submodule/some_package/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      800 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_prevents_submodule/some_package/some_module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.245159 Nuitka-1.7.5/tests/programs/package_program/
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/package_program/PackageAsMain/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      888 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_program/PackageAsMain/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1630 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/package_program/PackageAsMain/__main__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1728 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/PkgUtilIterModulesMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package1/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package1/SomeModuleC.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package1/SomeModuleD.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package1/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package2/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package2/SomeModuleA.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package2/SomeModuleB.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package2/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/pkgutil_usage/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1261 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_usage/PkgUtilUsageMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/pkgutil_usage/package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       13 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_usage/package/DATA_FILE.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       14 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_usage/package/DATA_FILE2.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       14 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_usage/package/DATA_FILE3.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1553 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/pkgutil_usage/package/__init__.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/plugin_import/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      859 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/plugin_import/PluginImportMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/plugin_import/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      771 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/plugin_import/some_package/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      781 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/plugin_import/some_package/some_module.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/reimport_main_dynamic/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      911 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/reimport_main_dynamic/ImportItselfDynamicMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/reimport_main_static/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      898 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/reimport_main_static/ImportItselfStaticMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/relative_import/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      842 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/relative_import/RelativeImportMain.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/relative_import/dircache.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/resource_reader37/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1169 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/resource_reader37/ResourceReaderMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/resource_reader37/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       13 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/resource_reader37/some_package/DATA_FILE.txt
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/resource_reader37/some_package/__init__.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6615 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/run_all.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/stdlib_overload/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1171 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/stdlib_overload/StdlibOverloadMain.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/stdlib_overload/pyexpat.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/stdlib_overload/some_package/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/stdlib_overload/some_package/__init__.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      909 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/stdlib_overload/some_package/normal_importing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/stdlib_overload/some_package/pyexpat.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1236 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/stdlib_overload/some_package/star_importing.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/syntax_errors/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      791 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/syntax_errors/IndentationErroring.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      800 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/syntax_errors/SyntaxErroring.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1079 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/syntax_errors/SyntaxErrorsMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/unicode_bom/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      963 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/unicode_bom/UnicodeBomMain.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      846 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/unicode_bom/unicode_bom.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/programs/with space/
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      826 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/programs/with space/Space Main.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/reflected/
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14061 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/reflected/compile_itself.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1243 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/run-tests
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/standalone/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1058 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/BrotliUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2554 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/CtypesUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1136 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/FlaskUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      990 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/GlfwUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1184 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/GtkUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1025 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/HexEncodingTest_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1086 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/IdnaUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1151 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/LxmlUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1431 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/MatplotlibUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2538 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/MetadataPackagesUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1727 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/NumpyUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      947 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/OpenGLUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1379 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PandasUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1066 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PasslibUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1216 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PendulumUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2074 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PkgResourcesRequiresUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1067 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PmwUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1085 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PyQt5Plugins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1105 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PyQt5SSLSupport.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2050 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PyQt5Using.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1085 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PyQt6Plugins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2050 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PyQt6Using.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1091 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PySide6Plugins.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1757 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/PySide6Using.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1323 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/RsaUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      973 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/ShlibUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1537 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/SocketUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1941 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/TkInterUsing.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3228 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/Urllib3Using.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1200 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/Win32ComUsing.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9531 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/run_all.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/standalone/zip_importer/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1264 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/standalone/zip_importer/ZipImporterMain.py
-drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-14 13:29:18.375159 Nuitka-1.7.5/tests/syntax/
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      811 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/AsyncgenReturn36.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      868 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/BreakWithoutLoop.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      791 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/ClassReturn.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      970 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/ClosureDel_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      849 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/ContinueWithoutLoop.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      791 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/DuplicateArgument.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1111 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/ExecWithNesting_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      826 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/FutureBraces.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      805 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/FutureUnknown.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1041 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/GeneratorExpressions38.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      879 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/GeneratorReturn_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      792 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/GlobalForParameter.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      995 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/Importing32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/IndentationError.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      915 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/LateFutureImport.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      841 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/MisplacedFutureImport.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      800 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/ModuleReturn.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      883 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/NonAsciiWithoutEncoding_2.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      794 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/NonlocalForParameter32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      868 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/NonlocalNotFound32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      908 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/StarImportExtra.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      869 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/SyntaxError.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      874 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/TryExceptAllNotLast.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      875 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/TryFinallyContinue_37.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      776 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/UnpackNoTuple.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/UnpackTwoStars32.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      793 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/YieldFromInModule.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      804 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/YieldInAsync35.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      923 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/YieldInGenexp38.py
--rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      781 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/YieldInModule.py
--rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2203 2023-07-14 13:29:02.000000 Nuitka-1.7.5/tests/syntax/run_all.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.974387 Nuitka-1.7.6/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)  2833663 2023-07-23 17:50:47.000000 Nuitka-1.7.6/Changelog.pdf
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   843525 2023-07-23 17:50:33.000000 Nuitka-1.7.6/Changelog.rst
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   812243 2023-07-23 17:50:41.000000 Nuitka-1.7.6/Developer_Manual.pdf
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   152515 2023-07-23 17:50:33.000000 Nuitka-1.7.6/Developer_Manual.rst
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11348 2023-07-23 17:50:33.000000 Nuitka-1.7.6/LICENSE.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1723 2023-07-23 17:50:33.000000 Nuitka-1.7.6/MANIFEST.in
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/Nuitka.egg-info/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    79087 2023-07-23 17:50:50.000000 Nuitka-1.7.6/Nuitka.egg-info/PKG-INFO
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76803 2023-07-23 17:50:50.000000 Nuitka-1.7.6/Nuitka.egg-info/SOURCES.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        1 2023-07-23 17:50:50.000000 Nuitka-1.7.6/Nuitka.egg-info/dependency_links.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      393 2023-07-23 17:50:50.000000 Nuitka-1.7.6/Nuitka.egg-info/entry_points.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        1 2023-07-23 17:50:50.000000 Nuitka-1.7.6/Nuitka.egg-info/not-zip-safe
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        7 2023-07-23 17:50:50.000000 Nuitka-1.7.6/Nuitka.egg-info/top_level.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    79087 2023-07-23 17:50:50.974387 Nuitka-1.7.6/PKG-INFO
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   345695 2023-07-23 17:50:39.000000 Nuitka-1.7.6/README.pdf
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76929 2023-07-23 17:50:33.000000 Nuitka-1.7.6/README.rst
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/bin/
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1135 2023-07-23 17:50:33.000000 Nuitka-1.7.6/bin/autoformat-nuitka-source
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1134 2023-07-23 17:50:33.000000 Nuitka-1.7.6/bin/check-nuitka-with-pylint
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1150 2023-07-23 17:50:33.000000 Nuitka-1.7.6/bin/compare_with_cpython
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3079 2023-07-23 17:50:33.000000 Nuitka-1.7.6/bin/compare_with_xml
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1163 2023-07-23 17:50:33.000000 Nuitka-1.7.6/bin/measure-construct-performance
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1685 2023-07-23 17:50:33.000000 Nuitka-1.7.6/bin/nuitka
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1685 2023-07-23 17:50:33.000000 Nuitka-1.7.6/bin/nuitka-run
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/doc/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/doc/Logo/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7321 2023-07-23 17:50:33.000000 Nuitka-1.7.6/doc/Logo/Nuitka-Logo-Horizontal.svg
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7401 2023-07-23 17:50:33.000000 Nuitka-1.7.6/doc/Logo/Nuitka-Logo-Symbol.svg
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17917 2023-07-23 17:50:33.000000 Nuitka-1.7.6/doc/Logo/Nuitka-Logo-Vertical.svg
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/doc/images/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7585 2023-07-23 17:50:33.000000 Nuitka-1.7.6/doc/images/Nuitka-Logo-Horizontal.png
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4452 2023-07-23 17:50:33.000000 Nuitka-1.7.6/doc/images/Nuitka-Logo-Symbol.png
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9828 2023-07-23 17:50:33.000000 Nuitka-1.7.6/doc/images/Nuitka-Logo-Vertical.png
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31239 2023-07-23 17:50:49.000000 Nuitka-1.7.6/doc/nuitka2-run.1
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31263 2023-07-23 17:50:49.000000 Nuitka-1.7.6/doc/nuitka2.1
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31252 2023-07-23 17:50:50.000000 Nuitka-1.7.6/doc/nuitka3-run.1
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31276 2023-07-23 17:50:50.000000 Nuitka-1.7.6/doc/nuitka3.1
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/lib/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4250 2023-07-23 17:50:33.000000 Nuitka-1.7.6/lib/hints.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/misc/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      901 2023-07-23 17:50:33.000000 Nuitka-1.7.6/misc/nuitka-run.bat
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1038 2023-07-23 17:50:33.000000 Nuitka-1.7.6/misc/nuitka.bat
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/nuitka/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7529 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Builtins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5437 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/BytecodeCaching.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3440 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Bytecodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1884 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/CacheCleanup.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11148 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Constants.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2447 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Errors.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    37438 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/MainControl.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8064 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/ModuleRegistry.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    55483 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/OptionParsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    66897 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Options.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5022 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/OutputDirectories.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14520 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/PostProcessing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5770 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Progress.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7472 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/PythonFlavors.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4061 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/PythonOperators.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12179 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/PythonVersions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9062 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Serialization.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4670 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/SourceCodeReferences.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11235 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Tracing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3395 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/TreeXML.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15235 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Variables.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2055 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/Version.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5615 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/__main__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5295 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/__past__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/nuitka/build/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34239 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/Backend.scons
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8300 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/CCompilerVersion.scons
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2716 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/DataComposerInterface.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18756 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/Onefile.scons
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15698 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/SconsCaching.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31010 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/SconsCompilerSettings.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5527 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/SconsHacks.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15827 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/SconsInterface.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2671 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/SconsProgress.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12022 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/SconsSpawn.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24338 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/SconsUtils.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.804387 Nuitka-1.7.6/nuitka/build/include/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.834387 Nuitka-1.7.6/nuitka/build/include/nuitka/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7972 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/allocator.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3470 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/builtins.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4604 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/calling.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1977 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/checkers.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1261 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/checksum_tools.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9571 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_asyncgen.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2002 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_cell.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9325 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_coroutine.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16949 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_frame.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5972 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_function.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9136 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_generator.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1838 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_method.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7408 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/constants.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1293 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/constants_blob.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34083 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/exceptions.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3473 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/filesystem_paths.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6253 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/freelists.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    86326 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/hedley.h
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3393 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/attributes.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2663 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/boolean.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1181 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/bytearrays.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1135 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/bytes.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9335 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/calling_generated.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13140 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_eq.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10616 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_ge.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10615 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_gt.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13140 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_le.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13139 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_lt.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10616 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_ne.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1743 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/complex.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13109 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/dictionaries.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1206 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/floats.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3897 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/import_hard.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1798 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/indexes.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2941 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/ints.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9992 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/iterators.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3411 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/lists.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1633 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/lists_generated.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1328 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/mappings.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4573 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12685 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_add.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5663 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_bitand.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5641 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_bitor.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5663 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_bitxor.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5422 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_divmod.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5460 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_floordiv.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5115 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_lshift.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2799 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_matmult.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15778 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_mod.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13210 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_mult.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5791 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_olddiv.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4714 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_pow.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5115 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_rshift.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5824 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_sub.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5438 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_truediv.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15100 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_builtin_types.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8670 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_add.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3767 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_bitand.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3753 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_bitor.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3767 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_bitxor.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4846 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_floordiv.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3011 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_lshift.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2727 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_matmult.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10626 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_mod.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9201 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_mult.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5147 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_olddiv.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4349 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_pow.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3011 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_rshift.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4975 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_sub.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4826 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_truediv.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3297 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/raising.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2178 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/rangeobjects.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1146 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/richcomparisons.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1112 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/sequences.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1025 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/sets.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8419 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/slices.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1242 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/strings.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17575 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/subscripts.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5720 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helper/tuples.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14521 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/helpers.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5375 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/importing.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12979 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/incbin.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14853 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/prelude.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2870 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/printing.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1761 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/python_pgo.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2243 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/safe_string_ops.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3840 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/threading.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3144 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/tracing.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2936 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/include/nuitka/unfreezing.h
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.814387 Nuitka-1.7.6/nuitka/build/inline_copy/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/appdirs/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1097 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/appdirs/LICENSE.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24824 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/appdirs/appdirs.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/atomicwrites/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1069 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/atomicwrites/LICENSE
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6794 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/atomicwrites/atomicwrites.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/bin/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1331 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/bin/scons.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.804387 Nuitka-1.7.6/nuitka/build/inline_copy/clcache/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/clcache/clcache/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1585 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/clcache/clcache/LICENSE
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       93 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/clcache/clcache/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    65424 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/clcache/clcache/caching.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/colorama/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1491 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/colorama/LICENSE.txt
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      243 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2522 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/ansi.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10517 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/ansitowin32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1915 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/initialise.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5404 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/win32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6438 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/winterm.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/glob2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1359 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/glob2/LICENSE
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/glob2/glob2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       82 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/glob2/glob2/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6859 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/glob2/glob2/compat.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4463 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/glob2/glob2/fnmatch.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8304 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/glob2/glob2/impl.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1467 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/LICENSE.rst
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       85 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/README.rst
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2423 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2685 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/_compat.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1726 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/_identifier.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12719 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/bccache.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    65386 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/compiler.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1626 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/constants.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12281 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/debug.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1400 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/defaults.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    50849 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/environment.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4428 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/exceptions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24500 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/ext.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36528 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/filters.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9197 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/idtracking.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28559 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/lexer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17473 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/loaders.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4340 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/meta.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7308 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/nativetypes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30853 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/nodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1722 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/optimizer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35875 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/parser.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27644 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/runtime.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17080 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/sandbox.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4214 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/tests.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20501 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/utils.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3316 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/visitor.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1466 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/LICENSE.rst
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       84 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/README.rst
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.844387 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2616 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2685 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/_compat.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1726 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/_identifier.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12719 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/bccache.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    65386 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/compiler.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1626 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/constants.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12281 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/debug.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1400 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/defaults.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    50849 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/environment.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4428 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/exceptions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24500 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/ext.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36528 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/filters.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9197 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/idtracking.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28559 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/lexer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17474 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/loaders.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4340 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/meta.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7308 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/nativetypes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30853 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/nodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1722 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/optimizer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35875 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/parser.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27644 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/runtime.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17080 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/sandbox.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4214 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/tests.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20501 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/utils.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3316 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/visitor.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.814387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.814387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.854387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    47844 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Action.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    33996 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Builder.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8083 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/CacheDir.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27693 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Conftest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6938 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Debug.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17622 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Defaults.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    96183 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Environment.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7358 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Errors.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21540 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Executor.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16000 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Job.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9589 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Memoize.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.854387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4197 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/Alias.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   121420 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/FS.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4164 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/Python.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    49503 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.854387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1950 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/BoolOption.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1950 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/EnumOption.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1950 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/ListOption.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1965 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/PackageOption.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2736 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/PathOption.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2614 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8467 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/PathList.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.854387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9314 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3131 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/aix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1989 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/cygwin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2483 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/darwin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1718 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/hpux.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1605 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/irix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2170 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/os2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4179 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/posix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1882 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/sunos.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14948 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/win32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39700 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/SConf.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12950 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/SConsign.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.854387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4810 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/C.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3751 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/Dir.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3233 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/Prog.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2011 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/RC.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14663 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.854387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14029 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/Interactive.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    52665 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/Main.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    40719 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/SConsOptions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24133 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/SConscript.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14053 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2305 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Sig.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34903 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Subst.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    40510 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Taskmaster.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2166 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/386asm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2433 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/BitKeeper.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2859 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/CVS.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18084 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/GettextCommon.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2078 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2004 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/arch.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9248 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/common.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2784 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/netframework.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14869 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/sdk.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19499 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/vc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20832 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/vs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3763 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/Perforce.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5149 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/PharLapCommon.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2290 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/RCS.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2328 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/SCCS.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2657 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/Subversion.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31283 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2379 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixc++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2267 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2681 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixf77.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2720 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixlink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2796 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/applelink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2147 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2936 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/as.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2935 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/bcc32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3432 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/c++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3785 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/cc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2777 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/cyglink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1711 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/default.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      142 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/dmd.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/docbook/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    29618 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/docbook/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3428 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/filesystem.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2681 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/g++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2433 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/g77.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1844 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gas.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3472 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4782 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gdc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2025 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gettext.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2256 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gfortran.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2460 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gnulink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2639 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hpc++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1810 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hpcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2333 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hplink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2140 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/icc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1902 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/icl.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2077 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ilink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2043 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ilink32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18600 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/install.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25816 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/intelc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3328 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/lex.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8394 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/link.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3953 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/linkloc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2309 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/m4.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2945 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/masm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6919 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mingw.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4381 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msgfmt.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4658 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msginit.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4224 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msgmerge.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2168 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mslib.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13881 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mslink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1804 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mssdk.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11380 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msvc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    72761 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msvs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6841 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mwcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3579 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mwld.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2618 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/nasm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4375 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/rmic.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2827 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/rpcgen.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2513 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgiar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1991 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgic++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1819 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgicc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2123 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgilink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2502 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4695 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunc++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1927 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/suncc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2349 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunlink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2473 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/tar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5992 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/textfile.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1831 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/tlib.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3730 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/wix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13016 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/xgettext.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3415 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/zip.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    48938 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Util.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3007 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/BoolVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3784 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/EnumVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4404 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/ListVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3557 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/PackageVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5612 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/PathVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11034 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6824 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Warnings.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1563 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8120 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3596 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_builtins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1818 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_collections.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1742 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_dbm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2465 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_hashlib.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1776 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_io.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19253 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_sets.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    44500 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_subprocess.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19664 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/cpp.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7509 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/dblite.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2107 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/exitfuncs.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.814387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53545 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Action.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34985 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Builder.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13596 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/CacheDir.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28403 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Conftest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7533 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Debug.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20988 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Defaults.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    96818 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Environment.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7752 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Errors.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22350 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Executor.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16068 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Job.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9565 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Memoize.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5239 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/Alias.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   135413 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/FS.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5758 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/Python.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    63474 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8354 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/PathList.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11500 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3180 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/aix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2227 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/cygwin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2739 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/darwin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1767 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/hpux.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1654 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/irix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1460 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/mingw.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2219 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/os2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4476 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/posix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1931 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/sunos.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4003 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/virtualenv.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16962 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/win32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    41186 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/SConf.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13880 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/SConsign.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4853 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/C.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3812 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/Dir.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3643 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/Prog.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2328 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/RC.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15053 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.864387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13779 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/Interactive.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53260 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/Main.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39394 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/SConsOptions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26467 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/SConscript.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14489 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35863 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Subst.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42204 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Taskmaster.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.874387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2211 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/386asm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18207 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/GettextCommon.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.874387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2152 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2057 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/arch.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10674 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/common.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2855 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/netframework.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15165 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/sdk.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    33537 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/vc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21762 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/vs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4464 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/PharLapCommon.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    50660 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1667 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixc++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2316 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2475 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixcxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2840 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixlink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8618 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/applelink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2226 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2978 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/as.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2977 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/bcc32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1653 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/c++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3827 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3389 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clang.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.874387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clangCommon/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      313 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clangCommon/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3631 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clangxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3444 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8494 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cyglink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1753 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/default.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.874387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/docbook/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    29765 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/docbook/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3472 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/filesystem.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1630 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/g++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1977 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gas.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3686 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2580 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gettext_tool.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2948 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gnulink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2655 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1645 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpc++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1859 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2765 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpcxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2386 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hplink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2189 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/icc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1944 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/icl.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2123 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ilink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2085 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ilink32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15791 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/install.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26195 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/intelc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13924 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/link.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4041 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/linkloc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2351 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/m4.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2987 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/masm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7808 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mingw.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4956 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msgfmt.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5235 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msginit.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4808 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msgmerge.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2475 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mslib.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14751 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mslink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1847 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mssdk.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12588 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msvc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    82939 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msvs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6883 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mwcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3663 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mwld.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2660 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/nasm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4904 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/rmic.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2877 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/rpcgen.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2567 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgiar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1652 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgic++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1868 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgicc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2088 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgicxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2176 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgilink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2366 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1658 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunc++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1976 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/suncc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5335 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/suncxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2583 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunlink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2515 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/tar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6756 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/textfile.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1873 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/tlib.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3773 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/wix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13982 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/xgettext.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3201 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/zip.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53803 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Util.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.874387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3064 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/BoolVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3818 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/EnumVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4459 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/ListVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3643 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/PackageVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5579 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/PathVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11655 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6504 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Warnings.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1647 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.874387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6869 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1784 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/_scons_dbm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19816 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/cpp.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9002 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/dblite.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2149 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/exitfuncs.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.814387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.874387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    56578 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Action.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35213 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Builder.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11061 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/CacheDir.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27408 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Conftest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7884 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Debug.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21423 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Defaults.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    97269 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Environment.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3979 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/EnvironmentValues.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7515 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Errors.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21937 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Executor.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16583 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Job.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9430 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Memoize.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.874387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5126 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/Alias.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   136271 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/FS.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6167 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/Python.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    63768 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8183 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/PathList.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.874387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12836 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3087 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/aix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2107 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/cygwin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2630 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/darwin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1674 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/hpux.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1536 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/irix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1311 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/mingw.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2076 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/os2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4356 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/posix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1805 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/sunos.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3860 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/virtualenv.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14831 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/win32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    41983 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/SConf.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14673 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/SConsign.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7394 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/C.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4357 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/Dir.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3546 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/Prog.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1972 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/RC.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15577 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13597 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/Interactive.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53509 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/Main.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42760 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/SConsOptions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26676 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/SConscript.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14272 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36753 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Subst.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    41191 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Taskmaster.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2122 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/386asm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15570 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/GettextCommon.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2014 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1943 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/arch.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13182 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/common.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2734 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/netframework.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15027 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/sdk.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    38783 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/vc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22570 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/vs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4368 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/PharLapCommon.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    32724 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1578 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixc++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2228 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2386 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixcxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2616 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixlink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7993 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/applelink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2141 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1661 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/as.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2893 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/asm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2889 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/bcc32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1567 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/c++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3742 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3296 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clang.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clangCommon/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      343 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clangCommon/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3534 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clangxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3259 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7461 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cyglink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1663 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/default.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3379 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/filesystem.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1544 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/g++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1891 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gas.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3616 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2377 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gettext_tool.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2437 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gnulink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2526 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1557 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpc++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1772 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2677 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpcxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2206 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hplink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2096 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/icc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1851 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/icl.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1954 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ilink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1995 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ilink32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19180 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/install.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25826 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/intelc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2588 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/link.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4649 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/LoadableModule.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7652 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/SharedLibrary.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6064 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3931 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkloc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2266 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/m4.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2900 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/masm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8622 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mingw.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4577 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msgfmt.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4517 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msginit.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4113 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msgmerge.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2387 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mslib.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14473 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mslink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1752 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mssdk.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12902 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msvc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    84784 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msvs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6788 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mwcc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3576 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mwld.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2573 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/nasm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4817 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/rmic.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2788 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/rpcgen.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2479 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgiar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1563 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgic++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1780 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgicc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1999 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgicxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2006 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgilink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2271 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1569 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunc++.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1888 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/suncc.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4879 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/suncxx.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2419 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunlink.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2429 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/tar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6412 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/textfile.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1786 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/tlib.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3687 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/wix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12548 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/xgettext.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4076 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/zip.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    71693 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Util.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6632 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/ConfigureCache.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15278 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/sconsign.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3134 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/BoolVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3896 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/EnumVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4672 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/ListVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3536 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/PackageVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5588 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/PathVariable.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12708 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6785 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Warnings.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      353 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4307 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1644 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/_scons_dbm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3395 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/win32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21614 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/cpp.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9295 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/dblite.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2032 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/exitfuncs.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1467 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/LICENSE.rst
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/markupsafe/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10126 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/markupsafe/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      558 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/markupsafe/_compat.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4690 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/markupsafe/_constants.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1873 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/markupsafe/_native.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.814387 Nuitka-1.7.6/nuitka/build/inline_copy/pkg_resources/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.884387 Nuitka-1.7.6/nuitka/build/inline_copy/pkg_resources/pkg_resources/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   107452 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/pkg_resources/pkg_resources/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      538 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/pkg_resources/pkg_resources/py31compat.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.814387 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1591 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      283 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_main.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3687 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_monitor.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      283 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_tqdm.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      287 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_tqdm_gui.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      307 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_tqdm_notebook.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      888 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_tqdm_pandas.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      596 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_utils.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1106 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/auto.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      857 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/autonotebook.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1376 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/dask.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5943 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/gui.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10790 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/notebook.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    57572 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/std.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6948 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/tk.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9533 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/utils.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      333 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/version.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1101 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/LICENSE
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13170 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4883 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/composer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28639 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/constructor.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3851 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/cyaml.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2837 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/dumper.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    43006 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/emitter.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2533 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/error.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2445 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/events.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2061 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/loader.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1440 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/nodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25495 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/parser.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6794 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/reader.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14184 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/representer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8999 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/resolver.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51277 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/scanner.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4165 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/serializer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2573 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/tokens.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1101 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/LICENSE
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9776 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4921 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/composer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25145 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/constructor.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3290 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/cyaml.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2719 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/dumper.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    43298 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/emitter.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2559 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/error.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2445 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/events.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1132 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/loader.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1440 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/nodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25542 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/parser.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6746 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/reader.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17711 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/representer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9122 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/resolver.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    52446 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/scanner.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4171 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/serializer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2573 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/tokens.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1101 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/LICENSE
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9607 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4881 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/composer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25554 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/constructor.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3294 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/cyaml.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2723 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/dumper.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42954 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/emitter.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2533 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/error.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2445 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/events.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1138 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/loader.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1440 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/nodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    25495 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/parser.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6854 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/reader.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14097 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/representer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8970 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/resolver.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51695 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/scanner.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4165 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/serializer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2573 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/tokens.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1530 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/LICENSE.txt
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18198 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/bitstream.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10157 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/compiler.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4455 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/cpu.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3763 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/debug.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13662 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/entropy_common.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3009 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/error_private.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2441 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/error_private.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34422 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/fse.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14748 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/fse_decompress.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20216 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/huf.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13930 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/mem.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26976 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/xxhash.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11706 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/xxhash.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2728 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/zstd_common.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2497 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/zstd_deps.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3828 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/zstd_errors.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15880 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/zstd_internal.h
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.894387 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    54982 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/huf_decompress.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9164 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_ddict.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1321 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_ddict.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    80283 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_decompress.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    66784 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_block.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2253 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_block.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7906 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_internal.h
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   138334 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/inline_copy/zstd/zstd.h
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.904387 Nuitka-1.7.6/nuitka/build/static_src/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    82393 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/CompiledAsyncgenType.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8250 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/CompiledCellType.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    56307 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/CompiledCodeHelpers.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    71532 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/CompiledCoroutineType.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35861 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/CompiledFrameType.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   100376 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/CompiledFunctionType.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    61078 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/CompiledGeneratorType.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    48523 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/CompiledGeneratorTypeUncompiledIntegration.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21638 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/CompiledMethodType.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18993 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersAllocator.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    37540 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersAttributes.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22263 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersBuiltin.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   107641 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersBuiltinTypeMethods.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3033 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersBytes.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13057 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersCalling.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   470655 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersCallingGenerated.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1617 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersChecksumTools.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2991 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersClasses.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   317872 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonEq.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4673 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonEqUtils.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   313003 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonGe.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   312414 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonGt.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   316217 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonLe.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   315628 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonLt.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   314618 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonNe.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36068 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersConstantsBlob.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19313 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersDeepcopy.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    38364 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersDictionaries.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24295 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersDictionariesGenerated.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7035 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersExceptions.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6668 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersFiles.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28131 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersFilesystemPaths.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2426 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersFloats.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1774 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersHeapStorage.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14585 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersImport.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14756 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersImportHard.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18431 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersLists.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13915 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersListsGenerated.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1640 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersMappings.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3513 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersMatching.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   181243 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryAdd.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16700 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryAddUtils.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    77943 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryBitand.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    77782 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryBitor.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    77943 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryBitxor.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    67487 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryDivmod.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1236 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryDivmodUtils.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    68748 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryFloordiv.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6274 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryInplaceAdd.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    83405 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryLshift.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13776 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryMatmult.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   183202 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryMod.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   188514 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryMult.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3404 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryMultUtils.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    66453 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryOlddiv.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    78891 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryPow.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1023 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryPowUtils.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    77305 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryRshift.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    70465 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinarySub.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    68005 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryTruediv.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   149580 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceAdd.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4071 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceAddUtils.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53224 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceBitand.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53122 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceBitor.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    53224 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceBitxor.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76512 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceFloordiv.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    47568 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceLshift.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17742 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceMatmult.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   136100 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceMod.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   142211 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceMult.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    74142 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceOlddiv.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    82669 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplacePow.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    45052 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceRshift.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    82842 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceSub.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76343 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceTruediv.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3219 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersProfiling.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3805 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersPythonPgo.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15369 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersRaising.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3758 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersSafeStrings.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3730 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersSequences.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1946 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersSlices.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26642 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersStrings.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4037 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersTuples.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5578 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/HelpersTypes.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11986 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/InspectPatcher.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    47877 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/MainProgram.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    58887 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/MetaPathBasedLoader.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4513 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/MetaPathBasedLoaderImportlibMetadataDistribution.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6427 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/MetaPathBasedLoaderResourceReader.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17285 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/MetaPathBasedLoaderResourceReaderFiles.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30910 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/OnefileBootstrap.c
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8021 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/build/static_src/OnefileSplashScreen.cpp
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.914387 Nuitka-1.7.6/nuitka/code_generation/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6414 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/AsyncgenCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10599 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/AttributeCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21864 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/BinaryOperationHelperDefinitions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2339 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/BranchCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16492 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/BuiltinCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    35905 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/CallCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4896 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ClassCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51533 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/CodeGeneration.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2375 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/CodeHelperSelection.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14392 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/CodeHelpers.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4879 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/CodeObjectCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17570 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ComparisonCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4446 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ComparisonHelperDefinitions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7335 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ConditionalCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6539 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ConstantCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31186 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/Contexts.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8484 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/CoroutineCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1574 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/CtypesCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28478 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/DictCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2125 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/Emission.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9325 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ErrorCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12304 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/EvalCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8975 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ExceptionCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7350 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ExpressionCTypeSelectionHelpers.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2093 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ExpressionCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17725 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/FrameCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    27968 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/FunctionCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7690 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/GeneratorCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5943 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/GlobalConstants.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6911 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/GlobalsLocalsCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1794 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/IdCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13318 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ImportCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1396 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/Indentation.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1506 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/IndexCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1033 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/InjectCCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3432 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/IntegerCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12010 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/IteratorCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2022 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/LabelCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2612 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/LineNumberCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15906 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ListCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6375 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/LoaderCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9951 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/LocalsDictCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3135 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/LoopCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1597 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/MatchCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6291 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ModuleCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8118 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/Namify.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12777 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/OperationCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    29459 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/PackageResourceCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3021 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/PrintCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5474 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/PythonAPICodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13095 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/RaisingCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3443 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/Reports.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5234 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/ReturnCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6517 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/SetCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13949 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/SliceCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9809 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/StringCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8188 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/SubscriptCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11176 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/TryCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3786 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/TupleCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14717 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/VariableCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9121 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/VariableDeclarations.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7881 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/YieldCodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.914387 Nuitka-1.7.6/nuitka/code_generation/c_types/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6069 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeBases.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3399 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeBooleans.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1804 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeCFloats.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1378 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeCLongs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3610 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeModuleDictVariables.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5128 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeNuitkaBooleans.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5211 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeNuitkaInts.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3955 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeNuitkaVoids.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19628 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypePyObjectPointers.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2852 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeVoids.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/c_types/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.914387 Nuitka-1.7.6/nuitka/code_generation/templates/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2885 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesAsyncgens.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5865 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesConstants.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2961 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesCoroutines.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2290 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesExceptions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6339 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesFrames.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3321 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesFunction.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3306 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesGeneratorFunction.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2335 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesIterators.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4217 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesLoader.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21244 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesModules.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6640 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesVariables.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2475 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/TemplateDebugWrapper.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.924387 Nuitka-1.7.6/nuitka/code_generation/templates_c/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11231 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateCallsMethodPositional.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5847 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateCallsMixed.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    23760 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateCallsPositional.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5238 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateCallsPositionalMethodDescr.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1905 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateMakeListHinted.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1843 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateMakeListSmall.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2817 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperBuiltinMethodOperation.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12819 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperDictionaryCopy.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2044 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperImportHard.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2762 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperLongTools.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1544 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperObjectTools.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7197 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationBinary.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12850 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparison.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4288 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonBytes.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2088 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonFloat.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2118 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonInt.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3933 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonList.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7407 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonLong.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4292 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonStr.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3860 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonTuple.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4487 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonUnicode.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11579 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationInplace.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19317 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsBinary.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2843 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsBytes.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3635 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsCommon.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11102 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsFloat.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15380 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsInt.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2979 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsList.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10421 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsLong.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2557 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsSet.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3020 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsStr.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2984 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsTuple.c.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3173 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsUnicode.c.j2
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.924387 Nuitka-1.7.6/nuitka/containers/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1435 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/containers/Namedtuples.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6553 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/containers/OrderedDicts.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      554 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/containers/OrderedSets.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4397 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/containers/OrderedSetsFallback.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/containers/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.924387 Nuitka-1.7.6/nuitka/distutils/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1964 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/distutils/Build.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14219 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/distutils/DistutilCommands.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/distutils/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.924387 Nuitka-1.7.6/nuitka/finalizations/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1224 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/finalizations/Finalization.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6110 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/finalizations/FinalizeMarkups.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/finalizations/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.924387 Nuitka-1.7.6/nuitka/freezer/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7311 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/DependsExe.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2584 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/DllDependenciesCommon.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11992 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/DllDependenciesMacOS.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7211 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/DllDependenciesPosix.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6620 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/DllDependenciesWin32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17058 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/IncludedDataFiles.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9492 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/IncludedEntryPoints.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9304 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/Onefile.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26319 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/Standalone.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/freezer/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.924387 Nuitka-1.7.6/nuitka/importing/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11007 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/importing/IgnoreListing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2899 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/importing/ImportCache.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6719 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/importing/ImportResolving.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28503 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/importing/Importing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4738 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/importing/PreloadedPackages.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14918 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/importing/Recursion.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10981 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/importing/StandardLibrary.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/importing/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/nodes/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3637 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/AsyncgenNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4082 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/AttributeLookupNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13567 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/AttributeNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   378745 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/AttributeNodesGenerated.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3823 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinAllNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4098 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinAnyNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2496 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinComplexNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1698 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinDecodingNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2727 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinDecoratorNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4694 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinDictNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4948 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinFormatNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2142 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinHashNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1424 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinInputNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5334 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinIntegerNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12723 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinIteratorNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1996 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinLenNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3606 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinNextNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3240 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinOpenNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   245536 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinOperationNodeBasesGenerated.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18589 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinRangeNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9067 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinRefNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3307 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinSumNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13543 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinTypeNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1573 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BuiltinVarsNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26113 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/BytesNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6478 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/CallNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1550 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/Checkers.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   604445 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ChildrenHavingMixins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8448 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ClassNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6585 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/CodeObjectSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21683 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ComparisonNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30314 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ConditionalNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    46536 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ConstantRefNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12213 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ContainerMakingNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2834 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ContainerOperationNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4581 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/CoroutineNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1714 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/CtypesNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51021 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/DictionaryNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7856 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ExceptionNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7317 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ExecEvalNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    44996 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ExpressionBases.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    52352 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ExpressionBasesGenerated.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21278 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ExpressionShapeMixins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12156 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/FrameNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3544 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/FunctionAttributeNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39803 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/FunctionNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5376 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/FutureSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6256 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/GeneratorNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6850 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/GlobalsLocalsNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    76798 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/HardImportNodesGenerated.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5508 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ImportHardNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    45942 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ImportNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2733 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/IndicatorMixins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1502 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/InjectCNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11228 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/IterationHandles.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11002 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/KeyValuePairNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    16320 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ListOperationNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    23094 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/LocalsDictNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14922 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/LocalsScopes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15581 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/LoopNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1712 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/MatchNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6534 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ModuleAttributeNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30972 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ModuleNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    24899 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/NodeBases.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15128 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/NodeMakingHelpers.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5550 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/NodeMetaClasses.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31894 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/OperatorNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9134 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/OperatorNodesUnary.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4202 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/OsSysNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12442 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/OutlineNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    31534 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/PackageMetadataNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7901 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/PackageResourceNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3407 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/PrintNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6772 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/ReturnNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4715 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/SideEffectNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12501 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/SliceNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    94880 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/StatementBasesGenerated.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9430 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/StatementNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    28658 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/StrNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3504 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/StringConcatenationNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8640 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/SubscriptNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17853 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/TryNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2405 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/TypeMatchNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11061 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/TypeNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39522 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/VariableAssignNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10746 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/VariableDelNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4574 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/VariableNameNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30982 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/VariableRefNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4748 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/VariableReleaseNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3902 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/YieldNodes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/nodes/shapes/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   156243 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/shapes/BuiltinTypeShapes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4387 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/shapes/ControlFlowDescriptions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4567 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/shapes/ShapeMixins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42374 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/shapes/StandardShapes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/nodes/shapes/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/optimizations/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3279 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/optimizations/BytecodeDemotion.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3920 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/optimizations/FunctionInlining.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2144 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/optimizations/Graphs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10762 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/optimizations/Optimization.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    52370 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/optimizations/OptimizeBuiltinCalls.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2272 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/optimizations/Tags.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    40896 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/optimizations/TraceCollections.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    23977 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/optimizations/ValueTraces.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/optimizations/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/pgo/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4663 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/pgo/PGO.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/pgo/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/plugins/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    40887 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/PluginBase.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    57995 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/Plugins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/plugins/standard/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22510 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/AntiBloatPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3460 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/ConsiderPyLintAnnotationsPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10383 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/DataFilesPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4404 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/DelvewheelPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5675 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/DillPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13744 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/DllFilesPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2062 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/EnumPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1905 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/EventletPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1880 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/GeventPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3482 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/GiPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5027 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/GlfwPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18335 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/ImplicitImports.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4948 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/KivyPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7239 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/MatplotlibPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6352 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/MultiprocessingPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1187 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/NumpyPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6691 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/OptionsNannyPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1917 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/PbrPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4665 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/PkgResourcesPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6992 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/PmwPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    50584 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/PySidePyQtPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2986 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/PywebViewPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1160 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/TensorflowPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12242 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/TkinterPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1140 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/TorchPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10191 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/TransformersPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1073 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/TrioPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5640 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/UpxPlugin.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)   166853 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/standard.nuitka-package.config.yml
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2221 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/stdlib2.nuitka-package.config.yml
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9940 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/plugins/standard/stdlib3.nuitka-package.config.yml
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/reports/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2209 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/reports/LicenseReport.rst.j2
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17538 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/reports/Reports.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/reports/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/specs/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5911 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/BuiltinBytesOperationSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2786 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/BuiltinDictOperationSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2541 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/BuiltinListOperationSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    26553 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/BuiltinParameterSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6065 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/BuiltinStrOperationSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1159 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/BuiltinTypeOperationSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4802 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/BuiltinUnicodeOperationSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5263 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/HardImportSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    18740 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/ParameterSpecs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/specs/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1603 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/Basics.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/commercial/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      815 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/commercial/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/data_composer/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14250 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/data_composer/DataComposer.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/data_composer/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1306 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/data_composer/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/environments/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2449 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/environments/CreateEnvironment.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3735 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/environments/Virtualenv.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/environments/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/general/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/general/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/general/dll_report/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/general/dll_report/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2366 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/general/dll_report/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/general/find_module/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3920 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/general/find_module/FindModuleCode.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/general/find_module/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/onefile_compressor/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10345 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/onefile_compressor/OnefileCompressor.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/onefile_compressor/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1311 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/onefile_compressor/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/podman/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1872 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/podman/Podman.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/podman/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6685 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/podman/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/profiler/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/profiler/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2529 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/profiler/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.934387 Nuitka-1.7.6/nuitka/tools/scanning/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3344 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/scanning/DisplayPackageDLLs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2095 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/scanning/DisplayPackageData.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/scanning/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/tools/specialize/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    51143 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/specialize/CTypeDescriptions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7685 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/specialize/Common.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    39625 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/specialize/SpecializeC.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    34664 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/specialize/SpecializePython.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/specialize/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/tools/testing/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    55424 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/Common.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1483 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/Constructs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8940 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/OutputComparison.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1278 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/Pythons.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8024 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/RuntimeTracing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5371 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/SearchModes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3375 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/Valgrind.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/tools/testing/check_reference_counts/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/check_reference_counts/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3064 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/check_reference_counts/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/tools/testing/compare_with_cpython/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/compare_with_cpython/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    29429 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/compare_with_cpython/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/tools/testing/find_sxs_modules/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/find_sxs_modules/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1949 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/find_sxs_modules/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/tools/testing/measure_construct_performance/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/measure_construct_performance/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8755 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/measure_construct_performance/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/tools/testing/run_nuitka_tests/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/run_nuitka_tests/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36321 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/testing/run_nuitka_tests/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/tools/watch/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/watch/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9503 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tools/watch/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/tree/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    47135 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/Building.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    74608 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ComplexCallHelperFunctions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1700 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/Extractions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2572 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/InternalModule.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1511 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/Operations.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2807 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationAssertStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    42768 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationAssignmentStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2948 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationBooleanExpressions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11693 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationCallExpressions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15072 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationClasses.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    37638 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationClasses3.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6430 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationComparisonExpressions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    21824 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationContractionExpressions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    11061 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationDictionaryCreation.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14607 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationExecStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7782 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationForLoopStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    30544 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationFunctionStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    13437 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationImportStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6577 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationLambdaExpressions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20962 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationMatchStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2409 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationMultidist.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8194 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationNamespacePackages.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4658 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationPrintStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15371 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationSequenceCreation.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4824 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationSubscriptExpressions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14615 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationTryExceptStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6982 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationTryFinallyStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5674 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationWhileLoopStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14341 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationWithStatements.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3088 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/ReformulationYieldExpressions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12746 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/SourceHandling.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3757 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/SyntaxErrors.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22973 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/TreeHelpers.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    20012 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/VariableClosure.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/tree/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/nuitka/utils/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2655 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/AppDirs.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3248 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/CStrings.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3653 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/CommandLineOptions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4297 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Distributions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5794 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Download.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12781 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Execution.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    36129 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/FileOperations.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2885 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Hashing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2362 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Images.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6985 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Importing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8149 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/InstalledPythons.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2224 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/InstanceCounters.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4336 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Jinja2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1238 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Json.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4304 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/MacOSApp.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5040 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/MemoryUsage.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9062 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/ModuleNames.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4309 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/ReExecute.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3815 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Rest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    23096 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/SharedLibraries.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3664 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Shebang.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2591 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Signing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6207 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/StaticLibraries.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2602 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/ThreadedExecutor.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2772 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Timing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10826 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Utils.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    10574 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/WindowsFileUsage.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    19540 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/WindowsResources.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6108 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/Yaml.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      833 2023-07-23 17:50:33.000000 Nuitka-1.7.6/nuitka/utils/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      834 2023-07-23 17:50:33.000000 Nuitka-1.7.6/pyproject.toml
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       38 2023-07-23 17:50:50.974387 Nuitka-1.7.6/setup.cfg
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    15575 2023-07-23 17:50:33.000000 Nuitka-1.7.6/setup.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.944387 Nuitka-1.7.6/tests/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/basics/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1766 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/AssertsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5934 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/AssignmentsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5866 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/AssignmentsTest32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4055 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/BranchingTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1104 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/BuiltinOverload.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3749 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/BuiltinSuperTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    17080 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/BuiltinsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      866 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ClassMinimalTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4764 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ClassesTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3414 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ClassesTest32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1406 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ClassesTest34.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4698 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ComparisonChainsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4639 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ConstantsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      995 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ConstantsTest27.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1628 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/DecoratorsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2317 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/DefaultParametersTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1127 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/DoubleDeletionsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      806 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/EmptyModuleTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14387 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ExceptionRaisingTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      961 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ExceptionRaisingTest32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1458 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ExceptionRaisingTest33.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6747 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ExecEvalTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1417 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ExtremeClosureTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1658 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/FunctionObjectsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    12335 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/FunctionsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3603 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/FunctionsTest32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2627 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/FunctionsTest_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      890 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/FutureTest32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5809 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/GeneratorExpressionsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1041 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/GeneratorExpressionsTest_37.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3824 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/GlobalStatementTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1286 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/HelloWorldTest_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2469 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ImportingTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1296 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/InplaceOperationsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4227 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/InspectionTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1504 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/InspectionTest_35.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1618 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/InspectionTest_36.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1671 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/LambdasTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2731 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/LateClosureAssignmentTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2923 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ListContractionsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3329 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/LoopingTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1536 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/MainProgramsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1925 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ModuleAttributesTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1988 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/OperatorsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14903 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/OrderChecksTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1827 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/OrderChecksTest27.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1452 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/OverflowFunctionsTest_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5853 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ParameterErrorsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1899 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ParameterErrorsTest32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      863 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/PrintFutureTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1413 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/PrintingTest_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      878 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/RecursionTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    23840 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ReferencingTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2076 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ReferencingTest27.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     7819 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ReferencingTest33.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4904 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ReferencingTest35.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5446 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ReferencingTest36.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2899 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ReferencingTest_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1630 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/SlotsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1159 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/ThreadedGeneratorsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    22966 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/TrickAssignmentsTest32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1541 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/TrickAssignmentsTest35.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1788 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/TrickAssignmentsTest_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2086 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/TryContinueFinallyTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2212 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/TryExceptContinueTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2275 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/TryExceptFinallyTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2304 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/TryExceptFramesTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2842 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/TryReturnFinallyTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2328 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/TryYieldFinallyTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1093 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/UnicodeTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1877 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/UnpackingTest35.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2095 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/VarargsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     4879 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/WithStatementsTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3070 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/YieldFromTest33.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3821 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/run_all.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2271 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/basics/run_xml.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/onefile/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1213 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/onefile/HelloWorldTest.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1307 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/onefile/KeyboardInterruptTest.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     5816 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/onefile/run_all.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/optimizations/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      958 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/ArgumentTypes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1055 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/Attributes.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1021 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/Calls.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      921 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/Conditions.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      909 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/DecodingOperations.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1212 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/FormatStrings36.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1150 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/HardImports.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      974 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/HardImports_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      918 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/Iterations.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1260 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/Len.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2262 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/Operations.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1333 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/Subscripts.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     8736 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/optimizations/run_all.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/packages/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/packages/package_import_success_after_failure/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2382 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/package_import_success_after_failure/PackageImportSuccessAfterFailure.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/packages/package_import_success_after_failure/variable_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      942 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/package_import_success_after_failure/variable_package/SomeModule.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1168 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/package_import_success_after_failure/variable_package/__init__.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3671 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/run_all.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.814387 Nuitka-1.7.6/tests/packages/sub_package/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/packages/sub_package/kitty/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1230 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/sub_package/kitty/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      908 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/sub_package/kitty/bigkitty.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      910 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/sub_package/kitty/smallkitty.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/packages/sub_package/kitty/speak/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      929 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/sub_package/kitty/speak/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1053 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/sub_package/kitty/speak/hello.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      966 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/sub_package/kitty/speak/miau.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      968 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/sub_package/kitty/speak/purr.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.814387 Nuitka-1.7.6/tests/packages/top_level_attributes_3/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/packages/top_level_attributes_3/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2336 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/top_level_attributes_3/some_package/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      907 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/packages/top_level_attributes_3/some_package/some_module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/plugins/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/plugins/code_signing/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1170 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/plugins/code_signing/CodeSigningMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/plugins/data_files/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1332 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/plugins/data_files/DataFilesMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/plugins/data_files/data_files_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      924 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/plugins/data_files/data_files_package/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/plugins/data_files/data_files_package/lala.txt
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/plugins/data_files/data_files_package/sub_dir/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/plugins/data_files/data_files_package/sub_dir/lulu.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      255 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/plugins/data_files/test_case.nuitka-package.config.yml
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/plugins/parameters/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1019 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/plugins/parameters/ParametersMain.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2168 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/plugins/parameters/parameter-using-plugin.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3861 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/plugins/run_all.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/absolute_import/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      867 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/absolute_import/AbsoluteImportMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/absolute_import/foobar/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      796 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/absolute_import/foobar/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1043 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/absolute_import/foobar/foobar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      879 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/absolute_import/foobar/local.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      860 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/absolute_import/foobar/util.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports1/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      808 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports1/CasedImportingMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports1/path1/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports1/path1/Some_Module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports1/path1/Some_Package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports1/path1/Some_Package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports1/path2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports1/path2/some_module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports1/path2/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports1/path2/some_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      808 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports2/CasedImportingMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports2/path1/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports2/path1/some_module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports2/path1/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports2/path1/some_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports2/path2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports2/path2/Some_Module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports2/path2/Some_Package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports2/path2/Some_Package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports3/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1075 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports3/CasedImportingMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports3/path1/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports3/path1/Some_Module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports3/path1/Some_Package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports3/path1/Some_Package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports3/path2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports3/path2/Some_Module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/case_imports3/path2/Some_Package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/case_imports3/path2/Some_Package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/cyclic_imports/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      801 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/cyclic_imports/CyclicImportsMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/cyclic_imports/cyclic_importing_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      875 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/cyclic_imports/cyclic_importing_package/Child1.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      875 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/cyclic_imports/cyclic_importing_package/Child2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      842 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/cyclic_imports/cyclic_importing_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/dash_import/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      888 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/dash_import/DashImportMain.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      817 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/dash_import/dash-module.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      817 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/dash_import/plus+module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/dash_main/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/dash_main/Dash-Main.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.954387 Nuitka-1.7.6/tests/programs/deep/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      898 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/deep/DeepProgramMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/deep/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      980 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/deep/some_package/DeepBrother.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      909 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/deep/some_package/DeepChild.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/deep/some_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/deep/some_package/deep_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      876 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/deep/some_package/deep_package/DeepDeepChild.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      952 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/deep/some_package/deep_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/dunderinit_imports/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      794 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/dunderinit_imports/DunderInitImportsMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/dunderinit_imports/package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      797 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/dunderinit_imports/package/SubModule.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      857 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/dunderinit_imports/package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/import_variants/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1005 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/import_variants/ImportVariationsMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/import_variants/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      946 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/import_variants/some_package/Child1.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1098 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/import_variants/some_package/Child2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      822 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/import_variants/some_package/Child3.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      994 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/import_variants/some_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/main_raises/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      911 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/main_raises/ErrorMain.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      808 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/main_raises/ErrorRaising.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/main_raises2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1080 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/main_raises2/ErrorInFunctionMain.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      808 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/main_raises2/ErrorRaising.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/module_attributes/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1529 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_attributes/ModuleAttributesMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/module_attributes/package_level1/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1744 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_attributes/package_level1/Nearby1.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1611 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_attributes/package_level1/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1744 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/Nearby2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1611 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/package_level3/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1744 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/package_level3/Nearby3.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1611 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/package_level3/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/module_exits/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      869 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_exits/ErrorExitingModule.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      867 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_exits/Main.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/module_object_replacing/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1078 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_object_replacing/ModuleObjectReplacingMain.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1359 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/module_object_replacing/SelfReplacingModule.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/multiprocessing_using/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      990 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/multiprocessing_using/MultiprocessingUsingMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/multiprocessing_using/foo/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/multiprocessing_using/foo/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      836 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/multiprocessing_using/foo/__main__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1758 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/multiprocessing_using/foo/entry.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/named_imports/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      846 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/named_imports/NamedImportsMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/named_imports/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/named_imports/some_package/SomeModule.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      824 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/named_imports/some_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/named_imports/some_package/sub_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/named_imports/some_package/sub_package/SomeModule.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_code/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      800 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_code/PackageInitCodeMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_code/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_code/some_package/SomeModule.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_code/some_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_contains_main/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      789 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_contains_main/PackageContainsMain.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_contains_main/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      801 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_contains_main/local.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_init_import/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      823 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_init_import/PackageInitImportMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_init_import/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1008 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_init_import/some_package/PackageLocal.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1169 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_init_import/some_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_init_issue/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      789 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_init_issue/PackageInitIssueMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_init_issue/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_init_issue/some_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_init_issue/some_package/child_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      798 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_init_issue/some_package/child_package/SomeModule.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      795 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_init_issue/some_package/child_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_missing_init/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      926 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_missing_init/PackageMissingInitMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_missing_init/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      965 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_missing_init/some_package/some_module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_missing_init/some_package/sub_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      977 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_missing_init/some_package/sub_package/some_sub_module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_module_collision/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      901 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_module_collision/PackageAndModuleNamedSameMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_module_collision/Something/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_module_collision/Something/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      801 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_module_collision/something.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_overload/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      852 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_overload/Main.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_overload/foo/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_overload/foo/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_overload/foo/bar.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_overload/foo/bar2.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_prevents_submodule/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2972 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_prevents_submodule/PackagePreventsSubmoduleMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_prevents_submodule/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1078 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_prevents_submodule/some_package/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      800 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_prevents_submodule/some_package/some_module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.824387 Nuitka-1.7.6/tests/programs/package_program/
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/package_program/PackageAsMain/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      888 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_program/PackageAsMain/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1630 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/package_program/PackageAsMain/__main__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1728 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/PkgUtilIterModulesMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package1/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package1/SomeModuleC.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package1/SomeModuleD.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package1/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package2/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package2/SomeModuleA.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package2/SomeModuleB.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package2/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/pkgutil_usage/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1261 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_usage/PkgUtilUsageMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/pkgutil_usage/package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       13 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_usage/package/DATA_FILE.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       14 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_usage/package/DATA_FILE2.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       14 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_usage/package/DATA_FILE3.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1553 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/pkgutil_usage/package/__init__.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/plugin_import/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      859 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/plugin_import/PluginImportMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/plugin_import/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      771 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/plugin_import/some_package/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      781 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/plugin_import/some_package/some_module.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/reimport_main_dynamic/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      911 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/reimport_main_dynamic/ImportItselfDynamicMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/reimport_main_static/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      898 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/reimport_main_static/ImportItselfStaticMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/relative_import/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      842 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/relative_import/RelativeImportMain.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/relative_import/dircache.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/resource_reader37/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1169 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/resource_reader37/ResourceReaderMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/resource_reader37/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)       13 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/resource_reader37/some_package/DATA_FILE.txt
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/resource_reader37/some_package/__init__.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     6615 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/run_all.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/stdlib_overload/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1171 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/stdlib_overload/StdlibOverloadMain.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/stdlib_overload/pyexpat.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/stdlib_overload/some_package/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      769 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/stdlib_overload/some_package/__init__.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      909 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/stdlib_overload/some_package/normal_importing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      810 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/stdlib_overload/some_package/pyexpat.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1236 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/stdlib_overload/some_package/star_importing.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/syntax_errors/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      791 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/syntax_errors/IndentationErroring.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      800 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/syntax_errors/SyntaxErroring.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1079 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/syntax_errors/SyntaxErrorsMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/unicode_bom/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      963 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/unicode_bom/UnicodeBomMain.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      846 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/unicode_bom/unicode_bom.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/programs/with space/
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      826 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/programs/with space/Space Main.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.964387 Nuitka-1.7.6/tests/reflected/
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)    14061 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/reflected/compile_itself.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1243 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/run-tests
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.974387 Nuitka-1.7.6/tests/standalone/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1058 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/BrotliUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2554 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/CtypesUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1136 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/FlaskUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      990 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/GlfwUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1184 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/GtkUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1025 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/HexEncodingTest_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1086 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/IdnaUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1151 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/LxmlUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1431 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/MatplotlibUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2538 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/MetadataPackagesUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1727 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/NumpyUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      947 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/OpenGLUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1379 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PandasUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1066 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PasslibUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1216 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PendulumUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2074 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PkgResourcesRequiresUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1067 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PmwUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1085 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PyQt5Plugins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1105 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PyQt5SSLSupport.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2050 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PyQt5Using.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1085 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PyQt6Plugins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2050 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PyQt6Using.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1091 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PySide6Plugins.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1757 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/PySide6Using.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1323 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/RsaUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      973 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/ShlibUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1537 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/SocketUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1941 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/TkInterUsing.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     3228 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/Urllib3Using.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1200 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/Win32ComUsing.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     9531 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/run_all.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.974387 Nuitka-1.7.6/tests/standalone/zip_importer/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1264 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/standalone/zip_importer/ZipImporterMain.py
+drwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)        0 2023-07-23 17:50:50.974387 Nuitka-1.7.6/tests/syntax/
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      811 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/AsyncgenReturn36.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      868 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/BreakWithoutLoop.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      791 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/ClassReturn.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      970 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/ClosureDel_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      849 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/ContinueWithoutLoop.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      791 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/DuplicateArgument.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1111 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/ExecWithNesting_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      826 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/FutureBraces.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      805 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/FutureUnknown.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     1041 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/GeneratorExpressions38.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      879 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/GeneratorReturn_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      792 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/GlobalForParameter.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      995 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/Importing32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      799 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/IndentationError.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      915 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/LateFutureImport.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      841 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/MisplacedFutureImport.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      800 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/ModuleReturn.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      883 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/NonAsciiWithoutEncoding_2.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      794 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/NonlocalForParameter32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      868 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/NonlocalNotFound32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      908 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/StarImportExtra.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      869 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/SyntaxError.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      874 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/TryExceptAllNotLast.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      875 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/TryFinallyContinue_37.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      776 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/UnpackNoTuple.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      809 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/UnpackTwoStars32.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      793 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/YieldFromInModule.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      804 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/YieldInAsync35.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      923 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/YieldInGenexp38.py
+-rw-r--r--   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)      781 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/YieldInModule.py
+-rwxr-xr-x   0 nuitka-buildslave  (2001) nuitka-buildslave  (2001)     2203 2023-07-23 17:50:33.000000 Nuitka-1.7.6/tests/syntax/run_all.py
```

### Comparing `Nuitka-1.7.5/Changelog.pdf` & `Nuitka-1.7.6/Changelog.pdf`

 * *Installing the 'pypdf' Python module from the 'python3-pypdf' package may produce a better output.*

 * *Files 0% similar despite different names*

#### dumppdf -adt {}

 * *error from `dumppdf -adt {}`:*

 * *DEBUG:pdfminer.psparser:seek: 0*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b''*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b'%%EOF'*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b'2799825'*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b'startxref'*

 * *DEBUG:pdfminer.pdfdocument:xref found: pos=b'2799825'*

 * *DEBUG:pdfminer.psparser:seek: 2799825*

 * *DEBUG:pdfminer.psparser:nexttoken: (2799825, /b'xref')*

 * *DEBUG:pdfminer.pdfdocument:read_xref_from: start=2799825, token=/b'xref'*

 * *DEBUG:pdfminer.psparser:nextline: 2799829, b'\n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799830, b'0 1680\n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799837, b'0000000000 65535 f \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799857, b'0000000073 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799877, b'0000000172 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799897, b'0000000279 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799917, b'0000000391 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799937, b'0000000496 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799957, b'0000000705 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799977, b'0000000914 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2799997, b'0000001123 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2800017, b'0000001332 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2800037, b'0000001541 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2800057, b'0000001655 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2800077, b'0000001766 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 2800097, b'0000001976 00000 n \n'*

 * *[ truncated after 25 lines; 71393 ignored ]*

```diff
@@ -12186,21 +12186,21 @@
 </object>
 
 <object id="348">
 <dict size="9">
 <key>Author</key>
 <value><string size="0"></string></value>
 <key>CreationDate</key>
-<value><string size="23">D:20230714152912+00&#39;00&#39;</string></value>
+<value><string size="23">D:20230723195044+00&#39;00&#39;</string></value>
 <key>Creator</key>
 <value><string size="13">&#40;unspecified&#41;</string></value>
 <key>Keywords</key>
 <value><string size="0"></string></value>
 <key>ModDate</key>
-<value><string size="23">D:20230714152912+00&#39;00&#39;</string></value>
+<value><string size="23">D:20230723195044+00&#39;00&#39;</string></value>
 <key>Producer</key>
 <value><string size="41">ReportLab PDF Library - www.reportlab.com</string></value>
 <key>Subject</key>
 <value><string size="13">&#40;unspecified&#41;</string></value>
 <key>Title</key>
 <value><string size="16">Nuitka Changelog</string></value>
 <key>Trapped</key>
@@ -35333,16 +35333,16 @@
 </dict>
 </object>
 
 <trailer>
 <dict size="4">
 <key>ID</key>
 <value><list size="2">
-<string size="16">3&#142;&#17;&#239;&#186;&#222;{M&#164;&#219;&#181; &#250;&#255;&#19;2</string>
-<string size="16">3&#142;&#17;&#239;&#186;&#222;{M&#164;&#219;&#181; &#250;&#255;&#19;2</string>
+<string size="16">&#187;9&#245;&#231;2&#139;26&#237;VI&#160;f&#190;&#127;&#164;</string>
+<string size="16">&#187;9&#245;&#231;2&#139;26&#237;VI&#160;f&#190;&#127;&#164;</string>
 </list></value>
 <key>Info</key>
 <value><ref id="348" /></value>
 <key>Root</key>
 <value><ref id="347" /></value>
 <key>Size</key>
 <value><number>1680</number></value>
```

### Comparing `Nuitka-1.7.5/Changelog.rst` & `Nuitka-1.7.6/Changelog.rst`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/Developer_Manual.pdf` & `Nuitka-1.7.6/Developer_Manual.pdf`

 * *Installing the 'pypdf' Python module from the 'python3-pypdf' package may produce a better output.*

 * *Files 0% similar despite different names*

#### dumppdf -adt {}

 * *error from `dumppdf -adt {}`:*

 * *DEBUG:pdfminer.psparser:seek: 0*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b''*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b'%%EOF'*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b'798508'*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b'startxref'*

 * *DEBUG:pdfminer.pdfdocument:xref found: pos=b'798508'*

 * *DEBUG:pdfminer.psparser:seek: 798508*

 * *DEBUG:pdfminer.psparser:nexttoken: (798508, /b'xref')*

 * *DEBUG:pdfminer.pdfdocument:read_xref_from: start=798508, token=/b'xref'*

 * *DEBUG:pdfminer.psparser:nextline: 798512, b'\n'*

 * *DEBUG:pdfminer.psparser:nextline: 798513, b'0 675\n'*

 * *DEBUG:pdfminer.psparser:nextline: 798519, b'0000000000 65535 f \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798539, b'0000000073 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798559, b'0000000204 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798579, b'0000000311 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798599, b'0000006874 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798619, b'0000007598 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798639, b'0000007868 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798659, b'0000007980 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798679, b'0000008149 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798699, b'0000008318 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798719, b'0000008487 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798739, b'0000008657 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798759, b'0000008827 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 798779, b'0000008997 00000 n \n'*

 * *[ truncated after 25 lines; 32054 ignored ]*

```diff
@@ -12877,21 +12877,21 @@
 </object>
 
 <object id="384">
 <dict size="9">
 <key>Author</key>
 <value><string size="0"></string></value>
 <key>CreationDate</key>
-<value><string size="23">D:20230714152909+00&#39;00&#39;</string></value>
+<value><string size="23">D:20230723195040+00&#39;00&#39;</string></value>
 <key>Creator</key>
 <value><string size="13">&#40;unspecified&#41;</string></value>
 <key>Keywords</key>
 <value><string size="0"></string></value>
 <key>ModDate</key>
-<value><string size="23">D:20230714152909+00&#39;00&#39;</string></value>
+<value><string size="23">D:20230723195040+00&#39;00&#39;</string></value>
 <key>Producer</key>
 <value><string size="41">ReportLab PDF Library - www.reportlab.com</string></value>
 <key>Subject</key>
 <value><string size="13">&#40;unspecified&#41;</string></value>
 <key>Title</key>
 <value><string size="23">Nuitka Developer Manual</string></value>
 <key>Trapped</key>
@@ -17679,16 +17679,16 @@
 </dict>
 </object>
 
 <trailer>
 <dict size="4">
 <key>ID</key>
 <value><list size="2">
-<string size="16">&#218;&#62;&#25;&#172;:&#30;&#213;d&#129;&#221;o=Q&#146;H&#30;</string>
-<string size="16">&#218;&#62;&#25;&#172;:&#30;&#213;d&#129;&#221;o=Q&#146;H&#30;</string>
+<string size="16">&#3;S&#184;&#163;&#224;&#40;I&#34;&#170;&#60;&#12;&#232;*&#178;&#34;6</string>
+<string size="16">&#3;S&#184;&#163;&#224;&#40;I&#34;&#170;&#60;&#12;&#232;*&#178;&#34;6</string>
 </list></value>
 <key>Info</key>
 <value><ref id="384" /></value>
 <key>Root</key>
 <value><ref id="383" /></value>
 <key>Size</key>
 <value><number>675</number></value>
```

### Comparing `Nuitka-1.7.5/Developer_Manual.rst` & `Nuitka-1.7.6/Developer_Manual.rst`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/LICENSE.txt` & `Nuitka-1.7.6/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/MANIFEST.in` & `Nuitka-1.7.6/MANIFEST.in`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/Nuitka.egg-info/PKG-INFO` & `Nuitka-1.7.6/Nuitka.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Nuitka
-Version: 1.7.5
+Version: 1.7.6
 Summary: Python compiler with full language support and CPython compatibility
 Home-page: https://nuitka.net
 Author: Kay Hayen
 Author-email: Kay.Hayen@gmail.com
 License: Apache License, Version 2.0
 Project-URL: Commercial, https://nuitka.net/doc/commercial.html
 Project-URL: Support, https://nuitka.net/pages/support.html
@@ -19,15 +19,14 @@
 Classifier: Intended Audience :: Science/Research
 Classifier: Topic :: Software Development :: Compilers
 Classifier: Topic :: Software Development :: Build Tools
 Classifier: Topic :: Software Development :: Quality Assurance
 Classifier: Topic :: System :: Software Distribution
 Classifier: Programming Language :: Python :: 2.6
 Classifier: Programming Language :: Python :: 2.7
-Classifier: Programming Language :: Python :: 3.3
 Classifier: Programming Language :: Python :: 3.4
 Classifier: Programming Language :: Python :: 3.5
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

### Comparing `Nuitka-1.7.5/Nuitka.egg-info/SOURCES.txt` & `Nuitka-1.7.6/Nuitka.egg-info/SOURCES.txt`

 * *Files 0% similar despite different names*

```diff
@@ -1015,14 +1015,15 @@
 nuitka/nodes/BuiltinAnyNodes.py
 nuitka/nodes/BuiltinComplexNodes.py
 nuitka/nodes/BuiltinDecodingNodes.py
 nuitka/nodes/BuiltinDecoratorNodes.py
 nuitka/nodes/BuiltinDictNodes.py
 nuitka/nodes/BuiltinFormatNodes.py
 nuitka/nodes/BuiltinHashNodes.py
+nuitka/nodes/BuiltinInputNodes.py
 nuitka/nodes/BuiltinIntegerNodes.py
 nuitka/nodes/BuiltinIteratorNodes.py
 nuitka/nodes/BuiltinLenNodes.py
 nuitka/nodes/BuiltinNextNodes.py
 nuitka/nodes/BuiltinOpenNodes.py
 nuitka/nodes/BuiltinOperationNodeBasesGenerated.py
 nuitka/nodes/BuiltinRangeNodes.py
```

### Comparing `Nuitka-1.7.5/PKG-INFO` & `Nuitka-1.7.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Nuitka
-Version: 1.7.5
+Version: 1.7.6
 Summary: Python compiler with full language support and CPython compatibility
 Home-page: https://nuitka.net
 Author: Kay Hayen
 Author-email: Kay.Hayen@gmail.com
 License: Apache License, Version 2.0
 Project-URL: Commercial, https://nuitka.net/doc/commercial.html
 Project-URL: Support, https://nuitka.net/pages/support.html
@@ -19,15 +19,14 @@
 Classifier: Intended Audience :: Science/Research
 Classifier: Topic :: Software Development :: Compilers
 Classifier: Topic :: Software Development :: Build Tools
 Classifier: Topic :: Software Development :: Quality Assurance
 Classifier: Topic :: System :: Software Distribution
 Classifier: Programming Language :: Python :: 2.6
 Classifier: Programming Language :: Python :: 2.7
-Classifier: Programming Language :: Python :: 3.3
 Classifier: Programming Language :: Python :: 3.4
 Classifier: Programming Language :: Python :: 3.5
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

### Comparing `Nuitka-1.7.5/README.pdf` & `Nuitka-1.7.6/README.pdf`

 * *Installing the 'pypdf' Python module from the 'python3-pypdf' package may produce a better output.*

 * *Files 0% similar despite different names*

#### dumppdf -adt {}

 * *error from `dumppdf -adt {}`:*

 * *DEBUG:pdfminer.psparser:seek: 0*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b''*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b'%%EOF'*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b'340862'*

 * *DEBUG:pdfminer.pdfdocument:find_xref: b'startxref'*

 * *DEBUG:pdfminer.pdfdocument:xref found: pos=b'340862'*

 * *DEBUG:pdfminer.psparser:seek: 340862*

 * *DEBUG:pdfminer.psparser:nexttoken: (340862, /b'xref')*

 * *DEBUG:pdfminer.pdfdocument:read_xref_from: start=340862, token=/b'xref'*

 * *DEBUG:pdfminer.psparser:nextline: 340866, b'\n'*

 * *DEBUG:pdfminer.psparser:nextline: 340867, b'0 230\n'*

 * *DEBUG:pdfminer.psparser:nextline: 340873, b'0000000000 65535 f \n'*

 * *DEBUG:pdfminer.psparser:nextline: 340893, b'0000000073 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 340913, b'0000000195 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 340933, b'0000000302 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 340953, b'0000000414 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 340973, b'0000000519 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 340993, b'0000000687 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 341013, b'0000000802 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 341033, b'0000000970 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 341053, b'0000001089 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 341073, b'0000001320 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 341093, b'0000001528 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 341113, b'0000001717 00000 n \n'*

 * *DEBUG:pdfminer.psparser:nextline: 341133, b'0000001912 00000 n \n'*

 * *[ truncated after 25 lines; 10014 ignored ]*

```diff
@@ -2453,21 +2453,21 @@
 </object>
 
 <object id="72">
 <dict size="9">
 <key>Author</key>
 <value><string size="0"></string></value>
 <key>CreationDate</key>
-<value><string size="23">D:20230714152907+00&#39;00&#39;</string></value>
+<value><string size="23">D:20230723195039+00&#39;00&#39;</string></value>
 <key>Creator</key>
 <value><string size="13">&#40;unspecified&#41;</string></value>
 <key>Keywords</key>
 <value><string size="0"></string></value>
 <key>ModDate</key>
-<value><string size="23">D:20230714152907+00&#39;00&#39;</string></value>
+<value><string size="23">D:20230723195039+00&#39;00&#39;</string></value>
 <key>Producer</key>
 <value><string size="41">ReportLab PDF Library - www.reportlab.com</string></value>
 <key>Subject</key>
 <value><string size="13">&#40;unspecified&#41;</string></value>
 <key>Title</key>
 <value><string size="18">Nuitka User Manual</string></value>
 <key>Trapped</key>
@@ -5206,16 +5206,16 @@
 </dict>
 </object>
 
 <trailer>
 <dict size="4">
 <key>ID</key>
 <value><list size="2">
-<string size="16">{k&#223;&#202;&#224;&#152;&#199;&#14;&#17;&#249;t&#25;&#34;qc&#31;</string>
-<string size="16">{k&#223;&#202;&#224;&#152;&#199;&#14;&#17;&#249;t&#25;&#34;qc&#31;</string>
+<string size="16">&#209;&#92;&#172;V&#199;&#175;i&#242;y&#131;k&#41;Sn&#222;&#60;</string>
+<string size="16">&#209;&#92;&#172;V&#199;&#175;i&#242;y&#131;k&#41;Sn&#222;&#60;</string>
 </list></value>
 <key>Info</key>
 <value><ref id="72" /></value>
 <key>Root</key>
 <value><ref id="71" /></value>
 <key>Size</key>
 <value><number>230</number></value>
```

### Comparing `Nuitka-1.7.5/README.rst` & `Nuitka-1.7.6/README.rst`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/bin/autoformat-nuitka-source` & `Nuitka-1.7.6/bin/autoformat-nuitka-source`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/bin/check-nuitka-with-pylint` & `Nuitka-1.7.6/bin/check-nuitka-with-pylint`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/bin/compare_with_cpython` & `Nuitka-1.7.6/bin/compare_with_cpython`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/bin/compare_with_xml` & `Nuitka-1.7.6/bin/compare_with_xml`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/bin/measure-construct-performance` & `Nuitka-1.7.6/bin/measure-construct-performance`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/bin/nuitka` & `Nuitka-1.7.6/bin/nuitka`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/bin/nuitka-run` & `Nuitka-1.7.6/bin/nuitka-run`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/doc/Logo/Nuitka-Logo-Horizontal.svg` & `Nuitka-1.7.6/doc/Logo/Nuitka-Logo-Horizontal.svg`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/doc/Logo/Nuitka-Logo-Symbol.svg` & `Nuitka-1.7.6/doc/Logo/Nuitka-Logo-Symbol.svg`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/doc/Logo/Nuitka-Logo-Vertical.svg` & `Nuitka-1.7.6/doc/Logo/Nuitka-Logo-Vertical.svg`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/doc/images/Nuitka-Logo-Horizontal.png` & `Nuitka-1.7.6/doc/images/Nuitka-Logo-Horizontal.png`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/doc/images/Nuitka-Logo-Symbol.png` & `Nuitka-1.7.6/doc/images/Nuitka-Logo-Symbol.png`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/doc/images/Nuitka-Logo-Vertical.png` & `Nuitka-1.7.6/doc/images/Nuitka-Logo-Vertical.png`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/doc/nuitka2-run.1` & `Nuitka-1.7.6/doc/nuitka2-run.1`

 * *Files 0% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 .\" DO NOT MODIFY THIS FILE!  It was generated by help2man 1.48.1.
-.TH NUITKA-RUN "1" "July 2023" "nuitka-run 1.7.5" "User Commands"
+.TH NUITKA-RUN "1" "July 2023" "nuitka-run 1.7.6" "User Commands"
 .SH NAME
 nuitka-run \- the Python compiler
 .SH SYNOPSIS
 .B nuitka-run
 [\fI\,options\/\fR] \fI\,main_module.py\/\fR
 .SH OPTIONS
 .TP
```

### Comparing `Nuitka-1.7.5/doc/nuitka2.1` & `Nuitka-1.7.6/doc/nuitka2.1`

 * *Files 0% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 .\" DO NOT MODIFY THIS FILE!  It was generated by help2man 1.48.1.
-.TH NUITKA "1" "July 2023" "nuitka 1.7.5" "User Commands"
+.TH NUITKA "1" "July 2023" "nuitka 1.7.6" "User Commands"
 .SH NAME
 nuitka \- the Python compiler
 .SH SYNOPSIS
 .B nuitka
 [\fI\,--module\/\fR] [\fI\,--run\/\fR] [\fI\,options\/\fR] \fI\,main_module.py\/\fR
 .SH OPTIONS
 .TP
```

### Comparing `Nuitka-1.7.5/doc/nuitka3-run.1` & `Nuitka-1.7.6/doc/nuitka3-run.1`

 * *Files 0% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 .\" DO NOT MODIFY THIS FILE!  It was generated by help2man 1.48.1.
-.TH NUITKA-RUN "1" "July 2023" "nuitka-run 1.7.5" "User Commands"
+.TH NUITKA-RUN "1" "July 2023" "nuitka-run 1.7.6" "User Commands"
 .SH NAME
 nuitka-run \- the Python compiler
 .SH SYNOPSIS
 .B nuitka-run
 [\fI\,options\/\fR] \fI\,main_module.py\/\fR
 .SH OPTIONS
 .TP
```

### Comparing `Nuitka-1.7.5/doc/nuitka3.1` & `Nuitka-1.7.6/doc/nuitka3.1`

 * *Files 0% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 .\" DO NOT MODIFY THIS FILE!  It was generated by help2man 1.48.1.
-.TH NUITKA "1" "July 2023" "nuitka 1.7.5" "User Commands"
+.TH NUITKA "1" "July 2023" "nuitka 1.7.6" "User Commands"
 .SH NAME
 nuitka \- the Python compiler
 .SH SYNOPSIS
 .B nuitka
 [\fI\,--module\/\fR] [\fI\,--run\/\fR] [\fI\,options\/\fR] \fI\,main_module.py\/\fR
 .SH OPTIONS
 .TP
```

### Comparing `Nuitka-1.7.5/lib/hints.py` & `Nuitka-1.7.6/lib/hints.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/misc/nuitka-run.bat` & `Nuitka-1.7.6/misc/nuitka-run.bat`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/misc/nuitka.bat` & `Nuitka-1.7.6/misc/nuitka.bat`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/Builtins.py` & `Nuitka-1.7.6/nuitka/Builtins.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/BytecodeCaching.py` & `Nuitka-1.7.6/nuitka/BytecodeCaching.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/Bytecodes.py` & `Nuitka-1.7.6/nuitka/Bytecodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/CacheCleanup.py` & `Nuitka-1.7.6/nuitka/CacheCleanup.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/Constants.py` & `Nuitka-1.7.6/nuitka/Constants.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/Errors.py` & `Nuitka-1.7.6/nuitka/Errors.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/MainControl.py` & `Nuitka-1.7.6/nuitka/MainControl.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/ModuleRegistry.py` & `Nuitka-1.7.6/nuitka/ModuleRegistry.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/OptionParsing.py` & `Nuitka-1.7.6/nuitka/OptionParsing.py`

 * *Files 0% similar despite different names*

```diff
@@ -324,15 +324,15 @@
 )
 
 onefile_group.add_option(
     "--onefile-child-grace-time",
     action="store",
     dest="onefile_child_grace_time",
     metavar="GRACE_TIME_MS",
-    default="5000",
+    default=None,
     help="""\
 When stopping the child, e.g. due to CTRL-C or shutdown, etc. the
 Python code gets a "KeyboardInterrupt", that it may handle e.g. to
 flush data. This is the amount of time in ms, before the child it
 killed in the hard way. Unit is ms, and default 5000.""",
 )
```

### Comparing `Nuitka-1.7.5/nuitka/Options.py` & `Nuitka-1.7.6/nuitka/Options.py`

 * *Files 3% similar despite different names*

```diff
@@ -363,14 +363,50 @@
     if options.is_standalone:
         options.python_flags.insert(0, "no_site")
 
     # Check onefile tempdir spec.
     if options.onefile_tempdir_spec:
         _checkOnefileTargetSpec()
 
+        if not options.is_onefile:
+            Tracing.options_logger.warning(
+                """\
+Using onefile specific option '--onefile-windows-splash-screen-image' has no effect \
+when '--onefile' is not specified."""
+            )
+
+    # Check onefile splash image
+    if options.splash_screen_image:
+        if not os.path.exists(options.splash_screen_image):
+            Tracing.options_logger.sysexit(
+                "Error, splash screen image path '%s' does not exist."
+                % options.splash_screen_image
+            )
+
+        if not options.is_onefile:
+            Tracing.options_logger.warning(
+                """\
+Using onefile specific option '--onefile-windows-splash-screen-image' has no effect \
+when '--onefile' is not specified."""
+            )
+
+    if options.onefile_child_grace_time is not None:
+        if not options.onefile_child_grace_time.isdigit():
+            Tracing.options_logger.sysexit(
+                """\
+Error, value given for '--onefile-child-grace-time' must be integer."""
+            )
+
+        if not options.is_onefile:
+            Tracing.options_logger.warning(
+                """\
+Using onefile specific option '--onefile-windows-splash-screen-image' has no effect \
+when '--onefile-child-grace-time' is not specified."""
+            )
+
     if options.force_stdout_spec:
         checkPathSpec(
             options.force_stdout_spec, "--force-stdout-spec", allow_disable=True
         )
 
     if options.force_stderr_spec:
         checkPathSpec(
@@ -1372,15 +1408,15 @@
     """:returns: bool derived from ``--show-scons``"""
     return options.show_scons
 
 
 def getJobLimit():
     """*int*, value of ``--jobs`` / "-j" or number of CPU kernels"""
     if options.jobs is None:
-        if options.low_memory:
+        if isLowMemory():
             return 1
         else:
             return getCPUCoreCount()
 
     return int(options.jobs)
 
 
@@ -1605,15 +1641,19 @@
 
     # This changes the '/' to '\' on Windows at least.
     return os.path.normpath(result)
 
 
 def getOnefileChildGraceTime():
     """*int* = ``--onefile-child-grace-time``"""
-    return int(options.onefile_child_grace_time)
+    return (
+        int(options.onefile_child_grace_time)
+        if options.onefile_child_grace_time is not None
+        else 5000
+    )
 
 
 def shallNotCompressOnefile():
     """*bool* = ``--onefile-no-compression``"""
     return options.onefile_no_compression
```

### Comparing `Nuitka-1.7.5/nuitka/OutputDirectories.py` & `Nuitka-1.7.6/nuitka/OutputDirectories.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/PostProcessing.py` & `Nuitka-1.7.6/nuitka/PostProcessing.py`

 * *Files 1% similar despite different names*

```diff
@@ -41,15 +41,15 @@
     putTextFileContents,
     removeFileExecutablePermission,
 )
 from nuitka.utils.Images import convertImageToIconFormat
 from nuitka.utils.MacOSApp import createPlistInfoFile
 from nuitka.utils.SharedLibraries import (
     callInstallNameTool,
-    convertRPathToRunPath,
+    cleanupHeaderForAndroid,
 )
 from nuitka.utils.Utils import isAndroidBasedLinux, isMacOS, isWin32Windows
 from nuitka.utils.WindowsResources import (
     RT_GROUP_ICON,
     RT_ICON,
     RT_RCDATA,
     addResourceToFile,
@@ -373,16 +373,16 @@
             os.path.dirname(result_filename),
             "lib" + os.path.basename(result_filename)[:-4] + ".a",
         )
 
         if os.path.exists(candidate):
             os.unlink(candidate)
 
-    if isAndroidBasedLinux() and not Options.shallMakeModule():
-        convertRPathToRunPath(result_filename)
+    if isAndroidBasedLinux():
+        cleanupHeaderForAndroid(result_filename)
 
     # Might have to create a CMD file, potentially with debugger run.
     if Options.shallCreateCmdFileForExecution():
         dll_directory = getExternalUsePath(os.path.dirname(getTargetPythonDLLPath()))
 
         cmd_filename = OutputDirectories.getResultRunFilename(onefile=False)
```

### Comparing `Nuitka-1.7.5/nuitka/Progress.py` & `Nuitka-1.7.6/nuitka/Progress.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/PythonFlavors.py` & `Nuitka-1.7.6/nuitka/PythonFlavors.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/PythonOperators.py` & `Nuitka-1.7.6/nuitka/PythonOperators.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/PythonVersions.py` & `Nuitka-1.7.6/nuitka/PythonVersions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/Serialization.py` & `Nuitka-1.7.6/nuitka/Serialization.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/SourceCodeReferences.py` & `Nuitka-1.7.6/nuitka/SourceCodeReferences.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/Tracing.py` & `Nuitka-1.7.6/nuitka/Tracing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/TreeXML.py` & `Nuitka-1.7.6/nuitka/TreeXML.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/Variables.py` & `Nuitka-1.7.6/nuitka/Variables.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/Version.py` & `Nuitka-1.7.6/nuitka/Version.py`

 * *Files 4% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 #     limitations under the License.
 #
 """ Nuitka version related stuff.
 
 """
 
 version_string = """\
-Nuitka V1.7.5
+Nuitka V1.7.6
 Copyright (C) 2023 Kay Hayen."""
 
 
 def getNuitkaVersion():
     """Return Nuitka version as a string.
 
     This should not be used for >= comparisons directly.
```

### Comparing `Nuitka-1.7.5/nuitka/__init__.py` & `Nuitka-1.7.6/nuitka/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/__main__.py` & `Nuitka-1.7.6/nuitka/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/__past__.py` & `Nuitka-1.7.6/nuitka/__past__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/Backend.scons` & `Nuitka-1.7.6/nuitka/build/Backend.scons`

 * *Files 0% similar despite different names*

```diff
@@ -956,14 +956,17 @@
 
     if main_module_name != "__main__":
         build_definitions["NUITKA_MAIN_PACKAGE_MODE"] = 1
 
     createDefinitionsFile(source_dir, "build_definitions.h", build_definitions)
 
 
+if forced_stderr_path and not forced_stdout_path:
+    env.Append(CPPDEFINES=["NUITKA_STDERR_NOT_VISIBLE"])
+
 createBuildDefinitionsFile()
 
 # The meta path based loader might want to respect that, so it does verbose traces in module
 # mode, mostly for debugging purposes only.
 if module_mode and python_sysflag_verbose:
     env.Append(CPPDEFINES=["_NUITKA_SYSFLAG_VERBOSE=1"])
```

### Comparing `Nuitka-1.7.5/nuitka/build/CCompilerVersion.scons` & `Nuitka-1.7.6/nuitka/build/CCompilerVersion.scons`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/DataComposerInterface.py` & `Nuitka-1.7.6/nuitka/build/DataComposerInterface.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/Onefile.scons` & `Nuitka-1.7.6/nuitka/build/Onefile.scons`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/SconsCaching.py` & `Nuitka-1.7.6/nuitka/build/SconsCaching.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/SconsCompilerSettings.py` & `Nuitka-1.7.6/nuitka/build/SconsCompilerSettings.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/SconsHacks.py` & `Nuitka-1.7.6/nuitka/build/SconsHacks.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/SconsInterface.py` & `Nuitka-1.7.6/nuitka/build/SconsInterface.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/SconsProgress.py` & `Nuitka-1.7.6/nuitka/build/SconsProgress.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/SconsSpawn.py` & `Nuitka-1.7.6/nuitka/build/SconsSpawn.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/SconsUtils.py` & `Nuitka-1.7.6/nuitka/build/SconsUtils.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/__init__.py` & `Nuitka-1.7.6/nuitka/build/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/allocator.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/allocator.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/builtins.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/builtins.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/calling.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/calling.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/checkers.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/checkers.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/checksum_tools.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/checksum_tools.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_asyncgen.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_asyncgen.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_cell.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_cell.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_coroutine.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_coroutine.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_frame.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_frame.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_function.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_function.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_generator.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_generator.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/compiled_method.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/compiled_method.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/constants.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/constants.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/constants_blob.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/constants_blob.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/exceptions.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/exceptions.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/filesystem_paths.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/filesystem_paths.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/freelists.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/freelists.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/hedley.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/hedley.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/attributes.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/attributes.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/boolean.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/boolean.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/bytearrays.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/bytearrays.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/bytes.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/bytes.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/calling_generated.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/calling_generated.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_eq.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_eq.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_ge.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_ge.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_gt.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_gt.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_le.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_le.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_lt.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_lt.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/comparisons_ne.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/comparisons_ne.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/complex.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/complex.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/dictionaries.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/dictionaries.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/floats.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/floats.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/import_hard.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/import_hard.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/indexes.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/indexes.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/ints.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/ints.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/iterators.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/iterators.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/lists.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/lists.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/lists_generated.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/lists_generated.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/mappings.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/mappings.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_add.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_add.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_bitand.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_bitand.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_bitor.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_bitor.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_bitxor.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_bitxor.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_divmod.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_divmod.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_floordiv.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_floordiv.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_lshift.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_lshift.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_matmult.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_matmult.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_mod.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_mod.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_mult.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_mult.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_olddiv.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_olddiv.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_pow.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_pow.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_rshift.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_rshift.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_sub.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_sub.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_binary_truediv.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_binary_truediv.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_builtin_types.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_builtin_types.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_add.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_add.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_bitand.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_bitand.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_bitor.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_bitor.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_bitxor.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_bitxor.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_floordiv.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_floordiv.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_lshift.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_lshift.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_matmult.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_matmult.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_mod.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_mod.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_mult.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_mult.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_olddiv.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_olddiv.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_pow.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_pow.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_rshift.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_rshift.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_sub.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_sub.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/operations_inplace_truediv.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/operations_inplace_truediv.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/raising.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/raising.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/rangeobjects.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/rangeobjects.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/richcomparisons.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/richcomparisons.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/sequences.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/sequences.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/sets.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/sets.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/slices.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/slices.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/strings.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/strings.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/subscripts.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/subscripts.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helper/tuples.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helper/tuples.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/helpers.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/helpers.h`

 * *Files 2% similar despite different names*

```diff
@@ -275,14 +275,17 @@
 
 // For built-in staticmethod() functionality.
 extern PyObject *BUILTIN_STATICMETHOD(PyObject *function);
 
 // For built-in classmethod() functionality.
 extern PyObject *BUILTIN_CLASSMETHOD(PyObject *function);
 
+// For built-in input() functionality, prompt can be NULL.
+extern PyObject *BUILTIN_INPUT(PyObject *prompt);
+
 // For built-in "int()" functionality with 2 arguments.
 extern PyObject *BUILTIN_INT2(PyObject *value, PyObject *base);
 
 #if PYTHON_VERSION < 0x300
 // For built-in "long()" functionality with 2 arguments.
 extern PyObject *BUILTIN_LONG2(PyObject *value, PyObject *base);
 #endif
```

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/importing.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/importing.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/incbin.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/incbin.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/prelude.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/prelude.h`

 * *Files 4% similar despite different names*

```diff
@@ -323,24 +323,35 @@
 #define NUITKA_CROSS_MODULE
 #define NUITKA_LOCAL_MODULE static
 
 /* Due to ABI issues, it seems that on Windows the symbols used by
  * "_PyObject_GC_TRACK" were not exported before 3.8 and we need to use a
  * function that does it instead.
  *
- * TODO: Make it work for Win32 Python <= 3.7 too.
- * TODO: The Python 3.7.0 on Linux doesn't work this way either, was a bad
- * CPython release apparently.
+ * The Python 3.7.0 release on at Linux doesn't work this way either, was
+ * a bad CPython release apparently and between 3.7.3 and 3.7.4 these have
+ * become runtime incompatible.
  */
 #if (defined(_WIN32) || defined(__MSYS__)) && PYTHON_VERSION < 0x380
 #define Nuitka_GC_Track PyObject_GC_Track
 #define Nuitka_GC_UnTrack PyObject_GC_UnTrack
+#undef _PyObject_GC_TRACK
+#undef _PyObject_GC_UNTRACK
 #elif PYTHON_VERSION == 0x370
 #define Nuitka_GC_Track PyObject_GC_Track
 #define Nuitka_GC_UnTrack PyObject_GC_UnTrack
+#undef _PyObject_GC_TRACK
+#undef _PyObject_GC_UNTRACK
+#elif defined(_NUITKA_MODULE) && PYTHON_VERSION >= 0x370 && PYTHON_VERSION < 0x380
+#define Nuitka_GC_Track PyObject_GC_Track
+#define Nuitka_GC_UnTrack PyObject_GC_UnTrack
+#undef _PyObject_GC_TRACK
+#undef _PyObject_GC_UNTRACK
+#undef PyThreadState_GET
+#define PyThreadState_GET PyThreadState_Get
 #else
 #define Nuitka_GC_Track _PyObject_GC_TRACK
 #define Nuitka_GC_UnTrack _PyObject_GC_UNTRACK
 #endif
 
 #if _NUITKA_EXPERIMENTAL_FAST_THREAD_GET && PYTHON_VERSION >= 0x300 && PYTHON_VERSION < 0x370
 // We are careful, access without locking under the assumption that we hold
```

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/printing.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/printing.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/python_pgo.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/python_pgo.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/safe_string_ops.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/safe_string_ops.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/threading.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/threading.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/tracing.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/tracing.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/include/nuitka/unfreezing.h` & `Nuitka-1.7.6/nuitka/build/include/nuitka/unfreezing.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/appdirs/LICENSE.txt` & `Nuitka-1.7.6/nuitka/build/inline_copy/appdirs/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/appdirs/appdirs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/appdirs/appdirs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/atomicwrites/LICENSE` & `Nuitka-1.7.6/nuitka/build/inline_copy/atomicwrites/LICENSE`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/atomicwrites/atomicwrites.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/atomicwrites/atomicwrites.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/bin/scons.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/bin/scons.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/clcache/clcache/LICENSE` & `Nuitka-1.7.6/nuitka/build/inline_copy/clcache/clcache/LICENSE`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/clcache/clcache/caching.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/clcache/clcache/caching.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/colorama/LICENSE.txt` & `Nuitka-1.7.6/nuitka/build/inline_copy/colorama/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/ansi.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/ansi.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/ansitowin32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/ansitowin32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/initialise.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/initialise.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/win32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/win32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/colorama/colorama/winterm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/colorama/colorama/winterm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/glob2/LICENSE` & `Nuitka-1.7.6/nuitka/build/inline_copy/glob2/LICENSE`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/glob2/glob2/compat.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/glob2/glob2/compat.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/glob2/glob2/fnmatch.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/glob2/glob2/fnmatch.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/glob2/glob2/impl.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/glob2/glob2/impl.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/LICENSE.rst` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/LICENSE.rst`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/_compat.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/_compat.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/_identifier.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/_identifier.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/bccache.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/bccache.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/compiler.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/compiler.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/constants.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/constants.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/debug.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/debug.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/defaults.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/defaults.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/environment.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/environment.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/exceptions.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/exceptions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/ext.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/ext.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/filters.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/filters.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/idtracking.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/idtracking.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/lexer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/lexer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/loaders.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/loaders.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/meta.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/meta.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/nativetypes.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/nativetypes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/nodes.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/nodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/optimizer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/optimizer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/parser.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/parser.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/runtime.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/runtime.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/sandbox.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/sandbox.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/tests.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/tests.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/utils.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/utils.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2/jinja2/visitor.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2/jinja2/visitor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/LICENSE.rst` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/LICENSE.rst`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/_compat.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/_compat.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/_identifier.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/_identifier.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/bccache.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/bccache.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/compiler.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/compiler.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/constants.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/constants.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/debug.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/debug.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/defaults.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/defaults.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/environment.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/environment.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/exceptions.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/exceptions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/ext.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/ext.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/filters.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/filters.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/idtracking.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/idtracking.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/lexer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/lexer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/loaders.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/loaders.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/meta.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/meta.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/nativetypes.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/nativetypes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/nodes.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/nodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/optimizer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/optimizer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/parser.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/parser.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/runtime.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/runtime.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/sandbox.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/sandbox.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/tests.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/tests.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/utils.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/utils.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/jinja2_35/jinja2/visitor.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/jinja2_35/jinja2/visitor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Action.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Action.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Builder.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Builder.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/CacheDir.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/CacheDir.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Conftest.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Conftest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Debug.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Debug.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Defaults.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Defaults.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Environment.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Environment.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Errors.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Errors.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Executor.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Executor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Job.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Job.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Memoize.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Memoize.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/Alias.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/Alias.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/FS.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/FS.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/Python.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/Python.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Node/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/BoolOption.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/BoolOption.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/EnumOption.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/EnumOption.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/ListOption.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/ListOption.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/PackageOption.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/PackageOption.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/PathOption.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/PathOption.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Options/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/PathList.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/PathList.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/aix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/aix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/cygwin.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/cygwin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/darwin.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/darwin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/hpux.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/hpux.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/irix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/irix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/os2.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/os2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/posix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/posix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/sunos.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/sunos.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/win32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Platform/win32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/SConf.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/SConf.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/SConsign.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/SConsign.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/C.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/C.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/Dir.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/Dir.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/Prog.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/Prog.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/RC.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/RC.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Scanner/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/Interactive.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/Interactive.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/Main.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/Main.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/SConsOptions.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/SConsOptions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/SConscript.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/SConscript.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Script/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Sig.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Sig.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Subst.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Subst.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Taskmaster.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Taskmaster.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/386asm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/386asm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/BitKeeper.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/BitKeeper.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/CVS.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/CVS.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/GettextCommon.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/GettextCommon.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/arch.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/arch.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/common.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/common.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/netframework.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/netframework.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/sdk.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/sdk.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/vc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/vc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/vs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/MSCommon/vs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/Perforce.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/Perforce.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/PharLapCommon.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/PharLapCommon.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/RCS.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/RCS.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/SCCS.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/SCCS.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/Subversion.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/Subversion.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixc++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixc++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixf77.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixf77.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixlink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/aixlink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/applelink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/applelink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/as.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/as.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/bcc32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/bcc32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/c++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/c++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/cc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/cc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/cyglink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/cyglink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/default.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/default.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/docbook/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/docbook/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/filesystem.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/filesystem.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/g++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/g++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/g77.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/g77.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gas.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gas.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gdc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gdc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gettext.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gettext.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gfortran.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gfortran.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gnulink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/gnulink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hpc++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hpc++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hpcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hpcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hplink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/hplink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/icc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/icc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/icl.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/icl.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ilink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ilink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ilink32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/ilink32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/install.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/install.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/intelc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/intelc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/lex.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/lex.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/link.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/link.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/linkloc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/linkloc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/m4.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/m4.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/masm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/masm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mingw.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mingw.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msgfmt.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msgfmt.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msginit.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msginit.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msgmerge.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msgmerge.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mslib.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mslib.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mslink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mslink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mssdk.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mssdk.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msvc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msvc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msvs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/msvs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mwcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mwcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mwld.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/mwld.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/nasm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/nasm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/rmic.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/rmic.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/rpcgen.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/rpcgen.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgiar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgiar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgic++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgic++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgicc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgicc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgilink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sgilink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunc++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunc++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/suncc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/suncc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunlink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/sunlink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/tar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/tar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/textfile.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/textfile.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/tlib.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/tlib.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/wix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/wix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/xgettext.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/xgettext.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/zip.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Tool/zip.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Util.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Util.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/BoolVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/BoolVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/EnumVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/EnumVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/ListVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/ListVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/PackageVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/PackageVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/PathVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/PathVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Variables/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Warnings.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/Warnings.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_builtins.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_builtins.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_collections.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_collections.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_dbm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_dbm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_hashlib.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_hashlib.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_io.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_io.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_sets.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_sets.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_subprocess.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/compat/_scons_subprocess.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/cpp.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/cpp.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/dblite.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/dblite.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/exitfuncs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-2.3.2/SCons/exitfuncs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Action.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Action.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Builder.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Builder.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/CacheDir.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/CacheDir.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Conftest.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Conftest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Debug.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Debug.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Defaults.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Defaults.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Environment.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Environment.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Errors.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Errors.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Executor.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Executor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Job.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Job.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Memoize.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Memoize.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/Alias.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/Alias.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/FS.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/FS.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/Python.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/Python.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Node/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/PathList.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/PathList.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/aix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/aix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/cygwin.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/cygwin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/darwin.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/darwin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/hpux.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/hpux.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/irix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/irix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/mingw.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/mingw.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/os2.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/os2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/posix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/posix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/sunos.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/sunos.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/virtualenv.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/virtualenv.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/win32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Platform/win32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/SConf.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/SConf.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/SConsign.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/SConsign.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/C.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/C.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/Dir.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/Dir.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/Prog.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/Prog.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/RC.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/RC.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Scanner/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/Interactive.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/Interactive.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/Main.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/Main.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/SConsOptions.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/SConsOptions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/SConscript.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/SConscript.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Script/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Subst.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Subst.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Taskmaster.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Taskmaster.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/386asm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/386asm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/GettextCommon.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/GettextCommon.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/arch.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/arch.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/common.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/common.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/netframework.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/netframework.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/sdk.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/sdk.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/vc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/vc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/vs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/MSCommon/vs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/PharLapCommon.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/PharLapCommon.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixc++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixc++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixcxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixcxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixlink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/aixlink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/applelink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/applelink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/as.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/as.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/bcc32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/bcc32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/c++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/c++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clang.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clang.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clangxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/clangxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cyglink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/cyglink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/default.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/default.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/docbook/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/docbook/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/filesystem.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/filesystem.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/g++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/g++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gas.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gas.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gettext_tool.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gettext_tool.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gnulink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gnulink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/gxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpc++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpc++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpcxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hpcxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hplink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/hplink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/icc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/icc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/icl.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/icl.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ilink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ilink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ilink32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/ilink32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/install.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/install.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/intelc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/intelc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/link.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/link.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/linkloc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/linkloc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/m4.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/m4.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/masm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/masm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mingw.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mingw.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msgfmt.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msgfmt.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msginit.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msginit.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msgmerge.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msgmerge.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mslib.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mslib.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mslink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mslink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mssdk.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mssdk.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msvc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msvc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msvs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/msvs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mwcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mwcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mwld.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/mwld.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/nasm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/nasm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/rmic.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/rmic.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/rpcgen.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/rpcgen.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgiar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgiar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgic++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgic++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgicc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgicc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgicxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgicxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgilink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sgilink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunc++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunc++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/suncc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/suncc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/suncxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/suncxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunlink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/sunlink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/tar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/tar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/textfile.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/textfile.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/tlib.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/tlib.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/wix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/wix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/xgettext.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/xgettext.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/zip.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Tool/zip.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Util.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Util.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/BoolVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/BoolVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/EnumVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/EnumVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/ListVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/ListVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/PackageVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/PackageVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/PathVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/PathVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Variables/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Warnings.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/Warnings.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/_scons_dbm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/compat/_scons_dbm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/cpp.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/cpp.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/dblite.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/dblite.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/exitfuncs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-3.1.2/SCons/exitfuncs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Action.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Action.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Builder.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Builder.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/CacheDir.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/CacheDir.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Conftest.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Conftest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Debug.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Debug.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Defaults.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Defaults.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Environment.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Environment.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/EnvironmentValues.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/EnvironmentValues.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Errors.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Errors.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Executor.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Executor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Job.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Job.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Memoize.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Memoize.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/Alias.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/Alias.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/FS.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/FS.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/Python.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/Python.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Node/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/PathList.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/PathList.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/aix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/aix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/cygwin.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/cygwin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/darwin.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/darwin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/hpux.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/hpux.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/irix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/irix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/mingw.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/mingw.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/os2.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/os2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/posix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/posix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/sunos.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/sunos.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/virtualenv.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/virtualenv.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/win32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Platform/win32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/SConf.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/SConf.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/SConsign.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/SConsign.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/C.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/C.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/Dir.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/Dir.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/Prog.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/Prog.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/RC.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/RC.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Scanner/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/Interactive.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/Interactive.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/Main.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/Main.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/SConsOptions.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/SConsOptions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/SConscript.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/SConscript.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Script/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Subst.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Subst.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Taskmaster.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Taskmaster.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/386asm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/386asm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/GettextCommon.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/GettextCommon.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/arch.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/arch.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/common.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/common.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/netframework.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/netframework.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/sdk.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/sdk.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/vc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/vc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/vs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/MSCommon/vs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/PharLapCommon.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/PharLapCommon.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixc++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixc++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixcxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixcxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixlink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/aixlink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/applelink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/applelink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/as.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/as.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/asm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/asm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/bcc32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/bcc32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/c++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/c++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clang.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clang.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clangxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/clangxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cyglink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/cyglink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/default.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/default.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/filesystem.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/filesystem.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/g++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/g++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gas.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gas.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gettext_tool.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gettext_tool.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gnulink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gnulink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/gxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpc++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpc++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpcxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hpcxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hplink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/hplink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/icc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/icc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/icl.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/icl.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ilink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ilink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ilink32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/ilink32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/install.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/install.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/intelc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/intelc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/link.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/link.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/LoadableModule.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/LoadableModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/SharedLibrary.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/SharedLibrary.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkCommon/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkloc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/linkloc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/m4.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/m4.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/masm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/masm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mingw.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mingw.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msgfmt.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msgfmt.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msginit.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msginit.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msgmerge.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msgmerge.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mslib.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mslib.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mslink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mslink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mssdk.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mssdk.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msvc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msvc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msvs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/msvs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mwcc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mwcc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mwld.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/mwld.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/nasm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/nasm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/rmic.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/rmic.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/rpcgen.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/rpcgen.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgiar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgiar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgic++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgic++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgicc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgicc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgicxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgicxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgilink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sgilink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunc++.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunc++.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/suncc.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/suncc.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/suncxx.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/suncxx.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunlink.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/sunlink.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/tar.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/tar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/textfile.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/textfile.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/tlib.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/tlib.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/wix.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/wix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/xgettext.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/xgettext.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/zip.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Tool/zip.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Util.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Util.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/ConfigureCache.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/ConfigureCache.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/sconsign.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Utilities/sconsign.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/BoolVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/BoolVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/EnumVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/EnumVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/ListVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/ListVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/PackageVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/PackageVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/PathVariable.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/PathVariable.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Variables/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Warnings.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/Warnings.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/_scons_dbm.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/_scons_dbm.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/win32.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/compat/win32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/cpp.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/cpp.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/dblite.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/dblite.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/exitfuncs.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/lib/scons-4.3.0/SCons/exitfuncs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/LICENSE.rst` & `Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/LICENSE.rst`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/markupsafe/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/markupsafe/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/markupsafe/_compat.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/markupsafe/_compat.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/markupsafe/_constants.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/markupsafe/_constants.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/markupsafe/markupsafe/_native.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/markupsafe/markupsafe/_native.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/pkg_resources/pkg_resources/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/pkg_resources/pkg_resources/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/pkg_resources/pkg_resources/py31compat.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/pkg_resources/pkg_resources/py31compat.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_monitor.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_monitor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_tqdm_pandas.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_tqdm_pandas.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/_utils.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/_utils.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/auto.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/auto.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/autonotebook.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/autonotebook.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/dask.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/dask.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/gui.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/gui.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/notebook.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/notebook.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/std.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/std.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/tk.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/tk.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/tqdm/tqdm/utils.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/tqdm/tqdm/utils.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/LICENSE` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/LICENSE`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/composer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/composer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/constructor.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/constructor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/cyaml.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/cyaml.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/dumper.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/dumper.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/emitter.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/emitter.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/error.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/error.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/events.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/events.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/loader.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/loader.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/nodes.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/nodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/parser.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/parser.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/reader.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/reader.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/representer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/representer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/resolver.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/resolver.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/scanner.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/scanner.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/serializer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/serializer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml/yaml/tokens.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml/yaml/tokens.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/LICENSE` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/LICENSE`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/composer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/composer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/constructor.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/constructor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/cyaml.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/cyaml.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/dumper.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/dumper.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/emitter.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/emitter.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/error.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/error.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/events.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/events.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/loader.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/loader.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/nodes.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/nodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/parser.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/parser.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/reader.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/reader.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/representer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/representer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/resolver.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/resolver.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/scanner.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/scanner.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/serializer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/serializer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_27/yaml/tokens.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_27/yaml/tokens.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/LICENSE` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/LICENSE`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/__init__.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/composer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/composer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/constructor.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/constructor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/cyaml.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/cyaml.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/dumper.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/dumper.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/emitter.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/emitter.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/error.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/error.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/events.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/events.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/loader.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/loader.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/nodes.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/nodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/parser.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/parser.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/reader.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/reader.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/representer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/representer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/resolver.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/resolver.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/scanner.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/scanner.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/serializer.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/serializer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/yaml_35/yaml/tokens.py` & `Nuitka-1.7.6/nuitka/build/inline_copy/yaml_35/yaml/tokens.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/LICENSE.txt` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/bitstream.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/bitstream.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/compiler.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/compiler.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/cpu.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/cpu.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/debug.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/debug.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/entropy_common.c` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/entropy_common.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/error_private.c` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/error_private.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/error_private.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/error_private.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/fse.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/fse.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/fse_decompress.c` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/fse_decompress.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/huf.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/huf.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/mem.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/mem.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/xxhash.c` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/xxhash.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/xxhash.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/xxhash.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/zstd_common.c` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/zstd_common.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/zstd_deps.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/zstd_deps.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/zstd_errors.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/zstd_errors.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/common/zstd_internal.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/common/zstd_internal.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/huf_decompress.c` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/huf_decompress.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_ddict.c` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_ddict.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_ddict.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_ddict.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_decompress.c` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_decompress.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_block.c` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_block.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_block.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_block.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_internal.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/decompress/zstd_decompress_internal.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/inline_copy/zstd/zstd.h` & `Nuitka-1.7.6/nuitka/build/inline_copy/zstd/zstd.h`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/CompiledAsyncgenType.c` & `Nuitka-1.7.6/nuitka/build/static_src/CompiledAsyncgenType.c`

 * *Files 1% similar despite different names*

```diff
@@ -308,34 +308,41 @@
         assert(exception_type == NULL);
         assert(exception_value == NULL);
         assert(exception_tb == NULL);
     }
 
     if (asyncgen->m_status == status_Unused && value != NULL && value != Py_None) {
         // No exception if value is given.
+        Py_XDECREF(value);
 
         SET_CURRENT_EXCEPTION_TYPE0_STR(PyExc_TypeError, "can't send non-None value to a just-started async generator");
         return PYGEN_ERROR;
     }
 
     if (asyncgen->m_status != status_Finished) {
         if (asyncgen->m_running) {
+            Py_XDECREF(value);
+
             SET_CURRENT_EXCEPTION_TYPE0_STR(PyExc_ValueError, "async generator already executing");
             return PYGEN_ERROR;
         }
 
         PyThreadState *thread_state = PyThreadState_GET();
 
         // Put the asyncgen back on the frame stack.
         Nuitka_ThreadStateFrameType *return_frame = _Nuitka_GetThreadStateFrame(thread_state);
 
         // Consider it as running.
         if (asyncgen->m_status == status_Unused) {
             asyncgen->m_status = status_Running;
             assert(asyncgen->m_resume_frame == NULL);
+
+            // Value will not be used, can only be Py_None or NULL.
+            Py_XDECREF(value);
+            value = NULL;
         } else {
             assert(asyncgen->m_resume_frame);
             pushFrameStackGenerator(asyncgen->m_resume_frame);
 
             asyncgen->m_resume_frame = NULL;
         }
 
@@ -363,15 +370,17 @@
 #endif
 
         PyObject *yielded;
 
         if (asyncgen->m_yieldfrom == NULL) {
             yielded = ((asyncgen_code)asyncgen->m_code)(asyncgen, value);
         } else {
+            // This does not release the value if any, so we need to do it afterwards.
             yielded = Nuitka_YieldFromAsyncgenInitial(asyncgen, value);
+            Py_XDECREF(value);
         }
 
         // If the asyncgen returns with m_yieldfrom set, it wants us to yield
         // from that value from now on.
         while (yielded == NULL && asyncgen->m_yieldfrom != NULL) {
             yielded = Nuitka_YieldFromAsyncgenNext(asyncgen);
         }
@@ -454,25 +463,27 @@
                 return PYGEN_ERROR;
             }
 
             return PYGEN_ERROR;
         } else {
             // For normal yield, wrap the result value before returning.
             if (asyncgen->m_yieldfrom == NULL) {
-                // TODO: Why not transfer ownership to constructor.
+                // Transferred ownership to constructor of Nuitka_AsyncgenValueWrapper
                 PyObject *wrapped = Nuitka_AsyncgenValueWrapper_New(yielded);
                 yielded = wrapped;
 
                 assert(yielded != NULL);
             }
 
             *result = yielded;
             return PYGEN_NEXT;
         }
     } else {
+        Py_XDECREF(value);
+
         // Release exception if any, we are finished with it and will raise another.
         Py_XDECREF(exception_type);
         Py_XDECREF(exception_value);
         Py_XDECREF(exception_tb);
 
         return PYGEN_RETURN;
     }
@@ -903,20 +914,21 @@
         return NULL;
     }
 
     return Nuitka_AsyncgenAthrow_New(asyncgen, args);
 }
 
 #if PYTHON_VERSION >= 0x3a0
-static PySendResult _Nuitka_Asyncgen_amsend(struct Nuitka_AsyncgenObject *asyncgen, PyObject *arg, PyObject **result) {
+static PySendResult _Nuitka_Asyncgen_am_send(struct Nuitka_AsyncgenObject *asyncgen, PyObject *arg, PyObject **result) {
 #if _DEBUG_ASYNCGEN
     PRINT_ASYNCGEN_STATUS("Enter", asyncgen);
 #endif
 
     *result = NULL;
+    Py_INCREF(arg);
     PySendResult res = _Nuitka_Asyncgen_sendR(asyncgen, arg, false, NULL, NULL, NULL, result);
 
 #if _DEBUG_ASYNCGEN
     PRINT_ASYNCGEN_STATUS("Leave", asyncgen);
     PRINT_COROUTINE_VALUE("result", *result);
     PRINT_NEW_LINE();
 #endif
@@ -1053,15 +1065,15 @@
 
 static PyAsyncMethods Nuitka_Asyncgen_as_async = {
     0,                               // am_await
     0,                               // am_aiter (PyObject_SelfIter)
     (unaryfunc)Nuitka_Asyncgen_anext // am_anext
 #if PYTHON_VERSION >= 0x3a0
     ,
-    (sendfunc)_Nuitka_Asyncgen_amsend // am_anext
+    (sendfunc)_Nuitka_Asyncgen_am_send // am_send
 #endif
 };
 
 // TODO: Set "__doc__" automatically for method clones of compiled types from
 // the documentation of built-in original type.
 static PyGetSetDef Nuitka_Asyncgen_getsetlist[] = {
     {(char *)"__name__", (getter)Nuitka_Asyncgen_get_name, (setter)Nuitka_Asyncgen_set_name, NULL},
@@ -1279,16 +1291,15 @@
 
 // Note: This expects a reference given in value, because that is the
 // only way we use it.
 static PyObject *Nuitka_AsyncgenValueWrapper_New(PyObject *value) {
     CHECK_OBJECT(value);
 
 #if _DEBUG_REFCOUNTS
-    count_active_Nuitka_AsyncgenValueWrapper_Type -= 1;
-    count_released_Nuitka_AsyncgenValueWrapper_Type += 1;
+    count_active_Nuitka_AsyncgenValueWrapper_Type += 1;
 #endif
 
     struct Nuitka_AsyncgenWrappedValueObject *result;
 
     allocateFromFreeListFixed(free_list_asyncgen_value_wrappers, struct Nuitka_AsyncgenWrappedValueObject,
                               Nuitka_AsyncgenValueWrapper_Type);
 
@@ -1488,22 +1499,21 @@
         PRINT_NEW_LINE();
 #endif
     }
 
 #if PYTHON_VERSION >= 0x380
     asyncgen_asend->m_gen->m_running_async = true;
 #endif
-    // TODO: Who releases arg.
-    // Py_INCREF(arg);
 
 #if _DEBUG_ASYNCGEN
     PRINT_STRING("Deferring to _Nuitka_Asyncgen_send\n");
     PRINT_NEW_LINE();
 #endif
 
+    Py_INCREF(arg);
     PyObject *result = _Nuitka_Asyncgen_send(asyncgen_asend->m_gen, arg, false, NULL, NULL, NULL);
 
 #if _DEBUG_ASYNCGEN
     PRINT_STRING("Returned from _Nuitka_Asyncgen_send\n");
     PRINT_COROUTINE_VALUE("result", result);
     PRINT_CURRENT_EXCEPTION();
 #endif
```

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/CompiledCellType.c` & `Nuitka-1.7.6/nuitka/build/static_src/CompiledCellType.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/CompiledCodeHelpers.c` & `Nuitka-1.7.6/nuitka/build/static_src/CompiledCodeHelpers.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/CompiledCoroutineType.c` & `Nuitka-1.7.6/nuitka/build/static_src/CompiledCoroutineType.c`

 * *Files 1% similar despite different names*

```diff
@@ -211,30 +211,32 @@
     if (exception_type != NULL) {
         // Exception, was thrown into us, need to send that to sub-generator.
         // We acquired ownership of the published exception and need to release it potentially.
 
         // Transfer exception owner this.
         retval = _Nuitka_YieldFromPassExceptionTo(yieldfrom, exception_type, exception_value, exception_tb);
 
+        // TODO: This wants to look at retval most definitely, send_value is going to be NULL.
         if (unlikely(send_value == NULL)) {
             PyObject *error = GET_ERROR_OCCURRED();
 
             if (error != NULL && EXCEPTION_MATCH_BOOL_SINGLE(error, PyExc_StopIteration)) {
                 *returned_value = ERROR_GET_STOP_ITERATION_VALUE();
-
                 assert(!ERROR_OCCURRED());
+
                 return NULL;
             }
         }
     } else if (PyGen_CheckExact(yieldfrom) || PyCoro_CheckExact(yieldfrom)) {
         retval = Nuitka_PyGen_Send((PyGenObject *)yieldfrom, Py_None);
     } else if (send_value == Py_None && Nuitka_CoroutineWrapper_Check(yieldfrom)) {
         struct Nuitka_CoroutineObject *yieldfrom_coroutine =
             ((struct Nuitka_CoroutineWrapperObject *)yieldfrom)->m_coroutine;
 
+        Py_INCREF(Py_None);
         retval = _Nuitka_Coroutine_send(yieldfrom_coroutine, Py_None, mode ? false : true, NULL, NULL, NULL);
     } else if (send_value == Py_None && Py_TYPE(yieldfrom)->tp_iternext != NULL) {
         retval = Py_TYPE(yieldfrom)->tp_iternext(yieldfrom);
     } else {
 #if 0
         // TODO: Add slow mode traces.
         PRINT_ITEM(yieldfrom);
@@ -253,16 +255,17 @@
             *returned_value = Py_None;
         } else if (likely(EXCEPTION_MATCH_BOOL_SINGLE(error, PyExc_StopIteration))) {
             // The sub-generator has given an exception. In case of
             // StopIteration, we need to check the value, as it is going to be
             // the expression value of this "yield from", and we are done. All
             // other errors, we need to raise.
             *returned_value = ERROR_GET_STOP_ITERATION_VALUE();
-            assert(*returned_value != NULL);
             assert(!ERROR_OCCURRED());
+
+            assert(*returned_value != NULL);
         } else {
             *returned_value = NULL;
         }
 
         return NULL;
     } else {
         assert(!ERROR_OCCURRED());
@@ -388,43 +391,50 @@
     PRINT_COROUTINE_STRING("closing", closing ? "(closing) " : "(not closing) ");
     PRINT_COROUTINE_VALUE("value", value);
     PRINT_EXCEPTION(exception_type, exception_value, exception_tb);
     PRINT_CURRENT_EXCEPTION();
     PRINT_NEW_LINE();
 #endif
 
+    // Not both a value and an exception please.
     if (value != NULL) {
         assert(exception_type == NULL);
         assert(exception_value == NULL);
         assert(exception_tb == NULL);
     }
 
     if (coroutine->m_status == status_Unused && value != NULL && value != Py_None) {
         // No exception if value is given.
+        Py_XDECREF(value);
 
         SET_CURRENT_EXCEPTION_TYPE0_STR(PyExc_TypeError, "can't send non-None value to a just-started coroutine");
         return PYGEN_ERROR;
     }
 
     if (coroutine->m_status != status_Finished) {
         if (coroutine->m_running) {
+            Py_XDECREF(value);
+
             SET_CURRENT_EXCEPTION_TYPE0_STR(PyExc_ValueError, "coroutine already executing");
             return PYGEN_ERROR;
         }
 
         PyThreadState *thread_state = PyThreadState_GET();
 
         // Put the coroutine back on the frame stack.
         Nuitka_ThreadStateFrameType *return_frame = _Nuitka_GetThreadStateFrame(thread_state);
 
         // Consider it as running.
         if (coroutine->m_status == status_Unused) {
             coroutine->m_status = status_Running;
             assert(coroutine->m_resume_frame == NULL);
 
+            // Value will not be used, can only be Py_None or NULL.
+            Py_XDECREF(value);
+            value = NULL;
         } else {
             assert(coroutine->m_resume_frame);
             pushFrameStackGenerator(coroutine->m_resume_frame);
 
             coroutine->m_resume_frame = NULL;
         }
 
@@ -448,15 +458,17 @@
 #endif
 
         PyObject *yielded;
 
         if (coroutine->m_yieldfrom == NULL) {
             yielded = ((coroutine_code)coroutine->m_code)(coroutine, value);
         } else {
+            // This does not release the value if any, so we need to do it afterwards.
             yielded = Nuitka_YieldFromCoroutineInitial(coroutine, value);
+            Py_XDECREF(value);
         }
 
         // If the coroutine returns with m_yieldfrom set, it wants us to yield
         // from that value from now on.
         while (yielded == NULL && coroutine->m_yieldfrom != NULL) {
             yielded = Nuitka_YieldFromCoroutineNext(coroutine);
         }
@@ -564,14 +576,16 @@
                 return PYGEN_ERROR;
             }
         } else {
             *result = yielded;
             return PYGEN_NEXT;
         }
     } else {
+        Py_XDECREF(value);
+
         // Release exception if any, we are finished with it and will raise another.
         Py_XDECREF(exception_type);
         Py_XDECREF(exception_value);
         Py_XDECREF(exception_tb);
 
         /* This is for status_Finished */
         assert(coroutine->m_status == status_Finished);
@@ -632,16 +646,16 @@
     }
 }
 
 static PyObject *Nuitka_Coroutine_send(struct Nuitka_CoroutineObject *coroutine, PyObject *value) {
     CHECK_OBJECT(coroutine);
     CHECK_OBJECT(value);
 
-    // TODO: Does it release value ?
-    // Py_INCREF(value);
+    // We need to transfer ownership of the sent value.
+    Py_INCREF(value);
     PyObject *result = _Nuitka_Coroutine_send(coroutine, value, false, NULL, NULL, NULL);
 
     if (result == NULL) {
         if (GET_ERROR_OCCURRED() == NULL) {
             SET_CURRENT_EXCEPTION_TYPE0(PyExc_StopIteration);
         }
     }
@@ -850,14 +864,15 @@
 
 #if _DEBUG_COROUTINE
                 PRINT_COROUTINE_STATUS("Sending return value into ourselves", coroutine);
                 PRINT_COROUTINE_VALUE("value", val);
                 PRINT_NEW_LINE();
 #endif
 
+                // The ownership of val is transferred.
                 ret = _Nuitka_Coroutine_send(coroutine, val, false, NULL, NULL, NULL);
             } else {
 #if _DEBUG_COROUTINE
                 PRINT_COROUTINE_STATUS("Sending exception value into ourselves", coroutine);
                 PRINT_CURRENT_EXCEPTION();
                 PRINT_NEW_LINE();
 #endif
@@ -1049,20 +1064,22 @@
 
     Nuitka_GC_Track(result);
 
     return (PyObject *)result;
 }
 
 #if PYTHON_VERSION >= 0x3a0
-static PySendResult _Nuitka_Coroutine_amsend(struct Nuitka_CoroutineObject *coroutine, PyObject *arg,
-                                             PyObject **result) {
+static PySendResult _Nuitka_Coroutine_am_send(struct Nuitka_CoroutineObject *coroutine, PyObject *arg,
+                                              PyObject **result) {
 #if _DEBUG_COROUTINE
     PRINT_COROUTINE_STATUS("Enter", coroutine);
 #endif
 
+    // We need to transfer ownership of the sent value.
+    Py_INCREF(arg);
     PySendResult res = _Nuitka_Coroutine_sendR(coroutine, arg, false, NULL, NULL, NULL, result);
 
 #if _DEBUG_COROUTINE
     PRINT_COROUTINE_STATUS("Leave", coroutine);
     PRINT_COROUTINE_VALUE("result", *result);
     PRINT_NEW_LINE();
 #endif
@@ -1178,20 +1195,20 @@
 #if PYTHON_VERSION >= 0x370
     {(char *)"cr_origin", T_OBJECT, offsetof(struct Nuitka_CoroutineObject, m_origin), READONLY},
 
 #endif
     {NULL}};
 
 static PyAsyncMethods Nuitka_Coroutine_as_async = {
-    (unaryfunc)Nuitka_Coroutine_await, /* am_await */
-    0,                                 /* am_aiter */
-    0                                  /* am_anext */
+    (unaryfunc)Nuitka_Coroutine_await, // am_await
+    0,                                 // am_aiter
+    0                                  // am_anext
 #if PYTHON_VERSION >= 0x3a0
     ,
-    (sendfunc)_Nuitka_Coroutine_amsend /* am_send */
+    (sendfunc)_Nuitka_Coroutine_am_send // am_send
 #endif
 
 };
 
 PyTypeObject Nuitka_Coroutine_Type = {
     PyVarObject_HEAD_INIT(NULL, 0) "compiled_coroutine",                // tp_name
     sizeof(struct Nuitka_CoroutineObject),                              // tp_basicsize
@@ -1542,27 +1559,26 @@
 
                 SET_CURRENT_EXCEPTION_TYPE0_STR(PyExc_TypeError, "__await__() returned a coroutine");
 
                 return NULL;
             }
 
             if (unlikely(!HAS_ITERNEXT(result))) {
-                PyErr_Format(PyExc_TypeError, "__await__() returned non-iterator of type '%s'",
-                             Py_TYPE(result)->tp_name);
+                SET_CURRENT_EXCEPTION_TYPE_COMPLAINT("__await__() returned non-iterator of type '%s'", result);
 
                 Py_DECREF(result);
 
                 return NULL;
             }
         }
 
         return result;
     }
 
-    PyErr_Format(PyExc_TypeError, "object %s can't be used in 'await' expression", Py_TYPE(value)->tp_name);
+    SET_CURRENT_EXCEPTION_TYPE_COMPLAINT("object %s can't be used in 'await' expression", value);
 
     return NULL;
 }
 
 #if PYTHON_VERSION >= 0x366
 static void FORMAT_AWAIT_ERROR(PyObject *value, int await_kind) {
     CHECK_OBJECT(value);
@@ -1841,16 +1857,15 @@
     unaryfunc getter = NULL;
 
     if (Py_TYPE(value)->tp_as_async) {
         getter = Py_TYPE(value)->tp_as_async->am_anext;
     }
 
     if (unlikely(getter == NULL)) {
-        PyErr_Format(PyExc_TypeError, "'async for' requires an iterator with __anext__ method, got %s",
-                     Py_TYPE(value)->tp_name);
+        SET_CURRENT_EXCEPTION_TYPE_COMPLAINT("'async for' requires an iterator with __anext__ method, got %s", value);
 
         return NULL;
     }
 
     PyObject *next_value = (*getter)(value);
 
     if (unlikely(next_value == NULL)) {
```

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/CompiledFrameType.c` & `Nuitka-1.7.6/nuitka/build/static_src/CompiledFrameType.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/CompiledFunctionType.c` & `Nuitka-1.7.6/nuitka/build/static_src/CompiledFunctionType.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/CompiledGeneratorType.c` & `Nuitka-1.7.6/nuitka/build/static_src/CompiledGeneratorType.c`

 * *Files 1% similar despite different names*

```diff
@@ -320,21 +320,22 @@
     FETCH_ERROR_OCCURRED(&exception_type, &exception_value, &exception_tb);
 
     // Exception, was thrown into us, need to send that to sub-generator.
     if (exception_type != NULL) {
         // Passing ownership of exception fetch to it.
         retval = _Nuitka_YieldFromPassExceptionTo(yieldfrom, exception_type, exception_value, exception_tb);
 
+        // TODO: This wants to look at retval most definitely, send_value is going to be NULL.
         if (unlikely(send_value == NULL)) {
             PyObject *error = GET_ERROR_OCCURRED();
 
             if (error != NULL && EXCEPTION_MATCH_BOOL_SINGLE(error, PyExc_StopIteration)) {
                 generator->m_returned = ERROR_GET_STOP_ITERATION_VALUE();
-
                 assert(!ERROR_OCCURRED());
+
                 return NULL;
             }
         }
     } else if (PyGen_CheckExact(yieldfrom)) {
         retval = Nuitka_PyGen_Send((PyGenObject *)yieldfrom, Py_None);
     }
 #if PYTHON_VERSION >= 0x350
@@ -476,14 +477,16 @@
         assert(exception_type == NULL);
         assert(exception_value == NULL);
         assert(exception_tb == NULL);
     }
 
     if (generator->m_status != status_Finished) {
         if (generator->m_running) {
+            Py_XDECREF(value);
+
             SET_CURRENT_EXCEPTION_TYPE0_STR(PyExc_ValueError, "generator already executing");
             return NULL;
         }
 
         PyThreadState *thread_state = PyThreadState_GET();
 
 #if PYTHON_VERSION < 0x300
@@ -501,14 +504,17 @@
 #endif
 
         // Put the asyncgen back on the frame stack.
         Nuitka_ThreadStateFrameType *return_frame = _Nuitka_GetThreadStateFrame(thread_state);
 
         if (generator->m_status == status_Unused) {
             generator->m_status = status_Running;
+
+            Py_XDECREF(value);
+            value = NULL;
         } else {
             // Put the generator back on the frame stack.
             pushFrameStackGeneratorCompiledFrame(generator->m_frame);
         }
 
         // Continue the yielder function while preventing recursion.
         Nuitka_MarkGeneratorAsRunning(generator);
@@ -531,15 +537,17 @@
 
         PyObject *yielded;
 
 #if PYTHON_VERSION >= 0x300
         if (generator->m_yieldfrom == NULL) {
             yielded = ((generator_code)generator->m_code)(generator, value);
         } else {
+            // This does not release the value if any, so we need to do it afterwards.
             yielded = Nuitka_YieldFromGeneratorInitial(generator, value);
+            Py_XDECREF(value);
         }
 #else
         yielded = ((generator_code)generator->m_code)(generator, value);
 #endif
 
 #if PYTHON_VERSION >= 0x300
         // If the generator returns with m_yieldfrom set, it wants us to yield
@@ -719,32 +727,36 @@
         Nuitka_MarkGeneratorAsFinished(generator);
 #endif
 
         SET_CURRENT_EXCEPTION_TYPE0_STR(PyExc_TypeError, "can't send non-None value to a just-started generator");
         return NULL;
     }
 
+    // We need to transfer ownership of the sent value.
+    Py_INCREF(value);
     PyObject *result = _Nuitka_Generator_send(generator, value, NULL, NULL, NULL);
 
     if (result == NULL) {
         if (GET_ERROR_OCCURRED() == NULL) {
             SET_CURRENT_EXCEPTION_TYPE0(PyExc_StopIteration);
         }
     }
 
     return result;
 }
 
 static PyObject *Nuitka_Generator_tp_iternext(struct Nuitka_GeneratorObject *generator) {
+    Py_INCREF(Py_None);
     return _Nuitka_Generator_send(generator, Py_None, NULL, NULL, NULL);
 }
 
 /* Our own qiter interface, which is for quicker simple loop style iteration,
    that does not send anything in. */
 PyObject *Nuitka_Generator_qiter(struct Nuitka_GeneratorObject *generator, bool *finished) {
+    Py_INCREF(Py_None);
     PyObject *result = _Nuitka_Generator_send(generator, Py_None, NULL, NULL, NULL);
 
     if (result == NULL) {
         if (unlikely(!CHECK_AND_CLEAR_STOP_ITERATION_OCCURRED())) {
             *finished = false;
             return NULL;
         }
@@ -1431,16 +1443,16 @@
 
 // This is only used.
 #if PYTHON_VERSION >= 0x3a0
 static PyAsyncMethods Nuitka_Generator_as_async = {
     NULL, /* am_await */
     NULL, /* am_aiter */
     NULL, /* am_anext */
-    // TODO: have this too, (sendfunc)_Nuitka_Generator_amsend
-    NULL /* am_anext */
+    // TODO: have this too, (sendfunc)_Nuitka_Generator_am_send
+    NULL /* am_send */
 };
 #endif
 
 #include <structmember.h>
 
 PyTypeObject Nuitka_Generator_Type = {
     PyVarObject_HEAD_INIT(NULL, 0) "compiled_generator", // tp_name
```

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/CompiledGeneratorTypeUncompiledIntegration.c` & `Nuitka-1.7.6/nuitka/build/static_src/CompiledGeneratorTypeUncompiledIntegration.c`

 * *Files 0% similar despite different names*

```diff
@@ -683,15 +683,15 @@
             f->f_back = (PyFrameObject *)Py_NewRef(back);
         }
 
         frame->previous = NULL;
     }
 
     if (!_PyObject_GC_IS_TRACKED((PyObject *)f)) {
-        _PyObject_GC_TRACK((PyObject *)f);
+        Nuitka_GC_Track((PyObject *)f);
     }
 }
 
 // Cleanup up the frame is also not exported.
 static void _Nuitka_PyFrame_Clear(_PyInterpreterFrame *frame) {
     assert(frame->owner != FRAME_OWNED_BY_GENERATOR || _PyFrame_GetGenerator(frame)->gi_frame_state == FRAME_CLEARED);
```

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/CompiledMethodType.c` & `Nuitka-1.7.6/nuitka/build/static_src/CompiledMethodType.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersAllocator.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersAllocator.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersAttributes.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersAttributes.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersBuiltin.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersBuiltin.c`

 * *Files 2% similar despite different names*

```diff
@@ -239,14 +239,33 @@
     char const *arg_names[] = {"file", "mode", "buffering", "encoding", "errors", "newline", "closefd", "opener"};
 
     return CALL_BUILTIN_KW_ARGS(NUITKA_ACCESS_BUILTIN(open), args, arg_names, 8);
 }
 
 #endif
 
+NUITKA_DEFINE_BUILTIN(input);
+
+PyObject *BUILTIN_INPUT(PyObject *prompt) {
+    NUITKA_ASSIGN_BUILTIN(input);
+
+#if NUITKA_STDERR_NOT_VISIBLE && (PYTHON_VERSION >= 0x300 || !defined(_WIN32))
+    if (prompt != NULL) {
+        PRINT_ITEM(prompt);
+        prompt = NULL;
+    }
+#endif
+
+    if (prompt == NULL) {
+        return CALL_FUNCTION_NO_ARGS(NUITKA_ACCESS_BUILTIN(input));
+    } else {
+        return CALL_FUNCTION_WITH_SINGLE_ARG(NUITKA_ACCESS_BUILTIN(input), prompt);
+    }
+}
+
 /** The "staticmethod" built-in.
  *
  **/
 
 NUITKA_DEFINE_BUILTIN(staticmethod)
 
 PyObject *BUILTIN_STATICMETHOD(PyObject *value) {
```

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersBuiltinTypeMethods.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersBuiltinTypeMethods.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersBytes.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersBytes.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersCalling.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersCalling.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersCallingGenerated.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersCallingGenerated.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersChecksumTools.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersChecksumTools.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersClasses.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersClasses.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonEq.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonEq.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonEqUtils.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonEqUtils.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonGe.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonGe.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonGt.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonGt.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonLe.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonLe.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonLt.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonLt.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersComparisonNe.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersComparisonNe.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersConstantsBlob.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersConstantsBlob.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersDeepcopy.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersDeepcopy.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersDictionaries.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersDictionaries.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersDictionariesGenerated.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersDictionariesGenerated.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersExceptions.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersExceptions.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersFiles.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersFiles.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersFilesystemPaths.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersFilesystemPaths.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersFloats.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersFloats.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersHeapStorage.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersHeapStorage.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersImport.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersImport.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersImportHard.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersImportHard.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersLists.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersLists.c`

 * *Files 0% similar despite different names*

```diff
@@ -330,15 +330,15 @@
 
     return false;
 }
 #endif
 
 bool LIST_APPEND1(PyObject *target, PyObject *item) {
 #if _NUITKA_EXPERIMENTAL_DISABLE_LIST_OPT
-    int res == PyList_Append(target, item);
+    int res = PyList_Append(target, item);
     Py_DECREF(item);
     return res == 0;
 #else
     CHECK_OBJECT(target);
     assert(PyList_CheckExact(target));
 
     CHECK_OBJECT(item);
@@ -358,15 +358,15 @@
 
     return true;
 #endif
 }
 
 bool LIST_APPEND0(PyObject *target, PyObject *item) {
 #if _NUITKA_EXPERIMENTAL_DISABLE_LIST_OPT
-    int res == PyList_Append(target, item);
+    int res = PyList_Append(target, item);
     return res == 0;
 #else
     CHECK_OBJECT(target);
     assert(PyList_CheckExact(target));
 
     CHECK_OBJECT(item);
```

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersListsGenerated.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersListsGenerated.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersMappings.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersMappings.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersMatching.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersMatching.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryAdd.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryAdd.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryAddUtils.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryAddUtils.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryBitand.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryBitand.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryBitor.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryBitor.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryBitxor.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryBitxor.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryDivmod.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryDivmod.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryDivmodUtils.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryDivmodUtils.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryFloordiv.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryFloordiv.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryInplaceAdd.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryInplaceAdd.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryLshift.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryLshift.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryMatmult.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryMatmult.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryMod.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryMod.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryMult.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryMult.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryMultUtils.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryMultUtils.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryOlddiv.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryOlddiv.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryPow.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryPow.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryPowUtils.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryPowUtils.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryRshift.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryRshift.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinarySub.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinarySub.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationBinaryTruediv.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationBinaryTruediv.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceAdd.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceAdd.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceAddUtils.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceAddUtils.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceBitand.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceBitand.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceBitor.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceBitor.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceBitxor.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceBitxor.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceFloordiv.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceFloordiv.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceLshift.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceLshift.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceMatmult.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceMatmult.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceMod.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceMod.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceMult.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceMult.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceOlddiv.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceOlddiv.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplacePow.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplacePow.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceRshift.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceRshift.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceSub.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceSub.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersOperationInplaceTruediv.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersOperationInplaceTruediv.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersProfiling.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersProfiling.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersPythonPgo.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersPythonPgo.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersRaising.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersRaising.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersSafeStrings.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersSafeStrings.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersSequences.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersSequences.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersSlices.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersSlices.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersStrings.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersStrings.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersTuples.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersTuples.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/HelpersTypes.c` & `Nuitka-1.7.6/nuitka/build/static_src/HelpersTypes.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/InspectPatcher.c` & `Nuitka-1.7.6/nuitka/build/static_src/InspectPatcher.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/MainProgram.c` & `Nuitka-1.7.6/nuitka/build/static_src/MainProgram.c`

 * *Files 0% similar despite different names*

```diff
@@ -328,15 +328,55 @@
     setlocale(LC_ALL, old_locale);
     free(old_locale);
 
     return argv_copy;
 }
 #endif
 
+#if _DEBUG_REFCOUNTS
+static void PRINT_REFCOUNTS(void) {
+    // spell-checker: ignore Asend, Athrow
+
+    PRINT_STRING("REFERENCE counts at program end:\n");
+    PRINT_STRING("active | allocated | released\n");
+#if PYTHON_VERSION >= 0x350
+    PRINT_FORMAT("Compiled Coroutines: %d | %d | %d\n", count_active_Nuitka_Coroutine_Type,
+                 count_allocated_Nuitka_Coroutine_Type, count_released_Nuitka_Coroutine_Type);
+    PRINT_FORMAT("Compiled Coroutines Wrappers: %d | %d | %d\n", count_active_Nuitka_CoroutineWrapper_Type,
+                 count_allocated_Nuitka_CoroutineWrapper_Type, count_released_Nuitka_CoroutineWrapper_Type);
+
+    PRINT_FORMAT("Compiled Coroutines AIter Wrappers: %d | %d | %d\n", count_active_Nuitka_AIterWrapper_Type,
+                 count_allocated_Nuitka_AIterWrapper_Type, count_released_Nuitka_AIterWrapper_Type);
+#endif
+#if PYTHON_VERSION >= 0x360
+    PRINT_FORMAT("Compiled Asyncgen: %d | %d | %d\n", count_active_Nuitka_Asyncgen_Type,
+                 count_allocated_Nuitka_Asyncgen_Type, count_released_Nuitka_Asyncgen_Type);
+    PRINT_FORMAT("Compiled Asyncgen Wrappers: %d | %d | %d\n", count_active_Nuitka_AsyncgenValueWrapper_Type,
+                 count_allocated_Nuitka_AsyncgenValueWrapper_Type, count_released_Nuitka_AsyncgenValueWrapper_Type);
+    PRINT_FORMAT("Compiled Asyncgen Asend: %d | %d | %d\n", count_active_Nuitka_AsyncgenAsend_Type,
+                 count_allocated_Nuitka_AsyncgenAsend_Type, count_released_Nuitka_AsyncgenAsend_Type);
+    PRINT_FORMAT("Compiled Asyncgen Athrow: %d | %d | %d\n", count_active_Nuitka_AsyncgenAthrow_Type,
+                 count_allocated_Nuitka_AsyncgenAthrow_Type, count_released_Nuitka_AsyncgenAthrow_Type);
+#endif
+
+    PRINT_FORMAT("Compiled Frames: %d | %d | %d (cache usage may occur)\n", count_active_Nuitka_Frame_Type,
+                 count_allocated_Nuitka_Frame_Type, count_released_Nuitka_Frame_Type);
+    PRINT_STRING("CACHED counts at program end:\n");
+    PRINT_STRING("active | allocated | released | hits\n");
+    PRINT_FORMAT("Cached Frames: %d | %d | %d | %d\n", count_active_frame_cache_instances,
+                 count_allocated_frame_cache_instances, count_released_frame_cache_instances,
+                 count_hit_frame_cache_instances);
+}
+#endif
+
 static int HANDLE_PROGRAM_EXIT(void) {
+#if _DEBUG_REFCOUNTS
+    PRINT_REFCOUNTS();
+#endif
+
     int exit_code;
 
     PyThreadState *thread_state = PyThreadState_GET();
 
     if (HAS_ERROR_OCCURRED(thread_state)) {
 #if PYTHON_VERSION >= 0x300
         /* Remove the frozen importlib traceback part, which would not be compatible. */
@@ -476,48 +516,14 @@
                 }
             }
 #endif
         }
     }
 }
 
-#if _DEBUG_REFCOUNTS
-static void PRINT_REFCOUNTS(void) {
-    PRINT_STRING("REFERENCE counts at program end:\n");
-    PRINT_STRING("active | allocated | released\n");
-#if PYTHON_VERSION >= 0x350
-    PRINT_FORMAT("Compiled Coroutines: %d | %d | %d\n", count_active_Nuitka_Coroutine_Type,
-                 count_allocated_Nuitka_Coroutine_Type, count_released_Nuitka_Coroutine_Type);
-    PRINT_FORMAT("Compiled Coroutines Wrappers: %d | %d | %d\n", count_active_Nuitka_CoroutineWrapper_Type,
-                 count_allocated_Nuitka_CoroutineWrapper_Type, count_released_Nuitka_CoroutineWrapper_Type);
-
-    PRINT_FORMAT("Compiled Coroutines AIter Wrappers: %d | %d | %d\n", count_active_Nuitka_AIterWrapper_Type,
-                 count_allocated_Nuitka_AIterWrapper_Type, count_released_Nuitka_AIterWrapper_Type);
-#endif
-#if PYTHON_VERSION >= 0x360
-    PRINT_FORMAT("Compiled Asyncgen: %d | %d | %d\n", count_active_Nuitka_Asyncgen_Type,
-                 count_allocated_Nuitka_Asyncgen_Type, count_released_Nuitka_Asyncgen_Type);
-    PRINT_FORMAT("Compiled Asyncgen Wrappers: %d | %d | %d\n", count_active_Nuitka_AsyncgenValueWrapper_Type,
-                 count_allocated_Nuitka_AsyncgenValueWrapper_Type, count_released_Nuitka_AsyncgenValueWrapper_Type);
-    PRINT_FORMAT("Compiled Asyncgen Asend: %d | %d | %d\n", count_active_Nuitka_AsyncgenAsend_Type,
-                 count_allocated_Nuitka_AsyncgenAsend_Type, count_released_Nuitka_AsyncgenAsend_Type);
-    PRINT_FORMAT("Compiled Asyncgen Athrow: %d | %d | %d\n", count_active_Nuitka_AsyncgenAthrow_Type,
-                 count_allocated_Nuitka_AsyncgenAthrow_Type, count_released_Nuitka_AsyncgenAthrow_Type);
-#endif
-
-    PRINT_FORMAT("Compiled Frames: %d | %d | %d (cache usage may occur)\n", count_active_Nuitka_Frame_Type,
-                 count_allocated_Nuitka_Frame_Type, count_released_Nuitka_Frame_Type);
-    PRINT_STRING("CACHED counts at program end:\n");
-    PRINT_STRING("active | allocated | released | hits\n");
-    PRINT_FORMAT("Cached Frames: %d | %d | %d | %d\n", count_active_frame_cache_instances,
-                 count_allocated_frame_cache_instances, count_released_frame_cache_instances,
-                 count_hit_frame_cache_instances);
-}
-#endif
-
 #if defined(_NUITKA_ONEFILE_MODE) && defined(_WIN32)
 
 static long onefile_ppid;
 
 DWORD WINAPI doOnefileParentMonitoring(LPVOID lpParam) {
     NUITKA_PRINT_TRACE("Onefile parent monitoring starts.");
 
@@ -1562,18 +1568,14 @@
     checkModuleConstants___main__();
 #endif
 
 #endif
 
     int exit_code = HANDLE_PROGRAM_EXIT();
 
-#if _DEBUG_REFCOUNTS
-    PRINT_REFCOUNTS();
-#endif
-
     NUITKA_PRINT_TIMING("main(): Calling Py_Exit.");
     Py_Exit(exit_code);
 
     // The "Py_Exit()" calls is not supposed to return.
     NUITKA_CANNOT_GET_HERE("Py_Exit does not return");
 }
```

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/MetaPathBasedLoader.c` & `Nuitka-1.7.6/nuitka/build/static_src/MetaPathBasedLoader.c`

 * *Files 0% similar despite different names*

```diff
@@ -1375,15 +1375,21 @@
         basename = entry->name;
     } else {
         basename += 1;
     }
 
     copyStringSafe(filename_buffer, basename, sizeof(filename_buffer));
 
-    if ((entry->flags & NUITKA_PACKAGE_FLAG) != 0) {
+    if ((entry->flags & NUITKA_EXTENSION_MODULE_FLAG) != 0) {
+#if defined(_WIN32)
+        appendStringSafe(filename_buffer, ".pyd", sizeof(filename_buffer));
+#else
+        appendStringSafe(filename_buffer, ".so", sizeof(filename_buffer));
+#endif
+    } else if ((entry->flags & NUITKA_PACKAGE_FLAG) != 0) {
         appendCharSafe(filename_buffer, SEP, sizeof(filename_buffer));
         appendStringSafe(filename_buffer, "__init__.py", sizeof(filename_buffer));
     } else {
         appendStringSafe(filename_buffer, ".py", sizeof(filename_buffer));
     }
 
     PyObject *module_filename = Nuitka_String_FromString(filename_buffer);
```

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/MetaPathBasedLoaderImportlibMetadataDistribution.c` & `Nuitka-1.7.6/nuitka/build/static_src/MetaPathBasedLoaderImportlibMetadataDistribution.c`

 * *Files 2% similar despite different names*

```diff
@@ -42,17 +42,17 @@
     static PyObject *importlib_metadata_distribution = NULL;
     // TODO: Use pathlib.Path for "locate_file" result should be more compatible.
 
     if (nuitka_distribution_type == NULL) {
         static char const *nuitka_distribution_code = "\n\
 import os,sys\n\
 if sys.version_info >= (3, 8):\n\
-    from importlib.metadata import Distribution,distribution,EntryPoints\n\
+    from importlib.metadata import Distribution,distribution\n\
 else:\n\
-    from importlib_metadata import Distribution,distribution,EntryPoints\n\
+    from importlib_metadata import Distribution,distribution\n\
 class nuitka_distribution(Distribution):\n\
     def __init__(self, base_path, metadata, entry_points):\n\
         self.base_path = base_path; self.metadata_data = metadata\n\
         self.entry_points_data = entry_points\n\
     def read_text(self, filename):\n\
         if filename == 'METADATA':\n\
             return self.metadata_data\n\
```

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/MetaPathBasedLoaderResourceReader.c` & `Nuitka-1.7.6/nuitka/build/static_src/MetaPathBasedLoaderResourceReader.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/MetaPathBasedLoaderResourceReaderFiles.c` & `Nuitka-1.7.6/nuitka/build/static_src/MetaPathBasedLoaderResourceReaderFiles.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/OnefileBootstrap.c` & `Nuitka-1.7.6/nuitka/build/static_src/OnefileBootstrap.c`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/build/static_src/OnefileSplashScreen.cpp` & `Nuitka-1.7.6/nuitka/build/static_src/OnefileSplashScreen.cpp`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/AsyncgenCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/AsyncgenCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/AttributeCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/AttributeCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/BinaryOperationHelperDefinitions.py` & `Nuitka-1.7.6/nuitka/code_generation/BinaryOperationHelperDefinitions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/BranchCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/BranchCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/BuiltinCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/BuiltinCodes.py`

 * *Files 2% similar despite different names*

```diff
@@ -118,14 +118,28 @@
             emit=emit,
             context=context,
         )
 
         context.addCleanupTempName(value_name)
 
 
+def generateBuiltinInputCode(to_name, expression, emit, context):
+    generateCAPIObjectCode(
+        to_name=to_name,
+        capi="BUILTIN_INPUT",
+        arg_desc=(("input_arg", expression.subnode_prompt),),
+        may_raise=expression.mayRaiseExceptionOperation(),
+        conversion_check=decideConversionCheckNeeded(to_name, expression),
+        none_null=True,
+        source_ref=expression.getCompatibleSourceReference(),
+        emit=emit,
+        context=context,
+    )
+
+
 def generateBuiltinOpenCode(to_name, expression, emit, context):
     arg_desc = (
         ("open_filename", expression.subnode_filename),
         ("open_mode", expression.subnode_mode),
         ("open_buffering", expression.subnode_buffering),
     )
```

### Comparing `Nuitka-1.7.5/nuitka/code_generation/CallCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/CallCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ClassCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ClassCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/CodeGeneration.py` & `Nuitka-1.7.6/nuitka/code_generation/CodeGeneration.py`

 * *Files 1% similar despite different names*

```diff
@@ -60,14 +60,15 @@
     generateBuiltinBytearray1Code,
     generateBuiltinBytearray3Code,
     generateBuiltinClassmethodCode,
     generateBuiltinComplex1Code,
     generateBuiltinComplex2Code,
     generateBuiltinFloatCode,
     generateBuiltinHexCode,
+    generateBuiltinInputCode,
     generateBuiltinOctCode,
     generateBuiltinOpenCode,
     generateBuiltinRange1Code,
     generateBuiltinRange2Code,
     generateBuiltinRange3Code,
     generateBuiltinRefCode,
     generateBuiltinStaticmethodCode,
@@ -662,14 +663,15 @@
         "EXPRESSION_MATCH_TYPE_CHECK_SEQUENCE": generateMatchTypeCheckSequenceCode,
         "EXPRESSION_MATCH_TYPE_CHECK_MAPPING": generateMatchTypeCheckMappingCode,
         "EXPRESSION_BUILTIN_DIR1": generateBuiltinDir1Code,
         "EXPRESSION_BUILTIN_VARS": generateBuiltinVarsCode,
         "EXPRESSION_BUILTIN_HASATTR": generateBuiltinHasattrCode,
         "EXPRESSION_BUILTIN_GETATTR": generateBuiltinGetattrCode,
         "EXPRESSION_BUILTIN_SETATTR": generateBuiltinSetattrCode,
+        "EXPRESSION_BUILTIN_INPUT": generateBuiltinInputCode,
         "EXPRESSION_BUILTIN_OPEN_P2": generateBuiltinOpenCode,
         "EXPRESSION_BUILTIN_OPEN_P3": generateBuiltinOpenCode,
         "EXPRESSION_BUILTIN_STATICMETHOD": generateBuiltinStaticmethodCode,
         "EXPRESSION_BUILTIN_CLASSMETHOD": generateBuiltinClassmethodCode,
         "EXPRESSION_BUILTIN_RANGE1": generateBuiltinRange1Code,
         "EXPRESSION_BUILTIN_RANGE2": generateBuiltinRange2Code,
         "EXPRESSION_BUILTIN_RANGE3": generateBuiltinRange3Code,
```

### Comparing `Nuitka-1.7.5/nuitka/code_generation/CodeHelperSelection.py` & `Nuitka-1.7.6/nuitka/code_generation/CodeHelperSelection.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/CodeHelpers.py` & `Nuitka-1.7.6/nuitka/code_generation/CodeHelpers.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/CodeObjectCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/CodeObjectCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ComparisonCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ComparisonCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ComparisonHelperDefinitions.py` & `Nuitka-1.7.6/nuitka/code_generation/ComparisonHelperDefinitions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ConditionalCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ConditionalCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ConstantCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ConstantCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/Contexts.py` & `Nuitka-1.7.6/nuitka/code_generation/Contexts.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/CoroutineCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/CoroutineCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/CtypesCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/CtypesCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/DictCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/DictCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/Emission.py` & `Nuitka-1.7.6/nuitka/code_generation/Emission.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ErrorCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ErrorCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/EvalCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/EvalCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ExceptionCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ExceptionCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ExpressionCTypeSelectionHelpers.py` & `Nuitka-1.7.6/nuitka/code_generation/ExpressionCTypeSelectionHelpers.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ExpressionCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ExpressionCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/FrameCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/FrameCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/FunctionCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/FunctionCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/GeneratorCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/GeneratorCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/GlobalConstants.py` & `Nuitka-1.7.6/nuitka/code_generation/GlobalConstants.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/GlobalsLocalsCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/GlobalsLocalsCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/IdCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/IdCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ImportCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ImportCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/Indentation.py` & `Nuitka-1.7.6/nuitka/code_generation/Indentation.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/IndexCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/IndexCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/InjectCCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/InjectCCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/IntegerCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/IntegerCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/IteratorCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/IteratorCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/LabelCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/LabelCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/LineNumberCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/LineNumberCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ListCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ListCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/LoaderCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/LoaderCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/LocalsDictCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/LocalsDictCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/LoopCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/LoopCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/MatchCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/MatchCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ModuleCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ModuleCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/Namify.py` & `Nuitka-1.7.6/nuitka/code_generation/Namify.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/OperationCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/OperationCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/PackageResourceCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/PackageResourceCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/PrintCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/PrintCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/PythonAPICodes.py` & `Nuitka-1.7.6/nuitka/code_generation/PythonAPICodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/RaisingCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/RaisingCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/Reports.py` & `Nuitka-1.7.6/nuitka/code_generation/Reports.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/ReturnCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/ReturnCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/SetCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/SetCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/SliceCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/SliceCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/StringCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/StringCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/SubscriptCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/SubscriptCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/TryCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/TryCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/TupleCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/TupleCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/VariableCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/VariableCodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/VariableDeclarations.py` & `Nuitka-1.7.6/nuitka/code_generation/VariableDeclarations.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/YieldCodes.py` & `Nuitka-1.7.6/nuitka/code_generation/YieldCodes.py`

 * *Files 2% similar despite different names*

```diff
@@ -115,16 +115,17 @@
 
     yield_return_name = VariableDeclaration(
         "PyObject *", "yield_return_value", None, None
     )
 
     getErrorExitCode(check_name=yield_return_name, emit=emit, context=context)
 
-    # Called with object
+    # Called with object, so we can simply do this.
     emit("%s = %s;" % (to_name, yield_return_name))
+    context.addCleanupTempName(to_name)
 
 
 def generateYieldCode(to_name, expression, emit, context):
     (value_name,) = generateChildExpressionsCode(
         expression=expression, emit=emit, context=context
     )
 
@@ -189,16 +190,14 @@
             yield_code=yield_code,
             resume_code=None,
             preserve_exception=preserve_exception,
             emit=emit,
             context=context,
         )
 
-        context.addCleanupTempName(result_name)
-
 
 def generateYieldFromWaitableCode(to_name, expression, emit, context):
 
     # In handlers, we must preserve/restore the exception.
     preserve_exception = expression.isExceptionPreserving()
 
     (awaited_name,) = generateChildExpressionsCode(
@@ -233,20 +232,14 @@
             yield_code=yield_code,
             resume_code=resume_code,
             preserve_exception=preserve_exception,
             emit=emit,
             context=context,
         )
 
-        # TODO: Seems to be redundant with and _getYieldPreserveCode doing
-        # it and could be removed
-        getErrorExitCode(check_name=result_name, emit=emit, context=context)
-
-        context.addCleanupTempName(result_name)
-
 
 def getYieldReturnDispatchCode(context):
     function_dispatch = [
         "case %(index)d: goto yield_return_%(index)d;" % {"index": yield_index}
         for yield_index in range(context.getLabelCount("yield_return"), 0, -1)
     ]
```

### Comparing `Nuitka-1.7.5/nuitka/code_generation/__init__.py` & `Nuitka-1.7.6/nuitka/code_generation/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeBases.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeBases.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeBooleans.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeBooleans.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeCFloats.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeCFloats.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeCLongs.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeCLongs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeModuleDictVariables.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeModuleDictVariables.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeNuitkaBooleans.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeNuitkaBooleans.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeNuitkaInts.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeNuitkaInts.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeNuitkaVoids.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeNuitkaVoids.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypePyObjectPointers.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypePyObjectPointers.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/CTypeVoids.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/CTypeVoids.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/c_types/__init__.py` & `Nuitka-1.7.6/nuitka/code_generation/c_types/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesAsyncgens.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesAsyncgens.py`

 * *Files 5% similar despite different names*

```diff
@@ -29,14 +29,15 @@
 %(function_local_types)s
 };
 #endif
 
 static PyObject *%(function_identifier)s_context(struct Nuitka_AsyncgenObject *asyncgen, PyObject *yield_return_value) {
     CHECK_OBJECT(asyncgen);
     assert(Nuitka_Asyncgen_Check((PyObject *)asyncgen));
+    CHECK_OBJECT_X(yield_return_value);
 
 #if %(has_heap_declaration)s
     // Heap access.
 %(heap_declaration)s
 #endif
 
     // Dispatch to yield based on return label index:
```

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesConstants.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesConstants.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesCoroutines.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesCoroutines.py`

 * *Files 6% similar despite different names*

```diff
@@ -29,14 +29,15 @@
 %(function_local_types)s
 };
 #endif
 
 static PyObject *%(function_identifier)s_context(struct Nuitka_CoroutineObject *coroutine, PyObject *yield_return_value) {
     CHECK_OBJECT(coroutine);
     assert(Nuitka_Coroutine_Check((PyObject *)coroutine));
+    CHECK_OBJECT_X(yield_return_value);
 
 #if %(has_heap_declaration)s
     // Heap access.
 %(heap_declaration)s
 #endif
 
     // Dispatch to yield based on return label index:
```

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesExceptions.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesExceptions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesFrames.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesFrames.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesFunction.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesFunction.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesGeneratorFunction.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesGeneratorFunction.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesIterators.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesIterators.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesLoader.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesLoader.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesModules.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesModules.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/CodeTemplatesVariables.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/CodeTemplatesVariables.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/TemplateDebugWrapper.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/TemplateDebugWrapper.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates/__init__.py` & `Nuitka-1.7.6/nuitka/code_generation/templates/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateCallsMethodPositional.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateCallsMethodPositional.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateCallsMixed.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateCallsMixed.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateCallsPositional.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateCallsPositional.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateCallsPositionalMethodDescr.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateCallsPositionalMethodDescr.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateMakeListHinted.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateMakeListHinted.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/CodeTemplateMakeListSmall.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/CodeTemplateMakeListSmall.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperBuiltinMethodOperation.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperBuiltinMethodOperation.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperDictionaryCopy.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperDictionaryCopy.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperImportHard.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperImportHard.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperLongTools.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperLongTools.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperObjectTools.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperObjectTools.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationBinary.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationBinary.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparison.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparison.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonBytes.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonBytes.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonFloat.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonFloat.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonInt.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonInt.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonList.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonList.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonLong.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonLong.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonStr.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonStr.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonTuple.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonTuple.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationComparisonUnicode.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationComparisonUnicode.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperOperationInplace.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperOperationInplace.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsBinary.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsBinary.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsBytes.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsBytes.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsCommon.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsCommon.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsFloat.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsFloat.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsInt.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsInt.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsList.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsList.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsLong.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsLong.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsSet.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsSet.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsStr.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsStr.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsTuple.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsTuple.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/code_generation/templates_c/HelperSlotsUnicode.c.j2` & `Nuitka-1.7.6/nuitka/code_generation/templates_c/HelperSlotsUnicode.c.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/containers/Namedtuples.py` & `Nuitka-1.7.6/nuitka/containers/Namedtuples.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/containers/OrderedDicts.py` & `Nuitka-1.7.6/nuitka/containers/OrderedDicts.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/containers/OrderedSets.py` & `Nuitka-1.7.6/nuitka/containers/OrderedSets.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/containers/OrderedSetsFallback.py` & `Nuitka-1.7.6/nuitka/containers/OrderedSetsFallback.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/containers/__init__.py` & `Nuitka-1.7.6/nuitka/containers/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/distutils/Build.py` & `Nuitka-1.7.6/nuitka/distutils/Build.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/distutils/DistutilCommands.py` & `Nuitka-1.7.6/nuitka/distutils/DistutilCommands.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/distutils/__init__.py` & `Nuitka-1.7.6/nuitka/distutils/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/finalizations/Finalization.py` & `Nuitka-1.7.6/nuitka/finalizations/Finalization.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/finalizations/FinalizeMarkups.py` & `Nuitka-1.7.6/nuitka/finalizations/FinalizeMarkups.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/finalizations/__init__.py` & `Nuitka-1.7.6/nuitka/finalizations/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/freezer/DependsExe.py` & `Nuitka-1.7.6/nuitka/freezer/DependsExe.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/freezer/DllDependenciesCommon.py` & `Nuitka-1.7.6/nuitka/freezer/DllDependenciesCommon.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/freezer/DllDependenciesMacOS.py` & `Nuitka-1.7.6/nuitka/freezer/DllDependenciesMacOS.py`

 * *Files 3% similar despite different names*

```diff
@@ -183,14 +183,25 @@
                 candidate = os.path.join(library_dir, path)
                 if os.path.exists(candidate):
                     resolved_path = os.path.normpath(candidate)
                     break
         else:
             resolved_path = path
 
+        # Some extension modules seem to reference themselves a wrong name,
+        # duplicating their module name into the filename, but that does
+        # not exist.
+        if not os.path.exists(resolved_path) and package_name is not None:
+            parts = os.path.basename(resolved_path).split(".")
+
+            if parts[0] == package_name.asString():
+                resolved_path = os.path.join(
+                    os.path.dirname(resolved_path), ".".join(parts[1:])
+                )
+
         # Some extension modules seem to reference themselves by a different
         # extension module name, so use that if it exists.
         if not os.path.exists(resolved_path) and python_version >= 0x300:
             so_suffixes = getSharedLibrarySuffixes()[:-1]
 
             specific_suffix = so_suffixes[0]
             abi_suffix = so_suffixes[1]
```

### Comparing `Nuitka-1.7.5/nuitka/freezer/DllDependenciesPosix.py` & `Nuitka-1.7.6/nuitka/freezer/DllDependenciesPosix.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/freezer/DllDependenciesWin32.py` & `Nuitka-1.7.6/nuitka/freezer/DllDependenciesWin32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/freezer/IncludedDataFiles.py` & `Nuitka-1.7.6/nuitka/freezer/IncludedDataFiles.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/freezer/IncludedEntryPoints.py` & `Nuitka-1.7.6/nuitka/freezer/IncludedEntryPoints.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/freezer/Onefile.py` & `Nuitka-1.7.6/nuitka/freezer/Onefile.py`

 * *Files 2% similar despite different names*

```diff
@@ -44,16 +44,22 @@
 from nuitka.utils.FileOperations import (
     areSamePaths,
     getExternalUsePath,
     getFileContents,
     removeDirectory,
 )
 from nuitka.utils.InstalledPythons import findInstalledPython
+from nuitka.utils.SharedLibraries import cleanupHeaderForAndroid
 from nuitka.utils.Signing import addMacOSCodeSignature
-from nuitka.utils.Utils import isMacOS, isWin32OrPosixWindows, isWin32Windows
+from nuitka.utils.Utils import (
+    isAndroidBasedLinux,
+    isMacOS,
+    isWin32OrPosixWindows,
+    isWin32Windows,
+)
 from nuitka.utils.WindowsResources import RT_RCDATA, addResourceToFile
 
 
 def packDistFolderToOnefile(dist_dir):
     """Pack distribution to onefile, i.e. a single file that is directly executable."""
 
     onefile_output_filename = getResultFullpath(onefile=True)
@@ -153,14 +159,15 @@
         attachOnefilePayload(
             dist_dir=dist_dir,
             onefile_output_filename=onefile_output_filename,
             start_binary=start_binary,
             expect_compression=compressor_python is not None,
             file_checksums=file_checksums,
             win_path_sep=win_path_sep,
+            low_memory=Options.isLowMemory(),
         )
     else:
         onefile_compressor_path = os.path.normpath(
             os.path.join(os.path.dirname(__file__), "..", "tools", "onefile_compressor")
         )
 
         mapping = {
@@ -182,14 +189,15 @@
                     compressor_python.getPythonExe(),
                     onefile_compressor_path,
                     dist_dir,
                     getExternalUsePath(onefile_output_filename, only_dirname=True),
                     start_binary,
                     str(file_checksums),
                     str(win_path_sep),
+                    str(Options.isLowMemory()),
                 ],
                 shell=False,
             )
 
 
 def packDistFolderToOnefileBootstrap(onefile_output_filename, dist_dir):
     postprocessing_logger.info(
@@ -224,14 +232,17 @@
     _runOnefileScons(
         onefile_compression=compressor_python is not None,
     )
 
     if isWin32Windows():
         executePostProcessingResources(manifest=None, onefile=True)
 
+    if isAndroidBasedLinux():
+        cleanupHeaderForAndroid(onefile_output_filename)
+
     Plugins.onBootstrapBinary(onefile_output_filename)
 
     if isMacOS():
         addMacOSCodeSignature(filenames=[onefile_output_filename])
 
     if not payload_used_in_build:
         runOnefileCompressor(
```

### Comparing `Nuitka-1.7.5/nuitka/freezer/Standalone.py` & `Nuitka-1.7.6/nuitka/freezer/Standalone.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/freezer/__init__.py` & `Nuitka-1.7.6/nuitka/freezer/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/importing/IgnoreListing.py` & `Nuitka-1.7.6/nuitka/importing/IgnoreListing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/importing/ImportCache.py` & `Nuitka-1.7.6/nuitka/importing/ImportCache.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/importing/ImportResolving.py` & `Nuitka-1.7.6/nuitka/importing/ImportResolving.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/importing/Importing.py` & `Nuitka-1.7.6/nuitka/importing/Importing.py`

 * *Files 0% similar despite different names*

```diff
@@ -51,15 +51,18 @@
 from nuitka.plugins.Plugins import Plugins
 from nuitka.PythonFlavors import isNuitkaPython
 from nuitka.PythonVersions import python_version
 from nuitka.Tracing import my_print, recursion_logger
 from nuitka.tree.ReformulationMultidist import locateMultidistModule
 from nuitka.utils.AppDirs import getCacheDir
 from nuitka.utils.FileOperations import listDir, removeDirectory
-from nuitka.utils.Importing import getSharedLibrarySuffixes
+from nuitka.utils.Importing import (
+    getSharedLibrarySuffixes,
+    isBuiltinModuleName,
+)
 from nuitka.utils.ModuleNames import ModuleName
 from nuitka.utils.SharedLibraries import (
     hasUniversalOrMatchingMacOSArchitecture,
 )
 from nuitka.utils.Utils import isMacOS, isWin32OrPosixWindows
 
 from .IgnoreListing import isIgnoreListedNotExistingModule
@@ -658,16 +661,16 @@
     # and on some systems, that fails.
     if package_name is None and module_name == "site":
         candidate = os.environ.get("NUITKA_SITE_FILENAME", "")
 
         if candidate:
             return candidate, "py"
 
-    # Free pass for built-in modules, the need not exist.
-    if package_name is None and imp.is_builtin(module_name):
+    # Free pass for built-in modules, they need not exist.
+    if package_name is None and isBuiltinModuleName(module_name):
         return None
 
     search_path = getPackageSearchPath(package_name)
 
     if _debug_module_finding:
         my_print(
             "_findModuleInPath: Using search path", search_path, "for", package_name
```

### Comparing `Nuitka-1.7.5/nuitka/importing/PreloadedPackages.py` & `Nuitka-1.7.6/nuitka/importing/PreloadedPackages.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/importing/Recursion.py` & `Nuitka-1.7.6/nuitka/importing/Recursion.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/importing/StandardLibrary.py` & `Nuitka-1.7.6/nuitka/importing/StandardLibrary.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/importing/__init__.py` & `Nuitka-1.7.6/nuitka/importing/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/AsyncgenNodes.py` & `Nuitka-1.7.6/nuitka/nodes/AsyncgenNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/AttributeLookupNodes.py` & `Nuitka-1.7.6/nuitka/nodes/AttributeLookupNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/AttributeNodes.py` & `Nuitka-1.7.6/nuitka/nodes/AttributeNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/AttributeNodesGenerated.py` & `Nuitka-1.7.6/nuitka/nodes/AttributeNodesGenerated.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinAllNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinAllNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinAnyNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinAnyNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinComplexNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinComplexNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinDecodingNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinDecodingNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinDecoratorNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinDecoratorNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinDictNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinDictNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinFormatNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinFormatNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinHashNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinHashNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinIntegerNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinIntegerNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinIteratorNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinIteratorNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinLenNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinLenNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinNextNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinNextNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinOpenNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinOpenNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinOperationNodeBasesGenerated.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinOperationNodeBasesGenerated.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinRangeNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinRangeNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinRefNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinRefNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinSumNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinSumNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinTypeNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinTypeNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BuiltinVarsNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BuiltinVarsNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/BytesNodes.py` & `Nuitka-1.7.6/nuitka/nodes/BytesNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/CallNodes.py` & `Nuitka-1.7.6/nuitka/nodes/CallNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/Checkers.py` & `Nuitka-1.7.6/nuitka/nodes/Checkers.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ChildrenHavingMixins.py` & `Nuitka-1.7.6/nuitka/nodes/ChildrenHavingMixins.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ClassNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ClassNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/CodeObjectSpecs.py` & `Nuitka-1.7.6/nuitka/nodes/CodeObjectSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ComparisonNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ComparisonNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ConditionalNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ConditionalNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ConstantRefNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ConstantRefNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ContainerMakingNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ContainerMakingNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ContainerOperationNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ContainerOperationNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/CoroutineNodes.py` & `Nuitka-1.7.6/nuitka/nodes/CoroutineNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/CtypesNodes.py` & `Nuitka-1.7.6/nuitka/nodes/CtypesNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/DictionaryNodes.py` & `Nuitka-1.7.6/nuitka/nodes/DictionaryNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ExceptionNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ExceptionNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ExecEvalNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ExecEvalNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ExpressionBases.py` & `Nuitka-1.7.6/nuitka/nodes/ExpressionBases.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ExpressionBasesGenerated.py` & `Nuitka-1.7.6/nuitka/nodes/ExpressionBasesGenerated.py`

 * *Files 1% similar despite different names*

```diff
@@ -1500,14 +1500,120 @@
     ChildHavingPairsTupleFinalNoRaiseMixin
 )
 ExpressionImportlibMetadataSelectableGroupsValueRefBase = (
     ChildHavingPairsTupleFinalNoRaiseMixin
 )
 
 
+class ChildHavingPromptOptionalFinalMixin(ExpressionBase):
+    # Mixins are not allowed to specify slots, pylint: disable=assigning-non-slot
+    __slots__ = ()
+
+    # This is generated for use in
+    #   ExpressionBuiltinInput
+
+    def __init__(self, prompt, source_ref):
+        if prompt is not None:
+            prompt.parent = self
+
+        self.subnode_prompt = prompt
+
+        ExpressionBase.__init__(self, source_ref)
+
+    def getVisitableNodes(self):
+        """The visitable nodes, with tuple values flattened."""
+
+        value = self.subnode_prompt
+
+        if value is None:
+            return ()
+        else:
+            return (value,)
+
+    def getVisitableNodesNamed(self):
+        """Named children dictionary.
+
+        For use in cloning nodes, debugging and XML output.
+        """
+
+        return (("prompt", self.subnode_prompt),)
+
+    def replaceChild(self, old_node, new_node):
+        value = self.subnode_prompt
+        if old_node is value:
+            if new_node is not None:
+                new_node.parent = self
+
+            self.subnode_prompt = new_node
+
+            return
+
+        raise AssertionError("Didn't find child", old_node, "in", self)
+
+    def getCloneArgs(self):
+        """Get clones of all children to pass for a new node.
+
+        Needs to make clones of child nodes too.
+        """
+
+        values = {
+            "prompt": self.subnode_prompt.makeClone()
+            if self.subnode_prompt is not None
+            else None,
+        }
+
+        values.update(self.getDetails())
+
+        return values
+
+    def finalize(self):
+        del self.parent
+
+        if self.subnode_prompt is not None:
+            self.subnode_prompt.finalize()
+        del self.subnode_prompt
+
+    def computeExpressionRaw(self, trace_collection):
+        """Compute an expression.
+
+        Default behavior is to just visit the child expressions first, and
+        then the node "computeExpression". For a few cases this needs to
+        be overloaded, e.g. conditional expressions.
+        """
+
+        # First apply the sub-expression, as they it's evaluated before.
+        expression = self.subnode_prompt
+
+        if expression is not None:
+            expression = trace_collection.onExpression(expression)
+
+            if expression.willRaiseAnyException():
+                return (
+                    expression,
+                    "new_raise",
+                    lambda: "For '%s' the child expression '%s' will raise."
+                    % (self.getChildNameNice(), expression.getChildNameNice()),
+                )
+
+        trace_collection.onExceptionRaiseExit(BaseException)
+        return self, None, None
+
+    def collectVariableAccesses(self, emit_read, emit_write):
+        """Collect variable reads and writes of child nodes."""
+
+        subnode_prompt = self.subnode_prompt
+
+        if subnode_prompt is not None:
+            self.subnode_prompt.collectVariableAccesses(emit_read, emit_write)
+
+
+# Assign the names that are easier to import with a stable name.
+ExpressionBuiltinInputBase = ChildHavingPromptOptionalFinalMixin
+
+
 class ChildHavingValueFinalNoRaiseMixin(ExpressionBase):
     # Mixins are not allowed to specify slots, pylint: disable=assigning-non-slot
     __slots__ = ()
 
     # This is generated for use in
     #   ExpressionBuiltinClassmethod
     #   ExpressionBuiltinStaticmethod
```

### Comparing `Nuitka-1.7.5/nuitka/nodes/ExpressionShapeMixins.py` & `Nuitka-1.7.6/nuitka/nodes/ExpressionShapeMixins.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/FrameNodes.py` & `Nuitka-1.7.6/nuitka/nodes/FrameNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/FunctionAttributeNodes.py` & `Nuitka-1.7.6/nuitka/nodes/FunctionAttributeNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/FunctionNodes.py` & `Nuitka-1.7.6/nuitka/nodes/FunctionNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/FutureSpecs.py` & `Nuitka-1.7.6/nuitka/nodes/FutureSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/GeneratorNodes.py` & `Nuitka-1.7.6/nuitka/nodes/GeneratorNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/GlobalsLocalsNodes.py` & `Nuitka-1.7.6/nuitka/nodes/GlobalsLocalsNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/HardImportNodesGenerated.py` & `Nuitka-1.7.6/nuitka/nodes/HardImportNodesGenerated.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ImportHardNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ImportHardNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ImportNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ImportNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/IndicatorMixins.py` & `Nuitka-1.7.6/nuitka/nodes/IndicatorMixins.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/InjectCNodes.py` & `Nuitka-1.7.6/nuitka/nodes/InjectCNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/IterationHandles.py` & `Nuitka-1.7.6/nuitka/nodes/IterationHandles.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/KeyValuePairNodes.py` & `Nuitka-1.7.6/nuitka/nodes/KeyValuePairNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ListOperationNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ListOperationNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/LocalsDictNodes.py` & `Nuitka-1.7.6/nuitka/nodes/LocalsDictNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/LocalsScopes.py` & `Nuitka-1.7.6/nuitka/nodes/LocalsScopes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/LoopNodes.py` & `Nuitka-1.7.6/nuitka/nodes/LoopNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/MatchNodes.py` & `Nuitka-1.7.6/nuitka/nodes/MatchNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ModuleAttributeNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ModuleAttributeNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ModuleNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ModuleNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/NodeBases.py` & `Nuitka-1.7.6/nuitka/nodes/NodeBases.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/NodeMakingHelpers.py` & `Nuitka-1.7.6/nuitka/nodes/NodeMakingHelpers.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/NodeMetaClasses.py` & `Nuitka-1.7.6/nuitka/nodes/NodeMetaClasses.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/OperatorNodes.py` & `Nuitka-1.7.6/nuitka/nodes/OperatorNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/OperatorNodesUnary.py` & `Nuitka-1.7.6/nuitka/nodes/OperatorNodesUnary.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/OsSysNodes.py` & `Nuitka-1.7.6/nuitka/nodes/OsSysNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/OutlineNodes.py` & `Nuitka-1.7.6/nuitka/nodes/OutlineNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/PackageMetadataNodes.py` & `Nuitka-1.7.6/nuitka/nodes/PackageMetadataNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/PackageResourceNodes.py` & `Nuitka-1.7.6/nuitka/nodes/PackageResourceNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/PrintNodes.py` & `Nuitka-1.7.6/nuitka/nodes/PrintNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/ReturnNodes.py` & `Nuitka-1.7.6/nuitka/nodes/ReturnNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/SideEffectNodes.py` & `Nuitka-1.7.6/nuitka/nodes/SideEffectNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/SliceNodes.py` & `Nuitka-1.7.6/nuitka/nodes/SliceNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/StatementBasesGenerated.py` & `Nuitka-1.7.6/nuitka/nodes/StatementBasesGenerated.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/StatementNodes.py` & `Nuitka-1.7.6/nuitka/nodes/StatementNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/StrNodes.py` & `Nuitka-1.7.6/nuitka/nodes/StrNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/StringConcatenationNodes.py` & `Nuitka-1.7.6/nuitka/nodes/StringConcatenationNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/SubscriptNodes.py` & `Nuitka-1.7.6/nuitka/nodes/SubscriptNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/TryNodes.py` & `Nuitka-1.7.6/nuitka/nodes/TryNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/TypeMatchNodes.py` & `Nuitka-1.7.6/nuitka/nodes/TypeMatchNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/TypeNodes.py` & `Nuitka-1.7.6/nuitka/nodes/TypeNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/VariableAssignNodes.py` & `Nuitka-1.7.6/nuitka/nodes/VariableAssignNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/VariableDelNodes.py` & `Nuitka-1.7.6/nuitka/nodes/VariableDelNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/VariableNameNodes.py` & `Nuitka-1.7.6/nuitka/nodes/VariableNameNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/VariableRefNodes.py` & `Nuitka-1.7.6/nuitka/nodes/VariableRefNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/VariableReleaseNodes.py` & `Nuitka-1.7.6/nuitka/nodes/VariableReleaseNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/YieldNodes.py` & `Nuitka-1.7.6/nuitka/nodes/YieldNodes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/__init__.py` & `Nuitka-1.7.6/nuitka/nodes/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/shapes/BuiltinTypeShapes.py` & `Nuitka-1.7.6/nuitka/nodes/shapes/BuiltinTypeShapes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/shapes/ControlFlowDescriptions.py` & `Nuitka-1.7.6/nuitka/nodes/shapes/ControlFlowDescriptions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/shapes/ShapeMixins.py` & `Nuitka-1.7.6/nuitka/nodes/shapes/ShapeMixins.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/shapes/StandardShapes.py` & `Nuitka-1.7.6/nuitka/nodes/shapes/StandardShapes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/nodes/shapes/__init__.py` & `Nuitka-1.7.6/nuitka/nodes/shapes/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/optimizations/BytecodeDemotion.py` & `Nuitka-1.7.6/nuitka/optimizations/BytecodeDemotion.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/optimizations/FunctionInlining.py` & `Nuitka-1.7.6/nuitka/optimizations/FunctionInlining.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/optimizations/Graphs.py` & `Nuitka-1.7.6/nuitka/optimizations/Graphs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/optimizations/Optimization.py` & `Nuitka-1.7.6/nuitka/optimizations/Optimization.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/optimizations/OptimizeBuiltinCalls.py` & `Nuitka-1.7.6/nuitka/optimizations/OptimizeBuiltinCalls.py`

 * *Files 0% similar despite different names*

```diff
@@ -49,14 +49,15 @@
     ExpressionBuiltinBin,
     ExpressionBuiltinFormat,
     ExpressionBuiltinHex,
     ExpressionBuiltinId,
     ExpressionBuiltinOct,
 )
 from nuitka.nodes.BuiltinHashNodes import ExpressionBuiltinHash
+from nuitka.nodes.BuiltinInputNodes import ExpressionBuiltinInput
 from nuitka.nodes.BuiltinIntegerNodes import (
     ExpressionBuiltinInt1,
     ExpressionBuiltinInt2,
 )
 from nuitka.nodes.BuiltinIteratorNodes import (
     ExpressionBuiltinIter1,
     ExpressionBuiltinIter2,
@@ -1322,14 +1323,22 @@
     return BuiltinParameterSpecs.extractBuiltinArgs(
         node=node,
         builtin_class=ExpressionBuiltinHash,
         builtin_spec=BuiltinParameterSpecs.builtin_hash_spec,
     )
 
 
+def input_extractor(node):
+    return BuiltinParameterSpecs.extractBuiltinArgs(
+        node=node,
+        builtin_class=ExpressionBuiltinInput,
+        builtin_spec=BuiltinParameterSpecs.builtin_input_spec,
+    )
+
+
 def format_extractor(node):
     def makeFormat0(source_ref):
         # pylint: disable=unused-argument
 
         return makeRaiseExceptionReplacementExpressionFromInstance(
             expression=node,
             exception=TypeError("format() takes at least 1 argument (0 given)"),
@@ -1428,14 +1437,15 @@
     "slice": slice_extractor,
     "hash": hash_extractor,
     "format": format_extractor,
     "open": open_extractor,
     "staticmethod": staticmethod_extractor,
     "classmethod": classmethod_extractor,
     "divmod": divmod_extractor,
+    "input": input_extractor,
 }
 
 if python_version < 0x300:
     # These are not in Python3
     _dispatch_dict["long"] = long_extractor
     _dispatch_dict["unicode"] = unicode_extractor
     _dispatch_dict["execfile"] = execfile_extractor
```

### Comparing `Nuitka-1.7.5/nuitka/optimizations/Tags.py` & `Nuitka-1.7.6/nuitka/optimizations/Tags.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/optimizations/TraceCollections.py` & `Nuitka-1.7.6/nuitka/optimizations/TraceCollections.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/optimizations/ValueTraces.py` & `Nuitka-1.7.6/nuitka/optimizations/ValueTraces.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/optimizations/__init__.py` & `Nuitka-1.7.6/nuitka/optimizations/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/pgo/PGO.py` & `Nuitka-1.7.6/nuitka/pgo/PGO.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/pgo/__init__.py` & `Nuitka-1.7.6/nuitka/pgo/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/PluginBase.py` & `Nuitka-1.7.6/nuitka/plugins/PluginBase.py`

 * *Files 1% similar despite different names*

```diff
@@ -24,15 +24,14 @@
 
 The base class will serve as documentation. And it will point to examples of
 it being used.
 """
 
 import ast
 import functools
-import imp
 import inspect
 import os
 import sys
 
 from nuitka import Options
 from nuitka.__past__ import getMetaClassBase
 from nuitka.containers.Namedtuples import makeNamedtupleClass
@@ -66,14 +65,15 @@
 from nuitka.PythonVersions import (
     getTestExecutionPythonVersions,
     python_version,
 )
 from nuitka.Tracing import plugins_logger
 from nuitka.utils.Distributions import isDistributionCondaPackage
 from nuitka.utils.Execution import NuitkaCalledProcessError, check_output
+from nuitka.utils.Importing import isBuiltinModuleName
 from nuitka.utils.ModuleNames import (
     ModuleName,
     makeTriggerModuleName,
     post_module_load_trigger_name,
     pre_module_load_trigger_name,
 )
 from nuitka.utils.SharedLibraries import locateDLL, locateDLLsInDirectory
@@ -1141,15 +1141,15 @@
                 # Querying package versions.
                 "version": _getPackageVersion,
                 "plugin": _isPluginActive,
                 "no_asserts": hasPythonFlagNoAsserts(),
                 "no_docstrings": hasPythonFlagNoDocStrings(),
                 "no_annotations": hasPythonFlagNoAnnotations(),
                 # Querying package properties
-                "has_builtin_module": imp.is_builtin,
+                "has_builtin_module": isBuiltinModuleName,
             }
         )
 
         if isWin32Windows():
             context.update(
                 {
                     "arch_x86": getArchitecture() == "x86",
```

### Comparing `Nuitka-1.7.5/nuitka/plugins/Plugins.py` & `Nuitka-1.7.6/nuitka/plugins/Plugins.py`

 * *Files 0% similar despite different names*

```diff
@@ -203,14 +203,25 @@
     return ("tk-inter",)
 
 
 def getGuiPluginNames():
     return getQtPluginNames() + getOtherGuiPluginNames()
 
 
+def hasActiveGuiPluginForBinding(binding_name):
+    if binding_name in ("tkinter", "Tkinter"):
+        return hasActivePlugin("tk-inter")
+    elif binding_name in getQtBindingNames():
+        return hasActivePlugin(binding_name.lower())
+    else:
+        # For wx, we do not have a plugin right now, it just works, but
+        # also means it cannot be picked.
+        return False
+
+
 def hasActivePlugin(plugin_name):
     """Decide if a plugin is active.
 
     Args:
         plugin_name - name of the plugin
 
     Notes:
```

### Comparing `Nuitka-1.7.5/nuitka/plugins/__init__.py` & `Nuitka-1.7.6/nuitka/plugins/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/AntiBloatPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/AntiBloatPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/ConsiderPyLintAnnotationsPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/ConsiderPyLintAnnotationsPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/DataFilesPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/DataFilesPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/DelvewheelPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/DelvewheelPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/DillPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/DillPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/DllFilesPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/DllFilesPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/EnumPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/EnumPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/EventletPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/EventletPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/GeventPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/GeventPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/GiPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/GiPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/GlfwPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/GlfwPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/ImplicitImports.py` & `Nuitka-1.7.6/nuitka/plugins/standard/ImplicitImports.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/KivyPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/KivyPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/MatplotlibPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/MatplotlibPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/MultiprocessingPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/MultiprocessingPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/NumpyPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/NumpyPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/OptionsNannyPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/OptionsNannyPlugin.py`

 * *Files 2% similar despite different names*

```diff
@@ -93,15 +93,17 @@
                 else:
                     downside_message = """\
 Otherwise a terminal window will open"""
 
                 self.info(
                     """\
 Note, when using '%s', consider using '--disable-console' option. %s. However for \
-debugging, terminal output is the easiest way to see informative traceback information."""
+debugging, terminal output is the easiest way to see informative traceback \
+and error information, so delay this until your program working and remove \
+once you find it non-working."""
                     % (full_name, downside_message)
                 )
 
         else:
             self.sysexitIllegalOptionValue(full_name, "console", console)
 
     def _checkMacOSBundleMode(self, full_name, macos_bundle):
```

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/PbrPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/PbrPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/PkgResourcesPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/PkgResourcesPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/PmwPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/PmwPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/PySidePyQtPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/PySidePyQtPlugin.py`

 * *Files 1% similar despite different names*

```diff
@@ -28,32 +28,31 @@
     isOnefileMode,
     isStandaloneMode,
     shallCreateAppBundle,
 )
 from nuitka.plugins.PluginBase import NuitkaPluginBase
 from nuitka.plugins.Plugins import (
     getActiveQtPlugin,
+    getOtherGUIBindingNames,
     getQtBindingNames,
     getQtPluginNames,
+    hasActiveGuiPluginForBinding,
 )
 from nuitka.PythonFlavors import isAnacondaPython
 from nuitka.PythonVersions import python_version
 from nuitka.utils.FileOperations import getFileList, listDir
 from nuitka.utils.ModuleNames import ModuleName
 from nuitka.utils.Utils import (
     getArchitecture,
     isDebianBasedLinux,
     isLinux,
     isMacOS,
     isWin32Windows,
 )
 
-# Use to detect the Qt plugin that is active and check for conflicts.
-_qt_binding_names = getQtBindingNames()
-
 
 class NuitkaPluginQtBindingsPluginBase(NuitkaPluginBase):
     # Automatically suppress detectors for any other toolkit
     plugin_gui_toolkit = True
 
     # For overload in the derived bindings plugin.
     binding_name = None
@@ -76,15 +75,15 @@
         self.binding_package_name = ModuleName(self.binding_name)
 
         # Allow to specify none.
         if self.qt_plugins == set(["none"]):
             self.qt_plugins = set()
 
         # Prevent the list of binding names from being incomplete, it's used for conflicts.
-        assert self.binding_name in _qt_binding_names, self.binding_name
+        assert self.binding_name in getQtBindingNames(), self.binding_name
 
         # Also lets have consistency in naming.
         assert self.plugin_name in getQtPluginNames()
 
         active_qt_plugin_name = getActiveQtPlugin()
 
         if active_qt_plugin_name is not None:
@@ -105,15 +104,15 @@
 by default only the sensible ones are included, but you can also put
 "all" or list them individually. If you specify something that does
 not exist, a list of all available will be given.""",
         )
 
         group.add_option(
             "--noinclude-qt-translations",
-            action="store",
+            action="store_true",
             dest="no_qt_translations",
             default=False,
             help="""\
 Include Qt translations with QtWebEngine if used. These can be a lot
 of files that you may not want to be included.""",
         )
 
@@ -1060,15 +1059,15 @@
     def onModuleEncounter(
         self, using_module_name, module_name, module_filename, module_kind
     ):
         top_package_name = module_name.getTopLevelPackageName()
 
         if isStandaloneMode():
             if (
-                top_package_name in _qt_binding_names
+                top_package_name in getQtBindingNames()
                 and top_package_name != self.binding_name
             ):
                 if top_package_name not in self.warned_about:
                     self.info(
                         """\
 Unwanted import of '%(unwanted)s' that conflicts with '%(binding_name)s' \
 encountered, preventing its inclusion. As a result an "ImportError" might \
@@ -1084,14 +1083,23 @@
 
                 return (
                     False,
                     "Not included due to potentially conflicting Qt versions with selected Qt binding '%s'."
                     % self.binding_name,
                 )
 
+            if (
+                top_package_name in getOtherGUIBindingNames()
+                and not hasActiveGuiPluginForBinding(top_package_name)
+            ):
+                return (
+                    False,
+                    "Not included due to its plugin not being active, but a Qt plugin is.",
+                )
+
     def onModuleCompleteSet(self, module_set):
         self.onModuleCompleteSetGUI(
             module_set=module_set, plugin_binding_name=self.binding_name
         )
 
     def onModuleSourceCode(self, module_name, source_code):
         """Third party packages that make binding selections."""
@@ -1417,15 +1425,15 @@
 
     def onModuleEncounter(
         self, using_module_name, module_name, module_filename, module_kind
     ):
         top_package_name = module_name.getTopLevelPackageName()
 
         if isStandaloneMode():
-            if top_package_name in _qt_binding_names:
+            if top_package_name in getQtBindingNames():
                 if top_package_name not in self.warned_about:
                     self.info(
                         """\
 Unwanted import of '%(unwanted)s' that is forbidden encountered, preventing
 its use. As a result an "ImportError" might be given at run time. Uninstall
 it for full compatible behavior with the uncompiled code to debug it."""
                         % {
```

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/PywebViewPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/PywebViewPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/TensorflowPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/TensorflowPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/TkinterPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/TkinterPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/TorchPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/TorchPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/TransformersPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/TransformersPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/TrioPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/TrioPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/UpxPlugin.py` & `Nuitka-1.7.6/nuitka/plugins/standard/UpxPlugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/__init__.py` & `Nuitka-1.7.6/nuitka/plugins/standard/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/standard.nuitka-package.config.yml` & `Nuitka-1.7.6/nuitka/plugins/standard/standard.nuitka-package.config.yml`

 * *Files 0% similar despite different names*

```diff
@@ -1149,14 +1149,27 @@
 - module-name: 'keras.utils.vis_utils'
   anti-bloat:
     - description: 'remove IPython reference'
       replacements_plain:
         'from IPython import display': 'raise ImportError'
       when: 'not use_ipython'
 
+- module-name: 'keyring'
+  data-files:
+    include-metadata:
+      - 'keyring'
+  implicit-imports:
+    - depends:
+        - 'keyring.backends.*'
+
+- module-name: 'keyring.backends.Windows'
+  implicit-imports:
+    - depends:
+        - 'win32timezone'
+
 - module-name: 'kivy'
   data-files:
     dirs:
       - 'data'
 
 - module-name: 'kivy._clock'
   implicit-imports:
@@ -1666,30 +1679,30 @@
           if not val:
               try:
                   smsg = msg()
               except TypeError:
                   smsg = msg
               raise AssertionError(smsg)
 
-        def assert_equal(actual, desired, err_msg='', verbose=True):
+        def assert_equal(*args, **kwargs):
           pass
 
-        def assert_approx_equal(actual, desired, significant=7, err_msg='', verbose=True):
+        def assert_approx_equal(*args, **kwargs):
           pass
 
-        def assert_almost_equal(actual, desired, decimal=7, err_msg='', verbose=True):
+        def assert_almost_equal(*args, **kwargs):
           pass
 
-        def assert_array_equal(x, y, err_msg='', verbose=True, *, strict=False):
+        def assert_array_equal(*args, **kwargs):
           pass
 
-        def assert_array_less(x, y, err_msg='', verbose=True):
+        def assert_array_less(*args, **kwargs):
           pass
 
-        def assert_array_almost_equal(x, y, decimal=6, err_msg='', verbose=True):
+        def assert_array_almost_equal(*args, **kwargs):
           pass
 
 - module-name: 'numpy.testing._private.pytesttester'
   anti-bloat:
     - description: 'remove numpy testing framework'
       module_code: |
         class PytestTester:
@@ -1751,14 +1764,27 @@
 
 - module-name: 'opentele.utils'
   anti-bloat:
     - description: 'workaround compiled function decorator issues'
       replacements_plain:
         'bases = func.__class__.__bases__': 'bases = func.__class__.__bases__ if func.__class__.__bases__ != (FunctionType,) else (object,)'
 
+- module-name: 'opentelemetry.exporter.jaeger.thrift'
+  import-hacks:
+    - global-sys-path:
+        # This package forces itself into "sys.path" and expects absolute
+        # imports like "jaeger" to be available.
+        - 'gen'
+
+- module-name: 'opentelemetry.exporter.jaeger.thrift.gen'
+  anti-bloat:
+    - description: 'remove "sys.path" hack'
+      replacements_plain:
+        'sys.path.append': ''
+
 - module-name: 'opentelemetry.propagate'
   data-files:
     include-metadata:
       - 'opentelemetry-api'
 
   implicit-imports:
     - depends:
@@ -5043,21 +5069,44 @@
     - description: 'compatibility workaround'
       replacements_plain:
         ? "\ndef _dp_init_subclass"
         : |-
           @classmethod
           def _dp_init_subclass
 
+- module-name: 'torch_scatter'
+  anti-bloat:
+    - description: 'workaround finding DLLs as modules by wrong names'
+      replacements_plain:
+        "f'{library}_cuda', [osp.dirname(__file__)]": "f'torch_scatter.{library}_cuda'"
+        "f'{library}_cpu', [osp.dirname(__file__)]": "f'torch_scatter.{library}_cpu'"
+        'importlib.machinery.PathFinder()': 'importlib.util'
+  implicit-imports:
+    - depends:
+        - '._version_cpu'
+        - '._scatter_cpu'
+        - '._segment_csr_cpu'
+        - '._segment_coo_cpu'
+        - '._version_cuda'
+        - '._scatter_cuda'
+        - '._segment_csr_cuda'
+        - '._segment_coo_cuda'
+
 - module-name: 'torchaudio'
   import-hacks:
     - find-dlls-near-module:
         - 'torch'
     - acceptable-missing-dlls:
         - '_torchaudio_ffmpeg'
 
+- module-name: 'torchaudio.lib._torchaudio'
+  implicit-imports:
+    - depends:
+        - 'torchaudio.lib.libtorchaudio'
+
 - module-name: 'torchmetrics.utilities.checks'
   anti-bloat:
     - description: 'remove unittest reference'
       replacements_plain:
         'from unittest.mock import Mock': ''
         'isinstance(instance_attr, Mock)': 'False'
 
@@ -5153,14 +5202,20 @@
 - module-name: 'transformers.models.yoso.modeling_yoso'
   anti-bloat:
     - description: 'remove setuptools usage'
       change_function:
         'load_cuda_kernels': "'(lambda : False)'"
       when: 'not use_setuptools'
 
+- module-name: 'transformers.processing_utils'
+  anti-bloat:
+    - description: 'workaround manual import issue'
+      replacements_plain:
+        'transformers_module = direct_transformers_import(Path(__file__).parent)': 'import transformers as transformers_module'
+
 - module-name: 'transformers.trainer'
   anti-bloat:
     - description: 'remove IPython reference'
       replacements_plain:
         'is_in_notebook()': 'False'
       when: 'not use_ipython'
 
@@ -5481,14 +5536,29 @@
 
 - module-name: 'webview'
   data-files:
     dirs:
       - 'lib'
   dlls:
     - from_filenames:
+        relative_path: 'lib/runtimes/win-x86/native'
+        prefixes:
+          - 'WebView2Loader'
+      when: 'win32 and arch_x86'
+    - from_filenames:
+        relative_path: 'lib/runtimes/win-x64/native'
+        prefixes:
+          - 'WebView2Loader'
+      when: 'win32 and arch_amd64'
+    - from_filenames:
+        relative_path: 'lib/runtimes/win-arm64/native'
+        prefixes:
+          - 'WebView2Loader'
+      when: 'win32 and arch_arm64'
+    - from_filenames:
         relative_path: 'lib/x86'
         prefixes:
           - 'WebView2Loader'
       when: 'win32 and arch_x86'
     - from_filenames:
         relative_path: 'lib/x64'
         prefixes:
@@ -5517,14 +5587,20 @@
 
 - module-name: 'webview.platforms.edgechromium'
   anti-bloat:
     - description: 'workaround unused platform DLL checks'
       replacements_plain:
         "';' + interop_dll_path(platform)": "';' + os.path.abspath(os.path.join(os.path.dirname(__file__), '..', 'lib', platform))"
 
+- module-name: 'werkzeug.serving'
+  anti-bloat:
+    - description: 'remove ability to run with reloader'
+      replacements_plain:
+        'if use_reloader:': 'if False:'
+
 - module-name: 'win32com'
   import-hacks:
     # This package adds another directory to the search path of itself,
     # which we will not find packages in unless added.
     - package-dirs:
         - 'win32comext'
       when: 'win32'
@@ -5543,14 +5619,21 @@
       - description: 'wx will crash in console mode during startup'
         console: 'yes'
         when: 'macos'
       - description: 'wx requires program to be in bundle form'
         macos_bundle: 'yes'
         when: 'macos'
 
+- module-name: 'wx.html2'
+  dlls:
+    - from_filenames:
+        prefixes:
+          - 'WebView2Loader'
+      when: 'win32'
+
 - module-name: 'xarray'
   data-files:
     dirs:
       - 'static'
 
 - module-name: 'xarray.backends.locks'
   anti-bloat:
```

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/stdlib2.nuitka-package.config.yml` & `Nuitka-1.7.6/nuitka/plugins/standard/stdlib2.nuitka-package.config.yml`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/plugins/standard/stdlib3.nuitka-package.config.yml` & `Nuitka-1.7.6/nuitka/plugins/standard/stdlib3.nuitka-package.config.yml`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/reports/LicenseReport.rst.j2` & `Nuitka-1.7.6/nuitka/reports/LicenseReport.rst.j2`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/reports/Reports.py` & `Nuitka-1.7.6/nuitka/reports/Reports.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/reports/__init__.py` & `Nuitka-1.7.6/nuitka/reports/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/specs/BuiltinBytesOperationSpecs.py` & `Nuitka-1.7.6/nuitka/specs/BuiltinBytesOperationSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/specs/BuiltinDictOperationSpecs.py` & `Nuitka-1.7.6/nuitka/specs/BuiltinDictOperationSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/specs/BuiltinListOperationSpecs.py` & `Nuitka-1.7.6/nuitka/specs/BuiltinListOperationSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/specs/BuiltinParameterSpecs.py` & `Nuitka-1.7.6/nuitka/specs/BuiltinParameterSpecs.py`

 * *Files 0% similar despite different names*

```diff
@@ -487,14 +487,18 @@
 # Beware: One argument version defines "stop", not "start".
 builtin_slice_spec = BuiltinParameterSpecNoKeywords(
     "slice", ("start", "stop", "step"), default_count=2
 )
 
 builtin_hash_spec = BuiltinParameterSpecNoKeywords("hash", ("object",), default_count=0)
 
+builtin_input_spec = BuiltinParameterSpecNoKeywords(
+    "input", ("prompt",), default_count=1
+)
+
 builtin_format_spec = BuiltinParameterSpecNoKeywords(
     "format", ("value", "format_spec"), default_count=1
 )
 
 if python_version < 0x380:
     builtin_sum_spec = BuiltinParameterSpecNoKeywords(
         "sum", ("sequence", "start"), default_count=1
```

### Comparing `Nuitka-1.7.5/nuitka/specs/BuiltinStrOperationSpecs.py` & `Nuitka-1.7.6/nuitka/specs/BuiltinStrOperationSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/specs/BuiltinTypeOperationSpecs.py` & `Nuitka-1.7.6/nuitka/specs/BuiltinTypeOperationSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/specs/BuiltinUnicodeOperationSpecs.py` & `Nuitka-1.7.6/nuitka/specs/BuiltinUnicodeOperationSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/specs/HardImportSpecs.py` & `Nuitka-1.7.6/nuitka/specs/HardImportSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/specs/ParameterSpecs.py` & `Nuitka-1.7.6/nuitka/specs/ParameterSpecs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/specs/__init__.py` & `Nuitka-1.7.6/nuitka/specs/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/Basics.py` & `Nuitka-1.7.6/nuitka/tools/Basics.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/__init__.py` & `Nuitka-1.7.6/nuitka/tools/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/commercial/__init__.py` & `Nuitka-1.7.6/nuitka/tools/commercial/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/data_composer/DataComposer.py` & `Nuitka-1.7.6/nuitka/tools/data_composer/DataComposer.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/data_composer/__init__.py` & `Nuitka-1.7.6/nuitka/tools/data_composer/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/data_composer/__main__.py` & `Nuitka-1.7.6/nuitka/tools/data_composer/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/environments/CreateEnvironment.py` & `Nuitka-1.7.6/nuitka/tools/environments/CreateEnvironment.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/environments/Virtualenv.py` & `Nuitka-1.7.6/nuitka/tools/environments/Virtualenv.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/environments/__init__.py` & `Nuitka-1.7.6/nuitka/tools/environments/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/general/__init__.py` & `Nuitka-1.7.6/nuitka/tools/general/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/general/dll_report/__init__.py` & `Nuitka-1.7.6/nuitka/tools/general/dll_report/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/general/dll_report/__main__.py` & `Nuitka-1.7.6/nuitka/tools/general/dll_report/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/general/find_module/FindModuleCode.py` & `Nuitka-1.7.6/nuitka/tools/general/find_module/FindModuleCode.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/general/find_module/__init__.py` & `Nuitka-1.7.6/nuitka/tools/general/find_module/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/onefile_compressor/OnefileCompressor.py` & `Nuitka-1.7.6/nuitka/tools/onefile_compressor/OnefileCompressor.py`

 * *Files 2% similar despite different names*

```diff
@@ -40,21 +40,21 @@
     decoratorRetries,
     isPosixWindows,
     isWin32OrPosixWindows,
     isWin32Windows,
 )
 
 
-def getCompressorFunction(expect_compression):
+def getCompressorFunction(expect_compression, low_memory):
     # spell-checker: ignore zstd, closefd
 
     if expect_compression:
         from zstandard import ZstdCompressor  # pylint: disable=I0021,import-error
 
-        compressor_context = ZstdCompressor(level=22)
+        compressor_context = ZstdCompressor(level=3 if low_memory else 22)
 
         @contextmanager
         def useCompressedFile(output_file):
             with compressor_context.stream_writer(
                 output_file, closefd=False
             ) as compressed_file:
                 yield compressed_file
@@ -117,18 +117,20 @@
 def attachOnefilePayload(
     dist_dir,
     onefile_output_filename,
     start_binary,
     expect_compression,
     file_checksums,
     win_path_sep,
+    low_memory,
 ):
     # Somewhat detail rich, pylint: disable=too-many-statements
     compression_indicator, compressor = getCompressorFunction(
-        expect_compression=expect_compression
+        expect_compression=expect_compression,
+        low_memory=low_memory,
     )
 
     def _attachOnefilePayloadFile(
         compressed_file, filename_full, dist_dir, filename_encoding
     ):
         payload_item_size = 0
 
@@ -283,22 +285,24 @@
     # Internal tool, most simple command line handling. This is the build directory
     # where main Nuitka put the .const files.
     dist_dir = sys.argv[1]
     onefile_output_filename = sys.argv[2]
     start_binary = os.path.normpath(sys.argv[3])  # Might switch from MSYS2 to CPython
     file_checksums = sys.argv[4] == "True"
     win_path_sep = sys.argv[5] == "True"
+    low_memory = sys.argv[6] == "True"
 
     if os.environ.get("NUITKA_PROGRESS_BAR") == "1":
         enableProgressBar()
 
     attachOnefilePayload(
         dist_dir=dist_dir,
         onefile_output_filename=onefile_output_filename,
         start_binary=start_binary,
         # We wouldn't be here, if that was not the case.
         expect_compression=True,
         file_checksums=file_checksums,
         win_path_sep=win_path_sep,
+        low_memory=low_memory,
     )
 
     sys.exit(0)
```

### Comparing `Nuitka-1.7.5/nuitka/tools/onefile_compressor/__init__.py` & `Nuitka-1.7.6/nuitka/tools/onefile_compressor/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/onefile_compressor/__main__.py` & `Nuitka-1.7.6/nuitka/tools/onefile_compressor/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/podman/Podman.py` & `Nuitka-1.7.6/nuitka/tools/podman/Podman.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/podman/__init__.py` & `Nuitka-1.7.6/nuitka/tools/podman/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/podman/__main__.py` & `Nuitka-1.7.6/nuitka/tools/podman/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/profiler/__init__.py` & `Nuitka-1.7.6/nuitka/tools/profiler/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/profiler/__main__.py` & `Nuitka-1.7.6/nuitka/tools/profiler/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/scanning/DisplayPackageDLLs.py` & `Nuitka-1.7.6/nuitka/tools/scanning/DisplayPackageDLLs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/scanning/DisplayPackageData.py` & `Nuitka-1.7.6/nuitka/tools/scanning/DisplayPackageData.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/scanning/__init__.py` & `Nuitka-1.7.6/nuitka/tools/scanning/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/specialize/CTypeDescriptions.py` & `Nuitka-1.7.6/nuitka/tools/specialize/CTypeDescriptions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/specialize/Common.py` & `Nuitka-1.7.6/nuitka/tools/specialize/Common.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/specialize/SpecializeC.py` & `Nuitka-1.7.6/nuitka/tools/specialize/SpecializeC.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/specialize/SpecializePython.py` & `Nuitka-1.7.6/nuitka/tools/specialize/SpecializePython.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/specialize/__init__.py` & `Nuitka-1.7.6/nuitka/tools/specialize/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/Common.py` & `Nuitka-1.7.6/nuitka/tools/testing/Common.py`

 * *Files 0% similar despite different names*

```diff
@@ -586,15 +586,15 @@
         elif type(x) is dict:
             if "__builtins__" in x:
                 k = "<module dict %s>" % x["__name__"]
             elif "__spec__" in x and "__name__" in x:
                 k = "<module dict %s>" % x["__name__"]
             else:
                 k = str(x)
-        elif x.__class__.__name__ == "compiled_frame":
+        elif hasattr(x, "__class__") and x.__class__.__name__ == "compiled_frame":
             k = "<compiled_frame at xxx, line %d code %s" % (x.f_lineno, x.f_code)
         else:
             k = str(x)
 
         c = sys.getrefcount(x)
 
         if k in m:
```

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/Constructs.py` & `Nuitka-1.7.6/nuitka/tools/testing/Constructs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/OutputComparison.py` & `Nuitka-1.7.6/nuitka/tools/testing/OutputComparison.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/Pythons.py` & `Nuitka-1.7.6/nuitka/tools/testing/Pythons.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/RuntimeTracing.py` & `Nuitka-1.7.6/nuitka/tools/testing/RuntimeTracing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/SearchModes.py` & `Nuitka-1.7.6/nuitka/tools/testing/SearchModes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/Valgrind.py` & `Nuitka-1.7.6/nuitka/tools/testing/Valgrind.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/__init__.py` & `Nuitka-1.7.6/nuitka/tools/testing/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/check_reference_counts/__init__.py` & `Nuitka-1.7.6/nuitka/tools/testing/check_reference_counts/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/check_reference_counts/__main__.py` & `Nuitka-1.7.6/nuitka/tools/testing/check_reference_counts/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/compare_with_cpython/__init__.py` & `Nuitka-1.7.6/nuitka/tools/testing/compare_with_cpython/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/compare_with_cpython/__main__.py` & `Nuitka-1.7.6/nuitka/tools/testing/compare_with_cpython/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/find_sxs_modules/__init__.py` & `Nuitka-1.7.6/nuitka/tools/testing/find_sxs_modules/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/find_sxs_modules/__main__.py` & `Nuitka-1.7.6/nuitka/tools/testing/find_sxs_modules/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/measure_construct_performance/__init__.py` & `Nuitka-1.7.6/nuitka/tools/testing/measure_construct_performance/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/measure_construct_performance/__main__.py` & `Nuitka-1.7.6/nuitka/tools/testing/measure_construct_performance/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/run_nuitka_tests/__init__.py` & `Nuitka-1.7.6/nuitka/tools/testing/run_nuitka_tests/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/testing/run_nuitka_tests/__main__.py` & `Nuitka-1.7.6/nuitka/tools/testing/run_nuitka_tests/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/watch/__init__.py` & `Nuitka-1.7.6/nuitka/tools/watch/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tools/watch/__main__.py` & `Nuitka-1.7.6/nuitka/tools/watch/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/Building.py` & `Nuitka-1.7.6/nuitka/tree/Building.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ComplexCallHelperFunctions.py` & `Nuitka-1.7.6/nuitka/tree/ComplexCallHelperFunctions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/Extractions.py` & `Nuitka-1.7.6/nuitka/tree/Extractions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/InternalModule.py` & `Nuitka-1.7.6/nuitka/tree/InternalModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/Operations.py` & `Nuitka-1.7.6/nuitka/tree/Operations.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationAssertStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationAssertStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationAssignmentStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationAssignmentStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationBooleanExpressions.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationBooleanExpressions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationCallExpressions.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationCallExpressions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationClasses.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationClasses.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationClasses3.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationClasses3.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationComparisonExpressions.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationComparisonExpressions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationContractionExpressions.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationContractionExpressions.py`

 * *Files 1% similar despite different names*

```diff
@@ -42,15 +42,14 @@
 )
 from nuitka.nodes.DictionaryNodes import (
     StatementDictOperationSet,
     StatementDictOperationSetKeyValue,
 )
 from nuitka.nodes.FrameNodes import (
     StatementsFrameAsyncgen,
-    StatementsFrameFunction,
     StatementsFrameGenerator,
 )
 from nuitka.nodes.FunctionNodes import ExpressionFunctionRef
 from nuitka.nodes.GeneratorNodes import (
     ExpressionGeneratorObjectBody,
     ExpressionMakeGeneratorObject,
     StatementGeneratorReturnNone,
@@ -399,25 +398,14 @@
                     for_asyncgen=False,
                     source_ref=source_ref,
                 ),
                 source_ref=source_ref.atInternal(),
             )
         )
 
-    if for_asyncgen and python_version >= 0x370 and node.generators[0].is_async:
-        statements.append(
-            makeStatementAssignmentVariable(
-                variable=iter_tmp,
-                source=ExpressionTempVariableRef(
-                    variable=iter_tmp, source_ref=source_ref
-                ),
-                source_ref=source_ref,
-            )
-        )
-
     if start_value is not None:
         statements.append(
             makeStatementAssignmentVariable(
                 variable=container_tmp,
                 source=makeConstantRefNode(constant=start_value, source_ref=source_ref),
                 source_ref=source_ref.atInternal(),
             )
@@ -436,15 +424,19 @@
                 ),
                 source_ref=source_ref,
             )
         else:
             assert emit_class is ExpressionYield
 
             current_body = emit_class(
-                buildNode(provider=function_body, node=node.elt, source_ref=source_ref),
+                buildNode(
+                    provider=function_body,
+                    node=node.elt,
+                    source_ref=source_ref,
+                ),
                 source_ref=source_ref,
             )
     else:
         current_body = emit_class(
             dict_arg=ExpressionTempVariableRef(
                 variable=container_tmp, source_ref=source_ref
             ),
@@ -586,15 +578,16 @@
 
     return statements, release_statements
 
 
 def _buildContractionNode(provider, node, name, emit_class, start_value, source_ref):
     # The contraction nodes are reformulated to function bodies, with loops as
     # described in the Developer Manual. They use a lot of temporary names,
-    # nested blocks, etc. and so a lot of variable names, pylint:disable=too-many-locals
+    # nested blocks, etc. and so a lot of variable names.
+    # pylint: disable=too-many-locals
 
     function_body = ExpressionOutlineFunction(
         provider=provider, name=intern(name[1:-1]), source_ref=source_ref
     )
 
     iter_tmp = function_body.allocateTempVariable(temp_scope=None, name=".0")
 
@@ -639,15 +632,15 @@
             provider=function_body,
             tried=mergeStatements((statements, return_statement)),
             final=release_statements,
             source_ref=source_ref.atInternal(),
         ),
     )
 
-    if python_version < 0x300:
+    if python_version < 0x300 or emit_class is not ExpressionYield:
         body = makeStatementsSequenceFromStatements(assign_iter_statement, statements)
     else:
         parent_module = provider.getParentModule()
 
         code_object = CodeObjectSpec(
             co_name=name,
             co_qualname=provider.getChildQualname(name),
@@ -662,15 +655,15 @@
             co_filename=parent_module.getRunTimeFilename(),
             co_lineno=source_ref.getLineNumber(),
             future_spec=parent_module.getFutureSpec(),
         )
 
         body = makeStatementsSequenceFromStatements(
             assign_iter_statement,
-            StatementsFrameFunction(
+            StatementsFrameGenerator(
                 statements=mergeStatements(statements, False),
                 code_object=code_object,
                 source_ref=source_ref,
             ),
         )
 
     function_body.setChildBody(body)
```

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationDictionaryCreation.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationDictionaryCreation.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationExecStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationExecStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationForLoopStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationForLoopStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationFunctionStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationFunctionStatements.py`

 * *Files 1% similar despite different names*

```diff
@@ -62,15 +62,15 @@
 )
 from nuitka.nodes.VariableRefNodes import (
     ExpressionTempVariableRef,
     ExpressionVariableRef,
 )
 from nuitka.nodes.VariableReleaseNodes import makeStatementReleaseVariable
 from nuitka.Options import hasPythonFlagNoAnnotations
-from nuitka.plugins.Plugins import Plugins
+from nuitka.plugins.Plugins import Plugins, hasActivePlugin
 from nuitka.PythonVersions import python_version
 from nuitka.specs.ParameterSpecs import ParameterSpec
 
 from .ReformulationExecStatements import wrapEvalGlobalsAndLocals
 from .ReformulationTryFinallyStatements import makeTryFinallyStatement
 from .SyntaxErrors import raiseSyntaxError
 from .TreeHelpers import (
@@ -133,33 +133,48 @@
             break
     else:
         decorators.append(
             makeExpressionBuiltinTypeRef(builtin_name=inject, source_ref=source_ref)
         )
 
 
+_has_pyqt_plugin = None
+
+
 def decideFunctionCompilationMode(decorators):
-    for decorator in decorators:
-        if (
-            decorator.isExpressionCall()
-            and decorator.subnode_called.isExpressionVariableNameRef()
-        ):
-            if decorator.subnode_called.variable_name == "pyqtSlot":
-                return "bytecode"
+    """Decide how to compile a function based on decorator names."""
+
+    global _has_pyqt_plugin  # singleton, pylint: disable=global-statement
+
+    if _has_pyqt_plugin is None:
+        _has_pyqt_plugin = hasActivePlugin("pyqt5") or hasActivePlugin("pyqt6")
+
+    # TODO: Expose the interface to plugins, so we don't hardcode stuff for
+    # specific plugins here, but for performance I guess, we would have to add a
+    # registry for the plugins to use, so not every decorator name is being
+    # called for every plugin.
+    if _has_pyqt_plugin:
+        for decorator in decorators:
+            if (
+                decorator.isExpressionCall()
+                and decorator.subnode_called.isExpressionVariableNameRef()
+            ):
+                if decorator.subnode_called.variable_name == "pyqtSlot":
+                    return "bytecode"
 
     return "compiled"
 
 
 def _buildBytecodeOrSourceFunction(provider, node, compilation_mode, source_ref):
     # TODO: We should have a compile() builtin usage here, lookup "co_code" and
     # support that as a constant value. We then would have the "bytecode" only
-    # in the binary, right now "bytecode" and "sourcecode" make no difference.
-    # For commercial, we need to protect this constant just like all the others,
-    # and ideally maybe, we add (delayed creation) code objects from blobs for
-    # use by compiled code, while doing this. pylint: disable=unused-argument
+    # in the binary, right now "bytecode" and "source" make no difference. For
+    # commercial, we need to protect this constant just like all the others, and
+    # ideally maybe, we add (delayed creation) code objects from blobs for use
+    # by compiled code, while doing this. pylint: disable=unused-argument
     source_code = ast.unparse(node)
 
     source = makeConstantRefNode(
         constant=source_code,
         source_ref=source_ref,
         user_provided=True,
     )
@@ -171,19 +186,24 @@
     #         mode=makeConstantRefNode(constant="exec", source_ref=source_ref),
     #         flags=None,
     #         dont_inherit=None,
     #         optimize=None,
     #         source_ref=source_ref
     #     )
 
+    # This is actually for the globals locals usage to be default values of the
+    # scope.
+
+    temp_scope = provider.allocateTempScope("function_exec")
+
     globals_ref, locals_ref, tried, final = wrapEvalGlobalsAndLocals(
         provider=provider,
         globals_node=None,
         locals_node=None,
-        temp_scope=None,
+        temp_scope=temp_scope,
         source_ref=source_ref,
     )
 
     tried = makeStatementsSequence(
         statements=(
             tried,
             (
@@ -560,14 +580,18 @@
 
     return kw_defaults
 
 
 def buildParameterAnnotations(provider, node, source_ref):
     # Too many branches, because there is too many cases, pylint: disable=too-many-branches
 
+    # The ast uses funny names a bunch.
+    # spellchecker: ignore varnames,elts,posonlyargs,kwonlyargs,varargannotation,vararg
+    # spellchecker: ignore kwargannotation
+
     # Build annotations. We are hiding here, that it is a Python3 only feature.
     if python_version < 0x300 or hasPythonFlagNoAnnotations():
         return None
 
     # Starting with Python 3.4, the names of parameters are mangled in
     # annotations as well.
     if python_version < 0x340:
```

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationImportStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationImportStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationLambdaExpressions.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationLambdaExpressions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationMatchStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationMatchStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationMultidist.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationMultidist.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationNamespacePackages.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationNamespacePackages.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationPrintStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationPrintStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationSequenceCreation.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationSequenceCreation.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationSubscriptExpressions.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationSubscriptExpressions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationTryExceptStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationTryExceptStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationTryFinallyStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationTryFinallyStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationWhileLoopStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationWhileLoopStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationWithStatements.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationWithStatements.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/ReformulationYieldExpressions.py` & `Nuitka-1.7.6/nuitka/tree/ReformulationYieldExpressions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/SourceHandling.py` & `Nuitka-1.7.6/nuitka/tree/SourceHandling.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/SyntaxErrors.py` & `Nuitka-1.7.6/nuitka/tree/SyntaxErrors.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/TreeHelpers.py` & `Nuitka-1.7.6/nuitka/tree/TreeHelpers.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/VariableClosure.py` & `Nuitka-1.7.6/nuitka/tree/VariableClosure.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/tree/__init__.py` & `Nuitka-1.7.6/nuitka/tree/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/AppDirs.py` & `Nuitka-1.7.6/nuitka/utils/AppDirs.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/CStrings.py` & `Nuitka-1.7.6/nuitka/utils/CStrings.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/CommandLineOptions.py` & `Nuitka-1.7.6/nuitka/utils/CommandLineOptions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Distributions.py` & `Nuitka-1.7.6/nuitka/utils/Distributions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Download.py` & `Nuitka-1.7.6/nuitka/utils/Download.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Execution.py` & `Nuitka-1.7.6/nuitka/utils/Execution.py`

 * *Files 2% similar despite different names*

```diff
@@ -329,22 +329,28 @@
         return subprocess.NULLDEV
     except AttributeError:
         # File is supposed to stay open, pylint: disable=consider-using-with
         subprocess.NULLDEV = open(os.devnull, "rb")
         return subprocess.NULLDEV
 
 
-def executeToolChecked(logger, command, absence_message, stderr_filter=None):
+def executeToolChecked(
+    logger, command, absence_message, stderr_filter=None, optional=False
+):
     """Execute external tool, checking for success and no error outputs, returning result."""
 
     command = list(command)
     tool = command[0]
 
     if not isExecutableCommand(tool):
-        logger.sysexit(absence_message)
+        if optional:
+            logger.warning(absence_message)
+            return 0, b"", b""
+        else:
+            logger.sysexit(absence_message)
 
     # Allow to avoid repeated scans in PATH for the tool.
     command[0] = getExecutablePath(tool)
 
     process = subprocess.Popen(
         command,
         stdin=getNullInput(),
```

### Comparing `Nuitka-1.7.5/nuitka/utils/FileOperations.py` & `Nuitka-1.7.6/nuitka/utils/FileOperations.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Hashing.py` & `Nuitka-1.7.6/nuitka/utils/Hashing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Images.py` & `Nuitka-1.7.6/nuitka/utils/Images.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Importing.py` & `Nuitka-1.7.6/nuitka/utils/Importing.py`

 * *Files 1% similar despite different names*

```diff
@@ -212,7 +212,16 @@
                 _compile_time_modules[module_name] = sys.modules[module_name]
 
     # Some code should only use this, after knowing it will be found. Complain if
     # that is not the case.
     assert _compile_time_modules[module_name] or not must_exist
 
     return _compile_time_modules[module_name] or None
+
+
+def isBuiltinModuleName(module_name):
+    if python_version < 0x300:
+        import imp as _imp
+    else:
+        import _imp
+
+    return _imp.is_builtin(module_name)
```

### Comparing `Nuitka-1.7.5/nuitka/utils/InstalledPythons.py` & `Nuitka-1.7.6/nuitka/utils/InstalledPythons.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/InstanceCounters.py` & `Nuitka-1.7.6/nuitka/utils/InstanceCounters.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Jinja2.py` & `Nuitka-1.7.6/nuitka/utils/Jinja2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Json.py` & `Nuitka-1.7.6/nuitka/utils/Json.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/MacOSApp.py` & `Nuitka-1.7.6/nuitka/utils/MacOSApp.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/MemoryUsage.py` & `Nuitka-1.7.6/nuitka/utils/MemoryUsage.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/ModuleNames.py` & `Nuitka-1.7.6/nuitka/utils/ModuleNames.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/ReExecute.py` & `Nuitka-1.7.6/nuitka/utils/ReExecute.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Rest.py` & `Nuitka-1.7.6/nuitka/utils/Rest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/SharedLibraries.py` & `Nuitka-1.7.6/nuitka/utils/SharedLibraries.py`

 * *Files 2% similar despite different names*

```diff
@@ -737,27 +737,40 @@
             continue
 
         result[os.path.basename(filename)] = filename
 
     return result
 
 
-def convertRPathToRunPath(filename):
+# spell-checker: ignore termux DT_RUNPATH
+_termux_elf_cleaner_usage = (
+    "Needs 'termux-elf-cleaner' to clean up created files. Install it for best results."
+)
+
+
+def cleanupHeaderForAndroid(filename):
     """Change a DT_RPATH to DT_RUNPATH
 
     On Android this seems required, because the linker doesn't support the one
     created by default.
     """
 
     with withEnvironmentVarOverridden("LANG", "C"):
         executeToolChecked(
             logger=postprocessing_logger,
             command=("patchelf", "--shrink-rpath", filename),
-            stderr_filter=_filterPatchelfErrorOutput,
             absence_message=_patchelf_usage,
+            stderr_filter=_filterPatchelfErrorOutput,
+        )
+
+        executeToolChecked(
+            logger=postprocessing_logger,
+            command=("termux-elf-cleaner", "--quiet", filename),
+            absence_message=_termux_elf_cleaner_usage,
+            optional=True,
         )
 
 
 _nm_usage = """\
 Error, needs 'nm' on your system, to detect exported DLL symbols."""
```

### Comparing `Nuitka-1.7.5/nuitka/utils/Shebang.py` & `Nuitka-1.7.6/nuitka/utils/Shebang.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Signing.py` & `Nuitka-1.7.6/nuitka/utils/Signing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/StaticLibraries.py` & `Nuitka-1.7.6/nuitka/utils/StaticLibraries.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/ThreadedExecutor.py` & `Nuitka-1.7.6/nuitka/utils/ThreadedExecutor.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Timing.py` & `Nuitka-1.7.6/nuitka/utils/Timing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Utils.py` & `Nuitka-1.7.6/nuitka/utils/Utils.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/WindowsFileUsage.py` & `Nuitka-1.7.6/nuitka/utils/WindowsFileUsage.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/WindowsResources.py` & `Nuitka-1.7.6/nuitka/utils/WindowsResources.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/Yaml.py` & `Nuitka-1.7.6/nuitka/utils/Yaml.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/nuitka/utils/__init__.py` & `Nuitka-1.7.6/nuitka/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/pyproject.toml` & `Nuitka-1.7.6/pyproject.toml`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/setup.py` & `Nuitka-1.7.6/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -385,15 +385,14 @@
         "Topic :: Software Development :: Quality Assurance",
         # Nuitka standalone mode aims at distribution
         "Topic :: System :: Software Distribution",
         # Python2 supported versions.
         "Programming Language :: Python :: 2.6",
         "Programming Language :: Python :: 2.7",
         # Python3 supported versions.
-        "Programming Language :: Python :: 3.3",
         "Programming Language :: Python :: 3.4",
         "Programming Language :: Python :: 3.5",
         "Programming Language :: Python :: 3.6",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
         "Programming Language :: Python :: 3.9",
         "Programming Language :: Python :: 3.10",
```

### Comparing `Nuitka-1.7.5/tests/basics/AssertsTest.py` & `Nuitka-1.7.6/tests/basics/AssertsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/AssignmentsTest.py` & `Nuitka-1.7.6/tests/basics/AssignmentsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/AssignmentsTest32.py` & `Nuitka-1.7.6/tests/basics/AssignmentsTest32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/BranchingTest.py` & `Nuitka-1.7.6/tests/basics/BranchingTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/BuiltinOverload.py` & `Nuitka-1.7.6/tests/basics/BuiltinOverload.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/BuiltinSuperTest.py` & `Nuitka-1.7.6/tests/basics/BuiltinSuperTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/BuiltinsTest.py` & `Nuitka-1.7.6/tests/basics/BuiltinsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ClassMinimalTest.py` & `Nuitka-1.7.6/tests/basics/ClassMinimalTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ClassesTest.py` & `Nuitka-1.7.6/tests/basics/ClassesTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ClassesTest32.py` & `Nuitka-1.7.6/tests/basics/ClassesTest32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ClassesTest34.py` & `Nuitka-1.7.6/tests/basics/ClassesTest34.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ComparisonChainsTest.py` & `Nuitka-1.7.6/tests/basics/ComparisonChainsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ConstantsTest.py` & `Nuitka-1.7.6/tests/basics/ConstantsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ConstantsTest27.py` & `Nuitka-1.7.6/tests/basics/ConstantsTest27.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/DecoratorsTest.py` & `Nuitka-1.7.6/tests/basics/DecoratorsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/DefaultParametersTest.py` & `Nuitka-1.7.6/tests/basics/DefaultParametersTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/DoubleDeletionsTest.py` & `Nuitka-1.7.6/tests/basics/DoubleDeletionsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/EmptyModuleTest.py` & `Nuitka-1.7.6/tests/basics/EmptyModuleTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ExceptionRaisingTest.py` & `Nuitka-1.7.6/tests/basics/ExceptionRaisingTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ExceptionRaisingTest32.py` & `Nuitka-1.7.6/tests/basics/ExceptionRaisingTest32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ExceptionRaisingTest33.py` & `Nuitka-1.7.6/tests/basics/ExceptionRaisingTest33.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ExecEvalTest.py` & `Nuitka-1.7.6/tests/basics/ExecEvalTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ExtremeClosureTest.py` & `Nuitka-1.7.6/tests/basics/ExtremeClosureTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/FunctionObjectsTest.py` & `Nuitka-1.7.6/tests/basics/FunctionObjectsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/FunctionsTest.py` & `Nuitka-1.7.6/tests/basics/FunctionsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/FunctionsTest32.py` & `Nuitka-1.7.6/tests/basics/FunctionsTest32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/FunctionsTest_2.py` & `Nuitka-1.7.6/tests/basics/FunctionsTest_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/FutureTest32.py` & `Nuitka-1.7.6/tests/basics/FutureTest32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/GeneratorExpressionsTest.py` & `Nuitka-1.7.6/tests/basics/GeneratorExpressionsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/GeneratorExpressionsTest_37.py` & `Nuitka-1.7.6/tests/basics/GeneratorExpressionsTest_37.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/GlobalStatementTest.py` & `Nuitka-1.7.6/tests/basics/GlobalStatementTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/HelloWorldTest_2.py` & `Nuitka-1.7.6/tests/basics/HelloWorldTest_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ImportingTest.py` & `Nuitka-1.7.6/tests/basics/ImportingTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/InplaceOperationsTest.py` & `Nuitka-1.7.6/tests/basics/InplaceOperationsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/InspectionTest.py` & `Nuitka-1.7.6/tests/basics/InspectionTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/InspectionTest_35.py` & `Nuitka-1.7.6/tests/basics/InspectionTest_35.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/InspectionTest_36.py` & `Nuitka-1.7.6/tests/basics/InspectionTest_36.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/LambdasTest.py` & `Nuitka-1.7.6/tests/basics/LambdasTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/LateClosureAssignmentTest.py` & `Nuitka-1.7.6/tests/basics/LateClosureAssignmentTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ListContractionsTest.py` & `Nuitka-1.7.6/tests/basics/ListContractionsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/LoopingTest.py` & `Nuitka-1.7.6/tests/basics/LoopingTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/MainProgramsTest.py` & `Nuitka-1.7.6/tests/basics/MainProgramsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ModuleAttributesTest.py` & `Nuitka-1.7.6/tests/basics/ModuleAttributesTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/OperatorsTest.py` & `Nuitka-1.7.6/tests/basics/OperatorsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/OrderChecksTest.py` & `Nuitka-1.7.6/tests/basics/OrderChecksTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/OrderChecksTest27.py` & `Nuitka-1.7.6/tests/basics/OrderChecksTest27.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/OverflowFunctionsTest_2.py` & `Nuitka-1.7.6/tests/basics/OverflowFunctionsTest_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ParameterErrorsTest.py` & `Nuitka-1.7.6/tests/basics/ParameterErrorsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ParameterErrorsTest32.py` & `Nuitka-1.7.6/tests/basics/ParameterErrorsTest32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/PrintFutureTest.py` & `Nuitka-1.7.6/tests/basics/PrintFutureTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/PrintingTest_2.py` & `Nuitka-1.7.6/tests/basics/PrintingTest_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/RecursionTest.py` & `Nuitka-1.7.6/tests/basics/RecursionTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ReferencingTest.py` & `Nuitka-1.7.6/tests/basics/ReferencingTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ReferencingTest27.py` & `Nuitka-1.7.6/tests/basics/ReferencingTest27.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ReferencingTest33.py` & `Nuitka-1.7.6/tests/basics/ReferencingTest33.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ReferencingTest35.py` & `Nuitka-1.7.6/tests/basics/ReferencingTest35.py`

 * *Files 0% similar despite different names*

```diff
@@ -92,15 +92,15 @@
         return value
 
 
 def simpleFunction3():
     async def f():
         result = []
 
-        # Python 3.5 before 3.2 won't allow this.
+        # Python 3.5 before 3.5.2 won't allow this.
         try:
             async for letter in AsyncIteratorWrapper("abcdefg"):
                 result.append(letter)
         except TypeError:
             assert sys.version_info < (3, 5, 2)
 
         return result
```

### Comparing `Nuitka-1.7.5/tests/basics/ReferencingTest36.py` & `Nuitka-1.7.6/tests/basics/ReferencingTest36.py`

 * *Files 6% similar despite different names*

```diff
@@ -61,15 +61,15 @@
         try:
             if exc:
                 exc = False
                 fut = coro.throw(AwaitException)
             else:
                 fut = coro.send(None)
         except StopIteration as ex:
-            return ex.args[0]
+            return ex.args[0] if ex.args else None
 
         if fut == ("throw",):
             exc = True
 
 
 def simpleFunction1():
     async def gen1():
@@ -77,15 +77,15 @@
             yield
         except:  # pylint: disable=bare-except
             pass
 
     async def run():
         g = gen1()
         await g.asend(None)
-        await g.asend(None)
+        await g.asend(2772)
 
     try:
         run_async(run())
     except StopAsyncIteration:
         pass
 
 
@@ -172,17 +172,39 @@
         rawdata = b"The quick brown fox jumps over the lazy dog.\r\n"
         # Be slow so we don't depend on other modules
         rawdata += bytes(range(256))
 
     return C()
 
 
+async def funcTrace1():
+    return [await awaitable() for _i in range(50)]
+
+
+def simpleFunction6():
+    run_async(funcTrace1())
+
+
+async def funcTrace2():
+    result = []
+
+    for _i in range(50):
+        value = await awaitable()
+        result.append(value)
+
+    return result
+
+
+def simpleFunction7():
+    run_async(funcTrace2())
+
+
 # This refleaks big time, but the construct is rare enough to not bother
 # as this proves hard to find.
-def disabled_simpleFunction6():
+def disabled_simpleFunction8():
     loop = asyncio.new_event_loop()
     asyncio.set_event_loop(None)
 
     async def waiter(timeout):
         await asyncio.sleep(timeout)
         yield 1
```

### Comparing `Nuitka-1.7.5/tests/basics/ReferencingTest_2.py` & `Nuitka-1.7.6/tests/basics/ReferencingTest_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/SlotsTest.py` & `Nuitka-1.7.6/tests/basics/SlotsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/ThreadedGeneratorsTest.py` & `Nuitka-1.7.6/tests/basics/ThreadedGeneratorsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/TrickAssignmentsTest32.py` & `Nuitka-1.7.6/tests/basics/TrickAssignmentsTest32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/TrickAssignmentsTest35.py` & `Nuitka-1.7.6/tests/basics/TrickAssignmentsTest35.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/TrickAssignmentsTest_2.py` & `Nuitka-1.7.6/tests/basics/TrickAssignmentsTest_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/TryContinueFinallyTest.py` & `Nuitka-1.7.6/tests/basics/TryContinueFinallyTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/TryExceptContinueTest.py` & `Nuitka-1.7.6/tests/basics/TryExceptContinueTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/TryExceptFinallyTest.py` & `Nuitka-1.7.6/tests/basics/TryExceptFinallyTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/TryExceptFramesTest.py` & `Nuitka-1.7.6/tests/basics/TryExceptFramesTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/TryReturnFinallyTest.py` & `Nuitka-1.7.6/tests/basics/TryReturnFinallyTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/TryYieldFinallyTest.py` & `Nuitka-1.7.6/tests/basics/TryYieldFinallyTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/UnicodeTest.py` & `Nuitka-1.7.6/tests/basics/UnicodeTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/UnpackingTest35.py` & `Nuitka-1.7.6/tests/basics/UnpackingTest35.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/VarargsTest.py` & `Nuitka-1.7.6/tests/basics/VarargsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/WithStatementsTest.py` & `Nuitka-1.7.6/tests/basics/WithStatementsTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/YieldFromTest33.py` & `Nuitka-1.7.6/tests/basics/YieldFromTest33.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/run_all.py` & `Nuitka-1.7.6/tests/basics/run_all.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/basics/run_xml.py` & `Nuitka-1.7.6/tests/basics/run_xml.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/onefile/HelloWorldTest.py` & `Nuitka-1.7.6/tests/onefile/HelloWorldTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/onefile/KeyboardInterruptTest.py` & `Nuitka-1.7.6/tests/onefile/KeyboardInterruptTest.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/onefile/run_all.py` & `Nuitka-1.7.6/tests/onefile/run_all.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/ArgumentTypes.py` & `Nuitka-1.7.6/tests/optimizations/ArgumentTypes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/Attributes.py` & `Nuitka-1.7.6/tests/optimizations/Attributes.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/Calls.py` & `Nuitka-1.7.6/tests/optimizations/Calls.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/Conditions.py` & `Nuitka-1.7.6/tests/optimizations/Conditions.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/DecodingOperations.py` & `Nuitka-1.7.6/tests/optimizations/DecodingOperations.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/FormatStrings36.py` & `Nuitka-1.7.6/tests/optimizations/FormatStrings36.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/HardImports.py` & `Nuitka-1.7.6/tests/optimizations/HardImports.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/HardImports_2.py` & `Nuitka-1.7.6/tests/optimizations/HardImports_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/Iterations.py` & `Nuitka-1.7.6/tests/optimizations/Iterations.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/Len.py` & `Nuitka-1.7.6/tests/optimizations/Len.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/Operations.py` & `Nuitka-1.7.6/tests/optimizations/Operations.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/Subscripts.py` & `Nuitka-1.7.6/tests/optimizations/Subscripts.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/optimizations/run_all.py` & `Nuitka-1.7.6/tests/optimizations/run_all.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/package_import_success_after_failure/PackageImportSuccessAfterFailure.py` & `Nuitka-1.7.6/tests/packages/package_import_success_after_failure/PackageImportSuccessAfterFailure.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/package_import_success_after_failure/variable_package/SomeModule.py` & `Nuitka-1.7.6/tests/packages/package_import_success_after_failure/variable_package/SomeModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/package_import_success_after_failure/variable_package/__init__.py` & `Nuitka-1.7.6/tests/packages/package_import_success_after_failure/variable_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/run_all.py` & `Nuitka-1.7.6/tests/packages/run_all.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/sub_package/kitty/__init__.py` & `Nuitka-1.7.6/tests/packages/sub_package/kitty/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/sub_package/kitty/bigkitty.py` & `Nuitka-1.7.6/tests/packages/sub_package/kitty/bigkitty.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/sub_package/kitty/smallkitty.py` & `Nuitka-1.7.6/tests/packages/sub_package/kitty/smallkitty.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/sub_package/kitty/speak/__init__.py` & `Nuitka-1.7.6/tests/packages/sub_package/kitty/speak/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/sub_package/kitty/speak/hello.py` & `Nuitka-1.7.6/tests/packages/sub_package/kitty/speak/hello.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/sub_package/kitty/speak/miau.py` & `Nuitka-1.7.6/tests/packages/sub_package/kitty/speak/miau.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/sub_package/kitty/speak/purr.py` & `Nuitka-1.7.6/tests/packages/sub_package/kitty/speak/purr.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/top_level_attributes_3/some_package/__init__.py` & `Nuitka-1.7.6/tests/packages/top_level_attributes_3/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/packages/top_level_attributes_3/some_package/some_module.py` & `Nuitka-1.7.6/tests/packages/top_level_attributes_3/some_package/some_module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/plugins/code_signing/CodeSigningMain.py` & `Nuitka-1.7.6/tests/plugins/code_signing/CodeSigningMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/plugins/data_files/DataFilesMain.py` & `Nuitka-1.7.6/tests/plugins/data_files/DataFilesMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/plugins/data_files/data_files_package/__init__.py` & `Nuitka-1.7.6/tests/plugins/data_files/data_files_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/plugins/parameters/ParametersMain.py` & `Nuitka-1.7.6/tests/plugins/parameters/ParametersMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/plugins/parameters/parameter-using-plugin.py` & `Nuitka-1.7.6/tests/plugins/parameters/parameter-using-plugin.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/plugins/run_all.py` & `Nuitka-1.7.6/tests/plugins/run_all.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/absolute_import/AbsoluteImportMain.py` & `Nuitka-1.7.6/tests/programs/absolute_import/AbsoluteImportMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/absolute_import/foobar/__init__.py` & `Nuitka-1.7.6/tests/programs/absolute_import/foobar/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/absolute_import/foobar/foobar.py` & `Nuitka-1.7.6/tests/programs/absolute_import/foobar/foobar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/absolute_import/foobar/local.py` & `Nuitka-1.7.6/tests/programs/absolute_import/foobar/local.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/absolute_import/foobar/util.py` & `Nuitka-1.7.6/tests/programs/absolute_import/foobar/util.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports1/CasedImportingMain.py` & `Nuitka-1.7.6/tests/programs/case_imports1/CasedImportingMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports1/path1/Some_Module.py` & `Nuitka-1.7.6/tests/programs/case_imports1/path1/Some_Module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports1/path1/Some_Package/__init__.py` & `Nuitka-1.7.6/tests/programs/case_imports1/path1/Some_Package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports1/path2/some_module.py` & `Nuitka-1.7.6/tests/programs/case_imports1/path2/some_module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports1/path2/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/case_imports1/path2/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports2/CasedImportingMain.py` & `Nuitka-1.7.6/tests/programs/case_imports2/CasedImportingMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports2/path1/some_module.py` & `Nuitka-1.7.6/tests/programs/case_imports2/path1/some_module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports2/path1/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/case_imports2/path1/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports2/path2/Some_Module.py` & `Nuitka-1.7.6/tests/programs/case_imports2/path2/Some_Module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports2/path2/Some_Package/__init__.py` & `Nuitka-1.7.6/tests/programs/case_imports2/path2/Some_Package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports3/CasedImportingMain.py` & `Nuitka-1.7.6/tests/programs/case_imports3/CasedImportingMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports3/path1/Some_Module.py` & `Nuitka-1.7.6/tests/programs/case_imports3/path1/Some_Module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports3/path1/Some_Package/__init__.py` & `Nuitka-1.7.6/tests/programs/case_imports3/path1/Some_Package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports3/path2/Some_Module.py` & `Nuitka-1.7.6/tests/programs/case_imports3/path2/Some_Module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/case_imports3/path2/Some_Package/__init__.py` & `Nuitka-1.7.6/tests/programs/case_imports3/path2/Some_Package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/cyclic_imports/CyclicImportsMain.py` & `Nuitka-1.7.6/tests/programs/cyclic_imports/CyclicImportsMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/cyclic_imports/cyclic_importing_package/Child1.py` & `Nuitka-1.7.6/tests/programs/cyclic_imports/cyclic_importing_package/Child1.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/cyclic_imports/cyclic_importing_package/Child2.py` & `Nuitka-1.7.6/tests/programs/cyclic_imports/cyclic_importing_package/Child2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/cyclic_imports/cyclic_importing_package/__init__.py` & `Nuitka-1.7.6/tests/programs/cyclic_imports/cyclic_importing_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/dash_import/DashImportMain.py` & `Nuitka-1.7.6/tests/programs/dash_import/DashImportMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/dash_import/dash-module.py` & `Nuitka-1.7.6/tests/programs/dash_import/dash-module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/dash_import/plus+module.py` & `Nuitka-1.7.6/tests/programs/dash_import/plus+module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/dash_main/Dash-Main.py` & `Nuitka-1.7.6/tests/programs/dash_main/Dash-Main.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/deep/DeepProgramMain.py` & `Nuitka-1.7.6/tests/programs/deep/DeepProgramMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/deep/some_package/DeepBrother.py` & `Nuitka-1.7.6/tests/programs/deep/some_package/DeepBrother.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/deep/some_package/DeepChild.py` & `Nuitka-1.7.6/tests/programs/deep/some_package/DeepChild.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/deep/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/deep/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/deep/some_package/deep_package/DeepDeepChild.py` & `Nuitka-1.7.6/tests/programs/deep/some_package/deep_package/DeepDeepChild.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/deep/some_package/deep_package/__init__.py` & `Nuitka-1.7.6/tests/programs/deep/some_package/deep_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/dunderinit_imports/DunderInitImportsMain.py` & `Nuitka-1.7.6/tests/programs/dunderinit_imports/DunderInitImportsMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/dunderinit_imports/package/SubModule.py` & `Nuitka-1.7.6/tests/programs/dunderinit_imports/package/SubModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/dunderinit_imports/package/__init__.py` & `Nuitka-1.7.6/tests/programs/dunderinit_imports/package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/import_variants/ImportVariationsMain.py` & `Nuitka-1.7.6/tests/programs/import_variants/ImportVariationsMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/import_variants/some_package/Child1.py` & `Nuitka-1.7.6/tests/programs/import_variants/some_package/Child1.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/import_variants/some_package/Child2.py` & `Nuitka-1.7.6/tests/programs/import_variants/some_package/Child2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/import_variants/some_package/Child3.py` & `Nuitka-1.7.6/tests/programs/import_variants/some_package/Child3.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/import_variants/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/import_variants/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/main_raises/ErrorMain.py` & `Nuitka-1.7.6/tests/programs/main_raises/ErrorMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/main_raises/ErrorRaising.py` & `Nuitka-1.7.6/tests/programs/main_raises/ErrorRaising.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/main_raises2/ErrorInFunctionMain.py` & `Nuitka-1.7.6/tests/programs/main_raises2/ErrorInFunctionMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/main_raises2/ErrorRaising.py` & `Nuitka-1.7.6/tests/programs/main_raises2/ErrorRaising.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_attributes/ModuleAttributesMain.py` & `Nuitka-1.7.6/tests/programs/module_attributes/ModuleAttributesMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_attributes/package_level1/Nearby1.py` & `Nuitka-1.7.6/tests/programs/module_attributes/package_level1/Nearby1.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_attributes/package_level1/__init__.py` & `Nuitka-1.7.6/tests/programs/module_attributes/package_level1/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/Nearby2.py` & `Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/Nearby2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/__init__.py` & `Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/package_level3/Nearby3.py` & `Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/package_level3/Nearby3.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_attributes/package_level1/package_level2/package_level3/__init__.py` & `Nuitka-1.7.6/tests/programs/module_attributes/package_level1/package_level2/package_level3/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_exits/ErrorExitingModule.py` & `Nuitka-1.7.6/tests/programs/module_exits/ErrorExitingModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_exits/Main.py` & `Nuitka-1.7.6/tests/programs/module_exits/Main.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_object_replacing/ModuleObjectReplacingMain.py` & `Nuitka-1.7.6/tests/programs/module_object_replacing/ModuleObjectReplacingMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/module_object_replacing/SelfReplacingModule.py` & `Nuitka-1.7.6/tests/programs/module_object_replacing/SelfReplacingModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/multiprocessing_using/MultiprocessingUsingMain.py` & `Nuitka-1.7.6/tests/programs/multiprocessing_using/MultiprocessingUsingMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/multiprocessing_using/foo/__init__.py` & `Nuitka-1.7.6/tests/programs/multiprocessing_using/foo/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/multiprocessing_using/foo/__main__.py` & `Nuitka-1.7.6/tests/programs/multiprocessing_using/foo/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/multiprocessing_using/foo/entry.py` & `Nuitka-1.7.6/tests/programs/multiprocessing_using/foo/entry.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/named_imports/NamedImportsMain.py` & `Nuitka-1.7.6/tests/programs/named_imports/NamedImportsMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/named_imports/some_package/SomeModule.py` & `Nuitka-1.7.6/tests/programs/named_imports/some_package/SomeModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/named_imports/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/named_imports/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/named_imports/some_package/sub_package/SomeModule.py` & `Nuitka-1.7.6/tests/programs/named_imports/some_package/sub_package/SomeModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_code/PackageInitCodeMain.py` & `Nuitka-1.7.6/tests/programs/package_code/PackageInitCodeMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_code/some_package/SomeModule.py` & `Nuitka-1.7.6/tests/programs/package_code/some_package/SomeModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_code/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/package_code/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_contains_main/PackageContainsMain.py` & `Nuitka-1.7.6/tests/programs/package_contains_main/PackageContainsMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_contains_main/__init__.py` & `Nuitka-1.7.6/tests/programs/package_contains_main/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_contains_main/local.py` & `Nuitka-1.7.6/tests/programs/package_contains_main/local.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_init_import/PackageInitImportMain.py` & `Nuitka-1.7.6/tests/programs/package_init_import/PackageInitImportMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_init_import/some_package/PackageLocal.py` & `Nuitka-1.7.6/tests/programs/package_init_import/some_package/PackageLocal.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_init_import/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/package_init_import/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_init_issue/PackageInitIssueMain.py` & `Nuitka-1.7.6/tests/programs/package_init_issue/PackageInitIssueMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_init_issue/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/package_init_issue/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_init_issue/some_package/child_package/SomeModule.py` & `Nuitka-1.7.6/tests/programs/package_init_issue/some_package/child_package/SomeModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_init_issue/some_package/child_package/__init__.py` & `Nuitka-1.7.6/tests/programs/package_init_issue/some_package/child_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_missing_init/PackageMissingInitMain.py` & `Nuitka-1.7.6/tests/programs/package_missing_init/PackageMissingInitMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_missing_init/some_package/some_module.py` & `Nuitka-1.7.6/tests/programs/package_missing_init/some_package/some_module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_missing_init/some_package/sub_package/some_sub_module.py` & `Nuitka-1.7.6/tests/programs/package_missing_init/some_package/sub_package/some_sub_module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_module_collision/PackageAndModuleNamedSameMain.py` & `Nuitka-1.7.6/tests/programs/package_module_collision/PackageAndModuleNamedSameMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_module_collision/Something/__init__.py` & `Nuitka-1.7.6/tests/programs/package_module_collision/Something/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_module_collision/something.py` & `Nuitka-1.7.6/tests/programs/package_module_collision/something.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_overload/Main.py` & `Nuitka-1.7.6/tests/programs/package_overload/Main.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_overload/foo/__init__.py` & `Nuitka-1.7.6/tests/programs/package_overload/foo/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_overload/foo/bar.py` & `Nuitka-1.7.6/tests/programs/package_overload/foo/bar.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_overload/foo/bar2.py` & `Nuitka-1.7.6/tests/programs/package_overload/foo/bar2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_prevents_submodule/PackagePreventsSubmoduleMain.py` & `Nuitka-1.7.6/tests/programs/package_prevents_submodule/PackagePreventsSubmoduleMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_prevents_submodule/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/package_prevents_submodule/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_prevents_submodule/some_package/some_module.py` & `Nuitka-1.7.6/tests/programs/package_prevents_submodule/some_package/some_module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_program/PackageAsMain/__init__.py` & `Nuitka-1.7.6/tests/programs/package_program/PackageAsMain/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/package_program/PackageAsMain/__main__.py` & `Nuitka-1.7.6/tests/programs/package_program/PackageAsMain/__main__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_itermodules/PkgUtilIterModulesMain.py` & `Nuitka-1.7.6/tests/programs/pkgutil_itermodules/PkgUtilIterModulesMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package1/SomeModuleC.py` & `Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package1/SomeModuleC.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package1/SomeModuleD.py` & `Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package1/SomeModuleD.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package1/__init__.py` & `Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package1/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package2/SomeModuleA.py` & `Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package2/SomeModuleA.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package2/SomeModuleB.py` & `Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package2/SomeModuleB.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_itermodules/some_package/sub_package2/__init__.py` & `Nuitka-1.7.6/tests/programs/pkgutil_itermodules/some_package/sub_package2/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_usage/PkgUtilUsageMain.py` & `Nuitka-1.7.6/tests/programs/pkgutil_usage/PkgUtilUsageMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/pkgutil_usage/package/__init__.py` & `Nuitka-1.7.6/tests/programs/pkgutil_usage/package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/plugin_import/PluginImportMain.py` & `Nuitka-1.7.6/tests/programs/plugin_import/PluginImportMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/plugin_import/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/plugin_import/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/plugin_import/some_package/some_module.py` & `Nuitka-1.7.6/tests/programs/plugin_import/some_package/some_module.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/reimport_main_dynamic/ImportItselfDynamicMain.py` & `Nuitka-1.7.6/tests/programs/reimport_main_dynamic/ImportItselfDynamicMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/reimport_main_static/ImportItselfStaticMain.py` & `Nuitka-1.7.6/tests/programs/reimport_main_static/ImportItselfStaticMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/relative_import/RelativeImportMain.py` & `Nuitka-1.7.6/tests/programs/relative_import/RelativeImportMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/relative_import/dircache.py` & `Nuitka-1.7.6/tests/programs/relative_import/dircache.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/resource_reader37/ResourceReaderMain.py` & `Nuitka-1.7.6/tests/programs/resource_reader37/ResourceReaderMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/resource_reader37/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/resource_reader37/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/run_all.py` & `Nuitka-1.7.6/tests/programs/run_all.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/stdlib_overload/StdlibOverloadMain.py` & `Nuitka-1.7.6/tests/programs/stdlib_overload/StdlibOverloadMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/stdlib_overload/pyexpat.py` & `Nuitka-1.7.6/tests/programs/stdlib_overload/pyexpat.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/stdlib_overload/some_package/__init__.py` & `Nuitka-1.7.6/tests/programs/stdlib_overload/some_package/__init__.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/stdlib_overload/some_package/normal_importing.py` & `Nuitka-1.7.6/tests/programs/stdlib_overload/some_package/normal_importing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/stdlib_overload/some_package/pyexpat.py` & `Nuitka-1.7.6/tests/programs/stdlib_overload/some_package/pyexpat.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/stdlib_overload/some_package/star_importing.py` & `Nuitka-1.7.6/tests/programs/stdlib_overload/some_package/star_importing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/syntax_errors/IndentationErroring.py` & `Nuitka-1.7.6/tests/programs/syntax_errors/IndentationErroring.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/syntax_errors/SyntaxErroring.py` & `Nuitka-1.7.6/tests/programs/syntax_errors/SyntaxErroring.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/syntax_errors/SyntaxErrorsMain.py` & `Nuitka-1.7.6/tests/programs/syntax_errors/SyntaxErrorsMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/unicode_bom/UnicodeBomMain.py` & `Nuitka-1.7.6/tests/programs/unicode_bom/UnicodeBomMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/unicode_bom/unicode_bom.py` & `Nuitka-1.7.6/tests/programs/unicode_bom/unicode_bom.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/programs/with space/Space Main.py` & `Nuitka-1.7.6/tests/programs/with space/Space Main.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/reflected/compile_itself.py` & `Nuitka-1.7.6/tests/reflected/compile_itself.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/run-tests` & `Nuitka-1.7.6/tests/run-tests`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/BrotliUsing.py` & `Nuitka-1.7.6/tests/standalone/BrotliUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/CtypesUsing.py` & `Nuitka-1.7.6/tests/standalone/CtypesUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/FlaskUsing.py` & `Nuitka-1.7.6/tests/standalone/FlaskUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/GlfwUsing.py` & `Nuitka-1.7.6/tests/standalone/GlfwUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/GtkUsing.py` & `Nuitka-1.7.6/tests/standalone/GtkUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/HexEncodingTest_2.py` & `Nuitka-1.7.6/tests/standalone/HexEncodingTest_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/IdnaUsing.py` & `Nuitka-1.7.6/tests/standalone/IdnaUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/LxmlUsing.py` & `Nuitka-1.7.6/tests/standalone/LxmlUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/MatplotlibUsing.py` & `Nuitka-1.7.6/tests/standalone/MatplotlibUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/MetadataPackagesUsing.py` & `Nuitka-1.7.6/tests/standalone/MetadataPackagesUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/NumpyUsing.py` & `Nuitka-1.7.6/tests/standalone/NumpyUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/OpenGLUsing.py` & `Nuitka-1.7.6/tests/standalone/OpenGLUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PandasUsing.py` & `Nuitka-1.7.6/tests/standalone/PandasUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PasslibUsing.py` & `Nuitka-1.7.6/tests/standalone/PasslibUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PendulumUsing.py` & `Nuitka-1.7.6/tests/standalone/PendulumUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PkgResourcesRequiresUsing.py` & `Nuitka-1.7.6/tests/standalone/PkgResourcesRequiresUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PmwUsing.py` & `Nuitka-1.7.6/tests/standalone/PmwUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PyQt5Plugins.py` & `Nuitka-1.7.6/tests/standalone/PyQt5Plugins.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PyQt5SSLSupport.py` & `Nuitka-1.7.6/tests/standalone/PyQt5SSLSupport.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PyQt5Using.py` & `Nuitka-1.7.6/tests/standalone/PyQt5Using.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PyQt6Plugins.py` & `Nuitka-1.7.6/tests/standalone/PyQt6Plugins.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PyQt6Using.py` & `Nuitka-1.7.6/tests/standalone/PyQt6Using.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PySide6Plugins.py` & `Nuitka-1.7.6/tests/standalone/PySide6Plugins.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/PySide6Using.py` & `Nuitka-1.7.6/tests/standalone/PySide6Using.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/RsaUsing.py` & `Nuitka-1.7.6/tests/standalone/RsaUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/ShlibUsing.py` & `Nuitka-1.7.6/tests/standalone/ShlibUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/SocketUsing.py` & `Nuitka-1.7.6/tests/standalone/SocketUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/TkInterUsing.py` & `Nuitka-1.7.6/tests/standalone/TkInterUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/Urllib3Using.py` & `Nuitka-1.7.6/tests/standalone/Urllib3Using.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/Win32ComUsing.py` & `Nuitka-1.7.6/tests/standalone/Win32ComUsing.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/run_all.py` & `Nuitka-1.7.6/tests/standalone/run_all.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/standalone/zip_importer/ZipImporterMain.py` & `Nuitka-1.7.6/tests/standalone/zip_importer/ZipImporterMain.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/AsyncgenReturn36.py` & `Nuitka-1.7.6/tests/syntax/AsyncgenReturn36.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/BreakWithoutLoop.py` & `Nuitka-1.7.6/tests/syntax/BreakWithoutLoop.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/ClassReturn.py` & `Nuitka-1.7.6/tests/syntax/ClassReturn.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/ClosureDel_2.py` & `Nuitka-1.7.6/tests/syntax/ClosureDel_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/ContinueWithoutLoop.py` & `Nuitka-1.7.6/tests/syntax/ContinueWithoutLoop.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/DuplicateArgument.py` & `Nuitka-1.7.6/tests/syntax/DuplicateArgument.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/ExecWithNesting_2.py` & `Nuitka-1.7.6/tests/syntax/ExecWithNesting_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/FutureBraces.py` & `Nuitka-1.7.6/tests/syntax/FutureBraces.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/FutureUnknown.py` & `Nuitka-1.7.6/tests/syntax/FutureUnknown.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/GeneratorExpressions38.py` & `Nuitka-1.7.6/tests/syntax/GeneratorExpressions38.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/GeneratorReturn_2.py` & `Nuitka-1.7.6/tests/syntax/GeneratorReturn_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/GlobalForParameter.py` & `Nuitka-1.7.6/tests/syntax/GlobalForParameter.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/Importing32.py` & `Nuitka-1.7.6/tests/syntax/Importing32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/IndentationError.py` & `Nuitka-1.7.6/tests/syntax/IndentationError.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/LateFutureImport.py` & `Nuitka-1.7.6/tests/syntax/LateFutureImport.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/MisplacedFutureImport.py` & `Nuitka-1.7.6/tests/syntax/MisplacedFutureImport.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/ModuleReturn.py` & `Nuitka-1.7.6/tests/syntax/ModuleReturn.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/NonAsciiWithoutEncoding_2.py` & `Nuitka-1.7.6/tests/syntax/NonAsciiWithoutEncoding_2.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/NonlocalForParameter32.py` & `Nuitka-1.7.6/tests/syntax/NonlocalForParameter32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/NonlocalNotFound32.py` & `Nuitka-1.7.6/tests/syntax/NonlocalNotFound32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/StarImportExtra.py` & `Nuitka-1.7.6/tests/syntax/StarImportExtra.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/SyntaxError.py` & `Nuitka-1.7.6/tests/syntax/SyntaxError.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/TryExceptAllNotLast.py` & `Nuitka-1.7.6/tests/syntax/TryExceptAllNotLast.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/TryFinallyContinue_37.py` & `Nuitka-1.7.6/tests/syntax/TryFinallyContinue_37.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/UnpackNoTuple.py` & `Nuitka-1.7.6/tests/syntax/UnpackNoTuple.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/UnpackTwoStars32.py` & `Nuitka-1.7.6/tests/syntax/UnpackTwoStars32.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/YieldFromInModule.py` & `Nuitka-1.7.6/tests/syntax/YieldFromInModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/YieldInAsync35.py` & `Nuitka-1.7.6/tests/syntax/YieldInAsync35.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/YieldInGenexp38.py` & `Nuitka-1.7.6/tests/syntax/YieldInGenexp38.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/YieldInModule.py` & `Nuitka-1.7.6/tests/syntax/YieldInModule.py`

 * *Files identical despite different names*

### Comparing `Nuitka-1.7.5/tests/syntax/run_all.py` & `Nuitka-1.7.6/tests/syntax/run_all.py`

 * *Files identical despite different names*

