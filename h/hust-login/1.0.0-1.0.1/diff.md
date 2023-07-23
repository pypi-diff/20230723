# Comparing `tmp/hust-login-1.0.0.tar.gz` & `tmp/hust_login-1.0.1-py3.11.egg`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hust-login-1.0.0.tar", last modified: Wed Jul 19 06:00:35 2023, max compression
+Zip archive data, at least v2.0 to extract, compression method=deflate
```

## filetype from diffoscope

```diff
@@ -1 +1 @@
-GzipFile
+ZipFile
```

