# Comparing `tmp/krakenci_server-1.2.2.tar.gz` & `tmp/krakenci_server-1.3.25.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "krakenci_server-1.2.2.tar", max compression
+gzip compressed data, was "krakenci_server-1.3.25.tar", max compression
```

## Comparing `krakenci_server-1.2.2.tar` & `krakenci_server-1.3.25.tar`

### file list

```diff
@@ -1,126 +1,127 @@
--rw-r--r--   0        0        0     2900 2023-05-20 18:21:27.692439 krakenci_server-1.2.2/README.md
--rw-r--r--   0        0        0        0 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/__init__.py
--rw-r--r--   0        0        0       38 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/README
--rw-r--r--   0        0        0        0 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/__init__.py
--rw-r--r--   0        0        0     2032 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/alembic.ini
--rw-r--r--   0        0        0     2041 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/apply.py
--rw-r--r--   0        0        0     2703 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/env.py
--rw-r--r--   0        0        0      494 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/script.py.mako
--rw-r--r--   0        0        0      560 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/050fbc3d126c_added_deployment_to_agents_group.py
--rw-r--r--   0        0        0      707 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/0615faca43b1_added_url_tag_and_tool_file_to_tool.py
--rw-r--r--   0        0        0      433 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/0731897c862e_add_enabled_to_stage.py
--rw-r--r--   0        0        0      448 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/0ad7507aa6d0_added_age_to_issue.py
--rw-r--r--   0        0        0      562 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/19396769e240_added_extra_atrs_to_agents_group.py
--rw-r--r--   0        0        0      461 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/1982be95e79f_added_system_to_job.py
--rw-r--r--   0        0        0     1173 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/1cf31ab18f84_create_secret_table.py
--rw-r--r--   0        0        0     1485 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/1f5039135dd8_removed_enabled_from_projects.py
--rw-r--r--   0        0        0     1122 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/26c6d691e7ce_added_last_flows_to_branch.py
--rw-r--r--   0        0        0      587 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/2996b1b6e227_user_is_session_nullable.py
--rw-r--r--   0        0        0      654 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/29b96da53f09_added_reason_to_run.py
--rw-r--r--   0        0        0      533 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/2b5751b83fec_added_artifacts_to_flow.py
--rw-r--r--   0        0        0     1035 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/2dd5cf2d12dc_added_new_repo_fields_to_stage.py
--rw-r--r--   0        0        0      482 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/38088514157a_removed_cancel_from_agent.py
--rw-r--r--   0        0        0      656 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/3c1af14e0370_added_timeouts_to_stage_and_job.py
--rw-r--r--   0        0        0      527 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/411094f6b709_added_details_to_user.py
--rw-r--r--   0        0        0    21962 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/42ea01a6cf31_convert_timestamps_to_with_timezones.py
--rw-r--r--   0        0        0      458 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/466de256799e_added_label_to_run.py
--rw-r--r--   0        0        0     1867 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/4a7ac9143bb1_added_branch_sequences.py
--rw-r--r--   0        0        0      492 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/54efe873f88f_added_git_clone_params_to_stage.py
--rw-r--r--   0        0        0     3897 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/5b13b262b132_added_repo_changes.py
--rw-r--r--   0        0        0      545 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/5c16623f4d55_added_fields_masked_to_step.py
--rw-r--r--   0        0        0      527 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/5e38f55beb11_added_summary_to_flow.py
--rw-r--r--   0        0        0      407 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/66808ea51a72_delete_setting_records_with_no_group.py
--rw-r--r--   0        0        0     1028 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/6745adaf40e5_added_schema_repo_to_stage.py
--rw-r--r--   0        0        0      478 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/67d4f5a5ee98_added_authorized_to_executor.py
--rw-r--r--   0        0        0      638 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/735e81eedae4_change_project_id_in_executorgroup_to_.py
--rw-r--r--   0        0        0      457 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/73db0f22e1e6_added_cancel_to_agent.py
--rw-r--r--   0        0        0      500 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/770cfcc80cfb_added_relevancy_to_test_case_result.py
--rw-r--r--   0        0        0      706 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/818e190ca142_move_webhook_to_project.py
--rw-r--r--   0        0        0     1732 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/8200318b9e18_added_several_stats_fields_to_run.py
--rw-r--r--   0        0        0     1317 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/87358b464400_added_casbin_rules_table.py
--rw-r--r--   0        0        0     1737 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/899dadc28f9c_added_missing_indexes.py
--rw-r--r--   0        0        0     5629 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/89ffd52f1f00_rename_executor_to_agent.py
--rw-r--r--   0        0        0      490 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/8b4adeca953d_added_group_to_setting.py
--rw-r--r--   0        0        0      551 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/9666bf8c1bb0_added_details_to_user_session.py
--rw-r--r--   0        0        0      826 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/98af95844f27_added_results_change_stats_to_run.py
--rw-r--r--   0        0        0      509 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/9d8d8713c1ad_added_unique_index_for_address_of_non_.py
--rw-r--r--   0        0        0        0 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/__init__.py
--rw-r--r--   0        0        0      700 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/a0741baf2dbc_added_indexes_to_test_case_results.py
--rw-r--r--   0        0        0      542 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/a26a02d0ac01_added_extra_atrs_to_agents.py
--rw-r--r--   0        0        0      698 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/a35aec7afa0a_added_processed_at_in_run_and_index_to_.py
--rw-r--r--   0        0        0      469 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/a7de4bdee425_added_section_to_artifact.py
--rw-r--r--   0        0        0     1385 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/ab9326d5fc02_added_index_to_flows.py
--rw-r--r--   0        0        0      690 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/af348b43d9d5_extended_tool.py
--rw-r--r--   0        0        0      626 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/b2c9024746f5_added_unique_constraint_for_system_name_.py
--rw-r--r--   0        0        0      859 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/b510fae321ba_added_seq_to_flow_and_run.py
--rw-r--r--   0        0        0      522 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/b5cc62f79980_add_extra_to_issue.py
--rw-r--r--   0        0        0      604 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/b84bdc5d3c67_uniqued_agent_address.py
--rw-r--r--   0        0        0      698 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/b908e219f07f_longer_message_in_issue.py
--rw-r--r--   0        0        0      384 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/ba436d491bf8_update_stage_enabled_to_true.py
--rw-r--r--   0        0        0     1478 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/bb0d4908ba49_added_artifact_and_file.py
--rw-r--r--   0        0        0     1377 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/bdcdbb4b5b3f_added_user_data_to_several_entities.py
--rw-r--r--   0        0        0      880 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/befa07ac5d1c_changed_tool_version_to_string.py
--rw-r--r--   0        0        0     3622 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/cb7654d57bca_added_systems_table_and_host_info_user_.py
--rw-r--r--   0        0        0    11177 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/ce05198f524a_convert_char_n_to_text.py
--rw-r--r--   0        0        0      562 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/cea0e48abb5a_added_retention_policy_to_branch.py
--rw-r--r--   0        0        0      461 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/d2b23f410d02_added_label_to_flow.py
--rw-r--r--   0        0        0      714 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/d45087b62027_move_trigger_data_to_flow.py
--rw-r--r--   0        0        0     1542 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/d524cbcbf19c_added_users_and_users_session.py
--rw-r--r--   0        0        0      530 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/dae910bd9587_added_repo_data_to_run.py
--rw-r--r--   0        0        0      719 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/e0d8421619c2_removed_unique_constraint_agent_non_.py
--rw-r--r--   0        0        0      814 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/e404f52562c2_added_unique_constraints_on_branch_name_.py
--rw-r--r--   0        0        0     1638 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/f566580fd139_added_test_case_comment_table.py
--rw-r--r--   0        0        0      476 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/migrations/versions/ff4a425a6070_added_last_seen_to_executor.py
--rw-r--r--   0        0        0      582 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/__init__.py
--rw-r--r--   0        0        0    12197 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/access.py
--rw-r--r--   0        0        0     2919 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/agentblob.py
--rw-r--r--   0        0        0    10192 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/authn.py
--rw-r--r--   0        0        0    22134 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/backend.py
--rw-r--r--   0        0        0     4378 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/badge.py
--rw-r--r--   0        0        0        0 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/bg/__init__.py
--rw-r--r--   0        0        0    44857 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/bg/jobs.py
--rw-r--r--   0        0        0     6287 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/chops.py
--rw-r--r--   0        0        0        0 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/cloud/__init__.py
--rw-r--r--   0        0        0     2003 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/cloud/aws.py
--rw-r--r--   0        0        0     9147 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/cloud/aws_ec2.py
--rw-r--r--   0        0        0     7191 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/cloud/aws_ecs.py
--rw-r--r--   0        0        0    17629 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/cloud/azure.py
--rw-r--r--   0        0        0     3244 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/cloud/cloud.py
--rw-r--r--   0        0        0     1892 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/cloud/common.py
--rw-r--r--   0        0        0     9421 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/cloud/k8s.py
--rw-r--r--   0        0        0        0 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/config.py
--rw-r--r--   0        0        0     5127 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/consts.py
--rw-r--r--   0        0        0     3772 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/datastore.py
--rw-r--r--   0        0        0     1687 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/dbutils.py
--rw-r--r--   0        0        0    18026 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/exec_utils.py
--rw-r--r--   0        0        0    21211 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/execution.py
--rw-r--r--   0        0        0     9981 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/gitops.py
--rw-r--r--   0        0        0    27015 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/initdb.py
--rw-r--r--   0        0        0     5460 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/job_log.py
--rw-r--r--   0        0        0     4489 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/kkrq.py
--rw-r--r--   0        0        0    14059 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/logs.py
--rw-r--r--   0        0        0    46016 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/management.py
--rw-r--r--   0        0        0     4435 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/minioops.py
--rw-r--r--   0        0        0    47658 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/models.py
--rw-r--r--   0        0        0    10039 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/notify.py
--rwxr-xr-x   0        0        0     6478 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/planner.py
--rw-r--r--   0        0        0     1248 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/pljobs.py
--rw-r--r--   0        0        0     4440 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/qneck.py
--rw-r--r--   0        0        0    11643 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/results.py
--rwxr-xr-x   0        0        0     5714 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/scheduler.py
--rw-r--r--   0        0        0    15415 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/schema.py
--rw-r--r--   0        0        0    30836 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/schemaval.py
--rwxr-xr-x   0        0        0     7508 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/server.py
--rw-r--r--   0        0        0     2010 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/srvcheck.py
--rw-r--r--   0        0        0     3908 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/storage.py
--rw-r--r--   0        0        0    83344 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/swagger.yml
--rw-r--r--   0        0        0     2222 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/toolops.py
--rw-r--r--   0        0        0     3197 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/toolutils.py
--rw-r--r--   0        0        0    10872 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/users.py
--rw-r--r--   0        0        0     1032 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/utils.py
--rw-r--r--   0        0        0    19687 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/watchdog.py
--rw-r--r--   0        0        0    12005 2023-05-20 18:20:04.000000 krakenci_server-1.2.2/kraken/server/webhooks.py
--rw-r--r--   0        0        0       18 2023-05-20 18:21:27.688444 krakenci_server-1.2.2/kraken/version.py
--rw-r--r--   0        0        0     2439 2023-05-20 18:21:28.579345 krakenci_server-1.2.2/pyproject.tml
--rw-r--r--   0        0        0     5341 1970-01-01 00:00:00.000000 krakenci_server-1.2.2/setup.py
--rw-r--r--   0        0        0     5708 1970-01-01 00:00:00.000000 krakenci_server-1.2.2/PKG-INFO
+-rw-r--r--   0        0        0     2900 2023-07-22 13:19:52.793934 krakenci_server-1.3.25/README.md
+-rw-r--r--   0        0        0        0 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/__init__.py
+-rw-r--r--   0        0        0       38 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/README
+-rw-r--r--   0        0        0        0 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/__init__.py
+-rw-r--r--   0        0        0     2032 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/alembic.ini
+-rw-r--r--   0        0        0     2041 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/apply.py
+-rw-r--r--   0        0        0     2703 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/env.py
+-rw-r--r--   0        0        0      494 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/script.py.mako
+-rw-r--r--   0        0        0      560 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/050fbc3d126c_added_deployment_to_agents_group.py
+-rw-r--r--   0        0        0      707 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/0615faca43b1_added_url_tag_and_tool_file_to_tool.py
+-rw-r--r--   0        0        0      433 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/0731897c862e_add_enabled_to_stage.py
+-rw-r--r--   0        0        0      448 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/0ad7507aa6d0_added_age_to_issue.py
+-rw-r--r--   0        0        0      562 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/19396769e240_added_extra_atrs_to_agents_group.py
+-rw-r--r--   0        0        0      461 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/1982be95e79f_added_system_to_job.py
+-rw-r--r--   0        0        0     1173 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/1cf31ab18f84_create_secret_table.py
+-rw-r--r--   0        0        0     1485 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/1f5039135dd8_removed_enabled_from_projects.py
+-rw-r--r--   0        0        0     1122 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/26c6d691e7ce_added_last_flows_to_branch.py
+-rw-r--r--   0        0        0      587 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/2996b1b6e227_user_is_session_nullable.py
+-rw-r--r--   0        0        0      654 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/29b96da53f09_added_reason_to_run.py
+-rw-r--r--   0        0        0      533 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/2b5751b83fec_added_artifacts_to_flow.py
+-rw-r--r--   0        0        0     1035 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/2dd5cf2d12dc_added_new_repo_fields_to_stage.py
+-rw-r--r--   0        0        0      482 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/38088514157a_removed_cancel_from_agent.py
+-rw-r--r--   0        0        0      656 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/3c1af14e0370_added_timeouts_to_stage_and_job.py
+-rw-r--r--   0        0        0      527 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/411094f6b709_added_details_to_user.py
+-rw-r--r--   0        0        0    21962 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/42ea01a6cf31_convert_timestamps_to_with_timezones.py
+-rw-r--r--   0        0        0      458 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/466de256799e_added_label_to_run.py
+-rw-r--r--   0        0        0     1867 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/4a7ac9143bb1_added_branch_sequences.py
+-rw-r--r--   0        0        0      492 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/54efe873f88f_added_git_clone_params_to_stage.py
+-rw-r--r--   0        0        0     3897 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/5b13b262b132_added_repo_changes.py
+-rw-r--r--   0        0        0      545 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/5c16623f4d55_added_fields_masked_to_step.py
+-rw-r--r--   0        0        0      527 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/5e38f55beb11_added_summary_to_flow.py
+-rw-r--r--   0        0        0      407 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/66808ea51a72_delete_setting_records_with_no_group.py
+-rw-r--r--   0        0        0     1028 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/6745adaf40e5_added_schema_repo_to_stage.py
+-rw-r--r--   0        0        0      478 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/67d4f5a5ee98_added_authorized_to_executor.py
+-rw-r--r--   0        0        0      638 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/735e81eedae4_change_project_id_in_executorgroup_to_.py
+-rw-r--r--   0        0        0      457 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/73db0f22e1e6_added_cancel_to_agent.py
+-rw-r--r--   0        0        0      500 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/770cfcc80cfb_added_relevancy_to_test_case_result.py
+-rw-r--r--   0        0        0      706 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/818e190ca142_move_webhook_to_project.py
+-rw-r--r--   0        0        0     1732 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/8200318b9e18_added_several_stats_fields_to_run.py
+-rw-r--r--   0        0        0     1317 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/87358b464400_added_casbin_rules_table.py
+-rw-r--r--   0        0        0     1737 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/899dadc28f9c_added_missing_indexes.py
+-rw-r--r--   0        0        0     5629 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/89ffd52f1f00_rename_executor_to_agent.py
+-rw-r--r--   0        0        0      490 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/8b4adeca953d_added_group_to_setting.py
+-rw-r--r--   0        0        0      551 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/9666bf8c1bb0_added_details_to_user_session.py
+-rw-r--r--   0        0        0      826 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/98af95844f27_added_results_change_stats_to_run.py
+-rw-r--r--   0        0        0      509 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/9d8d8713c1ad_added_unique_index_for_address_of_non_.py
+-rw-r--r--   0        0        0      536 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/9e57e0f30a5f_added_fields_raw_to_step.py
+-rw-r--r--   0        0        0        0 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/__init__.py
+-rw-r--r--   0        0        0      700 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/a0741baf2dbc_added_indexes_to_test_case_results.py
+-rw-r--r--   0        0        0      542 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/a26a02d0ac01_added_extra_atrs_to_agents.py
+-rw-r--r--   0        0        0      698 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/a35aec7afa0a_added_processed_at_in_run_and_index_to_.py
+-rw-r--r--   0        0        0      469 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/a7de4bdee425_added_section_to_artifact.py
+-rw-r--r--   0        0        0     1385 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/ab9326d5fc02_added_index_to_flows.py
+-rw-r--r--   0        0        0      690 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/af348b43d9d5_extended_tool.py
+-rw-r--r--   0        0        0      626 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/b2c9024746f5_added_unique_constraint_for_system_name_.py
+-rw-r--r--   0        0        0      859 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/b510fae321ba_added_seq_to_flow_and_run.py
+-rw-r--r--   0        0        0      522 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/b5cc62f79980_add_extra_to_issue.py
+-rw-r--r--   0        0        0      604 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/b84bdc5d3c67_uniqued_agent_address.py
+-rw-r--r--   0        0        0      698 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/b908e219f07f_longer_message_in_issue.py
+-rw-r--r--   0        0        0      384 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/ba436d491bf8_update_stage_enabled_to_true.py
+-rw-r--r--   0        0        0     1478 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/bb0d4908ba49_added_artifact_and_file.py
+-rw-r--r--   0        0        0     1377 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/bdcdbb4b5b3f_added_user_data_to_several_entities.py
+-rw-r--r--   0        0        0      880 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/befa07ac5d1c_changed_tool_version_to_string.py
+-rw-r--r--   0        0        0     3622 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/cb7654d57bca_added_systems_table_and_host_info_user_.py
+-rw-r--r--   0        0        0    11177 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/ce05198f524a_convert_char_n_to_text.py
+-rw-r--r--   0        0        0      562 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/cea0e48abb5a_added_retention_policy_to_branch.py
+-rw-r--r--   0        0        0      461 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/d2b23f410d02_added_label_to_flow.py
+-rw-r--r--   0        0        0      714 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/d45087b62027_move_trigger_data_to_flow.py
+-rw-r--r--   0        0        0     1542 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/d524cbcbf19c_added_users_and_users_session.py
+-rw-r--r--   0        0        0      530 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/dae910bd9587_added_repo_data_to_run.py
+-rw-r--r--   0        0        0      719 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/e0d8421619c2_removed_unique_constraint_agent_non_.py
+-rw-r--r--   0        0        0      814 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/e404f52562c2_added_unique_constraints_on_branch_name_.py
+-rw-r--r--   0        0        0     1638 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/f566580fd139_added_test_case_comment_table.py
+-rw-r--r--   0        0        0      476 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/migrations/versions/ff4a425a6070_added_last_seen_to_executor.py
+-rw-r--r--   0        0        0      582 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/__init__.py
+-rw-r--r--   0        0        0    12197 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/access.py
+-rw-r--r--   0        0        0     2919 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/agentblob.py
+-rw-r--r--   0        0        0    10192 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/authn.py
+-rw-r--r--   0        0        0    32566 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/backend.py
+-rw-r--r--   0        0        0     4378 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/badge.py
+-rw-r--r--   0        0        0        0 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/bg/__init__.py
+-rw-r--r--   0        0        0    44857 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/bg/jobs.py
+-rw-r--r--   0        0        0     6287 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/chops.py
+-rw-r--r--   0        0        0        0 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/cloud/__init__.py
+-rw-r--r--   0        0        0     2003 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/cloud/aws.py
+-rw-r--r--   0        0        0     9147 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/cloud/aws_ec2.py
+-rw-r--r--   0        0        0     7191 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/cloud/aws_ecs.py
+-rw-r--r--   0        0        0    17629 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/cloud/azure.py
+-rw-r--r--   0        0        0     3244 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/cloud/cloud.py
+-rw-r--r--   0        0        0     1892 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/cloud/common.py
+-rw-r--r--   0        0        0     9421 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/cloud/k8s.py
+-rw-r--r--   0        0        0        0 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/config.py
+-rw-r--r--   0        0        0     5336 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/consts.py
+-rw-r--r--   0        0        0     3772 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/datastore.py
+-rw-r--r--   0        0        0     1687 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/dbutils.py
+-rw-r--r--   0        0        0    18341 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/exec_utils.py
+-rw-r--r--   0        0        0    21211 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/execution.py
+-rw-r--r--   0        0        0     9981 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/gitops.py
+-rw-r--r--   0        0        0    27015 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/initdb.py
+-rw-r--r--   0        0        0     5460 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/job_log.py
+-rw-r--r--   0        0        0     4489 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/kkrq.py
+-rw-r--r--   0        0        0    14059 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/logs.py
+-rw-r--r--   0        0        0    46016 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/management.py
+-rw-r--r--   0        0        0     4435 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/minioops.py
+-rw-r--r--   0        0        0    47775 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/models.py
+-rw-r--r--   0        0        0    10039 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/notify.py
+-rwxr-xr-x   0        0        0     6478 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/planner.py
+-rw-r--r--   0        0        0     1248 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/pljobs.py
+-rw-r--r--   0        0        0     4440 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/qneck.py
+-rw-r--r--   0        0        0    11643 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/results.py
+-rwxr-xr-x   0        0        0     5724 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/scheduler.py
+-rw-r--r--   0        0        0    16235 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/schema.py
+-rw-r--r--   0        0        0    31297 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/schemaval.py
+-rwxr-xr-x   0        0        0     7508 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/server.py
+-rw-r--r--   0        0        0     2010 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/srvcheck.py
+-rw-r--r--   0        0        0     3908 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/storage.py
+-rw-r--r--   0        0        0    83344 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/swagger.yml
+-rw-r--r--   0        0        0     2222 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/toolops.py
+-rw-r--r--   0        0        0     3197 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/toolutils.py
+-rw-r--r--   0        0        0    10872 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/users.py
+-rw-r--r--   0        0        0     1032 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/utils.py
+-rw-r--r--   0        0        0    19687 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/watchdog.py
+-rw-r--r--   0        0        0    12005 2023-07-22 13:18:10.000000 krakenci_server-1.3.25/kraken/server/webhooks.py
+-rw-r--r--   0        0        0       19 2023-07-22 13:19:52.789933 krakenci_server-1.3.25/kraken/version.py
+-rw-r--r--   0        0        0     2609 2023-07-22 13:19:53.714193 krakenci_server-1.3.25/pyproject.tml
+-rw-r--r--   0        0        0     5341 1970-01-01 00:00:00.000000 krakenci_server-1.3.25/setup.py
+-rw-r--r--   0        0        0     5658 1970-01-01 00:00:00.000000 krakenci_server-1.3.25/PKG-INFO
```

### Comparing `krakenci_server-1.2.2/README.md` & `krakenci_server-1.3.25/README.md`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/alembic.ini` & `krakenci_server-1.3.25/kraken/migrations/alembic.ini`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/apply.py` & `krakenci_server-1.3.25/kraken/migrations/apply.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/env.py` & `krakenci_server-1.3.25/kraken/migrations/env.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/050fbc3d126c_added_deployment_to_agents_group.py` & `krakenci_server-1.3.25/kraken/migrations/versions/050fbc3d126c_added_deployment_to_agents_group.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/0615faca43b1_added_url_tag_and_tool_file_to_tool.py` & `krakenci_server-1.3.25/kraken/migrations/versions/0615faca43b1_added_url_tag_and_tool_file_to_tool.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/19396769e240_added_extra_atrs_to_agents_group.py` & `krakenci_server-1.3.25/kraken/migrations/versions/19396769e240_added_extra_atrs_to_agents_group.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/1cf31ab18f84_create_secret_table.py` & `krakenci_server-1.3.25/kraken/migrations/versions/1cf31ab18f84_create_secret_table.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/1f5039135dd8_removed_enabled_from_projects.py` & `krakenci_server-1.3.25/kraken/migrations/versions/1f5039135dd8_removed_enabled_from_projects.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/26c6d691e7ce_added_last_flows_to_branch.py` & `krakenci_server-1.3.25/kraken/migrations/versions/26c6d691e7ce_added_last_flows_to_branch.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/2996b1b6e227_user_is_session_nullable.py` & `krakenci_server-1.3.25/kraken/migrations/versions/2996b1b6e227_user_is_session_nullable.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/29b96da53f09_added_reason_to_run.py` & `krakenci_server-1.3.25/kraken/migrations/versions/29b96da53f09_added_reason_to_run.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/2b5751b83fec_added_artifacts_to_flow.py` & `krakenci_server-1.3.25/kraken/migrations/versions/2b5751b83fec_added_artifacts_to_flow.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/2dd5cf2d12dc_added_new_repo_fields_to_stage.py` & `krakenci_server-1.3.25/kraken/migrations/versions/2dd5cf2d12dc_added_new_repo_fields_to_stage.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/3c1af14e0370_added_timeouts_to_stage_and_job.py` & `krakenci_server-1.3.25/kraken/migrations/versions/3c1af14e0370_added_timeouts_to_stage_and_job.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/411094f6b709_added_details_to_user.py` & `krakenci_server-1.3.25/kraken/migrations/versions/411094f6b709_added_details_to_user.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/42ea01a6cf31_convert_timestamps_to_with_timezones.py` & `krakenci_server-1.3.25/kraken/migrations/versions/42ea01a6cf31_convert_timestamps_to_with_timezones.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/4a7ac9143bb1_added_branch_sequences.py` & `krakenci_server-1.3.25/kraken/migrations/versions/4a7ac9143bb1_added_branch_sequences.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/5b13b262b132_added_repo_changes.py` & `krakenci_server-1.3.25/kraken/migrations/versions/5b13b262b132_added_repo_changes.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/5c16623f4d55_added_fields_masked_to_step.py` & `krakenci_server-1.3.25/kraken/migrations/versions/5c16623f4d55_added_fields_masked_to_step.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/5e38f55beb11_added_summary_to_flow.py` & `krakenci_server-1.3.25/kraken/migrations/versions/5e38f55beb11_added_summary_to_flow.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/6745adaf40e5_added_schema_repo_to_stage.py` & `krakenci_server-1.3.25/kraken/migrations/versions/6745adaf40e5_added_schema_repo_to_stage.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/735e81eedae4_change_project_id_in_executorgroup_to_.py` & `krakenci_server-1.3.25/kraken/migrations/versions/735e81eedae4_change_project_id_in_executorgroup_to_.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/818e190ca142_move_webhook_to_project.py` & `krakenci_server-1.3.25/kraken/migrations/versions/818e190ca142_move_webhook_to_project.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/8200318b9e18_added_several_stats_fields_to_run.py` & `krakenci_server-1.3.25/kraken/migrations/versions/8200318b9e18_added_several_stats_fields_to_run.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/87358b464400_added_casbin_rules_table.py` & `krakenci_server-1.3.25/kraken/migrations/versions/87358b464400_added_casbin_rules_table.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/899dadc28f9c_added_missing_indexes.py` & `krakenci_server-1.3.25/kraken/migrations/versions/899dadc28f9c_added_missing_indexes.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/89ffd52f1f00_rename_executor_to_agent.py` & `krakenci_server-1.3.25/kraken/migrations/versions/89ffd52f1f00_rename_executor_to_agent.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/9666bf8c1bb0_added_details_to_user_session.py` & `krakenci_server-1.3.25/kraken/migrations/versions/9666bf8c1bb0_added_details_to_user_session.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/98af95844f27_added_results_change_stats_to_run.py` & `krakenci_server-1.3.25/kraken/migrations/versions/98af95844f27_added_results_change_stats_to_run.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/a0741baf2dbc_added_indexes_to_test_case_results.py` & `krakenci_server-1.3.25/kraken/migrations/versions/a0741baf2dbc_added_indexes_to_test_case_results.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/a26a02d0ac01_added_extra_atrs_to_agents.py` & `krakenci_server-1.3.25/kraken/migrations/versions/a26a02d0ac01_added_extra_atrs_to_agents.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/a35aec7afa0a_added_processed_at_in_run_and_index_to_.py` & `krakenci_server-1.3.25/kraken/migrations/versions/a35aec7afa0a_added_processed_at_in_run_and_index_to_.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/ab9326d5fc02_added_index_to_flows.py` & `krakenci_server-1.3.25/kraken/migrations/versions/ab9326d5fc02_added_index_to_flows.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/af348b43d9d5_extended_tool.py` & `krakenci_server-1.3.25/kraken/migrations/versions/af348b43d9d5_extended_tool.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/b2c9024746f5_added_unique_constraint_for_system_name_.py` & `krakenci_server-1.3.25/kraken/migrations/versions/b2c9024746f5_added_unique_constraint_for_system_name_.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/b510fae321ba_added_seq_to_flow_and_run.py` & `krakenci_server-1.3.25/kraken/migrations/versions/b510fae321ba_added_seq_to_flow_and_run.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/b5cc62f79980_add_extra_to_issue.py` & `krakenci_server-1.3.25/kraken/migrations/versions/b5cc62f79980_add_extra_to_issue.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/b84bdc5d3c67_uniqued_agent_address.py` & `krakenci_server-1.3.25/kraken/migrations/versions/b84bdc5d3c67_uniqued_agent_address.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/b908e219f07f_longer_message_in_issue.py` & `krakenci_server-1.3.25/kraken/migrations/versions/b908e219f07f_longer_message_in_issue.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/bb0d4908ba49_added_artifact_and_file.py` & `krakenci_server-1.3.25/kraken/migrations/versions/bb0d4908ba49_added_artifact_and_file.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/bdcdbb4b5b3f_added_user_data_to_several_entities.py` & `krakenci_server-1.3.25/kraken/migrations/versions/bdcdbb4b5b3f_added_user_data_to_several_entities.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/befa07ac5d1c_changed_tool_version_to_string.py` & `krakenci_server-1.3.25/kraken/migrations/versions/befa07ac5d1c_changed_tool_version_to_string.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/cb7654d57bca_added_systems_table_and_host_info_user_.py` & `krakenci_server-1.3.25/kraken/migrations/versions/cb7654d57bca_added_systems_table_and_host_info_user_.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/ce05198f524a_convert_char_n_to_text.py` & `krakenci_server-1.3.25/kraken/migrations/versions/ce05198f524a_convert_char_n_to_text.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/cea0e48abb5a_added_retention_policy_to_branch.py` & `krakenci_server-1.3.25/kraken/migrations/versions/cea0e48abb5a_added_retention_policy_to_branch.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/d45087b62027_move_trigger_data_to_flow.py` & `krakenci_server-1.3.25/kraken/migrations/versions/d45087b62027_move_trigger_data_to_flow.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/d524cbcbf19c_added_users_and_users_session.py` & `krakenci_server-1.3.25/kraken/migrations/versions/d524cbcbf19c_added_users_and_users_session.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/dae910bd9587_added_repo_data_to_run.py` & `krakenci_server-1.3.25/kraken/migrations/versions/dae910bd9587_added_repo_data_to_run.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/e0d8421619c2_removed_unique_constraint_agent_non_.py` & `krakenci_server-1.3.25/kraken/migrations/versions/e0d8421619c2_removed_unique_constraint_agent_non_.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/e404f52562c2_added_unique_constraints_on_branch_name_.py` & `krakenci_server-1.3.25/kraken/migrations/versions/e404f52562c2_added_unique_constraints_on_branch_name_.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/migrations/versions/f566580fd139_added_test_case_comment_table.py` & `krakenci_server-1.3.25/kraken/migrations/versions/f566580fd139_added_test_case_comment_table.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/__init__.py` & `krakenci_server-1.3.25/kraken/server/__init__.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/access.py` & `krakenci_server-1.3.25/kraken/server/access.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/agentblob.py` & `krakenci_server-1.3.25/kraken/server/agentblob.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/authn.py` & `krakenci_server-1.3.25/kraken/server/authn.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/backend.py` & `krakenci_server-1.3.25/kraken/server/watchdog.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,671 +1,583 @@
-# Copyright 2020-2021 The Kraken Authors
+#!/usr/bin/env python3
+
+# Copyright 2020 The Kraken Authors
 #
 # Licensed under the Apache License, Version 2.0 (the "License");
 # you may not use this file except in compliance with the License.
 # You may obtain a copy of the License at
 #
 #     http://www.apache.org/licenses/LICENSE-2.0
 #
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 import os
-import json
 import time
 import logging
