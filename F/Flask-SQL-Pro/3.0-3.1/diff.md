# Comparing `tmp/Flask-SQL-Pro-3.0.tar.gz` & `tmp/Flask-SQL-Pro-3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Flask-SQL-Pro-3.0.tar", last modified: Sun Jul 23 14:59:00 2023, max compression
+gzip compressed data, was "Flask-SQL-Pro-3.1.tar", last modified: Sun Jul 23 16:38:08 2023, max compression
```

## Comparing `Flask-SQL-Pro-3.0.tar` & `Flask-SQL-Pro-3.1.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 14:59:00.394890 Flask-SQL-Pro-3.0/
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 14:59:00.393660 Flask-SQL-Pro-3.0/Flask_SQL_Pro.egg-info/
--rw-r--r--   0 kela       (501) staff       (20)     8292 2023-07-23 14:59:00.000000 Flask-SQL-Pro-3.0/Flask_SQL_Pro.egg-info/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-23 14:59:00.000000 Flask-SQL-Pro-3.0/Flask_SQL_Pro.egg-info/SOURCES.txt
--rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-23 14:59:00.000000 Flask-SQL-Pro-3.0/Flask_SQL_Pro.egg-info/dependency_links.txt
--rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-23 14:59:00.000000 Flask-SQL-Pro-3.0/Flask_SQL_Pro.egg-info/requires.txt
--rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-23 14:59:00.000000 Flask-SQL-Pro-3.0/Flask_SQL_Pro.egg-info/top_level.txt
--rw-r--r--   0 kela       (501) staff       (20)     8292 2023-07-23 14:59:00.394718 Flask-SQL-Pro-3.0/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)     7775 2023-07-23 14:55:41.000000 Flask-SQL-Pro-3.0/README.rst
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 14:59:00.394383 Flask-SQL-Pro-3.0/flask_sql_pro/
--rw-r--r--   0 kela       (501) staff       (20)     1739 2023-07-21 05:57:01.000000 Flask-SQL-Pro-3.0/flask_sql_pro/__init__.py
--rw-r--r--   0 kela       (501) staff       (20)     8149 2023-07-21 05:07:24.000000 Flask-SQL-Pro-3.0/flask_sql_pro/db.py
--rw-r--r--   0 kela       (501) staff       (20)     6025 2023-07-21 05:10:52.000000 Flask-SQL-Pro-3.0/flask_sql_pro/sql_loader.py
--rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-23 14:59:00.394938 Flask-SQL-Pro-3.0/setup.cfg
--rw-r--r--   0 kela       (501) staff       (20)      816 2023-07-23 14:58:47.000000 Flask-SQL-Pro-3.0/setup.py
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:38:08.301905 Flask-SQL-Pro-3.1/
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:38:08.294306 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/
+-rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/SOURCES.txt
+-rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/dependency_links.txt
+-rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/requires.txt
+-rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/top_level.txt
+-rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:38:08.296663 Flask-SQL-Pro-3.1/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)     8316 2023-07-23 16:37:58.000000 Flask-SQL-Pro-3.1/README.rst
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:38:08.296307 Flask-SQL-Pro-3.1/flask_sql_pro/
+-rw-r--r--   0 kela       (501) staff       (20)     1843 2023-07-23 16:05:44.000000 Flask-SQL-Pro-3.1/flask_sql_pro/__init__.py
+-rw-r--r--   0 kela       (501) staff       (20)     8871 2023-07-23 16:34:23.000000 Flask-SQL-Pro-3.1/flask_sql_pro/db.py
+-rw-r--r--   0 kela       (501) staff       (20)     6020 2023-07-23 16:21:52.000000 Flask-SQL-Pro-3.1/flask_sql_pro/sql_loader.py
+-rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-23 16:38:08.301973 Flask-SQL-Pro-3.1/setup.cfg
+-rw-r--r--   0 kela       (501) staff       (20)      816 2023-07-23 16:35:18.000000 Flask-SQL-Pro-3.1/setup.py
```

### Comparing `Flask-SQL-Pro-3.0/Flask_SQL_Pro.egg-info/PKG-INFO` & `Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,168 +1,181 @@
 Metadata-Version: 2.1
 Name: Flask-SQL-Pro
-Version: 3.0
+Version: 3.1
 Summary: 基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页
 Author: miaokela
 Author-email: 2972799448@qq.com
 Maintainer: miaokela
 Maintainer-email: 2972799448@qq.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 
-Flask-SQL-Pro的使用
+
+Changelog
+=============
+
+v3.1 (2023-07-24)
+----------------------
+
+- Added security check
+- Fixed bug default delete flag
+
+
+Use of Flask-SQL-Pro
 ==========================
 
-示例: https://www.cnblogs.com/miaokela/articles/17571427.html
+Example: https://www.cnblogs.com/miaokela/articles/17571427.html
 
 
 .. pull-quote:: 
   pip install flask-sql-pro
 
-注册
-----
+Register
+----------
 
 .. pull-quote:: 
-  在create_app中注册
+  Register in create_app
 
 .. code-block:: python
 
   def create_app():
-      # 注册Flask-SQL-Pro对象,并且注册Flask-SQLAlchemy
+      # Register Flask-SQL-Pro objects, and register Flask-SQLAlchemy
       sqlpro = FlaskSQLPro()
       db = sqlpro.init_app(app)
 
 .. pull-quote:: 
