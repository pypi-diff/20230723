# Comparing `tmp/lisql-2.0.9.tar.gz` & `tmp/lisql-2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lisql-2.0.9.tar", last modified: Tue Apr  4 12:30:35 2023, max compression
+gzip compressed data, was "lisql-2.1.tar", last modified: Sun Jul 23 18:21:51 2023, max compression
```

## Comparing `lisql-2.0.9.tar` & `lisql-2.1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 aliahammad   (501) staff       (20)        0 2023-04-04 12:30:35.679161 lisql-2.0.9/
--rw-rw-r--   0 aliahammad   (501) staff       (20)     1068 2023-03-08 15:14:22.000000 lisql-2.0.9/LICENSE
--rw-r--r--   0 aliahammad   (501) staff       (20)    16634 2023-04-04 12:30:35.679312 lisql-2.0.9/PKG-INFO
--rw-r--r--   0 aliahammad   (501) staff       (20)    15852 2023-04-04 10:26:45.000000 lisql-2.0.9/README.md
--rw-rw-r--   0 aliahammad   (501) staff       (20)      103 2022-09-11 17:28:42.000000 lisql-2.0.9/pyproject.toml
--rw-rw-r--   0 aliahammad   (501) staff       (20)      603 2023-04-04 12:30:35.679801 lisql-2.0.9/setup.cfg
--rw-rw-r--   0 aliahammad   (501) staff       (20)      725 2023-04-04 10:48:21.000000 lisql-2.0.9/setup.py
-drwxr-xr-x   0 aliahammad   (501) staff       (20)        0 2023-04-04 12:30:35.678201 lisql-2.0.9/src/
-drwxr-xr-x   0 aliahammad   (501) staff       (20)        0 2023-04-04 12:30:35.678987 lisql-2.0.9/src/lisql.egg-info/
--rw-r--r--   0 aliahammad   (501) staff       (20)    16634 2023-04-04 12:30:35.000000 lisql-2.0.9/src/lisql.egg-info/PKG-INFO
--rw-r--r--   0 aliahammad   (501) staff       (20)      196 2023-04-04 12:30:35.000000 lisql-2.0.9/src/lisql.egg-info/SOURCES.txt
--rw-r--r--   0 aliahammad   (501) staff       (20)        1 2023-04-04 12:30:35.000000 lisql-2.0.9/src/lisql.egg-info/dependency_links.txt
--rw-r--r--   0 aliahammad   (501) staff       (20)        6 2023-04-04 12:30:35.000000 lisql-2.0.9/src/lisql.egg-info/top_level.txt
--rw-rw-r--   0 aliahammad   (501) staff       (20)    14534 2023-04-04 12:27:59.000000 lisql-2.0.9/src/lisql.py
+drwxr-xr-x   0 li         (501) staff       (20)        0 2023-07-23 18:21:51.287914 lisql-2.1/
+-rw-r--r--   0 li         (501) staff       (20)     1068 2023-05-14 18:33:24.000000 lisql-2.1/LICENSE
+-rw-r--r--   0 li         (501) staff       (20)    19100 2023-07-23 18:21:51.288016 lisql-2.1/PKG-INFO
+-rw-r--r--   0 li         (501) staff       (20)    18320 2023-07-23 17:26:59.000000 lisql-2.1/README.md
+-rw-r--r--   0 li         (501) staff       (20)      103 2023-05-14 18:33:24.000000 lisql-2.1/pyproject.toml
+-rw-r--r--   0 li         (501) staff       (20)      601 2023-07-23 18:21:51.288669 lisql-2.1/setup.cfg
+-rw-r--r--   0 li         (501) staff       (20)      723 2023-07-21 21:32:35.000000 lisql-2.1/setup.py
+drwxr-xr-x   0 li         (501) staff       (20)        0 2023-07-23 18:21:51.286919 lisql-2.1/src/
+drwxr-xr-x   0 li         (501) staff       (20)        0 2023-07-23 18:21:51.287798 lisql-2.1/src/lisql.egg-info/
+-rw-r--r--   0 li         (501) staff       (20)    19100 2023-07-23 18:21:51.000000 lisql-2.1/src/lisql.egg-info/PKG-INFO
+-rw-r--r--   0 li         (501) staff       (20)      196 2023-07-23 18:21:51.000000 lisql-2.1/src/lisql.egg-info/SOURCES.txt
+-rw-r--r--   0 li         (501) staff       (20)        1 2023-07-23 18:21:51.000000 lisql-2.1/src/lisql.egg-info/dependency_links.txt
+-rw-r--r--   0 li         (501) staff       (20)        6 2023-07-23 18:21:51.000000 lisql-2.1/src/lisql.egg-info/top_level.txt
+-rw-r--r--   0 li         (501) staff       (20)    22817 2023-07-23 18:15:58.000000 lisql-2.1/src/lisql.py
```

### Comparing `lisql-2.0.9/LICENSE` & `lisql-2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `lisql-2.0.9/PKG-INFO` & `lisql-2.1/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -1,42 +1,58 @@
-Metadata-Version: 2.1
-Name: lisql
-Version: 2.0.9
-Summary: Provides simple funtions to interact with MySQL databases and tables.
-Home-page: https://github.com/li812/lisql
-Author: Ali Ahammad
-Author-email: aliahammad0812@outlook.com
-Project-URL: Bug Tracker, https://github.com/li812/lisql/issues
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
-Requires-Python: >=3.6
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
-# `lisql`
-
-![logo](https://user-images.githubusercontent.com/68907011/229516295-04088400-302d-4849-bc48-9fd327800566.png)
-
-`lisql` is a Python package that provides a simple and intuitive interface to work with MySQL databases. It can be used to perform various operations such as creating and dropping databases and tables, inserting and selecting data, and executing SQL queries. `lisql` can also be used in various fields where data is stored in MySQL databases, such as web development, data analytics, business intelligence, and more. With its easy-to-use functions for connecting to, querying, and modifying databases, `lisql` can help developers and analysts efficiently work with MySQL databases in their projects. Additionally, `lisql` can be integrated with other Python libraries and tools, such as Pandas and Scikit-learn, to provide more advanced data manipulation and analysis capabilities.
-
-## Requirements:
-Python 3.6 or higher
-mysql-connector-python library (version 8.0 or higher)
+
+# LiSQL
+## Simplifying MySQL Database Management with Python
+
+![LiSQL Logo](https://user-images.githubusercontent.com/68907011/229516295-04088400-302d-4849-bc48-9fd327800566.png)
+
+## Overview
+
+LiSQL is a feature-rich Python package designed to streamline interactions with multiple MySQL databases across different servers. Whether you're a developer or a data scientist, LiSQL offers an intuitive interface that simplifies database management, data manipulation, and aggregation tasks.
+
+With LiSQL, connecting to both local and remote MySQL databases becomes effortless. Its seamless integration with Python projects, including web development, data analytics, and business intelligence, makes it a versatile tool for various applications.
+
+
+## Key Features of LiSQL
+
+- **Efficient Connection** Management: LiSQL facilitates establishing connections to different servers, enabling seamless data access and manipulation.
+
+- **Simplified Database and Table Operations**: Create, drop, and describe databases and tables with ease, effectively organizing and structuring your data.
+
+- **Easy Data Manipulation**: Perform data manipulations effortlessly with LiSQL's functions for selecting, inserting, updating, and deleting data.
+- **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
+- **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
+- **Transaction Support**: Execute multiple database operations as a single unit with transaction support, ensuring data integrity and consistency.
+
+
+## Requirements
+#### 1. Python 3.6 or higher:
+LiSQL requires Python 3.6 or higher.
+#### 2. MySQL Connector/Python: 
+LiSQL depends on the MySQL Connector/Python library to establish connections with MySQL databases. Make sure you have this library installed.
 
 You can install the mysql-connector-python library using pip:
 ```commandline
 pip install mysql-connector-python
 
 ```
+#### 3. MySQL Server: 
+You need access to a MySQL server, either on your local machine or a remote server, to use LiSQL for database operations.
+
+#### 4. MySQL Database: 
+Ensure that you have the necessary privileges to create, drop, and modify databases on the MySQL server you are connecting to.
+
+#### 5. Network Connectivity: 
+If you plan to connect to a remote MySQL server, make sure you have network connectivity to the server and the required permissions to access it.
+
+#### 6. Operating System: 
+LiSQL is compatible with Windows, macOS, and Linux operating systems.
+
+#### 7. Python Packages: 
+LiSQL itself does not have additional dependencies beyond the MySQL Connector/Python library. However, depending on your specific use case, you may need additional Python packages for data processing, web development, or other functionalities.
+
 ## Installation:
 
 To install the `lisql` package, you can follow the steps below:
 
 1: Open a terminal or command prompt on your machine.
 ```commandline
 python --version