+import datetime
 
-from flask import request
-from sqlalchemy import or_
-from sqlalchemy.orm import joinedload
-from sqlalchemy.orm.attributes import flag_modified
-from sqlalchemy.exc import IntegrityError
-from psycopg2.errors import UniqueViolation  # pylint: disable=no-name-in-module
-import giturlparse
-
-from .models import db, Job, Step, Agent, TestCase, TestCaseResult, Issue, Secret, Artifact, File
-from .models import System
-from . import consts
+from flask import Flask
+from sqlalchemy.sql.expression import asc, desc, cast, or_
+from sqlalchemy import Integer, func
+import redis
+
+from . import logs
+from .models import db, Agent, AgentsGroup, Run, Job, get_setting
+from .models import Branch
 from .bg import jobs as bg_jobs
-from . import minioops
+from .cloud import cloud
+from . import consts
+from . import srvcheck
 from .. import version
+from . import exec_utils
 from . import kkrq
 from . import utils
 from . import dbutils
-from . import datastore
+from . import chops
 
-log = logging.getLogger(__name__)
+log = logging.getLogger('watchdog')
 
-JOB = {
-    "name": "build-tarball",
-    "id": 123,
-    "steps": [{
-        "tool": "git",
-        "checkout": "git@gitlab.isc.org:isc-projects/kea.git",
-        "branch": "master"
-    }, {
-        "tool": "shell",
-        "cmd": "cd kea && autoreconf -fi && ./configure && make dist"
-    }, {
-        "tool": "artifacts",
-        "type": "file",
-        "upload": "aaa-{ver}.tar.gz"
-    }]
-}
 
