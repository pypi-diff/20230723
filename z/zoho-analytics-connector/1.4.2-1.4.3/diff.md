# Comparing `tmp/zoho_analytics_connector-1.4.2.tar.gz` & `tmp/zoho_analytics_connector-1.4.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zoho_analytics_connector-1.4.2.tar", last modified: Thu Apr 20 06:17:20 2023, max compression
+gzip compressed data, was "zoho_analytics_connector-1.4.3.tar", last modified: Sun Jul 23 05:13:11 2023, max compression
```

## Comparing `zoho_analytics_connector-1.4.2.tar` & `zoho_analytics_connector-1.4.3.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxr-x   0 tim       (1000) tim       (1000)        0 2023-04-20 06:17:20.880615 zoho_analytics_connector-1.4.2/
--rw-rw-r--   0 tim       (1000) tim       (1000)      217 2022-07-14 03:04:02.000000 zoho_analytics_connector-1.4.2/LICENSE
--rw-rw-r--   0 tim       (1000) tim       (1000)    14383 2023-04-20 06:17:20.880615 zoho_analytics_connector-1.4.2/PKG-INFO
--rw-rw-r--   0 tim       (1000) tim       (1000)    13559 2023-04-20 06:16:45.000000 zoho_analytics_connector-1.4.2/README.md
--rw-rw-r--   0 tim       (1000) tim       (1000)       38 2023-04-20 06:17:20.880615 zoho_analytics_connector-1.4.2/setup.cfg
--rw-rw-r--   0 tim       (1000) tim       (1000)     1747 2023-04-20 06:16:45.000000 zoho_analytics_connector-1.4.2/setup.py
-drwxrwxr-x   0 tim       (1000) tim       (1000)        0 2023-04-20 06:17:20.876615 zoho_analytics_connector-1.4.2/zoho_analytics_connector/
--rw-rw-r--   0 tim       (1000) tim       (1000)   100603 2022-11-23 02:51:47.000000 zoho_analytics_connector-1.4.2/zoho_analytics_connector/analytics_client_upstream.py
--rw-rw-r--   0 tim       (1000) tim       (1000)    10019 2023-04-20 06:14:57.000000 zoho_analytics_connector-1.4.2/zoho_analytics_connector/enhanced_report_client.py
--rw-rw-r--   0 tim       (1000) tim       (1000)   113880 2023-03-14 04:40:03.000000 zoho_analytics_connector-1.4.2/zoho_analytics_connector/report_client.py
-drwxrwxr-x   0 tim       (1000) tim       (1000)        0 2023-04-20 06:17:20.880615 zoho_analytics_connector-1.4.2/zoho_analytics_connector.egg-info/
--rw-rw-r--   0 tim       (1000) tim       (1000)    14383 2023-04-20 06:17:20.000000 zoho_analytics_connector-1.4.2/zoho_analytics_connector.egg-info/PKG-INFO
--rw-rw-r--   0 tim       (1000) tim       (1000)      412 2023-04-20 06:17:20.000000 zoho_analytics_connector-1.4.2/zoho_analytics_connector.egg-info/SOURCES.txt
--rw-rw-r--   0 tim       (1000) tim       (1000)        1 2023-04-20 06:17:20.000000 zoho_analytics_connector-1.4.2/zoho_analytics_connector.egg-info/dependency_links.txt
--rw-rw-r--   0 tim       (1000) tim       (1000)       15 2023-04-20 06:17:20.000000 zoho_analytics_connector-1.4.2/zoho_analytics_connector.egg-info/requires.txt
--rw-rw-r--   0 tim       (1000) tim       (1000)       25 2023-04-20 06:17:20.000000 zoho_analytics_connector-1.4.2/zoho_analytics_connector.egg-info/top_level.txt
+drwxrwxr-x   0 tim       (1000) tim       (1000)        0 2023-07-23 05:13:11.677274 zoho_analytics_connector-1.4.3/
+-rw-rw-r--   0 tim       (1000) tim       (1000)      217 2022-07-14 03:04:02.000000 zoho_analytics_connector-1.4.3/LICENSE
+-rw-rw-r--   0 tim       (1000) tim       (1000)    14408 2023-07-23 05:13:11.677274 zoho_analytics_connector-1.4.3/PKG-INFO
+-rw-rw-r--   0 tim       (1000) tim       (1000)    13584 2023-07-23 03:20:17.000000 zoho_analytics_connector-1.4.3/README.md
+-rw-rw-r--   0 tim       (1000) tim       (1000)       38 2023-07-23 05:13:11.677274 zoho_analytics_connector-1.4.3/setup.cfg
+-rw-rw-r--   0 tim       (1000) tim       (1000)     1747 2023-07-23 03:20:17.000000 zoho_analytics_connector-1.4.3/setup.py
+drwxrwxr-x   0 tim       (1000) tim       (1000)        0 2023-07-23 05:13:11.677274 zoho_analytics_connector-1.4.3/zoho_analytics_connector/
+-rw-rw-r--   0 tim       (1000) tim       (1000)   100603 2022-11-23 02:51:47.000000 zoho_analytics_connector-1.4.3/zoho_analytics_connector/analytics_client_upstream.py
+-rw-rw-r--   0 tim       (1000) tim       (1000)    10075 2023-07-23 03:06:02.000000 zoho_analytics_connector-1.4.3/zoho_analytics_connector/enhanced_report_client.py
+-rw-rw-r--   0 tim       (1000) tim       (1000)   115313 2023-07-23 03:17:37.000000 zoho_analytics_connector-1.4.3/zoho_analytics_connector/report_client.py
+drwxrwxr-x   0 tim       (1000) tim       (1000)        0 2023-07-23 05:13:11.677274 zoho_analytics_connector-1.4.3/zoho_analytics_connector.egg-info/
+-rw-rw-r--   0 tim       (1000) tim       (1000)    14408 2023-07-23 05:13:11.000000 zoho_analytics_connector-1.4.3/zoho_analytics_connector.egg-info/PKG-INFO
+-rw-rw-r--   0 tim       (1000) tim       (1000)      412 2023-07-23 05:13:11.000000 zoho_analytics_connector-1.4.3/zoho_analytics_connector.egg-info/SOURCES.txt
+-rw-rw-r--   0 tim       (1000) tim       (1000)        1 2023-07-23 05:13:11.000000 zoho_analytics_connector-1.4.3/zoho_analytics_connector.egg-info/dependency_links.txt
+-rw-rw-r--   0 tim       (1000) tim       (1000)       15 2023-07-23 05:13:11.000000 zoho_analytics_connector-1.4.3/zoho_analytics_connector.egg-info/requires.txt
+-rw-rw-r--   0 tim       (1000) tim       (1000)       25 2023-07-23 05:13:11.000000 zoho_analytics_connector-1.4.3/zoho_analytics_connector.egg-info/top_level.txt
```

### Comparing `zoho_analytics_connector-1.4.2/PKG-INFO` & `zoho_analytics_connector-1.4.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zoho_analytics_connector
-Version: 1.4.2
+Version: 1.4.3
 Summary: Zoho Analytics connector
 Home-page: https://github.com/timrichardson/zoho_analytics_connector
 Author: Tim Richardson
 Author-email: tim@growthpath.com.au
 License: MPL-2.0
 Keywords: zoho analytics
 Platform: UNKNOWN
