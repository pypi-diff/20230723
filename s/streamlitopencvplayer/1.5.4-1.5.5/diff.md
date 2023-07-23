# Comparing `tmp/streamlitopencvplayer-1.5.4.tar.gz` & `tmp/streamlitopencvplayer-1.5.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "streamlitopencvplayer-1.5.4.tar", last modified: Sun Jul 23 21:19:34 2023, max compression
+gzip compressed data, was "streamlitopencvplayer-1.5.5.tar", last modified: Sun Jul 23 21:23:22 2023, max compression
```

## Comparing `streamlitopencvplayer-1.5.4.tar` & `streamlitopencvplayer-1.5.5.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 21:19:34.732107 streamlitopencvplayer-1.5.4/
--rw-rw-rw-   0        0        0      419 2023-07-23 21:19:34.730108 streamlitopencvplayer-1.5.4/PKG-INFO
--rw-rw-rw-   0        0        0      705 2023-07-10 16:34:21.000000 streamlitopencvplayer-1.5.4/README.md
--rw-rw-rw-   0        0        0       42 2023-07-23 21:19:34.733108 streamlitopencvplayer-1.5.4/setup.cfg
--rw-rw-rw-   0        0        0      934 2023-07-23 21:19:30.000000 streamlitopencvplayer-1.5.4/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 21:19:34.698444 streamlitopencvplayer-1.5.4/streamlitopencvplayer/
--rw-rw-rw-   0        0        0        0 2023-05-22 10:55:16.000000 streamlitopencvplayer-1.5.4/streamlitopencvplayer/__init__.py
--rw-rw-rw-   0        0        0     8515 2023-07-23 21:19:23.000000 streamlitopencvplayer-1.5.4/streamlitopencvplayer/app.py
-drwxrwxrwx   0        0        0        0 2023-07-23 21:19:34.717997 streamlitopencvplayer-1.5.4/streamlitopencvplayer.egg-info/
--rw-rw-rw-   0        0        0      419 2023-07-23 21:19:34.000000 streamlitopencvplayer-1.5.4/streamlitopencvplayer.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      291 2023-07-23 21:19:34.000000 streamlitopencvplayer-1.5.4/streamlitopencvplayer.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 21:19:34.000000 streamlitopencvplayer-1.5.4/streamlitopencvplayer.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       27 2023-07-23 21:19:34.000000 streamlitopencvplayer-1.5.4/streamlitopencvplayer.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 21:19:34.725627 streamlitopencvplayer-1.5.4/test/
--rw-rw-rw-   0        0        0        0 2023-05-22 15:15:43.000000 streamlitopencvplayer-1.5.4/test/__init__.py
--rw-rw-rw-   0        0        0     1633 2023-07-16 23:22:17.000000 streamlitopencvplayer-1.5.4/test/test.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:23:22.534446 streamlitopencvplayer-1.5.5/
+-rw-rw-rw-   0        0        0      419 2023-07-23 21:23:22.532383 streamlitopencvplayer-1.5.5/PKG-INFO
+-rw-rw-rw-   0        0        0      705 2023-07-10 16:34:21.000000 streamlitopencvplayer-1.5.5/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 21:23:22.535519 streamlitopencvplayer-1.5.5/setup.cfg
+-rw-rw-rw-   0        0        0      934 2023-07-23 21:23:16.000000 streamlitopencvplayer-1.5.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:23:22.500481 streamlitopencvplayer-1.5.5/streamlitopencvplayer/
+-rw-rw-rw-   0        0        0        0 2023-05-22 10:55:16.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer/__init__.py
+-rw-rw-rw-   0        0        0     8610 2023-07-23 21:23:11.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer/app.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:23:22.519924 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/
+-rw-rw-rw-   0        0        0      419 2023-07-23 21:23:22.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      291 2023-07-23 21:23:22.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 21:23:22.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       27 2023-07-23 21:23:22.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 21:23:22.527379 streamlitopencvplayer-1.5.5/test/
+-rw-rw-rw-   0        0        0        0 2023-05-22 15:15:43.000000 streamlitopencvplayer-1.5.5/test/__init__.py
+-rw-rw-rw-   0        0        0     1633 2023-07-16 23:22:17.000000 streamlitopencvplayer-1.5.5/test/test.py
```

### Comparing `streamlitopencvplayer-1.5.4/README.md` & `streamlitopencvplayer-1.5.5/README.md`

 * *Files identical despite different names*

### Comparing `streamlitopencvplayer-1.5.4/setup.py` & `streamlitopencvplayer-1.5.5/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '1.5.4' 
+VERSION = '1.5.5' 
 DESCRIPTION = 'Streamlit Opencv player'
 LONG_DESCRIPTION = 'Streamlit Opencv Player is a video player written in python for easy video playback and frames management using OpenCV'
 
 # Setting up
 setup(
        # the name must match the folder name 'verysimplemodule'
         name="streamlitopencvplayer",
```

### Comparing `streamlitopencvplayer-1.5.4/streamlitopencvplayer/app.py` & `streamlitopencvplayer-1.5.5/streamlitopencvplayer/app.py`

 * *Files 5% similar despite different names*

```diff
@@ -88,14 +88,16 @@
     with column3:
         # Create buttons for alerts
         st.subheader('Alerts :')
         # Determine the number of buttons based on the number of alerts
         num_buttons = len(st.session_state['alerts'])
         # Create a dictionary to store the button values
         button_values = {f'{i}': 0 for i in range(num_buttons)}
+        st.write(len(st.session_state['alerts']))
+        st.write(st.session_state['data'])
 
         # Display the buttons and update their values
         for button_label, button_value in button_values.items():
             if st.button(str('Alert ')+button_label):
                 # Set the selected button to 1, others to 0
                 button_values = {label: 1 if label ==
                                  button_label else 0 for label in button_values}
```

### Comparing `streamlitopencvplayer-1.5.4/test/test.py` & `streamlitopencvplayer-1.5.5/test/test.py`

 * *Files identical despite different names*