+def create_app():
+    # addresses
+    db_url = os.environ.get('KRAKEN_DB_URL', consts.DEFAULT_DB_URL)
+    planner_url = os.environ.get('KRAKEN_PLANNER_URL', consts.DEFAULT_PLANNER_URL)
 
-def _left_time(job):
-    now = utils.utcnow()
-    slip = now - job.assigned
-    timeout = job.timeout
-    timeout2 = timeout - slip.total_seconds()
-    # reduce slightly timeout
-    timeout3 = timeout2 * 0.9
-    log.info('%s-%s-%s: now: %s, slip:%s, to1: %s, to2: %s, to3: %s',
-             job.name, job.system.id, job.agents_group_id,
-             now, slip, timeout, timeout2, timeout3)
-    return int(timeout3)
-
-
-def _handle_get_job(agent):
-    if agent.job is None:
-        return {'job': {}}
-
-    # handle canceling situation
-    if agent.job.state == consts.JOB_STATE_COMPLETED:
-        job = agent.job
-        agent.job = None
-        db.session.commit()
-        log.info("unassigned canceled job %s from %s", job, agent)
-        return {'job': {}}
+    srvcheck.check_postgresql(db_url)
+    srvcheck.wait_for_service('planner', planner_url, 7997)
 
-    job = agent.job.get_json()
+    logs.setup_logging('watchdog')
+    log.info('Kraken Watchdog started, version %s', version.version)
 
-    job['timeout'] = _left_time(agent.job)
+    # Create  Flask app instance
+    app = Flask('Kraken Watchdog')
 
-    # prepare test list for execution
-    tests = []
-    for tcr in agent.job.results:
-        tests.append(tcr.test_case.name)
-    if tests:
-        job['steps'][-1]['tests'] = tests
-
-    # attach trigger data to job
-    if agent.job.run.flow.trigger_data:
-        job['trigger_data'] = agent.job.run.flow.trigger_data.data
-    elif agent.job.run.repo_data_id:
-        # pick any repo for now (TODO: it should be more sophisticated and handle all repos)
-        url = agent.job.run.repo_data.data[0]['repo']
-        commits = agent.job.run.repo_data.data[0]['commits']
-        job['trigger_data'] = [dict(repo=url,
-                                    after=commits[0]['id'])]
-
-    # attach storage info to job
-    job['branch_id'] = agent.job.run.flow.branch_id
-    job['flow_kind'] = agent.job.run.flow.kind
-    job['flow_id'] = agent.job.run.flow_id
-    job['run_id'] = agent.job.run_id
-
-    minio_bucket = minioops.get_or_create_minio_bucket_for_artifacts(agent.job.run.flow.branch_id)
-    minio_addr, minio_access_key, minio_secret_key = minioops.get_minio_addr()
-
-    # prepare steps
-    project = agent.job.run.flow.branch.project
-    for step in job['steps']:
-        add_minio = False
-
-        # insert secret from ssh-key
-        if 'ssh-key' in step:
-            value = step['ssh-key']
-            secret = Secret.query.filter_by(project=project, name=value, deleted=None).one_or_none()
-            if secret is None:
-                raise Exception("Secret '%s' does not exist in project %s" % (value, project.id))
-            step['ssh-key'] = dict(username=secret.data['username'],
-                                   key=secret.data['key'])
-
-        # insert secret from access-token
-        if 'access-token' in step:
-            value = step['access-token']
-            secret = Secret.query.filter_by(project=project, name=value).one_or_none()
-            if secret is None:
-                raise Exception("Secret '%s' does not exist in project %s" % (value, project.id))
-            step['access-token'] = secret.data['secret']
-
-        # custom fields for GIT
-        if step['tool'] == 'git':
-            # add http url to git
-            url = step['checkout']
-            url = giturlparse.parse(url)
-            if url.valid:
-                url = url.url2https
-                step['http_url'] = url
-            else:
-                log.info('invalid git url %s', step['checkout'])
+    # Configure the SqlAlchemy part of the app instance
+    app.config["SQLALCHEMY_ECHO"] = False
+    app.config["SQLALCHEMY_DATABASE_URI"] = db_url + '?application_name=watchdog'
+    app.config["SQLALCHEMY_TRACK_MODIFICATIONS"] = False
 
