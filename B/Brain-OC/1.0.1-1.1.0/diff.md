# Comparing `tmp/Brain-OC-1.0.1.tar.gz` & `tmp/Brain-OC-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Brain-OC-1.0.1.tar", last modified: Tue Mar 14 14:33:12 2023, max compression
+gzip compressed data, was "Brain-OC-1.1.0.tar", last modified: Sun Jul 23 21:22:29 2023, max compression
```

## Comparing `Brain-OC-1.0.1.tar` & `Brain-OC-1.1.0.tar`

### file list

```diff
@@ -1,27 +1,33 @@
-drwxrwxr-x   0 bast      (1002) bast      (1002)        0 2023-03-14 14:33:12.684303 Brain-OC-1.0.1/
-drwxrwxr-x   0 bast      (1002) bast      (1002)        0 2023-03-14 14:33:12.684303 Brain-OC-1.0.1/Brain_OC.egg-info/
--rw-rw-r--   0 bast      (1002) bast      (1002)      812 2023-03-14 14:33:12.000000 Brain-OC-1.0.1/Brain_OC.egg-info/PKG-INFO
--rw-rw-r--   0 bast      (1002) bast      (1002)      507 2023-03-14 14:33:12.000000 Brain-OC-1.0.1/Brain_OC.egg-info/SOURCES.txt
--rw-rw-r--   0 bast      (1002) bast      (1002)        1 2023-03-14 14:33:12.000000 Brain-OC-1.0.1/Brain_OC.egg-info/dependency_links.txt
--rw-rw-r--   0 bast      (1002) bast      (1002)       46 2023-03-14 14:33:12.000000 Brain-OC-1.0.1/Brain_OC.egg-info/entry_points.txt
--rw-rw-r--   0 bast      (1002) bast      (1002)       30 2023-03-14 14:33:12.000000 Brain-OC-1.0.1/Brain_OC.egg-info/requires.txt
--rw-rw-r--   0 bast      (1002) bast      (1002)        6 2023-03-14 14:33:12.000000 Brain-OC-1.0.1/Brain_OC.egg-info/top_level.txt
--rw-rw-r--   0 bast      (1002) bast      (1002)        1 2023-01-16 14:54:01.000000 Brain-OC-1.0.1/Brain_OC.egg-info/zip-safe
--rw-rw-r--   0 bast      (1002) bast      (1002)      360 2023-01-27 13:18:35.000000 Brain-OC-1.0.1/LICENSE
--rw-rw-r--   0 bast      (1002) bast      (1002)      812 2023-03-14 14:33:12.684303 Brain-OC-1.0.1/PKG-INFO
--rw-rw-r--   0 bast      (1002) bast      (1002)      213 2023-01-27 13:18:35.000000 Brain-OC-1.0.1/README.md
-drwxrwxr-x   0 bast      (1002) bast      (1002)        0 2023-03-14 14:33:12.684303 Brain-OC-1.0.1/brain/
--rw-rw-r--   0 bast      (1002) bast      (1002)    33283 2023-03-11 19:49:37.000000 Brain-OC-1.0.1/brain/__init__.py
--rw-rw-r--   0 bast      (1002) bast      (1002)     4745 2023-03-14 14:25:30.000000 Brain-OC-1.0.1/brain/__main__.py
--rw-rw-r--   0 bast      (1002) bast      (1002)     3849 2023-03-11 19:49:37.000000 Brain-OC-1.0.1/brain/access.py
-drwxrwxr-x   0 bast      (1002) bast      (1002)        0 2023-03-14 14:33:12.684303 Brain-OC-1.0.1/brain/definitions/
--rw-rw-r--   0 bast      (1002) bast      (1002)     1075 2023-01-27 13:18:35.000000 Brain-OC-1.0.1/brain/definitions/db_host.json
--rw-rw-r--   0 bast      (1002) bast      (1002)      787 2023-01-27 13:18:35.000000 Brain-OC-1.0.1/brain/definitions/group.json
--rw-rw-r--   0 bast      (1002) bast      (1002)      819 2023-01-27 13:18:35.000000 Brain-OC-1.0.1/brain/definitions/key.json
--rw-rw-r--   0 bast      (1002) bast      (1002)      837 2023-01-27 13:18:35.000000 Brain-OC-1.0.1/brain/definitions/permissions.json
--rw-rw-r--   0 bast      (1002) bast      (1002)     2802 2023-01-27 13:18:35.000000 Brain-OC-1.0.1/brain/definitions/user.json
--rw-rw-r--   0 bast      (1002) bast      (1002)      304 2023-01-27 13:18:35.000000 Brain-OC-1.0.1/brain/errors.py
--rw-rw-r--   0 bast      (1002) bast      (1002)     9967 2023-03-11 19:49:37.000000 Brain-OC-1.0.1/brain/records.py
--rw-rw-r--   0 bast      (1002) bast      (1002)     1524 2023-03-11 19:49:37.000000 Brain-OC-1.0.1/brain/users.py
--rw-rw-r--   0 bast      (1002) bast      (1002)       79 2023-03-14 14:33:12.684303 Brain-OC-1.0.1/setup.cfg
--rw-rw-r--   0 bast      (1002) bast      (1002)      928 2023-03-14 14:24:30.000000 Brain-OC-1.0.1/setup.py
+drwxrwxr-x   0 bast      (1000) bast      (1000)        0 2023-07-23 21:22:29.424156 Brain-OC-1.1.0/
+drwxrwxr-x   0 bast      (1000) bast      (1000)        0 2023-07-23 21:22:29.424156 Brain-OC-1.1.0/Brain_OC.egg-info/
+-rw-rw-r--   0 bast      (1000) bast      (1000)      815 2023-07-23 21:22:29.000000 Brain-OC-1.1.0/Brain_OC.egg-info/PKG-INFO
+-rw-rw-r--   0 bast      (1000) bast      (1000)      614 2023-07-23 21:22:29.000000 Brain-OC-1.1.0/Brain_OC.egg-info/SOURCES.txt
+-rw-rw-r--   0 bast      (1000) bast      (1000)        1 2023-07-23 21:22:29.000000 Brain-OC-1.1.0/Brain_OC.egg-info/dependency_links.txt
+-rw-rw-r--   0 bast      (1000) bast      (1000)       46 2023-07-23 21:22:29.000000 Brain-OC-1.1.0/Brain_OC.egg-info/entry_points.txt
+-rw-rw-r--   0 bast      (1000) bast      (1000)      116 2023-07-23 21:22:29.000000 Brain-OC-1.1.0/Brain_OC.egg-info/requires.txt
+-rw-rw-r--   0 bast      (1000) bast      (1000)        6 2023-07-23 21:22:29.000000 Brain-OC-1.1.0/Brain_OC.egg-info/top_level.txt
+-rw-rw-r--   0 bast      (1000) bast      (1000)        1 2023-07-19 17:54:35.000000 Brain-OC-1.1.0/Brain_OC.egg-info/zip-safe
+-rw-rw-r--   0 bast      (1000) bast      (1000)      360 2023-01-27 13:18:35.000000 Brain-OC-1.1.0/LICENSE
+-rw-rw-r--   0 bast      (1000) bast      (1000)      815 2023-07-23 21:22:29.424156 Brain-OC-1.1.0/PKG-INFO
+-rw-rw-r--   0 bast      (1000) bast      (1000)      213 2023-01-27 13:18:35.000000 Brain-OC-1.1.0/README.md
+drwxrwxr-x   0 bast      (1000) bast      (1000)        0 2023-07-23 21:22:29.424156 Brain-OC-1.1.0/brain/
+-rw-rw-r--   0 bast      (1000) bast      (1000)      296 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/__init__.py
+-rw-rw-r--   0 bast      (1000) bast      (1000)     2071 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/__main__.py
+-rw-rw-r--   0 bast      (1000) bast      (1000)     3849 2023-07-19 17:29:16.000000 Brain-OC-1.1.0/brain/access.py
+drwxrwxr-x   0 bast      (1000) bast      (1000)        0 2023-07-23 21:22:29.424156 Brain-OC-1.1.0/brain/definitions/
+-rw-rw-r--   0 bast      (1000) bast      (1000)     1075 2023-07-19 17:29:16.000000 Brain-OC-1.1.0/brain/definitions/db_host.json
+-rw-rw-r--   0 bast      (1000) bast      (1000)      787 2023-07-19 17:29:16.000000 Brain-OC-1.1.0/brain/definitions/group.json
+-rw-rw-r--   0 bast      (1000) bast      (1000)      819 2023-07-19 17:29:16.000000 Brain-OC-1.1.0/brain/definitions/key.json
+-rw-rw-r--   0 bast      (1000) bast      (1000)     1042 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/definitions/permissions.json
+-rw-rw-r--   0 bast      (1000) bast      (1000)     2802 2023-07-19 17:29:16.000000 Brain-OC-1.1.0/brain/definitions/user.json
+-rw-rw-r--   0 bast      (1000) bast      (1000)      395 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/errors.py
+-rw-rw-r--   0 bast      (1000) bast      (1000)     1366 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/install.py
+-rw-rw-r--   0 bast      (1000) bast      (1000)    10758 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/records.py
+-rw-rw-r--   0 bast      (1000) bast      (1000)     2826 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/rest.py
+-rw-rw-r--   0 bast      (1000) bast      (1000)    35916 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/service.py
+drwxrwxr-x   0 bast      (1000) bast      (1000)        0 2023-07-23 21:22:29.424156 Brain-OC-1.1.0/brain/upgrades/
+-rw-rw-r--   0 bast      (1000) bast      (1000)        0 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/upgrades/__init__.py
+-rw-rw-r--   0 bast      (1000) bast      (1000)     2598 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/brain/upgrades/v1_0_1_v1_1_0.py
+-rw-rw-r--   0 bast      (1000) bast      (1000)     1524 2023-07-19 17:29:16.000000 Brain-OC-1.1.0/brain/users.py
+-rw-rw-r--   0 bast      (1000) bast      (1000)       79 2023-07-23 21:22:29.424156 Brain-OC-1.1.0/setup.cfg
+-rw-rw-r--   0 bast      (1000) bast      (1000)     1058 2023-07-23 21:21:05.000000 Brain-OC-1.1.0/setup.py
```

### Comparing `Brain-OC-1.0.1/Brain_OC.egg-info/PKG-INFO` & `Brain-OC-1.1.0/Brain_OC.egg-info/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: Brain-OC
-Version: 1.0.1
-Summary: Brain contains a service to run users and permissions
+Version: 1.1.0
+Summary: Brain contains a service to manage users and permissions
 Home-page: https://ouroboroscoding.com/body/brain
 Author: Chris Nasr - Ouroboros Coding Inc.
 Author-email: chris@ouroboroscoding.com
 License: Custom
 Project-URL: Documentation, https://ouroboroscoding.com/body/brain
 Project-URL: Source, https://github.com/ouroboroscoding/brain
 Project-URL: Tracker, https://github.com/ouroboroscoding/brain/issues
