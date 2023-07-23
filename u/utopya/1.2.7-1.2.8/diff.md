# Comparing `tmp/utopya-1.2.7.tar.gz` & `tmp/utopya-1.2.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "utopya-1.2.7.tar", last modified: Mon Jul 10 08:52:54 2023, max compression
+gzip compressed data, was "utopya-1.2.8.tar", last modified: Sun Jul 23 15:43:53 2023, max compression
```

## Comparing `utopya-1.2.7.tar` & `utopya-1.2.8.tar`

### file list

```diff
@@ -1,128 +1,128 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.576851 utopya-1.2.7/
--rw-rw-rw-   0 root         (0) root         (0)    35149 2023-07-10 08:52:43.000000 utopya-1.2.7/COPYING
--rw-rw-rw-   0 root         (0) root         (0)     7633 2023-07-10 08:52:43.000000 utopya-1.2.7/COPYING.LESSER
--rw-r--r--   0 root         (0) root         (0)     3168 2023-07-10 08:52:54.576851 utopya-1.2.7/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)     5594 2023-07-10 08:52:43.000000 utopya-1.2.7/README.md
--rw-rw-rw-   0 root         (0) root         (0)     1734 2023-07-10 08:52:43.000000 utopya-1.2.7/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-07-10 08:52:54.577850 utopya-1.2.7/setup.cfg
--rw-rw-rw-   0 root         (0) root         (0)     5813 2023-07-10 08:52:43.000000 utopya-1.2.7/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.558850 utopya-1.2.7/tests/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.560850 utopya-1.2.7/tests/_gen_figures/
--rw-rw-rw-   0 root         (0) root         (0)      560 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/_gen_figures/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)       50 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/_gen_figures/_utils.py
--rw-rw-rw-   0 root         (0) root         (0)     5271 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/_gen_figures/test_plots.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.561850 utopya-1.2.7/tests/backend/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/backend/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     8239 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/backend/test_benchmark.py
--rw-rw-rw-   0 root         (0) root         (0)    10242 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/backend/test_model.py
--rw-rw-rw-   0 root         (0) root         (0)     2898 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/backend/test_tools.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.562850 utopya-1.2.7/tests/cli/
--rw-rw-rw-   0 root         (0) root         (0)      193 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/cli/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     2844 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/cli/test__shell_complete.py
--rw-rw-rw-   0 root         (0) root         (0)     2810 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/cli/test__to_migrate.py
--rw-rw-rw-   0 root         (0) root         (0)      914 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/cli/test_batch.py
--rw-rw-rw-   0 root         (0) root         (0)     4804 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/cli/test_config.py
--rw-rw-rw-   0 root         (0) root         (0)    15337 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/cli/test_models.py
--rw-rw-rw-   0 root         (0) root         (0)     6940 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/cli/test_projects.py
--rw-rw-rw-   0 root         (0) root         (0)     2019 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/cli/test_run_and_eval.py
--rw-rw-rw-   0 root         (0) root         (0)     2477 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/cli/test_test.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.563850 utopya-1.2.7/tests/eval/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/eval/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     9145 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/eval/test_containers.py
--rw-rw-rw-   0 root         (0) root         (0)     6607 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/eval/test_datamanager.py
--rw-rw-rw-   0 root         (0) root         (0)     2975 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/eval/test_groups.py
--rw-rw-rw-   0 root         (0) root         (0)     6444 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/eval/test_plot_utils.py
--rw-rw-rw-   0 root         (0) root         (0)    45377 2023-07-10 08:52:43.000000 utopya-1.2.7/tests/eval/test_plotting.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.567850 utopya-1.2.7/utopya/
--rw-rw-rw-   0 root         (0) root         (0)     3255 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     3340 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/_cluster.py
--rw-rw-rw-   0 root         (0) root         (0)      704 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/_import_tools.py
--rw-rw-rw-   0 root         (0) root         (0)      249 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/_signal.py
--rw-rw-rw-   0 root         (0) root         (0)      225 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/_yaml.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.568850 utopya-1.2.7/utopya/_yaml_registry/
--rw-rw-rw-   0 root         (0) root         (0)      135 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/_yaml_registry/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     9532 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/_yaml_registry/entry.py
--rw-rw-rw-   0 root         (0) root         (0)    10253 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/_yaml_registry/registry.py
--rw-rw-rw-   0 root         (0) root         (0)    18565 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/batch.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.569850 utopya-1.2.7/utopya/cfg/
--rw-rw-rw-   0 root         (0) root         (0)    20229 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/cfg/base_cfg.yml
--rw-rw-rw-   0 root         (0) root         (0)    13771 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/cfg/base_plots.yml
--rw-rw-rw-   0 root         (0) root         (0)     8757 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/cfg/btm_cfg.yml
--rw-rw-rw-   0 root         (0) root         (0)      339 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/cfg/user_cfg_header.yml
--rw-rw-rw-   0 root         (0) root         (0)     2939 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/cfg.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.570850 utopya-1.2.7/utopya/eval/
--rw-rw-rw-   0 root         (0) root         (0)      480 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     6936 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/_plot_func_resolver.py
--rw-rw-rw-   0 root         (0) root         (0)    16707 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/containers.py
--rw-rw-rw-   0 root         (0) root         (0)     1311 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/data_ops.py
--rw-rw-rw-   0 root         (0) root         (0)     3079 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/datamanager.py
--rw-rw-rw-   0 root         (0) root         (0)     2507 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/groups.py
--rw-rw-rw-   0 root         (0) root         (0)     1623 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plotcreators.py
--rw-rw-rw-   0 root         (0) root         (0)      853 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plothelper.py
--rw-rw-rw-   0 root         (0) root         (0)     9048 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plotmanager.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.572850 utopya-1.2.7/utopya/eval/plots/
--rw-rw-rw-   0 root         (0) root         (0)      445 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     7502 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/_attractor.py
--rw-rw-rw-   0 root         (0) root         (0)    72723 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/_graph.py
--rw-rw-rw-   0 root         (0) root         (0)     1789 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/_mpl.py
--rw-rw-rw-   0 root         (0) root         (0)    12091 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/_utils.py
--rw-rw-rw-   0 root         (0) root         (0)    58799 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/abm.py
--rw-rw-rw-   0 root         (0) root         (0)    25571 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/attractor.py
--rw-rw-rw-   0 root         (0) root         (0)    62459 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/ca.py
--rw-rw-rw-   0 root         (0) root         (0)     6924 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/distributions.py
--rw-rw-rw-   0 root         (0) root         (0)    24529 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/graph.py
--rw-rw-rw-   0 root         (0) root         (0)     9451 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/snsplot.py
--rw-rw-rw-   0 root         (0) root         (0)     3193 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/plots/time_series.py
--rw-rw-rw-   0 root         (0) root         (0)     2265 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/eval/transform.py
--rw-rw-rw-   0 root         (0) root         (0)     3623 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/exceptions.py
--rw-rw-rw-   0 root         (0) root         (0)    23144 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/model.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.573850 utopya-1.2.7/utopya/model_registry/
--rw-rw-rw-   0 root         (0) root         (0)      659 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/model_registry/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     3494 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/model_registry/_registration.py
--rw-rw-rw-   0 root         (0) root         (0)    16777 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/model_registry/entry.py
--rw-rw-rw-   0 root         (0) root         (0)    15927 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/model_registry/info_bundle.py
--rw-rw-rw-   0 root         (0) root         (0)    11936 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/model_registry/registry.py
--rw-rw-rw-   0 root         (0) root         (0)     3635 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/model_registry/utils.py
--rw-rw-rw-   0 root         (0) root         (0)    70544 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/multiverse.py
--rw-rw-rw-   0 root         (0) root         (0)    19695 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/parameter.py
--rw-rw-rw-   0 root         (0) root         (0)      674 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/plotting.py
--rw-rw-rw-   0 root         (0) root         (0)    12297 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/project_registry.py
--rw-rw-rw-   0 root         (0) root         (0)    54018 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/reporter.py
--rw-rw-rw-   0 root         (0) root         (0)    13652 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/stop_conditions.py
--rw-rw-rw-   0 root         (0) root         (0)    52862 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/task.py
--rw-rw-rw-   0 root         (0) root         (0)     1835 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/testtools.py
--rw-rw-rw-   0 root         (0) root         (0)     9031 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/tools.py
--rw-rw-rw-   0 root         (0) root         (0)    41450 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/workermanager.py
--rw-rw-rw-   0 root         (0) root         (0)     5421 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya/yaml.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.568850 utopya-1.2.7/utopya.egg-info/
--rw-r--r--   0 root         (0) root         (0)     3168 2023-07-10 08:52:54.000000 utopya-1.2.7/utopya.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     2762 2023-07-10 08:52:54.000000 utopya-1.2.7/utopya.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-07-10 08:52:54.000000 utopya-1.2.7/utopya.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       46 2023-07-10 08:52:54.000000 utopya-1.2.7/utopya.egg-info/entry_points.txt
--rw-r--r--   0 root         (0) root         (0)      493 2023-07-10 08:52:54.000000 utopya-1.2.7/utopya.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       39 2023-07-10 08:52:54.000000 utopya-1.2.7/utopya.egg-info/top_level.txt
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.574850 utopya-1.2.7/utopya_backend/
--rw-rw-rw-   0 root         (0) root         (0)      460 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_backend/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    17418 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_backend/benchmark.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.574850 utopya-1.2.7/utopya_backend/io/
--rw-rw-rw-   0 root         (0) root         (0)       63 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_backend/io/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1504 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_backend/logging.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.574850 utopya-1.2.7/utopya_backend/model/
--rw-rw-rw-   0 root         (0) root         (0)      512 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_backend/model/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    18987 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_backend/model/base.py
--rw-rw-rw-   0 root         (0) root         (0)     8082 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_backend/model/step.py
--rw-rw-rw-   0 root         (0) root         (0)     1619 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_backend/signal.py
--rw-rw-rw-   0 root         (0) root         (0)     5411 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_backend/tools.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-10 08:52:54.576851 utopya-1.2.7/utopya_cli/
--rw-rw-rw-   0 root         (0) root         (0)       66 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    18051 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/_copy_model.py
--rw-rw-rw-   0 root         (0) root         (0)     9861 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/_shared.py
--rw-rw-rw-   0 root         (0) root         (0)    15347 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/_utils.py
--rw-rw-rw-   0 root         (0) root         (0)     1644 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/batch.py
--rw-rw-rw-   0 root         (0) root         (0)     1382 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/cli.py
--rw-rw-rw-   0 root         (0) root         (0)     5722 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/config.py
--rw-rw-rw-   0 root         (0) root         (0)    17744 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/eval.py
--rw-rw-rw-   0 root         (0) root         (0)    24141 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/models.py
--rw-rw-rw-   0 root         (0) root         (0)     7872 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/projects.py
--rw-rw-rw-   0 root         (0) root         (0)     6753 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/run.py
--rw-rw-rw-   0 root         (0) root         (0)     2627 2023-07-10 08:52:43.000000 utopya-1.2.7/utopya_cli/test.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.331644 utopya-1.2.8/
+-rw-rw-rw-   0 root         (0) root         (0)    35149 2023-07-23 15:43:42.000000 utopya-1.2.8/COPYING
+-rw-rw-rw-   0 root         (0) root         (0)     7633 2023-07-23 15:43:42.000000 utopya-1.2.8/COPYING.LESSER
+-rw-r--r--   0 root         (0) root         (0)     3168 2023-07-23 15:43:53.331644 utopya-1.2.8/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)     5594 2023-07-23 15:43:42.000000 utopya-1.2.8/README.md
+-rw-rw-rw-   0 root         (0) root         (0)     1734 2023-07-23 15:43:42.000000 utopya-1.2.8/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-07-23 15:43:53.331644 utopya-1.2.8/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)     5842 2023-07-23 15:43:42.000000 utopya-1.2.8/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.311644 utopya-1.2.8/tests/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.313645 utopya-1.2.8/tests/_gen_figures/
+-rw-rw-rw-   0 root         (0) root         (0)      560 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/_gen_figures/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)       50 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/_gen_figures/_utils.py
+-rw-rw-rw-   0 root         (0) root         (0)     5271 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/_gen_figures/test_plots.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.314644 utopya-1.2.8/tests/backend/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/backend/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     8239 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/backend/test_benchmark.py
+-rw-rw-rw-   0 root         (0) root         (0)    12007 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/backend/test_model.py
+-rw-rw-rw-   0 root         (0) root         (0)     2898 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/backend/test_tools.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.316644 utopya-1.2.8/tests/cli/
+-rw-rw-rw-   0 root         (0) root         (0)      193 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/cli/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     2844 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/cli/test__shell_complete.py
+-rw-rw-rw-   0 root         (0) root         (0)     2810 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/cli/test__to_migrate.py
+-rw-rw-rw-   0 root         (0) root         (0)      914 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/cli/test_batch.py
+-rw-rw-rw-   0 root         (0) root         (0)     4804 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/cli/test_config.py
+-rw-rw-rw-   0 root         (0) root         (0)    15337 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/cli/test_models.py
+-rw-rw-rw-   0 root         (0) root         (0)     6940 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/cli/test_projects.py
+-rw-rw-rw-   0 root         (0) root         (0)     2019 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/cli/test_run_and_eval.py
+-rw-rw-rw-   0 root         (0) root         (0)     2477 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/cli/test_test.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.317644 utopya-1.2.8/tests/eval/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/eval/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     9145 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/eval/test_containers.py
+-rw-rw-rw-   0 root         (0) root         (0)     6607 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/eval/test_datamanager.py
+-rw-rw-rw-   0 root         (0) root         (0)     2975 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/eval/test_groups.py
+-rw-rw-rw-   0 root         (0) root         (0)     6444 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/eval/test_plot_utils.py
+-rw-rw-rw-   0 root         (0) root         (0)    45377 2023-07-23 15:43:42.000000 utopya-1.2.8/tests/eval/test_plotting.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.321644 utopya-1.2.8/utopya/
+-rw-rw-rw-   0 root         (0) root         (0)     3255 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     3340 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/_cluster.py
+-rw-rw-rw-   0 root         (0) root         (0)      704 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/_import_tools.py
+-rw-rw-rw-   0 root         (0) root         (0)      249 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/_signal.py
+-rw-rw-rw-   0 root         (0) root         (0)      169 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/_yaml.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.322644 utopya-1.2.8/utopya/_yaml_registry/
+-rw-rw-rw-   0 root         (0) root         (0)      135 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/_yaml_registry/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     9532 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/_yaml_registry/entry.py
+-rw-rw-rw-   0 root         (0) root         (0)    10253 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/_yaml_registry/registry.py
+-rw-rw-rw-   0 root         (0) root         (0)    18565 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/batch.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.323644 utopya-1.2.8/utopya/cfg/
+-rw-rw-rw-   0 root         (0) root         (0)    20229 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/cfg/base_cfg.yml
+-rw-rw-rw-   0 root         (0) root         (0)    13771 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/cfg/base_plots.yml
+-rw-rw-rw-   0 root         (0) root         (0)     8757 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/cfg/btm_cfg.yml
+-rw-rw-rw-   0 root         (0) root         (0)      339 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/cfg/user_cfg_header.yml
+-rw-rw-rw-   0 root         (0) root         (0)     2939 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/cfg.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.324644 utopya-1.2.8/utopya/eval/
+-rw-rw-rw-   0 root         (0) root         (0)      480 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     6936 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/_plot_func_resolver.py
+-rw-rw-rw-   0 root         (0) root         (0)    16707 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/containers.py
+-rw-rw-rw-   0 root         (0) root         (0)     1311 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/data_ops.py
+-rw-rw-rw-   0 root         (0) root         (0)     3079 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/datamanager.py
+-rw-rw-rw-   0 root         (0) root         (0)     2507 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/groups.py
+-rw-rw-rw-   0 root         (0) root         (0)     1623 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plotcreators.py
+-rw-rw-rw-   0 root         (0) root         (0)      853 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plothelper.py
+-rw-rw-rw-   0 root         (0) root         (0)     9048 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plotmanager.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.326644 utopya-1.2.8/utopya/eval/plots/
+-rw-rw-rw-   0 root         (0) root         (0)      445 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     7502 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/_attractor.py
+-rw-rw-rw-   0 root         (0) root         (0)    72723 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/_graph.py
+-rw-rw-rw-   0 root         (0) root         (0)     1789 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/_mpl.py
+-rw-rw-rw-   0 root         (0) root         (0)    12091 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/_utils.py
+-rw-rw-rw-   0 root         (0) root         (0)    58799 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/abm.py
+-rw-rw-rw-   0 root         (0) root         (0)    25571 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/attractor.py
+-rw-rw-rw-   0 root         (0) root         (0)    62459 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/ca.py
+-rw-rw-rw-   0 root         (0) root         (0)     6924 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/distributions.py
+-rw-rw-rw-   0 root         (0) root         (0)    24529 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/graph.py
+-rw-rw-rw-   0 root         (0) root         (0)     9451 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/snsplot.py
+-rw-rw-rw-   0 root         (0) root         (0)     3193 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/plots/time_series.py
+-rw-rw-rw-   0 root         (0) root         (0)     2265 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/eval/transform.py
+-rw-rw-rw-   0 root         (0) root         (0)     3623 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/exceptions.py
+-rw-rw-rw-   0 root         (0) root         (0)    23144 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/model.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.327644 utopya-1.2.8/utopya/model_registry/
+-rw-rw-rw-   0 root         (0) root         (0)      659 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/model_registry/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     3494 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/model_registry/_registration.py
+-rw-rw-rw-   0 root         (0) root         (0)    16777 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/model_registry/entry.py
+-rw-rw-rw-   0 root         (0) root         (0)    15927 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/model_registry/info_bundle.py
+-rw-rw-rw-   0 root         (0) root         (0)    11936 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/model_registry/registry.py
+-rw-rw-rw-   0 root         (0) root         (0)     3635 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/model_registry/utils.py
+-rw-rw-rw-   0 root         (0) root         (0)    70544 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/multiverse.py
+-rw-rw-rw-   0 root         (0) root         (0)    19695 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/parameter.py
+-rw-rw-rw-   0 root         (0) root         (0)      674 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/plotting.py
+-rw-rw-rw-   0 root         (0) root         (0)    12297 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/project_registry.py
+-rw-rw-rw-   0 root         (0) root         (0)    54018 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/reporter.py
+-rw-rw-rw-   0 root         (0) root         (0)    13652 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/stop_conditions.py
+-rw-rw-rw-   0 root         (0) root         (0)    52862 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/task.py
+-rw-rw-rw-   0 root         (0) root         (0)     1835 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/testtools.py
+-rw-rw-rw-   0 root         (0) root         (0)     9031 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/tools.py
+-rw-rw-rw-   0 root         (0) root         (0)    41450 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/workermanager.py
+-rw-rw-rw-   0 root         (0) root         (0)     1598 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya/yaml.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.322644 utopya-1.2.8/utopya.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     3168 2023-07-23 15:43:53.000000 utopya-1.2.8/utopya.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     2762 2023-07-23 15:43:53.000000 utopya-1.2.8/utopya.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-07-23 15:43:53.000000 utopya-1.2.8/utopya.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       46 2023-07-23 15:43:53.000000 utopya-1.2.8/utopya.egg-info/entry_points.txt
+-rw-r--r--   0 root         (0) root         (0)      511 2023-07-23 15:43:53.000000 utopya-1.2.8/utopya.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       39 2023-07-23 15:43:53.000000 utopya-1.2.8/utopya.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.328644 utopya-1.2.8/utopya_backend/
+-rw-rw-rw-   0 root         (0) root         (0)      460 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_backend/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    17418 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_backend/benchmark.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.328644 utopya-1.2.8/utopya_backend/io/
+-rw-rw-rw-   0 root         (0) root         (0)       63 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_backend/io/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1504 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_backend/logging.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.329644 utopya-1.2.8/utopya_backend/model/
+-rw-rw-rw-   0 root         (0) root         (0)      512 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_backend/model/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    21214 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_backend/model/base.py
+-rw-rw-rw-   0 root         (0) root         (0)     8082 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_backend/model/step.py
+-rw-rw-rw-   0 root         (0) root         (0)     1619 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_backend/signal.py
+-rw-rw-rw-   0 root         (0) root         (0)     5411 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_backend/tools.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:43:53.331644 utopya-1.2.8/utopya_cli/
+-rw-rw-rw-   0 root         (0) root         (0)       66 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    18051 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/_copy_model.py
+-rw-rw-rw-   0 root         (0) root         (0)     9861 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/_shared.py
+-rw-rw-rw-   0 root         (0) root         (0)    15347 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/_utils.py
+-rw-rw-rw-   0 root         (0) root         (0)     1644 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/batch.py
+-rw-rw-rw-   0 root         (0) root         (0)     1382 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/cli.py
+-rw-rw-rw-   0 root         (0) root         (0)     5722 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/config.py
+-rw-rw-rw-   0 root         (0) root         (0)    17744 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/eval.py
+-rw-rw-rw-   0 root         (0) root         (0)    24141 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/models.py
+-rw-rw-rw-   0 root         (0) root         (0)     7872 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/projects.py
+-rw-rw-rw-   0 root         (0) root         (0)     6753 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/run.py
+-rw-rw-rw-   0 root         (0) root         (0)     2627 2023-07-23 15:43:42.000000 utopya-1.2.8/utopya_cli/test.py
```

### Comparing `utopya-1.2.7/COPYING` & `utopya-1.2.8/COPYING`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/COPYING.LESSER` & `utopya-1.2.8/COPYING.LESSER`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/PKG-INFO` & `utopya-1.2.8/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: utopya
-Version: 1.2.7
+Version: 1.2.8
 Summary: A simulation management and evaluation framework
 Home-page: https://gitlab.com/utopia-project/utopya
 Author: utopya developers
 Author-email: Benjamin Herdeanu <Benjamin.Herdeanu@iup.uni-heidelberg.de>, Yunus Sevinchan <yunus.sevinchan@hu-berlin.de>
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