@@ -54,31 +70,20 @@
 
 4: You can now start using the `lisql` package in your Python scripts by importing it:
 ```commandline
 import lisql
 
 ```
 
-5: If you want to use a remote MySQL server, make sure you have the necessary credentials (host, username, and password) to connect to the server.
-
-6: To connect to a remote MySQL server, you can use the `create_remote_connection()` function, passing in the host, username, and password as arguments:
-```
-mydb = lisql.create_remote_connection(host, username, password)
-```
 
-7: Once you have a database connection, you can use the `connect_database()` function to connect to a specific database:
-```commandline
-mydb = lisql.connect_database(mydb, 'mydatabase')
-
-```
-8: You can now start executing SQL queries using the `lisql` package.
+5: You can now start executing SQL queries using the `lisql` package.
 Note: If you encounter any errors during installation, make sure you have the necessary permissions to install Python packages on your machine. You can also try running the installation command with administrative privileges (e.g., using sudo on Linux or macOS).
 
 ## Usage:
-
+### LiSQL provides a range of functions for seamless MySQL database interaction:
 ### 1: Creating a Connection
 To create a connection to a MySQL server, you can use the create_connection() function:
 ```
 import lisql
 
 mydb = lisql.create_connection()
 ```
@@ -304,14 +309,21 @@
 # Create a connection
 mydb = lisql.create_connection()
 
 # Drop a database
 lisql.drop_database(mydb, 'mydatabase')
 
 ```
+### 10: For help:
+```commandline
+import lisql
+
+lisql.help
+
+```
 ## Examples
 ### Here's an example program that demonstrates connecting to multiple servers and databases:
 ```
 import lisql
 
 # Create a connection to a local MySQL server with default user and password values
 local_db = lisql.create_connection()
@@ -369,14 +381,49 @@
 print("Tables in remote database:")
 for table in remote_description:
     print(table)
 
 ```
 This program connects to a local and remote MySQL server, connects to databases on each server, performs various database operations, and retrieves information about tables and databases.
 
+
+### Here's an example of using Transaction Support in the lisql package to create a table and insert data into it as part of a single transaction:
+
+```
+import lisql
+
+# Create a connection to a local MySQL server
+mydb = lisql.create_connection()
+
+# Connect to a database
+mydb = lisql.connect_database(mydb, 'mydatabase')
+
+# Enable transaction support
+mydb.autocommit = False
+
+# Define the table columns
+columns = ['id INT PRIMARY KEY', 'name VARCHAR(255)', 'age INT']
+
+# Create a table with transaction support
+lisql.create_table(mydb, 'students', columns, transaction=True)
+
+# Insert data into the table as part of the same transaction
+values = [(1, 'John Doe', 25), (2, 'Jane Smith', 30)]
+lisql.insert_data(mydb, 'students', values, transaction=True)
+
+# Commit the transaction to save changes
+mydb.commit()
+
+# Display the contents of the table after the transaction
+data = lisql.select_data(mydb, 'students', ['id', 'name', 'age'])
+for row in data:
+    print(row)
+
+```
+
 ### Here's an example program that demonstrates how to use lisql with pandas and numpy on two servers:
 ```
 import lisql
 import pandas as pd
 import numpy as np
 
 # create connections to two MySQL servers
@@ -488,12 +535,17 @@
 print('Test accuracy:', test_acc)
 
 ```
 In this example, we first create connections to two remote MySQL servers using create_remote_connection(). We then use Pandas and SQL queries to extract data from the servers and preprocess the data. We then train a machine learning model using TensorFlow and evaluate the model on test data extracted from one of the servers.
 
 Note that this is just an example, and you can use other data science technologies such as Apache Spark or PyTorch with lisql in a similar way.
 
-## For any questions, bug reports, or feedback, please feel free to contact the developers via:
+## License
+
+LiSQL is distributed under the MIT License. See the [LICENSE](https://github.com/li812/lisql/blob/main/LICENSE) file for more details.
+
+## Contact
+stions, bug reports, or feedback, please feel free to contact the developers via:
 ### Email: aliahammad0812@outlook.com 
 
 ### Instagram: https://www.instagram.com/the_raptor_rider_/
```

### Comparing `lisql-2.0.9/README.md` & `lisql-2.1/PKG-INFO`

 * *Files 13% similar despite different names*

```diff
@@ -1,22 +1,78 @@
-# `lisql`
+Metadata-Version: 2.1
+Name: lisql
+Version: 2.1
+Summary: Provides simple funtions to interact with MySQL databases and tables.
+Home-page: https://github.com/li812/lisql
+Author: Ali Ahammad
+Author-email: aliahammad0812@outlook.com
+Project-URL: Bug Tracker, https://github.com/li812/lisql/issues
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.6
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Python: >=3.6
+Description-Content-Type: text/markdown
+License-File: LICENSE
 
-![logo](https://user-images.githubusercontent.com/68907011/229516295-04088400-302d-4849-bc48-9fd327800566.png)
 
-`lisql` is a Python package that provides a simple and intuitive interface to work with MySQL databases. It can be used to perform various operations such as creating and dropping databases and tables, inserting and selecting data, and executing SQL queries. `lisql` can also be used in various fields where data is stored in MySQL databases, such as web development, data analytics, business intelligence, and more. With its easy-to-use functions for connecting to, querying, and modifying databases, `lisql` can help developers and analysts efficiently work with MySQL databases in their projects. Additionally, `lisql` can be integrated with other Python libraries and tools, such as Pandas and Scikit-learn, to provide more advanced data manipulation and analysis capabilities.
+# LiSQL
+## Simplifying MySQL Database Management with Python
 
-## Requirements:
-Python 3.6 or higher
-mysql-connector-python library (version 8.0 or higher)
+![LiSQL Logo](https://user-images.githubusercontent.com/68907011/229516295-04088400-302d-4849-bc48-9fd327800566.png)
+
+## Overview
+
+LiSQL is a feature-rich Python package designed to streamline interactions with multiple MySQL databases across different servers. Whether you're a developer or a data scientist, LiSQL offers an intuitive interface that simplifies database management, data manipulation, and aggregation tasks.
+
+With LiSQL, connecting to both local and remote MySQL databases becomes effortless. Its seamless integration with Python projects, including web development, data analytics, and business intelligence, makes it a versatile tool for various applications.
+
+
+## Key Features of LiSQL
+
+- **Efficient Connection** Management: LiSQL facilitates establishing connections to different servers, enabling seamless data access and manipulation.
+
+- **Simplified Database and Table Operations**: Create, drop, and describe databases and tables with ease, effectively organizing and structuring your data.
+
+- **Easy Data Manipulation**: Perform data manipulations effortlessly with LiSQL's functions for selecting, inserting, updating, and deleting data.
+- **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
+- **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
+- **Transaction Support**: Execute multiple database operations as a single unit with transaction support, ensuring data integrity and consistency.
+
+
+## Requirements
+#### 1. Python 3.6 or higher:
+LiSQL requires Python 3.6 or higher.
+#### 2. MySQL Connector/Python: 
+LiSQL depends on the MySQL Connector/Python library to establish connections with MySQL databases. Make sure you have this library installed.
 
 You can install the mysql-connector-python library using pip:
 ```commandline
 pip install mysql-connector-python
 
 ```
+#### 3. MySQL Server: 
+You need access to a MySQL server, either on your local machine or a remote server, to use LiSQL for database operations.
+
+#### 4. MySQL Database: 
+Ensure that you have the necessary privileges to create, drop, and modify databases on the MySQL server you are connecting to.
+
+#### 5. Network Connectivity: 
+If you plan to connect to a remote MySQL server, make sure you have network connectivity to the server and the required permissions to access it.
+
+#### 6. Operating System: 
+LiSQL is compatible with Windows, macOS, and Linux operating systems.
+
+#### 7. Python Packages: 
+LiSQL itself does not have additional dependencies beyond the MySQL Connector/Python library. However, depending on your specific use case, you may need additional Python packages for data processing, web development, or other functionalities.
+
 ## Installation:
 
 To install the `lisql` package, you can follow the steps below:
 
 1: Open a terminal or command prompt on your machine.
 ```commandline
 python --version
