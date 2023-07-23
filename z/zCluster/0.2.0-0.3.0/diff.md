# Comparing `tmp/zCluster-0.2.0.tar.gz` & `tmp/zCluster-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zCluster-0.2.0.tar", last modified: Fri Nov 12 13:51:05 2021, max compression
+gzip compressed data, was "zCluster-0.3.0.tar", last modified: Sun Jul 23 13:53:57 2023, max compression
```

## Comparing `zCluster-0.2.0.tar` & `zCluster-0.3.0.tar`

### file list

```diff
@@ -1,116 +1,104 @@
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.383601 zCluster-0.2.0/
--rw-rw-r--   0 matty     (1000) matty     (1000)       84 2020-09-01 13:56:35.000000 zCluster-0.2.0/.gitattributes
--rw-r--r--   0 matty     (1000) matty     (1000)       53 2017-02-10 06:00:34.000000 zCluster-0.2.0/.kateproject
--rw-r--r--   0 matty     (1000) matty     (1000)    35147 2017-02-10 06:00:34.000000 zCluster-0.2.0/COPYING
--rw-rw-r--   0 matty     (1000) matty     (1000)     2028 2021-08-19 09:51:36.000000 zCluster-0.2.0/INSTALL.rst
--rw-rw-r--   0 matty     (1000) matty     (1000)      204 2021-08-19 09:58:51.000000 zCluster-0.2.0/MANIFEST.in
--rw-rw-r--   0 matty     (1000) matty     (1000)      476 2021-11-12 13:51:05.383601 zCluster-0.2.0/PKG-INFO
--rw-rw-r--   0 matty     (1000) matty     (1000)     2294 2021-11-12 13:29:41.000000 zCluster-0.2.0/README.rst
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.355602 zCluster-0.2.0/bin/
--rw-rw-r--   0 matty     (1000) matty     (1000)    34869 2021-11-04 15:13:17.000000 zCluster-0.2.0/bin/zCluster
--rw-rw-r--   0 matty     (1000) matty     (1000)    19806 2021-01-20 14:01:53.000000 zCluster-0.2.0/bin/zClusterBCG
--rw-rw-r--   0 matty     (1000) matty     (1000)    15662 2021-01-20 14:01:53.000000 zCluster-0.2.0/bin/zClusterComparisonPlot
--rw-rw-r--   0 matty     (1000) matty     (1000)    10468 2021-11-12 13:36:46.000000 zCluster-0.2.0/bin/zField
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.355602 zCluster-0.2.0/docs/
--rw-rw-r--   0 matty     (1000) matty     (1000)      634 2021-01-20 14:01:53.000000 zCluster-0.2.0/docs/Makefile
--rw-rw-r--   0 matty     (1000) matty     (1000)      671 2021-11-12 13:24:13.000000 zCluster-0.2.0/docs/commands.rst
--rw-rw-r--   0 matty     (1000) matty     (1000)     5627 2021-11-12 10:02:40.000000 zCluster-0.2.0/docs/conf.py
--rw-rw-r--   0 matty     (1000) matty     (1000)      586 2021-08-19 09:51:36.000000 zCluster-0.2.0/docs/index.rst
--rw-rw-r--   0 matty     (1000) matty     (1000)       89 2021-08-19 09:51:36.000000 zCluster-0.2.0/docs/install.rst
--rw-rw-r--   0 matty     (1000) matty     (1000)      583 2021-01-20 14:01:53.000000 zCluster-0.2.0/docs/reference.rst
--rw-rw-r--   0 matty     (1000) matty     (1000)      142 2021-08-19 09:51:36.000000 zCluster-0.2.0/docs/usage.rst
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.355602 zCluster-0.2.0/examples/
--rw-r--r--   0 matty     (1000) matty     (1000)     7643 2017-02-10 06:00:35.000000 zCluster-0.2.0/examples/400SDAll.csv
--rw-r--r--   0 matty     (1000) matty     (1000)      617 2017-02-10 06:00:35.000000 zCluster-0.2.0/examples/400SDSmall.csv
--rw-rw-r--   0 matty     (1000) matty     (1000)     1026 2021-08-19 09:51:36.000000 zCluster-0.2.0/examples/README_EXAMPLE.rst
--rw-rw-r--   0 matty     (1000) matty     (1000)       69 2021-08-19 09:59:20.000000 zCluster-0.2.0/pyproject.toml
--rw-rw-r--   0 matty     (1000) matty     (1000)       67 2021-08-19 09:58:05.000000 zCluster-0.2.0/requirements.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)      204 2021-11-12 13:51:05.383601 zCluster-0.2.0/setup.cfg
--rw-rw-r--   0 matty     (1000) matty     (1000)     1516 2021-08-19 11:45:58.000000 zCluster-0.2.0/setup.py
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.355602 zCluster-0.2.0/tests/
--rw-rw-r--   0 matty     (1000) matty     (1000)      636 2021-01-20 14:01:53.000000 zCluster-0.2.0/tests/tests.sh
--rw-rw-r--   0 matty     (1000) matty     (1000)    68611 2020-09-01 13:56:35.000000 zCluster-0.2.0/versioneer.py
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.383601 zCluster-0.2.0/zCluster/
--rw-rw-r--   0 matty     (1000) matty     (1000)    18962 2021-08-19 09:51:36.000000 zCluster-0.2.0/zCluster/PhotoRedshiftEngine.py
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.351602 zCluster-0.2.0/zCluster/SED/
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.359602 zCluster-0.2.0/zCluster/SED/BR07/
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/default_sed1.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/default_sed2.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/default_sed3.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/default_sed4.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/default_sed5.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/goods_sed1.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/goods_sed2.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/goods_sed3.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/goods_sed4.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/goods_sed5.dat
--rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/BR07/lrg1_sed1.dat
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.359602 zCluster-0.2.0/zCluster/SED/CWW/
--rw-r--r--   0 matty     (1000) matty     (1000)    27744 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/CWW/CWW_E_ext.sed
--rw-r--r--   0 matty     (1000) matty     (1000)    27744 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/CWW/CWW_Im_ext.sed
--rw-r--r--   0 matty     (1000) matty     (1000)    28672 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/CWW/CWW_Sbc_ext.sed
--rw-r--r--   0 matty     (1000) matty     (1000)    28672 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/CWW/CWW_Scd_ext.sed
--rw-------   0 matty     (1000) matty     (1000)    77885 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/CWW/SB2_kin.sed
--rw-------   0 matty     (1000) matty     (1000)    73743 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/CWW/SB3_kin.sed
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.363601 zCluster-0.2.0/zCluster/SED/EAZY_v1.0/
--rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed1.dat
--rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed2.dat
--rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed3.dat
--rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed4.dat
--rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed5.dat
--rw-r--r--   0 matty     (1000) matty     (1000)    36630 2017-02-10 06:00:36.000000 zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed6.dat
--rw-rw-r--   0 matty     (1000) matty     (1000)      297 2021-01-20 14:01:53.000000 zCluster-0.2.0/zCluster/__init__.py
--rw-rw-r--   0 matty     (1000) matty     (1000)      497 2021-11-12 13:51:05.383601 zCluster-0.2.0/zCluster/_version.py
--rw-rw-r--   0 matty     (1000) matty     (1000)    10794 2021-01-27 14:07:52.000000 zCluster-0.2.0/zCluster/catalogs.py
--rw-rw-r--   0 matty     (1000) matty     (1000)    26167 2021-11-04 15:18:04.000000 zCluster-0.2.0/zCluster/clusters.py
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.371601 zCluster-0.2.0/zCluster/data/
--rw-r-----   0 matty     (1000) matty     (1000) 10339200 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/data/redmapper_dr8_public_v5.10_catalog.fits
--rw-r--r--   0 matty     (1000) matty     (1000)  1622508 2017-04-20 07:47:07.000000 zCluster-0.2.0/zCluster/data/tau0p1Gyr_m62.20
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.383601 zCluster-0.2.0/zCluster/passbands/
--rw-r--r--   0 matty     (1000) matty     (1000)     1723 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/K_2MASS.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    10472 2018-04-12 09:49:23.000000 zCluster-0.2.0/zCluster/passbands/RSR-W1.EE.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)    14372 2018-04-12 09:49:23.000000 zCluster-0.2.0/zCluster/passbands/RSR-W2.EE.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)    66658 2018-04-12 09:49:23.000000 zCluster-0.2.0/zCluster/passbands/RSR-W3.EE.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)    66658 2018-04-12 09:49:23.000000 zCluster-0.2.0/zCluster/passbands/RSR-W4.EE.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)    39168 2019-03-20 17:29:07.000000 zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_H.dat
--rw-rw-r--   0 matty     (1000) matty     (1000)    50048 2019-03-20 17:29:07.000000 zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_J.dat
--rw-rw-r--   0 matty     (1000) matty     (1000)    41344 2019-03-20 17:29:13.000000 zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Ks.dat
--rw-rw-r--   0 matty     (1000) matty     (1000)    46341 2019-03-20 17:29:07.000000 zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Y.dat
--rw-rw-r--   0 matty     (1000) matty     (1000)   176418 2019-03-20 17:29:07.000000 zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Z.dat
--rw-rw-r--   0 matty     (1000) matty     (1000)    21744 2019-02-21 15:14:44.000000 zCluster-0.2.0/zCluster/passbands/decam.g.am1p4.dat.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)    21744 2019-02-21 15:15:04.000000 zCluster-0.2.0/zCluster/passbands/decam.r.am1p4.dat.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)    21744 2019-02-21 15:15:09.000000 zCluster-0.2.0/zCluster/passbands/decam.z.am1p4.dat.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.2.0/zCluster/passbands/gDES.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.2.0/zCluster/passbands/gPS1.res
--rw-r--r--   0 matty     (1000) matty     (1000)     1298 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/g_CFHTLS.res
--rw-r--r--   0 matty     (1000) matty     (1000)      491 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/g_SDSS.res
--rw-r--r--   0 matty     (1000) matty     (1000)     1320 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/g_SDSS3.res
--rw-r--r--   0 matty     (1000) matty     (1000)      955 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/i2_CFHTLS.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.2.0/zCluster/passbands/iDES.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.2.0/zCluster/passbands/iPS1.res
--rw-r--r--   0 matty     (1000) matty     (1000)     1385 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/i_CFHTLS.res
--rw-r--r--   0 matty     (1000) matty     (1000)      491 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/i_SDSS.res
--rw-r--r--   0 matty     (1000) matty     (1000)     1318 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/i_SDSS3.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.2.0/zCluster/passbands/rDES.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.2.0/zCluster/passbands/rPS1.res
--rw-r--r--   0 matty     (1000) matty     (1000)     1163 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/r_CFHTLS.res
--rw-r--r--   0 matty     (1000) matty     (1000)      512 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/r_SDSS.res
--rw-r--r--   0 matty     (1000) matty     (1000)     1102 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/r_SDSS3.res
--rw-r--r--   0 matty     (1000) matty     (1000)     1335 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/u_CFHTLS.res
--rw-r--r--   0 matty     (1000) matty     (1000)      426 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/u_SDSS.res
--rw-r--r--   0 matty     (1000) matty     (1000)      691 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/u_SDSS3.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.2.0/zCluster/passbands/yDES.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.2.0/zCluster/passbands/yPS1.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.2.0/zCluster/passbands/zDES.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.2.0/zCluster/passbands/zPS1.res
--rw-r--r--   0 matty     (1000) matty     (1000)     1345 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/z_CFHTLS.res
--rw-r--r--   0 matty     (1000) matty     (1000)      602 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/z_SDSS.res
--rw-r--r--   0 matty     (1000) matty     (1000)     2089 2017-02-10 06:00:37.000000 zCluster-0.2.0/zCluster/passbands/z_SDSS3.res
--rw-rw-r--   0 matty     (1000) matty     (1000)    74259 2021-08-19 09:51:36.000000 zCluster-0.2.0/zCluster/retrievers.py
--rw-rw-r--   0 matty     (1000) matty     (1000)     4958 2020-09-01 13:56:35.000000 zCluster-0.2.0/zCluster/zClusterCython.pyx
-drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2021-11-12 13:51:05.355602 zCluster-0.2.0/zCluster.egg-info/
--rw-rw-r--   0 matty     (1000) matty     (1000)      476 2021-11-12 13:51:05.000000 zCluster-0.2.0/zCluster.egg-info/PKG-INFO
--rw-rw-r--   0 matty     (1000) matty     (1000)     2949 2021-11-12 13:51:05.000000 zCluster-0.2.0/zCluster.egg-info/SOURCES.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)        1 2021-11-12 13:51:05.000000 zCluster-0.2.0/zCluster.egg-info/dependency_links.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)       83 2021-11-12 13:51:05.000000 zCluster-0.2.0/zCluster.egg-info/requires.txt
--rw-rw-r--   0 matty     (1000) matty     (1000)       24 2021-11-12 13:51:05.000000 zCluster-0.2.0/zCluster.egg-info/top_level.txt
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.995848 zCluster-0.3.0/
+-rw-r--r--   0 matty     (1000) matty     (1000)    35147 2017-02-10 06:00:34.000000 zCluster-0.3.0/COPYING
+-rw-rw-r--   0 matty     (1000) matty     (1000)     1935 2023-07-23 13:47:53.000000 zCluster-0.3.0/INSTALL.rst
+-rw-rw-r--   0 matty     (1000) matty     (1000)      204 2021-08-19 09:58:51.000000 zCluster-0.3.0/MANIFEST.in
+-rw-rw-r--   0 matty     (1000) matty     (1000)      443 2023-07-23 13:53:56.995848 zCluster-0.3.0/PKG-INFO
+-rw-rw-r--   0 matty     (1000) matty     (1000)     2296 2023-07-23 13:48:26.000000 zCluster-0.3.0/README.rst
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.963848 zCluster-0.3.0/bin/
+-rw-rw-r--   0 matty     (1000) matty     (1000)    36226 2023-07-23 13:47:53.000000 zCluster-0.3.0/bin/zCluster
+-rw-rw-r--   0 matty     (1000) matty     (1000)    19806 2021-01-20 14:01:53.000000 zCluster-0.3.0/bin/zClusterBCG
+-rw-rw-r--   0 matty     (1000) matty     (1000)    15662 2021-01-20 14:01:53.000000 zCluster-0.3.0/bin/zClusterComparisonPlot
+-rw-rw-r--   0 matty     (1000) matty     (1000)    12092 2022-04-26 07:44:02.000000 zCluster-0.3.0/bin/zField
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.963848 zCluster-0.3.0/examples/
+-rw-r--r--   0 matty     (1000) matty     (1000)     7643 2017-02-10 06:00:35.000000 zCluster-0.3.0/examples/400SDAll.csv
+-rw-r--r--   0 matty     (1000) matty     (1000)      617 2017-02-10 06:00:35.000000 zCluster-0.3.0/examples/400SDSmall.csv
+-rw-rw-r--   0 matty     (1000) matty     (1000)     1026 2021-08-19 09:51:36.000000 zCluster-0.3.0/examples/README_EXAMPLE.rst
+-rw-rw-r--   0 matty     (1000) matty     (1000)       72 2023-07-23 13:47:53.000000 zCluster-0.3.0/pyproject.toml
+-rw-rw-r--   0 matty     (1000) matty     (1000)      204 2023-07-23 13:53:56.995848 zCluster-0.3.0/setup.cfg
+-rw-rw-r--   0 matty     (1000) matty     (1000)     1520 2023-07-23 13:47:53.000000 zCluster-0.3.0/setup.py
+-rw-rw-r--   0 matty     (1000) matty     (1000)    68611 2020-09-01 13:56:35.000000 zCluster-0.3.0/versioneer.py
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.995848 zCluster-0.3.0/zCluster/
+-rw-rw-r--   0 matty     (1000) matty     (1000)    22167 2023-07-23 13:47:53.000000 zCluster-0.3.0/zCluster/PhotoRedshiftEngine.py
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.963848 zCluster-0.3.0/zCluster/SED/
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.971848 zCluster-0.3.0/zCluster/SED/BR07/
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/default_sed1.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/default_sed2.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/default_sed3.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/default_sed4.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/default_sed5.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/goods_sed1.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/goods_sed2.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/goods_sed3.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/goods_sed4.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/goods_sed5.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)   123196 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/BR07/lrg1_sed1.dat
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.975848 zCluster-0.3.0/zCluster/SED/CWW/
+-rw-r--r--   0 matty     (1000) matty     (1000)    27744 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/CWW/CWW_E_ext.sed
+-rw-r--r--   0 matty     (1000) matty     (1000)    27744 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/CWW/CWW_Im_ext.sed
+-rw-r--r--   0 matty     (1000) matty     (1000)    28672 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/CWW/CWW_Sbc_ext.sed
+-rw-r--r--   0 matty     (1000) matty     (1000)    28672 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/CWW/CWW_Scd_ext.sed
+-rw-------   0 matty     (1000) matty     (1000)    77885 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/CWW/SB2_kin.sed
+-rw-------   0 matty     (1000) matty     (1000)    73743 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/CWW/SB3_kin.sed
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.975848 zCluster-0.3.0/zCluster/SED/EAZY_v1.0/
+-rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed1.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed2.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed3.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed4.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)    40293 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed5.dat
+-rw-r--r--   0 matty     (1000) matty     (1000)    36630 2017-02-10 06:00:36.000000 zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed6.dat
+-rw-rw-r--   0 matty     (1000) matty     (1000)      312 2022-03-30 13:22:56.000000 zCluster-0.3.0/zCluster/__init__.py
+-rw-rw-r--   0 matty     (1000) matty     (1000)      497 2023-07-23 13:53:56.995848 zCluster-0.3.0/zCluster/_version.py
+-rw-rw-r--   0 matty     (1000) matty     (1000)    10794 2021-01-27 14:07:52.000000 zCluster-0.3.0/zCluster/catalogs.py
+-rw-rw-r--   0 matty     (1000) matty     (1000)    29888 2023-07-23 13:47:53.000000 zCluster-0.3.0/zCluster/clusters.py
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.983848 zCluster-0.3.0/zCluster/data/
+-rw-r-----   0 matty     (1000) matty     (1000) 10339200 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/data/redmapper_dr8_public_v5.10_catalog.fits
+-rw-r--r--   0 matty     (1000) matty     (1000)  1622508 2017-04-20 07:47:07.000000 zCluster-0.3.0/zCluster/data/tau0p1Gyr_m62.20
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.995848 zCluster-0.3.0/zCluster/passbands/
+-rw-r--r--   0 matty     (1000) matty     (1000)     1723 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/K_2MASS.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    10472 2018-04-12 09:49:23.000000 zCluster-0.3.0/zCluster/passbands/RSR-W1.EE.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)    14372 2018-04-12 09:49:23.000000 zCluster-0.3.0/zCluster/passbands/RSR-W2.EE.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)    66658 2018-04-12 09:49:23.000000 zCluster-0.3.0/zCluster/passbands/RSR-W3.EE.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)    66658 2018-04-12 09:49:23.000000 zCluster-0.3.0/zCluster/passbands/RSR-W4.EE.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)    39168 2019-03-20 17:29:07.000000 zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_H.dat
+-rw-rw-r--   0 matty     (1000) matty     (1000)    50048 2019-03-20 17:29:07.000000 zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_J.dat
+-rw-rw-r--   0 matty     (1000) matty     (1000)    41344 2019-03-20 17:29:13.000000 zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Ks.dat
+-rw-rw-r--   0 matty     (1000) matty     (1000)    46341 2019-03-20 17:29:07.000000 zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Y.dat
+-rw-rw-r--   0 matty     (1000) matty     (1000)   176418 2019-03-20 17:29:07.000000 zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Z.dat
+-rw-rw-r--   0 matty     (1000) matty     (1000)    21744 2019-02-21 15:14:44.000000 zCluster-0.3.0/zCluster/passbands/decam.g.am1p4.dat.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)    21743 2023-03-23 13:15:34.000000 zCluster-0.3.0/zCluster/passbands/decam.i.am1p4.dat.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)    21744 2019-02-21 15:15:04.000000 zCluster-0.3.0/zCluster/passbands/decam.r.am1p4.dat.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)    21744 2019-02-21 15:15:09.000000 zCluster-0.3.0/zCluster/passbands/decam.z.am1p4.dat.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.3.0/zCluster/passbands/gDES.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.3.0/zCluster/passbands/gPS1.res
+-rw-r--r--   0 matty     (1000) matty     (1000)     1298 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/g_CFHTLS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)      491 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/g_SDSS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)     1320 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/g_SDSS3.res
+-rw-r--r--   0 matty     (1000) matty     (1000)      955 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/i2_CFHTLS.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.3.0/zCluster/passbands/iDES.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.3.0/zCluster/passbands/iPS1.res
+-rw-r--r--   0 matty     (1000) matty     (1000)     1385 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/i_CFHTLS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)      491 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/i_SDSS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)     1318 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/i_SDSS3.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.3.0/zCluster/passbands/rDES.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.3.0/zCluster/passbands/rPS1.res
+-rw-r--r--   0 matty     (1000) matty     (1000)     1163 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/r_CFHTLS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)      512 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/r_SDSS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)     1102 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/r_SDSS3.res
+-rw-r--r--   0 matty     (1000) matty     (1000)     1335 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/u_CFHTLS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)      426 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/u_SDSS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)      691 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/u_SDSS3.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.3.0/zCluster/passbands/yDES.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.3.0/zCluster/passbands/yPS1.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    26139 2018-01-25 11:57:26.000000 zCluster-0.3.0/zCluster/passbands/zDES.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    12358 2018-11-07 14:56:52.000000 zCluster-0.3.0/zCluster/passbands/zPS1.res
+-rw-r--r--   0 matty     (1000) matty     (1000)     1345 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/z_CFHTLS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)      602 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/z_SDSS.res
+-rw-r--r--   0 matty     (1000) matty     (1000)     2089 2017-02-10 06:00:37.000000 zCluster-0.3.0/zCluster/passbands/z_SDSS3.res
+-rw-rw-r--   0 matty     (1000) matty     (1000)    77488 2023-07-23 13:47:53.000000 zCluster-0.3.0/zCluster/retrievers.py
+-rw-rw-r--   0 matty     (1000) matty     (1000)    12567 2022-03-30 13:22:56.000000 zCluster-0.3.0/zCluster/stellarmass.py
+drwxrwxr-x   0 matty     (1000) matty     (1000)        0 2023-07-23 13:53:56.967848 zCluster-0.3.0/zCluster.egg-info/
+-rw-rw-r--   0 matty     (1000) matty     (1000)      443 2023-07-23 13:53:56.000000 zCluster-0.3.0/zCluster.egg-info/PKG-INFO
+-rw-rw-r--   0 matty     (1000) matty     (1000)     2815 2023-07-23 13:53:56.000000 zCluster-0.3.0/zCluster.egg-info/SOURCES.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)        1 2023-07-23 13:53:56.000000 zCluster-0.3.0/zCluster.egg-info/dependency_links.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)       76 2023-07-23 13:53:56.000000 zCluster-0.3.0/zCluster.egg-info/requires.txt
+-rw-rw-r--   0 matty     (1000) matty     (1000)        9 2023-07-23 13:53:56.000000 zCluster-0.3.0/zCluster.egg-info/top_level.txt
```

### Comparing `zCluster-0.2.0/COPYING` & `zCluster-0.3.0/COPYING`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/INSTALL.rst` & `zCluster-0.3.0/INSTALL.rst`

 * *Files 5% similar despite different names*