```

### Comparing `Brain-OC-1.0.1/PKG-INFO` & `Brain-OC-1.1.0/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: Brain-OC
-Version: 1.0.1
-Summary: Brain contains a service to run users and permissions
+Version: 1.1.0
+Summary: Brain contains a service to manage users and permissions
 Home-page: https://ouroboroscoding.com/body/brain
 Author: Chris Nasr - Ouroboros Coding Inc.
 Author-email: chris@ouroboroscoding.com
 License: Custom
 Project-URL: Documentation, https://ouroboroscoding.com/body/brain
 Project-URL: Source, https://github.com/ouroboroscoding/brain
 Project-URL: Tracker, https://github.com/ouroboroscoding/brain/issues
```

### Comparing `Brain-OC-1.0.1/brain/__init__.py` & `Brain-OC-1.1.0/brain/service.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,35 @@
 # coding=utf8
 """ Brain Service
 
 Handles all Authorization / Login requests
 """
 
-__author__ = "Chris Nasr"
-__copyright__ = "Ouroboros Coding Inc."
-__version__ = "1.0.0"
-__email__ = "chris@ouroboroscoding.com"
-__created__ = "2022-08-26"
+__author__		= "Chris Nasr"
+__copyright__	= "Ouroboros Coding Inc."
+__email__		= "chris@ouroboroscoding.com"
+__created__		= "2022-08-26"
+
+# Ouroboros imports
+import body
+from config import config
+from strings import random
 
 # Python imports
-from time import time
-import uuid
+import uuid as _uuid
 
 # Pip imports
-import body
 from redis import StrictRedis
-from RestOC import	Conf, DictHelper, Record_Base, Services, Session, StrHelper
+from RestOC import DictHelper, Record_MySQL, Services, Session
 
 # Records imports
-from .records import cache as record_cache, Key, Permissions, User
+from brain.records import cache as record_cache, Key, Permissions, User
 
 # Local
-from . import access as _access, users as _users, errors
-
-# Export child modules
-access = _access
-users = _users
+from brain import access, users, errors
 
 class Brain(Services.Service):
 	"""Brain Service class
 
 	Service for authorization, sign in, sign up, permissions etc.
 	"""
 
@@ -46,15 +44,15 @@
 
 		Returns:
 			str
 		"""
 
 		# Create an instance
 		oKey = Key({
-			'_id': StrHelper.random(32, '_0x'),
+			'_id': random(32, ['0x']),
 			'user': user,
 			'type': type_
 		})
 
 		# Loop until we resolve the issue
 		while True:
 			try:
@@ -62,52 +60,56 @@
 				# Create the key record
 				oKey.create()
 
 				# Return the key
 				return oKey['_id']
 
 			# If we got a duplicate key error
-			except Record_Base.DuplicateException as e:
+			except Record_MySQL.DuplicateException as e:
 
 				# If the primary key is the duplicate
 				if 'PRIMARY' in e.args[1]:
 
 					# Generate a new key and try again
-					oKey['_id'] = StrHelper.random(32, '_0x')
+					oKey['_id'] = random(32, ['0x'])
 					continue
 
 				# Else, the type has already been used for the user
 				else:
 
-					# Find the existing key
-					dKey = Key.filter({'user': user, 'type': type_}, raw=['_id'], limit=1)
-					return dKey['_id']
+					# Find and return the existing key
+					return Key.filter({
+						'user': user,
+						'type': type_
+					}, raw=['_id'], limit=1)['_id']
 
 	@classmethod
-	def _verify(cls, user, name, right):
+	def _verify(cls, _id, name, right):
 		"""Verify
 
-		Checks the user currently in the session has access to the requested
+		Checks the user currently in the session has access to the requested \
 		permission
 
 		Arguments:
-			user (str): The ID of the user
+			_id (tuple): The user ID and portal of the permissions
 			name (str): The name of the permission to check
 			right (uint): The specific right on the permission to verify
 
 		Returns:
 			bool
 		"""
 
 		# Find the permissions
-		dPermissions = Permissions.get(user, raw=True)
+		dPermissions = Permissions.get(_id, raw=True)
 
-		# If the user has no permissions at all
+		# If there's no such permissions
 		if not dPermissions:
-			return False
+			raise Services.ResponseException(
+				error=(errors.BAD_PORTAL, _id[1])
+			)
 
 		# If one permission was requested
 		if isinstance(name, str):
 
 			# If we don't have it
 			if name not in dPermissions['rights']:
 				return False
@@ -126,15 +128,18 @@
 
 			# Else, return failure
 			else:
 				return False
 
 		# Else, invalid name data
 		else:
-			raise Services.ResponseException(error=(body.errors.DATA_FIELDS, [['name', 'invalid, must be string or string[]']]))
+			raise Services.ResponseException(error=(
+				body.errors.DATA_FIELDS,
+				[['name', 'invalid, must be string or string[]']]
+			))
 
 		# If one right was requested
 		if isinstance(right, int):
 
 			# If the permission doesn't contain the requested right
 			if not dPermissions['rights'][sName] & right:
 				return False
@@ -149,36 +154,39 @@
 
 			# Else, no rights matched
 			else:
 				return False
 
 		# Else, invalid right data
 		else:
-			raise Services.ResponseException(error=(body.errors.DATA_FIELDS, [['right', 'invalid, must be int or int[]']]))
+			raise Services.ResponseException(error=(
+				body.errors.DATA_FIELDS,
+				[['right', 'invalid, must be int or int[]']]
+			))
 
 		# Seems ok
 		return True
 
 	def initialise(self):
 		"""Initialise
 
 		Initialises the instance and returns itself for chaining
 
 		Returns:
 			Authorization
 		"""
 
 		# Get config
-		self._conf = Conf.get('brain', {
+		self._conf = config.brain({
 			'user_default_locale': 'en-US',
 			'redis_host': 'brain'
 		})
 
 		# Create a connection to Redis
-		self._redis = StrictRedis(**Conf.get(('redis', self._conf['redis_host']), {
+		self._redis = StrictRedis(**config.redis[self._conf['redis_host']]({
 			'host': 'localhost',
 			'port': 6379,
 			'db': 0
 		}))
 
 		# Pass the Redis connection to the records
 		record_cache(self._redis)
@@ -188,151 +196,216 @@
 
 	def permissions_read(self, req):
 		"""Permissions read
 
 		Returns all permissions associated with a user
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# If the user is missing
 		if 'user' not in req['data']:
-			return Services.Error(body.errors.DATA_FIELDS, [['user', 'missing']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['user', 'missing']]
+			)
 
 		# If this is an internal request
 		if '_internal_' in req['data']:
 
 			# Verify the key, remove it if it's ok
 			if not Services.internal_key(req['data']['_internal_']):
-				raise Services.ResponseException(error=body.errors.SERVICE_INTERNAL_KEY)
+				raise Services.ResponseException(
+					error=body.errors.SERVICE_INTERNAL_KEY
+				)
 			del req['data']['_internal_']
 
 		# Else, check permissions
 		else:
-			if not self._verify(req['session']['user']['_id'], 'brain_permission', access.READ):
+			if not self._verify(
+				(req['session']['user']['_id'], req['session']['portal']),
+				'brain_permission',
+				access.READ
+			):
 				return Services.Error(body.errors.RIGHTS)
 
 		# Fetch the Permissions
-		dPermissions = Permissions.get(req['data']['user'], raw=True)
+		dPermissions = Permissions.filter({
+			'user': req['data']['user']
+		}, raw=True)
 
 		# Return all permissions
 		return Services.Response(dPermissions)
 
 	def permissions_update(self, req):
 		"""Permissions update
 
 		Updates the permissions for a single user
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Check minimum fields
 		try: DictHelper.eval(req['data'], ['user', 'rights'])
 		except ValueError as e: return Services.Error(body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args])
 
+		# If the portal wasn't passed
+		if 'portal' not in req['data']:
+			req['data']['portal'] = ''
+
 		# If this is an internal request
 		if '_internal_' in req['data']:
 
 			# Verify the key, remove it if it's ok
 			if not Services.internal_key(req['data']['_internal_']):
-				raise Services.ResponseException(error=body.errors.SERVICE_INTERNAL_KEY)
+				raise Services.ResponseException(
+					error=body.errors.SERVICE_INTERNAL_KEY
+				)
 			del req['data']['_internal_']
 
 			# Store the user ID as the system user
 			sSessionUser = users.SYSTEM_USER_ID
 
 		# Else, check permissions
 		else:
 
 			# Verify the rights
-			if not self._verify(req['session']['user']['_id'], 'brain_permission', access.UPDATE):
+			if not self._verify(
+				(req['session']['user']['_id'], req['session']['portal']),
+				'brain_permission',
+				access.UPDATE
+			):
 				return Services.Error(body.errors.RIGHTS)
 
 			# Store the user ID
 			sSessionUser = req['session']['user']['_id']
 
 		# If the user doesn't exist
 		if not User.exists(req['data']['user']):
-			return Services.Error(body.errors.DB_NO_RECORD, (req['data']['user'], 'user'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, [req['data']['user'], 'user']
+			)
 
 		# Find the permissions
-		oPermissions = Permissions.get(req['data']['user'])
+		oPermissions = Permissions.get(
+			(req['data']['user'], req['data']['portal'])
+		)
+
+		# If they don't exist
 		if not oPermissions:
-			return Services.Error(body.errors.DB_NO_RECORD, (req['data']['user'], 'permissions'))
 
-		# Try to set the new permissions
-		try:
-			oPermissions['rights'] = req['data']['rights']
-		except ValueError as e:
-			return Services.Error(body.errors.DATA_FIELDS, (e.args[0]))
+			# If the user doesn't exist
+			if not User.exists(req['data']['user']):
+				return Services.Error(
+					body.errors.DB_NO_RECORD,
+					[req['data']['user'], 'user']
+				)
+
+			# Test the new record
+			try:
+				oPermissions = Permissions({
+					'user': req['data']['user'],
+					'portal': req['data']['portal'],
+					'rights': req['data']['rights']
+				})
+			except ValueError as e:
+				return Services.Error(body.errors.DATA_FIELDS, e.args[0])
 
-		# Save the permissions
-		bSave = oPermissions.save(changes={'user': sSessionUser})
+			# Create the record
+			bRes = oPermissions.create(changes={'user': sSessionUser})
 
-		# Clear the cache
-		if bSave:
-			Permissions.clear(req['data']['user'])
+		# Else, we are updating
+		else:
+
+			# Try to set the new permissions
+			try:
+				oPermissions['rights'] = req['data']['rights']
+			except ValueError as e:
+				return Services.Error(body.errors.DATA_FIELDS, (e.args[0]))
+
+			# Save the permissions
+			bRes = oPermissions.save(changes={'user': sSessionUser})
+
+			# Clear the cache
+			if bRes:
+				Permissions.clear(
+					(req['data']['user'], req['data']['portal'])
+				)
 
 		# Return the result
-		return Services.Response(bSave)
+		return Services.Response(bRes)
 
 	def permissions_add_create(self, req):
 		"""Permissions Add create
 
 		Addes a specific permission type to existing permissions
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Check minimum fields
 		try: DictHelper.eval(req['data'], ['user', 'rights'])
 		except ValueError as e: return Services.Error(body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args])
 
+		# If the portal wasn't passed
+		if 'portal' not in req['data']:
+			req['data']['portal'] = ''
+
 		# If this is an internal request
 		if '_internal_' in req['data']:
 
 			# Verify the key, remove it if it's ok
 			access.internal(req['data'])
 
 			# Store the user ID as the system user
 			sSessionUser = users.SYSTEM_USER_ID
 
 		# Else, check permissions
 		else:
 
 			# Verify the rights
-			if not self._verify(req['session']['user']['_id'], 'brain_permission', access.UPDATE):
+			if not self._verify(
+				(req['session']['user']['_id'], req['session']['portal']),
+				'brain_permission',
+				access.UPDATE
+			):
 				return Services.Error(body.errors.RIGHTS)
 
 			# Store the user ID
 			sSessionUser = req['session']['user']['_id']
 
 		# If the user doesn't exist
 		if not User.exists(req['data']['user']):
-			return Services.Error(body.errors.DB_NO_RECORD, [req['data']['user'], 'user'])
+			return Services.Error(
+				body.errors.DB_NO_RECORD, [req['data']['user'], 'user']
+			)
 
 		# Find the permissions
-		oPermissions = Permissions.get(req['data']['user'])
+		oPermissions = Permissions.get(
+			(req['data']['user'], req['data']['portal'])
+		)
 		if not oPermissions:
-			return Services.Error(body.errors.DB_NO_RECORD, [req['data']['user'], 'permissions'])
+			return Services.Error(
+				body.errors.DB_NO_RECORD,
+				[req['data']['user'], req['data']['portal'], 'permissions']
+			)
 
 		# Combine the rights
 		dRights = DictHelper.combine(oPermissions['rights'], req['data']['rights'])
 
 		# Try to update the permissions
 		try:
 			oPermissions['rights'] = dRights
@@ -346,120 +419,153 @@
 
 	def search_read(self, req):
 		"""Search
 
 		Looks up users by search / query
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Check permissions
-		self._verify(req['session']['user']['_id'], 'brain_user', access.READ)
+		self._verify(
+			(req['session']['user']['_id'], req['session']['portal']),
+			'brain_user',
+			access.READ
+		)
 
 		# Check for filter
 		if 'filter' not in req['data']:
-			return Services.Error(body.errors.DATA_FIELDS, [['filter', 'missing']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['filter', 'missing']]
+			)
 
 		# If the filter isn't a dict
 		if not isinstance(req['data']['filter'], dict):
-			return Services.Error(body.errors.DATA_FIELDS, [['filter', 'must be an object']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['filter', 'must be an object']]
+			)
 
 		# If fields is not a list
-		if 'fields' in req['data'] and not isinstance(req['data']['fields'], list):
-			return Services.Error(body.errors.DATA_FIELDS, [['fields', 'must be a list']])
+		if 'fields' in req['data'] and \
+			not isinstance(req['data']['fields'], list):
+
+			# Return an error
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['fields', 'must be a list']]
+			)
 
 		# Search based on the req['data'] passed
-		lRecords = [d['_id'] for d in User.search(req['data']['filter'], raw=['_id'])]
+		lRecords = [
+			d['_id'] \
+			for d in User.search(req['data']['filter'], raw=['_id'])
+		]
 
 		# If we got something, fetch the records from the cache
 		if lRecords:
-			lRecords = User.cache(lRecords, raw=('fields' in req['data'] and req['data']['fields'] or True))
+			lRecords = User.cache(
+				lRecords,
+				raw=('fields' in req['data'] and req['data']['fields'] or True)
+			)
 
 		# Remove the passwd
 		for d in lRecords:
 			del d['passwd']
 
 		# Return the results
 		return Services.Response(lRecords)
 
 	def session_read(self, req):
 		"""Session
 
 		Returns the ID of the user logged into the current session
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 		return Services.Response({
 			'user' : {
 				'_id': req['session']['user']['_id']
-			}
+			},
+			'portal': req['session']['portal']
 		})
 
 	def signin_create(self, req):
 		"""Signin
 
 		Signs a user into the system
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Result
 		"""
 
 		# Check minimum fields
 		try: DictHelper.eval(req['data'], ['email', 'passwd'])