-            # add minio info for storing git repo bundle
-            add_minio = True
-            bucket, folder = minioops.get_or_create_minio_bucket_for_git(step['checkout'], branch_id=agent.job.run.flow.branch_id)
-            step['minio_bucket'] = bucket
-            step['minio_folder'] = folder
-
-        # custom fields for ARTIFACTS
-        if step['tool'] == 'artifacts':
-            add_minio = True
-            step['minio_bucket'] = minio_bucket
-            if 'destination' not in step:
-                step['destination'] = '.'
-
-        # custom fields for CACHE
-        if step['tool'] == 'cache':
-            add_minio = True
-            bucket, folders = minioops.get_or_create_minio_bucket_for_cache(agent.job, step)
-            step['minio_bucket'] = bucket
-            if step['action'] == 'save':
-                step['minio_folder'] = folders
-            else:
-                step['minio_folders'] = folders
+    # initialize SqlAlchemy
+    db.init_app(app)
 
-        if step['tool_location'].startswith('minio:'):
-            add_minio = True
+    # setup sentry
+    with app.app_context():
+        sentry_url = get_setting('monitoring', 'sentry_dsn')
+        logs.setup_sentry(sentry_url)
 
-        # add minio details
-        if add_minio:
-            step['minio_addr'] = minio_addr
-            step['minio_access_key'] = minio_access_key
-            step['minio_secret_key'] = minio_secret_key
-
-    if not agent.job.started:
-        agent.job.started = utils.utcnow()
-        agent.job.state = consts.JOB_STATE_ASSIGNED
-        db.session.commit()
+    return app
 
-    # prepare secrets
-    secrets = dbutils.get_secret_values(agent.job.run.flow.branch.project)
-    job['secrets'] = secrets
 
-    return {'job': job}
+def _exc_handler_with_db_rollback(fnc):
+    def inner_function(*args, **kwargs):
+        try:
+            return fnc(*args, **kwargs)
+        except Exception:
+            log.exception('IGNORED EXCEPTION')
+            db.session.rollback()
+            time.sleep(10)
+        return None
+    return inner_function
 
 
-def _store_results(job, step, result):
-    t0 = time.time()
-    q = TestCaseResult.query.filter_by(job=job)
-    q = q.options(joinedload('test_case'))
-    q = q.join('test_case')
-    or_list = []
-    results = {}
-    for tr in result['test-results']:
-        or_list.append(TestCase.name == tr['test'])
-        results[tr['test']] = tr
-        log.info('looking for existing results for TC: %s', tr)
-    q = q.filter(or_(*or_list))
-
-    # update status of existing test case results
-    cnt = 0
-    for tcr in q.all():
-        log.info('updating result for %s', tcr.test_case.name)
-        if tcr.test_case.name not in results:
-            log.warning('MISSING result')
-            continue
-        tr = results.pop(tcr.test_case.name)
-        tcr.cmd_line = tr['cmd']
-        tcr.result = tr['status']
-        tcr.values = tr['values'] if 'values' in tr else None
-        cnt += 1
-    db.session.commit()
-    t1 = time.time()
-    log.info('reporting %s existing test records took %ss', cnt, (t1 - t0))
+@_exc_handler_with_db_rollback
+def _check_jobs_if_expired():
+    now = utils.utcnow()
 
-    # create test case results if they didnt exist
-    tool_test_cases = {}
-    q = TestCase.query.filter_by(tool=step.tool)
-    for tc in q.all():
-        tool_test_cases[tc.name] = tc
-    for tc_name, tr in results.items():
-        tc = tool_test_cases.get(tc_name, None)
-        if tc is None:
-            tc = TestCase(name=tc_name, tool=step.tool)
-        TestCaseResult(test_case=tc, job=step.job,
-                       cmd_line=tr['cmd'],
-                       result=tr['status'],
-                       values=tr['values'] if 'values' in tr else None)
-    db.session.commit()
-    t2 = time.time()
-    log.info('reporting %s new test records took %ss', len(results), (t2 - t1))
+    q = Job.query.filter_by(state=consts.JOB_STATE_ASSIGNED)
 
+    job_count = 0
+    canceled_count = 0
 
-def _store_issues(job, result):
-    t0 = time.time()
-    for issue in result['issues']:
-        issue_type = 0
-        if issue['type'] in consts.ISSUE_TYPES_CODE:
-            issue_type = consts.ISSUE_TYPES_CODE[issue['type']]
-        else:
-            log.warning('unknown issue type: %s', issue['type'])
-        extra = {}
-        for k, v in issue.items():
-            if k not in ['line', 'column', 'path', 'symbol', 'message']:
-                extra[k] = v
-        Issue(issue_type=issue_type, line=issue['line'], column=issue['column'], path=issue['path'], symbol=issue['symbol'],
-              message=issue['message'][:511], extra=extra, job=job)
-    db.session.commit()
-    t1 = time.time()
-    log.info('reporting %s issues took %ss', len(result['issues']), (t1 - t0))
+    for job in q.all():
+        log.set_ctx(branch=job.run.flow.branch_id, flow_kind=job.run.flow.kind, flow=job.run.flow_id, run=job.run.id, job=job.id)
 
+        job_count += 1
+        if not job.assigned:
+            log.warning('job %s assigned but no assign time', job)
+            log.reset_ctx()
+            continue
 
-def _store_artifacts(job, step):
-    t0 = time.time()
-    flow = job.run.flow
-    if not flow.artifacts:
-        flow.artifacts = dict(public=dict(size=0, count=0, entries=[]),
-                              private=dict(size=0, count=0))
-    if not flow.artifacts_files:
-        flow.artifacts_files = []
-
-    run = job.run
-    if not run.artifacts:
-        run.artifacts = dict(public=dict(size=0, count=0, entries=[]),
-                             private=dict(size=0, count=0))
-    if not run.artifacts_files:
-        run.artifacts_files = []
-
-    public = step.fields.get('public', False)
-    report_entry = step.fields.get('report_entry', None)
-    if report_entry:
-        public = True
-        flow.artifacts['public']['entries'].append(report_entry)
-        run.artifacts['public']['entries'].append(report_entry)
-
-    if public:
-        section = 'public'
-        section_id = consts.ARTIFACTS_SECTION_PUBLIC
-    else:
-        section = 'private'
-        section_id = consts.ARTIFACTS_SECTION_PRIVATE
+        timeout = job.timeout if job.timeout else consts.DEFAULT_JOB_TIMEOUT
+        duration = now - job.assigned
+        if duration > datetime.timedelta(seconds=timeout):
+            log.warning('time %ss for job %s expired, canceling', timeout, job)
+            note = 'job expired after %ss' % timeout
+            exec_utils.cancel_job(job, note, consts.JOB_CMPLT_SERVER_TIMEOUT)
+            canceled_count += 1
+
+        log.reset_ctx()
+
+    if job_count > 0:
+        log.info('canceled jobs:%d / all:%d', canceled_count, job_count)
+
+
+@_exc_handler_with_db_rollback
+def _check_jobs_if_missing_agents():
+    groups_jobs = {}  # keep here groups that are needed and one, any job
+
+    q = Job.query.filter_by(covered=False, deleted=None, state=consts.JOB_STATE_QUEUED)
+    for job in q.all():
+        ag = job.agents_group
+        if (ag.deployment and
+            ag.deployment['method'] in [consts.AGENT_DEPLOYMENT_METHOD_AWS_EC2,
+                                        consts.AGENT_DEPLOYMENT_METHOD_AWS_ECS_FARGATE,
+                                        consts.AGENT_DEPLOYMENT_METHOD_AZURE_VM,
+                                        consts.AGENT_DEPLOYMENT_METHOD_K8S,
+                                        ]):
+            groups_jobs[ag.id] = job.id
+
+    for ag_id in groups_jobs:
+        kkrq.enq_neck(bg_jobs.spawn_new_agents, ag_id)
+    if groups_jobs:
+        n = len(groups_jobs)
+        grps = list(groups_jobs.keys())[:5]
+        job = groups_jobs.popitem()[1]
+        log.info('enqueued spawning new agents for %d groups eg:%s with no agents but with waiting jobs, eg: %s',
+                 n, grps, job)
+
+
+def _check_jobs():
+    _check_jobs_if_expired()
+    _check_jobs_if_missing_agents()
 
-    for artifact in step.result['artifacts']:
-        flow.artifacts[section]['size'] += artifact['size']
-        flow.artifacts[section]['count'] += 1
-
-        run.artifacts[section]['size'] += artifact['size']
-        run.artifacts[section]['count'] += 1
-
-        if section == 'public':
-            report_entry = artifact.get('report_entry', None)
-            if report_entry:
-                flow.artifacts['public']['entries'].append(report_entry)
-                run.artifacts['public']['entries'].append(report_entry)
-
-        path = artifact['path']
-        f = File.query.filter_by(path=path).one_or_none()
-        if f is None:
-            f = File(path=path)
-        Artifact(file=f, flow=flow, run=run, size=artifact['size'], section=section_id)
 
-    flag_modified(flow, 'artifacts')
-    flag_modified(run, 'artifacts')
-    db.session.commit()
+@_exc_handler_with_db_rollback
+def _check_runs_timeout():
+    now = utils.utcnow()
 
-    t1 = time.time()
-    log.info('reporting %s artifacts took %ss', len(step.result['artifacts']), (t1 - t0))
+    q = Run.query.filter_by(finished=None)
+    q = q.filter(Run.state != consts.RUN_STATE_MANUAL)  # TODO: manual runs will require timeouting as well when jobs are started
 
+    for run in q.all():
+        timeout = run.stage.schema.get('timeout', consts.DEFAULT_RUN_TIMEOUT)
+        if run.started:
+            begin = run.started
+        else:
+            begin = run.created
+        end_time = begin + datetime.timedelta(seconds=timeout)
+        if end_time > now:
+            # no timeout yet
+            continue
 
-def _handle_data(job, step, result):
-    data = result['data']
-    return datastore.handle_data(job, step, data)
+        log.set_ctx(branch=run.flow.branch_id, flow_kind=run.flow.kind, flow=run.flow_id, run=run.id)
 
+        note = 'run %s timed out, deadline was: %s' % (run, str(end_time))
+        log.info(note)
+        run.note = note
 
-def _destroy_machine_if_needed(agent, job):
-    to_destroy = False
+        # cancel any pending jobs
+        canceled_jobs_count = 0
+        for job in run.jobs:
+            if job.state != consts.JOB_STATE_COMPLETED:
+                exec_utils.cancel_job(job, note, consts.JOB_CMPLT_SERVER_TIMEOUT)
+                canceled_jobs_count += 1
 
-    # check if cloud machine should be destroyed now
-    ag = dbutils.find_cloud_assignment_group(agent)
-    if ag:
-        # aws ec2
-        if ag.deployment['method'] == consts.AGENT_DEPLOYMENT_METHOD_AWS_EC2:
-            depl = ag.deployment['aws']
+        # if there is no pending jobs then complete run now
+        if canceled_jobs_count == 0:
+            exec_utils.complete_run(run, now)
 
-            if depl and 'destruction_after_jobs' in depl and int(depl['destruction_after_jobs']) > 0:
-                max_jobs = int(depl['destruction_after_jobs'])
-                q = Job.query.filter_by(agent_used=agent)
-                q = q.filter(Job.finished.isnot(None))
-                q = q.filter(Job.finished > agent.created)
-                jobs_num = q.count()
-                log.info('JOB %s, num %d, max %d', job, jobs_num, max_jobs)
-                if jobs_num >= max_jobs:
-                    to_destroy = True
-
-        # aws ecs fargate
-        elif ag.deployment['method'] == consts.AGENT_DEPLOYMENT_METHOD_AWS_ECS_FARGATE:
-            log.info('ECS FARGATE JOB %s - destroying task: %d', job, agent.id)
-            to_destroy = True
+        log.reset_ctx()
 