@@ -297,17 +297,15 @@
             #get an error, but error handling is not working, the API returns a 400 with no content in the message
             r = get_enhanced_zoho_analytics_client.create_table(table_design=zoho_sales_fact_table)
             print (r)
 
 
 Changes
 -------------
-
-next_version Test updates
-
+1.4.3 Exponential backoff with jitter used for retry
 1.4.2 Added reporting_currency to enhanced_reporting_client
 1.4.1 Something seems to changed with the UTF encoding returned by the export endpoint. Change decoding to use utf-8-sig 
 1.4.0 some adaptation towards new API from Zoho
 
 1.3.6 Documentation updates, test updates. Added a 'pre-delete function' to calculate how many rows should be deleted.
     deleteData returns an int not a string for the number of rows deleted.
```

### Comparing `zoho_analytics_connector-1.4.2/README.md` & `zoho_analytics_connector-1.4.3/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -274,17 +274,15 @@
             #get an error, but error handling is not working, the API returns a 400 with no content in the message
             r = get_enhanced_zoho_analytics_client.create_table(table_design=zoho_sales_fact_table)
             print (r)
 
 
 Changes
 -------------
-
-next_version Test updates
-
+1.4.3 Exponential backoff with jitter used for retry
 1.4.2 Added reporting_currency to enhanced_reporting_client
 1.4.1 Something seems to changed with the UTF encoding returned by the export endpoint. Change decoding to use utf-8-sig 
 1.4.0 some adaptation towards new API from Zoho
 
 1.3.6 Documentation updates, test updates. Added a 'pre-delete function' to calculate how many rows should be deleted.
     deleteData returns an int not a string for the number of rows deleted.
```

### Comparing `zoho_analytics_connector-1.4.2/setup.py` & `zoho_analytics_connector-1.4.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from os import path
 cmdclass = {'build_sphinx': BuildDoc}
 
 # https://pypi.org/classifiers/
 
 name = 'zoho_analytics_connector'
 keywords = 'zoho analytics'
