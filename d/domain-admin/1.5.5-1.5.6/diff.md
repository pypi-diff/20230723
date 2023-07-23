# Comparing `tmp/domain-admin-1.5.5.tar.gz` & `tmp/domain-admin-1.5.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "domain-admin-1.5.5.tar", last modified: Sat Jul 22 09:42:08 2023, max compression
+gzip compressed data, was "domain-admin-1.5.6.tar", last modified: Sun Jul 23 14:37:36 2023, max compression
```

## Comparing `domain-admin-1.5.5.tar` & `domain-admin-1.5.6.tar`

### file list

```diff
@@ -1,444 +1,457 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.242355 domain-admin-1.5.5/
--rw-r--r--   0 runner    (1001) docker     (123)     1081 2023-07-22 09:41:54.000000 domain-admin-1.5.5/LICENSE
--rwxr-xr-x   0 runner    (1001) docker     (123)      417 2023-07-22 09:41:54.000000 domain-admin-1.5.5/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)    18454 2023-07-22 09:42:08.242355 domain-admin-1.5.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    17012 2023-07-22 09:41:54.000000 domain-admin-1.5.5/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.194354 domain-admin-1.5.5/domain_admin/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.198354 domain-admin-1.5.5/domain_admin/api/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5324 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/address_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      664 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/auth_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      964 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/cert_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    17243 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/domain_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    16941 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/domain_info_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     6361 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/group_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     4235 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/group_user_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      387 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/ip_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1243 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/log_async_task_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1152 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/log_operation_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1112 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/log_scheduler_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     6461 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/notify_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1796 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/prometheus_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2433 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/system_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     5805 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/user_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      582 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/api/whois_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      809 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/compat.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.198354 domain-admin-1.5.5/domain_admin/config/
--rw-r--r--   0 runner    (1001) docker     (123)      288 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      771 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/config/default_config.py
--rw-r--r--   0 runner    (1001) docker     (123)      782 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/config/env_config.py
--rw-r--r--   0 runner    (1001) docker     (123)     1026 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/config/runtime_config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.198354 domain-admin-1.5.5/domain_admin/enums/
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/enums/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      915 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/enums/config_key_enum.py
--rw-r--r--   0 runner    (1001) docker     (123)      348 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/enums/event_enum.py
--rw-r--r--   0 runner    (1001) docker     (123)      452 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/enums/notify_type_enum.py
--rw-r--r--   0 runner    (1001) docker     (123)      684 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/enums/operation_enum.py
--rw-r--r--   0 runner    (1001) docker     (123)      303 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/enums/role_enum.py
--rw-r--r--   0 runner    (1001) docker     (123)      345 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/enums/status_enum.py
--rw-r--r--   0 runner    (1001) docker     (123)     2607 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/enums/version_enum.py
--rw-r--r--   0 runner    (1001) docker     (123)      784 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/log.py
--rw-r--r--   0 runner    (1001) docker     (123)     2703 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/main.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.202355 domain-admin-1.5.5/domain_admin/migrate/
--rw-r--r--   0 runner    (1001) docker     (123)       79 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      704 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_102_to_103.py
--rw-r--r--   0 runner    (1001) docker     (123)     1087 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_106_to_110.py
--rw-r--r--   0 runner    (1001) docker     (123)      977 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_110_to_1212.py
--rw-r--r--   0 runner    (1001) docker     (123)     1013 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_1212_to_1213.py
--rw-r--r--   0 runner    (1001) docker     (123)      884 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_1213_to_131.py
--rw-r--r--   0 runner    (1001) docker     (123)      955 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_136_to_140_alpha.py
--rw-r--r--   0 runner    (1001) docker     (123)     2504 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_140_alpha_to_140.py
--rw-r--r--   0 runner    (1001) docker     (123)      962 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_1413_to_1414.py
--rw-r--r--   0 runner    (1001) docker     (123)      729 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_1422_to_1423.py
--rw-r--r--   0 runner    (1001) docker     (123)     1404 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_143_to_144.py
--rw-r--r--   0 runner    (1001) docker     (123)      980 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_145_to_146.py
--rw-r--r--   0 runner    (1001) docker     (123)     1217 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_151_to_152.py
--rw-r--r--   0 runner    (1001) docker     (123)      804 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_154_to_155.py
--rw-r--r--   0 runner    (1001) docker     (123)     1349 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/migrate/migrate_common.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.202355 domain-admin-1.5.5/domain_admin/model/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2049 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/address_model.py
--rw-r--r--   0 runner    (1001) docker     (123)      768 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/base_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     1716 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/database.py
--rw-r--r--   0 runner    (1001) docker     (123)     2942 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/domain_info_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     3786 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/domain_model.py
--rw-r--r--   0 runner    (1001) docker     (123)      633 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/group_model.py
--rw-r--r--   0 runner    (1001) docker     (123)      908 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/group_user_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/log_async_task_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     1198 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/log_operation_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     1122 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/log_scheduler_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     3377 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/notify_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     3753 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/system_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     1236 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/user_model.py
--rw-r--r--   0 runner    (1001) docker     (123)      595 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/model/version_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.202355 domain-admin-1.5.5/domain_admin/public/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/FETCH_HEAD
--rw-r--r--   0 runner    (1001) docker     (123)       21 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/HEAD
--rw-r--r--   0 runner    (1001) docker     (123)      420 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/config
--rwxr-xr-x   0 runner    (1001) docker     (123)       73 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/description
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/hooks/
--rwxr-xr-x   0 runner    (1001) docker     (123)      478 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/applypatch-msg.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      896 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/commit-msg.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     4726 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/fsmonitor-watchman.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      189 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/post-update.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      424 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-applypatch.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     1643 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-commit.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      416 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-merge-commit.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     1374 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-push.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     4898 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-rebase.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      544 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-receive.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     1492 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/prepare-commit-msg.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     2783 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/push-to-checkout.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     2308 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/sendemail-validate.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     3650 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/hooks/update.sample
--rw-r--r--   0 runner    (1001) docker     (123)     3638 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/index
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/info/
--rwxr-xr-x   0 runner    (1001) docker     (123)      240 2023-07-22 09:42:05.000000 domain-admin-1.5.5/domain_admin/public/.git/info/exclude
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/logs/
--rw-r--r--   0 runner    (1001) docker     (123)      217 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/logs/HEAD
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.186354 domain-admin-1.5.5/domain_admin/public/.git/logs/refs/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/logs/refs/heads/
--rw-r--r--   0 runner    (1001) docker     (123)      226 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/logs/refs/heads/dist
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.186354 domain-admin-1.5.5/domain_admin/public/.git/logs/refs/remotes/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/logs/refs/remotes/origin/
--rw-r--r--   0 runner    (1001) docker     (123)      347 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/logs/refs/remotes/origin/dist
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.190354 domain-admin-1.5.5/domain_admin/public/.git/objects/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/objects/19/
--r--r--r--   0 runner    (1001) docker     (123)    64350 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/19/7f5cf73cf11d43d915904e0d8aad4736a77d63
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/objects/21/
--r--r--r--   0 runner    (1001) docker     (123)       61 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/21/00bd7d2219a26827cc80aa37fe72fcb303bb50
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/objects/24/
--r--r--r--   0 runner    (1001) docker     (123)     2691 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/24/103afc71807fa9124dac4bacf6c71aea125714
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/objects/3c/
--r--r--r--   0 runner    (1001) docker     (123)     3081 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/3c/0f2e923566dc74d04e67d46d8b722923ed1949
--r--r--r--   0 runner    (1001) docker     (123)   148706 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/3c/2434ab20d756f0a95ad24f6a5adb7e1219a7d1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/objects/40/
--r--r--r--   0 runner    (1001) docker     (123)      279 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/40/c3b0a033be485b3c7e9d536a1b3a277818cb82
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.206354 domain-admin-1.5.5/domain_admin/public/.git/objects/46/
--r--r--r--   0 runner    (1001) docker     (123)      636 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/46/3ce0aa01de3b64fe18ece210e1570817c51008
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/51/
--r--r--r--   0 runner    (1001) docker     (123)     5816 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/51/ec8afb4a5571f29776853cff34b9084b989be8
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/52/
--r--r--r--   0 runner    (1001) docker     (123)    62564 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/52/c1926de72b181c9b7faf597fb8f71f48565462
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/55/
--r--r--r--   0 runner    (1001) docker     (123)      119 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/55/1103b11c4b699a3b4107d3a2ab173dfe238556
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/58/
--r--r--r--   0 runner    (1001) docker     (123)     7634 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/58/0919cf9322c635814fe723901eff5bc75ae450
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/5d/
--r--r--r--   0 runner    (1001) docker     (123)      464 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/5d/c222fd0913296f5d22a6d502848bc46e27cfbb
--r--r--r--   0 runner    (1001) docker     (123)     3441 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/5d/c54416f168ceb328978b483f7568ef176ab9ea
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/5f/
--r--r--r--   0 runner    (1001) docker     (123)      530 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/5f/a7faf700c98850aa96022ab07af6a07b854f34
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/69/
--r--r--r--   0 runner    (1001) docker     (123)   279936 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/69/a9dda41cf39bb60d1dc5b1158ffba197580b6a
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/6c/
--r--r--r--   0 runner    (1001) docker     (123)      155 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/6c/3e3059f9ec00c015681abca34b751c3439513d
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/6d/
--r--r--r--   0 runner    (1001) docker     (123)      612 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/6d/15191314c9b832ac41056a30bf0bf6533a29dc
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/6e/
--r--r--r--   0 runner    (1001) docker     (123)     6012 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/6e/25fd629c25bce876fa6e3d55f3d44ffc7403df
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/6f/
--r--r--r--   0 runner    (1001) docker     (123)     1815 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/6f/931c679b6da636cbb9ae74fbb156ec8588aacd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/76/
--r--r--r--   0 runner    (1001) docker     (123)      228 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/76/a77330292710a039cca1dabd8301893a8e5c20
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/79/
--r--r--r--   0 runner    (1001) docker     (123)   105817 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/79/404c2464172f80b414d111f49718327b3ef93b
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/7c/
--r--r--r--   0 runner    (1001) docker     (123)      473 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/7c/ffb379a2e31f7ecbc681d3e6a2988313d68c14
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/7f/
--r--r--r--   0 runner    (1001) docker     (123)      368 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/7f/64d8af0501887e805dc9ccf8228f4fb5e73fdb
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/83/
--r--r--r--   0 runner    (1001) docker     (123)      693 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/83/52bc71914e2d52dc5b8b5f432baed8fdb3a5b3
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/89/
--r--r--r--   0 runner    (1001) docker     (123)      106 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/89/0f3ed83973272c63b56a722a88fe25160d11d2
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/8c/
--r--r--r--   0 runner    (1001) docker     (123)       69 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/8c/f880f5a9481ef71cd22e08d59e7d366775b360
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/92/
--r--r--r--   0 runner    (1001) docker     (123)      200 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/92/cfface0a460c51331fb8f25083a09948e00cbf
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/95/
--r--r--r--   0 runner    (1001) docker     (123)      118 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/95/f07af46d709638b20c0b2c66cdf6de8e89a7e4
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/99/
--r--r--r--   0 runner    (1001) docker     (123)     1435 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/99/3174c206a21af6cacdc5834848444e2e5e20f4
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/aa/
--r--r--r--   0 runner    (1001) docker     (123)      220 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/aa/fb811a89caf497ae4598dda6ada91378dc70d3
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/b2/
--r--r--r--   0 runner    (1001) docker     (123)      957 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/b2/09e1e91fe0262794771b8d69d85d8d6bcab9f6
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.210354 domain-admin-1.5.5/domain_admin/public/.git/objects/b3/
--r--r--r--   0 runner    (1001) docker     (123)    41902 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/b3/1cb2667f48424e34cf9517362eadf899f704ad
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/c4/
--r--r--r--   0 runner    (1001) docker     (123)       61 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/c4/c46ae2c464a49661d7793709077759039f0b5e
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/c9/
--r--r--r--   0 runner    (1001) docker     (123)     4310 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/c9/55b903bc1c5de030fc58f36fd2ebf22ff6ac6d
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/cc/
--r--r--r--   0 runner    (1001) docker     (123)   361458 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/cc/bfeaa0b21986ed309cbb83d17585b54f3b2fb9
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/d3/
--r--r--r--   0 runner    (1001) docker     (123)     1700 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/d3/8d6c402e90bd375d028a0c70d3091cb2779e39
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/dc/
--r--r--r--   0 runner    (1001) docker     (123)     8843 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/dc/8bf2242bff0c8ee207b31910dda7a0463858df
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/e1/
--r--r--r--   0 runner    (1001) docker     (123)    23927 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/e1/13bfd922675ce50e68cdf88cd94d16130ad58b
--r--r--r--   0 runner    (1001) docker     (123)    11675 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/e1/f93ffe54644c9baa5e1bc6b9711a08bfba7750
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/e4/
--r--r--r--   0 runner    (1001) docker     (123)     1736 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/e4/56acd4f47f8661930733f5db393527f36e631b
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/ef/
--r--r--r--   0 runner    (1001) docker     (123)     1896 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/ef/6235d671af0b6113d18b3e63a1fa2fe30ea9bd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/f0/
--r--r--r--   0 runner    (1001) docker     (123)    17226 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/f0/5cb009efc03174da02974c45dfeac8fb5486ff
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/fa/
--r--r--r--   0 runner    (1001) docker     (123)     1024 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/fa/21601143ca66f766b9a994751adc37796b2455
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/fd/
--r--r--r--   0 runner    (1001) docker     (123)     5204 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/fd/bd32c675f85af4ed57021ac0638a21a3c6cad3
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/objects/ff/
--r--r--r--   0 runner    (1001) docker     (123)    13943 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/objects/ff/9c65dfdc7a16150c07745e0030a9d6373920cd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.190354 domain-admin-1.5.5/domain_admin/public/.git/refs/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/refs/heads/
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/refs/heads/dist
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.190354 domain-admin-1.5.5/domain_admin/public/.git/refs/remotes/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/.git/refs/remotes/origin/
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/refs/remotes/origin/dist
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/.git/shallow
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/css/
--rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/css/ConditionFilterGroup.a91875e6.css
--rw-r--r--   0 runner    (1001) docker     (123)      301 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/css/index.302e10d7.css
--rw-r--r--   0 runner    (1001) docker     (123)   331526 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/css/index.69a97337.css
--rw-r--r--   0 runner    (1001) docker     (123)      117 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/css/index.a676cc2e.css
--rw-r--r--   0 runner    (1001) docker     (123)      250 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/css/index.b285e10a.css
--rw-r--r--   0 runner    (1001) docker     (123)      117 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/css/index.cf805e1c.css
--rw-r--r--   0 runner    (1001) docker     (123)       45 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/css/index.d028ae37.css
--rwxr-xr-x   0 runner    (1001) docker     (123)    15406 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/favicon.ico
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/gif/
--rw-r--r--   0 runner    (1001) docker     (123)     6334 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/gif/user-avatar.ea67286d.gif
--rw-r--r--   0 runner    (1001) docker     (123)      911 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/index.html
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.214355 domain-admin-1.5.5/domain_admin/public/jpg/
--rw-r--r--   0 runner    (1001) docker     (123)    14271 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/jpg/chatpet-white.10f4f36c.jpg
--rw-r--r--   0 runner    (1001) docker     (123)    24940 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/jpg/chatpet.fce5580e.jpg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.222355 domain-admin-1.5.5/domain_admin/public/js/
--rw-r--r--   0 runner    (1001) docker     (123)    18591 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/ConditionFilterGroup.cc953e5c.js
--rw-r--r--   0 runner    (1001) docker     (123)      953 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/ConnectStatus.b87d1fee.js
--rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/SearchUser.1ba54ef6.js
--rw-r--r--   0 runner    (1001) docker     (123)     1257 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/SelectGroup.0ff8c614.js
--rw-r--r--   0 runner    (1001) docker     (123)   390997 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/codemirror-lib.a3a39aa0.js
--rw-r--r--   0 runner    (1001) docker     (123)   195335 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/element-icon.1ce1c350.js
--rw-r--r--   0 runner    (1001) docker     (123)   749914 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/element-plus.30eb1cab.js
--rw-r--r--   0 runner    (1001) docker     (123)      579 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/event-enums.6c6f25e7.js
--rw-r--r--   0 runner    (1001) docker     (123)  1058329 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/highlight-lib.3654f6d3.js
--rw-r--r--   0 runner    (1001) docker     (123)     9652 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.0a173b97.js
--rw-r--r--   0 runner    (1001) docker     (123)    10061 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.2a4ae78d.js
--rw-r--r--   0 runner    (1001) docker     (123)    28081 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.2d5be753.js
--rw-r--r--   0 runner    (1001) docker     (123)     4147 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.51ecb744.js
--rw-r--r--   0 runner    (1001) docker     (123)    21499 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.53934399.js
--rw-r--r--   0 runner    (1001) docker     (123)     4248 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.58c30995.js
--rw-r--r--   0 runner    (1001) docker     (123)    64152 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.5c0e1ecd.js
--rw-r--r--   0 runner    (1001) docker     (123)    28958 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.7089425b.js
--rw-r--r--   0 runner    (1001) docker     (123)     2691 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.87e9fadd.js
--rw-r--r--   0 runner    (1001) docker     (123)    39363 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.a747af4a.js
--rw-r--r--   0 runner    (1001) docker     (123)     8982 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.b77111ba.js
--rw-r--r--   0 runner    (1001) docker     (123)     5241 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.d21190a6.js
--rw-r--r--   0 runner    (1001) docker     (123)     1818 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.df8aa1f7.js
--rw-r--r--   0 runner    (1001) docker     (123)     4603 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/index.edfe11bc.js
--rw-r--r--   0 runner    (1001) docker     (123)   312580 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/vendor-lib.76301fc3.js
--rw-r--r--   0 runner    (1001) docker     (123)    94202 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/js/vendor-vue.9e61e0af.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.222355 domain-admin-1.5.5/domain_admin/public/m/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.222355 domain-admin-1.5.5/domain_admin/public/m/.git/
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/FETCH_HEAD
--rw-r--r--   0 runner    (1001) docker     (123)       21 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/HEAD
--rw-r--r--   0 runner    (1001) docker     (123)      421 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/config
--rwxr-xr-x   0 runner    (1001) docker     (123)       73 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/description
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/
--rwxr-xr-x   0 runner    (1001) docker     (123)      478 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/applypatch-msg.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      896 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/commit-msg.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     4726 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/fsmonitor-watchman.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      189 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/post-update.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      424 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-applypatch.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     1643 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-commit.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      416 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-merge-commit.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     1374 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-push.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     4898 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-rebase.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)      544 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-receive.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     1492 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/prepare-commit-msg.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     2783 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/push-to-checkout.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     2308 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/sendemail-validate.sample
--rwxr-xr-x   0 runner    (1001) docker     (123)     3650 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/hooks/update.sample
--rw-r--r--   0 runner    (1001) docker     (123)     2073 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/index
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/info/
--rwxr-xr-x   0 runner    (1001) docker     (123)      240 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/m/.git/info/exclude
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/logs/
--rw-r--r--   0 runner    (1001) docker     (123)      217 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/logs/HEAD
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.190354 domain-admin-1.5.5/domain_admin/public/m/.git/logs/refs/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/logs/refs/heads/
--rw-r--r--   0 runner    (1001) docker     (123)      226 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/logs/refs/heads/dist
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.190354 domain-admin-1.5.5/domain_admin/public/m/.git/logs/refs/remotes/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/logs/refs/remotes/origin/
--rw-r--r--   0 runner    (1001) docker     (123)      347 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/logs/refs/remotes/origin/dist
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.190354 domain-admin-1.5.5/domain_admin/public/m/.git/objects/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/2d/
--r--r--r--   0 runner    (1001) docker     (123)      814 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/2d/7cec3e00ed3b3b835eb233ae4bb2ea21fb5a0b
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/43/
--r--r--r--   0 runner    (1001) docker     (123)     1262 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/43/c4fcdf29fe10c6256aa4e9cf00f534e6933efc
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/4b/
--r--r--r--   0 runner    (1001) docker     (123)     5351 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/4b/63cfa29bd94b198d895f7a64e10c20f167e65b
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/5c/
--r--r--r--   0 runner    (1001) docker     (123)       60 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/5c/98d16331bcc99b0cbbe89a3ffb23e3f5918ff2
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/61/
--r--r--r--   0 runner    (1001) docker     (123)      421 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/61/05f9fd4f4b11812fcca0d2e0704e4c8dd6e7a3
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/62/
--r--r--r--   0 runner    (1001) docker     (123)      222 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/62/59838c4de171bc95a934ee2384d626eeb3040a
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/67/
--r--r--r--   0 runner    (1001) docker     (123)      478 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/67/d2a69f1213016d777c02e0c99a38871d07da5b
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/6f/
--r--r--r--   0 runner    (1001) docker     (123)      725 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/6f/9d23d38fd97c94c1dccf971fd7b7636cc075d2
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/71/
--r--r--r--   0 runner    (1001) docker     (123)     2231 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/71/4dbccc412b153f5044c269745126581e3cf373
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/7a/
--r--r--r--   0 runner    (1001) docker     (123)     2494 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/7a/694f3c8aca1586dc6f0e6e9e2773e207992329
--r--r--r--   0 runner    (1001) docker     (123)      968 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/7a/c4cdd0b7c56c8fe9f98aaf044df58bef26b7a5
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/8e/
--r--r--r--   0 runner    (1001) docker     (123)     2655 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/8e/ff5bef00cd2492d9b806988ea99996d636c126
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/93/
--r--r--r--   0 runner    (1001) docker     (123)     1108 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/93/85587145f9afbabe2aa1a489d24fd1f489e5c6
--r--r--r--   0 runner    (1001) docker     (123)     4673 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/93/db3989e7874cd6b75bc0e984690ffa16666ea6
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.226355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/98/
--r--r--r--   0 runner    (1001) docker     (123)     5141 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/98/1e059e0de4604a5dec80930d8ff7cdf84e0006
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/a9/
--r--r--r--   0 runner    (1001) docker     (123)     1110 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/a9/a1035a25ce05f60741e3f70716a18d93322203
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/b0/
--r--r--r--   0 runner    (1001) docker     (123)     1821 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/b0/ecf609c3df960010b6f7877bc379ea45d1e9da
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/c2/
--r--r--r--   0 runner    (1001) docker     (123)      505 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/c2/c748e84bc4d5118b0e33d6e0073e315a36d034
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/c7/
--r--r--r--   0 runner    (1001) docker     (123)    31300 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/c7/ef9b19427f9af9e445bb5d63231ccd58ef5b28
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/c8/
--r--r--r--   0 runner    (1001) docker     (123)   143922 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/c8/bec3f3e9b26642a8221c20a5e422bc2cada687
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/d9/
--r--r--r--   0 runner    (1001) docker     (123)      119 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/d9/d9ca2809d6994fef91c1ee2d22bc7a54b8b4a5
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/ed/
--r--r--r--   0 runner    (1001) docker     (123)      979 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/ed/50570bc6865f7dff2468d49072d7f4e4cb81d4
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/f0/
--r--r--r--   0 runner    (1001) docker     (123)      755 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/f0/a3f5a57d6bdb9961c3a56f4a992a08a0ecd671
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/f8/
--r--r--r--   0 runner    (1001) docker     (123)     1082 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/f8/0169320ed23edd9889e4de7631267635bfec27
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/objects/fd/
--r--r--r--   0 runner    (1001) docker     (123)     5204 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/objects/fd/bd32c675f85af4ed57021ac0638a21a3c6cad3
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.194354 domain-admin-1.5.5/domain_admin/public/m/.git/refs/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/refs/heads/
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/refs/heads/dist
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.194354 domain-admin-1.5.5/domain_admin/public/m/.git/refs/remotes/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.230355 domain-admin-1.5.5/domain_admin/public/m/.git/refs/remotes/origin/
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/refs/remotes/origin/dist
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/.git/shallow
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.234355 domain-admin-1.5.5/domain_admin/public/m/assets/
--rw-r--r--   0 runner    (1001) docker     (123)     1334 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/common-c7dd5d89.css
--rw-r--r--   0 runner    (1001) docker     (123)     3913 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/common.6194c42f.js
--rw-r--r--   0 runner    (1001) docker     (123)     8065 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index-5eda257b.css
--rw-r--r--   0 runner    (1001) docker     (123)     3782 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index-958ae3a0.css
--rw-r--r--   0 runner    (1001) docker     (123)   379599 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index-9c365a03.js
--rw-r--r--   0 runner    (1001) docker     (123)     2798 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index-ad047368.css
--rw-r--r--   0 runner    (1001) docker     (123)     5447 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index-e8224928.css
--rw-r--r--   0 runner    (1001) docker     (123)    53115 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index-f79acb3d.css
--rw-r--r--   0 runner    (1001) docker     (123)     2028 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index.1a0d1182.js
--rw-r--r--   0 runner    (1001) docker     (123)     1512 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index.1d067866.js
--rw-r--r--   0 runner    (1001) docker     (123)    10416 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index.daaf9893.js
--rw-r--r--   0 runner    (1001) docker     (123)     5355 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/index.feef7c0f.js
--rw-r--r--   0 runner    (1001) docker     (123)     4262 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/login-cb9f43ad.css
--rw-r--r--   0 runner    (1001) docker     (123)     1959 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/pages-cert-list-cert-list.e9ecbf65.js
--rw-r--r--   0 runner    (1001) docker     (123)     2016 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/pages-domain-list-domain-list.da5e6454.js
--rw-r--r--   0 runner    (1001) docker     (123)    10670 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/pages-login-login.09426b90.js
--rw-r--r--   0 runner    (1001) docker     (123)    12225 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/pages-user-index-user-index.d8efba8c.js
--rw-r--r--   0 runner    (1001) docker     (123)     1146 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/uni.06dd3c8e.css
--rw-r--r--   0 runner    (1001) docker     (123)     9118 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/assets/user-index-be7005ab.css
--rw-r--r--   0 runner    (1001) docker     (123)      835 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/index.html
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.234355 domain-admin-1.5.5/domain_admin/public/m/static/
--rwxr-xr-x   0 runner    (1001) docker     (123)     6334 2023-07-22 09:42:07.000000 domain-admin-1.5.5/domain_admin/public/m/static/user-avatar.gif
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.234355 domain-admin-1.5.5/domain_admin/public/svg/
--rw-r--r--   0 runner    (1001) docker     (123)     1478 2023-07-22 09:42:06.000000 domain-admin-1.5.5/domain_admin/public/svg/logo.184a2d7d.svg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.234355 domain-admin-1.5.5/domain_admin/router/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/router/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7412 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/router/api_map.py
--rw-r--r--   0 runner    (1001) docker     (123)     1529 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/router/permission.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.234355 domain-admin-1.5.5/domain_admin/service/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2424 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/async_task_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     1523 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/auth_service.py
--rw-r--r--   0 runner    (1001) docker     (123)      698 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/common_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     7393 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/domain_info_service.py
--rw-r--r--   0 runner    (1001) docker     (123)    12015 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/domain_service.py
--rw-r--r--   0 runner    (1001) docker     (123)      900 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/file_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     2560 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/group_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     1131 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/group_user_service.py
--rw-r--r--   0 runner    (1001) docker     (123)    11701 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/notify_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     2647 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/operation_service.py
--rw-r--r--   0 runner    (1001) docker     (123)      465 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/render_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     2764 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/scheduler_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     2061 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/system_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     1566 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/token_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     8731 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/service/version_service.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.238355 domain-admin-1.5.5/domain_admin/templates/
--rw-r--r--   0 runner    (1001) docker     (123)     3990 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/templates/cert-email.html
--rw-r--r--   0 runner    (1001) docker     (123)      276 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/templates/cert-export.csv
--rw-r--r--   0 runner    (1001) docker     (123)     2764 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/templates/domain-email.html
--rw-r--r--   0 runner    (1001) docker     (123)      392 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/templates/domain-export.csv
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.238355 domain-admin-1.5.5/domain_admin/utils/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      764 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/bcrypt_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.238355 domain-admin-1.5.5/domain_admin/utils/cert_util/
--rw-r--r--   0 runner    (1001) docker     (123)      508 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/cert_util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4695 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/cert_util/cert_common.py
--rw-r--r--   0 runner    (1001) docker     (123)      338 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/cert_util/cert_consts.py
--rw-r--r--   0 runner    (1001) docker     (123)      288 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/cert_util/cert_info.py
--rw-r--r--   0 runner    (1001) docker     (123)     2505 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/cert_util/cert_openssl_v2.py
--rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/cert_util/cert_socket.py
--rw-r--r--   0 runner    (1001) docker     (123)     2679 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/cert_util/cert_socket_v2.py
--rw-r--r--   0 runner    (1001) docker     (123)     3908 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/datetime_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     4690 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/domain_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     2201 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/email_util.py
--rw-r--r--   0 runner    (1001) docker     (123)      424 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/file_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.242355 domain-admin-1.5.5/domain_admin/utils/flask_ext/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      764 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/api_result.py
--rw-r--r--   0 runner    (1001) docker     (123)      877 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/app_exception.py
--rw-r--r--   0 runner    (1001) docker     (123)     1587 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/flask_app.py
--rw-r--r--   0 runner    (1001) docker     (123)     1133 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/handler.py
--rw-r--r--   0 runner    (1001) docker     (123)      392 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/http_code_enum.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.242355 domain-admin-1.5.5/domain_admin/utils/flask_ext/json/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/json/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/json/default.py
--rw-r--r--   0 runner    (1001) docker     (123)      569 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/json/json_encoder.py
--rw-r--r--   0 runner    (1001) docker     (123)      590 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/json/json_provider.py
--rw-r--r--   0 runner    (1001) docker     (123)      283 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/register.py
--rw-r--r--   0 runner    (1001) docker     (123)      314 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/flask_ext/request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2823 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/icp_util.py
--rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/ip_util.py
--rw-r--r--   0 runner    (1001) docker     (123)      862 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/json_util.py
--rw-r--r--   0 runner    (1001) docker     (123)      325 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/md5_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.242355 domain-admin-1.5.5/domain_admin/utils/open_api/
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/open_api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      850 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/open_api/crtsh_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1329 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/open_api/ding_talk_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1403 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/open_api/feishu_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1443 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/open_api/work_weixin_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.242355 domain-admin-1.5.5/domain_admin/utils/peewee_ext/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/peewee_ext/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1316 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/peewee_ext/model_util.py
--rw-r--r--   0 runner    (1001) docker     (123)      707 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/secret_util.py
--rw-r--r--   0 runner    (1001) docker     (123)      596 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/text_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     1061 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/time_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.242355 domain-admin-1.5.5/domain_admin/utils/whois_util/
--rw-r--r--   0 runner    (1001) docker     (123)      205 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/whois_util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2954 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/whois_util/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     1983 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/whois_util/util.py
--rw-r--r--   0 runner    (1001) docker     (123)    25912 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/whois_util/whois-servers.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5862 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/utils/whois_util/whois_util.py
--rwxr-xr-x   0 runner    (1001) docker     (123)      236 2023-07-22 09:41:54.000000 domain-admin-1.5.5/domain_admin/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.194354 domain-admin-1.5.5/domain_admin.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    18454 2023-07-22 09:42:08.000000 domain-admin-1.5.5/domain_admin.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    15688 2023-07-22 09:42:08.000000 domain-admin-1.5.5/domain_admin.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 09:42:08.000000 domain-admin-1.5.5/domain_admin.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      164 2023-07-22 09:42:08.000000 domain-admin-1.5.5/domain_admin.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-07-22 09:42:08.000000 domain-admin-1.5.5/domain_admin.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 09:42:08.000000 domain-admin-1.5.5/domain_admin.egg-info/zip-safe
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:42:08.242355 domain-admin-1.5.5/requirements/
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-07-22 09:41:54.000000 domain-admin-1.5.5/requirements/production.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 09:42:08.242355 domain-admin-1.5.5/setup.cfg
--rwxr-xr-x   0 runner    (1001) docker     (123)     3190 2023-07-22 09:41:54.000000 domain-admin-1.5.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.916354 domain-admin-1.5.6/
+-rw-r--r--   0 runner    (1001) docker     (123)     1081 2023-07-23 14:37:24.000000 domain-admin-1.5.6/LICENSE
+-rwxr-xr-x   0 runner    (1001) docker     (123)      417 2023-07-23 14:37:24.000000 domain-admin-1.5.6/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)    18454 2023-07-23 14:37:36.916354 domain-admin-1.5.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    17012 2023-07-23 14:37:24.000000 domain-admin-1.5.6/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.864354 domain-admin-1.5.6/domain_admin/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.868353 domain-admin-1.5.6/domain_admin/api/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5324 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/address_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      664 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/auth_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      964 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/cert_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17243 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/domain_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16941 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/domain_info_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6361 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/group_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4235 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/group_user_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      387 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/ip_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2710 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/issue_certificate_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1243 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/log_async_task_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1152 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/log_operation_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1112 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/log_scheduler_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6461 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/notify_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1796 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/prometheus_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2433 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/system_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5805 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/user_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      582 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/api/whois_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      809 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/compat.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.868353 domain-admin-1.5.6/domain_admin/config/
+-rw-r--r--   0 runner    (1001) docker     (123)      288 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      771 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/config/default_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      782 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/config/env_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1099 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/config/runtime_config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.868353 domain-admin-1.5.6/domain_admin/enums/
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/enums/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      915 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/enums/config_key_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)      348 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/enums/event_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)      452 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/enums/notify_type_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)      684 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/enums/operation_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)      303 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/enums/role_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)      345 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/enums/status_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2607 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/enums/version_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)      784 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/log.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2703 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/main.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.872353 domain-admin-1.5.6/domain_admin/migrate/
+-rw-r--r--   0 runner    (1001) docker     (123)       79 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      704 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_102_to_103.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1087 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_106_to_110.py
+-rw-r--r--   0 runner    (1001) docker     (123)      977 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_110_to_1212.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1013 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_1212_to_1213.py
+-rw-r--r--   0 runner    (1001) docker     (123)      884 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_1213_to_131.py
+-rw-r--r--   0 runner    (1001) docker     (123)      955 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_136_to_140_alpha.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2504 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_140_alpha_to_140.py
+-rw-r--r--   0 runner    (1001) docker     (123)      962 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_1413_to_1414.py
+-rw-r--r--   0 runner    (1001) docker     (123)      729 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_1422_to_1423.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1404 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_143_to_144.py
+-rw-r--r--   0 runner    (1001) docker     (123)      980 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_145_to_146.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1217 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_151_to_152.py
+-rw-r--r--   0 runner    (1001) docker     (123)      804 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_154_to_155.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1349 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/migrate/migrate_common.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.872353 domain-admin-1.5.6/domain_admin/model/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2049 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/address_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)      768 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/base_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1806 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/database.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2942 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/domain_info_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3786 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/domain_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)      633 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/group_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)      908 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/group_user_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2434 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/issue_certificate_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/log_async_task_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1198 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/log_operation_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1122 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/log_scheduler_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3377 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/notify_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3753 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/system_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1236 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/user_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)      595 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/model/version_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.872353 domain-admin-1.5.6/domain_admin/public/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/FETCH_HEAD
+-rw-r--r--   0 runner    (1001) docker     (123)       21 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/HEAD
+-rw-r--r--   0 runner    (1001) docker     (123)      420 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/config
+-rwxr-xr-x   0 runner    (1001) docker     (123)       73 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/description
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/hooks/
+-rwxr-xr-x   0 runner    (1001) docker     (123)      478 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/applypatch-msg.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      896 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/commit-msg.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4726 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/fsmonitor-watchman.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      189 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/post-update.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      424 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-applypatch.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1643 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-commit.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      416 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-merge-commit.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1374 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-push.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4898 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-rebase.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      544 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-receive.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1492 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/prepare-commit-msg.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2783 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/push-to-checkout.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2308 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/sendemail-validate.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     3650 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/hooks/update.sample
+-rw-r--r--   0 runner    (1001) docker     (123)     3814 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/index
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/info/
+-rwxr-xr-x   0 runner    (1001) docker     (123)      240 2023-07-23 14:37:33.000000 domain-admin-1.5.6/domain_admin/public/.git/info/exclude
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/logs/
+-rw-r--r--   0 runner    (1001) docker     (123)      172 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/logs/HEAD
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.856353 domain-admin-1.5.6/domain_admin/public/.git/logs/refs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/logs/refs/heads/
+-rw-r--r--   0 runner    (1001) docker     (123)      181 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/logs/refs/heads/dist
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.856353 domain-admin-1.5.6/domain_admin/public/.git/logs/refs/remotes/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/logs/refs/remotes/origin/
+-rw-r--r--   0 runner    (1001) docker     (123)      302 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/logs/refs/remotes/origin/dist
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.860353 domain-admin-1.5.6/domain_admin/public/.git/objects/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/objects/01/
+-r--r--r--   0 runner    (1001) docker     (123)     1738 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/01/9bb44cfca57b7aa35ea7f5b6f99c3ef48e8d8f
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/objects/19/
+-r--r--r--   0 runner    (1001) docker     (123)    64350 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/19/7f5cf73cf11d43d915904e0d8aad4736a77d63
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/objects/1e/
+-r--r--r--   0 runner    (1001) docker     (123)      984 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/1e/270d8f3cc5167242582434675642b5858ba482
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/objects/21/
+-r--r--r--   0 runner    (1001) docker     (123)       61 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/21/00bd7d2219a26827cc80aa37fe72fcb303bb50
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.876354 domain-admin-1.5.6/domain_admin/public/.git/objects/30/
+-r--r--r--   0 runner    (1001) docker     (123)     7634 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/30/0478ea1f19f5a14d6a7167e9f71f5848707d76
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/3c/
+-r--r--r--   0 runner    (1001) docker     (123)     3081 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/3c/0f2e923566dc74d04e67d46d8b722923ed1949
+-r--r--r--   0 runner    (1001) docker     (123)   148706 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/3c/2434ab20d756f0a95ad24f6a5adb7e1219a7d1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/40/
+-r--r--r--   0 runner    (1001) docker     (123)      637 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/40/03c2e07280d146ee3443587c38ea2d264c07ca
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/50/
+-r--r--r--   0 runner    (1001) docker     (123)     1895 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/50/c771a9bca6f87a2fb3381719fe0622eeae23bf
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/52/
+-r--r--r--   0 runner    (1001) docker     (123)    62564 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/52/c1926de72b181c9b7faf597fb8f71f48565462
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/53/
+-r--r--r--   0 runner    (1001) docker     (123)      221 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/53/0864cbe282ec11e8564a8a3ce33756977d59ee
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/55/
+-r--r--r--   0 runner    (1001) docker     (123)      119 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/55/1103b11c4b699a3b4107d3a2ab173dfe238556
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/58/
+-r--r--r--   0 runner    (1001) docker     (123)    11674 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/58/1d5e80145e76e2ba0d08b038e1a2fefebef3bb
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/5f/
+-r--r--r--   0 runner    (1001) docker     (123)      530 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/5f/a7faf700c98850aa96022ab07af6a07b854f34
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/69/
+-r--r--r--   0 runner    (1001) docker     (123)   279936 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/69/a9dda41cf39bb60d1dc5b1158ffba197580b6a
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/6c/
+-r--r--r--   0 runner    (1001) docker     (123)      155 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/6c/3e3059f9ec00c015681abca34b751c3439513d
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/6d/
+-r--r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/6d/15191314c9b832ac41056a30bf0bf6533a29dc
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/77/
+-r--r--r--   0 runner    (1001) docker     (123)     1436 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/77/bb86f804268cc8045d2cd2547ec17c22a0d166
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/79/
+-r--r--r--   0 runner    (1001) docker     (123)   105817 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/79/404c2464172f80b414d111f49718327b3ef93b
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/7f/
+-r--r--r--   0 runner    (1001) docker     (123)      368 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/7f/64d8af0501887e805dc9ccf8228f4fb5e73fdb
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/89/
+-r--r--r--   0 runner    (1001) docker     (123)      106 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/89/0f3ed83973272c63b56a722a88fe25160d11d2
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/8c/
+-r--r--r--   0 runner    (1001) docker     (123)       69 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/8c/f880f5a9481ef71cd22e08d59e7d366775b360
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/90/
+-r--r--r--   0 runner    (1001) docker     (123)     2691 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/90/4a4570929957b2678d3c499a9cd83658a6675e
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/91/
+-r--r--r--   0 runner    (1001) docker     (123)      310 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/91/dcfad5270425be228e01a34e9c9b11ef3a0c4e
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/92/
+-r--r--r--   0 runner    (1001) docker     (123)      200 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/92/cfface0a460c51331fb8f25083a09948e00cbf
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/93/
+-r--r--r--   0 runner    (1001) docker     (123)     8844 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/93/522d98a7fe61eb676e55f33d92d8d090b967e4
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/95/
+-r--r--r--   0 runner    (1001) docker     (123)      118 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/95/f07af46d709638b20c0b2c66cdf6de8e89a7e4
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/a0/
+-r--r--r--   0 runner    (1001) docker     (123)     1814 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/a0/e9b4ee6e91d304066df26b1bc6218de181c2c2
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/a2/
+-r--r--r--   0 runner    (1001) docker     (123)    17343 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/a2/86b0b36b3538d177580f0c25e8e3a3a9f007b7
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.880354 domain-admin-1.5.6/domain_admin/public/.git/objects/ab/
+-r--r--r--   0 runner    (1001) docker     (123)     1701 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/ab/2ba13bd2bd0cbf3e5b764ff0a29fd5872380c5
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/b1/
+-r--r--r--   0 runner    (1001) docker     (123)     6011 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/b1/115cb42fa8938fe1dbebccc9584aa03a895df0
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/b3/
+-r--r--r--   0 runner    (1001) docker     (123)    41902 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/b3/1cb2667f48424e34cf9517362eadf899f704ad
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/bb/
+-r--r--r--   0 runner    (1001) docker     (123)      474 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/bb/ecd10fc84228b6f4a1c2e0c90e2b68d4aa6bf2
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/c0/
+-r--r--r--   0 runner    (1001) docker     (123)      100 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/c0/76a86e24db79ccf75f79903b19cf145419d4bf
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/c1/
+-r--r--r--   0 runner    (1001) docker     (123)      694 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/c1/ff198374b288725eab95bc1294e1f04fe5c561
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/c4/
+-r--r--r--   0 runner    (1001) docker     (123)       61 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/c4/c46ae2c464a49661d7793709077759039f0b5e
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/cc/
+-r--r--r--   0 runner    (1001) docker     (123)   361458 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/cc/bfeaa0b21986ed309cbb83d17585b54f3b2fb9
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/ce/
+-r--r--r--   0 runner    (1001) docker     (123)     4311 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/ce/dcd8ba4511fabecdc11df81e55d82ca8b96ca3
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/cf/
+-r--r--r--   0 runner    (1001) docker     (123)     5817 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/cf/1eea719ca3a291ef7edaa6c60eaa808ca6e4ae
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/d4/
+-r--r--r--   0 runner    (1001) docker     (123)     1026 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/d4/9eb5d776f5b92a02189cebbe590f76db9575bd
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/d8/
+-r--r--r--   0 runner    (1001) docker     (123)      464 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/d8/1e4838c9ac36863e037e68a2f3552f736c5c8f
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/e1/
+-r--r--r--   0 runner    (1001) docker     (123)    23927 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/e1/13bfd922675ce50e68cdf88cd94d16130ad58b
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/e4/
+-r--r--r--   0 runner    (1001) docker     (123)     3441 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/e4/c5465d396f947d57739ed8266597d6a47ef51b
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/e6/
+-r--r--r--   0 runner    (1001) docker     (123)     4593 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/e6/72b6afc2744b043e6fbdf3031eb086a109ec3c
+-r--r--r--   0 runner    (1001) docker     (123)      227 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/e6/e5ddee110d6ed47cbb0a4f30db3d055efd21da
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/fd/
+-r--r--r--   0 runner    (1001) docker     (123)     5204 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/fd/bd32c675f85af4ed57021ac0638a21a3c6cad3
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/objects/ff/
+-r--r--r--   0 runner    (1001) docker     (123)    13943 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/objects/ff/9c65dfdc7a16150c07745e0030a9d6373920cd
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.860353 domain-admin-1.5.6/domain_admin/public/.git/refs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/refs/heads/
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/refs/heads/dist
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.860353 domain-admin-1.5.6/domain_admin/public/.git/refs/remotes/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.884353 domain-admin-1.5.6/domain_admin/public/.git/refs/remotes/origin/
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/refs/remotes/origin/dist
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/.git/shallow
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.888354 domain-admin-1.5.6/domain_admin/public/css/
+-rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/css/ConditionFilterGroup.a91875e6.css
+-rw-r--r--   0 runner    (1001) docker     (123)      301 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/css/index.302e10d7.css
+-rw-r--r--   0 runner    (1001) docker     (123)   331526 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/css/index.69a97337.css
+-rw-r--r--   0 runner    (1001) docker     (123)      111 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/css/index.75ef7015.css
+-rw-r--r--   0 runner    (1001) docker     (123)      117 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/css/index.a676cc2e.css
+-rw-r--r--   0 runner    (1001) docker     (123)      250 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/css/index.b285e10a.css
+-rw-r--r--   0 runner    (1001) docker     (123)      117 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/css/index.cf805e1c.css
+-rw-r--r--   0 runner    (1001) docker     (123)       45 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/css/index.d028ae37.css
+-rwxr-xr-x   0 runner    (1001) docker     (123)    15406 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/favicon.ico
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.888354 domain-admin-1.5.6/domain_admin/public/gif/
+-rw-r--r--   0 runner    (1001) docker     (123)     6334 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/gif/user-avatar.ea67286d.gif
+-rw-r--r--   0 runner    (1001) docker     (123)      911 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/index.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.888354 domain-admin-1.5.6/domain_admin/public/jpg/
+-rw-r--r--   0 runner    (1001) docker     (123)    14271 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/jpg/chatpet-white.10f4f36c.jpg
+-rw-r--r--   0 runner    (1001) docker     (123)    24940 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/jpg/chatpet.fce5580e.jpg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/js/
+-rw-r--r--   0 runner    (1001) docker     (123)    18591 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/ConditionFilterGroup.340936f7.js
+-rw-r--r--   0 runner    (1001) docker     (123)      953 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/ConnectStatus.89654d5c.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/SearchUser.983b7494.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1257 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/SelectGroup.d7e6e540.js
+-rw-r--r--   0 runner    (1001) docker     (123)   390997 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/codemirror-lib.a3a39aa0.js
+-rw-r--r--   0 runner    (1001) docker     (123)   195335 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/element-icon.1ce1c350.js
+-rw-r--r--   0 runner    (1001) docker     (123)   749914 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/element-plus.30eb1cab.js
+-rw-r--r--   0 runner    (1001) docker     (123)      579 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/event-enums.6c6f25e7.js
+-rw-r--r--   0 runner    (1001) docker     (123)  1058329 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/highlight-lib.3654f6d3.js
+-rw-r--r--   0 runner    (1001) docker     (123)    21499 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.075c6a16.js
+-rw-r--r--   0 runner    (1001) docker     (123)    64823 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.12198a8e.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1818 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.127485d4.js
+-rw-r--r--   0 runner    (1001) docker     (123)    10061 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.16184f42.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9652 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.2e3ad8c8.js
+-rw-r--r--   0 runner    (1001) docker     (123)     5241 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.34096d0f.js
+-rw-r--r--   0 runner    (1001) docker     (123)    39363 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.4704b0d3.js
+-rw-r--r--   0 runner    (1001) docker     (123)     4147 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.51aeadc3.js
+-rw-r--r--   0 runner    (1001) docker     (123)    28081 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.58059e0f.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8982 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.86cef4dd.js
+-rw-r--r--   0 runner    (1001) docker     (123)    13888 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.a3947126.js
+-rw-r--r--   0 runner    (1001) docker     (123)     4603 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.ab38e8b8.js
+-rw-r--r--   0 runner    (1001) docker     (123)     4248 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.b84878f9.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2691 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.c05aa8e8.js
+-rw-r--r--   0 runner    (1001) docker     (123)    28958 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/index.c512b8f1.js
+-rw-r--r--   0 runner    (1001) docker     (123)   312580 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/vendor-lib.76301fc3.js
+-rw-r--r--   0 runner    (1001) docker     (123)    94202 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/js/vendor-vue.9e61e0af.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/m/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/m/.git/
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/FETCH_HEAD
+-rw-r--r--   0 runner    (1001) docker     (123)       21 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/HEAD
+-rw-r--r--   0 runner    (1001) docker     (123)      421 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/config
+-rwxr-xr-x   0 runner    (1001) docker     (123)       73 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/description
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/
+-rwxr-xr-x   0 runner    (1001) docker     (123)      478 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/applypatch-msg.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      896 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/commit-msg.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4726 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/fsmonitor-watchman.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      189 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/post-update.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      424 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-applypatch.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1643 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-commit.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      416 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-merge-commit.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1374 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-push.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4898 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-rebase.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)      544 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-receive.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1492 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/prepare-commit-msg.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2783 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/push-to-checkout.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2308 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/sendemail-validate.sample
+-rwxr-xr-x   0 runner    (1001) docker     (123)     3650 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/hooks/update.sample
+-rw-r--r--   0 runner    (1001) docker     (123)     2073 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/index
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/m/.git/info/
+-rwxr-xr-x   0 runner    (1001) docker     (123)      240 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/m/.git/info/exclude
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/m/.git/logs/
+-rw-r--r--   0 runner    (1001) docker     (123)      172 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/logs/HEAD
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.860353 domain-admin-1.5.6/domain_admin/public/m/.git/logs/refs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/m/.git/logs/refs/heads/
+-rw-r--r--   0 runner    (1001) docker     (123)      181 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/logs/refs/heads/dist
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.860353 domain-admin-1.5.6/domain_admin/public/m/.git/logs/refs/remotes/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/m/.git/logs/refs/remotes/origin/
+-rw-r--r--   0 runner    (1001) docker     (123)      302 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/logs/refs/remotes/origin/dist
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.860353 domain-admin-1.5.6/domain_admin/public/m/.git/objects/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/2d/
+-r--r--r--   0 runner    (1001) docker     (123)      814 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/2d/7cec3e00ed3b3b835eb233ae4bb2ea21fb5a0b
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.896354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/43/
+-r--r--r--   0 runner    (1001) docker     (123)     1262 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/43/c4fcdf29fe10c6256aa4e9cf00f534e6933efc
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/4b/
+-r--r--r--   0 runner    (1001) docker     (123)     5351 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/4b/63cfa29bd94b198d895f7a64e10c20f167e65b
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/5c/
+-r--r--r--   0 runner    (1001) docker     (123)       60 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/5c/98d16331bcc99b0cbbe89a3ffb23e3f5918ff2
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/61/
+-r--r--r--   0 runner    (1001) docker     (123)      421 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/61/05f9fd4f4b11812fcca0d2e0704e4c8dd6e7a3
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/62/
+-r--r--r--   0 runner    (1001) docker     (123)      222 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/62/59838c4de171bc95a934ee2384d626eeb3040a
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/67/
+-r--r--r--   0 runner    (1001) docker     (123)      478 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/67/d2a69f1213016d777c02e0c99a38871d07da5b
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/6f/
+-r--r--r--   0 runner    (1001) docker     (123)      725 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/6f/9d23d38fd97c94c1dccf971fd7b7636cc075d2
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/71/
+-r--r--r--   0 runner    (1001) docker     (123)     2231 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/71/4dbccc412b153f5044c269745126581e3cf373
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/7a/
+-r--r--r--   0 runner    (1001) docker     (123)     2494 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/7a/694f3c8aca1586dc6f0e6e9e2773e207992329
+-r--r--r--   0 runner    (1001) docker     (123)      968 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/7a/c4cdd0b7c56c8fe9f98aaf044df58bef26b7a5
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/8e/
+-r--r--r--   0 runner    (1001) docker     (123)     2655 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/8e/ff5bef00cd2492d9b806988ea99996d636c126
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/93/
+-r--r--r--   0 runner    (1001) docker     (123)     1108 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/93/85587145f9afbabe2aa1a489d24fd1f489e5c6
+-r--r--r--   0 runner    (1001) docker     (123)     4673 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/93/db3989e7874cd6b75bc0e984690ffa16666ea6
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/98/
+-r--r--r--   0 runner    (1001) docker     (123)     5141 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/98/1e059e0de4604a5dec80930d8ff7cdf84e0006
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/a9/
+-r--r--r--   0 runner    (1001) docker     (123)     1110 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/a9/a1035a25ce05f60741e3f70716a18d93322203
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/b0/
+-r--r--r--   0 runner    (1001) docker     (123)     1821 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/b0/ecf609c3df960010b6f7877bc379ea45d1e9da
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/c2/
+-r--r--r--   0 runner    (1001) docker     (123)      505 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/c2/c748e84bc4d5118b0e33d6e0073e315a36d034
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/c7/
+-r--r--r--   0 runner    (1001) docker     (123)    31300 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/c7/ef9b19427f9af9e445bb5d63231ccd58ef5b28
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/c8/
+-r--r--r--   0 runner    (1001) docker     (123)   143922 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/c8/bec3f3e9b26642a8221c20a5e422bc2cada687
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/d9/
+-r--r--r--   0 runner    (1001) docker     (123)      119 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/d9/d9ca2809d6994fef91c1ee2d22bc7a54b8b4a5
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/ed/
+-r--r--r--   0 runner    (1001) docker     (123)      979 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/ed/50570bc6865f7dff2468d49072d7f4e4cb81d4
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.900354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/f0/
+-r--r--r--   0 runner    (1001) docker     (123)      755 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/f0/a3f5a57d6bdb9961c3a56f4a992a08a0ecd671
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.904354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/f8/
+-r--r--r--   0 runner    (1001) docker     (123)     1082 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/f8/0169320ed23edd9889e4de7631267635bfec27
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.904354 domain-admin-1.5.6/domain_admin/public/m/.git/objects/fd/
+-r--r--r--   0 runner    (1001) docker     (123)     5204 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/objects/fd/bd32c675f85af4ed57021ac0638a21a3c6cad3
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.860353 domain-admin-1.5.6/domain_admin/public/m/.git/refs/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.904354 domain-admin-1.5.6/domain_admin/public/m/.git/refs/heads/
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/refs/heads/dist
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.860353 domain-admin-1.5.6/domain_admin/public/m/.git/refs/remotes/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.904354 domain-admin-1.5.6/domain_admin/public/m/.git/refs/remotes/origin/
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/refs/remotes/origin/dist
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/.git/shallow
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.904354 domain-admin-1.5.6/domain_admin/public/m/assets/
+-rw-r--r--   0 runner    (1001) docker     (123)     1334 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/common-c7dd5d89.css
+-rw-r--r--   0 runner    (1001) docker     (123)     3913 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/common.6194c42f.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8065 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index-5eda257b.css
+-rw-r--r--   0 runner    (1001) docker     (123)     3782 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index-958ae3a0.css
+-rw-r--r--   0 runner    (1001) docker     (123)   379599 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index-9c365a03.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2798 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index-ad047368.css
+-rw-r--r--   0 runner    (1001) docker     (123)     5447 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index-e8224928.css
+-rw-r--r--   0 runner    (1001) docker     (123)    53115 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index-f79acb3d.css
+-rw-r--r--   0 runner    (1001) docker     (123)     2028 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index.1a0d1182.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1512 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index.1d067866.js
+-rw-r--r--   0 runner    (1001) docker     (123)    10416 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index.daaf9893.js
+-rw-r--r--   0 runner    (1001) docker     (123)     5355 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/index.feef7c0f.js
+-rw-r--r--   0 runner    (1001) docker     (123)     4262 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/login-cb9f43ad.css
+-rw-r--r--   0 runner    (1001) docker     (123)     1959 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/pages-cert-list-cert-list.e9ecbf65.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2016 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/pages-domain-list-domain-list.da5e6454.js
+-rw-r--r--   0 runner    (1001) docker     (123)    10670 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/pages-login-login.09426b90.js
+-rw-r--r--   0 runner    (1001) docker     (123)    12225 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/pages-user-index-user-index.d8efba8c.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1146 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/uni.06dd3c8e.css
+-rw-r--r--   0 runner    (1001) docker     (123)     9118 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/assets/user-index-be7005ab.css
+-rw-r--r--   0 runner    (1001) docker     (123)      835 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/index.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.904354 domain-admin-1.5.6/domain_admin/public/m/static/
+-rwxr-xr-x   0 runner    (1001) docker     (123)     6334 2023-07-23 14:37:35.000000 domain-admin-1.5.6/domain_admin/public/m/static/user-avatar.gif
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.904354 domain-admin-1.5.6/domain_admin/public/svg/
+-rw-r--r--   0 runner    (1001) docker     (123)     1478 2023-07-23 14:37:34.000000 domain-admin-1.5.6/domain_admin/public/svg/logo.184a2d7d.svg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.908354 domain-admin-1.5.6/domain_admin/router/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/router/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7829 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/router/api_map.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1529 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/router/permission.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.908354 domain-admin-1.5.6/domain_admin/service/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2424 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/async_task_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1523 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/auth_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)      698 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/common_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7393 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/domain_info_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12015 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/domain_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)      900 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/file_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2560 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/group_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1131 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/group_user_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4618 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/issue_certificate_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11701 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/notify_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2647 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/operation_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)      465 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/render_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2764 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/scheduler_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2061 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/system_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1566 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/token_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8731 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/service/version_service.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.908354 domain-admin-1.5.6/domain_admin/templates/
+-rw-r--r--   0 runner    (1001) docker     (123)    11659 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/templates/cert-email.html
+-rw-r--r--   0 runner    (1001) docker     (123)      276 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/templates/cert-export.csv
+-rw-r--r--   0 runner    (1001) docker     (123)    10396 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/templates/domain-email.html
+-rw-r--r--   0 runner    (1001) docker     (123)      392 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/templates/domain-export.csv
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.912354 domain-admin-1.5.6/domain_admin/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.912354 domain-admin-1.5.6/domain_admin/utils/acme_util/
+-rw-r--r--   0 runner    (1001) docker     (123)       79 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/acme_util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6183 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/acme_util/acme_v2_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      764 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/bcrypt_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.912354 domain-admin-1.5.6/domain_admin/utils/cert_util/
+-rw-r--r--   0 runner    (1001) docker     (123)      508 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/cert_util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4695 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/cert_util/cert_common.py
+-rw-r--r--   0 runner    (1001) docker     (123)      338 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/cert_util/cert_consts.py
+-rw-r--r--   0 runner    (1001) docker     (123)      288 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/cert_util/cert_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2505 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/cert_util/cert_openssl_v2.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/cert_util/cert_socket.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2679 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/cert_util/cert_socket_v2.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3908 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/datetime_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4690 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/domain_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2201 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/email_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)      424 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/file_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.912354 domain-admin-1.5.6/domain_admin/utils/flask_ext/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      764 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/api_result.py
+-rw-r--r--   0 runner    (1001) docker     (123)      877 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/app_exception.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1587 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/flask_app.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1133 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)      392 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/http_code_enum.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.912354 domain-admin-1.5.6/domain_admin/utils/flask_ext/json/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/json/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/json/default.py
+-rw-r--r--   0 runner    (1001) docker     (123)      569 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/json/json_encoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)      590 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/json/json_provider.py
+-rw-r--r--   0 runner    (1001) docker     (123)      283 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/register.py
+-rw-r--r--   0 runner    (1001) docker     (123)      314 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/flask_ext/request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2841 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/icp_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/ip_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)      942 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/json_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)      325 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/md5_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.912354 domain-admin-1.5.6/domain_admin/utils/open_api/
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/open_api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      850 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/open_api/crtsh_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1329 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/open_api/ding_talk_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1403 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/open_api/feishu_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1443 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/open_api/work_weixin_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.912354 domain-admin-1.5.6/domain_admin/utils/peewee_ext/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/peewee_ext/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1316 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/peewee_ext/model_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)      707 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/secret_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)      596 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/text_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1061 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/time_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.916354 domain-admin-1.5.6/domain_admin/utils/whois_util/
+-rw-r--r--   0 runner    (1001) docker     (123)      205 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/whois_util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2954 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/whois_util/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1983 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/whois_util/util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25912 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/whois_util/whois-servers.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5862 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/utils/whois_util/whois_util.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)      236 2023-07-23 14:37:24.000000 domain-admin-1.5.6/domain_admin/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.864354 domain-admin-1.5.6/domain_admin.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    18454 2023-07-23 14:37:36.000000 domain-admin-1.5.6/domain_admin.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    16145 2023-07-23 14:37:36.000000 domain-admin-1.5.6/domain_admin.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:37:36.000000 domain-admin-1.5.6/domain_admin.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      169 2023-07-23 14:37:36.000000 domain-admin-1.5.6/domain_admin.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-07-23 14:37:36.000000 domain-admin-1.5.6/domain_admin.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:37:36.000000 domain-admin-1.5.6/domain_admin.egg-info/zip-safe
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:37:36.916354 domain-admin-1.5.6/requirements/
+-rw-r--r--   0 runner    (1001) docker     (123)      168 2023-07-23 14:37:24.000000 domain-admin-1.5.6/requirements/production.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 14:37:36.916354 domain-admin-1.5.6/setup.cfg
+-rwxr-xr-x   0 runner    (1001) docker     (123)     3190 2023-07-23 14:37:24.000000 domain-admin-1.5.6/setup.py
```

### Comparing `domain-admin-1.5.5/LICENSE` & `domain-admin-1.5.6/LICENSE`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/PKG-INFO` & `domain-admin-1.5.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: domain-admin
-Version: 1.5.5
+Version: 1.5.6
 Summary: a domain ssl cert admin
 Home-page: https://github.com/mouday/domain-admin
 Author: Peng Shiyu
 Author-email: pengshiyuyx@gmail.com
 License: MIT
 Keywords: domain,ssl,cert,web,monitor
 Platform: any
```

