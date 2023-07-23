# Comparing `tmp/stigg_api_client_v2-0.496.0.tar.gz` & `tmp/stigg_api_client_v2-0.499.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "stigg_api_client_v2-0.496.0.tar", max compression
+gzip compressed data, was "stigg_api_client_v2-0.499.0.tar", max compression
```

## Comparing `stigg_api_client_v2-0.496.0.tar` & `stigg_api_client_v2-0.499.0.tar`

### file list

```diff
@@ -1,44 +1,44 @@
--rw-r--r--   0        0        0     1644 2023-07-20 15:44:04.911350 stigg_api_client_v2-0.496.0/README.md
--rw-r--r--   0        0        0      432 2023-07-20 15:44:49.271891 stigg_api_client_v2-0.496.0/pyproject.toml
--rw-r--r--   0        0        0       62 2023-07-20 15:44:04.915350 stigg_api_client_v2-0.496.0/stigg/__init__.py
--rw-r--r--   0        0        0     1520 2023-07-20 15:44:04.915350 stigg_api_client_v2-0.496.0/stigg/client.py
--rw-r--r--   0        0        0    40178 2023-07-20 15:44:47.591872 stigg_api_client_v2-0.496.0/stigg/generated/__init__.py
--rw-r--r--   0        0        0      460 2023-07-20 15:44:46.343873 stigg_api_client_v2-0.496.0/stigg/generated/archive_customer.py
--rw-r--r--   0        0        0     7303 2023-07-20 15:44:47.211871 stigg_api_client_v2-0.496.0/stigg/generated/async_base_client.py
--rw-r--r--   0        0        0    68230 2023-07-20 15:44:47.431871 stigg_api_client_v2-0.496.0/stigg/generated/async_client.py
--rw-r--r--   0        0        0     2731 2023-07-20 15:44:42.283854 stigg_api_client_v2-0.496.0/stigg/generated/base_client.py
--rw-r--r--   0        0        0     1951 2023-07-20 15:44:47.211871 stigg_api_client_v2-0.496.0/stigg/generated/base_model.py
--rw-r--r--   0        0        0      527 2023-07-20 15:44:46.291874 stigg_api_client_v2-0.496.0/stigg/generated/cancel_subscription.py
--rw-r--r--   0        0        0      296 2023-07-20 15:44:46.307873 stigg_api_client_v2-0.496.0/stigg/generated/cancel_subscription_updates.py
--rw-r--r--   0        0        0    67803 2023-07-20 15:44:42.503857 stigg_api_client_v2-0.496.0/stigg/generated/client.py
--rw-r--r--   0        0        0      527 2023-07-20 15:44:46.331873 stigg_api_client_v2-0.496.0/stigg/generated/create_subscription.py
--rw-r--r--   0        0        0    24160 2023-07-20 15:44:44.007876 stigg_api_client_v2-0.496.0/stigg/generated/enums.py
--rw-r--r--   0        0        0      553 2023-07-20 15:44:46.295873 stigg_api_client_v2-0.496.0/stigg/generated/estimate_subscription.py
--rw-r--r--   0        0        0      614 2023-07-20 15:44:46.303873 stigg_api_client_v2-0.496.0/stigg/generated/estimate_subscription_update.py
--rw-r--r--   0        0        0     2366 2023-07-20 15:44:47.211871 stigg_api_client_v2-0.496.0/stigg/generated/exceptions.py
--rw-r--r--   0        0        0    56292 2023-07-20 15:44:47.207871 stigg_api_client_v2-0.496.0/stigg/generated/fragments.py
--rw-r--r--   0        0        0      591 2023-07-20 15:44:46.359873 stigg_api_client_v2-0.496.0/stigg/generated/get_active_subscriptions.py
--rw-r--r--   0        0        0      634 2023-07-20 15:44:46.367873 stigg_api_client_v2-0.496.0/stigg/generated/get_coupons.py
--rw-r--r--   0        0        0      572 2023-07-20 15:44:46.351873 stigg_api_client_v2-0.496.0/stigg/generated/get_customer_by_id.py
--rw-r--r--   0        0        0      533 2023-07-20 15:44:46.403873 stigg_api_client_v2-0.496.0/stigg/generated/get_customer_portal_by_ref_id.py
--rw-r--r--   0        0        0      390 2023-07-20 15:44:46.383873 stigg_api_client_v2-0.496.0/stigg/generated/get_entitlement.py
--rw-r--r--   0        0        0      430 2023-07-20 15:44:46.375873 stigg_api_client_v2-0.496.0/stigg/generated/get_entitlements.py
--rw-r--r--   0        0        0      893 2023-07-20 15:44:46.415873 stigg_api_client_v2-0.496.0/stigg/generated/get_mock_paywall.py
--rw-r--r--   0        0        0      346 2023-07-20 15:44:46.371873 stigg_api_client_v2-0.496.0/stigg/generated/get_paywall.py
--rw-r--r--   0        0        0      657 2023-07-20 15:44:46.387873 stigg_api_client_v2-0.496.0/stigg/generated/get_products.py
--rw-r--r--   0        0        0      650 2023-07-20 15:44:46.399873 stigg_api_client_v2-0.496.0/stigg/generated/get_sdk_configuration.py
--rw-r--r--   0        0        0      465 2023-07-20 15:44:46.259873 stigg_api_client_v2-0.496.0/stigg/generated/import_customer.py
--rw-r--r--   0        0        0      332 2023-07-20 15:44:46.251874 stigg_api_client_v2-0.496.0/stigg/generated/import_customer_bulk.py
--rw-r--r--   0        0        0      350 2023-07-20 15:44:46.279873 stigg_api_client_v2-0.496.0/stigg/generated/import_subscriptions_bulk.py
--rw-r--r--   0        0        0   126537 2023-07-20 15:44:46.235874 stigg_api_client_v2-0.496.0/stigg/generated/input_types.py
--rw-r--r--   0        0        0      604 2023-07-20 15:44:46.339873 stigg_api_client_v2-0.496.0/stigg/generated/migrate_subscription_to_latest.py
--rw-r--r--   0        0        0     1161 2023-07-20 15:44:46.247874 stigg_api_client_v2-0.496.0/stigg/generated/provision_customer.py
--rw-r--r--   0        0        0      971 2023-07-20 15:44:46.271874 stigg_api_client_v2-0.496.0/stigg/generated/provision_subscription.py
--rw-r--r--   0        0        0      359 2023-07-20 15:44:46.327873 stigg_api_client_v2-0.496.0/stigg/generated/report_entitlement_check_requested.py
--rw-r--r--   0        0        0      301 2023-07-20 15:44:46.319873 stigg_api_client_v2-0.496.0/stigg/generated/report_event.py
--rw-r--r--   0        0        0      637 2023-07-20 15:44:46.315873 stigg_api_client_v2-0.496.0/stigg/generated/report_usage.py
--rw-r--r--   0        0        0      220 2023-07-20 15:44:47.215871 stigg_api_client_v2-0.496.0/stigg/generated/scalars.py
--rw-r--r--   0        0        0      465 2023-07-20 15:44:46.263874 stigg_api_client_v2-0.496.0/stigg/generated/update_customer.py
--rw-r--r--   0        0        0      527 2023-07-20 15:44:46.283873 stigg_api_client_v2-0.496.0/stigg/generated/update_subscription.py
--rw-r--r--   0        0        0      445 2023-07-20 15:44:46.419873 stigg_api_client_v2-0.496.0/stigg/generated/usage_history.py
--rw-r--r--   0        0        0     2034 1970-01-01 00:00:00.000000 stigg_api_client_v2-0.496.0/PKG-INFO
+-rw-r--r--   0        0        0     1644 2023-07-23 07:18:22.431760 stigg_api_client_v2-0.499.0/README.md
+-rw-r--r--   0        0        0      432 2023-07-23 07:19:06.724995 stigg_api_client_v2-0.499.0/pyproject.toml
+-rw-r--r--   0        0        0       62 2023-07-23 07:18:22.435760 stigg_api_client_v2-0.499.0/stigg/__init__.py
+-rw-r--r--   0        0        0     1520 2023-07-23 07:18:22.435760 stigg_api_client_v2-0.499.0/stigg/client.py
+-rw-r--r--   0        0        0    40178 2023-07-23 07:19:04.972950 stigg_api_client_v2-0.499.0/stigg/generated/__init__.py
+-rw-r--r--   0        0        0      460 2023-07-23 07:19:03.688917 stigg_api_client_v2-0.499.0/stigg/generated/archive_customer.py
+-rw-r--r--   0        0        0     7303 2023-07-23 07:19:04.592940 stigg_api_client_v2-0.499.0/stigg/generated/async_base_client.py
+-rw-r--r--   0        0        0    68230 2023-07-23 07:19:04.812945 stigg_api_client_v2-0.499.0/stigg/generated/async_client.py
+-rw-r--r--   0        0        0     2731 2023-07-23 07:18:59.436806 stigg_api_client_v2-0.499.0/stigg/generated/base_client.py
+-rw-r--r--   0        0        0     1951 2023-07-23 07:19:04.592940 stigg_api_client_v2-0.499.0/stigg/generated/base_model.py
+-rw-r--r--   0        0        0      527 2023-07-23 07:19:03.632915 stigg_api_client_v2-0.499.0/stigg/generated/cancel_subscription.py
+-rw-r--r--   0        0        0      296 2023-07-23 07:19:03.652916 stigg_api_client_v2-0.499.0/stigg/generated/cancel_subscription_updates.py
+-rw-r--r--   0        0        0    67803 2023-07-23 07:18:59.664812 stigg_api_client_v2-0.499.0/stigg/generated/client.py
+-rw-r--r--   0        0        0      527 2023-07-23 07:19:03.676916 stigg_api_client_v2-0.499.0/stigg/generated/create_subscription.py
+-rw-r--r--   0        0        0    24160 2023-07-23 07:19:01.252853 stigg_api_client_v2-0.499.0/stigg/generated/enums.py
+-rw-r--r--   0        0        0      553 2023-07-23 07:19:03.640915 stigg_api_client_v2-0.499.0/stigg/generated/estimate_subscription.py
+-rw-r--r--   0        0        0      614 2023-07-23 07:19:03.648916 stigg_api_client_v2-0.499.0/stigg/generated/estimate_subscription_update.py
+-rw-r--r--   0        0        0     2366 2023-07-23 07:19:04.592940 stigg_api_client_v2-0.499.0/stigg/generated/exceptions.py
+-rw-r--r--   0        0        0    56292 2023-07-23 07:19:04.592940 stigg_api_client_v2-0.499.0/stigg/generated/fragments.py
+-rw-r--r--   0        0        0      591 2023-07-23 07:19:03.704917 stigg_api_client_v2-0.499.0/stigg/generated/get_active_subscriptions.py
+-rw-r--r--   0        0        0      634 2023-07-23 07:19:03.712917 stigg_api_client_v2-0.499.0/stigg/generated/get_coupons.py
+-rw-r--r--   0        0        0      572 2023-07-23 07:19:03.696917 stigg_api_client_v2-0.499.0/stigg/generated/get_customer_by_id.py
+-rw-r--r--   0        0        0      533 2023-07-23 07:19:03.748918 stigg_api_client_v2-0.499.0/stigg/generated/get_customer_portal_by_ref_id.py
+-rw-r--r--   0        0        0      390 2023-07-23 07:19:03.728918 stigg_api_client_v2-0.499.0/stigg/generated/get_entitlement.py
+-rw-r--r--   0        0        0      430 2023-07-23 07:19:03.720917 stigg_api_client_v2-0.499.0/stigg/generated/get_entitlements.py
+-rw-r--r--   0        0        0      893 2023-07-23 07:19:03.760918 stigg_api_client_v2-0.499.0/stigg/generated/get_mock_paywall.py
+-rw-r--r--   0        0        0      346 2023-07-23 07:19:03.716917 stigg_api_client_v2-0.499.0/stigg/generated/get_paywall.py
+-rw-r--r--   0        0        0      657 2023-07-23 07:19:03.736918 stigg_api_client_v2-0.499.0/stigg/generated/get_products.py
+-rw-r--r--   0        0        0      650 2023-07-23 07:19:03.744918 stigg_api_client_v2-0.499.0/stigg/generated/get_sdk_configuration.py
+-rw-r--r--   0        0        0      465 2023-07-23 07:19:03.600914 stigg_api_client_v2-0.499.0/stigg/generated/import_customer.py
+-rw-r--r--   0        0        0      332 2023-07-23 07:19:03.596914 stigg_api_client_v2-0.499.0/stigg/generated/import_customer_bulk.py
+-rw-r--r--   0        0        0      350 2023-07-23 07:19:03.620915 stigg_api_client_v2-0.499.0/stigg/generated/import_subscriptions_bulk.py
+-rw-r--r--   0        0        0   126604 2023-07-23 07:19:03.576914 stigg_api_client_v2-0.499.0/stigg/generated/input_types.py
+-rw-r--r--   0        0        0      604 2023-07-23 07:19:03.684916 stigg_api_client_v2-0.499.0/stigg/generated/migrate_subscription_to_latest.py
+-rw-r--r--   0        0        0     1161 2023-07-23 07:19:03.588914 stigg_api_client_v2-0.499.0/stigg/generated/provision_customer.py
+-rw-r--r--   0        0        0      971 2023-07-23 07:19:03.616915 stigg_api_client_v2-0.499.0/stigg/generated/provision_subscription.py
+-rw-r--r--   0        0        0      359 2023-07-23 07:19:03.668916 stigg_api_client_v2-0.499.0/stigg/generated/report_entitlement_check_requested.py
+-rw-r--r--   0        0        0      301 2023-07-23 07:19:03.664916 stigg_api_client_v2-0.499.0/stigg/generated/report_event.py
+-rw-r--r--   0        0        0      637 2023-07-23 07:19:03.660916 stigg_api_client_v2-0.499.0/stigg/generated/report_usage.py
+-rw-r--r--   0        0        0      220 2023-07-23 07:19:04.596940 stigg_api_client_v2-0.499.0/stigg/generated/scalars.py
+-rw-r--r--   0        0        0      465 2023-07-23 07:19:03.608914 stigg_api_client_v2-0.499.0/stigg/generated/update_customer.py
+-rw-r--r--   0        0        0      527 2023-07-23 07:19:03.628915 stigg_api_client_v2-0.499.0/stigg/generated/update_subscription.py
+-rw-r--r--   0        0        0      445 2023-07-23 07:19:03.764918 stigg_api_client_v2-0.499.0/stigg/generated/usage_history.py
+-rw-r--r--   0        0        0     2034 1970-01-01 00:00:00.000000 stigg_api_client_v2-0.499.0/PKG-INFO
```

### Comparing `stigg_api_client_v2-0.496.0/README.md` & `stigg_api_client_v2-0.499.0/README.md`

 * *Files identical despite different names*

### Comparing `stigg_api_client_v2-0.496.0/stigg/client.py` & `stigg_api_client_v2-0.499.0/stigg/client.py`

 * *Files identical despite different names*

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/__init__.py` & `stigg_api_client_v2-0.499.0/stigg/generated/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 
 from .archive_customer import ArchiveCustomer, ArchiveCustomerArchiveCustomer
 from .async_base_client import AsyncBaseClient
 from .async_client import AsyncClient
 from .base_model import BaseModel
 from .cancel_subscription import (
     CancelSubscription,
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/async_base_client.py` & `stigg_api_client_v2-0.499.0/stigg/generated/async_base_client.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 
 import enum
 import json
 from typing import Any, AsyncIterator, Dict, Optional, TypeVar, cast
 from uuid import uuid4
 
 import httpx
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/async_client.py` & `stigg_api_client_v2-0.499.0/stigg/generated/async_client.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from .archive_customer import ArchiveCustomer
 from .async_base_client import AsyncBaseClient
 from .cancel_subscription import CancelSubscription
 from .cancel_subscription_updates import CancelSubscriptionUpdates
 from .create_subscription import CreateSubscription
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/base_client.py` & `stigg_api_client_v2-0.499.0/stigg/generated/base_client.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:18
 
 import json
 from typing import Any, Dict, Optional, TypeVar, cast
 
 import httpx
 from pydantic import BaseModel
 from pydantic.json import pydantic_encoder
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/base_model.py` & `stigg_api_client_v2-0.499.0/stigg/generated/base_model.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 
 from typing import Any, Dict, Type, Union, get_args, get_origin
 
 from pydantic import BaseModel as PydanticBaseModel
 from pydantic.class_validators import validator
 from pydantic.fields import ModelField
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/cancel_subscription.py` & `stigg_api_client_v2-0.499.0/stigg/generated/cancel_subscription.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from pydantic import Field
 
 from .base_model import BaseModel
 from .fragments import SlimSubscriptionFragment
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/client.py` & `stigg_api_client_v2-0.499.0/stigg/generated/client.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:18
 # Source: operations.graphql
 
 from .archive_customer import ArchiveCustomer
 from .base_client import BaseClient
 from .cancel_subscription import CancelSubscription
 from .cancel_subscription_updates import CancelSubscriptionUpdates
 from .create_subscription import CreateSubscription
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/create_subscription.py` & `stigg_api_client_v2-0.499.0/stigg/generated/create_subscription.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from pydantic import Field
 
 from .base_model import BaseModel
 from .fragments import SlimSubscriptionFragment
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/enums.py` & `stigg_api_client_v2-0.499.0/stigg/generated/enums.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: ../api-client-schema/src/generated/schema.graphql
 
 from enum import Enum
 
 
 class AccessDeniedReason(str, Enum):
     CustomerIsArchived = "CustomerIsArchived"
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/estimate_subscription.py` & `stigg_api_client_v2-0.499.0/stigg/generated/estimate_subscription.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from pydantic import Field
 
 from .base_model import BaseModel
 from .fragments import SubscriptionPreviewFragment
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/estimate_subscription_update.py` & `stigg_api_client_v2-0.499.0/stigg/generated/estimate_subscription_update.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from pydantic import Field
 
 from .base_model import BaseModel
 from .fragments import SubscriptionPreviewFragment
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/exceptions.py` & `stigg_api_client_v2-0.499.0/stigg/generated/exceptions.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 
 from typing import Any, Dict, List, Optional, Union
 
 import httpx
 
 
 class GraphQLClientError(Exception):
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/fragments.py` & `stigg_api_client_v2-0.499.0/stigg/generated/fragments.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from typing import Annotated, Any, List, Literal, Optional, Union
 
 from pydantic import Field
 
 from .base_model import BaseModel
@@ -32,36 +32,14 @@
     VendorIdentifier,
     WeeklyAccordingTo,
     WidgetType,
     experimentGroupType,
 )
 
 
-class PackageEntitlementFragment(BaseModel):
-    usage_limit: Optional[float] = Field(alias="usageLimit")
-    has_unlimited_usage: Optional[bool] = Field(alias="hasUnlimitedUsage")
-    feature_id: str = Field(alias="featureId")
-    reset_period: Optional[EntitlementResetPeriod] = Field(alias="resetPeriod")
-    hidden_from_widgets: Optional[List[WidgetType]] = Field(alias="hiddenFromWidgets")
-    is_custom: Optional[bool] = Field(alias="isCustom")
-    display_name_override: Optional[str] = Field(alias="displayNameOverride")
-    feature: "PackageEntitlementFragmentFeature"
-
-
-class PackageEntitlementFragmentFeature(BaseModel):
-    feature_type: FeatureType = Field(alias="featureType")
-    meter_type: Optional[MeterType] = Field(alias="meterType")
-    feature_units: Optional[str] = Field(alias="featureUnits")
-    feature_units_plural: Optional[str] = Field(alias="featureUnitsPlural")
-    display_name: str = Field(alias="displayName")
-    description: Optional[str]
-    ref_id: str = Field(alias="refId")
-    additional_meta_data: Optional[Any] = Field(alias="additionalMetaData")
-
-
 class PriceFragment(BaseModel):
     billing_model: BillingModel = Field(alias="billingModel")
     billing_period: BillingPeriod = Field(alias="billingPeriod")
     billing_id: Optional[str] = Field(alias="billingId")
     min_unit_quantity: Optional[float] = Field(alias="minUnitQuantity")
     max_unit_quantity: Optional[float] = Field(alias="maxUnitQuantity")
     billing_country_code: Optional[str] = Field(alias="billingCountryCode")
@@ -78,14 +56,36 @@
     ref_id: str = Field(alias="refId")
     feature_units: Optional[str] = Field(alias="featureUnits")
     feature_units_plural: Optional[str] = Field(alias="featureUnitsPlural")
     display_name: str = Field(alias="displayName")
     description: Optional[str]
 
 
+class PackageEntitlementFragment(BaseModel):
+    usage_limit: Optional[float] = Field(alias="usageLimit")
+    has_unlimited_usage: Optional[bool] = Field(alias="hasUnlimitedUsage")
+    feature_id: str = Field(alias="featureId")
+    reset_period: Optional[EntitlementResetPeriod] = Field(alias="resetPeriod")
+    hidden_from_widgets: Optional[List[WidgetType]] = Field(alias="hiddenFromWidgets")
+    is_custom: Optional[bool] = Field(alias="isCustom")
+    display_name_override: Optional[str] = Field(alias="displayNameOverride")
+    feature: "PackageEntitlementFragmentFeature"
+
+
+class PackageEntitlementFragmentFeature(BaseModel):
+    feature_type: FeatureType = Field(alias="featureType")
+    meter_type: Optional[MeterType] = Field(alias="meterType")
+    feature_units: Optional[str] = Field(alias="featureUnits")
+    feature_units_plural: Optional[str] = Field(alias="featureUnitsPlural")
+    display_name: str = Field(alias="displayName")
+    description: Optional[str]
+    ref_id: str = Field(alias="refId")
+    additional_meta_data: Optional[Any] = Field(alias="additionalMetaData")
+
+
 class AddonFragment(BaseModel):
     id: str
     ref_id: str = Field(alias="refId")
     billing_id: Optional[str] = Field(alias="billingId")
     display_name: str = Field(alias="displayName")
     description: Optional[str]
     additional_meta_data: Optional[Any] = Field(alias="additionalMetaData")
@@ -125,25 +125,14 @@
     status: SyncStatus
 
 
 class CouponFragmentCustomers(BaseModel):
     id: str
 
 
-class SlimCustomerFragment(BaseModel):
-    id: str
-    name: Optional[str]
-    email: Optional[str]
-    created_at: Optional[Any] = Field(alias="createdAt")
-    updated_at: Any = Field(alias="updatedAt")
-    ref_id: str = Field(alias="refId")
-    billing_id: Optional[str] = Field(alias="billingId")
-    additional_meta_data: Optional[Any] = Field(alias="additionalMetaData")
-
-
 class PromotionalEntitlementFragment(BaseModel):
     status: PromotionalEntitlementStatus
     usage_limit: Optional[float] = Field(alias="usageLimit")
     feature_id: str = Field(alias="featureId")
     has_unlimited_usage: Optional[bool] = Field(alias="hasUnlimitedUsage")
     reset_period: Optional[EntitlementResetPeriod] = Field(alias="resetPeriod")
     end_date: Optional[Any] = Field(alias="endDate")
@@ -158,14 +147,25 @@
     feature_units_plural: Optional[str] = Field(alias="featureUnitsPlural")
     display_name: str = Field(alias="displayName")
     description: Optional[str]
     ref_id: str = Field(alias="refId")
     additional_meta_data: Optional[Any] = Field(alias="additionalMetaData")
 
 
+class SlimCustomerFragment(BaseModel):
+    id: str
+    name: Optional[str]
+    email: Optional[str]
+    created_at: Optional[Any] = Field(alias="createdAt")
+    updated_at: Any = Field(alias="updatedAt")
+    ref_id: str = Field(alias="refId")
+    billing_id: Optional[str] = Field(alias="billingId")
+    additional_meta_data: Optional[Any] = Field(alias="additionalMetaData")
+
+
 class CustomerFragment(SlimCustomerFragment):
     has_payment_method: bool = Field(alias="hasPaymentMethod")
     has_active_subscription: bool = Field(alias="hasActiveSubscription")
     default_payment_expiration_month: Optional[int] = Field(
         alias="defaultPaymentExpirationMonth"
     )
     default_payment_expiration_year: Optional[int] = Field(
@@ -342,34 +342,14 @@
     end_date: Optional[Any] = Field(alias="endDate")
 
 
 class CustomerResourceFragment(BaseModel):
     resource_id: str = Field(alias="resourceId")
 
 
-class CustomerPortalSubscriptionPriceFragment(BaseModel):
-    billing_period: Optional[BillingPeriod] = Field(alias="billingPeriod")
-    billing_model: Optional[BillingModel] = Field(alias="billingModel")
-    price: Optional["CustomerPortalSubscriptionPriceFragmentPrice"]
-    feature: Optional["CustomerPortalSubscriptionPriceFragmentFeature"]
-
-
-class CustomerPortalSubscriptionPriceFragmentPrice(BaseModel):
-    amount: float
-    currency: Currency
-
-
-class CustomerPortalSubscriptionPriceFragmentFeature(BaseModel):
-    id: str
-    ref_id: str = Field(alias="refId")
-    display_name: str = Field(alias="displayName")
-    feature_units: Optional[str] = Field(alias="featureUnits")
-    feature_units_plural: Optional[str] = Field(alias="featureUnitsPlural")
-
-
 class CustomerPortalSubscriptionScheduledUpdateData(BaseModel):
     subscription_schedule_type: SubscriptionScheduleType = Field(
         alias="subscriptionScheduleType"
     )
     schedule_status: SubscriptionScheduleStatus = Field(alias="scheduleStatus")
     scheduled_execution_time: Any = Field(alias="scheduledExecutionTime")
     target_package: Optional[
@@ -414,14 +394,34 @@
     BaseModel
 ):
     typename__: Literal["UnitAmountChangeVariables"] = Field(alias="__typename")
     new_unit_amount: Optional[float] = Field(alias="newUnitAmount")
     feature_id: Optional[str] = Field(alias="featureId")
 
 
+class CustomerPortalSubscriptionPriceFragment(BaseModel):
+    billing_period: Optional[BillingPeriod] = Field(alias="billingPeriod")
+    billing_model: Optional[BillingModel] = Field(alias="billingModel")
+    price: Optional["CustomerPortalSubscriptionPriceFragmentPrice"]
+    feature: Optional["CustomerPortalSubscriptionPriceFragmentFeature"]
+
+
+class CustomerPortalSubscriptionPriceFragmentPrice(BaseModel):
+    amount: float
+    currency: Currency
+
+
+class CustomerPortalSubscriptionPriceFragmentFeature(BaseModel):
+    id: str
+    ref_id: str = Field(alias="refId")
+    display_name: str = Field(alias="displayName")
+    feature_units: Optional[str] = Field(alias="featureUnits")
+    feature_units_plural: Optional[str] = Field(alias="featureUnitsPlural")
+
+
 class CustomerPortalSubscriptionAddon(BaseModel):
     addon_id: str = Field(alias="addonId")
     description: Optional[str]
     display_name: str = Field(alias="displayName")
     quantity: int
 
 
@@ -1341,28 +1341,28 @@
 
 class UsageHistoryFragmentUsageMeasurements(BaseModel):
     date: Any
     value: float
     is_reset_point: Optional[bool] = Field(alias="isResetPoint")
 
 
-PackageEntitlementFragment.update_forward_refs()
-PackageEntitlementFragmentFeature.update_forward_refs()
 PriceFragment.update_forward_refs()
 PriceFragmentPrice.update_forward_refs()
 PriceFragmentFeature.update_forward_refs()
+PackageEntitlementFragment.update_forward_refs()
+PackageEntitlementFragmentFeature.update_forward_refs()
 AddonFragment.update_forward_refs()
 AddonFragmentEntitlements.update_forward_refs()
 AddonFragmentPrices.update_forward_refs()
 CouponFragment.update_forward_refs()
 CouponFragmentSyncStates.update_forward_refs()
 CouponFragmentCustomers.update_forward_refs()
-SlimCustomerFragment.update_forward_refs()
 PromotionalEntitlementFragment.update_forward_refs()
 PromotionalEntitlementFragmentFeature.update_forward_refs()
+SlimCustomerFragment.update_forward_refs()
 CustomerFragment.update_forward_refs()
 CustomerFragmentTrialedPlans.update_forward_refs()
 CustomerFragmentExperimentInfo.update_forward_refs()
 CustomerFragmentCoupon.update_forward_refs()
 CustomerFragmentEligibleForTrial.update_forward_refs()
 CustomerFragmentPromotionalEntitlements.update_forward_refs()
 CustomerPortalBillingInformation.update_forward_refs()
@@ -1378,22 +1378,22 @@
 FeatureFragment.update_forward_refs()
 CustomerPortalEntitlement.update_forward_refs()
 CustomerPortalEntitlementResetPeriodConfigurationMonthlyResetPeriodConfig.update_forward_refs()
 CustomerPortalEntitlementResetPeriodConfigurationWeeklyResetPeriodConfig.update_forward_refs()
 CustomerPortalEntitlementFeature.update_forward_refs()
 CustomerPortalPromotionalEntitlement.update_forward_refs()
 CustomerResourceFragment.update_forward_refs()
-CustomerPortalSubscriptionPriceFragment.update_forward_refs()
-CustomerPortalSubscriptionPriceFragmentPrice.update_forward_refs()
-CustomerPortalSubscriptionPriceFragmentFeature.update_forward_refs()
 CustomerPortalSubscriptionScheduledUpdateData.update_forward_refs()
 CustomerPortalSubscriptionScheduledUpdateDataTargetPackage.update_forward_refs()
 CustomerPortalSubscriptionScheduledUpdateDataScheduleVariablesBillingPeriodChangeVariables.update_forward_refs()
 CustomerPortalSubscriptionScheduledUpdateDataScheduleVariablesDowngradeChangeVariables.update_forward_refs()
 CustomerPortalSubscriptionScheduledUpdateDataScheduleVariablesUnitAmountChangeVariables.update_forward_refs()
+CustomerPortalSubscriptionPriceFragment.update_forward_refs()
+CustomerPortalSubscriptionPriceFragmentPrice.update_forward_refs()
+CustomerPortalSubscriptionPriceFragmentFeature.update_forward_refs()
 CustomerPortalSubscriptionAddon.update_forward_refs()
 CustomerPortalSubscriptionFragment.update_forward_refs()
 CustomerPortalSubscriptionFragmentPrices.update_forward_refs()
 CustomerPortalSubscriptionFragmentPricing.update_forward_refs()
 CustomerPortalSubscriptionFragmentPricingPrice.update_forward_refs()
 CustomerPortalSubscriptionFragmentPricingFeature.update_forward_refs()
 CustomerPortalSubscriptionFragmentBillingPeriodRange.update_forward_refs()
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/get_active_subscriptions.py` & `stigg_api_client_v2-0.499.0/stigg/generated/get_active_subscriptions.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from typing import List
 
 from pydantic import Field
 
 from .base_model import BaseModel
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/get_coupons.py` & `stigg_api_client_v2-0.499.0/stigg/generated/get_coupons.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from typing import List
 
 from .base_model import BaseModel
 from .fragments import CouponFragment
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/get_customer_by_id.py` & `stigg_api_client_v2-0.499.0/stigg/generated/get_customer_by_id.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from typing import Optional
 
 from pydantic import Field
 
 from .base_model import BaseModel
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/get_customer_portal_by_ref_id.py` & `stigg_api_client_v2-0.499.0/stigg/generated/get_customer_portal_by_ref_id.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from pydantic import Field
 
 from .base_model import BaseModel
 from .fragments import CustomerPortalFragment
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/get_mock_paywall.py` & `stigg_api_client_v2-0.499.0/stigg/generated/get_mock_paywall.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from typing import List, Optional
 
 from pydantic import Field
 
 from .base_model import BaseModel
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/get_sdk_configuration.py` & `stigg_api_client_v2-0.499.0/stigg/generated/get_sdk_configuration.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from typing import Optional
 
 from pydantic import Field
 
 from .base_model import BaseModel
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/input_types.py` & `stigg_api_client_v2-0.499.0/stigg/generated/input_types.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: ../api-client-schema/src/generated/schema.graphql
 
 from typing import Any, List, Optional
 
 from pydantic import Field
 
 from .base_model import BaseModel
@@ -1085,14 +1085,15 @@
     font_weight: Optional[FontWeight] = Field(alias="fontWeight")
 
 
 class GetActiveSubscriptionsInput(BaseModel):
     customer_id: str = Field(alias="customerId")
     environment_id: Optional[str] = Field(alias="environmentId")
     resource_id: Optional[str] = Field(alias="resourceId")
+    resource_ids: Optional[List[str]] = Field(alias="resourceIds")
 
 
 class GetCustomerByRefIdInput(BaseModel):
     customer_id: str = Field(alias="customerId")
     environment_id: Optional[str] = Field(alias="environmentId")
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/migrate_subscription_to_latest.py` & `stigg_api_client_v2-0.499.0/stigg/generated/migrate_subscription_to_latest.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from pydantic import Field
 
 from .base_model import BaseModel
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/provision_customer.py` & `stigg_api_client_v2-0.499.0/stigg/generated/provision_customer.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from typing import Optional
 
 from pydantic import Field
 
 from .base_model import BaseModel
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/provision_subscription.py` & `stigg_api_client_v2-0.499.0/stigg/generated/provision_subscription.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from typing import Optional
 
 from pydantic import Field
 
 from .base_model import BaseModel
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/report_usage.py` & `stigg_api_client_v2-0.499.0/stigg/generated/report_usage.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from typing import Any, Optional
 
 from pydantic import Field
 
 from .base_model import BaseModel
```

### Comparing `stigg_api_client_v2-0.496.0/stigg/generated/update_subscription.py` & `stigg_api_client_v2-0.499.0/stigg/generated/update_subscription.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Generated by ariadne-codegen on 2023-07-20 15:44
+# Generated by ariadne-codegen on 2023-07-23 07:19
 # Source: operations.graphql
 
 from pydantic import Field
 
 from .base_model import BaseModel
 from .fragments import SlimSubscriptionFragment
```

### Comparing `stigg_api_client_v2-0.496.0/PKG-INFO` & `stigg_api_client_v2-0.499.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: stigg-api-client-v2
-Version: 0.496.0
+Version: 0.499.0
 Summary: 
 Author: Stigg
 Author-email: support@stigg.io
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