-		except ValueError as e: return Services.Error(body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args])
+		except ValueError as e:
+			return Services.Error(
+				body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args]
+			)
 
 		# Look for the user by alias
 		oUser = User.filter({'email': req['data']['email']}, limit=1)
 		if not oUser:
 			return Services.Error(errors.SIGNIN_FAILED)
 
 		# If it's the system user, reject it
 		if oUser['_id'] == users.SYSTEM_USER_ID:
 			return Services.Error(errors.SIGNIN_FAILED)
 
 		# Validate the password
 		if not oUser.password_validate(req['data']['passwd']):
 			return Services.Error(errors.SIGNIN_FAILED)
 
+		# Check if the user has permissions in the given portal
+		mPortal = 'portal' in req['data'] and req['data']['portal'] or ''
+		dPerms = Permissions.get((oUser['_id'], mPortal), raw=['user'])
+
+		# If we don't have permissions for the given portal
+		if not dPerms:
+			return Services.Error(errors.BAD_PORTAL, mPortal)
+
 		# Create a new session
-		oSesh = Session.create('sesh:%s' % uuid.uuid4().hex)
+		oSesh = Session.create('sesh:%s' % _uuid.uuid4().hex)
 
-		# Store the user ID and information in it
+		# Store the user ID and portal in th session
 		oSesh['user'] = {'_id': oUser['_id']}
+		oSesh['portal'] = mPortal
 
 		# Save the session
 		oSesh.save()
 
 		# Return the session ID and primary user data
 		return Services.Response({
 			'session': oSesh.id(),
-			'user': oSesh['user']
+			'user': oSesh['user'],
+			'portal': oSesh['portal']
 		})
 
 	def signout_create(self, req):
 		"""Signout
 
 		Called to sign out a user and destroy their session
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Close the session so it can no longer be found/used
@@ -471,41 +577,56 @@
 
 	def user_create(self, req):
 		"""User Create
 
 		Creates a new user
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Check permissions
-		self._verify(req['session']['user']['_id'], 'brain_user', access.CREATE)
+		self._verify(
+			(req['session']['user']['_id'], req['session']['portal']),
+			'brain_user',
+			access.CREATE
+		)
 
 		# Check minimum fields
 		try: DictHelper.eval(req['data'], ['email', 'url'])
-		except ValueError as e: return Services.Error(body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args])
+		except ValueError as e:
+			return Services.Error(
+				body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args]
+			)
 
 		# Make sure the URL has the {key} field
 		if '{key}' not in req['data']['url']:
-			return Services.Error(body.errors.DATA_FIELDS, [['url', 'missing {key}']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['url', 'missing {key}']]
+			)
+
+		# If the portal is not passed
+		if 'portal' not in req['data']:
+			req['data']['portal'] = ''
 
 		# Pop off the URL
 		sURL = req['data'].pop('url')
 
 		# Strip leading and trailing spaces on the email
 		req['data']['email'] = req['data']['email'].strip()
 
 		# Make sure the email is valid structurally
 		if not body.regex.EMAIL_ADDRESS.match(req['data']['email']):
-			return Services.Error(body.errors.DATA_FIELDS, [['email', 'invalid']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['email', 'invalid']]
+			)
 
 		# Check if a user with that email already exists
 		sExistingUserID = User.exists(req['data']['email'], 'email')
 		if sExistingUserID:
 			return Services.Error(body.errors.DB_DUPLICATE, sExistingUserID)
 
 		# Add the blank password
@@ -521,22 +642,19 @@
 		# Validate by creating a Record instance
 		try:
 			oUser = User(req['data'])
 		except ValueError as e:
 			return Services.Error(body.errors.DATA_FIELDS, e.args[0])
 
 		# Create the record
