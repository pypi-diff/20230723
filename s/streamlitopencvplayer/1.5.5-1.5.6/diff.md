# Comparing `tmp/streamlitopencvplayer-1.5.5.tar.gz` & `tmp/streamlitopencvplayer-1.5.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "streamlitopencvplayer-1.5.5.tar", last modified: Sun Jul 23 21:23:22 2023, max compression
+gzip compressed data, was "streamlitopencvplayer-1.5.6.tar", last modified: Sun Jul 23 21:32:54 2023, max compression
```

## Comparing `streamlitopencvplayer-1.5.5.tar` & `streamlitopencvplayer-1.5.6.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 21:23:22.534446 streamlitopencvplayer-1.5.5/
--rw-rw-rw-   0        0        0      419 2023-07-23 21:23:22.532383 streamlitopencvplayer-1.5.5/PKG-INFO
--rw-rw-rw-   0        0        0      705 2023-07-10 16:34:21.000000 streamlitopencvplayer-1.5.5/README.md
--rw-rw-rw-   0        0        0       42 2023-07-23 21:23:22.535519 streamlitopencvplayer-1.5.5/setup.cfg
--rw-rw-rw-   0        0        0      934 2023-07-23 21:23:16.000000 streamlitopencvplayer-1.5.5/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 21:23:22.500481 streamlitopencvplayer-1.5.5/streamlitopencvplayer/
--rw-rw-rw-   0        0        0        0 2023-05-22 10:55:16.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer/__init__.py
--rw-rw-rw-   0        0        0     8610 2023-07-23 21:23:11.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer/app.py
-drwxrwxrwx   0        0        0        0 2023-07-23 21:23:22.519924 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/
--rw-rw-rw-   0        0        0      419 2023-07-23 21:23:22.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      291 2023-07-23 21:23:22.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 21:23:22.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       27 2023-07-23 21:23:22.000000 streamlitopencvplayer-1.5.5/streamlitopencvplayer.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 21:23:22.527379 streamlitopencvplayer-1.5.5/test/
--rw-rw-rw-   0        0        0        0 2023-05-22 15:15:43.000000 streamlitopencvplayer-1.5.5/test/__init__.py
--rw-rw-rw-   0        0        0     1633 2023-07-16 23:22:17.000000 streamlitopencvplayer-1.5.5/test/test.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:32:54.465499 streamlitopencvplayer-1.5.6/
+-rw-rw-rw-   0        0        0      419 2023-07-23 21:32:54.463296 streamlitopencvplayer-1.5.6/PKG-INFO
+-rw-rw-rw-   0        0        0      705 2023-07-10 16:34:21.000000 streamlitopencvplayer-1.5.6/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 21:32:54.465499 streamlitopencvplayer-1.5.6/setup.cfg
+-rw-rw-rw-   0        0        0      934 2023-07-23 21:32:48.000000 streamlitopencvplayer-1.5.6/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:32:54.432676 streamlitopencvplayer-1.5.6/streamlitopencvplayer/
+-rw-rw-rw-   0        0        0        0 2023-05-22 10:55:16.000000 streamlitopencvplayer-1.5.6/streamlitopencvplayer/__init__.py
+-rw-rw-rw-   0        0        0     8225 2023-07-23 21:30:10.000000 streamlitopencvplayer-1.5.6/streamlitopencvplayer/app.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:32:54.452299 streamlitopencvplayer-1.5.6/streamlitopencvplayer.egg-info/
+-rw-rw-rw-   0        0        0      419 2023-07-23 21:32:54.000000 streamlitopencvplayer-1.5.6/streamlitopencvplayer.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      291 2023-07-23 21:32:54.000000 streamlitopencvplayer-1.5.6/streamlitopencvplayer.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 21:32:54.000000 streamlitopencvplayer-1.5.6/streamlitopencvplayer.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       27 2023-07-23 21:32:54.000000 streamlitopencvplayer-1.5.6/streamlitopencvplayer.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 21:32:54.458635 streamlitopencvplayer-1.5.6/test/
+-rw-rw-rw-   0        0        0        0 2023-05-22 15:15:43.000000 streamlitopencvplayer-1.5.6/test/__init__.py
+-rw-rw-rw-   0        0        0     1633 2023-07-16 23:22:17.000000 streamlitopencvplayer-1.5.6/test/test.py
```

### Comparing `streamlitopencvplayer-1.5.5/README.md` & `streamlitopencvplayer-1.5.6/README.md`

 * *Files identical despite different names*

### Comparing `streamlitopencvplayer-1.5.5/setup.py` & `streamlitopencvplayer-1.5.6/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION = '1.5.5' 
+VERSION = '1.5.6' 
 DESCRIPTION = 'Streamlit Opencv player'
 LONG_DESCRIPTION = 'Streamlit Opencv Player is a video player written in python for easy video playback and frames management using OpenCV'
 
 # Setting up
 setup(
        # the name must match the folder name 'verysimplemodule'
         name="streamlitopencvplayer",
```

### Comparing `streamlitopencvplayer-1.5.5/streamlitopencvplayer/app.py` & `streamlitopencvplayer-1.5.6/streamlitopencvplayer/app.py`

 * *Files 13% similar despite different names*

```diff
@@ -24,23 +24,18 @@
     # Display the frame with detections
     stframe.image(output, caption='', width=500)
     time.sleep(0.05)
 
 
 def display_video(video_path, json_file):
     # Check if video_url variables exists in session state
-    if "name_vid_old" not in st.session_state and "name_vid_sel" not in st.session_state:
-        if "capture" not in st.session_state:
+    if "capture" not in st.session_state:
             # Open the video file
             st.session_state['capture'] = cv2.VideoCapture(video_path)
-    else:
-        # Check if the video URL has changed
-        if st.session_state['name_vid_old'] != st.session_state['name_vid_sel']:
-            st.session_state['capture'] = cv2.VideoCapture(video_path)
-            st.session_state['name_vid_old'] = st.session_state['name_vid_sel']
+
 
 
     # Check if "fps" variable exists in session state
     if "fps" not in st.session_state:
         st.session_state['fps'] = st.session_state['capture'].get(
             cv2.CAP_PROP_FPS)
     if not st.session_state["capture"].isOpened():
```

### Comparing `streamlitopencvplayer-1.5.5/test/test.py` & `streamlitopencvplayer-1.5.6/test/test.py`

 * *Files identical despite different names*

