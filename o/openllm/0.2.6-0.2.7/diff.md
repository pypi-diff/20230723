# Comparing `tmp/openllm-0.2.6.tar.gz` & `tmp/openllm-0.2.7.tar.gz`

## Comparing `openllm-0.2.6.tar` & `openllm-0.2.7.tar`

### file list

```diff
@@ -1,137 +1,137 @@
--rw-r--r--   0        0        0      215 2020-02-02 00:00:00.000000 openllm-0.2.6/.gitattributes
--rw-r--r--   0        0        0     3550 2020-02-02 00:00:00.000000 openllm-0.2.6/.pre-commit-config.yaml
--rw-r--r--   0        0        0     2938 2020-02-02 00:00:00.000000 openllm-0.2.6/ADDING_NEW_MODEL.md
--rw-r--r--   0        0        0    13197 2020-02-02 00:00:00.000000 openllm-0.2.6/CHANGELOG.md
--rw-r--r--   0        0        0     2059 2020-02-02 00:00:00.000000 openllm-0.2.6/CITATION.cff
--rw-r--r--   0        0        0     6704 2020-02-02 00:00:00.000000 openllm-0.2.6/DEVELOPMENT.md
--rw-r--r--   0        0        0      283 2020-02-02 00:00:00.000000 openllm-0.2.6/nightly-requirements-gpu.txt
--rw-r--r--   0        0        0      566 2020-02-02 00:00:00.000000 openllm-0.2.6/nightly-requirements.txt
--rw-r--r--   0        0        0      519 2020-02-02 00:00:00.000000 openllm-0.2.6/package.json
--rw-r--r--   0        0        0     3483 2020-02-02 00:00:00.000000 openllm-0.2.6/pyoxidizer.bzl
--rw-r--r--   0        0        0      119 2020-02-02 00:00:00.000000 openllm-0.2.6/taplo.toml
--rw-r--r--   0        0        0      620 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/__about__.py
--rw-r--r--   0        0        0    12740 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/__init__.py
--rw-r--r--   0        0        0      804 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/__main__.py
--rw-r--r--   0        0        0    90013 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/_configuration.py
--rw-r--r--   0        0        0     1923 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/_generation.py
--rw-r--r--   0        0        0    70703 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/_llm.py
--rw-r--r--   0        0        0     1637 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/_prompt.py
--rw-r--r--   0        0        0     5974 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/_quantisation.py
--rw-r--r--   0        0        0     3217 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/_schema.py
--rw-r--r--   0        0        0     7301 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/_service.py
--rw-r--r--   0        0        0    18488 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/_strategies.py
--rw-r--r--   0        0        0     5361 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/_types.py
--rw-r--r--   0        0        0   101935 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/cli.py
--rw-r--r--   0        0        0     1908 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/client.py
--rw-r--r--   0        0        0     1524 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/exceptions.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/py.typed
--rw-r--r--   0        0        0     3406 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/testing.py
--rw-r--r--   0        0        0     2103 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/bundle/__init__.py
--rw-r--r--   0        0        0    14998 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/bundle/_package.py
--rw-r--r--   0        0        0     1902 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/bundle/oci/Dockerfile-builder
--rw-r--r--   0        0        0      170 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/bundle/oci/Dockerfile-vllm
--rw-r--r--   0        0        0      762 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/bundle/oci/__init__.py
--rw-r--r--   0        0        0      979 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/__init__.py
--rw-r--r--   0        0        0     4228 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/auto/__init__.py
--rw-r--r--   0        0        0     5810 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/auto/configuration_auto.py
--rw-r--r--   0        0        0    11869 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/auto/factory.py
--rw-r--r--   0        0        0     1337 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/auto/modeling_auto.py
--rw-r--r--   0        0        0     1085 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/auto/modeling_flax_auto.py
--rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/auto/modeling_tf_auto.py
--rw-r--r--   0        0        0     1051 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/auto/modeling_vllm_auto.py
--rw-r--r--   0        0        0     1865 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/baichuan/__init__.py
--rw-r--r--   0        0        0     2812 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/baichuan/configuration_baichuan.py
--rw-r--r--   0        0        0     3342 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/baichuan/modeling_baichuan.py
--rw-r--r--   0        0        0     1850 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/chatglm/__init__.py
--rw-r--r--   0        0        0     3230 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/chatglm/configuration_chatglm.py
--rw-r--r--   0        0        0     3969 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/chatglm/modeling_chatglm.py
--rw-r--r--   0        0        0     1745 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/dolly_v2/__init__.py
--rw-r--r--   0        0        0     4397 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/dolly_v2/configuration_dolly_v2.py
--rw-r--r--   0        0        0    12726 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/dolly_v2/modeling_dolly_v2.py
--rw-r--r--   0        0        0     1721 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/falcon/__init__.py
--rw-r--r--   0        0        0     2824 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/falcon/configuration_falcon.py
--rw-r--r--   0        0        0     4913 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/falcon/modeling_falcon.py
--rw-r--r--   0        0        0     2589 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/flan_t5/__init__.py
--rw-r--r--   0        0        0     2597 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/flan_t5/configuration_flan_t5.py
--rw-r--r--   0        0        0     3361 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/flan_t5/modeling_flan_t5.py
--rw-r--r--   0        0        0     3765 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/flan_t5/modeling_flax_flan_t5.py
--rw-r--r--   0        0        0     3182 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/flan_t5/modeling_tf_flan_t5.py
--rw-r--r--   0        0        0     1745 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/gpt_neox/__init__.py
--rw-r--r--   0        0        0     2819 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/gpt_neox/configuration_gpt_neox.py
--rw-r--r--   0        0        0     3903 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/gpt_neox/modeling_gpt_neox.py
--rw-r--r--   0        0        0     2264 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/llama/__init__.py
--rw-r--r--   0        0        0     5366 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/llama/configuration_llama.py
--rw-r--r--   0        0        0     4917 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/llama/modeling_llama.py
--rw-r--r--   0        0        0     3930 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/llama/modeling_vllm_llama.py
--rw-r--r--   0        0        0     1763 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/mpt/__init__.py
--rw-r--r--   0        0        0     4293 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/mpt/configuration_mpt.py
--rw-r--r--   0        0        0     7910 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/mpt/modeling_mpt.py
--rw-r--r--   0        0        0     2501 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/opt/__init__.py
--rw-r--r--   0        0        0     3396 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/opt/configuration_opt.py
--rw-r--r--   0        0        0     4775 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/opt/modeling_flax_opt.py
--rw-r--r--   0        0        0     5677 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/opt/modeling_opt.py
--rw-r--r--   0        0        0     4665 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/opt/modeling_tf_opt.py
--rw-r--r--   0        0        0     1751 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/stablelm/__init__.py
--rw-r--r--   0        0        0     3315 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/stablelm/configuration_stablelm.py
--rw-r--r--   0        0        0     3968 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/stablelm/modeling_stablelm.py
--rw-r--r--   0        0        0     1766 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/starcoder/__init__.py
--rw-r--r--   0        0        0     2607 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/starcoder/configuration_starcoder.py
--rw-r--r--   0        0        0     6310 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/models/starcoder/modeling_starcoder.py
--rw-r--r--   0        0        0      368 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/playground/README.md
--rw-r--r--   0        0        0      598 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/playground/__init__.py
--rw-r--r--   0        0        0     1958 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/playground/_meta.yml
--rw-r--r--   0        0        0     3390 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/playground/falcon_tuned.py
--rw-r--r--   0        0        0     1768 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/playground/features.py
--rw-r--r--   0        0        0     8512 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/playground/llama2_qlora.py
--rw-r--r--   0        0        0     2942 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/playground/opt_tuned.py
--rw-r--r--   0        0        0     5195 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/serialisation/__init__.py
--rw-r--r--   0        0        0     1135 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/serialisation/constants.py
--rw-r--r--   0        0        0     4441 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/serialisation/ggml.py
--rw-r--r--   0        0        0    15544 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/serialisation/transformers.py
--rw-r--r--   0        0        0    17096 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/__init__.py
--rw-r--r--   0        0        0     4023 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/analytics.py
--rw-r--r--   0        0        0    11261 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/codegen.py
--rw-r--r--   0        0        0    20013 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/dantic.py
--rw-r--r--   0        0        0     1253 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/dummy_flax_objects.py
--rw-r--r--   0        0        0     1119 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/dummy_pt_and_cpm_kernels_objects.py
--rw-r--r--   0        0        0      911 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/dummy_pt_and_einops_objects.py
--rw-r--r--   0        0        0      898 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/dummy_pt_and_triton_objects.py
--rw-r--r--   0        0        0     2073 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/dummy_pt_objects.py
--rw-r--r--   0        0        0     1233 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/dummy_tf_objects.py
--rw-r--r--   0        0        0     1085 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/dummy_vllm_objects.py
--rw-r--r--   0        0        0    20528 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/import_utils.py
--rw-r--r--   0        0        0     6686 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/lazy.py
--rw-r--r--   0        0        0     2664 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm/utils/representation.py
--rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm_client/__init__.py
--rw-r--r--   0        0        0     2377 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm_client/_prompt.py
--rw-r--r--   0        0        0      867 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm_client/runtimes/__init__.py
--rw-r--r--   0        0        0    12945 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm_client/runtimes/base.py
--rw-r--r--   0        0        0     3693 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm_client/runtimes/grpc.py
--rw-r--r--   0        0        0     3170 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm_client/runtimes/http.py
--rw-r--r--   0        0        0      263 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm_js/package.json
--rw-r--r--   0        0        0      165 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm_js/tsconfig.cjs.json
--rw-r--r--   0        0        0      237 2020-02-02 00:00:00.000000 openllm-0.2.6/src/openllm_js/tsconfig.json
--rw-r--r--   0        0        0      837 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/__init__.py
--rw-r--r--   0        0        0      861 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/client_test.py
--rw-r--r--   0        0        0     9274 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/configuration_test.py
--rw-r--r--   0        0        0     2496 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/conftest.py
--rw-r--r--   0        0        0     1516 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/llm_test.py
--rw-r--r--   0        0        0     1461 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/models_test.py
--rw-r--r--   0        0        0     2734 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/package_test.py
--rw-r--r--   0        0        0    10504 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/strategies_test.py
--rw-r--r--   0        0        0      598 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/_strategies/__init__.py
--rw-r--r--   0        0        0     3201 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/_strategies/_configuration.py
--rw-r--r--   0        0        0      598 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/models/__init__.py
--rw-r--r--   0        0        0     9686 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/models/conftest.py
--rw-r--r--   0        0        0     1896 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/models/flan_t5_test.py
--rw-r--r--   0        0        0     1879 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/models/opt_test.py
--rw-r--r--   0        0        0      837 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/models/__snapshots__/flan_t5_test/test_flan_t5[container].json
--rw-r--r--   0        0        0      820 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/models/__snapshots__/flan_t5_test/test_flan_t5[local].json
--rw-r--r--   0        0        0      952 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/models/__snapshots__/opt_test/test_opt_125m[container].json
--rw-r--r--   0        0        0      941 2020-02-02 00:00:00.000000 openllm-0.2.6/tests/models/__snapshots__/opt_test/test_opt_125m[local].json
--rw-r--r--   0        0        0     1931 2020-02-02 00:00:00.000000 openllm-0.2.6/.gitignore
--rw-r--r--   0        0        0    10470 2020-02-02 00:00:00.000000 openllm-0.2.6/LICENSE.md
--rw-r--r--   0        0        0    24680 2020-02-02 00:00:00.000000 openllm-0.2.6/README.md
--rw-r--r--   0        0        0     3627 2020-02-02 00:00:00.000000 openllm-0.2.6/hatch.toml
--rw-r--r--   0        0        0    10567 2020-02-02 00:00:00.000000 openllm-0.2.6/pyproject.toml
--rw-r--r--   0        0        0    30097 2020-02-02 00:00:00.000000 openllm-0.2.6/PKG-INFO
+-rw-r--r--   0        0        0      215 2020-02-02 00:00:00.000000 openllm-0.2.7/.gitattributes
+-rw-r--r--   0        0        0     3550 2020-02-02 00:00:00.000000 openllm-0.2.7/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     2938 2020-02-02 00:00:00.000000 openllm-0.2.7/ADDING_NEW_MODEL.md
+-rw-r--r--   0        0        0    13282 2020-02-02 00:00:00.000000 openllm-0.2.7/CHANGELOG.md
+-rw-r--r--   0        0        0     2059 2020-02-02 00:00:00.000000 openllm-0.2.7/CITATION.cff
+-rw-r--r--   0        0        0     6704 2020-02-02 00:00:00.000000 openllm-0.2.7/DEVELOPMENT.md
+-rw-r--r--   0        0        0      283 2020-02-02 00:00:00.000000 openllm-0.2.7/nightly-requirements-gpu.txt
+-rw-r--r--   0        0        0      566 2020-02-02 00:00:00.000000 openllm-0.2.7/nightly-requirements.txt
+-rw-r--r--   0        0        0      519 2020-02-02 00:00:00.000000 openllm-0.2.7/package.json
+-rw-r--r--   0        0        0     3483 2020-02-02 00:00:00.000000 openllm-0.2.7/pyoxidizer.bzl
+-rw-r--r--   0        0        0      119 2020-02-02 00:00:00.000000 openllm-0.2.7/taplo.toml
+-rw-r--r--   0        0        0      620 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/__about__.py
+-rw-r--r--   0        0        0    12740 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/__init__.py
+-rw-r--r--   0        0        0      804 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/__main__.py
+-rw-r--r--   0        0        0    90013 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/_configuration.py
+-rw-r--r--   0        0        0     1923 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/_generation.py
+-rw-r--r--   0        0        0    71077 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/_llm.py
+-rw-r--r--   0        0        0     1637 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/_prompt.py
+-rw-r--r--   0        0        0     5974 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/_quantisation.py
+-rw-r--r--   0        0        0     3217 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/_schema.py
+-rw-r--r--   0        0        0     7301 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/_service.py
+-rw-r--r--   0        0        0    18488 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/_strategies.py
+-rw-r--r--   0        0        0     5361 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/_types.py
+-rw-r--r--   0        0        0   101935 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/cli.py
+-rw-r--r--   0        0        0     1908 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/client.py
+-rw-r--r--   0        0        0     1524 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/exceptions.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/py.typed
+-rw-r--r--   0        0        0     3406 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/testing.py
+-rw-r--r--   0        0        0     2103 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/bundle/__init__.py
+-rw-r--r--   0        0        0    14998 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/bundle/_package.py
+-rw-r--r--   0        0        0     1902 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/bundle/oci/Dockerfile-builder
+-rw-r--r--   0        0        0      170 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/bundle/oci/Dockerfile-vllm
+-rw-r--r--   0        0        0      762 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/bundle/oci/__init__.py
+-rw-r--r--   0        0        0      979 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/__init__.py
+-rw-r--r--   0        0        0     4228 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/auto/__init__.py
+-rw-r--r--   0        0        0     5810 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/auto/configuration_auto.py
+-rw-r--r--   0        0        0    11869 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/auto/factory.py
+-rw-r--r--   0        0        0     1337 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/auto/modeling_auto.py
+-rw-r--r--   0        0        0     1085 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/auto/modeling_flax_auto.py
+-rw-r--r--   0        0        0     1071 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/auto/modeling_tf_auto.py
+-rw-r--r--   0        0        0     1051 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/auto/modeling_vllm_auto.py
+-rw-r--r--   0        0        0     1865 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/baichuan/__init__.py
+-rw-r--r--   0        0        0     2812 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/baichuan/configuration_baichuan.py
+-rw-r--r--   0        0        0     3342 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/baichuan/modeling_baichuan.py
+-rw-r--r--   0        0        0     1850 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/chatglm/__init__.py
+-rw-r--r--   0        0        0     3230 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/chatglm/configuration_chatglm.py
+-rw-r--r--   0        0        0     3969 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/chatglm/modeling_chatglm.py
+-rw-r--r--   0        0        0     1745 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/dolly_v2/__init__.py
+-rw-r--r--   0        0        0     4397 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/dolly_v2/configuration_dolly_v2.py
+-rw-r--r--   0        0        0    12726 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/dolly_v2/modeling_dolly_v2.py
+-rw-r--r--   0        0        0     1721 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/falcon/__init__.py
+-rw-r--r--   0        0        0     2824 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/falcon/configuration_falcon.py
+-rw-r--r--   0        0        0     4913 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/falcon/modeling_falcon.py
+-rw-r--r--   0        0        0     2589 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/flan_t5/__init__.py
+-rw-r--r--   0        0        0     2597 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/flan_t5/configuration_flan_t5.py
+-rw-r--r--   0        0        0     3361 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/flan_t5/modeling_flan_t5.py
+-rw-r--r--   0        0        0     3765 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/flan_t5/modeling_flax_flan_t5.py
+-rw-r--r--   0        0        0     3182 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/flan_t5/modeling_tf_flan_t5.py
+-rw-r--r--   0        0        0     1745 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/gpt_neox/__init__.py
+-rw-r--r--   0        0        0     2819 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/gpt_neox/configuration_gpt_neox.py
+-rw-r--r--   0        0        0     3903 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/gpt_neox/modeling_gpt_neox.py
+-rw-r--r--   0        0        0     2264 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/llama/__init__.py
+-rw-r--r--   0        0        0     5366 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/llama/configuration_llama.py
+-rw-r--r--   0        0        0     4917 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/llama/modeling_llama.py
+-rw-r--r--   0        0        0     3930 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/llama/modeling_vllm_llama.py
+-rw-r--r--   0        0        0     1763 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/mpt/__init__.py
+-rw-r--r--   0        0        0     4293 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/mpt/configuration_mpt.py
+-rw-r--r--   0        0        0     7910 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/mpt/modeling_mpt.py
+-rw-r--r--   0        0        0     2501 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/opt/__init__.py
+-rw-r--r--   0        0        0     3396 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/opt/configuration_opt.py
+-rw-r--r--   0        0        0     4775 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/opt/modeling_flax_opt.py
+-rw-r--r--   0        0        0     5677 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/opt/modeling_opt.py
+-rw-r--r--   0        0        0     4665 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/opt/modeling_tf_opt.py
+-rw-r--r--   0        0        0     1751 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/stablelm/__init__.py
+-rw-r--r--   0        0        0     3315 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/stablelm/configuration_stablelm.py
+-rw-r--r--   0        0        0     3968 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/stablelm/modeling_stablelm.py
+-rw-r--r--   0        0        0     1766 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/starcoder/__init__.py
+-rw-r--r--   0        0        0     2607 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/starcoder/configuration_starcoder.py
+-rw-r--r--   0        0        0     6310 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/models/starcoder/modeling_starcoder.py
+-rw-r--r--   0        0        0      368 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/playground/README.md
+-rw-r--r--   0        0        0      598 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/playground/__init__.py
+-rw-r--r--   0        0        0     1958 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/playground/_meta.yml
+-rw-r--r--   0        0        0     3390 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/playground/falcon_tuned.py
+-rw-r--r--   0        0        0     1768 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/playground/features.py
+-rw-r--r--   0        0        0     9019 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/playground/llama2_qlora.py
+-rw-r--r--   0        0        0     2942 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/playground/opt_tuned.py
+-rw-r--r--   0        0        0     5195 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/serialisation/__init__.py
+-rw-r--r--   0        0        0     1135 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/serialisation/constants.py
+-rw-r--r--   0        0        0     4441 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/serialisation/ggml.py
+-rw-r--r--   0        0        0    16004 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/serialisation/transformers.py
+-rw-r--r--   0        0        0    17096 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/__init__.py
+-rw-r--r--   0        0        0     4023 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/analytics.py
+-rw-r--r--   0        0        0    11261 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/codegen.py
+-rw-r--r--   0        0        0    20013 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/dantic.py
+-rw-r--r--   0        0        0     1253 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/dummy_flax_objects.py
+-rw-r--r--   0        0        0     1119 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/dummy_pt_and_cpm_kernels_objects.py
+-rw-r--r--   0        0        0      911 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/dummy_pt_and_einops_objects.py
+-rw-r--r--   0        0        0      898 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/dummy_pt_and_triton_objects.py
+-rw-r--r--   0        0        0     2073 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/dummy_pt_objects.py
+-rw-r--r--   0        0        0     1233 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/dummy_tf_objects.py
+-rw-r--r--   0        0        0     1085 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/dummy_vllm_objects.py
+-rw-r--r--   0        0        0    20528 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/import_utils.py
+-rw-r--r--   0        0        0     6686 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/lazy.py
+-rw-r--r--   0        0        0     2664 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm/utils/representation.py
+-rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm_client/__init__.py
+-rw-r--r--   0        0        0     2377 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm_client/_prompt.py
+-rw-r--r--   0        0        0      867 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm_client/runtimes/__init__.py
+-rw-r--r--   0        0        0    12945 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm_client/runtimes/base.py
+-rw-r--r--   0        0        0     3693 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm_client/runtimes/grpc.py
+-rw-r--r--   0        0        0     3170 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm_client/runtimes/http.py
+-rw-r--r--   0        0        0      263 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm_js/package.json
+-rw-r--r--   0        0        0      165 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm_js/tsconfig.cjs.json
+-rw-r--r--   0        0        0      237 2020-02-02 00:00:00.000000 openllm-0.2.7/src/openllm_js/tsconfig.json
+-rw-r--r--   0        0        0      837 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/__init__.py
+-rw-r--r--   0        0        0      861 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/client_test.py
+-rw-r--r--   0        0        0     9274 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/configuration_test.py
+-rw-r--r--   0        0        0     2496 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/conftest.py
+-rw-r--r--   0        0        0     1516 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/llm_test.py
+-rw-r--r--   0        0        0     1461 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/models_test.py
+-rw-r--r--   0        0        0     2734 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/package_test.py
+-rw-r--r--   0        0        0    10504 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/strategies_test.py
+-rw-r--r--   0        0        0      598 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/_strategies/__init__.py
+-rw-r--r--   0        0        0     3201 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/_strategies/_configuration.py
+-rw-r--r--   0        0        0      598 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/models/__init__.py
+-rw-r--r--   0        0        0     9686 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/models/conftest.py
+-rw-r--r--   0        0        0     1896 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/models/flan_t5_test.py
+-rw-r--r--   0        0        0     1879 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/models/opt_test.py
+-rw-r--r--   0        0        0      837 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/models/__snapshots__/flan_t5_test/test_flan_t5[container].json
+-rw-r--r--   0        0        0      820 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/models/__snapshots__/flan_t5_test/test_flan_t5[local].json
+-rw-r--r--   0        0        0      952 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/models/__snapshots__/opt_test/test_opt_125m[container].json
+-rw-r--r--   0        0        0      941 2020-02-02 00:00:00.000000 openllm-0.2.7/tests/models/__snapshots__/opt_test/test_opt_125m[local].json
+-rw-r--r--   0        0        0     1931 2020-02-02 00:00:00.000000 openllm-0.2.7/.gitignore
+-rw-r--r--   0        0        0    10470 2020-02-02 00:00:00.000000 openllm-0.2.7/LICENSE.md
+-rw-r--r--   0        0        0    24680 2020-02-02 00:00:00.000000 openllm-0.2.7/README.md
+-rw-r--r--   0        0        0     3627 2020-02-02 00:00:00.000000 openllm-0.2.7/hatch.toml
+-rw-r--r--   0        0        0    10567 2020-02-02 00:00:00.000000 openllm-0.2.7/pyproject.toml
+-rw-r--r--   0        0        0    30097 2020-02-02 00:00:00.000000 openllm-0.2.7/PKG-INFO
```

