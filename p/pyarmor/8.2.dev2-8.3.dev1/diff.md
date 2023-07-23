# Comparing `tmp/pyarmor-8.2.dev2.zip` & `tmp/pyarmor-8.3.dev1.zip`

## zipinfo {}

```diff
@@ -1,139 +1,145 @@
-Zip file size: 2309362 bytes, number of entries: 137
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/pyarmor.egg-info/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/
--rw-r--r--  2.0 unx     3004 b- defN 23-May-01 10:26 pyarmor-8.2.dev2/PKG-INFO
--rwxr-xr-x  2.0 unx      191 b- defN 23-Mar-04 11:58 pyarmor-8.2.dev2/MANIFEST.in
--rw-r--r--  2.0 unx     6692 b- defN 23-Apr-20 10:36 pyarmor-8.2.dev2/README.md
--rw-r--r--  2.0 unx     4296 b- defN 23-Apr-30 20:14 pyarmor-8.2.dev2/setup.py
--rw-r--r--  2.0 unx       38 b- defN 23-May-01 10:26 pyarmor-8.2.dev2/setup.cfg
--rw-r--r--  2.0 unx     3004 b- defN 23-May-01 10:26 pyarmor-8.2.dev2/pyarmor.egg-info/PKG-INFO
--rw-r--r--  2.0 unx     2911 b- defN 23-May-01 10:26 pyarmor-8.2.dev2/pyarmor.egg-info/SOURCES.txt
--rw-r--r--  2.0 unx      135 b- defN 23-May-01 10:26 pyarmor-8.2.dev2/pyarmor.egg-info/entry_points.txt
--rw-r--r--  2.0 unx       27 b- defN 23-May-01 10:26 pyarmor-8.2.dev2/pyarmor.egg-info/requires.txt
--rw-r--r--  2.0 unx        8 b- defN 23-May-01 10:26 pyarmor-8.2.dev2/pyarmor.egg-info/top_level.txt
--rw-r--r--  2.0 unx        1 b- defN 23-May-01 10:26 pyarmor-8.2.dev2/pyarmor.egg-info/dependency_links.txt
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/platforms/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/plugins/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/cli/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/polyfills/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/helper/
--rw-r--r--  2.0 unx      234 b- defN 19-Dec-07 07:11 pyarmor-8.2.dev2/src/pyshield.lic
--rwxr-xr-x  2.0 unx     2038 b- defN 23-Apr-30 20:13 pyarmor-8.2.dev2/src/config.py
--rwxr-xr-x  2.0 unx    10197 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/benchmark.py
--rw-r--r--  2.0 unx     7265 b- defN 22-Feb-25 10:48 pyarmor-8.2.dev2/src/register.py
--rw-r--r--  2.0 unx      140 b- defN 19-Dec-07 07:11 pyarmor-8.2.dev2/src/product.key
--rwxr-xr-x  2.0 unx    65827 b- defN 23-Mar-26 00:20 pyarmor-8.2.dev2/src/pyarmor.py
--rw-r--r--  2.0 unx     2664 b- defN 22-Jan-29 09:20 pyarmor-8.2.dev2/src/protect_code.pt
--rw-r--r--  2.0 unx    13587 b- defN 21-Nov-02 17:34 pyarmor-8.2.dev2/src/pytransform.py
--rw-r--r--  2.0 unx     3363 b- defN 22-Jun-27 00:08 pyarmor-8.2.dev2/src/sppmode.py
--rw-r--r--  2.0 unx      140 b- defN 19-Dec-07 07:11 pyarmor-8.2.dev2/src/public.key
--rwxr-xr-x  2.0 unx      113 b- defN 20-Jan-02 11:09 pyarmor-8.2.dev2/src/__init__.py
--rw-r--r--  2.0 unx     2191 b- defN 22-Dec-04 19:13 pyarmor-8.2.dev2/src/reform.py
--rwxr-xr-x  2.0 unx    25832 b- defN 22-Nov-20 13:42 pyarmor-8.2.dev2/src/packer.py
--rw-r--r--  2.0 unx     5200 b- defN 23-Jan-06 00:02 pyarmor-8.2.dev2/src/cobuilder.py
--rwxr-xr-x  2.0 unx    67431 b- defN 22-Dec-23 17:42 pyarmor-8.2.dev2/src/utils.py
--rw-r--r--  2.0 unx       37 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/pyarmor-webui.py
--rw-r--r--  2.0 unx     4028 b- defN 21-Dec-16 08:28 pyarmor-8.2.dev2/src/build_meta.py
--rw-r--r--  2.0 unx      256 b- defN 19-Dec-07 07:11 pyarmor-8.2.dev2/src/license.tri
--rw-r--r--  2.0 unx     1598 b- defN 23-Mar-04 17:07 pyarmor-8.2.dev2/src/README.rst
--rw-r--r--  2.0 unx     1596 b- defN 22-Jan-30 11:51 pyarmor-8.2.dev2/src/protect_code2.pt
--rw-r--r--  2.0 unx     2487 b- defN 19-Dec-07 07:11 pyarmor-8.2.dev2/src/public_capsule.zip
--rwxr-xr-x  2.0 unx     8023 b- defN 22-Jun-28 09:01 pyarmor-8.2.dev2/src/project.py
--rw-r--r--  2.0 unx      140 b- defN 19-Dec-07 07:11 pyarmor-8.2.dev2/src/pyshield.key
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/platforms/linux/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/platforms/darwin/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/platforms/windows/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/platforms/linux/x86/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/platforms/linux/x86_64/
--rwxr-xr-x  2.0 unx  1421600 b- defN 22-Sep-28 20:59 pyarmor-8.2.dev2/src/platforms/linux/x86/_pytransform.so
--rwxr-xr-x  2.0 unx  1198080 b- defN 22-Sep-28 20:59 pyarmor-8.2.dev2/src/platforms/linux/x86_64/_pytransform.so
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/platforms/darwin/x86_64/
--rwxr-xr-x  2.0 unx  1469620 b- defN 22-Sep-28 18:28 pyarmor-8.2.dev2/src/platforms/darwin/x86_64/_pytransform.dylib
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/platforms/windows/x86/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/platforms/windows/x86_64/
--rw-r--r--  2.0 unx  1373710 b- defN 22-Sep-28 21:00 pyarmor-8.2.dev2/src/platforms/windows/x86/_pytransform.dll
--rwxr-xr-x  2.0 unx  1165824 b- defN 22-Sep-28 20:59 pyarmor-8.2.dev2/src/platforms/windows/x86_64/_pytransform.dll
--rw-r--r--  2.0 unx     6360 b- defN 22-Jul-14 19:38 pyarmor-8.2.dev2/src/plugins/README.md
--rw-r--r--  2.0 unx    13688 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/plugins/check_ntp_time.py
--rw-r--r--  2.0 unx    10694 b- defN 23-Apr-20 15:01 pyarmor-8.2.dev2/src/cli/config.py
--rw-r--r--  2.0 unx    17413 b- defN 23-Apr-29 13:01 pyarmor-8.2.dev2/src/cli/register.py
--rw-r--r--  2.0 unx     5532 b- defN 23-Apr-30 16:53 pyarmor-8.2.dev2/src/cli/generate.py
--rw-r--r--  2.0 unx     2193 b- defN 23-Feb-22 22:43 pyarmor-8.2.dev2/src/cli/shell.py
--rw-r--r--  2.0 unx     6398 b- defN 23-Apr-13 14:46 pyarmor-8.2.dev2/src/cli/resource.py
--rw-r--r--  2.0 unx     1479 b- defN 23-Apr-29 22:32 pyarmor-8.2.dev2/src/cli/__init__.py
--rw-r--r--  2.0 unx    17473 b- defN 23-Apr-30 18:02 pyarmor-8.2.dev2/src/cli/context.py
--rw-r--r--  2.0 unx     2847 b- defN 23-Apr-22 22:15 pyarmor-8.2.dev2/src/cli/plugin.py
--rw-r--r--  2.0 unx     3956 b- defN 23-Apr-20 15:02 pyarmor-8.2.dev2/src/cli/mixer.py
--rw-r--r--  2.0 unx     2487 b- defN 23-Mar-26 06:51 pyarmor-8.2.dev2/src/cli/public_capsule.zip
--rw-r--r--  2.0 unx     8186 b- defN 23-May-01 10:05 pyarmor-8.2.dev2/src/cli/default.cfg
--rw-r--r--  2.0 unx    22526 b- defN 23-Apr-30 05:18 pyarmor-8.2.dev2/src/cli/__main__.py
--rw-r--r--  2.0 unx    11386 b- defN 23-Apr-20 15:01 pyarmor-8.2.dev2/src/cli/repack.py
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/helloworld/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/cx_Freeze/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/simple/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/pybench/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/testpkg/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/testmod/
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/py2exe/
--rwxr-xr-x  2.0 unx     2048 b- defN 22-Mar-10 20:03 pyarmor-8.2.dev2/src/examples/obfuscate-pkg.bat
--rwxr-xr-x  2.0 unx     1645 b- defN 22-Mar-10 20:03 pyarmor-8.2.dev2/src/examples/obfuscate-app.bat
--rwxr-xr-x  2.0 unx     1103 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/examples/obfuscate-app.sh
--rwxr-xr-x  2.0 unx     1685 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/examples/obfuscate-pkg.sh
--rwxr-xr-x  2.0 unx     4102 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/examples/build-with-project.bat
--rw-r--r--  2.0 unx     6876 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/examples/README.md
--rwxr-xr-x  2.0 unx      773 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/examples/pack-obfuscated-scripts.sh
--rwxr-xr-x  2.0 unx      928 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/examples/pack-obfuscated-scripts.bat
--rwxr-xr-x  2.0 unx     3146 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/examples/build-with-project.sh
--rwxr-xr-x  2.0 unx     4395 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/build-for-freeze.bat
--rw-r--r--  2.0 unx     7078 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/examples/README-ZH.md
--rwxr-xr-x  2.0 unx     4231 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/build-for-exe.bat
--rw-r--r--  2.0 unx     1747 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/helloworld/foo.py
--rwxr-xr-x  2.0 unx       49 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/cx_Freeze/hello.py
--rwxr-xr-x  2.0 unx     2309 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/cx_Freeze/queens.py
--rwxr-xr-x  2.0 unx      641 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/cx_Freeze/setup.py
--rwxr-xr-x  2.0 unx     2309 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/simple/queens.py
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/pybench/package/
--rwxr-xr-x  2.0 unx    13565 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Arithmetic.py
--rwxr-xr-x  2.0 unx     4134 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/With.py
--rwxr-xr-x  2.0 unx     6460 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Lists.py
--rwxr-xr-x  2.0 unx     8034 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Tuples.py
--rwxr-xr-x  2.0 unx     1388 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Instances.py
--rwxr-xr-x  2.0 unx     6672 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/systimes.py
--rwxr-xr-x  2.0 unx     1193 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/clockres.py
--rwxr-xr-x  2.0 unx    15254 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Lookups.py
--rwxr-xr-x  2.0 unx    16870 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/CommandLine.py
--rwxr-xr-x  2.0 unx    16198 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Numbers.py
--rwxr-xr-x  2.0 unx     2941 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Imports.py
--rwxr-xr-x  2.0 unx      961 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Setup.py
--rwxr-xr-x  2.0 unx    13400 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Exceptions.py
--rwxr-xr-x  2.0 unx     9261 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Dict.py
--rwxr-xr-x  2.0 unx    31828 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/pybench.py
--rwxr-xr-x  2.0 unx     1561 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/NewInstances.py
--rwxr-xr-x  2.0 unx     9252 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Calls.py
--rwxr-xr-x  2.0 unx    10946 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Strings.py
--rwxr-xr-x  2.0 unx    13207 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/Constructs.py
--rwxr-xr-x  2.0 unx        0 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/package/__init__.py
--rwxr-xr-x  2.0 unx        0 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/pybench/package/submodule.py
-drwxr-xr-x  2.0 unx        0 b- stor 23-May-01 10:26 pyarmor-8.2.dev2/src/examples/testpkg/mypkg/
--rw-r--r--  2.0 unx       66 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/testpkg/main.py
--rw-r--r--  2.0 unx      202 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/testpkg/mypkg/__init__.py
--rw-r--r--  2.0 unx       45 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/testpkg/mypkg/foo.py
--rwxr-xr-x  2.0 unx     1734 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/testmod/hello.py
--rwxr-xr-x  2.0 unx     3694 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/testmod/queens.py
--rwxr-xr-x  2.0 unx       44 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/py2exe/hello.py
--rwxr-xr-x  2.0 unx     2309 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/py2exe/queens.py
--rwxr-xr-x  2.0 unx     1081 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/examples/py2exe/setup.py
--rw-r--r--  2.0 unx       28 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/polyfills/__init__.py
--rwxr-xr-x  2.0 unx    88440 b- defN 19-Dec-05 18:38 pyarmor-8.2.dev2/src/polyfills/argparse.py
--rw-r--r--  2.0 unx     1505 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/helper/superuntime.py
--rw-r--r--  2.0 unx     9191 b- defN 22-Jan-06 22:40 pyarmor-8.2.dev2/src/helper/merge.py
--rw-r--r--  2.0 unx    11618 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/helper/buildext.py
--rw-r--r--  2.0 unx     2144 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/helper/get_platform_name.py
--rw-r--r--  2.0 unx      778 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/helper/get_license_info.py
--rw-r--r--  2.0 unx      728 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/helper/get_bind_key.py
--rw-r--r--  2.0 unx        1 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/helper/__init__.py
--rw-r--r--  2.0 unx     3821 b- defN 21-Oct-13 13:01 pyarmor-8.2.dev2/src/helper/build_data_module.py
--rw-r--r--  2.0 unx    12719 b- defN 23-Mar-21 13:48 pyarmor-8.2.dev2/src/helper/repack.py
-137 files, 7374484 bytes uncompressed, 2287638 bytes compressed:  69.0%
+Zip file size: 2330610 bytes, number of entries: 143
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor.egg-info/
+-rw-r--r--  2.0 unx     3004 b- defN 23-Jul-23 20:58 pyarmor-8.3.dev1/PKG-INFO
+-rwxr-xr-x  2.0 unx      191 b- defN 23-Mar-04 11:58 pyarmor-8.3.dev1/MANIFEST.in
+-rw-r--r--  2.0 unx     6553 b- defN 23-May-11 12:30 pyarmor-8.3.dev1/README.md
+-rw-r--r--  2.0 unx     4352 b- defN 23-Jul-19 09:21 pyarmor-8.3.dev1/setup.py
+-rw-r--r--  2.0 unx       38 b- defN 23-Jul-23 20:58 pyarmor-8.3.dev1/setup.cfg
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/platforms/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/plugins/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/cli/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/polyfills/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/helper/
+-rw-r--r--  2.0 unx      234 b- defN 19-Dec-07 07:11 pyarmor-8.3.dev1/pyarmor/pyshield.lic
+-rwxr-xr-x  2.0 unx     2038 b- defN 23-Jul-19 09:21 pyarmor-8.3.dev1/pyarmor/config.py
+-rwxr-xr-x  2.0 unx    10197 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/benchmark.py
+-rw-r--r--  2.0 unx     6994 b- defN 23-May-12 06:32 pyarmor-8.3.dev1/pyarmor/register.py
+-rw-r--r--  2.0 unx      140 b- defN 19-Dec-07 07:11 pyarmor-8.3.dev1/pyarmor/product.key
+-rwxr-xr-x  2.0 unx    65827 b- defN 23-Mar-26 00:20 pyarmor-8.3.dev1/pyarmor/pyarmor.py
+-rw-r--r--  2.0 unx     2664 b- defN 22-Jan-29 09:20 pyarmor-8.3.dev1/pyarmor/protect_code.pt
+-rw-r--r--  2.0 unx    13587 b- defN 21-Nov-02 17:34 pyarmor-8.3.dev1/pyarmor/pytransform.py
+-rw-r--r--  2.0 unx     3363 b- defN 22-Jun-27 00:08 pyarmor-8.3.dev1/pyarmor/sppmode.py
+-rw-r--r--  2.0 unx      140 b- defN 19-Dec-07 07:11 pyarmor-8.3.dev1/pyarmor/public.key
+-rwxr-xr-x  2.0 unx      113 b- defN 20-Jan-02 11:09 pyarmor-8.3.dev1/pyarmor/__init__.py
+-rw-r--r--  2.0 unx     2191 b- defN 22-Dec-04 19:13 pyarmor-8.3.dev1/pyarmor/reform.py
+-rwxr-xr-x  2.0 unx    25832 b- defN 22-Nov-20 13:42 pyarmor-8.3.dev1/pyarmor/packer.py
+-rw-r--r--  2.0 unx     5200 b- defN 23-Jan-06 00:02 pyarmor-8.3.dev1/pyarmor/cobuilder.py
+-rwxr-xr-x  2.0 unx    67431 b- defN 22-Dec-23 17:42 pyarmor-8.3.dev1/pyarmor/utils.py
+-rw-r--r--  2.0 unx       37 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/pyarmor-webui.py
+-rwxr-xr-x  2.0 unx    28176 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/pyarmor-deprecated.py
+-rw-r--r--  2.0 unx     4028 b- defN 21-Dec-16 08:28 pyarmor-8.3.dev1/pyarmor/build_meta.py
+-rw-r--r--  2.0 unx      256 b- defN 19-Dec-07 07:11 pyarmor-8.3.dev1/pyarmor/license.tri
+-rw-r--r--  2.0 unx     1598 b- defN 23-Mar-04 17:07 pyarmor-8.3.dev1/pyarmor/README.rst
+-rw-r--r--  2.0 unx     1596 b- defN 22-Jan-30 11:51 pyarmor-8.3.dev1/pyarmor/protect_code2.pt
+-rw-r--r--  2.0 unx     2234 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/pyimcore.py
+-rw-r--r--  2.0 unx     2487 b- defN 19-Dec-07 07:11 pyarmor-8.3.dev1/pyarmor/public_capsule.zip
+-rwxr-xr-x  2.0 unx     8023 b- defN 22-Jun-28 09:01 pyarmor-8.3.dev1/pyarmor/project.py
+-rw-r--r--  2.0 unx      140 b- defN 19-Dec-07 07:11 pyarmor-8.3.dev1/pyarmor/pyshield.key
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/platforms/linux/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/platforms/darwin/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/platforms/windows/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/platforms/linux/x86/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/platforms/linux/x86_64/
+-rwxr-xr-x  2.0 unx  1421600 b- defN 22-Sep-28 20:59 pyarmor-8.3.dev1/pyarmor/platforms/linux/x86/_pytransform.so
+-rwxr-xr-x  2.0 unx  1198080 b- defN 22-Sep-28 20:59 pyarmor-8.3.dev1/pyarmor/platforms/linux/x86_64/_pytransform.so
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/platforms/darwin/x86_64/
+-rwxr-xr-x  2.0 unx  1469620 b- defN 22-Sep-28 18:28 pyarmor-8.3.dev1/pyarmor/platforms/darwin/x86_64/_pytransform.dylib
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/platforms/windows/x86/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/platforms/windows/x86_64/
+-rw-r--r--  2.0 unx  1373710 b- defN 22-Sep-28 21:00 pyarmor-8.3.dev1/pyarmor/platforms/windows/x86/_pytransform.dll
+-rwxr-xr-x  2.0 unx  1165824 b- defN 22-Sep-28 20:59 pyarmor-8.3.dev1/pyarmor/platforms/windows/x86_64/_pytransform.dll
+-rw-r--r--  2.0 unx     6360 b- defN 22-Jul-14 19:38 pyarmor-8.3.dev1/pyarmor/plugins/README.md
+-rw-r--r--  2.0 unx    13688 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/plugins/check_ntp_time.py
+-rw-r--r--  2.0 unx     7036 b- defN 23-Jun-21 23:40 pyarmor-8.3.dev1/pyarmor/cli/bootstrap.py
+-rw-r--r--  2.0 unx     7184 b- defN 23-May-31 08:47 pyarmor-8.3.dev1/pyarmor/cli/merge.py
+-rw-r--r--  2.0 unx    10726 b- defN 23-May-31 08:18 pyarmor-8.3.dev1/pyarmor/cli/config.py
+-rw-r--r--  2.0 unx    18993 b- defN 23-Jul-23 15:37 pyarmor-8.3.dev1/pyarmor/cli/register.py
+-rw-r--r--  2.0 unx     5835 b- defN 23-May-22 18:36 pyarmor-8.3.dev1/pyarmor/cli/generate.py
+-rw-r--r--  2.0 unx     2193 b- defN 23-Feb-22 22:43 pyarmor-8.3.dev1/pyarmor/cli/shell.py
+-rw-r--r--  2.0 unx     7158 b- defN 23-May-07 11:39 pyarmor-8.3.dev1/pyarmor/cli/resource.py
+-rw-r--r--  2.0 unx     1526 b- defN 23-Jul-19 09:21 pyarmor-8.3.dev1/pyarmor/cli/__init__.py
+-rw-r--r--  2.0 unx     4594 b- defN 23-Jun-30 13:25 pyarmor-8.3.dev1/pyarmor/cli/docker.py
+-rw-r--r--  2.0 unx    19470 b- defN 23-Jul-20 10:16 pyarmor-8.3.dev1/pyarmor/cli/context.py
+-rw-r--r--  2.0 unx     3137 b- defN 23-Jun-25 16:00 pyarmor-8.3.dev1/pyarmor/cli/group.py
+-rw-r--r--  2.0 unx     7718 b- defN 23-Jun-09 14:11 pyarmor-8.3.dev1/pyarmor/cli/plugin.py
+-rw-r--r--  2.0 unx     3956 b- defN 23-Apr-20 15:02 pyarmor-8.3.dev1/pyarmor/cli/mixer.py
+-rw-r--r--  2.0 unx     2487 b- defN 23-Mar-26 06:51 pyarmor-8.3.dev1/pyarmor/cli/public_capsule.zip
+-rw-r--r--  2.0 unx     9133 b- defN 23-Jul-20 10:08 pyarmor-8.3.dev1/pyarmor/cli/default.cfg
+-rw-r--r--  2.0 unx    23065 b- defN 23-Jun-30 23:02 pyarmor-8.3.dev1/pyarmor/cli/__main__.py
+-rw-r--r--  2.0 unx    16099 b- defN 23-Jun-21 23:40 pyarmor-8.3.dev1/pyarmor/cli/repack.py
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/helloworld/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/simple/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/pybench/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/testpkg/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/testmod/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/py2exe/
+-rwxr-xr-x  2.0 unx     2048 b- defN 22-Mar-10 20:03 pyarmor-8.3.dev1/pyarmor/examples/obfuscate-pkg.bat
+-rwxr-xr-x  2.0 unx     1645 b- defN 22-Mar-10 20:03 pyarmor-8.3.dev1/pyarmor/examples/obfuscate-app.bat
+-rwxr-xr-x  2.0 unx     1103 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/examples/obfuscate-app.sh
+-rwxr-xr-x  2.0 unx     1685 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/examples/obfuscate-pkg.sh
+-rwxr-xr-x  2.0 unx     4102 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/examples/build-with-project.bat
+-rw-r--r--  2.0 unx     6876 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/examples/README.md
+-rwxr-xr-x  2.0 unx      773 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/examples/pack-obfuscated-scripts.sh
+-rwxr-xr-x  2.0 unx      928 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/examples/pack-obfuscated-scripts.bat
+-rwxr-xr-x  2.0 unx     3146 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/examples/build-with-project.sh
+-rwxr-xr-x  2.0 unx     4395 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/build-for-freeze.bat
+-rw-r--r--  2.0 unx     7078 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/examples/README-ZH.md
+-rwxr-xr-x  2.0 unx     4231 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/build-for-exe.bat
+-rw-r--r--  2.0 unx     1747 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/helloworld/foo.py
+-rwxr-xr-x  2.0 unx       49 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/hello.py
+-rwxr-xr-x  2.0 unx     2309 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/queens.py
+-rwxr-xr-x  2.0 unx      641 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/setup.py
+-rwxr-xr-x  2.0 unx     2309 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/simple/queens.py
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/pybench/package/
+-rwxr-xr-x  2.0 unx    13565 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Arithmetic.py
+-rwxr-xr-x  2.0 unx     4134 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/With.py
+-rwxr-xr-x  2.0 unx     6460 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Lists.py
+-rwxr-xr-x  2.0 unx     8034 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Tuples.py
+-rwxr-xr-x  2.0 unx     1388 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Instances.py
+-rwxr-xr-x  2.0 unx     6672 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/systimes.py
+-rwxr-xr-x  2.0 unx     1193 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/clockres.py
+-rwxr-xr-x  2.0 unx    15254 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Lookups.py
+-rwxr-xr-x  2.0 unx    16870 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/CommandLine.py
+-rwxr-xr-x  2.0 unx    16198 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Numbers.py
+-rwxr-xr-x  2.0 unx     2941 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Imports.py
+-rwxr-xr-x  2.0 unx      961 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Setup.py
+-rwxr-xr-x  2.0 unx    13400 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Exceptions.py
+-rwxr-xr-x  2.0 unx     9261 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Dict.py
+-rwxr-xr-x  2.0 unx    31828 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/pybench.py
+-rwxr-xr-x  2.0 unx     1561 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/NewInstances.py
+-rwxr-xr-x  2.0 unx     9252 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Calls.py
+-rwxr-xr-x  2.0 unx    10946 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Strings.py
+-rwxr-xr-x  2.0 unx    13207 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/Constructs.py
+-rwxr-xr-x  2.0 unx        0 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/package/__init__.py
+-rwxr-xr-x  2.0 unx        0 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/pybench/package/submodule.py
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor/examples/testpkg/mypkg/
+-rw-r--r--  2.0 unx       66 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/testpkg/main.py
+-rw-r--r--  2.0 unx      202 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/testpkg/mypkg/__init__.py
+-rw-r--r--  2.0 unx       45 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/testpkg/mypkg/foo.py
+-rwxr-xr-x  2.0 unx     1734 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/testmod/hello.py
+-rwxr-xr-x  2.0 unx     3694 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/testmod/queens.py
+-rwxr-xr-x  2.0 unx       44 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/py2exe/hello.py
+-rwxr-xr-x  2.0 unx     2309 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/py2exe/queens.py
+-rwxr-xr-x  2.0 unx     1081 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/examples/py2exe/setup.py
+-rw-r--r--  2.0 unx       28 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/polyfills/__init__.py
+-rwxr-xr-x  2.0 unx    88440 b- defN 19-Dec-05 18:38 pyarmor-8.3.dev1/pyarmor/polyfills/argparse.py
+-rw-r--r--  2.0 unx     1505 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/helper/superuntime.py
+-rw-r--r--  2.0 unx     9191 b- defN 22-Jan-06 22:40 pyarmor-8.3.dev1/pyarmor/helper/merge.py
+-rw-r--r--  2.0 unx    11618 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/helper/buildext.py
+-rw-r--r--  2.0 unx     2144 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/helper/get_platform_name.py
+-rw-r--r--  2.0 unx      778 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/helper/get_license_info.py
+-rw-r--r--  2.0 unx      728 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/helper/get_bind_key.py
+-rw-r--r--  2.0 unx        1 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/helper/__init__.py
+-rw-r--r--  2.0 unx     3821 b- defN 21-Oct-13 13:01 pyarmor-8.3.dev1/pyarmor/helper/build_data_module.py
+-rw-r--r--  2.0 unx    12719 b- defN 23-Mar-21 13:48 pyarmor-8.3.dev1/pyarmor/helper/repack.py
+-rw-r--r--  2.0 unx     3004 b- defN 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor.egg-info/PKG-INFO
+-rw-r--r--  2.0 unx     3450 b- defN 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor.egg-info/SOURCES.txt
+-rw-r--r--  2.0 unx      174 b- defN 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor.egg-info/entry_points.txt
+-rw-r--r--  2.0 unx       27 b- defN 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor.egg-info/requires.txt
+-rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor.egg-info/top_level.txt
+-rw-r--r--  2.0 unx        1 b- defN 23-Jul-23 20:58 pyarmor-8.3.dev1/pyarmor.egg-info/dependency_links.txt
+143 files, 7442858 bytes uncompressed, 2306968 bytes compressed:  69.0%
```

