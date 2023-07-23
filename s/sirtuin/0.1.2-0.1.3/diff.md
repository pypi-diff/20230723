# Comparing `tmp/sirtuin-0.1.2.tar.gz` & `tmp/sirtuin-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sirtuin-0.1.2.tar", max compression
+gzip compressed data, was "sirtuin-0.1.3.tar", max compression
```

## Comparing `sirtuin-0.1.2.tar` & `sirtuin-0.1.3.tar`

### file list

```diff
@@ -1,48 +1,48 @@
--rw-r--r--   0        0        0    10935 2023-01-24 13:34:07.454164 sirtuin-0.1.2/LICENSE
--rw-r--r--   0        0        0     7978 2023-04-11 17:07:47.857740 sirtuin-0.1.2/README.md
--rw-r--r--   0        0        0     1842 2023-07-23 02:54:17.152000 sirtuin-0.1.2/pyproject.toml
--rw-r--r--   0        0        0     9913 2023-01-13 13:59:59.790805 sirtuin-0.1.2/src/sirtuin/controllers/aws_beanstalk.py
--rw-r--r--   0        0        0     2536 2023-07-23 02:52:47.950894 sirtuin-0.1.2/src/sirtuin/controllers/aws_cloudfront.py
--rw-r--r--   0        0        0      633 2023-01-19 17:02:02.885001 sirtuin-0.1.2/src/sirtuin/controllers/aws_compute.py
--rw-r--r--   0        0        0     2575 2023-01-18 10:56:25.465966 sirtuin-0.1.2/src/sirtuin/controllers/aws_container.py
--rw-r--r--   0        0        0     1602 2023-01-12 18:14:28.104849 sirtuin-0.1.2/src/sirtuin/controllers/http_headers.py
--rw-r--r--   0        0        0     4245 2023-01-19 17:02:27.531745 sirtuin-0.1.2/src/sirtuin/main.py
--rw-r--r--   0        0        0     5155 2023-01-13 13:50:57.025042 sirtuin-0.1.2/src/sirtuin/models/aws_beanstalk.py
--rw-r--r--   0        0        0      620 2022-12-26 10:02:47.084568 sirtuin-0.1.2/src/sirtuin/models/aws_cloudfront.py
--rw-r--r--   0        0        0      139 2022-12-26 10:02:47.084642 sirtuin-0.1.2/src/sirtuin/models/aws_compute.py
--rw-r--r--   0        0        0      734 2023-01-18 10:29:46.377776 sirtuin-0.1.2/src/sirtuin/models/aws_container.py
--rw-r--r--   0        0        0      134 2022-12-26 10:02:47.084723 sirtuin-0.1.2/src/sirtuin/models/aws_instances.py
--rw-r--r--   0        0        0      282 2022-12-26 10:02:47.084804 sirtuin-0.1.2/src/sirtuin/models/aws_regions.py
--rw-r--r--   0        0        0      826 2022-12-26 10:02:47.084882 sirtuin-0.1.2/src/sirtuin/models/base_models.py
--rw-r--r--   0        0        0      891 2022-12-26 10:02:47.084977 sirtuin-0.1.2/src/sirtuin/models/http_headers.py
--rw-r--r--   0        0        0      149 2022-12-26 10:02:47.085154 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/autoscaling-policy.config
--rw-r--r--   0        0        0      288 2022-12-26 10:02:47.085235 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/autoscaling.config
--rw-r--r--   0        0        0       77 2022-12-26 10:02:47.085311 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/disable-alb-listener.config
--rw-r--r--   0        0        0       65 2022-12-26 10:02:47.085383 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/disable-clb-listener.config
--rw-r--r--   0        0        0       77 2022-12-26 10:02:47.085455 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/disable-nlb-listener.config
--rw-r--r--   0        0        0      483 2022-12-26 10:02:47.085550 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/health-alb-listener.config
--rw-r--r--   0        0        0      605 2022-12-26 10:02:47.085662 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/health-clb-listener.config
--rw-r--r--   0        0        0       86 2022-12-26 10:02:47.085750 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/httpd-proxy.config
--rw-r--r--   0        0        0       79 2022-12-26 10:02:47.085819 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/load-balancer.config
--rw-r--r--   0        0        0      165 2022-12-26 10:02:47.085909 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/modify-clb-listener.config
--rw-r--r--   0        0        0      207 2022-12-26 10:02:47.085992 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/platform-update.config
--rw-r--r--   0        0        0      446 2022-12-26 10:02:47.086076 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/redirect-alb-listener.config
--rw-r--r--   0        0        0      153 2022-12-26 10:02:47.086143 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/secure-alb-listener.config
--rw-r--r--   0        0        0      198 2022-12-26 10:02:47.086235 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/secure-clb-listener.config
--rw-r--r--   0        0        0       72 2022-12-26 10:02:47.086314 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/secure-nlb-listener.config
--rw-r--r--   0        0        0      131 2022-12-26 10:02:47.086386 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/security.config
--rw-r--r--   0        0        0       89 2022-12-26 10:02:47.086456 sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/timezone.config
--rw-r--r--   0        0        0      336 2022-12-26 10:02:47.086661 sirtuin-0.1.2/src/sirtuin/schemas/platform/hooks/prebuild/set_timezone.sh
--rw-r--r--   0        0        0       83 2022-12-26 10:02:47.086828 sirtuin-0.1.2/src/sirtuin/schemas/platform/httpd/conf.d/proxy.conf
--rw-r--r--   0        0        0      113 2022-12-26 10:02:47.086905 sirtuin-0.1.2/src/sirtuin/schemas/platform/httpd/conf.d/tunnel.conf
--rw-r--r--   0        0        0      158 2022-12-26 10:02:47.086970 sirtuin-0.1.2/src/sirtuin/schemas/platform/httpd/conf.d/wsgi.conf
--rw-r--r--   0        0        0       35 2022-12-26 10:02:47.087107 sirtuin-0.1.2/src/sirtuin/schemas/platform/nginx/conf.d/sizes.conf
--rw-r--r--   0        0        0      164 2022-12-26 10:02:47.087177 sirtuin-0.1.2/src/sirtuin/schemas/platform/nginx/conf.d/timeouts.conf
--rw-r--r--   0        0        0      456 2022-12-26 10:02:47.087334 sirtuin-0.1.2/src/sirtuin/schemas/platform/nginx/sites-enabled/streamlit.conf
--rw-r--r--   0        0        0      244 2022-12-26 10:02:47.087444 sirtuin-0.1.2/src/sirtuin/utils/cleaners.py
--rw-r--r--   0        0        0      132 2023-01-13 13:41:23.663530 sirtuin-0.1.2/src/sirtuin/utils/constants.py
--rw-r--r--   0        0        0     2467 2023-01-18 10:57:38.528732 sirtuin-0.1.2/src/sirtuin/utils/decorators.py
--rw-r--r--   0        0        0     1363 2022-12-26 10:02:47.087604 sirtuin-0.1.2/src/sirtuin/utils/dumpers.py
--rw-r--r--   0        0        0      406 2023-01-12 15:59:36.870468 sirtuin-0.1.2/src/sirtuin/utils/filepaths.py
--rw-r--r--   0        0        0     1309 2022-12-26 10:02:47.087768 sirtuin-0.1.2/src/sirtuin/utils/loaders.py
--rw-r--r--   0        0        0     8491 1970-01-01 00:00:00.000000 sirtuin-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0    10935 2023-01-24 13:34:07.454164 sirtuin-0.1.3/LICENSE
+-rw-r--r--   0        0        0     7978 2023-04-11 17:07:47.857740 sirtuin-0.1.3/README.md
+-rw-r--r--   0        0        0     1842 2023-07-23 03:10:50.616437 sirtuin-0.1.3/pyproject.toml
+-rw-r--r--   0        0        0     9913 2023-01-13 13:59:59.790805 sirtuin-0.1.3/src/sirtuin/controllers/aws_beanstalk.py
+-rw-r--r--   0        0        0     2537 2023-07-23 03:10:32.439252 sirtuin-0.1.3/src/sirtuin/controllers/aws_cloudfront.py
+-rw-r--r--   0        0        0      633 2023-01-19 17:02:02.885001 sirtuin-0.1.3/src/sirtuin/controllers/aws_compute.py
+-rw-r--r--   0        0        0     2575 2023-01-18 10:56:25.465966 sirtuin-0.1.3/src/sirtuin/controllers/aws_container.py
+-rw-r--r--   0        0        0     1602 2023-01-12 18:14:28.104849 sirtuin-0.1.3/src/sirtuin/controllers/http_headers.py
+-rw-r--r--   0        0        0     4245 2023-01-19 17:02:27.531745 sirtuin-0.1.3/src/sirtuin/main.py
+-rw-r--r--   0        0        0     5155 2023-01-13 13:50:57.025042 sirtuin-0.1.3/src/sirtuin/models/aws_beanstalk.py
+-rw-r--r--   0        0        0      620 2022-12-26 10:02:47.084568 sirtuin-0.1.3/src/sirtuin/models/aws_cloudfront.py
+-rw-r--r--   0        0        0      139 2022-12-26 10:02:47.084642 sirtuin-0.1.3/src/sirtuin/models/aws_compute.py
+-rw-r--r--   0        0        0      734 2023-01-18 10:29:46.377776 sirtuin-0.1.3/src/sirtuin/models/aws_container.py
+-rw-r--r--   0        0        0      134 2022-12-26 10:02:47.084723 sirtuin-0.1.3/src/sirtuin/models/aws_instances.py
+-rw-r--r--   0        0        0      282 2022-12-26 10:02:47.084804 sirtuin-0.1.3/src/sirtuin/models/aws_regions.py
+-rw-r--r--   0        0        0      826 2022-12-26 10:02:47.084882 sirtuin-0.1.3/src/sirtuin/models/base_models.py
+-rw-r--r--   0        0        0      891 2022-12-26 10:02:47.084977 sirtuin-0.1.3/src/sirtuin/models/http_headers.py
+-rw-r--r--   0        0        0      149 2022-12-26 10:02:47.085154 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/autoscaling-policy.config
+-rw-r--r--   0        0        0      288 2022-12-26 10:02:47.085235 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/autoscaling.config
+-rw-r--r--   0        0        0       77 2022-12-26 10:02:47.085311 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/disable-alb-listener.config
+-rw-r--r--   0        0        0       65 2022-12-26 10:02:47.085383 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/disable-clb-listener.config
+-rw-r--r--   0        0        0       77 2022-12-26 10:02:47.085455 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/disable-nlb-listener.config
+-rw-r--r--   0        0        0      483 2022-12-26 10:02:47.085550 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/health-alb-listener.config
+-rw-r--r--   0        0        0      605 2022-12-26 10:02:47.085662 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/health-clb-listener.config
+-rw-r--r--   0        0        0       86 2022-12-26 10:02:47.085750 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/httpd-proxy.config
+-rw-r--r--   0        0        0       79 2022-12-26 10:02:47.085819 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/load-balancer.config
+-rw-r--r--   0        0        0      165 2022-12-26 10:02:47.085909 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/modify-clb-listener.config
+-rw-r--r--   0        0        0      207 2022-12-26 10:02:47.085992 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/platform-update.config
+-rw-r--r--   0        0        0      446 2022-12-26 10:02:47.086076 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/redirect-alb-listener.config
+-rw-r--r--   0        0        0      153 2022-12-26 10:02:47.086143 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/secure-alb-listener.config
+-rw-r--r--   0        0        0      198 2022-12-26 10:02:47.086235 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/secure-clb-listener.config
+-rw-r--r--   0        0        0       72 2022-12-26 10:02:47.086314 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/secure-nlb-listener.config
+-rw-r--r--   0        0        0      131 2022-12-26 10:02:47.086386 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/security.config
+-rw-r--r--   0        0        0       89 2022-12-26 10:02:47.086456 sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/timezone.config
+-rw-r--r--   0        0        0      336 2022-12-26 10:02:47.086661 sirtuin-0.1.3/src/sirtuin/schemas/platform/hooks/prebuild/set_timezone.sh
+-rw-r--r--   0        0        0       83 2022-12-26 10:02:47.086828 sirtuin-0.1.3/src/sirtuin/schemas/platform/httpd/conf.d/proxy.conf
+-rw-r--r--   0        0        0      113 2022-12-26 10:02:47.086905 sirtuin-0.1.3/src/sirtuin/schemas/platform/httpd/conf.d/tunnel.conf
+-rw-r--r--   0        0        0      158 2022-12-26 10:02:47.086970 sirtuin-0.1.3/src/sirtuin/schemas/platform/httpd/conf.d/wsgi.conf
+-rw-r--r--   0        0        0       35 2022-12-26 10:02:47.087107 sirtuin-0.1.3/src/sirtuin/schemas/platform/nginx/conf.d/sizes.conf
+-rw-r--r--   0        0        0      164 2022-12-26 10:02:47.087177 sirtuin-0.1.3/src/sirtuin/schemas/platform/nginx/conf.d/timeouts.conf
+-rw-r--r--   0        0        0      456 2022-12-26 10:02:47.087334 sirtuin-0.1.3/src/sirtuin/schemas/platform/nginx/sites-enabled/streamlit.conf
+-rw-r--r--   0        0        0      244 2022-12-26 10:02:47.087444 sirtuin-0.1.3/src/sirtuin/utils/cleaners.py
+-rw-r--r--   0        0        0      132 2023-01-13 13:41:23.663530 sirtuin-0.1.3/src/sirtuin/utils/constants.py
+-rw-r--r--   0        0        0     2467 2023-01-18 10:57:38.528732 sirtuin-0.1.3/src/sirtuin/utils/decorators.py
+-rw-r--r--   0        0        0     1363 2022-12-26 10:02:47.087604 sirtuin-0.1.3/src/sirtuin/utils/dumpers.py
+-rw-r--r--   0        0        0      406 2023-01-12 15:59:36.870468 sirtuin-0.1.3/src/sirtuin/utils/filepaths.py
+-rw-r--r--   0        0        0     1309 2022-12-26 10:02:47.087768 sirtuin-0.1.3/src/sirtuin/utils/loaders.py
+-rw-r--r--   0        0        0     8491 1970-01-01 00:00:00.000000 sirtuin-0.1.3/PKG-INFO
```

### Comparing `sirtuin-0.1.2/LICENSE` & `sirtuin-0.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/README.md` & `sirtuin-0.1.3/README.md`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/pyproject.toml` & `sirtuin-0.1.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -43,15 +43,15 @@
 warn_unused_ignores = true
 
 [tool.poetry]
 authors = ["Meryll Dindin <merylldin@gmail.com>"]
 description = "AWS routines for Python projects"
 name = "sirtuin"
 readme = "README.md"
-version = "0.1.2"
+version = "0.1.3"
 
 [tool.poetry.dependencies]
 pydantic = ">=1.10"
 python = ">=3.10,<3.12"
 pyyaml = "^6.0"
 tomli = "^2.0"
 typer = {extras = ["all"], version = "^0.9"}
```

