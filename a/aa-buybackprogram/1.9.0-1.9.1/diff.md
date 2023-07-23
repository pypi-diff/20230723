# Comparing `tmp/aa-buybackprogram-1.9.0.tar.gz` & `tmp/aa-buybackprogram-1.9.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aa-buybackprogram-1.9.0.tar", last modified: Mon Mar 27 13:30:07 2023, max compression
+gzip compressed data, was "aa-buybackprogram-1.9.1.tar", last modified: Wed Mar 29 15:38:31 2023, max compression
```

## Comparing `aa-buybackprogram-1.9.0.tar` & `aa-buybackprogram-1.9.1.tar`

### file list

```diff
@@ -1,100 +1,108 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.815886 aa-buybackprogram-1.9.0/
--rwxrwxrwx   0 root         (0) root         (0)     1070 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/LICENSE
--rwxrwxrwx   0 root         (0) root         (0)      195 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)    19555 2023-03-27 13:30:07.815886 aa-buybackprogram-1.9.0/PKG-INFO
--rwxr-xr-x   0 root         (0) root         (0)    18610 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.803886 aa-buybackprogram-1.9.0/aa_buybackprogram.egg-info/
--rw-r--r--   0 root         (0) root         (0)    19555 2023-03-27 13:30:07.000000 aa-buybackprogram-1.9.0/aa_buybackprogram.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     3567 2023-03-27 13:30:07.000000 aa-buybackprogram-1.9.0/aa_buybackprogram.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-03-27 13:30:07.000000 aa-buybackprogram-1.9.0/aa_buybackprogram.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       73 2023-03-27 13:30:07.000000 aa-buybackprogram-1.9.0/aa_buybackprogram.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       24 2023-03-27 13:30:07.000000 aa-buybackprogram-1.9.0/aa_buybackprogram.egg-info/top_level.txt
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.807886 aa-buybackprogram-1.9.0/buybackprogram/
--rwxr-xr-x   0 root         (0) root         (0)      117 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/__init__.py
--rwxr-xr-x   0 root         (0) root         (0)      965 2023-03-25 14:23:02.000000 aa-buybackprogram-1.9.0/buybackprogram/admin.py
--rwxr-xr-x   0 root         (0) root         (0)     1641 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/app_settings.py
--rwxrwxrwx   0 root         (0) root         (0)      168 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/apps.py
--rwxrwxrwx   0 root         (0) root         (0)      936 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/auth_hooks.py
--rwxrwxrwx   0 root         (0) root         (0)      553 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/constants.py
--rwxrwxrwx   0 root         (0) root         (0)      553 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/decorators.py
--rwxr-xr-x   0 root         (0) root         (0)     5699 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/forms.py
--rwxr-xr-x   0 root         (0) root         (0)    34979 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/helpers.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.807886 aa-buybackprogram-1.9.0/buybackprogram/management/
--rwxrwxrwx   0 root         (0) root         (0)        0 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/management/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.807886 aa-buybackprogram-1.9.0/buybackprogram/management/commands/
--rwxrwxrwx   0 root         (0) root         (0)      102 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/management/commands/__init__.py
--rwxr-xr-x   0 root         (0) root         (0)     3519 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/management/commands/buybackprogram_generate_test_data.py
--rwxr-xr-x   0 root         (0) root         (0)     2179 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/management/commands/buybackprogram_link_contracts.py
--rwxr-xr-x   0 root         (0) root         (0)     1849 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/management/commands/buybackprogram_load_data.py
--rwxrwxrwx   0 root         (0) root         (0)     3792 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/management/commands/buybackprogram_load_prices.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.811886 aa-buybackprogram-1.9.0/buybackprogram/migrations/
--rwxr-xr-x   0 root         (0) root         (0)    23557 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0001_initial.py
--rwxr-xr-x   0 root         (0) root         (0)     1112 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0002_contractnotification.py
--rwxr-xr-x   0 root         (0) root         (0)     1119 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0003_statics_performance_increase.py
--rwxr-xr-x   0 root         (0) root         (0)      709 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0004_auto_20220323_1331.py
--rwxr-xr-x   0 root         (0) root         (0)      744 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0005_program_compression_price_dencity_modifier.py
--rwxr-xr-x   0 root         (0) root         (0)     1334 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0006_program_bonds_npc_price_and_more.py
--rwxr-xr-x   0 root         (0) root         (0)      809 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0007_program_expiration.py
--rwxr-xr-x   0 root         (0) root         (0)     1763 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0008_alter_general_options_alter_program_refining_rate.py
--rw-r--r--   0 root         (0) root         (0)      442 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0009_contract_location_name.py
--rw-r--r--   0 root         (0) root         (0)      568 2023-03-27 13:28:24.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/0010_contract_no_tracking_alter_tracking_tracking_number.py
--rwxrwxrwx   0 root         (0) root         (0)        0 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/migrations/__init__.py
--rwxr-xr-x   0 root         (0) root         (0)    49417 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/models.py
--rwxr-xr-x   0 root         (0) root         (0)     5514 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/notes.py
--rwxr-xr-x   0 root         (0) root         (0)     6138 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/notification.py
--rwxrwxrwx   0 root         (0) root         (0)      386 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/providers.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.803886 aa-buybackprogram-1.9.0/buybackprogram/static/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.803886 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.811886 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/css/
--rwxr-xr-x   0 root         (0) root         (0)     4582 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/css/billboards_dark.css
--rwxr-xr-x   0 root         (0) root         (0)     4558 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/css/billboards_light.css
--rwxr-xr-x   0 root         (0) root         (0)    21820 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/css/style_dark.css
--rwxrwxrwx   0 root         (0) root         (0)    21655 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/css/style_light.css
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.811886 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/images/
--rwxr-xr-x   0 root         (0) root         (0)      761 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/images/help.png
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.811886 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/js/
--rwxrwxrwx   0 root         (0) root         (0)      412 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/js/autocomplete.js
--rwxrwxrwx   0 root         (0) root         (0)    37085 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/js/bootstrap-autocomplete.min.js
--rwxrwxrwx   0 root         (0) root         (0)   947196 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/swagger.json
--rwxr-xr-x   0 root         (0) root         (0)     7971 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/tasks.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.803886 aa-buybackprogram-1.9.0/buybackprogram/templates/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.811886 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/
--rwxrwxrwx   0 root         (0) root         (0)      802 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/base.html
--rwxr-xr-x   0 root         (0) root         (0)     6729 2022-11-06 18:09:14.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/contract_details.html
--rwxr-xr-x   0 root         (0) root         (0)     1218 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/faq.html
--rwxrwxrwx   0 root         (0) root         (0)     3099 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/index.html
--rwxr-xr-x   0 root         (0) root         (0)     2774 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/leaderboards.html
--rwxrwxrwx   0 root         (0) root         (0)     1753 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/location_add.html
--rwxrwxrwx   0 root         (0) root         (0)     2838 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/menu.html
--rwxrwxrwx   0 root         (0) root         (0)      171 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/page.html
--rwxr-xr-x   0 root         (0) root         (0)     7008 2023-03-18 13:02:24.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/performance.html
--rwxrwxrwx   0 root         (0) root         (0)      584 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_add.html
--rwxrwxrwx   0 root         (0) root         (0)    16302 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_calculate.html
--rwxrwxrwx   0 root         (0) root         (0)      861 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_edit.html
--rwxrwxrwx   0 root         (0) root         (0)     1180 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_edit_item.html
--rwxr-xr-x   0 root         (0) root         (0)     1188 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_edit_marketgroup.html
--rwxr-xr-x   0 root         (0) root         (0)     2748 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_special_taxes.html
--rwxr-xr-x   0 root         (0) root         (0)    11272 2023-03-27 13:28:24.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/stats.html
--rwxr-xr-x   0 root         (0) root         (0)      669 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/user_settings.html
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.811886 aa-buybackprogram-1.9.0/buybackprogram/templatetags/
--rwxrwxrwx   0 root         (0) root         (0)        0 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templatetags/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)      430 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/templatetags/price_formats.py
--rwxr-xr-x   0 root         (0) root         (0)     4618 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/templatetags/program_settings.py
--rwxrwxrwx   0 root         (0) root         (0)       62 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/tests.py
--rwxrwxrwx   0 root         (0) root         (0)     2765 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/urls.py
--rwxr-xr-x   0 root         (0) root         (0)     3885 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/utils.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.811886 aa-buybackprogram-1.9.0/buybackprogram/views/
--rwxrwxrwx   0 root         (0) root         (0)       29 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/buybackprogram/views/__init__.py
--rwxr-xr-x   0 root         (0) root         (0)     9148 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/views/calculate.py
--rwxr-xr-x   0 root         (0) root         (0)     5261 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/views/common.py
--rwxr-xr-x   0 root         (0) root         (0)     8622 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/views/programs.py
--rwxr-xr-x   0 root         (0) root         (0)     6579 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.0/buybackprogram/views/special_taxes.py
--rwxr-xr-x   0 root         (0) root         (0)    23046 2023-03-27 13:28:24.000000 aa-buybackprogram-1.9.0/buybackprogram/views/stats.py
--rwxr-xr-x   0 root         (0) root         (0)      187 2023-03-27 13:30:07.815886 aa-buybackprogram-1.9.0/setup.cfg
--rwxr-xr-x   0 root         (0) root         (0)     1645 2022-11-06 18:25:26.000000 aa-buybackprogram-1.9.0/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-27 13:30:07.815886 aa-buybackprogram-1.9.0/testauth/
--rwxrwxrwx   0 root         (0) root         (0)       46 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/testauth/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)      612 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/testauth/celery.py
--rwxr-xr-x   0 root         (0) root         (0)     9935 2023-03-25 14:23:02.000000 aa-buybackprogram-1.9.0/testauth/settings.py
--rwxr-xr-x   0 root         (0) root         (0)      174 2023-03-25 14:23:02.000000 aa-buybackprogram-1.9.0/testauth/urls.py
--rwxrwxrwx   0 root         (0) root         (0)      397 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.0/testauth/wsgi.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.013009 aa-buybackprogram-1.9.1/
+-rwxrwxrwx   0 root         (0) root         (0)     1070 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/LICENSE
+-rwxrwxrwx   0 root         (0) root         (0)      195 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/MANIFEST.in
+-rw-r--r--   0 root         (0) root         (0)    19555 2023-03-29 15:38:31.013009 aa-buybackprogram-1.9.1/PKG-INFO
+-rwxr-xr-x   0 root         (0) root         (0)    18610 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.005009 aa-buybackprogram-1.9.1/aa_buybackprogram.egg-info/
+-rw-r--r--   0 root         (0) root         (0)    19555 2023-03-29 15:38:30.000000 aa-buybackprogram-1.9.1/aa_buybackprogram.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     3836 2023-03-29 15:38:31.000000 aa-buybackprogram-1.9.1/aa_buybackprogram.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-03-29 15:38:30.000000 aa-buybackprogram-1.9.1/aa_buybackprogram.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       75 2023-03-29 15:38:30.000000 aa-buybackprogram-1.9.1/aa_buybackprogram.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       24 2023-03-29 15:38:30.000000 aa-buybackprogram-1.9.1/aa_buybackprogram.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/
+-rwxr-xr-x   0 root         (0) root         (0)      117 2023-03-29 15:14:47.000000 aa-buybackprogram-1.9.1/buybackprogram/__init__.py
+-rwxr-xr-x   0 root         (0) root         (0)      965 2023-03-25 14:23:02.000000 aa-buybackprogram-1.9.1/buybackprogram/admin.py
+-rwxr-xr-x   0 root         (0) root         (0)     1641 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/app_settings.py
+-rwxrwxrwx   0 root         (0) root         (0)      168 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/apps.py
+-rwxrwxrwx   0 root         (0) root         (0)      936 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/auth_hooks.py
+-rwxrwxrwx   0 root         (0) root         (0)      553 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/constants.py
+-rwxrwxrwx   0 root         (0) root         (0)      553 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/decorators.py
+-rwxr-xr-x   0 root         (0) root         (0)     5699 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/forms.py
+-rwxr-xr-x   0 root         (0) root         (0)    35039 2023-03-29 15:14:47.000000 aa-buybackprogram-1.9.1/buybackprogram/helpers.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/management/
+-rwxrwxrwx   0 root         (0) root         (0)        0 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/management/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/management/commands/
+-rwxrwxrwx   0 root         (0) root         (0)      102 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/management/commands/__init__.py
+-rwxr-xr-x   0 root         (0) root         (0)     3519 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/management/commands/buybackprogram_generate_test_data.py
+-rwxr-xr-x   0 root         (0) root         (0)     2179 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/management/commands/buybackprogram_link_contracts.py
+-rwxr-xr-x   0 root         (0) root         (0)     1849 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/management/commands/buybackprogram_load_data.py
+-rwxrwxrwx   0 root         (0) root         (0)     3792 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/management/commands/buybackprogram_load_prices.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/migrations/
+-rwxr-xr-x   0 root         (0) root         (0)    23557 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0001_initial.py
+-rwxr-xr-x   0 root         (0) root         (0)     1112 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0002_contractnotification.py
+-rwxr-xr-x   0 root         (0) root         (0)     1119 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0003_statics_performance_increase.py
+-rwxr-xr-x   0 root         (0) root         (0)      709 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0004_auto_20220323_1331.py
+-rwxr-xr-x   0 root         (0) root         (0)      744 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0005_program_compression_price_dencity_modifier.py
+-rwxr-xr-x   0 root         (0) root         (0)     1334 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0006_program_bonds_npc_price_and_more.py
+-rwxr-xr-x   0 root         (0) root         (0)      809 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0007_program_expiration.py
+-rwxr-xr-x   0 root         (0) root         (0)     1763 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0008_alter_general_options_alter_program_refining_rate.py
+-rw-r--r--   0 root         (0) root         (0)      442 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0009_contract_location_name.py
+-rw-r--r--   0 root         (0) root         (0)      568 2023-03-27 13:28:24.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/0010_contract_no_tracking_alter_tracking_tracking_number.py
+-rwxrwxrwx   0 root         (0) root         (0)        0 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/migrations/__init__.py
+-rwxr-xr-x   0 root         (0) root         (0)    48918 2023-03-29 14:56:21.000000 aa-buybackprogram-1.9.1/buybackprogram/models.py
+-rwxr-xr-x   0 root         (0) root         (0)     5514 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/notes.py
+-rwxr-xr-x   0 root         (0) root         (0)     6138 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/notification.py
+-rwxrwxrwx   0 root         (0) root         (0)      386 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/providers.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.005009 aa-buybackprogram-1.9.1/buybackprogram/static/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.005009 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/css/
+-rwxr-xr-x   0 root         (0) root         (0)     4582 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/css/billboards_dark.css
+-rwxr-xr-x   0 root         (0) root         (0)     4558 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/css/billboards_light.css
+-rwxr-xr-x   0 root         (0) root         (0)    21820 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/css/style_dark.css
+-rwxrwxrwx   0 root         (0) root         (0)    21655 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/css/style_light.css
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/images/
+-rwxr-xr-x   0 root         (0) root         (0)      761 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/images/help.png
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/js/
+-rwxrwxrwx   0 root         (0) root         (0)      412 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/js/autocomplete.js
+-rwxrwxrwx   0 root         (0) root         (0)    37085 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/js/bootstrap-autocomplete.min.js
+-rwxrwxrwx   0 root         (0) root         (0)   947196 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/swagger.json
+-rwxr-xr-x   0 root         (0) root         (0)     7971 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/tasks.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.005009 aa-buybackprogram-1.9.1/buybackprogram/templates/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/
+-rwxrwxrwx   0 root         (0) root         (0)      802 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/base.html
+-rwxr-xr-x   0 root         (0) root         (0)     6729 2022-11-06 18:09:14.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/contract_details.html
+-rwxr-xr-x   0 root         (0) root         (0)     1218 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/faq.html
+-rwxrwxrwx   0 root         (0) root         (0)     3099 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/index.html
+-rwxr-xr-x   0 root         (0) root         (0)     2774 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/leaderboards.html
+-rwxrwxrwx   0 root         (0) root         (0)     1753 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/location_add.html
+-rwxrwxrwx   0 root         (0) root         (0)     2838 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/menu.html
+-rwxrwxrwx   0 root         (0) root         (0)      171 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/page.html
+-rwxr-xr-x   0 root         (0) root         (0)     7008 2023-03-18 13:02:24.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/performance.html
+-rwxrwxrwx   0 root         (0) root         (0)      584 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_add.html
+-rwxrwxrwx   0 root         (0) root         (0)    16302 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_calculate.html
+-rwxrwxrwx   0 root         (0) root         (0)      861 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_edit.html
+-rwxrwxrwx   0 root         (0) root         (0)     1180 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_edit_item.html
+-rwxr-xr-x   0 root         (0) root         (0)     1188 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_edit_marketgroup.html
+-rwxr-xr-x   0 root         (0) root         (0)     2748 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_special_taxes.html
+-rwxr-xr-x   0 root         (0) root         (0)    11272 2023-03-27 13:28:24.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/stats.html
+-rwxr-xr-x   0 root         (0) root         (0)      669 2022-11-06 17:12:51.000000 aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/user_settings.html
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/templatetags/
+-rwxrwxrwx   0 root         (0) root         (0)        0 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templatetags/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      430 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/templatetags/price_formats.py
+-rwxr-xr-x   0 root         (0) root         (0)     4618 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/templatetags/program_settings.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.009009 aa-buybackprogram-1.9.1/buybackprogram/tests/
+-rwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 14:56:21.000000 aa-buybackprogram-1.9.1/buybackprogram/tests/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      924 2023-03-29 15:14:47.000000 aa-buybackprogram-1.9.1/buybackprogram/tests/test_helpers.py
+-rw-r--r--   0 root         (0) root         (0)    10700 2023-03-29 14:56:21.000000 aa-buybackprogram-1.9.1/buybackprogram/tests/test_models.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.013009 aa-buybackprogram-1.9.1/buybackprogram/tests/testdata/
+-rw-r--r--   0 root         (0) root         (0)      267 2023-03-29 14:56:21.000000 aa-buybackprogram-1.9.1/buybackprogram/tests/testdata/__init__.py
+-rw-r--r--   0 root         (0) root         (0)      757 2023-03-29 14:56:21.000000 aa-buybackprogram-1.9.1/buybackprogram/tests/testdata/create_eveuniverse.py
+-rw-r--r--   0 root         (0) root         (0)     9166 2023-03-29 14:56:21.000000 aa-buybackprogram-1.9.1/buybackprogram/tests/testdata/factories.py
+-rw-r--r--   0 root         (0) root         (0)      412 2023-03-29 14:56:21.000000 aa-buybackprogram-1.9.1/buybackprogram/tests/testdata/load_eveuniverse.py
+-rwxrwxrwx   0 root         (0) root         (0)     2765 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/urls.py
+-rwxr-xr-x   0 root         (0) root         (0)     3885 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/utils.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.013009 aa-buybackprogram-1.9.1/buybackprogram/views/
+-rwxrwxrwx   0 root         (0) root         (0)       29 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/buybackprogram/views/__init__.py
+-rwxr-xr-x   0 root         (0) root         (0)     9148 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/views/calculate.py
+-rwxr-xr-x   0 root         (0) root         (0)     5261 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/views/common.py
+-rwxr-xr-x   0 root         (0) root         (0)     8622 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/views/programs.py
+-rwxr-xr-x   0 root         (0) root         (0)     6579 2023-03-27 13:16:33.000000 aa-buybackprogram-1.9.1/buybackprogram/views/special_taxes.py
+-rwxr-xr-x   0 root         (0) root         (0)    23046 2023-03-27 13:28:24.000000 aa-buybackprogram-1.9.1/buybackprogram/views/stats.py
+-rwxr-xr-x   0 root         (0) root         (0)      187 2023-03-29 15:38:31.013009 aa-buybackprogram-1.9.1/setup.cfg
+-rwxr-xr-x   0 root         (0) root         (0)     1647 2023-03-29 14:56:21.000000 aa-buybackprogram-1.9.1/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-03-29 15:38:31.013009 aa-buybackprogram-1.9.1/testauth/
+-rwxrwxrwx   0 root         (0) root         (0)       46 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/testauth/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      612 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/testauth/celery.py
+-rwxr-xr-x   0 root         (0) root         (0)    10041 2023-03-29 14:56:21.000000 aa-buybackprogram-1.9.1/testauth/settings.py
+-rwxr-xr-x   0 root         (0) root         (0)      174 2023-03-25 14:23:02.000000 aa-buybackprogram-1.9.1/testauth/urls.py
+-rwxrwxrwx   0 root         (0) root         (0)      397 2022-11-06 14:22:31.000000 aa-buybackprogram-1.9.1/testauth/wsgi.py
```

### Comparing `aa-buybackprogram-1.9.0/LICENSE` & `aa-buybackprogram-1.9.1/LICENSE`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/PKG-INFO` & `aa-buybackprogram-1.9.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aa-buybackprogram
-Version: 1.9.0
+Version: 1.9.1
 Summary: Buyback program plugin app for Alliance Auth
 Home-page: https://gitlab.com/paulipa/allianceauth-buyback-program
 Author: Ikarus Cesaille
 Author-email: contact@eve-linknet.com
 License: MIT
 Classifier: Environment :: Web Environment
 Classifier: Framework :: Django
```

