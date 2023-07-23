# Comparing `tmp/django-outbox-menu-1.0.8.tar.gz` & `tmp/django-outbox-menu-1.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-outbox-menu-1.0.8.tar", last modified: Fri Oct 28 22:03:29 2022, max compression
+gzip compressed data, was "django-outbox-menu-1.0.9.tar", last modified: Tue Nov 22 03:35:42 2022, max compression
```

## Comparing `django-outbox-menu-1.0.8.tar` & `django-outbox-menu-1.0.9.tar`

### file list

```diff
@@ -1,71 +1,72 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.432865 django-outbox-menu-1.0.8/
--rw-r--r--   0 runner    (1001) docker     (121)     1521 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)      138 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)     3915 2022-10-28 22:03:29.432865 django-outbox-menu-1.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     3458 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.424865 django-outbox-menu-1.0.8/django_outbox_menu.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     3915 2022-10-28 22:03:29.000000 django-outbox-menu-1.0.8/django_outbox_menu.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2025 2022-10-28 22:03:29.000000 django-outbox-menu-1.0.8/django_outbox_menu.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-10-28 22:03:29.000000 django-outbox-menu-1.0.8/django_outbox_menu.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)        5 2022-10-28 22:03:29.000000 django-outbox-menu-1.0.8/django_outbox_menu.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.424865 django-outbox-menu-1.0.8/menu/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      250 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/_version.py
--rw-r--r--   0 runner    (1001) docker     (121)      811 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/admin.py
--rw-r--r--   0 runner    (1001) docker     (121)      140 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/apps.py
--rw-r--r--   0 runner    (1001) docker     (121)    11555 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/menus.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.424865 django-outbox-menu-1.0.8/menu/migrations/
--rw-r--r--   0 runner    (1001) docker     (121)     3000 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/migrations/0001_initial.py
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/migrations/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     7829 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/models.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.420865 django-outbox-menu-1.0.8/menu/static/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.424865 django-outbox-menu-1.0.8/menu/static/css/
--rw-r--r--   0 runner    (1001) docker     (121)    35789 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/css/main.css
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.420865 django-outbox-menu-1.0.8/menu/static/fonts/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.420865 django-outbox-menu-1.0.8/menu/static/fonts/iconic/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.424865 django-outbox-menu-1.0.8/menu/static/fonts/iconic/css/
--rw-r--r--   0 runner    (1001) docker     (121)    85304 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/fonts/iconic/css/material-design-iconic-font.css
--rw-r--r--   0 runner    (1001) docker     (121)    70815 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/fonts/iconic/css/material-design-iconic-font.min.css
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.424865 django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/
--rw-r--r--   0 runner    (1001) docker     (121)    42495 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.eot
--rw-r--r--   0 runner    (1001) docker     (121)   238287 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.svg
--rw-r--r--   0 runner    (1001) docker     (121)    99212 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.ttf
--rw-r--r--   0 runner    (1001) docker     (121)    50312 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.woff
--rw-r--r--   0 runner    (1001) docker     (121)    38384 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.woff2
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.420865 django-outbox-menu-1.0.8/menu/static/vendor/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.420865 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.428865 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/
--rw-r--r--   0 runner    (1001) docker     (121)    29140 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-grid.css
--rw-r--r--   0 runner    (1001) docker     (121)    73751 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-grid.css.map
--rw-r--r--   0 runner    (1001) docker     (121)    21780 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-grid.min.css
--rw-r--r--   0 runner    (1001) docker     (121)    52677 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-grid.min.css.map
--rw-r--r--   0 runner    (1001) docker     (121)     4486 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-reboot.css
--rw-r--r--   0 runner    (1001) docker     (121)    51030 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-reboot.css.map
--rw-r--r--   0 runner    (1001) docker     (121)     3604 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-reboot.min.css
--rw-r--r--   0 runner    (1001) docker     (121)    24646 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-reboot.min.css.map
--rw-r--r--   0 runner    (1001) docker     (121)   156884 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap.css
--rw-r--r--   0 runner    (1001) docker     (121)   379132 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap.css.map
--rw-r--r--   0 runner    (1001) docker     (121)   124962 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap.min.css
--rw-r--r--   0 runner    (1001) docker     (121)   502438 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap.min.css.map
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.428865 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/
--rw-r--r--   0 runner    (1001) docker     (121)   111390 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/bootstrap.js
--rw-r--r--   0 runner    (1001) docker     (121)    51143 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/bootstrap.min.js
--rw-r--r--   0 runner    (1001) docker     (121)    81670 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/popper.js
--rw-r--r--   0 runner    (1001) docker     (121)    19033 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/popper.min.js
--rw-r--r--   0 runner    (1001) docker     (121)    17299 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/tooltip.js
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.428865 django-outbox-menu-1.0.8/menu/static/vendor/jquery/
--rw-r--r--   0 runner    (1001) docker     (121)    86659 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/static/vendor/jquery/jquery-3.2.1.min.js
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.432865 django-outbox-menu-1.0.8/menu/templates/
--rw-r--r--   0 runner    (1001) docker     (121)      939 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/templates/index.html
--rw-r--r--   0 runner    (1001) docker     (121)     7268 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/templates/test-menu.html
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.432865 django-outbox-menu-1.0.8/menu/templatetags/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/templatetags/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-28 22:03:29.432865 django-outbox-menu-1.0.8/menu/templatetags/__pycache__/
--rw-r--r--   0 runner    (1001) docker     (121)      171 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/templatetags/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0 runner    (1001) docker     (121)     2720 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/templatetags/__pycache__/menu_tags.cpython-310.pyc
--rw-r--r--   0 runner    (1001) docker     (121)     5851 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/templatetags/menu_tags.py
--rw-r--r--   0 runner    (1001) docker     (121)       60 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/tests.py
--rw-r--r--   0 runner    (1001) docker     (121)      324 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/urls.py
--rw-r--r--   0 runner    (1001) docker     (121)      221 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/menu/views.py
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-10-28 22:03:29.432865 django-outbox-menu-1.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     4860 2022-10-28 22:03:21.000000 django-outbox-menu-1.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.043089 django-outbox-menu-1.0.9/
+-rw-r--r--   0 runner    (1001) docker     (121)     1521 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (121)      138 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (121)     3915 2022-11-22 03:35:42.043089 django-outbox-menu-1.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     3458 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.035089 django-outbox-menu-1.0.9/django_outbox_menu.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     3915 2022-11-22 03:35:41.000000 django-outbox-menu-1.0.9/django_outbox_menu.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     2066 2022-11-22 03:35:41.000000 django-outbox-menu-1.0.9/django_outbox_menu.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-11-22 03:35:41.000000 django-outbox-menu-1.0.9/django_outbox_menu.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       14 2022-11-22 03:35:41.000000 django-outbox-menu-1.0.9/django_outbox_menu.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        5 2022-11-22 03:35:41.000000 django-outbox-menu-1.0.9/django_outbox_menu.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.035089 django-outbox-menu-1.0.9/menu/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)      318 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/_version.py
+-rw-r--r--   0 runner    (1001) docker     (121)      916 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/admin.py
+-rw-r--r--   0 runner    (1001) docker     (121)      140 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/apps.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12164 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/menus.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.035089 django-outbox-menu-1.0.9/menu/migrations/
+-rw-r--r--   0 runner    (1001) docker     (121)     5212 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/migrations/0001_initial.py
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/migrations/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8410 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/models.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.031089 django-outbox-menu-1.0.9/menu/static/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.035089 django-outbox-menu-1.0.9/menu/static/css/
+-rw-r--r--   0 runner    (1001) docker     (121)    35789 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/css/main.css
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.031089 django-outbox-menu-1.0.9/menu/static/fonts/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.031089 django-outbox-menu-1.0.9/menu/static/fonts/iconic/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.035089 django-outbox-menu-1.0.9/menu/static/fonts/iconic/css/
+-rw-r--r--   0 runner    (1001) docker     (121)    85304 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/fonts/iconic/css/material-design-iconic-font.css
+-rw-r--r--   0 runner    (1001) docker     (121)    70815 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/fonts/iconic/css/material-design-iconic-font.min.css
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.035089 django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/
+-rw-r--r--   0 runner    (1001) docker     (121)    42495 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.eot
+-rw-r--r--   0 runner    (1001) docker     (121)   238287 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.svg
+-rw-r--r--   0 runner    (1001) docker     (121)    99212 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.ttf
+-rw-r--r--   0 runner    (1001) docker     (121)    50312 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.woff
+-rw-r--r--   0 runner    (1001) docker     (121)    38384 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.woff2
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.031089 django-outbox-menu-1.0.9/menu/static/vendor/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.031089 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.039089 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/
+-rw-r--r--   0 runner    (1001) docker     (121)    29140 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-grid.css
+-rw-r--r--   0 runner    (1001) docker     (121)    73751 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-grid.css.map
+-rw-r--r--   0 runner    (1001) docker     (121)    21780 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-grid.min.css
+-rw-r--r--   0 runner    (1001) docker     (121)    52677 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-grid.min.css.map
+-rw-r--r--   0 runner    (1001) docker     (121)     4486 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-reboot.css
+-rw-r--r--   0 runner    (1001) docker     (121)    51030 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-reboot.css.map
+-rw-r--r--   0 runner    (1001) docker     (121)     3604 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-reboot.min.css
+-rw-r--r--   0 runner    (1001) docker     (121)    24646 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-reboot.min.css.map
+-rw-r--r--   0 runner    (1001) docker     (121)   156884 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap.css
+-rw-r--r--   0 runner    (1001) docker     (121)   379132 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap.css.map
+-rw-r--r--   0 runner    (1001) docker     (121)   124962 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap.min.css
+-rw-r--r--   0 runner    (1001) docker     (121)   502438 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap.min.css.map
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.039089 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/
+-rw-r--r--   0 runner    (1001) docker     (121)   111390 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/bootstrap.js
+-rw-r--r--   0 runner    (1001) docker     (121)    51143 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/bootstrap.min.js
+-rw-r--r--   0 runner    (1001) docker     (121)    81670 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/popper.js
+-rw-r--r--   0 runner    (1001) docker     (121)    19033 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/popper.min.js
+-rw-r--r--   0 runner    (1001) docker     (121)    17299 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/tooltip.js
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.039089 django-outbox-menu-1.0.9/menu/static/vendor/jquery/
+-rw-r--r--   0 runner    (1001) docker     (121)    86659 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/static/vendor/jquery/jquery-3.2.1.min.js
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.039089 django-outbox-menu-1.0.9/menu/templates/
+-rw-r--r--   0 runner    (1001) docker     (121)     1071 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/templates/index.html
+-rw-r--r--   0 runner    (1001) docker     (121)     7268 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/templates/test-menu.html
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.043089 django-outbox-menu-1.0.9/menu/templatetags/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/templatetags/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-22 03:35:42.043089 django-outbox-menu-1.0.9/menu/templatetags/__pycache__/
+-rw-r--r--   0 runner    (1001) docker     (121)      171 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/templatetags/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0 runner    (1001) docker     (121)     3249 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/templatetags/__pycache__/menu_tags.cpython-310.pyc
+-rw-r--r--   0 runner    (1001) docker     (121)     6496 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/templatetags/menu_tags.py
+-rw-r--r--   0 runner    (1001) docker     (121)       60 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/tests.py
+-rw-r--r--   0 runner    (1001) docker     (121)      324 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/urls.py
+-rw-r--r--   0 runner    (1001) docker     (121)      221 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/menu/views.py
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2022-11-22 03:35:42.043089 django-outbox-menu-1.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)     4834 2022-11-22 03:35:26.000000 django-outbox-menu-1.0.9/setup.py
```

### Comparing `django-outbox-menu-1.0.8/LICENSE` & `django-outbox-menu-1.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/PKG-INFO` & `django-outbox-menu-1.0.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-outbox-menu
-Version: 1.0.8
+Version: 1.0.9
 Summary: DJANGO OUTBOX MENU
 Home-page: https://github.com/PROJECT-OUTBOX/django_lib_outbox_menu.git
 Author-email: suratiwan03@gmail.com
 Keywords: menu,model base,environment,django
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Intended Audience :: Developers
 Classifier: Programming Language :: Python :: 3 :: Only
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: django-outbox-menu Version: 1.0.8 Summary: DJANGO
+Metadata-Version: 2.1 Name: django-outbox-menu Version: 1.0.9 Summary: DJANGO
 OUTBOX MENU Home-page: https://github.com/PROJECT-OUTBOX/
 django_lib_outbox_menu.git Author-email: suratiwan03@gmail.com Keywords:
 menu,model base,environment,django Classifier: License :: OSI Approved :: BSD
 License Classifier: Intended Audience :: Developers Classifier: Programming
 Language :: Python :: 3 :: Only Description-Content-Type: text/markdown
 License-File: LICENSE # DJANGO OUTBOX MENU Menu is almost use in every web
 project. With this library you can create menu for backend and frontend project