-  为什么要在init_app()中返回一个db呢? Flask-Migrate等插件数据库操作可能用到SQLAlchemy实例对象
+  Why return a db in init_app()? 
+  SQLAlchemy instance objects may be used for plug-in database operations such as Flask-Migrate
 
 .. code-block:: python
 
   from flask_migrate import Migrate
 
 
   Migrate(app, db)
 
 
-在models.py中引入
+Import in models.py
 -----------------------
 
 .. code-block:: python
 
   from flask_sql_pro import DataBaseHelper
   from sqlalchemy import text
   from sqlalchemy.dialects.mysql import TINYINT, BIGINT, VARCHAR, DATETIME, DOUBLE, INTEGER
 
-  # 其他文件中如果要使用db对象: from project_path.models import db
+  # If you want to use db objects in other files: from project_path.models import db
   db = DataBaseHelper.db
 
   class BaseModel(db.Model):
       __abstract__ = True
-      created_at = db.Column(DATETIME, comment='创建时间', server_default=text('Now()'))
-      updated_at = db.Column(DATETIME, comment='更新时间', server_default=text('Now()'), onupdate=datetime.now())
-      is_deleted = db.Column(TINYINT, comment='是否逻辑删除', server_default=text('0'), index=True)
+      created_at = db.Column(DATETIME, comment='Create Time', server_default=text('Now()'))
+      updated_at = db.Column(DATETIME, comment='Update Time', server_default=text('Now()'), onupdate=datetime.now())
+      is_deleted = db.Column(TINYINT, comment='Logical delete or not', server_default=text('0'), index=True)
 
       @classmethod
       def queryset(cls):
           """
           Data that is not logically deleted
           """
           return cls.query.filter(cls.is_deleted == 0)
 
-CRUD示例
---------
+CRUD example
+--------------
 
-- 增
+- Add
 
 .. code-block:: python
 
-  from flask_sql_pro import DataBaseHelper  # 主工具类
-  from app.models import db # SQLAlchemy实例对象
+  from flask_sql_pro import DataBaseHelper  # Master tool class
+  from app.models import db # SQLAlchemy Instance object
 
   with db.trans():
       _id = DataBaseHelper.execute_create(
-          'transit_record',  # 数据库名称
+          'transit_record',  # Table name
           data=data,
       )
 
       if not _id:
           raise AddRecordException()
 
-- 删
+- Delete
   
 .. code-block:: python
 
   with db.trans():
       rows = DataBaseHelper.execute_delete(
           'transit_record',
           where={
               'id': _id,
           },
           logic=True
       )
       if not rows:
           raise DelRecordException()
 
-- 改
+- Modify
 
 .. code-block:: python
 
   with db.trans():
       rows = DataBaseHelper.execute_update(
           'transit_record',
           data=data,
           where={
               'id': _id
           }
       )
       if not rows:
           raise ModifyRecordException()
 
-- 查
+- Select
 
 .. pull-quote:: 
-  创建存放SQL语句的文件夹
-  默认是Flask的instance_path路径, 即: project_path/instance/
-  则默认的SQL文件夹应该创建在: project_path/instance/sql
-  允许自定义路径，配置参数 DB_HELPER_SQL_FILE_PATH
+  Create a folder to store SQL statements
+  The default is Flask's instance_path path, which is project_path/instance/
+  The default SQL folder should be created in project_path/instance/sql
+  To allow custom paths, configure the DB_HELPER_SQL_FILE_PATH parameter
 
 .. code-block:: python
 
   import os
 
 
   class BaseConfig:
       BASE_DIR = os.path.dirname(os.path.realpath(__file__))
       APP_DIR = os.path.join(BASE_DIR, 'app')
       DB_HELPER_SQL_FILE_PATH = os.path.join(
           APP_DIR,
           'sql'
       )
 
-  # 在创建Flask应用时,注册配置
+  # Register the configuration when creating a Flask application
   # __init__.py
   def create_app():
       # ...
       app.config.from_object(BaseConfig())
       # ...
 
 .. pull-quote:: 
-  其他Flask-SQL-Pro的配置
+  Other Flask-SQL-Pro configurations
 
 .. code-block:: python
 
-  DB_HELPER_PAGE_PARAM = 'page'  # 默认分页第几页
-  DB_HELPER_PAGE_SIZE_PARAM = 'page_size'  # 默认分页每页数量
-  DB_HELPER_PRINT_MSG = True  # 是否在终端打印SQL执行的语句
+  DB_HELPER_LOGIC_DELETE_FLAG = 'delete_flag'  # The default logic delete flag name
+  DB_HELPER_PAGE_PARAM = 'page'  # The default page number
+  DB_HELPER_PAGE_SIZE_PARAM = 'page_size'  # Default number of pages per page
+  DB_HELPER_PRINT_MSG = True  # Whether to print SQL execution statements on the terminal
 
 .. pull-quote:: 
-  查询示例
+  Query example
 
-文件: sql/transit/index.yml
+Files: sql/transit/index.yml
 
 .. code-block:: yaml
 
   query_map: |
       SELECT
           TRG.latitude,
           TRG.longitude,
