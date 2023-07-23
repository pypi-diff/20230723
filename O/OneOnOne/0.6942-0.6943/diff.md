# Comparing `tmp/OneOnOne-0.6942.tar.gz` & `tmp/OneOnOne-0.6943.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "OneOnOne-0.6942.tar", last modified: Sun Jul 23 18:15:22 2023, max compression
+gzip compressed data, was "OneOnOne-0.6943.tar", last modified: Sun Jul 23 18:19:53 2023, max compression
```

## Comparing `OneOnOne-0.6942.tar` & `OneOnOne-0.6943.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:15:22.346150 OneOnOne-0.6942/
--rw-r--r--   0 sohinib    (501) staff       (20)     1076 2023-07-10 14:29:42.000000 OneOnOne-0.6942/LICENSE
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:15:22.340398 OneOnOne-0.6942/OneOnOne/
--rw-r--r--   0 sohinib    (501) staff       (20)    52629 2023-07-23 18:15:07.000000 OneOnOne-0.6942/OneOnOne/__init__.py
--rw-r--r--   0 sohinib    (501) staff       (20)  3312680 2023-07-07 06:05:06.000000 OneOnOne-0.6942/OneOnOne/classes.py
--rw-r--r--   0 sohinib    (501) staff       (20)    13595 2023-07-19 15:12:53.000000 OneOnOne-0.6942/OneOnOne/classification.py
--rw-r--r--   0 sohinib    (501) staff       (20)     5894 2023-07-22 03:02:07.000000 OneOnOne-0.6942/OneOnOne/contextdecider.py
--rw-r--r--   0 sohinib    (501) staff       (20)      936 2023-07-19 15:12:54.000000 OneOnOne-0.6942/OneOnOne/htmlparser.py
--rw-r--r--   0 sohinib    (501) staff       (20)     3047 2023-07-19 17:26:04.000000 OneOnOne-0.6942/OneOnOne/questionanswer.py
--rw-r--r--   0 sohinib    (501) staff       (20)    20836 2023-07-19 15:12:54.000000 OneOnOne-0.6942/OneOnOne/sampling.py
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:15:22.345134 OneOnOne-0.6942/OneOnOne.egg-info/
--rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:15:22.000000 OneOnOne-0.6942/OneOnOne.egg-info/PKG-INFO
--rw-r--r--   0 sohinib    (501) staff       (20)      351 2023-07-23 18:15:22.000000 OneOnOne-0.6942/OneOnOne.egg-info/SOURCES.txt
--rw-r--r--   0 sohinib    (501) staff       (20)        1 2023-07-23 18:15:22.000000 OneOnOne-0.6942/OneOnOne.egg-info/dependency_links.txt
--rw-r--r--   0 sohinib    (501) staff       (20)      139 2023-07-23 18:15:22.000000 OneOnOne-0.6942/OneOnOne.egg-info/requires.txt
--rw-r--r--   0 sohinib    (501) staff       (20)        9 2023-07-23 18:15:22.000000 OneOnOne-0.6942/OneOnOne.egg-info/top_level.txt
--rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:15:22.345684 OneOnOne-0.6942/PKG-INFO
--rw-r--r--   0 sohinib    (501) staff       (20)     3395 2023-07-22 18:26:11.000000 OneOnOne-0.6942/README.md
--rw-r--r--   0 sohinib    (501) staff       (20)       38 2023-07-23 18:15:22.346306 OneOnOne-0.6942/setup.cfg
--rw-r--r--   0 sohinib    (501) staff       (20)     1941 2023-07-23 18:15:16.000000 OneOnOne-0.6942/setup.py
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:19:53.335798 OneOnOne-0.6943/
+-rw-r--r--   0 sohinib    (501) staff       (20)     1076 2023-07-10 14:29:42.000000 OneOnOne-0.6943/LICENSE
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:19:53.328973 OneOnOne-0.6943/OneOnOne/
+-rw-r--r--   0 sohinib    (501) staff       (20)    52640 2023-07-23 18:19:42.000000 OneOnOne-0.6943/OneOnOne/__init__.py
+-rw-r--r--   0 sohinib    (501) staff       (20)  3312680 2023-07-07 06:05:06.000000 OneOnOne-0.6943/OneOnOne/classes.py
+-rw-r--r--   0 sohinib    (501) staff       (20)    13595 2023-07-19 15:12:53.000000 OneOnOne-0.6943/OneOnOne/classification.py
+-rw-r--r--   0 sohinib    (501) staff       (20)     5894 2023-07-22 03:02:07.000000 OneOnOne-0.6943/OneOnOne/contextdecider.py
+-rw-r--r--   0 sohinib    (501) staff       (20)      936 2023-07-19 15:12:54.000000 OneOnOne-0.6943/OneOnOne/htmlparser.py
+-rw-r--r--   0 sohinib    (501) staff       (20)     3047 2023-07-19 17:26:04.000000 OneOnOne-0.6943/OneOnOne/questionanswer.py
+-rw-r--r--   0 sohinib    (501) staff       (20)    20836 2023-07-19 15:12:54.000000 OneOnOne-0.6943/OneOnOne/sampling.py
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:19:53.334018 OneOnOne-0.6943/OneOnOne.egg-info/
+-rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:19:53.000000 OneOnOne-0.6943/OneOnOne.egg-info/PKG-INFO
+-rw-r--r--   0 sohinib    (501) staff       (20)      351 2023-07-23 18:19:53.000000 OneOnOne-0.6943/OneOnOne.egg-info/SOURCES.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)        1 2023-07-23 18:19:53.000000 OneOnOne-0.6943/OneOnOne.egg-info/dependency_links.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)      139 2023-07-23 18:19:53.000000 OneOnOne-0.6943/OneOnOne.egg-info/requires.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)        9 2023-07-23 18:19:53.000000 OneOnOne-0.6943/OneOnOne.egg-info/top_level.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:19:53.334791 OneOnOne-0.6943/PKG-INFO
+-rw-r--r--   0 sohinib    (501) staff       (20)     3395 2023-07-22 18:26:11.000000 OneOnOne-0.6943/README.md
+-rw-r--r--   0 sohinib    (501) staff       (20)       38 2023-07-23 18:19:53.336055 OneOnOne-0.6943/setup.cfg
+-rw-r--r--   0 sohinib    (501) staff       (20)     1941 2023-07-23 18:19:42.000000 OneOnOne-0.6943/setup.py
```

### Comparing `OneOnOne-0.6942/LICENSE` & `OneOnOne-0.6943/LICENSE`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6942/OneOnOne/__init__.py` & `OneOnOne-0.6943/OneOnOne/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -48,15 +48,15 @@
 import pkgutil
 import requests, zipfile
 from io import BytesIO
 import gdown
 import imageio as iio
 from PIL import Image
 import cv2
-from keras.preprocessing.image import load_img, img_to_array
+from tensorflow.keras.preprocessing.image import load_img, img_to_array
 
 import warnings
 
 class PretrainedModel:
     def __init__(self, model_type="resnet50", dataset="cifar10", samplingtype="none"):
         warnings.filterwarnings("ignore")
```

