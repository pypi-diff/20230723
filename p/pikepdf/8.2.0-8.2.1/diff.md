# Comparing `tmp/pikepdf-8.2.0.tar.gz` & `tmp/pikepdf-8.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pikepdf-8.2.0.tar", last modified: Fri Jul 21 23:42:03 2023, max compression
+gzip compressed data, was "pikepdf-8.2.1.tar", last modified: Sun Jul 23 08:28:49 2023, max compression
```

## Comparing `pikepdf-8.2.0.tar` & `pikepdf-8.2.1.tar`

### file list

```diff
@@ -1,130 +1,130 @@
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-21 23:42:03.612349 pikepdf-8.2.0/
--rw-r--r--   0 runner    (1001) docker     (122)    16725 2023-07-21 23:39:17.000000 pikepdf-8.2.0/LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (122)      122 2023-07-21 23:39:17.000000 pikepdf-8.2.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (122)     7294 2023-07-21 23:42:03.612349 pikepdf-8.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (122)     6158 2023-07-21 23:39:17.000000 pikepdf-8.2.0/README.md
--rw-r--r--   0 runner    (1001) docker     (122)     5924 2023-07-21 23:39:17.000000 pikepdf-8.2.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (122)       38 2023-07-21 23:42:03.612349 pikepdf-8.2.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (122)     3856 2023-07-21 23:39:17.000000 pikepdf-8.2.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-21 23:42:03.592349 pikepdf-8.2.0/src/
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-21 23:42:03.596349 pikepdf-8.2.0/src/core/
--rw-r--r--   0 runner    (1001) docker     (122)     4478 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/annotation.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     7216 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/embeddedfiles.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     3953 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/jbig2-inl.h
--rw-r--r--   0 runner    (1001) docker     (122)     5806 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/job.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     2256 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/logger.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     5731 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/mmap_inputsource-inl.h
--rw-r--r--   0 runner    (1001) docker     (122)     3621 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/nametree.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     3001 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/numbertree.cpp
--rw-r--r--   0 runner    (1001) docker     (122)    42072 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/object.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     5786 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/object_convert.cpp
--rw-r--r--   0 runner    (1001) docker     (122)    10569 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/object_repr.cpp
--rw-r--r--   0 runner    (1001) docker     (122)    14256 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/page.cpp
--rw-r--r--   0 runner    (1001) docker     (122)    11199 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/parsers.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     2156 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/parsers.h
--rw-r--r--   0 runner    (1001) docker     (122)     8253 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/pikepdf.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     5700 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/pikepdf.h
--rw-r--r--   0 runner    (1001) docker     (122)     1274 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/pipeline.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     1063 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/pipeline.h
--rw-r--r--   0 runner    (1001) docker     (122)    37394 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/qpdf.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     5594 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/qpdf_inputsource-inl.h
--rw-r--r--   0 runner    (1001) docker     (122)    15512 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/qpdf_pagelist.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     1144 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/qpdf_pagelist.h
--rw-r--r--   0 runner    (1001) docker     (122)     3901 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/rectangle.cpp
--rw-r--r--   0 runner    (1001) docker     (122)     5455 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/tokenfilter.cpp
--rw-r--r--   0 runner    (1001) docker     (122)      595 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/utils.cpp
--rw-r--r--   0 runner    (1001) docker     (122)      565 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/core/utils.h
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-21 23:42:03.600349 pikepdf-8.2.0/src/pikepdf/
--rw-r--r--   0 runner    (1001) docker     (122)     3001 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     6161 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/_augments.py
--rw-r--r--   0 runner    (1001) docker     (122)     3030 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/_cpphelpers.py
--rw-r--r--   0 runner    (1001) docker     (122)      232 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/_exceptions.py
--rw-r--r--   0 runner    (1001) docker     (122)     1666 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/_io.py
--rw-r--r--   0 runner    (1001) docker     (122)    57488 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/_methods.py
--rw-r--r--   0 runner    (1001) docker     (122)     1876 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/_qpdf.py
--rw-r--r--   0 runner    (1001) docker     (122)      879 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/_xml.py
--rw-r--r--   0 runner    (1001) docker     (122)     5952 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/codec.py
--rw-r--r--   0 runner    (1001) docker     (122)     3378 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/jbig2.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-21 23:42:03.600349 pikepdf-8.2.0/src/pikepdf/models/
--rw-r--r--   0 runner    (1001) docker     (122)     1139 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)     4950 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/models/_content_stream.py
--rw-r--r--   0 runner    (1001) docker     (122)     8204 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/models/_transcoding.py
--rw-r--r--   0 runner    (1001) docker     (122)     5499 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/models/encryption.py
--rw-r--r--   0 runner    (1001) docker     (122)    36349 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/models/image.py
--rw-r--r--   0 runner    (1001) docker     (122)     5979 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/models/matrix.py
--rw-r--r--   0 runner    (1001) docker     (122)    32023 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/models/metadata.py
--rw-r--r--   0 runner    (1001) docker     (122)    15420 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/models/outlines.py
--rw-r--r--   0 runner    (1001) docker     (122)    10415 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/objects.py
--rw-r--r--   0 runner    (1001) docker     (122)      101 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/py.typed
--rw-r--r--   0 runner    (1001) docker     (122)      369 2023-07-21 23:39:17.000000 pikepdf-8.2.0/src/pikepdf/settings.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-21 23:42:03.600349 pikepdf-8.2.0/src/pikepdf.egg-info/
--rw-r--r--   0 runner    (1001) docker     (122)     7294 2023-07-21 23:42:03.000000 pikepdf-8.2.0/src/pikepdf.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (122)     3097 2023-07-21 23:42:03.000000 pikepdf-8.2.0/src/pikepdf.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-21 23:42:03.000000 pikepdf-8.2.0/src/pikepdf.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (122)      688 2023-07-21 23:42:03.000000 pikepdf-8.2.0/src/pikepdf.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (122)       13 2023-07-21 23:42:03.000000 pikepdf-8.2.0/src/pikepdf.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-21 23:42:03.604349 pikepdf-8.2.0/tests/
--rw-r--r--   0 runner    (1001) docker     (122)     1731 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-21 23:42:03.612349 pikepdf-8.2.0/tests/resources/
--rw-r--r--   0 runner    (1001) docker     (122)     5661 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/1biticc.pdf
--rw-r--r--   0 runner    (1001) docker     (122)      420 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/Gray.icc
--rw-r--r--   0 runner    (1001) docker     (122)     1734 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/aquamarine-cie.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     1940 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/aquamarine-cie.png
--rw-r--r--   0 runner    (1001) docker     (122)     1461 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/cmyk-jpeg.pdf
--rw-r--r--   0 runner    (1001) docker     (122)    97969 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/congress-gray.pdf
--rw-r--r--   0 runner    (1001) docker     (122)   193947 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/congress.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     2889 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/content-stream-errors.pdf
--rw-r--r--   0 runner    (1001) docker     (122)    10876 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/form.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     2713 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/formxobject.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     2916 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/fourpages.pdf
--rw-r--r--   0 runner    (1001) docker     (122)   296661 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/graph-encrypted.pdf
--rw-r--r--   0 runner    (1001) docker     (122)   296322 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/graph.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     1544 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/image-mono-inline.pdf
--rw-r--r--   0 runner    (1001) docker     (122)      965 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/invalid_creationdate.pdf
--rw-r--r--   0 runner    (1001) docker     (122)    20306 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/jbig2.pdf
--rw-r--r--   0 runner    (1001) docker     (122)    60332 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/jbig2global.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     6994 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/outlines.pdf
--rw-r--r--   0 runner    (1001) docker     (122)      931 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/pal-1bit-rgb.pdf
--rw-r--r--   0 runner    (1001) docker     (122)      931 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/pal-1bit-trivial.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     2918 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/pal.pdf
--rwxr-xr-x   0 runner    (1001) docker     (122)   533953 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/pdfx.pdf
--rw-r--r--   0 runner    (1001) docker     (122)    18471 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/pike-flate-jp2.pdf
--rw-r--r--   0 runner    (1001) docker     (122)    18152 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/pike-jp2.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     2681 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/pink-palette-icc.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     2698 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/pink-palette-icc.png
--rw-r--r--   0 runner    (1001) docker     (122)     5432 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/rle.pdf
--rw-r--r--   0 runner    (1001) docker     (122)   115546 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/sandwich.pdf
--rw-r--r--   0 runner    (1001) docker     (122)    10049 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/veraPDF test suite 6-2-10-t02-pass-a.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     2676 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/resources/veraPDF test suite 6-2-3-3-t01-fail-c.pdf
--rw-r--r--   0 runner    (1001) docker     (122)     1439 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_annotation.py
--rw-r--r--   0 runner    (1001) docker     (122)     4721 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_attachments.py
--rw-r--r--   0 runner    (1001) docker     (122)     1312 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_augments.py
--rw-r--r--   0 runner    (1001) docker     (122)     4453 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_codec.py
--rw-r--r--   0 runner    (1001) docker     (122)     1961 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_decimal.py
--rw-r--r--   0 runner    (1001) docker     (122)     1181 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_dictionary.py
--rw-r--r--   0 runner    (1001) docker     (122)     5610 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_encrypt.py
--rw-r--r--   0 runner    (1001) docker     (122)     1690 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_errors.py
--rw-r--r--   0 runner    (1001) docker     (122)     3404 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_filters.py
--rw-r--r--   0 runner    (1001) docker     (122)     3135 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_foreign.py
--rw-r--r--   0 runner    (1001) docker     (122)     1988 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_formxobject.py
--rw-r--r--   0 runner    (1001) docker     (122)    36948 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_image_access.py
--rw-r--r--   0 runner    (1001) docker     (122)     9944 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_io.py
--rw-r--r--   0 runner    (1001) docker     (122)     2498 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_ipython.py
--rw-r--r--   0 runner    (1001) docker     (122)     2036 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_job.py
--rw-r--r--   0 runner    (1001) docker     (122)     1523 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_matrix.py
--rw-r--r--   0 runner    (1001) docker     (122)    25184 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_metadata.py
--rw-r--r--   0 runner    (1001) docker     (122)     2094 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_nametree.py
--rw-r--r--   0 runner    (1001) docker     (122)     2301 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_numbertree.py
--rw-r--r--   0 runner    (1001) docker     (122)    22294 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_object.py
--rw-r--r--   0 runner    (1001) docker     (122)      565 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_objectlist.py
--rw-r--r--   0 runner    (1001) docker     (122)    17177 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_outlines.py
--rw-r--r--   0 runner    (1001) docker     (122)     9131 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_page.py
--rw-r--r--   0 runner    (1001) docker     (122)    15569 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_pages.py
--rw-r--r--   0 runner    (1001) docker     (122)     9522 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_parsers.py
--rw-r--r--   0 runner    (1001) docker     (122)    13773 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_pdf.py
--rw-r--r--   0 runner    (1001) docker     (122)     3956 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_pdfa.py
--rw-r--r--   0 runner    (1001) docker     (122)      754 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_private_pdfs.py
--rw-r--r--   0 runner    (1001) docker     (122)     1393 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_rectangle.py
--rw-r--r--   0 runner    (1001) docker     (122)     2032 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_refcount.py
--rw-r--r--   0 runner    (1001) docker     (122)     3744 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_repr.py
--rw-r--r--   0 runner    (1001) docker     (122)     4682 2023-07-21 23:39:17.000000 pikepdf-8.2.0/tests/test_sanity.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 08:28:49.359531 pikepdf-8.2.1/
+-rw-r--r--   0 runner    (1001) docker     (122)    16725 2023-07-23 08:25:31.000000 pikepdf-8.2.1/LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (122)      122 2023-07-23 08:25:31.000000 pikepdf-8.2.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (122)     6958 2023-07-23 08:28:49.359531 pikepdf-8.2.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (122)     5821 2023-07-23 08:25:31.000000 pikepdf-8.2.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (122)     5978 2023-07-23 08:25:31.000000 pikepdf-8.2.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (122)       38 2023-07-23 08:28:49.359531 pikepdf-8.2.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (122)     3856 2023-07-23 08:25:31.000000 pikepdf-8.2.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 08:28:49.331531 pikepdf-8.2.1/src/
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 08:28:49.339531 pikepdf-8.2.1/src/core/
+-rw-r--r--   0 runner    (1001) docker     (122)     4478 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/annotation.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     7216 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/embeddedfiles.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     3953 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/jbig2-inl.h
+-rw-r--r--   0 runner    (1001) docker     (122)     5806 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/job.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     2256 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/logger.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     5731 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/mmap_inputsource-inl.h
+-rw-r--r--   0 runner    (1001) docker     (122)     3621 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/nametree.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     3001 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/numbertree.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)    42072 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/object.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     5786 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/object_convert.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)    10569 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/object_repr.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)    14256 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/page.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)    11199 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/parsers.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     2156 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/parsers.h
+-rw-r--r--   0 runner    (1001) docker     (122)     8253 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/pikepdf.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     5700 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/pikepdf.h
+-rw-r--r--   0 runner    (1001) docker     (122)     1274 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/pipeline.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     1063 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/pipeline.h
+-rw-r--r--   0 runner    (1001) docker     (122)    37394 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/qpdf.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     5594 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/qpdf_inputsource-inl.h
+-rw-r--r--   0 runner    (1001) docker     (122)    15512 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/qpdf_pagelist.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     1144 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/qpdf_pagelist.h
+-rw-r--r--   0 runner    (1001) docker     (122)     3901 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/rectangle.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)     5455 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/tokenfilter.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)      595 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/utils.cpp
+-rw-r--r--   0 runner    (1001) docker     (122)      565 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/core/utils.h
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 08:28:49.339531 pikepdf-8.2.1/src/pikepdf/
+-rw-r--r--   0 runner    (1001) docker     (122)     3001 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6161 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/_augments.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3030 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/_cpphelpers.py
+-rw-r--r--   0 runner    (1001) docker     (122)      232 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/_exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1666 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/_io.py
+-rw-r--r--   0 runner    (1001) docker     (122)    57488 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/_methods.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1876 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/_qpdf.py
+-rw-r--r--   0 runner    (1001) docker     (122)      879 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/_xml.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5952 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/codec.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3378 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/jbig2.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 08:28:49.343531 pikepdf-8.2.1/src/pikepdf/models/
+-rw-r--r--   0 runner    (1001) docker     (122)     1139 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4950 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/models/_content_stream.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8204 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/models/_transcoding.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5499 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/models/encryption.py
+-rw-r--r--   0 runner    (1001) docker     (122)    36349 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/models/image.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5979 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/models/matrix.py
+-rw-r--r--   0 runner    (1001) docker     (122)    32023 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/models/metadata.py
+-rw-r--r--   0 runner    (1001) docker     (122)    15420 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/models/outlines.py
+-rw-r--r--   0 runner    (1001) docker     (122)    10415 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/objects.py
+-rw-r--r--   0 runner    (1001) docker     (122)      101 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/py.typed
+-rw-r--r--   0 runner    (1001) docker     (122)      369 2023-07-23 08:25:31.000000 pikepdf-8.2.1/src/pikepdf/settings.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 08:28:49.343531 pikepdf-8.2.1/src/pikepdf.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (122)     6958 2023-07-23 08:28:49.000000 pikepdf-8.2.1/src/pikepdf.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (122)     3097 2023-07-23 08:28:49.000000 pikepdf-8.2.1/src/pikepdf.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-23 08:28:49.000000 pikepdf-8.2.1/src/pikepdf.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (122)      688 2023-07-23 08:28:49.000000 pikepdf-8.2.1/src/pikepdf.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (122)        8 2023-07-23 08:28:49.000000 pikepdf-8.2.1/src/pikepdf.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 08:28:49.351531 pikepdf-8.2.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (122)     1731 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 08:28:49.359531 pikepdf-8.2.1/tests/resources/
+-rw-r--r--   0 runner    (1001) docker     (122)     5661 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/1biticc.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)      420 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/Gray.icc
+-rw-r--r--   0 runner    (1001) docker     (122)     1734 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/aquamarine-cie.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     1940 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/aquamarine-cie.png
+-rw-r--r--   0 runner    (1001) docker     (122)     1461 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/cmyk-jpeg.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)    97969 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/congress-gray.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)   193947 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/congress.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     2889 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/content-stream-errors.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)    10876 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/form.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     2713 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/formxobject.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     2916 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/fourpages.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)   296661 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/graph-encrypted.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)   296322 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/graph.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     1544 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/image-mono-inline.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)      965 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/invalid_creationdate.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)    20306 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/jbig2.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)    60332 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/jbig2global.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     6994 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/outlines.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)      931 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/pal-1bit-rgb.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)      931 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/pal-1bit-trivial.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     2918 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/pal.pdf
+-rwxr-xr-x   0 runner    (1001) docker     (122)   533953 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/pdfx.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)    18471 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/pike-flate-jp2.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)    18152 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/pike-jp2.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     2681 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/pink-palette-icc.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     2698 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/pink-palette-icc.png
+-rw-r--r--   0 runner    (1001) docker     (122)     5432 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/rle.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)   115546 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/sandwich.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)    10049 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/veraPDF test suite 6-2-10-t02-pass-a.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     2676 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/resources/veraPDF test suite 6-2-3-3-t01-fail-c.pdf
+-rw-r--r--   0 runner    (1001) docker     (122)     1439 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_annotation.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4721 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_attachments.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1312 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_augments.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4453 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_codec.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1961 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_decimal.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1181 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_dictionary.py
+-rw-r--r--   0 runner    (1001) docker     (122)     5610 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_encrypt.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1690 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_errors.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3404 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_filters.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3135 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_foreign.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1988 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_formxobject.py
+-rw-r--r--   0 runner    (1001) docker     (122)    36948 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_image_access.py
+-rw-r--r--   0 runner    (1001) docker     (122)     9944 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_io.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2498 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_ipython.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2036 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_job.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1523 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_matrix.py
+-rw-r--r--   0 runner    (1001) docker     (122)    25184 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_metadata.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2094 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_nametree.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2301 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_numbertree.py
+-rw-r--r--   0 runner    (1001) docker     (122)    22294 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_object.py
+-rw-r--r--   0 runner    (1001) docker     (122)      565 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_objectlist.py
+-rw-r--r--   0 runner    (1001) docker     (122)    17177 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_outlines.py
+-rw-r--r--   0 runner    (1001) docker     (122)     9131 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_page.py
+-rw-r--r--   0 runner    (1001) docker     (122)    15569 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_pages.py
+-rw-r--r--   0 runner    (1001) docker     (122)     9522 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_parsers.py
+-rw-r--r--   0 runner    (1001) docker     (122)    13773 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_pdf.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3956 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_pdfa.py
+-rw-r--r--   0 runner    (1001) docker     (122)      754 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_private_pdfs.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1393 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_rectangle.py
+-rw-r--r--   0 runner    (1001) docker     (122)     2032 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_refcount.py
+-rw-r--r--   0 runner    (1001) docker     (122)     3744 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_repr.py
+-rw-r--r--   0 runner    (1001) docker     (122)     4682 2023-07-23 08:25:31.000000 pikepdf-8.2.1/tests/test_sanity.py
```

### Comparing `pikepdf-8.2.0/LICENSE.txt` & `pikepdf-8.2.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/PKG-INFO` & `pikepdf-8.2.1/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pikepdf
-Version: 8.2.0
+Version: 8.2.1
 Summary: Read and write PDFs with Python, powered by qpdf
 Author-email: "James R. Barlow" <james@purplerock.ca>
 License: MPL-2.0
 Project-URL: documentation, https://pikepdf.readthedocs.io/
 Project-URL: repository, https://github.com/pikepdf/pikepdf
 Project-URL: changelog, https://pikepdf.readthedocs.io/en/latest/releasenotes/index.html
 Keywords: PDF
