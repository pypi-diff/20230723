# Comparing `tmp/stigg_api_client-0.499.0.tar.gz` & `tmp/stigg_api_client-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "stigg_api_client-0.499.0.tar", max compression
+gzip compressed data, was "stigg_api_client-0.5.0.tar", max compression
```

## Comparing `stigg_api_client-0.499.0.tar` & `stigg_api_client-0.5.0.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0     2479 2023-07-23 07:18:24.430588 stigg_api_client-0.499.0/README.md
--rw-r--r--   0        0        0      460 2023-07-23 07:18:58.663039 stigg_api_client-0.499.0/pyproject.toml
--rw-r--r--   0        0        0       44 2023-07-23 07:18:24.430588 stigg_api_client-0.499.0/stigg/__init__.py
--rw-r--r--   0        0        0     1141 2023-07-23 07:18:24.430588 stigg_api_client-0.499.0/stigg/client.py
--rw-r--r--   0        0        0        0 2023-07-23 07:18:56.759017 stigg_api_client-0.499.0/stigg/generated/__init__.py
--rw-r--r--   0        0        0    49477 2023-07-23 07:18:57.179022 stigg_api_client-0.499.0/stigg/generated/operations.py
--rw-r--r--   0        0        0   464368 2023-07-23 07:18:57.023020 stigg_api_client-0.499.0/stigg/generated/schema.py
--rw-r--r--   0        0        0     3081 1970-01-01 00:00:00.000000 stigg_api_client-0.499.0/PKG-INFO
+-rw-r--r--   0        0        0     2479 2023-03-05 12:25:06.526402 stigg_api_client-0.5.0/README.md
+-rw-r--r--   0        0        0      396 2023-04-24 14:47:14.271119 stigg_api_client-0.5.0/pyproject.toml
+-rw-r--r--   0        0        0       44 2023-04-23 10:33:15.442973 stigg_api_client-0.5.0/stigg/__init__.py
+-rw-r--r--   0        0        0     1141 2023-04-24 07:23:15.920589 stigg_api_client-0.5.0/stigg/client.py
+-rw-r--r--   0        0        0        0 2023-03-05 12:25:06.527730 stigg_api_client-0.5.0/stigg/generated/__init__.py
+-rw-r--r--   0        0        0    44689 2023-04-24 14:46:41.477637 stigg_api_client-0.5.0/stigg/generated/operations.py
+-rw-r--r--   0        0        0   443944 2023-04-24 14:46:41.312733 stigg_api_client-0.5.0/stigg/generated/schema.py
+-rw-r--r--   0        0        0     3159 1970-01-01 00:00:00.000000 stigg_api_client-0.5.0/PKG-INFO
```

### Comparing `stigg_api_client-0.499.0/README.md` & `stigg_api_client-0.5.0/README.md`

 * *Files identical despite different names*

### Comparing `stigg_api_client-0.499.0/stigg/client.py` & `stigg_api_client-0.5.0/stigg/client.py`

 * *Files identical despite different names*

### Comparing `stigg_api_client-0.499.0/stigg/generated/operations.py` & `stigg_api_client-0.5.0/stigg/generated/operations.py`

 * *Files 2% similar despite different names*

```diff
@@ -39,15 +39,14 @@
     _frag.min_unit_quantity()
     _frag.max_unit_quantity()
     _frag.billing_country_code()
     _frag_price = _frag.price()
     _frag_price.amount()
     _frag_price.currency()
     _frag_feature = _frag.feature()
-    _frag_feature.ref_id()
     _frag_feature.feature_units()
     _frag_feature.feature_units_plural()
     _frag_feature.display_name()
     _frag_feature.description()
     return _frag
 
 
@@ -185,15 +184,14 @@
     _frag_schedule_variables__as__DowngradeChangeVariables.addon_ref_ids()
     _frag_schedule_variables__as__DowngradeChangeVariables.billing_period()
     _frag_schedule_variables__as__DowngradeChangeVariables.downgrade_plan_ref_id()
     _frag_schedule_variables__as__BillingPeriodChangeVariables = _frag_schedule_variables.__as__(_schema.BillingPeriodChangeVariables)
     _frag_schedule_variables__as__BillingPeriodChangeVariables.billing_period()
     _frag_schedule_variables__as__UnitAmountChangeVariables = _frag_schedule_variables.__as__(_schema.UnitAmountChangeVariables)
     _frag_schedule_variables__as__UnitAmountChangeVariables.new_unit_amount()
-    _frag_schedule_variables__as__UnitAmountChangeVariables.feature_id()
     return _frag
 
 
 def fragment_subscription_fragment():
     _frag = sgqlc.operation.Fragment(_schema.CustomerSubscription, 'SubscriptionFragment')
     _frag.id()
     _frag.start_date()
@@ -289,64 +287,42 @@
     _frag_coupon.__fragment__(fragment_coupon_fragment())
     _frag_eligible_for_trial = _frag.eligible_for_trial()
     _frag_eligible_for_trial.product_id()
     _frag_eligible_for_trial.product_ref_id()
     _frag_eligible_for_trial.eligible()
     _frag_promotional_entitlements = _frag.promotional_entitlements()
     _frag_promotional_entitlements.__fragment__(fragment_promotional_entitlement_fragment())
-    return _frag
-
-
-def fragment_customer_with_subscriptions_fragment():
-    _frag = sgqlc.operation.Fragment(_schema.Customer, 'CustomerWithSubscriptionsFragment')
-    _frag.__fragment__(fragment_customer_fragment())
     _frag_subscriptions = _frag.subscriptions()
     _frag_subscriptions.__fragment__(fragment_subscription_fragment())
     return _frag
 
 
 def fragment_subscription_preview_fragment():
     _frag = sgqlc.operation.Fragment(_schema.SubscriptionPreview, 'SubscriptionPreviewFragment')
     _frag_sub_total = _frag.sub_total()
     _frag_sub_total.amount()
     _frag_sub_total.currency()
-    _frag_total_excluding_tax = _frag.total_excluding_tax()
-    _frag_total_excluding_tax.amount()
-    _frag_total_excluding_tax.currency()
     _frag_total = _frag.total()
     _frag_total.amount()
     _frag_total.currency()
-    _frag_tax_details = _frag.tax_details()
-    _frag_tax_details.display_name()
-    _frag_tax_details.percentage()
-    _frag_tax_details.inclusive()
-    _frag_tax = _frag.tax()
-    _frag_tax.amount()
-    _frag_tax.currency()
     _frag_billing_period_range = _frag.billing_period_range()
     _frag_billing_period_range.start()
     _frag_billing_period_range.end()
     _frag_discount = _frag.discount()
     _frag_discount.type()
     _frag_discount.value()
     _frag_discount.duration_type()
     _frag_discount.duration_in_months()
     _frag_subscription = _frag.subscription()
     _frag_subscription_sub_total = _frag_subscription.sub_total()
     _frag_subscription_sub_total.amount()
     _frag_subscription_sub_total.currency()
-    _frag_subscription_total_excluding_tax = _frag_subscription.total_excluding_tax()
-    _frag_subscription_total_excluding_tax.amount()
-    _frag_subscription_total_excluding_tax.currency()
     _frag_subscription_total = _frag_subscription.total()
     _frag_subscription_total.amount()
     _frag_subscription_total.currency()
-    _frag_subscription_tax = _frag_subscription.tax()
-    _frag_subscription_tax.amount()
-    _frag_subscription_tax.currency()
     _frag_proration = _frag.proration()
     _frag_proration.proration_date()
     _frag_proration_credit = _frag_proration.credit()
     _frag_proration_credit.amount()
     _frag_proration_credit.currency()
     _frag_proration_debit = _frag_proration.debit()
     _frag_proration_debit.amount()
@@ -592,37 +568,18 @@
     _frag_palette.paywall_background_color()
     _frag_typography = _frag.typography()
     _frag_typography.__fragment__(fragment_typography_configuration_fragment())
     _frag.custom_css()
     return _frag
 
 
-def fragment_customer_portal_subscription_price_fragment():
-    _frag = sgqlc.operation.Fragment(_schema.CustomerPortalSubscriptionPrice, 'CustomerPortalSubscriptionPriceFragment')
-    _frag.billing_period()
-    _frag.billing_model()
-    _frag_price = _frag.price()
-    _frag_price.amount()
-    _frag_price.currency()
-    _frag_feature = _frag.feature()
-    _frag_feature.id()
-    _frag_feature.ref_id()
-    _frag_feature.display_name()
-    _frag_feature.feature_units()
-    _frag_feature.feature_units_plural()
-    return _frag
-
-
 def fragment_customer_portal_subscription_fragment():
     _frag = sgqlc.operation.Fragment(_schema.CustomerPortalSubscription, 'CustomerPortalSubscriptionFragment')
     _frag.subscription_id()
     _frag.plan_name()
-    _frag.pricing_type()
-    _frag_prices = _frag.prices()
-    _frag_prices.__fragment__(fragment_customer_portal_subscription_price_fragment())
     _frag_pricing = _frag.pricing()
     _frag_pricing.unit_quantity()
     _frag_pricing.billing_period()
     _frag_pricing.billing_model()
     _frag_pricing.pricing_type()
     _frag_pricing.usage_based_estimated_bill()
     _frag_pricing_price = _frag_pricing.price()
@@ -636,21 +593,18 @@
     _frag.trial_remaining_days()
     _frag_billing_period_range = _frag.billing_period_range()
     _frag_billing_period_range.start()
     _frag_billing_period_range.end()
     _frag_total_price = _frag.total_price()
     _frag_total_price_sub_total = _frag_total_price.sub_total()
     _frag_total_price_sub_total.amount()
-    _frag_total_price_sub_total.currency()
     _frag_total_price_total = _frag_total_price.total()
     _frag_total_price_total.amount()
-    _frag_total_price_total.currency()
     _frag_total_price_addons_total = _frag_total_price.addons_total()
     _frag_total_price_addons_total.amount()
-    _frag_total_price_addons_total.currency()
     _frag_addons = _frag.addons()
     _frag_addons.__fragment__(fragment_customer_portal_subscription_addon())
     _frag_scheduled_updates = _frag.scheduled_updates()
     _frag_scheduled_updates.__fragment__(fragment_customer_portal_subscription_scheduled_update_data())
     return _frag
 
 
@@ -668,25 +622,23 @@
     _frag.subscription_schedule_type()
     _frag.schedule_status()
     _frag.scheduled_execution_time()
     _frag_target_package = _frag.target_package()
     _frag_target_package.id()
     _frag_target_package.ref_id()
     _frag_target_package.display_name()
-    _frag_target_package.pricing_type()
     _frag_schedule_variables = _frag.schedule_variables()
     _frag_schedule_variables__as__DowngradeChangeVariables = _frag_schedule_variables.__as__(_schema.DowngradeChangeVariables)
     _frag_schedule_variables__as__DowngradeChangeVariables.addon_ref_ids()
     _frag_schedule_variables__as__DowngradeChangeVariables.billing_period()
     _frag_schedule_variables__as__DowngradeChangeVariables.downgrade_plan_ref_id()
     _frag_schedule_variables__as__BillingPeriodChangeVariables = _frag_schedule_variables.__as__(_schema.BillingPeriodChangeVariables)
     _frag_schedule_variables__as__BillingPeriodChangeVariables.billing_period()
     _frag_schedule_variables__as__UnitAmountChangeVariables = _frag_schedule_variables.__as__(_schema.UnitAmountChangeVariables)
     _frag_schedule_variables__as__UnitAmountChangeVariables.new_unit_amount()
-    _frag_schedule_variables__as__UnitAmountChangeVariables.feature_id()
     return _frag
 
 
 def fragment_customer_portal_entitlement():
     _frag = sgqlc.operation.Fragment(_schema.Entitlement, 'CustomerPortalEntitlement')
     _frag.is_granted()
     _frag.usage_limit()
@@ -781,38 +733,20 @@
     _frag.min_unit_quantity()
     _frag.max_unit_quantity()
     _frag.billing_country_code()
     _frag_price = _frag.price()
     _frag_price.amount()
     _frag_price.currency()
     _frag_feature = _frag.feature()
-    _frag_feature.ref_id()
     _frag_feature.feature_units()
     _frag_feature.feature_units_plural()
     _frag_feature.display_name()
     return _frag
 
 
-def fragment_paywall_calculated_price_points_fragment():
-    _frag = sgqlc.operation.Fragment(_schema.PaywallPricePoint, 'PaywallCalculatedPricePointsFragment')
-    _frag.plan_id()
-    _frag.additional_charges_may_apply()
-    _frag.billing_period()
-    _frag.amount()
-    _frag.currency()
-    _frag.billing_country_code()
-    _frag_feature = _frag.feature()
-    _frag_feature.ref_id()
-    _frag_feature.feature_units()
-    _frag_feature.feature_units_plural()
-    _frag_feature.display_name()
-    _frag_feature.description()
-    return _frag
-
-
 def fragment_mock_paywall_addon_fragment():
     _frag = sgqlc.operation.Fragment(_schema.PaywallAddon, 'MockPaywallAddonFragment')
     _frag.ref_id()
     _frag.display_name()
     _frag.description()
     _frag.additional_meta_data()
     _frag.billing_id()
@@ -830,62 +764,44 @@
     _frag_plans.__fragment__(fragment_plan_fragment())
     _frag_currency = _frag.currency()
     _frag_currency.__fragment__(fragment_paywall_currency())
     _frag_configuration = _frag.configuration()
     _frag_configuration.__fragment__(fragment_paywall_configuration_fragment())
     _frag_customer = _frag.customer()
     _frag_customer.__fragment__(fragment_customer_fragment())
-    _frag_active_subscriptions = _frag.active_subscriptions()
-    _frag_active_subscriptions.__fragment__(fragment_subscription_fragment())
     _frag_resource = _frag.resource()
     _frag_resource.__fragment__(fragment_customer_resource_fragment())
-    _frag_paywall_calculated_price_points = _frag.paywall_calculated_price_points()
-    _frag_paywall_calculated_price_points.__fragment__(fragment_paywall_calculated_price_points_fragment())
-    return _frag
-
-
-def fragment_usage_history_fragment():
-    _frag = sgqlc.operation.Fragment(_schema.UsageHistory, 'UsageHistoryFragment')
-    _frag.start_date()
-    _frag.end_date()
-    _frag_usage_measurements = _frag.usage_measurements()
-    _frag_usage_measurements.date()
-    _frag_usage_measurements.value()
-    _frag_usage_measurements.is_reset_point()
     return _frag
 
 
 class Fragment:
     addon_fragment = fragment_addon_fragment()
     coupon_fragment = fragment_coupon_fragment()
     customer_fragment = fragment_customer_fragment()
     customer_portal_billing_information = fragment_customer_portal_billing_information()
     customer_portal_configuration_fragment = fragment_customer_portal_configuration_fragment()
     customer_portal_entitlement = fragment_customer_portal_entitlement()
     customer_portal_fragment = fragment_customer_portal_fragment()
     customer_portal_promotional_entitlement = fragment_customer_portal_promotional_entitlement()
     customer_portal_subscription_addon = fragment_customer_portal_subscription_addon()
     customer_portal_subscription_fragment = fragment_customer_portal_subscription_fragment()
-    customer_portal_subscription_price_fragment = fragment_customer_portal_subscription_price_fragment()
     customer_portal_subscription_scheduled_update_data = fragment_customer_portal_subscription_scheduled_update_data()
     customer_resource_fragment = fragment_customer_resource_fragment()
-    customer_with_subscriptions_fragment = fragment_customer_with_subscriptions_fragment()
     entitlement_fragment = fragment_entitlement_fragment()
     entitlement_usage_updated = fragment_entitlement_usage_updated()
     entitlements_updated_payload = fragment_entitlements_updated_payload()
     feature_fragment = fragment_feature_fragment()
     font_variant_fragment = fragment_font_variant_fragment()
     layout_configuration_fragment = fragment_layout_configuration_fragment()
     mock_paywall_addon_fragment = fragment_mock_paywall_addon_fragment()
     mock_paywall_package_entitlement_fragment = fragment_mock_paywall_package_entitlement_fragment()
     mock_paywall_plan_fragment = fragment_mock_paywall_plan_fragment()
     mock_paywall_price_fragment = fragment_mock_paywall_price_fragment()
     package_entitlement_fragment = fragment_package_entitlement_fragment()
     paywall_addon_fragment = fragment_paywall_addon_fragment()
-    paywall_calculated_price_points_fragment = fragment_paywall_calculated_price_points_fragment()
     paywall_configuration_fragment = fragment_paywall_configuration_fragment()
     paywall_currency = fragment_paywall_currency()
     paywall_fragment = fragment_paywall_fragment()
     paywall_package_entitlement_fragment = fragment_paywall_package_entitlement_fragment()
     paywall_plan_fragment = fragment_paywall_plan_fragment()
     plan_fragment = fragment_plan_fragment()
     price_fragment = fragment_price_fragment()
@@ -895,15 +811,14 @@
     slim_customer_fragment = fragment_slim_customer_fragment()
     slim_subscription_fragment = fragment_slim_subscription_fragment()
     subscription_fragment = fragment_subscription_fragment()
     subscription_preview_fragment = fragment_subscription_preview_fragment()
     subscription_scheduled_update_data = fragment_subscription_scheduled_update_data()
     total_price_fragment = fragment_total_price_fragment()
     typography_configuration_fragment = fragment_typography_configuration_fragment()
-    usage_history_fragment = fragment_usage_history_fragment()
     usage_updated_fragment = fragment_usage_updated_fragment()
 
 
 def mutation_provision_customer():
     _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='ProvisionCustomer', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.ProvisionCustomerInput))))
     _op_provision_customer = _op.provision_customer(input=sgqlc.types.Variable('input'))
     _op_provision_customer_customer = _op_provision_customer.customer()
@@ -926,15 +841,15 @@
     _op_import_customer.__fragment__(fragment_slim_customer_fragment())
     return _op
 
 
 def mutation_update_customer():
     _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='UpdateCustomer', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.UpdateCustomerInput))))
     _op_update_customer = _op.update_one_customer(input=sgqlc.types.Variable('input'), __alias__='update_customer')
-    _op_update_customer.__fragment__(fragment_slim_customer_fragment())
+    _op_update_customer.__fragment__(fragment_customer_fragment())
     return _op
 
 
 def mutation_provision_subscription():
     _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='ProvisionSubscription', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.ProvisionSubscriptionInput))))
     _op_provision_subscription = _op.provision_subscription_v2(input=sgqlc.types.Variable('input'), __alias__='provision_subscription')
     _op_provision_subscription.checkout_url()
@@ -960,14 +875,22 @@
 def mutation_cancel_subscription():
     _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='CancelSubscription', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.SubscriptionCancellationInput))))
     _op_cancel_subscription = _op.cancel_subscription(input=sgqlc.types.Variable('input'))
     _op_cancel_subscription.__fragment__(fragment_slim_subscription_fragment())
     return _op
 
 
+def mutation_initiate_checkout():
+    _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='InitiateCheckout', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.InitiateCheckoutInput))))
+    _op_initiate_checkout = _op.initiate_checkout(input=sgqlc.types.Variable('input'))
+    _op_initiate_checkout.checkout_url()
+    _op_initiate_checkout.checkout_billing_id()
+    return _op
+
+
 def mutation_estimate_subscription():
     _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='EstimateSubscription', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.EstimateSubscriptionInput))))
     _op_estimate_subscription = _op.estimate_subscription(input=sgqlc.types.Variable('input'))
     _op_estimate_subscription.__fragment__(fragment_subscription_preview_fragment())
     return _op
 
 
@@ -990,71 +913,49 @@
     _op_create_usage_measurement.id()
     _op_create_usage_measurement.current_usage()
     _op_create_usage_measurement.next_reset_date()
     _op_create_usage_measurement.timestamp()
     return _op
 
 
-def mutation_report_event():
-    _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='ReportEvent', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.UsageEventsReportInput))))
-    _op.report_event(events=sgqlc.types.Variable('input'))
-    return _op
-
-
 def mutation_report_entitlement_check_requested():
     _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='ReportEntitlementCheckRequested', variables=dict(entitlementCheckRequested=sgqlc.types.Arg(sgqlc.types.non_null(_schema.EntitlementCheckRequested))))
     _op.report_entitlement_check_requested(entitlement_check_requested=sgqlc.types.Variable('entitlementCheckRequested'))
     return _op
 
 
 def mutation_create_subscription():
     _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='CreateSubscription', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.SubscriptionInput))))
     _op_create_subscription = _op.create_subscription(subscription=sgqlc.types.Variable('input'))
     _op_create_subscription.__fragment__(fragment_slim_subscription_fragment())
     return _op
 
 
