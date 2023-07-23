# Comparing `tmp/klvm_rs-0.1.24.tar.gz` & `tmp/klvm_rs-0.2.8.tar.gz`

## Comparing `klvm_rs-0.1.24.tar` & `klvm_rs-0.2.8.tar`

### file list

```diff
@@ -1,706 +1,754 @@
--rw-r--r--   0        0        0      651 1970-01-01 00:00:00.000000 klvm_rs-0.1.24/local_dependencies/klvmr/Cargo.toml
--rw-r--r--   0      501       20      224 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/.cargo/config
--rw-r--r--   0      501       20      290 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/audit-check.yaml.bak
--rw-r--r--   0      501       20     3149 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/benchmark.yml.bak
--rw-r--r--   0      501       20     3003 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/build-arm64-wheels.yml.bak
--rw-r--r--   0      501       20     2031 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/build-crate-and-npm.yml
--rw-r--r--   0      501       20     3408 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/build-m1-wheel.yml.bak
--rw-r--r--   0      501       20     7537 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/build-test.yml
--rw-r--r--   0      501       20      885 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/dependency-review.yml.bak
--rw-r--r--   0      501       20     1330 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/stale-issue.yml.bak
--rw-r--r--   0      501       20    11357 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/LICENSE
--rw-r--r--   0      501       20      928 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/README.md
--rw-r--r--   0      501       20      619 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/RELEASE.md
--rw-r--r--   0      501       20     2219 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/activate
--rw-r--r--   0      501       20        3 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/block-2000.envhex
--rw-r--r--   0      501       20  1560006 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/block-2000.hex
--rwxr-xr-x   0      501       20     4090 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/cmp.py
--rw-r--r--   0      501       20     1771 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/compressed-2000.envhex
--rw-r--r--   0      501       20   596274 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/compressed-2000.hex
--rw-r--r--   0      501       20       20 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/concat.env
--rw-r--r--   0      501       20      509 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/concat.klvm
--rw-r--r--   0      501       20      320 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/count-even.klvm
--rw-r--r--   0      501       20        8 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/factorial.env
--rw-r--r--   0      501       20      247 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/factorial.klvm
--rw-r--r--   0      501       20       51 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/hash-string.klvm
--rw-r--r--   0      501       20      246 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/hash-tree.klvm
--rw-r--r--   0      501       20      401 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/large-block.klvm
--rw-r--r--   0      501       20       10 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_add.env
--rw-r--r--   0      501       20      193 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_add.klvm
--rw-r--r--   0      501       20       10 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_ior.env
--rw-r--r--   0      501       20      183 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_ior.klvm
--rw-r--r--   0      501       20       10 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_not.env
--rw-r--r--   0      501       20      224 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_not.klvm
--rw-r--r--   0      501       20       10 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_sub.env
--rw-r--r--   0      501       20      193 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_sub.klvm
--rw-r--r--   0      501       20       10 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_xor.env
--rw-r--r--   0      501       20      207 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/loop_xor.klvm
--rw-r--r--   0      501       20     1793 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/matrix-multiply.klvm
--rw-r--r--   0      501       20      106 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/point-pow.env
--rw-r--r--   0      501       20      288 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/point-pow.klvm
--rw-r--r--   0      501       20      318 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/pubkey-tree.klvm
--rwxr-xr-x   0      501       20     8448 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/run-benchmark.py
--rw-r--r--   0      501       20      292 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/shift-left.klvm
--rw-r--r--   0      501       20      488 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/substr-tree.klvm
--rw-r--r--   0      501       20      390 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/substr.klvm
--rw-r--r--   0      501       20      237 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/sum-tree.klvm
--rw-r--r--   0      501       20     3853 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/docs/implementation-notes.md
--rw-r--r--   0      501       20    12490 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/allocator.rs
--rw-r--r--   0      501       20     3269 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/chik_dialect.rs
--rw-r--r--   0      501       20     3224 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/core_ops.rs
--rw-r--r--   0      501       20      289 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/cost.rs
--rw-r--r--   0      501       20      337 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/dialect.rs
--rw-r--r--   0      501       20      164 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/err_utils.rs
--rw-r--r--   0      501       20     2387 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/f_table.rs
--rw-r--r--   0      501       20      343 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/lib.rs
--rw-r--r--   0      501       20    28951 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/more_ops.rs
--rw-r--r--   0      501       20     2842 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/node.rs
--rw-r--r--   0      501       20    10082 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/number.rs
--rw-r--r--   0      501       20     8187 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/op_utils.rs
--rw-r--r--   0      501       20      403 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/reduction.rs
--rw-r--r--   0      501       20    30973 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/run_program.rs
--rw-r--r--   0      501       20     1553 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/runtime_dialect.rs
--rw-r--r--   0      501       20    19728 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/serialize.rs
--rw-r--r--   0      501       20     1349 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/sha2.rs
--rw-r--r--   0      501       20    87455 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/test_ops.rs
--rw-r--r--   0      501       20     4524 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/src/tests.rs
--rwxr-xr-x   0      501       20     8264 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/tests/generate-programs.py
--rwxr-xr-x   0      501       20     2979 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/tests/run-programs.py
--rwxr-xr-x   0      501       20     1569 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/local_dependencies/klvmr/tests/run.py
--rw-r--r--   0      501       20     2219 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/activate
--rw-r--r--   0      501       20     1271 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/activate.csh
--rw-r--r--   0      501       20     2423 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/activate.fish
--rwxr-xr-x   0      501       20      264 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/easy_install
--rwxr-xr-x   0      501       20      264 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/easy_install-3.7
--rwxr-xr-x   0      501       20      255 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/pip
--rwxr-xr-x   0      501       20      255 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/pip3
--rwxr-xr-x   0      501       20      255 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/pip3.7
--rwxr-xr-x   0      501       20    49640 2023-07-10 04:30:11.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/python
--rwxr-xr-x   0      501       20    49640 2023-07-10 04:30:11.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/python3
--rw-r--r--   0      501       20      126 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/easy_install.py
--rw-r--r--   0      501       20      357 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__init__.py
--rw-r--r--   0      501       20     1198 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__main__.py
--rw-r--r--   0      501       20     1444 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__pip-runner__.py
--rw-r--r--   0      501       20      573 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/__init__.py
--rw-r--r--   0      501       20    10243 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/build_env.py
--rw-r--r--   0      501       20    10734 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cache.py
--rw-r--r--   0      501       20      132 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/__init__.py
--rw-r--r--   0      501       20     6676 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/autocompletion.py
--rw-r--r--   0      501       20     7842 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/base_command.py
--rw-r--r--   0      501       20    29497 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/cmdoptions.py
--rw-r--r--   0      501       20      774 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/command_context.py
--rw-r--r--   0      501       20     2472 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/main.py
--rw-r--r--   0      501       20     4338 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/main_parser.py
--rw-r--r--   0      501       20    10817 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/parser.py
--rw-r--r--   0      501       20     1968 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/progress_bars.py
--rw-r--r--   0      501       20    18172 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/req_command.py
--rw-r--r--   0      501       20     5118 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/spinners.py
--rw-r--r--   0      501       20      116 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/status_codes.py
--rw-r--r--   0      501       20     3882 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/__init__.py
--rw-r--r--   0      501       20     7582 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/cache.py
--rw-r--r--   0      501       20     1685 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/check.py
--rw-r--r--   0      501       20     4129 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/completion.py
--rw-r--r--   0      501       20     9815 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/configuration.py
--rw-r--r--   0      501       20     6591 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/debug.py
--rw-r--r--   0      501       20     5289 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/download.py
--rw-r--r--   0      501       20     2951 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/freeze.py
--rw-r--r--   0      501       20     1703 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/hash.py
--rw-r--r--   0      501       20     1132 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/help.py
--rw-r--r--   0      501       20     4793 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/index.py
--rw-r--r--   0      501       20     3188 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/inspect.py
--rw-r--r--   0      501       20    32389 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/install.py
--rw-r--r--   0      501       20    12343 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/list.py
--rw-r--r--   0      501       20     5697 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/search.py
--rw-r--r--   0      501       20     6419 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/show.py
--rw-r--r--   0      501       20     3886 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/uninstall.py
--rw-r--r--   0      501       20     7396 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/wheel.py
--rw-r--r--   0      501       20    13529 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/configuration.py
--rw-r--r--   0      501       20      858 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/__init__.py
--rw-r--r--   0      501       20     1221 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/base.py
--rw-r--r--   0      501       20      729 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/installed.py
--rw-r--r--   0      501       20     6494 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/sdist.py
--rw-r--r--   0      501       20     1164 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/wheel.py
--rw-r--r--   0      501       20    24244 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/exceptions.py
--rw-r--r--   0      501       20       30 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/__init__.py
--rw-r--r--   0      501       20    16504 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/collector.py
--rw-r--r--   0      501       20    37873 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/package_finder.py
--rw-r--r--   0      501       20     6557 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/sources.py
--rw-r--r--   0      501       20    15365 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/__init__.py
--rw-r--r--   0      501       20     6100 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/_distutils.py
--rw-r--r--   0      501       20     7680 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/_sysconfig.py
--rw-r--r--   0      501       20     2556 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/base.py
--rw-r--r--   0      501       20      340 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/main.py
--rw-r--r--   0      501       20     4280 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/__init__.py
--rw-r--r--   0      501       20     2595 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/_json.py
--rw-r--r--   0      501       20    25277 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/base.py
--rw-r--r--   0      501       20      107 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/__init__.py
--rw-r--r--   0      501       20     1882 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_compat.py
--rw-r--r--   0      501       20     8181 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_dists.py
--rw-r--r--   0      501       20     7457 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_envs.py
--rw-r--r--   0      501       20     9773 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/pkg_resources.py
--rw-r--r--   0      501       20       63 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/__init__.py
--rw-r--r--   0      501       20      990 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/candidate.py
--rw-r--r--   0      501       20     6626 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/direct_url.py
--rw-r--r--   0      501       20     2520 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/format_control.py
--rw-r--r--   0      501       20     1030 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/index.py
--rw-r--r--   0      501       20     2617 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/installation_report.py
--rw-r--r--   0      501       20    18602 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/link.py
--rw-r--r--   0      501       20      738 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/scheme.py
--rw-r--r--   0      501       20     4644 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/search_scope.py
--rw-r--r--   0      501       20     1907 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/selection_prefs.py
--rw-r--r--   0      501       20     3858 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/target_python.py
--rw-r--r--   0      501       20     3600 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/wheel.py
--rw-r--r--   0      501       20       50 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/__init__.py
--rw-r--r--   0      501       20    16507 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/auth.py
--rw-r--r--   0      501       20     2145 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/cache.py
--rw-r--r--   0      501       20     6096 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/download.py
--rw-r--r--   0      501       20     7638 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/lazy_wheel.py
--rw-r--r--   0      501       20    18443 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/session.py
--rw-r--r--   0      501       20     4073 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/utils.py
--rw-r--r--   0      501       20     1791 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/xmlrpc.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/__init__.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/__init__.py
--rw-r--r--   0      501       20     4133 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/build_tracker.py
--rw-r--r--   0      501       20     1422 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata.py
--rw-r--r--   0      501       20     1474 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata_editable.py
--rw-r--r--   0      501       20     2198 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata_legacy.py
--rw-r--r--   0      501       20     1075 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel.py
--rw-r--r--   0      501       20     1417 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel_editable.py
--rw-r--r--   0      501       20     3064 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel_legacy.py
--rw-r--r--   0      501       20     5122 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/check.py
--rw-r--r--   0      501       20     9784 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/freeze.py
--rw-r--r--   0      501       20       51 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/__init__.py
--rw-r--r--   0      501       20     1354 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/editable_legacy.py
--rw-r--r--   0      501       20     4105 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/legacy.py
--rw-r--r--   0      501       20    27407 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/wheel.py
--rw-r--r--   0      501       20    25091 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/prepare.py
--rw-r--r--   0      501       20     6987 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/pyproject.py
--rw-r--r--   0      501       20     2807 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/__init__.py
--rw-r--r--   0      501       20    16611 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/constructors.py
--rw-r--r--   0      501       20    17646 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_file.py
--rw-r--r--   0      501       20    35763 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_install.py
--rw-r--r--   0      501       20     2858 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_set.py
--rw-r--r--   0      501       20    24045 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_uninstall.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/__init__.py
--rw-r--r--   0      501       20      583 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/base.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/legacy/__init__.py
--rw-r--r--   0      501       20    24129 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/legacy/resolver.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/__init__.py
--rw-r--r--   0      501       20     5220 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/base.py
--rw-r--r--   0      501       20    18963 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/candidates.py
--rw-r--r--   0      501       20    27878 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/factory.py
--rw-r--r--   0      501       20     5705 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/found_candidates.py
--rw-r--r--   0      501       20     9914 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/provider.py
--rw-r--r--   0      501       20     2526 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/reporter.py
--rw-r--r--   0      501       20     5455 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/requirements.py
--rw-r--r--   0      501       20    11533 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/resolver.py
--rw-r--r--   0      501       20     8167 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/self_outdated_check.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/__init__.py
--rw-r--r--   0      501       20     1015 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/_log.py
--rw-r--r--   0      501       20     1665 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/appdirs.py
--rw-r--r--   0      501       20     1884 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/compat.py
--rw-r--r--   0      501       20     5377 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/compatibility_tags.py
--rw-r--r--   0      501       20      242 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/datetime.py
--rw-r--r--   0      501       20     5764 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/deprecation.py
--rw-r--r--   0      501       20     3206 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/direct_url_helpers.py
--rw-r--r--   0      501       20     1115 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/distutils_args.py
--rw-r--r--   0      501       20     2118 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/egg_link.py
--rw-r--r--   0      501       20     1169 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/encoding.py
--rw-r--r--   0      501       20     3064 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/entrypoints.py
--rw-r--r--   0      501       20     5122 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/filesystem.py
--rw-r--r--   0      501       20      716 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/filetypes.py
--rw-r--r--   0      501       20     3110 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/glibc.py
--rw-r--r--   0      501       20     4831 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/hashes.py
--rw-r--r--   0      501       20      795 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/inject_securetransport.py
--rw-r--r--   0      501       20    11632 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/logging.py
--rw-r--r--   0      501       20    22253 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/misc.py
--rw-r--r--   0      501       20     1193 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/models.py
--rw-r--r--   0      501       20     2108 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/packaging.py
--rw-r--r--   0      501       20     5662 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/setuptools_build.py
--rw-r--r--   0      501       20     9200 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/subprocess.py
--rw-r--r--   0      501       20     7702 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/temp_dir.py
--rw-r--r--   0      501       20     8821 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/unpacking.py
--rw-r--r--   0      501       20     1759 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/urls.py
--rw-r--r--   0      501       20     3456 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/virtualenv.py
--rw-r--r--   0      501       20     4549 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/wheel.py
--rw-r--r--   0      501       20      596 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/__init__.py
--rw-r--r--   0      501       20     3519 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/bazaar.py
--rw-r--r--   0      501       20    18116 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/git.py
--rw-r--r--   0      501       20     5238 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/mercurial.py
--rw-r--r--   0      501       20    11729 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/subversion.py
--rw-r--r--   0      501       20    22811 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/versioncontrol.py
--rw-r--r--   0      501       20    13079 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/wheel_builder.py
--rw-r--r--   0      501       20     4966 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/__init__.py
--rw-r--r--   0      501       20      465 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/__init__.py
--rw-r--r--   0      501       20     1379 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/_cmd.py
--rw-r--r--   0      501       20     5033 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/adapter.py
--rw-r--r--   0      501       20     1535 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/cache.py
--rw-r--r--   0      501       20      242 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/__init__.py
--rw-r--r--   0      501       20     5271 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/file_cache.py
--rw-r--r--   0      501       20     1033 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/redis_cache.py
--rw-r--r--   0      501       20      778 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/compat.py
--rw-r--r--   0      501       20    16416 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/controller.py
--rw-r--r--   0      501       20     3946 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/filewrapper.py
--rw-r--r--   0      501       20     4154 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/heuristics.py
--rw-r--r--   0      501       20     7105 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/serialize.py
--rw-r--r--   0      501       20      774 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/wrapper.py
--rw-r--r--   0      501       20       94 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/__init__.py
--rw-r--r--   0      501       20      255 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/__main__.py
--rw-r--r--   0      501       20   275233 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/cacert.pem
--rw-r--r--   0      501       20     4279 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/core.py
--rw-r--r--   0      501       20     4797 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/__init__.py
--rw-r--r--   0      501       20    31274 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/big5freq.py
--rw-r--r--   0      501       20     1763 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/big5prober.py
--rw-r--r--   0      501       20    10032 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/chardistribution.py
--rw-r--r--   0      501       20     3915 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/charsetgroupprober.py
--rw-r--r--   0      501       20     5420 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/charsetprober.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cli/__init__.py
--rw-r--r--   0      501       20     3242 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cli/chardetect.py
--rw-r--r--   0      501       20     3732 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/codingstatemachine.py
--rw-r--r--   0      501       20      542 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/codingstatemachinedict.py
--rw-r--r--   0      501       20     1860 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cp949prober.py
--rw-r--r--   0      501       20     1683 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/enums.py
--rw-r--r--   0      501       20     4006 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/escprober.py
--rw-r--r--   0      501       20    12176 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/escsm.py
--rw-r--r--   0      501       20     3934 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/eucjpprober.py
--rw-r--r--   0      501       20    13566 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euckrfreq.py
--rw-r--r--   0      501       20     1753 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euckrprober.py
--rw-r--r--   0      501       20    36913 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euctwfreq.py
--rw-r--r--   0      501       20     1753 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euctwprober.py
--rw-r--r--   0      501       20    20735 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/gb2312freq.py
--rw-r--r--   0      501       20     1759 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/gb2312prober.py
--rw-r--r--   0      501       20    14537 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/hebrewprober.py
--rw-r--r--   0      501       20    25796 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/jisfreq.py
--rw-r--r--   0      501       20    42498 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/johabfreq.py
--rw-r--r--   0      501       20     1752 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/johabprober.py
--rw-r--r--   0      501       20    27055 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/jpcntx.py
--rw-r--r--   0      501       20   104562 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langbulgarianmodel.py
--rw-r--r--   0      501       20    98484 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langgreekmodel.py
--rw-r--r--   0      501       20    98196 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langhebrewmodel.py
--rw-r--r--   0      501       20   101363 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langhungarianmodel.py
--rw-r--r--   0      501       20   128035 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langrussianmodel.py
--rw-r--r--   0      501       20   102774 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langthaimodel.py
--rw-r--r--   0      501       20    95372 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langturkishmodel.py
--rw-r--r--   0      501       20     5380 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/latin1prober.py
--rw-r--r--   0      501       20     6077 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/macromanprober.py
--rw-r--r--   0      501       20     3715 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcharsetprober.py
--rw-r--r--   0      501       20     2131 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcsgroupprober.py
--rw-r--r--   0      501       20    30391 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcssm.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/metadata/__init__.py
--rw-r--r--   0      501       20    13560 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/metadata/languages.py
--rw-r--r--   0      501       20      402 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/resultdict.py
--rw-r--r--   0      501       20     6400 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sbcharsetprober.py
--rw-r--r--   0      501       20     4137 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sbcsgroupprober.py
--rw-r--r--   0      501       20     4007 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sjisprober.py
--rw-r--r--   0      501       20    14848 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/universaldetector.py
--rw-r--r--   0      501       20     8505 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/utf1632prober.py
--rw-r--r--   0      501       20     2812 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/utf8prober.py
--rw-r--r--   0      501       20      244 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/version.py
--rw-r--r--   0      501       20      266 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/__init__.py
--rw-r--r--   0      501       20     2522 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/ansi.py
--rw-r--r--   0      501       20    11128 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/ansitowin32.py
--rw-r--r--   0      501       20     3325 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/initialise.py
--rw-r--r--   0      501       20       75 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/__init__.py
--rw-r--r--   0      501       20     2839 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/ansi_test.py
--rw-r--r--   0      501       20    10678 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/ansitowin32_test.py
--rw-r--r--   0      501       20     6741 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/initialise_test.py
--rw-r--r--   0      501       20     1866 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/isatty_test.py
--rw-r--r--   0      501       20     1079 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/utils.py
--rw-r--r--   0      501       20     3709 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/winterm_test.py
--rw-r--r--   0      501       20     6181 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/win32.py
--rw-r--r--   0      501       20     7134 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/winterm.py
--rw-r--r--   0      501       20      581 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/__init__.py
--rw-r--r--   0      501       20    41259 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/compat.py
--rw-r--r--   0      501       20    51697 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/database.py
--rw-r--r--   0      501       20    20834 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/index.py
--rw-r--r--   0      501       20    51991 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/locators.py
--rw-r--r--   0      501       20    14811 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/manifest.py
--rw-r--r--   0      501       20     5058 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/markers.py
--rw-r--r--   0      501       20    39801 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/metadata.py
--rw-r--r--   0      501       20    10820 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/resources.py
--rw-r--r--   0      501       20    18102 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/scripts.py
--rw-r--r--   0      501       20    97792 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t32.exe
--rw-r--r--   0      501       20   182784 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t64-arm.exe
--rw-r--r--   0      501       20   108032 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t64.exe
--rw-r--r--   0      501       20    66262 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/util.py
--rw-r--r--   0      501       20    23513 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/version.py
--rw-r--r--   0      501       20    91648 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w32.exe
--rw-r--r--   0      501       20   168448 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w64-arm.exe
--rw-r--r--   0      501       20   101888 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w64.exe
--rw-r--r--   0      501       20    43898 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/wheel.py
--rw-r--r--   0      501       20      981 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/__init__.py
--rw-r--r--   0      501       20       64 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/__main__.py
--rw-r--r--   0      501       20    49330 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/distro.py
--rw-r--r--   0      501       20      849 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/__init__.py
--rw-r--r--   0      501       20     3374 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/codec.py
--rw-r--r--   0      501       20      321 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/compat.py
--rw-r--r--   0      501       20    12950 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/core.py
--rw-r--r--   0      501       20    44375 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/idnadata.py
--rw-r--r--   0      501       20     1881 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/intranges.py
--rw-r--r--   0      501       20       21 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/package_data.py
--rw-r--r--   0      501       20   206539 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/uts46data.py
--rw-r--r--   0      501       20     1132 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/__init__.py
--rw-r--r--   0      501       20     1081 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/exceptions.py
--rw-r--r--   0      501       20     6080 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/ext.py
--rw-r--r--   0      501       20    34557 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/fallback.py
--rw-r--r--   0      501       20      661 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/__about__.py
--rw-r--r--   0      501       20      497 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/__init__.py
--rw-r--r--   0      501       20    11488 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_manylinux.py
--rw-r--r--   0      501       20     4378 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_musllinux.py
--rw-r--r--   0      501       20     1431 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_structures.py
--rw-r--r--   0      501       20     8487 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/markers.py
--rw-r--r--   0      501       20     4676 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/requirements.py
--rw-r--r--   0      501       20    30110 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/specifiers.py
--rw-r--r--   0      501       20    15699 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/tags.py
--rw-r--r--   0      501       20     4200 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/utils.py
--rw-r--r--   0      501       20    14665 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/version.py
--rw-r--r--   0      501       20   108287 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pkg_resources/__init__.py
--rw-r--r--   0      501       20      562 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pkg_resources/py31compat.py
--rw-r--r--   0      501       20    12936 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/__init__.py
--rw-r--r--   0      501       20     1176 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/__main__.py
--rw-r--r--   0      501       20     4068 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/android.py
--rw-r--r--   0      501       20     4910 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/api.py
--rw-r--r--   0      501       20     2655 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/macos.py
--rw-r--r--   0      501       20     6911 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/unix.py
--rw-r--r--   0      501       20      160 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/version.py
--rw-r--r--   0      501       20     6596 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/windows.py
--rw-r--r--   0      501       20     2999 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/__init__.py
--rw-r--r--   0      501       20      353 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/__main__.py
--rw-r--r--   0      501       20    23685 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/cmdline.py
--rw-r--r--   0      501       20     1697 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/console.py
--rw-r--r--   0      501       20     1938 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/filter.py
--rw-r--r--   0      501       20    40386 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/filters/__init__.py
--rw-r--r--   0      501       20     2917 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatter.py
--rw-r--r--   0      501       20     4810 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/__init__.py
--rw-r--r--   0      501       20     4104 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/_mapping.py
--rw-r--r--   0      501       20     3314 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/bbcode.py
--rw-r--r--   0      501       20     5086 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/groff.py
--rw-r--r--   0      501       20    35441 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/html.py
--rw-r--r--   0      501       20    21938 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/img.py
--rw-r--r--   0      501       20     5871 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/irc.py
--rw-r--r--   0      501       20    19351 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/latex.py
--rw-r--r--   0      501       20     5073 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/other.py
--rw-r--r--   0      501       20     2212 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/pangomarkup.py
--rw-r--r--   0      501       20     5014 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/rtf.py
--rw-r--r--   0      501       20     7335 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/svg.py
--rw-r--r--   0      501       20     4674 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/terminal.py
--rw-r--r--   0      501       20    11753 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/terminal256.py
--rw-r--r--   0      501       20    32005 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexer.py
--rw-r--r--   0      501       20    11174 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/__init__.py
--rw-r--r--   0      501       20    70232 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/_mapping.py
--rw-r--r--   0      501       20    53376 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/python.py
--rw-r--r--   0      501       20      986 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/modeline.py
--rw-r--r--   0      501       20     2591 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/plugin.py
--rw-r--r--   0      501       20     3072 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/regexopt.py
--rw-r--r--   0      501       20     3092 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/scanner.py
--rw-r--r--   0      501       20     4630 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/sphinxext.py
--rw-r--r--   0      501       20     6257 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/style.py
--rw-r--r--   0      501       20     3419 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/styles/__init__.py
--rw-r--r--   0      501       20     6184 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/token.py
--rw-r--r--   0      501       20    63187 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/unistring.py
--rw-r--r--   0      501       20     9110 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/util.py
--rw-r--r--   0      501       20     9171 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/__init__.py
--rw-r--r--   0      501       20     6426 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/actions.py
--rw-r--r--   0      501       20    12936 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/common.py
--rw-r--r--   0      501       20   213344 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/core.py
--rw-r--r--   0      501       20    23685 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/diagram/__init__.py
--rw-r--r--   0      501       20     9023 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/exceptions.py
--rw-r--r--   0      501       20    39129 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/helpers.py
--rw-r--r--   0      501       20    25341 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/results.py
--rw-r--r--   0      501       20    13402 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/testing.py
--rw-r--r--   0      501       20    10787 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/unicode.py
--rw-r--r--   0      501       20     6805 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/util.py
--rw-r--r--   0      501       20      491 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/__init__.py
--rw-r--r--   0      501       20      138 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_compat.py
--rw-r--r--   0      501       20    11920 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_impl.py
--rw-r--r--   0      501       20      546 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_in_process/__init__.py
--rw-r--r--   0      501       20    10927 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py
--rw-r--r--   0      501       20     5178 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/__init__.py
--rw-r--r--   0      501       20      435 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/__version__.py
--rw-r--r--   0      501       20     1397 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/_internal_utils.py
--rw-r--r--   0      501       20    21443 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/adapters.py
--rw-r--r--   0      501       20     6377 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/api.py
--rw-r--r--   0      501       20    10187 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/auth.py
--rw-r--r--   0      501       20      575 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/certs.py
--rw-r--r--   0      501       20     1286 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/compat.py
--rw-r--r--   0      501       20    18560 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/cookies.py
--rw-r--r--   0      501       20     3823 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/exceptions.py
--rw-r--r--   0      501       20     3879 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/help.py
--rw-r--r--   0      501       20      733 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/hooks.py
--rw-r--r--   0      501       20    35288 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/models.py
--rw-r--r--   0      501       20      695 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/packages.py
--rw-r--r--   0      501       20    30180 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/sessions.py
--rw-r--r--   0      501       20     4235 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/status_codes.py
--rw-r--r--   0      501       20     2912 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/structures.py
--rw-r--r--   0      501       20    33240 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/utils.py
--rw-r--r--   0      501       20      537 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/__init__.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/compat/__init__.py
--rw-r--r--   0      501       20      156 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/compat/collections_abc.py
--rw-r--r--   0      501       20     5872 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/providers.py
--rw-r--r--   0      501       20     1583 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/reporters.py
--rw-r--r--   0      501       20    17592 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/resolvers.py
--rw-r--r--   0      501       20     4794 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/structs.py
--rw-r--r--   0      501       20     6090 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/__init__.py
--rw-r--r--   0      501       20     8478 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/__main__.py
--rw-r--r--   0      501       20    10096 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_cell_widths.py
--rw-r--r--   0      501       20   140235 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_emoji_codes.py
--rw-r--r--   0      501       20     1064 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_emoji_replace.py
--rw-r--r--   0      501       20     2114 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_export_format.py
--rw-r--r--   0      501       20      265 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_extension.py
--rw-r--r--   0      501       20     9695 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_inspect.py
--rw-r--r--   0      501       20     3225 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_log_render.py
--rw-r--r--   0      501       20     1236 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_loop.py
--rw-r--r--   0      501       20     1643 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_null_file.py
--rw-r--r--   0      501       20     7063 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_palettes.py
--rw-r--r--   0      501       20      423 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_pick.py
--rw-r--r--   0      501       20     5472 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_ratio.py
--rw-r--r--   0      501       20    19919 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_spinners.py
--rw-r--r--   0      501       20      351 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_stack.py
--rw-r--r--   0      501       20      417 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_timer.py
--rw-r--r--   0      501       20    22820 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_win32_console.py
--rw-r--r--   0      501       20     1926 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_windows.py
--rw-r--r--   0      501       20     2783 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_windows_renderer.py
--rw-r--r--   0      501       20     1840 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_wrap.py
--rw-r--r--   0      501       20      890 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/abc.py
--rw-r--r--   0      501       20    10368 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/align.py
--rw-r--r--   0      501       20     6819 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/ansi.py
--rw-r--r--   0      501       20     3264 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/bar.py
--rw-r--r--   0      501       20     9842 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/box.py
--rw-r--r--   0      501       20     4503 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/cells.py
--rw-r--r--   0      501       20    18015 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/color.py
--rw-r--r--   0      501       20     1054 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/color_triplet.py
--rw-r--r--   0      501       20     7131 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/columns.py
--rw-r--r--   0      501       20    97992 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/console.py
--rw-r--r--   0      501       20     1288 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/constrain.py
--rw-r--r--   0      501       20     5497 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/containers.py
--rw-r--r--   0      501       20     6630 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/control.py
--rw-r--r--   0      501       20     7954 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/default_styles.py
--rw-r--r--   0      501       20      972 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/diagnose.py
--rw-r--r--   0      501       20     2501 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/emoji.py
--rw-r--r--   0      501       20      642 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/errors.py
--rw-r--r--   0      501       20     1616 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/file_proxy.py
--rw-r--r--   0      501       20     2508 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/filesize.py
--rw-r--r--   0      501       20     9585 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/highlighter.py
--rw-r--r--   0      501       20     5053 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/json.py
--rw-r--r--   0      501       20     3252 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/jupyter.py
--rw-r--r--   0      501       20    14007 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/layout.py
--rw-r--r--   0      501       20    14172 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/live.py
--rw-r--r--   0      501       20     3667 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/live_render.py
--rw-r--r--   0      501       20    11903 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/logging.py
--rw-r--r--   0      501       20     8198 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/markup.py
--rw-r--r--   0      501       20     5305 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/measure.py
--rw-r--r--   0      501       20     4970 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/padding.py
--rw-r--r--   0      501       20      828 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/pager.py
--rw-r--r--   0      501       20     3396 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/palette.py
--rw-r--r--   0      501       20    10574 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/panel.py
--rw-r--r--   0      501       20    37414 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/pretty.py
--rw-r--r--   0      501       20    59836 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/progress.py
--rw-r--r--   0      501       20     8165 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/progress_bar.py
--rw-r--r--   0      501       20    11303 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/prompt.py
--rw-r--r--   0      501       20     1391 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/protocol.py
--rw-r--r--   0      501       20      166 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/region.py
--rw-r--r--   0      501       20     4436 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/repr.py
--rw-r--r--   0      501       20     4773 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/rule.py
--rw-r--r--   0      501       20     2843 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/scope.py
--rw-r--r--   0      501       20     1591 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/screen.py
--rw-r--r--   0      501       20    24224 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/segment.py
--rw-r--r--   0      501       20     4374 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/spinner.py
--rw-r--r--   0      501       20     4425 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/status.py
--rw-r--r--   0      501       20    26332 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/style.py
--rw-r--r--   0      501       20     1258 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/styled.py
--rw-r--r--   0      501       20    34995 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/syntax.py
--rw-r--r--   0      501       20    39684 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/table.py
--rw-r--r--   0      501       20     3370 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/terminal_theme.py
--rw-r--r--   0      501       20    45686 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/text.py
--rw-r--r--   0      501       20     3627 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/theme.py
--rw-r--r--   0      501       20      102 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/themes.py
--rw-r--r--   0      501       20    26070 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/traceback.py
--rw-r--r--   0      501       20     9169 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/tree.py
--rw-r--r--   0      501       20    34549 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/six.py
--rw-r--r--   0      501       20    18364 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/__init__.py
--rw-r--r--   0      501       20     3314 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/_asyncio.py
--rw-r--r--   0      501       20     1944 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/_utils.py
--rw-r--r--   0      501       20     1496 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/after.py
--rw-r--r--   0      501       20     1376 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/before.py
--rw-r--r--   0      501       20     1908 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/before_sleep.py
--rw-r--r--   0      501       20     1383 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/nap.py
--rw-r--r--   0      501       20     7550 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/retry.py
--rw-r--r--   0      501       20     2790 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/stop.py
--rw-r--r--   0      501       20     2145 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/tornadoweb.py
--rw-r--r--   0      501       20     8011 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/wait.py
--rw-r--r--   0      501       20      396 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/__init__.py
--rw-r--r--   0      501       20    22633 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_parser.py
--rw-r--r--   0      501       20     2943 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_re.py
--rw-r--r--   0      501       20      254 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_types.py
--rw-r--r--   0      501       20    80114 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/typing_extensions.py
--rw-r--r--   0      501       20     3333 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/__init__.py
--rw-r--r--   0      501       20    10811 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/_collections.py
--rw-r--r--   0      501       20       64 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/_version.py
--rw-r--r--   0      501       20    20070 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/connection.py
--rw-r--r--   0      501       20    39095 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/connectionpool.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/__init__.py
--rw-r--r--   0      501       20      957 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_appengine_environ.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/__init__.py
--rw-r--r--   0      501       20    17632 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/bindings.py
--rw-r--r--   0      501       20    13922 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/low_level.py
--rw-r--r--   0      501       20    11036 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/appengine.py
--rw-r--r--   0      501       20     4528 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/ntlmpool.py
--rw-r--r--   0      501       20    17081 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py
--rw-r--r--   0      501       20    34448 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/securetransport.py
--rw-r--r--   0      501       20     7097 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/socks.py
--rw-r--r--   0      501       20     8217 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/exceptions.py
--rw-r--r--   0      501       20     8579 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/fields.py
--rw-r--r--   0      501       20     2440 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/filepost.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/__init__.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/backports/__init__.py
--rw-r--r--   0      501       20     1417 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/backports/makefile.py
--rw-r--r--   0      501       20    34665 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/six.py
--rw-r--r--   0      501       20    19786 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/poolmanager.py
--rw-r--r--   0      501       20     5985 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/request.py
--rw-r--r--   0      501       20    30641 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/response.py
--rw-r--r--   0      501       20     1155 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/__init__.py
--rw-r--r--   0      501       20     4901 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/connection.py
--rw-r--r--   0      501       20     1605 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/proxy.py
--rw-r--r--   0      501       20      498 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/queue.py
--rw-r--r--   0      501       20     3997 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/request.py
--rw-r--r--   0      501       20     3510 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/response.py
--rw-r--r--   0      501       20    22003 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/retry.py
--rw-r--r--   0      501       20    17177 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssl_.py
--rw-r--r--   0      501       20     5758 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssl_match_hostname.py
--rw-r--r--   0      501       20     6895 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssltransport.py
--rw-r--r--   0      501       20    10003 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/timeout.py
--rw-r--r--   0      501       20    14298 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/url.py
--rw-r--r--   0      501       20     5403 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/wait.py
--rw-r--r--   0      501       20      476 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/vendor.txt
--rw-r--r--   0      501       20    10579 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/__init__.py
--rw-r--r--   0      501       20     8979 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/labels.py
--rw-r--r--   0      501       20     1305 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/mklabels.py
--rw-r--r--   0      501       20     6563 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/tests.py
--rw-r--r--   0      501       20     4307 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/x_user_defined.py
--rw-r--r--   0      501       20      286 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/py.typed
--rw-r--r--   0      501       20        4 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/INSTALLER
--rw-r--r--   0      501       20     1093 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/LICENSE.txt
--rw-r--r--   0      501       20     4072 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/METADATA
--rw-r--r--   0      501       20    76671 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/RECORD
--rw-r--r--   0      501       20        0 2023-07-23 15:01:50.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/REQUESTED
--rw-r--r--   0      501       20       92 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/WHEEL
--rw-r--r--   0      501       20      124 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/entry_points.txt
--rw-r--r--   0      501       20        4 2023-07-23 15:01:49.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/top_level.txt
--rw-r--r--   0      501       20   108570 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/__init__.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/__init__.py
--rw-r--r--   0      501       20    24701 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/appdirs.py
--rw-r--r--   0      501       20      720 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/__about__.py
--rw-r--r--   0      501       20      513 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/__init__.py
--rw-r--r--   0      501       20      860 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/_compat.py
--rw-r--r--   0      501       20     1416 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/_structures.py
--rw-r--r--   0      501       20     8248 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/markers.py
--rw-r--r--   0      501       20     4355 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/requirements.py
--rw-r--r--   0      501       20    28025 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/specifiers.py
--rw-r--r--   0      501       20      421 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/utils.py
--rw-r--r--   0      501       20    11556 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/version.py
--rw-r--r--   0      501       20   232055 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/pyparsing.py
--rw-r--r--   0      501       20    30098 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/six.py
--rw-r--r--   0      501       20     2101 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/extern/__init__.py
--rw-r--r--   0      501       20      396 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/py2_warn.py
--rw-r--r--   0      501       20      558 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/py31compat.py
--rw-r--r--   0      501       20     7341 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/__init__.py
--rw-r--r--   0      501       20      218 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_deprecation_warning.py
--rw-r--r--   0      501       20     2388 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_imp.py
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/__init__.py
--rw-r--r--   0      501       20    15130 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/ordered_set.py
--rw-r--r--   0      501       20      744 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/__about__.py
--rw-r--r--   0      501       20      562 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/__init__.py
--rw-r--r--   0      501       20      865 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/_compat.py
--rw-r--r--   0      501       20     1416 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/_structures.py
--rw-r--r--   0      501       20     8268 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/markers.py
--rw-r--r--   0      501       20     4742 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/requirements.py
--rw-r--r--   0      501       20    27778 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/specifiers.py
--rw-r--r--   0      501       20    12933 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/tags.py
--rw-r--r--   0      501       20     1520 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/utils.py
--rw-r--r--   0      501       20    11978 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/version.py
--rw-r--r--   0      501       20   232055 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/pyparsing.py
--rw-r--r--   0      501       20    30098 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/six.py
--rw-r--r--   0      501       20     6626 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/archive_util.py
--rw-r--r--   0      501       20     9960 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/build_meta.py
--rw-r--r--   0      501       20    65536 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli-32.exe
--rw-r--r--   0      501       20    74752 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli-64.exe
--rw-r--r--   0      501       20    65536 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli.exe
--rw-r--r--   0      501       20      568 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/__init__.py
--rw-r--r--   0      501       20     2426 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/alias.py
--rw-r--r--   0      501       20    18406 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_egg.py
--rw-r--r--   0      501       20     1508 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_rpm.py
--rw-r--r--   0      501       20      922 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_wininst.py
--rw-r--r--   0      501       20     4415 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_clib.py
--rw-r--r--   0      501       20    13048 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_ext.py
--rw-r--r--   0      501       20     9737 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_py.py
--rw-r--r--   0      501       20     8188 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/develop.py
--rw-r--r--   0      501       20      960 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/dist_info.py
--rw-r--r--   0      501       20    87657 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/easy_install.py
--rw-r--r--   0      501       20    25548 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/egg_info.py
--rw-r--r--   0      501       20     4705 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install.py
--rw-r--r--   0      501       20     2203 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_egg_info.py
--rw-r--r--   0      501       20     3875 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_lib.py
--rw-r--r--   0      501       20     2519 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_scripts.py
--rw-r--r--   0      501       20      628 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/launcher manifest.xml
--rw-r--r--   0      501       20     4994 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/py36compat.py
--rw-r--r--   0      501       20      468 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/register.py
--rw-r--r--   0      501       20     2164 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/rotate.py
--rw-r--r--   0      501       20      658 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/saveopts.py
--rw-r--r--   0      501       20     8092 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/sdist.py
--rw-r--r--   0      501       20     5085 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/setopt.py
--rw-r--r--   0      501       20     9623 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/test.py
--rw-r--r--   0      501       20      462 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/upload.py
--rw-r--r--   0      501       20     7314 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/upload_docs.py
--rw-r--r--   0      501       20    21757 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/config.py
--rw-r--r--   0      501       20      949 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/dep_util.py
--rw-r--r--   0      501       20     5517 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/depends.py
--rw-r--r--   0      501       20    39211 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/dist.py
--rw-r--r--   0      501       20      524 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/errors.py
--rw-r--r--   0      501       20     1729 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/extension.py
--rw-r--r--   0      501       20     2128 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/extern/__init__.py
--rw-r--r--   0      501       20     5084 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/glob.py
--rw-r--r--   0      501       20    65536 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui-32.exe
--rw-r--r--   0      501       20    75264 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui-64.exe
--rw-r--r--   0      501       20    65536 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui.exe
--rw-r--r--   0      501       20     5336 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/installer.py
--rw-r--r--   0      501       20      787 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/launch.py
--rw-r--r--   0      501       20     2384 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/lib2to3_ex.py
--rw-r--r--   0      501       20     5264 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/monkey.py
--rw-r--r--   0      501       20    50989 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/msvc.py
--rw-r--r--   0      501       20     3223 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/namespaces.py
--rw-r--r--   0      501       20    40737 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/package_index.py
--rw-r--r--   0      501       20     1504 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py27compat.py
--rw-r--r--   0      501       20      838 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py31compat.py
--rw-r--r--   0      501       20     1330 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py33compat.py
--rw-r--r--   0      501       20      245 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py34compat.py
--rw-r--r--   0      501       20    14284 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/sandbox.py
--rw-r--r--   0      501       20      218 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/script (dev).tmpl
--rw-r--r--   0      501       20      138 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/script.tmpl
--rw-r--r--   0      501       20     2346 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/site-patch.py
--rw-r--r--   0      501       20     8543 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/ssl_support.py
--rw-r--r--   0      501       20      996 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/unicode_utils.py
--rw-r--r--   0      501       20      144 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/version.py
--rw-r--r--   0      501       20     8371 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/wheel.py
--rw-r--r--   0      501       20      714 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/windows_support.py
--rw-r--r--   0      501       20        4 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/INSTALLER
--rw-r--r--   0      501       20     1078 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/LICENSE
--rw-r--r--   0      501       20     4806 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/METADATA
--rw-r--r--   0      501       20    14645 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/RECORD
--rw-r--r--   0      501       20        0 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/REQUESTED
--rw-r--r--   0      501       20       92 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/WHEEL
--rw-r--r--   0      501       20      239 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/dependency_links.txt
--rw-r--r--   0      501       20     3143 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/entry_points.txt
--rw-r--r--   0      501       20       38 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/top_level.txt
--rw-r--r--   0      501       20        1 2023-07-23 15:01:48.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/zip-safe
--rw-r--r--   0      501       20      113 2023-07-23 15:01:46.000000 klvm_rs-0.1.24/local_dependencies/klvmr/venv/pyvenv.cfg
--rw-r--r--   0        0        0      588 1970-01-01 00:00:00.000000 klvm_rs-0.1.24/Cargo.toml
--rw-r--r--   0      501       20      606 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/README.md
--rw-r--r--   0      501       20      106 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/pyproject.toml
--rw-r--r--   0      501       20     1007 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/src/adapt_response.rs
--rw-r--r--   0      501       20      862 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/src/api.rs
--rw-r--r--   0      501       20     1379 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/src/lazy_node.rs
--rw-r--r--   0      501       20       73 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/src/lib.rs
--rw-r--r--   0      501       20      107 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/src/mod.rs
--rw-r--r--   0      501       20     2642 2023-07-23 15:01:27.000000 klvm_rs-0.1.24/src/run_program.rs
--rw-r--r--   0      501       20    14645 2023-07-23 15:01:51.000000 klvm_rs-0.1.24/Cargo.lock
--rw-r--r--   0        0        0     1027 1970-01-01 00:00:00.000000 klvm_rs-0.1.24/PKG-INFO
+-rw-r--r--   0        0        0     1362 1970-01-01 00:00:00.000000 klvm_rs-0.2.8/local_dependencies/klvmr/Cargo.toml
+-rw-r--r--   0      501       20      224 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.cargo/config
+-rw-r--r--   0      501       20      290 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/audit-check.yaml.bak
+-rw-r--r--   0      501       20     3179 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/benchmark.yml.bak
+-rw-r--r--   0      501       20     2812 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/build-arm64-wheels.yml.bak
+-rw-r--r--   0      501       20     1136 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/build-crate.yml
+-rw-r--r--   0      501       20     3777 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/build-m1-wheel.yml.bak
+-rw-r--r--   0      501       20     1056 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/build-npm.yml
+-rw-r--r--   0      501       20     9614 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/build-test.yml
+-rw-r--r--   0      501       20      885 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/dependency-review.yml.bak
+-rw-r--r--   0      501       20        8 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/.gitignore
+-rw-r--r--   0      501       20    11357 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/LICENSE
+-rw-r--r--   0      501       20      912 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/README.md
+-rw-r--r--   0      501       20      619 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/RELEASE.md
+-rw-r--r--   0      501       20     2219 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/activate
+-rw-r--r--   0      501       20        3 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/block-2000.envhex
+-rw-r--r--   0      501       20  1560006 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/block-2000.hex
+-rwxr-xr-x   0      501       20     4090 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/cmp.py
+-rw-r--r--   0      501       20     1771 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/compressed-2000.envhex
+-rw-r--r--   0      501       20   596274 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/compressed-2000.hex
+-rw-r--r--   0      501       20       20 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/concat.env
+-rw-r--r--   0      501       20      509 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/concat.klvm
+-rw-r--r--   0      501       20      320 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/count-even.klvm
+-rw-r--r--   0      501       20        8 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/factorial.env
+-rw-r--r--   0      501       20      247 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/factorial.klvm
+-rw-r--r--   0      501       20       51 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/hash-string.klvm
+-rw-r--r--   0      501       20      246 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/hash-tree.klvm
+-rw-r--r--   0      501       20      401 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/large-block.klvm
+-rw-r--r--   0      501       20       10 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_add.env
+-rw-r--r--   0      501       20      193 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_add.klvm
+-rw-r--r--   0      501       20       10 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_ior.env
+-rw-r--r--   0      501       20      183 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_ior.klvm
+-rw-r--r--   0      501       20       10 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_not.env
+-rw-r--r--   0      501       20      224 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_not.klvm
+-rw-r--r--   0      501       20       10 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_sub.env
+-rw-r--r--   0      501       20      193 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_sub.klvm
+-rw-r--r--   0      501       20       10 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_xor.env
+-rw-r--r--   0      501       20      207 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/loop_xor.klvm
+-rw-r--r--   0      501       20     1793 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/matrix-multiply.klvm
+-rw-r--r--   0      501       20      106 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/point-pow.env
+-rw-r--r--   0      501       20      288 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/point-pow.klvm
+-rw-r--r--   0      501       20      318 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/pubkey-tree.klvm
+-rwxr-xr-x   0      501       20     8166 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/run-benchmark.py
+-rw-r--r--   0      501       20      292 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/shift-left.klvm
+-rw-r--r--   0      501       20      488 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/substr-tree.klvm
+-rw-r--r--   0      501       20      390 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/substr.klvm
+-rw-r--r--   0      501       20      237 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/sum-tree.klvm
+-rw-r--r--   0      501       20     3976 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/benchmarks.txt
+-rw-r--r--   0      501       20     2273 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/docs/new-operator-checklist.md
+-rw-r--r--   0      501       20    33096 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-bls-ops.txt
+-rw-r--r--   0      501       20     1286 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-bls-zk.txt
+-rw-r--r--   0      501       20    31892 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-blspy-g1.txt
+-rw-r--r--   0      501       20    60143 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-blspy-g2.txt
+-rw-r--r--   0      501       20    52970 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-blspy-hash.txt
+-rw-r--r--   0      501       20    43673 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-blspy-pairing.txt
+-rw-r--r--   0      501       20    23174 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-blspy-verify.txt
+-rw-r--r--   0      501       20     3784 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-core-ops.txt
+-rw-r--r--   0      501       20    19990 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-modpow.txt
+-rw-r--r--   0      501       20    69027 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-more-ops.txt
+-rw-r--r--   0      501       20     7730 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-secp-verify.txt
+-rw-r--r--   0      501       20    11662 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-secp256k1.txt
+-rw-r--r--   0      501       20    11662 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/op-tests/test-secp256r1.txt
+-rw-r--r--   0      501       20    32259 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/allocator.rs
+-rw-r--r--   0      501       20    12386 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/bls_ops.rs
+-rw-r--r--   0      501       20     7590 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/chik_dialect.rs
+-rw-r--r--   0      501       20     2911 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/core_ops.rs
+-rw-r--r--   0      501       20      289 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/cost.rs
+-rw-r--r--   0      501       20      604 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/dialect.rs
+-rw-r--r--   0      501       20      164 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/err_utils.rs
+-rw-r--r--   0      501       20     3265 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/f_table.rs
+-rw-r--r--   0      501       20      859 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/lib.rs
+-rw-r--r--   0      501       20    29171 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/more_ops.rs
+-rw-r--r--   0      501       20    10320 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/number.rs
+-rw-r--r--   0      501       20    19055 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/op_utils.rs
+-rw-r--r--   0      501       20      403 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/reduction.rs
+-rw-r--r--   0      501       20    50428 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/run_program.rs
+-rw-r--r--   0      501       20     1874 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/runtime_dialect.rs
+-rw-r--r--   0      501       20     2755 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/secp_ops.rs
+-rw-r--r--   0      501       20      383 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/bytes32.rs
+-rw-r--r--   0      501       20     1408 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/de.rs
+-rw-r--r--   0      501       20     4175 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/de_br.rs
+-rw-r--r--   0      501       20    11385 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/de_tree.rs
+-rw-r--r--   0      501       20      221 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/errors.rs
+-rw-r--r--   0      501       20      458 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/mod.rs
+-rw-r--r--   0      501       20     9793 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/object_cache.rs
+-rw-r--r--   0      501       20     7154 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/parse_atom.rs
+-rw-r--r--   0      501       20    14106 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/read_cache_lookup.rs
+-rw-r--r--   0      501       20     2897 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/ser.rs
+-rw-r--r--   0      501       20     2810 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/ser_br.rs
+-rw-r--r--   0      501       20     2414 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/test.rs
+-rw-r--r--   0      501       20    18846 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/tools.rs
+-rw-r--r--   0      501       20      596 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/utils.rs
+-rw-r--r--   0      501       20     6233 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/serde/write_atom.rs
+-rw-r--r--   0      501       20     1341 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/sha2.rs
+-rw-r--r--   0      501       20    17083 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/test_ops.rs
+-rw-r--r--   0      501       20     3763 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/tests.rs
+-rw-r--r--   0      501       20     5235 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/src/traverse_path.rs
+-rwxr-xr-x   0      501       20     8264 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/tests/generate-programs.py
+-rwxr-xr-x   0      501       20     3008 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/tests/run-programs.py
+-rwxr-xr-x   0      501       20     1543 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/local_dependencies/klvmr/tests/run.py
+-rw-r--r--   0      501       20     2219 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/activate
+-rw-r--r--   0      501       20     1271 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/activate.csh
+-rw-r--r--   0      501       20     2423 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/activate.fish
+-rwxr-xr-x   0      501       20      264 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/easy_install
+-rwxr-xr-x   0      501       20      264 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/easy_install-3.7
+-rwxr-xr-x   0      501       20      255 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/pip
+-rwxr-xr-x   0      501       20      255 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/pip3
+-rwxr-xr-x   0      501       20      255 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/pip3.7
+-rwxr-xr-x   0      501       20    49640 2023-07-10 04:30:11.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/python
+-rwxr-xr-x   0      501       20    49640 2023-07-10 04:30:11.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/python3
+-rw-r--r--   0      501       20      126 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/easy_install.py
+-rw-r--r--   0      501       20      357 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__init__.py
+-rw-r--r--   0      501       20     1198 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__main__.py
+-rw-r--r--   0      501       20     1444 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__pip-runner__.py
+-rw-r--r--   0      501       20      573 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/__init__.py
+-rw-r--r--   0      501       20    10243 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/build_env.py
+-rw-r--r--   0      501       20    10734 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cache.py
+-rw-r--r--   0      501       20      132 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/__init__.py
+-rw-r--r--   0      501       20     6676 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/autocompletion.py
+-rw-r--r--   0      501       20     7842 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/base_command.py
+-rw-r--r--   0      501       20    29497 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/cmdoptions.py
+-rw-r--r--   0      501       20      774 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/command_context.py
+-rw-r--r--   0      501       20     2472 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/main.py
+-rw-r--r--   0      501       20     4338 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/main_parser.py
+-rw-r--r--   0      501       20    10817 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/parser.py
+-rw-r--r--   0      501       20     1968 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/progress_bars.py
+-rw-r--r--   0      501       20    18172 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/req_command.py
+-rw-r--r--   0      501       20     5118 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/spinners.py
+-rw-r--r--   0      501       20      116 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/status_codes.py
+-rw-r--r--   0      501       20     3882 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/__init__.py
+-rw-r--r--   0      501       20     7582 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/cache.py
+-rw-r--r--   0      501       20     1685 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/check.py
+-rw-r--r--   0      501       20     4129 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/completion.py
+-rw-r--r--   0      501       20     9815 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/configuration.py
+-rw-r--r--   0      501       20     6591 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/debug.py
+-rw-r--r--   0      501       20     5289 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/download.py
+-rw-r--r--   0      501       20     2951 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/freeze.py
+-rw-r--r--   0      501       20     1703 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/hash.py
+-rw-r--r--   0      501       20     1132 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/help.py
+-rw-r--r--   0      501       20     4793 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/index.py
+-rw-r--r--   0      501       20     3188 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/inspect.py
+-rw-r--r--   0      501       20    32389 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/install.py
+-rw-r--r--   0      501       20    12343 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/list.py
+-rw-r--r--   0      501       20     5697 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/search.py
+-rw-r--r--   0      501       20     6419 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/show.py
+-rw-r--r--   0      501       20     3886 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/uninstall.py
+-rw-r--r--   0      501       20     7396 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/wheel.py
+-rw-r--r--   0      501       20    13529 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/configuration.py
+-rw-r--r--   0      501       20      858 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/__init__.py
+-rw-r--r--   0      501       20     1221 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/base.py
+-rw-r--r--   0      501       20      729 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/installed.py
+-rw-r--r--   0      501       20     6494 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/sdist.py
+-rw-r--r--   0      501       20     1164 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/wheel.py
+-rw-r--r--   0      501       20    24244 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/exceptions.py
+-rw-r--r--   0      501       20       30 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/__init__.py
+-rw-r--r--   0      501       20    16504 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/collector.py
+-rw-r--r--   0      501       20    37873 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/package_finder.py
+-rw-r--r--   0      501       20     6557 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/sources.py
+-rw-r--r--   0      501       20    15365 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/__init__.py
+-rw-r--r--   0      501       20     6100 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/_distutils.py
+-rw-r--r--   0      501       20     7680 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/_sysconfig.py
+-rw-r--r--   0      501       20     2556 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/base.py
+-rw-r--r--   0      501       20      340 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/main.py
+-rw-r--r--   0      501       20     4280 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/__init__.py
+-rw-r--r--   0      501       20     2595 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/_json.py
+-rw-r--r--   0      501       20    25277 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/base.py
+-rw-r--r--   0      501       20      107 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/__init__.py
+-rw-r--r--   0      501       20     1882 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_compat.py
+-rw-r--r--   0      501       20     8181 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_dists.py
+-rw-r--r--   0      501       20     7457 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_envs.py
+-rw-r--r--   0      501       20     9773 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/pkg_resources.py
+-rw-r--r--   0      501       20       63 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/__init__.py
+-rw-r--r--   0      501       20      990 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/candidate.py
+-rw-r--r--   0      501       20     6626 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/direct_url.py
+-rw-r--r--   0      501       20     2520 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/format_control.py
+-rw-r--r--   0      501       20     1030 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/index.py
+-rw-r--r--   0      501       20     2617 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/installation_report.py
+-rw-r--r--   0      501       20    18602 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/link.py
+-rw-r--r--   0      501       20      738 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/scheme.py
+-rw-r--r--   0      501       20     4644 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/search_scope.py
+-rw-r--r--   0      501       20     1907 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/selection_prefs.py
+-rw-r--r--   0      501       20     3858 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/target_python.py
+-rw-r--r--   0      501       20     3600 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/wheel.py
+-rw-r--r--   0      501       20       50 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/__init__.py
+-rw-r--r--   0      501       20    16507 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/auth.py
+-rw-r--r--   0      501       20     2145 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/cache.py
+-rw-r--r--   0      501       20     6096 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/download.py
+-rw-r--r--   0      501       20     7638 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/lazy_wheel.py
+-rw-r--r--   0      501       20    18443 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/session.py
+-rw-r--r--   0      501       20     4073 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/utils.py
+-rw-r--r--   0      501       20     1791 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/xmlrpc.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/__init__.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/__init__.py
+-rw-r--r--   0      501       20     4133 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/build_tracker.py
+-rw-r--r--   0      501       20     1422 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata.py
+-rw-r--r--   0      501       20     1474 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata_editable.py
+-rw-r--r--   0      501       20     2198 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata_legacy.py
+-rw-r--r--   0      501       20     1075 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel.py
+-rw-r--r--   0      501       20     1417 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel_editable.py
+-rw-r--r--   0      501       20     3064 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel_legacy.py
+-rw-r--r--   0      501       20     5122 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/check.py
+-rw-r--r--   0      501       20     9784 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/freeze.py
+-rw-r--r--   0      501       20       51 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/__init__.py
+-rw-r--r--   0      501       20     1354 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/editable_legacy.py
+-rw-r--r--   0      501       20     4105 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/legacy.py
+-rw-r--r--   0      501       20    27407 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/wheel.py
+-rw-r--r--   0      501       20    25091 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/prepare.py
+-rw-r--r--   0      501       20     6987 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/pyproject.py
+-rw-r--r--   0      501       20     2807 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/__init__.py
+-rw-r--r--   0      501       20    16611 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/constructors.py
+-rw-r--r--   0      501       20    17646 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_file.py
+-rw-r--r--   0      501       20    35763 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_install.py
+-rw-r--r--   0      501       20     2858 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_set.py
+-rw-r--r--   0      501       20    24045 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_uninstall.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/__init__.py
+-rw-r--r--   0      501       20      583 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/base.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/legacy/__init__.py
+-rw-r--r--   0      501       20    24129 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/legacy/resolver.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/__init__.py
+-rw-r--r--   0      501       20     5220 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/base.py
+-rw-r--r--   0      501       20    18963 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/candidates.py
+-rw-r--r--   0      501       20    27878 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/factory.py
+-rw-r--r--   0      501       20     5705 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/found_candidates.py
+-rw-r--r--   0      501       20     9914 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/provider.py
+-rw-r--r--   0      501       20     2526 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/reporter.py
+-rw-r--r--   0      501       20     5455 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/requirements.py
+-rw-r--r--   0      501       20    11533 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/resolver.py
+-rw-r--r--   0      501       20     8167 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/self_outdated_check.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/__init__.py
+-rw-r--r--   0      501       20     1015 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/_log.py
+-rw-r--r--   0      501       20     1665 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/appdirs.py
+-rw-r--r--   0      501       20     1884 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/compat.py
+-rw-r--r--   0      501       20     5377 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/compatibility_tags.py
+-rw-r--r--   0      501       20      242 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/datetime.py
+-rw-r--r--   0      501       20     5764 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/deprecation.py
+-rw-r--r--   0      501       20     3206 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/direct_url_helpers.py
+-rw-r--r--   0      501       20     1115 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/distutils_args.py
+-rw-r--r--   0      501       20     2118 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/egg_link.py
+-rw-r--r--   0      501       20     1169 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/encoding.py
+-rw-r--r--   0      501       20     3064 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/entrypoints.py
+-rw-r--r--   0      501       20     5122 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/filesystem.py
+-rw-r--r--   0      501       20      716 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/filetypes.py
+-rw-r--r--   0      501       20     3110 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/glibc.py
+-rw-r--r--   0      501       20     4831 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/hashes.py
+-rw-r--r--   0      501       20      795 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/inject_securetransport.py
+-rw-r--r--   0      501       20    11632 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/logging.py
+-rw-r--r--   0      501       20    22253 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/misc.py
+-rw-r--r--   0      501       20     1193 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/models.py
+-rw-r--r--   0      501       20     2108 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/packaging.py
+-rw-r--r--   0      501       20     5662 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/setuptools_build.py
+-rw-r--r--   0      501       20     9200 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/subprocess.py
+-rw-r--r--   0      501       20     7702 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/temp_dir.py
+-rw-r--r--   0      501       20     8821 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/unpacking.py
+-rw-r--r--   0      501       20     1759 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/urls.py
+-rw-r--r--   0      501       20     3456 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/virtualenv.py
+-rw-r--r--   0      501       20     4549 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/wheel.py
+-rw-r--r--   0      501       20      596 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/__init__.py
+-rw-r--r--   0      501       20     3519 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/bazaar.py
+-rw-r--r--   0      501       20    18116 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/git.py
+-rw-r--r--   0      501       20     5238 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/mercurial.py
+-rw-r--r--   0      501       20    11729 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/subversion.py
+-rw-r--r--   0      501       20    22811 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/versioncontrol.py
+-rw-r--r--   0      501       20    13079 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/wheel_builder.py
+-rw-r--r--   0      501       20     4966 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/__init__.py
+-rw-r--r--   0      501       20      465 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/__init__.py
+-rw-r--r--   0      501       20     1379 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/_cmd.py
+-rw-r--r--   0      501       20     5033 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/adapter.py
+-rw-r--r--   0      501       20     1535 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/cache.py
+-rw-r--r--   0      501       20      242 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/__init__.py
+-rw-r--r--   0      501       20     5271 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/file_cache.py
+-rw-r--r--   0      501       20     1033 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/redis_cache.py
+-rw-r--r--   0      501       20      778 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/compat.py
+-rw-r--r--   0      501       20    16416 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/controller.py
+-rw-r--r--   0      501       20     3946 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/filewrapper.py
+-rw-r--r--   0      501       20     4154 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/heuristics.py
+-rw-r--r--   0      501       20     7105 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/serialize.py
+-rw-r--r--   0      501       20      774 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/wrapper.py
+-rw-r--r--   0      501       20       94 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/__init__.py
+-rw-r--r--   0      501       20      255 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/__main__.py
+-rw-r--r--   0      501       20   275233 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/cacert.pem
+-rw-r--r--   0      501       20     4279 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/core.py
+-rw-r--r--   0      501       20     4797 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/__init__.py
+-rw-r--r--   0      501       20    31274 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/big5freq.py
+-rw-r--r--   0      501       20     1763 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/big5prober.py
+-rw-r--r--   0      501       20    10032 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/chardistribution.py
+-rw-r--r--   0      501       20     3915 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/charsetgroupprober.py
+-rw-r--r--   0      501       20     5420 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/charsetprober.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cli/__init__.py
+-rw-r--r--   0      501       20     3242 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cli/chardetect.py
+-rw-r--r--   0      501       20     3732 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/codingstatemachine.py
+-rw-r--r--   0      501       20      542 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/codingstatemachinedict.py
+-rw-r--r--   0      501       20     1860 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cp949prober.py
+-rw-r--r--   0      501       20     1683 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/enums.py
+-rw-r--r--   0      501       20     4006 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/escprober.py
+-rw-r--r--   0      501       20    12176 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/escsm.py
+-rw-r--r--   0      501       20     3934 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/eucjpprober.py
+-rw-r--r--   0      501       20    13566 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euckrfreq.py
+-rw-r--r--   0      501       20     1753 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euckrprober.py
+-rw-r--r--   0      501       20    36913 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euctwfreq.py
+-rw-r--r--   0      501       20     1753 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euctwprober.py
+-rw-r--r--   0      501       20    20735 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/gb2312freq.py
+-rw-r--r--   0      501       20     1759 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/gb2312prober.py
+-rw-r--r--   0      501       20    14537 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/hebrewprober.py
+-rw-r--r--   0      501       20    25796 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/jisfreq.py
+-rw-r--r--   0      501       20    42498 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/johabfreq.py
+-rw-r--r--   0      501       20     1752 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/johabprober.py
+-rw-r--r--   0      501       20    27055 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/jpcntx.py
+-rw-r--r--   0      501       20   104562 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langbulgarianmodel.py
+-rw-r--r--   0      501       20    98484 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langgreekmodel.py
+-rw-r--r--   0      501       20    98196 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langhebrewmodel.py
+-rw-r--r--   0      501       20   101363 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langhungarianmodel.py
+-rw-r--r--   0      501       20   128035 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langrussianmodel.py
+-rw-r--r--   0      501       20   102774 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langthaimodel.py
+-rw-r--r--   0      501       20    95372 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langturkishmodel.py
+-rw-r--r--   0      501       20     5380 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/latin1prober.py
+-rw-r--r--   0      501       20     6077 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/macromanprober.py
+-rw-r--r--   0      501       20     3715 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcharsetprober.py
+-rw-r--r--   0      501       20     2131 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcsgroupprober.py
+-rw-r--r--   0      501       20    30391 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcssm.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/metadata/__init__.py
+-rw-r--r--   0      501       20    13560 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/metadata/languages.py
+-rw-r--r--   0      501       20      402 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/resultdict.py
+-rw-r--r--   0      501       20     6400 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sbcharsetprober.py
+-rw-r--r--   0      501       20     4137 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sbcsgroupprober.py
+-rw-r--r--   0      501       20     4007 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sjisprober.py
+-rw-r--r--   0      501       20    14848 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/universaldetector.py
+-rw-r--r--   0      501       20     8505 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/utf1632prober.py
+-rw-r--r--   0      501       20     2812 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/utf8prober.py
+-rw-r--r--   0      501       20      244 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/version.py
+-rw-r--r--   0      501       20      266 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/__init__.py
+-rw-r--r--   0      501       20     2522 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/ansi.py
+-rw-r--r--   0      501       20    11128 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/ansitowin32.py
+-rw-r--r--   0      501       20     3325 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/initialise.py
+-rw-r--r--   0      501       20       75 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/__init__.py
+-rw-r--r--   0      501       20     2839 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/ansi_test.py
+-rw-r--r--   0      501       20    10678 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/ansitowin32_test.py
+-rw-r--r--   0      501       20     6741 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/initialise_test.py
+-rw-r--r--   0      501       20     1866 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/isatty_test.py
+-rw-r--r--   0      501       20     1079 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/utils.py
+-rw-r--r--   0      501       20     3709 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/winterm_test.py
+-rw-r--r--   0      501       20     6181 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/win32.py
+-rw-r--r--   0      501       20     7134 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/winterm.py
+-rw-r--r--   0      501       20      581 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/__init__.py
+-rw-r--r--   0      501       20    41259 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/compat.py
+-rw-r--r--   0      501       20    51697 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/database.py
+-rw-r--r--   0      501       20    20834 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/index.py
+-rw-r--r--   0      501       20    51991 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/locators.py
+-rw-r--r--   0      501       20    14811 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/manifest.py
+-rw-r--r--   0      501       20     5058 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/markers.py
+-rw-r--r--   0      501       20    39801 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/metadata.py
+-rw-r--r--   0      501       20    10820 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/resources.py
+-rw-r--r--   0      501       20    18102 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/scripts.py
+-rw-r--r--   0      501       20    97792 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t32.exe
+-rw-r--r--   0      501       20   182784 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t64-arm.exe
+-rw-r--r--   0      501       20   108032 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t64.exe
+-rw-r--r--   0      501       20    66262 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/util.py
+-rw-r--r--   0      501       20    23513 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/version.py
+-rw-r--r--   0      501       20    91648 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w32.exe
+-rw-r--r--   0      501       20   168448 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w64-arm.exe
+-rw-r--r--   0      501       20   101888 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w64.exe
+-rw-r--r--   0      501       20    43898 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/wheel.py
+-rw-r--r--   0      501       20      981 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/__init__.py
+-rw-r--r--   0      501       20       64 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/__main__.py
+-rw-r--r--   0      501       20    49330 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/distro.py
+-rw-r--r--   0      501       20      849 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/__init__.py
+-rw-r--r--   0      501       20     3374 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/codec.py
+-rw-r--r--   0      501       20      321 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/compat.py
+-rw-r--r--   0      501       20    12950 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/core.py
+-rw-r--r--   0      501       20    44375 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/idnadata.py
+-rw-r--r--   0      501       20     1881 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/intranges.py
+-rw-r--r--   0      501       20       21 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/package_data.py
+-rw-r--r--   0      501       20   206539 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/uts46data.py
+-rw-r--r--   0      501       20     1132 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/__init__.py
+-rw-r--r--   0      501       20     1081 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/exceptions.py
+-rw-r--r--   0      501       20     6080 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/ext.py
+-rw-r--r--   0      501       20    34557 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/fallback.py
+-rw-r--r--   0      501       20      661 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/__about__.py
+-rw-r--r--   0      501       20      497 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/__init__.py
+-rw-r--r--   0      501       20    11488 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_manylinux.py
+-rw-r--r--   0      501       20     4378 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_musllinux.py
+-rw-r--r--   0      501       20     1431 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_structures.py
+-rw-r--r--   0      501       20     8487 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/markers.py
+-rw-r--r--   0      501       20     4676 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/requirements.py
+-rw-r--r--   0      501       20    30110 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/specifiers.py
+-rw-r--r--   0      501       20    15699 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/tags.py
+-rw-r--r--   0      501       20     4200 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/utils.py
+-rw-r--r--   0      501       20    14665 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/version.py
+-rw-r--r--   0      501       20   108287 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pkg_resources/__init__.py
+-rw-r--r--   0      501       20      562 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pkg_resources/py31compat.py
+-rw-r--r--   0      501       20    12936 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/__init__.py
+-rw-r--r--   0      501       20     1176 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/__main__.py
+-rw-r--r--   0      501       20     4068 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/android.py
+-rw-r--r--   0      501       20     4910 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/api.py
+-rw-r--r--   0      501       20     2655 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/macos.py
+-rw-r--r--   0      501       20     6911 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/unix.py
+-rw-r--r--   0      501       20      160 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/version.py
+-rw-r--r--   0      501       20     6596 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/windows.py
+-rw-r--r--   0      501       20     2999 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/__init__.py
+-rw-r--r--   0      501       20      353 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/__main__.py
+-rw-r--r--   0      501       20    23685 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/cmdline.py
+-rw-r--r--   0      501       20     1697 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/console.py
+-rw-r--r--   0      501       20     1938 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/filter.py
+-rw-r--r--   0      501       20    40386 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/filters/__init__.py
+-rw-r--r--   0      501       20     2917 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatter.py
+-rw-r--r--   0      501       20     4810 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/__init__.py
+-rw-r--r--   0      501       20     4104 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/_mapping.py
+-rw-r--r--   0      501       20     3314 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/bbcode.py
+-rw-r--r--   0      501       20     5086 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/groff.py
+-rw-r--r--   0      501       20    35441 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/html.py
+-rw-r--r--   0      501       20    21938 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/img.py
+-rw-r--r--   0      501       20     5871 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/irc.py
+-rw-r--r--   0      501       20    19351 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/latex.py
+-rw-r--r--   0      501       20     5073 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/other.py
+-rw-r--r--   0      501       20     2212 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/pangomarkup.py
+-rw-r--r--   0      501       20     5014 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/rtf.py
+-rw-r--r--   0      501       20     7335 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/svg.py
+-rw-r--r--   0      501       20     4674 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/terminal.py
+-rw-r--r--   0      501       20    11753 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/terminal256.py
+-rw-r--r--   0      501       20    32005 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexer.py
+-rw-r--r--   0      501       20    11174 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/__init__.py
+-rw-r--r--   0      501       20    70232 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/_mapping.py
+-rw-r--r--   0      501       20    53376 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/python.py
+-rw-r--r--   0      501       20      986 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/modeline.py
+-rw-r--r--   0      501       20     2591 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/plugin.py
+-rw-r--r--   0      501       20     3072 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/regexopt.py
+-rw-r--r--   0      501       20     3092 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/scanner.py
+-rw-r--r--   0      501       20     4630 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/sphinxext.py
+-rw-r--r--   0      501       20     6257 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/style.py
+-rw-r--r--   0      501       20     3419 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/styles/__init__.py
+-rw-r--r--   0      501       20     6184 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/token.py
+-rw-r--r--   0      501       20    63187 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/unistring.py
+-rw-r--r--   0      501       20     9110 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/util.py
+-rw-r--r--   0      501       20     9171 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/__init__.py
+-rw-r--r--   0      501       20     6426 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/actions.py
+-rw-r--r--   0      501       20    12936 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/common.py
+-rw-r--r--   0      501       20   213344 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/core.py
+-rw-r--r--   0      501       20    23685 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/diagram/__init__.py
+-rw-r--r--   0      501       20     9023 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/exceptions.py
+-rw-r--r--   0      501       20    39129 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/helpers.py
+-rw-r--r--   0      501       20    25341 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/results.py
+-rw-r--r--   0      501       20    13402 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/testing.py
+-rw-r--r--   0      501       20    10787 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/unicode.py
+-rw-r--r--   0      501       20     6805 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/util.py
+-rw-r--r--   0      501       20      491 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/__init__.py
+-rw-r--r--   0      501       20      138 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_compat.py
+-rw-r--r--   0      501       20    11920 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_impl.py
+-rw-r--r--   0      501       20      546 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_in_process/__init__.py
+-rw-r--r--   0      501       20    10927 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py
+-rw-r--r--   0      501       20     5178 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/__init__.py
+-rw-r--r--   0      501       20      435 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/__version__.py
+-rw-r--r--   0      501       20     1397 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/_internal_utils.py
+-rw-r--r--   0      501       20    21443 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/adapters.py
+-rw-r--r--   0      501       20     6377 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/api.py
+-rw-r--r--   0      501       20    10187 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/auth.py
+-rw-r--r--   0      501       20      575 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/certs.py
+-rw-r--r--   0      501       20     1286 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/compat.py
+-rw-r--r--   0      501       20    18560 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/cookies.py
+-rw-r--r--   0      501       20     3823 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/exceptions.py
+-rw-r--r--   0      501       20     3879 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/help.py
+-rw-r--r--   0      501       20      733 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/hooks.py
+-rw-r--r--   0      501       20    35288 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/models.py
+-rw-r--r--   0      501       20      695 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/packages.py
+-rw-r--r--   0      501       20    30180 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/sessions.py
+-rw-r--r--   0      501       20     4235 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/status_codes.py
+-rw-r--r--   0      501       20     2912 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/structures.py
+-rw-r--r--   0      501       20    33240 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/utils.py
+-rw-r--r--   0      501       20      537 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/__init__.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/compat/__init__.py
+-rw-r--r--   0      501       20      156 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/compat/collections_abc.py
+-rw-r--r--   0      501       20     5872 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/providers.py
+-rw-r--r--   0      501       20     1583 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/reporters.py
+-rw-r--r--   0      501       20    17592 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/resolvers.py
+-rw-r--r--   0      501       20     4794 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/structs.py
+-rw-r--r--   0      501       20     6090 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/__init__.py
+-rw-r--r--   0      501       20     8478 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/__main__.py
+-rw-r--r--   0      501       20    10096 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_cell_widths.py
+-rw-r--r--   0      501       20   140235 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_emoji_codes.py
+-rw-r--r--   0      501       20     1064 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_emoji_replace.py
+-rw-r--r--   0      501       20     2114 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_export_format.py
+-rw-r--r--   0      501       20      265 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_extension.py
+-rw-r--r--   0      501       20     9695 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_inspect.py
+-rw-r--r--   0      501       20     3225 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_log_render.py
+-rw-r--r--   0      501       20     1236 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_loop.py
+-rw-r--r--   0      501       20     1643 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_null_file.py
+-rw-r--r--   0      501       20     7063 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_palettes.py
+-rw-r--r--   0      501       20      423 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_pick.py
+-rw-r--r--   0      501       20     5472 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_ratio.py
+-rw-r--r--   0      501       20    19919 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_spinners.py
+-rw-r--r--   0      501       20      351 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_stack.py
+-rw-r--r--   0      501       20      417 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_timer.py
+-rw-r--r--   0      501       20    22820 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_win32_console.py
+-rw-r--r--   0      501       20     1926 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_windows.py
+-rw-r--r--   0      501       20     2783 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_windows_renderer.py
+-rw-r--r--   0      501       20     1840 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_wrap.py
+-rw-r--r--   0      501       20      890 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/abc.py
+-rw-r--r--   0      501       20    10368 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/align.py
+-rw-r--r--   0      501       20     6819 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/ansi.py
+-rw-r--r--   0      501       20     3264 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/bar.py
+-rw-r--r--   0      501       20     9842 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/box.py
+-rw-r--r--   0      501       20     4503 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/cells.py
+-rw-r--r--   0      501       20    18015 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/color.py
+-rw-r--r--   0      501       20     1054 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/color_triplet.py
+-rw-r--r--   0      501       20     7131 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/columns.py
+-rw-r--r--   0      501       20    97992 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/console.py
+-rw-r--r--   0      501       20     1288 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/constrain.py
+-rw-r--r--   0      501       20     5497 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/containers.py
+-rw-r--r--   0      501       20     6630 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/control.py
+-rw-r--r--   0      501       20     7954 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/default_styles.py
+-rw-r--r--   0      501       20      972 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/diagnose.py
+-rw-r--r--   0      501       20     2501 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/emoji.py
+-rw-r--r--   0      501       20      642 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/errors.py
+-rw-r--r--   0      501       20     1616 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/file_proxy.py
+-rw-r--r--   0      501       20     2508 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/filesize.py
+-rw-r--r--   0      501       20     9585 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/highlighter.py
+-rw-r--r--   0      501       20     5053 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/json.py
+-rw-r--r--   0      501       20     3252 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/jupyter.py
+-rw-r--r--   0      501       20    14007 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/layout.py
+-rw-r--r--   0      501       20    14172 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/live.py
+-rw-r--r--   0      501       20     3667 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/live_render.py
+-rw-r--r--   0      501       20    11903 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/logging.py
+-rw-r--r--   0      501       20     8198 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/markup.py
+-rw-r--r--   0      501       20     5305 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/measure.py
+-rw-r--r--   0      501       20     4970 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/padding.py
+-rw-r--r--   0      501       20      828 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/pager.py
+-rw-r--r--   0      501       20     3396 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/palette.py
+-rw-r--r--   0      501       20    10574 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/panel.py
+-rw-r--r--   0      501       20    37414 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/pretty.py
+-rw-r--r--   0      501       20    59836 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/progress.py
+-rw-r--r--   0      501       20     8165 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/progress_bar.py
+-rw-r--r--   0      501       20    11303 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/prompt.py
+-rw-r--r--   0      501       20     1391 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/protocol.py
+-rw-r--r--   0      501       20      166 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/region.py
+-rw-r--r--   0      501       20     4436 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/repr.py
+-rw-r--r--   0      501       20     4773 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/rule.py
+-rw-r--r--   0      501       20     2843 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/scope.py
+-rw-r--r--   0      501       20     1591 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/screen.py
+-rw-r--r--   0      501       20    24224 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/segment.py
+-rw-r--r--   0      501       20     4374 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/spinner.py
+-rw-r--r--   0      501       20     4425 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/status.py
+-rw-r--r--   0      501       20    26332 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/style.py
+-rw-r--r--   0      501       20     1258 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/styled.py
+-rw-r--r--   0      501       20    34995 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/syntax.py
+-rw-r--r--   0      501       20    39684 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/table.py
+-rw-r--r--   0      501       20     3370 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/terminal_theme.py
+-rw-r--r--   0      501       20    45686 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/text.py
+-rw-r--r--   0      501       20     3627 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/theme.py
+-rw-r--r--   0      501       20      102 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/themes.py
+-rw-r--r--   0      501       20    26070 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/traceback.py
+-rw-r--r--   0      501       20     9169 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/tree.py
+-rw-r--r--   0      501       20    34549 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/six.py
+-rw-r--r--   0      501       20    18364 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/__init__.py
+-rw-r--r--   0      501       20     3314 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/_asyncio.py
+-rw-r--r--   0      501       20     1944 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/_utils.py
+-rw-r--r--   0      501       20     1496 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/after.py
+-rw-r--r--   0      501       20     1376 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/before.py
+-rw-r--r--   0      501       20     1908 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/before_sleep.py
+-rw-r--r--   0      501       20     1383 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/nap.py
+-rw-r--r--   0      501       20     7550 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/retry.py
+-rw-r--r--   0      501       20     2790 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/stop.py
+-rw-r--r--   0      501       20     2145 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/tornadoweb.py
+-rw-r--r--   0      501       20     8011 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/wait.py
+-rw-r--r--   0      501       20      396 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/__init__.py
+-rw-r--r--   0      501       20    22633 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_parser.py
+-rw-r--r--   0      501       20     2943 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_re.py
+-rw-r--r--   0      501       20      254 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_types.py
+-rw-r--r--   0      501       20    80114 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/typing_extensions.py
+-rw-r--r--   0      501       20     3333 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/__init__.py
+-rw-r--r--   0      501       20    10811 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/_collections.py
+-rw-r--r--   0      501       20       64 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/_version.py
+-rw-r--r--   0      501       20    20070 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/connection.py
+-rw-r--r--   0      501       20    39095 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/connectionpool.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/__init__.py
+-rw-r--r--   0      501       20      957 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_appengine_environ.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/__init__.py
+-rw-r--r--   0      501       20    17632 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/bindings.py
+-rw-r--r--   0      501       20    13922 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/low_level.py
+-rw-r--r--   0      501       20    11036 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/appengine.py
+-rw-r--r--   0      501       20     4528 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/ntlmpool.py
+-rw-r--r--   0      501       20    17081 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py
+-rw-r--r--   0      501       20    34448 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/securetransport.py
+-rw-r--r--   0      501       20     7097 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/socks.py
+-rw-r--r--   0      501       20     8217 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/exceptions.py
+-rw-r--r--   0      501       20     8579 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/fields.py
+-rw-r--r--   0      501       20     2440 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/filepost.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/__init__.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/backports/__init__.py
+-rw-r--r--   0      501       20     1417 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/backports/makefile.py
+-rw-r--r--   0      501       20    34665 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/six.py
+-rw-r--r--   0      501       20    19786 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/poolmanager.py
+-rw-r--r--   0      501       20     5985 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/request.py
+-rw-r--r--   0      501       20    30641 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/response.py
+-rw-r--r--   0      501       20     1155 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/__init__.py
+-rw-r--r--   0      501       20     4901 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/connection.py
+-rw-r--r--   0      501       20     1605 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/proxy.py
+-rw-r--r--   0      501       20      498 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/queue.py
+-rw-r--r--   0      501       20     3997 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/request.py
+-rw-r--r--   0      501       20     3510 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/response.py
+-rw-r--r--   0      501       20    22003 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/retry.py
+-rw-r--r--   0      501       20    17177 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssl_.py
+-rw-r--r--   0      501       20     5758 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssl_match_hostname.py
+-rw-r--r--   0      501       20     6895 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssltransport.py
+-rw-r--r--   0      501       20    10003 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/timeout.py
+-rw-r--r--   0      501       20    14298 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/url.py
+-rw-r--r--   0      501       20     5403 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/wait.py
+-rw-r--r--   0      501       20      476 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/vendor.txt
+-rw-r--r--   0      501       20    10579 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/__init__.py
+-rw-r--r--   0      501       20     8979 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/labels.py
+-rw-r--r--   0      501       20     1305 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/mklabels.py
+-rw-r--r--   0      501       20     6563 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/tests.py
+-rw-r--r--   0      501       20     4307 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/x_user_defined.py
+-rw-r--r--   0      501       20      286 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/py.typed
+-rw-r--r--   0      501       20        4 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/INSTALLER
+-rw-r--r--   0      501       20     1093 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/LICENSE.txt
+-rw-r--r--   0      501       20     4072 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/METADATA
+-rw-r--r--   0      501       20    76671 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/RECORD
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:51.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/REQUESTED
+-rw-r--r--   0      501       20       92 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/WHEEL
+-rw-r--r--   0      501       20      124 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/entry_points.txt
+-rw-r--r--   0      501       20        4 2023-07-22 23:28:50.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/top_level.txt
+-rw-r--r--   0      501       20   108570 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/__init__.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/__init__.py
+-rw-r--r--   0      501       20    24701 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/appdirs.py
+-rw-r--r--   0      501       20      720 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/__about__.py
+-rw-r--r--   0      501       20      513 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/__init__.py
+-rw-r--r--   0      501       20      860 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/_compat.py
+-rw-r--r--   0      501       20     1416 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/_structures.py
+-rw-r--r--   0      501       20     8248 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/markers.py
+-rw-r--r--   0      501       20     4355 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/requirements.py
+-rw-r--r--   0      501       20    28025 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/specifiers.py
+-rw-r--r--   0      501       20      421 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/utils.py
+-rw-r--r--   0      501       20    11556 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/version.py
+-rw-r--r--   0      501       20   232055 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/pyparsing.py
+-rw-r--r--   0      501       20    30098 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/six.py
+-rw-r--r--   0      501       20     2101 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/extern/__init__.py
+-rw-r--r--   0      501       20      396 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/py2_warn.py
+-rw-r--r--   0      501       20      558 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/py31compat.py
+-rw-r--r--   0      501       20     7341 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/__init__.py
+-rw-r--r--   0      501       20      218 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_deprecation_warning.py
+-rw-r--r--   0      501       20     2388 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_imp.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/__init__.py
+-rw-r--r--   0      501       20    15130 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/ordered_set.py
+-rw-r--r--   0      501       20      744 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/__about__.py
+-rw-r--r--   0      501       20      562 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/__init__.py
+-rw-r--r--   0      501       20      865 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/_compat.py
+-rw-r--r--   0      501       20     1416 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/_structures.py
+-rw-r--r--   0      501       20     8268 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/markers.py
+-rw-r--r--   0      501       20     4742 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/requirements.py
+-rw-r--r--   0      501       20    27778 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/specifiers.py
+-rw-r--r--   0      501       20    12933 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/tags.py
+-rw-r--r--   0      501       20     1520 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/utils.py
+-rw-r--r--   0      501       20    11978 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/version.py
+-rw-r--r--   0      501       20   232055 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/pyparsing.py
+-rw-r--r--   0      501       20    30098 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/six.py
+-rw-r--r--   0      501       20     6626 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/archive_util.py
+-rw-r--r--   0      501       20     9960 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/build_meta.py
+-rw-r--r--   0      501       20    65536 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli-32.exe
+-rw-r--r--   0      501       20    74752 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli-64.exe
+-rw-r--r--   0      501       20    65536 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli.exe
+-rw-r--r--   0      501       20      568 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/__init__.py
+-rw-r--r--   0      501       20     2426 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/alias.py
+-rw-r--r--   0      501       20    18406 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_egg.py
+-rw-r--r--   0      501       20     1508 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_rpm.py
+-rw-r--r--   0      501       20      922 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_wininst.py
+-rw-r--r--   0      501       20     4415 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_clib.py
+-rw-r--r--   0      501       20    13048 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_ext.py
+-rw-r--r--   0      501       20     9737 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_py.py
+-rw-r--r--   0      501       20     8188 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/develop.py
+-rw-r--r--   0      501       20      960 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/dist_info.py
+-rw-r--r--   0      501       20    87657 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/easy_install.py
+-rw-r--r--   0      501       20    25548 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/egg_info.py
+-rw-r--r--   0      501       20     4705 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install.py
+-rw-r--r--   0      501       20     2203 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_egg_info.py
+-rw-r--r--   0      501       20     3875 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_lib.py
+-rw-r--r--   0      501       20     2519 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_scripts.py
+-rw-r--r--   0      501       20      628 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/launcher manifest.xml
+-rw-r--r--   0      501       20     4994 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/py36compat.py
+-rw-r--r--   0      501       20      468 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/register.py
+-rw-r--r--   0      501       20     2164 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/rotate.py
+-rw-r--r--   0      501       20      658 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/saveopts.py
+-rw-r--r--   0      501       20     8092 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/sdist.py
+-rw-r--r--   0      501       20     5085 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/setopt.py
+-rw-r--r--   0      501       20     9623 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/test.py
+-rw-r--r--   0      501       20      462 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/upload.py
+-rw-r--r--   0      501       20     7314 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/upload_docs.py
+-rw-r--r--   0      501       20    21757 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/config.py
+-rw-r--r--   0      501       20      949 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/dep_util.py
+-rw-r--r--   0      501       20     5517 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/depends.py
+-rw-r--r--   0      501       20    39211 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/dist.py
+-rw-r--r--   0      501       20      524 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/errors.py
+-rw-r--r--   0      501       20     1729 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/extension.py
+-rw-r--r--   0      501       20     2128 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/extern/__init__.py
+-rw-r--r--   0      501       20     5084 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/glob.py
+-rw-r--r--   0      501       20    65536 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui-32.exe
+-rw-r--r--   0      501       20    75264 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui-64.exe
+-rw-r--r--   0      501       20    65536 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui.exe
+-rw-r--r--   0      501       20     5336 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/installer.py
+-rw-r--r--   0      501       20      787 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/launch.py
+-rw-r--r--   0      501       20     2384 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/lib2to3_ex.py
+-rw-r--r--   0      501       20     5264 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/monkey.py
+-rw-r--r--   0      501       20    50989 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/msvc.py
+-rw-r--r--   0      501       20     3223 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/namespaces.py
+-rw-r--r--   0      501       20    40737 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/package_index.py
+-rw-r--r--   0      501       20     1504 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py27compat.py
+-rw-r--r--   0      501       20      838 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py31compat.py
+-rw-r--r--   0      501       20     1330 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py33compat.py
+-rw-r--r--   0      501       20      245 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py34compat.py
+-rw-r--r--   0      501       20    14284 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/sandbox.py
+-rw-r--r--   0      501       20      218 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/script (dev).tmpl
+-rw-r--r--   0      501       20      138 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/script.tmpl
+-rw-r--r--   0      501       20     2346 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/site-patch.py
+-rw-r--r--   0      501       20     8543 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/ssl_support.py
+-rw-r--r--   0      501       20      996 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/unicode_utils.py
+-rw-r--r--   0      501       20      144 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/version.py
+-rw-r--r--   0      501       20     8371 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/wheel.py
+-rw-r--r--   0      501       20      714 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/windows_support.py
+-rw-r--r--   0      501       20        4 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/INSTALLER
+-rw-r--r--   0      501       20     1078 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/LICENSE
+-rw-r--r--   0      501       20     4806 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/METADATA
+-rw-r--r--   0      501       20    14645 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/RECORD
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/REQUESTED
+-rw-r--r--   0      501       20       92 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/WHEEL
+-rw-r--r--   0      501       20      239 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/dependency_links.txt
+-rw-r--r--   0      501       20     3143 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/entry_points.txt
+-rw-r--r--   0      501       20       38 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/top_level.txt
+-rw-r--r--   0      501       20        1 2023-07-22 23:28:49.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/zip-safe
+-rw-r--r--   0      501       20      113 2023-07-22 23:28:47.000000 klvm_rs-0.2.8/local_dependencies/klvmr/venv/pyvenv.cfg
+-rw-r--r--   0        0        0      587 1970-01-01 00:00:00.000000 klvm_rs-0.2.8/Cargo.toml
+-rw-r--r--   0      501       20      606 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/README.md
+-rw-r--r--   0      501       20      131 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/pyproject.toml
+-rw-r--r--   0      501       20      100 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/__init__.py
+-rw-r--r--   0      501       20      873 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/at.py
+-rw-r--r--   0      501       20     5444 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/casts.py
+-rw-r--r--   0      501       20      941 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/chik_dialect.py
+-rw-r--r--   0      501       20     5402 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/curry_and_treehash.py
+-rw-r--r--   0      501       20     3732 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/de.py
+-rw-r--r--   0      501       20      133 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/eval_error.py
+-rw-r--r--   0      501       20      609 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/klvm_rs.pyi
+-rw-r--r--   0      501       20      695 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/klvm_storage.py
+-rw-r--r--   0      501       20     4903 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/klvm_tree.py
+-rw-r--r--   0      501       20    10761 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/program.py
+-rw-r--r--   0      501       20     1164 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/replace.py
+-rw-r--r--   0      501       20     5038 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/ser.py
+-rw-r--r--   0      501       20     3559 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/klvm_rs/tree_hash.py
+-rw-r--r--   0      501       20        0 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/tests/__init__.py
+-rw-r--r--   0      501       20     6721 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/tests/test_apis.py
+-rw-r--r--   0      501       20     1530 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/tests/test_curry_and_treehash.py
+-rw-r--r--   0      501       20    16181 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/tests/test_program.py
+-rw-r--r--   0      501       20     5046 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/python/tests/test_serialize.py
+-rw-r--r--   0      501       20      828 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/src/adapt_response.rs
+-rw-r--r--   0      501       20     2672 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/src/api.rs
+-rw-r--r--   0      501       20     1381 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/src/lazy_node.rs
+-rw-r--r--   0      501       20       52 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/src/lib.rs
+-rw-r--r--   0      501       20    37919 2023-07-22 23:28:25.000000 klvm_rs-0.2.8/Cargo.lock
+-rw-r--r--   0        0        0     1026 1970-01-01 00:00:00.000000 klvm_rs-0.2.8/PKG-INFO
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/Cargo.toml` & `klvm_rs-0.2.8/Cargo.toml`

 * *Files 26% similar despite different names*