@@ -177,34 +190,34 @@
       WHERE
           TRG.is_deleted = 0
       AND
           TR.is_deleted = 0
       AND
           TR.id = :transit_record_id
 
-文件: app/api/transit.py
+Files: app/api/transit.py
 
 .. code-block:: python
 
   transit_record_gps = DataBaseHelper.select_all(
       'transit.index.query_map',
       params={
           'transit_record_id': transit_record_id
       },
-      return_obj=False,  # return_obj默认为True，即返回的是对象可以通过 transit_record_gps[0].transit_record_id 点的方式获取数据，如果为False，返回的是字典
+      return_obj=False,  # The default value of return_obj is True, which means that the object can obtain data from the transit_record_gps[0].transit_record_id point. If False, the dictionary is returned
   )
 
 
 
-- 分页
+- Pagination
 
 .. pull-quote:: 
-  默认需要传递的参数是 page/page_size, 两个参数都传递才会分页
+  The default parameter that needs to be passed is page/page_size, and paging occurs when both parameters are passeds
 
-文件: sql/history/index.yml
+Files: sql/history/index.yml
 
 .. code-block:: yaml
 
   select_user_experiments: |
       SELECT
           experiment_id,
           experiment_name,
@@ -223,20 +236,20 @@
       },
       options={
           'page': 1,
           'page_size': 20,
       }
   )
 
-- 动态SQL
+- Dynamic SQL
 
 .. pull-quote:: 
-  配合jinja2,实现条件语句,动态生成SQL
+  With jinja2, conditional statement is realized and SQL is generated dynamically
 
-文件: sql/experiment/index.yml
+Files: sql/experiment/index.yml
 
 .. code-block:: yaml
 
   select_history_data_by_id_and_time: |
       SELECT
           daedd.daq_data_id daqDataId,
           daedd.vel_rms_value rmsVelocityValue,
@@ -262,15 +275,15 @@
       {% endif %}
       {% if experiment_id %}
       AND 
           daedd.experiment_id = :experiment_id
       {% endif %}
       ORDER BY daedd.collection_datetime ASC
 