### Comparing `domain-admin-1.5.5/README.md` & `domain-admin-1.5.6/README.md`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/address_api.py` & `domain-admin-1.5.6/domain_admin/api/address_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/auth_api.py` & `domain-admin-1.5.6/domain_admin/api/auth_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/cert_api.py` & `domain-admin-1.5.6/domain_admin/api/cert_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/domain_api.py` & `domain-admin-1.5.6/domain_admin/api/domain_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/domain_info_api.py` & `domain-admin-1.5.6/domain_admin/api/domain_info_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/group_api.py` & `domain-admin-1.5.6/domain_admin/api/group_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/group_user_api.py` & `domain-admin-1.5.6/domain_admin/api/group_user_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/log_async_task_api.py` & `domain-admin-1.5.6/domain_admin/api/log_async_task_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/log_operation_api.py` & `domain-admin-1.5.6/domain_admin/api/log_operation_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/log_scheduler_api.py` & `domain-admin-1.5.6/domain_admin/api/log_scheduler_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/notify_api.py` & `domain-admin-1.5.6/domain_admin/api/notify_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/prometheus_api.py` & `domain-admin-1.5.6/domain_admin/api/prometheus_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/system_api.py` & `domain-admin-1.5.6/domain_admin/api/system_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/user_api.py` & `domain-admin-1.5.6/domain_admin/api/user_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/api/whois_api.py` & `domain-admin-1.5.6/domain_admin/api/whois_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/compat.py` & `domain-admin-1.5.6/domain_admin/compat.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/config/default_config.py` & `domain-admin-1.5.6/domain_admin/config/default_config.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/config/env_config.py` & `domain-admin-1.5.6/domain_admin/config/env_config.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/config/runtime_config.py` & `domain-admin-1.5.6/domain_admin/config/runtime_config.py`

 * *Files 8% similar despite different names*