-def mutation_migrate_subscription_to_latest():
-    _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='MigrateSubscriptionToLatest', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.SubscriptionMigrationInput))))
-    _op_migrate_subscription_to_latest = _op.migrate_subscription_to_latest(input=sgqlc.types.Variable('input'))
-    _op_migrate_subscription_to_latest.subscription_id()
-    return _op
-
-
-def mutation_archive_customer():
-    _op = sgqlc.operation.Operation(_schema_root.mutation_type, name='ArchiveCustomer', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.ArchiveCustomerInput))))
-    _op_archive_customer = _op.archive_customer(input=sgqlc.types.Variable('input'))
-    _op_archive_customer.customer_id()
-    return _op
-
-
 class Mutation:
-    archive_customer = mutation_archive_customer()
     cancel_subscription = mutation_cancel_subscription()
     cancel_subscription_updates = mutation_cancel_subscription_updates()
     create_subscription = mutation_create_subscription()
     estimate_subscription = mutation_estimate_subscription()
     estimate_subscription_update = mutation_estimate_subscription_update()
     import_customer = mutation_import_customer()
     import_customer_bulk = mutation_import_customer_bulk()
     import_subscriptions_bulk = mutation_import_subscriptions_bulk()
-    migrate_subscription_to_latest = mutation_migrate_subscription_to_latest()
+    initiate_checkout = mutation_initiate_checkout()
     provision_customer = mutation_provision_customer()
     provision_subscription = mutation_provision_subscription()
     report_entitlement_check_requested = mutation_report_entitlement_check_requested()
-    report_event = mutation_report_event()
     report_usage = mutation_report_usage()
     update_customer = mutation_update_customer()
     update_subscription = mutation_update_subscription()
 
 
 def query_get_customer_by_id():
     _op = sgqlc.operation.Operation(_schema_root.query_type, name='GetCustomerById', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.GetCustomerByRefIdInput))))
     _op_get_customer_by_ref_id = _op.get_customer_by_ref_id(input=sgqlc.types.Variable('input'))
-    _op_get_customer_by_ref_id.__fragment__(fragment_customer_with_subscriptions_fragment())
+    _op_get_customer_by_ref_id.__fragment__(fragment_customer_fragment())
     return _op
 
 
 def query_get_active_subscriptions():
     _op = sgqlc.operation.Operation(_schema_root.query_type, name='GetActiveSubscriptions', variables=dict(input=sgqlc.types.Arg(sgqlc.types.non_null(_schema.GetActiveSubscriptionsInput))))
     _op_get_active_subscriptions = _op.get_active_subscriptions(input=sgqlc.types.Variable('input'))
     _op_get_active_subscriptions.__fragment__(fragment_subscription_fragment())
@@ -1121,33 +1022,25 @@
     _op_mock_paywall_plans = _op_mock_paywall.plans()
     _op_mock_paywall_plans.__fragment__(fragment_mock_paywall_plan_fragment())
     _op_mock_paywall_configuration = _op_mock_paywall.configuration()
     _op_mock_paywall_configuration.__fragment__(fragment_paywall_configuration_fragment())
     return _op
 
 
-def query_usage_history():
-    _op = sgqlc.operation.Operation(_schema_root.query_type, name='UsageHistory', variables=dict(usageHistoryInput=sgqlc.types.Arg(sgqlc.types.non_null(_schema.UsageHistoryInput))))
-    _op_usage_history = _op.usage_history(usage_history_input=sgqlc.types.Variable('usageHistoryInput'))
-    _op_usage_history.__fragment__(fragment_usage_history_fragment())
-    return _op
-
-
 class Query:
     get_active_subscriptions = query_get_active_subscriptions()
     get_coupons = query_get_coupons()
     get_customer_by_id = query_get_customer_by_id()
     get_customer_portal_by_ref_id = query_get_customer_portal_by_ref_id()
     get_entitlement = query_get_entitlement()
     get_entitlements = query_get_entitlements()
     get_mock_paywall = query_get_mock_paywall()
     get_paywall = query_get_paywall()
     get_products = query_get_products()
     get_sdk_configuration = query_get_sdk_configuration()
-    usage_history = query_usage_history()
 
 
 def subscription_entitlements_updated():
     _op = sgqlc.operation.Operation(_schema_root.subscription_type, name='EntitlementsUpdated')
     _op_entitlements_updated = _op.entitlements_updated()
     _op_entitlements_updated.__fragment__(fragment_entitlements_updated_payload())
     return _op
```

### Comparing `stigg_api_client-0.499.0/stigg/generated/schema.py` & `stigg_api_client-0.5.0/stigg/generated/schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,32 +13,27 @@
 
 
 ########################################################################
 # Scalars and Enumerations
 ########################################################################
 class AccessDeniedReason(sgqlc.types.Enum):
     __schema__ = schema
-    __choices__ = ('CustomerIsArchived', 'CustomerNotFound', 'CustomerResourceNotFound', 'FeatureNotFound', 'NoActiveSubscription', 'NoFeatureEntitlementInSubscription', 'RequestedUsageExceedingLimit', 'Unknown')
+    __choices__ = ('CustomerNotFound', 'CustomerResourceNotFound', 'FeatureNotFound', 'NoActiveSubscription', 'NoFeatureEntitlementInSubscription', 'RequestedUsageExceedingLimit', 'Unknown')
 
 
 class AccountStatus(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('ACTIVE', 'BLOCKED')
 
 
 class AddonSortFields(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('billingId', 'createdAt', 'description', 'displayName', 'environmentId', 'id', 'isLatest', 'pricingType', 'productId', 'refId', 'status', 'updatedAt', 'versionNumber')
 
 
-class AggregationFunction(sgqlc.types.Enum):
-    __schema__ = schema
-    __choices__ = ('AVG', 'COUNT', 'MAX', 'MIN', 'SUM', 'UNIQUE')
-
-
 class Alignment(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('CENTER', 'LEFT', 'RIGHT')
 
 
 class ApiKeySortFields(sgqlc.types.Enum):
     __schema__ = schema
@@ -68,19 +63,14 @@
 Boolean = sgqlc.types.Boolean
 
 class ChangeType(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('ADDED', 'DELETED', 'MODIFIED', 'REORDERED')
 
 
-class ConditionOperation(sgqlc.types.Enum):
-    __schema__ = schema
-    __choices__ = ('EQUALS', 'GREATER_THAN', 'GREATER_THAN_OR_EQUAL', 'IS_NOT_NULL', 'IS_NULL', 'LESS_THAN', 'LESS_THAN_OR_EQUAL', 'NOT_EQUALS')
-
-
 class ConnectionCursor(sgqlc.types.Scalar):
     __schema__ = schema
 
 
 class CouponSortFields(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('billingId', 'createdAt', 'description', 'environmentId', 'id', 'name', 'refId', 'status', 'type', 'updatedAt')
@@ -104,20 +94,20 @@
 class CustomerResourceSortFields(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('createdAt', 'environmentId', 'resourceId')
 
 
 class CustomerSortFields(sgqlc.types.Enum):
     __schema__ = schema
-    __choices__ = ('billingId', 'createdAt', 'crmHubspotCompanyId', 'crmHubspotCompanyUrl', 'crmId', 'customerId', 'deletedAt', 'email', 'environmentId', 'id', 'name', 'refId', 'updatedAt')
+    __choices__ = ('billingId', 'createdAt', 'crmHubspotCompanyId', 'crmHubspotCompanyUrl', 'crmId', 'customerId', 'email', 'environmentId', 'id', 'name', 'refId', 'updatedAt')
 
 
 class CustomerSubscriptionSortFields(sgqlc.types.Enum):
     __schema__ = schema
-    __choices__ = ('billingId', 'cancelReason', 'cancellationDate', 'createdAt', 'crmId', 'crmLinkUrl', 'effectiveEndDate', 'endDate', 'environmentId', 'id', 'oldBillingId', 'pricingType', 'refId', 'resourceId', 'startDate', 'status', 'subscriptionId', 'trialEndDate')
+    __choices__ = ('billingId', 'cancelReason', 'cancellationDate', 'createdAt', 'crmId', 'crmLinkUrl', 'effectiveEndDate', 'endDate', 'environmentId', 'id', 'oldBillingId', 'pricingType', 'refId', 'startDate', 'status', 'subscriptionId', 'trialEndDate')
 
 
 DateTime = sgqlc.types.datetime.DateTime
 
 class Department(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('CEO_OR_FOUNDER', 'ENGINEERING', 'GROWTH', 'MARKETING', 'MONETIZATION', 'OTHER', 'PRODUCT')
@@ -151,20 +141,20 @@
 class EnvironmentSortFields(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('createdAt', 'displayName', 'id', 'slug')
 
 
 class ErrorCode(sgqlc.types.Enum):
     __schema__ = schema
-    __choices__ = ('AccountNotFoundError', 'AddonHasToHavePriceError', 'AddonNotFound', 'AddonWithDraftCannotBeDeletedError', 'ArchivedCouponCantBeApplied', 'AuthCustomerMismatch', 'BadUserInput', 'BillingPeriodMissingError', 'CannotDeleteCustomerError', 'CannotDeleteFeatureError', 'CannotDeleteProductError', 'CannotEditPackageInNonDraftMode', 'CannotReportUsageForEntitlementWithMeterError', 'CheckoutIsNotSupported', 'CheckoutOptionsMissing', 'CouponNotFound', 'CustomerAlreadyHaveCustomerCoupon', 'CustomerAlreadyUsesCoupon', 'CustomerHasNoPaymentMethod', 'CustomerNoBillingId', 'CustomerNotFound', 'CustomerResourceNotFound', 'DowngradeBillingPeriodNotSupportedError', 'DraftPlanCantBeArchived', 'DuplicatedEntityNotAllowed', 'EditAllowedOnDraftPackageOnlyError', 'EntitlementsMustBelongToSamePackage', 'EntityIdDifferentFromRefIdError', 'EntityIsArchivedError', 'EnvironmentMissing', 'ExperimentAlreadyRunning', 'ExperimentNotFoundError', 'ExperimentStatusError', 'FailedToCreateCheckoutSessionError', 'FailedToImportCustomer', 'FeatureNotFound', 'FetchAllCountriesPricesNotAllowed', 'IdentityForbidden', 'ImportAlreadyInProgress', 'ImportSubscriptionsBulkError', 'InitStripePaymentMethodError', 'IntegrationNotFound', 'IntegrityViolation', 'InvalidAddressError', 'InvalidArgumentError', 'InvalidCancellationDate', 'InvalidEntitlementResetPeriod', 'InvalidMemberDelete', 'InvalidMetadataError', 'InvalidQuantity', 'InvalidSubscriptionStatus', 'InvalidUpdatePriceUnitAmountError', 'MemberInvitationError', 'MemberNotFound', 'MeterMustBeAssociatedToMeteredFeature', 'MeteringNotAvailableForFeatureType', 'MissingEntityIdError', 'NoFeatureEntitlementInSubscription', 'NoProductsAvailable', 'OperationNotAllowedDuringInProgressExperiment', 'PackageAlreadyPublished', 'PackagePricingTypeNotSet', 'PaymentMethodNotFoundError', 'PlanAlreadyExtended', 'PlanCannotBePublishWhenBasePlanIsDraft', 'PlanIsUsedAsDefaultStartPlan', 'PlanIsUsedAsDowngradePlan', 'PlanNotFound', 'PlanWithChildCantBeDeleted', 'PlansCircularDependencyError', 'PriceNotFound', 'PromotionCodeCustomerNotFirstPurchase', 'PromotionCodeMaxRedemptionsReached', 'PromotionCodeMinimumAmountNotReached', 'PromotionCodeNotActive', 'PromotionCodeNotForCustomer', 'PromotionCodeNotFound', 'RateLimitExceeded', 'RecalculateEntitlementsError', 'ResyncAlreadyInProgress', 'ScheduledMigrationAlreadyExistsError', 'SelectedBillingModelDoesntMatchImportedItemError', 'StripeCustomerIsDeleted', 'StripeError', 'SubscriptionAlreadyCanceledOrExpired', 'SubscriptionAlreadyOnLatestPlanError', 'SubscriptionMustHaveSinglePlanError', 'SubscriptionNotFound', 'TooManySubscriptionsPerCustomer', 'TrialMinDateError', 'TrialMustBeCancelledImmediately', 'UnPublishedPackage', 'Unauthenticated', 'UncompatibleSubscriptionAddon', 'UnexpectedError', 'UnsupportedFeatureType', 'UnsupportedSubscriptionScheduleType', 'UnsupportedVendorIdentifier')
+    __choices__ = ('AccountNotFoundError', 'AddonHasToHavePriceError', 'AddonNotFound', 'ArchivedCouponCantBeApplied', 'AuthCustomerMismatch', 'BadUserInput', 'BillingPeriodMissingError', 'CannotDeleteCustomerError', 'CannotDeleteFeatureError', 'CannotDeleteProductError', 'CannotEditPackageInNonDraftMode', 'CheckoutIsNotSupported', 'CheckoutOptionsMissing', 'CouponNotFound', 'CustomerAlreadyHaveCustomerCoupon', 'CustomerAlreadyUsesCoupon', 'CustomerHasNoPaymentMethod', 'CustomerNoBillingId', 'CustomerNotFound', 'CustomerResourceNotFound', 'DowngradeBillingPeriodNotSupportedError', 'DraftPlanCantBeArchived', 'DuplicatedEntityNotAllowed', 'EditAllowedOnDraftPackageOnlyError', 'EntitlementsMustBelongToSamePackage', 'EntityIdDifferentFromRefIdError', 'EnvironmentMissing', 'ExperimentAlreadyRunning', 'ExperimentNotFoundError', 'ExperimentStatusError', 'FailedToCreateCheckoutSessionError', 'FailedToImportCustomer', 'FeatureNotFound', 'FetchAllCountriesPricesNotAllowed', 'IdentityForbidden', 'ImportAlreadyInProgress', 'InitStripePaymentMethodError', 'IntegrationNotFound', 'IntegrityViolation', 'InvalidAddressError', 'InvalidArgumentError', 'InvalidCancellationDate', 'InvalidEntitlementResetPeriod', 'InvalidMemberDelete', 'InvalidQuantity', 'InvalidSubscriptionStatus', 'InvalidUpdatePriceUnitAmountError', 'InvalidUsageValueForIncrementalFeatureError', 'MemberInvitationError', 'MemberNotFound', 'MeteringNotAvailableForFeatureType', 'MissingEntityIdError', 'NoFeatureEntitlementInSubscription', 'NoProductsAvailable', 'OperationNotAllowedDuringInProgressExperiment', 'PackageAlreadyPublished', 'PackagePricingTypeNotSet', 'PlanAlreadyExtended', 'PlanCannotBePublishWhenBasePlanIsDraft', 'PlanIsUsedAsDefaultStartPlan', 'PlanIsUsedAsDowngradePlan', 'PlanNotFound', 'PlanWithChildCantBeDeleted', 'PlansCircularDependencyError', 'PriceNotFound', 'PromotionCodeCustomerNotFirstPurchase', 'PromotionCodeMaxRedemptionsReached', 'PromotionCodeMinimumAmountNotReached', 'PromotionCodeNotActive', 'PromotionCodeNotForCustomer', 'PromotionCodeNotFound', 'RateLimitExceeded', 'ResyncAlreadyInProgress', 'SelectedBillingModelDoesntMatchImportedItemError', 'StripeCustomerIsDeleted', 'SubscriptionAlreadyCanceledOrExpired', 'SubscriptionMustHaveSinglePlanError', 'SubscriptionNotFound', 'TrialMinDateError', 'TrialMustBeCancelledImmediately', 'UnPublishedPackage', 'Unauthenticated', 'UncompatibleSubscriptionAddon', 'UnexpectedError', 'UnsupportedFeatureType', 'UnsupportedSubscriptionScheduleType', 'UnsupportedVendorIdentifier')
 
 
 class EventLogType(sgqlc.types.Enum):
     __schema__ = schema
-    __choices__ = ('ADDON_CREATED', 'ADDON_DELETED', 'ADDON_UPDATED', 'COUPON_ARCHIVED', 'COUPON_CREATED', 'COUPON_UPDATED', 'CREATE_SUBSCRIPTION_FAILED', 'CUSTOMER_CREATED', 'CUSTOMER_DELETED', 'CUSTOMER_ENTITLEMENT_CALCULATION_TRIGGERED', 'CUSTOMER_PAYMENT_FAILED', 'CUSTOMER_RESOURCE_ENTITLEMENT_CALCULATION_TRIGGERED', 'CUSTOMER_UPDATED', 'EDGE_API_DATA_RESYNC', 'ENTITLEMENTS_UPDATED', 'ENTITLEMENT_DENIED', 'ENTITLEMENT_GRANTED', 'ENTITLEMENT_REQUESTED', 'ENVIRONMENT_DELETED', 'FEATURE_CREATED', 'FEATURE_DELETED', 'FEATURE_UPDATED', 'IMPORT_INTEGRATION_CATALOG_TRIGGERED', 'IMPORT_INTEGRATION_CUSTOMERS_TRIGGERED', 'IMPORT_SUBSCRIPTIONS_BULK_TRIGGERED', 'MEASUREMENT_REPORTED', 'PACKAGE_PUBLISHED', 'PLAN_CREATED', 'PLAN_DELETED', 'PLAN_UPDATED', 'PRODUCT_CREATED', 'PRODUCT_DELETED', 'PRODUCT_UPDATED', 'PROMOTIONAL_ENTITLEMENT_EXPIRED', 'PROMOTIONAL_ENTITLEMENT_GRANTED', 'PROMOTIONAL_ENTITLEMENT_REVOKED', 'PROMOTIONAL_ENTITLEMENT_UPDATED', 'RECALCULATE_ENTITLEMENTS_TRIGGERED', 'RESYNC_INTEGRATION_TRIGGERED', 'SUBSCRIPTION_CANCELED', 'SUBSCRIPTION_CREATED', 'SUBSCRIPTION_EXPIRED', 'SUBSCRIPTION_TRIAL_CONVERTED', 'SUBSCRIPTION_TRIAL_ENDS_SOON', 'SUBSCRIPTION_TRIAL_EXPIRED', 'SUBSCRIPTION_TRIAL_STARTED', 'SUBSCRIPTION_UPDATED', 'SUBSCRIPTION_USAGE_UPDATED', 'SYNC_FAILED', 'WIDGET_CONFIGURATION_UPDATED')
+    __choices__ = ('ADDON_CREATED', 'ADDON_DELETED', 'ADDON_UPDATED', 'COUPON_ARCHIVED', 'COUPON_CREATED', 'COUPON_UPDATED', 'CREATE_SUBSCRIPTION_FAILED', 'CUSTOMER_CREATED', 'CUSTOMER_DELETED', 'CUSTOMER_ENTITLEMENT_CALCULATION_TRIGGERED', 'CUSTOMER_PAYMENT_FAILED', 'CUSTOMER_RESOURCE_ENTITLEMENT_CALCULATION_TRIGGERED', 'CUSTOMER_UPDATED', 'EDGE_API_DATA_RESYNC', 'ENTITLEMENTS_UPDATED', 'ENTITLEMENT_DENIED', 'ENTITLEMENT_GRANTED', 'ENTITLEMENT_REQUESTED', 'ENVIRONMENT_DELETED', 'FEATURE_CREATED', 'FEATURE_DELETED', 'FEATURE_UPDATED', 'IMPORT_INTEGRATION_CATALOG_TRIGGERED', 'IMPORT_INTEGRATION_CUSTOMERS_TRIGGERED', 'MEASUREMENT_REPORTED', 'PACKAGE_PUBLISHED', 'PLAN_CREATED', 'PLAN_DELETED', 'PLAN_UPDATED', 'PRODUCT_CREATED', 'PRODUCT_DELETED', 'PRODUCT_UPDATED', 'PROMOTIONAL_ENTITLEMENT_EXPIRED', 'PROMOTIONAL_ENTITLEMENT_GRANTED', 'PROMOTIONAL_ENTITLEMENT_REVOKED', 'PROMOTIONAL_ENTITLEMENT_UPDATED', 'RESYNC_INTEGRATION_TRIGGERED', 'SUBSCRIPTION_CANCELED', 'SUBSCRIPTION_CREATED', 'SUBSCRIPTION_EXPIRED', 'SUBSCRIPTION_TRIAL_CONVERTED', 'SUBSCRIPTION_TRIAL_ENDS_SOON', 'SUBSCRIPTION_TRIAL_EXPIRED', 'SUBSCRIPTION_TRIAL_STARTED', 'SUBSCRIPTION_UPDATED', 'SUBSCRIPTION_USAGE_UPDATED', 'SYNC_FAILED', 'WIDGET_CONFIGURATION_UPDATED')
 
 
 class ExperimentSortFields(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('createdAt', 'environmentId', 'id', 'name', 'productId', 'refId', 'status')
 
 
@@ -321,15 +311,15 @@
 class SortNulls(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('NULLS_FIRST', 'NULLS_LAST')
 
 
 class SourceType(sgqlc.types.Enum):
     __schema__ = schema
-    __choices__ = ('JS_CLIENT_SDK', 'NODE_SERVER_SDK', 'PERSISTENT_CACHE_SERVICE')
+    __choices__ = ('JS_CLIENT_SDK', 'NODE_SERVER_SDK')
 
 
 String = sgqlc.types.String
 
 class SubscriptionAddonSortFields(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('createdAt', 'id', 'quantity', 'updatedAt')
@@ -361,32 +351,27 @@
 
 
 class SubscriptionMigrationTaskSortFields(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('createdAt', 'environmentId', 'id', 'status', 'taskType')
 
 
-class SubscriptionMigrationTime(sgqlc.types.Enum):
-    __schema__ = schema
-    __choices__ = ('END_OF_BILLING_PERIOD', 'IMMEDIATE')
-
-
 class SubscriptionPriceSortFields(sgqlc.types.Enum):
     __schema__ = schema
-    __choices__ = ('billingModel', 'createdAt', 'featureId', 'id', 'updatedAt', 'usageLimit')
+    __choices__ = ('createdAt', 'id', 'updatedAt', 'usageLimit')
 
 
 class SubscriptionScheduleStatus(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('Canceled', 'Done', 'Failed', 'Scheduled')
 
 
 class SubscriptionScheduleType(sgqlc.types.Enum):
     __schema__ = schema
-    __choices__ = ('BillingPeriod', 'Downgrade', 'MigrateToLatest', 'UnitAmount')
+    __choices__ = ('BillingPeriod', 'Downgrade', 'UnitAmount')
 
 
 class SubscriptionStartSetup(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('FREE_PLAN', 'PLAN_SELECTION', 'TRIAL_PERIOD')
 
 
@@ -403,15 +388,15 @@
 class TaskStatus(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('COMPLETED', 'FAILED', 'IN_PROGRESS', 'PARTIALLY_FAILED', 'PENDING')
 
 
 class TaskType(sgqlc.types.Enum):
     __schema__ = schema
-    __choices__ = ('IMPORT_INTEGRATION_CATALOG', 'IMPORT_INTEGRATION_CUSTOMERS', 'IMPORT_SUBSCRIPTIONS_BULK', 'RECALCULATE_ENTITLEMENTS', 'RESYNC_INTEGRATION', 'SUBSCRIPTION_MIGRATION')
+    __choices__ = ('IMPORT_INTEGRATION_CATALOG', 'IMPORT_INTEGRATION_CUSTOMERS', 'RESYNC_INTEGRATION', 'SUBSCRIPTION_MIGRATION')
 
 
 class TrialPeriodUnits(sgqlc.types.Enum):
     __schema__ = schema
     __choices__ = ('DAY', 'MONTH')
 
 
@@ -518,23 +503,14 @@
     city = sgqlc.types.Field(String, graphql_name='city')
     country = sgqlc.types.Field(String, graphql_name='country')
     phone_number = sgqlc.types.Field(String, graphql_name='phoneNumber')
     postal_code = sgqlc.types.Field(String, graphql_name='postalCode')
     state = sgqlc.types.Field(String, graphql_name='state')
 
 
-class AggregatedEventsByCustomerInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('aggregation', 'customer_id', 'environment_id', 'filters')
-    aggregation = sgqlc.types.Field(sgqlc.types.non_null('MeterAggregation'), graphql_name='aggregation')
-    customer_id = sgqlc.types.Field(String, graphql_name='customerId')
-    environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
-    filters = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('MeterFilterDefinitionInput'))), graphql_name='filters')
-
-
 class ApiKeyFilter(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('and_', 'id', 'or_')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('ApiKeyFilter')), graphql_name='and')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('ApiKeyFilter')), graphql_name='or')
 
@@ -550,21 +526,14 @@
 class ArchiveCouponInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('environment_id', 'ref_id')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
 
 
-class ArchiveCustomerInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('customer_id', 'environment_id')
-    customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
-    environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
-
-
 class ArchivePlanInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('environment_id', 'id')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
 
 
@@ -574,21 +543,14 @@
     customer_id = sgqlc.types.Field(String, graphql_name='customerId')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     payment_method_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='paymentMethodId')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     vendor_identifier = sgqlc.types.Field(sgqlc.types.non_null(VendorIdentifier), graphql_name='vendorIdentifier')
 
 
-class BillableFeatureInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('feature_id', 'quantity')
-    feature_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='featureId')
-    quantity = sgqlc.types.Field(sgqlc.types.non_null(Float), graphql_name='quantity')
-
-
 class BillingModelFilterComparison(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('eq', 'gt', 'gte', 'i_like', 'in_', 'is_', 'is_not', 'like', 'lt', 'lte', 'neq', 'not_ilike', 'not_in', 'not_like')
     eq = sgqlc.types.Field(BillingModel, graphql_name='eq')
     gt = sgqlc.types.Field(BillingModel, graphql_name='gt')
     gte = sgqlc.types.Field(BillingModel, graphql_name='gte')
     i_like = sgqlc.types.Field(BillingModel, graphql_name='iLike')
@@ -666,23 +628,22 @@
     status = sgqlc.types.Field('CouponStatusFilterComparison', graphql_name='status')
     type = sgqlc.types.Field('CouponTypeFilterComparison', graphql_name='type')
     updated_at = sgqlc.types.Field('DateFieldComparison', graphql_name='updatedAt')
 
 
 class CouponFilterCustomerFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
+    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CouponFilterCustomerFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='billingId')
     created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmId')
     customer_id = sgqlc.types.Field('StringFieldComparison', graphql_name='customerId')
-    deleted_at = sgqlc.types.Field('DateFieldComparison', graphql_name='deletedAt')
     email = sgqlc.types.Field('StringFieldComparison', graphql_name='email')
     environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     name = sgqlc.types.Field('StringFieldComparison', graphql_name='name')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CouponFilterCustomerFilter')), graphql_name='or')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
     updated_at = sgqlc.types.Field('DateFieldComparison', graphql_name='updatedAt')
@@ -809,21 +770,14 @@
 
 class CreateManyPromotionalEntitlementsInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('promotional_entitlements',)
     promotional_entitlements = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('PromotionalEntitlementInput'))), graphql_name='promotionalEntitlements')
 
 
-class CreateMeter(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('aggregation', 'filters')
-    aggregation = sgqlc.types.Field(sgqlc.types.non_null('MeterAggregation'), graphql_name='aggregation')
-    filters = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('MeterFilterDefinitionInput'))), graphql_name='filters')
-
-
 class CreateOneEnvironmentInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('environment', 'options')
     environment = sgqlc.types.Field(sgqlc.types.non_null(CreateEnvironment), graphql_name='environment')
     options = sgqlc.types.Field(CreateEnvironmentOptions, graphql_name='options')
 
 
@@ -858,52 +812,50 @@
     before = sgqlc.types.Field(ConnectionCursor, graphql_name='before')
     first = sgqlc.types.Field(Int, graphql_name='first')
     last = sgqlc.types.Field(Int, graphql_name='last')
 
 
 class CustomerBillingInfo(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('billing_address', 'currency', 'customer_name', 'invoice_custom_fields', 'language', 'metadata', 'payment_method_id', 'shipping_address', 'tax_ids', 'timezone')
+    __field_names__ = ('billing_address', 'currency', 'customer_name', 'invoice_custom_fields', 'language', 'payment_method_id', 'shipping_address', 'tax_ids', 'timezone')
     billing_address = sgqlc.types.Field(Address, graphql_name='billingAddress')
     currency = sgqlc.types.Field(Currency, graphql_name='currency')
     customer_name = sgqlc.types.Field(String, graphql_name='customerName')
     invoice_custom_fields = sgqlc.types.Field(JSON, graphql_name='invoiceCustomFields')
     language = sgqlc.types.Field(String, graphql_name='language')
-    metadata = sgqlc.types.Field(JSON, graphql_name='metadata')
     payment_method_id = sgqlc.types.Field(String, graphql_name='paymentMethodId')
     shipping_address = sgqlc.types.Field(Address, graphql_name='shippingAddress')
     tax_ids = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('TaxExempt')), graphql_name='taxIds')
     timezone = sgqlc.types.Field(String, graphql_name='timezone')
 
 
 class CustomerFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'or_', 'promotional_entitlements', 'ref_id', 'subscriptions', 'updated_at')