```diff
@@ -1,27 +1,22 @@
 [package]
-name = "klvmr"
-version = "0.1.24"
+name = "klvm_rs"
+version = "0.2.8"
 authors = ["Richard Kiss <him@richardkiss.com>"]
-edition = "2018"
+edition = "2021"
 license = "Apache-2.0"
 description = "Implementation of `klvm` for Chik Network's cryptocurrency"
 homepage = "https://github.com/Chik-Network/klvm_rs/"
 repository = "https://github.com/Chik-Network/klvm_rs/"
 readme = "README.md"
 
 [lib]
-name = "klvmr"
-crate-type = ["rlib"]
-
-[profile.release]
-lto = true
+name = "klvm_rs"
+crate-type = ["cdylib"]
+path = "src/lib.rs"
 
 [dependencies]
-hex = "=0.4.3"
-lazy_static = "=1.4.0"
-num-bigint = "=0.4.3"
-num-traits = "=0.2.15"
-num-integer = "=0.1.45"
-bls12_381 = "=0.7.0"
-sha2 = "=0.10.2"
-openssl = { version = "=0.10.40", features = ["vendored"], optional = true }
+klvmr = { path = "local_dependencies/klvmr" }
+pyo3 = { version = "=0.18.3", features = ["abi3-py37", "extension-module"] }
+
+[features]
+openssl = ["klvmr/openssl"]
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/benchmark.yml.bak` & `klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/benchmark.yml.bak`

 * *Files 8% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 
 name: Run benchmarks
 
 on:
   push:
     branches:
-      - main
+      #- main
       - dev
     tags:
         - '**'
   pull_request:
     branches:
       - '**'
 
@@ -18,19 +18,19 @@
     runs-on: ${{ matrix.os }}
     strategy:
       fail-fast: false
       matrix:
         os: [macos-latest, ubuntu-latest, windows-latest]
 
     steps:
-    - uses: actions/checkout@v2
+    - uses: actions/checkout@v3
       with:
         fetch-depth: 1
 
-    - uses: actions/setup-python@v2
+    - uses: chik-network/actions/setup-python@main
       name: Install Python 3.9
       with:
         python-version: 3.9
 
     - name: Update pip
       run: |
           python -m pip install --upgrade pip
@@ -82,19 +82,19 @@
         python benchmark/run-benchmark.py
 
   max-cost-checks:
     name: Cost checks
     runs-on: ubuntu-latest
 
     steps:
-    - uses: actions/checkout@v2
+    - uses: actions/checkout@v3
       with:
         fetch-depth: 1
 
-    - uses: actions/setup-python@v2
+    - uses: chik-network/actions/setup-python@main
       name: Install Python 3.9
       with:
         python-version: 3.9
 
     - name: Update pip
       run: |
           python -m pip install --upgrade pip
@@ -123,8 +123,7 @@
 
     - name: Run cost checks
       run: |
         . ./activate
         cd tests
         ./generate-programs.py
         ./run-programs.py