```

### Comparing `django-outbox-menu-1.0.8/README.md` & `django-outbox-menu-1.0.9/README.md`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/django_outbox_menu.egg-info/PKG-INFO` & `django-outbox-menu-1.0.9/django_outbox_menu.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-outbox-menu
-Version: 1.0.8
+Version: 1.0.9
 Summary: DJANGO OUTBOX MENU
 Home-page: https://github.com/PROJECT-OUTBOX/django_lib_outbox_menu.git
 Author-email: suratiwan03@gmail.com
 Keywords: menu,model base,environment,django
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Intended Audience :: Developers
 Classifier: Programming Language :: Python :: 3 :: Only
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: django-outbox-menu Version: 1.0.8 Summary: DJANGO
+Metadata-Version: 2.1 Name: django-outbox-menu Version: 1.0.9 Summary: DJANGO
 OUTBOX MENU Home-page: https://github.com/PROJECT-OUTBOX/
 django_lib_outbox_menu.git Author-email: suratiwan03@gmail.com Keywords:
 menu,model base,environment,django Classifier: License :: OSI Approved :: BSD
 License Classifier: Intended Audience :: Developers Classifier: Programming
 Language :: Python :: 3 :: Only Description-Content-Type: text/markdown
 License-File: LICENSE # DJANGO OUTBOX MENU Menu is almost use in every web
 project. With this library you can create menu for backend and frontend project
```

