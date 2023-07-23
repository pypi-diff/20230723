# Comparing `tmp/shiny_mdc-1.7.1.tar.gz` & `tmp/shiny_mdc-1.8.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "shiny_mdc-1.7.1.tar", max compression
+gzip compressed data, was "shiny_mdc-1.8.0.tar", max compression
```

## Comparing `shiny_mdc-1.7.1.tar` & `shiny_mdc-1.8.0.tar`

### file list

```diff
@@ -1,64 +1,65 @@
--rw-r--r--   0        0        0     7079 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/CHANGELOG.md
--rw-r--r--   0        0        0     1082 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/LICENSE
--rw-r--r--   0        0        0       78 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/README.md
--rw-r--r--   0        0        0     2313 2023-06-30 00:42:13.354307 shiny_mdc-1.7.1/pyproject.toml
--rw-r--r--   0        0        0       34 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/__init__.py
--rw-r--r--   0        0        0     1061 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/_latexmk.py
--rw-r--r--   0        0        0     1867 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/_liquid.py
--rw-r--r--   0        0        0     4782 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/_pandoc.py
--rw-r--r--   0        0        0     5084 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/_templates.py
--rw-r--r--   0        0        0       64 2023-06-30 00:42:13.354307 shiny_mdc-1.7.1/shinymdc/_version.py
--rw-r--r--   0        0        0      410 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/dynamic/addappendices.tex
--rw-r--r--   0        0        0      879 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/dynamic/authsetup.tex
--rw-r--r--   0        0        0      316 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/dynamic/authsetupshort.tex
--rw-r--r--   0        0        0      572 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/dynamic/dblfloatsetup.tex
--rw-r--r--   0        0        0      491 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/bibnonatsetup.tex
--rw-r--r--   0        0        0      324 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/bibnosupersetup.tex
--rw-r--r--   0        0        0      745 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/bibsupersetup.tex
--rw-r--r--   0        0        0     3266 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/floatsetup.tex
--rw-r--r--   0        0        0    19901 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/iccv/bibstyle.bst
--rw-r--r--   0        0        0     9433 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/iccv/esopic.sty
--rw-r--r--   0        0        0     3869 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/iccv/everyshi.sty
--rw-r--r--   0        0        0     8276 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/iccv/iccv.sty
--rw-r--r--   0        0        0    26973 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/iclr/bibstyle.bst
--rw-r--r--   0        0        0     9153 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/iclr/iclr.sty
--rw-r--r--   0        0        0    12284 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/iclr/mathcommands.tex
--rw-r--r--   0        0        0    27146 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/icml/bibstyle.bst
--rw-r--r--   0        0        0    27887 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/icml/icml.sty
--rw-r--r--   0        0        0      735 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/mathsetup.tex
--rw-r--r--   0        0        0     1202 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/miscsetup.tex
--rw-r--r--   0        0        0    11306 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/neurips/neurips.sty
--rw-r--r--   0        0        0      503 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/resources/static/reqsetup.tex
--rw-r--r--   0        0        0    19497 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/shinymdc.py
--rw-r--r--   0        0        0     1017 2023-06-30 00:41:54.542353 shiny_mdc-1.7.1/shinymdc/templates/basic.tex
--rw-r--r--   0        0        0     1302 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/shinymdc/templates/iccv.tex
--rw-r--r--   0        0        0     1423 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/shinymdc/templates/iclr.tex
--rw-r--r--   0        0        0     2170 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/shinymdc/templates/icml.tex
--rw-r--r--   0        0        0      916 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/shinymdc/templates/neurips.tex
--rw-r--r--   0        0        0     3136 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/shinymdc/templates/spacious.tex
--rw-r--r--   0        0        0      464 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/shinymdc/templates/standalone.tex
--rw-r--r--   0        0        0     2483 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/shinymdc/templates/stylish.tex
--rw-r--r--   0        0        0    15953 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/test/figures/anscombe.pdf
--rw-r--r--   0        0        0    40892 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/test/figures/densities.pdf
--rw-r--r--   0        0        0    10736 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/test/figures/diamonds.pdf
--rw-r--r--   0        0        0   197017 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/test/figures/gaussian2d.pdf
--rw-r--r--   0        0        0    28282 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/test/figures/lines.png
--rw-r--r--   0        0        0     2988 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/test/main.md
--rwxr-xr-x   0        0        0      315 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/test/make.sh
--rw-r--r--   0        0        0     1166 2023-06-30 00:41:54.546353 shiny_mdc-1.7.1/test/references.bib
--rw-r--r--   0        0        0   690901 2023-06-30 00:41:54.550353 shiny_mdc-1.7.1/test/samples/basic.pdf
--rw-r--r--   0        0        0   414185 2023-06-30 00:41:54.550353 shiny_mdc-1.7.1/test/samples/iccv.pdf
--rw-r--r--   0        0        0   407653 2023-06-30 00:41:54.554353 shiny_mdc-1.7.1/test/samples/iclr.pdf
--rw-r--r--   0        0        0   446740 2023-06-30 00:41:54.554353 shiny_mdc-1.7.1/test/samples/icml.pdf
--rw-r--r--   0        0        0   451322 2023-06-30 00:41:54.558353 shiny_mdc-1.7.1/test/samples/neurips.pdf
--rw-r--r--   0        0        0   600276 2023-06-30 00:41:54.562353 shiny_mdc-1.7.1/test/samples/spacious.pdf
--rw-r--r--   0        0        0   555527 2023-06-30 00:41:54.562353 shiny_mdc-1.7.1/test/samples/standalone.pdf
--rw-r--r--   0        0        0   425326 2023-06-30 00:41:54.566353 shiny_mdc-1.7.1/test/samples/stylish.pdf
--rw-r--r--   0        0        0     1535 2023-06-30 00:41:54.566353 shiny_mdc-1.7.1/test/sections/appendix1.md
--rw-r--r--   0        0        0     1624 2023-06-30 00:41:54.566353 shiny_mdc-1.7.1/test/sections/appendix2.md
--rw-r--r--   0        0        0        0 2023-06-30 00:41:54.566353 shiny_mdc-1.7.1/test/sections/empty.md
--rw-r--r--   0        0        0     2326 2023-06-30 00:41:54.566353 shiny_mdc-1.7.1/test/sections/main1.md
--rw-r--r--   0        0        0     1351 2023-06-30 00:41:54.566353 shiny_mdc-1.7.1/test/sections/main2.md
--rw-r--r--   0        0        0      992 2023-06-30 00:41:54.566353 shiny_mdc-1.7.1/test/utils/commands.md
--rw-r--r--   0        0        0       41 2023-06-30 00:41:54.566353 shiny_mdc-1.7.1/test/utils/ext.md
--rw-r--r--   0        0        0     1043 1970-01-01 00:00:00.000000 shiny_mdc-1.7.1/PKG-INFO
+-rw-r--r--   0        0        0     8088 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/CHANGELOG.md
+-rw-r--r--   0        0        0     1082 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/LICENSE
+-rw-r--r--   0        0        0       78 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/README.md
+-rw-r--r--   0        0        0     2313 2023-07-23 18:19:49.918340 shiny_mdc-1.8.0/pyproject.toml
+-rw-r--r--   0        0        0       34 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/__init__.py
+-rw-r--r--   0        0        0     1309 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/_latexmk.py
+-rw-r--r--   0        0        0     1867 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/_liquid.py
+-rw-r--r--   0        0        0     4920 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/_pandoc.py
+-rw-r--r--   0        0        0     5100 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/_templates.py
+-rw-r--r--   0        0        0       64 2023-07-23 18:19:49.918340 shiny_mdc-1.8.0/shinymdc/_version.py
+-rw-r--r--   0        0        0      410 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/dynamic/addappendices.tex
+-rw-r--r--   0        0        0      879 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/dynamic/authsetup.tex
+-rw-r--r--   0        0        0      316 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/dynamic/authsetupshort.tex
+-rw-r--r--   0        0        0      572 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/dynamic/dblfloatsetup.tex
+-rw-r--r--   0        0        0      130 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/dynamic/pdfsetup.tex
+-rw-r--r--   0        0        0      491 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/bibnonatsetup.tex
+-rw-r--r--   0        0        0      345 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/bibnosupersetup.tex
+-rw-r--r--   0        0        0      721 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/bibsupersetup.tex
+-rw-r--r--   0        0        0     3266 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/floatsetup.tex
+-rw-r--r--   0        0        0    19901 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/iccv/bibstyle.bst
+-rw-r--r--   0        0        0     9433 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/iccv/esopic.sty
+-rw-r--r--   0        0        0     3869 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/iccv/everyshi.sty
+-rw-r--r--   0        0        0     8276 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/iccv/iccv.sty
+-rw-r--r--   0        0        0    26973 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/iclr/bibstyle.bst
+-rw-r--r--   0        0        0     9153 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/iclr/iclr.sty
+-rw-r--r--   0        0        0    12284 2023-07-23 18:19:29.762355 shiny_mdc-1.8.0/shinymdc/resources/static/iclr/mathcommands.tex
+-rw-r--r--   0        0        0    27146 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/resources/static/icml/bibstyle.bst
+-rw-r--r--   0        0        0    27887 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/resources/static/icml/icml.sty
+-rw-r--r--   0        0        0      735 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/resources/static/mathsetup.tex
+-rw-r--r--   0        0        0     1033 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/resources/static/miscsetup.tex
+-rw-r--r--   0        0        0    11306 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/resources/static/neurips/neurips.sty
+-rw-r--r--   0        0        0      503 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/resources/static/reqsetup.tex
+-rw-r--r--   0        0        0    19840 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/shinymdc.py
+-rw-r--r--   0        0        0     1062 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/templates/basic.tex
+-rw-r--r--   0        0        0     1354 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/templates/iccv.tex
+-rw-r--r--   0        0        0     1475 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/templates/iclr.tex
+-rw-r--r--   0        0        0     2222 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/templates/icml.tex
+-rw-r--r--   0        0        0      968 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/templates/neurips.tex
+-rw-r--r--   0        0        0     3172 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/templates/spacious.tex
+-rw-r--r--   0        0        0      464 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/templates/standalone.tex
+-rw-r--r--   0        0        0     2678 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/shinymdc/templates/stylish.tex
+-rw-r--r--   0        0        0    15953 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/test/figures/anscombe.pdf
+-rw-r--r--   0        0        0    40892 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/test/figures/densities.pdf
+-rw-r--r--   0        0        0    10736 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/test/figures/diamonds.pdf
+-rw-r--r--   0        0        0   197017 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/test/figures/gaussian2d.pdf
+-rw-r--r--   0        0        0    28282 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/test/figures/lines.png
+-rw-r--r--   0        0        0     2988 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/test/main.md
+-rwxr-xr-x   0        0        0      315 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/test/make.sh
+-rw-r--r--   0        0        0     1166 2023-07-23 18:19:29.766355 shiny_mdc-1.8.0/test/references.bib
+-rw-r--r--   0        0        0   690901 2023-07-23 18:19:29.770355 shiny_mdc-1.8.0/test/samples/basic.pdf
+-rw-r--r--   0        0        0   414185 2023-07-23 18:19:29.774355 shiny_mdc-1.8.0/test/samples/iccv.pdf
+-rw-r--r--   0        0        0   407653 2023-07-23 18:19:29.774355 shiny_mdc-1.8.0/test/samples/iclr.pdf
+-rw-r--r--   0        0        0   446740 2023-07-23 18:19:29.778355 shiny_mdc-1.8.0/test/samples/icml.pdf
+-rw-r--r--   0        0        0   451322 2023-07-23 18:19:29.778355 shiny_mdc-1.8.0/test/samples/neurips.pdf
+-rw-r--r--   0        0        0   600276 2023-07-23 18:19:29.782355 shiny_mdc-1.8.0/test/samples/spacious.pdf
+-rw-r--r--   0        0        0   555527 2023-07-23 18:19:29.782355 shiny_mdc-1.8.0/test/samples/standalone.pdf
+-rw-r--r--   0        0        0   425326 2023-07-23 18:19:29.786355 shiny_mdc-1.8.0/test/samples/stylish.pdf
+-rw-r--r--   0        0        0     1535 2023-07-23 18:19:29.786355 shiny_mdc-1.8.0/test/sections/appendix1.md
+-rw-r--r--   0        0        0     1624 2023-07-23 18:19:29.786355 shiny_mdc-1.8.0/test/sections/appendix2.md
+-rw-r--r--   0        0        0        0 2023-07-23 18:19:29.786355 shiny_mdc-1.8.0/test/sections/empty.md
+-rw-r--r--   0        0        0     2326 2023-07-23 18:19:29.786355 shiny_mdc-1.8.0/test/sections/main1.md
+-rw-r--r--   0        0        0     1351 2023-07-23 18:19:29.786355 shiny_mdc-1.8.0/test/sections/main2.md
+-rw-r--r--   0        0        0      992 2023-07-23 18:19:29.786355 shiny_mdc-1.8.0/test/utils/commands.md
+-rw-r--r--   0        0        0       41 2023-07-23 18:19:29.786355 shiny_mdc-1.8.0/test/utils/ext.md
+-rw-r--r--   0        0        0     1043 1970-01-01 00:00:00.000000 shiny_mdc-1.8.0/PKG-INFO
```

### Comparing `shiny_mdc-1.7.1/CHANGELOG.md` & `shiny_mdc-1.8.0/CHANGELOG.md`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,27 @@
 # Changelog
 
 All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.
 
+## [1.8.0](https://github.com/jayanthkoushik/shiny-mdc/compare/v1.7.1...v1.8.0) (2023-07-23)
+
+
+### Features
+
+* add options for strict and forced modes ([79f96b0](https://github.com/jayanthkoushik/shiny-mdc/commit/79f96b0ddd6d4a90b9ae2737a2b85e18d2ee01f9))
+* add resource to setup pdf metadata ([ad14fbc](https://github.com/jayanthkoushik/shiny-mdc/commit/ad14fbc47d3cd80b40dd7a3e29a8c9ec667a4221))
+* improve handling of footnotes and sub/super-scripts ([26911b2](https://github.com/jayanthkoushik/shiny-mdc/commit/26911b2007e21f0e0f0fe4047309e198a0be4549))
+* make improvements to stylish template ([1f1b4ad](https://github.com/jayanthkoushik/shiny-mdc/commit/1f1b4ad174d62df645e24636efdd7ca9fe0eb509))
+
+
+### Bug Fixes
+
+* fix url display for basic template ([95540b6](https://github.com/jayanthkoushik/shiny-mdc/commit/95540b6cf909bdcac22902fc6319f010a0538b29))
+* typeset document url in typewriter mode ([51967c2](https://github.com/jayanthkoushik/shiny-mdc/commit/51967c231b1e53128bbd2f361f0ec12830067aa1))
+
 ### [1.7.1](https://github.com/jayanthkoushik/shiny-mdc/compare/v1.7.0...v1.7.1) (2023-06-30)
 
 ## [1.7.0](https://github.com/jayanthkoushik/shiny-mdc/compare/v1.6.0...v1.7.0) (2023-06-29)
 
 
 ### Features
```