-
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/build-arm64-wheels.yml.bak` & `klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/build-arm64-wheels.yml.bak`

 * *Files 8% similar despite different names*

```diff
@@ -1,47 +1,40 @@
 name: Build ARM64 wheels on ubuntu-latest
 
 on:
   push:
     branches:
-      - main
+      #- main
       - dev
     tags:
         - '**'
   pull_request:
     branches:
       - '**'
 
 jobs:
   build_wheels:
-    name: ARM64 Python Wheels on ubuntu-latest
+    name: ARM64 Python Wheels on ARM64 Ubuntu
     runs-on: ${{ matrix.os }}
     strategy:
       matrix:
         os: [[ARM64, Linux]]
 
     steps:
     - uses: Chik-Network/actions/clean-workspace@main
 
     - name: Checkout repository
-      uses: actions/checkout@v2
+      uses: actions/checkout@v3
       with:
         fetch-depth: 1
 
-    - name: Set up QEMU on x86_64
-      if: startsWith(matrix.os, 'ubuntu-latest')
-      id: qemu
-      uses: docker/setup-qemu-action@v1
-      with:
-        platforms: arm64
-
     - name: Build Python wheels
       run: |
-        podman run --rm=true \
-          -v ${{ github.workspace }}:/ws:rw --workdir=/ws \
+        docker run --rm \
+          -v ${{ github.workspace }}:/ws --workdir=/ws \
           quay.io/pypa/manylinux2014_aarch64 \
           bash -exc '\
             echo $PATH && \
             curl -L https://sh.rustup.rs > rustup-init.sh && \
             sh rustup-init.sh -y && \
             yum -y install openssl-devel && \
             source $HOME/.cargo/env && \
@@ -55,47 +48,47 @@
             if [ ! -f "activate" ]; then ln -s venv/bin/activate; fi && \
             . ./activate && \
             pip install maturin && \
             CC=gcc maturin build -m wheel/Cargo.toml --release --strip --manylinux 2014 --features=openssl \
           '
 
     - name: Upload artifacts