### Comparing `django-outbox-menu-1.0.8/django_outbox_menu.egg-info/SOURCES.txt` & `django-outbox-menu-1.0.9/django_outbox_menu.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 LICENSE
 MANIFEST.in
 README.md
 setup.py
 django_outbox_menu.egg-info/PKG-INFO
 django_outbox_menu.egg-info/SOURCES.txt
 django_outbox_menu.egg-info/dependency_links.txt
+django_outbox_menu.egg-info/requires.txt
 django_outbox_menu.egg-info/top_level.txt
 menu/__init__.py
 menu/_version.py
 menu/admin.py
 menu/apps.py
 menu/menus.py
 menu/models.py
```

### Comparing `django-outbox-menu-1.0.8/menu/admin.py` & `django-outbox-menu-1.0.9/menu/admin.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,26 +1,28 @@
 from django.contrib import admin
 from .models import Menu, MenuGroup, MenuCustom
+from parler.admin import TranslatableAdmin
 
-class MenuAdmin(admin.ModelAdmin):    
-    list_filter = ('name', 'parent',) 
-    list_display = ['name', 'parent', 'link', 'order_menu', 'kind', 'updated_at']
-    search_fields = ('name', 'parent')
-    ordering = ('-updated_at',)
+# class MenuAdmin(admin.ModelAdmin):    
+#     list_filter = ('name', 'parent',) 
+#     list_display = ['name', 'parent', 'link', 'order_menu', 'kind', 'updated_at']
+#     search_fields = ('name', 'parent')
+#     ordering = ('-updated_at',)
 
-admin.site.register(Menu, MenuAdmin)
+admin.site.register(Menu, TranslatableAdmin)
 
-class MenuGroupAdmin(admin.ModelAdmin):
-    list_filter = ('name',) 
-    list_display = ['name', 'updated_at']
-    search_fields = ('name',)
-    ordering = ('-updated_at',)
+# class MenuGroupAdmin(admin.ModelAdmin):
+#     list_filter = ('name',) 
+#     list_display = ['name', 'updated_at']
+#     search_fields = ('name',)
+#     ordering = ('-updated_at',)
 
-admin.site.register(MenuGroup, MenuGroupAdmin)
+admin.site.register(MenuGroup, TranslatableAdmin)
 
+# tidak di update model yg ini
 class MenuCustomAdmin(admin.ModelAdmin):
     list_filter = ('menu',) 
     list_display = ['menu', 'menu_group', 'updated_at']
     search_fields = ('menu',)
     ordering = ('-updated_at',)
 
 admin.site.register(MenuCustom, MenuCustomAdmin)
```

### Comparing `django-outbox-menu-1.0.8/menu/menus.py` & `django-outbox-menu-1.0.9/menu/menus.py`

 * *Files 4% similar despite different names*

```diff
@@ -39,33 +39,41 @@
 # 6. Atur active menu
 # Buat function baru untuk Atur BreadCrumb, tambahkan List of Dictionary dengan format 
 #       [{'Nama','href'},{'nama2','href2'}]
 #       Data ini akan di cek di template dengan cara yang sama seperti generate menu
 #  --------------------------------------------------------------------------------------------------          
 
 from django.db.models import F