-version = '1.4.2'
+version = '1.4.3'
 this_directory = path.abspath(path.dirname(__file__))
 with open(path.join(this_directory, 'README.md'), encoding='utf-8') as f:
     long_description = f.read()
 
 setup(
     name=name,
     keywords=keywords,
```

### Comparing `zoho_analytics_connector-1.4.2/zoho_analytics_connector/analytics_client_upstream.py` & `zoho_analytics_connector-1.4.3/zoho_analytics_connector/analytics_client_upstream.py`

 * *Files identical despite different names*

### Comparing `zoho_analytics_connector-1.4.2/zoho_analytics_connector/enhanced_report_client.py` & `zoho_analytics_connector-1.4.3/zoho_analytics_connector/enhanced_report_client.py`

 * *Files 2% similar despite different names*

```diff
@@ -22,15 +22,14 @@
 ch.setLevel(logging.DEBUG)
 logger.addHandler(ch)
 
 """ add some helper functions on top of report_client"""
 
 
 class EnhancedZohoAnalyticsClient(report_client.ReportClient):
-
     @staticmethod
     def process_table_meta_data(catalog, force_lowercase_column_names=False):
         """ catalog is a ZOHO_CATALOG_INFO dict. Call this from get_database_metadata for example
          Return a dict keyed by tablename, each item being a dict keyed by column name, with the item being the
          catalog info for the col
          So all the table names can be found as table_data.keys()
          for for a given table name, the column names are table_data['table1'].keys()
@@ -52,16 +51,16 @@
                     else:
                         col_data[col['columnName']] = col
 
         return table_data
 
     def __init__(self, login_email_id: str, token: str, default_databasename: str = None, clientId=None,
                  clientSecret=None, serverURL=None, reportServerURL=None, default_retries=None,
-                 reporting_currency:str=None,
-                 error_email_list: Optional[List[str]]=None):
+                 reporting_currency: str = None,
+                 error_email_list: Optional[List[str]] = None):
         """ error email list is not used by the client, but it is available for callers as a convenience"""
         self.login_email_id = login_email_id
         self.default_databasename = default_databasename
         self.error_email_list = error_email_list or [login_email_id]
         self.reporting_currency = reporting_currency
         super().__init__(token=token, clientId=clientId, clientSecret=clientSecret, serverURL=serverURL,
                          reportServerURL=reportServerURL, default_retries=default_retries)
@@ -121,27 +120,28 @@
         """ data is a csv-style string, newline separated. Matching columns is a comma separated string
         import_mode is one of TRUNCATEADD, APPEND, UPDATEADD
         """
         retry_count = 0
         retry_limit = retry_limit or self.default_retries
         impResult = None
         # import_content_demojized = emoji.demojize(import_content)
-        import_content_demojized = import_content #try without this, move data cleaning to the calling function
+        import_content_demojized = import_content  # try without this, move data cleaning to the calling function
         database_name = database_name or self.default_databasename
         uri = self.getURI(dbOwnerName=self.login_email_id, dbName=database_name, tableOrReportName=table_name)
         # import_modes = APPEND / TRUNCATEADD / UPDATEADD
         impResult = self.importData_v2(uri, import_mode=import_mode, import_content=import_content_demojized,
                                        date_format=date_format,
                                        matching_columns=matching_columns, retry_countdown=retry_limit)
 
         return impResult
 
     def data_export_using_sql(self, sql, table_name, database_name: str = None, cache_object=None,
                               cache_timeout_seconds=60, retry_countdown=5) -> csv.DictReader:
         """ returns a csv.DictReader after querying with the sql provided.
+        retry_countdown is the number of retries
         The Zoho API insists on a table or report name, but it doesn't seem to restrict the query
         The cache object has a get and set function like the django cache does: https://docs.djangoproject.com/en/3.1/topics/cache/
         The cache key is the sql query"""
 
         if cache_object:
             returned_data = cache_object.get(sql)
         else:
@@ -191,8 +191,8 @@
 
     def rename_column(self, table_name, old_column_name, new_column_name, database_name: Optional[str] = None,
                       retry_countdown=5):
         """ rename a column in a table """
         uri = self.getURI(dbOwnerName=self.login_email_id, dbName=database_name or self.default_databasename,
                           tableOrReportName=table_name)
         self.renameColumn(tableURI=uri, oldColumnName=old_column_name, newColumnName=new_column_name,
-                          retry_countdown=retry_countdown)
+                          retry_countdown=retry_countdown)
```

### Comparing `zoho_analytics_connector-1.4.2/zoho_analytics_connector/report_client.py` & `zoho_analytics_connector-1.4.3/zoho_analytics_connector/report_client.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 
 This Source Code Form is subject to the terms of the Mozilla Public
 License, v. 2.0. If a copy of the MPL was not distributed with this
 file, You can obtain one at https://mozilla.org/MPL/2.0/.
 """
 import json
 import io
+import random
 import re
 import time
 import logging
 import urllib
 import urllib.parse
 import xml.dom.minidom
 from typing import MutableMapping, Optional, Union
@@ -49,20 +50,22 @@
     """
      ReportClient provides the python based language binding to the https based API of Zoho Analytics.
      @note: Authentication via authtoken is deprecated, use OAuth. kindly send parameter as ReportClient(token,clientId,clientSecret).
      """
 
     isOAuth = False
     request_timeout = 60
+
     # clientId = None
     # clientSecret = None
     # refresh_or_access_token = None
     # token_timestamp = time.time()
 
-    def __init__(self, token, clientId=None, clientSecret=None,serverURL=None,reportServerURL=None,default_retries=0):
+    def __init__(self, token, clientId=None, clientSecret=None, serverURL=None, reportServerURL=None,
+                 default_retries=0):
         """
         Creates a new C{ReportClient} instance.
         @param token: User's authtoken or ( refresh token for OAUth).
         @type token:string
         @param clientId: User client id for OAUth
         @type clientId:string
         @param clientSecret: User client secret for OAuth
@@ -74,268 +77,281 @@
         """
         self.iamServerURL = serverURL or "https://accounts.zoho.com"
         self.reportServerURL = reportServerURL or "https://analyticsapi.zoho.com"
         self.requests_session = requests_retry_session(retries=default_retries)
         self.clientId = clientId
         self.clientSecret = clientSecret
         self.accesstoken = token
-        self.token_timestamp = time.time()  #this is a safe default
+        self.token_timestamp = time.time()  # this is a safe default
         self.default_retries = default_retries
-        if (clientId == None and clientSecret == None): #not using OAuth2
+        if (clientId == None and clientSecret == None):  # not using OAuth2
             self.__token = token
         else:
-            self.getOAuthToken()  #this sets the instance variable
+            self.getOAuthToken()  # this sets the instance variable
             ReportClient.isOAuth = True
         self.request_timeout = 60
 
     @property
     def token(self):
         if ReportClient.isOAuth and time.time() - self.token_timestamp > 50 * 60:
             logger.debug("Refreshing zoho analytics oauth token")
             token = self.getOAuthToken()
             self.__token = token
             self.token_timestamp = time.time()
         return self.__token
 
     @token.setter
-    def token(self,token):
+    def token(self, token):
         self.__token = token
         self.token_timestamp = time.time()
 
-
     def getOAuthToken(self):
         """
         Internal method for getting OAuth token.
         """
         dict = {}
         dict["client_id"] = self.clientId
         dict["client_secret"] = self.clientSecret
         dict["refresh_token"] = self.accesstoken
         dict["grant_type"] = "refresh_token"
-        #dict = urllib.parse.urlencode(dict)  we should pass a dict, not a string
+        # dict = urllib.parse.urlencode(dict)  we should pass a dict, not a string
         accUrl = self.iamServerURL + "/oauth/v2/token"
-        respObj = self.getResp(accUrl, "POST", dict,add_token=False)
+        respObj = self.getResp(accUrl, "POST", dict, add_token=False)
         if (respObj.status_code != 200):
             raise ServerError(respObj)
         else:
             resp = respObj.response.json()
             if ("access_token" in resp):
                 self.__token = resp['access_token']
                 return resp["access_token"]
             else:
                 raise ValueError("Error while getting OAuth token ", resp)
 
-    def getResp(self, url: str, httpMethod: str, payLoad,add_token=True,extra_headers=None,**kwargs):
+    def getResp(self, url: str, httpMethod: str, payLoad, add_token=True, extra_headers=None, **kwargs):
         """
         Internal method. for GET, payLoad is params
         """
         requests_session = self.requests_session or requests_retry_session()
         if httpMethod.upper() == 'POST':
             headers = {}
-            if add_token and ReportClient.isOAuth and hasattr(self,'token'): #check for token because this can be called during __init__ and isOAuth could be true.
+            if add_token and ReportClient.isOAuth and hasattr(self,
+                                                              'token'):  # check for token because this can be called during __init__ and isOAuth could be true.
                 headers["Authorization"] = "Zoho-oauthtoken " + self.token
             headers['User-Agent'] = "ZohoAnalytics Python GrowthPath Library"
             if extra_headers:
                 headers = {**headers, **extra_headers}
             try:
-                resp = requests_session.post(url, data=payLoad, headers=headers, timeout=self.request_timeout,**kwargs)
+                resp = requests_session.post(url, data=payLoad, headers=headers, timeout=self.request_timeout, **kwargs)
                 if 'invalid client' in resp.text:
                     raise requests.exceptions.RequestException("Invalid Client")
                 respObj = ResponseObj(resp)
             except requests.exceptions.RequestException as e:
-               logger.exception(f"{e=}")
-               raise e
+                logger.exception(f"{e=}")
+                raise e
             return respObj
         elif httpMethod.upper() == 'GET':
             headers = {}
             if add_token and ReportClient.isOAuth and hasattr(self,
                                                               'token'):  # check for token because this can be called during __init__ and isOAuth could be true.
                 headers["Authorization"] = "Zoho-oauthtoken " + self.token
             headers['User-Agent'] = "ZohoAnalytics Python GrowthPath Library"
             if extra_headers:
                 headers = {**headers, **extra_headers}
             try:
-                resp = requests_session.get(url, params=payLoad, headers=headers, timeout=self.request_timeout,**kwargs)
+                resp = requests_session.get(url, params=payLoad, headers=headers, timeout=self.request_timeout,
+                                            **kwargs)
                 if 'invalid client' in resp.text:
                     raise requests.exceptions.RequestException("Invalid Client")
                 respObj = ResponseObj(resp)
             except requests.exceptions.RequestException as e:
                 logger.exception(f"{e=}")
                 raise e
             return respObj
 
 
         else:
             raise RuntimeError(f"Unexpected httpMethod in getResp, was expecting POST or GET but got {httpMethod}")
 
-    def __sendRequest(self, url, httpMethod, payLoad, action, callBackData=None,retry_countdown:int=None, extra_headers=None,**keywords):
+    def __sendRequest(self, url, httpMethod, payLoad, action, callBackData=None, retry_countdown: int = None,
+                      extra_headers=None, **keywords):
         code = ""
         if not retry_countdown:
             retry_countdown = self.default_retries or 1
         init_retry_countdown = retry_countdown
         while retry_countdown > 0:
             retry_countdown -= 1
             try:
-                respObj = self.getResp(url, httpMethod, payLoad, extra_headers=extra_headers,**keywords)
+                respObj = self.getResp(url, httpMethod, payLoad, extra_headers=extra_headers, **keywords)
             except Exception as e:
-                logger.exception(f" getResp exception in __sendRequest, {retry_countdown}, {e}")  #connection error
+                logger.exception(f" getResp exception in __sendRequest, {retry_countdown}, {e}")  # connection error
                 if retry_countdown <= 0:
                     raise e
                 else:
-                    time.sleep(min(10 - retry_countdown, 1) * 10)
+                    sleep_time = min((3 * (2 ** (10 - retry_countdown))) + random.random(),
+                                     60)  # Add jitter and cap max delay at 60 seconds
+
+                    time.sleep(sleep_time)
                     continue
 
-            if (respObj.status_code in [200,]):
+            if (respObj.status_code in [200, ]):
                 return self.handleResponse(respObj, action, callBackData)
-            elif (respObj.status_code in [400,]):
-                #400 errors may be an API limit error, which are handled by the result parsing
+            elif (respObj.status_code in [400, ]):
+                # 400 errors may be an API limit error, which are handled by the result parsing
                 try:
                     try:
-                        #j = respObj.response.json(strict=False) #getting decode errors in this and they don't make sense
-                        j = json.loads(respObj.response.text,strict=False)
+                        # j = respObj.response.json(strict=False) #getting decode errors in this and they don't make sense
+                        j = json.loads(respObj.response.text, strict=False)
                         code = j['response']['error']['code']
                     except json.JSONDecodeError as e:
                         logger.error(f"API caused a JSONDecodeError for {respObj.response.text} ")
                         code = None
                     if not code:
-                        m = re.search(r'"code":(\d+)',respObj.response.text)
+                        m = re.search(r'"code":(\d+)', respObj.response.text)
                         if m:
-                            code=int(m.group(1))
+                            code = int(m.group(1))
                         else:
                             code = -1
                             logger.error(f"could not find error code in {respObj.response.text} ")
                             time.sleep(min(10 - retry_countdown, 1) * 10)
                             continue
 
                     logger.debug(f"API returned a 400 result and an error code: {code} ")
-                    if code in [6045,]:
-                        logger.error(f"Zoho API Recoverable rate limit (rate limit exceeded); there are {retry_countdown+1} retries left")
+                    if code in [6045, ]:
+                        logger.error(
+                            f"Zoho API Recoverable rate limit (rate limit exceeded); there are {retry_countdown + 1} retries left")
                         if retry_countdown < 0:
                             logger.error(
-                                    f"Zoho API Recoverable error (rate limit exceeded), but exhausted retries")
-                            raise UnrecoverableRateLimitError(urlResp=respObj,zoho_error_code=code)
+                                f"Zoho API Recoverable error (rate limit exceeded), but exhausted retries")
+                            raise UnrecoverableRateLimitError(urlResp=respObj, zoho_error_code=code)
                         else:
-                            time.sleep(min(10-retry_countdown,1)*10)
+                            time.sleep(min(10 - retry_countdown, 1) * 10)
                             continue
                     elif code in [6001, ]:
                         logger.error(
                             f"6001 error, rows in Zoho plan exceeded {respObj.response.text}")
                         raise UnrecoverableRateLimitError(urlResp=respObj, zoho_error_code=code)
                     elif code in [6043, ]:
                         logger.error(
                             f"6043 error, daily API limit in Zoho plan exceeded {respObj.response.text}")
                         raise UnrecoverableRateLimitError(urlResp=respObj, zoho_error_code=code)
                     elif code in [7103, ]:
                         logger.error(
                             f"7103 error, workspace not found (check authentication) {respObj.response.text}")
                         raise ServerError(urlResp=respObj, zoho_error_code=code)
                     elif code in [7179, ]:
-                       logger.error(
-                           f"7179 error, workspace reports no view present. Initialise with a dummy table {respObj.response.text}")
-                       raise ServerError(urlResp=respObj, zoho_error_code=code)
+                        logger.error(
+                            f"7179 error, workspace reports no view present. Initialise with a dummy table {respObj.response.text}")
+                        raise ServerError(urlResp=respObj, zoho_error_code=code)
                     elif code in [7232, ]:
                         logger.error(
                             f"7232 error,an invalid value has been provided according to the column's data type) {respObj.response.text=} ")
                         raise ServerError(urlResp=respObj, zoho_error_code=code)
                     elif code in [7280, ]:
-                        logger.error(f"7280 error, relating to schema errors, return immediately {respObj.response.text}")
+                        logger.error(
+                            f"7280 error, relating to schema errors, return immediately {respObj.response.text}")
                         raise ServerError(urlResp=respObj, zoho_error_code=code)
                     elif code in [7389, ]:
                         logger.error(f"7389 Error from zoho Organisation doest not exist {respObj.response.text}")
                         raise ServerError(urlResp=respObj, zoho_error_code=code)
                     elif code in [8540, ]:
                         logger.error(f"8540 Error, token has incorrect scope {respObj.response.text}")
                         raise ServerError(urlResp=respObj, zoho_error_code=code)
