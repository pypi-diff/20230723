# Comparing `tmp/FirebaseDatabaseTakeover-1.0.0.tar.gz` & `tmp/FirebaseDatabaseTakeover-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "FirebaseDatabaseTakeover-1.0.0.tar", last modified: Sun Jul 23 14:36:24 2023, max compression
+gzip compressed data, was "FirebaseDatabaseTakeover-1.0.1.tar", last modified: Sun Jul 23 14:40:55 2023, max compression
```

## Comparing `FirebaseDatabaseTakeover-1.0.0.tar` & `FirebaseDatabaseTakeover-1.0.1.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:36:24.367168 FirebaseDatabaseTakeover-1.0.0/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:36:24.363168 FirebaseDatabaseTakeover-1.0.0/FirebaseDatabaseTakeover.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4874 2023-07-23 14:36:24.000000 FirebaseDatabaseTakeover-1.0.0/FirebaseDatabaseTakeover.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      348 2023-07-23 14:36:24.000000 FirebaseDatabaseTakeover-1.0.0/FirebaseDatabaseTakeover.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:36:24.000000 FirebaseDatabaseTakeover-1.0.0/FirebaseDatabaseTakeover.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       42 2023-07-23 14:36:24.000000 FirebaseDatabaseTakeover-1.0.0/FirebaseDatabaseTakeover.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-07-23 14:36:24.000000 FirebaseDatabaseTakeover-1.0.0/FirebaseDatabaseTakeover.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-23 14:36:24.000000 FirebaseDatabaseTakeover-1.0.0/FirebaseDatabaseTakeover.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-07-23 14:36:13.000000 FirebaseDatabaseTakeover-1.0.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     4874 2023-07-23 14:36:24.367168 FirebaseDatabaseTakeover-1.0.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4795 2023-07-23 14:36:13.000000 FirebaseDatabaseTakeover-1.0.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:36:24.367168 FirebaseDatabaseTakeover-1.0.0/fdt/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 14:36:13.000000 FirebaseDatabaseTakeover-1.0.0/fdt/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5167 2023-07-23 14:36:13.000000 FirebaseDatabaseTakeover-1.0.0/fdt/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 14:36:24.367168 FirebaseDatabaseTakeover-1.0.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     5166 2023-07-23 14:36:13.000000 FirebaseDatabaseTakeover-1.0.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:40:55.611001 FirebaseDatabaseTakeover-1.0.1/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:40:55.607001 FirebaseDatabaseTakeover-1.0.1/FirebaseDatabaseTakeover.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4963 2023-07-23 14:40:55.000000 FirebaseDatabaseTakeover-1.0.1/FirebaseDatabaseTakeover.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      348 2023-07-23 14:40:55.000000 FirebaseDatabaseTakeover-1.0.1/FirebaseDatabaseTakeover.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:40:55.000000 FirebaseDatabaseTakeover-1.0.1/FirebaseDatabaseTakeover.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       42 2023-07-23 14:40:55.000000 FirebaseDatabaseTakeover-1.0.1/FirebaseDatabaseTakeover.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-07-23 14:40:55.000000 FirebaseDatabaseTakeover-1.0.1/FirebaseDatabaseTakeover.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-23 14:40:55.000000 FirebaseDatabaseTakeover-1.0.1/FirebaseDatabaseTakeover.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-07-23 14:40:41.000000 FirebaseDatabaseTakeover-1.0.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     4963 2023-07-23 14:40:55.607001 FirebaseDatabaseTakeover-1.0.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4727 2023-07-23 14:40:41.000000 FirebaseDatabaseTakeover-1.0.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:40:55.607001 FirebaseDatabaseTakeover-1.0.1/fdt/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 14:40:41.000000 FirebaseDatabaseTakeover-1.0.1/fdt/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5167 2023-07-23 14:40:41.000000 FirebaseDatabaseTakeover-1.0.1/fdt/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 14:40:55.611001 FirebaseDatabaseTakeover-1.0.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     5255 2023-07-23 14:40:41.000000 FirebaseDatabaseTakeover-1.0.1/setup.py
```

### Comparing `FirebaseDatabaseTakeover-1.0.0/FirebaseDatabaseTakeover.egg-info/PKG-INFO` & `FirebaseDatabaseTakeover-1.0.1/FirebaseDatabaseTakeover.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: FirebaseDatabaseTakeover
-Version: 1.0.0
+Version: 1.0.1
 Summary: Firebase Database Takeover tool
 Author: Akhil Koradiya
 Author-email: akhil.koradiya.21@gmail.com
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Firebase Database Takeover (FDT)
 