-        # azure vm
-        elif ag.deployment['method'] == consts.AGENT_DEPLOYMENT_METHOD_AZURE_VM:
-            depl = ag.deployment['azure_vm']
 
-            if depl and 'destruction_after_jobs' in depl and int(depl['destruction_after_jobs']) > 0:
-                max_jobs = int(depl['destruction_after_jobs'])
-                q = Job.query.filter_by(agent_used=agent)
-                q = q.filter(Job.finished.isnot(None))
-                q = q.filter(Job.finished > agent.created)
-                jobs_num = q.count()
-                log.info('JOB %s, num %d, max %d', job, jobs_num, max_jobs)
-                if jobs_num >= max_jobs:
-                    to_destroy = True
+@_exc_handler_with_db_rollback
+def _check_runs_missing_history_analysis():
+    now = utils.utcnow()
+    three_months = now - datetime.timedelta(days=90)
+    twenty_mins = now - datetime.timedelta(minutes=20)
 
-        # kubernetes
-        elif ag.deployment['method'] == consts.AGENT_DEPLOYMENT_METHOD_K8S:
-            log.info('K8S JOB %s - destroying pod: %d', job, agent.id)
-            to_destroy = True
+    q = Run.query.filter(Run.finished > three_months)
+    q = q.filter(Run.finished < twenty_mins)
+    q = q.filter(Run.state != consts.RUN_STATE_PROCESSED)
+    q = q.order_by(asc(Run.finished))
+
+    visited_branches = set()
+    for run in q.all():
+        if run.flow.branch_id in visited_branches:
+            continue
 
-    # schedule destruction if needed
-    if to_destroy:
-        agent.disabled = True
-        kkrq.enq(bg_jobs.destroy_machine, agent.id)
+        log.set_ctx(branch=run.flow.branch_id, flow_kind=run.flow.kind, flow=run.flow_id, run=run.id)
 
+        log.info('run with missing history %s', run)
+        visited_branches.add(run.flow.branch_id)
+        kkrq.enq_neck(bg_jobs.analyze_results_history, run.id)
 
-def _handle_step_result(agent, req):
-    response = {}
-    if agent.job is None:
-        log.error('job in agent %s is missing, reporting some old job %s, step %s',
-                  agent, req['job_id'], req['step_idx'])
-        return response
-
-    if agent.job_id != req['job_id']:
-        log.error('agent %s is reporting some other job %s',
-                  agent, req['job_id'])
-        return response
+        log.reset_ctx()
 
-    log.set_ctx(job=agent.job_id)
 
-    try:
-        result = req['result']
-        step_idx = req['step_idx']
-        status = result['status']
-        del result['status']
-        if status not in consts.STEP_STATUS_TO_INT:
-            log.set_ctx(job=None)
-            raise ValueError("unknown status: %s" % status)
-    except Exception:
-        log.exception('problems with parsing request')
-        log.set_ctx(job=None)
-        return response
+def _check_runs():
+    _check_runs_timeout()
+    _check_runs_missing_history_analysis()
 
-    job = agent.job
-    step = job.steps[step_idx]
-    step.result = result
-    step.status = consts.STEP_STATUS_TO_INT[status]
-
-    # handle canceling situation
-    if job.state == consts.JOB_STATE_COMPLETED:
-        agent.job = None
-        db.session.commit()
-        log.info("canceling job %s on %s", job, agent)
-        response['cancel'] = True
-        log.set_ctx(job=None)
-        return response
 
+def _cancel_job_and_unassign_agent(agent):
+    exec_utils.cancel_job(agent.job, 'agent not alive', consts.JOB_CMPLT_AGENT_NOT_ALIVE)
+    job = agent.job
+    agent.job = None
+    job.agent = None
     db.session.commit()
 
-    # store test results
-    if 'test-results' in result:
-        _store_results(job, step, result)
-
-    # store issues
-    if 'issues' in result:
-        _store_issues(job, result)
-
-    # store artifacts
-    if 'artifacts' in result:
-        _store_artifacts(job, step)
-
-    # set, update or get data
-    if 'data' in result:
-        _handle_data(job, step, result)
-
-    # check if all steps are done so job is finised
-    job_finished = True
-    log.info('checking steps')
-    for s in job.steps:
-        log.info('%s: %s', s.index, consts.STEP_STATUS_NAME[s.status]
-                 if s.status in consts.STEP_STATUS_NAME else s.status)
-        if s.status == consts.STEP_STATUS_DONE:
-            continue
-        if s.status == consts.STEP_STATUS_ERROR:
-            job_finished = True
-            break
-        job_finished = False
-        break
-    if job_finished:
-        job.state = consts.JOB_STATE_EXECUTING_FINISHED
-        job.finished = utils.utcnow()
-        agent.job = None
 
-        _destroy_machine_if_needed(agent, job)
+@_exc_handler_with_db_rollback
+def _check_agents_keep_alive():
+    now = utils.utcnow()
+    five_mins_ago = now - datetime.timedelta(seconds=consts.AGENT_TIMEOUT)
+    ten_mins_ago = now - datetime.timedelta(seconds=consts.SLOW_AGENT_TIMEOUT)
 
+    q = Agent.query
+    q = q.filter_by(disabled=False, deleted=None)
+    q = q.filter(Agent.last_seen < five_mins_ago)
+
+    for a in q.all():
+        log.reset_ctx()
+        log.set_ctx(agent=a.id)
+        # in case of cloud machines check for 10mins, not 5mins
+        ag = dbutils.find_cloud_assignment_group(a)
+        if (ag and
+            ag.deployment['method'] in [consts.AGENT_DEPLOYMENT_METHOD_AWS_EC2,
+                                        consts.AGENT_DEPLOYMENT_METHOD_AWS_ECS_FARGATE,
+                                        consts.AGENT_DEPLOYMENT_METHOD_AZURE_VM,
+                                        consts.AGENT_DEPLOYMENT_METHOD_K8S]):
+            if a.last_seen > ten_mins_ago:
+                continue
+
+        a.disabled = True
+        a.status_line = 'agent was not seen for last 5 minutes, disabled'
+        log.info('agent %s not seen for 5 minutes, disabled', a)
         db.session.commit()
-        kkrq.enq(bg_jobs.job_completed, job.id)
-        log.info('job %s finished by %s', job, agent)
-    else:
-        response['timeout'] = _left_time(job)
 
-    log.set_ctx(job=None)
-    return response
+        if a.job:
+            _cancel_job_and_unassign_agent(a)
 
 
-def _create_test_records(step, tests):
-    t0 = time.time()
-    tool_test_cases = {}
-    q = TestCase.query.filter_by(tool=step.tool)
-    for tc in q.all():
-        tool_test_cases[tc.name] = tc
-
-    for t in tests:
-        tc = tool_test_cases.get(t, None)
-        if tc is None:
-            tc = TestCase(name=t, tool=step.tool)
-        TestCaseResult(test_case=tc, job=step.job)
-    db.session.commit()
-    t1 = time.time()
-    log.info('creating %s test records took %ss', len(tests), (t1 - t0))
+def _destroy_and_delete_if_outdated(agent, depl, method):
+    destroy = False
 
+    if method == consts.AGENT_DEPLOYMENT_METHOD_K8S:
+        # if for some reason k8s pod still exists after completing the job
+        # then destroy it after 3 mins
+        destruction_after_time = 3
+    else:
+        if 'destruction_after_time' in depl:
+            destruction_after_time = int(depl['destruction_after_time'])
+        else:
+            destruction_after_time = 10  # default if somehow not set
 
-def _handle_dispatch_tests(agent, req):
-    if agent.job is None:
-        log.error('job in agent %s is missing, reporting some old job %s, step %s',
-                  agent, req['job_id'], req['step_idx'])
-        return {}
-
-    if agent.job_id != req['job_id']:
-        log.error('agent %s is reporting some other job %s',
-                  agent, req['job_id'])
-        return {}
+    # check if idle time after job passed, then destroy VM
+    if destruction_after_time > 0:
+        max_idle_time = datetime.timedelta(seconds=60 * destruction_after_time)
+
+        q = Job.query.filter_by(agent_used=agent)
+        q = q.filter(Job.finished.isnot(None))
+        q = q.filter(Job.finished > agent.created)
+        q = q.order_by(desc(Job.finished))
+        last_job = q.first()
+        now = utils.utcnow()
+        if last_job:
+            dt = now - last_job.finished
+            if dt >= max_idle_time:
+                log.info('agent: %s, timed out %s > %s - destroying it, last job %s',
+                         agent, dt, max_idle_time, last_job)
+                destroy = True
+            else:
+                log.info('agent: %s, not yet timed out %s < %s - skipped', agent, dt, max_idle_time)
+        elif now - agent.created >= max_idle_time:
+            log.info('agent: %s, timed out %s - destroying it, created at %s vs now %s', agent, max_idle_time, agent.created, now)
+            destroy = True
+        else:
+            log.info('agent: %s, no last job and not idle enough - skipped', agent)
+    else:
+        log.info('agent: %s, destruction_after_time is 0 - skipped', agent)
 
-    job = agent.job
+    # check if number of executed jobs on VM is reached, then destroy VM
+    if not destroy:
+        if 'destruction_after_jobs' in depl and int(depl['destruction_after_jobs']) > 0:
+            max_jobs = int(depl['destruction_after_jobs'])
+            q = Job.query.filter_by(agent_used=agent, state=consts.JOB_STATE_COMPLETED)
+            q = q.filter(Job.finished > agent.created)
+            jobs_num = q.count()
+            if jobs_num >= max_jobs:
+                log.info('agent: %s, max jobs reached %d/%d', agent, jobs_num, max_jobs)
+                # TODO: remove it later, for debugging only
+                #for j in q.all():
+                #    log.info('  job: %s', j)
+                destroy = True
+            else:
+                log.info('agent: %s, max jobs not reached yet %d/%d - skipped', agent, jobs_num, max_jobs)
+        else:
+            log.info('agent: %s, destruction_after_jobs is 0 - skipped', agent)
 
-    # handle canceling situation
-    if job.state == consts.JOB_STATE_COMPLETED:
-        agent.job = None
+    # if machine mark for destruction then schedule it
+    if destroy:
+        log.info('disabling and destroying machine with agent %s', agent)
+        agent.disabled = True
         db.session.commit()
-        log.info("canceling job %s on %s", job, agent)
-        return {'cancel': True}
-
-    try:
-        tests = req['tests']
-        step_idx = req['step_idx']
-        step = job.steps[step_idx]
-    except Exception:
-        log.exception('problems with parsing request')
-        return {}
-
-    tests_cnt = len(tests)
+        kkrq.enq(bg_jobs.destroy_machine, agent.id)
+        return True
 
-    if len(set(tests)) != tests_cnt:
-        log.warning('there are tests duplicates')
-        return {}
+    return False
 
-    if tests_cnt == 0:
-        # TODO
-        raise NotImplementedError
 
-    if tests_cnt == 1 or 'autosplit' not in step.fields or not step.fields['autosplit']:
-        _create_test_records(step, tests)
-        db.session.commit()
-        return {'tests': tests}
+def _delete_if_missing_in_cloud(ag, agent):
+    if not agent.extra_attrs or 'instance_id' not in agent.extra_attrs:
+        log.warning('agent:%d, no instance id in extra_attrs', agent.id)
+        return False
 
-    # simple dispatching: divide to 2 jobs, current and new one
-    part = tests_cnt // 2
-    part1 = tests[:part]
-    part2 = tests[part:]
+    exists = True
+    try:
+        exists = cloud.check_if_machine_exists(ag, agent)
+    except Exception:
+        pass
 
-    _create_test_records(step, part1)
-    db.session.commit()
+    if not exists:
+        dbutils.delete_agent(agent)
+        log.info('deleted dangling agent %s', agent)
+        return True
+
+    return False
+
+
+@_exc_handler_with_db_rollback
+def _check_agents_to_destroy():
+    # look for agents that are not deleted, still available for use ie. authorized
+    # and without currently running job
+    # that have some deployment method configured
+    q = Agent.query.filter_by(deleted=None, authorized=True, job=None)
+    q = q.join('agents_groups', 'agents_group')
+    q = q.filter(AgentsGroup.deployment.isnot(None))
+    # TODO ECS
+    q = q.filter(or_(cast(AgentsGroup.deployment['method'], Integer) == consts.AGENT_DEPLOYMENT_METHOD_AWS_EC2,
+                     cast(AgentsGroup.deployment['method'], Integer) == consts.AGENT_DEPLOYMENT_METHOD_AZURE_VM,
+                     cast(AgentsGroup.deployment['method'], Integer) == consts.AGENT_DEPLOYMENT_METHOD_K8S))
+
+    outdated_count = 0
+    dangling_count = 0
+    all_count = 0
+    for agent in q.all():
+        log.reset_ctx()
+        log.set_ctx(agent=agent.id)
 