+    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'or_', 'promotional_entitlements', 'ref_id', 'subscriptions', 'updated_at')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='billingId')
     created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmId')
     customer_id = sgqlc.types.Field('StringFieldComparison', graphql_name='customerId')
-    deleted_at = sgqlc.types.Field('DateFieldComparison', graphql_name='deletedAt')
     email = sgqlc.types.Field('StringFieldComparison', graphql_name='email')
     environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     name = sgqlc.types.Field('StringFieldComparison', graphql_name='name')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerFilter')), graphql_name='or')
     promotional_entitlements = sgqlc.types.Field('CustomerFilterPromotionalEntitlementFilter', graphql_name='promotionalEntitlements')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
     subscriptions = sgqlc.types.Field('CustomerFilterCustomerSubscriptionFilter', graphql_name='subscriptions')
     updated_at = sgqlc.types.Field('DateFieldComparison', graphql_name='updatedAt')
 
 
 class CustomerFilterCustomerSubscriptionFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'resource_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerFilterCustomerSubscriptionFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='billingId')
     cancel_reason = sgqlc.types.Field('SubscriptionCancelReasonFilterComparison', graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field('DateFieldComparison', graphql_name='cancellationDate')
     created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
     crm_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmId')
     crm_link_url = sgqlc.types.Field('StringFieldComparison', graphql_name='crmLinkUrl')
@@ -911,15 +863,14 @@
     end_date = sgqlc.types.Field('DateFieldComparison', graphql_name='endDate')
     environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     old_billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='oldBillingId')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerFilterCustomerSubscriptionFilter')), graphql_name='or')
     pricing_type = sgqlc.types.Field('PricingTypeFilterComparison', graphql_name='pricingType')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
-    resource_id = sgqlc.types.Field('StringFieldComparison', graphql_name='resourceId')
     start_date = sgqlc.types.Field('DateFieldComparison', graphql_name='startDate')
     status = sgqlc.types.Field('SubscriptionStatusFilterComparison', graphql_name='status')
     subscription_id = sgqlc.types.Field('StringFieldComparison', graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field('DateFieldComparison', graphql_name='trialEndDate')
 
 
 class CustomerFilterPromotionalEntitlementFilter(sgqlc.types.Input):
@@ -969,17 +920,16 @@
     custom_css = sgqlc.types.Field(String, graphql_name='customCss')
     palette = sgqlc.types.Field(CustomerPortalColorsPaletteInput, graphql_name='palette')
     typography = sgqlc.types.Field('TypographyConfigurationInput', graphql_name='typography')
 
 
 class CustomerPortalInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('customer_id', 'product_id', 'resource_id')
+    __field_names__ = ('customer_id', 'resource_id')
     customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
-    product_id = sgqlc.types.Field(String, graphql_name='productId')
     resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
 
 
 class CustomerResourceFilter(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('and_', 'created_at', 'customer', 'environment_id', 'or_', 'resource_id', 'subscriptions')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerResourceFilter')), graphql_name='and')
@@ -989,35 +939,34 @@
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerResourceFilter')), graphql_name='or')
     resource_id = sgqlc.types.Field('StringFieldComparison', graphql_name='resourceId')
     subscriptions = sgqlc.types.Field('CustomerResourceFilterCustomerSubscriptionFilter', graphql_name='subscriptions')
 
 
 class CustomerResourceFilterCustomerFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
+    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerResourceFilterCustomerFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='billingId')
     created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmId')
     customer_id = sgqlc.types.Field('StringFieldComparison', graphql_name='customerId')
-    deleted_at = sgqlc.types.Field('DateFieldComparison', graphql_name='deletedAt')
     email = sgqlc.types.Field('StringFieldComparison', graphql_name='email')
     environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     name = sgqlc.types.Field('StringFieldComparison', graphql_name='name')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerResourceFilterCustomerFilter')), graphql_name='or')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
     updated_at = sgqlc.types.Field('DateFieldComparison', graphql_name='updatedAt')
 
 
 class CustomerResourceFilterCustomerSubscriptionFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'resource_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerResourceFilterCustomerSubscriptionFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='billingId')
     cancel_reason = sgqlc.types.Field('SubscriptionCancelReasonFilterComparison', graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field('DateFieldComparison', graphql_name='cancellationDate')
     created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
     crm_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmId')
     crm_link_url = sgqlc.types.Field('StringFieldComparison', graphql_name='crmLinkUrl')
@@ -1025,15 +974,14 @@
     end_date = sgqlc.types.Field('DateFieldComparison', graphql_name='endDate')
     environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     old_billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='oldBillingId')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerResourceFilterCustomerSubscriptionFilter')), graphql_name='or')
     pricing_type = sgqlc.types.Field('PricingTypeFilterComparison', graphql_name='pricingType')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
-    resource_id = sgqlc.types.Field('StringFieldComparison', graphql_name='resourceId')
     start_date = sgqlc.types.Field('DateFieldComparison', graphql_name='startDate')
     status = sgqlc.types.Field('SubscriptionStatusFilterComparison', graphql_name='status')
     subscription_id = sgqlc.types.Field('StringFieldComparison', graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field('DateFieldComparison', graphql_name='trialEndDate')
 
 
 class CustomerResourceSort(sgqlc.types.Input):
@@ -1050,15 +998,15 @@
     direction = sgqlc.types.Field(sgqlc.types.non_null(SortDirection), graphql_name='direction')
     field = sgqlc.types.Field(sgqlc.types.non_null(CustomerSortFields), graphql_name='field')
     nulls = sgqlc.types.Field(SortNulls, graphql_name='nulls')
 
 
 class CustomerSubscriptionFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('addons', 'and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'customer', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'plan', 'prices', 'pricing_type', 'ref_id', 'resource', 'resource_id', 'start_date', 'status', 'subscription_entitlements', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('addons', 'and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'customer', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'prices', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_entitlements', 'subscription_id', 'trial_end_date')
     addons = sgqlc.types.Field('CustomerSubscriptionFilterSubscriptionAddonFilter', graphql_name='addons')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='billingId')
     cancel_reason = sgqlc.types.Field('SubscriptionCancelReasonFilterComparison', graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field('DateFieldComparison', graphql_name='cancellationDate')
     created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
     crm_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmId')
@@ -1066,77 +1014,43 @@
     customer = sgqlc.types.Field('CustomerSubscriptionFilterCustomerFilter', graphql_name='customer')
     effective_end_date = sgqlc.types.Field('DateFieldComparison', graphql_name='effectiveEndDate')
     end_date = sgqlc.types.Field('DateFieldComparison', graphql_name='endDate')
     environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     old_billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='oldBillingId')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilter')), graphql_name='or')
-    plan = sgqlc.types.Field('CustomerSubscriptionFilterPlanFilter', graphql_name='plan')
     prices = sgqlc.types.Field('CustomerSubscriptionFilterSubscriptionPriceFilter', graphql_name='prices')
     pricing_type = sgqlc.types.Field('PricingTypeFilterComparison', graphql_name='pricingType')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
-    resource = sgqlc.types.Field('CustomerSubscriptionFilterCustomerResourceFilter', graphql_name='resource')
-    resource_id = sgqlc.types.Field('StringFieldComparison', graphql_name='resourceId')
     start_date = sgqlc.types.Field('DateFieldComparison', graphql_name='startDate')
     status = sgqlc.types.Field('SubscriptionStatusFilterComparison', graphql_name='status')
     subscription_entitlements = sgqlc.types.Field('CustomerSubscriptionFilterSubscriptionEntitlementFilter', graphql_name='subscriptionEntitlements')
     subscription_id = sgqlc.types.Field('StringFieldComparison', graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field('DateFieldComparison', graphql_name='trialEndDate')
 
 
 class CustomerSubscriptionFilterCustomerFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
+    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterCustomerFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='billingId')
     created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmId')
     customer_id = sgqlc.types.Field('StringFieldComparison', graphql_name='customerId')
-    deleted_at = sgqlc.types.Field('DateFieldComparison', graphql_name='deletedAt')
     email = sgqlc.types.Field('StringFieldComparison', graphql_name='email')
     environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     name = sgqlc.types.Field('StringFieldComparison', graphql_name='name')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterCustomerFilter')), graphql_name='or')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
     updated_at = sgqlc.types.Field('DateFieldComparison', graphql_name='updatedAt')
 
 
-class CustomerSubscriptionFilterCustomerResourceFilter(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('and_', 'created_at', 'environment_id', 'or_', 'resource_id')
-    and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterCustomerResourceFilter')), graphql_name='and')
-    created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
-    environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
-    or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterCustomerResourceFilter')), graphql_name='or')
-    resource_id = sgqlc.types.Field('StringFieldComparison', graphql_name='resourceId')
-
-
-class CustomerSubscriptionFilterPlanFilter(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'created_at', 'description', 'display_name', 'environment_id', 'id', 'is_latest', 'or_', 'pricing_type', 'product_id', 'ref_id', 'status', 'updated_at', 'version_number')
-    and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterPlanFilter')), graphql_name='and')
-    billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='billingId')
-    created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
-    description = sgqlc.types.Field('StringFieldComparison', graphql_name='description')
-    display_name = sgqlc.types.Field('StringFieldComparison', graphql_name='displayName')
-    environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
-    id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
-    is_latest = sgqlc.types.Field(BooleanFieldComparison, graphql_name='isLatest')
-    or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterPlanFilter')), graphql_name='or')
-    pricing_type = sgqlc.types.Field('PricingTypeFilterComparison', graphql_name='pricingType')
-    product_id = sgqlc.types.Field('StringFieldComparison', graphql_name='productId')
-    ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
-    status = sgqlc.types.Field('PackageStatusFilterComparison', graphql_name='status')
-    updated_at = sgqlc.types.Field('DateFieldComparison', graphql_name='updatedAt')
-    version_number = sgqlc.types.Field('IntFieldComparison', graphql_name='versionNumber')
-
-
 class CustomerSubscriptionFilterSubscriptionAddonFilter(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('and_', 'created_at', 'id', 'or_', 'quantity', 'updated_at')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterSubscriptionAddonFilter')), graphql_name='and')
     created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterSubscriptionAddonFilter')), graphql_name='or')
@@ -1154,19 +1068,17 @@
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterSubscriptionEntitlementFilter')), graphql_name='or')
     subscription_id = sgqlc.types.Field('StringFieldComparison', graphql_name='subscriptionId')
     updated_at = sgqlc.types.Field('DateFieldComparison', graphql_name='updatedAt')
 
 
 class CustomerSubscriptionFilterSubscriptionPriceFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_model', 'created_at', 'feature_id', 'id', 'or_', 'updated_at', 'usage_limit')
+    __field_names__ = ('and_', 'created_at', 'id', 'or_', 'updated_at', 'usage_limit')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterSubscriptionPriceFilter')), graphql_name='and')
-    billing_model = sgqlc.types.Field(BillingModelFilterComparison, graphql_name='billingModel')
     created_at = sgqlc.types.Field('DateFieldComparison', graphql_name='createdAt')
-    feature_id = sgqlc.types.Field('StringFieldComparison', graphql_name='featureId')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionFilterSubscriptionPriceFilter')), graphql_name='or')
     updated_at = sgqlc.types.Field('DateFieldComparison', graphql_name='updatedAt')
     usage_limit = sgqlc.types.Field('NumberFieldComparison', graphql_name='usageLimit')
 
 
 class CustomerSubscriptionSort(sgqlc.types.Input):
@@ -1204,14 +1116,21 @@
 class DefaultTrialConfigInputDTO(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('duration', 'units')
     duration = sgqlc.types.Field(Float, graphql_name='duration')
     units = sgqlc.types.Field(TrialPeriodUnits, graphql_name='units')
 
 
+class DeleteCustomerInput(sgqlc.types.Input):
+    __schema__ = schema
+    __field_names__ = ('environment_id', 'id')
+    environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
+    id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
+
+
 class DeleteFeatureInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('environment_id', 'id')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
 
 
@@ -1330,36 +1249,33 @@
     direction = sgqlc.types.Field(sgqlc.types.non_null(SortDirection), graphql_name='direction')
     field = sgqlc.types.Field(sgqlc.types.non_null(EnvironmentSortFields), graphql_name='field')
     nulls = sgqlc.types.Field(SortNulls, graphql_name='nulls')
 
 
 class EstimateSubscriptionInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('addons', 'billable_features', 'billing_country_code', 'billing_information', 'billing_period', 'customer_id', 'environment_id', 'plan_id', 'price_unit_amount', 'promotion_code', 'resource_id', 'skip_trial', 'start_date', 'unit_quantity')
+    __field_names__ = ('addons', 'billing_country_code', 'billing_information', 'billing_period', 'customer_id', 'environment_id', 'plan_id', 'price_unit_amount', 'promotion_code', 'resource_id', 'skip_trial', 'start_date')
     addons = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionAddonInput')), graphql_name='addons')
-    billable_features = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(BillableFeatureInput)), graphql_name='billableFeatures')
     billing_country_code = sgqlc.types.Field(String, graphql_name='billingCountryCode')
     billing_information = sgqlc.types.Field('SubscriptionBillingInfo', graphql_name='billingInformation')
     billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
     customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     plan_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='planId')
     price_unit_amount = sgqlc.types.Field(Float, graphql_name='priceUnitAmount')
     promotion_code = sgqlc.types.Field(String, graphql_name='promotionCode')
     resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     skip_trial = sgqlc.types.Field(Boolean, graphql_name='skipTrial')
     start_date = sgqlc.types.Field(DateTime, graphql_name='startDate')
-    unit_quantity = sgqlc.types.Field(Float, graphql_name='unitQuantity')
 
 
 class EstimateSubscriptionUpdateInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('addons', 'billable_features', 'environment_id', 'promotion_code', 'subscription_id', 'unit_quantity')
+    __field_names__ = ('addons', 'environment_id', 'promotion_code', 'subscription_id', 'unit_quantity')
     addons = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionAddonInput')), graphql_name='addons')
-    billable_features = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(BillableFeatureInput)), graphql_name='billableFeatures')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     promotion_code = sgqlc.types.Field(String, graphql_name='promotionCode')
     subscription_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='subscriptionId')
     unit_quantity = sgqlc.types.Field(Float, graphql_name='unitQuantity')
 
 
 class ExperimentFilter(sgqlc.types.Input):