## zipnote {}

```diff
@@ -1,412 +1,430 @@
-Filename: pyarmor-8.2.dev2/
+Filename: pyarmor-8.3.dev1/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/pyarmor.egg-info/
+Filename: pyarmor-8.3.dev1/pyarmor/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/
+Filename: pyarmor-8.3.dev1/pyarmor.egg-info/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/PKG-INFO
+Filename: pyarmor-8.3.dev1/PKG-INFO
 Comment: 
 
-Filename: pyarmor-8.2.dev2/MANIFEST.in
+Filename: pyarmor-8.3.dev1/MANIFEST.in
 Comment: 
 
-Filename: pyarmor-8.2.dev2/README.md
+Filename: pyarmor-8.3.dev1/README.md
 Comment: 
 
-Filename: pyarmor-8.2.dev2/setup.py
+Filename: pyarmor-8.3.dev1/setup.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/setup.cfg
+Filename: pyarmor-8.3.dev1/setup.cfg
 Comment: 
 
-Filename: pyarmor-8.2.dev2/pyarmor.egg-info/PKG-INFO
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/pyarmor.egg-info/SOURCES.txt
+Filename: pyarmor-8.3.dev1/pyarmor/plugins/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/pyarmor.egg-info/entry_points.txt
+Filename: pyarmor-8.3.dev1/pyarmor/cli/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/pyarmor.egg-info/requires.txt
+Filename: pyarmor-8.3.dev1/pyarmor/examples/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/pyarmor.egg-info/top_level.txt
+Filename: pyarmor-8.3.dev1/pyarmor/polyfills/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/pyarmor.egg-info/dependency_links.txt
+Filename: pyarmor-8.3.dev1/pyarmor/helper/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/
+Filename: pyarmor-8.3.dev1/pyarmor/pyshield.lic
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/plugins/
+Filename: pyarmor-8.3.dev1/pyarmor/config.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/
+Filename: pyarmor-8.3.dev1/pyarmor/benchmark.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/
+Filename: pyarmor-8.3.dev1/pyarmor/register.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/polyfills/
+Filename: pyarmor-8.3.dev1/pyarmor/product.key
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/
+Filename: pyarmor-8.3.dev1/pyarmor/pyarmor.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/pyshield.lic
+Filename: pyarmor-8.3.dev1/pyarmor/protect_code.pt
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/config.py
+Filename: pyarmor-8.3.dev1/pyarmor/pytransform.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/benchmark.py
+Filename: pyarmor-8.3.dev1/pyarmor/sppmode.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/register.py
+Filename: pyarmor-8.3.dev1/pyarmor/public.key
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/product.key
+Filename: pyarmor-8.3.dev1/pyarmor/__init__.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/pyarmor.py
+Filename: pyarmor-8.3.dev1/pyarmor/reform.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/protect_code.pt
+Filename: pyarmor-8.3.dev1/pyarmor/packer.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/pytransform.py
+Filename: pyarmor-8.3.dev1/pyarmor/cobuilder.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/sppmode.py
+Filename: pyarmor-8.3.dev1/pyarmor/utils.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/public.key
+Filename: pyarmor-8.3.dev1/pyarmor/pyarmor-webui.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/__init__.py
+Filename: pyarmor-8.3.dev1/pyarmor/pyarmor-deprecated.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/reform.py
+Filename: pyarmor-8.3.dev1/pyarmor/build_meta.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/packer.py
+Filename: pyarmor-8.3.dev1/pyarmor/license.tri
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cobuilder.py
+Filename: pyarmor-8.3.dev1/pyarmor/README.rst
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/utils.py
+Filename: pyarmor-8.3.dev1/pyarmor/protect_code2.pt
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/pyarmor-webui.py
+Filename: pyarmor-8.3.dev1/pyarmor/pyimcore.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/build_meta.py
+Filename: pyarmor-8.3.dev1/pyarmor/public_capsule.zip
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/license.tri
+Filename: pyarmor-8.3.dev1/pyarmor/project.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/README.rst
+Filename: pyarmor-8.3.dev1/pyarmor/pyshield.key
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/protect_code2.pt
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/linux/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/public_capsule.zip
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/darwin/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/project.py
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/windows/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/pyshield.key
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/linux/x86/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/linux/
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/linux/x86_64/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/darwin/
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/linux/x86/_pytransform.so
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/windows/
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/linux/x86_64/_pytransform.so
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/linux/x86/
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/darwin/x86_64/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/linux/x86_64/
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/darwin/x86_64/_pytransform.dylib
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/linux/x86/_pytransform.so
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/windows/x86/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/linux/x86_64/_pytransform.so
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/windows/x86_64/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/darwin/x86_64/
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/windows/x86/_pytransform.dll
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/darwin/x86_64/_pytransform.dylib
+Filename: pyarmor-8.3.dev1/pyarmor/platforms/windows/x86_64/_pytransform.dll
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/windows/x86/
+Filename: pyarmor-8.3.dev1/pyarmor/plugins/README.md
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/windows/x86_64/
+Filename: pyarmor-8.3.dev1/pyarmor/plugins/check_ntp_time.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/windows/x86/_pytransform.dll
+Filename: pyarmor-8.3.dev1/pyarmor/cli/bootstrap.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/platforms/windows/x86_64/_pytransform.dll
+Filename: pyarmor-8.3.dev1/pyarmor/cli/merge.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/plugins/README.md
+Filename: pyarmor-8.3.dev1/pyarmor/cli/config.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/plugins/check_ntp_time.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/register.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/config.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/generate.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/register.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/shell.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/generate.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/resource.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/shell.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/__init__.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/resource.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/docker.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/__init__.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/context.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/context.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/group.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/plugin.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/plugin.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/mixer.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/mixer.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/public_capsule.zip
+Filename: pyarmor-8.3.dev1/pyarmor/cli/public_capsule.zip
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/default.cfg
+Filename: pyarmor-8.3.dev1/pyarmor/cli/default.cfg
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/__main__.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/__main__.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/cli/repack.py
+Filename: pyarmor-8.3.dev1/pyarmor/cli/repack.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/helloworld/
+Filename: pyarmor-8.3.dev1/pyarmor/examples/helloworld/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/cx_Freeze/
+Filename: pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/simple/
+Filename: pyarmor-8.3.dev1/pyarmor/examples/simple/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/testpkg/
+Filename: pyarmor-8.3.dev1/pyarmor/examples/testpkg/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/testmod/
+Filename: pyarmor-8.3.dev1/pyarmor/examples/testmod/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/py2exe/
+Filename: pyarmor-8.3.dev1/pyarmor/examples/py2exe/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/obfuscate-pkg.bat
+Filename: pyarmor-8.3.dev1/pyarmor/examples/obfuscate-pkg.bat
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/obfuscate-app.bat
+Filename: pyarmor-8.3.dev1/pyarmor/examples/obfuscate-app.bat
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/obfuscate-app.sh
+Filename: pyarmor-8.3.dev1/pyarmor/examples/obfuscate-app.sh
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/obfuscate-pkg.sh
+Filename: pyarmor-8.3.dev1/pyarmor/examples/obfuscate-pkg.sh
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/build-with-project.bat
+Filename: pyarmor-8.3.dev1/pyarmor/examples/build-with-project.bat
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/README.md
+Filename: pyarmor-8.3.dev1/pyarmor/examples/README.md
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pack-obfuscated-scripts.sh
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pack-obfuscated-scripts.sh
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pack-obfuscated-scripts.bat
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pack-obfuscated-scripts.bat
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/build-with-project.sh
+Filename: pyarmor-8.3.dev1/pyarmor/examples/build-with-project.sh
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/build-for-freeze.bat
+Filename: pyarmor-8.3.dev1/pyarmor/examples/build-for-freeze.bat
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/README-ZH.md
+Filename: pyarmor-8.3.dev1/pyarmor/examples/README-ZH.md
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/build-for-exe.bat
+Filename: pyarmor-8.3.dev1/pyarmor/examples/build-for-exe.bat
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/helloworld/foo.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/helloworld/foo.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/cx_Freeze/hello.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/hello.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/cx_Freeze/queens.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/queens.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/cx_Freeze/setup.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/setup.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/simple/queens.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/simple/queens.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/package/
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/package/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Arithmetic.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Arithmetic.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/With.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/With.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Lists.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Lists.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Tuples.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Tuples.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Instances.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Instances.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/systimes.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/systimes.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/clockres.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/clockres.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Lookups.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Lookups.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/CommandLine.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/CommandLine.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Numbers.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Numbers.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Imports.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Imports.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Setup.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Setup.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Exceptions.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Exceptions.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Dict.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Dict.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/pybench.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/pybench.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/NewInstances.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/NewInstances.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Calls.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Calls.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Strings.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Strings.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/Constructs.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/Constructs.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/package/__init__.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/package/__init__.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/pybench/package/submodule.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/pybench/package/submodule.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/testpkg/mypkg/
+Filename: pyarmor-8.3.dev1/pyarmor/examples/testpkg/mypkg/
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/testpkg/main.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/testpkg/main.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/testpkg/mypkg/__init__.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/testpkg/mypkg/__init__.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/testpkg/mypkg/foo.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/testpkg/mypkg/foo.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/testmod/hello.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/testmod/hello.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/testmod/queens.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/testmod/queens.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/py2exe/hello.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/py2exe/hello.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/py2exe/queens.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/py2exe/queens.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/examples/py2exe/setup.py
+Filename: pyarmor-8.3.dev1/pyarmor/examples/py2exe/setup.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/polyfills/__init__.py
+Filename: pyarmor-8.3.dev1/pyarmor/polyfills/__init__.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/polyfills/argparse.py
+Filename: pyarmor-8.3.dev1/pyarmor/polyfills/argparse.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/superuntime.py
+Filename: pyarmor-8.3.dev1/pyarmor/helper/superuntime.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/merge.py
+Filename: pyarmor-8.3.dev1/pyarmor/helper/merge.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/buildext.py
+Filename: pyarmor-8.3.dev1/pyarmor/helper/buildext.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/get_platform_name.py
+Filename: pyarmor-8.3.dev1/pyarmor/helper/get_platform_name.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/get_license_info.py
+Filename: pyarmor-8.3.dev1/pyarmor/helper/get_license_info.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/get_bind_key.py
+Filename: pyarmor-8.3.dev1/pyarmor/helper/get_bind_key.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/__init__.py
+Filename: pyarmor-8.3.dev1/pyarmor/helper/__init__.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/build_data_module.py
+Filename: pyarmor-8.3.dev1/pyarmor/helper/build_data_module.py
 Comment: 
 
-Filename: pyarmor-8.2.dev2/src/helper/repack.py
+Filename: pyarmor-8.3.dev1/pyarmor/helper/repack.py
+Comment: 
+
+Filename: pyarmor-8.3.dev1/pyarmor.egg-info/PKG-INFO
+Comment: 
+
+Filename: pyarmor-8.3.dev1/pyarmor.egg-info/SOURCES.txt
+Comment: 
+
+Filename: pyarmor-8.3.dev1/pyarmor.egg-info/entry_points.txt
+Comment: 
+
+Filename: pyarmor-8.3.dev1/pyarmor.egg-info/requires.txt
+Comment: 
+
+Filename: pyarmor-8.3.dev1/pyarmor.egg-info/top_level.txt
+Comment: 
+
+Filename: pyarmor-8.3.dev1/pyarmor.egg-info/dependency_links.txt
 Comment: 
 
 Zip file comment:
```

