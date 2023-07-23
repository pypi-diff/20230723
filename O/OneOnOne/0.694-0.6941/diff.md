# Comparing `tmp/OneOnOne-0.694.tar.gz` & `tmp/OneOnOne-0.6941.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "OneOnOne-0.694.tar", last modified: Sun Jul 23 17:57:17 2023, max compression
+gzip compressed data, was "OneOnOne-0.6941.tar", last modified: Sun Jul 23 18:05:40 2023, max compression
```

## Comparing `OneOnOne-0.694.tar` & `OneOnOne-0.6941.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 17:57:17.055038 OneOnOne-0.694/
--rw-r--r--   0 sohinib    (501) staff       (20)     1076 2023-07-10 14:29:42.000000 OneOnOne-0.694/LICENSE
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 17:57:17.035775 OneOnOne-0.694/OneOnOne/
--rw-r--r--   0 sohinib    (501) staff       (20)    52459 2023-07-23 17:57:02.000000 OneOnOne-0.694/OneOnOne/__init__.py
--rw-r--r--   0 sohinib    (501) staff       (20)  3312680 2023-07-07 06:05:06.000000 OneOnOne-0.694/OneOnOne/classes.py
--rw-r--r--   0 sohinib    (501) staff       (20)    13595 2023-07-19 15:12:53.000000 OneOnOne-0.694/OneOnOne/classification.py
--rw-r--r--   0 sohinib    (501) staff       (20)     5894 2023-07-22 03:02:07.000000 OneOnOne-0.694/OneOnOne/contextdecider.py
--rw-r--r--   0 sohinib    (501) staff       (20)      936 2023-07-19 15:12:54.000000 OneOnOne-0.694/OneOnOne/htmlparser.py
--rw-r--r--   0 sohinib    (501) staff       (20)     3047 2023-07-19 17:26:04.000000 OneOnOne-0.694/OneOnOne/questionanswer.py
--rw-r--r--   0 sohinib    (501) staff       (20)    20836 2023-07-19 15:12:54.000000 OneOnOne-0.694/OneOnOne/sampling.py
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 17:57:17.049615 OneOnOne-0.694/OneOnOne.egg-info/
--rw-r--r--   0 sohinib    (501) staff       (20)     1577 2023-07-23 17:57:16.000000 OneOnOne-0.694/OneOnOne.egg-info/PKG-INFO
--rw-r--r--   0 sohinib    (501) staff       (20)      351 2023-07-23 17:57:16.000000 OneOnOne-0.694/OneOnOne.egg-info/SOURCES.txt
--rw-r--r--   0 sohinib    (501) staff       (20)        1 2023-07-23 17:57:16.000000 OneOnOne-0.694/OneOnOne.egg-info/dependency_links.txt
--rw-r--r--   0 sohinib    (501) staff       (20)      139 2023-07-23 17:57:16.000000 OneOnOne-0.694/OneOnOne.egg-info/requires.txt
--rw-r--r--   0 sohinib    (501) staff       (20)        9 2023-07-23 17:57:16.000000 OneOnOne-0.694/OneOnOne.egg-info/top_level.txt
--rw-r--r--   0 sohinib    (501) staff       (20)     1577 2023-07-23 17:57:17.052529 OneOnOne-0.694/PKG-INFO
--rw-r--r--   0 sohinib    (501) staff       (20)     3395 2023-07-22 18:26:11.000000 OneOnOne-0.694/README.md
--rw-r--r--   0 sohinib    (501) staff       (20)       38 2023-07-23 17:57:17.055612 OneOnOne-0.694/setup.cfg
--rw-r--r--   0 sohinib    (501) staff       (20)     1940 2023-07-23 17:57:07.000000 OneOnOne-0.694/setup.py
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:05:40.677526 OneOnOne-0.6941/
+-rw-r--r--   0 sohinib    (501) staff       (20)     1076 2023-07-10 14:29:42.000000 OneOnOne-0.6941/LICENSE
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:05:40.674091 OneOnOne-0.6941/OneOnOne/
+-rw-r--r--   0 sohinib    (501) staff       (20)    52522 2023-07-23 18:05:29.000000 OneOnOne-0.6941/OneOnOne/__init__.py
+-rw-r--r--   0 sohinib    (501) staff       (20)  3312680 2023-07-07 06:05:06.000000 OneOnOne-0.6941/OneOnOne/classes.py
+-rw-r--r--   0 sohinib    (501) staff       (20)    13595 2023-07-19 15:12:53.000000 OneOnOne-0.6941/OneOnOne/classification.py
+-rw-r--r--   0 sohinib    (501) staff       (20)     5894 2023-07-22 03:02:07.000000 OneOnOne-0.6941/OneOnOne/contextdecider.py
+-rw-r--r--   0 sohinib    (501) staff       (20)      936 2023-07-19 15:12:54.000000 OneOnOne-0.6941/OneOnOne/htmlparser.py
+-rw-r--r--   0 sohinib    (501) staff       (20)     3047 2023-07-19 17:26:04.000000 OneOnOne-0.6941/OneOnOne/questionanswer.py
+-rw-r--r--   0 sohinib    (501) staff       (20)    20836 2023-07-19 15:12:54.000000 OneOnOne-0.6941/OneOnOne/sampling.py
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:05:40.676744 OneOnOne-0.6941/OneOnOne.egg-info/
+-rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:05:40.000000 OneOnOne-0.6941/OneOnOne.egg-info/PKG-INFO
+-rw-r--r--   0 sohinib    (501) staff       (20)      351 2023-07-23 18:05:40.000000 OneOnOne-0.6941/OneOnOne.egg-info/SOURCES.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)        1 2023-07-23 18:05:40.000000 OneOnOne-0.6941/OneOnOne.egg-info/dependency_links.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)      139 2023-07-23 18:05:40.000000 OneOnOne-0.6941/OneOnOne.egg-info/requires.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)        9 2023-07-23 18:05:40.000000 OneOnOne-0.6941/OneOnOne.egg-info/top_level.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:05:40.677152 OneOnOne-0.6941/PKG-INFO
+-rw-r--r--   0 sohinib    (501) staff       (20)     3395 2023-07-22 18:26:11.000000 OneOnOne-0.6941/README.md
+-rw-r--r--   0 sohinib    (501) staff       (20)       38 2023-07-23 18:05:40.677647 OneOnOne-0.6941/setup.cfg
+-rw-r--r--   0 sohinib    (501) staff       (20)     1941 2023-07-23 18:05:34.000000 OneOnOne-0.6941/setup.py
```

### Comparing `OneOnOne-0.694/LICENSE` & `OneOnOne-0.6941/LICENSE`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.694/OneOnOne/__init__.py` & `OneOnOne-0.6941/OneOnOne/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -47,14 +47,15 @@
 from tqdm import keras
 import pkgutil
 import requests, zipfile
 from io import BytesIO
 import gdown
 import imageio as iio
 from PIL import Image
+import cv2
 
 import warnings
 
 class PretrainedModel:
     def __init__(self, model_type="resnet50", dataset="cifar10", samplingtype="none"):
         warnings.filterwarnings("ignore")
 
@@ -1036,14 +1037,15 @@
                                           samplingtype=self.samplingtype)
             self.contextmodel = pretrained.get_model()
 
         if self.user_input:
             path=input("Please enter image path in the current directory (str):    ")
             img = Image.open(os.getcwd()+f"{path}")
             img.show()
+            img = cv2.imread(os.getcwd()+f"{path}")
             # img = iio.imread(os.getcwd()+f"{path}")
             self.pred = self.contextmodel.predict_generator(img)
         else:
             # random.randint(1, 3000)
             self.pred = self.contextmodel.predict_generator(self.val_it, random.randint(1, 16))
 
     def preprocess_image_input(self,input_images):
```