-    # new timeout reduced by nearly a half
-    timeout = int(job.timeout * 0.6)
-    timeout = max(timeout, 60)
-
-    # create new job and its steps
-    job2 = Job(run=job.run, name=job.name, agents_group=job.agents_group, system=job.system, timeout=timeout)
-    for s in job.steps:
-        s2 = Step(job=job2, index=s.index, tool=s.tool, fields=s.fields.copy())
-        if s.index == step_idx:
-            _create_test_records(s2, part2)
-    db.session.commit()
+        all_count += 1
+        ag = dbutils.find_cloud_assignment_group(agent)
 
-    return {'tests': part1}
+        if not ag:
+            log.error('missing ag in agent %s', agent)
+            continue
 
+        if not ag.deployment:
+            log.error('missing deployment in ag %s', ag)
+            continue
 
-def _handle_host_info(agent, req):  # pylint: disable=unused-argument
-    log.info('HOST INFO %s', req['info'])
+        method = consts.AGENT_DEPLOYMENT_METHOD_MANUAL
+        try:
+            method, depl = ag.get_deployment()
+        except Exception:
+            pass
+        if method not in [consts.AGENT_DEPLOYMENT_METHOD_AWS_EC2,
+                          consts.AGENT_DEPLOYMENT_METHOD_AZURE_VM,
+                          consts.AGENT_DEPLOYMENT_METHOD_K8S]:
+            log.error('unsupported deployment method %s', ag.deployment['method'])
+            continue
+        deleted = _destroy_and_delete_if_outdated(agent, depl, method)
+        if deleted:
+            outdated_count += 1
+            if agent.job:
+                _cancel_job_and_unassign_agent(agent)
+            continue
 
-    system = req['info']['system']
+        deleted = _delete_if_missing_in_cloud(ag, agent)
+        if deleted:
+            dangling_count += 1
+            if agent.job:
+                _cancel_job_and_unassign_agent(agent)
+            continue
 
-    sys = None
-    if system.isdigit():
-        # agent has already identified system so find its name
-        sys_id = int(system)
-        sys = System.query.filter_by(id=sys_id).one_or_none()
-        if sys is not None:
-            # if this is real system id then substitute it
-            req['info']['system'] = sys.name
+    log.reset_ctx()
 
-    agent.host_info = req['info']
-    db.session.commit()
+    if outdated_count > 0:
+        log.info('all agents:%d, destroyed and deleted %d VM instances and agents',
+                 all_count, outdated_count)
+    if dangling_count > 0:
+        log.info('deleted %d dangling agents without any VM instance', dangling_count)
+
+    return all_count, outdated_count, dangling_count
+
+
+@_exc_handler_with_db_rollback
+def _check_machines_with_no_agent():
+    # look for AWS EC2 or Azure VM machines that do not have agents in database
+    # and destroy such machines
+    q = AgentsGroup.query
+    q = q.filter_by(deleted=None)
+    q = q.filter(AgentsGroup.deployment.isnot(None))
+
+    all_groups = 0
+    aws_ec2_groups = 0
+    azure_vm_groups = 0
+    k8s_groups = 0
 
-    resp = dict(agent_id=agent.id)
+    for ag in q.all():
+        all_groups += 1
 
-    if sys:
-        # agent has already identified system so it doesn't need to be created
-        return resp
+        if ag.deployment['method'] == consts.AGENT_DEPLOYMENT_METHOD_AWS_EC2:
+            aws_ec2_groups += 1
+        elif ag.deployment['method'] == consts.AGENT_DEPLOYMENT_METHOD_AZURE_VM:
+            azure_vm_groups += 1
+        elif ag.deployment['method'] == consts.AGENT_DEPLOYMENT_METHOD_K8S:
+            k8s_groups += 1
+        else:
+            continue
 
-    try:
-        System(name=system, executor='local')
-        db.session.commit()
-    except IntegrityError as e:
-        if not isinstance(e.orig, UniqueViolation):
-            log.exception('IGNORED')
+        counts = cloud.cleanup_dangling_machines(ag)
 
-    return resp
+        instances = counts[0]
+        terminated_instances = counts[1]
+        assigned_instances = counts[2]
+        orphaned_instances = counts[3]
+        orphaned_terminated_instances = counts[4]
+
+        if (instances + terminated_instances + assigned_instances +
+            orphaned_instances + orphaned_terminated_instances > 0):
+            log.info('group: %s, instances:%d, already-terminated:%d, still-assigned:%d, orphaned:%d, terminated-orphaned:%d',
+                     ag,
+                     instances,
+                     terminated_instances,
+                     assigned_instances,
+                     orphaned_instances,
+                     orphaned_terminated_instances)
+    if aws_ec2_groups + azure_vm_groups + k8s_groups > 0:
+        log.info('machines with no agent by groups: aws:%d, azure vm:%d, k8s:%d / all:%d',
+                 aws_ec2_groups, azure_vm_groups, k8s_groups, all_groups)
+
+
+@_exc_handler_with_db_rollback
+def _check_agents_counts():
+    q = db.session.query(Agent.authorized, func.count(Agent.authorized))
+    q = q.filter_by(deleted=None)
+    q = q.group_by(Agent.authorized)
+    counts = q.all()
+
+    redis_addr = os.environ.get('KRAKEN_REDIS_ADDR', consts.DEFAULT_REDIS_ADDR)
+    redis_host, redis_port = utils.split_host_port(redis_addr, 6379)
+    rds = redis.Redis(host=redis_host, port=redis_port, db=consts.REDIS_KRAKEN_DB)
+
+    for authorized, cnt in counts:
+        if authorized:
+            rds.set('authorized-agents', cnt)
+        else:
+            rds.set('non-authorized-agents', cnt)
 
 
-def _handle_keep_alive(agent, req):  # pylint: disable=unused-argument
-    job = agent.job
+def _check_agents():
+    _check_agents_keep_alive()
+    _check_agents_to_destroy()
+    _check_machines_with_no_agent()
+    _check_agents_counts()
 
-    # handle canceling situation
-    if job and job.state == consts.JOB_STATE_COMPLETED:
-        agent.job = None
-        db.session.commit()
-        log.info("canceling job %s on %s", job, agent)
-        return {'cancel': True}
 
-    return {}
+@_exc_handler_with_db_rollback
+def _check_for_errors_in_logs():
+    ch = chops.get_clickhouse()
 
+    now = utils.utcnow()
+    start_date = now - datetime.timedelta(hours=1)
 
-def _handle_unknown_agent(address, ip_address, agent):
-    try:
-        new = False
-        if agent:
-            now = utils.utcnow()
-            if agent.deleted:
-                log.info('undeleting agent %s with address %s', agent, address)
-                agent.deleted = None
-                agent.created = now
-            agent.authorized = False
-            agent.ip_address = ip_address
-            agent.last_seen = now
-        else:
-            agent = Agent(name=address, address=address, authorized=False, ip_address=ip_address, last_seen=utils.utcnow())
-            new = True
-        db.session.commit()
-        if new:
-            log.info('created new agent instance %s for address %s', agent, address)
-    except Exception as e:
-        log.warning('IGNORED EXCEPTION: %s', str(e))
+    query = "select count(*) from logs where level = 'ERROR' and time > %(start_date)s;"
+    rows = ch.execute(query, {'start_date': start_date})
+    errors_count = rows[0][0]
 
+    redis_addr = os.environ.get('KRAKEN_REDIS_ADDR', consts.DEFAULT_REDIS_ADDR)
+    redis_host, redis_port = utils.split_host_port(redis_addr, 6379)
+    rds = redis.Redis(host=redis_host, port=redis_port, db=consts.REDIS_KRAKEN_DB)
 
-def _serve_agent_request():
-    log.reset_ctx()
-    req = request.get_json()
-    # log.info('request headers: %s', request.headers)
-    # log.info('request remote_addr: %s', request.remote_addr)
-    # log.info('request args: %s', request.args)
-    log.info('request data: %s', str(req)[:200])
-
-    msg = req['msg']
-    address = req['address']
-    if address is None:
-        address = request.remote_addr
-    # log.info('agent address: %s', address)
-
-    agent = Agent.query.filter_by(address=address).one_or_none()
-    if agent is None or agent.deleted:
-        log.warning('unknown agent %s', address)
-        _handle_unknown_agent(address, request.remote_addr, agent)
-        return json.dumps({'unauthorized': True})
+    rds.set('error-logs-count', errors_count)
+    #log.info('updated errors count to %s', errors_count)
 
-    agent.last_seen = utils.utcnow()
-    db.session.commit()
 
-    if not agent.authorized:
-        log.warning('unauthorized agent %s from %s', address, request.remote_addr)
-        return json.dumps({'unauthorized': True})
+@_exc_handler_with_db_rollback
+def _run_branch_retention_policy():
+    log.info('branches logs retention')
+    ch = chops.get_clickhouse()
 
-    response = {}
+    q = Branch.query
+    q = q.filter_by(deleted=None)
 
-    if msg == consts.AGENT_MSG_GET_JOB:
-        response = _handle_get_job(agent)
+    for branch in q.all():
+        log.reset_ctx()
+        log.set_ctx(branch=branch.id)
 
-        clickhouse_addr = os.environ.get('KRAKEN_CLICKHOUSE_ADDR', consts.DEFAULT_CLICKHOUSE_ADDR)
-        response['cfg'] = dict(clickhouse_addr=clickhouse_addr)
-        response['version'] = version.version
+        if branch.retention_policy:
+            rp = branch.retention_policy
+            months = [rp['ci_logs'], rp['dev_logs']]
+        else:
+            months = [6, 3]
 
-    elif msg == consts.AGENT_MSG_STEP_RESULT:
-        response = _handle_step_result(agent, req)
+        for flow_kind in [0, 1]:
+            query = "ALTER TABLE logs DELETE WHERE branch = %(branch_id)s AND flow_kind = %(flow_kind)s AND time < (now() - toIntervalMonth(%(months)s))"
+            params = dict(branch_id=branch.id,
+                          flow_kind=flow_kind,
+                          months=months[flow_kind])
+            resp = ch.execute(query, params)
+            log.info('deleted logs %s', resp)
+            # TODO: trace number of deleted logs
 
-    elif msg == consts.AGENT_MSG_DISPATCH_TESTS:
-        response = _handle_dispatch_tests(agent, req)
+    log.reset_ctx()
 
-    elif msg == consts.AGENT_MSG_HOST_INFO:
-        response = _handle_host_info(agent, req)
 
-    elif msg == consts.AGENT_MSG_KEEP_ALIVE:
-        response = _handle_keep_alive(agent, req)
+def _main_loop():
+    t0 = time.time()
+    t0_log_errs = t0_jobs = t0_runs = t0_agents = t0
+    t0_branch_retention_policy = t0
 
-    else:
-        log.warning('unknown msg: %s', msg)
-        response = {}
 
