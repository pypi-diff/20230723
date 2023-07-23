# Comparing `tmp/ai_automation-3.1.tar.gz` & `tmp/ai_automation-3.2-py3.9.egg`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ai_automation-3.1.tar", last modified: Sun Dec 11 13:17:36 2022, max compression
+Zip archive data, at least v2.0 to extract, compression method=deflate
```

## filetype from diffoscope

```diff
@@ -1 +1 @@
-GzipFile
+ZipFile
```