-                    elif code in [8535,]: #invalid oauth token
+                    elif code in [8535, ]:  # invalid oauth token
                         try:
                             self.getOAuthToken()
                         except:
                             pass
                         logger.error(f"Zoho API Recoverable error encountered (invalid oauth token), will retry")
                         if retry_countdown < 0:
                             logger.error(
-                                    f"Zoho API Recoverable error (invalid oauth token) exhausted retries")
-                            raise UnrecoverableRateLimitError(urlResp=respObj,zoho_error_code=code)
+                                f"Zoho API Recoverable error (invalid oauth token) exhausted retries")
+                            raise UnrecoverableRateLimitError(urlResp=respObj, zoho_error_code=code)
                         else:
                             time.sleep(min(10 - retry_countdown, 1) * 10)
                             continue
                     elif code in [8509, ]:  # parameter does not match accepted input pattern
-                        logger.error(f"Error 8509 encountered, something is wrong with the data format, no retry is attempted")
-                        raise BadDataError(respObj,zoho_error_code=code)
-                    elif code in [10001,]:  #10001 is "Another import is in progress, so we can try this again"
-                        logger.error(f"Zoho API Recoverable error encountered (Another import is in progress), will retry")
+                        logger.error(
+                            f"Error 8509 encountered, something is wrong with the data format, no retry is attempted")
+                        raise BadDataError(respObj, zoho_error_code=code)
+                    elif code in [10001, ]:  # 10001 is "Another import is in progress, so we can try this again"
+                        logger.error(
+                            f"Zoho API Recoverable error encountered (Another import is in progress), will retry")
                         if retry_countdown < 0:
                             logger.error(
-                            f"Zoho API Recoverable error (Another import is in progress) but exhausted retries")
-                            raise UnrecoverableRateLimitError(urlResp=respObj,zoho_error_code=code, message="Zoho error: Another import is in progress")
+                                f"Zoho API Recoverable error (Another import is in progress) but exhausted retries")
+                            raise UnrecoverableRateLimitError(urlResp=respObj, zoho_error_code=code,
+                                                              message="Zoho error: Another import is in progress")
                         else:
                             time.sleep(min(10 - retry_countdown, 1) * 10)
                             continue
 
                     else:
-                        #raise ServerError(respObj,zoho_error_code=code)
+                        # raise ServerError(respObj,zoho_error_code=code)
                         msg = f"Unexpected status code {code=}, will attempt retry"
                         try:
                             msg += respObj.response.text
                         except Exception:
                             pass
                         logger.exception(msg)
                         time.sleep(min(10 - retry_countdown, 1) * 10)
                         continue
-                except (RecoverableRateLimitError,UnrecoverableRateLimitError,BadDataError):
+                except (RecoverableRateLimitError, UnrecoverableRateLimitError, BadDataError):
                     raise
                 except ServerError as e:
                     logger.error(f"ServerError raised on _sendRequest.  {url=} {payLoad=} {action=} ")
                     import_data = payLoad.get("ZOHO_IMPORT_DATA") if payLoad else None
                     if import_data:
-                        logger.error(f"Import data, a csv file as a string. Row 1 is header, col 0 is first col (id): {import_data} ")
-                    raise ServerError(respObj,zoho_error_code=code)
-            elif (respObj.status_code in [401,]):
+                        logger.error(
+                            f"Import data, a csv file as a string. Row 1 is header, col 0 is first col (id): {import_data} ")
+                    raise ServerError(respObj, zoho_error_code=code)
+            elif (respObj.status_code in [401, ]):
                 try:
-                    #j = respObj.response.json(strict=False) #getting decode errors in this and they don't make sense
-                    j = json.loads(respObj.response.text,strict=False)
+                    # j = respObj.response.json(strict=False) #getting decode errors in this and they don't make sense
+                    j = json.loads(respObj.response.text, strict=False)
                     code = j['response']['error']['code']
                 except json.JSONDecodeError as e:
                     logger.error(f"API caused a JSONDecodeError for {respObj.response.text} ")
                     code = None
                 logger.debug(f"API returned a 401 result and an error code: {code} ")
-                if code in [8535,]: #invalid oauth token
+                if code in [8535, ]:  # invalid oauth token
                     try:
                         self.getOAuthToken()
                     except:
                         pass
                     logger.error(f"Zoho API Recoverable error encountered (invalid oauth token), will retry")
                     if retry_countdown < 0:
                         logger.error(
                             f"Zoho API Recoverable error (invalid oauth token) exhausted retries")
-                        raise UnrecoverableRateLimitError(urlResp=respObj,zoho_error_code=code)
+                        raise UnrecoverableRateLimitError(urlResp=respObj, zoho_error_code=code)
                     else:
                         time.sleep(min(10 - retry_countdown, 1) * 10)
                         continue
-            elif (respObj.status_code in [414,]):
+            elif (respObj.status_code in [414, ]):
                 msg = f"HTTP response 414 was encountered (URI too large), no retry is attempted. {respObj.response.text} URL for {httpMethod=} {url=} {payLoad=}"
                 logger.error(msg)
-                raise BadDataError(respObj,zoho_error_code=None)
+                raise BadDataError(respObj, zoho_error_code=None)
 
-            elif (respObj.status_code in [500,]):
+            elif (respObj.status_code in [500, ]):
                 code = respObj.response.status_code
                 if ":7005" in respObj.response.text:
-                    logger.error(f"Error 7005 encountered ('unexpected error'), no retry is attempted. {respObj.response.text}")
-                    raise BadDataError(respObj,zoho_error_code=code)
+                    logger.error(
+                        f"Error 7005 encountered ('unexpected error'), no retry is attempted. {respObj.response.text}")
+                    raise BadDataError(respObj, zoho_error_code=code)
             else:
                 try:
                     response_text = respObj.response.text
                 except Exception as e:
                     response_text = "unreadable response text"
                 msg = f"Unexpected status code in from __sendRequest. Server response code is {respObj.status_code=} {response_text=}.  {url=}, {httpMethod=}, {payLoad=}, {action=} Retry attempts will be made..."
                 logger.exception(msg)
                 time.sleep(min(10 - retry_countdown, 1) * 10)
                 continue