### Comparing `sirtuin-0.1.2/src/sirtuin/controllers/aws_beanstalk.py` & `sirtuin-0.1.3/src/sirtuin/controllers/aws_beanstalk.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/controllers/aws_cloudfront.py` & `sirtuin-0.1.3/src/sirtuin/controllers/aws_cloudfront.py`

 * *Files 4% similar despite different names*

```diff
@@ -37,15 +37,15 @@
         f"--cache-control 'max-age=0,public,must-revalidate' "
         f"--delete "
         f"--region {config.bucket.region.value} "
         + (f"--profile {config.profile}" if config.profile is not None else "")
     )
 
 
-@run_command(description="Invalid CloudFront cache")
+@run_command(description="Revoke cloudfront caching")
 def _invalidate_cloudfront_distribution(
     config: CloudfrontSirtuinConfig, verbose: bool = False
 ) -> str:
     return (
         f"aws "
         f"cloudfront create-invalidation "
         f"--distribution-id {config.cloudfront.distribution} "
```

### Comparing `sirtuin-0.1.2/src/sirtuin/controllers/aws_compute.py` & `sirtuin-0.1.3/src/sirtuin/controllers/aws_compute.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/controllers/aws_container.py` & `sirtuin-0.1.3/src/sirtuin/controllers/aws_container.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/controllers/http_headers.py` & `sirtuin-0.1.3/src/sirtuin/controllers/http_headers.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/main.py` & `sirtuin-0.1.3/src/sirtuin/main.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/models/aws_beanstalk.py` & `sirtuin-0.1.3/src/sirtuin/models/aws_beanstalk.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/models/aws_cloudfront.py` & `sirtuin-0.1.3/src/sirtuin/models/aws_cloudfront.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/models/aws_container.py` & `sirtuin-0.1.3/src/sirtuin/models/aws_container.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/models/base_models.py` & `sirtuin-0.1.3/src/sirtuin/models/base_models.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/models/http_headers.py` & `sirtuin-0.1.3/src/sirtuin/models/http_headers.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/schemas/ebextensions/health-clb-listener.config` & `sirtuin-0.1.3/src/sirtuin/schemas/ebextensions/health-clb-listener.config`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/utils/decorators.py` & `sirtuin-0.1.3/src/sirtuin/utils/decorators.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/utils/dumpers.py` & `sirtuin-0.1.3/src/sirtuin/utils/dumpers.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/src/sirtuin/utils/loaders.py` & `sirtuin-0.1.3/src/sirtuin/utils/loaders.py`

 * *Files identical despite different names*

### Comparing `sirtuin-0.1.2/PKG-INFO` & `sirtuin-0.1.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sirtuin
-Version: 0.1.2
+Version: 0.1.3
 Summary: AWS routines for Python projects
 Author: Meryll Dindin
 Author-email: merylldin@gmail.com
 Requires-Python: >=3.10,<3.12
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
```

