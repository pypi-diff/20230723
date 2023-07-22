# Comparing `tmp/skyplane_nightly-0.3.2.dev20230720.tar.gz` & `tmp/skyplane_nightly-0.3.2.dev20230721.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "skyplane_nightly-0.3.2.dev20230720.tar", max compression
+gzip compressed data, was "skyplane_nightly-0.3.2.dev20230721.tar", max compression
```

## Comparing `skyplane_nightly-0.3.2.dev20230720.tar` & `skyplane_nightly-0.3.2.dev20230721.tar`

### file list

```diff
@@ -1,100 +1,100 @@
--rw-r--r--   0        0        0    11357 2023-07-20 23:44:03.795193 skyplane_nightly-0.3.2.dev20230720/LICENSE
--rw-r--r--   0        0        0     7221 2023-07-20 23:44:03.795193 skyplane_nightly-0.3.2.dev20230720/README.md
--rw-r--r--   0        0        0     3669 2023-07-20 23:44:51.964616 skyplane_nightly-0.3.2.dev20230720/pyproject.toml
--rw-r--r--   0        0        0      649 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/__init__.py
--rw-r--r--   0        0        0     4331 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/api/client.py
--rw-r--r--   0        0        0     3040 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/api/config.py
--rw-r--r--   0        0        0    14841 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/api/dataplane.py
--rw-r--r--   0        0        0     2081 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/api/obj_store.py
--rw-r--r--   0        0        0     7117 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/api/pipeline.py
--rw-r--r--   0        0        0    15091 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/api/provisioner.py
--rw-r--r--   0        0        0    17597 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/api/tracker.py
--rw-r--r--   0        0        0    38945 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/api/transfer_job.py
--rw-r--r--   0        0        0    14790 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/api/usage.py
--rw-r--r--   0        0        0     6120 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/chunk.py
--rw-r--r--   0        0        0     3317 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli.py
--rw-r--r--   0        0        0    18045 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli_cloud.py
--rw-r--r--   0        0        0     1678 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli_config.py
--rw-r--r--   0        0        0    27030 2023-07-20 23:44:03.807193 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli_init.py
--rw-r--r--   0        0        0    24587 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli_transfer.py
--rw-r--r--   0        0        0      461 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/experiments/__init__.py
--rw-r--r--   0        0        0    23462 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/experiments/cli_profile.py
--rw-r--r--   0        0        0     1757 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/experiments/cli_query.py
--rw-r--r--   0        0        0     9215 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/experiments/provision.py
--rw-r--r--   0        0        0     3100 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/impl/common.py
--rw-r--r--   0        0        0     4678 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/impl/cp_replicate_fallback.py
--rw-r--r--   0        0        0     3071 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/cli/impl/progress_bar.py
--rw-r--r--   0        0        0     1247 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/__init__.py
--rw-r--r--   0        0        0     5908 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_auth.py
--rw-r--r--   0        0        0    11591 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_cloud_provider.py
--rw-r--r--   0        0        0     4315 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_key_manager.py
--rw-r--r--   0        0        0    11509 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_network.py
--rw-r--r--   0        0        0     1606 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_pricing.py
--rw-r--r--   0        0        0     6294 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_server.py
--rw-r--r--   0        0        0     9526 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/azure/azure_auth.py
--rw-r--r--   0        0        0    20681 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/azure/azure_cloud_provider.py
--rw-r--r--   0        0        0     7503 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/azure/azure_server.py
--rw-r--r--   0        0        0     3564 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/cloud_provider.py
--rw-r--r--   0        0        0     2883 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/const_cmds.py
--rw-r--r--   0        0        0    12043 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_auth.py
--rw-r--r--   0        0        0     9355 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_cloud_provider.py
--rw-r--r--   0        0        0     2462 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_key_manager.py
--rw-r--r--   0        0        0     6288 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_network.py
--rw-r--r--   0        0        0     2786 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_pricing.py
--rw-r--r--   0        0        0     5151 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_server.py
--rw-r--r--   0        0        0      211 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_credentials.yaml.template
--rw-r--r--   0        0        0        0 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/__init__.py
--rw-r--r--   0        0        0     2242 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/config.py
--rw-r--r--   0        0        0      877 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/constants.py
--rw-r--r--   0        0        0     5353 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/ssh_client.py
--rw-r--r--   0        0        0      710 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/utils.py
--rw-r--r--   0        0        0    40464 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/vpc_backend.py
--rw-r--r--   0        0        0     5320 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibmcloud_auth.py
--rw-r--r--   0        0        0     2851 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibmcloud_provider.py
--rw-r--r--   0        0        0     3522 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibmcloud_server.py
--rw-r--r--   0        0        0      937 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/key_utils.py
--rw-r--r--   0        0        0    17426 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/compute/server.py
--rw-r--r--   0        0        0    13473 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/config.py
--rw-r--r--   0        0        0     1229 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/config_paths.py
--rw-r--r--   0        0        0        0 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/data/__init__.py
--rw-r--r--   0        0        0    19636 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/data/aws_transfer_costs.csv
--rw-r--r--   0        0        0      617 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/data/vcpu_info.csv
--rw-r--r--   0        0        0     3078 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/exceptions.py
--rw-r--r--   0        0        0      811 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/cert.py
--rw-r--r--   0        0        0     4349 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/chunk_store.py
--rw-r--r--   0        0        0    15655 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_daemon.py
--rw-r--r--   0        0        0    16570 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_daemon_api.py
--rw-r--r--   0        0        0      718 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_onprem.py
--rw-r--r--   0        0        0     5149 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_program.py
--rw-r--r--   0        0        0     1732 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_queue.py
--rw-r--r--   0        0        0        0 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/operators/__init__.py
--rw-r--r--   0        0        0    25487 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/operators/gateway_operator.py
--rw-r--r--   0        0        0    10552 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/operators/gateway_receiver.py
--rw-r--r--   0        0        0       37 2023-07-20 23:44:51.960616 skyplane_nightly-0.3.2.dev20230720/skyplane/gateway_version.py
--rw-r--r--   0        0        0    13101 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/azure_blob_interface.py
--rw-r--r--   0        0        0     2887 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/azure_storage_account_interface.py
--rw-r--r--   0        0        0    10871 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/cos_interface.py
--rw-r--r--   0        0        0     2010 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/file_system_interface.py
--rw-r--r--   0        0        0    12754 2023-07-20 23:44:03.811194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/gcs_interface.py
--rw-r--r--   0        0        0     5963 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/hdfs_interface.py
--rw-r--r--   0        0        0     3287 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/object_store_interface.py
--rw-r--r--   0        0        0     5644 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/posix_file_interface.py
--rw-r--r--   0        0        0     3606 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/r2_interface.py
--rw-r--r--   0        0        0    11595 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/s3_interface.py
--rw-r--r--   0        0        0     2569 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/storage_interface.py
--rw-r--r--   0        0        0    23858 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/planner/planner.py
--rw-r--r--   0        0        0    18157 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/planner/solver.py
--rw-r--r--   0        0        0     6467 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/planner/solver_ilp.py
--rw-r--r--   0        0        0     1996 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/planner/solver_ron.py
--rw-r--r--   0        0        0     7920 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/planner/topology.py
--rw-r--r--   0        0        0      846 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/cache.py
--rw-r--r--   0        0        0      617 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/definitions.py
--rw-r--r--   0        0        0     2494 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/fn.py
--rw-r--r--   0        0        0     1881 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/generator.py
--rw-r--r--   0        0        0     1386 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/imports.py
--rw-r--r--   0        0        0     2131 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/logger.py
--rw-r--r--   0        0        0     1447 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/networking_tools.py
--rw-r--r--   0        0        0     3162 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/path.py
--rw-r--r--   0        0        0     1160 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/retry.py
--rw-r--r--   0        0        0      612 2023-07-20 23:44:03.815194 skyplane_nightly-0.3.2.dev20230720/skyplane/utils/timer.py
--rw-r--r--   0        0        0    10493 1970-01-01 00:00:00.000000 skyplane_nightly-0.3.2.dev20230720/PKG-INFO
+-rw-r--r--   0        0        0    11357 2023-07-21 23:44:20.348726 skyplane_nightly-0.3.2.dev20230721/LICENSE
+-rw-r--r--   0        0        0     7468 2023-07-21 23:44:20.348726 skyplane_nightly-0.3.2.dev20230721/README.md
+-rw-r--r--   0        0        0     3669 2023-07-21 23:45:07.108894 skyplane_nightly-0.3.2.dev20230721/pyproject.toml
+-rw-r--r--   0        0        0      649 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/__init__.py
+-rw-r--r--   0        0        0     4331 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/api/client.py
+-rw-r--r--   0        0        0     3040 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/api/config.py
+-rw-r--r--   0        0        0    14841 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/api/dataplane.py
+-rw-r--r--   0        0        0     2081 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/api/obj_store.py
+-rw-r--r--   0        0        0     7117 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/api/pipeline.py
+-rw-r--r--   0        0        0    15091 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/api/provisioner.py
+-rw-r--r--   0        0        0    17597 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/api/tracker.py
+-rw-r--r--   0        0        0    38945 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/api/transfer_job.py
+-rw-r--r--   0        0        0    14790 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/api/usage.py
+-rw-r--r--   0        0        0     6120 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/chunk.py
+-rw-r--r--   0        0        0     3317 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli.py
+-rw-r--r--   0        0        0    18045 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli_cloud.py
+-rw-r--r--   0        0        0     1678 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli_config.py
+-rw-r--r--   0        0        0    27030 2023-07-21 23:44:20.364726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli_init.py
+-rw-r--r--   0        0        0    24587 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli_transfer.py
+-rw-r--r--   0        0        0      461 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/experiments/__init__.py
+-rw-r--r--   0        0        0    23462 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/experiments/cli_profile.py
+-rw-r--r--   0        0        0     1757 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/experiments/cli_query.py
+-rw-r--r--   0        0        0     9215 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/experiments/provision.py
+-rw-r--r--   0        0        0     3100 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/impl/common.py
+-rw-r--r--   0        0        0     4678 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/impl/cp_replicate_fallback.py
+-rw-r--r--   0        0        0     3071 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/cli/impl/progress_bar.py
+-rw-r--r--   0        0        0     1247 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/__init__.py
+-rw-r--r--   0        0        0     5908 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_auth.py
+-rw-r--r--   0        0        0    11591 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_cloud_provider.py
+-rw-r--r--   0        0        0     4315 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_key_manager.py
+-rw-r--r--   0        0        0    11509 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_network.py
+-rw-r--r--   0        0        0     1606 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_pricing.py
+-rw-r--r--   0        0        0     6294 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_server.py
+-rw-r--r--   0        0        0     9526 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/azure/azure_auth.py
+-rw-r--r--   0        0        0    20681 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/azure/azure_cloud_provider.py
+-rw-r--r--   0        0        0     7503 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/azure/azure_server.py
+-rw-r--r--   0        0        0     3564 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/cloud_provider.py
+-rw-r--r--   0        0        0     2883 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/const_cmds.py
+-rw-r--r--   0        0        0    12043 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_auth.py
+-rw-r--r--   0        0        0     9355 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_cloud_provider.py
+-rw-r--r--   0        0        0     2462 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_key_manager.py
+-rw-r--r--   0        0        0     6288 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_network.py
+-rw-r--r--   0        0        0     2786 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_pricing.py
+-rw-r--r--   0        0        0     5151 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_server.py
+-rw-r--r--   0        0        0      211 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_credentials.yaml.template
+-rw-r--r--   0        0        0        0 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/__init__.py
+-rw-r--r--   0        0        0     2242 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/config.py
+-rw-r--r--   0        0        0      877 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/constants.py
+-rw-r--r--   0        0        0     5353 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/ssh_client.py
+-rw-r--r--   0        0        0      710 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/utils.py
+-rw-r--r--   0        0        0    40464 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/vpc_backend.py
+-rw-r--r--   0        0        0     5320 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibmcloud_auth.py
+-rw-r--r--   0        0        0     2851 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibmcloud_provider.py
+-rw-r--r--   0        0        0     3522 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibmcloud_server.py
+-rw-r--r--   0        0        0      937 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/key_utils.py
+-rw-r--r--   0        0        0    17426 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/compute/server.py
+-rw-r--r--   0        0        0    13473 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/config.py
+-rw-r--r--   0        0        0     1229 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/config_paths.py
+-rw-r--r--   0        0        0        0 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/data/__init__.py
+-rw-r--r--   0        0        0    19636 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/data/aws_transfer_costs.csv
+-rw-r--r--   0        0        0      617 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/data/vcpu_info.csv
+-rw-r--r--   0        0        0     3078 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/exceptions.py
+-rw-r--r--   0        0        0      811 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/cert.py
+-rw-r--r--   0        0        0     4349 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/chunk_store.py
+-rw-r--r--   0        0        0    15655 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_daemon.py
+-rw-r--r--   0        0        0    16570 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_daemon_api.py
+-rw-r--r--   0        0        0      718 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_onprem.py
+-rw-r--r--   0        0        0     5149 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_program.py
+-rw-r--r--   0        0        0     1732 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_queue.py
+-rw-r--r--   0        0        0        0 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/operators/__init__.py
+-rw-r--r--   0        0        0    25487 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/operators/gateway_operator.py
+-rw-r--r--   0        0        0    10552 2023-07-21 23:44:20.368726 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/operators/gateway_receiver.py
+-rw-r--r--   0        0        0       37 2023-07-21 23:45:07.104894 skyplane_nightly-0.3.2.dev20230721/skyplane/gateway_version.py
+-rw-r--r--   0        0        0    13101 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/azure_blob_interface.py
+-rw-r--r--   0        0        0     2887 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/azure_storage_account_interface.py
+-rw-r--r--   0        0        0    10871 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/cos_interface.py
+-rw-r--r--   0        0        0     2010 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/file_system_interface.py
+-rw-r--r--   0        0        0    12754 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/gcs_interface.py
+-rw-r--r--   0        0        0     5963 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/hdfs_interface.py
+-rw-r--r--   0        0        0     3287 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/object_store_interface.py
+-rw-r--r--   0        0        0     5644 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/posix_file_interface.py
+-rw-r--r--   0        0        0     3606 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/r2_interface.py
+-rw-r--r--   0        0        0    11595 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/s3_interface.py
+-rw-r--r--   0        0        0     2569 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/storage_interface.py
+-rw-r--r--   0        0        0    23858 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/planner/planner.py
+-rw-r--r--   0        0        0    18157 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/planner/solver.py
+-rw-r--r--   0        0        0     6467 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/planner/solver_ilp.py
+-rw-r--r--   0        0        0     1996 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/planner/solver_ron.py
+-rw-r--r--   0        0        0     7920 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/planner/topology.py
+-rw-r--r--   0        0        0      846 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/cache.py
+-rw-r--r--   0        0        0      617 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/definitions.py
+-rw-r--r--   0        0        0     2494 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/fn.py
+-rw-r--r--   0        0        0     1881 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/generator.py
+-rw-r--r--   0        0        0     1386 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/imports.py
+-rw-r--r--   0        0        0     2131 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/logger.py
+-rw-r--r--   0        0        0     1447 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/networking_tools.py
+-rw-r--r--   0        0        0     3162 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/path.py
+-rw-r--r--   0        0        0     1160 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/retry.py
+-rw-r--r--   0        0        0      612 2023-07-21 23:44:20.372726 skyplane_nightly-0.3.2.dev20230721/skyplane/utils/timer.py
+-rw-r--r--   0        0        0    10740 1970-01-01 00:00:00.000000 skyplane_nightly-0.3.2.dev20230721/PKG-INFO
```

### Comparing `skyplane_nightly-0.3.2.dev20230720/LICENSE` & `skyplane_nightly-0.3.2.dev20230721/LICENSE`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/README.md` & `skyplane_nightly-0.3.2.dev20230721/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -1,452 +1,467 @@
-00000000: 3c70 6963 7475 7265 3e0a 2020 2020 3c73  <picture>.    <s
-00000010: 6f75 7263 6520 7372 6373 6574 3d22 646f  ource srcset="do
-00000020: 6373 2f5f 7374 6174 6963 2f6c 6f67 6f2d  cs/_static/logo-
-00000030: 6461 726b 2d6d 6f64 652e 706e 6722 206d  dark-mode.png" m
-00000040: 6564 6961 3d22 2870 7265 6665 7273 2d63  edia="(prefers-c
-00000050: 6f6c 6f72 2d73 6368 656d 653a 2064 6172  olor-scheme: dar
-00000060: 6b29 223e 0a20 2020 203c 696d 6720 7372  k)">.    <img sr
-00000070: 633d 2264 6f63 732f 5f73 7461 7469 632f  c="docs/_static/
-00000080: 6c6f 676f 2d6c 6967 6874 2d6d 6f64 652e  logo-light-mode.
-00000090: 706e 6722 2077 6964 7468 3d22 3330 3022  png" width="300"
-000000a0: 202f 3e0a 3c2f 7069 6374 7572 653e 0a0a   />.</picture>..
-000000b0: 5b21 5b4a 6f69 6e20 536c 6163 6b5d 2868  [![Join Slack](h
-000000c0: 7474 7073 3a2f 2f69 6d67 2e73 6869 656c  ttps://img.shiel
-000000d0: 6473 2e69 6f2f 6261 6467 652f 2d4a 6f69  ds.io/badge/-Joi
-000000e0: 6e25 3230 536b 7970 6c61 6e65 2532 3053  n%20Skyplane%20S
-000000f0: 6c61 636b 2d62 6c75 653f 6c6f 676f 3d73  lack-blue?logo=s
-00000100: 6c61 636b 295d 2868 7474 7073 3a2f 2f6a  lack)](https://j
-00000110: 6f69 6e2e 736c 6163 6b2e 636f 6d2f 742f  oin.slack.com/t/
-00000120: 736b 7970 6c61 6e65 776f 726b 7370 6163  skyplaneworkspac
-00000130: 652f 7368 6172 6564 5f69 6e76 6974 652f  e/shared_invite/
-00000140: 7a74 2d31 6378 6d65 6463 7563 2d47 7749  zt-1cxmedcuc-GwI
-00000150: 584c 4779 4854 794f 5945 4c71 374b 6f4f  XLGyHTyOYELq7KoO
-00000160: 6c36 5129 0a5b 215b 696e 7465 6772 6174  l6Q).[![integrat
-00000170: 696f 6e2d 7465 7374 5d28 6874 7470 733a  ion-test](https:
-00000180: 2f2f 6769 7468 7562 2e63 6f6d 2f73 6b79  //github.com/sky
-00000190: 706c 616e 652d 7072 6f6a 6563 742f 736b  plane-project/sk
-000001a0: 7970 6c61 6e65 2f61 6374 696f 6e73 2f77  yplane/actions/w
-000001b0: 6f72 6b66 6c6f 7773 2f69 6e74 6567 7261  orkflows/integra
-000001c0: 7469 6f6e 2d74 6573 742e 796d 6c2f 6261  tion-test.yml/ba
-000001d0: 6467 652e 7376 6729 5d28 6874 7470 733a  dge.svg)](https:
-000001e0: 2f2f 6769 7468 7562 2e63 6f6d 2f73 6b79  //github.com/sky
-000001f0: 706c 616e 652d 7072 6f6a 6563 742f 736b  plane-project/sk
-00000200: 7970 6c61 6e65 2f61 6374 696f 6e73 2f77  yplane/actions/w
-00000210: 6f72 6b66 6c6f 7773 2f69 6e74 6567 7261  orkflows/integra
-00000220: 7469 6f6e 2d74 6573 742e 796d 6c29 0a5b  tion-test.yml).[
-00000230: 215b 646f 636b 6572 5d28 6874 7470 733a  ![docker](https:
-00000240: 2f2f 6769 7468 7562 2e63 6f6d 2f73 6b79  //github.com/sky
-00000250: 706c 616e 652d 7072 6f6a 6563 742f 736b  plane-project/sk
-00000260: 7970 6c61 6e65 2f61 6374 696f 6e73 2f77  yplane/actions/w
-00000270: 6f72 6b66 6c6f 7773 2f64 6f63 6b65 722d  orkflows/docker-
-00000280: 7075 626c 6973 682e 796d 6c2f 6261 6467  publish.yml/badg
-00000290: 652e 7376 6729 5d28 6874 7470 733a 2f2f  e.svg)](https://
-000002a0: 6769 7468 7562 2e63 6f6d 2f73 6b79 706c  github.com/skypl
-000002b0: 616e 652d 7072 6f6a 6563 742f 736b 7970  ane-project/skyp
-000002c0: 6c61 6e65 2f61 6374 696f 6e73 2f77 6f72  lane/actions/wor
-000002d0: 6b66 6c6f 7773 2f64 6f63 6b65 722d 7075  kflows/docker-pu
-000002e0: 626c 6973 682e 796d 6c29 0a5b 215b 646f  blish.yml).[![do
-000002f0: 6373 5d28 6874 7470 733a 2f2f 7265 6164  cs](https://read
-00000300: 7468 6564 6f63 732e 6f72 672f 7072 6f6a  thedocs.org/proj
-00000310: 6563 7473 2f73 6b79 706c 616e 652f 6261  ects/skyplane/ba
-00000320: 6467 652f 3f76 6572 7369 6f6e 3d6c 6174  dge/?version=lat
-00000330: 6573 7429 5d28 6874 7470 733a 2f2f 736b  est)](https://sk
-00000340: 7970 6c61 6e65 2e72 6561 6474 6865 646f  yplane.readthedo
-00000350: 6373 2e69 6f2f 656e 2f6c 6174 6573 742f  cs.io/en/latest/
-00000360: 3f62 6164 6765 3d6c 6174 6573 7429 0a0a  ?badge=latest)..
-00000370: 2a2a f09f 94a5 2042 6c61 7a69 6e67 2066  **.... Blazing f
-00000380: 6173 7420 6275 6c6b 2064 6174 6120 7472  ast bulk data tr
-00000390: 616e 7366 6572 7320 6265 7477 6565 6e20  ansfers between 
-000003a0: 616e 7920 636c 6f75 6420 f09f 94a5 2a2a  any cloud ....**
-000003b0: 0a0a 536b 7970 6c61 6e65 2069 7320 6120  ..Skyplane is a 
-000003c0: 746f 6f6c 2066 6f72 2062 6c61 7a69 6e67  tool for blazing
-000003d0: 6c79 2066 6173 7420 6275 6c6b 2064 6174  ly fast bulk dat
-000003e0: 6120 7472 616e 7366 6572 7320 6265 7477  a transfers betw
-000003f0: 6565 6e20 6f62 6a65 6374 2073 746f 7265  een object store
-00000400: 7320 696e 2074 6865 2063 6c6f 7564 2e20  s in the cloud. 
-00000410: 4974 2070 726f 7669 7369 6f6e 7320 6120  It provisions a 
-00000420: 666c 6565 7420 6f66 2056 4d73 2069 6e20  fleet of VMs in 
-00000430: 7468 6520 636c 6f75 6420 746f 2074 7261  the cloud to tra
-00000440: 6e73 6665 7220 6461 7461 2069 6e20 7061  nsfer data in pa
-00000450: 7261 6c6c 656c 2077 6869 6c65 2075 7369  rallel while usi
-00000460: 6e67 2063 6f6d 7072 6573 7369 6f6e 2061  ng compression a
-00000470: 6e64 2062 616e 6477 6964 7468 2074 6965  nd bandwidth tie
-00000480: 7269 6e67 2074 6f20 7265 6475 6365 2063  ring to reduce c
-00000490: 6f73 742e 0a0a 536b 7970 6c61 6e65 2069  ost...Skyplane i
-000004a0: 733a 0a31 2e20 f09f 94a5 2042 6c61 7a69  s:.1. .... Blazi
-000004b0: 6e67 2066 6173 7420 285b 3131 3078 2066  ng fast ([110x f
-000004c0: 6173 7465 7220 7468 616e 2041 5753 2044  aster than AWS D
-000004d0: 6174 6153 796e 635d 2868 7474 7073 3a2f  ataSync](https:/
-000004e0: 2f73 6b79 706c 616e 652e 6f72 672f 656e  /skyplane.org/en
-000004f0: 2f6c 6174 6573 742f 6265 6e63 686d 6172  /latest/benchmar
-00000500: 6b2e 6874 6d6c 2929 0a32 2e20 f09f a491  k.html)).2. ....
-00000510: 2043 6865 6170 2028 3478 2063 6865 6170   Cheap (4x cheap
-00000520: 6572 2074 6861 6e20 7273 796e 6329 0a33  er than rsync).3
-00000530: 2e20 f09f 8c90 2055 6e69 7665 7273 616c  . .... Universal
-00000540: 2028 4157 532c 2041 7a75 7265 2c20 4942   (AWS, Azure, IB
-00000550: 4d20 616e 6420 4743 5029 0a0a 596f 7520  M and GCP)..You 
-00000560: 6361 6e20 7573 6520 536b 7970 6c61 6e65  can use Skyplane
-00000570: 2074 6f20 7472 616e 7366 6572 2064 6174   to transfer dat
-00000580: 613a 200a 2a20 6265 7477 6565 6e20 6f62  a: .* between ob
-00000590: 6a65 6374 2073 746f 7265 7320 7769 7468  ject stores with
-000005a0: 696e 2061 2063 6c6f 7564 2070 726f 7669  in a cloud provi
-000005b0: 6465 7220 2865 2e67 2e20 4157 5320 7573  der (e.g. AWS us
-000005c0: 2d65 6173 742d 3120 746f 2041 5753 2075  -east-1 to AWS u
-000005d0: 732d 7765 7374 2d32 290a 2a20 6265 7477  s-west-2).* betw
-000005e0: 6565 6e20 6f62 6a65 6374 2073 746f 7265  een object store
-000005f0: 7320 6163 726f 7373 206d 756c 7469 706c  s across multipl
-00000600: 6520 636c 6f75 6420 7072 6f76 6964 6572  e cloud provider
-00000610: 7320 2865 2e67 2e20 4157 5320 7573 2d65  s (e.g. AWS us-e
-00000620: 6173 742d 3120 746f 2047 4350 2075 732d  ast-1 to GCP us-
-00000630: 6365 6e74 7261 6c31 290a 2a20 6265 7477  central1).* betw
-00000640: 6565 6e20 6c6f 6361 6c20 7374 6f72 6167  een local storag
-00000650: 6520 616e 6420 636c 6f75 6420 6f62 6a65  e and cloud obje
-00000660: 6374 2073 746f 7265 7320 2865 7870 6572  ct stores (exper
-00000670: 696d 656e 7461 6c29 0a0a 536b 7970 6c61  imental)..Skypla
-00000680: 6e65 2063 7572 7265 6e74 6c79 2073 7570  ne currently sup
-00000690: 706f 7274 7320 7468 6520 666f 6c6c 6f77  ports the follow
-000006a0: 696e 6720 736f 7572 6365 2061 6e64 2064  ing source and d
-000006b0: 6573 7469 6e61 7469 6f6e 2065 6e64 706f  estination endpo
-000006c0: 696e 7473 2028 616e 7920 736f 7572 6365  ints (any source
-000006d0: 2061 6e64 2064 6573 7469 6e61 7469 6f6e   and destination
-000006e0: 2063 616e 2062 6520 636f 6d62 696e 6564   can be combined
-000006f0: 293a 200a 0a7c 2045 6e64 706f 696e 7420  ): ..| Endpoint 
-00000700: 2020 2020 2020 2020 2020 7c20 536f 7572            | Sour
-00000710: 6365 2020 2020 2020 2020 2020 2020 207c  ce             |
-00000720: 2044 6573 7469 6e61 7469 6f6e 2020 2020   Destination    
-00000730: 2020 2020 7c0a 7c2d 2d2d 2d2d 2d2d 2d2d      |.|---------
-00000740: 2d2d 2d2d 2d2d 2d2d 2d2d 2d7c 2d2d 2d2d  -----------|----
-00000750: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-00000760: 7c2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  |---------------
-00000770: 2d2d 2d2d 2d7c 0a7c 2041 5753 2053 3320  -----|.| AWS S3 
-00000780: 2020 2020 2020 2020 2020 2020 7c20 3a77              | :w
-00000790: 6869 7465 5f63 6865 636b 5f6d 6172 6b3a  hite_check_mark:
-000007a0: 207c 203a 7768 6974 655f 6368 6563 6b5f   | :white_check_
-000007b0: 6d61 726b 3a20 7c0a 7c20 476f 6f67 6c65  mark: |.| Google
-000007c0: 2053 746f 7261 6765 2020 2020 207c 203a   Storage     | :
-000007d0: 7768 6974 655f 6368 6563 6b5f 6d61 726b  white_check_mark
-000007e0: 3a20 7c20 3a77 6869 7465 5f63 6865 636b  : | :white_check
-000007f0: 5f6d 6172 6b3a 207c 0a7c 2041 7a75 7265  _mark: |.| Azure
-00000800: 2042 6c6f 6220 5374 6f72 6167 6520 7c20   Blob Storage | 
-00000810: 3a77 6869 7465 5f63 6865 636b 5f6d 6172  :white_check_mar
-00000820: 6b3a 207c 203a 7768 6974 655f 6368 6563  k: | :white_chec
-00000830: 6b5f 6d61 726b 3a20 7c0a 7c20 4942 4d20  k_mark: |.| IBM 
-00000840: 436c 6f75 6420 4f62 6a65 6374 2053 746f  Cloud Object Sto
-00000850: 7261 6765 207c 203a 7768 6974 655f 6368  rage | :white_ch
-00000860: 6563 6b5f 6d61 726b 3a20 7c20 3a77 6869  eck_mark: | :whi
-00000870: 7465 5f63 6865 636b 5f6d 6172 6b3a 207c  te_check_mark: |
-00000880: 0a7c 204c 6f63 616c 2044 6973 6b20 2020  .| Local Disk   
-00000890: 2020 2020 2020 7c20 3a77 6869 7465 5f63        | :white_c
-000008a0: 6865 636b 5f6d 6172 6b3a 207c 2028 696e  heck_mark: | (in
-000008b0: 2070 726f 6772 6573 7329 2020 2020 2020   progress)      
-000008c0: 7c0a 0a53 6b79 706c 616e 6520 6973 2061  |..Skyplane is a
-000008d0: 6e20 6163 7469 7665 6c79 2064 6576 656c  n actively devel
-000008e0: 6f70 6564 2070 726f 6a65 6374 2e20 4974  oped project. It
-000008f0: 2077 696c 6c20 6861 7665 20f0 9f94 aa20   will have .... 
-00000900: 5348 4152 5020 4544 4745 5320 f09f 94aa  SHARP EDGES ....
-00000910: 2e20 506c 6561 7365 2066 696c 6520 616e  . Please file an
-00000920: 2069 7373 7565 206f 7220 6173 6b20 7468   issue or ask th
-00000930: 6520 636f 6e74 7269 6275 746f 7273 2076  e contributors v
-00000940: 6961 205b 7468 6520 2368 656c 7020 6368  ia [the #help ch
-00000950: 616e 6e65 6c20 6f6e 206f 7572 2053 6c61  annel on our Sla
-00000960: 636b 5d28 6874 7470 733a 2f2f 6a6f 696e  ck](https://join
-00000970: 2e73 6c61 636b 2e63 6f6d 2f74 2f73 6b79  .slack.com/t/sky
-00000980: 706c 616e 6577 6f72 6b73 7061 6365 2f73  planeworkspace/s
-00000990: 6861 7265 645f 696e 7669 7465 2f7a 742d  hared_invite/zt-
-000009a0: 3163 786d 6564 6375 632d 4777 4958 4c47  1cxmedcuc-GwIXLG
-000009b0: 7948 5479 4f59 454c 7137 4b6f 4f6c 3651  yHTyOYELq7KoOl6Q
-000009c0: 2920 6966 2079 6f75 2065 6e63 6f75 6e74  ) if you encount
-000009d0: 6572 2062 7567 732e 0a0a 2320 5265 736f  er bugs...# Reso
-000009e0: 7572 6365 7320 0a2d 205b 5175 6963 6b73  urces .- [Quicks
-000009f0: 7461 7274 5d28 2371 7569 636b 7374 6172  tart](#quickstar
-00000a00: 7429 0a2d 205b 436f 6e74 7269 6275 7469  t).- [Contributi
-00000a10: 6e67 5d28 6874 7470 733a 2f2f 736b 7970  ng](https://skyp
-00000a20: 6c61 6e65 2e6f 7267 2f65 6e2f 6c61 7465  lane.org/en/late
-00000a30: 7374 2f63 6f6e 7472 6962 7574 696e 672e  st/contributing.
-00000a40: 6874 6d6c 290a 2d20 5b52 6f61 646d 6170  html).- [Roadmap
-00000a50: 5d28 6874 7470 733a 2f2f 736b 7970 6c61  ](https://skypla
-00000a60: 6e65 2e6f 7267 2f65 6e2f 6c61 7465 7374  ne.org/en/latest
-00000a70: 2f72 6f61 646d 6170 2e68 746d 6c29 0a2d  /roadmap.html).-
-00000a80: 205b 536c 6163 6b20 436f 6d6d 756e 6974   [Slack Communit
-00000a90: 795d 2868 7474 7073 3a2f 2f6a 6f69 6e2e  y](https://join.
-00000aa0: 736c 6163 6b2e 636f 6d2f 742f 736b 7970  slack.com/t/skyp
-00000ab0: 6c61 6e65 776f 726b 7370 6163 652f 7368  laneworkspace/sh
-00000ac0: 6172 6564 5f69 6e76 6974 652f 7a74 2d31  ared_invite/zt-1
-00000ad0: 6378 6d65 6463 7563 2d47 7749 584c 4779  cxmedcuc-GwIXLGy
-00000ae0: 4854 794f 5945 4c71 374b 6f4f 6c36 5129  HTyOYELq7KoOl6Q)
-00000af0: 0a0a 2320 5175 6963 6b73 7461 7274 0a0a  ..# Quickstart..
-00000b00: 2323 2031 2e20 496e 7374 616c 6c61 7469  ## 1. Installati
-00000b10: 6f6e 0a57 6520 7265 636f 6d6d 656e 6420  on.We recommend 
-00000b20: 696e 7374 616c 6c61 7469 6f6e 2066 726f  installation fro
-00000b30: 6d20 5079 5069 3a0a 6060 600a 2420 7069  m PyPi:.```.$ pi
-00000b40: 7020 696e 7374 616c 6c20 2273 6b79 706c  p install "skypl
-00000b50: 616e 655b 6177 735d 220a 0a23 2069 6e73  ane[aws]"..# ins
-00000b60: 7461 6c6c 2073 7570 706f 7274 2066 6f72  tall support for
-00000b70: 206f 7468 6572 2063 6c6f 7564 7320 6173   other clouds as
-00000b80: 206e 6565 6465 643a 0a0a 2320 2020 2420   needed:..#   $ 
-00000b90: 7069 7020 696e 7374 616c 6c20 2273 6b79  pip install "sky
-00000ba0: 706c 616e 655b 617a 7572 655d 220a 2320  plane[azure]".# 
-00000bb0: 2020 2420 7069 7020 696e 7374 616c 6c20    $ pip install 
-00000bc0: 2273 6b79 706c 616e 655b 6763 705d 220a  "skyplane[gcp]".
-00000bd0: 2320 2020 2420 7069 7020 696e 7374 616c  #   $ pip instal
-00000be0: 6c20 2273 6b79 706c 616e 655b 6962 6d63  l "skyplane[ibmc
-00000bf0: 6c6f 7564 5d22 0a23 2020 2024 2070 6970  loud]".#   $ pip
-00000c00: 2069 6e73 7461 6c6c 2022 736b 7970 6c61   install "skypla
-00000c10: 6e65 5b61 6c6c 5d22 0a60 6060 0a0a 536b  ne[all]".```..Sk
-00000c20: 7970 6c61 6e65 2073 7570 706f 7274 7320  yplane supports 
-00000c30: 4157 532c 2041 7a75 7265 2c20 4942 4d20  AWS, Azure, IBM 
-00000c40: 616e 6420 4743 502e 2059 6f75 2063 616e  and GCP. You can
-00000c50: 2069 6e73 7461 6c6c 2053 6b79 706c 616e   install Skyplan
-00000c60: 6520 7769 7468 2073 7570 706f 7274 2066  e with support f
-00000c70: 6f72 206f 6e65 206f 7220 6d6f 7265 206f  or one or more o
-00000c80: 6620 7468 6573 6520 636c 6f75 6473 2062  f these clouds b
-00000c90: 7920 7370 6563 6966 7969 6e67 2074 6865  y specifying the
-00000ca0: 2063 6f72 7265 7370 6f6e 6469 6e67 2065   corresponding e
-00000cb0: 7874 7261 732e 2054 6f20 696e 7374 616c  xtras. To instal
-00000cc0: 6c20 7477 6f20 6f75 7420 6f66 2074 6872  l two out of thr
-00000cd0: 6565 2063 6c6f 7564 732c 2079 6f75 2063  ee clouds, you c
-00000ce0: 616e 2072 756e 2060 7069 7020 696e 7374  an run `pip inst
-00000cf0: 616c 6c20 2273 6b79 706c 616e 655b 6177  all "skyplane[aw
-00000d00: 732c 617a 7572 655d 2260 2e0a 0a2a 4743  s,azure]"`...*GC
-00000d10: 5020 7375 7070 6f72 7420 6f6e 2074 6865  P support on the
-00000d20: 204d 3120 4d61 632a 3a20 4966 2079 6f75   M1 Mac*: If you
-00000d30: 2061 7265 2075 7369 6e67 2061 6e20 4d31   are using an M1
-00000d40: 204d 6163 2077 6974 6820 7468 6520 6172   Mac with the ar
-00000d50: 6d36 3420 6172 6368 6974 6563 7475 7265  m64 architecture
-00000d60: 2061 6e64 2077 616e 7420 746f 2069 6e73   and want to ins
-00000d70: 7461 6c6c 2047 4350 2073 7570 706f 7274  tall GCP support
-00000d80: 2066 6f72 2053 6b79 706c 616e 652c 2079   for Skyplane, y
-00000d90: 6f75 2077 696c 6c20 6e65 6564 2074 6f20  ou will need to 
-00000da0: 696e 7374 616c 6c20 6173 2066 6f6c 6c6f  install as follo
-00000db0: 7773 0a60 4752 5043 5f50 5954 484f 4e5f  ws.`GRPC_PYTHON_
-00000dc0: 4255 494c 445f 5359 5354 454d 5f4f 5045  BUILD_SYSTEM_OPE
-00000dd0: 4e53 534c 3d31 2047 5250 435f 5059 5448  NSSL=1 GRPC_PYTH
-00000de0: 4f4e 5f42 5549 4c44 5f53 5953 5445 4d5f  ON_BUILD_SYSTEM_
-00000df0: 5a4c 4942 3d31 2070 6970 2069 6e73 7461  ZLIB=1 pip insta
-00000e00: 6c6c 2022 736b 7970 6c61 6e65 5b61 7773  ll "skyplane[aws
-00000e10: 2c67 6370 5d22 600a 0a23 2320 322e 2053  ,gcp]"`..## 2. S
-00000e20: 6574 7570 2043 6c6f 7564 2043 7265 6465  etup Cloud Crede
-00000e30: 6e74 6961 6c73 200a 0a53 6b79 706c 616e  ntials ..Skyplan
-00000e40: 6520 6e65 6564 7320 6163 6365 7373 2074  e needs access t
-00000e50: 6f20 636c 6f75 6420 6372 6564 656e 7469  o cloud credenti
-00000e60: 616c 7320 746f 2070 6572 666f 726d 2074  als to perform t
-00000e70: 7261 6e73 6665 7273 2e20 546f 2067 6574  ransfers. To get
-00000e80: 2073 7461 7274 6564 2077 6974 6820 7365   started with se
-00000e90: 7474 696e 6720 7570 2063 7265 6465 6e74  tting up credent
-00000ea0: 6961 6c73 2c20 6d61 6b65 2073 7572 6520  ials, make sure 
-00000eb0: 796f 7520 6861 7665 2063 6c6f 7564 2070  you have cloud p
-00000ec0: 726f 7669 6465 7220 434c 4920 746f 6f6c  rovider CLI tool
-00000ed0: 7320 696e 7374 616c 6c65 643a 0a0a 6060  s installed:..``
-00000ee0: 600a 2d2d 2d3e 2046 6f72 2041 5753 3a0a  `.---> For AWS:.
-00000ef0: 2420 7069 7020 696e 7374 616c 6c20 6177  $ pip install aw
-00000f00: 7363 6c69 0a0a 2d2d 2d3e 2046 6f72 2047  scli..---> For G
-00000f10: 6f6f 676c 6520 436c 6f75 643a 0a24 2070  oogle Cloud:.$ p
-00000f20: 6970 2069 6e73 7461 6c6c 2067 636c 6f75  ip install gclou
-00000f30: 640a 0a2d 2d2d 3e20 466f 7220 417a 7572  d..---> For Azur
-00000f40: 653a 0a24 2070 6970 2069 6e73 7461 6c6c  e:.$ pip install
-00000f50: 2061 7a75 7265 0a0a 6060 600a 4f6e 6365   azure..```.Once
-00000f60: 2079 6f75 2068 6176 6520 7468 6520 434c   you have the CL
-00000f70: 4920 746f 6f6c 7320 7365 7475 702c 206c  I tools setup, l
-00000f80: 6f67 2069 6e74 6f20 6561 6368 2063 6c6f  og into each clo
-00000f90: 7564 2070 726f 7669 6465 7227 7320 434c  ud provider's CL
-00000fa0: 493a 0a60 6060 0a2d 2d2d 3e20 466f 7220  I:.```.---> For 
-00000fb0: 4157 533a 0a24 2061 7773 2063 6f6e 6669  AWS:.$ aws confi
-00000fc0: 6775 7265 0a0a 2d2d 2d3e 2046 6f72 2047  gure..---> For G
-00000fd0: 6f6f 676c 6520 436c 6f75 643a 0a24 2067  oogle Cloud:.$ g
-00000fe0: 636c 6f75 6420 6175 7468 2061 7070 6c69  cloud auth appli
-00000ff0: 6361 7469 6f6e 2d64 6566 6175 6c74 206c  cation-default l
-00001000: 6f67 696e 0a0a 2d2d 2d3e 2046 6f72 2041  ogin..---> For A
-00001010: 7a75 7265 3a0a 2420 617a 206c 6f67 696e  zure:.$ az login
-00001020: 0a0a 2d2d 2d3e 2046 6f72 2049 424d 2043  ..---> For IBM C
-00001030: 6c6f 7564 3a0a 2420 466f 6c6c 6f77 2049  loud:.$ Follow I
-00001040: 424d 2043 6c6f 7564 2061 6e64 2063 7265  BM Cloud and cre
-00001050: 6174 6520 616e 2061 6363 6f75 6e74 2077  ate an account w
-00001060: 6974 6820 7468 6520 7265 736f 7572 6365  ith the resource
-00001070: 2067 726f 7570 2e0a 436f 7079 2068 7474   group..Copy htt
-00001080: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
-00001090: 736b 7970 6c61 6e65 2d70 726f 6a65 6374  skyplane-project
-000010a0: 2f73 6b79 706c 616e 652f 626c 6f62 2f6d  /skyplane/blob/m
-000010b0: 6169 6e2f 736b 7970 6c61 6e65 2f63 6f6d  ain/skyplane/com
-000010c0: 7075 7465 2f69 626d 636c 6f75 642f 6962  pute/ibmcloud/ib
-000010d0: 6d5f 6372 6564 656e 7469 616c 732e 7961  m_credentials.ya
-000010e0: 6d6c 2e74 656d 706c 6174 650a 696e 746f  ml.template.into
-000010f0: 2060 7e2f 2e62 6c75 656d 6978 2f69 626d   `~/.bluemix/ibm
-00001100: 5f63 7265 6465 6e74 6961 6c73 6020 616e  _credentials` an
-00001110: 6420 6669 6c6c 2079 6f75 7220 0a49 424d  d fill your .IBM
-00001120: 2049 414d 206b 6579 2061 6e64 2063 7265   IAM key and cre
-00001130: 6465 6e74 6961 6c73 2074 6f20 796f 7572  dentials to your
-00001140: 2049 424d 2043 6c6f 7564 206f 626a 6563   IBM Cloud objec
-00001150: 7420 7374 6f72 6167 6520 0a0a 0a60 6060  t storage ...```
-00001160: 0a41 6674 6572 2061 7574 6865 6e74 6963  .After authentic
-00001170: 6174 696e 6720 7769 7468 2065 6163 6820  ating with each 
-00001180: 636c 6f75 6420 7072 6f76 6964 6572 2c20  cloud provider, 
-00001190: 796f 7520 6361 6e20 7275 6e20 6073 6b79  you can run `sky
-000011a0: 706c 616e 6520 696e 6974 6020 746f 2063  plane init` to c
-000011b0: 7265 6174 6520 6120 636f 6e66 6967 7572  reate a configur
-000011c0: 6174 696f 6e20 6669 6c65 2066 6f72 2053  ation file for S
-000011d0: 6b79 706c 616e 652e 0a0a 6060 6062 6173  kyplane...```bas
-000011e0: 680a 2420 736b 7970 6c61 6e65 2069 6e69  h.$ skyplane ini
-000011f0: 740a 6060 600a 3c64 6574 6169 6c73 3e0a  t.```.<details>.
-00001200: 3c73 756d 6d61 7279 3e73 6b79 706c 616e  <summary>skyplan
-00001210: 6520 696e 6974 206f 7574 7075 743c 2f73  e init output</s
-00001220: 756d 6d61 7279 3e0a 3c62 723e 0a0a 6060  ummary>.<br>..``
-00001230: 600a 2420 736b 7970 6c61 6e65 2069 6e69  `.$ skyplane ini
-00001240: 740a 0a3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  t..=============
-00001250: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
-00001260: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
-00001270: 3d3d 3d3d 3d3d 3d0a 205f 5f5f 5f5f 205f  =======. _____ _
-00001280: 2020 205f 5f5f 5f20 2020 5f5f 5f5f 5f5f     ____   ______
-00001290: 5f20 5f20 2020 2020 2020 5f5f 5f20 2020  _ _       ___   
-000012a0: 5f20 2020 5f20 205f 5f5f 5f5f 0a2f 2020  _   _  _____./  
-000012b0: 5f5f 5f7c 207c 202f 202f 5c20 5c20 2f20  ___| | / /\ \ / 
-000012c0: 2f20 5f5f 5f20 5c20 7c20 2020 2020 2f20  / ___ \ |     / 
-000012d0: 5f20 5c20 7c20 5c20 7c20 7c7c 2020 5f5f  _ \ | \ | ||  __
-000012e0: 5f7c 0a5c 2060 2d2d 2e7c 207c 2f20 2f20  _|.\ `--.| |/ / 
-000012f0: 205c 2056 202f 7c20 7c5f 2f20 2f20 7c20   \ V /| |_/ / | 
-00001300: 2020 202f 202f 5f5c 205c 7c20 205c 7c20     / /_\ \|  \| 
-00001310: 7c7c 207c 5f5f 0a20 602d 2d2e 205c 2020  || |__. `--. \  
-00001320: 2020 5c20 2020 5c20 2f20 7c20 205f 5f2f    \   \ / |  __/
-00001330: 7c20 7c20 2020 207c 2020 5f20 207c 7c20  | |    |  _  || 
-00001340: 2e20 6020 7c7c 2020 5f5f 7c0a 2f5c 5f5f  . ` ||  __|./\__
-00001350: 2f20 2f20 7c5c 2020 5c20 207c 207c 207c  / / |\  \  | | |
-00001360: 207c 2020 207c 207c 5f5f 5f5f 7c20 7c20   |   | |____| | 
-00001370: 7c20 7c7c 207c 5c20 207c 7c20 7c5f 5f5f  | || |\  || |___
-00001380: 0a5c 5f5f 5f5f 2f5c 5f7c 205c 5f2f 2020  .\____/\_| \_/  
-00001390: 5c5f 2f20 5c5f 7c20 2020 5c5f 5f5f 5f5f  \_/ \_|   \_____
-000013a0: 2f5c 5f7c 207c 5f2f 5c5f 7c20 5c5f 2f5c  /\_| |_/\_| \_/\
-000013b0: 5f5f 5f5f 2f0a 3d3d 3d3d 3d3d 3d3d 3d3d  ____/.==========
-000013c0: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
-000013d0: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
-000013e0: 3d3d 3d3d 3d3d 3d3d 3d3d 0a0a 0a28 3129  ==========...(1)
-000013f0: 2043 6f6e 6669 6775 7269 6e67 2041 5753   Configuring AWS
-00001400: 3a0a 2020 2020 4c6f 6164 6564 2041 5753  :.    Loaded AWS
-00001410: 2063 7265 6465 6e74 6961 6c73 2066 726f   credentials fro
-00001420: 6d20 7468 6520 4157 5320 434c 4920 5b49  m the AWS CLI [I
-00001430: 414d 2061 6363 6573 7320 6b65 7920 4944  AM access key ID
-00001440: 3a20 2e2e 2e58 5858 5858 585d 0a20 2020  : ...XXXXXX].   
-00001450: 2041 5753 2072 6567 696f 6e20 636f 6e66   AWS region conf
-00001460: 6967 2066 696c 6520 7361 7665 6420 746f  ig file saved to
-00001470: 202f 686f 6d65 2f75 6275 6e74 752f 2e73   /home/ubuntu/.s
-00001480: 6b79 706c 616e 652f 6177 735f 636f 6e66  kyplane/aws_conf
-00001490: 6967 0a0a 2832 2920 436f 6e66 6967 7572  ig..(2) Configur
-000014a0: 696e 6720 417a 7572 653a 0a20 2020 2041  ing Azure:.    A
-000014b0: 7a75 7265 2063 7265 6465 6e74 6961 6c73  zure credentials
-000014c0: 2066 6f75 6e64 2069 6e20 417a 7572 6520   found in Azure 
-000014d0: 434c 490a 2020 2020 417a 7572 6520 6372  CLI.    Azure cr
-000014e0: 6564 656e 7469 616c 7320 666f 756e 642c  edentials found,
-000014f0: 2064 6f20 796f 7520 7761 6e74 2074 6f20   do you want to 
-00001500: 656e 6162 6c65 2041 7a75 7265 2073 7570  enable Azure sup
-00001510: 706f 7274 2069 6e20 536b 7970 6c61 6e65  port in Skyplane
-00001520: 3f20 5b59 2f6e 5d3a 2059 0a20 2020 2045  ? [Y/n]: Y.    E
-00001530: 6e74 6572 2074 6865 2041 7a75 7265 2073  nter the Azure s
-00001540: 7562 7363 7269 7074 696f 6e20 4944 3a20  ubscription ID: 
-00001550: 5b58 5858 5858 5858 582d 5858 5858 2d58  [XXXXXXXX-XXXX-X
-00001560: 5858 582d 5858 5858 2d58 5858 5858 5858  XXX-XXXX-XXXXXXX
-00001570: 5858 5858 585d 3a0a 2020 2020 417a 7572  XXXXX]:.    Azur
-00001580: 6520 7265 6769 6f6e 2063 6f6e 6669 6720  e region config 
-00001590: 6669 6c65 2073 6176 6564 2074 6f20 2f68  file saved to /h
-000015a0: 6f6d 652f 7562 756e 7475 2f2e 736b 7970  ome/ubuntu/.skyp
-000015b0: 6c61 6e65 2f61 7a75 7265 5f63 6f6e 6669  lane/azure_confi
-000015c0: 670a 2020 2020 5175 6572 7969 6e67 2066  g.    Querying f
-000015d0: 6f72 2053 4b55 2061 7661 696c 6269 6c69  or SKU availbili
-000015e0: 7479 2069 6e20 7265 6769 6f6e 730a 2020  ty in regions.  
-000015f0: 2020 417a 7572 6520 534b 5520 6176 6169    Azure SKU avai
-00001600: 6c61 6269 6c69 7479 2063 6163 6865 6420  lability cached 
-00001610: 696e 202f 686f 6d65 2f75 6275 6e74 752f  in /home/ubuntu/
-00001620: 2e73 6b79 706c 616e 652f 617a 7572 655f  .skyplane/azure_
-00001630: 736b 755f 6d61 7070 696e 670a 0a28 3329  sku_mapping..(3)
-00001640: 2043 6f6e 6669 6775 7269 6e67 2047 4350   Configuring GCP
-00001650: 3a0a 2020 2020 4743 5020 6372 6564 656e  :.    GCP creden
-00001660: 7469 616c 7320 666f 756e 6420 696e 2047  tials found in G
-00001670: 4350 2043 4c49 0a20 2020 2047 4350 2063  CP CLI.    GCP c
-00001680: 7265 6465 6e74 6961 6c73 2066 6f75 6e64  redentials found
-00001690: 2c20 646f 2079 6f75 2077 616e 7420 746f  , do you want to
-000016a0: 2065 6e61 626c 6520 4743 5020 7375 7070   enable GCP supp
-000016b0: 6f72 7420 696e 2053 6b79 706c 616e 653f  ort in Skyplane?
-000016c0: 205b 592f 6e5d 3a20 590a 2020 2020 456e   [Y/n]: Y.    En
-000016d0: 7465 7220 7468 6520 4743 5020 7072 6f6a  ter the GCP proj
-000016e0: 6563 7420 4944 205b 5858 5858 5858 585d  ect ID [XXXXXXX]
-000016f0: 3a0a 2020 2020 4743 5020 7265 6769 6f6e  :.    GCP region
-00001700: 2063 6f6e 6669 6720 6669 6c65 2073 6176   config file sav
-00001710: 6564 2074 6f20 2f68 6f6d 652f 7562 756e  ed to /home/ubun
-00001720: 7475 2f2e 736b 7970 6c61 6e65 2f67 6370  tu/.skyplane/gcp
-00001730: 5f63 6f6e 6669 670a 0a43 6f6e 6669 6720  _config..Config 
-00001740: 6669 6c65 2073 6176 6564 2074 6f20 2f68  file saved to /h
-00001750: 6f6d 652f 7562 756e 7475 2f2e 736b 7970  ome/ubuntu/.skyp
-00001760: 6c61 6e65 2f63 6f6e 6669 670a 6060 600a  lane/config.```.
-00001770: 0a3c 2f64 6574 6169 6c73 3e0a 0a23 2320  .</details>..## 
-00001780: 332e 2052 756e 2054 7261 6e73 6665 7273  3. Run Transfers
-00001790: 200a 0a57 65e2 8099 7265 2072 6561 6479   ..We...re ready
-000017a0: 2074 6f20 7573 6520 536b 7970 6c61 6e65   to use Skyplane
-000017b0: 2120 4c65 74e2 8099 7320 7573 6520 6073  ! Let...s use `s
-000017c0: 6b79 706c 616e 6520 6370 6020 746f 2063  kyplane cp` to c
-000017d0: 6f70 7920 6669 6c65 7320 6672 6f6d 2041  opy files from A
-000017e0: 5753 2074 6f20 4743 503a 0a60 6060 0a73  WS to GCP:.```.s
-000017f0: 6b79 706c 616e 6520 6370 2073 333a 2f2f  kyplane cp s3://
-00001800: 2e2e 2e20 6773 3a2f 2f2e 2e2e 0a60 6060  ... gs://....```
-00001810: 0a54 6f20 7472 616e 7366 6572 206f 6e6c  .To transfer onl
-00001820: 7920 6e65 7720 6f62 6a65 6374 732c 2079  y new objects, y
-00001830: 6f75 2063 616e 2069 6e73 7465 6164 2075  ou can instead u
-00001840: 7365 2060 736b 7970 6c61 6e65 2073 796e  se `skyplane syn
-00001850: 6360 3a0a 6060 600a 2420 736b 7970 6c61  c`:.```.$ skypla
-00001860: 6e65 2073 796e 6320 7333 3a2f 2f2e 2e2e  ne sync s3://...
-00001870: 2067 733a 2f2f 2e2e 2e0a 6060 600a 0a59   gs://....```..Y
-00001880: 6f75 2063 616e 2063 6f6e 6669 6775 7265  ou can configure
-00001890: 2053 6b79 706c 616e 6520 746f 2075 7365   Skyplane to use
-000018a0: 206d 6f72 6520 564d 7320 7065 7220 7265   more VMs per re
-000018b0: 6769 6f6e 2077 6974 6820 7468 6520 602d  gion with the `-
-000018c0: 6e60 2066 6c61 672e 2046 6f72 2065 7861  n` flag. For exa
-000018d0: 6d70 6c65 2c20 746f 2064 6f75 626c 6520  mple, to double 
-000018e0: 7468 6520 7472 616e 7366 6572 2073 7065  the transfer spe
-000018f0: 6564 2077 6974 6820 7477 6f20 564d 732c  ed with two VMs,
-00001900: 2072 756e 3a20 0a60 6060 0a24 2073 6b79   run: .```.$ sky
-00001910: 706c 616e 6520 6370 202d 7220 7333 3a2f  plane cp -r s3:/
-00001920: 2f2e 2e2e 2073 333a 2f2f 2e2e 2e20 2d6e  /... s3://... -n
-00001930: 2032 0a60 6060 0a0a 2323 2034 2e20 436c   2.```..## 4. Cl
-00001940: 6561 6e20 5570 200a 536b 7970 6c61 6e65  ean Up .Skyplane
-00001950: 2077 696c 6c20 6175 746f 6d61 7469 6361   will automatica
-00001960: 6c6c 7920 6174 7465 6d70 7420 746f 2074  lly attempt to t
-00001970: 6572 6d69 6e61 7465 2056 4d73 2074 6861  erminate VMs tha
-00001980: 7420 6974 2073 7461 7274 732c 2062 7574  t it starts, but
-00001990: 2074 6f20 646f 7562 6c65 2063 6865 636b   to double check
-000019a0: 2061 6e64 2066 6f72 6365 6675 6c79 2074   and forcefuly t
-000019b0: 6572 6d69 6e61 7465 2061 6c6c 2056 4d73  erminate all VMs
-000019c0: 2c20 7275 6e20 6073 6b79 706c 616e 6520  , run `skyplane 
-000019d0: 6465 7072 6f76 6973 696f 6e60 2e0a 0a23  deprovision`...#
-000019e0: 2054 6563 686e 6963 616c 2044 6574 6169   Technical Detai
-000019f0: 6c73 0a53 6b79 706c 616e 6520 6973 2062  ls.Skyplane is b
-00001a00: 6173 6564 206f 6e20 7265 7365 6172 6368  ased on research
-00001a10: 2061 7420 5543 2042 6572 6b65 6c65 7920   at UC Berkeley 
-00001a20: 696e 746f 2061 6363 656c 6572 6174 6564  into accelerated
-00001a30: 206e 6574 776f 726b 7320 6265 7477 6565   networks betwee
-00001a40: 6e20 636c 6f75 6420 7072 6f76 6964 6572  n cloud provider
-00001a50: 732e 2055 6e64 6572 2074 6865 2068 6f6f  s. Under the hoo
-00001a60: 642c 2053 6b79 706c 616e 6520 7374 6172  d, Skyplane star
-00001a70: 7473 2061 2066 6c65 6574 206f 6620 564d  ts a fleet of VM
-00001a80: 7320 696e 2074 6865 2073 6f75 7263 6520  s in the source 
-00001a90: 616e 6420 6465 7374 696e 6174 696f 6e20  and destination 
-00001aa0: 7265 6769 6f6e 732e 2049 7420 7468 656e  regions. It then
-00001ab0: 2075 7365 7320 6120 6375 7374 6f6d 2054   uses a custom T
-00001ac0: 4350 2070 726f 746f 636f 6c20 746f 2061  CP protocol to a
-00001ad0: 6363 656c 6572 6174 6520 7468 6520 7472  ccelerate the tr
-00001ae0: 616e 7366 6572 2062 6574 7765 656e 2074  ansfer between t
-00001af0: 6865 2056 4d73 2e20 536b 7970 6c61 6e65  he VMs. Skyplane
-00001b00: 206d 6179 2075 7365 2061 204c 3720 6f76   may use a L7 ov
-00001b10: 6572 6c61 7920 6e65 7477 6f72 6b20 746f  erlay network to
-00001b20: 2072 6f75 7465 2074 7261 6666 6963 2061   route traffic a
-00001b30: 726f 756e 6420 636f 6e67 6573 7465 6420  round congested 
-00001b40: 6e65 7477 6f72 6b20 686f 7420 7370 6f74  network hot spot
-00001b50: 732e 200a 0a3c 696d 6720 7372 633d 2264  s. ..<img src="d
-00001b60: 6f63 732f 5f73 7461 7469 632f 736b 7970  ocs/_static/skyp
-00001b70: 6c61 6e65 2d64 6174 612d 706c 616e 652e  lane-data-plane.
-00001b80: 706e 6722 2077 6964 7468 3d22 3338 3422  png" width="384"
-00001b90: 202f 3e0a 0a46 6f72 206d 6f72 6520 6465   />..For more de
-00001ba0: 7461 696c 7320 6f6e 2053 6b79 706c 616e  tails on Skyplan
-00001bb0: 652c 2073 6565 3a20 0a2d 205b 5465 6368  e, see: .- [Tech
-00001bc0: 6e69 6361 6c20 5461 6c6b 5d28 6874 7470  nical Talk](http
-00001bd0: 733a 2f2f 736b 7970 6c61 6e65 2e6f 7267  s://skyplane.org
-00001be0: 2f65 6e2f 6c61 7465 7374 2f61 7263 6869  /en/latest/archi
-00001bf0: 7465 6374 7572 652e 6874 6d6c 290a 2d20  tecture.html).- 
-00001c00: 5b4e 5344 4920 2732 3320 5061 7065 725d  [NSDI '23 Paper]
-00001c10: 2868 7474 7073 3a2f 2f61 7278 6976 2e6f  (https://arxiv.o
-00001c20: 7267 2f61 6273 2f32 3231 302e 3037 3235  rg/abs/2210.0725
-00001c30: 3929 0a0a 0a                             9)...
+00000000: 3c70 2061 6c69 676e 3d22 6365 6e74 6572  <p align="center
+00000010: 223e 0a20 2020 203c 7069 6374 7572 653e  ">.    <picture>
+00000020: 0a20 2020 2020 2020 203c 736f 7572 6365  .        <source
+00000030: 2073 7263 7365 743d 2264 6f63 732f 5f73   srcset="docs/_s
+00000040: 7461 7469 632f 6c6f 676f 2d64 6172 6b2d  tatic/logo-dark-
+00000050: 6d6f 6465 2e70 6e67 2220 6d65 6469 613d  mode.png" media=
+00000060: 2228 7072 6566 6572 732d 636f 6c6f 722d  "(prefers-color-
+00000070: 7363 6865 6d65 3a20 6461 726b 2922 3e0a  scheme: dark)">.
+00000080: 2020 2020 2020 2020 3c69 6d67 2073 7263          <img src
+00000090: 3d22 646f 6373 2f5f 7374 6174 6963 2f6c  ="docs/_static/l
+000000a0: 6f67 6f2d 6c69 6768 742d 6d6f 6465 2e70  ogo-light-mode.p
+000000b0: 6e67 2220 7769 6474 683d 2233 3030 2220  ng" width="300" 
+000000c0: 2f3e 0a20 2020 203c 2f70 6963 7475 7265  />.    </picture
+000000d0: 3e0a 3c2f 703e 0a0a 3c70 2061 6c69 676e  >.</p>..<p align
+000000e0: 3d22 6365 6e74 6572 223e 0a20 203c 6120  ="center">.  <a 
+000000f0: 6872 6566 3d22 6874 7470 733a 2f2f 6a6f  href="https://jo
+00000100: 696e 2e73 6c61 636b 2e63 6f6d 2f74 2f73  in.slack.com/t/s
+00000110: 6b79 706c 616e 6577 6f72 6b73 7061 6365  kyplaneworkspace
+00000120: 2f73 6861 7265 645f 696e 7669 7465 2f7a  /shared_invite/z
+00000130: 742d 3163 786d 6564 6375 632d 4777 4958  t-1cxmedcuc-GwIX
+00000140: 4c47 7948 5479 4f59 454c 7137 4b6f 4f6c  LGyHTyOYELq7KoOl
+00000150: 3651 223e 200a 2020 2020 3c69 6d67 2061  6Q"> .    <img a
+00000160: 6c74 3d22 4a6f 696e 2053 6c61 636b 2220  lt="Join Slack" 
+00000170: 7372 633d 2268 7474 7073 3a2f 2f69 6d67  src="https://img
+00000180: 2e73 6869 656c 6473 2e69 6f2f 6261 6467  .shields.io/badg
+00000190: 652f 2d4a 6f69 6e25 3230 536b 7970 6c61  e/-Join%20Skypla
+000001a0: 6e65 2532 3053 6c61 636b 2d62 6c75 653f  ne%20Slack-blue?
+000001b0: 6c6f 676f 3d73 6c61 636b 223e 0a20 203c  logo=slack">.  <
+000001c0: 2f61 3e0a 2020 0a20 203c 6120 6872 6566  /a>.  .  <a href
+000001d0: 3d22 6874 7470 733a 2f2f 6769 7468 7562  ="https://github
+000001e0: 2e63 6f6d 2f73 6b79 706c 616e 652d 7072  .com/skyplane-pr
+000001f0: 6f6a 6563 742f 736b 7970 6c61 6e65 2f61  oject/skyplane/a
+00000200: 6374 696f 6e73 2f77 6f72 6b66 6c6f 7773  ctions/workflows
+00000210: 2f69 6e74 6567 7261 7469 6f6e 2d74 6573  /integration-tes
+00000220: 742d 6d75 6c74 6970 6c65 2d73 697a 6573  t-multiple-sizes
+00000230: 2e79 6d6c 223e 200a 2020 2020 3c69 6d67  .yml"> .    <img
+00000240: 2061 6c74 3d22 696e 7465 6772 6174 696f   alt="integratio
+00000250: 6e2d 7465 7374 2220 7372 633d 2268 7474  n-test" src="htt
+00000260: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
+00000270: 736b 7970 6c61 6e65 2d70 726f 6a65 6374  skyplane-project
+00000280: 2f73 6b79 706c 616e 652f 6163 7469 6f6e  /skyplane/action
+00000290: 732f 776f 726b 666c 6f77 732f 696e 7465  s/workflows/inte
+000002a0: 6772 6174 696f 6e2d 7465 7374 2d6d 756c  gration-test-mul
+000002b0: 7469 706c 652d 7369 7a65 732e 796d 6c2f  tiple-sizes.yml/
+000002c0: 6261 6467 652e 7376 6722 3e0a 2020 3c2f  badge.svg">.  </
+000002d0: 613e 0a20 200a 2020 3c61 2068 7265 663d  a>.  .  <a href=
+000002e0: 2268 7474 7073 3a2f 2f67 6974 6875 622e  "https://github.
+000002f0: 636f 6d2f 736b 7970 6c61 6e65 2d70 726f  com/skyplane-pro
+00000300: 6a65 6374 2f73 6b79 706c 616e 652f 6163  ject/skyplane/ac
+00000310: 7469 6f6e 732f 776f 726b 666c 6f77 732f  tions/workflows/
+00000320: 646f 636b 6572 2d70 7562 6c69 7368 2e79  docker-publish.y
+00000330: 6d6c 223e 200a 2020 2020 3c69 6d67 2061  ml"> .    <img a
+00000340: 6c74 3d22 646f 636b 6572 2220 7372 633d  lt="docker" src=
+00000350: 2268 7474 7073 3a2f 2f67 6974 6875 622e  "https://github.
+00000360: 636f 6d2f 736b 7970 6c61 6e65 2d70 726f  com/skyplane-pro
+00000370: 6a65 6374 2f73 6b79 706c 616e 652f 6163  ject/skyplane/ac
+00000380: 7469 6f6e 732f 776f 726b 666c 6f77 732f  tions/workflows/
+00000390: 646f 636b 6572 2d70 7562 6c69 7368 2e79  docker-publish.y
+000003a0: 6d6c 2f62 6164 6765 2e73 7667 223e 0a20  ml/badge.svg">. 
+000003b0: 203c 2f61 3e0a 2020 0a20 203c 6120 6872   </a>.  .  <a hr
+000003c0: 6566 3d22 6874 7470 733a 2f2f 736b 7970  ef="https://skyp
+000003d0: 6c61 6e65 2e72 6561 6474 6865 646f 6373  lane.readthedocs
+000003e0: 2e69 6f2f 656e 2f6c 6174 6573 742f 3f62  .io/en/latest/?b
+000003f0: 6164 6765 3d6c 6174 6573 7422 3e20 0a20  adge=latest"> . 
+00000400: 2020 203c 696d 6720 616c 743d 2264 6f63     <img alt="doc
+00000410: 7322 2073 7263 3d22 6874 7470 733a 2f2f  s" src="https://
+00000420: 7265 6164 7468 6564 6f63 732e 6f72 672f  readthedocs.org/
+00000430: 7072 6f6a 6563 7473 2f73 6b79 706c 616e  projects/skyplan
+00000440: 652f 6261 6467 652f 3f76 6572 7369 6f6e  e/badge/?version
+00000450: 3d6c 6174 6573 7422 3e0a 2020 3c2f 613e  =latest">.  </a>
+00000460: 0a3c 2f70 3e0a 0a2a 2af0 9f94 a520 426c  .</p>..**.... Bl
+00000470: 617a 696e 6720 6661 7374 2062 756c 6b20  azing fast bulk 
+00000480: 6461 7461 2074 7261 6e73 6665 7273 2062  data transfers b
+00000490: 6574 7765 656e 2061 6e79 2063 6c6f 7564  etween any cloud
+000004a0: 20f0 9f94 a52a 2a0a 0a53 6b79 706c 616e   ....**..Skyplan
+000004b0: 6520 6973 2061 2074 6f6f 6c20 666f 7220  e is a tool for 
+000004c0: 626c 617a 696e 676c 7920 6661 7374 2062  blazingly fast b
+000004d0: 756c 6b20 6461 7461 2074 7261 6e73 6665  ulk data transfe
+000004e0: 7273 2062 6574 7765 656e 206f 626a 6563  rs between objec
+000004f0: 7420 7374 6f72 6573 2069 6e20 7468 6520  t stores in the 
+00000500: 636c 6f75 642e 2049 7420 7072 6f76 6973  cloud. It provis
+00000510: 696f 6e73 2061 2066 6c65 6574 206f 6620  ions a fleet of 
+00000520: 564d 7320 696e 2074 6865 2063 6c6f 7564  VMs in the cloud
+00000530: 2074 6f20 7472 616e 7366 6572 2064 6174   to transfer dat
+00000540: 6120 696e 2070 6172 616c 6c65 6c20 7768  a in parallel wh
+00000550: 696c 6520 7573 696e 6720 636f 6d70 7265  ile using compre
+00000560: 7373 696f 6e20 616e 6420 6261 6e64 7769  ssion and bandwi
+00000570: 6474 6820 7469 6572 696e 6720 746f 2072  dth tiering to r
+00000580: 6564 7563 6520 636f 7374 2e0a 0a53 6b79  educe cost...Sky
+00000590: 706c 616e 6520 6973 3a0a 312e 20f0 9f94  plane is:.1. ...
+000005a0: a520 426c 617a 696e 6720 6661 7374 2028  . Blazing fast (
+000005b0: 5b31 3130 7820 6661 7374 6572 2074 6861  [110x faster tha
+000005c0: 6e20 4157 5320 4461 7461 5379 6e63 5d28  n AWS DataSync](
+000005d0: 6874 7470 733a 2f2f 736b 7970 6c61 6e65  https://skyplane
+000005e0: 2e6f 7267 2f65 6e2f 6c61 7465 7374 2f62  .org/en/latest/b
+000005f0: 656e 6368 6d61 726b 2e68 746d 6c29 290a  enchmark.html)).
+00000600: 322e 20f0 9fa4 9120 4368 6561 7020 2834  2. .... Cheap (4
+00000610: 7820 6368 6561 7065 7220 7468 616e 2072  x cheaper than r
+00000620: 7379 6e63 290a 332e 20f0 9f8c 9020 556e  sync).3. .... Un
+00000630: 6976 6572 7361 6c20 2841 5753 2c20 417a  iversal (AWS, Az
+00000640: 7572 652c 2049 424d 2061 6e64 2047 4350  ure, IBM and GCP
+00000650: 290a 0a59 6f75 2063 616e 2075 7365 2053  )..You can use S
+00000660: 6b79 706c 616e 6520 746f 2074 7261 6e73  kyplane to trans
+00000670: 6665 7220 6461 7461 3a20 0a2a 2062 6574  fer data: .* bet
+00000680: 7765 656e 206f 626a 6563 7420 7374 6f72  ween object stor
+00000690: 6573 2077 6974 6869 6e20 6120 636c 6f75  es within a clou
+000006a0: 6420 7072 6f76 6964 6572 2028 652e 672e  d provider (e.g.
+000006b0: 2041 5753 2075 732d 6561 7374 2d31 2074   AWS us-east-1 t
+000006c0: 6f20 4157 5320 7573 2d77 6573 742d 3229  o AWS us-west-2)
+000006d0: 0a2a 2062 6574 7765 656e 206f 626a 6563  .* between objec
+000006e0: 7420 7374 6f72 6573 2061 6372 6f73 7320  t stores across 
+000006f0: 6d75 6c74 6970 6c65 2063 6c6f 7564 2070  multiple cloud p
+00000700: 726f 7669 6465 7273 2028 652e 672e 2041  roviders (e.g. A
+00000710: 5753 2075 732d 6561 7374 2d31 2074 6f20  WS us-east-1 to 
+00000720: 4743 5020 7573 2d63 656e 7472 616c 3129  GCP us-central1)
+00000730: 0a2a 2062 6574 7765 656e 206c 6f63 616c  .* between local
+00000740: 2073 746f 7261 6765 2061 6e64 2063 6c6f   storage and clo
+00000750: 7564 206f 626a 6563 7420 7374 6f72 6573  ud object stores
+00000760: 2028 6578 7065 7269 6d65 6e74 616c 290a   (experimental).
+00000770: 0a53 6b79 706c 616e 6520 6375 7272 656e  .Skyplane curren
+00000780: 746c 7920 7375 7070 6f72 7473 2074 6865  tly supports the
+00000790: 2066 6f6c 6c6f 7769 6e67 2073 6f75 7263   following sourc
+000007a0: 6520 616e 6420 6465 7374 696e 6174 696f  e and destinatio
+000007b0: 6e20 656e 6470 6f69 6e74 7320 2861 6e79  n endpoints (any
+000007c0: 2073 6f75 7263 6520 616e 6420 6465 7374   source and dest
+000007d0: 696e 6174 696f 6e20 6361 6e20 6265 2063  ination can be c
+000007e0: 6f6d 6269 6e65 6429 3a20 0a0a 7c20 456e  ombined): ..| En
+000007f0: 6470 6f69 6e74 2020 2020 2020 2020 2020  dpoint          
+00000800: 207c 2053 6f75 7263 6520 2020 2020 2020   | Source       
+00000810: 2020 2020 2020 7c20 4465 7374 696e 6174        | Destinat
+00000820: 696f 6e20 2020 2020 2020 207c 0a7c 2d2d  ion        |.|--
+00000830: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+00000840: 2d2d 7c2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  --|-------------
+00000850: 2d2d 2d2d 2d2d 2d7c 2d2d 2d2d 2d2d 2d2d  -------|--------
+00000860: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 7c0a 7c20  ------------|.| 
+00000870: 4157 5320 5333 2020 2020 2020 2020 2020  AWS S3          
+00000880: 2020 207c 203a 7768 6974 655f 6368 6563     | :white_chec
+00000890: 6b5f 6d61 726b 3a20 7c20 3a77 6869 7465  k_mark: | :white
+000008a0: 5f63 6865 636b 5f6d 6172 6b3a 207c 0a7c  _check_mark: |.|
+000008b0: 2047 6f6f 676c 6520 5374 6f72 6167 6520   Google Storage 
+000008c0: 2020 2020 7c20 3a77 6869 7465 5f63 6865      | :white_che
+000008d0: 636b 5f6d 6172 6b3a 207c 203a 7768 6974  ck_mark: | :whit
+000008e0: 655f 6368 6563 6b5f 6d61 726b 3a20 7c0a  e_check_mark: |.
+000008f0: 7c20 417a 7572 6520 426c 6f62 2053 746f  | Azure Blob Sto
+00000900: 7261 6765 207c 203a 7768 6974 655f 6368  rage | :white_ch
+00000910: 6563 6b5f 6d61 726b 3a20 7c20 3a77 6869  eck_mark: | :whi
+00000920: 7465 5f63 6865 636b 5f6d 6172 6b3a 207c  te_check_mark: |
+00000930: 0a7c 2049 424d 2043 6c6f 7564 204f 626a  .| IBM Cloud Obj
+00000940: 6563 7420 5374 6f72 6167 6520 7c20 3a77  ect Storage | :w
+00000950: 6869 7465 5f63 6865 636b 5f6d 6172 6b3a  hite_check_mark:
+00000960: 207c 203a 7768 6974 655f 6368 6563 6b5f   | :white_check_
+00000970: 6d61 726b 3a20 7c0a 7c20 4c6f 6361 6c20  mark: |.| Local 
+00000980: 4469 736b 2020 2020 2020 2020 207c 203a  Disk         | :
+00000990: 7768 6974 655f 6368 6563 6b5f 6d61 726b  white_check_mark
+000009a0: 3a20 7c20 2869 6e20 7072 6f67 7265 7373  : | (in progress
+000009b0: 2920 2020 2020 207c 0a0a 536b 7970 6c61  )      |..Skypla
+000009c0: 6e65 2069 7320 616e 2061 6374 6976 656c  ne is an activel
+000009d0: 7920 6465 7665 6c6f 7065 6420 7072 6f6a  y developed proj
+000009e0: 6563 742e 2049 7420 7769 6c6c 2068 6176  ect. It will hav
+000009f0: 6520 f09f 94aa 2053 4841 5250 2045 4447  e .... SHARP EDG
+00000a00: 4553 20f0 9f94 aa2e 2050 6c65 6173 6520  ES ..... Please 
+00000a10: 6669 6c65 2061 6e20 6973 7375 6520 6f72  file an issue or
+00000a20: 2061 736b 2074 6865 2063 6f6e 7472 6962   ask the contrib
+00000a30: 7574 6f72 7320 7669 6120 5b74 6865 2023  utors via [the #
+00000a40: 6865 6c70 2063 6861 6e6e 656c 206f 6e20  help channel on 
+00000a50: 6f75 7220 536c 6163 6b5d 2868 7474 7073  our Slack](https
+00000a60: 3a2f 2f6a 6f69 6e2e 736c 6163 6b2e 636f  ://join.slack.co
+00000a70: 6d2f 742f 736b 7970 6c61 6e65 776f 726b  m/t/skyplanework
+00000a80: 7370 6163 652f 7368 6172 6564 5f69 6e76  space/shared_inv
+00000a90: 6974 652f 7a74 2d31 6378 6d65 6463 7563  ite/zt-1cxmedcuc
+00000aa0: 2d47 7749 584c 4779 4854 794f 5945 4c71  -GwIXLGyHTyOYELq
+00000ab0: 374b 6f4f 6c36 5129 2069 6620 796f 7520  7KoOl6Q) if you 
+00000ac0: 656e 636f 756e 7465 7220 6275 6773 2e0a  encounter bugs..
+00000ad0: 0a23 2052 6573 6f75 7263 6573 200a 2d20  .# Resources .- 
+00000ae0: 5b51 7569 636b 7374 6172 745d 2823 7175  [Quickstart](#qu
+00000af0: 6963 6b73 7461 7274 290a 2d20 5b43 6f6e  ickstart).- [Con
+00000b00: 7472 6962 7574 696e 675d 2868 7474 7073  tributing](https
+00000b10: 3a2f 2f73 6b79 706c 616e 652e 6f72 672f  ://skyplane.org/
+00000b20: 656e 2f6c 6174 6573 742f 636f 6e74 7269  en/latest/contri
+00000b30: 6275 7469 6e67 2e68 746d 6c29 0a2d 205b  buting.html).- [
+00000b40: 526f 6164 6d61 705d 2868 7474 7073 3a2f  Roadmap](https:/
+00000b50: 2f73 6b79 706c 616e 652e 6f72 672f 656e  /skyplane.org/en
+00000b60: 2f6c 6174 6573 742f 726f 6164 6d61 702e  /latest/roadmap.
+00000b70: 6874 6d6c 290a 2d20 5b53 6c61 636b 2043  html).- [Slack C
+00000b80: 6f6d 6d75 6e69 7479 5d28 6874 7470 733a  ommunity](https:
+00000b90: 2f2f 6a6f 696e 2e73 6c61 636b 2e63 6f6d  //join.slack.com
+00000ba0: 2f74 2f73 6b79 706c 616e 6577 6f72 6b73  /t/skyplaneworks
+00000bb0: 7061 6365 2f73 6861 7265 645f 696e 7669  pace/shared_invi
+00000bc0: 7465 2f7a 742d 3163 786d 6564 6375 632d  te/zt-1cxmedcuc-
+00000bd0: 4777 4958 4c47 7948 5479 4f59 454c 7137  GwIXLGyHTyOYELq7
+00000be0: 4b6f 4f6c 3651 290a 0a23 2051 7569 636b  KoOl6Q)..# Quick
+00000bf0: 7374 6172 740a 0a23 2320 312e 2049 6e73  start..## 1. Ins
+00000c00: 7461 6c6c 6174 696f 6e0a 5765 2072 6563  tallation.We rec
+00000c10: 6f6d 6d65 6e64 2069 6e73 7461 6c6c 6174  ommend installat
+00000c20: 696f 6e20 6672 6f6d 2050 7950 693a 0a60  ion from PyPi:.`
+00000c30: 6060 0a24 2070 6970 2069 6e73 7461 6c6c  ``.$ pip install
+00000c40: 2022 736b 7970 6c61 6e65 5b61 7773 5d22   "skyplane[aws]"
+00000c50: 0a0a 2320 696e 7374 616c 6c20 7375 7070  ..# install supp
+00000c60: 6f72 7420 666f 7220 6f74 6865 7220 636c  ort for other cl
+00000c70: 6f75 6473 2061 7320 6e65 6564 6564 3a0a  ouds as needed:.
+00000c80: 0a23 2020 2024 2070 6970 2069 6e73 7461  .#   $ pip insta
+00000c90: 6c6c 2022 736b 7970 6c61 6e65 5b61 7a75  ll "skyplane[azu
+00000ca0: 7265 5d22 0a23 2020 2024 2070 6970 2069  re]".#   $ pip i
+00000cb0: 6e73 7461 6c6c 2022 736b 7970 6c61 6e65  nstall "skyplane
+00000cc0: 5b67 6370 5d22 0a23 2020 2024 2070 6970  [gcp]".#   $ pip
+00000cd0: 2069 6e73 7461 6c6c 2022 736b 7970 6c61   install "skypla
+00000ce0: 6e65 5b69 626d 636c 6f75 645d 220a 2320  ne[ibmcloud]".# 
+00000cf0: 2020 2420 7069 7020 696e 7374 616c 6c20    $ pip install 
+00000d00: 2273 6b79 706c 616e 655b 616c 6c5d 220a  "skyplane[all]".
+00000d10: 6060 600a 0a53 6b79 706c 616e 6520 7375  ```..Skyplane su
+00000d20: 7070 6f72 7473 2041 5753 2c20 417a 7572  pports AWS, Azur
+00000d30: 652c 2049 424d 2061 6e64 2047 4350 2e20  e, IBM and GCP. 
+00000d40: 596f 7520 6361 6e20 696e 7374 616c 6c20  You can install 
+00000d50: 536b 7970 6c61 6e65 2077 6974 6820 7375  Skyplane with su
+00000d60: 7070 6f72 7420 666f 7220 6f6e 6520 6f72  pport for one or
+00000d70: 206d 6f72 6520 6f66 2074 6865 7365 2063   more of these c
+00000d80: 6c6f 7564 7320 6279 2073 7065 6369 6679  louds by specify
+00000d90: 696e 6720 7468 6520 636f 7272 6573 706f  ing the correspo
+00000da0: 6e64 696e 6720 6578 7472 6173 2e20 546f  nding extras. To
+00000db0: 2069 6e73 7461 6c6c 2074 776f 206f 7574   install two out
+00000dc0: 206f 6620 7468 7265 6520 636c 6f75 6473   of three clouds
+00000dd0: 2c20 796f 7520 6361 6e20 7275 6e20 6070  , you can run `p
+00000de0: 6970 2069 6e73 7461 6c6c 2022 736b 7970  ip install "skyp
+00000df0: 6c61 6e65 5b61 7773 2c61 7a75 7265 5d22  lane[aws,azure]"
+00000e00: 602e 0a0a 2a47 4350 2073 7570 706f 7274  `...*GCP support
+00000e10: 206f 6e20 7468 6520 4d31 204d 6163 2a3a   on the M1 Mac*:
+00000e20: 2049 6620 796f 7520 6172 6520 7573 696e   If you are usin
+00000e30: 6720 616e 204d 3120 4d61 6320 7769 7468  g an M1 Mac with
+00000e40: 2074 6865 2061 726d 3634 2061 7263 6869   the arm64 archi
+00000e50: 7465 6374 7572 6520 616e 6420 7761 6e74  tecture and want
+00000e60: 2074 6f20 696e 7374 616c 6c20 4743 5020   to install GCP 
+00000e70: 7375 7070 6f72 7420 666f 7220 536b 7970  support for Skyp
+00000e80: 6c61 6e65 2c20 796f 7520 7769 6c6c 206e  lane, you will n
+00000e90: 6565 6420 746f 2069 6e73 7461 6c6c 2061  eed to install a
+00000ea0: 7320 666f 6c6c 6f77 730a 6047 5250 435f  s follows.`GRPC_
+00000eb0: 5059 5448 4f4e 5f42 5549 4c44 5f53 5953  PYTHON_BUILD_SYS
+00000ec0: 5445 4d5f 4f50 454e 5353 4c3d 3120 4752  TEM_OPENSSL=1 GR
+00000ed0: 5043 5f50 5954 484f 4e5f 4255 494c 445f  PC_PYTHON_BUILD_
+00000ee0: 5359 5354 454d 5f5a 4c49 423d 3120 7069  SYSTEM_ZLIB=1 pi
+00000ef0: 7020 696e 7374 616c 6c20 2273 6b79 706c  p install "skypl
+00000f00: 616e 655b 6177 732c 6763 705d 2260 0a0a  ane[aws,gcp]"`..
+00000f10: 2323 2032 2e20 5365 7475 7020 436c 6f75  ## 2. Setup Clou
+00000f20: 6420 4372 6564 656e 7469 616c 7320 0a0a  d Credentials ..
+00000f30: 536b 7970 6c61 6e65 206e 6565 6473 2061  Skyplane needs a
+00000f40: 6363 6573 7320 746f 2063 6c6f 7564 2063  ccess to cloud c
+00000f50: 7265 6465 6e74 6961 6c73 2074 6f20 7065  redentials to pe
+00000f60: 7266 6f72 6d20 7472 616e 7366 6572 732e  rform transfers.
+00000f70: 2054 6f20 6765 7420 7374 6172 7465 6420   To get started 
+00000f80: 7769 7468 2073 6574 7469 6e67 2075 7020  with setting up 
+00000f90: 6372 6564 656e 7469 616c 732c 206d 616b  credentials, mak
+00000fa0: 6520 7375 7265 2079 6f75 2068 6176 6520  e sure you have 
+00000fb0: 636c 6f75 6420 7072 6f76 6964 6572 2043  cloud provider C
+00000fc0: 4c49 2074 6f6f 6c73 2069 6e73 7461 6c6c  LI tools install
+00000fd0: 6564 3a0a 0a60 6060 0a2d 2d2d 3e20 466f  ed:..```.---> Fo
+00000fe0: 7220 4157 533a 0a24 2070 6970 2069 6e73  r AWS:.$ pip ins
+00000ff0: 7461 6c6c 2061 7773 636c 690a 0a2d 2d2d  tall awscli..---
+00001000: 3e20 466f 7220 476f 6f67 6c65 2043 6c6f  > For Google Clo
+00001010: 7564 3a0a 2420 7069 7020 696e 7374 616c  ud:.$ pip instal
+00001020: 6c20 6763 6c6f 7564 0a0a 2d2d 2d3e 2046  l gcloud..---> F
+00001030: 6f72 2041 7a75 7265 3a0a 2420 7069 7020  or Azure:.$ pip 
+00001040: 696e 7374 616c 6c20 617a 7572 650a 0a60  install azure..`
+00001050: 6060 0a4f 6e63 6520 796f 7520 6861 7665  ``.Once you have
+00001060: 2074 6865 2043 4c49 2074 6f6f 6c73 2073   the CLI tools s
+00001070: 6574 7570 2c20 6c6f 6720 696e 746f 2065  etup, log into e
+00001080: 6163 6820 636c 6f75 6420 7072 6f76 6964  ach cloud provid
+00001090: 6572 2773 2043 4c49 3a0a 6060 600a 2d2d  er's CLI:.```.--
+000010a0: 2d3e 2046 6f72 2041 5753 3a0a 2420 6177  -> For AWS:.$ aw
+000010b0: 7320 636f 6e66 6967 7572 650a 0a2d 2d2d  s configure..---
+000010c0: 3e20 466f 7220 476f 6f67 6c65 2043 6c6f  > For Google Clo
+000010d0: 7564 3a0a 2420 6763 6c6f 7564 2061 7574  ud:.$ gcloud aut
+000010e0: 6820 6170 706c 6963 6174 696f 6e2d 6465  h application-de
+000010f0: 6661 756c 7420 6c6f 6769 6e0a 0a2d 2d2d  fault login..---
+00001100: 3e20 466f 7220 417a 7572 653a 0a24 2061  > For Azure:.$ a
+00001110: 7a20 6c6f 6769 6e0a 0a2d 2d2d 3e20 466f  z login..---> Fo
+00001120: 7220 4942 4d20 436c 6f75 643a 0a24 2046  r IBM Cloud:.$ F
+00001130: 6f6c 6c6f 7720 4942 4d20 436c 6f75 6420  ollow IBM Cloud 
+00001140: 616e 6420 6372 6561 7465 2061 6e20 6163  and create an ac
+00001150: 636f 756e 7420 7769 7468 2074 6865 2072  count with the r
+00001160: 6573 6f75 7263 6520 6772 6f75 702e 0a43  esource group..C
+00001170: 6f70 7920 6874 7470 733a 2f2f 6769 7468  opy https://gith
+00001180: 7562 2e63 6f6d 2f73 6b79 706c 616e 652d  ub.com/skyplane-
+00001190: 7072 6f6a 6563 742f 736b 7970 6c61 6e65  project/skyplane
+000011a0: 2f62 6c6f 622f 6d61 696e 2f73 6b79 706c  /blob/main/skypl
+000011b0: 616e 652f 636f 6d70 7574 652f 6962 6d63  ane/compute/ibmc
+000011c0: 6c6f 7564 2f69 626d 5f63 7265 6465 6e74  loud/ibm_credent
+000011d0: 6961 6c73 2e79 616d 6c2e 7465 6d70 6c61  ials.yaml.templa
+000011e0: 7465 0a69 6e74 6f20 607e 2f2e 626c 7565  te.into `~/.blue
+000011f0: 6d69 782f 6962 6d5f 6372 6564 656e 7469  mix/ibm_credenti
+00001200: 616c 7360 2061 6e64 2066 696c 6c20 796f  als` and fill yo
+00001210: 7572 200a 4942 4d20 4941 4d20 6b65 7920  ur .IBM IAM key 
+00001220: 616e 6420 6372 6564 656e 7469 616c 7320  and credentials 
+00001230: 746f 2079 6f75 7220 4942 4d20 436c 6f75  to your IBM Clou
+00001240: 6420 6f62 6a65 6374 2073 746f 7261 6765  d object storage
+00001250: 200a 0a0a 6060 600a 4166 7465 7220 6175   ...```.After au
+00001260: 7468 656e 7469 6361 7469 6e67 2077 6974  thenticating wit
+00001270: 6820 6561 6368 2063 6c6f 7564 2070 726f  h each cloud pro
+00001280: 7669 6465 722c 2079 6f75 2063 616e 2072  vider, you can r
+00001290: 756e 2060 736b 7970 6c61 6e65 2069 6e69  un `skyplane ini
+000012a0: 7460 2074 6f20 6372 6561 7465 2061 2063  t` to create a c
+000012b0: 6f6e 6669 6775 7261 7469 6f6e 2066 696c  onfiguration fil
+000012c0: 6520 666f 7220 536b 7970 6c61 6e65 2e0a  e for Skyplane..
+000012d0: 0a60 6060 6261 7368 0a24 2073 6b79 706c  .```bash.$ skypl
+000012e0: 616e 6520 696e 6974 0a60 6060 0a3c 6465  ane init.```.<de
+000012f0: 7461 696c 733e 0a3c 7375 6d6d 6172 793e  tails>.<summary>
+00001300: 736b 7970 6c61 6e65 2069 6e69 7420 6f75  skyplane init ou
+00001310: 7470 7574 3c2f 7375 6d6d 6172 793e 0a3c  tput</summary>.<
+00001320: 6272 3e0a 0a60 6060 0a24 2073 6b79 706c  br>..```.$ skypl
+00001330: 616e 6520 696e 6974 0a0a 3d3d 3d3d 3d3d  ane init..======
+00001340: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
+00001350: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
+00001360: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 0a20  ==============. 
+00001370: 5f5f 5f5f 5f20 5f20 2020 5f5f 5f5f 2020  _____ _   ____  
+00001380: 205f 5f5f 5f5f 5f5f 205f 2020 2020 2020   _______ _      
+00001390: 205f 5f5f 2020 205f 2020 205f 2020 5f5f   ___   _   _  __
+000013a0: 5f5f 5f0a 2f20 205f 5f5f 7c20 7c20 2f20  ___./  ___| | / 
+000013b0: 2f5c 205c 202f 202f 205f 5f5f 205c 207c  /\ \ / / ___ \ |
+000013c0: 2020 2020 202f 205f 205c 207c 205c 207c       / _ \ | \ |
+000013d0: 207c 7c20 205f 5f5f 7c0a 5c20 602d 2d2e   ||  ___|.\ `--.
+000013e0: 7c20 7c2f 202f 2020 5c20 5620 2f7c 207c  | |/ /  \ V /| |
+000013f0: 5f2f 202f 207c 2020 2020 2f20 2f5f 5c20  _/ / |    / /_\ 
+00001400: 5c7c 2020 5c7c 207c 7c20 7c5f 5f0a 2060  \|  \| || |__. `
+00001410: 2d2d 2e20 5c20 2020 205c 2020 205c 202f  --. \    \   \ /
+00001420: 207c 2020 5f5f 2f7c 207c 2020 2020 7c20   |  __/| |    | 
+00001430: 205f 2020 7c7c 202e 2060 207c 7c20 205f   _  || . ` ||  _
+00001440: 5f7c 0a2f 5c5f 5f2f 202f 207c 5c20 205c  _|./\__/ / |\  \
+00001450: 2020 7c20 7c20 7c20 7c20 2020 7c20 7c5f    | | | |   | |_
+00001460: 5f5f 5f7c 207c 207c 207c 7c20 7c5c 2020  ___| | | || |\  
+00001470: 7c7c 207c 5f5f 5f0a 5c5f 5f5f 5f2f 5c5f  || |___.\____/\_
+00001480: 7c20 5c5f 2f20 205c 5f2f 205c 5f7c 2020  | \_/  \_/ \_|  
+00001490: 205c 5f5f 5f5f 5f2f 5c5f 7c20 7c5f 2f5c   \_____/\_| |_/\
+000014a0: 5f7c 205c 5f2f 5c5f 5f5f 5f2f 0a3d 3d3d  _| \_/\____/.===
+000014b0: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
+000014c0: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
+000014d0: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
+000014e0: 3d0a 0a0a 2831 2920 436f 6e66 6967 7572  =...(1) Configur
+000014f0: 696e 6720 4157 533a 0a20 2020 204c 6f61  ing AWS:.    Loa
+00001500: 6465 6420 4157 5320 6372 6564 656e 7469  ded AWS credenti
+00001510: 616c 7320 6672 6f6d 2074 6865 2041 5753  als from the AWS
+00001520: 2043 4c49 205b 4941 4d20 6163 6365 7373   CLI [IAM access
+00001530: 206b 6579 2049 443a 202e 2e2e 5858 5858   key ID: ...XXXX
+00001540: 5858 5d0a 2020 2020 4157 5320 7265 6769  XX].    AWS regi
+00001550: 6f6e 2063 6f6e 6669 6720 6669 6c65 2073  on config file s
+00001560: 6176 6564 2074 6f20 2f68 6f6d 652f 7562  aved to /home/ub
+00001570: 756e 7475 2f2e 736b 7970 6c61 6e65 2f61  untu/.skyplane/a
+00001580: 7773 5f63 6f6e 6669 670a 0a28 3229 2043  ws_config..(2) C
+00001590: 6f6e 6669 6775 7269 6e67 2041 7a75 7265  onfiguring Azure
+000015a0: 3a0a 2020 2020 417a 7572 6520 6372 6564  :.    Azure cred
+000015b0: 656e 7469 616c 7320 666f 756e 6420 696e  entials found in
+000015c0: 2041 7a75 7265 2043 4c49 0a20 2020 2041   Azure CLI.    A
+000015d0: 7a75 7265 2063 7265 6465 6e74 6961 6c73  zure credentials
+000015e0: 2066 6f75 6e64 2c20 646f 2079 6f75 2077   found, do you w
+000015f0: 616e 7420 746f 2065 6e61 626c 6520 417a  ant to enable Az
+00001600: 7572 6520 7375 7070 6f72 7420 696e 2053  ure support in S
+00001610: 6b79 706c 616e 653f 205b 592f 6e5d 3a20  kyplane? [Y/n]: 
+00001620: 590a 2020 2020 456e 7465 7220 7468 6520  Y.    Enter the 
+00001630: 417a 7572 6520 7375 6273 6372 6970 7469  Azure subscripti
+00001640: 6f6e 2049 443a 205b 5858 5858 5858 5858  on ID: [XXXXXXXX
+00001650: 2d58 5858 582d 5858 5858 2d58 5858 582d  -XXXX-XXXX-XXXX-
+00001660: 5858 5858 5858 5858 5858 5858 5d3a 0a20  XXXXXXXXXXXX]:. 
+00001670: 2020 2041 7a75 7265 2072 6567 696f 6e20     Azure region 
+00001680: 636f 6e66 6967 2066 696c 6520 7361 7665  config file save
+00001690: 6420 746f 202f 686f 6d65 2f75 6275 6e74  d to /home/ubunt
+000016a0: 752f 2e73 6b79 706c 616e 652f 617a 7572  u/.skyplane/azur
+000016b0: 655f 636f 6e66 6967 0a20 2020 2051 7565  e_config.    Que
+000016c0: 7279 696e 6720 666f 7220 534b 5520 6176  rying for SKU av
+000016d0: 6169 6c62 696c 6974 7920 696e 2072 6567  ailbility in reg
+000016e0: 696f 6e73 0a20 2020 2041 7a75 7265 2053  ions.    Azure S
+000016f0: 4b55 2061 7661 696c 6162 696c 6974 7920  KU availability 
+00001700: 6361 6368 6564 2069 6e20 2f68 6f6d 652f  cached in /home/
+00001710: 7562 756e 7475 2f2e 736b 7970 6c61 6e65  ubuntu/.skyplane
+00001720: 2f61 7a75 7265 5f73 6b75 5f6d 6170 7069  /azure_sku_mappi
+00001730: 6e67 0a0a 2833 2920 436f 6e66 6967 7572  ng..(3) Configur
+00001740: 696e 6720 4743 503a 0a20 2020 2047 4350  ing GCP:.    GCP
+00001750: 2063 7265 6465 6e74 6961 6c73 2066 6f75   credentials fou
+00001760: 6e64 2069 6e20 4743 5020 434c 490a 2020  nd in GCP CLI.  
+00001770: 2020 4743 5020 6372 6564 656e 7469 616c    GCP credential
+00001780: 7320 666f 756e 642c 2064 6f20 796f 7520  s found, do you 
+00001790: 7761 6e74 2074 6f20 656e 6162 6c65 2047  want to enable G
+000017a0: 4350 2073 7570 706f 7274 2069 6e20 536b  CP support in Sk
+000017b0: 7970 6c61 6e65 3f20 5b59 2f6e 5d3a 2059  yplane? [Y/n]: Y
+000017c0: 0a20 2020 2045 6e74 6572 2074 6865 2047  .    Enter the G
+000017d0: 4350 2070 726f 6a65 6374 2049 4420 5b58  CP project ID [X
+000017e0: 5858 5858 5858 5d3a 0a20 2020 2047 4350  XXXXXX]:.    GCP
+000017f0: 2072 6567 696f 6e20 636f 6e66 6967 2066   region config f
+00001800: 696c 6520 7361 7665 6420 746f 202f 686f  ile saved to /ho
+00001810: 6d65 2f75 6275 6e74 752f 2e73 6b79 706c  me/ubuntu/.skypl
+00001820: 616e 652f 6763 705f 636f 6e66 6967 0a0a  ane/gcp_config..
+00001830: 436f 6e66 6967 2066 696c 6520 7361 7665  Config file save
+00001840: 6420 746f 202f 686f 6d65 2f75 6275 6e74  d to /home/ubunt
+00001850: 752f 2e73 6b79 706c 616e 652f 636f 6e66  u/.skyplane/conf
+00001860: 6967 0a60 6060 0a0a 3c2f 6465 7461 696c  ig.```..</detail
+00001870: 733e 0a0a 2323 2033 2e20 5275 6e20 5472  s>..## 3. Run Tr
+00001880: 616e 7366 6572 7320 0a0a 5765 e280 9972  ansfers ..We...r
+00001890: 6520 7265 6164 7920 746f 2075 7365 2053  e ready to use S
+000018a0: 6b79 706c 616e 6521 204c 6574 e280 9973  kyplane! Let...s
+000018b0: 2075 7365 2060 736b 7970 6c61 6e65 2063   use `skyplane c
+000018c0: 7060 2074 6f20 636f 7079 2066 696c 6573  p` to copy files
+000018d0: 2066 726f 6d20 4157 5320 746f 2047 4350   from AWS to GCP
+000018e0: 3a0a 6060 600a 736b 7970 6c61 6e65 2063  :.```.skyplane c
+000018f0: 7020 7333 3a2f 2f2e 2e2e 2067 733a 2f2f  p s3://... gs://
+00001900: 2e2e 2e0a 6060 600a 546f 2074 7261 6e73  ....```.To trans
+00001910: 6665 7220 6f6e 6c79 206e 6577 206f 626a  fer only new obj
+00001920: 6563 7473 2c20 796f 7520 6361 6e20 696e  ects, you can in
+00001930: 7374 6561 6420 7573 6520 6073 6b79 706c  stead use `skypl
+00001940: 616e 6520 7379 6e63 603a 0a60 6060 0a24  ane sync`:.```.$
+00001950: 2073 6b79 706c 616e 6520 7379 6e63 2073   skyplane sync s
+00001960: 333a 2f2f 2e2e 2e20 6773 3a2f 2f2e 2e2e  3://... gs://...
+00001970: 0a60 6060 0a0a 596f 7520 6361 6e20 636f  .```..You can co
+00001980: 6e66 6967 7572 6520 536b 7970 6c61 6e65  nfigure Skyplane
+00001990: 2074 6f20 7573 6520 6d6f 7265 2056 4d73   to use more VMs
+000019a0: 2070 6572 2072 6567 696f 6e20 7769 7468   per region with
+000019b0: 2074 6865 2060 2d6e 6020 666c 6167 2e20   the `-n` flag. 
+000019c0: 466f 7220 6578 616d 706c 652c 2074 6f20  For example, to 
+000019d0: 646f 7562 6c65 2074 6865 2074 7261 6e73  double the trans
+000019e0: 6665 7220 7370 6565 6420 7769 7468 2074  fer speed with t
+000019f0: 776f 2056 4d73 2c20 7275 6e3a 200a 6060  wo VMs, run: .``
+00001a00: 600a 2420 736b 7970 6c61 6e65 2063 7020  `.$ skyplane cp 
+00001a10: 2d72 2073 333a 2f2f 2e2e 2e20 7333 3a2f  -r s3://... s3:/
+00001a20: 2f2e 2e2e 202d 6e20 320a 6060 600a 0a23  /... -n 2.```..#
+00001a30: 2320 342e 2043 6c65 616e 2055 7020 0a53  # 4. Clean Up .S
+00001a40: 6b79 706c 616e 6520 7769 6c6c 2061 7574  kyplane will aut
+00001a50: 6f6d 6174 6963 616c 6c79 2061 7474 656d  omatically attem
+00001a60: 7074 2074 6f20 7465 726d 696e 6174 6520  pt to terminate 
+00001a70: 564d 7320 7468 6174 2069 7420 7374 6172  VMs that it star
+00001a80: 7473 2c20 6275 7420 746f 2064 6f75 626c  ts, but to doubl
+00001a90: 6520 6368 6563 6b20 616e 6420 666f 7263  e check and forc
+00001aa0: 6566 756c 7920 7465 726d 696e 6174 6520  efuly terminate 
+00001ab0: 616c 6c20 564d 732c 2072 756e 2060 736b  all VMs, run `sk
+00001ac0: 7970 6c61 6e65 2064 6570 726f 7669 7369  yplane deprovisi
+00001ad0: 6f6e 602e 0a0a 2320 5465 6368 6e69 6361  on`...# Technica
+00001ae0: 6c20 4465 7461 696c 730a 536b 7970 6c61  l Details.Skypla
+00001af0: 6e65 2069 7320 6261 7365 6420 6f6e 2072  ne is based on r
+00001b00: 6573 6561 7263 6820 6174 2055 4320 4265  esearch at UC Be
+00001b10: 726b 656c 6579 2069 6e74 6f20 6163 6365  rkeley into acce
+00001b20: 6c65 7261 7465 6420 6e65 7477 6f72 6b73  lerated networks
+00001b30: 2062 6574 7765 656e 2063 6c6f 7564 2070   between cloud p
+00001b40: 726f 7669 6465 7273 2e20 556e 6465 7220  roviders. Under 
+00001b50: 7468 6520 686f 6f64 2c20 536b 7970 6c61  the hood, Skypla
+00001b60: 6e65 2073 7461 7274 7320 6120 666c 6565  ne starts a flee
+00001b70: 7420 6f66 2056 4d73 2069 6e20 7468 6520  t of VMs in the 
+00001b80: 736f 7572 6365 2061 6e64 2064 6573 7469  source and desti
+00001b90: 6e61 7469 6f6e 2072 6567 696f 6e73 2e20  nation regions. 
+00001ba0: 4974 2074 6865 6e20 7573 6573 2061 2063  It then uses a c
+00001bb0: 7573 746f 6d20 5443 5020 7072 6f74 6f63  ustom TCP protoc
+00001bc0: 6f6c 2074 6f20 6163 6365 6c65 7261 7465  ol to accelerate
+00001bd0: 2074 6865 2074 7261 6e73 6665 7220 6265   the transfer be
+00001be0: 7477 6565 6e20 7468 6520 564d 732e 2053  tween the VMs. S
+00001bf0: 6b79 706c 616e 6520 6d61 7920 7573 6520  kyplane may use 
+00001c00: 6120 4c37 206f 7665 726c 6179 206e 6574  a L7 overlay net
+00001c10: 776f 726b 2074 6f20 726f 7574 6520 7472  work to route tr
+00001c20: 6166 6669 6320 6172 6f75 6e64 2063 6f6e  affic around con
+00001c30: 6765 7374 6564 206e 6574 776f 726b 2068  gested network h
+00001c40: 6f74 2073 706f 7473 2e20 0a0a 3c69 6d67  ot spots. ..<img
+00001c50: 2073 7263 3d22 646f 6373 2f5f 7374 6174   src="docs/_stat
+00001c60: 6963 2f73 6b79 706c 616e 652d 6461 7461  ic/skyplane-data
+00001c70: 2d70 6c61 6e65 2e70 6e67 2220 7769 6474  -plane.png" widt
+00001c80: 683d 2233 3834 2220 2f3e 0a0a 466f 7220  h="384" />..For 
+00001c90: 6d6f 7265 2064 6574 6169 6c73 206f 6e20  more details on 
+00001ca0: 536b 7970 6c61 6e65 2c20 7365 653a 200a  Skyplane, see: .
+00001cb0: 2d20 5b54 6563 686e 6963 616c 2054 616c  - [Technical Tal
+00001cc0: 6b5d 2868 7474 7073 3a2f 2f73 6b79 706c  k](https://skypl
+00001cd0: 616e 652e 6f72 672f 656e 2f6c 6174 6573  ane.org/en/lates
+00001ce0: 742f 6172 6368 6974 6563 7475 7265 2e68  t/architecture.h
+00001cf0: 746d 6c29 0a2d 205b 4e53 4449 2027 3233  tml).- [NSDI '23
+00001d00: 2050 6170 6572 5d28 6874 7470 733a 2f2f   Paper](https://
+00001d10: 6172 7869 762e 6f72 672f 6162 732f 3232  arxiv.org/abs/22
+00001d20: 3130 2e30 3732 3539 290a 0a0a            10.07259)...
```

### Comparing `skyplane_nightly-0.3.2.dev20230720/pyproject.toml` & `skyplane_nightly-0.3.2.dev20230721/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool.poetry]
 name = "skyplane-nightly"
 packages = [{ include = "skyplane" }]