@@ -34,31 +90,20 @@
 
 4: You can now start using the `lisql` package in your Python scripts by importing it:
 ```commandline
 import lisql
 
 ```
 
-5: If you want to use a remote MySQL server, make sure you have the necessary credentials (host, username, and password) to connect to the server.
 
-6: To connect to a remote MySQL server, you can use the `create_remote_connection()` function, passing in the host, username, and password as arguments:
-```
-mydb = lisql.create_remote_connection(host, username, password)
-```
-
-7: Once you have a database connection, you can use the `connect_database()` function to connect to a specific database:
-```commandline
-mydb = lisql.connect_database(mydb, 'mydatabase')
-
-```
-8: You can now start executing SQL queries using the `lisql` package.
+5: You can now start executing SQL queries using the `lisql` package.
 Note: If you encounter any errors during installation, make sure you have the necessary permissions to install Python packages on your machine. You can also try running the installation command with administrative privileges (e.g., using sudo on Linux or macOS).
 
 ## Usage:
-
+### LiSQL provides a range of functions for seamless MySQL database interaction:
 ### 1: Creating a Connection
 To create a connection to a MySQL server, you can use the create_connection() function:
 ```
 import lisql
 
 mydb = lisql.create_connection()
 ```
@@ -284,14 +329,21 @@
 # Create a connection
 mydb = lisql.create_connection()
 
 # Drop a database
 lisql.drop_database(mydb, 'mydatabase')
 
 ```
+### 10: For help:
+```commandline
+import lisql
+
+lisql.help
+
+```
 ## Examples
 ### Here's an example program that demonstrates connecting to multiple servers and databases:
 ```
 import lisql
 
 # Create a connection to a local MySQL server with default user and password values
 local_db = lisql.create_connection()
@@ -349,14 +401,49 @@
 print("Tables in remote database:")
 for table in remote_description:
     print(table)
 
 ```
 This program connects to a local and remote MySQL server, connects to databases on each server, performs various database operations, and retrieves information about tables and databases.
 
+
+### Here's an example of using Transaction Support in the lisql package to create a table and insert data into it as part of a single transaction:
+
+```
+import lisql
+
+# Create a connection to a local MySQL server
+mydb = lisql.create_connection()
+
+# Connect to a database
+mydb = lisql.connect_database(mydb, 'mydatabase')
+
+# Enable transaction support
+mydb.autocommit = False
+
+# Define the table columns
+columns = ['id INT PRIMARY KEY', 'name VARCHAR(255)', 'age INT']
+
+# Create a table with transaction support
+lisql.create_table(mydb, 'students', columns, transaction=True)
+
+# Insert data into the table as part of the same transaction
+values = [(1, 'John Doe', 25), (2, 'Jane Smith', 30)]
+lisql.insert_data(mydb, 'students', values, transaction=True)
+
+# Commit the transaction to save changes
+mydb.commit()
+
+# Display the contents of the table after the transaction
+data = lisql.select_data(mydb, 'students', ['id', 'name', 'age'])
+for row in data:
+    print(row)
+
+```
+
 ### Here's an example program that demonstrates how to use lisql with pandas and numpy on two servers:
 ```
 import lisql
 import pandas as pd
 import numpy as np
 
 # create connections to two MySQL servers
@@ -468,12 +555,17 @@
 print('Test accuracy:', test_acc)
 
 ```
 In this example, we first create connections to two remote MySQL servers using create_remote_connection(). We then use Pandas and SQL queries to extract data from the servers and preprocess the data. We then train a machine learning model using TensorFlow and evaluate the model on test data extracted from one of the servers.
 
 Note that this is just an example, and you can use other data science technologies such as Apache Spark or PyTorch with lisql in a similar way.
 
-## For any questions, bug reports, or feedback, please feel free to contact the developers via:
+## License
+
+LiSQL is distributed under the MIT License. See the [LICENSE](https://github.com/li812/lisql/blob/main/LICENSE) file for more details.
+
+## Contact
+stions, bug reports, or feedback, please feel free to contact the developers via:
 ### Email: aliahammad0812@outlook.com 
 
 ### Instagram: https://www.instagram.com/the_raptor_rider_/
```

### Comparing `lisql-2.0.9/setup.cfg` & `lisql-2.1/setup.cfg`

 * *Files 27% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = lisql
-version = 2.0.9
+version = 2.1
 author = Ali Ahammad
 author_email = aliahammad0812@outlook.com
 description = Python sql companion
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/li812/lisql
 project_urls =