-文件: app/api/experiment.py
+Files: app/api/experiment.py
 
 .. code-block:: python
 
   daq_data_list = DataBaseHelper.select_all(
       "experiment.index.select_history_data_by_id_and_time",
       params={
           "sensor_id": query.sensorId,
@@ -281,56 +294,56 @@
       options={
           "query_start_time": query.queryStartTime,
           "query_end_time": query.queryEndTime,
           "experiment_id": experiment_id,
       },
   )
 
-- 多数据库操作
+- Multi-database operation
 
 .. pull-quote:: 
-  除了系统当前配置的 SQLALCHEMY_DATABASE_URI 对应的数据库之外，想操作其他数据库
+  You want to operate other databases other than the database corresponding to the SQLALCHEMY_DATABASE_URI configured in the system
 
 .. pull-quote:: 
-  配置参数
+  Configuration parameter
 
 .. code-block:: python
 
   class BaseConfig:
       SQLALCHEMY_BINDS = {
           'cloud': 'mysql+pymysql://root:123456@127.0.0.1:3306/cloud_db?charset=utf8'
       }
 
 .. pull-quote:: 
-  示例
+  Give an example
 
 .. code-block:: python
 
   add = DataBaseHelper.execute_create(
       'daq_data',
       data=online_data,
       app=cp,  # from flask import current_app as cp
-      bind='cloud'  # 指定Bind的数据库
+      bind='cloud'  # Specifies the database for Bind
   )
   if not add:
-      raise Exception('推送线上数据失败')
+      raise Exception('Description Failed to push online data')
 
   DataBaseHelper.commit()
 
-- 事务
+- Transaction
 
 .. pull-quote:: 
-  默认不提交,使用DataBaseHelper.commit()来提交,或者 通过db.trans()上下文事务
+  No commit by default, commit using databaseHelper.mit (), or through the db.trans() context transaction
 
 .. code-block:: python
 
   from app.models import db
 
   with db.trans():
       add = DataBaseHelper.execute_create(
           'daq_data',
           data=online_data,
           app=cp,  # from flask import current_app as cp
-          bind='cloud'  # 指定Bind的数据库
+          bind='cloud'  # Specifies the database for Bind
       )
       if not add:
-          raise Exception('推送线上数据失败')
+          raise Exception('Description Failed to push online data')
```

### Comparing `Flask-SQL-Pro-3.0/PKG-INFO` & `Flask-SQL-Pro-3.1/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,168 +1,181 @@
 Metadata-Version: 2.1
 Name: Flask-SQL-Pro
-Version: 3.0
+Version: 3.1
 Summary: 基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页
 Author: miaokela
 Author-email: 2972799448@qq.com
 Maintainer: miaokela
 Maintainer-email: 2972799448@qq.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 
-Flask-SQL-Pro的使用
+
+Changelog
+=============
+
+v3.1 (2023-07-24)
+----------------------
+
+- Added security check
+- Fixed bug default delete flag
+
+
+Use of Flask-SQL-Pro
 ==========================
 
-示例: https://www.cnblogs.com/miaokela/articles/17571427.html
+Example: https://www.cnblogs.com/miaokela/articles/17571427.html
 
 
 .. pull-quote:: 
   pip install flask-sql-pro
 
-注册
-----
+Register
+----------
 
 .. pull-quote:: 
-  在create_app中注册
+  Register in create_app
 
 .. code-block:: python
 
   def create_app():
-      # 注册Flask-SQL-Pro对象,并且注册Flask-SQLAlchemy
+      # Register Flask-SQL-Pro objects, and register Flask-SQLAlchemy
       sqlpro = FlaskSQLPro()
       db = sqlpro.init_app(app)
 
 .. pull-quote:: 
-  为什么要在init_app()中返回一个db呢? Flask-Migrate等插件数据库操作可能用到SQLAlchemy实例对象
+  Why return a db in init_app()? 
+  SQLAlchemy instance objects may be used for plug-in database operations such as Flask-Migrate
 
 .. code-block:: python
 
   from flask_migrate import Migrate
 
 
   Migrate(app, db)
 
 
-在models.py中引入
+Import in models.py
 -----------------------
 
 .. code-block:: python
 
   from flask_sql_pro import DataBaseHelper
   from sqlalchemy import text
   from sqlalchemy.dialects.mysql import TINYINT, BIGINT, VARCHAR, DATETIME, DOUBLE, INTEGER
 
-  # 其他文件中如果要使用db对象: from project_path.models import db
+  # If you want to use db objects in other files: from project_path.models import db
   db = DataBaseHelper.db
 
   class BaseModel(db.Model):
       __abstract__ = True
-      created_at = db.Column(DATETIME, comment='创建时间', server_default=text('Now()'))
-      updated_at = db.Column(DATETIME, comment='更新时间', server_default=text('Now()'), onupdate=datetime.now())
-      is_deleted = db.Column(TINYINT, comment='是否逻辑删除', server_default=text('0'), index=True)
+      created_at = db.Column(DATETIME, comment='Create Time', server_default=text('Now()'))
+      updated_at = db.Column(DATETIME, comment='Update Time', server_default=text('Now()'), onupdate=datetime.now())
+      is_deleted = db.Column(TINYINT, comment='Logical delete or not', server_default=text('0'), index=True)
 
       @classmethod
       def queryset(cls):
           """
           Data that is not logically deleted
           """
           return cls.query.filter(cls.is_deleted == 0)
 
-CRUD示例
---------
+CRUD example
+--------------
 
-- 增
+- Add
 
 .. code-block:: python
 
-  from flask_sql_pro import DataBaseHelper  # 主工具类
-  from app.models import db # SQLAlchemy实例对象
+  from flask_sql_pro import DataBaseHelper  # Master tool class
+  from app.models import db # SQLAlchemy Instance object
 
   with db.trans():
       _id = DataBaseHelper.execute_create(
-          'transit_record',  # 数据库名称
+          'transit_record',  # Table name
           data=data,
       )
 
       if not _id:
           raise AddRecordException()
 
-- 删
+- Delete
   
 .. code-block:: python
 
   with db.trans():
       rows = DataBaseHelper.execute_delete(
           'transit_record',
           where={
               'id': _id,
           },
           logic=True
       )
       if not rows:
           raise DelRecordException()
 
-- 改
+- Modify
 
 .. code-block:: python
 
   with db.trans():
       rows = DataBaseHelper.execute_update(
           'transit_record',
           data=data,
           where={
               'id': _id
           }
       )
       if not rows:
           raise ModifyRecordException()
 
-- 查
+- Select
 
 .. pull-quote:: 
-  创建存放SQL语句的文件夹
-  默认是Flask的instance_path路径, 即: project_path/instance/
-  则默认的SQL文件夹应该创建在: project_path/instance/sql
-  允许自定义路径，配置参数 DB_HELPER_SQL_FILE_PATH
+  Create a folder to store SQL statements
+  The default is Flask's instance_path path, which is project_path/instance/
+  The default SQL folder should be created in project_path/instance/sql
+  To allow custom paths, configure the DB_HELPER_SQL_FILE_PATH parameter
 
 .. code-block:: python
 
   import os
 
 
   class BaseConfig:
       BASE_DIR = os.path.dirname(os.path.realpath(__file__))
       APP_DIR = os.path.join(BASE_DIR, 'app')
       DB_HELPER_SQL_FILE_PATH = os.path.join(
           APP_DIR,
           'sql'
       )
 
-  # 在创建Flask应用时,注册配置
+  # Register the configuration when creating a Flask application
   # __init__.py
   def create_app():
       # ...
       app.config.from_object(BaseConfig())
       # ...
 
 .. pull-quote:: 
-  其他Flask-SQL-Pro的配置
+  Other Flask-SQL-Pro configurations
 
 .. code-block:: python
 
-  DB_HELPER_PAGE_PARAM = 'page'  # 默认分页第几页
-  DB_HELPER_PAGE_SIZE_PARAM = 'page_size'  # 默认分页每页数量
-  DB_HELPER_PRINT_MSG = True  # 是否在终端打印SQL执行的语句
+  DB_HELPER_LOGIC_DELETE_FLAG = 'delete_flag'  # The default logic delete flag name
+  DB_HELPER_PAGE_PARAM = 'page'  # The default page number
+  DB_HELPER_PAGE_SIZE_PARAM = 'page_size'  # Default number of pages per page
+  DB_HELPER_PRINT_MSG = True  # Whether to print SQL execution statements on the terminal
 
 .. pull-quote:: 
-  查询示例
+  Query example
 
-文件: sql/transit/index.yml
+Files: sql/transit/index.yml
 
 .. code-block:: yaml
 
   query_map: |
       SELECT
           TRG.latitude,
           TRG.longitude,
@@ -177,34 +190,34 @@
       WHERE
           TRG.is_deleted = 0
       AND
           TR.is_deleted = 0
       AND
           TR.id = :transit_record_id
 
-文件: app/api/transit.py
+Files: app/api/transit.py
 
 .. code-block:: python
 
   transit_record_gps = DataBaseHelper.select_all(
       'transit.index.query_map',
       params={
           'transit_record_id': transit_record_id
       },
-      return_obj=False,  # return_obj默认为True，即返回的是对象可以通过 transit_record_gps[0].transit_record_id 点的方式获取数据，如果为False，返回的是字典
+      return_obj=False,  # The default value of return_obj is True, which means that the object can obtain data from the transit_record_gps[0].transit_record_id point. If False, the dictionary is returned
   )
 
 
 
-- 分页
+- Pagination
 
 .. pull-quote:: 
-  默认需要传递的参数是 page/page_size, 两个参数都传递才会分页
+  The default parameter that needs to be passed is page/page_size, and paging occurs when both parameters are passeds
 
-文件: sql/history/index.yml
+Files: sql/history/index.yml
 
 .. code-block:: yaml
 
   select_user_experiments: |
       SELECT
           experiment_id,
           experiment_name,
@@ -223,20 +236,20 @@
       },
       options={
           'page': 1,
           'page_size': 20,
       }
   )
 