### Comparing `OneOnOne-0.6942/OneOnOne/classes.py` & `OneOnOne-0.6943/OneOnOne/classes.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6942/OneOnOne/classification.py` & `OneOnOne-0.6943/OneOnOne/classification.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6942/OneOnOne/contextdecider.py` & `OneOnOne-0.6943/OneOnOne/contextdecider.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6942/OneOnOne/htmlparser.py` & `OneOnOne-0.6943/OneOnOne/htmlparser.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6942/OneOnOne/questionanswer.py` & `OneOnOne-0.6943/OneOnOne/questionanswer.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6942/OneOnOne/sampling.py` & `OneOnOne-0.6943/OneOnOne/sampling.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6942/OneOnOne.egg-info/PKG-INFO` & `OneOnOne-0.6943/OneOnOne.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OneOnOne
-Version: 0.6942
+Version: 0.6943
 Summary: A package for pre-trained image classification and context-decider for question-answering chatbots.
 Author: Sohini Bhattacharya
 Author-email: mail.sohinibhattacharya@gmail.com
 Keywords: python,image-classification,active-learning-sampling,question-answering,pre-trained models,tiny-image-net,cifar10
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `OneOnOne-0.6942/PKG-INFO` & `OneOnOne-0.6943/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OneOnOne
-Version: 0.6942
+Version: 0.6943
 Summary: A package for pre-trained image classification and context-decider for question-answering chatbots.
 Author: Sohini Bhattacharya
 Author-email: mail.sohinibhattacharya@gmail.com
 Keywords: python,image-classification,active-learning-sampling,question-answering,pre-trained models,tiny-image-net,cifar10
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `OneOnOne-0.6942/README.md` & `OneOnOne-0.6943/README.md`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6942/setup.py` & `OneOnOne-0.6943/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION=0.6942
+VERSION=0.6943
 
 DESCRIPTION="A package for pre-trained image classification and context-decider for question-answering chatbots."
 LONG_DESCRIPTION="Your one-stop destination to utilize image-classification models with just one line of code. A library meant to simplify your life by providing you with pre-trained models like ResNet50, EfficientNetVB6, VGG19, etc. You can simply opt for training your own models from scratch by just tweaking a few values. If you want to try popular active-learning sampling methods on image classification, no need to worry! This library has got you covered. Along with that for simple-bridging and basic into NLP, we have context-deciders, HTML parsers and simple chatbot object classes, to create an interface similar to Google Lens. You input an image or item that you are curious about and you can ask one-on-one questions from the chatbot. This is made possible by using the tiny imagenet dataset. This library is being actively updated and new features are being added frequently. New datasets and pre-trained models will be updated soon. Feel free to share your feedback! I would really appreciate it!"
 CLASSIFIERS=[
     'Development Status :: 5 - Production/Stable',
     'Intended Audience :: Education',
     'License :: OSI Approved :: MIT License',
```