```diff
@@ -24,15 +24,14 @@
 
 The latest tagged version of **zCluster** can be installed using ``pip``:
     
 .. code-block::
 
    pip install zCluster
 
-Note that you will need to have ``cython`` and ``numpy`` installed already (for the moment).
 Other dependencies will be installed by ``pip``.
 
 You may also install using the standard ``setup.py`` script, e.g., as root:
 
 .. code-block::
 
    sudo python setup.py install
```

### Comparing `zCluster-0.2.0/README.rst` & `zCluster-0.3.0/README.rst`

 * *Files 10% similar despite different names*

```diff
@@ -14,15 +14,15 @@
   
 **zCluster** has built-in support for querying large photometric surveys - currently:
 
 * SDSS (DR7 - DR12)
 * SDSS Stripe 82 (from SDSS DR7)
 * CFHTLenS
 * PS1 (DR2)
-* DECaLS (DR8, DR9)
+* DECaLS (DR8 - DR10)
 * DES (DR1, DR2 and Y3 internal)
 * KiDS (DR4)
 
 For details of the algorithm, its performance, and the output of the code, refer to 
 `Hilton et al. (2018) <https://ui.adsabs.harvard.edu/abs/2018ApJS..235...20H/abstract>`_, which presents
 results based on SDSS, S82, and CFHTLenS, and/or 
 `Hilton et al. (2021) <https://ui.adsabs.harvard.edu/abs/2021ApJS..253....3H/abstract>`_, which presents