@@ -98,10 +98,10 @@
 * [PDF Arranger](https://github.com/jeromerobert/pdfarranger) is a small Python application that provides a graphical user interface to rotate, crop and rearrange PDFs.
 
 * [PDFStitcher](https://github.com/cfcurtis/sewingutils) is a utility for stitching PDF pages into a single document (i.e. N-up or page imposition).
 
 License
 -------
 
-pikepdf is provided under the [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/) license (MPL) that can be found in the LICENSE file. By using, distributing, or contributing to this project, you agree to the terms and conditions of this license. Some components of the project may be under other license agreements, as indicated in their SPDX license header or the [`.dep5/reuse`](REUSE) file.
+pikepdf is licensed under the [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/) license (MPL-2.0) that can be found in the LICENSE file. By using, distributing, or contributing to this project, you agree to the terms and conditions of this license. MPL 2.0 permits you to combine the software with other work, including commercial and closed source software, but asks you to publish source-level modifications you make to pikepdf itself.
 
-[Informally](https://www.mozilla.org/en-US/MPL/2.0/FAQ/), MPL 2.0 is a not "viral" license. It may be combined with other work, including commercial software. However, you must disclose your modifications *to pikepdf* in source code form. In other works, fork this repository on GitHub or elsewhere and commit your contributions there, and you've satisfied your obligations. MPL 2.0 is compatible with the GPL and LGPL - see the [guidelines](https://www.mozilla.org/en-US/MPL/2.0/combining-mpl-and-gpl/) for notes on use in GPL.
+Some components of the project may be under other license agreements, as indicated in their SPDX license header or the [`.dep5/reuse`](REUSE) file.
```

### Comparing `pikepdf-8.2.0/README.md` & `pikepdf-8.2.1/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -70,10 +70,10 @@
 * [PDF Arranger](https://github.com/jeromerobert/pdfarranger) is a small Python application that provides a graphical user interface to rotate, crop and rearrange PDFs.
 
 * [PDFStitcher](https://github.com/cfcurtis/sewingutils) is a utility for stitching PDF pages into a single document (i.e. N-up or page imposition).
 
 License
 -------
 
-pikepdf is provided under the [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/) license (MPL) that can be found in the LICENSE file. By using, distributing, or contributing to this project, you agree to the terms and conditions of this license. Some components of the project may be under other license agreements, as indicated in their SPDX license header or the [`.dep5/reuse`](REUSE) file.
+pikepdf is licensed under the [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/) license (MPL-2.0) that can be found in the LICENSE file. By using, distributing, or contributing to this project, you agree to the terms and conditions of this license. MPL 2.0 permits you to combine the software with other work, including commercial and closed source software, but asks you to publish source-level modifications you make to pikepdf itself.
 
-[Informally](https://www.mozilla.org/en-US/MPL/2.0/FAQ/), MPL 2.0 is a not "viral" license. It may be combined with other work, including commercial software. However, you must disclose your modifications *to pikepdf* in source code form. In other works, fork this repository on GitHub or elsewhere and commit your contributions there, and you've satisfied your obligations. MPL 2.0 is compatible with the GPL and LGPL - see the [guidelines](https://www.mozilla.org/en-US/MPL/2.0/combining-mpl-and-gpl/) for notes on use in GPL.
+Some components of the project may be under other license agreements, as indicated in their SPDX license header or the [`.dep5/reuse`](REUSE) file.
```

### Comparing `pikepdf-8.2.0/pyproject.toml` & `pikepdf-8.2.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
   "wheel >= 0.37",
   "pybind11 >= 2.10.1",
 ]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "pikepdf"
-version = "8.2.0"
+version = "8.2.1"
 description = "Read and write PDFs with Python, powered by qpdf"
 readme = "README.md"
 requires-python = ">= 3.8"
 keywords = ["PDF"]
 authors = [
   { name = "James R. Barlow", email= "james@purplerock.ca"}
 ]
@@ -83,14 +83,16 @@
     "python-dateutil>=2.8.1",
     "python-xmp-toolkit>=2.0.1 ;sys_platform != 'nt' and platform_machine == 'x86_64'",
     "tomli;python_version < '3.11'",
 ]
 
 [tool.setuptools.packages.find]
 where = ["src"]
+include = ["pikepdf", "pikepdf.*"]
+namespaces = false
 
 [tool.setuptools.package-data]
 pikepdf = ["*.dll", "py.typed"]
 
 [tool.black]
 line-length = 88
 target-version = ["py38", "py39", "py310", "py311"]
```

### Comparing `pikepdf-8.2.0/setup.py` & `pikepdf-8.2.1/setup.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/annotation.cpp` & `pikepdf-8.2.1/src/core/annotation.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/embeddedfiles.cpp` & `pikepdf-8.2.1/src/core/embeddedfiles.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/jbig2-inl.h` & `pikepdf-8.2.1/src/core/jbig2-inl.h`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/job.cpp` & `pikepdf-8.2.1/src/core/job.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/logger.cpp` & `pikepdf-8.2.1/src/core/logger.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/mmap_inputsource-inl.h` & `pikepdf-8.2.1/src/core/mmap_inputsource-inl.h`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/nametree.cpp` & `pikepdf-8.2.1/src/core/nametree.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/numbertree.cpp` & `pikepdf-8.2.1/src/core/numbertree.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/object.cpp` & `pikepdf-8.2.1/src/core/object.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/object_convert.cpp` & `pikepdf-8.2.1/src/core/object_convert.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/object_repr.cpp` & `pikepdf-8.2.1/src/core/object_repr.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/page.cpp` & `pikepdf-8.2.1/src/core/page.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/parsers.cpp` & `pikepdf-8.2.1/src/core/parsers.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/parsers.h` & `pikepdf-8.2.1/src/core/parsers.h`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/pikepdf.cpp` & `pikepdf-8.2.1/src/core/pikepdf.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/pikepdf.h` & `pikepdf-8.2.1/src/core/pikepdf.h`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/pipeline.cpp` & `pikepdf-8.2.1/src/core/pipeline.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/pipeline.h` & `pikepdf-8.2.1/src/core/pipeline.h`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/qpdf.cpp` & `pikepdf-8.2.1/src/core/qpdf.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/qpdf_inputsource-inl.h` & `pikepdf-8.2.1/src/core/qpdf_inputsource-inl.h`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/qpdf_pagelist.cpp` & `pikepdf-8.2.1/src/core/qpdf_pagelist.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/qpdf_pagelist.h` & `pikepdf-8.2.1/src/core/qpdf_pagelist.h`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/rectangle.cpp` & `pikepdf-8.2.1/src/core/rectangle.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/tokenfilter.cpp` & `pikepdf-8.2.1/src/core/tokenfilter.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/utils.cpp` & `pikepdf-8.2.1/src/core/utils.cpp`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/core/utils.h` & `pikepdf-8.2.1/src/core/utils.h`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/__init__.py` & `pikepdf-8.2.1/src/pikepdf/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 """A library for manipulating PDFs."""
 
 # isort:skip_file
 
 from __future__ import annotations
 
-__version__ = "8.2.0"
+__version__ = "8.2.1"
 
 try:
     from . import _core
 except ImportError as _e:  # pragma: no cover
     _msg = "pikepdf's extension library failed to import"
     raise ImportError(_msg) from _e
```

### Comparing `pikepdf-8.2.0/src/pikepdf/_augments.py` & `pikepdf-8.2.1/src/pikepdf/_augments.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/_cpphelpers.py` & `pikepdf-8.2.1/src/pikepdf/_cpphelpers.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/_io.py` & `pikepdf-8.2.1/src/pikepdf/_io.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/_methods.py` & `pikepdf-8.2.1/src/pikepdf/_methods.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/_qpdf.py` & `pikepdf-8.2.1/src/pikepdf/_qpdf.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/_xml.py` & `pikepdf-8.2.1/src/pikepdf/_xml.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/codec.py` & `pikepdf-8.2.1/src/pikepdf/codec.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/jbig2.py` & `pikepdf-8.2.1/src/pikepdf/jbig2.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/models/__init__.py` & `pikepdf-8.2.1/src/pikepdf/models/__init__.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/models/_content_stream.py` & `pikepdf-8.2.1/src/pikepdf/models/_content_stream.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/models/_transcoding.py` & `pikepdf-8.2.1/src/pikepdf/models/_transcoding.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/models/encryption.py` & `pikepdf-8.2.1/src/pikepdf/models/encryption.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/models/image.py` & `pikepdf-8.2.1/src/pikepdf/models/image.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/models/matrix.py` & `pikepdf-8.2.1/src/pikepdf/models/matrix.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/models/metadata.py` & `pikepdf-8.2.1/src/pikepdf/models/metadata.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/models/outlines.py` & `pikepdf-8.2.1/src/pikepdf/models/outlines.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf/objects.py` & `pikepdf-8.2.1/src/pikepdf/objects.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf.egg-info/PKG-INFO` & `pikepdf-8.2.1/src/pikepdf.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pikepdf
-Version: 8.2.0
+Version: 8.2.1
 Summary: Read and write PDFs with Python, powered by qpdf
 Author-email: "James R. Barlow" <james@purplerock.ca>
 License: MPL-2.0
 Project-URL: documentation, https://pikepdf.readthedocs.io/
 Project-URL: repository, https://github.com/pikepdf/pikepdf
 Project-URL: changelog, https://pikepdf.readthedocs.io/en/latest/releasenotes/index.html
 Keywords: PDF
@@ -98,10 +98,10 @@
 * [PDF Arranger](https://github.com/jeromerobert/pdfarranger) is a small Python application that provides a graphical user interface to rotate, crop and rearrange PDFs.
 
 * [PDFStitcher](https://github.com/cfcurtis/sewingutils) is a utility for stitching PDF pages into a single document (i.e. N-up or page imposition).
 
 License
 -------
 
-pikepdf is provided under the [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/) license (MPL) that can be found in the LICENSE file. By using, distributing, or contributing to this project, you agree to the terms and conditions of this license. Some components of the project may be under other license agreements, as indicated in their SPDX license header or the [`.dep5/reuse`](REUSE) file.
+pikepdf is licensed under the [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/) license (MPL-2.0) that can be found in the LICENSE file. By using, distributing, or contributing to this project, you agree to the terms and conditions of this license. MPL 2.0 permits you to combine the software with other work, including commercial and closed source software, but asks you to publish source-level modifications you make to pikepdf itself.
 
-[Informally](https://www.mozilla.org/en-US/MPL/2.0/FAQ/), MPL 2.0 is a not "viral" license. It may be combined with other work, including commercial software. However, you must disclose your modifications *to pikepdf* in source code form. In other works, fork this repository on GitHub or elsewhere and commit your contributions there, and you've satisfied your obligations. MPL 2.0 is compatible with the GPL and LGPL - see the [guidelines](https://www.mozilla.org/en-US/MPL/2.0/combining-mpl-and-gpl/) for notes on use in GPL.
+Some components of the project may be under other license agreements, as indicated in their SPDX license header or the [`.dep5/reuse`](REUSE) file.
```

### Comparing `pikepdf-8.2.0/src/pikepdf.egg-info/SOURCES.txt` & `pikepdf-8.2.1/src/pikepdf.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/src/pikepdf.egg-info/requires.txt` & `pikepdf-8.2.1/src/pikepdf.egg-info/requires.txt`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/conftest.py` & `pikepdf-8.2.1/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/1biticc.pdf` & `pikepdf-8.2.1/tests/resources/1biticc.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/aquamarine-cie.pdf` & `pikepdf-8.2.1/tests/resources/aquamarine-cie.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/aquamarine-cie.png` & `pikepdf-8.2.1/tests/resources/aquamarine-cie.png`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/cmyk-jpeg.pdf` & `pikepdf-8.2.1/tests/resources/cmyk-jpeg.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/congress-gray.pdf` & `pikepdf-8.2.1/tests/resources/congress-gray.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/congress.pdf` & `pikepdf-8.2.1/tests/resources/congress.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/content-stream-errors.pdf` & `pikepdf-8.2.1/tests/resources/content-stream-errors.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/form.pdf` & `pikepdf-8.2.1/tests/resources/form.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/formxobject.pdf` & `pikepdf-8.2.1/tests/resources/formxobject.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/fourpages.pdf` & `pikepdf-8.2.1/tests/resources/fourpages.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/graph-encrypted.pdf` & `pikepdf-8.2.1/tests/resources/graph-encrypted.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/graph.pdf` & `pikepdf-8.2.1/tests/resources/graph.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/image-mono-inline.pdf` & `pikepdf-8.2.1/tests/resources/image-mono-inline.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/invalid_creationdate.pdf` & `pikepdf-8.2.1/tests/resources/invalid_creationdate.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/jbig2.pdf` & `pikepdf-8.2.1/tests/resources/jbig2.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/jbig2global.pdf` & `pikepdf-8.2.1/tests/resources/jbig2global.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/outlines.pdf` & `pikepdf-8.2.1/tests/resources/outlines.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/pal-1bit-rgb.pdf` & `pikepdf-8.2.1/tests/resources/pal-1bit-rgb.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/pal-1bit-trivial.pdf` & `pikepdf-8.2.1/tests/resources/pal-1bit-trivial.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/pal.pdf` & `pikepdf-8.2.1/tests/resources/pal.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/pdfx.pdf` & `pikepdf-8.2.1/tests/resources/pdfx.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/pike-flate-jp2.pdf` & `pikepdf-8.2.1/tests/resources/pike-flate-jp2.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/pike-jp2.pdf` & `pikepdf-8.2.1/tests/resources/pike-jp2.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/pink-palette-icc.pdf` & `pikepdf-8.2.1/tests/resources/pink-palette-icc.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/pink-palette-icc.png` & `pikepdf-8.2.1/tests/resources/pink-palette-icc.png`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/rle.pdf` & `pikepdf-8.2.1/tests/resources/rle.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/sandwich.pdf` & `pikepdf-8.2.1/tests/resources/sandwich.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/veraPDF test suite 6-2-10-t02-pass-a.pdf` & `pikepdf-8.2.1/tests/resources/veraPDF test suite 6-2-10-t02-pass-a.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/resources/veraPDF test suite 6-2-3-3-t01-fail-c.pdf` & `pikepdf-8.2.1/tests/resources/veraPDF test suite 6-2-3-3-t01-fail-c.pdf`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_annotation.py` & `pikepdf-8.2.1/tests/test_annotation.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_attachments.py` & `pikepdf-8.2.1/tests/test_attachments.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_augments.py` & `pikepdf-8.2.1/tests/test_augments.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_codec.py` & `pikepdf-8.2.1/tests/test_codec.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_decimal.py` & `pikepdf-8.2.1/tests/test_decimal.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_dictionary.py` & `pikepdf-8.2.1/tests/test_dictionary.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_encrypt.py` & `pikepdf-8.2.1/tests/test_encrypt.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_errors.py` & `pikepdf-8.2.1/tests/test_errors.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_filters.py` & `pikepdf-8.2.1/tests/test_filters.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_foreign.py` & `pikepdf-8.2.1/tests/test_foreign.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_formxobject.py` & `pikepdf-8.2.1/tests/test_formxobject.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_image_access.py` & `pikepdf-8.2.1/tests/test_image_access.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_io.py` & `pikepdf-8.2.1/tests/test_io.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_ipython.py` & `pikepdf-8.2.1/tests/test_ipython.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_job.py` & `pikepdf-8.2.1/tests/test_job.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_matrix.py` & `pikepdf-8.2.1/tests/test_matrix.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_metadata.py` & `pikepdf-8.2.1/tests/test_metadata.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_nametree.py` & `pikepdf-8.2.1/tests/test_nametree.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_numbertree.py` & `pikepdf-8.2.1/tests/test_numbertree.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_object.py` & `pikepdf-8.2.1/tests/test_object.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_objectlist.py` & `pikepdf-8.2.1/tests/test_objectlist.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_outlines.py` & `pikepdf-8.2.1/tests/test_outlines.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_page.py` & `pikepdf-8.2.1/tests/test_page.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_pages.py` & `pikepdf-8.2.1/tests/test_pages.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_parsers.py` & `pikepdf-8.2.1/tests/test_parsers.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_pdf.py` & `pikepdf-8.2.1/tests/test_pdf.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_pdfa.py` & `pikepdf-8.2.1/tests/test_pdfa.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_private_pdfs.py` & `pikepdf-8.2.1/tests/test_private_pdfs.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_rectangle.py` & `pikepdf-8.2.1/tests/test_rectangle.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_refcount.py` & `pikepdf-8.2.1/tests/test_refcount.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_repr.py` & `pikepdf-8.2.1/tests/test_repr.py`

 * *Files identical despite different names*

### Comparing `pikepdf-8.2.0/tests/test_sanity.py` & `pikepdf-8.2.1/tests/test_sanity.py`

 * *Files identical despite different names*