## Comparing `pyarmor-8.2.dev2/PKG-INFO` & `pyarmor-8.3.dev1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.1
 Name: pyarmor
-Version: 8.2.dev2
+Version: 8.3.dev1
 Summary: A tool used to obfuscate python scripts, bind obfuscated scripts to fixed machine or expire obfuscated scripts.
 Home-page: https://github.com/dashingsoft/pyarmor
 Author: Jondy Zhao
 Author-email: pyarmor@163.com
 License: Free To Use But Restricted
 Description: Protect Python Scripts By Pyarmor
         =================================
```

## Comparing `pyarmor-8.2.dev2/README.md` & `pyarmor-8.3.dev1/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -58,15 +58,15 @@
 
 Pyarmor is published as shareware. The free trial version never expires, but has some limitations.
 
 Refer to [Pyarmor licenses][licenses] for information on license types, features, limitations, and purchasing a Pyarmor license.
 
 Please read the [Pyarmor EULA](LICENSE).
 
-[licenses]: https://pyarmor.readthedocs.io/en/stable/licenses.html
+[licenses]: https://pyarmor.readthedocs.io/en/latest/licenses.html
 
 ## Getting Help
 
 1. **Consult the [Pyarmor 8.0 Documentation][doc].**
 2. **Check the [FAQ][faq] for answers to common questions.**
 3. **Try the documentation [index][genindex] or the [detailed table of contents][mastertoc].**
 4. **If you still can't find the information you need, see [asking questions on GitHub][asking].**
