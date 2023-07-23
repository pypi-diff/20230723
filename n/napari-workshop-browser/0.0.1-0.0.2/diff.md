# Comparing `tmp/napari-workshop-browser-0.0.1.tar.gz` & `tmp/napari-workshop-browser-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "napari-workshop-browser-0.0.1.tar", last modified: Wed Jul  5 20:39:01 2023, max compression
+gzip compressed data, was "napari-workshop-browser-0.0.2.tar", last modified: Sun Jul 23 18:46:18 2023, max compression
```

## Comparing `napari-workshop-browser-0.0.1.tar` & `napari-workshop-browser-0.0.2.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-05 20:39:01.051056 napari-workshop-browser-0.0.1/
--rw-r--r--   0 kharrington   (503) staff       (20)     1490 2023-07-05 16:05:24.000000 napari-workshop-browser-0.0.1/LICENSE
--rw-r--r--   0 kharrington   (503) staff       (20)       96 2023-07-05 16:05:24.000000 napari-workshop-browser-0.0.1/MANIFEST.in
--rw-r--r--   0 kharrington   (503) staff       (20)     4077 2023-07-05 20:39:01.051121 napari-workshop-browser-0.0.1/PKG-INFO
--rw-r--r--   0 kharrington   (503) staff       (20)     2777 2023-07-05 16:05:24.000000 napari-workshop-browser-0.0.1/README.md
--rw-r--r--   0 kharrington   (503) staff       (20)     1177 2023-07-05 16:05:24.000000 napari-workshop-browser-0.0.1/pyproject.toml
--rw-r--r--   0 kharrington   (503) staff       (20)     1794 2023-07-05 20:39:01.051443 napari-workshop-browser-0.0.1/setup.cfg
-drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-05 20:39:01.047783 napari-workshop-browser-0.0.1/src/
-drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-05 20:39:01.049468 napari-workshop-browser-0.0.1/src/napari_workshop_browser/
--rw-r--r--   0 kharrington   (503) staff       (20)       95 2023-07-05 20:25:28.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser/__init__.py
-drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-05 20:39:01.050702 napari-workshop-browser-0.0.1/src/napari_workshop_browser/_tests/
--rw-r--r--   0 kharrington   (503) staff       (20)        0 2023-07-05 16:05:24.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser/_tests/__init__.py
--rw-r--r--   0 kharrington   (503) staff       (20)     1256 2023-07-05 16:05:24.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser/_tests/test_widget.py
--rw-r--r--   0 kharrington   (503) staff       (20)     6682 2023-07-05 20:26:09.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser/_widget.py
--rw-r--r--   0 kharrington   (503) staff       (20)      350 2023-07-05 20:19:13.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser/napari.yaml
-drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-05 20:39:01.050443 napari-workshop-browser-0.0.1/src/napari_workshop_browser.egg-info/
--rw-r--r--   0 kharrington   (503) staff       (20)     4077 2023-07-05 20:39:01.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser.egg-info/PKG-INFO
--rw-r--r--   0 kharrington   (503) staff       (20)      578 2023-07-05 20:39:01.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser.egg-info/SOURCES.txt
--rw-r--r--   0 kharrington   (503) staff       (20)        1 2023-07-05 20:39:01.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser.egg-info/dependency_links.txt
--rw-r--r--   0 kharrington   (503) staff       (20)       80 2023-07-05 20:39:01.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser.egg-info/entry_points.txt
--rw-r--r--   0 kharrington   (503) staff       (20)       93 2023-07-05 20:39:01.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser.egg-info/requires.txt
--rw-r--r--   0 kharrington   (503) staff       (20)       24 2023-07-05 20:39:01.000000 napari-workshop-browser-0.0.1/src/napari_workshop_browser.egg-info/top_level.txt
+drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-23 18:46:18.775063 napari-workshop-browser-0.0.2/
+-rw-r--r--   0 kharrington   (503) staff       (20)     1490 2023-07-05 16:02:24.000000 napari-workshop-browser-0.0.2/LICENSE
+-rw-r--r--   0 kharrington   (503) staff       (20)       96 2023-07-05 16:02:24.000000 napari-workshop-browser-0.0.2/MANIFEST.in
+-rw-r--r--   0 kharrington   (503) staff       (20)     4501 2023-07-23 18:46:18.775152 napari-workshop-browser-0.0.2/PKG-INFO
+-rw-r--r--   0 kharrington   (503) staff       (20)     3201 2023-07-18 16:13:35.000000 napari-workshop-browser-0.0.2/README.md
+-rw-r--r--   0 kharrington   (503) staff       (20)     1177 2023-07-05 16:02:24.000000 napari-workshop-browser-0.0.2/pyproject.toml
+-rw-r--r--   0 kharrington   (503) staff       (20)     1821 2023-07-23 18:46:18.775537 napari-workshop-browser-0.0.2/setup.cfg
+drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-23 18:46:18.772501 napari-workshop-browser-0.0.2/src/
+drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-23 18:46:18.773797 napari-workshop-browser-0.0.2/src/napari_workshop_browser/
+-rw-r--r--   0 kharrington   (503) staff       (20)       95 2023-07-23 18:45:56.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser/__init__.py
+drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-23 18:46:18.774941 napari-workshop-browser-0.0.2/src/napari_workshop_browser/_tests/
+-rw-r--r--   0 kharrington   (503) staff       (20)        0 2023-07-05 16:02:24.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser/_tests/__init__.py
+-rw-r--r--   0 kharrington   (503) staff       (20)      666 2023-07-18 16:13:35.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser/_tests/test_widget.py
+-rw-r--r--   0 kharrington   (503) staff       (20)     6951 2023-07-23 18:40:22.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser/_widget.py
+-rw-r--r--   0 kharrington   (503) staff       (20)      350 2023-07-18 16:13:35.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser/napari.yaml
+drwxr-xr-x   0 kharrington   (503) staff       (20)        0 2023-07-23 18:46:18.774680 napari-workshop-browser-0.0.2/src/napari_workshop_browser.egg-info/
+-rw-r--r--   0 kharrington   (503) staff       (20)     4501 2023-07-23 18:46:18.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser.egg-info/PKG-INFO
+-rw-r--r--   0 kharrington   (503) staff       (20)      578 2023-07-23 18:46:18.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser.egg-info/SOURCES.txt
+-rw-r--r--   0 kharrington   (503) staff       (20)        1 2023-07-23 18:46:18.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser.egg-info/dependency_links.txt
+-rw-r--r--   0 kharrington   (503) staff       (20)       80 2023-07-23 18:46:18.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser.egg-info/entry_points.txt
+-rw-r--r--   0 kharrington   (503) staff       (20)      117 2023-07-23 18:46:18.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser.egg-info/requires.txt
+-rw-r--r--   0 kharrington   (503) staff       (20)       24 2023-07-23 18:46:18.000000 napari-workshop-browser-0.0.2/src/napari_workshop_browser.egg-info/top_level.txt
```

### Comparing `napari-workshop-browser-0.0.1/LICENSE` & `napari-workshop-browser-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `napari-workshop-browser-0.0.1/PKG-INFO` & `napari-workshop-browser-0.0.2/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: napari-workshop-browser
-Version: 0.0.1
+Version: 0.0.2
 Summary: A plugin to browse and follow napari workshops
 Home-page: https://github.com/kephale/napari-workshop-browser
 Author: Kyle Harrington
 Author-email: napari@kyleharrington.com
 License: BSD-3-Clause
 Project-URL: Bug Tracker, https://github.com/kephale/napari-workshop-browser/issues
 Project-URL: Documentation, https://github.com/kephale/napari-workshop-browser#README.md
@@ -46,14 +46,23 @@
 Don't miss the full getting started guide to set up your new package:
 https://github.com/napari/cookiecutter-napari-plugin#getting-started
 
 and review the napari docs for plugin developers:
 https://napari.org/stable/plugins/index.html
 -->
 
+## How to use this
+
+1. Download napari as an app (e.g. the 0.4.18 release candidates here: https://github.com/napari/packaging/actions/runs/5410466633 or a nightly build from here: https://github.com/napari/napari/releases/tag/latest)
+2. Open napari
+3. Select `Plugins \ Plugin Manager`
+4. Install this plugin, and restart napari.
+6. Run this plugin and enter the URL of your workshop's zip file
+7. Click `Launch workshop`
+
 ## Installation
 
 You can install `napari-workshop-browser` via [pip]:
 
     pip install napari-workshop-browser
```