```

### Comparing `zCluster-0.2.0/bin/zCluster` & `zCluster-0.3.0/bin/zCluster`

 * *Files 8% similar despite different names*

```diff
@@ -143,18 +143,19 @@
         leg=plt.legend(loc = 'upper right', numpoints = 1) 
         leg.draw_frame(False)
         plt.title("%s (z = %.2f)" % (objName.replace("_", " "), result['z'])) 
         plt.savefig(plotsDir+os.path.sep+"pz_"+objName.replace(" ", "_")+".pdf")
         plt.close()
 
 #-------------------------------------------------------------------------------------------------------------
-def runOnCatalog(catalog, retriever, retrieverOptions, photoRedshiftEngine, outDir, zPriorMin,
-                 zPriorMax, weightsType, maxRMpc, zMethod, bckCatalogFileName, bckAreaDeg2,
-                 maskPath = None, writeGalaxyCatalogs = False, writeDensityMaps = False, writePlots = False, 
-                 rank = 0, zDebias = None, fitZPOffsets = False, maxIter = 5, minBackgroundAreaMpc2 = 11):
+def runOnCatalog(catalog, retriever, retrieverOptions, photoRedshiftEngine, outDir, zPriorMin,\
+                 zPriorMax, weightsType, maxRMpc, zMethod, bckCatalogFileName, bckAreaDeg2,\
+                 maskPath = None, writeGalaxyCatalogs = False, writeDensityMaps = False, writePlots = False,\
+                 rank = 0, zDebias = None, fitZPOffsets = False, maxIter = 5, minBackgroundAreaMpc2 = 11,\
+                 fetchAndCacheOnly = False):
     """Runs zCluster algorithm on each object in catalog.
     
     """
     
     # Now using sqlite database for storage, rather than loads of .pickle files (filesystem friendly)
     # We're only storing final results in here - if the user wants to see n(z) later, they can use -n option 
     # to rerun specific clusters
@@ -206,14 +207,16 @@
             globalMatches=cGlobal.fetchall()
         else:
             globalMatches=[]
         if len(matches) == 0 and len(globalMatches) == 0:
             stuff="retry"
             while stuff == "retry":
                 stuff=retriever(obj['RADeg'], obj['decDeg'], optionsDict = retrieverOptions)
+            if fetchAndCacheOnly == True:
+                continue
             galaxyCatalog=stuff
             # Default values... will get filled if sucessful
             obj['origRADeg']=obj['RADeg']
             obj['origDecDeg']=obj['decDeg']
             obj['offsetArcmin']=-99
             obj['offsetMpc']=-99
             obj['z']=-99
@@ -413,14 +416,20 @@
                         default = 'odds')
     parser.add_argument("-i", "--max-iter", dest="maxIter", help="Maximum number of iterations for finding\
                         the cluster redshift and optical position based on projected density map (default: 1).",
                         default = 1, type = int)
     parser.add_argument("-c", "--cachedir", dest="cacheDir", default = None, help="Cache directory location\
                         (default: $HOME/.zCluster/cache). Downloaded photometric catalogs will be stored\
                         here.")
+    parser.add_argument("-F", "--fetch-only-and-cache", dest="fetchAndCacheOnly",
+                        help="Only fetch and cache galaxy catalogs - i.e., do not run photo-z estimation.\
+                        This is useful if you are running on a compute cluster where compute nodes do\
+                        not have internet access (allows a first run with -F, followed by a second run\
+                        under MPI to compute the photo-zs in parallel).",
+                        default = False, action = "store_true")
     parser.add_argument("-M", "--mpi", dest="MPIEnabled", action="store_true", help="Enable MPI. If you\
                         want to use this, run zCluster using something like: mpirun --np 4 zCluster ...",
                         default = False)
     parser.add_argument("-e", "--max-mag-error", dest="maxMagError", help="Maximum acceptable\
                         photometric error (in magnitudes; default: 0.25).", default = 0.25)
     parser.add_argument("-E", "--photometric-zero-point-error", dest="ZPError", type = float, 
                         help="Global photometric zero point uncertainty in magnitudes, applied to all bands\
@@ -431,16 +440,19 @@
                         for magnitude zero point offsets. These will then be applied when estimating galaxy\
                         photometric redshifts.", 
                         default = False, action = "store_true")
     parser.add_argument("-z", "--z-prior-min", dest="zPriorMin", help="Set minimum redshift of prior.",
                         default = None)
     parser.add_argument("-Z", "--z-prior-max", dest="zPriorMax", help="Set maximum redshift of prior.",
                         default = None)