-      uses: actions/upload-artifact@v2
+      uses: actions/upload-artifact@v3
       with:
         name: wheels
-        path: wheel/target/wheels/
+        path: target/wheels/
 
     - name: Install Twine
       run: |
-        if [ ! -f "venv" ]; then rm -rf venv; fi
+        if [ ! -f "venv" ]; then sudo rm -rf venv; fi
         sudo apt-get install python3-venv python3-pip -y
         python3 -m venv venv
         if [ ! -f "activate" ]; then ln -s venv/bin/activate; fi
         . ./activate
         pip install setuptools_rust
         pip install twine
 
     - name: Test for secrets access
       id: check_secrets
       shell: bash
       run: |
         unset HAS_SECRET
         if [ -n "$SECRET" ]; then HAS_SECRET='true' ; fi
-        echo ::set-output name=HAS_SECRET::${HAS_SECRET}
+        echo "HAS_SECRET=${HAS_SECRET}" >>$GITHUB_OUTPUT
       env:
         SECRET: "${{ secrets.test_pypi_password }}"
 
     - name: publish (PyPi)
       if: startsWith(github.event.ref, 'refs/tags') && steps.check_secrets.outputs.HAS_SECRET
       env:
         TWINE_USERNAME: __token__
         TWINE_NON_INTERACTIVE: 1
         TWINE_PASSWORD: ${{ secrets.pypi_password }}
       run: |
         . ./activate
-        twine upload --non-interactive --skip-existing --verbose 'wheel/target/wheels/*'
+        twine upload --non-interactive --skip-existing --verbose 'target/wheels/*'
 
     - name: Clean up AMR64
       if: startsWith(matrix.os, 'ARM64')
       run: |
         rm -rf venv
         rm -rf dist
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/build-m1-wheel.yml.bak` & `klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/build-m1-wheel.yml.bak`

 * *Files 12% similar despite different names*

```diff
@@ -1,38 +1,36 @@
 name: Build M1 Wheels
 
 on:
   push:
     branches:
-      - main
+      #- main
       - dev
     tags:
         - '**'
   pull_request:
     branches:
       - '**'
 
+concurrency:
+  group: ${{ github.ref }}-${{ github.workflow }}-${{ github.event_name }}--${{ (github.ref == 'refs/heads/main' || startsWith(github.ref, 'refs/heads/release/') || startsWith(github.ref, 'refs/heads/long_lived/')) && github.sha || '' }}
+  cancel-in-progress: true
+
 jobs:
   build_wheels:
     name: Build wheel on Mac M1
     runs-on: [m1]
     strategy:
       fail-fast: false
 
     steps:
-    - name: Cancel previous runs on the same branch
-      if: ${{ github.ref != 'refs/heads/main' }}
-      uses: styfle/cancel-workflow-action@0.9.1
-      with:
-        access_token: ${{ github.token }}
-
     - uses: Chik-Network/actions/clean-workspace@main
 
     - name: Checkout code
-      uses: actions/checkout@v2
+      uses: actions/checkout@v3
       with:
         fetch-depth: 0
 
     - name: Set up rust
       run: |
         curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs > rust.sh
         arch -arm64 sh rust.sh -y
@@ -44,16 +42,16 @@
         export PATH=~/.cargo/bin:$PATH
         arch -arm64 pip install maturin
         arch -arm64 maturin build -m wheel/Cargo.toml -i python --release --strip --features=openssl
 
     - name: Install klvm_rs wheel
       run: |
         . ./venv/bin/activate
-        ls ./wheel/target/wheels/
-        arch -arm64 pip install ./wheel/target/wheels/klvm_rs*.whl
+        ls ./target/wheels/
+        arch -arm64 pip install ./target/wheels/klvm_rs*.whl
 
     - name: Install other wheels
       run: |
         . ./venv/bin/activate
         arch -arm64 python -m pip install pytest
         arch -arm64 python -m pip install blspy
 
@@ -77,33 +75,41 @@
     - name: Run tests from klvm
       run: |
         . ./venv/bin/activate
         cd klvm
         arch -arm64 pytest tests
 
     - name: Run tests from klvm_tools
-      continue-on-error: true
       run: |
         . ./venv/bin/activate
         cd klvm_tools
         arch -arm64 pytest tests
 
+    - name: Run tests from wheel
+      run: |
+        . ./venv/bin/activate
+        cd wheel/python
+        pytest --import-mode append tests
+        # we use `append` because otherwise the `klvm_rs` source is added
+        # to `sys.path` and it uses that instead of the wheel (and so
+        # ignoring `klvm_rs.so`, which is pretty important)
+
     - name: Upload wheels
-      uses: actions/upload-artifact@v2
+      uses: actions/upload-artifact@v3
       with:
         name: wheels
-        path: ./wheel/target/wheels
+        path: ./target/wheels
 
     - name: Test for secrets access
       id: check_secrets
       shell: bash
       run: |
         unset HAS_SECRET
         if [ -n "$SECRET" ]; then HAS_SECRET='true' ; fi
-        echo ::set-output name=HAS_SECRET::${HAS_SECRET}
+        echo "HAS_SECRET=${HAS_SECRET}" >>$GITHUB_OUTPUT
       env:
         SECRET: "${{ secrets.test_pypi_password }}"
 
     - name: Install twine
       run: |
         . ./venv/bin/activate
         arch -arm64 pip install twine
@@ -112,8 +118,8 @@
       if: startsWith(github.event.ref, 'refs/tags') && steps.check_secrets.outputs.HAS_SECRET
       env:
         TWINE_USERNAME: __token__
         TWINE_NON_INTERACTIVE: 1
         TWINE_PASSWORD: ${{ secrets.pypi_password }}
       run: |
         . ./venv/bin/activate
-        arch -arm64 twine upload --non-interactive --skip-existing --verbose 'wheel/target/wheels/*'
+        arch -arm64 twine upload --non-interactive --skip-existing --verbose 'target/wheels/*'
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/build-test.yml` & `klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/build-test.yml`

 * *Files 17% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 name: Build Mac, Linux, and Windows wheels
 
 on:
   push:
     branches:
-      - main
+      #- main
       - dev
     tags:
         - '**'
   pull_request:
     branches:
       - '**'
 
@@ -18,19 +18,19 @@
     strategy:
       fail-fast: false
       matrix:
         os: [macos-latest, ubuntu-latest, windows-latest]
         python: [3.7]
 
     steps:
-    - uses: actions/checkout@v2
+    - uses: actions/checkout@v3
       with:
         fetch-depth: 0
 
-    - uses: actions/setup-python@v2
+    - uses: chik-network/actions/setup-python@main
       name: Install Python ${{ matrix.python }}
       with:
         python-version: ${{ matrix.python }}
 
     - name: Update pip
       run: |
           python -m pip install --upgrade pip
@@ -42,30 +42,32 @@
 
     - name: Install dependencies
       run: |
           python -m pip install maturin
 
     - name: Build MacOs with maturin on Python ${{ matrix.python }}
       if: startsWith(matrix.os, 'macos')
+      env:
+        MACOSX_DEPLOYMENT_TARGET: '10.14'
       run: |
         python -m venv venv
         ln -s venv/bin/activate
         . ./activate
         maturin build -m wheel/Cargo.toml --sdist -i python --release --strip --features=openssl
 
     - name: Build Linux in manylinux2014 with maturin on Python ${{ matrix.python }}
       if: startsWith(matrix.os, 'ubuntu')
       run: |
-        podman run --rm=true \
-          -v ${{ github.workspace }}:/ws:rw --workdir=/ws \
+        docker run --rm \
+          -v ${{ github.workspace }}:/ws --workdir=/ws \
           quay.io/pypa/manylinux2014_x86_64 \
           bash -exc '\
             curl -L https://sh.rustup.rs > rustup-init.sh && \
             sh rustup-init.sh -y && \
-            yum -y install openssl-devel && \
+            yum -y --disablerepo=epel install openssl-devel && \
             source $HOME/.cargo/env && \
             rustup target add x86_64-unknown-linux-musl && \
             PY_VERSION=${{ matrix.python }}
             PY_VERSION=${PY_VERSION/.} && \
             echo "Python version with dot removed is $PY_VERSION" && \
             if [ "$PY_VERSION" = "37" ]; \
             then export SCND_VERSION="${PY_VERSION}m"; \
@@ -87,157 +89,190 @@
         python -m venv venv
         . .\venv\Scripts\Activate.ps1
         ln -s venv\Scripts\Activate.ps1 activate
         maturin build -m wheel/Cargo.toml -i python --release --strip
         # this will install into the venv
         # it'd be better to use the wheel, but I can't figure out how to do that
         # TODO: figure this out
-        # this does NOT work: pip install wheel/target/wheels/klvm_rs-*.whl
+        # this does NOT work: pip install target/wheels/klvm_rs-*.whl
         maturin develop --release -m wheel/Cargo.toml
         # the line above also doesn't seem to work
 
     - name: Install klvm_rs wheel
       if: ${{ !startsWith(matrix.os, 'windows') }}
       run: |
         . ./activate
-        ls wheel/target/wheels/
+        ls target/wheels/
         # this mess puts the name of the `.whl` file into `$WHEEL_PATH`
         # remove the dot, use the `glob` lib to grab the file from the directory
-        WHEEL_PATH=$(echo ${{ matrix.python }} | python -c 'DOTLESS=input().replace(".", ""); import glob; print(" ".join(glob.glob("wheel/target/wheels/klvm_rs-*-cp%s-abi3-*.whl" % DOTLESS)))' )
+        WHEEL_PATH=$(echo ${{ matrix.python }} | python -c 'DOTLESS=input().replace(".", ""); import glob; print(" ".join(glob.glob("target/wheels/klvm_rs-*-cp%s-abi3-*.whl" % DOTLESS)))' )
         echo ${WHEEL_PATH}
         pip install ${WHEEL_PATH}
 
     - name: Install other wheels
       run: |
         . ./activate
         python -m pip install pytest
         python -m pip install blspy
 
-    - name: install klvm & klvm_tools
-      run: |
-        . ./activate
-        git clone https://github.com/Chik-Network/klvm.git --branch=main --single-branch
-        python -m pip install ./klvm
-
-        git clone https://github.com/Chik-Network/klvm_tools.git --branch=main --single-branch
-        python -m pip install ./klvm_tools
-
-    - name: Ensure klvm, klvm_rs, klvm_tools are installed
-      run: |
-        . ./activate
-        python -c 'import klvm'
-        python -c 'import klvm; print(klvm.__file__)'
-        python -c 'import klvm_rs; print(klvm_rs.__file__)'
-        python -c 'import klvm_tools; print(klvm_tools.__file__)'
-
-    - name: Run tests from klvm
+    - name: Run tests from wheel
       run: |
         . ./activate
-        cd klvm
-        pytest tests
-
-    - name: Run tests from klvm_tools
-      continue-on-error: true
-      run: |
-        . ./activate
-        cd klvm_tools
-        pytest tests
+        cd wheel/python
+        pytest --import-mode append tests
+        # we use `append` because otherwise the `klvm_rs` source is added
+        # to `sys.path` and it uses that instead of the wheel (and so
+        # ignoring `klvm_rs.so`, which is pretty important)
 
     - name: Upload artifacts
-      uses: actions/upload-artifact@v2
+      uses: actions/upload-artifact@v3
       with:
         name: wheels
-        path: ./wheel/target/wheels/
+        path: ./target/wheels/
 
     - name: Install Twine
       run: pip install twine
 
     - name: Test for secrets access
       id: check_secrets
       shell: bash
       run: |
         unset HAS_SECRET
         if [ -n "$SECRET" ]; then HAS_SECRET='true' ; fi
-        echo ::set-output name=HAS_SECRET::${HAS_SECRET}
+        echo "HAS_SECRET=${HAS_SECRET}" >>$GITHUB_OUTPUT
       env:
-        SECRET: "${{ secrets.pypi_password }}"
+        SECRET: "${{ secrets.test_pypi_password }}"
 
     - name: publish (PyPi)
       if: startsWith(github.event.ref, 'refs/tags') && steps.check_secrets.outputs.HAS_SECRET
       env:
         TWINE_USERNAME: __token__
         TWINE_NON_INTERACTIVE: 1
         TWINE_PASSWORD: ${{ secrets.pypi_password }}
-      run: twine upload --non-interactive --skip-existing --verbose 'wheel/target/wheels/*'
+      run: twine upload --non-interactive --skip-existing --verbose 'target/wheels/*'
 
-  fmt:
+  checks:
     runs-on: ubuntu-20.04
-    name: cargo fmt
+    name: Checks
     steps:
-      - uses: actions/checkout@v2
+      - uses: actions/checkout@v3
         with:
           fetch-depth: 1
       - name: Install rust
         uses: actions-rs/toolchain@v1
         with:
             toolchain: stable
             override: true
             components: rustfmt, clippy
+      - name: Clippy
+        run: cargo clippy --all-targets --workspace -- -D warnings
       - name: fmt
-        run: cargo fmt -- --files-with-diff --check
-
-  clippy:
-    runs-on: ubuntu-20.04
-    steps:
-      - uses: actions/checkout@v1
-      - uses: actions-rs/toolchain@v1
-        with:
-          toolchain: stable
-          components: clippy
-          override: true
-      - uses: actions-rs/clippy-check@v1
-        with:
-          token: ${{ secrets.GITHUB_TOKEN }}
-          args: --all-features
+        run: cargo fmt --all -- --files-with-diff --check
 
   # leaving out Windows fuzzing for now though it seems supported
   # https://llvm.org/docs/LibFuzzer.html#q-does-libfuzzer-support-windows
   fuzz_targets:
-    name: Build fuzz targets
+    name: Run fuzz targets
     runs-on: ${{ matrix.os }}
     strategy:
       fail-fast: false
       matrix:
         os: [macos-latest, ubuntu-latest]
         python: [3.7]
     steps:
-      - uses: actions/checkout@v2
+      - uses: actions/checkout@v3
         with:
           fetch-depth: 1
       - name: Install rust
         uses: actions-rs/toolchain@v1
         with:
             toolchain: nightly
+            override: true
+            components: rustfmt, clippy
+      - name: fmt
+        run: |
+          cd fuzz
+          cargo fmt -- --files-with-diff --check
+      - name: clippy
+        run: |
+          cd fuzz
+          cargo clippy
       - name: cargo-fuzz
         run: cargo +nightly install cargo-fuzz
+      # TODO: it would be nice to save and restore the corpus between runs
+      - name: build corpus
+        run: |
+          cd tools
+          cargo run --bin generate-fuzz-corpus
       - name: build
-        run: cargo +nightly fuzz build
+        run: cargo fuzz list | xargs -I "%" sh -c "cargo +nightly fuzz run % -- -max_total_time=30 || exit 255"
 
   unit_tests:
     name: Unit tests
     runs-on: ${{ matrix.os }}
     strategy:
       fail-fast: false
       matrix:
         os: [macos-latest, ubuntu-latest, windows-latest]
         python: [3.7]
     steps:
-      - uses: actions/checkout@v2
+      - uses: actions/checkout@v3
         with:
           fetch-depth: 1
       - name: Install rust
         uses: actions-rs/toolchain@v1
         with:
             toolchain: stable
             components: rustfmt, clippy
-      - name: cargo test
-        run: cargo test
+
+      - name: build
+        run: cargo build --workspace --exclude klvm_rs-fuzz
+
+      - name: cargo test (default)
+        run: cargo test && cargo test --release
+
+      - name: cargo test (counters)
+        run: cargo test --features=counters && cargo test --features=counters --release
+
+      - name: cargo test (pre-eval)
+        run: cargo test --features=pre-eval && cargo test --features=pre-eval --release
+
+      - name: cargo test (pre-eval and counters)
+        run: cargo test --features=pre-eval,counters && cargo test --features=pre-eval,counters --release
+
+  coverage:
+    runs-on: ubuntu-latest
+    steps:
+      - uses: actions/checkout@v3
+      - uses: actions-rs/toolchain@v1
+        with:
+            toolchain: stable
+      - name: Run for coverage
+        run: |
+          sudo apt-get update
+          sudo apt-get install lcov -y
+          rustup component add llvm-tools-preview
+          export CARGOFLAGS="-j $(nproc)"
+          cargo install grcov
+          export RUSTFLAGS="-Cinstrument-coverage"
+          export LLVM_PROFILE_FILE=$(pwd)/target/klvm_rs-%p-%m.profraw
+          export CARGO_TARGET_DIR=$(pwd)/target
+          export RUST_TEST_THREADS=$(nproc)
+          cargo test --release --workspace
+          python -m venv venv
+          source venv/bin/activate
+          git clone https://github.com/Chik-Network/klvm_tools.git --branch=main --single-branch
+          pip install ./klvm_tools
+          pip install colorama maturin pytest pytest-cov
+          maturin develop --release -m wheel/Cargo.toml --features=openssl
+          (cd tests && python generate-programs.py && python run-programs.py) || true
+          pytest wheel/python/tests --cov=klvm_rs --cov-report lcov:py_cov.info --cov-branch
+          grcov . --binary-path target -s . --branch --ignore-not-existing --ignore='*/.cargo/*' --ignore='target/*' -o pre_rust_cov.info
+          python -c 'with open("pre_rust_cov.info") as f: lines = [l for l in f if not (l.startswith("DA:") and int(l.split(",")[1].strip()) >= 2**63)]; open("rust_cov.info", "w").writelines(lines)'
+          lcov --add-tracefile rust_cov.info -a py_cov.info -o lcov.info
+      - name: Upload to Coveralls
+        uses: coverallsapp/github-action@v2
+        if: always()
+        env:
+          COVERALLS_REPO_TOKEN: ${{ secrets.COVERALLS_REPO_TOKEN }}
+        with:
+          path-to-lcov: './lcov.info'
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/.github/workflows/dependency-review.yml.bak` & `klvm_rs-0.2.8/local_dependencies/klvmr/.github/workflows/dependency-review.yml.bak`

 * *Files 1% similar despite different names*

