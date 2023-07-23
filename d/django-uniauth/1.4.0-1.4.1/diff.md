# Comparing `tmp/django-uniauth-1.4.0.tar.gz` & `tmp/django-uniauth-1.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/django-uniauth-1.4.0.tar", last modified: Sat Nov 12 22:37:06 2022, max compression
+gzip compressed data, was "dist/django-uniauth-1.4.1.tar", last modified: Sun Jul 23 03:21:01 2023, max compression
```

## Comparing `django-uniauth-1.4.0.tar` & `django-uniauth-1.4.1.tar`

### file list

```diff
@@ -1,94 +1,94 @@
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/
--rw-r--r--   0 lanceg     (501) staff       (20)    29177 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/PKG-INFO
--rw-r--r--   0 lanceg     (501) staff       (20)     7560 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/LICENSE.md
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/migrations/
--rw-r--r--   0 lanceg     (501) staff       (20)      602 2022-11-08 01:43:42.000000 django-uniauth-1.4.0/uniauth/migrations/0002_auto_20190707_2305.py
--rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/migrations/__init__.py
--rw-r--r--   0 lanceg     (501) staff       (20)      372 2022-11-08 01:43:41.000000 django-uniauth-1.4.0/uniauth/migrations/0003_auto_20221107_2353.py
--rw-r--r--   0 lanceg     (501) staff       (20)     3559 2022-11-08 01:43:42.000000 django-uniauth-1.4.0/uniauth/migrations/0001_initial.py
--rw-r--r--   0 lanceg     (501) staff       (20)     5806 2022-11-08 01:49:05.000000 django-uniauth-1.4.0/uniauth/merge.py
--rw-r--r--   0 lanceg     (501) staff       (20)     6215 2022-11-08 01:49:05.000000 django-uniauth-1.4.0/uniauth/models.py
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/management/
--rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/management/__init__.py
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/management/commands/
--rw-r--r--   0 lanceg     (501) staff       (20)     1165 2022-11-08 01:43:42.000000 django-uniauth-1.4.0/uniauth/management/commands/remove_institution.py
--rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/management/commands/__init__.py
--rw-r--r--   0 lanceg     (501) staff       (20)     2068 2022-11-08 01:49:05.000000 django-uniauth-1.4.0/uniauth/management/commands/add_institution.py
--rw-r--r--   0 lanceg     (501) staff       (20)     1051 2022-11-08 01:43:42.000000 django-uniauth-1.4.0/uniauth/management/commands/flush_tmp_users.py
--rw-r--r--   0 lanceg     (501) staff       (20)     2126 2022-11-08 01:43:42.000000 django-uniauth-1.4.0/uniauth/management/commands/migrate_cas.py
--rw-r--r--   0 lanceg     (501) staff       (20)     2323 2022-11-08 01:49:05.000000 django-uniauth-1.4.0/uniauth/management/commands/migrate_custom.py
--rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/__init__.py
--rw-r--r--   0 lanceg     (501) staff       (20)     1200 2022-11-12 22:15:08.000000 django-uniauth-1.4.0/uniauth/tokens.py
--rw-r--r--   0 lanceg     (501) staff       (20)      143 2022-11-08 01:43:41.000000 django-uniauth-1.4.0/uniauth/apps.py
--rw-r--r--   0 lanceg     (501) staff       (20)    10246 2022-11-08 01:49:05.000000 django-uniauth-1.4.0/uniauth/forms.py
--rw-r--r--   0 lanceg     (501) staff       (20)     4651 2022-11-08 01:49:05.000000 django-uniauth-1.4.0/uniauth/backends.py
--rw-r--r--   0 lanceg     (501) staff       (20)      229 2022-11-08 01:43:42.000000 django-uniauth-1.4.0/uniauth/admin.py
--rw-r--r--   0 lanceg     (501) staff       (20)     6857 2022-11-08 01:49:05.000000 django-uniauth-1.4.0/uniauth/utils.py
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/urls/
--rw-r--r--   0 lanceg     (501) staff       (20)      872 2022-11-08 01:49:04.000000 django-uniauth-1.4.0/uniauth/urls/cas_only.py
--rw-r--r--   0 lanceg     (501) staff       (20)       51 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/urls/__init__.py
--rw-r--r--   0 lanceg     (501) staff       (20)     1590 2022-11-08 01:49:05.000000 django-uniauth-1.4.0/uniauth/urls/all.py
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/static/
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/static/uniauth/
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/static/uniauth/css/
--rwxr-xr-x   0 lanceg     (501) staff       (20)   140421 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/css/bootstrap.min.css
--rwxr-xr-x   0 lanceg     (501) staff       (20)   197784 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/css/theme.css
--rwxr-xr-x   0 lanceg     (501) staff       (20)     5371 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/css/style.css
--rwxr-xr-x   0 lanceg     (501) staff       (20)    31000 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/css/font-awesome.min.css
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/static/uniauth/js/
--rwxr-xr-x   0 lanceg     (501) staff       (20)    50676 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/js/bootstrap.min.js
--rwxr-xr-x   0 lanceg     (501) staff       (20)    86709 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/js/jquery-3.1.1.min.js
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/static/uniauth/img/
--rwxr-xr-x   0 lanceg     (501) staff       (20)    15406 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/img/favicon.ico
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/static/uniauth/fonts/
--rwxr-xr-x   0 lanceg     (501) staff       (20)    23424 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/fonts/glyphicons-halflings-regular.woff
--rwxr-xr-x   0 lanceg     (501) staff       (20)    18028 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/fonts/glyphicons-halflings-regular.woff2
--rwxr-xr-x   0 lanceg     (501) staff       (20)    77160 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/fonts/fontawesome-webfont.woff2
--rwxr-xr-x   0 lanceg     (501) staff       (20)    98024 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/static/uniauth/fonts/fontawesome-webfont.woff
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/templates/
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/
--rw-r--r--   0 lanceg     (501) staff       (20)     4544 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/password-reset-verify.html
--rw-r--r--   0 lanceg     (501) staff       (20)     1321 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/verification-waiting.html
--rw-r--r--   0 lanceg     (501) staff       (20)     1577 2020-09-06 01:29:49.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/base.html
--rw-r--r--   0 lanceg     (501) staff       (20)     5336 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/login.html
--rw-r--r--   0 lanceg     (501) staff       (20)     2636 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/password-reset.html
--rw-r--r--   0 lanceg     (501) staff       (20)     1277 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/password-reset-verify-done.html
--rw-r--r--   0 lanceg     (501) staff       (20)     1108 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/verification-failure.html
--rw-r--r--   0 lanceg     (501) staff       (20)     1271 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/link-success.html
--rw-r--r--   0 lanceg     (501) staff       (20)     1248 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/password-reset-done.html
--rw-r--r--   0 lanceg     (501) staff       (20)     1819 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/verification-success.html
--rw-r--r--   0 lanceg     (501) staff       (20)     3701 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/link-to-profile.html
--rw-r--r--   0 lanceg     (501) staff       (20)      208 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/verification-email.html
--rw-r--r--   0 lanceg     (501) staff       (20)      438 2020-09-06 01:30:38.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/base-site.html
--rw-r--r--   0 lanceg     (501) staff       (20)    13663 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/settings.html
--rw-r--r--   0 lanceg     (501) staff       (20)      284 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/password-reset-email.html
--rw-r--r--   0 lanceg     (501) staff       (20)     1022 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/logout.html
--rw-r--r--   0 lanceg     (501) staff       (20)     4549 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/uniauth/templates/uniauth/signup.html
--rw-r--r--   0 lanceg     (501) staff       (20)    30806 2022-11-08 01:49:05.000000 django-uniauth-1.4.0/uniauth/views.py
--rw-r--r--   0 lanceg     (501) staff       (20)      757 2022-11-08 01:43:42.000000 django-uniauth-1.4.0/uniauth/decorators.py
--rw-r--r--   0 lanceg     (501) staff       (20)       79 2022-11-08 01:48:57.000000 django-uniauth-1.4.0/pyproject.toml
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/tests/
--rw-r--r--   0 lanceg     (501) staff       (20)    15169 2022-11-12 22:15:16.000000 django-uniauth-1.4.0/tests/test_utils.py
--rw-r--r--   0 lanceg     (501) staff       (20)       48 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/tests/models.py
--rw-r--r--   0 lanceg     (501) staff       (20)     1123 2022-11-12 22:15:15.000000 django-uniauth-1.4.0/tests/test_simple.py
--rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/tests/__init__.py
--rw-r--r--   0 lanceg     (501) staff       (20)     7543 2022-11-12 22:15:16.000000 django-uniauth-1.4.0/tests/test_merge.py
--rw-r--r--   0 lanceg     (501) staff       (20)      873 2022-11-12 22:15:15.000000 django-uniauth-1.4.0/tests/utils.py
--rw-r--r--   0 lanceg     (501) staff       (20)    12295 2022-11-12 22:15:16.000000 django-uniauth-1.4.0/tests/test_commands.py
--rw-r--r--   0 lanceg     (501) staff       (20)     2602 2022-11-12 22:15:16.000000 django-uniauth-1.4.0/tests/settings.py
--rw-r--r--   0 lanceg     (501) staff       (20)    11183 2022-11-12 22:15:16.000000 django-uniauth-1.4.0/tests/test_models.py
--rw-r--r--   0 lanceg     (501) staff       (20)    16368 2022-11-12 22:15:16.000000 django-uniauth-1.4.0/tests/test_backends.py
--rw-r--r--   0 lanceg     (501) staff       (20)     9648 2022-11-12 22:15:16.000000 django-uniauth-1.4.0/tests/test_view_utils.py
--rw-r--r--   0 lanceg     (501) staff       (20)      277 2022-11-12 22:15:15.000000 django-uniauth-1.4.0/tests/urls.py
--rw-r--r--   0 lanceg     (501) staff       (20)     3494 2022-11-12 22:21:54.000000 django-uniauth-1.4.0/tests/test_tokens.py
--rw-r--r--   0 lanceg     (501) staff       (20)      220 2020-06-07 00:49:12.000000 django-uniauth-1.4.0/MANIFEST.in
--rw-r--r--   0 lanceg     (501) staff       (20)    25263 2022-11-12 22:21:01.000000 django-uniauth-1.4.0/README.md
--rw-r--r--   0 lanceg     (501) staff       (20)     2049 2022-11-12 22:15:08.000000 django-uniauth-1.4.0/setup.py
--rw-r--r--   0 lanceg     (501) staff       (20)       38 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/setup.cfg
-drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/django_uniauth.egg-info/
--rw-r--r--   0 lanceg     (501) staff       (20)    29177 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/django_uniauth.egg-info/PKG-INFO
--rw-r--r--   0 lanceg     (501) staff       (20)     2549 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/django_uniauth.egg-info/SOURCES.txt
--rw-r--r--   0 lanceg     (501) staff       (20)       99 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/django_uniauth.egg-info/requires.txt
--rw-r--r--   0 lanceg     (501) staff       (20)       14 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/django_uniauth.egg-info/top_level.txt
--rw-r--r--   0 lanceg     (501) staff       (20)        1 2022-11-12 22:37:06.000000 django-uniauth-1.4.0/django_uniauth.egg-info/dependency_links.txt
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/
+-rw-r--r--   0 lanceg     (501) staff       (20)    28707 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/PKG-INFO
+-rw-r--r--   0 lanceg     (501) staff       (20)     7560 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/LICENSE.md
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/migrations/
+-rw-r--r--   0 lanceg     (501) staff       (20)      602 2022-11-08 01:43:42.000000 django-uniauth-1.4.1/uniauth/migrations/0002_auto_20190707_2305.py
+-rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/migrations/__init__.py
+-rw-r--r--   0 lanceg     (501) staff       (20)      372 2022-11-08 01:43:41.000000 django-uniauth-1.4.1/uniauth/migrations/0003_auto_20221107_2353.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     3559 2022-11-08 01:43:42.000000 django-uniauth-1.4.1/uniauth/migrations/0001_initial.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     5806 2022-11-08 01:49:05.000000 django-uniauth-1.4.1/uniauth/merge.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     6215 2022-11-08 01:49:05.000000 django-uniauth-1.4.1/uniauth/models.py
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/management/
+-rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/management/__init__.py
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/management/commands/
+-rw-r--r--   0 lanceg     (501) staff       (20)     1165 2022-11-08 01:43:42.000000 django-uniauth-1.4.1/uniauth/management/commands/remove_institution.py
+-rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/management/commands/__init__.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     2068 2022-11-08 01:49:05.000000 django-uniauth-1.4.1/uniauth/management/commands/add_institution.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     1051 2022-11-08 01:43:42.000000 django-uniauth-1.4.1/uniauth/management/commands/flush_tmp_users.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     2126 2022-11-08 01:43:42.000000 django-uniauth-1.4.1/uniauth/management/commands/migrate_cas.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     2323 2022-11-08 01:49:05.000000 django-uniauth-1.4.1/uniauth/management/commands/migrate_custom.py
+-rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/__init__.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     1200 2022-11-12 22:15:08.000000 django-uniauth-1.4.1/uniauth/tokens.py
+-rw-r--r--   0 lanceg     (501) staff       (20)      143 2022-11-08 01:43:41.000000 django-uniauth-1.4.1/uniauth/apps.py
+-rw-r--r--   0 lanceg     (501) staff       (20)    10246 2022-11-08 01:49:05.000000 django-uniauth-1.4.1/uniauth/forms.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     4651 2022-11-08 01:49:05.000000 django-uniauth-1.4.1/uniauth/backends.py
+-rw-r--r--   0 lanceg     (501) staff       (20)      229 2022-11-08 01:43:42.000000 django-uniauth-1.4.1/uniauth/admin.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     6857 2022-11-08 01:49:05.000000 django-uniauth-1.4.1/uniauth/utils.py
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/urls/
+-rw-r--r--   0 lanceg     (501) staff       (20)      872 2022-11-08 01:49:04.000000 django-uniauth-1.4.1/uniauth/urls/cas_only.py
+-rw-r--r--   0 lanceg     (501) staff       (20)       51 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/urls/__init__.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     1590 2022-11-08 01:49:05.000000 django-uniauth-1.4.1/uniauth/urls/all.py
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/static/
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/static/uniauth/
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/static/uniauth/css/
+-rwxr-xr-x   0 lanceg     (501) staff       (20)   140421 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/css/bootstrap.min.css
+-rwxr-xr-x   0 lanceg     (501) staff       (20)   197784 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/css/theme.css
+-rwxr-xr-x   0 lanceg     (501) staff       (20)     5371 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/css/style.css
+-rwxr-xr-x   0 lanceg     (501) staff       (20)    31000 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/css/font-awesome.min.css
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/static/uniauth/js/
+-rwxr-xr-x   0 lanceg     (501) staff       (20)    50676 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/js/bootstrap.min.js
+-rwxr-xr-x   0 lanceg     (501) staff       (20)    86709 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/js/jquery-3.1.1.min.js
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/static/uniauth/img/
+-rwxr-xr-x   0 lanceg     (501) staff       (20)    15406 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/img/favicon.ico
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/static/uniauth/fonts/
+-rwxr-xr-x   0 lanceg     (501) staff       (20)    23424 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/fonts/glyphicons-halflings-regular.woff
+-rwxr-xr-x   0 lanceg     (501) staff       (20)    18028 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/fonts/glyphicons-halflings-regular.woff2
+-rwxr-xr-x   0 lanceg     (501) staff       (20)    77160 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/fonts/fontawesome-webfont.woff2
+-rwxr-xr-x   0 lanceg     (501) staff       (20)    98024 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/static/uniauth/fonts/fontawesome-webfont.woff
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/templates/
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/
+-rw-r--r--   0 lanceg     (501) staff       (20)     4544 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/password-reset-verify.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     1321 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/verification-waiting.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     1577 2020-09-06 01:29:49.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/base.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     5336 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/login.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     2636 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/password-reset.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     1277 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/password-reset-verify-done.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     1108 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/verification-failure.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     1271 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/link-success.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     1248 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/password-reset-done.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     1819 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/verification-success.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     3701 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/link-to-profile.html
+-rw-r--r--   0 lanceg     (501) staff       (20)      208 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/verification-email.html
+-rw-r--r--   0 lanceg     (501) staff       (20)      438 2020-09-06 01:30:38.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/base-site.html
+-rw-r--r--   0 lanceg     (501) staff       (20)    13663 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/settings.html
+-rw-r--r--   0 lanceg     (501) staff       (20)      284 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/password-reset-email.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     1022 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/logout.html
+-rw-r--r--   0 lanceg     (501) staff       (20)     4549 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/uniauth/templates/uniauth/signup.html
+-rw-r--r--   0 lanceg     (501) staff       (20)    30806 2022-11-08 01:49:05.000000 django-uniauth-1.4.1/uniauth/views.py
+-rw-r--r--   0 lanceg     (501) staff       (20)      757 2022-11-08 01:43:42.000000 django-uniauth-1.4.1/uniauth/decorators.py
+-rw-r--r--   0 lanceg     (501) staff       (20)       79 2022-11-08 01:48:57.000000 django-uniauth-1.4.1/pyproject.toml
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/tests/
+-rw-r--r--   0 lanceg     (501) staff       (20)    15169 2022-11-12 22:15:16.000000 django-uniauth-1.4.1/tests/test_utils.py
+-rw-r--r--   0 lanceg     (501) staff       (20)       48 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/tests/models.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     1123 2022-11-12 22:15:15.000000 django-uniauth-1.4.1/tests/test_simple.py
+-rw-r--r--   0 lanceg     (501) staff       (20)        0 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/tests/__init__.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     7543 2022-11-12 22:15:16.000000 django-uniauth-1.4.1/tests/test_merge.py
+-rw-r--r--   0 lanceg     (501) staff       (20)      873 2022-11-12 22:15:15.000000 django-uniauth-1.4.1/tests/utils.py
+-rw-r--r--   0 lanceg     (501) staff       (20)    12295 2022-11-12 22:15:16.000000 django-uniauth-1.4.1/tests/test_commands.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     2602 2022-11-12 22:15:16.000000 django-uniauth-1.4.1/tests/settings.py
+-rw-r--r--   0 lanceg     (501) staff       (20)    11183 2022-11-12 22:15:16.000000 django-uniauth-1.4.1/tests/test_models.py
+-rw-r--r--   0 lanceg     (501) staff       (20)    16368 2022-11-12 22:15:16.000000 django-uniauth-1.4.1/tests/test_backends.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     9648 2022-11-12 22:15:16.000000 django-uniauth-1.4.1/tests/test_view_utils.py
+-rw-r--r--   0 lanceg     (501) staff       (20)      277 2022-11-12 22:15:15.000000 django-uniauth-1.4.1/tests/urls.py
+-rw-r--r--   0 lanceg     (501) staff       (20)     3494 2022-11-12 22:21:54.000000 django-uniauth-1.4.1/tests/test_tokens.py
+-rw-r--r--   0 lanceg     (501) staff       (20)      220 2020-06-07 00:49:12.000000 django-uniauth-1.4.1/MANIFEST.in
+-rw-r--r--   0 lanceg     (501) staff       (20)    25306 2023-07-23 03:04:29.000000 django-uniauth-1.4.1/README.md
+-rw-r--r--   0 lanceg     (501) staff       (20)     1547 2023-07-23 03:04:29.000000 django-uniauth-1.4.1/setup.py
+-rw-r--r--   0 lanceg     (501) staff       (20)       38 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/setup.cfg
+drwxr-xr-x   0 lanceg     (501) staff       (20)        0 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/django_uniauth.egg-info/
+-rw-r--r--   0 lanceg     (501) staff       (20)    28707 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/django_uniauth.egg-info/PKG-INFO
+-rw-r--r--   0 lanceg     (501) staff       (20)     2549 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/django_uniauth.egg-info/SOURCES.txt
+-rw-r--r--   0 lanceg     (501) staff       (20)       99 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/django_uniauth.egg-info/requires.txt
+-rw-r--r--   0 lanceg     (501) staff       (20)       14 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/django_uniauth.egg-info/top_level.txt
+-rw-r--r--   0 lanceg     (501) staff       (20)        1 2023-07-23 03:21:01.000000 django-uniauth-1.4.1/django_uniauth.egg-info/dependency_links.txt
```

### Comparing `django-uniauth-1.4.0/PKG-INFO` & `django-uniauth-1.4.1/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 Metadata-Version: 2.1
 Name: django-uniauth