### Comparing `aa-buybackprogram-1.9.0/README.md` & `aa-buybackprogram-1.9.1/README.md`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/aa_buybackprogram.egg-info/PKG-INFO` & `aa-buybackprogram-1.9.1/aa_buybackprogram.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aa-buybackprogram
-Version: 1.9.0
+Version: 1.9.1
 Summary: Buyback program plugin app for Alliance Auth
 Home-page: https://gitlab.com/paulipa/allianceauth-buyback-program
 Author: Ikarus Cesaille
 Author-email: contact@eve-linknet.com
 License: MIT
 Classifier: Environment :: Web Environment
 Classifier: Framework :: Django
```

### Comparing `aa-buybackprogram-1.9.0/aa_buybackprogram.egg-info/SOURCES.txt` & `aa-buybackprogram-1.9.1/aa_buybackprogram.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -19,15 +19,14 @@
 buybackprogram/helpers.py
 buybackprogram/models.py
 buybackprogram/notes.py
 buybackprogram/notification.py
 buybackprogram/providers.py
 buybackprogram/swagger.json
 buybackprogram/tasks.py
-buybackprogram/tests.py
 buybackprogram/urls.py
 buybackprogram/utils.py
 buybackprogram/management/__init__.py
 buybackprogram/management/commands/__init__.py
 buybackprogram/management/commands/buybackprogram_generate_test_data.py
 buybackprogram/management/commands/buybackprogram_link_contracts.py
 buybackprogram/management/commands/buybackprogram_load_data.py