-    log.info('sending response: %s', str(response)[:200])
-    return json.dumps(response)
+    while True:
+        # check jobs every 5 seconds
+        dt = time.time() - t0_jobs
+        if dt > 5:
+            _check_jobs()
+            t0_jobs = time.time()
+
+        # check for error in logs every 15 seconds
+        dt = time.time() - t0_log_errs
+        if dt > 15:
+            _check_for_errors_in_logs()
+            t0_log_errs = time.time()
+
+        # check runs every 30 seconds
+        dt = time.time() - t0_runs
+        if dt > 30:
+            _check_runs()
+            t0_runs = time.time()
+
+        # check agents every 30 seconds
+        dt = time.time() - t0_agents
+        if dt > 30:
+            _check_agents()
+            t0_agents = time.time()
+
+        # run retention policy every 24 h
+        dt = time.time() - t0_branch_retention_policy
+        if dt > 60 * 60 * 24:
+            _run_branch_retention_policy()
+            t0_branch_retention_policy = time.time()
+
+        time.sleep(1)
+
+def main():
+    app = create_app()
+
+    with app.app_context():
+        while True:
+            try:
+                _main_loop()
+            except Exception:
+                log.exception('IGNORED EXCEPTION')
+                db.session.rollback()
+                time.sleep(10)
 
 
-def serve_agent_request():
-    try:
-        return _serve_agent_request()
-    except Exception:
-        db.session.rollback()
-        db.session.close()
-        raise
+if __name__ == "__main__":
+    main()
```

### Comparing `krakenci_server-1.2.2/kraken/server/badge.py` & `krakenci_server-1.3.25/kraken/server/badge.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/bg/jobs.py` & `krakenci_server-1.3.25/kraken/server/bg/jobs.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/chops.py` & `krakenci_server-1.3.25/kraken/server/chops.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/cloud/aws.py` & `krakenci_server-1.3.25/kraken/server/cloud/aws.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/cloud/aws_ec2.py` & `krakenci_server-1.3.25/kraken/server/cloud/aws_ec2.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/cloud/aws_ecs.py` & `krakenci_server-1.3.25/kraken/server/cloud/aws_ecs.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/cloud/azure.py` & `krakenci_server-1.3.25/kraken/server/cloud/azure.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/cloud/cloud.py` & `krakenci_server-1.3.25/kraken/server/cloud/cloud.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/cloud/common.py` & `krakenci_server-1.3.25/kraken/server/cloud/common.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/cloud/k8s.py` & `krakenci_server-1.3.25/kraken/server/cloud/k8s.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/consts.py` & `krakenci_server-1.3.25/kraken/server/consts.py`

 * *Files 5% similar despite different names*

```diff
@@ -42,26 +42,29 @@
 JOB_CMPLT_NO_AGENTS = 10
 JOB_CMPLT_AGENT_NOT_ALIVE = 11
 
 STEP_STATUS_NOT_STARTED = 0
 STEP_STATUS_IN_PROGRES = 1
 STEP_STATUS_DONE = 2
 STEP_STATUS_ERROR = 3
+STEP_STATUS_SKIPPED = 4
 
 STEP_STATUS_TO_INT = {
     'not-started': STEP_STATUS_NOT_STARTED,
     'in-progress': STEP_STATUS_IN_PROGRES,
     'done': STEP_STATUS_DONE,
-    'error': STEP_STATUS_ERROR
+    'error': STEP_STATUS_ERROR,
+    'skipped': STEP_STATUS_SKIPPED
 }
 STEP_STATUS_NAME = {
     STEP_STATUS_NOT_STARTED: 'not-started',
     STEP_STATUS_IN_PROGRES: 'in-progress',
     STEP_STATUS_DONE: 'done',
-    STEP_STATUS_ERROR: 'error'
+    STEP_STATUS_ERROR: 'error',
+    STEP_STATUS_SKIPPED: 'skipped',
 }
 
 TC_RESULT_NOT_RUN = 0
 TC_RESULT_PASSED = 1
 TC_RESULT_FAILED = 2
 TC_RESULT_ERROR = 3
 TC_RESULT_DISABLED = 4
@@ -167,15 +170,18 @@
 ARTIFACTS_SECTION_PUBLIC = 1
 
 
 AGENT_DIR = '/opt/kraken'
 
 
 AGENT_MSG_GET_JOB = 'get-job'
+AGENT_MSG_GET_JOB2 = 'get-job2'
+AGENT_MSG_GET_JOB_STEP = 'get-job-step'
 AGENT_MSG_STEP_RESULT = 'step-result'
+AGENT_MSG_STEP_RESULT2 = 'step-result2'
 AGENT_MSG_DISPATCH_TESTS = 'dispatch-tests'
 AGENT_MSG_HOST_INFO = 'host-info'
 AGENT_MSG_KEEP_ALIVE = 'keep-alive'
 
 
 BRANCH_SEQ_FLOW = 0
 BRANCH_SEQ_CI_FLOW = 1
```

### Comparing `krakenci_server-1.2.2/kraken/server/datastore.py` & `krakenci_server-1.3.25/kraken/server/datastore.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/dbutils.py` & `krakenci_server-1.3.25/kraken/server/dbutils.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/exec_utils.py` & `krakenci_server-1.3.25/kraken/server/exec_utils.py`

 * *Files 3% similar despite different names*

```diff
@@ -294,17 +294,14 @@
 
         schema = run.stage.schema
 
         # find any prev jobs that will be covered by jobs triggered here in this function
         if replay:
             covered_jobs = _find_covered_jobs(run)
 
-        # prepare secrets to pass them to substitute in steps
-        secrets = prepare_secrets(run)
-
         # prepare missing group
         missing_agents_group = AgentsGroup.query.filter_by(name='missing').one_or_none()
         if missing_agents_group is None:
             missing_agents_group = AgentsGroup(name='missing')
             db.session.commit()
 
         # count how many agents are in each group, if there is 0 for given job then return an error
@@ -407,34 +404,29 @@
                             job.notes = "there are no agents in group '%s' - add some agents" % agents_group.name
                         erred_job = True
 
                     if not erred_job:
                         all_started_erred = False
                         # substitute vars in steps
                         for idx, s in enumerate(j['steps']):
-                            args = secrets.copy()
-                            if run.args:
-                                args.update(run.args)
-                            step = Step(job=job, index=idx, tool=tools[idx], fields={}, fields_masked={})
-                            step_ctx = prepare_context(step, args)
-                            fields, fields_masked = substitute_vars(s, args, step_ctx)
-                            del fields['tool']
-                            step.fields = fields
-                            step.fields_masked = fields_masked
+                            step = Step(job=job, index=idx, tool=tools[idx], fields={}, fields_masked={}, fields_raw=s)
+                            evaluate_step_fields(step)
 
                     # if this is rerun/replay then mark prev jobs as covered
                     if replay:
                         key = '%s-%s' % (j['name'], agents_group.id)
                         if key in covered_jobs:
                             for cj in covered_jobs[key]:
                                 cj.covered = True
                                 # TODO: we should cancel these jobs if they are still running
 
                     db.session.commit()
+                    log.set_ctx(job=job.id)
                     log.info('created job %s', job.get_json(mask_secrets=True))
+                    log.set_ctx(job=None)
 
     except Exception as ex:
         log.exception('Problem with starting jobs')
         now = utils.utcnow()
         run.started = now
         run.note = "Triggering run's jobs failed: %s" % str(ex)
         complete_run(run, now)
@@ -454,7 +446,28 @@
 
     # notify
     kkrq.enq(bg_jobs.notify_about_started_run, run.id)
     log.info('enqueued notification about start of run %s', run)
 
     if len(schema['jobs']) == 0 or all_started_erred:
         complete_run(run, now)
+
+
+def evaluate_step_fields(step):
+    run = step.job.run
+    # prepare secrets to pass them to substitute in steps
+    secrets = prepare_secrets(run)
+    args = secrets.copy()
+    if run.args:
+        args.update(run.args)
+    step_ctx = prepare_context(step, args)
+    if 'when' in step.fields_raw:
+        if not step.fields_raw['when'].startswith('#{'):
+            step.fields_raw['when'] = '#{' + step.fields_raw['when'] + '}'
+    else:
+        step.fields_raw['when'] = '#{was_no_error}'
+    flag_modified(step, 'fields_raw')
+    fields, fields_masked = substitute_vars(step.fields_raw, args, step_ctx)
+    del fields['tool']
+    step.fields = fields
+    step.fields_masked = fields_masked
+    db.session.commit()
```

### Comparing `krakenci_server-1.2.2/kraken/server/execution.py` & `krakenci_server-1.3.25/kraken/server/execution.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/gitops.py` & `krakenci_server-1.3.25/kraken/server/gitops.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/initdb.py` & `krakenci_server-1.3.25/kraken/server/initdb.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/job_log.py` & `krakenci_server-1.3.25/kraken/server/job_log.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/kkrq.py` & `krakenci_server-1.3.25/kraken/server/kkrq.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/logs.py` & `krakenci_server-1.3.25/kraken/server/logs.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/management.py` & `krakenci_server-1.3.25/kraken/server/management.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/minioops.py` & `krakenci_server-1.3.25/kraken/server/minioops.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/models.py` & `krakenci_server-1.3.25/kraken/server/models.py`

 * *Files 0% similar despite different names*

```diff
@@ -559,14 +559,15 @@
     job = relationship("Job", back_populates="steps")
     tool_id = Column(Integer, ForeignKey('tools.id'), nullable=False)
     tool = relationship("Tool", back_populates="steps")
     fields = Column(JSONB, nullable=False)
     result = Column(JSONB)
     status = Column(Integer)
     fields_masked = Column(JSONB, nullable=True)
+    fields_raw = Column(JSONB, nullable=True)
     # services
 
     def get_json(self, with_fields=True, mask_secrets=False):
         data = dict(id=self.id,
                     index=self.index,
                     tool=self.tool.name,
                     tool_id=self.tool_id,
@@ -576,16 +577,18 @@
                     job_id=self.job_id,
                     status=self.status,
                     result=self.result)
 
         if with_fields:
             if mask_secrets and self.fields_masked:
                 fields = self.fields_masked
-            else:
+            elif self.fields:
                 fields = self.fields
+            else:
+                fields = self.fields_raw
 
             name = self.tool.name
             if 'name' in fields:
                 name = fields['name']
             elif self.tool.name == 'shell':
                 if 'script' in fields and fields['script']:
                     name = fields['script'].strip().splitlines()[0] + '...'
```

### Comparing `krakenci_server-1.2.2/kraken/server/notify.py` & `krakenci_server-1.3.25/kraken/server/notify.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/planner.py` & `krakenci_server-1.3.25/kraken/server/planner.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/pljobs.py` & `krakenci_server-1.3.25/kraken/server/pljobs.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/qneck.py` & `krakenci_server-1.3.25/kraken/server/qneck.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/results.py` & `krakenci_server-1.3.25/kraken/server/results.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/scheduler.py` & `krakenci_server-1.3.25/kraken/server/scheduler.py`

 * *Files 2% similar despite different names*

```diff
@@ -66,15 +66,15 @@
 
 
 def _assign_jobs(agents_count, idle_agents_by_group, idle_agents_by_sys_group,
                  waiting_jobs):
     counter = 0
 
     for j in waiting_jobs:
-        log.set_ctx(branch=j.run.flow.branch_id, flow_kind=j.run.flow.kind, flow=j.run.flow_id, run=j.run.id)
+        log.set_ctx(branch=j.run.flow.branch_id, flow_kind=j.run.flow.kind, flow=j.run.flow_id, run=j.run.id, job=j.id)
         log.info('job %s, executor %s', j, j.system.executor)
 
         # system does not have to be taken into account when user selects ANY system
         # or when executor is not local eg. it is a docker container
         if j.system.name == 'any' or j.system.executor != 'local':
             idle_agents = idle_agents_by_group.get(j.agents_group_id, [])
         else:
```

### Comparing `krakenci_server-1.2.2/kraken/server/schema.py` & `krakenci_server-1.3.25/kraken/server/schema.py`

 * *Files 7% similar despite different names*

```diff
@@ -219,19 +219,23 @@
                 val_masked = val_masked.replace(var, '******')
                 secret_present = True
             else:
                 val_masked = val_masked.replace(var, arg_val)
 
     # new way of exposing context in fields
     env = SandboxedEnvironment()
-    for var in re.findall(r'#{[A-Za-z0-9_\. ]+}', val):
+    for var in re.findall(r'#{[A-Za-z0-9_\. \[\]<>=\-\+/\*|^()]+}', val):
         expr = var[2:-1].strip()
 
-        tpl = env.from_string("{{ %s }}" % expr)
-        new_str = tpl.render(**ctx)
+        try:
+            tpl = env.from_string("{{ %s }}" % expr)
+            new_str = tpl.render(**ctx)
+        except Exception:
+            log.exception('IGNORED')
+            new_str = '<ERROR>'
         val = val.replace(var, new_str)
 
         if expr.startswith('secrets.'):
             secret_present = True
             val_masked = val_masked.replace(var, '******')
         else:
             val_masked = val_masked.replace(var, new_str)
@@ -301,17 +305,39 @@
         ctx['run'] = run.get_json(with_project=False, with_branch=False, with_artifacts=False, with_counts=False)
         ctx['is_ci'] = run.flow.kind == consts.FLOW_KIND_CI
         ctx['is_dev'] = run.flow.kind == consts.FLOW_KIND_DEV
         ctx['run_label'] = run.label
         ctx['flow_label'] = run.flow.label
 
     if step:
-        ctx['job'] = step.job.get_json(with_steps=False)
+        ctx['job'] = step.job.get_json()
         ctx['step'] = step.get_json(with_fields=False)
 