### Comparing `openllm-0.2.6/.pre-commit-config.yaml` & `openllm-0.2.7/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/ADDING_NEW_MODEL.md` & `openllm-0.2.7/ADDING_NEW_MODEL.md`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/CHANGELOG.md` & `openllm-0.2.7/CHANGELOG.md`

 * *Files 1% similar despite different names*

```diff
@@ -14,14 +14,18 @@
 Do *NOT* add changelog entries here!
 
 This changelog is managed by towncrier and is compiled at release time.
 -->
 
 <!-- towncrier release notes start -->
 
+## [0.2.7](https://github.com/bentoml/openllm/tree/v0.2.7)
+No significant changes.
+
+
 ## [0.2.6](https://github.com/bentoml/openllm/tree/v0.2.6)
 
 ### Backwards-incompatible Changes
 
 - Updated signature for `load_model` and `load_tokenizer` not to allow tag.
   Tag can be accessed via `llm.tag`, or if using `openllm.serialisation` or `bentoml.transformers` then you can use `self._bentomodel`
```

### Comparing `openllm-0.2.6/CITATION.cff` & `openllm-0.2.7/CITATION.cff`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/DEVELOPMENT.md` & `openllm-0.2.7/DEVELOPMENT.md`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/nightly-requirements.txt` & `openllm-0.2.7/nightly-requirements.txt`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/package.json` & `openllm-0.2.7/package.json`

 * *Files 2% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9545454545454546%*

 * *Differences: {"'version'": "'0.2.7'"}*