@@ -66,14 +65,21 @@
 buybackprogram/templates/buybackprogram/program_edit_marketgroup.html
 buybackprogram/templates/buybackprogram/program_special_taxes.html
 buybackprogram/templates/buybackprogram/stats.html
 buybackprogram/templates/buybackprogram/user_settings.html
 buybackprogram/templatetags/__init__.py
 buybackprogram/templatetags/price_formats.py
 buybackprogram/templatetags/program_settings.py
+buybackprogram/tests/__init__.py
+buybackprogram/tests/test_helpers.py
+buybackprogram/tests/test_models.py
+buybackprogram/tests/testdata/__init__.py
+buybackprogram/tests/testdata/create_eveuniverse.py
+buybackprogram/tests/testdata/factories.py
+buybackprogram/tests/testdata/load_eveuniverse.py
 buybackprogram/views/__init__.py
 buybackprogram/views/calculate.py
 buybackprogram/views/common.py
 buybackprogram/views/programs.py
 buybackprogram/views/special_taxes.py
 buybackprogram/views/stats.py
 testauth/__init__.py
```

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/admin.py` & `aa-buybackprogram-1.9.1/buybackprogram/admin.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/app_settings.py` & `aa-buybackprogram-1.9.1/buybackprogram/app_settings.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/auth_hooks.py` & `aa-buybackprogram-1.9.1/buybackprogram/auth_hooks.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/constants.py` & `aa-buybackprogram-1.9.1/buybackprogram/constants.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/decorators.py` & `aa-buybackprogram-1.9.1/buybackprogram/decorators.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/forms.py` & `aa-buybackprogram-1.9.1/buybackprogram/forms.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/helpers.py` & `aa-buybackprogram-1.9.1/buybackprogram/helpers.py`

 * *Files 1% similar despite different names*