-- 动态SQL
+- Dynamic SQL
 
 .. pull-quote:: 
-  配合jinja2,实现条件语句,动态生成SQL
+  With jinja2, conditional statement is realized and SQL is generated dynamically
 
-文件: sql/experiment/index.yml
+Files: sql/experiment/index.yml
 
 .. code-block:: yaml
 
   select_history_data_by_id_and_time: |
       SELECT
           daedd.daq_data_id daqDataId,
           daedd.vel_rms_value rmsVelocityValue,
@@ -262,15 +275,15 @@
       {% endif %}
       {% if experiment_id %}
       AND 
           daedd.experiment_id = :experiment_id
       {% endif %}
       ORDER BY daedd.collection_datetime ASC
 
-文件: app/api/experiment.py
+Files: app/api/experiment.py
 
 .. code-block:: python
 
   daq_data_list = DataBaseHelper.select_all(
       "experiment.index.select_history_data_by_id_and_time",
       params={
           "sensor_id": query.sensorId,
@@ -281,56 +294,56 @@
       options={
           "query_start_time": query.queryStartTime,
           "query_end_time": query.queryEndTime,
           "experiment_id": experiment_id,
       },
   )
 
-- 多数据库操作
+- Multi-database operation
 
 .. pull-quote:: 
-  除了系统当前配置的 SQLALCHEMY_DATABASE_URI 对应的数据库之外，想操作其他数据库
+  You want to operate other databases other than the database corresponding to the SQLALCHEMY_DATABASE_URI configured in the system
 
 .. pull-quote:: 
-  配置参数
+  Configuration parameter
 
 .. code-block:: python
 
   class BaseConfig:
       SQLALCHEMY_BINDS = {
           'cloud': 'mysql+pymysql://root:123456@127.0.0.1:3306/cloud_db?charset=utf8'
       }
 
 .. pull-quote:: 
-  示例
+  Give an example
 
 .. code-block:: python
 
   add = DataBaseHelper.execute_create(
       'daq_data',
       data=online_data,
       app=cp,  # from flask import current_app as cp
-      bind='cloud'  # 指定Bind的数据库
+      bind='cloud'  # Specifies the database for Bind
   )
   if not add:
-      raise Exception('推送线上数据失败')
+      raise Exception('Description Failed to push online data')
 
   DataBaseHelper.commit()
 
-- 事务
+- Transaction
 
 .. pull-quote:: 
-  默认不提交,使用DataBaseHelper.commit()来提交,或者 通过db.trans()上下文事务
+  No commit by default, commit using databaseHelper.mit (), or through the db.trans() context transaction
 
 .. code-block:: python
 
   from app.models import db
 
   with db.trans():
       add = DataBaseHelper.execute_create(
           'daq_data',
           data=online_data,
           app=cp,  # from flask import current_app as cp
-          bind='cloud'  # 指定Bind的数据库
+          bind='cloud'  # Specifies the database for Bind
       )
       if not add:
-          raise Exception('推送线上数据失败')
+          raise Exception('Description Failed to push online data')
```

### Comparing `Flask-SQL-Pro-3.0/README.rst` & `Flask-SQL-Pro-3.1/README.rst`

 * *Files 14% similar despite different names*

```diff
@@ -1,155 +1,168 @@
-Flask-SQL-Pro的使用
+
+Changelog
+=============
+
+v3.1 (2023-07-24)
+----------------------
+
+- Added security check
+- Fixed bug default delete flag
+
+
+Use of Flask-SQL-Pro
 ==========================
 
-示例: https://www.cnblogs.com/miaokela/articles/17571427.html
+Example: https://www.cnblogs.com/miaokela/articles/17571427.html
 
 
 .. pull-quote:: 
   pip install flask-sql-pro
 
-注册
-----
+Register
+----------
 
 .. pull-quote:: 
-  在create_app中注册
+  Register in create_app
 
 .. code-block:: python
 
   def create_app():
-      # 注册Flask-SQL-Pro对象,并且注册Flask-SQLAlchemy
+      # Register Flask-SQL-Pro objects, and register Flask-SQLAlchemy
       sqlpro = FlaskSQLPro()
       db = sqlpro.init_app(app)
 
 .. pull-quote:: 
-  为什么要在init_app()中返回一个db呢? Flask-Migrate等插件数据库操作可能用到SQLAlchemy实例对象
+  Why return a db in init_app()? 
+  SQLAlchemy instance objects may be used for plug-in database operations such as Flask-Migrate
 
 .. code-block:: python
 
   from flask_migrate import Migrate
 
 
   Migrate(app, db)
 
 
-在models.py中引入
+Import in models.py
 -----------------------
 
 .. code-block:: python
 
   from flask_sql_pro import DataBaseHelper
   from sqlalchemy import text
   from sqlalchemy.dialects.mysql import TINYINT, BIGINT, VARCHAR, DATETIME, DOUBLE, INTEGER
 
-  # 其他文件中如果要使用db对象: from project_path.models import db
+  # If you want to use db objects in other files: from project_path.models import db
   db = DataBaseHelper.db
 
   class BaseModel(db.Model):
       __abstract__ = True
-      created_at = db.Column(DATETIME, comment='创建时间', server_default=text('Now()'))
-      updated_at = db.Column(DATETIME, comment='更新时间', server_default=text('Now()'), onupdate=datetime.now())
-      is_deleted = db.Column(TINYINT, comment='是否逻辑删除', server_default=text('0'), index=True)
+      created_at = db.Column(DATETIME, comment='Create Time', server_default=text('Now()'))
+      updated_at = db.Column(DATETIME, comment='Update Time', server_default=text('Now()'), onupdate=datetime.now())
+      is_deleted = db.Column(TINYINT, comment='Logical delete or not', server_default=text('0'), index=True)
 
       @classmethod
       def queryset(cls):
           """
           Data that is not logically deleted
           """
           return cls.query.filter(cls.is_deleted == 0)
 
-CRUD示例
---------
+CRUD example
+--------------
 
-- 增
+- Add
 
 .. code-block:: python
 
-  from flask_sql_pro import DataBaseHelper  # 主工具类
-  from app.models import db # SQLAlchemy实例对象
+  from flask_sql_pro import DataBaseHelper  # Master tool class
+  from app.models import db # SQLAlchemy Instance object
 
   with db.trans():
       _id = DataBaseHelper.execute_create(
-          'transit_record',  # 数据库名称
+          'transit_record',  # Table name
           data=data,
       )
 
       if not _id:
           raise AddRecordException()
 
-- 删
+- Delete
   
 .. code-block:: python
 
   with db.trans():
       rows = DataBaseHelper.execute_delete(
           'transit_record',
           where={
               'id': _id,
           },
           logic=True
       )
       if not rows:
           raise DelRecordException()
 
-- 改
+- Modify
 
 .. code-block:: python
 
   with db.trans():
       rows = DataBaseHelper.execute_update(
           'transit_record',
           data=data,
           where={
               'id': _id
           }
       )
       if not rows:
           raise ModifyRecordException()
 
-- 查
+- Select
 
 .. pull-quote:: 
-  创建存放SQL语句的文件夹
-  默认是Flask的instance_path路径, 即: project_path/instance/
-  则默认的SQL文件夹应该创建在: project_path/instance/sql
-  允许自定义路径，配置参数 DB_HELPER_SQL_FILE_PATH
+  Create a folder to store SQL statements
+  The default is Flask's instance_path path, which is project_path/instance/
+  The default SQL folder should be created in project_path/instance/sql
+  To allow custom paths, configure the DB_HELPER_SQL_FILE_PATH parameter
 
 .. code-block:: python
 
   import os
 
 
   class BaseConfig:
       BASE_DIR = os.path.dirname(os.path.realpath(__file__))
       APP_DIR = os.path.join(BASE_DIR, 'app')
       DB_HELPER_SQL_FILE_PATH = os.path.join(
           APP_DIR,
           'sql'
       )
 
-  # 在创建Flask应用时,注册配置
+  # Register the configuration when creating a Flask application
   # __init__.py
   def create_app():
       # ...
       app.config.from_object(BaseConfig())
       # ...
 
 .. pull-quote:: 
-  其他Flask-SQL-Pro的配置
+  Other Flask-SQL-Pro configurations
 
 .. code-block:: python
 
-  DB_HELPER_PAGE_PARAM = 'page'  # 默认分页第几页
-  DB_HELPER_PAGE_SIZE_PARAM = 'page_size'  # 默认分页每页数量
-  DB_HELPER_PRINT_MSG = True  # 是否在终端打印SQL执行的语句
+  DB_HELPER_LOGIC_DELETE_FLAG = 'delete_flag'  # The default logic delete flag name
+  DB_HELPER_PAGE_PARAM = 'page'  # The default page number
+  DB_HELPER_PAGE_SIZE_PARAM = 'page_size'  # Default number of pages per page
+  DB_HELPER_PRINT_MSG = True  # Whether to print SQL execution statements on the terminal
 
 .. pull-quote:: 
-  查询示例
+  Query example
 
-文件: sql/transit/index.yml
+Files: sql/transit/index.yml
 
 .. code-block:: yaml
 
   query_map: |
       SELECT
           TRG.latitude,
           TRG.longitude,
@@ -164,34 +177,34 @@
       WHERE
           TRG.is_deleted = 0
       AND
           TR.is_deleted = 0
       AND
           TR.id = :transit_record_id
 
-文件: app/api/transit.py
+Files: app/api/transit.py
 
 .. code-block:: python
 
   transit_record_gps = DataBaseHelper.select_all(
       'transit.index.query_map',
       params={
           'transit_record_id': transit_record_id
       },
-      return_obj=False,  # return_obj默认为True，即返回的是对象可以通过 transit_record_gps[0].transit_record_id 点的方式获取数据，如果为False，返回的是字典
+      return_obj=False,  # The default value of return_obj is True, which means that the object can obtain data from the transit_record_gps[0].transit_record_id point. If False, the dictionary is returned
   )
 
 
 
-- 分页
+- Pagination
 
 .. pull-quote:: 
-  默认需要传递的参数是 page/page_size, 两个参数都传递才会分页
+  The default parameter that needs to be passed is page/page_size, and paging occurs when both parameters are passeds
 
-文件: sql/history/index.yml
+Files: sql/history/index.yml
 
 .. code-block:: yaml
 
   select_user_experiments: |
       SELECT
           experiment_id,
           experiment_name,
@@ -210,20 +223,20 @@
       },
       options={
           'page': 1,
           'page_size': 20,
       }
   )
 