-        #fell off while loop
-        raise RuntimeError(f"After starting with {init_retry_countdown} retries allowed, there are now no more retries left in __sendRequest.  ")
+        # fell off while loop
+        raise RuntimeError(
+            f"After starting with {init_retry_countdown} retries allowed, there are now no more retries left in __sendRequest.  ")
 
     def invalidOAUTH(self, respObj):
         """
         Internal method to check whether accesstoken expires or not.
         """
         if (respObj.status_code != 200):
             try:
@@ -504,15 +520,15 @@
         # url += "&" + payLoad
         # return self.__sendRequest(url, "POST", payLoad=None, action="ADDROW", callBackData=None)
 
         payLoad = ReportClientHelper.getAsPayLoad([columnValues, config], None, None)
         url = ReportClientHelper.addQueryParams(tableURI, self.token, "ADDROW", "XML")
         return self.__sendRequest(url, "POST", payLoad, "ADDROW", None)
 
-    def deleteData(self, tableURI, criteria=None, config=None,retry_countdown=0)->int:
+    def deleteData(self, tableURI, criteria=None, config=None, retry_countdown=0) -> int:
         """  This has been refactored to use requests.post.
         Returns the number of rows deleted
         Delete the data in the  specified table identified by the URI.
         @param tableURI: The URI of the table. See L{getURI<getURI>}.
         @type tableURI:string
         @param criteria: The criteria to be applied for deleting. Only rows matching the criteria will be
         updated. Can be C{None}. Incase it is C{None}, then all rows will be deleted.
@@ -522,15 +538,16 @@
         @raise ServerError: If the server has recieved the request but did not process the request
         due to some error.
         @raise ParseError: If the server has responded but client was not able to parse the response.
         """
         # payLoad = ReportClientHelper.getAsPayLoad([config], criteria, None)
         payload = None  # can't put the SQL in the body of the post request, the library is wrong or out of date
         url = ReportClientHelper.addQueryParams(tableURI, self.token, "DELETE", "JSON", criteria=criteria)
-        r = self.__sendRequest(url=url,httpMethod="POST",payLoad=payload,action="DELETE",callBackData=None,retry_countdown=retry_countdown)
+        r = self.__sendRequest(url=url, httpMethod="POST", payLoad=payload, action="DELETE", callBackData=None,
+                               retry_countdown=retry_countdown)
         return int(r)
 
     def updateData(self, tableURI, columnValues, criteria, config=None):
         """
         update the data in the  specified table identified by the URI.
         @param tableURI: The URI of the table. See L{getURI<getURI>}.
         @type tableURI:string
@@ -631,14 +648,20 @@
         See U{Import types<http://zohoreportsapi.wiki.zoho.com/Importing-CSV-File.html>} for more details.
         @type import_mode:string
         @param import_content: The data in csv format.
         @type import_content:string
         @param import_config: Contains any additional control parameters.
         See U{Import types<http://zohoreportsapi.wiki.zoho.com/Importing-CSV-File.html>} for more details.
         @type import_config:dictionary
+        @param matching_columns: A comma separated list of column names to match on.  If this is not provided, then the first column is used.
+        @type matching_columns:string
+        @param date_format: The Zoho date format to use.  If this is not provided, then the default is used.
+        @type date_format:string
+        @param retry_countdown: The number of retries to attempt if the API returns a recoverable error.  If this is not provided, then the default is used.
+        @type retry_countdown:int
         @return: An L{ImportResult} containing the results of the Import
         @rtype:L{ImportResult}
         @raise ServerError: If the server has received the request but did not process the request
         due to some error.
         @raise ParseError: If the server has responded but client was not able to parse the response.
         """
         date_format = date_format or "yyyy-MM-dd"
@@ -652,15 +675,16 @@
                    "ZOHO_DATE_FORMAT": date_format,
                    "ZOHO_IMPORT_DATA": import_content}
 
         if matching_columns:
             payload['ZOHO_MATCHING_COLUMNS'] = matching_columns
 
         url = ReportClientHelper.addQueryParams(tableURI, self.token, "IMPORT", "XML")
-        r = self.__sendRequest(url=url,httpMethod="POST",payLoad=payload,action="IMPORT",callBackData=None,retry_countdown=retry_countdown)
+        r = self.__sendRequest(url=url, httpMethod="POST", payLoad=payload, action="IMPORT", callBackData=None,
+                               retry_countdown=retry_countdown)
         return ImportResult(r.response)  # a parser from Zoho
 
     def importDataAsString(self, tableURI, importType, importContent, autoIdentify, onError, importConfig=None):
         """
         Bulk import data into the table identified by the URI.
         @param tableURI: The URI of the table. See L{getURI<getURI>}.
         @type tableURI:string
@@ -731,38 +755,42 @@
         the supported types.
         @type format:string
         @param exportToFileObj: File (or file like object) to which the exported data is to be written
         @type exportToFileObj:file
         @param sql: The sql whose output need to be exported.
         @type sql:string
         @param config: Contains any additional control parameters. Can be C{None}.
+
         @type config:dictionary
         @raise ServerError: If the server has received the request but did not process the request
         due to some error.
         @raise ParseError: If the server has responded but client was not able to parse the response.
+
         """
         payLoad = ReportClientHelper.getAsPayLoad([config], None, sql)
         url = ReportClientHelper.addQueryParams(tableOrReportURI, self.token, "EXPORT", format)
         return self.__sendRequest(url, "POST", payLoad, "EXPORT", exportToFileObj)
 
-    def exportDataUsingSQL_v2(self, tableOrReportURI, format, sql, config=None,retry_countdown=0) -> io.BytesIO:
+    def exportDataUsingSQL_v2(self, tableOrReportURI, format, sql, config=None, retry_countdown=0) -> io.BytesIO:
         """ This has been refactored to use requests.post
         Export the data with the  specified SQL query identified by the URI.
         @param tableOrReportURI: The URI of the database. See L{getDBURI<getDBURI>}.
         @type tableOrReportURI:string
         @param format: The format in which the data is to be exported.
         See U{Supported Export Formats<http://zohoreportsapi.wiki.zoho.com/Export.html>} for
         the supported types.
         @type format:string
         @param exportToFileObj: File (or file like object) to which the exported data is to be written
         @type exportToFileObj:file
         @param sql: The sql whose output need to be exported.
         @type sql:string
         @param config: Contains any additional control parameters. Can be C{None}.
         @type config:dictionary
+        @param retry_countdown: Number of retry attempts allowed.  If 0, no retries are attempted.
+        @type retry_countdown:int
         @raise ServerError: If the server has recieved the request but did not process the request
         due to some error.
         @raise ParseError: If the server has responded but client was not able to parse the response.
         """
 
         # this is a bug in Zoho's Python library. The SQL query must be passed as a parameter, not in the body.
         # in the body, it is ignored.