```diff
@@ -11,12 +11,12 @@
     "engines": {
         "node": ">=16"
     },
     "license": "Apache 2.0",
     "name": "openllm",
     "private": true,
     "repository": "git@github.com:llmsys/OpenLLM.git",
-    "version": "0.2.6",
+    "version": "0.2.7",
     "workspaces": [
         "src/openllm_js"
     ]
 }
```

### Comparing `openllm-0.2.6/pyoxidizer.bzl` & `openllm-0.2.7/pyoxidizer.bzl`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/__about__.py` & `openllm-0.2.7/src/openllm/__about__.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,8 +7,8 @@
 #     http://www.apache.org/licenses/LICENSE-2.0
 #
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
-__version__ = "0.2.6"
+__version__ = "0.2.7"
```

### Comparing `openllm-0.2.6/src/openllm/__init__.py` & `openllm-0.2.7/src/openllm/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/__main__.py` & `openllm-0.2.7/src/openllm/__main__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/_configuration.py` & `openllm-0.2.7/src/openllm/_configuration.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/_generation.py` & `openllm-0.2.7/src/openllm/_generation.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/_llm.py` & `openllm-0.2.7/src/openllm/_llm.py`

 * *Files 1% similar despite different names*

```diff
@@ -42,27 +42,25 @@
 from ._configuration import _setattr_class
 from ._quantisation import infer_quantisation_config
 from .exceptions import ForbiddenAttributeError
 from .exceptions import GpuNotAvailableError
 from .utils import DEBUG
 from .utils import ENV_VARS_TRUE_VALUES
 from .utils import MYPY