-- 动态SQL
+- Dynamic SQL
 
 .. pull-quote:: 
-  配合jinja2,实现条件语句,动态生成SQL
+  With jinja2, conditional statement is realized and SQL is generated dynamically
 
-文件: sql/experiment/index.yml
+Files: sql/experiment/index.yml
 
 .. code-block:: yaml
 
   select_history_data_by_id_and_time: |
       SELECT
           daedd.daq_data_id daqDataId,
           daedd.vel_rms_value rmsVelocityValue,
@@ -249,15 +262,15 @@
       {% endif %}
       {% if experiment_id %}
       AND 
           daedd.experiment_id = :experiment_id
       {% endif %}
       ORDER BY daedd.collection_datetime ASC
 
-文件: app/api/experiment.py
+Files: app/api/experiment.py
 
 .. code-block:: python
 
   daq_data_list = DataBaseHelper.select_all(
       "experiment.index.select_history_data_by_id_and_time",
       params={
           "sensor_id": query.sensorId,
@@ -268,56 +281,56 @@
       options={
           "query_start_time": query.queryStartTime,
           "query_end_time": query.queryEndTime,
           "experiment_id": experiment_id,
       },
   )
 
-- 多数据库操作
+- Multi-database operation
 
 .. pull-quote:: 
-  除了系统当前配置的 SQLALCHEMY_DATABASE_URI 对应的数据库之外，想操作其他数据库
+  You want to operate other databases other than the database corresponding to the SQLALCHEMY_DATABASE_URI configured in the system
 
 .. pull-quote:: 
-  配置参数
+  Configuration parameter
 
 .. code-block:: python
 
   class BaseConfig:
       SQLALCHEMY_BINDS = {
           'cloud': 'mysql+pymysql://root:123456@127.0.0.1:3306/cloud_db?charset=utf8'
       }
 
 .. pull-quote:: 
-  示例
+  Give an example
 
 .. code-block:: python
 
   add = DataBaseHelper.execute_create(
       'daq_data',
       data=online_data,
       app=cp,  # from flask import current_app as cp
-      bind='cloud'  # 指定Bind的数据库
+      bind='cloud'  # Specifies the database for Bind
   )
   if not add:
-      raise Exception('推送线上数据失败')
+      raise Exception('Description Failed to push online data')
 
   DataBaseHelper.commit()
 
-- 事务
+- Transaction
 
 .. pull-quote:: 
-  默认不提交,使用DataBaseHelper.commit()来提交,或者 通过db.trans()上下文事务
+  No commit by default, commit using databaseHelper.mit (), or through the db.trans() context transaction
 
 .. code-block:: python
 
   from app.models import db
 
   with db.trans():
       add = DataBaseHelper.execute_create(
           'daq_data',
           data=online_data,
           app=cp,  # from flask import current_app as cp
-          bind='cloud'  # 指定Bind的数据库
+          bind='cloud'  # Specifies the database for Bind
       )
       if not add:
-          raise Exception('推送线上数据失败')
+          raise Exception('Description Failed to push online data')
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `Flask-SQL-Pro-3.0/flask_sql_pro/__init__.py` & `Flask-SQL-Pro-3.1/flask_sql_pro/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -28,14 +28,15 @@
 
     def init_app(self, app, *args, **kwargs):
         if not hasattr(app, 'extensions'):
             app.extensions = {}
         _db = SQLAlchemy(app, *args, **kwargs)
         app.extensions['flask_sql_pro'] = self  # You can now access instances of the my_extension plugin in your Flask application
         DataBaseHelper.db = _db
+        DataBaseHelper.logic_delete_flag = app.config.get('DB_HELPER_LOGIC_DELETE_FLAG', 'delete_flag')
         DataBaseHelper.page_param = app.config.get('DB_HELPER_PAGE_PARAM', 'page')
         DataBaseHelper.page_size_param = app.config.get('DB_HELPER_PAGE_SIZE_PARAM', 'page_size')
         DataBaseHelper.print_msg = app.config.get('DB_HELPER_PRINT_MSG', False)
         SqlLoader.page_param = app.config.get('DB_HELPER_PAGE_PARAM', 'page')
         SqlLoader.page_size_param = app.config.get('DB_HELPER_PAGE_SIZE_PARAM', 'page_size')
 
         default_sql_file_path = os.path.join(
```

### Comparing `Flask-SQL-Pro-3.0/flask_sql_pro/db.py` & `Flask-SQL-Pro-3.1/flask_sql_pro/db.py`

 * *Files 8% similar despite different names*

```diff
@@ -23,15 +23,17 @@
             self[key] = value
 
 
 class DataBaseHelper(object):
     db = None
     page_param = None
     page_size_param = None
+    logic_delete_flag = None
     print_msg = False
+    sql_injection_keywords = ['DROP', 'SELECT', 'DELETE' 'UPDATE', 'INSERT', 'EXEC', '--', '/*', '*/', 'xp_', 'sp_']
 
     @classmethod
     def print(cls, msg):
         if cls.print_msg:
             print(msg)
 
     @classmethod
@@ -53,26 +55,33 @@
         if not where:
             return sql
         where_str = " WHERE "
         for key in where.keys():
             where_str += key + " = :" + "_where_%s" % key + " and "
         where_str = where_str[0:-5]
         sql += where_str
+
         return sql
 
     @classmethod
     def fullfilled_data(cls, data, where):
         """
         The delete/update operation adds a _where_${field} field to each field in the where condition of the incoming data,
         which is used for the assignment of the where condition
         """
         if not where:
             return data
 
         for k, v in where.items():
+            # Avoid sql injection
+            if any(keyword in str(k).upper() for keyword in cls.sql_injection_keywords):
+                raise ValueError('Keywords that may be at risk for SQL injection in key: ' + str(k))
+            if any(keyword in str(v).upper() for keyword in cls.sql_injection_keywords):
+                raise ValueError('Keywords that may be at risk for SQL injection in value: ' + str(v))
+
             if k.startswith("_where_"):
                 raise Exception("The where condition cannot contain a field starting with _where_")
             data.update(**{
                 "_where_%s" % k: v
             })
 
         return data
@@ -158,26 +167,32 @@
         :param bind:
         :param app:
         :param logic:
         :param tb_name: indicates the table name
         :param where: indicates the filter condition
         :return: indicates the number of deleted items
         """
-        sql = "DELETE FROM " + tb_name
         if logic:
-            sql = "UPDATE %s SET delete_flag=1" % tb_name
+            sql = "UPDATE :table SET :flag=1"
+            params = {"table": tb_name, "flag": cls.logic_delete_flag}
+        else:
+            sql = "DELETE FROM :table"
+            params = {"table": tb_name}
+            
         sql = cls.set_where_phrase(sql, where)
         where = cls.fullfilled_data({}, where)
 
+        params.update(where)
+
         try:
             if app and bind:
                 bind = cls.db.get_engine(app, bind=bind)
-                result = cls.db.session.execute(sql, where, bind=bind)
+                result = cls.db.session.execute(sql, params, bind=bind)
             else:
-                result = cls.db.session.execute(sql, where)
+                result = cls.db.session.execute(sql, params)
             return result.rowcount
         except Exception as e:
             cls.print("Failed to execute sql: < %s %s >! Cause: %s" % (sql, str(where), str(e)))
             return None
 
     @classmethod
     def execute_sql(cls, sql_id, params=None, options: typing.Dict[str, str] = None, app=None, bind=None, return_obj=True):
```

### Comparing `Flask-SQL-Pro-3.0/flask_sql_pro/sql_loader.py` & `Flask-SQL-Pro-3.1/flask_sql_pro/sql_loader.py`

 * *Files 2% similar despite different names*

```diff
@@ -161,16 +161,16 @@
         if page_num:
             del options[self.page_param]
         if page_size:
             del options[self.page_size_param]
 
         if any([page_num, page_size]):
             page_num = page_num if page_num else 1
-            options['limit'] = page_size if page_size else 10  # 默认10条
-            options['offset'] = (page_num - 1) * options['limit']
+            options['limit'] = int(page_size if page_size else 10)
+            options['offset'] = int((page_num - 1) * options['limit'])
 
             c_sql += """
             {% if limit and not offset %}
                 LIMIT {{ limit }}
                 {% elif limit and offset %}
                 LIMIT {{ offset }},{{ limit }}
             {% endif %}
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