```diff
@@ -27,23 +27,27 @@
 # 临时文件存放地
 TEMP_DIR = os.path.join(RUNTIME_DIR, 'temp')
 TEMP_DIR_BASE_URL = '/temp'
 
 # 数据库文件存放
 DATABASE_DIR = os.path.join(RUNTIME_DIR, 'database')
 
+# acme_dir
+ACME_DIR = os.path.join(DATABASE_DIR, 'acme')
+
 # sqlite 数据库
 SQLITE_DATABASE_PATH = os.path.join(DATABASE_DIR, 'database.db')
 
 # 日志文件夹
 LOG_DIR = os.path.join(RUNTIME_DIR, 'logs')
 
 # 创建文件夹
 dir_list = [
     TEMP_DIR,
     DATABASE_DIR,
-    LOG_DIR
+    LOG_DIR,
+    ACME_DIR,
 ]
 
 for dirname in dir_list:
     if not os.path.exists(dirname):
         os.mkdir(dirname)
```

### Comparing `domain-admin-1.5.5/domain_admin/enums/config_key_enum.py` & `domain-admin-1.5.6/domain_admin/enums/config_key_enum.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/enums/operation_enum.py` & `domain-admin-1.5.6/domain_admin/enums/operation_enum.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/enums/version_enum.py` & `domain-admin-1.5.6/domain_admin/enums/version_enum.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/log.py` & `domain-admin-1.5.6/domain_admin/log.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/main.py` & `domain-admin-1.5.6/domain_admin/main.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_102_to_103.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_102_to_103.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_106_to_110.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_106_to_110.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_110_to_1212.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_110_to_1212.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_1212_to_1213.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_1212_to_1213.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_1213_to_131.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_1213_to_131.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_136_to_140_alpha.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_136_to_140_alpha.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_140_alpha_to_140.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_140_alpha_to_140.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_1413_to_1414.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_1413_to_1414.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_1422_to_1423.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_1422_to_1423.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_143_to_144.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_143_to_144.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_145_to_146.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_145_to_146.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_151_to_152.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_151_to_152.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_154_to_155.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_154_to_155.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/migrate/migrate_common.py` & `domain-admin-1.5.6/domain_admin/migrate/migrate_common.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/address_model.py` & `domain-admin-1.5.6/domain_admin/model/address_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/base_model.py` & `domain-admin-1.5.6/domain_admin/model/base_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/database.py` & `domain-admin-1.5.6/domain_admin/model/database.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 # -*- coding: utf-8 -*-
 """
 database.py
 """
 from __future__ import print_function, unicode_literals, absolute_import, division
 from domain_admin.log import logger