@@ -770,15 +798,16 @@
         payload = None
         """ sql does not need to URL encoded when passed in, but wrap in quotes"""
         # addQueryParams  adds parameters to the URL, not in the POST body but that seems ok for zoho..   url += "&ZOHO_ERROR_FORMAT=XML&ZOHO_ACTION=" + urllib.parse.quote(action)
         # addQueryParams adds: ZOHO_ERROR_FORMAT, ZOHO_OUTPUT_FORMAT
         url = ReportClientHelper.addQueryParams(tableOrReportURI, self.token, "EXPORT", format,
                                                 sql=sql)  # urlencoding is done in here
         callback_object = io.BytesIO()
-        r = self.__sendRequest(url=url,httpMethod="POST",payLoad=payload,action="EXPORT",callBackData=callback_object,retry_countdown=retry_countdown)
+        r = self.__sendRequest(url=url, httpMethod="POST", payLoad=payload, action="EXPORT",
+                               callBackData=callback_object, retry_countdown=retry_countdown)
         return callback_object
 
     def copyDatabase(self, dbURI, config=None):
         """
         Copy the specified database identified by the URI.
         @param dbURI: The URI of the database. See L{getDBURI<getDBURI>}.
         @type dbURI:string
@@ -790,48 +819,49 @@
         due to some error.
         @raise ParseError: If the server has responded but client was not able to parse the response.
         """
         payLoad = ReportClientHelper.getAsPayLoad([config], None, None)
         url = ReportClientHelper.addQueryParams(dbURI, self.token, "COPYDATABASE", "JSON")
         return self.__sendRequest(url, "POST", payLoad, "COPYDB", None)
 
-    def copy_workspace_api_v2(self, workspace_id, new_workspace_name, workspace_key, copy_with_data:bool,
-                      source_org_id,
-                      dest_org_id,
-                      copy_with_import_source:bool=False,
+    def copy_workspace_api_v2(self, workspace_id, new_workspace_name, workspace_key, copy_with_data: bool,
+                              source_org_id,
+                              dest_org_id,
+                              copy_with_import_source: bool = False,
 
-                      ):
+                              ):
         """
        A v2 API functions
         """
-        config_dict = {"newWorkspaceName":new_workspace_name,"newWorkspaceDesc":f"copy",
-                                                    "workspaceKey":workspace_key,
-                                                    "copyWithData":copy_with_data,
-                                                    "copyWithImportSource":copy_with_import_source}
+        config_dict = {"newWorkspaceName": new_workspace_name, "newWorkspaceDesc": f"copy",
+                       "workspaceKey": workspace_key,
+                       "copyWithData": copy_with_data,
+                       "copyWithImportSource": copy_with_import_source}
 
         config_data = "CONFIG=" + urllib.parse.quote_plus(json.dumps(config_dict))
         url = self.getURI_v2() + f"workspaces/{workspace_id}"
 
-        extra_headers = {"ZANALYTICS-ORGID": source_org_id,"ZANALYTICS-DEST-ORGID": dest_org_id}
-        return self.__sendRequest(url, "POST",payLoad=None, params=config_data, action=None,extra_headers=extra_headers)
+        extra_headers = {"ZANALYTICS-ORGID": source_org_id, "ZANALYTICS-DEST-ORGID": dest_org_id}
+        return self.__sendRequest(url, "POST", payLoad=None, params=config_data, action=None,
+                                  extra_headers=extra_headers)
 
     def get_orgs_metadata_api_v2(self):
         url = self.getURI_v2() + f"orgs/"
         return self.__sendRequest(url, "GET", payLoad=None, action=None)
 
     def get_all_workspaces_metadata_api_v2(self):
         url = self.getURI_v2() + f"workspaces/"
         return self.__sendRequest(url, "GET", payLoad=None, action=None)
 
-    def get_workspace_secretkey_api_v2(self,workspace_id, org_id):
+    def get_workspace_secretkey_api_v2(self, workspace_id, org_id):
         extra_headers = {"ZANALYTICS-ORGID": org_id, }
         url = self.getURI_v2() + f"workspaces/{workspace_id}/secretkey"
         return self.__sendRequest(url, "GET", payLoad=None, action=None, extra_headers=extra_headers)
 
-    def get_workspace_details_api_v2(self,workspace_id):
+    def get_workspace_details_api_v2(self, workspace_id):
         extra_headers = None
         url = self.getURI_v2() + f"workspaces/{workspace_id}"
         return self.__sendRequest(url, "GET", payLoad=None, action=None, extra_headers=extra_headers)
 
     def deleteDatabase(self, userURI, databaseName, config=None):
         """
         Delete the specified database.
@@ -1243,15 +1273,16 @@
         @raise ServerError: If the server has recieved the request but did not process the request
         due to some error.
         @raise ParseError: If the server has responded but client was not able to parse the response.
         """
         payload = ReportClientHelper.getAsPayLoad([config], None, None)
         url = ReportClientHelper.addQueryParams(requestURI, self.token, "DATABASEMETADATA", "JSON")
         url += "&ZOHO_METADATA=" + urllib.parse.quote(metadata)