@@ -1375,23 +1291,22 @@
     product_id = sgqlc.types.Field('StringFieldComparison', graphql_name='productId')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
     status = sgqlc.types.Field('ExperimentStatusFilterComparison', graphql_name='status')
 
 
 class ExperimentFilterCustomerFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
+    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('ExperimentFilterCustomerFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field('StringFieldComparison', graphql_name='billingId')
     created_at = sgqlc.types.Field(DateFieldComparison, graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field('StringFieldComparison', graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field('StringFieldComparison', graphql_name='crmId')
     customer_id = sgqlc.types.Field('StringFieldComparison', graphql_name='customerId')
-    deleted_at = sgqlc.types.Field(DateFieldComparison, graphql_name='deletedAt')
     email = sgqlc.types.Field('StringFieldComparison', graphql_name='email')
     environment_id = sgqlc.types.Field('StringFieldComparison', graphql_name='environmentId')
     id = sgqlc.types.Field('StringFieldComparison', graphql_name='id')
     name = sgqlc.types.Field('StringFieldComparison', graphql_name='name')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('ExperimentFilterCustomerFilter')), graphql_name='or')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
     updated_at = sgqlc.types.Field(DateFieldComparison, graphql_name='updatedAt')
@@ -1446,24 +1361,23 @@
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('FeatureFilter')), graphql_name='or')
     ref_id = sgqlc.types.Field('StringFieldComparison', graphql_name='refId')
     updated_at = sgqlc.types.Field(DateFieldComparison, graphql_name='updatedAt')
 
 
 class FeatureInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('additional_meta_data', 'description', 'display_name', 'environment_id', 'feature_status', 'feature_type', 'feature_units', 'feature_units_plural', 'meter', 'meter_type', 'ref_id')
+    __field_names__ = ('additional_meta_data', 'description', 'display_name', 'environment_id', 'feature_status', 'feature_type', 'feature_units', 'feature_units_plural', 'meter_type', 'ref_id')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     description = sgqlc.types.Field(String, graphql_name='description')
     display_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='displayName')
     environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
     feature_status = sgqlc.types.Field(FeatureStatus, graphql_name='featureStatus')
     feature_type = sgqlc.types.Field(sgqlc.types.non_null(FeatureType), graphql_name='featureType')
     feature_units = sgqlc.types.Field(String, graphql_name='featureUnits')
     feature_units_plural = sgqlc.types.Field(String, graphql_name='featureUnitsPlural')
-    meter = sgqlc.types.Field(CreateMeter, graphql_name='meter')
     meter_type = sgqlc.types.Field(MeterType, graphql_name='meterType')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
 
 
 class FeatureSort(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('direction', 'field', 'nulls')
@@ -1533,19 +1447,18 @@
     __field_names__ = ('font_size', 'font_weight')
     font_size = sgqlc.types.Field(Float, graphql_name='fontSize')
     font_weight = sgqlc.types.Field(FontWeight, graphql_name='fontWeight')
 
 
 class GetActiveSubscriptionsInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('customer_id', 'environment_id', 'resource_id', 'resource_ids')
+    __field_names__ = ('customer_id', 'environment_id', 'resource_id')
     customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
-    resource_ids = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(String)), graphql_name='resourceIds')
 
 
 class GetCustomerByRefIdInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('customer_id', 'environment_id')
     customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
@@ -1712,14 +1625,32 @@
 class InitAddStripeCustomerPaymentMethodInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('customer_ref_id', 'environment_id')
     customer_ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerRefId')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
 
 
+class InitiateCheckoutInput(sgqlc.types.Input):
+    __schema__ = schema
+    __field_names__ = ('addons', 'allow_promo_codes', 'allow_tax_id_collection', 'billing_country_code', 'billing_period', 'cancel_url', 'collect_billing_address', 'collect_phone_number', 'customer_id', 'plan_id', 'resource_id', 'success_url', 'unit_quantity')
+    addons = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionAddonInput')), graphql_name='addons')
+    allow_promo_codes = sgqlc.types.Field(Boolean, graphql_name='allowPromoCodes')
+    allow_tax_id_collection = sgqlc.types.Field(Boolean, graphql_name='allowTaxIdCollection')
+    billing_country_code = sgqlc.types.Field(String, graphql_name='billingCountryCode')
+    billing_period = sgqlc.types.Field(sgqlc.types.non_null(BillingPeriod), graphql_name='billingPeriod')
+    cancel_url = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='cancelUrl')
+    collect_billing_address = sgqlc.types.Field(Boolean, graphql_name='collectBillingAddress')
+    collect_phone_number = sgqlc.types.Field(Boolean, graphql_name='collectPhoneNumber')
+    customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
+    plan_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='planId')
+    resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
+    success_url = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='successUrl')
+    unit_quantity = sgqlc.types.Field(Int, graphql_name='unitQuantity')
+
+
 class IntFieldComparison(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('between', 'eq', 'gt', 'gte', 'in_', 'is_', 'is_not', 'lt', 'lte', 'neq', 'not_between', 'not_in')
     between = sgqlc.types.Field('IntFieldComparisonBetween', graphql_name='between')
     eq = sgqlc.types.Field(Int, graphql_name='eq')
     gt = sgqlc.types.Field(Int, graphql_name='gt')
     gte = sgqlc.types.Field(Int, graphql_name='gte')
@@ -1772,35 +1703,14 @@
     __schema__ = schema
     __field_names__ = ('direction', 'field', 'nulls')
     direction = sgqlc.types.Field(sgqlc.types.non_null(SortDirection), graphql_name='direction')
     field = sgqlc.types.Field(sgqlc.types.non_null(MemberSortFields), graphql_name='field')
     nulls = sgqlc.types.Field(SortNulls, graphql_name='nulls')
 
 
-class MeterAggregation(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('field', 'function')
-    field = sgqlc.types.Field(String, graphql_name='field')
-    function = sgqlc.types.Field(sgqlc.types.non_null(AggregationFunction), graphql_name='function')
-
-
-class MeterConditionInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('field', 'operation', 'value')
-    field = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='field')
-    operation = sgqlc.types.Field(sgqlc.types.non_null(ConditionOperation), graphql_name='operation')
-    value = sgqlc.types.Field(String, graphql_name='value')
-
-
-class MeterFilterDefinitionInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('conditions',)
-    conditions = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(MeterConditionInput))), graphql_name='conditions')
-
-
 class MeterTypeFilterComparison(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('eq', 'gt', 'gte', 'i_like', 'in_', 'is_', 'is_not', 'like', 'lt', 'lte', 'neq', 'not_ilike', 'not_in', 'not_like')
     eq = sgqlc.types.Field(MeterType, graphql_name='eq')
     gt = sgqlc.types.Field(MeterType, graphql_name='gt')
     gte = sgqlc.types.Field(MeterType, graphql_name='gte')
     i_like = sgqlc.types.Field(MeterType, graphql_name='iLike')
@@ -1971,19 +1881,18 @@
     reset_period = sgqlc.types.Field(EntitlementResetPeriod, graphql_name='resetPeriod')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
     weekly_reset_period_configuration = sgqlc.types.Field('WeeklyResetPeriodConfigInput', graphql_name='weeklyResetPeriodConfiguration')
 
 
 class PackagePricingInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('environment_id', 'package_id', 'pricing_model', 'pricing_models', 'pricing_type')
+    __field_names__ = ('environment_id', 'package_id', 'pricing_model', 'pricing_type')
     environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
     package_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='packageId')
     pricing_model = sgqlc.types.Field('PricingModelCreateInput', graphql_name='pricingModel')
-    pricing_models = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('PricingModelCreateInput')), graphql_name='pricingModels')
     pricing_type = sgqlc.types.Field(sgqlc.types.non_null(PricingType), graphql_name='pricingType')
 
 
 class PackagePublishInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('id', 'migration_type')
     id = sgqlc.types.Field(sgqlc.types.non_null(ID), graphql_name='id')
@@ -2351,96 +2260,80 @@
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     should_sync_free = sgqlc.types.Field(Boolean, graphql_name='shouldSyncFree')
     subscription_params = sgqlc.types.Field('ProvisionCustomerSubscriptionInput', graphql_name='subscriptionParams')
 
 
 class ProvisionCustomerSubscriptionInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('additional_meta_data', 'addons', 'await_payment_confirmation', 'billable_features', 'billing_country_code', 'billing_id', 'billing_information', 'billing_period', 'plan_id', 'price_unit_amount', 'promotion_code', 'ref_id', 'resource_id', 'start_date', 'subscription_id', 'unit_quantity')
+    __field_names__ = ('additional_meta_data', 'addons', 'await_payment_confirmation', 'billing_country_code', 'billing_id', 'billing_information', 'billing_period', 'plan_id', 'price_unit_amount', 'promotion_code', 'ref_id', 'resource_id', 'start_date', 'subscription_id')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     addons = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionAddonInput')), graphql_name='addons')
     await_payment_confirmation = sgqlc.types.Field(Boolean, graphql_name='awaitPaymentConfirmation')
-    billable_features = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(BillableFeatureInput)), graphql_name='billableFeatures')
     billing_country_code = sgqlc.types.Field(String, graphql_name='billingCountryCode')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     billing_information = sgqlc.types.Field('SubscriptionBillingInfo', graphql_name='billingInformation')
     billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
     plan_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='planId')
     price_unit_amount = sgqlc.types.Field(Float, graphql_name='priceUnitAmount')
     promotion_code = sgqlc.types.Field(String, graphql_name='promotionCode')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     start_date = sgqlc.types.Field(DateTime, graphql_name='startDate')
     subscription_id = sgqlc.types.Field(String, graphql_name='subscriptionId')
-    unit_quantity = sgqlc.types.Field(Float, graphql_name='unitQuantity')
 
 
 class ProvisionSandboxInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('billing_model', 'display_name')
     billing_model = sgqlc.types.Field(sgqlc.types.non_null(BillingModel), graphql_name='billingModel')
     display_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='displayName')
 
 
 class ProvisionSubscription(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('additional_meta_data', 'addons', 'await_payment_confirmation', 'billable_features', 'billing_country_code', 'billing_id', 'billing_information', 'billing_period', 'checkout_options', 'customer_id', 'plan_id', 'price_unit_amount', 'promotion_code', 'ref_id', 'resource_id', 'skip_trial', 'start_date', 'subscription_id', 'unit_quantity')
+    __field_names__ = ('additional_meta_data', 'addons', 'await_payment_confirmation', 'billing_country_code', 'billing_id', 'billing_information', 'billing_period', 'checkout_options', 'customer_id', 'plan_id', 'price_unit_amount', 'promotion_code', 'ref_id', 'resource_id', 'skip_trial', 'start_date', 'subscription_id')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     addons = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionAddonInput')), graphql_name='addons')
     await_payment_confirmation = sgqlc.types.Field(Boolean, graphql_name='awaitPaymentConfirmation')
-    billable_features = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(BillableFeatureInput)), graphql_name='billableFeatures')
     billing_country_code = sgqlc.types.Field(String, graphql_name='billingCountryCode')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     billing_information = sgqlc.types.Field('SubscriptionBillingInfo', graphql_name='billingInformation')
     billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
     checkout_options = sgqlc.types.Field(CheckoutOptions, graphql_name='checkoutOptions')
     customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
     plan_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='planId')
     price_unit_amount = sgqlc.types.Field(Float, graphql_name='priceUnitAmount')
     promotion_code = sgqlc.types.Field(String, graphql_name='promotionCode')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     skip_trial = sgqlc.types.Field(Boolean, graphql_name='skipTrial')
     start_date = sgqlc.types.Field(DateTime, graphql_name='startDate')
     subscription_id = sgqlc.types.Field(String, graphql_name='subscriptionId')
-    unit_quantity = sgqlc.types.Field(Float, graphql_name='unitQuantity')
 
 
 class ProvisionSubscriptionInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('additional_meta_data', 'addons', 'await_payment_confirmation', 'billable_features', 'billing_country_code', 'billing_id', 'billing_information', 'billing_period', 'checkout_options', 'customer_id', 'plan_id', 'price_unit_amount', 'promotion_code', 'ref_id', 'resource_id', 'skip_trial', 'start_date', 'subscription_id', 'unit_quantity')
+    __field_names__ = ('additional_meta_data', 'addons', 'await_payment_confirmation', 'billing_country_code', 'billing_id', 'billing_information', 'billing_period', 'checkout_options', 'customer_id', 'plan_id', 'price_unit_amount', 'promotion_code', 'ref_id', 'resource_id', 'skip_trial', 'start_date', 'subscription_id')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     addons = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionAddonInput')), graphql_name='addons')
     await_payment_confirmation = sgqlc.types.Field(Boolean, graphql_name='awaitPaymentConfirmation')
-    billable_features = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(BillableFeatureInput)), graphql_name='billableFeatures')
     billing_country_code = sgqlc.types.Field(String, graphql_name='billingCountryCode')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     billing_information = sgqlc.types.Field('SubscriptionBillingInfo', graphql_name='billingInformation')
     billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
     checkout_options = sgqlc.types.Field(CheckoutOptions, graphql_name='checkoutOptions')
     customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
     plan_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='planId')
     price_unit_amount = sgqlc.types.Field(Float, graphql_name='priceUnitAmount')
     promotion_code = sgqlc.types.Field(String, graphql_name='promotionCode')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     skip_trial = sgqlc.types.Field(Boolean, graphql_name='skipTrial')
     start_date = sgqlc.types.Field(DateTime, graphql_name='startDate')
     subscription_id = sgqlc.types.Field(String, graphql_name='subscriptionId')
-    unit_quantity = sgqlc.types.Field(Float, graphql_name='unitQuantity')
-
-
-class RecalculateEntitlementsInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('customer_ids', 'environment_id', 'for_all_customers', 'last_calculation_before', 'max_batches')
-    customer_ids = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(String)), graphql_name='customerIds')
-    environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
-    for_all_customers = sgqlc.types.Field(Boolean, graphql_name='forAllCustomers')
-    last_calculation_before = sgqlc.types.Field(DateTime, graphql_name='lastCalculationBefore')
-    max_batches = sgqlc.types.Field(Int, graphql_name='maxBatches')
 
 
 class RemoveBasePlanFromPlanInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('id', 'relation_id')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
     relation_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='relationId')
@@ -2477,26 +2370,14 @@
 class RemoveExperimentFromCustomerSubscriptionInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('id', 'relation_id')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
     relation_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='relationId')
 
 
-class ReportUsageInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('created_at', 'customer_id', 'environment_id', 'feature_id', 'resource_id', 'update_behavior', 'value')
-    created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
-    customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
-    environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
-    feature_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='featureId')
-    resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
-    update_behavior = sgqlc.types.Field(UsageUpdateBehavior, graphql_name='updateBehavior')
-    value = sgqlc.types.Field(sgqlc.types.non_null(Float), graphql_name='value')
-
-
 class ResyncIntegrationInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('environment_id', 'vendor_identifier')
     environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
     vendor_identifier = sgqlc.types.Field(sgqlc.types.non_null(VendorIdentifier), graphql_name='vendorIdentifier')
 
 