-
 from .models import Menu, MenuCustom
 
 
 class Menus:    
     # mLvl_prev = -1   # catat level sebelumnya  
     mList_recursive = []
     mList_active = []
     menu_custom_list = []   # exclude this menu from default menus
     # mDict = {}     
     # mList = []      # result ada di mList
     site_id = 1
+    lang = 'id'
 
-    # defailt menu_group = 0 artinya front end
+    # defailt menu_group = 0 artinya all
+    # kinds = 1 Front end
+    # kinds =2 backend
+    # kinds =0 all
     def __init__(self, menu_group = 0, kinds = 0, site_id = 1): #, pIs_master_menu = False):         # menu_group adalah filter untuk company tertentu saja
         '''
             Jika pKind = 0 maka ambil data semua, frontend dan backend
         '''
         self.site_id = site_id
+
+        # get active language
+        obj = Menu()
+        self.lang = obj.get_current_language()
+
         if len(self.mList_recursive) == 0:
             #if menu_group != "":
             self.create_menus(menu_group, kinds) #, pIs_master_menu)
         else:
             # self.mDict = {}  # clear dulu (karena prosedur init ini sekali dijalankan saat class di buat)
             self.mList_recursive = []
             self.mList_active = []
@@ -99,26 +107,29 @@
         # 1. Clear circular reference (ignore it, or set as None)
         self.ignore_circular_parent()
        
         # exclude custom menu tidak digunakan disini karena hanya di ambil root menu saja
         # [UPDATE] tetap digunakan untuk antisipasi root menu digunakan sebagai custom menu
         self.get_menu_custom_list(menu_group)
 
+        # get active language
+        
+
         # 2. Get data by user options (UPDATE only get ROOT MENU base on User OPTION)
         # Harus konversi ke integer karena tidak masuk ke kondisi        
         if int(kinds) == 0: # jika kind = 0 ambil semua data front end dan back end            
-            mData = Menu.objects.filter(menu_group__id=menu_group, is_visibled=True, parent=None) \
+            mData = Menu.objects.language(self.lang).filter(menu_group__id=menu_group, is_visibled=True, parent=None) \
                 .exclude(id__in=self.menu_custom_list) \
                 .order_by('parent_id','order_menu').values('id')     
         elif int(menu_group) == 0:   # menu group = 0 artinya menu frontend            
-            mData = Menu.objects.filter(kind=kinds, is_visibled=True, parent=None) \
+            mData = Menu.objects.language(self.lang).filter(kind=kinds, is_visibled=True, parent=None) \
                 .exclude(id__in=self.menu_custom_list) \
                 .order_by('parent_id','order_menu').values('id')     
         else:            
-            mData = Menu.objects.filter(menu_group__id=menu_group, kind=kinds, is_visibled=True, parent=None) \
+            mData = Menu.objects.language(self.lang).filter(menu_group__id=menu_group, kind=kinds, is_visibled=True, parent=None) \
                 .exclude(id__in=self.menu_custom_list) \
                 .order_by('parent_id','order_menu').values('id')                  
 
         # .exclude(id__in=menu_custom_list) \
         # 3. Get root menu
         # get menu id only
         # print(mData)
@@ -143,18 +154,23 @@
         # 6. get complete data base on mData
         self.get_menus_complete()
 
         # 6. return result
         #return self.get_menus()
 
     def get_menus_complete(self):
+        # obj = Menu()
+        # lang = obj.get_current_language()
+
         mCount = 0
         while mCount < len(self.mList_recursive):
-            mData = Menu.objects.get(id=self.mList_recursive[mCount]['id'])
+            mData = Menu.objects.language(self.lang).get(id=self.mList_recursive[mCount]['id'])
             # print(mData)
+            self.mList_recursive[mCount]['uuid'] = mData.uuid
+            self.mList_recursive[mCount]['order_menu'] = mData.order_menu
             self.mList_recursive[mCount]['name'] = mData.name
             self.mList_recursive[mCount]['link'] = mData.link
             self.mList_recursive[mCount]['icon'] = mData.icon
             self.mList_recursive[mCount]['is_external'] = mData.is_external
             self.mList_recursive[mCount]['parent_id'] = mData.parent_id
 
             mCount += 1
@@ -168,14 +184,15 @@
     #     return ret
 
     def is_have_child(self, menu_id):
         '''
             cek apakah ada menu dengan parent = menu_id?
             jika ya return True, else False
         '''
+        # tidak perlu lang disini karena tidak ada field name di ambil
         data = Menu.objects.filter(parent_id=menu_id) \
             .exclude(id__in=self.menu_custom_list) \
             .order_by('parent_id','order_menu').values('id')        
         ret = []
         for i in data:
             ret.append(i['id'])
 
@@ -230,15 +247,15 @@
             mCount += 1
 
     # Menu bisa diberikan dengan nama yg sama, oleh karena itu cari active menu dan breadcrumb menggunakan ID
     def get_active_menu(self, menu_id):
         '''
             Find active menu recursively
         '''        
-        data = Menu.objects.filter(id=menu_id) \
+        data = Menu.objects.language(self.lang).filter(id=menu_id) \
                 .exclude(id__in=self.menu_custom_list) 
         if data:
             for i in data:
                 # print(i.parent_id)
                 parent_id = i.parent_id
                 self.mList_active.insert(0, {'id': i.id, 'name': i.name, 'link': i.link, 'icon': i.icon, 'is_external':i.is_external})
                 self.get_active_menu(parent_id)