-version = "0.3.2.dev20230720"
+version = "0.3.2.dev20230721"
 description = "Skyplane efficiently transports data between cloud regions and providers."
 authors = ["Skyplane authors <skyplaneproject@gmail.com>"]
 license = "Apache-2.0"
 homepage = "https://skyplane.org/"
 repository = "https://github.com/skyplane-project/skyplane"
 documentation = "https://skyplane.org/"
 readme = "README.md"
```

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/__init__.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/__init__.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/api/client.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/api/client.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/api/config.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/api/config.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/api/dataplane.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/api/dataplane.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/api/obj_store.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/api/obj_store.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/api/pipeline.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/api/pipeline.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/api/provisioner.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/api/provisioner.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/api/tracker.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/api/tracker.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/api/transfer_job.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/api/transfer_job.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/api/usage.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/api/usage.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/chunk.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/chunk.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli_cloud.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli_cloud.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli_config.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli_config.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli_init.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli_init.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/cli_transfer.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/cli_transfer.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/experiments/cli_profile.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/experiments/cli_profile.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/experiments/cli_query.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/experiments/cli_query.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/experiments/provision.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/experiments/provision.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/impl/common.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/impl/common.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/impl/cp_replicate_fallback.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/impl/cp_replicate_fallback.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/cli/impl/progress_bar.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/cli/impl/progress_bar.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/__init__.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/__init__.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_auth.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_auth.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_cloud_provider.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_cloud_provider.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_key_manager.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_key_manager.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_network.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_network.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_pricing.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_pricing.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/aws/aws_server.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/aws/aws_server.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/azure/azure_auth.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/azure/azure_auth.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/azure/azure_cloud_provider.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/azure/azure_cloud_provider.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/azure/azure_server.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/azure/azure_server.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/cloud_provider.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/cloud_provider.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/const_cmds.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/const_cmds.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_auth.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_auth.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_cloud_provider.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_cloud_provider.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_key_manager.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_key_manager.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_network.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_network.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_pricing.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_pricing.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/gcp/gcp_server.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/gcp/gcp_server.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/config.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/config.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/constants.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/constants.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/ssh_client.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/ssh_client.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/utils.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/utils.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibm_gen2/vpc_backend.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibm_gen2/vpc_backend.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibmcloud_auth.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibmcloud_auth.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibmcloud_provider.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibmcloud_provider.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/ibmcloud/ibmcloud_server.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/ibmcloud/ibmcloud_server.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/key_utils.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/key_utils.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/compute/server.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/compute/server.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/config.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/config.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/config_paths.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/config_paths.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/data/aws_transfer_costs.csv` & `skyplane_nightly-0.3.2.dev20230721/skyplane/data/aws_transfer_costs.csv`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/data/vcpu_info.csv` & `skyplane_nightly-0.3.2.dev20230721/skyplane/data/vcpu_info.csv`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/exceptions.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/exceptions.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/cert.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/cert.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/chunk_store.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/chunk_store.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_daemon.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_daemon.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_daemon_api.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_daemon_api.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_onprem.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_onprem.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_program.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_program.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/gateway_queue.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/gateway_queue.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/operators/gateway_operator.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/operators/gateway_operator.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/gateway/operators/gateway_receiver.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/gateway/operators/gateway_receiver.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/azure_blob_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/azure_blob_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/azure_storage_account_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/azure_storage_account_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/cos_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/cos_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/file_system_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/file_system_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/gcs_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/gcs_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/hdfs_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/hdfs_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/object_store_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/object_store_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/posix_file_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/posix_file_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/r2_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/r2_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/s3_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/s3_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/obj_store/storage_interface.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/obj_store/storage_interface.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/planner/planner.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/planner/planner.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/planner/solver.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/planner/solver.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/planner/solver_ilp.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/planner/solver_ilp.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/planner/solver_ron.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/planner/solver_ron.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/planner/topology.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/planner/topology.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/cache.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/cache.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/definitions.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/definitions.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/fn.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/fn.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/generator.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/generator.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/imports.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/imports.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/logger.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/logger.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/networking_tools.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/networking_tools.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/path.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/path.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/retry.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/retry.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/skyplane/utils/timer.py` & `skyplane_nightly-0.3.2.dev20230721/skyplane/utils/timer.py`

 * *Files identical despite different names*