-from domain_admin.model import address_model, log_operation_model, group_user_model, log_async_task_model
+from domain_admin.model import address_model, log_operation_model, group_user_model, log_async_task_model, \
+    issue_certificate_model
 from domain_admin.model import domain_info_model
 from domain_admin.model import domain_model
 from domain_admin.model import group_model
 from domain_admin.model import log_scheduler_model
 from domain_admin.model import notify_model
 from domain_admin.model import system_model
 from domain_admin.model import user_model
@@ -25,14 +26,15 @@
     (domain_model.DomainModel, None),
     (notify_model.NotifyModel, None),
     (address_model.AddressModel, None),
     (domain_info_model.DomainInfoModel, None),
     (log_operation_model.LogOperationModel, None),
     (group_user_model.GroupUserModel, None),
     (log_async_task_model.AsyncTaskModel, None),
+    (issue_certificate_model.IssueCertificateModel, None),
 ]
 
 
 def init_database():
     """
     初始化数据表
     :return:
```

### Comparing `domain-admin-1.5.5/domain_admin/model/domain_info_model.py` & `domain-admin-1.5.6/domain_admin/model/domain_info_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/domain_model.py` & `domain-admin-1.5.6/domain_admin/model/domain_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/group_model.py` & `domain-admin-1.5.6/domain_admin/model/group_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/group_user_model.py` & `domain-admin-1.5.6/domain_admin/model/group_user_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/log_async_task_model.py` & `domain-admin-1.5.6/domain_admin/model/log_async_task_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/log_operation_model.py` & `domain-admin-1.5.6/domain_admin/model/log_operation_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/log_scheduler_model.py` & `domain-admin-1.5.6/domain_admin/model/log_scheduler_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/notify_model.py` & `domain-admin-1.5.6/domain_admin/model/notify_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/system_model.py` & `domain-admin-1.5.6/domain_admin/model/system_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/user_model.py` & `domain-admin-1.5.6/domain_admin/model/user_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/model/version_model.py` & `domain-admin-1.5.6/domain_admin/model/version_model.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/commit-msg.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/commit-msg.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/fsmonitor-watchman.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/fsmonitor-watchman.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-commit.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-commit.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-push.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-push.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-rebase.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-rebase.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/pre-receive.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/pre-receive.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/prepare-commit-msg.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/prepare-commit-msg.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/push-to-checkout.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/push-to-checkout.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/sendemail-validate.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/sendemail-validate.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/hooks/update.sample` & `domain-admin-1.5.6/domain_admin/public/.git/hooks/update.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/19/7f5cf73cf11d43d915904e0d8aad4736a77d63` & `domain-admin-1.5.6/domain_admin/public/.git/objects/19/7f5cf73cf11d43d915904e0d8aad4736a77d63`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/3c/0f2e923566dc74d04e67d46d8b722923ed1949` & `domain-admin-1.5.6/domain_admin/public/.git/objects/3c/0f2e923566dc74d04e67d46d8b722923ed1949`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/3c/2434ab20d756f0a95ad24f6a5adb7e1219a7d1` & `domain-admin-1.5.6/domain_admin/public/.git/objects/3c/2434ab20d756f0a95ad24f6a5adb7e1219a7d1`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/52/c1926de72b181c9b7faf597fb8f71f48565462` & `domain-admin-1.5.6/domain_admin/public/.git/objects/52/c1926de72b181c9b7faf597fb8f71f48565462`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/5f/a7faf700c98850aa96022ab07af6a07b854f34` & `domain-admin-1.5.6/domain_admin/public/.git/objects/5f/a7faf700c98850aa96022ab07af6a07b854f34`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/69/a9dda41cf39bb60d1dc5b1158ffba197580b6a` & `domain-admin-1.5.6/domain_admin/public/.git/objects/69/a9dda41cf39bb60d1dc5b1158ffba197580b6a`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/6d/15191314c9b832ac41056a30bf0bf6533a29dc` & `domain-admin-1.5.6/domain_admin/public/.git/objects/6d/15191314c9b832ac41056a30bf0bf6533a29dc`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/79/404c2464172f80b414d111f49718327b3ef93b` & `domain-admin-1.5.6/domain_admin/public/.git/objects/79/404c2464172f80b414d111f49718327b3ef93b`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/b3/1cb2667f48424e34cf9517362eadf899f704ad` & `domain-admin-1.5.6/domain_admin/public/.git/objects/b3/1cb2667f48424e34cf9517362eadf899f704ad`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/cc/bfeaa0b21986ed309cbb83d17585b54f3b2fb9` & `domain-admin-1.5.6/domain_admin/public/.git/objects/cc/bfeaa0b21986ed309cbb83d17585b54f3b2fb9`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/e1/13bfd922675ce50e68cdf88cd94d16130ad58b` & `domain-admin-1.5.6/domain_admin/public/.git/objects/e1/13bfd922675ce50e68cdf88cd94d16130ad58b`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/fd/bd32c675f85af4ed57021ac0638a21a3c6cad3` & `domain-admin-1.5.6/domain_admin/public/.git/objects/fd/bd32c675f85af4ed57021ac0638a21a3c6cad3`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/.git/objects/ff/9c65dfdc7a16150c07745e0030a9d6373920cd` & `domain-admin-1.5.6/domain_admin/public/.git/objects/ff/9c65dfdc7a16150c07745e0030a9d6373920cd`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/css/ConditionFilterGroup.a91875e6.css` & `domain-admin-1.5.6/domain_admin/public/css/ConditionFilterGroup.a91875e6.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/css/index.69a97337.css` & `domain-admin-1.5.6/domain_admin/public/css/index.69a97337.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/favicon.ico` & `domain-admin-1.5.6/domain_admin/public/favicon.ico`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/gif/user-avatar.ea67286d.gif` & `domain-admin-1.5.6/domain_admin/public/gif/user-avatar.ea67286d.gif`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/index.html` & `domain-admin-1.5.6/domain_admin/public/index.html`

 * *Files 2% similar despite different names*

```diff
@@ -12,15 +12,15 @@
       content="width=device-width, initial-scale=1.0"
     />
     <meta
       name="referrer"
       content="no-referrer"
     />
     <title>Domain Admin-域名和SSL证书监测系统</title>
-    <script type="module" crossorigin src="./js/index.5c0e1ecd.js"></script>
+    <script type="module" crossorigin src="./js/index.12198a8e.js"></script>
     <link rel="modulepreload" crossorigin href="./js/vendor-vue.9e61e0af.js">
     <link rel="modulepreload" crossorigin href="./js/element-icon.1ce1c350.js">
     <link rel="modulepreload" crossorigin href="./js/element-plus.30eb1cab.js">
     <link rel="modulepreload" crossorigin href="./js/vendor-lib.76301fc3.js">
     <link rel="stylesheet" href="./css/index.69a97337.css">
   </head>
   <body>
```

### Comparing `domain-admin-1.5.5/domain_admin/public/jpg/chatpet-white.10f4f36c.jpg` & `domain-admin-1.5.6/domain_admin/public/jpg/chatpet-white.10f4f36c.jpg`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/jpg/chatpet.fce5580e.jpg` & `domain-admin-1.5.6/domain_admin/public/jpg/chatpet.fce5580e.jpg`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/js/ConditionFilterGroup.cc953e5c.js` & `domain-admin-1.5.6/domain_admin/public/js/ConditionFilterGroup.340936f7.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -1,14 +1,14 @@
 import {
     d as O
 } from "./element-plus.30eb1cab.js";
 import {
     _ as D,
     R as E
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     o as d,
     c as u,
     J as I,
     U as w,
     ah as l,
     V as n,
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/ConnectStatus.b87d1fee.js` & `domain-admin-1.5.6/domain_admin/public/js/ConnectStatus.89654d5c.js`

 * *Files 18% similar despite different names*

#### js-beautify {}

```diff
@@ -1,10 +1,10 @@
 import {
     _
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as n,
     o as a,
     O as s,
     P as e,
     V as l
 } from "./vendor-vue.9e61e0af.js";
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/SearchUser.1ba54ef6.js` & `domain-admin-1.5.6/domain_admin/public/js/SearchUser.983b7494.js`

 * *Files 3% similar despite different names*

#### js-beautify {}

```diff
@@ -1,10 +1,10 @@
 import {
     _ as l
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as c,
     o as d,
     O as i
 } from "./vendor-vue.9e61e0af.js";
 const u = {
     name: "SearchUser",
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/SelectGroup.0ff8c614.js` & `domain-admin-1.5.6/domain_admin/public/js/SelectGroup.d7e6e540.js`

 * *Files 6% similar despite different names*

#### js-beautify {}

```diff
@@ -9,15 +9,15 @@
     F as h,
     L as g,
     al as _
 } from "./vendor-vue.9e61e0af.js";
 import {
     H as f,
     _ as O
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 const S = u({
         id: "group-store",
         state: () => ({
             groupOptions: []
         }),
         getters: {
             getGroupOptions: e => e.groupOptions
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/codemirror-lib.a3a39aa0.js` & `domain-admin-1.5.6/domain_admin/public/js/codemirror-lib.a3a39aa0.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/js/element-icon.1ce1c350.js` & `domain-admin-1.5.6/domain_admin/public/js/element-icon.1ce1c350.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/js/element-plus.30eb1cab.js` & `domain-admin-1.5.6/domain_admin/public/js/element-plus.30eb1cab.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/js/event-enums.6c6f25e7.js` & `domain-admin-1.5.6/domain_admin/public/js/event-enums.6c6f25e7.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/js/highlight-lib.3654f6d3.js` & `domain-admin-1.5.6/domain_admin/public/js/highlight-lib.3654f6d3.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.0a173b97.js` & `domain-admin-1.5.6/domain_admin/public/js/index.2e3ad8c8.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -1,10 +1,10 @@
 import {
     _ as C
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as i,
     o as b,
     c as k,
     V as t,
     P as l,
     a as h,
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.2a4ae78d.js` & `domain-admin-1.5.6/domain_admin/public/js/index.16184f42.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -1,14 +1,14 @@
 import {
     H as U,
     a as J
 } from "./highlight-lib.3654f6d3.js";
 import {
     _ as R
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as m,
     o as x,
     c as O,
     V as f,
     P as d,
     a as w,
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.2d5be753.js` & `domain-admin-1.5.6/domain_admin/public/js/index.58059e0f.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -10,15 +10,15 @@
     T as K,
     t as Q,
     o as B,
     j as X
 } from "./codemirror-lib.a3a39aa0.js";
 import {
     _ as V
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as i,
     o as b,
     O as x,
     K as Y,
     c as S,
     V as o,
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.51ecb744.js` & `domain-admin-1.5.6/domain_admin/public/js/index.51aeadc3.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -1,10 +1,10 @@
 import {
     _ as u
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as n,
     o as _,
     c as g,
     V as a,
     P as l,
     a as c,
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.53934399.js` & `domain-admin-1.5.6/domain_admin/public/js/index.075c6a16.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -1,11 +1,11 @@
 import {
     _ as C,
     R as O
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as a,
     o as p,
     c as y,
     V as s,
     P as i,
     a as _,
@@ -21,18 +21,18 @@
     Q as T,
     F as A,
     ay as N
 } from "./vendor-vue.9e61e0af.js";
 import {
     S as j,
     u as B
-} from "./SelectGroup.0ff8c614.js";
+} from "./SelectGroup.d7e6e540.js";
 import {
     S as F
-} from "./SearchUser.1ba54ef6.js";
+} from "./SearchUser.983b7494.js";
 import "./element-icon.1ce1c350.js";
 import "./vendor-lib.76301fc3.js";
 import "./element-plus.30eb1cab.js";
 const P = {
         name: [{
             message: "\u540D\u79F0\u4E0D\u80FD\u4E3A\u7A7A",
             required: !0,
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.58c30995.js` & `domain-admin-1.5.6/domain_admin/public/js/index.b84878f9.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -1,13 +1,13 @@
 import {
     C as w
-} from "./ConnectStatus.b87d1fee.js";
+} from "./ConnectStatus.89654d5c.js";
 import {
     _ as m
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as l,
     o as _,
     c as f,
     V as a,
     P as n,
     a as c,
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.5c0e1ecd.js` & `domain-admin-1.5.6/domain_admin/public/js/index.12198a8e.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -1,16 +1,16 @@
 import {
     aw as J,
     ax as U,
     o as d,
     c as g,
     U as x,
-    S as $,
+    S as B,
     a as u,
-    ay as V,
+    ay as F,
     ah as r,
     V as i,
     P as s,
     F as C,
     a8 as A,
     O as p,
     R as j,
@@ -272,15 +272,20 @@
         updateGroupUserById: "/updateGroupUserById",
         deleteGroupUserById: "/deleteGroupUserById",
         deleteGroupUserByIds: "/deleteGroupUserByIds",
         getGroupUserById: "/getGroupUserById",
         getGroupUserList: "/getGroupUserList",
         getCertInformation: "/getCertInformation",
         getAsyncTaskLogList: "/getAsyncTaskLogList",
-        clearAsyncTaskLogList: "/clearAsyncTaskLogList"
+        clearAsyncTaskLogList: "/clearAsyncTaskLogList",
+        getCertificateList: "/getCertificateList",
+        issueCertificate: "/issueCertificate",
+        renewCertificate: "/renewCertificate",
+        getIssueCertificateById: "/getIssueCertificateById",
+        verifyCertificateById: "/verifyCertificateById"
     },
     M = "token";
 
 function ct(e) {
     R.set(M, e, {
         expires: 7
     })
@@ -319,15 +324,15 @@
 function gt() {
     let e = {};
     for (let [t, n] of Object.entries(mt)) e[t] = ft(n);
     return e
 }
 const N = gt();
 
-function $o(e) {
+function Bo(e) {
     return X + e
 }
 class ht {
     static message(t) {
         return O.closeAll(), O(t)
     }
     static success(t) {
@@ -410,15 +415,15 @@
                 e.code == 0 && (this._userInfo = e.data)
             },
             removeUserInfo() {
                 this._userInfo = null
             }
         }
     }),
-    B = J({
+    $ = J({
         id: "system-store",
         state: () => ({
             _isCollapse: !1,
             _version: ""
         }),
         getters: {
             isCollapse(e) {
@@ -450,15 +455,15 @@
         name: "",
         props: [],
         components: {},
         data() {
             return {}
         },
         computed: {
-            ...U(B, {
+            ...U($, {
                 version: "version"
             })
         },
         methods: {
             async getData() {}
         },
         created() {
@@ -485,15 +490,15 @@
         class: "sidebar-info__box"
     }, [u("img", {
         alt: "GitHub stars",
         src: "https://img.shields.io/github/stars/mouday/domain-admin.svg?style=social"
     })], -1);
 
 function Ct(e, t, n, m, o, a) {
-    return d(), g("div", wt, [e.version ? (d(), g("div", It, x(e.version), 1)) : $("", !0), Dt, xt])
+    return d(), g("div", wt, [e.version ? (d(), g("div", It, x(e.version), 1)) : B("", !0), Dt, xt])
 }
 const Et = w(vt, [
     ["render", Ct]
 ]);
 const kt = {
         name: "Menu",
         props: {},
@@ -508,20 +513,20 @@
         },
         computed: {
             ...U(P, {
                 userInfo: "userInfo",
                 isAdmin: "isAdmin",
                 userRoles: "userRoles"
             }),
-            ...U(B, {
+            ...U($, {
                 isCollapse: "isCollapse"
             })
         },
         methods: {
-            ...V(B, {
+            ...F($, {
                 toggleCollapse: "toggleCollapse"
             }),
             async getData() {},
             handleSelect(e) {},
             handleRouteClick(e) {
                 this.$router.push({
                     name: e.name
@@ -540,27 +545,27 @@
     },
     St = {
         class: "layout-container"
     },
     Lt = {
         class: "layout__menu-wrap"
     },
-    $t = {
+    Bt = {
         class: "layout__menu__collapse-wrap"
     };
 
-function Bt(e, t, n, m, o, a) {
+function $t(e, t, n, m, o, a) {
     const l = r("el-icon"),
         _ = r("el-menu-item"),
         c = r("el-sub-menu"),
         y = r("Info"),
         I = r("el-menu"),
         T = r("CaretRight"),
         E = r("el-link"),
-        F = r("CaretLeft");
+        V = r("CaretLeft");
     return d(), g("div", St, [u("div", Lt, [i(I, {
         "default-active": o.activeIndex,
         ellipsis: !1,
         class: "layout__menu",
         mode: "vertical",
         "menu-trigger": "click",
         "unique-opened": "",
@@ -590,23 +595,23 @@
             default: s(() => [(d(!0), g(C, null, A(b.children, S => (d(), g(C, null, [a.hasRoutePermission(S) ? (d(), p(_, {
                 key: 0,
                 index: S.name,
                 onClick: q => a.handleRouteClick(S)
             }, {
                 default: s(() => [v(x(S.meta.title), 1)]),
                 _: 2
-            }, 1032, ["index", "onClick"])) : $("", !0)], 64))), 256))]),
+            }, 1032, ["index", "onClick"])) : B("", !0)], 64))), 256))]),
             _: 2
-        }, 1032, ["index"]))], 64)) : $("", !0)], 64))), 256)), Qe(i(y, {
+        }, 1032, ["index"]))], 64)) : B("", !0)], 64))), 256)), Qe(i(y, {
             class: "menu-info"
         }, null, 512), [
             [Xe, !e.isCollapse]
         ])]),
         _: 1
-    }, 8, ["default-active", "onSelect", "collapse"]), u("div", $t, [u("div", {
+    }, 8, ["default-active", "onSelect", "collapse"]), u("div", Bt, [u("div", {
         class: "layout__menu__collapse",
         onClick: t[0] || (t[0] = (...b) => e.toggleCollapse && e.toggleCollapse(...b))
     }, [e.isCollapse ? (d(), p(E, {
         key: 0,
         underline: !1
     }, {
         default: s(() => [i(l, null, {
@@ -615,22 +620,22 @@
         })]),
         _: 1
     })) : (d(), p(E, {
         key: 1,
         underline: !1
     }, {
         default: s(() => [i(l, null, {
-            default: s(() => [i(F)]),
+            default: s(() => [i(V)]),
             _: 1
         })]),
         _: 1
     }))])])])])
 }
 const Ot = w(kt, [
-        ["render", Bt]
+        ["render", $t]
     ]),
     Ut = {
         name: "Footer",
         props: {},
         components: {},
         data() {
             return {}
@@ -643,19 +648,19 @@
             this.getData()
         }
     },
     At = {
         class: "footer"
     };
 
-function Ft(e, t, n, m, o, a) {
+function Vt(e, t, n, m, o, a) {
     return d(), g("div", At)
 }
-const Vt = w(Ut, [
-        ["render", Ft]
+const Ft = w(Ut, [
+        ["render", Vt]
     ]),
     Pt = {
         password: [{
             message: "\u65E7\u5BC6\u7801\u4E0D\u80FD\u4E3A\u7A7A",
             required: !0,
             trigger: "blur"
         }],
@@ -835,15 +840,15 @@
         "append-to-body": ""
     }, {
         default: s(() => [a.dialogVisible ? (d(), p(l, {
             key: 0,
             row: n.row,
             onOnCancel: a.handleClose,
             onOnSuccess: a.handleSuccess
-        }, null, 8, ["row", "onOnCancel", "onOnSuccess"])) : $("", !0)]),
+        }, null, 8, ["row", "onOnCancel", "onOnSuccess"])) : B("", !0)]),
         _: 1
     }, 8, ["modelValue"])
 }
 const qt = w(Gt, [
     ["render", Nt]
 ]);
 const zt = {
@@ -998,15 +1003,15 @@
         "lock-scroll": !1
     }, {
         default: s(() => [a.dialogVisible ? (d(), p(l, {
             key: 0,
             row: n.row,
             onOnCancel: a.handleClose,
             onOnSuccess: a.handleSuccess
-        }, null, 8, ["row", "onOnCancel", "onOnSuccess"])) : $("", !0)]),
+        }, null, 8, ["row", "onOnCancel", "onOnSuccess"])) : B("", !0)]),
         _: 1
     }, 8, ["modelValue"])
 }
 const ta = w(Zt, [
         ["render", ea]
     ]),
     aa = {};
@@ -1188,15 +1193,15 @@
         "lock-scroll": !1
     }, {
         default: s(() => [a.dialogVisible ? (d(), p(l, {
             key: 0,
             row: n.row,
             onOnCancel: a.handleClose,
             onOnSuccess: a.handleSuccess
-        }, null, 8, ["row", "onOnCancel", "onOnSuccess"])) : $("", !0)]),
+        }, null, 8, ["row", "onOnCancel", "onOnSuccess"])) : B("", !0)]),
         _: 1
     }, 8, ["modelValue"])
 }
 const ma = w(ua, [
         ["render", _a]
     ]),
     ca = {
@@ -1269,14 +1274,18 @@
                     label: "\u8BC1\u4E66\u4FE1\u606F\u67E5\u8BE2",
                     value: "cert-info"
                 }, {
                     type: "router",
                     label: "ICP\u5907\u6848\u67E5\u8BE2",
                     value: "icp-info"
                 }, {
+                    type: "router",
+                    label: "SSL\u8BC1\u4E66\u7533\u8BF7",
+                    value: "issue-certificate-list"
+                }, {
                     type: "url",
                     label: "SSL\u914D\u7F6E\u751F\u6210",
                     value: "https://ssl-config.mozilla.org/"
                 }, {
                     type: "url",
                     label: "\u514D\u8D39SSL\u8BC1\u4E66",
                     value: "https://yundun.console.aliyun.com/?p=cas#/certExtend/free"
@@ -1301,27 +1310,27 @@
             this.getData()
         },
         computed: {
             ...U(P, {
                 userInfo: "userInfo",
                 isAdmin: "isAdmin"
             }),
-            ...U(B, {
+            ...U($, {
                 isCollapse: "isCollapse"
             }),
             username() {
                 return this.userInfo ? this.userInfo.username : ""
             }
         },
         methods: {
-            ...V(P, {
+            ...F(P, {
                 updateUserInfo: "updateUserInfo",
                 removeUserInfo: "removeUserInfo"
             }),
-            ...V(B, {
+            ...F($, {
                 toggleCollapse: "toggleCollapse"
             }),
             handleLogoutClick(e) {
                 this.removeUserInfo(), pt(), this.$router.push({
                     path: "/login"
                 })
             },
@@ -1425,15 +1434,15 @@
     const l = r("Menu"),
         _ = r("el-icon"),
         c = r("Breadcrumb"),
         y = r("Suitcase"),
         I = r("arrow-down"),
         T = r("Link"),
         E = r("el-dropdown-item"),
-        F = r("el-dropdown-menu"),
+        V = r("el-dropdown-menu"),
         b = r("el-dropdown"),
         S = r("el-radio-button"),
         q = r("el-radio-group"),
         ze = r("el-avatar"),
         He = r("UserPaswordEditDataFormDailog"),
         We = r("UserDataFormDailig"),
         Ke = r("AboutDataFormDailig");
@@ -1447,15 +1456,15 @@
         }
     }, {
         default: s(() => [i(l)]),
         _: 1
     })]), wa, u("div", Ia, [i(c)]), u("div", Da, [xa, i(b, {
         trigger: "hover"
     }, {
-        dropdown: s(() => [i(F, null, {
+        dropdown: s(() => [i(V, null, {
             default: s(() => [(d(!0), g(C, null, A(o.toolList, f => (d(), g(C, null, [f.type == "url" ? (d(), p(E, {
                 key: 0,
                 onClick: Je => a.handleToolItemClick(f),
                 class: "justify-center"
             }, {
                 default: s(() => [v(x(f.label), 1), i(_, null, {
                     default: s(() => [i(T)]),
@@ -1494,15 +1503,15 @@
             default: s(() => [v(x(f.label), 1)]),
             _: 2
         }, 1032, ["label"]))), 128))]),
         _: 1
     }, 8, ["modelValue", "onChange"]), i(b, {
         trigger: "hover"
     }, {
-        dropdown: s(() => [i(F, null, {
+        dropdown: s(() => [i(V, null, {
             default: s(() => [i(E, {
                 onClick: a.handleUpdatePasswordClick,
                 class: "justify-center"
             }, {
                 default: s(() => [v("\u4FEE\u6539\u5BC6\u7801")]),
                 _: 1
             }, 8, ["onClick"]), i(E, {
@@ -1538,20 +1547,20 @@
         visible: o.aboutDialogVisible,
         "onUpdate:visible": t[4] || (t[4] = f => o.aboutDialogVisible = f)
     }, null, 8, ["visible"])])
 }
 const La = w(ba, [
     ["render", Sa]
 ]);
-const $a = {
+const Ba = {
         name: "index",
         props: {},
         components: {
             Menu: Ot,
-            Footer: Vt,
+            Footer: Ft,
             Header: La
         },
         data() {
             return {}
         },
         computed: {
             currentPathName() {
@@ -1564,51 +1573,51 @@
         methods: {
             async getData() {}
         },
         created() {
             this.getData()
         }
     },
-    Ba = {
+    $a = {
         class: "app-layout"
     },
     Oa = {
         class: "app-layout__main"
     },
     Ua = {
         class: "app-layout__body"
     },
     Aa = {
         class: "app-layout__view"
     };
 
-function Fa(e, t, n, m, o, a) {
+function Va(e, t, n, m, o, a) {
     const l = r("Header"),
         _ = r("Menu"),
         c = r("router-view"),
         y = r("Footer");
-    return d(), g("div", Ba, [i(l), u("div", Oa, [i(_), u("div", Ua, [u("div", Aa, [i(c, null, {
+    return d(), g("div", $a, [i(l), u("div", Oa, [i(_), u("div", Ua, [u("div", Aa, [i(c, null, {
         default: s(({
             Component: I
         }) => [i(Ye, {
             name: "fade-transform",
             mode: "out-in"
         }, {
             default: s(() => [(d(), p(j(I), {
                 key: a.key
             }))]),
             _: 2
         }, 1024)]),
         _: 1
     })])])]), i(y)])
 }
-const k = w($a, [
-    ["render", Fa]
+const k = w(Ba, [
+    ["render", Va]
 ]);
-const Va = {
+const Fa = {
         name: "Login",
         props: {},
         components: {},
         data() {
             return {
                 form: {
                     username: "",
@@ -1710,15 +1719,15 @@
         size: "large",
         onClick: et(a.onSubmit, ["prevent"])
     }, {
         default: s(() => [v("\u767B \u5F55")]),
         _: 1
     }, 8, ["onClick"])])])])
 }
-const Ga = w(Va, [
+const Ga = w(Fa, [
         ["render", Ma],
         ["__scopeId", "data-v-ea6aa27d"]
     ]),
     ee = [{
         path: "/login",
         component: Ga,
         meta: {
@@ -1742,15 +1751,15 @@
         },
         redirect: {
             name: "cert-list"
         },
         children: [{
             path: "list",
             name: "cert-list",
-            component: () => h(() => import("./index.7089425b.js"), ["index.7089425b.js", "event-enums.6c6f25e7.js", "SelectGroup.0ff8c614.js", "vendor-vue.9e61e0af.js", "ConditionFilterGroup.cc953e5c.js", "../css/ConditionFilterGroup.a91875e6.css", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "ConnectStatus.b87d1fee.js", "vendor-lib.76301fc3.js"], import.meta.url),
+            component: () => h(() => import("./index.c512b8f1.js"), ["index.c512b8f1.js", "event-enums.6c6f25e7.js", "SelectGroup.d7e6e540.js", "vendor-vue.9e61e0af.js", "ConditionFilterGroup.340936f7.js", "../css/ConditionFilterGroup.a91875e6.css", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "ConnectStatus.89654d5c.js", "vendor-lib.76301fc3.js"], import.meta.url),
             meta: {
                 title: "\u8BC1\u4E66\u5217\u8868",
                 icon: "Tickets"
             }
         }]
     }, {
         path: "/domain",
@@ -1762,15 +1771,15 @@
         },
         redirect: {
             name: "domain-list"
         },
         children: [{
             path: "list",
             name: "domain-list",
-            component: () => h(() => import("./index.a747af4a.js"), ["index.a747af4a.js", "../css/index.302e10d7.css", "event-enums.6c6f25e7.js", "SelectGroup.0ff8c614.js", "vendor-vue.9e61e0af.js", "SearchUser.1ba54ef6.js", "ConditionFilterGroup.cc953e5c.js", "../css/ConditionFilterGroup.a91875e6.css", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js"], import.meta.url),
+            component: () => h(() => import("./index.4704b0d3.js"), ["index.4704b0d3.js", "../css/index.302e10d7.css", "event-enums.6c6f25e7.js", "SelectGroup.d7e6e540.js", "vendor-vue.9e61e0af.js", "SearchUser.983b7494.js", "ConditionFilterGroup.340936f7.js", "../css/ConditionFilterGroup.a91875e6.css", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js"], import.meta.url),
             meta: {
                 title: "\u57DF\u540D\u5217\u8868",
                 icon: "Coin"
             }
         }]
     }, {
         path: "/group",
@@ -1782,15 +1791,15 @@
         },
         redirect: {
             name: "group-list"
         },
         children: [{
             path: "list",
             name: "group-list",
-            component: () => h(() => import("./index.53934399.js"), ["index.53934399.js", "vendor-vue.9e61e0af.js", "SelectGroup.0ff8c614.js", "SearchUser.1ba54ef6.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.075c6a16.js"), ["index.075c6a16.js", "vendor-vue.9e61e0af.js", "SelectGroup.d7e6e540.js", "SearchUser.983b7494.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "\u5206\u7EC4\u7BA1\u7406",
                 icon: "Files"
             }
         }]
     }, {
         path: "/notify",
@@ -1802,15 +1811,15 @@
         },
         redirect: {
             name: "notify-list"
         },
         children: [{
             path: "edit",
             name: "notify-list",
-            component: () => h(() => import("./index.2d5be753.js"), ["index.2d5be753.js", "event-enums.6c6f25e7.js", "codemirror-lib.a3a39aa0.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.58059e0f.js"), ["index.58059e0f.js", "event-enums.6c6f25e7.js", "codemirror-lib.a3a39aa0.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "\u901A\u77E5\u5217\u8868",
                 icon: "Message"
             }
         }]
     }, {
         path: "/data",
@@ -1823,37 +1832,37 @@
             title: "\u6570\u636E\u7BA1\u7406",
             icon: "Box",
             roles: [D.Admin]
         },
         children: [{
             path: "cert-list",
             name: "data-cert-list",
-            component: () => h(() => import("./index.7089425b.js"), ["index.7089425b.js", "event-enums.6c6f25e7.js", "SelectGroup.0ff8c614.js", "vendor-vue.9e61e0af.js", "ConditionFilterGroup.cc953e5c.js", "../css/ConditionFilterGroup.a91875e6.css", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "ConnectStatus.b87d1fee.js", "vendor-lib.76301fc3.js"], import.meta.url),
+            component: () => h(() => import("./index.c512b8f1.js"), ["index.c512b8f1.js", "event-enums.6c6f25e7.js", "SelectGroup.d7e6e540.js", "vendor-vue.9e61e0af.js", "ConditionFilterGroup.340936f7.js", "../css/ConditionFilterGroup.a91875e6.css", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "ConnectStatus.89654d5c.js", "vendor-lib.76301fc3.js"], import.meta.url),
             meta: {
                 title: "\u5168\u90E8\u8BC1\u4E66",
                 icon: "Tickets"
             },
             props: {
                 role: D.Admin
             }
         }, {
             path: "domain-list",
             name: "data-domain-list",
-            component: () => h(() => import("./index.a747af4a.js"), ["index.a747af4a.js", "../css/index.302e10d7.css", "event-enums.6c6f25e7.js", "SelectGroup.0ff8c614.js", "vendor-vue.9e61e0af.js", "SearchUser.1ba54ef6.js", "ConditionFilterGroup.cc953e5c.js", "../css/ConditionFilterGroup.a91875e6.css", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js"], import.meta.url),
+            component: () => h(() => import("./index.4704b0d3.js"), ["index.4704b0d3.js", "../css/index.302e10d7.css", "event-enums.6c6f25e7.js", "SelectGroup.d7e6e540.js", "vendor-vue.9e61e0af.js", "SearchUser.983b7494.js", "ConditionFilterGroup.340936f7.js", "../css/ConditionFilterGroup.a91875e6.css", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js"], import.meta.url),
             meta: {
                 title: "\u5168\u90E8\u57DF\u540D",
                 icon: "Coin"
             },
             props: {
                 role: D.Admin
             }
         }, {
             path: "group-list",
             name: "data-group-list",
-            component: () => h(() => import("./index.53934399.js"), ["index.53934399.js", "vendor-vue.9e61e0af.js", "SelectGroup.0ff8c614.js", "SearchUser.1ba54ef6.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.075c6a16.js"), ["index.075c6a16.js", "vendor-vue.9e61e0af.js", "SelectGroup.d7e6e540.js", "SearchUser.983b7494.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "\u5168\u90E8\u5206\u7EC4",
                 icon: "Files"
             },
             props: {
                 role: D.Admin
             }
@@ -1869,24 +1878,24 @@
             title: "\u7CFB\u7EDF\u7BA1\u7406",
             icon: "Setting",
             roles: [D.Admin]
         },
         children: [{
             path: "user-list",
             name: "admin-user-list",
-            component: () => h(() => import("./index.0a173b97.js"), ["index.0a173b97.js", "vendor-vue.9e61e0af.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js"], import.meta.url),
+            component: () => h(() => import("./index.2e3ad8c8.js"), ["index.2e3ad8c8.js", "vendor-vue.9e61e0af.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js"], import.meta.url),
             meta: {
                 title: "\u7528\u6237\u7BA1\u7406",
                 icon: "User",
                 roles: [D.Admin]
             }
         }, {
             path: "system-setup",
             name: "system-setup",
-            component: () => h(() => import("./index.b77111ba.js"), ["index.b77111ba.js", "../css/index.d028ae37.css", "vendor-vue.9e61e0af.js", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js"], import.meta.url),
+            component: () => h(() => import("./index.86cef4dd.js"), ["index.86cef4dd.js", "../css/index.d028ae37.css", "vendor-vue.9e61e0af.js", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js"], import.meta.url),
             meta: {
                 title: "\u7CFB\u7EDF\u8BBE\u7F6E",
                 icon: "Setting",
                 roles: [D.Admin]
             }
         }]
     }, {
@@ -1900,33 +1909,33 @@
             title: "\u7CFB\u7EDF\u65E5\u5FD7",
             icon: "Clock",
             roles: [D.Admin]
         },
         children: [{
             path: "log-scheduler-list",
             name: "log-scheduler-list",
-            component: () => h(() => import("./index.58c30995.js"), ["index.58c30995.js", "ConnectStatus.b87d1fee.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.b84878f9.js"), ["index.b84878f9.js", "ConnectStatus.89654d5c.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "\u76D1\u6D4B\u65E5\u5FD7",
                 icon: "Calendar",
                 roles: [D.Admin]
             }
         }, {
             path: "log-operation-list",
             name: "log-operation-list",
-            component: () => h(() => import("./index.2a4ae78d.js"), ["index.2a4ae78d.js", "../css/index.b285e10a.css", "highlight-lib.3654f6d3.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.16184f42.js"), ["index.16184f42.js", "../css/index.b285e10a.css", "highlight-lib.3654f6d3.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "\u64CD\u4F5C\u65E5\u5FD7",
                 icon: "Compass",
                 roles: [D.Admin]
             }
         }, {
             path: "log-async-task-list",
             name: "log-async-task-list",
-            component: () => h(() => import("./index.edfe11bc.js"), ["index.edfe11bc.js", "ConnectStatus.b87d1fee.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.ab38e8b8.js"), ["index.ab38e8b8.js", "ConnectStatus.89654d5c.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "\u5F02\u6B65\u4EFB\u52A1",
                 icon: "Compass",
                 roles: [D.Admin]
             }
         }]
     }, {
@@ -1939,47 +1948,56 @@
         meta: {
             hidden: !0,
             title: "\u5DE5\u5177\u7BB1"
         },
         children: [{
             path: "lab",
             name: "lab",
-            component: () => h(() => import("./index.df8aa1f7.js"), ["index.df8aa1f7.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.127485d4.js"), ["index.127485d4.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "WHOIS\u67E5\u8BE2",
                 icon: "Box",
                 hidden: !0
             }
         }, {
             path: "domain-cert-list",
             name: "domain-cert-list",
-            component: () => h(() => import("./index.51ecb744.js"), ["index.51ecb744.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.51aeadc3.js"), ["index.51aeadc3.js", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "\u5B50\u57DF\u540D\u8BC1\u4E66\u67E5\u8BE2",
                 icon: "Box",
                 hidden: !0
             }
         }, {
             path: "cert-info",
             name: "cert-info",
-            component: () => h(() => import("./index.d21190a6.js"), ["index.d21190a6.js", "../css/index.a676cc2e.css", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.34096d0f.js"), ["index.34096d0f.js", "../css/index.a676cc2e.css", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "\u8BC1\u4E66\u4FE1\u606F\u67E5\u8BE2",
                 icon: "Box",
                 hidden: !0
             }
         }, {
             path: "icp-info",
             name: "icp-info",
-            component: () => h(() => import("./index.87e9fadd.js"), ["index.87e9fadd.js", "../css/index.cf805e1c.css", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
+            component: () => h(() => import("./index.c05aa8e8.js"), ["index.c05aa8e8.js", "../css/index.cf805e1c.css", "vendor-vue.9e61e0af.js", "element-icon.1ce1c350.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js"], import.meta.url),
             meta: {
                 title: "ICP\u5907\u6848\u67E5\u8BE2",
                 icon: "Box",
                 hidden: !0
             }
+        }, {
+            path: "issue-certificate-list",
+            name: "issue-certificate-list",
+            component: () => h(() => import("./index.a3947126.js"), ["index.a3947126.js", "../css/index.75ef7015.css", "vendor-vue.9e61e0af.js", "vendor-lib.76301fc3.js", "element-plus.30eb1cab.js", "element-icon.1ce1c350.js", "ConnectStatus.89654d5c.js"], import.meta.url),
+            meta: {
+                title: "SSL\u8BC1\u4E66\u7533\u8BF7",
+                icon: "Box",
+                hidden: !0
+            }
         }]
     }];
 const Na = ["/login"];
 
 function qa(e) {
     e.beforeEach(async (t, n, m) => {
         z.start();
@@ -2934,15 +2952,15 @@
         data: ke,
         msg: Se,
         default: lo
     }, Symbol.toStringTag, {
         value: "Module"
     })),
     Le = 0,
-    $e = {
+    Be = {
         list: [{
             after: '{"id": 2, "user_id": 1, "domain": "wenku.baidu.com", "root_domain": "baidu.com", "port": 443, "alias": "", "group_id": 0, "start_time": "2022-07-05 13:16:02", "expire_time": "2023-08-06 13:16:01", "expire_days": 32, "auto_update": true, "is_monitor": true, "is_dynamic_host": false, "connect_status": true, "total_days": 0, "create_time": "2023-06-29 17:32:01", "update_time": "2023-07-05 10:17:30"}',
             before: '{"id": 2, "user_id": 1, "domain": "zhidao.baidu.com", "root_domain": "baidu.com", "port": 443, "alias": "", "group_id": 0, "start_time": "2022-07-05 13:16:02", "expire_time": "2023-08-06 13:16:01", "expire_days": 32, "auto_update": true, "is_monitor": true, "is_dynamic_host": false, "connect_status": true, "total_days": 0, "create_time": "2023-06-29 17:32:01", "update_time": "2023-07-05 10:17:02"}',
             create_time: "2023-07-05 10:17:30",
             create_time_label: "4\u5C0F\u65F6\u524D",
             id: 19,
             table: "tb_domain",
@@ -3058,25 +3076,25 @@
             type_label: "\u5220\u9664",
             update_time: "2023-07-04 22:45:16",
             user_id: 1,
             user_name: "admin"
         }],
         total: 19
     },
-    Be = "success",
+    $e = "success",
     _o = {
         code: Le,
-        data: $e,
-        msg: Be
+        data: Be,
+        msg: $e
     },
     mo = Object.freeze(Object.defineProperty({
         __proto__: null,
         code: Le,
-        data: $e,
-        msg: Be,
+        data: Be,
+        msg: $e,
         default: _o
     }, Symbol.toStringTag, {
         value: "Module"
     })),
     Oe = 0,
     Ue = {
         version: "latest"
@@ -3092,35 +3110,35 @@
         code: Oe,
         data: Ue,
         msg: Ae,
         default: co
     }, Symbol.toStringTag, {
         value: "Module"
     })),
-    Fe = 0,
-    Ve = {
+    Ve = 0,
+    Fe = {
         id: 1,
         username: "admin",
         avatar_url: "",
         before_expire_days: 3,
         email_list: ["email@qq.com"],
         status: !0,
         create_time: "2022-10-03 23:07:21",
         update_time: "2022-10-08 16:54:08"
     },
     Pe = "success",
     fo = {
-        code: Fe,
-        data: Ve,
+        code: Ve,
+        data: Fe,
         msg: Pe
     },
     go = Object.freeze(Object.defineProperty({
         __proto__: null,
-        code: Fe,
-        data: Ve,
+        code: Ve,
+        data: Fe,
         msg: Pe,
         default: fo
     }, Symbol.toStringTag, {
         value: "Module"
     })),
     Te = 0,
     je = {
@@ -3214,15 +3232,15 @@
     props: {},
     components: {},
     data() {
         return {}
     },
     computed: {},
     methods: {
-        ...V(B, {
+        ...F($, {
             updateVersion: "updateVersion",
             setIsCollapse: "setIsCollapse"
         })
     },
     created() {
         let e = localStorage.getItem("isCollapse");
         this.setIsCollapse(e == "true"), this.updateVersion()
@@ -3255,9 +3273,9 @@
     locale: _t
 });
 for (const [e, t] of Object.entries(nt)) L.component(e, t);
 const Co = rt();
 L.use(Co);
 L.mount("#app");
 export {
-    N as H, D as R, w as _, mt as d, $o as r, P as u
+    N as H, D as R, w as _, mt as d, Bo as r, P as u
 };
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.7089425b.js` & `domain-admin-1.5.6/domain_admin/public/js/index.c512b8f1.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -1,21 +1,21 @@
 import {
     i as Y,
     E as M
 } from "./event-enums.6c6f25e7.js";
 import {
     S as N,
     u as z
-} from "./SelectGroup.0ff8c614.js";
+} from "./SelectGroup.d7e6e540.js";
 import {
     _ as v,
     R as $,
     d as L,
     r as W
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as s,
     ar as P,
     Q as G,
     o as u,
     c as g,
     V as o,
@@ -33,18 +33,18 @@
 } from "./vendor-vue.9e61e0af.js";
 import {
     E as q,
     A as J,
     a as Z,
     b as ee,
     C as te
-} from "./ConditionFilterGroup.cc953e5c.js";
+} from "./ConditionFilterGroup.340936f7.js";
 import {
     C as oe
-} from "./ConnectStatus.b87d1fee.js";
+} from "./ConnectStatus.89654d5c.js";
 import {
     F as le
 } from "./vendor-lib.76301fc3.js";
 import {
     b as ie
 } from "./element-plus.30eb1cab.js";
 import "./element-icon.1ce1c350.js";
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.87e9fadd.js` & `domain-admin-1.5.6/domain_admin/public/js/index.c05aa8e8.js`

 * *Files 4% similar despite different names*

#### js-beautify {}

```diff
@@ -11,15 +11,15 @@
     T as f,
     U as u,
     az as I,
     aA as k
 } from "./vendor-vue.9e61e0af.js";
 import {
     _ as C
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import "./element-icon.1ce1c350.js";
 import "./vendor-lib.76301fc3.js";
 import "./element-plus.30eb1cab.js";
 const V = {
         name: "index",
         props: {},
         components: {},
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.a747af4a.js` & `domain-admin-1.5.6/domain_admin/public/js/index.4704b0d3.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -1,25 +1,25 @@
 import {
     i as X,
     E as Z
 } from "./event-enums.6c6f25e7.js";
 import {
     S as q,
     u as $
-} from "./SelectGroup.0ff8c614.js";
+} from "./SelectGroup.d7e6e540.js";
 import {
     S as ee
-} from "./SearchUser.1ba54ef6.js";
+} from "./SearchUser.983b7494.js";
 import {
     R as V,
     _ as v,
     u as te,
     d as j,
     r as oe
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ax as G,
     ah as r,
     ar as P,
     Q as A,
     o as m,
     c as y,
@@ -40,15 +40,15 @@
 } from "./vendor-vue.9e61e0af.js";
 import {
     E as M,
     A as ae,
     a as re,
     b as de,
     C as ce
-} from "./ConditionFilterGroup.cc953e5c.js";
+} from "./ConditionFilterGroup.340936f7.js";
 import {
     F as me
 } from "./vendor-lib.76301fc3.js";
 import {
     b as ue
 } from "./element-plus.30eb1cab.js";
 import "./element-icon.1ce1c350.js";
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.b77111ba.js` & `domain-admin-1.5.6/domain_admin/public/js/index.86cef4dd.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -1,10 +1,10 @@
 import {
     _ as g
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as a,
     o as u,
     c as d,
     V as r,
     P as l,
     a as f,
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.d21190a6.js` & `domain-admin-1.5.6/domain_admin/public/js/index.34096d0f.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -13,15 +13,15 @@
     F as k,
     a8 as N,
     az as w,
     aA as j
 } from "./vendor-vue.9e61e0af.js";
 import {
     _ as V
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import "./element-icon.1ce1c350.js";
 import "./vendor-lib.76301fc3.js";
 import "./element-plus.30eb1cab.js";
 const A = {
         name: "index",
         props: {},
         components: {},
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.df8aa1f7.js` & `domain-admin-1.5.6/domain_admin/public/js/index.127485d4.js`

 * *Files 5% similar despite different names*

#### js-beautify {}

```diff
@@ -8,15 +8,15 @@
     a as i,
     U as w,
     a9 as S,
     T as b
 } from "./vendor-vue.9e61e0af.js";
 import {
     _ as V
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import "./element-icon.1ce1c350.js";
 import "./vendor-lib.76301fc3.js";
 import "./element-plus.30eb1cab.js";
 const k = {
         name: "index",
         props: {},
         components: {},
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/index.edfe11bc.js` & `domain-admin-1.5.6/domain_admin/public/js/index.ab38e8b8.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -1,13 +1,13 @@
 import {
     C as S
-} from "./ConnectStatus.b87d1fee.js";
+} from "./ConnectStatus.89654d5c.js";
 import {
     _ as m
-} from "./index.5c0e1ecd.js";
+} from "./index.12198a8e.js";
 import {
     ah as o,
     o as _,
     c as f,
     V as s,
     P as n,
     a as i,
```

### Comparing `domain-admin-1.5.5/domain_admin/public/js/vendor-lib.76301fc3.js` & `domain-admin-1.5.6/domain_admin/public/js/vendor-lib.76301fc3.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/js/vendor-vue.9e61e0af.js` & `domain-admin-1.5.6/domain_admin/public/js/vendor-vue.9e61e0af.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/commit-msg.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/commit-msg.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/fsmonitor-watchman.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/fsmonitor-watchman.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-commit.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-commit.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-push.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-push.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-rebase.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-rebase.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/pre-receive.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/pre-receive.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/prepare-commit-msg.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/prepare-commit-msg.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/push-to-checkout.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/push-to-checkout.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/sendemail-validate.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/sendemail-validate.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/hooks/update.sample` & `domain-admin-1.5.6/domain_admin/public/m/.git/hooks/update.sample`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/index` & `domain-admin-1.5.6/domain_admin/public/m/.git/index`

 * *Files 24% similar despite different names*

#### Comparing `/tmp/diffoscope_jllqw4yh_/tmpzm0ltiwn_TarContainer/0/263` & `/tmp/diffoscope_jllqw4yh_/tmpfqzw_lb4_TarContainer/0/272`

```diff
@@ -5,232 +5,232 @@
 
 Path:      b'assets/common-c7dd5d89.css'
 SHA:       6105f9fd4f4b11812fcca0d2e0704e4c8dd6e7a3
 Size:      1334
 Flags:     0b11010
 User ID:   1001
 Group ID:  123
-Created:   1690018927.266340916
-Modified:  1690018927.266340916
-Inode:     291727
-Device ID: (8, 1)
+Created:   1690123055.436349260
+Modified:  1690123055.436349260
+Inode:     291743
+Device ID: (8, 17)
 
 Path:      b'assets/common.6194c42f.js'
 SHA:       b0ecf609c3df960010b6f7877bc379ea45d1e9da
 Size:      3913
 Flags:     0b11001
 User ID:   1001
 Group ID:  123
-Created:   1690018927.266340916
-Modified:  1690018927.266340916
-Inode:     291728
-Device ID: (8, 1)
+Created:   1690123055.436349260
+Modified:  1690123055.436349260
+Inode:     291744
+Device ID: (8, 17)
 
 Path:      b'assets/index-5eda257b.css'
 SHA:       8eff5bef00cd2492d9b806988ea99996d636c126
 Size:      8065
 Flags:     0b11001
 User ID:   1001
 Group ID:  123
-Created:   1690018927.266340916
-Modified:  1690018927.266340916
-Inode:     291729
-Device ID: (8, 1)
+Created:   1690123055.436349260
+Modified:  1690123055.436349260
+Inode:     291745
+Device ID: (8, 17)
 
 Path:      b'assets/index-958ae3a0.css'
 SHA:       ed50570bc6865f7dff2468d49072d7f4e4cb81d4
 Size:      3782
 Flags:     0b11001
 User ID:   1001
 Group ID:  123
-Created:   1690018927.266340916
-Modified:  1690018927.266340916
-Inode:     291730
-Device ID: (8, 1)
+Created:   1690123055.436349260
+Modified:  1690123055.436349260
+Inode:     291746
+Device ID: (8, 17)
 
 Path:      b'assets/index-9c365a03.js'
 SHA:       c8bec3f3e9b26642a8221c20a5e422bc2cada687
 Size:      379599
 Flags:     0b11000
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291731
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291747
+Device ID: (8, 17)
 
 Path:      b'assets/index-ad047368.css'
 SHA:       2d7cec3e00ed3b3b835eb233ae4bb2ea21fb5a0b
 Size:      2798
 Flags:     0b11001
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291732
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291748
+Device ID: (8, 17)
 
 Path:      b'assets/index-e8224928.css'
 SHA:       43c4fcdf29fe10c6256aa4e9cf00f534e6933efc
 Size:      5447
 Flags:     0b11001
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291733
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291749
+Device ID: (8, 17)
 
 Path:      b'assets/index-f79acb3d.css'
 SHA:       c7ef9b19427f9af9e445bb5d63231ccd58ef5b28
 Size:      53115
 Flags:     0b11001
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291734
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291750
+Device ID: (8, 17)
 
 Path:      b'assets/index.1a0d1182.js'
 SHA:       7ac4cdd0b7c56c8fe9f98aaf044df58bef26b7a5
 Size:      2028
 Flags:     0b11000
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291735
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291751
+Device ID: (8, 17)
 
 Path:      b'assets/index.1d067866.js'
 SHA:       f0a3f5a57d6bdb9961c3a56f4a992a08a0ecd671
 Size:      1512
 Flags:     0b11000
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291736
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291752
+Device ID: (8, 17)
 
 Path:      b'assets/index.daaf9893.js'
 SHA:       981e059e0de4604a5dec80930d8ff7cdf84e0006
 Size:      10416
 Flags:     0b11000
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291737
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291753
+Device ID: (8, 17)
 
 Path:      b'assets/index.feef7c0f.js'
 SHA:       7a694f3c8aca1586dc6f0e6e9e2773e207992329
 Size:      5355
 Flags:     0b11000
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291738
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291754
+Device ID: (8, 17)
 
 Path:      b'assets/login-cb9f43ad.css'
 SHA:       a9a1035a25ce05f60741e3f70716a18d93322203
 Size:      4262
 Flags:     0b11001
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291739
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291755
+Device ID: (8, 17)
 
 Path:      b'assets/pages-cert-list-cert-list.e9ecbf65.js'
 SHA:       f80169320ed23edd9889e4de7631267635bfec27
 Size:      1959
 Flags:     0b101100
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291740
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291756
+Device ID: (8, 17)
 
 Path:      b'assets/pages-domain-list-domain-list.da5e6454.js'
 SHA:       9385587145f9afbabe2aa1a489d24fd1f489e5c6
 Size:      2016
 Flags:     0b110000
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291741
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291757
+Device ID: (8, 17)
 
 Path:      b'assets/pages-login-login.09426b90.js'
 SHA:       93db3989e7874cd6b75bc0e984690ffa16666ea6
 Size:      10670
 Flags:     0b100100
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291742
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291758
+Device ID: (8, 17)
 
 Path:      b'assets/pages-user-index-user-index.d8efba8c.js'
 SHA:       4b63cfa29bd94b198d895f7a64e10c20f167e65b
 Size:      12225
 Flags:     0b101110
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291743
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291759
+Device ID: (8, 17)
 
 Path:      b'assets/uni.06dd3c8e.css'
 SHA:       c2c748e84bc4d5118b0e33d6e0073e315a36d034
 Size:      1146
 Flags:     0b10111
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291744
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291760
+Device ID: (8, 17)
 
 Path:      b'assets/user-index-be7005ab.css'
 SHA:       714dbccc412b153f5044c269745126581e3cf373
 Size:      9118
 Flags:     0b11110
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291745
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291761
+Device ID: (8, 17)
 
 Path:      b'index.html'
 SHA:       67d2a69f1213016d777c02e0c99a38871d07da5b
 Size:      835
 Flags:     0b1010
 User ID:   1001
 Group ID:  123
-Created:   1690018927.270340975
-Modified:  1690018927.270340975
-Inode:     291746
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291762
+Device ID: (8, 17)
 
 Path:      b'static/user-avatar.gif'
 SHA:       fdbd32c675f85af4ed57021ac0638a21a3c6cad3
 Size:      6334
 Flags:     0b10110
 User ID:   1001
 Group ID:  123
-Created:   1690018927.274341033
-Modified:  1690018927.274341033
-Inode:     291748
-Device ID: (8, 1)
+Created:   1690123055.440349272
+Modified:  1690123055.440349272
+Inode:     291764
+Device ID: (8, 17)
```

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/2d/7cec3e00ed3b3b835eb233ae4bb2ea21fb5a0b` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/2d/7cec3e00ed3b3b835eb233ae4bb2ea21fb5a0b`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/43/c4fcdf29fe10c6256aa4e9cf00f534e6933efc` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/43/c4fcdf29fe10c6256aa4e9cf00f534e6933efc`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/4b/63cfa29bd94b198d895f7a64e10c20f167e65b` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/4b/63cfa29bd94b198d895f7a64e10c20f167e65b`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/6f/9d23d38fd97c94c1dccf971fd7b7636cc075d2` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/6f/9d23d38fd97c94c1dccf971fd7b7636cc075d2`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/71/4dbccc412b153f5044c269745126581e3cf373` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/71/4dbccc412b153f5044c269745126581e3cf373`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/7a/694f3c8aca1586dc6f0e6e9e2773e207992329` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/7a/694f3c8aca1586dc6f0e6e9e2773e207992329`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/7a/c4cdd0b7c56c8fe9f98aaf044df58bef26b7a5` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/7a/c4cdd0b7c56c8fe9f98aaf044df58bef26b7a5`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/8e/ff5bef00cd2492d9b806988ea99996d636c126` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/8e/ff5bef00cd2492d9b806988ea99996d636c126`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/93/85587145f9afbabe2aa1a489d24fd1f489e5c6` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/93/85587145f9afbabe2aa1a489d24fd1f489e5c6`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/93/db3989e7874cd6b75bc0e984690ffa16666ea6` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/93/db3989e7874cd6b75bc0e984690ffa16666ea6`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/98/1e059e0de4604a5dec80930d8ff7cdf84e0006` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/98/1e059e0de4604a5dec80930d8ff7cdf84e0006`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/a9/a1035a25ce05f60741e3f70716a18d93322203` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/a9/a1035a25ce05f60741e3f70716a18d93322203`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/b0/ecf609c3df960010b6f7877bc379ea45d1e9da` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/b0/ecf609c3df960010b6f7877bc379ea45d1e9da`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/c7/ef9b19427f9af9e445bb5d63231ccd58ef5b28` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/c7/ef9b19427f9af9e445bb5d63231ccd58ef5b28`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/c8/bec3f3e9b26642a8221c20a5e422bc2cada687` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/c8/bec3f3e9b26642a8221c20a5e422bc2cada687`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/ed/50570bc6865f7dff2468d49072d7f4e4cb81d4` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/ed/50570bc6865f7dff2468d49072d7f4e4cb81d4`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/f0/a3f5a57d6bdb9961c3a56f4a992a08a0ecd671` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/f0/a3f5a57d6bdb9961c3a56f4a992a08a0ecd671`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/f8/0169320ed23edd9889e4de7631267635bfec27` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/f8/0169320ed23edd9889e4de7631267635bfec27`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/.git/objects/fd/bd32c675f85af4ed57021ac0638a21a3c6cad3` & `domain-admin-1.5.6/domain_admin/public/m/.git/objects/fd/bd32c675f85af4ed57021ac0638a21a3c6cad3`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/common-c7dd5d89.css` & `domain-admin-1.5.6/domain_admin/public/m/assets/common-c7dd5d89.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/common.6194c42f.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/common.6194c42f.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index-5eda257b.css` & `domain-admin-1.5.6/domain_admin/public/m/assets/index-5eda257b.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index-958ae3a0.css` & `domain-admin-1.5.6/domain_admin/public/m/assets/index-958ae3a0.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index-9c365a03.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/index-9c365a03.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index-ad047368.css` & `domain-admin-1.5.6/domain_admin/public/m/assets/index-ad047368.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index-e8224928.css` & `domain-admin-1.5.6/domain_admin/public/m/assets/index-e8224928.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index-f79acb3d.css` & `domain-admin-1.5.6/domain_admin/public/m/assets/index-f79acb3d.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index.1a0d1182.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/index.1a0d1182.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index.1d067866.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/index.1d067866.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index.daaf9893.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/index.daaf9893.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/index.feef7c0f.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/index.feef7c0f.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/login-cb9f43ad.css` & `domain-admin-1.5.6/domain_admin/public/m/assets/login-cb9f43ad.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/pages-cert-list-cert-list.e9ecbf65.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/pages-cert-list-cert-list.e9ecbf65.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/pages-domain-list-domain-list.da5e6454.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/pages-domain-list-domain-list.da5e6454.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/pages-login-login.09426b90.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/pages-login-login.09426b90.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/pages-user-index-user-index.d8efba8c.js` & `domain-admin-1.5.6/domain_admin/public/m/assets/pages-user-index-user-index.d8efba8c.js`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/uni.06dd3c8e.css` & `domain-admin-1.5.6/domain_admin/public/m/assets/uni.06dd3c8e.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/assets/user-index-be7005ab.css` & `domain-admin-1.5.6/domain_admin/public/m/assets/user-index-be7005ab.css`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/index.html` & `domain-admin-1.5.6/domain_admin/public/m/index.html`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/m/static/user-avatar.gif` & `domain-admin-1.5.6/domain_admin/public/m/static/user-avatar.gif`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/public/svg/logo.184a2d7d.svg` & `domain-admin-1.5.6/domain_admin/public/svg/logo.184a2d7d.svg`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/router/api_map.py` & `domain-admin-1.5.6/domain_admin/router/api_map.py`

 * *Files 14% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 """
 from __future__ import print_function, unicode_literals, absolute_import, division
 from domain_admin.api import (
     cert_api, ip_api, notify_api,
     whois_api, address_api,
     domain_info_api, prometheus_api,
     log_operation_api, group_user_api,
-    log_async_task_api)
+    log_async_task_api, issue_certificate_api)
 from domain_admin.api import domain_api
 from domain_admin.api import group_api
 from domain_admin.api import auth_api
 from domain_admin.api import system_api
 from domain_admin.api import user_api
 from domain_admin.api import log_scheduler_api
 