+        if step.index == 0:
+            prev_ok = True
+        else:
+            prev_step = step.job.steps[step.index - 1]
+            prev_ok = prev_step.status in [consts.STEP_STATUS_DONE, consts.STEP_STATUS_SKIPPED]
+
+        was_any_error = False
+        was_no_error = True
+        for s in step.job.steps:
+            if s.index == step.index:
+                break
+            if s.status == consts.STEP_STATUS_ERROR:
+                was_any_error = True
+                was_no_error = False
+                break
+
+        ctx['prev_ok'] = prev_ok
+        ctx['always'] = True
+        ctx['never'] = False
+        ctx['was_any_error'] = was_any_error
+        ctx['was_no_error'] = was_no_error
+
     return ctx
 
 
 def prepare_new_planner_triggers(stage_id, new_triggers, prev_triggers, triggers):
     planner_url = os.environ.get('KRAKEN_PLANNER_URL', consts.DEFAULT_PLANNER_URL)
     planner = xmlrpc.client.ServerProxy(planner_url, allow_none=True)
```

### Comparing `krakenci_server-1.2.2/kraken/server/schemaval.py` & `krakenci_server-1.3.25/kraken/server/schemaval.py`

 * *Files 2% similar despite different names*

```diff
@@ -854,14 +854,15 @@
             tools.append((tool, name))
         else:
             name = '%s@%s' % (tool.name, tool.version)
             tools.append((tool, name))
 
     tools_schemas = {}
     for tool, name_ver in tools:
+        # common fields to all tools
         fields = {
             "tool": {
                 "description": tool.description,
                 "const": name_ver
             },
             "attempts": {
                 "description": "A number of times the step is retried if if it returns error.",
@@ -873,15 +874,20 @@
                 "default": 0,
                 "type": "integer"
             },
             "name": {
                 "description": "A name of the step, displayed in web UI.",
                 "default": "",
                 "type": "string"
-            }
+            },
+            "when": {
+                "description": "A condition when a step may be executed. Any Jinja2 expression can be used, e.g.: `'job.steps[step.index - 1].result.duration > 3'`. The following predefined values are available: `'prev_ok'`, `'always'`, `'never'`, `'was_any_error'`, `'was_no_error'`, `'is_ci'`, `'is_dev'`.",
+                "default": "was_no_error",
+                "type": "string"
+            },
         }
 
         if "properties" not in tool.fields:
             raise Exception("Schema of '%s' tool does not have 'properties' field." % name_ver)
 
         for fname, fdef in tool.fields["properties"].items():
             fields[fname] = fdef
```

### Comparing `krakenci_server-1.2.2/kraken/server/server.py` & `krakenci_server-1.3.25/kraken/server/server.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/srvcheck.py` & `krakenci_server-1.3.25/kraken/server/srvcheck.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/storage.py` & `krakenci_server-1.3.25/kraken/server/storage.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/swagger.yml` & `krakenci_server-1.3.25/kraken/server/swagger.yml`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/toolops.py` & `krakenci_server-1.3.25/kraken/server/toolops.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/toolutils.py` & `krakenci_server-1.3.25/kraken/server/toolutils.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/users.py` & `krakenci_server-1.3.25/kraken/server/users.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/utils.py` & `krakenci_server-1.3.25/kraken/server/utils.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/kraken/server/webhooks.py` & `krakenci_server-1.3.25/kraken/server/webhooks.py`

 * *Files identical despite different names*

### Comparing `krakenci_server-1.2.2/pyproject.tml` & `krakenci_server-1.3.25/pyproject.tml`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "krakenci-server"
-version="1.2.2"
+version="1.3.25"
 description = "Kraken CI server."
 authors = ["Michal Nowikowski <godfryd@gmail.com>"]
 readme = "README.md"
 homepage = "https://kraken.ci/"
 repository = "https://github.com/kraken-ci/kraken"
 documentation = "https://kraken.ci/docs"
 keywords = ["building", "testing", "continuous-integration", "ci", "cd", "cicd"]
@@ -21,15 +21,15 @@
 packages = [
   { include = "kraken" },
 ]
 
 include = ["kraken/version.py"]
 
 [tool.poetry.dependencies]
-python = "^3.7"
+python = "^3.8"
 connexion = "^2.14.2"
 MarkupSafe = "2.1.2"
 Flask = "^2.2.3"
 Flask-SQLAlchemy = "^3.0.3"
 psycopg2-binary = "^2.9.1"
 redis = "^3.5.3"
 requests = "^2.26.0"
@@ -38,15 +38,17 @@
 apscheduler = "^3.8.0"
 tzlocal = "2.1"  # this is required by apscheduler that still relies on pytz; aps 4.x will have this fixed and then this line can be removed
 pytimeparse = "^1.1.8"
 python-dateutil = "^2.8.2"
 gunicorn = "^20.1.0"
 RestrictedPython = "5.0"
 alembic = "^1.7.3"
-giturlparse = "^0.10.0"
+# giturlparse = "^0.10.0"
+# giturlparse = { git = "https://github.com/nephila/giturlparse.git", rev = "f65f609662edb5f21dc7ccf506f54b3ac888cc89" }
+giturlparse2 = "^1.0.0"
 clickhouse-driver = "^0.2.5"
 minio = "^7.1.0"
 passlib = "^1.7.4"
 sentry-sdk = {extras = ["flask"], version = "^1.5.0"}
 boto3 = "^1.18.52"
 jsonschema = "^4.5.0"
 rq = "^1.10.0"
@@ -69,14 +71,15 @@
 addict = "^2.4.0"
 
 [tool.poetry.dev-dependencies]
 pytest = "^7.1.2"
 pylint = "2.13.9"
 pudb = "^2021.1"
 PyHamcrest = "^2.0.3"
+pytest-cov = "^4.1.0"
 
 [tool.poetry.scripts]
 # kkserver = 'kraken.server.server:main' # this does not work due to flask problems
 kkscheduler = 'kraken.server.scheduler:main'
 kkplanner = 'kraken.server.planner:main'
 kkwatchdog = 'kraken.server.watchdog:main'
 kkrq = 'kraken.server.kkrq:main'
```

### Comparing `krakenci_server-1.2.2/setup.py` & `krakenci_server-1.3.25/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -30,15 +30,15 @@
  'azure-mgmt-storage>=18.0.0,<19.0.0',
  'azure-mgmt-subscription>=1.0.0,<2.0.0',
  'boto3>=1.18.52,<2.0.0',
  'casbin>=1.17.1,<2.0.0',
  'clickhouse-driver>=0.2.5,<0.3.0',
  'connexion>=2.14.2,<3.0.0',
  'furl>=2.1.3,<3.0.0',
- 'giturlparse>=0.10.0,<0.11.0',
+ 'giturlparse2>=1.0.0,<2.0.0',
  'gunicorn>=20.1.0,<21.0.0',
  'jinja2>=3.1.2,<4.0.0',
  'jq>=1.4.0,<2.0.0',
  'jsonpatch>=1.32,<2.0',
  'jsonschema>=4.5.0,<5.0.0',
  'kubernetes>=20.13.0,<21.0.0',
  'minio>=7.1.0,<8.0.0',
@@ -61,24 +61,24 @@
                      'kkqneck = kraken.server.qneck:main',
                      'kkrq = kraken.server.kkrq:main',
                      'kkscheduler = kraken.server.scheduler:main',
                      'kkwatchdog = kraken.server.watchdog:main']}
 
 setup_kwargs = {
     'name': 'krakenci-server',
-    'version': '1.2.2',
+    'version': '1.3.25',
     'description': 'Kraken CI server.',
     'long_description': '# Kraken CI\n\n![Release Version](https://img.shields.io/github/v/release/Kraken-CI/kraken)\n![Release Date](https://img.shields.io/github/release-date/Kraken-CI/kraken)\n\n![Kraken Build](https://lab.kraken.ci/bk/branch-badge/2)\n![Kraken Tests](https://lab.kraken.ci/bk/branch-badge/2/tests)\n![Kraken Issues](https://lab.kraken.ci/bk/branch-badge/2/issues)\n\n[![Codacy Badge](https://app.codacy.com/project/badge/Grade/be770bd29e374ece9e6f2782a1de99fc)](https://www.codacy.com/gh/Kraken-CI/kraken/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Kraken-CI/kraken&amp;utm_campaign=Badge_Grade)\n[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/Kraken-CI/kraken.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/Kraken-CI/kraken/context:python)\n[![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/Kraken-CI/kraken.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/Kraken-CI/kraken/context:javascript)\n[![Total alerts](https://img.shields.io/lgtm/alerts/g/Kraken-CI/kraken.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/Kraken-CI/kraken/alerts/)\n[![codebeat badge](https://codebeat.co/badges/556ac028-2390-4093-839e-a509f5678cf1)](https://codebeat.co/projects/github-com-kraken-ci-kraken-master)\n\n[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/4758/badge)](https://bestpractices.coreinfrastructure.org/projects/4758)\n[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/kraken-ci)](https://artifacthub.io/packages/search?repo=kraken-ci)\n\n\n<!-- ABOUT THE PROJECT -->\n## About Kraken CI\n\n![Kraken CI Results Page](https://kraken.ci/img/slide-branch-results.png)\n\nKraken CI is a modern, open-source, on-premise CI/CD system\nthat is highly scalable and focused on testing.\n\nMore information can be found on https://kraken.ci\n\n\n<!-- GETTING STARTED -->\n## Getting Started\n\nQuick start guide is here: https://kraken.ci/docs/quick-start\n\nFull installation manual: https://kraken.ci/docs/installation\n\nAnd here is developers guide: https://kraken.ci/docs/dev-guide\n\n\n<!-- USAGE EXAMPLES -->\n## Usage\n\nGuides can be found here: https://kraken.ci/docs/guide-intro\n\nDemo site is available here: https://lab.kraken.ci/\n\n\n<!-- ROADMAP -->\n## Roadmap\n\nSee the [open issues](https://github.com/kraken-ci/kraken/issues) for a list of proposed features (and known issues).\n\n\n<!-- CONTRIBUTING -->\n## Contributing\n\nContributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.\n\nDetails on https://kraken.ci/docs/contrib-kraken\n\n\n<!-- LICENSE -->\n## License\n\nDistributed under the Apache 2.0 License. See `LICENSE` for more information.\n\n\n<!-- CONTACT -->\n## Contact\n\nMichal Nowikowski - godfryd@gmail.com\n\nProject Link: [https://kraken.ci](https://kraken.ci)\n',
     'author': 'Michal Nowikowski',
     'author_email': 'godfryd@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://kraken.ci/',
     'packages': packages,
     'package_data': package_data,
     'install_requires': install_requires,
     'entry_points': entry_points,
-    'python_requires': '>=3.7,<4.0',
+    'python_requires': '>=3.8,<4.0',
 }
 
 
 setup(**setup_kwargs)
```

### Comparing `krakenci_server-1.2.2/PKG-INFO` & `krakenci_server-1.3.25/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,20 +1,19 @@
 Metadata-Version: 2.1
 Name: krakenci-server
-Version: 1.2.2
+Version: 1.3.25
 Summary: Kraken CI server.
 Home-page: https://kraken.ci/
 License: Apache-2.0
 Keywords: building,testing,continuous-integration,ci,cd,cicd
 Author: Michal Nowikowski
 Author-email: godfryd@gmail.com
-Requires-Python: >=3.7,<4.0
+Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Software Development
 Classifier: Topic :: Software Development :: Build Tools
 Classifier: Topic :: Software Development :: Quality Assurance
@@ -36,15 +35,15 @@
 Requires-Dist: azure-mgmt-storage (>=18.0.0,<19.0.0)
 Requires-Dist: azure-mgmt-subscription (>=1.0.0,<2.0.0)
 Requires-Dist: boto3 (>=1.18.52,<2.0.0)
 Requires-Dist: casbin (>=1.17.1,<2.0.0)
 Requires-Dist: clickhouse-driver (>=0.2.5,<0.3.0)
 Requires-Dist: connexion (>=2.14.2,<3.0.0)
 Requires-Dist: furl (>=2.1.3,<3.0.0)
-Requires-Dist: giturlparse (>=0.10.0,<0.11.0)
+Requires-Dist: giturlparse2 (>=1.0.0,<2.0.0)
 Requires-Dist: gunicorn (>=20.1.0,<21.0.0)
 Requires-Dist: jinja2 (>=3.1.2,<4.0.0)
 Requires-Dist: jq (>=1.4.0,<2.0.0)
 Requires-Dist: jsonpatch (>=1.32,<2.0)
 Requires-Dist: jsonschema (>=4.5.0,<5.0.0)
 Requires-Dist: kubernetes (>=20.13.0,<21.0.0)
 Requires-Dist: minio (>=7.1.0,<8.0.0)
```