-Version: 1.4.0
+Version: 1.4.1
 Summary: A Django app for managing CAS and custom user authentication.
 Home-page: https://github.com/lgoodridge/django-uniauth
 Author: Lance Goodridge
 Author-email: ldgoodridge95@gmail.com
 License: LGPLv3
 Description: # django-uniauth
         
-        [![travis][travis-image]][travis-url]
+        [![build][build-image]][build-url]
         [![pyver][pyver-image]][pyver-url]
         [![djangover][djangover-image]][djangover-url]
         [![pypi][pypi-image]][pypi-url]
         
         `django-uniauth` is an app for allowing authentication through services commonly used by universities, such as [CAS](https://www.apereo.org/projects/cas), while also permitting custom authentication schemes. This approach allows developers to leverage the user data contained within university databases, without strictly tethering themselves to those services. It also allows educational software to have a drop-in authentication solution utilizing the single-sign-on mechanisms of universities, typically CAS, to avoid requiring students to create an additional username or password.
         
         The app was designed to replace key features of the built-in `django.contrib.auth` package. Developers may simply replace the appropriate backends and URLs and let Uniauth handle authentication entirely if they wish. However, the app is also fully customizable, and components may be swapped with compatible replacements if desired.
@@ -278,14 +278,17 @@
         
         The source repository contains a `demo_app` directory which demonstrates how to setup a simple Django app to use Uniauth. This app has no functionality, and exists solely to show off the installable `uniauth` app. A quick-start guide for integrating Uniauth can be found [here](https://github.com/lgoodridge/django-uniauth/tree/master/demo_app).
         
         ## Acknowledgements
         
         Special thank you to [Jérémie Lumbroso](https://github.com/jlumbroso) for his guidance in developing this package.
         
+        [build-image]: https://img.shields.io/github/actions/workflow/status/lgoodridge/django-uniauth/run_tests.yml
+        [build-url]: https://github.com/lgoodridge/django-uniauth/actions/workflows/run_tests.yml
+        
         [djangover-image]: https://img.shields.io/pypi/djversions/django-uniauth.svg?label=django
         [djangover-url]: https://pypi.python.org/pypi/django-uniauth/
         
         [license-image]: https://img.shields.io/github/license/lgoodridge/django-uniauth.svg
         [license-url]: https://github.com/lgoodridge/django-uniauth/blob/master/LICENSE.md
         
         [pypi-image]: https://img.shields.io/pypi/v/django-uniauth.svg
@@ -293,38 +296,24 @@
         
         [pyver-image]: https://img.shields.io/pypi/pyversions/django-uniauth.svg
         [pyver-url]: https://pypi.python.org/pypi/django-uniauth/
         
         [status-image]: https://img.shields.io/pypi/status/django-uniauth.svg
         [status-url]: https://pypi.python.org/pypi/django-uniauth/
         
-        [travis-image]: https://img.shields.io/travis/lgoodridge/django-uniauth.svg?style=flat
-        [travis-url]: https://app.travis-ci.com/lgoodridge/django-uniauth
-        
 Keywords: django,auth,authentication,cas,sso,single sign-on
 Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Framework :: Django
 Classifier: Framework :: Django :: 1.11
-Classifier: Framework :: Django :: 2.0
-Classifier: Framework :: Django :: 2.1
-Classifier: Framework :: Django :: 2.2
-Classifier: Framework :: Django :: 3.0
-Classifier: Framework :: Django :: 3.1
-Classifier: Framework :: Django :: 3.2
-Classifier: Framework :: Django :: 4.0
+Classifier: Framework :: Django :: 2
+Classifier: Framework :: Django :: 3
+Classifier: Framework :: Django :: 4
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: GNU Lesser General Public License v3 (LGPLv3)
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 2
-Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.5
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
 Requires-Python: >=2.7, !=3.0.*, !=3.1.*, !=3.2.*, !=3.3.*, !=3.4.*
 Description-Content-Type: text/markdown
```

### Comparing `django-uniauth-1.4.0/LICENSE.md` & `django-uniauth-1.4.1/LICENSE.md`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/migrations/0002_auto_20190707_2305.py` & `django-uniauth-1.4.1/uniauth/migrations/0002_auto_20190707_2305.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/migrations/0001_initial.py` & `django-uniauth-1.4.1/uniauth/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/merge.py` & `django-uniauth-1.4.1/uniauth/merge.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/models.py` & `django-uniauth-1.4.1/uniauth/models.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/management/commands/remove_institution.py` & `django-uniauth-1.4.1/uniauth/management/commands/remove_institution.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/management/commands/add_institution.py` & `django-uniauth-1.4.1/uniauth/management/commands/add_institution.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/management/commands/flush_tmp_users.py` & `django-uniauth-1.4.1/uniauth/management/commands/flush_tmp_users.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/management/commands/migrate_cas.py` & `django-uniauth-1.4.1/uniauth/management/commands/migrate_cas.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/management/commands/migrate_custom.py` & `django-uniauth-1.4.1/uniauth/management/commands/migrate_custom.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/tokens.py` & `django-uniauth-1.4.1/uniauth/tokens.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/forms.py` & `django-uniauth-1.4.1/uniauth/forms.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/backends.py` & `django-uniauth-1.4.1/uniauth/backends.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/utils.py` & `django-uniauth-1.4.1/uniauth/utils.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/urls/cas_only.py` & `django-uniauth-1.4.1/uniauth/urls/cas_only.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/urls/all.py` & `django-uniauth-1.4.1/uniauth/urls/all.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/css/bootstrap.min.css` & `django-uniauth-1.4.1/uniauth/static/uniauth/css/bootstrap.min.css`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/css/theme.css` & `django-uniauth-1.4.1/uniauth/static/uniauth/css/theme.css`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/css/style.css` & `django-uniauth-1.4.1/uniauth/static/uniauth/css/style.css`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/css/font-awesome.min.css` & `django-uniauth-1.4.1/uniauth/static/uniauth/css/font-awesome.min.css`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/js/bootstrap.min.js` & `django-uniauth-1.4.1/uniauth/static/uniauth/js/bootstrap.min.js`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/js/jquery-3.1.1.min.js` & `django-uniauth-1.4.1/uniauth/static/uniauth/js/jquery-3.1.1.min.js`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/img/favicon.ico` & `django-uniauth-1.4.1/uniauth/static/uniauth/img/favicon.ico`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/fonts/glyphicons-halflings-regular.woff` & `django-uniauth-1.4.1/uniauth/static/uniauth/fonts/glyphicons-halflings-regular.woff`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/fonts/glyphicons-halflings-regular.woff2` & `django-uniauth-1.4.1/uniauth/static/uniauth/fonts/glyphicons-halflings-regular.woff2`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/fonts/fontawesome-webfont.woff2` & `django-uniauth-1.4.1/uniauth/static/uniauth/fonts/fontawesome-webfont.woff2`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/static/uniauth/fonts/fontawesome-webfont.woff` & `django-uniauth-1.4.1/uniauth/static/uniauth/fonts/fontawesome-webfont.woff`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/password-reset-verify.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/password-reset-verify.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/verification-waiting.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/verification-waiting.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/base.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/base.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/login.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/login.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/password-reset.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/password-reset.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/password-reset-verify-done.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/password-reset-verify-done.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/verification-failure.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/verification-failure.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/link-success.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/link-success.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/password-reset-done.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/password-reset-done.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/verification-success.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/verification-success.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/link-to-profile.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/link-to-profile.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/settings.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/settings.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/logout.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/logout.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/templates/uniauth/signup.html` & `django-uniauth-1.4.1/uniauth/templates/uniauth/signup.html`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/views.py` & `django-uniauth-1.4.1/uniauth/views.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/uniauth/decorators.py` & `django-uniauth-1.4.1/uniauth/decorators.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/test_utils.py` & `django-uniauth-1.4.1/tests/test_utils.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/test_simple.py` & `django-uniauth-1.4.1/tests/test_simple.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/test_merge.py` & `django-uniauth-1.4.1/tests/test_merge.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/utils.py` & `django-uniauth-1.4.1/tests/utils.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/test_commands.py` & `django-uniauth-1.4.1/tests/test_commands.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/settings.py` & `django-uniauth-1.4.1/tests/settings.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/test_models.py` & `django-uniauth-1.4.1/tests/test_models.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/test_backends.py` & `django-uniauth-1.4.1/tests/test_backends.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/test_view_utils.py` & `django-uniauth-1.4.1/tests/test_view_utils.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/tests/test_tokens.py` & `django-uniauth-1.4.1/tests/test_tokens.py`

 * *Files identical despite different names*

### Comparing `django-uniauth-1.4.0/README.md` & `django-uniauth-1.4.1/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # django-uniauth
 
-[![travis][travis-image]][travis-url]
+[![build][build-image]][build-url]
 [![pyver][pyver-image]][pyver-url]
 [![djangover][djangover-image]][djangover-url]
 [![pypi][pypi-image]][pypi-url]
 
 `django-uniauth` is an app for allowing authentication through services commonly used by universities, such as [CAS](https://www.apereo.org/projects/cas), while also permitting custom authentication schemes. This approach allows developers to leverage the user data contained within university databases, without strictly tethering themselves to those services. It also allows educational software to have a drop-in authentication solution utilizing the single-sign-on mechanisms of universities, typically CAS, to avoid requiring students to create an additional username or password.
 
 The app was designed to replace key features of the built-in `django.contrib.auth` package. Developers may simply replace the appropriate backends and URLs and let Uniauth handle authentication entirely if they wish. However, the app is also fully customizable, and components may be swapped with compatible replacements if desired.
@@ -270,24 +270,24 @@
 
 The source repository contains a `demo_app` directory which demonstrates how to setup a simple Django app to use Uniauth. This app has no functionality, and exists solely to show off the installable `uniauth` app. A quick-start guide for integrating Uniauth can be found [here](https://github.com/lgoodridge/django-uniauth/tree/master/demo_app).
 
 ## Acknowledgements
 
 Special thank you to [Jérémie Lumbroso](https://github.com/jlumbroso) for his guidance in developing this package.
 
+[build-image]: https://img.shields.io/github/actions/workflow/status/lgoodridge/django-uniauth/run_tests.yml
+[build-url]: https://github.com/lgoodridge/django-uniauth/actions/workflows/run_tests.yml
+
 [djangover-image]: https://img.shields.io/pypi/djversions/django-uniauth.svg?label=django
 [djangover-url]: https://pypi.python.org/pypi/django-uniauth/
 
 [license-image]: https://img.shields.io/github/license/lgoodridge/django-uniauth.svg
 [license-url]: https://github.com/lgoodridge/django-uniauth/blob/master/LICENSE.md
 
 [pypi-image]: https://img.shields.io/pypi/v/django-uniauth.svg
 [pypi-url]: https://pypi.python.org/pypi/django-uniauth/
 
 [pyver-image]: https://img.shields.io/pypi/pyversions/django-uniauth.svg
 [pyver-url]: https://pypi.python.org/pypi/django-uniauth/
 
 [status-image]: https://img.shields.io/pypi/status/django-uniauth.svg
 [status-url]: https://pypi.python.org/pypi/django-uniauth/
-
-[travis-image]: https://img.shields.io/travis/lgoodridge/django-uniauth.svg?style=flat
-[travis-url]: https://app.travis-ci.com/lgoodridge/django-uniauth
```

### Comparing `django-uniauth-1.4.0/django_uniauth.egg-info/PKG-INFO` & `django-uniauth-1.4.1/django_uniauth.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 Metadata-Version: 2.1
 Name: django-uniauth
-Version: 1.4.0
+Version: 1.4.1
 Summary: A Django app for managing CAS and custom user authentication.
 Home-page: https://github.com/lgoodridge/django-uniauth
 Author: Lance Goodridge
 Author-email: ldgoodridge95@gmail.com
 License: LGPLv3
 Description: # django-uniauth
         
-        [![travis][travis-image]][travis-url]
+        [![build][build-image]][build-url]
         [![pyver][pyver-image]][pyver-url]
         [![djangover][djangover-image]][djangover-url]
         [![pypi][pypi-image]][pypi-url]
         
         `django-uniauth` is an app for allowing authentication through services commonly used by universities, such as [CAS](https://www.apereo.org/projects/cas), while also permitting custom authentication schemes. This approach allows developers to leverage the user data contained within university databases, without strictly tethering themselves to those services. It also allows educational software to have a drop-in authentication solution utilizing the single-sign-on mechanisms of universities, typically CAS, to avoid requiring students to create an additional username or password.
         
         The app was designed to replace key features of the built-in `django.contrib.auth` package. Developers may simply replace the appropriate backends and URLs and let Uniauth handle authentication entirely if they wish. However, the app is also fully customizable, and components may be swapped with compatible replacements if desired.
@@ -278,14 +278,17 @@
         
         The source repository contains a `demo_app` directory which demonstrates how to setup a simple Django app to use Uniauth. This app has no functionality, and exists solely to show off the installable `uniauth` app. A quick-start guide for integrating Uniauth can be found [here](https://github.com/lgoodridge/django-uniauth/tree/master/demo_app).
         
         ## Acknowledgements
         
         Special thank you to [Jérémie Lumbroso](https://github.com/jlumbroso) for his guidance in developing this package.
         
+        [build-image]: https://img.shields.io/github/actions/workflow/status/lgoodridge/django-uniauth/run_tests.yml
+        [build-url]: https://github.com/lgoodridge/django-uniauth/actions/workflows/run_tests.yml
+        
         [djangover-image]: https://img.shields.io/pypi/djversions/django-uniauth.svg?label=django
         [djangover-url]: https://pypi.python.org/pypi/django-uniauth/
         
         [license-image]: https://img.shields.io/github/license/lgoodridge/django-uniauth.svg
         [license-url]: https://github.com/lgoodridge/django-uniauth/blob/master/LICENSE.md
         
         [pypi-image]: https://img.shields.io/pypi/v/django-uniauth.svg
@@ -293,38 +296,24 @@
         
         [pyver-image]: https://img.shields.io/pypi/pyversions/django-uniauth.svg
         [pyver-url]: https://pypi.python.org/pypi/django-uniauth/
         
         [status-image]: https://img.shields.io/pypi/status/django-uniauth.svg
         [status-url]: https://pypi.python.org/pypi/django-uniauth/
         
-        [travis-image]: https://img.shields.io/travis/lgoodridge/django-uniauth.svg?style=flat
-        [travis-url]: https://app.travis-ci.com/lgoodridge/django-uniauth
-        
 Keywords: django,auth,authentication,cas,sso,single sign-on
 Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Framework :: Django
 Classifier: Framework :: Django :: 1.11
-Classifier: Framework :: Django :: 2.0
-Classifier: Framework :: Django :: 2.1
-Classifier: Framework :: Django :: 2.2
-Classifier: Framework :: Django :: 3.0
-Classifier: Framework :: Django :: 3.1
-Classifier: Framework :: Django :: 3.2
-Classifier: Framework :: Django :: 4.0
+Classifier: Framework :: Django :: 2
+Classifier: Framework :: Django :: 3
+Classifier: Framework :: Django :: 4
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: GNU Lesser General Public License v3 (LGPLv3)
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 2
-Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.5
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
 Requires-Python: >=2.7, !=3.0.*, !=3.1.*, !=3.2.*, !=3.3.*, !=3.4.*
 Description-Content-Type: text/markdown
```

### Comparing `django-uniauth-1.4.0/django_uniauth.egg-info/SOURCES.txt` & `django-uniauth-1.4.1/django_uniauth.egg-info/SOURCES.txt`

 * *Files identical despite different names*