@@ -74,15 +74,15 @@
 6. **For business and security inquiries, send an email to <pyarmor@163.com>.**
 
 [faq]: https://pyarmor.readthedocs.io/en/stable/questions.html
 [issues]: https://github.com/dashingsoft/pyarmor/issues
 [genindex]: https://pyarmor.readthedocs.io/en/stable/genindex.html
 [mastertoc]: https://pyarmor.readthedocs.io/en/stable/index.html#table-of-contents
 [asking]: https://pyarmor.readthedocs.io/en/stable/questions.html#asking-questions-in-github
-[doc]: https://pyarmor.readthedocs.io/en/stable/
+[doc]: https://pyarmor.readthedocs.io/
 
 ## Resources
 
 * [Website](https://pyarmor.dashingsoft.com)
 * [Documentation 8.0][doc]
 * [Documentation 7.x](https://pyarmor.readthedocs.io/en/v7.7/)
 
@@ -93,33 +93,27 @@
 * [Pyarmor 7.x 在线文档](https://pyarmor.readthedocs.io/zh/v7.x/)
 
 ## Changelog
 
 Pyarmor 8.0 introduces significant changes. It has been rewritten and new features are implemented through the new commands:
 `gen`, `reg`, `cfg`. These commands only work for Python 3.7 and above.
 
-### Initial Release Support (2023-03-08)
-
-- **Supported Architectures**: x86_64
-- **Supported Platforms**: Windows, Linux, and macOS
-
-### Upcoming Support
-
-- **aarch64 for Linux and macOS**: Before 2023-04-01
-- **armv7 and x86 without bcc mode**: Around 2023-04-10
-- **Other architectures**: On request
-
 Users of versions prior to 8.0 should read the [Import Notes][important-notes] section to decide whether to upgrade Pyarmor.
 
-Each major version comes with a separate changelog file, detailing fixed issues, new features, and compatibility
-issues between different versions.
+Each major version comes with a separate changelog file, detailing fixed issues, new features, and compatibility issues between different versions.
 
 Make sure to read the changelog carefully before upgrading Pyarmor:
 - [Pyarmor 8.x Changelog](docs/ChangeLogs.8)
 
+**Full changelogs** at [releases](releases)
+
+**Upcoming features** at [Pyarmor 8.x Release Plan](ReleasePlan.md)
+
+[releases]: https://github.com/dashingsoft/pyarmor/releases
+
 [important-notes]: #important-notes-for-users-of-pyarmor-prior-to-80
 
 ## Important Notes for Users of Pyarmor Prior to 8.0
 
 Going forward, only bug fixes will be provided for older commands, such as `obfuscate` and `licenses`.
 No new features will be added to these commands, but they will continue to be usable.
```

## Comparing `pyarmor-8.2.dev2/setup.py` & `pyarmor-8.3.dev1/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -102,25 +102,26 @@
     # This field adds keywords for your project which will appear on the
     # project page. What does your project relate to?
     #
     # Note that this is a string of words separated by whitespace, not a list.
     keywords='protect obfuscate encrypt obfuscation distribute',
 
     packages=['pyarmor', 'pyarmor.polyfills', 'pyarmor.helper', 'pyarmor.cli'],
-    package_dir={'pyarmor': 'src'},
+    package_dir={'pyarmor': 'pyarmor'},
     package_data={
         'pyarmor': pyarmor_data_files + platform_data_files,
         'pyarmor.cli': ['default.cfg', 'public_capsule.zip'],
     },
 
     install_requires=[
-        'pyarmor.cli.core~=3.2.dev2'
+        'pyarmor.cli.core~=4.3.dev1'
     ],
 
     entry_points={
         'console_scripts': [
             'pyarmor=pyarmor.pyarmor:main_entry_8',
+            'pyarmor-auth=pyarmor.cli.docker:main',
             'pyarmor-7=pyarmor.pyarmor:main_entry',
             'pyarmor-8=pyarmor.cli.__main__:main',
         ],
     },
 )
```

## Comparing `pyarmor-8.2.dev2/pyarmor.egg-info/PKG-INFO` & `pyarmor-8.3.dev1/pyarmor.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.1
 Name: pyarmor
-Version: 8.2.dev2
+Version: 8.3.dev1
 Summary: A tool used to obfuscate python scripts, bind obfuscated scripts to fixed machine or expire obfuscated scripts.
 Home-page: https://github.com/dashingsoft/pyarmor
 Author: Jondy Zhao
 Author-email: pyarmor@163.com
 License: Free To Use But Restricted
 Description: Protect Python Scripts By Pyarmor
         =================================
```

## Comparing `pyarmor-8.2.dev2/src/config.py` & `pyarmor-8.3.dev1/pyarmor/config.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from sys import platform
 
-version = '8.2.dev2'
+version = '8.3.dev1'
 
 # The corresponding version of pytransform.so
 core_version = 'r52.6'
 
 version_info = '''
 PyArmor is a command line tool used to obfuscate python scripts, bind
 obfuscated scripts to fixed machine or expire obfuscated scripts.
```

## Comparing `pyarmor-8.2.dev2/src/benchmark.py` & `pyarmor-8.3.dev1/pyarmor/benchmark.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/register.py` & `pyarmor-8.3.dev1/pyarmor/register.py`

 * *Files 3% similar despite different names*

```diff
@@ -53,19 +53,15 @@
     except Exception as e:
         note = 'Note: sometimes remote server is busy, please try it later'
         return '\nError: %s\n%s' % (str(e), note)
 
     name = data['name']
     email = data['email']
     if name and email:
-        return 'This code is authorized to "%s <%s>"\n\n' \
-            'Note: the registration name and email got from ' \
-            'remote server is shown here only, they will not be used ' \
-            'anywhere else. But the code "%s" will be distributed ' \
-            'with obfusated scripts.' % (name, email, key)
+        return 'License to: "%s <%s>"' % (name, email)
 
     if 'error' in data:
         return '\nError: %s' % data['error']
 
     return '\nError: this code may NOT be issued by PyArmor officially.' \
         '\nPlease contact <pyarmor@163.com>'
```

## Comparing `pyarmor-8.2.dev2/src/pyarmor.py` & `pyarmor-8.3.dev1/pyarmor/pyarmor.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/protect_code.pt` & `pyarmor-8.3.dev1/pyarmor/protect_code.pt`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/pytransform.py` & `pyarmor-8.3.dev1/pyarmor/pytransform.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/sppmode.py` & `pyarmor-8.3.dev1/pyarmor/sppmode.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/reform.py` & `pyarmor-8.3.dev1/pyarmor/reform.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/packer.py` & `pyarmor-8.3.dev1/pyarmor/packer.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/cobuilder.py` & `pyarmor-8.3.dev1/pyarmor/cobuilder.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/utils.py` & `pyarmor-8.3.dev1/pyarmor/utils.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/build_meta.py` & `pyarmor-8.3.dev1/pyarmor/build_meta.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/README.rst` & `pyarmor-8.3.dev1/pyarmor/README.rst`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/protect_code2.pt` & `pyarmor-8.3.dev1/pyarmor/protect_code2.pt`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/public_capsule.zip` & `pyarmor-8.3.dev1/pyarmor/public_capsule.zip`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/project.py` & `pyarmor-8.3.dev1/pyarmor/project.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/platforms/linux/x86/_pytransform.so` & `pyarmor-8.3.dev1/pyarmor/platforms/linux/x86/_pytransform.so`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/platforms/linux/x86_64/_pytransform.so` & `pyarmor-8.3.dev1/pyarmor/platforms/linux/x86_64/_pytransform.so`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/platforms/darwin/x86_64/_pytransform.dylib` & `pyarmor-8.3.dev1/pyarmor/platforms/darwin/x86_64/_pytransform.dylib`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/platforms/windows/x86/_pytransform.dll` & `pyarmor-8.3.dev1/pyarmor/platforms/windows/x86/_pytransform.dll`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/platforms/windows/x86_64/_pytransform.dll` & `pyarmor-8.3.dev1/pyarmor/platforms/windows/x86_64/_pytransform.dll`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/plugins/README.md` & `pyarmor-8.3.dev1/pyarmor/plugins/README.md`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/plugins/check_ntp_time.py` & `pyarmor-8.3.dev1/pyarmor/plugins/check_ntp_time.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/cli/config.py` & `pyarmor-8.3.dev1/pyarmor/cli/config.py`

 * *Files 2% similar despite different names*

```diff
@@ -147,15 +147,17 @@
             optvalue = optvalue.strip(optvalue[0])
 
         if not optvalue:
             if op is None:
                 self._clear(sect, optname, local, name)
             return
 
-        old = cfg[sect].get(optname, '') if cfg.has_section(sect) else ''
+        ctxcfg = ctx.cfg
+        old = ctxcfg[sect].get(optname, '') if ctxcfg.has_section(sect) else ''
+
         if op == '+':
             if (optvalue + ' ').find(old + ' ') == -1:
                 optvalue = ('%s %s' % (old, optvalue)).strip()
         elif op == '-':
             optvalue = (old + ' ').replace(optvalue + ' ', '').strip()
         elif op == '^':
             optvalue = '\n'.join((old.splitlines() + [optvalue]))
```

## Comparing `pyarmor-8.2.dev2/src/cli/register.py` & `pyarmor-8.3.dev1/pyarmor/cli/register.py`

 * *Files 4% similar despite different names*

```diff
@@ -149,39 +149,78 @@
         path = self.ctx.reg_path
         with ZipFile(regfile, 'r') as f:
             for item in ('license.lic', '.pyarmor_capsule.zip'):
                 logger.debug('extracting %s', item)
                 f.extract(item, path=path)
             namelist = f.namelist()
             if 'group.tokens' in namelist:
-                machid = self._get_machine_id()
-                name = '/'.join(['tokens', machid.decode('utf-8')])
+                machid = self._get_machine_id().decode('utf-8')
+                name = '/'.join(['tokens', machid])
                 if name not in namelist:
-                    logger.debug('no found "%s" in offline regfile', name)
-                    raise CliError('this regfile is not for this device')
+                    machid = self._get_docker_hostname()
+                    if not machid:
+                        raise CliError('could not get docker host machine id')
+                    hostname = '/'.join(['tokens', machid])
+                    if hostname not in namelist:
+                        logger.debug('no found "%s" in offline regfile', name)
+                        raise CliError('this regfile is not for this device')
+                    name = hostname
                 logger.debug('extracting %s', name)
                 self.ctx.save_token(f.read(name))
                 return
             if 'group.info' in namelist:
                 raise CliError('wrong usage for group license, please '
                                'check `pyarmor reg` in Man page')
 
         logger.info('update license token')
         self.update_token()
 
-    def _get_machine_id(self):
+    def _get_docker_hostname(self):
+        try:
+            from socket import socket, AF_INET, SOCK_STREAM
+            host = 'host.docker.internal'
+            port = 29092
+            with socket(AF_INET, SOCK_STREAM) as s:
+                s.connect((host, port))
+                s.sendall(b'PADH' + b'x' * 60)
+                flag = s.recv(1)
+                if flag in (b'a', b'b'):
+                    data = s.recv(32)
+                machid = (flag + data).decode('utf-8')
+                logger.info('got docker host machine id: %s', machid)
+                return machid
+        except Exception:
+            logger.exception('could not get docker host machine id')
+
+    def _get_machine_id(self, idver=11):
         from .core import Pytransform3
-        return Pytransform3.get_hd_info(10)
+        return Pytransform3.get_hd_info(idver)
 
     def generate_group_device(self, devid):
+        from datetime import datetime
+        from platform import uname
         path = self.ctx.group_device_file(devid)
         logger.info('generating device file "%s"', path)
         os.makedirs(os.path.dirname(path), exist_ok=True)
+        uinfo = uname()
+        tpl = Template('\n'.join([
+            '# Generated by Pyarmor $rev, $timestamp',
+            'host: $node',
+            'system: $host ($version)',
+            'machine: $machine'
+        ])).substitute(
+            rev='.'.join(self.ctx.version),
+            node=uinfo.node,
+            host=uinfo.system,
+            version=uinfo.version,
+            timestamp=datetime.now().isoformat(),
+            machine=self._get_machine_id(16).decode('utf-8')
+        )
         with open(path, "wb") as f:
-            f.write(b'machine: ' + self._get_machine_id())
+            f.write(tpl.encode('utf-8'))
         return path
 
     def __str__(self):
         '''$advanced
 
 Notes
 $notes
@@ -260,15 +299,15 @@
             os.remove(self.ctx.license_token)
 
     def prepare(self, keyfile, product, upgrade=False):
         reginfo = self.parse_keyfile(keyfile)
         logger.info('prepare "%s"', keyfile)
 
         rcode = self._get_old_rcode() if upgrade else None
-        if upgrade and keyfile.endswith('regcode-to-pro.txt'):
+        if upgrade and not rcode and keyfile.endswith('regcode-to-pro.txt'):
             logger.error('please use `pyarmor-7 -v` to check old license')
             logger.error('this code is used to upgrade old license')
             raise CliError('no found old license in this machine')
         url = self.regurl(reginfo[1], rcode=rcode, prepare=True)
         logger.debug('url: %s', url)
 
         logger.info('query key file from server')
@@ -286,17 +325,17 @@
             info['product'] = product
         elif pname != product:
             logger.warning('this license is bind to product "%s"', pname)
             logger.warning('it can not be changed to "%s"', product)
 
         lines = []
         if upgrade:
-            if not (rcode and rcode.startswith('pyarmor-vax-')):
-                logger.error('please check Pyarmor 8.0 EULA')
-                raise CliError('old code "%s" can not be upgraded' % rcode)
+            if rcode and not rcode.startswith('pyarmor-vax-'):
+                logger.error('please check Pyarmor 8 EULA')
+                raise CliError('old license "%s" can not be upgraded' % rcode)
             if info['upgrade']:
                 lines.append(upgrade_to_pro_info.substitute(rcode=rcode))
             else:
                 lines.append(upgrade_to_basic_info.substitute())
         else:
             if info['lictype'] not in ('BASIC', 'PRO', 'GROUP'):
                 logger.error('this license does not work in Pyarmor 8')
```

## Comparing `pyarmor-8.2.dev2/src/cli/generate.py` & `pyarmor-8.3.dev1/pyarmor/cli/generate.py`

 * *Files 8% similar despite different names*

```diff
@@ -28,45 +28,53 @@
 
 
 class Finder(object):
 
     def __init__(self, ctx):
         self.ctx = ctx
 
-    def prepare(self, input_paths):
+    def _build_resource(self, pathlist):
         resources = []
-        for path in input_paths:
+        for path in pathlist:
             if not os.path.exists(path):
                 raise CliError('argument "%s" doesn\'t exists' % path)
             if os.path.isfile(path):
                 logger.info('find script %s', path)
                 res = FileResource(path)
                 resources.append(res)
             else:
                 logger.info('find package at %s', path)
                 res = PathResource(path)
                 resources.append(res)
                 options = self.ctx.get_res_options(res.fullname)
                 res.rebuild(**options)
-        self.ctx.resources = resources
+        return resources
+
+    def prepare(self, input_paths):
+        self.ctx.resources = self._build_resource(input_paths)
+
+    def process_extra(self, contents):
+        extra_paths = [x for x in contents if x.endswith('.pyc')]
+        for pyz in [x for x in contents if x.endswith('.pyz_extracted')]:
+            extra_paths.extend([os.path.join(pyz, x) for x in os.listdir(pyz)])
+        resnames = [x.pkgname for x in self.ctx.resources]
+        for res in self._build_resource(extra_paths):
+            if res.pkgname not in resnames:
+                self.ctx.obfuscated_modules.add(res.pkgname)
+                self.ctx.extra_resources.append(res)
 
-    def process(self, pack=None):
+    def process(self):
         logger.info('search inputs ...')
         self.prepare(self.ctx.input_paths)
         logger.info('find %d top resources', len(self.ctx.resources))
 
         modules = [x.fullname for res in self.ctx.resources for x in res
                    if x.is_script()]
         self.ctx.obfuscated_modules.update(modules)
 
-        # TBD: implement it in next Release
-        # if pack:
-        #     from .repack import list_modules
-        #     self.ctx.obfuscated_modules.update(list_modules(pack))
-
 
 class Builder(object):
 
     def __init__(self, ctx):
         self.ctx = ctx
 
     def format_output(self, outputs, count=0):
@@ -80,29 +88,23 @@
         return Pytransform3.generate_runtime_key(self.ctx, outer)
 
     def generate_runtime_package(self, output):
         if self.ctx.runtime_key is None:
             self.ctx.runtime_key = self.generate_runtime_key()
         Pytransform3.generate_runtime_package(self.ctx, output)
 
-    def _pack_script(self, bundle, output, entry=None, codesign=None):
-        from .repack import repacker
-        buildpath = os.path.join('.pyarmor', 'pack')
-        repacker(bundle, output, buildpath, entry=entry, codesign=codesign)
-        shutil.rmtree(buildpath)
-
     def _obfuscate_scripts(self):
         rev = self.ctx.version_info()
         template = self.ctx.bootstrap_template
         relative = self.ctx.import_prefix
         pkgname = self.ctx.runtime_package_name
         bootpath = self.ctx.cfg.get('builder', 'bootstrap_file')
 
         namelist = []
-        for res in self.ctx.resources:
+        for res in self.ctx.resources + self.ctx.extra_resources:
             logger.info('process resource "%s"', res.fullname)
             name = res.name
             path = self.format_output(self.ctx.outputs, namelist.count(name))
             namelist.append(name)
             os.makedirs(path, exist_ok=True)
 
             for r in res:
@@ -123,36 +125,38 @@
                 fullpath = os.path.join(path, r.output_filename)
                 os.makedirs(os.path.dirname(fullpath), exist_ok=True)
 
                 logger.info('write %s', fullpath)
                 with open(fullpath, 'w') as f:
                     f.write(source)
 
-    def process(self, options, pack=None):
+    def process(self, options, packer=None):
         for opt in options['inputs']:
             if not os.path.exists(opt):
                 raise CliError('no found input "%s"' % opt)
         self.ctx.input_paths = options['inputs']
 
         output = options.get('output', 'dist')
         self.ctx.outputs = output.split(',')
 
         finder = Finder(self.ctx)
-        finder.process(pack=pack)
+        finder.process()
+
+        if packer and options.get('self_contained'):
+            finder.process_extra(packer.contents)
 
         Pytransform3.pre_build(self.ctx)
 
         self.ctx.runtime_key = self.generate_runtime_key()
-
         if not options.get('no_runtime'):
             logger.info('start to generate runtime files')
             self.generate_runtime_package(self.ctx.outputs[0])
             logger.info('generate runtime files OK')
 
         logger.info('start to obfuscate scripts')
         self._obfuscate_scripts()
         logger.info('obfuscate scripts OK')
 
         Pytransform3.post_build(self.ctx)
 
-        if pack:
-            self._pack_script(pack, output)
+        if packer:
+            packer.repack(output, self.ctx.runtime_package_name)
```

## Comparing `pyarmor-8.2.dev2/src/cli/shell.py` & `pyarmor-8.3.dev1/pyarmor/cli/shell.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/cli/resource.py` & `pyarmor-8.3.dev1/pyarmor/cli/resource.py`

 * *Files 6% similar despite different names*

```diff
@@ -40,15 +40,15 @@
     def _format_name(self, path):
         return os.path.splitext(os.path.basename(path))[0]
 
     def is_top(self):
         return self.parent is None
 
     def is_script(self):
-        return isinstance(self, FileResource)
+        return isinstance(self, (FileResource, PycResource))
 
     @property
     def fullname(self):
         return self.name if self.is_top() else \
             '.'.join([self.parent.fullname, self.name])
 
     @property
@@ -96,28 +96,40 @@
         return self.fullname.replace('.', os.path.sep) + self.pyext
 
     @property
     def frozenname(self):
         n = self.fullname.find('.__init__')
         return '<frozen %s>' % self.fullname[:None if n == -1 else n]
 
+    @property
+    def is_pyc(self):
+        return self.pyext.lower() == '.pyc'
+
     def readlines(self, encoding=None):
         if not os.path.exists(self.fullpath):
             raise RuntimeError('file "%s" doesn\'t exists' % self.fullpath)
 
         with open(self.fullpath, encoding=encoding) as f:
             # file.read() can't read the whole data of big files
             return f.readlines()
 
     def reparse(self, lines=None, encoding=None):
         if lines is None:
             lines = self.readlines(encoding=encoding)
         self.mtree = ast.parse(''.join(lines), self.frozenname, 'exec')
 
+    def _recompile_pyc(self):
+        from importlib._bootstrap_external import SourcelessFileLoader
+        path, name = self.fullpath, self.pkgname
+        self.mco = SourcelessFileLoader(name, path).get_code(name)
+
     def recompile(self, mtree=None, optimize=1):
+        if self.is_pyc:
+            return self._recompile_pyc()
+
         if mtree is None:
             mtree = self.mtree
         assert mtree is not None
         self.mco = compile(mtree, self.frozenname, 'exec', optimize=optimize)
 
     def clean(self):
         self.lines = None
@@ -135,23 +147,33 @@
         elif relative == 1:
             prefix = '.' * self.fullname.count('.')
         else:
             assert(isinstance(relative, str))
             prefix = relative + '.'
             if self.fullname.startswith(prefix):
                 prefix = '.' * self.fullname.count('.')
+            elif prefix.startswith(self.pkgname + '.'):
+                prefix = prefix[len(self.pkgname):]
 
         return Template(tpl).safe_substitute(
             timestamp=datetime.now().isoformat(),
             package=prefix + pkgname,
             path=bootpath,
             code=repr(code),
             rev=rev)
 
 
+class PycResource(FileResource):
+
+    def recompile(self, mtree=None, optimize=1):
+        from importlib._bootstrap_external import SourcelessFileLoader
+        path, name = self.fullpath, self.pkgname
+        self.mco = SourcelessFileLoader(name, path).get_code(name)
+
+
 class PathResource(Resource):
 
     def __init__(self, path, name=None, parent=None):
         super().__init__(path, name=name, parent=parent)
         self.respaths = []
         self.resfiles = []
```

## Comparing `pyarmor-8.2.dev2/src/cli/__init__.py` & `pyarmor-8.3.dev1/pyarmor/cli/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import logging
 
-__VERSION__ = '8.2'
+__VERSION__ = '8.3.dev1'
 
 logger = logging.getLogger('cli')
 
 
 class CliError(Exception):
     pass
 
@@ -20,14 +20,15 @@
 
 class Component(object):
 
     trace_loggers = {
         'StrProtector': 'trace.mix.str',
         'CallProtector': 'trace.assert.call',
         'ImportProtector': 'trace.assert.import',
+        'AttrProtector': 'trace.co.attr',
         'CodeProtector': 'trace.co',
         'CoPatcher': 'trace.co',
         'BccPatcher': 'trace.bcc',
     }
 
     def __init__(self, ctx):
         self.ctx = ctx
```

## Comparing `pyarmor-8.2.dev2/src/cli/context.py` & `pyarmor-8.3.dev1/pyarmor/cli/context.py`

 * *Files 15% similar despite different names*

```diff
@@ -28,26 +28,71 @@
 __pyarmor__(__name__, $path, $code)
 '''
 
 runtime_package_template = '''# Pyarmor $rev, $timestamp
 from .pyarmor_runtime import __pyarmor__
 '''
 
-runtime_package_template2 = '''# Pyarmor $rev, $timestamp
-for suffix in '', '_a1', '_a2', '_a3':
-    try:
-        __pyarmor__ = __import__('pyarmor_runtime' + suffix,
-                                 globals(), locals(),
-                                 ('__pyarmor__',),
-                                 0).__pyarmor__
-        break
-    except ModuleNotFoundError:
-        pass
-else:
-    raise ModuleNotFoundError('no pyarmor_runtime extension found')
+multi_runtime_package_template = '''# Pyarmor $rev, $timestamp
+def __pyarmor__():
+    import platform
+    import sys
+    from struct import calcsize
+
+    def format_system():
+        plat = platform.system().lower()
+        plat = ('windows' if plat.startswith('cygwin') else
+                'linux' if plat.startswith('linux') else
+                'freebsd' if plat.startswith(
+                    ('freebsd', 'openbsd', 'isilon onefs')) else plat)
+        if plat == 'linux':
+            if hasattr(sys, 'getandroidapilevel'):
+                plat = 'android'
+            else:
+                cname, cver = platform.libc_ver()
+                if cname == 'musl':
+                    plat = 'alpine'
+                elif cname == 'libc':
+                    plat = 'android'
+        return plat
+
+    def format_machine():
+        mach = platform.machine().lower()
+        arch_table = (
+            ('x86', ('i386', 'i486', 'i586', 'i686')),
+            ('x86_64', ('x64', 'x86_64', 'amd64', 'intel')),
+            ('arm', ('armv5',)),
+            ('armv6', ('armv6l',)),
+            ('armv7', ('armv7l',)),
+            ('aarch32', ('aarch32',)),
+            ('aarch64', ('aarch64', 'arm64'))
+        )
+        for alias, archlist in arch_table:
+            if mach in archlist:
+                mach = alias
+                break
+        return mach
+
+    plat, mach = format_system(), format_machine()
+    if plat == 'windows' and mach == 'x86_64':
+        bitness = calcsize('P'.encode()) * 8
+        if bitness == 32:
+            mach = 'x86'
+
+    name = '.'.join(['_'.join([plat, mach]), 'pyarmor_runtime'])
+    return __import__(name, globals(), locals(), ['__pyarmor__'], level=1)
+__pyarmor__ = __pyarmor__().__pyarmor__
+'''
+
+runtime_package_template3 = '''# Pyarmor $rev, $timestamp
+from importlib.machinery import ExtensionFileLoader
+from sysconfig import get_platform
+__pyarmor__ = ExtensionFileLoader(
+    '.pyarmor_runtime', __file__.replace('__init__.py', 'pyarmor_runtime.so')
+).load_module().__pyarmor__
 '''
 
 
 def format_platform(plat, arch):
     from struct import calcsize
     from fnmatch import fnmatchcase
 
@@ -96,25 +141,20 @@
             os.path.join(self.home_path, rpath)
 
         # self.encoding is just for reading config file
         self.encoding = encoding
         cfglist = self.default_config, self.global_config, self.local_config
         self.cfg = self._read_config(cfglist, encoding=encoding)
 
-        self.inline_plugin_marker = '# pyarmor: '
         # self.runtime_package = 'pyarmor_runtime'
         # self.runtime_suffix = '_000000'
         # default inner key filename within runtime package
         self.runtime_keyfile = '.pyarmor.ikey'
 
         self.bootstrap_template = bootstrap_template
-        self.runtime_package_templates = (
-            runtime_package_template,
-            runtime_package_template2,
-        )
 
         # Alias format for duplicated input names
         self.alias_suffix = '{0}-{1}'
 
         self.input_paths = []
         self.outputs = []
         self.resources = []
@@ -211,15 +251,15 @@
 
     def version_info(self, verbose=3):
         #    8.0.1
         #    8.0.1 (trial)
         #    8.0.1 (basic), 002000
         #    8.0.1 (group), 002002, Product
         #    8.0.1 (group), 002002, Product, Company
-        rev = '.'.join([str(x) for x in self.version])
+        rev = '.'.join(self.version)
         if not verbose:
             return rev
 
         licinfo = self.license_info
         lictype = 'basic' if licinfo['features'] == 1 else \
             'pro' if licinfo['features'] == 7 else \
             'group' if licinfo['features'] == 15 else \
@@ -238,16 +278,15 @@
             if regname:
                 verinfo.append(regname)
 
         return ', '.join(verinfo)
 
     @property
     def version(self):
-        getint = self.cfg.getint
-        return [getint('pyarmor', x) for x in ('major', 'minor', 'patch')]
+        return [self.cfg.get('pyarmor', x) for x in ('major', 'minor', 'patch')]
 
     @property
     def python_version(self):
         return sys.version_info[:2]
 
     @property
     def default_config(self):
@@ -315,14 +354,18 @@
             self.cfg['logging'].get('debug_logfile', 'pyarmor.debug.log'))
 
     @property
     def trace_logfile(self):
         return self._check_logpath(
             self.cfg['logging'].get('trace_logfile', 'pyarmor.trace.log'))
 
+    @property
+    def repack_path(self):
+        return os.path.join(self.local_path, 'pack')
+
     def _optb(self, section, name):
         return self.cfg.getboolean(section, name, vars=self.cmd_options)
 
     def _opts(self, section, name):
         return self.cfg.get(section, name, vars=self.cmd_options)
 
     def _opti(self, section, name):
@@ -434,14 +477,20 @@
         return self.cfg['builder'].get('outer_keyname', 'pyarmor.rkey')
 
     @property
     def use_runtime(self):
         return self.cmd_options.get('use_runtime',
                                     self.cfg['builder'].get('use_runtime'))
 
+    @property
+    def inline_plugin_marker(self):
+        marker = self.cfg['builder'].get('inline_plugin_marker', 'false')
+        if marker.lower() not in ('', 'false', '0'):
+            return '# %s: ' % marker
+
     #
     # runtime configuration
     #
     def _rt_opt(self, opt):
         return self.cmd_options.get(opt, self.cfg['runtime'].get(opt))
 
     @property
@@ -498,15 +547,24 @@
     @property
     def runtime_devices(self):
         value = self._rt_opt('devices')
         return value.splitlines() if isinstance(value, str) else value
 
     @property
     def runtime_interps(self):
-        return self._rt_opt('interps')
+        interps = self._rt_opt('interps')
+        rules = interps.splitlines() if interps else []
+        cfg = self.cfg['builder']
+        if cfg.getboolean('check_debugger', False):
+            rules.append('check-debugger')
+        if cfg.getboolean('check_interp', False):
+            rules.append('check-interp')
+        if self.runtime_hook('pyarmor_runtime'):
+            rules.append('py:bootstrap')
+        return '\n'.join(rules)
 
     @property
     def runtime_timer(self):
         return self._opti('runtime', 'timer')
 
     @property
     def runtime_simple_extension_name(self):
@@ -519,31 +577,29 @@
         if filename:
             if filename[0] == '@':
                 with open(filename[1:], 'rb') as f:
                     data = f.read()
             else:
                 data = filename.encode()
 
-        hook = b''
-        filename = os.path.join(self.local_path, 'hooks', 'pyarmor_runtime.py')
-        if os.path.exists(filename):
-            with open(filename, 'rb') as f:
-                hook = f.read()
-
-        return hook, data
+        return data
 
     @property
     def runtime_messages(self):
         value = self.cfg['runtime'].get('messages', '')
         if value:
             name, encoding = (value + ':utf-8').split(':')[:2]
             cfg = self._named_config(name, encoding=encoding)
             if cfg.has_section('runtime.message'):
                 return cfg
 
+    def runtime_package_template(self, platforms):
+        return runtime_package_template if len(platforms) < 2 else \
+            multi_runtime_package_template
+
     #
     # RFT settings
     #
 
     def rft_output_script(self, name):
         return self._check_logpath(os.path.join(self.local_path, 'rft', name))
```

## Comparing `pyarmor-8.2.dev2/src/cli/mixer.py` & `pyarmor-8.3.dev1/pyarmor/cli/mixer.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/cli/public_capsule.zip` & `pyarmor-8.3.dev1/pyarmor/cli/public_capsule.zip`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/cli/default.cfg` & `pyarmor-8.3.dev1/pyarmor/cli/default.cfg`

 * *Files 26% similar despite different names*

```diff
@@ -1,17 +1,19 @@
 [pyarmor]
 
 ;; Pyarmor version
 major = 8
-minor = 2
-patch = 0
+minor = 3
+patch = dev1
 
 ;; Core version
-cli.core = 3.2
-cli.runtime = 3.2
+cli.core = 4.3.dev1
+
+;; Deprecated since Pyarmor 8.2.5
+; cli.runtime = 3.2.5
 
 ;; Default timeout when send request to remote server for
 ;;     check Pyarmor license
 ;;     register Pyarmor license
 timeout = 6
 
 regurl = https://api.dashingsoft.com/product/key/enter/%s/?
@@ -21,15 +23,15 @@
 
 debug_logfile = .pyarmor/pyarmor.debug.log
 trace_logfile = .pyarmor/pyarmor.trace.log
 
 [finder]
 recursive = 0
 ;; includes =
-;; excludes =
+excludes = */__pycache__
 pyexts = .py .pyw
 
 ;; Data files need to copy to output path
 ;;   *.txt only copy .txt file
 ;;   * means all data files
 ;;   0 means nothing to copy
 data_files = 0
@@ -56,24 +58,28 @@
 ;; Import prefix to import runtime package
 import_prefix = 0
 
 ;; Sometimes __file__ is not defined, replace it with __name__ to fix this issue
 bootstrap_file = __file__
 
 ;; Exclude co objects by co_name
-exclude_co_names = <lambda> <listcomp> <setcomp> <dictcomp> <generator>
+exclude_co_names = <lambda> <listcomp> <setcomp> <dictcomp> <genexpr>
 
 ;; Common modules which are no restrict
 exclude_restrict_modules = __init__
 
 ;; Outer key name
 outer_keyname = pyarmor.rkey
 
-;; inline_plugin = "# pyarmor: "
-inline_plugin = 1
+;; The final marker is "# %s: " % VALUE
+;; If VALUE == "false", then disable inline plugin
+inline_plugin_marker = pyarmor
+
+;; Default plugins
+plugins = CodesignPlugin
 
 ;; Using shared runtime package
 ; use_runtime = /path/to/runtime
 
 ;; How many loops for jit iv
 jit_iv_threshold = 100
 
@@ -110,15 +116,15 @@
 ;;
 
 ;; The argument optimize specifies the optimization level of the
 ;; compiler; the default value of -1 selects the optimization level of
 ;; the interpreter as given by -O options. Explicit levels are 0 (no
 ;; optimization; __debug__ is true), 1 (asserts are removed, __debug__
 ;; is false) or 2 (docstrings are removed too).
-optimize = 1
+optimize = -1
 
 ;; It's not used now
 type_comments = false
 
 ;; Write refactor result scripts
 trace_rft = 0
 
@@ -225,20 +231,17 @@
 
 ;; Bind runtime key to multiple devices, one line one machine
 ; devices =
 
 ;; Bind runtime key to Python interperter. Each line defines a rule,
 ;; match all the rules. The rule formats
 ;;
-;;      s: symbol symbol DIFF
-;;      S: symbol symbol xxxxxx(md5)
-;;      f: name SIZE
-;;      F: name xxxxxxxx(md5)
-;;      m: name SIZE
-;;      M: name xxxxxxxx(md5)
+;;      D
+;;      S: symbol start end xxxxxx(md5)
+;;
 ; interps =
 
 ;; Insert runtime hooks
 ; hooks = hooks.py
 
 ;; Enable timer
 timer = 0
@@ -269,24 +272,20 @@
 ;; do not mix short string len(s) < this value
 threshold = 8
 
 ; includes =
 ; excludes =
 
 [pack]
+;; For Darwin to code sign binary file
+; codesign_identify =
+
 ;; Strip output path to match archive info
 strip = 0
 
-;; How to handle other .pyc in the bundle
-;;     0  not obfuscate
-;;     1  obf module only
-;;     2  obf module and co_code without lambda and comprehensions
-;;     3  obf module and all co_code
-other_pyc = 0
-
 ;; How to do when the obfuscated module has no matched .pyc in bundle
 ;;    error, issue a error and exit
 ;;    warning, issue a warning and continue
 ;;    ignore, do nothing
 ;;    append, append it to archive
 no_matched_pyc = error
 
@@ -337,7 +336,28 @@
 cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fno-stack-protector -shared -nostdlib -Tlinux.armv7.ldscript
 
 [darwin.x86_64.bcc]
 cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables --target=x86_64-elf-gnu_linux -fPIC -c
 
 [darwin.aarch64.bcc]
 cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables --target=arm64-macho-darwin -fPIC -fno-addrsig -fno-stack-protector -shared -nostdlib -lsystem
+
+[android.x86_64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -c
+
+[android.aarch64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -shared -nostdlib -Tlinux.aarch64.ldscript
+
+[android.x86.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fno-stack-protector -fPIC -c
+
+[android.armv7.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fno-stack-protector -shared -nostdlib -Tlinux.armv7.ldscript
+
+[alpine.x86_64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -c
+
+[alpine.aarch64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -shared -nostdlib -Tlinux.aarch64.ldscript
+
+[freebsd.x86_64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -c
```

## Comparing `pyarmor-8.2.dev2/src/cli/__main__.py` & `pyarmor-8.3.dev1/pyarmor/cli/__main__.py`

 * *Files 2% similar despite different names*

```diff
@@ -26,14 +26,16 @@
 
 from . import logger, CliError
 from .context import Context
 from .register import Register, WebRegister
 from .config import Configer
 from .shell import PyarmorShell
 from .plugin import Plugin
+from .generate import Builder
+from .bootstrap import check_prebuilt_runtime_library
 
 
 def _cmd_gen_key(builder, options):
     n = len(options['inputs'])
     if n > 1:
         logger.error('please check online documentation to learn')
         logger.error('how to use command "pyarmor gen key"')
@@ -59,15 +61,15 @@
         logger.error('please check online documentation to learn')
         logger.error('how to use command "pyarmor gen runtime"')
         raise CliError('invalid arguments: %s' % options['inputs'][1:])
 
     output = options.get('output', 'dist')
 
     logger.info('start to generate runtime package')
-    builder.generate_runtime(output)
+    builder.generate_runtime_package(output)
 
     keyname = os.path.join(output, builder.ctx.runtime_keyfile)
     logger.info('write "%s"', keyname)
     with open(keyname, 'wb') as f:
         f.write(builder.ctx.runtime_key)
     logger.info('generate runtime package to "%s" OK', output)
 
@@ -105,16 +107,14 @@
         if options.get('restrict_module', 0) < 2:
             logger.debug('implicitly set restrict_module = 2')
             options['restrict_module'] = 2
 
     if args.enables:
         for x in args.enables:
             options['enable_' + x] = True
-    if options.get('enable_themida'):
-        raise NotImplementedError('--enable_themida is still not implemented')
 
     if args.prefix:
         options['import_prefix'] = args.prefix
 
     if args.no_wrap:
         options['wrap_mode'] = 0
 
@@ -122,14 +122,19 @@
         options['includes'] = ' '.join(args.includes)
     if args.excludes:
         options['excludes'] = ' '.join(args.excludes)
 
     if args.bind_data:
         options['user_data'] = args.bind_data
 
+    if args.pack:
+        dist_path = os.path.join(ctx.repack_path, 'dist')
+        logger.info('implicitly set output to "%s"', dist_path)
+        options['output'] = dist_path
+
     return options
 
 
 def check_cross_platform(ctx, platforms):
     rtver = ctx.cfg.get('pyarmor', 'cli.runtime')
     cmd = 'pip install pyarmor.cli.runtime~=%s.0' % rtver
     try:
@@ -153,29 +158,34 @@
 
     if unknown:
         logger.error('please check documentation "References/Environments"')
         raise CliError('unsupported platforms "%s"' % ', '.join(unknown))
 
 
 def check_gen_context(ctx, args):
-    enable_bcc = args.enable_bcc or (args.enables and 'bcc' in args.enables)
-    if ctx.runtime_platforms:
-        if ctx.enable_themida and not ctx.pyarmor_platform.startswith('win'):
-            raise CliError('--enable_themida only works for Windows')
-        if enable_bcc:
+    platforms = ctx.runtime_platforms
+    if platforms and set(platforms) != set([ctx.pyarmor_platform]):
+        if ctx.enable_bcc:
             raise CliError('bcc mode does not support cross platform')
-        check_cross_platform(ctx, ctx.runtime_platforms)
+        rtver = ctx.cfg['pyarmor'].get('cli.runtime', '')
+        check_prebuilt_runtime_library(platforms, ctx.enable_themida, rtver)
 
-    if enable_bcc:
+    elif ctx.enable_themida:
+        if not ctx.pyarmor_platform.startswith('windows'):
+            raise CliError('--enable-themida only works for Windows')
+        rtver = ctx.cfg['pyarmor'].get('cli.runtime', '')
+        check_prebuilt_runtime_library([], ['themida'], rtver)
+
+    if ctx.enable_bcc:
         plat, arch = ctx.pyarmor_platform.split('.')
         if arch not in ('x86_64', 'aarch64', 'x86', 'armv7'):
             raise CliError('bcc mode still not support arch "%s"' % arch)
 
-    if ctx.cmd_options['no_runtime'] and not ctx.runtime_outer:
-        raise CliError('--no_runtime must be used with --outer')
+    if ctx.cmd_options.get('no_runtime') and not ctx.runtime_outer:
+        raise CliError('--outer is required if using --no_runtime')
 
     if ctx.use_runtime and not ctx.runtime_outer:
         if os.path.exists(ctx.use_runtime):
             keyname = os.path.join(ctx.use_runtime, ctx.runtime_keyfile)
             if not os.path.exists(keyname):
                 raise CliError('no runtime key in "%s"', ctx.use_runtime)
 
@@ -189,31 +199,35 @@
         if args.no_runtime:
             raise CliError('--pack conficts with --no-runtime, --use-runtime')
         if ctx.import_prefix:
             raise CliError('--pack conficts with -i, --prefix')
 
 
 def cmd_gen(ctx, args):
-    from .generate import Builder
-
     options = format_gen_args(ctx, args)
     logger.debug('command options: %s', options)
     ctx.push(options)
     check_gen_context(ctx, args)
 
     builder = Builder(ctx)
 
     Plugin.install(ctx)
     if args.inputs[0].lower() in ('key', 'k'):
         _cmd_gen_key(builder, options)
     elif args.inputs[0].lower() in ('runtime', 'run', 'r'):
         _cmd_gen_runtime(builder, options)
-    else:
-        builder.process(options, pack=args.pack)
+    elif args.pack:
+        from .repack import Repacker
+        codesign = ctx.cfg['pack'].get('codesign_identify', None)
+        packer = Repacker(args.pack, ctx.repack_path, codesign=codesign)
+        builder.process(options, packer=packer)
         Plugin.post_build(ctx, pack=args.pack)
+    else:
+        builder.process(options)
+        Plugin.post_build(ctx)
 
 
 def cmd_cfg(ctx, args):
     scope = 'global' if args.scope else 'local'
     cfg = Configer(ctx, encoding=args.encoding)
     name = 'reset' if args.reset else 'run'
     getattr(cfg, name)(args.options, scope == 'local', args.name)
@@ -259,14 +273,15 @@
                "", "")
         prompt = 'I have known the changes of Pyarmor 8? (yes/no/help) '
         choice = input('\n'.join(msg) + prompt).lower()[:1]
         if choice == 'h':
             import webbrowser
             webbrowser.open(url)
         if not choice == 'y':
+            logger.info('abort upgrade')
             return
 
     if args.device:
         if not regfile.endswith('.zip'):
             logger.error('invalid registeration file "%s"', regfile)
             raise CliError('please use ".zip" file to register group device')
         regsvr = WebRegister(ctx)
@@ -279,15 +294,18 @@
         reg.register_regfile(regfile)
         logger.info('This license registration information:\n\n%s', str(reg))
 
     else:
         regsvr = WebRegister(ctx)
         info, msg = regsvr.prepare(regfile, args.product, upgrade=upgrade)
         prompt = 'Are you sure to continue? (yes/no) '
-        if input(msg + prompt) not in ('y', 'yes'):
+        if args.confirm:
+            from time import sleep
+            sleep(1.0)
+        elif input(msg + prompt) not in ('y', 'yes'):
             logger.info('abort registration')
             return
         # Free upgrade to Pyarmor Basic
         if upgrade and not info['upgrade']:
             return regsvr.register(regfile, args.product, upgrade=True)
 
         if upgrade:
@@ -296,14 +314,15 @@
             group = info['lictype'] == 'GROUP'
             regsvr.register(regfile, args.product, group=group)
 
 
 def main_parser():
     parser = argparse.ArgumentParser(
         prog='pyarmor',
+        fromfile_prefix_chars='@',
         formatter_class=argparse.RawDescriptionHelpFormatter,
     )
     parser.add_argument(
         '-v', '--version', action='store_true',
         help='show version information and exit'
     )
     parser.add_argument(
@@ -382,23 +401,23 @@
     )
     group.add_argument(
         '--include', dest='includes', metavar='PATTERN', action='append',
         help=argparse.SUPPRESS
     )
     group.add_argument(
         '--exclude', dest='excludes', metavar='PATTERN', action='append',
-        help=argparse.SUPPRESS
+        help='Exclude scripts and paths'
     )
 
     group.add_argument(
         '--obf-module', type=int, default=None, choices=(0, 1),
         help='obfuscate whole module (default is 1)'
     )
     group.add_argument(
-        '--obf-code', type=int, default=None, choices=(0, 1),
+        '--obf-code', type=int, default=None, choices=(0, 1, 2),
         help='obfuscate each function (default is 1)'
     )
     group.add_argument(
         '--no-wrap', action='store_true', default=None,
         help='disable wrap mode',
     )
 
@@ -467,37 +486,28 @@
         help='enable outer runtime key'
     )
     group.add_argument(
         '-e', '--expired', metavar='DATE',
         help='set expired date'
     )
     group.add_argument(
-        '--period', type=int, metavar='N', dest='period',
+        '--period', metavar='N', dest='period',
         help='check runtime key periodically'
     )
     group.add_argument(
         '-b', '--bind-device', dest='devices', metavar='DEV', action='append',
         help='bind obfuscated scripts to device'
     )
     group.add_argument(
         '--bind-data', metavar='FILE',
         help=argparse.SUPPRESS
     )
-    group.add_argument(
-        '--bind-interp', metavar='INTERP',
-        help=argparse.SUPPRESS
-    )
-    group.add_argument(
-        '--hook', metavar='HOOK',
-        help=argparse.SUPPRESS
-    )
 
     cparser.add_argument(
-        'inputs', metavar='ARG', nargs='+',
-        help='script, package or keyword "key", "runtime"'
+        'inputs', metavar='ARG', nargs='+', help='scripts or packages'
     )
 
     cparser.set_defaults(func=cmd_gen)
 
 
 def cfg_parser(subparsers):
     '''show all options:
@@ -559,15 +569,15 @@
 https://pyarmor.readthedocs.io/en/stable/reference/man.html#pyarmor-reg
     '''
     cparser = subparsers.add_parser(
         'reg',
         aliases=['register', 'r'],
         formatter_class=argparse.RawDescriptionHelpFormatter,
         description=reg_parser.__doc__,
-        help='register Pyarmor or upgrade Pyarmor license'
+        help='register Pyarmor or upgrade old Pyarmor license'
     )
 
     cparser.add_argument(
         '-r', '--regname', metavar='NAME',
         help=argparse.SUPPRESS
     )
     cparser.add_argument(
```

## Comparing `pyarmor-8.2.dev2/src/cli/repack.py` & `pyarmor-8.3.dev1/pyarmor/helper/repack.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,16 +1,66 @@
+'''
+This script is used to repack PyInstaller bundle with obfuscated scripts
+
+First pack the script by PyInstaller, next obfuscate the scripts by PyArmor,
+finally run this script to repack the bundle with obfuscated scripts.
+
+* Pack the script with PyInstaller, make sure the final bundle works
+
+    # One folder mode
+    pyinstaller foo.py
+
+    # Check it works
+    dist/foo/foo
+
+    # One file mode
+    pyinstaller --onefile foo.py
+
+    # Check it works
+    dist/foo
+
+* Obfuscate the scripts to "obfdist", make sure the obfuscated scripts
+  work
+
+    # Option --package-runtime should be set to 0
+    pyarmor obfuscate -O obfdist --package-runtime 0 foo.py
+
+    # For super mode
+    pyarmor obfuscate -O obfdist --advanced 2 foo.py
+
+    # Check it works
+    python dist/foo.py
+
+* Repack the final executable, use the same Python interpreter as PyInstaller using
+
+    # One folder mode
+    python repack.py -p obfdist dist/foo/foo
+
+    # Overwrite the old one
+    cp foo-obf dist/foo/foo
+
+    # One file mode
+    python repack.py -p obfdist dist/foo
+
+    # Overwrite the old one
+    cp foo-obf dist/foo
+
+Here "foo-obf" is the patched bundle.
+
+'''
+import argparse
 import logging
 import marshal
 import os
 import shutil
 import struct
+import sys
 import zlib
 
 from subprocess import check_call
-from tempfile import TemporaryDirectory
 
 from PyInstaller.archive.writers import ZlibArchiveWriter, CArchiveWriter
 from PyInstaller.archive.readers import CArchiveReader
 try:
     from PyInstaller.loader.pyimod02_archive import ZlibArchiveReader
     from PyInstaller.loader.pyimod02_archive import PYZ_TYPE_PKG
 except ModuleNotFoundError:
@@ -30,33 +80,37 @@
             we understand.
         """
         self.lib.seek(self.start)  # default - magic is at start of file.
         if self.lib.read(len(self.MAGIC)) != self.MAGIC:
             raise RuntimeError("%s is not a valid %s archive file"
                                % (self.path, self.__class__.__name__))
         if self.lib.read(len(self.pymagic)) != self.pymagic:
-            logger.warning("pyz is from a different Python version")
+            print("Warning: pyz is from a different Python version")
         self.lib.read(4)
 
 
 class CArchiveWriter2(CArchiveWriter):
 
     def add(self, entry):
         patched, dlen, ulen, flag, typcd, nm, pathnm = entry
         where = self.lib.tell()
 
-        logger.debug('add item "%s"', nm)
+        logger.debug('Add item "%s"', nm)
+
+        if is_darwin and patched and typcd == 'b':
+            from PyInstaller.depend import dylib
+            dylib.mac_set_relative_dylib_deps(pathnm, os.path.basename(pathnm))
 
         fh = open(pathnm, 'rb')
         filedata = fh.read()
         fh.close()
 
         if patched:
-            logger.info('replace item with "%s"(%s)', pathnm, typcd)
-            if typcd.lower() in ('s', 'm'):
+            logger.info('Replace item "%s" with "%s"', nm, pathnm)
+            if typcd in ('s', 'M'):
                 code = compile(filedata, '<%s>' % nm, 'exec')
                 filedata = marshal.dumps(code)
                 ulen = len(filedata)
             else:
                 ulen = len(filedata)
 
         if flag == 1 and patched:
@@ -123,220 +177,219 @@
     fp.close()
 
     # Overlay is the data appended at the end of the PE
     pos = filesize - lengthofPackage
     return pos, pylibname.decode()
 
 
-def append_runtime_files(obfpath, rtname):
-    logger.info('appending runtime files to archive')
-    logic_toc = []
+def append_runtime_files(logic_toc, obfpath):
+    logger.info('Appending runtime files to archive')
+
+    n = 0
 
     def add_toc(typcd, name, pathnm):
-        logger.info('add "%s"(%s)', pathnm, typcd)
+        logger.info('Add "%s"', pathnm)
+        if os.path.isdir(pathnm):
+            raise RuntimeError('It is not allowed to write path "%s" to '
+                               'bundle. When obfuscating the scripts, '
+                               'make sure "--package-runtime 0" is used',
+                               pathnm)
+        if n > 1:
+            raise RuntimeError('In the path "%s", there are too many '
+                               'files start with "pytransform" or '
+                               '"_pytransform", there shuold be only one',
+                               obfpath)
         logic_toc.append((1, 0, 0, 1, typcd, name, pathnm))
 
-    for name in os.listdir(os.path.join(obfpath, rtname)):
-        if name.endswith('.py'):
-            continue
-        typcd = 'x' if name.endswith('key') else 'b'
-        pathnm = os.path.join(obfpath, rtname, name)
-        distname = '/'.join([rtname, name])
-        add_toc(typcd, distname, pathnm)
+    for name in os.listdir(obfpath):
+        pathnm = os.path.join(obfpath, name)
+        if (name.startswith('pytransform') and name[-3:] != '.py') \
+           or name.startswith('_pytransform'):
+            n += 1
+            add_toc('b', name, pathnm)
+        elif name == 'license.lic':
+            add_toc('x', name, pathnm)
 
-        if is_darwin and typcd == 'b':
-            from PyInstaller.depend import dylib
-            logger.debug('mac_set_relative_dylib_deps "%s"', distname)
-            dylib.mac_set_relative_dylib_deps(pathnm, distname)
-
-    return logic_toc
+    logger.info('Append runtime files OK')
 
 
-def repack_pyz(pyz, obfpath, rtname, cipher=None, clean=False):
+def repack_pyz(pyz, obfpath, cipher=None, clean=False):
     code_dict = {}
     obflist = []
 
     n = len(obfpath) + 1
     for dirpath, dirnames, filenames in os.walk(obfpath):
         for pyfile in [x for x in filenames if x.endswith('.py')]:
             pyfile = os.path.join(dirpath, pyfile)
-            logger.info('compile %s', pyfile)
+            logger.info('Compile %s', pyfile)
             name = pyfile[n:].replace('\\', '.').replace('/', '.')[:-3]
             if name.endswith('__init__.py'):
                 name = name[:-len('__init__.py')].strip('.')
             with open(pyfile, 'r') as f:
                 source = f.read()
-            logger.debug('got obfuscated item: %s', name)
+            logger.debug('Got obfuscated item: %s', name)
             code_dict[name] = compile(source, '<%s>' % name, 'exec')
             obflist.append(name)
-    logger.info('got %d obfuscated items', len(obflist))
+    logger.info('Got %d obfuscated items', len(obflist))
 
-    logger.info('patching PYZ file "%s"', pyz)
+    logger.info('Patching PYZ file "%s"', pyz)
     arch = ZlibArchive(pyz)
 
     logic_toc = []
     for name in arch.toc:
-        logger.debug('extract %s', name)
+        logger.debug('Extract %s', name)
         typ, obj = arch.extract(name)
         if name in obflist:
-            logger.info('replace item "%s" with obfsucated one', name)
+            logger.info('Replace item "%s" with obfsucated one', name)
             obflist.remove(name)
         else:
             code_dict[name] = obj
         pathname = '__init__.py' if typ == PYZ_TYPE_PKG else name
         logic_toc.append((name, pathname, 'PYMODULE'))
-
-        if name == rtname:
-            raise RuntimeError('this bundle has been patched by Pyarmor')
-
-    logic_toc.append((rtname, '__init__.py', 'PYMODULE'))
-    pathname = os.path.join(obfpath, rtname, '__init__.py')
-    with open(pathname, 'r') as f:
-        source = f.read()
-    code_dict[rtname] = compile(source, '<%s>' % rtname, 'exec')
-
     logger.debug('unhandled obfuscated items are %s', obflist)
 
     ZlibArchiveWriter(pyz, logic_toc, code_dict=code_dict, cipher=cipher)
-    logger.info('patch PYZ done')
+    logger.info('Patch PYZ done')
 
 
 def repack_exe(path, obfname, logic_toc, obfentry, codesign=None):
-    logger.info('repacking EXE "%s"', obfname)
+    logger.info('Repacking EXE "%s"', obfname)
 
     if is_darwin:
         import PyInstaller.utils.osx as osxutils
         if hasattr(osxutils, 'remove_signature_from_binary'):
-            logger.info("removing signature(s) from EXE")
+            logger.info("Removing signature(s) from EXE")
             osxutils.remove_signature_from_binary(obfname)
 
     offset, pylib_name = get_carchive_info(obfname)
-    logger.info('get archive info (%d, "%s")', offset, pylib_name)
+    logger.info('Get archive info (%d, "%s")', offset, pylib_name)
 
     pkgname = os.path.join(path, 'PKG-pyarmor-patched')
-    logging.info('patching PKG file "%s"', pkgname)
+    logging.info('Patching PKG file "%s"', pkgname)
     CArchiveWriter2(pkgname, logic_toc, pylib_name=pylib_name)
-    logging.info('patch PKG done')
+    logging.info('Patch PKG done')
 
     if is_linux:
-        logger.info('replace section "pydata" with "%s" in EXE', pkgname)
+        logger.info('Replace section "pydata" with "%s" in EXE', pkgname)
         check_call(['objcopy', '--update-section', 'pydata=%s' % pkgname,
                     obfname])
     else:
-        logger.info('replace PKG with "%s" in EXE', pkgname)
+        logger.info('Replace PKG with "%s" in EXE', pkgname)
         with open(obfname, 'r+b') as outf:
             # Keep bootloader
             outf.seek(offset, os.SEEK_SET)
 
             # Write the patched archive
             with open(pkgname, 'rb') as infh:
                 shutil.copyfileobj(infh, outf, length=64*1024)
 
             outf.truncate()
 
     if is_darwin:
         # Fix Mach-O header for codesigning on OS X.
-        logger.info('fixing EXE for code signing "%s"', obfname)
+        logger.info('Fixing EXE for code signing "%s"', obfname)
         import PyInstaller.utils.osx as osxutils
         osxutils.fix_exe_for_code_signing(obfname)
 
         if hasattr(osxutils, 'sign_binary'):
-            logger.info("re-signing the EXE")
+            logger.info("Re-signing the EXE")
             osxutils.sign_binary(obfname, identity=codesign)
 
     if is_win:
         # Set checksum to appease antiviral software.
         from PyInstaller.utils.win32 import winutils
         if hasattr(winutils, 'set_exe_checksum'):
             winutils.set_exe_checksum(obfname)
 
-    logger.info('generate patched bundle "%s" successfully', obfname)
+    logger.info('Generate patched bundle "%s" successfully', obfname)
 
 
-def repacker(executable, obfpath, buildpath='', entry=None, codesign=None):
-    logger.info('repack bundle "%s"', executable)
+def repacker(executable, obfpath, entry=None, codesign=None):
+    logger.info('Repack PyInstaller bundle "%s"', executable)
 
     obfpath = os.path.normpath(obfpath)
-    logger.info('obfuscated scripts at "%s"', obfpath)
+    logger.info('Obfuscated scripts in the path "%s"', obfpath)
 
     name, ext = os.path.splitext(os.path.basename(executable))
     entry = name if entry is None else entry
-    logger.info('entry script name is "%s.py"', entry)
+    logger.info('Entry script name is "%s.py"', entry)
 
     arch = CArchiveReader(executable)
     logic_toc = []
 
     obfentry = os.path.join(obfpath, entry + '.py')
     if not os.path.exists(obfentry):
-        raise RuntimeError('no obfuscated entry "%s" found', obfentry)
+        raise RuntimeError('No obfuscated script "%s" found', obfentry)
 
-    for item in os.listdir(obfpath):
-        if item.startswith('pyarmor_runtime_'):
-            logger.info('runtime package is "%s"', item)
-            rtname = item
-            break
-    else:
-        raise RuntimeError('no runtime package found')
-
-    path = os.path.join(buildpath, name + '_extracted')
-    logger.info('extracted bundle files to "%s"', path)
+    path = os.path.join(name + '_extracted')
+    logger.info('Extracted bundle files to "%s"', path)
     makedirs(path, exist_ok=True)
 
     for item in arch.toc:
         logger.debug('toc: %s', item)
         dpos, dlen, ulen, flag, typcd, nm = item
         pathnm = os.path.join(path, nm)
         makedirs(os.path.dirname(pathnm), exist_ok=True)
         with arch.lib:
             arch.lib.seek(arch.pkg_start + dpos)
             with open(pathnm, 'wb') as f:
                 f.write(arch.lib.read(dlen))
 
             if nm.endswith('.pyz') and typcd in ('z', 'Z'):
-                logger.info('extract pyz file "%s"', pathnm)
-                repack_pyz(pathnm, obfpath, rtname)
+                logger.info('Extract pyz file "%s"', pathnm)
+                repack_pyz(pathnm, obfpath)
                 patched = 1
             elif name == nm:
                 patched = 1
                 pathnm = obfentry
             else:
                 patched = 0
             logic_toc.append((patched, dlen, ulen, flag, typcd, nm, pathnm))
 
-    extra_toc = append_runtime_files(obfpath, rtname)
-    if len(logic_toc) > 10:
-        logic_toc.extend(extra_toc)
-    else:
-        dest = os.path.dirname(executable)
-        logger.info('copy runtime files to "%s"', dest)
-        os.makedirs(os.path.join(dest, rtname), exist_ok=True)
-        for item in extra_toc:
-            shutil.copy2(item[-1], os.path.join(dest, item[-2]))
+    append_runtime_files(logic_toc, obfpath)
 
-    obfname = os.path.join(buildpath, name + '_obf' + ext)
+    obfname = os.path.join(name + '_obf' + ext)
     shutil.copy2(executable, obfname)
     repack_exe(path, obfname, logic_toc, obfentry, codesign=codesign)
 
-    logger.info('move "%s" to "%s"', obfname, executable)
-    shutil.move(obfname, executable)
-
 
-def list_modules(executable):
-    modules = []
-    arch = CArchiveReader(executable)
-
-    def read_toc(nm, dlen):
-        with TemporaryDirectory() as tmp:
-            path = os.path.join(tmp, nm)
-            with open(path, 'wb') as f:
-                f.write(arch.lib.read(dlen))
-            return ZlibArchiveReader(path).toc
+def excepthook(type, exc, traceback):
+    try:
+        msg = exc.args[0] % exc.args[1:]
+    except Exception:
+        msg = str(exc)
+    logging.error(msg)
+    sys.exit(1)
+
+
+def main():
+    parser = argparse.ArgumentParser()
+    parser.add_argument('-d', '--debug',
+                        default=False,
+                        action='store_true',
+                        dest='debug',
+                        help='print debug log (default: %(default)s)')
+    parser.add_argument('-p', '--path',
+                        default='obfdist',
+                        dest='obfpath',
+                        help='obfuscated scripts path (default: %(default)s)')
+    parser.add_argument('-e', '--entry',
+                        help="Entry script if it's different from bundle name")
+    parser.add_argument('--codesign-identity',
+                        help="Code signing identity (macOS only).")
+    parser.add_argument('executable', metavar='executable',
+                        help="PyInstaller archive")
+
+    args = parser.parse_args(sys.argv[1:])
+    if args.debug:
+        logger.setLevel(logging.DEBUG)
+    else:
+        sys.excepthook = excepthook
+    repacker(args.executable, args.obfpath, args.entry, args.codesign_identity)
 
-    for item in arch.toc:
-        logger.debug('toc: %s', item)
-        dpos, dlen, ulen, flag, typcd, nm = item
-        with arch.lib:
-            arch.lib.seek(arch.pkg_start + dpos)
-            if nm.endswith('.pyz') and typcd in ('z', 'Z'):
-                modules.extend(read_toc(nm, dlen))
 
-    return modules
+if __name__ == '__main__':
+    logging.basicConfig(
+        level=logging.INFO,
+        format='%(message)s',
+    )
+    main()
```

## Comparing `pyarmor-8.2.dev2/src/examples/obfuscate-pkg.bat` & `pyarmor-8.3.dev1/pyarmor/examples/obfuscate-pkg.bat`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/obfuscate-app.bat` & `pyarmor-8.3.dev1/pyarmor/examples/obfuscate-app.bat`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/obfuscate-app.sh` & `pyarmor-8.3.dev1/pyarmor/examples/obfuscate-app.sh`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/obfuscate-pkg.sh` & `pyarmor-8.3.dev1/pyarmor/examples/obfuscate-pkg.sh`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/build-with-project.bat` & `pyarmor-8.3.dev1/pyarmor/examples/build-with-project.bat`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/README.md` & `pyarmor-8.3.dev1/pyarmor/examples/README.md`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pack-obfuscated-scripts.sh` & `pyarmor-8.3.dev1/pyarmor/examples/pack-obfuscated-scripts.sh`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pack-obfuscated-scripts.bat` & `pyarmor-8.3.dev1/pyarmor/examples/pack-obfuscated-scripts.bat`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/build-with-project.sh` & `pyarmor-8.3.dev1/pyarmor/examples/build-with-project.sh`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/build-for-freeze.bat` & `pyarmor-8.3.dev1/pyarmor/examples/build-for-freeze.bat`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/README-ZH.md` & `pyarmor-8.3.dev1/pyarmor/examples/README-ZH.md`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/build-for-exe.bat` & `pyarmor-8.3.dev1/pyarmor/examples/build-for-exe.bat`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/helloworld/foo.py` & `pyarmor-8.3.dev1/pyarmor/examples/helloworld/foo.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/cx_Freeze/queens.py` & `pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/queens.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/cx_Freeze/setup.py` & `pyarmor-8.3.dev1/pyarmor/examples/cx_Freeze/setup.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/simple/queens.py` & `pyarmor-8.3.dev1/pyarmor/examples/simple/queens.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Arithmetic.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Arithmetic.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/With.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/With.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Lists.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Lists.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Tuples.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Tuples.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Instances.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Instances.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/systimes.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/systimes.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/clockres.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/clockres.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Lookups.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Lookups.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/CommandLine.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/CommandLine.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Numbers.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Numbers.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Imports.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Imports.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Setup.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Setup.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Exceptions.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Exceptions.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Dict.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Dict.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/pybench.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/pybench.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/NewInstances.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/NewInstances.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Calls.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Calls.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Strings.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Strings.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/pybench/Constructs.py` & `pyarmor-8.3.dev1/pyarmor/examples/pybench/Constructs.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/testmod/hello.py` & `pyarmor-8.3.dev1/pyarmor/examples/testmod/hello.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/testmod/queens.py` & `pyarmor-8.3.dev1/pyarmor/examples/testmod/queens.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/py2exe/queens.py` & `pyarmor-8.3.dev1/pyarmor/examples/py2exe/queens.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/examples/py2exe/setup.py` & `pyarmor-8.3.dev1/pyarmor/examples/py2exe/setup.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/polyfills/argparse.py` & `pyarmor-8.3.dev1/pyarmor/polyfills/argparse.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/helper/superuntime.py` & `pyarmor-8.3.dev1/pyarmor/helper/superuntime.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/helper/merge.py` & `pyarmor-8.3.dev1/pyarmor/helper/merge.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/helper/buildext.py` & `pyarmor-8.3.dev1/pyarmor/helper/buildext.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/helper/get_platform_name.py` & `pyarmor-8.3.dev1/pyarmor/helper/get_platform_name.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/helper/get_license_info.py` & `pyarmor-8.3.dev1/pyarmor/helper/get_license_info.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/helper/get_bind_key.py` & `pyarmor-8.3.dev1/pyarmor/helper/get_bind_key.py`

 * *Files identical despite different names*

## Comparing `pyarmor-8.2.dev2/src/helper/build_data_module.py` & `pyarmor-8.3.dev1/pyarmor/helper/build_data_module.py`

 * *Files identical despite different names*