### Comparing `skyplane_nightly-0.3.2.dev20230720/PKG-INFO` & `skyplane_nightly-0.3.2.dev20230721/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 00000000: 4d65 7461 6461 7461 2d56 6572 7369 6f6e  Metadata-Version
 00000010: 3a20 322e 310a 4e61 6d65 3a20 736b 7970  : 2.1.Name: skyp
 00000020: 6c61 6e65 2d6e 6967 6874 6c79 0a56 6572  lane-nightly.Ver
 00000030: 7369 6f6e 3a20 302e 332e 322e 6465 7632  sion: 0.3.2.dev2
-00000040: 3032 3330 3732 300a 5375 6d6d 6172 793a  0230720.Summary:
+00000040: 3032 3330 3732 310a 5375 6d6d 6172 793a  0230721.Summary:
 00000050: 2053 6b79 706c 616e 6520 6566 6669 6369   Skyplane effici
 00000060: 656e 746c 7920 7472 616e 7370 6f72 7473  ently transports
 00000070: 2064 6174 6120 6265 7477 6565 6e20 636c   data between cl
 00000080: 6f75 6420 7265 6769 6f6e 7320 616e 6420  oud regions and 
 00000090: 7072 6f76 6964 6572 732e 0a48 6f6d 652d  providers..Home-
 000000a0: 7061 6765 3a20 6874 7470 733a 2f2f 736b  page: https://sk
 000000b0: 7970 6c61 6e65 2e6f 7267 2f0a 4c69 6365  yplane.org/.Lice