```diff
@@ -991,15 +991,18 @@
 
     return values
 
 
 def get_tracking_number(
     user, program, form_donation, buyback_data, contract_price_data
 ):
-    last_id = Tracking.objects.last().id
+    try:
+        last_id = Tracking.objects.last().id
+    except AttributeError:
+        last_id = 0
 
     tracking_number = (
         BUYBACKPROGRAM_TRACKING_PREFILL
         + "-"
         + str(last_id)
         + "-"
         + uuid.uuid4().hex[:6].upper()
```

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/management/commands/buybackprogram_generate_test_data.py` & `aa-buybackprogram-1.9.1/buybackprogram/management/commands/buybackprogram_generate_test_data.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/management/commands/buybackprogram_link_contracts.py` & `aa-buybackprogram-1.9.1/buybackprogram/management/commands/buybackprogram_link_contracts.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/management/commands/buybackprogram_load_data.py` & `aa-buybackprogram-1.9.1/buybackprogram/management/commands/buybackprogram_load_data.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/management/commands/buybackprogram_load_prices.py` & `aa-buybackprogram-1.9.1/buybackprogram/management/commands/buybackprogram_load_prices.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/migrations/0001_initial.py` & `aa-buybackprogram-1.9.1/buybackprogram/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/migrations/0002_contractnotification.py` & `aa-buybackprogram-1.9.1/buybackprogram/migrations/0002_contractnotification.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/migrations/0003_statics_performance_increase.py` & `aa-buybackprogram-1.9.1/buybackprogram/migrations/0003_statics_performance_increase.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/migrations/0004_auto_20220323_1331.py` & `aa-buybackprogram-1.9.1/buybackprogram/migrations/0004_auto_20220323_1331.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/migrations/0005_program_compression_price_dencity_modifier.py` & `aa-buybackprogram-1.9.1/buybackprogram/migrations/0005_program_compression_price_dencity_modifier.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/migrations/0006_program_bonds_npc_price_and_more.py` & `aa-buybackprogram-1.9.1/buybackprogram/migrations/0006_program_bonds_npc_price_and_more.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/migrations/0007_program_expiration.py` & `aa-buybackprogram-1.9.1/buybackprogram/migrations/0007_program_expiration.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/migrations/0008_alter_general_options_alter_program_refining_rate.py` & `aa-buybackprogram-1.9.1/buybackprogram/migrations/0008_alter_general_options_alter_program_refining_rate.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/migrations/0010_contract_no_tracking_alter_tracking_tracking_number.py` & `aa-buybackprogram-1.9.1/buybackprogram/migrations/0010_contract_no_tracking_alter_tracking_tracking_number.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/models.py` & `aa-buybackprogram-1.9.1/buybackprogram/models.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 
 from django.contrib.auth.models import Group, User
 from django.contrib.humanize.templatetags.humanize import intcomma
 from django.core.exceptions import ValidationError
 from django.core.validators import MaxValueValidator, MinValueValidator
 from django.db import Error, models
 from django.utils.translation import gettext as _