-    parser.add_argument("-b", "--brighter-absmag-cut", dest="absMagCut", help="Set bright absolute magnitude cut.",
-                        default = -24.)
+    parser.add_argument("-b", "--absmag-cut", dest="absMagCut",
+                        help="Set absolute (r-band) magnitude cut to use in magnitude-based prior. If a single number\
+                        is given, p(z) for objects brighter than this limit will be set to 0. If a\
+                        list of numbers is given (e.g., [-15,-24]), p(z) will be set to 0\
+                        for objects outside of the absolute magnitude range.", default = -24.)
     parser.add_argument("-n", "--name", dest="name", help="Find photo-z of only the named cluster in the catalog.")
     parser.add_argument("-t", "--templates-directory", dest="templatesDir", help="Specify a directory containing\
                         a custom set of spectral templates.",  default = None)
     parser.add_argument("-d", "--write-density-maps", dest="writeDensityMaps", action="store_true", 
                         help="Write out a .fits image projected density map (within delta z = +/- 0.1 of the best\
                         fit redshift) for each cluster.", default = False)
     parser.add_argument("-W", "--write-galaxy-catalogs", dest="writeGalaxyCatalogs", action="store_true", 
@@ -481,15 +493,22 @@
     cacheDir=args.cacheDir
     weightsType=args.weightsType
     maxRMpc=float(args.maxRMpc)
     method=args.algorithm
     MPIEnabled=args.MPIEnabled
     maxMagError=float(args.maxMagError)
     #magsBrighterMStarCut=float(args.magsBrighterMStarCut)
-    absMagCut=float(args.absMagCut)
+    try:
+        absMagCut=float(args.absMagCut)
+    except:
+        vals=args.absMagCut.replace("[", "").replace("]", "").split(",")
+        if len(vals) != 2:
+            raise Exception("If you want to give a range for --absmag-cut, write as e.g. [-15,-23]")
+        absMagCut=[float(vals[0]), float(vals[1])]
+        absMagCut.sort() # Bright mag comes first
     writeGalaxyCatalogs=args.writeGalaxyCatalogs
     writePlots=args.writePlots
     maskPath=args.mask
     ZPError=args.ZPError
     maxIter=args.maxIter
     
     update_rcParams()
@@ -651,15 +670,16 @@
             catalog=[]
 
     catalog=runOnCatalog(catalog, retriever, retrieverOptions, photoRedshiftEngine, outDir,
                          zPriorMin, zPriorMax, weightsType, maxRMpc, method, bckCatalogFileName, bckAreaDeg2,
                          maskPath = maskPath, writeGalaxyCatalogs = writeGalaxyCatalogs, 
                          writeDensityMaps = args.writeDensityMaps, writePlots = writePlots, 
                          rank = rank, zDebias = zDebias, fitZPOffsets = args.fitZPOffsets,
-                         maxIter = maxIter, minBackgroundAreaMpc2 = args.minBackgroundAreaMpc2)
+                         maxIter = maxIter, minBackgroundAreaMpc2 = args.minBackgroundAreaMpc2,
+                         fetchAndCacheOnly = args.fetchAndCacheOnly)
     
     # If running under MPI, gather everything back together
     # Rank 0 process will continue with plots
     if MPIEnabled == True:
         if rank == 0:
             wholeCatalog=catalog
             for i in range(1, size):
```

### Comparing `zCluster-0.2.0/bin/zClusterBCG` & `zCluster-0.3.0/bin/zClusterBCG`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/bin/zClusterComparisonPlot` & `zCluster-0.3.0/bin/zClusterComparisonPlot`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/bin/zField` & `zCluster-0.3.0/bin/zField`

 * *Files 14% similar despite different names*

```diff
@@ -67,40 +67,52 @@
                         help="Write out a DS9 .reg file corresponding to the fetched photometric catalog.", default = False)
     parser.add_argument("-ErrMap", "--make-error-map", dest="ErrMap", action="store_true",
                         help="Estimate and output uncertainties on the projected density map and associated\
                         summary statistics (warning: extremely slow).""", default = False)
     parser.add_argument("-MC", "--monte-carlo-samples", dest="MC",
                         help="Number of Monte Carlo samples to use when estimating uncertainties on the\
                         projected galaxy density map", type = int, default = 1000)
+    parser.add_argument("-S", "--stellar-mass-model-dir", dest="stellarMassModelDir", default = None,
+                        help = "If given, estimate stellar masses for galaxies using the (for now) BC03-format\
+                        stellar population models in the given directory. If -z (--redshift) is given, stellar\
+                        masses will be estimated at the given redshift. Otherwise, the stellar masses will be\
+                        estimated at the maximum likelihood redshift of each galaxy (although that isn't\
+                        actually implemented yet).")
 
     return parser
 
 #------------------------------------------------------------------------------------------------------------
 start=time.time()
 if __name__ == '__main__':
 
     parser=makeParser()
     args=parser.parse_args()
 
     RADeg=args.RADeg
     decDeg=args.decDeg
-    maxRDeg=args.maxRDeg
+    maxRDeg=float(args.maxRDeg)
     ZPError=args.ZPError
     templatesDir=args.templatesDir
-    absMagCut=args.absMagCut
+    absMagCut=float(args.absMagCut)
     database=args.database
-    maxMagError=args.maxMagError
+    maxMagError=float(args.maxMagError)
     fitZPOffsets=args.fitZPOffsets
     cacheDir=args.cacheDir
     writeDensityMaps=args.writeDensityMaps
     z=args.z
     dz=args.dz
     ErrMap=args.ErrMap
     MC=args.MC
 
+    # Memory saving - we don't care about carrying around p(z) if we're not writing density maps
+    if args.writeDensityMaps == False:
+        returnPZ=False
+    else:
+        returnPZ=True
+
     # Set-up cache
     if cacheDir is not None:
         if os.path.exists(cacheDir) == False:
             os.makedirs(cacheDir, exist_ok=True)
     else:
         if os.path.exists(retrievers.CACHE_DIR) == False:
                 os.makedirs(retrievers.CACHE_DIR, exist_ok = True)
@@ -128,28 +140,37 @@
 
     galaxyCatalog=retriever(RADeg, decDeg, halfBoxSizeDeg = maxRDeg, optionsDict = retrieverOptions)
 
     if galaxyCatalog is None:
         print("No galaxies found at the given position.")
         sys.exit()
     
-    photoRedshiftEngine=PhotoRedshiftEngine.PhotoRedshiftEngine(absMagCut, ZPError = ZPError, passbandSet = passbandSet,
-                                                                templatesDir = templatesDir, ZPOffsets = ZPOffsets)
+    photoRedshiftEngine=PhotoRedshiftEngine.PhotoRedshiftEngine(absMagCut, ZPError = ZPError,
+                                                                passbandSet = passbandSet,
+                                                                templatesDir = templatesDir,
+                                                                ZPOffsets = ZPOffsets)
     bands=photoRedshiftEngine.bands
     bandErrs=[]
     for b in bands:
         bandErrs.append(b+"Err")
     bands=bands+bandErrs
 
     if fitZPOffsets == True:
         photoRedshiftEngine.calcZeroPointOffsets(galaxyCatalog)
-    photoRedshiftEngine.calcPhotoRedshifts(galaxyCatalog, calcMLRedshiftAndOdds = True)
+    photoRedshiftEngine.calcPhotoRedshifts(galaxyCatalog, calcMLRedshiftAndOdds = True, returnPZ = returnPZ)
     
+    # Optional stellar mass estimates
+    if args.stellarMassModelDir is not None:
+        photoRedshiftEngine.estimateStellarMasses(galaxyCatalog, args.stellarMassModelDir, z = z)
+
+    # Write catalog and region file
     wantedKeys=['id', 'RADeg', 'decDeg', 'zPhot', 'odds']
-    wantedKeys=np.concatenate((wantedKeys,bands))
+    if args.stellarMassModelDir is not None:
+        wantedKeys.append('log10StellarMass')
+    wantedKeys=wantedKeys+bands
     tab=atpy.Table()
     for key in wantedKeys:
         arr=[]
         for gobj in galaxyCatalog:
             try:
                 arr.append(gobj[key])
             except:
@@ -161,17 +182,21 @@
         catalogs.catalog2DS9(galaxyCatalog, args.outDir+os.path.sep+"%s_%s.reg" % (database, outputLabel),
                                  idKeyToUse = 'id', addInfo = [{'key': 'r', 'fmt': '%.3f'}, {'key': 'zPhot', 'fmt': '%.2f'}])
         
     if writeDensityMaps == True:
         if z is None:
             raise Exception("Redshift needs to be specified using -z when using the -d option")
         else:
-            dMapDict = clusters.makeDensityMap(RADeg, decDeg, galaxyCatalog, z, dz, rMaxMpc = 1.5)
-            astImages.saveFITS(args.outDir+os.path.sep+"densityMap_z%.2f_%s.fits" % (z, outputLabel),
-                               dMapDict['map'], dMapDict['wcs'])
+            sizeMpc=astCalc.da(z)*np.tan(np.radians(maxRDeg))*2
+            dMapDict=clusters.makeDensityMap(RADeg, decDeg, galaxyCatalog, z, dz, sizeMpc = sizeMpc,
+                                             outFITSFileName = args.outDir+os.path.sep+"densityMap_z%.2f_%s.fits" % (z, outputLabel),
+                                             outPlotFileName = args.outDir+os.path.sep+"densityMap_z%.2f_%s.png" % (z, outputLabel))
+            #astImages.saveFITS(args.outDir+os.path.sep+"densityMap_z%.2f_%s.fits" % (z, outputLabel),
+                               #dMapDict['map'], dMapDict['wcs'])
+
             
     # Estimate errors for density map, CS and A
     if ErrMap == True:
         print(">>> Estimating galaxy density error map ...")
         AErr = [] ; CSErr = [] ; MapErr=[]
         newGalaxyCatalog=galaxyCatalog
         for monteCarlo in range(0,MC):
@@ -180,23 +205,23 @@
                     res = g.get(i, None)
                     if res and i[-3:]!="Err" and g[i]!=99:
                         g[i]=g[i]+ np.random.normal(0,g[i+'Err']) # Add Gaussian noise to photmetry of each galaxy
             
             if fitZPOffsets == True:
                 photoRedshiftEngine.calcZeroPointOffsets(newGalaxyCatalog)
             photoRedshiftEngine.calcPhotoRedshifts(newGalaxyCatalog, calcMLRedshiftAndOdds = True) # Recompute photo-z's