```diff
@@ -13,8 +13,8 @@
 jobs:
   dependency-review:
     runs-on: ubuntu-latest
     steps:
       - name: 'Checkout Repository'
         uses: actions/checkout@v3
       - name: 'Dependency Review'
-        uses: actions/dependency-review-action@v2
+        uses: actions/dependency-review-action@v3
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/LICENSE` & `klvm_rs-0.2.8/local_dependencies/klvmr/LICENSE`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/README.md` & `klvm_rs-0.2.8/local_dependencies/klvmr/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -19,21 +19,20 @@
 The fuzzing infrastructure for `klvm_rs` uses [cargo-fuzz](https://github.com/rust-fuzz/cargo-fuzz).
 
 Documentation for setting up fuzzing in rust can be found [here](https://rust-fuzz.github.io/book/cargo-fuzz.html).
 
 To generate an initial corpus (for the `run_program` fuzzer), run:
 
 ```
-cd fuzz
-mkdir -p corpus/fuzz_run_program/
-python gen_corpus.py
+cd tools
+cargo run generate-fuzz-corpus
 ```
 
 To get started, run:
 
 ```
 cargo fuzz run fuzz_run_program --jobs=32 -- -rss_limit_mb=4096
 ```
 
 But with whatever number of jobs works best for you.
 
-If you find issues in `klvm_rs` please see the [Bug Bounty program](https://www.chik.net/2021/10/21/bugcrowd-bounty-launch.en.html).
+If you find issues in `klvm_rs` please see the [Bug Bounty program](https://www.chiknetwork.com/2021/10/21/bugcrowd-bounty-launch.en.html).
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/RELEASE.md` & `klvm_rs-0.2.8/local_dependencies/klvmr/RELEASE.md`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/activate` & `klvm_rs-0.2.8/local_dependencies/klvmr/activate`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/block-2000.hex` & `klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/block-2000.hex`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/cmp.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/cmp.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/compressed-2000.envhex` & `klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/compressed-2000.envhex`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/compressed-2000.hex` & `klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/compressed-2000.hex`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/matrix-multiply.klvm` & `klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/matrix-multiply.klvm`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/benchmark/run-benchmark.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/benchmark/run-benchmark.py`

 * *Files 4% similar despite different names*

```diff
@@ -2,17 +2,15 @@
 
 import glob
 import subprocess
 import sys
 import os
 import time
 import random
-from klvm import KEYWORD_FROM_ATOM, KEYWORD_TO_ATOM
-from klvm.operators import OP_REWRITE
-from klvm_rs import run_chik_program
+from klvm_rs import Program
 from colorama import init, Fore, Style
 
 init()
 
 procs = []
 
 def long_string(filename):
@@ -180,20 +178,14 @@
         print(".", end="")
         sys.stdout.flush()
     print("")
 
 test_runs = {}
 test_costs = {}
 
-native_opcode_names_by_opcode = dict(
-    ("op_%s" % OP_REWRITE.get(k, k), op)
-    for op, k in KEYWORD_FROM_ATOM.items()
-    if k not in "qa."
-)
-
 print('benchmarking...')
 for n in range(5):
     if "-v" in sys.argv:
         print('pass %d' % n)
     for fn in glob.glob('benchmark/*.hex'):
         env_fn = fn[:-3] + 'envhex'
 
@@ -205,21 +197,20 @@
                 print(" ".join(command))
             output = subprocess.check_output(command)
             output = output.decode('ascii').split('\n', 5)[:-1]
             cost = 0
         else:
             if "-v" in sys.argv:
                 print(fn)
-            program_data = bytes.fromhex(open(fn, 'r').read())
-            env_data = bytes.fromhex(open(env_fn, 'r').read())
+            program = Program.fromhex(open(fn, 'r').read())
+            env = Program.fromhex(open(env_fn, 'r').read())
 
             time_start = time.perf_counter()
-            cost, result = run_chik_program(
-                program_data,
-                env_data,
+            cost, result = program.run_with_cost(
+                env,
                 max_cost,
                 flags,
             )
             time_end = time.perf_counter()
 
             output = ["run_program: %f" % (time_end - time_start)]
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/src/f_table.rs` & `klvm_rs-0.2.8/local_dependencies/klvmr/src/f_table.rs`

 * *Files 25% similar despite different names*

```diff
@@ -1,37 +1,45 @@
 use std::collections::HashMap;
 
 use crate::allocator::{Allocator, NodePtr};
+use crate::bls_ops::{
+    op_bls_g1_multiply, op_bls_g1_negate, op_bls_g1_subtract, op_bls_g2_add, op_bls_g2_multiply,
+    op_bls_g2_negate, op_bls_g2_subtract, op_bls_map_to_g1, op_bls_map_to_g2,
+    op_bls_pairing_identity, op_bls_verify,
+};
 use crate::core_ops::{op_cons, op_eq, op_first, op_if, op_listp, op_raise, op_rest};
 use crate::cost::Cost;
 use crate::more_ops::{
-    op_add, op_all, op_any, op_ash, op_concat, op_div, op_div_deprecated, op_divmod, op_gr,
-    op_gr_bytes, op_logand, op_logior, op_lognot, op_logxor, op_lsh, op_multiply, op_not,
-    op_point_add, op_pubkey_for_exp, op_sha256, op_softfork, op_strlen, op_substr, op_subtract,
+    op_add, op_all, op_any, op_ash, op_concat, op_div, op_divmod, op_gr, op_gr_bytes, op_logand,
+    op_logior, op_lognot, op_logxor, op_lsh, op_mod, op_modpow, op_multiply, op_not, op_point_add,
+    op_pubkey_for_exp, op_sha256, op_strlen, op_substr, op_subtract,
 };
 use crate::reduction::Response;
+use crate::secp_ops::{op_secp256k1_verify, op_secp256r1_verify};
 
 type OpFn = fn(&mut Allocator, NodePtr, Cost) -> Response;
 
 pub type FLookup = [Option<OpFn>; 256];
 
 pub fn opcode_by_name(name: &str) -> Option<OpFn> {
-    let opcode_lookup: [(OpFn, &str); 31] = [
+    let opcode_lookup: [(OpFn, &str); 44] = [
         (op_if, "op_if"),
         (op_cons, "op_cons"),
         (op_first, "op_first"),
         (op_rest, "op_rest"),
         (op_listp, "op_listp"),
         (op_raise, "op_raise"),
         (op_eq, "op_eq"),
         (op_sha256, "op_sha256"),
         (op_add, "op_add"),
         (op_subtract, "op_subtract"),
         (op_multiply, "op_multiply"),
+        (op_modpow, "op_modpow"),
         (op_divmod, "op_divmod"),
+        (op_mod, "op_mod"),
         (op_substr, "op_substr"),
         (op_strlen, "op_strlen"),
         (op_point_add, "op_point_add"),
         (op_pubkey_for_exp, "op_pubkey_for_exp"),
         (op_concat, "op_concat"),
         (op_gr, "op_gr"),
         (op_gr_bytes, "op_gr_bytes"),
@@ -40,17 +48,28 @@
         (op_logxor, "op_logxor"),
         (op_lognot, "op_lognot"),
         (op_ash, "op_ash"),
         (op_lsh, "op_lsh"),
         (op_not, "op_not"),
         (op_any, "op_any"),
         (op_all, "op_all"),
-        (op_softfork, "op_softfork"),
         (op_div, "op_div"),
-        (op_div_deprecated, "op_div_deprecated"),
+        (op_bls_g1_subtract, "op_g1_subtract"),
+        (op_bls_g1_multiply, "op_g1_multiply"),
+        (op_bls_g1_negate, "op_g1_negate"),
+        (op_bls_g2_add, "op_g2_add"),
+        (op_bls_g2_subtract, "op_g2_subtract"),
+        (op_bls_g2_multiply, "op_g2_multiply"),
+        (op_bls_g2_negate, "op_g2_negate"),
+        (op_bls_map_to_g1, "op_g1_map"),
+        (op_bls_map_to_g2, "op_g2_map"),
+        (op_bls_pairing_identity, "op_bls_pairing_identity"),
+        (op_bls_verify, "op_bls_verify"),
+        (op_secp256k1_verify, "op_secp256k1_verify"),
+        (op_secp256r1_verify, "op_secp256r1_verify"),
     ];
     let name: &[u8] = name.as_ref();
     for (f, op) in opcode_lookup.iter() {
         let pu8: &[u8] = op.as_ref();
         if pu8 == name {
             return Some(*f);
         }
@@ -60,13 +79,13 @@
 
 pub fn f_lookup_for_hashmap(opcode_lookup_by_name: HashMap<String, Vec<u8>>) -> FLookup {
     let mut f_lookup = [None; 256];
     for (name, idx) in opcode_lookup_by_name.iter() {
         if idx.len() == 1 {
             let index = idx[0];
             let op = opcode_by_name(name);
-            assert!(op.is_some(), "can't find native operator {:?}", name);
+            assert!(op.is_some(), "can't find native operator {name}");
             f_lookup[index as usize] = op;
         }
     }
     f_lookup
 }
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/src/more_ops.rs` & `klvm_rs-0.2.8/local_dependencies/klvmr/src/more_ops.rs`

 * *Files 16% similar despite different names*

```diff
@@ -1,32 +1,25 @@
 use bls12_381::{G1Affine, G1Projective, Scalar};
 use num_bigint::{BigUint, Sign};
 use num_integer::Integer;
-use std::convert::TryFrom;
 use std::ops::BitAndAssign;
 use std::ops::BitOrAssign;
 use std::ops::BitXorAssign;
 
-use lazy_static::lazy_static;
-
 use crate::allocator::{Allocator, NodePtr, SExp};
 use crate::cost::{check_cost, Cost};
 use crate::err_utils::err;
-use crate::node::Node;
-use crate::number::{number_from_u8, ptr_from_number, Number};
+use crate::number::Number;
 use crate::op_utils::{
-    arg_count, atom, check_arg_count, i32_atom, int_atom, two_ints, u32_from_u8,
+    atom, atom_len, get_args, get_varargs, i32_atom, int_atom, mod_group_order, new_atom_and_cost,
+    nullp, number_to_scalar, u32_from_u8, MALLOC_COST_PER_BYTE,
 };
 use crate::reduction::{Reduction, Response};
-use crate::serialize::node_to_bytes;
 use crate::sha2::{Digest, Sha256};
 
-// We ascribe some additional cost per byte for operations that allocate new atoms
-const MALLOC_COST_PER_BYTE: Cost = 10;
-
 const ARITH_BASE_COST: Cost = 99;
 const ARITH_COST_PER_ARG: Cost = 320;
 const ARITH_COST_PER_BYTE: Cost = 3;
 
 const LOG_BASE_COST: Cost = 100;
 const LOG_COST_PER_ARG: Cost = 264;
 const LOG_COST_PER_BYTE: Cost = 3;
@@ -83,25 +76,38 @@
 // in the pubkey benchmark
 
 // increased from 419535 to better model Raspberry PI
 const PUBKEY_BASE_COST: Cost = 1325730;
 // increased from 12 to closer model Raspberry PI
 const PUBKEY_COST_PER_BYTE: Cost = 38;
 
+// the new coinid operator
+// we subtract 153 cost as a discount, to incentivice using this operator rather
+// than "naked" sha256
+const COINID_COST: Cost =
+    SHA256_BASE_COST + SHA256_COST_PER_ARG * 3 + SHA256_COST_PER_BYTE * (32 + 32 + 8) - 153;
+
+const MODPOW_BASE_COST: Cost = 17000;
+const MODPOW_COST_PER_BYTE_BASE_VALUE: Cost = 38;
+// the cost for exponent and modular scale by the square of the size of the
+// respective operands
+const MODPOW_COST_PER_BYTE_EXPONENT: Cost = 3;
+const MODPOW_COST_PER_BYTE_MOD: Cost = 21;
+
 fn limbs_for_int(v: &Number) -> usize {
     ((v.bits() + 7) / 8) as usize
 }
 
 #[cfg(test)]
 fn limb_test_helper(bytes: &[u8]) {
-    let bigint = Number::from_signed_bytes_be(&bytes);
+    let bigint = Number::from_signed_bytes_be(bytes);
     println!("{} bits: {}", &bigint, &bigint.bits());
 
     // redundant leading zeros don't count, since they aren't stored internally
-    let expected = if bytes.len() > 0 && bytes[0] == 0 {
+    let expected = if !bytes.is_empty() && bytes[0] == 0 {
         bytes.len() - 1
     } else {
         bytes.len()
     };
     assert_eq!(limbs_for_int(&bigint), expected);
 }
 
@@ -138,28 +144,23 @@
     limb_test_helper(&[0x80, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]);
     limb_test_helper(&[0x80, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]);
     limb_test_helper(&[0x80, 0, 0, 0, 0, 0, 0, 0, 0, 0]);
     limb_test_helper(&[0x80, 0, 0, 0, 0, 0, 0, 0, 0]);
     limb_test_helper(&[0x80, 0, 0, 0, 0, 0, 0, 0]);
 }
 
-fn new_atom_and_cost(a: &mut Allocator, cost: Cost, buf: &[u8]) -> Response {
-    let c = buf.len() as Cost * MALLOC_COST_PER_BYTE;
-    Ok(Reduction(cost + c, a.new_atom(buf)?))
-}
-
 fn malloc_cost(a: &Allocator, cost: Cost, ptr: NodePtr) -> Reduction {
-    let c = a.atom(ptr).len() as Cost * MALLOC_COST_PER_BYTE;
+    let c = a.atom_len(ptr) as Cost * MALLOC_COST_PER_BYTE;
     Reduction(cost + c, ptr)
 }
 
 pub fn op_unknown(
     allocator: &mut Allocator,
     o: NodePtr,
-    args: NodePtr,
+    mut args: NodePtr,
     max_cost: Cost,
 ) -> Response {
     // unknown opcode in lenient mode
     // unknown ops are reserved if they start with 0xffff
     // otherwise, unknown ops are no-ops, but they have costs. The cost is computed
     // like this:
 
@@ -167,15 +168,15 @@
     // | 4 | 3 | 2 | 1 | 0          |
     // +---+---+---+---+------------+
     // | multiplier    |XX | XXXXXX |
     // +---+---+---+---+---+--------+
     //  ^               ^    ^
     //  |               |    + 6 bits ignored when computing cost
     // cost_multiplier  |
-    //                  + 2 bits
+    // (up to 4 bytes)  + 2 bits
     //                    cost_function
 
     // 1 is always added to the multiplier before using it to multiply the cost, this
     // is since cost may not be 0.
 
     // cost_function is 2 bits and defines how cost is computed based on arguments:
     // 0: constant, cost is 1 * (multiplier + 1)
@@ -199,62 +200,65 @@
             return err(o, "invalid operator");
         }
     };
 
     let mut cost = match cost_function {
         0 => 1,
         1 => {
-            let mut cost = ARITH_BASE_COST as u64;
+            let mut cost = ARITH_BASE_COST;
             let mut byte_count: u64 = 0;
-            for arg in Node::new(allocator, args) {
-                cost += ARITH_COST_PER_ARG as u64;
-                let blob = int_atom(&arg, "unknown op")?;
-                byte_count += blob.len() as u64;
+            while let Some((arg, rest)) = allocator.next(args) {
+                args = rest;
+                cost += ARITH_COST_PER_ARG;
+                let len = atom_len(allocator, arg, "unknown op")?;
+                byte_count += len as u64;
                 check_cost(
                     allocator,
                     cost + (byte_count as Cost * ARITH_COST_PER_BYTE),
                     max_cost,
                 )?;
             }
-            cost + (byte_count * ARITH_COST_PER_BYTE as u64)
+            cost + (byte_count * ARITH_COST_PER_BYTE)
         }
         2 => {
-            let mut cost = MUL_BASE_COST as u64;
+            let mut cost = MUL_BASE_COST;
             let mut first_iter: bool = true;
             let mut l0: u64 = 0;
-            for arg in Node::new(allocator, args) {
-                let blob = int_atom(&arg, "unknown op")?;
+            while let Some((arg, rest)) = allocator.next(args) {
+                args = rest;
+                let len = atom_len(allocator, arg, "unknown op")?;
                 if first_iter {
-                    l0 = blob.len() as u64;
+                    l0 = len as u64;
                     first_iter = false;
                     continue;
                 }
-                let l1 = blob.len() as u64;
-                cost += MUL_COST_PER_OP as u64;
-                cost += (l0 + l1) * MUL_LINEAR_COST_PER_BYTE as u64;
-                cost += (l0 * l1) / MUL_SQUARE_COST_PER_BYTE_DIVIDER as u64;
+                let l1 = len as u64;
+                cost += MUL_COST_PER_OP;
+                cost += (l0 + l1) * MUL_LINEAR_COST_PER_BYTE;
+                cost += (l0 * l1) / MUL_SQUARE_COST_PER_BYTE_DIVIDER;
                 l0 += l1;
                 check_cost(allocator, cost, max_cost)?;
             }
             cost
         }
         3 => {
-            let mut cost = CONCAT_BASE_COST as u64;
+            let mut cost = CONCAT_BASE_COST;
             let mut total_size: u64 = 0;
-            for arg in Node::new(allocator, args) {
-                cost += CONCAT_COST_PER_ARG as u64;
-                let blob = atom(&arg, "unknown op")?;
-                total_size += blob.len() as u64;
+            while let Some((arg, rest)) = allocator.next(args) {
+                args = rest;
+                cost += CONCAT_COST_PER_ARG;
+                let len = atom_len(allocator, arg, "unknown op")?;
+                total_size += len as u64;
                 check_cost(
                     allocator,
                     cost + total_size as Cost * CONCAT_COST_PER_BYTE,
                     max_cost,
                 )?;
             }
-            cost + total_size * CONCAT_COST_PER_BYTE as u64
+            cost + total_size * CONCAT_COST_PER_BYTE
         }
         _ => 1,
     };
 
     assert!(cost > 0);
 
     check_cost(allocator, cost, max_cost)?;
@@ -275,31 +279,31 @@
 #[test]
 fn test_unknown_op_reserved() {
     let mut a = Allocator::new();
 
     // any op starting with ffff is reserved and a hard failure
     let buf = vec![0xff, 0xff];
     let null = a.null();
-    assert!(!test_op_unknown(&buf, &mut a, null).is_ok());
+    assert!(test_op_unknown(&buf, &mut a, null).is_err());
 
     let buf = vec![0xff, 0xff, 0xff];
-    assert!(!test_op_unknown(&buf, &mut a, null).is_ok());
+    assert!(test_op_unknown(&buf, &mut a, null).is_err());
 
     let buf = vec![0xff, 0xff, b'0'];
-    assert!(!test_op_unknown(&buf, &mut a, null).is_ok());
+    assert!(test_op_unknown(&buf, &mut a, null).is_err());
 
     let buf = vec![0xff, 0xff, 0];
-    assert!(!test_op_unknown(&buf, &mut a, null).is_ok());
+    assert!(test_op_unknown(&buf, &mut a, null).is_err());
 
     let buf = vec![0xff, 0xff, 0xcc, 0xcc, 0xfe, 0xed, 0xce];
-    assert!(!test_op_unknown(&buf, &mut a, null).is_ok());
+    assert!(test_op_unknown(&buf, &mut a, null).is_err());
 
     // an empty atom is not a valid opcode
     let buf = Vec::<u8>::new();
-    assert!(!test_op_unknown(&buf, &mut a, null).is_ok());
+    assert!(test_op_unknown(&buf, &mut a, null).is_err());
 
     // a single ff is not sufficient to be treated as a reserved opcode
     let buf = vec![0xff];
     assert_eq!(
         test_op_unknown(&buf, &mut a, null),
         Ok(Reduction(142, null))
     );
@@ -328,263 +332,252 @@
     let buf = vec![0x3c, 0x00];
     assert_eq!(test_op_unknown(&buf, &mut a, null), Ok(Reduction(61, null)));
 
     let buf = vec![0x3c, 0x2c];
     assert_eq!(test_op_unknown(&buf, &mut a, null), Ok(Reduction(61, null)));
 }
 
-pub fn op_sha256(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
+pub fn op_sha256(a: &mut Allocator, mut input: NodePtr, max_cost: Cost) -> Response {
     let mut cost = SHA256_BASE_COST;
     let mut byte_count: usize = 0;
     let mut hasher = Sha256::new();
-    for arg in Node::new(a, input) {
+    while let Some((arg, rest)) = a.next(input) {
+        input = rest;
         cost += SHA256_COST_PER_ARG;
         check_cost(
             a,
             cost + byte_count as Cost * SHA256_COST_PER_BYTE,
             max_cost,
         )?;
-        let blob = atom(&arg, "sha256")?;
+        let blob = atom(a, arg, "sha256")?;
         byte_count += blob.len();
         hasher.update(blob);
     }
     cost += byte_count as Cost * SHA256_COST_PER_BYTE;
     new_atom_and_cost(a, cost, &hasher.finalize())
 }
 
-pub fn op_add(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
+pub fn op_add(a: &mut Allocator, mut input: NodePtr, max_cost: Cost) -> Response {
     let mut cost = ARITH_BASE_COST;
     let mut byte_count: usize = 0;
     let mut total: Number = 0.into();
-    for arg in Node::new(a, input) {
+    while let Some((arg, rest)) = a.next(input) {
+        input = rest;
         cost += ARITH_COST_PER_ARG;
         check_cost(
             a,
             cost + (byte_count as Cost * ARITH_COST_PER_BYTE),
             max_cost,
         )?;
-        let blob = int_atom(&arg, "+")?;
-        let v: Number = number_from_u8(blob);
-        byte_count += blob.len();
+        let (v, len) = int_atom(a, arg, "+")?;
+        byte_count += len;
         total += v;
     }
-    let total = ptr_from_number(a, &total)?;
+    let total = a.new_number(total)?;
     cost += byte_count as Cost * ARITH_COST_PER_BYTE;
     Ok(malloc_cost(a, cost, total))
 }
 
-pub fn op_subtract(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
+pub fn op_subtract(a: &mut Allocator, mut input: NodePtr, max_cost: Cost) -> Response {
     let mut cost = ARITH_BASE_COST;
     let mut byte_count: usize = 0;
     let mut total: Number = 0.into();
     let mut is_first = true;
-    for arg in Node::new(a, input) {
+    while let Some((arg, rest)) = a.next(input) {
+        input = rest;
         cost += ARITH_COST_PER_ARG;
         check_cost(a, cost + byte_count as Cost * ARITH_COST_PER_BYTE, max_cost)?;
-        let blob = int_atom(&arg, "-")?;
-        let v: Number = number_from_u8(blob);
-        byte_count += blob.len();
+        let (v, len) = int_atom(a, arg, "-")?;
+        byte_count += len;
         if is_first {
             total += v;
         } else {
             total -= v;
         };
         is_first = false;
     }
-    let total = ptr_from_number(a, &total)?;
+    let total = a.new_number(total)?;
     cost += byte_count as Cost * ARITH_COST_PER_BYTE;
     Ok(malloc_cost(a, cost, total))
 }
 
-pub fn op_multiply(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
+pub fn op_multiply(a: &mut Allocator, mut input: NodePtr, max_cost: Cost) -> Response {
     let mut cost: Cost = MUL_BASE_COST;
     let mut first_iter: bool = true;
     let mut total: Number = 1.into();
     let mut l0: usize = 0;
-    for arg in Node::new(a, input) {
+    while let Some((arg, rest)) = a.next(input) {
+        input = rest;
         check_cost(a, cost, max_cost)?;
-        let blob = int_atom(&arg, "*")?;
         if first_iter {
-            l0 = blob.len();
-            total = number_from_u8(blob);
+            (total, l0) = int_atom(a, arg, "*")?;
             first_iter = false;
             continue;
         }
-        let l1 = blob.len();
 
-        total *= number_from_u8(blob);
+        let (v0, l1) = int_atom(a, arg, "*")?;
+
+        total *= v0;
         cost += MUL_COST_PER_OP;
 
         cost += (l0 + l1) as Cost * MUL_LINEAR_COST_PER_BYTE;
         cost += (l0 * l1) as Cost / MUL_SQUARE_COST_PER_BYTE_DIVIDER;
 
         l0 = limbs_for_int(&total);
     }
-    let total = ptr_from_number(a, &total)?;
+    let total = a.new_number(total)?;
     Ok(malloc_cost(a, cost, total))
 }
 
-pub fn op_div_impl(a: &mut Allocator, input: NodePtr, mempool: bool) -> Response {
-    let args = Node::new(a, input);
-    let (a0, l0, a1, l1) = two_ints(&args, "/")?;
-    let cost = DIV_BASE_COST + ((l0 + l1) as Cost) * DIV_COST_PER_BYTE;
+pub fn op_div(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
+    let [v0, v1] = get_args::<2>(a, input, "/")?;
+    let (a0, a0_len) = int_atom(a, v0, "/")?;
+    let (a1, a1_len) = int_atom(a, v1, "/")?;
+    let cost = DIV_BASE_COST + ((a0_len + a1_len) as Cost) * DIV_COST_PER_BYTE;
     if a1.sign() == Sign::NoSign {
-        args.first()?.err("div with 0")
+        err(input, "div with 0")
     } else {
-        if mempool && (a0.sign() == Sign::Minus || a1.sign() == Sign::Minus) {
-            return args.err("div operator with negative operands is deprecated");
+        if a0.sign() == Sign::Minus || a1.sign() == Sign::Minus {
+            return err(input, "div operator with negative operands is deprecated");
         }
-        let (mut q, r) = a0.div_mod_floor(&a1);
-
-        // this is to preserve a buggy behavior from the initial implementation
-        // of this operator.
-        if q == (-1).into() && r != 0.into() {
-            q += 1;
-        }
-        let q1 = ptr_from_number(a, &q)?;
-        Ok(malloc_cost(a, cost, q1))
+        let q = a0.div_floor(&a1);
+        let q = a.new_number(q)?;
+        Ok(malloc_cost(a, cost, q))
     }
 }
 
-pub fn op_div(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    op_div_impl(a, input, false)
-}
-
-pub fn op_div_deprecated(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    op_div_impl(a, input, true)
+pub fn op_div_fixed(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
+    let [v0, v1] = get_args::<2>(a, input, "/")?;
+    let (a0, a0_len) = int_atom(a, v0, "/")?;
+    let (a1, a1_len) = int_atom(a, v1, "/")?;
+    let cost = DIV_BASE_COST + ((a0_len + a1_len) as Cost) * DIV_COST_PER_BYTE;
+    if a1.sign() == Sign::NoSign {
+        err(input, "div with 0")
+    } else {
+        let q = a0.div_floor(&a1);
+        let q = a.new_number(q)?;
+        Ok(malloc_cost(a, cost, q))
+    }
 }
 
 pub fn op_divmod(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    let (a0, l0, a1, l1) = two_ints(&args, "divmod")?;
-    let cost = DIVMOD_BASE_COST + ((l0 + l1) as Cost) * DIVMOD_COST_PER_BYTE;
+    let [v0, v1] = get_args::<2>(a, input, "divmod")?;
+    let (a0, a0_len) = int_atom(a, v0, "divmod")?;
+    let (a1, a1_len) = int_atom(a, v1, "divmod")?;
+    let cost = DIVMOD_BASE_COST + ((a0_len + a1_len) as Cost) * DIVMOD_COST_PER_BYTE;
     if a1.sign() == Sign::NoSign {
-        args.first()?.err("divmod with 0")
+        err(input, "divmod with 0")
     } else {
         let (q, r) = a0.div_mod_floor(&a1);
-        let q1 = ptr_from_number(a, &q)?;
-        let r1 = ptr_from_number(a, &r)?;
+        let q1 = a.new_number(q)?;
+        let r1 = a.new_number(r)?;
 
-        let c = (a.atom(q1).len() + a.atom(r1).len()) as Cost * MALLOC_COST_PER_BYTE;
+        let c = (a.atom_len(q1) + a.atom_len(r1)) as Cost * MALLOC_COST_PER_BYTE;
         let r: NodePtr = a.new_pair(q1, r1)?;
         Ok(Reduction(cost + c, r))
     }
 }
 
+pub fn op_mod(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
+    let [v0, v1] = get_args::<2>(a, input, "mod")?;
+    let (a0, a0_len) = int_atom(a, v0, "mod")?;
+    let (a1, a1_len) = int_atom(a, v1, "mod")?;
+    let cost = DIV_BASE_COST + ((a0_len + a1_len) as Cost) * DIV_COST_PER_BYTE;
+    if a1.sign() == Sign::NoSign {
+        err(input, "mod with 0")
+    } else {
+        let q = a.new_number(a0.mod_floor(&a1))?;
+        let c = a.atom_len(q) as Cost * MALLOC_COST_PER_BYTE;
+        Ok(Reduction(cost + c, q))
+    }
+}
+
 pub fn op_gr(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    check_arg_count(&args, 2, ">")?;
-    let a0 = args.first()?;
-    let a1 = args.rest()?.first()?;
-    let v0 = int_atom(&a0, ">")?;
-    let v1 = int_atom(&a1, ">")?;
-    let cost = GR_BASE_COST + (v0.len() + v1.len()) as Cost * GR_COST_PER_BYTE;
-    Ok(Reduction(
-        cost,
-        if number_from_u8(v0) > number_from_u8(v1) {
-            a.one()
-        } else {
-            a.null()
-        },
-    ))
+    let [v0, v1] = get_args::<2>(a, input, ">")?;
+    let (v0, v0_len) = int_atom(a, v0, ">")?;
+    let (v1, v1_len) = int_atom(a, v1, ">")?;
+    let cost = GR_BASE_COST + (v0_len + v1_len) as Cost * GR_COST_PER_BYTE;
+    Ok(Reduction(cost, if v0 > v1 { a.one() } else { a.null() }))
 }
 
 pub fn op_gr_bytes(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    check_arg_count(&args, 2, ">s")?;
-    let a0 = args.first()?;
-    let a1 = args.rest()?.first()?;
-    let v0 = atom(&a0, ">s")?;
-    let v1 = atom(&a1, ">s")?;
+    let [n0, n1] = get_args::<2>(a, input, ">s")?;
+    let v0 = atom(a, n0, ">s")?;
+    let v1 = atom(a, n1, ">s")?;
     let cost = GRS_BASE_COST + (v0.len() + v1.len()) as Cost * GRS_COST_PER_BYTE;
     Ok(Reduction(cost, if v0 > v1 { a.one() } else { a.null() }))
 }
 
 pub fn op_strlen(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    check_arg_count(&args, 1, "strlen")?;
-    let a0 = args.first()?;
-    let v0 = atom(&a0, "strlen")?;
-    let size = v0.len();
-    let size_num: Number = size.into();
-    let size_node = ptr_from_number(a, &size_num)?;
+    let [n] = get_args::<1>(a, input, "strlen")?;
+    let size = atom_len(a, n, "strlen")?;
+    let size_node = a.new_number(size.into())?;
     let cost = STRLEN_BASE_COST + size as Cost * STRLEN_COST_PER_BYTE;
     Ok(malloc_cost(a, cost, size_node))
 }
 
 pub fn op_substr(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    let ac = arg_count(&args, 3);
-    if !(2..=3).contains(&ac) {
-        return args.err("substr takes exactly 2 or 3 arguments");
-    }
-    let a0 = args.first()?;
-    let s0 = atom(&a0, "substr")?;
-    let size = s0.len();
-    let rest = args.rest()?;
-    let i1 = i32_atom(&rest.first()?, "substr")?;
-    let rest = rest.rest()?;
+    let ([a0, start, end], argc) = get_varargs::<3>(a, input, "substr")?;
+    if !(2..=3).contains(&argc) {
+        return err(input, "substr takes exactly 2 or 3 arguments");
+    }
+    let size = atom_len(a, a0, "substr")?;
+    let start = i32_atom(a, start, "substr")?;
 
-    let i2 = if ac == 3 {
-        i32_atom(&rest.first()?, "substr")?
+    let end = if argc == 3 {
+        i32_atom(a, end, "substr")?
     } else {
         size as i32
     };
-    if i2 < 0 || i1 < 0 || i2 as usize > size || i2 < i1 {
-        args.err("invalid indices for substr")
+    if end < 0 || start < 0 || end as usize > size || end < start {
+        err(input, "invalid indices for substr")
     } else {
-        let atom_node = a0.node;
-        let r = a.new_substr(atom_node, i1 as u32, i2 as u32)?;
+        let r = a.new_substr(a0, start as u32, end as u32)?;
         let cost: Cost = 1;
         Ok(Reduction(cost, r))
     }
 }
 
-pub fn op_concat(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
+pub fn op_concat(a: &mut Allocator, mut input: NodePtr, max_cost: Cost) -> Response {
     let mut cost = CONCAT_BASE_COST;
     let mut total_size: usize = 0;
     let mut terms = Vec::<NodePtr>::new();
-    for arg in &args {
+    while let Some((arg, rest)) = a.next(input) {
+        input = rest;
         cost += CONCAT_COST_PER_ARG;
         check_cost(
             a,
             cost + total_size as Cost * CONCAT_COST_PER_BYTE,
             max_cost,
         )?;
-        match arg.sexp() {
-            SExp::Pair(_, _) => return arg.err("concat on list"),
-            SExp::Atom(b) => total_size += b.len(),
+        match a.sexp(arg) {
+            SExp::Pair(_, _) => return err(arg, "concat on list"),
+            SExp::Atom() => total_size += a.atom_len(arg),
         };
-        terms.push(arg.node);
+        terms.push(arg);
     }
 
     cost += total_size as Cost * CONCAT_COST_PER_BYTE;
     cost += total_size as Cost * MALLOC_COST_PER_BYTE;
     check_cost(a, cost, max_cost)?;
     let new_atom = a.new_concat(total_size, &terms)?;
     Ok(Reduction(cost, new_atom))
 }
 
 pub fn op_ash(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    check_arg_count(&args, 2, "ash")?;
-    let a0 = args.first()?;
-    let b0 = int_atom(&a0, "ash")?;
-    let i0 = number_from_u8(b0);
-    let l0 = b0.len();
-    let rest = args.rest()?;
-    let a1 = i32_atom(&rest.first()?, "ash")?;
+    let [n0, n1] = get_args::<2>(a, input, "ash")?;
+    let (i0, l0) = int_atom(a, n0, "ash")?;
+    let a1 = i32_atom(a, n1, "ash")?;
     if !(-65535..=65535).contains(&a1) {
-        return args.rest()?.first()?.err("shift too large");
+        return err(n1, "shift too large");
     }
 
     let v: Number = if a1 > 0 { i0 << a1 } else { i0 >> -a1 };
     let l1 = limbs_for_int(&v);
-    let r = ptr_from_number(a, &v)?;
+    let r = a.new_number(v)?;
     let cost = ASHIFT_BASE_COST + ((l0 + l1) as Cost) * ASHIFT_COST_PER_BYTE;
     Ok(malloc_cost(a, cost, r))
 }
 
 #[cfg(test)]
 fn test_shift(
     op: fn(&mut Allocator, NodePtr, Cost) -> Response,
@@ -639,32 +632,28 @@
     // the result is 1 followed by 4064 zeroes
     let node = a.atom(node);
     assert_eq!(node[0], 1);
     assert_eq!(node.len(), 4065);
 }
 
 pub fn op_lsh(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    check_arg_count(&args, 2, "lsh")?;
-    let a0 = args.first()?;
-    let b0 = int_atom(&a0, "lsh")?;
-    let i0 = BigUint::from_bytes_be(b0);
-    let l0 = b0.len();
-    let rest = args.rest()?;
-    let a1 = i32_atom(&rest.first()?, "lsh")?;
+    let [n0, n1] = get_args::<2>(a, input, "lsh")?;
+    let b0 = atom(a, n0, "lsh")?;
+    let a1 = i32_atom(a, n1, "lsh")?;
     if !(-65535..=65535).contains(&a1) {
-        return args.rest()?.first()?.err("shift too large");
+        return err(n1, "shift too large");
     }
-
+    let i0 = BigUint::from_bytes_be(b0);
+    let l0 = b0.len();
     let i0: Number = i0.into();
 
     let v: Number = if a1 > 0 { i0 << a1 } else { i0 >> -a1 };
 
     let l1 = limbs_for_int(&v);
-    let r = ptr_from_number(a, &v)?;
+    let r = a.new_number(v)?;
     let cost = LSHIFT_BASE_COST + ((l0 + l1) as Cost) * LSHIFT_COST_PER_BYTE;
     Ok(malloc_cost(a, cost, r))
 }
 
 #[test]
 fn test_op_lsh() {
     let mut a = Allocator::new();
@@ -707,31 +696,31 @@
     assert_eq!(node.len(), 4065);
 }
 
 fn binop_reduction(
     op_name: &str,
     a: &mut Allocator,
     initial_value: Number,
-    input: NodePtr,
+    mut input: NodePtr,
     max_cost: Cost,
     op_f: fn(&mut Number, &Number) -> (),
 ) -> Response {
     let mut total = initial_value;
     let mut arg_size: usize = 0;
     let mut cost = LOG_BASE_COST;
-    for arg in Node::new(a, input) {
-        let blob = int_atom(&arg, op_name)?;
-        let n0 = number_from_u8(blob);
+    while let Some((arg, rest)) = a.next(input) {
+        input = rest;
+        let (n0, len) = int_atom(a, arg, op_name)?;
         op_f(&mut total, &n0);
-        arg_size += blob.len();
+        arg_size += len;
         cost += LOG_COST_PER_ARG;
         check_cost(a, cost + (arg_size as Cost * LOG_COST_PER_BYTE), max_cost)?;
     }
     cost += arg_size as Cost * LOG_COST_PER_BYTE;
-    let total = ptr_from_number(a, &total)?;
+    let total = a.new_number(total)?;
     Ok(malloc_cost(a, cost, total))
 }
 
 fn logand_op(a: &mut Number, b: &Number) {
     a.bitand_assign(b);
 }
 
@@ -755,147 +744,145 @@
 
 pub fn op_logxor(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
     let v: Number = (0).into();
     binop_reduction("logxor", a, v, input, max_cost, logxor_op)
 }
 
 pub fn op_lognot(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    check_arg_count(&args, 1, "lognot")?;
-    let a0 = args.first()?;
-    let v0 = int_atom(&a0, "lognot")?;
-    let mut n: Number = number_from_u8(v0);
+    let [n] = get_args::<1>(a, input, "lognot")?;
+    let (mut n, len) = int_atom(a, n, "lognot")?;
     n = !n;
-    let cost = LOGNOT_BASE_COST + ((v0.len() as Cost) * LOGNOT_COST_PER_BYTE);
-    let r = ptr_from_number(a, &n)?;
+    let cost = LOGNOT_BASE_COST + ((len as Cost) * LOGNOT_COST_PER_BYTE);
+    let r = a.new_number(n)?;
     Ok(malloc_cost(a, cost, r))
 }
 
 pub fn op_not(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    check_arg_count(&args, 1, "not")?;
-    let r: NodePtr = args.from_bool(!args.first()?.as_bool()).node;
+    let [n] = get_args::<1>(a, input, "not")?;
+    let r = if nullp(a, n) { a.one() } else { a.null() };
     let cost = BOOL_BASE_COST;
     Ok(Reduction(cost, r))
 }
 
-pub fn op_any(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
+pub fn op_any(a: &mut Allocator, mut input: NodePtr, max_cost: Cost) -> Response {
     let mut cost = BOOL_BASE_COST;
     let mut is_any = false;
-    for arg in &args {
+    while let Some((arg, rest)) = a.next(input) {
+        input = rest;
         cost += BOOL_COST_PER_ARG;
         check_cost(a, cost, max_cost)?;
-        is_any = is_any || arg.as_bool();
+        is_any = is_any || !nullp(a, arg);
     }
-    let total: Node = args.from_bool(is_any);
-    Ok(Reduction(cost, total.node))
+    Ok(Reduction(cost, if is_any { a.one() } else { a.null() }))
 }
 
-pub fn op_all(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
+pub fn op_all(a: &mut Allocator, mut input: NodePtr, max_cost: Cost) -> Response {
     let mut cost = BOOL_BASE_COST;
     let mut is_all = true;
-    for arg in &args {
+    while let Some((arg, rest)) = a.next(input) {
+        input = rest;
         cost += BOOL_COST_PER_ARG;
         check_cost(a, cost, max_cost)?;
-        is_all = is_all && arg.as_bool();
-    }
-    let total: Node = args.from_bool(is_all);
-    Ok(Reduction(cost, total.node))
-}
-
-pub fn op_softfork(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    match args.pair() {
-        Some((p1, _)) => {
-            let n: Number = number_from_u8(int_atom(&p1, "softfork")?);
-            if n.sign() == Sign::Plus {
-                if n > Number::from(max_cost) {
-                    return err(a.null(), "cost exceeded");
-                }
-                let cost: Cost = TryFrom::try_from(&n).unwrap();
-                Ok(Reduction(cost, args.null().node))
-            } else {
-                args.err("cost must be > 0")
-            }
-        }
-        _ => args.err("softfork takes at least 1 argument"),
-    }
-}
-
-lazy_static! {
-    static ref GROUP_ORDER: Number = {
-        let order_as_bytes = &[
-            0x73, 0xed, 0xa7, 0x53, 0x29, 0x9d, 0x7d, 0x48, 0x33, 0x39, 0xd8, 0x08, 0x09, 0xa1,
-            0xd8, 0x05, 0x53, 0xbd, 0xa4, 0x02, 0xff, 0xfe, 0x5b, 0xfe, 0xff, 0xff, 0xff, 0xff,
-            0x00, 0x00, 0x00, 0x01,
-        ];
-        let n = BigUint::from_bytes_be(order_as_bytes);
-        n.into()
-    };
-}
-
-fn mod_group_order(n: Number) -> Number {
-    let order = GROUP_ORDER.clone();
-    let mut remainder = n.mod_floor(&order);
-    if remainder.sign() == Sign::Minus {
-        remainder += order;
-    }
-    remainder
-}
-
-fn number_to_scalar(n: Number) -> Scalar {
-    let (sign, as_u8): (Sign, Vec<u8>) = n.to_bytes_le();
-    let mut scalar_array: [u8; 32] = [0; 32];
-    scalar_array[..as_u8.len()].clone_from_slice(&as_u8[..]);
-    let exp: Scalar = Scalar::from_bytes(&scalar_array).unwrap();
-    if sign == Sign::Minus {
-        exp.neg()
-    } else {
-        exp
+        is_all = is_all && !nullp(a, arg);
     }
+    Ok(Reduction(cost, if is_all { a.one() } else { a.null() }))
 }
 
 pub fn op_pubkey_for_exp(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
-    check_arg_count(&args, 1, "pubkey_for_exp")?;
-    let a0 = args.first()?;
-
-    let v0 = int_atom(&a0, "pubkey_for_exp")?;
-    let exp: Number = mod_group_order(number_from_u8(v0));
-    let cost = PUBKEY_BASE_COST + (v0.len() as Cost) * PUBKEY_COST_PER_BYTE;
+    let [n] = get_args::<1>(a, input, "pubkey_for_exp")?;
+    let (v0, v0_len) = int_atom(a, n, "pubkey_for_exp")?;
+    let exp: Number = mod_group_order(v0);
+    let cost = PUBKEY_BASE_COST + (v0_len as Cost) * PUBKEY_COST_PER_BYTE;
     let exp: Scalar = number_to_scalar(exp);
     let point: G1Projective = G1Affine::generator() * exp;
-    let point: G1Affine = point.into();
-
-    new_atom_and_cost(a, cost, &point.to_compressed())
+    Ok(Reduction(
+        cost + 48 * MALLOC_COST_PER_BYTE,
+        a.new_g1(point)?,
+    ))
 }
 
-pub fn op_point_add(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
-    let args = Node::new(a, input);
+pub fn op_point_add(a: &mut Allocator, mut input: NodePtr, max_cost: Cost) -> Response {
     let mut cost = POINT_ADD_BASE_COST;
     let mut total: G1Projective = G1Projective::identity();
-    for arg in &args {
-        let blob = atom(&arg, "point_add")?;
-        let mut is_ok: bool = blob.len() == 48;
-        if is_ok {
-            let mut as_array: [u8; 48] = [0; 48];
-            as_array.clone_from_slice(&blob[0..48]);
-            let v = G1Affine::from_compressed(&as_array);
-            is_ok = v.is_some().into();
-            if is_ok {
-                let point = v.unwrap();
-                cost += POINT_ADD_COST_PER_ARG;
-                check_cost(a, cost, max_cost)?;
-                total += &point;
-            }
+    while let Some((arg, rest)) = a.next(input) {
+        input = rest;
+        let point = a.g1(arg)?;
+        cost += POINT_ADD_COST_PER_ARG;
+        check_cost(a, cost, max_cost)?;
+        total += &point;
+    }
+    Ok(Reduction(
+        cost + 48 * MALLOC_COST_PER_BYTE,
+        a.new_g1(total)?,
+    ))
+}
+
+pub fn op_coinid(a: &mut Allocator, input: NodePtr, _max_cost: Cost) -> Response {
+    let [parent_coin, puzzle_hash, amount] = get_args::<3>(a, input, "coinid")?;
+
+    let parent_coin = atom(a, parent_coin, "coinid")?;
+    if parent_coin.len() != 32 {
+        return err(input, "coinid: invalid parent coin id (must be 32 bytes)");
+    }
+    let puzzle_hash = atom(a, puzzle_hash, "coinid")?;
+    if puzzle_hash.len() != 32 {
+        return err(input, "coinid: invalid puzzle hash (must be 32 bytes)");
+    }
+    let amount = atom(a, amount, "coinid")?;
+    if !amount.is_empty() {
+        if (amount[0] & 0x80) != 0 {
+            return err(input, "coinid: invalid amount (may not be negative");
         }
-        if !is_ok {
-            let blob: String = hex::encode(node_to_bytes(&arg).unwrap());
-            let msg = format!("point_add expects blob, got {}: Length of bytes object not equal to G1Element::SIZE", blob);
-            return args.err(&msg);
+        if amount == [0_u8] || (amount.len() > 1 && amount[0] == 0 && (amount[1] & 0x80) == 0) {
+            return err(
+                input,
+                "coinid: invalid amount (may not have redundant leading zero)",
+            );
         }
+        // the only valid coin value that's 9 bytes is when a leading zero is
+        // required to not have the value interpreted as negative
+        if amount.len() > 9 || (amount.len() == 9 && amount[0] != 0) {
+            return err(
+                input,
+                "coinid: invalid amount (may not exceed max coin amount)",
+            );
+        }
+    }
+
+    let mut hasher = Sha256::new();
+    hasher.update(parent_coin);
+    hasher.update(puzzle_hash);
+    hasher.update(amount);
+    let ret: [u8; 32] = hasher
+        .finalize()
+        .as_slice()
+        .try_into()
+        .expect("sha256 hash is not 32 bytes");
+
+    new_atom_and_cost(a, COINID_COST, &ret)
+}
+
+pub fn op_modpow(a: &mut Allocator, input: NodePtr, max_cost: Cost) -> Response {
+    let [base, exponent, modulus] = get_args::<3>(a, input, "modpow")?;
+
+    let mut cost = MODPOW_BASE_COST;
+    let (base, bsize) = int_atom(a, base, "modpow")?;
+    cost += bsize as Cost * MODPOW_COST_PER_BYTE_BASE_VALUE;
+    let (exponent, esize) = int_atom(a, exponent, "modpow")?;
+    cost += (esize * esize) as Cost * MODPOW_COST_PER_BYTE_EXPONENT;
+    check_cost(a, cost, max_cost)?;
+    let (modulus, msize) = int_atom(a, modulus, "modpow")?;
+    cost += (msize * msize) as Cost * MODPOW_COST_PER_BYTE_MOD;
+    check_cost(a, cost, max_cost)?;
+
+    if exponent.sign() == Sign::Minus {
+        return err(input, "modpow with negative exponent");
+    }
+
+    if modulus.sign() == Sign::NoSign {
+        return err(input, "modpow with 0 modulus");
     }
-    let total: G1Affine = total.into();
-    new_atom_and_cost(a, cost, &total.to_compressed())
+
+    let ret = base.modpow(&exponent, &modulus);
+    let ret = a.new_number(ret)?;
+    Ok(malloc_cost(a, cost, ret))
 }
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/src/number.rs` & `klvm_rs-0.2.8/local_dependencies/klvmr/src/number.rs`

 * *Files 13% similar despite different names*

```diff
@@ -1,114 +1,112 @@
 use crate::allocator::{Allocator, NodePtr};
-use crate::node::Node;
 use crate::reduction::EvalErr;
 
 use num_bigint::BigInt;
 pub type Number = BigInt;
 
-pub fn ptr_from_number(allocator: &mut Allocator, item: &Number) -> Result<NodePtr, EvalErr> {
+// This low-level conversion function is meant to be used by the Allocator, for
+// logic interacting with the KLVM heap/allocator, use new_number() and number()
+// instead.
+pub fn node_from_number(allocator: &mut Allocator, item: &Number) -> Result<NodePtr, EvalErr> {
     let bytes: Vec<u8> = item.to_signed_bytes_be();
     let mut slice = bytes.as_slice();
 
     // make number minimal by removing leading zeros
     while (!slice.is_empty()) && (slice[0] == 0) {
         if slice.len() > 1 && (slice[1] & 0x80 == 0x80) {
             break;
         }
         slice = &slice[1..];
     }
     allocator.new_atom(slice)
 }
 
-impl From<&Node<'_>> for Option<Number> {
-    fn from(item: &Node) -> Self {
-        let v: &[u8] = item.atom()?;
-        Some(number_from_u8(v))
-    }
-}
-
+// This low-level conversion function is meant to be used by the Allocator, for
+// logic interacting with the KLVM heap/allocator, use new_number() and number()
+// instead.
 pub fn number_from_u8(v: &[u8]) -> Number {
     let len = v.len();
     if len == 0 {
         0.into()
     } else {
         Number::from_signed_bytes_be(v)
     }
 }
 
 #[test]
-fn test_ptr_from_number() {
+fn test_node_from_number() {
     let mut a = Allocator::new();
 
     // 0 is encoded as an empty string
     let num = number_from_u8(&[0]);
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(format!("{}", num), "0");
     assert_eq!(a.atom(ptr).len(), 0);
 
     let num = number_from_u8(&[1]);
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(format!("{}", num), "1");
     assert_eq!(&[1], &a.atom(ptr));
 
     // leading zeroes are redundant
     let num = number_from_u8(&[0, 0, 0, 1]);
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(format!("{}", num), "1");
     assert_eq!(&[1], &a.atom(ptr));
 
     let num = number_from_u8(&[0x00, 0x00, 0x80]);
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(format!("{}", num), "128");
     assert_eq!(&[0x00, 0x80], &a.atom(ptr));
 
     // A leading zero is necessary to encode a positive number with the
     // penultimate byte's most significant bit set
     let num = number_from_u8(&[0x00, 0xff]);
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(format!("{}", num), "255");
     assert_eq!(&[0x00, 0xff], &a.atom(ptr));
 
     let num = number_from_u8(&[0x7f, 0xff]);
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(format!("{}", num), "32767");
     assert_eq!(&[0x7f, 0xff], &a.atom(ptr));
 
     // the first byte is redundant, it's still -1
     let num = number_from_u8(&[0xff, 0xff]);
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(format!("{}", num), "-1");
     assert_eq!(&[0xff], &a.atom(ptr));
 
     let num = number_from_u8(&[0xff]);
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(format!("{}", num), "-1");
     assert_eq!(&[0xff], &a.atom(ptr));
 
     let num = number_from_u8(&[0x00, 0x80, 0x00]);
     assert_eq!(format!("{}", num), "32768");
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(&[0x00, 0x80, 0x00], &a.atom(ptr));
 
     let num = number_from_u8(&[0x00, 0x40, 0x00]);
     assert_eq!(format!("{}", num), "16384");
-    let ptr = ptr_from_number(&mut a, &num).unwrap();
+    let ptr = node_from_number(&mut a, &num).unwrap();
     assert_eq!(&[0x40, 0x00], &a.atom(ptr));
 }
 
 #[cfg(test)]
 use num_bigint::{BigUint, Sign};
 
 #[cfg(test)]
 use std::convert::TryFrom;
 
 #[cfg(test)]
 fn roundtrip_bytes(b: &[u8]) {
-    let negative = b.len() > 0 && (b[0] & 0x80) != 0;
-    let zero = b.len() == 0 || (b.len() == 1 && b[0] == 0);
+    let negative = !b.is_empty() && (b[0] & 0x80) != 0;
+    let zero = b.is_empty() || (b.len() == 1 && b[0] == 0);
 
     {
         let num = Number::from_signed_bytes_be(b);
 
         if negative {
             assert!(num.sign() == Sign::Minus);
         } else if zero {
@@ -116,41 +114,41 @@
         } else {
             assert!(num.sign() == Sign::Plus);
         }
 
         let round_trip = num.to_signed_bytes_be();
         // num-bigin produces a single 0 byte for the value 0. We expect an
         // empty array
-        let round_trip = if round_trip == &[0] {
+        let round_trip = if round_trip == [0] {
             &round_trip[1..]
         } else {
             &round_trip
         };
 
         assert_eq!(round_trip, b);
 
         // test to_bytes_le()
         let (sign, mut buf_le) = num.to_bytes_le();
 
         // there's a special case for empty input buffers, which will result in
         // a single 0 byte here
-        if b == &[] {
+        if b.is_empty() {
             assert_eq!(buf_le, &[0]);
             buf_le.remove(0);
         }
         assert!(sign == num.sign());
 
         // the buffer we get from to_bytes_le() is unsigned (since the sign is
         // returned separately). This means it doesn't ever need to prepend a 0
         // byte when the MSB is set. When we're comparing this against the input
         // buffer, we need to add such 0 byte to buf_le to make them compare
         // equal.
         // the 0 prefix has to be added to the end though, since it's little
         // endian
-        if buf_le.len() > 0 && (buf_le.last().unwrap() & 0x80) != 0 {
+        if !buf_le.is_empty() && (buf_le.last().unwrap() & 0x80) != 0 {
             buf_le.push(0);
         }
 
         if sign != Sign::Minus {
             assert!(buf_le.iter().eq(b.iter().rev()));
         } else {
             let negated = -num;
@@ -160,20 +158,20 @@
     }
 
     // test parsing unsigned bytes
     {
         let unsigned_num: Number = BigUint::from_bytes_be(b).into();
         assert!(unsigned_num.sign() != Sign::Minus);
         let unsigned_round_trip = unsigned_num.to_signed_bytes_be();
-        let unsigned_round_trip = if unsigned_round_trip == &[0] {
+        let unsigned_round_trip = if unsigned_round_trip == [0] {
             &unsigned_round_trip[1..]
         } else {
             &unsigned_round_trip
         };
-        if b.len() > 0 && (b[0] & 0x80) != 0 {
+        if !b.is_empty() && (b[0] & 0x80) != 0 {
             // we expect a new leading zero here, to keep the value positive
             assert!(unsigned_round_trip[0] == 0);
             assert_eq!(&unsigned_round_trip[1..], b);
         } else {
             assert_eq!(unsigned_round_trip, b);
         }
     }
@@ -255,21 +253,22 @@
     for v in 0xfffffffffffffffe..=0xffffffffffffffff {
         roundtrip_u64(v);
     }
 }
 
 #[cfg(test)]
 fn roundtrip_i64(v: i64) {
+    use std::cmp::Ordering;
+
     let num: Number = v.into();
-    if v == 0 {
-        assert!(num.sign() == Sign::NoSign);
-    } else if v < 0 {
-        assert!(num.sign() == Sign::Minus);
-    } else if v > 0 {
-        assert!(num.sign() == Sign::Plus);
+
+    match v.cmp(&0) {
+        Ordering::Equal => assert!(num.sign() == Sign::NoSign),
+        Ordering::Less => assert!(num.sign() == Sign::Minus),
+        Ordering::Greater => assert!(num.sign() == Sign::Plus),
     }
 
     assert!(num.bits() <= 64);
 
     let round_trip: i64 = TryFrom::try_from(num).unwrap();
     assert_eq!(round_trip, v);
 }
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/src/runtime_dialect.rs` & `klvm_rs-0.2.8/local_dependencies/klvmr/src/runtime_dialect.rs`

 * *Files 17% similar despite different names*

```diff
@@ -1,47 +1,50 @@
 use crate::allocator::{Allocator, NodePtr};
 use crate::chik_dialect::NO_UNKNOWN_OPS;
 use crate::cost::Cost;
-use crate::dialect::Dialect;
+use crate::dialect::{Dialect, OperatorSet};
 use crate::err_utils::err;
 use crate::f_table::{f_lookup_for_hashmap, FLookup};
 use crate::more_ops::op_unknown;
 use crate::reduction::Response;
 use std::collections::HashMap;
 
 pub struct RuntimeDialect {
     f_lookup: FLookup,
     quote_kw: Vec<u8>,
     apply_kw: Vec<u8>,
+    softfork_kw: Vec<u8>,
     flags: u32,
 }
 
 impl RuntimeDialect {
     pub fn new(
         op_map: HashMap<String, Vec<u8>>,
         quote_kw: Vec<u8>,
         apply_kw: Vec<u8>,
         flags: u32,
     ) -> RuntimeDialect {
         RuntimeDialect {
             f_lookup: f_lookup_for_hashmap(op_map),
             quote_kw,
             apply_kw,
+            softfork_kw: vec![36], // softfork opcode
             flags,
         }
     }
 }
 
 impl Dialect for RuntimeDialect {
     fn op(
         &self,
         allocator: &mut Allocator,
         o: NodePtr,
         argument_list: NodePtr,
         max_cost: Cost,
+        _extensions: OperatorSet,
     ) -> Response {
         let b = &allocator.atom(o);
         if b.len() == 1 {
             if let Some(f) = self.f_lookup[b[0] as usize] {
                 return f(allocator, argument_list, max_cost);
             }
         }
@@ -56,11 +59,19 @@
         &self.quote_kw
     }
 
     fn apply_kw(&self) -> &[u8] {
         &self.apply_kw
     }
 
-    fn val_stack_limit(&self) -> usize {
-        usize::MAX
+    fn softfork_kw(&self) -> &[u8] {
+        &self.softfork_kw
+    }
+
+    fn softfork_extension(&self, _ext: u32) -> OperatorSet {
+        OperatorSet::Default
+    }
+
+    fn allow_unknown_ops(&self) -> bool {
+        (self.flags & NO_UNKNOWN_OPS) == 0
     }
 }
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/src/sha2.rs` & `klvm_rs-0.2.8/local_dependencies/klvmr/src/sha2.rs`

 * *Files 21% similar despite different names*

```diff
@@ -32,26 +32,26 @@
     let output = &[
         0xba, 0x78, 0x16, 0xbf, 0x8f, 0x01, 0xcf, 0xea, 0x41, 0x41, 0x40, 0xde, 0x5d, 0xae, 0x22,
         0x23, 0xb0, 0x03, 0x61, 0xa3, 0x96, 0x17, 0x7a, 0x9c, 0xb4, 0x10, 0xff, 0x61, 0xf2, 0x00,
         0x15, 0xad,
     ];
 
     let mut ctx = Sha256::new();
-    ctx.update(&[0x61, 0x62, 0x63]);
+    ctx.update([0x61, 0x62, 0x63]);
     assert_eq!(&ctx.finalize().as_slice(), output);
 
     let mut ctx = Sha256::new();
-    ctx.update(&[0x61]);
-    ctx.update(&[0x62]);
-    ctx.update(&[0x63]);
+    ctx.update([0x61]);
+    ctx.update([0x62]);
+    ctx.update([0x63]);
     assert_eq!(&ctx.finalize().as_slice(), output);
 
     let mut ctx = Sha256::new();
-    ctx.update(&[0x61, 0x62]);
-    ctx.update(&[0x63]);
+    ctx.update([0x61, 0x62]);
+    ctx.update([0x63]);
     assert_eq!(&ctx.finalize().as_slice(), output);
 
     let mut ctx = Sha256::new();
-    ctx.update(&[0x61]);
-    ctx.update(&[0x62, 0x63]);
+    ctx.update([0x61]);
+    ctx.update([0x62, 0x63]);
     assert_eq!(&ctx.finalize().as_slice(), output);
 }
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/tests/generate-programs.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/tests/generate-programs.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/tests/run-programs.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/tests/run-programs.py`

 * *Files 6% similar despite different names*

```diff
@@ -78,18 +78,18 @@
                 continue
             size = int(l.split('maxresident)k')[0].split(' ')[-1]) / 1024
     if size != None:
         print(Fore.YELLOW + ('  Resident Size: %d MiB' % size) + Style.RESET_ALL)
 
         if size > 2300:
             ret += 1
-            print(Fore.RED + '\nTEST FAILURE: Max memory use exceeded\n' + Style.RESET_ALL)
+            print(Fore.RED + '\nTEST FAILURE: Max memory use exceeded (limit: 2300 MB)\n' + Style.RESET_ALL)
 
     # cost 10923314721 roughly corresponds to 11 seconds
     if end - start > 11:
         ret += 1
-        print(Fore.RED + '\nTEST FAILURE: Time exceeded: %f\n' % (end - start) + Style.RESET_ALL)
+        print(Fore.RED + '\nTEST FAILURE: Time exceeded: %f (limit: 11)\n' % (end - start) + Style.RESET_ALL)
 
 if ret:
     print(Fore.RED + f'\n   There were {ret} failures!\n' + Style.RESET_ALL)
 
 sys.exit(ret)
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/tests/run.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/tests/run.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,31 +1,32 @@
 #!/usr/bin/env python3
 
-from klvm_rs import run_chik_program
+from klvm_rs import Program
+
 
 def run_klvm(fn, env=None):
 
-    program_data = bytes.fromhex(open(fn, 'r').read())
+    program = Program.fromhex(open(fn, 'r').read())
     if env is not None:
-        env_data = bytes.fromhex(open(env, 'r').read())
+        env = Program.fromhex(open(env, 'r').read())
     else:
-        env_data = bytes.fromhex("ff80")
+        env = Program.fromhex("ff80")
     # constants from the main chik blockchain:
     # https://github.com/Chik-Network/chik-blockchain/blob/main/chik/consensus/default_constants.py
     max_cost = 11000000000
     cost_per_byte = 12000
 
-    max_cost -= (len(program_data) + len(env_data)) * cost_per_byte
-    return run_chik_program(
-        program_data,
-        env_data,
+    max_cost -= (len(bytes(program)) + len(bytes(env))) * cost_per_byte
+    return program.run_with_cost(
+        env,
         max_cost,
         0,
     )
 
+
 def count_tree_size(tree) -> int:
     stack = [tree]
     ret = 0
     while len(stack):
         i = stack.pop()
         if i.atom is not None:
             ret += len(i.atom)
@@ -44,15 +45,15 @@
     try:
         start = time()
         cost, result = run_klvm(sys.argv[1], sys.argv[2])
         duration = time() - start;
         print(f"cost: {cost}")
         print(f"execution time: {duration:.2f}s")
     except Exception as e:
-        print("FAIL:", e)
+        print("FAIL:", e.args[0])
         sys.exit(1)
     start = time()
     ret_size = count_tree_size(result)
     duration = time() - start;
     print(f"returned bytes: {ret_size}")
     print(f"parse return value time: {duration:.2f}s")
     sys.exit(0)
```

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/activate` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/activate`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/activate.csh` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/activate.csh`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/activate.fish` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/activate.fish`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/python` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/python`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/bin/python3` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/bin/python3`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__main__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__main__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__pip-runner__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/__pip-runner__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/build_env.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/build_env.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cache.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cache.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/autocompletion.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/autocompletion.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/base_command.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/base_command.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/cmdoptions.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/cmdoptions.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/command_context.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/command_context.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/main.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/main.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/main_parser.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/main_parser.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/parser.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/parser.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/progress_bars.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/progress_bars.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/req_command.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/req_command.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/spinners.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/cli/spinners.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/cache.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/cache.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/check.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/check.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/completion.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/completion.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/configuration.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/configuration.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/debug.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/debug.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/download.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/download.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/freeze.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/freeze.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/hash.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/hash.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/help.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/help.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/index.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/index.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/inspect.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/inspect.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/install.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/install.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/list.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/list.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/search.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/search.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/show.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/show.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/uninstall.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/uninstall.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/wheel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/commands/wheel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/configuration.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/configuration.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/base.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/base.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/installed.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/installed.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/sdist.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/sdist.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/wheel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/distributions/wheel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/exceptions.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/exceptions.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/collector.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/collector.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/package_finder.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/package_finder.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/sources.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/index/sources.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/_distutils.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/_distutils.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/_sysconfig.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/_sysconfig.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/base.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/locations/base.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/_json.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/_json.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/base.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/base.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_dists.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_dists.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_envs.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/importlib/_envs.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/pkg_resources.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/metadata/pkg_resources.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/candidate.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/candidate.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/direct_url.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/direct_url.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/format_control.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/format_control.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/index.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/index.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/installation_report.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/installation_report.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/link.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/link.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/scheme.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/scheme.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/search_scope.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/search_scope.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/selection_prefs.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/selection_prefs.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/target_python.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/target_python.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/wheel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/models/wheel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/auth.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/auth.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/cache.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/cache.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/download.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/download.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/lazy_wheel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/lazy_wheel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/session.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/session.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/utils.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/utils.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/xmlrpc.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/network/xmlrpc.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/build_tracker.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/build_tracker.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata_editable.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata_editable.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata_legacy.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/metadata_legacy.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel_editable.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel_editable.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel_legacy.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/build/wheel_legacy.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/check.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/check.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/freeze.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/freeze.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/editable_legacy.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/editable_legacy.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/legacy.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/legacy.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/wheel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/install/wheel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/prepare.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/operations/prepare.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/pyproject.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/pyproject.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/constructors.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/constructors.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_file.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_file.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_install.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_install.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_set.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_set.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_uninstall.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/req/req_uninstall.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/base.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/base.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/legacy/resolver.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/legacy/resolver.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/base.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/base.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/candidates.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/candidates.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/factory.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/factory.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/found_candidates.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/found_candidates.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/provider.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/provider.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/reporter.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/reporter.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/requirements.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/requirements.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/resolver.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/resolution/resolvelib/resolver.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/self_outdated_check.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/self_outdated_check.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/_log.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/_log.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/appdirs.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/appdirs.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/compatibility_tags.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/compatibility_tags.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/deprecation.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/deprecation.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/direct_url_helpers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/direct_url_helpers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/distutils_args.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/distutils_args.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/egg_link.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/egg_link.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/encoding.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/encoding.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/entrypoints.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/entrypoints.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/filesystem.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/filesystem.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/filetypes.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/filetypes.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/glibc.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/glibc.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/hashes.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/hashes.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/inject_securetransport.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/inject_securetransport.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/logging.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/logging.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/misc.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/misc.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/models.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/models.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/packaging.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/packaging.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/setuptools_build.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/setuptools_build.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/subprocess.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/subprocess.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/temp_dir.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/temp_dir.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/unpacking.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/unpacking.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/urls.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/urls.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/virtualenv.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/virtualenv.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/wheel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/utils/wheel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/bazaar.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/bazaar.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/git.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/git.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/mercurial.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/mercurial.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/subversion.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/subversion.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/versioncontrol.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/vcs/versioncontrol.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/wheel_builder.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_internal/wheel_builder.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/_cmd.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/_cmd.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/adapter.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/adapter.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/cache.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/cache.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/file_cache.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/file_cache.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/redis_cache.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/caches/redis_cache.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/controller.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/controller.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/filewrapper.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/filewrapper.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/heuristics.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/heuristics.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/serialize.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/serialize.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/wrapper.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/cachecontrol/wrapper.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/cacert.pem` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/cacert.pem`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/core.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/certifi/core.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/big5freq.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/big5freq.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/big5prober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/big5prober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/chardistribution.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/chardistribution.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/charsetgroupprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/charsetgroupprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/charsetprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/charsetprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cli/chardetect.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cli/chardetect.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/codingstatemachine.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/codingstatemachine.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/codingstatemachinedict.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/codingstatemachinedict.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cp949prober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/cp949prober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/enums.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/enums.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/escprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/escprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/escsm.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/escsm.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/eucjpprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/eucjpprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euckrfreq.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euckrfreq.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euckrprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euckrprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euctwfreq.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euctwfreq.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euctwprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/euctwprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/gb2312freq.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/gb2312freq.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/gb2312prober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/gb2312prober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/hebrewprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/hebrewprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/jisfreq.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/jisfreq.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/johabfreq.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/johabfreq.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/johabprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/johabprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/jpcntx.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/jpcntx.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langbulgarianmodel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langbulgarianmodel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langgreekmodel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langgreekmodel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langhebrewmodel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langhebrewmodel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langhungarianmodel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langhungarianmodel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langrussianmodel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langrussianmodel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langthaimodel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langthaimodel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langturkishmodel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/langturkishmodel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/latin1prober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/latin1prober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/macromanprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/macromanprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcharsetprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcharsetprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcsgroupprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcsgroupprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcssm.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/mbcssm.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/metadata/languages.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/metadata/languages.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sbcharsetprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sbcharsetprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sbcsgroupprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sbcsgroupprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sjisprober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/sjisprober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/universaldetector.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/universaldetector.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/utf1632prober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/utf1632prober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/utf8prober.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/chardet/utf8prober.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/ansi.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/ansi.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/ansitowin32.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/ansitowin32.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/initialise.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/initialise.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/ansi_test.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/ansi_test.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/ansitowin32_test.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/ansitowin32_test.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/initialise_test.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/initialise_test.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/isatty_test.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/isatty_test.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/utils.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/utils.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/winterm_test.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/tests/winterm_test.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/win32.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/win32.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/winterm.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/colorama/winterm.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/database.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/database.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/index.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/index.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/locators.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/locators.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/manifest.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/manifest.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/markers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/markers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/metadata.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/metadata.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/resources.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/resources.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/scripts.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/scripts.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t32.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t32.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t64-arm.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t64-arm.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t64.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/t64.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/util.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/util.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/version.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/version.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w32.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w32.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w64-arm.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w64-arm.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w64.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/w64.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/wheel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distlib/wheel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/distro.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/distro/distro.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/codec.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/codec.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/core.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/core.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/idnadata.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/idnadata.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/intranges.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/intranges.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/uts46data.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/idna/uts46data.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/exceptions.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/exceptions.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/ext.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/ext.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/fallback.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/msgpack/fallback.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/__about__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/__about__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_manylinux.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_manylinux.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_musllinux.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_musllinux.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_structures.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/_structures.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/markers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/markers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/requirements.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/requirements.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/specifiers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/specifiers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/tags.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/tags.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/utils.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/utils.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/version.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/packaging/version.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pkg_resources/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pkg_resources/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pkg_resources/py31compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pkg_resources/py31compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/__main__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/__main__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/android.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/android.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/api.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/api.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/macos.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/macos.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/unix.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/unix.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/windows.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/platformdirs/windows.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/cmdline.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/cmdline.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/console.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/console.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/filter.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/filter.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/filters/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/filters/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatter.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatter.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/_mapping.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/_mapping.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/bbcode.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/bbcode.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/groff.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/groff.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/html.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/html.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/img.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/img.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/irc.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/irc.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/latex.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/latex.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/other.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/other.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/pangomarkup.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/pangomarkup.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/rtf.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/rtf.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/svg.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/svg.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/terminal.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/terminal.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/terminal256.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/formatters/terminal256.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexer.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexer.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/_mapping.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/_mapping.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/python.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/lexers/python.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/modeline.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/modeline.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/plugin.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/plugin.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/regexopt.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/regexopt.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/scanner.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/scanner.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/sphinxext.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/sphinxext.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/style.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/style.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/styles/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/styles/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/token.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/token.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/unistring.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/unistring.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/util.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pygments/util.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/actions.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/actions.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/common.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/common.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/core.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/core.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/diagram/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/diagram/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/exceptions.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/exceptions.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/helpers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/helpers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/results.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/results.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/testing.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/testing.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/unicode.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/unicode.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/util.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyparsing/util.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_impl.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_impl.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_in_process/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_in_process/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/_internal_utils.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/_internal_utils.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/adapters.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/adapters.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/api.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/api.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/auth.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/auth.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/certs.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/certs.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/cookies.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/cookies.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/exceptions.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/exceptions.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/help.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/help.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/hooks.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/hooks.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/models.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/models.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/packages.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/packages.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/sessions.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/sessions.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/status_codes.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/status_codes.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/structures.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/structures.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/utils.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/requests/utils.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/providers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/providers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/reporters.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/reporters.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/resolvers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/resolvers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/structs.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/resolvelib/structs.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/__main__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/__main__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_cell_widths.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_cell_widths.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_emoji_codes.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_emoji_codes.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_emoji_replace.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_emoji_replace.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_export_format.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_export_format.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_inspect.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_inspect.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_log_render.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_log_render.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_loop.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_loop.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_null_file.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_null_file.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_palettes.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_palettes.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_ratio.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_ratio.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_spinners.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_spinners.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_win32_console.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_win32_console.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_windows.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_windows.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_windows_renderer.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_windows_renderer.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_wrap.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/_wrap.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/abc.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/abc.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/align.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/align.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/ansi.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/ansi.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/bar.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/bar.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/box.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/box.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/cells.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/cells.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/color.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/color.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/color_triplet.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/color_triplet.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/columns.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/columns.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/console.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/console.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/constrain.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/constrain.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/containers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/containers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/control.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/control.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/default_styles.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/default_styles.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/diagnose.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/diagnose.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/emoji.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/emoji.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/errors.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/errors.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/file_proxy.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/file_proxy.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/filesize.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/filesize.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/highlighter.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/highlighter.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/json.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/json.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/jupyter.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/jupyter.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/layout.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/layout.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/live.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/live.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/live_render.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/live_render.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/logging.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/logging.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/markup.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/markup.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/measure.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/measure.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/padding.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/padding.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/pager.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/pager.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/palette.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/palette.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/panel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/panel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/pretty.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/pretty.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/progress.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/progress.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/progress_bar.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/progress_bar.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/prompt.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/prompt.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/protocol.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/protocol.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/repr.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/repr.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/rule.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/rule.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/scope.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/scope.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/screen.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/screen.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/segment.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/segment.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/spinner.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/spinner.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/status.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/status.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/style.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/style.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/styled.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/styled.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/syntax.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/syntax.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/table.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/table.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/terminal_theme.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/terminal_theme.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/text.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/text.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/theme.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/theme.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/traceback.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/traceback.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/tree.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/rich/tree.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/six.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/six.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/_asyncio.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/_asyncio.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/_utils.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/_utils.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/after.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/after.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/before.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/before.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/before_sleep.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/before_sleep.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/nap.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/nap.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/retry.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/retry.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/stop.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/stop.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/tornadoweb.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/tornadoweb.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/wait.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tenacity/wait.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_parser.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_parser.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_re.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/tomli/_re.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/typing_extensions.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/typing_extensions.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/_collections.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/_collections.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/connection.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/connection.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/connectionpool.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/connectionpool.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_appengine_environ.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_appengine_environ.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/bindings.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/bindings.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/low_level.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/_securetransport/low_level.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/appengine.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/appengine.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/ntlmpool.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/ntlmpool.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/pyopenssl.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/securetransport.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/securetransport.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/socks.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/contrib/socks.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/exceptions.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/exceptions.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/fields.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/fields.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/filepost.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/filepost.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/backports/makefile.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/backports/makefile.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/six.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/packages/six.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/poolmanager.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/poolmanager.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/request.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/request.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/response.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/response.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/connection.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/connection.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/proxy.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/proxy.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/request.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/request.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/response.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/response.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/retry.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/retry.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssl_.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssl_.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssl_match_hostname.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssl_match_hostname.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssltransport.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/ssltransport.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/timeout.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/timeout.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/url.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/url.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/wait.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/urllib3/util/wait.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/labels.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/labels.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/mklabels.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/mklabels.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/tests.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/tests.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/x_user_defined.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip/_vendor/webencodings/x_user_defined.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/LICENSE.txt` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/METADATA` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/METADATA`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/RECORD` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pip-23.0.1.dist-info/RECORD`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/appdirs.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/appdirs.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/__about__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/__about__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/_compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/_compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/_structures.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/_structures.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/markers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/markers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/requirements.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/requirements.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/specifiers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/specifiers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/version.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/packaging/version.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/pyparsing.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/pyparsing.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/six.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/_vendor/six.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/extern/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/extern/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/py31compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/pkg_resources/py31compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_imp.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_imp.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/ordered_set.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/ordered_set.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/__about__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/__about__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/_compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/_compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/_structures.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/_structures.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/markers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/markers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/requirements.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/requirements.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/specifiers.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/specifiers.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/tags.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/tags.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/utils.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/utils.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/version.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/packaging/version.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/pyparsing.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/pyparsing.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/six.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/_vendor/six.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/archive_util.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/archive_util.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/build_meta.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/build_meta.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli-32.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli-32.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli-64.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli-64.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/cli.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/alias.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/alias.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_egg.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_egg.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_rpm.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_rpm.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_wininst.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/bdist_wininst.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_clib.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_clib.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_ext.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_ext.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_py.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/build_py.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/develop.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/develop.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/dist_info.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/dist_info.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/easy_install.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/easy_install.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/egg_info.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/egg_info.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_egg_info.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_egg_info.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_lib.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_lib.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_scripts.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/install_scripts.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/launcher manifest.xml` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/launcher manifest.xml`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/py36compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/py36compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/rotate.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/rotate.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/saveopts.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/saveopts.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/sdist.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/sdist.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/setopt.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/setopt.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/test.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/test.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/upload_docs.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/command/upload_docs.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/config.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/config.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/dep_util.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/dep_util.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/depends.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/depends.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/dist.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/dist.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/errors.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/errors.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/extension.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/extension.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/extern/__init__.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/extern/__init__.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/glob.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/glob.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui-32.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui-32.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui-64.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui-64.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui.exe` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/gui.exe`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/installer.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/installer.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/launch.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/launch.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/lib2to3_ex.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/lib2to3_ex.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/monkey.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/monkey.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/msvc.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/msvc.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/namespaces.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/namespaces.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/package_index.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/package_index.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py27compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py27compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py31compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py31compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py33compat.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/py33compat.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/sandbox.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/sandbox.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/site-patch.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/site-patch.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/ssl_support.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/ssl_support.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/unicode_utils.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/unicode_utils.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/wheel.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/wheel.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/windows_support.py` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools/windows_support.py`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/LICENSE` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/LICENSE`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/METADATA` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/METADATA`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/RECORD` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/RECORD`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/entry_points.txt` & `klvm_rs-0.2.8/local_dependencies/klvmr/venv/lib/python3.7/site-packages/setuptools-47.1.0.dist-info/entry_points.txt`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/README.md` & `klvm_rs-0.2.8/README.md`

 * *Files identical despite different names*

### Comparing `klvm_rs-0.1.24/src/lazy_node.rs` & `klvm_rs-0.2.8/src/lazy_node.rs`

 * *Files 6% similar despite different names*

```diff
@@ -33,15 +33,15 @@
             _ => Ok(None),
         }
     }
 
     #[getter(atom)]
     pub fn atom(&self, py: Python) -> Option<PyObject> {
         match &self.allocator.sexp(self.node) {
-            SExp::Atom(atom) => Some(PyBytes::new(py, self.allocator.buf(atom)).into()),
+            SExp::Atom() => Some(PyBytes::new(py, self.allocator.atom(self.node)).into()),
             _ => None,
         }
     }
 }
 
 impl LazyNode {
     pub const fn new(a: Rc<Allocator>, n: NodePtr) -> Self {
```

### Comparing `klvm_rs-0.1.24/PKG-INFO` & `klvm_rs-0.2.8/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: klvm_rs
-Version: 0.1.24
+Version: 0.2.8
 Summary: Implementation of `klvm` for Chik Network's cryptocurrency
 Home-Page: https://github.com/Chik-Network/klvm_rs/
 Author: Richard Kiss <him@richardkiss.com>
 Author-email: Richard Kiss <him@richardkiss.com>
 License: Apache-2.0
 Description-Content-Type: text/markdown; charset=UTF-8; variant=GFM
 Project-URL: Source Code, https://github.com/Chik-Network/klvm_rs/
```