-from esi.clients import EsiClientProvider
 from esi.errors import TokenExpiredError, TokenInvalidError
 from esi.models import Token
 from eveuniverse.models import EveEntity, EveSolarSystem, EveType
 
 from allianceauth.authentication.models import CharacterOwnership, State
 
 # Create your models here.
@@ -302,19 +301,15 @@
                 logger.debug("Got corporations for contract owner: %s" % corporations)
 
                 objs = []
 
                 # Prepare objects for bulk create
                 for item in contract_items:
                     cont = Contract.objects.get(contract_id=contract["contract_id"])
-                    try:
-                        itm = EveType.objects.get(pk=item["type_id"])
-                    except EveType.DoesNotExist:
-                        itm = EveType.objects.get_or_create(id=item["type_id"])
-                        itm = EveType.objects.get(pk=item["type_id"])
+                    itm, _ = EveType.objects.get_or_create_esi(id=item["type_id"])
 
                     contract_item = ContractItem(
                         contract=cont,
                         eve_type=itm,
                         quantity=item["quantity"],
                     )
 
@@ -588,20 +583,15 @@
                 )
 
                 objs = []
 
                 # Prepare objects for bulk create
                 for item in contract_items:
                     cont = Contract.objects.get(contract_id=contract["contract_id"])