-		sID = oUser.create(changes={'user': req['session'] and req['session']['user']['_id'] or users.SYSTEM_USER_ID})
-
-		# Create empty permissions
-		oPermissions = Permissions({
-			'_user': sID,
-			'rights': {}
+		sID = oUser.create(changes={
+			'user': req['session'] and \
+						req['session']['user']['_id'] or \
+						users.SYSTEM_USER_ID
 		})
-		oPermissions.create(changes={'user': req['session'] and req['session']['user']['_id'] or users.SYSTEM_USER_ID})
 
 		# If the record was created
 		if sID:
 
 			# Create key for setup validation
 			sSetupKey = self._create_key(oUser['_id'], 'setup')
 
@@ -562,94 +680,118 @@
 
 	def user_read(self, req):
 		"""User Read
 
 		Fetches an existing user and returns their data
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# If there's an ID, check permissions
 		if 'data' in req and '_id' in req['data']:
-			self._verify(req['session']['user']['_id'], 'brain_user', access.READ)
+			self._verify(
+				(req['session']['user']['_id'], req['session']['portal']),
+				'brain_user',
+				access.READ
+			)
 
 		# Else, assume the signed in user's Record
 		else:
 			req['data'] = {'_id': req['session']['user']['_id']}
 
 		# Fetch it from the cache
 		dUser = User.cache(req['data']['_id'], raw=True)
 
 		# If it doesn't exist
 		if not dUser:
-			return Services.Error(body.errors.DB_NO_RECORD, (req['data']['_id'], 'user'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, [req['data']['_id'], 'user']
+			)
 
 		# Remove the passwd
 		del dUser['passwd']
 
+		# If no portal was passed
+		if 'portal' not in req['data']:
+			req['data']['portal'] = ''
+
 		# Fetch the permissions and add them to the user
-		dPermissions = Permissions.get(req['data']['_id'], raw=['rights'])
+		dPermissions = Permissions.get(
+			(req['data']['_id'], req['data']['portal']),
+			raw=['rights']
+		)
 		dUser['permissions'] = dPermissions['rights']
 
 		# Return the user data
 		return Services.Response(dUser)
 
 	def user_update(self, req):
 		"""User Update
 
 		Updates an existing user
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# If there's an ID, check permissions
-		if '_id' in req['data'] and req['data']['_id'] != req['session']['user']['_id']:
+		if '_id' in req['data'] and \
+			req['data']['_id'] != req['session']['user']['_id']:
 
 			# If the ID isn't set
 			if not req['data']['_id']:
-				return Services.Error(body.errors.DATA_FIELDS, [['_id', 'missing']])
+				return Services.Error(
+					body.errors.DATA_FIELDS, [['_id', 'missing']]
+				)
 
 			# Make sure the user has the proper permission to do this
-			self._verify(req['session']['user']['_id'], 'brain_user', access.UPDATE)
+			self._verify(
+				(req['session']['user']['_id'], req['session']['portal']),
+				'brain_user',
+				access.UPDATE
+			)
 
 		# Else, assume the signed in user's Record
 		else:
 			req['data']['_id'] = req['session']['user']['_id']
 
 		# Fetch it from the cache
 		oUser = User.cache(req['data']['_id'])
 
 		# If the user isn't found
 		if not oUser:
-			return Services.Error(body.errors.DB_NO_RECORD, (req['data']['_id'], 'user'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, (req['data']['_id'], 'user')
+			)
 
 		# Remove fields that can't be changed
 		for k in ['_id', '_created', '_updated', 'email', 'passwd']:
 			try: del req['data'][k]
 			except KeyError: pass
 
 		# If the email was passed
 		if 'email' in req['data']:
 
 			# Strip leading and trailing spaces
 			req['data']['email'] = req['data']['email'].strip()
 
 			# Make sure it's valid structurally
 			if not body.regex.EMAIL_ADDRESS.match(req['data']['email']):
-				return Services.Error(body.errors.DATA_FIELDS, [['email', 'invalid']])
+				return Services.Error(
+					body.errors.DATA_FIELDS, [['email', 'invalid']]
+				)
 
 		# Step through each field passed and update/validate it
 		lErrors = []
 		for f in req['data']:
 			try: oUser[f] = req['data'][f]
 			except ValueError as e: lErrors.append(e.args[0])
 
@@ -669,53 +811,65 @@
 
 	def user_email_update(self, req):
 		"""User Email update
 
 		Changes the email for the current signed in user
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Check minimum fields
 		try: DictHelper.eval(req['data'], ['email', 'email_passwd', 'url'])
-		except ValueError as e: return Services.Error(body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args])
+		except ValueError as e:
+			return Services.Error(
+				body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args]
+			)
 
 		# Make sure the URL has the {key} field
 		if '{key}' not in req['data']['url']:
-			return Services.Error(body.errors.DATA_FIELDS, [['url', 'missing {key}']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['url', 'missing {key}']]
+			)
 
 		# Find the user
 		oUser = User.get(req['session']['user']['_id'])
 		if not oUser:
-			return Services.Error(body.errors.DB_NO_RECORD, (req['session']['user']['_id'], 'user'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD,
+				(req['session']['user']['_id'], 'user')
+			)
 
 		# Validate the password
 		if not oUser.password_validate(req['data']['email_passwd']):
 			return Services.Error(errors.SIGNIN_FAILED)
 
 		# If the email hasn't changed
 		if oUser['email'] == req['data']['email']:
 			return Services.Response(False)
 
 		# Strip leading and trailing spaces on email
 		req['data']['email'] = req['data']['email'].strip()
 
 		# Make sure the email is valid structurally
 		if not body.regex.EMAIL_ADDRESS.match(req['data']['email']):
-			return Services.Error(body.errors.DATA_FIELDS, [['email', 'invalid']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['email', 'invalid']]
+			)
 
 		# Look for someone else with that email
 		dUser = User.filter({'email': req['data']['email']}, raw=['_id'])
 		if dUser:
-			return Services.Error(body.errors.DB_DUPLICATE, (req['data']['email'], 'user'))
+			return Services.Error(
+				body.errors.DB_DUPLICATE, (req['data']['email'], 'user')
+			)
 
 		# Update the email and verified fields
 		try:
 			oUser['email'] = req['data']['email']
 			oUser['verified'] = False
 		except ValueError as e:
 			return Services.Error(body.errors.DATA_FIELDS, e.args[0])
@@ -760,34 +914,40 @@
 
 	def user_email_verify_update(self, req):
 		"""User Email Verify update
 
 		Marks the user/email as verified
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# If the key is not passed
 		if 'key' not in req['data']:
-			return Services.Error(body.errors.DATA_FIELDS, [['key', 'missing']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['key', 'missing']]
+			)
 
 		# Look for the key
 		oKey = Key.get(req['data']['key'])
 		if not oKey:
-			return Services.Error(body.errors.DB_NO_RECORD, (req['data']['key'], 'key'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, [req['data']['key'], 'key']
+			)
 
 		# Find the user associated with they key
 		oUser = User.get(oKey['user'])
 		if not oUser:
-			return Services.Error(body.errors.DB_NO_RECORD, (oKey['user'], 'user'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, (oKey['user'], 'user')
+			)
 
 		# Mark the user as verified and save
 		oUser['verified'] = True
 		bRes = oUser.save(changes={'user': oKey['user']})
 
 		# If the save was successful
 		if bRes:
@@ -803,99 +963,127 @@
 
 	def user_names_read(self, req):
 		"""User Names read
 
 		Returns a list or dict of IDs to names of users
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Make sure we got an ID
 		if '_id' not in req['data']:
-			return Services.Error(body.errors.DATA_FIELDS, [['_id', 'missing']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['_id', 'missing']]
+			)
 
 		# If the type is missing
 		if 'type' not in req['data'] or not req['data']['type']:
 			req['data']['type'] = 'object'
 
 		# Else, if the type is invalid
 		elif req['data']['type'] not in ['array', 'object']:
-			return Services.Error(body.errors.DATA_FIELDS, [['type', 'invalid']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['type', 'invalid']]
+			)
 
 		# If we only got one ID
 		if isinstance(req['data']['_id'], str):
 			req['data']['_id'] = [req['data']['_id']]
 
 		# If the list is empty
 		if not req['data']['_id']:
-			return Services.Error(body.errors.DATA_FIELDS, [['_id', 'empty']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['_id', 'empty']]
+			)
 
 		# If the client requested an array, return a list
 		if req['data']['type'] == 'array':
 			return Services.Response(
-				User.get(req['data']['_id'], raw=['_id', 'first_name', 'last_name'], orderby=['first_name', 'last_name'])
+				User.get(
+					req['data']['_id'],
+					raw=['_id', 'first_name', 'last_name'],
+					orderby=['first_name', 'last_name']
+				)
 			)
 
 		# Else, they requested an object, so return a dict
 		else:
 			return Services.Response({
-				d['_id']: {'first_name':d['first_name'], 'last_name':d['last_name']}
-				for d in User.get(req['data']['_id'], raw=['_id', 'first_name', 'last_name'])
+				d['_id']: {
+					'first_name': d['first_name'],
+					'last_name': d['last_name']
+				} \
+				for d in User.get(
+					req['data']['_id'],
+					raw=['_id', 'first_name', 'last_name']
+				)
 			})
 
 	def user_passwd_update(self, req):
 		"""User Password update
 
 		Changes the password for the current signed in user
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Make sure we got a new password
 		if 'new_passwd' not in req['data']:
-			return Services.Error(body.errors.DATA_FIELDS, [['new_passwd', 'missing']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['new_passwd', 'missing']]
+			)
 
 		# If the id is passed
 		if '_id' in req['data'] and req['data']['_id'] is not None:
 
 			# If it doesn't match the logged in user, check permissions
 			if req['data']['_id'] != req['session']['user']['_id']:
-				self._verify(req['session']['user']['_id'], 'brain_user', access.UPDATE)
+				self._verify(
+					(req['session']['user']['_id'], req['session']['portal']),
+					'brain_user',
+					access.UPDATE
+				)
 
 		# Else, use the user from the session
 		else:
 
 			# If the old password is missing
 			if 'passwd' not in req['data']:
-				return Services.Error(body.errors.DATA_FIELDS, [['passwd', 'missing']])
+				return Services.Error(
+					body.errors.DATA_FIELDS, [['passwd', 'missing']]
+				)
 
 			# Store the session as the user ID
 			req['data']['_id'] = req['session']['user']['_id']
 
 		# Find the user
 		oUser = User.get(req['data']['_id'])
 		if not oUser:
-			return Services.Error(body.errors.DB_NO_RECORD, (req['data']['_id'], 'user'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, (req['data']['_id'], 'user')
+			)
 
 		# If we have an old password
 		if 'passwd' in req['data']:
 
 			# Validate it
 			if not oUser.password_validate(req['data']['passwd']):
-				return Services.Error(body.errors.DATA_FIELDS, [['passwd', 'invalid']])
+				return Services.Error(
+					body.errors.DATA_FIELDS, [['passwd', 'invalid']]
+				)
 
 		# Make sure the new password is strong enough
 		if not User.password_strength(req['data']['new_passwd']):
 			return Services.Error(errors.PASSWORD_STRENGTH)
 
 		# Set the new password and save
 		oUser['passwd'] = User.password_hash(req['data']['new_passwd'])
@@ -903,35 +1091,44 @@
 
 		# Return OK
 		return Services.Response(True)
 
 	def user_passwd_forgot_create(self, req):
 		"""User Password Forgot create
 
-		Creates the key that will be used to allow a user to change their
+		Creates the key that will be used to allow a user to change their \
 		password if they forgot it
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Check minimum fields
 		try: DictHelper.eval(req['data'], ['email', 'url'])
-		except ValueError as e: return Services.Error(body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args])
+		except ValueError as e:
+			return Services.Error(
+				body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args]
+			)
 
 		# Make sure the URL has the {key} field
 		if '{key}' not in req['data']['url']:
-			return Services.Error(body.errors.DATA_FIELDS, [['url', 'missing {key}']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['url', 'missing {key}']]
+			)
 
 		# Look for the user by email
-		dUser = User.filter({'email': req['data']['email']}, raw=['_id', 'locale'], limit=1)
+		dUser = User.filter(
+			{'email': req['data']['email']},
+			raw = ['_id', 'locale'],
+			limit = 1
+		)
 		if not dUser:
 			return Services.Response(False)
 
 		# Generate a key
 		sKey = self._create_key(dUser['_id'], 'forgot')
 
 		# Forgot email template variables
@@ -959,38 +1156,45 @@
 
 	def user_passwd_forgot_update(self, req):
 		"""User Password Forgot update
 
 		Validates the key and changes the password to the given value
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Check minimum fields
 		try: DictHelper.eval(req['data'], ['passwd', 'key'])
-		except ValueError as e: return Services.Error(body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args])
+		except ValueError as e:
+			return Services.Error(
+				body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args]
+			)
 
 		# Look up the key
 		oKey = Key.get(req['data']['key'])
 		if not oKey:
-			return Services.Error(body.errors.DB_NO_RECORD, (req['data']['key'], 'key'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, (req['data']['key'], 'key')
+			)
 
 		# Make sure the new password is strong enough
 		if not User.password_strength(req['data']['passwd']):
 			return Services.Error(errors.PASSWORD_STRENGTH)
 
 		# Find the User
 		oUser = User.get(oKey['user'])
 		if not oUser:
-			return Services.Error(body.errors.DB_NO_RECORD, (oKey['user'], 'user'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, (oKey['user'], 'user')
+			)
 
 		# Store the new password, mark verified, and update
 		oUser['passwd'] = User.password_hash(req['data']['passwd'])
 		oUser['verified'] = True
 		oUser.save(changes=False)
 
 		# Delete the key
@@ -1001,70 +1205,83 @@
 
 	def user_setup_read(self, req):
 		"""User Setup read
 
 		Validates the key exists and returns the user's info
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# If the key is missing
 		if 'key' not in req['data']:
-			return Services.Error(body.errors.DATA_FIELDS, [['key', 'missing']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['key', 'missing']]
+			)
 
 		# Look up the key
 		dKey = Key.get(req['data']['key'], raw=True)
 		if not dKey:
-			return Services.Error(body.errors.DB_NO_RECORD, (req['data']['key'], 'key'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, (req['data']['key'], 'key')
+			)
 
 		# Get the user
 		dUser = User.get(dKey['user'], raw=True)
 		if not dUser:
-			return Services.Error(body.errors.DB_NO_RECORD, (dKey['user'], 'user'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, (dKey['user'], 'user')
+			)
 
 		# Delete unnecessary fields
 		for k in ['_id', '_created', '_updated', 'passwd', 'verified']:
 			del dUser[k]
 
 		# Return the user
 		return Services.Response(dUser)
 
 	def user_setup_update(self, req):
 		"""User Setup update
 
-		Finishes setting up the account for the user by setting their password
+		Finishes setting up the account for the user by setting their password \
 		and verified fields
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Verify the minimum fields
 		try: DictHelper.eval(req['data'], ['passwd', 'key'])
-		except ValueError as e: return Services.Error(body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args])
+		except ValueError as e:
+			return Services.Error(
+				body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args]
+			)
 
 		# Look up the key
 		oKey = Key.get(req['data']['key'])
 		if not oKey:
-			return Services.Error(body.errors.DB_NO_RECORD, (req['data']['key'], 'key'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, (req['data']['key'], 'key')
+			)
 		req['data'].pop('key')
 
 		# Find the user
 		oUser = User.get(oKey['user'])
 		if not oUser:
-			return Services.Error(body.errors.DB_NO_RECORD, (oKey['user'], 'user'))
+			return Services.Error(
+				body.errors.DB_NO_RECORD, (oKey['user'], 'user')
+			)
 
 		# Make sure the new password is strong enough
 		if not User.password_strength(req['data']['passwd']):
 			return Services.Error(errors.PASSWORD_STRENGTH)
 
 		# Pop off the password
 		sPassword = req['data'].pop('passwd')
@@ -1081,29 +1298,32 @@
 		oUser['passwd'] = User.password_hash(sPassword)
 		oUser['verified'] = True
 		oUser.save(changes={'user': oKey['user']})
 
 		# Delete the key
 		oKey.delete()
 
-		# Create a new session, store the user ID, and save it
+		# Create a new session, store the user ID and portal, and save it
 		oSesh = Session.create()
 		oSesh['user'] = {'_id': oUser['_id']}
+		oSesh['portal'] = 'portal' in req['data'] and \
+							req['data']['portal'] or \
+							''
 		oSesh.save()
 
 		# Return the session ID
 		return Services.Response(oSesh.id())
 
 	def users_by_email_read(self, req):
 		"""Users By E-Mail read
 
 		Finds a user given their unique email address
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# If this is an internal request
@@ -1115,61 +1335,76 @@
 			# Store the user ID as the system user
 			sSessionUser = users.SYSTEM_USER_ID
 
 		# Else, check permissions
 		else:
 
 			# Verify the rights
-			if not self._verify(req['session']['user']['_id'], 'brain_user', access.READ):
+			if not self._verify(
+				(req['session']['user']['_id'], req['session']['portal']),
+				'brain_user',
+				access.READ
+			):
 				return Services.Error(body.errors.RIGHTS)
 
 			# Store the user ID
 			sSessionUser = req['session']['user']['_id']
 
 		# If we are missing the ID
 		if 'email' not in req['data']:
-			return Services.Error(body.errors.DATA_FIELDS, [['email', 'missing']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['email', 'missing']]
+			)
 
 		# If the fields are passed
 		if 'fields' in req['data']:
 
 			# If it's not a list
 			if not isinstance(req['data']['fields'], list):
-				return Services.Error(body.errors.DATA_FIELDS, [['fields', 'must be an array']])
+				return Services.Error(
+					body.errors.DATA_FIELDS, [['fields', 'must be an array']]
+				)
 
 		# Else, set default fields
 		else:
 			req['data']['fields'] = ['_id', 'email', 'first_name', 'last_name']
 
 		# If the order is passed
 		if 'order' in req['data']:
 
 			# If it's not a list
 			if not isinstance(req['data']['order'], list):
-				return Services.Error(body.errors.DATA_FIELDS, [['order', 'must be an array']])
+				return Services.Error(
+					body.errors.DATA_FIELDS, [['order', 'must be an array']]
+				)
 
 		# Else, set default fields
 		else:
 			req['data']['order'] = ['first_name', 'last_name']
 
 		# If we only got one email
 		mLimit = isinstance(req['data']['email'], str) and 1 or None
 
 		# Find and return the user(s)
 		return Services.Response(
-			User.get(req['data']['email'], index='email', raw=req['data']['fields'], orderby=req['data']['order'], limit=mLimit)
+			User.filter(
+				{ 'email': req['data']['email'] },
+				raw=req['data']['fields'],
+				orderby=req['data']['order'],
+				limit=mLimit
+			)
 		)
 
 	def users_by_id_read(self, req):
 		"""Users By ID read
 
 		Finds all users with a specific id
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# If this is an internal request
@@ -1181,70 +1416,84 @@
 			# Store the user ID as the system user
 			sSessionUser = users.SYSTEM_USER_ID
 
 		# Else, check permissions
 		else:
 
 			# Verify the rights
-			if not self._verify(req['session']['user']['_id'], 'brain_user', access.READ):
+			if not self._verify(
+				(req['session']['user']['_id'], req['session']['portal']),
+				'brain_user',
+				access.READ
+			):
 				return Services.Error(body.errors.RIGHTS)
 
 			# Store the user ID
 			sSessionUser = req['session']['user']['_id']
 
 		# If we are missing the ID
 		if '_id' not in req['data']:
-			return Services.Error(body.errors.DATA_FIELDS, [['_id', 'missing']])
+			return Services.Error(
+				body.errors.DATA_FIELDS, [['_id', 'missing']]
+			)
 
 		# If the fields are passed
 		if 'fields' in req['data']:
 
 			# If it's not a list
 			if not isinstance(req['data']['fields'], list):
-				return Services.Error(body.errors.DATA_FIELDS, [['fields', 'must be an array']])
+				return Services.Error(
+					body.errors.DATA_FIELDS, [['fields', 'must be an array']]
+				)
 
 		# Else, set default fields
 		else:
 			req['data']['fields'] = ['_id', 'email', 'first_name', 'last_name']
 
 		# If the order is passed
 		if 'order' in req['data']:
 
 			# If it's not a list
 			if not isinstance(req['data']['order'], list):
-				return Services.Error(body.errors.DATA_FIELDS, [['order', 'must be an array']])
+				return Services.Error(
+					body.errors.DATA_FIELDS, [['order', 'must be an array']]
+				)
 
 		# Else, set default fields
 		else:
 			req['data']['order'] = ['first_name', 'last_name']
 
 		# Find and return the users
 		return Services.Response(
-			User.get(req['data']['_id'], raw=req['data']['fields'], orderby=req['data']['order'])
+			User.get(
+				req['data']['_id'],
+				raw=req['data']['fields'],
+				orderby=req['data']['order']
+			)
 		)
 
 	def verify_read(self, req):
 		"""Verify read
 
 		Checks the user currently in the session has access to the requested
 		permission
 
 		Arguments:
-			req (dict): The request details, which can include 'data',
+			req (dict): The request details, which can include 'data', \
 						'environment', and 'session'
 
 		Returns:
 			Services.Response
 		"""
 
 		# Check minimum fields
 		try: DictHelper.eval(req['data'], ['name', 'right'])
 		except ValueError as e: return Services.Error(body.errors.DATA_FIELDS, [[f, 'missing'] for f in e.args])
 
 		# Verify and return the result
 		return Services.Response(
 			self._verify(
-				req['session']['user']['_id'],
+				(req['session']['user']['_id'], req['session']['portal']),
 				req['data']['name'],
 				req['data']['right']
 			)
 		)
```

### Comparing `Brain-OC-1.0.1/brain/access.py` & `Brain-OC-1.1.0/brain/access.py`

 * *Files identical despite different names*

### Comparing `Brain-OC-1.0.1/brain/definitions/db_host.json` & `Brain-OC-1.1.0/brain/definitions/db_host.json`

 * *Files identical despite different names*

### Comparing `Brain-OC-1.0.1/brain/definitions/group.json` & `Brain-OC-1.1.0/brain/definitions/group.json`

 * *Files identical despite different names*

### Comparing `Brain-OC-1.0.1/brain/definitions/key.json` & `Brain-OC-1.1.0/brain/definitions/key.json`

 * *Files identical despite different names*

### Comparing `Brain-OC-1.0.1/brain/definitions/permissions.json` & `Brain-OC-1.1.0/brain/definitions/permissions.json`

 * *Files 23% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.5486111111111112%*

 * *Differences: {"'__sql__'": "{'create': {insert: [(2, 'user'), (3, 'portal')], delete: [0]}, 'indexes': "*

 * *              "{replace: OrderedDict([('u_user_portal', ['user', 'portal'])])}, 'primary': '_id'}",*

 * * "'_id'": "OrderedDict([('__type__', 'uuid'), ('__optional__', True)])",*

 * * "'portal'": "OrderedDict([('__type__', 'string'), ('__maximum__', 16), ('__sql__', "*

 * *             "OrderedDict([('type', 'char(16)')]))])",*

 * * "'user'": "OrderedDict([('__type__', 'uuid')])",*

 * * 'delete': "['_user']"}*

```diff
@@ -4,48 +4,65 @@
         "auto_primary": "UUID()",
         "changes": [
             "user"
         ],
         "charset": "utf8mb4",
         "collate": "utf8mb4_bin",
         "create": [
-            "_user",
             "_created",
             "_updated",
+            "user",
+            "portal",
             "rights"
         ],
         "db": "brain",
         "host": "brain",
-        "indexes": {},
-        "primary": "_user",
+        "indexes": {
+            "u_user_portal": [
+                "user",
+                "portal"
+            ]
+        },
+        "primary": "_id",
         "table": "brain_permissions"
     },
     "_created": {
         "__optional__": true,
         "__sql__": {
             "opts": "default CURRENT_TIMESTAMP"
         },
         "__type__": "timestamp"
     },
+    "_id": {
+        "__optional__": true,
+        "__type__": "uuid"
+    },
     "_updated": {
         "__optional__": true,
         "__sql__": {
             "opts": "default CURRENT_TIMESTAMP on update CURRENT_TIMESTAMP"
         },
         "__type__": "timestamp"
     },
-    "_user": {
-        "__type__": "uuid"
+    "portal": {
+        "__maximum__": 16,
+        "__sql__": {
+            "type": "char(16)"
+        },
+        "__type__": "string"
     },
     "rights": {
         "__hash__": {
             "__regex__": "[a-z_]+",
             "__type__": "string"
         },
         "__maximum__": 15,
         "__minimum__": 1,
         "__sql__": {
             "json": true
         },
         "__type__": "uint"
+    },
+    "user": {
+        "__type__": "uuid"
     }
 }
```

### Comparing `Brain-OC-1.0.1/brain/definitions/user.json` & `Brain-OC-1.1.0/brain/definitions/user.json`

 * *Files identical despite different names*

### Comparing `Brain-OC-1.0.1/brain/records.py` & `Brain-OC-1.1.0/brain/records.py`

 * *Files 6% similar despite different names*

```diff
@@ -6,22 +6,28 @@
 
 __author__		= "Chris Nasr"
 __version__		= "1.0.0"
 __maintainer__	= "Chris Nasr"
 __email__		= "chris@ouroboroscoding.com"
 __created__		= "2022-03-20"
 
+# Ouroboros imports
+from config import config
+import jsonb
+from strings import random
+
 # Python imports
 from hashlib import sha1
 import re
 import pathlib
+from typing import Literal
 
 # Pip imports
 from FormatOC import Tree
-from RestOC import Conf, JSON, Record_MySQL, StrHelper
+from RestOC import Record_MySQL
 
 # Module variable
 _moRedis = None
 
 # Get the definitions path
 _defPath = '%s/definitions' % pathlib.Path(__file__).parent.resolve()
 
@@ -76,15 +82,15 @@
 			dict
 		"""
 
 		# If we haven't loaded the config yet
 		if not cls._conf:
 			cls._conf = Record_MySQL.Record.generate_config(
 				Tree.fromFile('%s/key.json' % _defPath),
-				override={'db': Conf.get(('mysql', 'db'), 'brain')}
+				override={'db': config.mysql.db('brain')}
 			)
 
 		# Return the config
 		return cls._conf
 
 class Permissions(Record_MySQL.Record):
 	"""Permissions
@@ -94,29 +100,35 @@
 	Extends:
 		Record_MySQL.Record
 	"""
 
 	_conf = None
 	"""Configuration"""
 
+	_key = 'perms:%s%s'
+	"""The template used to generate the cache keys"""
+
 	@classmethod
 	def clear(cls, _id):
 		"""Clear
 
 		Removes permissions from the cache by ID
 
 		Arguments:
 			_id (str): The ID of the user to remove
 
 		Returns:
 			None
 		"""
 
 		# Delete the key in Redis
-		_moRedis.delete('perms:%s' % _id)
+		_moRedis.delete(cls._key % (
+			_id[0],
+			_id[1] and _id[1] or ''
+		))
 
 	@classmethod
 	def config(cls):
 		"""Config
 
 		Returns the configuration data associated with the record type
 
@@ -124,32 +136,43 @@
 			dict
 		"""
 
 		# If we haven't loaded the config yet
 		if not cls._conf:
 			cls._conf = Record_MySQL.Record.generate_config(
 				Tree.fromFile('%s/permissions.json' % _defPath),
-				override={'db': Conf.get(('mysql', 'db'), 'brain')}
+				override={'db': config.mysql.db('brain')}
 			)
 
 		# Return the config
 		return cls._conf
 
 	@classmethod
-	def get(cls, _id=None, index=None, filter=None, match=None, raw=None, distinct=False, orderby=None, limit=None, custom={}):
+	def get(cls,
+		_id: tuple | list[tuple] = None,
+		index: str = None,
+		filter: dict = None,
+		match: None = None,
+		raw: Literal[True] | list[str] = None,
+		distinct: bool = False,
+		orderby: str | list[str] = None,
+		limit: int | tuple = None,
+		custom: dict = {}
+	):
 		"""Get
 
-		Returns records by primary key or index, can also be given an extra filter
+		Returns records by primary key or index, can also be given an extra \
+		filter
 
 		Arguments:
-			_id (str|str[]): The primary key(s) to fetch from the table
+			_id (tuple|tuple[]): The primary key(s) to fetch from the table
 			index (str): N/A in MySQL
 			filter (dict): Additional filter
 			match (tuple): N/A in MySQL
-			raw (bool|list): Return raw data (dict) for all or a set list of
+			raw (bool|list): Return raw data (dict) for all or a set list of \
 				fields
 			distinct (bool): Only return distinct data
 			orderby (str|str[]): A field or fields to order the results by
 			limit (int|tuple): The limit and possible starting point
 			custom (dict): Custom Host and DB info
 				'host' the name of the host to get/set data on
 				'append' optional postfix for dynamic DBs
@@ -163,89 +186,115 @@
 		# If we have an ID
 		if _id:
 
 			# If we have no index
 			if not index:
 
 				# If we have one ID
-				if isinstance(_id, str):
+				if isinstance(_id, tuple):
+
+					# Generate the key
+					sKey = cls._key % _id
 
 					# Try to fetch it from the cache
-					sPermissions = _moRedis.get('perms:%s' % _id)
+					sPermissions = _moRedis.get(sKey)
 
 					# If it's found
 					if sPermissions:
 
 						# Decode the data
-						dPermissions = JSON.decode(sPermissions)
+						dPermissions = jsonb.decode(sPermissions)
 
 					# Else, permissions not found in cache
 					else:
 
 						# Fetch the record from the DB
-						dPermissions = super().get(_id, raw=True, custom=custom)
+						dPermissions = super().filter({
+							'user': _id[0],
+							'portal': _id[1]
+						}, raw=True, limit=1, custom=custom)
+
+						# If it doesn't exist
+						if not dPermissions:
+							return None
 
 						# Store it in the cache
-						_moRedis.set('perms:%s' % _id, JSON.encode(dPermissions))
+						_moRedis.set(sKey, jsonb.encode(dPermissions))
 
 					# If we want raw data
 					if raw:
 
 						# If we want all data
 						if raw is True:
 							return dPermissions
 
 						# Else return only specific fields
-						return {k:dPermissions[k] for k in raw if k in dPermissions}
+						return {
+							k: dPermissions[k] \
+							for k in raw if k in dPermissions
+						}
 
 					# Else, create and return an instance
 					return cls(dPermissions)
 
 				# Else, if we have multiple IDs
 				elif isinstance(_id, list):
 
+					# Generate the keys
+					lKeys = [cls._key % k for k in _id]
+
 					# Fetch multiple keys
-					lPermissions = _moRedis.mget(['perms:%s' % k for k in _id])
+					lPermissions = _moRedis.mget(lKeys)
 
 					# Go through each one
 					for i in range(len(_id)):
 
-						# Generate the key
-						sKey = 'perms:%s' % i
-
 						# If we have a record
-						if lPermissions[sKey]:
+						if lPermissions[lKeys[i]]:
 
-							# Decode it
-							lPermissions[i] = JSON.decode(lPermissions[sKey])
-							del lPermissions[sKey]
+							# Decode it and store it under the index, deleting
+							#	the old value by key
+							lPermissions[i] = jsonb.decode(
+								lPermissions[lKeys[i]]
+							)
+							del lPermissions[lKeys[i]]
 
+						# Else, we have no record in the cache
 						else:
 
 							# Fetch the record from the DB
-							lPermissions[i] = super().get(_id[i], raw=True, custom=custom)
+							lPermissions[i] = super().filter({
+								'user': _id[i][0],
+								'portal': _id[i][1]
+							}, raw=True, custom=custom)
 
 					# Store it in the cache
-					_moRedis.set('perms:%s' % _id[i], JSON.encode(lPermissions[i]))
+					_moRedis.set(lKeys[i], jsonb.encode(lPermissions[i]))
 
 					# If we want raw
 					if raw:
 
 						# If we want all data
 						if raw is True:
 							return lPermissions
 
 						# Else return only specific fields
-						return [{k:dPermissions[k] for k in raw if k in d} for d in lPermissions]
+						return [
+							{ k: dPermissions[k] for k in raw if k in d} \
+							for d in lPermissions
+						]
 
 					# Else, create and return an instances
 					return [d and cls(d) or None for d in lPermissions]
 
 		# Invalid use of get
-		raise ValueError('Invalid use of Permissions.get')
+		raise ValueError(
+			'Invalid use of Permissions.get. ' \
+			'Try using Permissions.filter instead'
+		)
 
 class User(Record_MySQL.Record):
 	"""User
 
 	Represents a single user in the micro services system
 
 	Extends:
@@ -280,23 +329,23 @@
 			# Fetch a single key
 			sUser = _moRedis.get(_id)
 
 			# If we have a record
 			if sUser:
 
 				# Decode it
-				dUser = JSON.decode(sUser);
+				dUser = jsonb.decode(sUser)
 
 			else:
 
 				# Fetch the record from the DB
 				dUser = cls.get(_id, raw=True, custom=custom)
 
 				# Store it in the cache
-				_moRedis.set(_id, JSON.encode(dUser))
+				_moRedis.set(_id, jsonb.encode(dUser))
 
 			# If we don't have a record
 			if not dUser:
 				return None
 
 			# If we want raw
 			if raw:
@@ -317,23 +366,23 @@
 			# Go through each one
 			for i in range(len(_id)):
 
 				# If we have a record
 				if lUsers[i]:
 
 					# Decode it
-					lUsers[i] = JSON.decode(lUsers[i])
+					lUsers[i] = jsonb.decode(lUsers[i])
 
 				else:
 
 					# Fetch the record from the DB
 					lUsers[i] = cls.get(_id[i], raw=True, custom=custom)
 
 					# Store it in the cache
-					_moRedis.set(_id[i], JSON.encode(lUsers[i]))
+					_moRedis.set(_id[i], jsonb.encode(lUsers[i]))
 
 			# If we want raw
 			if raw:
 				return lUsers
 
 			# Return instances
 			return [d and cls(d) or None for d in lUsers]
@@ -364,15 +413,15 @@
 			dict
 		"""
 
 		# If we haven't loaded the config yet
 		if not cls._conf:
 			cls._conf = Record_MySQL.Record.generate_config(
 				Tree.fromFile('%s/user.json' % _defPath),
-				override={'db': Conf.get(('mysql', 'db'), 'brain')}
+				override={'db': config.mysql.db('brain')}
 			)
 
 		# Return the config
 		return cls._conf
 
 	@staticmethod
 	def password_hash(passwd):
@@ -384,15 +433,15 @@
 			passwd (str): The password to hash
 
 		Returns:
 			str
 		"""
 
 		# Generate the salt
-		sSalt = StrHelper.random(32, '_0x')
+		sSalt = random(32, ['0x'])
 
 		# Generate the hash
 		sHash = sha1(sSalt.encode('utf-8') + passwd.encode('utf-8')).hexdigest()
 
 		# Combine the salt and hash and return the new value
 		return sSalt[:20] + sHash + sSalt[20:]
 
@@ -436,16 +485,18 @@
 		# Get the password from the record
 		sPasswd = self.field_get('passwd')
 
 		# Split the password
 		sSalt = sPasswd[:20] + sPasswd[60:]
 		sHash = sPasswd[20:60]
 
-		# Return OK if the rehashed password matches
-		return sHash == sha1(sSalt.encode('utf-8') + passwd.encode('utf-8')).hexdigest()
+		# Return OK if the re-hashed password matches
+		return sHash == sha1(
+			sSalt.encode('utf-8') + passwd.encode('utf-8')
+		).hexdigest()
 
 	@classmethod
 	def simple_search(cls, query, custom={}):
 		"""Simple Search
 
 		Looks for query in multiple fields
```

### Comparing `Brain-OC-1.0.1/brain/users.py` & `Brain-OC-1.1.0/brain/users.py`

 * *Files identical despite different names*

### Comparing `Brain-OC-1.0.1/setup.py` & `Brain-OC-1.1.0/setup.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,33 +1,40 @@
 from setuptools import setup
 
 with open('README.md', 'r') as oF:
 	long_description=oF.read()
 
 setup(
 	name='Brain-OC',
-	version='1.0.1',
-	description='Brain contains a service to run users and permissions',
+	version='1.1.0',
+	description='Brain contains a service to manage users and permissions',
 	long_description=long_description,
 	long_description_content_type='text/markdown',
 	url='https://ouroboroscoding.com/body/brain',
 	project_urls={
 		'Documentation': 'https://ouroboroscoding.com/body/brain',
 		'Source': 'https://github.com/ouroboroscoding/brain',
 		'Tracker': 'https://github.com/ouroboroscoding/brain/issues'
 	},
 	keywords=['rest','microservices'],
 	author='Chris Nasr - Ouroboros Coding Inc.',
 	author_email='chris@ouroboroscoding.com',
 	license='Custom',
 	packages=['brain'],
-	package_data={'brain': ['definitions/*.json']},
+	package_data={'brain': [
+		'definitions/*.json',
+		'upgrades/*'
+	]},
 	python_requires='>=3.10',
 	install_requires=[
-		'Rest-OC>=1.1.2',
-		'Body-OC>=1.0.1'
+		'Body-OC>=1.0.1',
+		'Config-OC>=1.0.1,<1.1',
+		'jsonb>=1.0.0,<1.1',
+		'Rest-OC>=1.2.4',
+		'Strings-OC>=1.0.1,<1.1',
+		'Upgrade-OC>=1.0.0,<1.1'
 	],
 	entry_points={
 		'console_scripts': ['brain=brain.__main__:cli']
 	},
 	zip_safe=True
 )
```