```

### Comparing `django-outbox-menu-1.0.8/menu/models.py` & `django-outbox-menu-1.0.9/menu/models.py`

 * *Files 5% similar despite different names*

```diff
@@ -3,14 +3,16 @@
     29th September 2022
     Grid Software, Inc.
 '''
 # from django.contrib.auth.models import User
 # from django.contrib.auth import get_user_model
 from django.contrib.sites.models import Site
 from django.db import models
+from parler.models import TranslatableModel, TranslatedFields
+import uuid
 
 # User = get_user_model()
 
 class OptMenuKinds(models.IntegerChoices):
     '''
         Jenis menu : 
             0 : Front end without user login
@@ -24,57 +26,61 @@
     FRONTEND = 1
     BACKEND = 2 
     # Tidak jadi karena crash dengan unique together di model
     # BACKEND_DEFAULT = 3 # Penanda user baru login, belum ada company yg aktif, sehingga menu belum bisa di generate
                         # untuk itu generate menu default langsung   
 
 
-class MenuGroup(models.Model):
+class MenuGroup(TranslatableModel):
     '''
         Group : Model Menu
         Simpan data group menu :
         1. Owner
         2. Manager
         3. Operator
         4. Kasir
         5. dll...
 
         Tidak ada interface, maintenance di halaman admin
     '''
     # Update 19 Oktober 2022
     # untuk membedakan menu project 1 dengan yg lain, dengan nama sama
     site = models.ForeignKey(Site, on_delete=models.CASCADE)
+    uuid = models.UUIDField(unique=True, default=uuid.uuid4, editable=False)
 
     # Tidak boleh ada data kembar di name
-    name = models.CharField(max_length=100) # unique=True (Unique together with site)
+    translations = TranslatedFields(
+        name = models.CharField(max_length=100) # unique=True (Unique together with site)
+    )
 
     created_at = models.DateTimeField(auto_now_add=True, editable=False)
     updated_at = models.DateTimeField(auto_now=True, editable=False)    
 
     # Optional Fields:
     # created_at = models.DateTimeField(auto_now_add=True)
     # updated_at = models.DateTimeField(auto_now=True)
 
     # objects = MenuGroupManager()
     
-    def __str__(self):
+    # def __str__(self):
+    def __unicode__(self):
         return self.name
 
-    class Meta:
-        constraints = [
-            models.UniqueConstraint(fields=['site', 'name'], name='unique_site_name')
-        ]
+    # class Meta:
+    #     constraints = [
+    #         models.UniqueConstraint(fields=['site', 'translations__name'], name='unique_site_name')
+    #     ]
 
 # def company_name_validate(value):
 #     if len(value) < 3:
 #         raise ValidationError("Company name mush be more than 3 character")
 #     else:
 #         return value
 
-class Menu(models.Model):
+class Menu(TranslatableModel):
     '''    
         Relase :
             User --1:N-- Menu
         Deskripsi :
             # Menu di buat per user,
             # Satu company bisa mempunyai banyak user,
             # Satu User bisa punya banyak menu
@@ -82,16 +88,20 @@
     
         # ada 1 company dengan site ID = 1 sebagai master menu
         # seluruh menu di create dari site ini (berarti is_master_menu tidak di perlukan lagi)
         # Untuk menu di app blog, user tidak dalam kondisi login
         # Untuk menu di app inventory, user harus login dulu        
         # Jika user telah di create, langsung generate menu untuk user tersebut
         # dapat di visible sesuai kebutuhan
-    '''       
-    name = models.CharField(max_length=100)
+    '''      
+    # ID tetap di create otomaris
+    uuid = models.UUIDField(unique=True, default=uuid.uuid4, editable=False) 
+    translations = TranslatedFields(
+        name = models.CharField(max_length=100)
+    )
 
     # menu group, relasi many to many 
     # Untuk frontend menu group kosong
     menu_group = models.ManyToManyField(MenuGroup, blank=True) # , null=True, blank=True)  not effect to m2m relation
 
     # Optional Fields:
     # user = models.ForeignKey(User, null=True, blank=True, on_delete=models.PROTECT)        # Menu di generate per user   
@@ -173,15 +183,16 @@
     #     return get_natural_datetime(self.updated_at)        
     
     # def updated_at_(self):
     #     return  "naturalday(self.updated_at)"
        # return serializers.serialize("json",' naturalday(self.updated_at)')
         #return serializers.serialize('json', naturalday(self.updated_at))
 
-    def __str__(self):          
+    # def __str__(self):          
+    def __unicode__(self):
         if self.kind == OptMenuKinds.FRONTEND:
             res = '[ Front-End ]'       # halaman depan
         # elif self.kind == OptMenuKinds.BACKEND_DEFAULT:
         #     res = '[ Default ]'
         else:
             res = '[ Back-End ]'        # halaman dashboard
 
@@ -191,14 +202,18 @@
             par = 'ROOT'
 
         return "{} {} > {}".format(res, par, self.name)  
 
 
 class MenuCustom(models.Model):
     '''