@@ -2638,15 +2519,15 @@
     status = sgqlc.types.Field(PackageStatusFilterComparison, graphql_name='status')
     updated_at = sgqlc.types.Field(DateFieldComparison, graphql_name='updatedAt')
     version_number = sgqlc.types.Field(IntFieldComparison, graphql_name='versionNumber')
 
 
 class SubscriptionAddonFilterCustomerSubscriptionFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'resource_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionAddonFilterCustomerSubscriptionFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field(StringFieldComparison, graphql_name='billingId')
     cancel_reason = sgqlc.types.Field('SubscriptionCancelReasonFilterComparison', graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field(DateFieldComparison, graphql_name='cancellationDate')
     created_at = sgqlc.types.Field(DateFieldComparison, graphql_name='createdAt')
     crm_id = sgqlc.types.Field(StringFieldComparison, graphql_name='crmId')
     crm_link_url = sgqlc.types.Field(StringFieldComparison, graphql_name='crmLinkUrl')
@@ -2654,15 +2535,14 @@
     end_date = sgqlc.types.Field(DateFieldComparison, graphql_name='endDate')
     environment_id = sgqlc.types.Field(StringFieldComparison, graphql_name='environmentId')
     id = sgqlc.types.Field(StringFieldComparison, graphql_name='id')
     old_billing_id = sgqlc.types.Field(StringFieldComparison, graphql_name='oldBillingId')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionAddonFilterCustomerSubscriptionFilter')), graphql_name='or')
     pricing_type = sgqlc.types.Field(PricingTypeFilterComparison, graphql_name='pricingType')
     ref_id = sgqlc.types.Field(StringFieldComparison, graphql_name='refId')
-    resource_id = sgqlc.types.Field(StringFieldComparison, graphql_name='resourceId')
     start_date = sgqlc.types.Field(DateFieldComparison, graphql_name='startDate')
     status = sgqlc.types.Field('SubscriptionStatusFilterComparison', graphql_name='status')
     subscription_id = sgqlc.types.Field(StringFieldComparison, graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field(DateFieldComparison, graphql_name='trialEndDate')
 
 
 class SubscriptionAddonFilterPriceFilter(sgqlc.types.Input):
@@ -2738,15 +2618,15 @@
     subscription = sgqlc.types.Field('SubscriptionEntitlementFilterCustomerSubscriptionFilter', graphql_name='subscription')
     subscription_id = sgqlc.types.Field(StringFieldComparison, graphql_name='subscriptionId')
     updated_at = sgqlc.types.Field(DateFieldComparison, graphql_name='updatedAt')
 
 
 class SubscriptionEntitlementFilterCustomerSubscriptionFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'resource_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionEntitlementFilterCustomerSubscriptionFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field(StringFieldComparison, graphql_name='billingId')
     cancel_reason = sgqlc.types.Field(SubscriptionCancelReasonFilterComparison, graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field(DateFieldComparison, graphql_name='cancellationDate')
     created_at = sgqlc.types.Field(DateFieldComparison, graphql_name='createdAt')
     crm_id = sgqlc.types.Field(StringFieldComparison, graphql_name='crmId')
     crm_link_url = sgqlc.types.Field(StringFieldComparison, graphql_name='crmLinkUrl')
@@ -2754,15 +2634,14 @@
     end_date = sgqlc.types.Field(DateFieldComparison, graphql_name='endDate')
     environment_id = sgqlc.types.Field(StringFieldComparison, graphql_name='environmentId')
     id = sgqlc.types.Field(StringFieldComparison, graphql_name='id')
     old_billing_id = sgqlc.types.Field(StringFieldComparison, graphql_name='oldBillingId')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionEntitlementFilterCustomerSubscriptionFilter')), graphql_name='or')
     pricing_type = sgqlc.types.Field(PricingTypeFilterComparison, graphql_name='pricingType')
     ref_id = sgqlc.types.Field(StringFieldComparison, graphql_name='refId')
-    resource_id = sgqlc.types.Field(StringFieldComparison, graphql_name='resourceId')
     start_date = sgqlc.types.Field(DateFieldComparison, graphql_name='startDate')
     status = sgqlc.types.Field('SubscriptionStatusFilterComparison', graphql_name='status')
     subscription_id = sgqlc.types.Field(StringFieldComparison, graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field(DateFieldComparison, graphql_name='trialEndDate')
 
 
 class SubscriptionEntitlementFilterFeatureFilter(sgqlc.types.Input):
@@ -2800,19 +2679,18 @@
     direction = sgqlc.types.Field(sgqlc.types.non_null(SortDirection), graphql_name='direction')
     field = sgqlc.types.Field(sgqlc.types.non_null(SubscriptionEntitlementSortFields), graphql_name='field')
     nulls = sgqlc.types.Field(SortNulls, graphql_name='nulls')
 
 
 class SubscriptionInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('additional_meta_data', 'addons', 'await_payment_confirmation', 'billable_features', 'billing_country_code', 'billing_id', 'billing_information', 'billing_period', 'crm_id', 'customer_id', 'end_date', 'environment_id', 'is_custom_price_subscription', 'is_overriding_trial_config', 'is_trial', 'plan_id', 'price_unit_amount', 'promotion_code', 'ref_id', 'resource_id', 'start_date', 'subscription_entitlements', 'subscription_id', 'unit_quantity')
+    __field_names__ = ('additional_meta_data', 'addons', 'await_payment_confirmation', 'billing_country_code', 'billing_id', 'billing_information', 'billing_period', 'crm_id', 'customer_id', 'end_date', 'environment_id', 'is_custom_price_subscription', 'is_overriding_trial_config', 'is_trial', 'plan_id', 'price_unit_amount', 'promotion_code', 'ref_id', 'resource_id', 'start_date', 'subscription_entitlements', 'subscription_id')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     addons = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(SubscriptionAddonInput)), graphql_name='addons')
     await_payment_confirmation = sgqlc.types.Field(Boolean, graphql_name='awaitPaymentConfirmation')
-    billable_features = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(BillableFeatureInput)), graphql_name='billableFeatures')
     billing_country_code = sgqlc.types.Field(String, graphql_name='billingCountryCode')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     billing_information = sgqlc.types.Field(SubscriptionBillingInfo, graphql_name='billingInformation')
     billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
     crm_id = sgqlc.types.Field(String, graphql_name='crmId')
     customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
     end_date = sgqlc.types.Field(DateTime, graphql_name='endDate')
@@ -2824,23 +2702,21 @@
     price_unit_amount = sgqlc.types.Field(Float, graphql_name='priceUnitAmount')
     promotion_code = sgqlc.types.Field(String, graphql_name='promotionCode')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     start_date = sgqlc.types.Field(DateTime, graphql_name='startDate')
     subscription_entitlements = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(SubscriptionEntitlementInput)), graphql_name='subscriptionEntitlements')
     subscription_id = sgqlc.types.Field(String, graphql_name='subscriptionId')
-    unit_quantity = sgqlc.types.Field(Float, graphql_name='unitQuantity')
 
 
 class SubscriptionMigrationInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('environment_id', 'subscription_id', 'subscription_migration_time')
+    __field_names__ = ('environment_id', 'subscription_id')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     subscription_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='subscriptionId')
-    subscription_migration_time = sgqlc.types.Field(SubscriptionMigrationTime, graphql_name='subscriptionMigrationTime')
 
 
 class SubscriptionMigrationTaskFilter(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('and_', 'created_at', 'environment_id', 'id', 'or_', 'status', 'task_type')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionMigrationTaskFilter')), graphql_name='and')
     created_at = sgqlc.types.Field(DateFieldComparison, graphql_name='createdAt')
@@ -2857,30 +2733,28 @@
     direction = sgqlc.types.Field(sgqlc.types.non_null(SortDirection), graphql_name='direction')
     field = sgqlc.types.Field(sgqlc.types.non_null(SubscriptionMigrationTaskSortFields), graphql_name='field')
     nulls = sgqlc.types.Field(SortNulls, graphql_name='nulls')
 
 
 class SubscriptionPriceFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_model', 'created_at', 'feature_id', 'id', 'or_', 'price', 'subscription', 'updated_at', 'usage_limit')
+    __field_names__ = ('and_', 'created_at', 'id', 'or_', 'price', 'subscription', 'updated_at', 'usage_limit')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionPriceFilter')), graphql_name='and')
-    billing_model = sgqlc.types.Field(BillingModelFilterComparison, graphql_name='billingModel')
     created_at = sgqlc.types.Field(DateFieldComparison, graphql_name='createdAt')
-    feature_id = sgqlc.types.Field(StringFieldComparison, graphql_name='featureId')
     id = sgqlc.types.Field(StringFieldComparison, graphql_name='id')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionPriceFilter')), graphql_name='or')
     price = sgqlc.types.Field('SubscriptionPriceFilterPriceFilter', graphql_name='price')
     subscription = sgqlc.types.Field('SubscriptionPriceFilterCustomerSubscriptionFilter', graphql_name='subscription')
     updated_at = sgqlc.types.Field(DateFieldComparison, graphql_name='updatedAt')
     usage_limit = sgqlc.types.Field(NumberFieldComparison, graphql_name='usageLimit')
 
 
 class SubscriptionPriceFilterCustomerSubscriptionFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'resource_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('and_', 'billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'or_', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionPriceFilterCustomerSubscriptionFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field(StringFieldComparison, graphql_name='billingId')
     cancel_reason = sgqlc.types.Field(SubscriptionCancelReasonFilterComparison, graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field(DateFieldComparison, graphql_name='cancellationDate')
     created_at = sgqlc.types.Field(DateFieldComparison, graphql_name='createdAt')
     crm_id = sgqlc.types.Field(StringFieldComparison, graphql_name='crmId')
     crm_link_url = sgqlc.types.Field(StringFieldComparison, graphql_name='crmLinkUrl')
@@ -2888,15 +2762,14 @@
     end_date = sgqlc.types.Field(DateFieldComparison, graphql_name='endDate')
     environment_id = sgqlc.types.Field(StringFieldComparison, graphql_name='environmentId')
     id = sgqlc.types.Field(StringFieldComparison, graphql_name='id')
     old_billing_id = sgqlc.types.Field(StringFieldComparison, graphql_name='oldBillingId')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionPriceFilterCustomerSubscriptionFilter')), graphql_name='or')
     pricing_type = sgqlc.types.Field(PricingTypeFilterComparison, graphql_name='pricingType')
     ref_id = sgqlc.types.Field(StringFieldComparison, graphql_name='refId')
-    resource_id = sgqlc.types.Field(StringFieldComparison, graphql_name='resourceId')
     start_date = sgqlc.types.Field(DateFieldComparison, graphql_name='startDate')
     status = sgqlc.types.Field('SubscriptionStatusFilterComparison', graphql_name='status')
     subscription_id = sgqlc.types.Field(StringFieldComparison, graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field(DateFieldComparison, graphql_name='trialEndDate')
 
 
 class SubscriptionPriceFilterPriceFilter(sgqlc.types.Input):
@@ -3008,15 +2881,15 @@
     h3 = sgqlc.types.Field(FontVariantInput, graphql_name='h3')
 
 
 class UpdateAccountInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('display_name', 'id', 'subscription_billing_anchor', 'subscription_proration_behavior', 'timezone')
     display_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='displayName')
-    id = sgqlc.types.Field(String, graphql_name='id')
+    id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
     subscription_billing_anchor = sgqlc.types.Field(BillingAnchor, graphql_name='subscriptionBillingAnchor')
     subscription_proration_behavior = sgqlc.types.Field(ProrationBehavior, graphql_name='subscriptionProrationBehavior')
     timezone = sgqlc.types.Field(String, graphql_name='timezone')
 
 
 class UpdateCouponInput(sgqlc.types.Input):
     __schema__ = schema
@@ -3181,18 +3054,17 @@
     reset_period = sgqlc.types.Field(EntitlementResetPeriod, graphql_name='resetPeriod')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
     weekly_reset_period_configuration = sgqlc.types.Field('WeeklyResetPeriodConfigInput', graphql_name='weeklyResetPeriodConfiguration')
 
 
 class UpdateSubscriptionInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('additional_meta_data', 'addons', 'billable_features', 'billing_period', 'environment_id', 'promotion_code', 'ref_id', 'subscription_entitlements', 'subscription_id', 'trial_end_date', 'unit_quantity')
+    __field_names__ = ('additional_meta_data', 'addons', 'billing_period', 'environment_id', 'promotion_code', 'ref_id', 'subscription_entitlements', 'subscription_id', 'trial_end_date', 'unit_quantity')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     addons = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(SubscriptionAddonInput)), graphql_name='addons')
-    billable_features = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(BillableFeatureInput)), graphql_name='billableFeatures')
     billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     promotion_code = sgqlc.types.Field(String, graphql_name='promotionCode')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     subscription_entitlements = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(UpdateSubscriptionEntitlementInput)), graphql_name='subscriptionEntitlements')
     subscription_id = sgqlc.types.Field(String, graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field(DateTime, graphql_name='trialEndDate')
@@ -3202,39 +3074,14 @@
 class UpdateUserInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('department', 'name')
     department = sgqlc.types.Field(Department, graphql_name='department')
     name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='name')
 
 
-class UsageEventReportInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('customer_id', 'dimensions', 'event_name', 'idempotency_key', 'resource_id', 'timestamp')
-    customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
-    dimensions = sgqlc.types.Field(JSON, graphql_name='dimensions')
-    event_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='eventName')
-    idempotency_key = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='idempotencyKey')
-    resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
-    timestamp = sgqlc.types.Field(DateTime, graphql_name='timestamp')
-
-
-class UsageEventsInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('environment_id', 'filters')
-    environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
-    filters = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(MeterFilterDefinitionInput))), graphql_name='filters')
-
-
-class UsageEventsReportInput(sgqlc.types.Input):
-    __schema__ = schema
-    __field_names__ = ('environment_id', 'usage_events')
-    environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
-    usage_events = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(UsageEventReportInput))), graphql_name='usageEvents')
-
-
 class UsageHistoryInput(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('customer_ref_id', 'end_date', 'environment_id', 'feature_ref_id', 'monthly_reset_period_configuration', 'reset_period', 'resource_ref_id', 'start_date', 'weekly_reset_period_configuration')
     customer_ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerRefId')
     end_date = sgqlc.types.Field(DateTime, graphql_name='endDate')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     feature_ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='featureRefId')
@@ -3267,23 +3114,22 @@
     feature = sgqlc.types.Field('UsageMeasurementFilterFeatureFilter', graphql_name='feature')
     id = sgqlc.types.Field(StringFieldComparison, graphql_name='id')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('UsageMeasurementFilter')), graphql_name='or')
 
 
 class UsageMeasurementFilterCustomerFilter(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
+    __field_names__ = ('and_', 'billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'or_', 'ref_id', 'updated_at')
     and_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('UsageMeasurementFilterCustomerFilter')), graphql_name='and')
     billing_id = sgqlc.types.Field(StringFieldComparison, graphql_name='billingId')
     created_at = sgqlc.types.Field(DateFieldComparison, graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field(StringFieldComparison, graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field(StringFieldComparison, graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field(StringFieldComparison, graphql_name='crmId')
     customer_id = sgqlc.types.Field(StringFieldComparison, graphql_name='customerId')
-    deleted_at = sgqlc.types.Field(DateFieldComparison, graphql_name='deletedAt')
     email = sgqlc.types.Field(StringFieldComparison, graphql_name='email')
     environment_id = sgqlc.types.Field(StringFieldComparison, graphql_name='environmentId')
     id = sgqlc.types.Field(StringFieldComparison, graphql_name='id')
     name = sgqlc.types.Field(StringFieldComparison, graphql_name='name')
     or_ = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('UsageMeasurementFilterCustomerFilter')), graphql_name='or')
     ref_id = sgqlc.types.Field(StringFieldComparison, graphql_name='refId')
     updated_at = sgqlc.types.Field(DateFieldComparison, graphql_name='updatedAt')
@@ -3411,15 +3257,15 @@
     )
     pricing_type = sgqlc.types.Field(PricingType, graphql_name='pricingType')
     product = sgqlc.types.Field('Product', graphql_name='product')
     product_id = sgqlc.types.Field(String, graphql_name='productId')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
     status = sgqlc.types.Field(sgqlc.types.non_null(PackageStatus), graphql_name='status')
     sync_states = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SyncState')), graphql_name='syncStates')
-    type = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='type')
+    type = sgqlc.types.Field(String, graphql_name='type')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
     version_number = sgqlc.types.Field(sgqlc.types.non_null(Int), graphql_name='versionNumber')
 
 
 class AddonAggregateGroupBy(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('billing_id', 'created_at', 'description', 'display_name', 'environment_id', 'id', 'is_latest', 'pricing_type', 'product_id', 'ref_id', 'status', 'updated_at', 'version_number')
@@ -3540,27 +3386,14 @@
 
 class AddonSumAggregate(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('version_number',)
     version_number = sgqlc.types.Field(Float, graphql_name='versionNumber')
 
 
-class AggregatedEventsByCustomer(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('aggregated_usage',)
-    aggregated_usage = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('CustomerAggregatedUsage'))), graphql_name='aggregatedUsage')
-
-
-class Aggregation(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('field', 'function')
-    field = sgqlc.types.Field(String, graphql_name='field')
-    function = sgqlc.types.Field(sgqlc.types.non_null(AggregationFunction), graphql_name='function')
-
-
 class ApiKey(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('id', 'key_type', 'token')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
     key_type = sgqlc.types.Field(sgqlc.types.non_null(ApiKeyType), graphql_name='keyType')
     token = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='token')
 
@@ -3581,21 +3414,14 @@
     __schema__ = schema
     __field_names__ = ('after', 'before', 'change_type')
     after = sgqlc.types.Field(Addon, graphql_name='after')
     before = sgqlc.types.Field(Addon, graphql_name='before')
     change_type = sgqlc.types.Field(ChangeType, graphql_name='changeType')
 
 
-class BillableFeature(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('feature_id', 'quantity')
-    feature_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='featureId')
-    quantity = sgqlc.types.Field(sgqlc.types.non_null(Float), graphql_name='quantity')
-
-
 class BillingPeriodChangeVariables(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('billing_period',)
     billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
 
 
 class CannotDeleteCustomerError(sgqlc.types.Type):
@@ -3610,14 +3436,22 @@
     __schema__ = schema
     __field_names__ = ('code', 'is_validation_error', 'ref_id')
     code = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='code')
     is_validation_error = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isValidationError')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
 
 
+class Checkout(sgqlc.types.Type):
+    __schema__ = schema
+    __field_names__ = ('checkout_billing_id', 'checkout_url', 'id')
+    checkout_billing_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='checkoutBillingId')
+    checkout_url = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='checkoutUrl')
+    id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
+
+
 class Coupon(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('additional_meta_data', 'billing_id', 'billing_link_url', 'created_at', 'customers', 'description', 'discount_value', 'environment', 'environment_id', 'id', 'name', 'ref_id', 'status', 'sync_states', 'type', 'updated_at')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     billing_link_url = sgqlc.types.Field(String, graphql_name='billingLinkUrl')
     created_at = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='createdAt')
@@ -3724,15 +3558,15 @@
     __schema__ = schema
     __field_names__ = ('id',)
     id = sgqlc.types.Field(Float, graphql_name='id')
 
 
 class Customer(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('additional_meta_data', 'billing_currency', 'billing_id', 'billing_link_url', 'coupon', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'default_payment_expiration_month', 'default_payment_expiration_year', 'default_payment_method_id', 'default_payment_method_last4_digits', 'default_payment_method_type', 'deleted_at', 'eligible_for_trial', 'email', 'environment', 'environment_id', 'exclude_from_experiment', 'experiment', 'experiment_info', 'has_active_resource', 'has_active_subscription', 'has_payment_method', 'id', 'name', 'promotional_entitlements', 'ref_id', 'subscriptions', 'sync_states', 'total_active_subscription', 'trialed_plans', 'updated_at')
+    __field_names__ = ('additional_meta_data', 'billing_currency', 'billing_id', 'billing_link_url', 'coupon', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'default_payment_expiration_month', 'default_payment_expiration_year', 'default_payment_method_id', 'default_payment_method_last4_digits', 'default_payment_method_type', 'eligible_for_trial', 'email', 'environment', 'environment_id', 'exclude_from_experiment', 'experiment', 'experiment_info', 'has_active_resource', 'has_active_subscription', 'has_payment_method', 'id', 'name', 'promotional_entitlements', 'ref_id', 'subscriptions', 'sync_states', 'total_active_subscription', 'trialed_plans', 'updated_at')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     billing_currency = sgqlc.types.Field(Currency, graphql_name='billingCurrency')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     billing_link_url = sgqlc.types.Field(String, graphql_name='billingLinkUrl')
     coupon = sgqlc.types.Field(Coupon, graphql_name='coupon')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field(String, graphql_name='crmHubspotCompanyId')
@@ -3740,15 +3574,14 @@
     crm_id = sgqlc.types.Field(String, graphql_name='crmId')
     customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
     default_payment_expiration_month = sgqlc.types.Field(Int, graphql_name='defaultPaymentExpirationMonth')
     default_payment_expiration_year = sgqlc.types.Field(Int, graphql_name='defaultPaymentExpirationYear')
     default_payment_method_id = sgqlc.types.Field(String, graphql_name='defaultPaymentMethodId')
     default_payment_method_last4_digits = sgqlc.types.Field(String, graphql_name='defaultPaymentMethodLast4Digits')
     default_payment_method_type = sgqlc.types.Field(PaymentMethodType, graphql_name='defaultPaymentMethodType')
-    deleted_at = sgqlc.types.Field(DateTime, graphql_name='deletedAt')
     eligible_for_trial = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('EligibleForTrial')), graphql_name='eligibleForTrial')
     email = sgqlc.types.Field(String, graphql_name='email')
     environment = sgqlc.types.Field('Environment', graphql_name='environment')
     environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
     exclude_from_experiment = sgqlc.types.Field(Boolean, graphql_name='excludeFromExperiment')
     experiment = sgqlc.types.Field('Experiment', graphql_name='experiment')
     experiment_info = sgqlc.types.Field('experimentInfo', graphql_name='experimentInfo')