-            
-            dMapDictwerr = clusters.makeDensityMap(RADeg, decDeg, newGalaxyCatalog, z, dz, rMaxMpc = 1.5) # Make new density maps with added noise
+            sizeMpc=astCalc.da(z)*np.tan(np.radians(maxRDeg))*2
+            dMapDictwerr = clusters.makeDensityMap(RADeg, decDeg, newGalaxyCatalog, z, dz, sizeMpc = sizeMpc) # Make new density maps with added noise
             CSErr.append(dMapDictwerr['CS'])
             AErr.append(dMapDictwerr['A'])
             MapErr.append(dMapDictwerr['map'])
         AError=np.percentile(AErr, 68.3) # 68th percentile as error
         CSError=np.percentile(CSErr, 68.3)
         MapError=np.percentile(MapErr,68.3, axis=0)
         astImages.saveFITS(args.outDir+os.path.sep+"errorMap_z%.2f_%s.fits" % (z, outputLabel),
                                MapError, dMapDict['wcs'])
         print(">>> CS:\t"+str(dMapDict['CS'])+" +- "+str(CSError)+"\n A:\t"+str(dMapDict['A'])+" +- "+str(AError))
         
     # We may as well print some stats
     print(">>> Summary:")
     print("    N = %d" %  (len(tab['zPhot'])))
-    print(">>> Total time: {:.1g} minutes".format((time.time()-start)/60.))
+    print(">>> Total time: %.1f sec" % (time.time()-start))
```

### Comparing `zCluster-0.2.0/examples/400SDAll.csv` & `zCluster-0.3.0/examples/400SDAll.csv`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/examples/400SDSmall.csv` & `zCluster-0.3.0/examples/400SDSmall.csv`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/examples/README_EXAMPLE.rst` & `zCluster-0.3.0/examples/README_EXAMPLE.rst`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/setup.py` & `zCluster-0.3.0/setup.py`

 * *Files 7% similar despite different names*

```diff
@@ -2,20 +2,20 @@
 
 import os
 import glob
 from setuptools import setup
 from setuptools import Extension
 from setuptools.command.install import install
 import stat
-from Cython.Distutils import build_ext
+#from Cython.Distutils import build_ext
 import numpy
 import versioneer
 
 cmdclass=versioneer.get_cmdclass()
-cmdclass['build_ext']=build_ext
+#cmdclass['build_ext']=build_ext
 
 setup(name='zCluster',
       version=versioneer.get_version(),
       cmdclass=cmdclass,
       url="https://github.com/ACTCollaboration/zCluster",
       author='Matt Hilton + zCluster contributors',
       author_email='matt.hilton@mykolab.com',
@@ -23,16 +23,16 @@
       description='A code for measuring galaxy cluster photometric redshifts.',
       long_description="""A code for measuring galaxy cluster photometric redshifts. Runs on both large scale
       public survey data (e.g., SDSS) and user-supplied photometric catalogs.""",
       packages=['zCluster'],
       package_data={'zCluster': ['data/*', 'SED/CWW/*', 'SED/BR07/*', 'SED/EAZY_v1.0/*', 
                                  'passbands/*']},
       scripts=['bin/zCluster', 'bin/zField', 'bin/zClusterBCG', 'bin/zClusterComparisonPlot'],
-      ext_modules=[Extension("zClusterCython", ["zCluster/zClusterCython.pyx"], include_dirs=[numpy.get_include()])],
+      #ext_modules=[Extension("zClusterCython", ["zCluster/zClusterCython.pyx"], include_dirs=[numpy.get_include()])],
       install_requires=["astropy >= 4.0",
                         "numpy >= 1.19",
                         "matplotlib >= 2.0",
                         "astLib >= 0.11.7",
                         "scipy >= 1.0",
-                        "cython",
+                        #"cython",
                         "requests"]
 )
```

### Comparing `zCluster-0.2.0/versioneer.py` & `zCluster-0.3.0/versioneer.py`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/PhotoRedshiftEngine.py` & `zCluster-0.3.0/zCluster/PhotoRedshiftEngine.py`

 * *Files 10% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 This module contains a class for estimating galaxy photometric redshifts using a template fitting method.
 
 """
 
 import os
 import numpy as np
 import zCluster
+from zCluster import stellarmass as sm
 from astLib import *
 from scipy import stats
 from scipy import interpolate
 from pkg_resources import resource_filename
 import string
 import glob
 import pickle
@@ -23,16 +24,18 @@
     """
     
     def __init__(self, absMagCut, passbandSet = 'SDSS+Ks', zMin = 0.01, zMax = 3.0, zStep = 0.01, 
                  ZPError = 0.0, ZPOffsets = None, templatesDir = None):
         """Sets up the stuff we would otherwise calculate every time, i.e., the templates.
         
         """
-                                
-        # Redshift grid on which to calculate p(z)
+
+        if zStep < 0:
+            print("... WARNING: zStep was negative - forced to be positive")
+            zStep=abs(zStep)
         self.zRange=np.linspace(zMin, zMax, int(((zMax+zStep)-zMin)/zStep))
 
         # Set up passbands
         passbandsDir=zCluster.__path__[0]+os.path.sep+"passbands"+os.path.sep
         self.passbandsList=[]
         if passbandSet == 'SDSS+Ks':
             self.bands=['u', 'g', 'r', 'i', 'z', 'Ks']
@@ -71,15 +74,16 @@
             for band in self.bands:
                 if band[0] != "w":
                     self.passbandsList.append(astSED.Passband(passbandsDir+band+"DES.res"))
                 else:
                     self.passbandsList.append(astSED.Passband(passbandsDir+"RSR-%s.EE.txt" % (band.upper()), inputUnits = "microns"))
         elif passbandSet == 'DECaLS':
             # NOTE: WISE passbands from here: http://wise2.ipac.caltech.edu/docs/release/allsky/expsup/sec4_4h.html
-            self.bands=['g', 'r', 'z', "w1", "w2"]
+            # DR10 adds i-band
+            self.bands=['g', 'r', 'i', 'z', "w1", "w2"]
             for band in self.bands:
                 if band[0] != "w":
                     self.passbandsList.append(astSED.Passband(passbandsDir+"decam.%s.am1p4.dat.txt" % (band)))
                 else:
                     self.passbandsList.append(astSED.Passband(passbandsDir+"RSR-%s.EE.txt" % (band.upper()), inputUnits = "microns"))
         else:
             raise Exception("Unknown passbandSet '%s'" % (passbandSet))
@@ -254,15 +258,16 @@
         for i in range(diffMags.shape[1]):
             d=diffMags[:, i]
             ZPOffsets.append(np.median(d[np.less(d, 1)]))
         self.ZPOffsets=np.array(ZPOffsets)
         print("... offsets found: %s mag." % (str(self.ZPOffsets)))
 
     
-    def calcPhotoRedshifts(self, galaxyCatalog, calcMLRedshiftAndOdds = False):
+    def calcPhotoRedshifts(self, galaxyCatalog, calcMLRedshiftAndOdds = False, returnPZ = True,
+                           storeBestFitSEDModels = False):
         """Calculates photometric redshifts and adds to the galaxy catalog in place.
         
         NOTE: since normally we're normally only interested in p(z), this only returns
         the maximum likelihood z and BPZ-style odds parameter if calcMLRedshiftAndOdds = True.
         
         """
                
@@ -307,33 +312,44 @@
             norm=np.sum((self.modelFlux*sedFlux)/(sedFluxErr2), axis=1)/np.sum(self.modelFlux2/sedFluxErr2, axis=1)
             chiSq=np.sum(((sedFlux-norm.reshape([norm.shape[0], 1])*self.modelFlux)**2)/sedFluxErr2, axis=1)
             chiSq[np.isnan(chiSq)]=1e6   # throw these out, should check this out and handle more gracefully
             
             # This extracts chiSq as function of redshift for the best-fit template only, if we wanted it
             #chiSq=chiSq[self.templateIndex == self.templateIndex[np.argmin(chiSq)]]
             #pz=np.exp(-chiSq/2)
+
+            # This is useful if we want to add rest frame color calculation
+            if storeBestFitSEDModels == True:
+                galaxy['bestFitSED']=self.modelSEDDictList[self.templateIndex[np.argmin(chiSq)]]['SED']
+
             # This uses all templates at once
             chiSqProb=np.exp(-chiSq/2)#stats.chisqprob(chiSq, len(self.bands)-2)
             chiSqProb=chiSqProb.reshape([self.numModels, self.zRange.shape[0]])
             #pz=np.sum(chiSqProb, axis = 0)
             pz=np.max(chiSqProb, axis = 0)
             # Mag prior
             absMag=magAB[self.magPriorBand]-5.0*np.log10(1e5*self.dlRange)
-            pPrior=np.array(np.greater(absMag, self.magPriorCut), dtype = float)
+            if type(self.magPriorCut) == float:
+                pPrior=np.array(np.greater(absMag, self.magPriorCut), dtype = float)
+            elif len(self.magPriorCut) == 2:
+                pPrior=np.array(np.logical_and(np.greater(absMag, self.magPriorCut[0]), np.less(absMag, self.magPriorCut[1]), dtype = float))
+            else:
+                raise Exception("magPriorCut should have only 1 or 2 elements")
             pz=pz*pPrior
             # Normalise
             pzNorm=np.trapz(pz, self.zRange)
             if pzNorm != 0:
                 pz=pz/pzNorm 
             if calcMLRedshiftAndOdds == True:
                 zp, odds=self.calculateMLRedshiftAndOdds(pz, dzOdds = 0.2)
                 galaxy['zPhot']=zp
                 galaxy['odds']=odds