-
-                    try:
-                        itm = EveType.objects.get(pk=item["type_id"])
-                    except EveType.DoesNotExist:
-                        itm = EveType.objects.get_or_create(id=item["type_id"])
-                        itm = EveType.objects.get(pk=item["type_id"])
+                    itm, _ = EveType.objects.get_or_create_esi(id=item["type_id"])
 
                     contract_item = ContractItem(
                         contract=cont,
                         eve_type=itm,
                         quantity=item["quantity"],
                     )
 
@@ -643,15 +633,14 @@
                 logger.debug(
                     "No changes to the status of contract %s, update completed"
                     % obj.contract_id
                 )
 
     @fetch_token_for_owner(["esi-universe.read_structures.v1"])
     def _get_location_name(self, token, structid) -> list:
-        esi = EsiClientProvider()
         status = fetch_esi_status()
 
         if not status.is_online or status.error_limit_remain < 5:
             return "Unknown"
         if structid <= 100000000:  # likely to be NPC station
             return EveEntity.objects.resolve_name(structid)
```

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/notes.py` & `aa-buybackprogram-1.9.1/buybackprogram/notes.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/notification.py` & `aa-buybackprogram-1.9.1/buybackprogram/notification.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/css/billboards_dark.css` & `aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/css/billboards_dark.css`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/css/billboards_light.css` & `aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/css/billboards_light.css`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/css/style_dark.css` & `aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/css/style_dark.css`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/css/style_light.css` & `aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/css/style_light.css`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/images/help.png` & `aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/images/help.png`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/static/buybackprogram/js/bootstrap-autocomplete.min.js` & `aa-buybackprogram-1.9.1/buybackprogram/static/buybackprogram/js/bootstrap-autocomplete.min.js`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/swagger.json` & `aa-buybackprogram-1.9.1/buybackprogram/swagger.json`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/tasks.py` & `aa-buybackprogram-1.9.1/buybackprogram/tasks.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/base.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/base.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/contract_details.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/contract_details.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/faq.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/faq.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/index.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/index.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/leaderboards.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/leaderboards.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/location_add.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/location_add.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/menu.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/menu.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/performance.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/performance.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_add.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_add.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_calculate.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_calculate.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_edit.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_edit.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_edit_item.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_edit_item.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_edit_marketgroup.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_edit_marketgroup.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/program_special_taxes.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/program_special_taxes.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/stats.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/stats.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templates/buybackprogram/user_settings.html` & `aa-buybackprogram-1.9.1/buybackprogram/templates/buybackprogram/user_settings.html`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/templatetags/program_settings.py` & `aa-buybackprogram-1.9.1/buybackprogram/templatetags/program_settings.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/urls.py` & `aa-buybackprogram-1.9.1/buybackprogram/urls.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/utils.py` & `aa-buybackprogram-1.9.1/buybackprogram/utils.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/views/calculate.py` & `aa-buybackprogram-1.9.1/buybackprogram/views/calculate.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/views/common.py` & `aa-buybackprogram-1.9.1/buybackprogram/views/common.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/views/programs.py` & `aa-buybackprogram-1.9.1/buybackprogram/views/programs.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/views/special_taxes.py` & `aa-buybackprogram-1.9.1/buybackprogram/views/special_taxes.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/buybackprogram/views/stats.py` & `aa-buybackprogram-1.9.1/buybackprogram/views/stats.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/setup.py` & `aa-buybackprogram-1.9.1/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -39,10 +39,10 @@
         "Topic :: Internet :: WWW/HTTP",
         "Topic :: Internet :: WWW/HTTP :: Dynamic Content",
     ],
     python_requires="~=3.8",
     install_requires=[
         "allianceauth>=3.0",
         "django-eveuniverse>=0.8.2",
-        "allianceauth-app-utils>=1.14",
+        "allianceauth-app-utils>=1.17.1",
     ],
 )
```

### Comparing `aa-buybackprogram-1.9.0/testauth/celery.py` & `aa-buybackprogram-1.9.1/testauth/celery.py`

 * *Files identical despite different names*

### Comparing `aa-buybackprogram-1.9.0/testauth/settings.py` & `aa-buybackprogram-1.9.1/testauth/settings.py`

 * *Files 2% similar despite different names*

```diff
@@ -300,10 +300,14 @@
 EMAIL_HOST = ""
 EMAIL_PORT = 587
 EMAIL_HOST_USER = ""
 EMAIL_HOST_PASSWORD = ""
 EMAIL_USE_TLS = True
 DEFAULT_FROM_EMAIL = ""
 
+DEFAULT_AUTO_FIELD = "django.db.models.AutoField"
+
 #######################################
 # Add any custom settings below here. #
 #######################################
+
+STATICFILES_DIRS = []  # needed to suppress a warning
```