### Comparing `utopya-1.2.7/README.md` & `utopya-1.2.8/README.md`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/pyproject.toml` & `utopya-1.2.8/pyproject.toml`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/setup.py` & `utopya-1.2.8/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,28 +1,29 @@
 """Sets up the utopya package, test dependencies, and command line scripts"""
 
 from setuptools import find_packages, setup
 
 # .. Dependency lists .........................................................
 
 INSTALL_DEPS = [
-    "numpy",
+    "numpy < 2.0",
     "scipy",
     "matplotlib",
     "seaborn",
     "ruamel.yaml",
     "coloredlogs",
     "colorama",
     "click",
     "pydantic >= 2.0",
     "python-git-info",
     #
-    # related to utopya:
-    "paramspace>=2.5.9",
-    "dantro>=0.18.5",
+    # first-party packages
+    "yayaml>=0.1.1",
+    "paramspace>=2.6.1",
+    "dantro>=0.19.2",
 ]
 # NOTE When adding a new dependency, make sure to denote it in the isort
 #      configuration, see pyproject.toml.
 
 # Dependencies for running tests and general development of utopya
 TEST_DEPS = [
     "pytest",
```

### Comparing `utopya-1.2.7/tests/_gen_figures/__init__.py` & `utopya-1.2.8/tests/_gen_figures/__init__.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/_gen_figures/test_plots.py` & `utopya-1.2.8/tests/_gen_figures/test_plots.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/backend/test_benchmark.py` & `utopya-1.2.8/tests/backend/test_benchmark.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/backend/test_model.py` & `utopya-1.2.8/tests/backend/test_model.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,14 +1,16 @@
 """Tests utopya_backend.base_model"""
 
 import copy
 import os
+import random
 import signal
 import time
 
+import numpy as np
 import pytest
 
 from utopya.testtools import ModelTest
 from utopya.tools import load_yml, write_yml
 from utopya_backend.model import BaseModel, StepwiseModel
 from utopya_backend.signal import SIG_STOPCOND, SIGNAL_INFO
 
@@ -146,14 +148,62 @@
 
     # Teardown does not fail even if there is some unexpected error.
     # Here, provoke it by removing the attribute altogether
     model._h5file = None
     del model
 
 
+def test_BaseModel_rngs(minimal_pspace_cfg, tmpdir):
+    cfg = minimal_pspace_cfg
+    cfg["root_model_name"] = "MyModel"
+    cfg["MyModel"] = dict(some_param="foo", max_n_iter=13)
+
+    cfg_path = tmpdir.join("cfg.yml")
+    write_yml(cfg, path=cfg_path)
+
+    # Set up a first model and let it generate random numbers
+    N = 100
+    m1 = MyModel(cfg_file_path=cfg_path)
+    rands1 = dict(
+        model=[m1.rng.random() for _ in range(N)],
+        np=[np.random.random() for _ in range(N)],
+        sys=[random.random() for _ in range(N)],
+    )
+
+    # When setting up a second model, it should generate the same numbers
+    os.remove(cfg["output_path"])  # because m1's file still exists
+    m2 = MyModel(cfg_file_path=cfg_path)
+    rands2 = dict(
+        model=[m2.rng.random() for _ in range(N)],
+        np=[np.random.random() for _ in range(N)],
+        sys=[random.random() for _ in range(N)],
+    )
+
+    assert np.isclose(rands1["model"], rands2["model"]).all()
+    assert np.isclose(rands1["np"], rands2["np"]).all()
+    assert np.isclose(rands1["sys"], rands2["sys"]).all()
+
+    # When setting different seeds, this is not the case *for np & system*
+    os.remove(cfg["output_path"])  # because m1s file still exists
+    cfg["seed_numpy_rng"] = False
+    cfg["seed_system_rng"] = None
+    write_yml(cfg, path=cfg_path)
+
+    m3 = MyModel(cfg_file_path=cfg_path)
+    rands3 = dict(
+        model=[m3.rng.random() for _ in range(N)],
+        np=[np.random.random() for _ in range(N)],
+        sys=[random.random() for _ in range(N)],
+    )
+
+    assert np.isclose(rands1["model"], rands3["model"]).all()
+    assert not np.isclose(rands1["np"], rands3["np"]).any()
+    assert not np.isclose(rands1["sys"], rands3["sys"]).any()
+
+
 # -----------------------------------------------------------------------------
 
 
 def test_StepwiseModel_basic(minimal_pspace_cfg, tmpdir):
     """Tests instantiation of a base model"""
     # Create the configuration file, filling it with model-specific info
     cfg = minimal_pspace_cfg
```

### Comparing `utopya-1.2.7/tests/backend/test_tools.py` & `utopya-1.2.8/tests/backend/test_tools.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/cli/test__shell_complete.py` & `utopya-1.2.8/tests/cli/test__shell_complete.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/cli/test__to_migrate.py` & `utopya-1.2.8/tests/cli/test__to_migrate.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/cli/test_batch.py` & `utopya-1.2.8/tests/cli/test_batch.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/cli/test_config.py` & `utopya-1.2.8/tests/cli/test_config.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/cli/test_models.py` & `utopya-1.2.8/tests/cli/test_models.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/cli/test_projects.py` & `utopya-1.2.8/tests/cli/test_projects.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/cli/test_run_and_eval.py` & `utopya-1.2.8/tests/cli/test_run_and_eval.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/cli/test_test.py` & `utopya-1.2.8/tests/cli/test_test.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/eval/test_containers.py` & `utopya-1.2.8/tests/eval/test_containers.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/eval/test_datamanager.py` & `utopya-1.2.8/tests/eval/test_datamanager.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/eval/test_groups.py` & `utopya-1.2.8/tests/eval/test_groups.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/eval/test_plot_utils.py` & `utopya-1.2.8/tests/eval/test_plot_utils.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/tests/eval/test_plotting.py` & `utopya-1.2.8/tests/eval/test_plotting.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/__init__.py` & `utopya-1.2.8/utopya/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -34,15 +34,15 @@
 utopya as its frontend.
 For model implementations, the :py:mod:`utopya_backend` package can assist in
 building Python-based models that use :py:mod:`utopya` as a frontend.
 
 Also visit :ref:`the user manual front page <welcome>` for more information.
 """
 
-__version__ = "1.2.7"
+__version__ = "1.2.8"
 """The :py:mod:`utopya` package version"""
 
 # .. Logging ..................................................................
 # TODO Consider setting up logging elsewhere -- but needs to be done first!
 from dantro.logging import REMARK as _DEFAULT_LOG_LEVEL
 from dantro.logging import getLogger as _getLogger
```

### Comparing `utopya-1.2.7/utopya/_cluster.py` & `utopya-1.2.8/utopya/_cluster.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/_import_tools.py` & `utopya-1.2.8/utopya/_import_tools.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/_yaml_registry/entry.py` & `utopya-1.2.8/utopya/_yaml_registry/entry.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/_yaml_registry/registry.py` & `utopya-1.2.8/utopya/_yaml_registry/registry.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/batch.py` & `utopya-1.2.8/utopya/batch.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/cfg/base_cfg.yml` & `utopya-1.2.8/utopya/cfg/base_cfg.yml`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/cfg/base_plots.yml` & `utopya-1.2.8/utopya/cfg/base_plots.yml`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/cfg/btm_cfg.yml` & `utopya-1.2.8/utopya/cfg/btm_cfg.yml`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/cfg.py` & `utopya-1.2.8/utopya/cfg.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/_plot_func_resolver.py` & `utopya-1.2.8/utopya/eval/_plot_func_resolver.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/containers.py` & `utopya-1.2.8/utopya/eval/containers.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/data_ops.py` & `utopya-1.2.8/utopya/eval/data_ops.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/datamanager.py` & `utopya-1.2.8/utopya/eval/datamanager.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/groups.py` & `utopya-1.2.8/utopya/eval/groups.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plotcreators.py` & `utopya-1.2.8/utopya/eval/plotcreators.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plothelper.py` & `utopya-1.2.8/utopya/eval/plothelper.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plotmanager.py` & `utopya-1.2.8/utopya/eval/plotmanager.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/_attractor.py` & `utopya-1.2.8/utopya/eval/plots/_attractor.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/_graph.py` & `utopya-1.2.8/utopya/eval/plots/_graph.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/_mpl.py` & `utopya-1.2.8/utopya/eval/plots/_mpl.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/_utils.py` & `utopya-1.2.8/utopya/eval/plots/_utils.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/abm.py` & `utopya-1.2.8/utopya/eval/plots/abm.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/attractor.py` & `utopya-1.2.8/utopya/eval/plots/attractor.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/ca.py` & `utopya-1.2.8/utopya/eval/plots/ca.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/distributions.py` & `utopya-1.2.8/utopya/eval/plots/distributions.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/graph.py` & `utopya-1.2.8/utopya/eval/plots/graph.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/snsplot.py` & `utopya-1.2.8/utopya/eval/plots/snsplot.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/plots/time_series.py` & `utopya-1.2.8/utopya/eval/plots/time_series.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/eval/transform.py` & `utopya-1.2.8/utopya/eval/transform.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/exceptions.py` & `utopya-1.2.8/utopya/exceptions.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/model.py` & `utopya-1.2.8/utopya/model.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/model_registry/__init__.py` & `utopya-1.2.8/utopya/model_registry/__init__.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/model_registry/_registration.py` & `utopya-1.2.8/utopya/model_registry/_registration.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/model_registry/entry.py` & `utopya-1.2.8/utopya/model_registry/entry.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/model_registry/info_bundle.py` & `utopya-1.2.8/utopya/model_registry/info_bundle.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/model_registry/registry.py` & `utopya-1.2.8/utopya/model_registry/registry.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/model_registry/utils.py` & `utopya-1.2.8/utopya/model_registry/utils.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/multiverse.py` & `utopya-1.2.8/utopya/multiverse.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/parameter.py` & `utopya-1.2.8/utopya/parameter.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/plotting.py` & `utopya-1.2.8/utopya/plotting.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/project_registry.py` & `utopya-1.2.8/utopya/project_registry.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/reporter.py` & `utopya-1.2.8/utopya/reporter.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/stop_conditions.py` & `utopya-1.2.8/utopya/stop_conditions.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/task.py` & `utopya-1.2.8/utopya/task.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/testtools.py` & `utopya-1.2.8/utopya/testtools.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/tools.py` & `utopya-1.2.8/utopya/tools.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya/workermanager.py` & `utopya-1.2.8/utopya/workermanager.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya.egg-info/PKG-INFO` & `utopya-1.2.8/utopya.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: utopya
-Version: 1.2.7
+Version: 1.2.8
 Summary: A simulation management and evaluation framework
 Home-page: https://gitlab.com/utopia-project/utopya
 Author: utopya developers
 Author-email: Benjamin Herdeanu <Benjamin.Herdeanu@iup.uni-heidelberg.de>, Yunus Sevinchan <yunus.sevinchan@hu-berlin.de>
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

### Comparing `utopya-1.2.7/utopya.egg-info/SOURCES.txt` & `utopya-1.2.8/utopya.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_backend/benchmark.py` & `utopya-1.2.8/utopya_backend/benchmark.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_backend/logging.py` & `utopya-1.2.8/utopya_backend/logging.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_backend/model/__init__.py` & `utopya-1.2.8/utopya_backend/model/__init__.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_backend/model/base.py` & `utopya-1.2.8/utopya_backend/model/base.py`

 * *Files 9% similar despite different names*

```diff
@@ -2,18 +2,19 @@
 inherited from for implementing a utopya-controlled model.
 
 Its main aim is to provide shared simulation infrastructure and does not make
 further assumptions about the abstraction a model makes, like the step-wise
 iteration done in :py:class:`~utopya_backend.model.step.StepwiseModel`."""
 
 import abc
+import random
 import signal
 import sys
 import time
-from typing import Union
+from typing import Optional, Union
 
 import h5py as h5
 import numpy as np
 
 from ..logging import backend_logger as _backend_logger
 from ..logging import get_level as _get_level
 from ..signal import SIG_STOPCOND, SIGNAL_INFO, attach_signal_handlers
@@ -101,15 +102,23 @@
         self._monitor_info = dict()
         self._monitor_emit_interval = self.root_cfg["monitor_emit_interval"]
 
         # Keep track of number of iterations
         self._n_iterations = 0
 
         # RNG
-        self._rng = self._setup_rng(seed=self.root_cfg["seed"])
+        # In order to ensure that a simulation is deterministic even when not
+        # using the model-specific RNG instance, some singleton-like default
+        # RNGs are (by default) seeded additionally. To avoid equal random
+        # number sequences, they are salted.
+        self._rng = self._setup_rng(
+            seed=self.root_cfg["seed"],
+            seed_numpy_rng=self.root_cfg.get("seed_numpy_rng", True),
+            seed_system_rng=self.root_cfg.get("seed_system_rng", True),
+        )
 
         # Create the output file
         self._h5file = self._setup_output_file()
         self._h5group = self._setup_output_group()
 
         # Allow subclasses to parse root config parameters, potentiaally adding
         # more attributes
@@ -501,18 +510,63 @@
         backend_log_level = self.root_cfg["log_levels"].get("backend")
         if backend_log_level is not None:
             _backend_logger.setLevel(_get_level(backend_log_level))
             self.log.info(
                 "  Set backend logger's level to '%s'.", backend_log_level
             )
 
-    def _setup_rng(self, *, seed: int, **kwargs) -> "numpy.random.Generator":
-        """Sets up the shared RNG"""
+    def _setup_rng(
+        self,
+        *,
+        seed: int,
+        seed_numpy_rng: Optional[Union[bool, int]] = None,
+        seed_system_rng: Optional[Union[bool, int]] = None,
+        **rng_kwargs,
+    ) -> "numpy.random.Generator":
+        """Sets up the shared RNG.
+
+        .. note::
+
+            If also seeding the other RNGs, make sure to use different seeds
+            for them, such that random number sequences are ensured to be
+            different even if the underlying generator may be the same.
+
+        Args:
+            seed (int): The seed for the new, model-specific RNG, constructed
+                via :py:func:`numpy.random.default_rng`
+            seed_numpy_rng (Optional[Union[bool, int]], optional): If not
+                False or None, will also seed numpy's singleton (i.e.
+                *default*) RNG by calling :py:func:`numpy.random.seed`.
+                If True, will use ``seed + 1`` for that.
+            seed_system_rng (Optional[Union[bool, int]], optional): If not
+                False or None, will also seed the system's default RNG by
+                calling :py:func:`random.seed`.
+                If True, will use ``seed + 2`` for that.
+            **rng_kwargs: Passed on to :py:func:`numpy.random.default_rng`
+        """
         self.log.info("Creating shared RNG (seed: %s) ...", seed)
-        return np.random.default_rng(seed, **kwargs)
+        rng = np.random.default_rng(seed, **rng_kwargs)
+
+        if seed_numpy_rng not in (None, False):
+            if seed_numpy_rng is True:
+                seed_numpy_rng = seed + 1
+            np.random.seed(seed_numpy_rng)
+            self.log.debug(
+                "  Default numpy RNG seeded with:  %s", seed_numpy_rng
+            )
+
+        if seed_system_rng not in (None, False):
+            if seed_system_rng is True:
+                seed_system_rng = seed + 2
+            random.seed(seed_system_rng)
+            self.log.debug(
+                "  Default system RNG seeded with: %s", seed_system_rng
+            )
+
+        return rng
 
     def _setup_output_file(self) -> "h5py.File":
         """Creates the output file for this model; by default, it is a HDF5
         file that is managed by a :py:class:`h5py.File` object.
 
         .. note::
```

### Comparing `utopya-1.2.7/utopya_backend/model/step.py` & `utopya-1.2.8/utopya_backend/model/step.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_backend/signal.py` & `utopya-1.2.8/utopya_backend/signal.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_backend/tools.py` & `utopya-1.2.8/utopya_backend/tools.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/_copy_model.py` & `utopya-1.2.8/utopya_cli/_copy_model.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/_shared.py` & `utopya-1.2.8/utopya_cli/_shared.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/_utils.py` & `utopya-1.2.8/utopya_cli/_utils.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/batch.py` & `utopya-1.2.8/utopya_cli/batch.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/cli.py` & `utopya-1.2.8/utopya_cli/cli.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/config.py` & `utopya-1.2.8/utopya_cli/config.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/eval.py` & `utopya-1.2.8/utopya_cli/eval.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/models.py` & `utopya-1.2.8/utopya_cli/models.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/projects.py` & `utopya-1.2.8/utopya_cli/projects.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/run.py` & `utopya-1.2.8/utopya_cli/run.py`

 * *Files identical despite different names*

### Comparing `utopya-1.2.7/utopya_cli/test.py` & `utopya-1.2.8/utopya_cli/test.py`

 * *Files identical despite different names*