@@ -3772,55 +3605,46 @@
     total_active_subscription = sgqlc.types.Field(sgqlc.types.non_null(Float), graphql_name='totalActiveSubscription')
     trialed_plans = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('TrialedPlan')), graphql_name='trialedPlans')
     updated_at = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='updatedAt')
 
 
 class CustomerAggregateGroupBy(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'ref_id', 'updated_at')
+    __field_names__ = ('billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'ref_id', 'updated_at')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field(String, graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field(String, graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field(String, graphql_name='crmId')
     customer_id = sgqlc.types.Field(String, graphql_name='customerId')
-    deleted_at = sgqlc.types.Field(DateTime, graphql_name='deletedAt')
     email = sgqlc.types.Field(String, graphql_name='email')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     id = sgqlc.types.Field(String, graphql_name='id')
     name = sgqlc.types.Field(String, graphql_name='name')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
 
 
-class CustomerAggregatedUsage(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('customer_id', 'usage')
-    customer_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='customerId')
-    usage = sgqlc.types.Field(sgqlc.types.non_null(Float), graphql_name='usage')
-
-
 class CustomerConnection(sgqlc.types.relay.Connection):
     __schema__ = schema
     __field_names__ = ('edges', 'page_info', 'total_count')
     edges = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('CustomerEdge'))), graphql_name='edges')
     page_info = sgqlc.types.Field(sgqlc.types.non_null('PageInfo'), graphql_name='pageInfo')
     total_count = sgqlc.types.Field(sgqlc.types.non_null(Int), graphql_name='totalCount')
 
 
 class CustomerCountAggregate(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'ref_id', 'updated_at')
+    __field_names__ = ('billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'ref_id', 'updated_at')
     billing_id = sgqlc.types.Field(Int, graphql_name='billingId')
     created_at = sgqlc.types.Field(Int, graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field(Int, graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field(Int, graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field(Int, graphql_name='crmId')
     customer_id = sgqlc.types.Field(Int, graphql_name='customerId')
-    deleted_at = sgqlc.types.Field(Int, graphql_name='deletedAt')
     email = sgqlc.types.Field(Int, graphql_name='email')
     environment_id = sgqlc.types.Field(Int, graphql_name='environmentId')
     id = sgqlc.types.Field(Int, graphql_name='id')
     name = sgqlc.types.Field(Int, graphql_name='name')
     ref_id = sgqlc.types.Field(Int, graphql_name='refId')
     updated_at = sgqlc.types.Field(Int, graphql_name='updatedAt')
 
@@ -3830,40 +3654,38 @@
     __field_names__ = ('cursor', 'node')
     cursor = sgqlc.types.Field(sgqlc.types.non_null(ConnectionCursor), graphql_name='cursor')
     node = sgqlc.types.Field(sgqlc.types.non_null(Customer), graphql_name='node')
 
 
 class CustomerMaxAggregate(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'ref_id', 'updated_at')
+    __field_names__ = ('billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'ref_id', 'updated_at')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field(String, graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field(String, graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field(String, graphql_name='crmId')
     customer_id = sgqlc.types.Field(String, graphql_name='customerId')
-    deleted_at = sgqlc.types.Field(DateTime, graphql_name='deletedAt')
     email = sgqlc.types.Field(String, graphql_name='email')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     id = sgqlc.types.Field(String, graphql_name='id')
     name = sgqlc.types.Field(String, graphql_name='name')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
 
 
 class CustomerMinAggregate(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'deleted_at', 'email', 'environment_id', 'id', 'name', 'ref_id', 'updated_at')
+    __field_names__ = ('billing_id', 'created_at', 'crm_hubspot_company_id', 'crm_hubspot_company_url', 'crm_id', 'customer_id', 'email', 'environment_id', 'id', 'name', 'ref_id', 'updated_at')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     crm_hubspot_company_id = sgqlc.types.Field(String, graphql_name='crmHubspotCompanyId')
     crm_hubspot_company_url = sgqlc.types.Field(String, graphql_name='crmHubspotCompanyUrl')
     crm_id = sgqlc.types.Field(String, graphql_name='crmId')
     customer_id = sgqlc.types.Field(String, graphql_name='customerId')
-    deleted_at = sgqlc.types.Field(DateTime, graphql_name='deletedAt')
     email = sgqlc.types.Field(String, graphql_name='email')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     id = sgqlc.types.Field(String, graphql_name='id')
     name = sgqlc.types.Field(String, graphql_name='name')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
 
@@ -3937,23 +3759,21 @@
     custom_css = sgqlc.types.Field(String, graphql_name='customCss')
     palette = sgqlc.types.Field(CustomerPortalColorsPalette, graphql_name='palette')
     typography = sgqlc.types.Field('TypographyConfiguration', graphql_name='typography')
 
 
 class CustomerPortalPricingFeature(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('description', 'display_name', 'feature_type', 'feature_units', 'feature_units_plural', 'id', 'meter_type', 'ref_id')
+    __field_names__ = ('description', 'display_name', 'feature_type', 'feature_units', 'feature_units_plural', 'meter_type')
     description = sgqlc.types.Field(String, graphql_name='description')
     display_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='displayName')
     feature_type = sgqlc.types.Field(sgqlc.types.non_null(FeatureType), graphql_name='featureType')
     feature_units = sgqlc.types.Field(String, graphql_name='featureUnits')
     feature_units_plural = sgqlc.types.Field(String, graphql_name='featureUnitsPlural')
-    id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
     meter_type = sgqlc.types.Field(MeterType, graphql_name='meterType')
-    ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
 
 
 class CustomerPortalPromotionalEntitlement(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('description', 'display_name', 'end_date', 'has_unlimited_usage', 'period', 'start_date', 'usage_limit')
     description = sgqlc.types.Field(String, graphql_name='description')
     display_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='displayName')
@@ -3962,37 +3782,26 @@
     period = sgqlc.types.Field(sgqlc.types.non_null(PromotionalEntitlementPeriod), graphql_name='period')
     start_date = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='startDate')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
 
 
 class CustomerPortalSubscription(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('addons', 'billing_period_range', 'plan_name', 'prices', 'pricing', 'pricing_type', 'scheduled_updates', 'status', 'subscription_id', 'total_price', 'trial_remaining_days')
+    __field_names__ = ('addons', 'billing_period_range', 'plan_name', 'pricing', 'scheduled_updates', 'status', 'subscription_id', 'total_price', 'trial_remaining_days')
     addons = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(CustomerPortalAddon))), graphql_name='addons')
     billing_period_range = sgqlc.types.Field('DateRange', graphql_name='billingPeriodRange')
     plan_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='planName')
-    prices = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('CustomerPortalSubscriptionPrice'))), graphql_name='prices')
     pricing = sgqlc.types.Field(sgqlc.types.non_null('CustomerPortalSubscriptionPricing'), graphql_name='pricing')
-    pricing_type = sgqlc.types.Field(sgqlc.types.non_null(PricingType), graphql_name='pricingType')
     scheduled_updates = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SubscriptionScheduledUpdate')), graphql_name='scheduledUpdates')
     status = sgqlc.types.Field(sgqlc.types.non_null(SubscriptionStatus), graphql_name='status')
     subscription_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='subscriptionId')
     total_price = sgqlc.types.Field('CustomerSubscriptionTotalPrice', graphql_name='totalPrice')
     trial_remaining_days = sgqlc.types.Field(Int, graphql_name='trialRemainingDays')
 
 
-class CustomerPortalSubscriptionPrice(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('billing_model', 'billing_period', 'feature', 'price')
-    billing_model = sgqlc.types.Field(BillingModel, graphql_name='billingModel')
-    billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
-    feature = sgqlc.types.Field(CustomerPortalPricingFeature, graphql_name='feature')
-    price = sgqlc.types.Field('Money', graphql_name='price')
-
-
 class CustomerPortalSubscriptionPricing(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('billing_country_code', 'billing_model', 'billing_period', 'feature', 'price', 'pricing_type', 'unit_quantity', 'usage_based_estimated_bill')
     billing_country_code = sgqlc.types.Field(String, graphql_name='billingCountryCode')
     billing_model = sgqlc.types.Field(BillingModel, graphql_name='billingModel')
     billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
     feature = sgqlc.types.Field(CustomerPortalPricingFeature, graphql_name='feature')
@@ -4115,29 +3924,28 @@
     total_price = sgqlc.types.Field('CustomerSubscriptionTotalPrice', graphql_name='totalPrice')
     trial_end_date = sgqlc.types.Field(DateTime, graphql_name='trialEndDate')
     was_in_trial = sgqlc.types.Field(Boolean, graphql_name='wasInTrial')
 
 
 class CustomerSubscriptionAggregateGroupBy(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'pricing_type', 'ref_id', 'resource_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     cancel_reason = sgqlc.types.Field(SubscriptionCancelReason, graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field(DateTime, graphql_name='cancellationDate')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     crm_id = sgqlc.types.Field(String, graphql_name='crmId')
     crm_link_url = sgqlc.types.Field(String, graphql_name='crmLinkUrl')
     effective_end_date = sgqlc.types.Field(DateTime, graphql_name='effectiveEndDate')
     end_date = sgqlc.types.Field(DateTime, graphql_name='endDate')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     id = sgqlc.types.Field(String, graphql_name='id')
     old_billing_id = sgqlc.types.Field(String, graphql_name='oldBillingId')
     pricing_type = sgqlc.types.Field(PricingType, graphql_name='pricingType')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
-    resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     start_date = sgqlc.types.Field(DateTime, graphql_name='startDate')
     status = sgqlc.types.Field(SubscriptionStatus, graphql_name='status')
     subscription_id = sgqlc.types.Field(String, graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field(DateTime, graphql_name='trialEndDate')
 
 
 class CustomerSubscriptionConnection(sgqlc.types.relay.Connection):
@@ -4146,29 +3954,28 @@
     edges = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('CustomerSubscriptionEdge'))), graphql_name='edges')
     page_info = sgqlc.types.Field(sgqlc.types.non_null('PageInfo'), graphql_name='pageInfo')
     total_count = sgqlc.types.Field(sgqlc.types.non_null(Int), graphql_name='totalCount')
 
 
 class CustomerSubscriptionCountAggregate(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'pricing_type', 'ref_id', 'resource_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
     billing_id = sgqlc.types.Field(Int, graphql_name='billingId')
     cancel_reason = sgqlc.types.Field(Int, graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field(Int, graphql_name='cancellationDate')
     created_at = sgqlc.types.Field(Int, graphql_name='createdAt')
     crm_id = sgqlc.types.Field(Int, graphql_name='crmId')
     crm_link_url = sgqlc.types.Field(Int, graphql_name='crmLinkUrl')
     effective_end_date = sgqlc.types.Field(Int, graphql_name='effectiveEndDate')
     end_date = sgqlc.types.Field(Int, graphql_name='endDate')
     environment_id = sgqlc.types.Field(Int, graphql_name='environmentId')
     id = sgqlc.types.Field(Int, graphql_name='id')
     old_billing_id = sgqlc.types.Field(Int, graphql_name='oldBillingId')
     pricing_type = sgqlc.types.Field(Int, graphql_name='pricingType')
     ref_id = sgqlc.types.Field(Int, graphql_name='refId')
-    resource_id = sgqlc.types.Field(Int, graphql_name='resourceId')
     start_date = sgqlc.types.Field(Int, graphql_name='startDate')
     status = sgqlc.types.Field(Int, graphql_name='status')
     subscription_id = sgqlc.types.Field(Int, graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field(Int, graphql_name='trialEndDate')
 
 
 class CustomerSubscriptionEdge(sgqlc.types.Type):
@@ -4176,52 +3983,50 @@
     __field_names__ = ('cursor', 'node')
     cursor = sgqlc.types.Field(sgqlc.types.non_null(ConnectionCursor), graphql_name='cursor')
     node = sgqlc.types.Field(sgqlc.types.non_null(CustomerSubscription), graphql_name='node')
 
 
 class CustomerSubscriptionMaxAggregate(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'pricing_type', 'ref_id', 'resource_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     cancel_reason = sgqlc.types.Field(SubscriptionCancelReason, graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field(DateTime, graphql_name='cancellationDate')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     crm_id = sgqlc.types.Field(String, graphql_name='crmId')
     crm_link_url = sgqlc.types.Field(String, graphql_name='crmLinkUrl')
     effective_end_date = sgqlc.types.Field(DateTime, graphql_name='effectiveEndDate')
     end_date = sgqlc.types.Field(DateTime, graphql_name='endDate')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     id = sgqlc.types.Field(String, graphql_name='id')
     old_billing_id = sgqlc.types.Field(String, graphql_name='oldBillingId')
     pricing_type = sgqlc.types.Field(PricingType, graphql_name='pricingType')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
-    resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     start_date = sgqlc.types.Field(DateTime, graphql_name='startDate')
     status = sgqlc.types.Field(SubscriptionStatus, graphql_name='status')
     subscription_id = sgqlc.types.Field(String, graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field(DateTime, graphql_name='trialEndDate')
 
 
 class CustomerSubscriptionMinAggregate(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'pricing_type', 'ref_id', 'resource_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
+    __field_names__ = ('billing_id', 'cancel_reason', 'cancellation_date', 'created_at', 'crm_id', 'crm_link_url', 'effective_end_date', 'end_date', 'environment_id', 'id', 'old_billing_id', 'pricing_type', 'ref_id', 'start_date', 'status', 'subscription_id', 'trial_end_date')
     billing_id = sgqlc.types.Field(String, graphql_name='billingId')
     cancel_reason = sgqlc.types.Field(SubscriptionCancelReason, graphql_name='cancelReason')
     cancellation_date = sgqlc.types.Field(DateTime, graphql_name='cancellationDate')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     crm_id = sgqlc.types.Field(String, graphql_name='crmId')
     crm_link_url = sgqlc.types.Field(String, graphql_name='crmLinkUrl')
     effective_end_date = sgqlc.types.Field(DateTime, graphql_name='effectiveEndDate')
     end_date = sgqlc.types.Field(DateTime, graphql_name='endDate')
     environment_id = sgqlc.types.Field(String, graphql_name='environmentId')
     id = sgqlc.types.Field(String, graphql_name='id')
     old_billing_id = sgqlc.types.Field(String, graphql_name='oldBillingId')
     pricing_type = sgqlc.types.Field(PricingType, graphql_name='pricingType')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
-    resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     start_date = sgqlc.types.Field(DateTime, graphql_name='startDate')
     status = sgqlc.types.Field(SubscriptionStatus, graphql_name='status')
     subscription_id = sgqlc.types.Field(String, graphql_name='subscriptionId')
     trial_end_date = sgqlc.types.Field(DateTime, graphql_name='trialEndDate')
 
 
 class CustomerSubscriptionTotalPrice(sgqlc.types.Type):
@@ -4252,17 +4057,16 @@
     after = sgqlc.types.Field(DefaultTrialConfig, graphql_name='after')
     before = sgqlc.types.Field(DefaultTrialConfig, graphql_name='before')
     change_type = sgqlc.types.Field(ChangeType, graphql_name='changeType')
 
 
 class DowngradeChangeVariables(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('addon_ref_ids', 'billable_features', 'billing_period', 'downgrade_plan_ref_id')
+    __field_names__ = ('addon_ref_ids', 'billing_period', 'downgrade_plan_ref_id')
     addon_ref_ids = sgqlc.types.Field(String, graphql_name='addonRefIds')
-    billable_features = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(BillableFeature)), graphql_name='billableFeatures')
     billing_period = sgqlc.types.Field(BillingPeriod, graphql_name='billingPeriod')
     downgrade_plan_ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='downgradePlanRefId')
 
 
 class DuplicatedEntityNotAllowedError(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('code', 'entity_name', 'identifier', 'is_validation_error')
@@ -4285,25 +4089,24 @@
     eligible = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='eligible')
     product_id = sgqlc.types.Field(String, graphql_name='productId')
     product_ref_id = sgqlc.types.Field(String, graphql_name='productRefId')
 
 
 class Entitlement(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('access_denied_reason', 'current_usage', 'customer_id', 'display_name_override', 'entitlement_updated_at', 'feature', 'has_unlimited_usage', 'hidden_from_widgets', 'is_granted', 'meter_id', 'next_reset_date', 'requested_usage', 'reset_period', 'reset_period_configuration', 'resource_id', 'usage_limit', 'usage_updated_at')
+    __field_names__ = ('access_denied_reason', 'current_usage', 'customer_id', 'display_name_override', 'entitlement_updated_at', 'feature', 'has_unlimited_usage', 'hidden_from_widgets', 'is_granted', 'next_reset_date', 'requested_usage', 'reset_period', 'reset_period_configuration', 'resource_id', 'usage_limit', 'usage_updated_at')
     access_denied_reason = sgqlc.types.Field(AccessDeniedReason, graphql_name='accessDeniedReason')
     current_usage = sgqlc.types.Field(Float, graphql_name='currentUsage')
     customer_id = sgqlc.types.Field(String, graphql_name='customerId')
     display_name_override = sgqlc.types.Field(String, graphql_name='displayNameOverride')
     entitlement_updated_at = sgqlc.types.Field(DateTime, graphql_name='entitlementUpdatedAt')
     feature = sgqlc.types.Field('EntitlementFeature', graphql_name='feature')
     has_unlimited_usage = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='hasUnlimitedUsage')
     hidden_from_widgets = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(WidgetType)), graphql_name='hiddenFromWidgets')
     is_granted = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isGranted')
-    meter_id = sgqlc.types.Field(String, graphql_name='meterId')
     next_reset_date = sgqlc.types.Field(DateTime, graphql_name='nextResetDate')
     requested_usage = sgqlc.types.Field(Float, graphql_name='requestedUsage')
     reset_period = sgqlc.types.Field(EntitlementResetPeriod, graphql_name='resetPeriod')
     reset_period_configuration = sgqlc.types.Field('ResetPeriodConfiguration', graphql_name='resetPeriodConfiguration')
     resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
     usage_updated_at = sgqlc.types.Field(DateTime, graphql_name='usageUpdatedAt')
@@ -4334,25 +4137,24 @@
     plan = sgqlc.types.Field('Plan', graphql_name='plan')
     price_entitlement = sgqlc.types.Field('PriceEntitlement', graphql_name='priceEntitlement')
     subscription = sgqlc.types.Field(CustomerSubscription, graphql_name='subscription')
 
 
 class EntitlementWithSummary(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('access_denied_reason', 'current_usage', 'customer_id', 'display_name_override', 'entitlement_updated_at', 'feature', 'has_unlimited_usage', 'hidden_from_widgets', 'is_granted', 'meter_id', 'next_reset_date', 'requested_usage', 'reset_period', 'reset_period_configuration', 'resource_id', 'summaries', 'usage_limit', 'usage_updated_at')
+    __field_names__ = ('access_denied_reason', 'current_usage', 'customer_id', 'display_name_override', 'entitlement_updated_at', 'feature', 'has_unlimited_usage', 'hidden_from_widgets', 'is_granted', 'next_reset_date', 'requested_usage', 'reset_period', 'reset_period_configuration', 'resource_id', 'summaries', 'usage_limit', 'usage_updated_at')
     access_denied_reason = sgqlc.types.Field(AccessDeniedReason, graphql_name='accessDeniedReason')
     current_usage = sgqlc.types.Field(Float, graphql_name='currentUsage')
     customer_id = sgqlc.types.Field(String, graphql_name='customerId')
     display_name_override = sgqlc.types.Field(String, graphql_name='displayNameOverride')
     entitlement_updated_at = sgqlc.types.Field(DateTime, graphql_name='entitlementUpdatedAt')
     feature = sgqlc.types.Field(EntitlementFeature, graphql_name='feature')
     has_unlimited_usage = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='hasUnlimitedUsage')
     hidden_from_widgets = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(WidgetType)), graphql_name='hiddenFromWidgets')
     is_granted = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isGranted')
-    meter_id = sgqlc.types.Field(String, graphql_name='meterId')
     next_reset_date = sgqlc.types.Field(DateTime, graphql_name='nextResetDate')
     requested_usage = sgqlc.types.Field(Float, graphql_name='requestedUsage')
     reset_period = sgqlc.types.Field(EntitlementResetPeriod, graphql_name='resetPeriod')
     reset_period_configuration = sgqlc.types.Field('ResetPeriodConfiguration', graphql_name='resetPeriodConfiguration')
     resource_id = sgqlc.types.Field(String, graphql_name='resourceId')
     summaries = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(EntitlementSummary)), graphql_name='summaries')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