-            galaxy['pz']=pz
-            galaxy['pz_z']=self.zRange
+            if returnPZ == True:
+                galaxy['pz']=pz
+                galaxy['pz_z']=self.zRange
         t1=time.time()
         
 
     def calculateMLRedshiftAndOdds(self, pz, dzOdds = 0.2, method = 'max'):
         """Calculates maximum likelihood z and BPZ/EAZY style odds for given pz, zArray
         
         Method == 'max' finds z based on max peak in pz
@@ -371,8 +387,58 @@
                 odds=np.trapz(pz[indexMin:indexMax], self.zRange[indexMin:indexMax])
                 zOdds.append(odds)
             zOdds=np.array(zOdds)
             z=self.zRange[zOdds.tolist().index(zOdds.max())]
             odds=zOdds[zOdds.tolist().index(zOdds.max())]    
     
         return [z, odds]
-    
+
+
+    def estimateStellarMasses(self, galaxyCatalog, stellarMassModelDir, z = None):
+        """Given a directory containing BC03-format stellar population models, estimate
+        the stellar mass of galaxies in the given catalog.
+
+        Args:
+            galaxyCatalog (:obj:`list`): Galaxy catalog as a list of dictionaries, i.e.,
+                in the format returned by self.calcPhotoRedshifts().
+            stellarMassModelDir (:obj:`str`): Path to a directory containing the stellar
+                population models (BC03 format for now).
+            z (:obj:`float`, optional): If given, the redshift will be fixed to this value
+                and applied to all the galaxies in the catalog (this is what you want for
+                galaxy clusters, and is quicker). If None, then the maximum likelihood
+                redshift of each individual galaxy will be used (this will be very slow,
+                but actually isn't implemented yet...).
+
+        Returns:
+            None ['log10StellarMass' key is added in-place to each galaxy in galaxyCatalog]
+
+        """
+
+        if z is None:
+            raise Exception("Stellar mass estimation at individual galaxy maximum likelihood redshifts is not implemented yet.")
+
+        # Make model SEDs - this is very time consuming and needs a lot of speeding up...
+        modelSEDDictList=sm.setUpStellarMassSEDs(stellarMassModelDir, self.passbandsList, z)
+
+        # Fit each observed SED
+        wantedKeys=['log10StellarMass']
+        count=0
+        DL=astCalc.dl(z)
+        print(">>> Estimating stellar masses")
+        for objDict in galaxyCatalog:
+            count=count+1
+            print("... %d/%d ..." % (count, len(galaxyCatalog)))
+            mags=[]
+            magErrs=[]
+            for band in self.bands:
+                if band in list(objDict.keys()):
+                    mags.append(objDict[band])
+                    magErrs.append(objDict[band+"Err"])
+                else:
+                    mags.append(99)
+                    magErrs.append(99)
+            obsSEDDict=astSED.mags2SEDDict(mags, magErrs, self.passbandsList)
+            distNorm=4*np.pi*np.power(DL*3.08567758e24, 2)
+            fitResult=sm.fitSEDDictAndCalcStellarMass(obsSEDDict, modelSEDDictList, distNorm)
+            # Insert monte-carlo error estimation here...
+            for key in wantedKeys:
+                objDict[key]=fitResult[key]
```

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/default_sed1.dat` & `zCluster-0.3.0/zCluster/SED/BR07/default_sed1.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/default_sed2.dat` & `zCluster-0.3.0/zCluster/SED/BR07/default_sed2.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/default_sed3.dat` & `zCluster-0.3.0/zCluster/SED/BR07/default_sed3.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/default_sed4.dat` & `zCluster-0.3.0/zCluster/SED/BR07/default_sed4.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/default_sed5.dat` & `zCluster-0.3.0/zCluster/SED/BR07/default_sed5.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/goods_sed1.dat` & `zCluster-0.3.0/zCluster/SED/BR07/goods_sed1.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/goods_sed2.dat` & `zCluster-0.3.0/zCluster/SED/BR07/goods_sed2.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/goods_sed3.dat` & `zCluster-0.3.0/zCluster/SED/BR07/goods_sed3.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/goods_sed4.dat` & `zCluster-0.3.0/zCluster/SED/BR07/goods_sed4.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/goods_sed5.dat` & `zCluster-0.3.0/zCluster/SED/BR07/goods_sed5.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/BR07/lrg1_sed1.dat` & `zCluster-0.3.0/zCluster/SED/BR07/lrg1_sed1.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/CWW/CWW_E_ext.sed` & `zCluster-0.3.0/zCluster/SED/CWW/CWW_E_ext.sed`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/CWW/CWW_Im_ext.sed` & `zCluster-0.3.0/zCluster/SED/CWW/CWW_Im_ext.sed`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/CWW/CWW_Sbc_ext.sed` & `zCluster-0.3.0/zCluster/SED/CWW/CWW_Sbc_ext.sed`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/CWW/CWW_Scd_ext.sed` & `zCluster-0.3.0/zCluster/SED/CWW/CWW_Scd_ext.sed`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/CWW/SB2_kin.sed` & `zCluster-0.3.0/zCluster/SED/CWW/SB2_kin.sed`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/CWW/SB3_kin.sed` & `zCluster-0.3.0/zCluster/SED/CWW/SB3_kin.sed`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed1.dat` & `zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed1.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed2.dat` & `zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed2.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed3.dat` & `zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed3.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed4.dat` & `zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed4.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed5.dat` & `zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed5.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed6.dat` & `zCluster-0.3.0/zCluster/SED/EAZY_v1.0/eazy_v1.0_sed6.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/catalogs.py` & `zCluster-0.3.0/zCluster/catalogs.py`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/clusters.py` & `zCluster-0.3.0/zCluster/clusters.py`

 * *Files 4% similar despite different names*

```diff
@@ -12,15 +12,14 @@
 from scipy import stats
 from scipy import ndimage
 import astropy.io.fits as pyfits
 from astropy.coordinates import SkyCoord
 from astropy.coordinates import match_coordinates_sky
 from PIL import Image
 from PIL import ImageDraw
-import zClusterCython
 import pylab as plt
 
 #------------------------------------------------------------------------------------------------------------
 def getPixelAreaDeg2Map(mapData, wcs):
     """Returns a map of pixel area in square degrees.
     
     """
@@ -38,14 +37,74 @@
         yPixScale=astCoords.calcAngSepDeg(ra0, dec0, ra0, dec1)
         pixAreasDeg2.append(xPixScale*yPixScale)
     pixAreasDeg2=np.array(pixAreasDeg2)
     pixAreasDeg2Map=np.array([pixAreasDeg2]*mapData.shape[1]).transpose()
     
     return pixAreasDeg2Map   
 
+#---------------------------------------------------------------------------------------------------
+def makeDegreesDistanceMap(degreesMap, wcs, RADeg, decDeg, maxDistDegrees):
+    """Fills (in place) the 2d array degreesMap with distance in degrees from the given position,
+    out to some user-specified maximum distance.
+
+    Args:
+        degreesMap (:obj:`np.ndarray`): Map (2d array) that will be filled with angular distance
+            from the given coordinates. Probably you should feed in an array set to some extreme
+            initial value (e.g., 1e6 everywhere) to make it easy to filter for pixels near the
+            object coords afterwards.
+        wcs (:obj:`astWCS.WCS`): WCS corresponding to degreesMap.
+        RADeg (float): RA in decimal degrees of position of interest (e.g., object location).
+        decDeg (float): Declination in decimal degrees of position of interest (e.g., object
+            location).
+        maxDistDegrees: The maximum radius out to which distance will be calculated.
+
+    Returns:
+        A map (2d array) of distance in degrees from the given position,
+        (min x, max x) pixel coords corresponding to maxDistDegrees box,
+        (min y, max y) pixel coords corresponding to maxDistDegrees box
+
+    Note:
+        This routine measures the pixel scale local to the given position, then assumes that it
+        does not change. So, this routine may only be accurate close to the given position,
+        depending upon the WCS projection used.
+
+    """
+
+    x0, y0=wcs.wcs2pix(RADeg, decDeg)
+    ra0, dec0=RADeg, decDeg
+    ra1, dec1=wcs.pix2wcs(x0+1, y0+1)
+    xPixScale=astCoords.calcAngSepDeg(ra0, dec0, ra1, dec0)
+    yPixScale=astCoords.calcAngSepDeg(ra0, dec0, ra0, dec1)
+
+    xDistPix=int(round((maxDistDegrees)/xPixScale))
+    yDistPix=int(round((maxDistDegrees)/yPixScale))
+
+    Y=degreesMap.shape[0]
+    X=degreesMap.shape[1]
+
+    minX=int(round(x0))-xDistPix
+    maxX=int(round(x0))+xDistPix
+    minY=int(round(y0))-yDistPix
+    maxY=int(round(y0))+yDistPix
+    if minX < 0:
+        minX=0
+    if maxX > X:
+        maxX=X
+    if minY < 0:
+        minY=0
+    if maxY > Y:
+        maxY=Y
+
+    xDeg=(np.arange(degreesMap.shape[1])-x0)*xPixScale
+    yDeg=(np.arange(degreesMap.shape[0])-y0)*yPixScale
+    for i in range(minY, maxY):
+        degreesMap[i][minX:maxX]=np.sqrt(yDeg[i]**2+xDeg[minX:maxX]**2)
+
+    return degreesMap, [minX, maxX], [minY, maxY]
+
 #------------------------------------------------------------------------------------------------------------
 def makeBlankMap(RADeg, decDeg, sizePix, sizeDeg):
     """Makes a square blank map with a WCS.
     
     Returns:
         - mapData (2d array)
         - wcs (astWCS.WCS object)
@@ -75,15 +134,15 @@
     newHead['CUNIT2']='deg'
     wcs=astWCS.WCS(newHead, mode='pyfits')
     
     return np.zeros([int(sizePix), int(sizePix)], dtype = float), wcs
 
 #-------------------------------------------------------------------------------------------------------------
 def makeDensityMap(RADeg, decDeg, catalog, z, dz = 0.1, rMaxMpc = 1.5, sizeMpc = 8.0, MpcPerPix = 0.1,
-                   gaussSmoothPix = 2):
+                   gaussSmoothPix = 2, outFITSFileName = None, outPlotFileName = None):
     """Makes a projected density map within +/- dz of the given redshift, smoothed using a Gaussian kernel,
     then calculates the centroid location, centroid shift (with respect to the original position), and an
     asymmetry statistic.
     
     Args:
         RADeg (float): RA coordinate (decimal degrees) of the center of the output map.
         decDeg (float): dec coordinate (decimal degrees) of the center of the output map.
@@ -92,14 +151,19 @@
             calculated.
         rMaxMpc (float, optional): The maximum radial distance in Mpc (from RADeg, decDeg) in which the
             centroid search is performed.
         sizeMpc (float, optional): The size of the density map (which is square) in projected Mpc.
         MpcPerPix (float, optional): The pixel size, in projected Mpc, for the output density map.
         gaussSmoothPix (int, optional): The size of the Gaussian smoothing kernel applied to the output
             projected density map, in pixels.
+        outFITSFileName (str, optional): If given, write the density map as a FITS file to the given
+            location.
+        makePlot (str, optional): If given, write a plot of the density map to the given location (the
+            file format is determined by the extension, and supported formats depend on the matplotlib
+            backend used).
         
     Returns:
         A dictionary with keys:
             - 'map': the output projected density map (2d array)
             - 'wcs': the output WCS
             - 'cRADeg': the RA of the centroid (peak) in the density map
             - 'cDecDeg': the dec of the centroid (peak) in the density map
@@ -148,17 +212,40 @@
     rMpcMap=np.radians(rDegMap)*DA
     rMask=np.less(rMpcMap, rMaxMpc)
     y, x=np.where((d*rMask) == (d*rMask).max())
     cRADeg, cDecDeg=wcs.pix2wcs(x[0], y[0])
     offsetArcmin=astCoords.calcAngSepDeg(cRADeg, cDecDeg, RADeg, decDeg)*60
     offsetMpc=np.radians(offsetArcmin/60.)*DA
     
+    if outFITSFileName is not None:
+        astImages.saveFITS(outFITSFileName, d, wcs)
+
+    if outPlotFileName is not None:
+        axes=[0, 0, 1, 1]
+        axesLabels="sexagesimal"    # Avoid dealing with axis flips
+        figSize=(8.25, 8.25)
+        fig=plt.figure(figsize = figSize, dpi = 300)
+        p=astPlots.ImagePlot(d, wcs, cutLevels = [d.min(), d.max()],
+                             colorMapName = 'magma', axes = axes,
+                             axesLabels = axesLabels)
+
+        if sizeMpc > 40:
+            scaleBarMpc=5
+        elif sizeMpc > 10 and sizeMpc < 40:
+            scaleBarMpc=2
+        elif sizeMpc < 10:
+            scaleBarMpc=1
+        scaleBarMpc=5#int(round(sizeMpc/5))
+        scaleBarSizeArcmin=np.degrees(scaleBarMpc/astCalc.da(z))*60
+        p.addScaleBar('SE', scaleBarSizeArcmin*60.0, color='cyan', fontSize=16, width=2.0, label = "%d Mpc" % (scaleBarMpc))
+        plt.savefig(outPlotFileName)
+
     return {'map': d, 'wcs': wcs, 'cRADeg': cRADeg, 'cDecDeg': cDecDeg, 
             'offsetArcmin': offsetArcmin, 'offsetMpc': offsetMpc, 'CS': CS, 'A': A}
-        
+
 #-------------------------------------------------------------------------------------------------------------
 def makeWeightedNz(RADeg, decDeg, catalog, zPriorMax, weightsType, minDistanceMpc = 0.0, maxDistanceMpc = 1.0, 
                    applySanityCheckRadius = True, sanityCheckRadiusArcmin = 1.0, areaMask = None, wcs = None):
     """Make a N(z) distribution in the direction of the postion (usually of a cluster) given by RADeg, decDeg.
     This is constructed from the p(z) distributions of all galaxies in the catalog, with radial weights applied
     as per weightsType. So, for 'flat1Mpc', the radial weight is 1 if within a projected distance of 1 Mpc of 
     RADeg, decDeg, and 0 otherwise.