@@ -198,459 +198,475 @@
 00000c50: 6e65 2e6f 7267 2f0a 5072 6f6a 6563 742d  ne.org/.Project-
 00000c60: 5552 4c3a 2052 6570 6f73 6974 6f72 792c  URL: Repository,
 00000c70: 2068 7474 7073 3a2f 2f67 6974 6875 622e   https://github.
 00000c80: 636f 6d2f 736b 7970 6c61 6e65 2d70 726f  com/skyplane-pro
 00000c90: 6a65 6374 2f73 6b79 706c 616e 650a 4465  ject/skyplane.De
 00000ca0: 7363 7269 7074 696f 6e2d 436f 6e74 656e  scription-Conten
 00000cb0: 742d 5479 7065 3a20 7465 7874 2f6d 6172  t-Type: text/mar
-00000cc0: 6b64 6f77 6e0a 0a3c 7069 6374 7572 653e  kdown..<picture>
-00000cd0: 0a20 2020 203c 736f 7572 6365 2073 7263  .    <source src
-00000ce0: 7365 743d 2264 6f63 732f 5f73 7461 7469  set="docs/_stati
-00000cf0: 632f 6c6f 676f 2d64 6172 6b2d 6d6f 6465  c/logo-dark-mode
-00000d00: 2e70 6e67 2220 6d65 6469 613d 2228 7072  .png" media="(pr
-00000d10: 6566 6572 732d 636f 6c6f 722d 7363 6865  efers-color-sche
-00000d20: 6d65 3a20 6461 726b 2922 3e0a 2020 2020  me: dark)">.    
-00000d30: 3c69 6d67 2073 7263 3d22 646f 6373 2f5f  <img src="docs/_
-00000d40: 7374 6174 6963 2f6c 6f67 6f2d 6c69 6768  static/logo-ligh
-00000d50: 742d 6d6f 6465 2e70 6e67 2220 7769 6474  t-mode.png" widt
-00000d60: 683d 2233 3030 2220 2f3e 0a3c 2f70 6963  h="300" />.</pic
-00000d70: 7475 7265 3e0a 0a5b 215b 4a6f 696e 2053  ture>..[![Join S
-00000d80: 6c61 636b 5d28 6874 7470 733a 2f2f 696d  lack](https://im
-00000d90: 672e 7368 6965 6c64 732e 696f 2f62 6164  g.shields.io/bad
-00000da0: 6765 2f2d 4a6f 696e 2532 3053 6b79 706c  ge/-Join%20Skypl
-00000db0: 616e 6525 3230 536c 6163 6b2d 626c 7565  ane%20Slack-blue
-00000dc0: 3f6c 6f67 6f3d 736c 6163 6b29 5d28 6874  ?logo=slack)](ht
-00000dd0: 7470 733a 2f2f 6a6f 696e 2e73 6c61 636b  tps://join.slack
-00000de0: 2e63 6f6d 2f74 2f73 6b79 706c 616e 6577  .com/t/skyplanew
-00000df0: 6f72 6b73 7061 6365 2f73 6861 7265 645f  orkspace/shared_
-00000e00: 696e 7669 7465 2f7a 742d 3163 786d 6564  invite/zt-1cxmed
-00000e10: 6375 632d 4777 4958 4c47 7948 5479 4f59  cuc-GwIXLGyHTyOY
-00000e20: 454c 7137 4b6f 4f6c 3651 290a 5b21 5b69  ELq7KoOl6Q).[![i
-00000e30: 6e74 6567 7261 7469 6f6e 2d74 6573 745d  ntegration-test]
-00000e40: 2868 7474 7073 3a2f 2f67 6974 6875 622e  (https://github.
-00000e50: 636f 6d2f 736b 7970 6c61 6e65 2d70 726f  com/skyplane-pro
-00000e60: 6a65 6374 2f73 6b79 706c 616e 652f 6163  ject/skyplane/ac
-00000e70: 7469 6f6e 732f 776f 726b 666c 6f77 732f  tions/workflows/
-00000e80: 696e 7465 6772 6174 696f 6e2d 7465 7374  integration-test
-00000e90: 2e79 6d6c 2f62 6164 6765 2e73 7667 295d  .yml/badge.svg)]
-00000ea0: 2868 7474 7073 3a2f 2f67 6974 6875 622e  (https://github.
-00000eb0: 636f 6d2f 736b 7970 6c61 6e65 2d70 726f  com/skyplane-pro
-00000ec0: 6a65 6374 2f73 6b79 706c 616e 652f 6163  ject/skyplane/ac
-00000ed0: 7469 6f6e 732f 776f 726b 666c 6f77 732f  tions/workflows/
-00000ee0: 696e 7465 6772 6174 696f 6e2d 7465 7374  integration-test
-00000ef0: 2e79 6d6c 290a 5b21 5b64 6f63 6b65 725d  .yml).[![docker]
-00000f00: 2868 7474 7073 3a2f 2f67 6974 6875 622e  (https://github.
-00000f10: 636f 6d2f 736b 7970 6c61 6e65 2d70 726f  com/skyplane-pro
-00000f20: 6a65 6374 2f73 6b79 706c 616e 652f 6163  ject/skyplane/ac
-00000f30: 7469 6f6e 732f 776f 726b 666c 6f77 732f  tions/workflows/
-00000f40: 646f 636b 6572 2d70 7562 6c69 7368 2e79  docker-publish.y
-00000f50: 6d6c 2f62 6164 6765 2e73 7667 295d 2868  ml/badge.svg)](h
-00000f60: 7474 7073 3a2f 2f67 6974 6875 622e 636f  ttps://github.co
-00000f70: 6d2f 736b 7970 6c61 6e65 2d70 726f 6a65  m/skyplane-proje
-00000f80: 6374 2f73 6b79 706c 616e 652f 6163 7469  ct/skyplane/acti
-00000f90: 6f6e 732f 776f 726b 666c 6f77 732f 646f  ons/workflows/do
-00000fa0: 636b 6572 2d70 7562 6c69 7368 2e79 6d6c  cker-publish.yml
-00000fb0: 290a 5b21 5b64 6f63 735d 2868 7474 7073  ).[![docs](https
-00000fc0: 3a2f 2f72 6561 6474 6865 646f 6373 2e6f  ://readthedocs.o
-00000fd0: 7267 2f70 726f 6a65 6374 732f 736b 7970  rg/projects/skyp
-00000fe0: 6c61 6e65 2f62 6164 6765 2f3f 7665 7273  lane/badge/?vers
-00000ff0: 696f 6e3d 6c61 7465 7374 295d 2868 7474  ion=latest)](htt
-00001000: 7073 3a2f 2f73 6b79 706c 616e 652e 7265  ps://skyplane.re
-00001010: 6164 7468 6564 6f63 732e 696f 2f65 6e2f  adthedocs.io/en/
-00001020: 6c61 7465 7374 2f3f 6261 6467 653d 6c61  latest/?badge=la
-00001030: 7465 7374 290a 0a2a 2af0 9f94 a520 426c  test)..**.... Bl
-00001040: 617a 696e 6720 6661 7374 2062 756c 6b20  azing fast bulk 
-00001050: 6461 7461 2074 7261 6e73 6665 7273 2062  data transfers b
-00001060: 6574 7765 656e 2061 6e79 2063 6c6f 7564  etween any cloud
-00001070: 20f0 9f94 a52a 2a0a 0a53 6b79 706c 616e   ....**..Skyplan
-00001080: 6520 6973 2061 2074 6f6f 6c20 666f 7220  e is a tool for 
-00001090: 626c 617a 696e 676c 7920 6661 7374 2062  blazingly fast b
-000010a0: 756c 6b20 6461 7461 2074 7261 6e73 6665  ulk data transfe
-000010b0: 7273 2062 6574 7765 656e 206f 626a 6563  rs between objec
-000010c0: 7420 7374 6f72 6573 2069 6e20 7468 6520  t stores in the 
-000010d0: 636c 6f75 642e 2049 7420 7072 6f76 6973  cloud. It provis
-000010e0: 696f 6e73 2061 2066 6c65 6574 206f 6620  ions a fleet of 
-000010f0: 564d 7320 696e 2074 6865 2063 6c6f 7564  VMs in the cloud
-00001100: 2074 6f20 7472 616e 7366 6572 2064 6174   to transfer dat
-00001110: 6120 696e 2070 6172 616c 6c65 6c20 7768  a in parallel wh
-00001120: 696c 6520 7573 696e 6720 636f 6d70 7265  ile using compre
-00001130: 7373 696f 6e20 616e 6420 6261 6e64 7769  ssion and bandwi
-00001140: 6474 6820 7469 6572 696e 6720 746f 2072  dth tiering to r
-00001150: 6564 7563 6520 636f 7374 2e0a 0a53 6b79  educe cost...Sky
-00001160: 706c 616e 6520 6973 3a0a 312e 20f0 9f94  plane is:.1. ...
-00001170: a520 426c 617a 696e 6720 6661 7374 2028  . Blazing fast (
-00001180: 5b31 3130 7820 6661 7374 6572 2074 6861  [110x faster tha
-00001190: 6e20 4157 5320 4461 7461 5379 6e63 5d28  n AWS DataSync](
-000011a0: 6874 7470 733a 2f2f 736b 7970 6c61 6e65  https://skyplane
-000011b0: 2e6f 7267 2f65 6e2f 6c61 7465 7374 2f62  .org/en/latest/b
-000011c0: 656e 6368 6d61 726b 2e68 746d 6c29 290a  enchmark.html)).
-000011d0: 322e 20f0 9fa4 9120 4368 6561 7020 2834  2. .... Cheap (4
-000011e0: 7820 6368 6561 7065 7220 7468 616e 2072  x cheaper than r
-000011f0: 7379 6e63 290a 332e 20f0 9f8c 9020 556e  sync).3. .... Un
-00001200: 6976 6572 7361 6c20 2841 5753 2c20 417a  iversal (AWS, Az
-00001210: 7572 652c 2049 424d 2061 6e64 2047 4350  ure, IBM and GCP
-00001220: 290a 0a59 6f75 2063 616e 2075 7365 2053  )..You can use S
-00001230: 6b79 706c 616e 6520 746f 2074 7261 6e73  kyplane to trans
-00001240: 6665 7220 6461 7461 3a20 0a2a 2062 6574  fer data: .* bet
-00001250: 7765 656e 206f 626a 6563 7420 7374 6f72  ween object stor
-00001260: 6573 2077 6974 6869 6e20 6120 636c 6f75  es within a clou
-00001270: 6420 7072 6f76 6964 6572 2028 652e 672e  d provider (e.g.
-00001280: 2041 5753 2075 732d 6561 7374 2d31 2074   AWS us-east-1 t
-00001290: 6f20 4157 5320 7573 2d77 6573 742d 3229  o AWS us-west-2)
-000012a0: 0a2a 2062 6574 7765 656e 206f 626a 6563  .* between objec
-000012b0: 7420 7374 6f72 6573 2061 6372 6f73 7320  t stores across 
-000012c0: 6d75 6c74 6970 6c65 2063 6c6f 7564 2070  multiple cloud p
-000012d0: 726f 7669 6465 7273 2028 652e 672e 2041  roviders (e.g. A
-000012e0: 5753 2075 732d 6561 7374 2d31 2074 6f20  WS us-east-1 to 
-000012f0: 4743 5020 7573 2d63 656e 7472 616c 3129  GCP us-central1)
-00001300: 0a2a 2062 6574 7765 656e 206c 6f63 616c  .* between local
-00001310: 2073 746f 7261 6765 2061 6e64 2063 6c6f   storage and clo
-00001320: 7564 206f 626a 6563 7420 7374 6f72 6573  ud object stores
-00001330: 2028 6578 7065 7269 6d65 6e74 616c 290a   (experimental).
-00001340: 0a53 6b79 706c 616e 6520 6375 7272 656e  .Skyplane curren
-00001350: 746c 7920 7375 7070 6f72 7473 2074 6865  tly supports the
-00001360: 2066 6f6c 6c6f 7769 6e67 2073 6f75 7263   following sourc
-00001370: 6520 616e 6420 6465 7374 696e 6174 696f  e and destinatio
-00001380: 6e20 656e 6470 6f69 6e74 7320 2861 6e79  n endpoints (any
-00001390: 2073 6f75 7263 6520 616e 6420 6465 7374   source and dest
-000013a0: 696e 6174 696f 6e20 6361 6e20 6265 2063  ination can be c
-000013b0: 6f6d 6269 6e65 6429 3a20 0a0a 7c20 456e  ombined): ..| En
-000013c0: 6470 6f69 6e74 2020 2020 2020 2020 2020  dpoint          
-000013d0: 207c 2053 6f75 7263 6520 2020 2020 2020   | Source       
-000013e0: 2020 2020 2020 7c20 4465 7374 696e 6174        | Destinat
-000013f0: 696f 6e20 2020 2020 2020 207c 0a7c 2d2d  ion        |.|--
-00001400: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
-00001410: 2d2d 7c2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  --|-------------
-00001420: 2d2d 2d2d 2d2d 2d7c 2d2d 2d2d 2d2d 2d2d  -------|--------
-00001430: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 7c0a 7c20  ------------|.| 
-00001440: 4157 5320 5333 2020 2020 2020 2020 2020  AWS S3          
-00001450: 2020 207c 203a 7768 6974 655f 6368 6563     | :white_chec
-00001460: 6b5f 6d61 726b 3a20 7c20 3a77 6869 7465  k_mark: | :white
-00001470: 5f63 6865 636b 5f6d 6172 6b3a 207c 0a7c  _check_mark: |.|
-00001480: 2047 6f6f 676c 6520 5374 6f72 6167 6520   Google Storage 
-00001490: 2020 2020 7c20 3a77 6869 7465 5f63 6865      | :white_che
-000014a0: 636b 5f6d 6172 6b3a 207c 203a 7768 6974  ck_mark: | :whit
-000014b0: 655f 6368 6563 6b5f 6d61 726b 3a20 7c0a  e_check_mark: |.
-000014c0: 7c20 417a 7572 6520 426c 6f62 2053 746f  | Azure Blob Sto
-000014d0: 7261 6765 207c 203a 7768 6974 655f 6368  rage | :white_ch
-000014e0: 6563 6b5f 6d61 726b 3a20 7c20 3a77 6869  eck_mark: | :whi
-000014f0: 7465 5f63 6865 636b 5f6d 6172 6b3a 207c  te_check_mark: |
-00001500: 0a7c 2049 424d 2043 6c6f 7564 204f 626a  .| IBM Cloud Obj
-00001510: 6563 7420 5374 6f72 6167 6520 7c20 3a77  ect Storage | :w
-00001520: 6869 7465 5f63 6865 636b 5f6d 6172 6b3a  hite_check_mark:
-00001530: 207c 203a 7768 6974 655f 6368 6563 6b5f   | :white_check_
-00001540: 6d61 726b 3a20 7c0a 7c20 4c6f 6361 6c20  mark: |.| Local 
-00001550: 4469 736b 2020 2020 2020 2020 207c 203a  Disk         | :
-00001560: 7768 6974 655f 6368 6563 6b5f 6d61 726b  white_check_mark
-00001570: 3a20 7c20 2869 6e20 7072 6f67 7265 7373  : | (in progress
-00001580: 2920 2020 2020 207c 0a0a 536b 7970 6c61  )      |..Skypla
-00001590: 6e65 2069 7320 616e 2061 6374 6976 656c  ne is an activel
-000015a0: 7920 6465 7665 6c6f 7065 6420 7072 6f6a  y developed proj
-000015b0: 6563 742e 2049 7420 7769 6c6c 2068 6176  ect. It will hav
-000015c0: 6520 f09f 94aa 2053 4841 5250 2045 4447  e .... SHARP EDG
-000015d0: 4553 20f0 9f94 aa2e 2050 6c65 6173 6520  ES ..... Please 
-000015e0: 6669 6c65 2061 6e20 6973 7375 6520 6f72  file an issue or
-000015f0: 2061 736b 2074 6865 2063 6f6e 7472 6962   ask the contrib
-00001600: 7574 6f72 7320 7669 6120 5b74 6865 2023  utors via [the #
-00001610: 6865 6c70 2063 6861 6e6e 656c 206f 6e20  help channel on 
-00001620: 6f75 7220 536c 6163 6b5d 2868 7474 7073  our Slack](https
-00001630: 3a2f 2f6a 6f69 6e2e 736c 6163 6b2e 636f  ://join.slack.co
-00001640: 6d2f 742f 736b 7970 6c61 6e65 776f 726b  m/t/skyplanework
-00001650: 7370 6163 652f 7368 6172 6564 5f69 6e76  space/shared_inv
-00001660: 6974 652f 7a74 2d31 6378 6d65 6463 7563  ite/zt-1cxmedcuc
-00001670: 2d47 7749 584c 4779 4854 794f 5945 4c71  -GwIXLGyHTyOYELq
-00001680: 374b 6f4f 6c36 5129 2069 6620 796f 7520  7KoOl6Q) if you 
-00001690: 656e 636f 756e 7465 7220 6275 6773 2e0a  encounter bugs..
-000016a0: 0a23 2052 6573 6f75 7263 6573 200a 2d20  .# Resources .- 
-000016b0: 5b51 7569 636b 7374 6172 745d 2823 7175  [Quickstart](#qu
-000016c0: 6963 6b73 7461 7274 290a 2d20 5b43 6f6e  ickstart).- [Con
-000016d0: 7472 6962 7574 696e 675d 2868 7474 7073  tributing](https
-000016e0: 3a2f 2f73 6b79 706c 616e 652e 6f72 672f  ://skyplane.org/
-000016f0: 656e 2f6c 6174 6573 742f 636f 6e74 7269  en/latest/contri
-00001700: 6275 7469 6e67 2e68 746d 6c29 0a2d 205b  buting.html).- [
-00001710: 526f 6164 6d61 705d 2868 7474 7073 3a2f  Roadmap](https:/
-00001720: 2f73 6b79 706c 616e 652e 6f72 672f 656e  /skyplane.org/en
-00001730: 2f6c 6174 6573 742f 726f 6164 6d61 702e  /latest/roadmap.
-00001740: 6874 6d6c 290a 2d20 5b53 6c61 636b 2043  html).- [Slack C
-00001750: 6f6d 6d75 6e69 7479 5d28 6874 7470 733a  ommunity](https:
-00001760: 2f2f 6a6f 696e 2e73 6c61 636b 2e63 6f6d  //join.slack.com
-00001770: 2f74 2f73 6b79 706c 616e 6577 6f72 6b73  /t/skyplaneworks
-00001780: 7061 6365 2f73 6861 7265 645f 696e 7669  pace/shared_invi
-00001790: 7465 2f7a 742d 3163 786d 6564 6375 632d  te/zt-1cxmedcuc-
-000017a0: 4777 4958 4c47 7948 5479 4f59 454c 7137  GwIXLGyHTyOYELq7
-000017b0: 4b6f 4f6c 3651 290a 0a23 2051 7569 636b  KoOl6Q)..# Quick
-000017c0: 7374 6172 740a 0a23 2320 312e 2049 6e73  start..## 1. Ins
-000017d0: 7461 6c6c 6174 696f 6e0a 5765 2072 6563  tallation.We rec
-000017e0: 6f6d 6d65 6e64 2069 6e73 7461 6c6c 6174  ommend installat
-000017f0: 696f 6e20 6672 6f6d 2050 7950 693a 0a60  ion from PyPi:.`
-00001800: 6060 0a24 2070 6970 2069 6e73 7461 6c6c  ``.$ pip install
-00001810: 2022 736b 7970 6c61 6e65 5b61 7773 5d22   "skyplane[aws]"
-00001820: 0a0a 2320 696e 7374 616c 6c20 7375 7070  ..# install supp
-00001830: 6f72 7420 666f 7220 6f74 6865 7220 636c  ort for other cl
-00001840: 6f75 6473 2061 7320 6e65 6564 6564 3a0a  ouds as needed:.
-00001850: 0a23 2020 2024 2070 6970 2069 6e73 7461  .#   $ pip insta
-00001860: 6c6c 2022 736b 7970 6c61 6e65 5b61 7a75  ll "skyplane[azu
-00001870: 7265 5d22 0a23 2020 2024 2070 6970 2069  re]".#   $ pip i
-00001880: 6e73 7461 6c6c 2022 736b 7970 6c61 6e65  nstall "skyplane
-00001890: 5b67 6370 5d22 0a23 2020 2024 2070 6970  [gcp]".#   $ pip
-000018a0: 2069 6e73 7461 6c6c 2022 736b 7970 6c61   install "skypla
-000018b0: 6e65 5b69 626d 636c 6f75 645d 220a 2320  ne[ibmcloud]".# 
-000018c0: 2020 2420 7069 7020 696e 7374 616c 6c20    $ pip install 
-000018d0: 2273 6b79 706c 616e 655b 616c 6c5d 220a  "skyplane[all]".
-000018e0: 6060 600a 0a53 6b79 706c 616e 6520 7375  ```..Skyplane su
-000018f0: 7070 6f72 7473 2041 5753 2c20 417a 7572  pports AWS, Azur
-00001900: 652c 2049 424d 2061 6e64 2047 4350 2e20  e, IBM and GCP. 
-00001910: 596f 7520 6361 6e20 696e 7374 616c 6c20  You can install 
-00001920: 536b 7970 6c61 6e65 2077 6974 6820 7375  Skyplane with su
-00001930: 7070 6f72 7420 666f 7220 6f6e 6520 6f72  pport for one or
-00001940: 206d 6f72 6520 6f66 2074 6865 7365 2063   more of these c
-00001950: 6c6f 7564 7320 6279 2073 7065 6369 6679  louds by specify
-00001960: 696e 6720 7468 6520 636f 7272 6573 706f  ing the correspo
-00001970: 6e64 696e 6720 6578 7472 6173 2e20 546f  nding extras. To
-00001980: 2069 6e73 7461 6c6c 2074 776f 206f 7574   install two out
-00001990: 206f 6620 7468 7265 6520 636c 6f75 6473   of three clouds
-000019a0: 2c20 796f 7520 6361 6e20 7275 6e20 6070  , you can run `p
-000019b0: 6970 2069 6e73 7461 6c6c 2022 736b 7970  ip install "skyp
-000019c0: 6c61 6e65 5b61 7773 2c61 7a75 7265 5d22  lane[aws,azure]"
-000019d0: 602e 0a0a 2a47 4350 2073 7570 706f 7274  `...*GCP support
-000019e0: 206f 6e20 7468 6520 4d31 204d 6163 2a3a   on the M1 Mac*:
-000019f0: 2049 6620 796f 7520 6172 6520 7573 696e   If you are usin
-00001a00: 6720 616e 204d 3120 4d61 6320 7769 7468  g an M1 Mac with
-00001a10: 2074 6865 2061 726d 3634 2061 7263 6869   the arm64 archi
-00001a20: 7465 6374 7572 6520 616e 6420 7761 6e74  tecture and want
-00001a30: 2074 6f20 696e 7374 616c 6c20 4743 5020   to install GCP 
-00001a40: 7375 7070 6f72 7420 666f 7220 536b 7970  support for Skyp
-00001a50: 6c61 6e65 2c20 796f 7520 7769 6c6c 206e  lane, you will n
-00001a60: 6565 6420 746f 2069 6e73 7461 6c6c 2061  eed to install a
-00001a70: 7320 666f 6c6c 6f77 730a 6047 5250 435f  s follows.`GRPC_
-00001a80: 5059 5448 4f4e 5f42 5549 4c44 5f53 5953  PYTHON_BUILD_SYS
-00001a90: 5445 4d5f 4f50 454e 5353 4c3d 3120 4752  TEM_OPENSSL=1 GR
-00001aa0: 5043 5f50 5954 484f 4e5f 4255 494c 445f  PC_PYTHON_BUILD_
-00001ab0: 5359 5354 454d 5f5a 4c49 423d 3120 7069  SYSTEM_ZLIB=1 pi
-00001ac0: 7020 696e 7374 616c 6c20 2273 6b79 706c  p install "skypl
-00001ad0: 616e 655b 6177 732c 6763 705d 2260 0a0a  ane[aws,gcp]"`..
-00001ae0: 2323 2032 2e20 5365 7475 7020 436c 6f75  ## 2. Setup Clou
-00001af0: 6420 4372 6564 656e 7469 616c 7320 0a0a  d Credentials ..
-00001b00: 536b 7970 6c61 6e65 206e 6565 6473 2061  Skyplane needs a
-00001b10: 6363 6573 7320 746f 2063 6c6f 7564 2063  ccess to cloud c
-00001b20: 7265 6465 6e74 6961 6c73 2074 6f20 7065  redentials to pe
-00001b30: 7266 6f72 6d20 7472 616e 7366 6572 732e  rform transfers.
-00001b40: 2054 6f20 6765 7420 7374 6172 7465 6420   To get started 
-00001b50: 7769 7468 2073 6574 7469 6e67 2075 7020  with setting up 
-00001b60: 6372 6564 656e 7469 616c 732c 206d 616b  credentials, mak
-00001b70: 6520 7375 7265 2079 6f75 2068 6176 6520  e sure you have 
-00001b80: 636c 6f75 6420 7072 6f76 6964 6572 2043  cloud provider C
-00001b90: 4c49 2074 6f6f 6c73 2069 6e73 7461 6c6c  LI tools install
-00001ba0: 6564 3a0a 0a60 6060 0a2d 2d2d 3e20 466f  ed:..```.---> Fo
-00001bb0: 7220 4157 533a 0a24 2070 6970 2069 6e73  r AWS:.$ pip ins
-00001bc0: 7461 6c6c 2061 7773 636c 690a 0a2d 2d2d  tall awscli..---
-00001bd0: 3e20 466f 7220 476f 6f67 6c65 2043 6c6f  > For Google Clo
-00001be0: 7564 3a0a 2420 7069 7020 696e 7374 616c  ud:.$ pip instal
-00001bf0: 6c20 6763 6c6f 7564 0a0a 2d2d 2d3e 2046  l gcloud..---> F
-00001c00: 6f72 2041 7a75 7265 3a0a 2420 7069 7020  or Azure:.$ pip 
-00001c10: 696e 7374 616c 6c20 617a 7572 650a 0a60  install azure..`
-00001c20: 6060 0a4f 6e63 6520 796f 7520 6861 7665  ``.Once you have
-00001c30: 2074 6865 2043 4c49 2074 6f6f 6c73 2073   the CLI tools s
-00001c40: 6574 7570 2c20 6c6f 6720 696e 746f 2065  etup, log into e
-00001c50: 6163 6820 636c 6f75 6420 7072 6f76 6964  ach cloud provid
-00001c60: 6572 2773 2043 4c49 3a0a 6060 600a 2d2d  er's CLI:.```.--
-00001c70: 2d3e 2046 6f72 2041 5753 3a0a 2420 6177  -> For AWS:.$ aw
-00001c80: 7320 636f 6e66 6967 7572 650a 0a2d 2d2d  s configure..---
-00001c90: 3e20 466f 7220 476f 6f67 6c65 2043 6c6f  > For Google Clo
-00001ca0: 7564 3a0a 2420 6763 6c6f 7564 2061 7574  ud:.$ gcloud aut
-00001cb0: 6820 6170 706c 6963 6174 696f 6e2d 6465  h application-de
-00001cc0: 6661 756c 7420 6c6f 6769 6e0a 0a2d 2d2d  fault login..---
-00001cd0: 3e20 466f 7220 417a 7572 653a 0a24 2061  > For Azure:.$ a
-00001ce0: 7a20 6c6f 6769 6e0a 0a2d 2d2d 3e20 466f  z login..---> Fo
-00001cf0: 7220 4942 4d20 436c 6f75 643a 0a24 2046  r IBM Cloud:.$ F
-00001d00: 6f6c 6c6f 7720 4942 4d20 436c 6f75 6420  ollow IBM Cloud 
-00001d10: 616e 6420 6372 6561 7465 2061 6e20 6163  and create an ac
-00001d20: 636f 756e 7420 7769 7468 2074 6865 2072  count with the r
-00001d30: 6573 6f75 7263 6520 6772 6f75 702e 0a43  esource group..C
-00001d40: 6f70 7920 6874 7470 733a 2f2f 6769 7468  opy https://gith
-00001d50: 7562 2e63 6f6d 2f73 6b79 706c 616e 652d  ub.com/skyplane-
-00001d60: 7072 6f6a 6563 742f 736b 7970 6c61 6e65  project/skyplane
-00001d70: 2f62 6c6f 622f 6d61 696e 2f73 6b79 706c  /blob/main/skypl
-00001d80: 616e 652f 636f 6d70 7574 652f 6962 6d63  ane/compute/ibmc
-00001d90: 6c6f 7564 2f69 626d 5f63 7265 6465 6e74  loud/ibm_credent
-00001da0: 6961 6c73 2e79 616d 6c2e 7465 6d70 6c61  ials.yaml.templa
-00001db0: 7465 0a69 6e74 6f20 607e 2f2e 626c 7565  te.into `~/.blue
-00001dc0: 6d69 782f 6962 6d5f 6372 6564 656e 7469  mix/ibm_credenti
-00001dd0: 616c 7360 2061 6e64 2066 696c 6c20 796f  als` and fill yo
-00001de0: 7572 200a 4942 4d20 4941 4d20 6b65 7920  ur .IBM IAM key 
-00001df0: 616e 6420 6372 6564 656e 7469 616c 7320  and credentials 
-00001e00: 746f 2079 6f75 7220 4942 4d20 436c 6f75  to your IBM Clou
-00001e10: 6420 6f62 6a65 6374 2073 746f 7261 6765  d object storage
-00001e20: 200a 0a0a 6060 600a 4166 7465 7220 6175   ...```.After au
-00001e30: 7468 656e 7469 6361 7469 6e67 2077 6974  thenticating wit
-00001e40: 6820 6561 6368 2063 6c6f 7564 2070 726f  h each cloud pro
-00001e50: 7669 6465 722c 2079 6f75 2063 616e 2072  vider, you can r
-00001e60: 756e 2060 736b 7970 6c61 6e65 2069 6e69  un `skyplane ini
-00001e70: 7460 2074 6f20 6372 6561 7465 2061 2063  t` to create a c
-00001e80: 6f6e 6669 6775 7261 7469 6f6e 2066 696c  onfiguration fil
-00001e90: 6520 666f 7220 536b 7970 6c61 6e65 2e0a  e for Skyplane..
-00001ea0: 0a60 6060 6261 7368 0a24 2073 6b79 706c  .```bash.$ skypl
-00001eb0: 616e 6520 696e 6974 0a60 6060 0a3c 6465  ane init.```.<de
-00001ec0: 7461 696c 733e 0a3c 7375 6d6d 6172 793e  tails>.<summary>
-00001ed0: 736b 7970 6c61 6e65 2069 6e69 7420 6f75  skyplane init ou
-00001ee0: 7470 7574 3c2f 7375 6d6d 6172 793e 0a3c  tput</summary>.<
-00001ef0: 6272 3e0a 0a60 6060 0a24 2073 6b79 706c  br>..```.$ skypl
-00001f00: 616e 6520 696e 6974 0a0a 3d3d 3d3d 3d3d  ane init..======
-00001f10: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
-00001f20: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
-00001f30: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 0a20  ==============. 
-00001f40: 5f5f 5f5f 5f20 5f20 2020 5f5f 5f5f 2020  _____ _   ____  
-00001f50: 205f 5f5f 5f5f 5f5f 205f 2020 2020 2020   _______ _      
-00001f60: 205f 5f5f 2020 205f 2020 205f 2020 5f5f   ___   _   _  __
-00001f70: 5f5f 5f0a 2f20 205f 5f5f 7c20 7c20 2f20  ___./  ___| | / 
-00001f80: 2f5c 205c 202f 202f 205f 5f5f 205c 207c  /\ \ / / ___ \ |
-00001f90: 2020 2020 202f 205f 205c 207c 205c 207c       / _ \ | \ |
-00001fa0: 207c 7c20 205f 5f5f 7c0a 5c20 602d 2d2e   ||  ___|.\ `--.
-00001fb0: 7c20 7c2f 202f 2020 5c20 5620 2f7c 207c  | |/ /  \ V /| |
-00001fc0: 5f2f 202f 207c 2020 2020 2f20 2f5f 5c20  _/ / |    / /_\ 
-00001fd0: 5c7c 2020 5c7c 207c 7c20 7c5f 5f0a 2060  \|  \| || |__. `
-00001fe0: 2d2d 2e20 5c20 2020 205c 2020 205c 202f  --. \    \   \ /
-00001ff0: 207c 2020 5f5f 2f7c 207c 2020 2020 7c20   |  __/| |    | 
-00002000: 205f 2020 7c7c 202e 2060 207c 7c20 205f   _  || . ` ||  _
-00002010: 5f7c 0a2f 5c5f 5f2f 202f 207c 5c20 205c  _|./\__/ / |\  \
-00002020: 2020 7c20 7c20 7c20 7c20 2020 7c20 7c5f    | | | |   | |_
-00002030: 5f5f 5f7c 207c 207c 207c 7c20 7c5c 2020  ___| | | || |\  
-00002040: 7c7c 207c 5f5f 5f0a 5c5f 5f5f 5f2f 5c5f  || |___.\____/\_
-00002050: 7c20 5c5f 2f20 205c 5f2f 205c 5f7c 2020  | \_/  \_/ \_|  
-00002060: 205c 5f5f 5f5f 5f2f 5c5f 7c20 7c5f 2f5c   \_____/\_| |_/\
-00002070: 5f7c 205c 5f2f 5c5f 5f5f 5f2f 0a3d 3d3d  _| \_/\____/.===
-00002080: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
-00002090: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
-000020a0: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
-000020b0: 3d0a 0a0a 2831 2920 436f 6e66 6967 7572  =...(1) Configur
-000020c0: 696e 6720 4157 533a 0a20 2020 204c 6f61  ing AWS:.    Loa
-000020d0: 6465 6420 4157 5320 6372 6564 656e 7469  ded AWS credenti
-000020e0: 616c 7320 6672 6f6d 2074 6865 2041 5753  als from the AWS
-000020f0: 2043 4c49 205b 4941 4d20 6163 6365 7373   CLI [IAM access
-00002100: 206b 6579 2049 443a 202e 2e2e 5858 5858   key ID: ...XXXX
-00002110: 5858 5d0a 2020 2020 4157 5320 7265 6769  XX].    AWS regi
-00002120: 6f6e 2063 6f6e 6669 6720 6669 6c65 2073  on config file s
-00002130: 6176 6564 2074 6f20 2f68 6f6d 652f 7562  aved to /home/ub
-00002140: 756e 7475 2f2e 736b 7970 6c61 6e65 2f61  untu/.skyplane/a
-00002150: 7773 5f63 6f6e 6669 670a 0a28 3229 2043  ws_config..(2) C
-00002160: 6f6e 6669 6775 7269 6e67 2041 7a75 7265  onfiguring Azure
-00002170: 3a0a 2020 2020 417a 7572 6520 6372 6564  :.    Azure cred
-00002180: 656e 7469 616c 7320 666f 756e 6420 696e  entials found in
-00002190: 2041 7a75 7265 2043 4c49 0a20 2020 2041   Azure CLI.    A
-000021a0: 7a75 7265 2063 7265 6465 6e74 6961 6c73  zure credentials
-000021b0: 2066 6f75 6e64 2c20 646f 2079 6f75 2077   found, do you w
-000021c0: 616e 7420 746f 2065 6e61 626c 6520 417a  ant to enable Az
-000021d0: 7572 6520 7375 7070 6f72 7420 696e 2053  ure support in S
-000021e0: 6b79 706c 616e 653f 205b 592f 6e5d 3a20  kyplane? [Y/n]: 
-000021f0: 590a 2020 2020 456e 7465 7220 7468 6520  Y.    Enter the 
-00002200: 417a 7572 6520 7375 6273 6372 6970 7469  Azure subscripti
-00002210: 6f6e 2049 443a 205b 5858 5858 5858 5858  on ID: [XXXXXXXX
-00002220: 2d58 5858 582d 5858 5858 2d58 5858 582d  -XXXX-XXXX-XXXX-
-00002230: 5858 5858 5858 5858 5858 5858 5d3a 0a20  XXXXXXXXXXXX]:. 
-00002240: 2020 2041 7a75 7265 2072 6567 696f 6e20     Azure region 
-00002250: 636f 6e66 6967 2066 696c 6520 7361 7665  config file save
-00002260: 6420 746f 202f 686f 6d65 2f75 6275 6e74  d to /home/ubunt
-00002270: 752f 2e73 6b79 706c 616e 652f 617a 7572  u/.skyplane/azur
-00002280: 655f 636f 6e66 6967 0a20 2020 2051 7565  e_config.    Que
-00002290: 7279 696e 6720 666f 7220 534b 5520 6176  rying for SKU av
-000022a0: 6169 6c62 696c 6974 7920 696e 2072 6567  ailbility in reg
-000022b0: 696f 6e73 0a20 2020 2041 7a75 7265 2053  ions.    Azure S
-000022c0: 4b55 2061 7661 696c 6162 696c 6974 7920  KU availability 
-000022d0: 6361 6368 6564 2069 6e20 2f68 6f6d 652f  cached in /home/
-000022e0: 7562 756e 7475 2f2e 736b 7970 6c61 6e65  ubuntu/.skyplane
-000022f0: 2f61 7a75 7265 5f73 6b75 5f6d 6170 7069  /azure_sku_mappi
-00002300: 6e67 0a0a 2833 2920 436f 6e66 6967 7572  ng..(3) Configur
-00002310: 696e 6720 4743 503a 0a20 2020 2047 4350  ing GCP:.    GCP
-00002320: 2063 7265 6465 6e74 6961 6c73 2066 6f75   credentials fou
-00002330: 6e64 2069 6e20 4743 5020 434c 490a 2020  nd in GCP CLI.  
-00002340: 2020 4743 5020 6372 6564 656e 7469 616c    GCP credential
-00002350: 7320 666f 756e 642c 2064 6f20 796f 7520  s found, do you 
-00002360: 7761 6e74 2074 6f20 656e 6162 6c65 2047  want to enable G
-00002370: 4350 2073 7570 706f 7274 2069 6e20 536b  CP support in Sk
-00002380: 7970 6c61 6e65 3f20 5b59 2f6e 5d3a 2059  yplane? [Y/n]: Y
-00002390: 0a20 2020 2045 6e74 6572 2074 6865 2047  .    Enter the G
-000023a0: 4350 2070 726f 6a65 6374 2049 4420 5b58  CP project ID [X
-000023b0: 5858 5858 5858 5d3a 0a20 2020 2047 4350  XXXXXX]:.    GCP
-000023c0: 2072 6567 696f 6e20 636f 6e66 6967 2066   region config f
-000023d0: 696c 6520 7361 7665 6420 746f 202f 686f  ile saved to /ho
-000023e0: 6d65 2f75 6275 6e74 752f 2e73 6b79 706c  me/ubuntu/.skypl
-000023f0: 616e 652f 6763 705f 636f 6e66 6967 0a0a  ane/gcp_config..
-00002400: 436f 6e66 6967 2066 696c 6520 7361 7665  Config file save
-00002410: 6420 746f 202f 686f 6d65 2f75 6275 6e74  d to /home/ubunt
-00002420: 752f 2e73 6b79 706c 616e 652f 636f 6e66  u/.skyplane/conf
-00002430: 6967 0a60 6060 0a0a 3c2f 6465 7461 696c  ig.```..</detail
-00002440: 733e 0a0a 2323 2033 2e20 5275 6e20 5472  s>..## 3. Run Tr
-00002450: 616e 7366 6572 7320 0a0a 5765 e280 9972  ansfers ..We...r
-00002460: 6520 7265 6164 7920 746f 2075 7365 2053  e ready to use S
-00002470: 6b79 706c 616e 6521 204c 6574 e280 9973  kyplane! Let...s
-00002480: 2075 7365 2060 736b 7970 6c61 6e65 2063   use `skyplane c
-00002490: 7060 2074 6f20 636f 7079 2066 696c 6573  p` to copy files
-000024a0: 2066 726f 6d20 4157 5320 746f 2047 4350   from AWS to GCP
-000024b0: 3a0a 6060 600a 736b 7970 6c61 6e65 2063  :.```.skyplane c
-000024c0: 7020 7333 3a2f 2f2e 2e2e 2067 733a 2f2f  p s3://... gs://
-000024d0: 2e2e 2e0a 6060 600a 546f 2074 7261 6e73  ....```.To trans
-000024e0: 6665 7220 6f6e 6c79 206e 6577 206f 626a  fer only new obj
-000024f0: 6563 7473 2c20 796f 7520 6361 6e20 696e  ects, you can in
-00002500: 7374 6561 6420 7573 6520 6073 6b79 706c  stead use `skypl
-00002510: 616e 6520 7379 6e63 603a 0a60 6060 0a24  ane sync`:.```.$
-00002520: 2073 6b79 706c 616e 6520 7379 6e63 2073   skyplane sync s
-00002530: 333a 2f2f 2e2e 2e20 6773 3a2f 2f2e 2e2e  3://... gs://...
-00002540: 0a60 6060 0a0a 596f 7520 6361 6e20 636f  .```..You can co
-00002550: 6e66 6967 7572 6520 536b 7970 6c61 6e65  nfigure Skyplane
-00002560: 2074 6f20 7573 6520 6d6f 7265 2056 4d73   to use more VMs
-00002570: 2070 6572 2072 6567 696f 6e20 7769 7468   per region with
-00002580: 2074 6865 2060 2d6e 6020 666c 6167 2e20   the `-n` flag. 
-00002590: 466f 7220 6578 616d 706c 652c 2074 6f20  For example, to 
-000025a0: 646f 7562 6c65 2074 6865 2074 7261 6e73  double the trans
-000025b0: 6665 7220 7370 6565 6420 7769 7468 2074  fer speed with t
-000025c0: 776f 2056 4d73 2c20 7275 6e3a 200a 6060  wo VMs, run: .``
-000025d0: 600a 2420 736b 7970 6c61 6e65 2063 7020  `.$ skyplane cp 
-000025e0: 2d72 2073 333a 2f2f 2e2e 2e20 7333 3a2f  -r s3://... s3:/
-000025f0: 2f2e 2e2e 202d 6e20 320a 6060 600a 0a23  /... -n 2.```..#
-00002600: 2320 342e 2043 6c65 616e 2055 7020 0a53  # 4. Clean Up .S
-00002610: 6b79 706c 616e 6520 7769 6c6c 2061 7574  kyplane will aut
-00002620: 6f6d 6174 6963 616c 6c79 2061 7474 656d  omatically attem
-00002630: 7074 2074 6f20 7465 726d 696e 6174 6520  pt to terminate 
-00002640: 564d 7320 7468 6174 2069 7420 7374 6172  VMs that it star
-00002650: 7473 2c20 6275 7420 746f 2064 6f75 626c  ts, but to doubl
-00002660: 6520 6368 6563 6b20 616e 6420 666f 7263  e check and forc
-00002670: 6566 756c 7920 7465 726d 696e 6174 6520  efuly terminate 
-00002680: 616c 6c20 564d 732c 2072 756e 2060 736b  all VMs, run `sk
-00002690: 7970 6c61 6e65 2064 6570 726f 7669 7369  yplane deprovisi
-000026a0: 6f6e 602e 0a0a 2320 5465 6368 6e69 6361  on`...# Technica
-000026b0: 6c20 4465 7461 696c 730a 536b 7970 6c61  l Details.Skypla
-000026c0: 6e65 2069 7320 6261 7365 6420 6f6e 2072  ne is based on r
-000026d0: 6573 6561 7263 6820 6174 2055 4320 4265  esearch at UC Be
-000026e0: 726b 656c 6579 2069 6e74 6f20 6163 6365  rkeley into acce
-000026f0: 6c65 7261 7465 6420 6e65 7477 6f72 6b73  lerated networks
-00002700: 2062 6574 7765 656e 2063 6c6f 7564 2070   between cloud p
-00002710: 726f 7669 6465 7273 2e20 556e 6465 7220  roviders. Under 
-00002720: 7468 6520 686f 6f64 2c20 536b 7970 6c61  the hood, Skypla
-00002730: 6e65 2073 7461 7274 7320 6120 666c 6565  ne starts a flee
-00002740: 7420 6f66 2056 4d73 2069 6e20 7468 6520  t of VMs in the 
-00002750: 736f 7572 6365 2061 6e64 2064 6573 7469  source and desti
-00002760: 6e61 7469 6f6e 2072 6567 696f 6e73 2e20  nation regions. 
-00002770: 4974 2074 6865 6e20 7573 6573 2061 2063  It then uses a c
-00002780: 7573 746f 6d20 5443 5020 7072 6f74 6f63  ustom TCP protoc
-00002790: 6f6c 2074 6f20 6163 6365 6c65 7261 7465  ol to accelerate
-000027a0: 2074 6865 2074 7261 6e73 6665 7220 6265   the transfer be
-000027b0: 7477 6565 6e20 7468 6520 564d 732e 2053  tween the VMs. S
-000027c0: 6b79 706c 616e 6520 6d61 7920 7573 6520  kyplane may use 
-000027d0: 6120 4c37 206f 7665 726c 6179 206e 6574  a L7 overlay net
-000027e0: 776f 726b 2074 6f20 726f 7574 6520 7472  work to route tr
-000027f0: 6166 6669 6320 6172 6f75 6e64 2063 6f6e  affic around con
-00002800: 6765 7374 6564 206e 6574 776f 726b 2068  gested network h
-00002810: 6f74 2073 706f 7473 2e20 0a0a 3c69 6d67  ot spots. ..<img
-00002820: 2073 7263 3d22 646f 6373 2f5f 7374 6174   src="docs/_stat
-00002830: 6963 2f73 6b79 706c 616e 652d 6461 7461  ic/skyplane-data
-00002840: 2d70 6c61 6e65 2e70 6e67 2220 7769 6474  -plane.png" widt
-00002850: 683d 2233 3834 2220 2f3e 0a0a 466f 7220  h="384" />..For 
-00002860: 6d6f 7265 2064 6574 6169 6c73 206f 6e20  more details on 
-00002870: 536b 7970 6c61 6e65 2c20 7365 653a 200a  Skyplane, see: .
-00002880: 2d20 5b54 6563 686e 6963 616c 2054 616c  - [Technical Tal
-00002890: 6b5d 2868 7474 7073 3a2f 2f73 6b79 706c  k](https://skypl
-000028a0: 616e 652e 6f72 672f 656e 2f6c 6174 6573  ane.org/en/lates
-000028b0: 742f 6172 6368 6974 6563 7475 7265 2e68  t/architecture.h
-000028c0: 746d 6c29 0a2d 205b 4e53 4449 2027 3233  tml).- [NSDI '23
-000028d0: 2050 6170 6572 5d28 6874 7470 733a 2f2f   Paper](https://
-000028e0: 6172 7869 762e 6f72 672f 6162 732f 3232  arxiv.org/abs/22
-000028f0: 3130 2e30 3732 3539 290a 0a0a 0a         10.07259)....
+00000cc0: 6b64 6f77 6e0a 0a3c 7020 616c 6967 6e3d  kdown..<p align=
+00000cd0: 2263 656e 7465 7222 3e0a 2020 2020 3c70  "center">.    <p
+00000ce0: 6963 7475 7265 3e0a 2020 2020 2020 2020  icture>.        
+00000cf0: 3c73 6f75 7263 6520 7372 6373 6574 3d22  <source srcset="
+00000d00: 646f 6373 2f5f 7374 6174 6963 2f6c 6f67  docs/_static/log
+00000d10: 6f2d 6461 726b 2d6d 6f64 652e 706e 6722  o-dark-mode.png"
+00000d20: 206d 6564 6961 3d22 2870 7265 6665 7273   media="(prefers
+00000d30: 2d63 6f6c 6f72 2d73 6368 656d 653a 2064  -color-scheme: d
+00000d40: 6172 6b29 223e 0a20 2020 2020 2020 203c  ark)">.        <
+00000d50: 696d 6720 7372 633d 2264 6f63 732f 5f73  img src="docs/_s
+00000d60: 7461 7469 632f 6c6f 676f 2d6c 6967 6874  tatic/logo-light
+00000d70: 2d6d 6f64 652e 706e 6722 2077 6964 7468  -mode.png" width
+00000d80: 3d22 3330 3022 202f 3e0a 2020 2020 3c2f  ="300" />.    </
+00000d90: 7069 6374 7572 653e 0a3c 2f70 3e0a 0a3c  picture>.</p>..<
+00000da0: 7020 616c 6967 6e3d 2263 656e 7465 7222  p align="center"
+00000db0: 3e0a 2020 3c61 2068 7265 663d 2268 7474  >.  <a href="htt
+00000dc0: 7073 3a2f 2f6a 6f69 6e2e 736c 6163 6b2e  ps://join.slack.
+00000dd0: 636f 6d2f 742f 736b 7970 6c61 6e65 776f  com/t/skyplanewo
+00000de0: 726b 7370 6163 652f 7368 6172 6564 5f69  rkspace/shared_i
+00000df0: 6e76 6974 652f 7a74 2d31 6378 6d65 6463  nvite/zt-1cxmedc
+00000e00: 7563 2d47 7749 584c 4779 4854 794f 5945  uc-GwIXLGyHTyOYE
+00000e10: 4c71 374b 6f4f 6c36 5122 3e20 0a20 2020  Lq7KoOl6Q"> .   
+00000e20: 203c 696d 6720 616c 743d 224a 6f69 6e20   <img alt="Join 
+00000e30: 536c 6163 6b22 2073 7263 3d22 6874 7470  Slack" src="http
+00000e40: 733a 2f2f 696d 672e 7368 6965 6c64 732e  s://img.shields.
+00000e50: 696f 2f62 6164 6765 2f2d 4a6f 696e 2532  io/badge/-Join%2
+00000e60: 3053 6b79 706c 616e 6525 3230 536c 6163  0Skyplane%20Slac
+00000e70: 6b2d 626c 7565 3f6c 6f67 6f3d 736c 6163  k-blue?logo=slac
+00000e80: 6b22 3e0a 2020 3c2f 613e 0a20 200a 2020  k">.  </a>.  .  
+00000e90: 3c61 2068 7265 663d 2268 7474 7073 3a2f  <a href="https:/
+00000ea0: 2f67 6974 6875 622e 636f 6d2f 736b 7970  /github.com/skyp
+00000eb0: 6c61 6e65 2d70 726f 6a65 6374 2f73 6b79  lane-project/sky
+00000ec0: 706c 616e 652f 6163 7469 6f6e 732f 776f  plane/actions/wo
+00000ed0: 726b 666c 6f77 732f 696e 7465 6772 6174  rkflows/integrat
+00000ee0: 696f 6e2d 7465 7374 2d6d 756c 7469 706c  ion-test-multipl
+00000ef0: 652d 7369 7a65 732e 796d 6c22 3e20 0a20  e-sizes.yml"> . 
+00000f00: 2020 203c 696d 6720 616c 743d 2269 6e74     <img alt="int
+00000f10: 6567 7261 7469 6f6e 2d74 6573 7422 2073  egration-test" s
+00000f20: 7263 3d22 6874 7470 733a 2f2f 6769 7468  rc="https://gith
+00000f30: 7562 2e63 6f6d 2f73 6b79 706c 616e 652d  ub.com/skyplane-
+00000f40: 7072 6f6a 6563 742f 736b 7970 6c61 6e65  project/skyplane
+00000f50: 2f61 6374 696f 6e73 2f77 6f72 6b66 6c6f  /actions/workflo
+00000f60: 7773 2f69 6e74 6567 7261 7469 6f6e 2d74  ws/integration-t
+00000f70: 6573 742d 6d75 6c74 6970 6c65 2d73 697a  est-multiple-siz
+00000f80: 6573 2e79 6d6c 2f62 6164 6765 2e73 7667  es.yml/badge.svg
+00000f90: 223e 0a20 203c 2f61 3e0a 2020 0a20 203c  ">.  </a>.  .  <
+00000fa0: 6120 6872 6566 3d22 6874 7470 733a 2f2f  a href="https://
+00000fb0: 6769 7468 7562 2e63 6f6d 2f73 6b79 706c  github.com/skypl
+00000fc0: 616e 652d 7072 6f6a 6563 742f 736b 7970  ane-project/skyp
+00000fd0: 6c61 6e65 2f61 6374 696f 6e73 2f77 6f72  lane/actions/wor
+00000fe0: 6b66 6c6f 7773 2f64 6f63 6b65 722d 7075  kflows/docker-pu
+00000ff0: 626c 6973 682e 796d 6c22 3e20 0a20 2020  blish.yml"> .   
+00001000: 203c 696d 6720 616c 743d 2264 6f63 6b65   <img alt="docke
+00001010: 7222 2073 7263 3d22 6874 7470 733a 2f2f  r" src="https://
+00001020: 6769 7468 7562 2e63 6f6d 2f73 6b79 706c  github.com/skypl
+00001030: 616e 652d 7072 6f6a 6563 742f 736b 7970  ane-project/skyp
+00001040: 6c61 6e65 2f61 6374 696f 6e73 2f77 6f72  lane/actions/wor
+00001050: 6b66 6c6f 7773 2f64 6f63 6b65 722d 7075  kflows/docker-pu
+00001060: 626c 6973 682e 796d 6c2f 6261 6467 652e  blish.yml/badge.
+00001070: 7376 6722 3e0a 2020 3c2f 613e 0a20 200a  svg">.  </a>.  .
+00001080: 2020 3c61 2068 7265 663d 2268 7474 7073    <a href="https
+00001090: 3a2f 2f73 6b79 706c 616e 652e 7265 6164  ://skyplane.read
+000010a0: 7468 6564 6f63 732e 696f 2f65 6e2f 6c61  thedocs.io/en/la
+000010b0: 7465 7374 2f3f 6261 6467 653d 6c61 7465  test/?badge=late
+000010c0: 7374 223e 200a 2020 2020 3c69 6d67 2061  st"> .    <img a
+000010d0: 6c74 3d22 646f 6373 2220 7372 633d 2268  lt="docs" src="h
+000010e0: 7474 7073 3a2f 2f72 6561 6474 6865 646f  ttps://readthedo
+000010f0: 6373 2e6f 7267 2f70 726f 6a65 6374 732f  cs.org/projects/
+00001100: 736b 7970 6c61 6e65 2f62 6164 6765 2f3f  skyplane/badge/?
+00001110: 7665 7273 696f 6e3d 6c61 7465 7374 223e  version=latest">
+00001120: 0a20 203c 2f61 3e0a 3c2f 703e 0a0a 2a2a  .  </a>.</p>..**
+00001130: f09f 94a5 2042 6c61 7a69 6e67 2066 6173  .... Blazing fas
+00001140: 7420 6275 6c6b 2064 6174 6120 7472 616e  t bulk data tran
+00001150: 7366 6572 7320 6265 7477 6565 6e20 616e  sfers between an
+00001160: 7920 636c 6f75 6420 f09f 94a5 2a2a 0a0a  y cloud ....**..
+00001170: 536b 7970 6c61 6e65 2069 7320 6120 746f  Skyplane is a to
+00001180: 6f6c 2066 6f72 2062 6c61 7a69 6e67 6c79  ol for blazingly
+00001190: 2066 6173 7420 6275 6c6b 2064 6174 6120   fast bulk data 
+000011a0: 7472 616e 7366 6572 7320 6265 7477 6565  transfers betwee
+000011b0: 6e20 6f62 6a65 6374 2073 746f 7265 7320  n object stores 
+000011c0: 696e 2074 6865 2063 6c6f 7564 2e20 4974  in the cloud. It
+000011d0: 2070 726f 7669 7369 6f6e 7320 6120 666c   provisions a fl
+000011e0: 6565 7420 6f66 2056 4d73 2069 6e20 7468  eet of VMs in th
+000011f0: 6520 636c 6f75 6420 746f 2074 7261 6e73  e cloud to trans
+00001200: 6665 7220 6461 7461 2069 6e20 7061 7261  fer data in para
+00001210: 6c6c 656c 2077 6869 6c65 2075 7369 6e67  llel while using
+00001220: 2063 6f6d 7072 6573 7369 6f6e 2061 6e64   compression and
+00001230: 2062 616e 6477 6964 7468 2074 6965 7269   bandwidth tieri
+00001240: 6e67 2074 6f20 7265 6475 6365 2063 6f73  ng to reduce cos
+00001250: 742e 0a0a 536b 7970 6c61 6e65 2069 733a  t...Skyplane is:
+00001260: 0a31 2e20 f09f 94a5 2042 6c61 7a69 6e67  .1. .... Blazing
+00001270: 2066 6173 7420 285b 3131 3078 2066 6173   fast ([110x fas
+00001280: 7465 7220 7468 616e 2041 5753 2044 6174  ter than AWS Dat
+00001290: 6153 796e 635d 2868 7474 7073 3a2f 2f73  aSync](https://s
+000012a0: 6b79 706c 616e 652e 6f72 672f 656e 2f6c  kyplane.org/en/l
+000012b0: 6174 6573 742f 6265 6e63 686d 6172 6b2e  atest/benchmark.
+000012c0: 6874 6d6c 2929 0a32 2e20 f09f a491 2043  html)).2. .... C
+000012d0: 6865 6170 2028 3478 2063 6865 6170 6572  heap (4x cheaper
+000012e0: 2074 6861 6e20 7273 796e 6329 0a33 2e20   than rsync).3. 
+000012f0: f09f 8c90 2055 6e69 7665 7273 616c 2028  .... Universal (
+00001300: 4157 532c 2041 7a75 7265 2c20 4942 4d20  AWS, Azure, IBM 
+00001310: 616e 6420 4743 5029 0a0a 596f 7520 6361  and GCP)..You ca
+00001320: 6e20 7573 6520 536b 7970 6c61 6e65 2074  n use Skyplane t
+00001330: 6f20 7472 616e 7366 6572 2064 6174 613a  o transfer data:
+00001340: 200a 2a20 6265 7477 6565 6e20 6f62 6a65   .* between obje
+00001350: 6374 2073 746f 7265 7320 7769 7468 696e  ct stores within
+00001360: 2061 2063 6c6f 7564 2070 726f 7669 6465   a cloud provide
+00001370: 7220 2865 2e67 2e20 4157 5320 7573 2d65  r (e.g. AWS us-e
+00001380: 6173 742d 3120 746f 2041 5753 2075 732d  ast-1 to AWS us-
+00001390: 7765 7374 2d32 290a 2a20 6265 7477 6565  west-2).* betwee
+000013a0: 6e20 6f62 6a65 6374 2073 746f 7265 7320  n object stores 
+000013b0: 6163 726f 7373 206d 756c 7469 706c 6520  across multiple 
+000013c0: 636c 6f75 6420 7072 6f76 6964 6572 7320  cloud providers 
+000013d0: 2865 2e67 2e20 4157 5320 7573 2d65 6173  (e.g. AWS us-eas
+000013e0: 742d 3120 746f 2047 4350 2075 732d 6365  t-1 to GCP us-ce
+000013f0: 6e74 7261 6c31 290a 2a20 6265 7477 6565  ntral1).* betwee
+00001400: 6e20 6c6f 6361 6c20 7374 6f72 6167 6520  n local storage 
+00001410: 616e 6420 636c 6f75 6420 6f62 6a65 6374  and cloud object
+00001420: 2073 746f 7265 7320 2865 7870 6572 696d   stores (experim
+00001430: 656e 7461 6c29 0a0a 536b 7970 6c61 6e65  ental)..Skyplane
+00001440: 2063 7572 7265 6e74 6c79 2073 7570 706f   currently suppo
+00001450: 7274 7320 7468 6520 666f 6c6c 6f77 696e  rts the followin
+00001460: 6720 736f 7572 6365 2061 6e64 2064 6573  g source and des
+00001470: 7469 6e61 7469 6f6e 2065 6e64 706f 696e  tination endpoin
+00001480: 7473 2028 616e 7920 736f 7572 6365 2061  ts (any source a
+00001490: 6e64 2064 6573 7469 6e61 7469 6f6e 2063  nd destination c
+000014a0: 616e 2062 6520 636f 6d62 696e 6564 293a  an be combined):
+000014b0: 200a 0a7c 2045 6e64 706f 696e 7420 2020   ..| Endpoint   
+000014c0: 2020 2020 2020 2020 7c20 536f 7572 6365          | Source
+000014d0: 2020 2020 2020 2020 2020 2020 207c 2044               | D
+000014e0: 6573 7469 6e61 7469 6f6e 2020 2020 2020  estination      
+000014f0: 2020 7c0a 7c2d 2d2d 2d2d 2d2d 2d2d 2d2d    |.|-----------
+00001500: 2d2d 2d2d 2d2d 2d2d 2d7c 2d2d 2d2d 2d2d  ---------|------
+00001510: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 7c2d  --------------|-
+00001520: 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d 2d2d  ----------------
+00001530: 2d2d 2d7c 0a7c 2041 5753 2053 3320 2020  ---|.| AWS S3   
+00001540: 2020 2020 2020 2020 2020 7c20 3a77 6869            | :whi
+00001550: 7465 5f63 6865 636b 5f6d 6172 6b3a 207c  te_check_mark: |
+00001560: 203a 7768 6974 655f 6368 6563 6b5f 6d61   :white_check_ma
+00001570: 726b 3a20 7c0a 7c20 476f 6f67 6c65 2053  rk: |.| Google S
+00001580: 746f 7261 6765 2020 2020 207c 203a 7768  torage     | :wh
+00001590: 6974 655f 6368 6563 6b5f 6d61 726b 3a20  ite_check_mark: 
+000015a0: 7c20 3a77 6869 7465 5f63 6865 636b 5f6d  | :white_check_m
+000015b0: 6172 6b3a 207c 0a7c 2041 7a75 7265 2042  ark: |.| Azure B
+000015c0: 6c6f 6220 5374 6f72 6167 6520 7c20 3a77  lob Storage | :w
+000015d0: 6869 7465 5f63 6865 636b 5f6d 6172 6b3a  hite_check_mark:
+000015e0: 207c 203a 7768 6974 655f 6368 6563 6b5f   | :white_check_
+000015f0: 6d61 726b 3a20 7c0a 7c20 4942 4d20 436c  mark: |.| IBM Cl
+00001600: 6f75 6420 4f62 6a65 6374 2053 746f 7261  oud Object Stora
+00001610: 6765 207c 203a 7768 6974 655f 6368 6563  ge | :white_chec
+00001620: 6b5f 6d61 726b 3a20 7c20 3a77 6869 7465  k_mark: | :white
+00001630: 5f63 6865 636b 5f6d 6172 6b3a 207c 0a7c  _check_mark: |.|
+00001640: 204c 6f63 616c 2044 6973 6b20 2020 2020   Local Disk     
+00001650: 2020 2020 7c20 3a77 6869 7465 5f63 6865      | :white_che
+00001660: 636b 5f6d 6172 6b3a 207c 2028 696e 2070  ck_mark: | (in p
+00001670: 726f 6772 6573 7329 2020 2020 2020 7c0a  rogress)      |.
+00001680: 0a53 6b79 706c 616e 6520 6973 2061 6e20  .Skyplane is an 
+00001690: 6163 7469 7665 6c79 2064 6576 656c 6f70  actively develop
+000016a0: 6564 2070 726f 6a65 6374 2e20 4974 2077  ed project. It w
+000016b0: 696c 6c20 6861 7665 20f0 9f94 aa20 5348  ill have .... SH
+000016c0: 4152 5020 4544 4745 5320 f09f 94aa 2e20  ARP EDGES ..... 
+000016d0: 506c 6561 7365 2066 696c 6520 616e 2069  Please file an i
+000016e0: 7373 7565 206f 7220 6173 6b20 7468 6520  ssue or ask the 
+000016f0: 636f 6e74 7269 6275 746f 7273 2076 6961  contributors via
+00001700: 205b 7468 6520 2368 656c 7020 6368 616e   [the #help chan
+00001710: 6e65 6c20 6f6e 206f 7572 2053 6c61 636b  nel on our Slack
+00001720: 5d28 6874 7470 733a 2f2f 6a6f 696e 2e73  ](https://join.s
+00001730: 6c61 636b 2e63 6f6d 2f74 2f73 6b79 706c  lack.com/t/skypl
+00001740: 616e 6577 6f72 6b73 7061 6365 2f73 6861  aneworkspace/sha
+00001750: 7265 645f 696e 7669 7465 2f7a 742d 3163  red_invite/zt-1c
+00001760: 786d 6564 6375 632d 4777 4958 4c47 7948  xmedcuc-GwIXLGyH
+00001770: 5479 4f59 454c 7137 4b6f 4f6c 3651 2920  TyOYELq7KoOl6Q) 
+00001780: 6966 2079 6f75 2065 6e63 6f75 6e74 6572  if you encounter
+00001790: 2062 7567 732e 0a0a 2320 5265 736f 7572   bugs...# Resour
+000017a0: 6365 7320 0a2d 205b 5175 6963 6b73 7461  ces .- [Quicksta
+000017b0: 7274 5d28 2371 7569 636b 7374 6172 7429  rt](#quickstart)
+000017c0: 0a2d 205b 436f 6e74 7269 6275 7469 6e67  .- [Contributing
+000017d0: 5d28 6874 7470 733a 2f2f 736b 7970 6c61  ](https://skypla
+000017e0: 6e65 2e6f 7267 2f65 6e2f 6c61 7465 7374  ne.org/en/latest
+000017f0: 2f63 6f6e 7472 6962 7574 696e 672e 6874  /contributing.ht
+00001800: 6d6c 290a 2d20 5b52 6f61 646d 6170 5d28  ml).- [Roadmap](
+00001810: 6874 7470 733a 2f2f 736b 7970 6c61 6e65  https://skyplane
+00001820: 2e6f 7267 2f65 6e2f 6c61 7465 7374 2f72  .org/en/latest/r
+00001830: 6f61 646d 6170 2e68 746d 6c29 0a2d 205b  oadmap.html).- [
+00001840: 536c 6163 6b20 436f 6d6d 756e 6974 795d  Slack Community]
+00001850: 2868 7474 7073 3a2f 2f6a 6f69 6e2e 736c  (https://join.sl
+00001860: 6163 6b2e 636f 6d2f 742f 736b 7970 6c61  ack.com/t/skypla
+00001870: 6e65 776f 726b 7370 6163 652f 7368 6172  neworkspace/shar
+00001880: 6564 5f69 6e76 6974 652f 7a74 2d31 6378  ed_invite/zt-1cx
+00001890: 6d65 6463 7563 2d47 7749 584c 4779 4854  medcuc-GwIXLGyHT
+000018a0: 794f 5945 4c71 374b 6f4f 6c36 5129 0a0a  yOYELq7KoOl6Q)..
+000018b0: 2320 5175 6963 6b73 7461 7274 0a0a 2323  # Quickstart..##
+000018c0: 2031 2e20 496e 7374 616c 6c61 7469 6f6e   1. Installation
+000018d0: 0a57 6520 7265 636f 6d6d 656e 6420 696e  .We recommend in
+000018e0: 7374 616c 6c61 7469 6f6e 2066 726f 6d20  stallation from 
+000018f0: 5079 5069 3a0a 6060 600a 2420 7069 7020  PyPi:.```.$ pip 
+00001900: 696e 7374 616c 6c20 2273 6b79 706c 616e  install "skyplan
+00001910: 655b 6177 735d 220a 0a23 2069 6e73 7461  e[aws]"..# insta
+00001920: 6c6c 2073 7570 706f 7274 2066 6f72 206f  ll support for o
+00001930: 7468 6572 2063 6c6f 7564 7320 6173 206e  ther clouds as n
+00001940: 6565 6465 643a 0a0a 2320 2020 2420 7069  eeded:..#   $ pi
+00001950: 7020 696e 7374 616c 6c20 2273 6b79 706c  p install "skypl
+00001960: 616e 655b 617a 7572 655d 220a 2320 2020  ane[azure]".#   
+00001970: 2420 7069 7020 696e 7374 616c 6c20 2273  $ pip install "s
+00001980: 6b79 706c 616e 655b 6763 705d 220a 2320  kyplane[gcp]".# 
+00001990: 2020 2420 7069 7020 696e 7374 616c 6c20    $ pip install 
+000019a0: 2273 6b79 706c 616e 655b 6962 6d63 6c6f  "skyplane[ibmclo
+000019b0: 7564 5d22 0a23 2020 2024 2070 6970 2069  ud]".#   $ pip i
+000019c0: 6e73 7461 6c6c 2022 736b 7970 6c61 6e65  nstall "skyplane
+000019d0: 5b61 6c6c 5d22 0a60 6060 0a0a 536b 7970  [all]".```..Skyp
+000019e0: 6c61 6e65 2073 7570 706f 7274 7320 4157  lane supports AW
+000019f0: 532c 2041 7a75 7265 2c20 4942 4d20 616e  S, Azure, IBM an
+00001a00: 6420 4743 502e 2059 6f75 2063 616e 2069  d GCP. You can i
+00001a10: 6e73 7461 6c6c 2053 6b79 706c 616e 6520  nstall Skyplane 
+00001a20: 7769 7468 2073 7570 706f 7274 2066 6f72  with support for
+00001a30: 206f 6e65 206f 7220 6d6f 7265 206f 6620   one or more of 
+00001a40: 7468 6573 6520 636c 6f75 6473 2062 7920  these clouds by 
+00001a50: 7370 6563 6966 7969 6e67 2074 6865 2063  specifying the c
+00001a60: 6f72 7265 7370 6f6e 6469 6e67 2065 7874  orresponding ext
+00001a70: 7261 732e 2054 6f20 696e 7374 616c 6c20  ras. To install 
+00001a80: 7477 6f20 6f75 7420 6f66 2074 6872 6565  two out of three
+00001a90: 2063 6c6f 7564 732c 2079 6f75 2063 616e   clouds, you can
+00001aa0: 2072 756e 2060 7069 7020 696e 7374 616c   run `pip instal
+00001ab0: 6c20 2273 6b79 706c 616e 655b 6177 732c  l "skyplane[aws,
+00001ac0: 617a 7572 655d 2260 2e0a 0a2a 4743 5020  azure]"`...*GCP 
+00001ad0: 7375 7070 6f72 7420 6f6e 2074 6865 204d  support on the M
+00001ae0: 3120 4d61 632a 3a20 4966 2079 6f75 2061  1 Mac*: If you a
+00001af0: 7265 2075 7369 6e67 2061 6e20 4d31 204d  re using an M1 M
+00001b00: 6163 2077 6974 6820 7468 6520 6172 6d36  ac with the arm6
+00001b10: 3420 6172 6368 6974 6563 7475 7265 2061  4 architecture a
+00001b20: 6e64 2077 616e 7420 746f 2069 6e73 7461  nd want to insta
+00001b30: 6c6c 2047 4350 2073 7570 706f 7274 2066  ll GCP support f
+00001b40: 6f72 2053 6b79 706c 616e 652c 2079 6f75  or Skyplane, you
+00001b50: 2077 696c 6c20 6e65 6564 2074 6f20 696e   will need to in
+00001b60: 7374 616c 6c20 6173 2066 6f6c 6c6f 7773  stall as follows
+00001b70: 0a60 4752 5043 5f50 5954 484f 4e5f 4255  .`GRPC_PYTHON_BU
+00001b80: 494c 445f 5359 5354 454d 5f4f 5045 4e53  ILD_SYSTEM_OPENS
+00001b90: 534c 3d31 2047 5250 435f 5059 5448 4f4e  SL=1 GRPC_PYTHON
+00001ba0: 5f42 5549 4c44 5f53 5953 5445 4d5f 5a4c  _BUILD_SYSTEM_ZL
+00001bb0: 4942 3d31 2070 6970 2069 6e73 7461 6c6c  IB=1 pip install
+00001bc0: 2022 736b 7970 6c61 6e65 5b61 7773 2c67   "skyplane[aws,g
+00001bd0: 6370 5d22 600a 0a23 2320 322e 2053 6574  cp]"`..## 2. Set
+00001be0: 7570 2043 6c6f 7564 2043 7265 6465 6e74  up Cloud Credent
+00001bf0: 6961 6c73 200a 0a53 6b79 706c 616e 6520  ials ..Skyplane 
+00001c00: 6e65 6564 7320 6163 6365 7373 2074 6f20  needs access to 
+00001c10: 636c 6f75 6420 6372 6564 656e 7469 616c  cloud credential
+00001c20: 7320 746f 2070 6572 666f 726d 2074 7261  s to perform tra
+00001c30: 6e73 6665 7273 2e20 546f 2067 6574 2073  nsfers. To get s
+00001c40: 7461 7274 6564 2077 6974 6820 7365 7474  tarted with sett
+00001c50: 696e 6720 7570 2063 7265 6465 6e74 6961  ing up credentia
+00001c60: 6c73 2c20 6d61 6b65 2073 7572 6520 796f  ls, make sure yo
+00001c70: 7520 6861 7665 2063 6c6f 7564 2070 726f  u have cloud pro
+00001c80: 7669 6465 7220 434c 4920 746f 6f6c 7320  vider CLI tools 
+00001c90: 696e 7374 616c 6c65 643a 0a0a 6060 600a  installed:..```.
+00001ca0: 2d2d 2d3e 2046 6f72 2041 5753 3a0a 2420  ---> For AWS:.$ 
+00001cb0: 7069 7020 696e 7374 616c 6c20 6177 7363  pip install awsc
+00001cc0: 6c69 0a0a 2d2d 2d3e 2046 6f72 2047 6f6f  li..---> For Goo
+00001cd0: 676c 6520 436c 6f75 643a 0a24 2070 6970  gle Cloud:.$ pip
+00001ce0: 2069 6e73 7461 6c6c 2067 636c 6f75 640a   install gcloud.
+00001cf0: 0a2d 2d2d 3e20 466f 7220 417a 7572 653a  .---> For Azure:
+00001d00: 0a24 2070 6970 2069 6e73 7461 6c6c 2061  .$ pip install a
+00001d10: 7a75 7265 0a0a 6060 600a 4f6e 6365 2079  zure..```.Once y
+00001d20: 6f75 2068 6176 6520 7468 6520 434c 4920  ou have the CLI 
+00001d30: 746f 6f6c 7320 7365 7475 702c 206c 6f67  tools setup, log
+00001d40: 2069 6e74 6f20 6561 6368 2063 6c6f 7564   into each cloud
+00001d50: 2070 726f 7669 6465 7227 7320 434c 493a   provider's CLI:
+00001d60: 0a60 6060 0a2d 2d2d 3e20 466f 7220 4157  .```.---> For AW
+00001d70: 533a 0a24 2061 7773 2063 6f6e 6669 6775  S:.$ aws configu
+00001d80: 7265 0a0a 2d2d 2d3e 2046 6f72 2047 6f6f  re..---> For Goo
+00001d90: 676c 6520 436c 6f75 643a 0a24 2067 636c  gle Cloud:.$ gcl
+00001da0: 6f75 6420 6175 7468 2061 7070 6c69 6361  oud auth applica
+00001db0: 7469 6f6e 2d64 6566 6175 6c74 206c 6f67  tion-default log
+00001dc0: 696e 0a0a 2d2d 2d3e 2046 6f72 2041 7a75  in..---> For Azu
+00001dd0: 7265 3a0a 2420 617a 206c 6f67 696e 0a0a  re:.$ az login..
+00001de0: 2d2d 2d3e 2046 6f72 2049 424d 2043 6c6f  ---> For IBM Clo
+00001df0: 7564 3a0a 2420 466f 6c6c 6f77 2049 424d  ud:.$ Follow IBM
+00001e00: 2043 6c6f 7564 2061 6e64 2063 7265 6174   Cloud and creat
+00001e10: 6520 616e 2061 6363 6f75 6e74 2077 6974  e an account wit
+00001e20: 6820 7468 6520 7265 736f 7572 6365 2067  h the resource g
+00001e30: 726f 7570 2e0a 436f 7079 2068 7474 7073  roup..Copy https
+00001e40: 3a2f 2f67 6974 6875 622e 636f 6d2f 736b  ://github.com/sk
+00001e50: 7970 6c61 6e65 2d70 726f 6a65 6374 2f73  yplane-project/s
+00001e60: 6b79 706c 616e 652f 626c 6f62 2f6d 6169  kyplane/blob/mai
+00001e70: 6e2f 736b 7970 6c61 6e65 2f63 6f6d 7075  n/skyplane/compu
+00001e80: 7465 2f69 626d 636c 6f75 642f 6962 6d5f  te/ibmcloud/ibm_
+00001e90: 6372 6564 656e 7469 616c 732e 7961 6d6c  credentials.yaml
+00001ea0: 2e74 656d 706c 6174 650a 696e 746f 2060  .template.into `
+00001eb0: 7e2f 2e62 6c75 656d 6978 2f69 626d 5f63  ~/.bluemix/ibm_c
+00001ec0: 7265 6465 6e74 6961 6c73 6020 616e 6420  redentials` and 
+00001ed0: 6669 6c6c 2079 6f75 7220 0a49 424d 2049  fill your .IBM I
+00001ee0: 414d 206b 6579 2061 6e64 2063 7265 6465  AM key and crede
+00001ef0: 6e74 6961 6c73 2074 6f20 796f 7572 2049  ntials to your I
+00001f00: 424d 2043 6c6f 7564 206f 626a 6563 7420  BM Cloud object 
+00001f10: 7374 6f72 6167 6520 0a0a 0a60 6060 0a41  storage ...```.A
+00001f20: 6674 6572 2061 7574 6865 6e74 6963 6174  fter authenticat
+00001f30: 696e 6720 7769 7468 2065 6163 6820 636c  ing with each cl
+00001f40: 6f75 6420 7072 6f76 6964 6572 2c20 796f  oud provider, yo
+00001f50: 7520 6361 6e20 7275 6e20 6073 6b79 706c  u can run `skypl
+00001f60: 616e 6520 696e 6974 6020 746f 2063 7265  ane init` to cre
+00001f70: 6174 6520 6120 636f 6e66 6967 7572 6174  ate a configurat
+00001f80: 696f 6e20 6669 6c65 2066 6f72 2053 6b79  ion file for Sky
+00001f90: 706c 616e 652e 0a0a 6060 6062 6173 680a  plane...```bash.
+00001fa0: 2420 736b 7970 6c61 6e65 2069 6e69 740a  $ skyplane init.
+00001fb0: 6060 600a 3c64 6574 6169 6c73 3e0a 3c73  ```.<details>.<s
+00001fc0: 756d 6d61 7279 3e73 6b79 706c 616e 6520  ummary>skyplane 
+00001fd0: 696e 6974 206f 7574 7075 743c 2f73 756d  init output</sum
+00001fe0: 6d61 7279 3e0a 3c62 723e 0a0a 6060 600a  mary>.<br>..```.
+00001ff0: 2420 736b 7970 6c61 6e65 2069 6e69 740a  $ skyplane init.
+00002000: 0a3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  .===============
+00002010: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
+00002020: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
+00002030: 3d3d 3d3d 3d0a 205f 5f5f 5f5f 205f 2020  =====. _____ _  
+00002040: 205f 5f5f 5f20 2020 5f5f 5f5f 5f5f 5f20   ____   _______ 
+00002050: 5f20 2020 2020 2020 5f5f 5f20 2020 5f20  _       ___   _ 
+00002060: 2020 5f20 205f 5f5f 5f5f 0a2f 2020 5f5f    _  _____./  __
+00002070: 5f7c 207c 202f 202f 5c20 5c20 2f20 2f20  _| | / /\ \ / / 
+00002080: 5f5f 5f20 5c20 7c20 2020 2020 2f20 5f20  ___ \ |     / _ 
+00002090: 5c20 7c20 5c20 7c20 7c7c 2020 5f5f 5f7c  \ | \ | ||  ___|
+000020a0: 0a5c 2060 2d2d 2e7c 207c 2f20 2f20 205c  .\ `--.| |/ /  \
+000020b0: 2056 202f 7c20 7c5f 2f20 2f20 7c20 2020   V /| |_/ / |   
+000020c0: 202f 202f 5f5c 205c 7c20 205c 7c20 7c7c   / /_\ \|  \| ||
+000020d0: 207c 5f5f 0a20 602d 2d2e 205c 2020 2020   |__. `--. \    
+000020e0: 5c20 2020 5c20 2f20 7c20 205f 5f2f 7c20  \   \ / |  __/| 
+000020f0: 7c20 2020 207c 2020 5f20 207c 7c20 2e20  |    |  _  || . 
+00002100: 6020 7c7c 2020 5f5f 7c0a 2f5c 5f5f 2f20  ` ||  __|./\__/ 
+00002110: 2f20 7c5c 2020 5c20 207c 207c 207c 207c  / |\  \  | | | |
+00002120: 2020 207c 207c 5f5f 5f5f 7c20 7c20 7c20     | |____| | | 
+00002130: 7c7c 207c 5c20 207c 7c20 7c5f 5f5f 0a5c  || |\  || |___.\
+00002140: 5f5f 5f5f 2f5c 5f7c 205c 5f2f 2020 5c5f  ____/\_| \_/  \_
+00002150: 2f20 5c5f 7c20 2020 5c5f 5f5f 5f5f 2f5c  / \_|   \_____/\
+00002160: 5f7c 207c 5f2f 5c5f 7c20 5c5f 2f5c 5f5f  _| |_/\_| \_/\__
+00002170: 5f5f 2f0a 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  __/.============
+00002180: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
+00002190: 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d 3d3d  ================
+000021a0: 3d3d 3d3d 3d3d 3d3d 0a0a 0a28 3129 2043  ========...(1) C
+000021b0: 6f6e 6669 6775 7269 6e67 2041 5753 3a0a  onfiguring AWS:.
+000021c0: 2020 2020 4c6f 6164 6564 2041 5753 2063      Loaded AWS c
+000021d0: 7265 6465 6e74 6961 6c73 2066 726f 6d20  redentials from 
+000021e0: 7468 6520 4157 5320 434c 4920 5b49 414d  the AWS CLI [IAM
+000021f0: 2061 6363 6573 7320 6b65 7920 4944 3a20   access key ID: 
+00002200: 2e2e 2e58 5858 5858 585d 0a20 2020 2041  ...XXXXXX].    A
+00002210: 5753 2072 6567 696f 6e20 636f 6e66 6967  WS region config
+00002220: 2066 696c 6520 7361 7665 6420 746f 202f   file saved to /
+00002230: 686f 6d65 2f75 6275 6e74 752f 2e73 6b79  home/ubuntu/.sky
+00002240: 706c 616e 652f 6177 735f 636f 6e66 6967  plane/aws_config
+00002250: 0a0a 2832 2920 436f 6e66 6967 7572 696e  ..(2) Configurin
+00002260: 6720 417a 7572 653a 0a20 2020 2041 7a75  g Azure:.    Azu
+00002270: 7265 2063 7265 6465 6e74 6961 6c73 2066  re credentials f
+00002280: 6f75 6e64 2069 6e20 417a 7572 6520 434c  ound in Azure CL
+00002290: 490a 2020 2020 417a 7572 6520 6372 6564  I.    Azure cred
+000022a0: 656e 7469 616c 7320 666f 756e 642c 2064  entials found, d
+000022b0: 6f20 796f 7520 7761 6e74 2074 6f20 656e  o you want to en
+000022c0: 6162 6c65 2041 7a75 7265 2073 7570 706f  able Azure suppo
+000022d0: 7274 2069 6e20 536b 7970 6c61 6e65 3f20  rt in Skyplane? 
+000022e0: 5b59 2f6e 5d3a 2059 0a20 2020 2045 6e74  [Y/n]: Y.    Ent
+000022f0: 6572 2074 6865 2041 7a75 7265 2073 7562  er the Azure sub
+00002300: 7363 7269 7074 696f 6e20 4944 3a20 5b58  scription ID: [X
+00002310: 5858 5858 5858 582d 5858 5858 2d58 5858  XXXXXXX-XXXX-XXX
+00002320: 582d 5858 5858 2d58 5858 5858 5858 5858  X-XXXX-XXXXXXXXX
+00002330: 5858 585d 3a0a 2020 2020 417a 7572 6520  XXX]:.    Azure 
+00002340: 7265 6769 6f6e 2063 6f6e 6669 6720 6669  region config fi
+00002350: 6c65 2073 6176 6564 2074 6f20 2f68 6f6d  le saved to /hom
+00002360: 652f 7562 756e 7475 2f2e 736b 7970 6c61  e/ubuntu/.skypla
+00002370: 6e65 2f61 7a75 7265 5f63 6f6e 6669 670a  ne/azure_config.
+00002380: 2020 2020 5175 6572 7969 6e67 2066 6f72      Querying for
+00002390: 2053 4b55 2061 7661 696c 6269 6c69 7479   SKU availbility
+000023a0: 2069 6e20 7265 6769 6f6e 730a 2020 2020   in regions.    
+000023b0: 417a 7572 6520 534b 5520 6176 6169 6c61  Azure SKU availa
+000023c0: 6269 6c69 7479 2063 6163 6865 6420 696e  bility cached in
+000023d0: 202f 686f 6d65 2f75 6275 6e74 752f 2e73   /home/ubuntu/.s
+000023e0: 6b79 706c 616e 652f 617a 7572 655f 736b  kyplane/azure_sk
+000023f0: 755f 6d61 7070 696e 670a 0a28 3329 2043  u_mapping..(3) C
+00002400: 6f6e 6669 6775 7269 6e67 2047 4350 3a0a  onfiguring GCP:.
+00002410: 2020 2020 4743 5020 6372 6564 656e 7469      GCP credenti
+00002420: 616c 7320 666f 756e 6420 696e 2047 4350  als found in GCP
+00002430: 2043 4c49 0a20 2020 2047 4350 2063 7265   CLI.    GCP cre
+00002440: 6465 6e74 6961 6c73 2066 6f75 6e64 2c20  dentials found, 
+00002450: 646f 2079 6f75 2077 616e 7420 746f 2065  do you want to e
+00002460: 6e61 626c 6520 4743 5020 7375 7070 6f72  nable GCP suppor
+00002470: 7420 696e 2053 6b79 706c 616e 653f 205b  t in Skyplane? [
+00002480: 592f 6e5d 3a20 590a 2020 2020 456e 7465  Y/n]: Y.    Ente
+00002490: 7220 7468 6520 4743 5020 7072 6f6a 6563  r the GCP projec
+000024a0: 7420 4944 205b 5858 5858 5858 585d 3a0a  t ID [XXXXXXX]:.
+000024b0: 2020 2020 4743 5020 7265 6769 6f6e 2063      GCP region c
+000024c0: 6f6e 6669 6720 6669 6c65 2073 6176 6564  onfig file saved
+000024d0: 2074 6f20 2f68 6f6d 652f 7562 756e 7475   to /home/ubuntu
+000024e0: 2f2e 736b 7970 6c61 6e65 2f67 6370 5f63  /.skyplane/gcp_c
+000024f0: 6f6e 6669 670a 0a43 6f6e 6669 6720 6669  onfig..Config fi
+00002500: 6c65 2073 6176 6564 2074 6f20 2f68 6f6d  le saved to /hom
+00002510: 652f 7562 756e 7475 2f2e 736b 7970 6c61  e/ubuntu/.skypla
+00002520: 6e65 2f63 6f6e 6669 670a 6060 600a 0a3c  ne/config.```..<
+00002530: 2f64 6574 6169 6c73 3e0a 0a23 2320 332e  /details>..## 3.
+00002540: 2052 756e 2054 7261 6e73 6665 7273 200a   Run Transfers .
+00002550: 0a57 65e2 8099 7265 2072 6561 6479 2074  .We...re ready t
+00002560: 6f20 7573 6520 536b 7970 6c61 6e65 2120  o use Skyplane! 
+00002570: 4c65 74e2 8099 7320 7573 6520 6073 6b79  Let...s use `sky
+00002580: 706c 616e 6520 6370 6020 746f 2063 6f70  plane cp` to cop
+00002590: 7920 6669 6c65 7320 6672 6f6d 2041 5753  y files from AWS
+000025a0: 2074 6f20 4743 503a 0a60 6060 0a73 6b79   to GCP:.```.sky
+000025b0: 706c 616e 6520 6370 2073 333a 2f2f 2e2e  plane cp s3://..
+000025c0: 2e20 6773 3a2f 2f2e 2e2e 0a60 6060 0a54  . gs://....```.T
+000025d0: 6f20 7472 616e 7366 6572 206f 6e6c 7920  o transfer only 
+000025e0: 6e65 7720 6f62 6a65 6374 732c 2079 6f75  new objects, you
+000025f0: 2063 616e 2069 6e73 7465 6164 2075 7365   can instead use
+00002600: 2060 736b 7970 6c61 6e65 2073 796e 6360   `skyplane sync`
+00002610: 3a0a 6060 600a 2420 736b 7970 6c61 6e65  :.```.$ skyplane
+00002620: 2073 796e 6320 7333 3a2f 2f2e 2e2e 2067   sync s3://... g
+00002630: 733a 2f2f 2e2e 2e0a 6060 600a 0a59 6f75  s://....```..You
+00002640: 2063 616e 2063 6f6e 6669 6775 7265 2053   can configure S
+00002650: 6b79 706c 616e 6520 746f 2075 7365 206d  kyplane to use m
+00002660: 6f72 6520 564d 7320 7065 7220 7265 6769  ore VMs per regi
+00002670: 6f6e 2077 6974 6820 7468 6520 602d 6e60  on with the `-n`
+00002680: 2066 6c61 672e 2046 6f72 2065 7861 6d70   flag. For examp
+00002690: 6c65 2c20 746f 2064 6f75 626c 6520 7468  le, to double th
+000026a0: 6520 7472 616e 7366 6572 2073 7065 6564  e transfer speed
+000026b0: 2077 6974 6820 7477 6f20 564d 732c 2072   with two VMs, r
+000026c0: 756e 3a20 0a60 6060 0a24 2073 6b79 706c  un: .```.$ skypl
+000026d0: 616e 6520 6370 202d 7220 7333 3a2f 2f2e  ane cp -r s3://.
+000026e0: 2e2e 2073 333a 2f2f 2e2e 2e20 2d6e 2032  .. s3://... -n 2
+000026f0: 0a60 6060 0a0a 2323 2034 2e20 436c 6561  .```..## 4. Clea
+00002700: 6e20 5570 200a 536b 7970 6c61 6e65 2077  n Up .Skyplane w
+00002710: 696c 6c20 6175 746f 6d61 7469 6361 6c6c  ill automaticall
+00002720: 7920 6174 7465 6d70 7420 746f 2074 6572  y attempt to ter
+00002730: 6d69 6e61 7465 2056 4d73 2074 6861 7420  minate VMs that 
+00002740: 6974 2073 7461 7274 732c 2062 7574 2074  it starts, but t
+00002750: 6f20 646f 7562 6c65 2063 6865 636b 2061  o double check a
+00002760: 6e64 2066 6f72 6365 6675 6c79 2074 6572  nd forcefuly ter
+00002770: 6d69 6e61 7465 2061 6c6c 2056 4d73 2c20  minate all VMs, 
+00002780: 7275 6e20 6073 6b79 706c 616e 6520 6465  run `skyplane de
+00002790: 7072 6f76 6973 696f 6e60 2e0a 0a23 2054  provision`...# T
+000027a0: 6563 686e 6963 616c 2044 6574 6169 6c73  echnical Details
+000027b0: 0a53 6b79 706c 616e 6520 6973 2062 6173  .Skyplane is bas
+000027c0: 6564 206f 6e20 7265 7365 6172 6368 2061  ed on research a
+000027d0: 7420 5543 2042 6572 6b65 6c65 7920 696e  t UC Berkeley in
+000027e0: 746f 2061 6363 656c 6572 6174 6564 206e  to accelerated n
+000027f0: 6574 776f 726b 7320 6265 7477 6565 6e20  etworks between 
+00002800: 636c 6f75 6420 7072 6f76 6964 6572 732e  cloud providers.
+00002810: 2055 6e64 6572 2074 6865 2068 6f6f 642c   Under the hood,
+00002820: 2053 6b79 706c 616e 6520 7374 6172 7473   Skyplane starts
+00002830: 2061 2066 6c65 6574 206f 6620 564d 7320   a fleet of VMs 
+00002840: 696e 2074 6865 2073 6f75 7263 6520 616e  in the source an
+00002850: 6420 6465 7374 696e 6174 696f 6e20 7265  d destination re
+00002860: 6769 6f6e 732e 2049 7420 7468 656e 2075  gions. It then u
+00002870: 7365 7320 6120 6375 7374 6f6d 2054 4350  ses a custom TCP
+00002880: 2070 726f 746f 636f 6c20 746f 2061 6363   protocol to acc
+00002890: 656c 6572 6174 6520 7468 6520 7472 616e  elerate the tran
+000028a0: 7366 6572 2062 6574 7765 656e 2074 6865  sfer between the
+000028b0: 2056 4d73 2e20 536b 7970 6c61 6e65 206d   VMs. Skyplane m
+000028c0: 6179 2075 7365 2061 204c 3720 6f76 6572  ay use a L7 over
+000028d0: 6c61 7920 6e65 7477 6f72 6b20 746f 2072  lay network to r
+000028e0: 6f75 7465 2074 7261 6666 6963 2061 726f  oute traffic aro
+000028f0: 756e 6420 636f 6e67 6573 7465 6420 6e65  und congested ne
+00002900: 7477 6f72 6b20 686f 7420 7370 6f74 732e  twork hot spots.
+00002910: 200a 0a3c 696d 6720 7372 633d 2264 6f63   ..<img src="doc
+00002920: 732f 5f73 7461 7469 632f 736b 7970 6c61  s/_static/skypla
+00002930: 6e65 2d64 6174 612d 706c 616e 652e 706e  ne-data-plane.pn
+00002940: 6722 2077 6964 7468 3d22 3338 3422 202f  g" width="384" /
+00002950: 3e0a 0a46 6f72 206d 6f72 6520 6465 7461  >..For more deta
+00002960: 696c 7320 6f6e 2053 6b79 706c 616e 652c  ils on Skyplane,
+00002970: 2073 6565 3a20 0a2d 205b 5465 6368 6e69   see: .- [Techni
+00002980: 6361 6c20 5461 6c6b 5d28 6874 7470 733a  cal Talk](https:
+00002990: 2f2f 736b 7970 6c61 6e65 2e6f 7267 2f65  //skyplane.org/e
+000029a0: 6e2f 6c61 7465 7374 2f61 7263 6869 7465  n/latest/archite
+000029b0: 6374 7572 652e 6874 6d6c 290a 2d20 5b4e  cture.html).- [N
+000029c0: 5344 4920 2732 3320 5061 7065 725d 2868  SDI '23 Paper](h
+000029d0: 7474 7073 3a2f 2f61 7278 6976 2e6f 7267  ttps://arxiv.org
+000029e0: 2f61 6273 2f32 3231 302e 3037 3235 3929  /abs/2210.07259)
+000029f0: 0a0a 0a0a                                ....
```