-        r = self.__sendRequest(url=url,httpMethod="POST",payLoad=payload,action="DATABASEMETADATA",callBackData=None)
+        r = self.__sendRequest(url=url, httpMethod="POST", payLoad=payload, action="DATABASEMETADATA",
+                               callBackData=None)
         return r
 
     def getDatabaseName(self, userURI, dbid, config=None):
         """
         Get database name for a specified database identified by the URI.
         @param userURI: The URI of the user. See L{getUserURI<getUserURI>}.
         @type userURI:string
@@ -1808,14 +1839,15 @@
     def getURI_v2(self) -> str:
         """
         Returns the base URL for v2 api with trailing /
         """
         url = self.reportServerURL + "/restapi/v2/"
 
         return url
+
     def splCharReplace(self, value):
         """
         Internal method for handling special charecters in tale or database name.
         """
         value = value.replace("/", "(/)")
         value = value.replace("%5C", "(//)")
         return value
@@ -2013,50 +2045,50 @@
 
             self.trialEndDate = ReportClientHelper.getInfo(dom, "TrialEndDate", response)
             """
             The end date of the trial plan.
             @type:string
             """
 
+
 class RecoverableRateLimitError(Exception):
     """
     RatelimitError is thrown if the report server has received a ratelimit error.
     """
 
     def __init__(self, urlResp, **kwargs):
         self.httpStatusCode = urlResp.status_code  #:The http status code for the request.
         self.errorCode = self.httpStatusCode  # The error code sent by the server.
         self.uri = ""  #: The uri which threw this exception.
         self.action = ""  #:The action to be performed over the resource specified by the uri
         self.message = urlResp.content  #: Returns the message sent by the server.
         self.zoho_error_code = ""
         self.extra = kwargs
 
-
-
     def __str__(self):
         return repr(self.message)
 
+
 class UnrecoverableRateLimitError(Exception):
     """
     RatelimitError is thrown if the report server has received a ratelimit error.
     """
 
     def __init__(self, urlResp, **kwargs):
         self.httpStatusCode = urlResp.status_code  #:The http status code for the request.
         self.errorCode = self.httpStatusCode  # The error code sent by the server.
         self.uri = ""  #: The uri which threw this exception.
         self.action = ""  #:The action to be performed over the resource specified by the uri
         self.message = urlResp.content  #: Returns the message sent by the server.
         self.extra = kwargs
 
-
     def __str__(self):
         return repr(self.message)
 
+
 class ServerError(Exception):
     """
     ServerError is thrown if the report server has received the request but did not process the
     request due to some error. For example if authorization failure.
     """
 
     def __init__(self, urlResp, **kwargs):
@@ -2069,15 +2101,15 @@
         self.extra = kwargs
 
         parseable = False
         if not urlResp:
             logger.error(f"response object is None")
         else:
             try:
-                contHeader = urlResp.headers.get("Content-Type",None)
+                contHeader = urlResp.headers.get("Content-Type", None)
                 if (contHeader and contHeader.find("text/xml") > -1):
                     self.__parseErrorResponse()
             except AttributeError:
                 logger.error(f"response object is None")
 
     def __parseErrorResponse(self):
         try:
@@ -2090,14 +2122,15 @@
         except Exception as inst:
             print(inst)
             self.parseError = inst
 
     def __str__(self):
         return repr(self.message)
 
+
 class BadDataError(Exception):
     def __init__(self, urlResp, **kwargs):
         self.httpStatusCode = urlResp.status_code  #:The http status code for the request.
         self.errorCode = self.httpStatusCode  # The error code sent by the server.
         self.uri = ""  #: The uri which threw this exception.
         self.action = ""  #:The action to be performed over the resource specified by the uri
         self.message = urlResp.content  #: Returns the message sent by the server.
@@ -2166,15 +2199,15 @@
             # logger.debug(f"Note in import result: could not find result code {msg}")
             self.result_code = 0
 
         try:
             self.totalColCount = int(ReportClientHelper.getInfo(dom, "totalColumnCount", response))
         except ParseError as e:
             logger.debug(f"Error in import result: did not get a good return message: {msg}")
-            raise ParseError(responseContent=msg,message=None,origExcep=None)
+            raise ParseError(responseContent=msg, message=None, origExcep=None)
         """
         The total columns that were present in the imported file.
         @type:integer
         """
 
         self.selectedColCount = int(ReportClientHelper.getInfo(dom, "selectedColumnCount", response))
         """
@@ -2240,19 +2273,19 @@
 class ResponseObj:
     """
     Internal class.
     """
 
     def __init__(self, resp: requests.Response):
         """ updated to assume a urllib3 object"""
-        self.content = getattr(resp,'content',None)
-        self.reason = getattr(resp,'reason',None)  # This is used for communication about errors
-        self.status_code = getattr(resp,'status_code',None)
+        self.content = getattr(resp, 'content', None)
+        self.reason = getattr(resp, 'reason', None)  # This is used for communication about errors
+        self.status_code = getattr(resp, 'status_code', None)
         self.headers = {}
-        self.headers = getattr(resp,'headers',None)
+        self.headers = getattr(resp, 'headers', None)
         self.response = resp
 
 
 class ReportClientHelper:
     """
     Internal class.
     """
@@ -2300,15 +2333,15 @@
             url += "&ZOHO_CRITERIA=" + urllib.parse.quote(criteria)
         if table_design:
             # quote_plus seems to work and it makes for a smaller URL avoiding problems with a URL too long
             url += "&ZOHO_TABLE_DESIGN=" + urllib.parse.quote_plus(table_design)
         return url
 
     @staticmethod
-    def getAsPayLoad(separateDicts, criteria:Optional[str], sql:Optional[str],encode_payload=False):
+    def getAsPayLoad(separateDicts, criteria: Optional[str], sql: Optional[str], encode_payload=False):
         payload = {}
         for i in separateDicts:
             if (i != None):
                 payload.update(i)
 
         if (criteria != None):
             payload["ZOHO_CRITERIA"] = criteria
```

### Comparing `zoho_analytics_connector-1.4.2/zoho_analytics_connector.egg-info/PKG-INFO` & `zoho_analytics_connector-1.4.3/zoho_analytics_connector.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zoho-analytics-connector
-Version: 1.4.2
+Version: 1.4.3
 Summary: Zoho Analytics connector
 Home-page: https://github.com/timrichardson/zoho_analytics_connector
 Author: Tim Richardson
 Author-email: tim@growthpath.com.au
 License: MPL-2.0
 Keywords: zoho analytics
 Platform: UNKNOWN
@@ -297,17 +297,15 @@
             #get an error, but error handling is not working, the API returns a 400 with no content in the message
             r = get_enhanced_zoho_analytics_client.create_table(table_design=zoho_sales_fact_table)
             print (r)
 
 
 Changes
 -------------
-
-next_version Test updates
-
+1.4.3 Exponential backoff with jitter used for retry
 1.4.2 Added reporting_currency to enhanced_reporting_client
 1.4.1 Something seems to changed with the UTF encoding returned by the export endpoint. Change decoding to use utf-8-sig 
 1.4.0 some adaptation towards new API from Zoho
 
 1.3.6 Documentation updates, test updates. Added a 'pre-delete function' to calculate how many rows should be deleted.
     deleteData returns an int not a string for the number of rows deleted.
```