```

### Comparing `lisql-2.0.9/setup.py` & `lisql-2.1/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup
 
 setup(
     name='lisql',
-    version='2.0.9',
+    version='2.1',
     py_modules=['lisql'],
     description='Provides simple funtions to interact with MySQL databases and tables.',
     author='Ali Ahammad',
     author_email='aliahammad0812@outlook.com',
     url='https://github.com/li812/lisql',
     classifiers=[
         'License :: OSI Approved :: MIT License',
```

### Comparing `lisql-2.0.9/src/lisql.egg-info/PKG-INFO` & `lisql-2.1/src/lisql.egg-info/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lisql
-Version: 2.0.9
+Version: 2.1
 Summary: Provides simple funtions to interact with MySQL databases and tables.
 Home-page: https://github.com/li812/lisql
 Author: Ali Ahammad
 Author-email: aliahammad0812@outlook.com
 Project-URL: Bug Tracker, https://github.com/li812/lisql/issues
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -14,29 +14,65 @@
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
-# `lisql`
 
-![logo](https://user-images.githubusercontent.com/68907011/229516295-04088400-302d-4849-bc48-9fd327800566.png)
+# LiSQL
+## Simplifying MySQL Database Management with Python
 
-`lisql` is a Python package that provides a simple and intuitive interface to work with MySQL databases. It can be used to perform various operations such as creating and dropping databases and tables, inserting and selecting data, and executing SQL queries. `lisql` can also be used in various fields where data is stored in MySQL databases, such as web development, data analytics, business intelligence, and more. With its easy-to-use functions for connecting to, querying, and modifying databases, `lisql` can help developers and analysts efficiently work with MySQL databases in their projects. Additionally, `lisql` can be integrated with other Python libraries and tools, such as Pandas and Scikit-learn, to provide more advanced data manipulation and analysis capabilities.
+![LiSQL Logo](https://user-images.githubusercontent.com/68907011/229516295-04088400-302d-4849-bc48-9fd327800566.png)
 
-## Requirements:
-Python 3.6 or higher
-mysql-connector-python library (version 8.0 or higher)
+## Overview
+
+LiSQL is a feature-rich Python package designed to streamline interactions with multiple MySQL databases across different servers. Whether you're a developer or a data scientist, LiSQL offers an intuitive interface that simplifies database management, data manipulation, and aggregation tasks.
+
+With LiSQL, connecting to both local and remote MySQL databases becomes effortless. Its seamless integration with Python projects, including web development, data analytics, and business intelligence, makes it a versatile tool for various applications.
+
+
+## Key Features of LiSQL
+
+- **Efficient Connection** Management: LiSQL facilitates establishing connections to different servers, enabling seamless data access and manipulation.
+
+- **Simplified Database and Table Operations**: Create, drop, and describe databases and tables with ease, effectively organizing and structuring your data.
+
+- **Easy Data Manipulation**: Perform data manipulations effortlessly with LiSQL's functions for selecting, inserting, updating, and deleting data.
+- **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
+- **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
+- **Transaction Support**: Execute multiple database operations as a single unit with transaction support, ensuring data integrity and consistency.
+
+
+## Requirements
+#### 1. Python 3.6 or higher:
+LiSQL requires Python 3.6 or higher.
+#### 2. MySQL Connector/Python: 
+LiSQL depends on the MySQL Connector/Python library to establish connections with MySQL databases. Make sure you have this library installed.
 
 You can install the mysql-connector-python library using pip:
 ```commandline
 pip install mysql-connector-python
 
 ```
+#### 3. MySQL Server: 
+You need access to a MySQL server, either on your local machine or a remote server, to use LiSQL for database operations.
+
+#### 4. MySQL Database: 
+Ensure that you have the necessary privileges to create, drop, and modify databases on the MySQL server you are connecting to.
+
+#### 5. Network Connectivity: 
+If you plan to connect to a remote MySQL server, make sure you have network connectivity to the server and the required permissions to access it.
+
+#### 6. Operating System: 
+LiSQL is compatible with Windows, macOS, and Linux operating systems.
+
+#### 7. Python Packages: 
+LiSQL itself does not have additional dependencies beyond the MySQL Connector/Python library. However, depending on your specific use case, you may need additional Python packages for data processing, web development, or other functionalities.
+
 ## Installation:
 
 To install the `lisql` package, you can follow the steps below:
 
 1: Open a terminal or command prompt on your machine.
 ```commandline
 python --version
@@ -54,31 +90,20 @@
 
 4: You can now start using the `lisql` package in your Python scripts by importing it:
 ```commandline
 import lisql
 
 ```
 
-5: If you want to use a remote MySQL server, make sure you have the necessary credentials (host, username, and password) to connect to the server.
-
-6: To connect to a remote MySQL server, you can use the `create_remote_connection()` function, passing in the host, username, and password as arguments:
-```
-mydb = lisql.create_remote_connection(host, username, password)
-```
-
-7: Once you have a database connection, you can use the `connect_database()` function to connect to a specific database:
-```commandline
-mydb = lisql.connect_database(mydb, 'mydatabase')
 
-```
-8: You can now start executing SQL queries using the `lisql` package.
+5: You can now start executing SQL queries using the `lisql` package.
 Note: If you encounter any errors during installation, make sure you have the necessary permissions to install Python packages on your machine. You can also try running the installation command with administrative privileges (e.g., using sudo on Linux or macOS).
 
 ## Usage:
-
+### LiSQL provides a range of functions for seamless MySQL database interaction:
 ### 1: Creating a Connection
 To create a connection to a MySQL server, you can use the create_connection() function:
 ```
 import lisql
 
 mydb = lisql.create_connection()
 ```
@@ -304,14 +329,21 @@
 # Create a connection
 mydb = lisql.create_connection()
 
 # Drop a database
 lisql.drop_database(mydb, 'mydatabase')
 
 ```
+### 10: For help:
+```commandline
+import lisql
+
+lisql.help
+
+```
 ## Examples
 ### Here's an example program that demonstrates connecting to multiple servers and databases:
 ```
 import lisql
 
 # Create a connection to a local MySQL server with default user and password values
 local_db = lisql.create_connection()
@@ -369,14 +401,49 @@
 print("Tables in remote database:")
 for table in remote_description:
     print(table)
 
 ```
 This program connects to a local and remote MySQL server, connects to databases on each server, performs various database operations, and retrieves information about tables and databases.
 
+
+### Here's an example of using Transaction Support in the lisql package to create a table and insert data into it as part of a single transaction:
+
+```
+import lisql
+
+# Create a connection to a local MySQL server
+mydb = lisql.create_connection()
+
+# Connect to a database
+mydb = lisql.connect_database(mydb, 'mydatabase')
+
+# Enable transaction support
+mydb.autocommit = False
+
+# Define the table columns
+columns = ['id INT PRIMARY KEY', 'name VARCHAR(255)', 'age INT']
+
+# Create a table with transaction support
+lisql.create_table(mydb, 'students', columns, transaction=True)
+
+# Insert data into the table as part of the same transaction
+values = [(1, 'John Doe', 25), (2, 'Jane Smith', 30)]
+lisql.insert_data(mydb, 'students', values, transaction=True)
+
+# Commit the transaction to save changes
+mydb.commit()
+
+# Display the contents of the table after the transaction
+data = lisql.select_data(mydb, 'students', ['id', 'name', 'age'])
+for row in data:
+    print(row)
+
+```
+
 ### Here's an example program that demonstrates how to use lisql with pandas and numpy on two servers:
 ```
 import lisql
 import pandas as pd
 import numpy as np
 
 # create connections to two MySQL servers
@@ -488,12 +555,17 @@
 print('Test accuracy:', test_acc)
 
 ```
 In this example, we first create connections to two remote MySQL servers using create_remote_connection(). We then use Pandas and SQL queries to extract data from the servers and preprocess the data. We then train a machine learning model using TensorFlow and evaluate the model on test data extracted from one of the servers.
 
 Note that this is just an example, and you can use other data science technologies such as Apache Spark or PyTorch with lisql in a similar way.
 
-## For any questions, bug reports, or feedback, please feel free to contact the developers via:
+## License
+
+LiSQL is distributed under the MIT License. See the [LICENSE](https://github.com/li812/lisql/blob/main/LICENSE) file for more details.
+
+## Contact
+stions, bug reports, or feedback, please feel free to contact the developers via:
 ### Email: aliahammad0812@outlook.com 
 
 ### Instagram: https://www.instagram.com/the_raptor_rider_/
```

### Comparing `lisql-2.0.9/src/lisql.py` & `lisql-2.1/src/lisql.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,325 +1,515 @@
-import mysql.connector
 
+import importlib
 
-def create_connection():
-    mydb = mysql.connector.connect(
-        host='localhost',
-        user='root',
-        password=''
-    )
-    if mydb.is_connected():
-        print('MySQL connected')
-    else:
-        print('MySQL not connected')
-    return mydb
+def check_and_install_mysql_connector():
+    try:
+        importlib.import_module('mysql.connector')
+    except ImportError:
+        print("mysql-connector-python is not installed. Installing it now...")
+        try:
+            import pip
+            pip.main(['install', 'mysql-connector-python'])
+
+        except Exception as e:
+            print("Error installing mysql-connector-python:", str(e))
 
+check_and_install_mysql_connector()
+
+
+import mysql.connector
+
+def create_connection():
+    try:
+        mydb = mysql.connector.connect(
+            host='localhost',
+            user='root',
+            password=''
+        )
+        if mydb.is_connected():
+            print('MySQL connected')
+        else:
+            print('MySQL not connected')
+        return mydb
+    except mysql.connector.Error as e:
+        print(f"Error creating local connection: {e}")
+        return None
 
 def create_remote_connection(host, user, password):
-    mydb = mysql.connector.connect(
-        host=host,
-        user=user,
-        password=password
-    )
-    if mydb.is_connected():
-        print('MySQL connected')
-    else:
-        print('MySQL not connected')
-    return mydb
+    try:
+        mydb = mysql.connector.connect(
+            host=host,
+            user=user,
+            password=password
+        )
+        if mydb.is_connected():
+            print('MySQL connected')
+        else:
+            print('MySQL not connected')
+        return mydb
+    except mysql.connector.Error as e:
+        print(f"Error creating remote connection: {e}")
+        return None
 
-def create_database(mydb, name):
+def create_database(mydb, name, transaction=False):
     cursor = mydb.cursor()
     create_db_query = f'CREATE DATABASE {name}'
     print(f'Executing command: {create_db_query}')
     try:
+        if transaction:
+            mydb.start_transaction()  # Start the transaction explicitly
+            
         cursor.execute(create_db_query)
-        mydb.commit()
+        
+        if transaction:
+            mydb.commit()  # Commit the transaction if transaction=True
+            
         print(f'Database {name} created successfully!')
-    except mysql.connector.errors.DatabaseError:
-        print('Database already exists')
+    except mysql.connector.Error as e:
+        if transaction:
+            mydb.rollback()  # Roll back the transaction if an error occurs
+        if e.errno == mysql.connector.errorcode.ER_DB_CREATE_EXISTS:
+            print(f'Database {name} already exists')
+        else:
+            print(f'Something else went wrong: {e}')
     except Exception as e:
         print(f'Something else went wrong: {e}')
     return mydb
 
-def connect_remote_database(host, username, password, database):
+
+def connect_remote_database(host, username, password, database, transaction=False):
     try:
         mydb = mysql.connector.connect(
             host=host,
             user=username,
             password=password,
             database=database
         )
         print(f"Connected to {host} successfully!")
+        if transaction:
+            mydb.autocommit = False  # Disable autocommit to enable transactions
         return mydb
-    except Exception as e:
+    except mysql.connector.Error as e:
         print(f"Error connecting to {host}: {e}")
+        return None
 
-def drop_database(mydb, name):
+
+def drop_database(mydb, name, transaction=False):
     cursor = mydb.cursor()
     drop_db_query = f'DROP DATABASE IF EXISTS {name}'
     print(f'Executing command: {drop_db_query}')
     try:
+        if transaction:
+            mydb.start_transaction()  # Start the transaction explicitly
+            
         cursor.execute(drop_db_query)
+        
+        if transaction:
+            mydb.commit()  # Commit the transaction if transaction=True
+            
         print(f'Database {name} dropped successfully!')
-    except mysql.connector.errors.DatabaseError:
-        print(f'Database {name} does not exist')
+    except mysql.connector.Error as e:
+        if transaction:
+            mydb.rollback()  # Roll back the transaction if an error occurs
+        if e.errno == mysql.connector.errorcode.ER_BAD_DB_ERROR:
+            print(f'Database {name} does not exist')
+        else:
+            print(f'Something else went wrong: {e}')
     except Exception as e:
         print(f'Something else went wrong: {e}')
 
-def connect_database(mydb, name):
+
+def connect_database(mydb, name, transaction=False):
     try:
         mydb.database = name
         print('Connection established')
+
+        if transaction:
+            mydb.autocommit = False  # Disable autocommit to enable transactions
+        
         return mydb
-    except mysql.connector.errors.DatabaseError:
-        print('Database does not exist')
-    except (mysql.connector.errors.InterfaceError, mysql.connector.errors.ProgrammingError) as e:
+    except mysql.connector.Error as e:
+        print(f"Error connecting to {name}: {e}")
+    except (mysql.connector.InterfaceError, mysql.connector.ProgrammingError) as e:
         print(f'Connection error: {e}')
     except Exception as e:
         print(f'Something else went wrong: {e}')
     return None
 
+
+
 def show_tables(mydb):
-    cursor = mydb.cursor()
-    cursor.execute("SHOW TABLES")
-    tables = [table[0] for table in cursor]
-    print(tables)
-    return tables
+    try:
+        cursor = mydb.cursor()
+        cursor.execute("SHOW TABLES")
+        tables = [table[0] for table in cursor]
+        print(tables)
+        return tables
+    except mysql.connector.Error as e:
+        print(f"Error while showing tables: {e}")
+        return []
+    
+def create_table(mydb, table_name, columns, transaction=False):
+    cursor = mydb.cursor()
+    column_definitions = ", ".join(columns)
+    create_table_query = f"CREATE TABLE {table_name} ({column_definitions})"
+    print(f'Executing command: {create_table_query}')
+    try:
+        if transaction:
+            mydb.start_transaction()  # Start the transaction explicitly
+            
+        cursor.execute(create_table_query)
+        
+        if transaction:
+            mydb.commit()  # Commit the transaction if transaction=True
+            
+        print(f'Table {table_name} created successfully!')
+    except mysql.connector.Error as e:
+        if transaction:
+            mydb.rollback()  # Roll back the transaction if an error occurs
+        print(f"Error creating table: {e}")
 
-def show_databases(mydb):
+def drop_table(mydb, table_name, transaction=False):
     cursor = mydb.cursor()
-    cursor.execute("SHOW DATABASES")
-    databases = [database[0] for database in cursor]
-    print(databases)
-    return databases
+    drop_table_query = f'DROP TABLE IF EXISTS {table_name}'
+    print(f'Executing command: {drop_table_query}')
+    try:
+        if transaction:
+            mydb.start_transaction()  # Start the transaction explicitly
+            
+        cursor.execute(drop_table_query)
+        
+        if transaction:
+            mydb.commit()  # Commit the transaction if transaction=True
+            
+        print(f'Table {table_name} dropped successfully!')
+    except mysql.connector.Error as e:
+        if transaction:
+            mydb.rollback()  # Roll back the transaction if an error occurs
+        print(f"Error dropping table: {e}")
+
 
 
+def show_databases(mydb):
+    try:
+        cursor = mydb.cursor()
+        cursor.execute("SHOW DATABASES")
+        databases = [database[0] for database in cursor]
+        print(databases)
+        return databases
+    except mysql.connector.Error as e:
+        print(f"Error while showing databases: {e}")
+        return []
 
 def select_data(mydb, table_name, columns):
-    cursor = mydb.cursor()
-    column_list = ", ".join(columns)
-    select_query = f"SELECT {column_list} FROM {table_name}"
-    cursor.execute(select_query)
-    row = cursor.fetchone()
-    while row is not None:
-        yield row
+    try:
+        cursor = mydb.cursor()
+        column_list = ", ".join(columns)
+        select_query = f"SELECT {column_list} FROM {table_name}"
+        cursor.execute(select_query)
         row = cursor.fetchone()
+        while row is not None:
+            yield row
+            row = cursor.fetchone()
+    except mysql.connector.Error as e:
+        print(f"Error while selecting data: {e}")
+        return
 
-def insert_data(mydb, table_name, values):
-    cursor = mydb.cursor()
-    value_list = ", ".join(["%s"] * len(values))
-    insert_query = f"INSERT INTO {table_name} VALUES ({value_list})"
+def insert_data(mydb, table_name, values, transaction=False):
     try:
+        cursor = mydb.cursor()
+        value_list = ", ".join(["%s"] * len(values))
+        insert_query = f"INSERT INTO {table_name} VALUES ({value_list})"
+        
+        if transaction:
+            mydb.start_transaction()  # Start the transaction explicitly
+            
         cursor.execute(insert_query, values)
-        mydb.commit()
+        
+        if transaction:
+            mydb.commit()  # Commit the transaction if transaction=True
+            
         print("Data inserted successfully!")
-    except Exception as e:
+        
+    except mysql.connector.Error as e:
+        if transaction:
+            mydb.rollback()  # Roll back the transaction if an error occurs
         print(f"Error inserting data: {e}")
 
-def drop_table(mydb, table_name):
-    cursor = mydb.cursor()
-    drop_query = f"DROP TABLE IF EXISTS {table_name}"
-    try:
-        cursor.execute(drop_query)
-        mydb.commit()
-        print(f"Table {table_name} dropped successfully!")
-    except mysql.connector.errors.ProgrammingError:
-        print(f"Table {table_name} does not exist")
-    except Exception as e:
-        print(f"Something else went wrong: {e}")
 
-def delete_data(mydb, table_name, condition):
-    cursor = mydb.cursor()
-    delete_query = f"DELETE FROM {table_name} WHERE {condition}"
+
+
+def delete_data(mydb, table_name, condition, transaction=False):
     try:
+        cursor = mydb.cursor()
+        delete_query = f"DELETE FROM {table_name} WHERE {condition}"
+        
+        if transaction:
+            mydb.start_transaction()  # Start the transaction explicitly
+            
         cursor.execute(delete_query)
-        mydb.commit()
+        
+        if transaction:
+            mydb.commit()  # Commit the transaction if transaction=True
+            
         print(f"{cursor.rowcount} row(s) deleted successfully!")
-    except Exception as e:
+        
+    except mysql.connector.Error as e:
+        if transaction:
+            mydb.rollback()  # Roll back the transaction if an error occurs
         print(f"Error deleting data: {e}")
 
-def update_data(mydb, table_name, column_values, condition):
-    cursor = mydb.cursor()
-    column_value_pairs = [f"{col} = %s" for col in column_values.keys()]
-    set_clause = ", ".join(column_value_pairs)
-    update_query = f"UPDATE {table_name} SET {set_clause} WHERE {condition}"
+
+def update_data(mydb, table_name, column_values, condition, transaction=False):
     try:
+        cursor = mydb.cursor()
+        column_value_pairs = [f"{col} = %s" for col in column_values.keys()]
+        set_clause = ", ".join(column_value_pairs)
+        update_query = f"UPDATE {table_name} SET {set_clause} WHERE {condition}"
+        
+        if transaction:
+            mydb.start_transaction()  # Start the transaction explicitly
+            
         cursor.execute(update_query, tuple(column_values.values()))
-        mydb.commit()
+        
+        if transaction:
+            mydb.commit()  # Commit the transaction if transaction=True
+            
         print(f"{cursor.rowcount} row(s) updated successfully!")
-    except Exception as e:
+        
+    except mysql.connector.Error as e:
+        if transaction:
+            mydb.rollback()  # Roll back the transaction if an error occurs
         print(f"Error updating data: {e}")
 
-def execute_query(mydb, query, fetch=False):
-    cursor = mydb.cursor()
+
+def execute_query(mydb, query, fetch=False, transaction=False):
     try:
+        cursor = mydb.cursor()
+        
+        if transaction:
+            mydb.start_transaction()  # Start the transaction explicitly
+            
         cursor.execute(query)
-        mydb.commit()
+        
+        if transaction:
+            mydb.commit()  # Commit the transaction if transaction=True
+            
         if fetch:
             results = cursor.fetchall()
             return results
         else:
             print(f"{cursor.rowcount} row(s) affected!")
-    except Exception as e:
+            
+    except mysql.connector.Error as e:
+        if transaction:
+            mydb.rollback()  # Roll back the transaction if an error occurs
         print(f"Error executing query: {e}")
+        return []
 
-def describe_table(mydb, table_name):
-    cursor = mydb.cursor()
-    describe_query = f"DESCRIBE {table_name}"
-    cursor.execute(describe_query)
-    table_info = cursor.fetchall()
-    for info in table_info:
-        print(info)
-    return table_info
 
-def describe_database(mydb):
-    cursor = mydb.cursor()
-    cursor.execute("SELECT DATABASE()")
-    database_name = cursor.fetchone()[0]
-    print(f"Database: {database_name}")
-    print("Tables:")
-    cursor.execute("SHOW TABLES")
-    tables = [table[0] for table in cursor]
-    for table in tables:
-        describe_query = f"DESCRIBE {table}"
+def describe_table(mydb, table_name):
+    try:
+        cursor = mydb.cursor()
+        describe_query = f"DESCRIBE {table_name}"
         cursor.execute(describe_query)
         table_info = cursor.fetchall()
-        print(f"{table}:")
         for info in table_info:
             print(info)
+        return table_info
+    except mysql.connector.Error as e:
+        print(f"Error describing table: {e}")
+        return []
+
+def describe_database(mydb):
+    try:
+        cursor = mydb.cursor()
+        cursor.execute("SELECT DATABASE()")
+        database_name = cursor.fetchone()[0]
+        print(f"Database: {database_name}")
+        print("Tables:")
+        cursor.execute("SHOW TABLES")
+        tables = [table[0] for table in cursor]
+        for table in tables:
+            describe_query = f"DESCRIBE {table}"
+            cursor.execute(describe_query)
+            table_info = cursor.fetchall()
+            print(f"{table}:")
+            for info in table_info:
+                print(info)
+    except mysql.connector.Error as e:
+        print(f"Error describing database: {e}")
+
+
+########################   Start of Aggregate functions     #######################
+
+
+def select_count(connection, table, column):
+    query = f"SELECT COUNT({column}) FROM {table}"
+    result = connection.execute(query).fetchone()
+    return result[0]
+
+def select_sum(connection, table, column):
+    query = f"SELECT SUM({column}) FROM {table}"
+    result = connection.execute(query).fetchone()
+    return result[0]
+
+def select_avg(connection, table, column):
+    query = f"SELECT AVG({column}) FROM {table}"
+    result = connection.execute(query).fetchone()
+    return result[0]
+
+def select_min(connection, table, column):
+    query = f"SELECT MIN({column}) FROM {table}"
+    result = connection.execute(query).fetchone()
+    return result[0]
+
+
+def select_max(connection, table, column):
+    query = f"SELECT MAX({column}) FROM {table}"
+    result = connection.execute(query).fetchone()
+    return result[0]
+
 
+########################   End of Aggregate functions     #######################
 
+
+########################   Start of help    #######################
 def help(func=None):
     if func is None:
-        print("Available functions:")
-        print("- create_connection(): Creates a local connection to a SQLite database.")
-        print("- create_remote_connection(host, user, password): Creates a remote connection to a SQLite database on a specified host.")
+        print("LiSQL Package - Python Package for Interacting with MySQL Databases")
+        print("Version: 2.1")
+        print("Description: LiSQL is a Python package that simplifies working with MySQL databases by providing various functions for connection management, database operations, table operations, and data manipulation.")
+        print("\nAvailable functions:")
+
+        # Group 1: Connection Management
+        print("\nConnection Management:")
+        print("- create_connection(): Creates a local connection to a MySQL database.")
+        print("  Example: create_connection()")
+        print("  This function establishes a connection to a local MySQL database and returns the connection object.")
+        
+        print("- create_remote_connection(host, user, password): Creates a remote connection to a MySQL database on a specified host.")
+        print("  Example: create_remote_connection('remote_host', 'remote_user', 'remote_password')")
+        print("  This function establishes a remote connection to a MySQL database on the specified host and returns the connection object.")
+        
+        print("- connect_remote_database(host, username, password, database): Connects to a remote MySQL database on a specified host.")
+        print("  Example: connect_remote_database('remote_host', 'remote_user', 'remote_password', 'remote_db')")
+        print("  This function connects to a remote MySQL database on the specified host with the specified username, password, and database name, and returns the connection object.")
+        
+        # Group 2: Database Operations
+        print("\nDatabase Operations:")
         print("- create_database(mydb, name): Creates a new database with the specified name in the local or remote connection.")
-        print("- connect_remote_database(host, username, password, database): Connects to a remote database on a specified host.")
+        print("  Example: create_database(mydb, 'new_database')")
+        print("  This function creates a new database with the specified name in the connected local or remote MySQL connection.")
+        
         print("- drop_database(mydb, name): Deletes the database with the specified name from the local or remote connection.")
+        print("  Example: drop_database(mydb, 'existing_database')")
+        print("  This function drops the database with the specified name from the connected local or remote MySQL connection.")
+        
         print("- connect_database(mydb, name): Connects to an existing database with the specified name in the local or remote connection.")
-        print("- show_tables(mydb): Displays a list of tables in the connected database.")
+        print("  Example: connect_database(mydb, 'existing_database')")
+        print("  This function connects to an existing database with the specified name in the connected local or remote MySQL connection.")
+        
         print("- show_databases(mydb): Displays a list of all databases in the connected server.")
-        print("- select_data(mydb, table_name, columns): Retrieves data from the specified columns in the specified table.")
-        print("- insert_data(mydb, table_name, values): Inserts data into the specified table.")
-        print("- drop_table(mydb, table_name): Deletes the specified table from the connected database.")
-        print("- delete_data(mydb, table_name, condition): Deletes data from the specified table that meets the specified condition.")
-        print("- update_data(mydb, table_name, column_values, condition): Updates data in the specified table that meets the specified condition.")
-        print("- execute_query(mydb, query, fetch=False): Executes the specified SQL query.")
-        print("- describe_database(mydb): Displays information about the connected database.")
+        print("  Example: show_databases(mydb)")
+        print("  This function shows a list of all databases in the connected local or remote MySQL server.")
+
+        # Group 3: Table Operations
+        print("\nTable Operations:")
+        print("- show_tables(mydb): Displays a list of tables in the connected database.")
+        print("  Example: show_tables(mydb)")
+        print("  This function shows a list of tables in the connected local or remote MySQL database.")
+        
+        print("- create_table(mydb, table_name, columns, transaction=False): Creates a table with the specified columns.")
+        print("  Example: columns = ['id INT PRIMARY KEY', 'name VARCHAR(255)', 'age INT']")
+        print("           create_table(mydb, 'students', columns, transaction=True)")
+        print("  This function creates a new table with the specified name and columns in the connected local or remote MySQL database.")
+        
+        print("- drop_table(mydb, table_name, transaction=False): Deletes the specified table from the connected database.")
+        print("  Example: drop_table(mydb, 'students', transaction=True)")
+        print("  This function drops the specified table from the connected local or remote MySQL database.")
+
         print("- describe_table(mydb, table_name): Displays information about the specified table in the connected database.")
-    elif func == create_connection:
-        print("create_connection():\n")
-        print("Creates a local connection to a SQLite database.")
-        print("\nUsage:")
-        print("  conn = create_connection()")
-        print("\nReturns:")
-        print("  A connection object that can be used to interact with the database.")
-    elif func == create_remote_connection:
-        print("create_remote_connection(host, user, password):\n")
-        print("Creates a remote connection to a SQLite database on a specified host.")
-        print("\nArgs:")
-        print("  host (str): The host name or IP address of the server running the SQLite database.")
-        print("  user (str): The username to use when connecting to the remote database.")
-        print("  password (str): The password to use when connecting to the remote database.")
-        print("\nUsage:")
-        print("  conn = create_remote_connection('example.com', 'myuser', 'mypassword')")
-        print("\nReturns:")
-        print("  A connection object that can be used to interact with the database.")
-    elif func == create_database:
-        print("create_database(mydb, name):\n")
-        print("Creates a new database with the specified name in the local or remote connection.")
-        print("\nArgs:")
-        print("  mydb (connection object): The connection object to the database.")
-        print("  name (str): The name to use for the new database.")
-        print("\nUsage:")
-        print("  create_database(conn, 'my_new_db')")
-        print("\nReturns:")
-        print("  None")
-    elif func == connect_remote_database:
-        print("connect_remote_database(host, username, password, database):\n")
-        print("Connects to a remote database on a specified host.")
-        print("\nArgs:")
-        print("- host: The host name or IP address of the remote server.")
-        print("- username: The username used to authenticate with the remote server.")
-        print("- password: The password used to authenticate with the remote server.")
-        print("- database: The name of the remote database to connect to.")
-    elif func == drop_database:
-        print("drop_database(mydb, name):\n")
-        print("Deletes the database with the specified name from the local or remote connection.")
-        print("\nArgs:")
-        print("- mydb: The connection object created by create_connection(), create_remote_connection(), or connect_remote_database().")
-        print("- name: The name of the database to delete.")
-    elif func == connect_database:
-        print("connect_database(mydb, name):\n")
-        print("Connects to an existing database with the specified name in the local or remote connection.")
-        print("\nArgs:")
-        print("- mydb: The connection object created by create_connection(), create_remote_connection(), or connect_remote_database().")
-        print("- name: The name of the database to connect to.")
-    elif func == show_tables:
-        print("show_tables(mydb):\n")
-        print("Displays a list of tables in the connected database.")
-        print("\nArgs:")
-        print("- mydb: The connection object created by create_connection(), create_remote_connection(), or connect_remote_database().")
-    elif func == show_databases:
-        print("show_databases(mydb):\n")
-        print("Displays a list of all databases in the connected server.")
-        print("\nArgs:")
-        print("- mydb: The connection object created by create_connection(), create_remote_connection(), or connect_remote_database().")
-    elif func == select_data:
-        print("select_data(mydb, table_name, columns):\n")
-        print("Retrieves data from the specified columns in the specified table.")
-        print("\nArgs:")
-        print("- mydb: The connection object created by create_connection(), create_remote_connection(), or connect_remote_database().")
-        print("- table_name: The name of the table to retrieve data from.")
-        print("- columns: A list of column names to retrieve data from. If not specified, all columns will be returned.")
-    elif func == insert_data:
-        print("insert_data(mydb, table_name, values):\n")
-        print("Inserts data into the specified table.")
-        print("\nArgs:")
-        print("- mydb: The connection object created by create_connection(), create_remote_connection(), or connect_remote_database().")
-        print("- table_name: The name of the table to insert data into.")
-        print("- values: A list of tuples, where each tuple represents a row of data to be inserted.")
-    elif func == drop_table:
-        print("drop_table(mydb, table_name):\n")
-        print("Deletes the specified table from the connected database.")
-        print("\nArgs:")
-        print("- mydb: The connection object created by create_connection(), create_remote_connection(), or connect_remote_database().")
-        print("- table_name: The name of the table to delete.")
-    elif func == delete_data:
-        print("delete_data(mydb, table_name, condition):\n")
-        print("Deletes data from the specified table that meets the specified condition.")
-        print("\nArgs:")
-        print("- mydb: the database connection object.")
-        print("- table_name: the name of the table to delete data from.")
-        print("- condition: the condition that data must meet in order to be deleted.")
-
-    elif func == update_data:
-        print("update_data(mydb, table_name, column_values, condition):\n")
-        print("Updates data in the specified table that meets the specified condition.")
-        print("\nArgs:")
-        print("- mydb: the database connection object.")
-        print("- table_name: the name of the table to update data in.")
-        print("- column_values: a dictionary containing the column names and values to update.")
-        print("- condition: the condition that data must meet in order to be updated.")
-
-    elif func == execute_query:
-        print("execute_query(mydb, query, fetch=False):\n")
-        print("Executes the specified SQL query.")
-        print("\nArgs:")
-        print("- mydb: the database connection object.")
-        print("- query: the SQL query to execute.")
-        print("- fetch: a boolean indicating whether or not to fetch the results of the query.")
-
-    elif func == describe_database:
-        print("describe_database(mydb):\n")
-        print("Displays information about the connected database.")
-        print("\nArgs:")
-        print("- mydb: the database connection object.")
-
-    elif func == describe_table:
-        print("describe_table(mydb, table_name):\n")
-        print("Displays information about the specified table in the connected database.")
-        print("\nArgs:")
-        print("- mydb: the database connection object.")
-        print("- table_name: the name of the table to describe.")
+        print("  Example: describe_table(mydb, 'students')")
+        print("  This function describes the specified table in the connected local or remote MySQL database.")
+
+        # Group 4: Data Manipulation
+        print("\nData Manipulation:")
+        print("- select_data(mydb, table_name, columns): Retrieves data from the specified columns in the specified table.")
+        print("  Example: columns = ['name', 'age']")
+        print("           for data in select_data(mydb, 'students', columns):")
+        print("               print(data)")
+        print("  This function retrieves data from the specified columns in the specified table in the connected local or remote MySQL database.")
+        
+        print("- insert_data(mydb, table_name, values, transaction=False): Inserts data into the specified table.")
+        print("  Example: values = (1, 'John Doe', 25)")
+        print("           insert_data(mydb, 'students', values, transaction=True)")
+        print("  This function inserts data into the specified table in the connected local or remote MySQL database.")
+        
+        print("- delete_data(mydb, table_name, condition, transaction=False): Deletes data from the specified table that meets the specified condition.")
+        print("  Example: condition = 'age > 30'")
+        print("           delete_data(mydb, 'students', condition, transaction=True)")
+        print("  This function deletes data from the specified table that meets the specified condition in the connected local or remote MySQL database.")
+        
+        print("- update_data(mydb, table_name, column_values, condition, transaction=False): Updates data in the specified table that meets the specified condition.")
+        print("  Example: column_values = {'name': 'John Smith', 'age': 32}")
+        print("           condition = 'id = 1'")
+        print("           update_data(mydb, 'students', column_values, condition, transaction=True)")
+        print("  This function updates data in the specified table that meets the specified condition in the connected local or remote MySQL database.")
+        
+        print("- execute_query(mydb, query, fetch=False, transaction=False): Executes the specified SQL query.")
+        print("  Example: query = 'SELECT * FROM students'")
+        print("           execute_query(mydb, query, fetch=True)")
+        print("  This function executes the specified SQL query in the connected local or remote MySQL database.")
+        
+        # Group 5: Aggregate Functions
+        print("\nAggregate Functions:")
+        print("- select_count(connection, table, column): Calculates the COUNT of records in the specified column of the table.")
+        print("  Example: count = select_count(mydb, 'students', 'id')")
+        print("  This function calculates the COUNT of records in the specified column of the table in the connected local or remote MySQL database.")
+        
+        print("- select_sum(connection, table, column): Calculates the SUM of values in the specified column of the table.")
+        print("  Example: total_age = select_sum(mydb, 'students', 'age')")
+        print("  This function calculates the SUM of values in the specified column of the table in the connected local or remote MySQL database.")
+        
+        print("- select_avg(connection, table, column): Calculates the AVG of values in the specified column of the table.")
+        print("  Example: avg_age = select_avg(mydb, 'students', 'age')")
+        print("  This function calculates the AVG of values in the specified column of the table in the connected local or remote MySQL database.")
+        
+        print("- select_min(connection, table, column): Retrieves the minimum value in the specified column of the table.")
+        print("  Example: min_age = select_min(mydb, 'students', 'age')")
+        print("  This function retrieves the minimum value in the specified column of the table in the connected local or remote MySQL database.")
+        
+        print("- select_max(connection, table, column): Retrieves the maximum value in the specified column of the table.")
+        print("  Example: max_age = select_max(mydb, 'students', 'age')")
+        print("  This function retrieves the maximum value in the specified column of the table in the connected local or remote MySQL database.")
+        
+        # Transaction Support Examples
+        print("\nTransaction Support")
+        print("Here are the functions in LiSQL that support Transaction Support:")
+        print("- create_database(mydb, name, transaction=False)")
+        print("- drop_database(mydb, name, transaction=False)")
+        print("- create_table(mydb, table_name, columns, transaction=False)")
+        print("- drop_table(mydb, table_name, transaction=False)")
+        print("- insert_data(mydb, table_name, values, transaction=False)")
+        print("- delete_data(mydb, table_name, condition, transaction=False)")
+        print("- update_data(mydb, table_name, column_values, condition, transaction=False)")
+        print("- execute_query(mydb, query, fetch=False, transaction=False)")
+        print("Remember that you need to pass transaction=True as an argument to these functions to enable Transaction Support. This ensures that the operations are executed as part of a single transaction, providing data consistency and rollback capabilities in case of errors.")
+        print("- Example 1: Creating a table with transaction support")
+        print("  columns = ['id INT PRIMARY KEY', 'name VARCHAR(255)', 'age INT']")
+        print("  create_table(mydb, 'students', columns, transaction=True)")
+        print("  # This will create a new table 'students' with the specified columns.")
+        print("  # The transaction will ensure that the table is created only if the entire operation is successful.")
+        
+        print("\n- Example 2: Dropping a table with transaction support")
+        print("  drop_table(mydb, 'students', transaction=True)")
+        print("  # This will drop the table 'students' from the database.")
+        print("  # The transaction will ensure that the table is dropped only if the entire operation is successful.")
+
+        print("\nNote: When transaction=True is passed as an argument to the functions that support it, the function will start a transaction, execute the query, and then commit the transaction. If an error occurs, it will roll back the transaction.")
+
+########################   End of help    #######################
+
+def __version__():
+    return 2.1
```