@@ -149,8 +149,14 @@
     '/api/getGroupUserById': group_user_api.get_group_user_by_id,
     '/api/getGroupUserList': group_user_api.get_group_user_list,
 
     # 异步任务日志
     '/api/getAsyncTaskLogList': log_async_task_api.get_async_task_log_list,
     '/api/clearAsyncTaskLogList': log_async_task_api.clear_async_task_log_list,
 
+    # SSL证书
+    '/api/getCertificateList': issue_certificate_api.get_certificate_list,
+    '/api/issueCertificate': issue_certificate_api.issue_certificate,
+    '/api/renewCertificate': issue_certificate_api.renew_certificate,
+    '/api/getIssueCertificateById': issue_certificate_api.get_issue_certificate_by_id,
+    '/api/verifyCertificateById': issue_certificate_api.verify_certificate,
 }
```

### Comparing `domain-admin-1.5.5/domain_admin/router/permission.py` & `domain-admin-1.5.6/domain_admin/router/permission.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/async_task_service.py` & `domain-admin-1.5.6/domain_admin/service/async_task_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/auth_service.py` & `domain-admin-1.5.6/domain_admin/service/auth_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/common_service.py` & `domain-admin-1.5.6/domain_admin/service/common_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/domain_info_service.py` & `domain-admin-1.5.6/domain_admin/service/domain_info_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/domain_service.py` & `domain-admin-1.5.6/domain_admin/service/domain_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/file_service.py` & `domain-admin-1.5.6/domain_admin/service/file_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/group_service.py` & `domain-admin-1.5.6/domain_admin/service/group_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/group_user_service.py` & `domain-admin-1.5.6/domain_admin/service/group_user_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/notify_service.py` & `domain-admin-1.5.6/domain_admin/service/notify_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/operation_service.py` & `domain-admin-1.5.6/domain_admin/service/operation_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/scheduler_service.py` & `domain-admin-1.5.6/domain_admin/service/scheduler_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/system_service.py` & `domain-admin-1.5.6/domain_admin/service/system_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/token_service.py` & `domain-admin-1.5.6/domain_admin/service/token_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/service/version_service.py` & `domain-admin-1.5.6/domain_admin/service/version_service.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/bcrypt_util.py` & `domain-admin-1.5.6/domain_admin/utils/bcrypt_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/cert_util/cert_common.py` & `domain-admin-1.5.6/domain_admin/utils/cert_util/cert_common.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/cert_util/cert_openssl_v2.py` & `domain-admin-1.5.6/domain_admin/utils/cert_util/cert_openssl_v2.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/cert_util/cert_socket.py` & `domain-admin-1.5.6/domain_admin/utils/cert_util/cert_socket.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/cert_util/cert_socket_v2.py` & `domain-admin-1.5.6/domain_admin/utils/cert_util/cert_socket_v2.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/datetime_util.py` & `domain-admin-1.5.6/domain_admin/utils/datetime_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/domain_util.py` & `domain-admin-1.5.6/domain_admin/utils/domain_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/email_util.py` & `domain-admin-1.5.6/domain_admin/utils/email_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/flask_ext/api_result.py` & `domain-admin-1.5.6/domain_admin/utils/flask_ext/api_result.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/flask_ext/app_exception.py` & `domain-admin-1.5.6/domain_admin/utils/flask_ext/app_exception.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/flask_ext/flask_app.py` & `domain-admin-1.5.6/domain_admin/utils/flask_ext/flask_app.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/flask_ext/handler.py` & `domain-admin-1.5.6/domain_admin/utils/flask_ext/handler.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/flask_ext/json/default.py` & `domain-admin-1.5.6/domain_admin/utils/flask_ext/json/default.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/flask_ext/json/json_encoder.py` & `domain-admin-1.5.6/domain_admin/utils/flask_ext/json/json_encoder.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/flask_ext/json/json_provider.py` & `domain-admin-1.5.6/domain_admin/utils/flask_ext/json/json_provider.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/icp_util.py` & `domain-admin-1.5.6/domain_admin/utils/icp_util.py`

 * *Files 1% similar despite different names*

```diff
@@ -23,15 +23,15 @@
             'name': self.name,
             'icp': self.icp,
         }
 
 
 def get_icp_from_qq(domain):
     """
-    接口由网友提供
+    接口由网友 @因为遇见你 提供
     :param domain:
     :return:
 
     ({
         "data": {
             "retcode": 0,
             "results": {
```

### Comparing `domain-admin-1.5.5/domain_admin/utils/ip_util.py` & `domain-admin-1.5.6/domain_admin/utils/ip_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/json_util.py` & `domain-admin-1.5.6/domain_admin/utils/json_util.py`

 * *Files 10% similar despite different names*

```diff
@@ -37,7 +37,11 @@
     json序列化
     :param data:
     :param default:
     :param kwargs:
     :return:
     """
     return json.dumps(data, default=default, **kwargs)