-from .utils import SHOW_CODEGEN
 from .utils import EnvVarMixin
 from .utils import LazyLoader
 from .utils import ReprMixin
 from .utils import bentoml_cattr
 from .utils import codegen
 from .utils import first_not_none
 from .utils import in_docker
 from .utils import is_peft_available
 from .utils import is_torch_available
 from .utils import non_intrusive_setattr
 from .utils import normalize_attrs_to_model_tokenizer_pair
-from .utils import pkg
 from .utils import requires_dependencies
 from .utils import resolve_filepath
 from .utils import validate_is_path
 
 
 # NOTE: We need to do this so that overload can register
 # correct overloads to typing registry
@@ -146,14 +144,16 @@
         implementation: Given implementation for said LLM. One of t.Literal['pt', 'tf', 'flax']
         quiet: Whether to show warning logs. Default to 'False'
 
     Returns:
         A tuple of ``bentoml.Tag`` and a dict of unused kwargs.
     """
     model_name = normalise_model_name(model_id)
+    if os.getenv("OPENLLM_USE_LOCAL_LATEST", str(False)).upper() in ENV_VARS_TRUE_VALUES:
+        return bentoml.models.get(f"{implementation}-{model_name}").tag
 
     if validate_is_path(model_id):
         model_id = resolve_filepath(model_id)
         # special cases, if it is the model store, then we return the tags
         # this will happens within the container, where we use the relative path
         if in_docker() and os.getenv("BENTO_PATH") is not None:
             _store = ModelStore(Path(model_id).parent.parent)
@@ -361,14 +361,23 @@
     def load_tokenizer(self, tag: bentoml.Tag, **attrs: t.Any) -> T:
         """This function can be implemented to override how to load the tokenizer.
 
         See falcon for example implementation.
         """
         raise NotImplementedError
 
+    def save_pretrained(self, save_directory: str | Path, **attrs: t.Any) -> None:
+        """This function defines how this model can be saved to local store.
+
+        This will be called during ``import_model``. By default, it will use ``openllm.serialisation.save_pretrained``.
+        Additionally, the function signature are similar to ``transformers.PreTrainedModel.save_pretrained``
+        This is useful during fine tuning.
+        """
+        raise NotImplementedError
+
     # NOTE: All fields below are attributes that can be accessed by users.
     config_class: type[openllm.LLMConfig]
     """The config class to use for this LLM. If you are creating a custom LLM, you must specify this class."""
 
     bettertransformer: bool
     """Whether to load this LLM with FasterTransformer enabled. The order of loading is:
 
@@ -445,14 +454,18 @@
         def __call__(self, llm: LLM[M, T], **attrs: t.Any) -> T:
             ...
 
     class _llm_post_init_wrapper(t.Generic[M, T]):
         def __call__(self, llm: LLM[M, T]) -> T:
             ...
 