@@ -269,15 +356,15 @@
     
     # We may as well keep track of area as well
     if areaMask is None:
         areaMpc2=np.array([np.pi*maxDistanceMpc**2 - np.pi*minDistanceMpc**2]*len(zArray))
     else:
         areaMap=getPixelAreaDeg2Map(areaMask, wcs)
         rDegMap=np.zeros(areaMask.shape)
-        rDegMap, xRange, yRange=zClusterCython.makeDegreesDistanceMap(rDegMap, wcs, RADeg, decDeg, 2.0)
+        rDegMap, xRange, yRange=makeDegreesDistanceMap(rDegMap, wcs, RADeg, decDeg, 2.0)
         rDegMap=rDegMap[yRange[0]:yRange[1], xRange[0]:xRange[1]]
         areaMap=areaMask[yRange[0]:yRange[1], xRange[0]:xRange[1]]*areaMap[yRange[0]:yRange[1], xRange[0]:xRange[1]]
         areaMpc2=[]
         count=0
         for DA in DAArray:
             areaScaling=1/np.power(np.degrees(np.arctan(1.0/DA)), 2)
             max_rDegCut=np.degrees(np.arctan(maxDistanceMpc/DA))
```

### Comparing `zCluster-0.2.0/zCluster/data/redmapper_dr8_public_v5.10_catalog.fits` & `zCluster-0.3.0/zCluster/data/redmapper_dr8_public_v5.10_catalog.fits`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/data/tau0p1Gyr_m62.20` & `zCluster-0.3.0/zCluster/data/tau0p1Gyr_m62.20`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/K_2MASS.res` & `zCluster-0.3.0/zCluster/passbands/K_2MASS.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/RSR-W1.EE.txt` & `zCluster-0.3.0/zCluster/passbands/RSR-W1.EE.txt`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/RSR-W2.EE.txt` & `zCluster-0.3.0/zCluster/passbands/RSR-W2.EE.txt`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/RSR-W3.EE.txt` & `zCluster-0.3.0/zCluster/passbands/RSR-W3.EE.txt`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/RSR-W4.EE.txt` & `zCluster-0.3.0/zCluster/passbands/RSR-W4.EE.txt`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_H.dat` & `zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_H.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_J.dat` & `zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_J.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Ks.dat` & `zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Ks.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Y.dat` & `zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Y.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Z.dat` & `zCluster-0.3.0/zCluster/passbands/VISTA_Filters_at80K_forETC_Z.dat`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/decam.g.am1p4.dat.txt` & `zCluster-0.3.0/zCluster/passbands/decam.g.am1p4.dat.txt`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/decam.r.am1p4.dat.txt` & `zCluster-0.3.0/zCluster/passbands/decam.r.am1p4.dat.txt`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/decam.z.am1p4.dat.txt` & `zCluster-0.3.0/zCluster/passbands/decam.z.am1p4.dat.txt`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/gDES.res` & `zCluster-0.3.0/zCluster/passbands/gDES.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/gPS1.res` & `zCluster-0.3.0/zCluster/passbands/gPS1.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/g_CFHTLS.res` & `zCluster-0.3.0/zCluster/passbands/g_CFHTLS.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/g_SDSS3.res` & `zCluster-0.3.0/zCluster/passbands/g_SDSS3.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/i2_CFHTLS.res` & `zCluster-0.3.0/zCluster/passbands/i2_CFHTLS.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/iDES.res` & `zCluster-0.3.0/zCluster/passbands/iDES.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/iPS1.res` & `zCluster-0.3.0/zCluster/passbands/iPS1.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/i_CFHTLS.res` & `zCluster-0.3.0/zCluster/passbands/i_CFHTLS.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/i_SDSS3.res` & `zCluster-0.3.0/zCluster/passbands/i_SDSS3.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/rDES.res` & `zCluster-0.3.0/zCluster/passbands/rDES.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/rPS1.res` & `zCluster-0.3.0/zCluster/passbands/rPS1.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/r_CFHTLS.res` & `zCluster-0.3.0/zCluster/passbands/r_CFHTLS.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/r_SDSS.res` & `zCluster-0.3.0/zCluster/passbands/r_SDSS.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/r_SDSS3.res` & `zCluster-0.3.0/zCluster/passbands/r_SDSS3.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/u_CFHTLS.res` & `zCluster-0.3.0/zCluster/passbands/u_CFHTLS.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/u_SDSS3.res` & `zCluster-0.3.0/zCluster/passbands/u_SDSS3.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/yDES.res` & `zCluster-0.3.0/zCluster/passbands/yDES.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/yPS1.res` & `zCluster-0.3.0/zCluster/passbands/yPS1.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/zDES.res` & `zCluster-0.3.0/zCluster/passbands/zDES.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/zPS1.res` & `zCluster-0.3.0/zCluster/passbands/zPS1.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/z_CFHTLS.res` & `zCluster-0.3.0/zCluster/passbands/z_CFHTLS.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/z_SDSS.res` & `zCluster-0.3.0/zCluster/passbands/z_SDSS.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/passbands/z_SDSS3.res` & `zCluster-0.3.0/zCluster/passbands/z_SDSS3.res`

 * *Files identical despite different names*

### Comparing `zCluster-0.2.0/zCluster/retrievers.py` & `zCluster-0.3.0/zCluster/retrievers.py`

 * *Files 2% similar despite different names*

```diff
@@ -104,23 +104,31 @@
     elif database == 'ATLASDR4':
         passbandSet='KiDS-VIKING'
         retriever=ATLASDR4Retriever
         retrieverOptions={'maxMagError': maxMagError}
     elif database == 'CFHTLenS':
         retriever=CFHTLenSRetriever
         retrieverOptions={'maxMagError': maxMagError}
+    elif database == 'DELVEDR2':
+        retriever=DELVEDR2Retriever
+        retrieverOptions={'maxMagError': maxMagError}
     elif database.find("DECaLS") != -1:
         if database == "DECaLS":
-            raise Exception("Specify either 'DECaLSDR8' or 'DECaLSDR9' instead of DECaLS")
+            raise Exception("Specify either 'DECaLSDR8', 'DECaLSDR9', or 'DECaLSDR10' instead of DECaLS")
         if database == 'DECaLSDR8':
             DR="DR8"
             retriever=DECaLSDR8Retriever
         elif database == 'DECaLSDR9':
             DR="DR9"
             retriever=DECaLSDR9Retriever
+        elif database == "DECaLSDR10":
+            DR="DR10"
+            retriever=DECaLSDR10Retriever
+        else:
+            raise Exception("Didn't understand DECaLS database choice")
         passbandSet='DECaLS'
         # For DECaLS, need the bricks files that define survey on the sky
         # These were previously included in zCluster, but now we fetch over web and cache
         bricksCacheDir=CACHE_DIR
         makeCacheDir()
         bricksPath=bricksCacheDir+os.path.sep+"survey-bricks.fits.gz"
         if os.path.exists(bricksPath) == False:
@@ -1055,15 +1063,15 @@
                 if keep == True:
                     catalog.append(photDict)
         
     return catalog
 
 #-------------------------------------------------------------------------------------------------------------
 def DECaLSRetriever(RADeg, decDeg, halfBoxSizeDeg = 36.0/60.0, DR = None, optionsDict = {}):
-    """Retrieves DECaLS DR8 tractor catalogs (if they exist) at the given position. Cuts the catalog to the
+    """Retrieves DECaLS DRx tractor catalogs (if they exist) at the given position. Cuts the catalog to the
     radius specified by halfBoxSizeDeg.
 
     """
 
     makeCacheDir()
     
     if 'altCacheDir' in list(optionsDict.keys()):
@@ -1121,14 +1129,15 @@
             try:
                 urllib.request.urlretrieve(url, filename = fileName)
             except:
                 with open("wget_failed.sh", "a") as outFile:
                     outFile.write("wget -nc %s\n" % (url))
                 print("... WARNING: failed to fetch from %s" % (url))
         try:
+            print("... reading from cache: %s ..." % (fileName))
             tractorTab=atpy.Table.read(fileName)
             tractorTabs.append(tractorTab)
         except:
             print("... possibly a 404 error for %s - check if cached file is corrupted ..." % (fileName))
     if 'downloadOnly' in optionsDict.keys() and optionsDict['downloadOnly'] == True:
         return None
     
@@ -1150,20 +1159,29 @@
             tab=tab[np.where(tab['brightblob'] == 0)]
         except:
             # Use maskbits 1, 11, 12, 13 for DR9
             # [still use brightblob for DR8 for now to be consistent with past results, but it's basically the same anyway]
             tab=tab[tab['maskbits'] != 2**1]
             tab=tab[tab['maskbits'] < 2**11]
         # Below is clean but loses us some clusters that look ok (we can't do proper bitwise anyway with atpy table?)
-        #tab=tab[np.where(tab['maskbits'] == 0)] 
-        tab=tab[np.where(tab['type'] != 'PSF')]
-        tab=tab[np.where(tab['type'] != 'PSF ')] # Trailing space
-        
-        # WISE fluxes are available...
+        #tab=tab[np.where(tab['maskbits'] == 0)]
+        # Added getStars option for when we want to use this code for making
+        if 'getStars' in optionsDict.keys() and optionsDict['getStars'] == True:
+            starMask=np.logical_or(tab['type'] == 'PSF', tab['type'] == 'PSF ') # some catalogs have trailing space
+            tab=tab[starMask]
+            # Keep only Gaia objects - so we really, really get star-like objects
+            tab=tab[tab['ref_cat'] == 'G2']
+        else:
+            tab=tab[np.where(tab['type'] != 'PSF')]
+            tab=tab[np.where(tab['type'] != 'PSF ')] # Trailing space
+
+        # WISE fluxes are available... i-band added in DECaLS DR10
         bands=['g', 'r', 'z', "w1", "w2"]# , 'Y']
+        if DR == 'DR10':
+            bands.append('i')
         
         # Convert nanomaggies to mags and do extinction correction
         bricksInTab=np.unique(tab['brickname'])
         for brickName in bricksInTab:
             brickExtTab=DRTab[np.where(DRTab['BRICKNAME'] == brickName)]
             brickIndices=np.where(tab['brickname'] == brickName)
             brickMask=np.zeros(len(tab), dtype = bool)
@@ -1219,24 +1237,76 @@
     
     stuff=DECaLSRetriever(RADeg, decDeg, halfBoxSizeDeg = halfBoxSizeDeg, DR = 'DR8', optionsDict = optionsDict)
 
     return stuff
 
 #-------------------------------------------------------------------------------------------------------------
 def DECaLSDR9Retriever(RADeg, decDeg, halfBoxSizeDeg = 36.0/60.0, DR = None, optionsDict = {}):
-    """Retrieves DECaLS DR8 tractor catalogs (if they exist) at the given position. Cuts the catalog to the
+    """Retrieves DECaLS DR9 tractor catalogs (if they exist) at the given position. Cuts the catalog to the
     radius specified by halfBoxSizeDeg.
 
     """
     
     stuff=DECaLSRetriever(RADeg, decDeg, halfBoxSizeDeg = halfBoxSizeDeg, DR = 'DR9', optionsDict = optionsDict)
     
     return stuff
 
 #-------------------------------------------------------------------------------------------------------------
+def DECaLSDR10Retriever(RADeg, decDeg, halfBoxSizeDeg = 36.0/60.0, DR = None, optionsDict = {}):
+    """Retrieves DECaLS DR10 tractor catalogs (if they exist) at the given position. Cuts the catalog to the
+    radius specified by halfBoxSizeDeg.
+
+    """
+
+    stuff=DECaLSRetriever(RADeg, decDeg, halfBoxSizeDeg = halfBoxSizeDeg, DR = 'DR10', optionsDict = optionsDict)
+
+    return stuff
+
+#-------------------------------------------------------------------------------------------------------------
+def DELVEDR2Retriever(RADeg, decDeg, halfBoxSizeDeg = 36.0/60.0, DR = None, optionsDict = {}):
+    """DELVE DR2 retriever, using NOAO datalab.
+
+    """
+
+    from dl import queryClient as qc
+    RAMin, RAMax, decMin, decMax=astCoords.calcRADecSearchBox(RADeg, decDeg, halfBoxSizeDeg)
+    result=qc.query(sql='select ra, dec, mag_auto_g, mag_auto_r, mag_auto_i, mag_auto_z, magerr_auto_g, magerr_auto_r,\
+                    magerr_auto_i, magerr_auto_z, extinction_g, extinction_r, extinction_i, extinction_z from delve_dr2.objects where\
+                    extended_class_r > 1 and RA BETWEEN %.6f AND %.6f AND DEC BETWEEN %.6f and %.6f' % (RAMin, RAMax, decMin, decMax))
+
+    catalog=[]
+    count=0
+    bands=['g', 'r', 'i', 'z']
+    for row in result.split('\n')[1:]:
+        count=count+1
+        objDict={}
+        objDict['id']=count
+        bits=row.split(',')
+        if len(bits) > 1:
+            objDict['RADeg']=float(bits[0])
+            objDict['decDeg']=float(bits[1])
+            # Inc. extinction correction
+            objDict['g']=float(bits[2])-float(bits[10])
+            objDict['r']=float(bits[3])-float(bits[11])
+            objDict['i']=float(bits[4])-float(bits[12])
+            objDict['z']=float(bits[5])-float(bits[13])
+            objDict['gErr']=float(bits[6])
+            objDict['rErr']=float(bits[7])
+            objDict['iErr']=float(bits[8])
+            objDict['zErr']=float(bits[9])
+            if 'maxMagError' in list(optionsDict.keys()):
+                keep=checkMagErrors(objDict, optionsDict['maxMagError'], bands = bands)
+            else:
+                keep=True
+            if keep == True:
+                catalog.append(objDict)
+
+    return catalog
+
+#-------------------------------------------------------------------------------------------------------------
 def SDSSDR7Retriever(RADeg, decDeg, halfBoxSizeDeg = 9.0/60.0, optionsDict = {}):
     """Retrieves SDSS DR7 main photometry at the given position.
     
     """
     
     stuff=SDSSRetriever(RADeg, decDeg, halfBoxSizeDeg = halfBoxSizeDeg, DR = 7, optionsDict = optionsDict)
     return stuff
```

### Comparing `zCluster-0.2.0/zCluster.egg-info/SOURCES.txt` & `zCluster-0.3.0/zCluster.egg-info/SOURCES.txt`

 * *Files 14% similar despite different names*

```diff
@@ -1,40 +1,29 @@
-.gitattributes
-.kateproject
 COPYING
 INSTALL.rst
 MANIFEST.in
 README.rst
 pyproject.toml
-requirements.txt
 setup.cfg
 setup.py
 versioneer.py
 bin/zCluster
 bin/zClusterBCG
 bin/zClusterComparisonPlot
 bin/zField
-docs/Makefile
-docs/commands.rst
-docs/conf.py
-docs/index.rst
-docs/install.rst
-docs/reference.rst
-docs/usage.rst
 examples/400SDAll.csv
 examples/400SDSmall.csv
 examples/README_EXAMPLE.rst
-tests/tests.sh
 zCluster/PhotoRedshiftEngine.py
 zCluster/__init__.py
 zCluster/_version.py
 zCluster/catalogs.py
 zCluster/clusters.py
 zCluster/retrievers.py
-zCluster/zClusterCython.pyx
+zCluster/stellarmass.py
 zCluster.egg-info/PKG-INFO
 zCluster.egg-info/SOURCES.txt
 zCluster.egg-info/dependency_links.txt
 zCluster.egg-info/requires.txt
 zCluster.egg-info/top_level.txt
 zCluster/SED/BR07/default_sed1.dat
 zCluster/SED/BR07/default_sed2.dat
@@ -68,14 +57,15 @@
 zCluster/passbands/RSR-W4.EE.txt
 zCluster/passbands/VISTA_Filters_at80K_forETC_H.dat
 zCluster/passbands/VISTA_Filters_at80K_forETC_J.dat
 zCluster/passbands/VISTA_Filters_at80K_forETC_Ks.dat
 zCluster/passbands/VISTA_Filters_at80K_forETC_Y.dat
 zCluster/passbands/VISTA_Filters_at80K_forETC_Z.dat
 zCluster/passbands/decam.g.am1p4.dat.txt
+zCluster/passbands/decam.i.am1p4.dat.txt
 zCluster/passbands/decam.r.am1p4.dat.txt
 zCluster/passbands/decam.z.am1p4.dat.txt
 zCluster/passbands/gDES.res
 zCluster/passbands/gPS1.res
 zCluster/passbands/g_CFHTLS.res
 zCluster/passbands/g_SDSS.res
 zCluster/passbands/g_SDSS3.res
```