@@ -4622,29 +4424,27 @@
     billing_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='billingId')
     code = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='code')
     is_validation_error = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isValidationError')
 
 
 class Feature(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('account', 'additional_meta_data', 'created_at', 'description', 'display_name', 'environment', 'environment_id', 'feature_status', 'feature_type', 'feature_units', 'feature_units_plural', 'has_meter', 'id', 'meter', 'meter_type', 'ref_id', 'updated_at')
+    __field_names__ = ('account', 'additional_meta_data', 'created_at', 'description', 'display_name', 'environment', 'environment_id', 'feature_status', 'feature_type', 'feature_units', 'feature_units_plural', 'id', 'meter_type', 'ref_id', 'updated_at')
     account = sgqlc.types.Field(Account, graphql_name='account')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     description = sgqlc.types.Field(String, graphql_name='description')
     display_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='displayName')
     environment = sgqlc.types.Field(Environment, graphql_name='environment')
     environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
     feature_status = sgqlc.types.Field(sgqlc.types.non_null(FeatureStatus), graphql_name='featureStatus')
     feature_type = sgqlc.types.Field(sgqlc.types.non_null(FeatureType), graphql_name='featureType')
     feature_units = sgqlc.types.Field(String, graphql_name='featureUnits')
     feature_units_plural = sgqlc.types.Field(String, graphql_name='featureUnitsPlural')
-    has_meter = sgqlc.types.Field(Boolean, graphql_name='hasMeter')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
-    meter = sgqlc.types.Field('Meter', graphql_name='meter')
     meter_type = sgqlc.types.Field(MeterType, graphql_name='meterType')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
     updated_at = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='updatedAt')
 
 
 class FeatureAggregateGroupBy(sgqlc.types.Type):
     __schema__ = schema
@@ -5046,14 +4846,22 @@
 class InvalidSubscriptionStatus(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('code', 'is_validation_error')
     code = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='code')
     is_validation_error = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isValidationError')
 
 
+class InvalidUsageValueForIncrementalFeatureError(sgqlc.types.Type):
+    __schema__ = schema
+    __field_names__ = ('code', 'is_validation_error', 'usage_value')
+    code = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='code')
+    is_validation_error = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isValidationError')
+    usage_value = sgqlc.types.Field(sgqlc.types.non_null(Float), graphql_name='usageValue')
+
+
 class Member(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('account', 'created_at', 'cubejs_token', 'email', 'hide_getting_started_page', 'id', 'member_status', 'service_api_key', 'user')
     account = sgqlc.types.Field(sgqlc.types.non_null(Account), graphql_name='account')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     cubejs_token = sgqlc.types.Field(String, graphql_name='cubejsToken')
     email = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='email')
@@ -5124,39 +4932,14 @@
     __schema__ = schema
     __field_names__ = ('failed_invites', 'skipped_invites', 'success_invites')
     failed_invites = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(String))), graphql_name='failedInvites')
     skipped_invites = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(String))), graphql_name='skippedInvites')
     success_invites = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(String))), graphql_name='successInvites')
 
 
-class Meter(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('aggregation', 'created_at', 'environment_id', 'filters', 'id', 'updated_at')
-    aggregation = sgqlc.types.Field(sgqlc.types.non_null(Aggregation), graphql_name='aggregation')
-    created_at = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='createdAt')
-    environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
-    filters = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('MeterFilterDefinition'))), graphql_name='filters')
-    id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
-    updated_at = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='updatedAt')
-
-
-class MeterCondition(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('field', 'operation', 'value')
-    field = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='field')
-    operation = sgqlc.types.Field(sgqlc.types.non_null(ConditionOperation), graphql_name='operation')
-    value = sgqlc.types.Field(String, graphql_name='value')
-
-
-class MeterFilterDefinition(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('conditions',)
-    conditions = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(MeterCondition))), graphql_name='conditions')
-
-
 class MeteringNotAvailableForFeatureTypeError(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('code', 'feature_type', 'is_validation_error')
     code = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='code')
     feature_type = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='featureType')
     is_validation_error = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isValidationError')
 
@@ -5179,23 +4962,19 @@
     __schema__ = schema
     __field_names__ = ('monthly_according_to',)
     monthly_according_to = sgqlc.types.Field(MonthlyAccordingTo, graphql_name='monthlyAccordingTo')
 
 
 class Mutation(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('add_compatible_addons_to_plan', 'archive_customer', 'archive_one_coupon', 'archive_plan', 'attach_customer_payment_method', 'cancel_schedule', 'cancel_subscription', 'create_account', 'create_addon_draft', 'create_feature', 'create_many_package_entitlements', 'create_many_promotional_entitlements', 'create_one_addon', 'create_one_coupon', 'create_one_customer', 'create_one_environment', 'create_one_experiment', 'create_one_feature', 'create_one_hook', 'create_one_integration', 'create_one_plan', 'create_one_product', 'create_plan_draft', 'create_subscription', 'create_usage_measurement', 'delete_environment', 'delete_feature', 'delete_one_addon', 'delete_one_environment', 'delete_one_feature', 'delete_one_hook', 'delete_one_integration', 'delete_one_package_entitlement', 'delete_one_price', 'delete_one_product', 'delete_one_promotional_entitlement', 'estimate_subscription', 'estimate_subscription_update', 'hide_getting_started_page', 'import_customers_bulk', 'import_one_customer', 'import_subscriptions_bulk', 'init_add_stripe_customer_payment_method', 'invite_members', 'migrate_subscription_to_latest', 'provision_customer', 'provision_sandbox', 'provision_subscription', 'provision_subscription_v2', 'publish_addon', 'publish_plan', 'purge_customer_cache', 'recalculate_entitlements', 'register_member', 'remove_addon_draft', 'remove_base_plan_from_plan', 'remove_compatible_addons_from_plan', 'remove_coupon_from_customer', 'remove_coupon_from_customer_subscription', 'remove_experiment_from_customer', 'remove_experiment_from_customer_subscription', 'remove_member', 'remove_plan_draft', 'report_entitlement_check_requested', 'report_event', 'report_usage', 'resend_email_verification', 'resync_integration', 'set_base_plan_on_plan', 'set_compatible_addons_on_plan', 'set_coupon_on_customer', 'set_coupon_on_customer_subscription', 'set_experiment_on_customer', 'set_experiment_on_customer_subscription', 'set_package_pricing', 'set_widget_configuration', 'start_experiment', 'stop_experiment', 'trigger_import_catalog', 'trigger_import_customers', 'update_account', 'update_entitlements_order', 'update_feature', 'update_one_addon', 'update_one_coupon', 'update_one_customer', 'update_one_environment', 'update_one_experiment', 'update_one_feature', 'update_one_hook', 'update_one_integration', 'update_one_package_entitlement', 'update_one_plan', 'update_one_product', 'update_one_promotional_entitlement', 'update_one_subscription', 'update_user')
+    __field_names__ = ('add_compatible_addons_to_plan', 'archive_one_coupon', 'archive_plan', 'attach_customer_payment_method', 'cancel_schedule', 'cancel_subscription', 'create_account', 'create_addon_draft', 'create_feature', 'create_many_package_entitlements', 'create_many_promotional_entitlements', 'create_one_addon', 'create_one_coupon', 'create_one_customer', 'create_one_environment', 'create_one_experiment', 'create_one_feature', 'create_one_hook', 'create_one_integration', 'create_one_plan', 'create_one_product', 'create_plan_draft', 'create_subscription', 'create_usage_measurement', 'delete_environment', 'delete_feature', 'delete_one_addon', 'delete_one_customer', 'delete_one_environment', 'delete_one_feature', 'delete_one_hook', 'delete_one_integration', 'delete_one_package_entitlement', 'delete_one_price', 'delete_one_product', 'delete_one_promotional_entitlement', 'estimate_subscription', 'estimate_subscription_update', 'hide_getting_started_page', 'import_customers_bulk', 'import_one_customer', 'import_subscriptions_bulk', 'init_add_stripe_customer_payment_method', 'initiate_checkout', 'invite_members', 'migrate_subscription_to_latest', 'provision_customer', 'provision_sandbox', 'provision_subscription', 'provision_subscription_v2', 'publish_addon', 'publish_plan', 'purge_customer_cache', 'register_member', 'remove_addon_draft', 'remove_base_plan_from_plan', 'remove_compatible_addons_from_plan', 'remove_coupon_from_customer', 'remove_coupon_from_customer_subscription', 'remove_experiment_from_customer', 'remove_experiment_from_customer_subscription', 'remove_member', 'remove_plan_draft', 'report_entitlement_check_requested', 'resend_email_verification', 'resync_integration', 'set_base_plan_on_plan', 'set_compatible_addons_on_plan', 'set_coupon_on_customer', 'set_coupon_on_customer_subscription', 'set_experiment_on_customer', 'set_experiment_on_customer_subscription', 'set_package_pricing', 'set_widget_configuration', 'start_experiment', 'stop_experiment', 'trigger_import_catalog', 'trigger_import_customers', 'update_account', 'update_entitlements_order', 'update_feature', 'update_one_addon', 'update_one_coupon', 'update_one_customer', 'update_one_environment', 'update_one_experiment', 'update_one_feature', 'update_one_hook', 'update_one_integration', 'update_one_package_entitlement', 'update_one_plan', 'update_one_product', 'update_one_promotional_entitlement', 'update_one_subscription', 'update_user')
     add_compatible_addons_to_plan = sgqlc.types.Field(sgqlc.types.non_null('Plan'), graphql_name='addCompatibleAddonsToPlan', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(AddCompatibleAddonsToPlanInput), graphql_name='input', default=None)),
 ))
     )
-    archive_customer = sgqlc.types.Field(sgqlc.types.non_null(Customer), graphql_name='archiveCustomer', args=sgqlc.types.ArgDict((
-        ('input', sgqlc.types.Arg(sgqlc.types.non_null(ArchiveCustomerInput), graphql_name='input', default=None)),
-))
-    )
     archive_one_coupon = sgqlc.types.Field(sgqlc.types.non_null(Coupon), graphql_name='archiveOneCoupon', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(ArchiveCouponInput), graphql_name='input', default=None)),
 ))
     )
     archive_plan = sgqlc.types.Field(sgqlc.types.non_null('Plan'), graphql_name='archivePlan', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(ArchivePlanInput), graphql_name='input', default=None)),
 ))
@@ -5292,14 +5071,18 @@
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(DeleteFeatureInput), graphql_name='input', default=None)),
 ))
     )
     delete_one_addon = sgqlc.types.Field(sgqlc.types.non_null(AddonDeleteResponse), graphql_name='deleteOneAddon', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(DeleteOneAddonInput), graphql_name='input', default=None)),
 ))
     )
+    delete_one_customer = sgqlc.types.Field(sgqlc.types.non_null(Customer), graphql_name='deleteOneCustomer', args=sgqlc.types.ArgDict((
+        ('input', sgqlc.types.Arg(sgqlc.types.non_null(DeleteCustomerInput), graphql_name='input', default=None)),
+))
+    )
     delete_one_environment = sgqlc.types.Field(sgqlc.types.non_null(EnvironmentDeleteResponse), graphql_name='deleteOneEnvironment', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(DeleteOneEnvironmentInput), graphql_name='input', default=None)),
 ))
     )
     delete_one_feature = sgqlc.types.Field(sgqlc.types.non_null(Feature), graphql_name='deleteOneFeature', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(DeleteFeatureInput), graphql_name='input', default=None)),
 ))
@@ -5352,14 +5135,18 @@
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(ImportSubscriptionsBulk), graphql_name='input', default=None)),
 ))
     )
     init_add_stripe_customer_payment_method = sgqlc.types.Field(sgqlc.types.non_null(InitAddStripeCustomerPaymentMethod), graphql_name='initAddStripeCustomerPaymentMethod', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(InitAddStripeCustomerPaymentMethodInput), graphql_name='input', default=None)),
 ))
     )
+    initiate_checkout = sgqlc.types.Field(sgqlc.types.non_null(Checkout), graphql_name='initiateCheckout', args=sgqlc.types.ArgDict((
+        ('input', sgqlc.types.Arg(sgqlc.types.non_null(InitiateCheckoutInput), graphql_name='input', default=None)),
+))
+    )
     invite_members = sgqlc.types.Field(sgqlc.types.non_null(MembersInviteResponse), graphql_name='inviteMembers', args=sgqlc.types.ArgDict((
         ('invites', sgqlc.types.Arg(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(String))), graphql_name='invites', default=None)),
 ))
     )
     migrate_subscription_to_latest = sgqlc.types.Field(sgqlc.types.non_null(CustomerSubscription), graphql_name='migrateSubscriptionToLatest', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(SubscriptionMigrationInput), graphql_name='input', default=None)),
 ))
@@ -5388,18 +5175,14 @@
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(PackagePublishInput), graphql_name='input', default=None)),
 ))
     )
     purge_customer_cache = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='purgeCustomerCache', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(ClearCustomerPersistentCacheInput), graphql_name='input', default=None)),
 ))
     )
-    recalculate_entitlements = sgqlc.types.Field(sgqlc.types.non_null('RecalculateEntitlementsResult'), graphql_name='recalculateEntitlements', args=sgqlc.types.ArgDict((
-        ('input', sgqlc.types.Arg(sgqlc.types.non_null(RecalculateEntitlementsInput), graphql_name='input', default=None)),
-))
-    )
     register_member = sgqlc.types.Field(sgqlc.types.non_null('User'), graphql_name='registerMember')
     remove_addon_draft = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='removeAddonDraft', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(DiscardPackageDraftInput), graphql_name='input', default=None)),
 ))
     )
     remove_base_plan_from_plan = sgqlc.types.Field(sgqlc.types.non_null('Plan'), graphql_name='removeBasePlanFromPlan', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(RemoveBasePlanFromPlanInput), graphql_name='input', default=None)),
@@ -5433,22 +5216,14 @@
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(DiscardPackageDraftInput), graphql_name='input', default=None)),
 ))
     )
     report_entitlement_check_requested = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='reportEntitlementCheckRequested', args=sgqlc.types.ArgDict((
         ('entitlement_check_requested', sgqlc.types.Arg(sgqlc.types.non_null(EntitlementCheckRequested), graphql_name='entitlementCheckRequested', default=None)),
 ))
     )
-    report_event = sgqlc.types.Field(String, graphql_name='reportEvent', args=sgqlc.types.ArgDict((
-        ('events', sgqlc.types.Arg(sgqlc.types.non_null(UsageEventsReportInput), graphql_name='events', default=None)),
-))
-    )
-    report_usage = sgqlc.types.Field(sgqlc.types.non_null('UsageMeasurementWithCurrentUsage'), graphql_name='reportUsage', args=sgqlc.types.ArgDict((
-        ('input', sgqlc.types.Arg(sgqlc.types.non_null(ReportUsageInput), graphql_name='input', default=None)),
-))
-    )
     resend_email_verification = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='resendEmailVerification')
     resync_integration = sgqlc.types.Field(sgqlc.types.non_null('ResyncIntegrationResult'), graphql_name='resyncIntegration', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(ResyncIntegrationInput), graphql_name='input', default=None)),
 ))
     )
     set_base_plan_on_plan = sgqlc.types.Field(sgqlc.types.non_null('Plan'), graphql_name='setBasePlanOnPlan', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(SetBasePlanOnPlanInput), graphql_name='input', default=None)),
@@ -5608,15 +5383,15 @@
     is_latest = sgqlc.types.Field(Boolean, graphql_name='isLatest')
     prices = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('Price')), graphql_name='prices')
     pricing_type = sgqlc.types.Field(PricingType, graphql_name='pricingType')
     product_id = sgqlc.types.Field(String, graphql_name='productId')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
     status = sgqlc.types.Field(sgqlc.types.non_null(PackageStatus), graphql_name='status')
     sync_states = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('SyncState'))), graphql_name='syncStates')
-    type = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='type')
+    type = sgqlc.types.Field(String, graphql_name='type')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
     version_number = sgqlc.types.Field(sgqlc.types.non_null(Int), graphql_name='versionNumber')
 
 
 class PackageDraftDetails(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('affected_child_plans', 'changes', 'child_plans_with_draft', 'customers_affected', 'updated_at', 'updated_by', 'version')
@@ -5635,26 +5410,25 @@
     updated_at = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='updatedAt')
     updated_by = sgqlc.types.Field(String, graphql_name='updatedBy')
     version = sgqlc.types.Field(sgqlc.types.non_null(Int), graphql_name='version')
 
 
 class PackageEntitlement(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('created_at', 'description', 'display_name_override', 'environment_id', 'feature', 'feature_id', 'has_unlimited_usage', 'hidden_from_widgets', 'id', 'is_custom', 'meter', 'order', 'package', 'package_id', 'reset_period', 'reset_period_configuration', 'updated_at', 'usage_limit')
+    __field_names__ = ('created_at', 'description', 'display_name_override', 'environment_id', 'feature', 'feature_id', 'has_unlimited_usage', 'hidden_from_widgets', 'id', 'is_custom', 'order', 'package', 'package_id', 'reset_period', 'reset_period_configuration', 'updated_at', 'usage_limit')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     description = sgqlc.types.Field(String, graphql_name='description')
     display_name_override = sgqlc.types.Field(String, graphql_name='displayNameOverride')
     environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
     feature = sgqlc.types.Field(sgqlc.types.non_null(Feature), graphql_name='feature')
     feature_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='featureId')
     has_unlimited_usage = sgqlc.types.Field(Boolean, graphql_name='hasUnlimitedUsage')
     hidden_from_widgets = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(WidgetType)), graphql_name='hiddenFromWidgets')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
     is_custom = sgqlc.types.Field(Boolean, graphql_name='isCustom')
-    meter = sgqlc.types.Field(Meter, graphql_name='meter')
     order = sgqlc.types.Field(Float, graphql_name='order')
     package = sgqlc.types.Field(PackageDTO, graphql_name='package')
     package_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='packageId')
     reset_period = sgqlc.types.Field(EntitlementResetPeriod, graphql_name='resetPeriod')
     reset_period_configuration = sgqlc.types.Field('ResetPeriodConfiguration', graphql_name='resetPeriodConfiguration')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
@@ -5773,20 +5547,18 @@
     has_next_page = sgqlc.types.Field(Boolean, graphql_name='hasNextPage')
     has_previous_page = sgqlc.types.Field(Boolean, graphql_name='hasPreviousPage')
     start_cursor = sgqlc.types.Field(ConnectionCursor, graphql_name='startCursor')
 
 
 class Paywall(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('active_subscriptions', 'configuration', 'currency', 'customer', 'paywall_calculated_price_points', 'plans', 'resource')
-    active_subscriptions = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(CustomerSubscription)), graphql_name='activeSubscriptions')
+    __field_names__ = ('configuration', 'currency', 'customer', 'plans', 'resource')
     configuration = sgqlc.types.Field('PaywallConfiguration', graphql_name='configuration')
     currency = sgqlc.types.Field(sgqlc.types.non_null('PaywallCurrency'), graphql_name='currency')
     customer = sgqlc.types.Field(Customer, graphql_name='customer')
-    paywall_calculated_price_points = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('PaywallPricePoint')), graphql_name='paywallCalculatedPricePoints')
     plans = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('Plan'))), graphql_name='plans')
     resource = sgqlc.types.Field(CustomerResource, graphql_name='resource')
 
 
 class PaywallAddon(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('additional_meta_data', 'billing_id', 'description', 'display_name', 'entitlements', 'prices', 'pricing_type', 'ref_id')
@@ -5870,26 +5642,14 @@
     feature = sgqlc.types.Field(EntitlementFeature, graphql_name='feature')
     feature_id = sgqlc.types.Field(String, graphql_name='featureId')
     max_unit_quantity = sgqlc.types.Field(Float, graphql_name='maxUnitQuantity')
     min_unit_quantity = sgqlc.types.Field(Float, graphql_name='minUnitQuantity')
     price = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='price')
 
 