+
+
+def json_dump(obj):
+    print(json_encode(obj, ensure_ascii=False, indent=2))
```

### Comparing `domain-admin-1.5.5/domain_admin/utils/open_api/crtsh_api.py` & `domain-admin-1.5.6/domain_admin/utils/open_api/crtsh_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/open_api/ding_talk_api.py` & `domain-admin-1.5.6/domain_admin/utils/open_api/ding_talk_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/open_api/feishu_api.py` & `domain-admin-1.5.6/domain_admin/utils/open_api/feishu_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/open_api/work_weixin_api.py` & `domain-admin-1.5.6/domain_admin/utils/open_api/work_weixin_api.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/peewee_ext/model_util.py` & `domain-admin-1.5.6/domain_admin/utils/peewee_ext/model_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/secret_util.py` & `domain-admin-1.5.6/domain_admin/utils/secret_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/text_util.py` & `domain-admin-1.5.6/domain_admin/utils/text_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/time_util.py` & `domain-admin-1.5.6/domain_admin/utils/time_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/whois_util/config.py` & `domain-admin-1.5.6/domain_admin/utils/whois_util/config.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/whois_util/util.py` & `domain-admin-1.5.6/domain_admin/utils/whois_util/util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/whois_util/whois-servers.txt` & `domain-admin-1.5.6/domain_admin/utils/whois_util/whois-servers.txt`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin/utils/whois_util/whois_util.py` & `domain-admin-1.5.6/domain_admin/utils/whois_util/whois_util.py`

 * *Files identical despite different names*

