# Comparing `tmp/zzq_string_sum-0.3.0.tar.gz` & `tmp/zzq_string_sum-0.4.0-cp312-cp312-manylinux_2_12_i686.manylinux2010_i686.whl.zip`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data
+Zip archive data, at least v2.0 to extract, compression method=deflate
```

## filetype from diffoscope

```diff
@@ -1 +1 @@
-GzipFile
+ZipFile
```