+        # Akan di hapus di versi berikutnya
+        # status deprecated
+
+        # tidak ada update ke multi language khusus model ini
         Custom menu adalah menu yg hanya muncul di site dan menu_group tertentu saja
         tidak muncul di tempat lain
     '''
     # Menu ini digunakan untuk filter custom menu yg ada di site, exlude menu_group ada di get_menu_custom_list menus.py
     site = models.ForeignKey(Site, on_delete=models.CASCADE)
 
     menu_group = models.ForeignKey(MenuGroup, on_delete=models.PROTECT) #, blank=True, null=True)
```

### Comparing `django-outbox-menu-1.0.8/menu/static/css/main.css` & `django-outbox-menu-1.0.9/menu/static/css/main.css`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/fonts/iconic/css/material-design-iconic-font.css` & `django-outbox-menu-1.0.9/menu/static/fonts/iconic/css/material-design-iconic-font.css`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/fonts/iconic/css/material-design-iconic-font.min.css` & `django-outbox-menu-1.0.9/menu/static/fonts/iconic/css/material-design-iconic-font.min.css`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.eot` & `django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.eot`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.svg` & `django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.svg`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.ttf` & `django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.ttf`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.woff` & `django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.woff`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.woff2` & `django-outbox-menu-1.0.9/menu/static/fonts/iconic/fonts/Material-Design-Iconic-Font.woff2`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-grid.css` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-grid.css`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-grid.css.map` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-grid.css.map`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-grid.min.css` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-grid.min.css`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-grid.min.css.map` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-grid.min.css.map`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-reboot.css` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-reboot.css`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-reboot.css.map` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-reboot.css.map`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-reboot.min.css` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-reboot.min.css`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap-reboot.min.css.map` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap-reboot.min.css.map`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap.css` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap.css`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap.css.map` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap.css.map`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap.min.css` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap.min.css`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/css/bootstrap.min.css.map` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/css/bootstrap.min.css.map`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/bootstrap.js` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/bootstrap.js`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/bootstrap.min.js` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/bootstrap.min.js`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/popper.js` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/popper.js`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/popper.min.js` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/popper.min.js`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/bootstrap/js/tooltip.js` & `django-outbox-menu-1.0.9/menu/static/vendor/bootstrap/js/tooltip.js`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/static/vendor/jquery/jquery-3.2.1.min.js` & `django-outbox-menu-1.0.9/menu/static/vendor/jquery/jquery-3.2.1.min.js`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/templates/index.html` & `django-outbox-menu-1.0.9/menu/templates/index.html`

 * *Files 8% similar despite different names*

```diff
@@ -13,39 +13,41 @@
     {% menu_create FRONTEND 0 as my_menu %}
 
     <ul>
     {% for i in my_menu %}
       <li>{{i}}</li>
     {% endfor %}
     </ul>
+    
+    {% comment %}
+        <hr>
+        DAFTAR AKTIF : (position company)
+        {% menu_active 8 as my_active %}
+        <ul>
+            <li>{{my_active}}</li>
+        </ul>   
+    {% endcomment %}
 
     <hr>
-    DAFTAR AKTIF : (position company)
-    {% menu_active 8 as my_active %}
-    <ul>
-        <li>{{my_active}}</li>
-    </ul>   
-
-    <hr>
-    DAFTAR AKTIF BY NAME : (position company)
-    {% menu_active_by_name 'Grand Son Of What ???' as my_active2 %}
+    DAFTAR AKTIF BY NAME : (position company profil)
+    {% menu_active_by_name 'company_profile' as my_active2 %}
     <ul>
         <li>{{my_active2}}</li>
     </ul>  
     
     {% comment %}
-    {% for i in my_active2 %}
-    <ul>
-        <li>{{i}}</li>
-    </ul>  
-    {% endfor %}
+        {% for i in my_active2 %}
+        <ul>
+            <li>{{i}}</li>
+        </ul>  
+        {% endfor %}
 
-    
-    <hr>
-    Bread Crumb : (position company)
-    {% menu_breadcrumb 'company' as my_active %}
-    <ul>
-        <li>{{my_active}}</li>
-    </ul>       
+        
+        <hr>
+        Bread Crumb : (position company profile)
+        {% menu_breadcrumb 'company_profile' as my_active %}
+        <ul>
+            <li>{{my_active}}</li>
+        </ul>       
     {% endcomment %}
   </body>
 </html>
```

#### html2text {}

```diff
@@ -1,20 +1,23 @@
  {% load menu_tags %}
 DAFTAR MENU :
 {% menu_create FRONTEND 0 as my_menu %}
     * {% for i in my_menu %}
     * {{i}}
     * {% endfor %}
+{% comment %}
 ===============================================================================
 DAFTAR AKTIF : (position company) {% menu_active 8 as my_active %}
     * {{my_active}}
+{% endcomment %}
 ===============================================================================
-DAFTAR AKTIF BY NAME : (position company) {% menu_active_by_name 'Grand Son Of
-What ???' as my_active2 %}
+DAFTAR AKTIF BY NAME : (position company profil) {% menu_active_by_name
+'company_profile' as my_active2 %}
     * {{my_active2}}
 {% comment %} {% for i in my_active2 %}
     * {{i}}
 {% endfor %}
 ===============================================================================
-Bread Crumb : (position company) {% menu_breadcrumb 'company' as my_active %}
+Bread Crumb : (position company profile) {% menu_breadcrumb 'company_profile'
+as my_active %}
     * {{my_active}}
 {% endcomment %}
```

### Comparing `django-outbox-menu-1.0.8/menu/templates/test-menu.html` & `django-outbox-menu-1.0.9/menu/templates/test-menu.html`

 * *Files identical despite different names*

### Comparing `django-outbox-menu-1.0.8/menu/templatetags/__pycache__/menu_tags.cpython-310.pyc` & `django-outbox-menu-1.0.9/menu/templatetags/__pycache__/menu_tags.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Fri Oct 28 21:58:55 2022 UTC, .py size: 5851 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 8% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 9f50 5c63 db16 0000  o........P\c....
+00000000: 6f0d 0d0a 0000 0000 782b 7c63 6019 0000  o.......x+|c`...
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 7a00 0000 6400  .....@...sz...d.
 00000030: 5a00 6401 6402 6c01 6d02 5a02 0100 6403  Z.d.d.l.m.Z...d.
 00000040: 6404 6c03 6d04 5a04 0100 6403 6405 6c05  d.l.m.Z...d.d.l.
 00000050: 6d06 5a06 0100 6502 a007 a100 5a08 6900  m.Z...e.....Z.i.
 00000060: 5a09 4700 6406 6407 8400 6407 6502 6a0a  Z.G.d.d...d.e.j.
 00000070: 8303 5a0b 6508 6a0c 6408 6409 8d01 640a  ..Z.e.j.d.d...d.
@@ -135,36 +135,70 @@
 00000860: 720c 0000 0072 0d00 0000 da0d 6765 745f  r....r......get_
 00000870: 6d65 6e75 5f6c 6973 746e 0000 0073 1600  menu_listn...s..
 00000880: 0000 0402 0201 1201 0801 0401 0480 0601  ................
 00000890: 0601 0402 0a01 0c02 7223 0000 0063 0100  ........r#...c..
 000008a0: 0000 0000 0000 0000 0000 0200 0000 0300  ................
 000008b0: 0000 4300 0000 731a 0000 0074 0064 0119  ..C...s....t.d..
 000008c0: 007d 017c 01a0 017c 00a1 0101 007c 01a0  .}.|...|.....|..
-000008d0: 02a1 0053 00a9 024e 7211 0000 0029 0372  ...S...Nr....).r
+000008d0: 02a1 0053 0029 024e 7211 0000 0029 0372  ...S.).Nr....).r
 000008e0: 1300 0000 5a0f 6765 745f 6163 7469 7665  ....Z.get_active
 000008f0: 5f6d 656e 755a 0f67 6574 5f6c 6973 745f  _menuZ.get_list_
 00000900: 6163 7469 7665 2902 5a0b 6163 7469 7665  active).Z.active
 00000910: 5f6d 656e 7572 1500 0000 720c 0000 0072  _menur....r....r
 00000920: 0c00 0000 720d 0000 00da 0b6d 656e 755f  ....r......menu_
 00000930: 6163 7469 7665 8700 0000 7306 0000 0008  active....s.....
-00000940: 020a 0108 0172 2500 0000 6301 0000 0000  .....r%...c.....
-00000950: 0000 0000 0000 0002 0000 0003 0000 0043  ...............C
-00000960: 0000 0073 1200 0000 7400 6401 1900 7d01  ...s....t.d...}.
-00000970: 7c01 a001 7c00 a101 5300 7224 0000 0029  |...|...S.r$...)
-00000980: 0272 1300 0000 5a17 6765 745f 6163 7469  .r....Z.get_acti
-00000990: 7665 5f6d 656e 755f 6279 5f6e 616d 6529  ve_menu_by_name)
-000009a0: 025a 1061 6374 6976 655f 6d65 6e75 5f6e  .Z.active_menu_n
-000009b0: 616d 6572 1500 0000 720c 0000 0072 0c00  amer....r....r..
-000009c0: 0000 720d 0000 00da 136d 656e 755f 6163  ..r......menu_ac
-000009d0: 7469 7665 5f62 795f 6e61 6d65 9c00 0000  tive_by_name....
-000009e0: 7304 0000 0008 020a 0172 2600 0000 4e29  s........r&...N)
-000009f0: 1172 1a00 0000 da06 646a 616e 676f 7202  .r......djangor.
-00000a00: 0000 00da 066d 6f64 656c 7372 0400 0000  .....modelsr....
-00000a10: 5a05 6d65 6e75 7372 0500 0000 da07 4c69  Z.menusr......Li
-00000a20: 6272 6172 79da 0872 6567 6973 7465 7272  brary..registerr
-00000a30: 1300 0000 da04 4e6f 6465 7206 0000 00da  ......Noder.....
-00000a40: 0374 6167 7223 0000 00da 0a73 696d 706c  .tagr#.....simpl
-00000a50: 655f 7461 6772 2500 0000 7226 0000 0072  e_tagr%...r&...r
-00000a60: 0c00 0000 720c 0000 0072 0c00 0000 720d  ....r....r....r.
-00000a70: 0000 00da 083c 6d6f 6475 6c65 3e01 0000  .....<module>...
-00000a80: 0073 1a00 0000 0400 0c11 0c01 0c01 0802  .s..............
-00000a90: 0405 1207 0a4c 0a01 0418 0a01 0414 0e01  .....L..........
+00000940: 020a 0108 0172 2400 0000 6301 0000 0000  .....r$...c.....
+00000950: 0000 0000 0000 0002 0000 0006 0000 0043  ...............C
+00000960: 0000 0073 1a00 0000 7400 6401 1900 7d01  ...s....t.d...}.
+00000970: 7c01 a001 7c00 a002 6402 6403 a102 a101  |...|...d.d.....
+00000980: 5300 2904 61f3 0100 000a 2020 2020 2020  S.).a.....      
+00000990: 2020 4a69 6b61 2061 6374 6976 655f 6d65    Jika active_me
+000009a0: 6e75 5f6e 616d 6520 6d65 6e67 616e 6475  nu_name mengandu
+000009b0: 6e67 2075 6e64 6572 7363 6f72 6520 285f  ng underscore (_
+000009c0: 290a 2020 2020 2020 2020 6d61 6b61 2075  ).        maka u
+000009d0: 6261 6820 6d65 6e6a 6164 6920 7370 6173  bah menjadi spas
+000009e0: 690a 2020 2020 2020 2020 6b61 7265 6e61  i.        karena
+000009f0: 2064 6920 7465 6d70 6c61 7465 206a 616e   di template jan
+00000a00: 676f 2074 6964 616b 2062 6973 6120 6d65  go tidak bisa me
+00000a10: 6e65 7269 6d61 2073 7061 7369 2075 6e74  nerima spasi unt
+00000a20: 756b 206b 6f6e 6469 7369 2069 6e69 0a0a  uk kondisi ini..
+00000a30: 2020 2020 2020 2020 7661 7220 6163 7469          var acti
+00000a40: 7665 5f6d 656e 7520 3d20 2763 6f6d 7061  ve_menu = 'compa
+00000a50: 6e79 206e 616d 6527 0a20 2020 2020 2020  ny name'.       
+00000a60: 207b 2520 6d65 6e75 5f62 7265 6164 6372   {% menu_breadcr
+00000a70: 756d 6220 6163 7469 7665 5f6d 656e 7520  umb active_menu 
+00000a80: 6173 206d 795f 6163 7469 7665 2025 7d0a  as my_active %}.
+00000a90: 2020 2020 2020 2020 7465 6d70 6c61 7465          template
+00000aa0: 2061 6b61 6e20 6572 726f 720a 2020 2020   akan error.    
+00000ab0: 2020 2020 6a61 6469 2073 6f6c 7573 696e      jadi solusin
+00000ac0: 7961 2075 6261 6820 3a0a 2020 2020 2020  ya ubah :.      
+00000ad0: 2020 7661 7220 6163 7469 7665 5f6d 656e    var active_men
+00000ae0: 7520 3d20 2763 6f6d 7061 6e79 5f6e 616d  u = 'company_nam
+00000af0: 6527 0a20 2020 2020 2020 2070 726f 7365  e'.        prose
+00000b00: 7320 6469 2064 616c 616d 2066 756e 6773  s di dalam fungs
+00000b10: 6920 696e 6920 7562 6168 2075 6e64 6572  i ini ubah under
+00000b20: 2073 636f 7265 206d 656e 6a61 6469 2073   score menjadi s
+00000b30: 7061 7369 0a20 2020 2020 2020 206b 656d  pasi.        kem
+00000b40: 7564 6961 6e20 6261 7275 2062 6973 6120  udian baru bisa 
+00000b50: 6469 2063 6f6d 7061 7265 2064 656e 6761  di compare denga
+00000b60: 6e20 6d65 6e75 2072 6561 6c2e 6c6f 7765  n menu real.lowe
+00000b70: 7263 6173 6528 290a 2020 2020 7211 0000  rcase().    r...
+00000b80: 00da 015f fa01 2029 0372 1300 0000 5a17  ..._.. ).r....Z.
+00000b90: 6765 745f 6163 7469 7665 5f6d 656e 755f  get_active_menu_
+00000ba0: 6279 5f6e 616d 65da 0772 6570 6c61 6365  by_name..replace
+00000bb0: 2902 5a10 6163 7469 7665 5f6d 656e 755f  ).Z.active_menu_
+00000bc0: 6e61 6d65 7215 0000 0072 0c00 0000 720c  namer....r....r.
+00000bd0: 0000 0072 0d00 0000 da13 6d65 6e75 5f61  ...r......menu_a
+00000be0: 6374 6976 655f 6279 5f6e 616d 659e 0000  ctive_by_name...
+00000bf0: 0073 0400 0000 0813 1201 7228 0000 004e  .s........r(...N
+00000c00: 2911 721a 0000 00da 0664 6a61 6e67 6f72  ).r......djangor
+00000c10: 0200 0000 da06 6d6f 6465 6c73 7204 0000  ......modelsr...
+00000c20: 005a 056d 656e 7573 7205 0000 00da 074c  .Z.menusr......L
+00000c30: 6962 7261 7279 da08 7265 6769 7374 6572  ibrary..register
+00000c40: 7213 0000 00da 044e 6f64 6572 0600 0000  r......Noder....
+00000c50: da03 7461 6772 2300 0000 da0a 7369 6d70  ..tagr#.....simp
+00000c60: 6c65 5f74 6167 7224 0000 0072 2800 0000  le_tagr$...r(...
+00000c70: 720c 0000 0072 0c00 0000 720c 0000 0072  r....r....r....r
+00000c80: 0d00 0000 da08 3c6d 6f64 756c 653e 0100  ......<module>..
+00000c90: 0000 731a 0000 0004 000c 110c 010c 0108  ..s.............
+00000ca0: 0204 0512 070a 4c0a 0104 180a 0104 160e  ......L.........
+00000cb0: 01                                       .
```

### Comparing `django-outbox-menu-1.0.8/menu/templatetags/menu_tags.py` & `django-outbox-menu-1.0.9/menu/templatetags/menu_tags.py`

 * *Files 6% similar despite different names*

```diff
@@ -149,12 +149,31 @@
 # OKE pakai simple tag untuk create bread crumb
 # @register.simple_tag
 # def menu_bread_crumb():
 #     my_menu = global_menu['0']
 #     print('bread  =', my_menu.create_breadCrumb('profile')    )
 #     return my_menu.create_breadCrumb('profile')    
 
+
+# UPDATE 22 Nop 2022
 @register.simple_tag    #(takes_context=True) context, 
 def menu_active_by_name(active_menu_name):    
+    '''
+        Jika active_menu_name mengandung underscore (_)
+        maka ubah menjadi spasi
+        karena di template jango tidak bisa menerima spasi untuk kondisi ini
+
+        var active_menu = 'company name'
+        {% menu_breadcrumb active_menu as my_active %}
+        template akan error
+        jadi solusinya ubah :
+        var active_menu = 'company_name'
+        proses di dalam fungsi ini ubah under score menjadi spasi
+        kemudian baru bisa di compare dengan menu real.lowercase()
+    '''
+
+    # Update 22 Nop 22 :
+    # tambahan .replace('_','')
+    # replace underscore dengan spasi
     my_menu = global_menu['0']  # harus tipe data string    
-    return my_menu.get_active_menu_by_name(active_menu_name)
+    return my_menu.get_active_menu_by_name(active_menu_name.replace('_',' '))
     # return my_menu.get_list_active()
```

### Comparing `django-outbox-menu-1.0.8/setup.py` & `django-outbox-menu-1.0.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -79,18 +79,17 @@
     # you can instead use the py_modules field instead.
     # EITHER py_modules OR packages should be present.
 
     # use array for exclude for better way to exclude package
     packages=find_packages(exclude=["tests","django_menu",]),
 
     # dependencies
-    # install_requires=[
-    #     'cryptography',
-    #     'python-decouple',
-    # ],
+    install_requires=[
+        'django-parler',        
+    ],
 
     # agar file manifest .in dieksekusi
     include_package_data = True,
 
     # The description that will be shown on PyPI.
     # Keep it short and concise
     # This field is OPTIONAL
```