-class PaywallPricePoint(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('additional_charges_may_apply', 'amount', 'billing_country_code', 'billing_period', 'currency', 'feature', 'plan_id')
-    additional_charges_may_apply = sgqlc.types.Field(Boolean, graphql_name='additionalChargesMayApply')
-    amount = sgqlc.types.Field(sgqlc.types.non_null(Float), graphql_name='amount')
-    billing_country_code = sgqlc.types.Field(String, graphql_name='billingCountryCode')
-    billing_period = sgqlc.types.Field(sgqlc.types.non_null(BillingPeriod), graphql_name='billingPeriod')
-    currency = sgqlc.types.Field(sgqlc.types.non_null(Currency), graphql_name='currency')
-    feature = sgqlc.types.Field(Feature, graphql_name='feature')
-    plan_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='planId')
-
-
 class PaywallProduct(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('additional_meta_data', 'description', 'display_name', 'ref_id')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     description = sgqlc.types.Field(String, graphql_name='description')
     display_name = sgqlc.types.Field(String, graphql_name='displayName')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
@@ -5927,15 +5687,15 @@
     prices = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('Price')), graphql_name='prices')
     pricing_type = sgqlc.types.Field(PricingType, graphql_name='pricingType')
     product = sgqlc.types.Field(sgqlc.types.non_null('Product'), graphql_name='product')
     product_id = sgqlc.types.Field(String, graphql_name='productId')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
     status = sgqlc.types.Field(sgqlc.types.non_null(PackageStatus), graphql_name='status')
     sync_states = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null('SyncState')), graphql_name='syncStates')
-    type = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='type')
+    type = sgqlc.types.Field(String, graphql_name='type')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
     version_number = sgqlc.types.Field(sgqlc.types.non_null(Int), graphql_name='versionNumber')
 
 
 class PlanAggregateGroupBy(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('billing_id', 'created_at', 'description', 'display_name', 'environment_id', 'id', 'is_latest', 'pricing_type', 'product_id', 'ref_id', 'status', 'updated_at', 'version_number')
@@ -6324,26 +6084,25 @@
     __field_names__ = ('code', 'is_validation_error')
     code = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='code')
     is_validation_error = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isValidationError')
 
 
 class PromotionalEntitlement(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('created_at', 'customer', 'description', 'end_date', 'environment_id', 'feature', 'feature_id', 'has_unlimited_usage', 'id', 'is_visible', 'meter', 'period', 'reset_period', 'reset_period_configuration', 'start_date', 'status', 'unlimited', 'updated_at', 'usage_limit')
+    __field_names__ = ('created_at', 'customer', 'description', 'end_date', 'environment_id', 'feature', 'feature_id', 'has_unlimited_usage', 'id', 'is_visible', 'period', 'reset_period', 'reset_period_configuration', 'start_date', 'status', 'unlimited', 'updated_at', 'usage_limit')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     customer = sgqlc.types.Field(sgqlc.types.non_null(Customer), graphql_name='customer')
     description = sgqlc.types.Field(String, graphql_name='description')
     end_date = sgqlc.types.Field(DateTime, graphql_name='endDate')
     environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
     feature = sgqlc.types.Field(sgqlc.types.non_null(Feature), graphql_name='feature')
     feature_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='featureId')
     has_unlimited_usage = sgqlc.types.Field(Boolean, graphql_name='hasUnlimitedUsage')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
     is_visible = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isVisible')
-    meter = sgqlc.types.Field(Meter, graphql_name='meter')
     period = sgqlc.types.Field(sgqlc.types.non_null(PromotionalEntitlementPeriod), graphql_name='period')
     reset_period = sgqlc.types.Field(EntitlementResetPeriod, graphql_name='resetPeriod')
     reset_period_configuration = sgqlc.types.Field('ResetPeriodConfiguration', graphql_name='resetPeriodConfiguration')
     start_date = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='startDate')
     status = sgqlc.types.Field(sgqlc.types.non_null(PromotionalEntitlementStatus), graphql_name='status')
     unlimited = sgqlc.types.Field(Boolean, graphql_name='unlimited')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
@@ -6450,25 +6209,21 @@
     __schema__ = schema
     __field_names__ = ('task_id',)
     task_id = sgqlc.types.Field(String, graphql_name='taskId')
 
 
 class Query(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('addons', 'aggregated_events_by_customer', 'cached_entitlements', 'coupon', 'coupons', 'current_environment', 'current_user', 'customer_portal', 'customer_resources', 'customer_subscriptions', 'customers', 'entitlement', 'entitlements', 'environments', 'experiment', 'experiments', 'features', 'fetch_account', 'get_active_subscriptions', 'get_addon_by_ref_id', 'get_customer_by_ref_id', 'get_experiment_stats', 'get_paywall', 'get_plan_by_ref_id', 'hook', 'hooks', 'import_integration_tasks', 'integrations', 'members', 'mock_paywall', 'package_entitlements', 'paywall', 'plans', 'products', 'promotional_entitlements', 'sdk_configuration', 'send_test_hook', 'stripe_customers', 'stripe_products', 'stripe_subscriptions', 'subscription_entitlements', 'subscription_migration_tasks', 'test_hook_data', 'usage_events', 'usage_history', 'usage_measurements', 'widget_configuration')
+    __field_names__ = ('addons', 'cached_entitlements', 'coupon', 'coupons', 'current_environment', 'current_user', 'customer_portal', 'customer_resources', 'customer_subscriptions', 'customers', 'entitlement', 'entitlements', 'environments', 'experiment', 'experiments', 'features', 'fetch_account', 'get_active_subscriptions', 'get_addon_by_ref_id', 'get_customer_by_ref_id', 'get_experiment_stats', 'get_paywall', 'get_plan_by_ref_id', 'hook', 'hooks', 'import_integration_tasks', 'integrations', 'members', 'mock_paywall', 'package_entitlements', 'paywall', 'plans', 'products', 'promotional_entitlements', 'sdk_configuration', 'send_test_hook', 'stripe_customers', 'stripe_products', 'stripe_subscriptions', 'subscription_entitlements', 'subscription_migration_tasks', 'test_hook_data', 'usage_history', 'usage_measurements', 'widget_configuration')
     addons = sgqlc.types.Field(sgqlc.types.non_null(AddonConnection), graphql_name='addons', args=sgqlc.types.ArgDict((
         ('filter', sgqlc.types.Arg(AddonFilter, graphql_name='filter', default={})),
         ('paging', sgqlc.types.Arg(CursorPaging, graphql_name='paging', default={'first': 10})),
         ('sorting', sgqlc.types.Arg(sgqlc.types.list_of(sgqlc.types.non_null(AddonSort)), graphql_name='sorting', default=[{'direction': 'DESC', 'field': 'createdAt'}])),
 ))
     )
-    aggregated_events_by_customer = sgqlc.types.Field(sgqlc.types.non_null(AggregatedEventsByCustomer), graphql_name='aggregatedEventsByCustomer', args=sgqlc.types.ArgDict((
-        ('input', sgqlc.types.Arg(sgqlc.types.non_null(AggregatedEventsByCustomerInput), graphql_name='input', default=None)),
-))
-    )
     cached_entitlements = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(Entitlement))), graphql_name='cachedEntitlements', args=sgqlc.types.ArgDict((
         ('query', sgqlc.types.Arg(sgqlc.types.non_null(FetchEntitlementsQuery), graphql_name='query', default=None)),
 ))
     )
     coupon = sgqlc.types.Field(Coupon, graphql_name='coupon', args=sgqlc.types.ArgDict((
         ('id', sgqlc.types.Arg(sgqlc.types.non_null(String), graphql_name='id', default=None)),
 ))
@@ -6647,18 +6402,14 @@
         ('sorting', sgqlc.types.Arg(sgqlc.types.list_of(sgqlc.types.non_null(SubscriptionMigrationTaskSort)), graphql_name='sorting', default=[])),
 ))
     )
     test_hook_data = sgqlc.types.Field(sgqlc.types.non_null('TestHook'), graphql_name='testHookData', args=sgqlc.types.ArgDict((
         ('event_log_type', sgqlc.types.Arg(sgqlc.types.non_null(EventLogType), graphql_name='eventLogType', default=None)),
 ))
     )
-    usage_events = sgqlc.types.Field(sgqlc.types.non_null('UsageEventsPreview'), graphql_name='usageEvents', args=sgqlc.types.ArgDict((
-        ('input', sgqlc.types.Arg(sgqlc.types.non_null(UsageEventsInput), graphql_name='input', default=None)),
-))
-    )
     usage_history = sgqlc.types.Field(sgqlc.types.non_null('UsageHistory'), graphql_name='usageHistory', args=sgqlc.types.ArgDict((
         ('usage_history_input', sgqlc.types.Arg(sgqlc.types.non_null(UsageHistoryInput), graphql_name='usageHistoryInput', default=None)),
 ))
     )
     usage_measurements = sgqlc.types.Field(sgqlc.types.non_null('UsageMeasurementConnection'), graphql_name='usageMeasurements', args=sgqlc.types.ArgDict((
         ('filter', sgqlc.types.Arg(UsageMeasurementFilter, graphql_name='filter', default={})),
         ('paging', sgqlc.types.Arg(CursorPaging, graphql_name='paging', default={'first': 10})),
@@ -6667,20 +6418,14 @@
     )
     widget_configuration = sgqlc.types.Field(sgqlc.types.non_null('WidgetConfiguration'), graphql_name='widgetConfiguration', args=sgqlc.types.ArgDict((
         ('input', sgqlc.types.Arg(sgqlc.types.non_null(GetWidgetConfigurationInput), graphql_name='input', default=None)),
 ))
     )
 
 
-class RecalculateEntitlementsResult(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('task_id',)
-    task_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='taskId')
-
-
 class ResyncIntegrationResult(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('task_id',)
     task_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='taskId')
 
 
 class SdkConfiguration(sgqlc.types.Type):
@@ -6869,23 +6614,22 @@
     name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='name')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
     type = sgqlc.types.Field(sgqlc.types.non_null(CouponType), graphql_name='type')
 
 
 class SubscriptionEntitlement(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('created_at', 'description', 'environment_id', 'feature', 'feature_id', 'has_unlimited_usage', 'id', 'meter', 'reset_period', 'reset_period_configuration', 'subscription', 'subscription_id', 'updated_at', 'usage_limit')
+    __field_names__ = ('created_at', 'description', 'environment_id', 'feature', 'feature_id', 'has_unlimited_usage', 'id', 'reset_period', 'reset_period_configuration', 'subscription', 'subscription_id', 'updated_at', 'usage_limit')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
     description = sgqlc.types.Field(String, graphql_name='description')
     environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
     feature = sgqlc.types.Field(sgqlc.types.non_null(Feature), graphql_name='feature')
     feature_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='featureId')
     has_unlimited_usage = sgqlc.types.Field(Boolean, graphql_name='hasUnlimitedUsage')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
-    meter = sgqlc.types.Field(Meter, graphql_name='meter')
     reset_period = sgqlc.types.Field(EntitlementResetPeriod, graphql_name='resetPeriod')
     reset_period_configuration = sgqlc.types.Field('ResetPeriodConfiguration', graphql_name='resetPeriodConfiguration')
     subscription = sgqlc.types.Field(sgqlc.types.non_null(CustomerSubscription), graphql_name='subscription')
     subscription_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='subscriptionId')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
 
@@ -7024,24 +6768,21 @@
     code = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='code')
     is_validation_error = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isValidationError')
     ref_ids = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(String))), graphql_name='refIds')
 
 
 class SubscriptionPreview(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_period_range', 'discount', 'proration', 'sub_total', 'subscription', 'tax', 'tax_details', 'total', 'total_excluding_tax')
+    __field_names__ = ('billing_period_range', 'discount', 'proration', 'sub_total', 'subscription', 'total')
     billing_period_range = sgqlc.types.Field(sgqlc.types.non_null(DateRange), graphql_name='billingPeriodRange')
     discount = sgqlc.types.Field('SubscriptionPreviewDiscountDTO', graphql_name='discount')
     proration = sgqlc.types.Field('SubscriptionPreviewProrations', graphql_name='proration')
     sub_total = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='subTotal')
     subscription = sgqlc.types.Field('SubscriptionPricePreviewDTO', graphql_name='subscription')
-    tax = sgqlc.types.Field(Money, graphql_name='tax')
-    tax_details = sgqlc.types.Field('SubscriptionPreviewTaxDetails', graphql_name='taxDetails')
     total = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='total')
-    total_excluding_tax = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='totalExcludingTax')
 
 
 class SubscriptionPreviewDiscountDTO(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('duration_in_months', 'duration_type', 'type', 'value')
     duration_in_months = sgqlc.types.Field(Float, graphql_name='durationInMonths')
     duration_type = sgqlc.types.Field(sgqlc.types.non_null(DiscountDurationType), graphql_name='durationType')
@@ -7054,99 +6795,79 @@
     __field_names__ = ('credit', 'debit', 'net_amount', 'proration_date')
     credit = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='credit')
     debit = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='debit')
     net_amount = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='netAmount')
     proration_date = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='prorationDate')
 
 
-class SubscriptionPreviewTaxDetails(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('display_name', 'inclusive', 'percentage')
-    display_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='displayName')
-    inclusive = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='inclusive')
-    percentage = sgqlc.types.Field(sgqlc.types.non_null(Float), graphql_name='percentage')
-
-
 class SubscriptionPrice(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_model', 'created_at', 'feature_id', 'id', 'price', 'subscription', 'updated_at', 'usage_limit')
-    billing_model = sgqlc.types.Field(BillingModel, graphql_name='billingModel')
+    __field_names__ = ('created_at', 'id', 'price', 'subscription', 'updated_at', 'usage_limit')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
-    feature_id = sgqlc.types.Field(String, graphql_name='featureId')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
     price = sgqlc.types.Field(Price, graphql_name='price')
     subscription = sgqlc.types.Field(sgqlc.types.non_null(CustomerSubscription), graphql_name='subscription')
     updated_at = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='updatedAt')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
 
 
 class SubscriptionPriceAggregateGroupBy(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_model', 'created_at', 'feature_id', 'id', 'updated_at', 'usage_limit')
-    billing_model = sgqlc.types.Field(BillingModel, graphql_name='billingModel')
+    __field_names__ = ('created_at', 'id', 'updated_at', 'usage_limit')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
-    feature_id = sgqlc.types.Field(String, graphql_name='featureId')
     id = sgqlc.types.Field(String, graphql_name='id')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
 
 
 class SubscriptionPriceAvgAggregate(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('usage_limit',)
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
 
 
 class SubscriptionPriceCountAggregate(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_model', 'created_at', 'feature_id', 'id', 'updated_at', 'usage_limit')
-    billing_model = sgqlc.types.Field(Int, graphql_name='billingModel')
+    __field_names__ = ('created_at', 'id', 'updated_at', 'usage_limit')
     created_at = sgqlc.types.Field(Int, graphql_name='createdAt')
-    feature_id = sgqlc.types.Field(Int, graphql_name='featureId')
     id = sgqlc.types.Field(Int, graphql_name='id')
     updated_at = sgqlc.types.Field(Int, graphql_name='updatedAt')
     usage_limit = sgqlc.types.Field(Int, graphql_name='usageLimit')
 
 
 class SubscriptionPriceEdge(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('cursor', 'node')
     cursor = sgqlc.types.Field(sgqlc.types.non_null(ConnectionCursor), graphql_name='cursor')
     node = sgqlc.types.Field(sgqlc.types.non_null(SubscriptionPrice), graphql_name='node')
 
 
 class SubscriptionPriceMaxAggregate(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_model', 'created_at', 'feature_id', 'id', 'updated_at', 'usage_limit')
-    billing_model = sgqlc.types.Field(BillingModel, graphql_name='billingModel')
+    __field_names__ = ('created_at', 'id', 'updated_at', 'usage_limit')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
-    feature_id = sgqlc.types.Field(String, graphql_name='featureId')
     id = sgqlc.types.Field(String, graphql_name='id')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
 
 
 class SubscriptionPriceMinAggregate(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('billing_model', 'created_at', 'feature_id', 'id', 'updated_at', 'usage_limit')
-    billing_model = sgqlc.types.Field(BillingModel, graphql_name='billingModel')
+    __field_names__ = ('created_at', 'id', 'updated_at', 'usage_limit')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
-    feature_id = sgqlc.types.Field(String, graphql_name='featureId')
     id = sgqlc.types.Field(String, graphql_name='id')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
 
 
 class SubscriptionPricePreviewDTO(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('sub_total', 'tax', 'total', 'total_excluding_tax')
+    __field_names__ = ('sub_total', 'total')
     sub_total = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='subTotal')
-    tax = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='tax')
     total = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='total')
-    total_excluding_tax = sgqlc.types.Field(sgqlc.types.non_null(Money), graphql_name='totalExcludingTax')
 
 
 class SubscriptionPriceSumAggregate(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('usage_limit',)
     usage_limit = sgqlc.types.Field(Float, graphql_name='usageLimit')
 
@@ -7236,16 +6957,15 @@
     is_validation_error = sgqlc.types.Field(sgqlc.types.non_null(Boolean), graphql_name='isValidationError')
     non_compatible_addons = sgqlc.types.Field(sgqlc.types.list_of(sgqlc.types.non_null(String)), graphql_name='nonCompatibleAddons')
     plan_display_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='planDisplayName')
 
 
 class UnitAmountChangeVariables(sgqlc.types.Type):
     __schema__ = schema
-    __field_names__ = ('feature_id', 'new_unit_amount')
-    feature_id = sgqlc.types.Field(String, graphql_name='featureId')
+    __field_names__ = ('new_unit_amount',)
     new_unit_amount = sgqlc.types.Field(Float, graphql_name='newUnitAmount')
 
 
 class UnsupportedFeatureTypeError(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('code', 'feature_type')
     code = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='code')
@@ -7262,29 +6982,14 @@
 class UpdateEntitlementsOrderDTO(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('id', 'order')
     id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
     order = sgqlc.types.Field(Float, graphql_name='order')
 
 
-class UsageEvent(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('dimensions', 'event_name', 'id', 'timestamp')
-    dimensions = sgqlc.types.Field(JSON, graphql_name='dimensions')
-    event_name = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='eventName')
-    id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='id')
-    timestamp = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='timestamp')
-
-
-class UsageEventsPreview(sgqlc.types.Type):
-    __schema__ = schema
-    __field_names__ = ('events',)
-    events = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null(UsageEvent))), graphql_name='events')
-
-
 class UsageHistory(sgqlc.types.Type):
     __schema__ = schema
     __field_names__ = ('end_date', 'start_date', 'usage_measurements')
     end_date = sgqlc.types.Field(DateTime, graphql_name='endDate')
     start_date = sgqlc.types.Field(sgqlc.types.non_null(DateTime), graphql_name='startDate')
     usage_measurements = sgqlc.types.Field(sgqlc.types.non_null(sgqlc.types.list_of(sgqlc.types.non_null('UsageMeasurementPoint'))), graphql_name='usageMeasurements')
```

### Comparing `stigg_api_client-0.499.0/PKG-INFO` & `stigg_api_client-0.5.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,22 +1,24 @@
 Metadata-Version: 2.1
 Name: stigg-api-client
-Version: 0.499.0
+Version: 0.5.0
 Summary: 
 Author: Stigg
 Author-email: support@stigg.io
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: graphql-core (>=3.1,<4.0)
-Requires-Dist: requests (>=2.28,<3.0)
+Requires-Dist: black (>=22.8.0,<23.0.0)
+Requires-Dist: flake8 (>=5.0.4,<6.0.0)
+Requires-Dist: graphql-core (==3.1.6)
+Requires-Dist: requests (>=2.28.1,<3.0.0)
 Requires-Dist: sgqlc (>=16.0,<17.0)
 Description-Content-Type: text/markdown
 
 # stigg-api-client
 
 This library provides a Python wrapper to [Stigg's GraphQL API](https://docs.stigg.io/docs/graphql-api) based on 
 the operations that are in use by the [Stigg's Node.js SDK](https://docs.stigg.io/docs/nodejs-sdk).
```