### Comparing `OneOnOne-0.694/OneOnOne/classes.py` & `OneOnOne-0.6941/OneOnOne/classes.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.694/OneOnOne/classification.py` & `OneOnOne-0.6941/OneOnOne/classification.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.694/OneOnOne/contextdecider.py` & `OneOnOne-0.6941/OneOnOne/contextdecider.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.694/OneOnOne/htmlparser.py` & `OneOnOne-0.6941/OneOnOne/htmlparser.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.694/OneOnOne/questionanswer.py` & `OneOnOne-0.6941/OneOnOne/questionanswer.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.694/OneOnOne/sampling.py` & `OneOnOne-0.6941/OneOnOne/sampling.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.694/OneOnOne.egg-info/PKG-INFO` & `OneOnOne-0.6941/OneOnOne.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OneOnOne
-Version: 0.694
+Version: 0.6941
 Summary: A package for pre-trained image classification and context-decider for question-answering chatbots.
 Author: Sohini Bhattacharya
 Author-email: mail.sohinibhattacharya@gmail.com
 Keywords: python,image-classification,active-learning-sampling,question-answering,pre-trained models,tiny-image-net,cifar10
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `OneOnOne-0.694/PKG-INFO` & `OneOnOne-0.6941/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OneOnOne
-Version: 0.694
+Version: 0.6941
 Summary: A package for pre-trained image classification and context-decider for question-answering chatbots.
 Author: Sohini Bhattacharya
 Author-email: mail.sohinibhattacharya@gmail.com
 Keywords: python,image-classification,active-learning-sampling,question-answering,pre-trained models,tiny-image-net,cifar10
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `OneOnOne-0.694/README.md` & `OneOnOne-0.6941/README.md`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.694/setup.py` & `OneOnOne-0.6941/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION=0.694
+VERSION=0.6941
 
 DESCRIPTION="A package for pre-trained image classification and context-decider for question-answering chatbots."
 LONG_DESCRIPTION="Your one-stop destination to utilize image-classification models with just one line of code. A library meant to simplify your life by providing you with pre-trained models like ResNet50, EfficientNetVB6, VGG19, etc. You can simply opt for training your own models from scratch by just tweaking a few values. If you want to try popular active-learning sampling methods on image classification, no need to worry! This library has got you covered. Along with that for simple-bridging and basic into NLP, we have context-deciders, HTML parsers and simple chatbot object classes, to create an interface similar to Google Lens. You input an image or item that you are curious about and you can ask one-on-one questions from the chatbot. This is made possible by using the tiny imagenet dataset. This library is being actively updated and new features are being added frequently. New datasets and pre-trained models will be updated soon. Feel free to share your feedback! I would really appreciate it!"
 CLASSIFIERS=[
     'Development Status :: 5 - Production/Stable',
     'Intended Audience :: Education',
     'License :: OSI Approved :: MIT License',
```