### Comparing `domain-admin-1.5.5/domain_admin.egg-info/PKG-INFO` & `domain-admin-1.5.6/domain_admin.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: domain-admin
-Version: 1.5.5
+Version: 1.5.6
 Summary: a domain ssl cert admin
 Home-page: https://github.com/mouday/domain-admin
 Author: Peng Shiyu
 Author-email: pengshiyuyx@gmail.com
 License: MIT
 Keywords: domain,ssl,cert,web,monitor
 Platform: any
```

### Comparing `domain-admin-1.5.5/domain_admin.egg-info/SOURCES.txt` & `domain-admin-1.5.6/domain_admin.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -18,14 +18,15 @@
 domain_admin/api/auth_api.py
 domain_admin/api/cert_api.py
 domain_admin/api/domain_api.py
 domain_admin/api/domain_info_api.py
 domain_admin/api/group_api.py
 domain_admin/api/group_user_api.py
 domain_admin/api/ip_api.py
+domain_admin/api/issue_certificate_api.py
 domain_admin/api/log_async_task_api.py
 domain_admin/api/log_operation_api.py
 domain_admin/api/log_scheduler_api.py
 domain_admin/api/notify_api.py
 domain_admin/api/prometheus_api.py
 domain_admin/api/system_api.py
 domain_admin/api/user_api.py