+    class _save_pretrained_wrapper(t.Generic[M, T]):
+        def __call__(self, llm: LLM[M, T], save_directory: str | Path, **attrs: t.Any) -> None:
+            ...
+
 
 def _wrapped_import_model(f: _import_model_wrapper[bentoml.Model, M, T]):
     @functools.wraps(f)
     def wrapper(
         self: LLM[M, T], *decls: t.Any, trust_remote_code: bool | None = None, **attrs: t.Any
     ) -> bentoml.Model:
         trust_remote_code = first_not_none(trust_remote_code, default=self.__llm_trust_remote_code__)
@@ -494,58 +507,66 @@
     def wrapper(self: LLM[M, T]):
         _default_post_init(self)
         f(self)
 
     return wrapper
 
 
+def _wrapped_save_pretrained(f: _save_pretrained_wrapper[M, T]):
+    @functools.wraps(f)
+    def wrapper(self: LLM[M, T], save_directory: str | Path, **attrs: t.Any) -> None:
+        if isinstance(save_directory, Path):
+            save_directory = str(save_directory)
+        if self.__llm_model__ is not None and self.bettertransformer and self.__llm_implementation__ == "pt":
+            from optimum.bettertransformer import BetterTransformer
+
+            self.__llm_model__ = t.cast(
+                M,
+                BetterTransformer.reverse(t.cast("transformers.PreTrainedModel", self.__llm_model__)),
+            )
+        f(self, save_directory, **attrs)
+
+    return wrapper
+
+
 def _make_assignment_script(cls: type[LLM[M, T]]) -> t.Callable[[type[LLM[M, T]]], None]:
     attributes = {
         "import_model": _wrapped_import_model,
         "load_model": _wrapped_load_model,
         "load_tokenizer": _wrapped_load_tokenizer,
         "llm_post_init": _wrapped_llm_post_init,
+        "save_pretrained": _wrapped_save_pretrained,
     }
     args: ListStr = []
     anns: DictStrAny = {}
     lines: ListStr = []
-    globs: DictStrAny = {
-        "cls": cls,
-        "_cached_attribute": attributes,
-        "_cached_getattribute_get": _object_getattribute.__get__,
-        "LLMInterface": LLMInterface,
-        "openllm": openllm,
-    }
+    globs: DictStrAny = {"cls": cls, "_cached_LLMInterface_get": _object_getattribute.__get__(LLMInterface)}
     # function initialisation
     for func, impl in attributes.items():
-        globs[f"__wrapped_{func}"] = impl
         impl_name = f"__wrapped_{func}"
+        globs.update({f"__serialisation_{func}": getattr(openllm.serialisation, func, None), impl_name: impl})
         cached_func_name = f"_cached_{cls.__name__}_func"
         if func == "llm_post_init":
-            func_call = f"_impl_{cls.__name__}_{func}={impl_name}"
+            func_call = f"_impl_{cls.__name__}_{func}={cached_func_name}"
         else:
-            func_call = f"_impl_{cls.__name__}_{func}={cached_func_name} if {cached_func_name} is not _cached_LLMInterface_getattr('{func}') else openllm.serialisation.{func}"
+            func_call = f"_impl_{cls.__name__}_{func}={cached_func_name} if {cached_func_name} is not _cached_LLMInterface_get('{func}') else __serialisation_{func}"
         lines.extend(
             [
-                "_cached_LLMInterface_getattr=_cached_getattribute_get(LLMInterface)",
                 f"{cached_func_name}=cls.{func}",
                 func_call,
                 _setattr_class(func, f"{impl_name}(_impl_{cls.__name__}_{func})"),
             ]
         )
 
     # cached attribute initialisation
     interface_anns = codegen.get_annotations(LLMInterface)
     for v in {"bentomodel", "model", "tokenizer", "adapter_map"}:
         lines.append(_setattr_class(f"__llm_{v}__", None))
         anns[f"__llm_{v}__"] = interface_anns.get("__llm_{v}__")
 
-    if SHOW_CODEGEN:
-        logger.info("Generated script for %s:\n\n%s", cls.__name__, "\n".join(lines))
-
     return codegen.generate_function(cls, "__assign_attr", lines, args=("cls", *args), globs=globs, annotations=anns)
 
 
 _AdaptersTuple: type[AdaptersTuple] = codegen.make_attr_tuple_class("AdaptersTuple", ["adapter_id", "name", "config"])
 
 
 @attr.define(slots=True, repr=False, init=False)
@@ -605,27 +626,14 @@
 
             Note that if LoRA is enabled (via either SDK or CLI), `self.model` will become a `peft.PeftModel`
             The original can then be accessed with 'self.model.get_base_model()'.
             """
             )
             setattr(cls, fn, original_fn)
 
-    # The following is the similar interface to HuggingFace pretrained protocol.
-    def save_pretrained(self, save_directory: str | Path, **attrs: t.Any) -> None:
-        if isinstance(save_directory, Path):
-            save_directory = str(save_directory)
-        if self.__llm_model__ is not None and self.bettertransformer and self.__llm_implementation__ == "pt":
-            from optimum.bettertransformer import BetterTransformer
-
-            self.__llm_model__ = t.cast(
-                M,
-                BetterTransformer.reverse(t.cast("transformers.PreTrainedModel", self.__llm_model__)),
-            )
-        openllm.serialisation.save_pretrained(self, save_directory, **attrs)
-
     @classmethod
     @overload
     def from_pretrained(
         cls,
         model_id: str | None = ...,
         model_version: str | None = ...,
         llm_config: openllm.LLMConfig | None = ...,
@@ -732,20 +740,18 @@
             adapter_id: The [LoRA](https://arxiv.org/pdf/2106.09685.pdf) pretrained id or local path to use for this LLM. Defaults to None.
             adapter_name: The adapter name to use for this LLM. Defaults to None.
             adapter_map: The adapter map to use for this LLM. Defaults to None. Note that this is mutually exclusive with adapter_id/adapter_name arguments.
             *args: The args to be passed to the model.
             **attrs: The kwargs to be passed to the model.
         """
         cfg_cls = cls.config_class
-        if model_id is None:
-            model_id = first_not_none(
-                cfg_cls.__openllm_env__["model_id_value"], default=cfg_cls.__openllm_default_id__
-            )
-        if runtime is None:
-            runtime = cfg_cls.__openllm_runtime__
+        model_id = first_not_none(
+            model_id, cfg_cls.__openllm_env__["model_id_value"], default=cfg_cls.__openllm_default_id__
+        )
+        runtime = first_not_none(runtime, default=cfg_cls.__openllm_runtime__)
 
         model_id, *maybe_revision = model_id.rsplit(":")
         if len(maybe_revision) > 0:
             if model_version is not None:
                 logger.warning(
                     "revision is specified within 'model_id' (%s), which will override the 'model_version=%s'",
                     maybe_revision[0],
@@ -807,18 +813,18 @@
         )
 
     @classmethod
     def _infer_tag_from_model_id(cls, model_id: str, model_version: str | None) -> bentoml.Tag:
         # XXX: Fix me later, if the model is a valid tag, then we return it directly
         # instead of creating a new tag from the model_id. this branch will be hit during `openllm build`
         try:
-            return bentoml.models.get(model_id).tag
+            return bentoml.models.get(model_id.lower()).tag
         except (ValueError, bentoml.exceptions.BentoMLException):
             try:
-                return bentoml.Tag.from_taglike(model_id)
+                return bentoml.Tag.from_taglike(model_id.lower())
             except (ValueError, bentoml.exceptions.BentoMLException):
                 return make_tag(
                     model_id,
                     model_version=model_version,
                     trust_remote_code=cls.config_class.__openllm_trust_remote_code__,
                     implementation=cls.__llm_implementation__,
                     quiet=True,
@@ -1138,18 +1144,15 @@
     @requires_dependencies("peft", extra="fine-tune")
     def prepare_for_training(
         self,
         adapter_type: AdapterType = "lora",
         use_gradient_checkpointing: bool = True,
         **attrs: t.Any,
     ) -> tuple[peft.PeftModel, T]:
-        if pkg.pkg_version_info("peft")[:2] >= (0, 4):
-            from peft import prepare_model_for_kbit_training
-        else:
-            from peft import prepare_model_for_int8_training as prepare_model_for_kbit_training
+        from peft import prepare_model_for_kbit_training
 
         peft_config = (
             self.config["fine_tune_strategies"]
             .get(
                 adapter_type,
                 FineTuneConfig(
                     adapter_type=t.cast("PeftType", adapter_type),
```

### Comparing `openllm-0.2.6/src/openllm/_prompt.py` & `openllm-0.2.7/src/openllm/_prompt.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/_quantisation.py` & `openllm-0.2.7/src/openllm/_quantisation.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/_schema.py` & `openllm-0.2.7/src/openllm/_schema.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/_service.py` & `openllm-0.2.7/src/openllm/_service.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/_strategies.py` & `openllm-0.2.7/src/openllm/_strategies.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/_types.py` & `openllm-0.2.7/src/openllm/_types.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/cli.py` & `openllm-0.2.7/src/openllm/cli.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/client.py` & `openllm-0.2.7/src/openllm/client.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/exceptions.py` & `openllm-0.2.7/src/openllm/exceptions.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/testing.py` & `openllm-0.2.7/src/openllm/testing.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/bundle/__init__.py` & `openllm-0.2.7/src/openllm/bundle/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/bundle/_package.py` & `openllm-0.2.7/src/openllm/bundle/_package.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/bundle/oci/Dockerfile-builder` & `openllm-0.2.7/src/openllm/bundle/oci/Dockerfile-builder`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/bundle/oci/__init__.py` & `openllm-0.2.7/src/openllm/bundle/oci/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/__init__.py` & `openllm-0.2.7/src/openllm/models/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/auto/__init__.py` & `openllm-0.2.7/src/openllm/models/auto/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/auto/configuration_auto.py` & `openllm-0.2.7/src/openllm/models/auto/configuration_auto.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/auto/factory.py` & `openllm-0.2.7/src/openllm/models/auto/factory.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/auto/modeling_auto.py` & `openllm-0.2.7/src/openllm/models/auto/modeling_auto.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/auto/modeling_flax_auto.py` & `openllm-0.2.7/src/openllm/models/auto/modeling_flax_auto.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/auto/modeling_tf_auto.py` & `openllm-0.2.7/src/openllm/models/auto/modeling_tf_auto.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/auto/modeling_vllm_auto.py` & `openllm-0.2.7/src/openllm/models/auto/modeling_vllm_auto.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/baichuan/__init__.py` & `openllm-0.2.7/src/openllm/models/baichuan/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/baichuan/configuration_baichuan.py` & `openllm-0.2.7/src/openllm/models/baichuan/configuration_baichuan.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/baichuan/modeling_baichuan.py` & `openllm-0.2.7/src/openllm/models/baichuan/modeling_baichuan.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/chatglm/__init__.py` & `openllm-0.2.7/src/openllm/models/chatglm/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/chatglm/configuration_chatglm.py` & `openllm-0.2.7/src/openllm/models/chatglm/configuration_chatglm.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/chatglm/modeling_chatglm.py` & `openllm-0.2.7/src/openllm/models/chatglm/modeling_chatglm.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/dolly_v2/__init__.py` & `openllm-0.2.7/src/openllm/models/dolly_v2/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/dolly_v2/configuration_dolly_v2.py` & `openllm-0.2.7/src/openllm/models/dolly_v2/configuration_dolly_v2.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/dolly_v2/modeling_dolly_v2.py` & `openllm-0.2.7/src/openllm/models/dolly_v2/modeling_dolly_v2.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/falcon/__init__.py` & `openllm-0.2.7/src/openllm/models/falcon/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/falcon/configuration_falcon.py` & `openllm-0.2.7/src/openllm/models/falcon/configuration_falcon.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/falcon/modeling_falcon.py` & `openllm-0.2.7/src/openllm/models/falcon/modeling_falcon.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/flan_t5/__init__.py` & `openllm-0.2.7/src/openllm/models/flan_t5/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/flan_t5/configuration_flan_t5.py` & `openllm-0.2.7/src/openllm/models/flan_t5/configuration_flan_t5.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/flan_t5/modeling_flan_t5.py` & `openllm-0.2.7/src/openllm/models/flan_t5/modeling_flan_t5.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/flan_t5/modeling_flax_flan_t5.py` & `openllm-0.2.7/src/openllm/models/flan_t5/modeling_flax_flan_t5.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/flan_t5/modeling_tf_flan_t5.py` & `openllm-0.2.7/src/openllm/models/flan_t5/modeling_tf_flan_t5.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/gpt_neox/__init__.py` & `openllm-0.2.7/src/openllm/models/gpt_neox/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/gpt_neox/configuration_gpt_neox.py` & `openllm-0.2.7/src/openllm/models/gpt_neox/configuration_gpt_neox.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/gpt_neox/modeling_gpt_neox.py` & `openllm-0.2.7/src/openllm/models/gpt_neox/modeling_gpt_neox.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/llama/__init__.py` & `openllm-0.2.7/src/openllm/models/llama/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/llama/configuration_llama.py` & `openllm-0.2.7/src/openllm/models/llama/configuration_llama.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/llama/modeling_llama.py` & `openllm-0.2.7/src/openllm/models/llama/modeling_llama.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/llama/modeling_vllm_llama.py` & `openllm-0.2.7/src/openllm/models/llama/modeling_vllm_llama.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/mpt/__init__.py` & `openllm-0.2.7/src/openllm/models/mpt/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/mpt/configuration_mpt.py` & `openllm-0.2.7/src/openllm/models/mpt/configuration_mpt.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/mpt/modeling_mpt.py` & `openllm-0.2.7/src/openllm/models/mpt/modeling_mpt.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/opt/__init__.py` & `openllm-0.2.7/src/openllm/models/opt/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/opt/configuration_opt.py` & `openllm-0.2.7/src/openllm/models/opt/configuration_opt.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/opt/modeling_flax_opt.py` & `openllm-0.2.7/src/openllm/models/opt/modeling_flax_opt.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/opt/modeling_opt.py` & `openllm-0.2.7/src/openllm/models/opt/modeling_opt.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/opt/modeling_tf_opt.py` & `openllm-0.2.7/src/openllm/models/opt/modeling_tf_opt.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/stablelm/__init__.py` & `openllm-0.2.7/src/openllm/models/stablelm/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/stablelm/configuration_stablelm.py` & `openllm-0.2.7/src/openllm/models/stablelm/configuration_stablelm.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/stablelm/modeling_stablelm.py` & `openllm-0.2.7/src/openllm/models/stablelm/modeling_stablelm.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/starcoder/__init__.py` & `openllm-0.2.7/src/openllm/models/starcoder/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/starcoder/configuration_starcoder.py` & `openllm-0.2.7/src/openllm/models/starcoder/configuration_starcoder.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/models/starcoder/modeling_starcoder.py` & `openllm-0.2.7/src/openllm/models/starcoder/modeling_starcoder.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/playground/__init__.py` & `openllm-0.2.7/src/openllm/playground/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/playground/_meta.yml` & `openllm-0.2.7/src/openllm/playground/_meta.yml`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/playground/falcon_tuned.py` & `openllm-0.2.7/src/openllm/playground/falcon_tuned.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/playground/features.py` & `openllm-0.2.7/src/openllm/playground/features.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/playground/llama2_qlora.py` & `openllm-0.2.7/src/openllm/playground/llama2_qlora.py`

 * *Files 4% similar despite different names*

```diff
@@ -41,14 +41,16 @@
     if "lm_head" in lora_module_names:  # needed for 16-bit
         lora_module_names.remove("lm_head")
     return list(lora_module_names)
 
 
 # Change this to the local converted path if you don't have access to the meta-llama model
 DEFAULT_MODEL_ID = "meta-llama/Llama-2-7b-hf"
+# change this to 'main' if you want to use the latest llama
+DEFAULT_MODEL_VERSION = "335a02887eb6684d487240bbc28b5699298c3135"
 DATASET_NAME = "databricks/databricks-dolly-15k"
 
 
 def format_dolly(sample):
     instruction = f"### Instruction\n{sample['instruction']}"
     context = f"### Context\n{sample['context']}" if len(sample["context"]) > 0 else None
     response = f"### Answer\n{sample['response']}"
@@ -115,34 +117,40 @@
     # Print total number of samples
     print(f"Total number of samples: {len(lm_dataset)}")
     return lm_dataset
 
 
 @openllm.utils.requires_dependencies("peft", extra="fine-tune")
 def prepare_for_int4_training(
-    model_id: str, gradient_checkpointing: bool = True, bf16: bool = True
+    model_id: str,
+    model_version: str | None = None,
+    gradient_checkpointing: bool = True,
+    bf16: bool = True,
 ) -> tuple[peft.PeftModel, transformers.LlamaTokenizerFast]:
     from peft.tuners.lora import LoraLayer
 
     llm = openllm.AutoLLM.for_model(
         "llama",
         model_id=model_id,
+        model_version=model_version,
         ensure_available=True,
         quantize="int4",
         bnb_4bit_compute_dtype=torch.bfloat16,
         use_cache=not gradient_checkpointing,
         device_map="auto",
     )
     print("Model summary:", llm.model)
 
     # get lora target modules
     modules = find_all_linear_names(llm.model)
     print(f"Found {len(modules)} modules to quantize: {modules}")
 
-    model, tokenizer = llm.prepare_for_training(adapter_type="lora", use_gradient_checkpointing=gradient_checkpointing)
+    model, tokenizer = llm.prepare_for_training(
+        adapter_type="lora", use_gradient_checkpointing=gradient_checkpointing, target_modules=modules
+    )
 
     # pre-process the model by upcasting the layer norms in float 32 for
     for name, module in model.named_modules():
         if isinstance(module, LoraLayer):
             if bf16:
                 module = module.to(torch.bfloat16)
         if "norm" in name:
@@ -166,31 +174,35 @@
     output_dir: str = dataclasses.field(default=os.path.join(os.getcwd(), "outputs", "llama"))
     save_strategy: str = dataclasses.field(default="no")
 
 
 @dataclasses.dataclass
 class ModelArguments:
     model_id: str = dataclasses.field(default=DEFAULT_MODEL_ID)
+    model_version: str = dataclasses.field(default=DEFAULT_MODEL_VERSION)
     seed: int = dataclasses.field(default=42)
     merge_weights: bool = dataclasses.field(default=False)
 
 
-parser = transformers.HfArgumentParser((ModelArguments, TrainingArguments))
-if len(sys.argv) == 2 and sys.argv[1].endswith(".json"):
-    # If we pass only one argument to the script and it's the path to a json file,
-    # let's parse it to get our arguments.
-    model_args, training_args = parser.parse_json_file(json_file=os.path.abspath(sys.argv[1]))
+if openllm.utils.in_notebook():
+    model_args, training_rags = ModelArguments(), TrainingArguments()
 else:
-    model_args, training_args = t.cast(
-        t.Tuple[ModelArguments, TrainingArguments], parser.parse_args_into_dataclasses()
-    )
+    parser = transformers.HfArgumentParser((ModelArguments, TrainingArguments))
+    if len(sys.argv) == 2 and sys.argv[1].endswith(".json"):
+        # If we pass only one argument to the script and it's the path to a json file,
+        # let's parse it to get our arguments.
+        model_args, training_args = parser.parse_json_file(json_file=os.path.abspath(sys.argv[1]))
+    else:
+        model_args, training_args = t.cast(
+            t.Tuple[ModelArguments, TrainingArguments], parser.parse_args_into_dataclasses()
+        )
 
 
 # import the model first hand
-openllm.import_model("llama", model_id=model_args.model_id)
+openllm.import_model("llama", model_id=model_args.model_id, model_version=model_args.model_version)
 
 
 def train_loop(model_args: ModelArguments, training_args: TrainingArguments):
     import peft
 
     transformers.set_seed(model_args.seed)
```

### Comparing `openllm-0.2.6/src/openllm/playground/opt_tuned.py` & `openllm-0.2.7/src/openllm/playground/opt_tuned.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/serialisation/__init__.py` & `openllm-0.2.7/src/openllm/serialisation/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/serialisation/constants.py` & `openllm-0.2.7/src/openllm/serialisation/constants.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/serialisation/ggml.py` & `openllm-0.2.7/src/openllm/serialisation/ggml.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/serialisation/transformers.py` & `openllm-0.2.7/src/openllm/serialisation/transformers.py`

 * *Files 2% similar despite different names*

```diff
@@ -162,14 +162,18 @@
             **hub_attrs,
             **attrs,
         )
         metadata["_pretrained_class"] = model.__class__.__name__
         metadata["_framework"] = model.model.framework
         signatures["generate"] = {"batchable": False}
     else:
+        if "quantization_config" in attrs and getattr(attrs["quantization_config"], "load_in_4bit", False):
+            # this model might be called with --quantize int4, therefore we need to pop this out
+            # since saving int4 is not yet supported
+            attrs.pop("quantization_config")
         model = t.cast(
             "_transformers.PreTrainedModel",
             infer_autoclass_from_llm_config(llm, config).from_pretrained(
                 llm.model_id,
                 *decls,
                 config=config,
                 trust_remote_code=trust_remote_code,
@@ -202,20 +206,17 @@
                 importlib.import_module(model.__module__),
                 importlib.import_module(_tokenizer.__module__),
             ]
             if trust_remote_code
             else None,
             metadata=metadata,
         ) as bentomodel:
-            _tokenizer.save_pretrained(bentomodel.path)
-
-            if quantize_method == "gptq":
-                model.save_quantized(bentomodel.path, use_safetensors=safe_serialisation)
-            else:
-                model.save_pretrained(bentomodel.path, safe_serialization=safe_serialisation)
+            save_pretrained(
+                llm, bentomodel.path, model=model, tokenizer=_tokenizer, safe_serialization=safe_serialisation
+            )
             return bentomodel
     finally:
         # NOTE: We need to free up the cache after importing the model
         # in the case where users first run openllm start without the model
         # available locally.
         if is_torch_available() and torch.cuda.is_available():
             torch.cuda.empty_cache()
@@ -307,47 +308,53 @@
         from optimum.bettertransformer import BetterTransformer
 
         model = BetterTransformer.transform(model)  # type: ignore
     return t.cast("M", model)
 
 
 def save_pretrained(
-    llm: openllm.LLM[t.Any, t.Any],
+    llm: openllm.LLM[M, T],
     save_directory: str,
+    model: M | None = None,
+    tokenizer: T | None = None,
     is_main_process: bool = True,
     state_dict: DictStrAny | None = None,
     save_function: t.Callable[..., None] | None = None,
     push_to_hub: bool = False,
     max_shard_size: int | str = "10GB",
     safe_serialization: bool = False,
     variant: str | None = None,
     **attrs: t.Any,
 ) -> None:
     """Light wrapper around ``transformers.PreTrainedTokenizer.save_pretrained`` and ``transformers.PreTrainedModel.save_pretrained``."""
+    model = first_not_none(model, default=llm.__llm_model__)
+    tokenizer = first_not_none(tokenizer, default=llm.__llm_tokenizer__)
     save_function = first_not_none(save_function, default=torch.save)
-
     model_save_attrs, tokenizer_save_attrs = normalize_attrs_to_model_tokenizer_pair(**attrs)
-
     safe_serialization = safe_serialization or llm._serialisation_format == "safetensors"
+
+    if model is None or tokenizer is None:
+        raise RuntimeError("Failed to find loaded model or tokenizer to save to local store.")
+
     if llm._quantize_method == "gptq":
         if not is_autogptq_available():
             raise OpenLLMException(
                 "GPTQ quantisation requires 'auto-gptq' (Not found in local environment). Install it with 'pip install \"openllm[gptq]\"'"
             )
         if llm.config["model_type"] != "causal_lm":
             raise OpenLLMException(f"GPTQ only support Causal LM (got {llm.__class__} of {llm.config['model_type']})")
-        llm.model.save_quantized(save_directory, use_safetensors=safe_serialization)
-    elif isinstance(llm.model, _transformers.Pipeline):
-        llm.model.save_pretrained(save_directory, safe_serialization=safe_serialization)
+        model.save_quantized(save_directory, use_safetensors=safe_serialization)
+    elif isinstance(model, _transformers.Pipeline):
+        model.save_pretrained(save_directory, safe_serialization=safe_serialization)
     else:
-        llm.model.save_pretrained(
+        model.save_pretrained(
             save_directory,
             is_main_process=is_main_process,
             state_dict=state_dict,
             save_function=save_function,
             push_to_hub=push_to_hub,
             max_shard_size=max_shard_size,
             safe_serialization=safe_serialization,
             variant=variant,
             **model_save_attrs,
         )
-    llm.tokenizer.save_pretrained(save_directory, push_to_hub=push_to_hub, **tokenizer_save_attrs)
+    tokenizer.save_pretrained(save_directory, push_to_hub=push_to_hub, **tokenizer_save_attrs)
```

### Comparing `openllm-0.2.6/src/openllm/utils/__init__.py` & `openllm-0.2.7/src/openllm/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/analytics.py` & `openllm-0.2.7/src/openllm/utils/analytics.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/codegen.py` & `openllm-0.2.7/src/openllm/utils/codegen.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/dantic.py` & `openllm-0.2.7/src/openllm/utils/dantic.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/dummy_flax_objects.py` & `openllm-0.2.7/src/openllm/utils/dummy_flax_objects.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/dummy_pt_and_cpm_kernels_objects.py` & `openllm-0.2.7/src/openllm/utils/dummy_pt_and_cpm_kernels_objects.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/dummy_pt_and_einops_objects.py` & `openllm-0.2.7/src/openllm/utils/dummy_pt_and_einops_objects.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/dummy_pt_and_triton_objects.py` & `openllm-0.2.7/src/openllm/utils/dummy_pt_and_triton_objects.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/dummy_pt_objects.py` & `openllm-0.2.7/src/openllm/utils/dummy_pt_objects.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/dummy_tf_objects.py` & `openllm-0.2.7/src/openllm/utils/dummy_tf_objects.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/dummy_vllm_objects.py` & `openllm-0.2.7/src/openllm/utils/dummy_vllm_objects.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/import_utils.py` & `openllm-0.2.7/src/openllm/utils/import_utils.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/lazy.py` & `openllm-0.2.7/src/openllm/utils/lazy.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm/utils/representation.py` & `openllm-0.2.7/src/openllm/utils/representation.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm_client/__init__.py` & `openllm-0.2.7/src/openllm_client/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm_client/_prompt.py` & `openllm-0.2.7/src/openllm_client/_prompt.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm_client/runtimes/__init__.py` & `openllm-0.2.7/src/openllm_client/runtimes/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm_client/runtimes/base.py` & `openllm-0.2.7/src/openllm_client/runtimes/base.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm_client/runtimes/grpc.py` & `openllm-0.2.7/src/openllm_client/runtimes/grpc.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/src/openllm_client/runtimes/http.py` & `openllm-0.2.7/src/openllm_client/runtimes/http.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/__init__.py` & `openllm-0.2.7/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/client_test.py` & `openllm-0.2.7/tests/client_test.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/configuration_test.py` & `openllm-0.2.7/tests/configuration_test.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/conftest.py` & `openllm-0.2.7/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/llm_test.py` & `openllm-0.2.7/tests/llm_test.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/models_test.py` & `openllm-0.2.7/tests/models_test.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/package_test.py` & `openllm-0.2.7/tests/package_test.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/strategies_test.py` & `openllm-0.2.7/tests/strategies_test.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/_strategies/__init__.py` & `openllm-0.2.7/tests/_strategies/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/_strategies/_configuration.py` & `openllm-0.2.7/tests/_strategies/_configuration.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/models/__init__.py` & `openllm-0.2.7/tests/models/__init__.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/models/conftest.py` & `openllm-0.2.7/tests/models/conftest.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/models/flan_t5_test.py` & `openllm-0.2.7/tests/models/flan_t5_test.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/models/opt_test.py` & `openllm-0.2.7/tests/models/opt_test.py`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/models/__snapshots__/flan_t5_test/test_flan_t5[container].json` & `openllm-0.2.7/tests/models/__snapshots__/flan_t5_test/test_flan_t5[container].json`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/models/__snapshots__/flan_t5_test/test_flan_t5[local].json` & `openllm-0.2.7/tests/models/__snapshots__/flan_t5_test/test_flan_t5[local].json`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/models/__snapshots__/opt_test/test_opt_125m[container].json` & `openllm-0.2.7/tests/models/__snapshots__/opt_test/test_opt_125m[container].json`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/tests/models/__snapshots__/opt_test/test_opt_125m[local].json` & `openllm-0.2.7/tests/models/__snapshots__/opt_test/test_opt_125m[local].json`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/.gitignore` & `openllm-0.2.7/.gitignore`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/LICENSE.md` & `openllm-0.2.7/LICENSE.md`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/README.md` & `openllm-0.2.7/README.md`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/hatch.toml` & `openllm-0.2.7/hatch.toml`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/pyproject.toml` & `openllm-0.2.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `openllm-0.2.6/PKG-INFO` & `openllm-0.2.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: openllm
-Version: 0.2.6
+Version: 0.2.7
 Summary: OpenLLM: Operating LLMs in production
 Project-URL: Blog, https://modelserving.com
 Project-URL: Discord, https://l.bentoml.com/join-openllm-discord
 Project-URL: Documentation, https://github.com/bentoml/openllm#readme
 Project-URL: GitHub, https://github.com/bentoml/openllm
 Project-URL: History, https://github.com/bentoml/openllm/blob/main/CHANGELOG.md
 Project-URL: Homepage, https://bentoml.com
```