### Comparing `shiny_mdc-1.7.1/LICENSE` & `shiny_mdc-1.8.0/LICENSE`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/pyproject.toml` & `shiny_mdc-1.8.0/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "shiny-mdc"
-version = "1.7.1"  # managed by `poetry-dynamic-versioning`
+version = "1.8.0"  # managed by `poetry-dynamic-versioning`
 description = "Tool to compile markdown files to tex/pdf using pandoc, latexmk"
 readme = "README.md"
 authors = ["Jayanth Koushik <mail@jkoushik.me>"]
 license = "MIT"
 repository = "https://github.com/jayanthkoushik/shinymdc"
 packages = [
   { include = "shinymdc" }
```

### Comparing `shiny_mdc-1.7.1/shinymdc/_latexmk.py` & `shiny_mdc-1.8.0/shinymdc/_latexmk.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,35 +1,46 @@
 import subprocess
 import sys
 from pathlib import Path
 
 
 def run_latexmk(
-    input_path: Path, build_dir: Path, clean: bool = False, verbose: bool = False
+    input_path: Path,
+    build_dir: Path,
+    clean: bool = False,
+    verbose: bool = False,
+    force: bool = False,
+    strict: bool = False,
 ) -> Path:
     """Compile a LaTeX file using `latexmk`.
 
     Args:
         input_path: Path to input file.
         build_dir: Path to build directory.
         clean: Whether to do a clean build by passing `-gg` to `latexmk`.
         verbose: Whether to enable verbose output.
+        force: Whether to pass `-f` to `latexmk`.
+        strict: Whether to pass `-Werror` to `latexmk`.
 
     Returns:
         Path to output file.
 
     Raises:
         subprocess.CalledProcessError: If `latexmk` subprocess fails.
     """
-    cmd = ["latexmk", "-pdf", "-interaction=nonstopmode", "-lualatex", "-f"]
+    cmd = ["latexmk", "-pdf", "-interaction=nonstopmode", "-lualatex"]
 
     if clean:
         cmd.append("-gg")
     if not verbose:
         cmd.append("-silent")
+    if force:
+        cmd.append("-f")
+    if strict:
+        cmd.append("-Werror")
 
     cmd.append(f"-output-directory={build_dir}")
     cmd.append(str(input_path))
 
     print("+", *cmd, file=sys.stderr)
     subprocess.run(
         cmd,
```

### Comparing `shiny_mdc-1.7.1/shinymdc/_liquid.py` & `shiny_mdc-1.8.0/shinymdc/_liquid.py`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/_pandoc.py` & `shiny_mdc-1.8.0/shinymdc/_pandoc.py`

 * *Files 6% similar despite different names*

```diff
@@ -21,26 +21,28 @@
     input_path: Path,
     template_path: Path,
     bib_path: Optional[Path] = None,
     metadata_path: Optional[Path] = None,
     default_img_ext: Optional[str] = None,
     natbib: bool = False,
     verbose: bool = False,
+    strict: bool = False,
     **metadata,
 ) -> str:
     """Run `pandoc` to convert input markdown to LaTeX.
 
     Args:
         input_path: Path to input file.
         template_path: Path to template file.
         bib_path: Path to bibliography file.
         metadata_path: Path to metadata file.
         default_img_ext: Default image extension.
         natbib: Whether to use natbib for bibliography.
         verbose: Whether to enable verbose output.
+        strict: Whether to consider warnings as errors.
         metadata: Pandoc metadata (each key-value pair will be added using `-M`).
 
     Returns:
         Generated LaTeX text.
 
     Raises:
         subprocess.CalledProcessError: If `pandoc` subprocess fails.
@@ -61,14 +63,16 @@
         if natbib:
             cmd.append("--natbib")
 
     if default_img_ext is not None:
         cmd.append(f"--default-image-extension={default_img_ext}")
     if verbose:
         cmd.append("--verbose")
+    if strict:
+        cmd.append("--fail-if-warnings")
 
     base_metadata = BASE_METADATA.copy()
     base_metadata.update(metadata)
     for mk, mv in base_metadata.items():
         cmd.append(f"--metadata={mk}={mv}")
 
     cmd.append(str(input_path))
```

### Comparing `shiny_mdc-1.7.1/shinymdc/_templates.py` & `shiny_mdc-1.8.0/shinymdc/_templates.py`

 * *Files 1% similar despite different names*

```diff
@@ -65,15 +65,15 @@
             "neurips": ["neurips/neurips.sty", "bibnosupersetup.tex"],
         },
     )
     _dynamic_resources = defaultdict(
         list,
         {
             # Dynamic resources, defined similarly to static resources.
-            "*": ["addappendices.tex"],
+            "*": ["addappendices.tex", "pdfsetup.tex"],
             "basic": ["authsetup.tex"],
             "iccv": ["authsetup.tex", "dblfloatsetup.tex"],
             "iclr": ["authsetup.tex"],
             "icml": ["dblfloatsetup.tex"],
             "neurips": ["authsetup.tex"],
             "spacious": ["authsetupshort.tex"],
             "stylish": ["authsetupshort.tex", "dblfloatsetup.tex"],
```

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/dynamic/authsetup.tex` & `shiny_mdc-1.8.0/shinymdc/resources/dynamic/authsetup.tex`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/dynamic/dblfloatsetup.tex` & `shiny_mdc-1.8.0/shinymdc/resources/dynamic/dblfloatsetup.tex`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/bibsupersetup.tex` & `shiny_mdc-1.8.0/shinymdc/resources/static/bibsupersetup.tex`

 * *Files 18% similar despite different names*

```diff
@@ -1,15 +1,14 @@
 \ifdefined\nobibcompress
   \usepackage[square,numbers,sort]{natbib}
 \else
   \usepackage[square,numbers,sort&compress]{natbib}
 \fi
 \usepackage{xparse}
 \usepackage{letltxmacro}
-% \usepackage{etoolbox}
 
 \LetLtxMacro\oldcitep\citep
 \RenewDocumentCommand\citep{o o m}{%
   \textsuperscript{%
     \IfNoValueTF{#1}{%
       \oldcitep{#3}%
     }{%
```

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/floatsetup.tex` & `shiny_mdc-1.8.0/shinymdc/resources/static/floatsetup.tex`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/iccv/bibstyle.bst` & `shiny_mdc-1.8.0/shinymdc/resources/static/iccv/bibstyle.bst`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/iccv/esopic.sty` & `shiny_mdc-1.8.0/shinymdc/resources/static/iccv/esopic.sty`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/iccv/everyshi.sty` & `shiny_mdc-1.8.0/shinymdc/resources/static/iccv/everyshi.sty`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/iccv/iccv.sty` & `shiny_mdc-1.8.0/shinymdc/resources/static/iccv/iccv.sty`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/iclr/bibstyle.bst` & `shiny_mdc-1.8.0/shinymdc/resources/static/iclr/bibstyle.bst`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/iclr/iclr.sty` & `shiny_mdc-1.8.0/shinymdc/resources/static/iclr/iclr.sty`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/iclr/mathcommands.tex` & `shiny_mdc-1.8.0/shinymdc/resources/static/iclr/mathcommands.tex`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/icml/bibstyle.bst` & `shiny_mdc-1.8.0/shinymdc/resources/static/icml/bibstyle.bst`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/icml/icml.sty` & `shiny_mdc-1.8.0/shinymdc/resources/static/icml/icml.sty`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/mathsetup.tex` & `shiny_mdc-1.8.0/shinymdc/resources/static/mathsetup.tex`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/resources/static/neurips/neurips.sty` & `shiny_mdc-1.8.0/shinymdc/resources/static/neurips/neurips.sty`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/shinymdc/shinymdc.py` & `shiny_mdc-1.8.0/shinymdc/shinymdc.py`

 * *Files 2% similar despite different names*

```diff
@@ -21,14 +21,16 @@
 
 class ShinyMDC(Corgy, corgy_required_by_default=True):
     Flag = Literal[True]
 
     clean: NotRequired[Annotated[Flag, "do a clean build", ["-c", "--clean"]]]
     verbose: NotRequired[Annotated[Flag, "enable verbose output", ["-v", "--verbose"]]]
     quiet: NotRequired[Annotated[Flag, "suppress all output", ["-q", "--quiet"]]]
+    force: NotRequired[Annotated[Flag, "continue past 'latexmk' errors"]]
+    strict: NotRequired[Annotated[Flag, "treat warnings as errors"]]
 
     input_path: NotRequired[
         Annotated[
             Path,
             "input markdown file (will read from standard input if not specified)",
             ["-i", "--input"],
         ]
@@ -329,14 +331,15 @@
                 combined_liquified_md_path,
                 stub_template_path,
                 bib_path,
                 None,  # metadata_path
                 getattr(self, "default_img_ext", None),
                 self.natbib,
                 hasattr(self, "verbose"),
+                hasattr(self, "strict"),
                 **self.meta,
             )
 
         # Split compiled latex into constituent parts.
         parts = combined_tex.split(primary_sep.strip())
         body_tex = parts[0].strip()
         abstract_tex = parts[1].strip()
@@ -432,14 +435,15 @@
                     Path(os.devnull),
                     resc_path,
                     bib_path,
                     metadata_path,
                     getattr(self, "default_img_ext", None),
                     self.natbib,
                     hasattr(self, "verbose"),
+                    hasattr(self, "strict"),
                     **self.meta,
                 )
                 processed_resc_path = rescs_dir / f"{resc_name}{resc_path.suffix}"
                 print(f"+ write '{processed_resc_path}'", file=sys.stderr)
                 processed_resc_path.write_text(processed_resc_tex)
                 metadata[resc_name] = str(processed_resc_path.with_suffix(""))
 
@@ -452,14 +456,15 @@
                 Path(os.devnull),
                 template_path,
                 bib_path,
                 metadata_path,
                 getattr(self, "default_img_ext", None),
                 self.natbib,
                 hasattr(self, "verbose"),
+                hasattr(self, "strict"),
                 **self.meta,
             )
 
         # Write main tex to file.
         print(f"+ write '{self.main_tex_path}'", file=sys.stderr)
         self.main_tex_path.write_text(main_tex)
 
@@ -472,14 +477,16 @@
         print(f"+ mkdir -p '{latexmk_build_dir}'", file=sys.stderr)
         latexmk_build_dir.mkdir(exist_ok=True)
         result_path = run_latexmk(
             self.main_tex_path,
             latexmk_build_dir,
             hasattr(self, "clean"),
             hasattr(self, "verbose"),
+            hasattr(self, "force"),
+            hasattr(self, "strict"),
         )
 
         # Copy result to output file or write it to stdout.
         if hasattr(self, "output_path"):
             print(f"+ cp '{result_path}' '{self.output_path}'", file=sys.stderr)
             shutil.copy(result_path, self.output_path)
         else:
```

### Comparing `shiny_mdc-1.7.1/shinymdc/templates/basic.tex` & `shiny_mdc-1.8.0/shinymdc/templates/basic.tex`

 * *Files 18% similar despite different names*

```diff
@@ -9,14 +9,15 @@
 \usepackage{parskip}
 
 \input{$reqsetup$}
 \input{$floatsetup$}
 \input{$mathsetup$}
 \input{$bibsupersetup$}
 \input{$miscsetup$}
+\input{$pdfsetup$}
 
 % Increase maximum figure/table widths.
 \renewcommand{\maxfigwidth}{6.5in}
 \renewcommand{\maxtabwidth}{6.5in}
 
 \title{\vspace{-5ex} $title$}
 \date{$if(date)$$date$$endif$}
@@ -28,21 +29,22 @@
 $endfor$
 
 \begin{document}
 
 \setnowidow[2]
 \maketitle
 
+$if(url)$
+\blfootnote{This document can be read online at \href{$url$}{\texttt{$url$}}.}
+$endif$
+
 % Add equal-contrib footnote.
 $if(skipequal)$
 $else$
-\blfootnote{%
-$if(url)$This document can be read online at \url{$url$}.\\$endif$%
-\textsuperscript{*}\,Equal contribution.%
-}
+\blfootnote{\textsuperscript{*}\,Equal contribution.}
 $endif$
 
 $if(abstract)$
 \section*{Abstract}
 $abstract$
 $endif$
```

### Comparing `shiny_mdc-1.7.1/shinymdc/templates/iccv.tex` & `shiny_mdc-1.8.0/shinymdc/templates/iccv.tex`

 * *Files 3% similar despite different names*

```diff
@@ -14,14 +14,19 @@
 \input{$reqsetup$}
 \input{$floatsetup$}
 \input{$dblfloatsetup$}
 \input{$mathsetup$}
 \input{$miscsetup$}
 \input{$bibnonatsetup$}
 
+$if(submission)$
+$else$
+\input{$pdfsetup$}
+$endif$
+
 $if(submission)$$else$\iccvfinalcopy$endif$
 
 \def\iccvPaperID{$paperid$}
 \def\httilde{\mbox{\tt\raisebox{-.5ex}{\symbol{126}}}}
 
 % Pages are numbered in submission mode, and unnumbered in camera-ready.
 \ificcvfinal\pagestyle{empty}\fi
```

### Comparing `shiny_mdc-1.7.1/shinymdc/templates/iclr.tex` & `shiny_mdc-1.8.0/shinymdc/templates/iclr.tex`

 * *Files 4% similar despite different names*

```diff
@@ -5,14 +5,19 @@
 
 \input{$reqsetup$}
 \input{$floatsetup$}
 \input{$mathsetup$}
 \input{$miscsetup$}
 \input{$bibnosupersetup$}
 
+$if(submission)$
+$else$
+\input{$pdfsetup$}
+$endif$
+
 % Optional math commands from https://github.com/goodfeli/dlbook_notation.
 % \input{$mathcommands$.tex}
 
 \title{$title$}
 
 % The \author macro works with any number of authors. There are two commands
 % used to separate the names and addresses of multiple authors: \And and \AND.
```

### Comparing `shiny_mdc-1.7.1/shinymdc/templates/icml.tex` & `shiny_mdc-1.8.0/shinymdc/templates/icml.tex`

 * *Files 4% similar despite different names*

```diff
@@ -6,14 +6,19 @@
 
 \input{$floatsetup$}
 \input{$dblfloatsetup$}
 \input{$mathsetup$}
 \input{$miscsetup$}
 \input{$bibnosupersetup$}
 
+$if(submission)$
+$else$
+\input{$pdfsetup$}
+$endif$
+
 %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
 % THEOREMS
 %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
 \theoremstyle{plain}
 \newtheorem{theorem}{Theorem}[section]
 \newtheorem{proposition}[theorem]{Proposition}
 \newtheorem{lemma}[theorem]{Lemma}
```

### Comparing `shiny_mdc-1.7.1/shinymdc/templates/neurips.tex` & `shiny_mdc-1.8.0/shinymdc/templates/neurips.tex`

 * *Files 4% similar despite different names*

```diff
@@ -11,14 +11,19 @@
 
 \input{$reqsetup$}
 \input{$floatsetup$}
 \input{$mathsetup$}
 \input{$miscsetup$}
 \input{$bibnosupersetup$}
 
+$if(submission)$
+$else$
+\input{$pdfsetup$}
+$endif$
+
 \title{$title$}
 
 \input{$authsetup$}
 
 $for(includes)$
 $it$
 $endfor$
```

### Comparing `shiny_mdc-1.7.1/shinymdc/templates/spacious.tex` & `shiny_mdc-1.8.0/shinymdc/templates/spacious.tex`

 * *Files 3% similar despite different names*

```diff
@@ -13,14 +13,15 @@
 % \usepackage{ebgaramond}
 
 \input{$reqsetup$}
 \input{$floatsetup$}
 \input{$mathsetup$}
 \input{$bibsupersetup$}
 \input{$miscsetup$}
+\input{$pdfsetup$}
 
 % Increase maximum figure/table sizes.
 \renewcommand{\maxfigwidth}{6.5in}
 \renewcommand{\maxfigheight}{10in}
 \renewcommand{\maxtabwidth}{6.5in}
 \renewcommand{\maxtabheight}{10in}
 
@@ -91,15 +92,15 @@
 \thispagestyle{empty}
 \parindent=3em
 
 % Add author-info footnote.
 \blfootnote{%
   {%
     \normalfont\scriptsize\raggedright%
-    $if(url)$This document can be read online at \url{$url$}.\\$endif$%
+    $if(url)$This document can be read online at \href{$url$}{\texttt{$url$}}.\\$endif$%
     $if(skipequal)$$else$\mbox{\textsuperscript{*}\,Equal contribution.}\enskip$endif$%
     $for(institute)$\mbox{\textsuperscript{$institute.id$}\,$institute.name$.}\enskip$endfor$%
   }%
 }
 
 $if(abstract)$
 \section*{Abstract}
```

### Comparing `shiny_mdc-1.7.1/shinymdc/templates/stylish.tex` & `shiny_mdc-1.8.0/shinymdc/templates/stylish.tex`

 * *Files 17% similar despite different names*

```diff
@@ -1,48 +1,54 @@
 \RequirePackage{amssymb}
 \RequirePackage{amsthm}
 \PassOptionsToPackage{hidelinks}{hyperref}
+\PassOptionsToPackage{defaultlines=2,all}{nowidow}
 
 \documentclass[%
   letterpaper,%
   twocolumn,%
   $if(lang)$$lang$$else$english$endif$%
 ]{article}
 
 \usepackage[%
   textwidth=492pt,%
   textheight=624pt,%
   columnsep=12pt,%
-  footskip=50pt,%
-  footnotesep=50pt%
+  footskip=48pt,%
+  footnotesep=36pt%
 ]{geometry}
 \usepackage[sf,big,raggedright,compact]{titlesec}
 \usepackage{fancyhdr}
-\usepackage{newtx}
+\usepackage[p]{newtx}
 \usepackage{etoolbox}
 
 \def\nobibcompress{TRUE}
 \input{$reqsetup$}
 \input{$floatsetup$}
 \input{$dblfloatsetup$}
 \input{$mathsetup$}
 \input{$bibsupersetup$}
 \input{$miscsetup$}
+\input{$pdfsetup$}
 
 $if(smalltabs)$
 % Use small font for tables.
 \AtBeginEnvironment{tabular}{\smaller}
 $else$
 $endif$
 
-% Don't use smallcaps for acronyms.
-\renewcommand*{\acsfont}[1]{{\textsmaller{#1}}}
+% Reset acronym font.
+\renewcommand*{\acsfont}[1]{#1}
 
-% Configure caption font.
+\renewcommand*{\thefootnote}{\alph{footnote}}
+
+% Configure captions.
 \captionsetup{justification=raggedright,font={sf,small}}
+\renewcommand\thesubfigure{(\alph{subfigure})}
+\captionsetup[subfigure]{labelformat=simple}
 
 % Add periods after section numbers.
 \titlelabel{\thetitle.\enskip}
 
 % Configure page no.
 \pagestyle{fancy}
 \fancyhf{}
@@ -92,15 +98,15 @@
 \thispagestyle{fancy}
 \parindent=2em
 
 % Add author-info footnote.
 \blfootnote{%
   {%
     \normalfont\sffamily\scriptsize%
-    $if(url)$This document can be read online at \url{$url$}.\\$endif$%
+    $if(url)$This document can be read online at \href{$url$}{\texttt{$url$}}.\\$endif$%
     $if(skipequal)$$else$\mbox{\textsuperscript{*}\,Equal contribution.}\enskip$endif$%
     $for(institute)$\mbox{\textsuperscript{$institute.id$}\,$institute.name$.}\enskip$endfor$%
   }%
 }
 
 $if(abstract)$
 \hrule height 1pt
```

### Comparing `shiny_mdc-1.7.1/test/figures/anscombe.pdf` & `shiny_mdc-1.8.0/test/figures/anscombe.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/figures/densities.pdf` & `shiny_mdc-1.8.0/test/figures/densities.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/figures/diamonds.pdf` & `shiny_mdc-1.8.0/test/figures/diamonds.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/figures/gaussian2d.pdf` & `shiny_mdc-1.8.0/test/figures/gaussian2d.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/figures/lines.png` & `shiny_mdc-1.8.0/test/figures/lines.png`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/main.md` & `shiny_mdc-1.8.0/test/main.md`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/references.bib` & `shiny_mdc-1.8.0/test/references.bib`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/samples/basic.pdf` & `shiny_mdc-1.8.0/test/samples/basic.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/samples/iccv.pdf` & `shiny_mdc-1.8.0/test/samples/iccv.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/samples/iclr.pdf` & `shiny_mdc-1.8.0/test/samples/iclr.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/samples/icml.pdf` & `shiny_mdc-1.8.0/test/samples/icml.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/samples/neurips.pdf` & `shiny_mdc-1.8.0/test/samples/neurips.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/samples/spacious.pdf` & `shiny_mdc-1.8.0/test/samples/spacious.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/samples/standalone.pdf` & `shiny_mdc-1.8.0/test/samples/standalone.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/samples/stylish.pdf` & `shiny_mdc-1.8.0/test/samples/stylish.pdf`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/sections/appendix1.md` & `shiny_mdc-1.8.0/test/sections/appendix1.md`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/sections/appendix2.md` & `shiny_mdc-1.8.0/test/sections/appendix2.md`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/sections/main1.md` & `shiny_mdc-1.8.0/test/sections/main1.md`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/sections/main2.md` & `shiny_mdc-1.8.0/test/sections/main2.md`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/test/utils/commands.md` & `shiny_mdc-1.8.0/test/utils/commands.md`

 * *Files identical despite different names*

### Comparing `shiny_mdc-1.7.1/PKG-INFO` & `shiny_mdc-1.8.0/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: shiny-mdc
-Version: 1.7.1
+Version: 1.8.0
 Summary: Tool to compile markdown files to tex/pdf using pandoc, latexmk
 Home-page: https://github.com/jayanthkoushik/shinymdc
 License: MIT
 Author: Jayanth Koushik
 Author-email: mail@jkoushik.me
 Requires-Python: >=3.9,<4.0
 Classifier: Development Status :: 4 - Beta
```