@@ -61,14 +62,15 @@
 domain_admin/model/address_model.py
 domain_admin/model/base_model.py
 domain_admin/model/database.py
 domain_admin/model/domain_info_model.py
 domain_admin/model/domain_model.py
 domain_admin/model/group_model.py
 domain_admin/model/group_user_model.py
+domain_admin/model/issue_certificate_model.py
 domain_admin/model/log_async_task_model.py
 domain_admin/model/log_operation_model.py
 domain_admin/model/log_scheduler_model.py
 domain_admin/model/notify_model.py
 domain_admin/model/system_model.py
 domain_admin/model/user_model.py
 domain_admin/model/version_model.py
@@ -94,94 +96,98 @@
 domain_admin/public/.git/hooks/push-to-checkout.sample
 domain_admin/public/.git/hooks/sendemail-validate.sample
 domain_admin/public/.git/hooks/update.sample
 domain_admin/public/.git/info/exclude
 domain_admin/public/.git/logs/HEAD
 domain_admin/public/.git/logs/refs/heads/dist
 domain_admin/public/.git/logs/refs/remotes/origin/dist
+domain_admin/public/.git/objects/01/9bb44cfca57b7aa35ea7f5b6f99c3ef48e8d8f
 domain_admin/public/.git/objects/19/7f5cf73cf11d43d915904e0d8aad4736a77d63
+domain_admin/public/.git/objects/1e/270d8f3cc5167242582434675642b5858ba482
 domain_admin/public/.git/objects/21/00bd7d2219a26827cc80aa37fe72fcb303bb50
-domain_admin/public/.git/objects/24/103afc71807fa9124dac4bacf6c71aea125714
+domain_admin/public/.git/objects/30/0478ea1f19f5a14d6a7167e9f71f5848707d76
 domain_admin/public/.git/objects/3c/0f2e923566dc74d04e67d46d8b722923ed1949
 domain_admin/public/.git/objects/3c/2434ab20d756f0a95ad24f6a5adb7e1219a7d1
-domain_admin/public/.git/objects/40/c3b0a033be485b3c7e9d536a1b3a277818cb82
-domain_admin/public/.git/objects/46/3ce0aa01de3b64fe18ece210e1570817c51008
-domain_admin/public/.git/objects/51/ec8afb4a5571f29776853cff34b9084b989be8
+domain_admin/public/.git/objects/40/03c2e07280d146ee3443587c38ea2d264c07ca
+domain_admin/public/.git/objects/50/c771a9bca6f87a2fb3381719fe0622eeae23bf
 domain_admin/public/.git/objects/52/c1926de72b181c9b7faf597fb8f71f48565462
+domain_admin/public/.git/objects/53/0864cbe282ec11e8564a8a3ce33756977d59ee
 domain_admin/public/.git/objects/55/1103b11c4b699a3b4107d3a2ab173dfe238556
-domain_admin/public/.git/objects/58/0919cf9322c635814fe723901eff5bc75ae450
-domain_admin/public/.git/objects/5d/c222fd0913296f5d22a6d502848bc46e27cfbb
-domain_admin/public/.git/objects/5d/c54416f168ceb328978b483f7568ef176ab9ea
+domain_admin/public/.git/objects/58/1d5e80145e76e2ba0d08b038e1a2fefebef3bb
 domain_admin/public/.git/objects/5f/a7faf700c98850aa96022ab07af6a07b854f34
 domain_admin/public/.git/objects/69/a9dda41cf39bb60d1dc5b1158ffba197580b6a
 domain_admin/public/.git/objects/6c/3e3059f9ec00c015681abca34b751c3439513d
 domain_admin/public/.git/objects/6d/15191314c9b832ac41056a30bf0bf6533a29dc
-domain_admin/public/.git/objects/6e/25fd629c25bce876fa6e3d55f3d44ffc7403df
-domain_admin/public/.git/objects/6f/931c679b6da636cbb9ae74fbb156ec8588aacd
-domain_admin/public/.git/objects/76/a77330292710a039cca1dabd8301893a8e5c20
+domain_admin/public/.git/objects/77/bb86f804268cc8045d2cd2547ec17c22a0d166
 domain_admin/public/.git/objects/79/404c2464172f80b414d111f49718327b3ef93b
-domain_admin/public/.git/objects/7c/ffb379a2e31f7ecbc681d3e6a2988313d68c14
 domain_admin/public/.git/objects/7f/64d8af0501887e805dc9ccf8228f4fb5e73fdb
-domain_admin/public/.git/objects/83/52bc71914e2d52dc5b8b5f432baed8fdb3a5b3
 domain_admin/public/.git/objects/89/0f3ed83973272c63b56a722a88fe25160d11d2
 domain_admin/public/.git/objects/8c/f880f5a9481ef71cd22e08d59e7d366775b360
+domain_admin/public/.git/objects/90/4a4570929957b2678d3c499a9cd83658a6675e
+domain_admin/public/.git/objects/91/dcfad5270425be228e01a34e9c9b11ef3a0c4e
 domain_admin/public/.git/objects/92/cfface0a460c51331fb8f25083a09948e00cbf
+domain_admin/public/.git/objects/93/522d98a7fe61eb676e55f33d92d8d090b967e4
 domain_admin/public/.git/objects/95/f07af46d709638b20c0b2c66cdf6de8e89a7e4
-domain_admin/public/.git/objects/99/3174c206a21af6cacdc5834848444e2e5e20f4
-domain_admin/public/.git/objects/aa/fb811a89caf497ae4598dda6ada91378dc70d3
-domain_admin/public/.git/objects/b2/09e1e91fe0262794771b8d69d85d8d6bcab9f6
+domain_admin/public/.git/objects/a0/e9b4ee6e91d304066df26b1bc6218de181c2c2
+domain_admin/public/.git/objects/a2/86b0b36b3538d177580f0c25e8e3a3a9f007b7
+domain_admin/public/.git/objects/ab/2ba13bd2bd0cbf3e5b764ff0a29fd5872380c5
+domain_admin/public/.git/objects/b1/115cb42fa8938fe1dbebccc9584aa03a895df0
 domain_admin/public/.git/objects/b3/1cb2667f48424e34cf9517362eadf899f704ad
+domain_admin/public/.git/objects/bb/ecd10fc84228b6f4a1c2e0c90e2b68d4aa6bf2
+domain_admin/public/.git/objects/c0/76a86e24db79ccf75f79903b19cf145419d4bf
+domain_admin/public/.git/objects/c1/ff198374b288725eab95bc1294e1f04fe5c561
 domain_admin/public/.git/objects/c4/c46ae2c464a49661d7793709077759039f0b5e
-domain_admin/public/.git/objects/c9/55b903bc1c5de030fc58f36fd2ebf22ff6ac6d
 domain_admin/public/.git/objects/cc/bfeaa0b21986ed309cbb83d17585b54f3b2fb9
-domain_admin/public/.git/objects/d3/8d6c402e90bd375d028a0c70d3091cb2779e39
-domain_admin/public/.git/objects/dc/8bf2242bff0c8ee207b31910dda7a0463858df
+domain_admin/public/.git/objects/ce/dcd8ba4511fabecdc11df81e55d82ca8b96ca3
+domain_admin/public/.git/objects/cf/1eea719ca3a291ef7edaa6c60eaa808ca6e4ae
+domain_admin/public/.git/objects/d4/9eb5d776f5b92a02189cebbe590f76db9575bd
+domain_admin/public/.git/objects/d8/1e4838c9ac36863e037e68a2f3552f736c5c8f
 domain_admin/public/.git/objects/e1/13bfd922675ce50e68cdf88cd94d16130ad58b
-domain_admin/public/.git/objects/e1/f93ffe54644c9baa5e1bc6b9711a08bfba7750
-domain_admin/public/.git/objects/e4/56acd4f47f8661930733f5db393527f36e631b
-domain_admin/public/.git/objects/ef/6235d671af0b6113d18b3e63a1fa2fe30ea9bd
-domain_admin/public/.git/objects/f0/5cb009efc03174da02974c45dfeac8fb5486ff
-domain_admin/public/.git/objects/fa/21601143ca66f766b9a994751adc37796b2455
+domain_admin/public/.git/objects/e4/c5465d396f947d57739ed8266597d6a47ef51b
+domain_admin/public/.git/objects/e6/72b6afc2744b043e6fbdf3031eb086a109ec3c
+domain_admin/public/.git/objects/e6/e5ddee110d6ed47cbb0a4f30db3d055efd21da
 domain_admin/public/.git/objects/fd/bd32c675f85af4ed57021ac0638a21a3c6cad3
 domain_admin/public/.git/objects/ff/9c65dfdc7a16150c07745e0030a9d6373920cd
 domain_admin/public/.git/refs/heads/dist
 domain_admin/public/.git/refs/remotes/origin/dist
 domain_admin/public/css/ConditionFilterGroup.a91875e6.css
 domain_admin/public/css/index.302e10d7.css
 domain_admin/public/css/index.69a97337.css
+domain_admin/public/css/index.75ef7015.css
 domain_admin/public/css/index.a676cc2e.css
 domain_admin/public/css/index.b285e10a.css
 domain_admin/public/css/index.cf805e1c.css
 domain_admin/public/css/index.d028ae37.css
 domain_admin/public/gif/user-avatar.ea67286d.gif
 domain_admin/public/jpg/chatpet-white.10f4f36c.jpg
 domain_admin/public/jpg/chatpet.fce5580e.jpg
-domain_admin/public/js/ConditionFilterGroup.cc953e5c.js
-domain_admin/public/js/ConnectStatus.b87d1fee.js
-domain_admin/public/js/SearchUser.1ba54ef6.js
-domain_admin/public/js/SelectGroup.0ff8c614.js
+domain_admin/public/js/ConditionFilterGroup.340936f7.js
+domain_admin/public/js/ConnectStatus.89654d5c.js
+domain_admin/public/js/SearchUser.983b7494.js
+domain_admin/public/js/SelectGroup.d7e6e540.js
 domain_admin/public/js/codemirror-lib.a3a39aa0.js
 domain_admin/public/js/element-icon.1ce1c350.js
 domain_admin/public/js/element-plus.30eb1cab.js
 domain_admin/public/js/event-enums.6c6f25e7.js
 domain_admin/public/js/highlight-lib.3654f6d3.js
-domain_admin/public/js/index.0a173b97.js
-domain_admin/public/js/index.2a4ae78d.js
-domain_admin/public/js/index.2d5be753.js
-domain_admin/public/js/index.51ecb744.js
-domain_admin/public/js/index.53934399.js
-domain_admin/public/js/index.58c30995.js
-domain_admin/public/js/index.5c0e1ecd.js
-domain_admin/public/js/index.7089425b.js
-domain_admin/public/js/index.87e9fadd.js
-domain_admin/public/js/index.a747af4a.js
-domain_admin/public/js/index.b77111ba.js
-domain_admin/public/js/index.d21190a6.js
-domain_admin/public/js/index.df8aa1f7.js
-domain_admin/public/js/index.edfe11bc.js
+domain_admin/public/js/index.075c6a16.js
+domain_admin/public/js/index.12198a8e.js
+domain_admin/public/js/index.127485d4.js
+domain_admin/public/js/index.16184f42.js
+domain_admin/public/js/index.2e3ad8c8.js
+domain_admin/public/js/index.34096d0f.js
+domain_admin/public/js/index.4704b0d3.js
+domain_admin/public/js/index.51aeadc3.js
+domain_admin/public/js/index.58059e0f.js
+domain_admin/public/js/index.86cef4dd.js
+domain_admin/public/js/index.a3947126.js
+domain_admin/public/js/index.ab38e8b8.js
+domain_admin/public/js/index.b84878f9.js
+domain_admin/public/js/index.c05aa8e8.js
+domain_admin/public/js/index.c512b8f1.js
 domain_admin/public/js/vendor-lib.76301fc3.js
 domain_admin/public/js/vendor-vue.9e61e0af.js
 domain_admin/public/m/index.html
 domain_admin/public/m/.git/FETCH_HEAD
 domain_admin/public/m/.git/HEAD
 domain_admin/public/m/.git/config
 domain_admin/public/m/.git/description
@@ -261,14 +267,15 @@
 domain_admin/service/auth_service.py
 domain_admin/service/common_service.py
 domain_admin/service/domain_info_service.py
 domain_admin/service/domain_service.py
 domain_admin/service/file_service.py
 domain_admin/service/group_service.py
 domain_admin/service/group_user_service.py
+domain_admin/service/issue_certificate_service.py
 domain_admin/service/notify_service.py
 domain_admin/service/operation_service.py
 domain_admin/service/render_service.py
 domain_admin/service/scheduler_service.py
 domain_admin/service/system_service.py
 domain_admin/service/token_service.py
 domain_admin/service/version_service.py
@@ -285,14 +292,16 @@
 domain_admin/utils/icp_util.py
 domain_admin/utils/ip_util.py
 domain_admin/utils/json_util.py
 domain_admin/utils/md5_util.py
 domain_admin/utils/secret_util.py
 domain_admin/utils/text_util.py
 domain_admin/utils/time_util.py
+domain_admin/utils/acme_util/__init__.py
+domain_admin/utils/acme_util/acme_v2_api.py
 domain_admin/utils/cert_util/__init__.py
 domain_admin/utils/cert_util/cert_common.py
 domain_admin/utils/cert_util/cert_consts.py
 domain_admin/utils/cert_util/cert_info.py
 domain_admin/utils/cert_util/cert_openssl_v2.py
 domain_admin/utils/cert_util/cert_socket.py
 domain_admin/utils/cert_util/cert_socket_v2.py
```

### Comparing `domain-admin-1.5.5/setup.py` & `domain-admin-1.5.6/setup.py`

 * *Files identical despite different names*