-[![MIT License](https://img.shields.io/badge/License-MIT-green)](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/LICENSE)
+[![MIT License](https://img.shields.io/badge/License-MIT-green)](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/blob/main/LICENSE)
 [![YouTube Channel](https://img.shields.io/badge/YouTube-Subscribe-red)](https://www.youtube.com/@hackerno21)
 [![Twitter Follow](https://img.shields.io/twitter/follow/mytwitterhandle?label=Follow%20on%20Twitter&style=social)](https://twitter.com/akhilkoradiya21)
 [![LinkedIn Connect](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://in.linkedin.com/in/akhil-koradiya-2722a51a0)
 [![GitHub Follow](https://img.shields.io/github/followers/mygithubusername?label=Follow%20on%20GitHub&style=social)](https://github.com/akhilkoradiya)
 
 FDT stands for Firebase Database Takeover, an automation tool used to assess the vulnerability of Firebase databases for potential exploitation. Firebase Database Takeover is a Python script specifically developed for this purpose. By analyzing the given Firebase database URL, the script determines whether it is susceptible to a takeover. In the event of a vulnerability, the script empowers attackers to inject custom data into the database, offering them an option to exploit it. Additionally, the script provides a proof-of-concept URL as evidence of the exploit.
 
@@ -71,15 +71,15 @@
 fdt <add_your_firebase_database_url>
 ``` 
 
 ## Disclaimer
 This script is intended for educational and testing purposes only. The author is not responsible for any misuse or damage caused by the usage of this script. Use it at your own risk.
 
 ## License
-This project is licensed under the MIT License.
+This project is licensed under the [MIT License](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/blob/main/LICENSE).
 
 ## Author
 
 Firebase Database Takeover is developed by **Akhil Koradiya.**
 
 Follow me on:
```

#### html2text {}

```diff
@@ -1,15 +1,15 @@
-Metadata-Version: 2.1 Name: FirebaseDatabaseTakeover Version: 1.0.0 Summary:
+Metadata-Version: 2.1 Name: FirebaseDatabaseTakeover Version: 1.0.1 Summary:
 Firebase Database Takeover tool Author: Akhil Koradiya Author-email:
 akhil.koradiya.21@gmail.com Description-Content-Type: text/markdown License-
 File: LICENSE # Firebase Database Takeover (FDT) [![MIT License](https://
 img.shields.io/badge/License-MIT-green)](https://github.com/akhilkoradiya/
-FirebaseDatabaseTakeover/LICENSE) [![YouTube Channel](https://img.shields.io/
-badge/YouTube-Subscribe-red)](https://www.youtube.com/@hackerno21) [![Twitter
-Follow](https://img.shields.io/twitter/follow/
+FirebaseDatabaseTakeover/blob/main/LICENSE) [![YouTube Channel](https://
+img.shields.io/badge/YouTube-Subscribe-red)](https://www.youtube.com/
+@hackerno21) [![Twitter Follow](https://img.shields.io/twitter/follow/
 mytwitterhandle?label=Follow%20on%20Twitter&style=social)](https://twitter.com/
 akhilkoradiya21) [![LinkedIn Connect](https://img.shields.io/badge/LinkedIn-
 Connect-blue?logo=linkedin)](https://in.linkedin.com/in/akhil-koradiya-
 2722a51a0) [![GitHub Follow](https://img.shields.io/github/followers/
 mygithubusername?label=Follow%20on%20GitHub&style=social)](https://github.com/
 akhilkoradiya) FDT stands for Firebase Database Takeover, an automation tool
 used to assess the vulnerability of Firebase databases for potential
@@ -54,11 +54,13 @@
 colorama library is used for colored terminal output. Install it using the
 following command: ```pip install colorama``` ## Installation To use FDT, you
 need to have Python installed on your system. Follow these steps to install and
 use FDT: ``` pip install FirebaseDatabaseTakeover ``` ## Usage ``` fdt  ``` ##
 Disclaimer This script is intended for educational and testing purposes only.
 The author is not responsible for any misuse or damage caused by the usage of
 this script. Use it at your own risk. ## License This project is licensed under
-the MIT License. ## Author Firebase Database Takeover is developed by **Akhil
-Koradiya.** Follow me on: - YouTube: https://www.youtube.com/@hackerno21 -
-GitHub: https://github.com/akhilkoradiya - Twitter: https://twitter.com/
-akhilkoradiya21 - Linkedin: https://in.linkedin.com/in/akhil-koradiya-2722a51a0
+the [MIT License](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/
+blob/main/LICENSE). ## Author Firebase Database Takeover is developed by
+**Akhil Koradiya.** Follow me on: - YouTube: https://www.youtube.com/
+@hackerno21 - GitHub: https://github.com/akhilkoradiya - Twitter: https://
+twitter.com/akhilkoradiya21 - Linkedin: https://in.linkedin.com/in/akhil-
+koradiya-2722a51a0
```

### Comparing `FirebaseDatabaseTakeover-1.0.0/LICENSE` & `FirebaseDatabaseTakeover-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `FirebaseDatabaseTakeover-1.0.0/PKG-INFO` & `FirebaseDatabaseTakeover-1.0.1/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: FirebaseDatabaseTakeover
-Version: 1.0.0
+Version: 1.0.1
 Summary: Firebase Database Takeover tool
 Author: Akhil Koradiya
 Author-email: akhil.koradiya.21@gmail.com
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Firebase Database Takeover (FDT)
 
-[![MIT License](https://img.shields.io/badge/License-MIT-green)](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/LICENSE)
+[![MIT License](https://img.shields.io/badge/License-MIT-green)](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/blob/main/LICENSE)
 [![YouTube Channel](https://img.shields.io/badge/YouTube-Subscribe-red)](https://www.youtube.com/@hackerno21)
 [![Twitter Follow](https://img.shields.io/twitter/follow/mytwitterhandle?label=Follow%20on%20Twitter&style=social)](https://twitter.com/akhilkoradiya21)
 [![LinkedIn Connect](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://in.linkedin.com/in/akhil-koradiya-2722a51a0)
 [![GitHub Follow](https://img.shields.io/github/followers/mygithubusername?label=Follow%20on%20GitHub&style=social)](https://github.com/akhilkoradiya)
 
 FDT stands for Firebase Database Takeover, an automation tool used to assess the vulnerability of Firebase databases for potential exploitation. Firebase Database Takeover is a Python script specifically developed for this purpose. By analyzing the given Firebase database URL, the script determines whether it is susceptible to a takeover. In the event of a vulnerability, the script empowers attackers to inject custom data into the database, offering them an option to exploit it. Additionally, the script provides a proof-of-concept URL as evidence of the exploit.
 
@@ -71,15 +71,15 @@
 fdt <add_your_firebase_database_url>
 ``` 
 
 ## Disclaimer
 This script is intended for educational and testing purposes only. The author is not responsible for any misuse or damage caused by the usage of this script. Use it at your own risk.
 
 ## License
-This project is licensed under the MIT License.
+This project is licensed under the [MIT License](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/blob/main/LICENSE).
 
 ## Author
 
 Firebase Database Takeover is developed by **Akhil Koradiya.**
 
 Follow me on:
```

#### html2text {}

```diff
@@ -1,15 +1,15 @@
-Metadata-Version: 2.1 Name: FirebaseDatabaseTakeover Version: 1.0.0 Summary:
+Metadata-Version: 2.1 Name: FirebaseDatabaseTakeover Version: 1.0.1 Summary:
 Firebase Database Takeover tool Author: Akhil Koradiya Author-email:
 akhil.koradiya.21@gmail.com Description-Content-Type: text/markdown License-
 File: LICENSE # Firebase Database Takeover (FDT) [![MIT License](https://
 img.shields.io/badge/License-MIT-green)](https://github.com/akhilkoradiya/
-FirebaseDatabaseTakeover/LICENSE) [![YouTube Channel](https://img.shields.io/
-badge/YouTube-Subscribe-red)](https://www.youtube.com/@hackerno21) [![Twitter
-Follow](https://img.shields.io/twitter/follow/
+FirebaseDatabaseTakeover/blob/main/LICENSE) [![YouTube Channel](https://
+img.shields.io/badge/YouTube-Subscribe-red)](https://www.youtube.com/
+@hackerno21) [![Twitter Follow](https://img.shields.io/twitter/follow/
 mytwitterhandle?label=Follow%20on%20Twitter&style=social)](https://twitter.com/
 akhilkoradiya21) [![LinkedIn Connect](https://img.shields.io/badge/LinkedIn-
 Connect-blue?logo=linkedin)](https://in.linkedin.com/in/akhil-koradiya-
 2722a51a0) [![GitHub Follow](https://img.shields.io/github/followers/
 mygithubusername?label=Follow%20on%20GitHub&style=social)](https://github.com/
 akhilkoradiya) FDT stands for Firebase Database Takeover, an automation tool
 used to assess the vulnerability of Firebase databases for potential
@@ -54,11 +54,13 @@
 colorama library is used for colored terminal output. Install it using the
 following command: ```pip install colorama``` ## Installation To use FDT, you
 need to have Python installed on your system. Follow these steps to install and
 use FDT: ``` pip install FirebaseDatabaseTakeover ``` ## Usage ``` fdt  ``` ##
 Disclaimer This script is intended for educational and testing purposes only.
 The author is not responsible for any misuse or damage caused by the usage of
 this script. Use it at your own risk. ## License This project is licensed under
-the MIT License. ## Author Firebase Database Takeover is developed by **Akhil
-Koradiya.** Follow me on: - YouTube: https://www.youtube.com/@hackerno21 -
-GitHub: https://github.com/akhilkoradiya - Twitter: https://twitter.com/
-akhilkoradiya21 - Linkedin: https://in.linkedin.com/in/akhil-koradiya-2722a51a0
+the [MIT License](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/
+blob/main/LICENSE). ## Author Firebase Database Takeover is developed by
+**Akhil Koradiya.** Follow me on: - YouTube: https://www.youtube.com/
+@hackerno21 - GitHub: https://github.com/akhilkoradiya - Twitter: https://
+twitter.com/akhilkoradiya21 - Linkedin: https://in.linkedin.com/in/akhil-
+koradiya-2722a51a0
```

### Comparing `FirebaseDatabaseTakeover-1.0.0/README.md` & `FirebaseDatabaseTakeover-1.0.1/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # Firebase Database Takeover (FDT)
 
-[![MIT License](https://img.shields.io/badge/License-MIT-green)]([https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/LICENSE](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/blob/main/LICENSE))
+[![MIT License](https://img.shields.io/badge/License-MIT-green)](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/blob/main/LICENSE))
 [![YouTube Channel](https://img.shields.io/badge/YouTube-Subscribe-red)](https://www.youtube.com/@hackerno21)
 [![Twitter Follow](https://img.shields.io/twitter/follow/mytwitterhandle?label=Follow%20on%20Twitter&style=social)](https://twitter.com/akhilkoradiya21)
 [![LinkedIn Connect](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://in.linkedin.com/in/akhil-koradiya-2722a51a0)
 [![GitHub Follow](https://img.shields.io/github/followers/mygithubusername?label=Follow%20on%20GitHub&style=social)](https://github.com/akhilkoradiya)
 
 FDT stands for Firebase Database Takeover, an automation tool used to assess the vulnerability of Firebase databases for potential exploitation. Firebase Database Takeover is a Python script specifically developed for this purpose. By analyzing the given Firebase database URL, the script determines whether it is susceptible to a takeover. In the event of a vulnerability, the script empowers attackers to inject custom data into the database, offering them an option to exploit it. Additionally, the script provides a proof-of-concept URL as evidence of the exploit.
```

#### html2text {}

```diff
@@ -1,10 +1,9 @@
 # Firebase Database Takeover (FDT) [![MIT License](https://img.shields.io/
-badge/License-MIT-green)]([https://github.com/akhilkoradiya/
-FirebaseDatabaseTakeover/LICENSE](https://github.com/akhilkoradiya/
+badge/License-MIT-green)](https://github.com/akhilkoradiya/
 FirebaseDatabaseTakeover/blob/main/LICENSE)) [![YouTube Channel](https://
 img.shields.io/badge/YouTube-Subscribe-red)](https://www.youtube.com/
 @hackerno21) [![Twitter Follow](https://img.shields.io/twitter/follow/
 mytwitterhandle?label=Follow%20on%20Twitter&style=social)](https://twitter.com/
 akhilkoradiya21) [![LinkedIn Connect](https://img.shields.io/badge/LinkedIn-
 Connect-blue?logo=linkedin)](https://in.linkedin.com/in/akhil-koradiya-
 2722a51a0) [![GitHub Follow](https://img.shields.io/github/followers/
```

### Comparing `FirebaseDatabaseTakeover-1.0.0/fdt/__main__.py` & `FirebaseDatabaseTakeover-1.0.1/fdt/__main__.py`

 * *Files identical despite different names*

### Comparing `FirebaseDatabaseTakeover-1.0.0/setup.py` & `FirebaseDatabaseTakeover-1.0.1/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup
 
 readme = """# Firebase Database Takeover (FDT)
 
-[![MIT License](https://img.shields.io/badge/License-MIT-green)](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/LICENSE)
+[![MIT License](https://img.shields.io/badge/License-MIT-green)](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/blob/main/LICENSE)
 [![YouTube Channel](https://img.shields.io/badge/YouTube-Subscribe-red)](https://www.youtube.com/@hackerno21)
 [![Twitter Follow](https://img.shields.io/twitter/follow/mytwitterhandle?label=Follow%20on%20Twitter&style=social)](https://twitter.com/akhilkoradiya21)
 [![LinkedIn Connect](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://in.linkedin.com/in/akhil-koradiya-2722a51a0)
 [![GitHub Follow](https://img.shields.io/github/followers/mygithubusername?label=Follow%20on%20GitHub&style=social)](https://github.com/akhilkoradiya)
 
 FDT stands for Firebase Database Takeover, an automation tool used to assess the vulnerability of Firebase databases for potential exploitation. Firebase Database Takeover is a Python script specifically developed for this purpose. By analyzing the given Firebase database URL, the script determines whether it is susceptible to a takeover. In the event of a vulnerability, the script empowers attackers to inject custom data into the database, offering them an option to exploit it. Additionally, the script provides a proof-of-concept URL as evidence of the exploit.
 
@@ -64,15 +64,15 @@
 fdt <add_your_firebase_database_url>
 ``` 
 
 ## Disclaimer
 This script is intended for educational and testing purposes only. The author is not responsible for any misuse or damage caused by the usage of this script. Use it at your own risk.
 
 ## License
-This project is licensed under the MIT License.
+This project is licensed under the [MIT License](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/blob/main/LICENSE).
 
 ## Author
 
 Firebase Database Takeover is developed by **Akhil Koradiya.**
 
 Follow me on:
 
@@ -80,15 +80,15 @@
 - GitHub: https://github.com/akhilkoradiya
 - Twitter: https://twitter.com/akhilkoradiya21
 - Linkedin: https://in.linkedin.com/in/akhil-koradiya-2722a51a0
 """
 
 setup(
     name="FirebaseDatabaseTakeover",
-    version="1.0.0",
+    version="1.0.1",
     author="Akhil Koradiya",
     author_email="akhil.koradiya.21@gmail.com",
     description="Firebase Database Takeover tool",
     long_description=readme,
     long_description_content_type='text/markdown',
     py_modules=["fdt.__main__"],
     install_requires=[
```

#### html2text {}

```diff
@@ -1,16 +1,16 @@
 from setuptools import setup readme = """# Firebase Database Takeover (FDT) [!
 [MIT License](https://img.shields.io/badge/License-MIT-green)](https://
-github.com/akhilkoradiya/FirebaseDatabaseTakeover/LICENSE) [![YouTube Channel]
-(https://img.shields.io/badge/YouTube-Subscribe-red)](https://www.youtube.com/
-@hackerno21) [![Twitter Follow](https://img.shields.io/twitter/follow/
-mytwitterhandle?label=Follow%20on%20Twitter&style=social)](https://twitter.com/
-akhilkoradiya21) [![LinkedIn Connect](https://img.shields.io/badge/LinkedIn-
-Connect-blue?logo=linkedin)](https://in.linkedin.com/in/akhil-koradiya-
-2722a51a0) [![GitHub Follow](https://img.shields.io/github/followers/
+github.com/akhilkoradiya/FirebaseDatabaseTakeover/blob/main/LICENSE) [![YouTube
+Channel](https://img.shields.io/badge/YouTube-Subscribe-red)](https://
+www.youtube.com/@hackerno21) [![Twitter Follow](https://img.shields.io/twitter/
+follow/mytwitterhandle?label=Follow%20on%20Twitter&style=social)](https://
+twitter.com/akhilkoradiya21) [![LinkedIn Connect](https://img.shields.io/badge/
+LinkedIn-Connect-blue?logo=linkedin)](https://in.linkedin.com/in/akhil-
+koradiya-2722a51a0) [![GitHub Follow](https://img.shields.io/github/followers/
 mygithubusername?label=Follow%20on%20GitHub&style=social)](https://github.com/
 akhilkoradiya) FDT stands for Firebase Database Takeover, an automation tool
 used to assess the vulnerability of Firebase databases for potential
 exploitation. Firebase Database Takeover is a Python script specifically
 developed for this purpose. By analyzing the given Firebase database URL, the
 script determines whether it is susceptible to a takeover. In the event of a
 vulnerability, the script empowers attackers to inject custom data into the
@@ -51,17 +51,18 @@
 colorama library is used for colored terminal output. Install it using the
 following command: ```pip install colorama``` ## Installation To use FDT, you
 need to have Python installed on your system. Follow these steps to install and
 use FDT: ``` pip install FirebaseDatabaseTakeover ``` ## Usage ``` fdt  ``` ##
 Disclaimer This script is intended for educational and testing purposes only.
 The author is not responsible for any misuse or damage caused by the usage of
 this script. Use it at your own risk. ## License This project is licensed under
-the MIT License. ## Author Firebase Database Takeover is developed by **Akhil
-Koradiya.** Follow me on: - YouTube: https://www.youtube.com/@hackerno21 -
-GitHub: https://github.com/akhilkoradiya - Twitter: https://twitter.com/
-akhilkoradiya21 - Linkedin: https://in.linkedin.com/in/akhil-koradiya-2722a51a0
-""" setup( name="FirebaseDatabaseTakeover", version="1.0.0", author="Akhil
-Koradiya", author_email="akhil.koradiya.21@gmail.com", description="Firebase
-Database Takeover tool", long_description=readme,
+the [MIT License](https://github.com/akhilkoradiya/FirebaseDatabaseTakeover/
+blob/main/LICENSE). ## Author Firebase Database Takeover is developed by
+**Akhil Koradiya.** Follow me on: - YouTube: https://www.youtube.com/
+@hackerno21 - GitHub: https://github.com/akhilkoradiya - Twitter: https://
+twitter.com/akhilkoradiya21 - Linkedin: https://in.linkedin.com/in/akhil-
+koradiya-2722a51a0 """ setup( name="FirebaseDatabaseTakeover", version="1.0.1",
+author="Akhil Koradiya", author_email="akhil.koradiya.21@gmail.com",
+description="Firebase Database Takeover tool", long_description=readme,
 long_description_content_type='text/markdown', py_modules=["fdt.__main__"],
 install_requires=[ "requests", "colorama" ], entry_points={ "console_scripts":
 [ "fdt = fdt.__main__:main", ], }, )
```