### Comparing `napari-workshop-browser-0.0.1/README.md` & `napari-workshop-browser-0.0.2/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -17,14 +17,23 @@
 Don't miss the full getting started guide to set up your new package:
 https://github.com/napari/cookiecutter-napari-plugin#getting-started
 
 and review the napari docs for plugin developers:
 https://napari.org/stable/plugins/index.html
 -->
 
+## How to use this
+
+1. Download napari as an app (e.g. the 0.4.18 release candidates here: https://github.com/napari/packaging/actions/runs/5410466633 or a nightly build from here: https://github.com/napari/napari/releases/tag/latest)
+2. Open napari
+3. Select `Plugins \ Plugin Manager`
+4. Install this plugin, and restart napari.
+6. Run this plugin and enter the URL of your workshop's zip file
+7. Click `Launch workshop`
+
 ## Installation
 
 You can install `napari-workshop-browser` via [pip]:
 
     pip install napari-workshop-browser
```

### Comparing `napari-workshop-browser-0.0.1/pyproject.toml` & `napari-workshop-browser-0.0.2/pyproject.toml`

 * *Files identical despite different names*

### Comparing `napari-workshop-browser-0.0.1/setup.cfg` & `napari-workshop-browser-0.0.2/setup.cfg`

 * *Files 6% similar despite different names*

```diff
@@ -32,14 +32,17 @@
 packages = find:
 install_requires = 
 	numpy
 	superqt
 	qtpy
 	notebook
 	jupytext
+	napari
+	appdirs
+	requests
 python_requires = >=3.8
 include_package_data = True
 package_dir = 
 	=src
 
 [options.packages.find]
 where = src
```

### Comparing `napari-workshop-browser-0.0.1/src/napari_workshop_browser/_widget.py` & `napari-workshop-browser-0.0.2/src/napari_workshop_browser/_widget.py`

 * *Files 6% similar despite different names*

```diff
@@ -64,16 +64,22 @@
     temp_dir = os.path.join(cache_dir, "temp_unzip")
     os.makedirs(temp_dir, exist_ok=True)
     print(f"Temporary directory: {temp_dir}")
 
     try:
         # Download the zip file
         zip_file_path = os.path.join(temp_dir, "downloaded_file.zip")
-        download_file(url, zip_file_path)
-        print("File successfully downloaded.")
+
+        # Check if this is a URL, if so download
+        if url.startswith("https"):
+            download_file(url, zip_file_path)
+            print("File successfully downloaded.")
+        else:
+            # Otherwise we assume the URL is a local zip path
+            zip_file_path = url
 
         # Extract the zip file
         unzip_file(zip_file_path, temp_dir)
         print("File successfully unzipped.")
 
         return temp_dir
 
@@ -127,15 +133,14 @@
         label.setText("Workshop version")
         self.layout().addWidget(label)
         self.layout().addWidget(self.napari_workshop_template)
 
         self.layout().addWidget(btn)
 
     def _on_click(self):
-        print("napari has", len(self.viewer.layers), "layers")
         self.run()
 
     def run(self):
         # Hide the original window. This is really wasteful.
         self.viewer.window._qt_window.hide()
 
         from notebook import notebookapp
@@ -201,14 +206,20 @@
             except Exception as e:
                 print(
                     "An error occurred while launching Jupyter Notebook:",
                     str(e),
                 )
 
         worker = launch_jupyter_notebook()
+
+        def restore_napari():
+            self.viewer.window._qt_window.show()
+
+        worker.finished.connect(restore_napari)
+
         worker.start()
 
 
 if __name__ == "__main__":
     import napari
 
     viewer = napari.Viewer()
```

### Comparing `napari-workshop-browser-0.0.1/src/napari_workshop_browser.egg-info/PKG-INFO` & `napari-workshop-browser-0.0.2/src/napari_workshop_browser.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: napari-workshop-browser
-Version: 0.0.1
+Version: 0.0.2
 Summary: A plugin to browse and follow napari workshops
 Home-page: https://github.com/kephale/napari-workshop-browser
 Author: Kyle Harrington
 Author-email: napari@kyleharrington.com
 License: BSD-3-Clause
 Project-URL: Bug Tracker, https://github.com/kephale/napari-workshop-browser/issues
 Project-URL: Documentation, https://github.com/kephale/napari-workshop-browser#README.md
@@ -46,14 +46,23 @@
 Don't miss the full getting started guide to set up your new package:
 https://github.com/napari/cookiecutter-napari-plugin#getting-started
 
 and review the napari docs for plugin developers:
 https://napari.org/stable/plugins/index.html
 -->
 
+## How to use this
+
+1. Download napari as an app (e.g. the 0.4.18 release candidates here: https://github.com/napari/packaging/actions/runs/5410466633 or a nightly build from here: https://github.com/napari/napari/releases/tag/latest)
+2. Open napari
+3. Select `Plugins \ Plugin Manager`
+4. Install this plugin, and restart napari.
+6. Run this plugin and enter the URL of your workshop's zip file
+7. Click `Launch workshop`
+
 ## Installation
 
 You can install `napari-workshop-browser` via [pip]:
 
     pip install napari-workshop-browser
```

### Comparing `napari-workshop-browser-0.0.1/src/napari_workshop_browser.egg-info/SOURCES.txt` & `napari-workshop-browser-0.0.2/src/napari_workshop_browser.egg-info/SOURCES.txt`

 * *Files identical despite different names*

